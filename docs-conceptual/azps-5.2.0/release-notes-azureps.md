---
title: Viktig information om Azure PowerShell
description: Lär dig mer om alla de senaste uppdateringarna för Azure PowerShell-modulerna.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 25d4df411c6df652170880c123e2fbdf24546193
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "96856639"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="cb43e-103">Viktig information om Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="cb43e-103">Azure PowerShell release notes</span></span>

## <a name="520---december-2020"></a><span data-ttu-id="cb43e-104">5.2.0 – December 2020</span><span class="sxs-lookup"><span data-stu-id="cb43e-104">5.2.0 - December 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cb43e-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb43e-105">Az.Accounts</span></span>
* <span data-ttu-id="cb43e-106">Det gick att parsa ExpiresOn-tiden från rådatatoken om den inte kunde hämtas från det underliggande biblioteket</span><span class="sxs-lookup"><span data-stu-id="cb43e-106">Managed to parse ExpiresOn time from raw token if could not get from underlying library</span></span>
* <span data-ttu-id="cb43e-107">Förbättrat varningsmeddelande om interaktiv autentisering inte är tillgängligt</span><span class="sxs-lookup"><span data-stu-id="cb43e-107">Improved warning message if Interactive authentication is unavailable</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="cb43e-108">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cb43e-108">Az.ApiManagement</span></span>
* <span data-ttu-id="cb43e-109">[Icke-bakåtkompatibel ändring] New-AzApiManagementProduct har som standard ingen prenumerationsgräns.</span><span class="sxs-lookup"><span data-stu-id="cb43e-109">[Breaking change] 'New-AzApiManagementProduct' by default has no subscription limit.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb43e-110">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb43e-110">Az.Compute</span></span>
* <span data-ttu-id="cb43e-111">Redigerade get-AzVm för att filtrera efter -Name innan du kontrollerar begränsning på grund av för många resurser.</span><span class="sxs-lookup"><span data-stu-id="cb43e-111">Edited Get-AzVm to filter by '-Name' prior to checking for throttling due to too many resources.</span></span> 
* <span data-ttu-id="cb43e-112">Ny cmdlet Start-AzVmssRollingExtensionUpgrade.</span><span class="sxs-lookup"><span data-stu-id="cb43e-112">New cmdlet 'Start-AzVmssRollingExtensionUpgrade'.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="cb43e-113">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="cb43e-113">Az.ContainerRegistry</span></span>
* <span data-ttu-id="cb43e-114">Parametern Name och värdet från pipeline-indata stöds för Get-AzContainerRegistryUsage [#13605]</span><span class="sxs-lookup"><span data-stu-id="cb43e-114">Supported parameter 'Name' for and value from pipeline input for 'Get-AzContainerRegistryUsage' [#13605]</span></span>
* <span data-ttu-id="cb43e-115">Korrigerade undantag för Connect-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="cb43e-115">Polished exceptions for 'Connect-AzContainerRegistry'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cb43e-116">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cb43e-116">Az.DataFactory</span></span>
* <span data-ttu-id="cb43e-117">Uppdaterade ADF .Net SDK-versionen till 4.13.0</span><span class="sxs-lookup"><span data-stu-id="cb43e-117">Updated ADF .Net SDK version to 4.13.0</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="cb43e-118">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="cb43e-118">Az.HealthcareApis</span></span>
* <span data-ttu-id="cb43e-119">Stöd har lagts till för kundhanterade nycklar</span><span class="sxs-lookup"><span data-stu-id="cb43e-119">Added support for customer managed keys</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cb43e-120">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cb43e-120">Az.IotHub</span></span>
* <span data-ttu-id="cb43e-121">Ett problem med SAS-token har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="cb43e-121">Fixed an issue of SAS token.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cb43e-122">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cb43e-122">Az.KeyVault</span></span>
* <span data-ttu-id="cb43e-123">Stöder All som ett alternativ när du ställer in åtkomstprinciper för nyckelvalv</span><span class="sxs-lookup"><span data-stu-id="cb43e-123">Supported 'all' as an option when setting key vault access policies</span></span>
* <span data-ttu-id="cb43e-124">Ny version av SecretManagement-modulen stöds [#13366]</span><span class="sxs-lookup"><span data-stu-id="cb43e-124">Supported new version of SecretManagement module [#13366]</span></span>
* <span data-ttu-id="cb43e-125">Stöder ByteArray, String, PSCredential och Hashtable för SecretValue i SecretManagementModule [#12190]</span><span class="sxs-lookup"><span data-stu-id="cb43e-125">Supported ByteArray, String, PSCredential and Hashtable for 'SecretValue' in SecretManagementModule [#12190]</span></span>
* <span data-ttu-id="cb43e-126">[Icke-bakåtkompatibel ändring] Omdesignat API-ytan för cmdletar som är relaterade till hanterad HSM.</span><span class="sxs-lookup"><span data-stu-id="cb43e-126">[Breaking change] redesigned the API surface of cmdlets related to managed HSM.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cb43e-127">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cb43e-127">Az.Monitor</span></span>
* <span data-ttu-id="cb43e-128">Parametern Rule i New-AzAutoscaleProfile har ändrats för att godkänna en tom lista.</span><span class="sxs-lookup"><span data-stu-id="cb43e-128">Changed parameter 'Rule' of 'New-AzAutoscaleProfile' to accept empty list.</span></span> <span data-ttu-id="cb43e-129">[#12903]</span><span class="sxs-lookup"><span data-stu-id="cb43e-129">[#12903]</span></span>
* <span data-ttu-id="cb43e-130">Nya cmdletar har lagts till för att stöda skapande av mer flexibla diagnostikinställningar:</span><span class="sxs-lookup"><span data-stu-id="cb43e-130">Added new cmdlets to support creating diagnostic settings more flexible:</span></span>
    * <span data-ttu-id="cb43e-131">Get-AzDiagnosticSettingCategory</span><span class="sxs-lookup"><span data-stu-id="cb43e-131">'Get-AzDiagnosticSettingCategory'</span></span>
    * <span data-ttu-id="cb43e-132">New-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="cb43e-132">'New-AzDiagnosticSetting'</span></span>
    * <span data-ttu-id="cb43e-133">New-AzDiagnosticDetailSetting</span><span class="sxs-lookup"><span data-stu-id="cb43e-133">'New-AzDiagnosticDetailSetting'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cb43e-134">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb43e-134">Az.RecoveryServices</span></span>
* <span data-ttu-id="cb43e-135">Ändrat hjälptext och parameteruppsättningsnamn till cmdleten Restore-AzRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="cb43e-135">Made help text and parameter set name changes to 'Restore-AzRecoveryServicesBackupItem' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb43e-136">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb43e-136">Az.Resources</span></span>
* <span data-ttu-id="cb43e-137">Stöd för parametern -Tag har lagts till i Set-AzTemplateSpec och New-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="cb43e-137">Added '-Tag' parameter support to 'Set-AzTemplateSpec' and 'New-AzTemplateSpec'</span></span>
* <span data-ttu-id="cb43e-138">Stöd för taggvisning har lagts till som standard för formatering av Mallspecifikationer</span><span class="sxs-lookup"><span data-stu-id="cb43e-138">Added Tag display support to default formatter for Template Specs</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="cb43e-139">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cb43e-139">Az.ServiceFabric</span></span>
* <span data-ttu-id="cb43e-140">Lade till exempel i Set-AzServiceFabricSetting med parametern SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="cb43e-140">Added example to 'Set-AzServiceFabricSetting' with SettingsSectionDescription param</span></span>
* <span data-ttu-id="cb43e-141">Uppdaterade programrelaterade cmdletar för att anropa att stöd endast finns för ARM-distribuerade resurser</span><span class="sxs-lookup"><span data-stu-id="cb43e-141">Updated application related cmdlets to call out that support is only for ARM deployed resources</span></span>
* <span data-ttu-id="cb43e-142">Markerat för cmdletarna Add-AzureRmServiceFabricClusterCertificate och Remove-AzureRmServiceFabricClusterCertificate med utfasningsklustercertifikat</span><span class="sxs-lookup"><span data-stu-id="cb43e-142">Marked for deprecation cluster cert cmdlets 'Add-AzureRmServiceFabricClusterCertificate' and 'Remove-AzureRmServiceFabricClusterCertificate'</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb43e-143">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb43e-143">Az.Sql</span></span>
* <span data-ttu-id="cb43e-144">Lade till SecondaryType till följande:</span><span class="sxs-lookup"><span data-stu-id="cb43e-144">Added SecondaryType to the following:</span></span> 
    - <span data-ttu-id="cb43e-145">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="cb43e-145">'New-AzSqlDatabase'</span></span>
    - <span data-ttu-id="cb43e-146">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="cb43e-146">'Set-AzSqlDatabase'</span></span>
    - <span data-ttu-id="cb43e-147">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="cb43e-147">'New-AzSqlDatabaseSecondary'</span></span>
* <span data-ttu-id="cb43e-148">Lade till HighAvailabilityReplicaCount till följande:</span><span class="sxs-lookup"><span data-stu-id="cb43e-148">Added HighAvailabilityReplicaCount to the following:</span></span> 
    - <span data-ttu-id="cb43e-149">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="cb43e-149">'New-AzSqlDatabase'</span></span>
    - <span data-ttu-id="cb43e-150">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="cb43e-150">'Set-AzSqlDatabase'</span></span>
* <span data-ttu-id="cb43e-151">Gjorde ReadReplicaCount till ett alias för HighAvailabilityReplicaCount i följande:</span><span class="sxs-lookup"><span data-stu-id="cb43e-151">Made ReadReplicaCount an alias of HighAvailabilityReplicaCount in the following:</span></span> 
    - <span data-ttu-id="cb43e-152">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="cb43e-152">'New-AzSqlDatabase'</span></span>
    - <span data-ttu-id="cb43e-153">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="cb43e-153">'Set-AzSqlDatabase'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cb43e-154">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb43e-154">Az.Storage</span></span>
* <span data-ttu-id="cb43e-155">Stöder överföring av Azure-filstorlek på upp till 4 TiB</span><span class="sxs-lookup"><span data-stu-id="cb43e-155">Supported upload Azure File size up to 4 TiB</span></span>
    - <span data-ttu-id="cb43e-156">”Set-AzStorageFileContent”</span><span class="sxs-lookup"><span data-stu-id="cb43e-156">'Set-AzStorageFileContent'</span></span>
* <span data-ttu-id="cb43e-157">Uppgraderade Azure.Storage.Blobs till 12.7.0</span><span class="sxs-lookup"><span data-stu-id="cb43e-157">Upgraded Azure.Storage.Blobs to 12.7.0</span></span>
* <span data-ttu-id="cb43e-158">Uppgraderade Azure.Storage.Files.Shares till 12.5.0</span><span class="sxs-lookup"><span data-stu-id="cb43e-158">Upgraded Azure.Storage.Files.Shares to 12.5.0</span></span>
* <span data-ttu-id="cb43e-159">Uppgraderade Azure.Storage.Files.DataLake till 12.5.0</span><span class="sxs-lookup"><span data-stu-id="cb43e-159">Upgraded Azure.Storage.Files.DataLake to 12.5.0</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="cb43e-160">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="cb43e-160">Az.StorageSync</span></span>
* <span data-ttu-id="cb43e-161">Principfunktionen för synkronisering av nivåer har lagts till med hämtningsprincip och lokalt cacheläge</span><span class="sxs-lookup"><span data-stu-id="cb43e-161">Added Sync tiering policy feature with download policy and local cache mode</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cb43e-162">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb43e-162">Az.Websites</span></span>
* <span data-ttu-id="cb43e-163">Förhindra dubbletter av åtkomstbegränsningsregler</span><span class="sxs-lookup"><span data-stu-id="cb43e-163">Prevent duplicate access restriction rules</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="cb43e-164">Tack till våra community-deltagare</span><span class="sxs-lookup"><span data-stu-id="cb43e-164">Thanks to our community contributors</span></span>
* <span data-ttu-id="cb43e-165">Andrew Dawson (@dawsonar802), uppdatera Get-AzKeyVaultCertificate.md – hämta certifikat och spara det som pfx-avsnitt som fungerar med PowerShell Core (#13557)</span><span class="sxs-lookup"><span data-stu-id="cb43e-165">Andrew Dawson (@dawsonar802), Update Get-AzKeyVaultCertificate.md - Get cert and save it as pfx section to work with PowerShell Core (#13557)</span></span>
* <span data-ttu-id="cb43e-166">@iviark, sjukvårds-API:er PowerShell BYOK-uppdateringar (#13518)</span><span class="sxs-lookup"><span data-stu-id="cb43e-166">@iviark, Healthcare APIs Powershell BYOK Updates (#13518)</span></span>
* <span data-ttu-id="cb43e-167">John Duckmanton (@johnduckmanton), korrigera stavning av TagPatchOperation (#13508)</span><span class="sxs-lookup"><span data-stu-id="cb43e-167">John Duckmanton (@johnduckmanton), Correct spelling of TagPatchOperation (#13508)</span></span>
* <span data-ttu-id="cb43e-168">Michael James (@mikejwhat)</span><span class="sxs-lookup"><span data-stu-id="cb43e-168">Michael James (@mikejwhat)</span></span>
  * <span data-ttu-id="cb43e-169">Hjälp till att fixa Get-AzLogicAppRunHistory (#13513)</span><span class="sxs-lookup"><span data-stu-id="cb43e-169">Get-AzLogicAppRunHistory Help Tidy (#13513)</span></span>
* <span data-ttu-id="cb43e-170">Richard de Zwart (@mountain65)</span><span class="sxs-lookup"><span data-stu-id="cb43e-170">Richard de Zwart (@mountain65)</span></span>
  * <span data-ttu-id="cb43e-171">Uppdatera Update-AzAppConfigurationStore.md (#13485)</span><span class="sxs-lookup"><span data-stu-id="cb43e-171">Update Update-AzAppConfigurationStore.md (#13485)</span></span>
  * <span data-ttu-id="cb43e-172">Uppdatera New-AzCosmosDBAccount.md (#13490)</span><span class="sxs-lookup"><span data-stu-id="cb43e-172">Update New-AzCosmosDBAccount.md (#13490)</span></span>
* <span data-ttu-id="cb43e-173">@SteppingRazor, New-AzApiManagementProduct: Ändra standardvärdet för parametern SubscriptionsLimit till None (#13457)</span><span class="sxs-lookup"><span data-stu-id="cb43e-173">@SteppingRazor, New-AzApiManagementProduct: Change SubscriptionsLimit parameter default value to None (#13457)</span></span>
* <span data-ttu-id="cb43e-174">Steve Burkett (@SteveBurkettNZ), korrigera skrivfel för parametern WorkspaceResourceId i exemplet (#13589)</span><span class="sxs-lookup"><span data-stu-id="cb43e-174">Steve Burkett (@SteveBurkettNZ), Fix Typo for WorkspaceResourceId parameter in example (#13589)</span></span>

## <a name="510---november-2020"></a><span data-ttu-id="cb43e-175">5.1.0 – November 2020</span><span class="sxs-lookup"><span data-stu-id="cb43e-175">5.1.0 - November 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cb43e-176">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb43e-176">Az.Accounts</span></span>
* <span data-ttu-id="cb43e-177">Korrigerade ett problem där TenantId kanske inte kan respekteras när ”Connect-AzAccount -DeviceCode” används [#13477]</span><span class="sxs-lookup"><span data-stu-id="cb43e-177">Fixed an issue that TenantId may be not respected if using 'Connect-AzAccount -DeviceCode'[#13477]</span></span>
* <span data-ttu-id="cb43e-178">Lade till en ny cmdlet: ”Get-AzAccessToken”</span><span class="sxs-lookup"><span data-stu-id="cb43e-178">Added new cmdlet 'Get-AzAccessToken'</span></span>
* <span data-ttu-id="cb43e-179">Korrigerade ett problem som uppstår om det inte går att komma åt sökvägen till användarprofilen</span><span class="sxs-lookup"><span data-stu-id="cb43e-179">Fixed an issue that error happens if user profile path is inaccessible</span></span>
* <span data-ttu-id="cb43e-180">Korrigerade ett problem som orsakar ett skriv-objektfel under Connect-AzAccount [#13419]</span><span class="sxs-lookup"><span data-stu-id="cb43e-180">Fixed an issue causing Write-Object error during Connect-AzAccount [#13419]</span></span>
* <span data-ttu-id="cb43e-181">Lade till parametern ”ContainerRegistryEndpointSuffix” för: ”Add-AzEnvironment”, ”Set-AzEnvironment”</span><span class="sxs-lookup"><span data-stu-id="cb43e-181">Added parameter 'ContainerRegistryEndpointSuffix' to: 'Add-AzEnvironment', 'Set-AzEnvironment'</span></span> 
* <span data-ttu-id="cb43e-182">Stöd för att avbryta inloggning genom att trycka på <kbd>CTRL</kbd>+<kbd>C</kbd></span><span class="sxs-lookup"><span data-stu-id="cb43e-182">Supported interrupting login by hitting <kbd>CTRL</kbd>+<kbd>C</kbd></span></span>
* <span data-ttu-id="cb43e-183">Korrigerade ett problem som gjorde att ”Connect-AzAccount -KeyVaultAccessToken” inte fungerade [#13127]</span><span class="sxs-lookup"><span data-stu-id="cb43e-183">Fixed an issue causing 'Connect-AzAccount -KeyVaultAccessToken' not working [#13127]</span></span>
* <span data-ttu-id="cb43e-184">Korrigerade null-referens och skiftlägesokänslig metod i ”Invoke-AzRestMethod”</span><span class="sxs-lookup"><span data-stu-id="cb43e-184">Fixed null reference and method case insensitive in 'Invoke-AzRestMethod'</span></span>

#### <a name="azaks"></a><span data-ttu-id="cb43e-185">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="cb43e-185">Az.Aks</span></span>
* <span data-ttu-id="cb43e-186">Korrigerade problemet att användaren inte kunde använda tjänstens huvudnamn för att skapa ett nytt Kubernetes-kluster.</span><span class="sxs-lookup"><span data-stu-id="cb43e-186">Fixed the issue that user cannot use service principal to create a new Kubernetes cluster.</span></span> <span data-ttu-id="cb43e-187">[#13012]</span><span class="sxs-lookup"><span data-stu-id="cb43e-187">[#13012]</span></span>

#### <a name="azappconfiguration"></a><span data-ttu-id="cb43e-188">Az.AppConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb43e-188">Az.AppConfiguration</span></span>
* <span data-ttu-id="cb43e-189">Allmän tillgänglighet för modulen ”Az.AppConfiguration”</span><span class="sxs-lookup"><span data-stu-id="cb43e-189">General availability of 'Az.AppConfiguration' module</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cb43e-190">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cb43e-190">Az.DataFactory</span></span>
* <span data-ttu-id="cb43e-191">Förbättrade felmeddelandet för kommandot ”New-AzDataFactoryV2LinkedServiceEncryptedCredential”</span><span class="sxs-lookup"><span data-stu-id="cb43e-191">Improved error message of 'New-AzDataFactoryV2LinkedServiceEncryptedCredential' command</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cb43e-192">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cb43e-192">Az.DataLakeStore</span></span>
* <span data-ttu-id="cb43e-193">Uppdaterade SDK för ADLS-dataplanen till 1.2.4-alpha.</span><span class="sxs-lookup"><span data-stu-id="cb43e-193">Updated ADLS dataplane SDK to 1.2.4-alpha.</span></span> <span data-ttu-id="cb43e-194">Ändringar: https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-124-alpha</span><span class="sxs-lookup"><span data-stu-id="cb43e-194">Changes:https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-124-alpha</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="cb43e-195">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="cb43e-195">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="cb43e-196">Lade till nya cmdletar för MSIX-paket och uppdaterade program-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="cb43e-196">Added new MSIX Package cmdlets and updated Applications cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="cb43e-197">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="cb43e-197">Az.EventHub</span></span>
* <span data-ttu-id="cb43e-198">Korrigerade klusterkommandon för EventHub-kluster utan taggar</span><span class="sxs-lookup"><span data-stu-id="cb43e-198">Fixed Cluster commands for EventHub cluster without tags</span></span>
* <span data-ttu-id="cb43e-199">Uppdaterade hjälptext för PartnerNamespace i AzEventHubGeoDRConfiguration-kommandon</span><span class="sxs-lookup"><span data-stu-id="cb43e-199">Updated help text for PartnerNamespace of AzEventHubGeoDRConfiguration commands</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="cb43e-200">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cb43e-200">Az.HDInsight</span></span>
* <span data-ttu-id="cb43e-201">Lade till parametrarna ”ResourceProviderConnection” och ”PrivateLink” till cmdleten ”New-AzHDInsightCluster” för att stödja funktionen för att vidarebefordra utgående och privata länkar</span><span class="sxs-lookup"><span data-stu-id="cb43e-201">Add parameters 'ResourceProviderConnection' and 'PrivateLink' to cmdlet 'New-AzHDInsightCluster' to support relay outbound and private link feature</span></span>
* <span data-ttu-id="cb43e-202">Lade till parametern ”AmbariDatabase” till cmdleten ”New-AzHDInsightCluster” för att stödja en anpassad Ambari-databasfunktion</span><span class="sxs-lookup"><span data-stu-id="cb43e-202">Add parameter 'AmbariDatabase' to cmdlet 'New-AzHDInsightCluster' to support custom Ambari database feature</span></span>
* <span data-ttu-id="cb43e-203">Lade till det accepterade värdet ”AmbariDatabase” till parametern ”MetastoreType” för cmdleten ”Add-AzHDInsightMetastore”</span><span class="sxs-lookup"><span data-stu-id="cb43e-203">Add accept value 'AmbariDatabase' to the parameter 'MetastoreType' of the cmdlet 'Add-AzHDInsightMetastore'</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cb43e-204">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cb43e-204">Az.IotHub</span></span>
* <span data-ttu-id="cb43e-205">Tillät taggar i cmdlet för att skapa i IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="cb43e-205">Allowed tags in IoT Hub create cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cb43e-206">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cb43e-206">Az.KeyVault</span></span>
* <span data-ttu-id="cb43e-207">Stöd för att uppdatera nyckelvalvstagg</span><span class="sxs-lookup"><span data-stu-id="cb43e-207">Supported updating key vault tag</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="cb43e-208">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="cb43e-208">Az.LogicApp</span></span>
* <span data-ttu-id="cb43e-209">Korrigerade så att Get-AzLogicAppRunHistory endast hämtar den första sidan med resultat</span><span class="sxs-lookup"><span data-stu-id="cb43e-209">Fixed for Get-AzLogicAppRunHistory only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb43e-210">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb43e-210">Az.Network</span></span>
* <span data-ttu-id="cb43e-211">Uppdaterade cmdletarna här under</span><span class="sxs-lookup"><span data-stu-id="cb43e-211">Updated below cmdlet</span></span> 
    - <span data-ttu-id="cb43e-212">”New-AzLoadBalancerFrontendIpConfigCommand”, ”Set-AzLoadBalancerFrontendIpConfigCommand”, ”Add-AzLoadBalancerFrontendIpConfigCommand”:</span><span class="sxs-lookup"><span data-stu-id="cb43e-212">'New-AzLoadBalancerFrontendIpConfigCommand', 'Set-AzLoadBalancerFrontendIpConfigCommand', 'Add-AzLoadBalancerFrontendIpConfigCommand':</span></span>
        - <span data-ttu-id="cb43e-213">Lade till egenskapen PublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="cb43e-213">Added PublicIpAddressPrefix property</span></span>
        - <span data-ttu-id="cb43e-214">Lade till egenskapen PublicIpAddressPrefixId</span><span class="sxs-lookup"><span data-stu-id="cb43e-214">Added PublicIpAddressPrefixId property</span></span>
* <span data-ttu-id="cb43e-215">Lade till nya egenskaper till i följande cmdletar för att möjliggöra global belastningsutjämning:</span><span class="sxs-lookup"><span data-stu-id="cb43e-215">Added new properties to the following cmdlets to allow for global load balancing</span></span>
    - <span data-ttu-id="cb43e-216">”New-AzLoadBalancer”:</span><span class="sxs-lookup"><span data-stu-id="cb43e-216">'New-AzLoadBalancer':</span></span>
        - <span data-ttu-id="cb43e-217">Lade till egenskapen SKU-nivå</span><span class="sxs-lookup"><span data-stu-id="cb43e-217">Added Sku Tier property</span></span>
    - <span data-ttu-id="cb43e-218">”New-AzPuplicIpAddress”:</span><span class="sxs-lookup"><span data-stu-id="cb43e-218">'New-AzPuplicIpAddress':</span></span>
        - <span data-ttu-id="cb43e-219">Lade till egenskapen SKU-nivå</span><span class="sxs-lookup"><span data-stu-id="cb43e-219">Added Sku Tier property</span></span>
    - <span data-ttu-id="cb43e-220">”New-AzPublicIpPrefix”:</span><span class="sxs-lookup"><span data-stu-id="cb43e-220">'New-AzPublicIpPrefix':</span></span>
        - <span data-ttu-id="cb43e-221">Lade till egenskapen SKU-nivå</span><span class="sxs-lookup"><span data-stu-id="cb43e-221">Added Sku Tier property</span></span>
    - <span data-ttu-id="cb43e-222">”New-AzLoadBalancerBackendAddressConfig”:</span><span class="sxs-lookup"><span data-stu-id="cb43e-222">'New-AzLoadBalancerBackendAddressConfig':</span></span>
        - <span data-ttu-id="cb43e-223">Lade till egenskapen LoadBalancerFrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="cb43e-223">Added LoadBalancerFrontendIPConfigurationId property</span></span>
* <span data-ttu-id="cb43e-224">Uppdaterade planer att göra varningar för följande cmdletar inaktuella: -”New-AzVirtualHubRoute”, -”New-AzVirtualHubRouteTable”, -”Add-AzVirtualHubRoute”, -”Add-AzVirtualHubRouteTable” -”Get-AzVirtualHubRouteTable” och -”Remove-AzVirtualHubRouteTable”</span><span class="sxs-lookup"><span data-stu-id="cb43e-224">Updated planning to deprecate warnings for the following cmdlets   -'New-AzVirtualHubRoute'   -'New-AzVirtualHubRouteTable'   -'Add-AzVirtualHubRoute'   -'Add-AzVirtualHubRouteTable'   -'Get-AzVirtualHubRouteTable'   -'Remove-AzVirtualHubRouteTable'</span></span>
* <span data-ttu-id="cb43e-225">Lade till planer att göra varningar för argumentet ”RouteTable” inaktuella för följande cmdletar: -”New-AzVirtualHub”, -”Set-AzVirtualHub” och -”Update-AzVirtualHub”</span><span class="sxs-lookup"><span data-stu-id="cb43e-225">Added planning to deprecate warnings on the argument 'RouteTable' for the following cmdlets   -'New-AzVirtualHub'   -'Set-AzVirtualHub'   -'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="cb43e-226">Gjorde argumenten ”-MinScaleUnits” och ”-MaxScaleUnits” valfria i ”Set-AzExpressRouteGateway”</span><span class="sxs-lookup"><span data-stu-id="cb43e-226">Made arguments '-MinScaleUnits' and '-MaxScaleUnits' optional in 'Set-AzExpressRouteGateway'</span></span>
* <span data-ttu-id="cb43e-227">Lade till nya cmdletar för att stödja ömsesidig autentisering och SSL-profiler på Application Gateway</span><span class="sxs-lookup"><span data-stu-id="cb43e-227">Added new cmdlets to support Mutual Authentication and SSL Profiles on Application Gateway</span></span>
    - <span data-ttu-id="cb43e-228">”Get-AzApplicationGatewayClientAuthConfiguration”</span><span class="sxs-lookup"><span data-stu-id="cb43e-228">'Get-AzApplicationGatewayClientAuthConfiguration'</span></span>
    - <span data-ttu-id="cb43e-229">”New-AzApplicationGatewayClientAuthConfiguration”</span><span class="sxs-lookup"><span data-stu-id="cb43e-229">'New-AzApplicationGatewayClientAuthConfiguration'</span></span>
    - <span data-ttu-id="cb43e-230">”Remove-AzApplicationGatewayClientAuthConfiguration”</span><span class="sxs-lookup"><span data-stu-id="cb43e-230">'Remove-AzApplicationGatewayClientAuthConfiguration'</span></span>
    - <span data-ttu-id="cb43e-231">”Set-AzApplicationGatewayClientAuthConfiguration”</span><span class="sxs-lookup"><span data-stu-id="cb43e-231">'Set-AzApplicationGatewayClientAuthConfiguration'</span></span>
    - <span data-ttu-id="cb43e-232">”Add-AzApplicationGatewayTrustedClientCertificate”</span><span class="sxs-lookup"><span data-stu-id="cb43e-232">'Add-AzApplicationGatewayTrustedClientCertificate'</span></span> 
    - <span data-ttu-id="cb43e-233">”Get-AzApplicationGatewayTrustedClientCertificate”</span><span class="sxs-lookup"><span data-stu-id="cb43e-233">'Get-AzApplicationGatewayTrustedClientCertificate'</span></span> 
    - <span data-ttu-id="cb43e-234">”New-AzApplicationGatewayTrustedClientCertificate”</span><span class="sxs-lookup"><span data-stu-id="cb43e-234">'New-AzApplicationGatewayTrustedClientCertificate'</span></span> 
    - <span data-ttu-id="cb43e-235">”Remove-AzApplicationGatewayTrustedClientCertificate”</span><span class="sxs-lookup"><span data-stu-id="cb43e-235">'Remove-AzApplicationGatewayTrustedClientCertificate'</span></span> 
    - <span data-ttu-id="cb43e-236">”Set-AzApplicationGatewayTrustedClientCertificate”</span><span class="sxs-lookup"><span data-stu-id="cb43e-236">'Set-AzApplicationGatewayTrustedClientCertificate'</span></span>
    - <span data-ttu-id="cb43e-237">”Add-AzApplicationGatewaySslProfile”</span><span class="sxs-lookup"><span data-stu-id="cb43e-237">'Add-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="cb43e-238">”Get-AzApplicationGatewaySslProfile”</span><span class="sxs-lookup"><span data-stu-id="cb43e-238">'Get-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="cb43e-239">”New-AzApplicationGatewaySslProfile”</span><span class="sxs-lookup"><span data-stu-id="cb43e-239">'New-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="cb43e-240">”Remove-AzApplicationGatewaySslProfile”</span><span class="sxs-lookup"><span data-stu-id="cb43e-240">'Remove-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="cb43e-241">”Set-AzApplicationGatewaySslProfile”</span><span class="sxs-lookup"><span data-stu-id="cb43e-241">'Set-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="cb43e-242">”Get-AzApplicationGatewaySslProfilePolicy”</span><span class="sxs-lookup"><span data-stu-id="cb43e-242">'Get-AzApplicationGatewaySslProfilePolicy'</span></span>
    - <span data-ttu-id="cb43e-243">”Remove-AzApplicationGatewaySslProfilePolicy”</span><span class="sxs-lookup"><span data-stu-id="cb43e-243">'Remove-AzApplicationGatewaySslProfilePolicy'</span></span>
    - <span data-ttu-id="cb43e-244">”Set-AzApplicationGatewaySslProfilePolicy”</span><span class="sxs-lookup"><span data-stu-id="cb43e-244">'Set-AzApplicationGatewaySslProfilePolicy'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cb43e-245">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb43e-245">Az.RecoveryServices</span></span>
* <span data-ttu-id="cb43e-246">Specificera att principen BackupTime är i UTC.</span><span class="sxs-lookup"><span data-stu-id="cb43e-246">Specifying policy BackupTime is in UTC.</span></span>
* <span data-ttu-id="cb43e-247">Ändra varning för icke-bakåtkompatibel ändring i cmdleten Get-AzRecoveryServicesBackupJobDetails.</span><span class="sxs-lookup"><span data-stu-id="cb43e-247">Modifying breaking change warning in Get-AzRecoveryServicesBackupJobDetails cmdlet.</span></span>
* <span data-ttu-id="cb43e-248">Uppdaterar exempelskriptets hjälptext för cmdleten Set-AzRecoveryServicesBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="cb43e-248">Updating sample script help text for Set-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb43e-249">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb43e-249">Az.Resources</span></span>
* <span data-ttu-id="cb43e-250">Korrigerade ett problem där konsekvensgranskning visade två omfång för resursgrupper med olika skiftlägen</span><span class="sxs-lookup"><span data-stu-id="cb43e-250">Fixed an issue where What-If shows two resource group scopes with different casing</span></span>
* <span data-ttu-id="cb43e-251">Uppdaterade ”Export-AzResourceGroup” för att använda SDK.</span><span class="sxs-lookup"><span data-stu-id="cb43e-251">Updated 'Export-AzResourceGroup' to use the SDK.</span></span>
* <span data-ttu-id="cb43e-252">Lade till kulturinformation för att parsa metoder</span><span class="sxs-lookup"><span data-stu-id="cb43e-252">Added culture info to parse methods</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb43e-253">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb43e-253">Az.Sql</span></span>
* <span data-ttu-id="cb43e-254">Korrigerade problem där Set-AzSqlDatabaseAudit inte hade stöd för databas i hyperskala och databasversionen inte kunde fastställas</span><span class="sxs-lookup"><span data-stu-id="cb43e-254">Fixed issues where Set-AzSqlDatabaseAudit were not support Hyperscale database and database edition cannot be determined</span></span>
* <span data-ttu-id="cb43e-255">Lade till MaintenanceConfigurationId för ”New-AzSqlInstance” och ”Set-AzSqlInstance”</span><span class="sxs-lookup"><span data-stu-id="cb43e-255">Added MaintenanceConfigurationId to 'New-AzSqlInstance' and 'Set-AzSqlInstance'</span></span>
* <span data-ttu-id="cb43e-256">Korrigerade en bugg i GetAzureSqlDatabaseReplicationLink.cs där parametern PartnerServerName kontrollerades efter värde i stället för nyckel</span><span class="sxs-lookup"><span data-stu-id="cb43e-256">Fixed a bug in GetAzureSqlDatabaseReplicationLink.cs where PartnerServerName parameter was being checked for by value instead of key</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cb43e-257">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb43e-257">Az.Websites</span></span>
* <span data-ttu-id="cb43e-258">Lade till stöd för nya funktioner för åtkomstbegränsning: ServiceTag, flera IP-adresser och HTTP-rubriker</span><span class="sxs-lookup"><span data-stu-id="cb43e-258">Added support for new access restriction features: ServiceTag, multi-ip and http-headers</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="cb43e-259">Tack till våra community-deltagare</span><span class="sxs-lookup"><span data-stu-id="cb43e-259">Thanks to our community contributors</span></span>
* <span data-ttu-id="cb43e-260">John Q. Martin (@johnmart82), lägger till nödvändig brandväggsinformation (#13385)</span><span class="sxs-lookup"><span data-stu-id="cb43e-260">John Q. Martin (@johnmart82), Adding firewall prerequisite information (#13385)</span></span>
* <span data-ttu-id="cb43e-261">Manikandan Duraisamy (@madurais-msft), korrigerade argumentet PublicSubnetName (#13417)</span><span class="sxs-lookup"><span data-stu-id="cb43e-261">Manikandan Duraisamy (@madurais-msft), Corrected the PublicSubnetName argument (#13417)</span></span>
* <span data-ttu-id="cb43e-262">@mahortas, uppdatera parametervärden för -HostName (#13349)</span><span class="sxs-lookup"><span data-stu-id="cb43e-262">@mahortas, Update for -HostNames parameter values (#13349)</span></span>
* <span data-ttu-id="cb43e-263">@MariachiForHire, lade till TrafficAnalyticsInterval-värden som stöds (#13304)</span><span class="sxs-lookup"><span data-stu-id="cb43e-263">@MariachiForHire, added supported TrafficAnalyticsInterval values (#13304)</span></span>
* <span data-ttu-id="cb43e-264">Michael Jonas (@mikejwhat), tillåt att Get-AzLogicAppRunHistory returnerar fler än 30 poster (#13393)</span><span class="sxs-lookup"><span data-stu-id="cb43e-264">Michael James (@mikejwhat), Allow Get-AzLogicAppRunHistory to return more than 30 entries (#13393)</span></span>
* <span data-ttu-id="cb43e-265">Shashikant Shakya (@shshakya), uppdatera Restore-AzSqlInstanceDatabase.md (#13404)</span><span class="sxs-lookup"><span data-stu-id="cb43e-265">Shashikant Shakya (@shshakya), Update Restore-AzSqlInstanceDatabase.md (#13404)</span></span>

## <a name="500---october-2020"></a><span data-ttu-id="cb43e-266">5.0.0 – Oktober 2020</span><span class="sxs-lookup"><span data-stu-id="cb43e-266">5.0.0 - October 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cb43e-267">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb43e-267">Az.Accounts</span></span>
* <span data-ttu-id="cb43e-268">[Icke-bakåtkompatibel ändring] Tog bort ”Get-AzProfile” och ”Select-AzProfile”</span><span class="sxs-lookup"><span data-stu-id="cb43e-268">[Breaking Change] Removed 'Get-AzProfile' and 'Select-AzProfile'</span></span>
* <span data-ttu-id="cb43e-269">Ersatte Azure Directory Authentication Library med Microsoft Authentication Library (MSAL)</span><span class="sxs-lookup"><span data-stu-id="cb43e-269">Replaced Azure Directory Authentication Library with Microsoft Authentication Library(MSAL)</span></span>

#### <a name="azaks"></a><span data-ttu-id="cb43e-270">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="cb43e-270">Az.Aks</span></span>
* <span data-ttu-id="cb43e-271">[Icke-bakåtkompatibel ändring] Tog bort aliaset ”ClientIdAndSecret” i ”New-AzAksCluster” och ”Set-AzAksCluster”.</span><span class="sxs-lookup"><span data-stu-id="cb43e-271">[Breaking Change] Removed parameter alias 'ClientIdAndSecret' in 'New-AzAksCluster' and 'Set-AzAksCluster'.</span></span>
* <span data-ttu-id="cb43e-272">[Icke-bakåtkompatibel ändring] Ändrade standardvärdet för ”NodeVmSetType” i ”New-AzAksCluster” från ”AvailabilitySet” till ”VirtualMachineScaleSets”.</span><span class="sxs-lookup"><span data-stu-id="cb43e-272">[Breaking Change] Changed the default value of 'NodeVmSetType' in 'New-AzAksCluster' from 'AvailabilitySet' to 'VirtualMachineScaleSets'.</span></span>
* <span data-ttu-id="cb43e-273">[Icke-bakåtkompatibel ändring] Ändrade standardvärdet för ”NetworkPlugin” i ”New-AzAksCluster” från ”None” till ”azure”.</span><span class="sxs-lookup"><span data-stu-id="cb43e-273">[Breaking Change] Changed the default value of 'NetworkPlugin' in 'New-AzAksCluster' from 'None' to 'azure'.</span></span>
* <span data-ttu-id="cb43e-274">[Icke-bakåtkompatibel ändring] Tog bort parametern ”NodeOsType” i ”New-AzAksCluster” eftersom den endast har stöd för Linux med ett värde.</span><span class="sxs-lookup"><span data-stu-id="cb43e-274">[Breaking Change] Removed parameter 'NodeOsType' in 'New-AzAksCluster' as it supports only one value Linux.</span></span>

#### <a name="azbilling"></a><span data-ttu-id="cb43e-275">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="cb43e-275">Az.Billing</span></span>
* <span data-ttu-id="cb43e-276">Lade till cmdleten ”Get-AzBillingAccount”</span><span class="sxs-lookup"><span data-stu-id="cb43e-276">Added 'Get-AzBillingAccount' cmdlet</span></span>
* <span data-ttu-id="cb43e-277">Lade till cmdleten ”Get-AzBillingProfile”</span><span class="sxs-lookup"><span data-stu-id="cb43e-277">Added 'Get-AzBillingProfile' cmdlet</span></span>
* <span data-ttu-id="cb43e-278">Lade till cmdleten ”Get-AzInvoiceSection”</span><span class="sxs-lookup"><span data-stu-id="cb43e-278">Added 'Get-AzInvoiceSection' cmdlet</span></span>
* <span data-ttu-id="cb43e-279">Lade till nya parametrar i cmdleten ”Get-AzBillingInvoice”</span><span class="sxs-lookup"><span data-stu-id="cb43e-279">Added new parameters in 'Get-AzBillingInvoice' cmdlet</span></span>
* <span data-ttu-id="cb43e-280">Tog bort egenskaperna ”DownloadUrlExpiry”, ”Type” och ”BillingPeriodNames” från svaret för cmdleten ”Get-AzBillingInvoic”</span><span class="sxs-lookup"><span data-stu-id="cb43e-280">Removed properties DownloadUrlExpiry, Type, BillingPeriodNames from the response of Get-AzBillingInvoice cmdlet</span></span>

#### <a name="azcdn"></a><span data-ttu-id="cb43e-281">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="cb43e-281">Az.Cdn</span></span>
* <span data-ttu-id="cb43e-282">Lade till cmdletar för att stödja funktioner för flera ursprung och privat länk</span><span class="sxs-lookup"><span data-stu-id="cb43e-282">Added cmdlets to support multi-origin and private link functionality</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="cb43e-283">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cb43e-283">Az.CognitiveServices</span></span>
* <span data-ttu-id="cb43e-284">Uppdaterade SDK till 7.4.0-preview.</span><span class="sxs-lookup"><span data-stu-id="cb43e-284">Updated SDK to 7.4.0-preview.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb43e-285">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb43e-285">Az.Compute</span></span>
* <span data-ttu-id="cb43e-286">Lade till parametern ”-VmssId” till ”New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="cb43e-286">Added '-VmssId' parameter to 'New-AzVm'</span></span>
* <span data-ttu-id="cb43e-287">Lade till parametern ”PlatformFaultDomainCount” till cmdleten ”New-AzVmss”.</span><span class="sxs-lookup"><span data-stu-id="cb43e-287">Added 'PlatformFaultDomainCount' parameter to the 'New-AzVmss' cmdlet.</span></span>
* <span data-ttu-id="cb43e-288">Ny cmdlet: ”Get-AzDiskEncryptionSetAssociatedResource”</span><span class="sxs-lookup"><span data-stu-id="cb43e-288">New cmdlet 'Get-AzDiskEncryptionSetAssociatedResource'</span></span>
* <span data-ttu-id="cb43e-289">Lade till de valfria parametrarna ”Tier” och ”LogicalSectorSize” till cmdleten ”New-AzDiskConfig”.</span><span class="sxs-lookup"><span data-stu-id="cb43e-289">Added 'Tier' and 'LogicalSectorSize' optional parameters to the New-AzDiskConfig cmdlet.</span></span> 
* <span data-ttu-id="cb43e-290">Lade till de valfria parametrarna ”Tier”, ”MaxSharesCount”, ”DiskIOPSReadOnly” och ”DiskMBpsReadOnly” till cmdleten ”New-AzDiskUpdateConfig”.</span><span class="sxs-lookup"><span data-stu-id="cb43e-290">Added 'Tier', 'MaxSharesCount', 'DiskIOPSReadOnly', and 'DiskMBpsReadOnly' optional parameters to the 'New-AzDiskUpdateConfig' cmdlet.</span></span> 

#### <a name="azcontainerregistry"></a><span data-ttu-id="cb43e-291">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="cb43e-291">Az.ContainerRegistry</span></span>
* <span data-ttu-id="cb43e-292">[Icke-bakåtkompatibel ändring] Uppdaterar API-versionen till 2019-05-01</span><span class="sxs-lookup"><span data-stu-id="cb43e-292">[Breaking Change] Updates API version to 2019-05-01</span></span>
* <span data-ttu-id="cb43e-293">[Icke-bakåtkompatibel ändring] Tog bort SKU:n ”Classic” och parametern ”StorageAccountName” från ”New-AzContainerRegistry”</span><span class="sxs-lookup"><span data-stu-id="cb43e-293">[Breaking Change] Removed SKU 'Classic' and parameter 'StorageAccountName' from 'New-AzContainerRegistry'</span></span>
* <span data-ttu-id="cb43e-294">Lade till nya cmdletar: ”Connect-AzContainerRegistry”, ”Import-AzContainerRegistry”, ”Get-AzContainerRegistryUsage”, ”New-AzContainerRegistryNetworkRule”, ”Set-AzContainerRegistryNetworkRule”</span><span class="sxs-lookup"><span data-stu-id="cb43e-294">Added New cmdlets: 'Connect-AzContainerRegistry', 'Import-AzContainerRegistry', 'Get-AzContainerRegistryUsage', 'New-AzContainerRegistryNetworkRule', 'Set-AzContainerRegistryNetworkRule'</span></span>
* <span data-ttu-id="cb43e-295">Lade till den nya parametern ”NetworkRuleSet” till ”Update-AzContainerRegistry”</span><span class="sxs-lookup"><span data-stu-id="cb43e-295">Added new parameter 'NetworkRuleSet' to 'Update-AzContainerRegistry'</span></span>

#### <a name="azdatabricks"></a><span data-ttu-id="cb43e-296">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="cb43e-296">Az.Databricks</span></span>
* <span data-ttu-id="cb43e-297">Korrigerade en bugg som kunde leda till att en uppdatering av en Databricks-arbetsyta utan `-EncryptionKeyVersion` misslyckades.</span><span class="sxs-lookup"><span data-stu-id="cb43e-297">Fixed a bug that may cause updating databricks workspace without `-EncryptionKeyVersion` to fail.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cb43e-298">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cb43e-298">Az.DataFactory</span></span>
* <span data-ttu-id="cb43e-299">Uppdaterade ADF .Net SDK-versionen till 4.12.0</span><span class="sxs-lookup"><span data-stu-id="cb43e-299">Updated ADF .Net SDK version to 4.12.0</span></span>
* <span data-ttu-id="cb43e-300">Uppdaterade ADF-krypteringsklientens SDK-version till 4.14.7587.7</span><span class="sxs-lookup"><span data-stu-id="cb43e-300">Updated ADF encryption client SDK version to 4.14.7587.7</span></span>
* <span data-ttu-id="cb43e-301">Lade till kommandona ”Stop-AzDataFactoryV2TriggerRun” och ”Invoke-AzDataFactoryV2TriggerRun”</span><span class="sxs-lookup"><span data-stu-id="cb43e-301">Added 'Stop-AzDataFactoryV2TriggerRun' and 'Invoke-AzDataFactoryV2TriggerRun' commands</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="cb43e-302">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="cb43e-302">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="cb43e-303">Kräv egenskapen Plats för att skapa ARM-objekt på högsta nivån.</span><span class="sxs-lookup"><span data-stu-id="cb43e-303">Require Location property for creating top level arm objects.</span></span>
        <span data-ttu-id="cb43e-304">\* Gjorde så att `ApplicationGroupType` krävs för `New-AzWvdApplicationGroup`.</span><span class="sxs-lookup"><span data-stu-id="cb43e-304">\* Made `ApplicationGroupType` required for `New-AzWvdApplicationGroup`.</span></span>
        <span data-ttu-id="cb43e-305">\* Gjorde så att `HostPoolArmPath` krävs för `New-AzWvdApplicationGroup`.</span><span class="sxs-lookup"><span data-stu-id="cb43e-305">\* Made `HostPoolArmPath` required for `New-AzWvdApplicationGroup`.</span></span>
        <span data-ttu-id="cb43e-306">\* `PreferredAppGroupType` har lagts till för `New-AzWvdHostPool`.</span><span class="sxs-lookup"><span data-stu-id="cb43e-306">\* Added `PreferredAppGroupType` for `New-AzWvdHostPool`.</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="cb43e-307">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="cb43e-307">Az.Functions</span></span>
* <span data-ttu-id="cb43e-308">[Icke-bakåtkompatibel ändring] Tog bort växelparametern ”IncludeSlot” från alla förutom en parameteruppsättning i ”Get-AzFunctionApp”.</span><span class="sxs-lookup"><span data-stu-id="cb43e-308">[Breaking Change] Removed 'IncludeSlot' switch parameter from all but one parameter set of 'Get-AzFunctionApp'.</span></span> <span data-ttu-id="cb43e-309">Cmdleten stöder nu hämtning av distributionsfack i resultaten när ”-IncludeSlot” anges.</span><span class="sxs-lookup"><span data-stu-id="cb43e-309">The cmdlet now supports retrieving deployment slots in the results when '-IncludeSlot' is specified.</span></span> 
* <span data-ttu-id="cb43e-310">Uppdaterade ”New-AzFunctionApp”:</span><span class="sxs-lookup"><span data-stu-id="cb43e-310">Updated 'New-AzFunctionApp':</span></span>
  - <span data-ttu-id="cb43e-311">Korrigerade ”-DisableApplicationInsights” så att inga Application Insights-projekt skapas när det här alternativet har angetts.</span><span class="sxs-lookup"><span data-stu-id="cb43e-311">Fixed -DisableApplicationInsights so that no application insights project is created when this option is specified.</span></span> <span data-ttu-id="cb43e-312">[#12728]</span><span class="sxs-lookup"><span data-stu-id="cb43e-312">[#12728]</span></span>
  - <span data-ttu-id="cb43e-313">[Icke-bakåtkompatibel ändring] Tog bort stöd för att skapa PowerShell 6.2-funktionsappar.</span><span class="sxs-lookup"><span data-stu-id="cb43e-313">[Breaking Change] Removed support to create PowerShell 6.2 function apps.</span></span>
  - <span data-ttu-id="cb43e-314">[Icke-bakåtkompatibel ändring] Ändrade körningsversionen som är standard i Functions version 3 i Windows för PowerShell-funktionsappar från 6.2 till 7.0 när parametern RuntimeVersion inte har angetts.</span><span class="sxs-lookup"><span data-stu-id="cb43e-314">[Breaking Change] Changed the default runtime version in Functions version 3 on Windows for PowerShell function apps from 6.2 to 7.0 when the RuntimeVersion parameter is not specified.</span></span>
  - <span data-ttu-id="cb43e-315">[Icke-bakåtkompatibel ändring] Ändrade körningsversionen som är standard i Functions version 3 i Windows och Linux för Node-funktionsappar från 10 till 12 när parametern RuntimeVersion inte har angetts.</span><span class="sxs-lookup"><span data-stu-id="cb43e-315">[Breaking Change] Changed the default runtime version in Functions version 3 on Windows and Linux for Node function apps from 10 to 12 when the RuntimeVersion parameter is not specified.</span></span>
  - <span data-ttu-id="cb43e-316">[Icke-bakåtkompatibel ändring] Ändrade körningsversionen som är standard i Functions version 3 i Linux för Python-funktionsappar från 3.7 till 3.8 när parametern RuntimeVersion inte har angetts.</span><span class="sxs-lookup"><span data-stu-id="cb43e-316">[Breaking Change] Changed the default runtime version in Functions version 3 on Linux for Python function apps from 3.7 to 3.8 when the RuntimeVersion parameter is not specified.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="cb43e-317">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cb43e-317">Az.HDInsight</span></span>
 * <span data-ttu-id="cb43e-318">För cmdleten New-AzHDInsightCluster:</span><span class="sxs-lookup"><span data-stu-id="cb43e-318">For New-AzHDInsightCluster cmdlet:</span></span>
     - <span data-ttu-id="cb43e-319">Ersatte parametern ”DefaultStorageAccountName” med ”StorageAccountResourceId”</span><span class="sxs-lookup"><span data-stu-id="cb43e-319">Replaced parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
     - <span data-ttu-id="cb43e-320">Ersatte parametern ”DefaultStorageAccountKey” med ”StorageAccountKey”</span><span class="sxs-lookup"><span data-stu-id="cb43e-320">Replaced parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
     - <span data-ttu-id="cb43e-321">Ersatte parametern ”DefaultStorageAccountType” med ”StorageAccountType”</span><span class="sxs-lookup"><span data-stu-id="cb43e-321">Replaced parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
     - <span data-ttu-id="cb43e-322">Tog bort parametern ”PublicNetworkAccessType”</span><span class="sxs-lookup"><span data-stu-id="cb43e-322">Removed parameter 'PublicNetworkAccessType'</span></span>
     - <span data-ttu-id="cb43e-323">Ta bort parametern ”OutboundPublicNetworkAccessType”</span><span class="sxs-lookup"><span data-stu-id="cb43e-323">Removed parameter 'OutboundPublicNetworkAccessType'</span></span>
     - <span data-ttu-id="cb43e-324">Lade till nya parametrar: ”StorageFileSystem” och ”StorageAccountManagedIdentity” för att stödja ADLSGen2</span><span class="sxs-lookup"><span data-stu-id="cb43e-324">Added new parameters: 'StorageFileSystem' and 'StorageAccountManagedIdentity' to support ADLSGen2</span></span>
     - <span data-ttu-id="cb43e-325">Lade till den nya parametern ”EnableIDBroker” för att stödja ID-förmedlaren i HDInsight</span><span class="sxs-lookup"><span data-stu-id="cb43e-325">Added new parameter 'EnableIDBroker' to Support HDInsight ID Broker</span></span>
     - <span data-ttu-id="cb43e-326">Lade till nya parametrar: ”KafkaClientGroupId”, ”KafkaClientGroupName” och ”KafkaManagementNodeSize” för att stödja Kafka REST-proxy</span><span class="sxs-lookup"><span data-stu-id="cb43e-326">Added new parameters: 'KafkaClientGroupId', 'KafkaClientGroupName' and 'KafkaManagementNodeSize' to support Kafka Rest Proxy</span></span>
 * <span data-ttu-id="cb43e-327">För cmdleten New-AzHDInsightClusterConfig:</span><span class="sxs-lookup"><span data-stu-id="cb43e-327">For New-AzHDInsightClusterConfig cmdlet:</span></span>
     - <span data-ttu-id="cb43e-328">Ersatte parametern ”DefaultStorageAccountName” med ”StorageAccountResourceId”</span><span class="sxs-lookup"><span data-stu-id="cb43e-328">Replaced parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
     - <span data-ttu-id="cb43e-329">Ersatte parametern ”DefaultStorageAccountKey” med ”StorageAccountKey”</span><span class="sxs-lookup"><span data-stu-id="cb43e-329">Replaced parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
     - <span data-ttu-id="cb43e-330">Ersatte parametern ”DefaultStorageAccountType” med ”StorageAccountType”</span><span class="sxs-lookup"><span data-stu-id="cb43e-330">Replaced parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
     - <span data-ttu-id="cb43e-331">Tog bort parametern ”PublicNetworkAccessType”</span><span class="sxs-lookup"><span data-stu-id="cb43e-331">Removed parameter 'PublicNetworkAccessType'</span></span>
     - <span data-ttu-id="cb43e-332">Ta bort parametern ”OutboundPublicNetworkAccessType”</span><span class="sxs-lookup"><span data-stu-id="cb43e-332">Removed parameter 'OutboundPublicNetworkAccessType'</span></span>
* <span data-ttu-id="cb43e-333">För cmdleten Set-AzHDInsightDefaultStorage:</span><span class="sxs-lookup"><span data-stu-id="cb43e-333">For Set-AzHDInsightDefaultStorage cmdlet:</span></span>
    - <span data-ttu-id="cb43e-334">Ersatte parametern ”StorageAccountName” med ”StorageAccountResourceId”</span><span class="sxs-lookup"><span data-stu-id="cb43e-334">Replaced parameter 'StorageAccountName' with 'StorageAccountResourceId'</span></span>
* <span data-ttu-id="cb43e-335">För cmdleten Add-AzHDInsightSecurityProfile:</span><span class="sxs-lookup"><span data-stu-id="cb43e-335">For Add-AzHDInsightSecurityProfile cmdlet:</span></span>
    - <span data-ttu-id="cb43e-336">Ersatte parametern ”Domain” med ”DomainResourceId”</span><span class="sxs-lookup"><span data-stu-id="cb43e-336">Replaced parameter 'Domain' with 'DomainResourceId'</span></span>
    - <span data-ttu-id="cb43e-337">Tog bort det obligatoriska kravet för parametern ”OrganizationalUnitDN”</span><span class="sxs-lookup"><span data-stu-id="cb43e-337">Removed the mandatory requirement for parameter 'OrganizationalUnitDN'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cb43e-338">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cb43e-338">Az.KeyVault</span></span>
* <span data-ttu-id="cb43e-339">[Icke-bakåtkompatibel ändring] Parametrarna DisableSoftDelete i ”New-AzKeyVault” och EnableSoftDelete i ”Update-AzKeyVault” har gjorts inaktuella</span><span class="sxs-lookup"><span data-stu-id="cb43e-339">[Breaking Change] Deprecated parameter DisableSoftDelete in 'New-AzKeyVault' and EnableSoftDelete in 'Update-AzKeyVault'</span></span>
* <span data-ttu-id="cb43e-340">[Icke-bakåtkompatibel ändring] Tog bort attributet SecretValueText för att undvika att SecretValue visas direkt [#12266]</span><span class="sxs-lookup"><span data-stu-id="cb43e-340">[Breaking Change] Removed attribute SecretValueText to avoid displaying SecretValue directly [#12266]</span></span>
* <span data-ttu-id="cb43e-341">Stöd för ny resurstyp: hanterad HSM</span><span class="sxs-lookup"><span data-stu-id="cb43e-341">Supported new resource type: managed HSM</span></span>
    - <span data-ttu-id="cb43e-342">CRUD för hanterad HSM och cmdleter för att köra nycklar på hanterad HSM</span><span class="sxs-lookup"><span data-stu-id="cb43e-342">CRUD of managed HSM and cmdlets to operate keys on managed HSM</span></span>
    - <span data-ttu-id="cb43e-343">Fullständig HSM-säkerhetskopiering/återställning, skapande av AES-nyckel, säkerhetskopiering/återställning av domän, RBAC</span><span class="sxs-lookup"><span data-stu-id="cb43e-343">Full HSM backup/restore, AES key creation, security domain backup/restore, RBAC</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="cb43e-344">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="cb43e-344">Az.ManagedServices</span></span>
* <span data-ttu-id="cb43e-345">[Icke-bakåtkompatibel ändring] Uppdaterade namngivningskonventioner för parametrar och associerade exempel</span><span class="sxs-lookup"><span data-stu-id="cb43e-345">[Breaking Change] Updated parameters naming conventions and associated examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb43e-346">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb43e-346">Az.Network</span></span>
* <span data-ttu-id="cb43e-347">[Icke-bakåtkompatibel ändring] Tog bort parametern ”HostedSubnet” och lade till ”Subnet” i stället</span><span class="sxs-lookup"><span data-stu-id="cb43e-347">[Breaking Change] Removed parameter 'HostedSubnet' and added 'Subnet' instead</span></span>
* <span data-ttu-id="cb43e-348">Lade till nya cmdletar för peeringvägar för virtuella routrar</span><span class="sxs-lookup"><span data-stu-id="cb43e-348">Added new cmdlets for Virtual Router Peer Routes</span></span>
    - <span data-ttu-id="cb43e-349">”Get-AzVirtualRouterPeerLearnedRoute”</span><span class="sxs-lookup"><span data-stu-id="cb43e-349">'Get-AzVirtualRouterPeerLearnedRoute'</span></span>
    - <span data-ttu-id="cb43e-350">”Get-AzVirtualRouterPeerAdvertisedRoute”</span><span class="sxs-lookup"><span data-stu-id="cb43e-350">'Get-AzVirtualRouterPeerAdvertisedRoute'</span></span>
* <span data-ttu-id="cb43e-351">Cmdleten New-AzFirewall har uppdaterats:</span><span class="sxs-lookup"><span data-stu-id="cb43e-351">Updated New-AzFirewall cmdlet:</span></span>
    - <span data-ttu-id="cb43e-352">Lade till parametern ”-SkuTier”</span><span class="sxs-lookup"><span data-stu-id="cb43e-352">Added parameter '-SkuTier'</span></span>
    - <span data-ttu-id="cb43e-353">Lade till parametern ”-SkuName” och gjorde Sku till ett alias för den</span><span class="sxs-lookup"><span data-stu-id="cb43e-353">Added parameter '-SkuName' and made Sku as Alias for this</span></span>
    - <span data-ttu-id="cb43e-354">Tog bort parametern ”-Sku”</span><span class="sxs-lookup"><span data-stu-id="cb43e-354">Removed parameter '-Sku'</span></span>
* <span data-ttu-id="cb43e-355">[Icke-bakåtkompatibel ändring] Gjorde argumentet ”Connectionlink” obligatoriskt i ”Start-AzVpnConnectionPacketCapture” och ”Stop-AzVpnConnectionPacketCapture”</span><span class="sxs-lookup"><span data-stu-id="cb43e-355">[Breaking Change] Made 'Connectionlink' argument mandatory in 'Start-AzVpnConnectionPacketCapture' and 'Stop-AzVpnConnectionPacketCapture'</span></span>
* <span data-ttu-id="cb43e-356">[Icke-bakåtkompatibel ändring] Uppdaterade ”New-AzNetworkWatcherConnectionMonitorEndPointObject” för att ta bort parametern ”-Filter”</span><span class="sxs-lookup"><span data-stu-id="cb43e-356">[Breaking Change] Updated 'New-AzNetworkWatcherConnectionMonitorEndPointObject' to remove parameter '-Filter'</span></span>
* <span data-ttu-id="cb43e-357">[Icke-bakåtkompatibel ändring] Ersatte cmdleten ”New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject” med ”New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject”</span><span class="sxs-lookup"><span data-stu-id="cb43e-357">[Breaking Change] Replaced 'New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject' cmdlet with 'New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject'</span></span>
* <span data-ttu-id="cb43e-358">Uppdaterade cmdleten ”New-AzNetworkWatcherConnectionMonitorEndPointObject”:</span><span class="sxs-lookup"><span data-stu-id="cb43e-358">Updated 'New-AzNetworkWatcherConnectionMonitorEndPointObject' cmdlet:</span></span>
    - <span data-ttu-id="cb43e-359">Lade till parametern ”-Type”</span><span class="sxs-lookup"><span data-stu-id="cb43e-359">Added parameter '-Type'</span></span>
    - <span data-ttu-id="cb43e-360">Lade till parametern ”-CoverageLevel”</span><span class="sxs-lookup"><span data-stu-id="cb43e-360">Added parameter '-CoverageLevel'</span></span>
    - <span data-ttu-id="cb43e-361">Lade till parametern ”-Scope”</span><span class="sxs-lookup"><span data-stu-id="cb43e-361">Added parameter '-Scope'</span></span>
* <span data-ttu-id="cb43e-362">Uppdaterade cmdleten ”New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject” med den nya parametern ”-DestinationPortBehavior”</span><span class="sxs-lookup"><span data-stu-id="cb43e-362">Updated 'New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject' cmdlet with new parameter '-DestinationPortBehavior'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cb43e-363">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb43e-363">Az.RecoveryServices</span></span>
* <span data-ttu-id="cb43e-364">Korrigerar återställning av arbetsbelastningar för behörigheter för deltagare.</span><span class="sxs-lookup"><span data-stu-id="cb43e-364">Fixing Workload Restore for contributor permissions.</span></span>
* <span data-ttu-id="cb43e-365">Lade till nya parameteruppsättningar och valideringar för cmdleten ”Restore-AzRecoveryServicesBackupItem”.</span><span class="sxs-lookup"><span data-stu-id="cb43e-365">Added new parameter sets and validations for Restore-AzRecoveryServicesBackupItem cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb43e-366">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb43e-366">Az.Resources</span></span>
* <span data-ttu-id="cb43e-367">Korrigerade en bugg vid parsning</span><span class="sxs-lookup"><span data-stu-id="cb43e-367">Fixed parsing bug</span></span>
* <span data-ttu-id="cb43e-368">Uppdaterade What-If-cmdletar i ARM-mall för att ta bort förhandsgranskningsmeddelandet från resultaten</span><span class="sxs-lookup"><span data-stu-id="cb43e-368">Updated ARM template What-If cmdlets to remove preview message from results</span></span>
* <span data-ttu-id="cb43e-369">Korrigerade ett problem där cmdletar för mall-distribution kraschar om ”-WhatIf” har ställts in på ett högre omfång [#13038]</span><span class="sxs-lookup"><span data-stu-id="cb43e-369">Fixed an issue where template deployment cmdlets crash if '-WhatIf' is set at a higher scope [#13038]</span></span>
* <span data-ttu-id="cb43e-370">Korrigerade ett problem där cmdletar för malldistribution inte bevarar skiftläget för mallparametrar</span><span class="sxs-lookup"><span data-stu-id="cb43e-370">Fixed an issue where template deployment cmdlets does not preserve case for template parameters</span></span>
* <span data-ttu-id="cb43e-371">Lade till en standard-API-version som kan användas i cmdleten ”Export-AzResourceGroup”</span><span class="sxs-lookup"><span data-stu-id="cb43e-371">Added a default API version to be used in 'Export-AzResourceGroup' cmdlet</span></span>
* <span data-ttu-id="cb43e-372">Lade till cmdletar för mallspecifikationer (”Get-AzTemplateSpec”, ”Set-AzTemplateSpec”, ”New-AzTemplateSpec”, ”Remove-AzTemplateSpec”, ”Export-AzTemplateSpec”)</span><span class="sxs-lookup"><span data-stu-id="cb43e-372">Added cmdlets for Template Specs ('Get-AzTemplateSpec', 'Set-AzTemplateSpec', 'New-AzTemplateSpec', 'Remove-AzTemplateSpec', 'Export-AzTemplateSpec')</span></span>
* <span data-ttu-id="cb43e-373">Lade till stöd för att distribuera mallspecifikationer med befintliga cmdletar för distribution (via den nya parametern ”-TemplateSpecId”)</span><span class="sxs-lookup"><span data-stu-id="cb43e-373">Added support for deploying Template Specs using existing deployment cmdlets (via the new -TemplateSpecId parameter)</span></span> 
* <span data-ttu-id="cb43e-374">Uppdaterade ”Get-AzResourceGroupDeploymentOperation” för att använda SDK.</span><span class="sxs-lookup"><span data-stu-id="cb43e-374">Updated 'Get-AzResourceGroupDeploymentOperation' to use the SDK.</span></span>
* <span data-ttu-id="cb43e-375">Tog bort parametern ”ApiVersion” från cmdletarna ”\*-AzDeployment”.</span><span class="sxs-lookup"><span data-stu-id="cb43e-375">Removed '-ApiVersion' parameter from '\*-AzDeployment' cmdlets.</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb43e-376">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb43e-376">Az.Sql</span></span>
* <span data-ttu-id="cb43e-377">Korrigerade ett problem där New-AzSqlDatabaseExport misslyckas om networkIsolation inte har angetts [#13097]</span><span class="sxs-lookup"><span data-stu-id="cb43e-377">Fixed issue where New-AzSqlDatabaseExport fails if networkIsolation not specified [#13097]</span></span>
* <span data-ttu-id="cb43e-378">Korrigerade ett problem där New-AzSqlDatabaseExport och New-AzSqlDatabaseImport inte returnerade OperationStatusLink i resultatobjektet [#13097]</span><span class="sxs-lookup"><span data-stu-id="cb43e-378">Fixed issue where New-AzSqlDatabaseExport and New-AzSqlDatabaseImport were not returning OperationStatusLink in the result object [#13097]</span></span>
* <span data-ttu-id="cb43e-379">Uppdatera webbadresser för Azure-kopplade regioner i redundansvarningar för Backup Storage</span><span class="sxs-lookup"><span data-stu-id="cb43e-379">Update Azure Paired Regions URL in Backup Storage Redundancy Warnings</span></span> 

#### <a name="azstorage"></a><span data-ttu-id="cb43e-380">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb43e-380">Az.Storage</span></span>
* <span data-ttu-id="cb43e-381">Tog bort den föråldrade egenskapen RestorePolicy.LastEnabledTime</span><span class="sxs-lookup"><span data-stu-id="cb43e-381">Removed obsolete property RestorePolicy.LastEnabledTime</span></span>
    - <span data-ttu-id="cb43e-382">"Enable-AzStorageBlobRestorePolicy"</span><span class="sxs-lookup"><span data-stu-id="cb43e-382">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="cb43e-383">"Disable-AzStorageBlobRestorePolicy"</span><span class="sxs-lookup"><span data-stu-id="cb43e-383">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="cb43e-384">”Get-AzStorageBlobServiceProperty”</span><span class="sxs-lookup"><span data-stu-id="cb43e-384">'Get-AzStorageBlobServiceProperty'</span></span>
    - <span data-ttu-id="cb43e-385">”Update-AzStorageBlobServiceProperty”</span><span class="sxs-lookup"><span data-stu-id="cb43e-385">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="cb43e-386">Vill du ändra typen av DaysAfterModificationGreaterThan från int till int?</span><span class="sxs-lookup"><span data-stu-id="cb43e-386">Change Type of DaysAfterModificationGreaterThan from int to int?</span></span>
    - <span data-ttu-id="cb43e-387">"Set-AzStorageAccountManagementPolicy"</span><span class="sxs-lookup"><span data-stu-id="cb43e-387">'Set-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="cb43e-388">"Get-AzStorageAccountManagementPolicy"</span><span class="sxs-lookup"><span data-stu-id="cb43e-388">'Get-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="cb43e-389">"Add-AzStorageAccountManagementPolicyAction"</span><span class="sxs-lookup"><span data-stu-id="cb43e-389">'Add-AzStorageAccountManagementPolicyAction'</span></span>
    - <span data-ttu-id="cb43e-390">"New-AzStorageAccountManagementPolicyRule"</span><span class="sxs-lookup"><span data-stu-id="cb43e-390">'New-AzStorageAccountManagementPolicyRule'</span></span>
* <span data-ttu-id="cb43e-391">Stöd för skapa/uppdatera filresurs med åtkomstnivå</span><span class="sxs-lookup"><span data-stu-id="cb43e-391">Supported create/update file share with access tier</span></span>
    - <span data-ttu-id="cb43e-392">”New-AzRmStorageShare”</span><span class="sxs-lookup"><span data-stu-id="cb43e-392">'New-AzRmStorageShare'</span></span>
    - <span data-ttu-id="cb43e-393">”Update-AzRmStorageShare”</span><span class="sxs-lookup"><span data-stu-id="cb43e-393">'Update-AzRmStorageShare'</span></span>
* <span data-ttu-id="cb43e-394">Stöd för att konfigurera/uppdatera/ta bort ACL som stöds rekursivt på Datalake Gen2-objekt</span><span class="sxs-lookup"><span data-stu-id="cb43e-394">Supported set/update/remove Acl recursively on Datalake Gen2 item</span></span> 
    -  <span data-ttu-id="cb43e-395">”Set-AzDataLakeGen2AclRecursive”</span><span class="sxs-lookup"><span data-stu-id="cb43e-395">'Set-AzDataLakeGen2AclRecursive'</span></span> 
    -  <span data-ttu-id="cb43e-396">”Update-AzDataLakeGen2AclRecursive”</span><span class="sxs-lookup"><span data-stu-id="cb43e-396">'Update-AzDataLakeGen2AclRecursive'</span></span> 
    -  <span data-ttu-id="cb43e-397">”Remove-AzDataLakeGen2AclRecursive”</span><span class="sxs-lookup"><span data-stu-id="cb43e-397">'Remove-AzDataLakeGen2AclRecursive'</span></span>
* <span data-ttu-id="cb43e-398">Stöd för åtkomstprincip för containrar med de nya behörigheterna x, t</span><span class="sxs-lookup"><span data-stu-id="cb43e-398">Supported Container access policy with new permission x,t</span></span>
    -  <span data-ttu-id="cb43e-399">”New-AzStorageContainerStoredAccessPolicy”</span><span class="sxs-lookup"><span data-stu-id="cb43e-399">'New-AzStorageContainerStoredAccessPolicy'</span></span>
    -  <span data-ttu-id="cb43e-400">"Set-AzStorageContainerStoredAccessPolicy"</span><span class="sxs-lookup"><span data-stu-id="cb43e-400">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
* <span data-ttu-id="cb43e-401">Ändrade utdata från cmdleten hämta/ange åtkomstprincip för containrar genom att ändra behörighetstypen för den underordnade egenskapen från uppräkning till sträng</span><span class="sxs-lookup"><span data-stu-id="cb43e-401">Changed the output of get/set Container access policy cmdlet, by change the child property Permission type from enum to String</span></span>
    -  <span data-ttu-id="cb43e-402">"Get-AzStorageContainerStoredAccessPolicy"</span><span class="sxs-lookup"><span data-stu-id="cb43e-402">'Get-AzStorageContainerStoredAccessPolicy'</span></span>
    -  <span data-ttu-id="cb43e-403">"Set-AzStorageContainerStoredAccessPolicy"</span><span class="sxs-lookup"><span data-stu-id="cb43e-403">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
* <span data-ttu-id="cb43e-404">Korrigerade ett problem med exempelskript för att ange hanteringsprincip med JSON</span><span class="sxs-lookup"><span data-stu-id="cb43e-404">Fixed a sample script issue of set management policy with json</span></span>
    -  <span data-ttu-id="cb43e-405">"Set-AzStorageAccountManagementPolicy"</span><span class="sxs-lookup"><span data-stu-id="cb43e-405">'Set-AzStorageAccountManagementPolicy'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cb43e-406">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb43e-406">Az.Websites</span></span>
* <span data-ttu-id="cb43e-407">Lade till stöd för Premium V3-prisnivån</span><span class="sxs-lookup"><span data-stu-id="cb43e-407">Added support for Premium V3 pricing tier</span></span>
* <span data-ttu-id="cb43e-408">Uppdaterade SDK för WebSites till 3.1.0</span><span class="sxs-lookup"><span data-stu-id="cb43e-408">Updated the WebSites SDK to 3.1.0</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="cb43e-409">Tack till våra community-deltagare</span><span class="sxs-lookup"><span data-stu-id="cb43e-409">Thanks to our community contributors</span></span>
* <span data-ttu-id="cb43e-410">@atul-ram, uppdatera Get-AzDelegation.md (#13176)</span><span class="sxs-lookup"><span data-stu-id="cb43e-410">@atul-ram, Update Get-AzDelegation.md (#13176)</span></span>
* <span data-ttu-id="cb43e-411">@dineshreddy007, hämta approller som har tilldelats korrekt om Stack HCI-registrering använder WAC-token.</span><span class="sxs-lookup"><span data-stu-id="cb43e-411">@dineshreddy007, Get the App Roles assigned correctly in case of Stack HCI registration using WAC token.</span></span> <span data-ttu-id="cb43e-412">(#13249)</span><span class="sxs-lookup"><span data-stu-id="cb43e-412">(#13249)</span></span>
* <span data-ttu-id="cb43e-413">@kongou-ae, uppdatera New-AzOffice365PolicyProperty.md (#13217)</span><span class="sxs-lookup"><span data-stu-id="cb43e-413">@kongou-ae, Update New-AzOffice365PolicyProperty.md (#13217)</span></span>
* <span data-ttu-id="cb43e-414">Lohith Chowdary Chilukuri (@Lochiluk), uppdatera Set-AzApplicationGateway.md (#13150)</span><span class="sxs-lookup"><span data-stu-id="cb43e-414">Lohith Chowdary Chilukuri (@Lochiluk), Update Set-AzApplicationGateway.md (#13150)</span></span>
* <span data-ttu-id="cb43e-415">Matthew Burleigh (@mburleigh)</span><span class="sxs-lookup"><span data-stu-id="cb43e-415">Matthew Burleigh (@mburleigh)</span></span>
  * <span data-ttu-id="cb43e-416">Lägg till länkar till de PowerShell-cmdletar som refereras i dokumentet (#13203)</span><span class="sxs-lookup"><span data-stu-id="cb43e-416">Add links to PowerShell cmdlets referenced in the document (#13203)</span></span>
  * <span data-ttu-id="cb43e-417">Lägg till länkar till de PowerShell-cmdletar som refereras i dokumentet (#13190)</span><span class="sxs-lookup"><span data-stu-id="cb43e-417">Add links to PowerShell cmdlets referenced in the document (#13190)</span></span>
  * <span data-ttu-id="cb43e-418">Lägg till länkar till de PowerShell-cmdletar som refereras i dokumentet (#13189)</span><span class="sxs-lookup"><span data-stu-id="cb43e-418">Add links to PowerShell cmdlets referenced in the document (#13189)</span></span>
  * <span data-ttu-id="cb43e-419">lägg till länkar till cmdletar som refereras (#13137)</span><span class="sxs-lookup"><span data-stu-id="cb43e-419">add links to referenced cmdlets (#13137)</span></span>
  * <span data-ttu-id="cb43e-420">Lägg till länkar till de PowerShell-cmdletar som refereras i dokumentet (#13204)</span><span class="sxs-lookup"><span data-stu-id="cb43e-420">Add links to PowerShell cmdlets referenced in the document (#13204)</span></span>
  * <span data-ttu-id="cb43e-421">Lägg till länkar till de PowerShell-cmdletar som refereras i dokumentet (#13205)</span><span class="sxs-lookup"><span data-stu-id="cb43e-421">Add links to PowerShell cmdlets referenced in the document (#13205)</span></span>

## <a name="480---october-2020"></a><span data-ttu-id="cb43e-422">4.8.0 – oktober 2020</span><span class="sxs-lookup"><span data-stu-id="cb43e-422">4.8.0 - October 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cb43e-423">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb43e-423">Az.Accounts</span></span>
* <span data-ttu-id="cb43e-424">Åtgärdat DateTime-parsningsfel i vanliga bibliotek [#13045]</span><span class="sxs-lookup"><span data-stu-id="cb43e-424">Fixed DateTime parse issue in common libraries [#13045]</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="cb43e-425">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cb43e-425">Az.CognitiveServices</span></span>
* <span data-ttu-id="cb43e-426">Cmdleten New-AzCognitiveServicesAccountApiProperty har lagts till.</span><span class="sxs-lookup"><span data-stu-id="cb43e-426">Added 'New-AzCognitiveServicesAccountApiProperty' cmdlet.</span></span>
* <span data-ttu-id="cb43e-427">Stöd för parametern ApiProperty för New-AzCognitiveServicesAccount och Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="cb43e-427">Supported 'ApiProperty' parameter for 'New-AzCognitiveServicesAccount' and 'Set-AzCognitiveServicesAccount'</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb43e-428">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb43e-428">Az.Compute</span></span>
* <span data-ttu-id="cb43e-429">Åtgärdat problem i Update-ASRRecoveryPlan genom att fylla i FailoverTypes</span><span class="sxs-lookup"><span data-stu-id="cb43e-429">Fixed issue in 'Update-ASRRecoveryPlan' by populating FailoverTypes</span></span>
* <span data-ttu-id="cb43e-430">De valfria parametrarna -Top och -OrderBy har lagts till i cmdleten Get-AzVmImage.</span><span class="sxs-lookup"><span data-stu-id="cb43e-430">Added the '-Top' and '-OrderBy' optional parameters to the 'Get-AzVmImage' cmdlet.</span></span> 

#### <a name="azdatabricks"></a><span data-ttu-id="cb43e-431">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="cb43e-431">Az.Databricks</span></span>
* <span data-ttu-id="cb43e-432">Allmän tillgänglighet för modulen Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="cb43e-432">General availability of 'Az.Databricks' module</span></span>
* <span data-ttu-id="cb43e-433">Stöd har lagts till för virtuell nätverkspeering</span><span class="sxs-lookup"><span data-stu-id="cb43e-433">Added support for virtual network peering</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cb43e-434">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cb43e-434">Az.DataFactory</span></span>
* <span data-ttu-id="cb43e-435">Skrivfel har åtgärdats i utdatameddelanden</span><span class="sxs-lookup"><span data-stu-id="cb43e-435">Fixed typo in output messages</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="cb43e-436">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="cb43e-436">Az.EventHub</span></span>
* <span data-ttu-id="cb43e-437">Den valfria switchparametern TrustedServiceAccessEnabled har lagts till i cmdleten Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="cb43e-437">Added optional switch parameter 'TrustedServiceAccessEnabled' to 'Set-AzEventHubNetworkRuleSet' cmdlet</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="cb43e-438">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cb43e-438">Az.HDInsight</span></span>
* <span data-ttu-id="cb43e-439">Ett varningsmeddelande om att parametrarna PublicNetworkAccessType och OutboundPublicNetworkAccessType planeras att göras inaktuella har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-439">Added warning message for planning to deprecate the parameters 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType'</span></span>
* <span data-ttu-id="cb43e-440">Ett varningsmeddelande om att parametern DefaultStorageAccountName planeras att ersättas med StorageAccountResourceId har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-440">Added warning message for planning to replace the parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
* <span data-ttu-id="cb43e-441">Ett varningsmeddelande om att parametern DefaultStorageAccountKey planeras att ersättas med StorageAccountKey har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-441">Added warning message for planning to replace the parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
* <span data-ttu-id="cb43e-442">Ett varningsmeddelande om att parametern DefaultStorageAccountType planeras att ersättas med StorageAccountType har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-442">Added warning message for planning to replace the parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
* <span data-ttu-id="cb43e-443">Ett varningsmeddelande om att parametern DefaultStorageContainer planeras att ersättas med StorageContainer har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-443">Added warning message for planning to replace the parameter 'DefaultStorageContainer' with 'StorageContainer'</span></span>
* <span data-ttu-id="cb43e-444">Ett varningsmeddelande om att parametern DefaultStorageRootPath planeras att ersättas med StorageRootPath har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-444">Added warning message for planning to replace the parameter 'DefaultStorageRootPath' with 'StorageRootPath'</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cb43e-445">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cb43e-445">Az.IotHub</span></span>
* <span data-ttu-id="cb43e-446">SDK för enheter har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="cb43e-446">Updated devices sdk.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cb43e-447">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cb43e-447">Az.KeyVault</span></span>
* <span data-ttu-id="cb43e-448">Detaljerat datum för borttagning av egenskapen SecretValueText har tillhandahållits</span><span class="sxs-lookup"><span data-stu-id="cb43e-448">Provided the detailed date of removing property SecretValueText</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="cb43e-449">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="cb43e-449">Az.ManagedServices</span></span>
* <span data-ttu-id="cb43e-450">Varningar om icke-bakåtkompatibla ändringar för cmdletar för tilldelning och definition av hanterade tjänster har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="cb43e-450">Updated breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cb43e-451">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cb43e-451">Az.Monitor</span></span>
* <span data-ttu-id="cb43e-452">Felet som gjorde att ett varningsmeddelande inte kunde ignoreras har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="cb43e-452">Fixed the bug that warning message cannot be suppressed.</span></span> <span data-ttu-id="cb43e-453">[#12889]</span><span class="sxs-lookup"><span data-stu-id="cb43e-453">[#12889]</span></span>
* <span data-ttu-id="cb43e-454">Stöd för parametern SkipMetricValidation i aviseringsregelvillkor.</span><span class="sxs-lookup"><span data-stu-id="cb43e-454">Supported 'SkipMetricValidation' parameter in alert rule criteria.</span></span> <span data-ttu-id="cb43e-455">Tillåter att du skapar en aviseringsregel för ett anpassat mått som inte har genererats än, genom att göra så att måttverifieringen hoppas över.</span><span class="sxs-lookup"><span data-stu-id="cb43e-455">Allows creating an alert rule on a custom metric that isn't yet emitted, by causing the metric validation to be skipped.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb43e-456">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb43e-456">Az.Network</span></span>
* <span data-ttu-id="cb43e-457">Office365-princip har lagts till för VPNSite-resurs</span><span class="sxs-lookup"><span data-stu-id="cb43e-457">Added Office365 Policy to VPNSite Resource</span></span>
    - <span data-ttu-id="cb43e-458">New-AzO365PolicyProperty</span><span class="sxs-lookup"><span data-stu-id="cb43e-458">'New-AzO365PolicyProperty'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cb43e-459">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb43e-459">Az.RecoveryServices</span></span>
* <span data-ttu-id="cb43e-460">Verifiering av containernamn har lagts till för arbetsbelastningssäkerhetskopior.</span><span class="sxs-lookup"><span data-stu-id="cb43e-460">Added container name validation for workload backup.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="cb43e-461">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="cb43e-461">Az.RedisCache</span></span>
* <span data-ttu-id="cb43e-462">En korrigering har gjorts så att cmdletarna New-AzRedisCache och Set-AzRedisCache inte misslyckas på grund av behörighetsproblem som rör registrering av Microsoft.Cache RP</span><span class="sxs-lookup"><span data-stu-id="cb43e-462">Made 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets not fail because of permission issue related to registering Microsoft.Cache RP</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb43e-463">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb43e-463">Az.Sql</span></span>
* <span data-ttu-id="cb43e-464">BackupStorageRedundancy har lagts till i:</span><span class="sxs-lookup"><span data-stu-id="cb43e-464">Added BackupStorageRedundancy to the following:</span></span> 
    - <span data-ttu-id="cb43e-465">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="cb43e-465">'Restore-AzureRmSqlDatabase'</span></span>
    - <span data-ttu-id="cb43e-466">New-AzSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="cb43e-466">'New-AzSqlDatabaseCopy'</span></span>
    - <span data-ttu-id="cb43e-467">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="cb43e-467">'New-AzSqlDatabaseSecondary'</span></span>
* <span data-ttu-id="cb43e-468">Skiftlägeskänslighet har tagits bort för parametern BackupStorageRedundancy för alla SQL DB-referenser</span><span class="sxs-lookup"><span data-stu-id="cb43e-468">Removed case sensitivity for BackupStorageRedundancy parameter for all SQL DB references</span></span> 
* <span data-ttu-id="cb43e-469">Namnen på BackupStorageRedundancy-varningsmeddelanden har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="cb43e-469">Updated BackupStorageRedundancy warning message names</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cb43e-470">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb43e-470">Az.Storage</span></span>
* <span data-ttu-id="cb43e-471">Stöd för att aktivera/inaktivera/hämta egenskaper för mjuk borttagning av resurser för filtjänst för ett lagringskonto</span><span class="sxs-lookup"><span data-stu-id="cb43e-471">Supported enable/disable/get share soft delete properties on file Service of a Storage account</span></span>
    - <span data-ttu-id="cb43e-472">Update-AzStorageFileServiceProperty</span><span class="sxs-lookup"><span data-stu-id="cb43e-472">'Update-AzStorageFileServiceProperty'</span></span>
    - <span data-ttu-id="cb43e-473">Get-AzStorageFileServiceProperty</span><span class="sxs-lookup"><span data-stu-id="cb43e-473">'Get-AzStorageFileServiceProperty'</span></span>
* <span data-ttu-id="cb43e-474">Stöd för att visa filresurser inkluderar borttagna filresurser för ett lagringskonto och hämta förbrukning av enskild filresurs</span><span class="sxs-lookup"><span data-stu-id="cb43e-474">Supported list file shares include the deleted ones of a Storage account, and Get single file share usage</span></span>
    - <span data-ttu-id="cb43e-475">”Get-AzRmStorageShare”</span><span class="sxs-lookup"><span data-stu-id="cb43e-475">'Get-AzRmStorageShare'</span></span>
* <span data-ttu-id="cb43e-476">Stöd för återställning av en borttagen filresurs</span><span class="sxs-lookup"><span data-stu-id="cb43e-476">Supported restore a deleted file share</span></span>
    - <span data-ttu-id="cb43e-477">Restore-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="cb43e-477">'Restore-AzRmStorageShare'</span></span>
* <span data-ttu-id="cb43e-478">Cmdletarna för ändring av egenskaper för Blob Service har ändrats. De ursprungliga egenskaperna hämtas inte från servern utan anger bara de ändrade egenskaperna till servern.</span><span class="sxs-lookup"><span data-stu-id="cb43e-478">Changed the cmdlets for modify blob service properties, won't get the original properties from server, but only set the modified properties to server.</span></span>
    - <span data-ttu-id="cb43e-479">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="cb43e-479">'Enable-AzStorageBlobDeleteRetentionPolicy'</span></span>
    - <span data-ttu-id="cb43e-480">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="cb43e-480">'Disable-AzStorageBlobDeleteRetentionPolicy'</span></span>  
    - <span data-ttu-id="cb43e-481">"Enable-AzStorageBlobRestorePolicy"</span><span class="sxs-lookup"><span data-stu-id="cb43e-481">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="cb43e-482">"Disable-AzStorageBlobRestorePolicy"</span><span class="sxs-lookup"><span data-stu-id="cb43e-482">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="cb43e-483">”Update-AzStorageBlobServiceProperty”</span><span class="sxs-lookup"><span data-stu-id="cb43e-483">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="cb43e-484">Åtgärdat hjälpproblem för New-AzStorageAccount-parametern -Kind default value [#12189]</span><span class="sxs-lookup"><span data-stu-id="cb43e-484">Fixed help issue for New-AzStorageAccount parameter -Kind default value [#12189]</span></span>
* <span data-ttu-id="cb43e-485">Åtgärdat problem genom att lägga till exempel som visar hur ContentType anges på korrekt sätt i en blobuppladdning [#12989]</span><span class="sxs-lookup"><span data-stu-id="cb43e-485">Fixed issue by add example to show how to set correct ContentType in blob upload [#12989]</span></span>

## <a name="470---september-2020"></a><span data-ttu-id="cb43e-486">4.7.0 – September 2020</span><span class="sxs-lookup"><span data-stu-id="cb43e-486">4.7.0 - September 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cb43e-487">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb43e-487">Az.Accounts</span></span>
* <span data-ttu-id="cb43e-488">Formaterat kommande meddelanden om icke-bakåtkompatibel ändring</span><span class="sxs-lookup"><span data-stu-id="cb43e-488">Formatted the upcoming breaking change messages</span></span>
* <span data-ttu-id="cb43e-489">Uppdaterat Azure.Core till 1.4.1</span><span class="sxs-lookup"><span data-stu-id="cb43e-489">Updated Azure.Core to 1.4.1</span></span>

#### <a name="azaks"></a><span data-ttu-id="cb43e-490">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="cb43e-490">Az.Aks</span></span>
* <span data-ttu-id="cb43e-491">Valideringslogiken för parametern "New-AzAksCluster", "Set-AzAksCluster" och "New-AzAksNodePool" har lagts till på klientsidan.</span><span class="sxs-lookup"><span data-stu-id="cb43e-491">Added client side parameter validation logic for 'New-AzAksCluster', 'Set-AzAksCluster' and 'New-AzAksNodePool'.</span></span> <span data-ttu-id="cb43e-492">[#12372]</span><span class="sxs-lookup"><span data-stu-id="cb43e-492">[#12372]</span></span>
* <span data-ttu-id="cb43e-493">Stöd har lagts till för tillägg i "New-AzAksCluster".</span><span class="sxs-lookup"><span data-stu-id="cb43e-493">Added support for add-ons in 'New-AzAksCluster'.</span></span> <span data-ttu-id="cb43e-494">[#11239]</span><span class="sxs-lookup"><span data-stu-id="cb43e-494">[#11239]</span></span>
* <span data-ttu-id="cb43e-495">Cmdlet:arna "Enable-AzAksAddOn" och "Disable-AzAksAddOn" har lagts till för tillägg.</span><span class="sxs-lookup"><span data-stu-id="cb43e-495">Added cmdlets 'Enable-AzAksAddOn' and 'Disable-AzAksAddOn' for add-ons.</span></span> <span data-ttu-id="cb43e-496">[#11239]</span><span class="sxs-lookup"><span data-stu-id="cb43e-496">[#11239]</span></span>
* <span data-ttu-id="cb43e-497">Parametern "GenerateSshKey" har lagts till för "New-AzAksCluster".</span><span class="sxs-lookup"><span data-stu-id="cb43e-497">Added parameter 'GenerateSshKey' for 'New-AzAksCluster'.</span></span> <span data-ttu-id="cb43e-498">[#12371]</span><span class="sxs-lookup"><span data-stu-id="cb43e-498">[#12371]</span></span>
* <span data-ttu-id="cb43e-499">API-versionen har uppdaterats till 2020-06-01.</span><span class="sxs-lookup"><span data-stu-id="cb43e-499">Updated api version to 2020-06-01.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="cb43e-500">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cb43e-500">Az.CognitiveServices</span></span>
* <span data-ttu-id="cb43e-501">Visade ytterligare juridiska villkor för vissa API:er.</span><span class="sxs-lookup"><span data-stu-id="cb43e-501">Showed additional legal terms for certain APIs.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb43e-502">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb43e-502">Az.Compute</span></span>
* <span data-ttu-id="cb43e-503">Den valfria parametern "EncryptionType" har lagts till i "New-AzVmDiskEncryptionSetConfig"</span><span class="sxs-lookup"><span data-stu-id="cb43e-503">Added the '-EncryptionType' optional parameter to 'New-AzVmDiskEncryptionSetConfig'</span></span>
* <span data-ttu-id="cb43e-504">Nya cmdlet:ar för ny resurs typ: DiskAccess "Get-AzDiskAccess", "New-AzDiskAccess", "Get-AzDiskAccess"</span><span class="sxs-lookup"><span data-stu-id="cb43e-504">New cmdlets for new resource type: DiskAccess 'Get-AzDiskAccess', 'New-AzDiskAccess', 'Get-AzDiskAccess'</span></span>
* <span data-ttu-id="cb43e-505">De valfria parametrarna "-DiskAccessId" och "-NetworkAccessPolicy" har lagts till i "New-AzSnapshotConfig"</span><span class="sxs-lookup"><span data-stu-id="cb43e-505">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzSnapshotConfig'</span></span>
* <span data-ttu-id="cb43e-506">De valfria parametrarna "-DiskAccessId" och "-NetworkAccessPolicy" har lagts till i "New-AzDiskConfig"</span><span class="sxs-lookup"><span data-stu-id="cb43e-506">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzDiskConfig'</span></span>
* <span data-ttu-id="cb43e-507">PatchStatus-egenskapen har lagts till i VirtualMachine-instansvyn</span><span class="sxs-lookup"><span data-stu-id="cb43e-507">Added 'PatchStatus' property to VirtualMachine Instance View</span></span>
* <span data-ttu-id="cb43e-508">Egenskapen "VMHealth" har lagts till i den virtuella datorns instansvy, vilket är det returnerade objektet när "get-AzVm" anropas med "-Status"</span><span class="sxs-lookup"><span data-stu-id="cb43e-508">Added 'VMHealth' property to the virtual machine's instance view, which is the returned object when 'Get-AzVm' is invoked with '-Status'</span></span>
* <span data-ttu-id="cb43e-509">Fältet "AssignedHost" har lagts till i instansvyerna "Get-AzVM" och "Get-AzVmss".</span><span class="sxs-lookup"><span data-stu-id="cb43e-509">Added 'AssignedHost' field to 'Get-AzVM' and 'Get-AzVmss' instance views.</span></span> <span data-ttu-id="cb43e-510">I fältet visas resurs-ID för den virtuella datorinstansen</span><span class="sxs-lookup"><span data-stu-id="cb43e-510">The field shows the resource id of the virtual machine instance</span></span>
* <span data-ttu-id="cb43e-511">Den valfria parametern "-SupportAutomaticPlacement" har lagts till i "New-AzHostGroup"</span><span class="sxs-lookup"><span data-stu-id="cb43e-511">Added optional parameter '-SupportAutomaticPlacement' to 'New-AzHostGroup'</span></span> 
* <span data-ttu-id="cb43e-512">Parametern "-HostGroupId" har lagts till i "New-AzVm" och "New-AzVmss"</span><span class="sxs-lookup"><span data-stu-id="cb43e-512">Added the '-HostGroupId' parameter to 'New-AzVm' and 'New-AzVmss'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cb43e-513">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cb43e-513">Az.DataFactory</span></span>
* <span data-ttu-id="cb43e-514">ADF .Net SDK har uppdaterats till version 4.11.0</span><span class="sxs-lookup"><span data-stu-id="cb43e-514">Updated ADF .Net SDK version to 4.11.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="cb43e-515">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="cb43e-515">Az.EventHub</span></span>
* <span data-ttu-id="cb43e-516">Nya kluster-cmdlet:ar – "New-AzEventHubCluster", "Set-AzEventHubCluster", "Get-AzEventHubCluster", "Remove-AzEventHubCluster", "Get-AzEventHubClustersAvailableRegions" har lagts till.</span><span class="sxs-lookup"><span data-stu-id="cb43e-516">Added new Cluster cmdlets - 'New-AzEventHubCluster', 'Set-AzEventHubCluster', 'Get-AzEventHubCluster', 'Remove-AzEventHubCluster', 'Get-AzEventHubClustersAvailableRegions'.</span></span>
* <span data-ttu-id="cb43e-517">Åtgärdat för ärende #10722 : Korrigering för tilldelning av enbart lyssning till AuthorizationRule-rättigheter.</span><span class="sxs-lookup"><span data-stu-id="cb43e-517">Fixed for issue #10722 : Fix for assigning only 'Listen' to AuthorizationRule rights.</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="cb43e-518">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="cb43e-518">Az.Functions</span></span>
* <span data-ttu-id="cb43e-519">Möjligheten att skapa v2-funktioner i regioner som inte stöder det har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="cb43e-519">Removed the ability to create v2 Functions in regions that do not support it.</span></span>
* <span data-ttu-id="cb43e-520">Föråldrad PowerShell 6.2.</span><span class="sxs-lookup"><span data-stu-id="cb43e-520">Deprecated PowerShell 6.2.</span></span> <span data-ttu-id="cb43e-521">En varning har lagts till när en användare skapar en PowerShell 6.2-funktionsapp som uppmanar till att skapa en PowerShell 7.0-funktionsapp i stället.</span><span class="sxs-lookup"><span data-stu-id="cb43e-521">Added a warning for when a user creates a PowerShell 6.2 function app that advises them to create a PowerShell 7.0 function app instead.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="cb43e-522">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cb43e-522">Az.HDInsight</span></span>
* <span data-ttu-id="cb43e-523">Stöd för att skapa kluster med automatisk skalningskonfiguration</span><span class="sxs-lookup"><span data-stu-id="cb43e-523">Supported creating cluster with Autoscale configuration</span></span>
    - <span data-ttu-id="cb43e-524">Lägg till den nya parametern "AutoscaleConfiguration" till cmdleten ”New-AzHDInsightCluster”</span><span class="sxs-lookup"><span data-stu-id="cb43e-524">Add new parameter 'AutoscaleConfiguration' to the cmdlet 'New-AzHDInsightCluster'</span></span>
* <span data-ttu-id="cb43e-525">Stöd för att använda automatisk skalningskonfiguration i kluster</span><span class="sxs-lookup"><span data-stu-id="cb43e-525">Supported operating cluster's Autoscale configuration</span></span>
    - <span data-ttu-id="cb43e-526">Lägg till ny cmdlet "Get-AzHDInsihgtClusterAutoscaleConfiguration"</span><span class="sxs-lookup"><span data-stu-id="cb43e-526">Add new cmdlet 'Get-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="cb43e-527">Lägg till ny cmdlet "New-AzHDInsihgtClusterAutoscaleConfiguration"</span><span class="sxs-lookup"><span data-stu-id="cb43e-527">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="cb43e-528">Lägg till ny cmdlet "Set-AzHDInsihgtClusterAutoscaleConfiguration"</span><span class="sxs-lookup"><span data-stu-id="cb43e-528">Add new cmdlet 'Set-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="cb43e-529">Lägg till ny cmdlet "Remove-AzHDInsihgtClusterAutoscaleConfiguration"</span><span class="sxs-lookup"><span data-stu-id="cb43e-529">Add new cmdlet 'Remove-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="cb43e-530">Lägg till ny cmdlet "New-AzHDInsihgtClusterAutoscaleScheduleCondition"</span><span class="sxs-lookup"><span data-stu-id="cb43e-530">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleScheduleCondition'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cb43e-531">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cb43e-531">Az.KeyVault</span></span>
* <span data-ttu-id="cb43e-532">Stöd har lagts till för RBAC-auktorisering [#10557]</span><span class="sxs-lookup"><span data-stu-id="cb43e-532">Added support for RBAC authorization [#10557]</span></span>
* <span data-ttu-id="cb43e-533">Förbättrad felhantering i "Set-AzKeyVaultAccessPolicy" [#4007]</span><span class="sxs-lookup"><span data-stu-id="cb43e-533">Enhanced error handling in 'Set-AzKeyVaultAccessPolicy' [#4007]</span></span>

#### <a name="azkusto"></a><span data-ttu-id="cb43e-534">Az.Kusto</span><span class="sxs-lookup"><span data-stu-id="cb43e-534">Az.Kusto</span></span>
* <span data-ttu-id="cb43e-535">Allmän tillgänglighet för "Az.Kusto"-modulen</span><span class="sxs-lookup"><span data-stu-id="cb43e-535">General availability of 'Az.Kusto' module</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb43e-536">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb43e-536">Az.Network</span></span>
* <span data-ttu-id="cb43e-537">[Viktig ändring] Uppdaterade nedanstående cmdlets för att justera resursens virtuella router och virtuella hubb</span><span class="sxs-lookup"><span data-stu-id="cb43e-537">[Breaking Change] Updated below cmdlets to align resource virtual router and virtual hub</span></span>
    - <span data-ttu-id="cb43e-538">"New-AzVirtualRouter":</span><span class="sxs-lookup"><span data-stu-id="cb43e-538">'New-AzVirtualRouter':</span></span> 
        - <span data-ttu-id="cb43e-539">Parametern-HostedSubnet har lagts till för att stödja underordnad resurs för IP-konfiguration</span><span class="sxs-lookup"><span data-stu-id="cb43e-539">Added -HostedSubnet parameter to support IP configuration child resource</span></span>
        - <span data-ttu-id="cb43e-540">-HostedGateway och -HostedGatewayId har tagits bort</span><span class="sxs-lookup"><span data-stu-id="cb43e-540">deleted -HostedGateway and -HostedGatewayId</span></span>
    - <span data-ttu-id="cb43e-541">'Get-AzVirtualRouter':</span><span class="sxs-lookup"><span data-stu-id="cb43e-541">'Get-AzVirtualRouter':</span></span>
        - <span data-ttu-id="cb43e-542">Parameteruppsättningen har lagts till på prenumerationsnivå</span><span class="sxs-lookup"><span data-stu-id="cb43e-542">Added subscription level parameter set</span></span>
    - <span data-ttu-id="cb43e-543">"Remove-AzVirtualRouter"</span><span class="sxs-lookup"><span data-stu-id="cb43e-543">'Remove-AzVirtualRouter'</span></span>
    - <span data-ttu-id="cb43e-544">"Add-AzVirtualRouterPeer"</span><span class="sxs-lookup"><span data-stu-id="cb43e-544">'Add-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="cb43e-545">"Get-AzVirtualRouterPeer"</span><span class="sxs-lookup"><span data-stu-id="cb43e-545">'Get-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="cb43e-546">"Remove-AzVirtualRouterPeer"</span><span class="sxs-lookup"><span data-stu-id="cb43e-546">'Remove-AzVirtualRouterPeer'</span></span>
* <span data-ttu-id="cb43e-547">Ny cmdlet har lagts till för Azure Express Route-port</span><span class="sxs-lookup"><span data-stu-id="cb43e-547">Added new cmdlet for Azure Express Route Port</span></span>
    - <span data-ttu-id="cb43e-548">"New-AzExpressRoutePortLOA"</span><span class="sxs-lookup"><span data-stu-id="cb43e-548">'New-AzExpressRoutePortLOA'</span></span>
* <span data-ttu-id="cb43e-549">Egenskapen RemoteBgpCommunities har lagts till i VirtualNetwork Peering-resursen</span><span class="sxs-lookup"><span data-stu-id="cb43e-549">Added RemoteBgpCommunities property to the VirtualNetwork Peering Resource</span></span>
* <span data-ttu-id="cb43e-550">Ändrade varningsmeddelandet för ”New-AzLoadBalancerFrontendIpConfig”, ”New-AzPublicIpAddress” och ”New-AzPublicIpPrefix”.</span><span class="sxs-lookup"><span data-stu-id="cb43e-550">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>
* <span data-ttu-id="cb43e-551">Lade till VpnGatewayIpConfigurations till "Get-AzVpnGateway"-utdata</span><span class="sxs-lookup"><span data-stu-id="cb43e-551">Added VpnGatewayIpConfigurations to 'Get-AzVpnGateway' output</span></span>
* <span data-ttu-id="cb43e-552">Åtgärdade bugg för "Set-AzApplicationGatewaySslCertificate" [#9488]</span><span class="sxs-lookup"><span data-stu-id="cb43e-552">Fixed bug for 'Set-AzApplicationGatewaySslCertificate' [#9488]</span></span>
* <span data-ttu-id="cb43e-553">Parametern "AllowActiveFTP" har lagts till i "AzureFirewall"</span><span class="sxs-lookup"><span data-stu-id="cb43e-553">Added 'AllowActiveFTP' parameter to 'AzureFirewall'</span></span>
* <span data-ttu-id="cb43e-554">Nedanstående kommandon för funktionen har uppdaterats: Aktivera konfiguration/borttagning för Internetsäkerhet på VirtualWan P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="cb43e-554">Updated below commands for feature: Enable internet security set/remove on VirtualWan P2SVpnGateway.</span></span>
- <span data-ttu-id="cb43e-555">"New-AzP2sVpnGateway" har uppdaterats": Den valfria växelparametern "EnableInternetSecurityFlag" har lagts till för kunder som anger värdet true för att aktivera Internetsäkerhet på P2SVpnGateway, som ska användas för plats-till-plats-klienter.</span><span class="sxs-lookup"><span data-stu-id="cb43e-555">Updated 'New-AzP2sVpnGateway': Added optional switch parameter 'EnableInternetSecurityFlag' for customers to set true to enable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
- <span data-ttu-id="cb43e-556">"Update-AzP2sVpnGateway" har uppdaterats: De valfria växelparametrarna "EnableInternetSecurityFlag" eller "DisableInternetSecurityFlag" har lagts till för kunder som anger värdet true/false för att aktivera/inaktivera Internetsäkerhet på P2SVpnGateway, som ska användas för plats-till-plats-klienter.</span><span class="sxs-lookup"><span data-stu-id="cb43e-556">Updated 'Update-AzP2sVpnGateway': Added optional switch parameters 'EnableInternetSecurityFlag' or 'DisableInternetSecurityFlag' for customers to set true/false to enable/disable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
* <span data-ttu-id="cb43e-557">Den nya cmdleten "Reset-AzP2sVpnGateway" har lagts till för att kunder ska kunna återställa/starta om sina VirtualWan-P2SVpnGateway för felsökning.</span><span class="sxs-lookup"><span data-stu-id="cb43e-557">Added new cmdlet 'Reset-AzP2sVpnGateway' for customers to reset/reboot their VirtualWan P2SVpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="cb43e-558">Den nya cmdleten "Reset-AzVpnGateway" har lagts till för att kunder ska kunna återställa/starta om VirtualWan VpnGateway för felsökning.</span><span class="sxs-lookup"><span data-stu-id="cb43e-558">Added new cmdlet 'Reset-AzVpnGateway' for customers to reset/reboot their VirtualWan VpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="cb43e-559">"Set-AzVirtualNetworkSubnetConfig" har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="cb43e-559">Updated 'Set-AzVirtualNetworkSubnetConfig'</span></span>
    - <span data-ttu-id="cb43e-560">Ange egenskaper för NSG och routningstabell för undernät till null om det anges explicit i parametrarna [#1548] [#9718]</span><span class="sxs-lookup"><span data-stu-id="cb43e-560">Set NSG and Route Table properties of subnet to null if explicitly set in parameters [#1548][#9718]</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cb43e-561">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb43e-561">Az.RecoveryServices</span></span>
* <span data-ttu-id="cb43e-562">Åtgärdat borttagningstillståndet för säkerhetskopieringsobjekt.</span><span class="sxs-lookup"><span data-stu-id="cb43e-562">Fixed the Delete State for workload Backup Items.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb43e-563">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb43e-563">Az.Resources</span></span>
* <span data-ttu-id="cb43e-564">Lagt till saknad kontroll för Set-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="cb43e-564">Added missing check for Set-AzRoleAssignment</span></span>
* <span data-ttu-id="cb43e-565">Attribut som medför icke-bakåtkompatibel ändring har lagts till i parametern "SubscriptionId" i "Get-AzResourceGroupDeploymentOperation"</span><span class="sxs-lookup"><span data-stu-id="cb43e-565">Added breaking change attribute to 'SubscriptionId' parameter of 'Get-AzResourceGroupDeploymentOperation'</span></span>
* <span data-ttu-id="cb43e-566">Uppdaterat What-If-cmdlets i ARM-mall så att resursändringar av typen 'Ignorera' visas sist</span><span class="sxs-lookup"><span data-stu-id="cb43e-566">Updated ARM template What-If cmdlets to show 'Ignore' resource changes last</span></span>
* <span data-ttu-id="cb43e-567">Åtgärdat serialiseringsproblem med säkra parametrar och matrisparametrar för distributionscmdlets [#12773]</span><span class="sxs-lookup"><span data-stu-id="cb43e-567">Fixed secure and array parameter serialization issues for deployment cmdlets [#12773]</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="cb43e-568">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cb43e-568">Az.ServiceFabric</span></span>
* <span data-ttu-id="cb43e-569">Nya cmdletar har lagts till för hanterade kluster och nodtyper:</span><span class="sxs-lookup"><span data-stu-id="cb43e-569">Added new cmdlets for managed clusters and node types:</span></span>
    - <span data-ttu-id="cb43e-570">"New-AzServiceFabricManagedCluster"</span><span class="sxs-lookup"><span data-stu-id="cb43e-570">'New-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="cb43e-571">"Get-AzServiceFabricManagedCluster"</span><span class="sxs-lookup"><span data-stu-id="cb43e-571">'Get-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="cb43e-572">"Set-AzServiceFabricManagedCluster"</span><span class="sxs-lookup"><span data-stu-id="cb43e-572">'Set-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="cb43e-573">"Remove-AzServiceFabricManagedCluster"</span><span class="sxs-lookup"><span data-stu-id="cb43e-573">'Remove-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="cb43e-574">"Add-AzServiceFabricManagedClusterClientCertificate"</span><span class="sxs-lookup"><span data-stu-id="cb43e-574">'Add-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="cb43e-575">"Remove-AzServiceFabricManagedClusterClientCertificate"</span><span class="sxs-lookup"><span data-stu-id="cb43e-575">'Remove-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="cb43e-576">"New-AzServiceFabricManagedNodeType"</span><span class="sxs-lookup"><span data-stu-id="cb43e-576">'New-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="cb43e-577">"Get-AzServiceFabricManagedNodeType"</span><span class="sxs-lookup"><span data-stu-id="cb43e-577">'Get-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="cb43e-578">"Set-AzServiceFabricManagedNodeType"</span><span class="sxs-lookup"><span data-stu-id="cb43e-578">'Set-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="cb43e-579">"Remove-AzServiceFabricManagedNodeType"</span><span class="sxs-lookup"><span data-stu-id="cb43e-579">'Remove-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="cb43e-580">"Add-AzServiceFabricManagedNodeTypeVMExtension"</span><span class="sxs-lookup"><span data-stu-id="cb43e-580">'Add-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="cb43e-581">"Add-AzServiceFabricManagedNodeTypeVMSecret"</span><span class="sxs-lookup"><span data-stu-id="cb43e-581">'Add-AzServiceFabricManagedNodeTypeVMSecret'</span></span>
    - <span data-ttu-id="cb43e-582">"Remove-AzServiceFabricManagedNodeTypeVMExtension"</span><span class="sxs-lookup"><span data-stu-id="cb43e-582">'Remove-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="cb43e-583">"Restart-AzServiceFabricManagedNodeTyp"</span><span class="sxs-lookup"><span data-stu-id="cb43e-583">'Restart-AzServiceFabricManagedNodeTyp'</span></span>
* <span data-ttu-id="cb43e-584">Service Fabric SDK har uppgraderats till version 1.2.0 som använder Service Fabric-resursprovidern med API-version 2020-03-01 för aktuell modell och 2020-01-01-förhandsversion för hanterade kluster.</span><span class="sxs-lookup"><span data-stu-id="cb43e-584">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2020-03-01 for the current model and 2020-01-01-preview for managed clusters.</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb43e-585">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb43e-585">Az.Sql</span></span>
* <span data-ttu-id="cb43e-586">BackupStorageRedundancy har lagts till i "New-AzSqlInstance" och "Get-AzSqlInstance"</span><span class="sxs-lookup"><span data-stu-id="cb43e-586">Added BackupStorageRedundancy to 'New-AzSqlInstance' and 'Get-AzSqlInstance'</span></span>
* <span data-ttu-id="cb43e-587">Cmdlet:en "Get-AzSqlServerActiveDirectoryOnlyAuthentication" har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-587">Added cmdlet 'Get-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="cb43e-588">Cmdlet:en "Enable-AzSqlServerActiveDirectoryOnlyAuthentication" har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-588">Added cmdlet 'Enable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="cb43e-589">Force-parametern har lagts till i "New-AzSqlInstance"</span><span class="sxs-lookup"><span data-stu-id="cb43e-589">Added Force parameter to 'New-AzSqlInstance'</span></span>
* <span data-ttu-id="cb43e-590">Cmdlet:ar för logguppspelningstjänst för hanterade databaser har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-590">Added cmdlets for Managed Database Log Replay service</span></span>
    - <span data-ttu-id="cb43e-591">"Start-AzSqlInstanceDatabaseLogReplay"</span><span class="sxs-lookup"><span data-stu-id="cb43e-591">'Start-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="cb43e-592">"Get-AzSqlInstanceDatabaseLogReplay"</span><span class="sxs-lookup"><span data-stu-id="cb43e-592">'Get-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="cb43e-593">"Complete-AzSqlInstanceDatabaseLogReplay"</span><span class="sxs-lookup"><span data-stu-id="cb43e-593">'Complete-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="cb43e-594">"Stop-AzSqlInstanceDatabaseLogReplay"</span><span class="sxs-lookup"><span data-stu-id="cb43e-594">'Stop-AzSqlInstanceDatabaseLogReplay'</span></span>
* <span data-ttu-id="cb43e-595">Cmdlet:en "Get-AzSqlInstanceActiveDirectoryOnlyAuthentication" har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-595">Added cmdlet 'Get-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="cb43e-596">Cmdlet:en "Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication" har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-596">Added cmdlet 'Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="cb43e-597">Cmdlet:en "Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication" har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-597">Added cmdlet 'Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="cb43e-598">Cmdletarna "New-AzSqlDatabaseImport" och "New-AzSqlDatabaseExport" har uppdaterats för att stödja funktioner för nätverksisolering</span><span class="sxs-lookup"><span data-stu-id="cb43e-598">Updated cmdlets 'New-AzSqlDatabaseImport' and 'New-AzSqlDatabaseExport' to support network isolation functionality</span></span>
* <span data-ttu-id="cb43e-599">Cmdleten "New-AzSqlDatabaseImportExisting" har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-599">Added cmdlet 'New-AzSqlDatabaseImportExisting'</span></span>
* <span data-ttu-id="cb43e-600">Uppdaterade databas-cmdlet:ar som stöder typspecifikation av lagringsenhet för säkerhetskopiering</span><span class="sxs-lookup"><span data-stu-id="cb43e-600">Updated Databases cmdlets to support backup storage type specification</span></span>
* <span data-ttu-id="cb43e-601">Force-parametern har lagts till i "New-AzSqlDatabase"</span><span class="sxs-lookup"><span data-stu-id="cb43e-601">Added Force parameter to 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="cb43e-602">Varning för BackupStorageRedundancy-konfiguration har lagts till i utvalda regioner i "New-AzSqlDatabase"</span><span class="sxs-lookup"><span data-stu-id="cb43e-602">Added warning for BackupStorageRedundancy configuration in select regions in 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="cb43e-603">Uppdaterade ActiveDirectoryOnlyAuthentication-cmdletar för server och instans så att de innehåller ResourceId och InputObject</span><span class="sxs-lookup"><span data-stu-id="cb43e-603">Updated ActiveDirectoryOnlyAuthentication cmdlets for server and instance to include ResourceId and InputObject</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cb43e-604">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb43e-604">Az.Storage</span></span>
* <span data-ttu-id="cb43e-605">Åtgärdade fel vid uppladdning av blob genom uppgradering till Microsoft.Azure.Storage.DataMovement 2.0.0 [#12220]</span><span class="sxs-lookup"><span data-stu-id="cb43e-605">Fixed upload blob fail by upgrade to Microsoft.Azure.Storage.DataMovement 2.0.0 [#12220]</span></span>
* <span data-ttu-id="cb43e-606">Stöd för återställning baserat på tidpunkt</span><span class="sxs-lookup"><span data-stu-id="cb43e-606">Supported Point In Time Restore</span></span>
    - <span data-ttu-id="cb43e-607">"Enable-AzStorageBlobRestorePolicy"</span><span class="sxs-lookup"><span data-stu-id="cb43e-607">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="cb43e-608">"Disable-AzStorageBlobRestorePolicy"</span><span class="sxs-lookup"><span data-stu-id="cb43e-608">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="cb43e-609">"New-AzStorageBlobRangeToRestore"</span><span class="sxs-lookup"><span data-stu-id="cb43e-609">'New-AzStorageBlobRangeToRestore'</span></span>
    - <span data-ttu-id="cb43e-610">"Restore-AzStorageBlobRange"</span><span class="sxs-lookup"><span data-stu-id="cb43e-610">'Restore-AzStorageBlobRange'</span></span>
* <span data-ttu-id="cb43e-611">Stöd för att hämta status för blobåterställning genom att köra get-AzureRMStorageAccount med parametern -IncludeBlobRestoreStatus</span><span class="sxs-lookup"><span data-stu-id="cb43e-611">Supported get blob restore status of Storage account by run get-AzureRMStorageAccount with parameter -IncludeBlobRestoreStatus</span></span> 
    - <span data-ttu-id="cb43e-612">"Get-AzureRMStorageAccount"</span><span class="sxs-lookup"><span data-stu-id="cb43e-612">'Get-AzureRMStorageAccount'</span></span>
* <span data-ttu-id="cb43e-613">Meddelande om icke-bakåtkompatibel ändring för kommande ändring av cmdlet-utdata har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-613">Added breaking change warning message for upcoming cmdlet output change</span></span>
    - <span data-ttu-id="cb43e-614">"Get-AzStorageContainerStoredAccessPolicy"</span><span class="sxs-lookup"><span data-stu-id="cb43e-614">'Get-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="cb43e-615">"Set-AzStorageContainerStoredAccessPolicy"</span><span class="sxs-lookup"><span data-stu-id="cb43e-615">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="cb43e-616">"Set-AzStorageAccountManagementPolicy"</span><span class="sxs-lookup"><span data-stu-id="cb43e-616">'Set-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="cb43e-617">"Get-AzStorageAccountManagementPolicy"</span><span class="sxs-lookup"><span data-stu-id="cb43e-617">'Get-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="cb43e-618">"Add-AzStorageAccountManagementPolicyAction"</span><span class="sxs-lookup"><span data-stu-id="cb43e-618">'Add-AzStorageAccountManagementPolicyAction'</span></span>
    - <span data-ttu-id="cb43e-619">"New-AzStorageAccountManagementPolicyRule"</span><span class="sxs-lookup"><span data-stu-id="cb43e-619">'New-AzStorageAccountManagementPolicyRule'</span></span>
* <span data-ttu-id="cb43e-620">Uppgraderade Microsoft.Azure.Cosmos.Table SDK till 1.0.8</span><span class="sxs-lookup"><span data-stu-id="cb43e-620">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.8</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="cb43e-621">Tack till våra community-deltagare</span><span class="sxs-lookup"><span data-stu-id="cb43e-621">Thanks to our community contributors</span></span>
* <span data-ttu-id="cb43e-622">Thomas Van Laere (@ThomVanL), Lägg till Dockerfile-alpine-3.10 (#12911)</span><span class="sxs-lookup"><span data-stu-id="cb43e-622">Thomas Van Laere (@ThomVanL), Add Dockerfile-alpine-3.10 (#12911)</span></span> 
* <span data-ttu-id="cb43e-623">Lohith Chowdary Chilukuri (@Lochiluk), Uppdatering av Remove-AzNetworkInterfaceIpConfig.md (#12807)</span><span class="sxs-lookup"><span data-stu-id="cb43e-623">Lohith Chowdary Chilukuri (@Lochiluk), Update Remove-AzNetworkInterfaceIpConfig.md (#12807)</span></span> 
* <span data-ttu-id="cb43e-624">Roberth Strand (@roberthstrand), Get-AzResourceGroup – Nytt exempel och rensning (#12828)</span><span class="sxs-lookup"><span data-stu-id="cb43e-624">Roberth Strand (@roberthstrand), Get-AzResourceGroup - New example, and cleanup (#12828)</span></span> 
* <span data-ttu-id="cb43e-625">Ravi Mishra (@inmishrar), uppdatering av Azure Web App-körningsstack till DOTNETCORE (#12833)</span><span class="sxs-lookup"><span data-stu-id="cb43e-625">Ravi Mishra (@inmishrar), update Azure Web App runtime stack to DOTNETCORE (#12833)</span></span> 
* <span data-ttu-id="cb43e-626">@jack-education, uppdaterat set-AzVirtualNetworkSubnetConfig för att tillåta att NSG och routningstabell tas bort från undernät (#12351)</span><span class="sxs-lookup"><span data-stu-id="cb43e-626">@jack-education, Updated Set-AzVirtualNetworkSubnetConfig to allow NSG and Route Table to be removed from subnet (#12351)</span></span> 
* <span data-ttu-id="cb43e-627">@hagop-globanet, uppdatering av Add-AzApplicationGatewayCustomError.md (#12784)</span><span class="sxs-lookup"><span data-stu-id="cb43e-627">@hagop-globanet, Update Add-AzApplicationGatewayCustomError.md (#12784)</span></span> 
* <span data-ttu-id="cb43e-628">Joshua Van Daalen (@greenSacrifice)</span><span class="sxs-lookup"><span data-stu-id="cb43e-628">Joshua Van Daalen (@greenSacrifice)</span></span>
  * <span data-ttu-id="cb43e-629">Uppdatering av stavning av egenskaper till egenskaper (#12821)</span><span class="sxs-lookup"><span data-stu-id="cb43e-629">Update spelling of Property to Property (#12821)</span></span> 
  * <span data-ttu-id="cb43e-630">Uppdatering av New-AzResourceLock.md-exempel (#12806)</span><span class="sxs-lookup"><span data-stu-id="cb43e-630">Update New-AzResourceLock.md examples (#12806)</span></span>
* <span data-ttu-id="cb43e-631">Eragon Riddle (@eragonriddle), korrigerat fältnamn för parameter i exemplet (#12825)</span><span class="sxs-lookup"><span data-stu-id="cb43e-631">Eragon Riddle (@eragonriddle), Corrected parameter field name in the example (#12825)</span></span> 
* <span data-ttu-id="cb43e-632">@rossifumax, åtgärdat skrivfel i New-AzConfigurationAssignment.md (#12701)</span><span class="sxs-lookup"><span data-stu-id="cb43e-632">@rossifumax, Fix typo in New-AzConfigurationAssignment.md (#12701)</span></span>

## <a name="461---august-2020"></a><span data-ttu-id="cb43e-633">4.6.1 – augusti 2020</span><span class="sxs-lookup"><span data-stu-id="cb43e-633">4.6.1 - August 2020</span></span>
#### <a name="azcompute"></a><span data-ttu-id="cb43e-634">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb43e-634">Az.Compute</span></span>
* <span data-ttu-id="cb43e-635">Korrigerade EncryptionAtHost-parametern i New-AzVm för att ta bort standardvärdet FALSE [#12776]</span><span class="sxs-lookup"><span data-stu-id="cb43e-635">Patched '-EncryptionAtHost' parameter in 'New-AzVm' to remove default value of false [#12776]</span></span>

## <a name="460---august-2020"></a><span data-ttu-id="cb43e-636">4.6.0 – augusti 2020</span><span class="sxs-lookup"><span data-stu-id="cb43e-636">4.6.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cb43e-637">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb43e-637">Az.Accounts</span></span>
* <span data-ttu-id="cb43e-638">Alla offentliga molnmiljöer läses in när slutpunktsidentifieringen inte returnerar AzureCloud (standard) eller andra offentliga miljöer [#12633]</span><span class="sxs-lookup"><span data-stu-id="cb43e-638">Loaded all public cloud environments when discovery endpoint doesn't return default AzureCloud or other public environments [#12633]</span></span>
* <span data-ttu-id="cb43e-639">SubscriptionPolicies har exponerats i Get-AzSubscription [#12551]</span><span class="sxs-lookup"><span data-stu-id="cb43e-639">Exposed SubscriptionPolicies in 'Get-AzSubscription' [#12551]</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cb43e-640">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cb43e-640">Az.Automation</span></span>
* <span data-ttu-id="cb43e-641">Parametern -RunOn har lagts till i Set-AzAutomationWebhook för att ange en Hybrid Worker-grupp</span><span class="sxs-lookup"><span data-stu-id="cb43e-641">Added '-RunOn' parameters to 'Set-AzAutomationWebhook' to specify a Hybrid Worker Group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb43e-642">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb43e-642">Az.Compute</span></span>
* <span data-ttu-id="cb43e-643">Parametern -EncryptionAtHost har lagts till i New-AzVm, New-AzVmss, New-AzVMConfig, New-AzVmssConfig, Update-AzVM och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="cb43e-643">Added '-EncryptionAtHost' parameter to 'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM', and 'Update-AzVmss'</span></span>
* <span data-ttu-id="cb43e-644">SecurityProfile har lagts till i Get-AzVM och Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="cb43e-644">Added 'SecurityProfile' to 'Get-AzVM' and 'Get-AzVmss' return object</span></span>
* <span data-ttu-id="cb43e-645">Växeln -InstanceView har lagts till som valfri parameter i Get-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="cb43e-645">Added '-InstanceView' switch as optional parameter to 'Get-AzHostGroup'</span></span>
* <span data-ttu-id="cb43e-646">En ny cmdlet, Invoke-AzVmPatchAssessment, har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-646">Added new cmdlet 'Invoke-AzVmPatchAssessment'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cb43e-647">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cb43e-647">Az.DataFactory</span></span>
* <span data-ttu-id="cb43e-648">Saknade egenskaper har lagts till i klassen PSPipelineRun.</span><span class="sxs-lookup"><span data-stu-id="cb43e-648">Added missing properties to PSPipelineRun class.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="cb43e-649">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cb43e-649">Az.HDInsight</span></span>
* <span data-ttu-id="cb43e-650">Stöd för att skapa kluster med funktionen för kryptering under överföring.</span><span class="sxs-lookup"><span data-stu-id="cb43e-650">Supported creating cluster with encryption at host feature.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cb43e-651">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cb43e-651">Az.KeyVault</span></span>
* <span data-ttu-id="cb43e-652">Varningsmeddelanden har lagts till för planering att inaktivera mjuk borttagning</span><span class="sxs-lookup"><span data-stu-id="cb43e-652">Added warning messages for planning to disable soft delete</span></span>
* <span data-ttu-id="cb43e-653">Varningsmeddelanden har lagts till för planering att ta bort attributet SecretValueText</span><span class="sxs-lookup"><span data-stu-id="cb43e-653">Added warning messages for planning to remove attribute SecretValueText</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="cb43e-654">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="cb43e-654">Az.Maintenance</span></span>
* <span data-ttu-id="cb43e-655">Valfria schemarelaterade fält har lagts till i New-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb43e-655">Added optional schedule related fields to 'New-AzMaintenanceConfiguration'</span></span>
* <span data-ttu-id="cb43e-656">En ny cmdlet har lagts till för Get-AzMaintenancePublicConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb43e-656">Added new cmdlet for 'Get-AzMaintenancePublicConfiguration'</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="cb43e-657">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="cb43e-657">Az.ManagedServices</span></span>
* <span data-ttu-id="cb43e-658">Varningar har lagts till om icke-bakåtkompatibla ändringar för cmdletar för tilldelning och definition av hanterade tjänster</span><span class="sxs-lookup"><span data-stu-id="cb43e-658">Added breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cb43e-659">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cb43e-659">Az.Monitor</span></span>
* <span data-ttu-id="cb43e-660">Utökade parametern som angetts i Set-AzDiagnosticSetting för separering av aktivering av loggar och mått [#12482]</span><span class="sxs-lookup"><span data-stu-id="cb43e-660">Extended the parameter set in 'Set-AzDiagnosticSetting' for separation of Logs and Metrics enablement [#12482]</span></span>
* <span data-ttu-id="cb43e-661">Åtgärdat fel för Add-AzMetricAlertRuleV2 vid hämtning av måttavisering från pipelinen</span><span class="sxs-lookup"><span data-stu-id="cb43e-661">Fixed bug for 'Add-AzMetricAlertRuleV2' when getting metric alert from pipeline</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb43e-662">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb43e-662">Az.Resources</span></span>
* <span data-ttu-id="cb43e-663">Get-AzPolicyAlias-svaret har uppdaterats för att ta med information som anger om aliaset kan ändras eller inte av Azure Policy.</span><span class="sxs-lookup"><span data-stu-id="cb43e-663">Updated 'Get-AzPolicyAlias' response to include information indicating whether the alias is modifiable by Azure Policy.</span></span>
* <span data-ttu-id="cb43e-664">Skapade en ny cmdlet, set-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="cb43e-664">Created new cmdlet 'Set-AzRoleAssignment'</span></span>
* <span data-ttu-id="cb43e-665">Get-AzDeploymentManagementGroupWhatIfResult har lagts till för att hämta What-If-resultat för ARM-mall i hanteringsgruppsomfånget</span><span class="sxs-lookup"><span data-stu-id="cb43e-665">Added 'Get-AzDeploymentManagementGroupWhatIfResult' for getting ARM template What-If results at management Group scope</span></span>
* <span data-ttu-id="cb43e-666">En ny cmdlet, Get-AzTenantWhatIfResult, har lagts till för att hämta What-If-resultat för ARM-mall i klientorganisationsomfånget</span><span class="sxs-lookup"><span data-stu-id="cb43e-666">Added 'Get-AzTenantWhatIfResult' new cmdlet for getting ARM template What-If results at tenant scope</span></span>
* <span data-ttu-id="cb43e-667">-WhatIf och -Confirm har åsidosatts för New-AzManagementGroupDeployment och New-AzTenantDeployment för att använda What-If-resultat för ARM-mall</span><span class="sxs-lookup"><span data-stu-id="cb43e-667">Overrode '-WhatIf' and '-Confirm' for 'New-AzManagementGroupDeployment' and 'New-AzTenantDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="cb43e-668">Beteenden har åtgärdats för -WhatIf och -Confirm för nya cmdletar för distribution så att de stämmer överens med False och</span><span class="sxs-lookup"><span data-stu-id="cb43e-668">Fixed the behaviors of '-WhatIf' and '-Confirm' for new deployment cmdlets so they comply with False and</span></span> 
* <span data-ttu-id="cb43e-669">Serialiseringsfel har åtgärdats för -TemplateObject och TemplateParameterObject [#1528] [#6292]</span><span class="sxs-lookup"><span data-stu-id="cb43e-669">Fixed serialization error for '-TemplateObject' and 'TemplateParameterObject' [#1528] [#6292]</span></span>
* <span data-ttu-id="cb43e-670">Attribut som medför icke-bakåtkompatibel ändring har lagts till i Get-AzResourceGroupDeploymentOperation för den kommande ändringen av utdatatyp</span><span class="sxs-lookup"><span data-stu-id="cb43e-670">Added breaking change attribute to 'Get-AzResourceGroupDeploymentOperation' for the upcoming output type change</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="cb43e-671">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="cb43e-671">Az.SignalR</span></span>
* <span data-ttu-id="cb43e-672">Fel i hjälpfilerna Restart-AzSignalR och Update-AzSignalR har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="cb43e-672">Fixed 'Restart-AzSignalR' and 'Update-AzSignalR' help files errors</span></span>
* <span data-ttu-id="cb43e-673">Cmdletarna Update-AzSignalRNetworkAcl och Set-AzSignalRUpstream har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-673">Added cmdlets 'Update-AzSignalRNetworkAcl', 'Set-AzSignalRUpstream'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cb43e-674">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb43e-674">Az.Storage</span></span>
* <span data-ttu-id="cb43e-675">Stöd för blobfrågeacceleration</span><span class="sxs-lookup"><span data-stu-id="cb43e-675">Supported blob query acceleration</span></span>
    -  <span data-ttu-id="cb43e-676">Get-AzStorageBlobQueryResult</span><span class="sxs-lookup"><span data-stu-id="cb43e-676">'Get-AzStorageBlobQueryResult'</span></span>
    -  <span data-ttu-id="cb43e-677">New-AzStorageBlobQueryConfig</span><span class="sxs-lookup"><span data-stu-id="cb43e-677">'New-AzStorageBlobQueryConfig'</span></span>
* <span data-ttu-id="cb43e-678">Hjälpfil har lagts till, ytterligare beskrivning har lagts till och stavfel har korrigerats</span><span class="sxs-lookup"><span data-stu-id="cb43e-678">Updated help file, added more description, and fixed typo</span></span>
    -  <span data-ttu-id="cb43e-679">”Start-AzStorageBlobCopy”</span><span class="sxs-lookup"><span data-stu-id="cb43e-679">'Start-AzStorageBlobCopy'</span></span>
    -  <span data-ttu-id="cb43e-680">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="cb43e-680">'Get-AzDataLakeGen2Item'</span></span>
* <span data-ttu-id="cb43e-681">Problem med att ladda ned blob när relaterad underordnad katalog saknas har åtgärdats [#12592]</span><span class="sxs-lookup"><span data-stu-id="cb43e-681">Fixed download blob fail when related sub directory not exist [#12592]</span></span>
    -  <span data-ttu-id="cb43e-682">”Get-AzStorageBlobContent”</span><span class="sxs-lookup"><span data-stu-id="cb43e-682">'Get-AzStorageBlobContent'</span></span>
* <span data-ttu-id="cb43e-683">Replikeringsprincip för att ange, hämta, ta bort objekt på Storage-konton stöds</span><span class="sxs-lookup"><span data-stu-id="cb43e-683">Supported Set/Get/Remove Object Replication Policy on Storage accounts</span></span>
    - <span data-ttu-id="cb43e-684">New-AzStorageObjectReplicationPolicyRule</span><span class="sxs-lookup"><span data-stu-id="cb43e-684">'New-AzStorageObjectReplicationPolicyRule'</span></span>
    - <span data-ttu-id="cb43e-685">Set-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="cb43e-685">'Set-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="cb43e-686">Get-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="cb43e-686">'Get-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="cb43e-687">Remove-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="cb43e-687">'Remove-AzStorageObjectReplicationPolicy'</span></span>
* <span data-ttu-id="cb43e-688">Stöd har lagts till för att aktivera/inaktivera ChangeFeed i Blob Service för ett Storage-konto</span><span class="sxs-lookup"><span data-stu-id="cb43e-688">Supported enable/disable ChangeFeed on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="cb43e-689">”Update-AzStorageBlobServiceProperty”</span><span class="sxs-lookup"><span data-stu-id="cb43e-689">'Update-AzStorageBlobServiceProperty'</span></span>

## <a name="450---august-2020"></a><span data-ttu-id="cb43e-690">4.5.0 – augusti 2020</span><span class="sxs-lookup"><span data-stu-id="cb43e-690">4.5.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cb43e-691">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb43e-691">Az.Accounts</span></span>
* <span data-ttu-id="cb43e-692">Uppdaterade ”Connect-AzAccount” så att det accepterar parametern ”MaxContextPopulation” [#9865]</span><span class="sxs-lookup"><span data-stu-id="cb43e-692">Updated 'Connect-AzAccount' to accept parameter 'MaxContextPopulation' [#9865]</span></span>
* <span data-ttu-id="cb43e-693">Uppdaterade SubscriptionClient-versionen till 2019-06-01 och visa klientdomäner [#9838]</span><span class="sxs-lookup"><span data-stu-id="cb43e-693">Updated SubscriptionClient version to 2019-06-01 and display tenant domains [#9838]</span></span>
* <span data-ttu-id="cb43e-694">Information om hemklientorganisation och managedBy-klientorganisation som stöds för prenumerationen</span><span class="sxs-lookup"><span data-stu-id="cb43e-694">Supported home tenant and managedBy tenant information of subscription</span></span>
* <span data-ttu-id="cb43e-695">Korrigerade modulnamn, versionsinformation i telemetridata</span><span class="sxs-lookup"><span data-stu-id="cb43e-695">Corrected module name, version info in telemetry data</span></span>
* <span data-ttu-id="cb43e-696">Justerade SqlDatabaseDnsSuffix och ServiceManagementUrl om miljöns slutpunkt för metadata returnerar ett inkompatibelt värde</span><span class="sxs-lookup"><span data-stu-id="cb43e-696">Adjusted SqlDatabaseDnsSuffix and ServiceManagementUrl if environment metadata endpoint returns incompatible value</span></span>

#### <a name="azaks"></a><span data-ttu-id="cb43e-697">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="cb43e-697">Az.Aks</span></span>
* <span data-ttu-id="cb43e-698">Tog bort ”ClientIdAndSecret” för ”ServicePrincipalIdAndSecret” och ställde in ”ClientIdAndSecret” som ett alias [#12381].</span><span class="sxs-lookup"><span data-stu-id="cb43e-698">Removed 'ClientIdAndSecret' to 'ServicePrincipalIdAndSecret' and set 'ClientIdAndSecret' as an alias [#12381].</span></span>
* <span data-ttu-id="cb43e-699">Tog bort ”Get-AzAks”/”New-AzAks”/”Remove-AzAks”/”Set-AzAks” för ”Get-AzAksCluster”/”New-AzAksCluster”/”Remove-AzAksCluster”/”Set-AzAksCluster” och ställde in de ursprungliga som alias [#12373].</span><span class="sxs-lookup"><span data-stu-id="cb43e-699">Removed 'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' to 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' and set the original ones as alias [#12373].</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="cb43e-700">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cb43e-700">Az.ApiManagement</span></span>
* <span data-ttu-id="cb43e-701">Lade till ny cmdlet: ”Add-AzApiManagementApiToGateway”.</span><span class="sxs-lookup"><span data-stu-id="cb43e-701">Added new 'Add-AzApiManagementApiToGateway' cmdlet.</span></span>
* <span data-ttu-id="cb43e-702">Lade till ny cmdlet: ”Get-AzApiManagementGateway”.</span><span class="sxs-lookup"><span data-stu-id="cb43e-702">Added new 'Get-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="cb43e-703">Lade till ny cmdlet: ”Get-AzApiManagementGatewayHostnameConfiguration”.</span><span class="sxs-lookup"><span data-stu-id="cb43e-703">Added new 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="cb43e-704">Lade till ny cmdlet: ”Get-AzApiManagementGatewayKey”.</span><span class="sxs-lookup"><span data-stu-id="cb43e-704">Added new 'Get-AzApiManagementGatewayKey' cmdlet.</span></span>
* <span data-ttu-id="cb43e-705">Lade till ny cmdlet: ”New-AzApiManagementGateway”.</span><span class="sxs-lookup"><span data-stu-id="cb43e-705">Added new 'New-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="cb43e-706">Lade till ny cmdlet: ”New-AzApiManagementGatewayHostnameConfiguration”.</span><span class="sxs-lookup"><span data-stu-id="cb43e-706">Added new 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="cb43e-707">Lade till ny cmdlet: ”New-AzApiManagementResourceLocationObject”.</span><span class="sxs-lookup"><span data-stu-id="cb43e-707">Added new 'New-AzApiManagementResourceLocationObject' cmdlet.</span></span>
* <span data-ttu-id="cb43e-708">Lade till ny cmdlet: ”Remove-AzApiManagementApiFromGateway”.</span><span class="sxs-lookup"><span data-stu-id="cb43e-708">Added new 'Remove-AzApiManagementApiFromGateway' cmdlet.</span></span>
* <span data-ttu-id="cb43e-709">Lade till ny cmdlet: ”Remove-AzApiManagementGateway”.</span><span class="sxs-lookup"><span data-stu-id="cb43e-709">Added new 'Remove-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="cb43e-710">Lade till ny cmdlet: ”Remove-AzApiManagementGatewayHostnameConfiguration”.</span><span class="sxs-lookup"><span data-stu-id="cb43e-710">Added new 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="cb43e-711">Lade till ny cmdlet: ”Update-AzApiManagementGateway”.</span><span class="sxs-lookup"><span data-stu-id="cb43e-711">Added new 'Update-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="cb43e-712">Lade till den nya valfria parametern [-GatewayId] till cmdleten ”Get-AzApiManagementApi”.</span><span class="sxs-lookup"><span data-stu-id="cb43e-712">Added new optional [-GatewayId] parameter to the 'Get-AzApiManagementApi' cmdlet.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="cb43e-713">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cb43e-713">Az.CognitiveServices</span></span>
* <span data-ttu-id="cb43e-714">Använde ”Neka” som standardåtgärd för NetworkRules.</span><span class="sxs-lookup"><span data-stu-id="cb43e-714">Used 'Deny' specifically as NetworkRules default action.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="cb43e-715">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="cb43e-715">Az.FrontDoor</span></span>
* <span data-ttu-id="cb43e-716">Åtgärdade ett problem där ett undantag uppstår när Enum.Parse försöker att tvinga ett null-värde till aktiverade eller inaktiverade uppräkningsvärden [#12344]</span><span class="sxs-lookup"><span data-stu-id="cb43e-716">Fixed an issue where an exception is being thrown when Enum.Parse tries to coerce a null value to an Enabled or Disabled enum values [#12344]</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="cb43e-717">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cb43e-717">Az.HDInsight</span></span>
* <span data-ttu-id="cb43e-718">Stöd för att skapa kluster med funktionen Kryptering under överföring.</span><span class="sxs-lookup"><span data-stu-id="cb43e-718">Supported creating cluster with encryption in transit feature.</span></span>
    - <span data-ttu-id="cb43e-719">Lägg till den nya parametern ”EncryptionInTransit” till cmdleten ”New-AzHDInsightCluster”</span><span class="sxs-lookup"><span data-stu-id="cb43e-719">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="cb43e-720">Lägg till den nya parametern ”EncryptionInTransit” till cmdleten ”New-AzHDInsightClusterConfig”</span><span class="sxs-lookup"><span data-stu-id="cb43e-720">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="cb43e-721">Stöd för att skapa kluster med funktionen privat länk:</span><span class="sxs-lookup"><span data-stu-id="cb43e-721">Supported creating cluster with private link feature:</span></span>
    - <span data-ttu-id="cb43e-722">Lägg till de nya parametrarna ”PublicNetworkAccessType” och ”OutboundPublicNetworkAccessType” till cmdleten ”New-AzHDInsightCluster”</span><span class="sxs-lookup"><span data-stu-id="cb43e-722">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="cb43e-723">Lägg till de nya parametrarna ”PublicNetworkAccessType” och ”OutboundPublicNetworkAccessType” till cmdleten ”New-AzHDInsightClusterConfig”</span><span class="sxs-lookup"><span data-stu-id="cb43e-723">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="cb43e-724">Returnerade information om det virtuella nätverket vid anrop till ”New-AzHDInsightCluster” eller ”Get-AzHDInsightCluster”</span><span class="sxs-lookup"><span data-stu-id="cb43e-724">Returned virtual network information when calling 'New-AzHDInsightCluster' or 'Get-AzHDInsightCluster'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb43e-725">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb43e-725">Az.Network</span></span>
* <span data-ttu-id="cb43e-726">Stöd har lagts till för parametern AddressPrefixType i ”Remove-AzExpressRouteCircuitConnectionConfig”</span><span class="sxs-lookup"><span data-stu-id="cb43e-726">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="cb43e-727">Lade till bakåtkompatibel ändringar: PeerAddressType-funktioner för privat peering i ”Remove-AzExpressRouteCircutPeeringConfig”.</span><span class="sxs-lookup"><span data-stu-id="cb43e-727">Added non-breaking changes: PeerAddressType functionality for Private Peering in 'Remove-AzExpressRouteCircutPeeringConfig'.</span></span>
* <span data-ttu-id="cb43e-728">Koden ändrades för att ignorera skiftläge för parametrarna AddressPrefixType och PeerAddressType.</span><span class="sxs-lookup"><span data-stu-id="cb43e-728">Code changed to ignore case for AddressPrefixType and PeerAddressType parameter.</span></span>
* <span data-ttu-id="cb43e-729">Ändrade varningsmeddelandet för ”New-AzLoadBalancerFrontendIpConfig”, ”New-AzPublicIpAddress” och ”New-AzPublicIpPrefix”.</span><span class="sxs-lookup"><span data-stu-id="cb43e-729">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="cb43e-730">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cb43e-730">Az.OperationalInsights</span></span>
* <span data-ttu-id="cb43e-731">Lade till alternativet ”-ForceDelete” för ”Remove-AzOperationalInsightsworkspace”</span><span class="sxs-lookup"><span data-stu-id="cb43e-731">Added '-ForceDelete' option for 'Remove-AzOperationalInsightsworkspace'</span></span>
* <span data-ttu-id="cb43e-732">Lade till ny cmdlet: ”Get-AzOperationalInsightsDeletedWorkspace”</span><span class="sxs-lookup"><span data-stu-id="cb43e-732">Added new cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'</span></span>
* <span data-ttu-id="cb43e-733">Lade till ny cmdlet: ”Restore-AzOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="cb43e-733">Added new cmdlet 'Restore-AzOperationalInsightsWorkspace'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cb43e-734">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb43e-734">Az.RecoveryServices</span></span>
* <span data-ttu-id="cb43e-735">Förbättrade sättet Azure Backup-containrar/objekt identifieras.</span><span class="sxs-lookup"><span data-stu-id="cb43e-735">Improved the Azure Backup container/item discovery experience.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb43e-736">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb43e-736">Az.Resources</span></span>
* <span data-ttu-id="cb43e-737">Lade till egenskaperna ”Condition”, ”ConditionVersion” och ”Description” till ”New-AzRoleAssignment”</span><span class="sxs-lookup"><span data-stu-id="cb43e-737">Added properties 'Condition', 'ConditionVersion' and 'Description' to 'New-AzRoleAssignment'</span></span>
    - <span data-ttu-id="cb43e-738">Detta omfattade alla relevanta ändringar av datamodellerna</span><span class="sxs-lookup"><span data-stu-id="cb43e-738">This included all the relevant changes to the data models</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb43e-739">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb43e-739">Az.Sql</span></span>
* <span data-ttu-id="cb43e-740">Korrigerade ett potentiellt fel med skiftlägesokänsliga servernamn i ”New-AzSqlServer” och ”Set-AzSqlServer”</span><span class="sxs-lookup"><span data-stu-id="cb43e-740">Fixed potential server name case insensitive error in 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="cb43e-741">Korrigerade att fel databasnamn returnerades vid ett befintligt databasfel i ”New-AzSqlDatabaseSecondary”</span><span class="sxs-lookup"><span data-stu-id="cb43e-741">Fixed wrong database name returned on existing database error in 'New-AzSqlDatabaseSecondary'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cb43e-742">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb43e-742">Az.Storage</span></span>
* <span data-ttu-id="cb43e-743">Stöd för att skapa container/blob för SAS-token med de nya behörigheterna x, t</span><span class="sxs-lookup"><span data-stu-id="cb43e-743">Supported create container/blob Sas token with new permission x,t</span></span>
    -  <span data-ttu-id="cb43e-744">”New-AzStorageBlobSASToken”</span><span class="sxs-lookup"><span data-stu-id="cb43e-744">'New-AzStorageBlobSASToken'</span></span>
    -  <span data-ttu-id="cb43e-745">”New-AzStorageContainerSASToken”</span><span class="sxs-lookup"><span data-stu-id="cb43e-745">'New-AzStorageContainerSASToken'</span></span>
* <span data-ttu-id="cb43e-746">Stöd för att skapa konto för SAS-token med de nya behörigheterna x, t, f</span><span class="sxs-lookup"><span data-stu-id="cb43e-746">Supported create account Sas token with new permission x,t,f</span></span>
    -  <span data-ttu-id="cb43e-747">”New-AzStorageAccountSASToken”</span><span class="sxs-lookup"><span data-stu-id="cb43e-747">'New-AzStorageAccountSASToken'</span></span>
* <span data-ttu-id="cb43e-748">Stöd för att hämta förbrukning av enskild filresurs</span><span class="sxs-lookup"><span data-stu-id="cb43e-748">Supported get single file share usage</span></span>
    - <span data-ttu-id="cb43e-749">”Get-AzRmStorageShare”</span><span class="sxs-lookup"><span data-stu-id="cb43e-749">'Get-AzRmStorageShare'</span></span>

## <a name="440---july-2020"></a><span data-ttu-id="cb43e-750">4.4.0 – juli 2020</span><span class="sxs-lookup"><span data-stu-id="cb43e-750">4.4.0 - July 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cb43e-751">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb43e-751">Az.Accounts</span></span>
* <span data-ttu-id="cb43e-752">En ny cmdlet, ”Invoke-AzRestMethod”, har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-752">Added new cmdlet 'Invoke-AzRestMethod'</span></span>
* <span data-ttu-id="cb43e-753">Ett problem åtgärdades som kan orsaka autentiseringsfel i scenarier med fler processer, t.ex. när flera Azure PowerShell-cmdletar körs med ”Start-Job” [#9448]</span><span class="sxs-lookup"><span data-stu-id="cb43e-753">Fixed an issue that may cause authentication errors in multi-process scenarios such as running multiple Azure PowerShell cmdlets using 'Start-Job' [#9448]</span></span>

#### <a name="azaks"></a><span data-ttu-id="cb43e-754">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="cb43e-754">Az.Aks</span></span>
* <span data-ttu-id="cb43e-755">Felet som gjorde att ”Get-AzAks” inte hämtade alla kluster har åtgärdats [#12296]</span><span class="sxs-lookup"><span data-stu-id="cb43e-755">Fixed bug 'Get-AzAks' doesn't get all clusters [#12296]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="cb43e-756">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="cb43e-756">Az.AnalysisServices</span></span>
* <span data-ttu-id="cb43e-757">Projektreferensen till autentisering har tagits bort</span><span class="sxs-lookup"><span data-stu-id="cb43e-757">Removed project reference to Authentication</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cb43e-758">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cb43e-758">Az.Automation</span></span>
* <span data-ttu-id="cb43e-759">Problemet som gjorde att strängar med escape-tecken inte kunde konverteras till JSON-objekt har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="cb43e-759">Fixed the issue that string with escape chars cannot be converted into json object.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb43e-760">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb43e-760">Az.Compute</span></span>
* <span data-ttu-id="cb43e-761">En varning har lats till som visas när ”New-AzVmss” används utan den senaste avbildningsversionen</span><span class="sxs-lookup"><span data-stu-id="cb43e-761">Added warning when using 'New-AzVmss' without 'latest' image version</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cb43e-762">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cb43e-762">Az.DataFactory</span></span>
* <span data-ttu-id="cb43e-763">Globala parametrar har lagts till för Data Factory.</span><span class="sxs-lookup"><span data-stu-id="cb43e-763">Added global parameters to Data Factory.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="cb43e-764">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="cb43e-764">Az.EventGrid</span></span>
* <span data-ttu-id="cb43e-765">Modulen har uppdaterats så att API-version 2020-06-01 används.</span><span class="sxs-lookup"><span data-stu-id="cb43e-765">Updated to use the 2020-06-01 API version.</span></span>
* <span data-ttu-id="cb43e-766">Nya funktioner har lagts till:</span><span class="sxs-lookup"><span data-stu-id="cb43e-766">Added new features:</span></span>
    - <span data-ttu-id="cb43e-767">Indatamappning</span><span class="sxs-lookup"><span data-stu-id="cb43e-767">Input mapping</span></span>
    - <span data-ttu-id="cb43e-768">Schema för händelseleverans</span><span class="sxs-lookup"><span data-stu-id="cb43e-768">Event Delivery Schema</span></span>
    - <span data-ttu-id="cb43e-769">Private Link</span><span class="sxs-lookup"><span data-stu-id="cb43e-769">Private Link</span></span>
    - <span data-ttu-id="cb43e-770">Cloud Event V10 Schema</span><span class="sxs-lookup"><span data-stu-id="cb43e-770">Cloud Event V10 Schema</span></span>
    - <span data-ttu-id="cb43e-771">Service Bus-ämne som mål</span><span class="sxs-lookup"><span data-stu-id="cb43e-771">Service Bus Topic As Destination</span></span>
    - <span data-ttu-id="cb43e-772">Azure-funktion som mål</span><span class="sxs-lookup"><span data-stu-id="cb43e-772">Azure Function As Destination</span></span>
    - <span data-ttu-id="cb43e-773">Webhook-batchbearbetning</span><span class="sxs-lookup"><span data-stu-id="cb43e-773">WebHook Batching</span></span>
    - <span data-ttu-id="cb43e-774">Säker webhook (AAD-stöd)</span><span class="sxs-lookup"><span data-stu-id="cb43e-774">Secure webhook (AAD support)</span></span>
    - <span data-ttu-id="cb43e-775">IpFiltering</span><span class="sxs-lookup"><span data-stu-id="cb43e-775">IpFiltering</span></span>
* <span data-ttu-id="cb43e-776">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="cb43e-776">Updated cmdlets:</span></span>
    - <span data-ttu-id="cb43e-777">”New-AzEventGridSubscription”/”Update-AzEventGridSubscription”:</span><span class="sxs-lookup"><span data-stu-id="cb43e-777">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span></span>
        - <span data-ttu-id="cb43e-778">Lägg till nya valfria parametrar för att ge stöd för webhook-batchbearbetning.</span><span class="sxs-lookup"><span data-stu-id="cb43e-778">Add new optional parameters to support webhook batching.</span></span>
        - <span data-ttu-id="cb43e-779">Lägg till nya valfria parametrar för att ge stöd för skyddad webhook med AAD.</span><span class="sxs-lookup"><span data-stu-id="cb43e-779">Add new optional parameters to support secured webhook using AAD.</span></span>
        - <span data-ttu-id="cb43e-780">Lägg till ny enum (uppräkning) för EndpointType-parametern för att ge stöd för Azure-funktion och Service Bus-ämne som nya mål.</span><span class="sxs-lookup"><span data-stu-id="cb43e-780">Add new enum for EndpointType parameter to support azure function and service bus topic as new destinations.</span></span>
        - <span data-ttu-id="cb43e-781">Lägg till ny valfri parameter för leveransschema.</span><span class="sxs-lookup"><span data-stu-id="cb43e-781">Add new optional parameter for delivery schema.</span></span>
    - <span data-ttu-id="cb43e-782">”New-AzEventGridTopic”/”Update-AzEventGridTopic” och ”New-AzEventGridDomain”/”Update-AzEventGridDomain”:</span><span class="sxs-lookup"><span data-stu-id="cb43e-782">'New-AzEventGridTopic'/'Update-AzEventGridTopic' and 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span></span>
        - <span data-ttu-id="cb43e-783">Lägg till nya valfria parametrar för att ge stöd för IpFiltering.</span><span class="sxs-lookup"><span data-stu-id="cb43e-783">Add new optional parameters to support IpFiltering.</span></span>
    - <span data-ttu-id="cb43e-784">”New-AzEventGridTopic”/”New-AzEventGridDomain”:</span><span class="sxs-lookup"><span data-stu-id="cb43e-784">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span></span>
        - <span data-ttu-id="cb43e-785">Lägg till nya valfria parametrar för att ge stöd för indatamappning.</span><span class="sxs-lookup"><span data-stu-id="cb43e-785">Add new optional parameters to support Input mapping.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="cb43e-786">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="cb43e-786">Az.FrontDoor</span></span>
* <span data-ttu-id="cb43e-787">Modulen har uppdaterats så att API 2020-05-01 används</span><span class="sxs-lookup"><span data-stu-id="cb43e-787">Updated module to use API 2020-05-01</span></span>
* <span data-ttu-id="cb43e-788">Stöd för privat länk har lagts till för Storage-, KeyVault- och Web App Service-resurser</span><span class="sxs-lookup"><span data-stu-id="cb43e-788">Added Private link support for Storage, Keyvault and Web App Service resources</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="cb43e-789">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cb43e-789">Az.HDInsight</span></span>
* <span data-ttu-id="cb43e-790">Stöd för att skapa kluster med ADLSGen1/2-lagring i nationella moln.</span><span class="sxs-lookup"><span data-stu-id="cb43e-790">Supported creating cluster with ADLSGen1/2 storage in national clouds.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cb43e-791">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cb43e-791">Az.Monitor</span></span>
* <span data-ttu-id="cb43e-792">Bugg som orsakade fel med ”Get-AzDiagnosticSetting” när mått eller loggar var null har åtgärdats [#12272]</span><span class="sxs-lookup"><span data-stu-id="cb43e-792">Fixed bug for 'Get-AzDiagnosticSetting' when metrics or logs are null [#12272]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb43e-793">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb43e-793">Az.Network</span></span>
* <span data-ttu-id="cb43e-794">Parameterväxlingen i VWan HubVnet-anslutningar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="cb43e-794">Fixed parameters swap in VWan HubVnet connection</span></span>
* <span data-ttu-id="cb43e-795">Nya cmdletar har lagts till för platser för virtuella installationer i Azure-nätverk</span><span class="sxs-lookup"><span data-stu-id="cb43e-795">Added new cmdlets for Azure Network Virtual Appliance Sites</span></span>
    - <span data-ttu-id="cb43e-796">”Get-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="cb43e-796">'Get-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="cb43e-797">”New-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="cb43e-797">'New-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="cb43e-798">”Remove-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="cb43e-798">'Remove-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="cb43e-799">”Update-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="cb43e-799">'Update-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="cb43e-800">”New-AzOffice365PolicyProperty”</span><span class="sxs-lookup"><span data-stu-id="cb43e-800">'New-AzOffice365PolicyProperty'</span></span>
* <span data-ttu-id="cb43e-801">Nya cmdletar har lagts till för virtuella installationer i Azure-nätverk</span><span class="sxs-lookup"><span data-stu-id="cb43e-801">Added new cmdlets for Azure Network Virtual Appliance</span></span>
    - <span data-ttu-id="cb43e-802">”Get-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="cb43e-802">'Get-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="cb43e-803">”New-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="cb43e-803">'New-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="cb43e-804">”Remove-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="cb43e-804">'Remove-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="cb43e-805">”Update-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="cb43e-805">'Update-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="cb43e-806">”Get-AzNetworkVirtualApplianceSku”</span><span class="sxs-lookup"><span data-stu-id="cb43e-806">'Get-AzNetworkVirtualApplianceSku'</span></span>
    - <span data-ttu-id="cb43e-807">”New-AzVirtualApplianceSkuProperty”</span><span class="sxs-lookup"><span data-stu-id="cb43e-807">'New-AzVirtualApplianceSkuProperty'</span></span>
* <span data-ttu-id="cb43e-808">Application Gateway har introducerats i vanliga cmdletar för Private Link</span><span class="sxs-lookup"><span data-stu-id="cb43e-808">Onboarded Application Gateway to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="cb43e-809">StorageSync har introducerats i vanliga cmdletar för Private Link</span><span class="sxs-lookup"><span data-stu-id="cb43e-809">Onboarded StorageSync to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="cb43e-810">SignalR har introducerats i vanliga cmdletar för Private Link</span><span class="sxs-lookup"><span data-stu-id="cb43e-810">Onboarded SignalR to Private Link Common Cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cb43e-811">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb43e-811">Az.RecoveryServices</span></span>
* <span data-ttu-id="cb43e-812">Projektreferensen till autentisering har tagits bort</span><span class="sxs-lookup"><span data-stu-id="cb43e-812">Removed project reference to Authentication</span></span>
* <span data-ttu-id="cb43e-813">Azure Backup-anpassade cmdletar gör text mer korrekt.</span><span class="sxs-lookup"><span data-stu-id="cb43e-813">Azure Backup tuned cmdlets help text to be more accurate.</span></span>
* <span data-ttu-id="cb43e-814">Stöd har lagts till som gör att Azure Backup kan hämta MAB-agentjobb med cmdleten ”Get-AzRecoveryServicesBackupJob”.</span><span class="sxs-lookup"><span data-stu-id="cb43e-814">Azure Backup added support for fetching MAB agent jobs using 'Get-AzRecoveryServicesBackupJob' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb43e-815">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb43e-815">Az.Resources</span></span>
* <span data-ttu-id="cb43e-816">”Save-AzResourceGroupDeploymentTemplate” har uppdaterats för att använda SDK:n.</span><span class="sxs-lookup"><span data-stu-id="cb43e-816">Updated 'Save-AzResourceGroupDeploymentTemplate' to use the SDK.</span></span>
* <span data-ttu-id="cb43e-817">Cmdleten ”Unregister-AzResourceProvider” har lagts till.</span><span class="sxs-lookup"><span data-stu-id="cb43e-817">Added 'Unregister-AzResourceProvider' cmdlet.</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb43e-818">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb43e-818">Az.Sql</span></span>
* <span data-ttu-id="cb43e-819">Stöd har lagts till för SPN och gästanvändare i cmdleten ”Set-AzSqlInstanceActiveDirectoryAdministrator”</span><span class="sxs-lookup"><span data-stu-id="cb43e-819">Added support for Service principal and guest users in Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet'</span></span>
* <span data-ttu-id="cb43e-820">En bugg har åtgärdats i cmdletar för dataklassificering.</span><span class="sxs-lookup"><span data-stu-id="cb43e-820">Fixed a bug in Data Classification cmdlets.'</span></span>
* <span data-ttu-id="cb43e-821">Stöd har lagts till för redundansväxling med Azure SQL Managed Instance: ”Invoke-AzSqlInstanceFailover”</span><span class="sxs-lookup"><span data-stu-id="cb43e-821">Added support for Azure SQL Managed Instance failover: 'Invoke-AzSqlInstanceFailover'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cb43e-822">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb43e-822">Az.Storage</span></span>
* <span data-ttu-id="cb43e-823">Problemet som gjorde att UserAgent inte lades till för vissa cmdletar för dataplanet har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="cb43e-823">Fixed the issue that UserAgent is not added for some data plane cmdlets.</span></span>
* <span data-ttu-id="cb43e-824">Stöd har lagts till för att skapa/uppdatera Storage-konto med MinimumTlsVersion och AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="cb43e-824">Supported create/update Storage account with MinimumTlsVersion and AllowBlobPublicAccess</span></span>
    -  <span data-ttu-id="cb43e-825">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="cb43e-825">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="cb43e-826">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="cb43e-826">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="cb43e-827">Stöd har lagts till för att aktivera/inaktivera versionshantering i Blob Service för ett Storage-konto</span><span class="sxs-lookup"><span data-stu-id="cb43e-827">Support enable/disable versioning on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="cb43e-828">”Update-AzStorageBlobServiceProperty”</span><span class="sxs-lookup"><span data-stu-id="cb43e-828">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="cb43e-829">Stöd har lagts till för att visa blobar med blobversioner</span><span class="sxs-lookup"><span data-stu-id="cb43e-829">Support list blobs with blob versions</span></span>
    - <span data-ttu-id="cb43e-830">”Get-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="cb43e-830">'Get-AzStorageBlob'</span></span>
* <span data-ttu-id="cb43e-831">Stöd har lagts till för att hämta/ta bort enskilda ögonblicksbilder av blobar eller blobversioner</span><span class="sxs-lookup"><span data-stu-id="cb43e-831">Support get/remove single blob snapshot or blob version</span></span>
    - <span data-ttu-id="cb43e-832">”Get-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="cb43e-832">'Get-AzStorageBlob'</span></span>
    - <span data-ttu-id="cb43e-833">”Remove-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="cb43e-833">'Remove-AzStorageBlob'</span></span>
* <span data-ttu-id="cb43e-834">Stöd har lagts till för pipelines från blobobjekt genererade av Azure.Storage.Blobs V12</span><span class="sxs-lookup"><span data-stu-id="cb43e-834">Support pipeline from blob object generated from Azure.Storage.Blobs V12</span></span>
    - <span data-ttu-id="cb43e-835">”Get-AzStorageBlobContent”</span><span class="sxs-lookup"><span data-stu-id="cb43e-835">'Get-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="cb43e-836">”New-AzStorageBlobSASToken”</span><span class="sxs-lookup"><span data-stu-id="cb43e-836">'New-AzStorageBlobSASToken'</span></span>
    - <span data-ttu-id="cb43e-837">”Remove-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="cb43e-837">'Remove-AzStorageBlob'</span></span>
    - <span data-ttu-id="cb43e-838">”Set-AzStorageBlobContent”</span><span class="sxs-lookup"><span data-stu-id="cb43e-838">'Set-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="cb43e-839">”Start-AzStorageBlobCopy”</span><span class="sxs-lookup"><span data-stu-id="cb43e-839">'Start-AzStorageBlobCopy'</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="cb43e-840">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="cb43e-840">Az.StorageSync</span></span>
* <span data-ttu-id="cb43e-841">En ny version har lagts till för StorageSync SDK som körs mot ApiVersion 2020-03-01</span><span class="sxs-lookup"><span data-stu-id="cb43e-841">Added a new version StorageSync SDK targeting ApiVersion 2020-03-01</span></span>
* <span data-ttu-id="cb43e-842">En cmdlet för synkroniseringstjänsten för lagringsuppdatering har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-842">Added Update Storage Sync Service cmdlet</span></span>
    - <span data-ttu-id="cb43e-843">”Set-AzStorageSyncService”</span><span class="sxs-lookup"><span data-stu-id="cb43e-843">'Set-AzStorageSyncService'</span></span>
* <span data-ttu-id="cb43e-844">IncomingTrafficPolicy och PrivateEndpointConnections har lagts till för StorageSyncService-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="cb43e-844">Added IncomingTrafficPolicy and PrivateEndpointConnections to StorageSyncService cmdlets.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cb43e-845">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb43e-845">Az.Websites</span></span>
* <span data-ttu-id="cb43e-846">Stöd har lagts till för att utföra åtgärder för platser som inte tillhör samma resursgrupp som App Services-planen</span><span class="sxs-lookup"><span data-stu-id="cb43e-846">Added support to perform operations for Slots not in the same resource group as the App Service Plan</span></span>

## <a name="430---june-2020"></a><span data-ttu-id="cb43e-847">4.3.0 – juni 2020</span><span class="sxs-lookup"><span data-stu-id="cb43e-847">4.3.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cb43e-848">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb43e-848">Az.Accounts</span></span>
* <span data-ttu-id="cb43e-849">Stöd för identifiering av miljöinställning som standard och tillägg av miljön via ”Add-AzEnvironment”</span><span class="sxs-lookup"><span data-stu-id="cb43e-849">Supported discovering environment setting by default and adding environment via 'Add-AzEnvironment'</span></span>
* <span data-ttu-id="cb43e-850">Uppdatera förinlästa sammansättningar [#12024], [#11976]</span><span class="sxs-lookup"><span data-stu-id="cb43e-850">Update preloaded assemblies [#12024], [#11976]</span></span>
* <span data-ttu-id="cb43e-851">Uppdaterad Azure.Core-sammansättning</span><span class="sxs-lookup"><span data-stu-id="cb43e-851">Updated Azure.Core assembly</span></span>
* <span data-ttu-id="cb43e-852">Ett problem har åtgärdats som kan orsaka att ”Connect-AzAccount” misslyckas vid körning av flera trådar [#11201]</span><span class="sxs-lookup"><span data-stu-id="cb43e-852">Fixed an issue that may cause 'Connect-AzAccount' to fail in multi-threaded execution [#11201]</span></span>

#### <a name="azaks"></a><span data-ttu-id="cb43e-853">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="cb43e-853">Az.Aks</span></span>
* <span data-ttu-id="cb43e-854">Användning av gamla [AccessProfile API](/rest/api/aks/managedclusters/getaccessprofile) ersattes med anrop till API:erna [ListClusterAdmin](/rest/api/aks/managedclusters/listclusteradmincredentials) och [ListClusterUser](/rest/api/aks/managedclusters/listclusterusercredentials)</span><span class="sxs-lookup"><span data-stu-id="cb43e-854">Replaced usage of old [AccessProfile API](/rest/api/aks/managedclusters/getaccessprofile) with calls to [ListClusterAdmin](/rest/api/aks/managedclusters/listclusteradmincredentials) and [ListClusterUser](/rest/api/aks/managedclusters/listclusterusercredentials) APIs</span></span>

#### <a name="azbatch"></a><span data-ttu-id="cb43e-855">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="cb43e-855">Az.Batch</span></span>
* <span data-ttu-id="cb43e-856">Az.Batch har uppdaterats att använda ”Microsoft.Azure.Management.Batch” SDK till och med version 11.0.0.</span><span class="sxs-lookup"><span data-stu-id="cb43e-856">Updated Az.Batch to use 'Microsoft.Azure.Management.Batch' SDK version to 11.0.0</span></span>
* <span data-ttu-id="cb43e-857">Möjligheten att ange BatchAccount-identiteten har lagts till i cmdleten ”New-AzBatchAccount”</span><span class="sxs-lookup"><span data-stu-id="cb43e-857">Added the ability to set the BatchAccount Identity in the 'New-AzBatchAccount' cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="cb43e-858">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cb43e-858">Az.CognitiveServices</span></span>
* <span data-ttu-id="cb43e-859">Stöd för att visa kontofunktioner.</span><span class="sxs-lookup"><span data-stu-id="cb43e-859">Supported displaying account capabilities.</span></span>
* <span data-ttu-id="cb43e-860">Stöd för att ändra PublicNetworkAccess.</span><span class="sxs-lookup"><span data-stu-id="cb43e-860">Supported modifying PublicNetworkAccess.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb43e-861">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb43e-861">Az.Compute</span></span>
* <span data-ttu-id="cb43e-862">Parametern SimulateEviction har lagts till i cmdletarna set-AzVM och set-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="cb43e-862">Added SimulateEviction parameter to Set-AzVM and Set-AzVmssVM cmdlets.</span></span>
* <span data-ttu-id="cb43e-863">”Premium_LRS” har lagts till i argumentslutföraren för parametern StorageAccountType för cmdleten New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="cb43e-863">Added 'Premium_LRS' to the argument completer of StorageAccountType parameter for New-AzGalleryImageVersion cmdlet.</span></span>
* <span data-ttu-id="cb43e-864">Understatusar har lagts till i VMCustomScriptExtension [#11297]</span><span class="sxs-lookup"><span data-stu-id="cb43e-864">Added Substatuses to VMCustomScriptExtension [#11297]</span></span>
* <span data-ttu-id="cb43e-865">”Delete” har lagts till i argumentslutföraren för parametern EvictionPolicy för cmdletarna New-AzVM och New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="cb43e-865">Added 'Delete' to the argument completer of EvictionPolicy parameter for New-AzVM and New-AzVMConfig cmdlets.</span></span>
* <span data-ttu-id="cb43e-866">Åtgärdat namn för nytt VM-tillägg för SAP</span><span class="sxs-lookup"><span data-stu-id="cb43e-866">Fixed name of new VM Extension for SAP</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cb43e-867">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cb43e-867">Az.DataFactory</span></span>
* <span data-ttu-id="cb43e-868">ADF .Net SDK har uppdaterats till 4.9.0</span><span class="sxs-lookup"><span data-stu-id="cb43e-868">Updated ADF .Net SDK version to 4.9.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="cb43e-869">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="cb43e-869">Az.EventHub</span></span>
* <span data-ttu-id="cb43e-870">Parametrar för hanterad identitet har lagts till i cmdletarna ”New-AzEventHubNamespace” och ”set-AzEventHubNamespace”</span><span class="sxs-lookup"><span data-stu-id="cb43e-870">Added Managed Identity parameters to 'New-AzEventHubNamespace' and 'Set-AzEventHubNamespace' cmdlets</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="cb43e-871">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="cb43e-871">Az.Functions</span></span>
* <span data-ttu-id="cb43e-872">Stöd har lagts till för att skapa PowerShell 7.0- och Java 11-funktionsappar</span><span class="sxs-lookup"><span data-stu-id="cb43e-872">Added support to create PowerShell 7.0 and Java 11 function apps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="cb43e-873">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cb43e-873">Az.HDInsight</span></span>
* <span data-ttu-id="cb43e-874">Stöd för listning av värdar och omstart för specifika värdar i HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="cb43e-874">Supported listing hosts and restart specific hosts of the HDInsight cluster.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="cb43e-875">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="cb43e-875">Az.HealthcareApis</span></span>
* <span data-ttu-id="cb43e-876">Uppdaterade SDK-versionen till 1.1.0</span><span class="sxs-lookup"><span data-stu-id="cb43e-876">Updated the SDK version to 1.1.0</span></span>
* <span data-ttu-id="cb43e-877">Stöd har lagts till för exportinställningar och hanterad identitet</span><span class="sxs-lookup"><span data-stu-id="cb43e-877">Added support for Export settings and Managed Identity</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cb43e-878">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cb43e-878">Az.Monitor</span></span>
* <span data-ttu-id="cb43e-879">Parameter för inmatningsobjekt har åtgärdats för ”Set-AzActivityLogAlert”</span><span class="sxs-lookup"><span data-stu-id="cb43e-879">Fixed input object parameter for 'Set-AzActivityLogAlert'</span></span>
* <span data-ttu-id="cb43e-880">Parametern ”InputObject” har åtgärdats för ”Set-AzActionGroup” [#10868]</span><span class="sxs-lookup"><span data-stu-id="cb43e-880">Fixed 'InputObject' parameter for 'Set-AzActionGroup' [#10868]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb43e-881">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb43e-881">Az.Network</span></span>
* <span data-ttu-id="cb43e-882">Stöd har lagts till för parametern AddressPrefixType i ”Remove-AzExpressRouteCircuitConnectionConfig”</span><span class="sxs-lookup"><span data-stu-id="cb43e-882">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="cb43e-883">Nya cmdletar har lagts till för Azure FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="cb43e-883">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="cb43e-884">”New-AzFirewallPolicyDnsSetting”</span><span class="sxs-lookup"><span data-stu-id="cb43e-884">'New-AzFirewallPolicyDnsSetting'</span></span>
    - <span data-ttu-id="cb43e-885">Stöd för mål-FQDN i nätverksregler för brandväggsprincip</span><span class="sxs-lookup"><span data-stu-id="cb43e-885">Support for Destination FQDN in Network Rules for Firewall Policy</span></span>
* <span data-ttu-id="cb43e-886">Stöd har lagts till för åtgärder i serverdelsadresspooler</span><span class="sxs-lookup"><span data-stu-id="cb43e-886">Added support for backend address pool operations</span></span>
    - <span data-ttu-id="cb43e-887">”New-AzLoadBalancerBackendAddressConfig”</span><span class="sxs-lookup"><span data-stu-id="cb43e-887">'New-AzLoadBalancerBackendAddressConfig'</span></span>
    - <span data-ttu-id="cb43e-888">”New-AzLoadBalancerBackendAddressPool”</span><span class="sxs-lookup"><span data-stu-id="cb43e-888">'New-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="cb43e-889">”Set-AzLoadBalancerBackendAddressPool”</span><span class="sxs-lookup"><span data-stu-id="cb43e-889">'Set-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="cb43e-890">”Remove-AzLoadBalancerBackendAddressPool”</span><span class="sxs-lookup"><span data-stu-id="cb43e-890">'Remove-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="cb43e-891">”Get-AzLoadBalancerBackendAddressPool”</span><span class="sxs-lookup"><span data-stu-id="cb43e-891">'Get-AzLoadBalancerBackendAddressPool'</span></span>
* <span data-ttu-id="cb43e-892">Namnvalidering har lagts till för ”New-AzIpGroup”</span><span class="sxs-lookup"><span data-stu-id="cb43e-892">Added name validation for 'New-AzIpGroup'</span></span>
* <span data-ttu-id="cb43e-893">Nya cmdletar har lagts till för Azure FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="cb43e-893">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="cb43e-894">”New-AzFirewallPolicyThreatIntelWhitelist”</span><span class="sxs-lookup"><span data-stu-id="cb43e-894">'New-AzFirewallPolicyThreatIntelWhitelist'</span></span>
* <span data-ttu-id="cb43e-895">Nedanstående kommandon för funktionen har uppdaterats: Konfiguration/borttagning av anpassade DNS-servrar på VirtualWan P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="cb43e-895">Updated below commands for feature: Custom dns servers set/remove on VirtualWan P2SVpnGateway.</span></span>
    - <span data-ttu-id="cb43e-896">New-AzP2sVpnGateway har uppdaterats: Den valfria parametern ”-CustomDnsServer” har lagts till för att kunder ska kunna ange att deras DNS-servrar ska konfigureras på P2SVpnGateway, som kan användas av punkt-till-plats-klienter.</span><span class="sxs-lookup"><span data-stu-id="cb43e-896">Updated New-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
    - <span data-ttu-id="cb43e-897">Update-AzP2sVpnGateway har uppdaterats: Den valfria parametern ”-CustomDnsServer” har lagts till för att kunder ska kunna ange att deras DNS-servrar ska konfigureras på P2SVpnGateway, som kan användas av punkt-till-plats-klienter.</span><span class="sxs-lookup"><span data-stu-id="cb43e-897">Updated Update-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
* <span data-ttu-id="cb43e-898">”Update-AzVpnGateway” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="cb43e-898">Updated 'Update-AzVpnGateway'</span></span>
    - <span data-ttu-id="cb43e-899">Den valfria parametern ”-BgpPeeringAddress” har lagts till för att kunder ska kunna ange sina anpassade BGP:er som ska konfigurerar på VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="cb43e-899">Added optional parameter '-BgpPeeringAddress' for customers to specify their custom bgps to set on VpnGateway.</span></span>
* <span data-ttu-id="cb43e-900">Ny cmdlet har lagts till för att stödja återställning av en VirtualHub-resurs routningsstatus:</span><span class="sxs-lookup"><span data-stu-id="cb43e-900">Added new cmdlet to support resetting the routing state of a VirtualHub resource:</span></span>
    - <span data-ttu-id="cb43e-901">”Reset-AzHubRouter”</span><span class="sxs-lookup"><span data-stu-id="cb43e-901">'Reset-AzHubRouter'</span></span>
* <span data-ttu-id="cb43e-902">Nedanstående saker har uppdaterats baserat på den senaste Swagger-ändringen för brandväggspolicyn</span><span class="sxs-lookup"><span data-stu-id="cb43e-902">Updated below things based on recent swagger change for Firewall Policy</span></span>
    - <span data-ttu-id="cb43e-903">Namn ändras för RuleGroup, RuleCollectionGroup och RuleType</span><span class="sxs-lookup"><span data-stu-id="cb43e-903">Changes names for RuleGroup, RuleCollectionGroup and RuleType</span></span>
    - <span data-ttu-id="cb43e-904">Stöd har lagts till för NAT-regelsamlingar för brandväggsprincip så att flera NAT-regelsamlingar stöds</span><span class="sxs-lookup"><span data-stu-id="cb43e-904">Added support for Firewall Policy NAT Rule Collections to support multiple NAT Rule Collection</span></span>
* <span data-ttu-id="cb43e-905">[Icke-bakåtkompatibel ändring] Den obligatoriska parametern ”SourceIpGroup” har lagts till för ”New-AzFirewallPolicyApplicationRule” och ”New-AzFirewallPolicyNetworkRule”.</span><span class="sxs-lookup"><span data-stu-id="cb43e-905">[Breaking Change] Added mandatory parameter 'SourceIpGroup' for 'New-AzFirewallPolicyApplicationRule' and 'New-AzFirewallPolicyNetworkRule'.</span></span>
* <span data-ttu-id="cb43e-906">[Icke-bakåtkompatibel ändring] ”New-AzFirewallPolicyApplicationRule” har åtgärdats, parametern ”SourceAddress” är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="cb43e-906">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="cb43e-907">[Icke-bakåtkompatibel ändring] ”New-AzFirewallPolicyApplicationRule” har åtgärdats, parametern ”SourceAddress” är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="cb43e-907">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="cb43e-908">[Icke-bakåtkompatibel ändring] Obligatoriska parametrar har tagits bort: ”TranslatedAddress”, ”TranslatedPort” för ”New-AzFirewallPolicyNatRuleCollection”.</span><span class="sxs-lookup"><span data-stu-id="cb43e-908">[Breaking Change] Removed mandatory parameters: 'TranslatedAddress', 'TranslatedPort' for 'New-AzFirewallPolicyNatRuleCollection'.</span></span>
* <span data-ttu-id="cb43e-909">Nya cmdletar har lagts till för att stödja PrivateLink på Application Gateway</span><span class="sxs-lookup"><span data-stu-id="cb43e-909">Added new cmdlets to support PrivateLink On Application Gateway</span></span>
    - <span data-ttu-id="cb43e-910">”New-AzApplicationGatewayPrivateLinkConfiguration”</span><span class="sxs-lookup"><span data-stu-id="cb43e-910">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="cb43e-911">”Get-AzApplicationGatewayPrivateLinkConfiguration”</span><span class="sxs-lookup"><span data-stu-id="cb43e-911">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="cb43e-912">”New-AzApplicationGatewayPrivateLinkConfiguration”</span><span class="sxs-lookup"><span data-stu-id="cb43e-912">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="cb43e-913">”Set-AzApplicationGatewayPrivateLinkConfiguration”</span><span class="sxs-lookup"><span data-stu-id="cb43e-913">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="cb43e-914">”Remove-AzApplicationGatewayPrivateLinkConfiguration”</span><span class="sxs-lookup"><span data-stu-id="cb43e-914">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="cb43e-915">”New-AzApplicationGatewayPrivateLinkIpConfiguration”</span><span class="sxs-lookup"><span data-stu-id="cb43e-915">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span></span>
* <span data-ttu-id="cb43e-916">Nya cmdletar har lagts till för VirtualHubs underordnade resurs HubRouteTables.</span><span class="sxs-lookup"><span data-stu-id="cb43e-916">Added new cmdlets for HubRouteTables child resource of VirtualHub.</span></span>
    - <span data-ttu-id="cb43e-917">”New-AzVHubRoute”</span><span class="sxs-lookup"><span data-stu-id="cb43e-917">'New-AzVHubRoute'</span></span>
    - <span data-ttu-id="cb43e-918">”New-AzVHubRouteTable”</span><span class="sxs-lookup"><span data-stu-id="cb43e-918">'New-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="cb43e-919">”Get-AzVHubRouteTable”</span><span class="sxs-lookup"><span data-stu-id="cb43e-919">'Get-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="cb43e-920">”Update-AzVHubRouteTable”</span><span class="sxs-lookup"><span data-stu-id="cb43e-920">'Update-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="cb43e-921">”Remove-AzVHubRouteTable”</span><span class="sxs-lookup"><span data-stu-id="cb43e-921">'Remove-AzVHubRouteTable'</span></span>
* <span data-ttu-id="cb43e-922">Befintliga cmdletar har uppdaterats för att stödja valfri RoutingConfiguration-indataparameter för anpassad routning i VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="cb43e-922">Updated existing cmdlets to support optional RoutingConfiguration input parameter for custom routing in VirtualWan.</span></span>
    - <span data-ttu-id="cb43e-923">”New-AzExpressRouteConnection”</span><span class="sxs-lookup"><span data-stu-id="cb43e-923">'New-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="cb43e-924">”Set-AzExpressRouteConnection”</span><span class="sxs-lookup"><span data-stu-id="cb43e-924">'Set-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="cb43e-925">”New-AzVirtualHubVnetConnection”</span><span class="sxs-lookup"><span data-stu-id="cb43e-925">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="cb43e-926">”Update-AzVirtualHubVnetConnection”</span><span class="sxs-lookup"><span data-stu-id="cb43e-926">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="cb43e-927">”New-AzVpnConnection”</span><span class="sxs-lookup"><span data-stu-id="cb43e-927">'New-AzVpnConnection'</span></span>
    - <span data-ttu-id="cb43e-928">”Update-AzVpnConnection”</span><span class="sxs-lookup"><span data-stu-id="cb43e-928">'Update-AzVpnConnection'</span></span>
    - <span data-ttu-id="cb43e-929">”New-AzP2sVpnGateway”</span><span class="sxs-lookup"><span data-stu-id="cb43e-929">'New-AzP2sVpnGateway'</span></span>
    - <span data-ttu-id="cb43e-930">”Update-AzP2sVpnGateway”</span><span class="sxs-lookup"><span data-stu-id="cb43e-930">'Update-AzP2sVpnGateway'</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="cb43e-931">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cb43e-931">Az.OperationalInsights</span></span>
* <span data-ttu-id="cb43e-932">Fast fel PSWorkspace implementerar inte IOperationalInsightsWorkspace [#12135]</span><span class="sxs-lookup"><span data-stu-id="cb43e-932">Fixed bug PSWorkspace doesn't implement IOperationalInsightsWorkspace [#12135]</span></span>
* <span data-ttu-id="cb43e-933">”pergb2018” har lagts till i uppsättningen med giltiga värden för parametern ”Sku” i ”Set-AzOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="cb43e-933">Added 'pergb2018' to valid value set of parameter 'Sku' in 'Set-AzOperationalInsightsWorkspace'</span></span> 
* <span data-ttu-id="cb43e-934">Alias ”FunctionParameters” lades till för parametern ”FunctionParameter” till</span><span class="sxs-lookup"><span data-stu-id="cb43e-934">Added alias 'FunctionParameters' for parameter 'FunctionParameter' to</span></span>
    - <span data-ttu-id="cb43e-935">”New-AzOperationalInsightsSavedSearch”</span><span class="sxs-lookup"><span data-stu-id="cb43e-935">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="cb43e-936">”Set-AzOperationalInsightsSavedSearch”</span><span class="sxs-lookup"><span data-stu-id="cb43e-936">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cb43e-937">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb43e-937">Az.RecoveryServices</span></span>
* <span data-ttu-id="cb43e-938">Azure Backup har fått stöd för att hämta MAB-objekt.</span><span class="sxs-lookup"><span data-stu-id="cb43e-938">Azure Backup added support for fetching MAB items.</span></span>
* <span data-ttu-id="cb43e-939">Azure Site Recovery stöder disktypen ”StandardSSD_LRS”</span><span class="sxs-lookup"><span data-stu-id="cb43e-939">Azure Site Recovery supports disk type 'StandardSSD_LRS'</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb43e-940">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb43e-940">Az.Resources</span></span>
* <span data-ttu-id="cb43e-941">”UsageLocation”, ”GivenName”, ”Surname”, ”AccountEnabled”, ”MailNickname”, ”Mail” på ”PSADUser” lades till [#10526] [#10497]</span><span class="sxs-lookup"><span data-stu-id="cb43e-941">Added 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' on 'PSADUser' [#10526] [#10497]</span></span>
* <span data-ttu-id="cb43e-942">Problem med att ”-Mail” inte fungerar på ”Get-AzADUser” har åtgärdats [#11981]</span><span class="sxs-lookup"><span data-stu-id="cb43e-942">Fixed issue that '-Mail' doesn't work on 'Get-AzADUser' [#11981]</span></span>
* <span data-ttu-id="cb43e-943">Parametern ”-ExcludeChangeType” har lagts till i ”Get-AzDeploymentWhatIfResult” och ”Get-AzResourceGroupDeploymentWhatIfResult”</span><span class="sxs-lookup"><span data-stu-id="cb43e-943">Added '-ExcludeChangeType' parameter to 'Get-AzDeploymentWhatIfResult' and 'Get-AzResourceGroupDeploymentWhatIfResult'</span></span>
* <span data-ttu-id="cb43e-944">Parametern ”-WhatIfExcludeChangeType” har lagts till i ”New-AzDeployment” och ”New-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="cb43e-944">Added '-WhatIfExcludeChangeType' parameter to 'New-AzDeployment' and 'New-AzResourceGroupDeployment'</span></span>
* <span data-ttu-id="cb43e-945">Cmdletar för ”Test-Az\*Deployment” har uppdaterats för att visa bättre felmeddelanden</span><span class="sxs-lookup"><span data-stu-id="cb43e-945">Updated 'Test-Az\*Deployment' cmdlets to show better error messages</span></span>
* <span data-ttu-id="cb43e-946">Hjälpmeddelandet för parametern ”-Name” i distributionsskapande och What If-cmdletar</span><span class="sxs-lookup"><span data-stu-id="cb43e-946">Fixed help message for '-Name' parameter of deployment create and What-If cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb43e-947">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb43e-947">Az.Sql</span></span>
* <span data-ttu-id="cb43e-948">Stöd för tjänsthuvudnamn har lagts till för administratörs-cmdlet för SQL Server Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="cb43e-948">Added support for service principal for Set SQL Server Azure Active Directory Admin cmdlet</span></span>
* <span data-ttu-id="cb43e-949">Synkroniseringsproblem i Data Classification-cmdletar har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="cb43e-949">Fixed sync issue in Data Classification cmdlets.</span></span>
* <span data-ttu-id="cb43e-950">Stöd för att söka efter användare via e-postadress på ”Set-AzSqlServerActiveDirectoryAdministrator” [#12192]</span><span class="sxs-lookup"><span data-stu-id="cb43e-950">Supported searching user by mail on 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cb43e-951">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb43e-951">Az.Storage</span></span>
* <span data-ttu-id="cb43e-952">Skapa lagringskonto med RequireInfrastructureEncryption stöds</span><span class="sxs-lookup"><span data-stu-id="cb43e-952">Supported create Storage account with RequireInfrastructureEncryption</span></span>
    -  <span data-ttu-id="cb43e-953">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="cb43e-953">'New-AzStorageAccount'</span></span>
* <span data-ttu-id="cb43e-954">Logiken för inläsning av Azure.Core flyttades till Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb43e-954">Moved the logic of loading Azure.Core to Az.Accounts</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cb43e-955">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb43e-955">Az.Websites</span></span>
* <span data-ttu-id="cb43e-956">Skydd för att ta bort skapad webapp om återställningen misslyckades har lagts till i ”Restore-AzDeletedWebApp”</span><span class="sxs-lookup"><span data-stu-id="cb43e-956">Added safeguard to delete created webapp if restore failed in 'Restore-AzDeletedWebApp'</span></span>
* <span data-ttu-id="cb43e-957">”SourceWebApp.Location” har lagts till för ”New-AzWebApp” och ”New-AzWebAppSlot”</span><span class="sxs-lookup"><span data-stu-id="cb43e-957">Added 'SourceWebApp.Location' for 'New-AzWebApp' and 'New-AzWebAppSlot'</span></span>
* <span data-ttu-id="cb43e-958">Fel som förhindrade ändring av containerinställningar i ”Set-AzWebApp” och ”Set-AzWebAppSlot” har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="cb43e-958">Fixed bug that prevented changing Container settings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>
* <span data-ttu-id="cb43e-959">Ett fel för att hämta SiteConfig när -Name inte anges för Get-AzWebApp har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="cb43e-959">Fixed bug to get SiteConfig when -Name is not given for Get-AzWebApp</span></span>
* <span data-ttu-id="cb43e-960">Stöd har lagts till för att skapa ASP för Linux-appar</span><span class="sxs-lookup"><span data-stu-id="cb43e-960">Added a support to create ASP for Linux Apps</span></span>
* <span data-ttu-id="cb43e-961">Undantag har lagts till för kloning över resursgrupper</span><span class="sxs-lookup"><span data-stu-id="cb43e-961">Added exceptions for clone across resource groups</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="cb43e-962">4.2.0 – juni 2020</span><span class="sxs-lookup"><span data-stu-id="cb43e-962">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cb43e-963">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb43e-963">Az.Accounts</span></span>
* <span data-ttu-id="cb43e-964">Åtgärdade ett problem som kan få Az att hoppa över loggar i Azure Automation- eller PowerShell-jobb [#11492]</span><span class="sxs-lookup"><span data-stu-id="cb43e-964">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="cb43e-965">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="cb43e-965">Az.AnalysisServices</span></span>
* <span data-ttu-id="cb43e-966">Uppdaterad sammansättningsversion för dataplan-cmdletar</span><span class="sxs-lookup"><span data-stu-id="cb43e-966">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="cb43e-967">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cb43e-967">Az.ApiManagement</span></span>
* <span data-ttu-id="cb43e-968">Uppdaterad sammansättningsversion för cmdletar för tjänsthantering</span><span class="sxs-lookup"><span data-stu-id="cb43e-968">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="cb43e-969">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="cb43e-969">Az.Billing</span></span>
* <span data-ttu-id="cb43e-970">Uppdaterad sammansättningsversion för förbrukningscmdletar</span><span class="sxs-lookup"><span data-stu-id="cb43e-970">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="cb43e-971">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cb43e-971">Az.CognitiveServices</span></span>
* <span data-ttu-id="cb43e-972">Stöd för PrivateEndpoint- och PublicNetworkAccess-kontroll.</span><span class="sxs-lookup"><span data-stu-id="cb43e-972">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="cb43e-973">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cb43e-973">Az.DataFactory</span></span>
* <span data-ttu-id="cb43e-974">Uppdaterad sammansättningsversion för datafabrik V2-cmdletar</span><span class="sxs-lookup"><span data-stu-id="cb43e-974">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="cb43e-975">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="cb43e-975">Az.DataShare</span></span>
* <span data-ttu-id="cb43e-976">Allmän tillgänglighet för modulen ”Az.DataShare”</span><span class="sxs-lookup"><span data-stu-id="cb43e-976">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="cb43e-977">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="cb43e-977">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="cb43e-978">Allmän tillgänglighet för modulen ”Az.DesktopVirtualization”</span><span class="sxs-lookup"><span data-stu-id="cb43e-978">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="cb43e-979">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cb43e-979">Az.OperationalInsights</span></span>
* <span data-ttu-id="cb43e-980">Uppgraderad SDK till 0.21.0</span><span class="sxs-lookup"><span data-stu-id="cb43e-980">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="cb43e-981">Lade till valfria parametrar till</span><span class="sxs-lookup"><span data-stu-id="cb43e-981">Added optional parameters to</span></span> 
    - <span data-ttu-id="cb43e-982">”New-AzOperationalInsightsSavedSearch”</span><span class="sxs-lookup"><span data-stu-id="cb43e-982">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="cb43e-983">”Set-AzOperationalInsightsSavedSearch”</span><span class="sxs-lookup"><span data-stu-id="cb43e-983">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="cb43e-984">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="cb43e-984">Az.PolicyInsights</span></span>
* <span data-ttu-id="cb43e-985">Korrigerade exempel 3 för ”Start-AzPolicyComplianceScan”</span><span class="sxs-lookup"><span data-stu-id="cb43e-985">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="cb43e-986">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="cb43e-986">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="cb43e-987">Uppdaterad sammansättningsversion för PowerBI-cmdletar</span><span class="sxs-lookup"><span data-stu-id="cb43e-987">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="cb43e-988">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="cb43e-988">Az.PrivateDns</span></span>
* <span data-ttu-id="cb43e-989">Korrigerade formatering av utförlig utdatasträng för Remove-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="cb43e-989">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cb43e-990">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb43e-990">Az.RecoveryServices</span></span>
* <span data-ttu-id="cb43e-991">Azure Site Recovery-stöd för att skapa en återställningsplan för replikering mellan zoner från xml-indata.</span><span class="sxs-lookup"><span data-stu-id="cb43e-991">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="cb43e-992">Uppdaterad sammansättningsversion för cmdletar för SiteRecovery och Backup</span><span class="sxs-lookup"><span data-stu-id="cb43e-992">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb43e-993">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb43e-993">Az.Resources</span></span>
* <span data-ttu-id="cb43e-994">Lade till slutparameter för cmdletarna Get-AzDeploymentScriptLog och Save-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="cb43e-994">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="cb43e-995">Formaterad utdataegenskap så att den kan visas i cmdlet-utdata för Get-AzDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="cb43e-995">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="cb43e-996">Bytte namn på parametern -DeploymentScriptInputObject till -DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="cb43e-996">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="cb43e-997">Åtgärdade saknade fil/målnamn i cmdlet-meddelanden.</span><span class="sxs-lookup"><span data-stu-id="cb43e-997">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="cb43e-998">Uppdaterad sammansättningsversion för cmdletar för resurshanterare och taggar</span><span class="sxs-lookup"><span data-stu-id="cb43e-998">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb43e-999">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb43e-999">Az.Sql</span></span>
* <span data-ttu-id="cb43e-1000">Lade till UsePrivateLinkConnection till ”New-AzSqlSyncGroup”, ”Update-AzSqlSyncGroup”, ”New-AzSqlSyncMember” och ”Update-AzSqlSyncMember”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1000">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="cb43e-1001">Lade till SyncMemberAzureDatabaseResourceId till ”New-AzSqlSyncMember” and ”Update-AzSqlSyncMember”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1001">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="cb43e-1002">Lade till stöd för att söka efter gästanvändare för att ange administratörs-cmdlet för SQL Server Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="cb43e-1002">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cb43e-1003">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb43e-1003">Az.Storage</span></span>
* <span data-ttu-id="cb43e-1004">Uppdaterad sammansättningsversion för dataplan-cmdletar</span><span class="sxs-lookup"><span data-stu-id="cb43e-1004">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="cb43e-1005">4.1.0 – maj 2020</span><span class="sxs-lookup"><span data-stu-id="cb43e-1005">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="cb43e-1006">Höjdpunkter sedan den senaste uppdateringen</span><span class="sxs-lookup"><span data-stu-id="cb43e-1006">Highlights since the last release</span></span>
* <span data-ttu-id="cb43e-1007">PowerShell-versioner som stöds: Windows PowerShell 5.1, PowerShell Core 6.2.4+ och PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="cb43e-1007">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="cb43e-1008">Allmän tillgänglighet för Az.Functions</span><span class="sxs-lookup"><span data-stu-id="cb43e-1008">General availability of Az.Functions</span></span> 
* <span data-ttu-id="cb43e-1009">Nya stora uppdateringar har gjorts för Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources och Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb43e-1009">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="cb43e-1010">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb43e-1010">Az.Accounts</span></span>
* <span data-ttu-id="cb43e-1011">”Add-AzEnvironment” och ”Set-AzEnvironment” har uppdaterats med stöd för parametrarna ”AzureSynapseAnalyticsEndpointResourceId” och ”AzureSynapseAnalyticsEndpointSuffix”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1011">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="cb43e-1012">Azure.Core-relaterade sammansättningar har lagts till i Az.Accounts; PowerShell-plattformar som stöds är Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span><span class="sxs-lookup"><span data-stu-id="cb43e-1012">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="cb43e-1013">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="cb43e-1013">Az.Aks</span></span>
* <span data-ttu-id="cb43e-1014">API-versionen har uppgraderats till 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="cb43e-1014">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="cb43e-1015">Stöds för att skapa AKS med hjälp av Windows-container</span><span class="sxs-lookup"><span data-stu-id="cb43e-1015">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="cb43e-1016">Nya cmdletar är tillgängliga: ”New-AzAksNodePool”, ”Update-AzAksNodePool”, ”Remove-AzAksNodePool”,        ”Get-AzAksNodePool”, ”Install-AzAksKubectl”, ”Get-AzAksVersion”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1016">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="cb43e-1017">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cb43e-1017">Az.ApiManagement</span></span>
* <span data-ttu-id="cb43e-1018">Parametrarna ”New-AzApiManagement” och ”Set-AzApiManagement”: [-AssignIdentity] har bytt namn till [-SystemAssignedIdentity]</span><span class="sxs-lookup"><span data-stu-id="cb43e-1018">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="cb43e-1019">”New-AzApiManagement” och ”Set-AzApiManagement”: En ny parameter har lagts till: [-UserAssignedIdentity <String[]>]</span><span class="sxs-lookup"><span data-stu-id="cb43e-1019">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="cb43e-1020">”Get-AzApiManagementProperty” har bytt namn till ”Get-AzApiManagementNamedValue”.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1020">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="cb43e-1021">PropertyId-parametern har bytt namn till NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1021">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="cb43e-1022">”New-AzApiManagementProperty” har bytt namn till ”New-AzApiManagementNamedValue”.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1022">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="cb43e-1023">PropertyId-parametern har bytt namn till NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1023">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="cb43e-1024">”Set-AzApiManagementProperty” har bytt namn till ”Set-AzApiManagementNamedValue”.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1024">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="cb43e-1025">PropertyId-parametern har bytt namn till NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1025">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="cb43e-1026">”Remove-AzApiManagementProperty” har bytt namn till ”Remove-AzApiManagementNamedValue”.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1026">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="cb43e-1027">PropertyId-parametern har bytt namn till NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1027">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="cb43e-1028">Den nya cmdleten Get-AzApiManagementAuthorizationServerClientSecret gör att ”Get-AzApiManagementAuthorizationServer” inte längre returnerar klienthemligheter.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1028">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="cb43e-1029">Den nya cmdleten ”Get-AzApiManagementNamedValueSecretValue” gör att ”Get-AzApiManagementNamedValue” inte returnerar värdet för en hemlighet.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1029">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="cb43e-1030">Den nya cmdleten ”Get-AzApiManagementOpenIdConnectProviderClientSecret” gör att ”Get-AzApiManagementOpenIdConnectProvider” inte längre returnerar klienthemligheter.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1030">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="cb43e-1031">Den nya cmdleten ”Get-AzApiManagementSubscriptionKey” gör att ”Get-AzApiManagementSubscription” inte längre returnerar prenumerationsnycklar.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1031">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="cb43e-1032">Den nya cmdleten ”Get-AzApiManagementTenantAccessSecret” gör att ”Get-AzApiManagementTenantAccess” inte längre returnerar nycklar.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1032">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="cb43e-1033">Den nya cmdleten ”Get-AzApiManagementTenantGitAccessSecret” gör att ”Get-AzApiManagementTenantGitAccess” inte längre returnerar nycklar.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1033">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="cb43e-1034">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="cb43e-1034">Az.ApplicationInsights</span></span>
* <span data-ttu-id="cb43e-1035">Tillagda parametrar: ”RetentionInDays” ”PublicNetworkAccessForIngestion” ”PublicNetworkAccessForQuery” för ”New-AzApplicationInsights”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1035">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="cb43e-1036">Cmdleten ”Update-AzApplicationInsights” har skapats</span><span class="sxs-lookup"><span data-stu-id="cb43e-1036">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="cb43e-1037">Cmdletar har skapats för länkat lagringskonto</span><span class="sxs-lookup"><span data-stu-id="cb43e-1037">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="cb43e-1038">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="cb43e-1038">Az.Batch</span></span>
* <span data-ttu-id="cb43e-1039">Az.Batch har uppdaterats att använda ”Microsoft.Azure.Batch” SDK version 13.0.0 och ”Microsoft.Azure.Management.Batch” SDK version 9.0.0.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1039">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="cb43e-1040">Nu kan du välja vilken typ av certifikat du lägger till genom att använda den nya parametern ”-CertificateKind” med ”New-AzBatchCertificate”.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1040">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="cb43e-1041">Egenskapen ”ApplicationPackages” har tagits bort från ”PSApplication”, som tidigare alltid var ''.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1041">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="cb43e-1042">Specifika paket i ett program kan nu hämtas med hjälp av ”Get-AzBatchApplicationPackage”.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1042">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="cb43e-1043">Ett exempel: ”Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication”.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1043">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="cb43e-1044">Nu när du skapar en pool med hjälp av ”New-AzBatchPool” kan egenskapen ”VirtualMachineImageId” för ”PSImageReference” endast referera till en Shared Image Gallery-avbildning.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1044">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="cb43e-1045">När du skapar en pool med hjälp av ”New-AzBatchPool” kan poolen etableras utan en offentlig IP-adress med hjälp av den nya egenskapen ”PublicIPAddressConfiguration” för ”PSNetworkConfiguration”.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1045">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="cb43e-1046">Egenskapen ”PublicIPs” för ”PSNetworkConfiguration” har också flyttats till ”PSPublicIPAddressConfiguration”.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1046">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="cb43e-1047">Den här egenskapen kan bara anges om ”IPAddressProvisioningType” är ”UserManaged”.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1047">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb43e-1048">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb43e-1048">Az.Compute</span></span>
* <span data-ttu-id="cb43e-1049">Parametern HostId har lagts till för cmdleten ”Update-AzVM”t</span><span class="sxs-lookup"><span data-stu-id="cb43e-1049">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="cb43e-1050">Hjälpdokumenten har uppdaterats för cmdletarna ”New-AzVMConfig”, ”New-AzVmssConfig”, ”Update-AzVmss”, ”Set-AzVMOperatingSystem” och ”Set-AzVmssOsProfile”.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1050">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="cb43e-1051">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="cb43e-1051">Breaking changes</span></span>
    - <span data-ttu-id="cb43e-1052">Parametern FilterExpression tas bort från cmdleten ”Get-AzVMImage”.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1052">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="cb43e-1053">Parametern AssignIdentity tas bort från cmdletarna ”New-AzVmssConfig”, ”New-AzVMConfig” och ”Update-AzVM”.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1053">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="cb43e-1054">AutomaticRepairMaxInstanceRepairsPercent tas bort från cmdletarna ”New-AzVmssConfig” och ”Update-AzVmss”.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1054">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="cb43e-1055">Egenskaperna AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus och VirtualMachineScaleSetsColocationStatus tas bort från ProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1055">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="cb43e-1056">Egenskapen MaxInstanceRepairsPercent tas bort från AutomaticRepairsPolicy.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1056">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="cb43e-1057">Typerna AvailabilitySets, VirtualMachines och VirtualMachineScaleSets ändras från IList<SubResource> till IList<SubResourceWithColocationStatus>.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1057">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="cb43e-1058">Beskrivningen för cmdleten ”Get-AzVM” har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1058">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="cb43e-1059">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cb43e-1059">Az.DataFactory</span></span>
* <span data-ttu-id="cb43e-1060">CRUD-stöd för egenskaper för dataflödeskörning  i hanterad IR.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1060">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="cb43e-1061">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="cb43e-1061">Az.FrontDoor</span></span>
* <span data-ttu-id="cb43e-1062">Nya cmdletar har lagts till för att skapa, uppdatera, hämta och ta bort (CRUD) Front Door-regelmotorobjekt</span><span class="sxs-lookup"><span data-stu-id="cb43e-1062">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="cb43e-1063">Hjälp-cmdletar har lagts till för konstruktion av Front Door-regelmotorobjekt</span><span class="sxs-lookup"><span data-stu-id="cb43e-1063">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="cb43e-1064">Regelmotorreferens har lagts till för Front Door-hanteringsregelobjekt.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1064">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="cb43e-1065">Parametrar för Private Link har lagts till för Front Door-serverdelsobjekt</span><span class="sxs-lookup"><span data-stu-id="cb43e-1065">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="cb43e-1066">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="cb43e-1066">Az.Functions</span></span>
* <span data-ttu-id="cb43e-1067">Allmän tillgänglighet för ”Az.Functions”-modulen</span><span class="sxs-lookup"><span data-stu-id="cb43e-1067">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="cb43e-1068">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cb43e-1068">Az.HDInsight</span></span>
* <span data-ttu-id="cb43e-1069">Stöd för diskkryptering med kundhanterad nyckel.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1069">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="cb43e-1070">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="cb43e-1070">Az.HealthcareApis</span></span>
* <span data-ttu-id="cb43e-1071">Åtkomstprinciper använder inte längre det aktiva huvudkontot som standard</span><span class="sxs-lookup"><span data-stu-id="cb43e-1071">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cb43e-1072">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cb43e-1072">Az.IotHub</span></span>
* <span data-ttu-id="cb43e-1073">En cmdlet har lagts till som anropar en fråga i en IoT-hubb för att hämta information med ett SQL-liknande språk.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1073">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="cb43e-1074">Problemet som gjorde att ”Add-AzIotHubDevice” inte skapade en Edge-aktiverad enhet utan underordnade enheter har åtgärdats [#11597]</span><span class="sxs-lookup"><span data-stu-id="cb43e-1074">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="cb43e-1075">En cmdlet har lagts till för att generera SAS-token för en Iot-hubb, enhet eller modul.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1075">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="cb43e-1076">En cmdlet har lagts till för att anropa en måttfråga om konfiguration.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1076">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="cb43e-1077">Hantera automatisk distribution av IoT Edge i stor skala.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1077">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="cb43e-1078">Nya cmdlet:ar är:</span><span class="sxs-lookup"><span data-stu-id="cb43e-1078">New cmdlets are:</span></span>
    - <span data-ttu-id="cb43e-1079">”Add-AzIotHubDeployment”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1079">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="cb43e-1080">”Get-AzIotHubDeployment”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1080">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="cb43e-1081">”Remove-AzIotHubDeployment”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1081">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="cb43e-1082">”Set-AzIotHubDeployment”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1082">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="cb43e-1083">En cmdlet har lagts till för att anropa en måttfråga om IoT Edge-distribution.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1083">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="cb43e-1084">En cmdlet har lagts till för att tillämpa konfigurationsinnehåll på den angivna gränsenheten.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1084">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cb43e-1085">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cb43e-1085">Az.KeyVault</span></span>
* <span data-ttu-id="cb43e-1086">Två alias har tagits bort: ”New-AzKeyVaultCertificateAdministratorDetails” och ”New-AzKeyVaultCertificateOrganizationDetails”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1086">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="cb43e-1087">Nu är mjuk borttagning aktiverat som standard när ett nyckelvalv skapas</span><span class="sxs-lookup"><span data-stu-id="cb43e-1087">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="cb43e-1088">Nätverksregler kan ställas in för att styra åtkomsten från särskilda nätverksplatser när du skapar ett nyckelvalv</span><span class="sxs-lookup"><span data-stu-id="cb43e-1088">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="cb43e-1089">Stöd för BYOK (Bring Your Own Key) har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-1089">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="cb43e-1090">”Add-AzKeyVaultKey” stöder generering av en KeyExchange-nyckel</span><span class="sxs-lookup"><span data-stu-id="cb43e-1090">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="cb43e-1091">”Get-AzKeyVaultKey” stöder nedladdning av en offentlig nyckel i PEM-format</span><span class="sxs-lookup"><span data-stu-id="cb43e-1091">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="cb43e-1092">”KeyOps”-delen av hjälpdokumentet för ”Add-AzKeyVaultKey” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="cb43e-1092">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cb43e-1093">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cb43e-1093">Az.Monitor</span></span>
* <span data-ttu-id="cb43e-1094">Bugg för ”Set-AzDiagnosticSettings” har åtgärdats; kvarhållningsprincipen tillämpas inte på alla kategorier [#11589]</span><span class="sxs-lookup"><span data-stu-id="cb43e-1094">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="cb43e-1095">Stöd för WebTest-tillgänglighetskriterier för måttavisering V2</span><span class="sxs-lookup"><span data-stu-id="cb43e-1095">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="cb43e-1096">”New-AzMetricAlertRuleV2Criteria”: ett alternativ för att skapa tillgänglighetskriterier för webbtest har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-1096">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="cb43e-1097">”Add-AzMetricAlertRuleV2”: stöd för de nya tillgänglighetskriterierna för webbtest</span><span class="sxs-lookup"><span data-stu-id="cb43e-1097">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="cb43e-1098">Redundant definition har tagits bort för RetentionPolicy i PSLogProfile [#7608]</span><span class="sxs-lookup"><span data-stu-id="cb43e-1098">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="cb43e-1099">Redundanta egenskaper som definierats i PSEventData har tagits bort [#11353]</span><span class="sxs-lookup"><span data-stu-id="cb43e-1099">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="cb43e-1100">”Get-AzLog” har bytt namn till ”Get-AzActivityLog”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1100">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb43e-1101">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb43e-1101">Az.Network</span></span>
* <span data-ttu-id="cb43e-1102">Attribut för icke-bakåtkompatibel ändring har lagts till för att meddela att standardbeteendet för zoner kommer att ändras</span><span class="sxs-lookup"><span data-stu-id="cb43e-1102">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="cb43e-1103">”New-AzPublicIpAddress”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1103">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="cb43e-1104">”New-AzPublicIpPrefix”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1104">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="cb43e-1105">”New-AzLoadBalancerFrontendIpConfig”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1105">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="cb43e-1106">Stöd har lagts till för en ny resurs på den översta nivån, SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="cb43e-1106">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="cb43e-1107">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="cb43e-1107">New cmdlets added:</span></span>
        - <span data-ttu-id="cb43e-1108">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="cb43e-1108">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="cb43e-1109">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="cb43e-1109">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="cb43e-1110">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="cb43e-1110">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="cb43e-1111">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="cb43e-1111">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="cb43e-1112">”RequiredZoneNames” har lagts till för ”PSPrivateLinkResource” och ”GroupId” för ”PSPrivateEndpointConnection”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1112">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="cb43e-1113">Fel parametertyp för SuccessThresholdRoundTripTimeMs-parametern för New-AzNetworkWatcherConnectionMonitorTestConfigurationObject har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="cb43e-1113">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="cb43e-1114">VirtualWan-cmdletar har uppdaterats för att ange AllowVnetToVnetTraffic-argumentets standardvärde till True.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1114">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="cb43e-1115">”New-AzVirtualWan”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1115">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="cb43e-1116">”Update-AzVirtualWan”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1116">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="cb43e-1117">Nya cmdletar har lagts till för att stödja DNS-zongrupp för privat slutpunkt</span><span class="sxs-lookup"><span data-stu-id="cb43e-1117">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="cb43e-1118">”New-AzPrivateDnsZoneConfig”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1118">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="cb43e-1119">”Get-AzPrivateDnsZoneGroup”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1119">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="cb43e-1120">”New-AzPrivateDnsZoneGroup”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1120">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="cb43e-1121">”Set-AzPrivateDnsZoneGroup”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1121">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="cb43e-1122">”Remove-AzPrivateDnsZoneGroup”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1122">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="cb43e-1123">Parametrarna ”DNSEnableProxy”, ”DNSRequireProxyForNetworkRules” och ”DNSServers” har lagts till för ”AzureFirewall”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1123">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="cb43e-1124">Parametrarna ”EnableDnsProxy”, ”DnsProxyNotRequiredForNetworkRule” och ”DnsServer” har lagts till för ”AzureFirewall”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1124">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="cb43e-1125">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="cb43e-1125">Updated cmdlet:</span></span>
        - <span data-ttu-id="cb43e-1126">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="cb43e-1126">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="cb43e-1127">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cb43e-1127">Az.OperationalInsights</span></span>
* <span data-ttu-id="cb43e-1128">Äldre kod har uppdaterats för att tillämpa ny genererad SDK</span><span class="sxs-lookup"><span data-stu-id="cb43e-1128">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="cb43e-1129">Cmdletar har tagits bort på grund av föråldrade API:er</span><span class="sxs-lookup"><span data-stu-id="cb43e-1129">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="cb43e-1130">”Get-AzOperationalInsightsSavedSearchResult” (alias ”Get-AzOperationalInsightsSavedSearchResults”)</span><span class="sxs-lookup"><span data-stu-id="cb43e-1130">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="cb43e-1131">”Get-AzOperationalInsightsSearchResult” (alias ”Get-AzOperationalInsightsSearchResults”)</span><span class="sxs-lookup"><span data-stu-id="cb43e-1131">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="cb43e-1132">”Get-AzOperationalInsightsLinkTarget” (alias ”Get-AzOperationalInsightsLinkTargets”)</span><span class="sxs-lookup"><span data-stu-id="cb43e-1132">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="cb43e-1133">Parametrar har lagts till för ”Set-AzOperationalInsightsWorkspace” och ”New-AzOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1133">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="cb43e-1134">Cmdletar har skapats för länkat lagringskonto</span><span class="sxs-lookup"><span data-stu-id="cb43e-1134">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="cb43e-1135">Cmdletar har skapats för kluster och länkad tjänst</span><span class="sxs-lookup"><span data-stu-id="cb43e-1135">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cb43e-1136">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb43e-1136">Az.RecoveryServices</span></span>
* <span data-ttu-id="cb43e-1137">Azure Site Recovery: Stöd har lagts till för att skydda VM-närhetsplaceringsgrupper för Azure till Azure-provider.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1137">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="cb43e-1138">Azure Site Recovery: Stöd har lagts till för replikering mellan zoner.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1138">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="cb43e-1139">Azure Backup: Stöd har lagts till för långsiktig kvarhållning för Azure FileShare-återställningspunkter.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1139">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="cb43e-1140">Azure Backup: Egenskaper för diskexkludering har lagts till för cmdlet-utdata från ”Get-AzRecoveryServicesBackupItem”.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1140">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="cb43e-1141">En privat slutpunkt har lagts till för filen med valvets autentiseringsuppgifter för Site Recovery-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1141">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb43e-1142">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb43e-1142">Az.Resources</span></span>
* <span data-ttu-id="cb43e-1143">En varning har lagts till om visningsfördröjning när en ny rolldefinition skapas</span><span class="sxs-lookup"><span data-stu-id="cb43e-1143">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="cb43e-1144">Princip-cmdletar har ändrats för utmatning av starkt typifierade objekt</span><span class="sxs-lookup"><span data-stu-id="cb43e-1144">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="cb43e-1145">Parametern ”-TenantLevel” har tagits bort för användning med ”Get-AzResourceLock” [#11335]</span><span class="sxs-lookup"><span data-stu-id="cb43e-1145">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="cb43e-1146">”Remove-AzResourceGroup -Id ResourceId” har åtgärdats [#9882]</span><span class="sxs-lookup"><span data-stu-id="cb43e-1146">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="cb43e-1147">En ny cmdlet har lagts till för att hämta What-If-resultat för ARM-mallar i omfånget för resursgrupper: ”Get-AzDeploymentResourceGroupWhatIfResult”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1147">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="cb43e-1148">En ny cmdlet har lagts till för att hämta What-If-resultat för ARM-mallar i prenumerationsomfånget: ”Get-AzDeploymentWhatIfResult”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1148">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="cb43e-1149">Alias: ”Get-AzSubscriptionDeploymentWhatIf”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1149">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="cb43e-1150">Parametrarna ”-WhatIf” och ”-Confirm” har åsidosatts för ”New-AzDeployment” och ”New-AzResourceGroupDeployment” för att använda What-If-resultat för ARM-mallar</span><span class="sxs-lookup"><span data-stu-id="cb43e-1150">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="cb43e-1151">Ett utfasningsmeddelande har lagts till för parametern ”ApiVersion” i distributions-cmdletar</span><span class="sxs-lookup"><span data-stu-id="cb43e-1151">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="cb43e-1152">En funktion har lagts till för att visa förbättrade felmeddelanden för distributionsfel</span><span class="sxs-lookup"><span data-stu-id="cb43e-1152">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="cb43e-1153">CorrelationId-loggning har lagts till för distributionsfel</span><span class="sxs-lookup"><span data-stu-id="cb43e-1153">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="cb43e-1154">Egenskapen ”error” har lagts till i utdata från distributionsskript</span><span class="sxs-lookup"><span data-stu-id="cb43e-1154">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="cb43e-1155">Nuget Microsoft.Azure.Management.ResourceManager har uppdaterats till ”3.7.1-preview”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1155">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="cb43e-1156">Specifika testfall har tagits bort då egenskapen Error i DeploymentValidateResult har ändrats till lässkyddad från nuget 3.7.1-preview</span><span class="sxs-lookup"><span data-stu-id="cb43e-1156">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="cb43e-1157">GenericResourceExpanded har flyttats från SDK ResourceManager 3.7.1-preview</span><span class="sxs-lookup"><span data-stu-id="cb43e-1157">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="cb43e-1158">Stöd för taggar har lagts till för alla Get-cmdletar för distribution, samt</span><span class="sxs-lookup"><span data-stu-id="cb43e-1158">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="cb43e-1159">”New-AzDeployment”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1159">'New-AzDeployment'</span></span>
    - <span data-ttu-id="cb43e-1160">”New-AzManagementGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1160">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="cb43e-1161">”New-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1161">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="cb43e-1162">”New-AzTenantDeployment”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1162">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="cb43e-1163">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cb43e-1163">Az.ServiceFabric</span></span>
* <span data-ttu-id="cb43e-1164">En bugg har åtgärdats som gjorde att --SecretIdentifier fick fel tumavtryck för certifikat när ett certifikat lades till</span><span class="sxs-lookup"><span data-stu-id="cb43e-1164">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb43e-1165">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb43e-1165">Az.Sql</span></span>
* <span data-ttu-id="cb43e-1166">Förbättrade prestanda för:</span><span class="sxs-lookup"><span data-stu-id="cb43e-1166">Enhance performance of:</span></span>
    - <span data-ttu-id="cb43e-1167">”Set-AzSqlDatabaseSensitivityClassification”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1167">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="cb43e-1168">”Set-AzSqlInstanceDatabaseSensitivityClassification”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1168">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="cb43e-1169">”Remove-AzSqlDatabaseSensitivityClassification”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1169">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="cb43e-1170">”Remove-AzSqlInstanceDatabaseSensitivityClassification”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1170">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="cb43e-1171">”Enable-AzSqlDatabaseSensitivityRecommendation”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1171">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="cb43e-1172">”Enable-AzSqlInstanceDatabaseSensitivityRecommendation”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1172">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="cb43e-1173">”Disable-AzSqlDatabaseSensitivityRecommendation”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1173">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="cb43e-1174">”Disable-AzSqlInstanceDatabaseSensitivityRecommendation”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1174">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="cb43e-1175">Validering på klientsidan har tagits bort för parametern ”RetentionDays” från cmdleten ”Set-AzSqlDatabaseBackupShortTermRetentionPolicy”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1175">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="cb43e-1176">Granskning av ett lagringskonto i Vnet; en bugg har åtgärdats som orsakade fel när en Storage Blob Data-deltagarroll skapades.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1176">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cb43e-1177">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb43e-1177">Az.Storage</span></span>
* <span data-ttu-id="cb43e-1178">”-AsJob” har lagts till för att hämta/lista konto med cmdleten ”Get-AzStorageAccount”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1178">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="cb43e-1179">Gör KeyVersion valfri när lagringskontot uppdateras med KeyvaultEncryption, för att ge stöd för automatisk nyckelrotation</span><span class="sxs-lookup"><span data-stu-id="cb43e-1179">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="cb43e-1180">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="cb43e-1180">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="cb43e-1181">Problemet med borttagning av Azure-filkatalog i pipeline har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="cb43e-1181">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="cb43e-1182">”Remove-AzStorageDirectory”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1182">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="cb43e-1183">Åtgärdat [#9880]: Definitionen av DefaultAction-värdet för NetWorkRule har ändrats för konsekvens med Swagger.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1183">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="cb43e-1184">”Update-AzStorageAccountNetworkRuleSet”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1184">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="cb43e-1185">”Get-AzStorageAccountNetworkRuleSet”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1185">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="cb43e-1186">Åtgärdat [#11624]: Hoppa över dubblettregler när NetworkRules läggs till, för att undvika serverfel</span><span class="sxs-lookup"><span data-stu-id="cb43e-1186">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="cb43e-1187">”Add-AzStorageAccountNetworkRule”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1187">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="cb43e-1188">Microsoft.Azure.Cosmos.Table SDK har uppgraderats till 1.0.7</span><span class="sxs-lookup"><span data-stu-id="cb43e-1188">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="cb43e-1189">Ett varningsmeddelande har lagts till för att påminna användaren om att lista igen med ContinuationToken när endast delobjekt returneras i listan med DataLake Gen2-objekt,</span><span class="sxs-lookup"><span data-stu-id="cb43e-1189">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="cb43e-1190">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="cb43e-1190">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="cb43e-1191">Stöd för att skapa eller uppdatera lagringskonto med Azure Files Active Directory Domain Service-autentisering</span><span class="sxs-lookup"><span data-stu-id="cb43e-1191">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="cb43e-1192">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="cb43e-1192">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="cb43e-1193">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="cb43e-1193">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="cb43e-1194">Stöd för nya eller listade Kerberos-nycklar för lagringskontot</span><span class="sxs-lookup"><span data-stu-id="cb43e-1194">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="cb43e-1195">”New-AzStorageAccountKey”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1195">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="cb43e-1196">”Get-AzStorageAccountKey”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1196">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="cb43e-1197">Stöd för redundans med lagringskonto</span><span class="sxs-lookup"><span data-stu-id="cb43e-1197">Supported failover Storage account</span></span>
    - <span data-ttu-id="cb43e-1198">”Invoke-AzStorageAccountFailover”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1198">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="cb43e-1199">Hjälpen för ”Get-AzStorageBlobCopyState” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="cb43e-1199">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="cb43e-1200">Hjälpen för ”Get-AzStorageFileCopyState” och ”Start-AzStorageBlobCopy” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="cb43e-1200">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="cb43e-1201">Lagringsklientbibliotek v12 har integrerats med Queue- och File-cmdletar</span><span class="sxs-lookup"><span data-stu-id="cb43e-1201">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="cb43e-1202">Utdatatypen har ändrats från CloudFile till AzureStorageFile; ursprungliga utdata blir en underordnad egenskap i den nya utmatningen</span><span class="sxs-lookup"><span data-stu-id="cb43e-1202">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="cb43e-1203">”Get-AzStorageFile”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1203">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="cb43e-1204">”Remove-AzStorageFile”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1204">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="cb43e-1205">”Get-AzStorageFileContent”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1205">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="cb43e-1206">”Set-AzStorageFileContent”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1206">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="cb43e-1207">”Start-AzStorageFileCopy”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1207">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="cb43e-1208">Utdatatypen har ändrats från CloudFileDirectory till AzureStorageFileDirectory; ursprungliga utdata blir en underordnad egenskap i den nya utmatningen</span><span class="sxs-lookup"><span data-stu-id="cb43e-1208">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="cb43e-1209">”New-AzStorageDirectory”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1209">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="cb43e-1210">”Remove-AzStorageDirectory”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1210">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="cb43e-1211">Utdatatypen har ändrats från CloudFileShare till AzureStorageFileShare; ursprungliga utdata blir en underordnad egenskap i den nya utmatningen</span><span class="sxs-lookup"><span data-stu-id="cb43e-1211">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="cb43e-1212">”Get-AzStorageShare”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1212">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="cb43e-1213">”New-AzStorageShare”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1213">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="cb43e-1214">”Remove-AzStorageShare”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1214">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="cb43e-1215">Utdatatypen har ändrats från FileShareProperties till AzureStorageFileShare; ursprungliga utdata blir en underordnad egenskap i den nya utmatningen</span><span class="sxs-lookup"><span data-stu-id="cb43e-1215">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="cb43e-1216">”Set-AzStorageShareQuota”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1216">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="cb43e-1217">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="cb43e-1217">Az.TrafficManager</span></span>
* <span data-ttu-id="cb43e-1218">Felaktigt profilnamn har åtgärdats i utförliga utdata för ”DisableAzureTrafficManagerEndpoint”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1218">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cb43e-1219">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb43e-1219">Az.Websites</span></span>
* <span data-ttu-id="cb43e-1220">Stavfel har åtgärdats i hjälpen för ”Update-AzWebAppAccessRestrictionConfig”.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1220">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="cb43e-1221">3.8.0 – April 2020</span><span class="sxs-lookup"><span data-stu-id="cb43e-1221">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="cb43e-1222">Höjdpunkter sedan den senaste uppdateringen</span><span class="sxs-lookup"><span data-stu-id="cb43e-1222">Highlights since the last release</span></span>
* <span data-ttu-id="cb43e-1223">PowerShell-versioner som Az.Storage stöder: Windows PowerShell 5.1, PowerShell Core 6.2.4+ och PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="cb43e-1223">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="cb43e-1224">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb43e-1224">Az.Accounts</span></span>
* <span data-ttu-id="cb43e-1225">Uppdaterade URL:en för Azure PowerShell-enkäten i ”Resolve-AzError” [#11507]</span><span class="sxs-lookup"><span data-stu-id="cb43e-1225">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="cb43e-1226">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cb43e-1226">Az.ApiManagement</span></span>
* <span data-ttu-id="cb43e-1227">Lade till meddelande om icke-bakåtkompatibel ändring vid ändring i utdata för Azure File-cmdletar i en framtida version</span><span class="sxs-lookup"><span data-stu-id="cb43e-1227">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="cb43e-1228">"Set-AzApiManagementGroup" Uppdaterad dokumentation för att ange GroupId-parametern</span><span class="sxs-lookup"><span data-stu-id="cb43e-1228">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="cb43e-1229">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="cb43e-1229">Az.Cdn</span></span>
* <span data-ttu-id="cb43e-1230">Fast ChinaCDN-relaterad prissättning för SKU-visning</span><span class="sxs-lookup"><span data-stu-id="cb43e-1230">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="cb43e-1231">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cb43e-1231">Az.CognitiveServices</span></span>
* <span data-ttu-id="cb43e-1232">Identitet som stöds, kryptering, UserOwnedStorage</span><span class="sxs-lookup"><span data-stu-id="cb43e-1232">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb43e-1233">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb43e-1233">Az.Compute</span></span>
* <span data-ttu-id="cb43e-1234">Cmdleten ”Set-AzVmssOrchestrationServiceState” har lagts till.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1234">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="cb43e-1235">”Get-AzVmss” med -InstanceView visar OrchestrationService-tillstånd.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1235">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cb43e-1236">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cb43e-1236">Az.IotHub</span></span>
* <span data-ttu-id="cb43e-1237">Hantera den dubbla konfigurationen för IoT-enheter, nya cmdletar är:</span><span class="sxs-lookup"><span data-stu-id="cb43e-1237">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="cb43e-1238">'Get-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="cb43e-1238">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="cb43e-1239">'Update-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="cb43e-1239">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="cb43e-1240">En cmdlet har lagts till för att anropa direkt metod på en enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1240">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="cb43e-1241">Hantera dubbel konfiguration för IoT-enhetsmodul, nya cmdletar är:</span><span class="sxs-lookup"><span data-stu-id="cb43e-1241">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="cb43e-1242">'Get-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="cb43e-1242">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="cb43e-1243">'Update-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="cb43e-1243">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="cb43e-1244">Hantera IoT-automatisk konfiguration av enhetshantering i stor skala.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1244">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="cb43e-1245">Nya cmdlet:ar är:</span><span class="sxs-lookup"><span data-stu-id="cb43e-1245">New cmdlets are:</span></span>
    - <span data-ttu-id="cb43e-1246">'Add-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="cb43e-1246">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="cb43e-1247">'Get-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="cb43e-1247">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="cb43e-1248">'Remove-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="cb43e-1248">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="cb43e-1249">'Set-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="cb43e-1249">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="cb43e-1250">En cmdlet har lagts till för att anropa en edge-modulmetod i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1250">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cb43e-1251">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cb43e-1251">Az.KeyVault</span></span>
* <span data-ttu-id="cb43e-1252">Har lagt till en ny cmdlet, "Update-AzKeyVault", som kan aktivera mjuk borttagning och rensning av skydd i ett valv</span><span class="sxs-lookup"><span data-stu-id="cb43e-1252">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="cb43e-1253">Har lagt till stöd i Microsoft.PowerShell.SecretManagement [#11178]</span><span class="sxs-lookup"><span data-stu-id="cb43e-1253">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="cb43e-1254">Åtgärdat fel i exemplen i 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span><span class="sxs-lookup"><span data-stu-id="cb43e-1254">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="cb43e-1255">Har lagt till stöd för privat slutpunkt</span><span class="sxs-lookup"><span data-stu-id="cb43e-1255">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="cb43e-1256">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="cb43e-1256">Az.Maintenance</span></span>
* <span data-ttu-id="cb43e-1257">Publicerar slutversion av underhålls-cmdletar för GA</span><span class="sxs-lookup"><span data-stu-id="cb43e-1257">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cb43e-1258">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cb43e-1258">Az.Monitor</span></span>
* <span data-ttu-id="cb43e-1259">Har lagt till cmdletar för privat länkomfång</span><span class="sxs-lookup"><span data-stu-id="cb43e-1259">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="cb43e-1260">'Get-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="cb43e-1260">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="cb43e-1261">'Remove-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="cb43e-1261">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="cb43e-1262">'New-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="cb43e-1262">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="cb43e-1263">'Update-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="cb43e-1263">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="cb43e-1264">'Get-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="cb43e-1264">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="cb43e-1265">'New-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="cb43e-1265">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="cb43e-1266">'Remove-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="cb43e-1266">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb43e-1267">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb43e-1267">Az.Network</span></span>
* <span data-ttu-id="cb43e-1268">Uppdaterade cmdletar för att aktivera anslutning på privat IP för Virtual Network Gateway.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1268">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="cb43e-1269">'New-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="cb43e-1269">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="cb43e-1270">'Set-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="cb43e-1270">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="cb43e-1271">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="cb43e-1271">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="cb43e-1272">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="cb43e-1272">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="cb43e-1273">Uppdaterade cmdletar för att aktivera FQDN-baserade LocalNetworkGateways och VpnSites</span><span class="sxs-lookup"><span data-stu-id="cb43e-1273">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="cb43e-1274">'New-AzLocalNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="cb43e-1274">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="cb43e-1275">'New-AzVpnSiteLink'</span><span class="sxs-lookup"><span data-stu-id="cb43e-1275">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="cb43e-1276">Stöd har lagts till för IPv6-adresstypen i ExpressRouteCircuitConnectionConfig (Global Reach)</span><span class="sxs-lookup"><span data-stu-id="cb43e-1276">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="cb43e-1277">Lade till 'Set-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="cb43e-1277">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="cb43e-1278">tillåter inställning av alla befintliga egenskaper inklusive IPv6CircuitConnectionProperties</span><span class="sxs-lookup"><span data-stu-id="cb43e-1278">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="cb43e-1279">Uppdaterade 'Add-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="cb43e-1279">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="cb43e-1280">Lade till en ytterligare valfri parameter, AddressPrefixType, för att specificera adresstypen för adressprefix</span><span class="sxs-lookup"><span data-stu-id="cb43e-1280">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="cb43e-1281">Uppdaterade cmdletar för att aktivera inställningen för DPD-timeout på Virtual Network Gateway-anslutningar.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1281">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="cb43e-1282">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="cb43e-1282">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="cb43e-1283">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="cb43e-1283">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="cb43e-1284">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="cb43e-1284">Az.PolicyInsights</span></span>
* <span data-ttu-id="cb43e-1285">Cmdleten "Start-AzPolicyComplianceScan" har lagts till för att utlösa genomsökningar av principefterlevnad</span><span class="sxs-lookup"><span data-stu-id="cb43e-1285">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="cb43e-1286">Principdefinition, uppsättningsdefinition och tilldelningsversioner har lagts till i "Get-AzPolicyState"-utdata</span><span class="sxs-lookup"><span data-stu-id="cb43e-1286">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="cb43e-1287">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cb43e-1287">Az.ServiceFabric</span></span>
* <span data-ttu-id="cb43e-1288">Förbättrad kodformatering och användbarhet för "New-AzServiceFabricCluster"-exempel</span><span class="sxs-lookup"><span data-stu-id="cb43e-1288">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb43e-1289">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb43e-1289">Az.Sql</span></span>
* <span data-ttu-id="cb43e-1290">Lade till cmdletarna "Get-AzSqlInstanceOperation" och "Stop-AzSqlInstanceOperation"</span><span class="sxs-lookup"><span data-stu-id="cb43e-1290">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="cb43e-1291">Stöd för granskning för ett lagringskonto i VNet.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1291">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cb43e-1292">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb43e-1292">Az.Storage</span></span>
* <span data-ttu-id="cb43e-1293">Lade till meddelande om icke-bakåtkompatibel ändring vid ändring i utdata för Azure File-cmdletar i en framtida version</span><span class="sxs-lookup"><span data-stu-id="cb43e-1293">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="cb43e-1294">Stöd för nya SkuName StandardGZRS, StandardRAGZRS när ett lagringskonto skapas/uppdateras</span><span class="sxs-lookup"><span data-stu-id="cb43e-1294">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="cb43e-1295">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="cb43e-1295">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="cb43e-1296">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="cb43e-1296">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="cb43e-1297">Stöd för DataLake Gen2</span><span class="sxs-lookup"><span data-stu-id="cb43e-1297">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="cb43e-1298">'New-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="cb43e-1298">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="cb43e-1299">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="cb43e-1299">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="cb43e-1300">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="cb43e-1300">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="cb43e-1301">'Move-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="cb43e-1301">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="cb43e-1302">'Set-AzDataLakeGen2ItemAclObject'</span><span class="sxs-lookup"><span data-stu-id="cb43e-1302">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="cb43e-1303">'Update-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="cb43e-1303">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="cb43e-1304">'Get-AzDataLakeGen2ItemContent'</span><span class="sxs-lookup"><span data-stu-id="cb43e-1304">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="cb43e-1305">'Remove-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="cb43e-1305">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="cb43e-1306">0.10.0-förhandsversion – April 2020</span><span class="sxs-lookup"><span data-stu-id="cb43e-1306">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="cb43e-1307">Allmänt</span><span class="sxs-lookup"><span data-stu-id="cb43e-1307">General</span></span>
* <span data-ttu-id="cb43e-1308">Az-moduler är nu tillgängliga i förhandsversion på Azure Stack Hub.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1308">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="cb43e-1309">Därmed möjliggörs kompatibilitet för flera plattformar med Linux och macOs.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1309">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="cb43e-1310">Azure Stack Hub stöder nu PowerShell Core med AZ-moduler. Mer information finns [här](/azure-stack/operator/powershell-install-az-module)</span><span class="sxs-lookup"><span data-stu-id="cb43e-1310">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](/azure-stack/operator/powershell-install-az-module)</span></span>
* <span data-ttu-id="cb43e-1311">Supportprofil för AZ-moduler 2019-03-01-hybrid:</span><span class="sxs-lookup"><span data-stu-id="cb43e-1311">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="cb43e-1312">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="cb43e-1312">Az.Billing</span></span>
  - <span data-ttu-id="cb43e-1313">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb43e-1313">Az.Compute</span></span>
  - <span data-ttu-id="cb43e-1314">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="cb43e-1314">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="cb43e-1315">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="cb43e-1315">Az.EventHub</span></span>
  - <span data-ttu-id="cb43e-1316">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cb43e-1316">Az.IotHub</span></span>
  - <span data-ttu-id="cb43e-1317">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cb43e-1317">Az.KeyVault</span></span>
  - <span data-ttu-id="cb43e-1318">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cb43e-1318">Az.Monitor</span></span>
  - <span data-ttu-id="cb43e-1319">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb43e-1319">Az.Network</span></span>
  - <span data-ttu-id="cb43e-1320">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb43e-1320">Az.Resources</span></span>
  - <span data-ttu-id="cb43e-1321">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb43e-1321">Az.Storage</span></span>
  - <span data-ttu-id="cb43e-1322">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb43e-1322">Az.Websites</span></span>
* <span data-ttu-id="cb43e-1323">Tre nya PowerShell-moduler för AZ har introducerats som fungerar med Azure Stack Hub, och de är Az.Databox, Az.IotHub och Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="cb43e-1323">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="cb43e-1324">Kommandona är i princip oförändrade, med endast mindre ändringar som att AzureRM ändras till AZ</span><span class="sxs-lookup"><span data-stu-id="cb43e-1324">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="cb43e-1325">En uppdaterad länk till PowerShell-dokumentationen för Azure Stack Hub finns [här](/azure-stack/operator/powershell-install-az-module)</span><span class="sxs-lookup"><span data-stu-id="cb43e-1325">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](/azure-stack/operator/powershell-install-az-module)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="cb43e-1326">3.7.0 – mars 2020</span><span class="sxs-lookup"><span data-stu-id="cb43e-1326">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cb43e-1327">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb43e-1327">Az.Accounts</span></span>
* <span data-ttu-id="cb43e-1328">Åtgärdade ”Get-AzTenant”/”Get-AzDefault”/”Set-AzDefault”-utlösning av NullReferenceException när du inte är inloggad [#10292]</span><span class="sxs-lookup"><span data-stu-id="cb43e-1328">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb43e-1329">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb43e-1329">Az.Compute</span></span>
* <span data-ttu-id="cb43e-1330">Följande parametrar har lagts till i cmdleten ”New-AzDiskConfig”:</span><span class="sxs-lookup"><span data-stu-id="cb43e-1330">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="cb43e-1331">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="cb43e-1331">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="cb43e-1332">Tillåten krypteringsegenskap till målparametern för cmdleten ”New-AzGalleryImageVersion”.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1332">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="cb43e-1333">Åtgärdade tempDisk-problem för cmdletarna ”Set-AzVmss”-Reimage och ”Invoke-AzVMReimage”.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1333">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="cb43e-1334">[#11354]</span><span class="sxs-lookup"><span data-stu-id="cb43e-1334">[#11354]</span></span>
* <span data-ttu-id="cb43e-1335">Stöd har lagts till i nedanstående cmdletar för nytt SAP-tillägg</span><span class="sxs-lookup"><span data-stu-id="cb43e-1335">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="cb43e-1336">”Set-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1336">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="cb43e-1337">”Get-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1337">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="cb43e-1338">”Remove-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1338">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="cb43e-1339">”Update-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1339">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="cb43e-1340">Åtgärdade fel i exempel på hjälpdokument</span><span class="sxs-lookup"><span data-stu-id="cb43e-1340">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="cb43e-1341">Visade det exakta strängvärdet för VM PowerState i tabellformat.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1341">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="cb43e-1342">”New-AzVmssConfig”: den fasta serialiseringen av egenskapen AutomaticRepairs när SinglePlacementGroup är inaktiverad.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1342">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="cb43e-1343">[#11257]</span><span class="sxs-lookup"><span data-stu-id="cb43e-1343">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cb43e-1344">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cb43e-1344">Az.DataFactory</span></span>
* <span data-ttu-id="cb43e-1345">ADF .Net SDK har uppdaterats till 4.8.0</span><span class="sxs-lookup"><span data-stu-id="cb43e-1345">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="cb43e-1346">Valfria parametrar har lagts till i kommandot ”Invoke-AzDataFactoryV2Pipeline” för att stödja omkörning</span><span class="sxs-lookup"><span data-stu-id="cb43e-1346">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cb43e-1347">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cb43e-1347">Az.DataLakeStore</span></span>
* <span data-ttu-id="cb43e-1348">Lade till beskrivning för icke-bakåtkompatibel ändring för ”Export-AzDataLakeStoreItem” och ”Import-AzDataLakeStoreItem”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1348">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="cb43e-1349">Lade till alternativ för bytekodning för ”New-AzDataLakeStoreItem”, ”Add-AzDAtaLakeStoreItemContent” och ”Get-AzDAtaLakeStoreItemContent”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1349">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="cb43e-1350">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cb43e-1350">Az.HDInsight</span></span>
* <span data-ttu-id="cb43e-1351">Stöd för att ange en minimal TLS-version som stöds när klustret skapas.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1351">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cb43e-1352">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cb43e-1352">Az.IotHub</span></span>
* <span data-ttu-id="cb43e-1353">Stöd har lagts till för att hantera distribuerade inställningar per enhet.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1353">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="cb43e-1354">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="cb43e-1354">New Cmdlets are:</span></span>
    - <span data-ttu-id="cb43e-1355">”Get-AzIotHubDistributedTracing”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1355">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="cb43e-1356">”Set-AzIotHubDistributedTracing”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1356">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cb43e-1357">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cb43e-1357">Az.KeyVault</span></span>
* <span data-ttu-id="cb43e-1358">Ändrade attribut för icke-bakåtkompatibel ändring lades till för ”New-AzKeyVault”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1358">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cb43e-1359">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cb43e-1359">Az.Monitor</span></span>
* <span data-ttu-id="cb43e-1360">Uppdaterad dokumentation för ”New-AzScheduledQueryRuleLogMetricTrigger”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1360">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb43e-1361">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb43e-1361">Az.Network</span></span>
* <span data-ttu-id="cb43e-1362">Uppdaterade cmdletar för att tillåta VirtualHubVnetConnections mellan klienter</span><span class="sxs-lookup"><span data-stu-id="cb43e-1362">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="cb43e-1363">”New-AzVirtualHubVnetConnection”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1363">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="cb43e-1364">”Update-AzVirtualHubVnetConnection”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1364">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="cb43e-1365">”New-AzVirtualHub”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1365">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="cb43e-1366">”Update-AzVirtualHub”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1366">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="cb43e-1367">SQL Management SDK-beroende har tagits bort</span><span class="sxs-lookup"><span data-stu-id="cb43e-1367">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="cb43e-1368">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="cb43e-1368">Az.PolicyInsights</span></span>
* <span data-ttu-id="cb43e-1369">Förbättrade felmeddelanden</span><span class="sxs-lookup"><span data-stu-id="cb43e-1369">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cb43e-1370">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb43e-1370">Az.RecoveryServices</span></span>
* <span data-ttu-id="cb43e-1371">Azure Site Recovery har lagt till stöd för återaktivering av skydd och uppdaterade VM-egenskaper för virtuella Azure-datorer med krypterad disk.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1371">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="cb43e-1372">Lade till Azure Site Recovery VmwareToAzure-egenskaper för DR-övervakning</span><span class="sxs-lookup"><span data-stu-id="cb43e-1372">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="cb43e-1373">Azure Backup har lagt till stöd för att försöka uppdatera principuppdateringen för misslyckade objekt på nytt.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1373">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="cb43e-1374">Azure Backup lagt till stöd för diskundantagsinställningar under säkerhetskopiering och återställning.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1374">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="cb43e-1375">Azure Backup lagt till stöd för att återställa flera filer/mappar i AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="cb43e-1375">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="cb43e-1376">Azure Backup lade till support för användardefinierad Resourcegroup-support vid uppdatering av IaasVM-princip</span><span class="sxs-lookup"><span data-stu-id="cb43e-1376">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb43e-1377">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb43e-1377">Az.Resources</span></span>
* <span data-ttu-id="cb43e-1378">Åtgärdade ”Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType” så att den använder den faktisk apiVersion av resurser i stället för standard-apiVersion [#11267]</span><span class="sxs-lookup"><span data-stu-id="cb43e-1378">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="cb43e-1379">Lade till correlationId-loggning för felscenarier</span><span class="sxs-lookup"><span data-stu-id="cb43e-1379">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="cb43e-1380">Liten dokumentationsändring för ”Get-AzResourceLock”.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1380">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="cb43e-1381">Lade till exempel.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1381">Added example.</span></span>
* <span data-ttu-id="cb43e-1382">Undantaget enkelt citattecken i parametervärde för ”Get-AzADUser” [#11317]</span><span class="sxs-lookup"><span data-stu-id="cb43e-1382">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="cb43e-1383">Nya cmdletar har lagts till för distributionsskript (”Get-AzDeploymentScript”, ”Get-AzDeploymentScriptLog”, ”Save-AzDeploymentScriptLog”, ”Remove-AzDeploymentScript”)</span><span class="sxs-lookup"><span data-stu-id="cb43e-1383">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb43e-1384">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb43e-1384">Az.Sql</span></span>
* <span data-ttu-id="cb43e-1385">En läsbar sekundär parameter har lagts till i Invoke-AzSqlDatabaseFailover</span><span class="sxs-lookup"><span data-stu-id="cb43e-1385">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="cb43e-1386">Cmdleten Disable-AzSqlServerActiveDirectoryOnlyAuthentication har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-1386">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="cb43e-1387">Den sparade känslighet rangordningen när kolumner klassificeras i databasen.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1387">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="cb43e-1388">Az.Support</span><span class="sxs-lookup"><span data-stu-id="cb43e-1388">Az.Support</span></span>
* <span data-ttu-id="cb43e-1389">Allmän tillgänglighet för ”Az.Support”-modulen</span><span class="sxs-lookup"><span data-stu-id="cb43e-1389">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cb43e-1390">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb43e-1390">Az.Websites</span></span>
* <span data-ttu-id="cb43e-1391">Stöd har lagts till för att arbeta med trafikdirigeringsregler för webbappar under nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="cb43e-1391">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="cb43e-1392">”Get-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1392">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="cb43e-1393">”Update-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1393">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="cb43e-1394">”Add-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1394">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="cb43e-1395">”Remove-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1395">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="cb43e-1396">3.6.1 – mars 2020</span><span class="sxs-lookup"><span data-stu-id="cb43e-1396">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cb43e-1397">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb43e-1397">Az.Accounts</span></span>
* <span data-ttu-id="cb43e-1398">Öppna sidan med Azure PowerShell-enkäten i ”Send-Feedback” [#11020]</span><span class="sxs-lookup"><span data-stu-id="cb43e-1398">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="cb43e-1399">Visa URL:en för Azure PowerShell-enkäten i ”Resolve-Error” [#11021]</span><span class="sxs-lookup"><span data-stu-id="cb43e-1399">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="cb43e-1400">Az-version har lagts till i UserAgent</span><span class="sxs-lookup"><span data-stu-id="cb43e-1400">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="cb43e-1401">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cb43e-1401">Az.ApiManagement</span></span>
* <span data-ttu-id="cb43e-1402">Stöd har lagts till för att hämta och konfigurera en anpassad domän på DeveloperPortal-slutpunkten [#11007]</span><span class="sxs-lookup"><span data-stu-id="cb43e-1402">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="cb43e-1403">”Export-AzApiManagementApi” Stöd har lagts till för att ladda ned API-definition i Json-format [#9987]</span><span class="sxs-lookup"><span data-stu-id="cb43e-1403">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="cb43e-1404">”Import-AzApiManagementApi” Stöd har lagts till för att importera OpenApi 3.0-definition från Json-dokument</span><span class="sxs-lookup"><span data-stu-id="cb43e-1404">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="cb43e-1405">”New-AzApiManagementIdentityProvider” och ”Set-AzApiManagementIdentityProvider” Stöd har lagts till för att konfigurera ”Signin Tenant” för AAD B2C-provider [#9784]</span><span class="sxs-lookup"><span data-stu-id="cb43e-1405">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cb43e-1406">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cb43e-1406">Az.DataLakeStore</span></span>
* <span data-ttu-id="cb43e-1407">En referens har uttryckligen lagts till för System.Buffers i csproj och psd1.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1407">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cb43e-1408">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cb43e-1408">Az.IotHub</span></span>
* <span data-ttu-id="cb43e-1409">Lade till stöd för att hantera enheter i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1409">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="cb43e-1410">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="cb43e-1410">New Cmdlets are:</span></span>
    - <span data-ttu-id="cb43e-1411">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="cb43e-1411">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="cb43e-1412">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="cb43e-1412">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="cb43e-1413">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="cb43e-1413">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="cb43e-1414">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="cb43e-1414">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="cb43e-1415">Stöd har lagts till för att hantera moduler på en mål-IoT-enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1415">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="cb43e-1416">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="cb43e-1416">New Cmdlets are:</span></span>
    - <span data-ttu-id="cb43e-1417">”Add-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1417">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="cb43e-1418">”Get-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1418">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="cb43e-1419">”Remove-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1419">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="cb43e-1420">”Set-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1420">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="cb43e-1421">Cmdlet har lagts till för att hämta anslutningssträngen för en mål-IoT-enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1421">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="cb43e-1422">Cmdlet har lagts till för att hämta anslutningssträngen för en modul på en mål-IoT-enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1422">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="cb43e-1423">Stöd har lagts till för att hämta/ange en överordnad enhet för en IoT-enhet.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1423">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="cb43e-1424">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="cb43e-1424">New Cmdlets are:</span></span>
    - <span data-ttu-id="cb43e-1425">”Get-AzIotHubDeviceParent”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1425">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="cb43e-1426">”Set-AzIotHubDeviceParent”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1426">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="cb43e-1427">Stöd har lagts till för att hantera en enhets överordnade och underordnade relationer.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1427">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cb43e-1428">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cb43e-1428">Az.Monitor</span></span>
* <span data-ttu-id="cb43e-1429">Utdatavärdet har åtgärdats för ”Get-AzMetricDefinition” [#9714]</span><span class="sxs-lookup"><span data-stu-id="cb43e-1429">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb43e-1430">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb43e-1430">Az.Network</span></span>
* <span data-ttu-id="cb43e-1431">SQL Management SDK har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1431">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="cb43e-1432">Ett problem har åtgärdats med namngivningsskillnader i klassen PrivateLinkServiceConnectionState.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1432">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="cb43e-1433">Fältet ActionsRequired mappar till ActionRequired.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1433">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="cb43e-1434">PublicNetworkAccess har lagts till i ”New-AzSqlServer” och ”Set-AzSqlServer”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1434">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb43e-1435">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb43e-1435">Az.Resources</span></span>
* <span data-ttu-id="cb43e-1436">Null-referensfel har åtgärdats i ”Get-AzRoleAssignment”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1436">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="cb43e-1437">Växlarna ”-Force” och ”-PassThru” är valfria i ”Remove-AzADGroup” [#10849]</span><span class="sxs-lookup"><span data-stu-id="cb43e-1437">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="cb43e-1438">Ett problem har åtgärdats som gjorde att ”MailNickname” inte returnerades i ”Remove-AzADGroup” [#11167]</span><span class="sxs-lookup"><span data-stu-id="cb43e-1438">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="cb43e-1439">Ett problem har åtgärdats som gjorde att pipe-åtgärden ”Remove-AzADGroup” inte fungerar [#11171]</span><span class="sxs-lookup"><span data-stu-id="cb43e-1439">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="cb43e-1440">Ett null-referensfel har åtgärdats i GetAzureRoleAssignmentCommand</span><span class="sxs-lookup"><span data-stu-id="cb43e-1440">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="cb43e-1441">Attribut för icke-bakåtkompatibla ändringar har lagts till för kommande ändringar i cmdlets för principer</span><span class="sxs-lookup"><span data-stu-id="cb43e-1441">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="cb43e-1442">”Get-AzResourceGroup” har uppdaterats för att utföra taggfiltrering för resursgrupper på serversidan</span><span class="sxs-lookup"><span data-stu-id="cb43e-1442">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="cb43e-1443">Utökade Tag-cmdlets stöder -ResourceId</span><span class="sxs-lookup"><span data-stu-id="cb43e-1443">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="cb43e-1444">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="cb43e-1444">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="cb43e-1445">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="cb43e-1445">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="cb43e-1446">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="cb43e-1446">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="cb43e-1447">Ny Tag-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-1447">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="cb43e-1448">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="cb43e-1448">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="cb43e-1449">Flyttade ScopedDeployment från SDK 3.3.0</span><span class="sxs-lookup"><span data-stu-id="cb43e-1449">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb43e-1450">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb43e-1450">Az.Sql</span></span>
* <span data-ttu-id="cb43e-1451">PublicNetworkAccess har lagts till i ”New-AzSqlServer” och ”Set-AzSqlServer”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1451">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="cb43e-1452">Stöd har lagts till för konfiguration av säkerhetskopiering för långsiktig kvarhållning för hanterade databaser</span><span class="sxs-lookup"><span data-stu-id="cb43e-1452">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="cb43e-1453">Hämta/ange LTR-princip på en hanterad databas</span><span class="sxs-lookup"><span data-stu-id="cb43e-1453">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="cb43e-1454">Hämta LTR-säkerhetskopior efter hanterad databas, hanterad instans eller plats</span><span class="sxs-lookup"><span data-stu-id="cb43e-1454">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="cb43e-1455">Ta bort en LTR-säkerhetskopia</span><span class="sxs-lookup"><span data-stu-id="cb43e-1455">Remove an LTR backup</span></span>
    - <span data-ttu-id="cb43e-1456">Återställa en LTR-säkerhetskopia för att skapa en ny hanterad databas</span><span class="sxs-lookup"><span data-stu-id="cb43e-1456">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="cb43e-1457">MinimalTlsVersion har lagts till för New-AzSqlServer och Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="cb43e-1457">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="cb43e-1458">MinimalTlsVersion har lagts till för New-AzSqlInstance och Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="cb43e-1458">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="cb43e-1459">SQL SDK-versionen för Az.Network har ändrats</span><span class="sxs-lookup"><span data-stu-id="cb43e-1459">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cb43e-1460">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb43e-1460">Az.Storage</span></span>
* <span data-ttu-id="cb43e-1461">AllowProtectedAppendWrite stöds i ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="cb43e-1461">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="cb43e-1462">”Set-AzRmStorageContainerImmutabilityPolicy”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1462">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="cb43e-1463">Varningsmeddelande har lagts till om icke-bakåtkompatibel ändring för ändring av typen AzureStorageTable i en senare version</span><span class="sxs-lookup"><span data-stu-id="cb43e-1463">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="cb43e-1464">”New-AzStorageTable”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1464">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="cb43e-1465">”Get-AzStorageTable”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1465">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cb43e-1466">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb43e-1466">Az.Websites</span></span>
* <span data-ttu-id="cb43e-1467">Tag-parametern har lagts till för ”New-AzAppServicePlan” och ”Set-AzAppServicePlan”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1467">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="cb43e-1468">Stoppa cmdlet-körning om ett undantag uppstår när en anpassad domän läggs till på en webbplats</span><span class="sxs-lookup"><span data-stu-id="cb43e-1468">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="cb43e-1469">Stöd har lagts till för att utföra åtgärder för App Services som inte tillhör samma resursgrupp som App Services-planen</span><span class="sxs-lookup"><span data-stu-id="cb43e-1469">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="cb43e-1470">Åtkomstbegränsning har tillämpats på WebApp/Function i olika resursgrupper</span><span class="sxs-lookup"><span data-stu-id="cb43e-1470">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="cb43e-1471">Ett problem har åtgärdats för att ange anpassade värdnamn för WebAppSlots</span><span class="sxs-lookup"><span data-stu-id="cb43e-1471">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="cb43e-1472">3.5.0 – februari 2020</span><span class="sxs-lookup"><span data-stu-id="cb43e-1472">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="cb43e-1473">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="cb43e-1473">Highlights since the last major release</span></span>
* <span data-ttu-id="cb43e-1474">Uppdaterade telemetri på klientsidan.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1474">Updated client side telemetry.</span></span>
* <span data-ttu-id="cb43e-1475">Az.IotHub lade till cmdletar som stöd för att hantera enheter.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1475">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="cb43e-1476">Az.SqlVirtualMachine lade till cmdletar för lyssningsfunktion för tillgänglighetsgrupp.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1476">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="cb43e-1477">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb43e-1477">Az.Accounts</span></span>
* <span data-ttu-id="cb43e-1478">Lade till SubscriptionId, TenantId och körningstid i data för telemetri på klientsidan</span><span class="sxs-lookup"><span data-stu-id="cb43e-1478">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cb43e-1479">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cb43e-1479">Az.Automation</span></span>
* <span data-ttu-id="cb43e-1480">Åtgärdade skrivfel i exempel 1 i referensdokumentation för ”New-AzAutomationSoftwareUpdateConfiguration”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1480">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="cb43e-1481">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cb43e-1481">Az.CognitiveServices</span></span>
* <span data-ttu-id="cb43e-1482">Uppdaterade SDK till 7.0</span><span class="sxs-lookup"><span data-stu-id="cb43e-1482">Updated SDK to 7.0</span></span>
* <span data-ttu-id="cb43e-1483">Förbättrade felmeddelande vid serversvar om tom brödtext</span><span class="sxs-lookup"><span data-stu-id="cb43e-1483">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb43e-1484">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb43e-1484">Az.Compute</span></span>
* <span data-ttu-id="cb43e-1485">Tillät tomt värde för ProximityPlacementGroupId under uppdatering</span><span class="sxs-lookup"><span data-stu-id="cb43e-1485">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="cb43e-1486">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="cb43e-1486">Az.FrontDoor</span></span>
* <span data-ttu-id="cb43e-1487">Lade till cmdlet för att hämta hanterade regeldefinitioner som kan användas i WAF</span><span class="sxs-lookup"><span data-stu-id="cb43e-1487">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cb43e-1488">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cb43e-1488">Az.IotHub</span></span>
* <span data-ttu-id="cb43e-1489">Lade till stöd för att hantera enheter i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1489">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="cb43e-1490">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="cb43e-1490">New Cmdlets are:</span></span>
    - <span data-ttu-id="cb43e-1491">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="cb43e-1491">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="cb43e-1492">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="cb43e-1492">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="cb43e-1493">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="cb43e-1493">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="cb43e-1494">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="cb43e-1494">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cb43e-1495">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cb43e-1495">Az.KeyVault</span></span>
* <span data-ttu-id="cb43e-1496">Åtgärdade duplicerad text för Add-AzKeyVaultKey.md</span><span class="sxs-lookup"><span data-stu-id="cb43e-1496">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cb43e-1497">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cb43e-1497">Az.Monitor</span></span>
* <span data-ttu-id="cb43e-1498">Åtgärdade beskrivning av cmdleten Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1498">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="cb43e-1499">En ny parameter med namnet ActionGroupId har lagts till i kommandot ”New-AzMetricAlertRuleV2”.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1499">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="cb43e-1500">Användaren kan ange ActionGroupId(string) eller ActionGroup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="cb43e-1500">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb43e-1501">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb43e-1501">Az.Network</span></span>
* <span data-ttu-id="cb43e-1502">Lade till en extra parameteranteckning för parametern ”-EnableProxyProtocol” för cmdleten ”New-AzPrivateLinkService”.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1502">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="cb43e-1503">Åtgärdade FilterData-exempel i Start-AzVirtualNetworkGatewayConnectionPacketCapture.md och Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1503">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="cb43e-1504">Lade till paketinsamlingsexempel för att samla in alla inre och yttre paket i Start-AzVirtualNetworkGatewayConnectionPacketCapture.md och Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1504">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="cb43e-1505">Lade till stöd för Azure-brandväggsprincip på VNet-brandväggar</span><span class="sxs-lookup"><span data-stu-id="cb43e-1505">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="cb43e-1506">Inga nya cmdletar har lagts till.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1506">No new cmdlets are added.</span></span> <span data-ttu-id="cb43e-1507">Lättar begränsningen för brandväggsprincip på VNet-brandväggar</span><span class="sxs-lookup"><span data-stu-id="cb43e-1507">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cb43e-1508">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb43e-1508">Az.RecoveryServices</span></span>
* <span data-ttu-id="cb43e-1509">Lade till stöd för Restore-as-files för SQL-databaser.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1509">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb43e-1510">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb43e-1510">Az.Resources</span></span>
* <span data-ttu-id="cb43e-1511">Omstrukturerade cmdletar för malldistribution</span><span class="sxs-lookup"><span data-stu-id="cb43e-1511">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="cb43e-1512">Lade till nya cmdletar för att hantera distributioner i hanteringsgruppen: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="cb43e-1512">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="cb43e-1513">Lade till nya cmdletar för att hantera distributioner i klientorganisationsområdet: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="cb43e-1513">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="cb43e-1514">Omstrukturerade \*-AzDeployment-cmdletar för att fungera specifikt i prenumerationsomfattningen</span><span class="sxs-lookup"><span data-stu-id="cb43e-1514">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="cb43e-1515">Skapade alias \*-AzSubscriptionDeployment för \*-AzDeployment-cmdletar</span><span class="sxs-lookup"><span data-stu-id="cb43e-1515">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="cb43e-1516">Åtgärdade ”Update-AzADApplication” när parametern ”AvailableToOtherTenants” inte har angetts</span><span class="sxs-lookup"><span data-stu-id="cb43e-1516">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="cb43e-1517">Tog bort ApplicationObjectWithoutCredentialParameterSet för att undvika AmbiguousParameterSetException.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1517">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="cb43e-1518">Återskapade hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="cb43e-1518">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb43e-1519">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb43e-1519">Az.Sql</span></span>
* <span data-ttu-id="cb43e-1520">Lade till stöd för återställning till tidpunkt mellan prenumerationer på hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1520">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="cb43e-1521">Lade till stöd för att ändra befintlig SQL Managed Instance-maskinvarugenerering</span><span class="sxs-lookup"><span data-stu-id="cb43e-1521">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="cb43e-1522">Åtgärdade ”Update-AzSqlServerVulnerabilityAssessmentSetting”-hjälpexempel: parameter/egenskapsutdata - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="cb43e-1522">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="cb43e-1523">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="cb43e-1523">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="cb43e-1524">Lade till cmdletar för lyssningsfunktion för tillgänglighetsgrupp</span><span class="sxs-lookup"><span data-stu-id="cb43e-1524">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="cb43e-1525">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="cb43e-1525">Az.StorageSync</span></span>
* <span data-ttu-id="cb43e-1526">Uppdaterade teckenuppsättningar som stöds i ”Invoke-AzStorageSyncCompatibilityCheck”.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1526">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="cb43e-1527">3.4.0 – februari 2020</span><span class="sxs-lookup"><span data-stu-id="cb43e-1527">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="cb43e-1528">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="cb43e-1528">Highlights since the last major release</span></span>
* <span data-ttu-id="cb43e-1529">Första Az.CosmosDB-versionen 0.1.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="cb43e-1529">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="cb43e-1530">Stöd för Az.Network ConnectionMonitor V2 har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-1530">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="cb43e-1531">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb43e-1531">Az.Accounts</span></span>
* <span data-ttu-id="cb43e-1532">Inaktivera automatisk sparande av kontext när AzureRmContext.json inte är tillgängligt</span><span class="sxs-lookup"><span data-stu-id="cb43e-1532">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="cb43e-1533">Uppdatera referensen till Azure Powershell Common till 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="cb43e-1533">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="cb43e-1534">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cb43e-1534">Az.ApiManagement</span></span>
* <span data-ttu-id="cb43e-1535">**Get-AzApiManagementApiSchema** Hämtning av Open-Api-schema som är associerat med ett API har åtgärdats   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="cb43e-1535">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="cb43e-1536">**New-AzApiManagementProduct** _ och _ *Set-AzApiManagementProduct*\*</span><span class="sxs-lookup"><span data-stu-id="cb43e-1536">**New-AzApiManagementProduct** _ and _ *Set-AzApiManagementProduct*\*</span></span>
  - <span data-ttu-id="cb43e-1537">Åtgärda dokumentation för https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="cb43e-1537">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="cb43e-1538">**Set-AzApiManagementApi** Exempel för att visa hur ServiceUrl uppdateras med hjälp av cmdleten har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-1538">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb43e-1539">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb43e-1539">Az.Compute</span></span>
* <span data-ttu-id="cb43e-1540">Begränsa antalet VM-status till 100 för att undvika begränsning när Get-AzVM -Status utförs utan VM-namn.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1540">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="cb43e-1541">Lägg till cmdleten Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="cb43e-1541">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="cb43e-1542">Lägg till parametrarna EncryptionType och DiskEncryptionSetId i följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="cb43e-1542">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="cb43e-1543">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="cb43e-1543">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="cb43e-1544">Lägg till parametern ColocationStatus för cmdleten Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1544">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cb43e-1545">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cb43e-1545">Az.DataFactory</span></span>
* <span data-ttu-id="cb43e-1546">Uppdatera ADF .Net SDK-versionen till 4.7.0</span><span class="sxs-lookup"><span data-stu-id="cb43e-1546">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="cb43e-1547">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="cb43e-1547">Az.DeploymentManager</span></span>
* <span data-ttu-id="cb43e-1548">Lägger till LIST-åtgärder för resurser</span><span class="sxs-lookup"><span data-stu-id="cb43e-1548">Adds LIST operations for resources</span></span>
* <span data-ttu-id="cb43e-1549">Lägger till funktion för att utföra åtgärder för hälsokontrollsteg</span><span class="sxs-lookup"><span data-stu-id="cb43e-1549">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="cb43e-1550">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cb43e-1550">Az.HDInsight</span></span>
* <span data-ttu-id="cb43e-1551">Åtgärda dokumentfel för New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1551">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cb43e-1552">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cb43e-1552">Az.KeyVault</span></span>
* <span data-ttu-id="cb43e-1553">Lägg till Name-alias för attributet VaultName så att Remove-AzureKeyVault stämmer överens med New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1553">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb43e-1554">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb43e-1554">Az.Network</span></span>
* <span data-ttu-id="cb43e-1555">Nytt exempel har lagts till i Set-AzNetworkWatcherConfigFlowLog.md för att demonstrera ett inaktiveringsscenario för Trafikanalys.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1555">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="cb43e-1556">Lägg till stöd för att tilldela konfiguration av hanterings-IP till Azure Firewall – ett dedikerat undernät och en offentlig IP som brandväggen använder för dess hanteringstrafik</span><span class="sxs-lookup"><span data-stu-id="cb43e-1556">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="cb43e-1557">Cmdleten New-AzFirewall har uppdaterats:</span><span class="sxs-lookup"><span data-stu-id="cb43e-1557">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="cb43e-1558">Parametern -ManagementPublicIpAddress (inte obligatorisk) som accepterar ett offentligt IP-adressobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-1558">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="cb43e-1559">Metoden SetManagementIpConfiguration har lagts till för brandväggsobjekt – kräver ett undernät och en offentlig IP-adress som indata – undernätets namn måste vara ”AzureFirewallManagementSubnet”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1559">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="cb43e-1560">Exempel för Get-AzNetworkSecurityGroup har korrigerats så att exempel visas för NSG:er i stället för nätverksgränssnitt.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1560">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="cb43e-1561">Ett skrivfel har åtgärdats i kommandot New-AzVpnSite som hindrade kompletteraren för resurs-ID från att fylla i en parameter.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1561">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="cb43e-1562">Stöd för Url-konfiguration i åtgärdsuppsättningen för omskrivningsregler i Application Gateway har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-1562">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="cb43e-1563">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="cb43e-1563">New cmdlets added:</span></span>
        - <span data-ttu-id="cb43e-1564">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb43e-1564">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="cb43e-1565">Cmdletar har uppdaterats med den valfria parametern -UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb43e-1565">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="cb43e-1566">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="cb43e-1566">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="cb43e-1567">Lägg till stöd för resurser för NetworkWatcher ConnectionMonitor version 2</span><span class="sxs-lookup"><span data-stu-id="cb43e-1567">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="cb43e-1568">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="cb43e-1568">Az.PolicyInsights</span></span>
* <span data-ttu-id="cb43e-1569">Stöd för utvärdering av efterlevnad innan fastställande av vilken resurs som ska åtgärdas</span><span class="sxs-lookup"><span data-stu-id="cb43e-1569">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="cb43e-1570">Lägg till parametern ”-ResourceDiscoverMode” för Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="cb43e-1570">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="cb43e-1571">Lägg till cmdleten Get-AzPolicyMetadata för att hämta resurser för principmetadata</span><span class="sxs-lookup"><span data-stu-id="cb43e-1571">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="cb43e-1572">Get-AzPolicyState och Get-AzPolicyStateSummary för API-versionen 2019-10-01 har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="cb43e-1572">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cb43e-1573">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb43e-1573">Az.RecoveryServices</span></span>
* <span data-ttu-id="cb43e-1574">Azure Site Recovery-stöd för att ta bort en replikerad disk.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1574">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="cb43e-1575">Tillagt Azure Backup-stöd för att lägga till taggar när ett Recovery Services-valv skapas.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1575">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb43e-1576">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb43e-1576">Az.Resources</span></span>
* <span data-ttu-id="cb43e-1577">Gör -Scope valfritt i cmdletarna \*-AzPolicyAssignment med standardinställning till kontextprenumeration</span><span class="sxs-lookup"><span data-stu-id="cb43e-1577">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="cb43e-1578">Lägg till exempel på att skapa ADServicePrincipal med lösenord och nyckelautentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="cb43e-1578">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb43e-1579">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb43e-1579">Az.Sql</span></span>
<span data-ttu-id="cb43e-1580">Åtgärda cmdleten New-AzSqlDatabaseSecondary så att existensen PartnerDatabaseName kontrolleras i stället för existensen DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1580">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cb43e-1581">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb43e-1581">Az.Storage</span></span>
* <span data-ttu-id="cb43e-1582">Stöd för angivning av krypteringsnyckeltyp för Tabell/kö i Skapa lagringskonto</span><span class="sxs-lookup"><span data-stu-id="cb43e-1582">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="cb43e-1583">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cb43e-1583">New-AzStorageAccount</span></span>
* <span data-ttu-id="cb43e-1584">Visa RequestId när StorageException inte har ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="cb43e-1584">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="cb43e-1585">Åtgärda exempel 6 för cmdleten Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="cb43e-1585">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cb43e-1586">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb43e-1586">Az.Websites</span></span>
* <span data-ttu-id="cb43e-1587">Set-AzWebapp och Set-AzWebappSlot stöder egenskaperna AlwaysOn, MinTls och FtpsState</span><span class="sxs-lookup"><span data-stu-id="cb43e-1587">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="cb43e-1588">Åtgärdar problemet där inställning av HttpsOnly samtidigt som AppservicePlan ändrades med det enskilda kommandot Set-AzWebApp återställde HttpsOnly till standardvärdet</span><span class="sxs-lookup"><span data-stu-id="cb43e-1588">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="cb43e-1589">3.3.0 – januari 2020</span><span class="sxs-lookup"><span data-stu-id="cb43e-1589">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cb43e-1590">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb43e-1590">Az.Accounts</span></span>
* <span data-ttu-id="cb43e-1591">Nu stöder Add-AzEnvironment och Set-AzEnvironment parametrarna AzureAttestationServiceEndpointResourceId och AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="cb43e-1591">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="cb43e-1592">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="cb43e-1592">Az.Cdn</span></span>
* <span data-ttu-id="cb43e-1593">Information om felsvar visas i New-AzCdnEndpoint-cmdleten</span><span class="sxs-lookup"><span data-stu-id="cb43e-1593">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb43e-1594">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb43e-1594">Az.Compute</span></span>
* <span data-ttu-id="cb43e-1595">Set-AzVMCustomScriptExtension-cmdleten har åtgärdats för en virtuell dator med hanterad OD-disk som inte har någon operativsystemprofil.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1595">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="cb43e-1596">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="cb43e-1596">Az.ContainerInstance</span></span>
* <span data-ttu-id="cb43e-1597">Parameternamn som används med New-AzContainerGroup-exempel har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="cb43e-1597">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="cb43e-1598">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="cb43e-1598">Az.DataBoxEdge</span></span>
* <span data-ttu-id="cb43e-1599">Cmdleten ”Get-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-1599">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="cb43e-1600">Hämta gränslagringscontainern</span><span class="sxs-lookup"><span data-stu-id="cb43e-1600">Get the Edge Storage Container</span></span>
* <span data-ttu-id="cb43e-1601">Cmdleten ”New-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-1601">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="cb43e-1602">Skapa en ny gränslagringscontainer</span><span class="sxs-lookup"><span data-stu-id="cb43e-1602">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="cb43e-1603">Cmdleten ”Remove-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-1603">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="cb43e-1604">Ta bort gränslagringscontainern</span><span class="sxs-lookup"><span data-stu-id="cb43e-1604">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="cb43e-1605">Cmdleten ”Invoke-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-1605">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="cb43e-1606">Anropa åtgärd för att uppdatera data i gränslagringscontainer</span><span class="sxs-lookup"><span data-stu-id="cb43e-1606">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="cb43e-1607">Cmdleten ”Get-AzDataBoxEdgeStorageAccount” har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-1607">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="cb43e-1608">Hämta gränslagringskontot</span><span class="sxs-lookup"><span data-stu-id="cb43e-1608">Get the Edge Storage Account</span></span>
* <span data-ttu-id="cb43e-1609">Cmdleten ”New-AzDataBoxEdgeStorageAccount” har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-1609">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="cb43e-1610">Skapa ett nytt gränslagringskonto</span><span class="sxs-lookup"><span data-stu-id="cb43e-1610">Create new Edge Storage Account</span></span>
* <span data-ttu-id="cb43e-1611">Cmdleten ”Remove-AzDataBoxEdgeStorageAccount” har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-1611">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="cb43e-1612">Ta bort gränslagringskontot</span><span class="sxs-lookup"><span data-stu-id="cb43e-1612">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="cb43e-1613">Anropa cmdleten ”Invoke-AzDataBoxEdgeShare”</span><span class="sxs-lookup"><span data-stu-id="cb43e-1613">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="cb43e-1614">Anropa åtgärd för att uppdatera resursdata</span><span class="sxs-lookup"><span data-stu-id="cb43e-1614">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="cb43e-1615">Cmdleten ”Set-AzDataBoxEdgeStorageAccountCredential” har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-1615">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="cb43e-1616">Ange autentiseringsuppgifter för az databoxedge-lagringskonto</span><span class="sxs-lookup"><span data-stu-id="cb43e-1616">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cb43e-1617">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cb43e-1617">Az.DataFactory</span></span>
* <span data-ttu-id="cb43e-1618">Lägg till AutoUpdateETA-, LatestVersion-, PushedVersion-, TaskQueueId- och VersionStatus-egenskaper för Get-AzDataFactoryV2IntegrationRuntime-cmd</span><span class="sxs-lookup"><span data-stu-id="cb43e-1618">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="cb43e-1619">Uppdatera ADF .Net SDK-versionen till 4.6.0</span><span class="sxs-lookup"><span data-stu-id="cb43e-1619">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="cb43e-1620">Lägg till parametern ”PublicIPs” för ”Set-AzureRmDataFactoryV2IntegrationRuntime”-cmd så att Azure-SSIS IR kan skapas med statiska offentliga IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1620">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="cb43e-1621">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="cb43e-1621">Az.DevTestLabs</span></span>
* <span data-ttu-id="cb43e-1622">Ta bort den brutna länken i Get-AzDtlAllowedVMSizesPolicy.md</span><span class="sxs-lookup"><span data-stu-id="cb43e-1622">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="cb43e-1623">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="cb43e-1623">Az.EventHub</span></span>
* <span data-ttu-id="cb43e-1624">Korrigering av problem 10634: Åtgärda referensen till null-objekt för eventhubnamespace-borttagning</span><span class="sxs-lookup"><span data-stu-id="cb43e-1624">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="cb43e-1625">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cb43e-1625">Az.HDInsight</span></span>
* <span data-ttu-id="cb43e-1626">Åtgärda Invoke-AzHDInsightHiveJob.md-fel.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1626">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="cb43e-1627">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="cb43e-1627">Az.MachineLearning</span></span>
* <span data-ttu-id="cb43e-1628">Nedanstående cmdletar har tagits bort eftersom MachineLearningCompute inte längre är tillgängligt</span><span class="sxs-lookup"><span data-stu-id="cb43e-1628">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="cb43e-1629">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="cb43e-1629">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="cb43e-1630">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="cb43e-1630">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="cb43e-1631">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="cb43e-1631">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="cb43e-1632">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="cb43e-1632">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="cb43e-1633">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="cb43e-1633">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="cb43e-1634">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="cb43e-1634">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="cb43e-1635">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="cb43e-1635">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb43e-1636">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb43e-1636">Az.Network</span></span>
* <span data-ttu-id="cb43e-1637">Uppgradera beroende av Microsoft.Azure.Management.Sql från 1.36-preview till 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="cb43e-1637">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cb43e-1638">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb43e-1638">Az.RecoveryServices</span></span>
* <span data-ttu-id="cb43e-1639">Ändrat Azure Site Recovery-stöd för krypterade vilande data på virtuella datorer med hanterade diskar med kundhanterade nycklar för Azure till Azure-providern.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1639">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="cb43e-1640">Azure Site Recovery-stöd för att ange ID för diskkrypteringsuppsättning som valfri inmatning för aktivering av skydd för VMware till Azure.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1640">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="cb43e-1641">Azure Site Recovery-stöd för att ange ID för diskkrypteringsuppsättning som valfri inmatning på disknivå för aktivering av skydd för VMware till Azure.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1641">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="cb43e-1642">Azure Site Recovery-stöd för att uppdatera replikeringsskyddade objekt med mappning för diskkrypteringsuppsättning för HyperV till Azure.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1642">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb43e-1643">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb43e-1643">Az.Resources</span></span>
* <span data-ttu-id="cb43e-1644">Åtgärda ett fel i hjälpdokument för ”Remove-AzTag”.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1644">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb43e-1645">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb43e-1645">Az.Sql</span></span>
* <span data-ttu-id="cb43e-1646">Åtgärda funktioner i cmdletar för att ange baslinjen för sårbarhetsbedömning för arbete med huvuddatabasen för Azure-databasen och begränsa den för systemdatabaser på hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1646">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="cb43e-1647">Åtgärda ett fel när en redundansgrupp för en SQL-instans skapas</span><span class="sxs-lookup"><span data-stu-id="cb43e-1647">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="cb43e-1648">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="cb43e-1648">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="cb43e-1649">Lägg till DR som en ny giltig licenstyp</span><span class="sxs-lookup"><span data-stu-id="cb43e-1649">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cb43e-1650">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb43e-1650">Az.Storage</span></span>
* <span data-ttu-id="cb43e-1651">Lägg till varningsmeddelande om icke-bakåtkompatibel ändring för DefaultAction-värdeändring i en framtida version</span><span class="sxs-lookup"><span data-stu-id="cb43e-1651">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="cb43e-1652">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="cb43e-1652">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="cb43e-1653">Stöd för att hämta lagringskontots senaste synkroniseringstid genom att köra get-AzureRMStorageAccount med parametern -IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="cb43e-1653">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="cb43e-1654">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cb43e-1654">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="cb43e-1655">3.2.0 – December 2019</span><span class="sxs-lookup"><span data-stu-id="cb43e-1655">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="cb43e-1656">Allmänt</span><span class="sxs-lookup"><span data-stu-id="cb43e-1656">General</span></span>
* <span data-ttu-id="cb43e-1657">Uppdatera referenser i .psd1 för att använda relativa sökvägar för alla moduler</span><span class="sxs-lookup"><span data-stu-id="cb43e-1657">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="cb43e-1658">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb43e-1658">Az.Accounts</span></span>
* <span data-ttu-id="cb43e-1659">Ange rätt UserAgent för telemetri på klientsidan för Az 4.0 preview</span><span class="sxs-lookup"><span data-stu-id="cb43e-1659">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="cb43e-1660">Visa användarvänligt felmeddelande när kontexten är null i Az 4.0 preview</span><span class="sxs-lookup"><span data-stu-id="cb43e-1660">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="cb43e-1661">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="cb43e-1661">Az.Batch</span></span>
* <span data-ttu-id="cb43e-1662">Korrigera problem [#10602](https://github.com/Azure/azure-powershell/issues/10602), där **New-AzBatchPool** skickade VirtualMachineConfiguration.ContainerConfiguration eller VirtualMachineConfiguration.DataDisks på ett felaktigt sätt till servern.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1662">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cb43e-1663">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cb43e-1663">Az.DataFactory</span></span>
* <span data-ttu-id="cb43e-1664">Uppdatera ADF .Net SDK-versionen till 4.5.0</span><span class="sxs-lookup"><span data-stu-id="cb43e-1664">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="cb43e-1665">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="cb43e-1665">Az.FrontDoor</span></span>
* <span data-ttu-id="cb43e-1666">Stöd har lagts till för undantag för hanterade regler för brandväggen för webbaserade program</span><span class="sxs-lookup"><span data-stu-id="cb43e-1666">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="cb43e-1667">Lägg till SocketAddr för automatisk komplettering</span><span class="sxs-lookup"><span data-stu-id="cb43e-1667">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="cb43e-1668">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="cb43e-1668">Az.HealthcareApis</span></span>
* <span data-ttu-id="cb43e-1669">Undantagshantering</span><span class="sxs-lookup"><span data-stu-id="cb43e-1669">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cb43e-1670">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cb43e-1670">Az.KeyVault</span></span>
* <span data-ttu-id="cb43e-1671">Åtgärdat fel vid åtkomst av värde som kanske inte har angetts</span><span class="sxs-lookup"><span data-stu-id="cb43e-1671">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="cb43e-1672">Hantering av ECC-certifikat (Elliptic Curve Cryptography)</span><span class="sxs-lookup"><span data-stu-id="cb43e-1672">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="cb43e-1673">Stöd har lagts till för att ange kurvan för certifikatprinciper</span><span class="sxs-lookup"><span data-stu-id="cb43e-1673">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cb43e-1674">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cb43e-1674">Az.Monitor</span></span>
* <span data-ttu-id="cb43e-1675">Lägger till valfritt argument i kommandot Lägg till diagnostikinställningar.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1675">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="cb43e-1676">Ett växelargument som om det finns visar att exporten till Log Analytics måste ske till ett fast schema (kallas även</span><span class="sxs-lookup"><span data-stu-id="cb43e-1676">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="cb43e-1677">dedikerad, datatyp)</span><span class="sxs-lookup"><span data-stu-id="cb43e-1677">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb43e-1678">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb43e-1678">Az.Network</span></span>
* <span data-ttu-id="cb43e-1679">Stöd för IpGroups i program-, NAT- och nätverksregler för Azure Firewall.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1679">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb43e-1680">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb43e-1680">Az.Resources</span></span>
* <span data-ttu-id="cb43e-1681">Åtgärda ett problem där malldistributionen inte kan läsa en mallparameter om dess namn står i konflikt med ett inbyggt parameternamn.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1681">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="cb43e-1682">Uppdaterade princip-cmdletar för att använda den nya API-versionen 2019-09-01 som introducerar grupperingsstöd inom principuppsättningsdefinitioner.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1682">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb43e-1683">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb43e-1683">Az.Sql</span></span>
* <span data-ttu-id="cb43e-1684">Uppgraderad funktion för att skapa lagring i automatisk aktivering av sårbarhetsbedömning till StorageV2</span><span class="sxs-lookup"><span data-stu-id="cb43e-1684">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cb43e-1685">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb43e-1685">Az.Storage</span></span>
* <span data-ttu-id="cb43e-1686">Stöd för generering av blob/container-identitetsbaserad SAS-token med lagringskontextbaserad på OAuth-autentisering</span><span class="sxs-lookup"><span data-stu-id="cb43e-1686">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="cb43e-1687">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="cb43e-1687">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="cb43e-1688">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="cb43e-1688">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="cb43e-1689">Stöd för återkallning av användardelegeringsnycklar för lagringskonto för att återkalla alla SAS-token</span><span class="sxs-lookup"><span data-stu-id="cb43e-1689">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="cb43e-1690">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="cb43e-1690">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="cb43e-1691">Uppgradera till Microsoft.Azure.Management.Storage 14.2.0 för att stödja den nya API-versionen 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1691">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="cb43e-1692">Stöd för QuotaGiB (resurskvot i Gibibye) för värden över 5120 i hanteringsplanet för cmdletar för filresurser och parameteraliaset. Quota har också lagts till för parametern ”QuotaGiB”.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1692">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="cb43e-1693">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="cb43e-1693">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="cb43e-1694">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="cb43e-1694">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="cb43e-1695">Lägg till parameteraliaset QuotaGiB i parametern Quota</span><span class="sxs-lookup"><span data-stu-id="cb43e-1695">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="cb43e-1696">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="cb43e-1696">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="cb43e-1697">Åtgärda problemet att Set-AzStorageContainerAcl kan rensa den lagrade åtkomstprincipen</span><span class="sxs-lookup"><span data-stu-id="cb43e-1697">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="cb43e-1698">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="cb43e-1698">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="cb43e-1699">3.1.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="cb43e-1699">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="cb43e-1700">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="cb43e-1700">Highlights since the last major release</span></span>
* <span data-ttu-id="cb43e-1701">Az.DataBoxEdge 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="cb43e-1701">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="cb43e-1702">Az.SqlVirtualMachine 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="cb43e-1702">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb43e-1703">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb43e-1703">Az.Compute</span></span>
* <span data-ttu-id="cb43e-1704">Funktion för att använda en virtuell dator igen</span><span class="sxs-lookup"><span data-stu-id="cb43e-1704">VM Reapply feature</span></span>
    - <span data-ttu-id="cb43e-1705">Lägg till parameter för att använda igen till cmdleten Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="cb43e-1705">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="cb43e-1706">Funktionen AutomaticRepairs i VM-skalningsuppsättningar:</span><span class="sxs-lookup"><span data-stu-id="cb43e-1706">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="cb43e-1707">Lägg till parametrarna EnableAutomaticRepair, AutomaticRepairGracePeriod och AutomaticRepairMaxInstanceRepairsPercent till följande cmdletar:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="cb43e-1707">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="cb43e-1708">Stöd för galleriavbildningar i flera klientorganisationer för New-AzVM</span><span class="sxs-lookup"><span data-stu-id="cb43e-1708">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="cb43e-1709">Lägg till "Spot" till argumentslutföraren i prioritetsparametern i cmdletarna New-AzVM, New-AzVMConfig och New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="cb43e-1709">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="cb43e-1710">Lägg till parametrarna DiskIOPSReadWrite och DiskMBpsReadWrite till cmdleten Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="cb43e-1710">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="cb43e-1711">Ändra parametern SourceImageId för cmdleten New-AzGalleryImageVersion till valfri</span><span class="sxs-lookup"><span data-stu-id="cb43e-1711">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="cb43e-1712">Lägg till parametrarna OSDiskImage och DataDiskImage till cmdleten New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="cb43e-1712">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="cb43e-1713">Lägg till parametern HyperVGeneration till cmdleten New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="cb43e-1713">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="cb43e-1714">Lägg till parametern SkipExtensionsOnOverprovisionedVMs till cmdletarna New-AzVmss, New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="cb43e-1714">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="cb43e-1715">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="cb43e-1715">Az.DataBoxEdge</span></span>
* <span data-ttu-id="cb43e-1716">Cmdleten `Get-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-1716">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="cb43e-1717">Hämta ordning</span><span class="sxs-lookup"><span data-stu-id="cb43e-1717">Get the Order</span></span>
* <span data-ttu-id="cb43e-1718">Cmdleten `New-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-1718">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="cb43e-1719">Skapa ny ordning</span><span class="sxs-lookup"><span data-stu-id="cb43e-1719">Create new Order</span></span>
* <span data-ttu-id="cb43e-1720">Cmdleten `Remove-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-1720">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="cb43e-1721">Ta bort ordning</span><span class="sxs-lookup"><span data-stu-id="cb43e-1721">Remove the Order</span></span>
* <span data-ttu-id="cb43e-1722">Cmdleten `New-AzDataBoxEdgeShare` har ändrats</span><span class="sxs-lookup"><span data-stu-id="cb43e-1722">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="cb43e-1723">Nu skapas lokal filresurs</span><span class="sxs-lookup"><span data-stu-id="cb43e-1723">Now creates Local Share</span></span>
* <span data-ttu-id="cb43e-1724">Cmdleten `Set-AzDataBoxEdgeRole` har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-1724">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="cb43e-1725">Nu kan IotRole mappas till filresursen</span><span class="sxs-lookup"><span data-stu-id="cb43e-1725">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="cb43e-1726">Cmdleten `Invoke-AzDataBoxEdgeDevice` har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-1726">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="cb43e-1727">Anropa genomsökningsuppdatering, ladda ned uppdatering, installera uppdateringar på enheten</span><span class="sxs-lookup"><span data-stu-id="cb43e-1727">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="cb43e-1728">Cmdleten `Get-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-1728">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="cb43e-1729">Hämtar information om utlösare</span><span class="sxs-lookup"><span data-stu-id="cb43e-1729">Gets the information about Triggers</span></span>
* <span data-ttu-id="cb43e-1730">Cmdleten `New-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-1730">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="cb43e-1731">Skapa nya utlösare</span><span class="sxs-lookup"><span data-stu-id="cb43e-1731">Create new Triggers</span></span>
* <span data-ttu-id="cb43e-1732">Cmdleten `Remove-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-1732">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="cb43e-1733">Ta bort utlösare</span><span class="sxs-lookup"><span data-stu-id="cb43e-1733">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cb43e-1734">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cb43e-1734">Az.DataFactory</span></span>
* <span data-ttu-id="cb43e-1735">Uppdatera ADF .Net SDK-versionen till 4.4.0</span><span class="sxs-lookup"><span data-stu-id="cb43e-1735">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="cb43e-1736">Lägg till parametern ExpressCustomSetup för kommandot Set-AzureRmDataFactoryV2IntegrationRuntime för att aktivera installationskonfigurationer och komponenter från tredje part utan anpassat konfigurationsskript.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1736">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cb43e-1737">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cb43e-1737">Az.DataLakeStore</span></span>
* <span data-ttu-id="cb43e-1738">Uppdatera dokumentation för Get-AzDataLakeStoreDeletedItem och Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="cb43e-1738">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="cb43e-1739">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="cb43e-1739">Az.EventHub</span></span>
* <span data-ttu-id="cb43e-1740">Korrigering av problem #10301: Korrigera datumformat för SAS-token</span><span class="sxs-lookup"><span data-stu-id="cb43e-1740">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="cb43e-1741">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="cb43e-1741">Az.FrontDoor</span></span>
* <span data-ttu-id="cb43e-1742">Lägg till parametern MinimumTlsVersion till Enable-AzFrontDoorCustomDomainHttps och New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="cb43e-1742">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="cb43e-1743">Lägg till parametrarna HealthProbeMethod och EnabledState till New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="cb43e-1743">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="cb43e-1744">Lägg till en ny cmdlet för att skapa BackendPoolsSettings-objekt som passar i skapande/uppdatering av Front Door</span><span class="sxs-lookup"><span data-stu-id="cb43e-1744">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="cb43e-1745">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="cb43e-1745">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb43e-1746">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb43e-1746">Az.Network</span></span>
* <span data-ttu-id="cb43e-1747">Ändra alternativexemplen Start-AzVirtualNetworkGatewayConnectionPacketCapture.md och Start-AzVirtualnetworkGatewayPacketCapture.md för FilterData.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1747">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="cb43e-1748">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="cb43e-1748">Az.PrivateDns</span></span>
* <span data-ttu-id="cb43e-1749">Uppdaterade PrivateDns .NET SDK till version 1.0.0</span><span class="sxs-lookup"><span data-stu-id="cb43e-1749">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cb43e-1750">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb43e-1750">Az.RecoveryServices</span></span>
* <span data-ttu-id="cb43e-1751">Stöd för att välja disktyp vid aktivering av skydd i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1751">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="cb43e-1752">Korrigering av bugg för åtgärdsredigering av återställningsplan i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1752">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="cb43e-1753">Återställningsstöd för att godkänna filestream-databaser i Azure Backup SQL.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1753">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="cb43e-1754">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="cb43e-1754">Az.RedisCache</span></span>
* <span data-ttu-id="cb43e-1755">Parametern MinimumTlsVersion har lagts till i cmdletarna New-AzRedisCache och Set-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1755">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="cb43e-1756">Dessutom har MinimumTlsVersion lagts till i utdata för cmdleten Get-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1756">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="cb43e-1757">Verifiering har lagts till på parametern -Size i cmdletarna Set-AzRedisCache och New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="cb43e-1757">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb43e-1758">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb43e-1758">Az.Resources</span></span>
- <span data-ttu-id="cb43e-1759">Uppdaterade policy-cmdletar för att använda den nya API-versionen 2019-06-01 som har en ny EnforcementMode-egenskap i policytilldelningen.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1759">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="cb43e-1760">Uppdaterade hjälpexempel för skapandet av policydefinition</span><span class="sxs-lookup"><span data-stu-id="cb43e-1760">Updated create policy definition help example</span></span>
- <span data-ttu-id="cb43e-1761">Åtgärda bugg i Remove-AZADServicePrincipal -ServicePrincipalName, utlös null-referens när tjänstens huvudnamn inte hittas.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1761">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="cb43e-1762">Åtgärda bugg i New-AZADServicePrincipal, utlös null-referens när klientorganisationen inte har någon prenumeration.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1762">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="cb43e-1763">Ändra New-AzAdServicePrincipal för att endast lägga till autentiseringsuppgifter för det associerade programmet.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1763">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb43e-1764">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb43e-1764">Az.Sql</span></span>
* <span data-ttu-id="cb43e-1765">Stöd har lagts till för databasen ReadReplicaCount.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1765">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="cb43e-1766">Korrigerade Set-AzSqlDatabase när zonredundans inte har angetts</span><span class="sxs-lookup"><span data-stu-id="cb43e-1766">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="cb43e-1767">3.0.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="cb43e-1767">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="cb43e-1768">Allmänt</span><span class="sxs-lookup"><span data-stu-id="cb43e-1768">General</span></span>
* <span data-ttu-id="cb43e-1769">Az. PrivateDns 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="cb43e-1769">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="cb43e-1770">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb43e-1770">Az.Accounts</span></span>
* <span data-ttu-id="cb43e-1771">Lägg till ett utfasningsmeddelande för aliaset Resolve-error.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1771">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="cb43e-1772">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="cb43e-1772">Az.Advisor</span></span>
* <span data-ttu-id="cb43e-1773">Den nya kategorin Operational Excellence har lagts till i cmdleten Get-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1773">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="cb43e-1774">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="cb43e-1774">Az.Batch</span></span>
* <span data-ttu-id="cb43e-1775">`CoreQuota` på `BatchAccountContext` har bytt namn till `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1775">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="cb43e-1776">Det finns även en ny `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1776">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="cb43e-1777">Detta påverkar **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1777">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="cb43e-1778">**New-AzBatchTask** `-ResourceFile`-parametern tar nu en samling `PSResourceFile`-objekt som kan skapas med hjälp av den nya cmdleten **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1778">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="cb43e-1779">Ny **New-AzBatchResourceFile**-cmdlet för att skapa `PSResourceFile`-objekt.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1779">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="cb43e-1780">Dessa kan tillhandahållas till **New-AzBatchTask** på `-ResourceFile`-parametern.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1780">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="cb43e-1781">Detta stöder två nya typer av resursfiler förutom det befintliga sättet med `HttpUrl`:</span><span class="sxs-lookup"><span data-stu-id="cb43e-1781">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="cb43e-1782">`AutoStorageContainerName`-baserade resursfiler laddar ned en hel container för automatisk lagring till Batch-noden.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1782">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="cb43e-1783">`StorageContainerUrl`-baserade resursfiler laddar ned containern som anges i webbadressen till Batch-noden.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1783">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="cb43e-1784">Tog bort egenskapen `ApplicationPackages` för `PSApplication` som returnerades av **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1784">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="cb43e-1785">Specifika paket i ett program kan nu hämtas med hjälp av **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1785">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="cb43e-1786">Till exempel: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1786">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="cb43e-1787">Bytt namn på `ApplicationId` till `ApplicationName` på **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** och **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1787">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="cb43e-1788">`ApplicationId` är nu ett alias för `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1788">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="cb43e-1789">Ny `PSWindowsUserConfiguration`-egenskap till `PSUserAccount` lades till.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1789">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="cb43e-1790">Bytte namn på `Version` till `Name` på `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1790">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="cb43e-1791">Bytte namn på `BlobSource` till `HttpUrl` på `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1791">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="cb43e-1792">Tog bort egenskapen `OSDisk` från `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1792">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="cb43e-1793">Tog bort **Set-AzBatchPoolOSVersion**.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1793">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="cb43e-1794">Den här åtgärden stöds inte längre.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1794">This operation is no longer supported.</span></span>
* <span data-ttu-id="cb43e-1795">`TargetOSVersion` har tagits bort från `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1795">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="cb43e-1796">Bytte namn på `CurrentOSVersion` till `OSVersion` på `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1796">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="cb43e-1797">`DataEgressGiB` och `DataIngressGiB` har tagits bort från `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1797">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="cb43e-1798">Tog bort **Get-AzBatchNodeAgentSku** och ersatte det med **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1798">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="cb43e-1799">**Get-AzBatchSupportedImage** returnerar samma data som **Get-AzBatchNodeAgentSku** men i ett mer användarvänligt format.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1799">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="cb43e-1800">Nya icke-verifierade avbildningar returneras nu också.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1800">New non-verified images are also now returned.</span></span> <span data-ttu-id="cb43e-1801">Ytterligare information om `Capabilities` och `BatchSupportEndOfLife` för varje avbildning inkluderas också.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1801">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="cb43e-1802">Lade till möjlighet att montera fjärrfilsystem på varje nod i en pool via den nya parametern `MountConfiguration` för **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1802">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="cb43e-1803">Har nu stöd för nätverkssäkerhetsregler som blockerar nätverksåtkomst till en pool baserat på källportens trafik.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1803">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="cb43e-1804">Detta görs via egenskapen `SourcePortRanges` på `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1804">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="cb43e-1805">När du kör en container stöder nu Batch körningen av uppgiften i arbetskatalogen för containern eller i arbetskatalogen för Batch-uppgiften.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1805">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="cb43e-1806">Detta styrs av egenskapen `WorkingDirectory` på `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1806">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="cb43e-1807">Lade till en funktion för att ange en samling av offentliga IP-adresser på `PSNetworkConfiguration` via den nya egenskapen `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1807">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="cb43e-1808">Detta garanterar att noderna i poolen har en IP-adress från listan över IP-adresser som tillhandahållits av användare.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1808">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="cb43e-1809">Om inget värde anges är standardvärdet för `WaitForSuccess` på `PSSTartTask` nu `$True` (var tidigare `$False`).</span><span class="sxs-lookup"><span data-stu-id="cb43e-1809">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="cb43e-1810">Om inget värde anges är standardvärdet för `Scope` på `PSAutoUserSpecification` nu `Pool` (var tidigare `Task` på Windows och `Pool` på Linux).</span><span class="sxs-lookup"><span data-stu-id="cb43e-1810">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="cb43e-1811">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="cb43e-1811">Az.Cdn</span></span>
* <span data-ttu-id="cb43e-1812">Introducerade UrlRewriteAction och CacheKeyQueryStringAction till RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1812">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="cb43e-1813">Åtgärdade flera buggar, som saknade indata för ”väljare” i cmdleten New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1813">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb43e-1814">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb43e-1814">Az.Compute</span></span>
* <span data-ttu-id="cb43e-1815">Funktion för diskkrypteringsuppsättning</span><span class="sxs-lookup"><span data-stu-id="cb43e-1815">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="cb43e-1816">Nya cmdletar:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="cb43e-1816">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="cb43e-1817">Parametern DiskEncryptionSetId har lagts till i följande cmdletar:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="cb43e-1817">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="cb43e-1818">Parametrarna DiskEncryptionSetId och EncryptionType har lagts till i följande cmdletar:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="cb43e-1818">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="cb43e-1819">Lägg till parametern PublicIPAddressVersion i New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="cb43e-1819">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="cb43e-1820">Flytta FileUris för anpassat skripttillägg från offentlig inställning till skyddad inställning</span><span class="sxs-lookup"><span data-stu-id="cb43e-1820">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="cb43e-1821">Lägg till ScaleInPolicy i cmdletarna New-AzVmss, New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="cb43e-1821">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="cb43e-1822">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="cb43e-1822">Breaking changes</span></span>
    - <span data-ttu-id="cb43e-1823">Parametern UploadSizeInBytes används istället för DiskSizeGB för New-AzDiskConfig när CreateOption är Uppladdning</span><span class="sxs-lookup"><span data-stu-id="cb43e-1823">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="cb43e-1824">PublishingProfile.Source.ManagedImage.Id ersätts med StorageProfile.Source.Id i objektet GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="cb43e-1824">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cb43e-1825">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cb43e-1825">Az.DataFactory</span></span>
* <span data-ttu-id="cb43e-1826">Uppdatera ADF .Net SDK-versionen till 4.3.0</span><span class="sxs-lookup"><span data-stu-id="cb43e-1826">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cb43e-1827">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cb43e-1827">Az.DataLakeStore</span></span>
* <span data-ttu-id="cb43e-1828">Uppdatera ADLS SDK-version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) innehåller följande korrigeringar</span><span class="sxs-lookup"><span data-stu-id="cb43e-1828">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="cb43e-1829">Undvik att utlösa undantag när det inte går att deserialisera creationtime för inmatning av papperskorg eller katalog.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1829">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="cb43e-1830">Gör inställning tillgänglig per tidsgräns för förfrågan i adlsclient</span><span class="sxs-lookup"><span data-stu-id="cb43e-1830">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="cb43e-1831">Korrigera överföringen av ursprunglig syncflag för badoffset-återställning</span><span class="sxs-lookup"><span data-stu-id="cb43e-1831">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="cb43e-1832">Korrigera EnumerateDirectory för att hämta fortsättningstoken när svar har kontrollerats</span><span class="sxs-lookup"><span data-stu-id="cb43e-1832">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="cb43e-1833">Korrigera bugg i Concat</span><span class="sxs-lookup"><span data-stu-id="cb43e-1833">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="cb43e-1834">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="cb43e-1834">Az.FrontDoor</span></span>
* <span data-ttu-id="cb43e-1835">Åtgärdade diverse stavfel i modul</span><span class="sxs-lookup"><span data-stu-id="cb43e-1835">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="cb43e-1836">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cb43e-1836">Az.HDInsight</span></span>
* <span data-ttu-id="cb43e-1837">Korrigerade buggen att kunder får felet ”inte en giltig Base-64-sträng” vid användning av Get-AzHDInsightCluster för att hämta klustret med ADLSGen1-lagring.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1837">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="cb43e-1838">Lägg till en parameter med namnet ”ApplicationId” i de tre cmdletarna Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig och New-AzHDInsightCluster så att kunden kan tillhandahålla tjänstens huvudnamn för program-ID för åtkomst till Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1838">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="cb43e-1839">Ändrade Microsoft.Azure.Management.HDInsight från 2.1.0 till 5.1.0</span><span class="sxs-lookup"><span data-stu-id="cb43e-1839">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="cb43e-1840">Fem cmdletar har tagits bort:</span><span class="sxs-lookup"><span data-stu-id="cb43e-1840">Removed five cmdlets:</span></span>
    - <span data-ttu-id="cb43e-1841">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="cb43e-1841">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="cb43e-1842">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="cb43e-1842">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="cb43e-1843">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="cb43e-1843">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="cb43e-1844">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="cb43e-1844">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="cb43e-1845">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="cb43e-1845">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="cb43e-1846">Tre cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="cb43e-1846">Added three cmdlets:</span></span>
    - <span data-ttu-id="cb43e-1847">Get-AzHDInsightMonitoring som ersätter Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1847">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="cb43e-1848">Enable-AzHDInsightMonitoring som ersätter Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1848">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="cb43e-1849">Disable-AzHDInsightMonitoring som ersätter Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1849">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="cb43e-1850">Korrigerade cmdleten Get-AzHDInsightProperties för att stödja hämtning av funktionsinformation från en viss plats.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1850">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="cb43e-1851">Parameteruppsättningarna (Spark1 och Spark2) har tagits bort från Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1851">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="cb43e-1852">Lägg till exempel för cmdleten Add-AzHDInsightSecurityProfile till hjälpdokumenten.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1852">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="cb43e-1853">Ändrade utdatatyp för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="cb43e-1853">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="cb43e-1854">Ändrade utdatatyp för Get-AzHDInsightProperties från CapabilitiesResponse till AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1854">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="cb43e-1855">Ändrade utdatatyp för Remove-AzHDInsightCluster från ClusterGetResponse till bool.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1855">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="cb43e-1856">Ändrade utdatatyp för Set-AzHDInsightGatewaySettings HttpConnectivitySettings till GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1856">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="cb43e-1857">Lade till testfall för vissa scenarier.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1857">Added some scenario test cases.</span></span>
* <span data-ttu-id="cb43e-1858">Ta bort vissa alias: Add-AzHDInsightConfigValues, Get-AzHDInsightProperties.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1858">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cb43e-1859">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cb43e-1859">Az.IotHub</span></span>
* <span data-ttu-id="cb43e-1860">Icke-bakåtkompatibla ändringar:</span><span class="sxs-lookup"><span data-stu-id="cb43e-1860">Breaking changes:</span></span>
    - <span data-ttu-id="cb43e-1861">Cmdleten Add-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1861">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="cb43e-1862">Parameteruppsättningen __AllParameterSets för cmdleten Add-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1862">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="cb43e-1863">Cmdleten Get-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1863">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="cb43e-1864">Parameteruppsättningen __AllParameterSets för cmdleten Get-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1864">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="cb43e-1865">Egenskapen OperationsMonitoringProperties av typen Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1865">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="cb43e-1866">Egenskapen OperationsMonitoringProperties av typen Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1866">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="cb43e-1867">Cmdleten New-AzIotHubExportDevice stöder inte längre aliaset New-AzIotHubExportDevices.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1867">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="cb43e-1868">Cmdleten New-AzIotHubImportDevice stöder inte längre aliaset New-AzIotHubImportDevices.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1868">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="cb43e-1869">Cmdleten Remove-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1869">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="cb43e-1870">Parameteruppsättningen __AllParameterSets för cmdleten Remove-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1870">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="cb43e-1871">Cmdleten Set-AzIotHub har inte längre stöd för parametern OperationsMonitoringProperties och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1871">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="cb43e-1872">Parameteruppsättningen UpdateOperationsMonitoringProperties för cmdleten Set-AzIotHub har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1872">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cb43e-1873">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb43e-1873">Az.RecoveryServices</span></span>
* <span data-ttu-id="cb43e-1874">Azure Site Recovery-stöd för att konfigurera nätverksresurser som NSG, offentliga IP-adresser och interna lastbalanserare för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1874">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="cb43e-1875">Azure Site Recovery-stöd för att skriva till hanterad disk för vMWare till Azure.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1875">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="cb43e-1876">Azure Site Recovery-stöd för NIC-reduktion för vMWare till Azure.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1876">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="cb43e-1877">Azure Site Recovery-stöd för accelererat nätverk för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1877">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="cb43e-1878">Azure Site Recovery-stöd för automatisk uppdatering av agent för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1878">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="cb43e-1879">Azure Site Recovery-stöd för Standard SSD för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1879">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="cb43e-1880">Azure Site Recovery-stöd för tvåstegskryptering i Azure Disk Encryption för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1880">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="cb43e-1881">Azure Site Recovery-stöd för att skydda nyligen tillagda diskar för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1881">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="cb43e-1882">En funktion för mjuk borttagning av virtuella datorer samt tester för mjuk borttagning har tagits bort</span><span class="sxs-lookup"><span data-stu-id="cb43e-1882">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb43e-1883">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb43e-1883">Az.Resources</span></span>
* <span data-ttu-id="cb43e-1884">Uppdatera beroendesammansättning för Microsoft.Extensions.Caching.Memory från 1.1.1 till 2.2</span><span class="sxs-lookup"><span data-stu-id="cb43e-1884">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb43e-1885">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb43e-1885">Az.Network</span></span>
* <span data-ttu-id="cb43e-1886">Ändra alla cmdletar för PrivateEndpointConnection så att de stöder generiska tjänstleverantörer.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1886">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="cb43e-1887">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="cb43e-1887">Updated cmdlet:</span></span>
        - <span data-ttu-id="cb43e-1888">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="cb43e-1888">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="cb43e-1889">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="cb43e-1889">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="cb43e-1890">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="cb43e-1890">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="cb43e-1891">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="cb43e-1891">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="cb43e-1892">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="cb43e-1892">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="cb43e-1893">Lägg till ny cmdlet för PrivateLinkResource så att det också stöder generiska tjänstleverantörer.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1893">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="cb43e-1894">Ny cmdlet:</span><span class="sxs-lookup"><span data-stu-id="cb43e-1894">New cmdlet:</span></span>
        - <span data-ttu-id="cb43e-1895">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="cb43e-1895">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="cb43e-1896">Lägg till nya fält och parametrar för funktionen Proxy Protocol V2.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1896">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="cb43e-1897">Lägg till egenskapen EnableProxyProtocol i PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="cb43e-1897">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="cb43e-1898">Lägg till egenskapen LinkIdentifier i PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="cb43e-1898">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="cb43e-1899">Uppdaterade New-AzPrivateLinkService för att lägga till den nya valfria parametern EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1899">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="cb43e-1900">Korrigera felaktig beskrivning av parameter i referensdokumentationen för New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="cb43e-1900">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="cb43e-1901">Nya cmdletar som stöder Azure-brandväggsprincipen</span><span class="sxs-lookup"><span data-stu-id="cb43e-1901">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="cb43e-1902">Lägg till stöd för den underordnade resursen RouteTables för VirtualHub</span><span class="sxs-lookup"><span data-stu-id="cb43e-1902">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="cb43e-1903">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="cb43e-1903">New cmdlets added:</span></span>
        - <span data-ttu-id="cb43e-1904">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="cb43e-1904">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="cb43e-1905">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="cb43e-1905">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="cb43e-1906">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="cb43e-1906">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="cb43e-1907">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="cb43e-1907">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="cb43e-1908">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="cb43e-1908">Set-AzVirtualHub</span></span>
* <span data-ttu-id="cb43e-1909">Lägg till stöd för ny egenskaps-SKU för VirtualHub och VirtualWANType för VirtualWan</span><span class="sxs-lookup"><span data-stu-id="cb43e-1909">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="cb43e-1910">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="cb43e-1910">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="cb43e-1911">New-AzVirtualHub: lade till parameter-SKU</span><span class="sxs-lookup"><span data-stu-id="cb43e-1911">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="cb43e-1912">Update-AzVirtualHub: lade till parameter-SKU</span><span class="sxs-lookup"><span data-stu-id="cb43e-1912">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="cb43e-1913">New-AzVirtualWan: lade till parametern VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="cb43e-1913">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="cb43e-1914">Update-AzVirtualWan: lade till parametern VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="cb43e-1914">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="cb43e-1915">Lägg till stöd för egenskapen EnableInternetSecurity för HubVnetConnection, VpnConnection och ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="cb43e-1915">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="cb43e-1916">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="cb43e-1916">New cmdlets added:</span></span>
        - <span data-ttu-id="cb43e-1917">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="cb43e-1917">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="cb43e-1918">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="cb43e-1918">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="cb43e-1919">New-AzureRmVirtualHubVnetConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-1919">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="cb43e-1920">New-AzureRmVpnConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-1920">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="cb43e-1921">Update-AzureRmVpnConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-1921">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="cb43e-1922">New-AzureRmExpressRouteConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-1922">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="cb43e-1923">Set-AzureRmExpressRouteConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-1923">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="cb43e-1924">Lägg till stöd för att konfigurera TopLevel WebApplicationFirewall-princip</span><span class="sxs-lookup"><span data-stu-id="cb43e-1924">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="cb43e-1925">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="cb43e-1925">New cmdlets added:</span></span>
        - <span data-ttu-id="cb43e-1926">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="cb43e-1926">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="cb43e-1927">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="cb43e-1927">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="cb43e-1928">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="cb43e-1928">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="cb43e-1929">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="cb43e-1929">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="cb43e-1930">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="cb43e-1930">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="cb43e-1931">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="cb43e-1931">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="cb43e-1932">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="cb43e-1932">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="cb43e-1933">New-AzApplicationGatewayFirewallPolicy: parametrarna PolicySetting, ManagedRule har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-1933">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="cb43e-1934">Stöd för operator för geomatchning har lagts till på CustomRule</span><span class="sxs-lookup"><span data-stu-id="cb43e-1934">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="cb43e-1935">Geomatchning har lagts till i operatorn på FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="cb43e-1935">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="cb43e-1936">Stöd har lagts till för brandväggsprinciperna perListener och perSite</span><span class="sxs-lookup"><span data-stu-id="cb43e-1936">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="cb43e-1937">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="cb43e-1937">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="cb43e-1938">New-AzApplicationGatewayHttpListener: parametrarna FirewallPolicy, FirewallPolicyId har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-1938">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="cb43e-1939">New-AzApplicationGatewayPathRuleConfig: parametrarna FirewallPolicy, FirewallPolicyId har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-1939">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="cb43e-1940">Åtgärdat så att nödvändigt undernät med namnet AzureBastionSubnet i PSBastion kan vara skiftlägesokänsligt</span><span class="sxs-lookup"><span data-stu-id="cb43e-1940">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="cb43e-1941">Stöd för mål-FQDN:er i nätverksregler och översatt FQDN i NAT-regler för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="cb43e-1941">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="cb43e-1942">Lägg till stöd för resursen RouteTables för IpGroup på den högsta nivån</span><span class="sxs-lookup"><span data-stu-id="cb43e-1942">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="cb43e-1943">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="cb43e-1943">New cmdlets added:</span></span>
        - <span data-ttu-id="cb43e-1944">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="cb43e-1944">New-AzIpGroup</span></span>
        - <span data-ttu-id="cb43e-1945">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="cb43e-1945">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="cb43e-1946">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="cb43e-1946">Get-AzIpGroup</span></span>
        - <span data-ttu-id="cb43e-1947">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="cb43e-1947">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="cb43e-1948">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cb43e-1948">Az.ServiceFabric</span></span>
* <span data-ttu-id="cb43e-1949">Ta bort cmdleten Add-AzServiceFabricApplicationCertificate eftersom det här scenariot omfattas av Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1949">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb43e-1950">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb43e-1950">Az.Sql</span></span>
* <span data-ttu-id="cb43e-1951">Stöd har lagts till för återställning av utelämnade databaser på hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1951">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="cb43e-1952">Inaktuella gamla cmdletar för granskning från kod.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1952">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="cb43e-1953">Tog bort inaktuella alias:</span><span class="sxs-lookup"><span data-stu-id="cb43e-1953">Removed deprecated aliases:</span></span>
* <span data-ttu-id="cb43e-1954">Get-AzSqlDatabaseIndexRecommendations (använd Get-AzSqlDatabaseIndexRecommendation istället)</span><span class="sxs-lookup"><span data-stu-id="cb43e-1954">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="cb43e-1955">Get-AzSqlDatabaseRestorePoints (använd Get-AzSqlDatabaseRestorePoint istället)</span><span class="sxs-lookup"><span data-stu-id="cb43e-1955">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="cb43e-1956">Ta bort cmdleten Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="cb43e-1956">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="cb43e-1957">Ta bort alias för inaktuella cmdletar för inställningar för utvärdering av säkerhetsrisk</span><span class="sxs-lookup"><span data-stu-id="cb43e-1957">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="cb43e-1958">Inaktualisera cmdletar för inställningar för avancerad hotidentifiering</span><span class="sxs-lookup"><span data-stu-id="cb43e-1958">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="cb43e-1959">Lägga till cmdletar för att inaktivera och aktivera känslighetsrekommendationer på kolumner i en databas.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1959">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cb43e-1960">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb43e-1960">Az.Storage</span></span>
* <span data-ttu-id="cb43e-1961">Stöd för att aktivera stora filresurser vid skapande eller uppdatering av lagringskonto</span><span class="sxs-lookup"><span data-stu-id="cb43e-1961">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="cb43e-1962">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cb43e-1962">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="cb43e-1963">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cb43e-1963">Set-AzStorageAccount</span></span>
* <span data-ttu-id="cb43e-1964">När du stänger/hämtar en filreferens kan du hoppa över kontrollen av huruvida indatasökvägen är en filkatalog eller en fil för att undvika problem med objekt som har status DeletePending</span><span class="sxs-lookup"><span data-stu-id="cb43e-1964">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="cb43e-1965">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="cb43e-1965">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="cb43e-1966">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="cb43e-1966">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="cb43e-1967">2.8.0 – oktober 2019</span><span class="sxs-lookup"><span data-stu-id="cb43e-1967">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="cb43e-1968">Allmänt</span><span class="sxs-lookup"><span data-stu-id="cb43e-1968">General</span></span>
* <span data-ttu-id="cb43e-1969">AZ. HealthcareApis 1.0.0-version</span><span class="sxs-lookup"><span data-stu-id="cb43e-1969">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="cb43e-1970">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb43e-1970">Az.Accounts</span></span>
* <span data-ttu-id="cb43e-1971">Uppdatera telemetri och URL-omskrivning för genererade moduler, korrigera Windows-enhetstester.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1971">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="cb43e-1972">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cb43e-1972">Az.ApiManagement</span></span>
* <span data-ttu-id="cb43e-1973">**Set-AzApiManagementApi** – Tillagt stöd för att uppdatera Api till ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="cb43e-1973">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="cb43e-1974">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="cb43e-1974">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cb43e-1975">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cb43e-1975">Az.Automation</span></span>
* <span data-ttu-id="cb43e-1976">Åtgärdade cmdleten New-AzureAutomationSoftwareUpdateConfiguration för parametern för inställning av Linux-omstart.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1976">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="cb43e-1977">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="cb43e-1977">Az.Batch</span></span>
* <span data-ttu-id="cb43e-1978">**Get-AzBatchNodeAgentSku** är inaktuell och ersätts av **Get-AzBatchSupportImage** i version 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1978">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb43e-1979">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb43e-1979">Az.Compute</span></span>
* <span data-ttu-id="cb43e-1980">Lägg till parametrarna Priority, EvictionPolicy och MaxPrice till cmdletarna New-AzVM och New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="cb43e-1980">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="cb43e-1981">Korrigera varningsmeddelande och hjälpdokument för cmdletarna Add-AzVMAdditionalUnattendContent och Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="cb43e-1981">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="cb43e-1982">Åtgärda – skipVmBackup-undantag för virtuella Linux-datorer med hanterade diskar för Set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1982">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="cb43e-1983">Åtgärda fel i uppdatera krypteringsinställningarna i set-AzVMDiskEncryptionExtension, scenario i två steg.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1983">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cb43e-1984">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cb43e-1984">Az.DataFactory</span></span>
* <span data-ttu-id="cb43e-1985">Lägga till CRUD-kommandon för ADF V2-dataflödet: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow och Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1985">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="cb43e-1986">Lägger till åtgärdskommandon för ADF V2-dataflödesfelsökningssession: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand och Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1986">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="cb43e-1987">Uppdatera ADF .Net SDK-versionen till 4.2.0</span><span class="sxs-lookup"><span data-stu-id="cb43e-1987">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cb43e-1988">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cb43e-1988">Az.DataLakeStore</span></span>
* <span data-ttu-id="cb43e-1989">Korrigera kontovalidering så att konton med ”-” kan skickas utan domän</span><span class="sxs-lookup"><span data-stu-id="cb43e-1989">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="cb43e-1990">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="cb43e-1990">Az.HealthcareApis</span></span>
* <span data-ttu-id="cb43e-1991">PowerShell-versionen har uppdaterats till 1.0.0</span><span class="sxs-lookup"><span data-stu-id="cb43e-1991">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="cb43e-1992">Uppdaterade SDK-versionen till 1.0.2</span><span class="sxs-lookup"><span data-stu-id="cb43e-1992">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="cb43e-1993">Uppdatera i tester för att referera till en ny SDK-version</span><span class="sxs-lookup"><span data-stu-id="cb43e-1993">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="cb43e-1994">Utdatastrukturen har uppdaterats från kapslad till förenklad.</span><span class="sxs-lookup"><span data-stu-id="cb43e-1994">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cb43e-1995">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cb43e-1995">Az.IotHub</span></span>
* <span data-ttu-id="cb43e-1996">Lägg till ny routningskälla: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="cb43e-1996">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="cb43e-1997">Mindre felkorrigering: Get-AzIothub returnerar inte subscriptionId</span><span class="sxs-lookup"><span data-stu-id="cb43e-1997">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cb43e-1998">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cb43e-1998">Az.Monitor</span></span>
* <span data-ttu-id="cb43e-1999">Nya åtgärdsgruppsmottagare har lagts till för åtgärdsgrupp   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="cb43e-1999">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="cb43e-2000">Använd vanligt aviseringsschema som är aktiverat för mottagarna.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2000">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="cb43e-2001">Detta gäller inte för SMS, push för Azure-app, ITSM och röstmottagare</span><span class="sxs-lookup"><span data-stu-id="cb43e-2001">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="cb43e-2002">Webhooks har nu stöd för Azure Active Directory-autentisering.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2002">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb43e-2003">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb43e-2003">Az.Network</span></span>
* <span data-ttu-id="cb43e-2004">Lägg till ny cmdlet Get-AzAvailableServiceAlias som kan anropas för att hämta de alias som kan användas för tjänstslutpunktsprinciper.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2004">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="cb43e-2005">Stöd för tillägg av trafikväljare har lagts till i gatewayanslutningar för virtuella nätverk</span><span class="sxs-lookup"><span data-stu-id="cb43e-2005">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="cb43e-2006">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="cb43e-2006">New cmdlets added:</span></span>
        - <span data-ttu-id="cb43e-2007">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="cb43e-2007">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="cb43e-2008">Cmdletar har uppdaterats med valfri parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="cb43e-2008">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="cb43e-2009">Lägg till stöd för ESP- och AH-protokoll i konfiguration av nätverkssäkerhetsregler</span><span class="sxs-lookup"><span data-stu-id="cb43e-2009">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="cb43e-2010">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="cb43e-2010">Updated cmdlets:</span></span>
        - <span data-ttu-id="cb43e-2011">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cb43e-2011">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="cb43e-2012">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cb43e-2012">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="cb43e-2013">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cb43e-2013">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="cb43e-2014">Förbättra hanteringen av undantag i Cortex-cmdletar</span><span class="sxs-lookup"><span data-stu-id="cb43e-2014">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="cb43e-2015">Nya generationer och SKU:er för VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="cb43e-2015">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="cb43e-2016">Introducera nya generationer för VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2016">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="cb43e-2017">Introducera nya SKU:er med högt dataflöde för VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2017">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="cb43e-2018">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="cb43e-2018">Az.RedisCache</span></span>
* <span data-ttu-id="cb43e-2019">Uppdaterad referensdokumentation för ”set-AzRedisCache” för att inkludera saknade värden för parametern ”size”</span><span class="sxs-lookup"><span data-stu-id="cb43e-2019">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb43e-2020">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb43e-2020">Az.Sql</span></span>
* <span data-ttu-id="cb43e-2021">Lägg till stöd för inställningen Active Directory administratör på den hanterade instansen</span><span class="sxs-lookup"><span data-stu-id="cb43e-2021">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cb43e-2022">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb43e-2022">Az.Storage</span></span>
* <span data-ttu-id="cb43e-2023">Uppdatera Lagringsklientbibliotek till 11.1.0</span><span class="sxs-lookup"><span data-stu-id="cb43e-2023">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="cb43e-2024">Lista containrar med hanteringsplans-API, kommer att listas med NextPageLink</span><span class="sxs-lookup"><span data-stu-id="cb43e-2024">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="cb43e-2025">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="cb43e-2025">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="cb43e-2026">Lista lagringskonton från prenumerationen, kommer att listas med NextPageLink</span><span class="sxs-lookup"><span data-stu-id="cb43e-2026">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="cb43e-2027">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cb43e-2027">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="cb43e-2028">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="cb43e-2028">Az.StorageSync</span></span>
* <span data-ttu-id="cb43e-2029">Åtgärda problemet 9810 i Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2029">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cb43e-2030">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb43e-2030">Az.Websites</span></span>
* <span data-ttu-id="cb43e-2031">Set-AzWebApp – uppdatering av ASP för en app misslyckades</span><span class="sxs-lookup"><span data-stu-id="cb43e-2031">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="cb43e-2032">2.7.0 – september 2019</span><span class="sxs-lookup"><span data-stu-id="cb43e-2032">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="cb43e-2033">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cb43e-2033">Az.ApiManagement</span></span>
* <span data-ttu-id="cb43e-2034">Uppdatera ”-Format”-parameterbeskrivningen i ”Set-AzApiManagementPolicy”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="cb43e-2034">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="cb43e-2035">Referenser för den föråldrade cmdleten ”Update-AzApiManagementDeployment” har tagits bort från referensdokumentationen.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2035">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="cb43e-2036">Använd ”Set-AzApiManagement” i stället.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2036">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cb43e-2037">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cb43e-2037">Az.Automation</span></span>
* <span data-ttu-id="cb43e-2038">Stavfel har korrigerats i exempel i referensdokumentationen för ”Register-AzAutomationDscNode”</span><span class="sxs-lookup"><span data-stu-id="cb43e-2038">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="cb43e-2039">Klargörande har lagts till om OS-begränsningar för Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="cb43e-2039">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="cb43e-2040">Null-referensundantag har korrigerats för -Wait-alternativet i Start-AzAutomationRunbook-cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2040">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb43e-2041">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb43e-2041">Az.Compute</span></span>
* <span data-ttu-id="cb43e-2042">Lägg till UploadSizeInBytes-parameter till New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="cb43e-2042">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="cb43e-2043">Lägg till Incremental-parameter till New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="cb43e-2043">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="cb43e-2044">Lägg till en funktion för virtuella datorer med låg prioritet:</span><span class="sxs-lookup"><span data-stu-id="cb43e-2044">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="cb43e-2045">MaxPrice-, EvictionPolicy- och Priority-parametrar har lagts till i New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2045">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="cb43e-2046">MaxPrice-parametern har lagts till i New-AzVmssConfig-, Update-AzVM- och Update-AzVmss-cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2046">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="cb43e-2047">Åtgärda problem med VM-referenser för Get-AzAvailabilitySet-cmdleten när alla tillgänglighetsuppsättningar i prenumerationen visas.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2047">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="cb43e-2048">Korrigera null-undantaget för Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2048">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="cb43e-2049">Korrigera VHD-metoden för sökning relativt till slut.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2049">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="cb43e-2050">Åtgärda UltraSSD-problem för New-AzVM och Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2050">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cb43e-2051">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cb43e-2051">Az.DataFactory</span></span>
* <span data-ttu-id="cb43e-2052">Lägger till 3 nya kommandon för ADF V2 – Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription och Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="cb43e-2052">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="cb43e-2053">ADF .Net SDK har uppdaterats till 4.1.3</span><span class="sxs-lookup"><span data-stu-id="cb43e-2053">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="cb43e-2054">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cb43e-2054">Az.HDInsight</span></span>
* <span data-ttu-id="cb43e-2055">Anrop för icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="cb43e-2055">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cb43e-2056">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cb43e-2056">Az.IotHub</span></span>
* <span data-ttu-id="cb43e-2057">Lägg till stöd för att anropa redundans för en IotHub till den geo-länkade katastrofåterställningsregionen.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2057">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="cb43e-2058">Lägg till stöd för att hantera meddelandeberikning för en IotHub.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2058">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="cb43e-2059">Nya cmdlet:ar är:</span><span class="sxs-lookup"><span data-stu-id="cb43e-2059">New cmdlets are:</span></span>
    - <span data-ttu-id="cb43e-2060">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="cb43e-2060">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="cb43e-2061">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="cb43e-2061">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="cb43e-2062">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="cb43e-2062">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="cb43e-2063">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="cb43e-2063">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cb43e-2064">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cb43e-2064">Az.Monitor</span></span>
* <span data-ttu-id="cb43e-2065">Pekar på den senaste Monitor SDK:n, dvs. 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="cb43e-2065">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="cb43e-2066">Lägger till bakåtkompatibla ändringar i Metrics-cmdletarna, dvs. enhetsuppräkningen stöder flera nya värden.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2066">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="cb43e-2067">Detta är skrivskyddade cmdletar, så det förekommer inga ändringar i inmatningen för cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2067">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="cb43e-2068">API-versionen för **ActionGroups**-begäranden är nu **2019-06-01**. Tidigare var den **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2068">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="cb43e-2069">Test av scenarier har uppdaterats för att anpassas till den här ändringen.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2069">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="cb43e-2070">Ett nytt obligatoriskt argument har lagts till för konstruktorerna för klasserna **EmailReceiver** och **WebhookReceiver** – ett booleskt värde med namnet **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2070">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="cb43e-2071">Värdet är för närvarande fast till **false** så att den här icke-bakåtkompatibla ändringen är dold från cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2071">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="cb43e-2072">**Obs!** Det här är en tillfällig ändring som måste verifieras av Alerts-teamet.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2072">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="cb43e-2073">Ordningen på argumenten för konstruktorn för klassen **Source** (relaterad till klassen **ScheduledQueryRuleSource**) har ändrats från den tidigare SDK:n.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2073">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="cb43e-2074">Den här ändringen krävde korrigering av två enhetstest: de kompilerades, men testerna skickades inte.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2074">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="cb43e-2075">Ordningen på argumenten för konstruktorn för klassen **AlertingAction** (relaterad till klassen **ScheduledQueryRuleSource**) har ändrats från den tidigare SDK:n.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2075">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="cb43e-2076">Den här ändringen krävde korrigering av två enhetstest: de kompilerades, men testerna skickades inte.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2076">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="cb43e-2077">Stöd för kriterier för dynamiskt tröskelvärde för måttavisering v2</span><span class="sxs-lookup"><span data-stu-id="cb43e-2077">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="cb43e-2078">New-AzMetricAlertRuleV2Criteria: skapar nu även kriterier för dynamiskt tröskelvärde</span><span class="sxs-lookup"><span data-stu-id="cb43e-2078">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="cb43e-2079">Add-AzMetricAlertRuleV2: accepterar nu även kriterier för dynamiskt tröskelvärde</span><span class="sxs-lookup"><span data-stu-id="cb43e-2079">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="cb43e-2080">Förbättringar i schemalagd frågeregel (SQR)</span><span class="sxs-lookup"><span data-stu-id="cb43e-2080">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="cb43e-2081">Cmdletar accepterar ”Location”-parameter i båda formaten, antingen platsen (t.ex. eastus) eller platsens visningsnamn (t.ex. USA, östra)</span><span class="sxs-lookup"><span data-stu-id="cb43e-2081">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="cb43e-2082">”Enabled”-parametern illustreras korrekt i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="cb43e-2082">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="cb43e-2083">Exempel för den valfria parametern ”ActionGroup” har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-2083">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="cb43e-2084">Förbättrade hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="cb43e-2084">Overall improved help files</span></span>
* <span data-ttu-id="cb43e-2085">Åtgärda bugg då omfattningstypen fastställs för ”Set-AzActionRule”</span><span class="sxs-lookup"><span data-stu-id="cb43e-2085">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb43e-2086">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb43e-2086">Az.Network</span></span>
* <span data-ttu-id="cb43e-2087">Korrigera felaktigt exempel i referensdokumentationen för ”New-AzApplicationGateway”</span><span class="sxs-lookup"><span data-stu-id="cb43e-2087">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="cb43e-2088">Lägg till anmärkning i ”Get-AzNetworkWatcherPacketCapture”-referensdokumentationen om hämtning av alla egenskaper för en paketinsamling</span><span class="sxs-lookup"><span data-stu-id="cb43e-2088">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="cb43e-2089">Exempel har korrigerats i ”Test-AzNetworkWatcherIPFlow”-referensdokumentationen för korrekt uppräkning av nätverkskort</span><span class="sxs-lookup"><span data-stu-id="cb43e-2089">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="cb43e-2090">Förbättrad tolkning av molnundantag för att visa eventuell ytterligare information</span><span class="sxs-lookup"><span data-stu-id="cb43e-2090">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="cb43e-2091">Förbättrad tolkning av molnundantag för att hantera ytterligare en typ av SDK-undantag</span><span class="sxs-lookup"><span data-stu-id="cb43e-2091">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="cb43e-2092">Felaktig mappning av säkerhetsregelmodeller har korrigerats</span><span class="sxs-lookup"><span data-stu-id="cb43e-2092">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="cb43e-2093">Egenskaper har lagts till för nätverksgränssnittet för funktionen Privat IP</span><span class="sxs-lookup"><span data-stu-id="cb43e-2093">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="cb43e-2094">Egenskapen ”PrivateEndpoint” har lagts till som en typ av PSResourceId till PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="cb43e-2094">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="cb43e-2095">Egenskapen ”PrivateLinkConnectionProperties” har lagts till som en typ av PSIpConfigurationConnectivityInformation till PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb43e-2095">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="cb43e-2096">Modellklassen PSIpConfigurationConnectivityInformation har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-2096">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="cb43e-2097">ApplicationRuleProtocolType ”mssql” har lagts till för Azure Firewall-resurs</span><span class="sxs-lookup"><span data-stu-id="cb43e-2097">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="cb43e-2098">MultiLink-stöd i virtuellt WAN</span><span class="sxs-lookup"><span data-stu-id="cb43e-2098">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="cb43e-2099">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="cb43e-2099">New cmdlets</span></span>
        - <span data-ttu-id="cb43e-2100">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="cb43e-2100">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="cb43e-2101">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="cb43e-2101">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="cb43e-2102">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="cb43e-2102">Updated cmdlet:</span></span>
        - <span data-ttu-id="cb43e-2103">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="cb43e-2103">New-VpnSite</span></span>
        - <span data-ttu-id="cb43e-2104">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="cb43e-2104">Update-VpnSite</span></span>
        - <span data-ttu-id="cb43e-2105">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="cb43e-2105">New-VpnConnection</span></span>
        - <span data-ttu-id="cb43e-2106">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="cb43e-2106">Update-VpnConnection</span></span>
* <span data-ttu-id="cb43e-2107">Dokument för vissa PowerShell-exempel har korrigerats så att Az-cmdletar används i stället för AzureRM-cmdletar</span><span class="sxs-lookup"><span data-stu-id="cb43e-2107">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cb43e-2108">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb43e-2108">Az.RecoveryServices</span></span>
* <span data-ttu-id="cb43e-2109">Uppdatera AzureVMpolicy-objekt med ProtectedItemsCount-attribut</span><span class="sxs-lookup"><span data-stu-id="cb43e-2109">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="cb43e-2110">Ytterligare tester har lagts till för VM-princip och återställning av ursprungligt lagringskonto</span><span class="sxs-lookup"><span data-stu-id="cb43e-2110">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb43e-2111">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb43e-2111">Az.Resources</span></span>
* <span data-ttu-id="cb43e-2112">Åtgärda fel där det inte gick att anropa New-AzRoleAssignment utan parametern Scope.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2112">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="cb43e-2113">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cb43e-2113">Az.ServiceFabric</span></span>
* <span data-ttu-id="cb43e-2114">Stavfel har korrigerats i exempel för ”Update-AzServiceFabricReliability”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="cb43e-2114">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="cb43e-2115">Lägger till nya cmdletar för att hantera program och tjänster:</span><span class="sxs-lookup"><span data-stu-id="cb43e-2115">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="cb43e-2116">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="cb43e-2116">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="cb43e-2117">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="cb43e-2117">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="cb43e-2118">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="cb43e-2118">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="cb43e-2119">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="cb43e-2119">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="cb43e-2120">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="cb43e-2120">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="cb43e-2121">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="cb43e-2121">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="cb43e-2122">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="cb43e-2122">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="cb43e-2123">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="cb43e-2123">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="cb43e-2124">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="cb43e-2124">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="cb43e-2125">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="cb43e-2125">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="cb43e-2126">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="cb43e-2126">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="cb43e-2127">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="cb43e-2127">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="cb43e-2128">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="cb43e-2128">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="cb43e-2129">Service Fabric SDK har uppgraderats till version 1.2.0 som använder Service Fabric-resursprovidern med API-version 2019-03-01.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2129">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="cb43e-2130">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="cb43e-2130">Az.SignalR</span></span>
* <span data-ttu-id="cb43e-2131">Lägg till Update-, Restart-, CheckNameAvailability- och GetUsage-cmdletar</span><span class="sxs-lookup"><span data-stu-id="cb43e-2131">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb43e-2132">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb43e-2132">Az.Sql</span></span>
* <span data-ttu-id="cb43e-2133">Uppdatera exempel i referensdokumentationen för ”Get-AzSqlElasticPool”</span><span class="sxs-lookup"><span data-stu-id="cb43e-2133">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="cb43e-2134">vCore-exempel för att skapa en elastisk pool (New-AzSqlElasticPool) har lagts till.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2134">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="cb43e-2135">Ta bort verifieringen av EmailAddresses och kontrollen som bekräftar att EmailAdmins inte är falskt när EmailAddresses är tomt i Set-AzSqlServerAdvancedThreatProtectionPolicy och Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="cb43e-2135">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="cb43e-2136">Server-/databasgranskningsinställningar kan tas bort när det finns flera diagnostikinställningar som aktiverar granskningskategorin.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2136">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="cb43e-2137">Åtgärda verifiering av e-postadresser i flera Sql Vulnerability Assessment-cmdletar (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting och Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="cb43e-2137">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cb43e-2138">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb43e-2138">Az.Storage</span></span>
* <span data-ttu-id="cb43e-2139">Exempel i referensdokumentationen för ”Get-AzStorageAccountKey” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="cb43e-2139">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="cb43e-2140">Vid upp- och nedladdning av en Azure-fil kan SMB-egenskaperna för källfilen (t.ex. filattribut, tidpunkten då filen skapades och tidpunkten för den senaste skrivningen) sparas i målfilen</span><span class="sxs-lookup"><span data-stu-id="cb43e-2140">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="cb43e-2141">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="cb43e-2141">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="cb43e-2142">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="cb43e-2142">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="cb43e-2143">Korrigera problem med uppladdningen av blockblob med egenskaper/metadata för ImmutabilityPolicy i containrar.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2143">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="cb43e-2144">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="cb43e-2144">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="cb43e-2145">Stöd för hantering av Azure-filresurser med API för hanteringsplan</span><span class="sxs-lookup"><span data-stu-id="cb43e-2145">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="cb43e-2146">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="cb43e-2146">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="cb43e-2147">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="cb43e-2147">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="cb43e-2148">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="cb43e-2148">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="cb43e-2149">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="cb43e-2149">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cb43e-2150">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb43e-2150">Az.Websites</span></span>
* <span data-ttu-id="cb43e-2151">Åtgärdar problemet där webapp-taggar togs bort när appen migrerades till nya ASP</span><span class="sxs-lookup"><span data-stu-id="cb43e-2151">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="cb43e-2152">Åtgärda Publish-AzureWebapp så att det fungerar i Linux och Windows</span><span class="sxs-lookup"><span data-stu-id="cb43e-2152">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="cb43e-2153">Uppdatera exempel i ”Get-AzWebAppPublishingProfile”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="cb43e-2153">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="cb43e-2154">2.6.0 – augusti 2019</span><span class="sxs-lookup"><span data-stu-id="cb43e-2154">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="cb43e-2155">Allmänt</span><span class="sxs-lookup"><span data-stu-id="cb43e-2155">General</span></span>
* <span data-ttu-id="cb43e-2156">Åtgärdade diverse skrivfel i flera moduler</span><span class="sxs-lookup"><span data-stu-id="cb43e-2156">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="cb43e-2157">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb43e-2157">Az.Accounts</span></span>
* <span data-ttu-id="cb43e-2158">Stöd för användartilldelat MSI i Azure Functions-autentisering (#9479)</span><span class="sxs-lookup"><span data-stu-id="cb43e-2158">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="cb43e-2159">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="cb43e-2159">Az.Aks</span></span>
* <span data-ttu-id="cb43e-2160">Åtgärda problem med utdata för "Get-AzAks"</span><span class="sxs-lookup"><span data-stu-id="cb43e-2160">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="cb43e-2161">Mer information här: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="cb43e-2161">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="cb43e-2162">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cb43e-2162">Az.ApiManagement</span></span>
* <span data-ttu-id="cb43e-2163">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="cb43e-2163">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="cb43e-2164">Uppdatera .net-NuGet-versionen, som inte tillämpar begränsningar för productId, apiId och userId</span><span class="sxs-lookup"><span data-stu-id="cb43e-2164">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="cb43e-2165">**Get-AzApiManagementProduct** – Lade till stöd för frågekörning mot produkter via API.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2165">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="cb43e-2166">**New-AzApiManagementApiRevision** – Korrigering för problem där ApiRevisionDescription inte angavs vid skapande av ny API-revision https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="cb43e-2166">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="cb43e-2167">Åtgärdade skrivfel i modellen "PsApiManagementOAuth2AuthrozationServer" till "PsApiManagementOAuth2AuthorizationServer"</span><span class="sxs-lookup"><span data-stu-id="cb43e-2167">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="cb43e-2168">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="cb43e-2168">Az.Batch</span></span>
* <span data-ttu-id="cb43e-2169">Åtgärdade skrivfel i hjälpmeddelande och dokumentation till att skriva Windows med versaler</span><span class="sxs-lookup"><span data-stu-id="cb43e-2169">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="cb43e-2170">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="cb43e-2170">Az.Cdn</span></span>
* <span data-ttu-id="cb43e-2171">Åtgärdade skrivfel i CDN-modulens konverteringshjälp</span><span class="sxs-lookup"><span data-stu-id="cb43e-2171">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb43e-2172">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb43e-2172">Az.Compute</span></span>
* <span data-ttu-id="cb43e-2173">Lägg till VmssId i New-AzVMConfig-cmdleten</span><span class="sxs-lookup"><span data-stu-id="cb43e-2173">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="cb43e-2174">Lägg till parametrarna TerminateScheduledEvents och TerminateScheduledEventNotBeforeTimeoutInMinutes i New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="cb43e-2174">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="cb43e-2175">Lägg till egenskapen HyperVGeneration till avbildningsobjekt för virtuell dator</span><span class="sxs-lookup"><span data-stu-id="cb43e-2175">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="cb43e-2176">Lägg till funktioner för Host och HostGroup</span><span class="sxs-lookup"><span data-stu-id="cb43e-2176">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="cb43e-2177">Nya cmdletar:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="cb43e-2177">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="cb43e-2178">HostId-parametern läggs till i New-AzVMConfig och New-AzVM</span><span class="sxs-lookup"><span data-stu-id="cb43e-2178">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="cb43e-2179">Uppdatera exempel i "Invoke-AzVMRunCommand"-dokumentationen till att använda rätt parameternamn</span><span class="sxs-lookup"><span data-stu-id="cb43e-2179">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="cb43e-2180">Uppdatera "-VolumeType"-beskrivningen i referensdokumentationen för "set-AzVMDiskEncryptionExtension" och "set-AzVmssDiskEncryptionExtension"</span><span class="sxs-lookup"><span data-stu-id="cb43e-2180">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cb43e-2181">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cb43e-2181">Az.DataFactory</span></span>
* <span data-ttu-id="cb43e-2182">Åtgärda skrivfel till att använda versaler för "Windows" i "New-AzDataFactoryEncryptValue"-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="cb43e-2182">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="cb43e-2183">Uppdaterade ADF .Net SDK-versionen till 4.1.2</span><span class="sxs-lookup"><span data-stu-id="cb43e-2183">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="cb43e-2184">Lägg till parametrarna "DataProxyIntegrationRuntimeName", "DataProxyStagingLinkedServiceName" och "DataProxyStagingPath" för "Set-AzureRmDataFactoryV2IntegrationRuntime"-cmd för att aktivera konfiguration av lokalt installerad integrationskörning som en proxy för SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="cb43e-2184">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="cb43e-2185">Uppdaterade PSTriggerRun till att visa utlöst pipeline, meddelande och egenskaper samt PSActivityRun till att visa aktivitetstypen</span><span class="sxs-lookup"><span data-stu-id="cb43e-2185">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cb43e-2186">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cb43e-2186">Az.DataLakeStore</span></span>
* <span data-ttu-id="cb43e-2187">Korrigering av frysning av Get-DataLakeStoreDeletedItem för fel eller fjärrundantag.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2187">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="cb43e-2188">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="cb43e-2188">Az.EventHub</span></span>
* <span data-ttu-id="cb43e-2189">Korrigering av problem #9658 : Skrivfel i parametern VirtualNteworkRule i Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="cb43e-2189">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="cb43e-2190">Korrigering av problem #9558 : Set-AzEventHubNamespace använder PATCH i stället för PUT</span><span class="sxs-lookup"><span data-stu-id="cb43e-2190">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="cb43e-2191">lade till parametern EnableKafka i Set-AzEventHubNamespace-cmdleten</span><span class="sxs-lookup"><span data-stu-id="cb43e-2191">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="cb43e-2192">Korrigering av problem #9786 : kan inte skapa en regel med Endast lyssna-behörighet</span><span class="sxs-lookup"><span data-stu-id="cb43e-2192">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="cb43e-2193">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="cb43e-2193">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="cb43e-2194">Åtgärdade skrivfel i dokumentation där "Azure" skrevs helt med gemener</span><span class="sxs-lookup"><span data-stu-id="cb43e-2194">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cb43e-2195">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cb43e-2195">Az.Monitor</span></span>
* <span data-ttu-id="cb43e-2196">Åtgärdade felaktigt parameternamn i hjälpdokumentationen</span><span class="sxs-lookup"><span data-stu-id="cb43e-2196">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb43e-2197">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb43e-2197">Az.Network</span></span>
* <span data-ttu-id="cb43e-2198">Uppdaterade New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="cb43e-2198">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="cb43e-2199">Gjorde parametern "PublicIpAddress" inaktuell eftersom den aldrig används på serversidan.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2199">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="cb43e-2200">Lade till den valfria parametern "Primary", som anger huruvida den aktuella IP-konfigurationen är den primära.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2200">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="cb43e-2201">Förbättrade hanteringen av felundantag för begärande från SDK – åtgärdar problemet att tidigare SDK-undantag inte hanteras på rätt sätt, vilket leder till att viktig felinformation inte visas</span><span class="sxs-lookup"><span data-stu-id="cb43e-2201">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="cb43e-2202">Justerade valideringslogiken för IPv6-IP-prefix till att kontrollera korrekt IPv6-prefixlängd.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2202">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="cb43e-2203">Uppdaterade Get-AzVirtualNetworkSubnetConfig: Lade till parameter som anges till get av undernätets resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2203">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="cb43e-2204">Uppdaterade beskrivningen av parametern Location för AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="cb43e-2204">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="cb43e-2205">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cb43e-2205">Az.OperationalInsights</span></span>
* <span data-ttu-id="cb43e-2206">Uppdaterade dokumentation för "New-AzOperationalInsightsLinuxSyslogDataSource"</span><span class="sxs-lookup"><span data-stu-id="cb43e-2206">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="cb43e-2207">Lade till exempel</span><span class="sxs-lookup"><span data-stu-id="cb43e-2207">Added example</span></span>
    - <span data-ttu-id="cb43e-2208">Uppdaterade beskrivningen av parametern "-Name"</span><span class="sxs-lookup"><span data-stu-id="cb43e-2208">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="cb43e-2209">Lade till ett exempel för New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="cb43e-2209">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="cb43e-2210">Ändrade beskrivningen av parametern -Name för New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="cb43e-2210">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cb43e-2211">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb43e-2211">Az.RecoveryServices</span></span>
* <span data-ttu-id="cb43e-2212">Uppdatera "Get-AzRecoveryServicesBackupJobDetail.md"</span><span class="sxs-lookup"><span data-stu-id="cb43e-2212">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb43e-2213">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb43e-2213">Az.Resources</span></span>
* <span data-ttu-id="cb43e-2214">Lägg till stöd för den nya API-versionen från 2019-05-10 för Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="cb43e-2214">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="cb43e-2215">Lägg till stöd för "copy.count = 0" för variabler, resurser och egenskaper</span><span class="sxs-lookup"><span data-stu-id="cb43e-2215">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="cb43e-2216">Resurser med "condition = false" eller "copy.count = 0" tas bort i complete-läget</span><span class="sxs-lookup"><span data-stu-id="cb43e-2216">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="cb43e-2217">Lägg till ett exempel på tilldelning av princip på prenumerationsnivå i hjälpdokumentationen</span><span class="sxs-lookup"><span data-stu-id="cb43e-2217">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="cb43e-2218">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="cb43e-2218">Az.ServiceBus</span></span>
* <span data-ttu-id="cb43e-2219">Korrigering av problem #9658 : Skrivfel i parametern VirtualNetworkRule i set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="cb43e-2219">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="cb43e-2220">Korrigering av problem #9786 : kan inte skapa en regel med Endast lyssna-behörighet</span><span class="sxs-lookup"><span data-stu-id="cb43e-2220">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="cb43e-2221">Lade till det nya kommandot "Test-AzServiceBusNameAvailability" för att kontrollera namntillgängligheten för kö och ämne</span><span class="sxs-lookup"><span data-stu-id="cb43e-2221">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="cb43e-2222">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cb43e-2222">Az.ServiceFabric</span></span>
* <span data-ttu-id="cb43e-2223">Åtgärda buggar med tillägg av nodtyps-cmdlet:</span><span class="sxs-lookup"><span data-stu-id="cb43e-2223">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="cb43e-2224">NullReferenceException-bugg när resursgrupp hade annan vmss som inte är relaterad till Service Fabric-klustret.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2224">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="cb43e-2225">Åtgärdar problemet: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="cb43e-2225">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="cb43e-2226">Åtgärda bugg där cmdleten misslyckades om virtualNetwork var i en annan resursgrupp än klustret.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2226">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="cb43e-2227">Åtgärdar problemet: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="cb43e-2227">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="cb43e-2228">AzServiceFabricApplicationCertificate-cmdleten görs inaktuell</span><span class="sxs-lookup"><span data-stu-id="cb43e-2228">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb43e-2229">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb43e-2229">Az.Sql</span></span>
* <span data-ttu-id="cb43e-2230">Uppdatera dokumentation om gamla gransknings-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2230">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cb43e-2231">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb43e-2231">Az.Storage</span></span>
* <span data-ttu-id="cb43e-2232">Uppdatera hjälpen för Get/Close-AzStorageFileHandle genom att lägga till fler scenarier i cmdlet-exempel och uppdatera parameterbeskrivningar</span><span class="sxs-lookup"><span data-stu-id="cb43e-2232">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="cb43e-2233">Stöd för StandardBlobTier i uppladdningsblob och kopieringsblob</span><span class="sxs-lookup"><span data-stu-id="cb43e-2233">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="cb43e-2234">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="cb43e-2234">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="cb43e-2235">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="cb43e-2235">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="cb43e-2236">Stöd för rehydratiseringsprioritet i kopieringsblob</span><span class="sxs-lookup"><span data-stu-id="cb43e-2236">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="cb43e-2237">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="cb43e-2237">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cb43e-2238">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb43e-2238">Az.Websites</span></span>
* <span data-ttu-id="cb43e-2239">Lägg till klargöranden gällande parametern -AppSettings i Set-AzWebApp och Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="cb43e-2239">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="cb43e-2240">2.5.0 – July 2019</span><span class="sxs-lookup"><span data-stu-id="cb43e-2240">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cb43e-2241">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb43e-2241">Az.Accounts</span></span>
* <span data-ttu-id="cb43e-2242">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="cb43e-2242">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="cb43e-2243">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="cb43e-2243">Az.ApplicationInsights</span></span>
* <span data-ttu-id="cb43e-2244">Korrigera skrivfel i exempel i dokumentationen för Remove-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="cb43e-2244">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cb43e-2245">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cb43e-2245">Az.Automation</span></span>
* <span data-ttu-id="cb43e-2246">Korrigera skrivfel i resurssträng</span><span class="sxs-lookup"><span data-stu-id="cb43e-2246">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="cb43e-2247">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cb43e-2247">Az.CognitiveServices</span></span>
* <span data-ttu-id="cb43e-2248">Stöd för NetworkRuleSet har lagts till.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2248">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb43e-2249">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb43e-2249">Az.Compute</span></span>
* <span data-ttu-id="cb43e-2250">Lägg till saknade egenskaper (ComputerName, OsName, OsVersion och HyperVGeneration) för visningsobjekt i den virtuella datorinstansen.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2250">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="cb43e-2251">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="cb43e-2251">Az.ContainerRegistry</span></span>
* <span data-ttu-id="cb43e-2252">Åtgärda skrivfel i Remove-AzContainerRegistryReplication för parametern Replication</span><span class="sxs-lookup"><span data-stu-id="cb43e-2252">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="cb43e-2253">Mer information finns här: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="cb43e-2253">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cb43e-2254">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cb43e-2254">Az.DataFactory</span></span>
* <span data-ttu-id="cb43e-2255">ADF .Net SDK-versionen har uppdaterats till 4.1.0</span><span class="sxs-lookup"><span data-stu-id="cb43e-2255">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="cb43e-2256">Korrigera skrivfel i dokumentationen för Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="cb43e-2256">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="cb43e-2257">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="cb43e-2257">Az.EventHub</span></span>
* <span data-ttu-id="cb43e-2258">Ny cmmdlet har lagts till för att skapa SAS-token: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="cb43e-2258">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="cb43e-2259">verifierings- och felmeddelande har lagts till för authorizationrules-rättigheter om endast "hantera" har tilldelats</span><span class="sxs-lookup"><span data-stu-id="cb43e-2259">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cb43e-2260">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cb43e-2260">Az.KeyVault</span></span>
* <span data-ttu-id="cb43e-2261">Stöd har lagts till för att ange KeySize för certifikatprinciper</span><span class="sxs-lookup"><span data-stu-id="cb43e-2261">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="cb43e-2262">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="cb43e-2262">Az.LogicApp</span></span>
* <span data-ttu-id="cb43e-2263">Korrigering för Get-AzIntegrationAccountMap för att lista alla mappningstyper</span><span class="sxs-lookup"><span data-stu-id="cb43e-2263">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="cb43e-2264">Ny MapType-parameter har lagts till för filtrering</span><span class="sxs-lookup"><span data-stu-id="cb43e-2264">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="cb43e-2265">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="cb43e-2265">Az.ManagedServices</span></span>
* <span data-ttu-id="cb43e-2266">Stöd för API-versionen 2019-06-01 (GA) har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-2266">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb43e-2267">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb43e-2267">Az.Network</span></span>
* <span data-ttu-id="cb43e-2268">Lägg till stöd för privat slutpunkt och privat länktjänst</span><span class="sxs-lookup"><span data-stu-id="cb43e-2268">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="cb43e-2269">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="cb43e-2269">New cmdlets</span></span>
        - <span data-ttu-id="cb43e-2270">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="cb43e-2270">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="cb43e-2271">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="cb43e-2271">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="cb43e-2272">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="cb43e-2272">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="cb43e-2273">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="cb43e-2273">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="cb43e-2274">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="cb43e-2274">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="cb43e-2275">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="cb43e-2275">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="cb43e-2276">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="cb43e-2276">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="cb43e-2277">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="cb43e-2277">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="cb43e-2278">Nedanstående kommandon för funktionen har uppdaterats: Flaggan PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies på undernätet i VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cb43e-2278">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="cb43e-2279">Uppdaterade New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="cb43e-2279">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="cb43e-2280">Valfri parameter har lagts till – PrivateEndpointNetworkPoliciesFlag som konfigurerar huruvida nätverksprinciper ska tillämpas på en privat slutpunkt i det här undernätet.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2280">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="cb43e-2281">Valfri parameter har lagts till – PrivateLinkServiceNetworkPoliciesFlag som konfigurerar huruvida nätverksprinciper ska tillämpas på en privat länktjänst i det här undernätet.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2281">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="cb43e-2282">AzPrivateLinkService för cmdlet-parametern ServiceName har bytt namn till Name med aliaset ServiceName för bakåtkompatibilitet</span><span class="sxs-lookup"><span data-stu-id="cb43e-2282">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="cb43e-2283">Aktivera ICMP-protokoll för konfiguration av nätverkssäkerhetsregler</span><span class="sxs-lookup"><span data-stu-id="cb43e-2283">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="cb43e-2284">Uppdaterade cmdletar</span><span class="sxs-lookup"><span data-stu-id="cb43e-2284">Updated cmdlets</span></span>
        - <span data-ttu-id="cb43e-2285">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cb43e-2285">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="cb43e-2286">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cb43e-2286">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="cb43e-2287">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cb43e-2287">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="cb43e-2288">Lägg till ConnectionProtocolType (Ikev1/Ikev2) som en konfigurerbar parameter för New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="cb43e-2288">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="cb43e-2289">Lägg till PrivateIpAddressVersion i LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb43e-2289">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="cb43e-2290">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="cb43e-2290">Updated cmdlet:</span></span>
        - <span data-ttu-id="cb43e-2291">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="cb43e-2291">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="cb43e-2292">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="cb43e-2292">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="cb43e-2293">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="cb43e-2293">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="cb43e-2294">Uppdatering av Application Gateway-kommandot New-AzApplicationGatewayProbeConfig för stöd av anpassad port i Probe</span><span class="sxs-lookup"><span data-stu-id="cb43e-2294">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="cb43e-2295">Uppdaterade New-AzApplicationGatewayProbeConfig: Den valfria parametern Port som används för avsökning i serverdelen har lagts till.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2295">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="cb43e-2296">Denna parameter gäller för SKU:erna Standard_V2 och WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2296">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="cb43e-2297">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cb43e-2297">Az.OperationalInsights</span></span>
* <span data-ttu-id="cb43e-2298">Uppdaterade standardversionen för sparade sökningar till 1.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2298">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="cb43e-2299">Åtgärdade hantering av anpassad log null regex</span><span class="sxs-lookup"><span data-stu-id="cb43e-2299">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cb43e-2300">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb43e-2300">Az.RecoveryServices</span></span>
* <span data-ttu-id="cb43e-2301">Uppdatera Get-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="cb43e-2301">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="cb43e-2302">Uppdatera Get-AzRecoveryServicesBackupContainer.md</span><span class="sxs-lookup"><span data-stu-id="cb43e-2302">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="cb43e-2303">Uppdatera Get-AzRecoveryServicesVault.md</span><span class="sxs-lookup"><span data-stu-id="cb43e-2303">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="cb43e-2304">Uppdatera Wait-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="cb43e-2304">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="cb43e-2305">Uppdatera Set-AzRecoveryServicesVaultContext.md</span><span class="sxs-lookup"><span data-stu-id="cb43e-2305">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="cb43e-2306">Uppdatera Get-AzRecoveryServicesBackupItem.md</span><span class="sxs-lookup"><span data-stu-id="cb43e-2306">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="cb43e-2307">Uppdatera Get-AzRecoveryServicesBackupRecoveryPoint.md</span><span class="sxs-lookup"><span data-stu-id="cb43e-2307">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="cb43e-2308">Uppdatera Restore-AzRecoveryServicesBackupItem.md</span><span class="sxs-lookup"><span data-stu-id="cb43e-2308">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="cb43e-2309">Uppdaterat tjänstanrop för avregistrering av container för Azure-filresurs</span><span class="sxs-lookup"><span data-stu-id="cb43e-2309">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="cb43e-2310">Uppdatera Set-AzRecoveryServicesAsrAlertSetting.md</span><span class="sxs-lookup"><span data-stu-id="cb43e-2310">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb43e-2311">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb43e-2311">Az.Resources</span></span>
- <span data-ttu-id="cb43e-2312">Ta bort den cmdlet som saknas och som refereras i dokumentationen till New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="cb43e-2312">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="cb43e-2313">Princip-cmdletar har uppdaterats så att de använder den nya API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="cb43e-2313">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="cb43e-2314">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="cb43e-2314">Az.ServiceBus</span></span>
* <span data-ttu-id="cb43e-2315">Ny cmmdlet har lagts till för att skapa SAS-token: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="cb43e-2315">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="cb43e-2316">verifierings- och felmeddelande har lagts till för authorizationrules-rättigheter om endast "hantera" har tilldelats</span><span class="sxs-lookup"><span data-stu-id="cb43e-2316">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb43e-2317">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb43e-2317">Az.Sql</span></span>
* <span data-ttu-id="cb43e-2318">Åtgärda saknade exempel för Set-AzSqlDatabaseSecondary cmdlet</span><span class="sxs-lookup"><span data-stu-id="cb43e-2318">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="cb43e-2319">Åtgärda angivna återkommande genomsökningar för bedömning av säkerhetsrisk utan angivna e-postadresser</span><span class="sxs-lookup"><span data-stu-id="cb43e-2319">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="cb43e-2320">Korrigera ett skrivfel i ett varningsmeddelande.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2320">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cb43e-2321">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb43e-2321">Az.Storage</span></span>
* <span data-ttu-id="cb43e-2322">Uppdatera exempel i referensdokumentationen för Get-AzStorageAccount så att rätt parameternamn används</span><span class="sxs-lookup"><span data-stu-id="cb43e-2322">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="cb43e-2323">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="cb43e-2323">Az.StorageSync</span></span>
* <span data-ttu-id="cb43e-2324">Lägger till cmdleten Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2324">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="cb43e-2325">Åtgärda problem 9551 så att TierFilesOlderThanDays föredras</span><span class="sxs-lookup"><span data-stu-id="cb43e-2325">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cb43e-2326">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb43e-2326">Az.Websites</span></span>
* <span data-ttu-id="cb43e-2327">Åtgärdar ett fel där vissa SiteConfig-egenskaper inte returnerades av Get-AzWebApp och Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="cb43e-2327">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="cb43e-2328">Lägger till en ny platsparameter för Get-AzDeletedWebApp och Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="cb43e-2328">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="cb43e-2329">Åtgärdar ett fel i kloning av webbapp-platser som använder New-AzWebApp-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="cb43e-2329">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="cb43e-2330">2.4.0 – juli 2019</span><span class="sxs-lookup"><span data-stu-id="cb43e-2330">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cb43e-2331">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb43e-2331">Az.Accounts</span></span>
* <span data-ttu-id="cb43e-2332">Lägg till stöd för profil-cmdletar</span><span class="sxs-lookup"><span data-stu-id="cb43e-2332">Add support for profile cmdlets</span></span>
* <span data-ttu-id="cb43e-2333">Lägg till stöd för miljöer och dataplaner i genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="cb43e-2333">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="cb43e-2334">Åtgärda bugg där fel slutpunkt i vissa fall användes för cmdletar för dataplaner i Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="cb43e-2334">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="cb43e-2335">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="cb43e-2335">Az.Advisor</span></span>
* <span data-ttu-id="cb43e-2336">GA-version av Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="cb43e-2336">GA release of Az.Advisor</span></span>
* <span data-ttu-id="cb43e-2337">Den här modulen ingår nu som en del av `Az`-sammanslagningsmodulen</span><span class="sxs-lookup"><span data-stu-id="cb43e-2337">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="cb43e-2338">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cb43e-2338">Az.ApiManagement</span></span>
* <span data-ttu-id="cb43e-2339">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="cb43e-2339">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="cb43e-2340">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="cb43e-2340">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="cb43e-2341">Stöd för att fråga prenumerationer efter användare och produkt har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-2341">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="cb43e-2342">Stöd för att fråga med hjälp av omfång ”/”, ”/apis”, ”/apis/echo-api” har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-2342">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="cb43e-2343">Korrigering av problem https://github.com/Azure/azure-powershell/issues/9307 och https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="cb43e-2343">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="cb43e-2344">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="cb43e-2344">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="cb43e-2345">Stöd för att ange ”ApiVersion” och ”ApiVersionSetId” när API:er importeras har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-2345">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cb43e-2346">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cb43e-2346">Az.Automation</span></span>
* <span data-ttu-id="cb43e-2347">Bugg med cmdleten Set-AzAutomationConnectionFieldValue för att hantera strängvärde har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2347">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb43e-2348">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb43e-2348">Az.Compute</span></span>
* <span data-ttu-id="cb43e-2349">Lägg till parametern HyperVGeneration i New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="cb43e-2349">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cb43e-2350">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cb43e-2350">Az.DataFactory</span></span>
* <span data-ttu-id="cb43e-2351">Uppdaterar utdata från ADF-cmdletar som hämtar aktivitetskörningar, hämtar pipelinekörningar och hämtar utlösarkörningar för stöd för Select-Object-pipe.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2351">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="cb43e-2352">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="cb43e-2352">Az.EventGrid</span></span>
* <span data-ttu-id="cb43e-2353">Korrigera stavfel i dokumentation om ”New-AzEventGridSubscription”</span><span class="sxs-lookup"><span data-stu-id="cb43e-2353">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cb43e-2354">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cb43e-2354">Az.IotHub</span></span>
* <span data-ttu-id="cb43e-2355">Lägg till stöd för att återskapa principnycklar för auktorisering.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2355">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb43e-2356">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb43e-2356">Az.Network</span></span>
* <span data-ttu-id="cb43e-2357">”RoutingPreference” har lagts till i offentliga IP-taggar</span><span class="sxs-lookup"><span data-stu-id="cb43e-2357">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="cb43e-2358">Förbättra exempel för referensdokumentation om ”Get-AzNetworkServiceTag”</span><span class="sxs-lookup"><span data-stu-id="cb43e-2358">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="cb43e-2359">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="cb43e-2359">Az.PolicyInsights</span></span>
* <span data-ttu-id="cb43e-2360">Åtgärda problem med null-referens i Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="cb43e-2360">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="cb43e-2361">Mer information här: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="cb43e-2361">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="cb43e-2362">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cb43e-2362">Az.OperationalInsights</span></span>
* <span data-ttu-id="cb43e-2363">Modellen för CustomLog-datakälla som returneras i Get-AzOperationalInsightsDataSource har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="cb43e-2363">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cb43e-2364">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb43e-2364">Az.RecoveryServices</span></span>
* <span data-ttu-id="cb43e-2365">Kommandot get-policy för IaaSVM:er har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="cb43e-2365">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb43e-2366">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb43e-2366">Az.Resources</span></span>
    - <span data-ttu-id="cb43e-2367">Korrigera hjälptext för den översta parametern i Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="cb43e-2367">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="cb43e-2368">Lägg till växlingsstöd på klientsidan för Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="cb43e-2368">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="cb43e-2369">Lägg till nya parametrar för Set-AzPolicyAssignment, -PolicyParameters och -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="cb43e-2369">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="cb43e-2370">En mängd dokument- och exempeluppdateringar för Policy-cmdletar</span><span class="sxs-lookup"><span data-stu-id="cb43e-2370">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="cb43e-2371">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="cb43e-2371">Az.ServiceBus</span></span>
* <span data-ttu-id="cb43e-2372">Korrigering av problem #4938 – New-AzureRmServiceBusQueue returnerar BadRequest vid konfiguration av MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="cb43e-2372">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb43e-2373">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb43e-2373">Az.Sql</span></span>
* <span data-ttu-id="cb43e-2374">Lägg till cmdletar för instansredundansgrupper från förhandsversion till offentlig version</span><span class="sxs-lookup"><span data-stu-id="cb43e-2374">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="cb43e-2375">Stöd för granskning för Azure SQL Server\Database med nya cmdletar.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2375">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="cb43e-2376">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="cb43e-2376">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="cb43e-2377">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="cb43e-2377">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="cb43e-2378">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="cb43e-2378">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="cb43e-2379">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="cb43e-2379">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="cb43e-2380">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="cb43e-2380">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="cb43e-2381">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="cb43e-2381">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="cb43e-2382">Ta bort begränsningar för e-post från inställningarna för sårbarhetsbedömning</span><span class="sxs-lookup"><span data-stu-id="cb43e-2382">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cb43e-2383">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb43e-2383">Az.Storage</span></span>
* <span data-ttu-id="cb43e-2384">Ändra två parametrar ”-IndexDocument” och ”-ErrorDocument404Path” från ”krävs” till ”valfri” i cmdlet:</span><span class="sxs-lookup"><span data-stu-id="cb43e-2384">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="cb43e-2385">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="cb43e-2385">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="cb43e-2386">Uppdatera hjälpen för Get-AzStorageBlobContent genom att lägga till ett exempel</span><span class="sxs-lookup"><span data-stu-id="cb43e-2386">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="cb43e-2387">Visa mer felinformation när cmdleten misslyckas med StorageException</span><span class="sxs-lookup"><span data-stu-id="cb43e-2387">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="cb43e-2388">Stöd för att skapa eller uppdatera lagringskonto med Azure Files AAD DS-autentisering</span><span class="sxs-lookup"><span data-stu-id="cb43e-2388">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="cb43e-2389">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cb43e-2389">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="cb43e-2390">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cb43e-2390">Set-AzStorageAccount</span></span>
* <span data-ttu-id="cb43e-2391">Stöd för att lista eller stänga filreferenser för en filresurs, filkatalog eller en fil</span><span class="sxs-lookup"><span data-stu-id="cb43e-2391">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="cb43e-2392">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="cb43e-2392">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="cb43e-2393">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="cb43e-2393">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="cb43e-2394">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="cb43e-2394">Az.StorageSync</span></span>
* <span data-ttu-id="cb43e-2395">Den här modulen ingår nu som en del av `Az`-sammanslagningsmodulen</span><span class="sxs-lookup"><span data-stu-id="cb43e-2395">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="cb43e-2396">2.3.2 – juni 2019</span><span class="sxs-lookup"><span data-stu-id="cb43e-2396">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cb43e-2397">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb43e-2397">Az.Accounts</span></span>
* <span data-ttu-id="cb43e-2398">Åtgärda bugg med felaktiga webbadresser som i vissa fall användes för Functions-anrop</span><span class="sxs-lookup"><span data-stu-id="cb43e-2398">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="cb43e-2399">Mer information här: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="cb43e-2399">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="cb43e-2400">Åtgärda problem med alias från AzureRM i Az-cmdletar</span><span class="sxs-lookup"><span data-stu-id="cb43e-2400">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="cb43e-2401">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="cb43e-2401">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="cb43e-2402">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="cb43e-2402">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb43e-2403">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb43e-2403">Az.Compute</span></span>
* <span data-ttu-id="cb43e-2404">Parameteruppsättningarna New-AzVm och New-AzVmss accepterar nu parametern ”ProximityPlacementGroup”.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2404">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="cb43e-2405">Stavfel i referensdokumentationen för ”New-AzVM” har korrigerats</span><span class="sxs-lookup"><span data-stu-id="cb43e-2405">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="cb43e-2406">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="cb43e-2406">Az.Dns</span></span>
* <span data-ttu-id="cb43e-2407">Stavfel i hjälpexempel för ”Set-AzDnsZone” har korrigerats.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2407">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="cb43e-2408">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="cb43e-2408">Az.EventGrid</span></span>
* <span data-ttu-id="cb43e-2409">Har uppdaterats för att använda API-versionen 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2409">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="cb43e-2410">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="cb43e-2410">New cmdlets:</span></span>
    - <span data-ttu-id="cb43e-2411">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="cb43e-2411">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="cb43e-2412">Skapar en ny Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2412">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="cb43e-2413">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="cb43e-2413">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="cb43e-2414">Hämtar information om en Event Grid-domän eller hämtar en lista med alla Event Grid-domäner i den aktuella Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2414">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="cb43e-2415">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="cb43e-2415">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="cb43e-2416">Tar bort en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2416">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="cb43e-2417">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="cb43e-2417">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="cb43e-2418">Återskapar nyckeln för delad åtkomst för en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2418">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="cb43e-2419">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="cb43e-2419">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="cb43e-2420">Hämtar de nycklar för delad åtkomst som används för att publicera händelser till en Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2420">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="cb43e-2421">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="cb43e-2421">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="cb43e-2422">Skapar ett nytt Azure Event Grid-domänämne.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2422">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="cb43e-2423">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="cb43e-2423">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="cb43e-2424">Hämtar information om ett Event Grid-domänämne eller hämtar en lista med alla Event Grid-domänämnen under en specifik Event Grid-domän i nuvarande Azure</span><span class="sxs-lookup"><span data-stu-id="cb43e-2424">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="cb43e-2425">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="cb43e-2425">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="cb43e-2426">Tar bort ett befintligt Azure Event Grid-domänämne.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2426">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="cb43e-2427">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="cb43e-2427">Updated cmdlets:</span></span>
    - <span data-ttu-id="cb43e-2428">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="cb43e-2428">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="cb43e-2429">Lägg till nya obligatoriska parametrar för att stödja piping för den nya Event Grid-domänen och Event Grid-domänämnet för att göra det möjligt att skapa nya händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2429">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="cb43e-2430">Lägg till nya obligatoriska parametrar för att ange det nya Event Grid-domännamnet och/eller namnet på Event Grid-domänämnet för att göra det möjligt att skapa nya händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2430">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="cb43e-2431">Lägg till ny parameteruppsättningar för domäner och domänämnen för att göra det möjligt att återanvända befintliga parametrar (t.ex. EndPointType, SubjectBeginsWith osv).</span><span class="sxs-lookup"><span data-stu-id="cb43e-2431">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="cb43e-2432">Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="cb43e-2432">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="cb43e-2433">Förfallodatum för händelseprenumeration</span><span class="sxs-lookup"><span data-stu-id="cb43e-2433">Event subscription expiration date,</span></span>
            - <span data-ttu-id="cb43e-2434">Avancerade filterparametrar.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2434">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="cb43e-2435">Lägg till ny uppräkning för servicebusqueue som mål.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2435">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="cb43e-2436">Tillåt inte användning av ”Alla” i alternativet -IncludedEventType och ersätt det med</span><span class="sxs-lookup"><span data-stu-id="cb43e-2436">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="cb43e-2437">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="cb43e-2437">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="cb43e-2438">Lägg till ny valfria parametrar (Top, ODataQuery och NextLink) för att stödja sidnumrering och filtrering av resultat.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2438">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="cb43e-2439">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="cb43e-2439">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="cb43e-2440">Lägg till nya obligatoriska parametrar för att stödja piping för en Event Grid-domän och Event Grid-domänämnen för att göra det möjligt att ta bort befintliga händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2440">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="cb43e-2441">Lägg till nya obligatoriska parametrar för att ange Event Grid-domännamnet och/eller namnet på Event Grid-domänämnet för att göra det möjligt att ta bort befintliga händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2441">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="cb43e-2442">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="cb43e-2442">Az.FrontDoor</span></span>
* <span data-ttu-id="cb43e-2443">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="cb43e-2443">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="cb43e-2444">Lägg till stöd för transformeringar och nytt värde för automatisk komplettering för operatorer (RegEx)</span><span class="sxs-lookup"><span data-stu-id="cb43e-2444">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="cb43e-2445">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="cb43e-2445">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="cb43e-2446">Lägg till nya värden för automatisk komplettering</span><span class="sxs-lookup"><span data-stu-id="cb43e-2446">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb43e-2447">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb43e-2447">Az.Network</span></span>
* <span data-ttu-id="cb43e-2448">Lägg till stöd för resurs för virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="cb43e-2448">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="cb43e-2449">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="cb43e-2449">New cmdlets</span></span>
        - <span data-ttu-id="cb43e-2450">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="cb43e-2450">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="cb43e-2451">Lägg till AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="cb43e-2451">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="cb43e-2452">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="cb43e-2452">New cmdlets</span></span>
        - <span data-ttu-id="cb43e-2453">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="cb43e-2453">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="cb43e-2454">Lägg till PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="cb43e-2454">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="cb43e-2455">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="cb43e-2455">New cmdlets</span></span>
        - <span data-ttu-id="cb43e-2456">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="cb43e-2456">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="cb43e-2457">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="cb43e-2457">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="cb43e-2458">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="cb43e-2458">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="cb43e-2459">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="cb43e-2459">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="cb43e-2460">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="cb43e-2460">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="cb43e-2461">Lägg till PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="cb43e-2461">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="cb43e-2462">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="cb43e-2462">New cmdlets</span></span>
        - <span data-ttu-id="cb43e-2463">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="cb43e-2463">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="cb43e-2464">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="cb43e-2464">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="cb43e-2465">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="cb43e-2465">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="cb43e-2466">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="cb43e-2466">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="cb43e-2467">Nedanstående kommandon för funktionen har uppdaterats: Flaggan UseLocalAzureIpAddress på VpnConnection</span><span class="sxs-lookup"><span data-stu-id="cb43e-2467">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="cb43e-2468">New-AzVpnConnection har uppdaterats: Den valfria parametern -UseLocalAzureIpAddress har lagts till för att visa att en lokal IP-adress i Azure ska användas som källadress när anslutningen initieras.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2468">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="cb43e-2469">Set-AzVpnConnection har uppdaterats: Den valfria parametern -UseLocalAzureIpAddress har lagts till för att visa att en lokal IP-adress i Azure ska användas som källadress när anslutningen initieras.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2469">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="cb43e-2470">Det skrivskyddade fältet PeeredConnections har lagts till i ExpressRoute-peering.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2470">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="cb43e-2471">Det skrivskyddade fältet GlobalReachEnabled har lagts till i ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2471">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="cb43e-2472">Ett attribut för icke-bakåtkompatibla ändringar har lagts till för att lyfta fram utfasning av fältet AllowGlobalReach i modellen ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="cb43e-2472">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="cb43e-2473">Problem 8756 har åtgärdats: Fel vid användning av TargetListenerID med AzApplicationGatewayRedirectConfiguration-cmdletar</span><span class="sxs-lookup"><span data-stu-id="cb43e-2473">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="cb43e-2474">En bugg i New-AzApplicationGatewayPathRuleConfig som gjorde att regeluppsättningen för att återskapa inte kunde anges har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2474">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="cb43e-2475">Visningen av VirtualNetworkTaps i NetworkInterfaceIpConfiguration har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="cb43e-2475">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="cb43e-2476">Cortex Get-cmdletar för att visa en lista med alla delar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="cb43e-2476">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="cb43e-2477">Funktionen för att skapa VirtualHub-referenser för ExpressRouteGateways och VpnGateway har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="cb43e-2477">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="cb43e-2478">Stöd för tillgänglighetszoner i AzureFirewall och NatGateway har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-2478">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="cb43e-2479">Cmdleten Get-AzNetworkServiceTag har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-2479">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="cb43e-2480">Lägg till stöd för flera offentliga IP-adresser för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="cb43e-2480">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="cb43e-2481">Cmdleten New-AzFirewall har uppdaterats:</span><span class="sxs-lookup"><span data-stu-id="cb43e-2481">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="cb43e-2482">Parametern -PublicIpAddress som accepterar ett eller flera offentliga IP-adressobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-2482">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="cb43e-2483">Parametern -VirtualNetwork som accepterar ett virtuellt nätverksobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-2483">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="cb43e-2484">Metoderna AddPublicIpAddress och RemovePublicIpAddress har lagts till på brandväggsobjekt – dessa accepterar ett offentligt IP-adressobjekt som indata</span><span class="sxs-lookup"><span data-stu-id="cb43e-2484">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="cb43e-2485">Inaktuella parametrar -PublicIpName och -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="cb43e-2485">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="cb43e-2486">Nedanstående kommandon för funktionen har uppdaterats: Ange autentiseringsalternativ för VpnClient AAD till resurser för virtuella nätverksgatewayer.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2486">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="cb43e-2487">New-AzVirtualNetworkGateway har uppdaterats: De valfria parametrarna AadTenantUri, AadAudienceId och AadIssuerUri för att ange VpnClient AAD-autentiseringsalternativ på en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2487">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="cb43e-2488">Set-AzVirtualNetworkGateway har uppdaterats: De valfria parametrarna AadTenantUri, AadAudienceId och AadIssuerUri för att ange VpnClient AAD-autentiseringsalternativ på en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2488">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="cb43e-2489">Set-AzVirtualNetworkGateway har uppdaterats: Den valfria växelparametern RemoveAadAuthentication som tar bort VpnClient AAD-autentiseringsalternativ från en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2489">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="cb43e-2490">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cb43e-2490">Az.OperationalInsights</span></span>
* <span data-ttu-id="cb43e-2491">Aktivera prisnivån **pergb2018** i kommandot ”New-AzureRmOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="cb43e-2491">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb43e-2492">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb43e-2492">Az.Resources</span></span>
* <span data-ttu-id="cb43e-2493">Stöd för ytterligare alternativ för att exportera en mall</span><span class="sxs-lookup"><span data-stu-id="cb43e-2493">Support for additional Template Export options</span></span>
    - <span data-ttu-id="cb43e-2494">Lägg till parametern ”-SkipResourceNameParameterization” till Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="cb43e-2494">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="cb43e-2495">Lägg till parametern ”-SkipAllParameterization” till Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="cb43e-2495">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="cb43e-2496">Lägg till parametern ”-Resource” till Export-AzResourceGroup för exporterad resursfiltrering</span><span class="sxs-lookup"><span data-stu-id="cb43e-2496">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="cb43e-2497">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cb43e-2497">Az.ServiceFabric</span></span>
* <span data-ttu-id="cb43e-2498">Åtgärda att fel tumavtryck används vid tilläggning av certifikat i ByExistingKeyVault i vissa fall</span><span class="sxs-lookup"><span data-stu-id="cb43e-2498">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb43e-2499">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb43e-2499">Az.Sql</span></span>
* <span data-ttu-id="cb43e-2500">Åtgärda suffix för lagringsslutpunkt i Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="cb43e-2500">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="cb43e-2501">Åtgärda att aktivering av Advanced Data Security åsidosätter Advanced Threat Protection-princip</span><span class="sxs-lookup"><span data-stu-id="cb43e-2501">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="cb43e-2502">Nya cmdletar för Management.Sql som gör att kunderna kan lägga till nycklar för transparent datakryptering (TDE) och ange TDE-skydd för hanterade instanser</span><span class="sxs-lookup"><span data-stu-id="cb43e-2502">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="cb43e-2503">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="cb43e-2503">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="cb43e-2504">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="cb43e-2504">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="cb43e-2505">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="cb43e-2505">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="cb43e-2506">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="cb43e-2506">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="cb43e-2507">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="cb43e-2507">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cb43e-2508">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb43e-2508">Az.Storage</span></span>
* <span data-ttu-id="cb43e-2509">Stöd för typerna FileStorage och SkuName Premium_ZRS när lagringskonton skapas</span><span class="sxs-lookup"><span data-stu-id="cb43e-2509">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="cb43e-2510">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cb43e-2510">New-AzStorageAccount</span></span>
* <span data-ttu-id="cb43e-2511">Beskrivningen av cmdleten för bloboföränderlighet har förtydligats</span><span class="sxs-lookup"><span data-stu-id="cb43e-2511">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="cb43e-2512">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="cb43e-2512">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cb43e-2513">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb43e-2513">Az.Websites</span></span>
* <span data-ttu-id="cb43e-2514">Optimerar Get-AzWebAppCertificate för att filtrera efter resursgrupp på servern i stället för klienten</span><span class="sxs-lookup"><span data-stu-id="cb43e-2514">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="cb43e-2515">Lägger till växlingsparametern -UseDisasterRecovery till Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="cb43e-2515">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="cb43e-2516">2.2.0 – juni 2019</span><span class="sxs-lookup"><span data-stu-id="cb43e-2516">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="cb43e-2517">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="cb43e-2517">Az.Cdn</span></span>
* <span data-ttu-id="cb43e-2518">Uppdaterade cmdletar för att ge stöd för rulesEngine-funktion baserat på API-version 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2518">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb43e-2519">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb43e-2519">Az.Compute</span></span>
* <span data-ttu-id="cb43e-2520">Lade till parameter `NoWait` som startar åtgärden och returnerar omedelbart, innan åtgärden har slutförts.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2520">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="cb43e-2521">Uppdaterade cmdletar:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="cb43e-2521">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="cb43e-2522">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="cb43e-2522">Az.EventHub</span></span>
* <span data-ttu-id="cb43e-2523">Korrigering för #9231 – Get-AzEventHubNamespace returnerar inga taggar</span><span class="sxs-lookup"><span data-stu-id="cb43e-2523">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="cb43e-2524">Korrigering för #9230 – Get-AzEventHubNamespace returnerar ResourceGroup istället för ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb43e-2524">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb43e-2525">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb43e-2525">Az.Network</span></span>
* <span data-ttu-id="cb43e-2526">Uppdatera ResourceId och InputObject för NAT-gateway</span><span class="sxs-lookup"><span data-stu-id="cb43e-2526">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="cb43e-2527">Lägg till alias för ResourceId och InputObject</span><span class="sxs-lookup"><span data-stu-id="cb43e-2527">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="cb43e-2528">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="cb43e-2528">Az.PolicyInsights</span></span>
* <span data-ttu-id="cb43e-2529">Åtgärda Null-referensproblem i Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="cb43e-2529">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cb43e-2530">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb43e-2530">Az.RecoveryServices</span></span>
* <span data-ttu-id="cb43e-2531">Minsta kvarhållning för IaaSVM-policy i dagar ändrat till 7 från 1</span><span class="sxs-lookup"><span data-stu-id="cb43e-2531">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="cb43e-2532">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="cb43e-2532">Az.ServiceBus</span></span>
* <span data-ttu-id="cb43e-2533">Korrigering för ärende #9182 – Get-AzServiceBusNamespace returnerar ResourceGroup istället för ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb43e-2533">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="cb43e-2534">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cb43e-2534">Az.ServiceFabric</span></span>
* <span data-ttu-id="cb43e-2535">Åtgärda stavfel i felmeddelandet för Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="cb43e-2535">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="cb43e-2536">Åtgärda saknat tecken i Service Fabric-kommandorader</span><span class="sxs-lookup"><span data-stu-id="cb43e-2536">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb43e-2537">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb43e-2537">Az.Sql</span></span>
* <span data-ttu-id="cb43e-2538">Lägg till parametern DnsZonePartner för New-AzureSqlInstance-cmdlet för att ge stöd för AutoDr för hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2538">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="cb43e-2539">Avvecklar cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="cb43e-2539">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="cb43e-2540">Döp om cmdletar för hotidentifiering till Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="cb43e-2540">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="cb43e-2541">Parametrarna New-AzSqlInstance -StorageSizeInGB och -LicenseType är nu valfria.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2541">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cb43e-2542">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb43e-2542">Az.Websites</span></span>
* <span data-ttu-id="cb43e-2543">åtgärdar problemet där användningen av Set-AzWebApp och Set-AzWebAppSlot med -WebApp-egenskap tog bort taggarna</span><span class="sxs-lookup"><span data-stu-id="cb43e-2543">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="cb43e-2544">2.1.0 – maj 2019</span><span class="sxs-lookup"><span data-stu-id="cb43e-2544">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="cb43e-2545">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cb43e-2545">Az.ApiManagement</span></span>
* <span data-ttu-id="cb43e-2546">Skapade nya cmdletar för att hantera diagnostik för global- och API-omfång</span><span class="sxs-lookup"><span data-stu-id="cb43e-2546">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="cb43e-2547">**Get-AzApiManagementDiagnostic** – Skaffa diagnostik konfigurerad för global- eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="cb43e-2547">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="cb43e-2548">**New-AzApiManagementDiagnostic** – Skapa ny diagnostik för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="cb43e-2548">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="cb43e-2549">**New-AzApiManagementHttpMessageDiagnostic** – Skapa diagnostikinställning om vilka rubriker som ska loggas och storleken på brödtextbyte</span><span class="sxs-lookup"><span data-stu-id="cb43e-2549">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="cb43e-2550">**New-AzApiManagementPipelineDiagnosticSetting** – Skapa diagnostikinställningar för inkommande/utgående HTTP-meddelanden till gatewayen.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2550">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="cb43e-2551">**New-AzApiManagementSamplingSetting** – Skapa samplinginställningar för begäranden/svar för en diagnostik</span><span class="sxs-lookup"><span data-stu-id="cb43e-2551">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="cb43e-2552">**Remove-AzApiManagementDiagnostic** – Ta bort en diagnostikenhet för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="cb43e-2552">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="cb43e-2553">**Set-AzApiManagementDiagnostic** – Uppdatera en diagnostikenhet för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="cb43e-2553">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="cb43e-2554">Skapade nya cmdletar för hantering av cacheminne i ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="cb43e-2554">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="cb43e-2555">**Get-AzApiManagementCache** – Hämta information om cacheminnet som anges av identifierare eller alla cacheminnen</span><span class="sxs-lookup"><span data-stu-id="cb43e-2555">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="cb43e-2556">**New-AzApiManagementCache** – Skapa ett nytt default-cacheminne eller cacheminne i en viss Azure-region</span><span class="sxs-lookup"><span data-stu-id="cb43e-2556">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="cb43e-2557">**Remove-AzApiManagementCache** – Ta bort ett cacheminne</span><span class="sxs-lookup"><span data-stu-id="cb43e-2557">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="cb43e-2558">**Remove-AzApiManagementCache** – Ta bort ett cacheminne</span><span class="sxs-lookup"><span data-stu-id="cb43e-2558">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="cb43e-2559">Skapade nya cmdletar för hantering av API-schema</span><span class="sxs-lookup"><span data-stu-id="cb43e-2559">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="cb43e-2560">**New-AzApiManagementSchema** – Skapa ett nytt schema för ett API</span><span class="sxs-lookup"><span data-stu-id="cb43e-2560">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="cb43e-2561">**Get-AzApiManagementSchema** – Hämta de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="cb43e-2561">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="cb43e-2562">**Remove-AzApiManagementSchema** – Ta bort de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="cb43e-2562">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="cb43e-2563">**Set-AzApiManagementSchema** – Uppdatera de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="cb43e-2563">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="cb43e-2564">Skapa ny cmdlet för att generera en användartoken.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2564">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="cb43e-2565">**New-AzApiManagementUserToken** – Skapa en ny användartoken som enligt standardinställning är giltig i 8 timmar. Token för GIT-användaren kan skapas med den här cmdleten./</span><span class="sxs-lookup"><span data-stu-id="cb43e-2565">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="cb43e-2566">Skapade en ny cmdlet för att hämta nätverksstatus</span><span class="sxs-lookup"><span data-stu-id="cb43e-2566">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="cb43e-2567">**Get-AzApiManagementNetworkStatus** – Hämta nätverksstatusanslutningen för resurserna som API Management-tjänsten är beroende av.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2567">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="cb43e-2568">Det här är användbart när du distribuerar ApiManagement-tjänsten i ett virtuellt nätverk och validerar om något beroende är brutet.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2568">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="cb43e-2569">Uppdaterade cmdlet **New-AzApiManagement** för att hantera ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="cb43e-2569">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="cb43e-2570">Lade till stöd för den nya SKU:n Consumption</span><span class="sxs-lookup"><span data-stu-id="cb43e-2570">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="cb43e-2571">Aktiverade stöd för att slå på flaggan EnableClientCertificate för SKU:n Consumption</span><span class="sxs-lookup"><span data-stu-id="cb43e-2571">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="cb43e-2572">Den nya cmdleten **New-AzApiManagementSslSetting** gör det möjligt att ställa in TLS/SSL-inställningen på ”Backend” och ”Frontend” (serverdel och klientdel).</span><span class="sxs-lookup"><span data-stu-id="cb43e-2572">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="cb43e-2573">Det här kan också användas till att konfigurera chiffer som 3DES och ServerProtocols som Http2 för Frontend för en ApiManagement-tjänst.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2573">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="cb43e-2574">Stöd har lagts till för att konfigurera värdnamnet DeveloperPortal på ApiManagement-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2574">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="cb43e-2575">Uppdaterade cmdletar **Get-AzApiManagementSsoToken** för att ta PsApiManagement-objekt som indata</span><span class="sxs-lookup"><span data-stu-id="cb43e-2575">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="cb43e-2576">Uppdaterad cmdleten för att visa infogade felmeddelanden</span><span class="sxs-lookup"><span data-stu-id="cb43e-2576">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="cb43e-2577">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Felkod: Felmeddelande av typen ValidationError: Ett eller flera fält innehåller felaktiga värden: Felinformation:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="cb43e-2577">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="cb43e-2578">Uppdaterade cmdlet **Export-AzApiManagementApi** för att exportera API:er i OpenApi 3.0-format</span><span class="sxs-lookup"><span data-stu-id="cb43e-2578">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="cb43e-2579">Uppdaterade cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="cb43e-2579">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="cb43e-2580">Importera API från dokumentspecifikationen OpenApi 3.0</span><span class="sxs-lookup"><span data-stu-id="cb43e-2580">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="cb43e-2581">Om du vill åsidosätta egenskapen PsApiManagementSchema specificerad i ett dokument (Swagger, Wadl, Wsdl, OpenApi).</span><span class="sxs-lookup"><span data-stu-id="cb43e-2581">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="cb43e-2582">Åsidosätta egenskapen ServiceUrl som specificeras i ett dokument.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2582">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="cb43e-2583">Uppdaterade cmdlet **Get-AzApiManagementPolicy** för att returnera policy i undantaget format av typen icke-XML med rawxml</span><span class="sxs-lookup"><span data-stu-id="cb43e-2583">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="cb43e-2584">Uppdaterade cmdlet **Set-AzApiManagementPolicy** för att godkänna policy i undantaget format av typen icke-XML med rawxml och XML undantaget med xml</span><span class="sxs-lookup"><span data-stu-id="cb43e-2584">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="cb43e-2585">Uppdaterad cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="cb43e-2585">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="cb43e-2586">Konfigurera API med OpenId auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2586">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="cb43e-2587">Skapa ett API i ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="cb43e-2587">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="cb43e-2588">Klona ett API med SourceApiId och SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2588">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="cb43e-2589">Möjlighet att konfigurera SubscriptionRequired i API-omfattningen.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2589">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="cb43e-2590">Uppdaterad cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="cb43e-2590">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="cb43e-2591">Konfigurera API med OpenId auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2591">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="cb43e-2592">Uppdatera ett API till ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="cb43e-2592">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="cb43e-2593">Möjlighet att konfigurera SubscriptionRequired i API-omfattningen.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2593">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="cb43e-2594">Uppdaterad cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="cb43e-2594">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="cb43e-2595">Klona en befintlig version med hjälp av SourceApiRevision (kopiera taggar, produkter, åtgärder och principer).</span><span class="sxs-lookup"><span data-stu-id="cb43e-2595">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="cb43e-2596">Den nya revisionen antar ApiId från den överordnade instansen.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2596">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="cb43e-2597">Tillhandahålla ApiRevisionDescription</span><span class="sxs-lookup"><span data-stu-id="cb43e-2597">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="cb43e-2598">Åsidosätta ServiceUrl vid kloning av ett API.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2598">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="cb43e-2599">Uppdaterad cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="cb43e-2599">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="cb43e-2600">Konfigurera AAD eller AADB2C med en Authority</span><span class="sxs-lookup"><span data-stu-id="cb43e-2600">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="cb43e-2601">Konfigurera SignupPolicy, SigninPolicy, ProfileEditingPolicy och PasswordResetPolicy</span><span class="sxs-lookup"><span data-stu-id="cb43e-2601">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="cb43e-2602">Uppdaterad cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="cb43e-2602">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="cb43e-2603">Kompensera för ny SubscriptonModel med Scope och UserId</span><span class="sxs-lookup"><span data-stu-id="cb43e-2603">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="cb43e-2604">Kompensera för gammal prenumerationsmodell med ProductId och UserId</span><span class="sxs-lookup"><span data-stu-id="cb43e-2604">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="cb43e-2605">Lägg till funktion för att aktivera AllowTracing på prenumerationsnivå.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2605">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="cb43e-2606">Uppdaterad cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="cb43e-2606">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="cb43e-2607">Kompensera för ny SubscriptonModel med Scope och UserId</span><span class="sxs-lookup"><span data-stu-id="cb43e-2607">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="cb43e-2608">Kompensera för gammal prenumerationsmodell med ProductId och UserId</span><span class="sxs-lookup"><span data-stu-id="cb43e-2608">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="cb43e-2609">Lägg till funktion för att aktivera AllowTracing på prenumerationsnivå.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2609">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="cb43e-2610">Uppdaterade följande cmdletar för att acceptera ResourceId som indata</span><span class="sxs-lookup"><span data-stu-id="cb43e-2610">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="cb43e-2611">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="cb43e-2611">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="cb43e-2612">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="cb43e-2612">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="cb43e-2613">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="cb43e-2613">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="cb43e-2614">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="cb43e-2614">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="cb43e-2615">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="cb43e-2615">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="cb43e-2616">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="cb43e-2616">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="cb43e-2617">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="cb43e-2617">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="cb43e-2618">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="cb43e-2618">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="cb43e-2619">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="cb43e-2619">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="cb43e-2620">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="cb43e-2620">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="cb43e-2621">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="cb43e-2621">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="cb43e-2622">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="cb43e-2622">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cb43e-2623">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cb43e-2623">Az.Automation</span></span>
* <span data-ttu-id="cb43e-2624">Uppdaterade Get-AzAutomationJobOutputRecord för att hantera postvärden av typen JSON och Text.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2624">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="cb43e-2625">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="cb43e-2625">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="cb43e-2626">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="cb43e-2626">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="cb43e-2627">Ändrade beteende för Start-AzAutomationDscCompilationJob till att bara starta jobbet istället för att vänta på slutförandet.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2627">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="cb43e-2628">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="cb43e-2628">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="cb43e-2629">Korrigering för Get-AzAutomationDscNode när using -Name returnerar alla noder.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2629">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="cb43e-2630">Nu returnerar den endast den matchande noden.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2630">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb43e-2631">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb43e-2631">Az.Compute</span></span>
* <span data-ttu-id="cb43e-2632">Lägg till parametrarna ProtectFromScaleIn och ProtectFromScaleSetAction i cmdleten Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2632">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="cb43e-2633">Nu är standardinställningen att vimpelparametern New-AzVM använder en tillgänglig plats om USA, östra inte stöds</span><span class="sxs-lookup"><span data-stu-id="cb43e-2633">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cb43e-2634">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cb43e-2634">Az.DataLakeStore</span></span>
* <span data-ttu-id="cb43e-2635">Uppdatera ADLS-sdk för att använda httpclient, integrera dataplanstestning med Azure-ramverk</span><span class="sxs-lookup"><span data-stu-id="cb43e-2635">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cb43e-2636">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cb43e-2636">Az.Monitor</span></span>
* <span data-ttu-id="cb43e-2637">Korrigera felaktiga parameternamn i hjälpexempel</span><span class="sxs-lookup"><span data-stu-id="cb43e-2637">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb43e-2638">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb43e-2638">Az.Network</span></span>
* <span data-ttu-id="cb43e-2639">Lägg till flaggan DisableBgpRoutePropagation i utdata för effektiv routningstabell</span><span class="sxs-lookup"><span data-stu-id="cb43e-2639">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="cb43e-2640">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="cb43e-2640">Updated cmdlet:</span></span>
        - <span data-ttu-id="cb43e-2641">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="cb43e-2641">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="cb43e-2642">Åtgärda dubbelstreck i dokumentationen New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="cb43e-2642">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb43e-2643">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb43e-2643">Az.Resources</span></span>
* <span data-ttu-id="cb43e-2644">Lägg till ny cmdlet Get-AzureRmDenyAssignment för att hämta tilldelningsnekanden</span><span class="sxs-lookup"><span data-stu-id="cb43e-2644">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb43e-2645">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb43e-2645">Az.Sql</span></span>
* <span data-ttu-id="cb43e-2646">Döp om Advanced Threat Protection-cmdletar för Advanced Data Security och aktivera Vulnerability Assessment som standard</span><span class="sxs-lookup"><span data-stu-id="cb43e-2646">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="cb43e-2647">2.0.0 – maj 2019</span><span class="sxs-lookup"><span data-stu-id="cb43e-2647">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cb43e-2648">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb43e-2648">Az.Accounts</span></span>
* <span data-ttu-id="cb43e-2649">Uppdatera autentiseringsbiblioteket för att åtgärda ADFS-problem med autentisering av användarnamn/lösenord</span><span class="sxs-lookup"><span data-stu-id="cb43e-2649">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="cb43e-2650">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cb43e-2650">Az.CognitiveServices</span></span>
* <span data-ttu-id="cb43e-2651">Visa endast Bing-ansvarsfriskrivning för Bing-sökningstjänster.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2651">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="cb43e-2652">Förbättra felmeddelande när det inte går att skapa konton.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2652">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb43e-2653">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb43e-2653">Az.Compute</span></span>
* <span data-ttu-id="cb43e-2654">Funktion för närhetsplaceringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2654">Proximity placement group feature.</span></span>
    - <span data-ttu-id="cb43e-2655">Följande nya cmdletar har lagts till:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="cb43e-2655">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="cb43e-2656">Den nya parametern ProximityPlacementGroupId har lagts till i följande cmdletar:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="cb43e-2656">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="cb43e-2657">Parametern StorageAccountType har lagts till i New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2657">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="cb43e-2658">TargetRegion för New-AzGalleryImageVersion kan innehålla StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2658">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="cb43e-2659">Växlingsparametern SkipShutdown har lagts till i Stop-AzVM och Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="cb43e-2659">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="cb43e-2660">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="cb43e-2660">Breaking changes</span></span>
    - <span data-ttu-id="cb43e-2661">Set-AzVMBootDiagnostics har ändrats till Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2661">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="cb43e-2662">Export-AzLogAnalyticThrottledRequests har ändrats till Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2662">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="cb43e-2663">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="cb43e-2663">Az.DeploymentManager</span></span>
* <span data-ttu-id="cb43e-2664">De första allmänt tillgängliga versionerna av cmdletar för Distributionshanteraren i Azure</span><span class="sxs-lookup"><span data-stu-id="cb43e-2664">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="cb43e-2665">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="cb43e-2665">Az.Dns</span></span>
* <span data-ttu-id="cb43e-2666">Automatisk delegering av DNS för NameServer</span><span class="sxs-lookup"><span data-stu-id="cb43e-2666">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="cb43e-2667">Det överordnade zonnamnet kan användas som ytterligare valfri parameter i cmdleten för att skapa DNS-zoner.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2667">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="cb43e-2668">Lägger till NS-poster för en nyligen skapad underordnad zon i den överordnade zonen.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2668">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="cb43e-2669">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="cb43e-2669">Az.FrontDoor</span></span>
* <span data-ttu-id="cb43e-2670">De första allmänt tillgängliga versionerna av cmdletar för Azure FrontDoor</span><span class="sxs-lookup"><span data-stu-id="cb43e-2670">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="cb43e-2671">Byt namn på WAF-cmdletar så att de omfattar ”Waf”</span><span class="sxs-lookup"><span data-stu-id="cb43e-2671">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="cb43e-2672">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cb43e-2672">Az.HDInsight</span></span>
* <span data-ttu-id="cb43e-2673">Två cmdletar har tagits bort:</span><span class="sxs-lookup"><span data-stu-id="cb43e-2673">Removed two cmdlets:</span></span>
    - <span data-ttu-id="cb43e-2674">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="cb43e-2674">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="cb43e-2675">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="cb43e-2675">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="cb43e-2676">En ny cmdlet har lagts till, Set-AzHDInsightGatewayCredential, som ersätter Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="cb43e-2676">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="cb43e-2677">Uppdatera cmdleten Get-AzHDInsightJobOutput för att skilja mellan läsarrollen och HDInsight-operatörsrollen:</span><span class="sxs-lookup"><span data-stu-id="cb43e-2677">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="cb43e-2678">Användare med läsarrollen måste uttryckligen ange parametern ”DefaultStorageAccountKey”, annars uppstår fel.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2678">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="cb43e-2679">Användare med HDInsight-operatörsrollen påverkas inte.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2679">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cb43e-2680">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cb43e-2680">Az.Monitor</span></span>
* <span data-ttu-id="cb43e-2681">Nya cmdletar för SQR API (schemalagd frågeregel)</span><span class="sxs-lookup"><span data-stu-id="cb43e-2681">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="cb43e-2682">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="cb43e-2682">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="cb43e-2683">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="cb43e-2683">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="cb43e-2684">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="cb43e-2684">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="cb43e-2685">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="cb43e-2685">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="cb43e-2686">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="cb43e-2686">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="cb43e-2687">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="cb43e-2687">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="cb43e-2688">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="cb43e-2688">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="cb43e-2689">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="cb43e-2689">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="cb43e-2690">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="cb43e-2690">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="cb43e-2691">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="cb43e-2691">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="cb43e-2692">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="cb43e-2692">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="cb43e-2693">[Mer](/rest/api/monitor/scheduledqueryrules) information om SQR API</span><span class="sxs-lookup"><span data-stu-id="cb43e-2693">[More](/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="cb43e-2694">Az.Monitor.md har uppdaterats för att omfatta cmdletar för måttbaserade aviseringsregler i GenV2 (inte klassiska)</span><span class="sxs-lookup"><span data-stu-id="cb43e-2694">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb43e-2695">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb43e-2695">Az.Network</span></span>
* <span data-ttu-id="cb43e-2696">Lägg till stöd för NAT Gateway-resurs</span><span class="sxs-lookup"><span data-stu-id="cb43e-2696">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="cb43e-2697">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="cb43e-2697">New cmdlets</span></span>
        - <span data-ttu-id="cb43e-2698">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="cb43e-2698">New-AzNatGateway</span></span>
        - <span data-ttu-id="cb43e-2699">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="cb43e-2699">Get-AzNatGateway</span></span>
        - <span data-ttu-id="cb43e-2700">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="cb43e-2700">Set-AzNatGateway</span></span>
        - <span data-ttu-id="cb43e-2701">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="cb43e-2701">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="cb43e-2702">Uppdaterade cmdletar</span><span class="sxs-lookup"><span data-stu-id="cb43e-2702">Updated cmdlets</span></span>
        - <span data-ttu-id="cb43e-2703">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="cb43e-2703">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="cb43e-2704">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="cb43e-2704">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="cb43e-2705">Nedanstående kommandon för funktionen har uppdaterats: Ange/ta bort anpassade vägar på Brooklyn Gateway.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2705">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="cb43e-2706">New-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ställa in adressprefix som anpassade vägar för att ange gateway.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2706">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="cb43e-2707">Set-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ange adressprefix som anpassade vägar för att ange gateway.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2707">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="cb43e-2708">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="cb43e-2708">Az.PolicyInsights</span></span>
* <span data-ttu-id="cb43e-2709">Stöd för att fråga efter information om principutvärdering.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2709">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="cb43e-2710">Lägg till parametern ”-Expand” för Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2710">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="cb43e-2711">Stöd för -Expand PolicyEvaluationDetails.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2711">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cb43e-2712">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb43e-2712">Az.RecoveryServices</span></span>
* <span data-ttu-id="cb43e-2713">Stöd för att dela prenumeration mellan Azure och Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2713">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="cb43e-2714">Markering av kommande icke-bakåtkompatibla ändringar för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2714">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="cb43e-2715">Korrigering för återställningsplan och åtgärdsplan i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2715">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="cb43e-2716">Korrigering för mappning av uppdateringsnätverk i Azure Site Recovery för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2716">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="cb43e-2717">Korrigering för instruktioner för uppdateringsskydd i Azure Site Recovery för Azure till Azure för hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2717">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="cb43e-2718">Andra mindre korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2718">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="cb43e-2719">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="cb43e-2719">Az.Relay</span></span>
* <span data-ttu-id="cb43e-2720">Korrigera stavfel i kundriktade meddelanden</span><span class="sxs-lookup"><span data-stu-id="cb43e-2720">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="cb43e-2721">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="cb43e-2721">Az.ServiceBus</span></span>
* <span data-ttu-id="cb43e-2722">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="cb43e-2722">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cb43e-2723">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb43e-2723">Az.Storage</span></span>
* <span data-ttu-id="cb43e-2724">Uppgradera till lagringsklientbiblioteket 10.0.1 (namnområdet för alla objekt från detta SDK ändras från ”Microsoft.WindowsAzure.Storage. *till ”Microsoft.Azure.Storage.* ”)</span><span class="sxs-lookup"><span data-stu-id="cb43e-2724">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="cb43e-2725">Uppgradera till Microsoft.Azure.Management.Storage 11.0.0 för att stödja den nya API-versionen 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2725">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="cb43e-2726">Standardlagringskontot i Skapa lagringskonto ändras från ”Storage” till ”StorageV2”</span><span class="sxs-lookup"><span data-stu-id="cb43e-2726">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="cb43e-2727">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cb43e-2727">New-AzStorageAccount</span></span>
* <span data-ttu-id="cb43e-2728">Ändra lagringskontots cmdlet-utdata Sku.Name för att passa med indata-SkuName genom att lägga till ”-”. Till exempel ändras ”StandardLRS” till ”Standard_LRS”</span><span class="sxs-lookup"><span data-stu-id="cb43e-2728">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="cb43e-2729">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cb43e-2729">New-AzStorageAccount</span></span>
    - <span data-ttu-id="cb43e-2730">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cb43e-2730">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="cb43e-2731">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cb43e-2731">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cb43e-2732">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb43e-2732">Az.Websites</span></span>
* <span data-ttu-id="cb43e-2733">Egenskapen ”typ” konfigureras nu för PSSite-objekt som returneras av Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="cb43e-2733">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="cb43e-2734">Get-AzWebApp\*Metrics och Get-AzAppServicePlanMetrics markeras som inaktuella</span><span class="sxs-lookup"><span data-stu-id="cb43e-2734">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="cb43e-2735">1.8.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="cb43e-2735">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="cb43e-2736">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="cb43e-2736">Highlights since the last major release</span></span>
* <span data-ttu-id="cb43e-2737">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="cb43e-2737">General availability of `Az` module</span></span>
* <span data-ttu-id="cb43e-2738">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="cb43e-2738">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="cb43e-2739">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="cb43e-2739">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="cb43e-2740">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-2740">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="cb43e-2741">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-2741">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="cb43e-2742">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-2742">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="cb43e-2743">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="cb43e-2743">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="cb43e-2744">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb43e-2744">Az.Accounts</span></span>
* <span data-ttu-id="cb43e-2745">Uppdatera Uninstall-AzureRm för att ta bort moduler i Mac på ett korrekt sätt</span><span class="sxs-lookup"><span data-stu-id="cb43e-2745">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="cb43e-2746">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="cb43e-2746">Az.Batch</span></span>
* <span data-ttu-id="cb43e-2747">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2747">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="cb43e-2748">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="cb43e-2748">Az.Cdn</span></span>
* <span data-ttu-id="cb43e-2749">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2749">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="cb43e-2750">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cb43e-2750">Az.CognitiveServices</span></span>
* <span data-ttu-id="cb43e-2751">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2751">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb43e-2752">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb43e-2752">Az.Compute</span></span>
* <span data-ttu-id="cb43e-2753">Åtgärda problem med AEM-installationen om resurs-ID:n för diskar innehåller resourcegroups i gemener i resurs-ID:n</span><span class="sxs-lookup"><span data-stu-id="cb43e-2753">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="cb43e-2754">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2754">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="cb43e-2755">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="cb43e-2755">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cb43e-2756">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cb43e-2756">Az.DataFactory</span></span>
* <span data-ttu-id="cb43e-2757">Lägg till SsisProperties om NodeCount inte är null för hanterad integreringskörning.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2757">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cb43e-2758">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cb43e-2758">Az.DataLakeStore</span></span>
* <span data-ttu-id="cb43e-2759">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2759">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="cb43e-2760">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="cb43e-2760">Az.EventGrid</span></span>
* <span data-ttu-id="cb43e-2761">Hjälptexten för slutpunkten har uppdaterats för att visa att resurser ska skapas innan cmdletarna för att skapa/uppdatera händelseprenumerationer används.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2761">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="cb43e-2762">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="cb43e-2762">Az.EventHub</span></span>
* <span data-ttu-id="cb43e-2763">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="cb43e-2763">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="cb43e-2764">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cb43e-2764">Az.HDInsight</span></span>
* <span data-ttu-id="cb43e-2765">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2765">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cb43e-2766">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cb43e-2766">Az.IotHub</span></span>
* <span data-ttu-id="cb43e-2767">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2767">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cb43e-2768">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cb43e-2768">Az.KeyVault</span></span>
* <span data-ttu-id="cb43e-2769">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2769">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="cb43e-2770">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="cb43e-2770">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="cb43e-2771">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="cb43e-2771">Az.MachineLearning</span></span>
* <span data-ttu-id="cb43e-2772">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2772">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="cb43e-2773">Az.Media</span><span class="sxs-lookup"><span data-stu-id="cb43e-2773">Az.Media</span></span>
* <span data-ttu-id="cb43e-2774">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2774">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cb43e-2775">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cb43e-2775">Az.Monitor</span></span>
  * <span data-ttu-id="cb43e-2776">Nya cmdletar för måttbaserad aviseringsregel i GenV2 (inte klassisk)</span><span class="sxs-lookup"><span data-stu-id="cb43e-2776">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="cb43e-2777">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="cb43e-2777">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="cb43e-2778">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="cb43e-2778">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="cb43e-2779">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="cb43e-2779">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="cb43e-2780">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="cb43e-2780">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="cb43e-2781">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="cb43e-2781">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="cb43e-2782">Monitor SDK har uppdaterats till version 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="cb43e-2782">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb43e-2783">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb43e-2783">Az.Network</span></span>
* <span data-ttu-id="cb43e-2784">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2784">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="cb43e-2785">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="cb43e-2785">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="cb43e-2786">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="cb43e-2786">Az.NotificationHubs</span></span>
* <span data-ttu-id="cb43e-2787">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2787">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="cb43e-2788">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cb43e-2788">Az.OperationalInsights</span></span>
* <span data-ttu-id="cb43e-2789">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2789">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="cb43e-2790">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="cb43e-2790">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="cb43e-2791">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2791">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cb43e-2792">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb43e-2792">Az.RecoveryServices</span></span>
* <span data-ttu-id="cb43e-2793">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2793">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="cb43e-2794">Tabellformatet för SQL i virtuella Azure-datorer har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="cb43e-2794">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="cb43e-2795">En alternativ metod för att hämta platser i AzureFileShare har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-2795">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="cb43e-2796">ScheduleRunDays i SchedulePolicy-objekt har uppdaterats enligt tidszon</span><span class="sxs-lookup"><span data-stu-id="cb43e-2796">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="cb43e-2797">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="cb43e-2797">Az.RedisCache</span></span>
* <span data-ttu-id="cb43e-2798">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2798">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb43e-2799">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb43e-2799">Az.Resources</span></span>
* <span data-ttu-id="cb43e-2800">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="cb43e-2800">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb43e-2801">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb43e-2801">Az.Sql</span></span>
* <span data-ttu-id="cb43e-2802">Ersätt Monitor SDK-beroende med vanlig kod</span><span class="sxs-lookup"><span data-stu-id="cb43e-2802">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="cb43e-2803">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2803">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="cb43e-2804">Förbättrad process för klassificering av flera kolumner.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2804">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="cb43e-2805">Inkludera SKU-egenskaper (SKU-namn, serie, kapacitet) i svaret från Get-AzSqlServerServiceObjective och formatera som tabell som standard.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2805">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="cb43e-2806">Möjlighet att använda Get-AzSqlServerServiceObjective efter plats utan att behöva en redan befintlig server i regionen.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2806">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="cb43e-2807">Stöd för tidszonsparametern när hanterade instanser skapas.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2807">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="cb43e-2808">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="cb43e-2808">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cb43e-2809">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb43e-2809">Az.Websites</span></span>
* <span data-ttu-id="cb43e-2810">åtgärdar Set-AzWebApp och Set-AzWebAppSlot så att de inte tar bort taggar vid körning</span><span class="sxs-lookup"><span data-stu-id="cb43e-2810">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="cb43e-2811">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2811">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="cb43e-2812">SDK för WebSites har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2812">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="cb43e-2813">Egenskapen AdminSiteName har tagits bort från PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2813">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="cb43e-2814">1.7.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="cb43e-2814">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="cb43e-2815">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="cb43e-2815">Highlights since the last major release</span></span>
* <span data-ttu-id="cb43e-2816">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="cb43e-2816">General availability of `Az` module</span></span>
* <span data-ttu-id="cb43e-2817">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="cb43e-2817">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="cb43e-2818">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="cb43e-2818">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="cb43e-2819">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-2819">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="cb43e-2820">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-2820">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="cb43e-2821">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-2821">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="cb43e-2822">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="cb43e-2822">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="cb43e-2823">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb43e-2823">Az.Accounts</span></span>
* <span data-ttu-id="cb43e-2824">Add-AzEnvironment och Set-AzEnvironment har uppdaterats för att godkänna parametern AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="cb43e-2824">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="cb43e-2825">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="cb43e-2825">Az.AnalysisServices</span></span>
* <span data-ttu-id="cb43e-2826">ServiceClient används i cmdletar för dataplan och den ursprungliga autentiseringslogiken har tagits bort</span><span class="sxs-lookup"><span data-stu-id="cb43e-2826">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="cb43e-2827">Add-AzureASAccount används för omslutning av Connect-AzAccount för att undvika en icke-bakåtkompatibel ändring</span><span class="sxs-lookup"><span data-stu-id="cb43e-2827">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cb43e-2828">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cb43e-2828">Az.Automation</span></span>
* <span data-ttu-id="cb43e-2829">Buggen för cmdleten New-AzAutomationSoftwareUpdateConfiguration för inkluderingar har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2829">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="cb43e-2830">Nu bör parametern IncludedKbNumber och IncludedPackageNameMask fungera.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2830">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="cb43e-2831">Felkorrigering för dynamiska grupper i uppdateringshanteringen för azure automation</span><span class="sxs-lookup"><span data-stu-id="cb43e-2831">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb43e-2832">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb43e-2832">Az.Compute</span></span>
* <span data-ttu-id="cb43e-2833">Lägg till parametern HyperVGeneration i New-AzDiskConfig och New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="cb43e-2833">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="cb43e-2834">Tillåt att virtuella datorer skapas med galleribilder från andra klientorganisationer.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2834">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="cb43e-2835">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="cb43e-2835">Az.ContainerInstance</span></span>
* <span data-ttu-id="cb43e-2836">Ett problem har åtgärdats i parametern -Command för New-AzContainerGroup som lade till ett avslutande tomt argument</span><span class="sxs-lookup"><span data-stu-id="cb43e-2836">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cb43e-2837">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cb43e-2837">Az.DataFactory</span></span>
* <span data-ttu-id="cb43e-2838">ADF .Net SDK-versionen har uppdaterats till 3.0.2</span><span class="sxs-lookup"><span data-stu-id="cb43e-2838">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="cb43e-2839">Cmdleten Set-AzDataFactoryV2 har uppdaterats med extra parametrar för inställningar som rör RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2839">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb43e-2840">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb43e-2840">Az.Resources</span></span>
* <span data-ttu-id="cb43e-2841">Förbättra hanteringen av providrar för Get-AzResource när parametrarna -ResourceId eller -ResourceGroupName, -Name och -ResourceType tillhandahålls</span><span class="sxs-lookup"><span data-stu-id="cb43e-2841">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="cb43e-2842">Förbättra felhanteringen för ”Test-AzDeployment” och ”Test-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="cb43e-2842">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="cb43e-2843">Hantera fel utanför distributionsvalideringen och ta med dem i kommandoutdata istället</span><span class="sxs-lookup"><span data-stu-id="cb43e-2843">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="cb43e-2844">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="cb43e-2844">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="cb43e-2845">Lägg till växlingsparametern -IgnoreDynamicParameters till en uppsättning av cmdletar för distribution för att hoppa över fråga i skript och jobbscenarier</span><span class="sxs-lookup"><span data-stu-id="cb43e-2845">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="cb43e-2846">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="cb43e-2846">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb43e-2847">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb43e-2847">Az.Sql</span></span>
* <span data-ttu-id="cb43e-2848">Stöd för dataklassificering av databaser.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2848">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cb43e-2849">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb43e-2849">Az.Storage</span></span>
* <span data-ttu-id="cb43e-2850">Rapportera detaljfel när lagringskontext skapas med parametern -UseConnectedAccount, men utan inloggning på Azure-kontot</span><span class="sxs-lookup"><span data-stu-id="cb43e-2850">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="cb43e-2851">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="cb43e-2851">New-AzStorageContext</span></span>
* <span data-ttu-id="cb43e-2852">Stöd för att hantera Blob Service-egenskaper för ett angivet lagringskonto med API:et för hanteringsplan</span><span class="sxs-lookup"><span data-stu-id="cb43e-2852">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="cb43e-2853">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="cb43e-2853">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="cb43e-2854">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="cb43e-2854">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="cb43e-2855">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="cb43e-2855">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="cb43e-2856">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="cb43e-2856">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="cb43e-2857">Stöd för -AsJob-cmdletar för att ladda upp och ladda ned blobar och filer</span><span class="sxs-lookup"><span data-stu-id="cb43e-2857">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="cb43e-2858">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="cb43e-2858">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="cb43e-2859">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="cb43e-2859">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="cb43e-2860">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="cb43e-2860">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="cb43e-2861">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="cb43e-2861">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="cb43e-2862">1.6.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="cb43e-2862">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="cb43e-2863">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="cb43e-2863">Highlights since the last major release</span></span>
* <span data-ttu-id="cb43e-2864">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="cb43e-2864">General availability of `Az` module</span></span>
* <span data-ttu-id="cb43e-2865">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="cb43e-2865">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="cb43e-2866">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="cb43e-2866">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="cb43e-2867">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-2867">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="cb43e-2868">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-2868">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="cb43e-2869">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-2869">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="cb43e-2870">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="cb43e-2870">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cb43e-2871">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cb43e-2871">Az.Automation</span></span>
* <span data-ttu-id="cb43e-2872">Azure Automation – ändring av uppdateringshantering för stöd för de nya funktionerna:</span><span class="sxs-lookup"><span data-stu-id="cb43e-2872">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="cb43e-2873">Dynamisk gruppering</span><span class="sxs-lookup"><span data-stu-id="cb43e-2873">Dynamic grouping</span></span>
    * <span data-ttu-id="cb43e-2874">För-/efterskrift</span><span class="sxs-lookup"><span data-stu-id="cb43e-2874">Pre-Post script</span></span>
    * <span data-ttu-id="cb43e-2875">Inställning för omstart</span><span class="sxs-lookup"><span data-stu-id="cb43e-2875">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb43e-2876">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb43e-2876">Az.Compute</span></span>
* <span data-ttu-id="cb43e-2877">Åtgärda problem med sökvägsmatchning i Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="cb43e-2877">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="cb43e-2878">Uppdatera Compute-klientbibliotek till 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2878">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cb43e-2879">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cb43e-2879">Az.KeyVault</span></span>
* <span data-ttu-id="cb43e-2880">Stöd för jokertecken för KeyVault-cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-2880">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb43e-2881">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb43e-2881">Az.Network</span></span>
* <span data-ttu-id="cb43e-2882">Lägg till stöd för Threat Intelligence för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="cb43e-2882">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="cb43e-2883">Lägg till resurs för brandväggsprincip på översta nivå och anpassade regler för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="cb43e-2883">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cb43e-2884">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb43e-2884">Az.RecoveryServices</span></span>
* <span data-ttu-id="cb43e-2885">SnapshotRetentionInDays har lagts till i Azure-principen för virtuella datorer för stöd av Instant RP</span><span class="sxs-lookup"><span data-stu-id="cb43e-2885">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="cb43e-2886">Pipe-stöd för avregistrering av container har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-2886">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb43e-2887">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb43e-2887">Az.Resources</span></span>
* <span data-ttu-id="cb43e-2888">Uppdatera stöd för jokertecken för Get-AzResource och Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="cb43e-2888">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="cb43e-2889">Uppdatera autentiseringsuppgifter som används vid allmänna anrop till ARM</span><span class="sxs-lookup"><span data-stu-id="cb43e-2889">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb43e-2890">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb43e-2890">Az.Sql</span></span>
* <span data-ttu-id="cb43e-2891">Cmdlet-parametern (ExcludeDetectionType) för Hotidentifiering ändrades från DetectionType till sträng[] för att framtidssäkra den när nya DetectionTypes läggs till, och även för att stödja automatisk ifyllning.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2891">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cb43e-2892">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb43e-2892">Az.Storage</span></span>
* <span data-ttu-id="cb43e-2893">Stöd för att hämta/ange/ta bort hanteringsprincip på ett lagringskonto</span><span class="sxs-lookup"><span data-stu-id="cb43e-2893">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="cb43e-2894">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="cb43e-2894">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="cb43e-2895">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="cb43e-2895">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="cb43e-2896">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="cb43e-2896">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="cb43e-2897">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="cb43e-2897">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="cb43e-2898">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="cb43e-2898">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="cb43e-2899">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="cb43e-2899">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cb43e-2900">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb43e-2900">Az.Websites</span></span>
* <span data-ttu-id="cb43e-2901">Åtgärda fel med ARM-mall som avbryter kloning av alla platser med 'New-AzWebApp -IncludeSourceWebAppSlots'</span><span class="sxs-lookup"><span data-stu-id="cb43e-2901">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="cb43e-2902">1.5.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="cb43e-2902">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cb43e-2903">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb43e-2903">Az.Accounts</span></span>
* <span data-ttu-id="cb43e-2904">Lägg till kommandot Register-AzModule för stöd för AutoRest-genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="cb43e-2904">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="cb43e-2905">Uppdatera exempel för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="cb43e-2905">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cb43e-2906">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cb43e-2906">Az.Automation</span></span>
* <span data-ttu-id="cb43e-2907">Problem med att hämta vissa månadsscheman i flera Azure Automation-cmdletar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="cb43e-2907">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="cb43e-2908">Åtgärda problem med att Get-AzAutomationDscNode bara returnerar de 20 översta noderna.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2908">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="cb43e-2909">Nu returneras alla noder</span><span class="sxs-lookup"><span data-stu-id="cb43e-2909">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="cb43e-2910">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="cb43e-2910">Az.Cdn</span></span>
* <span data-ttu-id="cb43e-2911">Nya Powershell-cmdletar för att aktivera/inaktivera anpassade domän-HTTPS har lagts till och de gamla har gjorts inaktuella</span><span class="sxs-lookup"><span data-stu-id="cb43e-2911">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb43e-2912">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb43e-2912">Az.Compute</span></span>
* <span data-ttu-id="cb43e-2913">Lägg till stöd för jokertecken för Get-cmdletar</span><span class="sxs-lookup"><span data-stu-id="cb43e-2913">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cb43e-2914">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cb43e-2914">Az.DataFactory</span></span>
* <span data-ttu-id="cb43e-2915">ADF .Net SDK-versionen har uppdaterats till 3.0.1</span><span class="sxs-lookup"><span data-stu-id="cb43e-2915">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="cb43e-2916">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="cb43e-2916">Az.LogicApp</span></span>
* <span data-ttu-id="cb43e-2917">Åtgärda problemet med att ListWorkflows endast hämtar den första sidan med resultat</span><span class="sxs-lookup"><span data-stu-id="cb43e-2917">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb43e-2918">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb43e-2918">Az.Network</span></span>
* <span data-ttu-id="cb43e-2919">Lägg till stöd för jokertecken för Network-cmdletar</span><span class="sxs-lookup"><span data-stu-id="cb43e-2919">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cb43e-2920">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb43e-2920">Az.RecoveryServices</span></span>
* <span data-ttu-id="cb43e-2921">Stöd har lagts till för SQL Server i virtuella Azure-datorer</span><span class="sxs-lookup"><span data-stu-id="cb43e-2921">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="cb43e-2922">SDK-uppdatering</span><span class="sxs-lookup"><span data-stu-id="cb43e-2922">SDK Update</span></span>
* <span data-ttu-id="cb43e-2923">Get-ProtectableItem-incheckning i VMappContainer har tagits bort</span><span class="sxs-lookup"><span data-stu-id="cb43e-2923">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="cb43e-2924">Name och ServerName har lagts till som parametrar för Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="cb43e-2924">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb43e-2925">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb43e-2925">Az.Resources</span></span>
* <span data-ttu-id="cb43e-2926">Lägg till parametern `-TemplateObject` i cmdletar för distribution</span><span class="sxs-lookup"><span data-stu-id="cb43e-2926">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="cb43e-2927">Mer information här: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="cb43e-2927">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="cb43e-2928">Åtgärda problem med piping av resultatet i `Get-AzResource` till `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="cb43e-2928">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="cb43e-2929">Mer information här: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="cb43e-2929">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="cb43e-2930">Åtgärda problem med ändring av JSON-datatyp när `Set-AzResource` körs</span><span class="sxs-lookup"><span data-stu-id="cb43e-2930">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="cb43e-2931">Mer information här: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="cb43e-2931">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb43e-2932">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb43e-2932">Az.Sql</span></span>
* <span data-ttu-id="cb43e-2933">AuditingEndpointsCommunicator uppdateras.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2933">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="cb43e-2934">Åtgärdar beteendet hos ett gränsscenario när nya diagnostikinställningar skapas.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2934">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cb43e-2935">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb43e-2935">Az.Storage</span></span>
* <span data-ttu-id="cb43e-2936">Stöd för BlockBlobStorage när Storage-konto skapas      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cb43e-2936">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="cb43e-2937">1.4.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="cb43e-2937">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="cb43e-2938">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="cb43e-2938">Az.AnalysisServices</span></span>
* <span data-ttu-id="cb43e-2939">Inaktuell AddAzureASAccount-cmdlet</span><span class="sxs-lookup"><span data-stu-id="cb43e-2939">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cb43e-2940">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cb43e-2940">Az.Automation</span></span>
* <span data-ttu-id="cb43e-2941">Hjälpen för Import-AzAutomationDscNodeConfiguration har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="cb43e-2941">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="cb43e-2942">Konfigurationsnamnsvalidering har lagts till i cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb43e-2942">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="cb43e-2943">Förbättrad felhantering för cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb43e-2943">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="cb43e-2944">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cb43e-2944">Az.CognitiveServices</span></span>
* <span data-ttu-id="cb43e-2945">CustomSubdomainName har lagts till som en ny valfri parameter för New-AzCognitiveServicesAccount, som används för att ange underdomän för resursen.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2945">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb43e-2946">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb43e-2946">Az.Compute</span></span>
* <span data-ttu-id="cb43e-2947">Problemet med ID-parameteruppsättningar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="cb43e-2947">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="cb43e-2948">Get-AzVMExtension har uppdaterats så att alla installerade tillägg visas om parametern Name inte har angetts</span><span class="sxs-lookup"><span data-stu-id="cb43e-2948">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="cb43e-2949">Parametrarna Tag och ResourceId har lagts till i cmdleten Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="cb43e-2949">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="cb43e-2950">Get-AzVmssVM utan instans-ID och med InstanceView kan visa virtuella VMSS-datorer med instansvyn.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2950">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cb43e-2951">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cb43e-2951">Az.DataLakeStore</span></span>
* <span data-ttu-id="cb43e-2952">Cmdletar har lagts till för uppräkning och återställning av borttagna objekt i ADL</span><span class="sxs-lookup"><span data-stu-id="cb43e-2952">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="cb43e-2953">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="cb43e-2953">Az.EventHub</span></span>
* <span data-ttu-id="cb43e-2954">Ny boolesk egenskap SkipEmptyArchives har lagts till i Skip Empty Archives i CaptureDescription-klassen i Eventhub</span><span class="sxs-lookup"><span data-stu-id="cb43e-2954">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cb43e-2955">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cb43e-2955">Az.KeyVault</span></span>
* <span data-ttu-id="cb43e-2956">Taggning i Set-AzKeyVaultSecret har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="cb43e-2956">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="cb43e-2957">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="cb43e-2957">Az.LogicApp</span></span>
* <span data-ttu-id="cb43e-2958">Grundläggande SKU har lagts till för Integrationskonton</span><span class="sxs-lookup"><span data-stu-id="cb43e-2958">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="cb43e-2959">XSLT 2.0, XSLT 3.0 och Flytande mappningstyper har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-2959">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="cb43e-2960">Nya cmdletar för integrationskontosammansättningar</span><span class="sxs-lookup"><span data-stu-id="cb43e-2960">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="cb43e-2961">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="cb43e-2961">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="cb43e-2962">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="cb43e-2962">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="cb43e-2963">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="cb43e-2963">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="cb43e-2964">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="cb43e-2964">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="cb43e-2965">Nya cmdletar för batchkonfiguration för integrationskonto</span><span class="sxs-lookup"><span data-stu-id="cb43e-2965">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="cb43e-2966">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb43e-2966">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="cb43e-2967">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb43e-2967">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="cb43e-2968">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb43e-2968">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="cb43e-2969">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb43e-2969">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="cb43e-2970">Logic App-SDK har uppdaterats till version 4.1.0</span><span class="sxs-lookup"><span data-stu-id="cb43e-2970">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cb43e-2971">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cb43e-2971">Az.Monitor</span></span>
* <span data-ttu-id="cb43e-2972">Hjälpen för Get-AzMetric har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="cb43e-2972">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb43e-2973">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb43e-2973">Az.Network</span></span>
* <span data-ttu-id="cb43e-2974">Hjälpexempel för Add-AzApplicationGatewayCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-2974">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="cb43e-2975">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cb43e-2975">Az.OperationalInsights</span></span>
* <span data-ttu-id="cb43e-2976">Ytterligare stöd för datakällorna New och Get ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2976">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="cb43e-2977">Ny ApplicationInsights-typ har lagts till för att ge stöd för ”Get specific” och ”Get all” för ApplicationInsights-datakällor för angiven arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2977">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="cb43e-2978">Cmdleten New-AzOperationalInsightsApplicationInsightsDataSource har lagts till för att skapa datakälla med angivna parametrar för Application Insights-resurs: subscription Id, resourceGroupName och name.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2978">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb43e-2979">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb43e-2979">Az.Resources</span></span>
* <span data-ttu-id="cb43e-2980">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="cb43e-2980">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="cb43e-2981">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="cb43e-2981">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="cb43e-2982">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="cb43e-2982">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="cb43e-2983">Fel som gör att KeyCredentials inte kan skapas upprepade gånger har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="cb43e-2983">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb43e-2984">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb43e-2984">Az.Sql</span></span>
* <span data-ttu-id="cb43e-2985">Lägg till stöd för hyperskalanivån för SQL DB</span><span class="sxs-lookup"><span data-stu-id="cb43e-2985">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="cb43e-2986">Ett fel har åtgärdats där återställningen kunde misslyckas på grund av onödiga inställningsegenskaper i restore-förfrågan</span><span class="sxs-lookup"><span data-stu-id="cb43e-2986">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cb43e-2987">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb43e-2987">Az.Websites</span></span>
* <span data-ttu-id="cb43e-2988">Rätt exempel i Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="cb43e-2988">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="cb43e-2989">1.3.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="cb43e-2989">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cb43e-2990">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb43e-2990">Az.Accounts</span></span>
* <span data-ttu-id="cb43e-2991">Uppdatera till den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="cb43e-2991">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="cb43e-2992">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="cb43e-2992">Az.AnalysisServices</span></span>
<span data-ttu-id="cb43e-2993">Allmän tillgänglighet för Az.AnalysisServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2993">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb43e-2994">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb43e-2994">Az.Compute</span></span>
* <span data-ttu-id="cb43e-2995">AEM-tillägg: Lägg till stöd för UltraSSD-, P60-, P70- och P80-diskar</span><span class="sxs-lookup"><span data-stu-id="cb43e-2995">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="cb43e-2996">Uppdatera hjälpbeskrivning för Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="cb43e-2996">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="cb43e-2997">Uppdatera hjälpbeskrivning och exempel för Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="cb43e-2997">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cb43e-2998">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb43e-2998">Az.RecoveryServices</span></span>
<span data-ttu-id="cb43e-2999">Allmän tillgänglighet för Az.RecoveryServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="cb43e-2999">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb43e-3000">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb43e-3000">Az.Resources</span></span>
* <span data-ttu-id="cb43e-3001">Korrigera taggar för resursgrupper</span><span class="sxs-lookup"><span data-stu-id="cb43e-3001">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="cb43e-3002">Mer information här: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="cb43e-3002">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="cb43e-3003">Åtgärda problem där `Get-AzureRmRoleAssignment` inte respekterar -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="cb43e-3003">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="cb43e-3004">Mer information här: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="cb43e-3004">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb43e-3005">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb43e-3005">Az.Sql</span></span>
* <span data-ttu-id="cb43e-3006">Lägga till Get/Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="cb43e-3006">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="cb43e-3007">Åtgärda problem där ett nullref-undantag uppstår när du kör SQL-cmdletar och inte är inloggad på ett Azure-konto</span><span class="sxs-lookup"><span data-stu-id="cb43e-3007">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="cb43e-3008">Åtgärda nullref-undantag i Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="cb43e-3008">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="cb43e-3009">1.2.1 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="cb43e-3009">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cb43e-3010">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb43e-3010">Az.Accounts</span></span>
* <span data-ttu-id="cb43e-3011">Version med rätt version av autentisering</span><span class="sxs-lookup"><span data-stu-id="cb43e-3011">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="cb43e-3012">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="cb43e-3012">Az.AnalysisServices</span></span>
* <span data-ttu-id="cb43e-3013">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="cb43e-3013">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cb43e-3014">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb43e-3014">Az.RecoveryServices</span></span>
* <span data-ttu-id="cb43e-3015">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="cb43e-3015">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="cb43e-3016">1.2.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="cb43e-3016">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cb43e-3017">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb43e-3017">Az.Accounts</span></span>
* <span data-ttu-id="cb43e-3018">Lägga till interaktiv autentisering och autentisering med användarnamn/lösenord för endast Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="cb43e-3018">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="cb43e-3019">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="cb43e-3019">Update incorrect online help URLs</span></span>
* <span data-ttu-id="cb43e-3020">Lägga till varningsmeddelande i PS Core för Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="cb43e-3020">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="cb43e-3021">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="cb43e-3021">Az.Aks</span></span>
* <span data-ttu-id="cb43e-3022">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="cb43e-3022">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cb43e-3023">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cb43e-3023">Az.Automation</span></span>
* <span data-ttu-id="cb43e-3024">Stöd för Python 2-runbookflöden har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-3024">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="cb43e-3025">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="cb43e-3025">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="cb43e-3026">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="cb43e-3026">Az.Cdn</span></span>
* <span data-ttu-id="cb43e-3027">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="cb43e-3027">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb43e-3028">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb43e-3028">Az.Compute</span></span>
* <span data-ttu-id="cb43e-3029">Lägga till cmdleten Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="cb43e-3029">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="cb43e-3030">Lägga till TempDisk-parameter i Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="cb43e-3030">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="cb43e-3031">Korrigera varningsmeddelande för New-AzVM</span><span class="sxs-lookup"><span data-stu-id="cb43e-3031">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="cb43e-3032">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="cb43e-3032">Az.ContainerRegistry</span></span>
* <span data-ttu-id="cb43e-3033">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="cb43e-3033">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cb43e-3034">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cb43e-3034">Az.DataFactory</span></span>
* <span data-ttu-id="cb43e-3035">ADF .Net SDK-versionen har uppdaterats till 3.0.0</span><span class="sxs-lookup"><span data-stu-id="cb43e-3035">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cb43e-3036">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cb43e-3036">Az.DataLakeStore</span></span>
* <span data-ttu-id="cb43e-3037">Åtgärda problem med ADLS-slutpunkt vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="cb43e-3037">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="cb43e-3038">Mer information här: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="cb43e-3038">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="cb43e-3039">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="cb43e-3039">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cb43e-3040">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cb43e-3040">Az.IotHub</span></span>
* <span data-ttu-id="cb43e-3041">Lägga till kodningsformat i cmdleten Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="cb43e-3041">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cb43e-3042">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cb43e-3042">Az.KeyVault</span></span>
* <span data-ttu-id="cb43e-3043">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="cb43e-3043">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb43e-3044">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb43e-3044">Az.Network</span></span>
* <span data-ttu-id="cb43e-3045">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="cb43e-3045">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb43e-3046">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb43e-3046">Az.Resources</span></span>
* <span data-ttu-id="cb43e-3047">Åtgärda felaktiga exempel i referensdokumentationen ”New-AzADAppCredential” och ”New-AzADSpCredential”</span><span class="sxs-lookup"><span data-stu-id="cb43e-3047">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="cb43e-3048">Åtgärda problem där sökvägen för parametern ”-TemplateFile” inte omvandlas innan cmdletarna för distribution i resursgruppen körs</span><span class="sxs-lookup"><span data-stu-id="cb43e-3048">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="cb43e-3049">Az.Resources: Korrigera dokumentationen om standardvärdet för New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="cb43e-3049">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="cb43e-3050">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="cb43e-3050">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="cb43e-3051">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="cb43e-3051">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="cb43e-3052">Åtgärda formateringsproblemet med objektet ”PSResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="cb43e-3052">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="cb43e-3053">Mer information här: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="cb43e-3053">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="cb43e-3054">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cb43e-3054">Az.ServiceFabric</span></span>
* <span data-ttu-id="cb43e-3055">Återställ när ett certifikat läggs till i en Virtual Machine Scale Sets-modell men ett undantag genereras. Detta har gjorts för att åtgärda följande fel: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="cb43e-3055">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="cb43e-3056">Korrigera några felmeddelanden.</span><span class="sxs-lookup"><span data-stu-id="cb43e-3056">Fix some error messages.</span></span>
* <span data-ttu-id="cb43e-3057">Korrigering av skapande av kluster med ARM-mall som är standard för New-AzServiceFabriCluster som inte fungerade med migrering till Az.</span><span class="sxs-lookup"><span data-stu-id="cb43e-3057">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="cb43e-3058">Korrigering av tilläggning av kluster/programcertifikat så att endast VM Scale Sets som motsvarar klustret läggs till genom att kontrollera ID för klustret i tillägget.</span><span class="sxs-lookup"><span data-stu-id="cb43e-3058">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="cb43e-3059">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="cb43e-3059">Az.SignalR</span></span>
* <span data-ttu-id="cb43e-3060">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="cb43e-3060">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb43e-3061">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb43e-3061">Az.Sql</span></span>
* <span data-ttu-id="cb43e-3062">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="cb43e-3062">Update incorrect online help URLs</span></span>
* <span data-ttu-id="cb43e-3063">Uppdaterad parameterbeskrivning för LicenseType-parameter med möjliga värden</span><span class="sxs-lookup"><span data-stu-id="cb43e-3063">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="cb43e-3064">Korrigering för att uppdatera hanterad instansidentitet som inte fungerar när det är den enda uppdaterade egenskapen</span><span class="sxs-lookup"><span data-stu-id="cb43e-3064">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="cb43e-3065">Stöd för anpassad sortering på hanterad instans</span><span class="sxs-lookup"><span data-stu-id="cb43e-3065">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cb43e-3066">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb43e-3066">Az.Storage</span></span>
* <span data-ttu-id="cb43e-3067">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="cb43e-3067">Update incorrect online help URLs</span></span>
* <span data-ttu-id="cb43e-3068">Tillhandahåll detaljerat felmeddelande när en användare försöker hämta/konfigurera klassisk loggning/mått på ett Premium Storage-konto eftersom Premium Storage-kontot inte har stöd för klassisk loggning/mått.</span><span class="sxs-lookup"><span data-stu-id="cb43e-3068">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="cb43e-3069">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="cb43e-3069">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="cb43e-3070">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="cb43e-3070">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="cb43e-3071">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="cb43e-3071">Az.TrafficManager</span></span>
* <span data-ttu-id="cb43e-3072">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="cb43e-3072">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cb43e-3073">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb43e-3073">Az.Websites</span></span>
* <span data-ttu-id="cb43e-3074">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="cb43e-3074">Update incorrect online help URLs</span></span>
* <span data-ttu-id="cb43e-3075">Korrigerar ”New-AzWebAppSSLBinding” så att certifikatet laddas upp till rätt resursgrupp och plats om appen finns i en ASE.</span><span class="sxs-lookup"><span data-stu-id="cb43e-3075">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="cb43e-3076">Korrigerar ”New-AzWebAppSSLBinding” så att taggarna inte skrivs över på en bindning av ett SSL-certifikat till en app</span><span class="sxs-lookup"><span data-stu-id="cb43e-3076">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="cb43e-3077">1.1.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="cb43e-3077">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cb43e-3078">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb43e-3078">Az.Accounts</span></span>
* <span data-ttu-id="cb43e-3079">Lade till omfattningen ”Lokal” till Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="cb43e-3079">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb43e-3080">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb43e-3080">Az.Compute</span></span>
* <span data-ttu-id="cb43e-3081">Namn är nu valfritt i ID-parametern för Restart/Start/Stop/Remove/Set-AzVM och Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="cb43e-3081">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="cb43e-3082">Uppdaterade beskrivningen av ID i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="cb43e-3082">Updated the description of ID in help files</span></span>
* <span data-ttu-id="cb43e-3083">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb43e-3083">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cb43e-3084">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cb43e-3084">Az.DataLakeStore</span></span>
* <span data-ttu-id="cb43e-3085">Uppdatera sdk-versionen av dataplanet till 1.1.14 för SDK-korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="cb43e-3085">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="cb43e-3086">Korrigerade hanteringen av negativ accesstime och modificationtime för getfilestatus och liststatus; korrigera asynkront annulleringstoken</span><span class="sxs-lookup"><span data-stu-id="cb43e-3086">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="cb43e-3087">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="cb43e-3087">Az.EventGrid</span></span>
* <span data-ttu-id="cb43e-3088">Uppdaterat för användning av API-versionen 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="cb43e-3088">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="cb43e-3089">Uppdaterade följande cmdletar för att stödja nytt scenario i API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="cb43e-3089">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="cb43e-3090">New-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="cb43e-3090">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="cb43e-3091">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="cb43e-3091">Event Time-To-Live,</span></span>
        - <span data-ttu-id="cb43e-3092">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="cb43e-3092">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="cb43e-3093">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="cb43e-3093">Dead letter endpoint.</span></span>
    - <span data-ttu-id="cb43e-3094">Update-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="cb43e-3094">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="cb43e-3095">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="cb43e-3095">Event Time-To-Live,</span></span>
        - <span data-ttu-id="cb43e-3096">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="cb43e-3096">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="cb43e-3097">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="cb43e-3097">Dead letter endpoint.</span></span>
* <span data-ttu-id="cb43e-3098">Lade till nya enum-värden (storageQueue och hybridConnection) för alternativet EndpointType i cmdletarna New-AzureRmEventGridSubscription och Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="cb43e-3098">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="cb43e-3099">Visa varningsmeddelanden om skapande eller uppdatering av händelseprenumerationen förväntas medföra manuell åtgärd från användaren.</span><span class="sxs-lookup"><span data-stu-id="cb43e-3099">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cb43e-3100">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cb43e-3100">Az.IotHub</span></span>
* <span data-ttu-id="cb43e-3101">Har uppdaterats till den senaste versionen av SDK:n lotHub</span><span class="sxs-lookup"><span data-stu-id="cb43e-3101">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="cb43e-3102">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="cb43e-3102">Az.LogicApp</span></span>
* <span data-ttu-id="cb43e-3103">Get-AzLogicApp visar en lista över alla som inte har angivet namn</span><span class="sxs-lookup"><span data-stu-id="cb43e-3103">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb43e-3104">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb43e-3104">Az.Resources</span></span>
* <span data-ttu-id="cb43e-3105">Åtgärdade problem med parameteruppsättningen när parametrarna -ODataQuery och -ResourceId anges för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="cb43e-3105">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="cb43e-3106">Mer information här: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="cb43e-3106">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="cb43e-3107">Åtgärdade hantering av parametern -Custom i New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="cb43e-3107">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="cb43e-3108">Korrigerade stavfel i New-AzDeployment-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="cb43e-3108">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="cb43e-3109">Gjorde parametern -MailNickname obligatorisk för New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="cb43e-3109">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="cb43e-3110">Mer information här: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="cb43e-3110">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="cb43e-3111">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="cb43e-3111">Az.SignalR</span></span>
* <span data-ttu-id="cb43e-3112">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb43e-3112">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb43e-3113">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb43e-3113">Az.Sql</span></span>
* <span data-ttu-id="cb43e-3114">Konverterade lagringshanteringsklientens beroende av den normala SDK-implementeringen.</span><span class="sxs-lookup"><span data-stu-id="cb43e-3114">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cb43e-3115">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb43e-3115">Az.Storage</span></span>
* <span data-ttu-id="cb43e-3116">Angav StorageAccountName för lagringskontext som det verkliga namnet på lagringskontot när det skapas med Sas Token, OAuth eller Anonymous</span><span class="sxs-lookup"><span data-stu-id="cb43e-3116">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="cb43e-3117">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="cb43e-3117">New-AzStorageContext</span></span>
* <span data-ttu-id="cb43e-3118">Skapade Sas Token för Blob Snapshot-objekt med parametern -FullUri, åtgärdade den returnerade URI:n så att den blir URI för ögonblicksbild</span><span class="sxs-lookup"><span data-stu-id="cb43e-3118">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="cb43e-3119">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="cb43e-3119">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cb43e-3120">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb43e-3120">Az.Websites</span></span>
* <span data-ttu-id="cb43e-3121">Åtgärdade en bugg i datumparsningen i Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="cb43e-3121">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="cb43e-3122">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb43e-3122">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="cb43e-3123">1.0.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="cb43e-3123">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="cb43e-3124">Allmänt</span><span class="sxs-lookup"><span data-stu-id="cb43e-3124">General</span></span>

- <span data-ttu-id="cb43e-3125">Allmän tillgänglighet för Az-modulen</span><span class="sxs-lookup"><span data-stu-id="cb43e-3125">General Availability of Az Module</span></span>
- <span data-ttu-id="cb43e-3126">Onlinehjälp för varje modul</span><span class="sxs-lookup"><span data-stu-id="cb43e-3126">Online help for each module</span></span>
- <span data-ttu-id="cb43e-3127">Mer information och en översikt finns på [Az-informationssidan](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="cb43e-3127">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="cb43e-3128">Information om hur du migrerar från AzureRM finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="cb43e-3128">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="cb43e-3129">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb43e-3129">Az.Accounts</span></span>
- <span data-ttu-id="cb43e-3130">Har ändrats från Az.Profile</span><span class="sxs-lookup"><span data-stu-id="cb43e-3130">Changed from Az.Profile</span></span>
- <span data-ttu-id="cb43e-3131">Fasta tabellformat för profil- och kontexttyper</span><span class="sxs-lookup"><span data-stu-id="cb43e-3131">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="cb43e-3132">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cb43e-3132">Az.ApiManagement</span></span>
- <span data-ttu-id="cb43e-3133">Korrigeringar för #7002</span><span class="sxs-lookup"><span data-stu-id="cb43e-3133">Fixes for #7002</span></span>
- <span data-ttu-id="cb43e-3134">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="cb43e-3134">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="cb43e-3135">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="cb43e-3135">Az.Batch</span></span>
- <span data-ttu-id="cb43e-3136">Lade till möjligheten att se vilken version av Azure Batch Node Agent som körs på var och en av de virtuella datorerna i en pool, via den nya egenskapen `NodeAgentInformation` på `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="cb43e-3136">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="cb43e-3137">Standarden `Caching` för `PSDataDisk` är nu `ReadWrite` i stället för `None`.</span><span class="sxs-lookup"><span data-stu-id="cb43e-3137">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="cb43e-3138">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="cb43e-3138">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="cb43e-3139">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="cb43e-3139">Az.Billing</span></span>
- <span data-ttu-id="cb43e-3140">Kombinerar cmdletarna för fakturering, förbrukning och UsageAggregates. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="cb43e-3140">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="cb43e-3141">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="cb43e-3141">Az.CognitivServices</span></span>
- <span data-ttu-id="cb43e-3142">Lade till kompletterare för SkuName och Typem som är tillgängliga i New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="cb43e-3142">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="cb43e-3143">Tog bort parameteruppsättningen GetSkusWithAccountParamSetName från Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="cb43e-3143">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="cb43e-3144">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="cb43e-3144">Az.ContainerInstance</span></span>
- <span data-ttu-id="cb43e-3145">Stöd för ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="cb43e-3145">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="cb43e-3146">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="cb43e-3146">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="cb43e-3147">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="cb43e-3147">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="cb43e-3148">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cb43e-3148">Az.DataLakeStore</span></span>
- <span data-ttu-id="cb43e-3149">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="cb43e-3149">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="cb43e-3150">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cb43e-3150">Az.Monitor</span></span>
- <span data-ttu-id="cb43e-3151">Döpte om Az.Insights till Az.Monitor och andra mindre icke-bakåtkompatibla ändringar. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="cb43e-3151">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="cb43e-3152">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cb43e-3152">Az.KeyVault</span></span>
- <span data-ttu-id="cb43e-3153">Tog bort den inaktuella egenskapen PurgeDisabled från utdatatyper</span><span class="sxs-lookup"><span data-stu-id="cb43e-3153">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="cb43e-3154">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="cb43e-3154">Az.MachineLearning</span></span>
- <span data-ttu-id="cb43e-3155">Inkluderade cmdletarna från modulen Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="cb43e-3155">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="cb43e-3156">Az.Media</span><span class="sxs-lookup"><span data-stu-id="cb43e-3156">Az.Media</span></span>
- <span data-ttu-id="cb43e-3157">Tog bort inaktuella -Tags-alias från New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="cb43e-3157">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="cb43e-3158">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb43e-3158">Az.Network</span></span>
<span data-ttu-id="cb43e-3159">Stöd har lagts till för konfiguration av RewriteRuleSets i Application Gateway</span><span class="sxs-lookup"><span data-stu-id="cb43e-3159">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="cb43e-3160">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="cb43e-3160">New cmdlets added:</span></span>
        - <span data-ttu-id="cb43e-3161">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cb43e-3161">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="cb43e-3162">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cb43e-3162">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="cb43e-3163">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cb43e-3163">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="cb43e-3164">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cb43e-3164">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="cb43e-3165">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cb43e-3165">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="cb43e-3166">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="cb43e-3166">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="cb43e-3167">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="cb43e-3167">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="cb43e-3168">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb43e-3168">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="cb43e-3169">Cmdletar har uppdaterats med den valfria parametern -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cb43e-3169">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="cb43e-3170">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cb43e-3170">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="cb43e-3171">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="cb43e-3171">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="cb43e-3172">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="cb43e-3172">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="cb43e-3173">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cb43e-3173">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="cb43e-3174">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="cb43e-3174">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="cb43e-3175">New-AzureRmApplicationGatewayUrlPathMapConfig har lagt till KeyVault-stöd för Application Gateway med Identity.</span><span class="sxs-lookup"><span data-stu-id="cb43e-3175">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="cb43e-3176">Cmdletar har uppdaterats med den valfria parametern -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="cb43e-3176">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="cb43e-3177">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="cb43e-3177">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="cb43e-3178">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="cb43e-3178">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="cb43e-3179">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="cb43e-3179">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="cb43e-3180">Cmdleten New-AzApplicationGateway har uppdaterats med den valfria parametern -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="cb43e-3180">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="cb43e-3181">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="cb43e-3181">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="cb43e-3182">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cb43e-3182">Az.OperationalInsights</span></span>
- <span data-ttu-id="cb43e-3183">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="cb43e-3183">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="cb43e-3184">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="cb43e-3184">Az.Profile</span></span>
- <span data-ttu-id="cb43e-3185">Modulnamnet har ändrats till Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb43e-3185">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="cb43e-3186">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb43e-3186">Az.RecoveryServices</span></span>
- <span data-ttu-id="cb43e-3187">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="cb43e-3187">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="cb43e-3188">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb43e-3188">Az.Resources</span></span>
- <span data-ttu-id="cb43e-3189">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="cb43e-3189">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="cb43e-3190">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cb43e-3190">Az.ServiceFabric</span></span>
- <span data-ttu-id="cb43e-3191">Stöd för specificering av certifikat efter eget namn och tumavtryck</span><span class="sxs-lookup"><span data-stu-id="cb43e-3191">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="cb43e-3192">Information om fler icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="cb43e-3192">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="cb43e-3193">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="cb43e-3193">Az.SIgnalR</span></span>
- <span data-ttu-id="cb43e-3194">Allmän tillgänglighet för PowerShell-cmdletar för SIgnalR</span><span class="sxs-lookup"><span data-stu-id="cb43e-3194">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="cb43e-3195">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb43e-3195">Az.Sql</span></span>
- <span data-ttu-id="cb43e-3196">Lade till de nya identifieringstyperna Data_Exfiltration och Unsafe_Action i Threat Detection-cmdletar</span><span class="sxs-lookup"><span data-stu-id="cb43e-3196">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="cb43e-3197">Uppdaterade dokumentationsexempel för Sql Auditing-cmdletar</span><span class="sxs-lookup"><span data-stu-id="cb43e-3197">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="cb43e-3198">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="cb43e-3198">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="cb43e-3199">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb43e-3199">Az.Storage</span></span>
- <span data-ttu-id="cb43e-3200">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="cb43e-3200">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="cb43e-3201">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb43e-3201">Az.Websites</span></span>
- <span data-ttu-id="cb43e-3202">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="cb43e-3202">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="cb43e-3203">0.7.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="cb43e-3203">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="cb43e-3204">Allmänt</span><span class="sxs-lookup"><span data-stu-id="cb43e-3204">General</span></span>

* <span data-ttu-id="cb43e-3205">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="cb43e-3205">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="cb43e-3206">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb43e-3206">Az.Compute</span></span>

* <span data-ttu-id="cb43e-3207">Lade till stöd för UltraSSD och Galleriavbildningar i de enkla parameteruppsättningarna för `New-AzVm(ss)`-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="cb43e-3207">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="cb43e-3208">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cb43e-3208">Az.DataLakeStore</span></span>

* <span data-ttu-id="cb43e-3209">Åtgärdade avslutande snedstreck i domänen för adls-konto</span><span class="sxs-lookup"><span data-stu-id="cb43e-3209">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="cb43e-3210">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="cb43e-3210">Az.FrontDoor</span></span>

* <span data-ttu-id="cb43e-3211">Brutna länkar korrigerades</span><span class="sxs-lookup"><span data-stu-id="cb43e-3211">Fixed some broken links</span></span>
    - <span data-ttu-id="cb43e-3212">I artiklarna New-AzureRmFrontDoor och Set-AzureRmFrontDoor artiklar korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="cb43e-3212">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="cb43e-3213">I artikeln New-AzureRmFrontDoorManagedRuleObject korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="cb43e-3213">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="cb43e-3214">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb43e-3214">Az.RecoveryServices</span></span>

* <span data-ttu-id="cb43e-3215">Lade till valideringar på klientsidan för Azure-filresurs med återställningsåtgärder.</span><span class="sxs-lookup"><span data-stu-id="cb43e-3215">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="cb43e-3216">Gjorde storageAccountName och storageAccountResourceGroupName valfritt för afs-återställning.</span><span class="sxs-lookup"><span data-stu-id="cb43e-3216">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="cb43e-3217">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb43e-3217">Az.Resources</span></span>

* <span data-ttu-id="cb43e-3218">Korrigering för https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="cb43e-3218">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="cb43e-3219">Uppdaterade Get-AzureRmRoleAssignment så att prenumerationsomfattningen används om den anges vid begäran om klassiska administratörer.</span><span class="sxs-lookup"><span data-stu-id="cb43e-3219">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="cb43e-3220">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb43e-3220">Az.Sql</span></span>

* <span data-ttu-id="cb43e-3221">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="cb43e-3221">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="cb43e-3222">Korrigerade ett problem med Get-AzureRmSqlDatabaseVulnerabilityAssessment med DotNet-kärna</span><span class="sxs-lookup"><span data-stu-id="cb43e-3222">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="cb43e-3223">Ändrade dokumentationen för hjälpmeddelanden som rör SQL Auditing-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="cb43e-3223">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="cb43e-3224">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb43e-3224">Az.Storage</span></span>

* <span data-ttu-id="cb43e-3225">Lade till -EnableHierarchicalNamespace i New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cb43e-3225">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="cb43e-3226">Åtgärdade problemet med att cmdleten Copy File inte kunde återanvända källkontexten på målet om inte -DestContext angetts</span><span class="sxs-lookup"><span data-stu-id="cb43e-3226">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="cb43e-3227">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="cb43e-3227">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="cb43e-3228">Stöd för statisk webbplatskonfiguration</span><span class="sxs-lookup"><span data-stu-id="cb43e-3228">Support Static Website configuration</span></span>
    - <span data-ttu-id="cb43e-3229">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="cb43e-3229">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="cb43e-3230">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="cb43e-3230">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="cb43e-3231">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb43e-3231">Az.Websites</span></span>

* <span data-ttu-id="cb43e-3232">Set-AzureRmWebApp och Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="cb43e-3232">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="cb43e-3233">Ny parameter (-AzureStoragePath) har lagts till för att ange att Azure Storage-sökvägar ska monteras i containerappar i Windows och Linux.</span><span class="sxs-lookup"><span data-stu-id="cb43e-3233">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="cb43e-3234">Använder utdata från den nya cmdleten New-AzureRmWebAppAzureStoragePath som en parameter för att ange sökvägar för Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="cb43e-3234">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="cb43e-3235">0.6.1 – november 2018</span><span class="sxs-lookup"><span data-stu-id="cb43e-3235">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="cb43e-3236">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cb43e-3236">Az.ApiManagement</span></span>
* <span data-ttu-id="cb43e-3237">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="cb43e-3237">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="cb43e-3238">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cb43e-3238">Az.Automation</span></span>
* <span data-ttu-id="cb43e-3239">Swagger baserade Azure Automation-cmdletar</span><span class="sxs-lookup"><span data-stu-id="cb43e-3239">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="cb43e-3240">Cmdletar för Uppdateringshantering har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-3240">Added Update Management cmdlets</span></span>
* <span data-ttu-id="cb43e-3241">Cmdletar för källkontroll har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-3241">Added Source Control cmdlets</span></span>
* <span data-ttu-id="cb43e-3242">Remove-AzureRmAutomationHybridWorkerGroup-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-3242">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="cb43e-3243">Kommandot för DSC-registreringsnod har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="cb43e-3243">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="cb43e-3244">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb43e-3244">Az.Compute</span></span>
* <span data-ttu-id="cb43e-3245">Problem med SystemAssigned-identitet har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="cb43e-3245">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="cb43e-3246">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="cb43e-3246">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="cb43e-3247">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="cb43e-3247">Az.ContainerInstance</span></span>
* <span data-ttu-id="cb43e-3248">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="cb43e-3248">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="cb43e-3249">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="cb43e-3249">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="cb43e-3250">uppdatera exempelbeskrivningen för marketplace-cmdletar</span><span class="sxs-lookup"><span data-stu-id="cb43e-3250">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="cb43e-3251">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb43e-3251">Az.Network</span></span>
* <span data-ttu-id="cb43e-3252">Cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomErreller Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-3252">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="cb43e-3253">ICMP tillbaka till stöd för Azure Firewall-nätverksprotokoll har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-3253">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="cb43e-3254">Uppdatera cmdlet Test-AzureRmNetworkWatcherConnectivity, lägga till verifiering av mål-id, adress och port.</span><span class="sxs-lookup"><span data-stu-id="cb43e-3254">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="cb43e-3255">Åtgärda problem med minnesanvändning i VirtualNetwork-karta</span><span class="sxs-lookup"><span data-stu-id="cb43e-3255">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="cb43e-3256">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="cb43e-3256">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="cb43e-3257">Åtgärda för att ändra principen för en skyddad fildelning.</span><span class="sxs-lookup"><span data-stu-id="cb43e-3257">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="cb43e-3258">Tidszonsprincipen har konverterats till versaler.</span><span class="sxs-lookup"><span data-stu-id="cb43e-3258">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="cb43e-3259">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="cb43e-3259">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="cb43e-3260">Exempel i New-AzureRmRecoveryServicesAsrProtectableItem har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="cb43e-3260">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="cb43e-3261">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="cb43e-3261">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="cb43e-3262">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="cb43e-3262">Az.Relay</span></span>
* <span data-ttu-id="cb43e-3263">Valfri parameter -KeyValue till New-AzureRmRelayKey cmdlet har lagts till, vilket gör det möjligt för användare att tillhandahålla KeyValue.</span><span class="sxs-lookup"><span data-stu-id="cb43e-3263">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="cb43e-3264">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb43e-3264">Az.Resources</span></span>
* <span data-ttu-id="cb43e-3265">Uppdatera hjälpdokumentation för resursidentitet kopplad till parametrar i `New-AzureRmPolicyAssignment` och `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="cb43e-3265">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="cb43e-3266">Lägg till ett exempel för New-AzureRmPolicyDefinition som använder -Metadata</span><span class="sxs-lookup"><span data-stu-id="cb43e-3266">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="cb43e-3267">Korrigera så att skiftläge behålls i taggnycklar i NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="cb43e-3267">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="cb43e-3268">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cb43e-3268">Az.ServiceFabric</span></span>
* <span data-ttu-id="cb43e-3269">Lägg till utfasningsmeddelanden för kommande icke-kompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="cb43e-3269">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="cb43e-3270">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb43e-3270">Az.Sql</span></span>
* <span data-ttu-id="cb43e-3271">Nya cmdletar för CRUD-åtgärder på Azure Sql Database-hanterad instans och Azure Sql-hanterad databas</span><span class="sxs-lookup"><span data-stu-id="cb43e-3271">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="cb43e-3272">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="cb43e-3272">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="cb43e-3273">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="cb43e-3273">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="cb43e-3274">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="cb43e-3274">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="cb43e-3275">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="cb43e-3275">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="cb43e-3276">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="cb43e-3276">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="cb43e-3277">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="cb43e-3277">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="cb43e-3278">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="cb43e-3278">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="cb43e-3279">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="cb43e-3279">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="cb43e-3280">Hantering av utökad granskningsprincip på en server eller en databas har aktiverats.</span><span class="sxs-lookup"><span data-stu-id="cb43e-3280">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="cb43e-3281">Ny parameter (PredicateExpression) har lagts till för att aktivera filtrering av granskningsloggar.</span><span class="sxs-lookup"><span data-stu-id="cb43e-3281">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="cb43e-3282">Cmdletar har ändrats så att de använder SQL-klienter i stället för äldre klienter.</span><span class="sxs-lookup"><span data-stu-id="cb43e-3282">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="cb43e-3283">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="cb43e-3283">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="cb43e-3284">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="cb43e-3284">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="cb43e-3285">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="cb43e-3285">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="cb43e-3286">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="cb43e-3286">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="cb43e-3287">Problem med att använda Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings med lagringskontots namnparameter har korrigerats</span><span class="sxs-lookup"><span data-stu-id="cb43e-3287">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="cb43e-3288">0.5.0 – november 2018</span><span class="sxs-lookup"><span data-stu-id="cb43e-3288">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="cb43e-3289">Allmänt</span><span class="sxs-lookup"><span data-stu-id="cb43e-3289">General</span></span>
* <span data-ttu-id="cb43e-3290">Lade till resurskompletterare till många kärn-cmdletar – dessa gör att du kan stega genom befintliga resursnamn med TABB vid interaktiva anrop till cmdletar</span><span class="sxs-lookup"><span data-stu-id="cb43e-3290">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="cb43e-3291">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="cb43e-3291">Az.Profile</span></span>
* <span data-ttu-id="cb43e-3292">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="cb43e-3292">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="cb43e-3293">Bytte namn på parametern TenantId i cmdleten Connect-AzAccount till Tenant och lade till ett alias för TenantId</span><span class="sxs-lookup"><span data-stu-id="cb43e-3293">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="cb43e-3294">Uppdaterade TenantId-beskrivningen för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="cb43e-3294">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="cb43e-3295">Åtgärda felmeddelande för misslyckad inloggning när du tillhandahåller klientdomän</span><span class="sxs-lookup"><span data-stu-id="cb43e-3295">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="cb43e-3296">Åtgärda problem med att kontextnamn hamnar i konflikt för konton utan prenumerationer i klientorganisationen</span><span class="sxs-lookup"><span data-stu-id="cb43e-3296">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="cb43e-3297">Åtgärda problem med DataLake-slutpunkter vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="cb43e-3297">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="cb43e-3298">Åtgärdade problem med att Disconnect-AzAccount kastades om den inte anslöts</span><span class="sxs-lookup"><span data-stu-id="cb43e-3298">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="cb43e-3299">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cb43e-3299">Az.CognitiveServices</span></span>
* <span data-ttu-id="cb43e-3300">Lade till åtgärden Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="cb43e-3300">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb43e-3301">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb43e-3301">Az.Compute</span></span>
* <span data-ttu-id="cb43e-3302">Lade till cmdletarna Add-AzVmssVMDataDisk och Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="cb43e-3302">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="cb43e-3303">Get-AzVMImage visar AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="cb43e-3303">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="cb43e-3304">Åtgärdade att värdena för alternativen SetAzVMChefExtension -BootstrapOptions och -JsonAttribute inte angavs i json-format.</span><span class="sxs-lookup"><span data-stu-id="cb43e-3304">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cb43e-3305">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cb43e-3305">Az.DataLakeStore</span></span>
* <span data-ttu-id="cb43e-3306">Uppdatera DataLake-paketet till 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="cb43e-3306">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="cb43e-3307">Lägg till standardsamtidighet för flertrådade åtgärder.</span><span class="sxs-lookup"><span data-stu-id="cb43e-3307">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="cb43e-3308">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="cb43e-3308">Az.Insights</span></span>
* <span data-ttu-id="cb43e-3309">Åtgärdade problem #7267 (autoskalningsområde)</span><span class="sxs-lookup"><span data-stu-id="cb43e-3309">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="cb43e-3310">Problem med att uppräknade parametrar inte ställdes in ordentligt när du skapade en ny autoskalningsregel (de ställdes alltid in med standardvärdet).</span><span class="sxs-lookup"><span data-stu-id="cb43e-3310">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="cb43e-3311">Åtgärdade problem #7513 [Insights] Set-AzDiagnosticSetting kräver uttrycklig specifikation av kategorier när inställningar skapas</span><span class="sxs-lookup"><span data-stu-id="cb43e-3311">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="cb43e-3312">Nu kräver inte cmdleten uttrycklig anvisning av kategorierna för att aktiveras under skapande, d.v.s. den fungerar enligt beskrivning</span><span class="sxs-lookup"><span data-stu-id="cb43e-3312">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb43e-3313">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb43e-3313">Az.Network</span></span>
* <span data-ttu-id="cb43e-3314">PeeringType ändrades till en obligatorisk parameter för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="cb43e-3314">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="cb43e-3315">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="cb43e-3315">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="cb43e-3316">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="cb43e-3316">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="cb43e-3317">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="cb43e-3317">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="cb43e-3318">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="cb43e-3318">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="cb43e-3319">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="cb43e-3319">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="cb43e-3320">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="cb43e-3320">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="cb43e-3321">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="cb43e-3321">Az.PolicyInsights</span></span>
* <span data-ttu-id="cb43e-3322">Cmdletar för principreparation har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-3322">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb43e-3323">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb43e-3323">Az.Resources</span></span>
* <span data-ttu-id="cb43e-3324">Korrigering för https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="cb43e-3324">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="cb43e-3325">Tillåt att resurser listas med parametern -ResourceId för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="cb43e-3325">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="cb43e-3326">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="cb43e-3326">Az.ServiceBus</span></span>
* <span data-ttu-id="cb43e-3327">Skrivskyddad MigrationState-egenskap har lagts till i PSServiceBusMigrationConfigurationAttributes, som hjälper till att hålla koll på migreringstillståndet.</span><span class="sxs-lookup"><span data-stu-id="cb43e-3327">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="cb43e-3328">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cb43e-3328">Az.ServiceFabric</span></span>
* <span data-ttu-id="cb43e-3329">Åtgärda att lägga till certifikat till Linux-Vmss.</span><span class="sxs-lookup"><span data-stu-id="cb43e-3329">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="cb43e-3330">Åtgärdade Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="cb43e-3330">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="cb43e-3331">Använd rätt tumavtryck från nya certifikat (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="cb43e-3331">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="cb43e-3332">Visa undantag korrekt (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="cb43e-3332">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="cb43e-3333">Åtgärdade Update-AzServiceFabricDurability så att klusterkonfigurationen uppdateras innan Vmss-åtgärden CreateOrUpdate påbörjas.</span><span class="sxs-lookup"><span data-stu-id="cb43e-3333">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="cb43e-3334">0.4.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="cb43e-3334">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="cb43e-3335">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="cb43e-3335">Az.Profile</span></span>
* <span data-ttu-id="cb43e-3336">Åtgärdade problemet med Get-AzSubscription i CloudShell</span><span class="sxs-lookup"><span data-stu-id="cb43e-3336">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="cb43e-3337">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="cb43e-3337">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb43e-3338">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb43e-3338">Az.Compute</span></span>
* <span data-ttu-id="cb43e-3339">Nya storlekar lades till i listan över godkända VM-storlekar för vilka accelererat nätverk kommer att aktiveras vid användning av den enkla parameteruppsättningen för New-AzVm</span><span class="sxs-lookup"><span data-stu-id="cb43e-3339">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="cb43e-3340">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="cb43e-3340">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cb43e-3341">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cb43e-3341">Az.DataLakeStore</span></span>
* <span data-ttu-id="cb43e-3342">Lägger till stöd för regler för virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="cb43e-3342">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="cb43e-3343">Get-AzDataLakeStoreVirtualNetworkRule: Hämtar eller listar regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="cb43e-3343">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="cb43e-3344">Add-AzDataLakeStoreVirtualNetworkRule: Lägger till en regel för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="cb43e-3344">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="cb43e-3345">Set-AzDataLakeStoreVirtualNetworkRule: Ändrar den angivna regeln för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="cb43e-3345">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="cb43e-3346">Remove-AzDataLakeStoreVirtualNetworkRule: Tar bort en regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="cb43e-3346">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb43e-3347">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb43e-3347">Az.Network</span></span>
* <span data-ttu-id="cb43e-3348">Skicka protokollvärdet till serverdelen för att uppdatera cmdleten Test-AzNetworkWatcherConnectivity.</span><span class="sxs-lookup"><span data-stu-id="cb43e-3348">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="cb43e-3349">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="cb43e-3349">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb43e-3350">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb43e-3350">Az.Resources</span></span>
* <span data-ttu-id="cb43e-3351">Åtgärdade problem där Get-AzRoleDefinition genererar ett oläsligt undantag (när standardprofilen inte innehåller någon prenumeration och ingen omfattning har angetts) genom att lägga till ett beskrivande undantag i scenariot.</span><span class="sxs-lookup"><span data-stu-id="cb43e-3351">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="cb43e-3352">Ställ in ”RoleDefinitionNameParameterSet” som standardparameteruppsättning.</span><span class="sxs-lookup"><span data-stu-id="cb43e-3352">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="cb43e-3353">0.3.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="cb43e-3353">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="cb43e-3354">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="cb43e-3354">Azure.Storage</span></span>
* <span data-ttu-id="cb43e-3355">Åtgärda fel där Kopiera blob/fil inte kopierar metadata när målplatsen har ett problem med metadata</span><span class="sxs-lookup"><span data-stu-id="cb43e-3355">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="cb43e-3356">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="cb43e-3356">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="cb43e-3357">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="cb43e-3357">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="cb43e-3358">Stöd för att hämta användningsinformation om en Storage-resurs för en specifik plats och för att lägga till ett varningsmeddelande för att hämta användningsinformation om en global Storage-resurs är inaktuellt.</span><span class="sxs-lookup"><span data-stu-id="cb43e-3358">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="cb43e-3359">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="cb43e-3359">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="cb43e-3360">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cb43e-3360">Az.CognitiveServices</span></span>
* <span data-ttu-id="cb43e-3361">Stöd för Get-AzCognitiveServicesAccountSkus utan ett befintligt konto.</span><span class="sxs-lookup"><span data-stu-id="cb43e-3361">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb43e-3362">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb43e-3362">Az.Compute</span></span>
* <span data-ttu-id="cb43e-3363">Åtgärdade fel där Get-AzVM -ResourceGroupName <rg> returnerar fler än 50 resultat om det behövs</span><span class="sxs-lookup"><span data-stu-id="cb43e-3363">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="cb43e-3364">Lade till ett exempel för SimpleParameterSet i hjälpen för cmdleten New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="cb43e-3364">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="cb43e-3365">Ett stavfel i förloppsmeddelandet för Azure Disk Encryption har korrigerats</span><span class="sxs-lookup"><span data-stu-id="cb43e-3365">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="cb43e-3366">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="cb43e-3366">Az.DataFactoryV2</span></span>
* <span data-ttu-id="cb43e-3367">ADF .Net SDK-versionen har uppdaterats till 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="cb43e-3367">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb43e-3368">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb43e-3368">Az.Network</span></span>
* <span data-ttu-id="cb43e-3369">Funktionalitet för NetworkProfile har lagts till.</span><span class="sxs-lookup"><span data-stu-id="cb43e-3369">Added NetworkProfile functionality.</span></span> <span data-ttu-id="cb43e-3370">nya cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-3370">new cmdlets added</span></span>
    - <span data-ttu-id="cb43e-3371">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="cb43e-3371">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="cb43e-3372">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="cb43e-3372">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="cb43e-3373">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="cb43e-3373">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="cb43e-3374">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="cb43e-3374">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="cb43e-3375">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="cb43e-3375">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="cb43e-3376">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="cb43e-3376">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="cb43e-3377">Länk för tjänstassociering på modell för undernät har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-3377">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="cb43e-3378">Cmdletarna New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap och Remove-AzVirtualNetworkTap har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-3378">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="cb43e-3379">Cmdletarna Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig och Remove-AzNEtworkInterfaceTapConfig har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-3379">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="cb43e-3380">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="cb43e-3380">Az.RedisCache</span></span>
* <span data-ttu-id="cb43e-3381">Tillåt att alla strängar används som storleksparametrar framöver.</span><span class="sxs-lookup"><span data-stu-id="cb43e-3381">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="cb43e-3382">Lägg till P5 i popup-fönstret PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="cb43e-3382">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb43e-3383">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb43e-3383">Az.Resources</span></span>
* <span data-ttu-id="cb43e-3384">Parametern -Mode som saknades i Set-AzPolicyDefinition har lagts till</span><span class="sxs-lookup"><span data-stu-id="cb43e-3384">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="cb43e-3385">Åtgärdade buggen för cmdleten Get-AzProviderOperation för åtgärder med ursprung som innehåller användare</span><span class="sxs-lookup"><span data-stu-id="cb43e-3385">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb43e-3386">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb43e-3386">Az.Sql</span></span>
* <span data-ttu-id="cb43e-3387">Ett problem där vissa cmdletar för säkerhetskopiering inte kunde identifiera den aktuella azure-prenumerationen har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="cb43e-3387">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cb43e-3388">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb43e-3388">Az.Websites</span></span>
* <span data-ttu-id="cb43e-3389">Ny cmdlet: Get-AzWebAppContainerContinuousDeploymentUrl – Hämtar webhook-URL:en för kontinuerlig distribution av container</span><span class="sxs-lookup"><span data-stu-id="cb43e-3389">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="cb43e-3390">Nya cmdletar: New-AzWebAppContainerPSSession och Enter-WebAppContainerPSSession – Startar en PowerShell-fjärrsession i en containerapp för windows</span><span class="sxs-lookup"><span data-stu-id="cb43e-3390">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="cb43e-3391">0.2.0 – september 2018</span><span class="sxs-lookup"><span data-stu-id="cb43e-3391">0.2.0 - September 2018</span></span>
 <span data-ttu-id="cb43e-3392">Första versionen</span><span class="sxs-lookup"><span data-stu-id="cb43e-3392">Initial Release</span></span>