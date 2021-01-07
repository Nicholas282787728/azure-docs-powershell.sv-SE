---
title: Viktig information om Azure PowerShell
description: Lär dig mer om alla de senaste uppdateringarna för Azure PowerShell-modulerna.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 613ef1e104cf825c32f50fd012132d1dde91a45c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "97894074"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="71536-103">Viktig information om Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="71536-103">Azure PowerShell release notes</span></span>

## <a name="530---december-2020"></a><span data-ttu-id="71536-104">5.3.0 – december 2020</span><span class="sxs-lookup"><span data-stu-id="71536-104">5.3.0 - December 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="71536-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="71536-105">Az.Accounts</span></span>
* <span data-ttu-id="71536-106">Åtgärdat problemet med att http-proxy inte iakttas i Windows PowerShell [#13647]</span><span class="sxs-lookup"><span data-stu-id="71536-106">Fixed the issue that Http proxy is not respected in Windows PowerShell [#13647]</span></span>
* <span data-ttu-id="71536-107">Förbättrad felsökningslogg för tidskrävande åtgärder i genererade moduler</span><span class="sxs-lookup"><span data-stu-id="71536-107">Improved debug log of long running operations in generated modules</span></span>

#### <a name="azautomation"></a><span data-ttu-id="71536-108">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="71536-108">Az.Automation</span></span>
* <span data-ttu-id="71536-109">Åtgärdat problemet med att parametrar för start-AzAutomationRunbook inte kan konvertera PSObject-omsluten sträng till JSON-sträng [#13240]</span><span class="sxs-lookup"><span data-stu-id="71536-109">Fixed issue that parameters of 'Start-AzAutomationRunbook' cannot convert PSObject wrapped string to JSON string [#13240]</span></span>
* <span data-ttu-id="71536-110">Åtgärdade platsifyllning för cmdleten New-AzAutomationUpdateManagementAzureQuery</span><span class="sxs-lookup"><span data-stu-id="71536-110">Fixed location completer for New-AzAutomationUpdateManagementAzureQuery cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71536-111">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71536-111">Az.Compute</span></span>
* <span data-ttu-id="71536-112">Den nya parametern VM i den nya parameteruppsättningen VMParameterSet har lagts till i cmdletarna Get-AzVMDscExtensionStatus och Get-AzVMDscExtension.</span><span class="sxs-lookup"><span data-stu-id="71536-112">New parameter 'VM' in new parameter set 'VMParameterSet' added to 'Get-AzVMDscExtensionStatus' and 'Get-AzVMDscExtension' cmdlets.</span></span> 

#### <a name="azdatabricks"></a><span data-ttu-id="71536-113">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="71536-113">Az.Databricks</span></span>
* <span data-ttu-id="71536-114">Åtgärdade ett problem som kan få New-AzDatabricksVNetPeering att returneras innan den etablerats helt (https://github.com/Azure/autorest.powershell/issues/610)</span><span class="sxs-lookup"><span data-stu-id="71536-114">Fixed an issue that may cause 'New-AzDatabricksVNetPeering' to return before it is fully provisioned (https://github.com/Azure/autorest.powershell/issues/610)</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="71536-115">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="71536-115">Az.DataFactory</span></span>
* <span data-ttu-id="71536-116">Åtgärdat problemet med kommandot Invoke-AzDataFactoryV2Pipeline för SupportsShouldProcess</span><span class="sxs-lookup"><span data-stu-id="71536-116">Fixed the command 'Invoke-AzDataFactoryV2Pipeline' for SupportsShouldProcess issue</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="71536-117">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="71536-117">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="71536-118">Egenskapen StartVMOnConnect har lagts till i värdpool.</span><span class="sxs-lookup"><span data-stu-id="71536-118">Added StartVMOnConnect property to hostpool.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="71536-119">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="71536-119">Az.HDInsight</span></span>
* <span data-ttu-id="71536-120">Lade till egenskaperna: Fqdn och EffectiveDiskEncryptionKeyUrl i klassen AzureHDInsightHostInfo.</span><span class="sxs-lookup"><span data-stu-id="71536-120">Added properties: Fqdn and EffectiveDiskEncryptionKeyUrl in the class AzureHDInsightHostInfo.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="71536-121">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="71536-121">Az.KeyVault</span></span>
* <span data-ttu-id="71536-122">Lade till nya parametern -AsPlainText till Get-AzKeyVaultSecret för att direkt returnera hemligheten i klartext [#13630]</span><span class="sxs-lookup"><span data-stu-id="71536-122">Added a new parameter '-AsPlainText' to 'Get-AzKeyVaultSecret' to directly return the secret in plain text [#13630]</span></span>
* <span data-ttu-id="71536-123">Stöd för selektiv återställning av nyckel från en hanterad fullständig HSM-säkerhetskopia [#13526]</span><span class="sxs-lookup"><span data-stu-id="71536-123">Supported selective restore a key from a managed HSM full backup [#13526]</span></span>
* <span data-ttu-id="71536-124">Några mindre problem har åtgärdats [#13583] [#13584]</span><span class="sxs-lookup"><span data-stu-id="71536-124">Fixed some minor issues [#13583] [#13584]</span></span>
* <span data-ttu-id="71536-125">Lade till saknade returnerade objekt för Get-Secret i SecretManagement-modulen</span><span class="sxs-lookup"><span data-stu-id="71536-125">Added missing return objects of 'Get-Secret' in SecretManagement module</span></span>
* <span data-ttu-id="71536-126">Åtgärdade ett problem som kan leda till att valvet skapas utan standardåtkomstprincip [#13687]</span><span class="sxs-lookup"><span data-stu-id="71536-126">Fixed an issue that may cause vault to be created without default access policy [#13687]</span></span>

#### <a name="azkusto"></a><span data-ttu-id="71536-127">Az.Kusto</span><span class="sxs-lookup"><span data-stu-id="71536-127">Az.Kusto</span></span>
* <span data-ttu-id="71536-128">API-versionen har uppdaterats till 2020-09-18.</span><span class="sxs-lookup"><span data-stu-id="71536-128">Updated API version to 2020-09-18.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71536-129">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71536-129">Az.Network</span></span>
* <span data-ttu-id="71536-130">Åtgärdade problem med att ta bort peering- och anslutnings-cmdlet för ExpressRouteCircuit-scenario</span><span class="sxs-lookup"><span data-stu-id="71536-130">Fixed issue in remove peering and connection cmdlet for ExpressRouteCircuit scenario</span></span>
    - <span data-ttu-id="71536-131">Remove-AzExpressRouteCircuitPeeringConfig och Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="71536-131">'Remove-AzExpressRouteCircuitPeeringConfig' and 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="71536-132">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="71536-132">Az.PolicyInsights</span></span>
* <span data-ttu-id="71536-133">Lade till stöd för att returnera sidnumrerade resultat för Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="71536-133">Added support for returning paginated results for Get-AzPolicyState</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="71536-134">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="71536-134">Az.RecoveryServices</span></span>
* <span data-ttu-id="71536-135">Funktionen mjuk borttagning har aktiverats för SQL.</span><span class="sxs-lookup"><span data-stu-id="71536-135">Enabled softdelete feature for SQL.</span></span>
* <span data-ttu-id="71536-136">Åtgärdade SQL AG-återställning och tog bort containernamnskontrollen.</span><span class="sxs-lookup"><span data-stu-id="71536-136">Fixed SQL AG restore and removed the container name check.</span></span>
* <span data-ttu-id="71536-137">Ändrade containernamnsformatet för Azure Files-säkerhetskopieringsobjekt.</span><span class="sxs-lookup"><span data-stu-id="71536-137">Changed container name format for Azure Files backup item.</span></span>
* <span data-ttu-id="71536-138">Stöd för CMK-funktioner har lagts till i Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="71536-138">Added CMK feature support for Recovery services vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="71536-139">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71536-139">Az.Resources</span></span>
* <span data-ttu-id="71536-140">Åtgärdade ett NullRef-undantagsproblem i New-AzureManagedApplication och Set-AzureManagedApplication.</span><span class="sxs-lookup"><span data-stu-id="71536-140">Fixed a NullRef exception issue in 'New-AzureManagedApplication' and 'Set-AzureManagedApplication'.</span></span>
* <span data-ttu-id="71536-141">Uppdaterade Azure Resource Manager SDK för att använda den senaste DeploymentScripts GA API-versionen: 2020-10-01.</span><span class="sxs-lookup"><span data-stu-id="71536-141">Updated Azure Resource Manager SDK to use latest DeploymentScripts GA api-version: 2020-10-01.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="71536-142">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="71536-142">Az.ServiceFabric</span></span>
* <span data-ttu-id="71536-143">Åtgärdade Add-AzServiceFabricNodeType.</span><span class="sxs-lookup"><span data-stu-id="71536-143">Fixed 'Add-AzServiceFabricNodeType'.</span></span> <span data-ttu-id="71536-144">Lade till nodtypen till Service Fabric-kluster innan VM-skalningsuppsättningar skapas.</span><span class="sxs-lookup"><span data-stu-id="71536-144">Added node type to service fabric cluster before creating virtual machine scale set.</span></span>

#### <a name="azsql"></a><span data-ttu-id="71536-145">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71536-145">Az.Sql</span></span>
* <span data-ttu-id="71536-146">Parameterbeskrivningen för kommandot InstanceFailoverGroup har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="71536-146">Fixed parameter description for 'InstanceFailoverGroup' command.</span></span>
* <span data-ttu-id="71536-147">Uppdaterade logiken där schemaName, tableName och columnName extraheras från ID:t för SQL-dataklassificeringskommandon.</span><span class="sxs-lookup"><span data-stu-id="71536-147">Updated the logic in which schemaName, tableName and columnName are being extracted from the id of SQL Data Classification commands.</span></span>
* <span data-ttu-id="71536-148">Uppdaterade fälten Status och StatusMessage i Get-AzSqlDatabaseImportExportStatus så att de överensstämmer med dokumentationen</span><span class="sxs-lookup"><span data-stu-id="71536-148">Fixed Status and StatusMessage fields in 'Get-AzSqlDatabaseImportExportStatus' to conform to documentation</span></span>
* <span data-ttu-id="71536-149">Lade till gransknings-cmdletar för Microsoft-supportåtgärder (DevOps): Get-AzSqlServerMSSupportAudit, Set-AzSqlServerMSSupportAudit, Remove-AzSqlServerMSSupportAudit</span><span class="sxs-lookup"><span data-stu-id="71536-149">Added Microsoft support operations (DevOps) auditing cmdlets: Get-AzSqlServerMSSupportAudit, Set-AzSqlServerMSSupportAudit, Remove-AzSqlServerMSSupportAudit</span></span>

#### <a name="azstorage"></a><span data-ttu-id="71536-150">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="71536-150">Az.Storage</span></span>
* <span data-ttu-id="71536-151">Stöd för att skapa/uppdatera/hämta/lista EncryptionScope för ett lagringskonto</span><span class="sxs-lookup"><span data-stu-id="71536-151">Supported create/update/get/list EncryptionScope of a Storage account</span></span>
    - <span data-ttu-id="71536-152">New-AzStorageEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="71536-152">'New-AzStorageEncryptionScope'</span></span>
    - <span data-ttu-id="71536-153">Update-AzStorageEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="71536-153">'Update-AzStorageEncryptionScope'</span></span>
    - <span data-ttu-id="71536-154">Get-AzStorageEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="71536-154">'Get-AzStorageEncryptionScope'</span></span>
* <span data-ttu-id="71536-155">Stöd för att skapa container och ladda upp blob med inställning för krypteringsomfång</span><span class="sxs-lookup"><span data-stu-id="71536-155">Supported create container and upload blob with Encryption Scope setting</span></span>
    - <span data-ttu-id="71536-156">New-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="71536-156">'New-AzRmStorageContainer'</span></span>
    - <span data-ttu-id="71536-157">New-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="71536-157">'New-AzStorageContainer'</span></span>
    - <span data-ttu-id="71536-158">”Set-AzStorageBlobContent”</span><span class="sxs-lookup"><span data-stu-id="71536-158">'Set-AzStorageBlobContent'</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="71536-159">Tack till våra community-deltagare</span><span class="sxs-lookup"><span data-stu-id="71536-159">Thanks to our community contributors</span></span>
* <span data-ttu-id="71536-160">Andreas Wolter (@AndreasWolter), tog bort marknadsföringsspråk, bättre exempelfilter (#13671)</span><span class="sxs-lookup"><span data-stu-id="71536-160">Andreas Wolter (@AndreasWolter), removed marketing language, better example filter (#13671)</span></span>
* <span data-ttu-id="71536-161">Tidjani Belmansour (@BelRarr), uppdatera Get-AzBillingInvoice.md (#13634)</span><span class="sxs-lookup"><span data-stu-id="71536-161">Tidjani Belmansour (@BelRarr), Update Get-AzBillingInvoice.md (#13634)</span></span>
* <span data-ttu-id="71536-162">David Klempfner (@DavidKlempfner)</span><span class="sxs-lookup"><span data-stu-id="71536-162">David Klempfner (@DavidKlempfner)</span></span>
  * <span data-ttu-id="71536-163">Åtgärdade stavfel (#13677)</span><span class="sxs-lookup"><span data-stu-id="71536-163">Fixed spelling mistake (#13677)</span></span>
  * <span data-ttu-id="71536-164">Uppdatera PSMetricNoDetails.cs (#13676)</span><span class="sxs-lookup"><span data-stu-id="71536-164">Update PSMetricNoDetails.cs (#13676)</span></span>
* <span data-ttu-id="71536-165">@kilobyte97, felsökning för borttagning av cmdlet för att ta bort konfiguration (#13655)</span><span class="sxs-lookup"><span data-stu-id="71536-165">@kilobyte97, bugfix for remove cmdlet to delete config (#13655)</span></span>
* <span data-ttu-id="71536-166">@kongou-ae, uppdatera Set-AzFirewall.md (#13727)</span><span class="sxs-lookup"><span data-stu-id="71536-166">@kongou-ae, Update Set-AzFirewall.md (#13727)</span></span>
* <span data-ttu-id="71536-167">@MasterKuat, åtgärda växling mellan rubrik och kod i dokumentationen (#13666)</span><span class="sxs-lookup"><span data-stu-id="71536-167">@MasterKuat, Fix swap between title and code in documentation (#13666)</span></span>
* <span data-ttu-id="71536-168">NickT (@nukeulis), uppdatera Set-AzContext.md (#13702)</span><span class="sxs-lookup"><span data-stu-id="71536-168">NickT (@nukeulis), Update Set-AzContext.md (#13702)</span></span>
* <span data-ttu-id="71536-169">@PaulHCode, uppdatera Start-AzJitNetworkAccessPolicy.md – åtgärda exemplet för att visa rätt cmdlet (#13713)</span><span class="sxs-lookup"><span data-stu-id="71536-169">@PaulHCode, Update Start-AzJitNetworkAccessPolicy.md - Fix the Example to display the proper cmdlet being demonstrated (#13713)</span></span>
* <span data-ttu-id="71536-170">Ryan Borstelmann (@ryanborMSFT), tog bort prenumerations-ID (#13715)</span><span class="sxs-lookup"><span data-stu-id="71536-170">Ryan Borstelmann (@ryanborMSFT), Removed Subscription ID (#13715)</span></span>
* <span data-ttu-id="71536-171">Shashikant Shakya (@shshakya), uppdatera Set-AzSqlDatabase.md (#13674)</span><span class="sxs-lookup"><span data-stu-id="71536-171">Shashikant Shakya (@shshakya), Update Set-AzSqlDatabase.md (#13674)</span></span>
* <span data-ttu-id="71536-172">Sebastian Olsen (@Spacebjorn), uppdatera Get-AzRecoveryServicesBackupItem.md (#13719)</span><span class="sxs-lookup"><span data-stu-id="71536-172">Sebastian Olsen (@Spacebjorn), Update Get-AzRecoveryServicesBackupItem.md (#13719)</span></span>

## <a name="520---december-2020"></a><span data-ttu-id="71536-173">5.2.0 – December 2020</span><span class="sxs-lookup"><span data-stu-id="71536-173">5.2.0 - December 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="71536-174">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="71536-174">Az.Accounts</span></span>
* <span data-ttu-id="71536-175">Det gick att parsa ExpiresOn-tiden från rådatatoken om den inte kunde hämtas från det underliggande biblioteket</span><span class="sxs-lookup"><span data-stu-id="71536-175">Managed to parse ExpiresOn time from raw token if could not get from underlying library</span></span>
* <span data-ttu-id="71536-176">Förbättrat varningsmeddelande om interaktiv autentisering inte är tillgängligt</span><span class="sxs-lookup"><span data-stu-id="71536-176">Improved warning message if Interactive authentication is unavailable</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="71536-177">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="71536-177">Az.ApiManagement</span></span>
* <span data-ttu-id="71536-178">[Icke-bakåtkompatibel ändring] New-AzApiManagementProduct har som standard ingen prenumerationsgräns.</span><span class="sxs-lookup"><span data-stu-id="71536-178">[Breaking change] 'New-AzApiManagementProduct' by default has no subscription limit.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71536-179">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71536-179">Az.Compute</span></span>
* <span data-ttu-id="71536-180">Redigerade get-AzVm för att filtrera efter -Name innan du kontrollerar begränsning på grund av för många resurser.</span><span class="sxs-lookup"><span data-stu-id="71536-180">Edited Get-AzVm to filter by '-Name' prior to checking for throttling due to too many resources.</span></span> 
* <span data-ttu-id="71536-181">Ny cmdlet Start-AzVmssRollingExtensionUpgrade.</span><span class="sxs-lookup"><span data-stu-id="71536-181">New cmdlet 'Start-AzVmssRollingExtensionUpgrade'.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="71536-182">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="71536-182">Az.ContainerRegistry</span></span>
* <span data-ttu-id="71536-183">Parametern Name och värdet från pipeline-indata stöds för Get-AzContainerRegistryUsage [#13605]</span><span class="sxs-lookup"><span data-stu-id="71536-183">Supported parameter 'Name' for and value from pipeline input for 'Get-AzContainerRegistryUsage' [#13605]</span></span>
* <span data-ttu-id="71536-184">Korrigerade undantag för Connect-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="71536-184">Polished exceptions for 'Connect-AzContainerRegistry'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="71536-185">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="71536-185">Az.DataFactory</span></span>
* <span data-ttu-id="71536-186">Uppdaterade ADF .Net SDK-versionen till 4.13.0</span><span class="sxs-lookup"><span data-stu-id="71536-186">Updated ADF .Net SDK version to 4.13.0</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="71536-187">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="71536-187">Az.HealthcareApis</span></span>
* <span data-ttu-id="71536-188">Stöd har lagts till för kundhanterade nycklar</span><span class="sxs-lookup"><span data-stu-id="71536-188">Added support for customer managed keys</span></span>

#### <a name="aziothub"></a><span data-ttu-id="71536-189">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="71536-189">Az.IotHub</span></span>
* <span data-ttu-id="71536-190">Ett problem med SAS-token har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="71536-190">Fixed an issue of SAS token.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="71536-191">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="71536-191">Az.KeyVault</span></span>
* <span data-ttu-id="71536-192">Stöder All som ett alternativ när du ställer in åtkomstprinciper för nyckelvalv</span><span class="sxs-lookup"><span data-stu-id="71536-192">Supported 'all' as an option when setting key vault access policies</span></span>
* <span data-ttu-id="71536-193">Ny version av SecretManagement-modulen stöds [#13366]</span><span class="sxs-lookup"><span data-stu-id="71536-193">Supported new version of SecretManagement module [#13366]</span></span>
* <span data-ttu-id="71536-194">Stöder ByteArray, String, PSCredential och Hashtable för SecretValue i SecretManagementModule [#12190]</span><span class="sxs-lookup"><span data-stu-id="71536-194">Supported ByteArray, String, PSCredential and Hashtable for 'SecretValue' in SecretManagementModule [#12190]</span></span>
* <span data-ttu-id="71536-195">[Icke-bakåtkompatibel ändring] Omdesignat API-ytan för cmdletar som är relaterade till hanterad HSM.</span><span class="sxs-lookup"><span data-stu-id="71536-195">[Breaking change] redesigned the API surface of cmdlets related to managed HSM.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="71536-196">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="71536-196">Az.Monitor</span></span>
* <span data-ttu-id="71536-197">Parametern Rule i New-AzAutoscaleProfile har ändrats för att godkänna en tom lista.</span><span class="sxs-lookup"><span data-stu-id="71536-197">Changed parameter 'Rule' of 'New-AzAutoscaleProfile' to accept empty list.</span></span> <span data-ttu-id="71536-198">[#12903]</span><span class="sxs-lookup"><span data-stu-id="71536-198">[#12903]</span></span>
* <span data-ttu-id="71536-199">Nya cmdletar har lagts till för att stöda skapande av mer flexibla diagnostikinställningar:</span><span class="sxs-lookup"><span data-stu-id="71536-199">Added new cmdlets to support creating diagnostic settings more flexible:</span></span>
    * <span data-ttu-id="71536-200">Get-AzDiagnosticSettingCategory</span><span class="sxs-lookup"><span data-stu-id="71536-200">'Get-AzDiagnosticSettingCategory'</span></span>
    * <span data-ttu-id="71536-201">New-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="71536-201">'New-AzDiagnosticSetting'</span></span>
    * <span data-ttu-id="71536-202">New-AzDiagnosticDetailSetting</span><span class="sxs-lookup"><span data-stu-id="71536-202">'New-AzDiagnosticDetailSetting'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="71536-203">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="71536-203">Az.RecoveryServices</span></span>
* <span data-ttu-id="71536-204">Ändrat hjälptext och parameteruppsättningsnamn till cmdleten Restore-AzRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="71536-204">Made help text and parameter set name changes to 'Restore-AzRecoveryServicesBackupItem' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="71536-205">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71536-205">Az.Resources</span></span>
* <span data-ttu-id="71536-206">Stöd för parametern -Tag har lagts till i Set-AzTemplateSpec och New-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="71536-206">Added '-Tag' parameter support to 'Set-AzTemplateSpec' and 'New-AzTemplateSpec'</span></span>
* <span data-ttu-id="71536-207">Stöd för taggvisning har lagts till som standard för formatering av Mallspecifikationer</span><span class="sxs-lookup"><span data-stu-id="71536-207">Added Tag display support to default formatter for Template Specs</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="71536-208">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="71536-208">Az.ServiceFabric</span></span>
* <span data-ttu-id="71536-209">Lade till exempel i Set-AzServiceFabricSetting med parametern SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="71536-209">Added example to 'Set-AzServiceFabricSetting' with SettingsSectionDescription param</span></span>
* <span data-ttu-id="71536-210">Uppdaterade programrelaterade cmdletar för att anropa att stöd endast finns för ARM-distribuerade resurser</span><span class="sxs-lookup"><span data-stu-id="71536-210">Updated application related cmdlets to call out that support is only for ARM deployed resources</span></span>
* <span data-ttu-id="71536-211">Markerat för cmdletarna Add-AzureRmServiceFabricClusterCertificate och Remove-AzureRmServiceFabricClusterCertificate med utfasningsklustercertifikat</span><span class="sxs-lookup"><span data-stu-id="71536-211">Marked for deprecation cluster cert cmdlets 'Add-AzureRmServiceFabricClusterCertificate' and 'Remove-AzureRmServiceFabricClusterCertificate'</span></span>

#### <a name="azsql"></a><span data-ttu-id="71536-212">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71536-212">Az.Sql</span></span>
* <span data-ttu-id="71536-213">Lade till SecondaryType till följande:</span><span class="sxs-lookup"><span data-stu-id="71536-213">Added SecondaryType to the following:</span></span> 
    - <span data-ttu-id="71536-214">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="71536-214">'New-AzSqlDatabase'</span></span>
    - <span data-ttu-id="71536-215">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="71536-215">'Set-AzSqlDatabase'</span></span>
    - <span data-ttu-id="71536-216">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="71536-216">'New-AzSqlDatabaseSecondary'</span></span>
* <span data-ttu-id="71536-217">Lade till HighAvailabilityReplicaCount till följande:</span><span class="sxs-lookup"><span data-stu-id="71536-217">Added HighAvailabilityReplicaCount to the following:</span></span> 
    - <span data-ttu-id="71536-218">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="71536-218">'New-AzSqlDatabase'</span></span>
    - <span data-ttu-id="71536-219">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="71536-219">'Set-AzSqlDatabase'</span></span>
* <span data-ttu-id="71536-220">Gjorde ReadReplicaCount till ett alias för HighAvailabilityReplicaCount i följande:</span><span class="sxs-lookup"><span data-stu-id="71536-220">Made ReadReplicaCount an alias of HighAvailabilityReplicaCount in the following:</span></span> 
    - <span data-ttu-id="71536-221">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="71536-221">'New-AzSqlDatabase'</span></span>
    - <span data-ttu-id="71536-222">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="71536-222">'Set-AzSqlDatabase'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="71536-223">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="71536-223">Az.Storage</span></span>
* <span data-ttu-id="71536-224">Stöder överföring av Azure-filstorlek på upp till 4 TiB</span><span class="sxs-lookup"><span data-stu-id="71536-224">Supported upload Azure File size up to 4 TiB</span></span>
    - <span data-ttu-id="71536-225">”Set-AzStorageFileContent”</span><span class="sxs-lookup"><span data-stu-id="71536-225">'Set-AzStorageFileContent'</span></span>
* <span data-ttu-id="71536-226">Uppgraderade Azure.Storage.Blobs till 12.7.0</span><span class="sxs-lookup"><span data-stu-id="71536-226">Upgraded Azure.Storage.Blobs to 12.7.0</span></span>
* <span data-ttu-id="71536-227">Uppgraderade Azure.Storage.Files.Shares till 12.5.0</span><span class="sxs-lookup"><span data-stu-id="71536-227">Upgraded Azure.Storage.Files.Shares to 12.5.0</span></span>
* <span data-ttu-id="71536-228">Uppgraderade Azure.Storage.Files.DataLake till 12.5.0</span><span class="sxs-lookup"><span data-stu-id="71536-228">Upgraded Azure.Storage.Files.DataLake to 12.5.0</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="71536-229">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="71536-229">Az.StorageSync</span></span>
* <span data-ttu-id="71536-230">Principfunktionen för synkronisering av nivåer har lagts till med hämtningsprincip och lokalt cacheläge</span><span class="sxs-lookup"><span data-stu-id="71536-230">Added Sync tiering policy feature with download policy and local cache mode</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="71536-231">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="71536-231">Az.Websites</span></span>
* <span data-ttu-id="71536-232">Förhindra dubbletter av åtkomstbegränsningsregler</span><span class="sxs-lookup"><span data-stu-id="71536-232">Prevent duplicate access restriction rules</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="71536-233">Tack till våra community-deltagare</span><span class="sxs-lookup"><span data-stu-id="71536-233">Thanks to our community contributors</span></span>
* <span data-ttu-id="71536-234">Andrew Dawson (@dawsonar802), uppdatera Get-AzKeyVaultCertificate.md – hämta certifikat och spara det som pfx-avsnitt som fungerar med PowerShell Core (#13557)</span><span class="sxs-lookup"><span data-stu-id="71536-234">Andrew Dawson (@dawsonar802), Update Get-AzKeyVaultCertificate.md - Get cert and save it as pfx section to work with PowerShell Core (#13557)</span></span>
* <span data-ttu-id="71536-235">@iviark, sjukvårds-API:er PowerShell BYOK-uppdateringar (#13518)</span><span class="sxs-lookup"><span data-stu-id="71536-235">@iviark, Healthcare APIs Powershell BYOK Updates (#13518)</span></span>
* <span data-ttu-id="71536-236">John Duckmanton (@johnduckmanton), korrigera stavning av TagPatchOperation (#13508)</span><span class="sxs-lookup"><span data-stu-id="71536-236">John Duckmanton (@johnduckmanton), Correct spelling of TagPatchOperation (#13508)</span></span>
* <span data-ttu-id="71536-237">Michael James (@mikejwhat)</span><span class="sxs-lookup"><span data-stu-id="71536-237">Michael James (@mikejwhat)</span></span>
  * <span data-ttu-id="71536-238">Hjälp till att fixa Get-AzLogicAppRunHistory (#13513)</span><span class="sxs-lookup"><span data-stu-id="71536-238">Get-AzLogicAppRunHistory Help Tidy (#13513)</span></span>
* <span data-ttu-id="71536-239">Richard de Zwart (@mountain65)</span><span class="sxs-lookup"><span data-stu-id="71536-239">Richard de Zwart (@mountain65)</span></span>
  * <span data-ttu-id="71536-240">Uppdatera Update-AzAppConfigurationStore.md (#13485)</span><span class="sxs-lookup"><span data-stu-id="71536-240">Update Update-AzAppConfigurationStore.md (#13485)</span></span>
  * <span data-ttu-id="71536-241">Uppdatera New-AzCosmosDBAccount.md (#13490)</span><span class="sxs-lookup"><span data-stu-id="71536-241">Update New-AzCosmosDBAccount.md (#13490)</span></span>
* <span data-ttu-id="71536-242">@SteppingRazor, New-AzApiManagementProduct: Ändra standardvärdet för parametern SubscriptionsLimit till None (#13457)</span><span class="sxs-lookup"><span data-stu-id="71536-242">@SteppingRazor, New-AzApiManagementProduct: Change SubscriptionsLimit parameter default value to None (#13457)</span></span>
* <span data-ttu-id="71536-243">Steve Burkett (@SteveBurkettNZ), korrigera skrivfel för parametern WorkspaceResourceId i exemplet (#13589)</span><span class="sxs-lookup"><span data-stu-id="71536-243">Steve Burkett (@SteveBurkettNZ), Fix Typo for WorkspaceResourceId parameter in example (#13589)</span></span>

## <a name="510---november-2020"></a><span data-ttu-id="71536-244">5.1.0 – November 2020</span><span class="sxs-lookup"><span data-stu-id="71536-244">5.1.0 - November 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="71536-245">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="71536-245">Az.Accounts</span></span>
* <span data-ttu-id="71536-246">Korrigerade ett problem där TenantId kanske inte kan respekteras när ”Connect-AzAccount -DeviceCode” används [#13477]</span><span class="sxs-lookup"><span data-stu-id="71536-246">Fixed an issue that TenantId may be not respected if using 'Connect-AzAccount -DeviceCode'[#13477]</span></span>
* <span data-ttu-id="71536-247">Lade till en ny cmdlet: ”Get-AzAccessToken”</span><span class="sxs-lookup"><span data-stu-id="71536-247">Added new cmdlet 'Get-AzAccessToken'</span></span>
* <span data-ttu-id="71536-248">Korrigerade ett problem som uppstår om det inte går att komma åt sökvägen till användarprofilen</span><span class="sxs-lookup"><span data-stu-id="71536-248">Fixed an issue that error happens if user profile path is inaccessible</span></span>
* <span data-ttu-id="71536-249">Korrigerade ett problem som orsakar ett skriv-objektfel under Connect-AzAccount [#13419]</span><span class="sxs-lookup"><span data-stu-id="71536-249">Fixed an issue causing Write-Object error during Connect-AzAccount [#13419]</span></span>
* <span data-ttu-id="71536-250">Lade till parametern ”ContainerRegistryEndpointSuffix” för: ”Add-AzEnvironment”, ”Set-AzEnvironment”</span><span class="sxs-lookup"><span data-stu-id="71536-250">Added parameter 'ContainerRegistryEndpointSuffix' to: 'Add-AzEnvironment', 'Set-AzEnvironment'</span></span> 
* <span data-ttu-id="71536-251">Stöd för att avbryta inloggning genom att trycka på <kbd>CTRL</kbd>+<kbd>C</kbd></span><span class="sxs-lookup"><span data-stu-id="71536-251">Supported interrupting login by hitting <kbd>CTRL</kbd>+<kbd>C</kbd></span></span>
* <span data-ttu-id="71536-252">Korrigerade ett problem som gjorde att ”Connect-AzAccount -KeyVaultAccessToken” inte fungerade [#13127]</span><span class="sxs-lookup"><span data-stu-id="71536-252">Fixed an issue causing 'Connect-AzAccount -KeyVaultAccessToken' not working [#13127]</span></span>
* <span data-ttu-id="71536-253">Korrigerade null-referens och skiftlägesokänslig metod i ”Invoke-AzRestMethod”</span><span class="sxs-lookup"><span data-stu-id="71536-253">Fixed null reference and method case insensitive in 'Invoke-AzRestMethod'</span></span>

#### <a name="azaks"></a><span data-ttu-id="71536-254">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="71536-254">Az.Aks</span></span>
* <span data-ttu-id="71536-255">Korrigerade problemet att användaren inte kunde använda tjänstens huvudnamn för att skapa ett nytt Kubernetes-kluster.</span><span class="sxs-lookup"><span data-stu-id="71536-255">Fixed the issue that user cannot use service principal to create a new Kubernetes cluster.</span></span> <span data-ttu-id="71536-256">[#13012]</span><span class="sxs-lookup"><span data-stu-id="71536-256">[#13012]</span></span>

#### <a name="azappconfiguration"></a><span data-ttu-id="71536-257">Az.AppConfiguration</span><span class="sxs-lookup"><span data-stu-id="71536-257">Az.AppConfiguration</span></span>
* <span data-ttu-id="71536-258">Allmän tillgänglighet för modulen ”Az.AppConfiguration”</span><span class="sxs-lookup"><span data-stu-id="71536-258">General availability of 'Az.AppConfiguration' module</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="71536-259">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="71536-259">Az.DataFactory</span></span>
* <span data-ttu-id="71536-260">Förbättrade felmeddelandet för kommandot ”New-AzDataFactoryV2LinkedServiceEncryptedCredential”</span><span class="sxs-lookup"><span data-stu-id="71536-260">Improved error message of 'New-AzDataFactoryV2LinkedServiceEncryptedCredential' command</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="71536-261">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="71536-261">Az.DataLakeStore</span></span>
* <span data-ttu-id="71536-262">Uppdaterade SDK för ADLS-dataplanen till 1.2.4-alpha.</span><span class="sxs-lookup"><span data-stu-id="71536-262">Updated ADLS dataplane SDK to 1.2.4-alpha.</span></span> <span data-ttu-id="71536-263">Ändringar: https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-124-alpha</span><span class="sxs-lookup"><span data-stu-id="71536-263">Changes:https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-124-alpha</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="71536-264">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="71536-264">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="71536-265">Lade till nya cmdletar för MSIX-paket och uppdaterade program-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="71536-265">Added new MSIX Package cmdlets and updated Applications cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="71536-266">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="71536-266">Az.EventHub</span></span>
* <span data-ttu-id="71536-267">Korrigerade klusterkommandon för EventHub-kluster utan taggar</span><span class="sxs-lookup"><span data-stu-id="71536-267">Fixed Cluster commands for EventHub cluster without tags</span></span>
* <span data-ttu-id="71536-268">Uppdaterade hjälptext för PartnerNamespace i AzEventHubGeoDRConfiguration-kommandon</span><span class="sxs-lookup"><span data-stu-id="71536-268">Updated help text for PartnerNamespace of AzEventHubGeoDRConfiguration commands</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="71536-269">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="71536-269">Az.HDInsight</span></span>
* <span data-ttu-id="71536-270">Lade till parametrarna ”ResourceProviderConnection” och ”PrivateLink” till cmdleten ”New-AzHDInsightCluster” för att stödja funktionen för att vidarebefordra utgående och privata länkar</span><span class="sxs-lookup"><span data-stu-id="71536-270">Add parameters 'ResourceProviderConnection' and 'PrivateLink' to cmdlet 'New-AzHDInsightCluster' to support relay outbound and private link feature</span></span>
* <span data-ttu-id="71536-271">Lade till parametern ”AmbariDatabase” till cmdleten ”New-AzHDInsightCluster” för att stödja en anpassad Ambari-databasfunktion</span><span class="sxs-lookup"><span data-stu-id="71536-271">Add parameter 'AmbariDatabase' to cmdlet 'New-AzHDInsightCluster' to support custom Ambari database feature</span></span>
* <span data-ttu-id="71536-272">Lade till det accepterade värdet ”AmbariDatabase” till parametern ”MetastoreType” för cmdleten ”Add-AzHDInsightMetastore”</span><span class="sxs-lookup"><span data-stu-id="71536-272">Add accept value 'AmbariDatabase' to the parameter 'MetastoreType' of the cmdlet 'Add-AzHDInsightMetastore'</span></span>

#### <a name="aziothub"></a><span data-ttu-id="71536-273">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="71536-273">Az.IotHub</span></span>
* <span data-ttu-id="71536-274">Tillät taggar i cmdlet för att skapa i IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="71536-274">Allowed tags in IoT Hub create cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="71536-275">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="71536-275">Az.KeyVault</span></span>
* <span data-ttu-id="71536-276">Stöd för att uppdatera nyckelvalvstagg</span><span class="sxs-lookup"><span data-stu-id="71536-276">Supported updating key vault tag</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="71536-277">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="71536-277">Az.LogicApp</span></span>
* <span data-ttu-id="71536-278">Korrigerade så att Get-AzLogicAppRunHistory endast hämtar den första sidan med resultat</span><span class="sxs-lookup"><span data-stu-id="71536-278">Fixed for Get-AzLogicAppRunHistory only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71536-279">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71536-279">Az.Network</span></span>
* <span data-ttu-id="71536-280">Uppdaterade cmdletarna här under</span><span class="sxs-lookup"><span data-stu-id="71536-280">Updated below cmdlet</span></span> 
    - <span data-ttu-id="71536-281">”New-AzLoadBalancerFrontendIpConfigCommand”, ”Set-AzLoadBalancerFrontendIpConfigCommand”, ”Add-AzLoadBalancerFrontendIpConfigCommand”:</span><span class="sxs-lookup"><span data-stu-id="71536-281">'New-AzLoadBalancerFrontendIpConfigCommand', 'Set-AzLoadBalancerFrontendIpConfigCommand', 'Add-AzLoadBalancerFrontendIpConfigCommand':</span></span>
        - <span data-ttu-id="71536-282">Lade till egenskapen PublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="71536-282">Added PublicIpAddressPrefix property</span></span>
        - <span data-ttu-id="71536-283">Lade till egenskapen PublicIpAddressPrefixId</span><span class="sxs-lookup"><span data-stu-id="71536-283">Added PublicIpAddressPrefixId property</span></span>
* <span data-ttu-id="71536-284">Lade till nya egenskaper till i följande cmdletar för att möjliggöra global belastningsutjämning:</span><span class="sxs-lookup"><span data-stu-id="71536-284">Added new properties to the following cmdlets to allow for global load balancing</span></span>
    - <span data-ttu-id="71536-285">”New-AzLoadBalancer”:</span><span class="sxs-lookup"><span data-stu-id="71536-285">'New-AzLoadBalancer':</span></span>
        - <span data-ttu-id="71536-286">Lade till egenskapen SKU-nivå</span><span class="sxs-lookup"><span data-stu-id="71536-286">Added Sku Tier property</span></span>
    - <span data-ttu-id="71536-287">”New-AzPuplicIpAddress”:</span><span class="sxs-lookup"><span data-stu-id="71536-287">'New-AzPuplicIpAddress':</span></span>
        - <span data-ttu-id="71536-288">Lade till egenskapen SKU-nivå</span><span class="sxs-lookup"><span data-stu-id="71536-288">Added Sku Tier property</span></span>
    - <span data-ttu-id="71536-289">”New-AzPublicIpPrefix”:</span><span class="sxs-lookup"><span data-stu-id="71536-289">'New-AzPublicIpPrefix':</span></span>
        - <span data-ttu-id="71536-290">Lade till egenskapen SKU-nivå</span><span class="sxs-lookup"><span data-stu-id="71536-290">Added Sku Tier property</span></span>
    - <span data-ttu-id="71536-291">”New-AzLoadBalancerBackendAddressConfig”:</span><span class="sxs-lookup"><span data-stu-id="71536-291">'New-AzLoadBalancerBackendAddressConfig':</span></span>
        - <span data-ttu-id="71536-292">Lade till egenskapen LoadBalancerFrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="71536-292">Added LoadBalancerFrontendIPConfigurationId property</span></span>
* <span data-ttu-id="71536-293">Uppdaterade planer att göra varningar för följande cmdletar inaktuella: -”New-AzVirtualHubRoute”, -”New-AzVirtualHubRouteTable”, -”Add-AzVirtualHubRoute”, -”Add-AzVirtualHubRouteTable” -”Get-AzVirtualHubRouteTable” och -”Remove-AzVirtualHubRouteTable”</span><span class="sxs-lookup"><span data-stu-id="71536-293">Updated planning to deprecate warnings for the following cmdlets   -'New-AzVirtualHubRoute'   -'New-AzVirtualHubRouteTable'   -'Add-AzVirtualHubRoute'   -'Add-AzVirtualHubRouteTable'   -'Get-AzVirtualHubRouteTable'   -'Remove-AzVirtualHubRouteTable'</span></span>
* <span data-ttu-id="71536-294">Lade till planer att göra varningar för argumentet ”RouteTable” inaktuella för följande cmdletar: -”New-AzVirtualHub”, -”Set-AzVirtualHub” och -”Update-AzVirtualHub”</span><span class="sxs-lookup"><span data-stu-id="71536-294">Added planning to deprecate warnings on the argument 'RouteTable' for the following cmdlets   -'New-AzVirtualHub'   -'Set-AzVirtualHub'   -'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="71536-295">Gjorde argumenten ”-MinScaleUnits” och ”-MaxScaleUnits” valfria i ”Set-AzExpressRouteGateway”</span><span class="sxs-lookup"><span data-stu-id="71536-295">Made arguments '-MinScaleUnits' and '-MaxScaleUnits' optional in 'Set-AzExpressRouteGateway'</span></span>
* <span data-ttu-id="71536-296">Lade till nya cmdletar för att stödja ömsesidig autentisering och SSL-profiler på Application Gateway</span><span class="sxs-lookup"><span data-stu-id="71536-296">Added new cmdlets to support Mutual Authentication and SSL Profiles on Application Gateway</span></span>
    - <span data-ttu-id="71536-297">”Get-AzApplicationGatewayClientAuthConfiguration”</span><span class="sxs-lookup"><span data-stu-id="71536-297">'Get-AzApplicationGatewayClientAuthConfiguration'</span></span>
    - <span data-ttu-id="71536-298">”New-AzApplicationGatewayClientAuthConfiguration”</span><span class="sxs-lookup"><span data-stu-id="71536-298">'New-AzApplicationGatewayClientAuthConfiguration'</span></span>
    - <span data-ttu-id="71536-299">”Remove-AzApplicationGatewayClientAuthConfiguration”</span><span class="sxs-lookup"><span data-stu-id="71536-299">'Remove-AzApplicationGatewayClientAuthConfiguration'</span></span>
    - <span data-ttu-id="71536-300">”Set-AzApplicationGatewayClientAuthConfiguration”</span><span class="sxs-lookup"><span data-stu-id="71536-300">'Set-AzApplicationGatewayClientAuthConfiguration'</span></span>
    - <span data-ttu-id="71536-301">”Add-AzApplicationGatewayTrustedClientCertificate”</span><span class="sxs-lookup"><span data-stu-id="71536-301">'Add-AzApplicationGatewayTrustedClientCertificate'</span></span> 
    - <span data-ttu-id="71536-302">”Get-AzApplicationGatewayTrustedClientCertificate”</span><span class="sxs-lookup"><span data-stu-id="71536-302">'Get-AzApplicationGatewayTrustedClientCertificate'</span></span> 
    - <span data-ttu-id="71536-303">”New-AzApplicationGatewayTrustedClientCertificate”</span><span class="sxs-lookup"><span data-stu-id="71536-303">'New-AzApplicationGatewayTrustedClientCertificate'</span></span> 
    - <span data-ttu-id="71536-304">”Remove-AzApplicationGatewayTrustedClientCertificate”</span><span class="sxs-lookup"><span data-stu-id="71536-304">'Remove-AzApplicationGatewayTrustedClientCertificate'</span></span> 
    - <span data-ttu-id="71536-305">”Set-AzApplicationGatewayTrustedClientCertificate”</span><span class="sxs-lookup"><span data-stu-id="71536-305">'Set-AzApplicationGatewayTrustedClientCertificate'</span></span>
    - <span data-ttu-id="71536-306">”Add-AzApplicationGatewaySslProfile”</span><span class="sxs-lookup"><span data-stu-id="71536-306">'Add-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="71536-307">”Get-AzApplicationGatewaySslProfile”</span><span class="sxs-lookup"><span data-stu-id="71536-307">'Get-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="71536-308">”New-AzApplicationGatewaySslProfile”</span><span class="sxs-lookup"><span data-stu-id="71536-308">'New-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="71536-309">”Remove-AzApplicationGatewaySslProfile”</span><span class="sxs-lookup"><span data-stu-id="71536-309">'Remove-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="71536-310">”Set-AzApplicationGatewaySslProfile”</span><span class="sxs-lookup"><span data-stu-id="71536-310">'Set-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="71536-311">”Get-AzApplicationGatewaySslProfilePolicy”</span><span class="sxs-lookup"><span data-stu-id="71536-311">'Get-AzApplicationGatewaySslProfilePolicy'</span></span>
    - <span data-ttu-id="71536-312">”Remove-AzApplicationGatewaySslProfilePolicy”</span><span class="sxs-lookup"><span data-stu-id="71536-312">'Remove-AzApplicationGatewaySslProfilePolicy'</span></span>
    - <span data-ttu-id="71536-313">”Set-AzApplicationGatewaySslProfilePolicy”</span><span class="sxs-lookup"><span data-stu-id="71536-313">'Set-AzApplicationGatewaySslProfilePolicy'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="71536-314">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="71536-314">Az.RecoveryServices</span></span>
* <span data-ttu-id="71536-315">Specificera att principen BackupTime är i UTC.</span><span class="sxs-lookup"><span data-stu-id="71536-315">Specifying policy BackupTime is in UTC.</span></span>
* <span data-ttu-id="71536-316">Ändra varning för icke-bakåtkompatibel ändring i cmdleten Get-AzRecoveryServicesBackupJobDetails.</span><span class="sxs-lookup"><span data-stu-id="71536-316">Modifying breaking change warning in Get-AzRecoveryServicesBackupJobDetails cmdlet.</span></span>
* <span data-ttu-id="71536-317">Uppdaterar exempelskriptets hjälptext för cmdleten Set-AzRecoveryServicesBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="71536-317">Updating sample script help text for Set-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="71536-318">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71536-318">Az.Resources</span></span>
* <span data-ttu-id="71536-319">Korrigerade ett problem där konsekvensgranskning visade två omfång för resursgrupper med olika skiftlägen</span><span class="sxs-lookup"><span data-stu-id="71536-319">Fixed an issue where What-If shows two resource group scopes with different casing</span></span>
* <span data-ttu-id="71536-320">Uppdaterade ”Export-AzResourceGroup” för att använda SDK.</span><span class="sxs-lookup"><span data-stu-id="71536-320">Updated 'Export-AzResourceGroup' to use the SDK.</span></span>
* <span data-ttu-id="71536-321">Lade till kulturinformation för att parsa metoder</span><span class="sxs-lookup"><span data-stu-id="71536-321">Added culture info to parse methods</span></span>

#### <a name="azsql"></a><span data-ttu-id="71536-322">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71536-322">Az.Sql</span></span>
* <span data-ttu-id="71536-323">Korrigerade problem där Set-AzSqlDatabaseAudit inte hade stöd för databas i hyperskala och databasversionen inte kunde fastställas</span><span class="sxs-lookup"><span data-stu-id="71536-323">Fixed issues where Set-AzSqlDatabaseAudit were not support Hyperscale database and database edition cannot be determined</span></span>
* <span data-ttu-id="71536-324">Lade till MaintenanceConfigurationId för ”New-AzSqlInstance” och ”Set-AzSqlInstance”</span><span class="sxs-lookup"><span data-stu-id="71536-324">Added MaintenanceConfigurationId to 'New-AzSqlInstance' and 'Set-AzSqlInstance'</span></span>
* <span data-ttu-id="71536-325">Korrigerade en bugg i GetAzureSqlDatabaseReplicationLink.cs där parametern PartnerServerName kontrollerades efter värde i stället för nyckel</span><span class="sxs-lookup"><span data-stu-id="71536-325">Fixed a bug in GetAzureSqlDatabaseReplicationLink.cs where PartnerServerName parameter was being checked for by value instead of key</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="71536-326">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="71536-326">Az.Websites</span></span>
* <span data-ttu-id="71536-327">Lade till stöd för nya funktioner för åtkomstbegränsning: ServiceTag, flera IP-adresser och HTTP-rubriker</span><span class="sxs-lookup"><span data-stu-id="71536-327">Added support for new access restriction features: ServiceTag, multi-ip and http-headers</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="71536-328">Tack till våra community-deltagare</span><span class="sxs-lookup"><span data-stu-id="71536-328">Thanks to our community contributors</span></span>
* <span data-ttu-id="71536-329">John Q. Martin (@johnmart82), lägger till nödvändig brandväggsinformation (#13385)</span><span class="sxs-lookup"><span data-stu-id="71536-329">John Q. Martin (@johnmart82), Adding firewall prerequisite information (#13385)</span></span>
* <span data-ttu-id="71536-330">Manikandan Duraisamy (@madurais-msft), korrigerade argumentet PublicSubnetName (#13417)</span><span class="sxs-lookup"><span data-stu-id="71536-330">Manikandan Duraisamy (@madurais-msft), Corrected the PublicSubnetName argument (#13417)</span></span>
* <span data-ttu-id="71536-331">@mahortas, uppdatera parametervärden för -HostName (#13349)</span><span class="sxs-lookup"><span data-stu-id="71536-331">@mahortas, Update for -HostNames parameter values (#13349)</span></span>
* <span data-ttu-id="71536-332">@MariachiForHire, lade till TrafficAnalyticsInterval-värden som stöds (#13304)</span><span class="sxs-lookup"><span data-stu-id="71536-332">@MariachiForHire, added supported TrafficAnalyticsInterval values (#13304)</span></span>
* <span data-ttu-id="71536-333">Michael Jonas (@mikejwhat), tillåt att Get-AzLogicAppRunHistory returnerar fler än 30 poster (#13393)</span><span class="sxs-lookup"><span data-stu-id="71536-333">Michael James (@mikejwhat), Allow Get-AzLogicAppRunHistory to return more than 30 entries (#13393)</span></span>
* <span data-ttu-id="71536-334">Shashikant Shakya (@shshakya), uppdatera Restore-AzSqlInstanceDatabase.md (#13404)</span><span class="sxs-lookup"><span data-stu-id="71536-334">Shashikant Shakya (@shshakya), Update Restore-AzSqlInstanceDatabase.md (#13404)</span></span>

## <a name="500---october-2020"></a><span data-ttu-id="71536-335">5.0.0 – Oktober 2020</span><span class="sxs-lookup"><span data-stu-id="71536-335">5.0.0 - October 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="71536-336">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="71536-336">Az.Accounts</span></span>
* <span data-ttu-id="71536-337">[Icke-bakåtkompatibel ändring] Tog bort ”Get-AzProfile” och ”Select-AzProfile”</span><span class="sxs-lookup"><span data-stu-id="71536-337">[Breaking Change] Removed 'Get-AzProfile' and 'Select-AzProfile'</span></span>
* <span data-ttu-id="71536-338">Ersatte Azure Directory Authentication Library med Microsoft Authentication Library (MSAL)</span><span class="sxs-lookup"><span data-stu-id="71536-338">Replaced Azure Directory Authentication Library with Microsoft Authentication Library(MSAL)</span></span>

#### <a name="azaks"></a><span data-ttu-id="71536-339">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="71536-339">Az.Aks</span></span>
* <span data-ttu-id="71536-340">[Icke-bakåtkompatibel ändring] Tog bort aliaset ”ClientIdAndSecret” i ”New-AzAksCluster” och ”Set-AzAksCluster”.</span><span class="sxs-lookup"><span data-stu-id="71536-340">[Breaking Change] Removed parameter alias 'ClientIdAndSecret' in 'New-AzAksCluster' and 'Set-AzAksCluster'.</span></span>
* <span data-ttu-id="71536-341">[Icke-bakåtkompatibel ändring] Ändrade standardvärdet för ”NodeVmSetType” i ”New-AzAksCluster” från ”AvailabilitySet” till ”VirtualMachineScaleSets”.</span><span class="sxs-lookup"><span data-stu-id="71536-341">[Breaking Change] Changed the default value of 'NodeVmSetType' in 'New-AzAksCluster' from 'AvailabilitySet' to 'VirtualMachineScaleSets'.</span></span>
* <span data-ttu-id="71536-342">[Icke-bakåtkompatibel ändring] Ändrade standardvärdet för ”NetworkPlugin” i ”New-AzAksCluster” från ”None” till ”azure”.</span><span class="sxs-lookup"><span data-stu-id="71536-342">[Breaking Change] Changed the default value of 'NetworkPlugin' in 'New-AzAksCluster' from 'None' to 'azure'.</span></span>
* <span data-ttu-id="71536-343">[Icke-bakåtkompatibel ändring] Tog bort parametern ”NodeOsType” i ”New-AzAksCluster” eftersom den endast har stöd för Linux med ett värde.</span><span class="sxs-lookup"><span data-stu-id="71536-343">[Breaking Change] Removed parameter 'NodeOsType' in 'New-AzAksCluster' as it supports only one value Linux.</span></span>

#### <a name="azbilling"></a><span data-ttu-id="71536-344">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="71536-344">Az.Billing</span></span>
* <span data-ttu-id="71536-345">Lade till cmdleten ”Get-AzBillingAccount”</span><span class="sxs-lookup"><span data-stu-id="71536-345">Added 'Get-AzBillingAccount' cmdlet</span></span>
* <span data-ttu-id="71536-346">Lade till cmdleten ”Get-AzBillingProfile”</span><span class="sxs-lookup"><span data-stu-id="71536-346">Added 'Get-AzBillingProfile' cmdlet</span></span>
* <span data-ttu-id="71536-347">Lade till cmdleten ”Get-AzInvoiceSection”</span><span class="sxs-lookup"><span data-stu-id="71536-347">Added 'Get-AzInvoiceSection' cmdlet</span></span>
* <span data-ttu-id="71536-348">Lade till nya parametrar i cmdleten ”Get-AzBillingInvoice”</span><span class="sxs-lookup"><span data-stu-id="71536-348">Added new parameters in 'Get-AzBillingInvoice' cmdlet</span></span>
* <span data-ttu-id="71536-349">Tog bort egenskaperna ”DownloadUrlExpiry”, ”Type” och ”BillingPeriodNames” från svaret för cmdleten ”Get-AzBillingInvoic”</span><span class="sxs-lookup"><span data-stu-id="71536-349">Removed properties DownloadUrlExpiry, Type, BillingPeriodNames from the response of Get-AzBillingInvoice cmdlet</span></span>

#### <a name="azcdn"></a><span data-ttu-id="71536-350">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="71536-350">Az.Cdn</span></span>
* <span data-ttu-id="71536-351">Lade till cmdletar för att stödja funktioner för flera ursprung och privat länk</span><span class="sxs-lookup"><span data-stu-id="71536-351">Added cmdlets to support multi-origin and private link functionality</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="71536-352">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="71536-352">Az.CognitiveServices</span></span>
* <span data-ttu-id="71536-353">Uppdaterade SDK till 7.4.0-preview.</span><span class="sxs-lookup"><span data-stu-id="71536-353">Updated SDK to 7.4.0-preview.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71536-354">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71536-354">Az.Compute</span></span>
* <span data-ttu-id="71536-355">Lade till parametern ”-VmssId” till ”New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="71536-355">Added '-VmssId' parameter to 'New-AzVm'</span></span>
* <span data-ttu-id="71536-356">Lade till parametern ”PlatformFaultDomainCount” till cmdleten ”New-AzVmss”.</span><span class="sxs-lookup"><span data-stu-id="71536-356">Added 'PlatformFaultDomainCount' parameter to the 'New-AzVmss' cmdlet.</span></span>
* <span data-ttu-id="71536-357">Ny cmdlet: ”Get-AzDiskEncryptionSetAssociatedResource”</span><span class="sxs-lookup"><span data-stu-id="71536-357">New cmdlet 'Get-AzDiskEncryptionSetAssociatedResource'</span></span>
* <span data-ttu-id="71536-358">Lade till de valfria parametrarna ”Tier” och ”LogicalSectorSize” till cmdleten ”New-AzDiskConfig”.</span><span class="sxs-lookup"><span data-stu-id="71536-358">Added 'Tier' and 'LogicalSectorSize' optional parameters to the New-AzDiskConfig cmdlet.</span></span> 
* <span data-ttu-id="71536-359">Lade till de valfria parametrarna ”Tier”, ”MaxSharesCount”, ”DiskIOPSReadOnly” och ”DiskMBpsReadOnly” till cmdleten ”New-AzDiskUpdateConfig”.</span><span class="sxs-lookup"><span data-stu-id="71536-359">Added 'Tier', 'MaxSharesCount', 'DiskIOPSReadOnly', and 'DiskMBpsReadOnly' optional parameters to the 'New-AzDiskUpdateConfig' cmdlet.</span></span> 

#### <a name="azcontainerregistry"></a><span data-ttu-id="71536-360">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="71536-360">Az.ContainerRegistry</span></span>
* <span data-ttu-id="71536-361">[Icke-bakåtkompatibel ändring] Uppdaterar API-versionen till 2019-05-01</span><span class="sxs-lookup"><span data-stu-id="71536-361">[Breaking Change] Updates API version to 2019-05-01</span></span>
* <span data-ttu-id="71536-362">[Icke-bakåtkompatibel ändring] Tog bort SKU:n ”Classic” och parametern ”StorageAccountName” från ”New-AzContainerRegistry”</span><span class="sxs-lookup"><span data-stu-id="71536-362">[Breaking Change] Removed SKU 'Classic' and parameter 'StorageAccountName' from 'New-AzContainerRegistry'</span></span>
* <span data-ttu-id="71536-363">Lade till nya cmdletar: ”Connect-AzContainerRegistry”, ”Import-AzContainerRegistry”, ”Get-AzContainerRegistryUsage”, ”New-AzContainerRegistryNetworkRule”, ”Set-AzContainerRegistryNetworkRule”</span><span class="sxs-lookup"><span data-stu-id="71536-363">Added New cmdlets: 'Connect-AzContainerRegistry', 'Import-AzContainerRegistry', 'Get-AzContainerRegistryUsage', 'New-AzContainerRegistryNetworkRule', 'Set-AzContainerRegistryNetworkRule'</span></span>
* <span data-ttu-id="71536-364">Lade till den nya parametern ”NetworkRuleSet” till ”Update-AzContainerRegistry”</span><span class="sxs-lookup"><span data-stu-id="71536-364">Added new parameter 'NetworkRuleSet' to 'Update-AzContainerRegistry'</span></span>

#### <a name="azdatabricks"></a><span data-ttu-id="71536-365">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="71536-365">Az.Databricks</span></span>
* <span data-ttu-id="71536-366">Korrigerade en bugg som kunde leda till att en uppdatering av en Databricks-arbetsyta utan `-EncryptionKeyVersion` misslyckades.</span><span class="sxs-lookup"><span data-stu-id="71536-366">Fixed a bug that may cause updating databricks workspace without `-EncryptionKeyVersion` to fail.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="71536-367">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="71536-367">Az.DataFactory</span></span>
* <span data-ttu-id="71536-368">Uppdaterade ADF .Net SDK-versionen till 4.12.0</span><span class="sxs-lookup"><span data-stu-id="71536-368">Updated ADF .Net SDK version to 4.12.0</span></span>
* <span data-ttu-id="71536-369">Uppdaterade ADF-krypteringsklientens SDK-version till 4.14.7587.7</span><span class="sxs-lookup"><span data-stu-id="71536-369">Updated ADF encryption client SDK version to 4.14.7587.7</span></span>
* <span data-ttu-id="71536-370">Lade till kommandona ”Stop-AzDataFactoryV2TriggerRun” och ”Invoke-AzDataFactoryV2TriggerRun”</span><span class="sxs-lookup"><span data-stu-id="71536-370">Added 'Stop-AzDataFactoryV2TriggerRun' and 'Invoke-AzDataFactoryV2TriggerRun' commands</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="71536-371">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="71536-371">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="71536-372">Kräv egenskapen Plats för att skapa ARM-objekt på högsta nivån.</span><span class="sxs-lookup"><span data-stu-id="71536-372">Require Location property for creating top level arm objects.</span></span>
        <span data-ttu-id="71536-373">\* Gjorde så att `ApplicationGroupType` krävs för `New-AzWvdApplicationGroup`.</span><span class="sxs-lookup"><span data-stu-id="71536-373">\* Made `ApplicationGroupType` required for `New-AzWvdApplicationGroup`.</span></span>
        <span data-ttu-id="71536-374">\* Gjorde så att `HostPoolArmPath` krävs för `New-AzWvdApplicationGroup`.</span><span class="sxs-lookup"><span data-stu-id="71536-374">\* Made `HostPoolArmPath` required for `New-AzWvdApplicationGroup`.</span></span>
        <span data-ttu-id="71536-375">\* `PreferredAppGroupType` har lagts till för `New-AzWvdHostPool`.</span><span class="sxs-lookup"><span data-stu-id="71536-375">\* Added `PreferredAppGroupType` for `New-AzWvdHostPool`.</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="71536-376">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="71536-376">Az.Functions</span></span>
* <span data-ttu-id="71536-377">[Icke-bakåtkompatibel ändring] Tog bort växelparametern ”IncludeSlot” från alla förutom en parameteruppsättning i ”Get-AzFunctionApp”.</span><span class="sxs-lookup"><span data-stu-id="71536-377">[Breaking Change] Removed 'IncludeSlot' switch parameter from all but one parameter set of 'Get-AzFunctionApp'.</span></span> <span data-ttu-id="71536-378">Cmdleten stöder nu hämtning av distributionsfack i resultaten när ”-IncludeSlot” anges.</span><span class="sxs-lookup"><span data-stu-id="71536-378">The cmdlet now supports retrieving deployment slots in the results when '-IncludeSlot' is specified.</span></span> 
* <span data-ttu-id="71536-379">Uppdaterade ”New-AzFunctionApp”:</span><span class="sxs-lookup"><span data-stu-id="71536-379">Updated 'New-AzFunctionApp':</span></span>
  - <span data-ttu-id="71536-380">Korrigerade ”-DisableApplicationInsights” så att inga Application Insights-projekt skapas när det här alternativet har angetts.</span><span class="sxs-lookup"><span data-stu-id="71536-380">Fixed -DisableApplicationInsights so that no application insights project is created when this option is specified.</span></span> <span data-ttu-id="71536-381">[#12728]</span><span class="sxs-lookup"><span data-stu-id="71536-381">[#12728]</span></span>
  - <span data-ttu-id="71536-382">[Icke-bakåtkompatibel ändring] Tog bort stöd för att skapa PowerShell 6.2-funktionsappar.</span><span class="sxs-lookup"><span data-stu-id="71536-382">[Breaking Change] Removed support to create PowerShell 6.2 function apps.</span></span>
  - <span data-ttu-id="71536-383">[Icke-bakåtkompatibel ändring] Ändrade körningsversionen som är standard i Functions version 3 i Windows för PowerShell-funktionsappar från 6.2 till 7.0 när parametern RuntimeVersion inte har angetts.</span><span class="sxs-lookup"><span data-stu-id="71536-383">[Breaking Change] Changed the default runtime version in Functions version 3 on Windows for PowerShell function apps from 6.2 to 7.0 when the RuntimeVersion parameter is not specified.</span></span>
  - <span data-ttu-id="71536-384">[Icke-bakåtkompatibel ändring] Ändrade körningsversionen som är standard i Functions version 3 i Windows och Linux för Node-funktionsappar från 10 till 12 när parametern RuntimeVersion inte har angetts.</span><span class="sxs-lookup"><span data-stu-id="71536-384">[Breaking Change] Changed the default runtime version in Functions version 3 on Windows and Linux for Node function apps from 10 to 12 when the RuntimeVersion parameter is not specified.</span></span>
  - <span data-ttu-id="71536-385">[Icke-bakåtkompatibel ändring] Ändrade körningsversionen som är standard i Functions version 3 i Linux för Python-funktionsappar från 3.7 till 3.8 när parametern RuntimeVersion inte har angetts.</span><span class="sxs-lookup"><span data-stu-id="71536-385">[Breaking Change] Changed the default runtime version in Functions version 3 on Linux for Python function apps from 3.7 to 3.8 when the RuntimeVersion parameter is not specified.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="71536-386">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="71536-386">Az.HDInsight</span></span>
 * <span data-ttu-id="71536-387">För cmdleten New-AzHDInsightCluster:</span><span class="sxs-lookup"><span data-stu-id="71536-387">For New-AzHDInsightCluster cmdlet:</span></span>
     - <span data-ttu-id="71536-388">Ersatte parametern ”DefaultStorageAccountName” med ”StorageAccountResourceId”</span><span class="sxs-lookup"><span data-stu-id="71536-388">Replaced parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
     - <span data-ttu-id="71536-389">Ersatte parametern ”DefaultStorageAccountKey” med ”StorageAccountKey”</span><span class="sxs-lookup"><span data-stu-id="71536-389">Replaced parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
     - <span data-ttu-id="71536-390">Ersatte parametern ”DefaultStorageAccountType” med ”StorageAccountType”</span><span class="sxs-lookup"><span data-stu-id="71536-390">Replaced parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
     - <span data-ttu-id="71536-391">Tog bort parametern ”PublicNetworkAccessType”</span><span class="sxs-lookup"><span data-stu-id="71536-391">Removed parameter 'PublicNetworkAccessType'</span></span>
     - <span data-ttu-id="71536-392">Ta bort parametern ”OutboundPublicNetworkAccessType”</span><span class="sxs-lookup"><span data-stu-id="71536-392">Removed parameter 'OutboundPublicNetworkAccessType'</span></span>
     - <span data-ttu-id="71536-393">Lade till nya parametrar: ”StorageFileSystem” och ”StorageAccountManagedIdentity” för att stödja ADLSGen2</span><span class="sxs-lookup"><span data-stu-id="71536-393">Added new parameters: 'StorageFileSystem' and 'StorageAccountManagedIdentity' to support ADLSGen2</span></span>
     - <span data-ttu-id="71536-394">Lade till den nya parametern ”EnableIDBroker” för att stödja ID-förmedlaren i HDInsight</span><span class="sxs-lookup"><span data-stu-id="71536-394">Added new parameter 'EnableIDBroker' to Support HDInsight ID Broker</span></span>
     - <span data-ttu-id="71536-395">Lade till nya parametrar: ”KafkaClientGroupId”, ”KafkaClientGroupName” och ”KafkaManagementNodeSize” för att stödja Kafka REST-proxy</span><span class="sxs-lookup"><span data-stu-id="71536-395">Added new parameters: 'KafkaClientGroupId', 'KafkaClientGroupName' and 'KafkaManagementNodeSize' to support Kafka Rest Proxy</span></span>
 * <span data-ttu-id="71536-396">För cmdleten New-AzHDInsightClusterConfig:</span><span class="sxs-lookup"><span data-stu-id="71536-396">For New-AzHDInsightClusterConfig cmdlet:</span></span>
     - <span data-ttu-id="71536-397">Ersatte parametern ”DefaultStorageAccountName” med ”StorageAccountResourceId”</span><span class="sxs-lookup"><span data-stu-id="71536-397">Replaced parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
     - <span data-ttu-id="71536-398">Ersatte parametern ”DefaultStorageAccountKey” med ”StorageAccountKey”</span><span class="sxs-lookup"><span data-stu-id="71536-398">Replaced parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
     - <span data-ttu-id="71536-399">Ersatte parametern ”DefaultStorageAccountType” med ”StorageAccountType”</span><span class="sxs-lookup"><span data-stu-id="71536-399">Replaced parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
     - <span data-ttu-id="71536-400">Tog bort parametern ”PublicNetworkAccessType”</span><span class="sxs-lookup"><span data-stu-id="71536-400">Removed parameter 'PublicNetworkAccessType'</span></span>
     - <span data-ttu-id="71536-401">Ta bort parametern ”OutboundPublicNetworkAccessType”</span><span class="sxs-lookup"><span data-stu-id="71536-401">Removed parameter 'OutboundPublicNetworkAccessType'</span></span>
* <span data-ttu-id="71536-402">För cmdleten Set-AzHDInsightDefaultStorage:</span><span class="sxs-lookup"><span data-stu-id="71536-402">For Set-AzHDInsightDefaultStorage cmdlet:</span></span>
    - <span data-ttu-id="71536-403">Ersatte parametern ”StorageAccountName” med ”StorageAccountResourceId”</span><span class="sxs-lookup"><span data-stu-id="71536-403">Replaced parameter 'StorageAccountName' with 'StorageAccountResourceId'</span></span>
* <span data-ttu-id="71536-404">För cmdleten Add-AzHDInsightSecurityProfile:</span><span class="sxs-lookup"><span data-stu-id="71536-404">For Add-AzHDInsightSecurityProfile cmdlet:</span></span>
    - <span data-ttu-id="71536-405">Ersatte parametern ”Domain” med ”DomainResourceId”</span><span class="sxs-lookup"><span data-stu-id="71536-405">Replaced parameter 'Domain' with 'DomainResourceId'</span></span>
    - <span data-ttu-id="71536-406">Tog bort det obligatoriska kravet för parametern ”OrganizationalUnitDN”</span><span class="sxs-lookup"><span data-stu-id="71536-406">Removed the mandatory requirement for parameter 'OrganizationalUnitDN'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="71536-407">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="71536-407">Az.KeyVault</span></span>
* <span data-ttu-id="71536-408">[Icke-bakåtkompatibel ändring] Parametrarna DisableSoftDelete i ”New-AzKeyVault” och EnableSoftDelete i ”Update-AzKeyVault” har gjorts inaktuella</span><span class="sxs-lookup"><span data-stu-id="71536-408">[Breaking Change] Deprecated parameter DisableSoftDelete in 'New-AzKeyVault' and EnableSoftDelete in 'Update-AzKeyVault'</span></span>
* <span data-ttu-id="71536-409">[Icke-bakåtkompatibel ändring] Tog bort attributet SecretValueText för att undvika att SecretValue visas direkt [#12266]</span><span class="sxs-lookup"><span data-stu-id="71536-409">[Breaking Change] Removed attribute SecretValueText to avoid displaying SecretValue directly [#12266]</span></span>
* <span data-ttu-id="71536-410">Stöd för ny resurstyp: hanterad HSM</span><span class="sxs-lookup"><span data-stu-id="71536-410">Supported new resource type: managed HSM</span></span>
    - <span data-ttu-id="71536-411">CRUD för hanterad HSM och cmdleter för att köra nycklar på hanterad HSM</span><span class="sxs-lookup"><span data-stu-id="71536-411">CRUD of managed HSM and cmdlets to operate keys on managed HSM</span></span>
    - <span data-ttu-id="71536-412">Fullständig HSM-säkerhetskopiering/återställning, skapande av AES-nyckel, säkerhetskopiering/återställning av domän, RBAC</span><span class="sxs-lookup"><span data-stu-id="71536-412">Full HSM backup/restore, AES key creation, security domain backup/restore, RBAC</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="71536-413">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="71536-413">Az.ManagedServices</span></span>
* <span data-ttu-id="71536-414">[Icke-bakåtkompatibel ändring] Uppdaterade namngivningskonventioner för parametrar och associerade exempel</span><span class="sxs-lookup"><span data-stu-id="71536-414">[Breaking Change] Updated parameters naming conventions and associated examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71536-415">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71536-415">Az.Network</span></span>
* <span data-ttu-id="71536-416">[Icke-bakåtkompatibel ändring] Tog bort parametern ”HostedSubnet” och lade till ”Subnet” i stället</span><span class="sxs-lookup"><span data-stu-id="71536-416">[Breaking Change] Removed parameter 'HostedSubnet' and added 'Subnet' instead</span></span>
* <span data-ttu-id="71536-417">Lade till nya cmdletar för peeringvägar för virtuella routrar</span><span class="sxs-lookup"><span data-stu-id="71536-417">Added new cmdlets for Virtual Router Peer Routes</span></span>
    - <span data-ttu-id="71536-418">”Get-AzVirtualRouterPeerLearnedRoute”</span><span class="sxs-lookup"><span data-stu-id="71536-418">'Get-AzVirtualRouterPeerLearnedRoute'</span></span>
    - <span data-ttu-id="71536-419">”Get-AzVirtualRouterPeerAdvertisedRoute”</span><span class="sxs-lookup"><span data-stu-id="71536-419">'Get-AzVirtualRouterPeerAdvertisedRoute'</span></span>
* <span data-ttu-id="71536-420">Cmdleten New-AzFirewall har uppdaterats:</span><span class="sxs-lookup"><span data-stu-id="71536-420">Updated New-AzFirewall cmdlet:</span></span>
    - <span data-ttu-id="71536-421">Lade till parametern ”-SkuTier”</span><span class="sxs-lookup"><span data-stu-id="71536-421">Added parameter '-SkuTier'</span></span>
    - <span data-ttu-id="71536-422">Lade till parametern ”-SkuName” och gjorde Sku till ett alias för den</span><span class="sxs-lookup"><span data-stu-id="71536-422">Added parameter '-SkuName' and made Sku as Alias for this</span></span>
    - <span data-ttu-id="71536-423">Tog bort parametern ”-Sku”</span><span class="sxs-lookup"><span data-stu-id="71536-423">Removed parameter '-Sku'</span></span>
* <span data-ttu-id="71536-424">[Icke-bakåtkompatibel ändring] Gjorde argumentet ”Connectionlink” obligatoriskt i ”Start-AzVpnConnectionPacketCapture” och ”Stop-AzVpnConnectionPacketCapture”</span><span class="sxs-lookup"><span data-stu-id="71536-424">[Breaking Change] Made 'Connectionlink' argument mandatory in 'Start-AzVpnConnectionPacketCapture' and 'Stop-AzVpnConnectionPacketCapture'</span></span>
* <span data-ttu-id="71536-425">[Icke-bakåtkompatibel ändring] Uppdaterade ”New-AzNetworkWatcherConnectionMonitorEndPointObject” för att ta bort parametern ”-Filter”</span><span class="sxs-lookup"><span data-stu-id="71536-425">[Breaking Change] Updated 'New-AzNetworkWatcherConnectionMonitorEndPointObject' to remove parameter '-Filter'</span></span>
* <span data-ttu-id="71536-426">[Icke-bakåtkompatibel ändring] Ersatte cmdleten ”New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject” med ”New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject”</span><span class="sxs-lookup"><span data-stu-id="71536-426">[Breaking Change] Replaced 'New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject' cmdlet with 'New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject'</span></span>
* <span data-ttu-id="71536-427">Uppdaterade cmdleten ”New-AzNetworkWatcherConnectionMonitorEndPointObject”:</span><span class="sxs-lookup"><span data-stu-id="71536-427">Updated 'New-AzNetworkWatcherConnectionMonitorEndPointObject' cmdlet:</span></span>
    - <span data-ttu-id="71536-428">Lade till parametern ”-Type”</span><span class="sxs-lookup"><span data-stu-id="71536-428">Added parameter '-Type'</span></span>
    - <span data-ttu-id="71536-429">Lade till parametern ”-CoverageLevel”</span><span class="sxs-lookup"><span data-stu-id="71536-429">Added parameter '-CoverageLevel'</span></span>
    - <span data-ttu-id="71536-430">Lade till parametern ”-Scope”</span><span class="sxs-lookup"><span data-stu-id="71536-430">Added parameter '-Scope'</span></span>
* <span data-ttu-id="71536-431">Uppdaterade cmdleten ”New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject” med den nya parametern ”-DestinationPortBehavior”</span><span class="sxs-lookup"><span data-stu-id="71536-431">Updated 'New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject' cmdlet with new parameter '-DestinationPortBehavior'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="71536-432">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="71536-432">Az.RecoveryServices</span></span>
* <span data-ttu-id="71536-433">Korrigerar återställning av arbetsbelastningar för behörigheter för deltagare.</span><span class="sxs-lookup"><span data-stu-id="71536-433">Fixing Workload Restore for contributor permissions.</span></span>
* <span data-ttu-id="71536-434">Lade till nya parameteruppsättningar och valideringar för cmdleten ”Restore-AzRecoveryServicesBackupItem”.</span><span class="sxs-lookup"><span data-stu-id="71536-434">Added new parameter sets and validations for Restore-AzRecoveryServicesBackupItem cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="71536-435">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71536-435">Az.Resources</span></span>
* <span data-ttu-id="71536-436">Korrigerade en bugg vid parsning</span><span class="sxs-lookup"><span data-stu-id="71536-436">Fixed parsing bug</span></span>
* <span data-ttu-id="71536-437">Uppdaterade What-If-cmdletar i ARM-mall för att ta bort förhandsgranskningsmeddelandet från resultaten</span><span class="sxs-lookup"><span data-stu-id="71536-437">Updated ARM template What-If cmdlets to remove preview message from results</span></span>
* <span data-ttu-id="71536-438">Korrigerade ett problem där cmdletar för mall-distribution kraschar om ”-WhatIf” har ställts in på ett högre omfång [#13038]</span><span class="sxs-lookup"><span data-stu-id="71536-438">Fixed an issue where template deployment cmdlets crash if '-WhatIf' is set at a higher scope [#13038]</span></span>
* <span data-ttu-id="71536-439">Korrigerade ett problem där cmdletar för malldistribution inte bevarar skiftläget för mallparametrar</span><span class="sxs-lookup"><span data-stu-id="71536-439">Fixed an issue where template deployment cmdlets does not preserve case for template parameters</span></span>
* <span data-ttu-id="71536-440">Lade till en standard-API-version som kan användas i cmdleten ”Export-AzResourceGroup”</span><span class="sxs-lookup"><span data-stu-id="71536-440">Added a default API version to be used in 'Export-AzResourceGroup' cmdlet</span></span>
* <span data-ttu-id="71536-441">Lade till cmdletar för mallspecifikationer (”Get-AzTemplateSpec”, ”Set-AzTemplateSpec”, ”New-AzTemplateSpec”, ”Remove-AzTemplateSpec”, ”Export-AzTemplateSpec”)</span><span class="sxs-lookup"><span data-stu-id="71536-441">Added cmdlets for Template Specs ('Get-AzTemplateSpec', 'Set-AzTemplateSpec', 'New-AzTemplateSpec', 'Remove-AzTemplateSpec', 'Export-AzTemplateSpec')</span></span>
* <span data-ttu-id="71536-442">Lade till stöd för att distribuera mallspecifikationer med befintliga cmdletar för distribution (via den nya parametern ”-TemplateSpecId”)</span><span class="sxs-lookup"><span data-stu-id="71536-442">Added support for deploying Template Specs using existing deployment cmdlets (via the new -TemplateSpecId parameter)</span></span> 
* <span data-ttu-id="71536-443">Uppdaterade ”Get-AzResourceGroupDeploymentOperation” för att använda SDK.</span><span class="sxs-lookup"><span data-stu-id="71536-443">Updated 'Get-AzResourceGroupDeploymentOperation' to use the SDK.</span></span>
* <span data-ttu-id="71536-444">Tog bort parametern ”ApiVersion” från cmdletarna ”\*-AzDeployment”.</span><span class="sxs-lookup"><span data-stu-id="71536-444">Removed '-ApiVersion' parameter from '\*-AzDeployment' cmdlets.</span></span>

#### <a name="azsql"></a><span data-ttu-id="71536-445">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71536-445">Az.Sql</span></span>
* <span data-ttu-id="71536-446">Korrigerade ett problem där New-AzSqlDatabaseExport misslyckas om networkIsolation inte har angetts [#13097]</span><span class="sxs-lookup"><span data-stu-id="71536-446">Fixed issue where New-AzSqlDatabaseExport fails if networkIsolation not specified [#13097]</span></span>
* <span data-ttu-id="71536-447">Korrigerade ett problem där New-AzSqlDatabaseExport och New-AzSqlDatabaseImport inte returnerade OperationStatusLink i resultatobjektet [#13097]</span><span class="sxs-lookup"><span data-stu-id="71536-447">Fixed issue where New-AzSqlDatabaseExport and New-AzSqlDatabaseImport were not returning OperationStatusLink in the result object [#13097]</span></span>
* <span data-ttu-id="71536-448">Uppdatera webbadresser för Azure-kopplade regioner i redundansvarningar för Backup Storage</span><span class="sxs-lookup"><span data-stu-id="71536-448">Update Azure Paired Regions URL in Backup Storage Redundancy Warnings</span></span> 

#### <a name="azstorage"></a><span data-ttu-id="71536-449">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="71536-449">Az.Storage</span></span>
* <span data-ttu-id="71536-450">Tog bort den föråldrade egenskapen RestorePolicy.LastEnabledTime</span><span class="sxs-lookup"><span data-stu-id="71536-450">Removed obsolete property RestorePolicy.LastEnabledTime</span></span>
    - <span data-ttu-id="71536-451">"Enable-AzStorageBlobRestorePolicy"</span><span class="sxs-lookup"><span data-stu-id="71536-451">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="71536-452">"Disable-AzStorageBlobRestorePolicy"</span><span class="sxs-lookup"><span data-stu-id="71536-452">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="71536-453">”Get-AzStorageBlobServiceProperty”</span><span class="sxs-lookup"><span data-stu-id="71536-453">'Get-AzStorageBlobServiceProperty'</span></span>
    - <span data-ttu-id="71536-454">”Update-AzStorageBlobServiceProperty”</span><span class="sxs-lookup"><span data-stu-id="71536-454">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="71536-455">Vill du ändra typen av DaysAfterModificationGreaterThan från int till int?</span><span class="sxs-lookup"><span data-stu-id="71536-455">Change Type of DaysAfterModificationGreaterThan from int to int?</span></span>
    - <span data-ttu-id="71536-456">"Set-AzStorageAccountManagementPolicy"</span><span class="sxs-lookup"><span data-stu-id="71536-456">'Set-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="71536-457">"Get-AzStorageAccountManagementPolicy"</span><span class="sxs-lookup"><span data-stu-id="71536-457">'Get-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="71536-458">"Add-AzStorageAccountManagementPolicyAction"</span><span class="sxs-lookup"><span data-stu-id="71536-458">'Add-AzStorageAccountManagementPolicyAction'</span></span>
    - <span data-ttu-id="71536-459">"New-AzStorageAccountManagementPolicyRule"</span><span class="sxs-lookup"><span data-stu-id="71536-459">'New-AzStorageAccountManagementPolicyRule'</span></span>
* <span data-ttu-id="71536-460">Stöd för skapa/uppdatera filresurs med åtkomstnivå</span><span class="sxs-lookup"><span data-stu-id="71536-460">Supported create/update file share with access tier</span></span>
    - <span data-ttu-id="71536-461">”New-AzRmStorageShare”</span><span class="sxs-lookup"><span data-stu-id="71536-461">'New-AzRmStorageShare'</span></span>
    - <span data-ttu-id="71536-462">”Update-AzRmStorageShare”</span><span class="sxs-lookup"><span data-stu-id="71536-462">'Update-AzRmStorageShare'</span></span>
* <span data-ttu-id="71536-463">Stöd för att konfigurera/uppdatera/ta bort ACL som stöds rekursivt på Datalake Gen2-objekt</span><span class="sxs-lookup"><span data-stu-id="71536-463">Supported set/update/remove Acl recursively on Datalake Gen2 item</span></span> 
    -  <span data-ttu-id="71536-464">”Set-AzDataLakeGen2AclRecursive”</span><span class="sxs-lookup"><span data-stu-id="71536-464">'Set-AzDataLakeGen2AclRecursive'</span></span> 
    -  <span data-ttu-id="71536-465">”Update-AzDataLakeGen2AclRecursive”</span><span class="sxs-lookup"><span data-stu-id="71536-465">'Update-AzDataLakeGen2AclRecursive'</span></span> 
    -  <span data-ttu-id="71536-466">”Remove-AzDataLakeGen2AclRecursive”</span><span class="sxs-lookup"><span data-stu-id="71536-466">'Remove-AzDataLakeGen2AclRecursive'</span></span>
* <span data-ttu-id="71536-467">Stöd för åtkomstprincip för containrar med de nya behörigheterna x, t</span><span class="sxs-lookup"><span data-stu-id="71536-467">Supported Container access policy with new permission x,t</span></span>
    -  <span data-ttu-id="71536-468">”New-AzStorageContainerStoredAccessPolicy”</span><span class="sxs-lookup"><span data-stu-id="71536-468">'New-AzStorageContainerStoredAccessPolicy'</span></span>
    -  <span data-ttu-id="71536-469">"Set-AzStorageContainerStoredAccessPolicy"</span><span class="sxs-lookup"><span data-stu-id="71536-469">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
* <span data-ttu-id="71536-470">Ändrade utdata från cmdleten hämta/ange åtkomstprincip för containrar genom att ändra behörighetstypen för den underordnade egenskapen från uppräkning till sträng</span><span class="sxs-lookup"><span data-stu-id="71536-470">Changed the output of get/set Container access policy cmdlet, by change the child property Permission type from enum to String</span></span>
    -  <span data-ttu-id="71536-471">"Get-AzStorageContainerStoredAccessPolicy"</span><span class="sxs-lookup"><span data-stu-id="71536-471">'Get-AzStorageContainerStoredAccessPolicy'</span></span>
    -  <span data-ttu-id="71536-472">"Set-AzStorageContainerStoredAccessPolicy"</span><span class="sxs-lookup"><span data-stu-id="71536-472">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
* <span data-ttu-id="71536-473">Korrigerade ett problem med exempelskript för att ange hanteringsprincip med JSON</span><span class="sxs-lookup"><span data-stu-id="71536-473">Fixed a sample script issue of set management policy with json</span></span>
    -  <span data-ttu-id="71536-474">"Set-AzStorageAccountManagementPolicy"</span><span class="sxs-lookup"><span data-stu-id="71536-474">'Set-AzStorageAccountManagementPolicy'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="71536-475">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="71536-475">Az.Websites</span></span>
* <span data-ttu-id="71536-476">Lade till stöd för Premium V3-prisnivån</span><span class="sxs-lookup"><span data-stu-id="71536-476">Added support for Premium V3 pricing tier</span></span>
* <span data-ttu-id="71536-477">Uppdaterade SDK för WebSites till 3.1.0</span><span class="sxs-lookup"><span data-stu-id="71536-477">Updated the WebSites SDK to 3.1.0</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="71536-478">Tack till våra community-deltagare</span><span class="sxs-lookup"><span data-stu-id="71536-478">Thanks to our community contributors</span></span>
* <span data-ttu-id="71536-479">@atul-ram, uppdatera Get-AzDelegation.md (#13176)</span><span class="sxs-lookup"><span data-stu-id="71536-479">@atul-ram, Update Get-AzDelegation.md (#13176)</span></span>
* <span data-ttu-id="71536-480">@dineshreddy007, hämta approller som har tilldelats korrekt om Stack HCI-registrering använder WAC-token.</span><span class="sxs-lookup"><span data-stu-id="71536-480">@dineshreddy007, Get the App Roles assigned correctly in case of Stack HCI registration using WAC token.</span></span> <span data-ttu-id="71536-481">(#13249)</span><span class="sxs-lookup"><span data-stu-id="71536-481">(#13249)</span></span>
* <span data-ttu-id="71536-482">@kongou-ae, uppdatera New-AzOffice365PolicyProperty.md (#13217)</span><span class="sxs-lookup"><span data-stu-id="71536-482">@kongou-ae, Update New-AzOffice365PolicyProperty.md (#13217)</span></span>
* <span data-ttu-id="71536-483">Lohith Chowdary Chilukuri (@Lochiluk), uppdatera Set-AzApplicationGateway.md (#13150)</span><span class="sxs-lookup"><span data-stu-id="71536-483">Lohith Chowdary Chilukuri (@Lochiluk), Update Set-AzApplicationGateway.md (#13150)</span></span>
* <span data-ttu-id="71536-484">Matthew Burleigh (@mburleigh)</span><span class="sxs-lookup"><span data-stu-id="71536-484">Matthew Burleigh (@mburleigh)</span></span>
  * <span data-ttu-id="71536-485">Lägg till länkar till de PowerShell-cmdletar som refereras i dokumentet (#13203)</span><span class="sxs-lookup"><span data-stu-id="71536-485">Add links to PowerShell cmdlets referenced in the document (#13203)</span></span>
  * <span data-ttu-id="71536-486">Lägg till länkar till de PowerShell-cmdletar som refereras i dokumentet (#13190)</span><span class="sxs-lookup"><span data-stu-id="71536-486">Add links to PowerShell cmdlets referenced in the document (#13190)</span></span>
  * <span data-ttu-id="71536-487">Lägg till länkar till de PowerShell-cmdletar som refereras i dokumentet (#13189)</span><span class="sxs-lookup"><span data-stu-id="71536-487">Add links to PowerShell cmdlets referenced in the document (#13189)</span></span>
  * <span data-ttu-id="71536-488">lägg till länkar till cmdletar som refereras (#13137)</span><span class="sxs-lookup"><span data-stu-id="71536-488">add links to referenced cmdlets (#13137)</span></span>
  * <span data-ttu-id="71536-489">Lägg till länkar till de PowerShell-cmdletar som refereras i dokumentet (#13204)</span><span class="sxs-lookup"><span data-stu-id="71536-489">Add links to PowerShell cmdlets referenced in the document (#13204)</span></span>
  * <span data-ttu-id="71536-490">Lägg till länkar till de PowerShell-cmdletar som refereras i dokumentet (#13205)</span><span class="sxs-lookup"><span data-stu-id="71536-490">Add links to PowerShell cmdlets referenced in the document (#13205)</span></span>

## <a name="480---october-2020"></a><span data-ttu-id="71536-491">4.8.0 – oktober 2020</span><span class="sxs-lookup"><span data-stu-id="71536-491">4.8.0 - October 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="71536-492">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="71536-492">Az.Accounts</span></span>
* <span data-ttu-id="71536-493">Åtgärdat DateTime-parsningsfel i vanliga bibliotek [#13045]</span><span class="sxs-lookup"><span data-stu-id="71536-493">Fixed DateTime parse issue in common libraries [#13045]</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="71536-494">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="71536-494">Az.CognitiveServices</span></span>
* <span data-ttu-id="71536-495">Cmdleten New-AzCognitiveServicesAccountApiProperty har lagts till.</span><span class="sxs-lookup"><span data-stu-id="71536-495">Added 'New-AzCognitiveServicesAccountApiProperty' cmdlet.</span></span>
* <span data-ttu-id="71536-496">Stöd för parametern ApiProperty för New-AzCognitiveServicesAccount och Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="71536-496">Supported 'ApiProperty' parameter for 'New-AzCognitiveServicesAccount' and 'Set-AzCognitiveServicesAccount'</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71536-497">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71536-497">Az.Compute</span></span>
* <span data-ttu-id="71536-498">Åtgärdat problem i Update-ASRRecoveryPlan genom att fylla i FailoverTypes</span><span class="sxs-lookup"><span data-stu-id="71536-498">Fixed issue in 'Update-ASRRecoveryPlan' by populating FailoverTypes</span></span>
* <span data-ttu-id="71536-499">De valfria parametrarna -Top och -OrderBy har lagts till i cmdleten Get-AzVmImage.</span><span class="sxs-lookup"><span data-stu-id="71536-499">Added the '-Top' and '-OrderBy' optional parameters to the 'Get-AzVmImage' cmdlet.</span></span> 

#### <a name="azdatabricks"></a><span data-ttu-id="71536-500">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="71536-500">Az.Databricks</span></span>
* <span data-ttu-id="71536-501">Allmän tillgänglighet för modulen Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="71536-501">General availability of 'Az.Databricks' module</span></span>
* <span data-ttu-id="71536-502">Stöd har lagts till för virtuell nätverkspeering</span><span class="sxs-lookup"><span data-stu-id="71536-502">Added support for virtual network peering</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="71536-503">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="71536-503">Az.DataFactory</span></span>
* <span data-ttu-id="71536-504">Skrivfel har åtgärdats i utdatameddelanden</span><span class="sxs-lookup"><span data-stu-id="71536-504">Fixed typo in output messages</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="71536-505">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="71536-505">Az.EventHub</span></span>
* <span data-ttu-id="71536-506">Den valfria switchparametern TrustedServiceAccessEnabled har lagts till i cmdleten Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="71536-506">Added optional switch parameter 'TrustedServiceAccessEnabled' to 'Set-AzEventHubNetworkRuleSet' cmdlet</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="71536-507">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="71536-507">Az.HDInsight</span></span>
* <span data-ttu-id="71536-508">Ett varningsmeddelande om att parametrarna PublicNetworkAccessType och OutboundPublicNetworkAccessType planeras att göras inaktuella har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-508">Added warning message for planning to deprecate the parameters 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType'</span></span>
* <span data-ttu-id="71536-509">Ett varningsmeddelande om att parametern DefaultStorageAccountName planeras att ersättas med StorageAccountResourceId har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-509">Added warning message for planning to replace the parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
* <span data-ttu-id="71536-510">Ett varningsmeddelande om att parametern DefaultStorageAccountKey planeras att ersättas med StorageAccountKey har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-510">Added warning message for planning to replace the parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
* <span data-ttu-id="71536-511">Ett varningsmeddelande om att parametern DefaultStorageAccountType planeras att ersättas med StorageAccountType har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-511">Added warning message for planning to replace the parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
* <span data-ttu-id="71536-512">Ett varningsmeddelande om att parametern DefaultStorageContainer planeras att ersättas med StorageContainer har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-512">Added warning message for planning to replace the parameter 'DefaultStorageContainer' with 'StorageContainer'</span></span>
* <span data-ttu-id="71536-513">Ett varningsmeddelande om att parametern DefaultStorageRootPath planeras att ersättas med StorageRootPath har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-513">Added warning message for planning to replace the parameter 'DefaultStorageRootPath' with 'StorageRootPath'</span></span>

#### <a name="aziothub"></a><span data-ttu-id="71536-514">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="71536-514">Az.IotHub</span></span>
* <span data-ttu-id="71536-515">SDK för enheter har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="71536-515">Updated devices sdk.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="71536-516">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="71536-516">Az.KeyVault</span></span>
* <span data-ttu-id="71536-517">Detaljerat datum för borttagning av egenskapen SecretValueText har tillhandahållits</span><span class="sxs-lookup"><span data-stu-id="71536-517">Provided the detailed date of removing property SecretValueText</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="71536-518">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="71536-518">Az.ManagedServices</span></span>
* <span data-ttu-id="71536-519">Varningar om icke-bakåtkompatibla ändringar för cmdletar för tilldelning och definition av hanterade tjänster har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="71536-519">Updated breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="71536-520">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="71536-520">Az.Monitor</span></span>
* <span data-ttu-id="71536-521">Felet som gjorde att ett varningsmeddelande inte kunde ignoreras har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="71536-521">Fixed the bug that warning message cannot be suppressed.</span></span> <span data-ttu-id="71536-522">[#12889]</span><span class="sxs-lookup"><span data-stu-id="71536-522">[#12889]</span></span>
* <span data-ttu-id="71536-523">Stöd för parametern SkipMetricValidation i aviseringsregelvillkor.</span><span class="sxs-lookup"><span data-stu-id="71536-523">Supported 'SkipMetricValidation' parameter in alert rule criteria.</span></span> <span data-ttu-id="71536-524">Tillåter att du skapar en aviseringsregel för ett anpassat mått som inte har genererats än, genom att göra så att måttverifieringen hoppas över.</span><span class="sxs-lookup"><span data-stu-id="71536-524">Allows creating an alert rule on a custom metric that isn't yet emitted, by causing the metric validation to be skipped.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71536-525">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71536-525">Az.Network</span></span>
* <span data-ttu-id="71536-526">Office365-princip har lagts till för VPNSite-resurs</span><span class="sxs-lookup"><span data-stu-id="71536-526">Added Office365 Policy to VPNSite Resource</span></span>
    - <span data-ttu-id="71536-527">New-AzO365PolicyProperty</span><span class="sxs-lookup"><span data-stu-id="71536-527">'New-AzO365PolicyProperty'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="71536-528">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="71536-528">Az.RecoveryServices</span></span>
* <span data-ttu-id="71536-529">Verifiering av containernamn har lagts till för arbetsbelastningssäkerhetskopior.</span><span class="sxs-lookup"><span data-stu-id="71536-529">Added container name validation for workload backup.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="71536-530">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="71536-530">Az.RedisCache</span></span>
* <span data-ttu-id="71536-531">En korrigering har gjorts så att cmdletarna New-AzRedisCache och Set-AzRedisCache inte misslyckas på grund av behörighetsproblem som rör registrering av Microsoft.Cache RP</span><span class="sxs-lookup"><span data-stu-id="71536-531">Made 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets not fail because of permission issue related to registering Microsoft.Cache RP</span></span>

#### <a name="azsql"></a><span data-ttu-id="71536-532">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71536-532">Az.Sql</span></span>
* <span data-ttu-id="71536-533">BackupStorageRedundancy har lagts till i:</span><span class="sxs-lookup"><span data-stu-id="71536-533">Added BackupStorageRedundancy to the following:</span></span> 
    - <span data-ttu-id="71536-534">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="71536-534">'Restore-AzureRmSqlDatabase'</span></span>
    - <span data-ttu-id="71536-535">New-AzSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="71536-535">'New-AzSqlDatabaseCopy'</span></span>
    - <span data-ttu-id="71536-536">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="71536-536">'New-AzSqlDatabaseSecondary'</span></span>
* <span data-ttu-id="71536-537">Skiftlägeskänslighet har tagits bort för parametern BackupStorageRedundancy för alla SQL DB-referenser</span><span class="sxs-lookup"><span data-stu-id="71536-537">Removed case sensitivity for BackupStorageRedundancy parameter for all SQL DB references</span></span> 
* <span data-ttu-id="71536-538">Namnen på BackupStorageRedundancy-varningsmeddelanden har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="71536-538">Updated BackupStorageRedundancy warning message names</span></span>

#### <a name="azstorage"></a><span data-ttu-id="71536-539">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="71536-539">Az.Storage</span></span>
* <span data-ttu-id="71536-540">Stöd för att aktivera/inaktivera/hämta egenskaper för mjuk borttagning av resurser för filtjänst för ett lagringskonto</span><span class="sxs-lookup"><span data-stu-id="71536-540">Supported enable/disable/get share soft delete properties on file Service of a Storage account</span></span>
    - <span data-ttu-id="71536-541">Update-AzStorageFileServiceProperty</span><span class="sxs-lookup"><span data-stu-id="71536-541">'Update-AzStorageFileServiceProperty'</span></span>
    - <span data-ttu-id="71536-542">Get-AzStorageFileServiceProperty</span><span class="sxs-lookup"><span data-stu-id="71536-542">'Get-AzStorageFileServiceProperty'</span></span>
* <span data-ttu-id="71536-543">Stöd för att visa filresurser inkluderar borttagna filresurser för ett lagringskonto och hämta förbrukning av enskild filresurs</span><span class="sxs-lookup"><span data-stu-id="71536-543">Supported list file shares include the deleted ones of a Storage account, and Get single file share usage</span></span>
    - <span data-ttu-id="71536-544">”Get-AzRmStorageShare”</span><span class="sxs-lookup"><span data-stu-id="71536-544">'Get-AzRmStorageShare'</span></span>
* <span data-ttu-id="71536-545">Stöd för återställning av en borttagen filresurs</span><span class="sxs-lookup"><span data-stu-id="71536-545">Supported restore a deleted file share</span></span>
    - <span data-ttu-id="71536-546">Restore-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="71536-546">'Restore-AzRmStorageShare'</span></span>
* <span data-ttu-id="71536-547">Cmdletarna för ändring av egenskaper för Blob Service har ändrats. De ursprungliga egenskaperna hämtas inte från servern utan anger bara de ändrade egenskaperna till servern.</span><span class="sxs-lookup"><span data-stu-id="71536-547">Changed the cmdlets for modify blob service properties, won't get the original properties from server, but only set the modified properties to server.</span></span>
    - <span data-ttu-id="71536-548">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="71536-548">'Enable-AzStorageBlobDeleteRetentionPolicy'</span></span>
    - <span data-ttu-id="71536-549">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="71536-549">'Disable-AzStorageBlobDeleteRetentionPolicy'</span></span>  
    - <span data-ttu-id="71536-550">"Enable-AzStorageBlobRestorePolicy"</span><span class="sxs-lookup"><span data-stu-id="71536-550">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="71536-551">"Disable-AzStorageBlobRestorePolicy"</span><span class="sxs-lookup"><span data-stu-id="71536-551">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="71536-552">”Update-AzStorageBlobServiceProperty”</span><span class="sxs-lookup"><span data-stu-id="71536-552">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="71536-553">Åtgärdat hjälpproblem för New-AzStorageAccount-parametern -Kind default value [#12189]</span><span class="sxs-lookup"><span data-stu-id="71536-553">Fixed help issue for New-AzStorageAccount parameter -Kind default value [#12189]</span></span>
* <span data-ttu-id="71536-554">Åtgärdat problem genom att lägga till exempel som visar hur ContentType anges på korrekt sätt i en blobuppladdning [#12989]</span><span class="sxs-lookup"><span data-stu-id="71536-554">Fixed issue by add example to show how to set correct ContentType in blob upload [#12989]</span></span>

## <a name="470---september-2020"></a><span data-ttu-id="71536-555">4.7.0 – September 2020</span><span class="sxs-lookup"><span data-stu-id="71536-555">4.7.0 - September 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="71536-556">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="71536-556">Az.Accounts</span></span>
* <span data-ttu-id="71536-557">Formaterat kommande meddelanden om icke-bakåtkompatibel ändring</span><span class="sxs-lookup"><span data-stu-id="71536-557">Formatted the upcoming breaking change messages</span></span>
* <span data-ttu-id="71536-558">Uppdaterat Azure.Core till 1.4.1</span><span class="sxs-lookup"><span data-stu-id="71536-558">Updated Azure.Core to 1.4.1</span></span>

#### <a name="azaks"></a><span data-ttu-id="71536-559">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="71536-559">Az.Aks</span></span>
* <span data-ttu-id="71536-560">Valideringslogiken för parametern "New-AzAksCluster", "Set-AzAksCluster" och "New-AzAksNodePool" har lagts till på klientsidan.</span><span class="sxs-lookup"><span data-stu-id="71536-560">Added client side parameter validation logic for 'New-AzAksCluster', 'Set-AzAksCluster' and 'New-AzAksNodePool'.</span></span> <span data-ttu-id="71536-561">[#12372]</span><span class="sxs-lookup"><span data-stu-id="71536-561">[#12372]</span></span>
* <span data-ttu-id="71536-562">Stöd har lagts till för tillägg i "New-AzAksCluster".</span><span class="sxs-lookup"><span data-stu-id="71536-562">Added support for add-ons in 'New-AzAksCluster'.</span></span> <span data-ttu-id="71536-563">[#11239]</span><span class="sxs-lookup"><span data-stu-id="71536-563">[#11239]</span></span>
* <span data-ttu-id="71536-564">Cmdlet:arna "Enable-AzAksAddOn" och "Disable-AzAksAddOn" har lagts till för tillägg.</span><span class="sxs-lookup"><span data-stu-id="71536-564">Added cmdlets 'Enable-AzAksAddOn' and 'Disable-AzAksAddOn' for add-ons.</span></span> <span data-ttu-id="71536-565">[#11239]</span><span class="sxs-lookup"><span data-stu-id="71536-565">[#11239]</span></span>
* <span data-ttu-id="71536-566">Parametern "GenerateSshKey" har lagts till för "New-AzAksCluster".</span><span class="sxs-lookup"><span data-stu-id="71536-566">Added parameter 'GenerateSshKey' for 'New-AzAksCluster'.</span></span> <span data-ttu-id="71536-567">[#12371]</span><span class="sxs-lookup"><span data-stu-id="71536-567">[#12371]</span></span>
* <span data-ttu-id="71536-568">API-versionen har uppdaterats till 2020-06-01.</span><span class="sxs-lookup"><span data-stu-id="71536-568">Updated api version to 2020-06-01.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="71536-569">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="71536-569">Az.CognitiveServices</span></span>
* <span data-ttu-id="71536-570">Visade ytterligare juridiska villkor för vissa API:er.</span><span class="sxs-lookup"><span data-stu-id="71536-570">Showed additional legal terms for certain APIs.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71536-571">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71536-571">Az.Compute</span></span>
* <span data-ttu-id="71536-572">Den valfria parametern "EncryptionType" har lagts till i "New-AzVmDiskEncryptionSetConfig"</span><span class="sxs-lookup"><span data-stu-id="71536-572">Added the '-EncryptionType' optional parameter to 'New-AzVmDiskEncryptionSetConfig'</span></span>
* <span data-ttu-id="71536-573">Nya cmdlet:ar för ny resurs typ: DiskAccess "Get-AzDiskAccess", "New-AzDiskAccess", "Get-AzDiskAccess"</span><span class="sxs-lookup"><span data-stu-id="71536-573">New cmdlets for new resource type: DiskAccess 'Get-AzDiskAccess', 'New-AzDiskAccess', 'Get-AzDiskAccess'</span></span>
* <span data-ttu-id="71536-574">De valfria parametrarna "-DiskAccessId" och "-NetworkAccessPolicy" har lagts till i "New-AzSnapshotConfig"</span><span class="sxs-lookup"><span data-stu-id="71536-574">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzSnapshotConfig'</span></span>
* <span data-ttu-id="71536-575">De valfria parametrarna "-DiskAccessId" och "-NetworkAccessPolicy" har lagts till i "New-AzDiskConfig"</span><span class="sxs-lookup"><span data-stu-id="71536-575">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzDiskConfig'</span></span>
* <span data-ttu-id="71536-576">PatchStatus-egenskapen har lagts till i VirtualMachine-instansvyn</span><span class="sxs-lookup"><span data-stu-id="71536-576">Added 'PatchStatus' property to VirtualMachine Instance View</span></span>
* <span data-ttu-id="71536-577">Egenskapen "VMHealth" har lagts till i den virtuella datorns instansvy, vilket är det returnerade objektet när "get-AzVm" anropas med "-Status"</span><span class="sxs-lookup"><span data-stu-id="71536-577">Added 'VMHealth' property to the virtual machine's instance view, which is the returned object when 'Get-AzVm' is invoked with '-Status'</span></span>
* <span data-ttu-id="71536-578">Fältet "AssignedHost" har lagts till i instansvyerna "Get-AzVM" och "Get-AzVmss".</span><span class="sxs-lookup"><span data-stu-id="71536-578">Added 'AssignedHost' field to 'Get-AzVM' and 'Get-AzVmss' instance views.</span></span> <span data-ttu-id="71536-579">I fältet visas resurs-ID för den virtuella datorinstansen</span><span class="sxs-lookup"><span data-stu-id="71536-579">The field shows the resource id of the virtual machine instance</span></span>
* <span data-ttu-id="71536-580">Den valfria parametern "-SupportAutomaticPlacement" har lagts till i "New-AzHostGroup"</span><span class="sxs-lookup"><span data-stu-id="71536-580">Added optional parameter '-SupportAutomaticPlacement' to 'New-AzHostGroup'</span></span> 
* <span data-ttu-id="71536-581">Parametern "-HostGroupId" har lagts till i "New-AzVm" och "New-AzVmss"</span><span class="sxs-lookup"><span data-stu-id="71536-581">Added the '-HostGroupId' parameter to 'New-AzVm' and 'New-AzVmss'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="71536-582">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="71536-582">Az.DataFactory</span></span>
* <span data-ttu-id="71536-583">ADF .Net SDK har uppdaterats till version 4.11.0</span><span class="sxs-lookup"><span data-stu-id="71536-583">Updated ADF .Net SDK version to 4.11.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="71536-584">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="71536-584">Az.EventHub</span></span>
* <span data-ttu-id="71536-585">Nya kluster-cmdlet:ar – "New-AzEventHubCluster", "Set-AzEventHubCluster", "Get-AzEventHubCluster", "Remove-AzEventHubCluster", "Get-AzEventHubClustersAvailableRegions" har lagts till.</span><span class="sxs-lookup"><span data-stu-id="71536-585">Added new Cluster cmdlets - 'New-AzEventHubCluster', 'Set-AzEventHubCluster', 'Get-AzEventHubCluster', 'Remove-AzEventHubCluster', 'Get-AzEventHubClustersAvailableRegions'.</span></span>
* <span data-ttu-id="71536-586">Åtgärdat för ärende #10722 : Korrigering för tilldelning av enbart lyssning till AuthorizationRule-rättigheter.</span><span class="sxs-lookup"><span data-stu-id="71536-586">Fixed for issue #10722 : Fix for assigning only 'Listen' to AuthorizationRule rights.</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="71536-587">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="71536-587">Az.Functions</span></span>
* <span data-ttu-id="71536-588">Möjligheten att skapa v2-funktioner i regioner som inte stöder det har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="71536-588">Removed the ability to create v2 Functions in regions that do not support it.</span></span>
* <span data-ttu-id="71536-589">Föråldrad PowerShell 6.2.</span><span class="sxs-lookup"><span data-stu-id="71536-589">Deprecated PowerShell 6.2.</span></span> <span data-ttu-id="71536-590">En varning har lagts till när en användare skapar en PowerShell 6.2-funktionsapp som uppmanar till att skapa en PowerShell 7.0-funktionsapp i stället.</span><span class="sxs-lookup"><span data-stu-id="71536-590">Added a warning for when a user creates a PowerShell 6.2 function app that advises them to create a PowerShell 7.0 function app instead.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="71536-591">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="71536-591">Az.HDInsight</span></span>
* <span data-ttu-id="71536-592">Stöd för att skapa kluster med automatisk skalningskonfiguration</span><span class="sxs-lookup"><span data-stu-id="71536-592">Supported creating cluster with Autoscale configuration</span></span>
    - <span data-ttu-id="71536-593">Lägg till den nya parametern "AutoscaleConfiguration" till cmdleten ”New-AzHDInsightCluster”</span><span class="sxs-lookup"><span data-stu-id="71536-593">Add new parameter 'AutoscaleConfiguration' to the cmdlet 'New-AzHDInsightCluster'</span></span>
* <span data-ttu-id="71536-594">Stöd för att använda automatisk skalningskonfiguration i kluster</span><span class="sxs-lookup"><span data-stu-id="71536-594">Supported operating cluster's Autoscale configuration</span></span>
    - <span data-ttu-id="71536-595">Lägg till ny cmdlet "Get-AzHDInsihgtClusterAutoscaleConfiguration"</span><span class="sxs-lookup"><span data-stu-id="71536-595">Add new cmdlet 'Get-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="71536-596">Lägg till ny cmdlet "New-AzHDInsihgtClusterAutoscaleConfiguration"</span><span class="sxs-lookup"><span data-stu-id="71536-596">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="71536-597">Lägg till ny cmdlet "Set-AzHDInsihgtClusterAutoscaleConfiguration"</span><span class="sxs-lookup"><span data-stu-id="71536-597">Add new cmdlet 'Set-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="71536-598">Lägg till ny cmdlet "Remove-AzHDInsihgtClusterAutoscaleConfiguration"</span><span class="sxs-lookup"><span data-stu-id="71536-598">Add new cmdlet 'Remove-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="71536-599">Lägg till ny cmdlet "New-AzHDInsihgtClusterAutoscaleScheduleCondition"</span><span class="sxs-lookup"><span data-stu-id="71536-599">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleScheduleCondition'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="71536-600">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="71536-600">Az.KeyVault</span></span>
* <span data-ttu-id="71536-601">Stöd har lagts till för RBAC-auktorisering [#10557]</span><span class="sxs-lookup"><span data-stu-id="71536-601">Added support for RBAC authorization [#10557]</span></span>
* <span data-ttu-id="71536-602">Förbättrad felhantering i "Set-AzKeyVaultAccessPolicy" [#4007]</span><span class="sxs-lookup"><span data-stu-id="71536-602">Enhanced error handling in 'Set-AzKeyVaultAccessPolicy' [#4007]</span></span>

#### <a name="azkusto"></a><span data-ttu-id="71536-603">Az.Kusto</span><span class="sxs-lookup"><span data-stu-id="71536-603">Az.Kusto</span></span>
* <span data-ttu-id="71536-604">Allmän tillgänglighet för "Az.Kusto"-modulen</span><span class="sxs-lookup"><span data-stu-id="71536-604">General availability of 'Az.Kusto' module</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71536-605">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71536-605">Az.Network</span></span>
* <span data-ttu-id="71536-606">[Viktig ändring] Uppdaterade nedanstående cmdlets för att justera resursens virtuella router och virtuella hubb</span><span class="sxs-lookup"><span data-stu-id="71536-606">[Breaking Change] Updated below cmdlets to align resource virtual router and virtual hub</span></span>
    - <span data-ttu-id="71536-607">"New-AzVirtualRouter":</span><span class="sxs-lookup"><span data-stu-id="71536-607">'New-AzVirtualRouter':</span></span> 
        - <span data-ttu-id="71536-608">Parametern-HostedSubnet har lagts till för att stödja underordnad resurs för IP-konfiguration</span><span class="sxs-lookup"><span data-stu-id="71536-608">Added -HostedSubnet parameter to support IP configuration child resource</span></span>
        - <span data-ttu-id="71536-609">-HostedGateway och -HostedGatewayId har tagits bort</span><span class="sxs-lookup"><span data-stu-id="71536-609">deleted -HostedGateway and -HostedGatewayId</span></span>
    - <span data-ttu-id="71536-610">'Get-AzVirtualRouter':</span><span class="sxs-lookup"><span data-stu-id="71536-610">'Get-AzVirtualRouter':</span></span>
        - <span data-ttu-id="71536-611">Parameteruppsättningen har lagts till på prenumerationsnivå</span><span class="sxs-lookup"><span data-stu-id="71536-611">Added subscription level parameter set</span></span>
    - <span data-ttu-id="71536-612">"Remove-AzVirtualRouter"</span><span class="sxs-lookup"><span data-stu-id="71536-612">'Remove-AzVirtualRouter'</span></span>
    - <span data-ttu-id="71536-613">"Add-AzVirtualRouterPeer"</span><span class="sxs-lookup"><span data-stu-id="71536-613">'Add-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="71536-614">"Get-AzVirtualRouterPeer"</span><span class="sxs-lookup"><span data-stu-id="71536-614">'Get-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="71536-615">"Remove-AzVirtualRouterPeer"</span><span class="sxs-lookup"><span data-stu-id="71536-615">'Remove-AzVirtualRouterPeer'</span></span>
* <span data-ttu-id="71536-616">Ny cmdlet har lagts till för Azure Express Route-port</span><span class="sxs-lookup"><span data-stu-id="71536-616">Added new cmdlet for Azure Express Route Port</span></span>
    - <span data-ttu-id="71536-617">"New-AzExpressRoutePortLOA"</span><span class="sxs-lookup"><span data-stu-id="71536-617">'New-AzExpressRoutePortLOA'</span></span>
* <span data-ttu-id="71536-618">Egenskapen RemoteBgpCommunities har lagts till i VirtualNetwork Peering-resursen</span><span class="sxs-lookup"><span data-stu-id="71536-618">Added RemoteBgpCommunities property to the VirtualNetwork Peering Resource</span></span>
* <span data-ttu-id="71536-619">Ändrade varningsmeddelandet för ”New-AzLoadBalancerFrontendIpConfig”, ”New-AzPublicIpAddress” och ”New-AzPublicIpPrefix”.</span><span class="sxs-lookup"><span data-stu-id="71536-619">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>
* <span data-ttu-id="71536-620">Lade till VpnGatewayIpConfigurations till "Get-AzVpnGateway"-utdata</span><span class="sxs-lookup"><span data-stu-id="71536-620">Added VpnGatewayIpConfigurations to 'Get-AzVpnGateway' output</span></span>
* <span data-ttu-id="71536-621">Åtgärdade bugg för "Set-AzApplicationGatewaySslCertificate" [#9488]</span><span class="sxs-lookup"><span data-stu-id="71536-621">Fixed bug for 'Set-AzApplicationGatewaySslCertificate' [#9488]</span></span>
* <span data-ttu-id="71536-622">Parametern "AllowActiveFTP" har lagts till i "AzureFirewall"</span><span class="sxs-lookup"><span data-stu-id="71536-622">Added 'AllowActiveFTP' parameter to 'AzureFirewall'</span></span>
* <span data-ttu-id="71536-623">Nedanstående kommandon för funktionen har uppdaterats: Aktivera konfiguration/borttagning för Internetsäkerhet på VirtualWan P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="71536-623">Updated below commands for feature: Enable internet security set/remove on VirtualWan P2SVpnGateway.</span></span>
- <span data-ttu-id="71536-624">"New-AzP2sVpnGateway" har uppdaterats": Den valfria växelparametern "EnableInternetSecurityFlag" har lagts till för kunder som anger värdet true för att aktivera Internetsäkerhet på P2SVpnGateway, som ska användas för plats-till-plats-klienter.</span><span class="sxs-lookup"><span data-stu-id="71536-624">Updated 'New-AzP2sVpnGateway': Added optional switch parameter 'EnableInternetSecurityFlag' for customers to set true to enable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
- <span data-ttu-id="71536-625">"Update-AzP2sVpnGateway" har uppdaterats: De valfria växelparametrarna "EnableInternetSecurityFlag" eller "DisableInternetSecurityFlag" har lagts till för kunder som anger värdet true/false för att aktivera/inaktivera Internetsäkerhet på P2SVpnGateway, som ska användas för plats-till-plats-klienter.</span><span class="sxs-lookup"><span data-stu-id="71536-625">Updated 'Update-AzP2sVpnGateway': Added optional switch parameters 'EnableInternetSecurityFlag' or 'DisableInternetSecurityFlag' for customers to set true/false to enable/disable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
* <span data-ttu-id="71536-626">Den nya cmdleten "Reset-AzP2sVpnGateway" har lagts till för att kunder ska kunna återställa/starta om sina VirtualWan-P2SVpnGateway för felsökning.</span><span class="sxs-lookup"><span data-stu-id="71536-626">Added new cmdlet 'Reset-AzP2sVpnGateway' for customers to reset/reboot their VirtualWan P2SVpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="71536-627">Den nya cmdleten "Reset-AzVpnGateway" har lagts till för att kunder ska kunna återställa/starta om VirtualWan VpnGateway för felsökning.</span><span class="sxs-lookup"><span data-stu-id="71536-627">Added new cmdlet 'Reset-AzVpnGateway' for customers to reset/reboot their VirtualWan VpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="71536-628">"Set-AzVirtualNetworkSubnetConfig" har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="71536-628">Updated 'Set-AzVirtualNetworkSubnetConfig'</span></span>
    - <span data-ttu-id="71536-629">Ange egenskaper för NSG och routningstabell för undernät till null om det anges explicit i parametrarna [#1548] [#9718]</span><span class="sxs-lookup"><span data-stu-id="71536-629">Set NSG and Route Table properties of subnet to null if explicitly set in parameters [#1548][#9718]</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="71536-630">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="71536-630">Az.RecoveryServices</span></span>
* <span data-ttu-id="71536-631">Åtgärdat borttagningstillståndet för säkerhetskopieringsobjekt.</span><span class="sxs-lookup"><span data-stu-id="71536-631">Fixed the Delete State for workload Backup Items.</span></span>

#### <a name="azresources"></a><span data-ttu-id="71536-632">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71536-632">Az.Resources</span></span>
* <span data-ttu-id="71536-633">Lagt till saknad kontroll för Set-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="71536-633">Added missing check for Set-AzRoleAssignment</span></span>
* <span data-ttu-id="71536-634">Attribut som medför icke-bakåtkompatibel ändring har lagts till i parametern "SubscriptionId" i "Get-AzResourceGroupDeploymentOperation"</span><span class="sxs-lookup"><span data-stu-id="71536-634">Added breaking change attribute to 'SubscriptionId' parameter of 'Get-AzResourceGroupDeploymentOperation'</span></span>
* <span data-ttu-id="71536-635">Uppdaterat What-If-cmdlets i ARM-mall så att resursändringar av typen 'Ignorera' visas sist</span><span class="sxs-lookup"><span data-stu-id="71536-635">Updated ARM template What-If cmdlets to show 'Ignore' resource changes last</span></span>
* <span data-ttu-id="71536-636">Åtgärdat serialiseringsproblem med säkra parametrar och matrisparametrar för distributionscmdlets [#12773]</span><span class="sxs-lookup"><span data-stu-id="71536-636">Fixed secure and array parameter serialization issues for deployment cmdlets [#12773]</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="71536-637">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="71536-637">Az.ServiceFabric</span></span>
* <span data-ttu-id="71536-638">Nya cmdletar har lagts till för hanterade kluster och nodtyper:</span><span class="sxs-lookup"><span data-stu-id="71536-638">Added new cmdlets for managed clusters and node types:</span></span>
    - <span data-ttu-id="71536-639">"New-AzServiceFabricManagedCluster"</span><span class="sxs-lookup"><span data-stu-id="71536-639">'New-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="71536-640">"Get-AzServiceFabricManagedCluster"</span><span class="sxs-lookup"><span data-stu-id="71536-640">'Get-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="71536-641">"Set-AzServiceFabricManagedCluster"</span><span class="sxs-lookup"><span data-stu-id="71536-641">'Set-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="71536-642">"Remove-AzServiceFabricManagedCluster"</span><span class="sxs-lookup"><span data-stu-id="71536-642">'Remove-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="71536-643">"Add-AzServiceFabricManagedClusterClientCertificate"</span><span class="sxs-lookup"><span data-stu-id="71536-643">'Add-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="71536-644">"Remove-AzServiceFabricManagedClusterClientCertificate"</span><span class="sxs-lookup"><span data-stu-id="71536-644">'Remove-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="71536-645">"New-AzServiceFabricManagedNodeType"</span><span class="sxs-lookup"><span data-stu-id="71536-645">'New-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="71536-646">"Get-AzServiceFabricManagedNodeType"</span><span class="sxs-lookup"><span data-stu-id="71536-646">'Get-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="71536-647">"Set-AzServiceFabricManagedNodeType"</span><span class="sxs-lookup"><span data-stu-id="71536-647">'Set-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="71536-648">"Remove-AzServiceFabricManagedNodeType"</span><span class="sxs-lookup"><span data-stu-id="71536-648">'Remove-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="71536-649">"Add-AzServiceFabricManagedNodeTypeVMExtension"</span><span class="sxs-lookup"><span data-stu-id="71536-649">'Add-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="71536-650">"Add-AzServiceFabricManagedNodeTypeVMSecret"</span><span class="sxs-lookup"><span data-stu-id="71536-650">'Add-AzServiceFabricManagedNodeTypeVMSecret'</span></span>
    - <span data-ttu-id="71536-651">"Remove-AzServiceFabricManagedNodeTypeVMExtension"</span><span class="sxs-lookup"><span data-stu-id="71536-651">'Remove-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="71536-652">"Restart-AzServiceFabricManagedNodeTyp"</span><span class="sxs-lookup"><span data-stu-id="71536-652">'Restart-AzServiceFabricManagedNodeTyp'</span></span>
* <span data-ttu-id="71536-653">Service Fabric SDK har uppgraderats till version 1.2.0 som använder Service Fabric-resursprovidern med API-version 2020-03-01 för aktuell modell och 2020-01-01-förhandsversion för hanterade kluster.</span><span class="sxs-lookup"><span data-stu-id="71536-653">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2020-03-01 for the current model and 2020-01-01-preview for managed clusters.</span></span>

#### <a name="azsql"></a><span data-ttu-id="71536-654">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71536-654">Az.Sql</span></span>
* <span data-ttu-id="71536-655">BackupStorageRedundancy har lagts till i "New-AzSqlInstance" och "Get-AzSqlInstance"</span><span class="sxs-lookup"><span data-stu-id="71536-655">Added BackupStorageRedundancy to 'New-AzSqlInstance' and 'Get-AzSqlInstance'</span></span>
* <span data-ttu-id="71536-656">Cmdlet:en "Get-AzSqlServerActiveDirectoryOnlyAuthentication" har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-656">Added cmdlet 'Get-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="71536-657">Cmdlet:en "Enable-AzSqlServerActiveDirectoryOnlyAuthentication" har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-657">Added cmdlet 'Enable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="71536-658">Force-parametern har lagts till i "New-AzSqlInstance"</span><span class="sxs-lookup"><span data-stu-id="71536-658">Added Force parameter to 'New-AzSqlInstance'</span></span>
* <span data-ttu-id="71536-659">Cmdlet:ar för logguppspelningstjänst för hanterade databaser har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-659">Added cmdlets for Managed Database Log Replay service</span></span>
    - <span data-ttu-id="71536-660">"Start-AzSqlInstanceDatabaseLogReplay"</span><span class="sxs-lookup"><span data-stu-id="71536-660">'Start-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="71536-661">"Get-AzSqlInstanceDatabaseLogReplay"</span><span class="sxs-lookup"><span data-stu-id="71536-661">'Get-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="71536-662">"Complete-AzSqlInstanceDatabaseLogReplay"</span><span class="sxs-lookup"><span data-stu-id="71536-662">'Complete-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="71536-663">"Stop-AzSqlInstanceDatabaseLogReplay"</span><span class="sxs-lookup"><span data-stu-id="71536-663">'Stop-AzSqlInstanceDatabaseLogReplay'</span></span>
* <span data-ttu-id="71536-664">Cmdlet:en "Get-AzSqlInstanceActiveDirectoryOnlyAuthentication" har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-664">Added cmdlet 'Get-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="71536-665">Cmdlet:en "Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication" har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-665">Added cmdlet 'Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="71536-666">Cmdlet:en "Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication" har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-666">Added cmdlet 'Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="71536-667">Cmdletarna "New-AzSqlDatabaseImport" och "New-AzSqlDatabaseExport" har uppdaterats för att stödja funktioner för nätverksisolering</span><span class="sxs-lookup"><span data-stu-id="71536-667">Updated cmdlets 'New-AzSqlDatabaseImport' and 'New-AzSqlDatabaseExport' to support network isolation functionality</span></span>
* <span data-ttu-id="71536-668">Cmdleten "New-AzSqlDatabaseImportExisting" har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-668">Added cmdlet 'New-AzSqlDatabaseImportExisting'</span></span>
* <span data-ttu-id="71536-669">Uppdaterade databas-cmdlet:ar som stöder typspecifikation av lagringsenhet för säkerhetskopiering</span><span class="sxs-lookup"><span data-stu-id="71536-669">Updated Databases cmdlets to support backup storage type specification</span></span>
* <span data-ttu-id="71536-670">Force-parametern har lagts till i "New-AzSqlDatabase"</span><span class="sxs-lookup"><span data-stu-id="71536-670">Added Force parameter to 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="71536-671">Varning för BackupStorageRedundancy-konfiguration har lagts till i utvalda regioner i "New-AzSqlDatabase"</span><span class="sxs-lookup"><span data-stu-id="71536-671">Added warning for BackupStorageRedundancy configuration in select regions in 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="71536-672">Uppdaterade ActiveDirectoryOnlyAuthentication-cmdletar för server och instans så att de innehåller ResourceId och InputObject</span><span class="sxs-lookup"><span data-stu-id="71536-672">Updated ActiveDirectoryOnlyAuthentication cmdlets for server and instance to include ResourceId and InputObject</span></span>

#### <a name="azstorage"></a><span data-ttu-id="71536-673">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="71536-673">Az.Storage</span></span>
* <span data-ttu-id="71536-674">Åtgärdade fel vid uppladdning av blob genom uppgradering till Microsoft.Azure.Storage.DataMovement 2.0.0 [#12220]</span><span class="sxs-lookup"><span data-stu-id="71536-674">Fixed upload blob fail by upgrade to Microsoft.Azure.Storage.DataMovement 2.0.0 [#12220]</span></span>
* <span data-ttu-id="71536-675">Stöd för återställning baserat på tidpunkt</span><span class="sxs-lookup"><span data-stu-id="71536-675">Supported Point In Time Restore</span></span>
    - <span data-ttu-id="71536-676">"Enable-AzStorageBlobRestorePolicy"</span><span class="sxs-lookup"><span data-stu-id="71536-676">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="71536-677">"Disable-AzStorageBlobRestorePolicy"</span><span class="sxs-lookup"><span data-stu-id="71536-677">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="71536-678">"New-AzStorageBlobRangeToRestore"</span><span class="sxs-lookup"><span data-stu-id="71536-678">'New-AzStorageBlobRangeToRestore'</span></span>
    - <span data-ttu-id="71536-679">"Restore-AzStorageBlobRange"</span><span class="sxs-lookup"><span data-stu-id="71536-679">'Restore-AzStorageBlobRange'</span></span>
* <span data-ttu-id="71536-680">Stöd för att hämta status för blobåterställning genom att köra get-AzureRMStorageAccount med parametern -IncludeBlobRestoreStatus</span><span class="sxs-lookup"><span data-stu-id="71536-680">Supported get blob restore status of Storage account by run get-AzureRMStorageAccount with parameter -IncludeBlobRestoreStatus</span></span> 
    - <span data-ttu-id="71536-681">"Get-AzureRMStorageAccount"</span><span class="sxs-lookup"><span data-stu-id="71536-681">'Get-AzureRMStorageAccount'</span></span>
* <span data-ttu-id="71536-682">Meddelande om icke-bakåtkompatibel ändring för kommande ändring av cmdlet-utdata har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-682">Added breaking change warning message for upcoming cmdlet output change</span></span>
    - <span data-ttu-id="71536-683">"Get-AzStorageContainerStoredAccessPolicy"</span><span class="sxs-lookup"><span data-stu-id="71536-683">'Get-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="71536-684">"Set-AzStorageContainerStoredAccessPolicy"</span><span class="sxs-lookup"><span data-stu-id="71536-684">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="71536-685">"Set-AzStorageAccountManagementPolicy"</span><span class="sxs-lookup"><span data-stu-id="71536-685">'Set-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="71536-686">"Get-AzStorageAccountManagementPolicy"</span><span class="sxs-lookup"><span data-stu-id="71536-686">'Get-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="71536-687">"Add-AzStorageAccountManagementPolicyAction"</span><span class="sxs-lookup"><span data-stu-id="71536-687">'Add-AzStorageAccountManagementPolicyAction'</span></span>
    - <span data-ttu-id="71536-688">"New-AzStorageAccountManagementPolicyRule"</span><span class="sxs-lookup"><span data-stu-id="71536-688">'New-AzStorageAccountManagementPolicyRule'</span></span>
* <span data-ttu-id="71536-689">Uppgraderade Microsoft.Azure.Cosmos.Table SDK till 1.0.8</span><span class="sxs-lookup"><span data-stu-id="71536-689">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.8</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="71536-690">Tack till våra community-deltagare</span><span class="sxs-lookup"><span data-stu-id="71536-690">Thanks to our community contributors</span></span>
* <span data-ttu-id="71536-691">Thomas Van Laere (@ThomVanL), Lägg till Dockerfile-alpine-3.10 (#12911)</span><span class="sxs-lookup"><span data-stu-id="71536-691">Thomas Van Laere (@ThomVanL), Add Dockerfile-alpine-3.10 (#12911)</span></span> 
* <span data-ttu-id="71536-692">Lohith Chowdary Chilukuri (@Lochiluk), Uppdatering av Remove-AzNetworkInterfaceIpConfig.md (#12807)</span><span class="sxs-lookup"><span data-stu-id="71536-692">Lohith Chowdary Chilukuri (@Lochiluk), Update Remove-AzNetworkInterfaceIpConfig.md (#12807)</span></span> 
* <span data-ttu-id="71536-693">Roberth Strand (@roberthstrand), Get-AzResourceGroup – Nytt exempel och rensning (#12828)</span><span class="sxs-lookup"><span data-stu-id="71536-693">Roberth Strand (@roberthstrand), Get-AzResourceGroup - New example, and cleanup (#12828)</span></span> 
* <span data-ttu-id="71536-694">Ravi Mishra (@inmishrar), uppdatering av Azure Web App-körningsstack till DOTNETCORE (#12833)</span><span class="sxs-lookup"><span data-stu-id="71536-694">Ravi Mishra (@inmishrar), update Azure Web App runtime stack to DOTNETCORE (#12833)</span></span> 
* <span data-ttu-id="71536-695">@jack-education, uppdaterat set-AzVirtualNetworkSubnetConfig för att tillåta att NSG och routningstabell tas bort från undernät (#12351)</span><span class="sxs-lookup"><span data-stu-id="71536-695">@jack-education, Updated Set-AzVirtualNetworkSubnetConfig to allow NSG and Route Table to be removed from subnet (#12351)</span></span> 
* <span data-ttu-id="71536-696">@hagop-globanet, uppdatering av Add-AzApplicationGatewayCustomError.md (#12784)</span><span class="sxs-lookup"><span data-stu-id="71536-696">@hagop-globanet, Update Add-AzApplicationGatewayCustomError.md (#12784)</span></span> 
* <span data-ttu-id="71536-697">Joshua Van Daalen (@greenSacrifice)</span><span class="sxs-lookup"><span data-stu-id="71536-697">Joshua Van Daalen (@greenSacrifice)</span></span>
  * <span data-ttu-id="71536-698">Uppdatering av stavning av egenskaper till egenskaper (#12821)</span><span class="sxs-lookup"><span data-stu-id="71536-698">Update spelling of Property to Property (#12821)</span></span> 
  * <span data-ttu-id="71536-699">Uppdatering av New-AzResourceLock.md-exempel (#12806)</span><span class="sxs-lookup"><span data-stu-id="71536-699">Update New-AzResourceLock.md examples (#12806)</span></span>
* <span data-ttu-id="71536-700">Eragon Riddle (@eragonriddle), korrigerat fältnamn för parameter i exemplet (#12825)</span><span class="sxs-lookup"><span data-stu-id="71536-700">Eragon Riddle (@eragonriddle), Corrected parameter field name in the example (#12825)</span></span> 
* <span data-ttu-id="71536-701">@rossifumax, åtgärdat skrivfel i New-AzConfigurationAssignment.md (#12701)</span><span class="sxs-lookup"><span data-stu-id="71536-701">@rossifumax, Fix typo in New-AzConfigurationAssignment.md (#12701)</span></span>

## <a name="461---august-2020"></a><span data-ttu-id="71536-702">4.6.1 – augusti 2020</span><span class="sxs-lookup"><span data-stu-id="71536-702">4.6.1 - August 2020</span></span>
#### <a name="azcompute"></a><span data-ttu-id="71536-703">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71536-703">Az.Compute</span></span>
* <span data-ttu-id="71536-704">Korrigerade EncryptionAtHost-parametern i New-AzVm för att ta bort standardvärdet FALSE [#12776]</span><span class="sxs-lookup"><span data-stu-id="71536-704">Patched '-EncryptionAtHost' parameter in 'New-AzVm' to remove default value of false [#12776]</span></span>

## <a name="460---august-2020"></a><span data-ttu-id="71536-705">4.6.0 – augusti 2020</span><span class="sxs-lookup"><span data-stu-id="71536-705">4.6.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="71536-706">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="71536-706">Az.Accounts</span></span>
* <span data-ttu-id="71536-707">Alla offentliga molnmiljöer läses in när slutpunktsidentifieringen inte returnerar AzureCloud (standard) eller andra offentliga miljöer [#12633]</span><span class="sxs-lookup"><span data-stu-id="71536-707">Loaded all public cloud environments when discovery endpoint doesn't return default AzureCloud or other public environments [#12633]</span></span>
* <span data-ttu-id="71536-708">SubscriptionPolicies har exponerats i Get-AzSubscription [#12551]</span><span class="sxs-lookup"><span data-stu-id="71536-708">Exposed SubscriptionPolicies in 'Get-AzSubscription' [#12551]</span></span>

#### <a name="azautomation"></a><span data-ttu-id="71536-709">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="71536-709">Az.Automation</span></span>
* <span data-ttu-id="71536-710">Parametern -RunOn har lagts till i Set-AzAutomationWebhook för att ange en Hybrid Worker-grupp</span><span class="sxs-lookup"><span data-stu-id="71536-710">Added '-RunOn' parameters to 'Set-AzAutomationWebhook' to specify a Hybrid Worker Group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71536-711">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71536-711">Az.Compute</span></span>
* <span data-ttu-id="71536-712">Parametern -EncryptionAtHost har lagts till i New-AzVm, New-AzVmss, New-AzVMConfig, New-AzVmssConfig, Update-AzVM och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="71536-712">Added '-EncryptionAtHost' parameter to 'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM', and 'Update-AzVmss'</span></span>
* <span data-ttu-id="71536-713">SecurityProfile har lagts till i Get-AzVM och Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="71536-713">Added 'SecurityProfile' to 'Get-AzVM' and 'Get-AzVmss' return object</span></span>
* <span data-ttu-id="71536-714">Växeln -InstanceView har lagts till som valfri parameter i Get-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="71536-714">Added '-InstanceView' switch as optional parameter to 'Get-AzHostGroup'</span></span>
* <span data-ttu-id="71536-715">En ny cmdlet, Invoke-AzVmPatchAssessment, har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-715">Added new cmdlet 'Invoke-AzVmPatchAssessment'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="71536-716">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="71536-716">Az.DataFactory</span></span>
* <span data-ttu-id="71536-717">Saknade egenskaper har lagts till i klassen PSPipelineRun.</span><span class="sxs-lookup"><span data-stu-id="71536-717">Added missing properties to PSPipelineRun class.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="71536-718">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="71536-718">Az.HDInsight</span></span>
* <span data-ttu-id="71536-719">Stöd för att skapa kluster med funktionen för kryptering under överföring.</span><span class="sxs-lookup"><span data-stu-id="71536-719">Supported creating cluster with encryption at host feature.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="71536-720">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="71536-720">Az.KeyVault</span></span>
* <span data-ttu-id="71536-721">Varningsmeddelanden har lagts till för planering att inaktivera mjuk borttagning</span><span class="sxs-lookup"><span data-stu-id="71536-721">Added warning messages for planning to disable soft delete</span></span>
* <span data-ttu-id="71536-722">Varningsmeddelanden har lagts till för planering att ta bort attributet SecretValueText</span><span class="sxs-lookup"><span data-stu-id="71536-722">Added warning messages for planning to remove attribute SecretValueText</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="71536-723">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="71536-723">Az.Maintenance</span></span>
* <span data-ttu-id="71536-724">Valfria schemarelaterade fält har lagts till i New-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="71536-724">Added optional schedule related fields to 'New-AzMaintenanceConfiguration'</span></span>
* <span data-ttu-id="71536-725">En ny cmdlet har lagts till för Get-AzMaintenancePublicConfiguration</span><span class="sxs-lookup"><span data-stu-id="71536-725">Added new cmdlet for 'Get-AzMaintenancePublicConfiguration'</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="71536-726">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="71536-726">Az.ManagedServices</span></span>
* <span data-ttu-id="71536-727">Varningar har lagts till om icke-bakåtkompatibla ändringar för cmdletar för tilldelning och definition av hanterade tjänster</span><span class="sxs-lookup"><span data-stu-id="71536-727">Added breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="71536-728">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="71536-728">Az.Monitor</span></span>
* <span data-ttu-id="71536-729">Utökade parametern som angetts i Set-AzDiagnosticSetting för separering av aktivering av loggar och mått [#12482]</span><span class="sxs-lookup"><span data-stu-id="71536-729">Extended the parameter set in 'Set-AzDiagnosticSetting' for separation of Logs and Metrics enablement [#12482]</span></span>
* <span data-ttu-id="71536-730">Åtgärdat fel för Add-AzMetricAlertRuleV2 vid hämtning av måttavisering från pipelinen</span><span class="sxs-lookup"><span data-stu-id="71536-730">Fixed bug for 'Add-AzMetricAlertRuleV2' when getting metric alert from pipeline</span></span>

#### <a name="azresources"></a><span data-ttu-id="71536-731">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71536-731">Az.Resources</span></span>
* <span data-ttu-id="71536-732">Get-AzPolicyAlias-svaret har uppdaterats för att ta med information som anger om aliaset kan ändras eller inte av Azure Policy.</span><span class="sxs-lookup"><span data-stu-id="71536-732">Updated 'Get-AzPolicyAlias' response to include information indicating whether the alias is modifiable by Azure Policy.</span></span>
* <span data-ttu-id="71536-733">Skapade en ny cmdlet, set-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="71536-733">Created new cmdlet 'Set-AzRoleAssignment'</span></span>
* <span data-ttu-id="71536-734">Get-AzDeploymentManagementGroupWhatIfResult har lagts till för att hämta What-If-resultat för ARM-mall i hanteringsgruppsomfånget</span><span class="sxs-lookup"><span data-stu-id="71536-734">Added 'Get-AzDeploymentManagementGroupWhatIfResult' for getting ARM template What-If results at management Group scope</span></span>
* <span data-ttu-id="71536-735">En ny cmdlet, Get-AzTenantWhatIfResult, har lagts till för att hämta What-If-resultat för ARM-mall i klientorganisationsomfånget</span><span class="sxs-lookup"><span data-stu-id="71536-735">Added 'Get-AzTenantWhatIfResult' new cmdlet for getting ARM template What-If results at tenant scope</span></span>
* <span data-ttu-id="71536-736">-WhatIf och -Confirm har åsidosatts för New-AzManagementGroupDeployment och New-AzTenantDeployment för att använda What-If-resultat för ARM-mall</span><span class="sxs-lookup"><span data-stu-id="71536-736">Overrode '-WhatIf' and '-Confirm' for 'New-AzManagementGroupDeployment' and 'New-AzTenantDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="71536-737">Beteenden har åtgärdats för -WhatIf och -Confirm för nya cmdletar för distribution så att de stämmer överens med False och</span><span class="sxs-lookup"><span data-stu-id="71536-737">Fixed the behaviors of '-WhatIf' and '-Confirm' for new deployment cmdlets so they comply with False and</span></span> 
* <span data-ttu-id="71536-738">Serialiseringsfel har åtgärdats för -TemplateObject och TemplateParameterObject [#1528] [#6292]</span><span class="sxs-lookup"><span data-stu-id="71536-738">Fixed serialization error for '-TemplateObject' and 'TemplateParameterObject' [#1528] [#6292]</span></span>
* <span data-ttu-id="71536-739">Attribut som medför icke-bakåtkompatibel ändring har lagts till i Get-AzResourceGroupDeploymentOperation för den kommande ändringen av utdatatyp</span><span class="sxs-lookup"><span data-stu-id="71536-739">Added breaking change attribute to 'Get-AzResourceGroupDeploymentOperation' for the upcoming output type change</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="71536-740">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="71536-740">Az.SignalR</span></span>
* <span data-ttu-id="71536-741">Fel i hjälpfilerna Restart-AzSignalR och Update-AzSignalR har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="71536-741">Fixed 'Restart-AzSignalR' and 'Update-AzSignalR' help files errors</span></span>
* <span data-ttu-id="71536-742">Cmdletarna Update-AzSignalRNetworkAcl och Set-AzSignalRUpstream har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-742">Added cmdlets 'Update-AzSignalRNetworkAcl', 'Set-AzSignalRUpstream'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="71536-743">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="71536-743">Az.Storage</span></span>
* <span data-ttu-id="71536-744">Stöd för blobfrågeacceleration</span><span class="sxs-lookup"><span data-stu-id="71536-744">Supported blob query acceleration</span></span>
    -  <span data-ttu-id="71536-745">Get-AzStorageBlobQueryResult</span><span class="sxs-lookup"><span data-stu-id="71536-745">'Get-AzStorageBlobQueryResult'</span></span>
    -  <span data-ttu-id="71536-746">New-AzStorageBlobQueryConfig</span><span class="sxs-lookup"><span data-stu-id="71536-746">'New-AzStorageBlobQueryConfig'</span></span>
* <span data-ttu-id="71536-747">Hjälpfil har lagts till, ytterligare beskrivning har lagts till och stavfel har korrigerats</span><span class="sxs-lookup"><span data-stu-id="71536-747">Updated help file, added more description, and fixed typo</span></span>
    -  <span data-ttu-id="71536-748">”Start-AzStorageBlobCopy”</span><span class="sxs-lookup"><span data-stu-id="71536-748">'Start-AzStorageBlobCopy'</span></span>
    -  <span data-ttu-id="71536-749">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="71536-749">'Get-AzDataLakeGen2Item'</span></span>
* <span data-ttu-id="71536-750">Problem med att ladda ned blob när relaterad underordnad katalog saknas har åtgärdats [#12592]</span><span class="sxs-lookup"><span data-stu-id="71536-750">Fixed download blob fail when related sub directory not exist [#12592]</span></span>
    -  <span data-ttu-id="71536-751">”Get-AzStorageBlobContent”</span><span class="sxs-lookup"><span data-stu-id="71536-751">'Get-AzStorageBlobContent'</span></span>
* <span data-ttu-id="71536-752">Replikeringsprincip för att ange, hämta, ta bort objekt på Storage-konton stöds</span><span class="sxs-lookup"><span data-stu-id="71536-752">Supported Set/Get/Remove Object Replication Policy on Storage accounts</span></span>
    - <span data-ttu-id="71536-753">New-AzStorageObjectReplicationPolicyRule</span><span class="sxs-lookup"><span data-stu-id="71536-753">'New-AzStorageObjectReplicationPolicyRule'</span></span>
    - <span data-ttu-id="71536-754">Set-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="71536-754">'Set-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="71536-755">Get-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="71536-755">'Get-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="71536-756">Remove-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="71536-756">'Remove-AzStorageObjectReplicationPolicy'</span></span>
* <span data-ttu-id="71536-757">Stöd har lagts till för att aktivera/inaktivera ChangeFeed i Blob Service för ett Storage-konto</span><span class="sxs-lookup"><span data-stu-id="71536-757">Supported enable/disable ChangeFeed on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="71536-758">”Update-AzStorageBlobServiceProperty”</span><span class="sxs-lookup"><span data-stu-id="71536-758">'Update-AzStorageBlobServiceProperty'</span></span>

## <a name="450---august-2020"></a><span data-ttu-id="71536-759">4.5.0 – augusti 2020</span><span class="sxs-lookup"><span data-stu-id="71536-759">4.5.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="71536-760">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="71536-760">Az.Accounts</span></span>
* <span data-ttu-id="71536-761">Uppdaterade ”Connect-AzAccount” så att det accepterar parametern ”MaxContextPopulation” [#9865]</span><span class="sxs-lookup"><span data-stu-id="71536-761">Updated 'Connect-AzAccount' to accept parameter 'MaxContextPopulation' [#9865]</span></span>
* <span data-ttu-id="71536-762">Uppdaterade SubscriptionClient-versionen till 2019-06-01 och visa klientdomäner [#9838]</span><span class="sxs-lookup"><span data-stu-id="71536-762">Updated SubscriptionClient version to 2019-06-01 and display tenant domains [#9838]</span></span>
* <span data-ttu-id="71536-763">Information om hemklientorganisation och managedBy-klientorganisation som stöds för prenumerationen</span><span class="sxs-lookup"><span data-stu-id="71536-763">Supported home tenant and managedBy tenant information of subscription</span></span>
* <span data-ttu-id="71536-764">Korrigerade modulnamn, versionsinformation i telemetridata</span><span class="sxs-lookup"><span data-stu-id="71536-764">Corrected module name, version info in telemetry data</span></span>
* <span data-ttu-id="71536-765">Justerade SqlDatabaseDnsSuffix och ServiceManagementUrl om miljöns slutpunkt för metadata returnerar ett inkompatibelt värde</span><span class="sxs-lookup"><span data-stu-id="71536-765">Adjusted SqlDatabaseDnsSuffix and ServiceManagementUrl if environment metadata endpoint returns incompatible value</span></span>

#### <a name="azaks"></a><span data-ttu-id="71536-766">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="71536-766">Az.Aks</span></span>
* <span data-ttu-id="71536-767">Tog bort ”ClientIdAndSecret” för ”ServicePrincipalIdAndSecret” och ställde in ”ClientIdAndSecret” som ett alias [#12381].</span><span class="sxs-lookup"><span data-stu-id="71536-767">Removed 'ClientIdAndSecret' to 'ServicePrincipalIdAndSecret' and set 'ClientIdAndSecret' as an alias [#12381].</span></span>
* <span data-ttu-id="71536-768">Tog bort ”Get-AzAks”/”New-AzAks”/”Remove-AzAks”/”Set-AzAks” för ”Get-AzAksCluster”/”New-AzAksCluster”/”Remove-AzAksCluster”/”Set-AzAksCluster” och ställde in de ursprungliga som alias [#12373].</span><span class="sxs-lookup"><span data-stu-id="71536-768">Removed 'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' to 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' and set the original ones as alias [#12373].</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="71536-769">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="71536-769">Az.ApiManagement</span></span>
* <span data-ttu-id="71536-770">Lade till ny cmdlet: ”Add-AzApiManagementApiToGateway”.</span><span class="sxs-lookup"><span data-stu-id="71536-770">Added new 'Add-AzApiManagementApiToGateway' cmdlet.</span></span>
* <span data-ttu-id="71536-771">Lade till ny cmdlet: ”Get-AzApiManagementGateway”.</span><span class="sxs-lookup"><span data-stu-id="71536-771">Added new 'Get-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="71536-772">Lade till ny cmdlet: ”Get-AzApiManagementGatewayHostnameConfiguration”.</span><span class="sxs-lookup"><span data-stu-id="71536-772">Added new 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="71536-773">Lade till ny cmdlet: ”Get-AzApiManagementGatewayKey”.</span><span class="sxs-lookup"><span data-stu-id="71536-773">Added new 'Get-AzApiManagementGatewayKey' cmdlet.</span></span>
* <span data-ttu-id="71536-774">Lade till ny cmdlet: ”New-AzApiManagementGateway”.</span><span class="sxs-lookup"><span data-stu-id="71536-774">Added new 'New-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="71536-775">Lade till ny cmdlet: ”New-AzApiManagementGatewayHostnameConfiguration”.</span><span class="sxs-lookup"><span data-stu-id="71536-775">Added new 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="71536-776">Lade till ny cmdlet: ”New-AzApiManagementResourceLocationObject”.</span><span class="sxs-lookup"><span data-stu-id="71536-776">Added new 'New-AzApiManagementResourceLocationObject' cmdlet.</span></span>
* <span data-ttu-id="71536-777">Lade till ny cmdlet: ”Remove-AzApiManagementApiFromGateway”.</span><span class="sxs-lookup"><span data-stu-id="71536-777">Added new 'Remove-AzApiManagementApiFromGateway' cmdlet.</span></span>
* <span data-ttu-id="71536-778">Lade till ny cmdlet: ”Remove-AzApiManagementGateway”.</span><span class="sxs-lookup"><span data-stu-id="71536-778">Added new 'Remove-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="71536-779">Lade till ny cmdlet: ”Remove-AzApiManagementGatewayHostnameConfiguration”.</span><span class="sxs-lookup"><span data-stu-id="71536-779">Added new 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="71536-780">Lade till ny cmdlet: ”Update-AzApiManagementGateway”.</span><span class="sxs-lookup"><span data-stu-id="71536-780">Added new 'Update-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="71536-781">Lade till den nya valfria parametern [-GatewayId] till cmdleten ”Get-AzApiManagementApi”.</span><span class="sxs-lookup"><span data-stu-id="71536-781">Added new optional [-GatewayId] parameter to the 'Get-AzApiManagementApi' cmdlet.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="71536-782">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="71536-782">Az.CognitiveServices</span></span>
* <span data-ttu-id="71536-783">Använde ”Neka” som standardåtgärd för NetworkRules.</span><span class="sxs-lookup"><span data-stu-id="71536-783">Used 'Deny' specifically as NetworkRules default action.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="71536-784">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="71536-784">Az.FrontDoor</span></span>
* <span data-ttu-id="71536-785">Åtgärdade ett problem där ett undantag uppstår när Enum.Parse försöker att tvinga ett null-värde till aktiverade eller inaktiverade uppräkningsvärden [#12344]</span><span class="sxs-lookup"><span data-stu-id="71536-785">Fixed an issue where an exception is being thrown when Enum.Parse tries to coerce a null value to an Enabled or Disabled enum values [#12344]</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="71536-786">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="71536-786">Az.HDInsight</span></span>
* <span data-ttu-id="71536-787">Stöd för att skapa kluster med funktionen Kryptering under överföring.</span><span class="sxs-lookup"><span data-stu-id="71536-787">Supported creating cluster with encryption in transit feature.</span></span>
    - <span data-ttu-id="71536-788">Lägg till den nya parametern ”EncryptionInTransit” till cmdleten ”New-AzHDInsightCluster”</span><span class="sxs-lookup"><span data-stu-id="71536-788">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="71536-789">Lägg till den nya parametern ”EncryptionInTransit” till cmdleten ”New-AzHDInsightClusterConfig”</span><span class="sxs-lookup"><span data-stu-id="71536-789">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="71536-790">Stöd för att skapa kluster med funktionen privat länk:</span><span class="sxs-lookup"><span data-stu-id="71536-790">Supported creating cluster with private link feature:</span></span>
    - <span data-ttu-id="71536-791">Lägg till de nya parametrarna ”PublicNetworkAccessType” och ”OutboundPublicNetworkAccessType” till cmdleten ”New-AzHDInsightCluster”</span><span class="sxs-lookup"><span data-stu-id="71536-791">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="71536-792">Lägg till de nya parametrarna ”PublicNetworkAccessType” och ”OutboundPublicNetworkAccessType” till cmdleten ”New-AzHDInsightClusterConfig”</span><span class="sxs-lookup"><span data-stu-id="71536-792">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="71536-793">Returnerade information om det virtuella nätverket vid anrop till ”New-AzHDInsightCluster” eller ”Get-AzHDInsightCluster”</span><span class="sxs-lookup"><span data-stu-id="71536-793">Returned virtual network information when calling 'New-AzHDInsightCluster' or 'Get-AzHDInsightCluster'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71536-794">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71536-794">Az.Network</span></span>
* <span data-ttu-id="71536-795">Stöd har lagts till för parametern AddressPrefixType i ”Remove-AzExpressRouteCircuitConnectionConfig”</span><span class="sxs-lookup"><span data-stu-id="71536-795">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="71536-796">Lade till bakåtkompatibel ändringar: PeerAddressType-funktioner för privat peering i ”Remove-AzExpressRouteCircutPeeringConfig”.</span><span class="sxs-lookup"><span data-stu-id="71536-796">Added non-breaking changes: PeerAddressType functionality for Private Peering in 'Remove-AzExpressRouteCircutPeeringConfig'.</span></span>
* <span data-ttu-id="71536-797">Koden ändrades för att ignorera skiftläge för parametrarna AddressPrefixType och PeerAddressType.</span><span class="sxs-lookup"><span data-stu-id="71536-797">Code changed to ignore case for AddressPrefixType and PeerAddressType parameter.</span></span>
* <span data-ttu-id="71536-798">Ändrade varningsmeddelandet för ”New-AzLoadBalancerFrontendIpConfig”, ”New-AzPublicIpAddress” och ”New-AzPublicIpPrefix”.</span><span class="sxs-lookup"><span data-stu-id="71536-798">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="71536-799">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="71536-799">Az.OperationalInsights</span></span>
* <span data-ttu-id="71536-800">Lade till alternativet ”-ForceDelete” för ”Remove-AzOperationalInsightsworkspace”</span><span class="sxs-lookup"><span data-stu-id="71536-800">Added '-ForceDelete' option for 'Remove-AzOperationalInsightsworkspace'</span></span>
* <span data-ttu-id="71536-801">Lade till ny cmdlet: ”Get-AzOperationalInsightsDeletedWorkspace”</span><span class="sxs-lookup"><span data-stu-id="71536-801">Added new cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'</span></span>
* <span data-ttu-id="71536-802">Lade till ny cmdlet: ”Restore-AzOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="71536-802">Added new cmdlet 'Restore-AzOperationalInsightsWorkspace'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="71536-803">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="71536-803">Az.RecoveryServices</span></span>
* <span data-ttu-id="71536-804">Förbättrade sättet Azure Backup-containrar/objekt identifieras.</span><span class="sxs-lookup"><span data-stu-id="71536-804">Improved the Azure Backup container/item discovery experience.</span></span>

#### <a name="azresources"></a><span data-ttu-id="71536-805">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71536-805">Az.Resources</span></span>
* <span data-ttu-id="71536-806">Lade till egenskaperna ”Condition”, ”ConditionVersion” och ”Description” till ”New-AzRoleAssignment”</span><span class="sxs-lookup"><span data-stu-id="71536-806">Added properties 'Condition', 'ConditionVersion' and 'Description' to 'New-AzRoleAssignment'</span></span>
    - <span data-ttu-id="71536-807">Detta omfattade alla relevanta ändringar av datamodellerna</span><span class="sxs-lookup"><span data-stu-id="71536-807">This included all the relevant changes to the data models</span></span>

#### <a name="azsql"></a><span data-ttu-id="71536-808">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71536-808">Az.Sql</span></span>
* <span data-ttu-id="71536-809">Korrigerade ett potentiellt fel med skiftlägesokänsliga servernamn i ”New-AzSqlServer” och ”Set-AzSqlServer”</span><span class="sxs-lookup"><span data-stu-id="71536-809">Fixed potential server name case insensitive error in 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="71536-810">Korrigerade att fel databasnamn returnerades vid ett befintligt databasfel i ”New-AzSqlDatabaseSecondary”</span><span class="sxs-lookup"><span data-stu-id="71536-810">Fixed wrong database name returned on existing database error in 'New-AzSqlDatabaseSecondary'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="71536-811">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="71536-811">Az.Storage</span></span>
* <span data-ttu-id="71536-812">Stöd för att skapa container/blob för SAS-token med de nya behörigheterna x, t</span><span class="sxs-lookup"><span data-stu-id="71536-812">Supported create container/blob Sas token with new permission x,t</span></span>
    -  <span data-ttu-id="71536-813">”New-AzStorageBlobSASToken”</span><span class="sxs-lookup"><span data-stu-id="71536-813">'New-AzStorageBlobSASToken'</span></span>
    -  <span data-ttu-id="71536-814">”New-AzStorageContainerSASToken”</span><span class="sxs-lookup"><span data-stu-id="71536-814">'New-AzStorageContainerSASToken'</span></span>
* <span data-ttu-id="71536-815">Stöd för att skapa konto för SAS-token med de nya behörigheterna x, t, f</span><span class="sxs-lookup"><span data-stu-id="71536-815">Supported create account Sas token with new permission x,t,f</span></span>
    -  <span data-ttu-id="71536-816">”New-AzStorageAccountSASToken”</span><span class="sxs-lookup"><span data-stu-id="71536-816">'New-AzStorageAccountSASToken'</span></span>
* <span data-ttu-id="71536-817">Stöd för att hämta förbrukning av enskild filresurs</span><span class="sxs-lookup"><span data-stu-id="71536-817">Supported get single file share usage</span></span>
    - <span data-ttu-id="71536-818">”Get-AzRmStorageShare”</span><span class="sxs-lookup"><span data-stu-id="71536-818">'Get-AzRmStorageShare'</span></span>

## <a name="440---july-2020"></a><span data-ttu-id="71536-819">4.4.0 – juli 2020</span><span class="sxs-lookup"><span data-stu-id="71536-819">4.4.0 - July 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="71536-820">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="71536-820">Az.Accounts</span></span>
* <span data-ttu-id="71536-821">En ny cmdlet, ”Invoke-AzRestMethod”, har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-821">Added new cmdlet 'Invoke-AzRestMethod'</span></span>
* <span data-ttu-id="71536-822">Ett problem åtgärdades som kan orsaka autentiseringsfel i scenarier med fler processer, t.ex. när flera Azure PowerShell-cmdletar körs med ”Start-Job” [#9448]</span><span class="sxs-lookup"><span data-stu-id="71536-822">Fixed an issue that may cause authentication errors in multi-process scenarios such as running multiple Azure PowerShell cmdlets using 'Start-Job' [#9448]</span></span>

#### <a name="azaks"></a><span data-ttu-id="71536-823">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="71536-823">Az.Aks</span></span>
* <span data-ttu-id="71536-824">Felet som gjorde att ”Get-AzAks” inte hämtade alla kluster har åtgärdats [#12296]</span><span class="sxs-lookup"><span data-stu-id="71536-824">Fixed bug 'Get-AzAks' doesn't get all clusters [#12296]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="71536-825">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="71536-825">Az.AnalysisServices</span></span>
* <span data-ttu-id="71536-826">Projektreferensen till autentisering har tagits bort</span><span class="sxs-lookup"><span data-stu-id="71536-826">Removed project reference to Authentication</span></span>

#### <a name="azautomation"></a><span data-ttu-id="71536-827">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="71536-827">Az.Automation</span></span>
* <span data-ttu-id="71536-828">Problemet som gjorde att strängar med escape-tecken inte kunde konverteras till JSON-objekt har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="71536-828">Fixed the issue that string with escape chars cannot be converted into json object.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71536-829">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71536-829">Az.Compute</span></span>
* <span data-ttu-id="71536-830">En varning har lats till som visas när ”New-AzVmss” används utan den senaste avbildningsversionen</span><span class="sxs-lookup"><span data-stu-id="71536-830">Added warning when using 'New-AzVmss' without 'latest' image version</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="71536-831">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="71536-831">Az.DataFactory</span></span>
* <span data-ttu-id="71536-832">Globala parametrar har lagts till för Data Factory.</span><span class="sxs-lookup"><span data-stu-id="71536-832">Added global parameters to Data Factory.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="71536-833">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="71536-833">Az.EventGrid</span></span>
* <span data-ttu-id="71536-834">Modulen har uppdaterats så att API-version 2020-06-01 används.</span><span class="sxs-lookup"><span data-stu-id="71536-834">Updated to use the 2020-06-01 API version.</span></span>
* <span data-ttu-id="71536-835">Nya funktioner har lagts till:</span><span class="sxs-lookup"><span data-stu-id="71536-835">Added new features:</span></span>
    - <span data-ttu-id="71536-836">Indatamappning</span><span class="sxs-lookup"><span data-stu-id="71536-836">Input mapping</span></span>
    - <span data-ttu-id="71536-837">Schema för händelseleverans</span><span class="sxs-lookup"><span data-stu-id="71536-837">Event Delivery Schema</span></span>
    - <span data-ttu-id="71536-838">Private Link</span><span class="sxs-lookup"><span data-stu-id="71536-838">Private Link</span></span>
    - <span data-ttu-id="71536-839">Cloud Event V10 Schema</span><span class="sxs-lookup"><span data-stu-id="71536-839">Cloud Event V10 Schema</span></span>
    - <span data-ttu-id="71536-840">Service Bus-ämne som mål</span><span class="sxs-lookup"><span data-stu-id="71536-840">Service Bus Topic As Destination</span></span>
    - <span data-ttu-id="71536-841">Azure-funktion som mål</span><span class="sxs-lookup"><span data-stu-id="71536-841">Azure Function As Destination</span></span>
    - <span data-ttu-id="71536-842">Webhook-batchbearbetning</span><span class="sxs-lookup"><span data-stu-id="71536-842">WebHook Batching</span></span>
    - <span data-ttu-id="71536-843">Säker webhook (AAD-stöd)</span><span class="sxs-lookup"><span data-stu-id="71536-843">Secure webhook (AAD support)</span></span>
    - <span data-ttu-id="71536-844">IpFiltering</span><span class="sxs-lookup"><span data-stu-id="71536-844">IpFiltering</span></span>
* <span data-ttu-id="71536-845">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="71536-845">Updated cmdlets:</span></span>
    - <span data-ttu-id="71536-846">”New-AzEventGridSubscription”/”Update-AzEventGridSubscription”:</span><span class="sxs-lookup"><span data-stu-id="71536-846">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span></span>
        - <span data-ttu-id="71536-847">Lägg till nya valfria parametrar för att ge stöd för webhook-batchbearbetning.</span><span class="sxs-lookup"><span data-stu-id="71536-847">Add new optional parameters to support webhook batching.</span></span>
        - <span data-ttu-id="71536-848">Lägg till nya valfria parametrar för att ge stöd för skyddad webhook med AAD.</span><span class="sxs-lookup"><span data-stu-id="71536-848">Add new optional parameters to support secured webhook using AAD.</span></span>
        - <span data-ttu-id="71536-849">Lägg till ny enum (uppräkning) för EndpointType-parametern för att ge stöd för Azure-funktion och Service Bus-ämne som nya mål.</span><span class="sxs-lookup"><span data-stu-id="71536-849">Add new enum for EndpointType parameter to support azure function and service bus topic as new destinations.</span></span>
        - <span data-ttu-id="71536-850">Lägg till ny valfri parameter för leveransschema.</span><span class="sxs-lookup"><span data-stu-id="71536-850">Add new optional parameter for delivery schema.</span></span>
    - <span data-ttu-id="71536-851">”New-AzEventGridTopic”/”Update-AzEventGridTopic” och ”New-AzEventGridDomain”/”Update-AzEventGridDomain”:</span><span class="sxs-lookup"><span data-stu-id="71536-851">'New-AzEventGridTopic'/'Update-AzEventGridTopic' and 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span></span>
        - <span data-ttu-id="71536-852">Lägg till nya valfria parametrar för att ge stöd för IpFiltering.</span><span class="sxs-lookup"><span data-stu-id="71536-852">Add new optional parameters to support IpFiltering.</span></span>
    - <span data-ttu-id="71536-853">”New-AzEventGridTopic”/”New-AzEventGridDomain”:</span><span class="sxs-lookup"><span data-stu-id="71536-853">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span></span>
        - <span data-ttu-id="71536-854">Lägg till nya valfria parametrar för att ge stöd för indatamappning.</span><span class="sxs-lookup"><span data-stu-id="71536-854">Add new optional parameters to support Input mapping.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="71536-855">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="71536-855">Az.FrontDoor</span></span>
* <span data-ttu-id="71536-856">Modulen har uppdaterats så att API 2020-05-01 används</span><span class="sxs-lookup"><span data-stu-id="71536-856">Updated module to use API 2020-05-01</span></span>
* <span data-ttu-id="71536-857">Stöd för privat länk har lagts till för Storage-, KeyVault- och Web App Service-resurser</span><span class="sxs-lookup"><span data-stu-id="71536-857">Added Private link support for Storage, Keyvault and Web App Service resources</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="71536-858">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="71536-858">Az.HDInsight</span></span>
* <span data-ttu-id="71536-859">Stöd för att skapa kluster med ADLSGen1/2-lagring i nationella moln.</span><span class="sxs-lookup"><span data-stu-id="71536-859">Supported creating cluster with ADLSGen1/2 storage in national clouds.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="71536-860">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="71536-860">Az.Monitor</span></span>
* <span data-ttu-id="71536-861">Bugg som orsakade fel med ”Get-AzDiagnosticSetting” när mått eller loggar var null har åtgärdats [#12272]</span><span class="sxs-lookup"><span data-stu-id="71536-861">Fixed bug for 'Get-AzDiagnosticSetting' when metrics or logs are null [#12272]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71536-862">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71536-862">Az.Network</span></span>
* <span data-ttu-id="71536-863">Parameterväxlingen i VWan HubVnet-anslutningar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="71536-863">Fixed parameters swap in VWan HubVnet connection</span></span>
* <span data-ttu-id="71536-864">Nya cmdletar har lagts till för platser för virtuella installationer i Azure-nätverk</span><span class="sxs-lookup"><span data-stu-id="71536-864">Added new cmdlets for Azure Network Virtual Appliance Sites</span></span>
    - <span data-ttu-id="71536-865">”Get-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="71536-865">'Get-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="71536-866">”New-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="71536-866">'New-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="71536-867">”Remove-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="71536-867">'Remove-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="71536-868">”Update-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="71536-868">'Update-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="71536-869">”New-AzOffice365PolicyProperty”</span><span class="sxs-lookup"><span data-stu-id="71536-869">'New-AzOffice365PolicyProperty'</span></span>
* <span data-ttu-id="71536-870">Nya cmdletar har lagts till för virtuella installationer i Azure-nätverk</span><span class="sxs-lookup"><span data-stu-id="71536-870">Added new cmdlets for Azure Network Virtual Appliance</span></span>
    - <span data-ttu-id="71536-871">”Get-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="71536-871">'Get-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="71536-872">”New-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="71536-872">'New-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="71536-873">”Remove-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="71536-873">'Remove-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="71536-874">”Update-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="71536-874">'Update-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="71536-875">”Get-AzNetworkVirtualApplianceSku”</span><span class="sxs-lookup"><span data-stu-id="71536-875">'Get-AzNetworkVirtualApplianceSku'</span></span>
    - <span data-ttu-id="71536-876">”New-AzVirtualApplianceSkuProperty”</span><span class="sxs-lookup"><span data-stu-id="71536-876">'New-AzVirtualApplianceSkuProperty'</span></span>
* <span data-ttu-id="71536-877">Application Gateway har introducerats i vanliga cmdletar för Private Link</span><span class="sxs-lookup"><span data-stu-id="71536-877">Onboarded Application Gateway to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="71536-878">StorageSync har introducerats i vanliga cmdletar för Private Link</span><span class="sxs-lookup"><span data-stu-id="71536-878">Onboarded StorageSync to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="71536-879">SignalR har introducerats i vanliga cmdletar för Private Link</span><span class="sxs-lookup"><span data-stu-id="71536-879">Onboarded SignalR to Private Link Common Cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="71536-880">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="71536-880">Az.RecoveryServices</span></span>
* <span data-ttu-id="71536-881">Projektreferensen till autentisering har tagits bort</span><span class="sxs-lookup"><span data-stu-id="71536-881">Removed project reference to Authentication</span></span>
* <span data-ttu-id="71536-882">Azure Backup-anpassade cmdletar gör text mer korrekt.</span><span class="sxs-lookup"><span data-stu-id="71536-882">Azure Backup tuned cmdlets help text to be more accurate.</span></span>
* <span data-ttu-id="71536-883">Stöd har lagts till som gör att Azure Backup kan hämta MAB-agentjobb med cmdleten ”Get-AzRecoveryServicesBackupJob”.</span><span class="sxs-lookup"><span data-stu-id="71536-883">Azure Backup added support for fetching MAB agent jobs using 'Get-AzRecoveryServicesBackupJob' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="71536-884">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71536-884">Az.Resources</span></span>
* <span data-ttu-id="71536-885">”Save-AzResourceGroupDeploymentTemplate” har uppdaterats för att använda SDK:n.</span><span class="sxs-lookup"><span data-stu-id="71536-885">Updated 'Save-AzResourceGroupDeploymentTemplate' to use the SDK.</span></span>
* <span data-ttu-id="71536-886">Cmdleten ”Unregister-AzResourceProvider” har lagts till.</span><span class="sxs-lookup"><span data-stu-id="71536-886">Added 'Unregister-AzResourceProvider' cmdlet.</span></span>

#### <a name="azsql"></a><span data-ttu-id="71536-887">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71536-887">Az.Sql</span></span>
* <span data-ttu-id="71536-888">Stöd har lagts till för SPN och gästanvändare i cmdleten ”Set-AzSqlInstanceActiveDirectoryAdministrator”</span><span class="sxs-lookup"><span data-stu-id="71536-888">Added support for Service principal and guest users in Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet'</span></span>
* <span data-ttu-id="71536-889">En bugg har åtgärdats i cmdletar för dataklassificering.</span><span class="sxs-lookup"><span data-stu-id="71536-889">Fixed a bug in Data Classification cmdlets.'</span></span>
* <span data-ttu-id="71536-890">Stöd har lagts till för redundansväxling med Azure SQL Managed Instance: ”Invoke-AzSqlInstanceFailover”</span><span class="sxs-lookup"><span data-stu-id="71536-890">Added support for Azure SQL Managed Instance failover: 'Invoke-AzSqlInstanceFailover'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="71536-891">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="71536-891">Az.Storage</span></span>
* <span data-ttu-id="71536-892">Problemet som gjorde att UserAgent inte lades till för vissa cmdletar för dataplanet har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="71536-892">Fixed the issue that UserAgent is not added for some data plane cmdlets.</span></span>
* <span data-ttu-id="71536-893">Stöd har lagts till för att skapa/uppdatera Storage-konto med MinimumTlsVersion och AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="71536-893">Supported create/update Storage account with MinimumTlsVersion and AllowBlobPublicAccess</span></span>
    -  <span data-ttu-id="71536-894">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="71536-894">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="71536-895">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="71536-895">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="71536-896">Stöd har lagts till för att aktivera/inaktivera versionshantering i Blob Service för ett Storage-konto</span><span class="sxs-lookup"><span data-stu-id="71536-896">Support enable/disable versioning on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="71536-897">”Update-AzStorageBlobServiceProperty”</span><span class="sxs-lookup"><span data-stu-id="71536-897">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="71536-898">Stöd har lagts till för att visa blobar med blobversioner</span><span class="sxs-lookup"><span data-stu-id="71536-898">Support list blobs with blob versions</span></span>
    - <span data-ttu-id="71536-899">”Get-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="71536-899">'Get-AzStorageBlob'</span></span>
* <span data-ttu-id="71536-900">Stöd har lagts till för att hämta/ta bort enskilda ögonblicksbilder av blobar eller blobversioner</span><span class="sxs-lookup"><span data-stu-id="71536-900">Support get/remove single blob snapshot or blob version</span></span>
    - <span data-ttu-id="71536-901">”Get-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="71536-901">'Get-AzStorageBlob'</span></span>
    - <span data-ttu-id="71536-902">”Remove-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="71536-902">'Remove-AzStorageBlob'</span></span>
* <span data-ttu-id="71536-903">Stöd har lagts till för pipelines från blobobjekt genererade av Azure.Storage.Blobs V12</span><span class="sxs-lookup"><span data-stu-id="71536-903">Support pipeline from blob object generated from Azure.Storage.Blobs V12</span></span>
    - <span data-ttu-id="71536-904">”Get-AzStorageBlobContent”</span><span class="sxs-lookup"><span data-stu-id="71536-904">'Get-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="71536-905">”New-AzStorageBlobSASToken”</span><span class="sxs-lookup"><span data-stu-id="71536-905">'New-AzStorageBlobSASToken'</span></span>
    - <span data-ttu-id="71536-906">”Remove-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="71536-906">'Remove-AzStorageBlob'</span></span>
    - <span data-ttu-id="71536-907">”Set-AzStorageBlobContent”</span><span class="sxs-lookup"><span data-stu-id="71536-907">'Set-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="71536-908">”Start-AzStorageBlobCopy”</span><span class="sxs-lookup"><span data-stu-id="71536-908">'Start-AzStorageBlobCopy'</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="71536-909">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="71536-909">Az.StorageSync</span></span>
* <span data-ttu-id="71536-910">En ny version har lagts till för StorageSync SDK som körs mot ApiVersion 2020-03-01</span><span class="sxs-lookup"><span data-stu-id="71536-910">Added a new version StorageSync SDK targeting ApiVersion 2020-03-01</span></span>
* <span data-ttu-id="71536-911">En cmdlet för synkroniseringstjänsten för lagringsuppdatering har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-911">Added Update Storage Sync Service cmdlet</span></span>
    - <span data-ttu-id="71536-912">”Set-AzStorageSyncService”</span><span class="sxs-lookup"><span data-stu-id="71536-912">'Set-AzStorageSyncService'</span></span>
* <span data-ttu-id="71536-913">IncomingTrafficPolicy och PrivateEndpointConnections har lagts till för StorageSyncService-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="71536-913">Added IncomingTrafficPolicy and PrivateEndpointConnections to StorageSyncService cmdlets.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="71536-914">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="71536-914">Az.Websites</span></span>
* <span data-ttu-id="71536-915">Stöd har lagts till för att utföra åtgärder för platser som inte tillhör samma resursgrupp som App Services-planen</span><span class="sxs-lookup"><span data-stu-id="71536-915">Added support to perform operations for Slots not in the same resource group as the App Service Plan</span></span>

## <a name="430---june-2020"></a><span data-ttu-id="71536-916">4.3.0 – juni 2020</span><span class="sxs-lookup"><span data-stu-id="71536-916">4.3.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="71536-917">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="71536-917">Az.Accounts</span></span>
* <span data-ttu-id="71536-918">Stöd för identifiering av miljöinställning som standard och tillägg av miljön via ”Add-AzEnvironment”</span><span class="sxs-lookup"><span data-stu-id="71536-918">Supported discovering environment setting by default and adding environment via 'Add-AzEnvironment'</span></span>
* <span data-ttu-id="71536-919">Uppdatera förinlästa sammansättningar [#12024], [#11976]</span><span class="sxs-lookup"><span data-stu-id="71536-919">Update preloaded assemblies [#12024], [#11976]</span></span>
* <span data-ttu-id="71536-920">Uppdaterad Azure.Core-sammansättning</span><span class="sxs-lookup"><span data-stu-id="71536-920">Updated Azure.Core assembly</span></span>
* <span data-ttu-id="71536-921">Ett problem har åtgärdats som kan orsaka att ”Connect-AzAccount” misslyckas vid körning av flera trådar [#11201]</span><span class="sxs-lookup"><span data-stu-id="71536-921">Fixed an issue that may cause 'Connect-AzAccount' to fail in multi-threaded execution [#11201]</span></span>

#### <a name="azaks"></a><span data-ttu-id="71536-922">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="71536-922">Az.Aks</span></span>
* <span data-ttu-id="71536-923">Användning av gamla [AccessProfile API](/rest/api/aks/managedclusters/getaccessprofile) ersattes med anrop till API:erna [ListClusterAdmin](/rest/api/aks/managedclusters/listclusteradmincredentials) och [ListClusterUser](/rest/api/aks/managedclusters/listclusterusercredentials)</span><span class="sxs-lookup"><span data-stu-id="71536-923">Replaced usage of old [AccessProfile API](/rest/api/aks/managedclusters/getaccessprofile) with calls to [ListClusterAdmin](/rest/api/aks/managedclusters/listclusteradmincredentials) and [ListClusterUser](/rest/api/aks/managedclusters/listclusterusercredentials) APIs</span></span>

#### <a name="azbatch"></a><span data-ttu-id="71536-924">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="71536-924">Az.Batch</span></span>
* <span data-ttu-id="71536-925">Az.Batch har uppdaterats att använda ”Microsoft.Azure.Management.Batch” SDK till och med version 11.0.0.</span><span class="sxs-lookup"><span data-stu-id="71536-925">Updated Az.Batch to use 'Microsoft.Azure.Management.Batch' SDK version to 11.0.0</span></span>
* <span data-ttu-id="71536-926">Möjligheten att ange BatchAccount-identiteten har lagts till i cmdleten ”New-AzBatchAccount”</span><span class="sxs-lookup"><span data-stu-id="71536-926">Added the ability to set the BatchAccount Identity in the 'New-AzBatchAccount' cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="71536-927">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="71536-927">Az.CognitiveServices</span></span>
* <span data-ttu-id="71536-928">Stöd för att visa kontofunktioner.</span><span class="sxs-lookup"><span data-stu-id="71536-928">Supported displaying account capabilities.</span></span>
* <span data-ttu-id="71536-929">Stöd för att ändra PublicNetworkAccess.</span><span class="sxs-lookup"><span data-stu-id="71536-929">Supported modifying PublicNetworkAccess.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71536-930">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71536-930">Az.Compute</span></span>
* <span data-ttu-id="71536-931">Parametern SimulateEviction har lagts till i cmdletarna set-AzVM och set-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="71536-931">Added SimulateEviction parameter to Set-AzVM and Set-AzVmssVM cmdlets.</span></span>
* <span data-ttu-id="71536-932">”Premium_LRS” har lagts till i argumentslutföraren för parametern StorageAccountType för cmdleten New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="71536-932">Added 'Premium_LRS' to the argument completer of StorageAccountType parameter for New-AzGalleryImageVersion cmdlet.</span></span>
* <span data-ttu-id="71536-933">Understatusar har lagts till i VMCustomScriptExtension [#11297]</span><span class="sxs-lookup"><span data-stu-id="71536-933">Added Substatuses to VMCustomScriptExtension [#11297]</span></span>
* <span data-ttu-id="71536-934">”Delete” har lagts till i argumentslutföraren för parametern EvictionPolicy för cmdletarna New-AzVM och New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="71536-934">Added 'Delete' to the argument completer of EvictionPolicy parameter for New-AzVM and New-AzVMConfig cmdlets.</span></span>
* <span data-ttu-id="71536-935">Åtgärdat namn för nytt VM-tillägg för SAP</span><span class="sxs-lookup"><span data-stu-id="71536-935">Fixed name of new VM Extension for SAP</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="71536-936">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="71536-936">Az.DataFactory</span></span>
* <span data-ttu-id="71536-937">ADF .Net SDK har uppdaterats till 4.9.0</span><span class="sxs-lookup"><span data-stu-id="71536-937">Updated ADF .Net SDK version to 4.9.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="71536-938">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="71536-938">Az.EventHub</span></span>
* <span data-ttu-id="71536-939">Parametrar för hanterad identitet har lagts till i cmdletarna ”New-AzEventHubNamespace” och ”set-AzEventHubNamespace”</span><span class="sxs-lookup"><span data-stu-id="71536-939">Added Managed Identity parameters to 'New-AzEventHubNamespace' and 'Set-AzEventHubNamespace' cmdlets</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="71536-940">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="71536-940">Az.Functions</span></span>
* <span data-ttu-id="71536-941">Stöd har lagts till för att skapa PowerShell 7.0- och Java 11-funktionsappar</span><span class="sxs-lookup"><span data-stu-id="71536-941">Added support to create PowerShell 7.0 and Java 11 function apps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="71536-942">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="71536-942">Az.HDInsight</span></span>
* <span data-ttu-id="71536-943">Stöd för listning av värdar och omstart för specifika värdar i HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="71536-943">Supported listing hosts and restart specific hosts of the HDInsight cluster.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="71536-944">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="71536-944">Az.HealthcareApis</span></span>
* <span data-ttu-id="71536-945">Uppdaterade SDK-versionen till 1.1.0</span><span class="sxs-lookup"><span data-stu-id="71536-945">Updated the SDK version to 1.1.0</span></span>
* <span data-ttu-id="71536-946">Stöd har lagts till för exportinställningar och hanterad identitet</span><span class="sxs-lookup"><span data-stu-id="71536-946">Added support for Export settings and Managed Identity</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="71536-947">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="71536-947">Az.Monitor</span></span>
* <span data-ttu-id="71536-948">Parameter för inmatningsobjekt har åtgärdats för ”Set-AzActivityLogAlert”</span><span class="sxs-lookup"><span data-stu-id="71536-948">Fixed input object parameter for 'Set-AzActivityLogAlert'</span></span>
* <span data-ttu-id="71536-949">Parametern ”InputObject” har åtgärdats för ”Set-AzActionGroup” [#10868]</span><span class="sxs-lookup"><span data-stu-id="71536-949">Fixed 'InputObject' parameter for 'Set-AzActionGroup' [#10868]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71536-950">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71536-950">Az.Network</span></span>
* <span data-ttu-id="71536-951">Stöd har lagts till för parametern AddressPrefixType i ”Remove-AzExpressRouteCircuitConnectionConfig”</span><span class="sxs-lookup"><span data-stu-id="71536-951">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="71536-952">Nya cmdletar har lagts till för Azure FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="71536-952">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="71536-953">”New-AzFirewallPolicyDnsSetting”</span><span class="sxs-lookup"><span data-stu-id="71536-953">'New-AzFirewallPolicyDnsSetting'</span></span>
    - <span data-ttu-id="71536-954">Stöd för mål-FQDN i nätverksregler för brandväggsprincip</span><span class="sxs-lookup"><span data-stu-id="71536-954">Support for Destination FQDN in Network Rules for Firewall Policy</span></span>
* <span data-ttu-id="71536-955">Stöd har lagts till för åtgärder i serverdelsadresspooler</span><span class="sxs-lookup"><span data-stu-id="71536-955">Added support for backend address pool operations</span></span>
    - <span data-ttu-id="71536-956">”New-AzLoadBalancerBackendAddressConfig”</span><span class="sxs-lookup"><span data-stu-id="71536-956">'New-AzLoadBalancerBackendAddressConfig'</span></span>
    - <span data-ttu-id="71536-957">”New-AzLoadBalancerBackendAddressPool”</span><span class="sxs-lookup"><span data-stu-id="71536-957">'New-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="71536-958">”Set-AzLoadBalancerBackendAddressPool”</span><span class="sxs-lookup"><span data-stu-id="71536-958">'Set-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="71536-959">”Remove-AzLoadBalancerBackendAddressPool”</span><span class="sxs-lookup"><span data-stu-id="71536-959">'Remove-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="71536-960">”Get-AzLoadBalancerBackendAddressPool”</span><span class="sxs-lookup"><span data-stu-id="71536-960">'Get-AzLoadBalancerBackendAddressPool'</span></span>
* <span data-ttu-id="71536-961">Namnvalidering har lagts till för ”New-AzIpGroup”</span><span class="sxs-lookup"><span data-stu-id="71536-961">Added name validation for 'New-AzIpGroup'</span></span>
* <span data-ttu-id="71536-962">Nya cmdletar har lagts till för Azure FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="71536-962">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="71536-963">”New-AzFirewallPolicyThreatIntelWhitelist”</span><span class="sxs-lookup"><span data-stu-id="71536-963">'New-AzFirewallPolicyThreatIntelWhitelist'</span></span>
* <span data-ttu-id="71536-964">Nedanstående kommandon för funktionen har uppdaterats: Konfiguration/borttagning av anpassade DNS-servrar på VirtualWan P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="71536-964">Updated below commands for feature: Custom dns servers set/remove on VirtualWan P2SVpnGateway.</span></span>
    - <span data-ttu-id="71536-965">New-AzP2sVpnGateway har uppdaterats: Den valfria parametern ”-CustomDnsServer” har lagts till för att kunder ska kunna ange att deras DNS-servrar ska konfigureras på P2SVpnGateway, som kan användas av punkt-till-plats-klienter.</span><span class="sxs-lookup"><span data-stu-id="71536-965">Updated New-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
    - <span data-ttu-id="71536-966">Update-AzP2sVpnGateway har uppdaterats: Den valfria parametern ”-CustomDnsServer” har lagts till för att kunder ska kunna ange att deras DNS-servrar ska konfigureras på P2SVpnGateway, som kan användas av punkt-till-plats-klienter.</span><span class="sxs-lookup"><span data-stu-id="71536-966">Updated Update-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
* <span data-ttu-id="71536-967">”Update-AzVpnGateway” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="71536-967">Updated 'Update-AzVpnGateway'</span></span>
    - <span data-ttu-id="71536-968">Den valfria parametern ”-BgpPeeringAddress” har lagts till för att kunder ska kunna ange sina anpassade BGP:er som ska konfigurerar på VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="71536-968">Added optional parameter '-BgpPeeringAddress' for customers to specify their custom bgps to set on VpnGateway.</span></span>
* <span data-ttu-id="71536-969">Ny cmdlet har lagts till för att stödja återställning av en VirtualHub-resurs routningsstatus:</span><span class="sxs-lookup"><span data-stu-id="71536-969">Added new cmdlet to support resetting the routing state of a VirtualHub resource:</span></span>
    - <span data-ttu-id="71536-970">”Reset-AzHubRouter”</span><span class="sxs-lookup"><span data-stu-id="71536-970">'Reset-AzHubRouter'</span></span>
* <span data-ttu-id="71536-971">Nedanstående saker har uppdaterats baserat på den senaste Swagger-ändringen för brandväggspolicyn</span><span class="sxs-lookup"><span data-stu-id="71536-971">Updated below things based on recent swagger change for Firewall Policy</span></span>
    - <span data-ttu-id="71536-972">Namn ändras för RuleGroup, RuleCollectionGroup och RuleType</span><span class="sxs-lookup"><span data-stu-id="71536-972">Changes names for RuleGroup, RuleCollectionGroup and RuleType</span></span>
    - <span data-ttu-id="71536-973">Stöd har lagts till för NAT-regelsamlingar för brandväggsprincip så att flera NAT-regelsamlingar stöds</span><span class="sxs-lookup"><span data-stu-id="71536-973">Added support for Firewall Policy NAT Rule Collections to support multiple NAT Rule Collection</span></span>
* <span data-ttu-id="71536-974">[Icke-bakåtkompatibel ändring] Den obligatoriska parametern ”SourceIpGroup” har lagts till för ”New-AzFirewallPolicyApplicationRule” och ”New-AzFirewallPolicyNetworkRule”.</span><span class="sxs-lookup"><span data-stu-id="71536-974">[Breaking Change] Added mandatory parameter 'SourceIpGroup' for 'New-AzFirewallPolicyApplicationRule' and 'New-AzFirewallPolicyNetworkRule'.</span></span>
* <span data-ttu-id="71536-975">[Icke-bakåtkompatibel ändring] ”New-AzFirewallPolicyApplicationRule” har åtgärdats, parametern ”SourceAddress” är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="71536-975">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="71536-976">[Icke-bakåtkompatibel ändring] ”New-AzFirewallPolicyApplicationRule” har åtgärdats, parametern ”SourceAddress” är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="71536-976">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="71536-977">[Icke-bakåtkompatibel ändring] Obligatoriska parametrar har tagits bort: ”TranslatedAddress”, ”TranslatedPort” för ”New-AzFirewallPolicyNatRuleCollection”.</span><span class="sxs-lookup"><span data-stu-id="71536-977">[Breaking Change] Removed mandatory parameters: 'TranslatedAddress', 'TranslatedPort' for 'New-AzFirewallPolicyNatRuleCollection'.</span></span>
* <span data-ttu-id="71536-978">Nya cmdletar har lagts till för att stödja PrivateLink på Application Gateway</span><span class="sxs-lookup"><span data-stu-id="71536-978">Added new cmdlets to support PrivateLink On Application Gateway</span></span>
    - <span data-ttu-id="71536-979">”New-AzApplicationGatewayPrivateLinkConfiguration”</span><span class="sxs-lookup"><span data-stu-id="71536-979">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="71536-980">”Get-AzApplicationGatewayPrivateLinkConfiguration”</span><span class="sxs-lookup"><span data-stu-id="71536-980">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="71536-981">”New-AzApplicationGatewayPrivateLinkConfiguration”</span><span class="sxs-lookup"><span data-stu-id="71536-981">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="71536-982">”Set-AzApplicationGatewayPrivateLinkConfiguration”</span><span class="sxs-lookup"><span data-stu-id="71536-982">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="71536-983">”Remove-AzApplicationGatewayPrivateLinkConfiguration”</span><span class="sxs-lookup"><span data-stu-id="71536-983">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="71536-984">”New-AzApplicationGatewayPrivateLinkIpConfiguration”</span><span class="sxs-lookup"><span data-stu-id="71536-984">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span></span>
* <span data-ttu-id="71536-985">Nya cmdletar har lagts till för VirtualHubs underordnade resurs HubRouteTables.</span><span class="sxs-lookup"><span data-stu-id="71536-985">Added new cmdlets for HubRouteTables child resource of VirtualHub.</span></span>
    - <span data-ttu-id="71536-986">”New-AzVHubRoute”</span><span class="sxs-lookup"><span data-stu-id="71536-986">'New-AzVHubRoute'</span></span>
    - <span data-ttu-id="71536-987">”New-AzVHubRouteTable”</span><span class="sxs-lookup"><span data-stu-id="71536-987">'New-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="71536-988">”Get-AzVHubRouteTable”</span><span class="sxs-lookup"><span data-stu-id="71536-988">'Get-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="71536-989">”Update-AzVHubRouteTable”</span><span class="sxs-lookup"><span data-stu-id="71536-989">'Update-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="71536-990">”Remove-AzVHubRouteTable”</span><span class="sxs-lookup"><span data-stu-id="71536-990">'Remove-AzVHubRouteTable'</span></span>
* <span data-ttu-id="71536-991">Befintliga cmdletar har uppdaterats för att stödja valfri RoutingConfiguration-indataparameter för anpassad routning i VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="71536-991">Updated existing cmdlets to support optional RoutingConfiguration input parameter for custom routing in VirtualWan.</span></span>
    - <span data-ttu-id="71536-992">”New-AzExpressRouteConnection”</span><span class="sxs-lookup"><span data-stu-id="71536-992">'New-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="71536-993">”Set-AzExpressRouteConnection”</span><span class="sxs-lookup"><span data-stu-id="71536-993">'Set-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="71536-994">”New-AzVirtualHubVnetConnection”</span><span class="sxs-lookup"><span data-stu-id="71536-994">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="71536-995">”Update-AzVirtualHubVnetConnection”</span><span class="sxs-lookup"><span data-stu-id="71536-995">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="71536-996">”New-AzVpnConnection”</span><span class="sxs-lookup"><span data-stu-id="71536-996">'New-AzVpnConnection'</span></span>
    - <span data-ttu-id="71536-997">”Update-AzVpnConnection”</span><span class="sxs-lookup"><span data-stu-id="71536-997">'Update-AzVpnConnection'</span></span>
    - <span data-ttu-id="71536-998">”New-AzP2sVpnGateway”</span><span class="sxs-lookup"><span data-stu-id="71536-998">'New-AzP2sVpnGateway'</span></span>
    - <span data-ttu-id="71536-999">”Update-AzP2sVpnGateway”</span><span class="sxs-lookup"><span data-stu-id="71536-999">'Update-AzP2sVpnGateway'</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="71536-1000">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="71536-1000">Az.OperationalInsights</span></span>
* <span data-ttu-id="71536-1001">Fast fel PSWorkspace implementerar inte IOperationalInsightsWorkspace [#12135]</span><span class="sxs-lookup"><span data-stu-id="71536-1001">Fixed bug PSWorkspace doesn't implement IOperationalInsightsWorkspace [#12135]</span></span>
* <span data-ttu-id="71536-1002">”pergb2018” har lagts till i uppsättningen med giltiga värden för parametern ”Sku” i ”Set-AzOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="71536-1002">Added 'pergb2018' to valid value set of parameter 'Sku' in 'Set-AzOperationalInsightsWorkspace'</span></span> 
* <span data-ttu-id="71536-1003">Alias ”FunctionParameters” lades till för parametern ”FunctionParameter” till</span><span class="sxs-lookup"><span data-stu-id="71536-1003">Added alias 'FunctionParameters' for parameter 'FunctionParameter' to</span></span>
    - <span data-ttu-id="71536-1004">”New-AzOperationalInsightsSavedSearch”</span><span class="sxs-lookup"><span data-stu-id="71536-1004">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="71536-1005">”Set-AzOperationalInsightsSavedSearch”</span><span class="sxs-lookup"><span data-stu-id="71536-1005">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="71536-1006">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="71536-1006">Az.RecoveryServices</span></span>
* <span data-ttu-id="71536-1007">Azure Backup har fått stöd för att hämta MAB-objekt.</span><span class="sxs-lookup"><span data-stu-id="71536-1007">Azure Backup added support for fetching MAB items.</span></span>
* <span data-ttu-id="71536-1008">Azure Site Recovery stöder disktypen ”StandardSSD_LRS”</span><span class="sxs-lookup"><span data-stu-id="71536-1008">Azure Site Recovery supports disk type 'StandardSSD_LRS'</span></span>

#### <a name="azresources"></a><span data-ttu-id="71536-1009">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71536-1009">Az.Resources</span></span>
* <span data-ttu-id="71536-1010">”UsageLocation”, ”GivenName”, ”Surname”, ”AccountEnabled”, ”MailNickname”, ”Mail” på ”PSADUser” lades till [#10526] [#10497]</span><span class="sxs-lookup"><span data-stu-id="71536-1010">Added 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' on 'PSADUser' [#10526] [#10497]</span></span>
* <span data-ttu-id="71536-1011">Problem med att ”-Mail” inte fungerar på ”Get-AzADUser” har åtgärdats [#11981]</span><span class="sxs-lookup"><span data-stu-id="71536-1011">Fixed issue that '-Mail' doesn't work on 'Get-AzADUser' [#11981]</span></span>
* <span data-ttu-id="71536-1012">Parametern ”-ExcludeChangeType” har lagts till i ”Get-AzDeploymentWhatIfResult” och ”Get-AzResourceGroupDeploymentWhatIfResult”</span><span class="sxs-lookup"><span data-stu-id="71536-1012">Added '-ExcludeChangeType' parameter to 'Get-AzDeploymentWhatIfResult' and 'Get-AzResourceGroupDeploymentWhatIfResult'</span></span>
* <span data-ttu-id="71536-1013">Parametern ”-WhatIfExcludeChangeType” har lagts till i ”New-AzDeployment” och ”New-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="71536-1013">Added '-WhatIfExcludeChangeType' parameter to 'New-AzDeployment' and 'New-AzResourceGroupDeployment'</span></span>
* <span data-ttu-id="71536-1014">Cmdletar för ”Test-Az\*Deployment” har uppdaterats för att visa bättre felmeddelanden</span><span class="sxs-lookup"><span data-stu-id="71536-1014">Updated 'Test-Az\*Deployment' cmdlets to show better error messages</span></span>
* <span data-ttu-id="71536-1015">Hjälpmeddelandet för parametern ”-Name” i distributionsskapande och What If-cmdletar</span><span class="sxs-lookup"><span data-stu-id="71536-1015">Fixed help message for '-Name' parameter of deployment create and What-If cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="71536-1016">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71536-1016">Az.Sql</span></span>
* <span data-ttu-id="71536-1017">Stöd för tjänsthuvudnamn har lagts till för administratörs-cmdlet för SQL Server Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="71536-1017">Added support for service principal for Set SQL Server Azure Active Directory Admin cmdlet</span></span>
* <span data-ttu-id="71536-1018">Synkroniseringsproblem i Data Classification-cmdletar har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="71536-1018">Fixed sync issue in Data Classification cmdlets.</span></span>
* <span data-ttu-id="71536-1019">Stöd för att söka efter användare via e-postadress på ”Set-AzSqlServerActiveDirectoryAdministrator” [#12192]</span><span class="sxs-lookup"><span data-stu-id="71536-1019">Supported searching user by mail on 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span></span>

#### <a name="azstorage"></a><span data-ttu-id="71536-1020">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="71536-1020">Az.Storage</span></span>
* <span data-ttu-id="71536-1021">Skapa lagringskonto med RequireInfrastructureEncryption stöds</span><span class="sxs-lookup"><span data-stu-id="71536-1021">Supported create Storage account with RequireInfrastructureEncryption</span></span>
    -  <span data-ttu-id="71536-1022">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="71536-1022">'New-AzStorageAccount'</span></span>
* <span data-ttu-id="71536-1023">Logiken för inläsning av Azure.Core flyttades till Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="71536-1023">Moved the logic of loading Azure.Core to Az.Accounts</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="71536-1024">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="71536-1024">Az.Websites</span></span>
* <span data-ttu-id="71536-1025">Skydd för att ta bort skapad webapp om återställningen misslyckades har lagts till i ”Restore-AzDeletedWebApp”</span><span class="sxs-lookup"><span data-stu-id="71536-1025">Added safeguard to delete created webapp if restore failed in 'Restore-AzDeletedWebApp'</span></span>
* <span data-ttu-id="71536-1026">”SourceWebApp.Location” har lagts till för ”New-AzWebApp” och ”New-AzWebAppSlot”</span><span class="sxs-lookup"><span data-stu-id="71536-1026">Added 'SourceWebApp.Location' for 'New-AzWebApp' and 'New-AzWebAppSlot'</span></span>
* <span data-ttu-id="71536-1027">Fel som förhindrade ändring av containerinställningar i ”Set-AzWebApp” och ”Set-AzWebAppSlot” har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="71536-1027">Fixed bug that prevented changing Container settings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>
* <span data-ttu-id="71536-1028">Ett fel för att hämta SiteConfig när -Name inte anges för Get-AzWebApp har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="71536-1028">Fixed bug to get SiteConfig when -Name is not given for Get-AzWebApp</span></span>
* <span data-ttu-id="71536-1029">Stöd har lagts till för att skapa ASP för Linux-appar</span><span class="sxs-lookup"><span data-stu-id="71536-1029">Added a support to create ASP for Linux Apps</span></span>
* <span data-ttu-id="71536-1030">Undantag har lagts till för kloning över resursgrupper</span><span class="sxs-lookup"><span data-stu-id="71536-1030">Added exceptions for clone across resource groups</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="71536-1031">4.2.0 – juni 2020</span><span class="sxs-lookup"><span data-stu-id="71536-1031">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="71536-1032">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="71536-1032">Az.Accounts</span></span>
* <span data-ttu-id="71536-1033">Åtgärdade ett problem som kan få Az att hoppa över loggar i Azure Automation- eller PowerShell-jobb [#11492]</span><span class="sxs-lookup"><span data-stu-id="71536-1033">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="71536-1034">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="71536-1034">Az.AnalysisServices</span></span>
* <span data-ttu-id="71536-1035">Uppdaterad sammansättningsversion för dataplan-cmdletar</span><span class="sxs-lookup"><span data-stu-id="71536-1035">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="71536-1036">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="71536-1036">Az.ApiManagement</span></span>
* <span data-ttu-id="71536-1037">Uppdaterad sammansättningsversion för cmdletar för tjänsthantering</span><span class="sxs-lookup"><span data-stu-id="71536-1037">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="71536-1038">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="71536-1038">Az.Billing</span></span>
* <span data-ttu-id="71536-1039">Uppdaterad sammansättningsversion för förbrukningscmdletar</span><span class="sxs-lookup"><span data-stu-id="71536-1039">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="71536-1040">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="71536-1040">Az.CognitiveServices</span></span>
* <span data-ttu-id="71536-1041">Stöd för PrivateEndpoint- och PublicNetworkAccess-kontroll.</span><span class="sxs-lookup"><span data-stu-id="71536-1041">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="71536-1042">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="71536-1042">Az.DataFactory</span></span>
* <span data-ttu-id="71536-1043">Uppdaterad sammansättningsversion för datafabrik V2-cmdletar</span><span class="sxs-lookup"><span data-stu-id="71536-1043">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="71536-1044">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="71536-1044">Az.DataShare</span></span>
* <span data-ttu-id="71536-1045">Allmän tillgänglighet för modulen ”Az.DataShare”</span><span class="sxs-lookup"><span data-stu-id="71536-1045">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="71536-1046">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="71536-1046">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="71536-1047">Allmän tillgänglighet för modulen ”Az.DesktopVirtualization”</span><span class="sxs-lookup"><span data-stu-id="71536-1047">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="71536-1048">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="71536-1048">Az.OperationalInsights</span></span>
* <span data-ttu-id="71536-1049">Uppgraderad SDK till 0.21.0</span><span class="sxs-lookup"><span data-stu-id="71536-1049">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="71536-1050">Lade till valfria parametrar till</span><span class="sxs-lookup"><span data-stu-id="71536-1050">Added optional parameters to</span></span> 
    - <span data-ttu-id="71536-1051">”New-AzOperationalInsightsSavedSearch”</span><span class="sxs-lookup"><span data-stu-id="71536-1051">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="71536-1052">”Set-AzOperationalInsightsSavedSearch”</span><span class="sxs-lookup"><span data-stu-id="71536-1052">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="71536-1053">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="71536-1053">Az.PolicyInsights</span></span>
* <span data-ttu-id="71536-1054">Korrigerade exempel 3 för ”Start-AzPolicyComplianceScan”</span><span class="sxs-lookup"><span data-stu-id="71536-1054">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="71536-1055">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="71536-1055">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="71536-1056">Uppdaterad sammansättningsversion för PowerBI-cmdletar</span><span class="sxs-lookup"><span data-stu-id="71536-1056">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="71536-1057">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="71536-1057">Az.PrivateDns</span></span>
* <span data-ttu-id="71536-1058">Korrigerade formatering av utförlig utdatasträng för Remove-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="71536-1058">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="71536-1059">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="71536-1059">Az.RecoveryServices</span></span>
* <span data-ttu-id="71536-1060">Azure Site Recovery-stöd för att skapa en återställningsplan för replikering mellan zoner från xml-indata.</span><span class="sxs-lookup"><span data-stu-id="71536-1060">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="71536-1061">Uppdaterad sammansättningsversion för cmdletar för SiteRecovery och Backup</span><span class="sxs-lookup"><span data-stu-id="71536-1061">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="71536-1062">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71536-1062">Az.Resources</span></span>
* <span data-ttu-id="71536-1063">Lade till slutparameter för cmdletarna Get-AzDeploymentScriptLog och Save-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="71536-1063">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="71536-1064">Formaterad utdataegenskap så att den kan visas i cmdlet-utdata för Get-AzDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="71536-1064">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="71536-1065">Bytte namn på parametern -DeploymentScriptInputObject till -DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="71536-1065">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="71536-1066">Åtgärdade saknade fil/målnamn i cmdlet-meddelanden.</span><span class="sxs-lookup"><span data-stu-id="71536-1066">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="71536-1067">Uppdaterad sammansättningsversion för cmdletar för resurshanterare och taggar</span><span class="sxs-lookup"><span data-stu-id="71536-1067">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="71536-1068">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71536-1068">Az.Sql</span></span>
* <span data-ttu-id="71536-1069">Lade till UsePrivateLinkConnection till ”New-AzSqlSyncGroup”, ”Update-AzSqlSyncGroup”, ”New-AzSqlSyncMember” och ”Update-AzSqlSyncMember”</span><span class="sxs-lookup"><span data-stu-id="71536-1069">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="71536-1070">Lade till SyncMemberAzureDatabaseResourceId till ”New-AzSqlSyncMember” and ”Update-AzSqlSyncMember”</span><span class="sxs-lookup"><span data-stu-id="71536-1070">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="71536-1071">Lade till stöd för att söka efter gästanvändare för att ange administratörs-cmdlet för SQL Server Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="71536-1071">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="71536-1072">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="71536-1072">Az.Storage</span></span>
* <span data-ttu-id="71536-1073">Uppdaterad sammansättningsversion för dataplan-cmdletar</span><span class="sxs-lookup"><span data-stu-id="71536-1073">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="71536-1074">4.1.0 – maj 2020</span><span class="sxs-lookup"><span data-stu-id="71536-1074">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="71536-1075">Höjdpunkter sedan den senaste uppdateringen</span><span class="sxs-lookup"><span data-stu-id="71536-1075">Highlights since the last release</span></span>
* <span data-ttu-id="71536-1076">PowerShell-versioner som stöds: Windows PowerShell 5.1, PowerShell Core 6.2.4+ och PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="71536-1076">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="71536-1077">Allmän tillgänglighet för Az.Functions</span><span class="sxs-lookup"><span data-stu-id="71536-1077">General availability of Az.Functions</span></span> 
* <span data-ttu-id="71536-1078">Nya stora uppdateringar har gjorts för Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources och Az.Storage</span><span class="sxs-lookup"><span data-stu-id="71536-1078">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="71536-1079">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="71536-1079">Az.Accounts</span></span>
* <span data-ttu-id="71536-1080">”Add-AzEnvironment” och ”Set-AzEnvironment” har uppdaterats med stöd för parametrarna ”AzureSynapseAnalyticsEndpointResourceId” och ”AzureSynapseAnalyticsEndpointSuffix”</span><span class="sxs-lookup"><span data-stu-id="71536-1080">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="71536-1081">Azure.Core-relaterade sammansättningar har lagts till i Az.Accounts; PowerShell-plattformar som stöds är Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span><span class="sxs-lookup"><span data-stu-id="71536-1081">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="71536-1082">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="71536-1082">Az.Aks</span></span>
* <span data-ttu-id="71536-1083">API-versionen har uppgraderats till 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="71536-1083">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="71536-1084">Stöds för att skapa AKS med hjälp av Windows-container</span><span class="sxs-lookup"><span data-stu-id="71536-1084">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="71536-1085">Nya cmdletar är tillgängliga: ”New-AzAksNodePool”, ”Update-AzAksNodePool”, ”Remove-AzAksNodePool”,        ”Get-AzAksNodePool”, ”Install-AzAksKubectl”, ”Get-AzAksVersion”</span><span class="sxs-lookup"><span data-stu-id="71536-1085">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="71536-1086">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="71536-1086">Az.ApiManagement</span></span>
* <span data-ttu-id="71536-1087">Parametrarna ”New-AzApiManagement” och ”Set-AzApiManagement”: [-AssignIdentity] har bytt namn till [-SystemAssignedIdentity]</span><span class="sxs-lookup"><span data-stu-id="71536-1087">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="71536-1088">”New-AzApiManagement” och ”Set-AzApiManagement”: En ny parameter har lagts till: [-UserAssignedIdentity <String[]>]</span><span class="sxs-lookup"><span data-stu-id="71536-1088">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="71536-1089">”Get-AzApiManagementProperty” har bytt namn till ”Get-AzApiManagementNamedValue”.</span><span class="sxs-lookup"><span data-stu-id="71536-1089">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="71536-1090">PropertyId-parametern har bytt namn till NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="71536-1090">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="71536-1091">”New-AzApiManagementProperty” har bytt namn till ”New-AzApiManagementNamedValue”.</span><span class="sxs-lookup"><span data-stu-id="71536-1091">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="71536-1092">PropertyId-parametern har bytt namn till NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="71536-1092">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="71536-1093">”Set-AzApiManagementProperty” har bytt namn till ”Set-AzApiManagementNamedValue”.</span><span class="sxs-lookup"><span data-stu-id="71536-1093">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="71536-1094">PropertyId-parametern har bytt namn till NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="71536-1094">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="71536-1095">”Remove-AzApiManagementProperty” har bytt namn till ”Remove-AzApiManagementNamedValue”.</span><span class="sxs-lookup"><span data-stu-id="71536-1095">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="71536-1096">PropertyId-parametern har bytt namn till NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="71536-1096">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="71536-1097">Den nya cmdleten Get-AzApiManagementAuthorizationServerClientSecret gör att ”Get-AzApiManagementAuthorizationServer” inte längre returnerar klienthemligheter.</span><span class="sxs-lookup"><span data-stu-id="71536-1097">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="71536-1098">Den nya cmdleten ”Get-AzApiManagementNamedValueSecretValue” gör att ”Get-AzApiManagementNamedValue” inte returnerar värdet för en hemlighet.</span><span class="sxs-lookup"><span data-stu-id="71536-1098">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="71536-1099">Den nya cmdleten ”Get-AzApiManagementOpenIdConnectProviderClientSecret” gör att ”Get-AzApiManagementOpenIdConnectProvider” inte längre returnerar klienthemligheter.</span><span class="sxs-lookup"><span data-stu-id="71536-1099">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="71536-1100">Den nya cmdleten ”Get-AzApiManagementSubscriptionKey” gör att ”Get-AzApiManagementSubscription” inte längre returnerar prenumerationsnycklar.</span><span class="sxs-lookup"><span data-stu-id="71536-1100">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="71536-1101">Den nya cmdleten ”Get-AzApiManagementTenantAccessSecret” gör att ”Get-AzApiManagementTenantAccess” inte längre returnerar nycklar.</span><span class="sxs-lookup"><span data-stu-id="71536-1101">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="71536-1102">Den nya cmdleten ”Get-AzApiManagementTenantGitAccessSecret” gör att ”Get-AzApiManagementTenantGitAccess” inte längre returnerar nycklar.</span><span class="sxs-lookup"><span data-stu-id="71536-1102">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="71536-1103">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="71536-1103">Az.ApplicationInsights</span></span>
* <span data-ttu-id="71536-1104">Tillagda parametrar: ”RetentionInDays” ”PublicNetworkAccessForIngestion” ”PublicNetworkAccessForQuery” för ”New-AzApplicationInsights”</span><span class="sxs-lookup"><span data-stu-id="71536-1104">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="71536-1105">Cmdleten ”Update-AzApplicationInsights” har skapats</span><span class="sxs-lookup"><span data-stu-id="71536-1105">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="71536-1106">Cmdletar har skapats för länkat lagringskonto</span><span class="sxs-lookup"><span data-stu-id="71536-1106">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="71536-1107">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="71536-1107">Az.Batch</span></span>
* <span data-ttu-id="71536-1108">Az.Batch har uppdaterats att använda ”Microsoft.Azure.Batch” SDK version 13.0.0 och ”Microsoft.Azure.Management.Batch” SDK version 9.0.0.</span><span class="sxs-lookup"><span data-stu-id="71536-1108">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="71536-1109">Nu kan du välja vilken typ av certifikat du lägger till genom att använda den nya parametern ”-CertificateKind” med ”New-AzBatchCertificate”.</span><span class="sxs-lookup"><span data-stu-id="71536-1109">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="71536-1110">Egenskapen ”ApplicationPackages” har tagits bort från ”PSApplication”, som tidigare alltid var ''.</span><span class="sxs-lookup"><span data-stu-id="71536-1110">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="71536-1111">Specifika paket i ett program kan nu hämtas med hjälp av ”Get-AzBatchApplicationPackage”.</span><span class="sxs-lookup"><span data-stu-id="71536-1111">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="71536-1112">Ett exempel: ”Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication”.</span><span class="sxs-lookup"><span data-stu-id="71536-1112">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="71536-1113">Nu när du skapar en pool med hjälp av ”New-AzBatchPool” kan egenskapen ”VirtualMachineImageId” för ”PSImageReference” endast referera till en Shared Image Gallery-avbildning.</span><span class="sxs-lookup"><span data-stu-id="71536-1113">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="71536-1114">När du skapar en pool med hjälp av ”New-AzBatchPool” kan poolen etableras utan en offentlig IP-adress med hjälp av den nya egenskapen ”PublicIPAddressConfiguration” för ”PSNetworkConfiguration”.</span><span class="sxs-lookup"><span data-stu-id="71536-1114">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="71536-1115">Egenskapen ”PublicIPs” för ”PSNetworkConfiguration” har också flyttats till ”PSPublicIPAddressConfiguration”.</span><span class="sxs-lookup"><span data-stu-id="71536-1115">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="71536-1116">Den här egenskapen kan bara anges om ”IPAddressProvisioningType” är ”UserManaged”.</span><span class="sxs-lookup"><span data-stu-id="71536-1116">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71536-1117">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71536-1117">Az.Compute</span></span>
* <span data-ttu-id="71536-1118">Parametern HostId har lagts till för cmdleten ”Update-AzVM”t</span><span class="sxs-lookup"><span data-stu-id="71536-1118">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="71536-1119">Hjälpdokumenten har uppdaterats för cmdletarna ”New-AzVMConfig”, ”New-AzVmssConfig”, ”Update-AzVmss”, ”Set-AzVMOperatingSystem” och ”Set-AzVmssOsProfile”.</span><span class="sxs-lookup"><span data-stu-id="71536-1119">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="71536-1120">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="71536-1120">Breaking changes</span></span>
    - <span data-ttu-id="71536-1121">Parametern FilterExpression tas bort från cmdleten ”Get-AzVMImage”.</span><span class="sxs-lookup"><span data-stu-id="71536-1121">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="71536-1122">Parametern AssignIdentity tas bort från cmdletarna ”New-AzVmssConfig”, ”New-AzVMConfig” och ”Update-AzVM”.</span><span class="sxs-lookup"><span data-stu-id="71536-1122">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="71536-1123">AutomaticRepairMaxInstanceRepairsPercent tas bort från cmdletarna ”New-AzVmssConfig” och ”Update-AzVmss”.</span><span class="sxs-lookup"><span data-stu-id="71536-1123">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="71536-1124">Egenskaperna AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus och VirtualMachineScaleSetsColocationStatus tas bort från ProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="71536-1124">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="71536-1125">Egenskapen MaxInstanceRepairsPercent tas bort från AutomaticRepairsPolicy.</span><span class="sxs-lookup"><span data-stu-id="71536-1125">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="71536-1126">Typerna AvailabilitySets, VirtualMachines och VirtualMachineScaleSets ändras från IList<SubResource> till IList<SubResourceWithColocationStatus>.</span><span class="sxs-lookup"><span data-stu-id="71536-1126">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="71536-1127">Beskrivningen för cmdleten ”Get-AzVM” har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="71536-1127">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="71536-1128">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="71536-1128">Az.DataFactory</span></span>
* <span data-ttu-id="71536-1129">CRUD-stöd för egenskaper för dataflödeskörning  i hanterad IR.</span><span class="sxs-lookup"><span data-stu-id="71536-1129">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="71536-1130">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="71536-1130">Az.FrontDoor</span></span>
* <span data-ttu-id="71536-1131">Nya cmdletar har lagts till för att skapa, uppdatera, hämta och ta bort (CRUD) Front Door-regelmotorobjekt</span><span class="sxs-lookup"><span data-stu-id="71536-1131">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="71536-1132">Hjälp-cmdletar har lagts till för konstruktion av Front Door-regelmotorobjekt</span><span class="sxs-lookup"><span data-stu-id="71536-1132">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="71536-1133">Regelmotorreferens har lagts till för Front Door-hanteringsregelobjekt.</span><span class="sxs-lookup"><span data-stu-id="71536-1133">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="71536-1134">Parametrar för Private Link har lagts till för Front Door-serverdelsobjekt</span><span class="sxs-lookup"><span data-stu-id="71536-1134">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="71536-1135">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="71536-1135">Az.Functions</span></span>
* <span data-ttu-id="71536-1136">Allmän tillgänglighet för ”Az.Functions”-modulen</span><span class="sxs-lookup"><span data-stu-id="71536-1136">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="71536-1137">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="71536-1137">Az.HDInsight</span></span>
* <span data-ttu-id="71536-1138">Stöd för diskkryptering med kundhanterad nyckel.</span><span class="sxs-lookup"><span data-stu-id="71536-1138">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="71536-1139">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="71536-1139">Az.HealthcareApis</span></span>
* <span data-ttu-id="71536-1140">Åtkomstprinciper använder inte längre det aktiva huvudkontot som standard</span><span class="sxs-lookup"><span data-stu-id="71536-1140">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="71536-1141">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="71536-1141">Az.IotHub</span></span>
* <span data-ttu-id="71536-1142">En cmdlet har lagts till som anropar en fråga i en IoT-hubb för att hämta information med ett SQL-liknande språk.</span><span class="sxs-lookup"><span data-stu-id="71536-1142">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="71536-1143">Problemet som gjorde att ”Add-AzIotHubDevice” inte skapade en Edge-aktiverad enhet utan underordnade enheter har åtgärdats [#11597]</span><span class="sxs-lookup"><span data-stu-id="71536-1143">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="71536-1144">En cmdlet har lagts till för att generera SAS-token för en Iot-hubb, enhet eller modul.</span><span class="sxs-lookup"><span data-stu-id="71536-1144">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="71536-1145">En cmdlet har lagts till för att anropa en måttfråga om konfiguration.</span><span class="sxs-lookup"><span data-stu-id="71536-1145">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="71536-1146">Hantera automatisk distribution av IoT Edge i stor skala.</span><span class="sxs-lookup"><span data-stu-id="71536-1146">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="71536-1147">Nya cmdlet:ar är:</span><span class="sxs-lookup"><span data-stu-id="71536-1147">New cmdlets are:</span></span>
    - <span data-ttu-id="71536-1148">”Add-AzIotHubDeployment”</span><span class="sxs-lookup"><span data-stu-id="71536-1148">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="71536-1149">”Get-AzIotHubDeployment”</span><span class="sxs-lookup"><span data-stu-id="71536-1149">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="71536-1150">”Remove-AzIotHubDeployment”</span><span class="sxs-lookup"><span data-stu-id="71536-1150">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="71536-1151">”Set-AzIotHubDeployment”</span><span class="sxs-lookup"><span data-stu-id="71536-1151">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="71536-1152">En cmdlet har lagts till för att anropa en måttfråga om IoT Edge-distribution.</span><span class="sxs-lookup"><span data-stu-id="71536-1152">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="71536-1153">En cmdlet har lagts till för att tillämpa konfigurationsinnehåll på den angivna gränsenheten.</span><span class="sxs-lookup"><span data-stu-id="71536-1153">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="71536-1154">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="71536-1154">Az.KeyVault</span></span>
* <span data-ttu-id="71536-1155">Två alias har tagits bort: ”New-AzKeyVaultCertificateAdministratorDetails” och ”New-AzKeyVaultCertificateOrganizationDetails”</span><span class="sxs-lookup"><span data-stu-id="71536-1155">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="71536-1156">Nu är mjuk borttagning aktiverat som standard när ett nyckelvalv skapas</span><span class="sxs-lookup"><span data-stu-id="71536-1156">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="71536-1157">Nätverksregler kan ställas in för att styra åtkomsten från särskilda nätverksplatser när du skapar ett nyckelvalv</span><span class="sxs-lookup"><span data-stu-id="71536-1157">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="71536-1158">Stöd för BYOK (Bring Your Own Key) har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-1158">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="71536-1159">”Add-AzKeyVaultKey” stöder generering av en KeyExchange-nyckel</span><span class="sxs-lookup"><span data-stu-id="71536-1159">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="71536-1160">”Get-AzKeyVaultKey” stöder nedladdning av en offentlig nyckel i PEM-format</span><span class="sxs-lookup"><span data-stu-id="71536-1160">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="71536-1161">”KeyOps”-delen av hjälpdokumentet för ”Add-AzKeyVaultKey” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="71536-1161">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="71536-1162">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="71536-1162">Az.Monitor</span></span>
* <span data-ttu-id="71536-1163">Bugg för ”Set-AzDiagnosticSettings” har åtgärdats; kvarhållningsprincipen tillämpas inte på alla kategorier [#11589]</span><span class="sxs-lookup"><span data-stu-id="71536-1163">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="71536-1164">Stöd för WebTest-tillgänglighetskriterier för måttavisering V2</span><span class="sxs-lookup"><span data-stu-id="71536-1164">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="71536-1165">”New-AzMetricAlertRuleV2Criteria”: ett alternativ för att skapa tillgänglighetskriterier för webbtest har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-1165">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="71536-1166">”Add-AzMetricAlertRuleV2”: stöd för de nya tillgänglighetskriterierna för webbtest</span><span class="sxs-lookup"><span data-stu-id="71536-1166">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="71536-1167">Redundant definition har tagits bort för RetentionPolicy i PSLogProfile [#7608]</span><span class="sxs-lookup"><span data-stu-id="71536-1167">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="71536-1168">Redundanta egenskaper som definierats i PSEventData har tagits bort [#11353]</span><span class="sxs-lookup"><span data-stu-id="71536-1168">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="71536-1169">”Get-AzLog” har bytt namn till ”Get-AzActivityLog”</span><span class="sxs-lookup"><span data-stu-id="71536-1169">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71536-1170">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71536-1170">Az.Network</span></span>
* <span data-ttu-id="71536-1171">Attribut för icke-bakåtkompatibel ändring har lagts till för att meddela att standardbeteendet för zoner kommer att ändras</span><span class="sxs-lookup"><span data-stu-id="71536-1171">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="71536-1172">”New-AzPublicIpAddress”</span><span class="sxs-lookup"><span data-stu-id="71536-1172">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="71536-1173">”New-AzPublicIpPrefix”</span><span class="sxs-lookup"><span data-stu-id="71536-1173">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="71536-1174">”New-AzLoadBalancerFrontendIpConfig”</span><span class="sxs-lookup"><span data-stu-id="71536-1174">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="71536-1175">Stöd har lagts till för en ny resurs på den översta nivån, SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="71536-1175">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="71536-1176">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="71536-1176">New cmdlets added:</span></span>
        - <span data-ttu-id="71536-1177">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="71536-1177">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="71536-1178">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="71536-1178">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="71536-1179">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="71536-1179">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="71536-1180">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="71536-1180">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="71536-1181">”RequiredZoneNames” har lagts till för ”PSPrivateLinkResource” och ”GroupId” för ”PSPrivateEndpointConnection”</span><span class="sxs-lookup"><span data-stu-id="71536-1181">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="71536-1182">Fel parametertyp för SuccessThresholdRoundTripTimeMs-parametern för New-AzNetworkWatcherConnectionMonitorTestConfigurationObject har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="71536-1182">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="71536-1183">VirtualWan-cmdletar har uppdaterats för att ange AllowVnetToVnetTraffic-argumentets standardvärde till True.</span><span class="sxs-lookup"><span data-stu-id="71536-1183">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="71536-1184">”New-AzVirtualWan”</span><span class="sxs-lookup"><span data-stu-id="71536-1184">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="71536-1185">”Update-AzVirtualWan”</span><span class="sxs-lookup"><span data-stu-id="71536-1185">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="71536-1186">Nya cmdletar har lagts till för att stödja DNS-zongrupp för privat slutpunkt</span><span class="sxs-lookup"><span data-stu-id="71536-1186">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="71536-1187">”New-AzPrivateDnsZoneConfig”</span><span class="sxs-lookup"><span data-stu-id="71536-1187">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="71536-1188">”Get-AzPrivateDnsZoneGroup”</span><span class="sxs-lookup"><span data-stu-id="71536-1188">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="71536-1189">”New-AzPrivateDnsZoneGroup”</span><span class="sxs-lookup"><span data-stu-id="71536-1189">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="71536-1190">”Set-AzPrivateDnsZoneGroup”</span><span class="sxs-lookup"><span data-stu-id="71536-1190">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="71536-1191">”Remove-AzPrivateDnsZoneGroup”</span><span class="sxs-lookup"><span data-stu-id="71536-1191">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="71536-1192">Parametrarna ”DNSEnableProxy”, ”DNSRequireProxyForNetworkRules” och ”DNSServers” har lagts till för ”AzureFirewall”</span><span class="sxs-lookup"><span data-stu-id="71536-1192">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="71536-1193">Parametrarna ”EnableDnsProxy”, ”DnsProxyNotRequiredForNetworkRule” och ”DnsServer” har lagts till för ”AzureFirewall”</span><span class="sxs-lookup"><span data-stu-id="71536-1193">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="71536-1194">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="71536-1194">Updated cmdlet:</span></span>
        - <span data-ttu-id="71536-1195">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="71536-1195">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="71536-1196">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="71536-1196">Az.OperationalInsights</span></span>
* <span data-ttu-id="71536-1197">Äldre kod har uppdaterats för att tillämpa ny genererad SDK</span><span class="sxs-lookup"><span data-stu-id="71536-1197">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="71536-1198">Cmdletar har tagits bort på grund av föråldrade API:er</span><span class="sxs-lookup"><span data-stu-id="71536-1198">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="71536-1199">”Get-AzOperationalInsightsSavedSearchResult” (alias ”Get-AzOperationalInsightsSavedSearchResults”)</span><span class="sxs-lookup"><span data-stu-id="71536-1199">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="71536-1200">”Get-AzOperationalInsightsSearchResult” (alias ”Get-AzOperationalInsightsSearchResults”)</span><span class="sxs-lookup"><span data-stu-id="71536-1200">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="71536-1201">”Get-AzOperationalInsightsLinkTarget” (alias ”Get-AzOperationalInsightsLinkTargets”)</span><span class="sxs-lookup"><span data-stu-id="71536-1201">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="71536-1202">Parametrar har lagts till för ”Set-AzOperationalInsightsWorkspace” och ”New-AzOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="71536-1202">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="71536-1203">Cmdletar har skapats för länkat lagringskonto</span><span class="sxs-lookup"><span data-stu-id="71536-1203">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="71536-1204">Cmdletar har skapats för kluster och länkad tjänst</span><span class="sxs-lookup"><span data-stu-id="71536-1204">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="71536-1205">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="71536-1205">Az.RecoveryServices</span></span>
* <span data-ttu-id="71536-1206">Azure Site Recovery: Stöd har lagts till för att skydda VM-närhetsplaceringsgrupper för Azure till Azure-provider.</span><span class="sxs-lookup"><span data-stu-id="71536-1206">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="71536-1207">Azure Site Recovery: Stöd har lagts till för replikering mellan zoner.</span><span class="sxs-lookup"><span data-stu-id="71536-1207">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="71536-1208">Azure Backup: Stöd har lagts till för långsiktig kvarhållning för Azure FileShare-återställningspunkter.</span><span class="sxs-lookup"><span data-stu-id="71536-1208">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="71536-1209">Azure Backup: Egenskaper för diskexkludering har lagts till för cmdlet-utdata från ”Get-AzRecoveryServicesBackupItem”.</span><span class="sxs-lookup"><span data-stu-id="71536-1209">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="71536-1210">En privat slutpunkt har lagts till för filen med valvets autentiseringsuppgifter för Site Recovery-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="71536-1210">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="71536-1211">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71536-1211">Az.Resources</span></span>
* <span data-ttu-id="71536-1212">En varning har lagts till om visningsfördröjning när en ny rolldefinition skapas</span><span class="sxs-lookup"><span data-stu-id="71536-1212">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="71536-1213">Princip-cmdletar har ändrats för utmatning av starkt typifierade objekt</span><span class="sxs-lookup"><span data-stu-id="71536-1213">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="71536-1214">Parametern ”-TenantLevel” har tagits bort för användning med ”Get-AzResourceLock” [#11335]</span><span class="sxs-lookup"><span data-stu-id="71536-1214">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="71536-1215">”Remove-AzResourceGroup -Id ResourceId” har åtgärdats [#9882]</span><span class="sxs-lookup"><span data-stu-id="71536-1215">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="71536-1216">En ny cmdlet har lagts till för att hämta What-If-resultat för ARM-mallar i omfånget för resursgrupper: ”Get-AzDeploymentResourceGroupWhatIfResult”</span><span class="sxs-lookup"><span data-stu-id="71536-1216">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="71536-1217">En ny cmdlet har lagts till för att hämta What-If-resultat för ARM-mallar i prenumerationsomfånget: ”Get-AzDeploymentWhatIfResult”</span><span class="sxs-lookup"><span data-stu-id="71536-1217">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="71536-1218">Alias: ”Get-AzSubscriptionDeploymentWhatIf”</span><span class="sxs-lookup"><span data-stu-id="71536-1218">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="71536-1219">Parametrarna ”-WhatIf” och ”-Confirm” har åsidosatts för ”New-AzDeployment” och ”New-AzResourceGroupDeployment” för att använda What-If-resultat för ARM-mallar</span><span class="sxs-lookup"><span data-stu-id="71536-1219">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="71536-1220">Ett utfasningsmeddelande har lagts till för parametern ”ApiVersion” i distributions-cmdletar</span><span class="sxs-lookup"><span data-stu-id="71536-1220">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="71536-1221">En funktion har lagts till för att visa förbättrade felmeddelanden för distributionsfel</span><span class="sxs-lookup"><span data-stu-id="71536-1221">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="71536-1222">CorrelationId-loggning har lagts till för distributionsfel</span><span class="sxs-lookup"><span data-stu-id="71536-1222">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="71536-1223">Egenskapen ”error” har lagts till i utdata från distributionsskript</span><span class="sxs-lookup"><span data-stu-id="71536-1223">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="71536-1224">Nuget Microsoft.Azure.Management.ResourceManager har uppdaterats till ”3.7.1-preview”</span><span class="sxs-lookup"><span data-stu-id="71536-1224">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="71536-1225">Specifika testfall har tagits bort då egenskapen Error i DeploymentValidateResult har ändrats till lässkyddad från nuget 3.7.1-preview</span><span class="sxs-lookup"><span data-stu-id="71536-1225">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="71536-1226">GenericResourceExpanded har flyttats från SDK ResourceManager 3.7.1-preview</span><span class="sxs-lookup"><span data-stu-id="71536-1226">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="71536-1227">Stöd för taggar har lagts till för alla Get-cmdletar för distribution, samt</span><span class="sxs-lookup"><span data-stu-id="71536-1227">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="71536-1228">”New-AzDeployment”</span><span class="sxs-lookup"><span data-stu-id="71536-1228">'New-AzDeployment'</span></span>
    - <span data-ttu-id="71536-1229">”New-AzManagementGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="71536-1229">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="71536-1230">”New-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="71536-1230">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="71536-1231">”New-AzTenantDeployment”</span><span class="sxs-lookup"><span data-stu-id="71536-1231">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="71536-1232">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="71536-1232">Az.ServiceFabric</span></span>
* <span data-ttu-id="71536-1233">En bugg har åtgärdats som gjorde att --SecretIdentifier fick fel tumavtryck för certifikat när ett certifikat lades till</span><span class="sxs-lookup"><span data-stu-id="71536-1233">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="71536-1234">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71536-1234">Az.Sql</span></span>
* <span data-ttu-id="71536-1235">Förbättrade prestanda för:</span><span class="sxs-lookup"><span data-stu-id="71536-1235">Enhance performance of:</span></span>
    - <span data-ttu-id="71536-1236">”Set-AzSqlDatabaseSensitivityClassification”</span><span class="sxs-lookup"><span data-stu-id="71536-1236">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="71536-1237">”Set-AzSqlInstanceDatabaseSensitivityClassification”</span><span class="sxs-lookup"><span data-stu-id="71536-1237">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="71536-1238">”Remove-AzSqlDatabaseSensitivityClassification”</span><span class="sxs-lookup"><span data-stu-id="71536-1238">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="71536-1239">”Remove-AzSqlInstanceDatabaseSensitivityClassification”</span><span class="sxs-lookup"><span data-stu-id="71536-1239">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="71536-1240">”Enable-AzSqlDatabaseSensitivityRecommendation”</span><span class="sxs-lookup"><span data-stu-id="71536-1240">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="71536-1241">”Enable-AzSqlInstanceDatabaseSensitivityRecommendation”</span><span class="sxs-lookup"><span data-stu-id="71536-1241">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="71536-1242">”Disable-AzSqlDatabaseSensitivityRecommendation”</span><span class="sxs-lookup"><span data-stu-id="71536-1242">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="71536-1243">”Disable-AzSqlInstanceDatabaseSensitivityRecommendation”</span><span class="sxs-lookup"><span data-stu-id="71536-1243">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="71536-1244">Validering på klientsidan har tagits bort för parametern ”RetentionDays” från cmdleten ”Set-AzSqlDatabaseBackupShortTermRetentionPolicy”</span><span class="sxs-lookup"><span data-stu-id="71536-1244">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="71536-1245">Granskning av ett lagringskonto i Vnet; en bugg har åtgärdats som orsakade fel när en Storage Blob Data-deltagarroll skapades.</span><span class="sxs-lookup"><span data-stu-id="71536-1245">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="71536-1246">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="71536-1246">Az.Storage</span></span>
* <span data-ttu-id="71536-1247">”-AsJob” har lagts till för att hämta/lista konto med cmdleten ”Get-AzStorageAccount”</span><span class="sxs-lookup"><span data-stu-id="71536-1247">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="71536-1248">Gör KeyVersion valfri när lagringskontot uppdateras med KeyvaultEncryption, för att ge stöd för automatisk nyckelrotation</span><span class="sxs-lookup"><span data-stu-id="71536-1248">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="71536-1249">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="71536-1249">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="71536-1250">Problemet med borttagning av Azure-filkatalog i pipeline har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="71536-1250">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="71536-1251">”Remove-AzStorageDirectory”</span><span class="sxs-lookup"><span data-stu-id="71536-1251">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="71536-1252">Åtgärdat [#9880]: Definitionen av DefaultAction-värdet för NetWorkRule har ändrats för konsekvens med Swagger.</span><span class="sxs-lookup"><span data-stu-id="71536-1252">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="71536-1253">”Update-AzStorageAccountNetworkRuleSet”</span><span class="sxs-lookup"><span data-stu-id="71536-1253">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="71536-1254">”Get-AzStorageAccountNetworkRuleSet”</span><span class="sxs-lookup"><span data-stu-id="71536-1254">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="71536-1255">Åtgärdat [#11624]: Hoppa över dubblettregler när NetworkRules läggs till, för att undvika serverfel</span><span class="sxs-lookup"><span data-stu-id="71536-1255">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="71536-1256">”Add-AzStorageAccountNetworkRule”</span><span class="sxs-lookup"><span data-stu-id="71536-1256">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="71536-1257">Microsoft.Azure.Cosmos.Table SDK har uppgraderats till 1.0.7</span><span class="sxs-lookup"><span data-stu-id="71536-1257">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="71536-1258">Ett varningsmeddelande har lagts till för att påminna användaren om att lista igen med ContinuationToken när endast delobjekt returneras i listan med DataLake Gen2-objekt,</span><span class="sxs-lookup"><span data-stu-id="71536-1258">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="71536-1259">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="71536-1259">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="71536-1260">Stöd för att skapa eller uppdatera lagringskonto med Azure Files Active Directory Domain Service-autentisering</span><span class="sxs-lookup"><span data-stu-id="71536-1260">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="71536-1261">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="71536-1261">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="71536-1262">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="71536-1262">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="71536-1263">Stöd för nya eller listade Kerberos-nycklar för lagringskontot</span><span class="sxs-lookup"><span data-stu-id="71536-1263">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="71536-1264">”New-AzStorageAccountKey”</span><span class="sxs-lookup"><span data-stu-id="71536-1264">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="71536-1265">”Get-AzStorageAccountKey”</span><span class="sxs-lookup"><span data-stu-id="71536-1265">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="71536-1266">Stöd för redundans med lagringskonto</span><span class="sxs-lookup"><span data-stu-id="71536-1266">Supported failover Storage account</span></span>
    - <span data-ttu-id="71536-1267">”Invoke-AzStorageAccountFailover”</span><span class="sxs-lookup"><span data-stu-id="71536-1267">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="71536-1268">Hjälpen för ”Get-AzStorageBlobCopyState” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="71536-1268">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="71536-1269">Hjälpen för ”Get-AzStorageFileCopyState” och ”Start-AzStorageBlobCopy” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="71536-1269">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="71536-1270">Lagringsklientbibliotek v12 har integrerats med Queue- och File-cmdletar</span><span class="sxs-lookup"><span data-stu-id="71536-1270">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="71536-1271">Utdatatypen har ändrats från CloudFile till AzureStorageFile; ursprungliga utdata blir en underordnad egenskap i den nya utmatningen</span><span class="sxs-lookup"><span data-stu-id="71536-1271">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="71536-1272">”Get-AzStorageFile”</span><span class="sxs-lookup"><span data-stu-id="71536-1272">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="71536-1273">”Remove-AzStorageFile”</span><span class="sxs-lookup"><span data-stu-id="71536-1273">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="71536-1274">”Get-AzStorageFileContent”</span><span class="sxs-lookup"><span data-stu-id="71536-1274">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="71536-1275">”Set-AzStorageFileContent”</span><span class="sxs-lookup"><span data-stu-id="71536-1275">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="71536-1276">”Start-AzStorageFileCopy”</span><span class="sxs-lookup"><span data-stu-id="71536-1276">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="71536-1277">Utdatatypen har ändrats från CloudFileDirectory till AzureStorageFileDirectory; ursprungliga utdata blir en underordnad egenskap i den nya utmatningen</span><span class="sxs-lookup"><span data-stu-id="71536-1277">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="71536-1278">”New-AzStorageDirectory”</span><span class="sxs-lookup"><span data-stu-id="71536-1278">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="71536-1279">”Remove-AzStorageDirectory”</span><span class="sxs-lookup"><span data-stu-id="71536-1279">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="71536-1280">Utdatatypen har ändrats från CloudFileShare till AzureStorageFileShare; ursprungliga utdata blir en underordnad egenskap i den nya utmatningen</span><span class="sxs-lookup"><span data-stu-id="71536-1280">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="71536-1281">”Get-AzStorageShare”</span><span class="sxs-lookup"><span data-stu-id="71536-1281">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="71536-1282">”New-AzStorageShare”</span><span class="sxs-lookup"><span data-stu-id="71536-1282">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="71536-1283">”Remove-AzStorageShare”</span><span class="sxs-lookup"><span data-stu-id="71536-1283">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="71536-1284">Utdatatypen har ändrats från FileShareProperties till AzureStorageFileShare; ursprungliga utdata blir en underordnad egenskap i den nya utmatningen</span><span class="sxs-lookup"><span data-stu-id="71536-1284">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="71536-1285">”Set-AzStorageShareQuota”</span><span class="sxs-lookup"><span data-stu-id="71536-1285">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="71536-1286">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="71536-1286">Az.TrafficManager</span></span>
* <span data-ttu-id="71536-1287">Felaktigt profilnamn har åtgärdats i utförliga utdata för ”DisableAzureTrafficManagerEndpoint”</span><span class="sxs-lookup"><span data-stu-id="71536-1287">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="71536-1288">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="71536-1288">Az.Websites</span></span>
* <span data-ttu-id="71536-1289">Stavfel har åtgärdats i hjälpen för ”Update-AzWebAppAccessRestrictionConfig”.</span><span class="sxs-lookup"><span data-stu-id="71536-1289">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="71536-1290">3.8.0 – April 2020</span><span class="sxs-lookup"><span data-stu-id="71536-1290">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="71536-1291">Höjdpunkter sedan den senaste uppdateringen</span><span class="sxs-lookup"><span data-stu-id="71536-1291">Highlights since the last release</span></span>
* <span data-ttu-id="71536-1292">PowerShell-versioner som Az.Storage stöder: Windows PowerShell 5.1, PowerShell Core 6.2.4+ och PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="71536-1292">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="71536-1293">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="71536-1293">Az.Accounts</span></span>
* <span data-ttu-id="71536-1294">Uppdaterade URL:en för Azure PowerShell-enkäten i ”Resolve-AzError” [#11507]</span><span class="sxs-lookup"><span data-stu-id="71536-1294">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="71536-1295">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="71536-1295">Az.ApiManagement</span></span>
* <span data-ttu-id="71536-1296">Lade till meddelande om icke-bakåtkompatibel ändring vid ändring i utdata för Azure File-cmdletar i en framtida version</span><span class="sxs-lookup"><span data-stu-id="71536-1296">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="71536-1297">"Set-AzApiManagementGroup" Uppdaterad dokumentation för att ange GroupId-parametern</span><span class="sxs-lookup"><span data-stu-id="71536-1297">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="71536-1298">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="71536-1298">Az.Cdn</span></span>
* <span data-ttu-id="71536-1299">Fast ChinaCDN-relaterad prissättning för SKU-visning</span><span class="sxs-lookup"><span data-stu-id="71536-1299">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="71536-1300">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="71536-1300">Az.CognitiveServices</span></span>
* <span data-ttu-id="71536-1301">Identitet som stöds, kryptering, UserOwnedStorage</span><span class="sxs-lookup"><span data-stu-id="71536-1301">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71536-1302">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71536-1302">Az.Compute</span></span>
* <span data-ttu-id="71536-1303">Cmdleten ”Set-AzVmssOrchestrationServiceState” har lagts till.</span><span class="sxs-lookup"><span data-stu-id="71536-1303">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="71536-1304">”Get-AzVmss” med -InstanceView visar OrchestrationService-tillstånd.</span><span class="sxs-lookup"><span data-stu-id="71536-1304">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="71536-1305">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="71536-1305">Az.IotHub</span></span>
* <span data-ttu-id="71536-1306">Hantera den dubbla konfigurationen för IoT-enheter, nya cmdletar är:</span><span class="sxs-lookup"><span data-stu-id="71536-1306">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="71536-1307">'Get-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="71536-1307">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="71536-1308">'Update-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="71536-1308">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="71536-1309">En cmdlet har lagts till för att anropa direkt metod på en enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="71536-1309">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="71536-1310">Hantera dubbel konfiguration för IoT-enhetsmodul, nya cmdletar är:</span><span class="sxs-lookup"><span data-stu-id="71536-1310">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="71536-1311">'Get-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="71536-1311">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="71536-1312">'Update-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="71536-1312">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="71536-1313">Hantera IoT-automatisk konfiguration av enhetshantering i stor skala.</span><span class="sxs-lookup"><span data-stu-id="71536-1313">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="71536-1314">Nya cmdlet:ar är:</span><span class="sxs-lookup"><span data-stu-id="71536-1314">New cmdlets are:</span></span>
    - <span data-ttu-id="71536-1315">'Add-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="71536-1315">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="71536-1316">'Get-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="71536-1316">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="71536-1317">'Remove-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="71536-1317">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="71536-1318">'Set-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="71536-1318">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="71536-1319">En cmdlet har lagts till för att anropa en edge-modulmetod i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="71536-1319">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="71536-1320">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="71536-1320">Az.KeyVault</span></span>
* <span data-ttu-id="71536-1321">Har lagt till en ny cmdlet, "Update-AzKeyVault", som kan aktivera mjuk borttagning och rensning av skydd i ett valv</span><span class="sxs-lookup"><span data-stu-id="71536-1321">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="71536-1322">Har lagt till stöd i Microsoft.PowerShell.SecretManagement [#11178]</span><span class="sxs-lookup"><span data-stu-id="71536-1322">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="71536-1323">Åtgärdat fel i exemplen i 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span><span class="sxs-lookup"><span data-stu-id="71536-1323">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="71536-1324">Har lagt till stöd för privat slutpunkt</span><span class="sxs-lookup"><span data-stu-id="71536-1324">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="71536-1325">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="71536-1325">Az.Maintenance</span></span>
* <span data-ttu-id="71536-1326">Publicerar slutversion av underhålls-cmdletar för GA</span><span class="sxs-lookup"><span data-stu-id="71536-1326">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="71536-1327">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="71536-1327">Az.Monitor</span></span>
* <span data-ttu-id="71536-1328">Har lagt till cmdletar för privat länkomfång</span><span class="sxs-lookup"><span data-stu-id="71536-1328">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="71536-1329">'Get-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="71536-1329">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="71536-1330">'Remove-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="71536-1330">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="71536-1331">'New-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="71536-1331">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="71536-1332">'Update-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="71536-1332">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="71536-1333">'Get-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="71536-1333">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="71536-1334">'New-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="71536-1334">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="71536-1335">'Remove-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="71536-1335">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71536-1336">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71536-1336">Az.Network</span></span>
* <span data-ttu-id="71536-1337">Uppdaterade cmdletar för att aktivera anslutning på privat IP för Virtual Network Gateway.</span><span class="sxs-lookup"><span data-stu-id="71536-1337">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="71536-1338">'New-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="71536-1338">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="71536-1339">'Set-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="71536-1339">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="71536-1340">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="71536-1340">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="71536-1341">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="71536-1341">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="71536-1342">Uppdaterade cmdletar för att aktivera FQDN-baserade LocalNetworkGateways och VpnSites</span><span class="sxs-lookup"><span data-stu-id="71536-1342">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="71536-1343">'New-AzLocalNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="71536-1343">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="71536-1344">'New-AzVpnSiteLink'</span><span class="sxs-lookup"><span data-stu-id="71536-1344">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="71536-1345">Stöd har lagts till för IPv6-adresstypen i ExpressRouteCircuitConnectionConfig (Global Reach)</span><span class="sxs-lookup"><span data-stu-id="71536-1345">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="71536-1346">Lade till 'Set-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="71536-1346">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="71536-1347">tillåter inställning av alla befintliga egenskaper inklusive IPv6CircuitConnectionProperties</span><span class="sxs-lookup"><span data-stu-id="71536-1347">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="71536-1348">Uppdaterade 'Add-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="71536-1348">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="71536-1349">Lade till en ytterligare valfri parameter, AddressPrefixType, för att specificera adresstypen för adressprefix</span><span class="sxs-lookup"><span data-stu-id="71536-1349">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="71536-1350">Uppdaterade cmdletar för att aktivera inställningen för DPD-timeout på Virtual Network Gateway-anslutningar.</span><span class="sxs-lookup"><span data-stu-id="71536-1350">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="71536-1351">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="71536-1351">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="71536-1352">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="71536-1352">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="71536-1353">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="71536-1353">Az.PolicyInsights</span></span>
* <span data-ttu-id="71536-1354">Cmdleten "Start-AzPolicyComplianceScan" har lagts till för att utlösa genomsökningar av principefterlevnad</span><span class="sxs-lookup"><span data-stu-id="71536-1354">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="71536-1355">Principdefinition, uppsättningsdefinition och tilldelningsversioner har lagts till i "Get-AzPolicyState"-utdata</span><span class="sxs-lookup"><span data-stu-id="71536-1355">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="71536-1356">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="71536-1356">Az.ServiceFabric</span></span>
* <span data-ttu-id="71536-1357">Förbättrad kodformatering och användbarhet för "New-AzServiceFabricCluster"-exempel</span><span class="sxs-lookup"><span data-stu-id="71536-1357">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="71536-1358">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71536-1358">Az.Sql</span></span>
* <span data-ttu-id="71536-1359">Lade till cmdletarna "Get-AzSqlInstanceOperation" och "Stop-AzSqlInstanceOperation"</span><span class="sxs-lookup"><span data-stu-id="71536-1359">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="71536-1360">Stöd för granskning för ett lagringskonto i VNet.</span><span class="sxs-lookup"><span data-stu-id="71536-1360">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="71536-1361">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="71536-1361">Az.Storage</span></span>
* <span data-ttu-id="71536-1362">Lade till meddelande om icke-bakåtkompatibel ändring vid ändring i utdata för Azure File-cmdletar i en framtida version</span><span class="sxs-lookup"><span data-stu-id="71536-1362">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="71536-1363">Stöd för nya SkuName StandardGZRS, StandardRAGZRS när ett lagringskonto skapas/uppdateras</span><span class="sxs-lookup"><span data-stu-id="71536-1363">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="71536-1364">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="71536-1364">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="71536-1365">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="71536-1365">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="71536-1366">Stöd för DataLake Gen2</span><span class="sxs-lookup"><span data-stu-id="71536-1366">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="71536-1367">'New-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="71536-1367">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="71536-1368">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="71536-1368">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="71536-1369">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="71536-1369">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="71536-1370">'Move-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="71536-1370">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="71536-1371">'Set-AzDataLakeGen2ItemAclObject'</span><span class="sxs-lookup"><span data-stu-id="71536-1371">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="71536-1372">'Update-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="71536-1372">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="71536-1373">'Get-AzDataLakeGen2ItemContent'</span><span class="sxs-lookup"><span data-stu-id="71536-1373">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="71536-1374">'Remove-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="71536-1374">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="71536-1375">0.10.0-förhandsversion – April 2020</span><span class="sxs-lookup"><span data-stu-id="71536-1375">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="71536-1376">Allmänt</span><span class="sxs-lookup"><span data-stu-id="71536-1376">General</span></span>
* <span data-ttu-id="71536-1377">Az-moduler är nu tillgängliga i förhandsversion på Azure Stack Hub.</span><span class="sxs-lookup"><span data-stu-id="71536-1377">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="71536-1378">Därmed möjliggörs kompatibilitet för flera plattformar med Linux och macOs.</span><span class="sxs-lookup"><span data-stu-id="71536-1378">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="71536-1379">Azure Stack Hub stöder nu PowerShell Core med AZ-moduler. Mer information finns [här](/azure-stack/operator/powershell-install-az-module)</span><span class="sxs-lookup"><span data-stu-id="71536-1379">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](/azure-stack/operator/powershell-install-az-module)</span></span>
* <span data-ttu-id="71536-1380">Supportprofil för AZ-moduler 2019-03-01-hybrid:</span><span class="sxs-lookup"><span data-stu-id="71536-1380">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="71536-1381">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="71536-1381">Az.Billing</span></span>
  - <span data-ttu-id="71536-1382">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71536-1382">Az.Compute</span></span>
  - <span data-ttu-id="71536-1383">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="71536-1383">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="71536-1384">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="71536-1384">Az.EventHub</span></span>
  - <span data-ttu-id="71536-1385">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="71536-1385">Az.IotHub</span></span>
  - <span data-ttu-id="71536-1386">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="71536-1386">Az.KeyVault</span></span>
  - <span data-ttu-id="71536-1387">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="71536-1387">Az.Monitor</span></span>
  - <span data-ttu-id="71536-1388">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71536-1388">Az.Network</span></span>
  - <span data-ttu-id="71536-1389">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71536-1389">Az.Resources</span></span>
  - <span data-ttu-id="71536-1390">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="71536-1390">Az.Storage</span></span>
  - <span data-ttu-id="71536-1391">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="71536-1391">Az.Websites</span></span>
* <span data-ttu-id="71536-1392">Tre nya PowerShell-moduler för AZ har introducerats som fungerar med Azure Stack Hub, och de är Az.Databox, Az.IotHub och Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="71536-1392">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="71536-1393">Kommandona är i princip oförändrade, med endast mindre ändringar som att AzureRM ändras till AZ</span><span class="sxs-lookup"><span data-stu-id="71536-1393">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="71536-1394">En uppdaterad länk till PowerShell-dokumentationen för Azure Stack Hub finns [här](/azure-stack/operator/powershell-install-az-module)</span><span class="sxs-lookup"><span data-stu-id="71536-1394">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](/azure-stack/operator/powershell-install-az-module)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="71536-1395">3.7.0 – mars 2020</span><span class="sxs-lookup"><span data-stu-id="71536-1395">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="71536-1396">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="71536-1396">Az.Accounts</span></span>
* <span data-ttu-id="71536-1397">Åtgärdade ”Get-AzTenant”/”Get-AzDefault”/”Set-AzDefault”-utlösning av NullReferenceException när du inte är inloggad [#10292]</span><span class="sxs-lookup"><span data-stu-id="71536-1397">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71536-1398">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71536-1398">Az.Compute</span></span>
* <span data-ttu-id="71536-1399">Följande parametrar har lagts till i cmdleten ”New-AzDiskConfig”:</span><span class="sxs-lookup"><span data-stu-id="71536-1399">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="71536-1400">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="71536-1400">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="71536-1401">Tillåten krypteringsegenskap till målparametern för cmdleten ”New-AzGalleryImageVersion”.</span><span class="sxs-lookup"><span data-stu-id="71536-1401">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="71536-1402">Åtgärdade tempDisk-problem för cmdletarna ”Set-AzVmss”-Reimage och ”Invoke-AzVMReimage”.</span><span class="sxs-lookup"><span data-stu-id="71536-1402">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="71536-1403">[#11354]</span><span class="sxs-lookup"><span data-stu-id="71536-1403">[#11354]</span></span>
* <span data-ttu-id="71536-1404">Stöd har lagts till i nedanstående cmdletar för nytt SAP-tillägg</span><span class="sxs-lookup"><span data-stu-id="71536-1404">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="71536-1405">”Set-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="71536-1405">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="71536-1406">”Get-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="71536-1406">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="71536-1407">”Remove-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="71536-1407">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="71536-1408">”Update-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="71536-1408">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="71536-1409">Åtgärdade fel i exempel på hjälpdokument</span><span class="sxs-lookup"><span data-stu-id="71536-1409">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="71536-1410">Visade det exakta strängvärdet för VM PowerState i tabellformat.</span><span class="sxs-lookup"><span data-stu-id="71536-1410">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="71536-1411">”New-AzVmssConfig”: den fasta serialiseringen av egenskapen AutomaticRepairs när SinglePlacementGroup är inaktiverad.</span><span class="sxs-lookup"><span data-stu-id="71536-1411">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="71536-1412">[#11257]</span><span class="sxs-lookup"><span data-stu-id="71536-1412">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="71536-1413">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="71536-1413">Az.DataFactory</span></span>
* <span data-ttu-id="71536-1414">ADF .Net SDK har uppdaterats till 4.8.0</span><span class="sxs-lookup"><span data-stu-id="71536-1414">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="71536-1415">Valfria parametrar har lagts till i kommandot ”Invoke-AzDataFactoryV2Pipeline” för att stödja omkörning</span><span class="sxs-lookup"><span data-stu-id="71536-1415">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="71536-1416">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="71536-1416">Az.DataLakeStore</span></span>
* <span data-ttu-id="71536-1417">Lade till beskrivning för icke-bakåtkompatibel ändring för ”Export-AzDataLakeStoreItem” och ”Import-AzDataLakeStoreItem”</span><span class="sxs-lookup"><span data-stu-id="71536-1417">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="71536-1418">Lade till alternativ för bytekodning för ”New-AzDataLakeStoreItem”, ”Add-AzDAtaLakeStoreItemContent” och ”Get-AzDAtaLakeStoreItemContent”</span><span class="sxs-lookup"><span data-stu-id="71536-1418">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="71536-1419">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="71536-1419">Az.HDInsight</span></span>
* <span data-ttu-id="71536-1420">Stöd för att ange en minimal TLS-version som stöds när klustret skapas.</span><span class="sxs-lookup"><span data-stu-id="71536-1420">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="71536-1421">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="71536-1421">Az.IotHub</span></span>
* <span data-ttu-id="71536-1422">Stöd har lagts till för att hantera distribuerade inställningar per enhet.</span><span class="sxs-lookup"><span data-stu-id="71536-1422">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="71536-1423">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="71536-1423">New Cmdlets are:</span></span>
    - <span data-ttu-id="71536-1424">”Get-AzIotHubDistributedTracing”</span><span class="sxs-lookup"><span data-stu-id="71536-1424">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="71536-1425">”Set-AzIotHubDistributedTracing”</span><span class="sxs-lookup"><span data-stu-id="71536-1425">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="71536-1426">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="71536-1426">Az.KeyVault</span></span>
* <span data-ttu-id="71536-1427">Ändrade attribut för icke-bakåtkompatibel ändring lades till för ”New-AzKeyVault”</span><span class="sxs-lookup"><span data-stu-id="71536-1427">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="71536-1428">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="71536-1428">Az.Monitor</span></span>
* <span data-ttu-id="71536-1429">Uppdaterad dokumentation för ”New-AzScheduledQueryRuleLogMetricTrigger”</span><span class="sxs-lookup"><span data-stu-id="71536-1429">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71536-1430">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71536-1430">Az.Network</span></span>
* <span data-ttu-id="71536-1431">Uppdaterade cmdletar för att tillåta VirtualHubVnetConnections mellan klienter</span><span class="sxs-lookup"><span data-stu-id="71536-1431">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="71536-1432">”New-AzVirtualHubVnetConnection”</span><span class="sxs-lookup"><span data-stu-id="71536-1432">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="71536-1433">”Update-AzVirtualHubVnetConnection”</span><span class="sxs-lookup"><span data-stu-id="71536-1433">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="71536-1434">”New-AzVirtualHub”</span><span class="sxs-lookup"><span data-stu-id="71536-1434">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="71536-1435">”Update-AzVirtualHub”</span><span class="sxs-lookup"><span data-stu-id="71536-1435">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="71536-1436">SQL Management SDK-beroende har tagits bort</span><span class="sxs-lookup"><span data-stu-id="71536-1436">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="71536-1437">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="71536-1437">Az.PolicyInsights</span></span>
* <span data-ttu-id="71536-1438">Förbättrade felmeddelanden</span><span class="sxs-lookup"><span data-stu-id="71536-1438">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="71536-1439">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="71536-1439">Az.RecoveryServices</span></span>
* <span data-ttu-id="71536-1440">Azure Site Recovery har lagt till stöd för återaktivering av skydd och uppdaterade VM-egenskaper för virtuella Azure-datorer med krypterad disk.</span><span class="sxs-lookup"><span data-stu-id="71536-1440">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="71536-1441">Lade till Azure Site Recovery VmwareToAzure-egenskaper för DR-övervakning</span><span class="sxs-lookup"><span data-stu-id="71536-1441">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="71536-1442">Azure Backup har lagt till stöd för att försöka uppdatera principuppdateringen för misslyckade objekt på nytt.</span><span class="sxs-lookup"><span data-stu-id="71536-1442">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="71536-1443">Azure Backup lagt till stöd för diskundantagsinställningar under säkerhetskopiering och återställning.</span><span class="sxs-lookup"><span data-stu-id="71536-1443">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="71536-1444">Azure Backup lagt till stöd för att återställa flera filer/mappar i AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="71536-1444">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="71536-1445">Azure Backup lade till support för användardefinierad Resourcegroup-support vid uppdatering av IaasVM-princip</span><span class="sxs-lookup"><span data-stu-id="71536-1445">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="71536-1446">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71536-1446">Az.Resources</span></span>
* <span data-ttu-id="71536-1447">Åtgärdade ”Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType” så att den använder den faktisk apiVersion av resurser i stället för standard-apiVersion [#11267]</span><span class="sxs-lookup"><span data-stu-id="71536-1447">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="71536-1448">Lade till correlationId-loggning för felscenarier</span><span class="sxs-lookup"><span data-stu-id="71536-1448">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="71536-1449">Liten dokumentationsändring för ”Get-AzResourceLock”.</span><span class="sxs-lookup"><span data-stu-id="71536-1449">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="71536-1450">Lade till exempel.</span><span class="sxs-lookup"><span data-stu-id="71536-1450">Added example.</span></span>
* <span data-ttu-id="71536-1451">Undantaget enkelt citattecken i parametervärde för ”Get-AzADUser” [#11317]</span><span class="sxs-lookup"><span data-stu-id="71536-1451">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="71536-1452">Nya cmdletar har lagts till för distributionsskript (”Get-AzDeploymentScript”, ”Get-AzDeploymentScriptLog”, ”Save-AzDeploymentScriptLog”, ”Remove-AzDeploymentScript”)</span><span class="sxs-lookup"><span data-stu-id="71536-1452">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="71536-1453">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71536-1453">Az.Sql</span></span>
* <span data-ttu-id="71536-1454">En läsbar sekundär parameter har lagts till i Invoke-AzSqlDatabaseFailover</span><span class="sxs-lookup"><span data-stu-id="71536-1454">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="71536-1455">Cmdleten Disable-AzSqlServerActiveDirectoryOnlyAuthentication har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-1455">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="71536-1456">Den sparade känslighet rangordningen när kolumner klassificeras i databasen.</span><span class="sxs-lookup"><span data-stu-id="71536-1456">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="71536-1457">Az.Support</span><span class="sxs-lookup"><span data-stu-id="71536-1457">Az.Support</span></span>
* <span data-ttu-id="71536-1458">Allmän tillgänglighet för ”Az.Support”-modulen</span><span class="sxs-lookup"><span data-stu-id="71536-1458">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="71536-1459">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="71536-1459">Az.Websites</span></span>
* <span data-ttu-id="71536-1460">Stöd har lagts till för att arbeta med trafikdirigeringsregler för webbappar under nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="71536-1460">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="71536-1461">”Get-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="71536-1461">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="71536-1462">”Update-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="71536-1462">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="71536-1463">”Add-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="71536-1463">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="71536-1464">”Remove-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="71536-1464">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="71536-1465">3.6.1 – mars 2020</span><span class="sxs-lookup"><span data-stu-id="71536-1465">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="71536-1466">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="71536-1466">Az.Accounts</span></span>
* <span data-ttu-id="71536-1467">Öppna sidan med Azure PowerShell-enkäten i ”Send-Feedback” [#11020]</span><span class="sxs-lookup"><span data-stu-id="71536-1467">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="71536-1468">Visa URL:en för Azure PowerShell-enkäten i ”Resolve-Error” [#11021]</span><span class="sxs-lookup"><span data-stu-id="71536-1468">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="71536-1469">Az-version har lagts till i UserAgent</span><span class="sxs-lookup"><span data-stu-id="71536-1469">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="71536-1470">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="71536-1470">Az.ApiManagement</span></span>
* <span data-ttu-id="71536-1471">Stöd har lagts till för att hämta och konfigurera en anpassad domän på DeveloperPortal-slutpunkten [#11007]</span><span class="sxs-lookup"><span data-stu-id="71536-1471">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="71536-1472">”Export-AzApiManagementApi” Stöd har lagts till för att ladda ned API-definition i Json-format [#9987]</span><span class="sxs-lookup"><span data-stu-id="71536-1472">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="71536-1473">”Import-AzApiManagementApi” Stöd har lagts till för att importera OpenApi 3.0-definition från Json-dokument</span><span class="sxs-lookup"><span data-stu-id="71536-1473">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="71536-1474">”New-AzApiManagementIdentityProvider” och ”Set-AzApiManagementIdentityProvider” Stöd har lagts till för att konfigurera ”Signin Tenant” för AAD B2C-provider [#9784]</span><span class="sxs-lookup"><span data-stu-id="71536-1474">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="71536-1475">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="71536-1475">Az.DataLakeStore</span></span>
* <span data-ttu-id="71536-1476">En referens har uttryckligen lagts till för System.Buffers i csproj och psd1.</span><span class="sxs-lookup"><span data-stu-id="71536-1476">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="71536-1477">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="71536-1477">Az.IotHub</span></span>
* <span data-ttu-id="71536-1478">Lade till stöd för att hantera enheter i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="71536-1478">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="71536-1479">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="71536-1479">New Cmdlets are:</span></span>
    - <span data-ttu-id="71536-1480">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="71536-1480">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="71536-1481">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="71536-1481">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="71536-1482">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="71536-1482">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="71536-1483">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="71536-1483">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="71536-1484">Stöd har lagts till för att hantera moduler på en mål-IoT-enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="71536-1484">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="71536-1485">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="71536-1485">New Cmdlets are:</span></span>
    - <span data-ttu-id="71536-1486">”Add-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="71536-1486">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="71536-1487">”Get-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="71536-1487">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="71536-1488">”Remove-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="71536-1488">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="71536-1489">”Set-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="71536-1489">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="71536-1490">Cmdlet har lagts till för att hämta anslutningssträngen för en mål-IoT-enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="71536-1490">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="71536-1491">Cmdlet har lagts till för att hämta anslutningssträngen för en modul på en mål-IoT-enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="71536-1491">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="71536-1492">Stöd har lagts till för att hämta/ange en överordnad enhet för en IoT-enhet.</span><span class="sxs-lookup"><span data-stu-id="71536-1492">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="71536-1493">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="71536-1493">New Cmdlets are:</span></span>
    - <span data-ttu-id="71536-1494">”Get-AzIotHubDeviceParent”</span><span class="sxs-lookup"><span data-stu-id="71536-1494">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="71536-1495">”Set-AzIotHubDeviceParent”</span><span class="sxs-lookup"><span data-stu-id="71536-1495">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="71536-1496">Stöd har lagts till för att hantera en enhets överordnade och underordnade relationer.</span><span class="sxs-lookup"><span data-stu-id="71536-1496">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="71536-1497">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="71536-1497">Az.Monitor</span></span>
* <span data-ttu-id="71536-1498">Utdatavärdet har åtgärdats för ”Get-AzMetricDefinition” [#9714]</span><span class="sxs-lookup"><span data-stu-id="71536-1498">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71536-1499">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71536-1499">Az.Network</span></span>
* <span data-ttu-id="71536-1500">SQL Management SDK har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="71536-1500">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="71536-1501">Ett problem har åtgärdats med namngivningsskillnader i klassen PrivateLinkServiceConnectionState.</span><span class="sxs-lookup"><span data-stu-id="71536-1501">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="71536-1502">Fältet ActionsRequired mappar till ActionRequired.</span><span class="sxs-lookup"><span data-stu-id="71536-1502">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="71536-1503">PublicNetworkAccess har lagts till i ”New-AzSqlServer” och ”Set-AzSqlServer”</span><span class="sxs-lookup"><span data-stu-id="71536-1503">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="71536-1504">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71536-1504">Az.Resources</span></span>
* <span data-ttu-id="71536-1505">Null-referensfel har åtgärdats i ”Get-AzRoleAssignment”</span><span class="sxs-lookup"><span data-stu-id="71536-1505">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="71536-1506">Växlarna ”-Force” och ”-PassThru” är valfria i ”Remove-AzADGroup” [#10849]</span><span class="sxs-lookup"><span data-stu-id="71536-1506">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="71536-1507">Ett problem har åtgärdats som gjorde att ”MailNickname” inte returnerades i ”Remove-AzADGroup” [#11167]</span><span class="sxs-lookup"><span data-stu-id="71536-1507">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="71536-1508">Ett problem har åtgärdats som gjorde att pipe-åtgärden ”Remove-AzADGroup” inte fungerar [#11171]</span><span class="sxs-lookup"><span data-stu-id="71536-1508">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="71536-1509">Ett null-referensfel har åtgärdats i GetAzureRoleAssignmentCommand</span><span class="sxs-lookup"><span data-stu-id="71536-1509">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="71536-1510">Attribut för icke-bakåtkompatibla ändringar har lagts till för kommande ändringar i cmdlets för principer</span><span class="sxs-lookup"><span data-stu-id="71536-1510">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="71536-1511">”Get-AzResourceGroup” har uppdaterats för att utföra taggfiltrering för resursgrupper på serversidan</span><span class="sxs-lookup"><span data-stu-id="71536-1511">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="71536-1512">Utökade Tag-cmdlets stöder -ResourceId</span><span class="sxs-lookup"><span data-stu-id="71536-1512">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="71536-1513">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="71536-1513">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="71536-1514">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="71536-1514">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="71536-1515">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="71536-1515">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="71536-1516">Ny Tag-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-1516">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="71536-1517">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="71536-1517">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="71536-1518">Flyttade ScopedDeployment från SDK 3.3.0</span><span class="sxs-lookup"><span data-stu-id="71536-1518">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="71536-1519">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71536-1519">Az.Sql</span></span>
* <span data-ttu-id="71536-1520">PublicNetworkAccess har lagts till i ”New-AzSqlServer” och ”Set-AzSqlServer”</span><span class="sxs-lookup"><span data-stu-id="71536-1520">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="71536-1521">Stöd har lagts till för konfiguration av säkerhetskopiering för långsiktig kvarhållning för hanterade databaser</span><span class="sxs-lookup"><span data-stu-id="71536-1521">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="71536-1522">Hämta/ange LTR-princip på en hanterad databas</span><span class="sxs-lookup"><span data-stu-id="71536-1522">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="71536-1523">Hämta LTR-säkerhetskopior efter hanterad databas, hanterad instans eller plats</span><span class="sxs-lookup"><span data-stu-id="71536-1523">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="71536-1524">Ta bort en LTR-säkerhetskopia</span><span class="sxs-lookup"><span data-stu-id="71536-1524">Remove an LTR backup</span></span>
    - <span data-ttu-id="71536-1525">Återställa en LTR-säkerhetskopia för att skapa en ny hanterad databas</span><span class="sxs-lookup"><span data-stu-id="71536-1525">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="71536-1526">MinimalTlsVersion har lagts till för New-AzSqlServer och Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="71536-1526">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="71536-1527">MinimalTlsVersion har lagts till för New-AzSqlInstance och Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="71536-1527">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="71536-1528">SQL SDK-versionen för Az.Network har ändrats</span><span class="sxs-lookup"><span data-stu-id="71536-1528">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="71536-1529">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="71536-1529">Az.Storage</span></span>
* <span data-ttu-id="71536-1530">AllowProtectedAppendWrite stöds i ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="71536-1530">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="71536-1531">”Set-AzRmStorageContainerImmutabilityPolicy”</span><span class="sxs-lookup"><span data-stu-id="71536-1531">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="71536-1532">Varningsmeddelande har lagts till om icke-bakåtkompatibel ändring för ändring av typen AzureStorageTable i en senare version</span><span class="sxs-lookup"><span data-stu-id="71536-1532">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="71536-1533">”New-AzStorageTable”</span><span class="sxs-lookup"><span data-stu-id="71536-1533">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="71536-1534">”Get-AzStorageTable”</span><span class="sxs-lookup"><span data-stu-id="71536-1534">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="71536-1535">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="71536-1535">Az.Websites</span></span>
* <span data-ttu-id="71536-1536">Tag-parametern har lagts till för ”New-AzAppServicePlan” och ”Set-AzAppServicePlan”</span><span class="sxs-lookup"><span data-stu-id="71536-1536">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="71536-1537">Stoppa cmdlet-körning om ett undantag uppstår när en anpassad domän läggs till på en webbplats</span><span class="sxs-lookup"><span data-stu-id="71536-1537">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="71536-1538">Stöd har lagts till för att utföra åtgärder för App Services som inte tillhör samma resursgrupp som App Services-planen</span><span class="sxs-lookup"><span data-stu-id="71536-1538">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="71536-1539">Åtkomstbegränsning har tillämpats på WebApp/Function i olika resursgrupper</span><span class="sxs-lookup"><span data-stu-id="71536-1539">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="71536-1540">Ett problem har åtgärdats för att ange anpassade värdnamn för WebAppSlots</span><span class="sxs-lookup"><span data-stu-id="71536-1540">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="71536-1541">3.5.0 – februari 2020</span><span class="sxs-lookup"><span data-stu-id="71536-1541">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="71536-1542">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="71536-1542">Highlights since the last major release</span></span>
* <span data-ttu-id="71536-1543">Uppdaterade telemetri på klientsidan.</span><span class="sxs-lookup"><span data-stu-id="71536-1543">Updated client side telemetry.</span></span>
* <span data-ttu-id="71536-1544">Az.IotHub lade till cmdletar som stöd för att hantera enheter.</span><span class="sxs-lookup"><span data-stu-id="71536-1544">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="71536-1545">Az.SqlVirtualMachine lade till cmdletar för lyssningsfunktion för tillgänglighetsgrupp.</span><span class="sxs-lookup"><span data-stu-id="71536-1545">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="71536-1546">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="71536-1546">Az.Accounts</span></span>
* <span data-ttu-id="71536-1547">Lade till SubscriptionId, TenantId och körningstid i data för telemetri på klientsidan</span><span class="sxs-lookup"><span data-stu-id="71536-1547">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="71536-1548">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="71536-1548">Az.Automation</span></span>
* <span data-ttu-id="71536-1549">Åtgärdade skrivfel i exempel 1 i referensdokumentation för ”New-AzAutomationSoftwareUpdateConfiguration”</span><span class="sxs-lookup"><span data-stu-id="71536-1549">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="71536-1550">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="71536-1550">Az.CognitiveServices</span></span>
* <span data-ttu-id="71536-1551">Uppdaterade SDK till 7.0</span><span class="sxs-lookup"><span data-stu-id="71536-1551">Updated SDK to 7.0</span></span>
* <span data-ttu-id="71536-1552">Förbättrade felmeddelande vid serversvar om tom brödtext</span><span class="sxs-lookup"><span data-stu-id="71536-1552">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71536-1553">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71536-1553">Az.Compute</span></span>
* <span data-ttu-id="71536-1554">Tillät tomt värde för ProximityPlacementGroupId under uppdatering</span><span class="sxs-lookup"><span data-stu-id="71536-1554">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="71536-1555">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="71536-1555">Az.FrontDoor</span></span>
* <span data-ttu-id="71536-1556">Lade till cmdlet för att hämta hanterade regeldefinitioner som kan användas i WAF</span><span class="sxs-lookup"><span data-stu-id="71536-1556">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="71536-1557">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="71536-1557">Az.IotHub</span></span>
* <span data-ttu-id="71536-1558">Lade till stöd för att hantera enheter i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="71536-1558">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="71536-1559">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="71536-1559">New Cmdlets are:</span></span>
    - <span data-ttu-id="71536-1560">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="71536-1560">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="71536-1561">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="71536-1561">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="71536-1562">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="71536-1562">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="71536-1563">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="71536-1563">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="71536-1564">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="71536-1564">Az.KeyVault</span></span>
* <span data-ttu-id="71536-1565">Åtgärdade duplicerad text för Add-AzKeyVaultKey.md</span><span class="sxs-lookup"><span data-stu-id="71536-1565">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="71536-1566">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="71536-1566">Az.Monitor</span></span>
* <span data-ttu-id="71536-1567">Åtgärdade beskrivning av cmdleten Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="71536-1567">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="71536-1568">En ny parameter med namnet ActionGroupId har lagts till i kommandot ”New-AzMetricAlertRuleV2”.</span><span class="sxs-lookup"><span data-stu-id="71536-1568">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="71536-1569">Användaren kan ange ActionGroupId(string) eller ActionGroup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="71536-1569">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71536-1570">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71536-1570">Az.Network</span></span>
* <span data-ttu-id="71536-1571">Lade till en extra parameteranteckning för parametern ”-EnableProxyProtocol” för cmdleten ”New-AzPrivateLinkService”.</span><span class="sxs-lookup"><span data-stu-id="71536-1571">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="71536-1572">Åtgärdade FilterData-exempel i Start-AzVirtualNetworkGatewayConnectionPacketCapture.md och Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="71536-1572">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="71536-1573">Lade till paketinsamlingsexempel för att samla in alla inre och yttre paket i Start-AzVirtualNetworkGatewayConnectionPacketCapture.md och Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="71536-1573">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="71536-1574">Lade till stöd för Azure-brandväggsprincip på VNet-brandväggar</span><span class="sxs-lookup"><span data-stu-id="71536-1574">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="71536-1575">Inga nya cmdletar har lagts till.</span><span class="sxs-lookup"><span data-stu-id="71536-1575">No new cmdlets are added.</span></span> <span data-ttu-id="71536-1576">Lättar begränsningen för brandväggsprincip på VNet-brandväggar</span><span class="sxs-lookup"><span data-stu-id="71536-1576">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="71536-1577">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="71536-1577">Az.RecoveryServices</span></span>
* <span data-ttu-id="71536-1578">Lade till stöd för Restore-as-files för SQL-databaser.</span><span class="sxs-lookup"><span data-stu-id="71536-1578">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="71536-1579">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71536-1579">Az.Resources</span></span>
* <span data-ttu-id="71536-1580">Omstrukturerade cmdletar för malldistribution</span><span class="sxs-lookup"><span data-stu-id="71536-1580">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="71536-1581">Lade till nya cmdletar för att hantera distributioner i hanteringsgruppen: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="71536-1581">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="71536-1582">Lade till nya cmdletar för att hantera distributioner i klientorganisationsområdet: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="71536-1582">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="71536-1583">Omstrukturerade \*-AzDeployment-cmdletar för att fungera specifikt i prenumerationsomfattningen</span><span class="sxs-lookup"><span data-stu-id="71536-1583">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="71536-1584">Skapade alias \*-AzSubscriptionDeployment för \*-AzDeployment-cmdletar</span><span class="sxs-lookup"><span data-stu-id="71536-1584">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="71536-1585">Åtgärdade ”Update-AzADApplication” när parametern ”AvailableToOtherTenants” inte har angetts</span><span class="sxs-lookup"><span data-stu-id="71536-1585">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="71536-1586">Tog bort ApplicationObjectWithoutCredentialParameterSet för att undvika AmbiguousParameterSetException.</span><span class="sxs-lookup"><span data-stu-id="71536-1586">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="71536-1587">Återskapade hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="71536-1587">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="71536-1588">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71536-1588">Az.Sql</span></span>
* <span data-ttu-id="71536-1589">Lade till stöd för återställning till tidpunkt mellan prenumerationer på hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="71536-1589">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="71536-1590">Lade till stöd för att ändra befintlig SQL Managed Instance-maskinvarugenerering</span><span class="sxs-lookup"><span data-stu-id="71536-1590">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="71536-1591">Åtgärdade ”Update-AzSqlServerVulnerabilityAssessmentSetting”-hjälpexempel: parameter/egenskapsutdata - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="71536-1591">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="71536-1592">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="71536-1592">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="71536-1593">Lade till cmdletar för lyssningsfunktion för tillgänglighetsgrupp</span><span class="sxs-lookup"><span data-stu-id="71536-1593">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="71536-1594">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="71536-1594">Az.StorageSync</span></span>
* <span data-ttu-id="71536-1595">Uppdaterade teckenuppsättningar som stöds i ”Invoke-AzStorageSyncCompatibilityCheck”.</span><span class="sxs-lookup"><span data-stu-id="71536-1595">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="71536-1596">3.4.0 – februari 2020</span><span class="sxs-lookup"><span data-stu-id="71536-1596">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="71536-1597">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="71536-1597">Highlights since the last major release</span></span>
* <span data-ttu-id="71536-1598">Första Az.CosmosDB-versionen 0.1.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="71536-1598">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="71536-1599">Stöd för Az.Network ConnectionMonitor V2 har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-1599">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="71536-1600">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="71536-1600">Az.Accounts</span></span>
* <span data-ttu-id="71536-1601">Inaktivera automatisk sparande av kontext när AzureRmContext.json inte är tillgängligt</span><span class="sxs-lookup"><span data-stu-id="71536-1601">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="71536-1602">Uppdatera referensen till Azure Powershell Common till 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="71536-1602">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="71536-1603">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="71536-1603">Az.ApiManagement</span></span>
* <span data-ttu-id="71536-1604">**Get-AzApiManagementApiSchema** Hämtning av Open-Api-schema som är associerat med ett API har åtgärdats   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="71536-1604">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="71536-1605">**New-AzApiManagementProduct** _ och _ *Set-AzApiManagementProduct*\*</span><span class="sxs-lookup"><span data-stu-id="71536-1605">**New-AzApiManagementProduct** _ and _ *Set-AzApiManagementProduct*\*</span></span>
  - <span data-ttu-id="71536-1606">Åtgärda dokumentation för https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="71536-1606">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="71536-1607">**Set-AzApiManagementApi** Exempel för att visa hur ServiceUrl uppdateras med hjälp av cmdleten har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-1607">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71536-1608">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71536-1608">Az.Compute</span></span>
* <span data-ttu-id="71536-1609">Begränsa antalet VM-status till 100 för att undvika begränsning när Get-AzVM -Status utförs utan VM-namn.</span><span class="sxs-lookup"><span data-stu-id="71536-1609">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="71536-1610">Lägg till cmdleten Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="71536-1610">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="71536-1611">Lägg till parametrarna EncryptionType och DiskEncryptionSetId i följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="71536-1611">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="71536-1612">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="71536-1612">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="71536-1613">Lägg till parametern ColocationStatus för cmdleten Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="71536-1613">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="71536-1614">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="71536-1614">Az.DataFactory</span></span>
* <span data-ttu-id="71536-1615">Uppdatera ADF .Net SDK-versionen till 4.7.0</span><span class="sxs-lookup"><span data-stu-id="71536-1615">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="71536-1616">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="71536-1616">Az.DeploymentManager</span></span>
* <span data-ttu-id="71536-1617">Lägger till LIST-åtgärder för resurser</span><span class="sxs-lookup"><span data-stu-id="71536-1617">Adds LIST operations for resources</span></span>
* <span data-ttu-id="71536-1618">Lägger till funktion för att utföra åtgärder för hälsokontrollsteg</span><span class="sxs-lookup"><span data-stu-id="71536-1618">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="71536-1619">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="71536-1619">Az.HDInsight</span></span>
* <span data-ttu-id="71536-1620">Åtgärda dokumentfel för New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="71536-1620">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="71536-1621">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="71536-1621">Az.KeyVault</span></span>
* <span data-ttu-id="71536-1622">Lägg till Name-alias för attributet VaultName så att Remove-AzureKeyVault stämmer överens med New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="71536-1622">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71536-1623">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71536-1623">Az.Network</span></span>
* <span data-ttu-id="71536-1624">Nytt exempel har lagts till i Set-AzNetworkWatcherConfigFlowLog.md för att demonstrera ett inaktiveringsscenario för Trafikanalys.</span><span class="sxs-lookup"><span data-stu-id="71536-1624">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="71536-1625">Lägg till stöd för att tilldela konfiguration av hanterings-IP till Azure Firewall – ett dedikerat undernät och en offentlig IP som brandväggen använder för dess hanteringstrafik</span><span class="sxs-lookup"><span data-stu-id="71536-1625">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="71536-1626">Cmdleten New-AzFirewall har uppdaterats:</span><span class="sxs-lookup"><span data-stu-id="71536-1626">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="71536-1627">Parametern -ManagementPublicIpAddress (inte obligatorisk) som accepterar ett offentligt IP-adressobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-1627">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="71536-1628">Metoden SetManagementIpConfiguration har lagts till för brandväggsobjekt – kräver ett undernät och en offentlig IP-adress som indata – undernätets namn måste vara ”AzureFirewallManagementSubnet”</span><span class="sxs-lookup"><span data-stu-id="71536-1628">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="71536-1629">Exempel för Get-AzNetworkSecurityGroup har korrigerats så att exempel visas för NSG:er i stället för nätverksgränssnitt.</span><span class="sxs-lookup"><span data-stu-id="71536-1629">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="71536-1630">Ett skrivfel har åtgärdats i kommandot New-AzVpnSite som hindrade kompletteraren för resurs-ID från att fylla i en parameter.</span><span class="sxs-lookup"><span data-stu-id="71536-1630">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="71536-1631">Stöd för Url-konfiguration i åtgärdsuppsättningen för omskrivningsregler i Application Gateway har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-1631">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="71536-1632">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="71536-1632">New cmdlets added:</span></span>
        - <span data-ttu-id="71536-1633">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="71536-1633">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="71536-1634">Cmdletar har uppdaterats med den valfria parametern -UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="71536-1634">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="71536-1635">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="71536-1635">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="71536-1636">Lägg till stöd för resurser för NetworkWatcher ConnectionMonitor version 2</span><span class="sxs-lookup"><span data-stu-id="71536-1636">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="71536-1637">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="71536-1637">Az.PolicyInsights</span></span>
* <span data-ttu-id="71536-1638">Stöd för utvärdering av efterlevnad innan fastställande av vilken resurs som ska åtgärdas</span><span class="sxs-lookup"><span data-stu-id="71536-1638">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="71536-1639">Lägg till parametern ”-ResourceDiscoverMode” för Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="71536-1639">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="71536-1640">Lägg till cmdleten Get-AzPolicyMetadata för att hämta resurser för principmetadata</span><span class="sxs-lookup"><span data-stu-id="71536-1640">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="71536-1641">Get-AzPolicyState och Get-AzPolicyStateSummary för API-versionen 2019-10-01 har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="71536-1641">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="71536-1642">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="71536-1642">Az.RecoveryServices</span></span>
* <span data-ttu-id="71536-1643">Azure Site Recovery-stöd för att ta bort en replikerad disk.</span><span class="sxs-lookup"><span data-stu-id="71536-1643">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="71536-1644">Tillagt Azure Backup-stöd för att lägga till taggar när ett Recovery Services-valv skapas.</span><span class="sxs-lookup"><span data-stu-id="71536-1644">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="71536-1645">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71536-1645">Az.Resources</span></span>
* <span data-ttu-id="71536-1646">Gör -Scope valfritt i cmdletarna \*-AzPolicyAssignment med standardinställning till kontextprenumeration</span><span class="sxs-lookup"><span data-stu-id="71536-1646">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="71536-1647">Lägg till exempel på att skapa ADServicePrincipal med lösenord och nyckelautentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="71536-1647">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="71536-1648">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71536-1648">Az.Sql</span></span>
<span data-ttu-id="71536-1649">Åtgärda cmdleten New-AzSqlDatabaseSecondary så att existensen PartnerDatabaseName kontrolleras i stället för existensen DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="71536-1649">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="71536-1650">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="71536-1650">Az.Storage</span></span>
* <span data-ttu-id="71536-1651">Stöd för angivning av krypteringsnyckeltyp för Tabell/kö i Skapa lagringskonto</span><span class="sxs-lookup"><span data-stu-id="71536-1651">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="71536-1652">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="71536-1652">New-AzStorageAccount</span></span>
* <span data-ttu-id="71536-1653">Visa RequestId när StorageException inte har ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="71536-1653">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="71536-1654">Åtgärda exempel 6 för cmdleten Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="71536-1654">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="71536-1655">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="71536-1655">Az.Websites</span></span>
* <span data-ttu-id="71536-1656">Set-AzWebapp och Set-AzWebappSlot stöder egenskaperna AlwaysOn, MinTls och FtpsState</span><span class="sxs-lookup"><span data-stu-id="71536-1656">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="71536-1657">Åtgärdar problemet där inställning av HttpsOnly samtidigt som AppservicePlan ändrades med det enskilda kommandot Set-AzWebApp återställde HttpsOnly till standardvärdet</span><span class="sxs-lookup"><span data-stu-id="71536-1657">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="71536-1658">3.3.0 – januari 2020</span><span class="sxs-lookup"><span data-stu-id="71536-1658">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="71536-1659">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="71536-1659">Az.Accounts</span></span>
* <span data-ttu-id="71536-1660">Nu stöder Add-AzEnvironment och Set-AzEnvironment parametrarna AzureAttestationServiceEndpointResourceId och AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="71536-1660">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="71536-1661">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="71536-1661">Az.Cdn</span></span>
* <span data-ttu-id="71536-1662">Information om felsvar visas i New-AzCdnEndpoint-cmdleten</span><span class="sxs-lookup"><span data-stu-id="71536-1662">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71536-1663">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71536-1663">Az.Compute</span></span>
* <span data-ttu-id="71536-1664">Set-AzVMCustomScriptExtension-cmdleten har åtgärdats för en virtuell dator med hanterad OD-disk som inte har någon operativsystemprofil.</span><span class="sxs-lookup"><span data-stu-id="71536-1664">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="71536-1665">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="71536-1665">Az.ContainerInstance</span></span>
* <span data-ttu-id="71536-1666">Parameternamn som används med New-AzContainerGroup-exempel har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="71536-1666">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="71536-1667">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="71536-1667">Az.DataBoxEdge</span></span>
* <span data-ttu-id="71536-1668">Cmdleten ”Get-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-1668">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="71536-1669">Hämta gränslagringscontainern</span><span class="sxs-lookup"><span data-stu-id="71536-1669">Get the Edge Storage Container</span></span>
* <span data-ttu-id="71536-1670">Cmdleten ”New-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-1670">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="71536-1671">Skapa en ny gränslagringscontainer</span><span class="sxs-lookup"><span data-stu-id="71536-1671">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="71536-1672">Cmdleten ”Remove-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-1672">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="71536-1673">Ta bort gränslagringscontainern</span><span class="sxs-lookup"><span data-stu-id="71536-1673">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="71536-1674">Cmdleten ”Invoke-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-1674">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="71536-1675">Anropa åtgärd för att uppdatera data i gränslagringscontainer</span><span class="sxs-lookup"><span data-stu-id="71536-1675">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="71536-1676">Cmdleten ”Get-AzDataBoxEdgeStorageAccount” har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-1676">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="71536-1677">Hämta gränslagringskontot</span><span class="sxs-lookup"><span data-stu-id="71536-1677">Get the Edge Storage Account</span></span>
* <span data-ttu-id="71536-1678">Cmdleten ”New-AzDataBoxEdgeStorageAccount” har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-1678">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="71536-1679">Skapa ett nytt gränslagringskonto</span><span class="sxs-lookup"><span data-stu-id="71536-1679">Create new Edge Storage Account</span></span>
* <span data-ttu-id="71536-1680">Cmdleten ”Remove-AzDataBoxEdgeStorageAccount” har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-1680">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="71536-1681">Ta bort gränslagringskontot</span><span class="sxs-lookup"><span data-stu-id="71536-1681">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="71536-1682">Anropa cmdleten ”Invoke-AzDataBoxEdgeShare”</span><span class="sxs-lookup"><span data-stu-id="71536-1682">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="71536-1683">Anropa åtgärd för att uppdatera resursdata</span><span class="sxs-lookup"><span data-stu-id="71536-1683">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="71536-1684">Cmdleten ”Set-AzDataBoxEdgeStorageAccountCredential” har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-1684">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="71536-1685">Ange autentiseringsuppgifter för az databoxedge-lagringskonto</span><span class="sxs-lookup"><span data-stu-id="71536-1685">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="71536-1686">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="71536-1686">Az.DataFactory</span></span>
* <span data-ttu-id="71536-1687">Lägg till AutoUpdateETA-, LatestVersion-, PushedVersion-, TaskQueueId- och VersionStatus-egenskaper för Get-AzDataFactoryV2IntegrationRuntime-cmd</span><span class="sxs-lookup"><span data-stu-id="71536-1687">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="71536-1688">Uppdatera ADF .Net SDK-versionen till 4.6.0</span><span class="sxs-lookup"><span data-stu-id="71536-1688">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="71536-1689">Lägg till parametern ”PublicIPs” för ”Set-AzureRmDataFactoryV2IntegrationRuntime”-cmd så att Azure-SSIS IR kan skapas med statiska offentliga IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="71536-1689">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="71536-1690">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="71536-1690">Az.DevTestLabs</span></span>
* <span data-ttu-id="71536-1691">Ta bort den brutna länken i Get-AzDtlAllowedVMSizesPolicy.md</span><span class="sxs-lookup"><span data-stu-id="71536-1691">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="71536-1692">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="71536-1692">Az.EventHub</span></span>
* <span data-ttu-id="71536-1693">Korrigering av problem 10634: Åtgärda referensen till null-objekt för eventhubnamespace-borttagning</span><span class="sxs-lookup"><span data-stu-id="71536-1693">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="71536-1694">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="71536-1694">Az.HDInsight</span></span>
* <span data-ttu-id="71536-1695">Åtgärda Invoke-AzHDInsightHiveJob.md-fel.</span><span class="sxs-lookup"><span data-stu-id="71536-1695">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="71536-1696">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="71536-1696">Az.MachineLearning</span></span>
* <span data-ttu-id="71536-1697">Nedanstående cmdletar har tagits bort eftersom MachineLearningCompute inte längre är tillgängligt</span><span class="sxs-lookup"><span data-stu-id="71536-1697">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="71536-1698">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="71536-1698">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="71536-1699">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="71536-1699">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="71536-1700">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="71536-1700">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="71536-1701">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="71536-1701">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="71536-1702">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="71536-1702">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="71536-1703">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="71536-1703">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="71536-1704">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="71536-1704">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71536-1705">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71536-1705">Az.Network</span></span>
* <span data-ttu-id="71536-1706">Uppgradera beroende av Microsoft.Azure.Management.Sql från 1.36-preview till 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="71536-1706">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="71536-1707">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="71536-1707">Az.RecoveryServices</span></span>
* <span data-ttu-id="71536-1708">Ändrat Azure Site Recovery-stöd för krypterade vilande data på virtuella datorer med hanterade diskar med kundhanterade nycklar för Azure till Azure-providern.</span><span class="sxs-lookup"><span data-stu-id="71536-1708">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="71536-1709">Azure Site Recovery-stöd för att ange ID för diskkrypteringsuppsättning som valfri inmatning för aktivering av skydd för VMware till Azure.</span><span class="sxs-lookup"><span data-stu-id="71536-1709">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="71536-1710">Azure Site Recovery-stöd för att ange ID för diskkrypteringsuppsättning som valfri inmatning på disknivå för aktivering av skydd för VMware till Azure.</span><span class="sxs-lookup"><span data-stu-id="71536-1710">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="71536-1711">Azure Site Recovery-stöd för att uppdatera replikeringsskyddade objekt med mappning för diskkrypteringsuppsättning för HyperV till Azure.</span><span class="sxs-lookup"><span data-stu-id="71536-1711">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="71536-1712">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71536-1712">Az.Resources</span></span>
* <span data-ttu-id="71536-1713">Åtgärda ett fel i hjälpdokument för ”Remove-AzTag”.</span><span class="sxs-lookup"><span data-stu-id="71536-1713">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="71536-1714">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71536-1714">Az.Sql</span></span>
* <span data-ttu-id="71536-1715">Åtgärda funktioner i cmdletar för att ange baslinjen för sårbarhetsbedömning för arbete med huvuddatabasen för Azure-databasen och begränsa den för systemdatabaser på hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="71536-1715">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="71536-1716">Åtgärda ett fel när en redundansgrupp för en SQL-instans skapas</span><span class="sxs-lookup"><span data-stu-id="71536-1716">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="71536-1717">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="71536-1717">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="71536-1718">Lägg till DR som en ny giltig licenstyp</span><span class="sxs-lookup"><span data-stu-id="71536-1718">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="71536-1719">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="71536-1719">Az.Storage</span></span>
* <span data-ttu-id="71536-1720">Lägg till varningsmeddelande om icke-bakåtkompatibel ändring för DefaultAction-värdeändring i en framtida version</span><span class="sxs-lookup"><span data-stu-id="71536-1720">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="71536-1721">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="71536-1721">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="71536-1722">Stöd för att hämta lagringskontots senaste synkroniseringstid genom att köra get-AzureRMStorageAccount med parametern -IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="71536-1722">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="71536-1723">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="71536-1723">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="71536-1724">3.2.0 – December 2019</span><span class="sxs-lookup"><span data-stu-id="71536-1724">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="71536-1725">Allmänt</span><span class="sxs-lookup"><span data-stu-id="71536-1725">General</span></span>
* <span data-ttu-id="71536-1726">Uppdatera referenser i .psd1 för att använda relativa sökvägar för alla moduler</span><span class="sxs-lookup"><span data-stu-id="71536-1726">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="71536-1727">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="71536-1727">Az.Accounts</span></span>
* <span data-ttu-id="71536-1728">Ange rätt UserAgent för telemetri på klientsidan för Az 4.0 preview</span><span class="sxs-lookup"><span data-stu-id="71536-1728">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="71536-1729">Visa användarvänligt felmeddelande när kontexten är null i Az 4.0 preview</span><span class="sxs-lookup"><span data-stu-id="71536-1729">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="71536-1730">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="71536-1730">Az.Batch</span></span>
* <span data-ttu-id="71536-1731">Korrigera problem [#10602](https://github.com/Azure/azure-powershell/issues/10602), där **New-AzBatchPool** skickade VirtualMachineConfiguration.ContainerConfiguration eller VirtualMachineConfiguration.DataDisks på ett felaktigt sätt till servern.</span><span class="sxs-lookup"><span data-stu-id="71536-1731">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="71536-1732">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="71536-1732">Az.DataFactory</span></span>
* <span data-ttu-id="71536-1733">Uppdatera ADF .Net SDK-versionen till 4.5.0</span><span class="sxs-lookup"><span data-stu-id="71536-1733">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="71536-1734">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="71536-1734">Az.FrontDoor</span></span>
* <span data-ttu-id="71536-1735">Stöd har lagts till för undantag för hanterade regler för brandväggen för webbaserade program</span><span class="sxs-lookup"><span data-stu-id="71536-1735">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="71536-1736">Lägg till SocketAddr för automatisk komplettering</span><span class="sxs-lookup"><span data-stu-id="71536-1736">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="71536-1737">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="71536-1737">Az.HealthcareApis</span></span>
* <span data-ttu-id="71536-1738">Undantagshantering</span><span class="sxs-lookup"><span data-stu-id="71536-1738">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="71536-1739">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="71536-1739">Az.KeyVault</span></span>
* <span data-ttu-id="71536-1740">Åtgärdat fel vid åtkomst av värde som kanske inte har angetts</span><span class="sxs-lookup"><span data-stu-id="71536-1740">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="71536-1741">Hantering av ECC-certifikat (Elliptic Curve Cryptography)</span><span class="sxs-lookup"><span data-stu-id="71536-1741">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="71536-1742">Stöd har lagts till för att ange kurvan för certifikatprinciper</span><span class="sxs-lookup"><span data-stu-id="71536-1742">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="71536-1743">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="71536-1743">Az.Monitor</span></span>
* <span data-ttu-id="71536-1744">Lägger till valfritt argument i kommandot Lägg till diagnostikinställningar.</span><span class="sxs-lookup"><span data-stu-id="71536-1744">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="71536-1745">Ett växelargument som om det finns visar att exporten till Log Analytics måste ske till ett fast schema (kallas även</span><span class="sxs-lookup"><span data-stu-id="71536-1745">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="71536-1746">dedikerad, datatyp)</span><span class="sxs-lookup"><span data-stu-id="71536-1746">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71536-1747">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71536-1747">Az.Network</span></span>
* <span data-ttu-id="71536-1748">Stöd för IpGroups i program-, NAT- och nätverksregler för Azure Firewall.</span><span class="sxs-lookup"><span data-stu-id="71536-1748">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="71536-1749">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71536-1749">Az.Resources</span></span>
* <span data-ttu-id="71536-1750">Åtgärda ett problem där malldistributionen inte kan läsa en mallparameter om dess namn står i konflikt med ett inbyggt parameternamn.</span><span class="sxs-lookup"><span data-stu-id="71536-1750">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="71536-1751">Uppdaterade princip-cmdletar för att använda den nya API-versionen 2019-09-01 som introducerar grupperingsstöd inom principuppsättningsdefinitioner.</span><span class="sxs-lookup"><span data-stu-id="71536-1751">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="71536-1752">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71536-1752">Az.Sql</span></span>
* <span data-ttu-id="71536-1753">Uppgraderad funktion för att skapa lagring i automatisk aktivering av sårbarhetsbedömning till StorageV2</span><span class="sxs-lookup"><span data-stu-id="71536-1753">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="71536-1754">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="71536-1754">Az.Storage</span></span>
* <span data-ttu-id="71536-1755">Stöd för generering av blob/container-identitetsbaserad SAS-token med lagringskontextbaserad på OAuth-autentisering</span><span class="sxs-lookup"><span data-stu-id="71536-1755">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="71536-1756">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="71536-1756">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="71536-1757">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="71536-1757">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="71536-1758">Stöd för återkallning av användardelegeringsnycklar för lagringskonto för att återkalla alla SAS-token</span><span class="sxs-lookup"><span data-stu-id="71536-1758">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="71536-1759">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="71536-1759">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="71536-1760">Uppgradera till Microsoft.Azure.Management.Storage 14.2.0 för att stödja den nya API-versionen 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="71536-1760">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="71536-1761">Stöd för QuotaGiB (resurskvot i Gibibye) för värden över 5120 i hanteringsplanet för cmdletar för filresurser och parameteraliaset. Quota har också lagts till för parametern ”QuotaGiB”.</span><span class="sxs-lookup"><span data-stu-id="71536-1761">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="71536-1762">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="71536-1762">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="71536-1763">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="71536-1763">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="71536-1764">Lägg till parameteraliaset QuotaGiB i parametern Quota</span><span class="sxs-lookup"><span data-stu-id="71536-1764">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="71536-1765">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="71536-1765">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="71536-1766">Åtgärda problemet att Set-AzStorageContainerAcl kan rensa den lagrade åtkomstprincipen</span><span class="sxs-lookup"><span data-stu-id="71536-1766">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="71536-1767">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="71536-1767">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="71536-1768">3.1.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="71536-1768">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="71536-1769">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="71536-1769">Highlights since the last major release</span></span>
* <span data-ttu-id="71536-1770">Az.DataBoxEdge 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="71536-1770">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="71536-1771">Az.SqlVirtualMachine 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="71536-1771">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71536-1772">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71536-1772">Az.Compute</span></span>
* <span data-ttu-id="71536-1773">Funktion för att använda en virtuell dator igen</span><span class="sxs-lookup"><span data-stu-id="71536-1773">VM Reapply feature</span></span>
    - <span data-ttu-id="71536-1774">Lägg till parameter för att använda igen till cmdleten Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="71536-1774">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="71536-1775">Funktionen AutomaticRepairs i VM-skalningsuppsättningar:</span><span class="sxs-lookup"><span data-stu-id="71536-1775">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="71536-1776">Lägg till parametrarna EnableAutomaticRepair, AutomaticRepairGracePeriod och AutomaticRepairMaxInstanceRepairsPercent till följande cmdletar:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="71536-1776">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="71536-1777">Stöd för galleriavbildningar i flera klientorganisationer för New-AzVM</span><span class="sxs-lookup"><span data-stu-id="71536-1777">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="71536-1778">Lägg till "Spot" till argumentslutföraren i prioritetsparametern i cmdletarna New-AzVM, New-AzVMConfig och New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="71536-1778">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="71536-1779">Lägg till parametrarna DiskIOPSReadWrite och DiskMBpsReadWrite till cmdleten Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="71536-1779">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="71536-1780">Ändra parametern SourceImageId för cmdleten New-AzGalleryImageVersion till valfri</span><span class="sxs-lookup"><span data-stu-id="71536-1780">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="71536-1781">Lägg till parametrarna OSDiskImage och DataDiskImage till cmdleten New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="71536-1781">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="71536-1782">Lägg till parametern HyperVGeneration till cmdleten New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="71536-1782">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="71536-1783">Lägg till parametern SkipExtensionsOnOverprovisionedVMs till cmdletarna New-AzVmss, New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="71536-1783">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="71536-1784">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="71536-1784">Az.DataBoxEdge</span></span>
* <span data-ttu-id="71536-1785">Cmdleten `Get-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-1785">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="71536-1786">Hämta ordning</span><span class="sxs-lookup"><span data-stu-id="71536-1786">Get the Order</span></span>
* <span data-ttu-id="71536-1787">Cmdleten `New-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-1787">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="71536-1788">Skapa ny ordning</span><span class="sxs-lookup"><span data-stu-id="71536-1788">Create new Order</span></span>
* <span data-ttu-id="71536-1789">Cmdleten `Remove-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-1789">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="71536-1790">Ta bort ordning</span><span class="sxs-lookup"><span data-stu-id="71536-1790">Remove the Order</span></span>
* <span data-ttu-id="71536-1791">Cmdleten `New-AzDataBoxEdgeShare` har ändrats</span><span class="sxs-lookup"><span data-stu-id="71536-1791">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="71536-1792">Nu skapas lokal filresurs</span><span class="sxs-lookup"><span data-stu-id="71536-1792">Now creates Local Share</span></span>
* <span data-ttu-id="71536-1793">Cmdleten `Set-AzDataBoxEdgeRole` har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-1793">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="71536-1794">Nu kan IotRole mappas till filresursen</span><span class="sxs-lookup"><span data-stu-id="71536-1794">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="71536-1795">Cmdleten `Invoke-AzDataBoxEdgeDevice` har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-1795">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="71536-1796">Anropa genomsökningsuppdatering, ladda ned uppdatering, installera uppdateringar på enheten</span><span class="sxs-lookup"><span data-stu-id="71536-1796">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="71536-1797">Cmdleten `Get-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-1797">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="71536-1798">Hämtar information om utlösare</span><span class="sxs-lookup"><span data-stu-id="71536-1798">Gets the information about Triggers</span></span>
* <span data-ttu-id="71536-1799">Cmdleten `New-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-1799">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="71536-1800">Skapa nya utlösare</span><span class="sxs-lookup"><span data-stu-id="71536-1800">Create new Triggers</span></span>
* <span data-ttu-id="71536-1801">Cmdleten `Remove-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-1801">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="71536-1802">Ta bort utlösare</span><span class="sxs-lookup"><span data-stu-id="71536-1802">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="71536-1803">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="71536-1803">Az.DataFactory</span></span>
* <span data-ttu-id="71536-1804">Uppdatera ADF .Net SDK-versionen till 4.4.0</span><span class="sxs-lookup"><span data-stu-id="71536-1804">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="71536-1805">Lägg till parametern ExpressCustomSetup för kommandot Set-AzureRmDataFactoryV2IntegrationRuntime för att aktivera installationskonfigurationer och komponenter från tredje part utan anpassat konfigurationsskript.</span><span class="sxs-lookup"><span data-stu-id="71536-1805">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="71536-1806">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="71536-1806">Az.DataLakeStore</span></span>
* <span data-ttu-id="71536-1807">Uppdatera dokumentation för Get-AzDataLakeStoreDeletedItem och Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="71536-1807">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="71536-1808">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="71536-1808">Az.EventHub</span></span>
* <span data-ttu-id="71536-1809">Korrigering av problem #10301: Korrigera datumformat för SAS-token</span><span class="sxs-lookup"><span data-stu-id="71536-1809">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="71536-1810">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="71536-1810">Az.FrontDoor</span></span>
* <span data-ttu-id="71536-1811">Lägg till parametern MinimumTlsVersion till Enable-AzFrontDoorCustomDomainHttps och New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="71536-1811">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="71536-1812">Lägg till parametrarna HealthProbeMethod och EnabledState till New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="71536-1812">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="71536-1813">Lägg till en ny cmdlet för att skapa BackendPoolsSettings-objekt som passar i skapande/uppdatering av Front Door</span><span class="sxs-lookup"><span data-stu-id="71536-1813">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="71536-1814">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="71536-1814">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71536-1815">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71536-1815">Az.Network</span></span>
* <span data-ttu-id="71536-1816">Ändra alternativexemplen Start-AzVirtualNetworkGatewayConnectionPacketCapture.md och Start-AzVirtualnetworkGatewayPacketCapture.md för FilterData.</span><span class="sxs-lookup"><span data-stu-id="71536-1816">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="71536-1817">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="71536-1817">Az.PrivateDns</span></span>
* <span data-ttu-id="71536-1818">Uppdaterade PrivateDns .NET SDK till version 1.0.0</span><span class="sxs-lookup"><span data-stu-id="71536-1818">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="71536-1819">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="71536-1819">Az.RecoveryServices</span></span>
* <span data-ttu-id="71536-1820">Stöd för att välja disktyp vid aktivering av skydd i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="71536-1820">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="71536-1821">Korrigering av bugg för åtgärdsredigering av återställningsplan i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="71536-1821">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="71536-1822">Återställningsstöd för att godkänna filestream-databaser i Azure Backup SQL.</span><span class="sxs-lookup"><span data-stu-id="71536-1822">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="71536-1823">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="71536-1823">Az.RedisCache</span></span>
* <span data-ttu-id="71536-1824">Parametern MinimumTlsVersion har lagts till i cmdletarna New-AzRedisCache och Set-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="71536-1824">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="71536-1825">Dessutom har MinimumTlsVersion lagts till i utdata för cmdleten Get-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="71536-1825">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="71536-1826">Verifiering har lagts till på parametern -Size i cmdletarna Set-AzRedisCache och New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="71536-1826">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="71536-1827">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71536-1827">Az.Resources</span></span>
- <span data-ttu-id="71536-1828">Uppdaterade policy-cmdletar för att använda den nya API-versionen 2019-06-01 som har en ny EnforcementMode-egenskap i policytilldelningen.</span><span class="sxs-lookup"><span data-stu-id="71536-1828">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="71536-1829">Uppdaterade hjälpexempel för skapandet av policydefinition</span><span class="sxs-lookup"><span data-stu-id="71536-1829">Updated create policy definition help example</span></span>
- <span data-ttu-id="71536-1830">Åtgärda bugg i Remove-AZADServicePrincipal -ServicePrincipalName, utlös null-referens när tjänstens huvudnamn inte hittas.</span><span class="sxs-lookup"><span data-stu-id="71536-1830">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="71536-1831">Åtgärda bugg i New-AZADServicePrincipal, utlös null-referens när klientorganisationen inte har någon prenumeration.</span><span class="sxs-lookup"><span data-stu-id="71536-1831">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="71536-1832">Ändra New-AzAdServicePrincipal för att endast lägga till autentiseringsuppgifter för det associerade programmet.</span><span class="sxs-lookup"><span data-stu-id="71536-1832">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="71536-1833">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71536-1833">Az.Sql</span></span>
* <span data-ttu-id="71536-1834">Stöd har lagts till för databasen ReadReplicaCount.</span><span class="sxs-lookup"><span data-stu-id="71536-1834">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="71536-1835">Korrigerade Set-AzSqlDatabase när zonredundans inte har angetts</span><span class="sxs-lookup"><span data-stu-id="71536-1835">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="71536-1836">3.0.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="71536-1836">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="71536-1837">Allmänt</span><span class="sxs-lookup"><span data-stu-id="71536-1837">General</span></span>
* <span data-ttu-id="71536-1838">Az. PrivateDns 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="71536-1838">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="71536-1839">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="71536-1839">Az.Accounts</span></span>
* <span data-ttu-id="71536-1840">Lägg till ett utfasningsmeddelande för aliaset Resolve-error.</span><span class="sxs-lookup"><span data-stu-id="71536-1840">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="71536-1841">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="71536-1841">Az.Advisor</span></span>
* <span data-ttu-id="71536-1842">Den nya kategorin Operational Excellence har lagts till i cmdleten Get-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="71536-1842">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="71536-1843">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="71536-1843">Az.Batch</span></span>
* <span data-ttu-id="71536-1844">`CoreQuota` på `BatchAccountContext` har bytt namn till `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="71536-1844">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="71536-1845">Det finns även en ny `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="71536-1845">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="71536-1846">Detta påverkar **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="71536-1846">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="71536-1847">**New-AzBatchTask** `-ResourceFile`-parametern tar nu en samling `PSResourceFile`-objekt som kan skapas med hjälp av den nya cmdleten **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="71536-1847">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="71536-1848">Ny **New-AzBatchResourceFile**-cmdlet för att skapa `PSResourceFile`-objekt.</span><span class="sxs-lookup"><span data-stu-id="71536-1848">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="71536-1849">Dessa kan tillhandahållas till **New-AzBatchTask** på `-ResourceFile`-parametern.</span><span class="sxs-lookup"><span data-stu-id="71536-1849">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="71536-1850">Detta stöder två nya typer av resursfiler förutom det befintliga sättet med `HttpUrl`:</span><span class="sxs-lookup"><span data-stu-id="71536-1850">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="71536-1851">`AutoStorageContainerName`-baserade resursfiler laddar ned en hel container för automatisk lagring till Batch-noden.</span><span class="sxs-lookup"><span data-stu-id="71536-1851">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="71536-1852">`StorageContainerUrl`-baserade resursfiler laddar ned containern som anges i webbadressen till Batch-noden.</span><span class="sxs-lookup"><span data-stu-id="71536-1852">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="71536-1853">Tog bort egenskapen `ApplicationPackages` för `PSApplication` som returnerades av **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="71536-1853">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="71536-1854">Specifika paket i ett program kan nu hämtas med hjälp av **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="71536-1854">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="71536-1855">Till exempel: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="71536-1855">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="71536-1856">Bytt namn på `ApplicationId` till `ApplicationName` på **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** och **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="71536-1856">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="71536-1857">`ApplicationId` är nu ett alias för `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="71536-1857">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="71536-1858">Ny `PSWindowsUserConfiguration`-egenskap till `PSUserAccount` lades till.</span><span class="sxs-lookup"><span data-stu-id="71536-1858">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="71536-1859">Bytte namn på `Version` till `Name` på `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="71536-1859">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="71536-1860">Bytte namn på `BlobSource` till `HttpUrl` på `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="71536-1860">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="71536-1861">Tog bort egenskapen `OSDisk` från `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="71536-1861">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="71536-1862">Tog bort **Set-AzBatchPoolOSVersion**.</span><span class="sxs-lookup"><span data-stu-id="71536-1862">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="71536-1863">Den här åtgärden stöds inte längre.</span><span class="sxs-lookup"><span data-stu-id="71536-1863">This operation is no longer supported.</span></span>
* <span data-ttu-id="71536-1864">`TargetOSVersion` har tagits bort från `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="71536-1864">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="71536-1865">Bytte namn på `CurrentOSVersion` till `OSVersion` på `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="71536-1865">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="71536-1866">`DataEgressGiB` och `DataIngressGiB` har tagits bort från `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="71536-1866">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="71536-1867">Tog bort **Get-AzBatchNodeAgentSku** och ersatte det med **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="71536-1867">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="71536-1868">**Get-AzBatchSupportedImage** returnerar samma data som **Get-AzBatchNodeAgentSku** men i ett mer användarvänligt format.</span><span class="sxs-lookup"><span data-stu-id="71536-1868">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="71536-1869">Nya icke-verifierade avbildningar returneras nu också.</span><span class="sxs-lookup"><span data-stu-id="71536-1869">New non-verified images are also now returned.</span></span> <span data-ttu-id="71536-1870">Ytterligare information om `Capabilities` och `BatchSupportEndOfLife` för varje avbildning inkluderas också.</span><span class="sxs-lookup"><span data-stu-id="71536-1870">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="71536-1871">Lade till möjlighet att montera fjärrfilsystem på varje nod i en pool via den nya parametern `MountConfiguration` för **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="71536-1871">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="71536-1872">Har nu stöd för nätverkssäkerhetsregler som blockerar nätverksåtkomst till en pool baserat på källportens trafik.</span><span class="sxs-lookup"><span data-stu-id="71536-1872">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="71536-1873">Detta görs via egenskapen `SourcePortRanges` på `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="71536-1873">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="71536-1874">När du kör en container stöder nu Batch körningen av uppgiften i arbetskatalogen för containern eller i arbetskatalogen för Batch-uppgiften.</span><span class="sxs-lookup"><span data-stu-id="71536-1874">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="71536-1875">Detta styrs av egenskapen `WorkingDirectory` på `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="71536-1875">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="71536-1876">Lade till en funktion för att ange en samling av offentliga IP-adresser på `PSNetworkConfiguration` via den nya egenskapen `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="71536-1876">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="71536-1877">Detta garanterar att noderna i poolen har en IP-adress från listan över IP-adresser som tillhandahållits av användare.</span><span class="sxs-lookup"><span data-stu-id="71536-1877">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="71536-1878">Om inget värde anges är standardvärdet för `WaitForSuccess` på `PSSTartTask` nu `$True` (var tidigare `$False`).</span><span class="sxs-lookup"><span data-stu-id="71536-1878">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="71536-1879">Om inget värde anges är standardvärdet för `Scope` på `PSAutoUserSpecification` nu `Pool` (var tidigare `Task` på Windows och `Pool` på Linux).</span><span class="sxs-lookup"><span data-stu-id="71536-1879">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="71536-1880">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="71536-1880">Az.Cdn</span></span>
* <span data-ttu-id="71536-1881">Introducerade UrlRewriteAction och CacheKeyQueryStringAction till RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="71536-1881">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="71536-1882">Åtgärdade flera buggar, som saknade indata för ”väljare” i cmdleten New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="71536-1882">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71536-1883">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71536-1883">Az.Compute</span></span>
* <span data-ttu-id="71536-1884">Funktion för diskkrypteringsuppsättning</span><span class="sxs-lookup"><span data-stu-id="71536-1884">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="71536-1885">Nya cmdletar:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="71536-1885">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="71536-1886">Parametern DiskEncryptionSetId har lagts till i följande cmdletar:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="71536-1886">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="71536-1887">Parametrarna DiskEncryptionSetId och EncryptionType har lagts till i följande cmdletar:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="71536-1887">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="71536-1888">Lägg till parametern PublicIPAddressVersion i New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="71536-1888">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="71536-1889">Flytta FileUris för anpassat skripttillägg från offentlig inställning till skyddad inställning</span><span class="sxs-lookup"><span data-stu-id="71536-1889">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="71536-1890">Lägg till ScaleInPolicy i cmdletarna New-AzVmss, New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="71536-1890">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="71536-1891">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="71536-1891">Breaking changes</span></span>
    - <span data-ttu-id="71536-1892">Parametern UploadSizeInBytes används istället för DiskSizeGB för New-AzDiskConfig när CreateOption är Uppladdning</span><span class="sxs-lookup"><span data-stu-id="71536-1892">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="71536-1893">PublishingProfile.Source.ManagedImage.Id ersätts med StorageProfile.Source.Id i objektet GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="71536-1893">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="71536-1894">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="71536-1894">Az.DataFactory</span></span>
* <span data-ttu-id="71536-1895">Uppdatera ADF .Net SDK-versionen till 4.3.0</span><span class="sxs-lookup"><span data-stu-id="71536-1895">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="71536-1896">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="71536-1896">Az.DataLakeStore</span></span>
* <span data-ttu-id="71536-1897">Uppdatera ADLS SDK-version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) innehåller följande korrigeringar</span><span class="sxs-lookup"><span data-stu-id="71536-1897">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="71536-1898">Undvik att utlösa undantag när det inte går att deserialisera creationtime för inmatning av papperskorg eller katalog.</span><span class="sxs-lookup"><span data-stu-id="71536-1898">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="71536-1899">Gör inställning tillgänglig per tidsgräns för förfrågan i adlsclient</span><span class="sxs-lookup"><span data-stu-id="71536-1899">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="71536-1900">Korrigera överföringen av ursprunglig syncflag för badoffset-återställning</span><span class="sxs-lookup"><span data-stu-id="71536-1900">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="71536-1901">Korrigera EnumerateDirectory för att hämta fortsättningstoken när svar har kontrollerats</span><span class="sxs-lookup"><span data-stu-id="71536-1901">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="71536-1902">Korrigera bugg i Concat</span><span class="sxs-lookup"><span data-stu-id="71536-1902">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="71536-1903">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="71536-1903">Az.FrontDoor</span></span>
* <span data-ttu-id="71536-1904">Åtgärdade diverse stavfel i modul</span><span class="sxs-lookup"><span data-stu-id="71536-1904">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="71536-1905">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="71536-1905">Az.HDInsight</span></span>
* <span data-ttu-id="71536-1906">Korrigerade buggen att kunder får felet ”inte en giltig Base-64-sträng” vid användning av Get-AzHDInsightCluster för att hämta klustret med ADLSGen1-lagring.</span><span class="sxs-lookup"><span data-stu-id="71536-1906">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="71536-1907">Lägg till en parameter med namnet ”ApplicationId” i de tre cmdletarna Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig och New-AzHDInsightCluster så att kunden kan tillhandahålla tjänstens huvudnamn för program-ID för åtkomst till Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="71536-1907">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="71536-1908">Ändrade Microsoft.Azure.Management.HDInsight från 2.1.0 till 5.1.0</span><span class="sxs-lookup"><span data-stu-id="71536-1908">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="71536-1909">Fem cmdletar har tagits bort:</span><span class="sxs-lookup"><span data-stu-id="71536-1909">Removed five cmdlets:</span></span>
    - <span data-ttu-id="71536-1910">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="71536-1910">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="71536-1911">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="71536-1911">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="71536-1912">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="71536-1912">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="71536-1913">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="71536-1913">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="71536-1914">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="71536-1914">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="71536-1915">Tre cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="71536-1915">Added three cmdlets:</span></span>
    - <span data-ttu-id="71536-1916">Get-AzHDInsightMonitoring som ersätter Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="71536-1916">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="71536-1917">Enable-AzHDInsightMonitoring som ersätter Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="71536-1917">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="71536-1918">Disable-AzHDInsightMonitoring som ersätter Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="71536-1918">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="71536-1919">Korrigerade cmdleten Get-AzHDInsightProperties för att stödja hämtning av funktionsinformation från en viss plats.</span><span class="sxs-lookup"><span data-stu-id="71536-1919">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="71536-1920">Parameteruppsättningarna (Spark1 och Spark2) har tagits bort från Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="71536-1920">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="71536-1921">Lägg till exempel för cmdleten Add-AzHDInsightSecurityProfile till hjälpdokumenten.</span><span class="sxs-lookup"><span data-stu-id="71536-1921">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="71536-1922">Ändrade utdatatyp för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="71536-1922">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="71536-1923">Ändrade utdatatyp för Get-AzHDInsightProperties från CapabilitiesResponse till AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="71536-1923">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="71536-1924">Ändrade utdatatyp för Remove-AzHDInsightCluster från ClusterGetResponse till bool.</span><span class="sxs-lookup"><span data-stu-id="71536-1924">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="71536-1925">Ändrade utdatatyp för Set-AzHDInsightGatewaySettings HttpConnectivitySettings till GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="71536-1925">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="71536-1926">Lade till testfall för vissa scenarier.</span><span class="sxs-lookup"><span data-stu-id="71536-1926">Added some scenario test cases.</span></span>
* <span data-ttu-id="71536-1927">Ta bort vissa alias: Add-AzHDInsightConfigValues, Get-AzHDInsightProperties.</span><span class="sxs-lookup"><span data-stu-id="71536-1927">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="71536-1928">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="71536-1928">Az.IotHub</span></span>
* <span data-ttu-id="71536-1929">Icke-bakåtkompatibla ändringar:</span><span class="sxs-lookup"><span data-stu-id="71536-1929">Breaking changes:</span></span>
    - <span data-ttu-id="71536-1930">Cmdleten Add-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="71536-1930">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="71536-1931">Parameteruppsättningen __AllParameterSets för cmdleten Add-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="71536-1931">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="71536-1932">Cmdleten Get-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="71536-1932">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="71536-1933">Parameteruppsättningen __AllParameterSets för cmdleten Get-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="71536-1933">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="71536-1934">Egenskapen OperationsMonitoringProperties av typen Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="71536-1934">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="71536-1935">Egenskapen OperationsMonitoringProperties av typen Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="71536-1935">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="71536-1936">Cmdleten New-AzIotHubExportDevice stöder inte längre aliaset New-AzIotHubExportDevices.</span><span class="sxs-lookup"><span data-stu-id="71536-1936">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="71536-1937">Cmdleten New-AzIotHubImportDevice stöder inte längre aliaset New-AzIotHubImportDevices.</span><span class="sxs-lookup"><span data-stu-id="71536-1937">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="71536-1938">Cmdleten Remove-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="71536-1938">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="71536-1939">Parameteruppsättningen __AllParameterSets för cmdleten Remove-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="71536-1939">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="71536-1940">Cmdleten Set-AzIotHub har inte längre stöd för parametern OperationsMonitoringProperties och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="71536-1940">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="71536-1941">Parameteruppsättningen UpdateOperationsMonitoringProperties för cmdleten Set-AzIotHub har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="71536-1941">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="71536-1942">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="71536-1942">Az.RecoveryServices</span></span>
* <span data-ttu-id="71536-1943">Azure Site Recovery-stöd för att konfigurera nätverksresurser som NSG, offentliga IP-adresser och interna lastbalanserare för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="71536-1943">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="71536-1944">Azure Site Recovery-stöd för att skriva till hanterad disk för vMWare till Azure.</span><span class="sxs-lookup"><span data-stu-id="71536-1944">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="71536-1945">Azure Site Recovery-stöd för NIC-reduktion för vMWare till Azure.</span><span class="sxs-lookup"><span data-stu-id="71536-1945">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="71536-1946">Azure Site Recovery-stöd för accelererat nätverk för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="71536-1946">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="71536-1947">Azure Site Recovery-stöd för automatisk uppdatering av agent för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="71536-1947">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="71536-1948">Azure Site Recovery-stöd för Standard SSD för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="71536-1948">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="71536-1949">Azure Site Recovery-stöd för tvåstegskryptering i Azure Disk Encryption för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="71536-1949">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="71536-1950">Azure Site Recovery-stöd för att skydda nyligen tillagda diskar för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="71536-1950">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="71536-1951">En funktion för mjuk borttagning av virtuella datorer samt tester för mjuk borttagning har tagits bort</span><span class="sxs-lookup"><span data-stu-id="71536-1951">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="71536-1952">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71536-1952">Az.Resources</span></span>
* <span data-ttu-id="71536-1953">Uppdatera beroendesammansättning för Microsoft.Extensions.Caching.Memory från 1.1.1 till 2.2</span><span class="sxs-lookup"><span data-stu-id="71536-1953">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71536-1954">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71536-1954">Az.Network</span></span>
* <span data-ttu-id="71536-1955">Ändra alla cmdletar för PrivateEndpointConnection så att de stöder generiska tjänstleverantörer.</span><span class="sxs-lookup"><span data-stu-id="71536-1955">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="71536-1956">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="71536-1956">Updated cmdlet:</span></span>
        - <span data-ttu-id="71536-1957">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="71536-1957">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="71536-1958">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="71536-1958">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="71536-1959">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="71536-1959">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="71536-1960">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="71536-1960">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="71536-1961">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="71536-1961">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="71536-1962">Lägg till ny cmdlet för PrivateLinkResource så att det också stöder generiska tjänstleverantörer.</span><span class="sxs-lookup"><span data-stu-id="71536-1962">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="71536-1963">Ny cmdlet:</span><span class="sxs-lookup"><span data-stu-id="71536-1963">New cmdlet:</span></span>
        - <span data-ttu-id="71536-1964">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="71536-1964">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="71536-1965">Lägg till nya fält och parametrar för funktionen Proxy Protocol V2.</span><span class="sxs-lookup"><span data-stu-id="71536-1965">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="71536-1966">Lägg till egenskapen EnableProxyProtocol i PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="71536-1966">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="71536-1967">Lägg till egenskapen LinkIdentifier i PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="71536-1967">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="71536-1968">Uppdaterade New-AzPrivateLinkService för att lägga till den nya valfria parametern EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="71536-1968">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="71536-1969">Korrigera felaktig beskrivning av parameter i referensdokumentationen för New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="71536-1969">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="71536-1970">Nya cmdletar som stöder Azure-brandväggsprincipen</span><span class="sxs-lookup"><span data-stu-id="71536-1970">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="71536-1971">Lägg till stöd för den underordnade resursen RouteTables för VirtualHub</span><span class="sxs-lookup"><span data-stu-id="71536-1971">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="71536-1972">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="71536-1972">New cmdlets added:</span></span>
        - <span data-ttu-id="71536-1973">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="71536-1973">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="71536-1974">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="71536-1974">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="71536-1975">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="71536-1975">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="71536-1976">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="71536-1976">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="71536-1977">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="71536-1977">Set-AzVirtualHub</span></span>
* <span data-ttu-id="71536-1978">Lägg till stöd för ny egenskaps-SKU för VirtualHub och VirtualWANType för VirtualWan</span><span class="sxs-lookup"><span data-stu-id="71536-1978">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="71536-1979">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="71536-1979">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="71536-1980">New-AzVirtualHub: lade till parameter-SKU</span><span class="sxs-lookup"><span data-stu-id="71536-1980">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="71536-1981">Update-AzVirtualHub: lade till parameter-SKU</span><span class="sxs-lookup"><span data-stu-id="71536-1981">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="71536-1982">New-AzVirtualWan: lade till parametern VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="71536-1982">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="71536-1983">Update-AzVirtualWan: lade till parametern VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="71536-1983">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="71536-1984">Lägg till stöd för egenskapen EnableInternetSecurity för HubVnetConnection, VpnConnection och ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="71536-1984">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="71536-1985">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="71536-1985">New cmdlets added:</span></span>
        - <span data-ttu-id="71536-1986">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="71536-1986">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="71536-1987">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="71536-1987">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="71536-1988">New-AzureRmVirtualHubVnetConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-1988">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="71536-1989">New-AzureRmVpnConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-1989">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="71536-1990">Update-AzureRmVpnConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-1990">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="71536-1991">New-AzureRmExpressRouteConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-1991">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="71536-1992">Set-AzureRmExpressRouteConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-1992">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="71536-1993">Lägg till stöd för att konfigurera TopLevel WebApplicationFirewall-princip</span><span class="sxs-lookup"><span data-stu-id="71536-1993">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="71536-1994">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="71536-1994">New cmdlets added:</span></span>
        - <span data-ttu-id="71536-1995">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="71536-1995">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="71536-1996">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="71536-1996">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="71536-1997">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="71536-1997">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="71536-1998">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="71536-1998">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="71536-1999">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="71536-1999">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="71536-2000">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="71536-2000">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="71536-2001">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="71536-2001">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="71536-2002">New-AzApplicationGatewayFirewallPolicy: parametrarna PolicySetting, ManagedRule har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-2002">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="71536-2003">Stöd för operator för geomatchning har lagts till på CustomRule</span><span class="sxs-lookup"><span data-stu-id="71536-2003">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="71536-2004">Geomatchning har lagts till i operatorn på FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="71536-2004">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="71536-2005">Stöd har lagts till för brandväggsprinciperna perListener och perSite</span><span class="sxs-lookup"><span data-stu-id="71536-2005">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="71536-2006">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="71536-2006">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="71536-2007">New-AzApplicationGatewayHttpListener: parametrarna FirewallPolicy, FirewallPolicyId har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-2007">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="71536-2008">New-AzApplicationGatewayPathRuleConfig: parametrarna FirewallPolicy, FirewallPolicyId har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-2008">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="71536-2009">Åtgärdat så att nödvändigt undernät med namnet AzureBastionSubnet i PSBastion kan vara skiftlägesokänsligt</span><span class="sxs-lookup"><span data-stu-id="71536-2009">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="71536-2010">Stöd för mål-FQDN:er i nätverksregler och översatt FQDN i NAT-regler för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="71536-2010">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="71536-2011">Lägg till stöd för resursen RouteTables för IpGroup på den högsta nivån</span><span class="sxs-lookup"><span data-stu-id="71536-2011">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="71536-2012">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="71536-2012">New cmdlets added:</span></span>
        - <span data-ttu-id="71536-2013">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="71536-2013">New-AzIpGroup</span></span>
        - <span data-ttu-id="71536-2014">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="71536-2014">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="71536-2015">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="71536-2015">Get-AzIpGroup</span></span>
        - <span data-ttu-id="71536-2016">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="71536-2016">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="71536-2017">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="71536-2017">Az.ServiceFabric</span></span>
* <span data-ttu-id="71536-2018">Ta bort cmdleten Add-AzServiceFabricApplicationCertificate eftersom det här scenariot omfattas av Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="71536-2018">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="71536-2019">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71536-2019">Az.Sql</span></span>
* <span data-ttu-id="71536-2020">Stöd har lagts till för återställning av utelämnade databaser på hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="71536-2020">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="71536-2021">Inaktuella gamla cmdletar för granskning från kod.</span><span class="sxs-lookup"><span data-stu-id="71536-2021">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="71536-2022">Tog bort inaktuella alias:</span><span class="sxs-lookup"><span data-stu-id="71536-2022">Removed deprecated aliases:</span></span>
* <span data-ttu-id="71536-2023">Get-AzSqlDatabaseIndexRecommendations (använd Get-AzSqlDatabaseIndexRecommendation istället)</span><span class="sxs-lookup"><span data-stu-id="71536-2023">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="71536-2024">Get-AzSqlDatabaseRestorePoints (använd Get-AzSqlDatabaseRestorePoint istället)</span><span class="sxs-lookup"><span data-stu-id="71536-2024">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="71536-2025">Ta bort cmdleten Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="71536-2025">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="71536-2026">Ta bort alias för inaktuella cmdletar för inställningar för utvärdering av säkerhetsrisk</span><span class="sxs-lookup"><span data-stu-id="71536-2026">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="71536-2027">Inaktualisera cmdletar för inställningar för avancerad hotidentifiering</span><span class="sxs-lookup"><span data-stu-id="71536-2027">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="71536-2028">Lägga till cmdletar för att inaktivera och aktivera känslighetsrekommendationer på kolumner i en databas.</span><span class="sxs-lookup"><span data-stu-id="71536-2028">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="71536-2029">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="71536-2029">Az.Storage</span></span>
* <span data-ttu-id="71536-2030">Stöd för att aktivera stora filresurser vid skapande eller uppdatering av lagringskonto</span><span class="sxs-lookup"><span data-stu-id="71536-2030">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="71536-2031">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="71536-2031">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="71536-2032">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="71536-2032">Set-AzStorageAccount</span></span>
* <span data-ttu-id="71536-2033">När du stänger/hämtar en filreferens kan du hoppa över kontrollen av huruvida indatasökvägen är en filkatalog eller en fil för att undvika problem med objekt som har status DeletePending</span><span class="sxs-lookup"><span data-stu-id="71536-2033">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="71536-2034">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="71536-2034">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="71536-2035">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="71536-2035">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="71536-2036">2.8.0 – oktober 2019</span><span class="sxs-lookup"><span data-stu-id="71536-2036">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="71536-2037">Allmänt</span><span class="sxs-lookup"><span data-stu-id="71536-2037">General</span></span>
* <span data-ttu-id="71536-2038">AZ. HealthcareApis 1.0.0-version</span><span class="sxs-lookup"><span data-stu-id="71536-2038">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="71536-2039">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="71536-2039">Az.Accounts</span></span>
* <span data-ttu-id="71536-2040">Uppdatera telemetri och URL-omskrivning för genererade moduler, korrigera Windows-enhetstester.</span><span class="sxs-lookup"><span data-stu-id="71536-2040">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="71536-2041">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="71536-2041">Az.ApiManagement</span></span>
* <span data-ttu-id="71536-2042">**Set-AzApiManagementApi** – Tillagt stöd för att uppdatera Api till ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="71536-2042">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="71536-2043">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="71536-2043">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="71536-2044">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="71536-2044">Az.Automation</span></span>
* <span data-ttu-id="71536-2045">Åtgärdade cmdleten New-AzureAutomationSoftwareUpdateConfiguration för parametern för inställning av Linux-omstart.</span><span class="sxs-lookup"><span data-stu-id="71536-2045">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="71536-2046">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="71536-2046">Az.Batch</span></span>
* <span data-ttu-id="71536-2047">**Get-AzBatchNodeAgentSku** är inaktuell och ersätts av **Get-AzBatchSupportImage** i version 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="71536-2047">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71536-2048">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71536-2048">Az.Compute</span></span>
* <span data-ttu-id="71536-2049">Lägg till parametrarna Priority, EvictionPolicy och MaxPrice till cmdletarna New-AzVM och New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="71536-2049">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="71536-2050">Korrigera varningsmeddelande och hjälpdokument för cmdletarna Add-AzVMAdditionalUnattendContent och Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="71536-2050">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="71536-2051">Åtgärda – skipVmBackup-undantag för virtuella Linux-datorer med hanterade diskar för Set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="71536-2051">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="71536-2052">Åtgärda fel i uppdatera krypteringsinställningarna i set-AzVMDiskEncryptionExtension, scenario i två steg.</span><span class="sxs-lookup"><span data-stu-id="71536-2052">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="71536-2053">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="71536-2053">Az.DataFactory</span></span>
* <span data-ttu-id="71536-2054">Lägga till CRUD-kommandon för ADF V2-dataflödet: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow och Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="71536-2054">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="71536-2055">Lägger till åtgärdskommandon för ADF V2-dataflödesfelsökningssession: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand och Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="71536-2055">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="71536-2056">Uppdatera ADF .Net SDK-versionen till 4.2.0</span><span class="sxs-lookup"><span data-stu-id="71536-2056">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="71536-2057">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="71536-2057">Az.DataLakeStore</span></span>
* <span data-ttu-id="71536-2058">Korrigera kontovalidering så att konton med ”-” kan skickas utan domän</span><span class="sxs-lookup"><span data-stu-id="71536-2058">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="71536-2059">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="71536-2059">Az.HealthcareApis</span></span>
* <span data-ttu-id="71536-2060">PowerShell-versionen har uppdaterats till 1.0.0</span><span class="sxs-lookup"><span data-stu-id="71536-2060">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="71536-2061">Uppdaterade SDK-versionen till 1.0.2</span><span class="sxs-lookup"><span data-stu-id="71536-2061">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="71536-2062">Uppdatera i tester för att referera till en ny SDK-version</span><span class="sxs-lookup"><span data-stu-id="71536-2062">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="71536-2063">Utdatastrukturen har uppdaterats från kapslad till förenklad.</span><span class="sxs-lookup"><span data-stu-id="71536-2063">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="71536-2064">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="71536-2064">Az.IotHub</span></span>
* <span data-ttu-id="71536-2065">Lägg till ny routningskälla: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="71536-2065">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="71536-2066">Mindre felkorrigering: Get-AzIothub returnerar inte subscriptionId</span><span class="sxs-lookup"><span data-stu-id="71536-2066">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="71536-2067">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="71536-2067">Az.Monitor</span></span>
* <span data-ttu-id="71536-2068">Nya åtgärdsgruppsmottagare har lagts till för åtgärdsgrupp   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="71536-2068">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="71536-2069">Använd vanligt aviseringsschema som är aktiverat för mottagarna.</span><span class="sxs-lookup"><span data-stu-id="71536-2069">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="71536-2070">Detta gäller inte för SMS, push för Azure-app, ITSM och röstmottagare</span><span class="sxs-lookup"><span data-stu-id="71536-2070">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="71536-2071">Webhooks har nu stöd för Azure Active Directory-autentisering.</span><span class="sxs-lookup"><span data-stu-id="71536-2071">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71536-2072">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71536-2072">Az.Network</span></span>
* <span data-ttu-id="71536-2073">Lägg till ny cmdlet Get-AzAvailableServiceAlias som kan anropas för att hämta de alias som kan användas för tjänstslutpunktsprinciper.</span><span class="sxs-lookup"><span data-stu-id="71536-2073">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="71536-2074">Stöd för tillägg av trafikväljare har lagts till i gatewayanslutningar för virtuella nätverk</span><span class="sxs-lookup"><span data-stu-id="71536-2074">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="71536-2075">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="71536-2075">New cmdlets added:</span></span>
        - <span data-ttu-id="71536-2076">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="71536-2076">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="71536-2077">Cmdletar har uppdaterats med valfri parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="71536-2077">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="71536-2078">Lägg till stöd för ESP- och AH-protokoll i konfiguration av nätverkssäkerhetsregler</span><span class="sxs-lookup"><span data-stu-id="71536-2078">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="71536-2079">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="71536-2079">Updated cmdlets:</span></span>
        - <span data-ttu-id="71536-2080">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="71536-2080">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="71536-2081">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="71536-2081">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="71536-2082">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="71536-2082">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="71536-2083">Förbättra hanteringen av undantag i Cortex-cmdletar</span><span class="sxs-lookup"><span data-stu-id="71536-2083">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="71536-2084">Nya generationer och SKU:er för VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="71536-2084">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="71536-2085">Introducera nya generationer för VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="71536-2085">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="71536-2086">Introducera nya SKU:er med högt dataflöde för VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="71536-2086">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="71536-2087">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="71536-2087">Az.RedisCache</span></span>
* <span data-ttu-id="71536-2088">Uppdaterad referensdokumentation för ”set-AzRedisCache” för att inkludera saknade värden för parametern ”size”</span><span class="sxs-lookup"><span data-stu-id="71536-2088">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="71536-2089">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71536-2089">Az.Sql</span></span>
* <span data-ttu-id="71536-2090">Lägg till stöd för inställningen Active Directory administratör på den hanterade instansen</span><span class="sxs-lookup"><span data-stu-id="71536-2090">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="71536-2091">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="71536-2091">Az.Storage</span></span>
* <span data-ttu-id="71536-2092">Uppdatera Lagringsklientbibliotek till 11.1.0</span><span class="sxs-lookup"><span data-stu-id="71536-2092">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="71536-2093">Lista containrar med hanteringsplans-API, kommer att listas med NextPageLink</span><span class="sxs-lookup"><span data-stu-id="71536-2093">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="71536-2094">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="71536-2094">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="71536-2095">Lista lagringskonton från prenumerationen, kommer att listas med NextPageLink</span><span class="sxs-lookup"><span data-stu-id="71536-2095">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="71536-2096">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="71536-2096">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="71536-2097">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="71536-2097">Az.StorageSync</span></span>
* <span data-ttu-id="71536-2098">Åtgärda problemet 9810 i Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="71536-2098">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="71536-2099">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="71536-2099">Az.Websites</span></span>
* <span data-ttu-id="71536-2100">Set-AzWebApp – uppdatering av ASP för en app misslyckades</span><span class="sxs-lookup"><span data-stu-id="71536-2100">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="71536-2101">2.7.0 – september 2019</span><span class="sxs-lookup"><span data-stu-id="71536-2101">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="71536-2102">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="71536-2102">Az.ApiManagement</span></span>
* <span data-ttu-id="71536-2103">Uppdatera ”-Format”-parameterbeskrivningen i ”Set-AzApiManagementPolicy”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="71536-2103">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="71536-2104">Referenser för den föråldrade cmdleten ”Update-AzApiManagementDeployment” har tagits bort från referensdokumentationen.</span><span class="sxs-lookup"><span data-stu-id="71536-2104">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="71536-2105">Använd ”Set-AzApiManagement” i stället.</span><span class="sxs-lookup"><span data-stu-id="71536-2105">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="71536-2106">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="71536-2106">Az.Automation</span></span>
* <span data-ttu-id="71536-2107">Stavfel har korrigerats i exempel i referensdokumentationen för ”Register-AzAutomationDscNode”</span><span class="sxs-lookup"><span data-stu-id="71536-2107">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="71536-2108">Klargörande har lagts till om OS-begränsningar för Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="71536-2108">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="71536-2109">Null-referensundantag har korrigerats för -Wait-alternativet i Start-AzAutomationRunbook-cmdleten.</span><span class="sxs-lookup"><span data-stu-id="71536-2109">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71536-2110">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71536-2110">Az.Compute</span></span>
* <span data-ttu-id="71536-2111">Lägg till UploadSizeInBytes-parameter till New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="71536-2111">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="71536-2112">Lägg till Incremental-parameter till New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="71536-2112">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="71536-2113">Lägg till en funktion för virtuella datorer med låg prioritet:</span><span class="sxs-lookup"><span data-stu-id="71536-2113">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="71536-2114">MaxPrice-, EvictionPolicy- och Priority-parametrar har lagts till i New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="71536-2114">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="71536-2115">MaxPrice-parametern har lagts till i New-AzVmssConfig-, Update-AzVM- och Update-AzVmss-cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="71536-2115">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="71536-2116">Åtgärda problem med VM-referenser för Get-AzAvailabilitySet-cmdleten när alla tillgänglighetsuppsättningar i prenumerationen visas.</span><span class="sxs-lookup"><span data-stu-id="71536-2116">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="71536-2117">Korrigera null-undantaget för Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="71536-2117">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="71536-2118">Korrigera VHD-metoden för sökning relativt till slut.</span><span class="sxs-lookup"><span data-stu-id="71536-2118">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="71536-2119">Åtgärda UltraSSD-problem för New-AzVM och Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="71536-2119">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="71536-2120">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="71536-2120">Az.DataFactory</span></span>
* <span data-ttu-id="71536-2121">Lägger till 3 nya kommandon för ADF V2 – Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription och Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="71536-2121">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="71536-2122">ADF .Net SDK har uppdaterats till 4.1.3</span><span class="sxs-lookup"><span data-stu-id="71536-2122">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="71536-2123">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="71536-2123">Az.HDInsight</span></span>
* <span data-ttu-id="71536-2124">Anrop för icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="71536-2124">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="71536-2125">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="71536-2125">Az.IotHub</span></span>
* <span data-ttu-id="71536-2126">Lägg till stöd för att anropa redundans för en IotHub till den geo-länkade katastrofåterställningsregionen.</span><span class="sxs-lookup"><span data-stu-id="71536-2126">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="71536-2127">Lägg till stöd för att hantera meddelandeberikning för en IotHub.</span><span class="sxs-lookup"><span data-stu-id="71536-2127">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="71536-2128">Nya cmdlet:ar är:</span><span class="sxs-lookup"><span data-stu-id="71536-2128">New cmdlets are:</span></span>
    - <span data-ttu-id="71536-2129">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="71536-2129">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="71536-2130">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="71536-2130">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="71536-2131">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="71536-2131">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="71536-2132">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="71536-2132">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="71536-2133">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="71536-2133">Az.Monitor</span></span>
* <span data-ttu-id="71536-2134">Pekar på den senaste Monitor SDK:n, dvs. 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="71536-2134">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="71536-2135">Lägger till bakåtkompatibla ändringar i Metrics-cmdletarna, dvs. enhetsuppräkningen stöder flera nya värden.</span><span class="sxs-lookup"><span data-stu-id="71536-2135">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="71536-2136">Detta är skrivskyddade cmdletar, så det förekommer inga ändringar i inmatningen för cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="71536-2136">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="71536-2137">API-versionen för **ActionGroups**-begäranden är nu **2019-06-01**. Tidigare var den **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="71536-2137">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="71536-2138">Test av scenarier har uppdaterats för att anpassas till den här ändringen.</span><span class="sxs-lookup"><span data-stu-id="71536-2138">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="71536-2139">Ett nytt obligatoriskt argument har lagts till för konstruktorerna för klasserna **EmailReceiver** och **WebhookReceiver** – ett booleskt värde med namnet **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="71536-2139">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="71536-2140">Värdet är för närvarande fast till **false** så att den här icke-bakåtkompatibla ändringen är dold från cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="71536-2140">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="71536-2141">**Obs!** Det här är en tillfällig ändring som måste verifieras av Alerts-teamet.</span><span class="sxs-lookup"><span data-stu-id="71536-2141">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="71536-2142">Ordningen på argumenten för konstruktorn för klassen **Source** (relaterad till klassen **ScheduledQueryRuleSource**) har ändrats från den tidigare SDK:n.</span><span class="sxs-lookup"><span data-stu-id="71536-2142">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="71536-2143">Den här ändringen krävde korrigering av två enhetstest: de kompilerades, men testerna skickades inte.</span><span class="sxs-lookup"><span data-stu-id="71536-2143">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="71536-2144">Ordningen på argumenten för konstruktorn för klassen **AlertingAction** (relaterad till klassen **ScheduledQueryRuleSource**) har ändrats från den tidigare SDK:n.</span><span class="sxs-lookup"><span data-stu-id="71536-2144">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="71536-2145">Den här ändringen krävde korrigering av två enhetstest: de kompilerades, men testerna skickades inte.</span><span class="sxs-lookup"><span data-stu-id="71536-2145">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="71536-2146">Stöd för kriterier för dynamiskt tröskelvärde för måttavisering v2</span><span class="sxs-lookup"><span data-stu-id="71536-2146">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="71536-2147">New-AzMetricAlertRuleV2Criteria: skapar nu även kriterier för dynamiskt tröskelvärde</span><span class="sxs-lookup"><span data-stu-id="71536-2147">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="71536-2148">Add-AzMetricAlertRuleV2: accepterar nu även kriterier för dynamiskt tröskelvärde</span><span class="sxs-lookup"><span data-stu-id="71536-2148">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="71536-2149">Förbättringar i schemalagd frågeregel (SQR)</span><span class="sxs-lookup"><span data-stu-id="71536-2149">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="71536-2150">Cmdletar accepterar ”Location”-parameter i båda formaten, antingen platsen (t.ex. eastus) eller platsens visningsnamn (t.ex. USA, östra)</span><span class="sxs-lookup"><span data-stu-id="71536-2150">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="71536-2151">”Enabled”-parametern illustreras korrekt i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="71536-2151">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="71536-2152">Exempel för den valfria parametern ”ActionGroup” har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-2152">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="71536-2153">Förbättrade hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="71536-2153">Overall improved help files</span></span>
* <span data-ttu-id="71536-2154">Åtgärda bugg då omfattningstypen fastställs för ”Set-AzActionRule”</span><span class="sxs-lookup"><span data-stu-id="71536-2154">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71536-2155">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71536-2155">Az.Network</span></span>
* <span data-ttu-id="71536-2156">Korrigera felaktigt exempel i referensdokumentationen för ”New-AzApplicationGateway”</span><span class="sxs-lookup"><span data-stu-id="71536-2156">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="71536-2157">Lägg till anmärkning i ”Get-AzNetworkWatcherPacketCapture”-referensdokumentationen om hämtning av alla egenskaper för en paketinsamling</span><span class="sxs-lookup"><span data-stu-id="71536-2157">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="71536-2158">Exempel har korrigerats i ”Test-AzNetworkWatcherIPFlow”-referensdokumentationen för korrekt uppräkning av nätverkskort</span><span class="sxs-lookup"><span data-stu-id="71536-2158">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="71536-2159">Förbättrad tolkning av molnundantag för att visa eventuell ytterligare information</span><span class="sxs-lookup"><span data-stu-id="71536-2159">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="71536-2160">Förbättrad tolkning av molnundantag för att hantera ytterligare en typ av SDK-undantag</span><span class="sxs-lookup"><span data-stu-id="71536-2160">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="71536-2161">Felaktig mappning av säkerhetsregelmodeller har korrigerats</span><span class="sxs-lookup"><span data-stu-id="71536-2161">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="71536-2162">Egenskaper har lagts till för nätverksgränssnittet för funktionen Privat IP</span><span class="sxs-lookup"><span data-stu-id="71536-2162">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="71536-2163">Egenskapen ”PrivateEndpoint” har lagts till som en typ av PSResourceId till PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="71536-2163">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="71536-2164">Egenskapen ”PrivateLinkConnectionProperties” har lagts till som en typ av PSIpConfigurationConnectivityInformation till PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="71536-2164">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="71536-2165">Modellklassen PSIpConfigurationConnectivityInformation har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-2165">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="71536-2166">ApplicationRuleProtocolType ”mssql” har lagts till för Azure Firewall-resurs</span><span class="sxs-lookup"><span data-stu-id="71536-2166">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="71536-2167">MultiLink-stöd i virtuellt WAN</span><span class="sxs-lookup"><span data-stu-id="71536-2167">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="71536-2168">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="71536-2168">New cmdlets</span></span>
        - <span data-ttu-id="71536-2169">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="71536-2169">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="71536-2170">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="71536-2170">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="71536-2171">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="71536-2171">Updated cmdlet:</span></span>
        - <span data-ttu-id="71536-2172">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="71536-2172">New-VpnSite</span></span>
        - <span data-ttu-id="71536-2173">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="71536-2173">Update-VpnSite</span></span>
        - <span data-ttu-id="71536-2174">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="71536-2174">New-VpnConnection</span></span>
        - <span data-ttu-id="71536-2175">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="71536-2175">Update-VpnConnection</span></span>
* <span data-ttu-id="71536-2176">Dokument för vissa PowerShell-exempel har korrigerats så att Az-cmdletar används i stället för AzureRM-cmdletar</span><span class="sxs-lookup"><span data-stu-id="71536-2176">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="71536-2177">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="71536-2177">Az.RecoveryServices</span></span>
* <span data-ttu-id="71536-2178">Uppdatera AzureVMpolicy-objekt med ProtectedItemsCount-attribut</span><span class="sxs-lookup"><span data-stu-id="71536-2178">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="71536-2179">Ytterligare tester har lagts till för VM-princip och återställning av ursprungligt lagringskonto</span><span class="sxs-lookup"><span data-stu-id="71536-2179">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="71536-2180">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71536-2180">Az.Resources</span></span>
* <span data-ttu-id="71536-2181">Åtgärda fel där det inte gick att anropa New-AzRoleAssignment utan parametern Scope.</span><span class="sxs-lookup"><span data-stu-id="71536-2181">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="71536-2182">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="71536-2182">Az.ServiceFabric</span></span>
* <span data-ttu-id="71536-2183">Stavfel har korrigerats i exempel för ”Update-AzServiceFabricReliability”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="71536-2183">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="71536-2184">Lägger till nya cmdletar för att hantera program och tjänster:</span><span class="sxs-lookup"><span data-stu-id="71536-2184">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="71536-2185">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="71536-2185">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="71536-2186">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="71536-2186">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="71536-2187">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="71536-2187">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="71536-2188">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="71536-2188">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="71536-2189">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="71536-2189">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="71536-2190">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="71536-2190">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="71536-2191">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="71536-2191">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="71536-2192">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="71536-2192">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="71536-2193">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="71536-2193">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="71536-2194">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="71536-2194">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="71536-2195">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="71536-2195">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="71536-2196">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="71536-2196">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="71536-2197">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="71536-2197">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="71536-2198">Service Fabric SDK har uppgraderats till version 1.2.0 som använder Service Fabric-resursprovidern med API-version 2019-03-01.</span><span class="sxs-lookup"><span data-stu-id="71536-2198">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="71536-2199">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="71536-2199">Az.SignalR</span></span>
* <span data-ttu-id="71536-2200">Lägg till Update-, Restart-, CheckNameAvailability- och GetUsage-cmdletar</span><span class="sxs-lookup"><span data-stu-id="71536-2200">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="71536-2201">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71536-2201">Az.Sql</span></span>
* <span data-ttu-id="71536-2202">Uppdatera exempel i referensdokumentationen för ”Get-AzSqlElasticPool”</span><span class="sxs-lookup"><span data-stu-id="71536-2202">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="71536-2203">vCore-exempel för att skapa en elastisk pool (New-AzSqlElasticPool) har lagts till.</span><span class="sxs-lookup"><span data-stu-id="71536-2203">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="71536-2204">Ta bort verifieringen av EmailAddresses och kontrollen som bekräftar att EmailAdmins inte är falskt när EmailAddresses är tomt i Set-AzSqlServerAdvancedThreatProtectionPolicy och Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="71536-2204">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="71536-2205">Server-/databasgranskningsinställningar kan tas bort när det finns flera diagnostikinställningar som aktiverar granskningskategorin.</span><span class="sxs-lookup"><span data-stu-id="71536-2205">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="71536-2206">Åtgärda verifiering av e-postadresser i flera Sql Vulnerability Assessment-cmdletar (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting och Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="71536-2206">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="71536-2207">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="71536-2207">Az.Storage</span></span>
* <span data-ttu-id="71536-2208">Exempel i referensdokumentationen för ”Get-AzStorageAccountKey” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="71536-2208">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="71536-2209">Vid upp- och nedladdning av en Azure-fil kan SMB-egenskaperna för källfilen (t.ex. filattribut, tidpunkten då filen skapades och tidpunkten för den senaste skrivningen) sparas i målfilen</span><span class="sxs-lookup"><span data-stu-id="71536-2209">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="71536-2210">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="71536-2210">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="71536-2211">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="71536-2211">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="71536-2212">Korrigera problem med uppladdningen av blockblob med egenskaper/metadata för ImmutabilityPolicy i containrar.</span><span class="sxs-lookup"><span data-stu-id="71536-2212">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="71536-2213">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="71536-2213">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="71536-2214">Stöd för hantering av Azure-filresurser med API för hanteringsplan</span><span class="sxs-lookup"><span data-stu-id="71536-2214">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="71536-2215">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="71536-2215">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="71536-2216">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="71536-2216">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="71536-2217">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="71536-2217">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="71536-2218">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="71536-2218">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="71536-2219">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="71536-2219">Az.Websites</span></span>
* <span data-ttu-id="71536-2220">Åtgärdar problemet där webapp-taggar togs bort när appen migrerades till nya ASP</span><span class="sxs-lookup"><span data-stu-id="71536-2220">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="71536-2221">Åtgärda Publish-AzureWebapp så att det fungerar i Linux och Windows</span><span class="sxs-lookup"><span data-stu-id="71536-2221">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="71536-2222">Uppdatera exempel i ”Get-AzWebAppPublishingProfile”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="71536-2222">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="71536-2223">2.6.0 – augusti 2019</span><span class="sxs-lookup"><span data-stu-id="71536-2223">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="71536-2224">Allmänt</span><span class="sxs-lookup"><span data-stu-id="71536-2224">General</span></span>
* <span data-ttu-id="71536-2225">Åtgärdade diverse skrivfel i flera moduler</span><span class="sxs-lookup"><span data-stu-id="71536-2225">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="71536-2226">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="71536-2226">Az.Accounts</span></span>
* <span data-ttu-id="71536-2227">Stöd för användartilldelat MSI i Azure Functions-autentisering (#9479)</span><span class="sxs-lookup"><span data-stu-id="71536-2227">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="71536-2228">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="71536-2228">Az.Aks</span></span>
* <span data-ttu-id="71536-2229">Åtgärda problem med utdata för "Get-AzAks"</span><span class="sxs-lookup"><span data-stu-id="71536-2229">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="71536-2230">Mer information här: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="71536-2230">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="71536-2231">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="71536-2231">Az.ApiManagement</span></span>
* <span data-ttu-id="71536-2232">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="71536-2232">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="71536-2233">Uppdatera .net-NuGet-versionen, som inte tillämpar begränsningar för productId, apiId och userId</span><span class="sxs-lookup"><span data-stu-id="71536-2233">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="71536-2234">**Get-AzApiManagementProduct** – Lade till stöd för frågekörning mot produkter via API.</span><span class="sxs-lookup"><span data-stu-id="71536-2234">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="71536-2235">**New-AzApiManagementApiRevision** – Korrigering för problem där ApiRevisionDescription inte angavs vid skapande av ny API-revision https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="71536-2235">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="71536-2236">Åtgärdade skrivfel i modellen "PsApiManagementOAuth2AuthrozationServer" till "PsApiManagementOAuth2AuthorizationServer"</span><span class="sxs-lookup"><span data-stu-id="71536-2236">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="71536-2237">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="71536-2237">Az.Batch</span></span>
* <span data-ttu-id="71536-2238">Åtgärdade skrivfel i hjälpmeddelande och dokumentation till att skriva Windows med versaler</span><span class="sxs-lookup"><span data-stu-id="71536-2238">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="71536-2239">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="71536-2239">Az.Cdn</span></span>
* <span data-ttu-id="71536-2240">Åtgärdade skrivfel i CDN-modulens konverteringshjälp</span><span class="sxs-lookup"><span data-stu-id="71536-2240">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71536-2241">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71536-2241">Az.Compute</span></span>
* <span data-ttu-id="71536-2242">Lägg till VmssId i New-AzVMConfig-cmdleten</span><span class="sxs-lookup"><span data-stu-id="71536-2242">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="71536-2243">Lägg till parametrarna TerminateScheduledEvents och TerminateScheduledEventNotBeforeTimeoutInMinutes i New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="71536-2243">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="71536-2244">Lägg till egenskapen HyperVGeneration till avbildningsobjekt för virtuell dator</span><span class="sxs-lookup"><span data-stu-id="71536-2244">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="71536-2245">Lägg till funktioner för Host och HostGroup</span><span class="sxs-lookup"><span data-stu-id="71536-2245">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="71536-2246">Nya cmdletar:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="71536-2246">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="71536-2247">HostId-parametern läggs till i New-AzVMConfig och New-AzVM</span><span class="sxs-lookup"><span data-stu-id="71536-2247">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="71536-2248">Uppdatera exempel i "Invoke-AzVMRunCommand"-dokumentationen till att använda rätt parameternamn</span><span class="sxs-lookup"><span data-stu-id="71536-2248">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="71536-2249">Uppdatera "-VolumeType"-beskrivningen i referensdokumentationen för "set-AzVMDiskEncryptionExtension" och "set-AzVmssDiskEncryptionExtension"</span><span class="sxs-lookup"><span data-stu-id="71536-2249">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="71536-2250">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="71536-2250">Az.DataFactory</span></span>
* <span data-ttu-id="71536-2251">Åtgärda skrivfel till att använda versaler för "Windows" i "New-AzDataFactoryEncryptValue"-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="71536-2251">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="71536-2252">Uppdaterade ADF .Net SDK-versionen till 4.1.2</span><span class="sxs-lookup"><span data-stu-id="71536-2252">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="71536-2253">Lägg till parametrarna "DataProxyIntegrationRuntimeName", "DataProxyStagingLinkedServiceName" och "DataProxyStagingPath" för "Set-AzureRmDataFactoryV2IntegrationRuntime"-cmd för att aktivera konfiguration av lokalt installerad integrationskörning som en proxy för SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="71536-2253">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="71536-2254">Uppdaterade PSTriggerRun till att visa utlöst pipeline, meddelande och egenskaper samt PSActivityRun till att visa aktivitetstypen</span><span class="sxs-lookup"><span data-stu-id="71536-2254">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="71536-2255">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="71536-2255">Az.DataLakeStore</span></span>
* <span data-ttu-id="71536-2256">Korrigering av frysning av Get-DataLakeStoreDeletedItem för fel eller fjärrundantag.</span><span class="sxs-lookup"><span data-stu-id="71536-2256">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="71536-2257">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="71536-2257">Az.EventHub</span></span>
* <span data-ttu-id="71536-2258">Korrigering av problem #9658 : Skrivfel i parametern VirtualNteworkRule i Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="71536-2258">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="71536-2259">Korrigering av problem #9558 : Set-AzEventHubNamespace använder PATCH i stället för PUT</span><span class="sxs-lookup"><span data-stu-id="71536-2259">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="71536-2260">lade till parametern EnableKafka i Set-AzEventHubNamespace-cmdleten</span><span class="sxs-lookup"><span data-stu-id="71536-2260">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="71536-2261">Korrigering av problem #9786 : kan inte skapa en regel med Endast lyssna-behörighet</span><span class="sxs-lookup"><span data-stu-id="71536-2261">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="71536-2262">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="71536-2262">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="71536-2263">Åtgärdade skrivfel i dokumentation där "Azure" skrevs helt med gemener</span><span class="sxs-lookup"><span data-stu-id="71536-2263">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="71536-2264">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="71536-2264">Az.Monitor</span></span>
* <span data-ttu-id="71536-2265">Åtgärdade felaktigt parameternamn i hjälpdokumentationen</span><span class="sxs-lookup"><span data-stu-id="71536-2265">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71536-2266">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71536-2266">Az.Network</span></span>
* <span data-ttu-id="71536-2267">Uppdaterade New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="71536-2267">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="71536-2268">Gjorde parametern "PublicIpAddress" inaktuell eftersom den aldrig används på serversidan.</span><span class="sxs-lookup"><span data-stu-id="71536-2268">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="71536-2269">Lade till den valfria parametern "Primary", som anger huruvida den aktuella IP-konfigurationen är den primära.</span><span class="sxs-lookup"><span data-stu-id="71536-2269">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="71536-2270">Förbättrade hanteringen av felundantag för begärande från SDK – åtgärdar problemet att tidigare SDK-undantag inte hanteras på rätt sätt, vilket leder till att viktig felinformation inte visas</span><span class="sxs-lookup"><span data-stu-id="71536-2270">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="71536-2271">Justerade valideringslogiken för IPv6-IP-prefix till att kontrollera korrekt IPv6-prefixlängd.</span><span class="sxs-lookup"><span data-stu-id="71536-2271">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="71536-2272">Uppdaterade Get-AzVirtualNetworkSubnetConfig: Lade till parameter som anges till get av undernätets resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="71536-2272">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="71536-2273">Uppdaterade beskrivningen av parametern Location för AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="71536-2273">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="71536-2274">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="71536-2274">Az.OperationalInsights</span></span>
* <span data-ttu-id="71536-2275">Uppdaterade dokumentation för "New-AzOperationalInsightsLinuxSyslogDataSource"</span><span class="sxs-lookup"><span data-stu-id="71536-2275">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="71536-2276">Lade till exempel</span><span class="sxs-lookup"><span data-stu-id="71536-2276">Added example</span></span>
    - <span data-ttu-id="71536-2277">Uppdaterade beskrivningen av parametern "-Name"</span><span class="sxs-lookup"><span data-stu-id="71536-2277">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="71536-2278">Lade till ett exempel för New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="71536-2278">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="71536-2279">Ändrade beskrivningen av parametern -Name för New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="71536-2279">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="71536-2280">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="71536-2280">Az.RecoveryServices</span></span>
* <span data-ttu-id="71536-2281">Uppdatera "Get-AzRecoveryServicesBackupJobDetail.md"</span><span class="sxs-lookup"><span data-stu-id="71536-2281">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="71536-2282">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71536-2282">Az.Resources</span></span>
* <span data-ttu-id="71536-2283">Lägg till stöd för den nya API-versionen från 2019-05-10 för Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="71536-2283">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="71536-2284">Lägg till stöd för "copy.count = 0" för variabler, resurser och egenskaper</span><span class="sxs-lookup"><span data-stu-id="71536-2284">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="71536-2285">Resurser med "condition = false" eller "copy.count = 0" tas bort i complete-läget</span><span class="sxs-lookup"><span data-stu-id="71536-2285">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="71536-2286">Lägg till ett exempel på tilldelning av princip på prenumerationsnivå i hjälpdokumentationen</span><span class="sxs-lookup"><span data-stu-id="71536-2286">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="71536-2287">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="71536-2287">Az.ServiceBus</span></span>
* <span data-ttu-id="71536-2288">Korrigering av problem #9658 : Skrivfel i parametern VirtualNetworkRule i set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="71536-2288">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="71536-2289">Korrigering av problem #9786 : kan inte skapa en regel med Endast lyssna-behörighet</span><span class="sxs-lookup"><span data-stu-id="71536-2289">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="71536-2290">Lade till det nya kommandot "Test-AzServiceBusNameAvailability" för att kontrollera namntillgängligheten för kö och ämne</span><span class="sxs-lookup"><span data-stu-id="71536-2290">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="71536-2291">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="71536-2291">Az.ServiceFabric</span></span>
* <span data-ttu-id="71536-2292">Åtgärda buggar med tillägg av nodtyps-cmdlet:</span><span class="sxs-lookup"><span data-stu-id="71536-2292">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="71536-2293">NullReferenceException-bugg när resursgrupp hade annan vmss som inte är relaterad till Service Fabric-klustret.</span><span class="sxs-lookup"><span data-stu-id="71536-2293">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="71536-2294">Åtgärdar problemet: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="71536-2294">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="71536-2295">Åtgärda bugg där cmdleten misslyckades om virtualNetwork var i en annan resursgrupp än klustret.</span><span class="sxs-lookup"><span data-stu-id="71536-2295">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="71536-2296">Åtgärdar problemet: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="71536-2296">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="71536-2297">AzServiceFabricApplicationCertificate-cmdleten görs inaktuell</span><span class="sxs-lookup"><span data-stu-id="71536-2297">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="71536-2298">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71536-2298">Az.Sql</span></span>
* <span data-ttu-id="71536-2299">Uppdatera dokumentation om gamla gransknings-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="71536-2299">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="71536-2300">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="71536-2300">Az.Storage</span></span>
* <span data-ttu-id="71536-2301">Uppdatera hjälpen för Get/Close-AzStorageFileHandle genom att lägga till fler scenarier i cmdlet-exempel och uppdatera parameterbeskrivningar</span><span class="sxs-lookup"><span data-stu-id="71536-2301">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="71536-2302">Stöd för StandardBlobTier i uppladdningsblob och kopieringsblob</span><span class="sxs-lookup"><span data-stu-id="71536-2302">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="71536-2303">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="71536-2303">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="71536-2304">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="71536-2304">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="71536-2305">Stöd för rehydratiseringsprioritet i kopieringsblob</span><span class="sxs-lookup"><span data-stu-id="71536-2305">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="71536-2306">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="71536-2306">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="71536-2307">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="71536-2307">Az.Websites</span></span>
* <span data-ttu-id="71536-2308">Lägg till klargöranden gällande parametern -AppSettings i Set-AzWebApp och Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="71536-2308">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="71536-2309">2.5.0 – July 2019</span><span class="sxs-lookup"><span data-stu-id="71536-2309">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="71536-2310">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="71536-2310">Az.Accounts</span></span>
* <span data-ttu-id="71536-2311">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="71536-2311">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="71536-2312">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="71536-2312">Az.ApplicationInsights</span></span>
* <span data-ttu-id="71536-2313">Korrigera skrivfel i exempel i dokumentationen för Remove-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="71536-2313">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="71536-2314">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="71536-2314">Az.Automation</span></span>
* <span data-ttu-id="71536-2315">Korrigera skrivfel i resurssträng</span><span class="sxs-lookup"><span data-stu-id="71536-2315">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="71536-2316">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="71536-2316">Az.CognitiveServices</span></span>
* <span data-ttu-id="71536-2317">Stöd för NetworkRuleSet har lagts till.</span><span class="sxs-lookup"><span data-stu-id="71536-2317">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71536-2318">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71536-2318">Az.Compute</span></span>
* <span data-ttu-id="71536-2319">Lägg till saknade egenskaper (ComputerName, OsName, OsVersion och HyperVGeneration) för visningsobjekt i den virtuella datorinstansen.</span><span class="sxs-lookup"><span data-stu-id="71536-2319">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="71536-2320">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="71536-2320">Az.ContainerRegistry</span></span>
* <span data-ttu-id="71536-2321">Åtgärda skrivfel i Remove-AzContainerRegistryReplication för parametern Replication</span><span class="sxs-lookup"><span data-stu-id="71536-2321">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="71536-2322">Mer information finns här: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="71536-2322">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="71536-2323">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="71536-2323">Az.DataFactory</span></span>
* <span data-ttu-id="71536-2324">ADF .Net SDK-versionen har uppdaterats till 4.1.0</span><span class="sxs-lookup"><span data-stu-id="71536-2324">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="71536-2325">Korrigera skrivfel i dokumentationen för Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="71536-2325">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="71536-2326">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="71536-2326">Az.EventHub</span></span>
* <span data-ttu-id="71536-2327">Ny cmmdlet har lagts till för att skapa SAS-token: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="71536-2327">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="71536-2328">verifierings- och felmeddelande har lagts till för authorizationrules-rättigheter om endast "hantera" har tilldelats</span><span class="sxs-lookup"><span data-stu-id="71536-2328">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="71536-2329">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="71536-2329">Az.KeyVault</span></span>
* <span data-ttu-id="71536-2330">Stöd har lagts till för att ange KeySize för certifikatprinciper</span><span class="sxs-lookup"><span data-stu-id="71536-2330">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="71536-2331">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="71536-2331">Az.LogicApp</span></span>
* <span data-ttu-id="71536-2332">Korrigering för Get-AzIntegrationAccountMap för att lista alla mappningstyper</span><span class="sxs-lookup"><span data-stu-id="71536-2332">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="71536-2333">Ny MapType-parameter har lagts till för filtrering</span><span class="sxs-lookup"><span data-stu-id="71536-2333">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="71536-2334">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="71536-2334">Az.ManagedServices</span></span>
* <span data-ttu-id="71536-2335">Stöd för API-versionen 2019-06-01 (GA) har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-2335">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71536-2336">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71536-2336">Az.Network</span></span>
* <span data-ttu-id="71536-2337">Lägg till stöd för privat slutpunkt och privat länktjänst</span><span class="sxs-lookup"><span data-stu-id="71536-2337">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="71536-2338">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="71536-2338">New cmdlets</span></span>
        - <span data-ttu-id="71536-2339">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="71536-2339">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="71536-2340">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="71536-2340">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="71536-2341">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="71536-2341">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="71536-2342">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="71536-2342">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="71536-2343">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="71536-2343">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="71536-2344">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="71536-2344">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="71536-2345">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="71536-2345">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="71536-2346">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="71536-2346">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="71536-2347">Nedanstående kommandon för funktionen har uppdaterats: Flaggan PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies på undernätet i VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="71536-2347">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="71536-2348">Uppdaterade New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="71536-2348">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="71536-2349">Valfri parameter har lagts till – PrivateEndpointNetworkPoliciesFlag som konfigurerar huruvida nätverksprinciper ska tillämpas på en privat slutpunkt i det här undernätet.</span><span class="sxs-lookup"><span data-stu-id="71536-2349">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="71536-2350">Valfri parameter har lagts till – PrivateLinkServiceNetworkPoliciesFlag som konfigurerar huruvida nätverksprinciper ska tillämpas på en privat länktjänst i det här undernätet.</span><span class="sxs-lookup"><span data-stu-id="71536-2350">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="71536-2351">AzPrivateLinkService för cmdlet-parametern ServiceName har bytt namn till Name med aliaset ServiceName för bakåtkompatibilitet</span><span class="sxs-lookup"><span data-stu-id="71536-2351">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="71536-2352">Aktivera ICMP-protokoll för konfiguration av nätverkssäkerhetsregler</span><span class="sxs-lookup"><span data-stu-id="71536-2352">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="71536-2353">Uppdaterade cmdletar</span><span class="sxs-lookup"><span data-stu-id="71536-2353">Updated cmdlets</span></span>
        - <span data-ttu-id="71536-2354">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="71536-2354">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="71536-2355">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="71536-2355">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="71536-2356">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="71536-2356">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="71536-2357">Lägg till ConnectionProtocolType (Ikev1/Ikev2) som en konfigurerbar parameter för New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="71536-2357">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="71536-2358">Lägg till PrivateIpAddressVersion i LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="71536-2358">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="71536-2359">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="71536-2359">Updated cmdlet:</span></span>
        - <span data-ttu-id="71536-2360">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="71536-2360">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="71536-2361">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="71536-2361">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="71536-2362">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="71536-2362">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="71536-2363">Uppdatering av Application Gateway-kommandot New-AzApplicationGatewayProbeConfig för stöd av anpassad port i Probe</span><span class="sxs-lookup"><span data-stu-id="71536-2363">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="71536-2364">Uppdaterade New-AzApplicationGatewayProbeConfig: Den valfria parametern Port som används för avsökning i serverdelen har lagts till.</span><span class="sxs-lookup"><span data-stu-id="71536-2364">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="71536-2365">Denna parameter gäller för SKU:erna Standard_V2 och WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="71536-2365">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="71536-2366">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="71536-2366">Az.OperationalInsights</span></span>
* <span data-ttu-id="71536-2367">Uppdaterade standardversionen för sparade sökningar till 1.</span><span class="sxs-lookup"><span data-stu-id="71536-2367">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="71536-2368">Åtgärdade hantering av anpassad log null regex</span><span class="sxs-lookup"><span data-stu-id="71536-2368">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="71536-2369">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="71536-2369">Az.RecoveryServices</span></span>
* <span data-ttu-id="71536-2370">Uppdatera Get-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="71536-2370">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="71536-2371">Uppdatera Get-AzRecoveryServicesBackupContainer.md</span><span class="sxs-lookup"><span data-stu-id="71536-2371">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="71536-2372">Uppdatera Get-AzRecoveryServicesVault.md</span><span class="sxs-lookup"><span data-stu-id="71536-2372">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="71536-2373">Uppdatera Wait-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="71536-2373">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="71536-2374">Uppdatera Set-AzRecoveryServicesVaultContext.md</span><span class="sxs-lookup"><span data-stu-id="71536-2374">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="71536-2375">Uppdatera Get-AzRecoveryServicesBackupItem.md</span><span class="sxs-lookup"><span data-stu-id="71536-2375">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="71536-2376">Uppdatera Get-AzRecoveryServicesBackupRecoveryPoint.md</span><span class="sxs-lookup"><span data-stu-id="71536-2376">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="71536-2377">Uppdatera Restore-AzRecoveryServicesBackupItem.md</span><span class="sxs-lookup"><span data-stu-id="71536-2377">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="71536-2378">Uppdaterat tjänstanrop för avregistrering av container för Azure-filresurs</span><span class="sxs-lookup"><span data-stu-id="71536-2378">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="71536-2379">Uppdatera Set-AzRecoveryServicesAsrAlertSetting.md</span><span class="sxs-lookup"><span data-stu-id="71536-2379">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="71536-2380">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71536-2380">Az.Resources</span></span>
- <span data-ttu-id="71536-2381">Ta bort den cmdlet som saknas och som refereras i dokumentationen till New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="71536-2381">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="71536-2382">Princip-cmdletar har uppdaterats så att de använder den nya API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="71536-2382">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="71536-2383">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="71536-2383">Az.ServiceBus</span></span>
* <span data-ttu-id="71536-2384">Ny cmmdlet har lagts till för att skapa SAS-token: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="71536-2384">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="71536-2385">verifierings- och felmeddelande har lagts till för authorizationrules-rättigheter om endast "hantera" har tilldelats</span><span class="sxs-lookup"><span data-stu-id="71536-2385">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="71536-2386">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71536-2386">Az.Sql</span></span>
* <span data-ttu-id="71536-2387">Åtgärda saknade exempel för Set-AzSqlDatabaseSecondary cmdlet</span><span class="sxs-lookup"><span data-stu-id="71536-2387">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="71536-2388">Åtgärda angivna återkommande genomsökningar för bedömning av säkerhetsrisk utan angivna e-postadresser</span><span class="sxs-lookup"><span data-stu-id="71536-2388">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="71536-2389">Korrigera ett skrivfel i ett varningsmeddelande.</span><span class="sxs-lookup"><span data-stu-id="71536-2389">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="71536-2390">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="71536-2390">Az.Storage</span></span>
* <span data-ttu-id="71536-2391">Uppdatera exempel i referensdokumentationen för Get-AzStorageAccount så att rätt parameternamn används</span><span class="sxs-lookup"><span data-stu-id="71536-2391">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="71536-2392">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="71536-2392">Az.StorageSync</span></span>
* <span data-ttu-id="71536-2393">Lägger till cmdleten Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="71536-2393">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="71536-2394">Åtgärda problem 9551 så att TierFilesOlderThanDays föredras</span><span class="sxs-lookup"><span data-stu-id="71536-2394">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="71536-2395">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="71536-2395">Az.Websites</span></span>
* <span data-ttu-id="71536-2396">Åtgärdar ett fel där vissa SiteConfig-egenskaper inte returnerades av Get-AzWebApp och Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="71536-2396">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="71536-2397">Lägger till en ny platsparameter för Get-AzDeletedWebApp och Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="71536-2397">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="71536-2398">Åtgärdar ett fel i kloning av webbapp-platser som använder New-AzWebApp-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="71536-2398">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="71536-2399">2.4.0 – juli 2019</span><span class="sxs-lookup"><span data-stu-id="71536-2399">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="71536-2400">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="71536-2400">Az.Accounts</span></span>
* <span data-ttu-id="71536-2401">Lägg till stöd för profil-cmdletar</span><span class="sxs-lookup"><span data-stu-id="71536-2401">Add support for profile cmdlets</span></span>
* <span data-ttu-id="71536-2402">Lägg till stöd för miljöer och dataplaner i genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="71536-2402">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="71536-2403">Åtgärda bugg där fel slutpunkt i vissa fall användes för cmdletar för dataplaner i Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="71536-2403">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="71536-2404">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="71536-2404">Az.Advisor</span></span>
* <span data-ttu-id="71536-2405">GA-version av Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="71536-2405">GA release of Az.Advisor</span></span>
* <span data-ttu-id="71536-2406">Den här modulen ingår nu som en del av `Az`-sammanslagningsmodulen</span><span class="sxs-lookup"><span data-stu-id="71536-2406">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="71536-2407">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="71536-2407">Az.ApiManagement</span></span>
* <span data-ttu-id="71536-2408">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="71536-2408">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="71536-2409">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="71536-2409">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="71536-2410">Stöd för att fråga prenumerationer efter användare och produkt har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-2410">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="71536-2411">Stöd för att fråga med hjälp av omfång ”/”, ”/apis”, ”/apis/echo-api” har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-2411">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="71536-2412">Korrigering av problem https://github.com/Azure/azure-powershell/issues/9307 och https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="71536-2412">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="71536-2413">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="71536-2413">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="71536-2414">Stöd för att ange ”ApiVersion” och ”ApiVersionSetId” när API:er importeras har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-2414">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="71536-2415">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="71536-2415">Az.Automation</span></span>
* <span data-ttu-id="71536-2416">Bugg med cmdleten Set-AzAutomationConnectionFieldValue för att hantera strängvärde har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="71536-2416">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71536-2417">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71536-2417">Az.Compute</span></span>
* <span data-ttu-id="71536-2418">Lägg till parametern HyperVGeneration i New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="71536-2418">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="71536-2419">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="71536-2419">Az.DataFactory</span></span>
* <span data-ttu-id="71536-2420">Uppdaterar utdata från ADF-cmdletar som hämtar aktivitetskörningar, hämtar pipelinekörningar och hämtar utlösarkörningar för stöd för Select-Object-pipe.</span><span class="sxs-lookup"><span data-stu-id="71536-2420">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="71536-2421">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="71536-2421">Az.EventGrid</span></span>
* <span data-ttu-id="71536-2422">Korrigera stavfel i dokumentation om ”New-AzEventGridSubscription”</span><span class="sxs-lookup"><span data-stu-id="71536-2422">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="71536-2423">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="71536-2423">Az.IotHub</span></span>
* <span data-ttu-id="71536-2424">Lägg till stöd för att återskapa principnycklar för auktorisering.</span><span class="sxs-lookup"><span data-stu-id="71536-2424">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71536-2425">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71536-2425">Az.Network</span></span>
* <span data-ttu-id="71536-2426">”RoutingPreference” har lagts till i offentliga IP-taggar</span><span class="sxs-lookup"><span data-stu-id="71536-2426">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="71536-2427">Förbättra exempel för referensdokumentation om ”Get-AzNetworkServiceTag”</span><span class="sxs-lookup"><span data-stu-id="71536-2427">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="71536-2428">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="71536-2428">Az.PolicyInsights</span></span>
* <span data-ttu-id="71536-2429">Åtgärda problem med null-referens i Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="71536-2429">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="71536-2430">Mer information här: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="71536-2430">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="71536-2431">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="71536-2431">Az.OperationalInsights</span></span>
* <span data-ttu-id="71536-2432">Modellen för CustomLog-datakälla som returneras i Get-AzOperationalInsightsDataSource har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="71536-2432">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="71536-2433">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="71536-2433">Az.RecoveryServices</span></span>
* <span data-ttu-id="71536-2434">Kommandot get-policy för IaaSVM:er har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="71536-2434">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="71536-2435">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71536-2435">Az.Resources</span></span>
    - <span data-ttu-id="71536-2436">Korrigera hjälptext för den översta parametern i Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="71536-2436">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="71536-2437">Lägg till växlingsstöd på klientsidan för Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="71536-2437">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="71536-2438">Lägg till nya parametrar för Set-AzPolicyAssignment, -PolicyParameters och -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="71536-2438">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="71536-2439">En mängd dokument- och exempeluppdateringar för Policy-cmdletar</span><span class="sxs-lookup"><span data-stu-id="71536-2439">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="71536-2440">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="71536-2440">Az.ServiceBus</span></span>
* <span data-ttu-id="71536-2441">Korrigering av problem #4938 – New-AzureRmServiceBusQueue returnerar BadRequest vid konfiguration av MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="71536-2441">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="71536-2442">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71536-2442">Az.Sql</span></span>
* <span data-ttu-id="71536-2443">Lägg till cmdletar för instansredundansgrupper från förhandsversion till offentlig version</span><span class="sxs-lookup"><span data-stu-id="71536-2443">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="71536-2444">Stöd för granskning för Azure SQL Server\Database med nya cmdletar.</span><span class="sxs-lookup"><span data-stu-id="71536-2444">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="71536-2445">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="71536-2445">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="71536-2446">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="71536-2446">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="71536-2447">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="71536-2447">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="71536-2448">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="71536-2448">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="71536-2449">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="71536-2449">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="71536-2450">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="71536-2450">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="71536-2451">Ta bort begränsningar för e-post från inställningarna för sårbarhetsbedömning</span><span class="sxs-lookup"><span data-stu-id="71536-2451">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="71536-2452">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="71536-2452">Az.Storage</span></span>
* <span data-ttu-id="71536-2453">Ändra två parametrar ”-IndexDocument” och ”-ErrorDocument404Path” från ”krävs” till ”valfri” i cmdlet:</span><span class="sxs-lookup"><span data-stu-id="71536-2453">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="71536-2454">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="71536-2454">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="71536-2455">Uppdatera hjälpen för Get-AzStorageBlobContent genom att lägga till ett exempel</span><span class="sxs-lookup"><span data-stu-id="71536-2455">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="71536-2456">Visa mer felinformation när cmdleten misslyckas med StorageException</span><span class="sxs-lookup"><span data-stu-id="71536-2456">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="71536-2457">Stöd för att skapa eller uppdatera lagringskonto med Azure Files AAD DS-autentisering</span><span class="sxs-lookup"><span data-stu-id="71536-2457">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="71536-2458">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="71536-2458">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="71536-2459">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="71536-2459">Set-AzStorageAccount</span></span>
* <span data-ttu-id="71536-2460">Stöd för att lista eller stänga filreferenser för en filresurs, filkatalog eller en fil</span><span class="sxs-lookup"><span data-stu-id="71536-2460">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="71536-2461">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="71536-2461">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="71536-2462">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="71536-2462">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="71536-2463">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="71536-2463">Az.StorageSync</span></span>
* <span data-ttu-id="71536-2464">Den här modulen ingår nu som en del av `Az`-sammanslagningsmodulen</span><span class="sxs-lookup"><span data-stu-id="71536-2464">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="71536-2465">2.3.2 – juni 2019</span><span class="sxs-lookup"><span data-stu-id="71536-2465">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="71536-2466">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="71536-2466">Az.Accounts</span></span>
* <span data-ttu-id="71536-2467">Åtgärda bugg med felaktiga webbadresser som i vissa fall användes för Functions-anrop</span><span class="sxs-lookup"><span data-stu-id="71536-2467">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="71536-2468">Mer information här: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="71536-2468">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="71536-2469">Åtgärda problem med alias från AzureRM i Az-cmdletar</span><span class="sxs-lookup"><span data-stu-id="71536-2469">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="71536-2470">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="71536-2470">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="71536-2471">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="71536-2471">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71536-2472">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71536-2472">Az.Compute</span></span>
* <span data-ttu-id="71536-2473">Parameteruppsättningarna New-AzVm och New-AzVmss accepterar nu parametern ”ProximityPlacementGroup”.</span><span class="sxs-lookup"><span data-stu-id="71536-2473">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="71536-2474">Stavfel i referensdokumentationen för ”New-AzVM” har korrigerats</span><span class="sxs-lookup"><span data-stu-id="71536-2474">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="71536-2475">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="71536-2475">Az.Dns</span></span>
* <span data-ttu-id="71536-2476">Stavfel i hjälpexempel för ”Set-AzDnsZone” har korrigerats.</span><span class="sxs-lookup"><span data-stu-id="71536-2476">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="71536-2477">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="71536-2477">Az.EventGrid</span></span>
* <span data-ttu-id="71536-2478">Har uppdaterats för att använda API-versionen 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="71536-2478">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="71536-2479">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="71536-2479">New cmdlets:</span></span>
    - <span data-ttu-id="71536-2480">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="71536-2480">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="71536-2481">Skapar en ny Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="71536-2481">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="71536-2482">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="71536-2482">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="71536-2483">Hämtar information om en Event Grid-domän eller hämtar en lista med alla Event Grid-domäner i den aktuella Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="71536-2483">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="71536-2484">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="71536-2484">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="71536-2485">Tar bort en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="71536-2485">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="71536-2486">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="71536-2486">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="71536-2487">Återskapar nyckeln för delad åtkomst för en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="71536-2487">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="71536-2488">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="71536-2488">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="71536-2489">Hämtar de nycklar för delad åtkomst som används för att publicera händelser till en Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="71536-2489">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="71536-2490">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="71536-2490">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="71536-2491">Skapar ett nytt Azure Event Grid-domänämne.</span><span class="sxs-lookup"><span data-stu-id="71536-2491">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="71536-2492">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="71536-2492">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="71536-2493">Hämtar information om ett Event Grid-domänämne eller hämtar en lista med alla Event Grid-domänämnen under en specifik Event Grid-domän i nuvarande Azure</span><span class="sxs-lookup"><span data-stu-id="71536-2493">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="71536-2494">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="71536-2494">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="71536-2495">Tar bort ett befintligt Azure Event Grid-domänämne.</span><span class="sxs-lookup"><span data-stu-id="71536-2495">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="71536-2496">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="71536-2496">Updated cmdlets:</span></span>
    - <span data-ttu-id="71536-2497">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="71536-2497">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="71536-2498">Lägg till nya obligatoriska parametrar för att stödja piping för den nya Event Grid-domänen och Event Grid-domänämnet för att göra det möjligt att skapa nya händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="71536-2498">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="71536-2499">Lägg till nya obligatoriska parametrar för att ange det nya Event Grid-domännamnet och/eller namnet på Event Grid-domänämnet för att göra det möjligt att skapa nya händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="71536-2499">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="71536-2500">Lägg till ny parameteruppsättningar för domäner och domänämnen för att göra det möjligt att återanvända befintliga parametrar (t.ex. EndPointType, SubjectBeginsWith osv).</span><span class="sxs-lookup"><span data-stu-id="71536-2500">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="71536-2501">Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="71536-2501">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="71536-2502">Förfallodatum för händelseprenumeration</span><span class="sxs-lookup"><span data-stu-id="71536-2502">Event subscription expiration date,</span></span>
            - <span data-ttu-id="71536-2503">Avancerade filterparametrar.</span><span class="sxs-lookup"><span data-stu-id="71536-2503">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="71536-2504">Lägg till ny uppräkning för servicebusqueue som mål.</span><span class="sxs-lookup"><span data-stu-id="71536-2504">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="71536-2505">Tillåt inte användning av ”Alla” i alternativet -IncludedEventType och ersätt det med</span><span class="sxs-lookup"><span data-stu-id="71536-2505">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="71536-2506">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="71536-2506">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="71536-2507">Lägg till ny valfria parametrar (Top, ODataQuery och NextLink) för att stödja sidnumrering och filtrering av resultat.</span><span class="sxs-lookup"><span data-stu-id="71536-2507">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="71536-2508">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="71536-2508">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="71536-2509">Lägg till nya obligatoriska parametrar för att stödja piping för en Event Grid-domän och Event Grid-domänämnen för att göra det möjligt att ta bort befintliga händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="71536-2509">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="71536-2510">Lägg till nya obligatoriska parametrar för att ange Event Grid-domännamnet och/eller namnet på Event Grid-domänämnet för att göra det möjligt att ta bort befintliga händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="71536-2510">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="71536-2511">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="71536-2511">Az.FrontDoor</span></span>
* <span data-ttu-id="71536-2512">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="71536-2512">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="71536-2513">Lägg till stöd för transformeringar och nytt värde för automatisk komplettering för operatorer (RegEx)</span><span class="sxs-lookup"><span data-stu-id="71536-2513">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="71536-2514">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="71536-2514">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="71536-2515">Lägg till nya värden för automatisk komplettering</span><span class="sxs-lookup"><span data-stu-id="71536-2515">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71536-2516">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71536-2516">Az.Network</span></span>
* <span data-ttu-id="71536-2517">Lägg till stöd för resurs för virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="71536-2517">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="71536-2518">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="71536-2518">New cmdlets</span></span>
        - <span data-ttu-id="71536-2519">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="71536-2519">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="71536-2520">Lägg till AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="71536-2520">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="71536-2521">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="71536-2521">New cmdlets</span></span>
        - <span data-ttu-id="71536-2522">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="71536-2522">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="71536-2523">Lägg till PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="71536-2523">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="71536-2524">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="71536-2524">New cmdlets</span></span>
        - <span data-ttu-id="71536-2525">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="71536-2525">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="71536-2526">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="71536-2526">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="71536-2527">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="71536-2527">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="71536-2528">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="71536-2528">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="71536-2529">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="71536-2529">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="71536-2530">Lägg till PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="71536-2530">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="71536-2531">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="71536-2531">New cmdlets</span></span>
        - <span data-ttu-id="71536-2532">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="71536-2532">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="71536-2533">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="71536-2533">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="71536-2534">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="71536-2534">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="71536-2535">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="71536-2535">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="71536-2536">Nedanstående kommandon för funktionen har uppdaterats: Flaggan UseLocalAzureIpAddress på VpnConnection</span><span class="sxs-lookup"><span data-stu-id="71536-2536">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="71536-2537">New-AzVpnConnection har uppdaterats: Den valfria parametern -UseLocalAzureIpAddress har lagts till för att visa att en lokal IP-adress i Azure ska användas som källadress när anslutningen initieras.</span><span class="sxs-lookup"><span data-stu-id="71536-2537">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="71536-2538">Set-AzVpnConnection har uppdaterats: Den valfria parametern -UseLocalAzureIpAddress har lagts till för att visa att en lokal IP-adress i Azure ska användas som källadress när anslutningen initieras.</span><span class="sxs-lookup"><span data-stu-id="71536-2538">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="71536-2539">Det skrivskyddade fältet PeeredConnections har lagts till i ExpressRoute-peering.</span><span class="sxs-lookup"><span data-stu-id="71536-2539">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="71536-2540">Det skrivskyddade fältet GlobalReachEnabled har lagts till i ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="71536-2540">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="71536-2541">Ett attribut för icke-bakåtkompatibla ändringar har lagts till för att lyfta fram utfasning av fältet AllowGlobalReach i modellen ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="71536-2541">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="71536-2542">Problem 8756 har åtgärdats: Fel vid användning av TargetListenerID med AzApplicationGatewayRedirectConfiguration-cmdletar</span><span class="sxs-lookup"><span data-stu-id="71536-2542">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="71536-2543">En bugg i New-AzApplicationGatewayPathRuleConfig som gjorde att regeluppsättningen för att återskapa inte kunde anges har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="71536-2543">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="71536-2544">Visningen av VirtualNetworkTaps i NetworkInterfaceIpConfiguration har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="71536-2544">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="71536-2545">Cortex Get-cmdletar för att visa en lista med alla delar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="71536-2545">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="71536-2546">Funktionen för att skapa VirtualHub-referenser för ExpressRouteGateways och VpnGateway har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="71536-2546">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="71536-2547">Stöd för tillgänglighetszoner i AzureFirewall och NatGateway har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-2547">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="71536-2548">Cmdleten Get-AzNetworkServiceTag har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-2548">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="71536-2549">Lägg till stöd för flera offentliga IP-adresser för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="71536-2549">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="71536-2550">Cmdleten New-AzFirewall har uppdaterats:</span><span class="sxs-lookup"><span data-stu-id="71536-2550">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="71536-2551">Parametern -PublicIpAddress som accepterar ett eller flera offentliga IP-adressobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-2551">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="71536-2552">Parametern -VirtualNetwork som accepterar ett virtuellt nätverksobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-2552">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="71536-2553">Metoderna AddPublicIpAddress och RemovePublicIpAddress har lagts till på brandväggsobjekt – dessa accepterar ett offentligt IP-adressobjekt som indata</span><span class="sxs-lookup"><span data-stu-id="71536-2553">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="71536-2554">Inaktuella parametrar -PublicIpName och -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="71536-2554">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="71536-2555">Nedanstående kommandon för funktionen har uppdaterats: Ange autentiseringsalternativ för VpnClient AAD till resurser för virtuella nätverksgatewayer.</span><span class="sxs-lookup"><span data-stu-id="71536-2555">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="71536-2556">New-AzVirtualNetworkGateway har uppdaterats: De valfria parametrarna AadTenantUri, AadAudienceId och AadIssuerUri för att ange VpnClient AAD-autentiseringsalternativ på en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="71536-2556">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="71536-2557">Set-AzVirtualNetworkGateway har uppdaterats: De valfria parametrarna AadTenantUri, AadAudienceId och AadIssuerUri för att ange VpnClient AAD-autentiseringsalternativ på en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="71536-2557">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="71536-2558">Set-AzVirtualNetworkGateway har uppdaterats: Den valfria växelparametern RemoveAadAuthentication som tar bort VpnClient AAD-autentiseringsalternativ från en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="71536-2558">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="71536-2559">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="71536-2559">Az.OperationalInsights</span></span>
* <span data-ttu-id="71536-2560">Aktivera prisnivån **pergb2018** i kommandot ”New-AzureRmOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="71536-2560">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="71536-2561">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71536-2561">Az.Resources</span></span>
* <span data-ttu-id="71536-2562">Stöd för ytterligare alternativ för att exportera en mall</span><span class="sxs-lookup"><span data-stu-id="71536-2562">Support for additional Template Export options</span></span>
    - <span data-ttu-id="71536-2563">Lägg till parametern ”-SkipResourceNameParameterization” till Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="71536-2563">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="71536-2564">Lägg till parametern ”-SkipAllParameterization” till Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="71536-2564">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="71536-2565">Lägg till parametern ”-Resource” till Export-AzResourceGroup för exporterad resursfiltrering</span><span class="sxs-lookup"><span data-stu-id="71536-2565">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="71536-2566">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="71536-2566">Az.ServiceFabric</span></span>
* <span data-ttu-id="71536-2567">Åtgärda att fel tumavtryck används vid tilläggning av certifikat i ByExistingKeyVault i vissa fall</span><span class="sxs-lookup"><span data-stu-id="71536-2567">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="71536-2568">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71536-2568">Az.Sql</span></span>
* <span data-ttu-id="71536-2569">Åtgärda suffix för lagringsslutpunkt i Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="71536-2569">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="71536-2570">Åtgärda att aktivering av Advanced Data Security åsidosätter Advanced Threat Protection-princip</span><span class="sxs-lookup"><span data-stu-id="71536-2570">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="71536-2571">Nya cmdletar för Management.Sql som gör att kunderna kan lägga till nycklar för transparent datakryptering (TDE) och ange TDE-skydd för hanterade instanser</span><span class="sxs-lookup"><span data-stu-id="71536-2571">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="71536-2572">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="71536-2572">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="71536-2573">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="71536-2573">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="71536-2574">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="71536-2574">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="71536-2575">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="71536-2575">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="71536-2576">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="71536-2576">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="71536-2577">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="71536-2577">Az.Storage</span></span>
* <span data-ttu-id="71536-2578">Stöd för typerna FileStorage och SkuName Premium_ZRS när lagringskonton skapas</span><span class="sxs-lookup"><span data-stu-id="71536-2578">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="71536-2579">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="71536-2579">New-AzStorageAccount</span></span>
* <span data-ttu-id="71536-2580">Beskrivningen av cmdleten för bloboföränderlighet har förtydligats</span><span class="sxs-lookup"><span data-stu-id="71536-2580">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="71536-2581">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="71536-2581">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="71536-2582">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="71536-2582">Az.Websites</span></span>
* <span data-ttu-id="71536-2583">Optimerar Get-AzWebAppCertificate för att filtrera efter resursgrupp på servern i stället för klienten</span><span class="sxs-lookup"><span data-stu-id="71536-2583">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="71536-2584">Lägger till växlingsparametern -UseDisasterRecovery till Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="71536-2584">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="71536-2585">2.2.0 – juni 2019</span><span class="sxs-lookup"><span data-stu-id="71536-2585">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="71536-2586">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="71536-2586">Az.Cdn</span></span>
* <span data-ttu-id="71536-2587">Uppdaterade cmdletar för att ge stöd för rulesEngine-funktion baserat på API-version 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="71536-2587">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71536-2588">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71536-2588">Az.Compute</span></span>
* <span data-ttu-id="71536-2589">Lade till parameter `NoWait` som startar åtgärden och returnerar omedelbart, innan åtgärden har slutförts.</span><span class="sxs-lookup"><span data-stu-id="71536-2589">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="71536-2590">Uppdaterade cmdletar:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="71536-2590">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="71536-2591">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="71536-2591">Az.EventHub</span></span>
* <span data-ttu-id="71536-2592">Korrigering för #9231 – Get-AzEventHubNamespace returnerar inga taggar</span><span class="sxs-lookup"><span data-stu-id="71536-2592">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="71536-2593">Korrigering för #9230 – Get-AzEventHubNamespace returnerar ResourceGroup istället för ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71536-2593">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71536-2594">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71536-2594">Az.Network</span></span>
* <span data-ttu-id="71536-2595">Uppdatera ResourceId och InputObject för NAT-gateway</span><span class="sxs-lookup"><span data-stu-id="71536-2595">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="71536-2596">Lägg till alias för ResourceId och InputObject</span><span class="sxs-lookup"><span data-stu-id="71536-2596">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="71536-2597">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="71536-2597">Az.PolicyInsights</span></span>
* <span data-ttu-id="71536-2598">Åtgärda Null-referensproblem i Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="71536-2598">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="71536-2599">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="71536-2599">Az.RecoveryServices</span></span>
* <span data-ttu-id="71536-2600">Minsta kvarhållning för IaaSVM-policy i dagar ändrat till 7 från 1</span><span class="sxs-lookup"><span data-stu-id="71536-2600">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="71536-2601">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="71536-2601">Az.ServiceBus</span></span>
* <span data-ttu-id="71536-2602">Korrigering för ärende #9182 – Get-AzServiceBusNamespace returnerar ResourceGroup istället för ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71536-2602">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="71536-2603">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="71536-2603">Az.ServiceFabric</span></span>
* <span data-ttu-id="71536-2604">Åtgärda stavfel i felmeddelandet för Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="71536-2604">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="71536-2605">Åtgärda saknat tecken i Service Fabric-kommandorader</span><span class="sxs-lookup"><span data-stu-id="71536-2605">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="71536-2606">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71536-2606">Az.Sql</span></span>
* <span data-ttu-id="71536-2607">Lägg till parametern DnsZonePartner för New-AzureSqlInstance-cmdlet för att ge stöd för AutoDr för hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="71536-2607">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="71536-2608">Avvecklar cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="71536-2608">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="71536-2609">Döp om cmdletar för hotidentifiering till Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="71536-2609">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="71536-2610">Parametrarna New-AzSqlInstance -StorageSizeInGB och -LicenseType är nu valfria.</span><span class="sxs-lookup"><span data-stu-id="71536-2610">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="71536-2611">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="71536-2611">Az.Websites</span></span>
* <span data-ttu-id="71536-2612">åtgärdar problemet där användningen av Set-AzWebApp och Set-AzWebAppSlot med -WebApp-egenskap tog bort taggarna</span><span class="sxs-lookup"><span data-stu-id="71536-2612">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="71536-2613">2.1.0 – maj 2019</span><span class="sxs-lookup"><span data-stu-id="71536-2613">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="71536-2614">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="71536-2614">Az.ApiManagement</span></span>
* <span data-ttu-id="71536-2615">Skapade nya cmdletar för att hantera diagnostik för global- och API-omfång</span><span class="sxs-lookup"><span data-stu-id="71536-2615">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="71536-2616">**Get-AzApiManagementDiagnostic** – Skaffa diagnostik konfigurerad för global- eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="71536-2616">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="71536-2617">**New-AzApiManagementDiagnostic** – Skapa ny diagnostik för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="71536-2617">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="71536-2618">**New-AzApiManagementHttpMessageDiagnostic** – Skapa diagnostikinställning om vilka rubriker som ska loggas och storleken på brödtextbyte</span><span class="sxs-lookup"><span data-stu-id="71536-2618">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="71536-2619">**New-AzApiManagementPipelineDiagnosticSetting** – Skapa diagnostikinställningar för inkommande/utgående HTTP-meddelanden till gatewayen.</span><span class="sxs-lookup"><span data-stu-id="71536-2619">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="71536-2620">**New-AzApiManagementSamplingSetting** – Skapa samplinginställningar för begäranden/svar för en diagnostik</span><span class="sxs-lookup"><span data-stu-id="71536-2620">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="71536-2621">**Remove-AzApiManagementDiagnostic** – Ta bort en diagnostikenhet för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="71536-2621">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="71536-2622">**Set-AzApiManagementDiagnostic** – Uppdatera en diagnostikenhet för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="71536-2622">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="71536-2623">Skapade nya cmdletar för hantering av cacheminne i ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="71536-2623">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="71536-2624">**Get-AzApiManagementCache** – Hämta information om cacheminnet som anges av identifierare eller alla cacheminnen</span><span class="sxs-lookup"><span data-stu-id="71536-2624">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="71536-2625">**New-AzApiManagementCache** – Skapa ett nytt default-cacheminne eller cacheminne i en viss Azure-region</span><span class="sxs-lookup"><span data-stu-id="71536-2625">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="71536-2626">**Remove-AzApiManagementCache** – Ta bort ett cacheminne</span><span class="sxs-lookup"><span data-stu-id="71536-2626">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="71536-2627">**Remove-AzApiManagementCache** – Ta bort ett cacheminne</span><span class="sxs-lookup"><span data-stu-id="71536-2627">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="71536-2628">Skapade nya cmdletar för hantering av API-schema</span><span class="sxs-lookup"><span data-stu-id="71536-2628">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="71536-2629">**New-AzApiManagementSchema** – Skapa ett nytt schema för ett API</span><span class="sxs-lookup"><span data-stu-id="71536-2629">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="71536-2630">**Get-AzApiManagementSchema** – Hämta de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="71536-2630">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="71536-2631">**Remove-AzApiManagementSchema** – Ta bort de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="71536-2631">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="71536-2632">**Set-AzApiManagementSchema** – Uppdatera de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="71536-2632">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="71536-2633">Skapa ny cmdlet för att generera en användartoken.</span><span class="sxs-lookup"><span data-stu-id="71536-2633">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="71536-2634">**New-AzApiManagementUserToken** – Skapa en ny användartoken som enligt standardinställning är giltig i 8 timmar. Token för GIT-användaren kan skapas med den här cmdleten./</span><span class="sxs-lookup"><span data-stu-id="71536-2634">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="71536-2635">Skapade en ny cmdlet för att hämta nätverksstatus</span><span class="sxs-lookup"><span data-stu-id="71536-2635">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="71536-2636">**Get-AzApiManagementNetworkStatus** – Hämta nätverksstatusanslutningen för resurserna som API Management-tjänsten är beroende av.</span><span class="sxs-lookup"><span data-stu-id="71536-2636">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="71536-2637">Det här är användbart när du distribuerar ApiManagement-tjänsten i ett virtuellt nätverk och validerar om något beroende är brutet.</span><span class="sxs-lookup"><span data-stu-id="71536-2637">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="71536-2638">Uppdaterade cmdlet **New-AzApiManagement** för att hantera ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="71536-2638">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="71536-2639">Lade till stöd för den nya SKU:n Consumption</span><span class="sxs-lookup"><span data-stu-id="71536-2639">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="71536-2640">Aktiverade stöd för att slå på flaggan EnableClientCertificate för SKU:n Consumption</span><span class="sxs-lookup"><span data-stu-id="71536-2640">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="71536-2641">Den nya cmdleten **New-AzApiManagementSslSetting** gör det möjligt att ställa in TLS/SSL-inställningen på ”Backend” och ”Frontend” (serverdel och klientdel).</span><span class="sxs-lookup"><span data-stu-id="71536-2641">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="71536-2642">Det här kan också användas till att konfigurera chiffer som 3DES och ServerProtocols som Http2 för Frontend för en ApiManagement-tjänst.</span><span class="sxs-lookup"><span data-stu-id="71536-2642">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="71536-2643">Stöd har lagts till för att konfigurera värdnamnet DeveloperPortal på ApiManagement-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="71536-2643">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="71536-2644">Uppdaterade cmdletar **Get-AzApiManagementSsoToken** för att ta PsApiManagement-objekt som indata</span><span class="sxs-lookup"><span data-stu-id="71536-2644">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="71536-2645">Uppdaterad cmdleten för att visa infogade felmeddelanden</span><span class="sxs-lookup"><span data-stu-id="71536-2645">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="71536-2646">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Felkod: Felmeddelande av typen ValidationError: Ett eller flera fält innehåller felaktiga värden: Felinformation:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="71536-2646">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="71536-2647">Uppdaterade cmdlet **Export-AzApiManagementApi** för att exportera API:er i OpenApi 3.0-format</span><span class="sxs-lookup"><span data-stu-id="71536-2647">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="71536-2648">Uppdaterade cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="71536-2648">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="71536-2649">Importera API från dokumentspecifikationen OpenApi 3.0</span><span class="sxs-lookup"><span data-stu-id="71536-2649">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="71536-2650">Om du vill åsidosätta egenskapen PsApiManagementSchema specificerad i ett dokument (Swagger, Wadl, Wsdl, OpenApi).</span><span class="sxs-lookup"><span data-stu-id="71536-2650">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="71536-2651">Åsidosätta egenskapen ServiceUrl som specificeras i ett dokument.</span><span class="sxs-lookup"><span data-stu-id="71536-2651">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="71536-2652">Uppdaterade cmdlet **Get-AzApiManagementPolicy** för att returnera policy i undantaget format av typen icke-XML med rawxml</span><span class="sxs-lookup"><span data-stu-id="71536-2652">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="71536-2653">Uppdaterade cmdlet **Set-AzApiManagementPolicy** för att godkänna policy i undantaget format av typen icke-XML med rawxml och XML undantaget med xml</span><span class="sxs-lookup"><span data-stu-id="71536-2653">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="71536-2654">Uppdaterad cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="71536-2654">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="71536-2655">Konfigurera API med OpenId auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="71536-2655">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="71536-2656">Skapa ett API i ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="71536-2656">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="71536-2657">Klona ett API med SourceApiId och SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="71536-2657">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="71536-2658">Möjlighet att konfigurera SubscriptionRequired i API-omfattningen.</span><span class="sxs-lookup"><span data-stu-id="71536-2658">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="71536-2659">Uppdaterad cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="71536-2659">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="71536-2660">Konfigurera API med OpenId auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="71536-2660">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="71536-2661">Uppdatera ett API till ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="71536-2661">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="71536-2662">Möjlighet att konfigurera SubscriptionRequired i API-omfattningen.</span><span class="sxs-lookup"><span data-stu-id="71536-2662">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="71536-2663">Uppdaterad cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="71536-2663">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="71536-2664">Klona en befintlig version med hjälp av SourceApiRevision (kopiera taggar, produkter, åtgärder och principer).</span><span class="sxs-lookup"><span data-stu-id="71536-2664">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="71536-2665">Den nya revisionen antar ApiId från den överordnade instansen.</span><span class="sxs-lookup"><span data-stu-id="71536-2665">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="71536-2666">Tillhandahålla ApiRevisionDescription</span><span class="sxs-lookup"><span data-stu-id="71536-2666">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="71536-2667">Åsidosätta ServiceUrl vid kloning av ett API.</span><span class="sxs-lookup"><span data-stu-id="71536-2667">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="71536-2668">Uppdaterad cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="71536-2668">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="71536-2669">Konfigurera AAD eller AADB2C med en Authority</span><span class="sxs-lookup"><span data-stu-id="71536-2669">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="71536-2670">Konfigurera SignupPolicy, SigninPolicy, ProfileEditingPolicy och PasswordResetPolicy</span><span class="sxs-lookup"><span data-stu-id="71536-2670">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="71536-2671">Uppdaterad cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="71536-2671">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="71536-2672">Kompensera för ny SubscriptonModel med Scope och UserId</span><span class="sxs-lookup"><span data-stu-id="71536-2672">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="71536-2673">Kompensera för gammal prenumerationsmodell med ProductId och UserId</span><span class="sxs-lookup"><span data-stu-id="71536-2673">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="71536-2674">Lägg till funktion för att aktivera AllowTracing på prenumerationsnivå.</span><span class="sxs-lookup"><span data-stu-id="71536-2674">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="71536-2675">Uppdaterad cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="71536-2675">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="71536-2676">Kompensera för ny SubscriptonModel med Scope och UserId</span><span class="sxs-lookup"><span data-stu-id="71536-2676">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="71536-2677">Kompensera för gammal prenumerationsmodell med ProductId och UserId</span><span class="sxs-lookup"><span data-stu-id="71536-2677">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="71536-2678">Lägg till funktion för att aktivera AllowTracing på prenumerationsnivå.</span><span class="sxs-lookup"><span data-stu-id="71536-2678">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="71536-2679">Uppdaterade följande cmdletar för att acceptera ResourceId som indata</span><span class="sxs-lookup"><span data-stu-id="71536-2679">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="71536-2680">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="71536-2680">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="71536-2681">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="71536-2681">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="71536-2682">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="71536-2682">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="71536-2683">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="71536-2683">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="71536-2684">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="71536-2684">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="71536-2685">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="71536-2685">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="71536-2686">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="71536-2686">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="71536-2687">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="71536-2687">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="71536-2688">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="71536-2688">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="71536-2689">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="71536-2689">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="71536-2690">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="71536-2690">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="71536-2691">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="71536-2691">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="71536-2692">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="71536-2692">Az.Automation</span></span>
* <span data-ttu-id="71536-2693">Uppdaterade Get-AzAutomationJobOutputRecord för att hantera postvärden av typen JSON och Text.</span><span class="sxs-lookup"><span data-stu-id="71536-2693">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="71536-2694">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="71536-2694">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="71536-2695">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="71536-2695">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="71536-2696">Ändrade beteende för Start-AzAutomationDscCompilationJob till att bara starta jobbet istället för att vänta på slutförandet.</span><span class="sxs-lookup"><span data-stu-id="71536-2696">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="71536-2697">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="71536-2697">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="71536-2698">Korrigering för Get-AzAutomationDscNode när using -Name returnerar alla noder.</span><span class="sxs-lookup"><span data-stu-id="71536-2698">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="71536-2699">Nu returnerar den endast den matchande noden.</span><span class="sxs-lookup"><span data-stu-id="71536-2699">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71536-2700">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71536-2700">Az.Compute</span></span>
* <span data-ttu-id="71536-2701">Lägg till parametrarna ProtectFromScaleIn och ProtectFromScaleSetAction i cmdleten Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="71536-2701">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="71536-2702">Nu är standardinställningen att vimpelparametern New-AzVM använder en tillgänglig plats om USA, östra inte stöds</span><span class="sxs-lookup"><span data-stu-id="71536-2702">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="71536-2703">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="71536-2703">Az.DataLakeStore</span></span>
* <span data-ttu-id="71536-2704">Uppdatera ADLS-sdk för att använda httpclient, integrera dataplanstestning med Azure-ramverk</span><span class="sxs-lookup"><span data-stu-id="71536-2704">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="71536-2705">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="71536-2705">Az.Monitor</span></span>
* <span data-ttu-id="71536-2706">Korrigera felaktiga parameternamn i hjälpexempel</span><span class="sxs-lookup"><span data-stu-id="71536-2706">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71536-2707">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71536-2707">Az.Network</span></span>
* <span data-ttu-id="71536-2708">Lägg till flaggan DisableBgpRoutePropagation i utdata för effektiv routningstabell</span><span class="sxs-lookup"><span data-stu-id="71536-2708">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="71536-2709">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="71536-2709">Updated cmdlet:</span></span>
        - <span data-ttu-id="71536-2710">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="71536-2710">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="71536-2711">Åtgärda dubbelstreck i dokumentationen New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="71536-2711">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="71536-2712">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71536-2712">Az.Resources</span></span>
* <span data-ttu-id="71536-2713">Lägg till ny cmdlet Get-AzureRmDenyAssignment för att hämta tilldelningsnekanden</span><span class="sxs-lookup"><span data-stu-id="71536-2713">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="71536-2714">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71536-2714">Az.Sql</span></span>
* <span data-ttu-id="71536-2715">Döp om Advanced Threat Protection-cmdletar för Advanced Data Security och aktivera Vulnerability Assessment som standard</span><span class="sxs-lookup"><span data-stu-id="71536-2715">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="71536-2716">2.0.0 – maj 2019</span><span class="sxs-lookup"><span data-stu-id="71536-2716">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="71536-2717">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="71536-2717">Az.Accounts</span></span>
* <span data-ttu-id="71536-2718">Uppdatera autentiseringsbiblioteket för att åtgärda ADFS-problem med autentisering av användarnamn/lösenord</span><span class="sxs-lookup"><span data-stu-id="71536-2718">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="71536-2719">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="71536-2719">Az.CognitiveServices</span></span>
* <span data-ttu-id="71536-2720">Visa endast Bing-ansvarsfriskrivning för Bing-sökningstjänster.</span><span class="sxs-lookup"><span data-stu-id="71536-2720">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="71536-2721">Förbättra felmeddelande när det inte går att skapa konton.</span><span class="sxs-lookup"><span data-stu-id="71536-2721">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71536-2722">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71536-2722">Az.Compute</span></span>
* <span data-ttu-id="71536-2723">Funktion för närhetsplaceringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="71536-2723">Proximity placement group feature.</span></span>
    - <span data-ttu-id="71536-2724">Följande nya cmdletar har lagts till:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="71536-2724">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="71536-2725">Den nya parametern ProximityPlacementGroupId har lagts till i följande cmdletar:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="71536-2725">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="71536-2726">Parametern StorageAccountType har lagts till i New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="71536-2726">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="71536-2727">TargetRegion för New-AzGalleryImageVersion kan innehålla StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="71536-2727">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="71536-2728">Växlingsparametern SkipShutdown har lagts till i Stop-AzVM och Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="71536-2728">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="71536-2729">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="71536-2729">Breaking changes</span></span>
    - <span data-ttu-id="71536-2730">Set-AzVMBootDiagnostics har ändrats till Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="71536-2730">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="71536-2731">Export-AzLogAnalyticThrottledRequests har ändrats till Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="71536-2731">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="71536-2732">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="71536-2732">Az.DeploymentManager</span></span>
* <span data-ttu-id="71536-2733">De första allmänt tillgängliga versionerna av cmdletar för Distributionshanteraren i Azure</span><span class="sxs-lookup"><span data-stu-id="71536-2733">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="71536-2734">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="71536-2734">Az.Dns</span></span>
* <span data-ttu-id="71536-2735">Automatisk delegering av DNS för NameServer</span><span class="sxs-lookup"><span data-stu-id="71536-2735">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="71536-2736">Det överordnade zonnamnet kan användas som ytterligare valfri parameter i cmdleten för att skapa DNS-zoner.</span><span class="sxs-lookup"><span data-stu-id="71536-2736">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="71536-2737">Lägger till NS-poster för en nyligen skapad underordnad zon i den överordnade zonen.</span><span class="sxs-lookup"><span data-stu-id="71536-2737">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="71536-2738">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="71536-2738">Az.FrontDoor</span></span>
* <span data-ttu-id="71536-2739">De första allmänt tillgängliga versionerna av cmdletar för Azure FrontDoor</span><span class="sxs-lookup"><span data-stu-id="71536-2739">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="71536-2740">Byt namn på WAF-cmdletar så att de omfattar ”Waf”</span><span class="sxs-lookup"><span data-stu-id="71536-2740">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="71536-2741">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="71536-2741">Az.HDInsight</span></span>
* <span data-ttu-id="71536-2742">Två cmdletar har tagits bort:</span><span class="sxs-lookup"><span data-stu-id="71536-2742">Removed two cmdlets:</span></span>
    - <span data-ttu-id="71536-2743">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="71536-2743">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="71536-2744">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="71536-2744">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="71536-2745">En ny cmdlet har lagts till, Set-AzHDInsightGatewayCredential, som ersätter Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="71536-2745">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="71536-2746">Uppdatera cmdleten Get-AzHDInsightJobOutput för att skilja mellan läsarrollen och HDInsight-operatörsrollen:</span><span class="sxs-lookup"><span data-stu-id="71536-2746">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="71536-2747">Användare med läsarrollen måste uttryckligen ange parametern ”DefaultStorageAccountKey”, annars uppstår fel.</span><span class="sxs-lookup"><span data-stu-id="71536-2747">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="71536-2748">Användare med HDInsight-operatörsrollen påverkas inte.</span><span class="sxs-lookup"><span data-stu-id="71536-2748">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="71536-2749">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="71536-2749">Az.Monitor</span></span>
* <span data-ttu-id="71536-2750">Nya cmdletar för SQR API (schemalagd frågeregel)</span><span class="sxs-lookup"><span data-stu-id="71536-2750">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="71536-2751">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="71536-2751">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="71536-2752">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="71536-2752">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="71536-2753">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="71536-2753">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="71536-2754">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="71536-2754">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="71536-2755">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="71536-2755">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="71536-2756">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="71536-2756">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="71536-2757">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="71536-2757">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="71536-2758">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="71536-2758">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="71536-2759">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="71536-2759">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="71536-2760">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="71536-2760">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="71536-2761">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="71536-2761">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="71536-2762">[Mer](/rest/api/monitor/scheduledqueryrules) information om SQR API</span><span class="sxs-lookup"><span data-stu-id="71536-2762">[More](/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="71536-2763">Az.Monitor.md har uppdaterats för att omfatta cmdletar för måttbaserade aviseringsregler i GenV2 (inte klassiska)</span><span class="sxs-lookup"><span data-stu-id="71536-2763">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71536-2764">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71536-2764">Az.Network</span></span>
* <span data-ttu-id="71536-2765">Lägg till stöd för NAT Gateway-resurs</span><span class="sxs-lookup"><span data-stu-id="71536-2765">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="71536-2766">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="71536-2766">New cmdlets</span></span>
        - <span data-ttu-id="71536-2767">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="71536-2767">New-AzNatGateway</span></span>
        - <span data-ttu-id="71536-2768">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="71536-2768">Get-AzNatGateway</span></span>
        - <span data-ttu-id="71536-2769">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="71536-2769">Set-AzNatGateway</span></span>
        - <span data-ttu-id="71536-2770">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="71536-2770">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="71536-2771">Uppdaterade cmdletar</span><span class="sxs-lookup"><span data-stu-id="71536-2771">Updated cmdlets</span></span>
        - <span data-ttu-id="71536-2772">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="71536-2772">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="71536-2773">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="71536-2773">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="71536-2774">Nedanstående kommandon för funktionen har uppdaterats: Ange/ta bort anpassade vägar på Brooklyn Gateway.</span><span class="sxs-lookup"><span data-stu-id="71536-2774">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="71536-2775">New-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ställa in adressprefix som anpassade vägar för att ange gateway.</span><span class="sxs-lookup"><span data-stu-id="71536-2775">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="71536-2776">Set-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ange adressprefix som anpassade vägar för att ange gateway.</span><span class="sxs-lookup"><span data-stu-id="71536-2776">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="71536-2777">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="71536-2777">Az.PolicyInsights</span></span>
* <span data-ttu-id="71536-2778">Stöd för att fråga efter information om principutvärdering.</span><span class="sxs-lookup"><span data-stu-id="71536-2778">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="71536-2779">Lägg till parametern ”-Expand” för Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="71536-2779">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="71536-2780">Stöd för -Expand PolicyEvaluationDetails.</span><span class="sxs-lookup"><span data-stu-id="71536-2780">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="71536-2781">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="71536-2781">Az.RecoveryServices</span></span>
* <span data-ttu-id="71536-2782">Stöd för att dela prenumeration mellan Azure och Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="71536-2782">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="71536-2783">Markering av kommande icke-bakåtkompatibla ändringar för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="71536-2783">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="71536-2784">Korrigering för återställningsplan och åtgärdsplan i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="71536-2784">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="71536-2785">Korrigering för mappning av uppdateringsnätverk i Azure Site Recovery för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="71536-2785">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="71536-2786">Korrigering för instruktioner för uppdateringsskydd i Azure Site Recovery för Azure till Azure för hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="71536-2786">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="71536-2787">Andra mindre korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="71536-2787">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="71536-2788">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="71536-2788">Az.Relay</span></span>
* <span data-ttu-id="71536-2789">Korrigera stavfel i kundriktade meddelanden</span><span class="sxs-lookup"><span data-stu-id="71536-2789">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="71536-2790">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="71536-2790">Az.ServiceBus</span></span>
* <span data-ttu-id="71536-2791">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="71536-2791">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="71536-2792">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="71536-2792">Az.Storage</span></span>
* <span data-ttu-id="71536-2793">Uppgradera till lagringsklientbiblioteket 10.0.1 (namnområdet för alla objekt från detta SDK ändras från ”Microsoft.WindowsAzure.Storage. *till ”Microsoft.Azure.Storage.* ”)</span><span class="sxs-lookup"><span data-stu-id="71536-2793">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="71536-2794">Uppgradera till Microsoft.Azure.Management.Storage 11.0.0 för att stödja den nya API-versionen 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="71536-2794">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="71536-2795">Standardlagringskontot i Skapa lagringskonto ändras från ”Storage” till ”StorageV2”</span><span class="sxs-lookup"><span data-stu-id="71536-2795">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="71536-2796">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="71536-2796">New-AzStorageAccount</span></span>
* <span data-ttu-id="71536-2797">Ändra lagringskontots cmdlet-utdata Sku.Name för att passa med indata-SkuName genom att lägga till ”-”. Till exempel ändras ”StandardLRS” till ”Standard_LRS”</span><span class="sxs-lookup"><span data-stu-id="71536-2797">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="71536-2798">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="71536-2798">New-AzStorageAccount</span></span>
    - <span data-ttu-id="71536-2799">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="71536-2799">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="71536-2800">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="71536-2800">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="71536-2801">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="71536-2801">Az.Websites</span></span>
* <span data-ttu-id="71536-2802">Egenskapen ”typ” konfigureras nu för PSSite-objekt som returneras av Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="71536-2802">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="71536-2803">Get-AzWebApp\*Metrics och Get-AzAppServicePlanMetrics markeras som inaktuella</span><span class="sxs-lookup"><span data-stu-id="71536-2803">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="71536-2804">1.8.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="71536-2804">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="71536-2805">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="71536-2805">Highlights since the last major release</span></span>
* <span data-ttu-id="71536-2806">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="71536-2806">General availability of `Az` module</span></span>
* <span data-ttu-id="71536-2807">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="71536-2807">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="71536-2808">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="71536-2808">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="71536-2809">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-2809">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="71536-2810">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-2810">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="71536-2811">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-2811">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="71536-2812">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="71536-2812">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="71536-2813">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="71536-2813">Az.Accounts</span></span>
* <span data-ttu-id="71536-2814">Uppdatera Uninstall-AzureRm för att ta bort moduler i Mac på ett korrekt sätt</span><span class="sxs-lookup"><span data-stu-id="71536-2814">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="71536-2815">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="71536-2815">Az.Batch</span></span>
* <span data-ttu-id="71536-2816">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="71536-2816">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="71536-2817">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="71536-2817">Az.Cdn</span></span>
* <span data-ttu-id="71536-2818">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="71536-2818">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="71536-2819">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="71536-2819">Az.CognitiveServices</span></span>
* <span data-ttu-id="71536-2820">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="71536-2820">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71536-2821">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71536-2821">Az.Compute</span></span>
* <span data-ttu-id="71536-2822">Åtgärda problem med AEM-installationen om resurs-ID:n för diskar innehåller resourcegroups i gemener i resurs-ID:n</span><span class="sxs-lookup"><span data-stu-id="71536-2822">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="71536-2823">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="71536-2823">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="71536-2824">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="71536-2824">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="71536-2825">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="71536-2825">Az.DataFactory</span></span>
* <span data-ttu-id="71536-2826">Lägg till SsisProperties om NodeCount inte är null för hanterad integreringskörning.</span><span class="sxs-lookup"><span data-stu-id="71536-2826">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="71536-2827">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="71536-2827">Az.DataLakeStore</span></span>
* <span data-ttu-id="71536-2828">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="71536-2828">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="71536-2829">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="71536-2829">Az.EventGrid</span></span>
* <span data-ttu-id="71536-2830">Hjälptexten för slutpunkten har uppdaterats för att visa att resurser ska skapas innan cmdletarna för att skapa/uppdatera händelseprenumerationer används.</span><span class="sxs-lookup"><span data-stu-id="71536-2830">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="71536-2831">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="71536-2831">Az.EventHub</span></span>
* <span data-ttu-id="71536-2832">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="71536-2832">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="71536-2833">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="71536-2833">Az.HDInsight</span></span>
* <span data-ttu-id="71536-2834">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="71536-2834">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="71536-2835">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="71536-2835">Az.IotHub</span></span>
* <span data-ttu-id="71536-2836">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="71536-2836">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="71536-2837">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="71536-2837">Az.KeyVault</span></span>
* <span data-ttu-id="71536-2838">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="71536-2838">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="71536-2839">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="71536-2839">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="71536-2840">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="71536-2840">Az.MachineLearning</span></span>
* <span data-ttu-id="71536-2841">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="71536-2841">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="71536-2842">Az.Media</span><span class="sxs-lookup"><span data-stu-id="71536-2842">Az.Media</span></span>
* <span data-ttu-id="71536-2843">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="71536-2843">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="71536-2844">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="71536-2844">Az.Monitor</span></span>
  * <span data-ttu-id="71536-2845">Nya cmdletar för måttbaserad aviseringsregel i GenV2 (inte klassisk)</span><span class="sxs-lookup"><span data-stu-id="71536-2845">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="71536-2846">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="71536-2846">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="71536-2847">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="71536-2847">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="71536-2848">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="71536-2848">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="71536-2849">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="71536-2849">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="71536-2850">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="71536-2850">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="71536-2851">Monitor SDK har uppdaterats till version 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="71536-2851">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71536-2852">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71536-2852">Az.Network</span></span>
* <span data-ttu-id="71536-2853">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="71536-2853">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="71536-2854">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="71536-2854">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="71536-2855">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="71536-2855">Az.NotificationHubs</span></span>
* <span data-ttu-id="71536-2856">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="71536-2856">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="71536-2857">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="71536-2857">Az.OperationalInsights</span></span>
* <span data-ttu-id="71536-2858">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="71536-2858">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="71536-2859">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="71536-2859">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="71536-2860">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="71536-2860">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="71536-2861">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="71536-2861">Az.RecoveryServices</span></span>
* <span data-ttu-id="71536-2862">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="71536-2862">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="71536-2863">Tabellformatet för SQL i virtuella Azure-datorer har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="71536-2863">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="71536-2864">En alternativ metod för att hämta platser i AzureFileShare har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-2864">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="71536-2865">ScheduleRunDays i SchedulePolicy-objekt har uppdaterats enligt tidszon</span><span class="sxs-lookup"><span data-stu-id="71536-2865">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="71536-2866">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="71536-2866">Az.RedisCache</span></span>
* <span data-ttu-id="71536-2867">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="71536-2867">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="71536-2868">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71536-2868">Az.Resources</span></span>
* <span data-ttu-id="71536-2869">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="71536-2869">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="71536-2870">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71536-2870">Az.Sql</span></span>
* <span data-ttu-id="71536-2871">Ersätt Monitor SDK-beroende med vanlig kod</span><span class="sxs-lookup"><span data-stu-id="71536-2871">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="71536-2872">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="71536-2872">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="71536-2873">Förbättrad process för klassificering av flera kolumner.</span><span class="sxs-lookup"><span data-stu-id="71536-2873">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="71536-2874">Inkludera SKU-egenskaper (SKU-namn, serie, kapacitet) i svaret från Get-AzSqlServerServiceObjective och formatera som tabell som standard.</span><span class="sxs-lookup"><span data-stu-id="71536-2874">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="71536-2875">Möjlighet att använda Get-AzSqlServerServiceObjective efter plats utan att behöva en redan befintlig server i regionen.</span><span class="sxs-lookup"><span data-stu-id="71536-2875">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="71536-2876">Stöd för tidszonsparametern när hanterade instanser skapas.</span><span class="sxs-lookup"><span data-stu-id="71536-2876">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="71536-2877">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="71536-2877">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="71536-2878">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="71536-2878">Az.Websites</span></span>
* <span data-ttu-id="71536-2879">åtgärdar Set-AzWebApp och Set-AzWebAppSlot så att de inte tar bort taggar vid körning</span><span class="sxs-lookup"><span data-stu-id="71536-2879">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="71536-2880">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="71536-2880">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="71536-2881">SDK för WebSites har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="71536-2881">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="71536-2882">Egenskapen AdminSiteName har tagits bort från PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="71536-2882">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="71536-2883">1.7.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="71536-2883">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="71536-2884">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="71536-2884">Highlights since the last major release</span></span>
* <span data-ttu-id="71536-2885">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="71536-2885">General availability of `Az` module</span></span>
* <span data-ttu-id="71536-2886">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="71536-2886">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="71536-2887">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="71536-2887">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="71536-2888">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-2888">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="71536-2889">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-2889">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="71536-2890">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-2890">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="71536-2891">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="71536-2891">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="71536-2892">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="71536-2892">Az.Accounts</span></span>
* <span data-ttu-id="71536-2893">Add-AzEnvironment och Set-AzEnvironment har uppdaterats för att godkänna parametern AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="71536-2893">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="71536-2894">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="71536-2894">Az.AnalysisServices</span></span>
* <span data-ttu-id="71536-2895">ServiceClient används i cmdletar för dataplan och den ursprungliga autentiseringslogiken har tagits bort</span><span class="sxs-lookup"><span data-stu-id="71536-2895">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="71536-2896">Add-AzureASAccount används för omslutning av Connect-AzAccount för att undvika en icke-bakåtkompatibel ändring</span><span class="sxs-lookup"><span data-stu-id="71536-2896">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="71536-2897">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="71536-2897">Az.Automation</span></span>
* <span data-ttu-id="71536-2898">Buggen för cmdleten New-AzAutomationSoftwareUpdateConfiguration för inkluderingar har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="71536-2898">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="71536-2899">Nu bör parametern IncludedKbNumber och IncludedPackageNameMask fungera.</span><span class="sxs-lookup"><span data-stu-id="71536-2899">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="71536-2900">Felkorrigering för dynamiska grupper i uppdateringshanteringen för azure automation</span><span class="sxs-lookup"><span data-stu-id="71536-2900">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71536-2901">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71536-2901">Az.Compute</span></span>
* <span data-ttu-id="71536-2902">Lägg till parametern HyperVGeneration i New-AzDiskConfig och New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="71536-2902">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="71536-2903">Tillåt att virtuella datorer skapas med galleribilder från andra klientorganisationer.</span><span class="sxs-lookup"><span data-stu-id="71536-2903">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="71536-2904">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="71536-2904">Az.ContainerInstance</span></span>
* <span data-ttu-id="71536-2905">Ett problem har åtgärdats i parametern -Command för New-AzContainerGroup som lade till ett avslutande tomt argument</span><span class="sxs-lookup"><span data-stu-id="71536-2905">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="71536-2906">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="71536-2906">Az.DataFactory</span></span>
* <span data-ttu-id="71536-2907">ADF .Net SDK-versionen har uppdaterats till 3.0.2</span><span class="sxs-lookup"><span data-stu-id="71536-2907">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="71536-2908">Cmdleten Set-AzDataFactoryV2 har uppdaterats med extra parametrar för inställningar som rör RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="71536-2908">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="71536-2909">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71536-2909">Az.Resources</span></span>
* <span data-ttu-id="71536-2910">Förbättra hanteringen av providrar för Get-AzResource när parametrarna -ResourceId eller -ResourceGroupName, -Name och -ResourceType tillhandahålls</span><span class="sxs-lookup"><span data-stu-id="71536-2910">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="71536-2911">Förbättra felhanteringen för ”Test-AzDeployment” och ”Test-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="71536-2911">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="71536-2912">Hantera fel utanför distributionsvalideringen och ta med dem i kommandoutdata istället</span><span class="sxs-lookup"><span data-stu-id="71536-2912">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="71536-2913">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="71536-2913">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="71536-2914">Lägg till växlingsparametern -IgnoreDynamicParameters till en uppsättning av cmdletar för distribution för att hoppa över fråga i skript och jobbscenarier</span><span class="sxs-lookup"><span data-stu-id="71536-2914">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="71536-2915">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="71536-2915">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="71536-2916">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71536-2916">Az.Sql</span></span>
* <span data-ttu-id="71536-2917">Stöd för dataklassificering av databaser.</span><span class="sxs-lookup"><span data-stu-id="71536-2917">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="71536-2918">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="71536-2918">Az.Storage</span></span>
* <span data-ttu-id="71536-2919">Rapportera detaljfel när lagringskontext skapas med parametern -UseConnectedAccount, men utan inloggning på Azure-kontot</span><span class="sxs-lookup"><span data-stu-id="71536-2919">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="71536-2920">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="71536-2920">New-AzStorageContext</span></span>
* <span data-ttu-id="71536-2921">Stöd för att hantera Blob Service-egenskaper för ett angivet lagringskonto med API:et för hanteringsplan</span><span class="sxs-lookup"><span data-stu-id="71536-2921">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="71536-2922">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="71536-2922">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="71536-2923">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="71536-2923">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="71536-2924">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="71536-2924">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="71536-2925">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="71536-2925">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="71536-2926">Stöd för -AsJob-cmdletar för att ladda upp och ladda ned blobar och filer</span><span class="sxs-lookup"><span data-stu-id="71536-2926">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="71536-2927">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="71536-2927">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="71536-2928">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="71536-2928">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="71536-2929">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="71536-2929">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="71536-2930">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="71536-2930">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="71536-2931">1.6.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="71536-2931">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="71536-2932">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="71536-2932">Highlights since the last major release</span></span>
* <span data-ttu-id="71536-2933">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="71536-2933">General availability of `Az` module</span></span>
* <span data-ttu-id="71536-2934">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="71536-2934">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="71536-2935">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="71536-2935">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="71536-2936">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-2936">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="71536-2937">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-2937">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="71536-2938">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-2938">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="71536-2939">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="71536-2939">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="71536-2940">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="71536-2940">Az.Automation</span></span>
* <span data-ttu-id="71536-2941">Azure Automation – ändring av uppdateringshantering för stöd för de nya funktionerna:</span><span class="sxs-lookup"><span data-stu-id="71536-2941">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="71536-2942">Dynamisk gruppering</span><span class="sxs-lookup"><span data-stu-id="71536-2942">Dynamic grouping</span></span>
    * <span data-ttu-id="71536-2943">För-/efterskrift</span><span class="sxs-lookup"><span data-stu-id="71536-2943">Pre-Post script</span></span>
    * <span data-ttu-id="71536-2944">Inställning för omstart</span><span class="sxs-lookup"><span data-stu-id="71536-2944">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71536-2945">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71536-2945">Az.Compute</span></span>
* <span data-ttu-id="71536-2946">Åtgärda problem med sökvägsmatchning i Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="71536-2946">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="71536-2947">Uppdatera Compute-klientbibliotek till 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="71536-2947">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="71536-2948">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="71536-2948">Az.KeyVault</span></span>
* <span data-ttu-id="71536-2949">Stöd för jokertecken för KeyVault-cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-2949">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71536-2950">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71536-2950">Az.Network</span></span>
* <span data-ttu-id="71536-2951">Lägg till stöd för Threat Intelligence för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="71536-2951">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="71536-2952">Lägg till resurs för brandväggsprincip på översta nivå och anpassade regler för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="71536-2952">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="71536-2953">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="71536-2953">Az.RecoveryServices</span></span>
* <span data-ttu-id="71536-2954">SnapshotRetentionInDays har lagts till i Azure-principen för virtuella datorer för stöd av Instant RP</span><span class="sxs-lookup"><span data-stu-id="71536-2954">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="71536-2955">Pipe-stöd för avregistrering av container har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-2955">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="71536-2956">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71536-2956">Az.Resources</span></span>
* <span data-ttu-id="71536-2957">Uppdatera stöd för jokertecken för Get-AzResource och Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="71536-2957">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="71536-2958">Uppdatera autentiseringsuppgifter som används vid allmänna anrop till ARM</span><span class="sxs-lookup"><span data-stu-id="71536-2958">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="71536-2959">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71536-2959">Az.Sql</span></span>
* <span data-ttu-id="71536-2960">Cmdlet-parametern (ExcludeDetectionType) för Hotidentifiering ändrades från DetectionType till sträng[] för att framtidssäkra den när nya DetectionTypes läggs till, och även för att stödja automatisk ifyllning.</span><span class="sxs-lookup"><span data-stu-id="71536-2960">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="71536-2961">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="71536-2961">Az.Storage</span></span>
* <span data-ttu-id="71536-2962">Stöd för att hämta/ange/ta bort hanteringsprincip på ett lagringskonto</span><span class="sxs-lookup"><span data-stu-id="71536-2962">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="71536-2963">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="71536-2963">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="71536-2964">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="71536-2964">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="71536-2965">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="71536-2965">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="71536-2966">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="71536-2966">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="71536-2967">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="71536-2967">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="71536-2968">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="71536-2968">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="71536-2969">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="71536-2969">Az.Websites</span></span>
* <span data-ttu-id="71536-2970">Åtgärda fel med ARM-mall som avbryter kloning av alla platser med 'New-AzWebApp -IncludeSourceWebAppSlots'</span><span class="sxs-lookup"><span data-stu-id="71536-2970">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="71536-2971">1.5.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="71536-2971">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="71536-2972">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="71536-2972">Az.Accounts</span></span>
* <span data-ttu-id="71536-2973">Lägg till kommandot Register-AzModule för stöd för AutoRest-genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="71536-2973">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="71536-2974">Uppdatera exempel för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="71536-2974">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="71536-2975">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="71536-2975">Az.Automation</span></span>
* <span data-ttu-id="71536-2976">Problem med att hämta vissa månadsscheman i flera Azure Automation-cmdletar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="71536-2976">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="71536-2977">Åtgärda problem med att Get-AzAutomationDscNode bara returnerar de 20 översta noderna.</span><span class="sxs-lookup"><span data-stu-id="71536-2977">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="71536-2978">Nu returneras alla noder</span><span class="sxs-lookup"><span data-stu-id="71536-2978">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="71536-2979">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="71536-2979">Az.Cdn</span></span>
* <span data-ttu-id="71536-2980">Nya Powershell-cmdletar för att aktivera/inaktivera anpassade domän-HTTPS har lagts till och de gamla har gjorts inaktuella</span><span class="sxs-lookup"><span data-stu-id="71536-2980">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71536-2981">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71536-2981">Az.Compute</span></span>
* <span data-ttu-id="71536-2982">Lägg till stöd för jokertecken för Get-cmdletar</span><span class="sxs-lookup"><span data-stu-id="71536-2982">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="71536-2983">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="71536-2983">Az.DataFactory</span></span>
* <span data-ttu-id="71536-2984">ADF .Net SDK-versionen har uppdaterats till 3.0.1</span><span class="sxs-lookup"><span data-stu-id="71536-2984">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="71536-2985">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="71536-2985">Az.LogicApp</span></span>
* <span data-ttu-id="71536-2986">Åtgärda problemet med att ListWorkflows endast hämtar den första sidan med resultat</span><span class="sxs-lookup"><span data-stu-id="71536-2986">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71536-2987">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71536-2987">Az.Network</span></span>
* <span data-ttu-id="71536-2988">Lägg till stöd för jokertecken för Network-cmdletar</span><span class="sxs-lookup"><span data-stu-id="71536-2988">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="71536-2989">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="71536-2989">Az.RecoveryServices</span></span>
* <span data-ttu-id="71536-2990">Stöd har lagts till för SQL Server i virtuella Azure-datorer</span><span class="sxs-lookup"><span data-stu-id="71536-2990">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="71536-2991">SDK-uppdatering</span><span class="sxs-lookup"><span data-stu-id="71536-2991">SDK Update</span></span>
* <span data-ttu-id="71536-2992">Get-ProtectableItem-incheckning i VMappContainer har tagits bort</span><span class="sxs-lookup"><span data-stu-id="71536-2992">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="71536-2993">Name och ServerName har lagts till som parametrar för Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="71536-2993">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="71536-2994">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71536-2994">Az.Resources</span></span>
* <span data-ttu-id="71536-2995">Lägg till parametern `-TemplateObject` i cmdletar för distribution</span><span class="sxs-lookup"><span data-stu-id="71536-2995">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="71536-2996">Mer information här: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="71536-2996">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="71536-2997">Åtgärda problem med piping av resultatet i `Get-AzResource` till `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="71536-2997">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="71536-2998">Mer information här: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="71536-2998">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="71536-2999">Åtgärda problem med ändring av JSON-datatyp när `Set-AzResource` körs</span><span class="sxs-lookup"><span data-stu-id="71536-2999">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="71536-3000">Mer information här: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="71536-3000">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="71536-3001">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71536-3001">Az.Sql</span></span>
* <span data-ttu-id="71536-3002">AuditingEndpointsCommunicator uppdateras.</span><span class="sxs-lookup"><span data-stu-id="71536-3002">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="71536-3003">Åtgärdar beteendet hos ett gränsscenario när nya diagnostikinställningar skapas.</span><span class="sxs-lookup"><span data-stu-id="71536-3003">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="71536-3004">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="71536-3004">Az.Storage</span></span>
* <span data-ttu-id="71536-3005">Stöd för BlockBlobStorage när Storage-konto skapas      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="71536-3005">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="71536-3006">1.4.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="71536-3006">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="71536-3007">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="71536-3007">Az.AnalysisServices</span></span>
* <span data-ttu-id="71536-3008">Inaktuell AddAzureASAccount-cmdlet</span><span class="sxs-lookup"><span data-stu-id="71536-3008">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="71536-3009">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="71536-3009">Az.Automation</span></span>
* <span data-ttu-id="71536-3010">Hjälpen för Import-AzAutomationDscNodeConfiguration har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="71536-3010">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="71536-3011">Konfigurationsnamnsvalidering har lagts till i cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="71536-3011">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="71536-3012">Förbättrad felhantering för cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="71536-3012">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="71536-3013">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="71536-3013">Az.CognitiveServices</span></span>
* <span data-ttu-id="71536-3014">CustomSubdomainName har lagts till som en ny valfri parameter för New-AzCognitiveServicesAccount, som används för att ange underdomän för resursen.</span><span class="sxs-lookup"><span data-stu-id="71536-3014">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71536-3015">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71536-3015">Az.Compute</span></span>
* <span data-ttu-id="71536-3016">Problemet med ID-parameteruppsättningar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="71536-3016">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="71536-3017">Get-AzVMExtension har uppdaterats så att alla installerade tillägg visas om parametern Name inte har angetts</span><span class="sxs-lookup"><span data-stu-id="71536-3017">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="71536-3018">Parametrarna Tag och ResourceId har lagts till i cmdleten Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="71536-3018">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="71536-3019">Get-AzVmssVM utan instans-ID och med InstanceView kan visa virtuella VMSS-datorer med instansvyn.</span><span class="sxs-lookup"><span data-stu-id="71536-3019">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="71536-3020">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="71536-3020">Az.DataLakeStore</span></span>
* <span data-ttu-id="71536-3021">Cmdletar har lagts till för uppräkning och återställning av borttagna objekt i ADL</span><span class="sxs-lookup"><span data-stu-id="71536-3021">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="71536-3022">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="71536-3022">Az.EventHub</span></span>
* <span data-ttu-id="71536-3023">Ny boolesk egenskap SkipEmptyArchives har lagts till i Skip Empty Archives i CaptureDescription-klassen i Eventhub</span><span class="sxs-lookup"><span data-stu-id="71536-3023">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="71536-3024">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="71536-3024">Az.KeyVault</span></span>
* <span data-ttu-id="71536-3025">Taggning i Set-AzKeyVaultSecret har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="71536-3025">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="71536-3026">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="71536-3026">Az.LogicApp</span></span>
* <span data-ttu-id="71536-3027">Grundläggande SKU har lagts till för Integrationskonton</span><span class="sxs-lookup"><span data-stu-id="71536-3027">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="71536-3028">XSLT 2.0, XSLT 3.0 och Flytande mappningstyper har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-3028">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="71536-3029">Nya cmdletar för integrationskontosammansättningar</span><span class="sxs-lookup"><span data-stu-id="71536-3029">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="71536-3030">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="71536-3030">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="71536-3031">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="71536-3031">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="71536-3032">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="71536-3032">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="71536-3033">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="71536-3033">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="71536-3034">Nya cmdletar för batchkonfiguration för integrationskonto</span><span class="sxs-lookup"><span data-stu-id="71536-3034">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="71536-3035">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="71536-3035">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="71536-3036">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="71536-3036">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="71536-3037">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="71536-3037">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="71536-3038">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="71536-3038">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="71536-3039">Logic App-SDK har uppdaterats till version 4.1.0</span><span class="sxs-lookup"><span data-stu-id="71536-3039">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="71536-3040">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="71536-3040">Az.Monitor</span></span>
* <span data-ttu-id="71536-3041">Hjälpen för Get-AzMetric har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="71536-3041">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71536-3042">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71536-3042">Az.Network</span></span>
* <span data-ttu-id="71536-3043">Hjälpexempel för Add-AzApplicationGatewayCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-3043">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="71536-3044">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="71536-3044">Az.OperationalInsights</span></span>
* <span data-ttu-id="71536-3045">Ytterligare stöd för datakällorna New och Get ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="71536-3045">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="71536-3046">Ny ApplicationInsights-typ har lagts till för att ge stöd för ”Get specific” och ”Get all” för ApplicationInsights-datakällor för angiven arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="71536-3046">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="71536-3047">Cmdleten New-AzOperationalInsightsApplicationInsightsDataSource har lagts till för att skapa datakälla med angivna parametrar för Application Insights-resurs: subscription Id, resourceGroupName och name.</span><span class="sxs-lookup"><span data-stu-id="71536-3047">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="71536-3048">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71536-3048">Az.Resources</span></span>
* <span data-ttu-id="71536-3049">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="71536-3049">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="71536-3050">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="71536-3050">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="71536-3051">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="71536-3051">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="71536-3052">Fel som gör att KeyCredentials inte kan skapas upprepade gånger har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="71536-3052">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="71536-3053">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71536-3053">Az.Sql</span></span>
* <span data-ttu-id="71536-3054">Lägg till stöd för hyperskalanivån för SQL DB</span><span class="sxs-lookup"><span data-stu-id="71536-3054">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="71536-3055">Ett fel har åtgärdats där återställningen kunde misslyckas på grund av onödiga inställningsegenskaper i restore-förfrågan</span><span class="sxs-lookup"><span data-stu-id="71536-3055">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="71536-3056">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="71536-3056">Az.Websites</span></span>
* <span data-ttu-id="71536-3057">Rätt exempel i Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="71536-3057">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="71536-3058">1.3.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="71536-3058">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="71536-3059">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="71536-3059">Az.Accounts</span></span>
* <span data-ttu-id="71536-3060">Uppdatera till den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="71536-3060">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="71536-3061">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="71536-3061">Az.AnalysisServices</span></span>
<span data-ttu-id="71536-3062">Allmän tillgänglighet för Az.AnalysisServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="71536-3062">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71536-3063">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71536-3063">Az.Compute</span></span>
* <span data-ttu-id="71536-3064">AEM-tillägg: Lägg till stöd för UltraSSD-, P60-, P70- och P80-diskar</span><span class="sxs-lookup"><span data-stu-id="71536-3064">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="71536-3065">Uppdatera hjälpbeskrivning för Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="71536-3065">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="71536-3066">Uppdatera hjälpbeskrivning och exempel för Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="71536-3066">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="71536-3067">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="71536-3067">Az.RecoveryServices</span></span>
<span data-ttu-id="71536-3068">Allmän tillgänglighet för Az.RecoveryServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="71536-3068">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="71536-3069">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71536-3069">Az.Resources</span></span>
* <span data-ttu-id="71536-3070">Korrigera taggar för resursgrupper</span><span class="sxs-lookup"><span data-stu-id="71536-3070">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="71536-3071">Mer information här: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="71536-3071">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="71536-3072">Åtgärda problem där `Get-AzureRmRoleAssignment` inte respekterar -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="71536-3072">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="71536-3073">Mer information här: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="71536-3073">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="71536-3074">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71536-3074">Az.Sql</span></span>
* <span data-ttu-id="71536-3075">Lägga till Get/Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="71536-3075">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="71536-3076">Åtgärda problem där ett nullref-undantag uppstår när du kör SQL-cmdletar och inte är inloggad på ett Azure-konto</span><span class="sxs-lookup"><span data-stu-id="71536-3076">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="71536-3077">Åtgärda nullref-undantag i Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="71536-3077">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="71536-3078">1.2.1 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="71536-3078">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="71536-3079">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="71536-3079">Az.Accounts</span></span>
* <span data-ttu-id="71536-3080">Version med rätt version av autentisering</span><span class="sxs-lookup"><span data-stu-id="71536-3080">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="71536-3081">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="71536-3081">Az.AnalysisServices</span></span>
* <span data-ttu-id="71536-3082">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="71536-3082">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="71536-3083">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="71536-3083">Az.RecoveryServices</span></span>
* <span data-ttu-id="71536-3084">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="71536-3084">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="71536-3085">1.2.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="71536-3085">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="71536-3086">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="71536-3086">Az.Accounts</span></span>
* <span data-ttu-id="71536-3087">Lägga till interaktiv autentisering och autentisering med användarnamn/lösenord för endast Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="71536-3087">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="71536-3088">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="71536-3088">Update incorrect online help URLs</span></span>
* <span data-ttu-id="71536-3089">Lägga till varningsmeddelande i PS Core för Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="71536-3089">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="71536-3090">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="71536-3090">Az.Aks</span></span>
* <span data-ttu-id="71536-3091">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="71536-3091">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="71536-3092">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="71536-3092">Az.Automation</span></span>
* <span data-ttu-id="71536-3093">Stöd för Python 2-runbookflöden har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-3093">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="71536-3094">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="71536-3094">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="71536-3095">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="71536-3095">Az.Cdn</span></span>
* <span data-ttu-id="71536-3096">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="71536-3096">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71536-3097">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71536-3097">Az.Compute</span></span>
* <span data-ttu-id="71536-3098">Lägga till cmdleten Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="71536-3098">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="71536-3099">Lägga till TempDisk-parameter i Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="71536-3099">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="71536-3100">Korrigera varningsmeddelande för New-AzVM</span><span class="sxs-lookup"><span data-stu-id="71536-3100">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="71536-3101">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="71536-3101">Az.ContainerRegistry</span></span>
* <span data-ttu-id="71536-3102">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="71536-3102">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="71536-3103">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="71536-3103">Az.DataFactory</span></span>
* <span data-ttu-id="71536-3104">ADF .Net SDK-versionen har uppdaterats till 3.0.0</span><span class="sxs-lookup"><span data-stu-id="71536-3104">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="71536-3105">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="71536-3105">Az.DataLakeStore</span></span>
* <span data-ttu-id="71536-3106">Åtgärda problem med ADLS-slutpunkt vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="71536-3106">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="71536-3107">Mer information här: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="71536-3107">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="71536-3108">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="71536-3108">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="71536-3109">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="71536-3109">Az.IotHub</span></span>
* <span data-ttu-id="71536-3110">Lägga till kodningsformat i cmdleten Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="71536-3110">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="71536-3111">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="71536-3111">Az.KeyVault</span></span>
* <span data-ttu-id="71536-3112">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="71536-3112">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71536-3113">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71536-3113">Az.Network</span></span>
* <span data-ttu-id="71536-3114">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="71536-3114">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="71536-3115">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71536-3115">Az.Resources</span></span>
* <span data-ttu-id="71536-3116">Åtgärda felaktiga exempel i referensdokumentationen ”New-AzADAppCredential” och ”New-AzADSpCredential”</span><span class="sxs-lookup"><span data-stu-id="71536-3116">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="71536-3117">Åtgärda problem där sökvägen för parametern ”-TemplateFile” inte omvandlas innan cmdletarna för distribution i resursgruppen körs</span><span class="sxs-lookup"><span data-stu-id="71536-3117">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="71536-3118">Az.Resources: Korrigera dokumentationen om standardvärdet för New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="71536-3118">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="71536-3119">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="71536-3119">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="71536-3120">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="71536-3120">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="71536-3121">Åtgärda formateringsproblemet med objektet ”PSResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="71536-3121">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="71536-3122">Mer information här: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="71536-3122">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="71536-3123">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="71536-3123">Az.ServiceFabric</span></span>
* <span data-ttu-id="71536-3124">Återställ när ett certifikat läggs till i en Virtual Machine Scale Sets-modell men ett undantag genereras. Detta har gjorts för att åtgärda följande fel: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="71536-3124">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="71536-3125">Korrigera några felmeddelanden.</span><span class="sxs-lookup"><span data-stu-id="71536-3125">Fix some error messages.</span></span>
* <span data-ttu-id="71536-3126">Korrigering av skapande av kluster med ARM-mall som är standard för New-AzServiceFabriCluster som inte fungerade med migrering till Az.</span><span class="sxs-lookup"><span data-stu-id="71536-3126">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="71536-3127">Korrigering av tilläggning av kluster/programcertifikat så att endast VM Scale Sets som motsvarar klustret läggs till genom att kontrollera ID för klustret i tillägget.</span><span class="sxs-lookup"><span data-stu-id="71536-3127">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="71536-3128">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="71536-3128">Az.SignalR</span></span>
* <span data-ttu-id="71536-3129">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="71536-3129">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="71536-3130">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71536-3130">Az.Sql</span></span>
* <span data-ttu-id="71536-3131">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="71536-3131">Update incorrect online help URLs</span></span>
* <span data-ttu-id="71536-3132">Uppdaterad parameterbeskrivning för LicenseType-parameter med möjliga värden</span><span class="sxs-lookup"><span data-stu-id="71536-3132">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="71536-3133">Korrigering för att uppdatera hanterad instansidentitet som inte fungerar när det är den enda uppdaterade egenskapen</span><span class="sxs-lookup"><span data-stu-id="71536-3133">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="71536-3134">Stöd för anpassad sortering på hanterad instans</span><span class="sxs-lookup"><span data-stu-id="71536-3134">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="71536-3135">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="71536-3135">Az.Storage</span></span>
* <span data-ttu-id="71536-3136">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="71536-3136">Update incorrect online help URLs</span></span>
* <span data-ttu-id="71536-3137">Tillhandahåll detaljerat felmeddelande när en användare försöker hämta/konfigurera klassisk loggning/mått på ett Premium Storage-konto eftersom Premium Storage-kontot inte har stöd för klassisk loggning/mått.</span><span class="sxs-lookup"><span data-stu-id="71536-3137">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="71536-3138">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="71536-3138">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="71536-3139">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="71536-3139">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="71536-3140">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="71536-3140">Az.TrafficManager</span></span>
* <span data-ttu-id="71536-3141">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="71536-3141">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="71536-3142">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="71536-3142">Az.Websites</span></span>
* <span data-ttu-id="71536-3143">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="71536-3143">Update incorrect online help URLs</span></span>
* <span data-ttu-id="71536-3144">Korrigerar ”New-AzWebAppSSLBinding” så att certifikatet laddas upp till rätt resursgrupp och plats om appen finns i en ASE.</span><span class="sxs-lookup"><span data-stu-id="71536-3144">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="71536-3145">Korrigerar ”New-AzWebAppSSLBinding” så att taggarna inte skrivs över på en bindning av ett SSL-certifikat till en app</span><span class="sxs-lookup"><span data-stu-id="71536-3145">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="71536-3146">1.1.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="71536-3146">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="71536-3147">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="71536-3147">Az.Accounts</span></span>
* <span data-ttu-id="71536-3148">Lade till omfattningen ”Lokal” till Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="71536-3148">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71536-3149">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71536-3149">Az.Compute</span></span>
* <span data-ttu-id="71536-3150">Namn är nu valfritt i ID-parametern för Restart/Start/Stop/Remove/Set-AzVM och Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="71536-3150">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="71536-3151">Uppdaterade beskrivningen av ID i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="71536-3151">Updated the description of ID in help files</span></span>
* <span data-ttu-id="71536-3152">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="71536-3152">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="71536-3153">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="71536-3153">Az.DataLakeStore</span></span>
* <span data-ttu-id="71536-3154">Uppdatera sdk-versionen av dataplanet till 1.1.14 för SDK-korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="71536-3154">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="71536-3155">Korrigerade hanteringen av negativ accesstime och modificationtime för getfilestatus och liststatus; korrigera asynkront annulleringstoken</span><span class="sxs-lookup"><span data-stu-id="71536-3155">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="71536-3156">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="71536-3156">Az.EventGrid</span></span>
* <span data-ttu-id="71536-3157">Uppdaterat för användning av API-versionen 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="71536-3157">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="71536-3158">Uppdaterade följande cmdletar för att stödja nytt scenario i API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="71536-3158">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="71536-3159">New-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="71536-3159">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="71536-3160">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="71536-3160">Event Time-To-Live,</span></span>
        - <span data-ttu-id="71536-3161">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="71536-3161">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="71536-3162">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="71536-3162">Dead letter endpoint.</span></span>
    - <span data-ttu-id="71536-3163">Update-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="71536-3163">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="71536-3164">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="71536-3164">Event Time-To-Live,</span></span>
        - <span data-ttu-id="71536-3165">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="71536-3165">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="71536-3166">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="71536-3166">Dead letter endpoint.</span></span>
* <span data-ttu-id="71536-3167">Lade till nya enum-värden (storageQueue och hybridConnection) för alternativet EndpointType i cmdletarna New-AzureRmEventGridSubscription och Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="71536-3167">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="71536-3168">Visa varningsmeddelanden om skapande eller uppdatering av händelseprenumerationen förväntas medföra manuell åtgärd från användaren.</span><span class="sxs-lookup"><span data-stu-id="71536-3168">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="71536-3169">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="71536-3169">Az.IotHub</span></span>
* <span data-ttu-id="71536-3170">Har uppdaterats till den senaste versionen av SDK:n lotHub</span><span class="sxs-lookup"><span data-stu-id="71536-3170">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="71536-3171">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="71536-3171">Az.LogicApp</span></span>
* <span data-ttu-id="71536-3172">Get-AzLogicApp visar en lista över alla som inte har angivet namn</span><span class="sxs-lookup"><span data-stu-id="71536-3172">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="71536-3173">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71536-3173">Az.Resources</span></span>
* <span data-ttu-id="71536-3174">Åtgärdade problem med parameteruppsättningen när parametrarna -ODataQuery och -ResourceId anges för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="71536-3174">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="71536-3175">Mer information här: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="71536-3175">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="71536-3176">Åtgärdade hantering av parametern -Custom i New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="71536-3176">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="71536-3177">Korrigerade stavfel i New-AzDeployment-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="71536-3177">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="71536-3178">Gjorde parametern -MailNickname obligatorisk för New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="71536-3178">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="71536-3179">Mer information här: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="71536-3179">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="71536-3180">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="71536-3180">Az.SignalR</span></span>
* <span data-ttu-id="71536-3181">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="71536-3181">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="71536-3182">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71536-3182">Az.Sql</span></span>
* <span data-ttu-id="71536-3183">Konverterade lagringshanteringsklientens beroende av den normala SDK-implementeringen.</span><span class="sxs-lookup"><span data-stu-id="71536-3183">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="71536-3184">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="71536-3184">Az.Storage</span></span>
* <span data-ttu-id="71536-3185">Angav StorageAccountName för lagringskontext som det verkliga namnet på lagringskontot när det skapas med Sas Token, OAuth eller Anonymous</span><span class="sxs-lookup"><span data-stu-id="71536-3185">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="71536-3186">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="71536-3186">New-AzStorageContext</span></span>
* <span data-ttu-id="71536-3187">Skapade Sas Token för Blob Snapshot-objekt med parametern -FullUri, åtgärdade den returnerade URI:n så att den blir URI för ögonblicksbild</span><span class="sxs-lookup"><span data-stu-id="71536-3187">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="71536-3188">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="71536-3188">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="71536-3189">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="71536-3189">Az.Websites</span></span>
* <span data-ttu-id="71536-3190">Åtgärdade en bugg i datumparsningen i Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="71536-3190">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="71536-3191">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="71536-3191">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="71536-3192">1.0.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="71536-3192">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="71536-3193">Allmänt</span><span class="sxs-lookup"><span data-stu-id="71536-3193">General</span></span>

- <span data-ttu-id="71536-3194">Allmän tillgänglighet för Az-modulen</span><span class="sxs-lookup"><span data-stu-id="71536-3194">General Availability of Az Module</span></span>
- <span data-ttu-id="71536-3195">Onlinehjälp för varje modul</span><span class="sxs-lookup"><span data-stu-id="71536-3195">Online help for each module</span></span>
- <span data-ttu-id="71536-3196">Mer information och en översikt finns på [Az-informationssidan](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="71536-3196">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="71536-3197">Information om hur du migrerar från AzureRM finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="71536-3197">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="71536-3198">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="71536-3198">Az.Accounts</span></span>
- <span data-ttu-id="71536-3199">Har ändrats från Az.Profile</span><span class="sxs-lookup"><span data-stu-id="71536-3199">Changed from Az.Profile</span></span>
- <span data-ttu-id="71536-3200">Fasta tabellformat för profil- och kontexttyper</span><span class="sxs-lookup"><span data-stu-id="71536-3200">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="71536-3201">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="71536-3201">Az.ApiManagement</span></span>
- <span data-ttu-id="71536-3202">Korrigeringar för #7002</span><span class="sxs-lookup"><span data-stu-id="71536-3202">Fixes for #7002</span></span>
- <span data-ttu-id="71536-3203">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="71536-3203">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="71536-3204">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="71536-3204">Az.Batch</span></span>
- <span data-ttu-id="71536-3205">Lade till möjligheten att se vilken version av Azure Batch Node Agent som körs på var och en av de virtuella datorerna i en pool, via den nya egenskapen `NodeAgentInformation` på `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="71536-3205">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="71536-3206">Standarden `Caching` för `PSDataDisk` är nu `ReadWrite` i stället för `None`.</span><span class="sxs-lookup"><span data-stu-id="71536-3206">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="71536-3207">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="71536-3207">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="71536-3208">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="71536-3208">Az.Billing</span></span>
- <span data-ttu-id="71536-3209">Kombinerar cmdletarna för fakturering, förbrukning och UsageAggregates. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="71536-3209">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="71536-3210">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="71536-3210">Az.CognitivServices</span></span>
- <span data-ttu-id="71536-3211">Lade till kompletterare för SkuName och Typem som är tillgängliga i New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="71536-3211">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="71536-3212">Tog bort parameteruppsättningen GetSkusWithAccountParamSetName från Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="71536-3212">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="71536-3213">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="71536-3213">Az.ContainerInstance</span></span>
- <span data-ttu-id="71536-3214">Stöd för ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="71536-3214">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="71536-3215">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="71536-3215">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="71536-3216">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="71536-3216">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="71536-3217">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="71536-3217">Az.DataLakeStore</span></span>
- <span data-ttu-id="71536-3218">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="71536-3218">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="71536-3219">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="71536-3219">Az.Monitor</span></span>
- <span data-ttu-id="71536-3220">Döpte om Az.Insights till Az.Monitor och andra mindre icke-bakåtkompatibla ändringar. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="71536-3220">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="71536-3221">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="71536-3221">Az.KeyVault</span></span>
- <span data-ttu-id="71536-3222">Tog bort den inaktuella egenskapen PurgeDisabled från utdatatyper</span><span class="sxs-lookup"><span data-stu-id="71536-3222">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="71536-3223">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="71536-3223">Az.MachineLearning</span></span>
- <span data-ttu-id="71536-3224">Inkluderade cmdletarna från modulen Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="71536-3224">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="71536-3225">Az.Media</span><span class="sxs-lookup"><span data-stu-id="71536-3225">Az.Media</span></span>
- <span data-ttu-id="71536-3226">Tog bort inaktuella -Tags-alias från New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="71536-3226">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="71536-3227">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71536-3227">Az.Network</span></span>
<span data-ttu-id="71536-3228">Stöd har lagts till för konfiguration av RewriteRuleSets i Application Gateway</span><span class="sxs-lookup"><span data-stu-id="71536-3228">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="71536-3229">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="71536-3229">New cmdlets added:</span></span>
        - <span data-ttu-id="71536-3230">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="71536-3230">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="71536-3231">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="71536-3231">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="71536-3232">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="71536-3232">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="71536-3233">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="71536-3233">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="71536-3234">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="71536-3234">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="71536-3235">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="71536-3235">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="71536-3236">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="71536-3236">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="71536-3237">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="71536-3237">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="71536-3238">Cmdletar har uppdaterats med den valfria parametern -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="71536-3238">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="71536-3239">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="71536-3239">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="71536-3240">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="71536-3240">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="71536-3241">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="71536-3241">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="71536-3242">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="71536-3242">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="71536-3243">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="71536-3243">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="71536-3244">New-AzureRmApplicationGatewayUrlPathMapConfig har lagt till KeyVault-stöd för Application Gateway med Identity.</span><span class="sxs-lookup"><span data-stu-id="71536-3244">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="71536-3245">Cmdletar har uppdaterats med den valfria parametern -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="71536-3245">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="71536-3246">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="71536-3246">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="71536-3247">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="71536-3247">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="71536-3248">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="71536-3248">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="71536-3249">Cmdleten New-AzApplicationGateway har uppdaterats med den valfria parametern -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="71536-3249">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="71536-3250">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="71536-3250">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="71536-3251">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="71536-3251">Az.OperationalInsights</span></span>
- <span data-ttu-id="71536-3252">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="71536-3252">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="71536-3253">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="71536-3253">Az.Profile</span></span>
- <span data-ttu-id="71536-3254">Modulnamnet har ändrats till Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="71536-3254">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="71536-3255">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="71536-3255">Az.RecoveryServices</span></span>
- <span data-ttu-id="71536-3256">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="71536-3256">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="71536-3257">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71536-3257">Az.Resources</span></span>
- <span data-ttu-id="71536-3258">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="71536-3258">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="71536-3259">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="71536-3259">Az.ServiceFabric</span></span>
- <span data-ttu-id="71536-3260">Stöd för specificering av certifikat efter eget namn och tumavtryck</span><span class="sxs-lookup"><span data-stu-id="71536-3260">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="71536-3261">Information om fler icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="71536-3261">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="71536-3262">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="71536-3262">Az.SIgnalR</span></span>
- <span data-ttu-id="71536-3263">Allmän tillgänglighet för PowerShell-cmdletar för SIgnalR</span><span class="sxs-lookup"><span data-stu-id="71536-3263">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="71536-3264">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71536-3264">Az.Sql</span></span>
- <span data-ttu-id="71536-3265">Lade till de nya identifieringstyperna Data_Exfiltration och Unsafe_Action i Threat Detection-cmdletar</span><span class="sxs-lookup"><span data-stu-id="71536-3265">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="71536-3266">Uppdaterade dokumentationsexempel för Sql Auditing-cmdletar</span><span class="sxs-lookup"><span data-stu-id="71536-3266">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="71536-3267">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="71536-3267">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="71536-3268">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="71536-3268">Az.Storage</span></span>
- <span data-ttu-id="71536-3269">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="71536-3269">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="71536-3270">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="71536-3270">Az.Websites</span></span>
- <span data-ttu-id="71536-3271">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="71536-3271">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="71536-3272">0.7.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="71536-3272">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="71536-3273">Allmänt</span><span class="sxs-lookup"><span data-stu-id="71536-3273">General</span></span>

* <span data-ttu-id="71536-3274">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="71536-3274">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="71536-3275">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71536-3275">Az.Compute</span></span>

* <span data-ttu-id="71536-3276">Lade till stöd för UltraSSD och Galleriavbildningar i de enkla parameteruppsättningarna för `New-AzVm(ss)`-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="71536-3276">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="71536-3277">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="71536-3277">Az.DataLakeStore</span></span>

* <span data-ttu-id="71536-3278">Åtgärdade avslutande snedstreck i domänen för adls-konto</span><span class="sxs-lookup"><span data-stu-id="71536-3278">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="71536-3279">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="71536-3279">Az.FrontDoor</span></span>

* <span data-ttu-id="71536-3280">Brutna länkar korrigerades</span><span class="sxs-lookup"><span data-stu-id="71536-3280">Fixed some broken links</span></span>
    - <span data-ttu-id="71536-3281">I artiklarna New-AzureRmFrontDoor och Set-AzureRmFrontDoor artiklar korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="71536-3281">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="71536-3282">I artikeln New-AzureRmFrontDoorManagedRuleObject korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="71536-3282">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="71536-3283">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="71536-3283">Az.RecoveryServices</span></span>

* <span data-ttu-id="71536-3284">Lade till valideringar på klientsidan för Azure-filresurs med återställningsåtgärder.</span><span class="sxs-lookup"><span data-stu-id="71536-3284">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="71536-3285">Gjorde storageAccountName och storageAccountResourceGroupName valfritt för afs-återställning.</span><span class="sxs-lookup"><span data-stu-id="71536-3285">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="71536-3286">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71536-3286">Az.Resources</span></span>

* <span data-ttu-id="71536-3287">Korrigering för https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="71536-3287">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="71536-3288">Uppdaterade Get-AzureRmRoleAssignment så att prenumerationsomfattningen används om den anges vid begäran om klassiska administratörer.</span><span class="sxs-lookup"><span data-stu-id="71536-3288">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="71536-3289">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71536-3289">Az.Sql</span></span>

* <span data-ttu-id="71536-3290">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="71536-3290">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="71536-3291">Korrigerade ett problem med Get-AzureRmSqlDatabaseVulnerabilityAssessment med DotNet-kärna</span><span class="sxs-lookup"><span data-stu-id="71536-3291">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="71536-3292">Ändrade dokumentationen för hjälpmeddelanden som rör SQL Auditing-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="71536-3292">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="71536-3293">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="71536-3293">Az.Storage</span></span>

* <span data-ttu-id="71536-3294">Lade till -EnableHierarchicalNamespace i New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="71536-3294">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="71536-3295">Åtgärdade problemet med att cmdleten Copy File inte kunde återanvända källkontexten på målet om inte -DestContext angetts</span><span class="sxs-lookup"><span data-stu-id="71536-3295">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="71536-3296">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="71536-3296">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="71536-3297">Stöd för statisk webbplatskonfiguration</span><span class="sxs-lookup"><span data-stu-id="71536-3297">Support Static Website configuration</span></span>
    - <span data-ttu-id="71536-3298">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="71536-3298">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="71536-3299">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="71536-3299">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="71536-3300">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="71536-3300">Az.Websites</span></span>

* <span data-ttu-id="71536-3301">Set-AzureRmWebApp och Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="71536-3301">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="71536-3302">Ny parameter (-AzureStoragePath) har lagts till för att ange att Azure Storage-sökvägar ska monteras i containerappar i Windows och Linux.</span><span class="sxs-lookup"><span data-stu-id="71536-3302">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="71536-3303">Använder utdata från den nya cmdleten New-AzureRmWebAppAzureStoragePath som en parameter för att ange sökvägar för Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="71536-3303">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="71536-3304">0.6.1 – november 2018</span><span class="sxs-lookup"><span data-stu-id="71536-3304">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="71536-3305">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="71536-3305">Az.ApiManagement</span></span>
* <span data-ttu-id="71536-3306">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="71536-3306">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="71536-3307">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="71536-3307">Az.Automation</span></span>
* <span data-ttu-id="71536-3308">Swagger baserade Azure Automation-cmdletar</span><span class="sxs-lookup"><span data-stu-id="71536-3308">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="71536-3309">Cmdletar för Uppdateringshantering har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-3309">Added Update Management cmdlets</span></span>
* <span data-ttu-id="71536-3310">Cmdletar för källkontroll har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-3310">Added Source Control cmdlets</span></span>
* <span data-ttu-id="71536-3311">Remove-AzureRmAutomationHybridWorkerGroup-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-3311">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="71536-3312">Kommandot för DSC-registreringsnod har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="71536-3312">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="71536-3313">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71536-3313">Az.Compute</span></span>
* <span data-ttu-id="71536-3314">Problem med SystemAssigned-identitet har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="71536-3314">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="71536-3315">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="71536-3315">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="71536-3316">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="71536-3316">Az.ContainerInstance</span></span>
* <span data-ttu-id="71536-3317">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="71536-3317">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="71536-3318">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="71536-3318">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="71536-3319">uppdatera exempelbeskrivningen för marketplace-cmdletar</span><span class="sxs-lookup"><span data-stu-id="71536-3319">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="71536-3320">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71536-3320">Az.Network</span></span>
* <span data-ttu-id="71536-3321">Cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomErreller Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-3321">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="71536-3322">ICMP tillbaka till stöd för Azure Firewall-nätverksprotokoll har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-3322">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="71536-3323">Uppdatera cmdlet Test-AzureRmNetworkWatcherConnectivity, lägga till verifiering av mål-id, adress och port.</span><span class="sxs-lookup"><span data-stu-id="71536-3323">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="71536-3324">Åtgärda problem med minnesanvändning i VirtualNetwork-karta</span><span class="sxs-lookup"><span data-stu-id="71536-3324">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="71536-3325">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="71536-3325">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="71536-3326">Åtgärda för att ändra principen för en skyddad fildelning.</span><span class="sxs-lookup"><span data-stu-id="71536-3326">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="71536-3327">Tidszonsprincipen har konverterats till versaler.</span><span class="sxs-lookup"><span data-stu-id="71536-3327">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="71536-3328">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="71536-3328">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="71536-3329">Exempel i New-AzureRmRecoveryServicesAsrProtectableItem har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="71536-3329">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="71536-3330">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="71536-3330">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="71536-3331">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="71536-3331">Az.Relay</span></span>
* <span data-ttu-id="71536-3332">Valfri parameter -KeyValue till New-AzureRmRelayKey cmdlet har lagts till, vilket gör det möjligt för användare att tillhandahålla KeyValue.</span><span class="sxs-lookup"><span data-stu-id="71536-3332">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="71536-3333">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71536-3333">Az.Resources</span></span>
* <span data-ttu-id="71536-3334">Uppdatera hjälpdokumentation för resursidentitet kopplad till parametrar i `New-AzureRmPolicyAssignment` och `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="71536-3334">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="71536-3335">Lägg till ett exempel för New-AzureRmPolicyDefinition som använder -Metadata</span><span class="sxs-lookup"><span data-stu-id="71536-3335">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="71536-3336">Korrigera så att skiftläge behålls i taggnycklar i NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="71536-3336">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="71536-3337">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="71536-3337">Az.ServiceFabric</span></span>
* <span data-ttu-id="71536-3338">Lägg till utfasningsmeddelanden för kommande icke-kompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="71536-3338">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="71536-3339">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71536-3339">Az.Sql</span></span>
* <span data-ttu-id="71536-3340">Nya cmdletar för CRUD-åtgärder på Azure Sql Database-hanterad instans och Azure Sql-hanterad databas</span><span class="sxs-lookup"><span data-stu-id="71536-3340">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="71536-3341">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="71536-3341">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="71536-3342">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="71536-3342">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="71536-3343">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="71536-3343">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="71536-3344">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="71536-3344">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="71536-3345">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="71536-3345">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="71536-3346">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="71536-3346">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="71536-3347">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="71536-3347">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="71536-3348">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="71536-3348">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="71536-3349">Hantering av utökad granskningsprincip på en server eller en databas har aktiverats.</span><span class="sxs-lookup"><span data-stu-id="71536-3349">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="71536-3350">Ny parameter (PredicateExpression) har lagts till för att aktivera filtrering av granskningsloggar.</span><span class="sxs-lookup"><span data-stu-id="71536-3350">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="71536-3351">Cmdletar har ändrats så att de använder SQL-klienter i stället för äldre klienter.</span><span class="sxs-lookup"><span data-stu-id="71536-3351">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="71536-3352">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="71536-3352">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="71536-3353">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="71536-3353">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="71536-3354">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="71536-3354">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="71536-3355">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="71536-3355">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="71536-3356">Problem med att använda Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings med lagringskontots namnparameter har korrigerats</span><span class="sxs-lookup"><span data-stu-id="71536-3356">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="71536-3357">0.5.0 – november 2018</span><span class="sxs-lookup"><span data-stu-id="71536-3357">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="71536-3358">Allmänt</span><span class="sxs-lookup"><span data-stu-id="71536-3358">General</span></span>
* <span data-ttu-id="71536-3359">Lade till resurskompletterare till många kärn-cmdletar – dessa gör att du kan stega genom befintliga resursnamn med TABB vid interaktiva anrop till cmdletar</span><span class="sxs-lookup"><span data-stu-id="71536-3359">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="71536-3360">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="71536-3360">Az.Profile</span></span>
* <span data-ttu-id="71536-3361">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="71536-3361">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="71536-3362">Bytte namn på parametern TenantId i cmdleten Connect-AzAccount till Tenant och lade till ett alias för TenantId</span><span class="sxs-lookup"><span data-stu-id="71536-3362">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="71536-3363">Uppdaterade TenantId-beskrivningen för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="71536-3363">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="71536-3364">Åtgärda felmeddelande för misslyckad inloggning när du tillhandahåller klientdomän</span><span class="sxs-lookup"><span data-stu-id="71536-3364">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="71536-3365">Åtgärda problem med att kontextnamn hamnar i konflikt för konton utan prenumerationer i klientorganisationen</span><span class="sxs-lookup"><span data-stu-id="71536-3365">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="71536-3366">Åtgärda problem med DataLake-slutpunkter vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="71536-3366">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="71536-3367">Åtgärdade problem med att Disconnect-AzAccount kastades om den inte anslöts</span><span class="sxs-lookup"><span data-stu-id="71536-3367">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="71536-3368">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="71536-3368">Az.CognitiveServices</span></span>
* <span data-ttu-id="71536-3369">Lade till åtgärden Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="71536-3369">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71536-3370">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71536-3370">Az.Compute</span></span>
* <span data-ttu-id="71536-3371">Lade till cmdletarna Add-AzVmssVMDataDisk och Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="71536-3371">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="71536-3372">Get-AzVMImage visar AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="71536-3372">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="71536-3373">Åtgärdade att värdena för alternativen SetAzVMChefExtension -BootstrapOptions och -JsonAttribute inte angavs i json-format.</span><span class="sxs-lookup"><span data-stu-id="71536-3373">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="71536-3374">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="71536-3374">Az.DataLakeStore</span></span>
* <span data-ttu-id="71536-3375">Uppdatera DataLake-paketet till 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="71536-3375">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="71536-3376">Lägg till standardsamtidighet för flertrådade åtgärder.</span><span class="sxs-lookup"><span data-stu-id="71536-3376">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="71536-3377">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="71536-3377">Az.Insights</span></span>
* <span data-ttu-id="71536-3378">Åtgärdade problem #7267 (autoskalningsområde)</span><span class="sxs-lookup"><span data-stu-id="71536-3378">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="71536-3379">Problem med att uppräknade parametrar inte ställdes in ordentligt när du skapade en ny autoskalningsregel (de ställdes alltid in med standardvärdet).</span><span class="sxs-lookup"><span data-stu-id="71536-3379">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="71536-3380">Åtgärdade problem #7513 [Insights] Set-AzDiagnosticSetting kräver uttrycklig specifikation av kategorier när inställningar skapas</span><span class="sxs-lookup"><span data-stu-id="71536-3380">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="71536-3381">Nu kräver inte cmdleten uttrycklig anvisning av kategorierna för att aktiveras under skapande, d.v.s. den fungerar enligt beskrivning</span><span class="sxs-lookup"><span data-stu-id="71536-3381">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71536-3382">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71536-3382">Az.Network</span></span>
* <span data-ttu-id="71536-3383">PeeringType ändrades till en obligatorisk parameter för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="71536-3383">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="71536-3384">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="71536-3384">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="71536-3385">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="71536-3385">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="71536-3386">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="71536-3386">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="71536-3387">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="71536-3387">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="71536-3388">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="71536-3388">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="71536-3389">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="71536-3389">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="71536-3390">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="71536-3390">Az.PolicyInsights</span></span>
* <span data-ttu-id="71536-3391">Cmdletar för principreparation har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-3391">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="71536-3392">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71536-3392">Az.Resources</span></span>
* <span data-ttu-id="71536-3393">Korrigering för https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="71536-3393">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="71536-3394">Tillåt att resurser listas med parametern -ResourceId för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="71536-3394">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="71536-3395">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="71536-3395">Az.ServiceBus</span></span>
* <span data-ttu-id="71536-3396">Skrivskyddad MigrationState-egenskap har lagts till i PSServiceBusMigrationConfigurationAttributes, som hjälper till att hålla koll på migreringstillståndet.</span><span class="sxs-lookup"><span data-stu-id="71536-3396">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="71536-3397">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="71536-3397">Az.ServiceFabric</span></span>
* <span data-ttu-id="71536-3398">Åtgärda att lägga till certifikat till Linux-Vmss.</span><span class="sxs-lookup"><span data-stu-id="71536-3398">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="71536-3399">Åtgärdade Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="71536-3399">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="71536-3400">Använd rätt tumavtryck från nya certifikat (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="71536-3400">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="71536-3401">Visa undantag korrekt (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="71536-3401">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="71536-3402">Åtgärdade Update-AzServiceFabricDurability så att klusterkonfigurationen uppdateras innan Vmss-åtgärden CreateOrUpdate påbörjas.</span><span class="sxs-lookup"><span data-stu-id="71536-3402">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="71536-3403">0.4.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="71536-3403">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="71536-3404">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="71536-3404">Az.Profile</span></span>
* <span data-ttu-id="71536-3405">Åtgärdade problemet med Get-AzSubscription i CloudShell</span><span class="sxs-lookup"><span data-stu-id="71536-3405">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="71536-3406">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="71536-3406">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71536-3407">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71536-3407">Az.Compute</span></span>
* <span data-ttu-id="71536-3408">Nya storlekar lades till i listan över godkända VM-storlekar för vilka accelererat nätverk kommer att aktiveras vid användning av den enkla parameteruppsättningen för New-AzVm</span><span class="sxs-lookup"><span data-stu-id="71536-3408">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="71536-3409">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="71536-3409">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="71536-3410">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="71536-3410">Az.DataLakeStore</span></span>
* <span data-ttu-id="71536-3411">Lägger till stöd för regler för virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="71536-3411">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="71536-3412">Get-AzDataLakeStoreVirtualNetworkRule: Hämtar eller listar regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="71536-3412">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="71536-3413">Add-AzDataLakeStoreVirtualNetworkRule: Lägger till en regel för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="71536-3413">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="71536-3414">Set-AzDataLakeStoreVirtualNetworkRule: Ändrar den angivna regeln för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="71536-3414">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="71536-3415">Remove-AzDataLakeStoreVirtualNetworkRule: Tar bort en regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="71536-3415">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71536-3416">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71536-3416">Az.Network</span></span>
* <span data-ttu-id="71536-3417">Skicka protokollvärdet till serverdelen för att uppdatera cmdleten Test-AzNetworkWatcherConnectivity.</span><span class="sxs-lookup"><span data-stu-id="71536-3417">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="71536-3418">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="71536-3418">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="71536-3419">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71536-3419">Az.Resources</span></span>
* <span data-ttu-id="71536-3420">Åtgärdade problem där Get-AzRoleDefinition genererar ett oläsligt undantag (när standardprofilen inte innehåller någon prenumeration och ingen omfattning har angetts) genom att lägga till ett beskrivande undantag i scenariot.</span><span class="sxs-lookup"><span data-stu-id="71536-3420">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="71536-3421">Ställ in ”RoleDefinitionNameParameterSet” som standardparameteruppsättning.</span><span class="sxs-lookup"><span data-stu-id="71536-3421">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="71536-3422">0.3.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="71536-3422">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="71536-3423">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="71536-3423">Azure.Storage</span></span>
* <span data-ttu-id="71536-3424">Åtgärda fel där Kopiera blob/fil inte kopierar metadata när målplatsen har ett problem med metadata</span><span class="sxs-lookup"><span data-stu-id="71536-3424">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="71536-3425">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="71536-3425">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="71536-3426">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="71536-3426">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="71536-3427">Stöd för att hämta användningsinformation om en Storage-resurs för en specifik plats och för att lägga till ett varningsmeddelande för att hämta användningsinformation om en global Storage-resurs är inaktuellt.</span><span class="sxs-lookup"><span data-stu-id="71536-3427">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="71536-3428">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="71536-3428">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="71536-3429">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="71536-3429">Az.CognitiveServices</span></span>
* <span data-ttu-id="71536-3430">Stöd för Get-AzCognitiveServicesAccountSkus utan ett befintligt konto.</span><span class="sxs-lookup"><span data-stu-id="71536-3430">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71536-3431">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71536-3431">Az.Compute</span></span>
* <span data-ttu-id="71536-3432">Åtgärdade fel där Get-AzVM -ResourceGroupName <rg> returnerar fler än 50 resultat om det behövs</span><span class="sxs-lookup"><span data-stu-id="71536-3432">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="71536-3433">Lade till ett exempel för SimpleParameterSet i hjälpen för cmdleten New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="71536-3433">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="71536-3434">Ett stavfel i förloppsmeddelandet för Azure Disk Encryption har korrigerats</span><span class="sxs-lookup"><span data-stu-id="71536-3434">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="71536-3435">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="71536-3435">Az.DataFactoryV2</span></span>
* <span data-ttu-id="71536-3436">ADF .Net SDK-versionen har uppdaterats till 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="71536-3436">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71536-3437">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71536-3437">Az.Network</span></span>
* <span data-ttu-id="71536-3438">Funktionalitet för NetworkProfile har lagts till.</span><span class="sxs-lookup"><span data-stu-id="71536-3438">Added NetworkProfile functionality.</span></span> <span data-ttu-id="71536-3439">nya cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-3439">new cmdlets added</span></span>
    - <span data-ttu-id="71536-3440">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="71536-3440">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="71536-3441">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="71536-3441">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="71536-3442">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="71536-3442">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="71536-3443">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="71536-3443">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="71536-3444">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="71536-3444">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="71536-3445">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="71536-3445">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="71536-3446">Länk för tjänstassociering på modell för undernät har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-3446">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="71536-3447">Cmdletarna New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap och Remove-AzVirtualNetworkTap har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-3447">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="71536-3448">Cmdletarna Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig och Remove-AzNEtworkInterfaceTapConfig har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-3448">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="71536-3449">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="71536-3449">Az.RedisCache</span></span>
* <span data-ttu-id="71536-3450">Tillåt att alla strängar används som storleksparametrar framöver.</span><span class="sxs-lookup"><span data-stu-id="71536-3450">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="71536-3451">Lägg till P5 i popup-fönstret PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="71536-3451">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="71536-3452">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71536-3452">Az.Resources</span></span>
* <span data-ttu-id="71536-3453">Parametern -Mode som saknades i Set-AzPolicyDefinition har lagts till</span><span class="sxs-lookup"><span data-stu-id="71536-3453">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="71536-3454">Åtgärdade buggen för cmdleten Get-AzProviderOperation för åtgärder med ursprung som innehåller användare</span><span class="sxs-lookup"><span data-stu-id="71536-3454">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="71536-3455">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71536-3455">Az.Sql</span></span>
* <span data-ttu-id="71536-3456">Ett problem där vissa cmdletar för säkerhetskopiering inte kunde identifiera den aktuella azure-prenumerationen har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="71536-3456">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="71536-3457">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="71536-3457">Az.Websites</span></span>
* <span data-ttu-id="71536-3458">Ny cmdlet: Get-AzWebAppContainerContinuousDeploymentUrl – Hämtar webhook-URL:en för kontinuerlig distribution av container</span><span class="sxs-lookup"><span data-stu-id="71536-3458">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="71536-3459">Nya cmdletar: New-AzWebAppContainerPSSession och Enter-WebAppContainerPSSession – Startar en PowerShell-fjärrsession i en containerapp för windows</span><span class="sxs-lookup"><span data-stu-id="71536-3459">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="71536-3460">0.2.0 – september 2018</span><span class="sxs-lookup"><span data-stu-id="71536-3460">0.2.0 - September 2018</span></span>
 <span data-ttu-id="71536-3461">Första versionen</span><span class="sxs-lookup"><span data-stu-id="71536-3461">Initial Release</span></span>