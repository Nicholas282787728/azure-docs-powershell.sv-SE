---
title: Viktig information om Azure PowerShell
description: Lär dig mer om alla de senaste uppdateringarna för Azure PowerShell-modulerna.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/09/2020
ms.openlocfilehash: 694439934afb41b465a89188d59bc964db3c0032
ms.sourcegitcommit: 9181f20c2c5eaa271150de9e25b9cb30ba5e6cb0
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/04/2020
ms.locfileid: "77002681"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="95fa9-103">Viktig information om Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="95fa9-103">Azure PowerShell release notes</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="95fa9-104">3.4.0 – februari 2020</span><span class="sxs-lookup"><span data-stu-id="95fa9-104">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="95fa9-105">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="95fa9-105">Highlights since the last major release</span></span>
* <span data-ttu-id="95fa9-106">Första Az.CosmosDB-versionen 0.1.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="95fa9-106">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="95fa9-107">Stöd för Az.Network ConnectionMonitor V2 har lagts till</span><span class="sxs-lookup"><span data-stu-id="95fa9-107">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="95fa9-108">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="95fa9-108">Az.Accounts</span></span>
* <span data-ttu-id="95fa9-109">Inaktivera automatisk sparande av kontext när AzureRmContext.json inte är tillgängligt</span><span class="sxs-lookup"><span data-stu-id="95fa9-109">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="95fa9-110">Uppdatera referensen till Azure Powershell Common till 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="95fa9-110">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="95fa9-111">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="95fa9-111">Az.ApiManagement</span></span>
* <span data-ttu-id="95fa9-112">**Get-AzApiManagementApiSchema** Hämtning av Open-Api-schema som är associerat med ett API har åtgärdats   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="95fa9-112">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="95fa9-113">**New-AzApiManagementProduct**\* och **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="95fa9-113">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="95fa9-114">Åtgärda dokumentation för https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="95fa9-114">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="95fa9-115">**Set-AzApiManagementApi** Exempel för att visa hur ServiceUrl uppdateras med hjälp av cmdleten har lagts till</span><span class="sxs-lookup"><span data-stu-id="95fa9-115">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="95fa9-116">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="95fa9-116">Az.Compute</span></span>
* <span data-ttu-id="95fa9-117">Begränsa antalet VM-status till 100 för att undvika begränsning när Get-AzVM -Status utförs utan VM-namn.</span><span class="sxs-lookup"><span data-stu-id="95fa9-117">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="95fa9-118">Lägg till cmdleten Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="95fa9-118">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="95fa9-119">Lägg till parametrarna EncryptionType och DiskEncryptionSetId i följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="95fa9-119">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="95fa9-120">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="95fa9-120">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="95fa9-121">Lägg till parametern ColocationStatus för cmdleten Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="95fa9-121">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="95fa9-122">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="95fa9-122">Az.DataFactory</span></span>
* <span data-ttu-id="95fa9-123">Uppdatera ADF .Net SDK-versionen till 4.7.0</span><span class="sxs-lookup"><span data-stu-id="95fa9-123">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="95fa9-124">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="95fa9-124">Az.DeploymentManager</span></span>
* <span data-ttu-id="95fa9-125">Lägger till LIST-åtgärder för resurser</span><span class="sxs-lookup"><span data-stu-id="95fa9-125">Adds LIST operations for resources</span></span>
* <span data-ttu-id="95fa9-126">Lägger till funktion för att utföra åtgärder för hälsokontrollsteg</span><span class="sxs-lookup"><span data-stu-id="95fa9-126">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="95fa9-127">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="95fa9-127">Az.HDInsight</span></span>
* <span data-ttu-id="95fa9-128">Åtgärda dokumentfel för New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="95fa9-128">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="95fa9-129">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="95fa9-129">Az.KeyVault</span></span>
* <span data-ttu-id="95fa9-130">Lägg till Name-alias för attributet VaultName så att Remove-AzureKeyVault stämmer överens med New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="95fa9-130">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="95fa9-131">Az.Network</span><span class="sxs-lookup"><span data-stu-id="95fa9-131">Az.Network</span></span>
* <span data-ttu-id="95fa9-132">Nytt exempel har lagts till i Set-AzNetworkWatcherConfigFlowLog.md för att demonstrera ett inaktiveringsscenario för Trafikanalys.</span><span class="sxs-lookup"><span data-stu-id="95fa9-132">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="95fa9-133">Lägg till stöd för att tilldela konfiguration av hanterings-IP till Azure Firewall – ett dedikerat undernät och en offentlig IP som brandväggen använder för dess hanteringstrafik</span><span class="sxs-lookup"><span data-stu-id="95fa9-133">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="95fa9-134">Cmdleten New-AzFirewall har uppdaterats:</span><span class="sxs-lookup"><span data-stu-id="95fa9-134">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="95fa9-135">Parametern -ManagementPublicIpAddress (inte obligatorisk) som accepterar ett offentligt IP-adressobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="95fa9-135">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="95fa9-136">Metoden SetManagementIpConfiguration har lagts till för brandväggsobjekt – kräver ett undernät och en offentlig IP-adress som indata – undernätets namn måste vara ”AzureFirewallManagementSubnet”</span><span class="sxs-lookup"><span data-stu-id="95fa9-136">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="95fa9-137">Exempel för Get-AzNetworkSecurityGroup har korrigerats så att exempel visas för NSG:er i stället för nätverksgränssnitt.</span><span class="sxs-lookup"><span data-stu-id="95fa9-137">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="95fa9-138">Ett skrivfel har åtgärdats i kommandot New-AzVpnSite som hindrade kompletteraren för resurs-ID från att fylla i en parameter.</span><span class="sxs-lookup"><span data-stu-id="95fa9-138">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="95fa9-139">Stöd för Url-konfiguration i åtgärdsuppsättningen för omskrivningsregler i Application Gateway har lagts till</span><span class="sxs-lookup"><span data-stu-id="95fa9-139">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="95fa9-140">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="95fa9-140">New cmdlets added:</span></span>
        - <span data-ttu-id="95fa9-141">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="95fa9-141">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="95fa9-142">Cmdletar har uppdaterats med den valfria parametern -UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="95fa9-142">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="95fa9-143">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="95fa9-143">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="95fa9-144">Lägg till stöd för resurser för NetworkWatcher ConnectionMonitor version 2</span><span class="sxs-lookup"><span data-stu-id="95fa9-144">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="95fa9-145">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="95fa9-145">Az.PolicyInsights</span></span>
* <span data-ttu-id="95fa9-146">Stöd för utvärdering av efterlevnad innan fastställande av vilken resurs som ska åtgärdas</span><span class="sxs-lookup"><span data-stu-id="95fa9-146">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="95fa9-147">Lägg till parametern ”-ResourceDiscoverMode” för Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="95fa9-147">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="95fa9-148">Lägg till cmdleten Get-AzPolicyMetadata för att hämta resurser för principmetadata</span><span class="sxs-lookup"><span data-stu-id="95fa9-148">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="95fa9-149">Get-AzPolicyState och Get-AzPolicyStateSummary för API-versionen 2019-10-01 har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="95fa9-149">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="95fa9-150">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="95fa9-150">Az.RecoveryServices</span></span>
* <span data-ttu-id="95fa9-151">Azure Site Recovery-stöd för att ta bort en replikerad disk.</span><span class="sxs-lookup"><span data-stu-id="95fa9-151">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="95fa9-152">Tillagt Azure Backup-stöd för att lägga till taggar när ett Recovery Services-valv skapas.</span><span class="sxs-lookup"><span data-stu-id="95fa9-152">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="95fa9-153">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="95fa9-153">Az.Resources</span></span>
* <span data-ttu-id="95fa9-154">Gör -Scope valfritt i cmdletarna \*-AzPolicyAssignment med standardinställning till kontextprenumeration</span><span class="sxs-lookup"><span data-stu-id="95fa9-154">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="95fa9-155">Lägg till exempel på att skapa ADServicePrincipal med lösenord och nyckelautentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="95fa9-155">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="95fa9-156">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="95fa9-156">Az.Sql</span></span>
<span data-ttu-id="95fa9-157">Åtgärda cmdleten New-AzSqlDatabaseSecondary så att existensen PartnerDatabaseName kontrolleras i stället för existensen DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="95fa9-157">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="95fa9-158">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="95fa9-158">Az.Storage</span></span>
* <span data-ttu-id="95fa9-159">Stöd för angivning av krypteringsnyckeltyp för Tabell/kö i Skapa lagringskonto</span><span class="sxs-lookup"><span data-stu-id="95fa9-159">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="95fa9-160">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="95fa9-160">New-AzStorageAccount</span></span>
* <span data-ttu-id="95fa9-161">Visa RequestId när StorageException inte har ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="95fa9-161">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="95fa9-162">Åtgärda exempel 6 för cmdleten Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="95fa9-162">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="95fa9-163">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="95fa9-163">Az.Websites</span></span>
* <span data-ttu-id="95fa9-164">Set-AzWebapp och Set-AzWebappSlot stöder egenskaperna AlwaysOn, MinTls och FtpsState</span><span class="sxs-lookup"><span data-stu-id="95fa9-164">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="95fa9-165">Åtgärdar problemet där inställning av HttpsOnly samtidigt som AppservicePlan ändrades med det enskilda kommandot Set-AzWebApp återställde HttpsOnly till standardvärdet</span><span class="sxs-lookup"><span data-stu-id="95fa9-165">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="95fa9-166">3.3.0 – januari 2020</span><span class="sxs-lookup"><span data-stu-id="95fa9-166">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="95fa9-167">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="95fa9-167">Az.Accounts</span></span>
* <span data-ttu-id="95fa9-168">Nu stöder Add-AzEnvironment och Set-AzEnvironment parametrarna AzureAttestationServiceEndpointResourceId och AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="95fa9-168">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="95fa9-169">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="95fa9-169">Az.Cdn</span></span>
* <span data-ttu-id="95fa9-170">Information om felsvar visas i New-AzCdnEndpoint-cmdleten</span><span class="sxs-lookup"><span data-stu-id="95fa9-170">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="95fa9-171">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="95fa9-171">Az.Compute</span></span>
* <span data-ttu-id="95fa9-172">Set-AzVMCustomScriptExtension-cmdleten har åtgärdats för en virtuell dator med hanterad OD-disk som inte har någon operativsystemprofil.</span><span class="sxs-lookup"><span data-stu-id="95fa9-172">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="95fa9-173">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="95fa9-173">Az.ContainerInstance</span></span>
* <span data-ttu-id="95fa9-174">Parameternamn som används med New-AzContainerGroup-exempel har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="95fa9-174">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="95fa9-175">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="95fa9-175">Az.DataBoxEdge</span></span>
* <span data-ttu-id="95fa9-176">Cmdleten ”Get-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="95fa9-176">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="95fa9-177">Hämta gränslagringscontainern</span><span class="sxs-lookup"><span data-stu-id="95fa9-177">Get the Edge Storage Container</span></span>
* <span data-ttu-id="95fa9-178">Cmdleten ”New-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="95fa9-178">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="95fa9-179">Skapa en ny gränslagringscontainer</span><span class="sxs-lookup"><span data-stu-id="95fa9-179">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="95fa9-180">Cmdleten ”Remove-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="95fa9-180">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="95fa9-181">Ta bort gränslagringscontainern</span><span class="sxs-lookup"><span data-stu-id="95fa9-181">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="95fa9-182">Cmdleten ”Invoke-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="95fa9-182">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="95fa9-183">Anropa åtgärd för att uppdatera data i gränslagringscontainer</span><span class="sxs-lookup"><span data-stu-id="95fa9-183">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="95fa9-184">Cmdleten ”Get-AzDataBoxEdgeStorageAccount” har lagts till</span><span class="sxs-lookup"><span data-stu-id="95fa9-184">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="95fa9-185">Hämta gränslagringskontot</span><span class="sxs-lookup"><span data-stu-id="95fa9-185">Get the Edge Storage Account</span></span>
* <span data-ttu-id="95fa9-186">Cmdleten ”New-AzDataBoxEdgeStorageAccount” har lagts till</span><span class="sxs-lookup"><span data-stu-id="95fa9-186">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="95fa9-187">Skapa ett nytt gränslagringskonto</span><span class="sxs-lookup"><span data-stu-id="95fa9-187">Create new Edge Storage Account</span></span>
* <span data-ttu-id="95fa9-188">Cmdleten ”Remove-AzDataBoxEdgeStorageAccount” har lagts till</span><span class="sxs-lookup"><span data-stu-id="95fa9-188">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="95fa9-189">Ta bort gränslagringskontot</span><span class="sxs-lookup"><span data-stu-id="95fa9-189">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="95fa9-190">Anropa cmdleten ”Invoke-AzDataBoxEdgeShare”</span><span class="sxs-lookup"><span data-stu-id="95fa9-190">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="95fa9-191">Anropa åtgärd för att uppdatera resursdata</span><span class="sxs-lookup"><span data-stu-id="95fa9-191">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="95fa9-192">Cmdleten ”Set-AzDataBoxEdgeStorageAccountCredential” har lagts till</span><span class="sxs-lookup"><span data-stu-id="95fa9-192">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="95fa9-193">Ange autentiseringsuppgifter för az databoxedge-lagringskonto</span><span class="sxs-lookup"><span data-stu-id="95fa9-193">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="95fa9-194">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="95fa9-194">Az.DataFactory</span></span>
* <span data-ttu-id="95fa9-195">Lägg till AutoUpdateETA-, LatestVersion-, PushedVersion-, TaskQueueId- och VersionStatus-egenskaper för Get-AzDataFactoryV2IntegrationRuntime-cmd</span><span class="sxs-lookup"><span data-stu-id="95fa9-195">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="95fa9-196">Uppdatera ADF .Net SDK-versionen till 4.6.0</span><span class="sxs-lookup"><span data-stu-id="95fa9-196">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="95fa9-197">Lägg till parametern ”PublicIPs” för ”Set-AzureRmDataFactoryV2IntegrationRuntime”-cmd så att Azure-SSIS IR kan skapas med statiska offentliga IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="95fa9-197">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="95fa9-198">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="95fa9-198">Az.DevTestLabs</span></span>
* <span data-ttu-id="95fa9-199">Ta bort den brutna länken i Get-AzDtlAllowedVMSizesPolicy.md</span><span class="sxs-lookup"><span data-stu-id="95fa9-199">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="95fa9-200">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="95fa9-200">Az.EventHub</span></span>
* <span data-ttu-id="95fa9-201">Korrigering av problem 10634: Åtgärda referensen till null-objekt för eventhubnamespace-borttagning</span><span class="sxs-lookup"><span data-stu-id="95fa9-201">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="95fa9-202">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="95fa9-202">Az.HDInsight</span></span>
* <span data-ttu-id="95fa9-203">Åtgärda Invoke-AzHDInsightHiveJob.md-fel.</span><span class="sxs-lookup"><span data-stu-id="95fa9-203">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="95fa9-204">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="95fa9-204">Az.MachineLearning</span></span>
* <span data-ttu-id="95fa9-205">Nedanstående cmdletar har tagits bort eftersom MachineLearningCompute inte längre är tillgängligt</span><span class="sxs-lookup"><span data-stu-id="95fa9-205">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="95fa9-206">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="95fa9-206">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="95fa9-207">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="95fa9-207">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="95fa9-208">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="95fa9-208">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="95fa9-209">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="95fa9-209">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="95fa9-210">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="95fa9-210">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="95fa9-211">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="95fa9-211">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="95fa9-212">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="95fa9-212">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="95fa9-213">Az.Network</span><span class="sxs-lookup"><span data-stu-id="95fa9-213">Az.Network</span></span>
* <span data-ttu-id="95fa9-214">Uppgradera beroende av Microsoft.Azure.Management.Sql från 1.36-preview till 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="95fa9-214">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="95fa9-215">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="95fa9-215">Az.RecoveryServices</span></span>
* <span data-ttu-id="95fa9-216">Ändrat Azure Site Recovery-stöd för krypterade vilande data på virtuella datorer med hanterade diskar med kundhanterade nycklar för Azure till Azure-providern.</span><span class="sxs-lookup"><span data-stu-id="95fa9-216">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="95fa9-217">Azure Site Recovery-stöd för att ange ID för diskkrypteringsuppsättning som valfri inmatning för aktivering av skydd för VMware till Azure.</span><span class="sxs-lookup"><span data-stu-id="95fa9-217">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="95fa9-218">Azure Site Recovery-stöd för att ange ID för diskkrypteringsuppsättning som valfri inmatning på disknivå för aktivering av skydd för VMware till Azure.</span><span class="sxs-lookup"><span data-stu-id="95fa9-218">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="95fa9-219">Azure Site Recovery-stöd för att uppdatera replikeringsskyddade objekt med mappning för diskkrypteringsuppsättning för HyperV till Azure.</span><span class="sxs-lookup"><span data-stu-id="95fa9-219">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="95fa9-220">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="95fa9-220">Az.Resources</span></span>
* <span data-ttu-id="95fa9-221">Åtgärda ett fel i hjälpdokument för ”Remove-AzTag”.</span><span class="sxs-lookup"><span data-stu-id="95fa9-221">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="95fa9-222">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="95fa9-222">Az.Sql</span></span>
* <span data-ttu-id="95fa9-223">Åtgärda funktioner i cmdletar för att ange baslinjen för sårbarhetsbedömning för arbete med huvuddatabasen för Azure-databasen och begränsa den för systemdatabaser på hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="95fa9-223">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="95fa9-224">Åtgärda ett fel när en redundansgrupp för en SQL-instans skapas</span><span class="sxs-lookup"><span data-stu-id="95fa9-224">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="95fa9-225">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="95fa9-225">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="95fa9-226">Lägg till DR som en ny giltig licenstyp</span><span class="sxs-lookup"><span data-stu-id="95fa9-226">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="95fa9-227">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="95fa9-227">Az.Storage</span></span>
* <span data-ttu-id="95fa9-228">Lägg till varningsmeddelande om icke-bakåtkompatibel ändring för DefaultAction-värdeändring i en framtida version</span><span class="sxs-lookup"><span data-stu-id="95fa9-228">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="95fa9-229">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="95fa9-229">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="95fa9-230">Stöd för att hämta lagringskontots senaste synkroniseringstid genom att köra get-AzureRMStorageAccount med parametern -IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="95fa9-230">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span> 
    - <span data-ttu-id="95fa9-231">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="95fa9-231">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="95fa9-232">3.2.0 – December 2019</span><span class="sxs-lookup"><span data-stu-id="95fa9-232">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="95fa9-233">Allmänt</span><span class="sxs-lookup"><span data-stu-id="95fa9-233">General</span></span>
