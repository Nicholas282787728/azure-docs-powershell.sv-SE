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
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="08996-103">Viktig information om Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="08996-103">Azure PowerShell release notes</span></span>

## <a name="480---october-2020"></a><span data-ttu-id="08996-104">4.8.0 – oktober 2020</span><span class="sxs-lookup"><span data-stu-id="08996-104">4.8.0 - October 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="08996-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="08996-105">Az.Accounts</span></span>
* <span data-ttu-id="08996-106">Åtgärdat DateTime-parsningsfel i vanliga bibliotek [#13045]</span><span class="sxs-lookup"><span data-stu-id="08996-106">Fixed DateTime parse issue in common libraries [#13045]</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="08996-107">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="08996-107">Az.CognitiveServices</span></span>
* <span data-ttu-id="08996-108">Cmdleten New-AzCognitiveServicesAccountApiProperty har lagts till.</span><span class="sxs-lookup"><span data-stu-id="08996-108">Added 'New-AzCognitiveServicesAccountApiProperty' cmdlet.</span></span>
* <span data-ttu-id="08996-109">Stöd för parametern ApiProperty för New-AzCognitiveServicesAccount och Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="08996-109">Supported 'ApiProperty' parameter for 'New-AzCognitiveServicesAccount' and 'Set-AzCognitiveServicesAccount'</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08996-110">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08996-110">Az.Compute</span></span>
* <span data-ttu-id="08996-111">Åtgärdat problem i Update-ASRRecoveryPlan genom att fylla i FailoverTypes</span><span class="sxs-lookup"><span data-stu-id="08996-111">Fixed issue in 'Update-ASRRecoveryPlan' by populating FailoverTypes</span></span>
* <span data-ttu-id="08996-112">De valfria parametrarna -Top och -OrderBy har lagts till i cmdleten Get-AzVmImage.</span><span class="sxs-lookup"><span data-stu-id="08996-112">Added the '-Top' and '-OrderBy' optional parameters to the 'Get-AzVmImage' cmdlet.</span></span> 

#### <a name="azdatabricks"></a><span data-ttu-id="08996-113">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="08996-113">Az.Databricks</span></span>
* <span data-ttu-id="08996-114">Allmän tillgänglighet för modulen Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="08996-114">General availability of 'Az.Databricks' module</span></span>
* <span data-ttu-id="08996-115">Stöd har lagts till för virtuell nätverkspeering</span><span class="sxs-lookup"><span data-stu-id="08996-115">Added support for virtual network peering</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="08996-116">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="08996-116">Az.DataFactory</span></span>
* <span data-ttu-id="08996-117">Skrivfel har åtgärdats i utdatameddelanden</span><span class="sxs-lookup"><span data-stu-id="08996-117">Fixed typo in output messages</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="08996-118">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="08996-118">Az.EventHub</span></span>
* <span data-ttu-id="08996-119">Den valfria switchparametern TrustedServiceAccessEnabled har lagts till i cmdleten Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="08996-119">Added optional switch parameter 'TrustedServiceAccessEnabled' to 'Set-AzEventHubNetworkRuleSet' cmdlet</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="08996-120">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="08996-120">Az.HDInsight</span></span>
* <span data-ttu-id="08996-121">Ett varningsmeddelande om att parametrarna PublicNetworkAccessType och OutboundPublicNetworkAccessType planeras att göras inaktuella har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-121">Added warning message for planning to deprecate the parameters 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType'</span></span>
* <span data-ttu-id="08996-122">Ett varningsmeddelande om att parametern DefaultStorageAccountName planeras att ersättas med StorageAccountResourceId har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-122">Added warning message for planning to replace the parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
* <span data-ttu-id="08996-123">Ett varningsmeddelande om att parametern DefaultStorageAccountKey planeras att ersättas med StorageAccountKey har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-123">Added warning message for planning to replace the parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
* <span data-ttu-id="08996-124">Ett varningsmeddelande om att parametern DefaultStorageAccountType planeras att ersättas med StorageAccountType har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-124">Added warning message for planning to replace the parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
* <span data-ttu-id="08996-125">Ett varningsmeddelande om att parametern DefaultStorageContainer planeras att ersättas med StorageContainer har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-125">Added warning message for planning to replace the parameter 'DefaultStorageContainer' with 'StorageContainer'</span></span>
* <span data-ttu-id="08996-126">Ett varningsmeddelande om att parametern DefaultStorageRootPath planeras att ersättas med StorageRootPath har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-126">Added warning message for planning to replace the parameter 'DefaultStorageRootPath' with 'StorageRootPath'</span></span>

#### <a name="aziothub"></a><span data-ttu-id="08996-127">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="08996-127">Az.IotHub</span></span>
* <span data-ttu-id="08996-128">SDK för enheter har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="08996-128">Updated devices sdk.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="08996-129">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="08996-129">Az.KeyVault</span></span>
* <span data-ttu-id="08996-130">Detaljerat datum för borttagning av egenskapen SecretValueText har tillhandahållits</span><span class="sxs-lookup"><span data-stu-id="08996-130">Provided the detailed date of removing property SecretValueText</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="08996-131">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="08996-131">Az.ManagedServices</span></span>
* <span data-ttu-id="08996-132">Varningar om icke-bakåtkompatibla ändringar för cmdletar för tilldelning och definition av hanterade tjänster har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="08996-132">Updated breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="08996-133">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="08996-133">Az.Monitor</span></span>
* <span data-ttu-id="08996-134">Felet som gjorde att ett varningsmeddelande inte kunde ignoreras har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="08996-134">Fixed the bug that warning message cannot be suppressed.</span></span> <span data-ttu-id="08996-135">[#12889]</span><span class="sxs-lookup"><span data-stu-id="08996-135">[#12889]</span></span>
* <span data-ttu-id="08996-136">Stöd för parametern SkipMetricValidation i aviseringsregelvillkor.</span><span class="sxs-lookup"><span data-stu-id="08996-136">Supported 'SkipMetricValidation' parameter in alert rule criteria.</span></span> <span data-ttu-id="08996-137">Tillåter att du skapar en aviseringsregel för ett anpassat mått som inte har genererats än, genom att göra så att måttverifieringen hoppas över.</span><span class="sxs-lookup"><span data-stu-id="08996-137">Allows creating an alert rule on a custom metric that isn't yet emitted, by causing the metric validation to be skipped.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="08996-138">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08996-138">Az.Network</span></span>
* <span data-ttu-id="08996-139">Office365-princip har lagts till för VPNSite-resurs</span><span class="sxs-lookup"><span data-stu-id="08996-139">Added Office365 Policy to VPNSite Resource</span></span>
    - <span data-ttu-id="08996-140">New-AzO365PolicyProperty</span><span class="sxs-lookup"><span data-stu-id="08996-140">'New-AzO365PolicyProperty'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="08996-141">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="08996-141">Az.RecoveryServices</span></span>
* <span data-ttu-id="08996-142">Verifiering av containernamn har lagts till för arbetsbelastningssäkerhetskopior.</span><span class="sxs-lookup"><span data-stu-id="08996-142">Added container name validation for workload backup.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="08996-143">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="08996-143">Az.RedisCache</span></span>
* <span data-ttu-id="08996-144">En korrigering har gjorts så att cmdletarna New-AzRedisCache och Set-AzRedisCache inte misslyckas på grund av behörighetsproblem som rör registrering av Microsoft.Cache RP</span><span class="sxs-lookup"><span data-stu-id="08996-144">Made 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets not fail because of permission issue related to registering Microsoft.Cache RP</span></span>

#### <a name="azsql"></a><span data-ttu-id="08996-145">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08996-145">Az.Sql</span></span>
* <span data-ttu-id="08996-146">BackupStorageRedundancy har lagts till i:</span><span class="sxs-lookup"><span data-stu-id="08996-146">Added BackupStorageRedundancy to the following:</span></span> 
    - <span data-ttu-id="08996-147">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="08996-147">'Restore-AzureRmSqlDatabase'</span></span>
    - <span data-ttu-id="08996-148">New-AzSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="08996-148">'New-AzSqlDatabaseCopy'</span></span>
    - <span data-ttu-id="08996-149">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="08996-149">'New-AzSqlDatabaseSecondary'</span></span>
* <span data-ttu-id="08996-150">Skiftlägeskänslighet har tagits bort för parametern BackupStorageRedundancy för alla SQL DB-referenser</span><span class="sxs-lookup"><span data-stu-id="08996-150">Removed case sensitivity for BackupStorageRedundancy parameter for all SQL DB references</span></span> 
* <span data-ttu-id="08996-151">Namnen på BackupStorageRedundancy-varningsmeddelanden har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="08996-151">Updated BackupStorageRedundancy warning message names</span></span>

#### <a name="azstorage"></a><span data-ttu-id="08996-152">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="08996-152">Az.Storage</span></span>
* <span data-ttu-id="08996-153">Stöd för att aktivera/inaktivera/hämta egenskaper för mjuk borttagning av resurser för filtjänst för ett lagringskonto</span><span class="sxs-lookup"><span data-stu-id="08996-153">Supported enable/disable/get share soft delete properties on file Service of a Storage account</span></span>
    - <span data-ttu-id="08996-154">Update-AzStorageFileServiceProperty</span><span class="sxs-lookup"><span data-stu-id="08996-154">'Update-AzStorageFileServiceProperty'</span></span>
    - <span data-ttu-id="08996-155">Get-AzStorageFileServiceProperty</span><span class="sxs-lookup"><span data-stu-id="08996-155">'Get-AzStorageFileServiceProperty'</span></span>
* <span data-ttu-id="08996-156">Stöd för att visa filresurser inkluderar borttagna filresurser för ett lagringskonto och hämta förbrukning av enskild filresurs</span><span class="sxs-lookup"><span data-stu-id="08996-156">Supported list file shares include the deleted ones of a Storage account, and Get single file share usage</span></span>
    - <span data-ttu-id="08996-157">”Get-AzRmStorageShare”</span><span class="sxs-lookup"><span data-stu-id="08996-157">'Get-AzRmStorageShare'</span></span>
* <span data-ttu-id="08996-158">Stöd för återställning av en borttagen filresurs</span><span class="sxs-lookup"><span data-stu-id="08996-158">Supported restore a deleted file share</span></span>
    - <span data-ttu-id="08996-159">Restore-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="08996-159">'Restore-AzRmStorageShare'</span></span>
* <span data-ttu-id="08996-160">Cmdletarna för ändring av egenskaper för Blob Service har ändrats. De ursprungliga egenskaperna hämtas inte från servern utan anger bara de ändrade egenskaperna till servern.</span><span class="sxs-lookup"><span data-stu-id="08996-160">Changed the cmdlets for modify blob service properties, won't get the original properties from server, but only set the modified properties to server.</span></span>
    - <span data-ttu-id="08996-161">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="08996-161">'Enable-AzStorageBlobDeleteRetentionPolicy'</span></span>
    - <span data-ttu-id="08996-162">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="08996-162">'Disable-AzStorageBlobDeleteRetentionPolicy'</span></span>  
    - <span data-ttu-id="08996-163">"Enable-AzStorageBlobRestorePolicy"</span><span class="sxs-lookup"><span data-stu-id="08996-163">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="08996-164">"Disable-AzStorageBlobRestorePolicy"</span><span class="sxs-lookup"><span data-stu-id="08996-164">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="08996-165">”Update-AzStorageBlobServiceProperty”</span><span class="sxs-lookup"><span data-stu-id="08996-165">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="08996-166">Åtgärdat hjälpproblem för New-AzStorageAccount-parametern -Kind default value [#12189]</span><span class="sxs-lookup"><span data-stu-id="08996-166">Fixed help issue for New-AzStorageAccount parameter -Kind default value [#12189]</span></span>
* <span data-ttu-id="08996-167">Åtgärdat problem genom att lägga till exempel som visar hur ContentType anges på korrekt sätt i en blobuppladdning [#12989]</span><span class="sxs-lookup"><span data-stu-id="08996-167">Fixed issue by add example to show how to set correct ContentType in blob upload [#12989]</span></span>

## <a name="470---september-2020"></a><span data-ttu-id="08996-168">4.7.0 – September 2020</span><span class="sxs-lookup"><span data-stu-id="08996-168">4.7.0 - September 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="08996-169">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="08996-169">Az.Accounts</span></span>
* <span data-ttu-id="08996-170">Formaterat kommande meddelanden om icke-bakåtkompatibel ändring</span><span class="sxs-lookup"><span data-stu-id="08996-170">Formatted the upcoming breaking change messages</span></span>
* <span data-ttu-id="08996-171">Uppdaterat Azure.Core till 1.4.1</span><span class="sxs-lookup"><span data-stu-id="08996-171">Updated Azure.Core to 1.4.1</span></span>

#### <a name="azaks"></a><span data-ttu-id="08996-172">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="08996-172">Az.Aks</span></span>
* <span data-ttu-id="08996-173">Valideringslogiken för parametern "New-AzAksCluster", "Set-AzAksCluster" och "New-AzAksNodePool" har lagts till på klientsidan.</span><span class="sxs-lookup"><span data-stu-id="08996-173">Added client side parameter validation logic for 'New-AzAksCluster', 'Set-AzAksCluster' and 'New-AzAksNodePool'.</span></span> <span data-ttu-id="08996-174">[#12372]</span><span class="sxs-lookup"><span data-stu-id="08996-174">[#12372]</span></span>
* <span data-ttu-id="08996-175">Stöd har lagts till för tillägg i "New-AzAksCluster".</span><span class="sxs-lookup"><span data-stu-id="08996-175">Added support for add-ons in 'New-AzAksCluster'.</span></span> <span data-ttu-id="08996-176">[#11239]</span><span class="sxs-lookup"><span data-stu-id="08996-176">[#11239]</span></span>
* <span data-ttu-id="08996-177">Cmdlet:arna "Enable-AzAksAddOn" och "Disable-AzAksAddOn" har lagts till för tillägg.</span><span class="sxs-lookup"><span data-stu-id="08996-177">Added cmdlets 'Enable-AzAksAddOn' and 'Disable-AzAksAddOn' for add-ons.</span></span> <span data-ttu-id="08996-178">[#11239]</span><span class="sxs-lookup"><span data-stu-id="08996-178">[#11239]</span></span>
* <span data-ttu-id="08996-179">Parametern "GenerateSshKey" har lagts till för "New-AzAksCluster".</span><span class="sxs-lookup"><span data-stu-id="08996-179">Added parameter 'GenerateSshKey' for 'New-AzAksCluster'.</span></span> <span data-ttu-id="08996-180">[#12371]</span><span class="sxs-lookup"><span data-stu-id="08996-180">[#12371]</span></span>
* <span data-ttu-id="08996-181">API-versionen har uppdaterats till 2020-06-01.</span><span class="sxs-lookup"><span data-stu-id="08996-181">Updated api version to 2020-06-01.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="08996-182">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="08996-182">Az.CognitiveServices</span></span>
* <span data-ttu-id="08996-183">Visade ytterligare juridiska villkor för vissa API:er.</span><span class="sxs-lookup"><span data-stu-id="08996-183">Showed additional legal terms for certain APIs.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08996-184">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08996-184">Az.Compute</span></span>
* <span data-ttu-id="08996-185">Den valfria parametern "EncryptionType" har lagts till i "New-AzVmDiskEncryptionSetConfig"</span><span class="sxs-lookup"><span data-stu-id="08996-185">Added the '-EncryptionType' optional parameter to 'New-AzVmDiskEncryptionSetConfig'</span></span>
* <span data-ttu-id="08996-186">Nya cmdlet:ar för ny resurs typ: DiskAccess "Get-AzDiskAccess", "New-AzDiskAccess", "Get-AzDiskAccess"</span><span class="sxs-lookup"><span data-stu-id="08996-186">New cmdlets for new resource type: DiskAccess 'Get-AzDiskAccess', 'New-AzDiskAccess', 'Get-AzDiskAccess'</span></span>
* <span data-ttu-id="08996-187">De valfria parametrarna "-DiskAccessId" och "-NetworkAccessPolicy" har lagts till i "New-AzSnapshotConfig"</span><span class="sxs-lookup"><span data-stu-id="08996-187">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzSnapshotConfig'</span></span>
* <span data-ttu-id="08996-188">De valfria parametrarna "-DiskAccessId" och "-NetworkAccessPolicy" har lagts till i "New-AzDiskConfig"</span><span class="sxs-lookup"><span data-stu-id="08996-188">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzDiskConfig'</span></span>
* <span data-ttu-id="08996-189">PatchStatus-egenskapen har lagts till i VirtualMachine-instansvyn</span><span class="sxs-lookup"><span data-stu-id="08996-189">Added 'PatchStatus' property to VirtualMachine Instance View</span></span>
* <span data-ttu-id="08996-190">Egenskapen "VMHealth" har lagts till i den virtuella datorns instansvy, vilket är det returnerade objektet när "get-AzVm" anropas med "-Status"</span><span class="sxs-lookup"><span data-stu-id="08996-190">Added 'VMHealth' property to the virtual machine's instance view, which is the returned object when 'Get-AzVm' is invoked with '-Status'</span></span>
* <span data-ttu-id="08996-191">Fältet "AssignedHost" har lagts till i instansvyerna "Get-AzVM" och "Get-AzVmss".</span><span class="sxs-lookup"><span data-stu-id="08996-191">Added 'AssignedHost' field to 'Get-AzVM' and 'Get-AzVmss' instance views.</span></span> <span data-ttu-id="08996-192">I fältet visas resurs-ID för den virtuella datorinstansen</span><span class="sxs-lookup"><span data-stu-id="08996-192">The field shows the resource id of the virtual machine instance</span></span>
* <span data-ttu-id="08996-193">Den valfria parametern "-SupportAutomaticPlacement" har lagts till i "New-AzHostGroup"</span><span class="sxs-lookup"><span data-stu-id="08996-193">Added optional parameter '-SupportAutomaticPlacement' to 'New-AzHostGroup'</span></span> 
* <span data-ttu-id="08996-194">Parametern "-HostGroupId" har lagts till i "New-AzVm" och "New-AzVmss"</span><span class="sxs-lookup"><span data-stu-id="08996-194">Added the '-HostGroupId' parameter to 'New-AzVm' and 'New-AzVmss'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="08996-195">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="08996-195">Az.DataFactory</span></span>
* <span data-ttu-id="08996-196">ADF .Net SDK har uppdaterats till version 4.11.0</span><span class="sxs-lookup"><span data-stu-id="08996-196">Updated ADF .Net SDK version to 4.11.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="08996-197">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="08996-197">Az.EventHub</span></span>
* <span data-ttu-id="08996-198">Nya kluster-cmdlet:ar – "New-AzEventHubCluster", "Set-AzEventHubCluster", "Get-AzEventHubCluster", "Remove-AzEventHubCluster", "Get-AzEventHubClustersAvailableRegions" har lagts till.</span><span class="sxs-lookup"><span data-stu-id="08996-198">Added new Cluster cmdlets - 'New-AzEventHubCluster', 'Set-AzEventHubCluster', 'Get-AzEventHubCluster', 'Remove-AzEventHubCluster', 'Get-AzEventHubClustersAvailableRegions'.</span></span>
* <span data-ttu-id="08996-199">Åtgärdat för ärende #10722 : Korrigering för tilldelning av enbart lyssning till AuthorizationRule-rättigheter.</span><span class="sxs-lookup"><span data-stu-id="08996-199">Fixed for issue #10722 : Fix for assigning only 'Listen' to AuthorizationRule rights.</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="08996-200">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="08996-200">Az.Functions</span></span>
* <span data-ttu-id="08996-201">Möjligheten att skapa v2-funktioner i regioner som inte stöder det har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="08996-201">Removed the ability to create v2 Functions in regions that do not support it.</span></span>
* <span data-ttu-id="08996-202">Föråldrad PowerShell 6.2.</span><span class="sxs-lookup"><span data-stu-id="08996-202">Deprecated PowerShell 6.2.</span></span> <span data-ttu-id="08996-203">En varning har lagts till när en användare skapar en PowerShell 6.2-funktionsapp som uppmanar till att skapa en PowerShell 7.0-funktionsapp i stället.</span><span class="sxs-lookup"><span data-stu-id="08996-203">Added a warning for when a user creates a PowerShell 6.2 function app that advises them to create a PowerShell 7.0 function app instead.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="08996-204">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="08996-204">Az.HDInsight</span></span>
* <span data-ttu-id="08996-205">Stöd för att skapa kluster med automatisk skalningskonfiguration</span><span class="sxs-lookup"><span data-stu-id="08996-205">Supported creating cluster with Autoscale configuration</span></span>
    - <span data-ttu-id="08996-206">Lägg till den nya parametern "AutoscaleConfiguration" till cmdleten ”New-AzHDInsightCluster”</span><span class="sxs-lookup"><span data-stu-id="08996-206">Add new parameter 'AutoscaleConfiguration' to the cmdlet 'New-AzHDInsightCluster'</span></span>
* <span data-ttu-id="08996-207">Stöd för att använda automatisk skalningskonfiguration i kluster</span><span class="sxs-lookup"><span data-stu-id="08996-207">Supported operating cluster's Autoscale configuration</span></span>
    - <span data-ttu-id="08996-208">Lägg till ny cmdlet "Get-AzHDInsihgtClusterAutoscaleConfiguration"</span><span class="sxs-lookup"><span data-stu-id="08996-208">Add new cmdlet 'Get-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="08996-209">Lägg till ny cmdlet "New-AzHDInsihgtClusterAutoscaleConfiguration"</span><span class="sxs-lookup"><span data-stu-id="08996-209">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="08996-210">Lägg till ny cmdlet "Set-AzHDInsihgtClusterAutoscaleConfiguration"</span><span class="sxs-lookup"><span data-stu-id="08996-210">Add new cmdlet 'Set-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="08996-211">Lägg till ny cmdlet "Remove-AzHDInsihgtClusterAutoscaleConfiguration"</span><span class="sxs-lookup"><span data-stu-id="08996-211">Add new cmdlet 'Remove-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="08996-212">Lägg till ny cmdlet "New-AzHDInsihgtClusterAutoscaleScheduleCondition"</span><span class="sxs-lookup"><span data-stu-id="08996-212">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleScheduleCondition'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="08996-213">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="08996-213">Az.KeyVault</span></span>
* <span data-ttu-id="08996-214">Stöd har lagts till för RBAC-auktorisering [#10557]</span><span class="sxs-lookup"><span data-stu-id="08996-214">Added support for RBAC authorization [#10557]</span></span>
* <span data-ttu-id="08996-215">Förbättrad felhantering i "Set-AzKeyVaultAccessPolicy" [#4007]</span><span class="sxs-lookup"><span data-stu-id="08996-215">Enhanced error handling in 'Set-AzKeyVaultAccessPolicy' [#4007]</span></span>

#### <a name="azkusto"></a><span data-ttu-id="08996-216">Az.Kusto</span><span class="sxs-lookup"><span data-stu-id="08996-216">Az.Kusto</span></span>
* <span data-ttu-id="08996-217">Allmän tillgänglighet för "Az.Kusto"-modulen</span><span class="sxs-lookup"><span data-stu-id="08996-217">General availability of 'Az.Kusto' module</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="08996-218">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08996-218">Az.Network</span></span>
* <span data-ttu-id="08996-219">[Viktig ändring] Uppdaterade nedanstående cmdlets för att justera resursens virtuella router och virtuella hubb</span><span class="sxs-lookup"><span data-stu-id="08996-219">[Breaking Change] Updated below cmdlets to align resource virtual router and virtual hub</span></span>
    - <span data-ttu-id="08996-220">"New-AzVirtualRouter":</span><span class="sxs-lookup"><span data-stu-id="08996-220">'New-AzVirtualRouter':</span></span> 
        - <span data-ttu-id="08996-221">Parametern-HostedSubnet har lagts till för att stödja underordnad resurs för IP-konfiguration</span><span class="sxs-lookup"><span data-stu-id="08996-221">Added -HostedSubnet parameter to support IP configuration child resource</span></span>
        - <span data-ttu-id="08996-222">-HostedGateway och -HostedGatewayId har tagits bort</span><span class="sxs-lookup"><span data-stu-id="08996-222">deleted -HostedGateway and -HostedGatewayId</span></span>
    - <span data-ttu-id="08996-223">'Get-AzVirtualRouter':</span><span class="sxs-lookup"><span data-stu-id="08996-223">'Get-AzVirtualRouter':</span></span>
        - <span data-ttu-id="08996-224">Parameteruppsättningen har lagts till på prenumerationsnivå</span><span class="sxs-lookup"><span data-stu-id="08996-224">Added subscription level parameter set</span></span>
    - <span data-ttu-id="08996-225">"Remove-AzVirtualRouter"</span><span class="sxs-lookup"><span data-stu-id="08996-225">'Remove-AzVirtualRouter'</span></span>
    - <span data-ttu-id="08996-226">"Add-AzVirtualRouterPeer"</span><span class="sxs-lookup"><span data-stu-id="08996-226">'Add-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="08996-227">"Get-AzVirtualRouterPeer"</span><span class="sxs-lookup"><span data-stu-id="08996-227">'Get-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="08996-228">"Remove-AzVirtualRouterPeer"</span><span class="sxs-lookup"><span data-stu-id="08996-228">'Remove-AzVirtualRouterPeer'</span></span>
* <span data-ttu-id="08996-229">Ny cmdlet har lagts till för Azure Express Route-port</span><span class="sxs-lookup"><span data-stu-id="08996-229">Added new cmdlet for Azure Express Route Port</span></span>
    - <span data-ttu-id="08996-230">"New-AzExpressRoutePortLOA"</span><span class="sxs-lookup"><span data-stu-id="08996-230">'New-AzExpressRoutePortLOA'</span></span>
* <span data-ttu-id="08996-231">Egenskapen RemoteBgpCommunities har lagts till i VirtualNetwork Peering-resursen</span><span class="sxs-lookup"><span data-stu-id="08996-231">Added RemoteBgpCommunities property to the VirtualNetwork Peering Resource</span></span>
* <span data-ttu-id="08996-232">Ändrade varningsmeddelandet för ”New-AzLoadBalancerFrontendIpConfig”, ”New-AzPublicIpAddress” och ”New-AzPublicIpPrefix”.</span><span class="sxs-lookup"><span data-stu-id="08996-232">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>
* <span data-ttu-id="08996-233">Lade till VpnGatewayIpConfigurations till "Get-AzVpnGateway"-utdata</span><span class="sxs-lookup"><span data-stu-id="08996-233">Added VpnGatewayIpConfigurations to 'Get-AzVpnGateway' output</span></span>
* <span data-ttu-id="08996-234">Åtgärdade bugg för "Set-AzApplicationGatewaySslCertificate" [#9488]</span><span class="sxs-lookup"><span data-stu-id="08996-234">Fixed bug for 'Set-AzApplicationGatewaySslCertificate' [#9488]</span></span>
* <span data-ttu-id="08996-235">Parametern "AllowActiveFTP" har lagts till i "AzureFirewall"</span><span class="sxs-lookup"><span data-stu-id="08996-235">Added 'AllowActiveFTP' parameter to 'AzureFirewall'</span></span>
* <span data-ttu-id="08996-236">Nedanstående kommandon för funktionen har uppdaterats: Aktivera konfiguration/borttagning för Internetsäkerhet på VirtualWan P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="08996-236">Updated below commands for feature: Enable internet security set/remove on VirtualWan P2SVpnGateway.</span></span>
- <span data-ttu-id="08996-237">"New-AzP2sVpnGateway" har uppdaterats": Den valfria växelparametern "EnableInternetSecurityFlag" har lagts till för kunder som anger värdet true för att aktivera Internetsäkerhet på P2SVpnGateway, som ska användas för plats-till-plats-klienter.</span><span class="sxs-lookup"><span data-stu-id="08996-237">Updated 'New-AzP2sVpnGateway': Added optional switch parameter 'EnableInternetSecurityFlag' for customers to set true to enable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
- <span data-ttu-id="08996-238">"Update-AzP2sVpnGateway" har uppdaterats: De valfria växelparametrarna "EnableInternetSecurityFlag" eller "DisableInternetSecurityFlag" har lagts till för kunder som anger värdet true/false för att aktivera/inaktivera Internetsäkerhet på P2SVpnGateway, som ska användas för plats-till-plats-klienter.</span><span class="sxs-lookup"><span data-stu-id="08996-238">Updated 'Update-AzP2sVpnGateway': Added optional switch parameters 'EnableInternetSecurityFlag' or 'DisableInternetSecurityFlag' for customers to set true/false to enable/disable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
* <span data-ttu-id="08996-239">Den nya cmdleten "Reset-AzP2sVpnGateway" har lagts till för att kunder ska kunna återställa/starta om sina VirtualWan-P2SVpnGateway för felsökning.</span><span class="sxs-lookup"><span data-stu-id="08996-239">Added new cmdlet 'Reset-AzP2sVpnGateway' for customers to reset/reboot their VirtualWan P2SVpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="08996-240">Den nya cmdleten "Reset-AzVpnGateway" har lagts till för att kunder ska kunna återställa/starta om VirtualWan VpnGateway för felsökning.</span><span class="sxs-lookup"><span data-stu-id="08996-240">Added new cmdlet 'Reset-AzVpnGateway' for customers to reset/reboot their VirtualWan VpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="08996-241">"Set-AzVirtualNetworkSubnetConfig" har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="08996-241">Updated 'Set-AzVirtualNetworkSubnetConfig'</span></span>
    - <span data-ttu-id="08996-242">Ange egenskaper för NSG och routningstabell för undernät till null om det anges explicit i parametrarna [#1548] [#9718]</span><span class="sxs-lookup"><span data-stu-id="08996-242">Set NSG and Route Table properties of subnet to null if explicitly set in parameters [#1548][#9718]</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="08996-243">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="08996-243">Az.RecoveryServices</span></span>
* <span data-ttu-id="08996-244">Åtgärdat borttagningstillståndet för säkerhetskopieringsobjekt.</span><span class="sxs-lookup"><span data-stu-id="08996-244">Fixed the Delete State for workload Backup Items.</span></span>

#### <a name="azresources"></a><span data-ttu-id="08996-245">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08996-245">Az.Resources</span></span>
* <span data-ttu-id="08996-246">Lagt till saknad kontroll för Set-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="08996-246">Added missing check for Set-AzRoleAssignment</span></span>
* <span data-ttu-id="08996-247">Attribut som medför icke-bakåtkompatibel ändring har lagts till i parametern "SubscriptionId" i "Get-AzResourceGroupDeploymentOperation"</span><span class="sxs-lookup"><span data-stu-id="08996-247">Added breaking change attribute to 'SubscriptionId' parameter of 'Get-AzResourceGroupDeploymentOperation'</span></span>
* <span data-ttu-id="08996-248">Uppdaterat What-If-cmdlets i ARM-mall så att resursändringar av typen 'Ignorera' visas sist</span><span class="sxs-lookup"><span data-stu-id="08996-248">Updated ARM template What-If cmdlets to show 'Ignore' resource changes last</span></span>
* <span data-ttu-id="08996-249">Åtgärdat serialiseringsproblem med säkra parametrar och matrisparametrar för distributionscmdlets [#12773]</span><span class="sxs-lookup"><span data-stu-id="08996-249">Fixed secure and array parameter serialization issues for deployment cmdlets [#12773]</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="08996-250">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="08996-250">Az.ServiceFabric</span></span>
* <span data-ttu-id="08996-251">Nya cmdletar har lagts till för hanterade kluster och nodtyper:</span><span class="sxs-lookup"><span data-stu-id="08996-251">Added new cmdlets for managed clusters and node types:</span></span>
    - <span data-ttu-id="08996-252">"New-AzServiceFabricManagedCluster"</span><span class="sxs-lookup"><span data-stu-id="08996-252">'New-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="08996-253">"Get-AzServiceFabricManagedCluster"</span><span class="sxs-lookup"><span data-stu-id="08996-253">'Get-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="08996-254">"Set-AzServiceFabricManagedCluster"</span><span class="sxs-lookup"><span data-stu-id="08996-254">'Set-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="08996-255">"Remove-AzServiceFabricManagedCluster"</span><span class="sxs-lookup"><span data-stu-id="08996-255">'Remove-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="08996-256">"Add-AzServiceFabricManagedClusterClientCertificate"</span><span class="sxs-lookup"><span data-stu-id="08996-256">'Add-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="08996-257">"Remove-AzServiceFabricManagedClusterClientCertificate"</span><span class="sxs-lookup"><span data-stu-id="08996-257">'Remove-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="08996-258">"New-AzServiceFabricManagedNodeType"</span><span class="sxs-lookup"><span data-stu-id="08996-258">'New-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="08996-259">"Get-AzServiceFabricManagedNodeType"</span><span class="sxs-lookup"><span data-stu-id="08996-259">'Get-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="08996-260">"Set-AzServiceFabricManagedNodeType"</span><span class="sxs-lookup"><span data-stu-id="08996-260">'Set-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="08996-261">"Remove-AzServiceFabricManagedNodeType"</span><span class="sxs-lookup"><span data-stu-id="08996-261">'Remove-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="08996-262">"Add-AzServiceFabricManagedNodeTypeVMExtension"</span><span class="sxs-lookup"><span data-stu-id="08996-262">'Add-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="08996-263">"Add-AzServiceFabricManagedNodeTypeVMSecret"</span><span class="sxs-lookup"><span data-stu-id="08996-263">'Add-AzServiceFabricManagedNodeTypeVMSecret'</span></span>
    - <span data-ttu-id="08996-264">"Remove-AzServiceFabricManagedNodeTypeVMExtension"</span><span class="sxs-lookup"><span data-stu-id="08996-264">'Remove-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="08996-265">"Restart-AzServiceFabricManagedNodeTyp"</span><span class="sxs-lookup"><span data-stu-id="08996-265">'Restart-AzServiceFabricManagedNodeTyp'</span></span>
* <span data-ttu-id="08996-266">Service Fabric SDK har uppgraderats till version 1.2.0 som använder Service Fabric-resursprovidern med API-version 2020-03-01 för aktuell modell och 2020-01-01-förhandsversion för hanterade kluster.</span><span class="sxs-lookup"><span data-stu-id="08996-266">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2020-03-01 for the current model and 2020-01-01-preview for managed clusters.</span></span>

#### <a name="azsql"></a><span data-ttu-id="08996-267">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08996-267">Az.Sql</span></span>
* <span data-ttu-id="08996-268">BackupStorageRedundancy har lagts till i "New-AzSqlInstance" och "Get-AzSqlInstance"</span><span class="sxs-lookup"><span data-stu-id="08996-268">Added BackupStorageRedundancy to 'New-AzSqlInstance' and 'Get-AzSqlInstance'</span></span>
* <span data-ttu-id="08996-269">Cmdlet:en "Get-AzSqlServerActiveDirectoryOnlyAuthentication" har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-269">Added cmdlet 'Get-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="08996-270">Cmdlet:en "Enable-AzSqlServerActiveDirectoryOnlyAuthentication" har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-270">Added cmdlet 'Enable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="08996-271">Force-parametern har lagts till i "New-AzSqlInstance"</span><span class="sxs-lookup"><span data-stu-id="08996-271">Added Force parameter to 'New-AzSqlInstance'</span></span>
* <span data-ttu-id="08996-272">Cmdlet:ar för logguppspelningstjänst för hanterade databaser har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-272">Added cmdlets for Managed Database Log Replay service</span></span>
    - <span data-ttu-id="08996-273">"Start-AzSqlInstanceDatabaseLogReplay"</span><span class="sxs-lookup"><span data-stu-id="08996-273">'Start-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="08996-274">"Get-AzSqlInstanceDatabaseLogReplay"</span><span class="sxs-lookup"><span data-stu-id="08996-274">'Get-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="08996-275">"Complete-AzSqlInstanceDatabaseLogReplay"</span><span class="sxs-lookup"><span data-stu-id="08996-275">'Complete-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="08996-276">"Stop-AzSqlInstanceDatabaseLogReplay"</span><span class="sxs-lookup"><span data-stu-id="08996-276">'Stop-AzSqlInstanceDatabaseLogReplay'</span></span>
* <span data-ttu-id="08996-277">Cmdlet:en "Get-AzSqlInstanceActiveDirectoryOnlyAuthentication" har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-277">Added cmdlet 'Get-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="08996-278">Cmdlet:en "Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication" har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-278">Added cmdlet 'Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="08996-279">Cmdlet:en "Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication" har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-279">Added cmdlet 'Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="08996-280">Cmdletarna "New-AzSqlDatabaseImport" och "New-AzSqlDatabaseExport" har uppdaterats för att stödja funktioner för nätverksisolering</span><span class="sxs-lookup"><span data-stu-id="08996-280">Updated cmdlets 'New-AzSqlDatabaseImport' and 'New-AzSqlDatabaseExport' to support network isolation functionality</span></span>
* <span data-ttu-id="08996-281">Cmdleten "New-AzSqlDatabaseImportExisting" har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-281">Added cmdlet 'New-AzSqlDatabaseImportExisting'</span></span>
* <span data-ttu-id="08996-282">Uppdaterade databas-cmdlet:ar som stöder typspecifikation av lagringsenhet för säkerhetskopiering</span><span class="sxs-lookup"><span data-stu-id="08996-282">Updated Databases cmdlets to support backup storage type specification</span></span>
* <span data-ttu-id="08996-283">Force-parametern har lagts till i "New-AzSqlDatabase"</span><span class="sxs-lookup"><span data-stu-id="08996-283">Added Force parameter to 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="08996-284">Varning för BackupStorageRedundancy-konfiguration har lagts till i utvalda regioner i "New-AzSqlDatabase"</span><span class="sxs-lookup"><span data-stu-id="08996-284">Added warning for BackupStorageRedundancy configuration in select regions in 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="08996-285">Uppdaterade ActiveDirectoryOnlyAuthentication-cmdletar för server och instans så att de innehåller ResourceId och InputObject</span><span class="sxs-lookup"><span data-stu-id="08996-285">Updated ActiveDirectoryOnlyAuthentication cmdlets for server and instance to include ResourceId and InputObject</span></span>

#### <a name="azstorage"></a><span data-ttu-id="08996-286">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="08996-286">Az.Storage</span></span>
* <span data-ttu-id="08996-287">Åtgärdade fel vid uppladdning av blob genom uppgradering till Microsoft.Azure.Storage.DataMovement 2.0.0 [#12220]</span><span class="sxs-lookup"><span data-stu-id="08996-287">Fixed upload blob fail by upgrade to Microsoft.Azure.Storage.DataMovement 2.0.0 [#12220]</span></span>
* <span data-ttu-id="08996-288">Stöd för återställning baserat på tidpunkt</span><span class="sxs-lookup"><span data-stu-id="08996-288">Supported Point In Time Restore</span></span>
    - <span data-ttu-id="08996-289">"Enable-AzStorageBlobRestorePolicy"</span><span class="sxs-lookup"><span data-stu-id="08996-289">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="08996-290">"Disable-AzStorageBlobRestorePolicy"</span><span class="sxs-lookup"><span data-stu-id="08996-290">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="08996-291">"New-AzStorageBlobRangeToRestore"</span><span class="sxs-lookup"><span data-stu-id="08996-291">'New-AzStorageBlobRangeToRestore'</span></span>
    - <span data-ttu-id="08996-292">"Restore-AzStorageBlobRange"</span><span class="sxs-lookup"><span data-stu-id="08996-292">'Restore-AzStorageBlobRange'</span></span>
* <span data-ttu-id="08996-293">Stöd för att hämta status för blobåterställning genom att köra get-AzureRMStorageAccount med parametern -IncludeBlobRestoreStatus</span><span class="sxs-lookup"><span data-stu-id="08996-293">Supported get blob restore status of Storage account by run get-AzureRMStorageAccount with parameter -IncludeBlobRestoreStatus</span></span> 
    - <span data-ttu-id="08996-294">"Get-AzureRMStorageAccount"</span><span class="sxs-lookup"><span data-stu-id="08996-294">'Get-AzureRMStorageAccount'</span></span>
* <span data-ttu-id="08996-295">Meddelande om icke-bakåtkompatibel ändring för kommande ändring av cmdlet-utdata har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-295">Added breaking change warning message for upcoming cmdlet output change</span></span>
    - <span data-ttu-id="08996-296">"Get-AzStorageContainerStoredAccessPolicy"</span><span class="sxs-lookup"><span data-stu-id="08996-296">'Get-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="08996-297">"Set-AzStorageContainerStoredAccessPolicy"</span><span class="sxs-lookup"><span data-stu-id="08996-297">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="08996-298">"Set-AzStorageAccountManagementPolicy"</span><span class="sxs-lookup"><span data-stu-id="08996-298">'Set-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="08996-299">"Get-AzStorageAccountManagementPolicy"</span><span class="sxs-lookup"><span data-stu-id="08996-299">'Get-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="08996-300">"Add-AzStorageAccountManagementPolicyAction"</span><span class="sxs-lookup"><span data-stu-id="08996-300">'Add-AzStorageAccountManagementPolicyAction'</span></span>
    - <span data-ttu-id="08996-301">"New-AzStorageAccountManagementPolicyRule"</span><span class="sxs-lookup"><span data-stu-id="08996-301">'New-AzStorageAccountManagementPolicyRule'</span></span>
* <span data-ttu-id="08996-302">Uppgraderade Microsoft.Azure.Cosmos.Table SDK till 1.0.8</span><span class="sxs-lookup"><span data-stu-id="08996-302">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.8</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="08996-303">Tack till våra community-deltagare</span><span class="sxs-lookup"><span data-stu-id="08996-303">Thanks to our community contributors</span></span>
* <span data-ttu-id="08996-304">Thomas Van Laere (@ThomVanL), Lägg till Dockerfile-alpine-3.10 (#12911)</span><span class="sxs-lookup"><span data-stu-id="08996-304">Thomas Van Laere (@ThomVanL), Add Dockerfile-alpine-3.10 (#12911)</span></span> 
* <span data-ttu-id="08996-305">Lohith Chowdary Chilukuri (@Lochiluk), Uppdatering av Remove-AzNetworkInterfaceIpConfig.md (#12807)</span><span class="sxs-lookup"><span data-stu-id="08996-305">Lohith Chowdary Chilukuri (@Lochiluk), Update Remove-AzNetworkInterfaceIpConfig.md (#12807)</span></span> 
* <span data-ttu-id="08996-306">Roberth Strand (@roberthstrand), Get-AzResourceGroup – Nytt exempel och rensning (#12828)</span><span class="sxs-lookup"><span data-stu-id="08996-306">Roberth Strand (@roberthstrand), Get-AzResourceGroup - New example, and cleanup (#12828)</span></span> 
* <span data-ttu-id="08996-307">Ravi Mishra (@inmishrar), uppdatering av Azure Web App-körningsstack till DOTNETCORE (#12833)</span><span class="sxs-lookup"><span data-stu-id="08996-307">Ravi Mishra (@inmishrar), update Azure Web App runtime stack to DOTNETCORE (#12833)</span></span> 
* <span data-ttu-id="08996-308">@jack-education, uppdaterat set-AzVirtualNetworkSubnetConfig för att tillåta att NSG och routningstabell tas bort från undernät (#12351)</span><span class="sxs-lookup"><span data-stu-id="08996-308">@jack-education, Updated Set-AzVirtualNetworkSubnetConfig to allow NSG and Route Table to be removed from subnet (#12351)</span></span> 
* <span data-ttu-id="08996-309">@hagop-globanet, uppdatering av Add-AzApplicationGatewayCustomError.md (#12784)</span><span class="sxs-lookup"><span data-stu-id="08996-309">@hagop-globanet, Update Add-AzApplicationGatewayCustomError.md (#12784)</span></span> 
* <span data-ttu-id="08996-310">Joshua Van Daalen (@greenSacrifice)</span><span class="sxs-lookup"><span data-stu-id="08996-310">Joshua Van Daalen (@greenSacrifice)</span></span>
  * <span data-ttu-id="08996-311">Uppdatering av stavning av egenskaper till egenskaper (#12821)</span><span class="sxs-lookup"><span data-stu-id="08996-311">Update spelling of Property to Property (#12821)</span></span> 
  * <span data-ttu-id="08996-312">Uppdatering av New-AzResourceLock.md-exempel (#12806)</span><span class="sxs-lookup"><span data-stu-id="08996-312">Update New-AzResourceLock.md examples (#12806)</span></span>
* <span data-ttu-id="08996-313">Eragon Riddle (@eragonriddle), korrigerat fältnamn för parameter i exemplet (#12825)</span><span class="sxs-lookup"><span data-stu-id="08996-313">Eragon Riddle (@eragonriddle), Corrected parameter field name in the example (#12825)</span></span> 
* <span data-ttu-id="08996-314">@rossifumax, åtgärdat skrivfel i New-AzConfigurationAssignment.md (#12701)</span><span class="sxs-lookup"><span data-stu-id="08996-314">@rossifumax, Fix typo in New-AzConfigurationAssignment.md (#12701)</span></span>

## <a name="461---august-2020"></a><span data-ttu-id="08996-315">4.6.1 – augusti 2020</span><span class="sxs-lookup"><span data-stu-id="08996-315">4.6.1 - August 2020</span></span>
#### <a name="azcompute"></a><span data-ttu-id="08996-316">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08996-316">Az.Compute</span></span>
* <span data-ttu-id="08996-317">Korrigerade EncryptionAtHost-parametern i New-AzVm för att ta bort standardvärdet FALSE [#12776]</span><span class="sxs-lookup"><span data-stu-id="08996-317">Patched '-EncryptionAtHost' parameter in 'New-AzVm' to remove default value of false [#12776]</span></span>

## <a name="460---august-2020"></a><span data-ttu-id="08996-318">4.6.0 – augusti 2020</span><span class="sxs-lookup"><span data-stu-id="08996-318">4.6.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="08996-319">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="08996-319">Az.Accounts</span></span>
* <span data-ttu-id="08996-320">Alla offentliga molnmiljöer läses in när slutpunktsidentifieringen inte returnerar AzureCloud (standard) eller andra offentliga miljöer [#12633]</span><span class="sxs-lookup"><span data-stu-id="08996-320">Loaded all public cloud environments when discovery endpoint doesn't return default AzureCloud or other public environments [#12633]</span></span>
* <span data-ttu-id="08996-321">SubscriptionPolicies har exponerats i Get-AzSubscription [#12551]</span><span class="sxs-lookup"><span data-stu-id="08996-321">Exposed SubscriptionPolicies in 'Get-AzSubscription' [#12551]</span></span>

#### <a name="azautomation"></a><span data-ttu-id="08996-322">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="08996-322">Az.Automation</span></span>
* <span data-ttu-id="08996-323">Parametern -RunOn har lagts till i Set-AzAutomationWebhook för att ange en Hybrid Worker-grupp</span><span class="sxs-lookup"><span data-stu-id="08996-323">Added '-RunOn' parameters to 'Set-AzAutomationWebhook' to specify a Hybrid Worker Group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08996-324">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08996-324">Az.Compute</span></span>
* <span data-ttu-id="08996-325">Parametern -EncryptionAtHost har lagts till i New-AzVm, New-AzVmss, New-AzVMConfig, New-AzVmssConfig, Update-AzVM och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="08996-325">Added '-EncryptionAtHost' parameter to 'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM', and 'Update-AzVmss'</span></span>
* <span data-ttu-id="08996-326">SecurityProfile har lagts till i Get-AzVM och Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="08996-326">Added 'SecurityProfile' to 'Get-AzVM' and 'Get-AzVmss' return object</span></span>
* <span data-ttu-id="08996-327">Växeln -InstanceView har lagts till som valfri parameter i Get-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="08996-327">Added '-InstanceView' switch as optional parameter to 'Get-AzHostGroup'</span></span>
* <span data-ttu-id="08996-328">En ny cmdlet, Invoke-AzVmPatchAssessment, har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-328">Added new cmdlet 'Invoke-AzVmPatchAssessment'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="08996-329">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="08996-329">Az.DataFactory</span></span>
* <span data-ttu-id="08996-330">Saknade egenskaper har lagts till i klassen PSPipelineRun.</span><span class="sxs-lookup"><span data-stu-id="08996-330">Added missing properties to PSPipelineRun class.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="08996-331">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="08996-331">Az.HDInsight</span></span>
* <span data-ttu-id="08996-332">Stöd för att skapa kluster med funktionen för kryptering under överföring.</span><span class="sxs-lookup"><span data-stu-id="08996-332">Supported creating cluster with encryption at host feature.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="08996-333">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="08996-333">Az.KeyVault</span></span>
* <span data-ttu-id="08996-334">Varningsmeddelanden har lagts till för planering att inaktivera mjuk borttagning</span><span class="sxs-lookup"><span data-stu-id="08996-334">Added warning messages for planning to disable soft delete</span></span>
* <span data-ttu-id="08996-335">Varningsmeddelanden har lagts till för planering att ta bort attributet SecretValueText</span><span class="sxs-lookup"><span data-stu-id="08996-335">Added warning messages for planning to remove attribute SecretValueText</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="08996-336">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="08996-336">Az.Maintenance</span></span>
* <span data-ttu-id="08996-337">Valfria schemarelaterade fält har lagts till i New-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="08996-337">Added optional schedule related fields to 'New-AzMaintenanceConfiguration'</span></span>
* <span data-ttu-id="08996-338">En ny cmdlet har lagts till för Get-AzMaintenancePublicConfiguration</span><span class="sxs-lookup"><span data-stu-id="08996-338">Added new cmdlet for 'Get-AzMaintenancePublicConfiguration'</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="08996-339">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="08996-339">Az.ManagedServices</span></span>
* <span data-ttu-id="08996-340">Varningar har lagts till om icke-bakåtkompatibla ändringar för cmdletar för tilldelning och definition av hanterade tjänster</span><span class="sxs-lookup"><span data-stu-id="08996-340">Added breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="08996-341">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="08996-341">Az.Monitor</span></span>
* <span data-ttu-id="08996-342">Utökade parametern som angetts i Set-AzDiagnosticSetting för separering av aktivering av loggar och mått [#12482]</span><span class="sxs-lookup"><span data-stu-id="08996-342">Extended the parameter set in 'Set-AzDiagnosticSetting' for separation of Logs and Metrics enablement [#12482]</span></span>
* <span data-ttu-id="08996-343">Åtgärdat fel för Add-AzMetricAlertRuleV2 vid hämtning av måttavisering från pipelinen</span><span class="sxs-lookup"><span data-stu-id="08996-343">Fixed bug for 'Add-AzMetricAlertRuleV2' when getting metric alert from pipeline</span></span>

#### <a name="azresources"></a><span data-ttu-id="08996-344">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08996-344">Az.Resources</span></span>
* <span data-ttu-id="08996-345">Get-AzPolicyAlias-svaret har uppdaterats för att ta med information som anger om aliaset kan ändras eller inte av Azure Policy.</span><span class="sxs-lookup"><span data-stu-id="08996-345">Updated 'Get-AzPolicyAlias' response to include information indicating whether the alias is modifiable by Azure Policy.</span></span>
* <span data-ttu-id="08996-346">Skapade en ny cmdlet, set-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="08996-346">Created new cmdlet 'Set-AzRoleAssignment'</span></span>
* <span data-ttu-id="08996-347">Get-AzDeploymentManagementGroupWhatIfResult har lagts till för att hämta What-If-resultat för ARM-mall i hanteringsgruppsomfånget</span><span class="sxs-lookup"><span data-stu-id="08996-347">Added 'Get-AzDeploymentManagementGroupWhatIfResult' for getting ARM template What-If results at management Group scope</span></span>
* <span data-ttu-id="08996-348">En ny cmdlet, Get-AzTenantWhatIfResult, har lagts till för att hämta What-If-resultat för ARM-mall i klientorganisationsomfånget</span><span class="sxs-lookup"><span data-stu-id="08996-348">Added 'Get-AzTenantWhatIfResult' new cmdlet for getting ARM template What-If results at tenant scope</span></span>
* <span data-ttu-id="08996-349">-WhatIf och -Confirm har åsidosatts för New-AzManagementGroupDeployment och New-AzTenantDeployment för att använda What-If-resultat för ARM-mall</span><span class="sxs-lookup"><span data-stu-id="08996-349">Overrode '-WhatIf' and '-Confirm' for 'New-AzManagementGroupDeployment' and 'New-AzTenantDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="08996-350">Beteenden har åtgärdats för -WhatIf och -Confirm för nya cmdletar för distribution så att de stämmer överens med False och</span><span class="sxs-lookup"><span data-stu-id="08996-350">Fixed the behaviors of '-WhatIf' and '-Confirm' for new deployment cmdlets so they comply with False and</span></span> 
* <span data-ttu-id="08996-351">Serialiseringsfel har åtgärdats för -TemplateObject och TemplateParameterObject [#1528] [#6292]</span><span class="sxs-lookup"><span data-stu-id="08996-351">Fixed serialization error for '-TemplateObject' and 'TemplateParameterObject' [#1528] [#6292]</span></span>
* <span data-ttu-id="08996-352">Attribut som medför icke-bakåtkompatibel ändring har lagts till i Get-AzResourceGroupDeploymentOperation för den kommande ändringen av utdatatyp</span><span class="sxs-lookup"><span data-stu-id="08996-352">Added breaking change attribute to 'Get-AzResourceGroupDeploymentOperation' for the upcoming output type change</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="08996-353">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="08996-353">Az.SignalR</span></span>
* <span data-ttu-id="08996-354">Fel i hjälpfilerna Restart-AzSignalR och Update-AzSignalR har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="08996-354">Fixed 'Restart-AzSignalR' and 'Update-AzSignalR' help files errors</span></span>
* <span data-ttu-id="08996-355">Cmdletarna Update-AzSignalRNetworkAcl och Set-AzSignalRUpstream har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-355">Added cmdlets 'Update-AzSignalRNetworkAcl', 'Set-AzSignalRUpstream'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="08996-356">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="08996-356">Az.Storage</span></span>
* <span data-ttu-id="08996-357">Stöd för blobfrågeacceleration</span><span class="sxs-lookup"><span data-stu-id="08996-357">Supported blob query acceleration</span></span>
    -  <span data-ttu-id="08996-358">Get-AzStorageBlobQueryResult</span><span class="sxs-lookup"><span data-stu-id="08996-358">'Get-AzStorageBlobQueryResult'</span></span>
    -  <span data-ttu-id="08996-359">New-AzStorageBlobQueryConfig</span><span class="sxs-lookup"><span data-stu-id="08996-359">'New-AzStorageBlobQueryConfig'</span></span>
* <span data-ttu-id="08996-360">Hjälpfil har lagts till, ytterligare beskrivning har lagts till och stavfel har korrigerats</span><span class="sxs-lookup"><span data-stu-id="08996-360">Updated help file, added more description, and fixed typo</span></span>
    -  <span data-ttu-id="08996-361">”Start-AzStorageBlobCopy”</span><span class="sxs-lookup"><span data-stu-id="08996-361">'Start-AzStorageBlobCopy'</span></span>
    -  <span data-ttu-id="08996-362">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="08996-362">'Get-AzDataLakeGen2Item'</span></span>
* <span data-ttu-id="08996-363">Problem med att ladda ned blob när relaterad underordnad katalog saknas har åtgärdats [#12592]</span><span class="sxs-lookup"><span data-stu-id="08996-363">Fixed download blob fail when related sub directory not exist [#12592]</span></span>
    -  <span data-ttu-id="08996-364">”Get-AzStorageBlobContent”</span><span class="sxs-lookup"><span data-stu-id="08996-364">'Get-AzStorageBlobContent'</span></span>
* <span data-ttu-id="08996-365">Replikeringsprincip för att ange, hämta, ta bort objekt på Storage-konton stöds</span><span class="sxs-lookup"><span data-stu-id="08996-365">Supported Set/Get/Remove Object Replication Policy on Storage accounts</span></span>
    - <span data-ttu-id="08996-366">New-AzStorageObjectReplicationPolicyRule</span><span class="sxs-lookup"><span data-stu-id="08996-366">'New-AzStorageObjectReplicationPolicyRule'</span></span>
    - <span data-ttu-id="08996-367">Set-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="08996-367">'Set-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="08996-368">Get-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="08996-368">'Get-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="08996-369">Remove-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="08996-369">'Remove-AzStorageObjectReplicationPolicy'</span></span>
* <span data-ttu-id="08996-370">Stöd har lagts till för att aktivera/inaktivera ChangeFeed i Blob Service för ett Storage-konto</span><span class="sxs-lookup"><span data-stu-id="08996-370">Supported enable/disable ChangeFeed on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="08996-371">”Update-AzStorageBlobServiceProperty”</span><span class="sxs-lookup"><span data-stu-id="08996-371">'Update-AzStorageBlobServiceProperty'</span></span>

## <a name="450---august-2020"></a><span data-ttu-id="08996-372">4.5.0 – augusti 2020</span><span class="sxs-lookup"><span data-stu-id="08996-372">4.5.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="08996-373">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="08996-373">Az.Accounts</span></span>
* <span data-ttu-id="08996-374">Uppdaterade ”Connect-AzAccount” så att det accepterar parametern ”MaxContextPopulation” [#9865]</span><span class="sxs-lookup"><span data-stu-id="08996-374">Updated 'Connect-AzAccount' to accept parameter 'MaxContextPopulation' [#9865]</span></span>
* <span data-ttu-id="08996-375">Uppdaterade SubscriptionClient-versionen till 2019-06-01 och visa klientdomäner [#9838]</span><span class="sxs-lookup"><span data-stu-id="08996-375">Updated SubscriptionClient version to 2019-06-01 and display tenant domains [#9838]</span></span>
* <span data-ttu-id="08996-376">Information om hemklientorganisation och managedBy-klientorganisation som stöds för prenumerationen</span><span class="sxs-lookup"><span data-stu-id="08996-376">Supported home tenant and managedBy tenant information of subscription</span></span>
* <span data-ttu-id="08996-377">Korrigerade modulnamn, versionsinformation i telemetridata</span><span class="sxs-lookup"><span data-stu-id="08996-377">Corrected module name, version info in telemetry data</span></span>
* <span data-ttu-id="08996-378">Justerade SqlDatabaseDnsSuffix och ServiceManagementUrl om miljöns slutpunkt för metadata returnerar ett inkompatibelt värde</span><span class="sxs-lookup"><span data-stu-id="08996-378">Adjusted SqlDatabaseDnsSuffix and ServiceManagementUrl if environment metadata endpoint returns incompatible value</span></span>

#### <a name="azaks"></a><span data-ttu-id="08996-379">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="08996-379">Az.Aks</span></span>
* <span data-ttu-id="08996-380">Tog bort ”ClientIdAndSecret” för ”ServicePrincipalIdAndSecret” och ställde in ”ClientIdAndSecret” som ett alias [#12381].</span><span class="sxs-lookup"><span data-stu-id="08996-380">Removed 'ClientIdAndSecret' to 'ServicePrincipalIdAndSecret' and set 'ClientIdAndSecret' as an alias [#12381].</span></span>
* <span data-ttu-id="08996-381">Tog bort ”Get-AzAks”/”New-AzAks”/”Remove-AzAks”/”Set-AzAks” för ”Get-AzAksCluster”/”New-AzAksCluster”/”Remove-AzAksCluster”/”Set-AzAksCluster” och ställde in de ursprungliga som alias [#12373].</span><span class="sxs-lookup"><span data-stu-id="08996-381">Removed 'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' to 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' and set the original ones as alias [#12373].</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="08996-382">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="08996-382">Az.ApiManagement</span></span>
* <span data-ttu-id="08996-383">Lade till ny cmdlet: ”Add-AzApiManagementApiToGateway”.</span><span class="sxs-lookup"><span data-stu-id="08996-383">Added new 'Add-AzApiManagementApiToGateway' cmdlet.</span></span>
* <span data-ttu-id="08996-384">Lade till ny cmdlet: ”Get-AzApiManagementGateway”.</span><span class="sxs-lookup"><span data-stu-id="08996-384">Added new 'Get-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="08996-385">Lade till ny cmdlet: ”Get-AzApiManagementGatewayHostnameConfiguration”.</span><span class="sxs-lookup"><span data-stu-id="08996-385">Added new 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="08996-386">Lade till ny cmdlet: ”Get-AzApiManagementGatewayKey”.</span><span class="sxs-lookup"><span data-stu-id="08996-386">Added new 'Get-AzApiManagementGatewayKey' cmdlet.</span></span>
* <span data-ttu-id="08996-387">Lade till ny cmdlet: ”New-AzApiManagementGateway”.</span><span class="sxs-lookup"><span data-stu-id="08996-387">Added new 'New-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="08996-388">Lade till ny cmdlet: ”New-AzApiManagementGatewayHostnameConfiguration”.</span><span class="sxs-lookup"><span data-stu-id="08996-388">Added new 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="08996-389">Lade till ny cmdlet: ”New-AzApiManagementResourceLocationObject”.</span><span class="sxs-lookup"><span data-stu-id="08996-389">Added new 'New-AzApiManagementResourceLocationObject' cmdlet.</span></span>
* <span data-ttu-id="08996-390">Lade till ny cmdlet: ”Remove-AzApiManagementApiFromGateway”.</span><span class="sxs-lookup"><span data-stu-id="08996-390">Added new 'Remove-AzApiManagementApiFromGateway' cmdlet.</span></span>
* <span data-ttu-id="08996-391">Lade till ny cmdlet: ”Remove-AzApiManagementGateway”.</span><span class="sxs-lookup"><span data-stu-id="08996-391">Added new 'Remove-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="08996-392">Lade till ny cmdlet: ”Remove-AzApiManagementGatewayHostnameConfiguration”.</span><span class="sxs-lookup"><span data-stu-id="08996-392">Added new 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="08996-393">Lade till ny cmdlet: ”Update-AzApiManagementGateway”.</span><span class="sxs-lookup"><span data-stu-id="08996-393">Added new 'Update-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="08996-394">Lade till den nya valfria parametern [-GatewayId] till cmdleten ”Get-AzApiManagementApi”.</span><span class="sxs-lookup"><span data-stu-id="08996-394">Added new optional [-GatewayId] parameter to the 'Get-AzApiManagementApi' cmdlet.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="08996-395">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="08996-395">Az.CognitiveServices</span></span>
* <span data-ttu-id="08996-396">Använde ”Neka” som standardåtgärd för NetworkRules.</span><span class="sxs-lookup"><span data-stu-id="08996-396">Used 'Deny' specifically as NetworkRules default action.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="08996-397">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="08996-397">Az.FrontDoor</span></span>
* <span data-ttu-id="08996-398">Åtgärdade ett problem där ett undantag uppstår när Enum.Parse försöker att tvinga ett null-värde till aktiverade eller inaktiverade uppräkningsvärden [#12344]</span><span class="sxs-lookup"><span data-stu-id="08996-398">Fixed an issue where an exception is being thrown when Enum.Parse tries to coerce a null value to an Enabled or Disabled enum values [#12344]</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="08996-399">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="08996-399">Az.HDInsight</span></span>
* <span data-ttu-id="08996-400">Stöd för att skapa kluster med funktionen Kryptering under överföring.</span><span class="sxs-lookup"><span data-stu-id="08996-400">Supported creating cluster with encryption in transit feature.</span></span>
    - <span data-ttu-id="08996-401">Lägg till den nya parametern ”EncryptionInTransit” till cmdleten ”New-AzHDInsightCluster”</span><span class="sxs-lookup"><span data-stu-id="08996-401">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="08996-402">Lägg till den nya parametern ”EncryptionInTransit” till cmdleten ”New-AzHDInsightClusterConfig”</span><span class="sxs-lookup"><span data-stu-id="08996-402">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="08996-403">Stöd för att skapa kluster med funktionen privat länk:</span><span class="sxs-lookup"><span data-stu-id="08996-403">Supported creating cluster with private link feature:</span></span>
    - <span data-ttu-id="08996-404">Lägg till de nya parametrarna ”PublicNetworkAccessType” och ”OutboundPublicNetworkAccessType” till cmdleten ”New-AzHDInsightCluster”</span><span class="sxs-lookup"><span data-stu-id="08996-404">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="08996-405">Lägg till de nya parametrarna ”PublicNetworkAccessType” och ”OutboundPublicNetworkAccessType” till cmdleten ”New-AzHDInsightClusterConfig”</span><span class="sxs-lookup"><span data-stu-id="08996-405">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="08996-406">Returnerade information om det virtuella nätverket vid anrop till ”New-AzHDInsightCluster” eller ”Get-AzHDInsightCluster”</span><span class="sxs-lookup"><span data-stu-id="08996-406">Returned virtual network information when calling 'New-AzHDInsightCluster' or 'Get-AzHDInsightCluster'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="08996-407">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08996-407">Az.Network</span></span>
* <span data-ttu-id="08996-408">Stöd har lagts till för parametern AddressPrefixType i ”Remove-AzExpressRouteCircuitConnectionConfig”</span><span class="sxs-lookup"><span data-stu-id="08996-408">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="08996-409">Lade till bakåtkompatibel ändringar: PeerAddressType-funktioner för privat peering i ”Remove-AzExpressRouteCircutPeeringConfig”.</span><span class="sxs-lookup"><span data-stu-id="08996-409">Added non-breaking changes: PeerAddressType functionality for Private Peering in 'Remove-AzExpressRouteCircutPeeringConfig'.</span></span>
* <span data-ttu-id="08996-410">Koden ändrades för att ignorera skiftläge för parametrarna AddressPrefixType och PeerAddressType.</span><span class="sxs-lookup"><span data-stu-id="08996-410">Code changed to ignore case for AddressPrefixType and PeerAddressType parameter.</span></span>
* <span data-ttu-id="08996-411">Ändrade varningsmeddelandet för ”New-AzLoadBalancerFrontendIpConfig”, ”New-AzPublicIpAddress” och ”New-AzPublicIpPrefix”.</span><span class="sxs-lookup"><span data-stu-id="08996-411">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="08996-412">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="08996-412">Az.OperationalInsights</span></span>
* <span data-ttu-id="08996-413">Lade till alternativet ”-ForceDelete” för ”Remove-AzOperationalInsightsworkspace”</span><span class="sxs-lookup"><span data-stu-id="08996-413">Added '-ForceDelete' option for 'Remove-AzOperationalInsightsworkspace'</span></span>
* <span data-ttu-id="08996-414">Lade till ny cmdlet: ”Get-AzOperationalInsightsDeletedWorkspace”</span><span class="sxs-lookup"><span data-stu-id="08996-414">Added new cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'</span></span>
* <span data-ttu-id="08996-415">Lade till ny cmdlet: ”Restore-AzOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="08996-415">Added new cmdlet 'Restore-AzOperationalInsightsWorkspace'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="08996-416">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="08996-416">Az.RecoveryServices</span></span>
* <span data-ttu-id="08996-417">Förbättrade sättet Azure Backup-containrar/objekt identifieras.</span><span class="sxs-lookup"><span data-stu-id="08996-417">Improved the Azure Backup container/item discovery experience.</span></span>

#### <a name="azresources"></a><span data-ttu-id="08996-418">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08996-418">Az.Resources</span></span>
* <span data-ttu-id="08996-419">Lade till egenskaperna ”Condition”, ”ConditionVersion” och ”Description” till ”New-AzRoleAssignment”</span><span class="sxs-lookup"><span data-stu-id="08996-419">Added properties 'Condition', 'ConditionVersion' and 'Description' to 'New-AzRoleAssignment'</span></span>
    - <span data-ttu-id="08996-420">Detta omfattade alla relevanta ändringar av datamodellerna</span><span class="sxs-lookup"><span data-stu-id="08996-420">This included all the relevant changes to the data models</span></span>

#### <a name="azsql"></a><span data-ttu-id="08996-421">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08996-421">Az.Sql</span></span>
* <span data-ttu-id="08996-422">Korrigerade ett potentiellt fel med skiftlägesokänsliga servernamn i ”New-AzSqlServer” och ”Set-AzSqlServer”</span><span class="sxs-lookup"><span data-stu-id="08996-422">Fixed potential server name case insensitive error in 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="08996-423">Korrigerade att fel databasnamn returnerades vid ett befintligt databasfel i ”New-AzSqlDatabaseSecondary”</span><span class="sxs-lookup"><span data-stu-id="08996-423">Fixed wrong database name returned on existing database error in 'New-AzSqlDatabaseSecondary'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="08996-424">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="08996-424">Az.Storage</span></span>
* <span data-ttu-id="08996-425">Stöd för att skapa container/blob för SAS-token med de nya behörigheterna x, t</span><span class="sxs-lookup"><span data-stu-id="08996-425">Supported create container/blob Sas token with new permission x,t</span></span>
    -  <span data-ttu-id="08996-426">”New-AzStorageBlobSASToken”</span><span class="sxs-lookup"><span data-stu-id="08996-426">'New-AzStorageBlobSASToken'</span></span>
    -  <span data-ttu-id="08996-427">”New-AzStorageContainerSASToken”</span><span class="sxs-lookup"><span data-stu-id="08996-427">'New-AzStorageContainerSASToken'</span></span>
* <span data-ttu-id="08996-428">Stöd för att skapa konto för SAS-token med de nya behörigheterna x, t, f</span><span class="sxs-lookup"><span data-stu-id="08996-428">Supported create account Sas token with new permission x,t,f</span></span>
    -  <span data-ttu-id="08996-429">”New-AzStorageAccountSASToken”</span><span class="sxs-lookup"><span data-stu-id="08996-429">'New-AzStorageAccountSASToken'</span></span>
* <span data-ttu-id="08996-430">Stöd för att hämta förbrukning av enskild filresurs</span><span class="sxs-lookup"><span data-stu-id="08996-430">Supported get single file share usage</span></span>
    - <span data-ttu-id="08996-431">”Get-AzRmStorageShare”</span><span class="sxs-lookup"><span data-stu-id="08996-431">'Get-AzRmStorageShare'</span></span>

## <a name="440---july-2020"></a><span data-ttu-id="08996-432">4.4.0 – juli 2020</span><span class="sxs-lookup"><span data-stu-id="08996-432">4.4.0 - July 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="08996-433">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="08996-433">Az.Accounts</span></span>
* <span data-ttu-id="08996-434">En ny cmdlet, ”Invoke-AzRestMethod”, har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-434">Added new cmdlet 'Invoke-AzRestMethod'</span></span>
* <span data-ttu-id="08996-435">Ett problem åtgärdades som kan orsaka autentiseringsfel i scenarier med fler processer, t.ex. när flera Azure PowerShell-cmdletar körs med ”Start-Job” [#9448]</span><span class="sxs-lookup"><span data-stu-id="08996-435">Fixed an issue that may cause authentication errors in multi-process scenarios such as running multiple Azure PowerShell cmdlets using 'Start-Job' [#9448]</span></span>

#### <a name="azaks"></a><span data-ttu-id="08996-436">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="08996-436">Az.Aks</span></span>
* <span data-ttu-id="08996-437">Felet som gjorde att ”Get-AzAks” inte hämtade alla kluster har åtgärdats [#12296]</span><span class="sxs-lookup"><span data-stu-id="08996-437">Fixed bug 'Get-AzAks' doesn't get all clusters [#12296]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="08996-438">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="08996-438">Az.AnalysisServices</span></span>
* <span data-ttu-id="08996-439">Projektreferensen till autentisering har tagits bort</span><span class="sxs-lookup"><span data-stu-id="08996-439">Removed project reference to Authentication</span></span>

#### <a name="azautomation"></a><span data-ttu-id="08996-440">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="08996-440">Az.Automation</span></span>
* <span data-ttu-id="08996-441">Problemet som gjorde att strängar med escape-tecken inte kunde konverteras till JSON-objekt har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="08996-441">Fixed the issue that string with escape chars cannot be converted into json object.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08996-442">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08996-442">Az.Compute</span></span>
* <span data-ttu-id="08996-443">En varning har lats till som visas när ”New-AzVmss” används utan den senaste avbildningsversionen</span><span class="sxs-lookup"><span data-stu-id="08996-443">Added warning when using 'New-AzVmss' without 'latest' image version</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="08996-444">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="08996-444">Az.DataFactory</span></span>
* <span data-ttu-id="08996-445">Globala parametrar har lagts till för Data Factory.</span><span class="sxs-lookup"><span data-stu-id="08996-445">Added global parameters to Data Factory.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="08996-446">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="08996-446">Az.EventGrid</span></span>
* <span data-ttu-id="08996-447">Modulen har uppdaterats så att API-version 2020-06-01 används.</span><span class="sxs-lookup"><span data-stu-id="08996-447">Updated to use the 2020-06-01 API version.</span></span>
* <span data-ttu-id="08996-448">Nya funktioner har lagts till:</span><span class="sxs-lookup"><span data-stu-id="08996-448">Added new features:</span></span>
    - <span data-ttu-id="08996-449">Indatamappning</span><span class="sxs-lookup"><span data-stu-id="08996-449">Input mapping</span></span>
    - <span data-ttu-id="08996-450">Schema för händelseleverans</span><span class="sxs-lookup"><span data-stu-id="08996-450">Event Delivery Schema</span></span>
    - <span data-ttu-id="08996-451">Private Link</span><span class="sxs-lookup"><span data-stu-id="08996-451">Private Link</span></span>
    - <span data-ttu-id="08996-452">Cloud Event V10 Schema</span><span class="sxs-lookup"><span data-stu-id="08996-452">Cloud Event V10 Schema</span></span>
    - <span data-ttu-id="08996-453">Service Bus-ämne som mål</span><span class="sxs-lookup"><span data-stu-id="08996-453">Service Bus Topic As Destination</span></span>
    - <span data-ttu-id="08996-454">Azure-funktion som mål</span><span class="sxs-lookup"><span data-stu-id="08996-454">Azure Function As Destination</span></span>
    - <span data-ttu-id="08996-455">Webhook-batchbearbetning</span><span class="sxs-lookup"><span data-stu-id="08996-455">WebHook Batching</span></span>
    - <span data-ttu-id="08996-456">Säker webhook (AAD-stöd)</span><span class="sxs-lookup"><span data-stu-id="08996-456">Secure webhook (AAD support)</span></span>
    - <span data-ttu-id="08996-457">IpFiltering</span><span class="sxs-lookup"><span data-stu-id="08996-457">IpFiltering</span></span>
* <span data-ttu-id="08996-458">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="08996-458">Updated cmdlets:</span></span>
    - <span data-ttu-id="08996-459">”New-AzEventGridSubscription”/”Update-AzEventGridSubscription”:</span><span class="sxs-lookup"><span data-stu-id="08996-459">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span></span>
        - <span data-ttu-id="08996-460">Lägg till nya valfria parametrar för att ge stöd för webhook-batchbearbetning.</span><span class="sxs-lookup"><span data-stu-id="08996-460">Add new optional parameters to support webhook batching.</span></span>
        - <span data-ttu-id="08996-461">Lägg till nya valfria parametrar för att ge stöd för skyddad webhook med AAD.</span><span class="sxs-lookup"><span data-stu-id="08996-461">Add new optional parameters to support secured webhook using AAD.</span></span>
        - <span data-ttu-id="08996-462">Lägg till ny enum (uppräkning) för EndpointType-parametern för att ge stöd för Azure-funktion och Service Bus-ämne som nya mål.</span><span class="sxs-lookup"><span data-stu-id="08996-462">Add new enum for EndpointType parameter to support azure function and service bus topic as new destinations.</span></span>
        - <span data-ttu-id="08996-463">Lägg till ny valfri parameter för leveransschema.</span><span class="sxs-lookup"><span data-stu-id="08996-463">Add new optional parameter for delivery schema.</span></span>
    - <span data-ttu-id="08996-464">”New-AzEventGridTopic”/”Update-AzEventGridTopic” och ”New-AzEventGridDomain”/”Update-AzEventGridDomain”:</span><span class="sxs-lookup"><span data-stu-id="08996-464">'New-AzEventGridTopic'/'Update-AzEventGridTopic' and 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span></span>
        - <span data-ttu-id="08996-465">Lägg till nya valfria parametrar för att ge stöd för IpFiltering.</span><span class="sxs-lookup"><span data-stu-id="08996-465">Add new optional parameters to support IpFiltering.</span></span>
    - <span data-ttu-id="08996-466">”New-AzEventGridTopic”/”New-AzEventGridDomain”:</span><span class="sxs-lookup"><span data-stu-id="08996-466">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span></span>
        - <span data-ttu-id="08996-467">Lägg till nya valfria parametrar för att ge stöd för indatamappning.</span><span class="sxs-lookup"><span data-stu-id="08996-467">Add new optional parameters to support Input mapping.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="08996-468">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="08996-468">Az.FrontDoor</span></span>
* <span data-ttu-id="08996-469">Modulen har uppdaterats så att API 2020-05-01 används</span><span class="sxs-lookup"><span data-stu-id="08996-469">Updated module to use API 2020-05-01</span></span>
* <span data-ttu-id="08996-470">Stöd för privat länk har lagts till för Storage-, KeyVault- och Web App Service-resurser</span><span class="sxs-lookup"><span data-stu-id="08996-470">Added Private link support for Storage, Keyvault and Web App Service resources</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="08996-471">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="08996-471">Az.HDInsight</span></span>
* <span data-ttu-id="08996-472">Stöd för att skapa kluster med ADLSGen1/2-lagring i nationella moln.</span><span class="sxs-lookup"><span data-stu-id="08996-472">Supported creating cluster with ADLSGen1/2 storage in national clouds.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="08996-473">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="08996-473">Az.Monitor</span></span>
* <span data-ttu-id="08996-474">Bugg som orsakade fel med ”Get-AzDiagnosticSetting” när mått eller loggar var null har åtgärdats [#12272]</span><span class="sxs-lookup"><span data-stu-id="08996-474">Fixed bug for 'Get-AzDiagnosticSetting' when metrics or logs are null [#12272]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="08996-475">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08996-475">Az.Network</span></span>
* <span data-ttu-id="08996-476">Parameterväxlingen i VWan HubVnet-anslutningar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="08996-476">Fixed parameters swap in VWan HubVnet connection</span></span>
* <span data-ttu-id="08996-477">Nya cmdletar har lagts till för platser för virtuella installationer i Azure-nätverk</span><span class="sxs-lookup"><span data-stu-id="08996-477">Added new cmdlets for Azure Network Virtual Appliance Sites</span></span>
    - <span data-ttu-id="08996-478">”Get-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="08996-478">'Get-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="08996-479">”New-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="08996-479">'New-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="08996-480">”Remove-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="08996-480">'Remove-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="08996-481">”Update-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="08996-481">'Update-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="08996-482">”New-AzOffice365PolicyProperty”</span><span class="sxs-lookup"><span data-stu-id="08996-482">'New-AzOffice365PolicyProperty'</span></span>
* <span data-ttu-id="08996-483">Nya cmdletar har lagts till för virtuella installationer i Azure-nätverk</span><span class="sxs-lookup"><span data-stu-id="08996-483">Added new cmdlets for Azure Network Virtual Appliance</span></span>
    - <span data-ttu-id="08996-484">”Get-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="08996-484">'Get-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="08996-485">”New-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="08996-485">'New-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="08996-486">”Remove-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="08996-486">'Remove-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="08996-487">”Update-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="08996-487">'Update-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="08996-488">”Get-AzNetworkVirtualApplianceSku”</span><span class="sxs-lookup"><span data-stu-id="08996-488">'Get-AzNetworkVirtualApplianceSku'</span></span>
    - <span data-ttu-id="08996-489">”New-AzVirtualApplianceSkuProperty”</span><span class="sxs-lookup"><span data-stu-id="08996-489">'New-AzVirtualApplianceSkuProperty'</span></span>
* <span data-ttu-id="08996-490">Application Gateway har introducerats i vanliga cmdletar för Private Link</span><span class="sxs-lookup"><span data-stu-id="08996-490">Onboarded Application Gateway to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="08996-491">StorageSync har introducerats i vanliga cmdletar för Private Link</span><span class="sxs-lookup"><span data-stu-id="08996-491">Onboarded StorageSync to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="08996-492">SignalR har introducerats i vanliga cmdletar för Private Link</span><span class="sxs-lookup"><span data-stu-id="08996-492">Onboarded SignalR to Private Link Common Cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="08996-493">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="08996-493">Az.RecoveryServices</span></span>
* <span data-ttu-id="08996-494">Projektreferensen till autentisering har tagits bort</span><span class="sxs-lookup"><span data-stu-id="08996-494">Removed project reference to Authentication</span></span>
* <span data-ttu-id="08996-495">Azure Backup-anpassade cmdletar gör text mer korrekt.</span><span class="sxs-lookup"><span data-stu-id="08996-495">Azure Backup tuned cmdlets help text to be more accurate.</span></span>
* <span data-ttu-id="08996-496">Stöd har lagts till som gör att Azure Backup kan hämta MAB-agentjobb med cmdleten ”Get-AzRecoveryServicesBackupJob”.</span><span class="sxs-lookup"><span data-stu-id="08996-496">Azure Backup added support for fetching MAB agent jobs using 'Get-AzRecoveryServicesBackupJob' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="08996-497">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08996-497">Az.Resources</span></span>
* <span data-ttu-id="08996-498">”Save-AzResourceGroupDeploymentTemplate” har uppdaterats för att använda SDK:n.</span><span class="sxs-lookup"><span data-stu-id="08996-498">Updated 'Save-AzResourceGroupDeploymentTemplate' to use the SDK.</span></span>
* <span data-ttu-id="08996-499">Cmdleten ”Unregister-AzResourceProvider” har lagts till.</span><span class="sxs-lookup"><span data-stu-id="08996-499">Added 'Unregister-AzResourceProvider' cmdlet.</span></span>

#### <a name="azsql"></a><span data-ttu-id="08996-500">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08996-500">Az.Sql</span></span>
* <span data-ttu-id="08996-501">Stöd har lagts till för SPN och gästanvändare i cmdleten ”Set-AzSqlInstanceActiveDirectoryAdministrator”</span><span class="sxs-lookup"><span data-stu-id="08996-501">Added support for Service principal and guest users in Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet'</span></span>
* <span data-ttu-id="08996-502">En bugg har åtgärdats i cmdletar för dataklassificering.</span><span class="sxs-lookup"><span data-stu-id="08996-502">Fixed a bug in Data Classification cmdlets.'</span></span>
* <span data-ttu-id="08996-503">Stöd har lagts till för redundansväxling med Azure SQL Managed Instance: ”Invoke-AzSqlInstanceFailover”</span><span class="sxs-lookup"><span data-stu-id="08996-503">Added support for Azure SQL Managed Instance failover: 'Invoke-AzSqlInstanceFailover'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="08996-504">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="08996-504">Az.Storage</span></span>
* <span data-ttu-id="08996-505">Problemet som gjorde att UserAgent inte lades till för vissa cmdletar för dataplanet har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="08996-505">Fixed the issue that UserAgent is not added for some data plane cmdlets.</span></span>
* <span data-ttu-id="08996-506">Stöd har lagts till för att skapa/uppdatera Storage-konto med MinimumTlsVersion och AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="08996-506">Supported create/update Storage account with MinimumTlsVersion and AllowBlobPublicAccess</span></span>
    -  <span data-ttu-id="08996-507">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="08996-507">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="08996-508">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="08996-508">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="08996-509">Stöd har lagts till för att aktivera/inaktivera versionshantering i Blob Service för ett Storage-konto</span><span class="sxs-lookup"><span data-stu-id="08996-509">Support enable/disable versioning on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="08996-510">”Update-AzStorageBlobServiceProperty”</span><span class="sxs-lookup"><span data-stu-id="08996-510">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="08996-511">Stöd har lagts till för att visa blobar med blobversioner</span><span class="sxs-lookup"><span data-stu-id="08996-511">Support list blobs with blob versions</span></span>
    - <span data-ttu-id="08996-512">”Get-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="08996-512">'Get-AzStorageBlob'</span></span>
* <span data-ttu-id="08996-513">Stöd har lagts till för att hämta/ta bort enskilda ögonblicksbilder av blobar eller blobversioner</span><span class="sxs-lookup"><span data-stu-id="08996-513">Support get/remove single blob snapshot or blob version</span></span>
    - <span data-ttu-id="08996-514">”Get-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="08996-514">'Get-AzStorageBlob'</span></span>
    - <span data-ttu-id="08996-515">”Remove-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="08996-515">'Remove-AzStorageBlob'</span></span>
* <span data-ttu-id="08996-516">Stöd har lagts till för pipelines från blobobjekt genererade av Azure.Storage.Blobs V12</span><span class="sxs-lookup"><span data-stu-id="08996-516">Support pipeline from blob object generated from Azure.Storage.Blobs V12</span></span>
    - <span data-ttu-id="08996-517">”Get-AzStorageBlobContent”</span><span class="sxs-lookup"><span data-stu-id="08996-517">'Get-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="08996-518">”New-AzStorageBlobSASToken”</span><span class="sxs-lookup"><span data-stu-id="08996-518">'New-AzStorageBlobSASToken'</span></span>
    - <span data-ttu-id="08996-519">”Remove-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="08996-519">'Remove-AzStorageBlob'</span></span>
    - <span data-ttu-id="08996-520">”Set-AzStorageBlobContent”</span><span class="sxs-lookup"><span data-stu-id="08996-520">'Set-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="08996-521">”Start-AzStorageBlobCopy”</span><span class="sxs-lookup"><span data-stu-id="08996-521">'Start-AzStorageBlobCopy'</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="08996-522">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="08996-522">Az.StorageSync</span></span>
* <span data-ttu-id="08996-523">En ny version har lagts till för StorageSync SDK som körs mot ApiVersion 2020-03-01</span><span class="sxs-lookup"><span data-stu-id="08996-523">Added a new version StorageSync SDK targeting ApiVersion 2020-03-01</span></span>
* <span data-ttu-id="08996-524">En cmdlet för synkroniseringstjänsten för lagringsuppdatering har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-524">Added Update Storage Sync Service cmdlet</span></span>
    - <span data-ttu-id="08996-525">”Set-AzStorageSyncService”</span><span class="sxs-lookup"><span data-stu-id="08996-525">'Set-AzStorageSyncService'</span></span>
* <span data-ttu-id="08996-526">IncomingTrafficPolicy och PrivateEndpointConnections har lagts till för StorageSyncService-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="08996-526">Added IncomingTrafficPolicy and PrivateEndpointConnections to StorageSyncService cmdlets.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="08996-527">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="08996-527">Az.Websites</span></span>
* <span data-ttu-id="08996-528">Stöd har lagts till för att utföra åtgärder för platser som inte tillhör samma resursgrupp som App Services-planen</span><span class="sxs-lookup"><span data-stu-id="08996-528">Added support to perform operations for Slots not in the same resource group as the App Service Plan</span></span>

## <a name="430---june-2020"></a><span data-ttu-id="08996-529">4.3.0 – juni 2020</span><span class="sxs-lookup"><span data-stu-id="08996-529">4.3.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="08996-530">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="08996-530">Az.Accounts</span></span>
* <span data-ttu-id="08996-531">Stöd för identifiering av miljöinställning som standard och tillägg av miljön via ”Add-AzEnvironment”</span><span class="sxs-lookup"><span data-stu-id="08996-531">Supported discovering environment setting by default and adding environment via 'Add-AzEnvironment'</span></span>
* <span data-ttu-id="08996-532">Uppdatera förinlästa sammansättningar [#12024], [#11976]</span><span class="sxs-lookup"><span data-stu-id="08996-532">Update preloaded assemblies [#12024], [#11976]</span></span>
* <span data-ttu-id="08996-533">Uppdaterad Azure.Core-sammansättning</span><span class="sxs-lookup"><span data-stu-id="08996-533">Updated Azure.Core assembly</span></span>
* <span data-ttu-id="08996-534">Ett problem har åtgärdats som kan orsaka att ”Connect-AzAccount” misslyckas vid körning av flera trådar [#11201]</span><span class="sxs-lookup"><span data-stu-id="08996-534">Fixed an issue that may cause 'Connect-AzAccount' to fail in multi-threaded execution [#11201]</span></span>

#### <a name="azaks"></a><span data-ttu-id="08996-535">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="08996-535">Az.Aks</span></span>
* <span data-ttu-id="08996-536">Användning av gamla [AccessProfile API](/rest/api/aks/managedclusters/getaccessprofile) ersattes med anrop till API:erna [ListClusterAdmin](/rest/api/aks/managedclusters/listclusteradmincredentials) och [ListClusterUser](/rest/api/aks/managedclusters/listclusterusercredentials)</span><span class="sxs-lookup"><span data-stu-id="08996-536">Replaced usage of old [AccessProfile API](/rest/api/aks/managedclusters/getaccessprofile) with calls to [ListClusterAdmin](/rest/api/aks/managedclusters/listclusteradmincredentials) and [ListClusterUser](/rest/api/aks/managedclusters/listclusterusercredentials) APIs</span></span>

#### <a name="azbatch"></a><span data-ttu-id="08996-537">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="08996-537">Az.Batch</span></span>
* <span data-ttu-id="08996-538">Az.Batch har uppdaterats att använda ”Microsoft.Azure.Management.Batch” SDK till och med version 11.0.0.</span><span class="sxs-lookup"><span data-stu-id="08996-538">Updated Az.Batch to use 'Microsoft.Azure.Management.Batch' SDK version to 11.0.0</span></span>
* <span data-ttu-id="08996-539">Möjligheten att ange BatchAccount-identiteten har lagts till i cmdleten ”New-AzBatchAccount”</span><span class="sxs-lookup"><span data-stu-id="08996-539">Added the ability to set the BatchAccount Identity in the 'New-AzBatchAccount' cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="08996-540">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="08996-540">Az.CognitiveServices</span></span>
* <span data-ttu-id="08996-541">Stöd för att visa kontofunktioner.</span><span class="sxs-lookup"><span data-stu-id="08996-541">Supported displaying account capabilities.</span></span>
* <span data-ttu-id="08996-542">Stöd för att ändra PublicNetworkAccess.</span><span class="sxs-lookup"><span data-stu-id="08996-542">Supported modifying PublicNetworkAccess.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08996-543">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08996-543">Az.Compute</span></span>
* <span data-ttu-id="08996-544">Parametern SimulateEviction har lagts till i cmdletarna set-AzVM och set-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="08996-544">Added SimulateEviction parameter to Set-AzVM and Set-AzVmssVM cmdlets.</span></span>
* <span data-ttu-id="08996-545">”Premium_LRS” har lagts till i argumentslutföraren för parametern StorageAccountType för cmdleten New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="08996-545">Added 'Premium_LRS' to the argument completer of StorageAccountType parameter for New-AzGalleryImageVersion cmdlet.</span></span>
* <span data-ttu-id="08996-546">Understatusar har lagts till i VMCustomScriptExtension [#11297]</span><span class="sxs-lookup"><span data-stu-id="08996-546">Added Substatuses to VMCustomScriptExtension [#11297]</span></span>
* <span data-ttu-id="08996-547">”Delete” har lagts till i argumentslutföraren för parametern EvictionPolicy för cmdletarna New-AzVM och New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="08996-547">Added 'Delete' to the argument completer of EvictionPolicy parameter for New-AzVM and New-AzVMConfig cmdlets.</span></span>
* <span data-ttu-id="08996-548">Åtgärdat namn för nytt VM-tillägg för SAP</span><span class="sxs-lookup"><span data-stu-id="08996-548">Fixed name of new VM Extension for SAP</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="08996-549">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="08996-549">Az.DataFactory</span></span>
* <span data-ttu-id="08996-550">ADF .Net SDK har uppdaterats till 4.9.0</span><span class="sxs-lookup"><span data-stu-id="08996-550">Updated ADF .Net SDK version to 4.9.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="08996-551">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="08996-551">Az.EventHub</span></span>
* <span data-ttu-id="08996-552">Parametrar för hanterad identitet har lagts till i cmdletarna ”New-AzEventHubNamespace” och ”set-AzEventHubNamespace”</span><span class="sxs-lookup"><span data-stu-id="08996-552">Added Managed Identity parameters to 'New-AzEventHubNamespace' and 'Set-AzEventHubNamespace' cmdlets</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="08996-553">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="08996-553">Az.Functions</span></span>
* <span data-ttu-id="08996-554">Stöd har lagts till för att skapa PowerShell 7.0- och Java 11-funktionsappar</span><span class="sxs-lookup"><span data-stu-id="08996-554">Added support to create PowerShell 7.0 and Java 11 function apps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="08996-555">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="08996-555">Az.HDInsight</span></span>
* <span data-ttu-id="08996-556">Stöd för listning av värdar och omstart för specifika värdar i HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="08996-556">Supported listing hosts and restart specific hosts of the HDInsight cluster.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="08996-557">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="08996-557">Az.HealthcareApis</span></span>
* <span data-ttu-id="08996-558">Uppdaterade SDK-versionen till 1.1.0</span><span class="sxs-lookup"><span data-stu-id="08996-558">Updated the SDK version to 1.1.0</span></span>
* <span data-ttu-id="08996-559">Stöd har lagts till för exportinställningar och hanterad identitet</span><span class="sxs-lookup"><span data-stu-id="08996-559">Added support for Export settings and Managed Identity</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="08996-560">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="08996-560">Az.Monitor</span></span>
* <span data-ttu-id="08996-561">Parameter för inmatningsobjekt har åtgärdats för ”Set-AzActivityLogAlert”</span><span class="sxs-lookup"><span data-stu-id="08996-561">Fixed input object parameter for 'Set-AzActivityLogAlert'</span></span>
* <span data-ttu-id="08996-562">Parametern ”InputObject” har åtgärdats för ”Set-AzActionGroup” [#10868]</span><span class="sxs-lookup"><span data-stu-id="08996-562">Fixed 'InputObject' parameter for 'Set-AzActionGroup' [#10868]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="08996-563">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08996-563">Az.Network</span></span>
* <span data-ttu-id="08996-564">Stöd har lagts till för parametern AddressPrefixType i ”Remove-AzExpressRouteCircuitConnectionConfig”</span><span class="sxs-lookup"><span data-stu-id="08996-564">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="08996-565">Nya cmdletar har lagts till för Azure FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="08996-565">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="08996-566">”New-AzFirewallPolicyDnsSetting”</span><span class="sxs-lookup"><span data-stu-id="08996-566">'New-AzFirewallPolicyDnsSetting'</span></span>
    - <span data-ttu-id="08996-567">Stöd för mål-FQDN i nätverksregler för brandväggsprincip</span><span class="sxs-lookup"><span data-stu-id="08996-567">Support for Destination FQDN in Network Rules for Firewall Policy</span></span>
* <span data-ttu-id="08996-568">Stöd har lagts till för åtgärder i serverdelsadresspooler</span><span class="sxs-lookup"><span data-stu-id="08996-568">Added support for backend address pool operations</span></span>
    - <span data-ttu-id="08996-569">”New-AzLoadBalancerBackendAddressConfig”</span><span class="sxs-lookup"><span data-stu-id="08996-569">'New-AzLoadBalancerBackendAddressConfig'</span></span>
    - <span data-ttu-id="08996-570">”New-AzLoadBalancerBackendAddressPool”</span><span class="sxs-lookup"><span data-stu-id="08996-570">'New-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="08996-571">”Set-AzLoadBalancerBackendAddressPool”</span><span class="sxs-lookup"><span data-stu-id="08996-571">'Set-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="08996-572">”Remove-AzLoadBalancerBackendAddressPool”</span><span class="sxs-lookup"><span data-stu-id="08996-572">'Remove-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="08996-573">”Get-AzLoadBalancerBackendAddressPool”</span><span class="sxs-lookup"><span data-stu-id="08996-573">'Get-AzLoadBalancerBackendAddressPool'</span></span>
* <span data-ttu-id="08996-574">Namnvalidering har lagts till för ”New-AzIpGroup”</span><span class="sxs-lookup"><span data-stu-id="08996-574">Added name validation for 'New-AzIpGroup'</span></span>
* <span data-ttu-id="08996-575">Nya cmdletar har lagts till för Azure FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="08996-575">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="08996-576">”New-AzFirewallPolicyThreatIntelWhitelist”</span><span class="sxs-lookup"><span data-stu-id="08996-576">'New-AzFirewallPolicyThreatIntelWhitelist'</span></span>
* <span data-ttu-id="08996-577">Nedanstående kommandon för funktionen har uppdaterats: Konfiguration/borttagning av anpassade DNS-servrar på VirtualWan P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="08996-577">Updated below commands for feature: Custom dns servers set/remove on VirtualWan P2SVpnGateway.</span></span>
    - <span data-ttu-id="08996-578">New-AzP2sVpnGateway har uppdaterats: Den valfria parametern ”-CustomDnsServer” har lagts till för att kunder ska kunna ange att deras DNS-servrar ska konfigureras på P2SVpnGateway, som kan användas av punkt-till-plats-klienter.</span><span class="sxs-lookup"><span data-stu-id="08996-578">Updated New-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
    - <span data-ttu-id="08996-579">Update-AzP2sVpnGateway har uppdaterats: Den valfria parametern ”-CustomDnsServer” har lagts till för att kunder ska kunna ange att deras DNS-servrar ska konfigureras på P2SVpnGateway, som kan användas av punkt-till-plats-klienter.</span><span class="sxs-lookup"><span data-stu-id="08996-579">Updated Update-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
* <span data-ttu-id="08996-580">”Update-AzVpnGateway” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="08996-580">Updated 'Update-AzVpnGateway'</span></span>
    - <span data-ttu-id="08996-581">Den valfria parametern ”-BgpPeeringAddress” har lagts till för att kunder ska kunna ange sina anpassade BGP:er som ska konfigurerar på VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="08996-581">Added optional parameter '-BgpPeeringAddress' for customers to specify their custom bgps to set on VpnGateway.</span></span>
* <span data-ttu-id="08996-582">Ny cmdlet har lagts till för att stödja återställning av en VirtualHub-resurs routningsstatus:</span><span class="sxs-lookup"><span data-stu-id="08996-582">Added new cmdlet to support resetting the routing state of a VirtualHub resource:</span></span>
    - <span data-ttu-id="08996-583">”Reset-AzHubRouter”</span><span class="sxs-lookup"><span data-stu-id="08996-583">'Reset-AzHubRouter'</span></span>
* <span data-ttu-id="08996-584">Nedanstående saker har uppdaterats baserat på den senaste Swagger-ändringen för brandväggspolicyn</span><span class="sxs-lookup"><span data-stu-id="08996-584">Updated below things based on recent swagger change for Firewall Policy</span></span>
    - <span data-ttu-id="08996-585">Namn ändras för RuleGroup, RuleCollectionGroup och RuleType</span><span class="sxs-lookup"><span data-stu-id="08996-585">Changes names for RuleGroup, RuleCollectionGroup and RuleType</span></span>
    - <span data-ttu-id="08996-586">Stöd har lagts till för NAT-regelsamlingar för brandväggsprincip så att flera NAT-regelsamlingar stöds</span><span class="sxs-lookup"><span data-stu-id="08996-586">Added support for Firewall Policy NAT Rule Collections to support multiple NAT Rule Collection</span></span>
* <span data-ttu-id="08996-587">[Icke-bakåtkompatibel ändring] Den obligatoriska parametern ”SourceIpGroup” har lagts till för ”New-AzFirewallPolicyApplicationRule” och ”New-AzFirewallPolicyNetworkRule”.</span><span class="sxs-lookup"><span data-stu-id="08996-587">[Breaking Change] Added mandatory parameter 'SourceIpGroup' for 'New-AzFirewallPolicyApplicationRule' and 'New-AzFirewallPolicyNetworkRule'.</span></span>
* <span data-ttu-id="08996-588">[Icke-bakåtkompatibel ändring] ”New-AzFirewallPolicyApplicationRule” har åtgärdats, parametern ”SourceAddress” är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="08996-588">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="08996-589">[Icke-bakåtkompatibel ändring] ”New-AzFirewallPolicyApplicationRule” har åtgärdats, parametern ”SourceAddress” är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="08996-589">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="08996-590">[Icke-bakåtkompatibel ändring] Obligatoriska parametrar har tagits bort: ”TranslatedAddress”, ”TranslatedPort” för ”New-AzFirewallPolicyNatRuleCollection”.</span><span class="sxs-lookup"><span data-stu-id="08996-590">[Breaking Change] Removed mandatory parameters: 'TranslatedAddress', 'TranslatedPort' for 'New-AzFirewallPolicyNatRuleCollection'.</span></span>
* <span data-ttu-id="08996-591">Nya cmdletar har lagts till för att stödja PrivateLink på Application Gateway</span><span class="sxs-lookup"><span data-stu-id="08996-591">Added new cmdlets to support PrivateLink On Application Gateway</span></span>
    - <span data-ttu-id="08996-592">”New-AzApplicationGatewayPrivateLinkConfiguration”</span><span class="sxs-lookup"><span data-stu-id="08996-592">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="08996-593">”Get-AzApplicationGatewayPrivateLinkConfiguration”</span><span class="sxs-lookup"><span data-stu-id="08996-593">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="08996-594">”New-AzApplicationGatewayPrivateLinkConfiguration”</span><span class="sxs-lookup"><span data-stu-id="08996-594">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="08996-595">”Set-AzApplicationGatewayPrivateLinkConfiguration”</span><span class="sxs-lookup"><span data-stu-id="08996-595">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="08996-596">”Remove-AzApplicationGatewayPrivateLinkConfiguration”</span><span class="sxs-lookup"><span data-stu-id="08996-596">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="08996-597">”New-AzApplicationGatewayPrivateLinkIpConfiguration”</span><span class="sxs-lookup"><span data-stu-id="08996-597">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span></span>
* <span data-ttu-id="08996-598">Nya cmdletar har lagts till för VirtualHubs underordnade resurs HubRouteTables.</span><span class="sxs-lookup"><span data-stu-id="08996-598">Added new cmdlets for HubRouteTables child resource of VirtualHub.</span></span>
    - <span data-ttu-id="08996-599">”New-AzVHubRoute”</span><span class="sxs-lookup"><span data-stu-id="08996-599">'New-AzVHubRoute'</span></span>
    - <span data-ttu-id="08996-600">”New-AzVHubRouteTable”</span><span class="sxs-lookup"><span data-stu-id="08996-600">'New-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="08996-601">”Get-AzVHubRouteTable”</span><span class="sxs-lookup"><span data-stu-id="08996-601">'Get-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="08996-602">”Update-AzVHubRouteTable”</span><span class="sxs-lookup"><span data-stu-id="08996-602">'Update-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="08996-603">”Remove-AzVHubRouteTable”</span><span class="sxs-lookup"><span data-stu-id="08996-603">'Remove-AzVHubRouteTable'</span></span>
* <span data-ttu-id="08996-604">Befintliga cmdletar har uppdaterats för att stödja valfri RoutingConfiguration-indataparameter för anpassad routning i VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="08996-604">Updated existing cmdlets to support optional RoutingConfiguration input parameter for custom routing in VirtualWan.</span></span>
    - <span data-ttu-id="08996-605">”New-AzExpressRouteConnection”</span><span class="sxs-lookup"><span data-stu-id="08996-605">'New-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="08996-606">”Set-AzExpressRouteConnection”</span><span class="sxs-lookup"><span data-stu-id="08996-606">'Set-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="08996-607">”New-AzVirtualHubVnetConnection”</span><span class="sxs-lookup"><span data-stu-id="08996-607">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="08996-608">”Update-AzVirtualHubVnetConnection”</span><span class="sxs-lookup"><span data-stu-id="08996-608">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="08996-609">”New-AzVpnConnection”</span><span class="sxs-lookup"><span data-stu-id="08996-609">'New-AzVpnConnection'</span></span>
    - <span data-ttu-id="08996-610">”Update-AzVpnConnection”</span><span class="sxs-lookup"><span data-stu-id="08996-610">'Update-AzVpnConnection'</span></span>
    - <span data-ttu-id="08996-611">”New-AzP2sVpnGateway”</span><span class="sxs-lookup"><span data-stu-id="08996-611">'New-AzP2sVpnGateway'</span></span>
    - <span data-ttu-id="08996-612">”Update-AzP2sVpnGateway”</span><span class="sxs-lookup"><span data-stu-id="08996-612">'Update-AzP2sVpnGateway'</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="08996-613">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="08996-613">Az.OperationalInsights</span></span>
* <span data-ttu-id="08996-614">Fast fel PSWorkspace implementerar inte IOperationalInsightsWorkspace [#12135]</span><span class="sxs-lookup"><span data-stu-id="08996-614">Fixed bug PSWorkspace doesn't implement IOperationalInsightsWorkspace [#12135]</span></span>
* <span data-ttu-id="08996-615">”pergb2018” har lagts till i uppsättningen med giltiga värden för parametern ”Sku” i ”Set-AzOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="08996-615">Added 'pergb2018' to valid value set of parameter 'Sku' in 'Set-AzOperationalInsightsWorkspace'</span></span> 
* <span data-ttu-id="08996-616">Alias ”FunctionParameters” lades till för parametern ”FunctionParameter” till</span><span class="sxs-lookup"><span data-stu-id="08996-616">Added alias 'FunctionParameters' for parameter 'FunctionParameter' to</span></span>
    - <span data-ttu-id="08996-617">”New-AzOperationalInsightsSavedSearch”</span><span class="sxs-lookup"><span data-stu-id="08996-617">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="08996-618">”Set-AzOperationalInsightsSavedSearch”</span><span class="sxs-lookup"><span data-stu-id="08996-618">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="08996-619">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="08996-619">Az.RecoveryServices</span></span>
* <span data-ttu-id="08996-620">Azure Backup har fått stöd för att hämta MAB-objekt.</span><span class="sxs-lookup"><span data-stu-id="08996-620">Azure Backup added support for fetching MAB items.</span></span>
* <span data-ttu-id="08996-621">Azure Site Recovery stöder disktypen ”StandardSSD_LRS”</span><span class="sxs-lookup"><span data-stu-id="08996-621">Azure Site Recovery supports disk type 'StandardSSD_LRS'</span></span>

#### <a name="azresources"></a><span data-ttu-id="08996-622">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08996-622">Az.Resources</span></span>
* <span data-ttu-id="08996-623">”UsageLocation”, ”GivenName”, ”Surname”, ”AccountEnabled”, ”MailNickname”, ”Mail” på ”PSADUser” lades till [#10526] [#10497]</span><span class="sxs-lookup"><span data-stu-id="08996-623">Added 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' on 'PSADUser' [#10526] [#10497]</span></span>
* <span data-ttu-id="08996-624">Problem med att ”-Mail” inte fungerar på ”Get-AzADUser” har åtgärdats [#11981]</span><span class="sxs-lookup"><span data-stu-id="08996-624">Fixed issue that '-Mail' doesn't work on 'Get-AzADUser' [#11981]</span></span>
* <span data-ttu-id="08996-625">Parametern ”-ExcludeChangeType” har lagts till i ”Get-AzDeploymentWhatIfResult” och ”Get-AzResourceGroupDeploymentWhatIfResult”</span><span class="sxs-lookup"><span data-stu-id="08996-625">Added '-ExcludeChangeType' parameter to 'Get-AzDeploymentWhatIfResult' and 'Get-AzResourceGroupDeploymentWhatIfResult'</span></span>
* <span data-ttu-id="08996-626">Parametern ”-WhatIfExcludeChangeType” har lagts till i ”New-AzDeployment” och ”New-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="08996-626">Added '-WhatIfExcludeChangeType' parameter to 'New-AzDeployment' and 'New-AzResourceGroupDeployment'</span></span>
* <span data-ttu-id="08996-627">Cmdletar för ”Test-Az\*Deployment” har uppdaterats för att visa bättre felmeddelanden</span><span class="sxs-lookup"><span data-stu-id="08996-627">Updated 'Test-Az\*Deployment' cmdlets to show better error messages</span></span>
* <span data-ttu-id="08996-628">Hjälpmeddelandet för parametern ”-Name” i distributionsskapande och What If-cmdletar</span><span class="sxs-lookup"><span data-stu-id="08996-628">Fixed help message for '-Name' parameter of deployment create and What-If cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="08996-629">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08996-629">Az.Sql</span></span>
* <span data-ttu-id="08996-630">Stöd för tjänsthuvudnamn har lagts till för administratörs-cmdlet för SQL Server Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="08996-630">Added support for service principal for Set SQL Server Azure Active Directory Admin cmdlet</span></span>
* <span data-ttu-id="08996-631">Synkroniseringsproblem i Data Classification-cmdletar har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="08996-631">Fixed sync issue in Data Classification cmdlets.</span></span>
* <span data-ttu-id="08996-632">Stöd för att söka efter användare via e-postadress på ”Set-AzSqlServerActiveDirectoryAdministrator” [#12192]</span><span class="sxs-lookup"><span data-stu-id="08996-632">Supported searching user by mail on 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span></span>

#### <a name="azstorage"></a><span data-ttu-id="08996-633">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="08996-633">Az.Storage</span></span>
* <span data-ttu-id="08996-634">Skapa lagringskonto med RequireInfrastructureEncryption stöds</span><span class="sxs-lookup"><span data-stu-id="08996-634">Supported create Storage account with RequireInfrastructureEncryption</span></span>
    -  <span data-ttu-id="08996-635">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="08996-635">'New-AzStorageAccount'</span></span>
* <span data-ttu-id="08996-636">Logiken för inläsning av Azure.Core flyttades till Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="08996-636">Moved the logic of loading Azure.Core to Az.Accounts</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="08996-637">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="08996-637">Az.Websites</span></span>
* <span data-ttu-id="08996-638">Skydd för att ta bort skapad webapp om återställningen misslyckades har lagts till i ”Restore-AzDeletedWebApp”</span><span class="sxs-lookup"><span data-stu-id="08996-638">Added safeguard to delete created webapp if restore failed in 'Restore-AzDeletedWebApp'</span></span>
* <span data-ttu-id="08996-639">”SourceWebApp.Location” har lagts till för ”New-AzWebApp” och ”New-AzWebAppSlot”</span><span class="sxs-lookup"><span data-stu-id="08996-639">Added 'SourceWebApp.Location' for 'New-AzWebApp' and 'New-AzWebAppSlot'</span></span>
* <span data-ttu-id="08996-640">Fel som förhindrade ändring av containerinställningar i ”Set-AzWebApp” och ”Set-AzWebAppSlot” har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="08996-640">Fixed bug that prevented changing Container settings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>
* <span data-ttu-id="08996-641">Ett fel för att hämta SiteConfig när -Name inte anges för Get-AzWebApp har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="08996-641">Fixed bug to get SiteConfig when -Name is not given for Get-AzWebApp</span></span>
* <span data-ttu-id="08996-642">Stöd har lagts till för att skapa ASP för Linux-appar</span><span class="sxs-lookup"><span data-stu-id="08996-642">Added a support to create ASP for Linux Apps</span></span>
* <span data-ttu-id="08996-643">Undantag har lagts till för kloning över resursgrupper</span><span class="sxs-lookup"><span data-stu-id="08996-643">Added exceptions for clone across resource groups</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="08996-644">4.2.0 – juni 2020</span><span class="sxs-lookup"><span data-stu-id="08996-644">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="08996-645">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="08996-645">Az.Accounts</span></span>
* <span data-ttu-id="08996-646">Åtgärdade ett problem som kan få Az att hoppa över loggar i Azure Automation- eller PowerShell-jobb [#11492]</span><span class="sxs-lookup"><span data-stu-id="08996-646">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="08996-647">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="08996-647">Az.AnalysisServices</span></span>
* <span data-ttu-id="08996-648">Uppdaterad sammansättningsversion för dataplan-cmdletar</span><span class="sxs-lookup"><span data-stu-id="08996-648">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="08996-649">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="08996-649">Az.ApiManagement</span></span>
* <span data-ttu-id="08996-650">Uppdaterad sammansättningsversion för cmdletar för tjänsthantering</span><span class="sxs-lookup"><span data-stu-id="08996-650">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="08996-651">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="08996-651">Az.Billing</span></span>
* <span data-ttu-id="08996-652">Uppdaterad sammansättningsversion för förbrukningscmdletar</span><span class="sxs-lookup"><span data-stu-id="08996-652">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="08996-653">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="08996-653">Az.CognitiveServices</span></span>
* <span data-ttu-id="08996-654">Stöd för PrivateEndpoint- och PublicNetworkAccess-kontroll.</span><span class="sxs-lookup"><span data-stu-id="08996-654">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="08996-655">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="08996-655">Az.DataFactory</span></span>
* <span data-ttu-id="08996-656">Uppdaterad sammansättningsversion för datafabrik V2-cmdletar</span><span class="sxs-lookup"><span data-stu-id="08996-656">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="08996-657">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="08996-657">Az.DataShare</span></span>
* <span data-ttu-id="08996-658">Allmän tillgänglighet för modulen ”Az.DataShare”</span><span class="sxs-lookup"><span data-stu-id="08996-658">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="08996-659">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="08996-659">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="08996-660">Allmän tillgänglighet för modulen ”Az.DesktopVirtualization”</span><span class="sxs-lookup"><span data-stu-id="08996-660">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="08996-661">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="08996-661">Az.OperationalInsights</span></span>
* <span data-ttu-id="08996-662">Uppgraderad SDK till 0.21.0</span><span class="sxs-lookup"><span data-stu-id="08996-662">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="08996-663">Lade till valfria parametrar till</span><span class="sxs-lookup"><span data-stu-id="08996-663">Added optional parameters to</span></span> 
    - <span data-ttu-id="08996-664">”New-AzOperationalInsightsSavedSearch”</span><span class="sxs-lookup"><span data-stu-id="08996-664">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="08996-665">”Set-AzOperationalInsightsSavedSearch”</span><span class="sxs-lookup"><span data-stu-id="08996-665">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="08996-666">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="08996-666">Az.PolicyInsights</span></span>
* <span data-ttu-id="08996-667">Korrigerade exempel 3 för ”Start-AzPolicyComplianceScan”</span><span class="sxs-lookup"><span data-stu-id="08996-667">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="08996-668">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="08996-668">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="08996-669">Uppdaterad sammansättningsversion för PowerBI-cmdletar</span><span class="sxs-lookup"><span data-stu-id="08996-669">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="08996-670">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="08996-670">Az.PrivateDns</span></span>
* <span data-ttu-id="08996-671">Korrigerade formatering av utförlig utdatasträng för Remove-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="08996-671">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="08996-672">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="08996-672">Az.RecoveryServices</span></span>
* <span data-ttu-id="08996-673">Azure Site Recovery-stöd för att skapa en återställningsplan för replikering mellan zoner från xml-indata.</span><span class="sxs-lookup"><span data-stu-id="08996-673">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="08996-674">Uppdaterad sammansättningsversion för cmdletar för SiteRecovery och Backup</span><span class="sxs-lookup"><span data-stu-id="08996-674">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="08996-675">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08996-675">Az.Resources</span></span>
* <span data-ttu-id="08996-676">Lade till slutparameter för cmdletarna Get-AzDeploymentScriptLog och Save-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="08996-676">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="08996-677">Formaterad utdataegenskap så att den kan visas i cmdlet-utdata för Get-AzDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="08996-677">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="08996-678">Bytte namn på parametern -DeploymentScriptInputObject till -DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="08996-678">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="08996-679">Åtgärdade saknade fil/målnamn i cmdlet-meddelanden.</span><span class="sxs-lookup"><span data-stu-id="08996-679">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="08996-680">Uppdaterad sammansättningsversion för cmdletar för resurshanterare och taggar</span><span class="sxs-lookup"><span data-stu-id="08996-680">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="08996-681">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08996-681">Az.Sql</span></span>
* <span data-ttu-id="08996-682">Lade till UsePrivateLinkConnection till ”New-AzSqlSyncGroup”, ”Update-AzSqlSyncGroup”, ”New-AzSqlSyncMember” och ”Update-AzSqlSyncMember”</span><span class="sxs-lookup"><span data-stu-id="08996-682">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="08996-683">Lade till SyncMemberAzureDatabaseResourceId till ”New-AzSqlSyncMember” and ”Update-AzSqlSyncMember”</span><span class="sxs-lookup"><span data-stu-id="08996-683">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="08996-684">Lade till stöd för att söka efter gästanvändare för att ange administratörs-cmdlet för SQL Server Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="08996-684">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="08996-685">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="08996-685">Az.Storage</span></span>
* <span data-ttu-id="08996-686">Uppdaterad sammansättningsversion för dataplan-cmdletar</span><span class="sxs-lookup"><span data-stu-id="08996-686">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="08996-687">4.1.0 – maj 2020</span><span class="sxs-lookup"><span data-stu-id="08996-687">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="08996-688">Höjdpunkter sedan den senaste uppdateringen</span><span class="sxs-lookup"><span data-stu-id="08996-688">Highlights since the last release</span></span>
* <span data-ttu-id="08996-689">PowerShell-versioner som stöds: Windows PowerShell 5.1, PowerShell Core 6.2.4+ och PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="08996-689">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="08996-690">Allmän tillgänglighet för Az.Functions</span><span class="sxs-lookup"><span data-stu-id="08996-690">General availability of Az.Functions</span></span> 
* <span data-ttu-id="08996-691">Nya stora uppdateringar har gjorts för Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources och Az.Storage</span><span class="sxs-lookup"><span data-stu-id="08996-691">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="08996-692">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="08996-692">Az.Accounts</span></span>
* <span data-ttu-id="08996-693">”Add-AzEnvironment” och ”Set-AzEnvironment” har uppdaterats med stöd för parametrarna ”AzureSynapseAnalyticsEndpointResourceId” och ”AzureSynapseAnalyticsEndpointSuffix”</span><span class="sxs-lookup"><span data-stu-id="08996-693">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="08996-694">Azure.Core-relaterade sammansättningar har lagts till i Az.Accounts; PowerShell-plattformar som stöds är Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span><span class="sxs-lookup"><span data-stu-id="08996-694">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="08996-695">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="08996-695">Az.Aks</span></span>
* <span data-ttu-id="08996-696">API-versionen har uppgraderats till 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="08996-696">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="08996-697">Stöds för att skapa AKS med hjälp av Windows-container</span><span class="sxs-lookup"><span data-stu-id="08996-697">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="08996-698">Nya cmdletar är tillgängliga: ”New-AzAksNodePool”, ”Update-AzAksNodePool”, ”Remove-AzAksNodePool”,        ”Get-AzAksNodePool”, ”Install-AzAksKubectl”, ”Get-AzAksVersion”</span><span class="sxs-lookup"><span data-stu-id="08996-698">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="08996-699">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="08996-699">Az.ApiManagement</span></span>
* <span data-ttu-id="08996-700">Parametrarna ”New-AzApiManagement” och ”Set-AzApiManagement”: [-AssignIdentity] har bytt namn till [-SystemAssignedIdentity]</span><span class="sxs-lookup"><span data-stu-id="08996-700">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="08996-701">”New-AzApiManagement” och ”Set-AzApiManagement”: En ny parameter har lagts till: [-UserAssignedIdentity <String[]>]</span><span class="sxs-lookup"><span data-stu-id="08996-701">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="08996-702">”Get-AzApiManagementProperty” har bytt namn till ”Get-AzApiManagementNamedValue”.</span><span class="sxs-lookup"><span data-stu-id="08996-702">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="08996-703">PropertyId-parametern har bytt namn till NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="08996-703">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="08996-704">”New-AzApiManagementProperty” har bytt namn till ”New-AzApiManagementNamedValue”.</span><span class="sxs-lookup"><span data-stu-id="08996-704">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="08996-705">PropertyId-parametern har bytt namn till NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="08996-705">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="08996-706">”Set-AzApiManagementProperty” har bytt namn till ”Set-AzApiManagementNamedValue”.</span><span class="sxs-lookup"><span data-stu-id="08996-706">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="08996-707">PropertyId-parametern har bytt namn till NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="08996-707">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="08996-708">”Remove-AzApiManagementProperty” har bytt namn till ”Remove-AzApiManagementNamedValue”.</span><span class="sxs-lookup"><span data-stu-id="08996-708">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="08996-709">PropertyId-parametern har bytt namn till NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="08996-709">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="08996-710">Den nya cmdleten Get-AzApiManagementAuthorizationServerClientSecret gör att ”Get-AzApiManagementAuthorizationServer” inte längre returnerar klienthemligheter.</span><span class="sxs-lookup"><span data-stu-id="08996-710">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="08996-711">Den nya cmdleten ”Get-AzApiManagementNamedValueSecretValue” gör att ”Get-AzApiManagementNamedValue” inte returnerar värdet för en hemlighet.</span><span class="sxs-lookup"><span data-stu-id="08996-711">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="08996-712">Den nya cmdleten ”Get-AzApiManagementOpenIdConnectProviderClientSecret” gör att ”Get-AzApiManagementOpenIdConnectProvider” inte längre returnerar klienthemligheter.</span><span class="sxs-lookup"><span data-stu-id="08996-712">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="08996-713">Den nya cmdleten ”Get-AzApiManagementSubscriptionKey” gör att ”Get-AzApiManagementSubscription” inte längre returnerar prenumerationsnycklar.</span><span class="sxs-lookup"><span data-stu-id="08996-713">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="08996-714">Den nya cmdleten ”Get-AzApiManagementTenantAccessSecret” gör att ”Get-AzApiManagementTenantAccess” inte längre returnerar nycklar.</span><span class="sxs-lookup"><span data-stu-id="08996-714">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="08996-715">Den nya cmdleten ”Get-AzApiManagementTenantGitAccessSecret” gör att ”Get-AzApiManagementTenantGitAccess” inte längre returnerar nycklar.</span><span class="sxs-lookup"><span data-stu-id="08996-715">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="08996-716">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="08996-716">Az.ApplicationInsights</span></span>
* <span data-ttu-id="08996-717">Tillagda parametrar: ”RetentionInDays” ”PublicNetworkAccessForIngestion” ”PublicNetworkAccessForQuery” för ”New-AzApplicationInsights”</span><span class="sxs-lookup"><span data-stu-id="08996-717">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="08996-718">Cmdleten ”Update-AzApplicationInsights” har skapats</span><span class="sxs-lookup"><span data-stu-id="08996-718">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="08996-719">Cmdletar har skapats för länkat lagringskonto</span><span class="sxs-lookup"><span data-stu-id="08996-719">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="08996-720">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="08996-720">Az.Batch</span></span>
* <span data-ttu-id="08996-721">Az.Batch har uppdaterats att använda ”Microsoft.Azure.Batch” SDK version 13.0.0 och ”Microsoft.Azure.Management.Batch” SDK version 9.0.0.</span><span class="sxs-lookup"><span data-stu-id="08996-721">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="08996-722">Nu kan du välja vilken typ av certifikat du lägger till genom att använda den nya parametern ”-CertificateKind” med ”New-AzBatchCertificate”.</span><span class="sxs-lookup"><span data-stu-id="08996-722">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="08996-723">Egenskapen ”ApplicationPackages” har tagits bort från ”PSApplication”, som tidigare alltid var ''.</span><span class="sxs-lookup"><span data-stu-id="08996-723">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="08996-724">Specifika paket i ett program kan nu hämtas med hjälp av ”Get-AzBatchApplicationPackage”.</span><span class="sxs-lookup"><span data-stu-id="08996-724">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="08996-725">Ett exempel: ”Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication”.</span><span class="sxs-lookup"><span data-stu-id="08996-725">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="08996-726">Nu när du skapar en pool med hjälp av ”New-AzBatchPool” kan egenskapen ”VirtualMachineImageId” för ”PSImageReference” endast referera till en Shared Image Gallery-avbildning.</span><span class="sxs-lookup"><span data-stu-id="08996-726">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="08996-727">När du skapar en pool med hjälp av ”New-AzBatchPool” kan poolen etableras utan en offentlig IP-adress med hjälp av den nya egenskapen ”PublicIPAddressConfiguration” för ”PSNetworkConfiguration”.</span><span class="sxs-lookup"><span data-stu-id="08996-727">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="08996-728">Egenskapen ”PublicIPs” för ”PSNetworkConfiguration” har också flyttats till ”PSPublicIPAddressConfiguration”.</span><span class="sxs-lookup"><span data-stu-id="08996-728">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="08996-729">Den här egenskapen kan bara anges om ”IPAddressProvisioningType” är ”UserManaged”.</span><span class="sxs-lookup"><span data-stu-id="08996-729">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08996-730">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08996-730">Az.Compute</span></span>
* <span data-ttu-id="08996-731">Parametern HostId har lagts till för cmdleten ”Update-AzVM”t</span><span class="sxs-lookup"><span data-stu-id="08996-731">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="08996-732">Hjälpdokumenten har uppdaterats för cmdletarna ”New-AzVMConfig”, ”New-AzVmssConfig”, ”Update-AzVmss”, ”Set-AzVMOperatingSystem” och ”Set-AzVmssOsProfile”.</span><span class="sxs-lookup"><span data-stu-id="08996-732">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="08996-733">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="08996-733">Breaking changes</span></span>
    - <span data-ttu-id="08996-734">Parametern FilterExpression tas bort från cmdleten ”Get-AzVMImage”.</span><span class="sxs-lookup"><span data-stu-id="08996-734">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="08996-735">Parametern AssignIdentity tas bort från cmdletarna ”New-AzVmssConfig”, ”New-AzVMConfig” och ”Update-AzVM”.</span><span class="sxs-lookup"><span data-stu-id="08996-735">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="08996-736">AutomaticRepairMaxInstanceRepairsPercent tas bort från cmdletarna ”New-AzVmssConfig” och ”Update-AzVmss”.</span><span class="sxs-lookup"><span data-stu-id="08996-736">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="08996-737">Egenskaperna AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus och VirtualMachineScaleSetsColocationStatus tas bort från ProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="08996-737">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="08996-738">Egenskapen MaxInstanceRepairsPercent tas bort från AutomaticRepairsPolicy.</span><span class="sxs-lookup"><span data-stu-id="08996-738">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="08996-739">Typerna AvailabilitySets, VirtualMachines och VirtualMachineScaleSets ändras från IList<SubResource> till IList<SubResourceWithColocationStatus>.</span><span class="sxs-lookup"><span data-stu-id="08996-739">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="08996-740">Beskrivningen för cmdleten ”Get-AzVM” har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="08996-740">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="08996-741">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="08996-741">Az.DataFactory</span></span>
* <span data-ttu-id="08996-742">CRUD-stöd för egenskaper för dataflödeskörning  i hanterad IR.</span><span class="sxs-lookup"><span data-stu-id="08996-742">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="08996-743">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="08996-743">Az.FrontDoor</span></span>
* <span data-ttu-id="08996-744">Nya cmdletar har lagts till för att skapa, uppdatera, hämta och ta bort (CRUD) Front Door-regelmotorobjekt</span><span class="sxs-lookup"><span data-stu-id="08996-744">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="08996-745">Hjälp-cmdletar har lagts till för konstruktion av Front Door-regelmotorobjekt</span><span class="sxs-lookup"><span data-stu-id="08996-745">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="08996-746">Regelmotorreferens har lagts till för Front Door-hanteringsregelobjekt.</span><span class="sxs-lookup"><span data-stu-id="08996-746">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="08996-747">Parametrar för Private Link har lagts till för Front Door-serverdelsobjekt</span><span class="sxs-lookup"><span data-stu-id="08996-747">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="08996-748">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="08996-748">Az.Functions</span></span>
* <span data-ttu-id="08996-749">Allmän tillgänglighet för ”Az.Functions”-modulen</span><span class="sxs-lookup"><span data-stu-id="08996-749">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="08996-750">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="08996-750">Az.HDInsight</span></span>
* <span data-ttu-id="08996-751">Stöd för diskkryptering med kundhanterad nyckel.</span><span class="sxs-lookup"><span data-stu-id="08996-751">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="08996-752">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="08996-752">Az.HealthcareApis</span></span>
* <span data-ttu-id="08996-753">Åtkomstprinciper använder inte längre det aktiva huvudkontot som standard</span><span class="sxs-lookup"><span data-stu-id="08996-753">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="08996-754">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="08996-754">Az.IotHub</span></span>
* <span data-ttu-id="08996-755">En cmdlet har lagts till som anropar en fråga i en IoT-hubb för att hämta information med ett SQL-liknande språk.</span><span class="sxs-lookup"><span data-stu-id="08996-755">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="08996-756">Problemet som gjorde att ”Add-AzIotHubDevice” inte skapade en Edge-aktiverad enhet utan underordnade enheter har åtgärdats [#11597]</span><span class="sxs-lookup"><span data-stu-id="08996-756">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="08996-757">En cmdlet har lagts till för att generera SAS-token för en Iot-hubb, enhet eller modul.</span><span class="sxs-lookup"><span data-stu-id="08996-757">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="08996-758">En cmdlet har lagts till för att anropa en måttfråga om konfiguration.</span><span class="sxs-lookup"><span data-stu-id="08996-758">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="08996-759">Hantera automatisk distribution av IoT Edge i stor skala.</span><span class="sxs-lookup"><span data-stu-id="08996-759">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="08996-760">Nya cmdlet:ar är:</span><span class="sxs-lookup"><span data-stu-id="08996-760">New cmdlets are:</span></span>
    - <span data-ttu-id="08996-761">”Add-AzIotHubDeployment”</span><span class="sxs-lookup"><span data-stu-id="08996-761">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="08996-762">”Get-AzIotHubDeployment”</span><span class="sxs-lookup"><span data-stu-id="08996-762">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="08996-763">”Remove-AzIotHubDeployment”</span><span class="sxs-lookup"><span data-stu-id="08996-763">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="08996-764">”Set-AzIotHubDeployment”</span><span class="sxs-lookup"><span data-stu-id="08996-764">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="08996-765">En cmdlet har lagts till för att anropa en måttfråga om IoT Edge-distribution.</span><span class="sxs-lookup"><span data-stu-id="08996-765">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="08996-766">En cmdlet har lagts till för att tillämpa konfigurationsinnehåll på den angivna gränsenheten.</span><span class="sxs-lookup"><span data-stu-id="08996-766">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="08996-767">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="08996-767">Az.KeyVault</span></span>
* <span data-ttu-id="08996-768">Två alias har tagits bort: ”New-AzKeyVaultCertificateAdministratorDetails” och ”New-AzKeyVaultCertificateOrganizationDetails”</span><span class="sxs-lookup"><span data-stu-id="08996-768">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="08996-769">Nu är mjuk borttagning aktiverat som standard när ett nyckelvalv skapas</span><span class="sxs-lookup"><span data-stu-id="08996-769">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="08996-770">Nätverksregler kan ställas in för att styra åtkomsten från särskilda nätverksplatser när du skapar ett nyckelvalv</span><span class="sxs-lookup"><span data-stu-id="08996-770">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="08996-771">Stöd för BYOK (Bring Your Own Key) har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-771">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="08996-772">”Add-AzKeyVaultKey” stöder generering av en KeyExchange-nyckel</span><span class="sxs-lookup"><span data-stu-id="08996-772">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="08996-773">”Get-AzKeyVaultKey” stöder nedladdning av en offentlig nyckel i PEM-format</span><span class="sxs-lookup"><span data-stu-id="08996-773">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="08996-774">”KeyOps”-delen av hjälpdokumentet för ”Add-AzKeyVaultKey” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="08996-774">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="08996-775">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="08996-775">Az.Monitor</span></span>
* <span data-ttu-id="08996-776">Bugg för ”Set-AzDiagnosticSettings” har åtgärdats; kvarhållningsprincipen tillämpas inte på alla kategorier [#11589]</span><span class="sxs-lookup"><span data-stu-id="08996-776">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="08996-777">Stöd för WebTest-tillgänglighetskriterier för måttavisering V2</span><span class="sxs-lookup"><span data-stu-id="08996-777">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="08996-778">”New-AzMetricAlertRuleV2Criteria”: ett alternativ för att skapa tillgänglighetskriterier för webbtest har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-778">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="08996-779">”Add-AzMetricAlertRuleV2”: stöd för de nya tillgänglighetskriterierna för webbtest</span><span class="sxs-lookup"><span data-stu-id="08996-779">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="08996-780">Redundant definition har tagits bort för RetentionPolicy i PSLogProfile [#7608]</span><span class="sxs-lookup"><span data-stu-id="08996-780">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="08996-781">Redundanta egenskaper som definierats i PSEventData har tagits bort [#11353]</span><span class="sxs-lookup"><span data-stu-id="08996-781">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="08996-782">”Get-AzLog” har bytt namn till ”Get-AzActivityLog”</span><span class="sxs-lookup"><span data-stu-id="08996-782">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="08996-783">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08996-783">Az.Network</span></span>
* <span data-ttu-id="08996-784">Attribut för icke-bakåtkompatibel ändring har lagts till för att meddela att standardbeteendet för zoner kommer att ändras</span><span class="sxs-lookup"><span data-stu-id="08996-784">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="08996-785">”New-AzPublicIpAddress”</span><span class="sxs-lookup"><span data-stu-id="08996-785">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="08996-786">”New-AzPublicIpPrefix”</span><span class="sxs-lookup"><span data-stu-id="08996-786">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="08996-787">”New-AzLoadBalancerFrontendIpConfig”</span><span class="sxs-lookup"><span data-stu-id="08996-787">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="08996-788">Stöd har lagts till för en ny resurs på den översta nivån, SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="08996-788">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="08996-789">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="08996-789">New cmdlets added:</span></span>
        - <span data-ttu-id="08996-790">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="08996-790">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="08996-791">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="08996-791">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="08996-792">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="08996-792">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="08996-793">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="08996-793">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="08996-794">”RequiredZoneNames” har lagts till för ”PSPrivateLinkResource” och ”GroupId” för ”PSPrivateEndpointConnection”</span><span class="sxs-lookup"><span data-stu-id="08996-794">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="08996-795">Fel parametertyp för SuccessThresholdRoundTripTimeMs-parametern för New-AzNetworkWatcherConnectionMonitorTestConfigurationObject har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="08996-795">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="08996-796">VirtualWan-cmdletar har uppdaterats för att ange AllowVnetToVnetTraffic-argumentets standardvärde till True.</span><span class="sxs-lookup"><span data-stu-id="08996-796">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="08996-797">”New-AzVirtualWan”</span><span class="sxs-lookup"><span data-stu-id="08996-797">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="08996-798">”Update-AzVirtualWan”</span><span class="sxs-lookup"><span data-stu-id="08996-798">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="08996-799">Nya cmdletar har lagts till för att stödja DNS-zongrupp för privat slutpunkt</span><span class="sxs-lookup"><span data-stu-id="08996-799">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="08996-800">”New-AzPrivateDnsZoneConfig”</span><span class="sxs-lookup"><span data-stu-id="08996-800">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="08996-801">”Get-AzPrivateDnsZoneGroup”</span><span class="sxs-lookup"><span data-stu-id="08996-801">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="08996-802">”New-AzPrivateDnsZoneGroup”</span><span class="sxs-lookup"><span data-stu-id="08996-802">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="08996-803">”Set-AzPrivateDnsZoneGroup”</span><span class="sxs-lookup"><span data-stu-id="08996-803">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="08996-804">”Remove-AzPrivateDnsZoneGroup”</span><span class="sxs-lookup"><span data-stu-id="08996-804">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="08996-805">Parametrarna ”DNSEnableProxy”, ”DNSRequireProxyForNetworkRules” och ”DNSServers” har lagts till för ”AzureFirewall”</span><span class="sxs-lookup"><span data-stu-id="08996-805">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="08996-806">Parametrarna ”EnableDnsProxy”, ”DnsProxyNotRequiredForNetworkRule” och ”DnsServer” har lagts till för ”AzureFirewall”</span><span class="sxs-lookup"><span data-stu-id="08996-806">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="08996-807">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="08996-807">Updated cmdlet:</span></span>
        - <span data-ttu-id="08996-808">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="08996-808">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="08996-809">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="08996-809">Az.OperationalInsights</span></span>
* <span data-ttu-id="08996-810">Äldre kod har uppdaterats för att tillämpa ny genererad SDK</span><span class="sxs-lookup"><span data-stu-id="08996-810">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="08996-811">Cmdletar har tagits bort på grund av föråldrade API:er</span><span class="sxs-lookup"><span data-stu-id="08996-811">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="08996-812">”Get-AzOperationalInsightsSavedSearchResult” (alias ”Get-AzOperationalInsightsSavedSearchResults”)</span><span class="sxs-lookup"><span data-stu-id="08996-812">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="08996-813">”Get-AzOperationalInsightsSearchResult” (alias ”Get-AzOperationalInsightsSearchResults”)</span><span class="sxs-lookup"><span data-stu-id="08996-813">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="08996-814">”Get-AzOperationalInsightsLinkTarget” (alias ”Get-AzOperationalInsightsLinkTargets”)</span><span class="sxs-lookup"><span data-stu-id="08996-814">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="08996-815">Parametrar har lagts till för ”Set-AzOperationalInsightsWorkspace” och ”New-AzOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="08996-815">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="08996-816">Cmdletar har skapats för länkat lagringskonto</span><span class="sxs-lookup"><span data-stu-id="08996-816">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="08996-817">Cmdletar har skapats för kluster och länkad tjänst</span><span class="sxs-lookup"><span data-stu-id="08996-817">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="08996-818">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="08996-818">Az.RecoveryServices</span></span>
* <span data-ttu-id="08996-819">Azure Site Recovery: Stöd har lagts till för att skydda VM-närhetsplaceringsgrupper för Azure till Azure-provider.</span><span class="sxs-lookup"><span data-stu-id="08996-819">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="08996-820">Azure Site Recovery: Stöd har lagts till för replikering mellan zoner.</span><span class="sxs-lookup"><span data-stu-id="08996-820">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="08996-821">Azure Backup: Stöd har lagts till för långsiktig kvarhållning för Azure FileShare-återställningspunkter.</span><span class="sxs-lookup"><span data-stu-id="08996-821">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="08996-822">Azure Backup: Egenskaper för diskexkludering har lagts till för cmdlet-utdata från ”Get-AzRecoveryServicesBackupItem”.</span><span class="sxs-lookup"><span data-stu-id="08996-822">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="08996-823">En privat slutpunkt har lagts till för filen med valvets autentiseringsuppgifter för Site Recovery-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="08996-823">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="08996-824">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08996-824">Az.Resources</span></span>
* <span data-ttu-id="08996-825">En varning har lagts till om visningsfördröjning när en ny rolldefinition skapas</span><span class="sxs-lookup"><span data-stu-id="08996-825">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="08996-826">Princip-cmdletar har ändrats för utmatning av starkt typifierade objekt</span><span class="sxs-lookup"><span data-stu-id="08996-826">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="08996-827">Parametern ”-TenantLevel” har tagits bort för användning med ”Get-AzResourceLock” [#11335]</span><span class="sxs-lookup"><span data-stu-id="08996-827">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="08996-828">”Remove-AzResourceGroup -Id ResourceId” har åtgärdats [#9882]</span><span class="sxs-lookup"><span data-stu-id="08996-828">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="08996-829">En ny cmdlet har lagts till för att hämta What-If-resultat för ARM-mallar i omfånget för resursgrupper: ”Get-AzDeploymentResourceGroupWhatIfResult”</span><span class="sxs-lookup"><span data-stu-id="08996-829">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="08996-830">En ny cmdlet har lagts till för att hämta What-If-resultat för ARM-mallar i prenumerationsomfånget: ”Get-AzDeploymentWhatIfResult”</span><span class="sxs-lookup"><span data-stu-id="08996-830">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="08996-831">Alias: ”Get-AzSubscriptionDeploymentWhatIf”</span><span class="sxs-lookup"><span data-stu-id="08996-831">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="08996-832">Parametrarna ”-WhatIf” och ”-Confirm” har åsidosatts för ”New-AzDeployment” och ”New-AzResourceGroupDeployment” för att använda What-If-resultat för ARM-mallar</span><span class="sxs-lookup"><span data-stu-id="08996-832">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="08996-833">Ett utfasningsmeddelande har lagts till för parametern ”ApiVersion” i distributions-cmdletar</span><span class="sxs-lookup"><span data-stu-id="08996-833">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="08996-834">En funktion har lagts till för att visa förbättrade felmeddelanden för distributionsfel</span><span class="sxs-lookup"><span data-stu-id="08996-834">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="08996-835">CorrelationId-loggning har lagts till för distributionsfel</span><span class="sxs-lookup"><span data-stu-id="08996-835">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="08996-836">Egenskapen ”error” har lagts till i utdata från distributionsskript</span><span class="sxs-lookup"><span data-stu-id="08996-836">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="08996-837">Nuget Microsoft.Azure.Management.ResourceManager har uppdaterats till ”3.7.1-preview”</span><span class="sxs-lookup"><span data-stu-id="08996-837">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="08996-838">Specifika testfall har tagits bort då egenskapen Error i DeploymentValidateResult har ändrats till lässkyddad från nuget 3.7.1-preview</span><span class="sxs-lookup"><span data-stu-id="08996-838">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="08996-839">GenericResourceExpanded har flyttats från SDK ResourceManager 3.7.1-preview</span><span class="sxs-lookup"><span data-stu-id="08996-839">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="08996-840">Stöd för taggar har lagts till för alla Get-cmdletar för distribution, samt</span><span class="sxs-lookup"><span data-stu-id="08996-840">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="08996-841">”New-AzDeployment”</span><span class="sxs-lookup"><span data-stu-id="08996-841">'New-AzDeployment'</span></span>
    - <span data-ttu-id="08996-842">”New-AzManagementGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="08996-842">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="08996-843">”New-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="08996-843">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="08996-844">”New-AzTenantDeployment”</span><span class="sxs-lookup"><span data-stu-id="08996-844">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="08996-845">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="08996-845">Az.ServiceFabric</span></span>
* <span data-ttu-id="08996-846">En bugg har åtgärdats som gjorde att --SecretIdentifier fick fel tumavtryck för certifikat när ett certifikat lades till</span><span class="sxs-lookup"><span data-stu-id="08996-846">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="08996-847">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08996-847">Az.Sql</span></span>
* <span data-ttu-id="08996-848">Förbättrade prestanda för:</span><span class="sxs-lookup"><span data-stu-id="08996-848">Enhance performance of:</span></span>
    - <span data-ttu-id="08996-849">”Set-AzSqlDatabaseSensitivityClassification”</span><span class="sxs-lookup"><span data-stu-id="08996-849">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="08996-850">”Set-AzSqlInstanceDatabaseSensitivityClassification”</span><span class="sxs-lookup"><span data-stu-id="08996-850">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="08996-851">”Remove-AzSqlDatabaseSensitivityClassification”</span><span class="sxs-lookup"><span data-stu-id="08996-851">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="08996-852">”Remove-AzSqlInstanceDatabaseSensitivityClassification”</span><span class="sxs-lookup"><span data-stu-id="08996-852">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="08996-853">”Enable-AzSqlDatabaseSensitivityRecommendation”</span><span class="sxs-lookup"><span data-stu-id="08996-853">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="08996-854">”Enable-AzSqlInstanceDatabaseSensitivityRecommendation”</span><span class="sxs-lookup"><span data-stu-id="08996-854">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="08996-855">”Disable-AzSqlDatabaseSensitivityRecommendation”</span><span class="sxs-lookup"><span data-stu-id="08996-855">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="08996-856">”Disable-AzSqlInstanceDatabaseSensitivityRecommendation”</span><span class="sxs-lookup"><span data-stu-id="08996-856">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="08996-857">Validering på klientsidan har tagits bort för parametern ”RetentionDays” från cmdleten ”Set-AzSqlDatabaseBackupShortTermRetentionPolicy”</span><span class="sxs-lookup"><span data-stu-id="08996-857">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="08996-858">Granskning av ett lagringskonto i Vnet; en bugg har åtgärdats som orsakade fel när en Storage Blob Data-deltagarroll skapades.</span><span class="sxs-lookup"><span data-stu-id="08996-858">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="08996-859">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="08996-859">Az.Storage</span></span>
* <span data-ttu-id="08996-860">”-AsJob” har lagts till för att hämta/lista konto med cmdleten ”Get-AzStorageAccount”</span><span class="sxs-lookup"><span data-stu-id="08996-860">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="08996-861">Gör KeyVersion valfri när lagringskontot uppdateras med KeyvaultEncryption, för att ge stöd för automatisk nyckelrotation</span><span class="sxs-lookup"><span data-stu-id="08996-861">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="08996-862">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="08996-862">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="08996-863">Problemet med borttagning av Azure-filkatalog i pipeline har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="08996-863">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="08996-864">”Remove-AzStorageDirectory”</span><span class="sxs-lookup"><span data-stu-id="08996-864">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="08996-865">Åtgärdat [#9880]: Definitionen av DefaultAction-värdet för NetWorkRule har ändrats för konsekvens med Swagger.</span><span class="sxs-lookup"><span data-stu-id="08996-865">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="08996-866">”Update-AzStorageAccountNetworkRuleSet”</span><span class="sxs-lookup"><span data-stu-id="08996-866">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="08996-867">”Get-AzStorageAccountNetworkRuleSet”</span><span class="sxs-lookup"><span data-stu-id="08996-867">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="08996-868">Åtgärdat [#11624]: Hoppa över dubblettregler när NetworkRules läggs till, för att undvika serverfel</span><span class="sxs-lookup"><span data-stu-id="08996-868">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="08996-869">”Add-AzStorageAccountNetworkRule”</span><span class="sxs-lookup"><span data-stu-id="08996-869">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="08996-870">Microsoft.Azure.Cosmos.Table SDK har uppgraderats till 1.0.7</span><span class="sxs-lookup"><span data-stu-id="08996-870">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="08996-871">Ett varningsmeddelande har lagts till för att påminna användaren om att lista igen med ContinuationToken när endast delobjekt returneras i listan med DataLake Gen2-objekt,</span><span class="sxs-lookup"><span data-stu-id="08996-871">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="08996-872">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="08996-872">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="08996-873">Stöd för att skapa eller uppdatera lagringskonto med Azure Files Active Directory Domain Service-autentisering</span><span class="sxs-lookup"><span data-stu-id="08996-873">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="08996-874">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="08996-874">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="08996-875">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="08996-875">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="08996-876">Stöd för nya eller listade Kerberos-nycklar för lagringskontot</span><span class="sxs-lookup"><span data-stu-id="08996-876">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="08996-877">”New-AzStorageAccountKey”</span><span class="sxs-lookup"><span data-stu-id="08996-877">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="08996-878">”Get-AzStorageAccountKey”</span><span class="sxs-lookup"><span data-stu-id="08996-878">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="08996-879">Stöd för redundans med lagringskonto</span><span class="sxs-lookup"><span data-stu-id="08996-879">Supported failover Storage account</span></span>
    - <span data-ttu-id="08996-880">”Invoke-AzStorageAccountFailover”</span><span class="sxs-lookup"><span data-stu-id="08996-880">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="08996-881">Hjälpen för ”Get-AzStorageBlobCopyState” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="08996-881">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="08996-882">Hjälpen för ”Get-AzStorageFileCopyState” och ”Start-AzStorageBlobCopy” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="08996-882">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="08996-883">Lagringsklientbibliotek v12 har integrerats med Queue- och File-cmdletar</span><span class="sxs-lookup"><span data-stu-id="08996-883">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="08996-884">Utdatatypen har ändrats från CloudFile till AzureStorageFile; ursprungliga utdata blir en underordnad egenskap i den nya utmatningen</span><span class="sxs-lookup"><span data-stu-id="08996-884">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="08996-885">”Get-AzStorageFile”</span><span class="sxs-lookup"><span data-stu-id="08996-885">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="08996-886">”Remove-AzStorageFile”</span><span class="sxs-lookup"><span data-stu-id="08996-886">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="08996-887">”Get-AzStorageFileContent”</span><span class="sxs-lookup"><span data-stu-id="08996-887">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="08996-888">”Set-AzStorageFileContent”</span><span class="sxs-lookup"><span data-stu-id="08996-888">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="08996-889">”Start-AzStorageFileCopy”</span><span class="sxs-lookup"><span data-stu-id="08996-889">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="08996-890">Utdatatypen har ändrats från CloudFileDirectory till AzureStorageFileDirectory; ursprungliga utdata blir en underordnad egenskap i den nya utmatningen</span><span class="sxs-lookup"><span data-stu-id="08996-890">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="08996-891">”New-AzStorageDirectory”</span><span class="sxs-lookup"><span data-stu-id="08996-891">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="08996-892">”Remove-AzStorageDirectory”</span><span class="sxs-lookup"><span data-stu-id="08996-892">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="08996-893">Utdatatypen har ändrats från CloudFileShare till AzureStorageFileShare; ursprungliga utdata blir en underordnad egenskap i den nya utmatningen</span><span class="sxs-lookup"><span data-stu-id="08996-893">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="08996-894">”Get-AzStorageShare”</span><span class="sxs-lookup"><span data-stu-id="08996-894">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="08996-895">”New-AzStorageShare”</span><span class="sxs-lookup"><span data-stu-id="08996-895">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="08996-896">”Remove-AzStorageShare”</span><span class="sxs-lookup"><span data-stu-id="08996-896">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="08996-897">Utdatatypen har ändrats från FileShareProperties till AzureStorageFileShare; ursprungliga utdata blir en underordnad egenskap i den nya utmatningen</span><span class="sxs-lookup"><span data-stu-id="08996-897">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="08996-898">”Set-AzStorageShareQuota”</span><span class="sxs-lookup"><span data-stu-id="08996-898">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="08996-899">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="08996-899">Az.TrafficManager</span></span>
* <span data-ttu-id="08996-900">Felaktigt profilnamn har åtgärdats i utförliga utdata för ”DisableAzureTrafficManagerEndpoint”</span><span class="sxs-lookup"><span data-stu-id="08996-900">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="08996-901">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="08996-901">Az.Websites</span></span>
* <span data-ttu-id="08996-902">Stavfel har åtgärdats i hjälpen för ”Update-AzWebAppAccessRestrictionConfig”.</span><span class="sxs-lookup"><span data-stu-id="08996-902">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="08996-903">3.8.0 – April 2020</span><span class="sxs-lookup"><span data-stu-id="08996-903">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="08996-904">Höjdpunkter sedan den senaste uppdateringen</span><span class="sxs-lookup"><span data-stu-id="08996-904">Highlights since the last release</span></span>
* <span data-ttu-id="08996-905">PowerShell-versioner som Az.Storage stöder: Windows PowerShell 5.1, PowerShell Core 6.2.4+ och PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="08996-905">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="08996-906">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="08996-906">Az.Accounts</span></span>
* <span data-ttu-id="08996-907">Uppdaterade URL:en för Azure PowerShell-enkäten i ”Resolve-AzError” [#11507]</span><span class="sxs-lookup"><span data-stu-id="08996-907">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="08996-908">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="08996-908">Az.ApiManagement</span></span>
* <span data-ttu-id="08996-909">Lade till meddelande om icke-bakåtkompatibel ändring vid ändring i utdata för Azure File-cmdletar i en framtida version</span><span class="sxs-lookup"><span data-stu-id="08996-909">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="08996-910">"Set-AzApiManagementGroup" Uppdaterad dokumentation för att ange GroupId-parametern</span><span class="sxs-lookup"><span data-stu-id="08996-910">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="08996-911">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="08996-911">Az.Cdn</span></span>
* <span data-ttu-id="08996-912">Fast ChinaCDN-relaterad prissättning för SKU-visning</span><span class="sxs-lookup"><span data-stu-id="08996-912">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="08996-913">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="08996-913">Az.CognitiveServices</span></span>
* <span data-ttu-id="08996-914">Identitet som stöds, kryptering, UserOwnedStorage</span><span class="sxs-lookup"><span data-stu-id="08996-914">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08996-915">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08996-915">Az.Compute</span></span>
* <span data-ttu-id="08996-916">Cmdleten ”Set-AzVmssOrchestrationServiceState” har lagts till.</span><span class="sxs-lookup"><span data-stu-id="08996-916">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="08996-917">”Get-AzVmss” med -InstanceView visar OrchestrationService-tillstånd.</span><span class="sxs-lookup"><span data-stu-id="08996-917">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="08996-918">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="08996-918">Az.IotHub</span></span>
* <span data-ttu-id="08996-919">Hantera den dubbla konfigurationen för IoT-enheter, nya cmdletar är:</span><span class="sxs-lookup"><span data-stu-id="08996-919">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="08996-920">'Get-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="08996-920">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="08996-921">'Update-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="08996-921">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="08996-922">En cmdlet har lagts till för att anropa direkt metod på en enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="08996-922">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="08996-923">Hantera dubbel konfiguration för IoT-enhetsmodul, nya cmdletar är:</span><span class="sxs-lookup"><span data-stu-id="08996-923">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="08996-924">'Get-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="08996-924">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="08996-925">'Update-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="08996-925">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="08996-926">Hantera IoT-automatisk konfiguration av enhetshantering i stor skala.</span><span class="sxs-lookup"><span data-stu-id="08996-926">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="08996-927">Nya cmdlet:ar är:</span><span class="sxs-lookup"><span data-stu-id="08996-927">New cmdlets are:</span></span>
    - <span data-ttu-id="08996-928">'Add-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="08996-928">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="08996-929">'Get-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="08996-929">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="08996-930">'Remove-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="08996-930">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="08996-931">'Set-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="08996-931">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="08996-932">En cmdlet har lagts till för att anropa en edge-modulmetod i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="08996-932">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="08996-933">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="08996-933">Az.KeyVault</span></span>
* <span data-ttu-id="08996-934">Har lagt till en ny cmdlet, "Update-AzKeyVault", som kan aktivera mjuk borttagning och rensning av skydd i ett valv</span><span class="sxs-lookup"><span data-stu-id="08996-934">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="08996-935">Har lagt till stöd i Microsoft.PowerShell.SecretManagement [#11178]</span><span class="sxs-lookup"><span data-stu-id="08996-935">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="08996-936">Åtgärdat fel i exemplen i 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span><span class="sxs-lookup"><span data-stu-id="08996-936">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="08996-937">Har lagt till stöd för privat slutpunkt</span><span class="sxs-lookup"><span data-stu-id="08996-937">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="08996-938">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="08996-938">Az.Maintenance</span></span>
* <span data-ttu-id="08996-939">Publicerar slutversion av underhålls-cmdletar för GA</span><span class="sxs-lookup"><span data-stu-id="08996-939">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="08996-940">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="08996-940">Az.Monitor</span></span>
* <span data-ttu-id="08996-941">Har lagt till cmdletar för privat länkomfång</span><span class="sxs-lookup"><span data-stu-id="08996-941">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="08996-942">'Get-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="08996-942">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="08996-943">'Remove-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="08996-943">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="08996-944">'New-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="08996-944">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="08996-945">'Update-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="08996-945">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="08996-946">'Get-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="08996-946">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="08996-947">'New-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="08996-947">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="08996-948">'Remove-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="08996-948">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="08996-949">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08996-949">Az.Network</span></span>
* <span data-ttu-id="08996-950">Uppdaterade cmdletar för att aktivera anslutning på privat IP för Virtual Network Gateway.</span><span class="sxs-lookup"><span data-stu-id="08996-950">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="08996-951">'New-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="08996-951">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="08996-952">'Set-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="08996-952">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="08996-953">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="08996-953">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="08996-954">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="08996-954">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="08996-955">Uppdaterade cmdletar för att aktivera FQDN-baserade LocalNetworkGateways och VpnSites</span><span class="sxs-lookup"><span data-stu-id="08996-955">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="08996-956">'New-AzLocalNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="08996-956">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="08996-957">'New-AzVpnSiteLink'</span><span class="sxs-lookup"><span data-stu-id="08996-957">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="08996-958">Stöd har lagts till för IPv6-adresstypen i ExpressRouteCircuitConnectionConfig (Global Reach)</span><span class="sxs-lookup"><span data-stu-id="08996-958">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="08996-959">Lade till 'Set-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="08996-959">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="08996-960">tillåter inställning av alla befintliga egenskaper inklusive IPv6CircuitConnectionProperties</span><span class="sxs-lookup"><span data-stu-id="08996-960">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="08996-961">Uppdaterade 'Add-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="08996-961">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="08996-962">Lade till en ytterligare valfri parameter, AddressPrefixType, för att specificera adresstypen för adressprefix</span><span class="sxs-lookup"><span data-stu-id="08996-962">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="08996-963">Uppdaterade cmdletar för att aktivera inställningen för DPD-timeout på Virtual Network Gateway-anslutningar.</span><span class="sxs-lookup"><span data-stu-id="08996-963">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="08996-964">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="08996-964">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="08996-965">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="08996-965">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="08996-966">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="08996-966">Az.PolicyInsights</span></span>
* <span data-ttu-id="08996-967">Cmdleten "Start-AzPolicyComplianceScan" har lagts till för att utlösa genomsökningar av principefterlevnad</span><span class="sxs-lookup"><span data-stu-id="08996-967">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="08996-968">Principdefinition, uppsättningsdefinition och tilldelningsversioner har lagts till i "Get-AzPolicyState"-utdata</span><span class="sxs-lookup"><span data-stu-id="08996-968">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="08996-969">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="08996-969">Az.ServiceFabric</span></span>
* <span data-ttu-id="08996-970">Förbättrad kodformatering och användbarhet för "New-AzServiceFabricCluster"-exempel</span><span class="sxs-lookup"><span data-stu-id="08996-970">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="08996-971">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08996-971">Az.Sql</span></span>
* <span data-ttu-id="08996-972">Lade till cmdletarna "Get-AzSqlInstanceOperation" och "Stop-AzSqlInstanceOperation"</span><span class="sxs-lookup"><span data-stu-id="08996-972">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="08996-973">Stöd för granskning för ett lagringskonto i VNet.</span><span class="sxs-lookup"><span data-stu-id="08996-973">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="08996-974">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="08996-974">Az.Storage</span></span>
* <span data-ttu-id="08996-975">Lade till meddelande om icke-bakåtkompatibel ändring vid ändring i utdata för Azure File-cmdletar i en framtida version</span><span class="sxs-lookup"><span data-stu-id="08996-975">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="08996-976">Stöd för nya SkuName StandardGZRS, StandardRAGZRS när ett lagringskonto skapas/uppdateras</span><span class="sxs-lookup"><span data-stu-id="08996-976">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="08996-977">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="08996-977">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="08996-978">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="08996-978">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="08996-979">Stöd för DataLake Gen2</span><span class="sxs-lookup"><span data-stu-id="08996-979">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="08996-980">'New-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="08996-980">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="08996-981">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="08996-981">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="08996-982">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="08996-982">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="08996-983">'Move-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="08996-983">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="08996-984">'Set-AzDataLakeGen2ItemAclObject'</span><span class="sxs-lookup"><span data-stu-id="08996-984">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="08996-985">'Update-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="08996-985">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="08996-986">'Get-AzDataLakeGen2ItemContent'</span><span class="sxs-lookup"><span data-stu-id="08996-986">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="08996-987">'Remove-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="08996-987">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="08996-988">0.10.0-förhandsversion – April 2020</span><span class="sxs-lookup"><span data-stu-id="08996-988">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="08996-989">Allmänt</span><span class="sxs-lookup"><span data-stu-id="08996-989">General</span></span>
* <span data-ttu-id="08996-990">Az-moduler är nu tillgängliga i förhandsversion på Azure Stack Hub.</span><span class="sxs-lookup"><span data-stu-id="08996-990">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="08996-991">Därmed möjliggörs kompatibilitet för flera plattformar med Linux och macOs.</span><span class="sxs-lookup"><span data-stu-id="08996-991">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="08996-992">Azure Stack Hub stöder nu PowerShell Core med AZ-moduler. Mer information finns [här](/azure-stack/operator/powershell-install-az-module)</span><span class="sxs-lookup"><span data-stu-id="08996-992">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](/azure-stack/operator/powershell-install-az-module)</span></span>
* <span data-ttu-id="08996-993">Supportprofil för AZ-moduler 2019-03-01-hybrid:</span><span class="sxs-lookup"><span data-stu-id="08996-993">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="08996-994">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="08996-994">Az.Billing</span></span>
  - <span data-ttu-id="08996-995">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08996-995">Az.Compute</span></span>
  - <span data-ttu-id="08996-996">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="08996-996">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="08996-997">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="08996-997">Az.EventHub</span></span>
  - <span data-ttu-id="08996-998">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="08996-998">Az.IotHub</span></span>
  - <span data-ttu-id="08996-999">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="08996-999">Az.KeyVault</span></span>
  - <span data-ttu-id="08996-1000">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="08996-1000">Az.Monitor</span></span>
  - <span data-ttu-id="08996-1001">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08996-1001">Az.Network</span></span>
  - <span data-ttu-id="08996-1002">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08996-1002">Az.Resources</span></span>
  - <span data-ttu-id="08996-1003">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="08996-1003">Az.Storage</span></span>
  - <span data-ttu-id="08996-1004">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="08996-1004">Az.Websites</span></span>
* <span data-ttu-id="08996-1005">Tre nya PowerShell-moduler för AZ har introducerats som fungerar med Azure Stack Hub, och de är Az.Databox, Az.IotHub och Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="08996-1005">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="08996-1006">Kommandona är i princip oförändrade, med endast mindre ändringar som att AzureRM ändras till AZ</span><span class="sxs-lookup"><span data-stu-id="08996-1006">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="08996-1007">En uppdaterad länk till PowerShell-dokumentationen för Azure Stack Hub finns [här](/azure-stack/operator/powershell-install-az-module)</span><span class="sxs-lookup"><span data-stu-id="08996-1007">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](/azure-stack/operator/powershell-install-az-module)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="08996-1008">3.7.0 – mars 2020</span><span class="sxs-lookup"><span data-stu-id="08996-1008">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="08996-1009">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="08996-1009">Az.Accounts</span></span>
* <span data-ttu-id="08996-1010">Åtgärdade ”Get-AzTenant”/”Get-AzDefault”/”Set-AzDefault”-utlösning av NullReferenceException när du inte är inloggad [#10292]</span><span class="sxs-lookup"><span data-stu-id="08996-1010">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08996-1011">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08996-1011">Az.Compute</span></span>
* <span data-ttu-id="08996-1012">Följande parametrar har lagts till i cmdleten ”New-AzDiskConfig”:</span><span class="sxs-lookup"><span data-stu-id="08996-1012">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="08996-1013">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="08996-1013">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="08996-1014">Tillåten krypteringsegenskap till målparametern för cmdleten ”New-AzGalleryImageVersion”.</span><span class="sxs-lookup"><span data-stu-id="08996-1014">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="08996-1015">Åtgärdade tempDisk-problem för cmdletarna ”Set-AzVmss”-Reimage och ”Invoke-AzVMReimage”.</span><span class="sxs-lookup"><span data-stu-id="08996-1015">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="08996-1016">[#11354]</span><span class="sxs-lookup"><span data-stu-id="08996-1016">[#11354]</span></span>
* <span data-ttu-id="08996-1017">Stöd har lagts till i nedanstående cmdletar för nytt SAP-tillägg</span><span class="sxs-lookup"><span data-stu-id="08996-1017">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="08996-1018">”Set-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="08996-1018">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="08996-1019">”Get-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="08996-1019">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="08996-1020">”Remove-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="08996-1020">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="08996-1021">”Update-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="08996-1021">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="08996-1022">Åtgärdade fel i exempel på hjälpdokument</span><span class="sxs-lookup"><span data-stu-id="08996-1022">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="08996-1023">Visade det exakta strängvärdet för VM PowerState i tabellformat.</span><span class="sxs-lookup"><span data-stu-id="08996-1023">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="08996-1024">”New-AzVmssConfig”: den fasta serialiseringen av egenskapen AutomaticRepairs när SinglePlacementGroup är inaktiverad.</span><span class="sxs-lookup"><span data-stu-id="08996-1024">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="08996-1025">[#11257]</span><span class="sxs-lookup"><span data-stu-id="08996-1025">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="08996-1026">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="08996-1026">Az.DataFactory</span></span>
* <span data-ttu-id="08996-1027">ADF .Net SDK har uppdaterats till 4.8.0</span><span class="sxs-lookup"><span data-stu-id="08996-1027">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="08996-1028">Valfria parametrar har lagts till i kommandot ”Invoke-AzDataFactoryV2Pipeline” för att stödja omkörning</span><span class="sxs-lookup"><span data-stu-id="08996-1028">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="08996-1029">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="08996-1029">Az.DataLakeStore</span></span>
* <span data-ttu-id="08996-1030">Lade till beskrivning för icke-bakåtkompatibel ändring för ”Export-AzDataLakeStoreItem” och ”Import-AzDataLakeStoreItem”</span><span class="sxs-lookup"><span data-stu-id="08996-1030">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="08996-1031">Lade till alternativ för bytekodning för ”New-AzDataLakeStoreItem”, ”Add-AzDAtaLakeStoreItemContent” och ”Get-AzDAtaLakeStoreItemContent”</span><span class="sxs-lookup"><span data-stu-id="08996-1031">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="08996-1032">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="08996-1032">Az.HDInsight</span></span>
* <span data-ttu-id="08996-1033">Stöd för att ange en minimal TLS-version som stöds när klustret skapas.</span><span class="sxs-lookup"><span data-stu-id="08996-1033">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="08996-1034">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="08996-1034">Az.IotHub</span></span>
* <span data-ttu-id="08996-1035">Stöd har lagts till för att hantera distribuerade inställningar per enhet.</span><span class="sxs-lookup"><span data-stu-id="08996-1035">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="08996-1036">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="08996-1036">New Cmdlets are:</span></span>
    - <span data-ttu-id="08996-1037">”Get-AzIotHubDistributedTracing”</span><span class="sxs-lookup"><span data-stu-id="08996-1037">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="08996-1038">”Set-AzIotHubDistributedTracing”</span><span class="sxs-lookup"><span data-stu-id="08996-1038">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="08996-1039">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="08996-1039">Az.KeyVault</span></span>
* <span data-ttu-id="08996-1040">Ändrade attribut för icke-bakåtkompatibel ändring lades till för ”New-AzKeyVault”</span><span class="sxs-lookup"><span data-stu-id="08996-1040">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="08996-1041">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="08996-1041">Az.Monitor</span></span>
* <span data-ttu-id="08996-1042">Uppdaterad dokumentation för ”New-AzScheduledQueryRuleLogMetricTrigger”</span><span class="sxs-lookup"><span data-stu-id="08996-1042">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="08996-1043">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08996-1043">Az.Network</span></span>
* <span data-ttu-id="08996-1044">Uppdaterade cmdletar för att tillåta VirtualHubVnetConnections mellan klienter</span><span class="sxs-lookup"><span data-stu-id="08996-1044">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="08996-1045">”New-AzVirtualHubVnetConnection”</span><span class="sxs-lookup"><span data-stu-id="08996-1045">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="08996-1046">”Update-AzVirtualHubVnetConnection”</span><span class="sxs-lookup"><span data-stu-id="08996-1046">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="08996-1047">”New-AzVirtualHub”</span><span class="sxs-lookup"><span data-stu-id="08996-1047">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="08996-1048">”Update-AzVirtualHub”</span><span class="sxs-lookup"><span data-stu-id="08996-1048">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="08996-1049">SQL Management SDK-beroende har tagits bort</span><span class="sxs-lookup"><span data-stu-id="08996-1049">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="08996-1050">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="08996-1050">Az.PolicyInsights</span></span>
* <span data-ttu-id="08996-1051">Förbättrade felmeddelanden</span><span class="sxs-lookup"><span data-stu-id="08996-1051">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="08996-1052">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="08996-1052">Az.RecoveryServices</span></span>
* <span data-ttu-id="08996-1053">Azure Site Recovery har lagt till stöd för återaktivering av skydd och uppdaterade VM-egenskaper för virtuella Azure-datorer med krypterad disk.</span><span class="sxs-lookup"><span data-stu-id="08996-1053">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="08996-1054">Lade till Azure Site Recovery VmwareToAzure-egenskaper för DR-övervakning</span><span class="sxs-lookup"><span data-stu-id="08996-1054">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="08996-1055">Azure Backup har lagt till stöd för att försöka uppdatera principuppdateringen för misslyckade objekt på nytt.</span><span class="sxs-lookup"><span data-stu-id="08996-1055">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="08996-1056">Azure Backup lagt till stöd för diskundantagsinställningar under säkerhetskopiering och återställning.</span><span class="sxs-lookup"><span data-stu-id="08996-1056">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="08996-1057">Azure Backup lagt till stöd för att återställa flera filer/mappar i AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="08996-1057">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="08996-1058">Azure Backup lade till support för användardefinierad Resourcegroup-support vid uppdatering av IaasVM-princip</span><span class="sxs-lookup"><span data-stu-id="08996-1058">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="08996-1059">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08996-1059">Az.Resources</span></span>
* <span data-ttu-id="08996-1060">Åtgärdade ”Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType” så att den använder den faktisk apiVersion av resurser i stället för standard-apiVersion [#11267]</span><span class="sxs-lookup"><span data-stu-id="08996-1060">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="08996-1061">Lade till correlationId-loggning för felscenarier</span><span class="sxs-lookup"><span data-stu-id="08996-1061">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="08996-1062">Liten dokumentationsändring för ”Get-AzResourceLock”.</span><span class="sxs-lookup"><span data-stu-id="08996-1062">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="08996-1063">Lade till exempel.</span><span class="sxs-lookup"><span data-stu-id="08996-1063">Added example.</span></span>
* <span data-ttu-id="08996-1064">Undantaget enkelt citattecken i parametervärde för ”Get-AzADUser” [#11317]</span><span class="sxs-lookup"><span data-stu-id="08996-1064">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="08996-1065">Nya cmdletar har lagts till för distributionsskript (”Get-AzDeploymentScript”, ”Get-AzDeploymentScriptLog”, ”Save-AzDeploymentScriptLog”, ”Remove-AzDeploymentScript”)</span><span class="sxs-lookup"><span data-stu-id="08996-1065">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="08996-1066">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08996-1066">Az.Sql</span></span>
* <span data-ttu-id="08996-1067">En läsbar sekundär parameter har lagts till i Invoke-AzSqlDatabaseFailover</span><span class="sxs-lookup"><span data-stu-id="08996-1067">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="08996-1068">Cmdleten Disable-AzSqlServerActiveDirectoryOnlyAuthentication har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-1068">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="08996-1069">Den sparade känslighet rangordningen när kolumner klassificeras i databasen.</span><span class="sxs-lookup"><span data-stu-id="08996-1069">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="08996-1070">Az.Support</span><span class="sxs-lookup"><span data-stu-id="08996-1070">Az.Support</span></span>
* <span data-ttu-id="08996-1071">Allmän tillgänglighet för ”Az.Support”-modulen</span><span class="sxs-lookup"><span data-stu-id="08996-1071">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="08996-1072">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="08996-1072">Az.Websites</span></span>
* <span data-ttu-id="08996-1073">Stöd har lagts till för att arbeta med trafikdirigeringsregler för webbappar under nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="08996-1073">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="08996-1074">”Get-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="08996-1074">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="08996-1075">”Update-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="08996-1075">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="08996-1076">”Add-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="08996-1076">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="08996-1077">”Remove-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="08996-1077">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="08996-1078">3.6.1 – mars 2020</span><span class="sxs-lookup"><span data-stu-id="08996-1078">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="08996-1079">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="08996-1079">Az.Accounts</span></span>
* <span data-ttu-id="08996-1080">Öppna sidan med Azure PowerShell-enkäten i ”Send-Feedback” [#11020]</span><span class="sxs-lookup"><span data-stu-id="08996-1080">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="08996-1081">Visa URL:en för Azure PowerShell-enkäten i ”Resolve-Error” [#11021]</span><span class="sxs-lookup"><span data-stu-id="08996-1081">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="08996-1082">Az-version har lagts till i UserAgent</span><span class="sxs-lookup"><span data-stu-id="08996-1082">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="08996-1083">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="08996-1083">Az.ApiManagement</span></span>
* <span data-ttu-id="08996-1084">Stöd har lagts till för att hämta och konfigurera en anpassad domän på DeveloperPortal-slutpunkten [#11007]</span><span class="sxs-lookup"><span data-stu-id="08996-1084">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="08996-1085">”Export-AzApiManagementApi” Stöd har lagts till för att ladda ned API-definition i Json-format [#9987]</span><span class="sxs-lookup"><span data-stu-id="08996-1085">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="08996-1086">”Import-AzApiManagementApi” Stöd har lagts till för att importera OpenApi 3.0-definition från Json-dokument</span><span class="sxs-lookup"><span data-stu-id="08996-1086">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="08996-1087">”New-AzApiManagementIdentityProvider” och ”Set-AzApiManagementIdentityProvider” Stöd har lagts till för att konfigurera ”Signin Tenant” för AAD B2C-provider [#9784]</span><span class="sxs-lookup"><span data-stu-id="08996-1087">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="08996-1088">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="08996-1088">Az.DataLakeStore</span></span>
* <span data-ttu-id="08996-1089">En referens har uttryckligen lagts till för System.Buffers i csproj och psd1.</span><span class="sxs-lookup"><span data-stu-id="08996-1089">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="08996-1090">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="08996-1090">Az.IotHub</span></span>
* <span data-ttu-id="08996-1091">Lade till stöd för att hantera enheter i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="08996-1091">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="08996-1092">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="08996-1092">New Cmdlets are:</span></span>
    - <span data-ttu-id="08996-1093">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="08996-1093">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="08996-1094">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="08996-1094">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="08996-1095">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="08996-1095">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="08996-1096">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="08996-1096">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="08996-1097">Stöd har lagts till för att hantera moduler på en mål-IoT-enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="08996-1097">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="08996-1098">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="08996-1098">New Cmdlets are:</span></span>
    - <span data-ttu-id="08996-1099">”Add-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="08996-1099">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="08996-1100">”Get-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="08996-1100">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="08996-1101">”Remove-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="08996-1101">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="08996-1102">”Set-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="08996-1102">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="08996-1103">Cmdlet har lagts till för att hämta anslutningssträngen för en mål-IoT-enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="08996-1103">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="08996-1104">Cmdlet har lagts till för att hämta anslutningssträngen för en modul på en mål-IoT-enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="08996-1104">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="08996-1105">Stöd har lagts till för att hämta/ange en överordnad enhet för en IoT-enhet.</span><span class="sxs-lookup"><span data-stu-id="08996-1105">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="08996-1106">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="08996-1106">New Cmdlets are:</span></span>
    - <span data-ttu-id="08996-1107">”Get-AzIotHubDeviceParent”</span><span class="sxs-lookup"><span data-stu-id="08996-1107">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="08996-1108">”Set-AzIotHubDeviceParent”</span><span class="sxs-lookup"><span data-stu-id="08996-1108">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="08996-1109">Stöd har lagts till för att hantera en enhets överordnade och underordnade relationer.</span><span class="sxs-lookup"><span data-stu-id="08996-1109">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="08996-1110">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="08996-1110">Az.Monitor</span></span>
* <span data-ttu-id="08996-1111">Utdatavärdet har åtgärdats för ”Get-AzMetricDefinition” [#9714]</span><span class="sxs-lookup"><span data-stu-id="08996-1111">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="08996-1112">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08996-1112">Az.Network</span></span>
* <span data-ttu-id="08996-1113">SQL Management SDK har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="08996-1113">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="08996-1114">Ett problem har åtgärdats med namngivningsskillnader i klassen PrivateLinkServiceConnectionState.</span><span class="sxs-lookup"><span data-stu-id="08996-1114">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="08996-1115">Fältet ActionsRequired mappar till ActionRequired.</span><span class="sxs-lookup"><span data-stu-id="08996-1115">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="08996-1116">PublicNetworkAccess har lagts till i ”New-AzSqlServer” och ”Set-AzSqlServer”</span><span class="sxs-lookup"><span data-stu-id="08996-1116">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="08996-1117">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08996-1117">Az.Resources</span></span>
* <span data-ttu-id="08996-1118">Null-referensfel har åtgärdats i ”Get-AzRoleAssignment”</span><span class="sxs-lookup"><span data-stu-id="08996-1118">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="08996-1119">Växlarna ”-Force” och ”-PassThru” är valfria i ”Remove-AzADGroup” [#10849]</span><span class="sxs-lookup"><span data-stu-id="08996-1119">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="08996-1120">Ett problem har åtgärdats som gjorde att ”MailNickname” inte returnerades i ”Remove-AzADGroup” [#11167]</span><span class="sxs-lookup"><span data-stu-id="08996-1120">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="08996-1121">Ett problem har åtgärdats som gjorde att pipe-åtgärden ”Remove-AzADGroup” inte fungerar [#11171]</span><span class="sxs-lookup"><span data-stu-id="08996-1121">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="08996-1122">Ett null-referensfel har åtgärdats i GetAzureRoleAssignmentCommand</span><span class="sxs-lookup"><span data-stu-id="08996-1122">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="08996-1123">Attribut för icke-bakåtkompatibla ändringar har lagts till för kommande ändringar i cmdlets för principer</span><span class="sxs-lookup"><span data-stu-id="08996-1123">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="08996-1124">”Get-AzResourceGroup” har uppdaterats för att utföra taggfiltrering för resursgrupper på serversidan</span><span class="sxs-lookup"><span data-stu-id="08996-1124">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="08996-1125">Utökade Tag-cmdlets stöder -ResourceId</span><span class="sxs-lookup"><span data-stu-id="08996-1125">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="08996-1126">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="08996-1126">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="08996-1127">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="08996-1127">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="08996-1128">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="08996-1128">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="08996-1129">Ny Tag-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-1129">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="08996-1130">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="08996-1130">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="08996-1131">Flyttade ScopedDeployment från SDK 3.3.0</span><span class="sxs-lookup"><span data-stu-id="08996-1131">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="08996-1132">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08996-1132">Az.Sql</span></span>
* <span data-ttu-id="08996-1133">PublicNetworkAccess har lagts till i ”New-AzSqlServer” och ”Set-AzSqlServer”</span><span class="sxs-lookup"><span data-stu-id="08996-1133">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="08996-1134">Stöd har lagts till för konfiguration av säkerhetskopiering för långsiktig kvarhållning för hanterade databaser</span><span class="sxs-lookup"><span data-stu-id="08996-1134">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="08996-1135">Hämta/ange LTR-princip på en hanterad databas</span><span class="sxs-lookup"><span data-stu-id="08996-1135">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="08996-1136">Hämta LTR-säkerhetskopior efter hanterad databas, hanterad instans eller plats</span><span class="sxs-lookup"><span data-stu-id="08996-1136">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="08996-1137">Ta bort en LTR-säkerhetskopia</span><span class="sxs-lookup"><span data-stu-id="08996-1137">Remove an LTR backup</span></span>
    - <span data-ttu-id="08996-1138">Återställa en LTR-säkerhetskopia för att skapa en ny hanterad databas</span><span class="sxs-lookup"><span data-stu-id="08996-1138">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="08996-1139">MinimalTlsVersion har lagts till för New-AzSqlServer och Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="08996-1139">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="08996-1140">MinimalTlsVersion har lagts till för New-AzSqlInstance och Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="08996-1140">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="08996-1141">SQL SDK-versionen för Az.Network har ändrats</span><span class="sxs-lookup"><span data-stu-id="08996-1141">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="08996-1142">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="08996-1142">Az.Storage</span></span>
* <span data-ttu-id="08996-1143">AllowProtectedAppendWrite stöds i ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="08996-1143">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="08996-1144">”Set-AzRmStorageContainerImmutabilityPolicy”</span><span class="sxs-lookup"><span data-stu-id="08996-1144">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="08996-1145">Varningsmeddelande har lagts till om icke-bakåtkompatibel ändring för ändring av typen AzureStorageTable i en senare version</span><span class="sxs-lookup"><span data-stu-id="08996-1145">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="08996-1146">”New-AzStorageTable”</span><span class="sxs-lookup"><span data-stu-id="08996-1146">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="08996-1147">”Get-AzStorageTable”</span><span class="sxs-lookup"><span data-stu-id="08996-1147">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="08996-1148">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="08996-1148">Az.Websites</span></span>
* <span data-ttu-id="08996-1149">Tag-parametern har lagts till för ”New-AzAppServicePlan” och ”Set-AzAppServicePlan”</span><span class="sxs-lookup"><span data-stu-id="08996-1149">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="08996-1150">Stoppa cmdlet-körning om ett undantag uppstår när en anpassad domän läggs till på en webbplats</span><span class="sxs-lookup"><span data-stu-id="08996-1150">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="08996-1151">Stöd har lagts till för att utföra åtgärder för App Services som inte tillhör samma resursgrupp som App Services-planen</span><span class="sxs-lookup"><span data-stu-id="08996-1151">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="08996-1152">Åtkomstbegränsning har tillämpats på WebApp/Function i olika resursgrupper</span><span class="sxs-lookup"><span data-stu-id="08996-1152">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="08996-1153">Ett problem har åtgärdats för att ange anpassade värdnamn för WebAppSlots</span><span class="sxs-lookup"><span data-stu-id="08996-1153">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="08996-1154">3.5.0 – februari 2020</span><span class="sxs-lookup"><span data-stu-id="08996-1154">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="08996-1155">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="08996-1155">Highlights since the last major release</span></span>
* <span data-ttu-id="08996-1156">Uppdaterade telemetri på klientsidan.</span><span class="sxs-lookup"><span data-stu-id="08996-1156">Updated client side telemetry.</span></span>
* <span data-ttu-id="08996-1157">Az.IotHub lade till cmdletar som stöd för att hantera enheter.</span><span class="sxs-lookup"><span data-stu-id="08996-1157">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="08996-1158">Az.SqlVirtualMachine lade till cmdletar för lyssningsfunktion för tillgänglighetsgrupp.</span><span class="sxs-lookup"><span data-stu-id="08996-1158">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="08996-1159">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="08996-1159">Az.Accounts</span></span>
* <span data-ttu-id="08996-1160">Lade till SubscriptionId, TenantId och körningstid i data för telemetri på klientsidan</span><span class="sxs-lookup"><span data-stu-id="08996-1160">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="08996-1161">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="08996-1161">Az.Automation</span></span>
* <span data-ttu-id="08996-1162">Åtgärdade skrivfel i exempel 1 i referensdokumentation för ”New-AzAutomationSoftwareUpdateConfiguration”</span><span class="sxs-lookup"><span data-stu-id="08996-1162">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="08996-1163">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="08996-1163">Az.CognitiveServices</span></span>
* <span data-ttu-id="08996-1164">Uppdaterade SDK till 7.0</span><span class="sxs-lookup"><span data-stu-id="08996-1164">Updated SDK to 7.0</span></span>
* <span data-ttu-id="08996-1165">Förbättrade felmeddelande vid serversvar om tom brödtext</span><span class="sxs-lookup"><span data-stu-id="08996-1165">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08996-1166">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08996-1166">Az.Compute</span></span>
* <span data-ttu-id="08996-1167">Tillät tomt värde för ProximityPlacementGroupId under uppdatering</span><span class="sxs-lookup"><span data-stu-id="08996-1167">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="08996-1168">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="08996-1168">Az.FrontDoor</span></span>
* <span data-ttu-id="08996-1169">Lade till cmdlet för att hämta hanterade regeldefinitioner som kan användas i WAF</span><span class="sxs-lookup"><span data-stu-id="08996-1169">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="08996-1170">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="08996-1170">Az.IotHub</span></span>
* <span data-ttu-id="08996-1171">Lade till stöd för att hantera enheter i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="08996-1171">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="08996-1172">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="08996-1172">New Cmdlets are:</span></span>
    - <span data-ttu-id="08996-1173">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="08996-1173">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="08996-1174">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="08996-1174">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="08996-1175">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="08996-1175">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="08996-1176">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="08996-1176">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="08996-1177">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="08996-1177">Az.KeyVault</span></span>
* <span data-ttu-id="08996-1178">Åtgärdade duplicerad text för Add-AzKeyVaultKey.md</span><span class="sxs-lookup"><span data-stu-id="08996-1178">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="08996-1179">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="08996-1179">Az.Monitor</span></span>
* <span data-ttu-id="08996-1180">Åtgärdade beskrivning av cmdleten Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="08996-1180">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="08996-1181">En ny parameter med namnet ActionGroupId har lagts till i kommandot ”New-AzMetricAlertRuleV2”.</span><span class="sxs-lookup"><span data-stu-id="08996-1181">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="08996-1182">Användaren kan ange ActionGroupId(string) eller ActionGroup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="08996-1182">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="08996-1183">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08996-1183">Az.Network</span></span>
* <span data-ttu-id="08996-1184">Lade till en extra parameteranteckning för parametern ”-EnableProxyProtocol” för cmdleten ”New-AzPrivateLinkService”.</span><span class="sxs-lookup"><span data-stu-id="08996-1184">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="08996-1185">Åtgärdade FilterData-exempel i Start-AzVirtualNetworkGatewayConnectionPacketCapture.md och Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="08996-1185">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="08996-1186">Lade till paketinsamlingsexempel för att samla in alla inre och yttre paket i Start-AzVirtualNetworkGatewayConnectionPacketCapture.md och Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="08996-1186">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="08996-1187">Lade till stöd för Azure-brandväggsprincip på VNet-brandväggar</span><span class="sxs-lookup"><span data-stu-id="08996-1187">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="08996-1188">Inga nya cmdletar har lagts till.</span><span class="sxs-lookup"><span data-stu-id="08996-1188">No new cmdlets are added.</span></span> <span data-ttu-id="08996-1189">Lättar begränsningen för brandväggsprincip på VNet-brandväggar</span><span class="sxs-lookup"><span data-stu-id="08996-1189">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="08996-1190">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="08996-1190">Az.RecoveryServices</span></span>
* <span data-ttu-id="08996-1191">Lade till stöd för Restore-as-files för SQL-databaser.</span><span class="sxs-lookup"><span data-stu-id="08996-1191">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="08996-1192">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08996-1192">Az.Resources</span></span>
* <span data-ttu-id="08996-1193">Omstrukturerade cmdletar för malldistribution</span><span class="sxs-lookup"><span data-stu-id="08996-1193">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="08996-1194">Lade till nya cmdletar för att hantera distributioner i hanteringsgruppen: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="08996-1194">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="08996-1195">Lade till nya cmdletar för att hantera distributioner i klientorganisationsområdet: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="08996-1195">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="08996-1196">Omstrukturerade \*-AzDeployment-cmdletar för att fungera specifikt i prenumerationsomfattningen</span><span class="sxs-lookup"><span data-stu-id="08996-1196">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="08996-1197">Skapade alias \*-AzSubscriptionDeployment för \*-AzDeployment-cmdletar</span><span class="sxs-lookup"><span data-stu-id="08996-1197">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="08996-1198">Åtgärdade ”Update-AzADApplication” när parametern ”AvailableToOtherTenants” inte har angetts</span><span class="sxs-lookup"><span data-stu-id="08996-1198">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="08996-1199">Tog bort ApplicationObjectWithoutCredentialParameterSet för att undvika AmbiguousParameterSetException.</span><span class="sxs-lookup"><span data-stu-id="08996-1199">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="08996-1200">Återskapade hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="08996-1200">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="08996-1201">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08996-1201">Az.Sql</span></span>
* <span data-ttu-id="08996-1202">Lade till stöd för återställning till tidpunkt mellan prenumerationer på hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="08996-1202">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="08996-1203">Lade till stöd för att ändra befintlig SQL Managed Instance-maskinvarugenerering</span><span class="sxs-lookup"><span data-stu-id="08996-1203">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="08996-1204">Åtgärdade ”Update-AzSqlServerVulnerabilityAssessmentSetting”-hjälpexempel: parameter/egenskapsutdata - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="08996-1204">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="08996-1205">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="08996-1205">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="08996-1206">Lade till cmdletar för lyssningsfunktion för tillgänglighetsgrupp</span><span class="sxs-lookup"><span data-stu-id="08996-1206">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="08996-1207">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="08996-1207">Az.StorageSync</span></span>
* <span data-ttu-id="08996-1208">Uppdaterade teckenuppsättningar som stöds i ”Invoke-AzStorageSyncCompatibilityCheck”.</span><span class="sxs-lookup"><span data-stu-id="08996-1208">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="08996-1209">3.4.0 – februari 2020</span><span class="sxs-lookup"><span data-stu-id="08996-1209">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="08996-1210">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="08996-1210">Highlights since the last major release</span></span>
* <span data-ttu-id="08996-1211">Första Az.CosmosDB-versionen 0.1.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="08996-1211">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="08996-1212">Stöd för Az.Network ConnectionMonitor V2 har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-1212">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="08996-1213">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="08996-1213">Az.Accounts</span></span>
* <span data-ttu-id="08996-1214">Inaktivera automatisk sparande av kontext när AzureRmContext.json inte är tillgängligt</span><span class="sxs-lookup"><span data-stu-id="08996-1214">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="08996-1215">Uppdatera referensen till Azure Powershell Common till 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="08996-1215">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="08996-1216">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="08996-1216">Az.ApiManagement</span></span>
* <span data-ttu-id="08996-1217">**Get-AzApiManagementApiSchema** Hämtning av Open-Api-schema som är associerat med ett API har åtgärdats   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="08996-1217">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="08996-1218">**New-AzApiManagementProduct** _ och _ *Set-AzApiManagementProduct*\*</span><span class="sxs-lookup"><span data-stu-id="08996-1218">**New-AzApiManagementProduct** _ and _ *Set-AzApiManagementProduct*\*</span></span>
  - <span data-ttu-id="08996-1219">Åtgärda dokumentation för https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="08996-1219">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="08996-1220">**Set-AzApiManagementApi** Exempel för att visa hur ServiceUrl uppdateras med hjälp av cmdleten har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-1220">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08996-1221">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08996-1221">Az.Compute</span></span>
* <span data-ttu-id="08996-1222">Begränsa antalet VM-status till 100 för att undvika begränsning när Get-AzVM -Status utförs utan VM-namn.</span><span class="sxs-lookup"><span data-stu-id="08996-1222">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="08996-1223">Lägg till cmdleten Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="08996-1223">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="08996-1224">Lägg till parametrarna EncryptionType och DiskEncryptionSetId i följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="08996-1224">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="08996-1225">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="08996-1225">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="08996-1226">Lägg till parametern ColocationStatus för cmdleten Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="08996-1226">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="08996-1227">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="08996-1227">Az.DataFactory</span></span>
* <span data-ttu-id="08996-1228">Uppdatera ADF .Net SDK-versionen till 4.7.0</span><span class="sxs-lookup"><span data-stu-id="08996-1228">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="08996-1229">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="08996-1229">Az.DeploymentManager</span></span>
* <span data-ttu-id="08996-1230">Lägger till LIST-åtgärder för resurser</span><span class="sxs-lookup"><span data-stu-id="08996-1230">Adds LIST operations for resources</span></span>
* <span data-ttu-id="08996-1231">Lägger till funktion för att utföra åtgärder för hälsokontrollsteg</span><span class="sxs-lookup"><span data-stu-id="08996-1231">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="08996-1232">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="08996-1232">Az.HDInsight</span></span>
* <span data-ttu-id="08996-1233">Åtgärda dokumentfel för New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="08996-1233">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="08996-1234">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="08996-1234">Az.KeyVault</span></span>
* <span data-ttu-id="08996-1235">Lägg till Name-alias för attributet VaultName så att Remove-AzureKeyVault stämmer överens med New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="08996-1235">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="08996-1236">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08996-1236">Az.Network</span></span>
* <span data-ttu-id="08996-1237">Nytt exempel har lagts till i Set-AzNetworkWatcherConfigFlowLog.md för att demonstrera ett inaktiveringsscenario för Trafikanalys.</span><span class="sxs-lookup"><span data-stu-id="08996-1237">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="08996-1238">Lägg till stöd för att tilldela konfiguration av hanterings-IP till Azure Firewall – ett dedikerat undernät och en offentlig IP som brandväggen använder för dess hanteringstrafik</span><span class="sxs-lookup"><span data-stu-id="08996-1238">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="08996-1239">Cmdleten New-AzFirewall har uppdaterats:</span><span class="sxs-lookup"><span data-stu-id="08996-1239">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="08996-1240">Parametern -ManagementPublicIpAddress (inte obligatorisk) som accepterar ett offentligt IP-adressobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-1240">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="08996-1241">Metoden SetManagementIpConfiguration har lagts till för brandväggsobjekt – kräver ett undernät och en offentlig IP-adress som indata – undernätets namn måste vara ”AzureFirewallManagementSubnet”</span><span class="sxs-lookup"><span data-stu-id="08996-1241">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="08996-1242">Exempel för Get-AzNetworkSecurityGroup har korrigerats så att exempel visas för NSG:er i stället för nätverksgränssnitt.</span><span class="sxs-lookup"><span data-stu-id="08996-1242">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="08996-1243">Ett skrivfel har åtgärdats i kommandot New-AzVpnSite som hindrade kompletteraren för resurs-ID från att fylla i en parameter.</span><span class="sxs-lookup"><span data-stu-id="08996-1243">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="08996-1244">Stöd för Url-konfiguration i åtgärdsuppsättningen för omskrivningsregler i Application Gateway har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-1244">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="08996-1245">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="08996-1245">New cmdlets added:</span></span>
        - <span data-ttu-id="08996-1246">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="08996-1246">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="08996-1247">Cmdletar har uppdaterats med den valfria parametern -UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="08996-1247">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="08996-1248">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="08996-1248">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="08996-1249">Lägg till stöd för resurser för NetworkWatcher ConnectionMonitor version 2</span><span class="sxs-lookup"><span data-stu-id="08996-1249">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="08996-1250">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="08996-1250">Az.PolicyInsights</span></span>
* <span data-ttu-id="08996-1251">Stöd för utvärdering av efterlevnad innan fastställande av vilken resurs som ska åtgärdas</span><span class="sxs-lookup"><span data-stu-id="08996-1251">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="08996-1252">Lägg till parametern ”-ResourceDiscoverMode” för Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="08996-1252">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="08996-1253">Lägg till cmdleten Get-AzPolicyMetadata för att hämta resurser för principmetadata</span><span class="sxs-lookup"><span data-stu-id="08996-1253">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="08996-1254">Get-AzPolicyState och Get-AzPolicyStateSummary för API-versionen 2019-10-01 har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="08996-1254">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="08996-1255">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="08996-1255">Az.RecoveryServices</span></span>
* <span data-ttu-id="08996-1256">Azure Site Recovery-stöd för att ta bort en replikerad disk.</span><span class="sxs-lookup"><span data-stu-id="08996-1256">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="08996-1257">Tillagt Azure Backup-stöd för att lägga till taggar när ett Recovery Services-valv skapas.</span><span class="sxs-lookup"><span data-stu-id="08996-1257">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="08996-1258">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08996-1258">Az.Resources</span></span>
* <span data-ttu-id="08996-1259">Gör -Scope valfritt i cmdletarna \*-AzPolicyAssignment med standardinställning till kontextprenumeration</span><span class="sxs-lookup"><span data-stu-id="08996-1259">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="08996-1260">Lägg till exempel på att skapa ADServicePrincipal med lösenord och nyckelautentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="08996-1260">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="08996-1261">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08996-1261">Az.Sql</span></span>
<span data-ttu-id="08996-1262">Åtgärda cmdleten New-AzSqlDatabaseSecondary så att existensen PartnerDatabaseName kontrolleras i stället för existensen DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="08996-1262">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="08996-1263">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="08996-1263">Az.Storage</span></span>
* <span data-ttu-id="08996-1264">Stöd för angivning av krypteringsnyckeltyp för Tabell/kö i Skapa lagringskonto</span><span class="sxs-lookup"><span data-stu-id="08996-1264">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="08996-1265">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="08996-1265">New-AzStorageAccount</span></span>
* <span data-ttu-id="08996-1266">Visa RequestId när StorageException inte har ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="08996-1266">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="08996-1267">Åtgärda exempel 6 för cmdleten Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="08996-1267">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="08996-1268">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="08996-1268">Az.Websites</span></span>
* <span data-ttu-id="08996-1269">Set-AzWebapp och Set-AzWebappSlot stöder egenskaperna AlwaysOn, MinTls och FtpsState</span><span class="sxs-lookup"><span data-stu-id="08996-1269">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="08996-1270">Åtgärdar problemet där inställning av HttpsOnly samtidigt som AppservicePlan ändrades med det enskilda kommandot Set-AzWebApp återställde HttpsOnly till standardvärdet</span><span class="sxs-lookup"><span data-stu-id="08996-1270">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="08996-1271">3.3.0 – januari 2020</span><span class="sxs-lookup"><span data-stu-id="08996-1271">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="08996-1272">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="08996-1272">Az.Accounts</span></span>
* <span data-ttu-id="08996-1273">Nu stöder Add-AzEnvironment och Set-AzEnvironment parametrarna AzureAttestationServiceEndpointResourceId och AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="08996-1273">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="08996-1274">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="08996-1274">Az.Cdn</span></span>
* <span data-ttu-id="08996-1275">Information om felsvar visas i New-AzCdnEndpoint-cmdleten</span><span class="sxs-lookup"><span data-stu-id="08996-1275">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08996-1276">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08996-1276">Az.Compute</span></span>
* <span data-ttu-id="08996-1277">Set-AzVMCustomScriptExtension-cmdleten har åtgärdats för en virtuell dator med hanterad OD-disk som inte har någon operativsystemprofil.</span><span class="sxs-lookup"><span data-stu-id="08996-1277">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="08996-1278">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="08996-1278">Az.ContainerInstance</span></span>
* <span data-ttu-id="08996-1279">Parameternamn som används med New-AzContainerGroup-exempel har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="08996-1279">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="08996-1280">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="08996-1280">Az.DataBoxEdge</span></span>
* <span data-ttu-id="08996-1281">Cmdleten ”Get-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-1281">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="08996-1282">Hämta gränslagringscontainern</span><span class="sxs-lookup"><span data-stu-id="08996-1282">Get the Edge Storage Container</span></span>
* <span data-ttu-id="08996-1283">Cmdleten ”New-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-1283">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="08996-1284">Skapa en ny gränslagringscontainer</span><span class="sxs-lookup"><span data-stu-id="08996-1284">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="08996-1285">Cmdleten ”Remove-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-1285">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="08996-1286">Ta bort gränslagringscontainern</span><span class="sxs-lookup"><span data-stu-id="08996-1286">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="08996-1287">Cmdleten ”Invoke-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-1287">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="08996-1288">Anropa åtgärd för att uppdatera data i gränslagringscontainer</span><span class="sxs-lookup"><span data-stu-id="08996-1288">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="08996-1289">Cmdleten ”Get-AzDataBoxEdgeStorageAccount” har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-1289">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="08996-1290">Hämta gränslagringskontot</span><span class="sxs-lookup"><span data-stu-id="08996-1290">Get the Edge Storage Account</span></span>
* <span data-ttu-id="08996-1291">Cmdleten ”New-AzDataBoxEdgeStorageAccount” har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-1291">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="08996-1292">Skapa ett nytt gränslagringskonto</span><span class="sxs-lookup"><span data-stu-id="08996-1292">Create new Edge Storage Account</span></span>
* <span data-ttu-id="08996-1293">Cmdleten ”Remove-AzDataBoxEdgeStorageAccount” har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-1293">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="08996-1294">Ta bort gränslagringskontot</span><span class="sxs-lookup"><span data-stu-id="08996-1294">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="08996-1295">Anropa cmdleten ”Invoke-AzDataBoxEdgeShare”</span><span class="sxs-lookup"><span data-stu-id="08996-1295">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="08996-1296">Anropa åtgärd för att uppdatera resursdata</span><span class="sxs-lookup"><span data-stu-id="08996-1296">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="08996-1297">Cmdleten ”Set-AzDataBoxEdgeStorageAccountCredential” har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-1297">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="08996-1298">Ange autentiseringsuppgifter för az databoxedge-lagringskonto</span><span class="sxs-lookup"><span data-stu-id="08996-1298">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="08996-1299">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="08996-1299">Az.DataFactory</span></span>
* <span data-ttu-id="08996-1300">Lägg till AutoUpdateETA-, LatestVersion-, PushedVersion-, TaskQueueId- och VersionStatus-egenskaper för Get-AzDataFactoryV2IntegrationRuntime-cmd</span><span class="sxs-lookup"><span data-stu-id="08996-1300">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="08996-1301">Uppdatera ADF .Net SDK-versionen till 4.6.0</span><span class="sxs-lookup"><span data-stu-id="08996-1301">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="08996-1302">Lägg till parametern ”PublicIPs” för ”Set-AzureRmDataFactoryV2IntegrationRuntime”-cmd så att Azure-SSIS IR kan skapas med statiska offentliga IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="08996-1302">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="08996-1303">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="08996-1303">Az.DevTestLabs</span></span>
* <span data-ttu-id="08996-1304">Ta bort den brutna länken i Get-AzDtlAllowedVMSizesPolicy.md</span><span class="sxs-lookup"><span data-stu-id="08996-1304">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="08996-1305">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="08996-1305">Az.EventHub</span></span>
* <span data-ttu-id="08996-1306">Korrigering av problem 10634: Åtgärda referensen till null-objekt för eventhubnamespace-borttagning</span><span class="sxs-lookup"><span data-stu-id="08996-1306">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="08996-1307">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="08996-1307">Az.HDInsight</span></span>
* <span data-ttu-id="08996-1308">Åtgärda Invoke-AzHDInsightHiveJob.md-fel.</span><span class="sxs-lookup"><span data-stu-id="08996-1308">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="08996-1309">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="08996-1309">Az.MachineLearning</span></span>
* <span data-ttu-id="08996-1310">Nedanstående cmdletar har tagits bort eftersom MachineLearningCompute inte längre är tillgängligt</span><span class="sxs-lookup"><span data-stu-id="08996-1310">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="08996-1311">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="08996-1311">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="08996-1312">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="08996-1312">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="08996-1313">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="08996-1313">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="08996-1314">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="08996-1314">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="08996-1315">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="08996-1315">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="08996-1316">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="08996-1316">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="08996-1317">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="08996-1317">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="08996-1318">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08996-1318">Az.Network</span></span>
* <span data-ttu-id="08996-1319">Uppgradera beroende av Microsoft.Azure.Management.Sql från 1.36-preview till 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="08996-1319">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="08996-1320">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="08996-1320">Az.RecoveryServices</span></span>
* <span data-ttu-id="08996-1321">Ändrat Azure Site Recovery-stöd för krypterade vilande data på virtuella datorer med hanterade diskar med kundhanterade nycklar för Azure till Azure-providern.</span><span class="sxs-lookup"><span data-stu-id="08996-1321">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="08996-1322">Azure Site Recovery-stöd för att ange ID för diskkrypteringsuppsättning som valfri inmatning för aktivering av skydd för VMware till Azure.</span><span class="sxs-lookup"><span data-stu-id="08996-1322">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="08996-1323">Azure Site Recovery-stöd för att ange ID för diskkrypteringsuppsättning som valfri inmatning på disknivå för aktivering av skydd för VMware till Azure.</span><span class="sxs-lookup"><span data-stu-id="08996-1323">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="08996-1324">Azure Site Recovery-stöd för att uppdatera replikeringsskyddade objekt med mappning för diskkrypteringsuppsättning för HyperV till Azure.</span><span class="sxs-lookup"><span data-stu-id="08996-1324">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="08996-1325">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08996-1325">Az.Resources</span></span>
* <span data-ttu-id="08996-1326">Åtgärda ett fel i hjälpdokument för ”Remove-AzTag”.</span><span class="sxs-lookup"><span data-stu-id="08996-1326">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="08996-1327">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08996-1327">Az.Sql</span></span>
* <span data-ttu-id="08996-1328">Åtgärda funktioner i cmdletar för att ange baslinjen för sårbarhetsbedömning för arbete med huvuddatabasen för Azure-databasen och begränsa den för systemdatabaser på hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="08996-1328">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="08996-1329">Åtgärda ett fel när en redundansgrupp för en SQL-instans skapas</span><span class="sxs-lookup"><span data-stu-id="08996-1329">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="08996-1330">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="08996-1330">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="08996-1331">Lägg till DR som en ny giltig licenstyp</span><span class="sxs-lookup"><span data-stu-id="08996-1331">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="08996-1332">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="08996-1332">Az.Storage</span></span>
* <span data-ttu-id="08996-1333">Lägg till varningsmeddelande om icke-bakåtkompatibel ändring för DefaultAction-värdeändring i en framtida version</span><span class="sxs-lookup"><span data-stu-id="08996-1333">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="08996-1334">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="08996-1334">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="08996-1335">Stöd för att hämta lagringskontots senaste synkroniseringstid genom att köra get-AzureRMStorageAccount med parametern -IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="08996-1335">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="08996-1336">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="08996-1336">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="08996-1337">3.2.0 – December 2019</span><span class="sxs-lookup"><span data-stu-id="08996-1337">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="08996-1338">Allmänt</span><span class="sxs-lookup"><span data-stu-id="08996-1338">General</span></span>
* <span data-ttu-id="08996-1339">Uppdatera referenser i .psd1 för att använda relativa sökvägar för alla moduler</span><span class="sxs-lookup"><span data-stu-id="08996-1339">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="08996-1340">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="08996-1340">Az.Accounts</span></span>
* <span data-ttu-id="08996-1341">Ange rätt UserAgent för telemetri på klientsidan för Az 4.0 preview</span><span class="sxs-lookup"><span data-stu-id="08996-1341">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="08996-1342">Visa användarvänligt felmeddelande när kontexten är null i Az 4.0 preview</span><span class="sxs-lookup"><span data-stu-id="08996-1342">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="08996-1343">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="08996-1343">Az.Batch</span></span>
* <span data-ttu-id="08996-1344">Korrigera problem [#10602](https://github.com/Azure/azure-powershell/issues/10602), där **New-AzBatchPool** skickade VirtualMachineConfiguration.ContainerConfiguration eller VirtualMachineConfiguration.DataDisks på ett felaktigt sätt till servern.</span><span class="sxs-lookup"><span data-stu-id="08996-1344">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="08996-1345">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="08996-1345">Az.DataFactory</span></span>
* <span data-ttu-id="08996-1346">Uppdatera ADF .Net SDK-versionen till 4.5.0</span><span class="sxs-lookup"><span data-stu-id="08996-1346">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="08996-1347">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="08996-1347">Az.FrontDoor</span></span>
* <span data-ttu-id="08996-1348">Stöd har lagts till för undantag för hanterade regler för brandväggen för webbaserade program</span><span class="sxs-lookup"><span data-stu-id="08996-1348">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="08996-1349">Lägg till SocketAddr för automatisk komplettering</span><span class="sxs-lookup"><span data-stu-id="08996-1349">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="08996-1350">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="08996-1350">Az.HealthcareApis</span></span>
* <span data-ttu-id="08996-1351">Undantagshantering</span><span class="sxs-lookup"><span data-stu-id="08996-1351">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="08996-1352">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="08996-1352">Az.KeyVault</span></span>
* <span data-ttu-id="08996-1353">Åtgärdat fel vid åtkomst av värde som kanske inte har angetts</span><span class="sxs-lookup"><span data-stu-id="08996-1353">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="08996-1354">Hantering av ECC-certifikat (Elliptic Curve Cryptography)</span><span class="sxs-lookup"><span data-stu-id="08996-1354">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="08996-1355">Stöd har lagts till för att ange kurvan för certifikatprinciper</span><span class="sxs-lookup"><span data-stu-id="08996-1355">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="08996-1356">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="08996-1356">Az.Monitor</span></span>
* <span data-ttu-id="08996-1357">Lägger till valfritt argument i kommandot Lägg till diagnostikinställningar.</span><span class="sxs-lookup"><span data-stu-id="08996-1357">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="08996-1358">Ett växelargument som om det finns visar att exporten till Log Analytics måste ske till ett fast schema (kallas även</span><span class="sxs-lookup"><span data-stu-id="08996-1358">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="08996-1359">dedikerad, datatyp)</span><span class="sxs-lookup"><span data-stu-id="08996-1359">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="08996-1360">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08996-1360">Az.Network</span></span>
* <span data-ttu-id="08996-1361">Stöd för IpGroups i program-, NAT- och nätverksregler för Azure Firewall.</span><span class="sxs-lookup"><span data-stu-id="08996-1361">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="08996-1362">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08996-1362">Az.Resources</span></span>
* <span data-ttu-id="08996-1363">Åtgärda ett problem där malldistributionen inte kan läsa en mallparameter om dess namn står i konflikt med ett inbyggt parameternamn.</span><span class="sxs-lookup"><span data-stu-id="08996-1363">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="08996-1364">Uppdaterade princip-cmdletar för att använda den nya API-versionen 2019-09-01 som introducerar grupperingsstöd inom principuppsättningsdefinitioner.</span><span class="sxs-lookup"><span data-stu-id="08996-1364">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="08996-1365">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08996-1365">Az.Sql</span></span>
* <span data-ttu-id="08996-1366">Uppgraderad funktion för att skapa lagring i automatisk aktivering av sårbarhetsbedömning till StorageV2</span><span class="sxs-lookup"><span data-stu-id="08996-1366">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="08996-1367">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="08996-1367">Az.Storage</span></span>
* <span data-ttu-id="08996-1368">Stöd för generering av blob/container-identitetsbaserad SAS-token med lagringskontextbaserad på OAuth-autentisering</span><span class="sxs-lookup"><span data-stu-id="08996-1368">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="08996-1369">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="08996-1369">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="08996-1370">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="08996-1370">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="08996-1371">Stöd för återkallning av användardelegeringsnycklar för lagringskonto för att återkalla alla SAS-token</span><span class="sxs-lookup"><span data-stu-id="08996-1371">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="08996-1372">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="08996-1372">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="08996-1373">Uppgradera till Microsoft.Azure.Management.Storage 14.2.0 för att stödja den nya API-versionen 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="08996-1373">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="08996-1374">Stöd för QuotaGiB (resurskvot i Gibibye) för värden över 5120 i hanteringsplanet för cmdletar för filresurser och parameteraliaset. Quota har också lagts till för parametern ”QuotaGiB”.</span><span class="sxs-lookup"><span data-stu-id="08996-1374">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="08996-1375">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="08996-1375">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="08996-1376">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="08996-1376">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="08996-1377">Lägg till parameteraliaset QuotaGiB i parametern Quota</span><span class="sxs-lookup"><span data-stu-id="08996-1377">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="08996-1378">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="08996-1378">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="08996-1379">Åtgärda problemet att Set-AzStorageContainerAcl kan rensa den lagrade åtkomstprincipen</span><span class="sxs-lookup"><span data-stu-id="08996-1379">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="08996-1380">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="08996-1380">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="08996-1381">3.1.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="08996-1381">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="08996-1382">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="08996-1382">Highlights since the last major release</span></span>
* <span data-ttu-id="08996-1383">Az.DataBoxEdge 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="08996-1383">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="08996-1384">Az.SqlVirtualMachine 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="08996-1384">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08996-1385">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08996-1385">Az.Compute</span></span>
* <span data-ttu-id="08996-1386">Funktion för att använda en virtuell dator igen</span><span class="sxs-lookup"><span data-stu-id="08996-1386">VM Reapply feature</span></span>
    - <span data-ttu-id="08996-1387">Lägg till parameter för att använda igen till cmdleten Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="08996-1387">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="08996-1388">Funktionen AutomaticRepairs i VM-skalningsuppsättningar:</span><span class="sxs-lookup"><span data-stu-id="08996-1388">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="08996-1389">Lägg till parametrarna EnableAutomaticRepair, AutomaticRepairGracePeriod och AutomaticRepairMaxInstanceRepairsPercent till följande cmdletar:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="08996-1389">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="08996-1390">Stöd för galleriavbildningar i flera klientorganisationer för New-AzVM</span><span class="sxs-lookup"><span data-stu-id="08996-1390">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="08996-1391">Lägg till "Spot" till argumentslutföraren i prioritetsparametern i cmdletarna New-AzVM, New-AzVMConfig och New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="08996-1391">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="08996-1392">Lägg till parametrarna DiskIOPSReadWrite och DiskMBpsReadWrite till cmdleten Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="08996-1392">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="08996-1393">Ändra parametern SourceImageId för cmdleten New-AzGalleryImageVersion till valfri</span><span class="sxs-lookup"><span data-stu-id="08996-1393">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="08996-1394">Lägg till parametrarna OSDiskImage och DataDiskImage till cmdleten New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="08996-1394">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="08996-1395">Lägg till parametern HyperVGeneration till cmdleten New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="08996-1395">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="08996-1396">Lägg till parametern SkipExtensionsOnOverprovisionedVMs till cmdletarna New-AzVmss, New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="08996-1396">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="08996-1397">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="08996-1397">Az.DataBoxEdge</span></span>
* <span data-ttu-id="08996-1398">Cmdleten `Get-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-1398">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="08996-1399">Hämta ordning</span><span class="sxs-lookup"><span data-stu-id="08996-1399">Get the Order</span></span>
* <span data-ttu-id="08996-1400">Cmdleten `New-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-1400">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="08996-1401">Skapa ny ordning</span><span class="sxs-lookup"><span data-stu-id="08996-1401">Create new Order</span></span>
* <span data-ttu-id="08996-1402">Cmdleten `Remove-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-1402">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="08996-1403">Ta bort ordning</span><span class="sxs-lookup"><span data-stu-id="08996-1403">Remove the Order</span></span>
* <span data-ttu-id="08996-1404">Cmdleten `New-AzDataBoxEdgeShare` har ändrats</span><span class="sxs-lookup"><span data-stu-id="08996-1404">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="08996-1405">Nu skapas lokal filresurs</span><span class="sxs-lookup"><span data-stu-id="08996-1405">Now creates Local Share</span></span>
* <span data-ttu-id="08996-1406">Cmdleten `Set-AzDataBoxEdgeRole` har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-1406">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="08996-1407">Nu kan IotRole mappas till filresursen</span><span class="sxs-lookup"><span data-stu-id="08996-1407">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="08996-1408">Cmdleten `Invoke-AzDataBoxEdgeDevice` har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-1408">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="08996-1409">Anropa genomsökningsuppdatering, ladda ned uppdatering, installera uppdateringar på enheten</span><span class="sxs-lookup"><span data-stu-id="08996-1409">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="08996-1410">Cmdleten `Get-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-1410">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="08996-1411">Hämtar information om utlösare</span><span class="sxs-lookup"><span data-stu-id="08996-1411">Gets the information about Triggers</span></span>
* <span data-ttu-id="08996-1412">Cmdleten `New-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-1412">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="08996-1413">Skapa nya utlösare</span><span class="sxs-lookup"><span data-stu-id="08996-1413">Create new Triggers</span></span>
* <span data-ttu-id="08996-1414">Cmdleten `Remove-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-1414">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="08996-1415">Ta bort utlösare</span><span class="sxs-lookup"><span data-stu-id="08996-1415">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="08996-1416">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="08996-1416">Az.DataFactory</span></span>
* <span data-ttu-id="08996-1417">Uppdatera ADF .Net SDK-versionen till 4.4.0</span><span class="sxs-lookup"><span data-stu-id="08996-1417">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="08996-1418">Lägg till parametern ExpressCustomSetup för kommandot Set-AzureRmDataFactoryV2IntegrationRuntime för att aktivera installationskonfigurationer och komponenter från tredje part utan anpassat konfigurationsskript.</span><span class="sxs-lookup"><span data-stu-id="08996-1418">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="08996-1419">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="08996-1419">Az.DataLakeStore</span></span>
* <span data-ttu-id="08996-1420">Uppdatera dokumentation för Get-AzDataLakeStoreDeletedItem och Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="08996-1420">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="08996-1421">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="08996-1421">Az.EventHub</span></span>
* <span data-ttu-id="08996-1422">Korrigering av problem #10301: Korrigera datumformat för SAS-token</span><span class="sxs-lookup"><span data-stu-id="08996-1422">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="08996-1423">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="08996-1423">Az.FrontDoor</span></span>
* <span data-ttu-id="08996-1424">Lägg till parametern MinimumTlsVersion till Enable-AzFrontDoorCustomDomainHttps och New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="08996-1424">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="08996-1425">Lägg till parametrarna HealthProbeMethod och EnabledState till New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="08996-1425">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="08996-1426">Lägg till en ny cmdlet för att skapa BackendPoolsSettings-objekt som passar i skapande/uppdatering av Front Door</span><span class="sxs-lookup"><span data-stu-id="08996-1426">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="08996-1427">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="08996-1427">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="08996-1428">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08996-1428">Az.Network</span></span>
* <span data-ttu-id="08996-1429">Ändra alternativexemplen Start-AzVirtualNetworkGatewayConnectionPacketCapture.md och Start-AzVirtualnetworkGatewayPacketCapture.md för FilterData.</span><span class="sxs-lookup"><span data-stu-id="08996-1429">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="08996-1430">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="08996-1430">Az.PrivateDns</span></span>
* <span data-ttu-id="08996-1431">Uppdaterade PrivateDns .NET SDK till version 1.0.0</span><span class="sxs-lookup"><span data-stu-id="08996-1431">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="08996-1432">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="08996-1432">Az.RecoveryServices</span></span>
* <span data-ttu-id="08996-1433">Stöd för att välja disktyp vid aktivering av skydd i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="08996-1433">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="08996-1434">Korrigering av bugg för åtgärdsredigering av återställningsplan i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="08996-1434">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="08996-1435">Återställningsstöd för att godkänna filestream-databaser i Azure Backup SQL.</span><span class="sxs-lookup"><span data-stu-id="08996-1435">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="08996-1436">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="08996-1436">Az.RedisCache</span></span>
* <span data-ttu-id="08996-1437">Parametern MinimumTlsVersion har lagts till i cmdletarna New-AzRedisCache och Set-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="08996-1437">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="08996-1438">Dessutom har MinimumTlsVersion lagts till i utdata för cmdleten Get-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="08996-1438">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="08996-1439">Verifiering har lagts till på parametern -Size i cmdletarna Set-AzRedisCache och New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="08996-1439">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="08996-1440">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08996-1440">Az.Resources</span></span>
- <span data-ttu-id="08996-1441">Uppdaterade policy-cmdletar för att använda den nya API-versionen 2019-06-01 som har en ny EnforcementMode-egenskap i policytilldelningen.</span><span class="sxs-lookup"><span data-stu-id="08996-1441">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="08996-1442">Uppdaterade hjälpexempel för skapandet av policydefinition</span><span class="sxs-lookup"><span data-stu-id="08996-1442">Updated create policy definition help example</span></span>
- <span data-ttu-id="08996-1443">Åtgärda bugg i Remove-AZADServicePrincipal -ServicePrincipalName, utlös null-referens när tjänstens huvudnamn inte hittas.</span><span class="sxs-lookup"><span data-stu-id="08996-1443">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="08996-1444">Åtgärda bugg i New-AZADServicePrincipal, utlös null-referens när klientorganisationen inte har någon prenumeration.</span><span class="sxs-lookup"><span data-stu-id="08996-1444">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="08996-1445">Ändra New-AzAdServicePrincipal för att endast lägga till autentiseringsuppgifter för det associerade programmet.</span><span class="sxs-lookup"><span data-stu-id="08996-1445">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="08996-1446">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08996-1446">Az.Sql</span></span>
* <span data-ttu-id="08996-1447">Stöd har lagts till för databasen ReadReplicaCount.</span><span class="sxs-lookup"><span data-stu-id="08996-1447">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="08996-1448">Korrigerade Set-AzSqlDatabase när zonredundans inte har angetts</span><span class="sxs-lookup"><span data-stu-id="08996-1448">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="08996-1449">3.0.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="08996-1449">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="08996-1450">Allmänt</span><span class="sxs-lookup"><span data-stu-id="08996-1450">General</span></span>
* <span data-ttu-id="08996-1451">Az. PrivateDns 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="08996-1451">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="08996-1452">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="08996-1452">Az.Accounts</span></span>
* <span data-ttu-id="08996-1453">Lägg till ett utfasningsmeddelande för aliaset Resolve-error.</span><span class="sxs-lookup"><span data-stu-id="08996-1453">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="08996-1454">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="08996-1454">Az.Advisor</span></span>
* <span data-ttu-id="08996-1455">Den nya kategorin Operational Excellence har lagts till i cmdleten Get-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="08996-1455">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="08996-1456">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="08996-1456">Az.Batch</span></span>
* <span data-ttu-id="08996-1457">`CoreQuota` på `BatchAccountContext` har bytt namn till `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="08996-1457">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="08996-1458">Det finns även en ny `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="08996-1458">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="08996-1459">Detta påverkar **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="08996-1459">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="08996-1460">**New-AzBatchTask** `-ResourceFile`-parametern tar nu en samling `PSResourceFile`-objekt som kan skapas med hjälp av den nya cmdleten **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="08996-1460">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="08996-1461">Ny **New-AzBatchResourceFile**-cmdlet för att skapa `PSResourceFile`-objekt.</span><span class="sxs-lookup"><span data-stu-id="08996-1461">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="08996-1462">Dessa kan tillhandahållas till **New-AzBatchTask** på `-ResourceFile`-parametern.</span><span class="sxs-lookup"><span data-stu-id="08996-1462">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="08996-1463">Detta stöder två nya typer av resursfiler förutom det befintliga sättet med `HttpUrl`:</span><span class="sxs-lookup"><span data-stu-id="08996-1463">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="08996-1464">`AutoStorageContainerName`-baserade resursfiler laddar ned en hel container för automatisk lagring till Batch-noden.</span><span class="sxs-lookup"><span data-stu-id="08996-1464">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="08996-1465">`StorageContainerUrl`-baserade resursfiler laddar ned containern som anges i webbadressen till Batch-noden.</span><span class="sxs-lookup"><span data-stu-id="08996-1465">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="08996-1466">Tog bort egenskapen `ApplicationPackages` för `PSApplication` som returnerades av **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="08996-1466">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="08996-1467">Specifika paket i ett program kan nu hämtas med hjälp av **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="08996-1467">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="08996-1468">Till exempel: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="08996-1468">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="08996-1469">Bytt namn på `ApplicationId` till `ApplicationName` på **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** och **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="08996-1469">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="08996-1470">`ApplicationId` är nu ett alias för `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="08996-1470">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="08996-1471">Ny `PSWindowsUserConfiguration`-egenskap till `PSUserAccount` lades till.</span><span class="sxs-lookup"><span data-stu-id="08996-1471">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="08996-1472">Bytte namn på `Version` till `Name` på `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="08996-1472">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="08996-1473">Bytte namn på `BlobSource` till `HttpUrl` på `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="08996-1473">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="08996-1474">Tog bort egenskapen `OSDisk` från `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="08996-1474">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="08996-1475">Tog bort **Set-AzBatchPoolOSVersion**.</span><span class="sxs-lookup"><span data-stu-id="08996-1475">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="08996-1476">Den här åtgärden stöds inte längre.</span><span class="sxs-lookup"><span data-stu-id="08996-1476">This operation is no longer supported.</span></span>
* <span data-ttu-id="08996-1477">`TargetOSVersion` har tagits bort från `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="08996-1477">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="08996-1478">Bytte namn på `CurrentOSVersion` till `OSVersion` på `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="08996-1478">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="08996-1479">`DataEgressGiB` och `DataIngressGiB` har tagits bort från `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="08996-1479">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="08996-1480">Tog bort **Get-AzBatchNodeAgentSku** och ersatte det med **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="08996-1480">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="08996-1481">**Get-AzBatchSupportedImage** returnerar samma data som **Get-AzBatchNodeAgentSku** men i ett mer användarvänligt format.</span><span class="sxs-lookup"><span data-stu-id="08996-1481">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="08996-1482">Nya icke-verifierade avbildningar returneras nu också.</span><span class="sxs-lookup"><span data-stu-id="08996-1482">New non-verified images are also now returned.</span></span> <span data-ttu-id="08996-1483">Ytterligare information om `Capabilities` och `BatchSupportEndOfLife` för varje avbildning inkluderas också.</span><span class="sxs-lookup"><span data-stu-id="08996-1483">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="08996-1484">Lade till möjlighet att montera fjärrfilsystem på varje nod i en pool via den nya parametern `MountConfiguration` för **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="08996-1484">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="08996-1485">Har nu stöd för nätverkssäkerhetsregler som blockerar nätverksåtkomst till en pool baserat på källportens trafik.</span><span class="sxs-lookup"><span data-stu-id="08996-1485">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="08996-1486">Detta görs via egenskapen `SourcePortRanges` på `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="08996-1486">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="08996-1487">När du kör en container stöder nu Batch körningen av uppgiften i arbetskatalogen för containern eller i arbetskatalogen för Batch-uppgiften.</span><span class="sxs-lookup"><span data-stu-id="08996-1487">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="08996-1488">Detta styrs av egenskapen `WorkingDirectory` på `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="08996-1488">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="08996-1489">Lade till en funktion för att ange en samling av offentliga IP-adresser på `PSNetworkConfiguration` via den nya egenskapen `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="08996-1489">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="08996-1490">Detta garanterar att noderna i poolen har en IP-adress från listan över IP-adresser som tillhandahållits av användare.</span><span class="sxs-lookup"><span data-stu-id="08996-1490">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="08996-1491">Om inget värde anges är standardvärdet för `WaitForSuccess` på `PSSTartTask` nu `$True` (var tidigare `$False`).</span><span class="sxs-lookup"><span data-stu-id="08996-1491">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="08996-1492">Om inget värde anges är standardvärdet för `Scope` på `PSAutoUserSpecification` nu `Pool` (var tidigare `Task` på Windows och `Pool` på Linux).</span><span class="sxs-lookup"><span data-stu-id="08996-1492">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="08996-1493">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="08996-1493">Az.Cdn</span></span>
* <span data-ttu-id="08996-1494">Introducerade UrlRewriteAction och CacheKeyQueryStringAction till RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="08996-1494">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="08996-1495">Åtgärdade flera buggar, som saknade indata för ”väljare” i cmdleten New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="08996-1495">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08996-1496">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08996-1496">Az.Compute</span></span>
* <span data-ttu-id="08996-1497">Funktion för diskkrypteringsuppsättning</span><span class="sxs-lookup"><span data-stu-id="08996-1497">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="08996-1498">Nya cmdletar:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="08996-1498">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="08996-1499">Parametern DiskEncryptionSetId har lagts till i följande cmdletar:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="08996-1499">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="08996-1500">Parametrarna DiskEncryptionSetId och EncryptionType har lagts till i följande cmdletar:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="08996-1500">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="08996-1501">Lägg till parametern PublicIPAddressVersion i New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="08996-1501">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="08996-1502">Flytta FileUris för anpassat skripttillägg från offentlig inställning till skyddad inställning</span><span class="sxs-lookup"><span data-stu-id="08996-1502">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="08996-1503">Lägg till ScaleInPolicy i cmdletarna New-AzVmss, New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="08996-1503">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="08996-1504">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="08996-1504">Breaking changes</span></span>
    - <span data-ttu-id="08996-1505">Parametern UploadSizeInBytes används istället för DiskSizeGB för New-AzDiskConfig när CreateOption är Uppladdning</span><span class="sxs-lookup"><span data-stu-id="08996-1505">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="08996-1506">PublishingProfile.Source.ManagedImage.Id ersätts med StorageProfile.Source.Id i objektet GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="08996-1506">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="08996-1507">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="08996-1507">Az.DataFactory</span></span>
* <span data-ttu-id="08996-1508">Uppdatera ADF .Net SDK-versionen till 4.3.0</span><span class="sxs-lookup"><span data-stu-id="08996-1508">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="08996-1509">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="08996-1509">Az.DataLakeStore</span></span>
* <span data-ttu-id="08996-1510">Uppdatera ADLS SDK-version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) innehåller följande korrigeringar</span><span class="sxs-lookup"><span data-stu-id="08996-1510">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="08996-1511">Undvik att utlösa undantag när det inte går att deserialisera creationtime för inmatning av papperskorg eller katalog.</span><span class="sxs-lookup"><span data-stu-id="08996-1511">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="08996-1512">Gör inställning tillgänglig per tidsgräns för förfrågan i adlsclient</span><span class="sxs-lookup"><span data-stu-id="08996-1512">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="08996-1513">Korrigera överföringen av ursprunglig syncflag för badoffset-återställning</span><span class="sxs-lookup"><span data-stu-id="08996-1513">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="08996-1514">Korrigera EnumerateDirectory för att hämta fortsättningstoken när svar har kontrollerats</span><span class="sxs-lookup"><span data-stu-id="08996-1514">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="08996-1515">Korrigera bugg i Concat</span><span class="sxs-lookup"><span data-stu-id="08996-1515">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="08996-1516">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="08996-1516">Az.FrontDoor</span></span>
* <span data-ttu-id="08996-1517">Åtgärdade diverse stavfel i modul</span><span class="sxs-lookup"><span data-stu-id="08996-1517">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="08996-1518">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="08996-1518">Az.HDInsight</span></span>
* <span data-ttu-id="08996-1519">Korrigerade buggen att kunder får felet ”inte en giltig Base-64-sträng” vid användning av Get-AzHDInsightCluster för att hämta klustret med ADLSGen1-lagring.</span><span class="sxs-lookup"><span data-stu-id="08996-1519">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="08996-1520">Lägg till en parameter med namnet ”ApplicationId” i de tre cmdletarna Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig och New-AzHDInsightCluster så att kunden kan tillhandahålla tjänstens huvudnamn för program-ID för åtkomst till Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="08996-1520">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="08996-1521">Ändrade Microsoft.Azure.Management.HDInsight från 2.1.0 till 5.1.0</span><span class="sxs-lookup"><span data-stu-id="08996-1521">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="08996-1522">Fem cmdletar har tagits bort:</span><span class="sxs-lookup"><span data-stu-id="08996-1522">Removed five cmdlets:</span></span>
    - <span data-ttu-id="08996-1523">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="08996-1523">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="08996-1524">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="08996-1524">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="08996-1525">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="08996-1525">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="08996-1526">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="08996-1526">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="08996-1527">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="08996-1527">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="08996-1528">Tre cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="08996-1528">Added three cmdlets:</span></span>
    - <span data-ttu-id="08996-1529">Get-AzHDInsightMonitoring som ersätter Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="08996-1529">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="08996-1530">Enable-AzHDInsightMonitoring som ersätter Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="08996-1530">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="08996-1531">Disable-AzHDInsightMonitoring som ersätter Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="08996-1531">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="08996-1532">Korrigerade cmdleten Get-AzHDInsightProperties för att stödja hämtning av funktionsinformation från en viss plats.</span><span class="sxs-lookup"><span data-stu-id="08996-1532">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="08996-1533">Parameteruppsättningarna (Spark1 och Spark2) har tagits bort från Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="08996-1533">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="08996-1534">Lägg till exempel för cmdleten Add-AzHDInsightSecurityProfile till hjälpdokumenten.</span><span class="sxs-lookup"><span data-stu-id="08996-1534">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="08996-1535">Ändrade utdatatyp för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="08996-1535">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="08996-1536">Ändrade utdatatyp för Get-AzHDInsightProperties från CapabilitiesResponse till AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="08996-1536">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="08996-1537">Ändrade utdatatyp för Remove-AzHDInsightCluster från ClusterGetResponse till bool.</span><span class="sxs-lookup"><span data-stu-id="08996-1537">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="08996-1538">Ändrade utdatatyp för Set-AzHDInsightGatewaySettings HttpConnectivitySettings till GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="08996-1538">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="08996-1539">Lade till testfall för vissa scenarier.</span><span class="sxs-lookup"><span data-stu-id="08996-1539">Added some scenario test cases.</span></span>
* <span data-ttu-id="08996-1540">Ta bort vissa alias: Add-AzHDInsightConfigValues, Get-AzHDInsightProperties.</span><span class="sxs-lookup"><span data-stu-id="08996-1540">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="08996-1541">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="08996-1541">Az.IotHub</span></span>
* <span data-ttu-id="08996-1542">Icke-bakåtkompatibla ändringar:</span><span class="sxs-lookup"><span data-stu-id="08996-1542">Breaking changes:</span></span>
    - <span data-ttu-id="08996-1543">Cmdleten Add-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="08996-1543">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="08996-1544">Parameteruppsättningen __AllParameterSets för cmdleten Add-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="08996-1544">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="08996-1545">Cmdleten Get-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="08996-1545">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="08996-1546">Parameteruppsättningen __AllParameterSets för cmdleten Get-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="08996-1546">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="08996-1547">Egenskapen OperationsMonitoringProperties av typen Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="08996-1547">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="08996-1548">Egenskapen OperationsMonitoringProperties av typen Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="08996-1548">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="08996-1549">Cmdleten New-AzIotHubExportDevice stöder inte längre aliaset New-AzIotHubExportDevices.</span><span class="sxs-lookup"><span data-stu-id="08996-1549">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="08996-1550">Cmdleten New-AzIotHubImportDevice stöder inte längre aliaset New-AzIotHubImportDevices.</span><span class="sxs-lookup"><span data-stu-id="08996-1550">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="08996-1551">Cmdleten Remove-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="08996-1551">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="08996-1552">Parameteruppsättningen __AllParameterSets för cmdleten Remove-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="08996-1552">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="08996-1553">Cmdleten Set-AzIotHub har inte längre stöd för parametern OperationsMonitoringProperties och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="08996-1553">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="08996-1554">Parameteruppsättningen UpdateOperationsMonitoringProperties för cmdleten Set-AzIotHub har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="08996-1554">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="08996-1555">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="08996-1555">Az.RecoveryServices</span></span>
* <span data-ttu-id="08996-1556">Azure Site Recovery-stöd för att konfigurera nätverksresurser som NSG, offentliga IP-adresser och interna lastbalanserare för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="08996-1556">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="08996-1557">Azure Site Recovery-stöd för att skriva till hanterad disk för vMWare till Azure.</span><span class="sxs-lookup"><span data-stu-id="08996-1557">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="08996-1558">Azure Site Recovery-stöd för NIC-reduktion för vMWare till Azure.</span><span class="sxs-lookup"><span data-stu-id="08996-1558">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="08996-1559">Azure Site Recovery-stöd för accelererat nätverk för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="08996-1559">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="08996-1560">Azure Site Recovery-stöd för automatisk uppdatering av agent för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="08996-1560">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="08996-1561">Azure Site Recovery-stöd för Standard SSD för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="08996-1561">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="08996-1562">Azure Site Recovery-stöd för tvåstegskryptering i Azure Disk Encryption för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="08996-1562">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="08996-1563">Azure Site Recovery-stöd för att skydda nyligen tillagda diskar för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="08996-1563">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="08996-1564">En funktion för mjuk borttagning av virtuella datorer samt tester för mjuk borttagning har tagits bort</span><span class="sxs-lookup"><span data-stu-id="08996-1564">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="08996-1565">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08996-1565">Az.Resources</span></span>
* <span data-ttu-id="08996-1566">Uppdatera beroendesammansättning för Microsoft.Extensions.Caching.Memory från 1.1.1 till 2.2</span><span class="sxs-lookup"><span data-stu-id="08996-1566">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="08996-1567">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08996-1567">Az.Network</span></span>
* <span data-ttu-id="08996-1568">Ändra alla cmdletar för PrivateEndpointConnection så att de stöder generiska tjänstleverantörer.</span><span class="sxs-lookup"><span data-stu-id="08996-1568">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="08996-1569">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="08996-1569">Updated cmdlet:</span></span>
        - <span data-ttu-id="08996-1570">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="08996-1570">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="08996-1571">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="08996-1571">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="08996-1572">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="08996-1572">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="08996-1573">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="08996-1573">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="08996-1574">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="08996-1574">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="08996-1575">Lägg till ny cmdlet för PrivateLinkResource så att det också stöder generiska tjänstleverantörer.</span><span class="sxs-lookup"><span data-stu-id="08996-1575">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="08996-1576">Ny cmdlet:</span><span class="sxs-lookup"><span data-stu-id="08996-1576">New cmdlet:</span></span>
        - <span data-ttu-id="08996-1577">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="08996-1577">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="08996-1578">Lägg till nya fält och parametrar för funktionen Proxy Protocol V2.</span><span class="sxs-lookup"><span data-stu-id="08996-1578">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="08996-1579">Lägg till egenskapen EnableProxyProtocol i PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="08996-1579">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="08996-1580">Lägg till egenskapen LinkIdentifier i PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="08996-1580">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="08996-1581">Uppdaterade New-AzPrivateLinkService för att lägga till den nya valfria parametern EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="08996-1581">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="08996-1582">Korrigera felaktig beskrivning av parameter i referensdokumentationen för New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="08996-1582">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="08996-1583">Nya cmdletar som stöder Azure-brandväggsprincipen</span><span class="sxs-lookup"><span data-stu-id="08996-1583">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="08996-1584">Lägg till stöd för den underordnade resursen RouteTables för VirtualHub</span><span class="sxs-lookup"><span data-stu-id="08996-1584">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="08996-1585">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="08996-1585">New cmdlets added:</span></span>
        - <span data-ttu-id="08996-1586">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="08996-1586">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="08996-1587">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="08996-1587">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="08996-1588">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="08996-1588">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="08996-1589">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="08996-1589">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="08996-1590">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="08996-1590">Set-AzVirtualHub</span></span>
* <span data-ttu-id="08996-1591">Lägg till stöd för ny egenskaps-SKU för VirtualHub och VirtualWANType för VirtualWan</span><span class="sxs-lookup"><span data-stu-id="08996-1591">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="08996-1592">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="08996-1592">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="08996-1593">New-AzVirtualHub: lade till parameter-SKU</span><span class="sxs-lookup"><span data-stu-id="08996-1593">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="08996-1594">Update-AzVirtualHub: lade till parameter-SKU</span><span class="sxs-lookup"><span data-stu-id="08996-1594">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="08996-1595">New-AzVirtualWan: lade till parametern VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="08996-1595">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="08996-1596">Update-AzVirtualWan: lade till parametern VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="08996-1596">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="08996-1597">Lägg till stöd för egenskapen EnableInternetSecurity för HubVnetConnection, VpnConnection och ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="08996-1597">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="08996-1598">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="08996-1598">New cmdlets added:</span></span>
        - <span data-ttu-id="08996-1599">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="08996-1599">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="08996-1600">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="08996-1600">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="08996-1601">New-AzureRmVirtualHubVnetConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-1601">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="08996-1602">New-AzureRmVpnConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-1602">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="08996-1603">Update-AzureRmVpnConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-1603">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="08996-1604">New-AzureRmExpressRouteConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-1604">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="08996-1605">Set-AzureRmExpressRouteConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-1605">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="08996-1606">Lägg till stöd för att konfigurera TopLevel WebApplicationFirewall-princip</span><span class="sxs-lookup"><span data-stu-id="08996-1606">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="08996-1607">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="08996-1607">New cmdlets added:</span></span>
        - <span data-ttu-id="08996-1608">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="08996-1608">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="08996-1609">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="08996-1609">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="08996-1610">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="08996-1610">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="08996-1611">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="08996-1611">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="08996-1612">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="08996-1612">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="08996-1613">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="08996-1613">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="08996-1614">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="08996-1614">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="08996-1615">New-AzApplicationGatewayFirewallPolicy: parametrarna PolicySetting, ManagedRule har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-1615">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="08996-1616">Stöd för operator för geomatchning har lagts till på CustomRule</span><span class="sxs-lookup"><span data-stu-id="08996-1616">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="08996-1617">Geomatchning har lagts till i operatorn på FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="08996-1617">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="08996-1618">Stöd har lagts till för brandväggsprinciperna perListener och perSite</span><span class="sxs-lookup"><span data-stu-id="08996-1618">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="08996-1619">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="08996-1619">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="08996-1620">New-AzApplicationGatewayHttpListener: parametrarna FirewallPolicy, FirewallPolicyId har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-1620">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="08996-1621">New-AzApplicationGatewayPathRuleConfig: parametrarna FirewallPolicy, FirewallPolicyId har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-1621">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="08996-1622">Åtgärdat så att nödvändigt undernät med namnet AzureBastionSubnet i PSBastion kan vara skiftlägesokänsligt</span><span class="sxs-lookup"><span data-stu-id="08996-1622">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="08996-1623">Stöd för mål-FQDN:er i nätverksregler och översatt FQDN i NAT-regler för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="08996-1623">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="08996-1624">Lägg till stöd för resursen RouteTables för IpGroup på den högsta nivån</span><span class="sxs-lookup"><span data-stu-id="08996-1624">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="08996-1625">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="08996-1625">New cmdlets added:</span></span>
        - <span data-ttu-id="08996-1626">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="08996-1626">New-AzIpGroup</span></span>
        - <span data-ttu-id="08996-1627">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="08996-1627">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="08996-1628">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="08996-1628">Get-AzIpGroup</span></span>
        - <span data-ttu-id="08996-1629">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="08996-1629">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="08996-1630">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="08996-1630">Az.ServiceFabric</span></span>
* <span data-ttu-id="08996-1631">Ta bort cmdleten Add-AzServiceFabricApplicationCertificate eftersom det här scenariot omfattas av Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="08996-1631">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="08996-1632">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08996-1632">Az.Sql</span></span>
* <span data-ttu-id="08996-1633">Stöd har lagts till för återställning av utelämnade databaser på hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="08996-1633">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="08996-1634">Inaktuella gamla cmdletar för granskning från kod.</span><span class="sxs-lookup"><span data-stu-id="08996-1634">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="08996-1635">Tog bort inaktuella alias:</span><span class="sxs-lookup"><span data-stu-id="08996-1635">Removed deprecated aliases:</span></span>
* <span data-ttu-id="08996-1636">Get-AzSqlDatabaseIndexRecommendations (använd Get-AzSqlDatabaseIndexRecommendation istället)</span><span class="sxs-lookup"><span data-stu-id="08996-1636">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="08996-1637">Get-AzSqlDatabaseRestorePoints (använd Get-AzSqlDatabaseRestorePoint istället)</span><span class="sxs-lookup"><span data-stu-id="08996-1637">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="08996-1638">Ta bort cmdleten Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="08996-1638">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="08996-1639">Ta bort alias för inaktuella cmdletar för inställningar för utvärdering av säkerhetsrisk</span><span class="sxs-lookup"><span data-stu-id="08996-1639">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="08996-1640">Inaktualisera cmdletar för inställningar för avancerad hotidentifiering</span><span class="sxs-lookup"><span data-stu-id="08996-1640">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="08996-1641">Lägga till cmdletar för att inaktivera och aktivera känslighetsrekommendationer på kolumner i en databas.</span><span class="sxs-lookup"><span data-stu-id="08996-1641">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="08996-1642">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="08996-1642">Az.Storage</span></span>
* <span data-ttu-id="08996-1643">Stöd för att aktivera stora filresurser vid skapande eller uppdatering av lagringskonto</span><span class="sxs-lookup"><span data-stu-id="08996-1643">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="08996-1644">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="08996-1644">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="08996-1645">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="08996-1645">Set-AzStorageAccount</span></span>
* <span data-ttu-id="08996-1646">När du stänger/hämtar en filreferens kan du hoppa över kontrollen av huruvida indatasökvägen är en filkatalog eller en fil för att undvika problem med objekt som har status DeletePending</span><span class="sxs-lookup"><span data-stu-id="08996-1646">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="08996-1647">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="08996-1647">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="08996-1648">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="08996-1648">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="08996-1649">2.8.0 – oktober 2019</span><span class="sxs-lookup"><span data-stu-id="08996-1649">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="08996-1650">Allmänt</span><span class="sxs-lookup"><span data-stu-id="08996-1650">General</span></span>
* <span data-ttu-id="08996-1651">AZ. HealthcareApis 1.0.0-version</span><span class="sxs-lookup"><span data-stu-id="08996-1651">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="08996-1652">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="08996-1652">Az.Accounts</span></span>
* <span data-ttu-id="08996-1653">Uppdatera telemetri och URL-omskrivning för genererade moduler, korrigera Windows-enhetstester.</span><span class="sxs-lookup"><span data-stu-id="08996-1653">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="08996-1654">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="08996-1654">Az.ApiManagement</span></span>
* <span data-ttu-id="08996-1655">**Set-AzApiManagementApi** – Tillagt stöd för att uppdatera Api till ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="08996-1655">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="08996-1656">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="08996-1656">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="08996-1657">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="08996-1657">Az.Automation</span></span>
* <span data-ttu-id="08996-1658">Åtgärdade cmdleten New-AzureAutomationSoftwareUpdateConfiguration för parametern för inställning av Linux-omstart.</span><span class="sxs-lookup"><span data-stu-id="08996-1658">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="08996-1659">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="08996-1659">Az.Batch</span></span>
* <span data-ttu-id="08996-1660">**Get-AzBatchNodeAgentSku** är inaktuell och ersätts av **Get-AzBatchSupportImage** i version 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="08996-1660">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08996-1661">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08996-1661">Az.Compute</span></span>
* <span data-ttu-id="08996-1662">Lägg till parametrarna Priority, EvictionPolicy och MaxPrice till cmdletarna New-AzVM och New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="08996-1662">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="08996-1663">Korrigera varningsmeddelande och hjälpdokument för cmdletarna Add-AzVMAdditionalUnattendContent och Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="08996-1663">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="08996-1664">Åtgärda – skipVmBackup-undantag för virtuella Linux-datorer med hanterade diskar för Set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="08996-1664">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="08996-1665">Åtgärda fel i uppdatera krypteringsinställningarna i set-AzVMDiskEncryptionExtension, scenario i två steg.</span><span class="sxs-lookup"><span data-stu-id="08996-1665">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="08996-1666">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="08996-1666">Az.DataFactory</span></span>
* <span data-ttu-id="08996-1667">Lägga till CRUD-kommandon för ADF V2-dataflödet: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow och Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="08996-1667">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="08996-1668">Lägger till åtgärdskommandon för ADF V2-dataflödesfelsökningssession: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand och Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="08996-1668">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="08996-1669">Uppdatera ADF .Net SDK-versionen till 4.2.0</span><span class="sxs-lookup"><span data-stu-id="08996-1669">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="08996-1670">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="08996-1670">Az.DataLakeStore</span></span>
* <span data-ttu-id="08996-1671">Korrigera kontovalidering så att konton med ”-” kan skickas utan domän</span><span class="sxs-lookup"><span data-stu-id="08996-1671">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="08996-1672">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="08996-1672">Az.HealthcareApis</span></span>
* <span data-ttu-id="08996-1673">PowerShell-versionen har uppdaterats till 1.0.0</span><span class="sxs-lookup"><span data-stu-id="08996-1673">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="08996-1674">Uppdaterade SDK-versionen till 1.0.2</span><span class="sxs-lookup"><span data-stu-id="08996-1674">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="08996-1675">Uppdatera i tester för att referera till en ny SDK-version</span><span class="sxs-lookup"><span data-stu-id="08996-1675">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="08996-1676">Utdatastrukturen har uppdaterats från kapslad till förenklad.</span><span class="sxs-lookup"><span data-stu-id="08996-1676">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="08996-1677">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="08996-1677">Az.IotHub</span></span>
* <span data-ttu-id="08996-1678">Lägg till ny routningskälla: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="08996-1678">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="08996-1679">Mindre felkorrigering: Get-AzIothub returnerar inte subscriptionId</span><span class="sxs-lookup"><span data-stu-id="08996-1679">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="08996-1680">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="08996-1680">Az.Monitor</span></span>
* <span data-ttu-id="08996-1681">Nya åtgärdsgruppsmottagare har lagts till för åtgärdsgrupp   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="08996-1681">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="08996-1682">Använd vanligt aviseringsschema som är aktiverat för mottagarna.</span><span class="sxs-lookup"><span data-stu-id="08996-1682">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="08996-1683">Detta gäller inte för SMS, push för Azure-app, ITSM och röstmottagare</span><span class="sxs-lookup"><span data-stu-id="08996-1683">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="08996-1684">Webhooks har nu stöd för Azure Active Directory-autentisering.</span><span class="sxs-lookup"><span data-stu-id="08996-1684">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="08996-1685">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08996-1685">Az.Network</span></span>
* <span data-ttu-id="08996-1686">Lägg till ny cmdlet Get-AzAvailableServiceAlias som kan anropas för att hämta de alias som kan användas för tjänstslutpunktsprinciper.</span><span class="sxs-lookup"><span data-stu-id="08996-1686">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="08996-1687">Stöd för tillägg av trafikväljare har lagts till i gatewayanslutningar för virtuella nätverk</span><span class="sxs-lookup"><span data-stu-id="08996-1687">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="08996-1688">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="08996-1688">New cmdlets added:</span></span>
        - <span data-ttu-id="08996-1689">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="08996-1689">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="08996-1690">Cmdletar har uppdaterats med valfri parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="08996-1690">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="08996-1691">Lägg till stöd för ESP- och AH-protokoll i konfiguration av nätverkssäkerhetsregler</span><span class="sxs-lookup"><span data-stu-id="08996-1691">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="08996-1692">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="08996-1692">Updated cmdlets:</span></span>
        - <span data-ttu-id="08996-1693">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="08996-1693">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="08996-1694">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="08996-1694">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="08996-1695">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="08996-1695">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="08996-1696">Förbättra hanteringen av undantag i Cortex-cmdletar</span><span class="sxs-lookup"><span data-stu-id="08996-1696">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="08996-1697">Nya generationer och SKU:er för VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="08996-1697">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="08996-1698">Introducera nya generationer för VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="08996-1698">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="08996-1699">Introducera nya SKU:er med högt dataflöde för VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="08996-1699">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="08996-1700">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="08996-1700">Az.RedisCache</span></span>
* <span data-ttu-id="08996-1701">Uppdaterad referensdokumentation för ”set-AzRedisCache” för att inkludera saknade värden för parametern ”size”</span><span class="sxs-lookup"><span data-stu-id="08996-1701">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="08996-1702">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08996-1702">Az.Sql</span></span>
* <span data-ttu-id="08996-1703">Lägg till stöd för inställningen Active Directory administratör på den hanterade instansen</span><span class="sxs-lookup"><span data-stu-id="08996-1703">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="08996-1704">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="08996-1704">Az.Storage</span></span>
* <span data-ttu-id="08996-1705">Uppdatera Lagringsklientbibliotek till 11.1.0</span><span class="sxs-lookup"><span data-stu-id="08996-1705">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="08996-1706">Lista containrar med hanteringsplans-API, kommer att listas med NextPageLink</span><span class="sxs-lookup"><span data-stu-id="08996-1706">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="08996-1707">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="08996-1707">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="08996-1708">Lista lagringskonton från prenumerationen, kommer att listas med NextPageLink</span><span class="sxs-lookup"><span data-stu-id="08996-1708">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="08996-1709">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="08996-1709">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="08996-1710">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="08996-1710">Az.StorageSync</span></span>
* <span data-ttu-id="08996-1711">Åtgärda problemet 9810 i Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="08996-1711">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="08996-1712">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="08996-1712">Az.Websites</span></span>
* <span data-ttu-id="08996-1713">Set-AzWebApp – uppdatering av ASP för en app misslyckades</span><span class="sxs-lookup"><span data-stu-id="08996-1713">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="08996-1714">2.7.0 – september 2019</span><span class="sxs-lookup"><span data-stu-id="08996-1714">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="08996-1715">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="08996-1715">Az.ApiManagement</span></span>
* <span data-ttu-id="08996-1716">Uppdatera ”-Format”-parameterbeskrivningen i ”Set-AzApiManagementPolicy”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="08996-1716">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="08996-1717">Referenser för den föråldrade cmdleten ”Update-AzApiManagementDeployment” har tagits bort från referensdokumentationen.</span><span class="sxs-lookup"><span data-stu-id="08996-1717">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="08996-1718">Använd ”Set-AzApiManagement” i stället.</span><span class="sxs-lookup"><span data-stu-id="08996-1718">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="08996-1719">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="08996-1719">Az.Automation</span></span>
* <span data-ttu-id="08996-1720">Stavfel har korrigerats i exempel i referensdokumentationen för ”Register-AzAutomationDscNode”</span><span class="sxs-lookup"><span data-stu-id="08996-1720">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="08996-1721">Klargörande har lagts till om OS-begränsningar för Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="08996-1721">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="08996-1722">Null-referensundantag har korrigerats för -Wait-alternativet i Start-AzAutomationRunbook-cmdleten.</span><span class="sxs-lookup"><span data-stu-id="08996-1722">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08996-1723">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08996-1723">Az.Compute</span></span>
* <span data-ttu-id="08996-1724">Lägg till UploadSizeInBytes-parameter till New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="08996-1724">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="08996-1725">Lägg till Incremental-parameter till New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="08996-1725">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="08996-1726">Lägg till en funktion för virtuella datorer med låg prioritet:</span><span class="sxs-lookup"><span data-stu-id="08996-1726">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="08996-1727">MaxPrice-, EvictionPolicy- och Priority-parametrar har lagts till i New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="08996-1727">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="08996-1728">MaxPrice-parametern har lagts till i New-AzVmssConfig-, Update-AzVM- och Update-AzVmss-cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="08996-1728">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="08996-1729">Åtgärda problem med VM-referenser för Get-AzAvailabilitySet-cmdleten när alla tillgänglighetsuppsättningar i prenumerationen visas.</span><span class="sxs-lookup"><span data-stu-id="08996-1729">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="08996-1730">Korrigera null-undantaget för Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="08996-1730">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="08996-1731">Korrigera VHD-metoden för sökning relativt till slut.</span><span class="sxs-lookup"><span data-stu-id="08996-1731">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="08996-1732">Åtgärda UltraSSD-problem för New-AzVM och Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="08996-1732">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="08996-1733">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="08996-1733">Az.DataFactory</span></span>
* <span data-ttu-id="08996-1734">Lägger till 3 nya kommandon för ADF V2 – Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription och Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="08996-1734">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="08996-1735">ADF .Net SDK har uppdaterats till 4.1.3</span><span class="sxs-lookup"><span data-stu-id="08996-1735">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="08996-1736">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="08996-1736">Az.HDInsight</span></span>
* <span data-ttu-id="08996-1737">Anrop för icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="08996-1737">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="08996-1738">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="08996-1738">Az.IotHub</span></span>
* <span data-ttu-id="08996-1739">Lägg till stöd för att anropa redundans för en IotHub till den geo-länkade katastrofåterställningsregionen.</span><span class="sxs-lookup"><span data-stu-id="08996-1739">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="08996-1740">Lägg till stöd för att hantera meddelandeberikning för en IotHub.</span><span class="sxs-lookup"><span data-stu-id="08996-1740">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="08996-1741">Nya cmdlet:ar är:</span><span class="sxs-lookup"><span data-stu-id="08996-1741">New cmdlets are:</span></span>
    - <span data-ttu-id="08996-1742">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="08996-1742">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="08996-1743">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="08996-1743">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="08996-1744">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="08996-1744">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="08996-1745">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="08996-1745">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="08996-1746">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="08996-1746">Az.Monitor</span></span>
* <span data-ttu-id="08996-1747">Pekar på den senaste Monitor SDK:n, dvs. 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="08996-1747">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="08996-1748">Lägger till bakåtkompatibla ändringar i Metrics-cmdletarna, dvs. enhetsuppräkningen stöder flera nya värden.</span><span class="sxs-lookup"><span data-stu-id="08996-1748">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="08996-1749">Detta är skrivskyddade cmdletar, så det förekommer inga ändringar i inmatningen för cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="08996-1749">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="08996-1750">API-versionen för **ActionGroups**-begäranden är nu **2019-06-01**. Tidigare var den **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="08996-1750">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="08996-1751">Test av scenarier har uppdaterats för att anpassas till den här ändringen.</span><span class="sxs-lookup"><span data-stu-id="08996-1751">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="08996-1752">Ett nytt obligatoriskt argument har lagts till för konstruktorerna för klasserna **EmailReceiver** och **WebhookReceiver** – ett booleskt värde med namnet **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="08996-1752">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="08996-1753">Värdet är för närvarande fast till **false** så att den här icke-bakåtkompatibla ändringen är dold från cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="08996-1753">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="08996-1754">**Obs!** Det här är en tillfällig ändring som måste verifieras av Alerts-teamet.</span><span class="sxs-lookup"><span data-stu-id="08996-1754">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="08996-1755">Ordningen på argumenten för konstruktorn för klassen **Source** (relaterad till klassen **ScheduledQueryRuleSource**) har ändrats från den tidigare SDK:n.</span><span class="sxs-lookup"><span data-stu-id="08996-1755">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="08996-1756">Den här ändringen krävde korrigering av två enhetstest: de kompilerades, men testerna skickades inte.</span><span class="sxs-lookup"><span data-stu-id="08996-1756">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="08996-1757">Ordningen på argumenten för konstruktorn för klassen **AlertingAction** (relaterad till klassen **ScheduledQueryRuleSource**) har ändrats från den tidigare SDK:n.</span><span class="sxs-lookup"><span data-stu-id="08996-1757">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="08996-1758">Den här ändringen krävde korrigering av två enhetstest: de kompilerades, men testerna skickades inte.</span><span class="sxs-lookup"><span data-stu-id="08996-1758">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="08996-1759">Stöd för kriterier för dynamiskt tröskelvärde för måttavisering v2</span><span class="sxs-lookup"><span data-stu-id="08996-1759">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="08996-1760">New-AzMetricAlertRuleV2Criteria: skapar nu även kriterier för dynamiskt tröskelvärde</span><span class="sxs-lookup"><span data-stu-id="08996-1760">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="08996-1761">Add-AzMetricAlertRuleV2: accepterar nu även kriterier för dynamiskt tröskelvärde</span><span class="sxs-lookup"><span data-stu-id="08996-1761">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="08996-1762">Förbättringar i schemalagd frågeregel (SQR)</span><span class="sxs-lookup"><span data-stu-id="08996-1762">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="08996-1763">Cmdletar accepterar ”Location”-parameter i båda formaten, antingen platsen (t.ex. eastus) eller platsens visningsnamn (t.ex. USA, östra)</span><span class="sxs-lookup"><span data-stu-id="08996-1763">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="08996-1764">”Enabled”-parametern illustreras korrekt i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="08996-1764">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="08996-1765">Exempel för den valfria parametern ”ActionGroup” har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-1765">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="08996-1766">Förbättrade hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="08996-1766">Overall improved help files</span></span>
* <span data-ttu-id="08996-1767">Åtgärda bugg då omfattningstypen fastställs för ”Set-AzActionRule”</span><span class="sxs-lookup"><span data-stu-id="08996-1767">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="08996-1768">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08996-1768">Az.Network</span></span>
* <span data-ttu-id="08996-1769">Korrigera felaktigt exempel i referensdokumentationen för ”New-AzApplicationGateway”</span><span class="sxs-lookup"><span data-stu-id="08996-1769">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="08996-1770">Lägg till anmärkning i ”Get-AzNetworkWatcherPacketCapture”-referensdokumentationen om hämtning av alla egenskaper för en paketinsamling</span><span class="sxs-lookup"><span data-stu-id="08996-1770">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="08996-1771">Exempel har korrigerats i ”Test-AzNetworkWatcherIPFlow”-referensdokumentationen för korrekt uppräkning av nätverkskort</span><span class="sxs-lookup"><span data-stu-id="08996-1771">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="08996-1772">Förbättrad tolkning av molnundantag för att visa eventuell ytterligare information</span><span class="sxs-lookup"><span data-stu-id="08996-1772">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="08996-1773">Förbättrad tolkning av molnundantag för att hantera ytterligare en typ av SDK-undantag</span><span class="sxs-lookup"><span data-stu-id="08996-1773">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="08996-1774">Felaktig mappning av säkerhetsregelmodeller har korrigerats</span><span class="sxs-lookup"><span data-stu-id="08996-1774">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="08996-1775">Egenskaper har lagts till för nätverksgränssnittet för funktionen Privat IP</span><span class="sxs-lookup"><span data-stu-id="08996-1775">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="08996-1776">Egenskapen ”PrivateEndpoint” har lagts till som en typ av PSResourceId till PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="08996-1776">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="08996-1777">Egenskapen ”PrivateLinkConnectionProperties” har lagts till som en typ av PSIpConfigurationConnectivityInformation till PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="08996-1777">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="08996-1778">Modellklassen PSIpConfigurationConnectivityInformation har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-1778">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="08996-1779">ApplicationRuleProtocolType ”mssql” har lagts till för Azure Firewall-resurs</span><span class="sxs-lookup"><span data-stu-id="08996-1779">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="08996-1780">MultiLink-stöd i virtuellt WAN</span><span class="sxs-lookup"><span data-stu-id="08996-1780">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="08996-1781">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="08996-1781">New cmdlets</span></span>
        - <span data-ttu-id="08996-1782">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="08996-1782">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="08996-1783">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="08996-1783">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="08996-1784">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="08996-1784">Updated cmdlet:</span></span>
        - <span data-ttu-id="08996-1785">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="08996-1785">New-VpnSite</span></span>
        - <span data-ttu-id="08996-1786">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="08996-1786">Update-VpnSite</span></span>
        - <span data-ttu-id="08996-1787">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="08996-1787">New-VpnConnection</span></span>
        - <span data-ttu-id="08996-1788">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="08996-1788">Update-VpnConnection</span></span>
* <span data-ttu-id="08996-1789">Dokument för vissa PowerShell-exempel har korrigerats så att Az-cmdletar används i stället för AzureRM-cmdletar</span><span class="sxs-lookup"><span data-stu-id="08996-1789">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="08996-1790">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="08996-1790">Az.RecoveryServices</span></span>
* <span data-ttu-id="08996-1791">Uppdatera AzureVMpolicy-objekt med ProtectedItemsCount-attribut</span><span class="sxs-lookup"><span data-stu-id="08996-1791">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="08996-1792">Ytterligare tester har lagts till för VM-princip och återställning av ursprungligt lagringskonto</span><span class="sxs-lookup"><span data-stu-id="08996-1792">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="08996-1793">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08996-1793">Az.Resources</span></span>
* <span data-ttu-id="08996-1794">Åtgärda fel där det inte gick att anropa New-AzRoleAssignment utan parametern Scope.</span><span class="sxs-lookup"><span data-stu-id="08996-1794">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="08996-1795">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="08996-1795">Az.ServiceFabric</span></span>
* <span data-ttu-id="08996-1796">Stavfel har korrigerats i exempel för ”Update-AzServiceFabricReliability”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="08996-1796">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="08996-1797">Lägger till nya cmdletar för att hantera program och tjänster:</span><span class="sxs-lookup"><span data-stu-id="08996-1797">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="08996-1798">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="08996-1798">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="08996-1799">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="08996-1799">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="08996-1800">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="08996-1800">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="08996-1801">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="08996-1801">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="08996-1802">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="08996-1802">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="08996-1803">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="08996-1803">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="08996-1804">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="08996-1804">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="08996-1805">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="08996-1805">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="08996-1806">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="08996-1806">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="08996-1807">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="08996-1807">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="08996-1808">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="08996-1808">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="08996-1809">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="08996-1809">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="08996-1810">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="08996-1810">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="08996-1811">Service Fabric SDK har uppgraderats till version 1.2.0 som använder Service Fabric-resursprovidern med API-version 2019-03-01.</span><span class="sxs-lookup"><span data-stu-id="08996-1811">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="08996-1812">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="08996-1812">Az.SignalR</span></span>
* <span data-ttu-id="08996-1813">Lägg till Update-, Restart-, CheckNameAvailability- och GetUsage-cmdletar</span><span class="sxs-lookup"><span data-stu-id="08996-1813">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="08996-1814">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08996-1814">Az.Sql</span></span>
* <span data-ttu-id="08996-1815">Uppdatera exempel i referensdokumentationen för ”Get-AzSqlElasticPool”</span><span class="sxs-lookup"><span data-stu-id="08996-1815">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="08996-1816">vCore-exempel för att skapa en elastisk pool (New-AzSqlElasticPool) har lagts till.</span><span class="sxs-lookup"><span data-stu-id="08996-1816">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="08996-1817">Ta bort verifieringen av EmailAddresses och kontrollen som bekräftar att EmailAdmins inte är falskt när EmailAddresses är tomt i Set-AzSqlServerAdvancedThreatProtectionPolicy och Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="08996-1817">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="08996-1818">Server-/databasgranskningsinställningar kan tas bort när det finns flera diagnostikinställningar som aktiverar granskningskategorin.</span><span class="sxs-lookup"><span data-stu-id="08996-1818">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="08996-1819">Åtgärda verifiering av e-postadresser i flera Sql Vulnerability Assessment-cmdletar (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting och Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="08996-1819">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="08996-1820">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="08996-1820">Az.Storage</span></span>
* <span data-ttu-id="08996-1821">Exempel i referensdokumentationen för ”Get-AzStorageAccountKey” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="08996-1821">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="08996-1822">Vid upp- och nedladdning av en Azure-fil kan SMB-egenskaperna för källfilen (t.ex. filattribut, tidpunkten då filen skapades och tidpunkten för den senaste skrivningen) sparas i målfilen</span><span class="sxs-lookup"><span data-stu-id="08996-1822">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="08996-1823">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="08996-1823">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="08996-1824">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="08996-1824">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="08996-1825">Korrigera problem med uppladdningen av blockblob med egenskaper/metadata för ImmutabilityPolicy i containrar.</span><span class="sxs-lookup"><span data-stu-id="08996-1825">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="08996-1826">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="08996-1826">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="08996-1827">Stöd för hantering av Azure-filresurser med API för hanteringsplan</span><span class="sxs-lookup"><span data-stu-id="08996-1827">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="08996-1828">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="08996-1828">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="08996-1829">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="08996-1829">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="08996-1830">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="08996-1830">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="08996-1831">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="08996-1831">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="08996-1832">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="08996-1832">Az.Websites</span></span>
* <span data-ttu-id="08996-1833">Åtgärdar problemet där webapp-taggar togs bort när appen migrerades till nya ASP</span><span class="sxs-lookup"><span data-stu-id="08996-1833">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="08996-1834">Åtgärda Publish-AzureWebapp så att det fungerar i Linux och Windows</span><span class="sxs-lookup"><span data-stu-id="08996-1834">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="08996-1835">Uppdatera exempel i ”Get-AzWebAppPublishingProfile”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="08996-1835">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="08996-1836">2.6.0 – augusti 2019</span><span class="sxs-lookup"><span data-stu-id="08996-1836">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="08996-1837">Allmänt</span><span class="sxs-lookup"><span data-stu-id="08996-1837">General</span></span>
* <span data-ttu-id="08996-1838">Åtgärdade diverse skrivfel i flera moduler</span><span class="sxs-lookup"><span data-stu-id="08996-1838">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="08996-1839">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="08996-1839">Az.Accounts</span></span>
* <span data-ttu-id="08996-1840">Stöd för användartilldelat MSI i Azure Functions-autentisering (#9479)</span><span class="sxs-lookup"><span data-stu-id="08996-1840">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="08996-1841">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="08996-1841">Az.Aks</span></span>
* <span data-ttu-id="08996-1842">Åtgärda problem med utdata för "Get-AzAks"</span><span class="sxs-lookup"><span data-stu-id="08996-1842">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="08996-1843">Mer information här: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="08996-1843">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="08996-1844">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="08996-1844">Az.ApiManagement</span></span>
* <span data-ttu-id="08996-1845">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="08996-1845">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="08996-1846">Uppdatera .net-NuGet-versionen, som inte tillämpar begränsningar för productId, apiId och userId</span><span class="sxs-lookup"><span data-stu-id="08996-1846">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="08996-1847">**Get-AzApiManagementProduct** – Lade till stöd för frågekörning mot produkter via API.</span><span class="sxs-lookup"><span data-stu-id="08996-1847">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="08996-1848">**New-AzApiManagementApiRevision** – Korrigering för problem där ApiRevisionDescription inte angavs vid skapande av ny API-revision https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="08996-1848">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="08996-1849">Åtgärdade skrivfel i modellen "PsApiManagementOAuth2AuthrozationServer" till "PsApiManagementOAuth2AuthorizationServer"</span><span class="sxs-lookup"><span data-stu-id="08996-1849">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="08996-1850">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="08996-1850">Az.Batch</span></span>
* <span data-ttu-id="08996-1851">Åtgärdade skrivfel i hjälpmeddelande och dokumentation till att skriva Windows med versaler</span><span class="sxs-lookup"><span data-stu-id="08996-1851">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="08996-1852">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="08996-1852">Az.Cdn</span></span>
* <span data-ttu-id="08996-1853">Åtgärdade skrivfel i CDN-modulens konverteringshjälp</span><span class="sxs-lookup"><span data-stu-id="08996-1853">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08996-1854">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08996-1854">Az.Compute</span></span>
* <span data-ttu-id="08996-1855">Lägg till VmssId i New-AzVMConfig-cmdleten</span><span class="sxs-lookup"><span data-stu-id="08996-1855">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="08996-1856">Lägg till parametrarna TerminateScheduledEvents och TerminateScheduledEventNotBeforeTimeoutInMinutes i New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="08996-1856">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="08996-1857">Lägg till egenskapen HyperVGeneration till avbildningsobjekt för virtuell dator</span><span class="sxs-lookup"><span data-stu-id="08996-1857">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="08996-1858">Lägg till funktioner för Host och HostGroup</span><span class="sxs-lookup"><span data-stu-id="08996-1858">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="08996-1859">Nya cmdletar:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="08996-1859">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="08996-1860">HostId-parametern läggs till i New-AzVMConfig och New-AzVM</span><span class="sxs-lookup"><span data-stu-id="08996-1860">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="08996-1861">Uppdatera exempel i "Invoke-AzVMRunCommand"-dokumentationen till att använda rätt parameternamn</span><span class="sxs-lookup"><span data-stu-id="08996-1861">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="08996-1862">Uppdatera "-VolumeType"-beskrivningen i referensdokumentationen för "set-AzVMDiskEncryptionExtension" och "set-AzVmssDiskEncryptionExtension"</span><span class="sxs-lookup"><span data-stu-id="08996-1862">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="08996-1863">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="08996-1863">Az.DataFactory</span></span>
* <span data-ttu-id="08996-1864">Åtgärda skrivfel till att använda versaler för "Windows" i "New-AzDataFactoryEncryptValue"-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="08996-1864">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="08996-1865">Uppdaterade ADF .Net SDK-versionen till 4.1.2</span><span class="sxs-lookup"><span data-stu-id="08996-1865">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="08996-1866">Lägg till parametrarna "DataProxyIntegrationRuntimeName", "DataProxyStagingLinkedServiceName" och "DataProxyStagingPath" för "Set-AzureRmDataFactoryV2IntegrationRuntime"-cmd för att aktivera konfiguration av lokalt installerad integrationskörning som en proxy för SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="08996-1866">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="08996-1867">Uppdaterade PSTriggerRun till att visa utlöst pipeline, meddelande och egenskaper samt PSActivityRun till att visa aktivitetstypen</span><span class="sxs-lookup"><span data-stu-id="08996-1867">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="08996-1868">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="08996-1868">Az.DataLakeStore</span></span>
* <span data-ttu-id="08996-1869">Korrigering av frysning av Get-DataLakeStoreDeletedItem för fel eller fjärrundantag.</span><span class="sxs-lookup"><span data-stu-id="08996-1869">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="08996-1870">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="08996-1870">Az.EventHub</span></span>
* <span data-ttu-id="08996-1871">Korrigering av problem #9658 : Skrivfel i parametern VirtualNteworkRule i Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="08996-1871">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="08996-1872">Korrigering av problem #9558 : Set-AzEventHubNamespace använder PATCH i stället för PUT</span><span class="sxs-lookup"><span data-stu-id="08996-1872">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="08996-1873">lade till parametern EnableKafka i Set-AzEventHubNamespace-cmdleten</span><span class="sxs-lookup"><span data-stu-id="08996-1873">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="08996-1874">Korrigering av problem #9786 : kan inte skapa en regel med Endast lyssna-behörighet</span><span class="sxs-lookup"><span data-stu-id="08996-1874">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="08996-1875">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="08996-1875">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="08996-1876">Åtgärdade skrivfel i dokumentation där "Azure" skrevs helt med gemener</span><span class="sxs-lookup"><span data-stu-id="08996-1876">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="08996-1877">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="08996-1877">Az.Monitor</span></span>
* <span data-ttu-id="08996-1878">Åtgärdade felaktigt parameternamn i hjälpdokumentationen</span><span class="sxs-lookup"><span data-stu-id="08996-1878">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="08996-1879">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08996-1879">Az.Network</span></span>
* <span data-ttu-id="08996-1880">Uppdaterade New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="08996-1880">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="08996-1881">Gjorde parametern "PublicIpAddress" inaktuell eftersom den aldrig används på serversidan.</span><span class="sxs-lookup"><span data-stu-id="08996-1881">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="08996-1882">Lade till den valfria parametern "Primary", som anger huruvida den aktuella IP-konfigurationen är den primära.</span><span class="sxs-lookup"><span data-stu-id="08996-1882">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="08996-1883">Förbättrade hanteringen av felundantag för begärande från SDK – åtgärdar problemet att tidigare SDK-undantag inte hanteras på rätt sätt, vilket leder till att viktig felinformation inte visas</span><span class="sxs-lookup"><span data-stu-id="08996-1883">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="08996-1884">Justerade valideringslogiken för IPv6-IP-prefix till att kontrollera korrekt IPv6-prefixlängd.</span><span class="sxs-lookup"><span data-stu-id="08996-1884">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="08996-1885">Uppdaterade Get-AzVirtualNetworkSubnetConfig: Lade till parameter som anges till get av undernätets resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="08996-1885">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="08996-1886">Uppdaterade beskrivningen av parametern Location för AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="08996-1886">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="08996-1887">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="08996-1887">Az.OperationalInsights</span></span>
* <span data-ttu-id="08996-1888">Uppdaterade dokumentation för "New-AzOperationalInsightsLinuxSyslogDataSource"</span><span class="sxs-lookup"><span data-stu-id="08996-1888">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="08996-1889">Lade till exempel</span><span class="sxs-lookup"><span data-stu-id="08996-1889">Added example</span></span>
    - <span data-ttu-id="08996-1890">Uppdaterade beskrivningen av parametern "-Name"</span><span class="sxs-lookup"><span data-stu-id="08996-1890">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="08996-1891">Lade till ett exempel för New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="08996-1891">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="08996-1892">Ändrade beskrivningen av parametern -Name för New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="08996-1892">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="08996-1893">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="08996-1893">Az.RecoveryServices</span></span>
* <span data-ttu-id="08996-1894">Uppdatera "Get-AzRecoveryServicesBackupJobDetail.md"</span><span class="sxs-lookup"><span data-stu-id="08996-1894">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="08996-1895">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08996-1895">Az.Resources</span></span>
* <span data-ttu-id="08996-1896">Lägg till stöd för den nya API-versionen från 2019-05-10 för Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="08996-1896">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="08996-1897">Lägg till stöd för "copy.count = 0" för variabler, resurser och egenskaper</span><span class="sxs-lookup"><span data-stu-id="08996-1897">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="08996-1898">Resurser med "condition = false" eller "copy.count = 0" tas bort i complete-läget</span><span class="sxs-lookup"><span data-stu-id="08996-1898">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="08996-1899">Lägg till ett exempel på tilldelning av princip på prenumerationsnivå i hjälpdokumentationen</span><span class="sxs-lookup"><span data-stu-id="08996-1899">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="08996-1900">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="08996-1900">Az.ServiceBus</span></span>
* <span data-ttu-id="08996-1901">Korrigering av problem #9658 : Skrivfel i parametern VirtualNetworkRule i set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="08996-1901">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="08996-1902">Korrigering av problem #9786 : kan inte skapa en regel med Endast lyssna-behörighet</span><span class="sxs-lookup"><span data-stu-id="08996-1902">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="08996-1903">Lade till det nya kommandot "Test-AzServiceBusNameAvailability" för att kontrollera namntillgängligheten för kö och ämne</span><span class="sxs-lookup"><span data-stu-id="08996-1903">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="08996-1904">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="08996-1904">Az.ServiceFabric</span></span>
* <span data-ttu-id="08996-1905">Åtgärda buggar med tillägg av nodtyps-cmdlet:</span><span class="sxs-lookup"><span data-stu-id="08996-1905">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="08996-1906">NullReferenceException-bugg när resursgrupp hade annan vmss som inte är relaterad till Service Fabric-klustret.</span><span class="sxs-lookup"><span data-stu-id="08996-1906">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="08996-1907">Åtgärdar problemet: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="08996-1907">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="08996-1908">Åtgärda bugg där cmdleten misslyckades om virtualNetwork var i en annan resursgrupp än klustret.</span><span class="sxs-lookup"><span data-stu-id="08996-1908">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="08996-1909">Åtgärdar problemet: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="08996-1909">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="08996-1910">AzServiceFabricApplicationCertificate-cmdleten görs inaktuell</span><span class="sxs-lookup"><span data-stu-id="08996-1910">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="08996-1911">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08996-1911">Az.Sql</span></span>
* <span data-ttu-id="08996-1912">Uppdatera dokumentation om gamla gransknings-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="08996-1912">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="08996-1913">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="08996-1913">Az.Storage</span></span>
* <span data-ttu-id="08996-1914">Uppdatera hjälpen för Get/Close-AzStorageFileHandle genom att lägga till fler scenarier i cmdlet-exempel och uppdatera parameterbeskrivningar</span><span class="sxs-lookup"><span data-stu-id="08996-1914">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="08996-1915">Stöd för StandardBlobTier i uppladdningsblob och kopieringsblob</span><span class="sxs-lookup"><span data-stu-id="08996-1915">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="08996-1916">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="08996-1916">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="08996-1917">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="08996-1917">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="08996-1918">Stöd för rehydratiseringsprioritet i kopieringsblob</span><span class="sxs-lookup"><span data-stu-id="08996-1918">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="08996-1919">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="08996-1919">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="08996-1920">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="08996-1920">Az.Websites</span></span>
* <span data-ttu-id="08996-1921">Lägg till klargöranden gällande parametern -AppSettings i Set-AzWebApp och Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="08996-1921">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="08996-1922">2.5.0 – July 2019</span><span class="sxs-lookup"><span data-stu-id="08996-1922">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="08996-1923">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="08996-1923">Az.Accounts</span></span>
* <span data-ttu-id="08996-1924">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="08996-1924">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="08996-1925">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="08996-1925">Az.ApplicationInsights</span></span>
* <span data-ttu-id="08996-1926">Korrigera skrivfel i exempel i dokumentationen för Remove-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="08996-1926">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="08996-1927">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="08996-1927">Az.Automation</span></span>
* <span data-ttu-id="08996-1928">Korrigera skrivfel i resurssträng</span><span class="sxs-lookup"><span data-stu-id="08996-1928">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="08996-1929">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="08996-1929">Az.CognitiveServices</span></span>
* <span data-ttu-id="08996-1930">Stöd för NetworkRuleSet har lagts till.</span><span class="sxs-lookup"><span data-stu-id="08996-1930">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08996-1931">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08996-1931">Az.Compute</span></span>
* <span data-ttu-id="08996-1932">Lägg till saknade egenskaper (ComputerName, OsName, OsVersion och HyperVGeneration) för visningsobjekt i den virtuella datorinstansen.</span><span class="sxs-lookup"><span data-stu-id="08996-1932">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="08996-1933">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="08996-1933">Az.ContainerRegistry</span></span>
* <span data-ttu-id="08996-1934">Åtgärda skrivfel i Remove-AzContainerRegistryReplication för parametern Replication</span><span class="sxs-lookup"><span data-stu-id="08996-1934">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="08996-1935">Mer information finns här: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="08996-1935">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="08996-1936">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="08996-1936">Az.DataFactory</span></span>
* <span data-ttu-id="08996-1937">ADF .Net SDK-versionen har uppdaterats till 4.1.0</span><span class="sxs-lookup"><span data-stu-id="08996-1937">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="08996-1938">Korrigera skrivfel i dokumentationen för Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="08996-1938">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="08996-1939">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="08996-1939">Az.EventHub</span></span>
* <span data-ttu-id="08996-1940">Ny cmmdlet har lagts till för att skapa SAS-token: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="08996-1940">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="08996-1941">verifierings- och felmeddelande har lagts till för authorizationrules-rättigheter om endast "hantera" har tilldelats</span><span class="sxs-lookup"><span data-stu-id="08996-1941">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="08996-1942">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="08996-1942">Az.KeyVault</span></span>
* <span data-ttu-id="08996-1943">Stöd har lagts till för att ange KeySize för certifikatprinciper</span><span class="sxs-lookup"><span data-stu-id="08996-1943">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="08996-1944">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="08996-1944">Az.LogicApp</span></span>
* <span data-ttu-id="08996-1945">Korrigering för Get-AzIntegrationAccountMap för att lista alla mappningstyper</span><span class="sxs-lookup"><span data-stu-id="08996-1945">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="08996-1946">Ny MapType-parameter har lagts till för filtrering</span><span class="sxs-lookup"><span data-stu-id="08996-1946">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="08996-1947">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="08996-1947">Az.ManagedServices</span></span>
* <span data-ttu-id="08996-1948">Stöd för API-versionen 2019-06-01 (GA) har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-1948">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="08996-1949">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08996-1949">Az.Network</span></span>
* <span data-ttu-id="08996-1950">Lägg till stöd för privat slutpunkt och privat länktjänst</span><span class="sxs-lookup"><span data-stu-id="08996-1950">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="08996-1951">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="08996-1951">New cmdlets</span></span>
        - <span data-ttu-id="08996-1952">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="08996-1952">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="08996-1953">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="08996-1953">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="08996-1954">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="08996-1954">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="08996-1955">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="08996-1955">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="08996-1956">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="08996-1956">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="08996-1957">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="08996-1957">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="08996-1958">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="08996-1958">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="08996-1959">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="08996-1959">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="08996-1960">Nedanstående kommandon för funktionen har uppdaterats: Flaggan PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies på undernätet i VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="08996-1960">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="08996-1961">Uppdaterade New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="08996-1961">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="08996-1962">Valfri parameter har lagts till – PrivateEndpointNetworkPoliciesFlag som konfigurerar huruvida nätverksprinciper ska tillämpas på en privat slutpunkt i det här undernätet.</span><span class="sxs-lookup"><span data-stu-id="08996-1962">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="08996-1963">Valfri parameter har lagts till – PrivateLinkServiceNetworkPoliciesFlag som konfigurerar huruvida nätverksprinciper ska tillämpas på en privat länktjänst i det här undernätet.</span><span class="sxs-lookup"><span data-stu-id="08996-1963">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="08996-1964">AzPrivateLinkService för cmdlet-parametern ServiceName har bytt namn till Name med aliaset ServiceName för bakåtkompatibilitet</span><span class="sxs-lookup"><span data-stu-id="08996-1964">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="08996-1965">Aktivera ICMP-protokoll för konfiguration av nätverkssäkerhetsregler</span><span class="sxs-lookup"><span data-stu-id="08996-1965">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="08996-1966">Uppdaterade cmdletar</span><span class="sxs-lookup"><span data-stu-id="08996-1966">Updated cmdlets</span></span>
        - <span data-ttu-id="08996-1967">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="08996-1967">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="08996-1968">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="08996-1968">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="08996-1969">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="08996-1969">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="08996-1970">Lägg till ConnectionProtocolType (Ikev1/Ikev2) som en konfigurerbar parameter för New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="08996-1970">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="08996-1971">Lägg till PrivateIpAddressVersion i LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="08996-1971">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="08996-1972">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="08996-1972">Updated cmdlet:</span></span>
        - <span data-ttu-id="08996-1973">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="08996-1973">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="08996-1974">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="08996-1974">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="08996-1975">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="08996-1975">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="08996-1976">Uppdatering av Application Gateway-kommandot New-AzApplicationGatewayProbeConfig för stöd av anpassad port i Probe</span><span class="sxs-lookup"><span data-stu-id="08996-1976">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="08996-1977">Uppdaterade New-AzApplicationGatewayProbeConfig: Den valfria parametern Port som används för avsökning i serverdelen har lagts till.</span><span class="sxs-lookup"><span data-stu-id="08996-1977">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="08996-1978">Denna parameter gäller för SKU:erna Standard_V2 och WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="08996-1978">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="08996-1979">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="08996-1979">Az.OperationalInsights</span></span>
* <span data-ttu-id="08996-1980">Uppdaterade standardversionen för sparade sökningar till 1.</span><span class="sxs-lookup"><span data-stu-id="08996-1980">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="08996-1981">Åtgärdade hantering av anpassad log null regex</span><span class="sxs-lookup"><span data-stu-id="08996-1981">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="08996-1982">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="08996-1982">Az.RecoveryServices</span></span>
* <span data-ttu-id="08996-1983">Uppdatera Get-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="08996-1983">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="08996-1984">Uppdatera Get-AzRecoveryServicesBackupContainer.md</span><span class="sxs-lookup"><span data-stu-id="08996-1984">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="08996-1985">Uppdatera Get-AzRecoveryServicesVault.md</span><span class="sxs-lookup"><span data-stu-id="08996-1985">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="08996-1986">Uppdatera Wait-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="08996-1986">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="08996-1987">Uppdatera Set-AzRecoveryServicesVaultContext.md</span><span class="sxs-lookup"><span data-stu-id="08996-1987">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="08996-1988">Uppdatera Get-AzRecoveryServicesBackupItem.md</span><span class="sxs-lookup"><span data-stu-id="08996-1988">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="08996-1989">Uppdatera Get-AzRecoveryServicesBackupRecoveryPoint.md</span><span class="sxs-lookup"><span data-stu-id="08996-1989">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="08996-1990">Uppdatera Restore-AzRecoveryServicesBackupItem.md</span><span class="sxs-lookup"><span data-stu-id="08996-1990">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="08996-1991">Uppdaterat tjänstanrop för avregistrering av container för Azure-filresurs</span><span class="sxs-lookup"><span data-stu-id="08996-1991">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="08996-1992">Uppdatera Set-AzRecoveryServicesAsrAlertSetting.md</span><span class="sxs-lookup"><span data-stu-id="08996-1992">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="08996-1993">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08996-1993">Az.Resources</span></span>
- <span data-ttu-id="08996-1994">Ta bort den cmdlet som saknas och som refereras i dokumentationen till New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="08996-1994">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="08996-1995">Princip-cmdletar har uppdaterats så att de använder den nya API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="08996-1995">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="08996-1996">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="08996-1996">Az.ServiceBus</span></span>
* <span data-ttu-id="08996-1997">Ny cmmdlet har lagts till för att skapa SAS-token: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="08996-1997">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="08996-1998">verifierings- och felmeddelande har lagts till för authorizationrules-rättigheter om endast "hantera" har tilldelats</span><span class="sxs-lookup"><span data-stu-id="08996-1998">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="08996-1999">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08996-1999">Az.Sql</span></span>
* <span data-ttu-id="08996-2000">Åtgärda saknade exempel för Set-AzSqlDatabaseSecondary cmdlet</span><span class="sxs-lookup"><span data-stu-id="08996-2000">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="08996-2001">Åtgärda angivna återkommande genomsökningar för bedömning av säkerhetsrisk utan angivna e-postadresser</span><span class="sxs-lookup"><span data-stu-id="08996-2001">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="08996-2002">Korrigera ett skrivfel i ett varningsmeddelande.</span><span class="sxs-lookup"><span data-stu-id="08996-2002">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="08996-2003">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="08996-2003">Az.Storage</span></span>
* <span data-ttu-id="08996-2004">Uppdatera exempel i referensdokumentationen för Get-AzStorageAccount så att rätt parameternamn används</span><span class="sxs-lookup"><span data-stu-id="08996-2004">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="08996-2005">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="08996-2005">Az.StorageSync</span></span>
* <span data-ttu-id="08996-2006">Lägger till cmdleten Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="08996-2006">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="08996-2007">Åtgärda problem 9551 så att TierFilesOlderThanDays föredras</span><span class="sxs-lookup"><span data-stu-id="08996-2007">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="08996-2008">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="08996-2008">Az.Websites</span></span>
* <span data-ttu-id="08996-2009">Åtgärdar ett fel där vissa SiteConfig-egenskaper inte returnerades av Get-AzWebApp och Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="08996-2009">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="08996-2010">Lägger till en ny platsparameter för Get-AzDeletedWebApp och Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="08996-2010">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="08996-2011">Åtgärdar ett fel i kloning av webbapp-platser som använder New-AzWebApp-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="08996-2011">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="08996-2012">2.4.0 – juli 2019</span><span class="sxs-lookup"><span data-stu-id="08996-2012">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="08996-2013">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="08996-2013">Az.Accounts</span></span>
* <span data-ttu-id="08996-2014">Lägg till stöd för profil-cmdletar</span><span class="sxs-lookup"><span data-stu-id="08996-2014">Add support for profile cmdlets</span></span>
* <span data-ttu-id="08996-2015">Lägg till stöd för miljöer och dataplaner i genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="08996-2015">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="08996-2016">Åtgärda bugg där fel slutpunkt i vissa fall användes för cmdletar för dataplaner i Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="08996-2016">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="08996-2017">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="08996-2017">Az.Advisor</span></span>
* <span data-ttu-id="08996-2018">GA-version av Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="08996-2018">GA release of Az.Advisor</span></span>
* <span data-ttu-id="08996-2019">Den här modulen ingår nu som en del av `Az`-sammanslagningsmodulen</span><span class="sxs-lookup"><span data-stu-id="08996-2019">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="08996-2020">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="08996-2020">Az.ApiManagement</span></span>
* <span data-ttu-id="08996-2021">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="08996-2021">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="08996-2022">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="08996-2022">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="08996-2023">Stöd för att fråga prenumerationer efter användare och produkt har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-2023">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="08996-2024">Stöd för att fråga med hjälp av omfång ”/”, ”/apis”, ”/apis/echo-api” har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-2024">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="08996-2025">Korrigering av problem https://github.com/Azure/azure-powershell/issues/9307 och https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="08996-2025">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="08996-2026">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="08996-2026">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="08996-2027">Stöd för att ange ”ApiVersion” och ”ApiVersionSetId” när API:er importeras har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-2027">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="08996-2028">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="08996-2028">Az.Automation</span></span>
* <span data-ttu-id="08996-2029">Bugg med cmdleten Set-AzAutomationConnectionFieldValue för att hantera strängvärde har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="08996-2029">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08996-2030">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08996-2030">Az.Compute</span></span>
* <span data-ttu-id="08996-2031">Lägg till parametern HyperVGeneration i New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="08996-2031">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="08996-2032">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="08996-2032">Az.DataFactory</span></span>
* <span data-ttu-id="08996-2033">Uppdaterar utdata från ADF-cmdletar som hämtar aktivitetskörningar, hämtar pipelinekörningar och hämtar utlösarkörningar för stöd för Select-Object-pipe.</span><span class="sxs-lookup"><span data-stu-id="08996-2033">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="08996-2034">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="08996-2034">Az.EventGrid</span></span>
* <span data-ttu-id="08996-2035">Korrigera stavfel i dokumentation om ”New-AzEventGridSubscription”</span><span class="sxs-lookup"><span data-stu-id="08996-2035">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="08996-2036">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="08996-2036">Az.IotHub</span></span>
* <span data-ttu-id="08996-2037">Lägg till stöd för att återskapa principnycklar för auktorisering.</span><span class="sxs-lookup"><span data-stu-id="08996-2037">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="08996-2038">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08996-2038">Az.Network</span></span>
* <span data-ttu-id="08996-2039">”RoutingPreference” har lagts till i offentliga IP-taggar</span><span class="sxs-lookup"><span data-stu-id="08996-2039">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="08996-2040">Förbättra exempel för referensdokumentation om ”Get-AzNetworkServiceTag”</span><span class="sxs-lookup"><span data-stu-id="08996-2040">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="08996-2041">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="08996-2041">Az.PolicyInsights</span></span>
* <span data-ttu-id="08996-2042">Åtgärda problem med null-referens i Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="08996-2042">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="08996-2043">Mer information här: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="08996-2043">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="08996-2044">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="08996-2044">Az.OperationalInsights</span></span>
* <span data-ttu-id="08996-2045">Modellen för CustomLog-datakälla som returneras i Get-AzOperationalInsightsDataSource har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="08996-2045">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="08996-2046">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="08996-2046">Az.RecoveryServices</span></span>
* <span data-ttu-id="08996-2047">Kommandot get-policy för IaaSVM:er har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="08996-2047">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="08996-2048">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08996-2048">Az.Resources</span></span>
    - <span data-ttu-id="08996-2049">Korrigera hjälptext för den översta parametern i Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="08996-2049">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="08996-2050">Lägg till växlingsstöd på klientsidan för Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="08996-2050">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="08996-2051">Lägg till nya parametrar för Set-AzPolicyAssignment, -PolicyParameters och -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="08996-2051">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="08996-2052">En mängd dokument- och exempeluppdateringar för Policy-cmdletar</span><span class="sxs-lookup"><span data-stu-id="08996-2052">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="08996-2053">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="08996-2053">Az.ServiceBus</span></span>
* <span data-ttu-id="08996-2054">Korrigering av problem #4938 – New-AzureRmServiceBusQueue returnerar BadRequest vid konfiguration av MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="08996-2054">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="08996-2055">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08996-2055">Az.Sql</span></span>
* <span data-ttu-id="08996-2056">Lägg till cmdletar för instansredundansgrupper från förhandsversion till offentlig version</span><span class="sxs-lookup"><span data-stu-id="08996-2056">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="08996-2057">Stöd för granskning för Azure SQL Server\Database med nya cmdletar.</span><span class="sxs-lookup"><span data-stu-id="08996-2057">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="08996-2058">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="08996-2058">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="08996-2059">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="08996-2059">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="08996-2060">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="08996-2060">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="08996-2061">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="08996-2061">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="08996-2062">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="08996-2062">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="08996-2063">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="08996-2063">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="08996-2064">Ta bort begränsningar för e-post från inställningarna för sårbarhetsbedömning</span><span class="sxs-lookup"><span data-stu-id="08996-2064">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="08996-2065">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="08996-2065">Az.Storage</span></span>
* <span data-ttu-id="08996-2066">Ändra två parametrar ”-IndexDocument” och ”-ErrorDocument404Path” från ”krävs” till ”valfri” i cmdlet:</span><span class="sxs-lookup"><span data-stu-id="08996-2066">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="08996-2067">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="08996-2067">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="08996-2068">Uppdatera hjälpen för Get-AzStorageBlobContent genom att lägga till ett exempel</span><span class="sxs-lookup"><span data-stu-id="08996-2068">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="08996-2069">Visa mer felinformation när cmdleten misslyckas med StorageException</span><span class="sxs-lookup"><span data-stu-id="08996-2069">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="08996-2070">Stöd för att skapa eller uppdatera lagringskonto med Azure Files AAD DS-autentisering</span><span class="sxs-lookup"><span data-stu-id="08996-2070">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="08996-2071">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="08996-2071">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="08996-2072">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="08996-2072">Set-AzStorageAccount</span></span>
* <span data-ttu-id="08996-2073">Stöd för att lista eller stänga filreferenser för en filresurs, filkatalog eller en fil</span><span class="sxs-lookup"><span data-stu-id="08996-2073">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="08996-2074">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="08996-2074">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="08996-2075">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="08996-2075">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="08996-2076">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="08996-2076">Az.StorageSync</span></span>
* <span data-ttu-id="08996-2077">Den här modulen ingår nu som en del av `Az`-sammanslagningsmodulen</span><span class="sxs-lookup"><span data-stu-id="08996-2077">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="08996-2078">2.3.2 – juni 2019</span><span class="sxs-lookup"><span data-stu-id="08996-2078">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="08996-2079">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="08996-2079">Az.Accounts</span></span>
* <span data-ttu-id="08996-2080">Åtgärda bugg med felaktiga webbadresser som i vissa fall användes för Functions-anrop</span><span class="sxs-lookup"><span data-stu-id="08996-2080">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="08996-2081">Mer information här: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="08996-2081">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="08996-2082">Åtgärda problem med alias från AzureRM i Az-cmdletar</span><span class="sxs-lookup"><span data-stu-id="08996-2082">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="08996-2083">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="08996-2083">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="08996-2084">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="08996-2084">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08996-2085">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08996-2085">Az.Compute</span></span>
* <span data-ttu-id="08996-2086">Parameteruppsättningarna New-AzVm och New-AzVmss accepterar nu parametern ”ProximityPlacementGroup”.</span><span class="sxs-lookup"><span data-stu-id="08996-2086">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="08996-2087">Stavfel i referensdokumentationen för ”New-AzVM” har korrigerats</span><span class="sxs-lookup"><span data-stu-id="08996-2087">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="08996-2088">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="08996-2088">Az.Dns</span></span>
* <span data-ttu-id="08996-2089">Stavfel i hjälpexempel för ”Set-AzDnsZone” har korrigerats.</span><span class="sxs-lookup"><span data-stu-id="08996-2089">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="08996-2090">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="08996-2090">Az.EventGrid</span></span>
* <span data-ttu-id="08996-2091">Har uppdaterats för att använda API-versionen 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="08996-2091">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="08996-2092">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="08996-2092">New cmdlets:</span></span>
    - <span data-ttu-id="08996-2093">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="08996-2093">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="08996-2094">Skapar en ny Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="08996-2094">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="08996-2095">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="08996-2095">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="08996-2096">Hämtar information om en Event Grid-domän eller hämtar en lista med alla Event Grid-domäner i den aktuella Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="08996-2096">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="08996-2097">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="08996-2097">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="08996-2098">Tar bort en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="08996-2098">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="08996-2099">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="08996-2099">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="08996-2100">Återskapar nyckeln för delad åtkomst för en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="08996-2100">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="08996-2101">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="08996-2101">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="08996-2102">Hämtar de nycklar för delad åtkomst som används för att publicera händelser till en Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="08996-2102">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="08996-2103">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="08996-2103">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="08996-2104">Skapar ett nytt Azure Event Grid-domänämne.</span><span class="sxs-lookup"><span data-stu-id="08996-2104">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="08996-2105">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="08996-2105">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="08996-2106">Hämtar information om ett Event Grid-domänämne eller hämtar en lista med alla Event Grid-domänämnen under en specifik Event Grid-domän i nuvarande Azure</span><span class="sxs-lookup"><span data-stu-id="08996-2106">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="08996-2107">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="08996-2107">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="08996-2108">Tar bort ett befintligt Azure Event Grid-domänämne.</span><span class="sxs-lookup"><span data-stu-id="08996-2108">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="08996-2109">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="08996-2109">Updated cmdlets:</span></span>
    - <span data-ttu-id="08996-2110">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="08996-2110">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="08996-2111">Lägg till nya obligatoriska parametrar för att stödja piping för den nya Event Grid-domänen och Event Grid-domänämnet för att göra det möjligt att skapa nya händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="08996-2111">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="08996-2112">Lägg till nya obligatoriska parametrar för att ange det nya Event Grid-domännamnet och/eller namnet på Event Grid-domänämnet för att göra det möjligt att skapa nya händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="08996-2112">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="08996-2113">Lägg till ny parameteruppsättningar för domäner och domänämnen för att göra det möjligt att återanvända befintliga parametrar (t.ex. EndPointType, SubjectBeginsWith osv).</span><span class="sxs-lookup"><span data-stu-id="08996-2113">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="08996-2114">Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="08996-2114">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="08996-2115">Förfallodatum för händelseprenumeration</span><span class="sxs-lookup"><span data-stu-id="08996-2115">Event subscription expiration date,</span></span>
            - <span data-ttu-id="08996-2116">Avancerade filterparametrar.</span><span class="sxs-lookup"><span data-stu-id="08996-2116">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="08996-2117">Lägg till ny uppräkning för servicebusqueue som mål.</span><span class="sxs-lookup"><span data-stu-id="08996-2117">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="08996-2118">Tillåt inte användning av ”Alla” i alternativet -IncludedEventType och ersätt det med</span><span class="sxs-lookup"><span data-stu-id="08996-2118">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="08996-2119">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="08996-2119">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="08996-2120">Lägg till ny valfria parametrar (Top, ODataQuery och NextLink) för att stödja sidnumrering och filtrering av resultat.</span><span class="sxs-lookup"><span data-stu-id="08996-2120">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="08996-2121">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="08996-2121">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="08996-2122">Lägg till nya obligatoriska parametrar för att stödja piping för en Event Grid-domän och Event Grid-domänämnen för att göra det möjligt att ta bort befintliga händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="08996-2122">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="08996-2123">Lägg till nya obligatoriska parametrar för att ange Event Grid-domännamnet och/eller namnet på Event Grid-domänämnet för att göra det möjligt att ta bort befintliga händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="08996-2123">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="08996-2124">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="08996-2124">Az.FrontDoor</span></span>
* <span data-ttu-id="08996-2125">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="08996-2125">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="08996-2126">Lägg till stöd för transformeringar och nytt värde för automatisk komplettering för operatorer (RegEx)</span><span class="sxs-lookup"><span data-stu-id="08996-2126">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="08996-2127">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="08996-2127">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="08996-2128">Lägg till nya värden för automatisk komplettering</span><span class="sxs-lookup"><span data-stu-id="08996-2128">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="08996-2129">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08996-2129">Az.Network</span></span>
* <span data-ttu-id="08996-2130">Lägg till stöd för resurs för virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="08996-2130">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="08996-2131">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="08996-2131">New cmdlets</span></span>
        - <span data-ttu-id="08996-2132">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="08996-2132">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="08996-2133">Lägg till AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="08996-2133">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="08996-2134">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="08996-2134">New cmdlets</span></span>
        - <span data-ttu-id="08996-2135">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="08996-2135">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="08996-2136">Lägg till PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="08996-2136">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="08996-2137">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="08996-2137">New cmdlets</span></span>
        - <span data-ttu-id="08996-2138">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="08996-2138">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="08996-2139">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="08996-2139">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="08996-2140">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="08996-2140">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="08996-2141">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="08996-2141">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="08996-2142">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="08996-2142">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="08996-2143">Lägg till PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="08996-2143">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="08996-2144">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="08996-2144">New cmdlets</span></span>
        - <span data-ttu-id="08996-2145">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="08996-2145">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="08996-2146">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="08996-2146">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="08996-2147">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="08996-2147">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="08996-2148">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="08996-2148">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="08996-2149">Nedanstående kommandon för funktionen har uppdaterats: Flaggan UseLocalAzureIpAddress på VpnConnection</span><span class="sxs-lookup"><span data-stu-id="08996-2149">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="08996-2150">New-AzVpnConnection har uppdaterats: Den valfria parametern -UseLocalAzureIpAddress har lagts till för att visa att en lokal IP-adress i Azure ska användas som källadress när anslutningen initieras.</span><span class="sxs-lookup"><span data-stu-id="08996-2150">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="08996-2151">Set-AzVpnConnection har uppdaterats: Den valfria parametern -UseLocalAzureIpAddress har lagts till för att visa att en lokal IP-adress i Azure ska användas som källadress när anslutningen initieras.</span><span class="sxs-lookup"><span data-stu-id="08996-2151">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="08996-2152">Det skrivskyddade fältet PeeredConnections har lagts till i ExpressRoute-peering.</span><span class="sxs-lookup"><span data-stu-id="08996-2152">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="08996-2153">Det skrivskyddade fältet GlobalReachEnabled har lagts till i ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="08996-2153">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="08996-2154">Ett attribut för icke-bakåtkompatibla ändringar har lagts till för att lyfta fram utfasning av fältet AllowGlobalReach i modellen ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="08996-2154">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="08996-2155">Problem 8756 har åtgärdats: Fel vid användning av TargetListenerID med AzApplicationGatewayRedirectConfiguration-cmdletar</span><span class="sxs-lookup"><span data-stu-id="08996-2155">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="08996-2156">En bugg i New-AzApplicationGatewayPathRuleConfig som gjorde att regeluppsättningen för att återskapa inte kunde anges har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="08996-2156">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="08996-2157">Visningen av VirtualNetworkTaps i NetworkInterfaceIpConfiguration har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="08996-2157">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="08996-2158">Cortex Get-cmdletar för att visa en lista med alla delar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="08996-2158">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="08996-2159">Funktionen för att skapa VirtualHub-referenser för ExpressRouteGateways och VpnGateway har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="08996-2159">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="08996-2160">Stöd för tillgänglighetszoner i AzureFirewall och NatGateway har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-2160">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="08996-2161">Cmdleten Get-AzNetworkServiceTag har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-2161">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="08996-2162">Lägg till stöd för flera offentliga IP-adresser för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="08996-2162">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="08996-2163">Cmdleten New-AzFirewall har uppdaterats:</span><span class="sxs-lookup"><span data-stu-id="08996-2163">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="08996-2164">Parametern -PublicIpAddress som accepterar ett eller flera offentliga IP-adressobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-2164">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="08996-2165">Parametern -VirtualNetwork som accepterar ett virtuellt nätverksobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-2165">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="08996-2166">Metoderna AddPublicIpAddress och RemovePublicIpAddress har lagts till på brandväggsobjekt – dessa accepterar ett offentligt IP-adressobjekt som indata</span><span class="sxs-lookup"><span data-stu-id="08996-2166">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="08996-2167">Inaktuella parametrar -PublicIpName och -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="08996-2167">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="08996-2168">Nedanstående kommandon för funktionen har uppdaterats: Ange autentiseringsalternativ för VpnClient AAD till resurser för virtuella nätverksgatewayer.</span><span class="sxs-lookup"><span data-stu-id="08996-2168">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="08996-2169">New-AzVirtualNetworkGateway har uppdaterats: De valfria parametrarna AadTenantUri, AadAudienceId och AadIssuerUri för att ange VpnClient AAD-autentiseringsalternativ på en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="08996-2169">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="08996-2170">Set-AzVirtualNetworkGateway har uppdaterats: De valfria parametrarna AadTenantUri, AadAudienceId och AadIssuerUri för att ange VpnClient AAD-autentiseringsalternativ på en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="08996-2170">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="08996-2171">Set-AzVirtualNetworkGateway har uppdaterats: Den valfria växelparametern RemoveAadAuthentication som tar bort VpnClient AAD-autentiseringsalternativ från en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="08996-2171">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="08996-2172">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="08996-2172">Az.OperationalInsights</span></span>
* <span data-ttu-id="08996-2173">Aktivera prisnivån **pergb2018** i kommandot ”New-AzureRmOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="08996-2173">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="08996-2174">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08996-2174">Az.Resources</span></span>
* <span data-ttu-id="08996-2175">Stöd för ytterligare alternativ för att exportera en mall</span><span class="sxs-lookup"><span data-stu-id="08996-2175">Support for additional Template Export options</span></span>
    - <span data-ttu-id="08996-2176">Lägg till parametern ”-SkipResourceNameParameterization” till Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="08996-2176">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="08996-2177">Lägg till parametern ”-SkipAllParameterization” till Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="08996-2177">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="08996-2178">Lägg till parametern ”-Resource” till Export-AzResourceGroup för exporterad resursfiltrering</span><span class="sxs-lookup"><span data-stu-id="08996-2178">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="08996-2179">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="08996-2179">Az.ServiceFabric</span></span>
* <span data-ttu-id="08996-2180">Åtgärda att fel tumavtryck används vid tilläggning av certifikat i ByExistingKeyVault i vissa fall</span><span class="sxs-lookup"><span data-stu-id="08996-2180">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="08996-2181">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08996-2181">Az.Sql</span></span>
* <span data-ttu-id="08996-2182">Åtgärda suffix för lagringsslutpunkt i Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="08996-2182">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="08996-2183">Åtgärda att aktivering av Advanced Data Security åsidosätter Advanced Threat Protection-princip</span><span class="sxs-lookup"><span data-stu-id="08996-2183">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="08996-2184">Nya cmdletar för Management.Sql som gör att kunderna kan lägga till nycklar för transparent datakryptering (TDE) och ange TDE-skydd för hanterade instanser</span><span class="sxs-lookup"><span data-stu-id="08996-2184">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="08996-2185">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="08996-2185">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="08996-2186">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="08996-2186">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="08996-2187">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="08996-2187">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="08996-2188">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="08996-2188">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="08996-2189">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="08996-2189">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="08996-2190">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="08996-2190">Az.Storage</span></span>
* <span data-ttu-id="08996-2191">Stöd för typerna FileStorage och SkuName Premium_ZRS när lagringskonton skapas</span><span class="sxs-lookup"><span data-stu-id="08996-2191">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="08996-2192">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="08996-2192">New-AzStorageAccount</span></span>
* <span data-ttu-id="08996-2193">Beskrivningen av cmdleten för bloboföränderlighet har förtydligats</span><span class="sxs-lookup"><span data-stu-id="08996-2193">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="08996-2194">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="08996-2194">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="08996-2195">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="08996-2195">Az.Websites</span></span>
* <span data-ttu-id="08996-2196">Optimerar Get-AzWebAppCertificate för att filtrera efter resursgrupp på servern i stället för klienten</span><span class="sxs-lookup"><span data-stu-id="08996-2196">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="08996-2197">Lägger till växlingsparametern -UseDisasterRecovery till Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="08996-2197">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="08996-2198">2.2.0 – juni 2019</span><span class="sxs-lookup"><span data-stu-id="08996-2198">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="08996-2199">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="08996-2199">Az.Cdn</span></span>
* <span data-ttu-id="08996-2200">Uppdaterade cmdletar för att ge stöd för rulesEngine-funktion baserat på API-version 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="08996-2200">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08996-2201">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08996-2201">Az.Compute</span></span>
* <span data-ttu-id="08996-2202">Lade till parameter `NoWait` som startar åtgärden och returnerar omedelbart, innan åtgärden har slutförts.</span><span class="sxs-lookup"><span data-stu-id="08996-2202">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="08996-2203">Uppdaterade cmdletar:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="08996-2203">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="08996-2204">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="08996-2204">Az.EventHub</span></span>
* <span data-ttu-id="08996-2205">Korrigering för #9231 – Get-AzEventHubNamespace returnerar inga taggar</span><span class="sxs-lookup"><span data-stu-id="08996-2205">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="08996-2206">Korrigering för #9230 – Get-AzEventHubNamespace returnerar ResourceGroup istället för ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08996-2206">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="08996-2207">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08996-2207">Az.Network</span></span>
* <span data-ttu-id="08996-2208">Uppdatera ResourceId och InputObject för NAT-gateway</span><span class="sxs-lookup"><span data-stu-id="08996-2208">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="08996-2209">Lägg till alias för ResourceId och InputObject</span><span class="sxs-lookup"><span data-stu-id="08996-2209">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="08996-2210">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="08996-2210">Az.PolicyInsights</span></span>
* <span data-ttu-id="08996-2211">Åtgärda Null-referensproblem i Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="08996-2211">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="08996-2212">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="08996-2212">Az.RecoveryServices</span></span>
* <span data-ttu-id="08996-2213">Minsta kvarhållning för IaaSVM-policy i dagar ändrat till 7 från 1</span><span class="sxs-lookup"><span data-stu-id="08996-2213">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="08996-2214">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="08996-2214">Az.ServiceBus</span></span>
* <span data-ttu-id="08996-2215">Korrigering för ärende #9182 – Get-AzServiceBusNamespace returnerar ResourceGroup istället för ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08996-2215">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="08996-2216">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="08996-2216">Az.ServiceFabric</span></span>
* <span data-ttu-id="08996-2217">Åtgärda stavfel i felmeddelandet för Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="08996-2217">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="08996-2218">Åtgärda saknat tecken i Service Fabric-kommandorader</span><span class="sxs-lookup"><span data-stu-id="08996-2218">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="08996-2219">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08996-2219">Az.Sql</span></span>
* <span data-ttu-id="08996-2220">Lägg till parametern DnsZonePartner för New-AzureSqlInstance-cmdlet för att ge stöd för AutoDr för hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="08996-2220">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="08996-2221">Avvecklar cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="08996-2221">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="08996-2222">Döp om cmdletar för hotidentifiering till Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="08996-2222">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="08996-2223">Parametrarna New-AzSqlInstance -StorageSizeInGB och -LicenseType är nu valfria.</span><span class="sxs-lookup"><span data-stu-id="08996-2223">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="08996-2224">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="08996-2224">Az.Websites</span></span>
* <span data-ttu-id="08996-2225">åtgärdar problemet där användningen av Set-AzWebApp och Set-AzWebAppSlot med -WebApp-egenskap tog bort taggarna</span><span class="sxs-lookup"><span data-stu-id="08996-2225">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="08996-2226">2.1.0 – maj 2019</span><span class="sxs-lookup"><span data-stu-id="08996-2226">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="08996-2227">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="08996-2227">Az.ApiManagement</span></span>
* <span data-ttu-id="08996-2228">Skapade nya cmdletar för att hantera diagnostik för global- och API-omfång</span><span class="sxs-lookup"><span data-stu-id="08996-2228">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="08996-2229">**Get-AzApiManagementDiagnostic** – Skaffa diagnostik konfigurerad för global- eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="08996-2229">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="08996-2230">**New-AzApiManagementDiagnostic** – Skapa ny diagnostik för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="08996-2230">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="08996-2231">**New-AzApiManagementHttpMessageDiagnostic** – Skapa diagnostikinställning om vilka rubriker som ska loggas och storleken på brödtextbyte</span><span class="sxs-lookup"><span data-stu-id="08996-2231">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="08996-2232">**New-AzApiManagementPipelineDiagnosticSetting** – Skapa diagnostikinställningar för inkommande/utgående HTTP-meddelanden till gatewayen.</span><span class="sxs-lookup"><span data-stu-id="08996-2232">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="08996-2233">**New-AzApiManagementSamplingSetting** – Skapa samplinginställningar för begäranden/svar för en diagnostik</span><span class="sxs-lookup"><span data-stu-id="08996-2233">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="08996-2234">**Remove-AzApiManagementDiagnostic** – Ta bort en diagnostikenhet för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="08996-2234">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="08996-2235">**Set-AzApiManagementDiagnostic** – Uppdatera en diagnostikenhet för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="08996-2235">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="08996-2236">Skapade nya cmdletar för hantering av cacheminne i ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="08996-2236">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="08996-2237">**Get-AzApiManagementCache** – Hämta information om cacheminnet som anges av identifierare eller alla cacheminnen</span><span class="sxs-lookup"><span data-stu-id="08996-2237">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="08996-2238">**New-AzApiManagementCache** – Skapa ett nytt default-cacheminne eller cacheminne i en viss Azure-region</span><span class="sxs-lookup"><span data-stu-id="08996-2238">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="08996-2239">**Remove-AzApiManagementCache** – Ta bort ett cacheminne</span><span class="sxs-lookup"><span data-stu-id="08996-2239">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="08996-2240">**Remove-AzApiManagementCache** – Ta bort ett cacheminne</span><span class="sxs-lookup"><span data-stu-id="08996-2240">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="08996-2241">Skapade nya cmdletar för hantering av API-schema</span><span class="sxs-lookup"><span data-stu-id="08996-2241">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="08996-2242">**New-AzApiManagementSchema** – Skapa ett nytt schema för ett API</span><span class="sxs-lookup"><span data-stu-id="08996-2242">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="08996-2243">**Get-AzApiManagementSchema** – Hämta de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="08996-2243">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="08996-2244">**Remove-AzApiManagementSchema** – Ta bort de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="08996-2244">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="08996-2245">**Set-AzApiManagementSchema** – Uppdatera de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="08996-2245">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="08996-2246">Skapa ny cmdlet för att generera en användartoken.</span><span class="sxs-lookup"><span data-stu-id="08996-2246">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="08996-2247">**New-AzApiManagementUserToken** – Skapa en ny användartoken som enligt standardinställning är giltig i 8 timmar. Token för GIT-användaren kan skapas med den här cmdleten./</span><span class="sxs-lookup"><span data-stu-id="08996-2247">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="08996-2248">Skapade en ny cmdlet för att hämta nätverksstatus</span><span class="sxs-lookup"><span data-stu-id="08996-2248">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="08996-2249">**Get-AzApiManagementNetworkStatus** – Hämta nätverksstatusanslutningen för resurserna som API Management-tjänsten är beroende av.</span><span class="sxs-lookup"><span data-stu-id="08996-2249">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="08996-2250">Det här är användbart när du distribuerar ApiManagement-tjänsten i ett virtuellt nätverk och validerar om något beroende är brutet.</span><span class="sxs-lookup"><span data-stu-id="08996-2250">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="08996-2251">Uppdaterade cmdlet **New-AzApiManagement** för att hantera ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="08996-2251">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="08996-2252">Lade till stöd för den nya SKU:n Consumption</span><span class="sxs-lookup"><span data-stu-id="08996-2252">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="08996-2253">Aktiverade stöd för att slå på flaggan EnableClientCertificate för SKU:n Consumption</span><span class="sxs-lookup"><span data-stu-id="08996-2253">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="08996-2254">Den nya cmdleten **New-AzApiManagementSslSetting** gör det möjligt att ställa in TLS/SSL-inställningen på ”Backend” och ”Frontend” (serverdel och klientdel).</span><span class="sxs-lookup"><span data-stu-id="08996-2254">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="08996-2255">Det här kan också användas till att konfigurera chiffer som 3DES och ServerProtocols som Http2 för Frontend för en ApiManagement-tjänst.</span><span class="sxs-lookup"><span data-stu-id="08996-2255">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="08996-2256">Stöd har lagts till för att konfigurera värdnamnet DeveloperPortal på ApiManagement-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="08996-2256">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="08996-2257">Uppdaterade cmdletar **Get-AzApiManagementSsoToken** för att ta PsApiManagement-objekt som indata</span><span class="sxs-lookup"><span data-stu-id="08996-2257">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="08996-2258">Uppdaterad cmdleten för att visa infogade felmeddelanden</span><span class="sxs-lookup"><span data-stu-id="08996-2258">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="08996-2259">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Felkod: Felmeddelande av typen ValidationError: Ett eller flera fält innehåller felaktiga värden: Felinformation:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="08996-2259">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="08996-2260">Uppdaterade cmdlet **Export-AzApiManagementApi** för att exportera API:er i OpenApi 3.0-format</span><span class="sxs-lookup"><span data-stu-id="08996-2260">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="08996-2261">Uppdaterade cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="08996-2261">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="08996-2262">Importera API från dokumentspecifikationen OpenApi 3.0</span><span class="sxs-lookup"><span data-stu-id="08996-2262">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="08996-2263">Om du vill åsidosätta egenskapen PsApiManagementSchema specificerad i ett dokument (Swagger, Wadl, Wsdl, OpenApi).</span><span class="sxs-lookup"><span data-stu-id="08996-2263">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="08996-2264">Åsidosätta egenskapen ServiceUrl som specificeras i ett dokument.</span><span class="sxs-lookup"><span data-stu-id="08996-2264">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="08996-2265">Uppdaterade cmdlet **Get-AzApiManagementPolicy** för att returnera policy i undantaget format av typen icke-XML med rawxml</span><span class="sxs-lookup"><span data-stu-id="08996-2265">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="08996-2266">Uppdaterade cmdlet **Set-AzApiManagementPolicy** för att godkänna policy i undantaget format av typen icke-XML med rawxml och XML undantaget med xml</span><span class="sxs-lookup"><span data-stu-id="08996-2266">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="08996-2267">Uppdaterad cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="08996-2267">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="08996-2268">Konfigurera API med OpenId auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="08996-2268">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="08996-2269">Skapa ett API i ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="08996-2269">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="08996-2270">Klona ett API med SourceApiId och SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="08996-2270">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="08996-2271">Möjlighet att konfigurera SubscriptionRequired i API-omfattningen.</span><span class="sxs-lookup"><span data-stu-id="08996-2271">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="08996-2272">Uppdaterad cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="08996-2272">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="08996-2273">Konfigurera API med OpenId auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="08996-2273">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="08996-2274">Uppdatera ett API till ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="08996-2274">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="08996-2275">Möjlighet att konfigurera SubscriptionRequired i API-omfattningen.</span><span class="sxs-lookup"><span data-stu-id="08996-2275">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="08996-2276">Uppdaterad cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="08996-2276">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="08996-2277">Klona en befintlig version med hjälp av SourceApiRevision (kopiera taggar, produkter, åtgärder och principer).</span><span class="sxs-lookup"><span data-stu-id="08996-2277">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="08996-2278">Den nya revisionen antar ApiId från den överordnade instansen.</span><span class="sxs-lookup"><span data-stu-id="08996-2278">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="08996-2279">Tillhandahålla ApiRevisionDescription</span><span class="sxs-lookup"><span data-stu-id="08996-2279">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="08996-2280">Åsidosätta ServiceUrl vid kloning av ett API.</span><span class="sxs-lookup"><span data-stu-id="08996-2280">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="08996-2281">Uppdaterad cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="08996-2281">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="08996-2282">Konfigurera AAD eller AADB2C med en Authority</span><span class="sxs-lookup"><span data-stu-id="08996-2282">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="08996-2283">Konfigurera SignupPolicy, SigninPolicy, ProfileEditingPolicy och PasswordResetPolicy</span><span class="sxs-lookup"><span data-stu-id="08996-2283">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="08996-2284">Uppdaterad cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="08996-2284">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="08996-2285">Kompensera för ny SubscriptonModel med Scope och UserId</span><span class="sxs-lookup"><span data-stu-id="08996-2285">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="08996-2286">Kompensera för gammal prenumerationsmodell med ProductId och UserId</span><span class="sxs-lookup"><span data-stu-id="08996-2286">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="08996-2287">Lägg till funktion för att aktivera AllowTracing på prenumerationsnivå.</span><span class="sxs-lookup"><span data-stu-id="08996-2287">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="08996-2288">Uppdaterad cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="08996-2288">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="08996-2289">Kompensera för ny SubscriptonModel med Scope och UserId</span><span class="sxs-lookup"><span data-stu-id="08996-2289">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="08996-2290">Kompensera för gammal prenumerationsmodell med ProductId och UserId</span><span class="sxs-lookup"><span data-stu-id="08996-2290">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="08996-2291">Lägg till funktion för att aktivera AllowTracing på prenumerationsnivå.</span><span class="sxs-lookup"><span data-stu-id="08996-2291">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="08996-2292">Uppdaterade följande cmdletar för att acceptera ResourceId som indata</span><span class="sxs-lookup"><span data-stu-id="08996-2292">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="08996-2293">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="08996-2293">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="08996-2294">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="08996-2294">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="08996-2295">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="08996-2295">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="08996-2296">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="08996-2296">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="08996-2297">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="08996-2297">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="08996-2298">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="08996-2298">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="08996-2299">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="08996-2299">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="08996-2300">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="08996-2300">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="08996-2301">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="08996-2301">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="08996-2302">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="08996-2302">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="08996-2303">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="08996-2303">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="08996-2304">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="08996-2304">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="08996-2305">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="08996-2305">Az.Automation</span></span>
* <span data-ttu-id="08996-2306">Uppdaterade Get-AzAutomationJobOutputRecord för att hantera postvärden av typen JSON och Text.</span><span class="sxs-lookup"><span data-stu-id="08996-2306">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="08996-2307">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="08996-2307">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="08996-2308">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="08996-2308">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="08996-2309">Ändrade beteende för Start-AzAutomationDscCompilationJob till att bara starta jobbet istället för att vänta på slutförandet.</span><span class="sxs-lookup"><span data-stu-id="08996-2309">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="08996-2310">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="08996-2310">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="08996-2311">Korrigering för Get-AzAutomationDscNode när using -Name returnerar alla noder.</span><span class="sxs-lookup"><span data-stu-id="08996-2311">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="08996-2312">Nu returnerar den endast den matchande noden.</span><span class="sxs-lookup"><span data-stu-id="08996-2312">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08996-2313">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08996-2313">Az.Compute</span></span>
* <span data-ttu-id="08996-2314">Lägg till parametrarna ProtectFromScaleIn och ProtectFromScaleSetAction i cmdleten Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="08996-2314">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="08996-2315">Nu är standardinställningen att vimpelparametern New-AzVM använder en tillgänglig plats om USA, östra inte stöds</span><span class="sxs-lookup"><span data-stu-id="08996-2315">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="08996-2316">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="08996-2316">Az.DataLakeStore</span></span>
* <span data-ttu-id="08996-2317">Uppdatera ADLS-sdk för att använda httpclient, integrera dataplanstestning med Azure-ramverk</span><span class="sxs-lookup"><span data-stu-id="08996-2317">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="08996-2318">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="08996-2318">Az.Monitor</span></span>
* <span data-ttu-id="08996-2319">Korrigera felaktiga parameternamn i hjälpexempel</span><span class="sxs-lookup"><span data-stu-id="08996-2319">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="08996-2320">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08996-2320">Az.Network</span></span>
* <span data-ttu-id="08996-2321">Lägg till flaggan DisableBgpRoutePropagation i utdata för effektiv routningstabell</span><span class="sxs-lookup"><span data-stu-id="08996-2321">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="08996-2322">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="08996-2322">Updated cmdlet:</span></span>
        - <span data-ttu-id="08996-2323">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="08996-2323">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="08996-2324">Åtgärda dubbelstreck i dokumentationen New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="08996-2324">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="08996-2325">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08996-2325">Az.Resources</span></span>
* <span data-ttu-id="08996-2326">Lägg till ny cmdlet Get-AzureRmDenyAssignment för att hämta tilldelningsnekanden</span><span class="sxs-lookup"><span data-stu-id="08996-2326">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="08996-2327">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08996-2327">Az.Sql</span></span>
* <span data-ttu-id="08996-2328">Döp om Advanced Threat Protection-cmdletar för Advanced Data Security och aktivera Vulnerability Assessment som standard</span><span class="sxs-lookup"><span data-stu-id="08996-2328">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="08996-2329">2.0.0 – maj 2019</span><span class="sxs-lookup"><span data-stu-id="08996-2329">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="08996-2330">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="08996-2330">Az.Accounts</span></span>
* <span data-ttu-id="08996-2331">Uppdatera autentiseringsbiblioteket för att åtgärda ADFS-problem med autentisering av användarnamn/lösenord</span><span class="sxs-lookup"><span data-stu-id="08996-2331">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="08996-2332">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="08996-2332">Az.CognitiveServices</span></span>
* <span data-ttu-id="08996-2333">Visa endast Bing-ansvarsfriskrivning för Bing-sökningstjänster.</span><span class="sxs-lookup"><span data-stu-id="08996-2333">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="08996-2334">Förbättra felmeddelande när det inte går att skapa konton.</span><span class="sxs-lookup"><span data-stu-id="08996-2334">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08996-2335">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08996-2335">Az.Compute</span></span>
* <span data-ttu-id="08996-2336">Funktion för närhetsplaceringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="08996-2336">Proximity placement group feature.</span></span>
    - <span data-ttu-id="08996-2337">Följande nya cmdletar har lagts till:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="08996-2337">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="08996-2338">Den nya parametern ProximityPlacementGroupId har lagts till i följande cmdletar:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="08996-2338">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="08996-2339">Parametern StorageAccountType har lagts till i New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="08996-2339">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="08996-2340">TargetRegion för New-AzGalleryImageVersion kan innehålla StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="08996-2340">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="08996-2341">Växlingsparametern SkipShutdown har lagts till i Stop-AzVM och Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="08996-2341">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="08996-2342">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="08996-2342">Breaking changes</span></span>
    - <span data-ttu-id="08996-2343">Set-AzVMBootDiagnostics har ändrats till Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="08996-2343">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="08996-2344">Export-AzLogAnalyticThrottledRequests har ändrats till Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="08996-2344">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="08996-2345">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="08996-2345">Az.DeploymentManager</span></span>
* <span data-ttu-id="08996-2346">De första allmänt tillgängliga versionerna av cmdletar för Distributionshanteraren i Azure</span><span class="sxs-lookup"><span data-stu-id="08996-2346">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="08996-2347">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="08996-2347">Az.Dns</span></span>
* <span data-ttu-id="08996-2348">Automatisk delegering av DNS för NameServer</span><span class="sxs-lookup"><span data-stu-id="08996-2348">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="08996-2349">Det överordnade zonnamnet kan användas som ytterligare valfri parameter i cmdleten för att skapa DNS-zoner.</span><span class="sxs-lookup"><span data-stu-id="08996-2349">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="08996-2350">Lägger till NS-poster för en nyligen skapad underordnad zon i den överordnade zonen.</span><span class="sxs-lookup"><span data-stu-id="08996-2350">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="08996-2351">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="08996-2351">Az.FrontDoor</span></span>
* <span data-ttu-id="08996-2352">De första allmänt tillgängliga versionerna av cmdletar för Azure FrontDoor</span><span class="sxs-lookup"><span data-stu-id="08996-2352">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="08996-2353">Byt namn på WAF-cmdletar så att de omfattar ”Waf”</span><span class="sxs-lookup"><span data-stu-id="08996-2353">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="08996-2354">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="08996-2354">Az.HDInsight</span></span>
* <span data-ttu-id="08996-2355">Två cmdletar har tagits bort:</span><span class="sxs-lookup"><span data-stu-id="08996-2355">Removed two cmdlets:</span></span>
    - <span data-ttu-id="08996-2356">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="08996-2356">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="08996-2357">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="08996-2357">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="08996-2358">En ny cmdlet har lagts till, Set-AzHDInsightGatewayCredential, som ersätter Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="08996-2358">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="08996-2359">Uppdatera cmdleten Get-AzHDInsightJobOutput för att skilja mellan läsarrollen och HDInsight-operatörsrollen:</span><span class="sxs-lookup"><span data-stu-id="08996-2359">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="08996-2360">Användare med läsarrollen måste uttryckligen ange parametern ”DefaultStorageAccountKey”, annars uppstår fel.</span><span class="sxs-lookup"><span data-stu-id="08996-2360">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="08996-2361">Användare med HDInsight-operatörsrollen påverkas inte.</span><span class="sxs-lookup"><span data-stu-id="08996-2361">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="08996-2362">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="08996-2362">Az.Monitor</span></span>
* <span data-ttu-id="08996-2363">Nya cmdletar för SQR API (schemalagd frågeregel)</span><span class="sxs-lookup"><span data-stu-id="08996-2363">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="08996-2364">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="08996-2364">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="08996-2365">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="08996-2365">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="08996-2366">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="08996-2366">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="08996-2367">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="08996-2367">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="08996-2368">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="08996-2368">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="08996-2369">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="08996-2369">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="08996-2370">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="08996-2370">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="08996-2371">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="08996-2371">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="08996-2372">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="08996-2372">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="08996-2373">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="08996-2373">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="08996-2374">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="08996-2374">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="08996-2375">[Mer](/rest/api/monitor/scheduledqueryrules) information om SQR API</span><span class="sxs-lookup"><span data-stu-id="08996-2375">[More](/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="08996-2376">Az.Monitor.md har uppdaterats för att omfatta cmdletar för måttbaserade aviseringsregler i GenV2 (inte klassiska)</span><span class="sxs-lookup"><span data-stu-id="08996-2376">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="08996-2377">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08996-2377">Az.Network</span></span>
* <span data-ttu-id="08996-2378">Lägg till stöd för NAT Gateway-resurs</span><span class="sxs-lookup"><span data-stu-id="08996-2378">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="08996-2379">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="08996-2379">New cmdlets</span></span>
        - <span data-ttu-id="08996-2380">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="08996-2380">New-AzNatGateway</span></span>
        - <span data-ttu-id="08996-2381">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="08996-2381">Get-AzNatGateway</span></span>
        - <span data-ttu-id="08996-2382">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="08996-2382">Set-AzNatGateway</span></span>
        - <span data-ttu-id="08996-2383">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="08996-2383">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="08996-2384">Uppdaterade cmdletar</span><span class="sxs-lookup"><span data-stu-id="08996-2384">Updated cmdlets</span></span>
        - <span data-ttu-id="08996-2385">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="08996-2385">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="08996-2386">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="08996-2386">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="08996-2387">Nedanstående kommandon för funktionen har uppdaterats: Ange/ta bort anpassade vägar på Brooklyn Gateway.</span><span class="sxs-lookup"><span data-stu-id="08996-2387">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="08996-2388">New-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ställa in adressprefix som anpassade vägar för att ange gateway.</span><span class="sxs-lookup"><span data-stu-id="08996-2388">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="08996-2389">Set-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ange adressprefix som anpassade vägar för att ange gateway.</span><span class="sxs-lookup"><span data-stu-id="08996-2389">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="08996-2390">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="08996-2390">Az.PolicyInsights</span></span>
* <span data-ttu-id="08996-2391">Stöd för att fråga efter information om principutvärdering.</span><span class="sxs-lookup"><span data-stu-id="08996-2391">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="08996-2392">Lägg till parametern ”-Expand” för Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="08996-2392">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="08996-2393">Stöd för -Expand PolicyEvaluationDetails.</span><span class="sxs-lookup"><span data-stu-id="08996-2393">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="08996-2394">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="08996-2394">Az.RecoveryServices</span></span>
* <span data-ttu-id="08996-2395">Stöd för att dela prenumeration mellan Azure och Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="08996-2395">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="08996-2396">Markering av kommande icke-bakåtkompatibla ändringar för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="08996-2396">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="08996-2397">Korrigering för återställningsplan och åtgärdsplan i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="08996-2397">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="08996-2398">Korrigering för mappning av uppdateringsnätverk i Azure Site Recovery för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="08996-2398">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="08996-2399">Korrigering för instruktioner för uppdateringsskydd i Azure Site Recovery för Azure till Azure för hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="08996-2399">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="08996-2400">Andra mindre korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="08996-2400">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="08996-2401">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="08996-2401">Az.Relay</span></span>
* <span data-ttu-id="08996-2402">Korrigera stavfel i kundriktade meddelanden</span><span class="sxs-lookup"><span data-stu-id="08996-2402">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="08996-2403">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="08996-2403">Az.ServiceBus</span></span>
* <span data-ttu-id="08996-2404">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="08996-2404">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="08996-2405">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="08996-2405">Az.Storage</span></span>
* <span data-ttu-id="08996-2406">Uppgradera till lagringsklientbiblioteket 10.0.1 (namnområdet för alla objekt från detta SDK ändras från ”Microsoft.WindowsAzure.Storage. *till ”Microsoft.Azure.Storage.* ”)</span><span class="sxs-lookup"><span data-stu-id="08996-2406">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="08996-2407">Uppgradera till Microsoft.Azure.Management.Storage 11.0.0 för att stödja den nya API-versionen 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="08996-2407">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="08996-2408">Standardlagringskontot i Skapa lagringskonto ändras från ”Storage” till ”StorageV2”</span><span class="sxs-lookup"><span data-stu-id="08996-2408">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="08996-2409">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="08996-2409">New-AzStorageAccount</span></span>
* <span data-ttu-id="08996-2410">Ändra lagringskontots cmdlet-utdata Sku.Name för att passa med indata-SkuName genom att lägga till ”-”. Till exempel ändras ”StandardLRS” till ”Standard_LRS”</span><span class="sxs-lookup"><span data-stu-id="08996-2410">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="08996-2411">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="08996-2411">New-AzStorageAccount</span></span>
    - <span data-ttu-id="08996-2412">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="08996-2412">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="08996-2413">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="08996-2413">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="08996-2414">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="08996-2414">Az.Websites</span></span>
* <span data-ttu-id="08996-2415">Egenskapen ”typ” konfigureras nu för PSSite-objekt som returneras av Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="08996-2415">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="08996-2416">Get-AzWebApp\*Metrics och Get-AzAppServicePlanMetrics markeras som inaktuella</span><span class="sxs-lookup"><span data-stu-id="08996-2416">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="08996-2417">1.8.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="08996-2417">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="08996-2418">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="08996-2418">Highlights since the last major release</span></span>
* <span data-ttu-id="08996-2419">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="08996-2419">General availability of `Az` module</span></span>
* <span data-ttu-id="08996-2420">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="08996-2420">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="08996-2421">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="08996-2421">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="08996-2422">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-2422">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="08996-2423">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-2423">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="08996-2424">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-2424">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="08996-2425">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="08996-2425">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="08996-2426">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="08996-2426">Az.Accounts</span></span>
* <span data-ttu-id="08996-2427">Uppdatera Uninstall-AzureRm för att ta bort moduler i Mac på ett korrekt sätt</span><span class="sxs-lookup"><span data-stu-id="08996-2427">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="08996-2428">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="08996-2428">Az.Batch</span></span>
* <span data-ttu-id="08996-2429">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="08996-2429">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="08996-2430">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="08996-2430">Az.Cdn</span></span>
* <span data-ttu-id="08996-2431">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="08996-2431">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="08996-2432">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="08996-2432">Az.CognitiveServices</span></span>
* <span data-ttu-id="08996-2433">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="08996-2433">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08996-2434">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08996-2434">Az.Compute</span></span>
* <span data-ttu-id="08996-2435">Åtgärda problem med AEM-installationen om resurs-ID:n för diskar innehåller resourcegroups i gemener i resurs-ID:n</span><span class="sxs-lookup"><span data-stu-id="08996-2435">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="08996-2436">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="08996-2436">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="08996-2437">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="08996-2437">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="08996-2438">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="08996-2438">Az.DataFactory</span></span>
* <span data-ttu-id="08996-2439">Lägg till SsisProperties om NodeCount inte är null för hanterad integreringskörning.</span><span class="sxs-lookup"><span data-stu-id="08996-2439">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="08996-2440">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="08996-2440">Az.DataLakeStore</span></span>
* <span data-ttu-id="08996-2441">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="08996-2441">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="08996-2442">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="08996-2442">Az.EventGrid</span></span>
* <span data-ttu-id="08996-2443">Hjälptexten för slutpunkten har uppdaterats för att visa att resurser ska skapas innan cmdletarna för att skapa/uppdatera händelseprenumerationer används.</span><span class="sxs-lookup"><span data-stu-id="08996-2443">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="08996-2444">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="08996-2444">Az.EventHub</span></span>
* <span data-ttu-id="08996-2445">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="08996-2445">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="08996-2446">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="08996-2446">Az.HDInsight</span></span>
* <span data-ttu-id="08996-2447">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="08996-2447">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="08996-2448">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="08996-2448">Az.IotHub</span></span>
* <span data-ttu-id="08996-2449">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="08996-2449">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="08996-2450">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="08996-2450">Az.KeyVault</span></span>
* <span data-ttu-id="08996-2451">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="08996-2451">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="08996-2452">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="08996-2452">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="08996-2453">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="08996-2453">Az.MachineLearning</span></span>
* <span data-ttu-id="08996-2454">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="08996-2454">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="08996-2455">Az.Media</span><span class="sxs-lookup"><span data-stu-id="08996-2455">Az.Media</span></span>
* <span data-ttu-id="08996-2456">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="08996-2456">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="08996-2457">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="08996-2457">Az.Monitor</span></span>
  * <span data-ttu-id="08996-2458">Nya cmdletar för måttbaserad aviseringsregel i GenV2 (inte klassisk)</span><span class="sxs-lookup"><span data-stu-id="08996-2458">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="08996-2459">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="08996-2459">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="08996-2460">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="08996-2460">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="08996-2461">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="08996-2461">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="08996-2462">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="08996-2462">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="08996-2463">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="08996-2463">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="08996-2464">Monitor SDK har uppdaterats till version 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="08996-2464">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="08996-2465">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08996-2465">Az.Network</span></span>
* <span data-ttu-id="08996-2466">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="08996-2466">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="08996-2467">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="08996-2467">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="08996-2468">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="08996-2468">Az.NotificationHubs</span></span>
* <span data-ttu-id="08996-2469">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="08996-2469">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="08996-2470">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="08996-2470">Az.OperationalInsights</span></span>
* <span data-ttu-id="08996-2471">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="08996-2471">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="08996-2472">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="08996-2472">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="08996-2473">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="08996-2473">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="08996-2474">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="08996-2474">Az.RecoveryServices</span></span>
* <span data-ttu-id="08996-2475">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="08996-2475">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="08996-2476">Tabellformatet för SQL i virtuella Azure-datorer har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="08996-2476">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="08996-2477">En alternativ metod för att hämta platser i AzureFileShare har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-2477">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="08996-2478">ScheduleRunDays i SchedulePolicy-objekt har uppdaterats enligt tidszon</span><span class="sxs-lookup"><span data-stu-id="08996-2478">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="08996-2479">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="08996-2479">Az.RedisCache</span></span>
* <span data-ttu-id="08996-2480">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="08996-2480">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="08996-2481">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08996-2481">Az.Resources</span></span>
* <span data-ttu-id="08996-2482">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="08996-2482">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="08996-2483">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08996-2483">Az.Sql</span></span>
* <span data-ttu-id="08996-2484">Ersätt Monitor SDK-beroende med vanlig kod</span><span class="sxs-lookup"><span data-stu-id="08996-2484">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="08996-2485">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="08996-2485">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="08996-2486">Förbättrad process för klassificering av flera kolumner.</span><span class="sxs-lookup"><span data-stu-id="08996-2486">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="08996-2487">Inkludera SKU-egenskaper (SKU-namn, serie, kapacitet) i svaret från Get-AzSqlServerServiceObjective och formatera som tabell som standard.</span><span class="sxs-lookup"><span data-stu-id="08996-2487">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="08996-2488">Möjlighet att använda Get-AzSqlServerServiceObjective efter plats utan att behöva en redan befintlig server i regionen.</span><span class="sxs-lookup"><span data-stu-id="08996-2488">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="08996-2489">Stöd för tidszonsparametern när hanterade instanser skapas.</span><span class="sxs-lookup"><span data-stu-id="08996-2489">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="08996-2490">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="08996-2490">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="08996-2491">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="08996-2491">Az.Websites</span></span>
* <span data-ttu-id="08996-2492">åtgärdar Set-AzWebApp och Set-AzWebAppSlot så att de inte tar bort taggar vid körning</span><span class="sxs-lookup"><span data-stu-id="08996-2492">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="08996-2493">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="08996-2493">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="08996-2494">SDK för WebSites har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="08996-2494">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="08996-2495">Egenskapen AdminSiteName har tagits bort från PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="08996-2495">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="08996-2496">1.7.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="08996-2496">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="08996-2497">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="08996-2497">Highlights since the last major release</span></span>
* <span data-ttu-id="08996-2498">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="08996-2498">General availability of `Az` module</span></span>
* <span data-ttu-id="08996-2499">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="08996-2499">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="08996-2500">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="08996-2500">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="08996-2501">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-2501">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="08996-2502">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-2502">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="08996-2503">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-2503">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="08996-2504">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="08996-2504">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="08996-2505">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="08996-2505">Az.Accounts</span></span>
* <span data-ttu-id="08996-2506">Add-AzEnvironment och Set-AzEnvironment har uppdaterats för att godkänna parametern AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="08996-2506">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="08996-2507">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="08996-2507">Az.AnalysisServices</span></span>
* <span data-ttu-id="08996-2508">ServiceClient används i cmdletar för dataplan och den ursprungliga autentiseringslogiken har tagits bort</span><span class="sxs-lookup"><span data-stu-id="08996-2508">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="08996-2509">Add-AzureASAccount används för omslutning av Connect-AzAccount för att undvika en icke-bakåtkompatibel ändring</span><span class="sxs-lookup"><span data-stu-id="08996-2509">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="08996-2510">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="08996-2510">Az.Automation</span></span>
* <span data-ttu-id="08996-2511">Buggen för cmdleten New-AzAutomationSoftwareUpdateConfiguration för inkluderingar har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="08996-2511">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="08996-2512">Nu bör parametern IncludedKbNumber och IncludedPackageNameMask fungera.</span><span class="sxs-lookup"><span data-stu-id="08996-2512">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="08996-2513">Felkorrigering för dynamiska grupper i uppdateringshanteringen för azure automation</span><span class="sxs-lookup"><span data-stu-id="08996-2513">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08996-2514">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08996-2514">Az.Compute</span></span>
* <span data-ttu-id="08996-2515">Lägg till parametern HyperVGeneration i New-AzDiskConfig och New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="08996-2515">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="08996-2516">Tillåt att virtuella datorer skapas med galleribilder från andra klientorganisationer.</span><span class="sxs-lookup"><span data-stu-id="08996-2516">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="08996-2517">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="08996-2517">Az.ContainerInstance</span></span>
* <span data-ttu-id="08996-2518">Ett problem har åtgärdats i parametern -Command för New-AzContainerGroup som lade till ett avslutande tomt argument</span><span class="sxs-lookup"><span data-stu-id="08996-2518">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="08996-2519">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="08996-2519">Az.DataFactory</span></span>
* <span data-ttu-id="08996-2520">ADF .Net SDK-versionen har uppdaterats till 3.0.2</span><span class="sxs-lookup"><span data-stu-id="08996-2520">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="08996-2521">Cmdleten Set-AzDataFactoryV2 har uppdaterats med extra parametrar för inställningar som rör RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="08996-2521">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="08996-2522">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08996-2522">Az.Resources</span></span>
* <span data-ttu-id="08996-2523">Förbättra hanteringen av providrar för Get-AzResource när parametrarna -ResourceId eller -ResourceGroupName, -Name och -ResourceType tillhandahålls</span><span class="sxs-lookup"><span data-stu-id="08996-2523">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="08996-2524">Förbättra felhanteringen för ”Test-AzDeployment” och ”Test-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="08996-2524">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="08996-2525">Hantera fel utanför distributionsvalideringen och ta med dem i kommandoutdata istället</span><span class="sxs-lookup"><span data-stu-id="08996-2525">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="08996-2526">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="08996-2526">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="08996-2527">Lägg till växlingsparametern -IgnoreDynamicParameters till en uppsättning av cmdletar för distribution för att hoppa över fråga i skript och jobbscenarier</span><span class="sxs-lookup"><span data-stu-id="08996-2527">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="08996-2528">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="08996-2528">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="08996-2529">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08996-2529">Az.Sql</span></span>
* <span data-ttu-id="08996-2530">Stöd för dataklassificering av databaser.</span><span class="sxs-lookup"><span data-stu-id="08996-2530">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="08996-2531">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="08996-2531">Az.Storage</span></span>
* <span data-ttu-id="08996-2532">Rapportera detaljfel när lagringskontext skapas med parametern -UseConnectedAccount, men utan inloggning på Azure-kontot</span><span class="sxs-lookup"><span data-stu-id="08996-2532">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="08996-2533">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="08996-2533">New-AzStorageContext</span></span>
* <span data-ttu-id="08996-2534">Stöd för att hantera Blob Service-egenskaper för ett angivet lagringskonto med API:et för hanteringsplan</span><span class="sxs-lookup"><span data-stu-id="08996-2534">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="08996-2535">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="08996-2535">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="08996-2536">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="08996-2536">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="08996-2537">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="08996-2537">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="08996-2538">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="08996-2538">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="08996-2539">Stöd för -AsJob-cmdletar för att ladda upp och ladda ned blobar och filer</span><span class="sxs-lookup"><span data-stu-id="08996-2539">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="08996-2540">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="08996-2540">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="08996-2541">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="08996-2541">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="08996-2542">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="08996-2542">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="08996-2543">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="08996-2543">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="08996-2544">1.6.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="08996-2544">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="08996-2545">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="08996-2545">Highlights since the last major release</span></span>
* <span data-ttu-id="08996-2546">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="08996-2546">General availability of `Az` module</span></span>
* <span data-ttu-id="08996-2547">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="08996-2547">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="08996-2548">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="08996-2548">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="08996-2549">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-2549">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="08996-2550">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-2550">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="08996-2551">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-2551">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="08996-2552">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="08996-2552">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="08996-2553">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="08996-2553">Az.Automation</span></span>
* <span data-ttu-id="08996-2554">Azure Automation – ändring av uppdateringshantering för stöd för de nya funktionerna:</span><span class="sxs-lookup"><span data-stu-id="08996-2554">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="08996-2555">Dynamisk gruppering</span><span class="sxs-lookup"><span data-stu-id="08996-2555">Dynamic grouping</span></span>
    * <span data-ttu-id="08996-2556">För-/efterskrift</span><span class="sxs-lookup"><span data-stu-id="08996-2556">Pre-Post script</span></span>
    * <span data-ttu-id="08996-2557">Inställning för omstart</span><span class="sxs-lookup"><span data-stu-id="08996-2557">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08996-2558">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08996-2558">Az.Compute</span></span>
* <span data-ttu-id="08996-2559">Åtgärda problem med sökvägsmatchning i Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="08996-2559">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="08996-2560">Uppdatera Compute-klientbibliotek till 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="08996-2560">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="08996-2561">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="08996-2561">Az.KeyVault</span></span>
* <span data-ttu-id="08996-2562">Stöd för jokertecken för KeyVault-cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-2562">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="08996-2563">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08996-2563">Az.Network</span></span>
* <span data-ttu-id="08996-2564">Lägg till stöd för Threat Intelligence för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="08996-2564">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="08996-2565">Lägg till resurs för brandväggsprincip på översta nivå och anpassade regler för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="08996-2565">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="08996-2566">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="08996-2566">Az.RecoveryServices</span></span>
* <span data-ttu-id="08996-2567">SnapshotRetentionInDays har lagts till i Azure-principen för virtuella datorer för stöd av Instant RP</span><span class="sxs-lookup"><span data-stu-id="08996-2567">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="08996-2568">Pipe-stöd för avregistrering av container har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-2568">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="08996-2569">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08996-2569">Az.Resources</span></span>
* <span data-ttu-id="08996-2570">Uppdatera stöd för jokertecken för Get-AzResource och Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="08996-2570">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="08996-2571">Uppdatera autentiseringsuppgifter som används vid allmänna anrop till ARM</span><span class="sxs-lookup"><span data-stu-id="08996-2571">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="08996-2572">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08996-2572">Az.Sql</span></span>
* <span data-ttu-id="08996-2573">Cmdlet-parametern (ExcludeDetectionType) för Hotidentifiering ändrades från DetectionType till sträng[] för att framtidssäkra den när nya DetectionTypes läggs till, och även för att stödja automatisk ifyllning.</span><span class="sxs-lookup"><span data-stu-id="08996-2573">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="08996-2574">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="08996-2574">Az.Storage</span></span>
* <span data-ttu-id="08996-2575">Stöd för att hämta/ange/ta bort hanteringsprincip på ett lagringskonto</span><span class="sxs-lookup"><span data-stu-id="08996-2575">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="08996-2576">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="08996-2576">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="08996-2577">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="08996-2577">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="08996-2578">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="08996-2578">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="08996-2579">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="08996-2579">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="08996-2580">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="08996-2580">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="08996-2581">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="08996-2581">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="08996-2582">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="08996-2582">Az.Websites</span></span>
* <span data-ttu-id="08996-2583">Åtgärda fel med ARM-mall som avbryter kloning av alla platser med 'New-AzWebApp -IncludeSourceWebAppSlots'</span><span class="sxs-lookup"><span data-stu-id="08996-2583">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="08996-2584">1.5.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="08996-2584">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="08996-2585">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="08996-2585">Az.Accounts</span></span>
* <span data-ttu-id="08996-2586">Lägg till kommandot Register-AzModule för stöd för AutoRest-genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="08996-2586">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="08996-2587">Uppdatera exempel för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="08996-2587">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="08996-2588">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="08996-2588">Az.Automation</span></span>
* <span data-ttu-id="08996-2589">Problem med att hämta vissa månadsscheman i flera Azure Automation-cmdletar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="08996-2589">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="08996-2590">Åtgärda problem med att Get-AzAutomationDscNode bara returnerar de 20 översta noderna.</span><span class="sxs-lookup"><span data-stu-id="08996-2590">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="08996-2591">Nu returneras alla noder</span><span class="sxs-lookup"><span data-stu-id="08996-2591">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="08996-2592">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="08996-2592">Az.Cdn</span></span>
* <span data-ttu-id="08996-2593">Nya Powershell-cmdletar för att aktivera/inaktivera anpassade domän-HTTPS har lagts till och de gamla har gjorts inaktuella</span><span class="sxs-lookup"><span data-stu-id="08996-2593">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08996-2594">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08996-2594">Az.Compute</span></span>
* <span data-ttu-id="08996-2595">Lägg till stöd för jokertecken för Get-cmdletar</span><span class="sxs-lookup"><span data-stu-id="08996-2595">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="08996-2596">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="08996-2596">Az.DataFactory</span></span>
* <span data-ttu-id="08996-2597">ADF .Net SDK-versionen har uppdaterats till 3.0.1</span><span class="sxs-lookup"><span data-stu-id="08996-2597">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="08996-2598">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="08996-2598">Az.LogicApp</span></span>
* <span data-ttu-id="08996-2599">Åtgärda problemet med att ListWorkflows endast hämtar den första sidan med resultat</span><span class="sxs-lookup"><span data-stu-id="08996-2599">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="08996-2600">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08996-2600">Az.Network</span></span>
* <span data-ttu-id="08996-2601">Lägg till stöd för jokertecken för Network-cmdletar</span><span class="sxs-lookup"><span data-stu-id="08996-2601">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="08996-2602">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="08996-2602">Az.RecoveryServices</span></span>
* <span data-ttu-id="08996-2603">Stöd har lagts till för SQL Server i virtuella Azure-datorer</span><span class="sxs-lookup"><span data-stu-id="08996-2603">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="08996-2604">SDK-uppdatering</span><span class="sxs-lookup"><span data-stu-id="08996-2604">SDK Update</span></span>
* <span data-ttu-id="08996-2605">Get-ProtectableItem-incheckning i VMappContainer har tagits bort</span><span class="sxs-lookup"><span data-stu-id="08996-2605">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="08996-2606">Name och ServerName har lagts till som parametrar för Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="08996-2606">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="08996-2607">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08996-2607">Az.Resources</span></span>
* <span data-ttu-id="08996-2608">Lägg till parametern `-TemplateObject` i cmdletar för distribution</span><span class="sxs-lookup"><span data-stu-id="08996-2608">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="08996-2609">Mer information här: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="08996-2609">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="08996-2610">Åtgärda problem med piping av resultatet i `Get-AzResource` till `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="08996-2610">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="08996-2611">Mer information här: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="08996-2611">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="08996-2612">Åtgärda problem med ändring av JSON-datatyp när `Set-AzResource` körs</span><span class="sxs-lookup"><span data-stu-id="08996-2612">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="08996-2613">Mer information här: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="08996-2613">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="08996-2614">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08996-2614">Az.Sql</span></span>
* <span data-ttu-id="08996-2615">AuditingEndpointsCommunicator uppdateras.</span><span class="sxs-lookup"><span data-stu-id="08996-2615">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="08996-2616">Åtgärdar beteendet hos ett gränsscenario när nya diagnostikinställningar skapas.</span><span class="sxs-lookup"><span data-stu-id="08996-2616">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="08996-2617">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="08996-2617">Az.Storage</span></span>
* <span data-ttu-id="08996-2618">Stöd för BlockBlobStorage när Storage-konto skapas      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="08996-2618">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="08996-2619">1.4.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="08996-2619">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="08996-2620">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="08996-2620">Az.AnalysisServices</span></span>
* <span data-ttu-id="08996-2621">Inaktuell AddAzureASAccount-cmdlet</span><span class="sxs-lookup"><span data-stu-id="08996-2621">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="08996-2622">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="08996-2622">Az.Automation</span></span>
* <span data-ttu-id="08996-2623">Hjälpen för Import-AzAutomationDscNodeConfiguration har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="08996-2623">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="08996-2624">Konfigurationsnamnsvalidering har lagts till i cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="08996-2624">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="08996-2625">Förbättrad felhantering för cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="08996-2625">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="08996-2626">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="08996-2626">Az.CognitiveServices</span></span>
* <span data-ttu-id="08996-2627">CustomSubdomainName har lagts till som en ny valfri parameter för New-AzCognitiveServicesAccount, som används för att ange underdomän för resursen.</span><span class="sxs-lookup"><span data-stu-id="08996-2627">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08996-2628">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08996-2628">Az.Compute</span></span>
* <span data-ttu-id="08996-2629">Problemet med ID-parameteruppsättningar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="08996-2629">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="08996-2630">Get-AzVMExtension har uppdaterats så att alla installerade tillägg visas om parametern Name inte har angetts</span><span class="sxs-lookup"><span data-stu-id="08996-2630">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="08996-2631">Parametrarna Tag och ResourceId har lagts till i cmdleten Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="08996-2631">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="08996-2632">Get-AzVmssVM utan instans-ID och med InstanceView kan visa virtuella VMSS-datorer med instansvyn.</span><span class="sxs-lookup"><span data-stu-id="08996-2632">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="08996-2633">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="08996-2633">Az.DataLakeStore</span></span>
* <span data-ttu-id="08996-2634">Cmdletar har lagts till för uppräkning och återställning av borttagna objekt i ADL</span><span class="sxs-lookup"><span data-stu-id="08996-2634">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="08996-2635">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="08996-2635">Az.EventHub</span></span>
* <span data-ttu-id="08996-2636">Ny boolesk egenskap SkipEmptyArchives har lagts till i Skip Empty Archives i CaptureDescription-klassen i Eventhub</span><span class="sxs-lookup"><span data-stu-id="08996-2636">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="08996-2637">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="08996-2637">Az.KeyVault</span></span>
* <span data-ttu-id="08996-2638">Taggning i Set-AzKeyVaultSecret har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="08996-2638">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="08996-2639">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="08996-2639">Az.LogicApp</span></span>
* <span data-ttu-id="08996-2640">Grundläggande SKU har lagts till för Integrationskonton</span><span class="sxs-lookup"><span data-stu-id="08996-2640">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="08996-2641">XSLT 2.0, XSLT 3.0 och Flytande mappningstyper har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-2641">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="08996-2642">Nya cmdletar för integrationskontosammansättningar</span><span class="sxs-lookup"><span data-stu-id="08996-2642">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="08996-2643">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="08996-2643">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="08996-2644">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="08996-2644">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="08996-2645">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="08996-2645">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="08996-2646">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="08996-2646">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="08996-2647">Nya cmdletar för batchkonfiguration för integrationskonto</span><span class="sxs-lookup"><span data-stu-id="08996-2647">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="08996-2648">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="08996-2648">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="08996-2649">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="08996-2649">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="08996-2650">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="08996-2650">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="08996-2651">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="08996-2651">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="08996-2652">Logic App-SDK har uppdaterats till version 4.1.0</span><span class="sxs-lookup"><span data-stu-id="08996-2652">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="08996-2653">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="08996-2653">Az.Monitor</span></span>
* <span data-ttu-id="08996-2654">Hjälpen för Get-AzMetric har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="08996-2654">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="08996-2655">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08996-2655">Az.Network</span></span>
* <span data-ttu-id="08996-2656">Hjälpexempel för Add-AzApplicationGatewayCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-2656">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="08996-2657">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="08996-2657">Az.OperationalInsights</span></span>
* <span data-ttu-id="08996-2658">Ytterligare stöd för datakällorna New och Get ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="08996-2658">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="08996-2659">Ny ApplicationInsights-typ har lagts till för att ge stöd för ”Get specific” och ”Get all” för ApplicationInsights-datakällor för angiven arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="08996-2659">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="08996-2660">Cmdleten New-AzOperationalInsightsApplicationInsightsDataSource har lagts till för att skapa datakälla med angivna parametrar för Application Insights-resurs: subscription Id, resourceGroupName och name.</span><span class="sxs-lookup"><span data-stu-id="08996-2660">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="08996-2661">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08996-2661">Az.Resources</span></span>
* <span data-ttu-id="08996-2662">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="08996-2662">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="08996-2663">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="08996-2663">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="08996-2664">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="08996-2664">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="08996-2665">Fel som gör att KeyCredentials inte kan skapas upprepade gånger har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="08996-2665">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="08996-2666">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08996-2666">Az.Sql</span></span>
* <span data-ttu-id="08996-2667">Lägg till stöd för hyperskalanivån för SQL DB</span><span class="sxs-lookup"><span data-stu-id="08996-2667">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="08996-2668">Ett fel har åtgärdats där återställningen kunde misslyckas på grund av onödiga inställningsegenskaper i restore-förfrågan</span><span class="sxs-lookup"><span data-stu-id="08996-2668">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="08996-2669">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="08996-2669">Az.Websites</span></span>
* <span data-ttu-id="08996-2670">Rätt exempel i Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="08996-2670">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="08996-2671">1.3.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="08996-2671">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="08996-2672">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="08996-2672">Az.Accounts</span></span>
* <span data-ttu-id="08996-2673">Uppdatera till den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="08996-2673">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="08996-2674">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="08996-2674">Az.AnalysisServices</span></span>
<span data-ttu-id="08996-2675">Allmän tillgänglighet för Az.AnalysisServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="08996-2675">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08996-2676">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08996-2676">Az.Compute</span></span>
* <span data-ttu-id="08996-2677">AEM-tillägg: Lägg till stöd för UltraSSD-, P60-, P70- och P80-diskar</span><span class="sxs-lookup"><span data-stu-id="08996-2677">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="08996-2678">Uppdatera hjälpbeskrivning för Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="08996-2678">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="08996-2679">Uppdatera hjälpbeskrivning och exempel för Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="08996-2679">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="08996-2680">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="08996-2680">Az.RecoveryServices</span></span>
<span data-ttu-id="08996-2681">Allmän tillgänglighet för Az.RecoveryServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="08996-2681">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="08996-2682">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08996-2682">Az.Resources</span></span>
* <span data-ttu-id="08996-2683">Korrigera taggar för resursgrupper</span><span class="sxs-lookup"><span data-stu-id="08996-2683">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="08996-2684">Mer information här: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="08996-2684">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="08996-2685">Åtgärda problem där `Get-AzureRmRoleAssignment` inte respekterar -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="08996-2685">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="08996-2686">Mer information här: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="08996-2686">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="08996-2687">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08996-2687">Az.Sql</span></span>
* <span data-ttu-id="08996-2688">Lägga till Get/Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="08996-2688">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="08996-2689">Åtgärda problem där ett nullref-undantag uppstår när du kör SQL-cmdletar och inte är inloggad på ett Azure-konto</span><span class="sxs-lookup"><span data-stu-id="08996-2689">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="08996-2690">Åtgärda nullref-undantag i Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="08996-2690">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="08996-2691">1.2.1 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="08996-2691">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="08996-2692">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="08996-2692">Az.Accounts</span></span>
* <span data-ttu-id="08996-2693">Version med rätt version av autentisering</span><span class="sxs-lookup"><span data-stu-id="08996-2693">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="08996-2694">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="08996-2694">Az.AnalysisServices</span></span>
* <span data-ttu-id="08996-2695">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="08996-2695">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="08996-2696">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="08996-2696">Az.RecoveryServices</span></span>
* <span data-ttu-id="08996-2697">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="08996-2697">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="08996-2698">1.2.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="08996-2698">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="08996-2699">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="08996-2699">Az.Accounts</span></span>
* <span data-ttu-id="08996-2700">Lägga till interaktiv autentisering och autentisering med användarnamn/lösenord för endast Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="08996-2700">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="08996-2701">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="08996-2701">Update incorrect online help URLs</span></span>
* <span data-ttu-id="08996-2702">Lägga till varningsmeddelande i PS Core för Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="08996-2702">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="08996-2703">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="08996-2703">Az.Aks</span></span>
* <span data-ttu-id="08996-2704">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="08996-2704">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="08996-2705">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="08996-2705">Az.Automation</span></span>
* <span data-ttu-id="08996-2706">Stöd för Python 2-runbookflöden har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-2706">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="08996-2707">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="08996-2707">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="08996-2708">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="08996-2708">Az.Cdn</span></span>
* <span data-ttu-id="08996-2709">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="08996-2709">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08996-2710">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08996-2710">Az.Compute</span></span>
* <span data-ttu-id="08996-2711">Lägga till cmdleten Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="08996-2711">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="08996-2712">Lägga till TempDisk-parameter i Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="08996-2712">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="08996-2713">Korrigera varningsmeddelande för New-AzVM</span><span class="sxs-lookup"><span data-stu-id="08996-2713">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="08996-2714">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="08996-2714">Az.ContainerRegistry</span></span>
* <span data-ttu-id="08996-2715">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="08996-2715">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="08996-2716">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="08996-2716">Az.DataFactory</span></span>
* <span data-ttu-id="08996-2717">ADF .Net SDK-versionen har uppdaterats till 3.0.0</span><span class="sxs-lookup"><span data-stu-id="08996-2717">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="08996-2718">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="08996-2718">Az.DataLakeStore</span></span>
* <span data-ttu-id="08996-2719">Åtgärda problem med ADLS-slutpunkt vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="08996-2719">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="08996-2720">Mer information här: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="08996-2720">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="08996-2721">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="08996-2721">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="08996-2722">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="08996-2722">Az.IotHub</span></span>
* <span data-ttu-id="08996-2723">Lägga till kodningsformat i cmdleten Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="08996-2723">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="08996-2724">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="08996-2724">Az.KeyVault</span></span>
* <span data-ttu-id="08996-2725">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="08996-2725">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="08996-2726">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08996-2726">Az.Network</span></span>
* <span data-ttu-id="08996-2727">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="08996-2727">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="08996-2728">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08996-2728">Az.Resources</span></span>
* <span data-ttu-id="08996-2729">Åtgärda felaktiga exempel i referensdokumentationen ”New-AzADAppCredential” och ”New-AzADSpCredential”</span><span class="sxs-lookup"><span data-stu-id="08996-2729">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="08996-2730">Åtgärda problem där sökvägen för parametern ”-TemplateFile” inte omvandlas innan cmdletarna för distribution i resursgruppen körs</span><span class="sxs-lookup"><span data-stu-id="08996-2730">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="08996-2731">Az.Resources: Korrigera dokumentationen om standardvärdet för New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="08996-2731">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="08996-2732">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="08996-2732">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="08996-2733">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="08996-2733">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="08996-2734">Åtgärda formateringsproblemet med objektet ”PSResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="08996-2734">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="08996-2735">Mer information här: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="08996-2735">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="08996-2736">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="08996-2736">Az.ServiceFabric</span></span>
* <span data-ttu-id="08996-2737">Återställ när ett certifikat läggs till i en Virtual Machine Scale Sets-modell men ett undantag genereras. Detta har gjorts för att åtgärda följande fel: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="08996-2737">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="08996-2738">Korrigera några felmeddelanden.</span><span class="sxs-lookup"><span data-stu-id="08996-2738">Fix some error messages.</span></span>
* <span data-ttu-id="08996-2739">Korrigering av skapande av kluster med ARM-mall som är standard för New-AzServiceFabriCluster som inte fungerade med migrering till Az.</span><span class="sxs-lookup"><span data-stu-id="08996-2739">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="08996-2740">Korrigering av tilläggning av kluster/programcertifikat så att endast VM Scale Sets som motsvarar klustret läggs till genom att kontrollera ID för klustret i tillägget.</span><span class="sxs-lookup"><span data-stu-id="08996-2740">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="08996-2741">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="08996-2741">Az.SignalR</span></span>
* <span data-ttu-id="08996-2742">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="08996-2742">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="08996-2743">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08996-2743">Az.Sql</span></span>
* <span data-ttu-id="08996-2744">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="08996-2744">Update incorrect online help URLs</span></span>
* <span data-ttu-id="08996-2745">Uppdaterad parameterbeskrivning för LicenseType-parameter med möjliga värden</span><span class="sxs-lookup"><span data-stu-id="08996-2745">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="08996-2746">Korrigering för att uppdatera hanterad instansidentitet som inte fungerar när det är den enda uppdaterade egenskapen</span><span class="sxs-lookup"><span data-stu-id="08996-2746">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="08996-2747">Stöd för anpassad sortering på hanterad instans</span><span class="sxs-lookup"><span data-stu-id="08996-2747">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="08996-2748">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="08996-2748">Az.Storage</span></span>
* <span data-ttu-id="08996-2749">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="08996-2749">Update incorrect online help URLs</span></span>
* <span data-ttu-id="08996-2750">Tillhandahåll detaljerat felmeddelande när en användare försöker hämta/konfigurera klassisk loggning/mått på ett Premium Storage-konto eftersom Premium Storage-kontot inte har stöd för klassisk loggning/mått.</span><span class="sxs-lookup"><span data-stu-id="08996-2750">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="08996-2751">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="08996-2751">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="08996-2752">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="08996-2752">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="08996-2753">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="08996-2753">Az.TrafficManager</span></span>
* <span data-ttu-id="08996-2754">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="08996-2754">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="08996-2755">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="08996-2755">Az.Websites</span></span>
* <span data-ttu-id="08996-2756">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="08996-2756">Update incorrect online help URLs</span></span>
* <span data-ttu-id="08996-2757">Korrigerar ”New-AzWebAppSSLBinding” så att certifikatet laddas upp till rätt resursgrupp och plats om appen finns i en ASE.</span><span class="sxs-lookup"><span data-stu-id="08996-2757">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="08996-2758">Korrigerar ”New-AzWebAppSSLBinding” så att taggarna inte skrivs över på en bindning av ett SSL-certifikat till en app</span><span class="sxs-lookup"><span data-stu-id="08996-2758">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="08996-2759">1.1.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="08996-2759">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="08996-2760">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="08996-2760">Az.Accounts</span></span>
* <span data-ttu-id="08996-2761">Lade till omfattningen ”Lokal” till Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="08996-2761">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08996-2762">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08996-2762">Az.Compute</span></span>
* <span data-ttu-id="08996-2763">Namn är nu valfritt i ID-parametern för Restart/Start/Stop/Remove/Set-AzVM och Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="08996-2763">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="08996-2764">Uppdaterade beskrivningen av ID i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="08996-2764">Updated the description of ID in help files</span></span>
* <span data-ttu-id="08996-2765">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="08996-2765">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="08996-2766">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="08996-2766">Az.DataLakeStore</span></span>
* <span data-ttu-id="08996-2767">Uppdatera sdk-versionen av dataplanet till 1.1.14 för SDK-korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="08996-2767">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="08996-2768">Korrigerade hanteringen av negativ accesstime och modificationtime för getfilestatus och liststatus; korrigera asynkront annulleringstoken</span><span class="sxs-lookup"><span data-stu-id="08996-2768">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="08996-2769">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="08996-2769">Az.EventGrid</span></span>
* <span data-ttu-id="08996-2770">Uppdaterat för användning av API-versionen 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="08996-2770">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="08996-2771">Uppdaterade följande cmdletar för att stödja nytt scenario i API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="08996-2771">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="08996-2772">New-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="08996-2772">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="08996-2773">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="08996-2773">Event Time-To-Live,</span></span>
        - <span data-ttu-id="08996-2774">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="08996-2774">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="08996-2775">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="08996-2775">Dead letter endpoint.</span></span>
    - <span data-ttu-id="08996-2776">Update-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="08996-2776">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="08996-2777">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="08996-2777">Event Time-To-Live,</span></span>
        - <span data-ttu-id="08996-2778">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="08996-2778">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="08996-2779">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="08996-2779">Dead letter endpoint.</span></span>
* <span data-ttu-id="08996-2780">Lade till nya enum-värden (storageQueue och hybridConnection) för alternativet EndpointType i cmdletarna New-AzureRmEventGridSubscription och Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="08996-2780">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="08996-2781">Visa varningsmeddelanden om skapande eller uppdatering av händelseprenumerationen förväntas medföra manuell åtgärd från användaren.</span><span class="sxs-lookup"><span data-stu-id="08996-2781">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="08996-2782">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="08996-2782">Az.IotHub</span></span>
* <span data-ttu-id="08996-2783">Har uppdaterats till den senaste versionen av SDK:n lotHub</span><span class="sxs-lookup"><span data-stu-id="08996-2783">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="08996-2784">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="08996-2784">Az.LogicApp</span></span>
* <span data-ttu-id="08996-2785">Get-AzLogicApp visar en lista över alla som inte har angivet namn</span><span class="sxs-lookup"><span data-stu-id="08996-2785">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="08996-2786">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08996-2786">Az.Resources</span></span>
* <span data-ttu-id="08996-2787">Åtgärdade problem med parameteruppsättningen när parametrarna -ODataQuery och -ResourceId anges för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="08996-2787">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="08996-2788">Mer information här: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="08996-2788">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="08996-2789">Åtgärdade hantering av parametern -Custom i New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="08996-2789">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="08996-2790">Korrigerade stavfel i New-AzDeployment-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="08996-2790">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="08996-2791">Gjorde parametern -MailNickname obligatorisk för New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="08996-2791">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="08996-2792">Mer information här: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="08996-2792">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="08996-2793">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="08996-2793">Az.SignalR</span></span>
* <span data-ttu-id="08996-2794">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="08996-2794">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="08996-2795">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08996-2795">Az.Sql</span></span>
* <span data-ttu-id="08996-2796">Konverterade lagringshanteringsklientens beroende av den normala SDK-implementeringen.</span><span class="sxs-lookup"><span data-stu-id="08996-2796">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="08996-2797">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="08996-2797">Az.Storage</span></span>
* <span data-ttu-id="08996-2798">Angav StorageAccountName för lagringskontext som det verkliga namnet på lagringskontot när det skapas med Sas Token, OAuth eller Anonymous</span><span class="sxs-lookup"><span data-stu-id="08996-2798">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="08996-2799">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="08996-2799">New-AzStorageContext</span></span>
* <span data-ttu-id="08996-2800">Skapade Sas Token för Blob Snapshot-objekt med parametern -FullUri, åtgärdade den returnerade URI:n så att den blir URI för ögonblicksbild</span><span class="sxs-lookup"><span data-stu-id="08996-2800">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="08996-2801">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="08996-2801">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="08996-2802">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="08996-2802">Az.Websites</span></span>
* <span data-ttu-id="08996-2803">Åtgärdade en bugg i datumparsningen i Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="08996-2803">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="08996-2804">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="08996-2804">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="08996-2805">1.0.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="08996-2805">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="08996-2806">Allmänt</span><span class="sxs-lookup"><span data-stu-id="08996-2806">General</span></span>

- <span data-ttu-id="08996-2807">Allmän tillgänglighet för Az-modulen</span><span class="sxs-lookup"><span data-stu-id="08996-2807">General Availability of Az Module</span></span>
- <span data-ttu-id="08996-2808">Onlinehjälp för varje modul</span><span class="sxs-lookup"><span data-stu-id="08996-2808">Online help for each module</span></span>
- <span data-ttu-id="08996-2809">Mer information och en översikt finns på [Az-informationssidan](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="08996-2809">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="08996-2810">Information om hur du migrerar från AzureRM finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="08996-2810">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="08996-2811">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="08996-2811">Az.Accounts</span></span>
- <span data-ttu-id="08996-2812">Har ändrats från Az.Profile</span><span class="sxs-lookup"><span data-stu-id="08996-2812">Changed from Az.Profile</span></span>
- <span data-ttu-id="08996-2813">Fasta tabellformat för profil- och kontexttyper</span><span class="sxs-lookup"><span data-stu-id="08996-2813">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="08996-2814">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="08996-2814">Az.ApiManagement</span></span>
- <span data-ttu-id="08996-2815">Korrigeringar för #7002</span><span class="sxs-lookup"><span data-stu-id="08996-2815">Fixes for #7002</span></span>
- <span data-ttu-id="08996-2816">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="08996-2816">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="08996-2817">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="08996-2817">Az.Batch</span></span>
- <span data-ttu-id="08996-2818">Lade till möjligheten att se vilken version av Azure Batch Node Agent som körs på var och en av de virtuella datorerna i en pool, via den nya egenskapen `NodeAgentInformation` på `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="08996-2818">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="08996-2819">Standarden `Caching` för `PSDataDisk` är nu `ReadWrite` i stället för `None`.</span><span class="sxs-lookup"><span data-stu-id="08996-2819">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="08996-2820">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="08996-2820">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="08996-2821">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="08996-2821">Az.Billing</span></span>
- <span data-ttu-id="08996-2822">Kombinerar cmdletarna för fakturering, förbrukning och UsageAggregates. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="08996-2822">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="08996-2823">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="08996-2823">Az.CognitivServices</span></span>
- <span data-ttu-id="08996-2824">Lade till kompletterare för SkuName och Typem som är tillgängliga i New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="08996-2824">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="08996-2825">Tog bort parameteruppsättningen GetSkusWithAccountParamSetName från Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="08996-2825">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="08996-2826">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="08996-2826">Az.ContainerInstance</span></span>
- <span data-ttu-id="08996-2827">Stöd för ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="08996-2827">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="08996-2828">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="08996-2828">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="08996-2829">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="08996-2829">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="08996-2830">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="08996-2830">Az.DataLakeStore</span></span>
- <span data-ttu-id="08996-2831">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="08996-2831">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="08996-2832">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="08996-2832">Az.Monitor</span></span>
- <span data-ttu-id="08996-2833">Döpte om Az.Insights till Az.Monitor och andra mindre icke-bakåtkompatibla ändringar. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="08996-2833">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="08996-2834">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="08996-2834">Az.KeyVault</span></span>
- <span data-ttu-id="08996-2835">Tog bort den inaktuella egenskapen PurgeDisabled från utdatatyper</span><span class="sxs-lookup"><span data-stu-id="08996-2835">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="08996-2836">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="08996-2836">Az.MachineLearning</span></span>
- <span data-ttu-id="08996-2837">Inkluderade cmdletarna från modulen Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="08996-2837">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="08996-2838">Az.Media</span><span class="sxs-lookup"><span data-stu-id="08996-2838">Az.Media</span></span>
- <span data-ttu-id="08996-2839">Tog bort inaktuella -Tags-alias från New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="08996-2839">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="08996-2840">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08996-2840">Az.Network</span></span>
<span data-ttu-id="08996-2841">Stöd har lagts till för konfiguration av RewriteRuleSets i Application Gateway</span><span class="sxs-lookup"><span data-stu-id="08996-2841">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="08996-2842">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="08996-2842">New cmdlets added:</span></span>
        - <span data-ttu-id="08996-2843">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="08996-2843">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="08996-2844">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="08996-2844">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="08996-2845">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="08996-2845">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="08996-2846">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="08996-2846">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="08996-2847">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="08996-2847">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="08996-2848">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="08996-2848">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="08996-2849">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="08996-2849">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="08996-2850">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="08996-2850">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="08996-2851">Cmdletar har uppdaterats med den valfria parametern -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="08996-2851">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="08996-2852">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="08996-2852">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="08996-2853">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="08996-2853">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="08996-2854">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="08996-2854">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="08996-2855">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="08996-2855">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="08996-2856">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="08996-2856">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="08996-2857">New-AzureRmApplicationGatewayUrlPathMapConfig har lagt till KeyVault-stöd för Application Gateway med Identity.</span><span class="sxs-lookup"><span data-stu-id="08996-2857">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="08996-2858">Cmdletar har uppdaterats med den valfria parametern -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="08996-2858">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="08996-2859">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="08996-2859">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="08996-2860">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="08996-2860">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="08996-2861">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="08996-2861">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="08996-2862">Cmdleten New-AzApplicationGateway har uppdaterats med den valfria parametern -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="08996-2862">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="08996-2863">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="08996-2863">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="08996-2864">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="08996-2864">Az.OperationalInsights</span></span>
- <span data-ttu-id="08996-2865">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="08996-2865">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="08996-2866">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="08996-2866">Az.Profile</span></span>
- <span data-ttu-id="08996-2867">Modulnamnet har ändrats till Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="08996-2867">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="08996-2868">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="08996-2868">Az.RecoveryServices</span></span>
- <span data-ttu-id="08996-2869">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="08996-2869">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="08996-2870">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08996-2870">Az.Resources</span></span>
- <span data-ttu-id="08996-2871">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="08996-2871">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="08996-2872">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="08996-2872">Az.ServiceFabric</span></span>
- <span data-ttu-id="08996-2873">Stöd för specificering av certifikat efter eget namn och tumavtryck</span><span class="sxs-lookup"><span data-stu-id="08996-2873">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="08996-2874">Information om fler icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="08996-2874">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="08996-2875">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="08996-2875">Az.SIgnalR</span></span>
- <span data-ttu-id="08996-2876">Allmän tillgänglighet för PowerShell-cmdletar för SIgnalR</span><span class="sxs-lookup"><span data-stu-id="08996-2876">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="08996-2877">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08996-2877">Az.Sql</span></span>
- <span data-ttu-id="08996-2878">Lade till de nya identifieringstyperna Data_Exfiltration och Unsafe_Action i Threat Detection-cmdletar</span><span class="sxs-lookup"><span data-stu-id="08996-2878">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="08996-2879">Uppdaterade dokumentationsexempel för Sql Auditing-cmdletar</span><span class="sxs-lookup"><span data-stu-id="08996-2879">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="08996-2880">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="08996-2880">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="08996-2881">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="08996-2881">Az.Storage</span></span>
- <span data-ttu-id="08996-2882">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="08996-2882">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="08996-2883">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="08996-2883">Az.Websites</span></span>
- <span data-ttu-id="08996-2884">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="08996-2884">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="08996-2885">0.7.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="08996-2885">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="08996-2886">Allmänt</span><span class="sxs-lookup"><span data-stu-id="08996-2886">General</span></span>

* <span data-ttu-id="08996-2887">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="08996-2887">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="08996-2888">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08996-2888">Az.Compute</span></span>

* <span data-ttu-id="08996-2889">Lade till stöd för UltraSSD och Galleriavbildningar i de enkla parameteruppsättningarna för `New-AzVm(ss)`-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="08996-2889">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="08996-2890">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="08996-2890">Az.DataLakeStore</span></span>

* <span data-ttu-id="08996-2891">Åtgärdade avslutande snedstreck i domänen för adls-konto</span><span class="sxs-lookup"><span data-stu-id="08996-2891">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="08996-2892">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="08996-2892">Az.FrontDoor</span></span>

* <span data-ttu-id="08996-2893">Brutna länkar korrigerades</span><span class="sxs-lookup"><span data-stu-id="08996-2893">Fixed some broken links</span></span>
    - <span data-ttu-id="08996-2894">I artiklarna New-AzureRmFrontDoor och Set-AzureRmFrontDoor artiklar korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="08996-2894">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="08996-2895">I artikeln New-AzureRmFrontDoorManagedRuleObject korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="08996-2895">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="08996-2896">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="08996-2896">Az.RecoveryServices</span></span>

* <span data-ttu-id="08996-2897">Lade till valideringar på klientsidan för Azure-filresurs med återställningsåtgärder.</span><span class="sxs-lookup"><span data-stu-id="08996-2897">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="08996-2898">Gjorde storageAccountName och storageAccountResourceGroupName valfritt för afs-återställning.</span><span class="sxs-lookup"><span data-stu-id="08996-2898">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="08996-2899">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08996-2899">Az.Resources</span></span>

* <span data-ttu-id="08996-2900">Korrigering för https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="08996-2900">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="08996-2901">Uppdaterade Get-AzureRmRoleAssignment så att prenumerationsomfattningen används om den anges vid begäran om klassiska administratörer.</span><span class="sxs-lookup"><span data-stu-id="08996-2901">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="08996-2902">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08996-2902">Az.Sql</span></span>

* <span data-ttu-id="08996-2903">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="08996-2903">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="08996-2904">Korrigerade ett problem med Get-AzureRmSqlDatabaseVulnerabilityAssessment med DotNet-kärna</span><span class="sxs-lookup"><span data-stu-id="08996-2904">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="08996-2905">Ändrade dokumentationen för hjälpmeddelanden som rör SQL Auditing-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="08996-2905">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="08996-2906">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="08996-2906">Az.Storage</span></span>

* <span data-ttu-id="08996-2907">Lade till -EnableHierarchicalNamespace i New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="08996-2907">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="08996-2908">Åtgärdade problemet med att cmdleten Copy File inte kunde återanvända källkontexten på målet om inte -DestContext angetts</span><span class="sxs-lookup"><span data-stu-id="08996-2908">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="08996-2909">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="08996-2909">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="08996-2910">Stöd för statisk webbplatskonfiguration</span><span class="sxs-lookup"><span data-stu-id="08996-2910">Support Static Website configuration</span></span>
    - <span data-ttu-id="08996-2911">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="08996-2911">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="08996-2912">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="08996-2912">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="08996-2913">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="08996-2913">Az.Websites</span></span>

* <span data-ttu-id="08996-2914">Set-AzureRmWebApp och Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="08996-2914">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="08996-2915">Ny parameter (-AzureStoragePath) har lagts till för att ange att Azure Storage-sökvägar ska monteras i containerappar i Windows och Linux.</span><span class="sxs-lookup"><span data-stu-id="08996-2915">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="08996-2916">Använder utdata från den nya cmdleten New-AzureRmWebAppAzureStoragePath som en parameter för att ange sökvägar för Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="08996-2916">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="08996-2917">0.6.1 – november 2018</span><span class="sxs-lookup"><span data-stu-id="08996-2917">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="08996-2918">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="08996-2918">Az.ApiManagement</span></span>
* <span data-ttu-id="08996-2919">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="08996-2919">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="08996-2920">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="08996-2920">Az.Automation</span></span>
* <span data-ttu-id="08996-2921">Swagger baserade Azure Automation-cmdletar</span><span class="sxs-lookup"><span data-stu-id="08996-2921">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="08996-2922">Cmdletar för Uppdateringshantering har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-2922">Added Update Management cmdlets</span></span>
* <span data-ttu-id="08996-2923">Cmdletar för källkontroll har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-2923">Added Source Control cmdlets</span></span>
* <span data-ttu-id="08996-2924">Remove-AzureRmAutomationHybridWorkerGroup-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-2924">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="08996-2925">Kommandot för DSC-registreringsnod har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="08996-2925">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="08996-2926">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08996-2926">Az.Compute</span></span>
* <span data-ttu-id="08996-2927">Problem med SystemAssigned-identitet har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="08996-2927">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="08996-2928">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="08996-2928">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="08996-2929">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="08996-2929">Az.ContainerInstance</span></span>
* <span data-ttu-id="08996-2930">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="08996-2930">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="08996-2931">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="08996-2931">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="08996-2932">uppdatera exempelbeskrivningen för marketplace-cmdletar</span><span class="sxs-lookup"><span data-stu-id="08996-2932">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="08996-2933">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08996-2933">Az.Network</span></span>
* <span data-ttu-id="08996-2934">Cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomErreller Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-2934">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="08996-2935">ICMP tillbaka till stöd för Azure Firewall-nätverksprotokoll har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-2935">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="08996-2936">Uppdatera cmdlet Test-AzureRmNetworkWatcherConnectivity, lägga till verifiering av mål-id, adress och port.</span><span class="sxs-lookup"><span data-stu-id="08996-2936">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="08996-2937">Åtgärda problem med minnesanvändning i VirtualNetwork-karta</span><span class="sxs-lookup"><span data-stu-id="08996-2937">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="08996-2938">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="08996-2938">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="08996-2939">Åtgärda för att ändra principen för en skyddad fildelning.</span><span class="sxs-lookup"><span data-stu-id="08996-2939">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="08996-2940">Tidszonsprincipen har konverterats till versaler.</span><span class="sxs-lookup"><span data-stu-id="08996-2940">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="08996-2941">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="08996-2941">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="08996-2942">Exempel i New-AzureRmRecoveryServicesAsrProtectableItem har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="08996-2942">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="08996-2943">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="08996-2943">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="08996-2944">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="08996-2944">Az.Relay</span></span>
* <span data-ttu-id="08996-2945">Valfri parameter -KeyValue till New-AzureRmRelayKey cmdlet har lagts till, vilket gör det möjligt för användare att tillhandahålla KeyValue.</span><span class="sxs-lookup"><span data-stu-id="08996-2945">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="08996-2946">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08996-2946">Az.Resources</span></span>
* <span data-ttu-id="08996-2947">Uppdatera hjälpdokumentation för resursidentitet kopplad till parametrar i `New-AzureRmPolicyAssignment` och `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="08996-2947">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="08996-2948">Lägg till ett exempel för New-AzureRmPolicyDefinition som använder -Metadata</span><span class="sxs-lookup"><span data-stu-id="08996-2948">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="08996-2949">Korrigera så att skiftläge behålls i taggnycklar i NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="08996-2949">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="08996-2950">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="08996-2950">Az.ServiceFabric</span></span>
* <span data-ttu-id="08996-2951">Lägg till utfasningsmeddelanden för kommande icke-kompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="08996-2951">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="08996-2952">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08996-2952">Az.Sql</span></span>
* <span data-ttu-id="08996-2953">Nya cmdletar för CRUD-åtgärder på Azure Sql Database-hanterad instans och Azure Sql-hanterad databas</span><span class="sxs-lookup"><span data-stu-id="08996-2953">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="08996-2954">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="08996-2954">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="08996-2955">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="08996-2955">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="08996-2956">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="08996-2956">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="08996-2957">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="08996-2957">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="08996-2958">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="08996-2958">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="08996-2959">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="08996-2959">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="08996-2960">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="08996-2960">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="08996-2961">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="08996-2961">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="08996-2962">Hantering av utökad granskningsprincip på en server eller en databas har aktiverats.</span><span class="sxs-lookup"><span data-stu-id="08996-2962">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="08996-2963">Ny parameter (PredicateExpression) har lagts till för att aktivera filtrering av granskningsloggar.</span><span class="sxs-lookup"><span data-stu-id="08996-2963">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="08996-2964">Cmdletar har ändrats så att de använder SQL-klienter i stället för äldre klienter.</span><span class="sxs-lookup"><span data-stu-id="08996-2964">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="08996-2965">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="08996-2965">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="08996-2966">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="08996-2966">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="08996-2967">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="08996-2967">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="08996-2968">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="08996-2968">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="08996-2969">Problem med att använda Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings med lagringskontots namnparameter har korrigerats</span><span class="sxs-lookup"><span data-stu-id="08996-2969">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="08996-2970">0.5.0 – november 2018</span><span class="sxs-lookup"><span data-stu-id="08996-2970">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="08996-2971">Allmänt</span><span class="sxs-lookup"><span data-stu-id="08996-2971">General</span></span>
* <span data-ttu-id="08996-2972">Lade till resurskompletterare till många kärn-cmdletar – dessa gör att du kan stega genom befintliga resursnamn med TABB vid interaktiva anrop till cmdletar</span><span class="sxs-lookup"><span data-stu-id="08996-2972">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="08996-2973">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="08996-2973">Az.Profile</span></span>
* <span data-ttu-id="08996-2974">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="08996-2974">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="08996-2975">Bytte namn på parametern TenantId i cmdleten Connect-AzAccount till Tenant och lade till ett alias för TenantId</span><span class="sxs-lookup"><span data-stu-id="08996-2975">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="08996-2976">Uppdaterade TenantId-beskrivningen för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="08996-2976">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="08996-2977">Åtgärda felmeddelande för misslyckad inloggning när du tillhandahåller klientdomän</span><span class="sxs-lookup"><span data-stu-id="08996-2977">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="08996-2978">Åtgärda problem med att kontextnamn hamnar i konflikt för konton utan prenumerationer i klientorganisationen</span><span class="sxs-lookup"><span data-stu-id="08996-2978">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="08996-2979">Åtgärda problem med DataLake-slutpunkter vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="08996-2979">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="08996-2980">Åtgärdade problem med att Disconnect-AzAccount kastades om den inte anslöts</span><span class="sxs-lookup"><span data-stu-id="08996-2980">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="08996-2981">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="08996-2981">Az.CognitiveServices</span></span>
* <span data-ttu-id="08996-2982">Lade till åtgärden Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="08996-2982">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08996-2983">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08996-2983">Az.Compute</span></span>
* <span data-ttu-id="08996-2984">Lade till cmdletarna Add-AzVmssVMDataDisk och Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="08996-2984">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="08996-2985">Get-AzVMImage visar AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="08996-2985">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="08996-2986">Åtgärdade att värdena för alternativen SetAzVMChefExtension -BootstrapOptions och -JsonAttribute inte angavs i json-format.</span><span class="sxs-lookup"><span data-stu-id="08996-2986">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="08996-2987">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="08996-2987">Az.DataLakeStore</span></span>
* <span data-ttu-id="08996-2988">Uppdatera DataLake-paketet till 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="08996-2988">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="08996-2989">Lägg till standardsamtidighet för flertrådade åtgärder.</span><span class="sxs-lookup"><span data-stu-id="08996-2989">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="08996-2990">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="08996-2990">Az.Insights</span></span>
* <span data-ttu-id="08996-2991">Åtgärdade problem #7267 (autoskalningsområde)</span><span class="sxs-lookup"><span data-stu-id="08996-2991">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="08996-2992">Problem med att uppräknade parametrar inte ställdes in ordentligt när du skapade en ny autoskalningsregel (de ställdes alltid in med standardvärdet).</span><span class="sxs-lookup"><span data-stu-id="08996-2992">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="08996-2993">Åtgärdade problem #7513 [Insights] Set-AzDiagnosticSetting kräver uttrycklig specifikation av kategorier när inställningar skapas</span><span class="sxs-lookup"><span data-stu-id="08996-2993">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="08996-2994">Nu kräver inte cmdleten uttrycklig anvisning av kategorierna för att aktiveras under skapande, d.v.s. den fungerar enligt beskrivning</span><span class="sxs-lookup"><span data-stu-id="08996-2994">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="08996-2995">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08996-2995">Az.Network</span></span>
* <span data-ttu-id="08996-2996">PeeringType ändrades till en obligatorisk parameter för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="08996-2996">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="08996-2997">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="08996-2997">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="08996-2998">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="08996-2998">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="08996-2999">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="08996-2999">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="08996-3000">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="08996-3000">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="08996-3001">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="08996-3001">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="08996-3002">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="08996-3002">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="08996-3003">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="08996-3003">Az.PolicyInsights</span></span>
* <span data-ttu-id="08996-3004">Cmdletar för principreparation har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-3004">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="08996-3005">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08996-3005">Az.Resources</span></span>
* <span data-ttu-id="08996-3006">Korrigering för https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="08996-3006">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="08996-3007">Tillåt att resurser listas med parametern -ResourceId för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="08996-3007">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="08996-3008">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="08996-3008">Az.ServiceBus</span></span>
* <span data-ttu-id="08996-3009">Skrivskyddad MigrationState-egenskap har lagts till i PSServiceBusMigrationConfigurationAttributes, som hjälper till att hålla koll på migreringstillståndet.</span><span class="sxs-lookup"><span data-stu-id="08996-3009">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="08996-3010">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="08996-3010">Az.ServiceFabric</span></span>
* <span data-ttu-id="08996-3011">Åtgärda att lägga till certifikat till Linux-Vmss.</span><span class="sxs-lookup"><span data-stu-id="08996-3011">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="08996-3012">Åtgärdade Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="08996-3012">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="08996-3013">Använd rätt tumavtryck från nya certifikat (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="08996-3013">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="08996-3014">Visa undantag korrekt (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="08996-3014">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="08996-3015">Åtgärdade Update-AzServiceFabricDurability så att klusterkonfigurationen uppdateras innan Vmss-åtgärden CreateOrUpdate påbörjas.</span><span class="sxs-lookup"><span data-stu-id="08996-3015">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="08996-3016">0.4.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="08996-3016">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="08996-3017">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="08996-3017">Az.Profile</span></span>
* <span data-ttu-id="08996-3018">Åtgärdade problemet med Get-AzSubscription i CloudShell</span><span class="sxs-lookup"><span data-stu-id="08996-3018">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="08996-3019">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="08996-3019">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08996-3020">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08996-3020">Az.Compute</span></span>
* <span data-ttu-id="08996-3021">Nya storlekar lades till i listan över godkända VM-storlekar för vilka accelererat nätverk kommer att aktiveras vid användning av den enkla parameteruppsättningen för New-AzVm</span><span class="sxs-lookup"><span data-stu-id="08996-3021">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="08996-3022">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="08996-3022">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="08996-3023">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="08996-3023">Az.DataLakeStore</span></span>
* <span data-ttu-id="08996-3024">Lägger till stöd för regler för virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="08996-3024">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="08996-3025">Get-AzDataLakeStoreVirtualNetworkRule: Hämtar eller listar regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="08996-3025">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="08996-3026">Add-AzDataLakeStoreVirtualNetworkRule: Lägger till en regel för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="08996-3026">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="08996-3027">Set-AzDataLakeStoreVirtualNetworkRule: Ändrar den angivna regeln för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="08996-3027">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="08996-3028">Remove-AzDataLakeStoreVirtualNetworkRule: Tar bort en regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="08996-3028">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="08996-3029">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08996-3029">Az.Network</span></span>
* <span data-ttu-id="08996-3030">Skicka protokollvärdet till serverdelen för att uppdatera cmdleten Test-AzNetworkWatcherConnectivity.</span><span class="sxs-lookup"><span data-stu-id="08996-3030">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="08996-3031">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="08996-3031">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="08996-3032">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08996-3032">Az.Resources</span></span>
* <span data-ttu-id="08996-3033">Åtgärdade problem där Get-AzRoleDefinition genererar ett oläsligt undantag (när standardprofilen inte innehåller någon prenumeration och ingen omfattning har angetts) genom att lägga till ett beskrivande undantag i scenariot.</span><span class="sxs-lookup"><span data-stu-id="08996-3033">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="08996-3034">Ställ in ”RoleDefinitionNameParameterSet” som standardparameteruppsättning.</span><span class="sxs-lookup"><span data-stu-id="08996-3034">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="08996-3035">0.3.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="08996-3035">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="08996-3036">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="08996-3036">Azure.Storage</span></span>
* <span data-ttu-id="08996-3037">Åtgärda fel där Kopiera blob/fil inte kopierar metadata när målplatsen har ett problem med metadata</span><span class="sxs-lookup"><span data-stu-id="08996-3037">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="08996-3038">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="08996-3038">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="08996-3039">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="08996-3039">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="08996-3040">Stöd för att hämta användningsinformation om en Storage-resurs för en specifik plats och för att lägga till ett varningsmeddelande för att hämta användningsinformation om en global Storage-resurs är inaktuellt.</span><span class="sxs-lookup"><span data-stu-id="08996-3040">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="08996-3041">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="08996-3041">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="08996-3042">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="08996-3042">Az.CognitiveServices</span></span>
* <span data-ttu-id="08996-3043">Stöd för Get-AzCognitiveServicesAccountSkus utan ett befintligt konto.</span><span class="sxs-lookup"><span data-stu-id="08996-3043">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08996-3044">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08996-3044">Az.Compute</span></span>
* <span data-ttu-id="08996-3045">Åtgärdade fel där Get-AzVM -ResourceGroupName <rg> returnerar fler än 50 resultat om det behövs</span><span class="sxs-lookup"><span data-stu-id="08996-3045">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="08996-3046">Lade till ett exempel för SimpleParameterSet i hjälpen för cmdleten New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="08996-3046">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="08996-3047">Ett stavfel i förloppsmeddelandet för Azure Disk Encryption har korrigerats</span><span class="sxs-lookup"><span data-stu-id="08996-3047">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="08996-3048">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="08996-3048">Az.DataFactoryV2</span></span>
* <span data-ttu-id="08996-3049">ADF .Net SDK-versionen har uppdaterats till 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="08996-3049">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="08996-3050">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08996-3050">Az.Network</span></span>
* <span data-ttu-id="08996-3051">Funktionalitet för NetworkProfile har lagts till.</span><span class="sxs-lookup"><span data-stu-id="08996-3051">Added NetworkProfile functionality.</span></span> <span data-ttu-id="08996-3052">nya cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-3052">new cmdlets added</span></span>
    - <span data-ttu-id="08996-3053">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="08996-3053">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="08996-3054">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="08996-3054">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="08996-3055">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="08996-3055">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="08996-3056">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="08996-3056">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="08996-3057">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="08996-3057">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="08996-3058">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="08996-3058">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="08996-3059">Länk för tjänstassociering på modell för undernät har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-3059">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="08996-3060">Cmdletarna New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap och Remove-AzVirtualNetworkTap har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-3060">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="08996-3061">Cmdletarna Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig och Remove-AzNEtworkInterfaceTapConfig har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-3061">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="08996-3062">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="08996-3062">Az.RedisCache</span></span>
* <span data-ttu-id="08996-3063">Tillåt att alla strängar används som storleksparametrar framöver.</span><span class="sxs-lookup"><span data-stu-id="08996-3063">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="08996-3064">Lägg till P5 i popup-fönstret PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="08996-3064">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="08996-3065">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08996-3065">Az.Resources</span></span>
* <span data-ttu-id="08996-3066">Parametern -Mode som saknades i Set-AzPolicyDefinition har lagts till</span><span class="sxs-lookup"><span data-stu-id="08996-3066">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="08996-3067">Åtgärdade buggen för cmdleten Get-AzProviderOperation för åtgärder med ursprung som innehåller användare</span><span class="sxs-lookup"><span data-stu-id="08996-3067">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="08996-3068">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08996-3068">Az.Sql</span></span>
* <span data-ttu-id="08996-3069">Ett problem där vissa cmdletar för säkerhetskopiering inte kunde identifiera den aktuella azure-prenumerationen har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="08996-3069">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="08996-3070">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="08996-3070">Az.Websites</span></span>
* <span data-ttu-id="08996-3071">Ny cmdlet: Get-AzWebAppContainerContinuousDeploymentUrl – Hämtar webhook-URL:en för kontinuerlig distribution av container</span><span class="sxs-lookup"><span data-stu-id="08996-3071">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="08996-3072">Nya cmdletar: New-AzWebAppContainerPSSession och Enter-WebAppContainerPSSession – Startar en PowerShell-fjärrsession i en containerapp för windows</span><span class="sxs-lookup"><span data-stu-id="08996-3072">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="08996-3073">0.2.0 – september 2018</span><span class="sxs-lookup"><span data-stu-id="08996-3073">0.2.0 - September 2018</span></span>
 <span data-ttu-id="08996-3074">Första versionen</span><span class="sxs-lookup"><span data-stu-id="08996-3074">Initial Release</span></span>