---
ms.openlocfilehash: e72aae940b48543d6a99801032186112748ea48b
ms.sourcegitcommit: 6c0d296bfec7c1c35a1d15074ca5eacda6684ea4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/30/2019
ms.locfileid: "68657968"
---
## <a name="250---july-2019"></a><span data-ttu-id="e2d87-101">2.5.0 – July 2019</span><span class="sxs-lookup"><span data-stu-id="e2d87-101">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e2d87-102">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e2d87-102">Az.Accounts</span></span>
* <span data-ttu-id="e2d87-103">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="e2d87-103">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="e2d87-104">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="e2d87-104">Az.ApplicationInsights</span></span>
* <span data-ttu-id="e2d87-105">Korrigera skrivfel i exempel i dokumentationen för Remove-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="e2d87-105">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="e2d87-106">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e2d87-106">Az.Automation</span></span>
* <span data-ttu-id="e2d87-107">Korrigera skrivfel i resurssträng</span><span class="sxs-lookup"><span data-stu-id="e2d87-107">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="e2d87-108">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e2d87-108">Az.CognitiveServices</span></span>
* <span data-ttu-id="e2d87-109">Stöd för NetworkRuleSet har lagts till.</span><span class="sxs-lookup"><span data-stu-id="e2d87-109">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e2d87-110">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e2d87-110">Az.Compute</span></span>
* <span data-ttu-id="e2d87-111">Lägg till saknade egenskaper (ComputerName, OsName, OsVersion och HyperVGeneration) för visningsobjekt i den virtuella datorinstansen.</span><span class="sxs-lookup"><span data-stu-id="e2d87-111">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="e2d87-112">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e2d87-112">Az.ContainerRegistry</span></span>
* <span data-ttu-id="e2d87-113">Åtgärda skrivfel i Remove-AzContainerRegistryReplication för parametern Replication</span><span class="sxs-lookup"><span data-stu-id="e2d87-113">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="e2d87-114">Mer information finns här: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="e2d87-114">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e2d87-115">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e2d87-115">Az.DataFactory</span></span>
* <span data-ttu-id="e2d87-116">ADF .Net SDK-versionen har uppdaterats till 4.1.0</span><span class="sxs-lookup"><span data-stu-id="e2d87-116">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="e2d87-117">Korrigera skrivfel i dokumentationen för Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="e2d87-117">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="e2d87-118">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e2d87-118">Az.EventHub</span></span>
* <span data-ttu-id="e2d87-119">Ny cmmdlet har lagts till för att skapa SAS-token: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="e2d87-119">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="e2d87-120">verifierings- och felmeddelande har lagts till för authorizationrules-rättigheter om endast "hantera" har tilldelats</span><span class="sxs-lookup"><span data-stu-id="e2d87-120">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e2d87-121">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e2d87-121">Az.KeyVault</span></span>
* <span data-ttu-id="e2d87-122">Stöd har lagts till för att ange KeySize för certifikatprinciper</span><span class="sxs-lookup"><span data-stu-id="e2d87-122">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="e2d87-123">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="e2d87-123">Az.LogicApp</span></span>
* <span data-ttu-id="e2d87-124">Korrigering för Get-AzIntegrationAccountMap för att lista alla mappningstyper</span><span class="sxs-lookup"><span data-stu-id="e2d87-124">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="e2d87-125">Ny MapType-parameter har lagts till för filtrering</span><span class="sxs-lookup"><span data-stu-id="e2d87-125">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="e2d87-126">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="e2d87-126">Az.ManagedServices</span></span>
* <span data-ttu-id="e2d87-127">Stöd för API-versionen 2019-06-01 (GA) har lagts till</span><span class="sxs-lookup"><span data-stu-id="e2d87-127">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e2d87-128">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e2d87-128">Az.Network</span></span>
* <span data-ttu-id="e2d87-129">Lägg till stöd för privat slutpunkt och privat länktjänst</span><span class="sxs-lookup"><span data-stu-id="e2d87-129">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="e2d87-130">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="e2d87-130">New cmdlets</span></span>
        - <span data-ttu-id="e2d87-131">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="e2d87-131">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="e2d87-132">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e2d87-132">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="e2d87-133">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e2d87-133">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="e2d87-134">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e2d87-134">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="e2d87-135">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e2d87-135">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="e2d87-136">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e2d87-136">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="e2d87-137">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="e2d87-137">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="e2d87-138">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e2d87-138">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="e2d87-139">Nedanstående kommandon för funktionen har uppdaterats: Flaggan PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies på undernätet i VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e2d87-139">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="e2d87-140">Uppdaterade New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="e2d87-140">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="e2d87-141">Valfri parameter -PrivateEndpointNetworkPoliciesFlag har lagts till för att indikera aktivering eller inaktivering av Tillämpa nätverksprinciper på privat slutpunkt i det här undernätet.</span><span class="sxs-lookup"><span data-stu-id="e2d87-141">Added optional parameter -PrivateEndpointNetworkPoliciesFlag to indicate that enable or disable apply network policies on pivate endpoint in this subnet.</span></span>
        - <span data-ttu-id="e2d87-142">Valfri parameter -PrivateEndpointNetworkPoliciesFlag har lagts till för att indikera aktivering eller inaktivering av Tillämpa nätverksprinciper på privat länktjänst i det här undernätet.</span><span class="sxs-lookup"><span data-stu-id="e2d87-142">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag to indicate that enable or disable apply network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="e2d87-143">AzPrivateLinkService för cmdlet-parametern ServiceName har bytt namn till Name med aliaset ServiceName för bakåtkompatibilitet</span><span class="sxs-lookup"><span data-stu-id="e2d87-143">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="e2d87-144">Aktivera ICMP-protokoll för konfiguration av nätverkssäkerhetsregler</span><span class="sxs-lookup"><span data-stu-id="e2d87-144">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="e2d87-145">Uppdaterade cmdletar</span><span class="sxs-lookup"><span data-stu-id="e2d87-145">Updated cmdlets</span></span>
        - <span data-ttu-id="e2d87-146">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e2d87-146">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="e2d87-147">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e2d87-147">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="e2d87-148">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e2d87-148">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="e2d87-149">Lägg till ConnectionProtocolType (Ikev1/Ikev2) som en konfigurerbar parameter för New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="e2d87-149">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="e2d87-150">Lägg till PrivateIpAddressVersion i LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="e2d87-150">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="e2d87-151">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="e2d87-151">Updated cmdlet:</span></span>
        - <span data-ttu-id="e2d87-152">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="e2d87-152">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="e2d87-153">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="e2d87-153">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="e2d87-154">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="e2d87-154">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="e2d87-155">Uppdatering av Application Gateway-kommandot New-AzApplicationGatewayProbeConfig för stöd av anpassad port i Probe</span><span class="sxs-lookup"><span data-stu-id="e2d87-155">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="e2d87-156">Uppdaterade New-AzApplicationGatewayProbeConfig: Den valfria parametern Port som används för avsökning i serverdelen har lagts till.</span><span class="sxs-lookup"><span data-stu-id="e2d87-156">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="e2d87-157">Denna parameter gäller för SKU:erna Standard_V2 och WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="e2d87-157">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e2d87-158">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e2d87-158">Az.OperationalInsights</span></span>
* <span data-ttu-id="e2d87-159">Uppdaterade standardversionen för sparade sökningar till 1.</span><span class="sxs-lookup"><span data-stu-id="e2d87-159">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="e2d87-160">Åtgärdade hantering av anpassad log null regex</span><span class="sxs-lookup"><span data-stu-id="e2d87-160">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e2d87-161">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e2d87-161">Az.RecoveryServices</span></span>
* <span data-ttu-id="e2d87-162">Uppdatera Get-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="e2d87-162">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="e2d87-163">Uppdatera Get-AzRecoveryServicesBackupContainer.md</span><span class="sxs-lookup"><span data-stu-id="e2d87-163">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="e2d87-164">Uppdatera Get-AzRecoveryServicesVault.md</span><span class="sxs-lookup"><span data-stu-id="e2d87-164">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="e2d87-165">Uppdatera Wait-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="e2d87-165">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="e2d87-166">Uppdatera Set-AzRecoveryServicesVaultContext.md</span><span class="sxs-lookup"><span data-stu-id="e2d87-166">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="e2d87-167">Uppdatera Get-AzRecoveryServicesBackupItem.md</span><span class="sxs-lookup"><span data-stu-id="e2d87-167">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="e2d87-168">Uppdatera Get-AzRecoveryServicesBackupRecoveryPoint.md</span><span class="sxs-lookup"><span data-stu-id="e2d87-168">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="e2d87-169">Uppdatera Restore-AzRecoveryServicesBackupItem.md</span><span class="sxs-lookup"><span data-stu-id="e2d87-169">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="e2d87-170">Uppdaterat tjänstanrop för avregistrering av container för Azure-filresurs</span><span class="sxs-lookup"><span data-stu-id="e2d87-170">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="e2d87-171">Uppdatera Set-AzRecoveryServicesAsrAlertSetting.md</span><span class="sxs-lookup"><span data-stu-id="e2d87-171">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="e2d87-172">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e2d87-172">Az.Resources</span></span>
- <span data-ttu-id="e2d87-173">Ta bort den cmdlet som saknas och som refereras i dokumentationen till New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e2d87-173">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="e2d87-174">Princip-cmdletar har uppdaterats så att de använder den nya API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="e2d87-174">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="e2d87-175">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e2d87-175">Az.ServiceBus</span></span>
* <span data-ttu-id="e2d87-176">Ny cmmdlet har lagts till för att skapa SAS-token: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="e2d87-176">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="e2d87-177">verifierings- och felmeddelande har lagts till för authorizationrules-rättigheter om endast "hantera" har tilldelats</span><span class="sxs-lookup"><span data-stu-id="e2d87-177">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="e2d87-178">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e2d87-178">Az.Sql</span></span>
* <span data-ttu-id="e2d87-179">Åtgärda saknade exempel för Set-AzSqlDatabaseSecondary cmdlet</span><span class="sxs-lookup"><span data-stu-id="e2d87-179">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="e2d87-180">Åtgärda angivna återkommande genomsökningar för bedömning av säkerhetsrisk utan angivna e-postadresser</span><span class="sxs-lookup"><span data-stu-id="e2d87-180">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="e2d87-181">Korrigera ett skrivfel i ett varningsmeddelande.</span><span class="sxs-lookup"><span data-stu-id="e2d87-181">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e2d87-182">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e2d87-182">Az.Storage</span></span>
* <span data-ttu-id="e2d87-183">Uppdatera exempel i referensdokumentationen för Get-AzStorageAccount så att rätt parameternamn används</span><span class="sxs-lookup"><span data-stu-id="e2d87-183">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="e2d87-184">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="e2d87-184">Az.StorageSync</span></span>
* <span data-ttu-id="e2d87-185">Lägger till cmdleten Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="e2d87-185">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="e2d87-186">Åtgärda problem 9551 så att TierFilesOlderThanDays föredras</span><span class="sxs-lookup"><span data-stu-id="e2d87-186">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e2d87-187">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e2d87-187">Az.Websites</span></span>
* <span data-ttu-id="e2d87-188">Åtgärdar ett fel där vissa SiteConfig-egenskaper inte returnerades av Get-AzWebApp och Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e2d87-188">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="e2d87-189">Lägger till en ny platsparameter för Get-AzDeletedWebApp och Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="e2d87-189">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="e2d87-190">Åtgärdar ett fel i kloning av webbapp-platser som använder New-AzWebApp-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="e2d87-190">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="e2d87-191">2.4.0 – juli 2019</span><span class="sxs-lookup"><span data-stu-id="e2d87-191">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e2d87-192">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e2d87-192">Az.Accounts</span></span>
* <span data-ttu-id="e2d87-193">Lägg till stöd för profil-cmdletar</span><span class="sxs-lookup"><span data-stu-id="e2d87-193">Add support for profile cmdlets</span></span>
* <span data-ttu-id="e2d87-194">Lägg till stöd för miljöer och dataplaner i genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="e2d87-194">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="e2d87-195">Åtgärda bugg där fel slutpunkt i vissa fall användes för cmdletar för dataplaner i Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="e2d87-195">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="e2d87-196">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="e2d87-196">Az.Advisor</span></span>
* <span data-ttu-id="e2d87-197">GA-version av Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="e2d87-197">GA release of Az.Advisor</span></span>
* <span data-ttu-id="e2d87-198">Den här modulen ingår nu som en del av `Az`-sammanslagningsmodulen</span><span class="sxs-lookup"><span data-stu-id="e2d87-198">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="e2d87-199">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e2d87-199">Az.ApiManagement</span></span>
* <span data-ttu-id="e2d87-200">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="e2d87-200">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="e2d87-201">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="e2d87-201">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="e2d87-202">Stöd för att fråga prenumerationer efter användare och produkt har lagts till</span><span class="sxs-lookup"><span data-stu-id="e2d87-202">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="e2d87-203">Stöd för att fråga med hjälp av omfång ”/”, ”/apis”, ”/apis/echo-api” har lagts till</span><span class="sxs-lookup"><span data-stu-id="e2d87-203">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="e2d87-204">Korrigering av problem https://github.com/Azure/azure-powershell/issues/9307 och https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="e2d87-204">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="e2d87-205">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="e2d87-205">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="e2d87-206">Stöd för att ange ”ApiVersion” och ”ApiVersionSetId” när API:er importeras har lagts till</span><span class="sxs-lookup"><span data-stu-id="e2d87-206">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e2d87-207">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e2d87-207">Az.Automation</span></span>
* <span data-ttu-id="e2d87-208">Bugg med cmdleten Set-AzAutomationConnectionFieldValue för att hantera strängvärde har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="e2d87-208">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e2d87-209">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e2d87-209">Az.Compute</span></span>
* <span data-ttu-id="e2d87-210">Lägg till parametern HyperVGeneration i New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="e2d87-210">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e2d87-211">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e2d87-211">Az.DataFactory</span></span>
* <span data-ttu-id="e2d87-212">Uppdaterar utdata från ADF-cmdletar som hämtar aktivitetskörningar, hämtar pipelinekörningar och hämtar utlösarkörningar för stöd för Select-Object-pipe.</span><span class="sxs-lookup"><span data-stu-id="e2d87-212">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="e2d87-213">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="e2d87-213">Az.EventGrid</span></span>
* <span data-ttu-id="e2d87-214">Korrigera stavfel i dokumentation om ”New-AzEventGridSubscription”</span><span class="sxs-lookup"><span data-stu-id="e2d87-214">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e2d87-215">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e2d87-215">Az.IotHub</span></span>
* <span data-ttu-id="e2d87-216">Lägg till stöd för att återskapa principnycklar för auktorisering.</span><span class="sxs-lookup"><span data-stu-id="e2d87-216">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e2d87-217">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e2d87-217">Az.Network</span></span>
* <span data-ttu-id="e2d87-218">”RoutingPreference” har lagts till i offentliga IP-taggar</span><span class="sxs-lookup"><span data-stu-id="e2d87-218">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="e2d87-219">Förbättra exempel för referensdokumentation om ”Get-AzNetworkServiceTag”</span><span class="sxs-lookup"><span data-stu-id="e2d87-219">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="e2d87-220">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="e2d87-220">Az.PolicyInsights</span></span>
* <span data-ttu-id="e2d87-221">Åtgärda problem med null-referens i Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="e2d87-221">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="e2d87-222">Mer information här: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="e2d87-222">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e2d87-223">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e2d87-223">Az.OperationalInsights</span></span>
* <span data-ttu-id="e2d87-224">Modellen för CustomLog-datakälla som returneras i Get-AzOperationalInsightsDataSource har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="e2d87-224">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e2d87-225">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e2d87-225">Az.RecoveryServices</span></span>
* <span data-ttu-id="e2d87-226">Kommandot get-policy för IaaSVM:er har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="e2d87-226">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="e2d87-227">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e2d87-227">Az.Resources</span></span>
    - <span data-ttu-id="e2d87-228">Korrigera hjälptext för den översta parametern i Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="e2d87-228">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="e2d87-229">Lägg till växlingsstöd på klientsidan för Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="e2d87-229">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="e2d87-230">Lägg till nya parametrar för Set-AzPolicyAssignment, -PolicyParameters och -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="e2d87-230">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="e2d87-231">En mängd dokument- och exempeluppdateringar för Policy-cmdletar</span><span class="sxs-lookup"><span data-stu-id="e2d87-231">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="e2d87-232">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e2d87-232">Az.ServiceBus</span></span>