* <span data-ttu-id="95fa9-234">Uppdatera referenser i .psd1 för att använda relativa sökvägar för alla moduler</span><span class="sxs-lookup"><span data-stu-id="95fa9-234">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="95fa9-235">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="95fa9-235">Az.Accounts</span></span>
* <span data-ttu-id="95fa9-236">Ange rätt UserAgent för telemetri på klientsidan för Az 4.0 preview</span><span class="sxs-lookup"><span data-stu-id="95fa9-236">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="95fa9-237">Visa användarvänligt felmeddelande när kontexten är null i Az 4.0 preview</span><span class="sxs-lookup"><span data-stu-id="95fa9-237">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="95fa9-238">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="95fa9-238">Az.Batch</span></span>
* <span data-ttu-id="95fa9-239">Korrigera problem [#10602](https://github.com/Azure/azure-powershell/issues/10602), där **New-AzBatchPool** skickade VirtualMachineConfiguration.ContainerConfiguration eller VirtualMachineConfiguration.DataDisks på ett felaktigt sätt till servern.</span><span class="sxs-lookup"><span data-stu-id="95fa9-239">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="95fa9-240">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="95fa9-240">Az.DataFactory</span></span>
* <span data-ttu-id="95fa9-241">Uppdatera ADF .Net SDK-versionen till 4.5.0</span><span class="sxs-lookup"><span data-stu-id="95fa9-241">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="95fa9-242">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="95fa9-242">Az.FrontDoor</span></span>
* <span data-ttu-id="95fa9-243">Stöd har lagts till för undantag för hanterade regler för brandväggen för webbaserade program</span><span class="sxs-lookup"><span data-stu-id="95fa9-243">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="95fa9-244">Lägg till SocketAddr för automatisk komplettering</span><span class="sxs-lookup"><span data-stu-id="95fa9-244">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="95fa9-245">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="95fa9-245">Az.HealthcareApis</span></span>
* <span data-ttu-id="95fa9-246">Undantagshantering</span><span class="sxs-lookup"><span data-stu-id="95fa9-246">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="95fa9-247">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="95fa9-247">Az.KeyVault</span></span>
* <span data-ttu-id="95fa9-248">Åtgärdat fel vid åtkomst av värde som kanske inte har angetts</span><span class="sxs-lookup"><span data-stu-id="95fa9-248">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="95fa9-249">Hantering av ECC-certifikat (Elliptic Curve Cryptography)</span><span class="sxs-lookup"><span data-stu-id="95fa9-249">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="95fa9-250">Stöd har lagts till för att ange kurvan för certifikatprinciper</span><span class="sxs-lookup"><span data-stu-id="95fa9-250">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="95fa9-251">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="95fa9-251">Az.Monitor</span></span>
* <span data-ttu-id="95fa9-252">Lägger till valfritt argument i kommandot Lägg till diagnostikinställningar.</span><span class="sxs-lookup"><span data-stu-id="95fa9-252">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="95fa9-253">Ett växelargument som om det finns visar att exporten till Log Analytics måste ske till ett fast schema (kallas även</span><span class="sxs-lookup"><span data-stu-id="95fa9-253">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="95fa9-254">dedikerad, datatyp)</span><span class="sxs-lookup"><span data-stu-id="95fa9-254">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="95fa9-255">Az.Network</span><span class="sxs-lookup"><span data-stu-id="95fa9-255">Az.Network</span></span>
* <span data-ttu-id="95fa9-256">Stöd för IpGroups i program-, NAT- och nätverksregler för Azure Firewall.</span><span class="sxs-lookup"><span data-stu-id="95fa9-256">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="95fa9-257">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="95fa9-257">Az.Resources</span></span>
* <span data-ttu-id="95fa9-258">Åtgärda ett problem där malldistributionen inte kan läsa en mallparameter om dess namn står i konflikt med ett inbyggt parameternamn.</span><span class="sxs-lookup"><span data-stu-id="95fa9-258">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="95fa9-259">Uppdaterade princip-cmdletar för att använda den nya API-versionen 2019-09-01 som introducerar grupperingsstöd inom principuppsättningsdefinitioner.</span><span class="sxs-lookup"><span data-stu-id="95fa9-259">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="95fa9-260">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="95fa9-260">Az.Sql</span></span>
* <span data-ttu-id="95fa9-261">Uppgraderad funktion för att skapa lagring i automatisk aktivering av sårbarhetsbedömning till StorageV2</span><span class="sxs-lookup"><span data-stu-id="95fa9-261">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="95fa9-262">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="95fa9-262">Az.Storage</span></span>
* <span data-ttu-id="95fa9-263">Stöd för generering av blob/container-identitetsbaserad SAS-token med lagringskontextbaserad på OAuth-autentisering</span><span class="sxs-lookup"><span data-stu-id="95fa9-263">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="95fa9-264">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="95fa9-264">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="95fa9-265">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="95fa9-265">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="95fa9-266">Stöd för återkallning av användardelegeringsnycklar för lagringskonto för att återkalla alla SAS-token</span><span class="sxs-lookup"><span data-stu-id="95fa9-266">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="95fa9-267">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="95fa9-267">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="95fa9-268">Uppgradera till Microsoft.Azure.Management.Storage 14.2.0 för att stödja den nya API-versionen 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="95fa9-268">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="95fa9-269">Stöd för QuotaGiB (resurskvot i Gibibye) för värden över 5120 i hanteringsplanet för cmdletar för filresurser och parameteraliaset. Quota har också lagts till för parametern ”QuotaGiB”.</span><span class="sxs-lookup"><span data-stu-id="95fa9-269">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span> 
    - <span data-ttu-id="95fa9-270">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="95fa9-270">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="95fa9-271">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="95fa9-271">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="95fa9-272">Lägg till parameteraliaset QuotaGiB i parametern Quota</span><span class="sxs-lookup"><span data-stu-id="95fa9-272">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="95fa9-273">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="95fa9-273">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="95fa9-274">Åtgärda problemet att Set-AzStorageContainerAcl kan rensa den lagrade åtkomstprincipen</span><span class="sxs-lookup"><span data-stu-id="95fa9-274">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="95fa9-275">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="95fa9-275">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="95fa9-276">3.1.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="95fa9-276">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="95fa9-277">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="95fa9-277">Highlights since the last major release</span></span>
* <span data-ttu-id="95fa9-278">Az.DataBoxEdge 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="95fa9-278">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="95fa9-279">Az.SqlVirtualMachine 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="95fa9-279">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="95fa9-280">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="95fa9-280">Az.Compute</span></span>
* <span data-ttu-id="95fa9-281">Funktion för att använda en virtuell dator igen</span><span class="sxs-lookup"><span data-stu-id="95fa9-281">VM Reapply feature</span></span>
    - <span data-ttu-id="95fa9-282">Lägg till parameter för att använda igen till cmdleten Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="95fa9-282">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="95fa9-283">Funktionen AutomaticRepairs i VM-skalningsuppsättningar:</span><span class="sxs-lookup"><span data-stu-id="95fa9-283">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="95fa9-284">Lägg till parametrarna EnableAutomaticRepair, AutomaticRepairGracePeriod och AutomaticRepairMaxInstanceRepairsPercent till följande cmdletar:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="95fa9-284">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="95fa9-285">Stöd för galleriavbildningar i flera klientorganisationer för New-AzVM</span><span class="sxs-lookup"><span data-stu-id="95fa9-285">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="95fa9-286">Lägg till "Spot" till argumentslutföraren i prioritetsparametern i cmdletarna New-AzVM, New-AzVMConfig och New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="95fa9-286">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="95fa9-287">Lägg till parametrarna DiskIOPSReadWrite och DiskMBpsReadWrite till cmdleten Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="95fa9-287">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="95fa9-288">Ändra parametern SourceImageId för cmdleten New-AzGalleryImageVersion till valfri</span><span class="sxs-lookup"><span data-stu-id="95fa9-288">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="95fa9-289">Lägg till parametrarna OSDiskImage och DataDiskImage till cmdleten New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="95fa9-289">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="95fa9-290">Lägg till parametern HyperVGeneration till cmdleten New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="95fa9-290">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="95fa9-291">Lägg till parametern SkipExtensionsOnOverprovisionedVMs till cmdletarna New-AzVmss, New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="95fa9-291">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="95fa9-292">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="95fa9-292">Az.DataBoxEdge</span></span>
* <span data-ttu-id="95fa9-293">Cmdleten `Get-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="95fa9-293">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="95fa9-294">Hämta ordning</span><span class="sxs-lookup"><span data-stu-id="95fa9-294">Get the Order</span></span>
* <span data-ttu-id="95fa9-295">Cmdleten `New-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="95fa9-295">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="95fa9-296">Skapa ny ordning</span><span class="sxs-lookup"><span data-stu-id="95fa9-296">Create new Order</span></span>
* <span data-ttu-id="95fa9-297">Cmdleten `Remove-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="95fa9-297">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="95fa9-298">Ta bort ordning</span><span class="sxs-lookup"><span data-stu-id="95fa9-298">Remove the Order</span></span>
* <span data-ttu-id="95fa9-299">Cmdleten `New-AzDataBoxEdgeShare` har ändrats</span><span class="sxs-lookup"><span data-stu-id="95fa9-299">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="95fa9-300">Nu skapas lokal filresurs</span><span class="sxs-lookup"><span data-stu-id="95fa9-300">Now creates Local Share</span></span>
* <span data-ttu-id="95fa9-301">Cmdleten `Set-AzDataBoxEdgeRole` har lagts till</span><span class="sxs-lookup"><span data-stu-id="95fa9-301">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="95fa9-302">Nu kan IotRole mappas till filresursen</span><span class="sxs-lookup"><span data-stu-id="95fa9-302">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="95fa9-303">Cmdleten `Invoke-AzDataBoxEdgeDevice` har lagts till</span><span class="sxs-lookup"><span data-stu-id="95fa9-303">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="95fa9-304">Anropa genomsökningsuppdatering, ladda ned uppdatering, installera uppdateringar på enheten</span><span class="sxs-lookup"><span data-stu-id="95fa9-304">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="95fa9-305">Cmdleten `Get-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="95fa9-305">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="95fa9-306">Hämtar information om utlösare</span><span class="sxs-lookup"><span data-stu-id="95fa9-306">Gets the information about Triggers</span></span>
* <span data-ttu-id="95fa9-307">Cmdleten `New-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="95fa9-307">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="95fa9-308">Skapa nya utlösare</span><span class="sxs-lookup"><span data-stu-id="95fa9-308">Create new Triggers</span></span>
* <span data-ttu-id="95fa9-309">Cmdleten `Remove-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="95fa9-309">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="95fa9-310">Ta bort utlösare</span><span class="sxs-lookup"><span data-stu-id="95fa9-310">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="95fa9-311">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="95fa9-311">Az.DataFactory</span></span>
* <span data-ttu-id="95fa9-312">Uppdatera ADF .Net SDK-versionen till 4.4.0</span><span class="sxs-lookup"><span data-stu-id="95fa9-312">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="95fa9-313">Lägg till parametern ExpressCustomSetup för kommandot Set-AzureRmDataFactoryV2IntegrationRuntime för att aktivera installationskonfigurationer och komponenter från tredje part utan anpassat konfigurationsskript.</span><span class="sxs-lookup"><span data-stu-id="95fa9-313">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="95fa9-314">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="95fa9-314">Az.DataLakeStore</span></span>
* <span data-ttu-id="95fa9-315">Uppdatera dokumentation för Get-AzDataLakeStoreDeletedItem och Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="95fa9-315">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="95fa9-316">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="95fa9-316">Az.EventHub</span></span>
* <span data-ttu-id="95fa9-317">Korrigering av problem #10301: Korrigera datumformat för SAS-token</span><span class="sxs-lookup"><span data-stu-id="95fa9-317">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="95fa9-318">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="95fa9-318">Az.FrontDoor</span></span>
* <span data-ttu-id="95fa9-319">Lägg till parametern MinimumTlsVersion till Enable-AzFrontDoorCustomDomainHttps och New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="95fa9-319">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="95fa9-320">Lägg till parametrarna HealthProbeMethod och EnabledState till New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="95fa9-320">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="95fa9-321">Lägg till en ny cmdlet för att skapa BackendPoolsSettings-objekt som passar i skapande/uppdatering av Front Door</span><span class="sxs-lookup"><span data-stu-id="95fa9-321">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="95fa9-322">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="95fa9-322">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="95fa9-323">Az.Network</span><span class="sxs-lookup"><span data-stu-id="95fa9-323">Az.Network</span></span>
* <span data-ttu-id="95fa9-324">Ändra alternativexemplen Start-AzVirtualNetworkGatewayConnectionPacketCapture.md och Start-AzVirtualnetworkGatewayPacketCapture.md för FilterData.</span><span class="sxs-lookup"><span data-stu-id="95fa9-324">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="95fa9-325">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="95fa9-325">Az.PrivateDns</span></span>
* <span data-ttu-id="95fa9-326">Uppdaterade PrivateDns .NET SDK till version 1.0.0</span><span class="sxs-lookup"><span data-stu-id="95fa9-326">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="95fa9-327">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="95fa9-327">Az.RecoveryServices</span></span>
* <span data-ttu-id="95fa9-328">Stöd för att välja disktyp vid aktivering av skydd i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="95fa9-328">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="95fa9-329">Korrigering av bugg för åtgärdsredigering av återställningsplan i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="95fa9-329">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="95fa9-330">Återställningsstöd för att godkänna filestream-databaser i Azure Backup SQL.</span><span class="sxs-lookup"><span data-stu-id="95fa9-330">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="95fa9-331">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="95fa9-331">Az.RedisCache</span></span>
* <span data-ttu-id="95fa9-332">Parametern MinimumTlsVersion har lagts till i cmdletarna New-AzRedisCache och Set-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="95fa9-332">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="95fa9-333">Dessutom har MinimumTlsVersion lagts till i utdata för cmdleten Get-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="95fa9-333">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="95fa9-334">Verifiering har lagts till på parametern -Size i cmdletarna Set-AzRedisCache och New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="95fa9-334">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="95fa9-335">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="95fa9-335">Az.Resources</span></span>
- <span data-ttu-id="95fa9-336">Uppdaterade policy-cmdletar för att använda den nya API-versionen 2019-06-01 som har en ny EnforcementMode-egenskap i policytilldelningen.</span><span class="sxs-lookup"><span data-stu-id="95fa9-336">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="95fa9-337">Uppdaterade hjälpexempel för skapandet av policydefinition</span><span class="sxs-lookup"><span data-stu-id="95fa9-337">Updated create policy definition help example</span></span>
- <span data-ttu-id="95fa9-338">Åtgärda bugg i Remove-AZADServicePrincipal -ServicePrincipalName, utlös null-referens när tjänstens huvudnamn inte hittas.</span><span class="sxs-lookup"><span data-stu-id="95fa9-338">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="95fa9-339">Åtgärda bugg i New-AZADServicePrincipal, utlös null-referens när klientorganisationen inte har någon prenumeration.</span><span class="sxs-lookup"><span data-stu-id="95fa9-339">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="95fa9-340">Ändra New-AzAdServicePrincipal för att endast lägga till autentiseringsuppgifter för det associerade programmet.</span><span class="sxs-lookup"><span data-stu-id="95fa9-340">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="95fa9-341">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="95fa9-341">Az.Sql</span></span>
* <span data-ttu-id="95fa9-342">Stöd har lagts till för databasen ReadReplicaCount.</span><span class="sxs-lookup"><span data-stu-id="95fa9-342">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="95fa9-343">Korrigerade Set-AzSqlDatabase när zonredundans inte har angetts</span><span class="sxs-lookup"><span data-stu-id="95fa9-343">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="95fa9-344">3.0.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="95fa9-344">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="95fa9-345">Allmänt</span><span class="sxs-lookup"><span data-stu-id="95fa9-345">General</span></span>
* <span data-ttu-id="95fa9-346">Az. PrivateDns 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="95fa9-346">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="95fa9-347">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="95fa9-347">Az.Accounts</span></span>
* <span data-ttu-id="95fa9-348">Lägg till ett utfasningsmeddelande för aliaset Resolve-error.</span><span class="sxs-lookup"><span data-stu-id="95fa9-348">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="95fa9-349">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="95fa9-349">Az.Advisor</span></span>
* <span data-ttu-id="95fa9-350">Den nya kategorin Operational Excellence har lagts till i cmdleten Get-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="95fa9-350">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="95fa9-351">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="95fa9-351">Az.Batch</span></span>
* <span data-ttu-id="95fa9-352">`CoreQuota` på `BatchAccountContext` har bytt namn till `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="95fa9-352">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="95fa9-353">Det finns även en ny `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="95fa9-353">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="95fa9-354">Detta påverkar **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="95fa9-354">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="95fa9-355">**New-AzBatchTask** `-ResourceFile`-parametern tar nu en samling `PSResourceFile`-objekt som kan skapas med hjälp av den nya cmdleten **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="95fa9-355">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="95fa9-356">Ny **New-AzBatchResourceFile**-cmdlet för att skapa `PSResourceFile`-objekt.</span><span class="sxs-lookup"><span data-stu-id="95fa9-356">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="95fa9-357">Dessa kan tillhandahållas till **New-AzBatchTask** på `-ResourceFile`-parametern.</span><span class="sxs-lookup"><span data-stu-id="95fa9-357">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="95fa9-358">Detta stöder två nya typer av resursfiler förutom det befintliga sättet med `HttpUrl`:</span><span class="sxs-lookup"><span data-stu-id="95fa9-358">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="95fa9-359">`AutoStorageContainerName`-baserade resursfiler laddar ned en hel container för automatisk lagring till Batch-noden.</span><span class="sxs-lookup"><span data-stu-id="95fa9-359">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="95fa9-360">`StorageContainerUrl`-baserade resursfiler laddar ned containern som anges i webbadressen till Batch-noden.</span><span class="sxs-lookup"><span data-stu-id="95fa9-360">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="95fa9-361">Tog bort egenskapen `ApplicationPackages` för `PSApplication` som returnerades av **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="95fa9-361">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="95fa9-362">Specifika paket i ett program kan nu hämtas med hjälp av **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="95fa9-362">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="95fa9-363">Till exempel: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="95fa9-363">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="95fa9-364">Bytt namn på `ApplicationId` till `ApplicationName` på **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** och **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="95fa9-364">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="95fa9-365">`ApplicationId` är nu ett alias för `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="95fa9-365">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="95fa9-366">Ny `PSWindowsUserConfiguration`-egenskap till `PSUserAccount` lades till.</span><span class="sxs-lookup"><span data-stu-id="95fa9-366">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="95fa9-367">Bytte namn på `Version` till `Name` på `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="95fa9-367">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="95fa9-368">Bytte namn på `BlobSource` till `HttpUrl` på `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="95fa9-368">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="95fa9-369">Tog bort egenskapen `OSDisk` från `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="95fa9-369">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="95fa9-370">Tog bort **Set-AzBatchPoolOSVersion**.</span><span class="sxs-lookup"><span data-stu-id="95fa9-370">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="95fa9-371">Den här åtgärden stöds inte längre.</span><span class="sxs-lookup"><span data-stu-id="95fa9-371">This operation is no longer supported.</span></span>
* <span data-ttu-id="95fa9-372">`TargetOSVersion` har tagits bort från `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="95fa9-372">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="95fa9-373">Bytte namn på `CurrentOSVersion` till `OSVersion` på `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="95fa9-373">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="95fa9-374">`DataEgressGiB` och `DataIngressGiB` har tagits bort från `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="95fa9-374">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="95fa9-375">Tog bort **Get-AzBatchNodeAgentSku** och ersatte det med **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="95fa9-375">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span> 
  - <span data-ttu-id="95fa9-376">**Get-AzBatchSupportedImage** returnerar samma data som **Get-AzBatchNodeAgentSku** men i ett mer användarvänligt format.</span><span class="sxs-lookup"><span data-stu-id="95fa9-376">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="95fa9-377">Nya icke-verifierade avbildningar returneras nu också.</span><span class="sxs-lookup"><span data-stu-id="95fa9-377">New non-verified images are also now returned.</span></span> <span data-ttu-id="95fa9-378">Ytterligare information om `Capabilities` och `BatchSupportEndOfLife` för varje avbildning inkluderas också.</span><span class="sxs-lookup"><span data-stu-id="95fa9-378">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="95fa9-379">Lade till möjlighet att montera fjärrfilsystem på varje nod i en pool via den nya parametern `MountConfiguration` för **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="95fa9-379">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="95fa9-380">Har nu stöd för nätverkssäkerhetsregler som blockerar nätverksåtkomst till en pool baserat på källportens trafik.</span><span class="sxs-lookup"><span data-stu-id="95fa9-380">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="95fa9-381">Detta görs via egenskapen `SourcePortRanges` på `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="95fa9-381">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="95fa9-382">När du kör en container stöder nu Batch körningen av uppgiften i arbetskatalogen för containern eller i arbetskatalogen för Batch-uppgiften.</span><span class="sxs-lookup"><span data-stu-id="95fa9-382">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="95fa9-383">Detta styrs av egenskapen `WorkingDirectory` på `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="95fa9-383">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="95fa9-384">Lade till en funktion för att ange en samling av offentliga IP-adresser på `PSNetworkConfiguration` via den nya egenskapen `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="95fa9-384">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="95fa9-385">Detta garanterar att noderna i poolen har en IP-adress från listan över IP-adresser som tillhandahållits av användare.</span><span class="sxs-lookup"><span data-stu-id="95fa9-385">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="95fa9-386">Om inget värde anges är standardvärdet för `WaitForSuccess` på `PSSTartTask` nu `$True` (var tidigare `$False`).</span><span class="sxs-lookup"><span data-stu-id="95fa9-386">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="95fa9-387">Om inget värde anges är standardvärdet för `Scope` på `PSAutoUserSpecification` nu `Pool` (var tidigare `Task` på Windows och `Pool` på Linux).</span><span class="sxs-lookup"><span data-stu-id="95fa9-387">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="95fa9-388">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="95fa9-388">Az.Cdn</span></span>
* <span data-ttu-id="95fa9-389">Introducerade UrlRewriteAction och CacheKeyQueryStringAction till RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="95fa9-389">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="95fa9-390">Åtgärdade flera buggar, som saknade indata för ”väljare” i cmdleten New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="95fa9-390">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="95fa9-391">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="95fa9-391">Az.Compute</span></span>
* <span data-ttu-id="95fa9-392">Funktion för diskkrypteringsuppsättning</span><span class="sxs-lookup"><span data-stu-id="95fa9-392">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="95fa9-393">Nya cmdletar:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="95fa9-393">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="95fa9-394">Parametern DiskEncryptionSetId har lagts till i följande cmdletar: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="95fa9-394">DiskEncryptionSetId parameter is added to the following cmdlets: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span></span>        
        <span data-ttu-id="95fa9-395">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="95fa9-395">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="95fa9-396">Parametrarna DiskEncryptionSetId och EncryptionType har lagts till i följande cmdletar:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="95fa9-396">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="95fa9-397">Lägg till parametern PublicIPAddressVersion i New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="95fa9-397">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="95fa9-398">Flytta FileUris för anpassat skripttillägg från offentlig inställning till skyddad inställning</span><span class="sxs-lookup"><span data-stu-id="95fa9-398">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="95fa9-399">Lägg till ScaleInPolicy i cmdletarna New-AzVmss, New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="95fa9-399">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="95fa9-400">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="95fa9-400">Breaking changes</span></span>
    - <span data-ttu-id="95fa9-401">Parametern UploadSizeInBytes används istället för DiskSizeGB för New-AzDiskConfig när CreateOption är Uppladdning</span><span class="sxs-lookup"><span data-stu-id="95fa9-401">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="95fa9-402">PublishingProfile.Source.ManagedImage.Id ersätts med StorageProfile.Source.Id i objektet GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="95fa9-402">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="95fa9-403">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="95fa9-403">Az.DataFactory</span></span>
* <span data-ttu-id="95fa9-404">Uppdatera ADF .Net SDK-versionen till 4.3.0</span><span class="sxs-lookup"><span data-stu-id="95fa9-404">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="95fa9-405">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="95fa9-405">Az.DataLakeStore</span></span>
* <span data-ttu-id="95fa9-406">Uppdatera ADLS SDK-version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) innehåller följande korrigeringar</span><span class="sxs-lookup"><span data-stu-id="95fa9-406">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="95fa9-407">Undvik att utlösa undantag när det inte går att deserialisera creationtime för inmatning av papperskorg eller katalog.</span><span class="sxs-lookup"><span data-stu-id="95fa9-407">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="95fa9-408">Gör inställning tillgänglig per tidsgräns för förfrågan i adlsclient</span><span class="sxs-lookup"><span data-stu-id="95fa9-408">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="95fa9-409">Korrigera överföringen av ursprunglig syncflag för badoffset-återställning</span><span class="sxs-lookup"><span data-stu-id="95fa9-409">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="95fa9-410">Korrigera EnumerateDirectory för att hämta fortsättningstoken när svar har kontrollerats</span><span class="sxs-lookup"><span data-stu-id="95fa9-410">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="95fa9-411">Korrigera bugg i Concat</span><span class="sxs-lookup"><span data-stu-id="95fa9-411">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="95fa9-412">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="95fa9-412">Az.FrontDoor</span></span>
* <span data-ttu-id="95fa9-413">Åtgärdade diverse stavfel i modul</span><span class="sxs-lookup"><span data-stu-id="95fa9-413">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="95fa9-414">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="95fa9-414">Az.HDInsight</span></span>
* <span data-ttu-id="95fa9-415">Korrigerade buggen att kunder får felet ”inte en giltig Base-64-sträng” vid användning av Get-AzHDInsightCluster för att hämta klustret med ADLSGen1-lagring.</span><span class="sxs-lookup"><span data-stu-id="95fa9-415">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="95fa9-416">Lägg till en parameter med namnet ”ApplicationId” i de tre cmdletarna Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig och New-AzHDInsightCluster så att kunden kan tillhandahålla tjänstens huvudnamn för program-ID för åtkomst till Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="95fa9-416">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="95fa9-417">Ändrade Microsoft.Azure.Management.HDInsight från 2.1.0 till 5.1.0</span><span class="sxs-lookup"><span data-stu-id="95fa9-417">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="95fa9-418">Fem cmdletar har tagits bort:</span><span class="sxs-lookup"><span data-stu-id="95fa9-418">Removed five cmdlets:</span></span>
    - <span data-ttu-id="95fa9-419">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="95fa9-419">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="95fa9-420">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="95fa9-420">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="95fa9-421">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="95fa9-421">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="95fa9-422">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="95fa9-422">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="95fa9-423">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="95fa9-423">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="95fa9-424">Tre cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="95fa9-424">Added three cmdlets:</span></span>
    - <span data-ttu-id="95fa9-425">Get-AzHDInsightMonitoring som ersätter Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="95fa9-425">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="95fa9-426">Enable-AzHDInsightMonitoring som ersätter Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="95fa9-426">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="95fa9-427">Disable-AzHDInsightMonitoring som ersätter Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="95fa9-427">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="95fa9-428">Korrigerade cmdleten Get-AzHDInsightProperties för att stödja hämtning av funktionsinformation från en viss plats.</span><span class="sxs-lookup"><span data-stu-id="95fa9-428">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="95fa9-429">Parameteruppsättningarna (Spark1 och Spark2) har tagits bort från Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="95fa9-429">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="95fa9-430">Lägg till exempel för cmdleten Add-AzHDInsightSecurityProfile till hjälpdokumenten.</span><span class="sxs-lookup"><span data-stu-id="95fa9-430">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="95fa9-431">Ändrade utdatatyp för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="95fa9-431">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="95fa9-432">Ändrade utdatatyp för Get-AzHDInsightProperties från CapabilitiesResponse till AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="95fa9-432">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="95fa9-433">Ändrade utdatatyp för Remove-AzHDInsightCluster från ClusterGetResponse till bool.</span><span class="sxs-lookup"><span data-stu-id="95fa9-433">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="95fa9-434">Ändrade utdatatyp för Set-AzHDInsightGatewaySettings HttpConnectivitySettings till GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="95fa9-434">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="95fa9-435">Lade till testfall för vissa scenarier.</span><span class="sxs-lookup"><span data-stu-id="95fa9-435">Added some scenario test cases.</span></span>
* <span data-ttu-id="95fa9-436">Ta bort vissa alias: Add-AzHDInsightConfigValues, Get-AzHDInsightProperties.</span><span class="sxs-lookup"><span data-stu-id="95fa9-436">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="95fa9-437">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="95fa9-437">Az.IotHub</span></span>
* <span data-ttu-id="95fa9-438">Icke-bakåtkompatibla ändringar:</span><span class="sxs-lookup"><span data-stu-id="95fa9-438">Breaking changes:</span></span>
    - <span data-ttu-id="95fa9-439">Cmdleten Add-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="95fa9-439">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="95fa9-440">Parameteruppsättningen __AllParameterSets för cmdleten Add-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="95fa9-440">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="95fa9-441">Cmdleten Get-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="95fa9-441">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="95fa9-442">Parameteruppsättningen __AllParameterSets för cmdleten Get-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="95fa9-442">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="95fa9-443">Egenskapen OperationsMonitoringProperties av typen Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="95fa9-443">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="95fa9-444">Egenskapen OperationsMonitoringProperties av typen Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="95fa9-444">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="95fa9-445">Cmdleten New-AzIotHubExportDevice stöder inte längre aliaset New-AzIotHubExportDevices.</span><span class="sxs-lookup"><span data-stu-id="95fa9-445">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="95fa9-446">Cmdleten New-AzIotHubImportDevice stöder inte längre aliaset New-AzIotHubImportDevices.</span><span class="sxs-lookup"><span data-stu-id="95fa9-446">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="95fa9-447">Cmdleten Remove-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="95fa9-447">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="95fa9-448">Parameteruppsättningen __AllParameterSets för cmdleten Remove-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="95fa9-448">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="95fa9-449">Cmdleten Set-AzIotHub har inte längre stöd för parametern OperationsMonitoringProperties och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="95fa9-449">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="95fa9-450">Parameteruppsättningen UpdateOperationsMonitoringProperties för cmdleten Set-AzIotHub har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="95fa9-450">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="95fa9-451">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="95fa9-451">Az.RecoveryServices</span></span>
* <span data-ttu-id="95fa9-452">Azure Site Recovery-stöd för att konfigurera nätverksresurser som NSG, offentliga IP-adresser och interna lastbalanserare för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="95fa9-452">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="95fa9-453">Azure Site Recovery-stöd för att skriva till hanterad disk för vMWare till Azure.</span><span class="sxs-lookup"><span data-stu-id="95fa9-453">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="95fa9-454">Azure Site Recovery-stöd för NIC-reduktion för vMWare till Azure.</span><span class="sxs-lookup"><span data-stu-id="95fa9-454">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="95fa9-455">Azure Site Recovery-stöd för accelererat nätverk för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="95fa9-455">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="95fa9-456">Azure Site Recovery-stöd för automatisk uppdatering av agent för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="95fa9-456">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="95fa9-457">Azure Site Recovery-stöd för Standard SSD för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="95fa9-457">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="95fa9-458">Azure Site Recovery-stöd för tvåstegskryptering i Azure Disk Encryption för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="95fa9-458">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="95fa9-459">Azure Site Recovery-stöd för att skydda nyligen tillagda diskar för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="95fa9-459">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="95fa9-460">En funktion för mjuk borttagning av virtuella datorer samt tester för mjuk borttagning har tagits bort</span><span class="sxs-lookup"><span data-stu-id="95fa9-460">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="95fa9-461">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="95fa9-461">Az.Resources</span></span>
* <span data-ttu-id="95fa9-462">Uppdatera beroendesammansättning för Microsoft.Extensions.Caching.Memory från 1.1.1 till 2.2</span><span class="sxs-lookup"><span data-stu-id="95fa9-462">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="95fa9-463">Az.Network</span><span class="sxs-lookup"><span data-stu-id="95fa9-463">Az.Network</span></span>
* <span data-ttu-id="95fa9-464">Ändra alla cmdletar för PrivateEndpointConnection så att de stöder generiska tjänstleverantörer.</span><span class="sxs-lookup"><span data-stu-id="95fa9-464">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="95fa9-465">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="95fa9-465">Updated cmdlet:</span></span>
        - <span data-ttu-id="95fa9-466">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="95fa9-466">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="95fa9-467">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="95fa9-467">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="95fa9-468">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="95fa9-468">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="95fa9-469">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="95fa9-469">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="95fa9-470">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="95fa9-470">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="95fa9-471">Lägg till ny cmdlet för PrivateLinkResource så att det också stöder generiska tjänstleverantörer.</span><span class="sxs-lookup"><span data-stu-id="95fa9-471">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="95fa9-472">Ny cmdlet:</span><span class="sxs-lookup"><span data-stu-id="95fa9-472">New cmdlet:</span></span>
        - <span data-ttu-id="95fa9-473">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="95fa9-473">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="95fa9-474">Lägg till nya fält och parametrar för funktionen Proxy Protocol V2.</span><span class="sxs-lookup"><span data-stu-id="95fa9-474">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="95fa9-475">Lägg till egenskapen EnableProxyProtocol i PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="95fa9-475">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="95fa9-476">Lägg till egenskapen LinkIdentifier i PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="95fa9-476">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="95fa9-477">Uppdaterade New-AzPrivateLinkService för att lägga till den nya valfria parametern EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="95fa9-477">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="95fa9-478">Korrigera felaktig beskrivning av parameter i referensdokumentationen för New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="95fa9-478">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="95fa9-479">Nya cmdletar som stöder Azure-brandväggsprincipen</span><span class="sxs-lookup"><span data-stu-id="95fa9-479">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="95fa9-480">Lägg till stöd för den underordnade resursen RouteTables för VirtualHub</span><span class="sxs-lookup"><span data-stu-id="95fa9-480">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="95fa9-481">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="95fa9-481">New cmdlets added:</span></span>
        - <span data-ttu-id="95fa9-482">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="95fa9-482">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="95fa9-483">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="95fa9-483">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="95fa9-484">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="95fa9-484">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="95fa9-485">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="95fa9-485">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="95fa9-486">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="95fa9-486">Set-AzVirtualHub</span></span>
* <span data-ttu-id="95fa9-487">Lägg till stöd för ny egenskaps-SKU för VirtualHub och VirtualWANType för VirtualWan</span><span class="sxs-lookup"><span data-stu-id="95fa9-487">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="95fa9-488">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="95fa9-488">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="95fa9-489">New-AzVirtualHub: lade till parameter-SKU</span><span class="sxs-lookup"><span data-stu-id="95fa9-489">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="95fa9-490">Update-AzVirtualHub: lade till parameter-SKU</span><span class="sxs-lookup"><span data-stu-id="95fa9-490">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="95fa9-491">New-AzVirtualWan: lade till parametern VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="95fa9-491">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="95fa9-492">Update-AzVirtualWan: lade till parametern VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="95fa9-492">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="95fa9-493">Lägg till stöd för egenskapen EnableInternetSecurity för HubVnetConnection, VpnConnection och ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="95fa9-493">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="95fa9-494">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="95fa9-494">New cmdlets added:</span></span>
        - <span data-ttu-id="95fa9-495">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="95fa9-495">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="95fa9-496">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="95fa9-496">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="95fa9-497">New-AzureRmVirtualHubVnetConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="95fa9-497">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="95fa9-498">New-AzureRmVpnConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="95fa9-498">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="95fa9-499">Update-AzureRmVpnConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="95fa9-499">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="95fa9-500">New-AzureRmExpressRouteConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="95fa9-500">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="95fa9-501">Set-AzureRmExpressRouteConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="95fa9-501">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="95fa9-502">Lägg till stöd för att konfigurera TopLevel WebApplicationFirewall-princip</span><span class="sxs-lookup"><span data-stu-id="95fa9-502">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="95fa9-503">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="95fa9-503">New cmdlets added:</span></span>
        - <span data-ttu-id="95fa9-504">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="95fa9-504">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="95fa9-505">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="95fa9-505">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="95fa9-506">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="95fa9-506">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="95fa9-507">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="95fa9-507">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="95fa9-508">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="95fa9-508">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="95fa9-509">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="95fa9-509">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="95fa9-510">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="95fa9-510">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="95fa9-511">New-AzApplicationGatewayFirewallPolicy: parametrarna PolicySetting, ManagedRule har lagts till</span><span class="sxs-lookup"><span data-stu-id="95fa9-511">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="95fa9-512">Stöd för operator för geomatchning har lagts till på CustomRule</span><span class="sxs-lookup"><span data-stu-id="95fa9-512">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="95fa9-513">Geomatchning har lagts till i operatorn på FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="95fa9-513">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="95fa9-514">Stöd har lagts till för brandväggsprinciperna perListener och perSite</span><span class="sxs-lookup"><span data-stu-id="95fa9-514">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="95fa9-515">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="95fa9-515">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="95fa9-516">New-AzApplicationGatewayHttpListener: parametrarna FirewallPolicy, FirewallPolicyId har lagts till</span><span class="sxs-lookup"><span data-stu-id="95fa9-516">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="95fa9-517">New-AzApplicationGatewayPathRuleConfig: parametrarna FirewallPolicy, FirewallPolicyId har lagts till</span><span class="sxs-lookup"><span data-stu-id="95fa9-517">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="95fa9-518">Åtgärdat så att nödvändigt undernät med namnet AzureBastionSubnet i PSBastion kan vara skiftlägesokänsligt</span><span class="sxs-lookup"><span data-stu-id="95fa9-518">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="95fa9-519">Stöd för mål-FQDN:er i nätverksregler och översatt FQDN i NAT-regler för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="95fa9-519">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="95fa9-520">Lägg till stöd för resursen RouteTables för IpGroup på den högsta nivån</span><span class="sxs-lookup"><span data-stu-id="95fa9-520">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="95fa9-521">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="95fa9-521">New cmdlets added:</span></span>
        - <span data-ttu-id="95fa9-522">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="95fa9-522">New-AzIpGroup</span></span>
        - <span data-ttu-id="95fa9-523">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="95fa9-523">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="95fa9-524">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="95fa9-524">Get-AzIpGroup</span></span>
        - <span data-ttu-id="95fa9-525">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="95fa9-525">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="95fa9-526">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="95fa9-526">Az.ServiceFabric</span></span>