* <span data-ttu-id="e2d87-233">Korrigering av problem #4938 – New-AzureRmServiceBusQueue returnerar BadRequest vid konfiguration av MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="e2d87-233">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="e2d87-234">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e2d87-234">Az.Sql</span></span>
* <span data-ttu-id="e2d87-235">Lägg till cmdletar för instansredundansgrupper från förhandsversion till offentlig version</span><span class="sxs-lookup"><span data-stu-id="e2d87-235">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="e2d87-236">Stöd för granskning för Azure SQL Server\Database med nya cmdletar.</span><span class="sxs-lookup"><span data-stu-id="e2d87-236">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="e2d87-237">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="e2d87-237">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="e2d87-238">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="e2d87-238">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="e2d87-239">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="e2d87-239">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="e2d87-240">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="e2d87-240">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="e2d87-241">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="e2d87-241">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="e2d87-242">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="e2d87-242">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="e2d87-243">Ta bort begränsningar för e-post från inställningarna för sårbarhetsbedömning</span><span class="sxs-lookup"><span data-stu-id="e2d87-243">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e2d87-244">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e2d87-244">Az.Storage</span></span>
* <span data-ttu-id="e2d87-245">Ändra två parametrar ”-IndexDocument” och ”-ErrorDocument404Path” från ”krävs” till ”valfri” i cmdlet:</span><span class="sxs-lookup"><span data-stu-id="e2d87-245">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="e2d87-246">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="e2d87-246">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="e2d87-247">Uppdatera hjälpen för Get-AzStorageBlobContent genom att lägga till ett exempel</span><span class="sxs-lookup"><span data-stu-id="e2d87-247">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="e2d87-248">Visa mer felinformation när cmdleten misslyckas med StorageException</span><span class="sxs-lookup"><span data-stu-id="e2d87-248">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="e2d87-249">Stöd för att skapa eller uppdatera lagringskonto med Azure Files AAD DS-autentisering</span><span class="sxs-lookup"><span data-stu-id="e2d87-249">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="e2d87-250">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e2d87-250">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="e2d87-251">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e2d87-251">Set-AzStorageAccount</span></span>
* <span data-ttu-id="e2d87-252">Stöd för att lista eller stänga filreferenser för en filresurs, filkatalog eller en fil</span><span class="sxs-lookup"><span data-stu-id="e2d87-252">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="e2d87-253">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="e2d87-253">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="e2d87-254">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="e2d87-254">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="e2d87-255">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="e2d87-255">Az.StorageSync</span></span>
* <span data-ttu-id="e2d87-256">Den här modulen ingår nu som en del av `Az`-sammanslagningsmodulen</span><span class="sxs-lookup"><span data-stu-id="e2d87-256">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="e2d87-257">2.3.2 – juni 2019</span><span class="sxs-lookup"><span data-stu-id="e2d87-257">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e2d87-258">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e2d87-258">Az.Accounts</span></span>
* <span data-ttu-id="e2d87-259">Åtgärda bugg med felaktiga webbadresser som i vissa fall användes för Functions-anrop</span><span class="sxs-lookup"><span data-stu-id="e2d87-259">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="e2d87-260">Mer information här: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="e2d87-260">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="e2d87-261">Åtgärda problem med alias från AzureRM i Az-cmdletar</span><span class="sxs-lookup"><span data-stu-id="e2d87-261">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="e2d87-262">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="e2d87-262">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="e2d87-263">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="e2d87-263">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e2d87-264">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e2d87-264">Az.Compute</span></span>
* <span data-ttu-id="e2d87-265">Parameteruppsättningarna New-AzVm och New-AzVmss accepterar nu parametern ”ProximityPlacementGroup”.</span><span class="sxs-lookup"><span data-stu-id="e2d87-265">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="e2d87-266">Stavfel i referensdokumentationen för ”New-AzVM” har korrigerats</span><span class="sxs-lookup"><span data-stu-id="e2d87-266">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="e2d87-267">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="e2d87-267">Az.Dns</span></span>
* <span data-ttu-id="e2d87-268">Stavfel i hjälpexempel för ”Set-AzDnsZone” har korrigerats.</span><span class="sxs-lookup"><span data-stu-id="e2d87-268">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="e2d87-269">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="e2d87-269">Az.EventGrid</span></span>
* <span data-ttu-id="e2d87-270">Har uppdaterats för att använda API-versionen 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="e2d87-270">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="e2d87-271">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="e2d87-271">New cmdlets:</span></span>
    - <span data-ttu-id="e2d87-272">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="e2d87-272">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="e2d87-273">Skapar en ny Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="e2d87-273">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="e2d87-274">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="e2d87-274">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="e2d87-275">Hämtar information om en Event Grid-domän eller hämtar en lista med alla Event Grid-domäner i den aktuella Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="e2d87-275">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="e2d87-276">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="e2d87-276">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="e2d87-277">Tar bort en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="e2d87-277">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="e2d87-278">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="e2d87-278">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="e2d87-279">Återskapar nyckeln för delad åtkomst för en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="e2d87-279">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="e2d87-280">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="e2d87-280">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="e2d87-281">Hämtar de nycklar för delad åtkomst som används för att publicera händelser till en Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="e2d87-281">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="e2d87-282">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="e2d87-282">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="e2d87-283">Skapar ett nytt Azure Event Grid-domänämne.</span><span class="sxs-lookup"><span data-stu-id="e2d87-283">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="e2d87-284">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="e2d87-284">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="e2d87-285">Hämtar information om ett Event Grid-domänämne eller hämtar en lista med alla Event Grid-domänämnen under en specifik Event Grid-domän i nuvarande Azure</span><span class="sxs-lookup"><span data-stu-id="e2d87-285">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="e2d87-286">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="e2d87-286">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="e2d87-287">Tar bort ett befintligt Azure Event Grid-domänämne.</span><span class="sxs-lookup"><span data-stu-id="e2d87-287">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="e2d87-288">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="e2d87-288">Updated cmdlets:</span></span>
    - <span data-ttu-id="e2d87-289">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="e2d87-289">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="e2d87-290">Lägg till nya obligatoriska parametrar för att stödja piping för den nya Event Grid-domänen och Event Grid-domänämnet för att göra det möjligt att skapa nya händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="e2d87-290">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="e2d87-291">Lägg till nya obligatoriska parametrar för att ange det nya Event Grid-domännamnet och/eller namnet på Event Grid-domänämnet för att göra det möjligt att skapa nya händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="e2d87-291">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="e2d87-292">Lägg till ny parameteruppsättningar för domäner och domänämnen för att göra det möjligt att återanvända befintliga parametrar (t.ex. EndPointType, SubjectBeginsWith osv).</span><span class="sxs-lookup"><span data-stu-id="e2d87-292">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="e2d87-293">Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="e2d87-293">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="e2d87-294">Förfallodatum för händelseprenumeration</span><span class="sxs-lookup"><span data-stu-id="e2d87-294">Event subscription expiration date,</span></span>
            - <span data-ttu-id="e2d87-295">Avancerade filterparametrar.</span><span class="sxs-lookup"><span data-stu-id="e2d87-295">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="e2d87-296">Lägg till ny uppräkning för servicebusqueue som mål.</span><span class="sxs-lookup"><span data-stu-id="e2d87-296">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="e2d87-297">Tillåt inte användning av ”Alla” i alternativet -IncludedEventType och ersätt det med</span><span class="sxs-lookup"><span data-stu-id="e2d87-297">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="e2d87-298">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="e2d87-298">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="e2d87-299">Lägg till ny valfria parametrar (Top, ODataQuery och NextLink) för att stödja sidnumrering och filtrering av resultat.</span><span class="sxs-lookup"><span data-stu-id="e2d87-299">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="e2d87-300">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="e2d87-300">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="e2d87-301">Lägg till nya obligatoriska parametrar för att stödja piping för en Event Grid-domän och Event Grid-domänämnen för att göra det möjligt att ta bort befintliga händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="e2d87-301">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="e2d87-302">Lägg till nya obligatoriska parametrar för att ange Event Grid-domännamnet och/eller namnet på Event Grid-domänämnet för att göra det möjligt att ta bort befintliga händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="e2d87-302">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="e2d87-303">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="e2d87-303">Az.FrontDoor</span></span>
* <span data-ttu-id="e2d87-304">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="e2d87-304">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="e2d87-305">Lägg till stöd för transformeringar och nytt värde för automatisk komplettering för operatorer (RegEx)</span><span class="sxs-lookup"><span data-stu-id="e2d87-305">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="e2d87-306">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="e2d87-306">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="e2d87-307">Lägg till nya värden för automatisk komplettering</span><span class="sxs-lookup"><span data-stu-id="e2d87-307">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e2d87-308">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e2d87-308">Az.Network</span></span>
* <span data-ttu-id="e2d87-309">Lägg till stöd för resurs för virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="e2d87-309">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="e2d87-310">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="e2d87-310">New cmdlets</span></span>
        - <span data-ttu-id="e2d87-311">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="e2d87-311">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="e2d87-312">Lägg till AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="e2d87-312">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="e2d87-313">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="e2d87-313">New cmdlets</span></span> 
        - <span data-ttu-id="e2d87-314">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="e2d87-314">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="e2d87-315">Lägg till PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e2d87-315">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="e2d87-316">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="e2d87-316">New cmdlets</span></span> 
        - <span data-ttu-id="e2d87-317">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e2d87-317">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="e2d87-318">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e2d87-318">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="e2d87-319">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e2d87-319">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="e2d87-320">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e2d87-320">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="e2d87-321">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e2d87-321">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="e2d87-322">Lägg till PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="e2d87-322">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="e2d87-323">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="e2d87-323">New cmdlets</span></span>
        - <span data-ttu-id="e2d87-324">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="e2d87-324">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="e2d87-325">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="e2d87-325">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="e2d87-326">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="e2d87-326">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="e2d87-327">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="e2d87-327">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="e2d87-328">Nedanstående kommandon för funktionen har uppdaterats: Flaggan UseLocalAzureIpAddress på VpnConnection</span><span class="sxs-lookup"><span data-stu-id="e2d87-328">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="e2d87-329">New-AzVpnConnection har uppdaterats: Den valfria parametern -UseLocalAzureIpAddress har lagts till för att visa att en lokal IP-adress i Azure ska användas som källadress när anslutningen initieras.</span><span class="sxs-lookup"><span data-stu-id="e2d87-329">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="e2d87-330">Set-AzVpnConnection har uppdaterats: Den valfria parametern -UseLocalAzureIpAddress har lagts till för att visa att en lokal IP-adress i Azure ska användas som källadress när anslutningen initieras.</span><span class="sxs-lookup"><span data-stu-id="e2d87-330">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="e2d87-331">Det skrivskyddade fältet PeeredConnections har lagts till i ExpressRoute-peering.</span><span class="sxs-lookup"><span data-stu-id="e2d87-331">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="e2d87-332">Det skrivskyddade fältet GlobalReachEnabled har lagts till i ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="e2d87-332">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="e2d87-333">Ett attribut för icke-bakåtkompatibla ändringar har lagts till för att lyfta fram utfasning av fältet AllowGlobalReach i modellen ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e2d87-333">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="e2d87-334">Problem 8756 har åtgärdats: Fel vid användning av TargetListenerID med AzApplicationGatewayRedirectConfiguration-cmdletar</span><span class="sxs-lookup"><span data-stu-id="e2d87-334">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="e2d87-335">En bugg i New-AzApplicationGatewayPathRuleConfig som gjorde att regeluppsättningen för att återskapa inte kunde anges har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="e2d87-335">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="e2d87-336">Visningen av VirtualNetworkTaps i NetworkInterfaceIpConfiguration har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="e2d87-336">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="e2d87-337">Cortex Get-cmdletar för att visa en lista med alla delar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="e2d87-337">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="e2d87-338">Funktionen för att skapa VirtualHub-referenser för ExpressRouteGateways och VpnGateway har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="e2d87-338">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="e2d87-339">Stöd för tillgänglighetszoner i AzureFirewall och NatGateway har lagts till</span><span class="sxs-lookup"><span data-stu-id="e2d87-339">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="e2d87-340">Cmdleten Get-AzNetworkServiceTag har lagts till</span><span class="sxs-lookup"><span data-stu-id="e2d87-340">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="e2d87-341">Lägg till stöd för flera offentliga IP-adresser för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="e2d87-341">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="e2d87-342">Cmdleten New-AzFirewall har uppdaterats:</span><span class="sxs-lookup"><span data-stu-id="e2d87-342">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="e2d87-343">Parametern -PublicIpAddress som accepterar ett eller flera offentliga IP-adressobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="e2d87-343">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="e2d87-344">Parametern -VirtualNetwork som accepterar ett virtuellt nätverksobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="e2d87-344">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="e2d87-345">Metoderna AddPublicIpAddress och RemovePublicIpAddress har lagts till på brandväggsobjekt – dessa accepterar ett offentligt IP-adressobjekt som indata</span><span class="sxs-lookup"><span data-stu-id="e2d87-345">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="e2d87-346">Inaktuella parametrar -PublicIpName och -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="e2d87-346">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="e2d87-347">Nedanstående kommandon för funktionen har uppdaterats: Ange autentiseringsalternativ för VpnClient AAD till resurser för virtuella nätverksgatewayer.</span><span class="sxs-lookup"><span data-stu-id="e2d87-347">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="e2d87-348">New-AzVirtualNetworkGateway har uppdaterats: De valfria parametrarna AadTenantUri, AadAudienceId och AadIssuerUri för att ange VpnClient AAD-autentiseringsalternativ på en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="e2d87-348">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="e2d87-349">Set-AzVirtualNetworkGateway har uppdaterats: De valfria parametrarna AadTenantUri, AadAudienceId och AadIssuerUri för att ange VpnClient AAD-autentiseringsalternativ på en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="e2d87-349">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="e2d87-350">Set-AzVirtualNetworkGateway har uppdaterats: Den valfria växelparametern RemoveAadAuthentication som tar bort VpnClient AAD-autentiseringsalternativ från en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="e2d87-350">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e2d87-351">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e2d87-351">Az.OperationalInsights</span></span>
* <span data-ttu-id="e2d87-352">Aktivera prisnivån **pergb2018** i kommandot ”New-AzureRmOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="e2d87-352">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="e2d87-353">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e2d87-353">Az.Resources</span></span>
* <span data-ttu-id="e2d87-354">Stöd för ytterligare alternativ för att exportera en mall</span><span class="sxs-lookup"><span data-stu-id="e2d87-354">Support for additional Template Export options</span></span>
    - <span data-ttu-id="e2d87-355">Lägg till parametern ”-SkipResourceNameParameterization” till Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e2d87-355">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="e2d87-356">Lägg till parametern ”-SkipAllParameterization” till Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e2d87-356">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="e2d87-357">Lägg till parametern ”-Resource” till Export-AzResourceGroup för exporterad resursfiltrering</span><span class="sxs-lookup"><span data-stu-id="e2d87-357">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e2d87-358">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e2d87-358">Az.ServiceFabric</span></span>
* <span data-ttu-id="e2d87-359">Åtgärda att fel tumavtryck används vid tilläggning av certifikat i ByExistingKeyVault i vissa fall</span><span class="sxs-lookup"><span data-stu-id="e2d87-359">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="e2d87-360">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e2d87-360">Az.Sql</span></span>
* <span data-ttu-id="e2d87-361">Åtgärda suffix för lagringsslutpunkt i Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="e2d87-361">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="e2d87-362">Åtgärda att aktivering av Advanced Data Security åsidosätter Advanced Threat Protection-princip</span><span class="sxs-lookup"><span data-stu-id="e2d87-362">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="e2d87-363">Nya cmdletar för Management.Sql som gör att kunderna kan lägga till nycklar för transparent datakryptering (TDE) och ange TDE-skydd för hanterade instanser</span><span class="sxs-lookup"><span data-stu-id="e2d87-363">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="e2d87-364">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e2d87-364">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="e2d87-365">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e2d87-365">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="e2d87-366">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e2d87-366">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="e2d87-367">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="e2d87-367">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="e2d87-368">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="e2d87-368">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e2d87-369">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e2d87-369">Az.Storage</span></span>
* <span data-ttu-id="e2d87-370">Stöd för typerna FileStorage och SkuName Premium_ZRS när lagringskonton skapas</span><span class="sxs-lookup"><span data-stu-id="e2d87-370">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="e2d87-371">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e2d87-371">New-AzStorageAccount</span></span>
* <span data-ttu-id="e2d87-372">Beskrivningen av cmdleten för bloboföränderlighet har förtydligats</span><span class="sxs-lookup"><span data-stu-id="e2d87-372">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="e2d87-373">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="e2d87-373">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e2d87-374">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e2d87-374">Az.Websites</span></span>
* <span data-ttu-id="e2d87-375">Optimerar Get-AzWebAppCertificate för att filtrera efter resursgrupp på servern i stället för klienten</span><span class="sxs-lookup"><span data-stu-id="e2d87-375">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="e2d87-376">Lägger till växlingsparametern -UseDisasterRecovery till Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="e2d87-376">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="e2d87-377">2.2.0 – juni 2019</span><span class="sxs-lookup"><span data-stu-id="e2d87-377">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="e2d87-378">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e2d87-378">Az.Cdn</span></span>
* <span data-ttu-id="e2d87-379">Uppdaterade cmdletar för att ge stöd för rulesEngine-funktion baserat på API-version 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="e2d87-379">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e2d87-380">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e2d87-380">Az.Compute</span></span>
* <span data-ttu-id="e2d87-381">Lade till parameter `NoWait` som startar åtgärden och returnerar omedelbart, innan åtgärden har slutförts.</span><span class="sxs-lookup"><span data-stu-id="e2d87-381">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="e2d87-382">Uppdaterade cmdletar:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="e2d87-382">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="e2d87-383">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e2d87-383">Az.EventHub</span></span>
* <span data-ttu-id="e2d87-384">Korrigering för #9231 – Get-AzEventHubNamespace returnerar inga taggar</span><span class="sxs-lookup"><span data-stu-id="e2d87-384">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="e2d87-385">Korrigering för #9230 – Get-AzEventHubNamespace returnerar ResourceGroup istället för ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2d87-385">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e2d87-386">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e2d87-386">Az.Network</span></span>
* <span data-ttu-id="e2d87-387">Uppdatera ResourceId och InputObject för NAT-gateway</span><span class="sxs-lookup"><span data-stu-id="e2d87-387">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="e2d87-388">Lägg till alias för ResourceId och InputObject</span><span class="sxs-lookup"><span data-stu-id="e2d87-388">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="e2d87-389">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="e2d87-389">Az.PolicyInsights</span></span>
* <span data-ttu-id="e2d87-390">Åtgärda Null-referensproblem i Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="e2d87-390">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e2d87-391">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e2d87-391">Az.RecoveryServices</span></span>
* <span data-ttu-id="e2d87-392">Minsta kvarhållning för IaaSVM-policy i dagar ändrat till 7 från 1</span><span class="sxs-lookup"><span data-stu-id="e2d87-392">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="e2d87-393">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e2d87-393">Az.ServiceBus</span></span>
* <span data-ttu-id="e2d87-394">Korrigering för ärende #9182 – Get-AzServiceBusNamespace returnerar ResourceGroup istället för ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2d87-394">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e2d87-395">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e2d87-395">Az.ServiceFabric</span></span>
* <span data-ttu-id="e2d87-396">Åtgärda stavfel i felmeddelandet för Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="e2d87-396">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="e2d87-397">Åtgärda saknat tecken i Service Fabric-kommandorader</span><span class="sxs-lookup"><span data-stu-id="e2d87-397">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="e2d87-398">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e2d87-398">Az.Sql</span></span>
* <span data-ttu-id="e2d87-399">Lägg till parametern DnsZonePartner för New-AzureSqlInstance-cmdlet för att ge stöd för AutoDr för hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="e2d87-399">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="e2d87-400">Avvecklar cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e2d87-400">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="e2d87-401">Döp om cmdletar för hotidentifiering till Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="e2d87-401">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="e2d87-402">Parametrarna New-AzSqlInstance -StorageSizeInGB och -LicenseType är nu valfria.</span><span class="sxs-lookup"><span data-stu-id="e2d87-402">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e2d87-403">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e2d87-403">Az.Websites</span></span>
* <span data-ttu-id="e2d87-404">åtgärdar problemet där användningen av Set-AzWebApp och Set-AzWebAppSlot med -WebApp-egenskap tog bort taggarna</span><span class="sxs-lookup"><span data-stu-id="e2d87-404">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="e2d87-405">2.1.0 – maj 2019</span><span class="sxs-lookup"><span data-stu-id="e2d87-405">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="e2d87-406">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e2d87-406">Az.ApiManagement</span></span>
* <span data-ttu-id="e2d87-407">Skapade nya cmdletar för att hantera diagnostik för global- och API-omfång</span><span class="sxs-lookup"><span data-stu-id="e2d87-407">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="e2d87-408">**Get-AzApiManagementDiagnostic** – Skaffa diagnostik konfigurerad för global- eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="e2d87-408">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="e2d87-409">**New-AzApiManagementDiagnostic** – Skapa ny diagnostik för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="e2d87-409">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="e2d87-410">**New-AzApiManagementHttpMessageDiagnostic** – Skapa diagnostikinställning om vilka rubriker som ska loggas och storleken på brödtextbyte</span><span class="sxs-lookup"><span data-stu-id="e2d87-410">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="e2d87-411">**New-AzApiManagementPipelineDiagnosticSetting** – Skapa diagnostikinställningar för inkommande/utgående HTTP-meddelanden till gatewayen.</span><span class="sxs-lookup"><span data-stu-id="e2d87-411">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="e2d87-412">**New-AzApiManagementSamplingSetting** – Skapa samplinginställningar för begäranden/svar för en diagnostik</span><span class="sxs-lookup"><span data-stu-id="e2d87-412">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="e2d87-413">**Remove-AzApiManagementDiagnostic** – Ta bort en diagnostikenhet för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="e2d87-413">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="e2d87-414">**Set-AzApiManagementDiagnostic** – Uppdatera en diagnostikenhet för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="e2d87-414">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="e2d87-415">Skapade nya cmdletar för hantering av cacheminne i ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="e2d87-415">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="e2d87-416">**Get-AzApiManagementCache** – Hämta information om cacheminnet som anges av identifierare eller alla cacheminnen</span><span class="sxs-lookup"><span data-stu-id="e2d87-416">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="e2d87-417">**New-AzApiManagementCache** – Skapa ett nytt default-cacheminne eller cacheminne i en viss Azure-region</span><span class="sxs-lookup"><span data-stu-id="e2d87-417">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="e2d87-418">**Remove-AzApiManagementCache** – Ta bort ett cacheminne</span><span class="sxs-lookup"><span data-stu-id="e2d87-418">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="e2d87-419">**Remove-AzApiManagementCache** – Ta bort ett cacheminne</span><span class="sxs-lookup"><span data-stu-id="e2d87-419">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="e2d87-420">Skapade nya cmdletar för hantering av API-schema</span><span class="sxs-lookup"><span data-stu-id="e2d87-420">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="e2d87-421">**New-AzApiManagementSchema** – Skapa ett nytt schema för ett API</span><span class="sxs-lookup"><span data-stu-id="e2d87-421">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="e2d87-422">**Get-AzApiManagementSchema** – Hämta de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="e2d87-422">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="e2d87-423">**Remove-AzApiManagementSchema** – Ta bort de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="e2d87-423">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="e2d87-424">**Set-AzApiManagementSchema** – Uppdatera de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="e2d87-424">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="e2d87-425">Skapa ny cmdlet för att generera en användartoken.</span><span class="sxs-lookup"><span data-stu-id="e2d87-425">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="e2d87-426">**New-AzApiManagementUserToken** – Skapa en ny användartoken som enligt standardinställning är giltig i 8 timmar. Token för GIT-användaren kan skapas med den här cmdleten./</span><span class="sxs-lookup"><span data-stu-id="e2d87-426">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="e2d87-427">Skapade en ny cmdlet för att hämta nätverksstatus</span><span class="sxs-lookup"><span data-stu-id="e2d87-427">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="e2d87-428">**Get-AzApiManagementNetworkStatus** – Hämta nätverksstatusanslutningen för resurserna som API Management-tjänsten är beroende av.</span><span class="sxs-lookup"><span data-stu-id="e2d87-428">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="e2d87-429">Det här är användbart när du distribuerar ApiManagement-tjänsten i ett virtuellt nätverk och validerar om något beroende är brutet.</span><span class="sxs-lookup"><span data-stu-id="e2d87-429">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="e2d87-430">Uppdaterade cmdlet **New-AzApiManagement** för att hantera ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="e2d87-430">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="e2d87-431">Lade till stöd för den nya SKU:n Consumption</span><span class="sxs-lookup"><span data-stu-id="e2d87-431">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="e2d87-432">Aktiverade stöd för att slå på flaggan EnableClientCertificate för SKU:n Consumption</span><span class="sxs-lookup"><span data-stu-id="e2d87-432">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="e2d87-433">Den nya cmdleten **New-AzApiManagementSslSetting** gör det möjligt att ställa in TLS/SSL-inställningen på ”Backend” och ”Frontend” (serverdel och klientdel).</span><span class="sxs-lookup"><span data-stu-id="e2d87-433">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="e2d87-434">Det här kan också användas till att konfigurera chiffer som 3DES och ServerProtocols som Http2 för Frontend för en ApiManagement-tjänst.</span><span class="sxs-lookup"><span data-stu-id="e2d87-434">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="e2d87-435">Stöd har lagts till för att konfigurera värdnamnet DeveloperPortal på ApiManagement-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="e2d87-435">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="e2d87-436">Uppdaterade cmdletar **Get-AzApiManagementSsoToken** för att ta PsApiManagement-objekt som indata</span><span class="sxs-lookup"><span data-stu-id="e2d87-436">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="e2d87-437">Uppdaterad cmdleten för att visa infogade felmeddelanden</span><span class="sxs-lookup"><span data-stu-id="e2d87-437">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="e2d87-438">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Felkod: Felmeddelande av typen ValidationError: Ett eller flera fält innehåller felaktiga värden: Felinformation:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="e2d87-438">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="e2d87-439">Uppdaterade cmdlet **Export-AzApiManagementApi** för att exportera API:er i OpenApi 3.0-format</span><span class="sxs-lookup"><span data-stu-id="e2d87-439">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="e2d87-440">Uppdaterade cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="e2d87-440">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="e2d87-441">Importera API från dokumentspecifikationen OpenApi 3.0</span><span class="sxs-lookup"><span data-stu-id="e2d87-441">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="e2d87-442">Om du vill åsidosätta egenskapen PsApiManagementSchema specificerad i ett dokument (Swagger, Wadl, Wsdl, OpenApi).</span><span class="sxs-lookup"><span data-stu-id="e2d87-442">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="e2d87-443">Åsidosätta egenskapen ServiceUrl som specificeras i ett dokument.</span><span class="sxs-lookup"><span data-stu-id="e2d87-443">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="e2d87-444">Uppdaterade cmdlet **Get-AzApiManagementPolicy** för att returnera policy i undantaget format av typen icke-XML med rawxml</span><span class="sxs-lookup"><span data-stu-id="e2d87-444">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="e2d87-445">Uppdaterade cmdlet **Set-AzApiManagementPolicy** för att godkänna policy i undantaget format av typen icke-XML med rawxml och XML undantaget med xml</span><span class="sxs-lookup"><span data-stu-id="e2d87-445">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="e2d87-446">Uppdaterad cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="e2d87-446">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="e2d87-447">Konfigurera API med OpenId auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="e2d87-447">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="e2d87-448">Skapa ett API i ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="e2d87-448">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="e2d87-449">Klona ett API med SourceApiId och SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="e2d87-449">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="e2d87-450">Möjlighet att konfigurera SubscriptionRequired i API-omfattningen.</span><span class="sxs-lookup"><span data-stu-id="e2d87-450">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="e2d87-451">Uppdaterad cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="e2d87-451">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="e2d87-452">Konfigurera API med OpenId auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="e2d87-452">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="e2d87-453">Uppdatera ett API till ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="e2d87-453">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="e2d87-454">Möjlighet att konfigurera SubscriptionRequired i API-omfattningen.</span><span class="sxs-lookup"><span data-stu-id="e2d87-454">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="e2d87-455">Uppdaterad cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="e2d87-455">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="e2d87-456">Klona en befintlig version med hjälp av SourceApiRevision (kopiera taggar, produkter, åtgärder och principer).</span><span class="sxs-lookup"><span data-stu-id="e2d87-456">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="e2d87-457">Den nya revisionen antar ApiId från den överordnade instansen.</span><span class="sxs-lookup"><span data-stu-id="e2d87-457">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="e2d87-458">Tillhandahålla ApiRevisionDescription</span><span class="sxs-lookup"><span data-stu-id="e2d87-458">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="e2d87-459">Åsidosätta ServiceUrl vid kloning av ett API.</span><span class="sxs-lookup"><span data-stu-id="e2d87-459">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="e2d87-460">Uppdaterad cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="e2d87-460">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="e2d87-461">Konfigurera AAD eller AADB2C med en Authority</span><span class="sxs-lookup"><span data-stu-id="e2d87-461">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="e2d87-462">Konfigurera SignupPolicy, SigninPolicy, ProfileEditingPolicy och PasswordResetPolicy</span><span class="sxs-lookup"><span data-stu-id="e2d87-462">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="e2d87-463">Uppdaterad cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="e2d87-463">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="e2d87-464">Kompensera för ny SubscriptonModel med Scope och UserId</span><span class="sxs-lookup"><span data-stu-id="e2d87-464">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="e2d87-465">Kompensera för gammal prenumerationsmodell med ProductId och UserId</span><span class="sxs-lookup"><span data-stu-id="e2d87-465">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="e2d87-466">Lägg till funktion för att aktivera AllowTracing på prenumerationsnivå.</span><span class="sxs-lookup"><span data-stu-id="e2d87-466">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="e2d87-467">Uppdaterad cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="e2d87-467">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="e2d87-468">Kompensera för ny SubscriptonModel med Scope och UserId</span><span class="sxs-lookup"><span data-stu-id="e2d87-468">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="e2d87-469">Kompensera för gammal prenumerationsmodell med ProductId och UserId</span><span class="sxs-lookup"><span data-stu-id="e2d87-469">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="e2d87-470">Lägg till funktion för att aktivera AllowTracing på prenumerationsnivå.</span><span class="sxs-lookup"><span data-stu-id="e2d87-470">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="e2d87-471">Uppdaterade följande cmdletar för att acceptera ResourceId som indata</span><span class="sxs-lookup"><span data-stu-id="e2d87-471">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="e2d87-472">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e2d87-472">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="e2d87-473">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="e2d87-473">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="e2d87-474">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="e2d87-474">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="e2d87-475">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="e2d87-475">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="e2d87-476">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="e2d87-476">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="e2d87-477">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="e2d87-477">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="e2d87-478">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="e2d87-478">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="e2d87-479">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e2d87-479">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="e2d87-480">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="e2d87-480">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="e2d87-481">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="e2d87-481">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="e2d87-482">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="e2d87-482">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="e2d87-483">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="e2d87-483">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e2d87-484">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e2d87-484">Az.Automation</span></span>
* <span data-ttu-id="e2d87-485">Uppdaterade Get-AzAutomationJobOutputRecord för att hantera postvärden av typen JSON och Text.</span><span class="sxs-lookup"><span data-stu-id="e2d87-485">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="e2d87-486">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="e2d87-486">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="e2d87-487">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="e2d87-487">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="e2d87-488">Ändrade beteende för Start-AzAutomationDscCompilationJob till att bara starta jobbet istället för att vänta på slutförandet.</span><span class="sxs-lookup"><span data-stu-id="e2d87-488">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="e2d87-489">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="e2d87-489">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="e2d87-490">Korrigering för Get-AzAutomationDscNode när using -Name returnerar alla noder.</span><span class="sxs-lookup"><span data-stu-id="e2d87-490">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="e2d87-491">Nu returnerar den endast den matchande noden.</span><span class="sxs-lookup"><span data-stu-id="e2d87-491">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e2d87-492">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e2d87-492">Az.Compute</span></span>
* <span data-ttu-id="e2d87-493">Lägg till parametrarna ProtectFromScaleIn och ProtectFromScaleSetAction i cmdleten Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="e2d87-493">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="e2d87-494">Nu är standardinställningen att vimpelparametern New-AzVM använder en tillgänglig plats om USA, östra inte stöds</span><span class="sxs-lookup"><span data-stu-id="e2d87-494">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e2d87-495">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e2d87-495">Az.DataLakeStore</span></span>
* <span data-ttu-id="e2d87-496">Uppdatera ADLS-sdk för att använda httpclient, integrera dataplanstestning med Azure-ramverk</span><span class="sxs-lookup"><span data-stu-id="e2d87-496">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e2d87-497">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e2d87-497">Az.Monitor</span></span>
* <span data-ttu-id="e2d87-498">Korrigera felaktiga parameternamn i hjälpexempel</span><span class="sxs-lookup"><span data-stu-id="e2d87-498">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e2d87-499">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e2d87-499">Az.Network</span></span>
* <span data-ttu-id="e2d87-500">Lägg till flaggan DisableBgpRoutePropagation i utdata för effektiv routningstabell</span><span class="sxs-lookup"><span data-stu-id="e2d87-500">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="e2d87-501">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="e2d87-501">Updated cmdlet:</span></span>
        - <span data-ttu-id="e2d87-502">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="e2d87-502">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="e2d87-503">Åtgärda dubbelstreck i dokumentationen New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="e2d87-503">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="e2d87-504">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e2d87-504">Az.Resources</span></span>