* <span data-ttu-id="95fa9-527">Ta bort cmdleten Add-AzServiceFabricApplicationCertificate eftersom det här scenariot omfattas av Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="95fa9-527">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="95fa9-528">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="95fa9-528">Az.Sql</span></span>
* <span data-ttu-id="95fa9-529">Stöd har lagts till för återställning av utelämnade databaser på hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="95fa9-529">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="95fa9-530">Inaktuella gamla cmdletar för granskning från kod.</span><span class="sxs-lookup"><span data-stu-id="95fa9-530">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="95fa9-531">Tog bort inaktuella alias:</span><span class="sxs-lookup"><span data-stu-id="95fa9-531">Removed deprecated aliases:</span></span>
* <span data-ttu-id="95fa9-532">Get-AzSqlDatabaseIndexRecommendations (använd Get-AzSqlDatabaseIndexRecommendation istället)</span><span class="sxs-lookup"><span data-stu-id="95fa9-532">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="95fa9-533">Get-AzSqlDatabaseRestorePoints (använd Get-AzSqlDatabaseRestorePoint istället)</span><span class="sxs-lookup"><span data-stu-id="95fa9-533">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="95fa9-534">Ta bort cmdleten Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="95fa9-534">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="95fa9-535">Ta bort alias för inaktuella cmdletar för inställningar för utvärdering av säkerhetsrisk</span><span class="sxs-lookup"><span data-stu-id="95fa9-535">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="95fa9-536">Inaktualisera cmdletar för inställningar för avancerad hotidentifiering</span><span class="sxs-lookup"><span data-stu-id="95fa9-536">Deprecate Advanced Threat Detection Settings cmdlets</span></span> 
* <span data-ttu-id="95fa9-537">Lägga till cmdletar för att inaktivera och aktivera känslighetsrekommendationer på kolumner i en databas.</span><span class="sxs-lookup"><span data-stu-id="95fa9-537">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="95fa9-538">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="95fa9-538">Az.Storage</span></span>
* <span data-ttu-id="95fa9-539">Stöd för att aktivera stora filresurser vid skapande eller uppdatering av lagringskonto</span><span class="sxs-lookup"><span data-stu-id="95fa9-539">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="95fa9-540">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="95fa9-540">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="95fa9-541">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="95fa9-541">Set-AzStorageAccount</span></span>
* <span data-ttu-id="95fa9-542">När du stänger/hämtar en filreferens kan du hoppa över kontrollen av huruvida indatasökvägen är en filkatalog eller en fil för att undvika problem med objekt som har status DeletePending</span><span class="sxs-lookup"><span data-stu-id="95fa9-542">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="95fa9-543">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="95fa9-543">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="95fa9-544">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="95fa9-544">Close-AzStorageFileHandle</span></span>
    
## <a name="280---october-2019"></a><span data-ttu-id="95fa9-545">2.8.0 – oktober 2019</span><span class="sxs-lookup"><span data-stu-id="95fa9-545">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="95fa9-546">Allmänt</span><span class="sxs-lookup"><span data-stu-id="95fa9-546">General</span></span>
* <span data-ttu-id="95fa9-547">AZ. HealthcareApis 1.0.0-version</span><span class="sxs-lookup"><span data-stu-id="95fa9-547">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="95fa9-548">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="95fa9-548">Az.Accounts</span></span>
* <span data-ttu-id="95fa9-549">Uppdatera telemetri och URL-omskrivning för genererade moduler, korrigera Windows-enhetstester.</span><span class="sxs-lookup"><span data-stu-id="95fa9-549">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="95fa9-550">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="95fa9-550">Az.ApiManagement</span></span>
* <span data-ttu-id="95fa9-551">**Set-AzApiManagementApi** – Tillagt stöd för att uppdatera Api till ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="95fa9-551">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="95fa9-552">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="95fa9-552">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="95fa9-553">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="95fa9-553">Az.Automation</span></span>
* <span data-ttu-id="95fa9-554">Åtgärdade cmdleten New-AzureAutomationSoftwareUpdateConfiguration för parametern för inställning av Linux-omstart.</span><span class="sxs-lookup"><span data-stu-id="95fa9-554">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="95fa9-555">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="95fa9-555">Az.Batch</span></span>
* <span data-ttu-id="95fa9-556">**Get-AzBatchNodeAgentSku** är inaktuell och ersätts av **Get-AzBatchSupportImage** i version 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="95fa9-556">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="95fa9-557">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="95fa9-557">Az.Compute</span></span>
* <span data-ttu-id="95fa9-558">Lägg till parametrarna Priority, EvictionPolicy och MaxPrice till cmdletarna New-AzVM och New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="95fa9-558">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="95fa9-559">Korrigera varningsmeddelande och hjälpdokument för cmdletarna Add-AzVMAdditionalUnattendContent och Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="95fa9-559">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="95fa9-560">Åtgärda – skipVmBackup-undantag för virtuella Linux-datorer med hanterade diskar för Set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="95fa9-560">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="95fa9-561">Åtgärda fel i uppdatera krypteringsinställningarna i set-AzVMDiskEncryptionExtension, scenario i två steg.</span><span class="sxs-lookup"><span data-stu-id="95fa9-561">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="95fa9-562">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="95fa9-562">Az.DataFactory</span></span>
* <span data-ttu-id="95fa9-563">Lägga till CRUD-kommandon för ADF V2-dataflödet: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow och Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="95fa9-563">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="95fa9-564">Lägger till åtgärdskommandon för ADF V2-dataflödesfelsökningssession: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand och Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="95fa9-564">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="95fa9-565">Uppdatera ADF .Net SDK-versionen till 4.2.0</span><span class="sxs-lookup"><span data-stu-id="95fa9-565">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="95fa9-566">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="95fa9-566">Az.DataLakeStore</span></span>
* <span data-ttu-id="95fa9-567">Korrigera kontovalidering så att konton med ”-” kan skickas utan domän</span><span class="sxs-lookup"><span data-stu-id="95fa9-567">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="95fa9-568">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="95fa9-568">Az.HealthcareApis</span></span>
* <span data-ttu-id="95fa9-569">PowerShell-versionen har uppdaterats till 1.0.0</span><span class="sxs-lookup"><span data-stu-id="95fa9-569">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="95fa9-570">Uppdaterade SDK-versionen till 1.0.2</span><span class="sxs-lookup"><span data-stu-id="95fa9-570">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="95fa9-571">Uppdatera i tester för att referera till en ny SDK-version</span><span class="sxs-lookup"><span data-stu-id="95fa9-571">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="95fa9-572">Utdatastrukturen har uppdaterats från kapslad till förenklad.</span><span class="sxs-lookup"><span data-stu-id="95fa9-572">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="95fa9-573">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="95fa9-573">Az.IotHub</span></span>
* <span data-ttu-id="95fa9-574">Lägg till ny routningskälla: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="95fa9-574">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="95fa9-575">Mindre felkorrigering: Get-AzIothub returnerar inte subscriptionId</span><span class="sxs-lookup"><span data-stu-id="95fa9-575">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="95fa9-576">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="95fa9-576">Az.Monitor</span></span>
* <span data-ttu-id="95fa9-577">Nya åtgärdsgruppsmottagare har lagts till för åtgärdsgrupp   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="95fa9-577">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="95fa9-578">Använd vanligt aviseringsschema som är aktiverat för mottagarna.</span><span class="sxs-lookup"><span data-stu-id="95fa9-578">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="95fa9-579">Detta gäller inte för SMS, push för Azure-app, ITSM och röstmottagare</span><span class="sxs-lookup"><span data-stu-id="95fa9-579">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="95fa9-580">Webhooks har nu stöd för Azure Active Directory-autentisering.</span><span class="sxs-lookup"><span data-stu-id="95fa9-580">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="95fa9-581">Az.Network</span><span class="sxs-lookup"><span data-stu-id="95fa9-581">Az.Network</span></span>
* <span data-ttu-id="95fa9-582">Lägg till ny cmdlet Get-AzAvailableServiceAlias som kan anropas för att hämta de alias som kan användas för tjänstslutpunktsprinciper.</span><span class="sxs-lookup"><span data-stu-id="95fa9-582">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="95fa9-583">Stöd för tillägg av trafikväljare har lagts till i gatewayanslutningar för virtuella nätverk</span><span class="sxs-lookup"><span data-stu-id="95fa9-583">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="95fa9-584">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="95fa9-584">New cmdlets added:</span></span>
        - <span data-ttu-id="95fa9-585">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="95fa9-585">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="95fa9-586">Cmdletar har uppdaterats med valfri parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="95fa9-586">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="95fa9-587">Lägg till stöd för ESP- och AH-protokoll i konfiguration av nätverkssäkerhetsregler</span><span class="sxs-lookup"><span data-stu-id="95fa9-587">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="95fa9-588">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="95fa9-588">Updated cmdlets:</span></span>
        - <span data-ttu-id="95fa9-589">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="95fa9-589">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="95fa9-590">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="95fa9-590">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="95fa9-591">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="95fa9-591">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="95fa9-592">Förbättra hanteringen av undantag i Cortex-cmdletar</span><span class="sxs-lookup"><span data-stu-id="95fa9-592">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="95fa9-593">Nya generationer och SKU:er för VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="95fa9-593">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="95fa9-594">Introducera nya generationer för VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="95fa9-594">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="95fa9-595">Introducera nya SKU:er med högt dataflöde för VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="95fa9-595">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="95fa9-596">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="95fa9-596">Az.RedisCache</span></span>
* <span data-ttu-id="95fa9-597">Uppdaterad referensdokumentation för ”set-AzRedisCache” för att inkludera saknade värden för parametern ”size”</span><span class="sxs-lookup"><span data-stu-id="95fa9-597">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="95fa9-598">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="95fa9-598">Az.Sql</span></span>
* <span data-ttu-id="95fa9-599">Lägg till stöd för inställningen Active Directory administratör på den hanterade instansen</span><span class="sxs-lookup"><span data-stu-id="95fa9-599">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="95fa9-600">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="95fa9-600">Az.Storage</span></span>
* <span data-ttu-id="95fa9-601">Uppdatera Lagringsklientbibliotek till 11.1.0</span><span class="sxs-lookup"><span data-stu-id="95fa9-601">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="95fa9-602">Lista containrar med hanteringsplans-API, kommer att listas med NextPageLink</span><span class="sxs-lookup"><span data-stu-id="95fa9-602">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="95fa9-603">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="95fa9-603">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="95fa9-604">Lista lagringskonton från prenumerationen, kommer att listas med NextPageLink</span><span class="sxs-lookup"><span data-stu-id="95fa9-604">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="95fa9-605">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="95fa9-605">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="95fa9-606">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="95fa9-606">Az.StorageSync</span></span>
* <span data-ttu-id="95fa9-607">Åtgärda problemet 9810 i Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="95fa9-607">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="95fa9-608">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="95fa9-608">Az.Websites</span></span>
* <span data-ttu-id="95fa9-609">Set-AzWebApp – uppdatering av ASP för en app misslyckades</span><span class="sxs-lookup"><span data-stu-id="95fa9-609">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="95fa9-610">2.7.0 – september 2019</span><span class="sxs-lookup"><span data-stu-id="95fa9-610">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="95fa9-611">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="95fa9-611">Az.ApiManagement</span></span>
* <span data-ttu-id="95fa9-612">Uppdatera ”-Format”-parameterbeskrivningen i ”Set-AzApiManagementPolicy”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="95fa9-612">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="95fa9-613">Referenser för den föråldrade cmdleten ”Update-AzApiManagementDeployment” har tagits bort från referensdokumentationen.</span><span class="sxs-lookup"><span data-stu-id="95fa9-613">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="95fa9-614">Använd ”Set-AzApiManagement” i stället.</span><span class="sxs-lookup"><span data-stu-id="95fa9-614">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="95fa9-615">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="95fa9-615">Az.Automation</span></span>
* <span data-ttu-id="95fa9-616">Stavfel har korrigerats i exempel i referensdokumentationen för ”Register-AzAutomationDscNode”</span><span class="sxs-lookup"><span data-stu-id="95fa9-616">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="95fa9-617">Klargörande har lagts till om OS-begränsningar för Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="95fa9-617">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="95fa9-618">Null-referensundantag har korrigerats för -Wait-alternativet i Start-AzAutomationRunbook-cmdleten.</span><span class="sxs-lookup"><span data-stu-id="95fa9-618">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="95fa9-619">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="95fa9-619">Az.Compute</span></span>
* <span data-ttu-id="95fa9-620">Lägg till UploadSizeInBytes-parameter till New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="95fa9-620">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="95fa9-621">Lägg till Incremental-parameter till New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="95fa9-621">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="95fa9-622">Lägg till en funktion för virtuella datorer med låg prioritet:</span><span class="sxs-lookup"><span data-stu-id="95fa9-622">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="95fa9-623">MaxPrice-, EvictionPolicy- och Priority-parametrar har lagts till i New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="95fa9-623">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="95fa9-624">MaxPrice-parametern har lagts till i New-AzVmssConfig-, Update-AzVM- och Update-AzVmss-cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="95fa9-624">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="95fa9-625">Åtgärda problem med VM-referenser för Get-AzAvailabilitySet-cmdleten när alla tillgänglighetsuppsättningar i prenumerationen visas.</span><span class="sxs-lookup"><span data-stu-id="95fa9-625">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="95fa9-626">Korrigera null-undantaget för Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="95fa9-626">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="95fa9-627">Korrigera VHD-metoden för sökning relativt till slut.</span><span class="sxs-lookup"><span data-stu-id="95fa9-627">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="95fa9-628">Åtgärda UltraSSD-problem för New-AzVM och Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="95fa9-628">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="95fa9-629">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="95fa9-629">Az.DataFactory</span></span>
* <span data-ttu-id="95fa9-630">Lägger till 3 nya kommandon för ADF V2 – Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription och Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="95fa9-630">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="95fa9-631">ADF .Net SDK har uppdaterats till 4.1.3</span><span class="sxs-lookup"><span data-stu-id="95fa9-631">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="95fa9-632">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="95fa9-632">Az.HDInsight</span></span>
* <span data-ttu-id="95fa9-633">Anrop för icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="95fa9-633">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="95fa9-634">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="95fa9-634">Az.IotHub</span></span>
* <span data-ttu-id="95fa9-635">Lägg till stöd för att anropa redundans för en IotHub till den geo-länkade katastrofåterställningsregionen.</span><span class="sxs-lookup"><span data-stu-id="95fa9-635">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="95fa9-636">Lägg till stöd för att hantera meddelandeberikning för en IotHub.</span><span class="sxs-lookup"><span data-stu-id="95fa9-636">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="95fa9-637">Nya cmdlet:ar är:</span><span class="sxs-lookup"><span data-stu-id="95fa9-637">New cmdlets are:</span></span>
    - <span data-ttu-id="95fa9-638">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="95fa9-638">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="95fa9-639">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="95fa9-639">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="95fa9-640">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="95fa9-640">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="95fa9-641">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="95fa9-641">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="95fa9-642">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="95fa9-642">Az.Monitor</span></span>
* <span data-ttu-id="95fa9-643">Pekar på den senaste Monitor SDK:n, dvs. 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="95fa9-643">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="95fa9-644">Lägger till bakåtkompatibla ändringar i Metrics-cmdletarna, dvs. enhetsuppräkningen stöder flera nya värden.</span><span class="sxs-lookup"><span data-stu-id="95fa9-644">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="95fa9-645">Detta är skrivskyddade cmdletar, så det förekommer inga ändringar i inmatningen för cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="95fa9-645">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="95fa9-646">API-versionen för **ActionGroups**-begäranden är nu **2019-06-01**. Tidigare var den **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="95fa9-646">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="95fa9-647">Test av scenarier har uppdaterats för att anpassas till den här ändringen.</span><span class="sxs-lookup"><span data-stu-id="95fa9-647">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="95fa9-648">Ett nytt obligatoriskt argument har lagts till för konstruktorerna för klasserna **EmailReceiver** och **WebhookReceiver** – ett booleskt värde med namnet **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="95fa9-648">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="95fa9-649">Värdet är för närvarande fast till **false** så att den här icke-bakåtkompatibla ändringen är dold från cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="95fa9-649">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="95fa9-650">**Obs!** Det här är en tillfällig ändring som måste verifieras av Alerts-teamet.</span><span class="sxs-lookup"><span data-stu-id="95fa9-650">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="95fa9-651">Ordningen på argumenten för konstruktorn för klassen **Source** (relaterad till klassen **ScheduledQueryRuleSource**) har ändrats från den tidigare SDK:n.</span><span class="sxs-lookup"><span data-stu-id="95fa9-651">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="95fa9-652">Den här ändringen krävde korrigering av två enhetstest: de kompilerades, men testerna skickades inte.</span><span class="sxs-lookup"><span data-stu-id="95fa9-652">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="95fa9-653">Ordningen på argumenten för konstruktorn för klassen **AlertingAction** (relaterad till klassen **ScheduledQueryRuleSource**) har ändrats från den tidigare SDK:n.</span><span class="sxs-lookup"><span data-stu-id="95fa9-653">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="95fa9-654">Den här ändringen krävde korrigering av två enhetstest: de kompilerades, men testerna skickades inte.</span><span class="sxs-lookup"><span data-stu-id="95fa9-654">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="95fa9-655">Stöd för kriterier för dynamiskt tröskelvärde för måttavisering v2</span><span class="sxs-lookup"><span data-stu-id="95fa9-655">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="95fa9-656">New-AzMetricAlertRuleV2Criteria: skapar nu även kriterier för dynamiskt tröskelvärde</span><span class="sxs-lookup"><span data-stu-id="95fa9-656">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="95fa9-657">Add-AzMetricAlertRuleV2: accepterar nu även kriterier för dynamiskt tröskelvärde</span><span class="sxs-lookup"><span data-stu-id="95fa9-657">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="95fa9-658">Förbättringar i schemalagd frågeregel (SQR)</span><span class="sxs-lookup"><span data-stu-id="95fa9-658">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="95fa9-659">Cmdletar accepterar ”Location”-parameter i båda formaten, antingen platsen (t.ex. eastus) eller platsens visningsnamn (t.ex. USA, östra)</span><span class="sxs-lookup"><span data-stu-id="95fa9-659">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="95fa9-660">”Enabled”-parametern illustreras korrekt i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="95fa9-660">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="95fa9-661">Exempel för den valfria parametern ”ActionGroup” har lagts till</span><span class="sxs-lookup"><span data-stu-id="95fa9-661">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="95fa9-662">Förbättrade hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="95fa9-662">Overall improved help files</span></span>
* <span data-ttu-id="95fa9-663">Åtgärda bugg då omfattningstypen fastställs för ”Set-AzActionRule”</span><span class="sxs-lookup"><span data-stu-id="95fa9-663">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="95fa9-664">Az.Network</span><span class="sxs-lookup"><span data-stu-id="95fa9-664">Az.Network</span></span>
* <span data-ttu-id="95fa9-665">Korrigera felaktigt exempel i referensdokumentationen för ”New-AzApplicationGateway”</span><span class="sxs-lookup"><span data-stu-id="95fa9-665">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="95fa9-666">Lägg till anmärkning i ”Get-AzNetworkWatcherPacketCapture”-referensdokumentationen om hämtning av alla egenskaper för en paketinsamling</span><span class="sxs-lookup"><span data-stu-id="95fa9-666">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="95fa9-667">Exempel har korrigerats i ”Test-AzNetworkWatcherIPFlow”-referensdokumentationen för korrekt uppräkning av nätverkskort</span><span class="sxs-lookup"><span data-stu-id="95fa9-667">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="95fa9-668">Förbättrad tolkning av molnundantag för att visa eventuell ytterligare information</span><span class="sxs-lookup"><span data-stu-id="95fa9-668">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="95fa9-669">Förbättrad tolkning av molnundantag för att hantera ytterligare en typ av SDK-undantag</span><span class="sxs-lookup"><span data-stu-id="95fa9-669">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="95fa9-670">Felaktig mappning av säkerhetsregelmodeller har korrigerats</span><span class="sxs-lookup"><span data-stu-id="95fa9-670">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="95fa9-671">Egenskaper har lagts till för nätverksgränssnittet för funktionen Privat IP</span><span class="sxs-lookup"><span data-stu-id="95fa9-671">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="95fa9-672">Egenskapen ”PrivateEndpoint” har lagts till som en typ av PSResourceId till PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="95fa9-672">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="95fa9-673">Egenskapen ”PrivateLinkConnectionProperties” har lagts till som en typ av PSIpConfigurationConnectivityInformation till PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="95fa9-673">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="95fa9-674">Modellklassen PSIpConfigurationConnectivityInformation har lagts till</span><span class="sxs-lookup"><span data-stu-id="95fa9-674">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="95fa9-675">ApplicationRuleProtocolType ”mssql” har lagts till för Azure Firewall-resurs</span><span class="sxs-lookup"><span data-stu-id="95fa9-675">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="95fa9-676">MultiLink-stöd i virtuellt WAN</span><span class="sxs-lookup"><span data-stu-id="95fa9-676">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="95fa9-677">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="95fa9-677">New cmdlets</span></span>
        - <span data-ttu-id="95fa9-678">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="95fa9-678">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="95fa9-679">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="95fa9-679">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="95fa9-680">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="95fa9-680">Updated cmdlet:</span></span>
        - <span data-ttu-id="95fa9-681">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="95fa9-681">New-VpnSite</span></span>
        - <span data-ttu-id="95fa9-682">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="95fa9-682">Update-VpnSite</span></span>
        - <span data-ttu-id="95fa9-683">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="95fa9-683">New-VpnConnection</span></span>
        - <span data-ttu-id="95fa9-684">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="95fa9-684">Update-VpnConnection</span></span>