* <span data-ttu-id="e2d87-505">Lägg till ny cmdlet Get-AzureRmDenyAssignment för att hämta tilldelningsnekanden</span><span class="sxs-lookup"><span data-stu-id="e2d87-505">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="e2d87-506">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e2d87-506">Az.Sql</span></span>
* <span data-ttu-id="e2d87-507">Döp om Advanced Threat Protection-cmdletar för Advanced Data Security och aktivera Vulnerability Assessment som standard</span><span class="sxs-lookup"><span data-stu-id="e2d87-507">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="e2d87-508">2.0.0 – maj 2019</span><span class="sxs-lookup"><span data-stu-id="e2d87-508">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e2d87-509">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e2d87-509">Az.Accounts</span></span>
* <span data-ttu-id="e2d87-510">Uppdatera autentiseringsbiblioteket för att åtgärda ADFS-problem med autentisering av användarnamn/lösenord</span><span class="sxs-lookup"><span data-stu-id="e2d87-510">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="e2d87-511">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e2d87-511">Az.CognitiveServices</span></span>
* <span data-ttu-id="e2d87-512">Visa endast Bing-ansvarsfriskrivning för Bing-sökningstjänster.</span><span class="sxs-lookup"><span data-stu-id="e2d87-512">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="e2d87-513">Förbättra felmeddelande när det inte går att skapa konton.</span><span class="sxs-lookup"><span data-stu-id="e2d87-513">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e2d87-514">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e2d87-514">Az.Compute</span></span>
* <span data-ttu-id="e2d87-515">Funktion för närhetsplaceringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="e2d87-515">Proximity placement group feature.</span></span>
    - <span data-ttu-id="e2d87-516">Följande nya cmdletar har lagts till:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="e2d87-516">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="e2d87-517">Den nya parametern ProximityPlacementGroupId har lagts till i följande cmdletar:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="e2d87-517">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="e2d87-518">Parametern StorageAccountType har lagts till i New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="e2d87-518">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="e2d87-519">TargetRegion för New-AzGalleryImageVersion kan innehålla StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="e2d87-519">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="e2d87-520">Växlingsparametern SkipShutdown har lagts till i Stop-AzVM och Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e2d87-520">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="e2d87-521">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="e2d87-521">Breaking changes</span></span>
    - <span data-ttu-id="e2d87-522">Set-AzVMBootDiagnostics har ändrats till Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="e2d87-522">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="e2d87-523">Export-AzLogAnalyticThrottledRequests har ändrats till Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="e2d87-523">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="e2d87-524">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="e2d87-524">Az.DeploymentManager</span></span>
* <span data-ttu-id="e2d87-525">De första allmänt tillgängliga versionerna av cmdletar för Distributionshanteraren i Azure</span><span class="sxs-lookup"><span data-stu-id="e2d87-525">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="e2d87-526">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="e2d87-526">Az.Dns</span></span>
* <span data-ttu-id="e2d87-527">Automatisk delegering av DNS för NameServer</span><span class="sxs-lookup"><span data-stu-id="e2d87-527">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="e2d87-528">Det överordnade zonnamnet kan användas som ytterligare valfri parameter i cmdleten för att skapa DNS-zoner.</span><span class="sxs-lookup"><span data-stu-id="e2d87-528">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="e2d87-529">Lägger till NS-poster för en nyligen skapad underordnad zon i den överordnade zonen.</span><span class="sxs-lookup"><span data-stu-id="e2d87-529">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="e2d87-530">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="e2d87-530">Az.FrontDoor</span></span>
* <span data-ttu-id="e2d87-531">De första allmänt tillgängliga versionerna av cmdletar för Azure FrontDoor</span><span class="sxs-lookup"><span data-stu-id="e2d87-531">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="e2d87-532">Byt namn på WAF-cmdletar så att de omfattar ”Waf”</span><span class="sxs-lookup"><span data-stu-id="e2d87-532">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="e2d87-533">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="e2d87-533">Az.HDInsight</span></span>
* <span data-ttu-id="e2d87-534">Två cmdletar har tagits bort:</span><span class="sxs-lookup"><span data-stu-id="e2d87-534">Removed two cmdlets:</span></span>
    - <span data-ttu-id="e2d87-535">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="e2d87-535">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="e2d87-536">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="e2d87-536">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="e2d87-537">En ny cmdlet har lagts till, Set-AzHDInsightGatewayCredential, som ersätter Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="e2d87-537">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="e2d87-538">Uppdatera cmdleten Get-AzHDInsightJobOutput för att skilja mellan läsarrollen och HDInsight-operatörsrollen:</span><span class="sxs-lookup"><span data-stu-id="e2d87-538">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="e2d87-539">Användare med läsarrollen måste uttryckligen ange parametern ”DefaultStorageAccountKey”, annars uppstår fel.</span><span class="sxs-lookup"><span data-stu-id="e2d87-539">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="e2d87-540">Användare med HDInsight-operatörsrollen påverkas inte.</span><span class="sxs-lookup"><span data-stu-id="e2d87-540">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e2d87-541">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e2d87-541">Az.Monitor</span></span>
* <span data-ttu-id="e2d87-542">Nya cmdletar för SQR API (schemalagd frågeregel)</span><span class="sxs-lookup"><span data-stu-id="e2d87-542">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="e2d87-543">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="e2d87-543">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="e2d87-544">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="e2d87-544">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="e2d87-545">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="e2d87-545">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="e2d87-546">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="e2d87-546">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="e2d87-547">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="e2d87-547">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="e2d87-548">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="e2d87-548">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="e2d87-549">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="e2d87-549">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="e2d87-550">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="e2d87-550">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="e2d87-551">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="e2d87-551">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="e2d87-552">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="e2d87-552">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="e2d87-553">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="e2d87-553">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="e2d87-554">[Mer](https://docs.microsoft.com/en-us/rest/api/monitor/scheduledqueryrules) information om SQR API</span><span class="sxs-lookup"><span data-stu-id="e2d87-554">[More](https://docs.microsoft.com/en-us/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="e2d87-555">Az.Monitor.md har uppdaterats för att omfatta cmdletar för måttbaserade aviseringsregler i GenV2 (inte klassiska)</span><span class="sxs-lookup"><span data-stu-id="e2d87-555">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e2d87-556">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e2d87-556">Az.Network</span></span>
* <span data-ttu-id="e2d87-557">Lägg till stöd för NAT Gateway-resurs</span><span class="sxs-lookup"><span data-stu-id="e2d87-557">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="e2d87-558">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="e2d87-558">New cmdlets</span></span>
        - <span data-ttu-id="e2d87-559">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="e2d87-559">New-AzNatGateway</span></span>
        - <span data-ttu-id="e2d87-560">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="e2d87-560">Get-AzNatGateway</span></span>
        - <span data-ttu-id="e2d87-561">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="e2d87-561">Set-AzNatGateway</span></span>
        - <span data-ttu-id="e2d87-562">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="e2d87-562">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="e2d87-563">Uppdaterade cmdletar</span><span class="sxs-lookup"><span data-stu-id="e2d87-563">Updated cmdlets</span></span>
        - <span data-ttu-id="e2d87-564">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="e2d87-564">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="e2d87-565">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="e2d87-565">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="e2d87-566">Nedanstående kommandon för funktionen har uppdaterats: Ange/ta bort anpassade vägar på Brooklyn Gateway.</span><span class="sxs-lookup"><span data-stu-id="e2d87-566">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="e2d87-567">New-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ställa in adressprefix som anpassade vägar för att ange gateway.</span><span class="sxs-lookup"><span data-stu-id="e2d87-567">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="e2d87-568">Set-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ange adressprefix som anpassade vägar för att ange gateway.</span><span class="sxs-lookup"><span data-stu-id="e2d87-568">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="e2d87-569">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="e2d87-569">Az.PolicyInsights</span></span>
* <span data-ttu-id="e2d87-570">Stöd för att fråga efter information om principutvärdering.</span><span class="sxs-lookup"><span data-stu-id="e2d87-570">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="e2d87-571">Lägg till parametern ”-Expand” för Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="e2d87-571">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="e2d87-572">Stöd för -Expand PolicyEvaluationDetails.</span><span class="sxs-lookup"><span data-stu-id="e2d87-572">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e2d87-573">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e2d87-573">Az.RecoveryServices</span></span>
* <span data-ttu-id="e2d87-574">Stöd för att dela prenumeration mellan Azure och Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="e2d87-574">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="e2d87-575">Markering av kommande icke-bakåtkompatibla ändringar för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="e2d87-575">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="e2d87-576">Korrigering för återställningsplan och åtgärdsplan i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="e2d87-576">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="e2d87-577">Korrigering för mappning av uppdateringsnätverk i Azure Site Recovery för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="e2d87-577">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="e2d87-578">Korrigering för instruktioner för uppdateringsskydd i Azure Site Recovery för Azure till Azure för hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="e2d87-578">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="e2d87-579">Andra mindre korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="e2d87-579">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="e2d87-580">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="e2d87-580">Az.Relay</span></span>
* <span data-ttu-id="e2d87-581">Korrigera stavfel i kundriktade meddelanden</span><span class="sxs-lookup"><span data-stu-id="e2d87-581">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="e2d87-582">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e2d87-582">Az.ServiceBus</span></span>
* <span data-ttu-id="e2d87-583">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="e2d87-583">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e2d87-584">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e2d87-584">Az.Storage</span></span>
* <span data-ttu-id="e2d87-585">Uppgradera till lagringsklientbiblioteket 10.0.1 (namnområdet för alla objekt från detta SDK ändras från ”Microsoft.WindowsAzure.Storage. *till ”Microsoft.Azure.Storage.* ”)</span><span class="sxs-lookup"><span data-stu-id="e2d87-585">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="e2d87-586">Uppgradera till Microsoft.Azure.Management.Storage 11.0.0 för att stödja den nya API-versionen 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="e2d87-586">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="e2d87-587">Standardlagringskontot i Skapa lagringskonto ändras från ”Storage” till ”StorageV2”</span><span class="sxs-lookup"><span data-stu-id="e2d87-587">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="e2d87-588">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e2d87-588">New-AzStorageAccount</span></span>
* <span data-ttu-id="e2d87-589">Ändra lagringskontots cmdlet-utdata Sku.Name för att passa med indata-SkuName genom att lägga till ”-”. Till exempel ändras ”StandardLRS” till ”Standard_LRS”</span><span class="sxs-lookup"><span data-stu-id="e2d87-589">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="e2d87-590">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e2d87-590">New-AzStorageAccount</span></span>
    - <span data-ttu-id="e2d87-591">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e2d87-591">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="e2d87-592">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e2d87-592">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e2d87-593">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e2d87-593">Az.Websites</span></span>
* <span data-ttu-id="e2d87-594">Egenskapen ”typ” konfigureras nu för PSSite-objekt som returneras av Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e2d87-594">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="e2d87-595">Get-AzWebApp\*Metrics och Get-AzAppServicePlanMetrics markeras som inaktuella</span><span class="sxs-lookup"><span data-stu-id="e2d87-595">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="e2d87-596">1.8.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="e2d87-596">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="e2d87-597">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="e2d87-597">Highlights since the last major release</span></span>
* <span data-ttu-id="e2d87-598">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="e2d87-598">General availability of `Az` module</span></span>
* <span data-ttu-id="e2d87-599">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="e2d87-599">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="e2d87-600">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="e2d87-600">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="e2d87-601">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="e2d87-601">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="e2d87-602">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="e2d87-602">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="e2d87-603">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="e2d87-603">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="e2d87-604">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="e2d87-604">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="e2d87-605">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e2d87-605">Az.Accounts</span></span>
* <span data-ttu-id="e2d87-606">Uppdatera Uninstall-AzureRm för att ta bort moduler i Mac på ett korrekt sätt</span><span class="sxs-lookup"><span data-stu-id="e2d87-606">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="e2d87-607">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="e2d87-607">Az.Batch</span></span>
* <span data-ttu-id="e2d87-608">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="e2d87-608">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="e2d87-609">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e2d87-609">Az.Cdn</span></span>
* <span data-ttu-id="e2d87-610">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="e2d87-610">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="e2d87-611">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e2d87-611">Az.CognitiveServices</span></span>
* <span data-ttu-id="e2d87-612">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="e2d87-612">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e2d87-613">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e2d87-613">Az.Compute</span></span>
* <span data-ttu-id="e2d87-614">Åtgärda problem med AEM-installationen om resurs-ID:n för diskar innehåller resourcegroups i gemener i resurs-ID:n</span><span class="sxs-lookup"><span data-stu-id="e2d87-614">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="e2d87-615">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="e2d87-615">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e2d87-616">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="e2d87-616">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e2d87-617">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e2d87-617">Az.DataFactory</span></span>
* <span data-ttu-id="e2d87-618">Lägg till SsisProperties om NodeCount inte är null för hanterad integreringskörning.</span><span class="sxs-lookup"><span data-stu-id="e2d87-618">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e2d87-619">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e2d87-619">Az.DataLakeStore</span></span>
* <span data-ttu-id="e2d87-620">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="e2d87-620">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="e2d87-621">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="e2d87-621">Az.EventGrid</span></span>
* <span data-ttu-id="e2d87-622">Hjälptexten för slutpunkten har uppdaterats för att visa att resurser ska skapas innan cmdletarna för att skapa/uppdatera händelseprenumerationer används.</span><span class="sxs-lookup"><span data-stu-id="e2d87-622">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="e2d87-623">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e2d87-623">Az.EventHub</span></span>
* <span data-ttu-id="e2d87-624">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="e2d87-624">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="e2d87-625">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="e2d87-625">Az.HDInsight</span></span>
* <span data-ttu-id="e2d87-626">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="e2d87-626">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e2d87-627">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e2d87-627">Az.IotHub</span></span>
* <span data-ttu-id="e2d87-628">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="e2d87-628">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e2d87-629">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e2d87-629">Az.KeyVault</span></span>
* <span data-ttu-id="e2d87-630">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="e2d87-630">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e2d87-631">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="e2d87-631">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="e2d87-632">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="e2d87-632">Az.MachineLearning</span></span>
* <span data-ttu-id="e2d87-633">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="e2d87-633">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="e2d87-634">Az.Media</span><span class="sxs-lookup"><span data-stu-id="e2d87-634">Az.Media</span></span>
* <span data-ttu-id="e2d87-635">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="e2d87-635">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e2d87-636">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e2d87-636">Az.Monitor</span></span>
  * <span data-ttu-id="e2d87-637">Nya cmdletar för måttbaserad aviseringsregel i GenV2 (inte klassisk)</span><span class="sxs-lookup"><span data-stu-id="e2d87-637">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="e2d87-638">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="e2d87-638">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="e2d87-639">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="e2d87-639">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="e2d87-640">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="e2d87-640">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="e2d87-641">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="e2d87-641">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="e2d87-642">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="e2d87-642">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="e2d87-643">Monitor SDK har uppdaterats till version 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="e2d87-643">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e2d87-644">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e2d87-644">Az.Network</span></span>
* <span data-ttu-id="e2d87-645">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="e2d87-645">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e2d87-646">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="e2d87-646">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="e2d87-647">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="e2d87-647">Az.NotificationHubs</span></span>
* <span data-ttu-id="e2d87-648">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="e2d87-648">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e2d87-649">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e2d87-649">Az.OperationalInsights</span></span>
* <span data-ttu-id="e2d87-650">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="e2d87-650">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="e2d87-651">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="e2d87-651">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="e2d87-652">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="e2d87-652">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e2d87-653">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e2d87-653">Az.RecoveryServices</span></span>
* <span data-ttu-id="e2d87-654">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="e2d87-654">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e2d87-655">Tabellformatet för SQL i virtuella Azure-datorer har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="e2d87-655">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="e2d87-656">En alternativ metod för att hämta platser i AzureFileShare har lagts till</span><span class="sxs-lookup"><span data-stu-id="e2d87-656">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="e2d87-657">ScheduleRunDays i SchedulePolicy-objekt har uppdaterats enligt tidszon</span><span class="sxs-lookup"><span data-stu-id="e2d87-657">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="e2d87-658">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="e2d87-658">Az.RedisCache</span></span>
* <span data-ttu-id="e2d87-659">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="e2d87-659">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e2d87-660">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e2d87-660">Az.Resources</span></span>
* <span data-ttu-id="e2d87-661">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="e2d87-661">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="e2d87-662">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e2d87-662">Az.Sql</span></span>
* <span data-ttu-id="e2d87-663">Ersätt Monitor SDK-beroende med vanlig kod</span><span class="sxs-lookup"><span data-stu-id="e2d87-663">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="e2d87-664">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="e2d87-664">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e2d87-665">Förbättrad process för klassificering av flera kolumner.</span><span class="sxs-lookup"><span data-stu-id="e2d87-665">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="e2d87-666">Inkludera SKU-egenskaper (SKU-namn, serie, kapacitet) i svaret från Get-AzSqlServerServiceObjective och formatera som tabell som standard.</span><span class="sxs-lookup"><span data-stu-id="e2d87-666">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="e2d87-667">Möjlighet att använda Get-AzSqlServerServiceObjective efter plats utan att behöva en redan befintlig server i regionen.</span><span class="sxs-lookup"><span data-stu-id="e2d87-667">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="e2d87-668">Stöd för tidszonsparametern när hanterade instanser skapas.</span><span class="sxs-lookup"><span data-stu-id="e2d87-668">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="e2d87-669">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="e2d87-669">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e2d87-670">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e2d87-670">Az.Websites</span></span>
* <span data-ttu-id="e2d87-671">åtgärdar Set-AzWebApp och Set-AzWebAppSlot så att de inte tar bort taggar vid körning</span><span class="sxs-lookup"><span data-stu-id="e2d87-671">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="e2d87-672">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="e2d87-672">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e2d87-673">SDK för WebSites har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="e2d87-673">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="e2d87-674">Egenskapen AdminSiteName har tagits bort från PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="e2d87-674">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="e2d87-675">1.7.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="e2d87-675">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="e2d87-676">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="e2d87-676">Highlights since the last major release</span></span>
* <span data-ttu-id="e2d87-677">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="e2d87-677">General availability of `Az` module</span></span>
* <span data-ttu-id="e2d87-678">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="e2d87-678">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="e2d87-679">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="e2d87-679">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="e2d87-680">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="e2d87-680">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="e2d87-681">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="e2d87-681">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="e2d87-682">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="e2d87-682">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="e2d87-683">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="e2d87-683">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="e2d87-684">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e2d87-684">Az.Accounts</span></span>
* <span data-ttu-id="e2d87-685">Add-AzEnvironment och Set-AzEnvironment har uppdaterats för att godkänna parametern AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="e2d87-685">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="e2d87-686">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e2d87-686">Az.AnalysisServices</span></span>
* <span data-ttu-id="e2d87-687">ServiceClient används i cmdletar för dataplan och den ursprungliga autentiseringslogiken har tagits bort</span><span class="sxs-lookup"><span data-stu-id="e2d87-687">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="e2d87-688">Add-AzureASAccount används för omslutning av Connect-AzAccount för att undvika en icke-bakåtkompatibel ändring</span><span class="sxs-lookup"><span data-stu-id="e2d87-688">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e2d87-689">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e2d87-689">Az.Automation</span></span>
* <span data-ttu-id="e2d87-690">Buggen för cmdleten New-AzAutomationSoftwareUpdateConfiguration för inkluderingar har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="e2d87-690">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="e2d87-691">Nu bör parametern IncludedKbNumber och IncludedPackageNameMask fungera.</span><span class="sxs-lookup"><span data-stu-id="e2d87-691">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="e2d87-692">Felkorrigering för dynamiska grupper i uppdateringshanteringen för azure automation</span><span class="sxs-lookup"><span data-stu-id="e2d87-692">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e2d87-693">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e2d87-693">Az.Compute</span></span>
* <span data-ttu-id="e2d87-694">Lägg till parametern HyperVGeneration i New-AzDiskConfig och New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="e2d87-694">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="e2d87-695">Tillåt att virtuella datorer skapas med galleribilder från andra klientorganisationer.</span><span class="sxs-lookup"><span data-stu-id="e2d87-695">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="e2d87-696">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="e2d87-696">Az.ContainerInstance</span></span>
* <span data-ttu-id="e2d87-697">Ett problem har åtgärdats i parametern -Command för New-AzContainerGroup som lade till ett avslutande tomt argument</span><span class="sxs-lookup"><span data-stu-id="e2d87-697">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e2d87-698">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e2d87-698">Az.DataFactory</span></span>
* <span data-ttu-id="e2d87-699">ADF .Net SDK-versionen har uppdaterats till 3.0.2</span><span class="sxs-lookup"><span data-stu-id="e2d87-699">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="e2d87-700">Cmdleten Set-AzDataFactoryV2 har uppdaterats med extra parametrar för inställningar som rör RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="e2d87-700">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e2d87-701">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e2d87-701">Az.Resources</span></span>
* <span data-ttu-id="e2d87-702">Förbättra hanteringen av providrar för Get-AzResource när parametrarna -ResourceId eller -ResourceGroupName, -Name och -ResourceType tillhandahålls</span><span class="sxs-lookup"><span data-stu-id="e2d87-702">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="e2d87-703">Förbättra felhanteringen för ”Test-AzDeployment” och ”Test-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="e2d87-703">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="e2d87-704">Hantera fel utanför distributionsvalideringen och ta med dem i kommandoutdata istället</span><span class="sxs-lookup"><span data-stu-id="e2d87-704">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="e2d87-705">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="e2d87-705">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="e2d87-706">Lägg till växlingsparametern -IgnoreDynamicParameters till en uppsättning av cmdletar för distribution för att hoppa över fråga i skript och jobbscenarier</span><span class="sxs-lookup"><span data-stu-id="e2d87-706">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="e2d87-707">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="e2d87-707">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="e2d87-708">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e2d87-708">Az.Sql</span></span>
* <span data-ttu-id="e2d87-709">Stöd för dataklassificering av databaser.</span><span class="sxs-lookup"><span data-stu-id="e2d87-709">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e2d87-710">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e2d87-710">Az.Storage</span></span>
* <span data-ttu-id="e2d87-711">Rapportera detaljfel när lagringskontext skapas med parametern -UseConnectedAccount, men utan inloggning på Azure-kontot</span><span class="sxs-lookup"><span data-stu-id="e2d87-711">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="e2d87-712">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="e2d87-712">New-AzStorageContext</span></span>
* <span data-ttu-id="e2d87-713">Stöd för att hantera Blob Service-egenskaper för ett angivet lagringskonto med API:et för hanteringsplan</span><span class="sxs-lookup"><span data-stu-id="e2d87-713">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="e2d87-714">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="e2d87-714">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="e2d87-715">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="e2d87-715">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="e2d87-716">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="e2d87-716">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="e2d87-717">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="e2d87-717">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="e2d87-718">Stöd för -AsJob-cmdletar för att ladda upp och ladda ned blobar och filer</span><span class="sxs-lookup"><span data-stu-id="e2d87-718">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="e2d87-719">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="e2d87-719">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="e2d87-720">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="e2d87-720">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="e2d87-721">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="e2d87-721">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="e2d87-722">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="e2d87-722">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="e2d87-723">1.6.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="e2d87-723">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="e2d87-724">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="e2d87-724">Highlights since the last major release</span></span>
* <span data-ttu-id="e2d87-725">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="e2d87-725">General availability of `Az` module</span></span>
* <span data-ttu-id="e2d87-726">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="e2d87-726">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="e2d87-727">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="e2d87-727">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="e2d87-728">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="e2d87-728">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="e2d87-729">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="e2d87-729">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="e2d87-730">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="e2d87-730">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="e2d87-731">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="e2d87-731">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e2d87-732">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e2d87-732">Az.Automation</span></span>
* <span data-ttu-id="e2d87-733">Azure Automation – ändring av uppdateringshantering för stöd för de nya funktionerna:</span><span class="sxs-lookup"><span data-stu-id="e2d87-733">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="e2d87-734">Dynamisk gruppering</span><span class="sxs-lookup"><span data-stu-id="e2d87-734">Dynamic grouping</span></span>
    * <span data-ttu-id="e2d87-735">För-/efterskrift</span><span class="sxs-lookup"><span data-stu-id="e2d87-735">Pre-Post script</span></span>
    * <span data-ttu-id="e2d87-736">Inställning för omstart</span><span class="sxs-lookup"><span data-stu-id="e2d87-736">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e2d87-737">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e2d87-737">Az.Compute</span></span>
* <span data-ttu-id="e2d87-738">Åtgärda problem med sökvägsmatchning i Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="e2d87-738">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="e2d87-739">Uppdatera Compute-klientbibliotek till 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="e2d87-739">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e2d87-740">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e2d87-740">Az.KeyVault</span></span>
* <span data-ttu-id="e2d87-741">Stöd för jokertecken för KeyVault-cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="e2d87-741">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e2d87-742">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e2d87-742">Az.Network</span></span>
* <span data-ttu-id="e2d87-743">Lägg till stöd för Threat Intelligence för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="e2d87-743">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="e2d87-744">Lägg till resurs för brandväggsprincip på översta nivå och anpassade regler för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="e2d87-744">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e2d87-745">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e2d87-745">Az.RecoveryServices</span></span>
* <span data-ttu-id="e2d87-746">SnapshotRetentionInDays har lagts till i Azure-principen för virtuella datorer för stöd av Instant RP</span><span class="sxs-lookup"><span data-stu-id="e2d87-746">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="e2d87-747">Pipe-stöd för avregistrering av container har lagts till</span><span class="sxs-lookup"><span data-stu-id="e2d87-747">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="e2d87-748">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e2d87-748">Az.Resources</span></span>
* <span data-ttu-id="e2d87-749">Uppdatera stöd för jokertecken för Get-AzResource och Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e2d87-749">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="e2d87-750">Uppdatera autentiseringsuppgifter som används vid allmänna anrop till ARM</span><span class="sxs-lookup"><span data-stu-id="e2d87-750">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="e2d87-751">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e2d87-751">Az.Sql</span></span>
* <span data-ttu-id="e2d87-752">Cmdlet-parametern (ExcludeDetectionType) för Hotidentifiering ändrades från DetectionType till sträng[] för att framtidssäkra den när nya DetectionTypes läggs till, och även för att stödja automatisk ifyllning.</span><span class="sxs-lookup"><span data-stu-id="e2d87-752">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e2d87-753">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e2d87-753">Az.Storage</span></span>
* <span data-ttu-id="e2d87-754">Stöd för att hämta/ange/ta bort hanteringsprincip på ett lagringskonto</span><span class="sxs-lookup"><span data-stu-id="e2d87-754">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="e2d87-755">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="e2d87-755">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="e2d87-756">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="e2d87-756">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="e2d87-757">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="e2d87-757">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="e2d87-758">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="e2d87-758">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="e2d87-759">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="e2d87-759">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="e2d87-760">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="e2d87-760">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e2d87-761">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e2d87-761">Az.Websites</span></span>
* <span data-ttu-id="e2d87-762">Åtgärda fel med ARM-mall som avbryter kloning av alla platser med 'New-AzWebApp -IncludeSourceWebAppSlots'</span><span class="sxs-lookup"><span data-stu-id="e2d87-762">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="e2d87-763">1.5.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="e2d87-763">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e2d87-764">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e2d87-764">Az.Accounts</span></span>
* <span data-ttu-id="e2d87-765">Lägg till kommandot Register-AzModule för stöd för AutoRest-genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="e2d87-765">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="e2d87-766">Uppdatera exempel för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="e2d87-766">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e2d87-767">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e2d87-767">Az.Automation</span></span>
* <span data-ttu-id="e2d87-768">Problem med att hämta vissa månadsscheman i flera Azure Automation-cmdletar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="e2d87-768">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="e2d87-769">Åtgärda problem med att Get-AzAutomationDscNode bara returnerar de 20 översta noderna.</span><span class="sxs-lookup"><span data-stu-id="e2d87-769">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="e2d87-770">Nu returneras alla noder</span><span class="sxs-lookup"><span data-stu-id="e2d87-770">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="e2d87-771">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e2d87-771">Az.Cdn</span></span>
* <span data-ttu-id="e2d87-772">Nya Powershell-cmdletar för att aktivera/inaktivera anpassade domän-HTTPS har lagts till och de gamla har gjorts inaktuella</span><span class="sxs-lookup"><span data-stu-id="e2d87-772">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e2d87-773">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e2d87-773">Az.Compute</span></span>
* <span data-ttu-id="e2d87-774">Lägg till stöd för jokertecken för Get-cmdletar</span><span class="sxs-lookup"><span data-stu-id="e2d87-774">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e2d87-775">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e2d87-775">Az.DataFactory</span></span>
* <span data-ttu-id="e2d87-776">ADF .Net SDK-versionen har uppdaterats till 3.0.1</span><span class="sxs-lookup"><span data-stu-id="e2d87-776">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="e2d87-777">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="e2d87-777">Az.LogicApp</span></span>
* <span data-ttu-id="e2d87-778">Åtgärda problemet med att ListWorkflows endast hämtar den första sidan med resultat</span><span class="sxs-lookup"><span data-stu-id="e2d87-778">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e2d87-779">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e2d87-779">Az.Network</span></span>
* <span data-ttu-id="e2d87-780">Lägg till stöd för jokertecken för Network-cmdletar</span><span class="sxs-lookup"><span data-stu-id="e2d87-780">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e2d87-781">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e2d87-781">Az.RecoveryServices</span></span>
* <span data-ttu-id="e2d87-782">Stöd har lagts till för SQL Server i virtuella Azure-datorer</span><span class="sxs-lookup"><span data-stu-id="e2d87-782">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="e2d87-783">SDK-uppdatering</span><span class="sxs-lookup"><span data-stu-id="e2d87-783">SDK Update</span></span>
* <span data-ttu-id="e2d87-784">Get-ProtectableItem-incheckning i VMappContainer har tagits bort</span><span class="sxs-lookup"><span data-stu-id="e2d87-784">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="e2d87-785">Name och ServerName har lagts till som parametrar för Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="e2d87-785">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="e2d87-786">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e2d87-786">Az.Resources</span></span>
* <span data-ttu-id="e2d87-787">Lägg till parametern `-TemplateObject` i cmdletar för distribution</span><span class="sxs-lookup"><span data-stu-id="e2d87-787">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="e2d87-788">Mer information här: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="e2d87-788">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="e2d87-789">Åtgärda problem med piping av resultatet i `Get-AzResource` till `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="e2d87-789">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="e2d87-790">Mer information här: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="e2d87-790">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="e2d87-791">Åtgärda problem med ändring av JSON-datatyp när `Set-AzResource` körs</span><span class="sxs-lookup"><span data-stu-id="e2d87-791">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="e2d87-792">Mer information här: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="e2d87-792">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="e2d87-793">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e2d87-793">Az.Sql</span></span>
* <span data-ttu-id="e2d87-794">AuditingEndpointsCommunicator uppdateras.</span><span class="sxs-lookup"><span data-stu-id="e2d87-794">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="e2d87-795">Åtgärdar beteendet hos ett gränsscenario när nya diagnostikinställningar skapas.</span><span class="sxs-lookup"><span data-stu-id="e2d87-795">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e2d87-796">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e2d87-796">Az.Storage</span></span>
* <span data-ttu-id="e2d87-797">Stöd för BlockBlobStorage när Storage-konto skapas      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e2d87-797">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="e2d87-798">1.4.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="e2d87-798">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="e2d87-799">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e2d87-799">Az.AnalysisServices</span></span>
* <span data-ttu-id="e2d87-800">Inaktuell AddAzureASAccount-cmdlet</span><span class="sxs-lookup"><span data-stu-id="e2d87-800">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e2d87-801">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e2d87-801">Az.Automation</span></span>
* <span data-ttu-id="e2d87-802">Hjälpen för Import-AzAutomationDscNodeConfiguration har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="e2d87-802">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="e2d87-803">Konfigurationsnamnsvalidering har lagts till i cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="e2d87-803">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="e2d87-804">Förbättrad felhantering för cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="e2d87-804">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="e2d87-805">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e2d87-805">Az.CognitiveServices</span></span>
* <span data-ttu-id="e2d87-806">CustomSubdomainName har lagts till som en ny valfri parameter för New-AzCognitiveServicesAccount, som används för att ange underdomän för resursen.</span><span class="sxs-lookup"><span data-stu-id="e2d87-806">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e2d87-807">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e2d87-807">Az.Compute</span></span>
* <span data-ttu-id="e2d87-808">Problemet med ID-parameteruppsättningar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="e2d87-808">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="e2d87-809">Get-AzVMExtension har uppdaterats så att alla installerade tillägg visas om parametern Name inte har angetts</span><span class="sxs-lookup"><span data-stu-id="e2d87-809">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="e2d87-810">Parametrarna Tag och ResourceId har lagts till i cmdleten Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="e2d87-810">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="e2d87-811">Get-AzVmssVM utan instans-ID och med InstanceView kan visa virtuella VMSS-datorer med instansvyn.</span><span class="sxs-lookup"><span data-stu-id="e2d87-811">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e2d87-812">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e2d87-812">Az.DataLakeStore</span></span>
* <span data-ttu-id="e2d87-813">Cmdletar har lagts till för uppräkning och återställning av borttagna objekt i ADL</span><span class="sxs-lookup"><span data-stu-id="e2d87-813">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="e2d87-814">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e2d87-814">Az.EventHub</span></span>
* <span data-ttu-id="e2d87-815">Ny boolesk egenskap SkipEmptyArchives har lagts till i Skip Empty Archives i CaptureDescription-klassen i Eventhub</span><span class="sxs-lookup"><span data-stu-id="e2d87-815">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="e2d87-816">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e2d87-816">Az.KeyVault</span></span>
* <span data-ttu-id="e2d87-817">Taggning i Set-AzKeyVaultSecret har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="e2d87-817">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="e2d87-818">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="e2d87-818">Az.LogicApp</span></span>
* <span data-ttu-id="e2d87-819">Grundläggande SKU har lagts till för Integrationskonton</span><span class="sxs-lookup"><span data-stu-id="e2d87-819">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="e2d87-820">XSLT 2.0, XSLT 3.0 och Flytande mappningstyper har lagts till</span><span class="sxs-lookup"><span data-stu-id="e2d87-820">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="e2d87-821">Nya cmdletar för integrationskontosammansättningar</span><span class="sxs-lookup"><span data-stu-id="e2d87-821">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="e2d87-822">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="e2d87-822">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="e2d87-823">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="e2d87-823">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="e2d87-824">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="e2d87-824">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="e2d87-825">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="e2d87-825">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="e2d87-826">Nya cmdletar för batchkonfiguration för integrationskonto</span><span class="sxs-lookup"><span data-stu-id="e2d87-826">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="e2d87-827">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="e2d87-827">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="e2d87-828">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="e2d87-828">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="e2d87-829">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="e2d87-829">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="e2d87-830">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="e2d87-830">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="e2d87-831">Logic App-SDK har uppdaterats till version 4.1.0</span><span class="sxs-lookup"><span data-stu-id="e2d87-831">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e2d87-832">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e2d87-832">Az.Monitor</span></span>
* <span data-ttu-id="e2d87-833">Hjälpen för Get-AzMetric har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="e2d87-833">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e2d87-834">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e2d87-834">Az.Network</span></span>
* <span data-ttu-id="e2d87-835">Hjälpexempel för Add-AzApplicationGatewayCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="e2d87-835">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e2d87-836">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e2d87-836">Az.OperationalInsights</span></span>
* <span data-ttu-id="e2d87-837">Ytterligare stöd för datakällorna New och Get ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="e2d87-837">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="e2d87-838">Ny ApplicationInsights-typ har lagts till för att ge stöd för ”Get specific” och ”Get all” för ApplicationInsights-datakällor för angiven arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="e2d87-838">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="e2d87-839">Cmdleten New-AzOperationalInsightsApplicationInsightsDataSource har lagts till för att skapa datakälla med angivna parametrar för Application Insights-resurs: subscription Id, resourceGroupName och name.</span><span class="sxs-lookup"><span data-stu-id="e2d87-839">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="e2d87-840">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e2d87-840">Az.Resources</span></span>
* <span data-ttu-id="e2d87-841">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="e2d87-841">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="e2d87-842">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="e2d87-842">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="e2d87-843">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="e2d87-843">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="e2d87-844">Fel som gör att KeyCredentials inte kan skapas upprepade gånger har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="e2d87-844">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="e2d87-845">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e2d87-845">Az.Sql</span></span>
* <span data-ttu-id="e2d87-846">Lägg till stöd för hyperskalanivån för SQL DB</span><span class="sxs-lookup"><span data-stu-id="e2d87-846">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="e2d87-847">Ett fel har åtgärdats där återställningen kunde misslyckas på grund av onödiga inställningsegenskaper i restore-förfrågan</span><span class="sxs-lookup"><span data-stu-id="e2d87-847">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e2d87-848">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e2d87-848">Az.Websites</span></span>
* <span data-ttu-id="e2d87-849">Rätt exempel i Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="e2d87-849">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="e2d87-850">1.3.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="e2d87-850">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e2d87-851">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e2d87-851">Az.Accounts</span></span>
* <span data-ttu-id="e2d87-852">Uppdatera till den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="e2d87-852">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="e2d87-853">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e2d87-853">Az.AnalysisServices</span></span>
<span data-ttu-id="e2d87-854">Allmän tillgänglighet för Az.AnalysisServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="e2d87-854">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e2d87-855">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e2d87-855">Az.Compute</span></span>
* <span data-ttu-id="e2d87-856">AEM-tillägg: Lägg till stöd för UltraSSD-, P60-, P70- och P80-diskar</span><span class="sxs-lookup"><span data-stu-id="e2d87-856">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="e2d87-857">Uppdatera hjälpbeskrivning för Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="e2d87-857">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="e2d87-858">Uppdatera hjälpbeskrivning och exempel för Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="e2d87-858">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e2d87-859">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e2d87-859">Az.RecoveryServices</span></span>
<span data-ttu-id="e2d87-860">Allmän tillgänglighet för Az.RecoveryServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="e2d87-860">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e2d87-861">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e2d87-861">Az.Resources</span></span>
* <span data-ttu-id="e2d87-862">Korrigera taggar för resursgrupper</span><span class="sxs-lookup"><span data-stu-id="e2d87-862">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="e2d87-863">Mer information här: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="e2d87-863">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="e2d87-864">Åtgärda problem där `Get-AzureRmRoleAssignment` inte respekterar -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="e2d87-864">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="e2d87-865">Mer information här: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="e2d87-865">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="e2d87-866">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e2d87-866">Az.Sql</span></span>
* <span data-ttu-id="e2d87-867">Lägga till Get/Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="e2d87-867">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="e2d87-868">Åtgärda problem där ett nullref-undantag uppstår när du kör SQL-cmdletar och inte är inloggad på ett Azure-konto</span><span class="sxs-lookup"><span data-stu-id="e2d87-868">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="e2d87-869">Åtgärda nullref-undantag i Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="e2d87-869">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="e2d87-870">1.2.1 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="e2d87-870">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e2d87-871">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e2d87-871">Az.Accounts</span></span>
* <span data-ttu-id="e2d87-872">Version med rätt version av autentisering</span><span class="sxs-lookup"><span data-stu-id="e2d87-872">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="e2d87-873">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e2d87-873">Az.AnalysisServices</span></span>
* <span data-ttu-id="e2d87-874">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="e2d87-874">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e2d87-875">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e2d87-875">Az.RecoveryServices</span></span>
* <span data-ttu-id="e2d87-876">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="e2d87-876">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="e2d87-877">1.2.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="e2d87-877">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e2d87-878">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e2d87-878">Az.Accounts</span></span>
* <span data-ttu-id="e2d87-879">Lägga till interaktiv autentisering och autentisering med användarnamn/lösenord för endast Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="e2d87-879">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="e2d87-880">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="e2d87-880">Update incorrect online help URLs</span></span>
* <span data-ttu-id="e2d87-881">Lägga till varningsmeddelande i PS Core för Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="e2d87-881">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="e2d87-882">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="e2d87-882">Az.Aks</span></span>
* <span data-ttu-id="e2d87-883">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="e2d87-883">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e2d87-884">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e2d87-884">Az.Automation</span></span>
* <span data-ttu-id="e2d87-885">Stöd för Python 2-runbookflöden har lagts till</span><span class="sxs-lookup"><span data-stu-id="e2d87-885">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="e2d87-886">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="e2d87-886">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="e2d87-887">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e2d87-887">Az.Cdn</span></span>
* <span data-ttu-id="e2d87-888">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="e2d87-888">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e2d87-889">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e2d87-889">Az.Compute</span></span>
* <span data-ttu-id="e2d87-890">Lägga till cmdleten Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="e2d87-890">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="e2d87-891">Lägga till TempDisk-parameter i Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e2d87-891">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="e2d87-892">Korrigera varningsmeddelande för New-AzVM</span><span class="sxs-lookup"><span data-stu-id="e2d87-892">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="e2d87-893">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e2d87-893">Az.ContainerRegistry</span></span>
* <span data-ttu-id="e2d87-894">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="e2d87-894">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e2d87-895">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e2d87-895">Az.DataFactory</span></span>
* <span data-ttu-id="e2d87-896">ADF .Net SDK-versionen har uppdaterats till 3.0.0</span><span class="sxs-lookup"><span data-stu-id="e2d87-896">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e2d87-897">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e2d87-897">Az.DataLakeStore</span></span>
* <span data-ttu-id="e2d87-898">Åtgärda problem med ADLS-slutpunkt vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="e2d87-898">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="e2d87-899">Mer information här: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="e2d87-899">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="e2d87-900">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="e2d87-900">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e2d87-901">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e2d87-901">Az.IotHub</span></span>
* <span data-ttu-id="e2d87-902">Lägga till kodningsformat i cmdleten Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="e2d87-902">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e2d87-903">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e2d87-903">Az.KeyVault</span></span>
* <span data-ttu-id="e2d87-904">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="e2d87-904">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e2d87-905">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e2d87-905">Az.Network</span></span>
* <span data-ttu-id="e2d87-906">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="e2d87-906">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="e2d87-907">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e2d87-907">Az.Resources</span></span>
* <span data-ttu-id="e2d87-908">Åtgärda felaktiga exempel i referensdokumentationen ”New-AzADAppCredential” och ”New-AzADSpCredential”</span><span class="sxs-lookup"><span data-stu-id="e2d87-908">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="e2d87-909">Åtgärda problem där sökvägen för parametern ”-TemplateFile” inte omvandlas innan cmdletarna för distribution i resursgruppen körs</span><span class="sxs-lookup"><span data-stu-id="e2d87-909">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="e2d87-910">Az.Resources: Korrigera dokumentationen om standardvärdet för New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="e2d87-910">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="e2d87-911">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="e2d87-911">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="e2d87-912">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="e2d87-912">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="e2d87-913">Åtgärda formateringsproblemet med objektet ”PSResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="e2d87-913">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="e2d87-914">Mer information här: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="e2d87-914">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e2d87-915">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e2d87-915">Az.ServiceFabric</span></span>
* <span data-ttu-id="e2d87-916">Återställ när ett certifikat läggs till i en Virtual Machine Scale Sets-modell men ett undantag genereras. Detta har gjorts för att åtgärda följande fel: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="e2d87-916">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="e2d87-917">Korrigera några felmeddelanden.</span><span class="sxs-lookup"><span data-stu-id="e2d87-917">Fix some error messages.</span></span>
* <span data-ttu-id="e2d87-918">Korrigering av skapande av kluster med ARM-mall som är standard för New-AzServiceFabriCluster som inte fungerade med migrering till Az.</span><span class="sxs-lookup"><span data-stu-id="e2d87-918">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="e2d87-919">Korrigering av tilläggning av kluster/programcertifikat så att endast VM Scale Sets som motsvarar klustret läggs till genom att kontrollera ID för klustret i tillägget.</span><span class="sxs-lookup"><span data-stu-id="e2d87-919">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="e2d87-920">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="e2d87-920">Az.SignalR</span></span>
* <span data-ttu-id="e2d87-921">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="e2d87-921">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="e2d87-922">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e2d87-922">Az.Sql</span></span>
* <span data-ttu-id="e2d87-923">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="e2d87-923">Update incorrect online help URLs</span></span>
* <span data-ttu-id="e2d87-924">Uppdaterad parameterbeskrivning för LicenseType-parameter med möjliga värden</span><span class="sxs-lookup"><span data-stu-id="e2d87-924">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="e2d87-925">Korrigering för att uppdatera hanterad instansidentitet som inte fungerar när det är den enda uppdaterade egenskapen</span><span class="sxs-lookup"><span data-stu-id="e2d87-925">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="e2d87-926">Stöd för anpassad sortering på hanterad instans</span><span class="sxs-lookup"><span data-stu-id="e2d87-926">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e2d87-927">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e2d87-927">Az.Storage</span></span>
* <span data-ttu-id="e2d87-928">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="e2d87-928">Update incorrect online help URLs</span></span>
* <span data-ttu-id="e2d87-929">Tillhandahåll detaljerat felmeddelande när en användare försöker hämta/konfigurera klassisk loggning/mått på ett Premium Storage-konto eftersom Premium Storage-kontot inte har stöd för klassisk loggning/mått.</span><span class="sxs-lookup"><span data-stu-id="e2d87-929">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="e2d87-930">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="e2d87-930">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="e2d87-931">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="e2d87-931">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="e2d87-932">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="e2d87-932">Az.TrafficManager</span></span>
* <span data-ttu-id="e2d87-933">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="e2d87-933">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e2d87-934">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e2d87-934">Az.Websites</span></span>
* <span data-ttu-id="e2d87-935">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="e2d87-935">Update incorrect online help URLs</span></span>
* <span data-ttu-id="e2d87-936">Korrigerar ”New-AzWebAppSSLBinding” så att certifikatet laddas upp till rätt resursgrupp och plats om appen finns i en ASE.</span><span class="sxs-lookup"><span data-stu-id="e2d87-936">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="e2d87-937">Korrigerar ”New-AzWebAppSSLBinding” så att taggarna inte skrivs över på en bindning av ett SSL-certifikat till en app</span><span class="sxs-lookup"><span data-stu-id="e2d87-937">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="e2d87-938">1.1.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="e2d87-938">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e2d87-939">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e2d87-939">Az.Accounts</span></span>
* <span data-ttu-id="e2d87-940">Lade till omfattningen ”Lokal” till Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="e2d87-940">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e2d87-941">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e2d87-941">Az.Compute</span></span>
* <span data-ttu-id="e2d87-942">Namn är nu valfritt i ID-parametern för Restart/Start/Stop/Remove/Set-AzVM och Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="e2d87-942">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="e2d87-943">Uppdaterade beskrivningen av ID i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="e2d87-943">Updated the description of ID in help files</span></span>
* <span data-ttu-id="e2d87-944">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e2d87-944">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e2d87-945">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e2d87-945">Az.DataLakeStore</span></span>
* <span data-ttu-id="e2d87-946">Uppdatera sdk-versionen av dataplanet till 1.1.14 för SDK-korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="e2d87-946">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="e2d87-947">Korrigerade hanteringen av negativ accesstime och modificationtime för getfilestatus och liststatus; korrigera asynkront annulleringstoken</span><span class="sxs-lookup"><span data-stu-id="e2d87-947">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="e2d87-948">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="e2d87-948">Az.EventGrid</span></span>
* <span data-ttu-id="e2d87-949">Uppdaterat för användning av API-versionen 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="e2d87-949">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="e2d87-950">Uppdaterade följande cmdletar för att stödja nytt scenario i API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="e2d87-950">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="e2d87-951">New-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="e2d87-951">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="e2d87-952">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="e2d87-952">Event Time-To-Live,</span></span>
        - <span data-ttu-id="e2d87-953">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="e2d87-953">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="e2d87-954">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="e2d87-954">Dead letter endpoint.</span></span>
    - <span data-ttu-id="e2d87-955">Update-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="e2d87-955">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="e2d87-956">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="e2d87-956">Event Time-To-Live,</span></span>
        - <span data-ttu-id="e2d87-957">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="e2d87-957">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="e2d87-958">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="e2d87-958">Dead letter endpoint.</span></span>
* <span data-ttu-id="e2d87-959">Lade till nya enum-värden (storageQueue och hybridConnection) för alternativet EndpointType i cmdletarna New-AzureRmEventGridSubscription och Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="e2d87-959">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="e2d87-960">Visa varningsmeddelanden om skapande eller uppdatering av händelseprenumerationen förväntas medföra manuell åtgärd från användaren.</span><span class="sxs-lookup"><span data-stu-id="e2d87-960">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e2d87-961">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e2d87-961">Az.IotHub</span></span>
* <span data-ttu-id="e2d87-962">Har uppdaterats till den senaste versionen av SDK:n lotHub</span><span class="sxs-lookup"><span data-stu-id="e2d87-962">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="e2d87-963">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="e2d87-963">Az.LogicApp</span></span>
* <span data-ttu-id="e2d87-964">Get-AzLogicApp visar en lista över alla som inte har angivet namn</span><span class="sxs-lookup"><span data-stu-id="e2d87-964">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="e2d87-965">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e2d87-965">Az.Resources</span></span>
* <span data-ttu-id="e2d87-966">Åtgärdade problem med parameteruppsättningen när parametrarna -ODataQuery och -ResourceId anges för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="e2d87-966">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="e2d87-967">Mer information här: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="e2d87-967">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="e2d87-968">Åtgärdade hantering av parametern -Custom i New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e2d87-968">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="e2d87-969">Korrigerade stavfel i New-AzDeployment-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="e2d87-969">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="e2d87-970">Gjorde parametern -MailNickname obligatorisk för New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="e2d87-970">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="e2d87-971">Mer information här: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="e2d87-971">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="e2d87-972">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="e2d87-972">Az.SignalR</span></span>
* <span data-ttu-id="e2d87-973">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e2d87-973">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="e2d87-974">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e2d87-974">Az.Sql</span></span>
* <span data-ttu-id="e2d87-975">Konverterade lagringshanteringsklientens beroende av den normala SDK-implementeringen.</span><span class="sxs-lookup"><span data-stu-id="e2d87-975">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e2d87-976">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e2d87-976">Az.Storage</span></span>
* <span data-ttu-id="e2d87-977">Angav StorageAccountName för lagringskontext som det verkliga namnet på lagringskontot när det skapas med Sas Token, OAuth eller Anonymous</span><span class="sxs-lookup"><span data-stu-id="e2d87-977">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="e2d87-978">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="e2d87-978">New-AzStorageContext</span></span>
* <span data-ttu-id="e2d87-979">Skapade Sas Token för Blob Snapshot-objekt med parametern -FullUri, åtgärdade den returnerade URI:n så att den blir URI för ögonblicksbild</span><span class="sxs-lookup"><span data-stu-id="e2d87-979">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="e2d87-980">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="e2d87-980">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e2d87-981">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e2d87-981">Az.Websites</span></span>
* <span data-ttu-id="e2d87-982">Åtgärdade en bugg i datumparsningen i Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="e2d87-982">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="e2d87-983">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e2d87-983">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="e2d87-984">1.0.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="e2d87-984">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="e2d87-985">Allmänt</span><span class="sxs-lookup"><span data-stu-id="e2d87-985">General</span></span>

- <span data-ttu-id="e2d87-986">Allmän tillgänglighet för Az-modulen</span><span class="sxs-lookup"><span data-stu-id="e2d87-986">General Availability of Az Module</span></span>
- <span data-ttu-id="e2d87-987">Onlinehjälp för varje modul</span><span class="sxs-lookup"><span data-stu-id="e2d87-987">Online help for each module</span></span>
- <span data-ttu-id="e2d87-988">Mer information och en översikt finns på [Az-informationssidan](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="e2d87-988">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="e2d87-989">Information om hur du migrerar från AzureRM finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e2d87-989">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="e2d87-990">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e2d87-990">Az.Accounts</span></span>
- <span data-ttu-id="e2d87-991">Har ändrats från Az.Profile</span><span class="sxs-lookup"><span data-stu-id="e2d87-991">Changed from Az.Profile</span></span>
- <span data-ttu-id="e2d87-992">Fasta tabellformat för profil- och kontexttyper</span><span class="sxs-lookup"><span data-stu-id="e2d87-992">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="e2d87-993">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e2d87-993">Az.ApiManagement</span></span>
- <span data-ttu-id="e2d87-994">Korrigeringar för #7002</span><span class="sxs-lookup"><span data-stu-id="e2d87-994">Fixes for #7002</span></span>
- <span data-ttu-id="e2d87-995">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e2d87-995">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="e2d87-996">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="e2d87-996">Az.Batch</span></span>
- <span data-ttu-id="e2d87-997">Lade till möjligheten att se vilken version av Azure Batch Node Agent som körs på var och en av de virtuella datorerna i en pool, via den nya egenskapen `NodeAgentInformation` på `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="e2d87-997">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="e2d87-998">Standarden `Caching` för `PSDataDisk` är nu `ReadWrite` i stället för `None`.</span><span class="sxs-lookup"><span data-stu-id="e2d87-998">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="e2d87-999">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e2d87-999">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="e2d87-1000">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="e2d87-1000">Az.Billing</span></span>
- <span data-ttu-id="e2d87-1001">Kombinerar cmdletarna för fakturering, förbrukning och UsageAggregates. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e2d87-1001">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="e2d87-1002">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="e2d87-1002">Az.CognitivServices</span></span>
- <span data-ttu-id="e2d87-1003">Lade till kompletterare för SkuName och Typem som är tillgängliga i New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="e2d87-1003">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="e2d87-1004">Tog bort parameteruppsättningen GetSkusWithAccountParamSetName från Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="e2d87-1004">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="e2d87-1005">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="e2d87-1005">Az.ContainerInstance</span></span>
- <span data-ttu-id="e2d87-1006">Stöd för ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="e2d87-1006">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="e2d87-1007">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="e2d87-1007">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="e2d87-1008">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e2d87-1008">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="e2d87-1009">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e2d87-1009">Az.DataLakeStore</span></span>
- <span data-ttu-id="e2d87-1010">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e2d87-1010">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="e2d87-1011">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e2d87-1011">Az.Monitor</span></span>
- <span data-ttu-id="e2d87-1012">Döpte om Az.Insights till Az.Monitor och andra mindre icke-bakåtkompatibla ändringar. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e2d87-1012">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="e2d87-1013">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e2d87-1013">Az.KeyVault</span></span>
- <span data-ttu-id="e2d87-1014">Tog bort den inaktuella egenskapen PurgeDisabled från utdatatyper</span><span class="sxs-lookup"><span data-stu-id="e2d87-1014">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="e2d87-1015">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="e2d87-1015">Az.MachineLearning</span></span>
- <span data-ttu-id="e2d87-1016">Inkluderade cmdletarna från modulen Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="e2d87-1016">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="e2d87-1017">Az.Media</span><span class="sxs-lookup"><span data-stu-id="e2d87-1017">Az.Media</span></span>
- <span data-ttu-id="e2d87-1018">Tog bort inaktuella -Tags-alias från New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="e2d87-1018">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="e2d87-1019">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e2d87-1019">Az.Network</span></span>
<span data-ttu-id="e2d87-1020">Stöd har lagts till för konfiguration av RewriteRuleSets i Application Gateway</span><span class="sxs-lookup"><span data-stu-id="e2d87-1020">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="e2d87-1021">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="e2d87-1021">New cmdlets added:</span></span>
        - <span data-ttu-id="e2d87-1022">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e2d87-1022">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e2d87-1023">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e2d87-1023">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e2d87-1024">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e2d87-1024">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e2d87-1025">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e2d87-1025">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e2d87-1026">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e2d87-1026">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e2d87-1027">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="e2d87-1027">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="e2d87-1028">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="e2d87-1028">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="e2d87-1029">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="e2d87-1029">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="e2d87-1030">Cmdletar har uppdaterats med den valfria parametern -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e2d87-1030">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="e2d87-1031">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e2d87-1031">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="e2d87-1032">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e2d87-1032">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="e2d87-1033">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e2d87-1033">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="e2d87-1034">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e2d87-1034">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="e2d87-1035">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e2d87-1035">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="e2d87-1036">New-AzureRmApplicationGatewayUrlPathMapConfig har lagt till KeyVault-stöd för Application Gateway med Identity.</span><span class="sxs-lookup"><span data-stu-id="e2d87-1036">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="e2d87-1037">Cmdletar har uppdaterats med den valfria parametern -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="e2d87-1037">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="e2d87-1038">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e2d87-1038">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="e2d87-1039">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e2d87-1039">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="e2d87-1040">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e2d87-1040">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="e2d87-1041">Cmdleten New-AzApplicationGateway har uppdaterats med den valfria parametern -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="e2d87-1041">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="e2d87-1042">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e2d87-1042">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="e2d87-1043">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e2d87-1043">Az.OperationalInsights</span></span>
- <span data-ttu-id="e2d87-1044">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e2d87-1044">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="e2d87-1045">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="e2d87-1045">Az.Profile</span></span>
- <span data-ttu-id="e2d87-1046">Modulnamnet har ändrats till Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e2d87-1046">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="e2d87-1047">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e2d87-1047">Az.RecoveryServices</span></span>
- <span data-ttu-id="e2d87-1048">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e2d87-1048">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="e2d87-1049">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e2d87-1049">Az.Resources</span></span>
- <span data-ttu-id="e2d87-1050">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e2d87-1050">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="e2d87-1051">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e2d87-1051">Az.ServiceFabric</span></span>
- <span data-ttu-id="e2d87-1052">Stöd för specificering av certifikat efter eget namn och tumavtryck</span><span class="sxs-lookup"><span data-stu-id="e2d87-1052">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="e2d87-1053">Information om fler icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e2d87-1053">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="e2d87-1054">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="e2d87-1054">Az.SIgnalR</span></span>
- <span data-ttu-id="e2d87-1055">Allmän tillgänglighet för PowerShell-cmdletar för SIgnalR</span><span class="sxs-lookup"><span data-stu-id="e2d87-1055">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="e2d87-1056">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e2d87-1056">Az.Sql</span></span>
- <span data-ttu-id="e2d87-1057">Lade till de nya identifieringstyperna Data_Exfiltration och Unsafe_Action i Threat Detection-cmdletar</span><span class="sxs-lookup"><span data-stu-id="e2d87-1057">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="e2d87-1058">Uppdaterade dokumentationsexempel för Sql Auditing-cmdletar</span><span class="sxs-lookup"><span data-stu-id="e2d87-1058">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="e2d87-1059">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e2d87-1059">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="e2d87-1060">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e2d87-1060">Az.Storage</span></span>
- <span data-ttu-id="e2d87-1061">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e2d87-1061">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="e2d87-1062">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e2d87-1062">Az.Websites</span></span>
- <span data-ttu-id="e2d87-1063">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e2d87-1063">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="e2d87-1064">0.7.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="e2d87-1064">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="e2d87-1065">Allmänt</span><span class="sxs-lookup"><span data-stu-id="e2d87-1065">General</span></span>

* <span data-ttu-id="e2d87-1066">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="e2d87-1066">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="e2d87-1067">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e2d87-1067">Az.Compute</span></span>

* <span data-ttu-id="e2d87-1068">Lade till stöd för UltraSSD och Galleriavbildningar i de enkla parameteruppsättningarna för `New-AzVm(ss)`-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="e2d87-1068">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="e2d87-1069">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e2d87-1069">Az.DataLakeStore</span></span>

* <span data-ttu-id="e2d87-1070">Åtgärdade avslutande snedstreck i domänen för adls-konto</span><span class="sxs-lookup"><span data-stu-id="e2d87-1070">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="e2d87-1071">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="e2d87-1071">Az.FrontDoor</span></span>

* <span data-ttu-id="e2d87-1072">Brutna länkar korrigerades</span><span class="sxs-lookup"><span data-stu-id="e2d87-1072">Fixed some broken links</span></span>
    - <span data-ttu-id="e2d87-1073">I artiklarna New-AzureRmFrontDoor och Set-AzureRmFrontDoor artiklar korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="e2d87-1073">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="e2d87-1074">I artikeln New-AzureRmFrontDoorManagedRuleObject korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="e2d87-1074">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="e2d87-1075">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e2d87-1075">Az.RecoveryServices</span></span>

* <span data-ttu-id="e2d87-1076">Lade till valideringar på klientsidan för Azure-filresurs med återställningsåtgärder.</span><span class="sxs-lookup"><span data-stu-id="e2d87-1076">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="e2d87-1077">Gjorde storageAccountName och storageAccountResourceGroupName valfritt för afs-återställning.</span><span class="sxs-lookup"><span data-stu-id="e2d87-1077">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="e2d87-1078">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e2d87-1078">Az.Resources</span></span>

* <span data-ttu-id="e2d87-1079">Korrigering för https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="e2d87-1079">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="e2d87-1080">Uppdaterade Get-AzureRmRoleAssignment så att prenumerationsomfattningen används om den anges vid begäran om klassiska administratörer.</span><span class="sxs-lookup"><span data-stu-id="e2d87-1080">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="e2d87-1081">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e2d87-1081">Az.Sql</span></span>

* <span data-ttu-id="e2d87-1082">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="e2d87-1082">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="e2d87-1083">Korrigerade ett problem med Get-AzureRmSqlDatabaseVulnerabilityAssessment med DotNet-kärna</span><span class="sxs-lookup"><span data-stu-id="e2d87-1083">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="e2d87-1084">Ändrade dokumentationen för hjälpmeddelanden som rör SQL Auditing-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="e2d87-1084">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="e2d87-1085">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e2d87-1085">Az.Storage</span></span>

* <span data-ttu-id="e2d87-1086">Lade till -EnableHierarchicalNamespace i New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e2d87-1086">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="e2d87-1087">Åtgärdade problemet med att cmdleten Copy File inte kunde återanvända källkontexten på målet om inte -DestContext angetts</span><span class="sxs-lookup"><span data-stu-id="e2d87-1087">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="e2d87-1088">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="e2d87-1088">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="e2d87-1089">Stöd för statisk webbplatskonfiguration</span><span class="sxs-lookup"><span data-stu-id="e2d87-1089">Support Static Website configuration</span></span>
    - <span data-ttu-id="e2d87-1090">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="e2d87-1090">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="e2d87-1091">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="e2d87-1091">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="e2d87-1092">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e2d87-1092">Az.Websites</span></span>

* <span data-ttu-id="e2d87-1093">Set-AzureRmWebApp och Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e2d87-1093">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="e2d87-1094">Ny parameter (-AzureStoragePath) har lagts till för att ange att Azure Storage-sökvägar ska monteras i containerappar i Windows och Linux.</span><span class="sxs-lookup"><span data-stu-id="e2d87-1094">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="e2d87-1095">Använder utdata från den nya cmdleten New-AzureRmWebAppAzureStoragePath som en parameter för att ange sökvägar för Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="e2d87-1095">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="e2d87-1096">0.6.1 – november 2018</span><span class="sxs-lookup"><span data-stu-id="e2d87-1096">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="e2d87-1097">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e2d87-1097">Az.ApiManagement</span></span>
* <span data-ttu-id="e2d87-1098">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="e2d87-1098">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="e2d87-1099">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e2d87-1099">Az.Automation</span></span>
* <span data-ttu-id="e2d87-1100">Swagger baserade Azure Automation-cmdletar</span><span class="sxs-lookup"><span data-stu-id="e2d87-1100">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="e2d87-1101">Cmdletar för Uppdateringshantering har lagts till</span><span class="sxs-lookup"><span data-stu-id="e2d87-1101">Added Update Management cmdlets</span></span>
* <span data-ttu-id="e2d87-1102">Cmdletar för källkontroll har lagts till</span><span class="sxs-lookup"><span data-stu-id="e2d87-1102">Added Source Control cmdlets</span></span>
* <span data-ttu-id="e2d87-1103">Remove-AzureRmAutomationHybridWorkerGroup-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="e2d87-1103">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="e2d87-1104">Kommandot för DSC-registreringsnod har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="e2d87-1104">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="e2d87-1105">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e2d87-1105">Az.Compute</span></span>
* <span data-ttu-id="e2d87-1106">Problem med SystemAssigned-identitet har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="e2d87-1106">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="e2d87-1107">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="e2d87-1107">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="e2d87-1108">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="e2d87-1108">Az.ContainerInstance</span></span>
* <span data-ttu-id="e2d87-1109">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="e2d87-1109">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="e2d87-1110">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="e2d87-1110">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="e2d87-1111">uppdatera exempelbeskrivningen för marketplace-cmdletar</span><span class="sxs-lookup"><span data-stu-id="e2d87-1111">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="e2d87-1112">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e2d87-1112">Az.Network</span></span>
* <span data-ttu-id="e2d87-1113">Cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomErreller Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="e2d87-1113">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="e2d87-1114">ICMP tillbaka till stöd för Azure Firewall-nätverksprotokoll har lagts till</span><span class="sxs-lookup"><span data-stu-id="e2d87-1114">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="e2d87-1115">Uppdatera cmdlet Test-AzureRmNetworkWatcherConnectivity, lägga till verifiering av mål-id, adress och port.</span><span class="sxs-lookup"><span data-stu-id="e2d87-1115">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="e2d87-1116">Åtgärda problem med minnesanvändning i VirtualNetwork-karta</span><span class="sxs-lookup"><span data-stu-id="e2d87-1116">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="e2d87-1117">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="e2d87-1117">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="e2d87-1118">Åtgärda för att ändra principen för en skyddad fildelning.</span><span class="sxs-lookup"><span data-stu-id="e2d87-1118">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="e2d87-1119">Tidszonsprincipen har konverterats till versaler.</span><span class="sxs-lookup"><span data-stu-id="e2d87-1119">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="e2d87-1120">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="e2d87-1120">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="e2d87-1121">Exempel i New-AzureRmRecoveryServicesAsrProtectableItem har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="e2d87-1121">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="e2d87-1122">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="e2d87-1122">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="e2d87-1123">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="e2d87-1123">Az.Relay</span></span>
* <span data-ttu-id="e2d87-1124">Valfri parameter -KeyValue till New-AzureRmRelayKey cmdlet har lagts till, vilket gör det möjligt för användare att tillhandahålla KeyValue.</span><span class="sxs-lookup"><span data-stu-id="e2d87-1124">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="e2d87-1125">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e2d87-1125">Az.Resources</span></span>
* <span data-ttu-id="e2d87-1126">Uppdatera hjälpdokumentation för resursidentitet kopplad till parametrar i `New-AzureRmPolicyAssignment` och `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="e2d87-1126">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="e2d87-1127">Lägg till ett exempel för New-AzureRmPolicyDefinition som använder -Metadata</span><span class="sxs-lookup"><span data-stu-id="e2d87-1127">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="e2d87-1128">Korrigera så att skiftläge behålls i taggnycklar i NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="e2d87-1128">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="e2d87-1129">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e2d87-1129">Az.ServiceFabric</span></span>
* <span data-ttu-id="e2d87-1130">Lägg till utfasningsmeddelanden för kommande icke-kompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="e2d87-1130">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="e2d87-1131">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e2d87-1131">Az.Sql</span></span>
* <span data-ttu-id="e2d87-1132">Nya cmdletar för CRUD-åtgärder på Azure Sql Database-hanterad instans och Azure Sql-hanterad databas</span><span class="sxs-lookup"><span data-stu-id="e2d87-1132">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="e2d87-1133">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="e2d87-1133">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="e2d87-1134">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="e2d87-1134">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="e2d87-1135">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="e2d87-1135">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="e2d87-1136">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="e2d87-1136">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="e2d87-1137">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="e2d87-1137">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="e2d87-1138">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="e2d87-1138">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="e2d87-1139">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="e2d87-1139">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="e2d87-1140">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="e2d87-1140">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="e2d87-1141">Hantering av utökad granskningsprincip på en server eller en databas har aktiverats.</span><span class="sxs-lookup"><span data-stu-id="e2d87-1141">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="e2d87-1142">Ny parameter (PredicateExpression) har lagts till för att aktivera filtrering av granskningsloggar.</span><span class="sxs-lookup"><span data-stu-id="e2d87-1142">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="e2d87-1143">Cmdletar har ändrats så att de använder SQL-klienter i stället för äldre klienter.</span><span class="sxs-lookup"><span data-stu-id="e2d87-1143">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="e2d87-1144">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="e2d87-1144">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="e2d87-1145">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="e2d87-1145">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="e2d87-1146">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="e2d87-1146">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="e2d87-1147">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="e2d87-1147">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="e2d87-1148">Problem med att använda Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings med lagringskontots namnparameter har korrigerats</span><span class="sxs-lookup"><span data-stu-id="e2d87-1148">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="e2d87-1149">0.5.0 – november 2018</span><span class="sxs-lookup"><span data-stu-id="e2d87-1149">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="e2d87-1150">Allmänt</span><span class="sxs-lookup"><span data-stu-id="e2d87-1150">General</span></span>
* <span data-ttu-id="e2d87-1151">Lade till resurskompletterare till många kärn-cmdletar – dessa gör att du kan stega genom befintliga resursnamn med TABB vid interaktiva anrop till cmdletar</span><span class="sxs-lookup"><span data-stu-id="e2d87-1151">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="e2d87-1152">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="e2d87-1152">Az.Profile</span></span>
* <span data-ttu-id="e2d87-1153">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="e2d87-1153">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="e2d87-1154">Bytte namn på parametern TenantId i cmdleten Connect-AzAccount till Tenant och lade till ett alias för TenantId</span><span class="sxs-lookup"><span data-stu-id="e2d87-1154">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="e2d87-1155">Uppdaterade TenantId-beskrivningen för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="e2d87-1155">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="e2d87-1156">Åtgärda felmeddelande för misslyckad inloggning när du tillhandahåller klientdomän</span><span class="sxs-lookup"><span data-stu-id="e2d87-1156">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="e2d87-1157">Åtgärda problem med att kontextnamn hamnar i konflikt för konton utan prenumerationer i klientorganisationen</span><span class="sxs-lookup"><span data-stu-id="e2d87-1157">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="e2d87-1158">Åtgärda problem med DataLake-slutpunkter vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="e2d87-1158">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="e2d87-1159">Åtgärdade problem med att Disconnect-AzAccount kastades om den inte anslöts</span><span class="sxs-lookup"><span data-stu-id="e2d87-1159">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="e2d87-1160">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e2d87-1160">Az.CognitiveServices</span></span>
* <span data-ttu-id="e2d87-1161">Lade till åtgärden Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="e2d87-1161">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e2d87-1162">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e2d87-1162">Az.Compute</span></span>
* <span data-ttu-id="e2d87-1163">Lade till cmdletarna Add-AzVmssVMDataDisk och Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="e2d87-1163">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="e2d87-1164">Get-AzVMImage visar AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="e2d87-1164">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="e2d87-1165">Åtgärdade att värdena för alternativen SetAzVMChefExtension -BootstrapOptions och -JsonAttribute inte angavs i json-format.</span><span class="sxs-lookup"><span data-stu-id="e2d87-1165">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e2d87-1166">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e2d87-1166">Az.DataLakeStore</span></span>
* <span data-ttu-id="e2d87-1167">Uppdatera DataLake-paketet till 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="e2d87-1167">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="e2d87-1168">Lägg till standardsamtidighet för flertrådade åtgärder.</span><span class="sxs-lookup"><span data-stu-id="e2d87-1168">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="e2d87-1169">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="e2d87-1169">Az.Insights</span></span>
* <span data-ttu-id="e2d87-1170">Åtgärdade problem #7267 (autoskalningsområde)</span><span class="sxs-lookup"><span data-stu-id="e2d87-1170">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="e2d87-1171">Problem med att uppräknade parametrar inte ställdes in ordentligt när du skapade en ny autoskalningsregel (de ställdes alltid in med standardvärdet).</span><span class="sxs-lookup"><span data-stu-id="e2d87-1171">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="e2d87-1172">Åtgärdade problem #7513 [Insights] Set-AzDiagnosticSetting kräver uttrycklig specifikation av kategorier när inställningar skapas</span><span class="sxs-lookup"><span data-stu-id="e2d87-1172">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="e2d87-1173">Nu kräver inte cmdleten uttrycklig anvisning av kategorierna för att aktiveras under skapande, d.v.s. den fungerar enligt beskrivning</span><span class="sxs-lookup"><span data-stu-id="e2d87-1173">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e2d87-1174">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e2d87-1174">Az.Network</span></span>
* <span data-ttu-id="e2d87-1175">PeeringType ändrades till en obligatorisk parameter för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="e2d87-1175">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="e2d87-1176">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="e2d87-1176">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="e2d87-1177">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="e2d87-1177">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="e2d87-1178">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="e2d87-1178">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="e2d87-1179">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="e2d87-1179">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="e2d87-1180">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="e2d87-1180">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="e2d87-1181">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="e2d87-1181">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="e2d87-1182">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="e2d87-1182">Az.PolicyInsights</span></span>
* <span data-ttu-id="e2d87-1183">Cmdletar för principreparation har lagts till</span><span class="sxs-lookup"><span data-stu-id="e2d87-1183">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="e2d87-1184">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e2d87-1184">Az.Resources</span></span>
* <span data-ttu-id="e2d87-1185">Korrigering för https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="e2d87-1185">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="e2d87-1186">Tillåt att resurser listas med parametern -ResourceId för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="e2d87-1186">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="e2d87-1187">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e2d87-1187">Az.ServiceBus</span></span>
* <span data-ttu-id="e2d87-1188">Skrivskyddad MigrationState-egenskap har lagts till i PSServiceBusMigrationConfigurationAttributes, som hjälper till att hålla koll på migreringstillståndet.</span><span class="sxs-lookup"><span data-stu-id="e2d87-1188">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e2d87-1189">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e2d87-1189">Az.ServiceFabric</span></span>
* <span data-ttu-id="e2d87-1190">Åtgärda att lägga till certifikat till Linux-Vmss.</span><span class="sxs-lookup"><span data-stu-id="e2d87-1190">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="e2d87-1191">Åtgärdade Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="e2d87-1191">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="e2d87-1192">Använd rätt tumavtryck från nya certifikat (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="e2d87-1192">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="e2d87-1193">Visa undantag korrekt (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="e2d87-1193">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="e2d87-1194">Åtgärdade Update-AzServiceFabricDurability så att klusterkonfigurationen uppdateras innan Vmss-åtgärden CreateOrUpdate påbörjas.</span><span class="sxs-lookup"><span data-stu-id="e2d87-1194">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="e2d87-1195">0.4.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="e2d87-1195">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="e2d87-1196">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="e2d87-1196">Az.Profile</span></span>
* <span data-ttu-id="e2d87-1197">Åtgärdade problemet med Get-AzSubscription i CloudShell</span><span class="sxs-lookup"><span data-stu-id="e2d87-1197">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="e2d87-1198">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="e2d87-1198">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e2d87-1199">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e2d87-1199">Az.Compute</span></span>
* <span data-ttu-id="e2d87-1200">Nya storlekar lades till i listan över godkända VM-storlekar för vilka accelererat nätverk kommer att aktiveras vid användning av den enkla parameteruppsättningen för New-AzVm</span><span class="sxs-lookup"><span data-stu-id="e2d87-1200">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="e2d87-1201">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="e2d87-1201">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e2d87-1202">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e2d87-1202">Az.DataLakeStore</span></span>
* <span data-ttu-id="e2d87-1203">Lägger till stöd för regler för virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="e2d87-1203">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="e2d87-1204">Get-AzDataLakeStoreVirtualNetworkRule: Hämtar eller listar regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e2d87-1204">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="e2d87-1205">Add-AzDataLakeStoreVirtualNetworkRule: Lägger till en regel för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="e2d87-1205">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="e2d87-1206">Set-AzDataLakeStoreVirtualNetworkRule: Ändrar den angivna regeln för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="e2d87-1206">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="e2d87-1207">Remove-AzDataLakeStoreVirtualNetworkRule: Tar bort en regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e2d87-1207">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e2d87-1208">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e2d87-1208">Az.Network</span></span>
* <span data-ttu-id="e2d87-1209">Skicka protokollvärdet till serverdelen för att uppdatera cmdleten Test-AzNetworkWatcherConnectivity.</span><span class="sxs-lookup"><span data-stu-id="e2d87-1209">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="e2d87-1210">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="e2d87-1210">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e2d87-1211">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e2d87-1211">Az.Resources</span></span>
* <span data-ttu-id="e2d87-1212">Åtgärdade problem där Get-AzRoleDefinition genererar ett oläsligt undantag (när standardprofilen inte innehåller någon prenumeration och ingen omfattning har angetts) genom att lägga till ett beskrivande undantag i scenariot.</span><span class="sxs-lookup"><span data-stu-id="e2d87-1212">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="e2d87-1213">Ställ in ”RoleDefinitionNameParameterSet” som standardparameteruppsättning.</span><span class="sxs-lookup"><span data-stu-id="e2d87-1213">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="e2d87-1214">0.3.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="e2d87-1214">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="e2d87-1215">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="e2d87-1215">Azure.Storage</span></span>
* <span data-ttu-id="e2d87-1216">Åtgärda fel där Kopiera blob/fil inte kopierar metadata när målplatsen har ett problem med metadata</span><span class="sxs-lookup"><span data-stu-id="e2d87-1216">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="e2d87-1217">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="e2d87-1217">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="e2d87-1218">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="e2d87-1218">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="e2d87-1219">Stöd för att hämta användningsinformation om en Storage-resurs för en specifik plats och för att lägga till ett varningsmeddelande för att hämta användningsinformation om en global Storage-resurs är inaktuellt.</span><span class="sxs-lookup"><span data-stu-id="e2d87-1219">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="e2d87-1220">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="e2d87-1220">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="e2d87-1221">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e2d87-1221">Az.CognitiveServices</span></span>
* <span data-ttu-id="e2d87-1222">Stöd för Get-AzCognitiveServicesAccountSkus utan ett befintligt konto.</span><span class="sxs-lookup"><span data-stu-id="e2d87-1222">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e2d87-1223">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e2d87-1223">Az.Compute</span></span>
* <span data-ttu-id="e2d87-1224">Åtgärdade fel där Get-AzVM -ResourceGroupName <rg> returnerar fler än 50 resultat om det behövs</span><span class="sxs-lookup"><span data-stu-id="e2d87-1224">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="e2d87-1225">Lade till ett exempel för SimpleParameterSet i hjälpen för cmdleten New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="e2d87-1225">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="e2d87-1226">Ett stavfel i förloppsmeddelandet för Azure Disk Encryption har korrigerats</span><span class="sxs-lookup"><span data-stu-id="e2d87-1226">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="e2d87-1227">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="e2d87-1227">Az.DataFactoryV2</span></span>
* <span data-ttu-id="e2d87-1228">ADF .Net SDK-versionen har uppdaterats till 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="e2d87-1228">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e2d87-1229">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e2d87-1229">Az.Network</span></span>
* <span data-ttu-id="e2d87-1230">Funktionalitet för NetworkProfile har lagts till.</span><span class="sxs-lookup"><span data-stu-id="e2d87-1230">Added NetworkProfile functionality.</span></span> <span data-ttu-id="e2d87-1231">nya cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="e2d87-1231">new cmdlets added</span></span>
    - <span data-ttu-id="e2d87-1232">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e2d87-1232">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="e2d87-1233">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e2d87-1233">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="e2d87-1234">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e2d87-1234">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="e2d87-1235">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e2d87-1235">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="e2d87-1236">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="e2d87-1236">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="e2d87-1237">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="e2d87-1237">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="e2d87-1238">Länk för tjänstassociering på modell för undernät har lagts till</span><span class="sxs-lookup"><span data-stu-id="e2d87-1238">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="e2d87-1239">Cmdletarna New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap och Remove-AzVirtualNetworkTap har lagts till</span><span class="sxs-lookup"><span data-stu-id="e2d87-1239">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="e2d87-1240">Cmdletarna Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig och Remove-AzNEtworkInterfaceTapConfig har lagts till</span><span class="sxs-lookup"><span data-stu-id="e2d87-1240">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="e2d87-1241">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="e2d87-1241">Az.RedisCache</span></span>
* <span data-ttu-id="e2d87-1242">Tillåt att alla strängar används som storleksparametrar framöver.</span><span class="sxs-lookup"><span data-stu-id="e2d87-1242">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="e2d87-1243">Lägg till P5 i popup-fönstret PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="e2d87-1243">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="e2d87-1244">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e2d87-1244">Az.Resources</span></span>
* <span data-ttu-id="e2d87-1245">Parametern -Mode som saknades i Set-AzPolicyDefinition har lagts till</span><span class="sxs-lookup"><span data-stu-id="e2d87-1245">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="e2d87-1246">Åtgärdade buggen för cmdleten Get-AzProviderOperation för åtgärder med ursprung som innehåller användare</span><span class="sxs-lookup"><span data-stu-id="e2d87-1246">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="e2d87-1247">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e2d87-1247">Az.Sql</span></span>
* <span data-ttu-id="e2d87-1248">Ett problem där vissa cmdletar för säkerhetskopiering inte kunde identifiera den aktuella azure-prenumerationen har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="e2d87-1248">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e2d87-1249">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e2d87-1249">Az.Websites</span></span>
* <span data-ttu-id="e2d87-1250">Ny cmdlet: Get-AzWebAppContainerContinuousDeploymentUrl – Hämtar webhook-URL:en för kontinuerlig distribution av container</span><span class="sxs-lookup"><span data-stu-id="e2d87-1250">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="e2d87-1251">Nya cmdletar: New-AzWebAppContainerPSSession och Enter-WebAppContainerPSSession – Startar en PowerShell-fjärrsession i en containerapp för windows</span><span class="sxs-lookup"><span data-stu-id="e2d87-1251">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="e2d87-1252">0.2.0 – september 2018</span><span class="sxs-lookup"><span data-stu-id="e2d87-1252">0.2.0 - September 2018</span></span>
 <span data-ttu-id="e2d87-1253">Första versionen</span><span class="sxs-lookup"><span data-stu-id="e2d87-1253">Initial Release</span></span>