* <span data-ttu-id="95fa9-685">Dokument för vissa PowerShell-exempel har korrigerats så att Az-cmdletar används i stället för AzureRM-cmdletar</span><span class="sxs-lookup"><span data-stu-id="95fa9-685">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="95fa9-686">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="95fa9-686">Az.RecoveryServices</span></span>
* <span data-ttu-id="95fa9-687">Uppdatera AzureVMpolicy-objekt med ProtectedItemsCount-attribut</span><span class="sxs-lookup"><span data-stu-id="95fa9-687">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="95fa9-688">Ytterligare tester har lagts till för VM-princip och återställning av ursprungligt lagringskonto</span><span class="sxs-lookup"><span data-stu-id="95fa9-688">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="95fa9-689">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="95fa9-689">Az.Resources</span></span>
* <span data-ttu-id="95fa9-690">Åtgärda fel där det inte gick att anropa New-AzRoleAssignment utan parametern Scope.</span><span class="sxs-lookup"><span data-stu-id="95fa9-690">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="95fa9-691">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="95fa9-691">Az.ServiceFabric</span></span>
* <span data-ttu-id="95fa9-692">Stavfel har korrigerats i exempel för ”Update-AzServiceFabricReliability”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="95fa9-692">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="95fa9-693">Lägger till nya cmdletar för att hantera program och tjänster:</span><span class="sxs-lookup"><span data-stu-id="95fa9-693">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="95fa9-694">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="95fa9-694">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="95fa9-695">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="95fa9-695">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="95fa9-696">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="95fa9-696">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="95fa9-697">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="95fa9-697">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="95fa9-698">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="95fa9-698">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="95fa9-699">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="95fa9-699">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="95fa9-700">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="95fa9-700">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="95fa9-701">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="95fa9-701">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="95fa9-702">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="95fa9-702">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="95fa9-703">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="95fa9-703">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="95fa9-704">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="95fa9-704">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="95fa9-705">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="95fa9-705">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="95fa9-706">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="95fa9-706">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="95fa9-707">Service Fabric SDK har uppgraderats till version 1.2.0 som använder Service Fabric-resursprovidern med API-version 2019-03-01.</span><span class="sxs-lookup"><span data-stu-id="95fa9-707">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="95fa9-708">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="95fa9-708">Az.SignalR</span></span>
* <span data-ttu-id="95fa9-709">Lägg till Update-, Restart-, CheckNameAvailability- och GetUsage-cmdletar</span><span class="sxs-lookup"><span data-stu-id="95fa9-709">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="95fa9-710">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="95fa9-710">Az.Sql</span></span>
* <span data-ttu-id="95fa9-711">Uppdatera exempel i referensdokumentationen för ”Get-AzSqlElasticPool”</span><span class="sxs-lookup"><span data-stu-id="95fa9-711">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="95fa9-712">vCore-exempel för att skapa en elastisk pool (New-AzSqlElasticPool) har lagts till.</span><span class="sxs-lookup"><span data-stu-id="95fa9-712">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="95fa9-713">Ta bort verifieringen av EmailAddresses och kontrollen som bekräftar att EmailAdmins inte är falskt när EmailAddresses är tomt i Set-AzSqlServerAdvancedThreatProtectionPolicy och Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="95fa9-713">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="95fa9-714">Server-/databasgranskningsinställningar kan tas bort när det finns flera diagnostikinställningar som aktiverar granskningskategorin.</span><span class="sxs-lookup"><span data-stu-id="95fa9-714">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="95fa9-715">Åtgärda verifiering av e-postadresser i flera Sql Vulnerability Assessment-cmdletar (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting och Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="95fa9-715">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="95fa9-716">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="95fa9-716">Az.Storage</span></span>
* <span data-ttu-id="95fa9-717">Exempel i referensdokumentationen för ”Get-AzStorageAccountKey” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="95fa9-717">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="95fa9-718">Vid upp- och nedladdning av en Azure-fil kan SMB-egenskaperna för källfilen (t.ex. filattribut, tidpunkten då filen skapades och tidpunkten för den senaste skrivningen) sparas i målfilen</span><span class="sxs-lookup"><span data-stu-id="95fa9-718">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="95fa9-719">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="95fa9-719">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="95fa9-720">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="95fa9-720">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="95fa9-721">Korrigera problem med uppladdningen av blockblob med egenskaper/metadata för ImmutabilityPolicy i containrar.</span><span class="sxs-lookup"><span data-stu-id="95fa9-721">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="95fa9-722">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="95fa9-722">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="95fa9-723">Stöd för hantering av Azure-filresurser med API för hanteringsplan</span><span class="sxs-lookup"><span data-stu-id="95fa9-723">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="95fa9-724">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="95fa9-724">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="95fa9-725">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="95fa9-725">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="95fa9-726">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="95fa9-726">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="95fa9-727">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="95fa9-727">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="95fa9-728">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="95fa9-728">Az.Websites</span></span>
* <span data-ttu-id="95fa9-729">Åtgärdar problemet där webapp-taggar togs bort när appen migrerades till nya ASP</span><span class="sxs-lookup"><span data-stu-id="95fa9-729">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="95fa9-730">Åtgärda Publish-AzureWebapp så att det fungerar i Linux och Windows</span><span class="sxs-lookup"><span data-stu-id="95fa9-730">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="95fa9-731">Uppdatera exempel i ”Get-AzWebAppPublishingProfile”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="95fa9-731">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="95fa9-732">2.6.0 – augusti 2019</span><span class="sxs-lookup"><span data-stu-id="95fa9-732">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="95fa9-733">Allmänt</span><span class="sxs-lookup"><span data-stu-id="95fa9-733">General</span></span>
* <span data-ttu-id="95fa9-734">Åtgärdade diverse skrivfel i flera moduler</span><span class="sxs-lookup"><span data-stu-id="95fa9-734">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="95fa9-735">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="95fa9-735">Az.Accounts</span></span>
* <span data-ttu-id="95fa9-736">Stöd för användartilldelat MSI i Azure Functions-autentisering (#9479)</span><span class="sxs-lookup"><span data-stu-id="95fa9-736">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="95fa9-737">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="95fa9-737">Az.Aks</span></span>
* <span data-ttu-id="95fa9-738">Åtgärda problem med utdata för "Get-AzAks"</span><span class="sxs-lookup"><span data-stu-id="95fa9-738">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="95fa9-739">Mer information här: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="95fa9-739">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="95fa9-740">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="95fa9-740">Az.ApiManagement</span></span>
* <span data-ttu-id="95fa9-741">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="95fa9-741">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="95fa9-742">Uppdatera .net-NuGet-versionen, som inte tillämpar begränsningar för productId, apiId och userId</span><span class="sxs-lookup"><span data-stu-id="95fa9-742">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="95fa9-743">**Get-AzApiManagementProduct** – Lade till stöd för frågekörning mot produkter via API.</span><span class="sxs-lookup"><span data-stu-id="95fa9-743">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="95fa9-744">**New-AzApiManagementApiRevision** – Korrigering för problem där ApiRevisionDescription inte angavs vid skapande av ny API-revision https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="95fa9-744">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="95fa9-745">Åtgärdade skrivfel i modellen "PsApiManagementOAuth2AuthrozationServer" till "PsApiManagementOAuth2AuthorizationServer"</span><span class="sxs-lookup"><span data-stu-id="95fa9-745">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="95fa9-746">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="95fa9-746">Az.Batch</span></span>
* <span data-ttu-id="95fa9-747">Åtgärdade skrivfel i hjälpmeddelande och dokumentation till att skriva Windows med versaler</span><span class="sxs-lookup"><span data-stu-id="95fa9-747">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="95fa9-748">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="95fa9-748">Az.Cdn</span></span>
* <span data-ttu-id="95fa9-749">Åtgärdade skrivfel i CDN-modulens konverteringshjälp</span><span class="sxs-lookup"><span data-stu-id="95fa9-749">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="95fa9-750">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="95fa9-750">Az.Compute</span></span>
* <span data-ttu-id="95fa9-751">Lägg till VmssId i New-AzVMConfig-cmdleten</span><span class="sxs-lookup"><span data-stu-id="95fa9-751">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="95fa9-752">Lägg till parametrarna TerminateScheduledEvents och TerminateScheduledEventNotBeforeTimeoutInMinutes i New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="95fa9-752">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="95fa9-753">Lägg till egenskapen HyperVGeneration till avbildningsobjekt för virtuell dator</span><span class="sxs-lookup"><span data-stu-id="95fa9-753">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="95fa9-754">Lägg till funktioner för Host och HostGroup</span><span class="sxs-lookup"><span data-stu-id="95fa9-754">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="95fa9-755">Nya cmdletar:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="95fa9-755">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="95fa9-756">HostId-parametern läggs till i New-AzVMConfig och New-AzVM</span><span class="sxs-lookup"><span data-stu-id="95fa9-756">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="95fa9-757">Uppdatera exempel i "Invoke-AzVMRunCommand"-dokumentationen till att använda rätt parameternamn</span><span class="sxs-lookup"><span data-stu-id="95fa9-757">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="95fa9-758">Uppdatera "-VolumeType"-beskrivningen i referensdokumentationen för "set-AzVMDiskEncryptionExtension" och "set-AzVmssDiskEncryptionExtension"</span><span class="sxs-lookup"><span data-stu-id="95fa9-758">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="95fa9-759">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="95fa9-759">Az.DataFactory</span></span>
* <span data-ttu-id="95fa9-760">Åtgärda skrivfel till att använda versaler för "Windows" i "New-AzDataFactoryEncryptValue"-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="95fa9-760">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="95fa9-761">Uppdaterade ADF .Net SDK-versionen till 4.1.2</span><span class="sxs-lookup"><span data-stu-id="95fa9-761">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="95fa9-762">Lägg till parametrarna "DataProxyIntegrationRuntimeName", "DataProxyStagingLinkedServiceName" och "DataProxyStagingPath" för "Set-AzureRmDataFactoryV2IntegrationRuntime"-cmd för att aktivera konfiguration av lokalt installerad integrationskörning som en proxy för SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="95fa9-762">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="95fa9-763">Uppdaterade PSTriggerRun till att visa utlöst pipeline, meddelande och egenskaper samt PSActivityRun till att visa aktivitetstypen</span><span class="sxs-lookup"><span data-stu-id="95fa9-763">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="95fa9-764">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="95fa9-764">Az.DataLakeStore</span></span>
* <span data-ttu-id="95fa9-765">Korrigering av frysning av Get-DataLakeStoreDeletedItem för fel eller fjärrundantag.</span><span class="sxs-lookup"><span data-stu-id="95fa9-765">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="95fa9-766">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="95fa9-766">Az.EventHub</span></span>
* <span data-ttu-id="95fa9-767">Korrigering av problem #9658 : Skrivfel i parametern VirtualNteworkRule i Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="95fa9-767">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="95fa9-768">Korrigering av problem #9558 : Set-AzEventHubNamespace använder PATCH i stället för PUT</span><span class="sxs-lookup"><span data-stu-id="95fa9-768">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="95fa9-769">lade till parametern EnableKafka i Set-AzEventHubNamespace-cmdleten</span><span class="sxs-lookup"><span data-stu-id="95fa9-769">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="95fa9-770">Korrigering av problem #9786 : kan inte skapa en regel med Endast lyssna-behörighet</span><span class="sxs-lookup"><span data-stu-id="95fa9-770">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="95fa9-771">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="95fa9-771">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="95fa9-772">Åtgärdade skrivfel i dokumentation där "Azure" skrevs helt med gemener</span><span class="sxs-lookup"><span data-stu-id="95fa9-772">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="95fa9-773">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="95fa9-773">Az.Monitor</span></span>
* <span data-ttu-id="95fa9-774">Åtgärdade felaktigt parameternamn i hjälpdokumentationen</span><span class="sxs-lookup"><span data-stu-id="95fa9-774">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="95fa9-775">Az.Network</span><span class="sxs-lookup"><span data-stu-id="95fa9-775">Az.Network</span></span>
* <span data-ttu-id="95fa9-776">Uppdaterade New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="95fa9-776">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="95fa9-777">Gjorde parametern "PublicIpAddress" inaktuell eftersom den aldrig används på serversidan.</span><span class="sxs-lookup"><span data-stu-id="95fa9-777">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="95fa9-778">Lade till den valfria parametern "Primary", som anger huruvida den aktuella IP-konfigurationen är den primära.</span><span class="sxs-lookup"><span data-stu-id="95fa9-778">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="95fa9-779">Förbättrade hanteringen av felundantag för begärande från SDK – åtgärdar problemet att tidigare SDK-undantag inte hanteras på rätt sätt, vilket leder till att viktig felinformation inte visas</span><span class="sxs-lookup"><span data-stu-id="95fa9-779">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="95fa9-780">Justerade valideringslogiken för IPv6-IP-prefix till att kontrollera korrekt IPv6-prefixlängd.</span><span class="sxs-lookup"><span data-stu-id="95fa9-780">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="95fa9-781">Uppdaterade Get-AzVirtualNetworkSubnetConfig: Lade till parameter som anges till get av undernätets resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="95fa9-781">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="95fa9-782">Uppdaterade beskrivningen av parametern Location för AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="95fa9-782">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="95fa9-783">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="95fa9-783">Az.OperationalInsights</span></span>
* <span data-ttu-id="95fa9-784">Uppdaterade dokumentation för "New-AzOperationalInsightsLinuxSyslogDataSource"</span><span class="sxs-lookup"><span data-stu-id="95fa9-784">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="95fa9-785">Lade till exempel</span><span class="sxs-lookup"><span data-stu-id="95fa9-785">Added example</span></span>
    - <span data-ttu-id="95fa9-786">Uppdaterade beskrivningen av parametern "-Name"</span><span class="sxs-lookup"><span data-stu-id="95fa9-786">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="95fa9-787">Lade till ett exempel för New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="95fa9-787">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="95fa9-788">Ändrade beskrivningen av parametern -Name för New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="95fa9-788">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="95fa9-789">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="95fa9-789">Az.RecoveryServices</span></span>
* <span data-ttu-id="95fa9-790">Uppdatera "Get-AzRecoveryServicesBackupJobDetail.md"</span><span class="sxs-lookup"><span data-stu-id="95fa9-790">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="95fa9-791">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="95fa9-791">Az.Resources</span></span>
* <span data-ttu-id="95fa9-792">Lägg till stöd för den nya API-versionen från 2019-05-10 för Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="95fa9-792">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="95fa9-793">Lägg till stöd för "copy.count = 0" för variabler, resurser och egenskaper</span><span class="sxs-lookup"><span data-stu-id="95fa9-793">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="95fa9-794">Resurser med "condition = false" eller "copy.count = 0" tas bort i complete-läget</span><span class="sxs-lookup"><span data-stu-id="95fa9-794">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="95fa9-795">Lägg till ett exempel på tilldelning av princip på prenumerationsnivå i hjälpdokumentationen</span><span class="sxs-lookup"><span data-stu-id="95fa9-795">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="95fa9-796">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="95fa9-796">Az.ServiceBus</span></span>
* <span data-ttu-id="95fa9-797">Korrigering av problem #9658 : Skrivfel i parametern VirtualNetworkRule i set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="95fa9-797">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="95fa9-798">Korrigering av problem #9786 : kan inte skapa en regel med Endast lyssna-behörighet</span><span class="sxs-lookup"><span data-stu-id="95fa9-798">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="95fa9-799">Lade till det nya kommandot "Test-AzServiceBusNameAvailability" för att kontrollera namntillgängligheten för kö och ämne</span><span class="sxs-lookup"><span data-stu-id="95fa9-799">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="95fa9-800">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="95fa9-800">Az.ServiceFabric</span></span>
* <span data-ttu-id="95fa9-801">Åtgärda buggar med tillägg av nodtyps-cmdlet:</span><span class="sxs-lookup"><span data-stu-id="95fa9-801">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="95fa9-802">NullReferenceException-bugg när resursgrupp hade annan vmss som inte är relaterad till Service Fabric-klustret.</span><span class="sxs-lookup"><span data-stu-id="95fa9-802">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="95fa9-803">Åtgärdar problemet: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="95fa9-803">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="95fa9-804">Åtgärda bugg där cmdleten misslyckades om virtualNetwork var i en annan resursgrupp än klustret.</span><span class="sxs-lookup"><span data-stu-id="95fa9-804">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="95fa9-805">Åtgärdar problemet: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="95fa9-805">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="95fa9-806">AzServiceFabricApplicationCertificate-cmdleten görs inaktuell</span><span class="sxs-lookup"><span data-stu-id="95fa9-806">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="95fa9-807">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="95fa9-807">Az.Sql</span></span>
* <span data-ttu-id="95fa9-808">Uppdatera dokumentation om gamla gransknings-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="95fa9-808">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="95fa9-809">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="95fa9-809">Az.Storage</span></span>
* <span data-ttu-id="95fa9-810">Uppdatera hjälpen för Get/Close-AzStorageFileHandle genom att lägga till fler scenarier i cmdlet-exempel och uppdatera parameterbeskrivningar</span><span class="sxs-lookup"><span data-stu-id="95fa9-810">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="95fa9-811">Stöd för StandardBlobTier i uppladdningsblob och kopieringsblob</span><span class="sxs-lookup"><span data-stu-id="95fa9-811">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="95fa9-812">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="95fa9-812">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="95fa9-813">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="95fa9-813">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="95fa9-814">Stöd för rehydratiseringsprioritet i kopieringsblob</span><span class="sxs-lookup"><span data-stu-id="95fa9-814">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="95fa9-815">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="95fa9-815">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="95fa9-816">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="95fa9-816">Az.Websites</span></span>
* <span data-ttu-id="95fa9-817">Lägg till klargöranden gällande parametern -AppSettings i Set-AzWebApp och Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="95fa9-817">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="95fa9-818">2.5.0 – July 2019</span><span class="sxs-lookup"><span data-stu-id="95fa9-818">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="95fa9-819">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="95fa9-819">Az.Accounts</span></span>
* <span data-ttu-id="95fa9-820">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="95fa9-820">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="95fa9-821">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="95fa9-821">Az.ApplicationInsights</span></span>
* <span data-ttu-id="95fa9-822">Korrigera skrivfel i exempel i dokumentationen för Remove-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="95fa9-822">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="95fa9-823">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="95fa9-823">Az.Automation</span></span>
* <span data-ttu-id="95fa9-824">Korrigera skrivfel i resurssträng</span><span class="sxs-lookup"><span data-stu-id="95fa9-824">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="95fa9-825">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="95fa9-825">Az.CognitiveServices</span></span>
* <span data-ttu-id="95fa9-826">Stöd för NetworkRuleSet har lagts till.</span><span class="sxs-lookup"><span data-stu-id="95fa9-826">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="95fa9-827">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="95fa9-827">Az.Compute</span></span>
* <span data-ttu-id="95fa9-828">Lägg till saknade egenskaper (ComputerName, OsName, OsVersion och HyperVGeneration) för visningsobjekt i den virtuella datorinstansen.</span><span class="sxs-lookup"><span data-stu-id="95fa9-828">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="95fa9-829">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="95fa9-829">Az.ContainerRegistry</span></span>
* <span data-ttu-id="95fa9-830">Åtgärda skrivfel i Remove-AzContainerRegistryReplication för parametern Replication</span><span class="sxs-lookup"><span data-stu-id="95fa9-830">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="95fa9-831">Mer information finns här: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="95fa9-831">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="95fa9-832">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="95fa9-832">Az.DataFactory</span></span>
* <span data-ttu-id="95fa9-833">ADF .Net SDK-versionen har uppdaterats till 4.1.0</span><span class="sxs-lookup"><span data-stu-id="95fa9-833">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="95fa9-834">Korrigera skrivfel i dokumentationen för Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="95fa9-834">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="95fa9-835">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="95fa9-835">Az.EventHub</span></span>
* <span data-ttu-id="95fa9-836">Ny cmmdlet har lagts till för att skapa SAS-token: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="95fa9-836">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="95fa9-837">verifierings- och felmeddelande har lagts till för authorizationrules-rättigheter om endast "hantera" har tilldelats</span><span class="sxs-lookup"><span data-stu-id="95fa9-837">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="95fa9-838">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="95fa9-838">Az.KeyVault</span></span>
* <span data-ttu-id="95fa9-839">Stöd har lagts till för att ange KeySize för certifikatprinciper</span><span class="sxs-lookup"><span data-stu-id="95fa9-839">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="95fa9-840">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="95fa9-840">Az.LogicApp</span></span>
* <span data-ttu-id="95fa9-841">Korrigering för Get-AzIntegrationAccountMap för att lista alla mappningstyper</span><span class="sxs-lookup"><span data-stu-id="95fa9-841">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="95fa9-842">Ny MapType-parameter har lagts till för filtrering</span><span class="sxs-lookup"><span data-stu-id="95fa9-842">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="95fa9-843">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="95fa9-843">Az.ManagedServices</span></span>
* <span data-ttu-id="95fa9-844">Stöd för API-versionen 2019-06-01 (GA) har lagts till</span><span class="sxs-lookup"><span data-stu-id="95fa9-844">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="95fa9-845">Az.Network</span><span class="sxs-lookup"><span data-stu-id="95fa9-845">Az.Network</span></span>
* <span data-ttu-id="95fa9-846">Lägg till stöd för privat slutpunkt och privat länktjänst</span><span class="sxs-lookup"><span data-stu-id="95fa9-846">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="95fa9-847">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="95fa9-847">New cmdlets</span></span>
        - <span data-ttu-id="95fa9-848">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="95fa9-848">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="95fa9-849">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="95fa9-849">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="95fa9-850">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="95fa9-850">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="95fa9-851">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="95fa9-851">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="95fa9-852">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="95fa9-852">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="95fa9-853">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="95fa9-853">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="95fa9-854">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="95fa9-854">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="95fa9-855">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="95fa9-855">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="95fa9-856">Nedanstående kommandon för funktionen har uppdaterats: Flaggan PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies på undernätet i VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="95fa9-856">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="95fa9-857">Uppdaterade New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="95fa9-857">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="95fa9-858">Valfri parameter har lagts till – PrivateEndpointNetworkPoliciesFlag som konfigurerar huruvida nätverksprinciper ska tillämpas på en privat slutpunkt i det här undernätet.</span><span class="sxs-lookup"><span data-stu-id="95fa9-858">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="95fa9-859">Valfri parameter har lagts till – PrivateLinkServiceNetworkPoliciesFlag som konfigurerar huruvida nätverksprinciper ska tillämpas på en privat länktjänst i det här undernätet.</span><span class="sxs-lookup"><span data-stu-id="95fa9-859">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="95fa9-860">AzPrivateLinkService för cmdlet-parametern ServiceName har bytt namn till Name med aliaset ServiceName för bakåtkompatibilitet</span><span class="sxs-lookup"><span data-stu-id="95fa9-860">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="95fa9-861">Aktivera ICMP-protokoll för konfiguration av nätverkssäkerhetsregler</span><span class="sxs-lookup"><span data-stu-id="95fa9-861">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="95fa9-862">Uppdaterade cmdletar</span><span class="sxs-lookup"><span data-stu-id="95fa9-862">Updated cmdlets</span></span>
        - <span data-ttu-id="95fa9-863">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="95fa9-863">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="95fa9-864">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="95fa9-864">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="95fa9-865">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="95fa9-865">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="95fa9-866">Lägg till ConnectionProtocolType (Ikev1/Ikev2) som en konfigurerbar parameter för New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="95fa9-866">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="95fa9-867">Lägg till PrivateIpAddressVersion i LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="95fa9-867">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="95fa9-868">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="95fa9-868">Updated cmdlet:</span></span>
        - <span data-ttu-id="95fa9-869">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="95fa9-869">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="95fa9-870">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="95fa9-870">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="95fa9-871">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="95fa9-871">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="95fa9-872">Uppdatering av Application Gateway-kommandot New-AzApplicationGatewayProbeConfig för stöd av anpassad port i Probe</span><span class="sxs-lookup"><span data-stu-id="95fa9-872">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="95fa9-873">Uppdaterade New-AzApplicationGatewayProbeConfig: Den valfria parametern Port som används för avsökning i serverdelen har lagts till.</span><span class="sxs-lookup"><span data-stu-id="95fa9-873">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="95fa9-874">Denna parameter gäller för SKU:erna Standard_V2 och WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="95fa9-874">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="95fa9-875">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="95fa9-875">Az.OperationalInsights</span></span>
* <span data-ttu-id="95fa9-876">Uppdaterade standardversionen för sparade sökningar till 1.</span><span class="sxs-lookup"><span data-stu-id="95fa9-876">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="95fa9-877">Åtgärdade hantering av anpassad log null regex</span><span class="sxs-lookup"><span data-stu-id="95fa9-877">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="95fa9-878">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="95fa9-878">Az.RecoveryServices</span></span>
* <span data-ttu-id="95fa9-879">Uppdatera Get-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="95fa9-879">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="95fa9-880">Uppdatera Get-AzRecoveryServicesBackupContainer.md</span><span class="sxs-lookup"><span data-stu-id="95fa9-880">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="95fa9-881">Uppdatera Get-AzRecoveryServicesVault.md</span><span class="sxs-lookup"><span data-stu-id="95fa9-881">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="95fa9-882">Uppdatera Wait-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="95fa9-882">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="95fa9-883">Uppdatera Set-AzRecoveryServicesVaultContext.md</span><span class="sxs-lookup"><span data-stu-id="95fa9-883">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="95fa9-884">Uppdatera Get-AzRecoveryServicesBackupItem.md</span><span class="sxs-lookup"><span data-stu-id="95fa9-884">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="95fa9-885">Uppdatera Get-AzRecoveryServicesBackupRecoveryPoint.md</span><span class="sxs-lookup"><span data-stu-id="95fa9-885">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="95fa9-886">Uppdatera Restore-AzRecoveryServicesBackupItem.md</span><span class="sxs-lookup"><span data-stu-id="95fa9-886">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="95fa9-887">Uppdaterat tjänstanrop för avregistrering av container för Azure-filresurs</span><span class="sxs-lookup"><span data-stu-id="95fa9-887">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="95fa9-888">Uppdatera Set-AzRecoveryServicesAsrAlertSetting.md</span><span class="sxs-lookup"><span data-stu-id="95fa9-888">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="95fa9-889">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="95fa9-889">Az.Resources</span></span>
- <span data-ttu-id="95fa9-890">Ta bort den cmdlet som saknas och som refereras i dokumentationen till New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="95fa9-890">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="95fa9-891">Princip-cmdletar har uppdaterats så att de använder den nya API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="95fa9-891">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="95fa9-892">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="95fa9-892">Az.ServiceBus</span></span>
* <span data-ttu-id="95fa9-893">Ny cmmdlet har lagts till för att skapa SAS-token: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="95fa9-893">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="95fa9-894">verifierings- och felmeddelande har lagts till för authorizationrules-rättigheter om endast "hantera" har tilldelats</span><span class="sxs-lookup"><span data-stu-id="95fa9-894">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="95fa9-895">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="95fa9-895">Az.Sql</span></span>
* <span data-ttu-id="95fa9-896">Åtgärda saknade exempel för Set-AzSqlDatabaseSecondary cmdlet</span><span class="sxs-lookup"><span data-stu-id="95fa9-896">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="95fa9-897">Åtgärda angivna återkommande genomsökningar för bedömning av säkerhetsrisk utan angivna e-postadresser</span><span class="sxs-lookup"><span data-stu-id="95fa9-897">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="95fa9-898">Korrigera ett skrivfel i ett varningsmeddelande.</span><span class="sxs-lookup"><span data-stu-id="95fa9-898">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="95fa9-899">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="95fa9-899">Az.Storage</span></span>
* <span data-ttu-id="95fa9-900">Uppdatera exempel i referensdokumentationen för Get-AzStorageAccount så att rätt parameternamn används</span><span class="sxs-lookup"><span data-stu-id="95fa9-900">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="95fa9-901">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="95fa9-901">Az.StorageSync</span></span>
* <span data-ttu-id="95fa9-902">Lägger till cmdleten Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="95fa9-902">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="95fa9-903">Åtgärda problem 9551 så att TierFilesOlderThanDays föredras</span><span class="sxs-lookup"><span data-stu-id="95fa9-903">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="95fa9-904">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="95fa9-904">Az.Websites</span></span>
* <span data-ttu-id="95fa9-905">Åtgärdar ett fel där vissa SiteConfig-egenskaper inte returnerades av Get-AzWebApp och Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="95fa9-905">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="95fa9-906">Lägger till en ny platsparameter för Get-AzDeletedWebApp och Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="95fa9-906">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="95fa9-907">Åtgärdar ett fel i kloning av webbapp-platser som använder New-AzWebApp-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="95fa9-907">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="95fa9-908">2.4.0 – juli 2019</span><span class="sxs-lookup"><span data-stu-id="95fa9-908">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="95fa9-909">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="95fa9-909">Az.Accounts</span></span>
* <span data-ttu-id="95fa9-910">Lägg till stöd för profil-cmdletar</span><span class="sxs-lookup"><span data-stu-id="95fa9-910">Add support for profile cmdlets</span></span>
* <span data-ttu-id="95fa9-911">Lägg till stöd för miljöer och dataplaner i genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="95fa9-911">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="95fa9-912">Åtgärda bugg där fel slutpunkt i vissa fall användes för cmdletar för dataplaner i Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="95fa9-912">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="95fa9-913">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="95fa9-913">Az.Advisor</span></span>
* <span data-ttu-id="95fa9-914">GA-version av Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="95fa9-914">GA release of Az.Advisor</span></span>
* <span data-ttu-id="95fa9-915">Den här modulen ingår nu som en del av `Az`-sammanslagningsmodulen</span><span class="sxs-lookup"><span data-stu-id="95fa9-915">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="95fa9-916">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="95fa9-916">Az.ApiManagement</span></span>
* <span data-ttu-id="95fa9-917">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="95fa9-917">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="95fa9-918">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="95fa9-918">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="95fa9-919">Stöd för att fråga prenumerationer efter användare och produkt har lagts till</span><span class="sxs-lookup"><span data-stu-id="95fa9-919">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="95fa9-920">Stöd för att fråga med hjälp av omfång ”/”, ”/apis”, ”/apis/echo-api” har lagts till</span><span class="sxs-lookup"><span data-stu-id="95fa9-920">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="95fa9-921">Korrigering av problem https://github.com/Azure/azure-powershell/issues/9307 och https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="95fa9-921">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="95fa9-922">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="95fa9-922">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="95fa9-923">Stöd för att ange ”ApiVersion” och ”ApiVersionSetId” när API:er importeras har lagts till</span><span class="sxs-lookup"><span data-stu-id="95fa9-923">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="95fa9-924">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="95fa9-924">Az.Automation</span></span>
* <span data-ttu-id="95fa9-925">Bugg med cmdleten Set-AzAutomationConnectionFieldValue för att hantera strängvärde har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="95fa9-925">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="95fa9-926">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="95fa9-926">Az.Compute</span></span>
* <span data-ttu-id="95fa9-927">Lägg till parametern HyperVGeneration i New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="95fa9-927">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="95fa9-928">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="95fa9-928">Az.DataFactory</span></span>
* <span data-ttu-id="95fa9-929">Uppdaterar utdata från ADF-cmdletar som hämtar aktivitetskörningar, hämtar pipelinekörningar och hämtar utlösarkörningar för stöd för Select-Object-pipe.</span><span class="sxs-lookup"><span data-stu-id="95fa9-929">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="95fa9-930">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="95fa9-930">Az.EventGrid</span></span>
* <span data-ttu-id="95fa9-931">Korrigera stavfel i dokumentation om ”New-AzEventGridSubscription”</span><span class="sxs-lookup"><span data-stu-id="95fa9-931">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="95fa9-932">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="95fa9-932">Az.IotHub</span></span>
* <span data-ttu-id="95fa9-933">Lägg till stöd för att återskapa principnycklar för auktorisering.</span><span class="sxs-lookup"><span data-stu-id="95fa9-933">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="95fa9-934">Az.Network</span><span class="sxs-lookup"><span data-stu-id="95fa9-934">Az.Network</span></span>
* <span data-ttu-id="95fa9-935">”RoutingPreference” har lagts till i offentliga IP-taggar</span><span class="sxs-lookup"><span data-stu-id="95fa9-935">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="95fa9-936">Förbättra exempel för referensdokumentation om ”Get-AzNetworkServiceTag”</span><span class="sxs-lookup"><span data-stu-id="95fa9-936">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="95fa9-937">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="95fa9-937">Az.PolicyInsights</span></span>
* <span data-ttu-id="95fa9-938">Åtgärda problem med null-referens i Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="95fa9-938">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="95fa9-939">Mer information här: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="95fa9-939">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="95fa9-940">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="95fa9-940">Az.OperationalInsights</span></span>
* <span data-ttu-id="95fa9-941">Modellen för CustomLog-datakälla som returneras i Get-AzOperationalInsightsDataSource har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="95fa9-941">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="95fa9-942">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="95fa9-942">Az.RecoveryServices</span></span>
* <span data-ttu-id="95fa9-943">Kommandot get-policy för IaaSVM:er har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="95fa9-943">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="95fa9-944">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="95fa9-944">Az.Resources</span></span>
    - <span data-ttu-id="95fa9-945">Korrigera hjälptext för den översta parametern i Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="95fa9-945">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="95fa9-946">Lägg till växlingsstöd på klientsidan för Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="95fa9-946">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="95fa9-947">Lägg till nya parametrar för Set-AzPolicyAssignment, -PolicyParameters och -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="95fa9-947">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="95fa9-948">En mängd dokument- och exempeluppdateringar för Policy-cmdletar</span><span class="sxs-lookup"><span data-stu-id="95fa9-948">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="95fa9-949">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="95fa9-949">Az.ServiceBus</span></span>
* <span data-ttu-id="95fa9-950">Korrigering av problem #4938 – New-AzureRmServiceBusQueue returnerar BadRequest vid konfiguration av MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="95fa9-950">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="95fa9-951">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="95fa9-951">Az.Sql</span></span>
* <span data-ttu-id="95fa9-952">Lägg till cmdletar för instansredundansgrupper från förhandsversion till offentlig version</span><span class="sxs-lookup"><span data-stu-id="95fa9-952">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="95fa9-953">Stöd för granskning för Azure SQL Server\Database med nya cmdletar.</span><span class="sxs-lookup"><span data-stu-id="95fa9-953">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="95fa9-954">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="95fa9-954">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="95fa9-955">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="95fa9-955">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="95fa9-956">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="95fa9-956">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="95fa9-957">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="95fa9-957">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="95fa9-958">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="95fa9-958">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="95fa9-959">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="95fa9-959">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="95fa9-960">Ta bort begränsningar för e-post från inställningarna för sårbarhetsbedömning</span><span class="sxs-lookup"><span data-stu-id="95fa9-960">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="95fa9-961">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="95fa9-961">Az.Storage</span></span>
* <span data-ttu-id="95fa9-962">Ändra två parametrar ”-IndexDocument” och ”-ErrorDocument404Path” från ”krävs” till ”valfri” i cmdlet:</span><span class="sxs-lookup"><span data-stu-id="95fa9-962">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="95fa9-963">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="95fa9-963">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="95fa9-964">Uppdatera hjälpen för Get-AzStorageBlobContent genom att lägga till ett exempel</span><span class="sxs-lookup"><span data-stu-id="95fa9-964">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="95fa9-965">Visa mer felinformation när cmdleten misslyckas med StorageException</span><span class="sxs-lookup"><span data-stu-id="95fa9-965">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="95fa9-966">Stöd för att skapa eller uppdatera lagringskonto med Azure Files AAD DS-autentisering</span><span class="sxs-lookup"><span data-stu-id="95fa9-966">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="95fa9-967">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="95fa9-967">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="95fa9-968">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="95fa9-968">Set-AzStorageAccount</span></span>
* <span data-ttu-id="95fa9-969">Stöd för att lista eller stänga filreferenser för en filresurs, filkatalog eller en fil</span><span class="sxs-lookup"><span data-stu-id="95fa9-969">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="95fa9-970">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="95fa9-970">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="95fa9-971">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="95fa9-971">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="95fa9-972">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="95fa9-972">Az.StorageSync</span></span>
* <span data-ttu-id="95fa9-973">Den här modulen ingår nu som en del av `Az`-sammanslagningsmodulen</span><span class="sxs-lookup"><span data-stu-id="95fa9-973">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="95fa9-974">2.3.2 – juni 2019</span><span class="sxs-lookup"><span data-stu-id="95fa9-974">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="95fa9-975">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="95fa9-975">Az.Accounts</span></span>
* <span data-ttu-id="95fa9-976">Åtgärda bugg med felaktiga webbadresser som i vissa fall användes för Functions-anrop</span><span class="sxs-lookup"><span data-stu-id="95fa9-976">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="95fa9-977">Mer information här: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="95fa9-977">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="95fa9-978">Åtgärda problem med alias från AzureRM i Az-cmdletar</span><span class="sxs-lookup"><span data-stu-id="95fa9-978">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="95fa9-979">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="95fa9-979">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="95fa9-980">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="95fa9-980">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="95fa9-981">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="95fa9-981">Az.Compute</span></span>
* <span data-ttu-id="95fa9-982">Parameteruppsättningarna New-AzVm och New-AzVmss accepterar nu parametern ”ProximityPlacementGroup”.</span><span class="sxs-lookup"><span data-stu-id="95fa9-982">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="95fa9-983">Stavfel i referensdokumentationen för ”New-AzVM” har korrigerats</span><span class="sxs-lookup"><span data-stu-id="95fa9-983">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="95fa9-984">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="95fa9-984">Az.Dns</span></span>
* <span data-ttu-id="95fa9-985">Stavfel i hjälpexempel för ”Set-AzDnsZone” har korrigerats.</span><span class="sxs-lookup"><span data-stu-id="95fa9-985">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="95fa9-986">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="95fa9-986">Az.EventGrid</span></span>
* <span data-ttu-id="95fa9-987">Har uppdaterats för att använda API-versionen 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="95fa9-987">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="95fa9-988">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="95fa9-988">New cmdlets:</span></span>
    - <span data-ttu-id="95fa9-989">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="95fa9-989">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="95fa9-990">Skapar en ny Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="95fa9-990">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="95fa9-991">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="95fa9-991">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="95fa9-992">Hämtar information om en Event Grid-domän eller hämtar en lista med alla Event Grid-domäner i den aktuella Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="95fa9-992">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="95fa9-993">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="95fa9-993">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="95fa9-994">Tar bort en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="95fa9-994">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="95fa9-995">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="95fa9-995">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="95fa9-996">Återskapar nyckeln för delad åtkomst för en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="95fa9-996">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="95fa9-997">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="95fa9-997">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="95fa9-998">Hämtar de nycklar för delad åtkomst som används för att publicera händelser till en Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="95fa9-998">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="95fa9-999">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="95fa9-999">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="95fa9-1000">Skapar ett nytt Azure Event Grid-domänämne.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1000">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="95fa9-1001">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="95fa9-1001">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="95fa9-1002">Hämtar information om ett Event Grid-domänämne eller hämtar en lista med alla Event Grid-domänämnen under en specifik Event Grid-domän i nuvarande Azure</span><span class="sxs-lookup"><span data-stu-id="95fa9-1002">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="95fa9-1003">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="95fa9-1003">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="95fa9-1004">Tar bort ett befintligt Azure Event Grid-domänämne.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1004">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="95fa9-1005">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="95fa9-1005">Updated cmdlets:</span></span>
    - <span data-ttu-id="95fa9-1006">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="95fa9-1006">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="95fa9-1007">Lägg till nya obligatoriska parametrar för att stödja piping för den nya Event Grid-domänen och Event Grid-domänämnet för att göra det möjligt att skapa nya händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1007">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="95fa9-1008">Lägg till nya obligatoriska parametrar för att ange det nya Event Grid-domännamnet och/eller namnet på Event Grid-domänämnet för att göra det möjligt att skapa nya händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1008">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="95fa9-1009">Lägg till ny parameteruppsättningar för domäner och domänämnen för att göra det möjligt att återanvända befintliga parametrar (t.ex. EndPointType, SubjectBeginsWith osv).</span><span class="sxs-lookup"><span data-stu-id="95fa9-1009">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="95fa9-1010">Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="95fa9-1010">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="95fa9-1011">Förfallodatum för händelseprenumeration</span><span class="sxs-lookup"><span data-stu-id="95fa9-1011">Event subscription expiration date,</span></span>
            - <span data-ttu-id="95fa9-1012">Avancerade filterparametrar.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1012">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="95fa9-1013">Lägg till ny uppräkning för servicebusqueue som mål.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1013">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="95fa9-1014">Tillåt inte användning av ”Alla” i alternativet -IncludedEventType och ersätt det med</span><span class="sxs-lookup"><span data-stu-id="95fa9-1014">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="95fa9-1015">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="95fa9-1015">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="95fa9-1016">Lägg till ny valfria parametrar (Top, ODataQuery och NextLink) för att stödja sidnumrering och filtrering av resultat.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1016">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="95fa9-1017">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="95fa9-1017">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="95fa9-1018">Lägg till nya obligatoriska parametrar för att stödja piping för en Event Grid-domän och Event Grid-domänämnen för att göra det möjligt att ta bort befintliga händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1018">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="95fa9-1019">Lägg till nya obligatoriska parametrar för att ange Event Grid-domännamnet och/eller namnet på Event Grid-domänämnet för att göra det möjligt att ta bort befintliga händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1019">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="95fa9-1020">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="95fa9-1020">Az.FrontDoor</span></span>
* <span data-ttu-id="95fa9-1021">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="95fa9-1021">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="95fa9-1022">Lägg till stöd för transformeringar och nytt värde för automatisk komplettering för operatorer (RegEx)</span><span class="sxs-lookup"><span data-stu-id="95fa9-1022">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="95fa9-1023">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="95fa9-1023">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="95fa9-1024">Lägg till nya värden för automatisk komplettering</span><span class="sxs-lookup"><span data-stu-id="95fa9-1024">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="95fa9-1025">Az.Network</span><span class="sxs-lookup"><span data-stu-id="95fa9-1025">Az.Network</span></span>
* <span data-ttu-id="95fa9-1026">Lägg till stöd för resurs för virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="95fa9-1026">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="95fa9-1027">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="95fa9-1027">New cmdlets</span></span>
        - <span data-ttu-id="95fa9-1028">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="95fa9-1028">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="95fa9-1029">Lägg till AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="95fa9-1029">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="95fa9-1030">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="95fa9-1030">New cmdlets</span></span> 
        - <span data-ttu-id="95fa9-1031">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="95fa9-1031">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="95fa9-1032">Lägg till PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="95fa9-1032">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="95fa9-1033">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="95fa9-1033">New cmdlets</span></span> 
        - <span data-ttu-id="95fa9-1034">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="95fa9-1034">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="95fa9-1035">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="95fa9-1035">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="95fa9-1036">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="95fa9-1036">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="95fa9-1037">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="95fa9-1037">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="95fa9-1038">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="95fa9-1038">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="95fa9-1039">Lägg till PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="95fa9-1039">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="95fa9-1040">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="95fa9-1040">New cmdlets</span></span>
        - <span data-ttu-id="95fa9-1041">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="95fa9-1041">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="95fa9-1042">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="95fa9-1042">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="95fa9-1043">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="95fa9-1043">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="95fa9-1044">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="95fa9-1044">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="95fa9-1045">Nedanstående kommandon för funktionen har uppdaterats: Flaggan UseLocalAzureIpAddress på VpnConnection</span><span class="sxs-lookup"><span data-stu-id="95fa9-1045">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="95fa9-1046">New-AzVpnConnection har uppdaterats: Den valfria parametern -UseLocalAzureIpAddress har lagts till för att visa att en lokal IP-adress i Azure ska användas som källadress när anslutningen initieras.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1046">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="95fa9-1047">Set-AzVpnConnection har uppdaterats: Den valfria parametern -UseLocalAzureIpAddress har lagts till för att visa att en lokal IP-adress i Azure ska användas som källadress när anslutningen initieras.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1047">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="95fa9-1048">Det skrivskyddade fältet PeeredConnections har lagts till i ExpressRoute-peering.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1048">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="95fa9-1049">Det skrivskyddade fältet GlobalReachEnabled har lagts till i ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1049">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="95fa9-1050">Ett attribut för icke-bakåtkompatibla ändringar har lagts till för att lyfta fram utfasning av fältet AllowGlobalReach i modellen ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="95fa9-1050">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="95fa9-1051">Problem 8756 har åtgärdats: Fel vid användning av TargetListenerID med AzApplicationGatewayRedirectConfiguration-cmdletar</span><span class="sxs-lookup"><span data-stu-id="95fa9-1051">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="95fa9-1052">En bugg i New-AzApplicationGatewayPathRuleConfig som gjorde att regeluppsättningen för att återskapa inte kunde anges har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1052">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="95fa9-1053">Visningen av VirtualNetworkTaps i NetworkInterfaceIpConfiguration har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="95fa9-1053">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="95fa9-1054">Cortex Get-cmdletar för att visa en lista med alla delar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="95fa9-1054">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="95fa9-1055">Funktionen för att skapa VirtualHub-referenser för ExpressRouteGateways och VpnGateway har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="95fa9-1055">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="95fa9-1056">Stöd för tillgänglighetszoner i AzureFirewall och NatGateway har lagts till</span><span class="sxs-lookup"><span data-stu-id="95fa9-1056">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="95fa9-1057">Cmdleten Get-AzNetworkServiceTag har lagts till</span><span class="sxs-lookup"><span data-stu-id="95fa9-1057">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="95fa9-1058">Lägg till stöd för flera offentliga IP-adresser för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="95fa9-1058">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="95fa9-1059">Cmdleten New-AzFirewall har uppdaterats:</span><span class="sxs-lookup"><span data-stu-id="95fa9-1059">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="95fa9-1060">Parametern -PublicIpAddress som accepterar ett eller flera offentliga IP-adressobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="95fa9-1060">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="95fa9-1061">Parametern -VirtualNetwork som accepterar ett virtuellt nätverksobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="95fa9-1061">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="95fa9-1062">Metoderna AddPublicIpAddress och RemovePublicIpAddress har lagts till på brandväggsobjekt – dessa accepterar ett offentligt IP-adressobjekt som indata</span><span class="sxs-lookup"><span data-stu-id="95fa9-1062">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="95fa9-1063">Inaktuella parametrar -PublicIpName och -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="95fa9-1063">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="95fa9-1064">Nedanstående kommandon för funktionen har uppdaterats: Ange autentiseringsalternativ för VpnClient AAD till resurser för virtuella nätverksgatewayer.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1064">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="95fa9-1065">New-AzVirtualNetworkGateway har uppdaterats: De valfria parametrarna AadTenantUri, AadAudienceId och AadIssuerUri för att ange VpnClient AAD-autentiseringsalternativ på en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1065">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="95fa9-1066">Set-AzVirtualNetworkGateway har uppdaterats: De valfria parametrarna AadTenantUri, AadAudienceId och AadIssuerUri för att ange VpnClient AAD-autentiseringsalternativ på en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1066">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="95fa9-1067">Set-AzVirtualNetworkGateway har uppdaterats: Den valfria växelparametern RemoveAadAuthentication som tar bort VpnClient AAD-autentiseringsalternativ från en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1067">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="95fa9-1068">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="95fa9-1068">Az.OperationalInsights</span></span>
* <span data-ttu-id="95fa9-1069">Aktivera prisnivån **pergb2018** i kommandot ”New-AzureRmOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="95fa9-1069">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="95fa9-1070">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="95fa9-1070">Az.Resources</span></span>
* <span data-ttu-id="95fa9-1071">Stöd för ytterligare alternativ för att exportera en mall</span><span class="sxs-lookup"><span data-stu-id="95fa9-1071">Support for additional Template Export options</span></span>
    - <span data-ttu-id="95fa9-1072">Lägg till parametern ”-SkipResourceNameParameterization” till Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="95fa9-1072">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="95fa9-1073">Lägg till parametern ”-SkipAllParameterization” till Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="95fa9-1073">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="95fa9-1074">Lägg till parametern ”-Resource” till Export-AzResourceGroup för exporterad resursfiltrering</span><span class="sxs-lookup"><span data-stu-id="95fa9-1074">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="95fa9-1075">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="95fa9-1075">Az.ServiceFabric</span></span>
* <span data-ttu-id="95fa9-1076">Åtgärda att fel tumavtryck används vid tilläggning av certifikat i ByExistingKeyVault i vissa fall</span><span class="sxs-lookup"><span data-stu-id="95fa9-1076">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="95fa9-1077">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="95fa9-1077">Az.Sql</span></span>
* <span data-ttu-id="95fa9-1078">Åtgärda suffix för lagringsslutpunkt i Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="95fa9-1078">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="95fa9-1079">Åtgärda att aktivering av Advanced Data Security åsidosätter Advanced Threat Protection-princip</span><span class="sxs-lookup"><span data-stu-id="95fa9-1079">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="95fa9-1080">Nya cmdletar för Management.Sql som gör att kunderna kan lägga till nycklar för transparent datakryptering (TDE) och ange TDE-skydd för hanterade instanser</span><span class="sxs-lookup"><span data-stu-id="95fa9-1080">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="95fa9-1081">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="95fa9-1081">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="95fa9-1082">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="95fa9-1082">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="95fa9-1083">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="95fa9-1083">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="95fa9-1084">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="95fa9-1084">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="95fa9-1085">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="95fa9-1085">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="95fa9-1086">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="95fa9-1086">Az.Storage</span></span>
* <span data-ttu-id="95fa9-1087">Stöd för typerna FileStorage och SkuName Premium_ZRS när lagringskonton skapas</span><span class="sxs-lookup"><span data-stu-id="95fa9-1087">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="95fa9-1088">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="95fa9-1088">New-AzStorageAccount</span></span>
* <span data-ttu-id="95fa9-1089">Beskrivningen av cmdleten för bloboföränderlighet har förtydligats</span><span class="sxs-lookup"><span data-stu-id="95fa9-1089">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="95fa9-1090">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="95fa9-1090">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="95fa9-1091">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="95fa9-1091">Az.Websites</span></span>
* <span data-ttu-id="95fa9-1092">Optimerar Get-AzWebAppCertificate för att filtrera efter resursgrupp på servern i stället för klienten</span><span class="sxs-lookup"><span data-stu-id="95fa9-1092">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="95fa9-1093">Lägger till växlingsparametern -UseDisasterRecovery till Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="95fa9-1093">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="95fa9-1094">2.2.0 – juni 2019</span><span class="sxs-lookup"><span data-stu-id="95fa9-1094">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="95fa9-1095">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="95fa9-1095">Az.Cdn</span></span>
* <span data-ttu-id="95fa9-1096">Uppdaterade cmdletar för att ge stöd för rulesEngine-funktion baserat på API-version 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1096">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="95fa9-1097">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="95fa9-1097">Az.Compute</span></span>
* <span data-ttu-id="95fa9-1098">Lade till parameter `NoWait` som startar åtgärden och returnerar omedelbart, innan åtgärden har slutförts.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1098">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="95fa9-1099">Uppdaterade cmdletar:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="95fa9-1099">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="95fa9-1100">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="95fa9-1100">Az.EventHub</span></span>
* <span data-ttu-id="95fa9-1101">Korrigering för #9231 – Get-AzEventHubNamespace returnerar inga taggar</span><span class="sxs-lookup"><span data-stu-id="95fa9-1101">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="95fa9-1102">Korrigering för #9230 – Get-AzEventHubNamespace returnerar ResourceGroup istället för ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95fa9-1102">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="95fa9-1103">Az.Network</span><span class="sxs-lookup"><span data-stu-id="95fa9-1103">Az.Network</span></span>
* <span data-ttu-id="95fa9-1104">Uppdatera ResourceId och InputObject för NAT-gateway</span><span class="sxs-lookup"><span data-stu-id="95fa9-1104">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="95fa9-1105">Lägg till alias för ResourceId och InputObject</span><span class="sxs-lookup"><span data-stu-id="95fa9-1105">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="95fa9-1106">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="95fa9-1106">Az.PolicyInsights</span></span>
* <span data-ttu-id="95fa9-1107">Åtgärda Null-referensproblem i Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="95fa9-1107">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="95fa9-1108">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="95fa9-1108">Az.RecoveryServices</span></span>
* <span data-ttu-id="95fa9-1109">Minsta kvarhållning för IaaSVM-policy i dagar ändrat till 7 från 1</span><span class="sxs-lookup"><span data-stu-id="95fa9-1109">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="95fa9-1110">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="95fa9-1110">Az.ServiceBus</span></span>
* <span data-ttu-id="95fa9-1111">Korrigering för ärende #9182 – Get-AzServiceBusNamespace returnerar ResourceGroup istället för ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95fa9-1111">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="95fa9-1112">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="95fa9-1112">Az.ServiceFabric</span></span>
* <span data-ttu-id="95fa9-1113">Åtgärda stavfel i felmeddelandet för Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="95fa9-1113">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="95fa9-1114">Åtgärda saknat tecken i Service Fabric-kommandorader</span><span class="sxs-lookup"><span data-stu-id="95fa9-1114">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="95fa9-1115">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="95fa9-1115">Az.Sql</span></span>
* <span data-ttu-id="95fa9-1116">Lägg till parametern DnsZonePartner för New-AzureSqlInstance-cmdlet för att ge stöd för AutoDr för hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1116">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="95fa9-1117">Avvecklar cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="95fa9-1117">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="95fa9-1118">Döp om cmdletar för hotidentifiering till Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="95fa9-1118">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="95fa9-1119">Parametrarna New-AzSqlInstance -StorageSizeInGB och -LicenseType är nu valfria.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1119">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="95fa9-1120">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="95fa9-1120">Az.Websites</span></span>
* <span data-ttu-id="95fa9-1121">åtgärdar problemet där användningen av Set-AzWebApp och Set-AzWebAppSlot med -WebApp-egenskap tog bort taggarna</span><span class="sxs-lookup"><span data-stu-id="95fa9-1121">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="95fa9-1122">2.1.0 – maj 2019</span><span class="sxs-lookup"><span data-stu-id="95fa9-1122">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="95fa9-1123">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="95fa9-1123">Az.ApiManagement</span></span>
* <span data-ttu-id="95fa9-1124">Skapade nya cmdletar för att hantera diagnostik för global- och API-omfång</span><span class="sxs-lookup"><span data-stu-id="95fa9-1124">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="95fa9-1125">**Get-AzApiManagementDiagnostic** – Skaffa diagnostik konfigurerad för global- eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="95fa9-1125">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="95fa9-1126">**New-AzApiManagementDiagnostic** – Skapa ny diagnostik för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="95fa9-1126">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="95fa9-1127">**New-AzApiManagementHttpMessageDiagnostic** – Skapa diagnostikinställning om vilka rubriker som ska loggas och storleken på brödtextbyte</span><span class="sxs-lookup"><span data-stu-id="95fa9-1127">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="95fa9-1128">**New-AzApiManagementPipelineDiagnosticSetting** – Skapa diagnostikinställningar för inkommande/utgående HTTP-meddelanden till gatewayen.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1128">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="95fa9-1129">**New-AzApiManagementSamplingSetting** – Skapa samplinginställningar för begäranden/svar för en diagnostik</span><span class="sxs-lookup"><span data-stu-id="95fa9-1129">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="95fa9-1130">**Remove-AzApiManagementDiagnostic** – Ta bort en diagnostikenhet för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="95fa9-1130">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="95fa9-1131">**Set-AzApiManagementDiagnostic** – Uppdatera en diagnostikenhet för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="95fa9-1131">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="95fa9-1132">Skapade nya cmdletar för hantering av cacheminne i ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="95fa9-1132">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="95fa9-1133">**Get-AzApiManagementCache** – Hämta information om cacheminnet som anges av identifierare eller alla cacheminnen</span><span class="sxs-lookup"><span data-stu-id="95fa9-1133">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="95fa9-1134">**New-AzApiManagementCache** – Skapa ett nytt default-cacheminne eller cacheminne i en viss Azure-region</span><span class="sxs-lookup"><span data-stu-id="95fa9-1134">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="95fa9-1135">**Remove-AzApiManagementCache** – Ta bort ett cacheminne</span><span class="sxs-lookup"><span data-stu-id="95fa9-1135">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="95fa9-1136">**Remove-AzApiManagementCache** – Ta bort ett cacheminne</span><span class="sxs-lookup"><span data-stu-id="95fa9-1136">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="95fa9-1137">Skapade nya cmdletar för hantering av API-schema</span><span class="sxs-lookup"><span data-stu-id="95fa9-1137">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="95fa9-1138">**New-AzApiManagementSchema** – Skapa ett nytt schema för ett API</span><span class="sxs-lookup"><span data-stu-id="95fa9-1138">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="95fa9-1139">**Get-AzApiManagementSchema** – Hämta de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="95fa9-1139">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="95fa9-1140">**Remove-AzApiManagementSchema** – Ta bort de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="95fa9-1140">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="95fa9-1141">**Set-AzApiManagementSchema** – Uppdatera de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="95fa9-1141">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="95fa9-1142">Skapa ny cmdlet för att generera en användartoken.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1142">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="95fa9-1143">**New-AzApiManagementUserToken** – Skapa en ny användartoken som enligt standardinställning är giltig i 8 timmar. Token för GIT-användaren kan skapas med den här cmdleten./</span><span class="sxs-lookup"><span data-stu-id="95fa9-1143">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="95fa9-1144">Skapade en ny cmdlet för att hämta nätverksstatus</span><span class="sxs-lookup"><span data-stu-id="95fa9-1144">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="95fa9-1145">**Get-AzApiManagementNetworkStatus** – Hämta nätverksstatusanslutningen för resurserna som API Management-tjänsten är beroende av.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1145">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="95fa9-1146">Det här är användbart när du distribuerar ApiManagement-tjänsten i ett virtuellt nätverk och validerar om något beroende är brutet.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1146">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="95fa9-1147">Uppdaterade cmdlet **New-AzApiManagement** för att hantera ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="95fa9-1147">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="95fa9-1148">Lade till stöd för den nya SKU:n Consumption</span><span class="sxs-lookup"><span data-stu-id="95fa9-1148">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="95fa9-1149">Aktiverade stöd för att slå på flaggan EnableClientCertificate för SKU:n Consumption</span><span class="sxs-lookup"><span data-stu-id="95fa9-1149">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="95fa9-1150">Den nya cmdleten **New-AzApiManagementSslSetting** gör det möjligt att ställa in TLS/SSL-inställningen på ”Backend” och ”Frontend” (serverdel och klientdel).</span><span class="sxs-lookup"><span data-stu-id="95fa9-1150">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="95fa9-1151">Det här kan också användas till att konfigurera chiffer som 3DES och ServerProtocols som Http2 för Frontend för en ApiManagement-tjänst.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1151">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="95fa9-1152">Stöd har lagts till för att konfigurera värdnamnet DeveloperPortal på ApiManagement-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1152">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="95fa9-1153">Uppdaterade cmdletar **Get-AzApiManagementSsoToken** för att ta PsApiManagement-objekt som indata</span><span class="sxs-lookup"><span data-stu-id="95fa9-1153">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="95fa9-1154">Uppdaterad cmdleten för att visa infogade felmeddelanden</span><span class="sxs-lookup"><span data-stu-id="95fa9-1154">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="95fa9-1155">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Felkod: Felmeddelande av typen ValidationError: Ett eller flera fält innehåller felaktiga värden: Felinformation:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="95fa9-1155">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="95fa9-1156">Uppdaterade cmdlet **Export-AzApiManagementApi** för att exportera API:er i OpenApi 3.0-format</span><span class="sxs-lookup"><span data-stu-id="95fa9-1156">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="95fa9-1157">Uppdaterade cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="95fa9-1157">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="95fa9-1158">Importera API från dokumentspecifikationen OpenApi 3.0</span><span class="sxs-lookup"><span data-stu-id="95fa9-1158">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="95fa9-1159">Om du vill åsidosätta egenskapen PsApiManagementSchema specificerad i ett dokument (Swagger, Wadl, Wsdl, OpenApi).</span><span class="sxs-lookup"><span data-stu-id="95fa9-1159">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="95fa9-1160">Åsidosätta egenskapen ServiceUrl som specificeras i ett dokument.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1160">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="95fa9-1161">Uppdaterade cmdlet **Get-AzApiManagementPolicy** för att returnera policy i undantaget format av typen icke-XML med rawxml</span><span class="sxs-lookup"><span data-stu-id="95fa9-1161">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="95fa9-1162">Uppdaterade cmdlet **Set-AzApiManagementPolicy** för att godkänna policy i undantaget format av typen icke-XML med rawxml och XML undantaget med xml</span><span class="sxs-lookup"><span data-stu-id="95fa9-1162">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="95fa9-1163">Uppdaterad cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="95fa9-1163">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="95fa9-1164">Konfigurera API med OpenId auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1164">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="95fa9-1165">Skapa ett API i ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="95fa9-1165">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="95fa9-1166">Klona ett API med SourceApiId och SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1166">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="95fa9-1167">Möjlighet att konfigurera SubscriptionRequired i API-omfattningen.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1167">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="95fa9-1168">Uppdaterad cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="95fa9-1168">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="95fa9-1169">Konfigurera API med OpenId auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1169">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="95fa9-1170">Uppdatera ett API till ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="95fa9-1170">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="95fa9-1171">Möjlighet att konfigurera SubscriptionRequired i API-omfattningen.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1171">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="95fa9-1172">Uppdaterad cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="95fa9-1172">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="95fa9-1173">Klona en befintlig version med hjälp av SourceApiRevision (kopiera taggar, produkter, åtgärder och principer).</span><span class="sxs-lookup"><span data-stu-id="95fa9-1173">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="95fa9-1174">Den nya revisionen antar ApiId från den överordnade instansen.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1174">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="95fa9-1175">Tillhandahålla ApiRevisionDescription</span><span class="sxs-lookup"><span data-stu-id="95fa9-1175">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="95fa9-1176">Åsidosätta ServiceUrl vid kloning av ett API.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1176">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="95fa9-1177">Uppdaterad cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="95fa9-1177">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="95fa9-1178">Konfigurera AAD eller AADB2C med en Authority</span><span class="sxs-lookup"><span data-stu-id="95fa9-1178">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="95fa9-1179">Konfigurera SignupPolicy, SigninPolicy, ProfileEditingPolicy och PasswordResetPolicy</span><span class="sxs-lookup"><span data-stu-id="95fa9-1179">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="95fa9-1180">Uppdaterad cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="95fa9-1180">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="95fa9-1181">Kompensera för ny SubscriptonModel med Scope och UserId</span><span class="sxs-lookup"><span data-stu-id="95fa9-1181">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="95fa9-1182">Kompensera för gammal prenumerationsmodell med ProductId och UserId</span><span class="sxs-lookup"><span data-stu-id="95fa9-1182">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="95fa9-1183">Lägg till funktion för att aktivera AllowTracing på prenumerationsnivå.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1183">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="95fa9-1184">Uppdaterad cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="95fa9-1184">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="95fa9-1185">Kompensera för ny SubscriptonModel med Scope och UserId</span><span class="sxs-lookup"><span data-stu-id="95fa9-1185">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="95fa9-1186">Kompensera för gammal prenumerationsmodell med ProductId och UserId</span><span class="sxs-lookup"><span data-stu-id="95fa9-1186">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="95fa9-1187">Lägg till funktion för att aktivera AllowTracing på prenumerationsnivå.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1187">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="95fa9-1188">Uppdaterade följande cmdletar för att acceptera ResourceId som indata</span><span class="sxs-lookup"><span data-stu-id="95fa9-1188">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="95fa9-1189">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="95fa9-1189">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="95fa9-1190">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="95fa9-1190">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="95fa9-1191">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="95fa9-1191">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="95fa9-1192">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="95fa9-1192">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="95fa9-1193">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="95fa9-1193">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="95fa9-1194">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="95fa9-1194">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="95fa9-1195">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="95fa9-1195">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="95fa9-1196">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="95fa9-1196">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="95fa9-1197">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="95fa9-1197">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="95fa9-1198">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="95fa9-1198">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="95fa9-1199">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="95fa9-1199">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="95fa9-1200">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="95fa9-1200">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="95fa9-1201">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="95fa9-1201">Az.Automation</span></span>
* <span data-ttu-id="95fa9-1202">Uppdaterade Get-AzAutomationJobOutputRecord för att hantera postvärden av typen JSON och Text.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1202">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="95fa9-1203">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="95fa9-1203">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="95fa9-1204">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="95fa9-1204">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="95fa9-1205">Ändrade beteende för Start-AzAutomationDscCompilationJob till att bara starta jobbet istället för att vänta på slutförandet.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1205">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="95fa9-1206">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="95fa9-1206">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="95fa9-1207">Korrigering för Get-AzAutomationDscNode när using -Name returnerar alla noder.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1207">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="95fa9-1208">Nu returnerar den endast den matchande noden.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1208">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="95fa9-1209">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="95fa9-1209">Az.Compute</span></span>
* <span data-ttu-id="95fa9-1210">Lägg till parametrarna ProtectFromScaleIn och ProtectFromScaleSetAction i cmdleten Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1210">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="95fa9-1211">Nu är standardinställningen att vimpelparametern New-AzVM använder en tillgänglig plats om USA, östra inte stöds</span><span class="sxs-lookup"><span data-stu-id="95fa9-1211">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="95fa9-1212">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="95fa9-1212">Az.DataLakeStore</span></span>
* <span data-ttu-id="95fa9-1213">Uppdatera ADLS-sdk för att använda httpclient, integrera dataplanstestning med Azure-ramverk</span><span class="sxs-lookup"><span data-stu-id="95fa9-1213">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="95fa9-1214">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="95fa9-1214">Az.Monitor</span></span>
* <span data-ttu-id="95fa9-1215">Korrigera felaktiga parameternamn i hjälpexempel</span><span class="sxs-lookup"><span data-stu-id="95fa9-1215">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="95fa9-1216">Az.Network</span><span class="sxs-lookup"><span data-stu-id="95fa9-1216">Az.Network</span></span>
* <span data-ttu-id="95fa9-1217">Lägg till flaggan DisableBgpRoutePropagation i utdata för effektiv routningstabell</span><span class="sxs-lookup"><span data-stu-id="95fa9-1217">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="95fa9-1218">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="95fa9-1218">Updated cmdlet:</span></span>
        - <span data-ttu-id="95fa9-1219">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="95fa9-1219">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="95fa9-1220">Åtgärda dubbelstreck i dokumentationen New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="95fa9-1220">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="95fa9-1221">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="95fa9-1221">Az.Resources</span></span>
* <span data-ttu-id="95fa9-1222">Lägg till ny cmdlet Get-AzureRmDenyAssignment för att hämta tilldelningsnekanden</span><span class="sxs-lookup"><span data-stu-id="95fa9-1222">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="95fa9-1223">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="95fa9-1223">Az.Sql</span></span>
* <span data-ttu-id="95fa9-1224">Döp om Advanced Threat Protection-cmdletar för Advanced Data Security och aktivera Vulnerability Assessment som standard</span><span class="sxs-lookup"><span data-stu-id="95fa9-1224">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="95fa9-1225">2.0.0 – maj 2019</span><span class="sxs-lookup"><span data-stu-id="95fa9-1225">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="95fa9-1226">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="95fa9-1226">Az.Accounts</span></span>
* <span data-ttu-id="95fa9-1227">Uppdatera autentiseringsbiblioteket för att åtgärda ADFS-problem med autentisering av användarnamn/lösenord</span><span class="sxs-lookup"><span data-stu-id="95fa9-1227">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="95fa9-1228">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="95fa9-1228">Az.CognitiveServices</span></span>
* <span data-ttu-id="95fa9-1229">Visa endast Bing-ansvarsfriskrivning för Bing-sökningstjänster.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1229">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="95fa9-1230">Förbättra felmeddelande när det inte går att skapa konton.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1230">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="95fa9-1231">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="95fa9-1231">Az.Compute</span></span>
* <span data-ttu-id="95fa9-1232">Funktion för närhetsplaceringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1232">Proximity placement group feature.</span></span>
    - <span data-ttu-id="95fa9-1233">Följande nya cmdletar har lagts till:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="95fa9-1233">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="95fa9-1234">Den nya parametern ProximityPlacementGroupId har lagts till i följande cmdletar:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="95fa9-1234">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="95fa9-1235">Parametern StorageAccountType har lagts till i New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1235">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="95fa9-1236">TargetRegion för New-AzGalleryImageVersion kan innehålla StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1236">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="95fa9-1237">Växlingsparametern SkipShutdown har lagts till i Stop-AzVM och Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="95fa9-1237">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="95fa9-1238">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="95fa9-1238">Breaking changes</span></span>
    - <span data-ttu-id="95fa9-1239">Set-AzVMBootDiagnostics har ändrats till Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1239">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="95fa9-1240">Export-AzLogAnalyticThrottledRequests har ändrats till Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1240">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="95fa9-1241">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="95fa9-1241">Az.DeploymentManager</span></span>
* <span data-ttu-id="95fa9-1242">De första allmänt tillgängliga versionerna av cmdletar för Distributionshanteraren i Azure</span><span class="sxs-lookup"><span data-stu-id="95fa9-1242">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="95fa9-1243">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="95fa9-1243">Az.Dns</span></span>
* <span data-ttu-id="95fa9-1244">Automatisk delegering av DNS för NameServer</span><span class="sxs-lookup"><span data-stu-id="95fa9-1244">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="95fa9-1245">Det överordnade zonnamnet kan användas som ytterligare valfri parameter i cmdleten för att skapa DNS-zoner.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1245">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="95fa9-1246">Lägger till NS-poster för en nyligen skapad underordnad zon i den överordnade zonen.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1246">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="95fa9-1247">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="95fa9-1247">Az.FrontDoor</span></span>
* <span data-ttu-id="95fa9-1248">De första allmänt tillgängliga versionerna av cmdletar för Azure FrontDoor</span><span class="sxs-lookup"><span data-stu-id="95fa9-1248">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="95fa9-1249">Byt namn på WAF-cmdletar så att de omfattar ”Waf”</span><span class="sxs-lookup"><span data-stu-id="95fa9-1249">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="95fa9-1250">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="95fa9-1250">Az.HDInsight</span></span>
* <span data-ttu-id="95fa9-1251">Två cmdletar har tagits bort:</span><span class="sxs-lookup"><span data-stu-id="95fa9-1251">Removed two cmdlets:</span></span>
    - <span data-ttu-id="95fa9-1252">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="95fa9-1252">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="95fa9-1253">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="95fa9-1253">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="95fa9-1254">En ny cmdlet har lagts till, Set-AzHDInsightGatewayCredential, som ersätter Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="95fa9-1254">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="95fa9-1255">Uppdatera cmdleten Get-AzHDInsightJobOutput för att skilja mellan läsarrollen och HDInsight-operatörsrollen:</span><span class="sxs-lookup"><span data-stu-id="95fa9-1255">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="95fa9-1256">Användare med läsarrollen måste uttryckligen ange parametern ”DefaultStorageAccountKey”, annars uppstår fel.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1256">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="95fa9-1257">Användare med HDInsight-operatörsrollen påverkas inte.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1257">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="95fa9-1258">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="95fa9-1258">Az.Monitor</span></span>
* <span data-ttu-id="95fa9-1259">Nya cmdletar för SQR API (schemalagd frågeregel)</span><span class="sxs-lookup"><span data-stu-id="95fa9-1259">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="95fa9-1260">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="95fa9-1260">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="95fa9-1261">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="95fa9-1261">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="95fa9-1262">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="95fa9-1262">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="95fa9-1263">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="95fa9-1263">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="95fa9-1264">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="95fa9-1264">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="95fa9-1265">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="95fa9-1265">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="95fa9-1266">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="95fa9-1266">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="95fa9-1267">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="95fa9-1267">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="95fa9-1268">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="95fa9-1268">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="95fa9-1269">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="95fa9-1269">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="95fa9-1270">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="95fa9-1270">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="95fa9-1271">[Mer](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information om SQR API</span><span class="sxs-lookup"><span data-stu-id="95fa9-1271">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="95fa9-1272">Az.Monitor.md har uppdaterats för att omfatta cmdletar för måttbaserade aviseringsregler i GenV2 (inte klassiska)</span><span class="sxs-lookup"><span data-stu-id="95fa9-1272">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="95fa9-1273">Az.Network</span><span class="sxs-lookup"><span data-stu-id="95fa9-1273">Az.Network</span></span>
* <span data-ttu-id="95fa9-1274">Lägg till stöd för NAT Gateway-resurs</span><span class="sxs-lookup"><span data-stu-id="95fa9-1274">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="95fa9-1275">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="95fa9-1275">New cmdlets</span></span>
        - <span data-ttu-id="95fa9-1276">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="95fa9-1276">New-AzNatGateway</span></span>
        - <span data-ttu-id="95fa9-1277">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="95fa9-1277">Get-AzNatGateway</span></span>
        - <span data-ttu-id="95fa9-1278">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="95fa9-1278">Set-AzNatGateway</span></span>
        - <span data-ttu-id="95fa9-1279">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="95fa9-1279">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="95fa9-1280">Uppdaterade cmdletar</span><span class="sxs-lookup"><span data-stu-id="95fa9-1280">Updated cmdlets</span></span>
        - <span data-ttu-id="95fa9-1281">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="95fa9-1281">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="95fa9-1282">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="95fa9-1282">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="95fa9-1283">Nedanstående kommandon för funktionen har uppdaterats: Ange/ta bort anpassade vägar på Brooklyn Gateway.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1283">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="95fa9-1284">New-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ställa in adressprefix som anpassade vägar för att ange gateway.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1284">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="95fa9-1285">Set-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ange adressprefix som anpassade vägar för att ange gateway.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1285">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="95fa9-1286">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="95fa9-1286">Az.PolicyInsights</span></span>
* <span data-ttu-id="95fa9-1287">Stöd för att fråga efter information om principutvärdering.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1287">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="95fa9-1288">Lägg till parametern ”-Expand” för Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1288">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="95fa9-1289">Stöd för -Expand PolicyEvaluationDetails.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1289">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="95fa9-1290">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="95fa9-1290">Az.RecoveryServices</span></span>
* <span data-ttu-id="95fa9-1291">Stöd för att dela prenumeration mellan Azure och Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1291">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="95fa9-1292">Markering av kommande icke-bakåtkompatibla ändringar för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1292">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="95fa9-1293">Korrigering för återställningsplan och åtgärdsplan i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1293">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="95fa9-1294">Korrigering för mappning av uppdateringsnätverk i Azure Site Recovery för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1294">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="95fa9-1295">Korrigering för instruktioner för uppdateringsskydd i Azure Site Recovery för Azure till Azure för hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1295">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="95fa9-1296">Andra mindre korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1296">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="95fa9-1297">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="95fa9-1297">Az.Relay</span></span>
* <span data-ttu-id="95fa9-1298">Korrigera stavfel i kundriktade meddelanden</span><span class="sxs-lookup"><span data-stu-id="95fa9-1298">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="95fa9-1299">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="95fa9-1299">Az.ServiceBus</span></span>
* <span data-ttu-id="95fa9-1300">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="95fa9-1300">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="95fa9-1301">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="95fa9-1301">Az.Storage</span></span>
* <span data-ttu-id="95fa9-1302">Uppgradera till lagringsklientbiblioteket 10.0.1 (namnområdet för alla objekt från detta SDK ändras från ”Microsoft.WindowsAzure.Storage. *till ”Microsoft.Azure.Storage.* ”)</span><span class="sxs-lookup"><span data-stu-id="95fa9-1302">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="95fa9-1303">Uppgradera till Microsoft.Azure.Management.Storage 11.0.0 för att stödja den nya API-versionen 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1303">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="95fa9-1304">Standardlagringskontot i Skapa lagringskonto ändras från ”Storage” till ”StorageV2”</span><span class="sxs-lookup"><span data-stu-id="95fa9-1304">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="95fa9-1305">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="95fa9-1305">New-AzStorageAccount</span></span>
* <span data-ttu-id="95fa9-1306">Ändra lagringskontots cmdlet-utdata Sku.Name för att passa med indata-SkuName genom att lägga till ”-”. Till exempel ändras ”StandardLRS” till ”Standard_LRS”</span><span class="sxs-lookup"><span data-stu-id="95fa9-1306">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="95fa9-1307">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="95fa9-1307">New-AzStorageAccount</span></span>
    - <span data-ttu-id="95fa9-1308">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="95fa9-1308">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="95fa9-1309">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="95fa9-1309">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="95fa9-1310">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="95fa9-1310">Az.Websites</span></span>
* <span data-ttu-id="95fa9-1311">Egenskapen ”typ” konfigureras nu för PSSite-objekt som returneras av Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="95fa9-1311">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="95fa9-1312">Get-AzWebApp\*Metrics och Get-AzAppServicePlanMetrics markeras som inaktuella</span><span class="sxs-lookup"><span data-stu-id="95fa9-1312">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="95fa9-1313">1.8.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="95fa9-1313">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="95fa9-1314">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="95fa9-1314">Highlights since the last major release</span></span>
* <span data-ttu-id="95fa9-1315">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="95fa9-1315">General availability of `Az` module</span></span>
* <span data-ttu-id="95fa9-1316">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="95fa9-1316">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="95fa9-1317">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="95fa9-1317">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="95fa9-1318">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="95fa9-1318">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="95fa9-1319">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="95fa9-1319">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="95fa9-1320">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="95fa9-1320">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="95fa9-1321">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="95fa9-1321">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="95fa9-1322">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="95fa9-1322">Az.Accounts</span></span>
* <span data-ttu-id="95fa9-1323">Uppdatera Uninstall-AzureRm för att ta bort moduler i Mac på ett korrekt sätt</span><span class="sxs-lookup"><span data-stu-id="95fa9-1323">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="95fa9-1324">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="95fa9-1324">Az.Batch</span></span>
* <span data-ttu-id="95fa9-1325">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1325">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="95fa9-1326">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="95fa9-1326">Az.Cdn</span></span>
* <span data-ttu-id="95fa9-1327">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1327">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="95fa9-1328">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="95fa9-1328">Az.CognitiveServices</span></span>
* <span data-ttu-id="95fa9-1329">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1329">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="95fa9-1330">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="95fa9-1330">Az.Compute</span></span>
* <span data-ttu-id="95fa9-1331">Åtgärda problem med AEM-installationen om resurs-ID:n för diskar innehåller resourcegroups i gemener i resurs-ID:n</span><span class="sxs-lookup"><span data-stu-id="95fa9-1331">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="95fa9-1332">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1332">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="95fa9-1333">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="95fa9-1333">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="95fa9-1334">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="95fa9-1334">Az.DataFactory</span></span>
* <span data-ttu-id="95fa9-1335">Lägg till SsisProperties om NodeCount inte är null för hanterad integreringskörning.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1335">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="95fa9-1336">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="95fa9-1336">Az.DataLakeStore</span></span>
* <span data-ttu-id="95fa9-1337">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1337">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="95fa9-1338">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="95fa9-1338">Az.EventGrid</span></span>
* <span data-ttu-id="95fa9-1339">Hjälptexten för slutpunkten har uppdaterats för att visa att resurser ska skapas innan cmdletarna för att skapa/uppdatera händelseprenumerationer används.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1339">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="95fa9-1340">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="95fa9-1340">Az.EventHub</span></span>
* <span data-ttu-id="95fa9-1341">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="95fa9-1341">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="95fa9-1342">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="95fa9-1342">Az.HDInsight</span></span>
* <span data-ttu-id="95fa9-1343">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1343">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="95fa9-1344">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="95fa9-1344">Az.IotHub</span></span>
* <span data-ttu-id="95fa9-1345">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1345">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="95fa9-1346">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="95fa9-1346">Az.KeyVault</span></span>
* <span data-ttu-id="95fa9-1347">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1347">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="95fa9-1348">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="95fa9-1348">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="95fa9-1349">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="95fa9-1349">Az.MachineLearning</span></span>
* <span data-ttu-id="95fa9-1350">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1350">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="95fa9-1351">Az.Media</span><span class="sxs-lookup"><span data-stu-id="95fa9-1351">Az.Media</span></span>
* <span data-ttu-id="95fa9-1352">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1352">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="95fa9-1353">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="95fa9-1353">Az.Monitor</span></span>
  * <span data-ttu-id="95fa9-1354">Nya cmdletar för måttbaserad aviseringsregel i GenV2 (inte klassisk)</span><span class="sxs-lookup"><span data-stu-id="95fa9-1354">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="95fa9-1355">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="95fa9-1355">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="95fa9-1356">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="95fa9-1356">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="95fa9-1357">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="95fa9-1357">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="95fa9-1358">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="95fa9-1358">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="95fa9-1359">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="95fa9-1359">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="95fa9-1360">Monitor SDK har uppdaterats till version 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="95fa9-1360">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="95fa9-1361">Az.Network</span><span class="sxs-lookup"><span data-stu-id="95fa9-1361">Az.Network</span></span>
* <span data-ttu-id="95fa9-1362">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1362">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="95fa9-1363">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="95fa9-1363">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="95fa9-1364">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="95fa9-1364">Az.NotificationHubs</span></span>
* <span data-ttu-id="95fa9-1365">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1365">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="95fa9-1366">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="95fa9-1366">Az.OperationalInsights</span></span>
* <span data-ttu-id="95fa9-1367">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1367">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="95fa9-1368">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="95fa9-1368">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="95fa9-1369">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1369">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="95fa9-1370">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="95fa9-1370">Az.RecoveryServices</span></span>
* <span data-ttu-id="95fa9-1371">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1371">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="95fa9-1372">Tabellformatet för SQL i virtuella Azure-datorer har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="95fa9-1372">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="95fa9-1373">En alternativ metod för att hämta platser i AzureFileShare har lagts till</span><span class="sxs-lookup"><span data-stu-id="95fa9-1373">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="95fa9-1374">ScheduleRunDays i SchedulePolicy-objekt har uppdaterats enligt tidszon</span><span class="sxs-lookup"><span data-stu-id="95fa9-1374">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="95fa9-1375">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="95fa9-1375">Az.RedisCache</span></span>
* <span data-ttu-id="95fa9-1376">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1376">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="95fa9-1377">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="95fa9-1377">Az.Resources</span></span>
* <span data-ttu-id="95fa9-1378">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="95fa9-1378">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="95fa9-1379">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="95fa9-1379">Az.Sql</span></span>
* <span data-ttu-id="95fa9-1380">Ersätt Monitor SDK-beroende med vanlig kod</span><span class="sxs-lookup"><span data-stu-id="95fa9-1380">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="95fa9-1381">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1381">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="95fa9-1382">Förbättrad process för klassificering av flera kolumner.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1382">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="95fa9-1383">Inkludera SKU-egenskaper (SKU-namn, serie, kapacitet) i svaret från Get-AzSqlServerServiceObjective och formatera som tabell som standard.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1383">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="95fa9-1384">Möjlighet att använda Get-AzSqlServerServiceObjective efter plats utan att behöva en redan befintlig server i regionen.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1384">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="95fa9-1385">Stöd för tidszonsparametern när hanterade instanser skapas.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1385">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="95fa9-1386">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="95fa9-1386">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="95fa9-1387">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="95fa9-1387">Az.Websites</span></span>
* <span data-ttu-id="95fa9-1388">åtgärdar Set-AzWebApp och Set-AzWebAppSlot så att de inte tar bort taggar vid körning</span><span class="sxs-lookup"><span data-stu-id="95fa9-1388">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="95fa9-1389">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1389">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="95fa9-1390">SDK för WebSites har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1390">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="95fa9-1391">Egenskapen AdminSiteName har tagits bort från PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1391">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="95fa9-1392">1.7.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="95fa9-1392">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="95fa9-1393">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="95fa9-1393">Highlights since the last major release</span></span>
* <span data-ttu-id="95fa9-1394">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="95fa9-1394">General availability of `Az` module</span></span>
* <span data-ttu-id="95fa9-1395">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="95fa9-1395">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="95fa9-1396">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="95fa9-1396">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="95fa9-1397">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="95fa9-1397">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="95fa9-1398">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="95fa9-1398">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="95fa9-1399">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="95fa9-1399">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="95fa9-1400">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="95fa9-1400">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="95fa9-1401">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="95fa9-1401">Az.Accounts</span></span>
* <span data-ttu-id="95fa9-1402">Add-AzEnvironment och Set-AzEnvironment har uppdaterats för att godkänna parametern AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="95fa9-1402">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="95fa9-1403">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="95fa9-1403">Az.AnalysisServices</span></span>
* <span data-ttu-id="95fa9-1404">ServiceClient används i cmdletar för dataplan och den ursprungliga autentiseringslogiken har tagits bort</span><span class="sxs-lookup"><span data-stu-id="95fa9-1404">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="95fa9-1405">Add-AzureASAccount används för omslutning av Connect-AzAccount för att undvika en icke-bakåtkompatibel ändring</span><span class="sxs-lookup"><span data-stu-id="95fa9-1405">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="95fa9-1406">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="95fa9-1406">Az.Automation</span></span>
* <span data-ttu-id="95fa9-1407">Buggen för cmdleten New-AzAutomationSoftwareUpdateConfiguration för inkluderingar har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1407">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="95fa9-1408">Nu bör parametern IncludedKbNumber och IncludedPackageNameMask fungera.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1408">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="95fa9-1409">Felkorrigering för dynamiska grupper i uppdateringshanteringen för azure automation</span><span class="sxs-lookup"><span data-stu-id="95fa9-1409">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="95fa9-1410">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="95fa9-1410">Az.Compute</span></span>
* <span data-ttu-id="95fa9-1411">Lägg till parametern HyperVGeneration i New-AzDiskConfig och New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="95fa9-1411">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="95fa9-1412">Tillåt att virtuella datorer skapas med galleribilder från andra klientorganisationer.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1412">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="95fa9-1413">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="95fa9-1413">Az.ContainerInstance</span></span>
* <span data-ttu-id="95fa9-1414">Ett problem har åtgärdats i parametern -Command för New-AzContainerGroup som lade till ett avslutande tomt argument</span><span class="sxs-lookup"><span data-stu-id="95fa9-1414">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="95fa9-1415">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="95fa9-1415">Az.DataFactory</span></span>
* <span data-ttu-id="95fa9-1416">ADF .Net SDK-versionen har uppdaterats till 3.0.2</span><span class="sxs-lookup"><span data-stu-id="95fa9-1416">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="95fa9-1417">Cmdleten Set-AzDataFactoryV2 har uppdaterats med extra parametrar för inställningar som rör RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1417">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="95fa9-1418">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="95fa9-1418">Az.Resources</span></span>
* <span data-ttu-id="95fa9-1419">Förbättra hanteringen av providrar för Get-AzResource när parametrarna -ResourceId eller -ResourceGroupName, -Name och -ResourceType tillhandahålls</span><span class="sxs-lookup"><span data-stu-id="95fa9-1419">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="95fa9-1420">Förbättra felhanteringen för ”Test-AzDeployment” och ”Test-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="95fa9-1420">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="95fa9-1421">Hantera fel utanför distributionsvalideringen och ta med dem i kommandoutdata istället</span><span class="sxs-lookup"><span data-stu-id="95fa9-1421">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="95fa9-1422">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="95fa9-1422">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="95fa9-1423">Lägg till växlingsparametern -IgnoreDynamicParameters till en uppsättning av cmdletar för distribution för att hoppa över fråga i skript och jobbscenarier</span><span class="sxs-lookup"><span data-stu-id="95fa9-1423">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="95fa9-1424">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="95fa9-1424">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="95fa9-1425">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="95fa9-1425">Az.Sql</span></span>
* <span data-ttu-id="95fa9-1426">Stöd för dataklassificering av databaser.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1426">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="95fa9-1427">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="95fa9-1427">Az.Storage</span></span>
* <span data-ttu-id="95fa9-1428">Rapportera detaljfel när lagringskontext skapas med parametern -UseConnectedAccount, men utan inloggning på Azure-kontot</span><span class="sxs-lookup"><span data-stu-id="95fa9-1428">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="95fa9-1429">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="95fa9-1429">New-AzStorageContext</span></span>
* <span data-ttu-id="95fa9-1430">Stöd för att hantera Blob Service-egenskaper för ett angivet lagringskonto med API:et för hanteringsplan</span><span class="sxs-lookup"><span data-stu-id="95fa9-1430">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="95fa9-1431">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="95fa9-1431">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="95fa9-1432">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="95fa9-1432">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="95fa9-1433">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="95fa9-1433">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="95fa9-1434">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="95fa9-1434">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="95fa9-1435">Stöd för -AsJob-cmdletar för att ladda upp och ladda ned blobar och filer</span><span class="sxs-lookup"><span data-stu-id="95fa9-1435">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="95fa9-1436">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="95fa9-1436">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="95fa9-1437">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="95fa9-1437">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="95fa9-1438">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="95fa9-1438">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="95fa9-1439">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="95fa9-1439">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="95fa9-1440">1.6.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="95fa9-1440">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="95fa9-1441">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="95fa9-1441">Highlights since the last major release</span></span>
* <span data-ttu-id="95fa9-1442">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="95fa9-1442">General availability of `Az` module</span></span>
* <span data-ttu-id="95fa9-1443">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="95fa9-1443">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="95fa9-1444">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="95fa9-1444">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="95fa9-1445">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="95fa9-1445">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="95fa9-1446">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="95fa9-1446">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="95fa9-1447">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="95fa9-1447">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="95fa9-1448">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="95fa9-1448">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="95fa9-1449">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="95fa9-1449">Az.Automation</span></span>
* <span data-ttu-id="95fa9-1450">Azure Automation – ändring av uppdateringshantering för stöd för de nya funktionerna:</span><span class="sxs-lookup"><span data-stu-id="95fa9-1450">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="95fa9-1451">Dynamisk gruppering</span><span class="sxs-lookup"><span data-stu-id="95fa9-1451">Dynamic grouping</span></span>
    * <span data-ttu-id="95fa9-1452">För-/efterskrift</span><span class="sxs-lookup"><span data-stu-id="95fa9-1452">Pre-Post script</span></span>
    * <span data-ttu-id="95fa9-1453">Inställning för omstart</span><span class="sxs-lookup"><span data-stu-id="95fa9-1453">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="95fa9-1454">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="95fa9-1454">Az.Compute</span></span>
* <span data-ttu-id="95fa9-1455">Åtgärda problem med sökvägsmatchning i Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="95fa9-1455">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="95fa9-1456">Uppdatera Compute-klientbibliotek till 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1456">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="95fa9-1457">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="95fa9-1457">Az.KeyVault</span></span>
* <span data-ttu-id="95fa9-1458">Stöd för jokertecken för KeyVault-cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="95fa9-1458">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="95fa9-1459">Az.Network</span><span class="sxs-lookup"><span data-stu-id="95fa9-1459">Az.Network</span></span>
* <span data-ttu-id="95fa9-1460">Lägg till stöd för Threat Intelligence för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="95fa9-1460">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="95fa9-1461">Lägg till resurs för brandväggsprincip på översta nivå och anpassade regler för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="95fa9-1461">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="95fa9-1462">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="95fa9-1462">Az.RecoveryServices</span></span>
* <span data-ttu-id="95fa9-1463">SnapshotRetentionInDays har lagts till i Azure-principen för virtuella datorer för stöd av Instant RP</span><span class="sxs-lookup"><span data-stu-id="95fa9-1463">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="95fa9-1464">Pipe-stöd för avregistrering av container har lagts till</span><span class="sxs-lookup"><span data-stu-id="95fa9-1464">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="95fa9-1465">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="95fa9-1465">Az.Resources</span></span>
* <span data-ttu-id="95fa9-1466">Uppdatera stöd för jokertecken för Get-AzResource och Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="95fa9-1466">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="95fa9-1467">Uppdatera autentiseringsuppgifter som används vid allmänna anrop till ARM</span><span class="sxs-lookup"><span data-stu-id="95fa9-1467">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="95fa9-1468">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="95fa9-1468">Az.Sql</span></span>
* <span data-ttu-id="95fa9-1469">Cmdlet-parametern (ExcludeDetectionType) för Hotidentifiering ändrades från DetectionType till sträng[] för att framtidssäkra den när nya DetectionTypes läggs till, och även för att stödja automatisk ifyllning.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1469">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="95fa9-1470">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="95fa9-1470">Az.Storage</span></span>
* <span data-ttu-id="95fa9-1471">Stöd för att hämta/ange/ta bort hanteringsprincip på ett lagringskonto</span><span class="sxs-lookup"><span data-stu-id="95fa9-1471">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="95fa9-1472">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="95fa9-1472">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="95fa9-1473">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="95fa9-1473">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="95fa9-1474">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="95fa9-1474">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="95fa9-1475">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="95fa9-1475">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="95fa9-1476">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="95fa9-1476">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="95fa9-1477">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="95fa9-1477">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="95fa9-1478">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="95fa9-1478">Az.Websites</span></span>
* <span data-ttu-id="95fa9-1479">Åtgärda fel med ARM-mall som avbryter kloning av alla platser med 'New-AzWebApp -IncludeSourceWebAppSlots'</span><span class="sxs-lookup"><span data-stu-id="95fa9-1479">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="95fa9-1480">1.5.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="95fa9-1480">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="95fa9-1481">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="95fa9-1481">Az.Accounts</span></span>
* <span data-ttu-id="95fa9-1482">Lägg till kommandot Register-AzModule för stöd för AutoRest-genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="95fa9-1482">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="95fa9-1483">Uppdatera exempel för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="95fa9-1483">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="95fa9-1484">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="95fa9-1484">Az.Automation</span></span>
* <span data-ttu-id="95fa9-1485">Problem med att hämta vissa månadsscheman i flera Azure Automation-cmdletar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="95fa9-1485">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="95fa9-1486">Åtgärda problem med att Get-AzAutomationDscNode bara returnerar de 20 översta noderna.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1486">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="95fa9-1487">Nu returneras alla noder</span><span class="sxs-lookup"><span data-stu-id="95fa9-1487">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="95fa9-1488">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="95fa9-1488">Az.Cdn</span></span>
* <span data-ttu-id="95fa9-1489">Nya Powershell-cmdletar för att aktivera/inaktivera anpassade domän-HTTPS har lagts till och de gamla har gjorts inaktuella</span><span class="sxs-lookup"><span data-stu-id="95fa9-1489">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="95fa9-1490">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="95fa9-1490">Az.Compute</span></span>
* <span data-ttu-id="95fa9-1491">Lägg till stöd för jokertecken för Get-cmdletar</span><span class="sxs-lookup"><span data-stu-id="95fa9-1491">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="95fa9-1492">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="95fa9-1492">Az.DataFactory</span></span>
* <span data-ttu-id="95fa9-1493">ADF .Net SDK-versionen har uppdaterats till 3.0.1</span><span class="sxs-lookup"><span data-stu-id="95fa9-1493">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="95fa9-1494">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="95fa9-1494">Az.LogicApp</span></span>
* <span data-ttu-id="95fa9-1495">Åtgärda problemet med att ListWorkflows endast hämtar den första sidan med resultat</span><span class="sxs-lookup"><span data-stu-id="95fa9-1495">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="95fa9-1496">Az.Network</span><span class="sxs-lookup"><span data-stu-id="95fa9-1496">Az.Network</span></span>
* <span data-ttu-id="95fa9-1497">Lägg till stöd för jokertecken för Network-cmdletar</span><span class="sxs-lookup"><span data-stu-id="95fa9-1497">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="95fa9-1498">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="95fa9-1498">Az.RecoveryServices</span></span>
* <span data-ttu-id="95fa9-1499">Stöd har lagts till för SQL Server i virtuella Azure-datorer</span><span class="sxs-lookup"><span data-stu-id="95fa9-1499">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="95fa9-1500">SDK-uppdatering</span><span class="sxs-lookup"><span data-stu-id="95fa9-1500">SDK Update</span></span>
* <span data-ttu-id="95fa9-1501">Get-ProtectableItem-incheckning i VMappContainer har tagits bort</span><span class="sxs-lookup"><span data-stu-id="95fa9-1501">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="95fa9-1502">Name och ServerName har lagts till som parametrar för Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="95fa9-1502">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="95fa9-1503">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="95fa9-1503">Az.Resources</span></span>
* <span data-ttu-id="95fa9-1504">Lägg till parametern `-TemplateObject` i cmdletar för distribution</span><span class="sxs-lookup"><span data-stu-id="95fa9-1504">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="95fa9-1505">Mer information här: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="95fa9-1505">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="95fa9-1506">Åtgärda problem med piping av resultatet i `Get-AzResource` till `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="95fa9-1506">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="95fa9-1507">Mer information här: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="95fa9-1507">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="95fa9-1508">Åtgärda problem med ändring av JSON-datatyp när `Set-AzResource` körs</span><span class="sxs-lookup"><span data-stu-id="95fa9-1508">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="95fa9-1509">Mer information här: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="95fa9-1509">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="95fa9-1510">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="95fa9-1510">Az.Sql</span></span>
* <span data-ttu-id="95fa9-1511">AuditingEndpointsCommunicator uppdateras.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1511">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="95fa9-1512">Åtgärdar beteendet hos ett gränsscenario när nya diagnostikinställningar skapas.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1512">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="95fa9-1513">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="95fa9-1513">Az.Storage</span></span>
* <span data-ttu-id="95fa9-1514">Stöd för BlockBlobStorage när Storage-konto skapas      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="95fa9-1514">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="95fa9-1515">1.4.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="95fa9-1515">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="95fa9-1516">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="95fa9-1516">Az.AnalysisServices</span></span>
* <span data-ttu-id="95fa9-1517">Inaktuell AddAzureASAccount-cmdlet</span><span class="sxs-lookup"><span data-stu-id="95fa9-1517">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="95fa9-1518">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="95fa9-1518">Az.Automation</span></span>
* <span data-ttu-id="95fa9-1519">Hjälpen för Import-AzAutomationDscNodeConfiguration har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="95fa9-1519">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="95fa9-1520">Konfigurationsnamnsvalidering har lagts till i cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="95fa9-1520">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="95fa9-1521">Förbättrad felhantering för cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="95fa9-1521">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="95fa9-1522">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="95fa9-1522">Az.CognitiveServices</span></span>
* <span data-ttu-id="95fa9-1523">CustomSubdomainName har lagts till som en ny valfri parameter för New-AzCognitiveServicesAccount, som används för att ange underdomän för resursen.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1523">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="95fa9-1524">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="95fa9-1524">Az.Compute</span></span>
* <span data-ttu-id="95fa9-1525">Problemet med ID-parameteruppsättningar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="95fa9-1525">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="95fa9-1526">Get-AzVMExtension har uppdaterats så att alla installerade tillägg visas om parametern Name inte har angetts</span><span class="sxs-lookup"><span data-stu-id="95fa9-1526">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="95fa9-1527">Parametrarna Tag och ResourceId har lagts till i cmdleten Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="95fa9-1527">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="95fa9-1528">Get-AzVmssVM utan instans-ID och med InstanceView kan visa virtuella VMSS-datorer med instansvyn.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1528">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="95fa9-1529">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="95fa9-1529">Az.DataLakeStore</span></span>
* <span data-ttu-id="95fa9-1530">Cmdletar har lagts till för uppräkning och återställning av borttagna objekt i ADL</span><span class="sxs-lookup"><span data-stu-id="95fa9-1530">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="95fa9-1531">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="95fa9-1531">Az.EventHub</span></span>
* <span data-ttu-id="95fa9-1532">Ny boolesk egenskap SkipEmptyArchives har lagts till i Skip Empty Archives i CaptureDescription-klassen i Eventhub</span><span class="sxs-lookup"><span data-stu-id="95fa9-1532">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="95fa9-1533">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="95fa9-1533">Az.KeyVault</span></span>
* <span data-ttu-id="95fa9-1534">Taggning i Set-AzKeyVaultSecret har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="95fa9-1534">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="95fa9-1535">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="95fa9-1535">Az.LogicApp</span></span>
* <span data-ttu-id="95fa9-1536">Grundläggande SKU har lagts till för Integrationskonton</span><span class="sxs-lookup"><span data-stu-id="95fa9-1536">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="95fa9-1537">XSLT 2.0, XSLT 3.0 och Flytande mappningstyper har lagts till</span><span class="sxs-lookup"><span data-stu-id="95fa9-1537">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="95fa9-1538">Nya cmdletar för integrationskontosammansättningar</span><span class="sxs-lookup"><span data-stu-id="95fa9-1538">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="95fa9-1539">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="95fa9-1539">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="95fa9-1540">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="95fa9-1540">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="95fa9-1541">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="95fa9-1541">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="95fa9-1542">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="95fa9-1542">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="95fa9-1543">Nya cmdletar för batchkonfiguration för integrationskonto</span><span class="sxs-lookup"><span data-stu-id="95fa9-1543">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="95fa9-1544">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="95fa9-1544">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="95fa9-1545">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="95fa9-1545">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="95fa9-1546">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="95fa9-1546">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="95fa9-1547">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="95fa9-1547">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="95fa9-1548">Logic App-SDK har uppdaterats till version 4.1.0</span><span class="sxs-lookup"><span data-stu-id="95fa9-1548">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="95fa9-1549">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="95fa9-1549">Az.Monitor</span></span>
* <span data-ttu-id="95fa9-1550">Hjälpen för Get-AzMetric har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="95fa9-1550">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="95fa9-1551">Az.Network</span><span class="sxs-lookup"><span data-stu-id="95fa9-1551">Az.Network</span></span>
* <span data-ttu-id="95fa9-1552">Hjälpexempel för Add-AzApplicationGatewayCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="95fa9-1552">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="95fa9-1553">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="95fa9-1553">Az.OperationalInsights</span></span>
* <span data-ttu-id="95fa9-1554">Ytterligare stöd för datakällorna New och Get ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1554">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="95fa9-1555">Ny ApplicationInsights-typ har lagts till för att ge stöd för ”Get specific” och ”Get all” för ApplicationInsights-datakällor för angiven arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1555">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="95fa9-1556">Cmdleten New-AzOperationalInsightsApplicationInsightsDataSource har lagts till för att skapa datakälla med angivna parametrar för Application Insights-resurs: subscription Id, resourceGroupName och name.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1556">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="95fa9-1557">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="95fa9-1557">Az.Resources</span></span>
* <span data-ttu-id="95fa9-1558">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="95fa9-1558">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="95fa9-1559">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="95fa9-1559">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="95fa9-1560">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="95fa9-1560">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="95fa9-1561">Fel som gör att KeyCredentials inte kan skapas upprepade gånger har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="95fa9-1561">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="95fa9-1562">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="95fa9-1562">Az.Sql</span></span>
* <span data-ttu-id="95fa9-1563">Lägg till stöd för hyperskalanivån för SQL DB</span><span class="sxs-lookup"><span data-stu-id="95fa9-1563">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="95fa9-1564">Ett fel har åtgärdats där återställningen kunde misslyckas på grund av onödiga inställningsegenskaper i restore-förfrågan</span><span class="sxs-lookup"><span data-stu-id="95fa9-1564">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="95fa9-1565">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="95fa9-1565">Az.Websites</span></span>
* <span data-ttu-id="95fa9-1566">Rätt exempel i Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="95fa9-1566">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="95fa9-1567">1.3.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="95fa9-1567">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="95fa9-1568">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="95fa9-1568">Az.Accounts</span></span>
* <span data-ttu-id="95fa9-1569">Uppdatera till den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="95fa9-1569">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="95fa9-1570">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="95fa9-1570">Az.AnalysisServices</span></span>
<span data-ttu-id="95fa9-1571">Allmän tillgänglighet för Az.AnalysisServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1571">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="95fa9-1572">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="95fa9-1572">Az.Compute</span></span>
* <span data-ttu-id="95fa9-1573">AEM-tillägg: Lägg till stöd för UltraSSD-, P60-, P70- och P80-diskar</span><span class="sxs-lookup"><span data-stu-id="95fa9-1573">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="95fa9-1574">Uppdatera hjälpbeskrivning för Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="95fa9-1574">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="95fa9-1575">Uppdatera hjälpbeskrivning och exempel för Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="95fa9-1575">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="95fa9-1576">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="95fa9-1576">Az.RecoveryServices</span></span>
<span data-ttu-id="95fa9-1577">Allmän tillgänglighet för Az.RecoveryServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1577">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="95fa9-1578">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="95fa9-1578">Az.Resources</span></span>
* <span data-ttu-id="95fa9-1579">Korrigera taggar för resursgrupper</span><span class="sxs-lookup"><span data-stu-id="95fa9-1579">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="95fa9-1580">Mer information här: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="95fa9-1580">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="95fa9-1581">Åtgärda problem där `Get-AzureRmRoleAssignment` inte respekterar -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="95fa9-1581">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="95fa9-1582">Mer information här: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="95fa9-1582">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="95fa9-1583">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="95fa9-1583">Az.Sql</span></span>
* <span data-ttu-id="95fa9-1584">Lägga till Get/Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="95fa9-1584">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="95fa9-1585">Åtgärda problem där ett nullref-undantag uppstår när du kör SQL-cmdletar och inte är inloggad på ett Azure-konto</span><span class="sxs-lookup"><span data-stu-id="95fa9-1585">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="95fa9-1586">Åtgärda nullref-undantag i Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="95fa9-1586">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="95fa9-1587">1.2.1 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="95fa9-1587">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="95fa9-1588">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="95fa9-1588">Az.Accounts</span></span>
* <span data-ttu-id="95fa9-1589">Version med rätt version av autentisering</span><span class="sxs-lookup"><span data-stu-id="95fa9-1589">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="95fa9-1590">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="95fa9-1590">Az.AnalysisServices</span></span>
* <span data-ttu-id="95fa9-1591">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="95fa9-1591">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="95fa9-1592">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="95fa9-1592">Az.RecoveryServices</span></span>
* <span data-ttu-id="95fa9-1593">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="95fa9-1593">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="95fa9-1594">1.2.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="95fa9-1594">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="95fa9-1595">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="95fa9-1595">Az.Accounts</span></span>
* <span data-ttu-id="95fa9-1596">Lägga till interaktiv autentisering och autentisering med användarnamn/lösenord för endast Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="95fa9-1596">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="95fa9-1597">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="95fa9-1597">Update incorrect online help URLs</span></span>
* <span data-ttu-id="95fa9-1598">Lägga till varningsmeddelande i PS Core för Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="95fa9-1598">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="95fa9-1599">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="95fa9-1599">Az.Aks</span></span>
* <span data-ttu-id="95fa9-1600">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="95fa9-1600">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="95fa9-1601">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="95fa9-1601">Az.Automation</span></span>
* <span data-ttu-id="95fa9-1602">Stöd för Python 2-runbookflöden har lagts till</span><span class="sxs-lookup"><span data-stu-id="95fa9-1602">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="95fa9-1603">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="95fa9-1603">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="95fa9-1604">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="95fa9-1604">Az.Cdn</span></span>
* <span data-ttu-id="95fa9-1605">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="95fa9-1605">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="95fa9-1606">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="95fa9-1606">Az.Compute</span></span>
* <span data-ttu-id="95fa9-1607">Lägga till cmdleten Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="95fa9-1607">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="95fa9-1608">Lägga till TempDisk-parameter i Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="95fa9-1608">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="95fa9-1609">Korrigera varningsmeddelande för New-AzVM</span><span class="sxs-lookup"><span data-stu-id="95fa9-1609">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="95fa9-1610">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="95fa9-1610">Az.ContainerRegistry</span></span>
* <span data-ttu-id="95fa9-1611">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="95fa9-1611">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="95fa9-1612">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="95fa9-1612">Az.DataFactory</span></span>
* <span data-ttu-id="95fa9-1613">ADF .Net SDK-versionen har uppdaterats till 3.0.0</span><span class="sxs-lookup"><span data-stu-id="95fa9-1613">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="95fa9-1614">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="95fa9-1614">Az.DataLakeStore</span></span>
* <span data-ttu-id="95fa9-1615">Åtgärda problem med ADLS-slutpunkt vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="95fa9-1615">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="95fa9-1616">Mer information här: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="95fa9-1616">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="95fa9-1617">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="95fa9-1617">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="95fa9-1618">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="95fa9-1618">Az.IotHub</span></span>
* <span data-ttu-id="95fa9-1619">Lägga till kodningsformat i cmdleten Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1619">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="95fa9-1620">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="95fa9-1620">Az.KeyVault</span></span>
* <span data-ttu-id="95fa9-1621">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="95fa9-1621">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="95fa9-1622">Az.Network</span><span class="sxs-lookup"><span data-stu-id="95fa9-1622">Az.Network</span></span>
* <span data-ttu-id="95fa9-1623">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="95fa9-1623">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="95fa9-1624">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="95fa9-1624">Az.Resources</span></span>
* <span data-ttu-id="95fa9-1625">Åtgärda felaktiga exempel i referensdokumentationen ”New-AzADAppCredential” och ”New-AzADSpCredential”</span><span class="sxs-lookup"><span data-stu-id="95fa9-1625">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="95fa9-1626">Åtgärda problem där sökvägen för parametern ”-TemplateFile” inte omvandlas innan cmdletarna för distribution i resursgruppen körs</span><span class="sxs-lookup"><span data-stu-id="95fa9-1626">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="95fa9-1627">Az.Resources: Korrigera dokumentationen om standardvärdet för New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="95fa9-1627">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="95fa9-1628">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="95fa9-1628">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="95fa9-1629">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="95fa9-1629">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="95fa9-1630">Åtgärda formateringsproblemet med objektet ”PSResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="95fa9-1630">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="95fa9-1631">Mer information här: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="95fa9-1631">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="95fa9-1632">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="95fa9-1632">Az.ServiceFabric</span></span>
* <span data-ttu-id="95fa9-1633">Återställ när ett certifikat läggs till i en Virtual Machine Scale Sets-modell men ett undantag genereras. Detta har gjorts för att åtgärda följande fel: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="95fa9-1633">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="95fa9-1634">Korrigera några felmeddelanden.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1634">Fix some error messages.</span></span>
* <span data-ttu-id="95fa9-1635">Korrigering av skapande av kluster med ARM-mall som är standard för New-AzServiceFabriCluster som inte fungerade med migrering till Az.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1635">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="95fa9-1636">Korrigering av tilläggning av kluster/programcertifikat så att endast VM Scale Sets som motsvarar klustret läggs till genom att kontrollera ID för klustret i tillägget.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1636">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="95fa9-1637">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="95fa9-1637">Az.SignalR</span></span>
* <span data-ttu-id="95fa9-1638">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="95fa9-1638">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="95fa9-1639">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="95fa9-1639">Az.Sql</span></span>
* <span data-ttu-id="95fa9-1640">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="95fa9-1640">Update incorrect online help URLs</span></span>
* <span data-ttu-id="95fa9-1641">Uppdaterad parameterbeskrivning för LicenseType-parameter med möjliga värden</span><span class="sxs-lookup"><span data-stu-id="95fa9-1641">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="95fa9-1642">Korrigering för att uppdatera hanterad instansidentitet som inte fungerar när det är den enda uppdaterade egenskapen</span><span class="sxs-lookup"><span data-stu-id="95fa9-1642">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="95fa9-1643">Stöd för anpassad sortering på hanterad instans</span><span class="sxs-lookup"><span data-stu-id="95fa9-1643">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="95fa9-1644">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="95fa9-1644">Az.Storage</span></span>
* <span data-ttu-id="95fa9-1645">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="95fa9-1645">Update incorrect online help URLs</span></span>
* <span data-ttu-id="95fa9-1646">Tillhandahåll detaljerat felmeddelande när en användare försöker hämta/konfigurera klassisk loggning/mått på ett Premium Storage-konto eftersom Premium Storage-kontot inte har stöd för klassisk loggning/mått.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1646">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="95fa9-1647">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="95fa9-1647">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="95fa9-1648">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="95fa9-1648">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="95fa9-1649">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="95fa9-1649">Az.TrafficManager</span></span>
* <span data-ttu-id="95fa9-1650">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="95fa9-1650">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="95fa9-1651">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="95fa9-1651">Az.Websites</span></span>
* <span data-ttu-id="95fa9-1652">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="95fa9-1652">Update incorrect online help URLs</span></span>
* <span data-ttu-id="95fa9-1653">Korrigerar ”New-AzWebAppSSLBinding” så att certifikatet laddas upp till rätt resursgrupp och plats om appen finns i en ASE.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1653">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="95fa9-1654">Korrigerar ”New-AzWebAppSSLBinding” så att taggarna inte skrivs över på en bindning av ett SSL-certifikat till en app</span><span class="sxs-lookup"><span data-stu-id="95fa9-1654">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="95fa9-1655">1.1.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="95fa9-1655">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="95fa9-1656">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="95fa9-1656">Az.Accounts</span></span>
* <span data-ttu-id="95fa9-1657">Lade till omfattningen ”Lokal” till Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="95fa9-1657">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="95fa9-1658">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="95fa9-1658">Az.Compute</span></span>
* <span data-ttu-id="95fa9-1659">Namn är nu valfritt i ID-parametern för Restart/Start/Stop/Remove/Set-AzVM och Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="95fa9-1659">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="95fa9-1660">Uppdaterade beskrivningen av ID i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="95fa9-1660">Updated the description of ID in help files</span></span>
* <span data-ttu-id="95fa9-1661">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="95fa9-1661">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="95fa9-1662">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="95fa9-1662">Az.DataLakeStore</span></span>
* <span data-ttu-id="95fa9-1663">Uppdatera sdk-versionen av dataplanet till 1.1.14 för SDK-korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1663">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="95fa9-1664">Korrigerade hanteringen av negativ accesstime och modificationtime för getfilestatus och liststatus; korrigera asynkront annulleringstoken</span><span class="sxs-lookup"><span data-stu-id="95fa9-1664">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="95fa9-1665">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="95fa9-1665">Az.EventGrid</span></span>
* <span data-ttu-id="95fa9-1666">Uppdaterat för användning av API-versionen 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1666">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="95fa9-1667">Uppdaterade följande cmdletar för att stödja nytt scenario i API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="95fa9-1667">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="95fa9-1668">New-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="95fa9-1668">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="95fa9-1669">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="95fa9-1669">Event Time-To-Live,</span></span>
        - <span data-ttu-id="95fa9-1670">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="95fa9-1670">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="95fa9-1671">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1671">Dead letter endpoint.</span></span>
    - <span data-ttu-id="95fa9-1672">Update-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="95fa9-1672">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="95fa9-1673">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="95fa9-1673">Event Time-To-Live,</span></span>
        - <span data-ttu-id="95fa9-1674">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="95fa9-1674">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="95fa9-1675">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1675">Dead letter endpoint.</span></span>
* <span data-ttu-id="95fa9-1676">Lade till nya enum-värden (storageQueue och hybridConnection) för alternativet EndpointType i cmdletarna New-AzureRmEventGridSubscription och Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1676">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="95fa9-1677">Visa varningsmeddelanden om skapande eller uppdatering av händelseprenumerationen förväntas medföra manuell åtgärd från användaren.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1677">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="95fa9-1678">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="95fa9-1678">Az.IotHub</span></span>
* <span data-ttu-id="95fa9-1679">Har uppdaterats till den senaste versionen av SDK:n lotHub</span><span class="sxs-lookup"><span data-stu-id="95fa9-1679">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="95fa9-1680">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="95fa9-1680">Az.LogicApp</span></span>
* <span data-ttu-id="95fa9-1681">Get-AzLogicApp visar en lista över alla som inte har angivet namn</span><span class="sxs-lookup"><span data-stu-id="95fa9-1681">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="95fa9-1682">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="95fa9-1682">Az.Resources</span></span>
* <span data-ttu-id="95fa9-1683">Åtgärdade problem med parameteruppsättningen när parametrarna -ODataQuery och -ResourceId anges för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="95fa9-1683">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="95fa9-1684">Mer information här: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="95fa9-1684">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="95fa9-1685">Åtgärdade hantering av parametern -Custom i New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="95fa9-1685">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="95fa9-1686">Korrigerade stavfel i New-AzDeployment-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="95fa9-1686">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="95fa9-1687">Gjorde parametern -MailNickname obligatorisk för New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="95fa9-1687">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="95fa9-1688">Mer information här: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="95fa9-1688">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="95fa9-1689">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="95fa9-1689">Az.SignalR</span></span>
* <span data-ttu-id="95fa9-1690">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="95fa9-1690">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="95fa9-1691">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="95fa9-1691">Az.Sql</span></span>
* <span data-ttu-id="95fa9-1692">Konverterade lagringshanteringsklientens beroende av den normala SDK-implementeringen.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1692">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="95fa9-1693">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="95fa9-1693">Az.Storage</span></span>
* <span data-ttu-id="95fa9-1694">Angav StorageAccountName för lagringskontext som det verkliga namnet på lagringskontot när det skapas med Sas Token, OAuth eller Anonymous</span><span class="sxs-lookup"><span data-stu-id="95fa9-1694">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="95fa9-1695">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="95fa9-1695">New-AzStorageContext</span></span>
* <span data-ttu-id="95fa9-1696">Skapade Sas Token för Blob Snapshot-objekt med parametern -FullUri, åtgärdade den returnerade URI:n så att den blir URI för ögonblicksbild</span><span class="sxs-lookup"><span data-stu-id="95fa9-1696">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="95fa9-1697">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="95fa9-1697">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="95fa9-1698">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="95fa9-1698">Az.Websites</span></span>
* <span data-ttu-id="95fa9-1699">Åtgärdade en bugg i datumparsningen i Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="95fa9-1699">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="95fa9-1700">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="95fa9-1700">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="95fa9-1701">1.0.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="95fa9-1701">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="95fa9-1702">Allmänt</span><span class="sxs-lookup"><span data-stu-id="95fa9-1702">General</span></span>

- <span data-ttu-id="95fa9-1703">Allmän tillgänglighet för Az-modulen</span><span class="sxs-lookup"><span data-stu-id="95fa9-1703">General Availability of Az Module</span></span>
- <span data-ttu-id="95fa9-1704">Onlinehjälp för varje modul</span><span class="sxs-lookup"><span data-stu-id="95fa9-1704">Online help for each module</span></span>
- <span data-ttu-id="95fa9-1705">Mer information och en översikt finns på [Az-informationssidan](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="95fa9-1705">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="95fa9-1706">Information om hur du migrerar från AzureRM finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="95fa9-1706">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="95fa9-1707">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="95fa9-1707">Az.Accounts</span></span>
- <span data-ttu-id="95fa9-1708">Har ändrats från Az.Profile</span><span class="sxs-lookup"><span data-stu-id="95fa9-1708">Changed from Az.Profile</span></span>
- <span data-ttu-id="95fa9-1709">Fasta tabellformat för profil- och kontexttyper</span><span class="sxs-lookup"><span data-stu-id="95fa9-1709">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="95fa9-1710">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="95fa9-1710">Az.ApiManagement</span></span>
- <span data-ttu-id="95fa9-1711">Korrigeringar för #7002</span><span class="sxs-lookup"><span data-stu-id="95fa9-1711">Fixes for #7002</span></span>
- <span data-ttu-id="95fa9-1712">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="95fa9-1712">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="95fa9-1713">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="95fa9-1713">Az.Batch</span></span>
- <span data-ttu-id="95fa9-1714">Lade till möjligheten att se vilken version av Azure Batch Node Agent som körs på var och en av de virtuella datorerna i en pool, via den nya egenskapen `NodeAgentInformation` på `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1714">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="95fa9-1715">Standarden `Caching` för `PSDataDisk` är nu `ReadWrite` i stället för `None`.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1715">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="95fa9-1716">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="95fa9-1716">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="95fa9-1717">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="95fa9-1717">Az.Billing</span></span>
- <span data-ttu-id="95fa9-1718">Kombinerar cmdletarna för fakturering, förbrukning och UsageAggregates. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="95fa9-1718">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="95fa9-1719">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="95fa9-1719">Az.CognitivServices</span></span>
- <span data-ttu-id="95fa9-1720">Lade till kompletterare för SkuName och Typem som är tillgängliga i New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="95fa9-1720">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="95fa9-1721">Tog bort parameteruppsättningen GetSkusWithAccountParamSetName från Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="95fa9-1721">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="95fa9-1722">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="95fa9-1722">Az.ContainerInstance</span></span>
- <span data-ttu-id="95fa9-1723">Stöd för ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="95fa9-1723">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="95fa9-1724">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="95fa9-1724">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="95fa9-1725">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="95fa9-1725">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="95fa9-1726">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="95fa9-1726">Az.DataLakeStore</span></span>
- <span data-ttu-id="95fa9-1727">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="95fa9-1727">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="95fa9-1728">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="95fa9-1728">Az.Monitor</span></span>
- <span data-ttu-id="95fa9-1729">Döpte om Az.Insights till Az.Monitor och andra mindre icke-bakåtkompatibla ändringar. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="95fa9-1729">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="95fa9-1730">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="95fa9-1730">Az.KeyVault</span></span>
- <span data-ttu-id="95fa9-1731">Tog bort den inaktuella egenskapen PurgeDisabled från utdatatyper</span><span class="sxs-lookup"><span data-stu-id="95fa9-1731">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="95fa9-1732">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="95fa9-1732">Az.MachineLearning</span></span>
- <span data-ttu-id="95fa9-1733">Inkluderade cmdletarna från modulen Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="95fa9-1733">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="95fa9-1734">Az.Media</span><span class="sxs-lookup"><span data-stu-id="95fa9-1734">Az.Media</span></span>
- <span data-ttu-id="95fa9-1735">Tog bort inaktuella -Tags-alias från New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="95fa9-1735">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="95fa9-1736">Az.Network</span><span class="sxs-lookup"><span data-stu-id="95fa9-1736">Az.Network</span></span>
<span data-ttu-id="95fa9-1737">Stöd har lagts till för konfiguration av RewriteRuleSets i Application Gateway</span><span class="sxs-lookup"><span data-stu-id="95fa9-1737">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="95fa9-1738">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="95fa9-1738">New cmdlets added:</span></span>
        - <span data-ttu-id="95fa9-1739">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="95fa9-1739">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="95fa9-1740">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="95fa9-1740">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="95fa9-1741">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="95fa9-1741">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="95fa9-1742">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="95fa9-1742">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="95fa9-1743">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="95fa9-1743">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="95fa9-1744">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="95fa9-1744">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="95fa9-1745">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="95fa9-1745">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="95fa9-1746">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="95fa9-1746">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="95fa9-1747">Cmdletar har uppdaterats med den valfria parametern -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="95fa9-1747">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="95fa9-1748">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="95fa9-1748">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="95fa9-1749">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="95fa9-1749">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="95fa9-1750">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="95fa9-1750">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="95fa9-1751">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="95fa9-1751">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="95fa9-1752">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="95fa9-1752">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="95fa9-1753">New-AzureRmApplicationGatewayUrlPathMapConfig har lagt till KeyVault-stöd för Application Gateway med Identity.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1753">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="95fa9-1754">Cmdletar har uppdaterats med den valfria parametern -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="95fa9-1754">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="95fa9-1755">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="95fa9-1755">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="95fa9-1756">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="95fa9-1756">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="95fa9-1757">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="95fa9-1757">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="95fa9-1758">Cmdleten New-AzApplicationGateway har uppdaterats med den valfria parametern -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="95fa9-1758">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="95fa9-1759">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="95fa9-1759">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="95fa9-1760">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="95fa9-1760">Az.OperationalInsights</span></span>
- <span data-ttu-id="95fa9-1761">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="95fa9-1761">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="95fa9-1762">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="95fa9-1762">Az.Profile</span></span>
- <span data-ttu-id="95fa9-1763">Modulnamnet har ändrats till Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="95fa9-1763">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="95fa9-1764">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="95fa9-1764">Az.RecoveryServices</span></span>
- <span data-ttu-id="95fa9-1765">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="95fa9-1765">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="95fa9-1766">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="95fa9-1766">Az.Resources</span></span>
- <span data-ttu-id="95fa9-1767">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="95fa9-1767">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="95fa9-1768">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="95fa9-1768">Az.ServiceFabric</span></span>
- <span data-ttu-id="95fa9-1769">Stöd för specificering av certifikat efter eget namn och tumavtryck</span><span class="sxs-lookup"><span data-stu-id="95fa9-1769">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="95fa9-1770">Information om fler icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="95fa9-1770">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="95fa9-1771">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="95fa9-1771">Az.SIgnalR</span></span>
- <span data-ttu-id="95fa9-1772">Allmän tillgänglighet för PowerShell-cmdletar för SIgnalR</span><span class="sxs-lookup"><span data-stu-id="95fa9-1772">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="95fa9-1773">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="95fa9-1773">Az.Sql</span></span>
- <span data-ttu-id="95fa9-1774">Lade till de nya identifieringstyperna Data_Exfiltration och Unsafe_Action i Threat Detection-cmdletar</span><span class="sxs-lookup"><span data-stu-id="95fa9-1774">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="95fa9-1775">Uppdaterade dokumentationsexempel för Sql Auditing-cmdletar</span><span class="sxs-lookup"><span data-stu-id="95fa9-1775">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="95fa9-1776">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="95fa9-1776">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="95fa9-1777">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="95fa9-1777">Az.Storage</span></span>
- <span data-ttu-id="95fa9-1778">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="95fa9-1778">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="95fa9-1779">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="95fa9-1779">Az.Websites</span></span>
- <span data-ttu-id="95fa9-1780">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="95fa9-1780">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="95fa9-1781">0.7.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="95fa9-1781">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="95fa9-1782">Allmänt</span><span class="sxs-lookup"><span data-stu-id="95fa9-1782">General</span></span>

* <span data-ttu-id="95fa9-1783">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="95fa9-1783">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="95fa9-1784">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="95fa9-1784">Az.Compute</span></span>

* <span data-ttu-id="95fa9-1785">Lade till stöd för UltraSSD och Galleriavbildningar i de enkla parameteruppsättningarna för `New-AzVm(ss)`-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1785">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="95fa9-1786">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="95fa9-1786">Az.DataLakeStore</span></span>

* <span data-ttu-id="95fa9-1787">Åtgärdade avslutande snedstreck i domänen för adls-konto</span><span class="sxs-lookup"><span data-stu-id="95fa9-1787">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="95fa9-1788">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="95fa9-1788">Az.FrontDoor</span></span>

* <span data-ttu-id="95fa9-1789">Brutna länkar korrigerades</span><span class="sxs-lookup"><span data-stu-id="95fa9-1789">Fixed some broken links</span></span>
    - <span data-ttu-id="95fa9-1790">I artiklarna New-AzureRmFrontDoor och Set-AzureRmFrontDoor artiklar korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1790">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="95fa9-1791">I artikeln New-AzureRmFrontDoorManagedRuleObject korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1791">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="95fa9-1792">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="95fa9-1792">Az.RecoveryServices</span></span>

* <span data-ttu-id="95fa9-1793">Lade till valideringar på klientsidan för Azure-filresurs med återställningsåtgärder.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1793">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="95fa9-1794">Gjorde storageAccountName och storageAccountResourceGroupName valfritt för afs-återställning.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1794">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="95fa9-1795">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="95fa9-1795">Az.Resources</span></span>

* <span data-ttu-id="95fa9-1796">Korrigering för https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="95fa9-1796">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="95fa9-1797">Uppdaterade Get-AzureRmRoleAssignment så att prenumerationsomfattningen används om den anges vid begäran om klassiska administratörer.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1797">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="95fa9-1798">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="95fa9-1798">Az.Sql</span></span>

* <span data-ttu-id="95fa9-1799">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="95fa9-1799">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="95fa9-1800">Korrigerade ett problem med Get-AzureRmSqlDatabaseVulnerabilityAssessment med DotNet-kärna</span><span class="sxs-lookup"><span data-stu-id="95fa9-1800">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="95fa9-1801">Ändrade dokumentationen för hjälpmeddelanden som rör SQL Auditing-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1801">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="95fa9-1802">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="95fa9-1802">Az.Storage</span></span>

* <span data-ttu-id="95fa9-1803">Lade till -EnableHierarchicalNamespace i New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="95fa9-1803">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="95fa9-1804">Åtgärdade problemet med att cmdleten Copy File inte kunde återanvända källkontexten på målet om inte -DestContext angetts</span><span class="sxs-lookup"><span data-stu-id="95fa9-1804">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="95fa9-1805">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="95fa9-1805">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="95fa9-1806">Stöd för statisk webbplatskonfiguration</span><span class="sxs-lookup"><span data-stu-id="95fa9-1806">Support Static Website configuration</span></span>
    - <span data-ttu-id="95fa9-1807">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="95fa9-1807">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="95fa9-1808">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="95fa9-1808">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="95fa9-1809">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="95fa9-1809">Az.Websites</span></span>

* <span data-ttu-id="95fa9-1810">Set-AzureRmWebApp och Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="95fa9-1810">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="95fa9-1811">Ny parameter (-AzureStoragePath) har lagts till för att ange att Azure Storage-sökvägar ska monteras i containerappar i Windows och Linux.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1811">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="95fa9-1812">Använder utdata från den nya cmdleten New-AzureRmWebAppAzureStoragePath som en parameter för att ange sökvägar för Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1812">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="95fa9-1813">0.6.1 – november 2018</span><span class="sxs-lookup"><span data-stu-id="95fa9-1813">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="95fa9-1814">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="95fa9-1814">Az.ApiManagement</span></span>
* <span data-ttu-id="95fa9-1815">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="95fa9-1815">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="95fa9-1816">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="95fa9-1816">Az.Automation</span></span>
* <span data-ttu-id="95fa9-1817">Swagger baserade Azure Automation-cmdletar</span><span class="sxs-lookup"><span data-stu-id="95fa9-1817">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="95fa9-1818">Cmdletar för Uppdateringshantering har lagts till</span><span class="sxs-lookup"><span data-stu-id="95fa9-1818">Added Update Management cmdlets</span></span>
* <span data-ttu-id="95fa9-1819">Cmdletar för källkontroll har lagts till</span><span class="sxs-lookup"><span data-stu-id="95fa9-1819">Added Source Control cmdlets</span></span>
* <span data-ttu-id="95fa9-1820">Remove-AzureRmAutomationHybridWorkerGroup-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="95fa9-1820">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="95fa9-1821">Kommandot för DSC-registreringsnod har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="95fa9-1821">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="95fa9-1822">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="95fa9-1822">Az.Compute</span></span>
* <span data-ttu-id="95fa9-1823">Problem med SystemAssigned-identitet har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="95fa9-1823">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="95fa9-1824">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="95fa9-1824">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="95fa9-1825">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="95fa9-1825">Az.ContainerInstance</span></span>
* <span data-ttu-id="95fa9-1826">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="95fa9-1826">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="95fa9-1827">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="95fa9-1827">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="95fa9-1828">uppdatera exempelbeskrivningen för marketplace-cmdletar</span><span class="sxs-lookup"><span data-stu-id="95fa9-1828">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="95fa9-1829">Az.Network</span><span class="sxs-lookup"><span data-stu-id="95fa9-1829">Az.Network</span></span>
* <span data-ttu-id="95fa9-1830">Cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomErreller Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="95fa9-1830">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="95fa9-1831">ICMP tillbaka till stöd för Azure Firewall-nätverksprotokoll har lagts till</span><span class="sxs-lookup"><span data-stu-id="95fa9-1831">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="95fa9-1832">Uppdatera cmdlet Test-AzureRmNetworkWatcherConnectivity, lägga till verifiering av mål-id, adress och port.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1832">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="95fa9-1833">Åtgärda problem med minnesanvändning i VirtualNetwork-karta</span><span class="sxs-lookup"><span data-stu-id="95fa9-1833">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="95fa9-1834">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="95fa9-1834">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="95fa9-1835">Åtgärda för att ändra principen för en skyddad fildelning.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1835">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="95fa9-1836">Tidszonsprincipen har konverterats till versaler.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1836">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="95fa9-1837">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="95fa9-1837">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="95fa9-1838">Exempel i New-AzureRmRecoveryServicesAsrProtectableItem har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="95fa9-1838">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="95fa9-1839">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="95fa9-1839">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="95fa9-1840">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="95fa9-1840">Az.Relay</span></span>
* <span data-ttu-id="95fa9-1841">Valfri parameter -KeyValue till New-AzureRmRelayKey cmdlet har lagts till, vilket gör det möjligt för användare att tillhandahålla KeyValue.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1841">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="95fa9-1842">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="95fa9-1842">Az.Resources</span></span>
* <span data-ttu-id="95fa9-1843">Uppdatera hjälpdokumentation för resursidentitet kopplad till parametrar i `New-AzureRmPolicyAssignment` och `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="95fa9-1843">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="95fa9-1844">Lägg till ett exempel för New-AzureRmPolicyDefinition som använder -Metadata</span><span class="sxs-lookup"><span data-stu-id="95fa9-1844">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="95fa9-1845">Korrigera så att skiftläge behålls i taggnycklar i NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="95fa9-1845">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="95fa9-1846">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="95fa9-1846">Az.ServiceFabric</span></span>
* <span data-ttu-id="95fa9-1847">Lägg till utfasningsmeddelanden för kommande icke-kompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="95fa9-1847">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="95fa9-1848">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="95fa9-1848">Az.Sql</span></span>
* <span data-ttu-id="95fa9-1849">Nya cmdletar för CRUD-åtgärder på Azure Sql Database-hanterad instans och Azure Sql-hanterad databas</span><span class="sxs-lookup"><span data-stu-id="95fa9-1849">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="95fa9-1850">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="95fa9-1850">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="95fa9-1851">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="95fa9-1851">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="95fa9-1852">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="95fa9-1852">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="95fa9-1853">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="95fa9-1853">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="95fa9-1854">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="95fa9-1854">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="95fa9-1855">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="95fa9-1855">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="95fa9-1856">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="95fa9-1856">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="95fa9-1857">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="95fa9-1857">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="95fa9-1858">Hantering av utökad granskningsprincip på en server eller en databas har aktiverats.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1858">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="95fa9-1859">Ny parameter (PredicateExpression) har lagts till för att aktivera filtrering av granskningsloggar.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1859">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="95fa9-1860">Cmdletar har ändrats så att de använder SQL-klienter i stället för äldre klienter.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1860">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="95fa9-1861">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1861">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="95fa9-1862">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1862">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="95fa9-1863">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1863">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="95fa9-1864">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1864">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="95fa9-1865">Problem med att använda Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings med lagringskontots namnparameter har korrigerats</span><span class="sxs-lookup"><span data-stu-id="95fa9-1865">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="95fa9-1866">0.5.0 – november 2018</span><span class="sxs-lookup"><span data-stu-id="95fa9-1866">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="95fa9-1867">Allmänt</span><span class="sxs-lookup"><span data-stu-id="95fa9-1867">General</span></span>
* <span data-ttu-id="95fa9-1868">Lade till resurskompletterare till många kärn-cmdletar – dessa gör att du kan stega genom befintliga resursnamn med TABB vid interaktiva anrop till cmdletar</span><span class="sxs-lookup"><span data-stu-id="95fa9-1868">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="95fa9-1869">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="95fa9-1869">Az.Profile</span></span>
* <span data-ttu-id="95fa9-1870">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="95fa9-1870">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="95fa9-1871">Bytte namn på parametern TenantId i cmdleten Connect-AzAccount till Tenant och lade till ett alias för TenantId</span><span class="sxs-lookup"><span data-stu-id="95fa9-1871">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="95fa9-1872">Uppdaterade TenantId-beskrivningen för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="95fa9-1872">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="95fa9-1873">Åtgärda felmeddelande för misslyckad inloggning när du tillhandahåller klientdomän</span><span class="sxs-lookup"><span data-stu-id="95fa9-1873">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="95fa9-1874">Åtgärda problem med att kontextnamn hamnar i konflikt för konton utan prenumerationer i klientorganisationen</span><span class="sxs-lookup"><span data-stu-id="95fa9-1874">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="95fa9-1875">Åtgärda problem med DataLake-slutpunkter vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="95fa9-1875">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="95fa9-1876">Åtgärdade problem med att Disconnect-AzAccount kastades om den inte anslöts</span><span class="sxs-lookup"><span data-stu-id="95fa9-1876">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="95fa9-1877">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="95fa9-1877">Az.CognitiveServices</span></span>
* <span data-ttu-id="95fa9-1878">Lade till åtgärden Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1878">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="95fa9-1879">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="95fa9-1879">Az.Compute</span></span>
* <span data-ttu-id="95fa9-1880">Lade till cmdletarna Add-AzVmssVMDataDisk och Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="95fa9-1880">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="95fa9-1881">Get-AzVMImage visar AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="95fa9-1881">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="95fa9-1882">Åtgärdade att värdena för alternativen SetAzVMChefExtension -BootstrapOptions och -JsonAttribute inte angavs i json-format.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1882">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="95fa9-1883">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="95fa9-1883">Az.DataLakeStore</span></span>
* <span data-ttu-id="95fa9-1884">Uppdatera DataLake-paketet till 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1884">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="95fa9-1885">Lägg till standardsamtidighet för flertrådade åtgärder.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1885">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="95fa9-1886">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="95fa9-1886">Az.Insights</span></span>
* <span data-ttu-id="95fa9-1887">Åtgärdade problem #7267 (autoskalningsområde)</span><span class="sxs-lookup"><span data-stu-id="95fa9-1887">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="95fa9-1888">Problem med att uppräknade parametrar inte ställdes in ordentligt när du skapade en ny autoskalningsregel (de ställdes alltid in med standardvärdet).</span><span class="sxs-lookup"><span data-stu-id="95fa9-1888">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="95fa9-1889">Åtgärdade problem #7513 [Insights] Set-AzDiagnosticSetting kräver uttrycklig specifikation av kategorier när inställningar skapas</span><span class="sxs-lookup"><span data-stu-id="95fa9-1889">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="95fa9-1890">Nu kräver inte cmdleten uttrycklig anvisning av kategorierna för att aktiveras under skapande, d.v.s. den fungerar enligt beskrivning</span><span class="sxs-lookup"><span data-stu-id="95fa9-1890">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="95fa9-1891">Az.Network</span><span class="sxs-lookup"><span data-stu-id="95fa9-1891">Az.Network</span></span>
* <span data-ttu-id="95fa9-1892">PeeringType ändrades till en obligatorisk parameter för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="95fa9-1892">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="95fa9-1893">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="95fa9-1893">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="95fa9-1894">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="95fa9-1894">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="95fa9-1895">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="95fa9-1895">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="95fa9-1896">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="95fa9-1896">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="95fa9-1897">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="95fa9-1897">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="95fa9-1898">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="95fa9-1898">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="95fa9-1899">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="95fa9-1899">Az.PolicyInsights</span></span>
* <span data-ttu-id="95fa9-1900">Cmdletar för principreparation har lagts till</span><span class="sxs-lookup"><span data-stu-id="95fa9-1900">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="95fa9-1901">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="95fa9-1901">Az.Resources</span></span>
* <span data-ttu-id="95fa9-1902">Korrigering för https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="95fa9-1902">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="95fa9-1903">Tillåt att resurser listas med parametern -ResourceId för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="95fa9-1903">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="95fa9-1904">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="95fa9-1904">Az.ServiceBus</span></span>
* <span data-ttu-id="95fa9-1905">Skrivskyddad MigrationState-egenskap har lagts till i PSServiceBusMigrationConfigurationAttributes, som hjälper till att hålla koll på migreringstillståndet.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1905">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="95fa9-1906">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="95fa9-1906">Az.ServiceFabric</span></span>
* <span data-ttu-id="95fa9-1907">Åtgärda att lägga till certifikat till Linux-Vmss.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1907">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="95fa9-1908">Åtgärdade Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="95fa9-1908">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="95fa9-1909">Använd rätt tumavtryck från nya certifikat (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="95fa9-1909">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="95fa9-1910">Visa undantag korrekt (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="95fa9-1910">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="95fa9-1911">Åtgärdade Update-AzServiceFabricDurability så att klusterkonfigurationen uppdateras innan Vmss-åtgärden CreateOrUpdate påbörjas.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1911">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="95fa9-1912">0.4.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="95fa9-1912">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="95fa9-1913">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="95fa9-1913">Az.Profile</span></span>
* <span data-ttu-id="95fa9-1914">Åtgärdade problemet med Get-AzSubscription i CloudShell</span><span class="sxs-lookup"><span data-stu-id="95fa9-1914">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="95fa9-1915">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="95fa9-1915">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="95fa9-1916">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="95fa9-1916">Az.Compute</span></span>
* <span data-ttu-id="95fa9-1917">Nya storlekar lades till i listan över godkända VM-storlekar för vilka accelererat nätverk kommer att aktiveras vid användning av den enkla parameteruppsättningen för New-AzVm</span><span class="sxs-lookup"><span data-stu-id="95fa9-1917">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="95fa9-1918">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1918">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="95fa9-1919">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="95fa9-1919">Az.DataLakeStore</span></span>
* <span data-ttu-id="95fa9-1920">Lägger till stöd för regler för virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="95fa9-1920">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="95fa9-1921">Get-AzDataLakeStoreVirtualNetworkRule: Hämtar eller listar regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1921">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="95fa9-1922">Add-AzDataLakeStoreVirtualNetworkRule: Lägger till en regel för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1922">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="95fa9-1923">Set-AzDataLakeStoreVirtualNetworkRule: Ändrar den angivna regeln för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1923">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="95fa9-1924">Remove-AzDataLakeStoreVirtualNetworkRule: Tar bort en regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1924">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="95fa9-1925">Az.Network</span><span class="sxs-lookup"><span data-stu-id="95fa9-1925">Az.Network</span></span>
* <span data-ttu-id="95fa9-1926">Skicka protokollvärdet till serverdelen för att uppdatera cmdleten Test-AzNetworkWatcherConnectivity.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1926">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="95fa9-1927">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1927">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="95fa9-1928">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="95fa9-1928">Az.Resources</span></span>
* <span data-ttu-id="95fa9-1929">Åtgärdade problem där Get-AzRoleDefinition genererar ett oläsligt undantag (när standardprofilen inte innehåller någon prenumeration och ingen omfattning har angetts) genom att lägga till ett beskrivande undantag i scenariot.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1929">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="95fa9-1930">Ställ in ”RoleDefinitionNameParameterSet” som standardparameteruppsättning.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1930">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="95fa9-1931">0.3.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="95fa9-1931">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="95fa9-1932">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="95fa9-1932">Azure.Storage</span></span>
* <span data-ttu-id="95fa9-1933">Åtgärda fel där Kopiera blob/fil inte kopierar metadata när målplatsen har ett problem med metadata</span><span class="sxs-lookup"><span data-stu-id="95fa9-1933">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="95fa9-1934">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="95fa9-1934">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="95fa9-1935">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="95fa9-1935">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="95fa9-1936">Stöd för att hämta användningsinformation om en Storage-resurs för en specifik plats och för att lägga till ett varningsmeddelande för att hämta användningsinformation om en global Storage-resurs är inaktuellt.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1936">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="95fa9-1937">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="95fa9-1937">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="95fa9-1938">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="95fa9-1938">Az.CognitiveServices</span></span>
* <span data-ttu-id="95fa9-1939">Stöd för Get-AzCognitiveServicesAccountSkus utan ett befintligt konto.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1939">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="95fa9-1940">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="95fa9-1940">Az.Compute</span></span>
* <span data-ttu-id="95fa9-1941">Åtgärdade fel där Get-AzVM -ResourceGroupName <rg> returnerar fler än 50 resultat om det behövs</span><span class="sxs-lookup"><span data-stu-id="95fa9-1941">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="95fa9-1942">Lade till ett exempel för SimpleParameterSet i hjälpen för cmdleten New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1942">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="95fa9-1943">Ett stavfel i förloppsmeddelandet för Azure Disk Encryption har korrigerats</span><span class="sxs-lookup"><span data-stu-id="95fa9-1943">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="95fa9-1944">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="95fa9-1944">Az.DataFactoryV2</span></span>
* <span data-ttu-id="95fa9-1945">ADF .Net SDK-versionen har uppdaterats till 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1945">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="95fa9-1946">Az.Network</span><span class="sxs-lookup"><span data-stu-id="95fa9-1946">Az.Network</span></span>
* <span data-ttu-id="95fa9-1947">Funktionalitet för NetworkProfile har lagts till.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1947">Added NetworkProfile functionality.</span></span> <span data-ttu-id="95fa9-1948">nya cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="95fa9-1948">new cmdlets added</span></span>
    - <span data-ttu-id="95fa9-1949">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="95fa9-1949">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="95fa9-1950">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="95fa9-1950">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="95fa9-1951">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="95fa9-1951">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="95fa9-1952">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="95fa9-1952">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="95fa9-1953">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="95fa9-1953">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="95fa9-1954">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="95fa9-1954">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="95fa9-1955">Länk för tjänstassociering på modell för undernät har lagts till</span><span class="sxs-lookup"><span data-stu-id="95fa9-1955">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="95fa9-1956">Cmdletarna New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap och Remove-AzVirtualNetworkTap har lagts till</span><span class="sxs-lookup"><span data-stu-id="95fa9-1956">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="95fa9-1957">Cmdletarna Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig och Remove-AzNEtworkInterfaceTapConfig har lagts till</span><span class="sxs-lookup"><span data-stu-id="95fa9-1957">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="95fa9-1958">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="95fa9-1958">Az.RedisCache</span></span>
* <span data-ttu-id="95fa9-1959">Tillåt att alla strängar används som storleksparametrar framöver.</span><span class="sxs-lookup"><span data-stu-id="95fa9-1959">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="95fa9-1960">Lägg till P5 i popup-fönstret PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="95fa9-1960">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="95fa9-1961">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="95fa9-1961">Az.Resources</span></span>
* <span data-ttu-id="95fa9-1962">Parametern -Mode som saknades i Set-AzPolicyDefinition har lagts till</span><span class="sxs-lookup"><span data-stu-id="95fa9-1962">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="95fa9-1963">Åtgärdade buggen för cmdleten Get-AzProviderOperation för åtgärder med ursprung som innehåller användare</span><span class="sxs-lookup"><span data-stu-id="95fa9-1963">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="95fa9-1964">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="95fa9-1964">Az.Sql</span></span>
* <span data-ttu-id="95fa9-1965">Ett problem där vissa cmdletar för säkerhetskopiering inte kunde identifiera den aktuella azure-prenumerationen har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="95fa9-1965">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="95fa9-1966">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="95fa9-1966">Az.Websites</span></span>
* <span data-ttu-id="95fa9-1967">Ny cmdlet: Get-AzWebAppContainerContinuousDeploymentUrl – Hämtar webhook-URL:en för kontinuerlig distribution av container</span><span class="sxs-lookup"><span data-stu-id="95fa9-1967">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="95fa9-1968">Nya cmdletar: New-AzWebAppContainerPSSession och Enter-WebAppContainerPSSession – Startar en PowerShell-fjärrsession i en containerapp för windows</span><span class="sxs-lookup"><span data-stu-id="95fa9-1968">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="95fa9-1969">0.2.0 – september 2018</span><span class="sxs-lookup"><span data-stu-id="95fa9-1969">0.2.0 - September 2018</span></span>
 <span data-ttu-id="95fa9-1970">Första versionen</span><span class="sxs-lookup"><span data-stu-id="95fa9-1970">Initial Release</span></span>
