---
title: Viktig information om Azure PowerShell
description: Lär dig mer om alla de senaste uppdateringarna för Azure PowerShell-modulerna.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/09/2020
ms.openlocfilehash: 81afcd63e5ca7a776965849de9090b833f49acc7
ms.sourcegitcommit: a321ef9d134c684fa24ababcbd898f86b00d9364
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/20/2020
ms.locfileid: "77477241"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="7e515-103">Viktig information om Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="7e515-103">Azure PowerShell release notes</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="7e515-104">3.5.0 – februari 2020</span><span class="sxs-lookup"><span data-stu-id="7e515-104">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="7e515-105">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="7e515-105">Highlights since the last major release</span></span>
* <span data-ttu-id="7e515-106">Uppdaterade telemetri på klientsidan.</span><span class="sxs-lookup"><span data-stu-id="7e515-106">Updated client side telemetry.</span></span>
* <span data-ttu-id="7e515-107">Az.IotHub lade till cmdletar som stöd för att hantera enheter.</span><span class="sxs-lookup"><span data-stu-id="7e515-107">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="7e515-108">Az.SqlVirtualMachine lade till cmdletar för lyssningsfunktion för tillgänglighetsgrupp.</span><span class="sxs-lookup"><span data-stu-id="7e515-108">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7e515-109">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7e515-109">Az.Accounts</span></span>
* <span data-ttu-id="7e515-110">Lade till SubscriptionId, TenantId och körningstid i data för telemetri på klientsidan</span><span class="sxs-lookup"><span data-stu-id="7e515-110">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7e515-111">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7e515-111">Az.Automation</span></span>
* <span data-ttu-id="7e515-112">Åtgärdade skrivfel i exempel 1 i referensdokumentation för ”New-AzAutomationSoftwareUpdateConfiguration”</span><span class="sxs-lookup"><span data-stu-id="7e515-112">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="7e515-113">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7e515-113">Az.CognitiveServices</span></span>
* <span data-ttu-id="7e515-114">Uppdaterade SDK till 7.0</span><span class="sxs-lookup"><span data-stu-id="7e515-114">Updated SDK to 7.0</span></span>
* <span data-ttu-id="7e515-115">Förbättrade felmeddelande vid serversvar om tom brödtext</span><span class="sxs-lookup"><span data-stu-id="7e515-115">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7e515-116">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7e515-116">Az.Compute</span></span>
* <span data-ttu-id="7e515-117">Tillät tomt värde för ProximityPlacementGroupId under uppdatering</span><span class="sxs-lookup"><span data-stu-id="7e515-117">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="7e515-118">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="7e515-118">Az.FrontDoor</span></span>
* <span data-ttu-id="7e515-119">Lade till cmdlet för att hämta hanterade regeldefinitioner som kan användas i WAF</span><span class="sxs-lookup"><span data-stu-id="7e515-119">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7e515-120">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7e515-120">Az.IotHub</span></span>
* <span data-ttu-id="7e515-121">Lade till stöd för att hantera enheter i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="7e515-121">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="7e515-122">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="7e515-122">New Cmdlets are:</span></span>
    - <span data-ttu-id="7e515-123">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="7e515-123">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="7e515-124">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="7e515-124">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="7e515-125">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="7e515-125">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="7e515-126">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="7e515-126">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7e515-127">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7e515-127">Az.KeyVault</span></span>
* <span data-ttu-id="7e515-128">Åtgärdade duplicerad text för Add-AzKeyVaultKey.md</span><span class="sxs-lookup"><span data-stu-id="7e515-128">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7e515-129">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7e515-129">Az.Monitor</span></span>
* <span data-ttu-id="7e515-130">Åtgärdade beskrivning av cmdleten Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="7e515-130">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="7e515-131">En ny parameter med namnet ActionGroupId har lagts till i kommandot ”New-AzMetricAlertRuleV2”.</span><span class="sxs-lookup"><span data-stu-id="7e515-131">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="7e515-132">Användaren kan ange ActionGroupId(string) eller ActionGroup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="7e515-132">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7e515-133">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7e515-133">Az.Network</span></span>
* <span data-ttu-id="7e515-134">Lade till en extra parameteranteckning för parametern ”-EnableProxyProtocol” för cmdleten ”New-AzPrivateLinkService”.</span><span class="sxs-lookup"><span data-stu-id="7e515-134">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="7e515-135">Åtgärdade FilterData-exempel i Start-AzVirtualNetworkGatewayConnectionPacketCapture.md och Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="7e515-135">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="7e515-136">Lade till paketinsamlingsexempel för att samla in alla inre och yttre paket i Start-AzVirtualNetworkGatewayConnectionPacketCapture.md och Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="7e515-136">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="7e515-137">Lade till stöd för Azure-brandväggsprincip på VNet-brandväggar</span><span class="sxs-lookup"><span data-stu-id="7e515-137">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="7e515-138">Inga nya cmdletar har lagts till.</span><span class="sxs-lookup"><span data-stu-id="7e515-138">No new cmdlets are added.</span></span> <span data-ttu-id="7e515-139">Lättar begränsningen för brandväggsprincip på VNet-brandväggar</span><span class="sxs-lookup"><span data-stu-id="7e515-139">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7e515-140">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7e515-140">Az.RecoveryServices</span></span>
* <span data-ttu-id="7e515-141">Lade till stöd för Restore-as-files för SQL-databaser.</span><span class="sxs-lookup"><span data-stu-id="7e515-141">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7e515-142">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7e515-142">Az.Resources</span></span>
* <span data-ttu-id="7e515-143">Omstrukturerade cmdletar för malldistribution</span><span class="sxs-lookup"><span data-stu-id="7e515-143">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="7e515-144">Lade till nya cmdletar för att hantera distributioner i hanteringsgruppen: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="7e515-144">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="7e515-145">Lade till nya cmdletar för att hantera distributioner i klientorganisationsområdet: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="7e515-145">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="7e515-146">Omstrukturerade \*-AzDeployment-cmdletar för att fungera specifikt i prenumerationsomfattningen</span><span class="sxs-lookup"><span data-stu-id="7e515-146">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="7e515-147">Skapade alias \*-AzSubscriptionDeployment för \*-AzDeployment-cmdletar</span><span class="sxs-lookup"><span data-stu-id="7e515-147">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="7e515-148">Åtgärdade ”Update-AzADApplication” när parametern ”AvailableToOtherTenants” inte har angetts</span><span class="sxs-lookup"><span data-stu-id="7e515-148">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="7e515-149">Tog bort ApplicationObjectWithoutCredentialParameterSet för att undvika AmbiguousParameterSetException.</span><span class="sxs-lookup"><span data-stu-id="7e515-149">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="7e515-150">Återskapade hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="7e515-150">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="7e515-151">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7e515-151">Az.Sql</span></span>
* <span data-ttu-id="7e515-152">Lade till stöd för återställning till tidpunkt mellan prenumerationer på hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="7e515-152">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="7e515-153">Lade till stöd för att ändra befintlig SQL Managed Instance-maskinvarugenerering</span><span class="sxs-lookup"><span data-stu-id="7e515-153">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="7e515-154">Åtgärdade ”Update-AzSqlServerVulnerabilityAssessmentSetting”-hjälpexempel: parameter/egenskapsutdata - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="7e515-154">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="7e515-155">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="7e515-155">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="7e515-156">Lade till cmdletar för lyssningsfunktion för tillgänglighetsgrupp</span><span class="sxs-lookup"><span data-stu-id="7e515-156">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="7e515-157">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="7e515-157">Az.StorageSync</span></span>
* <span data-ttu-id="7e515-158">Uppdaterade teckenuppsättningar som stöds i ”Invoke-AzStorageSyncCompatibilityCheck”.</span><span class="sxs-lookup"><span data-stu-id="7e515-158">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="7e515-159">3.4.0 – februari 2020</span><span class="sxs-lookup"><span data-stu-id="7e515-159">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="7e515-160">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="7e515-160">Highlights since the last major release</span></span>
* <span data-ttu-id="7e515-161">Första Az.CosmosDB-versionen 0.1.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="7e515-161">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="7e515-162">Stöd för Az.Network ConnectionMonitor V2 har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e515-162">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7e515-163">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7e515-163">Az.Accounts</span></span>
* <span data-ttu-id="7e515-164">Inaktivera automatisk sparande av kontext när AzureRmContext.json inte är tillgängligt</span><span class="sxs-lookup"><span data-stu-id="7e515-164">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="7e515-165">Uppdatera referensen till Azure Powershell Common till 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="7e515-165">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="7e515-166">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7e515-166">Az.ApiManagement</span></span>
* <span data-ttu-id="7e515-167">**Get-AzApiManagementApiSchema** Hämtning av Open-Api-schema som är associerat med ett API har åtgärdats   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="7e515-167">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="7e515-168">**New-AzApiManagementProduct**\* och **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="7e515-168">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="7e515-169">Åtgärda dokumentation för https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="7e515-169">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="7e515-170">**Set-AzApiManagementApi** Exempel för att visa hur ServiceUrl uppdateras med hjälp av cmdleten har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e515-170">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7e515-171">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7e515-171">Az.Compute</span></span>
* <span data-ttu-id="7e515-172">Begränsa antalet VM-status till 100 för att undvika begränsning när Get-AzVM -Status utförs utan VM-namn.</span><span class="sxs-lookup"><span data-stu-id="7e515-172">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="7e515-173">Lägg till cmdleten Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="7e515-173">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="7e515-174">Lägg till parametrarna EncryptionType och DiskEncryptionSetId i följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="7e515-174">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="7e515-175">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="7e515-175">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="7e515-176">Lägg till parametern ColocationStatus för cmdleten Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="7e515-176">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7e515-177">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7e515-177">Az.DataFactory</span></span>
* <span data-ttu-id="7e515-178">Uppdatera ADF .Net SDK-versionen till 4.7.0</span><span class="sxs-lookup"><span data-stu-id="7e515-178">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="7e515-179">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="7e515-179">Az.DeploymentManager</span></span>
* <span data-ttu-id="7e515-180">Lägger till LIST-åtgärder för resurser</span><span class="sxs-lookup"><span data-stu-id="7e515-180">Adds LIST operations for resources</span></span>
* <span data-ttu-id="7e515-181">Lägger till funktion för att utföra åtgärder för hälsokontrollsteg</span><span class="sxs-lookup"><span data-stu-id="7e515-181">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="7e515-182">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="7e515-182">Az.HDInsight</span></span>
* <span data-ttu-id="7e515-183">Åtgärda dokumentfel för New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="7e515-183">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7e515-184">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7e515-184">Az.KeyVault</span></span>
* <span data-ttu-id="7e515-185">Lägg till Name-alias för attributet VaultName så att Remove-AzureKeyVault stämmer överens med New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="7e515-185">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7e515-186">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7e515-186">Az.Network</span></span>
* <span data-ttu-id="7e515-187">Nytt exempel har lagts till i Set-AzNetworkWatcherConfigFlowLog.md för att demonstrera ett inaktiveringsscenario för Trafikanalys.</span><span class="sxs-lookup"><span data-stu-id="7e515-187">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="7e515-188">Lägg till stöd för att tilldela konfiguration av hanterings-IP till Azure Firewall – ett dedikerat undernät och en offentlig IP som brandväggen använder för dess hanteringstrafik</span><span class="sxs-lookup"><span data-stu-id="7e515-188">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="7e515-189">Cmdleten New-AzFirewall har uppdaterats:</span><span class="sxs-lookup"><span data-stu-id="7e515-189">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="7e515-190">Parametern -ManagementPublicIpAddress (inte obligatorisk) som accepterar ett offentligt IP-adressobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e515-190">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="7e515-191">Metoden SetManagementIpConfiguration har lagts till för brandväggsobjekt – kräver ett undernät och en offentlig IP-adress som indata – undernätets namn måste vara ”AzureFirewallManagementSubnet”</span><span class="sxs-lookup"><span data-stu-id="7e515-191">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="7e515-192">Exempel för Get-AzNetworkSecurityGroup har korrigerats så att exempel visas för NSG:er i stället för nätverksgränssnitt.</span><span class="sxs-lookup"><span data-stu-id="7e515-192">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="7e515-193">Ett skrivfel har åtgärdats i kommandot New-AzVpnSite som hindrade kompletteraren för resurs-ID från att fylla i en parameter.</span><span class="sxs-lookup"><span data-stu-id="7e515-193">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="7e515-194">Stöd för Url-konfiguration i åtgärdsuppsättningen för omskrivningsregler i Application Gateway har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e515-194">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="7e515-195">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="7e515-195">New cmdlets added:</span></span>
        - <span data-ttu-id="7e515-196">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="7e515-196">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="7e515-197">Cmdletar har uppdaterats med den valfria parametern -UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="7e515-197">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="7e515-198">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="7e515-198">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="7e515-199">Lägg till stöd för resurser för NetworkWatcher ConnectionMonitor version 2</span><span class="sxs-lookup"><span data-stu-id="7e515-199">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="7e515-200">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="7e515-200">Az.PolicyInsights</span></span>
* <span data-ttu-id="7e515-201">Stöd för utvärdering av efterlevnad innan fastställande av vilken resurs som ska åtgärdas</span><span class="sxs-lookup"><span data-stu-id="7e515-201">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="7e515-202">Lägg till parametern ”-ResourceDiscoverMode” för Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="7e515-202">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="7e515-203">Lägg till cmdleten Get-AzPolicyMetadata för att hämta resurser för principmetadata</span><span class="sxs-lookup"><span data-stu-id="7e515-203">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="7e515-204">Get-AzPolicyState och Get-AzPolicyStateSummary för API-versionen 2019-10-01 har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="7e515-204">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7e515-205">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7e515-205">Az.RecoveryServices</span></span>
* <span data-ttu-id="7e515-206">Azure Site Recovery-stöd för att ta bort en replikerad disk.</span><span class="sxs-lookup"><span data-stu-id="7e515-206">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="7e515-207">Tillagt Azure Backup-stöd för att lägga till taggar när ett Recovery Services-valv skapas.</span><span class="sxs-lookup"><span data-stu-id="7e515-207">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7e515-208">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7e515-208">Az.Resources</span></span>
* <span data-ttu-id="7e515-209">Gör -Scope valfritt i cmdletarna \*-AzPolicyAssignment med standardinställning till kontextprenumeration</span><span class="sxs-lookup"><span data-stu-id="7e515-209">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="7e515-210">Lägg till exempel på att skapa ADServicePrincipal med lösenord och nyckelautentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="7e515-210">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="7e515-211">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7e515-211">Az.Sql</span></span>
<span data-ttu-id="7e515-212">Åtgärda cmdleten New-AzSqlDatabaseSecondary så att existensen PartnerDatabaseName kontrolleras i stället för existensen DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="7e515-212">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7e515-213">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7e515-213">Az.Storage</span></span>
* <span data-ttu-id="7e515-214">Stöd för angivning av krypteringsnyckeltyp för Tabell/kö i Skapa lagringskonto</span><span class="sxs-lookup"><span data-stu-id="7e515-214">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="7e515-215">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7e515-215">New-AzStorageAccount</span></span>
* <span data-ttu-id="7e515-216">Visa RequestId när StorageException inte har ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="7e515-216">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="7e515-217">Åtgärda exempel 6 för cmdleten Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="7e515-217">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7e515-218">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7e515-218">Az.Websites</span></span>
* <span data-ttu-id="7e515-219">Set-AzWebapp och Set-AzWebappSlot stöder egenskaperna AlwaysOn, MinTls och FtpsState</span><span class="sxs-lookup"><span data-stu-id="7e515-219">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="7e515-220">Åtgärdar problemet där inställning av HttpsOnly samtidigt som AppservicePlan ändrades med det enskilda kommandot Set-AzWebApp återställde HttpsOnly till standardvärdet</span><span class="sxs-lookup"><span data-stu-id="7e515-220">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="7e515-221">3.3.0 – januari 2020</span><span class="sxs-lookup"><span data-stu-id="7e515-221">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7e515-222">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7e515-222">Az.Accounts</span></span>
* <span data-ttu-id="7e515-223">Nu stöder Add-AzEnvironment och Set-AzEnvironment parametrarna AzureAttestationServiceEndpointResourceId och AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="7e515-223">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="7e515-224">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7e515-224">Az.Cdn</span></span>
* <span data-ttu-id="7e515-225">Information om felsvar visas i New-AzCdnEndpoint-cmdleten</span><span class="sxs-lookup"><span data-stu-id="7e515-225">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7e515-226">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7e515-226">Az.Compute</span></span>
* <span data-ttu-id="7e515-227">Set-AzVMCustomScriptExtension-cmdleten har åtgärdats för en virtuell dator med hanterad OD-disk som inte har någon operativsystemprofil.</span><span class="sxs-lookup"><span data-stu-id="7e515-227">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="7e515-228">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="7e515-228">Az.ContainerInstance</span></span>
* <span data-ttu-id="7e515-229">Parameternamn som används med New-AzContainerGroup-exempel har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="7e515-229">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="7e515-230">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="7e515-230">Az.DataBoxEdge</span></span>
* <span data-ttu-id="7e515-231">Cmdleten ”Get-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e515-231">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="7e515-232">Hämta gränslagringscontainern</span><span class="sxs-lookup"><span data-stu-id="7e515-232">Get the Edge Storage Container</span></span>
* <span data-ttu-id="7e515-233">Cmdleten ”New-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e515-233">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="7e515-234">Skapa en ny gränslagringscontainer</span><span class="sxs-lookup"><span data-stu-id="7e515-234">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="7e515-235">Cmdleten ”Remove-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e515-235">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="7e515-236">Ta bort gränslagringscontainern</span><span class="sxs-lookup"><span data-stu-id="7e515-236">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="7e515-237">Cmdleten ”Invoke-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e515-237">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="7e515-238">Anropa åtgärd för att uppdatera data i gränslagringscontainer</span><span class="sxs-lookup"><span data-stu-id="7e515-238">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="7e515-239">Cmdleten ”Get-AzDataBoxEdgeStorageAccount” har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e515-239">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="7e515-240">Hämta gränslagringskontot</span><span class="sxs-lookup"><span data-stu-id="7e515-240">Get the Edge Storage Account</span></span>
* <span data-ttu-id="7e515-241">Cmdleten ”New-AzDataBoxEdgeStorageAccount” har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e515-241">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="7e515-242">Skapa ett nytt gränslagringskonto</span><span class="sxs-lookup"><span data-stu-id="7e515-242">Create new Edge Storage Account</span></span>
* <span data-ttu-id="7e515-243">Cmdleten ”Remove-AzDataBoxEdgeStorageAccount” har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e515-243">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="7e515-244">Ta bort gränslagringskontot</span><span class="sxs-lookup"><span data-stu-id="7e515-244">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="7e515-245">Anropa cmdleten ”Invoke-AzDataBoxEdgeShare”</span><span class="sxs-lookup"><span data-stu-id="7e515-245">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="7e515-246">Anropa åtgärd för att uppdatera resursdata</span><span class="sxs-lookup"><span data-stu-id="7e515-246">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="7e515-247">Cmdleten ”Set-AzDataBoxEdgeStorageAccountCredential” har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e515-247">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="7e515-248">Ange autentiseringsuppgifter för az databoxedge-lagringskonto</span><span class="sxs-lookup"><span data-stu-id="7e515-248">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7e515-249">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7e515-249">Az.DataFactory</span></span>
* <span data-ttu-id="7e515-250">Lägg till AutoUpdateETA-, LatestVersion-, PushedVersion-, TaskQueueId- och VersionStatus-egenskaper för Get-AzDataFactoryV2IntegrationRuntime-cmd</span><span class="sxs-lookup"><span data-stu-id="7e515-250">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="7e515-251">Uppdatera ADF .Net SDK-versionen till 4.6.0</span><span class="sxs-lookup"><span data-stu-id="7e515-251">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="7e515-252">Lägg till parametern ”PublicIPs” för ”Set-AzureRmDataFactoryV2IntegrationRuntime”-cmd så att Azure-SSIS IR kan skapas med statiska offentliga IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="7e515-252">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="7e515-253">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="7e515-253">Az.DevTestLabs</span></span>
* <span data-ttu-id="7e515-254">Ta bort den brutna länken i Get-AzDtlAllowedVMSizesPolicy.md</span><span class="sxs-lookup"><span data-stu-id="7e515-254">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="7e515-255">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7e515-255">Az.EventHub</span></span>
* <span data-ttu-id="7e515-256">Korrigering av problem 10634: Åtgärda referensen till null-objekt för eventhubnamespace-borttagning</span><span class="sxs-lookup"><span data-stu-id="7e515-256">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="7e515-257">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="7e515-257">Az.HDInsight</span></span>
* <span data-ttu-id="7e515-258">Åtgärda Invoke-AzHDInsightHiveJob.md-fel.</span><span class="sxs-lookup"><span data-stu-id="7e515-258">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="7e515-259">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="7e515-259">Az.MachineLearning</span></span>
* <span data-ttu-id="7e515-260">Nedanstående cmdletar har tagits bort eftersom MachineLearningCompute inte längre är tillgängligt</span><span class="sxs-lookup"><span data-stu-id="7e515-260">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="7e515-261">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="7e515-261">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="7e515-262">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="7e515-262">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="7e515-263">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="7e515-263">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="7e515-264">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="7e515-264">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="7e515-265">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="7e515-265">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="7e515-266">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="7e515-266">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="7e515-267">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="7e515-267">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7e515-268">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7e515-268">Az.Network</span></span>
* <span data-ttu-id="7e515-269">Uppgradera beroende av Microsoft.Azure.Management.Sql från 1.36-preview till 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="7e515-269">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7e515-270">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7e515-270">Az.RecoveryServices</span></span>
* <span data-ttu-id="7e515-271">Ändrat Azure Site Recovery-stöd för krypterade vilande data på virtuella datorer med hanterade diskar med kundhanterade nycklar för Azure till Azure-providern.</span><span class="sxs-lookup"><span data-stu-id="7e515-271">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="7e515-272">Azure Site Recovery-stöd för att ange ID för diskkrypteringsuppsättning som valfri inmatning för aktivering av skydd för VMware till Azure.</span><span class="sxs-lookup"><span data-stu-id="7e515-272">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="7e515-273">Azure Site Recovery-stöd för att ange ID för diskkrypteringsuppsättning som valfri inmatning på disknivå för aktivering av skydd för VMware till Azure.</span><span class="sxs-lookup"><span data-stu-id="7e515-273">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="7e515-274">Azure Site Recovery-stöd för att uppdatera replikeringsskyddade objekt med mappning för diskkrypteringsuppsättning för HyperV till Azure.</span><span class="sxs-lookup"><span data-stu-id="7e515-274">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7e515-275">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7e515-275">Az.Resources</span></span>
* <span data-ttu-id="7e515-276">Åtgärda ett fel i hjälpdokument för ”Remove-AzTag”.</span><span class="sxs-lookup"><span data-stu-id="7e515-276">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="7e515-277">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7e515-277">Az.Sql</span></span>
* <span data-ttu-id="7e515-278">Åtgärda funktioner i cmdletar för att ange baslinjen för sårbarhetsbedömning för arbete med huvuddatabasen för Azure-databasen och begränsa den för systemdatabaser på hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="7e515-278">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="7e515-279">Åtgärda ett fel när en redundansgrupp för en SQL-instans skapas</span><span class="sxs-lookup"><span data-stu-id="7e515-279">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="7e515-280">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="7e515-280">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="7e515-281">Lägg till DR som en ny giltig licenstyp</span><span class="sxs-lookup"><span data-stu-id="7e515-281">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7e515-282">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7e515-282">Az.Storage</span></span>
* <span data-ttu-id="7e515-283">Lägg till varningsmeddelande om icke-bakåtkompatibel ändring för DefaultAction-värdeändring i en framtida version</span><span class="sxs-lookup"><span data-stu-id="7e515-283">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="7e515-284">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="7e515-284">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="7e515-285">Stöd för att hämta lagringskontots senaste synkroniseringstid genom att köra get-AzureRMStorageAccount med parametern -IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="7e515-285">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span> 
    - <span data-ttu-id="7e515-286">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7e515-286">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="7e515-287">3.2.0 – December 2019</span><span class="sxs-lookup"><span data-stu-id="7e515-287">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="7e515-288">Allmänt</span><span class="sxs-lookup"><span data-stu-id="7e515-288">General</span></span>
* <span data-ttu-id="7e515-289">Uppdatera referenser i .psd1 för att använda relativa sökvägar för alla moduler</span><span class="sxs-lookup"><span data-stu-id="7e515-289">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7e515-290">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7e515-290">Az.Accounts</span></span>
* <span data-ttu-id="7e515-291">Ange rätt UserAgent för telemetri på klientsidan för Az 4.0 preview</span><span class="sxs-lookup"><span data-stu-id="7e515-291">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="7e515-292">Visa användarvänligt felmeddelande när kontexten är null i Az 4.0 preview</span><span class="sxs-lookup"><span data-stu-id="7e515-292">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="7e515-293">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="7e515-293">Az.Batch</span></span>
* <span data-ttu-id="7e515-294">Korrigera problem [#10602](https://github.com/Azure/azure-powershell/issues/10602), där **New-AzBatchPool** skickade VirtualMachineConfiguration.ContainerConfiguration eller VirtualMachineConfiguration.DataDisks på ett felaktigt sätt till servern.</span><span class="sxs-lookup"><span data-stu-id="7e515-294">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7e515-295">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7e515-295">Az.DataFactory</span></span>
* <span data-ttu-id="7e515-296">Uppdatera ADF .Net SDK-versionen till 4.5.0</span><span class="sxs-lookup"><span data-stu-id="7e515-296">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="7e515-297">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="7e515-297">Az.FrontDoor</span></span>
* <span data-ttu-id="7e515-298">Stöd har lagts till för undantag för hanterade regler för brandväggen för webbaserade program</span><span class="sxs-lookup"><span data-stu-id="7e515-298">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="7e515-299">Lägg till SocketAddr för automatisk komplettering</span><span class="sxs-lookup"><span data-stu-id="7e515-299">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="7e515-300">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="7e515-300">Az.HealthcareApis</span></span>
* <span data-ttu-id="7e515-301">Undantagshantering</span><span class="sxs-lookup"><span data-stu-id="7e515-301">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7e515-302">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7e515-302">Az.KeyVault</span></span>
* <span data-ttu-id="7e515-303">Åtgärdat fel vid åtkomst av värde som kanske inte har angetts</span><span class="sxs-lookup"><span data-stu-id="7e515-303">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="7e515-304">Hantering av ECC-certifikat (Elliptic Curve Cryptography)</span><span class="sxs-lookup"><span data-stu-id="7e515-304">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="7e515-305">Stöd har lagts till för att ange kurvan för certifikatprinciper</span><span class="sxs-lookup"><span data-stu-id="7e515-305">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7e515-306">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7e515-306">Az.Monitor</span></span>
* <span data-ttu-id="7e515-307">Lägger till valfritt argument i kommandot Lägg till diagnostikinställningar.</span><span class="sxs-lookup"><span data-stu-id="7e515-307">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="7e515-308">Ett växelargument som om det finns visar att exporten till Log Analytics måste ske till ett fast schema (kallas även</span><span class="sxs-lookup"><span data-stu-id="7e515-308">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="7e515-309">dedikerad, datatyp)</span><span class="sxs-lookup"><span data-stu-id="7e515-309">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7e515-310">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7e515-310">Az.Network</span></span>
* <span data-ttu-id="7e515-311">Stöd för IpGroups i program-, NAT- och nätverksregler för Azure Firewall.</span><span class="sxs-lookup"><span data-stu-id="7e515-311">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7e515-312">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7e515-312">Az.Resources</span></span>
* <span data-ttu-id="7e515-313">Åtgärda ett problem där malldistributionen inte kan läsa en mallparameter om dess namn står i konflikt med ett inbyggt parameternamn.</span><span class="sxs-lookup"><span data-stu-id="7e515-313">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="7e515-314">Uppdaterade princip-cmdletar för att använda den nya API-versionen 2019-09-01 som introducerar grupperingsstöd inom principuppsättningsdefinitioner.</span><span class="sxs-lookup"><span data-stu-id="7e515-314">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="7e515-315">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7e515-315">Az.Sql</span></span>
* <span data-ttu-id="7e515-316">Uppgraderad funktion för att skapa lagring i automatisk aktivering av sårbarhetsbedömning till StorageV2</span><span class="sxs-lookup"><span data-stu-id="7e515-316">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7e515-317">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7e515-317">Az.Storage</span></span>
* <span data-ttu-id="7e515-318">Stöd för generering av blob/container-identitetsbaserad SAS-token med lagringskontextbaserad på OAuth-autentisering</span><span class="sxs-lookup"><span data-stu-id="7e515-318">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="7e515-319">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="7e515-319">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="7e515-320">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="7e515-320">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="7e515-321">Stöd för återkallning av användardelegeringsnycklar för lagringskonto för att återkalla alla SAS-token</span><span class="sxs-lookup"><span data-stu-id="7e515-321">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="7e515-322">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="7e515-322">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="7e515-323">Uppgradera till Microsoft.Azure.Management.Storage 14.2.0 för att stödja den nya API-versionen 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="7e515-323">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="7e515-324">Stöd för QuotaGiB (resurskvot i Gibibye) för värden över 5120 i hanteringsplanet för cmdletar för filresurser och parameteraliaset. Quota har också lagts till för parametern ”QuotaGiB”.</span><span class="sxs-lookup"><span data-stu-id="7e515-324">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span> 
    - <span data-ttu-id="7e515-325">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="7e515-325">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="7e515-326">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="7e515-326">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="7e515-327">Lägg till parameteraliaset QuotaGiB i parametern Quota</span><span class="sxs-lookup"><span data-stu-id="7e515-327">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="7e515-328">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="7e515-328">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="7e515-329">Åtgärda problemet att Set-AzStorageContainerAcl kan rensa den lagrade åtkomstprincipen</span><span class="sxs-lookup"><span data-stu-id="7e515-329">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="7e515-330">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="7e515-330">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="7e515-331">3.1.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="7e515-331">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="7e515-332">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="7e515-332">Highlights since the last major release</span></span>
* <span data-ttu-id="7e515-333">Az.DataBoxEdge 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="7e515-333">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="7e515-334">Az.SqlVirtualMachine 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="7e515-334">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7e515-335">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7e515-335">Az.Compute</span></span>
* <span data-ttu-id="7e515-336">Funktion för att använda en virtuell dator igen</span><span class="sxs-lookup"><span data-stu-id="7e515-336">VM Reapply feature</span></span>
    - <span data-ttu-id="7e515-337">Lägg till parameter för att använda igen till cmdleten Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="7e515-337">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="7e515-338">Funktionen AutomaticRepairs i VM-skalningsuppsättningar:</span><span class="sxs-lookup"><span data-stu-id="7e515-338">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="7e515-339">Lägg till parametrarna EnableAutomaticRepair, AutomaticRepairGracePeriod och AutomaticRepairMaxInstanceRepairsPercent till följande cmdletar:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7e515-339">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="7e515-340">Stöd för galleriavbildningar i flera klientorganisationer för New-AzVM</span><span class="sxs-lookup"><span data-stu-id="7e515-340">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="7e515-341">Lägg till "Spot" till argumentslutföraren i prioritetsparametern i cmdletarna New-AzVM, New-AzVMConfig och New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7e515-341">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="7e515-342">Lägg till parametrarna DiskIOPSReadWrite och DiskMBpsReadWrite till cmdleten Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="7e515-342">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="7e515-343">Ändra parametern SourceImageId för cmdleten New-AzGalleryImageVersion till valfri</span><span class="sxs-lookup"><span data-stu-id="7e515-343">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="7e515-344">Lägg till parametrarna OSDiskImage och DataDiskImage till cmdleten New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="7e515-344">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="7e515-345">Lägg till parametern HyperVGeneration till cmdleten New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="7e515-345">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="7e515-346">Lägg till parametern SkipExtensionsOnOverprovisionedVMs till cmdletarna New-AzVmss, New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7e515-346">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="7e515-347">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="7e515-347">Az.DataBoxEdge</span></span>
* <span data-ttu-id="7e515-348">Cmdleten `Get-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e515-348">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="7e515-349">Hämta ordning</span><span class="sxs-lookup"><span data-stu-id="7e515-349">Get the Order</span></span>
* <span data-ttu-id="7e515-350">Cmdleten `New-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e515-350">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="7e515-351">Skapa ny ordning</span><span class="sxs-lookup"><span data-stu-id="7e515-351">Create new Order</span></span>
* <span data-ttu-id="7e515-352">Cmdleten `Remove-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e515-352">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="7e515-353">Ta bort ordning</span><span class="sxs-lookup"><span data-stu-id="7e515-353">Remove the Order</span></span>
* <span data-ttu-id="7e515-354">Cmdleten `New-AzDataBoxEdgeShare` har ändrats</span><span class="sxs-lookup"><span data-stu-id="7e515-354">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="7e515-355">Nu skapas lokal filresurs</span><span class="sxs-lookup"><span data-stu-id="7e515-355">Now creates Local Share</span></span>
* <span data-ttu-id="7e515-356">Cmdleten `Set-AzDataBoxEdgeRole` har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e515-356">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="7e515-357">Nu kan IotRole mappas till filresursen</span><span class="sxs-lookup"><span data-stu-id="7e515-357">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="7e515-358">Cmdleten `Invoke-AzDataBoxEdgeDevice` har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e515-358">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="7e515-359">Anropa genomsökningsuppdatering, ladda ned uppdatering, installera uppdateringar på enheten</span><span class="sxs-lookup"><span data-stu-id="7e515-359">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="7e515-360">Cmdleten `Get-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e515-360">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="7e515-361">Hämtar information om utlösare</span><span class="sxs-lookup"><span data-stu-id="7e515-361">Gets the information about Triggers</span></span>
* <span data-ttu-id="7e515-362">Cmdleten `New-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e515-362">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="7e515-363">Skapa nya utlösare</span><span class="sxs-lookup"><span data-stu-id="7e515-363">Create new Triggers</span></span>
* <span data-ttu-id="7e515-364">Cmdleten `Remove-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e515-364">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="7e515-365">Ta bort utlösare</span><span class="sxs-lookup"><span data-stu-id="7e515-365">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7e515-366">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7e515-366">Az.DataFactory</span></span>
* <span data-ttu-id="7e515-367">Uppdatera ADF .Net SDK-versionen till 4.4.0</span><span class="sxs-lookup"><span data-stu-id="7e515-367">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="7e515-368">Lägg till parametern ExpressCustomSetup för kommandot Set-AzureRmDataFactoryV2IntegrationRuntime för att aktivera installationskonfigurationer och komponenter från tredje part utan anpassat konfigurationsskript.</span><span class="sxs-lookup"><span data-stu-id="7e515-368">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7e515-369">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7e515-369">Az.DataLakeStore</span></span>
* <span data-ttu-id="7e515-370">Uppdatera dokumentation för Get-AzDataLakeStoreDeletedItem och Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="7e515-370">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="7e515-371">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7e515-371">Az.EventHub</span></span>
* <span data-ttu-id="7e515-372">Korrigering av problem #10301: Korrigera datumformat för SAS-token</span><span class="sxs-lookup"><span data-stu-id="7e515-372">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="7e515-373">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="7e515-373">Az.FrontDoor</span></span>
* <span data-ttu-id="7e515-374">Lägg till parametern MinimumTlsVersion till Enable-AzFrontDoorCustomDomainHttps och New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="7e515-374">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="7e515-375">Lägg till parametrarna HealthProbeMethod och EnabledState till New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="7e515-375">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="7e515-376">Lägg till en ny cmdlet för att skapa BackendPoolsSettings-objekt som passar i skapande/uppdatering av Front Door</span><span class="sxs-lookup"><span data-stu-id="7e515-376">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="7e515-377">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="7e515-377">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7e515-378">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7e515-378">Az.Network</span></span>
* <span data-ttu-id="7e515-379">Ändra alternativexemplen Start-AzVirtualNetworkGatewayConnectionPacketCapture.md och Start-AzVirtualnetworkGatewayPacketCapture.md för FilterData.</span><span class="sxs-lookup"><span data-stu-id="7e515-379">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="7e515-380">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="7e515-380">Az.PrivateDns</span></span>
* <span data-ttu-id="7e515-381">Uppdaterade PrivateDns .NET SDK till version 1.0.0</span><span class="sxs-lookup"><span data-stu-id="7e515-381">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7e515-382">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7e515-382">Az.RecoveryServices</span></span>
* <span data-ttu-id="7e515-383">Stöd för att välja disktyp vid aktivering av skydd i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="7e515-383">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="7e515-384">Korrigering av bugg för åtgärdsredigering av återställningsplan i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="7e515-384">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="7e515-385">Återställningsstöd för att godkänna filestream-databaser i Azure Backup SQL.</span><span class="sxs-lookup"><span data-stu-id="7e515-385">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="7e515-386">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="7e515-386">Az.RedisCache</span></span>
* <span data-ttu-id="7e515-387">Parametern MinimumTlsVersion har lagts till i cmdletarna New-AzRedisCache och Set-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="7e515-387">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="7e515-388">Dessutom har MinimumTlsVersion lagts till i utdata för cmdleten Get-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="7e515-388">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="7e515-389">Verifiering har lagts till på parametern -Size i cmdletarna Set-AzRedisCache och New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="7e515-389">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="7e515-390">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7e515-390">Az.Resources</span></span>
- <span data-ttu-id="7e515-391">Uppdaterade policy-cmdletar för att använda den nya API-versionen 2019-06-01 som har en ny EnforcementMode-egenskap i policytilldelningen.</span><span class="sxs-lookup"><span data-stu-id="7e515-391">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="7e515-392">Uppdaterade hjälpexempel för skapandet av policydefinition</span><span class="sxs-lookup"><span data-stu-id="7e515-392">Updated create policy definition help example</span></span>
- <span data-ttu-id="7e515-393">Åtgärda bugg i Remove-AZADServicePrincipal -ServicePrincipalName, utlös null-referens när tjänstens huvudnamn inte hittas.</span><span class="sxs-lookup"><span data-stu-id="7e515-393">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="7e515-394">Åtgärda bugg i New-AZADServicePrincipal, utlös null-referens när klientorganisationen inte har någon prenumeration.</span><span class="sxs-lookup"><span data-stu-id="7e515-394">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="7e515-395">Ändra New-AzAdServicePrincipal för att endast lägga till autentiseringsuppgifter för det associerade programmet.</span><span class="sxs-lookup"><span data-stu-id="7e515-395">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="7e515-396">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7e515-396">Az.Sql</span></span>
* <span data-ttu-id="7e515-397">Stöd har lagts till för databasen ReadReplicaCount.</span><span class="sxs-lookup"><span data-stu-id="7e515-397">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="7e515-398">Korrigerade Set-AzSqlDatabase när zonredundans inte har angetts</span><span class="sxs-lookup"><span data-stu-id="7e515-398">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="7e515-399">3.0.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="7e515-399">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="7e515-400">Allmänt</span><span class="sxs-lookup"><span data-stu-id="7e515-400">General</span></span>
* <span data-ttu-id="7e515-401">Az. PrivateDns 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="7e515-401">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7e515-402">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7e515-402">Az.Accounts</span></span>
* <span data-ttu-id="7e515-403">Lägg till ett utfasningsmeddelande för aliaset Resolve-error.</span><span class="sxs-lookup"><span data-stu-id="7e515-403">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="7e515-404">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="7e515-404">Az.Advisor</span></span>
* <span data-ttu-id="7e515-405">Den nya kategorin Operational Excellence har lagts till i cmdleten Get-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="7e515-405">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="7e515-406">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="7e515-406">Az.Batch</span></span>
* <span data-ttu-id="7e515-407">`CoreQuota` på `BatchAccountContext` har bytt namn till `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="7e515-407">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="7e515-408">Det finns även en ny `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="7e515-408">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="7e515-409">Detta påverkar **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="7e515-409">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="7e515-410">**New-AzBatchTask** `-ResourceFile`-parametern tar nu en samling `PSResourceFile`-objekt som kan skapas med hjälp av den nya cmdleten **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="7e515-410">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="7e515-411">Ny **New-AzBatchResourceFile**-cmdlet för att skapa `PSResourceFile`-objekt.</span><span class="sxs-lookup"><span data-stu-id="7e515-411">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="7e515-412">Dessa kan tillhandahållas till **New-AzBatchTask** på `-ResourceFile`-parametern.</span><span class="sxs-lookup"><span data-stu-id="7e515-412">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="7e515-413">Detta stöder två nya typer av resursfiler förutom det befintliga sättet med `HttpUrl`:</span><span class="sxs-lookup"><span data-stu-id="7e515-413">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="7e515-414">`AutoStorageContainerName`-baserade resursfiler laddar ned en hel container för automatisk lagring till Batch-noden.</span><span class="sxs-lookup"><span data-stu-id="7e515-414">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="7e515-415">`StorageContainerUrl`-baserade resursfiler laddar ned containern som anges i webbadressen till Batch-noden.</span><span class="sxs-lookup"><span data-stu-id="7e515-415">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="7e515-416">Tog bort egenskapen `ApplicationPackages` för `PSApplication` som returnerades av **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="7e515-416">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="7e515-417">Specifika paket i ett program kan nu hämtas med hjälp av **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="7e515-417">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="7e515-418">Till exempel: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="7e515-418">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="7e515-419">Bytt namn på `ApplicationId` till `ApplicationName` på **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** och **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="7e515-419">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="7e515-420">`ApplicationId` är nu ett alias för `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="7e515-420">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="7e515-421">Ny `PSWindowsUserConfiguration`-egenskap till `PSUserAccount` lades till.</span><span class="sxs-lookup"><span data-stu-id="7e515-421">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="7e515-422">Bytte namn på `Version` till `Name` på `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="7e515-422">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="7e515-423">Bytte namn på `BlobSource` till `HttpUrl` på `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="7e515-423">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="7e515-424">Tog bort egenskapen `OSDisk` från `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="7e515-424">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="7e515-425">Tog bort **Set-AzBatchPoolOSVersion**.</span><span class="sxs-lookup"><span data-stu-id="7e515-425">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="7e515-426">Den här åtgärden stöds inte längre.</span><span class="sxs-lookup"><span data-stu-id="7e515-426">This operation is no longer supported.</span></span>
* <span data-ttu-id="7e515-427">`TargetOSVersion` har tagits bort från `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="7e515-427">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="7e515-428">Bytte namn på `CurrentOSVersion` till `OSVersion` på `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="7e515-428">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="7e515-429">`DataEgressGiB` och `DataIngressGiB` har tagits bort från `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="7e515-429">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="7e515-430">Tog bort **Get-AzBatchNodeAgentSku** och ersatte det med **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="7e515-430">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span> 
  - <span data-ttu-id="7e515-431">**Get-AzBatchSupportedImage** returnerar samma data som **Get-AzBatchNodeAgentSku** men i ett mer användarvänligt format.</span><span class="sxs-lookup"><span data-stu-id="7e515-431">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="7e515-432">Nya icke-verifierade avbildningar returneras nu också.</span><span class="sxs-lookup"><span data-stu-id="7e515-432">New non-verified images are also now returned.</span></span> <span data-ttu-id="7e515-433">Ytterligare information om `Capabilities` och `BatchSupportEndOfLife` för varje avbildning inkluderas också.</span><span class="sxs-lookup"><span data-stu-id="7e515-433">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="7e515-434">Lade till möjlighet att montera fjärrfilsystem på varje nod i en pool via den nya parametern `MountConfiguration` för **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="7e515-434">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="7e515-435">Har nu stöd för nätverkssäkerhetsregler som blockerar nätverksåtkomst till en pool baserat på källportens trafik.</span><span class="sxs-lookup"><span data-stu-id="7e515-435">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="7e515-436">Detta görs via egenskapen `SourcePortRanges` på `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="7e515-436">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="7e515-437">När du kör en container stöder nu Batch körningen av uppgiften i arbetskatalogen för containern eller i arbetskatalogen för Batch-uppgiften.</span><span class="sxs-lookup"><span data-stu-id="7e515-437">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="7e515-438">Detta styrs av egenskapen `WorkingDirectory` på `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="7e515-438">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="7e515-439">Lade till en funktion för att ange en samling av offentliga IP-adresser på `PSNetworkConfiguration` via den nya egenskapen `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="7e515-439">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="7e515-440">Detta garanterar att noderna i poolen har en IP-adress från listan över IP-adresser som tillhandahållits av användare.</span><span class="sxs-lookup"><span data-stu-id="7e515-440">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="7e515-441">Om inget värde anges är standardvärdet för `WaitForSuccess` på `PSSTartTask` nu `$True` (var tidigare `$False`).</span><span class="sxs-lookup"><span data-stu-id="7e515-441">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="7e515-442">Om inget värde anges är standardvärdet för `Scope` på `PSAutoUserSpecification` nu `Pool` (var tidigare `Task` på Windows och `Pool` på Linux).</span><span class="sxs-lookup"><span data-stu-id="7e515-442">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="7e515-443">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7e515-443">Az.Cdn</span></span>
* <span data-ttu-id="7e515-444">Introducerade UrlRewriteAction och CacheKeyQueryStringAction till RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="7e515-444">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="7e515-445">Åtgärdade flera buggar, som saknade indata för ”väljare” i cmdleten New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="7e515-445">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7e515-446">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7e515-446">Az.Compute</span></span>
* <span data-ttu-id="7e515-447">Funktion för diskkrypteringsuppsättning</span><span class="sxs-lookup"><span data-stu-id="7e515-447">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="7e515-448">Nya cmdletar:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="7e515-448">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="7e515-449">Parametern DiskEncryptionSetId har lagts till i följande cmdletar: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="7e515-449">DiskEncryptionSetId parameter is added to the following cmdlets: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span></span>        
        <span data-ttu-id="7e515-450">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="7e515-450">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="7e515-451">Parametrarna DiskEncryptionSetId och EncryptionType har lagts till i följande cmdletar:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="7e515-451">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="7e515-452">Lägg till parametern PublicIPAddressVersion i New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="7e515-452">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="7e515-453">Flytta FileUris för anpassat skripttillägg från offentlig inställning till skyddad inställning</span><span class="sxs-lookup"><span data-stu-id="7e515-453">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="7e515-454">Lägg till ScaleInPolicy i cmdletarna New-AzVmss, New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7e515-454">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="7e515-455">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="7e515-455">Breaking changes</span></span>
    - <span data-ttu-id="7e515-456">Parametern UploadSizeInBytes används istället för DiskSizeGB för New-AzDiskConfig när CreateOption är Uppladdning</span><span class="sxs-lookup"><span data-stu-id="7e515-456">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="7e515-457">PublishingProfile.Source.ManagedImage.Id ersätts med StorageProfile.Source.Id i objektet GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="7e515-457">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7e515-458">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7e515-458">Az.DataFactory</span></span>
* <span data-ttu-id="7e515-459">Uppdatera ADF .Net SDK-versionen till 4.3.0</span><span class="sxs-lookup"><span data-stu-id="7e515-459">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7e515-460">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7e515-460">Az.DataLakeStore</span></span>
* <span data-ttu-id="7e515-461">Uppdatera ADLS SDK-version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) innehåller följande korrigeringar</span><span class="sxs-lookup"><span data-stu-id="7e515-461">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="7e515-462">Undvik att utlösa undantag när det inte går att deserialisera creationtime för inmatning av papperskorg eller katalog.</span><span class="sxs-lookup"><span data-stu-id="7e515-462">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="7e515-463">Gör inställning tillgänglig per tidsgräns för förfrågan i adlsclient</span><span class="sxs-lookup"><span data-stu-id="7e515-463">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="7e515-464">Korrigera överföringen av ursprunglig syncflag för badoffset-återställning</span><span class="sxs-lookup"><span data-stu-id="7e515-464">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="7e515-465">Korrigera EnumerateDirectory för att hämta fortsättningstoken när svar har kontrollerats</span><span class="sxs-lookup"><span data-stu-id="7e515-465">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="7e515-466">Korrigera bugg i Concat</span><span class="sxs-lookup"><span data-stu-id="7e515-466">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="7e515-467">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="7e515-467">Az.FrontDoor</span></span>
* <span data-ttu-id="7e515-468">Åtgärdade diverse stavfel i modul</span><span class="sxs-lookup"><span data-stu-id="7e515-468">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="7e515-469">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="7e515-469">Az.HDInsight</span></span>
* <span data-ttu-id="7e515-470">Korrigerade buggen att kunder får felet ”inte en giltig Base-64-sträng” vid användning av Get-AzHDInsightCluster för att hämta klustret med ADLSGen1-lagring.</span><span class="sxs-lookup"><span data-stu-id="7e515-470">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="7e515-471">Lägg till en parameter med namnet ”ApplicationId” i de tre cmdletarna Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig och New-AzHDInsightCluster så att kunden kan tillhandahålla tjänstens huvudnamn för program-ID för åtkomst till Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="7e515-471">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="7e515-472">Ändrade Microsoft.Azure.Management.HDInsight från 2.1.0 till 5.1.0</span><span class="sxs-lookup"><span data-stu-id="7e515-472">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="7e515-473">Fem cmdletar har tagits bort:</span><span class="sxs-lookup"><span data-stu-id="7e515-473">Removed five cmdlets:</span></span>
    - <span data-ttu-id="7e515-474">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="7e515-474">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="7e515-475">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="7e515-475">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="7e515-476">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="7e515-476">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="7e515-477">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="7e515-477">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="7e515-478">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="7e515-478">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="7e515-479">Tre cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="7e515-479">Added three cmdlets:</span></span>
    - <span data-ttu-id="7e515-480">Get-AzHDInsightMonitoring som ersätter Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="7e515-480">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="7e515-481">Enable-AzHDInsightMonitoring som ersätter Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="7e515-481">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="7e515-482">Disable-AzHDInsightMonitoring som ersätter Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="7e515-482">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="7e515-483">Korrigerade cmdleten Get-AzHDInsightProperties för att stödja hämtning av funktionsinformation från en viss plats.</span><span class="sxs-lookup"><span data-stu-id="7e515-483">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="7e515-484">Parameteruppsättningarna (Spark1 och Spark2) har tagits bort från Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="7e515-484">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="7e515-485">Lägg till exempel för cmdleten Add-AzHDInsightSecurityProfile till hjälpdokumenten.</span><span class="sxs-lookup"><span data-stu-id="7e515-485">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="7e515-486">Ändrade utdatatyp för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="7e515-486">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="7e515-487">Ändrade utdatatyp för Get-AzHDInsightProperties från CapabilitiesResponse till AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="7e515-487">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="7e515-488">Ändrade utdatatyp för Remove-AzHDInsightCluster från ClusterGetResponse till bool.</span><span class="sxs-lookup"><span data-stu-id="7e515-488">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="7e515-489">Ändrade utdatatyp för Set-AzHDInsightGatewaySettings HttpConnectivitySettings till GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="7e515-489">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="7e515-490">Lade till testfall för vissa scenarier.</span><span class="sxs-lookup"><span data-stu-id="7e515-490">Added some scenario test cases.</span></span>
* <span data-ttu-id="7e515-491">Ta bort vissa alias: Add-AzHDInsightConfigValues, Get-AzHDInsightProperties.</span><span class="sxs-lookup"><span data-stu-id="7e515-491">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7e515-492">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7e515-492">Az.IotHub</span></span>
* <span data-ttu-id="7e515-493">Icke-bakåtkompatibla ändringar:</span><span class="sxs-lookup"><span data-stu-id="7e515-493">Breaking changes:</span></span>
    - <span data-ttu-id="7e515-494">Cmdleten Add-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="7e515-494">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="7e515-495">Parameteruppsättningen __AllParameterSets för cmdleten Add-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="7e515-495">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="7e515-496">Cmdleten Get-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="7e515-496">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="7e515-497">Parameteruppsättningen __AllParameterSets för cmdleten Get-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="7e515-497">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="7e515-498">Egenskapen OperationsMonitoringProperties av typen Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="7e515-498">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="7e515-499">Egenskapen OperationsMonitoringProperties av typen Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="7e515-499">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="7e515-500">Cmdleten New-AzIotHubExportDevice stöder inte längre aliaset New-AzIotHubExportDevices.</span><span class="sxs-lookup"><span data-stu-id="7e515-500">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="7e515-501">Cmdleten New-AzIotHubImportDevice stöder inte längre aliaset New-AzIotHubImportDevices.</span><span class="sxs-lookup"><span data-stu-id="7e515-501">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="7e515-502">Cmdleten Remove-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="7e515-502">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="7e515-503">Parameteruppsättningen __AllParameterSets för cmdleten Remove-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="7e515-503">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="7e515-504">Cmdleten Set-AzIotHub har inte längre stöd för parametern OperationsMonitoringProperties och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="7e515-504">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="7e515-505">Parameteruppsättningen UpdateOperationsMonitoringProperties för cmdleten Set-AzIotHub har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="7e515-505">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7e515-506">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7e515-506">Az.RecoveryServices</span></span>
* <span data-ttu-id="7e515-507">Azure Site Recovery-stöd för att konfigurera nätverksresurser som NSG, offentliga IP-adresser och interna lastbalanserare för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="7e515-507">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="7e515-508">Azure Site Recovery-stöd för att skriva till hanterad disk för vMWare till Azure.</span><span class="sxs-lookup"><span data-stu-id="7e515-508">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="7e515-509">Azure Site Recovery-stöd för NIC-reduktion för vMWare till Azure.</span><span class="sxs-lookup"><span data-stu-id="7e515-509">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="7e515-510">Azure Site Recovery-stöd för accelererat nätverk för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="7e515-510">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="7e515-511">Azure Site Recovery-stöd för automatisk uppdatering av agent för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="7e515-511">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="7e515-512">Azure Site Recovery-stöd för Standard SSD för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="7e515-512">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="7e515-513">Azure Site Recovery-stöd för tvåstegskryptering i Azure Disk Encryption för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="7e515-513">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="7e515-514">Azure Site Recovery-stöd för att skydda nyligen tillagda diskar för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="7e515-514">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="7e515-515">En funktion för mjuk borttagning av virtuella datorer samt tester för mjuk borttagning har tagits bort</span><span class="sxs-lookup"><span data-stu-id="7e515-515">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="7e515-516">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7e515-516">Az.Resources</span></span>
* <span data-ttu-id="7e515-517">Uppdatera beroendesammansättning för Microsoft.Extensions.Caching.Memory från 1.1.1 till 2.2</span><span class="sxs-lookup"><span data-stu-id="7e515-517">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7e515-518">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7e515-518">Az.Network</span></span>
* <span data-ttu-id="7e515-519">Ändra alla cmdletar för PrivateEndpointConnection så att de stöder generiska tjänstleverantörer.</span><span class="sxs-lookup"><span data-stu-id="7e515-519">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="7e515-520">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="7e515-520">Updated cmdlet:</span></span>
        - <span data-ttu-id="7e515-521">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7e515-521">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="7e515-522">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7e515-522">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="7e515-523">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7e515-523">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="7e515-524">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7e515-524">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="7e515-525">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7e515-525">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="7e515-526">Lägg till ny cmdlet för PrivateLinkResource så att det också stöder generiska tjänstleverantörer.</span><span class="sxs-lookup"><span data-stu-id="7e515-526">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="7e515-527">Ny cmdlet:</span><span class="sxs-lookup"><span data-stu-id="7e515-527">New cmdlet:</span></span>
        - <span data-ttu-id="7e515-528">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="7e515-528">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="7e515-529">Lägg till nya fält och parametrar för funktionen Proxy Protocol V2.</span><span class="sxs-lookup"><span data-stu-id="7e515-529">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="7e515-530">Lägg till egenskapen EnableProxyProtocol i PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7e515-530">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="7e515-531">Lägg till egenskapen LinkIdentifier i PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7e515-531">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="7e515-532">Uppdaterade New-AzPrivateLinkService för att lägga till den nya valfria parametern EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="7e515-532">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="7e515-533">Korrigera felaktig beskrivning av parameter i referensdokumentationen för New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="7e515-533">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="7e515-534">Nya cmdletar som stöder Azure-brandväggsprincipen</span><span class="sxs-lookup"><span data-stu-id="7e515-534">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="7e515-535">Lägg till stöd för den underordnade resursen RouteTables för VirtualHub</span><span class="sxs-lookup"><span data-stu-id="7e515-535">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="7e515-536">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="7e515-536">New cmdlets added:</span></span>
        - <span data-ttu-id="7e515-537">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="7e515-537">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="7e515-538">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="7e515-538">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="7e515-539">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="7e515-539">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="7e515-540">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="7e515-540">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="7e515-541">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="7e515-541">Set-AzVirtualHub</span></span>
* <span data-ttu-id="7e515-542">Lägg till stöd för ny egenskaps-SKU för VirtualHub och VirtualWANType för VirtualWan</span><span class="sxs-lookup"><span data-stu-id="7e515-542">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="7e515-543">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="7e515-543">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="7e515-544">New-AzVirtualHub: lade till parameter-SKU</span><span class="sxs-lookup"><span data-stu-id="7e515-544">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="7e515-545">Update-AzVirtualHub: lade till parameter-SKU</span><span class="sxs-lookup"><span data-stu-id="7e515-545">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="7e515-546">New-AzVirtualWan: lade till parametern VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="7e515-546">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="7e515-547">Update-AzVirtualWan: lade till parametern VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="7e515-547">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="7e515-548">Lägg till stöd för egenskapen EnableInternetSecurity för HubVnetConnection, VpnConnection och ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="7e515-548">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="7e515-549">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="7e515-549">New cmdlets added:</span></span>
        - <span data-ttu-id="7e515-550">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="7e515-550">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="7e515-551">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="7e515-551">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="7e515-552">New-AzureRmVirtualHubVnetConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e515-552">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="7e515-553">New-AzureRmVpnConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e515-553">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="7e515-554">Update-AzureRmVpnConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e515-554">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="7e515-555">New-AzureRmExpressRouteConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e515-555">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="7e515-556">Set-AzureRmExpressRouteConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e515-556">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="7e515-557">Lägg till stöd för att konfigurera TopLevel WebApplicationFirewall-princip</span><span class="sxs-lookup"><span data-stu-id="7e515-557">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="7e515-558">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="7e515-558">New cmdlets added:</span></span>
        - <span data-ttu-id="7e515-559">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="7e515-559">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="7e515-560">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="7e515-560">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="7e515-561">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="7e515-561">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="7e515-562">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="7e515-562">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="7e515-563">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="7e515-563">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="7e515-564">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="7e515-564">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="7e515-565">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="7e515-565">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="7e515-566">New-AzApplicationGatewayFirewallPolicy: parametrarna PolicySetting, ManagedRule har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e515-566">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="7e515-567">Stöd för operator för geomatchning har lagts till på CustomRule</span><span class="sxs-lookup"><span data-stu-id="7e515-567">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="7e515-568">Geomatchning har lagts till i operatorn på FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="7e515-568">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="7e515-569">Stöd har lagts till för brandväggsprinciperna perListener och perSite</span><span class="sxs-lookup"><span data-stu-id="7e515-569">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="7e515-570">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="7e515-570">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="7e515-571">New-AzApplicationGatewayHttpListener: parametrarna FirewallPolicy, FirewallPolicyId har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e515-571">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="7e515-572">New-AzApplicationGatewayPathRuleConfig: parametrarna FirewallPolicy, FirewallPolicyId har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e515-572">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="7e515-573">Åtgärdat så att nödvändigt undernät med namnet AzureBastionSubnet i PSBastion kan vara skiftlägesokänsligt</span><span class="sxs-lookup"><span data-stu-id="7e515-573">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="7e515-574">Stöd för mål-FQDN:er i nätverksregler och översatt FQDN i NAT-regler för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="7e515-574">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="7e515-575">Lägg till stöd för resursen RouteTables för IpGroup på den högsta nivån</span><span class="sxs-lookup"><span data-stu-id="7e515-575">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="7e515-576">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="7e515-576">New cmdlets added:</span></span>
        - <span data-ttu-id="7e515-577">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="7e515-577">New-AzIpGroup</span></span>
        - <span data-ttu-id="7e515-578">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="7e515-578">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="7e515-579">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="7e515-579">Get-AzIpGroup</span></span>
        - <span data-ttu-id="7e515-580">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="7e515-580">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="7e515-581">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7e515-581">Az.ServiceFabric</span></span>
* <span data-ttu-id="7e515-582">Ta bort cmdleten Add-AzServiceFabricApplicationCertificate eftersom det här scenariot omfattas av Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="7e515-582">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="7e515-583">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7e515-583">Az.Sql</span></span>
* <span data-ttu-id="7e515-584">Stöd har lagts till för återställning av utelämnade databaser på hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="7e515-584">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="7e515-585">Inaktuella gamla cmdletar för granskning från kod.</span><span class="sxs-lookup"><span data-stu-id="7e515-585">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="7e515-586">Tog bort inaktuella alias:</span><span class="sxs-lookup"><span data-stu-id="7e515-586">Removed deprecated aliases:</span></span>
* <span data-ttu-id="7e515-587">Get-AzSqlDatabaseIndexRecommendations (använd Get-AzSqlDatabaseIndexRecommendation istället)</span><span class="sxs-lookup"><span data-stu-id="7e515-587">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="7e515-588">Get-AzSqlDatabaseRestorePoints (använd Get-AzSqlDatabaseRestorePoint istället)</span><span class="sxs-lookup"><span data-stu-id="7e515-588">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="7e515-589">Ta bort cmdleten Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="7e515-589">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="7e515-590">Ta bort alias för inaktuella cmdletar för inställningar för utvärdering av säkerhetsrisk</span><span class="sxs-lookup"><span data-stu-id="7e515-590">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="7e515-591">Inaktualisera cmdletar för inställningar för avancerad hotidentifiering</span><span class="sxs-lookup"><span data-stu-id="7e515-591">Deprecate Advanced Threat Detection Settings cmdlets</span></span> 
* <span data-ttu-id="7e515-592">Lägga till cmdletar för att inaktivera och aktivera känslighetsrekommendationer på kolumner i en databas.</span><span class="sxs-lookup"><span data-stu-id="7e515-592">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7e515-593">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7e515-593">Az.Storage</span></span>
* <span data-ttu-id="7e515-594">Stöd för att aktivera stora filresurser vid skapande eller uppdatering av lagringskonto</span><span class="sxs-lookup"><span data-stu-id="7e515-594">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="7e515-595">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7e515-595">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="7e515-596">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7e515-596">Set-AzStorageAccount</span></span>
* <span data-ttu-id="7e515-597">När du stänger/hämtar en filreferens kan du hoppa över kontrollen av huruvida indatasökvägen är en filkatalog eller en fil för att undvika problem med objekt som har status DeletePending</span><span class="sxs-lookup"><span data-stu-id="7e515-597">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="7e515-598">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="7e515-598">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="7e515-599">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="7e515-599">Close-AzStorageFileHandle</span></span>
    
## <a name="280---october-2019"></a><span data-ttu-id="7e515-600">2.8.0 – oktober 2019</span><span class="sxs-lookup"><span data-stu-id="7e515-600">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="7e515-601">Allmänt</span><span class="sxs-lookup"><span data-stu-id="7e515-601">General</span></span>
* <span data-ttu-id="7e515-602">AZ. HealthcareApis 1.0.0-version</span><span class="sxs-lookup"><span data-stu-id="7e515-602">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7e515-603">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7e515-603">Az.Accounts</span></span>
* <span data-ttu-id="7e515-604">Uppdatera telemetri och URL-omskrivning för genererade moduler, korrigera Windows-enhetstester.</span><span class="sxs-lookup"><span data-stu-id="7e515-604">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="7e515-605">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7e515-605">Az.ApiManagement</span></span>
* <span data-ttu-id="7e515-606">**Set-AzApiManagementApi** – Tillagt stöd för att uppdatera Api till ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="7e515-606">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="7e515-607">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="7e515-607">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7e515-608">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7e515-608">Az.Automation</span></span>
* <span data-ttu-id="7e515-609">Åtgärdade cmdleten New-AzureAutomationSoftwareUpdateConfiguration för parametern för inställning av Linux-omstart.</span><span class="sxs-lookup"><span data-stu-id="7e515-609">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="7e515-610">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="7e515-610">Az.Batch</span></span>
* <span data-ttu-id="7e515-611">**Get-AzBatchNodeAgentSku** är inaktuell och ersätts av **Get-AzBatchSupportImage** i version 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="7e515-611">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7e515-612">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7e515-612">Az.Compute</span></span>
* <span data-ttu-id="7e515-613">Lägg till parametrarna Priority, EvictionPolicy och MaxPrice till cmdletarna New-AzVM och New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7e515-613">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="7e515-614">Korrigera varningsmeddelande och hjälpdokument för cmdletarna Add-AzVMAdditionalUnattendContent och Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="7e515-614">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="7e515-615">Åtgärda – skipVmBackup-undantag för virtuella Linux-datorer med hanterade diskar för Set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="7e515-615">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="7e515-616">Åtgärda fel i uppdatera krypteringsinställningarna i set-AzVMDiskEncryptionExtension, scenario i två steg.</span><span class="sxs-lookup"><span data-stu-id="7e515-616">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7e515-617">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7e515-617">Az.DataFactory</span></span>
* <span data-ttu-id="7e515-618">Lägga till CRUD-kommandon för ADF V2-dataflödet: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow och Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="7e515-618">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="7e515-619">Lägger till åtgärdskommandon för ADF V2-dataflödesfelsökningssession: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand och Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="7e515-619">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="7e515-620">Uppdatera ADF .Net SDK-versionen till 4.2.0</span><span class="sxs-lookup"><span data-stu-id="7e515-620">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7e515-621">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7e515-621">Az.DataLakeStore</span></span>
* <span data-ttu-id="7e515-622">Korrigera kontovalidering så att konton med ”-” kan skickas utan domän</span><span class="sxs-lookup"><span data-stu-id="7e515-622">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="7e515-623">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="7e515-623">Az.HealthcareApis</span></span>
* <span data-ttu-id="7e515-624">PowerShell-versionen har uppdaterats till 1.0.0</span><span class="sxs-lookup"><span data-stu-id="7e515-624">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="7e515-625">Uppdaterade SDK-versionen till 1.0.2</span><span class="sxs-lookup"><span data-stu-id="7e515-625">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="7e515-626">Uppdatera i tester för att referera till en ny SDK-version</span><span class="sxs-lookup"><span data-stu-id="7e515-626">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="7e515-627">Utdatastrukturen har uppdaterats från kapslad till förenklad.</span><span class="sxs-lookup"><span data-stu-id="7e515-627">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7e515-628">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7e515-628">Az.IotHub</span></span>
* <span data-ttu-id="7e515-629">Lägg till ny routningskälla: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="7e515-629">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="7e515-630">Mindre felkorrigering: Get-AzIothub returnerar inte subscriptionId</span><span class="sxs-lookup"><span data-stu-id="7e515-630">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="7e515-631">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7e515-631">Az.Monitor</span></span>
* <span data-ttu-id="7e515-632">Nya åtgärdsgruppsmottagare har lagts till för åtgärdsgrupp   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="7e515-632">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="7e515-633">Använd vanligt aviseringsschema som är aktiverat för mottagarna.</span><span class="sxs-lookup"><span data-stu-id="7e515-633">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="7e515-634">Detta gäller inte för SMS, push för Azure-app, ITSM och röstmottagare</span><span class="sxs-lookup"><span data-stu-id="7e515-634">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="7e515-635">Webhooks har nu stöd för Azure Active Directory-autentisering.</span><span class="sxs-lookup"><span data-stu-id="7e515-635">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7e515-636">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7e515-636">Az.Network</span></span>
* <span data-ttu-id="7e515-637">Lägg till ny cmdlet Get-AzAvailableServiceAlias som kan anropas för att hämta de alias som kan användas för tjänstslutpunktsprinciper.</span><span class="sxs-lookup"><span data-stu-id="7e515-637">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="7e515-638">Stöd för tillägg av trafikväljare har lagts till i gatewayanslutningar för virtuella nätverk</span><span class="sxs-lookup"><span data-stu-id="7e515-638">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="7e515-639">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="7e515-639">New cmdlets added:</span></span>
        - <span data-ttu-id="7e515-640">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="7e515-640">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="7e515-641">Cmdletar har uppdaterats med valfri parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7e515-641">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="7e515-642">Lägg till stöd för ESP- och AH-protokoll i konfiguration av nätverkssäkerhetsregler</span><span class="sxs-lookup"><span data-stu-id="7e515-642">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="7e515-643">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="7e515-643">Updated cmdlets:</span></span>
        - <span data-ttu-id="7e515-644">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7e515-644">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="7e515-645">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7e515-645">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="7e515-646">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7e515-646">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="7e515-647">Förbättra hanteringen av undantag i Cortex-cmdletar</span><span class="sxs-lookup"><span data-stu-id="7e515-647">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="7e515-648">Nya generationer och SKU:er för VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="7e515-648">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="7e515-649">Introducera nya generationer för VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="7e515-649">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="7e515-650">Introducera nya SKU:er med högt dataflöde för VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="7e515-650">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="7e515-651">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="7e515-651">Az.RedisCache</span></span>
* <span data-ttu-id="7e515-652">Uppdaterad referensdokumentation för ”set-AzRedisCache” för att inkludera saknade värden för parametern ”size”</span><span class="sxs-lookup"><span data-stu-id="7e515-652">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="7e515-653">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7e515-653">Az.Sql</span></span>
* <span data-ttu-id="7e515-654">Lägg till stöd för inställningen Active Directory administratör på den hanterade instansen</span><span class="sxs-lookup"><span data-stu-id="7e515-654">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7e515-655">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7e515-655">Az.Storage</span></span>
* <span data-ttu-id="7e515-656">Uppdatera Lagringsklientbibliotek till 11.1.0</span><span class="sxs-lookup"><span data-stu-id="7e515-656">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="7e515-657">Lista containrar med hanteringsplans-API, kommer att listas med NextPageLink</span><span class="sxs-lookup"><span data-stu-id="7e515-657">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="7e515-658">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="7e515-658">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="7e515-659">Lista lagringskonton från prenumerationen, kommer att listas med NextPageLink</span><span class="sxs-lookup"><span data-stu-id="7e515-659">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="7e515-660">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7e515-660">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="7e515-661">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="7e515-661">Az.StorageSync</span></span>
* <span data-ttu-id="7e515-662">Åtgärda problemet 9810 i Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="7e515-662">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7e515-663">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7e515-663">Az.Websites</span></span>
* <span data-ttu-id="7e515-664">Set-AzWebApp – uppdatering av ASP för en app misslyckades</span><span class="sxs-lookup"><span data-stu-id="7e515-664">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="7e515-665">2.7.0 – september 2019</span><span class="sxs-lookup"><span data-stu-id="7e515-665">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="7e515-666">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7e515-666">Az.ApiManagement</span></span>
* <span data-ttu-id="7e515-667">Uppdatera ”-Format”-parameterbeskrivningen i ”Set-AzApiManagementPolicy”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="7e515-667">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="7e515-668">Referenser för den föråldrade cmdleten ”Update-AzApiManagementDeployment” har tagits bort från referensdokumentationen.</span><span class="sxs-lookup"><span data-stu-id="7e515-668">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="7e515-669">Använd ”Set-AzApiManagement” i stället.</span><span class="sxs-lookup"><span data-stu-id="7e515-669">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7e515-670">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7e515-670">Az.Automation</span></span>
* <span data-ttu-id="7e515-671">Stavfel har korrigerats i exempel i referensdokumentationen för ”Register-AzAutomationDscNode”</span><span class="sxs-lookup"><span data-stu-id="7e515-671">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="7e515-672">Klargörande har lagts till om OS-begränsningar för Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="7e515-672">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="7e515-673">Null-referensundantag har korrigerats för -Wait-alternativet i Start-AzAutomationRunbook-cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7e515-673">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7e515-674">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7e515-674">Az.Compute</span></span>
* <span data-ttu-id="7e515-675">Lägg till UploadSizeInBytes-parameter till New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="7e515-675">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="7e515-676">Lägg till Incremental-parameter till New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="7e515-676">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="7e515-677">Lägg till en funktion för virtuella datorer med låg prioritet:</span><span class="sxs-lookup"><span data-stu-id="7e515-677">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="7e515-678">MaxPrice-, EvictionPolicy- och Priority-parametrar har lagts till i New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="7e515-678">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="7e515-679">MaxPrice-parametern har lagts till i New-AzVmssConfig-, Update-AzVM- och Update-AzVmss-cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="7e515-679">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="7e515-680">Åtgärda problem med VM-referenser för Get-AzAvailabilitySet-cmdleten när alla tillgänglighetsuppsättningar i prenumerationen visas.</span><span class="sxs-lookup"><span data-stu-id="7e515-680">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="7e515-681">Korrigera null-undantaget för Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="7e515-681">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="7e515-682">Korrigera VHD-metoden för sökning relativt till slut.</span><span class="sxs-lookup"><span data-stu-id="7e515-682">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="7e515-683">Åtgärda UltraSSD-problem för New-AzVM och Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="7e515-683">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7e515-684">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7e515-684">Az.DataFactory</span></span>
* <span data-ttu-id="7e515-685">Lägger till 3 nya kommandon för ADF V2 – Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription och Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="7e515-685">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="7e515-686">ADF .Net SDK har uppdaterats till 4.1.3</span><span class="sxs-lookup"><span data-stu-id="7e515-686">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="7e515-687">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="7e515-687">Az.HDInsight</span></span>
* <span data-ttu-id="7e515-688">Anrop för icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="7e515-688">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7e515-689">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7e515-689">Az.IotHub</span></span>
* <span data-ttu-id="7e515-690">Lägg till stöd för att anropa redundans för en IotHub till den geo-länkade katastrofåterställningsregionen.</span><span class="sxs-lookup"><span data-stu-id="7e515-690">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="7e515-691">Lägg till stöd för att hantera meddelandeberikning för en IotHub.</span><span class="sxs-lookup"><span data-stu-id="7e515-691">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="7e515-692">Nya cmdlet:ar är:</span><span class="sxs-lookup"><span data-stu-id="7e515-692">New cmdlets are:</span></span>
    - <span data-ttu-id="7e515-693">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="7e515-693">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="7e515-694">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="7e515-694">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="7e515-695">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="7e515-695">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="7e515-696">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="7e515-696">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7e515-697">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7e515-697">Az.Monitor</span></span>
* <span data-ttu-id="7e515-698">Pekar på den senaste Monitor SDK:n, dvs. 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="7e515-698">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="7e515-699">Lägger till bakåtkompatibla ändringar i Metrics-cmdletarna, dvs. enhetsuppräkningen stöder flera nya värden.</span><span class="sxs-lookup"><span data-stu-id="7e515-699">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="7e515-700">Detta är skrivskyddade cmdletar, så det förekommer inga ändringar i inmatningen för cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="7e515-700">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="7e515-701">API-versionen för **ActionGroups**-begäranden är nu **2019-06-01**. Tidigare var den **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="7e515-701">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="7e515-702">Test av scenarier har uppdaterats för att anpassas till den här ändringen.</span><span class="sxs-lookup"><span data-stu-id="7e515-702">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="7e515-703">Ett nytt obligatoriskt argument har lagts till för konstruktorerna för klasserna **EmailReceiver** och **WebhookReceiver** – ett booleskt värde med namnet **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="7e515-703">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="7e515-704">Värdet är för närvarande fast till **false** så att den här icke-bakåtkompatibla ändringen är dold från cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="7e515-704">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="7e515-705">**Obs!** Det här är en tillfällig ändring som måste verifieras av Alerts-teamet.</span><span class="sxs-lookup"><span data-stu-id="7e515-705">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="7e515-706">Ordningen på argumenten för konstruktorn för klassen **Source** (relaterad till klassen **ScheduledQueryRuleSource**) har ändrats från den tidigare SDK:n.</span><span class="sxs-lookup"><span data-stu-id="7e515-706">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="7e515-707">Den här ändringen krävde korrigering av två enhetstest: de kompilerades, men testerna skickades inte.</span><span class="sxs-lookup"><span data-stu-id="7e515-707">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="7e515-708">Ordningen på argumenten för konstruktorn för klassen **AlertingAction** (relaterad till klassen **ScheduledQueryRuleSource**) har ändrats från den tidigare SDK:n.</span><span class="sxs-lookup"><span data-stu-id="7e515-708">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="7e515-709">Den här ändringen krävde korrigering av två enhetstest: de kompilerades, men testerna skickades inte.</span><span class="sxs-lookup"><span data-stu-id="7e515-709">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="7e515-710">Stöd för kriterier för dynamiskt tröskelvärde för måttavisering v2</span><span class="sxs-lookup"><span data-stu-id="7e515-710">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="7e515-711">New-AzMetricAlertRuleV2Criteria: skapar nu även kriterier för dynamiskt tröskelvärde</span><span class="sxs-lookup"><span data-stu-id="7e515-711">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="7e515-712">Add-AzMetricAlertRuleV2: accepterar nu även kriterier för dynamiskt tröskelvärde</span><span class="sxs-lookup"><span data-stu-id="7e515-712">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="7e515-713">Förbättringar i schemalagd frågeregel (SQR)</span><span class="sxs-lookup"><span data-stu-id="7e515-713">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="7e515-714">Cmdletar accepterar ”Location”-parameter i båda formaten, antingen platsen (t.ex. eastus) eller platsens visningsnamn (t.ex. USA, östra)</span><span class="sxs-lookup"><span data-stu-id="7e515-714">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="7e515-715">”Enabled”-parametern illustreras korrekt i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="7e515-715">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="7e515-716">Exempel för den valfria parametern ”ActionGroup” har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e515-716">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="7e515-717">Förbättrade hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="7e515-717">Overall improved help files</span></span>
* <span data-ttu-id="7e515-718">Åtgärda bugg då omfattningstypen fastställs för ”Set-AzActionRule”</span><span class="sxs-lookup"><span data-stu-id="7e515-718">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7e515-719">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7e515-719">Az.Network</span></span>
* <span data-ttu-id="7e515-720">Korrigera felaktigt exempel i referensdokumentationen för ”New-AzApplicationGateway”</span><span class="sxs-lookup"><span data-stu-id="7e515-720">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="7e515-721">Lägg till anmärkning i ”Get-AzNetworkWatcherPacketCapture”-referensdokumentationen om hämtning av alla egenskaper för en paketinsamling</span><span class="sxs-lookup"><span data-stu-id="7e515-721">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="7e515-722">Exempel har korrigerats i ”Test-AzNetworkWatcherIPFlow”-referensdokumentationen för korrekt uppräkning av nätverkskort</span><span class="sxs-lookup"><span data-stu-id="7e515-722">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="7e515-723">Förbättrad tolkning av molnundantag för att visa eventuell ytterligare information</span><span class="sxs-lookup"><span data-stu-id="7e515-723">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="7e515-724">Förbättrad tolkning av molnundantag för att hantera ytterligare en typ av SDK-undantag</span><span class="sxs-lookup"><span data-stu-id="7e515-724">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="7e515-725">Felaktig mappning av säkerhetsregelmodeller har korrigerats</span><span class="sxs-lookup"><span data-stu-id="7e515-725">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="7e515-726">Egenskaper har lagts till för nätverksgränssnittet för funktionen Privat IP</span><span class="sxs-lookup"><span data-stu-id="7e515-726">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="7e515-727">Egenskapen ”PrivateEndpoint” har lagts till som en typ av PSResourceId till PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="7e515-727">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="7e515-728">Egenskapen ”PrivateLinkConnectionProperties” har lagts till som en typ av PSIpConfigurationConnectivityInformation till PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="7e515-728">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="7e515-729">Modellklassen PSIpConfigurationConnectivityInformation har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e515-729">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="7e515-730">ApplicationRuleProtocolType ”mssql” har lagts till för Azure Firewall-resurs</span><span class="sxs-lookup"><span data-stu-id="7e515-730">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="7e515-731">MultiLink-stöd i virtuellt WAN</span><span class="sxs-lookup"><span data-stu-id="7e515-731">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="7e515-732">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="7e515-732">New cmdlets</span></span>
        - <span data-ttu-id="7e515-733">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="7e515-733">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="7e515-734">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="7e515-734">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="7e515-735">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="7e515-735">Updated cmdlet:</span></span>
        - <span data-ttu-id="7e515-736">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="7e515-736">New-VpnSite</span></span>
        - <span data-ttu-id="7e515-737">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="7e515-737">Update-VpnSite</span></span>
        - <span data-ttu-id="7e515-738">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="7e515-738">New-VpnConnection</span></span>
        - <span data-ttu-id="7e515-739">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="7e515-739">Update-VpnConnection</span></span>
* <span data-ttu-id="7e515-740">Dokument för vissa PowerShell-exempel har korrigerats så att Az-cmdletar används i stället för AzureRM-cmdletar</span><span class="sxs-lookup"><span data-stu-id="7e515-740">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7e515-741">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7e515-741">Az.RecoveryServices</span></span>
* <span data-ttu-id="7e515-742">Uppdatera AzureVMpolicy-objekt med ProtectedItemsCount-attribut</span><span class="sxs-lookup"><span data-stu-id="7e515-742">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="7e515-743">Ytterligare tester har lagts till för VM-princip och återställning av ursprungligt lagringskonto</span><span class="sxs-lookup"><span data-stu-id="7e515-743">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="7e515-744">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7e515-744">Az.Resources</span></span>
* <span data-ttu-id="7e515-745">Åtgärda fel där det inte gick att anropa New-AzRoleAssignment utan parametern Scope.</span><span class="sxs-lookup"><span data-stu-id="7e515-745">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="7e515-746">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7e515-746">Az.ServiceFabric</span></span>
* <span data-ttu-id="7e515-747">Stavfel har korrigerats i exempel för ”Update-AzServiceFabricReliability”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="7e515-747">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="7e515-748">Lägger till nya cmdletar för att hantera program och tjänster:</span><span class="sxs-lookup"><span data-stu-id="7e515-748">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="7e515-749">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="7e515-749">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="7e515-750">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="7e515-750">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="7e515-751">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="7e515-751">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="7e515-752">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="7e515-752">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="7e515-753">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="7e515-753">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="7e515-754">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="7e515-754">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="7e515-755">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="7e515-755">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="7e515-756">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="7e515-756">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="7e515-757">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="7e515-757">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="7e515-758">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="7e515-758">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="7e515-759">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="7e515-759">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="7e515-760">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="7e515-760">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="7e515-761">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="7e515-761">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="7e515-762">Service Fabric SDK har uppgraderats till version 1.2.0 som använder Service Fabric-resursprovidern med API-version 2019-03-01.</span><span class="sxs-lookup"><span data-stu-id="7e515-762">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="7e515-763">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="7e515-763">Az.SignalR</span></span>
* <span data-ttu-id="7e515-764">Lägg till Update-, Restart-, CheckNameAvailability- och GetUsage-cmdletar</span><span class="sxs-lookup"><span data-stu-id="7e515-764">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="7e515-765">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7e515-765">Az.Sql</span></span>
* <span data-ttu-id="7e515-766">Uppdatera exempel i referensdokumentationen för ”Get-AzSqlElasticPool”</span><span class="sxs-lookup"><span data-stu-id="7e515-766">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="7e515-767">vCore-exempel för att skapa en elastisk pool (New-AzSqlElasticPool) har lagts till.</span><span class="sxs-lookup"><span data-stu-id="7e515-767">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="7e515-768">Ta bort verifieringen av EmailAddresses och kontrollen som bekräftar att EmailAdmins inte är falskt när EmailAddresses är tomt i Set-AzSqlServerAdvancedThreatProtectionPolicy och Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="7e515-768">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="7e515-769">Server-/databasgranskningsinställningar kan tas bort när det finns flera diagnostikinställningar som aktiverar granskningskategorin.</span><span class="sxs-lookup"><span data-stu-id="7e515-769">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="7e515-770">Åtgärda verifiering av e-postadresser i flera Sql Vulnerability Assessment-cmdletar (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting och Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="7e515-770">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7e515-771">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7e515-771">Az.Storage</span></span>
* <span data-ttu-id="7e515-772">Exempel i referensdokumentationen för ”Get-AzStorageAccountKey” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="7e515-772">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="7e515-773">Vid upp- och nedladdning av en Azure-fil kan SMB-egenskaperna för källfilen (t.ex. filattribut, tidpunkten då filen skapades och tidpunkten för den senaste skrivningen) sparas i målfilen</span><span class="sxs-lookup"><span data-stu-id="7e515-773">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="7e515-774">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="7e515-774">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="7e515-775">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="7e515-775">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="7e515-776">Korrigera problem med uppladdningen av blockblob med egenskaper/metadata för ImmutabilityPolicy i containrar.</span><span class="sxs-lookup"><span data-stu-id="7e515-776">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="7e515-777">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="7e515-777">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="7e515-778">Stöd för hantering av Azure-filresurser med API för hanteringsplan</span><span class="sxs-lookup"><span data-stu-id="7e515-778">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="7e515-779">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="7e515-779">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="7e515-780">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="7e515-780">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="7e515-781">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="7e515-781">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="7e515-782">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="7e515-782">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7e515-783">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7e515-783">Az.Websites</span></span>
* <span data-ttu-id="7e515-784">Åtgärdar problemet där webapp-taggar togs bort när appen migrerades till nya ASP</span><span class="sxs-lookup"><span data-stu-id="7e515-784">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="7e515-785">Åtgärda Publish-AzureWebapp så att det fungerar i Linux och Windows</span><span class="sxs-lookup"><span data-stu-id="7e515-785">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="7e515-786">Uppdatera exempel i ”Get-AzWebAppPublishingProfile”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="7e515-786">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="7e515-787">2.6.0 – augusti 2019</span><span class="sxs-lookup"><span data-stu-id="7e515-787">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="7e515-788">Allmänt</span><span class="sxs-lookup"><span data-stu-id="7e515-788">General</span></span>
* <span data-ttu-id="7e515-789">Åtgärdade diverse skrivfel i flera moduler</span><span class="sxs-lookup"><span data-stu-id="7e515-789">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7e515-790">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7e515-790">Az.Accounts</span></span>
* <span data-ttu-id="7e515-791">Stöd för användartilldelat MSI i Azure Functions-autentisering (#9479)</span><span class="sxs-lookup"><span data-stu-id="7e515-791">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="7e515-792">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="7e515-792">Az.Aks</span></span>
* <span data-ttu-id="7e515-793">Åtgärda problem med utdata för "Get-AzAks"</span><span class="sxs-lookup"><span data-stu-id="7e515-793">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="7e515-794">Mer information här: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="7e515-794">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="7e515-795">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7e515-795">Az.ApiManagement</span></span>
* <span data-ttu-id="7e515-796">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="7e515-796">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="7e515-797">Uppdatera .net-NuGet-versionen, som inte tillämpar begränsningar för productId, apiId och userId</span><span class="sxs-lookup"><span data-stu-id="7e515-797">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="7e515-798">**Get-AzApiManagementProduct** – Lade till stöd för frågekörning mot produkter via API.</span><span class="sxs-lookup"><span data-stu-id="7e515-798">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="7e515-799">**New-AzApiManagementApiRevision** – Korrigering för problem där ApiRevisionDescription inte angavs vid skapande av ny API-revision https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="7e515-799">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="7e515-800">Åtgärdade skrivfel i modellen "PsApiManagementOAuth2AuthrozationServer" till "PsApiManagementOAuth2AuthorizationServer"</span><span class="sxs-lookup"><span data-stu-id="7e515-800">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="7e515-801">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="7e515-801">Az.Batch</span></span>
* <span data-ttu-id="7e515-802">Åtgärdade skrivfel i hjälpmeddelande och dokumentation till att skriva Windows med versaler</span><span class="sxs-lookup"><span data-stu-id="7e515-802">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="7e515-803">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7e515-803">Az.Cdn</span></span>
* <span data-ttu-id="7e515-804">Åtgärdade skrivfel i CDN-modulens konverteringshjälp</span><span class="sxs-lookup"><span data-stu-id="7e515-804">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7e515-805">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7e515-805">Az.Compute</span></span>
* <span data-ttu-id="7e515-806">Lägg till VmssId i New-AzVMConfig-cmdleten</span><span class="sxs-lookup"><span data-stu-id="7e515-806">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="7e515-807">Lägg till parametrarna TerminateScheduledEvents och TerminateScheduledEventNotBeforeTimeoutInMinutes i New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7e515-807">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="7e515-808">Lägg till egenskapen HyperVGeneration till avbildningsobjekt för virtuell dator</span><span class="sxs-lookup"><span data-stu-id="7e515-808">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="7e515-809">Lägg till funktioner för Host och HostGroup</span><span class="sxs-lookup"><span data-stu-id="7e515-809">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="7e515-810">Nya cmdletar:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="7e515-810">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="7e515-811">HostId-parametern läggs till i New-AzVMConfig och New-AzVM</span><span class="sxs-lookup"><span data-stu-id="7e515-811">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="7e515-812">Uppdatera exempel i "Invoke-AzVMRunCommand"-dokumentationen till att använda rätt parameternamn</span><span class="sxs-lookup"><span data-stu-id="7e515-812">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="7e515-813">Uppdatera "-VolumeType"-beskrivningen i referensdokumentationen för "set-AzVMDiskEncryptionExtension" och "set-AzVmssDiskEncryptionExtension"</span><span class="sxs-lookup"><span data-stu-id="7e515-813">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7e515-814">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7e515-814">Az.DataFactory</span></span>
* <span data-ttu-id="7e515-815">Åtgärda skrivfel till att använda versaler för "Windows" i "New-AzDataFactoryEncryptValue"-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="7e515-815">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="7e515-816">Uppdaterade ADF .Net SDK-versionen till 4.1.2</span><span class="sxs-lookup"><span data-stu-id="7e515-816">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="7e515-817">Lägg till parametrarna "DataProxyIntegrationRuntimeName", "DataProxyStagingLinkedServiceName" och "DataProxyStagingPath" för "Set-AzureRmDataFactoryV2IntegrationRuntime"-cmd för att aktivera konfiguration av lokalt installerad integrationskörning som en proxy för SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="7e515-817">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="7e515-818">Uppdaterade PSTriggerRun till att visa utlöst pipeline, meddelande och egenskaper samt PSActivityRun till att visa aktivitetstypen</span><span class="sxs-lookup"><span data-stu-id="7e515-818">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7e515-819">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7e515-819">Az.DataLakeStore</span></span>
* <span data-ttu-id="7e515-820">Korrigering av frysning av Get-DataLakeStoreDeletedItem för fel eller fjärrundantag.</span><span class="sxs-lookup"><span data-stu-id="7e515-820">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="7e515-821">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7e515-821">Az.EventHub</span></span>
* <span data-ttu-id="7e515-822">Korrigering av problem #9658 : Skrivfel i parametern VirtualNteworkRule i Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="7e515-822">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="7e515-823">Korrigering av problem #9558 : Set-AzEventHubNamespace använder PATCH i stället för PUT</span><span class="sxs-lookup"><span data-stu-id="7e515-823">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="7e515-824">lade till parametern EnableKafka i Set-AzEventHubNamespace-cmdleten</span><span class="sxs-lookup"><span data-stu-id="7e515-824">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="7e515-825">Korrigering av problem #9786 : kan inte skapa en regel med Endast lyssna-behörighet</span><span class="sxs-lookup"><span data-stu-id="7e515-825">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="7e515-826">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="7e515-826">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="7e515-827">Åtgärdade skrivfel i dokumentation där "Azure" skrevs helt med gemener</span><span class="sxs-lookup"><span data-stu-id="7e515-827">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7e515-828">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7e515-828">Az.Monitor</span></span>
* <span data-ttu-id="7e515-829">Åtgärdade felaktigt parameternamn i hjälpdokumentationen</span><span class="sxs-lookup"><span data-stu-id="7e515-829">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7e515-830">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7e515-830">Az.Network</span></span>
* <span data-ttu-id="7e515-831">Uppdaterade New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="7e515-831">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="7e515-832">Gjorde parametern "PublicIpAddress" inaktuell eftersom den aldrig används på serversidan.</span><span class="sxs-lookup"><span data-stu-id="7e515-832">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="7e515-833">Lade till den valfria parametern "Primary", som anger huruvida den aktuella IP-konfigurationen är den primära.</span><span class="sxs-lookup"><span data-stu-id="7e515-833">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="7e515-834">Förbättrade hanteringen av felundantag för begärande från SDK – åtgärdar problemet att tidigare SDK-undantag inte hanteras på rätt sätt, vilket leder till att viktig felinformation inte visas</span><span class="sxs-lookup"><span data-stu-id="7e515-834">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="7e515-835">Justerade valideringslogiken för IPv6-IP-prefix till att kontrollera korrekt IPv6-prefixlängd.</span><span class="sxs-lookup"><span data-stu-id="7e515-835">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="7e515-836">Uppdaterade Get-AzVirtualNetworkSubnetConfig: Lade till parameter som anges till get av undernätets resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="7e515-836">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="7e515-837">Uppdaterade beskrivningen av parametern Location för AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="7e515-837">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7e515-838">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7e515-838">Az.OperationalInsights</span></span>
* <span data-ttu-id="7e515-839">Uppdaterade dokumentation för "New-AzOperationalInsightsLinuxSyslogDataSource"</span><span class="sxs-lookup"><span data-stu-id="7e515-839">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="7e515-840">Lade till exempel</span><span class="sxs-lookup"><span data-stu-id="7e515-840">Added example</span></span>
    - <span data-ttu-id="7e515-841">Uppdaterade beskrivningen av parametern "-Name"</span><span class="sxs-lookup"><span data-stu-id="7e515-841">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="7e515-842">Lade till ett exempel för New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="7e515-842">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="7e515-843">Ändrade beskrivningen av parametern -Name för New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="7e515-843">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7e515-844">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7e515-844">Az.RecoveryServices</span></span>
* <span data-ttu-id="7e515-845">Uppdatera "Get-AzRecoveryServicesBackupJobDetail.md"</span><span class="sxs-lookup"><span data-stu-id="7e515-845">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="7e515-846">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7e515-846">Az.Resources</span></span>
* <span data-ttu-id="7e515-847">Lägg till stöd för den nya API-versionen från 2019-05-10 för Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="7e515-847">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="7e515-848">Lägg till stöd för "copy.count = 0" för variabler, resurser och egenskaper</span><span class="sxs-lookup"><span data-stu-id="7e515-848">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="7e515-849">Resurser med "condition = false" eller "copy.count = 0" tas bort i complete-läget</span><span class="sxs-lookup"><span data-stu-id="7e515-849">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="7e515-850">Lägg till ett exempel på tilldelning av princip på prenumerationsnivå i hjälpdokumentationen</span><span class="sxs-lookup"><span data-stu-id="7e515-850">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="7e515-851">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="7e515-851">Az.ServiceBus</span></span>
* <span data-ttu-id="7e515-852">Korrigering av problem #9658 : Skrivfel i parametern VirtualNetworkRule i set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="7e515-852">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="7e515-853">Korrigering av problem #9786 : kan inte skapa en regel med Endast lyssna-behörighet</span><span class="sxs-lookup"><span data-stu-id="7e515-853">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="7e515-854">Lade till det nya kommandot "Test-AzServiceBusNameAvailability" för att kontrollera namntillgängligheten för kö och ämne</span><span class="sxs-lookup"><span data-stu-id="7e515-854">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="7e515-855">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7e515-855">Az.ServiceFabric</span></span>
* <span data-ttu-id="7e515-856">Åtgärda buggar med tillägg av nodtyps-cmdlet:</span><span class="sxs-lookup"><span data-stu-id="7e515-856">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="7e515-857">NullReferenceException-bugg när resursgrupp hade annan vmss som inte är relaterad till Service Fabric-klustret.</span><span class="sxs-lookup"><span data-stu-id="7e515-857">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="7e515-858">Åtgärdar problemet: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="7e515-858">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="7e515-859">Åtgärda bugg där cmdleten misslyckades om virtualNetwork var i en annan resursgrupp än klustret.</span><span class="sxs-lookup"><span data-stu-id="7e515-859">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="7e515-860">Åtgärdar problemet: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="7e515-860">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="7e515-861">AzServiceFabricApplicationCertificate-cmdleten görs inaktuell</span><span class="sxs-lookup"><span data-stu-id="7e515-861">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="7e515-862">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7e515-862">Az.Sql</span></span>
* <span data-ttu-id="7e515-863">Uppdatera dokumentation om gamla gransknings-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="7e515-863">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7e515-864">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7e515-864">Az.Storage</span></span>
* <span data-ttu-id="7e515-865">Uppdatera hjälpen för Get/Close-AzStorageFileHandle genom att lägga till fler scenarier i cmdlet-exempel och uppdatera parameterbeskrivningar</span><span class="sxs-lookup"><span data-stu-id="7e515-865">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="7e515-866">Stöd för StandardBlobTier i uppladdningsblob och kopieringsblob</span><span class="sxs-lookup"><span data-stu-id="7e515-866">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="7e515-867">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="7e515-867">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="7e515-868">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="7e515-868">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="7e515-869">Stöd för rehydratiseringsprioritet i kopieringsblob</span><span class="sxs-lookup"><span data-stu-id="7e515-869">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="7e515-870">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="7e515-870">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7e515-871">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7e515-871">Az.Websites</span></span>
* <span data-ttu-id="7e515-872">Lägg till klargöranden gällande parametern -AppSettings i Set-AzWebApp och Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7e515-872">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="7e515-873">2.5.0 – July 2019</span><span class="sxs-lookup"><span data-stu-id="7e515-873">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7e515-874">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7e515-874">Az.Accounts</span></span>
* <span data-ttu-id="7e515-875">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="7e515-875">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="7e515-876">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="7e515-876">Az.ApplicationInsights</span></span>
* <span data-ttu-id="7e515-877">Korrigera skrivfel i exempel i dokumentationen för Remove-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="7e515-877">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="7e515-878">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7e515-878">Az.Automation</span></span>
* <span data-ttu-id="7e515-879">Korrigera skrivfel i resurssträng</span><span class="sxs-lookup"><span data-stu-id="7e515-879">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="7e515-880">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7e515-880">Az.CognitiveServices</span></span>
* <span data-ttu-id="7e515-881">Stöd för NetworkRuleSet har lagts till.</span><span class="sxs-lookup"><span data-stu-id="7e515-881">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7e515-882">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7e515-882">Az.Compute</span></span>
* <span data-ttu-id="7e515-883">Lägg till saknade egenskaper (ComputerName, OsName, OsVersion och HyperVGeneration) för visningsobjekt i den virtuella datorinstansen.</span><span class="sxs-lookup"><span data-stu-id="7e515-883">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="7e515-884">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="7e515-884">Az.ContainerRegistry</span></span>
* <span data-ttu-id="7e515-885">Åtgärda skrivfel i Remove-AzContainerRegistryReplication för parametern Replication</span><span class="sxs-lookup"><span data-stu-id="7e515-885">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="7e515-886">Mer information finns här: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="7e515-886">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7e515-887">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7e515-887">Az.DataFactory</span></span>
* <span data-ttu-id="7e515-888">ADF .Net SDK-versionen har uppdaterats till 4.1.0</span><span class="sxs-lookup"><span data-stu-id="7e515-888">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="7e515-889">Korrigera skrivfel i dokumentationen för Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="7e515-889">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="7e515-890">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7e515-890">Az.EventHub</span></span>
* <span data-ttu-id="7e515-891">Ny cmmdlet har lagts till för att skapa SAS-token: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="7e515-891">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="7e515-892">verifierings- och felmeddelande har lagts till för authorizationrules-rättigheter om endast "hantera" har tilldelats</span><span class="sxs-lookup"><span data-stu-id="7e515-892">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7e515-893">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7e515-893">Az.KeyVault</span></span>
* <span data-ttu-id="7e515-894">Stöd har lagts till för att ange KeySize för certifikatprinciper</span><span class="sxs-lookup"><span data-stu-id="7e515-894">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="7e515-895">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="7e515-895">Az.LogicApp</span></span>
* <span data-ttu-id="7e515-896">Korrigering för Get-AzIntegrationAccountMap för att lista alla mappningstyper</span><span class="sxs-lookup"><span data-stu-id="7e515-896">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="7e515-897">Ny MapType-parameter har lagts till för filtrering</span><span class="sxs-lookup"><span data-stu-id="7e515-897">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="7e515-898">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="7e515-898">Az.ManagedServices</span></span>
* <span data-ttu-id="7e515-899">Stöd för API-versionen 2019-06-01 (GA) har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e515-899">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7e515-900">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7e515-900">Az.Network</span></span>
* <span data-ttu-id="7e515-901">Lägg till stöd för privat slutpunkt och privat länktjänst</span><span class="sxs-lookup"><span data-stu-id="7e515-901">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="7e515-902">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="7e515-902">New cmdlets</span></span>
        - <span data-ttu-id="7e515-903">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="7e515-903">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="7e515-904">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7e515-904">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="7e515-905">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7e515-905">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="7e515-906">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7e515-906">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="7e515-907">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7e515-907">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="7e515-908">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7e515-908">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="7e515-909">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="7e515-909">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="7e515-910">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7e515-910">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="7e515-911">Nedanstående kommandon för funktionen har uppdaterats: Flaggan PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies på undernätet i VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7e515-911">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="7e515-912">Uppdaterade New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="7e515-912">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="7e515-913">Valfri parameter har lagts till – PrivateEndpointNetworkPoliciesFlag som konfigurerar huruvida nätverksprinciper ska tillämpas på en privat slutpunkt i det här undernätet.</span><span class="sxs-lookup"><span data-stu-id="7e515-913">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="7e515-914">Valfri parameter har lagts till – PrivateLinkServiceNetworkPoliciesFlag som konfigurerar huruvida nätverksprinciper ska tillämpas på en privat länktjänst i det här undernätet.</span><span class="sxs-lookup"><span data-stu-id="7e515-914">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="7e515-915">AzPrivateLinkService för cmdlet-parametern ServiceName har bytt namn till Name med aliaset ServiceName för bakåtkompatibilitet</span><span class="sxs-lookup"><span data-stu-id="7e515-915">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="7e515-916">Aktivera ICMP-protokoll för konfiguration av nätverkssäkerhetsregler</span><span class="sxs-lookup"><span data-stu-id="7e515-916">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="7e515-917">Uppdaterade cmdletar</span><span class="sxs-lookup"><span data-stu-id="7e515-917">Updated cmdlets</span></span>
        - <span data-ttu-id="7e515-918">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7e515-918">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="7e515-919">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7e515-919">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="7e515-920">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7e515-920">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="7e515-921">Lägg till ConnectionProtocolType (Ikev1/Ikev2) som en konfigurerbar parameter för New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7e515-921">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="7e515-922">Lägg till PrivateIpAddressVersion i LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="7e515-922">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="7e515-923">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="7e515-923">Updated cmdlet:</span></span>
        - <span data-ttu-id="7e515-924">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="7e515-924">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="7e515-925">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="7e515-925">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="7e515-926">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="7e515-926">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="7e515-927">Uppdatering av Application Gateway-kommandot New-AzApplicationGatewayProbeConfig för stöd av anpassad port i Probe</span><span class="sxs-lookup"><span data-stu-id="7e515-927">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="7e515-928">Uppdaterade New-AzApplicationGatewayProbeConfig: Den valfria parametern Port som används för avsökning i serverdelen har lagts till.</span><span class="sxs-lookup"><span data-stu-id="7e515-928">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="7e515-929">Denna parameter gäller för SKU:erna Standard_V2 och WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="7e515-929">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7e515-930">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7e515-930">Az.OperationalInsights</span></span>
* <span data-ttu-id="7e515-931">Uppdaterade standardversionen för sparade sökningar till 1.</span><span class="sxs-lookup"><span data-stu-id="7e515-931">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="7e515-932">Åtgärdade hantering av anpassad log null regex</span><span class="sxs-lookup"><span data-stu-id="7e515-932">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7e515-933">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7e515-933">Az.RecoveryServices</span></span>
* <span data-ttu-id="7e515-934">Uppdatera Get-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="7e515-934">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="7e515-935">Uppdatera Get-AzRecoveryServicesBackupContainer.md</span><span class="sxs-lookup"><span data-stu-id="7e515-935">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="7e515-936">Uppdatera Get-AzRecoveryServicesVault.md</span><span class="sxs-lookup"><span data-stu-id="7e515-936">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="7e515-937">Uppdatera Wait-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="7e515-937">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="7e515-938">Uppdatera Set-AzRecoveryServicesVaultContext.md</span><span class="sxs-lookup"><span data-stu-id="7e515-938">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="7e515-939">Uppdatera Get-AzRecoveryServicesBackupItem.md</span><span class="sxs-lookup"><span data-stu-id="7e515-939">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="7e515-940">Uppdatera Get-AzRecoveryServicesBackupRecoveryPoint.md</span><span class="sxs-lookup"><span data-stu-id="7e515-940">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="7e515-941">Uppdatera Restore-AzRecoveryServicesBackupItem.md</span><span class="sxs-lookup"><span data-stu-id="7e515-941">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="7e515-942">Uppdaterat tjänstanrop för avregistrering av container för Azure-filresurs</span><span class="sxs-lookup"><span data-stu-id="7e515-942">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="7e515-943">Uppdatera Set-AzRecoveryServicesAsrAlertSetting.md</span><span class="sxs-lookup"><span data-stu-id="7e515-943">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="7e515-944">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7e515-944">Az.Resources</span></span>
- <span data-ttu-id="7e515-945">Ta bort den cmdlet som saknas och som refereras i dokumentationen till New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="7e515-945">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="7e515-946">Princip-cmdletar har uppdaterats så att de använder den nya API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="7e515-946">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="7e515-947">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="7e515-947">Az.ServiceBus</span></span>
* <span data-ttu-id="7e515-948">Ny cmmdlet har lagts till för att skapa SAS-token: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="7e515-948">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="7e515-949">verifierings- och felmeddelande har lagts till för authorizationrules-rättigheter om endast "hantera" har tilldelats</span><span class="sxs-lookup"><span data-stu-id="7e515-949">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="7e515-950">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7e515-950">Az.Sql</span></span>
* <span data-ttu-id="7e515-951">Åtgärda saknade exempel för Set-AzSqlDatabaseSecondary cmdlet</span><span class="sxs-lookup"><span data-stu-id="7e515-951">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="7e515-952">Åtgärda angivna återkommande genomsökningar för bedömning av säkerhetsrisk utan angivna e-postadresser</span><span class="sxs-lookup"><span data-stu-id="7e515-952">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="7e515-953">Korrigera ett skrivfel i ett varningsmeddelande.</span><span class="sxs-lookup"><span data-stu-id="7e515-953">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7e515-954">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7e515-954">Az.Storage</span></span>
* <span data-ttu-id="7e515-955">Uppdatera exempel i referensdokumentationen för Get-AzStorageAccount så att rätt parameternamn används</span><span class="sxs-lookup"><span data-stu-id="7e515-955">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="7e515-956">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="7e515-956">Az.StorageSync</span></span>
* <span data-ttu-id="7e515-957">Lägger till cmdleten Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="7e515-957">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="7e515-958">Åtgärda problem 9551 så att TierFilesOlderThanDays föredras</span><span class="sxs-lookup"><span data-stu-id="7e515-958">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7e515-959">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7e515-959">Az.Websites</span></span>
* <span data-ttu-id="7e515-960">Åtgärdar ett fel där vissa SiteConfig-egenskaper inte returnerades av Get-AzWebApp och Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="7e515-960">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="7e515-961">Lägger till en ny platsparameter för Get-AzDeletedWebApp och Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="7e515-961">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="7e515-962">Åtgärdar ett fel i kloning av webbapp-platser som använder New-AzWebApp-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="7e515-962">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="7e515-963">2.4.0 – juli 2019</span><span class="sxs-lookup"><span data-stu-id="7e515-963">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7e515-964">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7e515-964">Az.Accounts</span></span>
* <span data-ttu-id="7e515-965">Lägg till stöd för profil-cmdletar</span><span class="sxs-lookup"><span data-stu-id="7e515-965">Add support for profile cmdlets</span></span>
* <span data-ttu-id="7e515-966">Lägg till stöd för miljöer och dataplaner i genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="7e515-966">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="7e515-967">Åtgärda bugg där fel slutpunkt i vissa fall användes för cmdletar för dataplaner i Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="7e515-967">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="7e515-968">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="7e515-968">Az.Advisor</span></span>
* <span data-ttu-id="7e515-969">GA-version av Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="7e515-969">GA release of Az.Advisor</span></span>
* <span data-ttu-id="7e515-970">Den här modulen ingår nu som en del av `Az`-sammanslagningsmodulen</span><span class="sxs-lookup"><span data-stu-id="7e515-970">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="7e515-971">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7e515-971">Az.ApiManagement</span></span>
* <span data-ttu-id="7e515-972">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="7e515-972">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="7e515-973">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="7e515-973">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="7e515-974">Stöd för att fråga prenumerationer efter användare och produkt har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e515-974">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="7e515-975">Stöd för att fråga med hjälp av omfång ”/”, ”/apis”, ”/apis/echo-api” har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e515-975">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="7e515-976">Korrigering av problem https://github.com/Azure/azure-powershell/issues/9307 och https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="7e515-976">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="7e515-977">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="7e515-977">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="7e515-978">Stöd för att ange ”ApiVersion” och ”ApiVersionSetId” när API:er importeras har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e515-978">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7e515-979">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7e515-979">Az.Automation</span></span>
* <span data-ttu-id="7e515-980">Bugg med cmdleten Set-AzAutomationConnectionFieldValue för att hantera strängvärde har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="7e515-980">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7e515-981">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7e515-981">Az.Compute</span></span>
* <span data-ttu-id="7e515-982">Lägg till parametern HyperVGeneration i New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="7e515-982">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7e515-983">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7e515-983">Az.DataFactory</span></span>
* <span data-ttu-id="7e515-984">Uppdaterar utdata från ADF-cmdletar som hämtar aktivitetskörningar, hämtar pipelinekörningar och hämtar utlösarkörningar för stöd för Select-Object-pipe.</span><span class="sxs-lookup"><span data-stu-id="7e515-984">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="7e515-985">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="7e515-985">Az.EventGrid</span></span>
* <span data-ttu-id="7e515-986">Korrigera stavfel i dokumentation om ”New-AzEventGridSubscription”</span><span class="sxs-lookup"><span data-stu-id="7e515-986">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7e515-987">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7e515-987">Az.IotHub</span></span>
* <span data-ttu-id="7e515-988">Lägg till stöd för att återskapa principnycklar för auktorisering.</span><span class="sxs-lookup"><span data-stu-id="7e515-988">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7e515-989">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7e515-989">Az.Network</span></span>
* <span data-ttu-id="7e515-990">”RoutingPreference” har lagts till i offentliga IP-taggar</span><span class="sxs-lookup"><span data-stu-id="7e515-990">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="7e515-991">Förbättra exempel för referensdokumentation om ”Get-AzNetworkServiceTag”</span><span class="sxs-lookup"><span data-stu-id="7e515-991">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="7e515-992">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="7e515-992">Az.PolicyInsights</span></span>
* <span data-ttu-id="7e515-993">Åtgärda problem med null-referens i Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="7e515-993">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="7e515-994">Mer information här: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="7e515-994">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7e515-995">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7e515-995">Az.OperationalInsights</span></span>
* <span data-ttu-id="7e515-996">Modellen för CustomLog-datakälla som returneras i Get-AzOperationalInsightsDataSource har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="7e515-996">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7e515-997">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7e515-997">Az.RecoveryServices</span></span>
* <span data-ttu-id="7e515-998">Kommandot get-policy för IaaSVM:er har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="7e515-998">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="7e515-999">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7e515-999">Az.Resources</span></span>
    - <span data-ttu-id="7e515-1000">Korrigera hjälptext för den översta parametern i Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="7e515-1000">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="7e515-1001">Lägg till växlingsstöd på klientsidan för Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="7e515-1001">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="7e515-1002">Lägg till nya parametrar för Set-AzPolicyAssignment, -PolicyParameters och -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="7e515-1002">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="7e515-1003">En mängd dokument- och exempeluppdateringar för Policy-cmdletar</span><span class="sxs-lookup"><span data-stu-id="7e515-1003">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="7e515-1004">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="7e515-1004">Az.ServiceBus</span></span>
* <span data-ttu-id="7e515-1005">Korrigering av problem #4938 – New-AzureRmServiceBusQueue returnerar BadRequest vid konfiguration av MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="7e515-1005">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="7e515-1006">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7e515-1006">Az.Sql</span></span>
* <span data-ttu-id="7e515-1007">Lägg till cmdletar för instansredundansgrupper från förhandsversion till offentlig version</span><span class="sxs-lookup"><span data-stu-id="7e515-1007">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="7e515-1008">Stöd för granskning för Azure SQL Server\Database med nya cmdletar.</span><span class="sxs-lookup"><span data-stu-id="7e515-1008">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="7e515-1009">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="7e515-1009">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="7e515-1010">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="7e515-1010">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="7e515-1011">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="7e515-1011">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="7e515-1012">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="7e515-1012">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="7e515-1013">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="7e515-1013">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="7e515-1014">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="7e515-1014">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="7e515-1015">Ta bort begränsningar för e-post från inställningarna för sårbarhetsbedömning</span><span class="sxs-lookup"><span data-stu-id="7e515-1015">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7e515-1016">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7e515-1016">Az.Storage</span></span>
* <span data-ttu-id="7e515-1017">Ändra två parametrar ”-IndexDocument” och ”-ErrorDocument404Path” från ”krävs” till ”valfri” i cmdlet:</span><span class="sxs-lookup"><span data-stu-id="7e515-1017">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="7e515-1018">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="7e515-1018">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="7e515-1019">Uppdatera hjälpen för Get-AzStorageBlobContent genom att lägga till ett exempel</span><span class="sxs-lookup"><span data-stu-id="7e515-1019">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="7e515-1020">Visa mer felinformation när cmdleten misslyckas med StorageException</span><span class="sxs-lookup"><span data-stu-id="7e515-1020">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="7e515-1021">Stöd för att skapa eller uppdatera lagringskonto med Azure Files AAD DS-autentisering</span><span class="sxs-lookup"><span data-stu-id="7e515-1021">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="7e515-1022">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7e515-1022">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="7e515-1023">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7e515-1023">Set-AzStorageAccount</span></span>
* <span data-ttu-id="7e515-1024">Stöd för att lista eller stänga filreferenser för en filresurs, filkatalog eller en fil</span><span class="sxs-lookup"><span data-stu-id="7e515-1024">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="7e515-1025">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="7e515-1025">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="7e515-1026">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="7e515-1026">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="7e515-1027">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="7e515-1027">Az.StorageSync</span></span>
* <span data-ttu-id="7e515-1028">Den här modulen ingår nu som en del av `Az`-sammanslagningsmodulen</span><span class="sxs-lookup"><span data-stu-id="7e515-1028">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="7e515-1029">2.3.2 – juni 2019</span><span class="sxs-lookup"><span data-stu-id="7e515-1029">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7e515-1030">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7e515-1030">Az.Accounts</span></span>
* <span data-ttu-id="7e515-1031">Åtgärda bugg med felaktiga webbadresser som i vissa fall användes för Functions-anrop</span><span class="sxs-lookup"><span data-stu-id="7e515-1031">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="7e515-1032">Mer information här: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="7e515-1032">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="7e515-1033">Åtgärda problem med alias från AzureRM i Az-cmdletar</span><span class="sxs-lookup"><span data-stu-id="7e515-1033">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="7e515-1034">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="7e515-1034">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="7e515-1035">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="7e515-1035">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7e515-1036">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7e515-1036">Az.Compute</span></span>
* <span data-ttu-id="7e515-1037">Parameteruppsättningarna New-AzVm och New-AzVmss accepterar nu parametern ”ProximityPlacementGroup”.</span><span class="sxs-lookup"><span data-stu-id="7e515-1037">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="7e515-1038">Stavfel i referensdokumentationen för ”New-AzVM” har korrigerats</span><span class="sxs-lookup"><span data-stu-id="7e515-1038">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="7e515-1039">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="7e515-1039">Az.Dns</span></span>
* <span data-ttu-id="7e515-1040">Stavfel i hjälpexempel för ”Set-AzDnsZone” har korrigerats.</span><span class="sxs-lookup"><span data-stu-id="7e515-1040">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="7e515-1041">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="7e515-1041">Az.EventGrid</span></span>
* <span data-ttu-id="7e515-1042">Har uppdaterats för att använda API-versionen 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="7e515-1042">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="7e515-1043">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="7e515-1043">New cmdlets:</span></span>
    - <span data-ttu-id="7e515-1044">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="7e515-1044">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="7e515-1045">Skapar en ny Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="7e515-1045">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="7e515-1046">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="7e515-1046">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="7e515-1047">Hämtar information om en Event Grid-domän eller hämtar en lista med alla Event Grid-domäner i den aktuella Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="7e515-1047">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="7e515-1048">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="7e515-1048">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="7e515-1049">Tar bort en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="7e515-1049">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="7e515-1050">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="7e515-1050">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="7e515-1051">Återskapar nyckeln för delad åtkomst för en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="7e515-1051">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="7e515-1052">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="7e515-1052">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="7e515-1053">Hämtar de nycklar för delad åtkomst som används för att publicera händelser till en Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="7e515-1053">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="7e515-1054">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="7e515-1054">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="7e515-1055">Skapar ett nytt Azure Event Grid-domänämne.</span><span class="sxs-lookup"><span data-stu-id="7e515-1055">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="7e515-1056">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="7e515-1056">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="7e515-1057">Hämtar information om ett Event Grid-domänämne eller hämtar en lista med alla Event Grid-domänämnen under en specifik Event Grid-domän i nuvarande Azure</span><span class="sxs-lookup"><span data-stu-id="7e515-1057">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="7e515-1058">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="7e515-1058">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="7e515-1059">Tar bort ett befintligt Azure Event Grid-domänämne.</span><span class="sxs-lookup"><span data-stu-id="7e515-1059">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="7e515-1060">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="7e515-1060">Updated cmdlets:</span></span>
    - <span data-ttu-id="7e515-1061">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="7e515-1061">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="7e515-1062">Lägg till nya obligatoriska parametrar för att stödja piping för den nya Event Grid-domänen och Event Grid-domänämnet för att göra det möjligt att skapa nya händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="7e515-1062">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="7e515-1063">Lägg till nya obligatoriska parametrar för att ange det nya Event Grid-domännamnet och/eller namnet på Event Grid-domänämnet för att göra det möjligt att skapa nya händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="7e515-1063">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="7e515-1064">Lägg till ny parameteruppsättningar för domäner och domänämnen för att göra det möjligt att återanvända befintliga parametrar (t.ex. EndPointType, SubjectBeginsWith osv).</span><span class="sxs-lookup"><span data-stu-id="7e515-1064">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="7e515-1065">Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="7e515-1065">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="7e515-1066">Förfallodatum för händelseprenumeration</span><span class="sxs-lookup"><span data-stu-id="7e515-1066">Event subscription expiration date,</span></span>
            - <span data-ttu-id="7e515-1067">Avancerade filterparametrar.</span><span class="sxs-lookup"><span data-stu-id="7e515-1067">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="7e515-1068">Lägg till ny uppräkning för servicebusqueue som mål.</span><span class="sxs-lookup"><span data-stu-id="7e515-1068">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="7e515-1069">Tillåt inte användning av ”Alla” i alternativet -IncludedEventType och ersätt det med</span><span class="sxs-lookup"><span data-stu-id="7e515-1069">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="7e515-1070">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="7e515-1070">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="7e515-1071">Lägg till ny valfria parametrar (Top, ODataQuery och NextLink) för att stödja sidnumrering och filtrering av resultat.</span><span class="sxs-lookup"><span data-stu-id="7e515-1071">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="7e515-1072">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="7e515-1072">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="7e515-1073">Lägg till nya obligatoriska parametrar för att stödja piping för en Event Grid-domän och Event Grid-domänämnen för att göra det möjligt att ta bort befintliga händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="7e515-1073">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="7e515-1074">Lägg till nya obligatoriska parametrar för att ange Event Grid-domännamnet och/eller namnet på Event Grid-domänämnet för att göra det möjligt att ta bort befintliga händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="7e515-1074">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="7e515-1075">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="7e515-1075">Az.FrontDoor</span></span>
* <span data-ttu-id="7e515-1076">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="7e515-1076">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="7e515-1077">Lägg till stöd för transformeringar och nytt värde för automatisk komplettering för operatorer (RegEx)</span><span class="sxs-lookup"><span data-stu-id="7e515-1077">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="7e515-1078">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="7e515-1078">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="7e515-1079">Lägg till nya värden för automatisk komplettering</span><span class="sxs-lookup"><span data-stu-id="7e515-1079">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7e515-1080">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7e515-1080">Az.Network</span></span>
* <span data-ttu-id="7e515-1081">Lägg till stöd för resurs för virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="7e515-1081">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="7e515-1082">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="7e515-1082">New cmdlets</span></span>
        - <span data-ttu-id="7e515-1083">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="7e515-1083">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="7e515-1084">Lägg till AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="7e515-1084">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="7e515-1085">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="7e515-1085">New cmdlets</span></span> 
        - <span data-ttu-id="7e515-1086">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="7e515-1086">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="7e515-1087">Lägg till PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7e515-1087">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="7e515-1088">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="7e515-1088">New cmdlets</span></span> 
        - <span data-ttu-id="7e515-1089">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7e515-1089">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="7e515-1090">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7e515-1090">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="7e515-1091">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7e515-1091">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="7e515-1092">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="7e515-1092">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="7e515-1093">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7e515-1093">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="7e515-1094">Lägg till PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="7e515-1094">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="7e515-1095">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="7e515-1095">New cmdlets</span></span>
        - <span data-ttu-id="7e515-1096">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="7e515-1096">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="7e515-1097">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="7e515-1097">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="7e515-1098">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="7e515-1098">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="7e515-1099">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="7e515-1099">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="7e515-1100">Nedanstående kommandon för funktionen har uppdaterats: Flaggan UseLocalAzureIpAddress på VpnConnection</span><span class="sxs-lookup"><span data-stu-id="7e515-1100">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="7e515-1101">New-AzVpnConnection har uppdaterats: Den valfria parametern -UseLocalAzureIpAddress har lagts till för att visa att en lokal IP-adress i Azure ska användas som källadress när anslutningen initieras.</span><span class="sxs-lookup"><span data-stu-id="7e515-1101">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="7e515-1102">Set-AzVpnConnection har uppdaterats: Den valfria parametern -UseLocalAzureIpAddress har lagts till för att visa att en lokal IP-adress i Azure ska användas som källadress när anslutningen initieras.</span><span class="sxs-lookup"><span data-stu-id="7e515-1102">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="7e515-1103">Det skrivskyddade fältet PeeredConnections har lagts till i ExpressRoute-peering.</span><span class="sxs-lookup"><span data-stu-id="7e515-1103">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="7e515-1104">Det skrivskyddade fältet GlobalReachEnabled har lagts till i ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="7e515-1104">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="7e515-1105">Ett attribut för icke-bakåtkompatibla ändringar har lagts till för att lyfta fram utfasning av fältet AllowGlobalReach i modellen ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7e515-1105">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="7e515-1106">Problem 8756 har åtgärdats: Fel vid användning av TargetListenerID med AzApplicationGatewayRedirectConfiguration-cmdletar</span><span class="sxs-lookup"><span data-stu-id="7e515-1106">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="7e515-1107">En bugg i New-AzApplicationGatewayPathRuleConfig som gjorde att regeluppsättningen för att återskapa inte kunde anges har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="7e515-1107">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="7e515-1108">Visningen av VirtualNetworkTaps i NetworkInterfaceIpConfiguration har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="7e515-1108">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="7e515-1109">Cortex Get-cmdletar för att visa en lista med alla delar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="7e515-1109">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="7e515-1110">Funktionen för att skapa VirtualHub-referenser för ExpressRouteGateways och VpnGateway har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="7e515-1110">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="7e515-1111">Stöd för tillgänglighetszoner i AzureFirewall och NatGateway har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e515-1111">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="7e515-1112">Cmdleten Get-AzNetworkServiceTag har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e515-1112">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="7e515-1113">Lägg till stöd för flera offentliga IP-adresser för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="7e515-1113">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="7e515-1114">Cmdleten New-AzFirewall har uppdaterats:</span><span class="sxs-lookup"><span data-stu-id="7e515-1114">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="7e515-1115">Parametern -PublicIpAddress som accepterar ett eller flera offentliga IP-adressobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e515-1115">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="7e515-1116">Parametern -VirtualNetwork som accepterar ett virtuellt nätverksobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e515-1116">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="7e515-1117">Metoderna AddPublicIpAddress och RemovePublicIpAddress har lagts till på brandväggsobjekt – dessa accepterar ett offentligt IP-adressobjekt som indata</span><span class="sxs-lookup"><span data-stu-id="7e515-1117">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="7e515-1118">Inaktuella parametrar -PublicIpName och -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="7e515-1118">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="7e515-1119">Nedanstående kommandon för funktionen har uppdaterats: Ange autentiseringsalternativ för VpnClient AAD till resurser för virtuella nätverksgatewayer.</span><span class="sxs-lookup"><span data-stu-id="7e515-1119">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="7e515-1120">New-AzVirtualNetworkGateway har uppdaterats: De valfria parametrarna AadTenantUri, AadAudienceId och AadIssuerUri för att ange VpnClient AAD-autentiseringsalternativ på en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="7e515-1120">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="7e515-1121">Set-AzVirtualNetworkGateway har uppdaterats: De valfria parametrarna AadTenantUri, AadAudienceId och AadIssuerUri för att ange VpnClient AAD-autentiseringsalternativ på en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="7e515-1121">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="7e515-1122">Set-AzVirtualNetworkGateway har uppdaterats: Den valfria växelparametern RemoveAadAuthentication som tar bort VpnClient AAD-autentiseringsalternativ från en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="7e515-1122">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7e515-1123">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7e515-1123">Az.OperationalInsights</span></span>
* <span data-ttu-id="7e515-1124">Aktivera prisnivån **pergb2018** i kommandot ”New-AzureRmOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="7e515-1124">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="7e515-1125">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7e515-1125">Az.Resources</span></span>
* <span data-ttu-id="7e515-1126">Stöd för ytterligare alternativ för att exportera en mall</span><span class="sxs-lookup"><span data-stu-id="7e515-1126">Support for additional Template Export options</span></span>
    - <span data-ttu-id="7e515-1127">Lägg till parametern ”-SkipResourceNameParameterization” till Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7e515-1127">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="7e515-1128">Lägg till parametern ”-SkipAllParameterization” till Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7e515-1128">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="7e515-1129">Lägg till parametern ”-Resource” till Export-AzResourceGroup för exporterad resursfiltrering</span><span class="sxs-lookup"><span data-stu-id="7e515-1129">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="7e515-1130">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7e515-1130">Az.ServiceFabric</span></span>
* <span data-ttu-id="7e515-1131">Åtgärda att fel tumavtryck används vid tilläggning av certifikat i ByExistingKeyVault i vissa fall</span><span class="sxs-lookup"><span data-stu-id="7e515-1131">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="7e515-1132">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7e515-1132">Az.Sql</span></span>
* <span data-ttu-id="7e515-1133">Åtgärda suffix för lagringsslutpunkt i Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="7e515-1133">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="7e515-1134">Åtgärda att aktivering av Advanced Data Security åsidosätter Advanced Threat Protection-princip</span><span class="sxs-lookup"><span data-stu-id="7e515-1134">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="7e515-1135">Nya cmdletar för Management.Sql som gör att kunderna kan lägga till nycklar för transparent datakryptering (TDE) och ange TDE-skydd för hanterade instanser</span><span class="sxs-lookup"><span data-stu-id="7e515-1135">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="7e515-1136">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="7e515-1136">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="7e515-1137">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="7e515-1137">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="7e515-1138">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="7e515-1138">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="7e515-1139">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="7e515-1139">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="7e515-1140">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="7e515-1140">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7e515-1141">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7e515-1141">Az.Storage</span></span>
* <span data-ttu-id="7e515-1142">Stöd för typerna FileStorage och SkuName Premium_ZRS när lagringskonton skapas</span><span class="sxs-lookup"><span data-stu-id="7e515-1142">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="7e515-1143">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7e515-1143">New-AzStorageAccount</span></span>
* <span data-ttu-id="7e515-1144">Beskrivningen av cmdleten för bloboföränderlighet har förtydligats</span><span class="sxs-lookup"><span data-stu-id="7e515-1144">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="7e515-1145">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="7e515-1145">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7e515-1146">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7e515-1146">Az.Websites</span></span>
* <span data-ttu-id="7e515-1147">Optimerar Get-AzWebAppCertificate för att filtrera efter resursgrupp på servern i stället för klienten</span><span class="sxs-lookup"><span data-stu-id="7e515-1147">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="7e515-1148">Lägger till växlingsparametern -UseDisasterRecovery till Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="7e515-1148">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="7e515-1149">2.2.0 – juni 2019</span><span class="sxs-lookup"><span data-stu-id="7e515-1149">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="7e515-1150">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7e515-1150">Az.Cdn</span></span>
* <span data-ttu-id="7e515-1151">Uppdaterade cmdletar för att ge stöd för rulesEngine-funktion baserat på API-version 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="7e515-1151">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7e515-1152">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7e515-1152">Az.Compute</span></span>
* <span data-ttu-id="7e515-1153">Lade till parameter `NoWait` som startar åtgärden och returnerar omedelbart, innan åtgärden har slutförts.</span><span class="sxs-lookup"><span data-stu-id="7e515-1153">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="7e515-1154">Uppdaterade cmdletar:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="7e515-1154">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="7e515-1155">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7e515-1155">Az.EventHub</span></span>
* <span data-ttu-id="7e515-1156">Korrigering för #9231 – Get-AzEventHubNamespace returnerar inga taggar</span><span class="sxs-lookup"><span data-stu-id="7e515-1156">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="7e515-1157">Korrigering för #9230 – Get-AzEventHubNamespace returnerar ResourceGroup istället för ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e515-1157">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7e515-1158">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7e515-1158">Az.Network</span></span>
* <span data-ttu-id="7e515-1159">Uppdatera ResourceId och InputObject för NAT-gateway</span><span class="sxs-lookup"><span data-stu-id="7e515-1159">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="7e515-1160">Lägg till alias för ResourceId och InputObject</span><span class="sxs-lookup"><span data-stu-id="7e515-1160">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="7e515-1161">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="7e515-1161">Az.PolicyInsights</span></span>
* <span data-ttu-id="7e515-1162">Åtgärda Null-referensproblem i Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="7e515-1162">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7e515-1163">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7e515-1163">Az.RecoveryServices</span></span>
* <span data-ttu-id="7e515-1164">Minsta kvarhållning för IaaSVM-policy i dagar ändrat till 7 från 1</span><span class="sxs-lookup"><span data-stu-id="7e515-1164">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="7e515-1165">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="7e515-1165">Az.ServiceBus</span></span>
* <span data-ttu-id="7e515-1166">Korrigering för ärende #9182 – Get-AzServiceBusNamespace returnerar ResourceGroup istället för ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e515-1166">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="7e515-1167">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7e515-1167">Az.ServiceFabric</span></span>
* <span data-ttu-id="7e515-1168">Åtgärda stavfel i felmeddelandet för Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="7e515-1168">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="7e515-1169">Åtgärda saknat tecken i Service Fabric-kommandorader</span><span class="sxs-lookup"><span data-stu-id="7e515-1169">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="7e515-1170">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7e515-1170">Az.Sql</span></span>
* <span data-ttu-id="7e515-1171">Lägg till parametern DnsZonePartner för New-AzureSqlInstance-cmdlet för att ge stöd för AutoDr för hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="7e515-1171">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="7e515-1172">Avvecklar cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="7e515-1172">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="7e515-1173">Döp om cmdletar för hotidentifiering till Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="7e515-1173">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="7e515-1174">Parametrarna New-AzSqlInstance -StorageSizeInGB och -LicenseType är nu valfria.</span><span class="sxs-lookup"><span data-stu-id="7e515-1174">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7e515-1175">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7e515-1175">Az.Websites</span></span>
* <span data-ttu-id="7e515-1176">åtgärdar problemet där användningen av Set-AzWebApp och Set-AzWebAppSlot med -WebApp-egenskap tog bort taggarna</span><span class="sxs-lookup"><span data-stu-id="7e515-1176">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="7e515-1177">2.1.0 – maj 2019</span><span class="sxs-lookup"><span data-stu-id="7e515-1177">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="7e515-1178">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7e515-1178">Az.ApiManagement</span></span>
* <span data-ttu-id="7e515-1179">Skapade nya cmdletar för att hantera diagnostik för global- och API-omfång</span><span class="sxs-lookup"><span data-stu-id="7e515-1179">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="7e515-1180">**Get-AzApiManagementDiagnostic** – Skaffa diagnostik konfigurerad för global- eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="7e515-1180">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="7e515-1181">**New-AzApiManagementDiagnostic** – Skapa ny diagnostik för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="7e515-1181">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="7e515-1182">**New-AzApiManagementHttpMessageDiagnostic** – Skapa diagnostikinställning om vilka rubriker som ska loggas och storleken på brödtextbyte</span><span class="sxs-lookup"><span data-stu-id="7e515-1182">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="7e515-1183">**New-AzApiManagementPipelineDiagnosticSetting** – Skapa diagnostikinställningar för inkommande/utgående HTTP-meddelanden till gatewayen.</span><span class="sxs-lookup"><span data-stu-id="7e515-1183">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="7e515-1184">**New-AzApiManagementSamplingSetting** – Skapa samplinginställningar för begäranden/svar för en diagnostik</span><span class="sxs-lookup"><span data-stu-id="7e515-1184">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="7e515-1185">**Remove-AzApiManagementDiagnostic** – Ta bort en diagnostikenhet för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="7e515-1185">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="7e515-1186">**Set-AzApiManagementDiagnostic** – Uppdatera en diagnostikenhet för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="7e515-1186">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="7e515-1187">Skapade nya cmdletar för hantering av cacheminne i ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="7e515-1187">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="7e515-1188">**Get-AzApiManagementCache** – Hämta information om cacheminnet som anges av identifierare eller alla cacheminnen</span><span class="sxs-lookup"><span data-stu-id="7e515-1188">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="7e515-1189">**New-AzApiManagementCache** – Skapa ett nytt default-cacheminne eller cacheminne i en viss Azure-region</span><span class="sxs-lookup"><span data-stu-id="7e515-1189">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="7e515-1190">**Remove-AzApiManagementCache** – Ta bort ett cacheminne</span><span class="sxs-lookup"><span data-stu-id="7e515-1190">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="7e515-1191">**Remove-AzApiManagementCache** – Ta bort ett cacheminne</span><span class="sxs-lookup"><span data-stu-id="7e515-1191">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="7e515-1192">Skapade nya cmdletar för hantering av API-schema</span><span class="sxs-lookup"><span data-stu-id="7e515-1192">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="7e515-1193">**New-AzApiManagementSchema** – Skapa ett nytt schema för ett API</span><span class="sxs-lookup"><span data-stu-id="7e515-1193">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="7e515-1194">**Get-AzApiManagementSchema** – Hämta de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="7e515-1194">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="7e515-1195">**Remove-AzApiManagementSchema** – Ta bort de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="7e515-1195">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="7e515-1196">**Set-AzApiManagementSchema** – Uppdatera de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="7e515-1196">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="7e515-1197">Skapa ny cmdlet för att generera en användartoken.</span><span class="sxs-lookup"><span data-stu-id="7e515-1197">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="7e515-1198">**New-AzApiManagementUserToken** – Skapa en ny användartoken som enligt standardinställning är giltig i 8 timmar. Token för GIT-användaren kan skapas med den här cmdleten./</span><span class="sxs-lookup"><span data-stu-id="7e515-1198">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="7e515-1199">Skapade en ny cmdlet för att hämta nätverksstatus</span><span class="sxs-lookup"><span data-stu-id="7e515-1199">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="7e515-1200">**Get-AzApiManagementNetworkStatus** – Hämta nätverksstatusanslutningen för resurserna som API Management-tjänsten är beroende av.</span><span class="sxs-lookup"><span data-stu-id="7e515-1200">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="7e515-1201">Det här är användbart när du distribuerar ApiManagement-tjänsten i ett virtuellt nätverk och validerar om något beroende är brutet.</span><span class="sxs-lookup"><span data-stu-id="7e515-1201">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="7e515-1202">Uppdaterade cmdlet **New-AzApiManagement** för att hantera ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="7e515-1202">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="7e515-1203">Lade till stöd för den nya SKU:n Consumption</span><span class="sxs-lookup"><span data-stu-id="7e515-1203">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="7e515-1204">Aktiverade stöd för att slå på flaggan EnableClientCertificate för SKU:n Consumption</span><span class="sxs-lookup"><span data-stu-id="7e515-1204">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="7e515-1205">Den nya cmdleten **New-AzApiManagementSslSetting** gör det möjligt att ställa in TLS/SSL-inställningen på ”Backend” och ”Frontend” (serverdel och klientdel).</span><span class="sxs-lookup"><span data-stu-id="7e515-1205">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="7e515-1206">Det här kan också användas till att konfigurera chiffer som 3DES och ServerProtocols som Http2 för Frontend för en ApiManagement-tjänst.</span><span class="sxs-lookup"><span data-stu-id="7e515-1206">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="7e515-1207">Stöd har lagts till för att konfigurera värdnamnet DeveloperPortal på ApiManagement-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="7e515-1207">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="7e515-1208">Uppdaterade cmdletar **Get-AzApiManagementSsoToken** för att ta PsApiManagement-objekt som indata</span><span class="sxs-lookup"><span data-stu-id="7e515-1208">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="7e515-1209">Uppdaterad cmdleten för att visa infogade felmeddelanden</span><span class="sxs-lookup"><span data-stu-id="7e515-1209">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="7e515-1210">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Felkod: Felmeddelande av typen ValidationError: Ett eller flera fält innehåller felaktiga värden: Felinformation:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="7e515-1210">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="7e515-1211">Uppdaterade cmdlet **Export-AzApiManagementApi** för att exportera API:er i OpenApi 3.0-format</span><span class="sxs-lookup"><span data-stu-id="7e515-1211">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="7e515-1212">Uppdaterade cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="7e515-1212">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="7e515-1213">Importera API från dokumentspecifikationen OpenApi 3.0</span><span class="sxs-lookup"><span data-stu-id="7e515-1213">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="7e515-1214">Om du vill åsidosätta egenskapen PsApiManagementSchema specificerad i ett dokument (Swagger, Wadl, Wsdl, OpenApi).</span><span class="sxs-lookup"><span data-stu-id="7e515-1214">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="7e515-1215">Åsidosätta egenskapen ServiceUrl som specificeras i ett dokument.</span><span class="sxs-lookup"><span data-stu-id="7e515-1215">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="7e515-1216">Uppdaterade cmdlet **Get-AzApiManagementPolicy** för att returnera policy i undantaget format av typen icke-XML med rawxml</span><span class="sxs-lookup"><span data-stu-id="7e515-1216">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="7e515-1217">Uppdaterade cmdlet **Set-AzApiManagementPolicy** för att godkänna policy i undantaget format av typen icke-XML med rawxml och XML undantaget med xml</span><span class="sxs-lookup"><span data-stu-id="7e515-1217">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="7e515-1218">Uppdaterad cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="7e515-1218">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="7e515-1219">Konfigurera API med OpenId auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="7e515-1219">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="7e515-1220">Skapa ett API i ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="7e515-1220">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="7e515-1221">Klona ett API med SourceApiId och SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="7e515-1221">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="7e515-1222">Möjlighet att konfigurera SubscriptionRequired i API-omfattningen.</span><span class="sxs-lookup"><span data-stu-id="7e515-1222">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="7e515-1223">Uppdaterad cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="7e515-1223">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="7e515-1224">Konfigurera API med OpenId auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="7e515-1224">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="7e515-1225">Uppdatera ett API till ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="7e515-1225">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="7e515-1226">Möjlighet att konfigurera SubscriptionRequired i API-omfattningen.</span><span class="sxs-lookup"><span data-stu-id="7e515-1226">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="7e515-1227">Uppdaterad cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="7e515-1227">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="7e515-1228">Klona en befintlig version med hjälp av SourceApiRevision (kopiera taggar, produkter, åtgärder och principer).</span><span class="sxs-lookup"><span data-stu-id="7e515-1228">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="7e515-1229">Den nya revisionen antar ApiId från den överordnade instansen.</span><span class="sxs-lookup"><span data-stu-id="7e515-1229">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="7e515-1230">Tillhandahålla ApiRevisionDescription</span><span class="sxs-lookup"><span data-stu-id="7e515-1230">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="7e515-1231">Åsidosätta ServiceUrl vid kloning av ett API.</span><span class="sxs-lookup"><span data-stu-id="7e515-1231">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="7e515-1232">Uppdaterad cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="7e515-1232">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="7e515-1233">Konfigurera AAD eller AADB2C med en Authority</span><span class="sxs-lookup"><span data-stu-id="7e515-1233">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="7e515-1234">Konfigurera SignupPolicy, SigninPolicy, ProfileEditingPolicy och PasswordResetPolicy</span><span class="sxs-lookup"><span data-stu-id="7e515-1234">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="7e515-1235">Uppdaterad cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="7e515-1235">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="7e515-1236">Kompensera för ny SubscriptonModel med Scope och UserId</span><span class="sxs-lookup"><span data-stu-id="7e515-1236">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="7e515-1237">Kompensera för gammal prenumerationsmodell med ProductId och UserId</span><span class="sxs-lookup"><span data-stu-id="7e515-1237">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="7e515-1238">Lägg till funktion för att aktivera AllowTracing på prenumerationsnivå.</span><span class="sxs-lookup"><span data-stu-id="7e515-1238">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="7e515-1239">Uppdaterad cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="7e515-1239">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="7e515-1240">Kompensera för ny SubscriptonModel med Scope och UserId</span><span class="sxs-lookup"><span data-stu-id="7e515-1240">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="7e515-1241">Kompensera för gammal prenumerationsmodell med ProductId och UserId</span><span class="sxs-lookup"><span data-stu-id="7e515-1241">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="7e515-1242">Lägg till funktion för att aktivera AllowTracing på prenumerationsnivå.</span><span class="sxs-lookup"><span data-stu-id="7e515-1242">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="7e515-1243">Uppdaterade följande cmdletar för att acceptera ResourceId som indata</span><span class="sxs-lookup"><span data-stu-id="7e515-1243">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="7e515-1244">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="7e515-1244">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="7e515-1245">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="7e515-1245">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="7e515-1246">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="7e515-1246">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="7e515-1247">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="7e515-1247">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="7e515-1248">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="7e515-1248">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="7e515-1249">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="7e515-1249">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="7e515-1250">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="7e515-1250">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="7e515-1251">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="7e515-1251">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="7e515-1252">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="7e515-1252">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="7e515-1253">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="7e515-1253">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="7e515-1254">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="7e515-1254">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="7e515-1255">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="7e515-1255">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7e515-1256">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7e515-1256">Az.Automation</span></span>
* <span data-ttu-id="7e515-1257">Uppdaterade Get-AzAutomationJobOutputRecord för att hantera postvärden av typen JSON och Text.</span><span class="sxs-lookup"><span data-stu-id="7e515-1257">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="7e515-1258">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="7e515-1258">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="7e515-1259">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="7e515-1259">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="7e515-1260">Ändrade beteende för Start-AzAutomationDscCompilationJob till att bara starta jobbet istället för att vänta på slutförandet.</span><span class="sxs-lookup"><span data-stu-id="7e515-1260">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="7e515-1261">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="7e515-1261">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="7e515-1262">Korrigering för Get-AzAutomationDscNode när using -Name returnerar alla noder.</span><span class="sxs-lookup"><span data-stu-id="7e515-1262">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="7e515-1263">Nu returnerar den endast den matchande noden.</span><span class="sxs-lookup"><span data-stu-id="7e515-1263">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7e515-1264">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7e515-1264">Az.Compute</span></span>
* <span data-ttu-id="7e515-1265">Lägg till parametrarna ProtectFromScaleIn och ProtectFromScaleSetAction i cmdleten Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="7e515-1265">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="7e515-1266">Nu är standardinställningen att vimpelparametern New-AzVM använder en tillgänglig plats om USA, östra inte stöds</span><span class="sxs-lookup"><span data-stu-id="7e515-1266">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7e515-1267">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7e515-1267">Az.DataLakeStore</span></span>
* <span data-ttu-id="7e515-1268">Uppdatera ADLS-sdk för att använda httpclient, integrera dataplanstestning med Azure-ramverk</span><span class="sxs-lookup"><span data-stu-id="7e515-1268">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7e515-1269">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7e515-1269">Az.Monitor</span></span>
* <span data-ttu-id="7e515-1270">Korrigera felaktiga parameternamn i hjälpexempel</span><span class="sxs-lookup"><span data-stu-id="7e515-1270">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7e515-1271">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7e515-1271">Az.Network</span></span>
* <span data-ttu-id="7e515-1272">Lägg till flaggan DisableBgpRoutePropagation i utdata för effektiv routningstabell</span><span class="sxs-lookup"><span data-stu-id="7e515-1272">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="7e515-1273">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="7e515-1273">Updated cmdlet:</span></span>
        - <span data-ttu-id="7e515-1274">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="7e515-1274">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="7e515-1275">Åtgärda dubbelstreck i dokumentationen New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="7e515-1275">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="7e515-1276">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7e515-1276">Az.Resources</span></span>
* <span data-ttu-id="7e515-1277">Lägg till ny cmdlet Get-AzureRmDenyAssignment för att hämta tilldelningsnekanden</span><span class="sxs-lookup"><span data-stu-id="7e515-1277">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="7e515-1278">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7e515-1278">Az.Sql</span></span>
* <span data-ttu-id="7e515-1279">Döp om Advanced Threat Protection-cmdletar för Advanced Data Security och aktivera Vulnerability Assessment som standard</span><span class="sxs-lookup"><span data-stu-id="7e515-1279">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="7e515-1280">2.0.0 – maj 2019</span><span class="sxs-lookup"><span data-stu-id="7e515-1280">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7e515-1281">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7e515-1281">Az.Accounts</span></span>
* <span data-ttu-id="7e515-1282">Uppdatera autentiseringsbiblioteket för att åtgärda ADFS-problem med autentisering av användarnamn/lösenord</span><span class="sxs-lookup"><span data-stu-id="7e515-1282">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="7e515-1283">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7e515-1283">Az.CognitiveServices</span></span>
* <span data-ttu-id="7e515-1284">Visa endast Bing-ansvarsfriskrivning för Bing-sökningstjänster.</span><span class="sxs-lookup"><span data-stu-id="7e515-1284">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="7e515-1285">Förbättra felmeddelande när det inte går att skapa konton.</span><span class="sxs-lookup"><span data-stu-id="7e515-1285">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7e515-1286">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7e515-1286">Az.Compute</span></span>
* <span data-ttu-id="7e515-1287">Funktion för närhetsplaceringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="7e515-1287">Proximity placement group feature.</span></span>
    - <span data-ttu-id="7e515-1288">Följande nya cmdletar har lagts till:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="7e515-1288">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="7e515-1289">Den nya parametern ProximityPlacementGroupId har lagts till i följande cmdletar:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="7e515-1289">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="7e515-1290">Parametern StorageAccountType har lagts till i New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="7e515-1290">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="7e515-1291">TargetRegion för New-AzGalleryImageVersion kan innehålla StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="7e515-1291">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="7e515-1292">Växlingsparametern SkipShutdown har lagts till i Stop-AzVM och Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7e515-1292">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="7e515-1293">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="7e515-1293">Breaking changes</span></span>
    - <span data-ttu-id="7e515-1294">Set-AzVMBootDiagnostics har ändrats till Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="7e515-1294">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="7e515-1295">Export-AzLogAnalyticThrottledRequests har ändrats till Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="7e515-1295">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="7e515-1296">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="7e515-1296">Az.DeploymentManager</span></span>
* <span data-ttu-id="7e515-1297">De första allmänt tillgängliga versionerna av cmdletar för Distributionshanteraren i Azure</span><span class="sxs-lookup"><span data-stu-id="7e515-1297">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="7e515-1298">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="7e515-1298">Az.Dns</span></span>
* <span data-ttu-id="7e515-1299">Automatisk delegering av DNS för NameServer</span><span class="sxs-lookup"><span data-stu-id="7e515-1299">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="7e515-1300">Det överordnade zonnamnet kan användas som ytterligare valfri parameter i cmdleten för att skapa DNS-zoner.</span><span class="sxs-lookup"><span data-stu-id="7e515-1300">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="7e515-1301">Lägger till NS-poster för en nyligen skapad underordnad zon i den överordnade zonen.</span><span class="sxs-lookup"><span data-stu-id="7e515-1301">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="7e515-1302">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="7e515-1302">Az.FrontDoor</span></span>
* <span data-ttu-id="7e515-1303">De första allmänt tillgängliga versionerna av cmdletar för Azure FrontDoor</span><span class="sxs-lookup"><span data-stu-id="7e515-1303">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="7e515-1304">Byt namn på WAF-cmdletar så att de omfattar ”Waf”</span><span class="sxs-lookup"><span data-stu-id="7e515-1304">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="7e515-1305">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="7e515-1305">Az.HDInsight</span></span>
* <span data-ttu-id="7e515-1306">Två cmdletar har tagits bort:</span><span class="sxs-lookup"><span data-stu-id="7e515-1306">Removed two cmdlets:</span></span>
    - <span data-ttu-id="7e515-1307">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="7e515-1307">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="7e515-1308">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="7e515-1308">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="7e515-1309">En ny cmdlet har lagts till, Set-AzHDInsightGatewayCredential, som ersätter Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="7e515-1309">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="7e515-1310">Uppdatera cmdleten Get-AzHDInsightJobOutput för att skilja mellan läsarrollen och HDInsight-operatörsrollen:</span><span class="sxs-lookup"><span data-stu-id="7e515-1310">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="7e515-1311">Användare med läsarrollen måste uttryckligen ange parametern ”DefaultStorageAccountKey”, annars uppstår fel.</span><span class="sxs-lookup"><span data-stu-id="7e515-1311">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="7e515-1312">Användare med HDInsight-operatörsrollen påverkas inte.</span><span class="sxs-lookup"><span data-stu-id="7e515-1312">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7e515-1313">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7e515-1313">Az.Monitor</span></span>
* <span data-ttu-id="7e515-1314">Nya cmdletar för SQR API (schemalagd frågeregel)</span><span class="sxs-lookup"><span data-stu-id="7e515-1314">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="7e515-1315">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="7e515-1315">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="7e515-1316">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="7e515-1316">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="7e515-1317">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="7e515-1317">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="7e515-1318">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="7e515-1318">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="7e515-1319">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="7e515-1319">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="7e515-1320">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="7e515-1320">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="7e515-1321">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="7e515-1321">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="7e515-1322">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="7e515-1322">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="7e515-1323">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="7e515-1323">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="7e515-1324">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="7e515-1324">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="7e515-1325">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="7e515-1325">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="7e515-1326">[Mer](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information om SQR API</span><span class="sxs-lookup"><span data-stu-id="7e515-1326">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="7e515-1327">Az.Monitor.md har uppdaterats för att omfatta cmdletar för måttbaserade aviseringsregler i GenV2 (inte klassiska)</span><span class="sxs-lookup"><span data-stu-id="7e515-1327">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7e515-1328">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7e515-1328">Az.Network</span></span>
* <span data-ttu-id="7e515-1329">Lägg till stöd för NAT Gateway-resurs</span><span class="sxs-lookup"><span data-stu-id="7e515-1329">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="7e515-1330">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="7e515-1330">New cmdlets</span></span>
        - <span data-ttu-id="7e515-1331">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="7e515-1331">New-AzNatGateway</span></span>
        - <span data-ttu-id="7e515-1332">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="7e515-1332">Get-AzNatGateway</span></span>
        - <span data-ttu-id="7e515-1333">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="7e515-1333">Set-AzNatGateway</span></span>
        - <span data-ttu-id="7e515-1334">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="7e515-1334">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="7e515-1335">Uppdaterade cmdletar</span><span class="sxs-lookup"><span data-stu-id="7e515-1335">Updated cmdlets</span></span>
        - <span data-ttu-id="7e515-1336">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="7e515-1336">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="7e515-1337">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="7e515-1337">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="7e515-1338">Nedanstående kommandon för funktionen har uppdaterats: Ange/ta bort anpassade vägar på Brooklyn Gateway.</span><span class="sxs-lookup"><span data-stu-id="7e515-1338">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="7e515-1339">New-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ställa in adressprefix som anpassade vägar för att ange gateway.</span><span class="sxs-lookup"><span data-stu-id="7e515-1339">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="7e515-1340">Set-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ange adressprefix som anpassade vägar för att ange gateway.</span><span class="sxs-lookup"><span data-stu-id="7e515-1340">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="7e515-1341">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="7e515-1341">Az.PolicyInsights</span></span>
* <span data-ttu-id="7e515-1342">Stöd för att fråga efter information om principutvärdering.</span><span class="sxs-lookup"><span data-stu-id="7e515-1342">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="7e515-1343">Lägg till parametern ”-Expand” för Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="7e515-1343">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="7e515-1344">Stöd för -Expand PolicyEvaluationDetails.</span><span class="sxs-lookup"><span data-stu-id="7e515-1344">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7e515-1345">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7e515-1345">Az.RecoveryServices</span></span>
* <span data-ttu-id="7e515-1346">Stöd för att dela prenumeration mellan Azure och Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="7e515-1346">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="7e515-1347">Markering av kommande icke-bakåtkompatibla ändringar för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="7e515-1347">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="7e515-1348">Korrigering för återställningsplan och åtgärdsplan i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="7e515-1348">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="7e515-1349">Korrigering för mappning av uppdateringsnätverk i Azure Site Recovery för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="7e515-1349">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="7e515-1350">Korrigering för instruktioner för uppdateringsskydd i Azure Site Recovery för Azure till Azure för hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="7e515-1350">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="7e515-1351">Andra mindre korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="7e515-1351">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="7e515-1352">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="7e515-1352">Az.Relay</span></span>
* <span data-ttu-id="7e515-1353">Korrigera stavfel i kundriktade meddelanden</span><span class="sxs-lookup"><span data-stu-id="7e515-1353">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="7e515-1354">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="7e515-1354">Az.ServiceBus</span></span>
* <span data-ttu-id="7e515-1355">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="7e515-1355">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7e515-1356">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7e515-1356">Az.Storage</span></span>
* <span data-ttu-id="7e515-1357">Uppgradera till lagringsklientbiblioteket 10.0.1 (namnområdet för alla objekt från detta SDK ändras från ”Microsoft.WindowsAzure.Storage. *till ”Microsoft.Azure.Storage.* ”)</span><span class="sxs-lookup"><span data-stu-id="7e515-1357">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="7e515-1358">Uppgradera till Microsoft.Azure.Management.Storage 11.0.0 för att stödja den nya API-versionen 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="7e515-1358">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="7e515-1359">Standardlagringskontot i Skapa lagringskonto ändras från ”Storage” till ”StorageV2”</span><span class="sxs-lookup"><span data-stu-id="7e515-1359">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="7e515-1360">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7e515-1360">New-AzStorageAccount</span></span>
* <span data-ttu-id="7e515-1361">Ändra lagringskontots cmdlet-utdata Sku.Name för att passa med indata-SkuName genom att lägga till ”-”. Till exempel ändras ”StandardLRS” till ”Standard_LRS”</span><span class="sxs-lookup"><span data-stu-id="7e515-1361">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="7e515-1362">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7e515-1362">New-AzStorageAccount</span></span>
    - <span data-ttu-id="7e515-1363">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7e515-1363">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="7e515-1364">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7e515-1364">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7e515-1365">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7e515-1365">Az.Websites</span></span>
* <span data-ttu-id="7e515-1366">Egenskapen ”typ” konfigureras nu för PSSite-objekt som returneras av Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="7e515-1366">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="7e515-1367">Get-AzWebApp\*Metrics och Get-AzAppServicePlanMetrics markeras som inaktuella</span><span class="sxs-lookup"><span data-stu-id="7e515-1367">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="7e515-1368">1.8.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="7e515-1368">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="7e515-1369">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="7e515-1369">Highlights since the last major release</span></span>
* <span data-ttu-id="7e515-1370">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="7e515-1370">General availability of `Az` module</span></span>
* <span data-ttu-id="7e515-1371">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="7e515-1371">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="7e515-1372">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="7e515-1372">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="7e515-1373">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e515-1373">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="7e515-1374">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e515-1374">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="7e515-1375">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e515-1375">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="7e515-1376">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="7e515-1376">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7e515-1377">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7e515-1377">Az.Accounts</span></span>
* <span data-ttu-id="7e515-1378">Uppdatera Uninstall-AzureRm för att ta bort moduler i Mac på ett korrekt sätt</span><span class="sxs-lookup"><span data-stu-id="7e515-1378">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="7e515-1379">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="7e515-1379">Az.Batch</span></span>
* <span data-ttu-id="7e515-1380">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="7e515-1380">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="7e515-1381">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7e515-1381">Az.Cdn</span></span>
* <span data-ttu-id="7e515-1382">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="7e515-1382">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="7e515-1383">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7e515-1383">Az.CognitiveServices</span></span>
* <span data-ttu-id="7e515-1384">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="7e515-1384">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7e515-1385">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7e515-1385">Az.Compute</span></span>
* <span data-ttu-id="7e515-1386">Åtgärda problem med AEM-installationen om resurs-ID:n för diskar innehåller resourcegroups i gemener i resurs-ID:n</span><span class="sxs-lookup"><span data-stu-id="7e515-1386">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="7e515-1387">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="7e515-1387">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7e515-1388">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="7e515-1388">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7e515-1389">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7e515-1389">Az.DataFactory</span></span>
* <span data-ttu-id="7e515-1390">Lägg till SsisProperties om NodeCount inte är null för hanterad integreringskörning.</span><span class="sxs-lookup"><span data-stu-id="7e515-1390">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7e515-1391">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7e515-1391">Az.DataLakeStore</span></span>
* <span data-ttu-id="7e515-1392">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="7e515-1392">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="7e515-1393">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="7e515-1393">Az.EventGrid</span></span>
* <span data-ttu-id="7e515-1394">Hjälptexten för slutpunkten har uppdaterats för att visa att resurser ska skapas innan cmdletarna för att skapa/uppdatera händelseprenumerationer används.</span><span class="sxs-lookup"><span data-stu-id="7e515-1394">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="7e515-1395">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7e515-1395">Az.EventHub</span></span>
* <span data-ttu-id="7e515-1396">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="7e515-1396">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="7e515-1397">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="7e515-1397">Az.HDInsight</span></span>
* <span data-ttu-id="7e515-1398">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="7e515-1398">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7e515-1399">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7e515-1399">Az.IotHub</span></span>
* <span data-ttu-id="7e515-1400">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="7e515-1400">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7e515-1401">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7e515-1401">Az.KeyVault</span></span>
* <span data-ttu-id="7e515-1402">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="7e515-1402">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7e515-1403">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="7e515-1403">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="7e515-1404">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="7e515-1404">Az.MachineLearning</span></span>
* <span data-ttu-id="7e515-1405">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="7e515-1405">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="7e515-1406">Az.Media</span><span class="sxs-lookup"><span data-stu-id="7e515-1406">Az.Media</span></span>
* <span data-ttu-id="7e515-1407">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="7e515-1407">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7e515-1408">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7e515-1408">Az.Monitor</span></span>
  * <span data-ttu-id="7e515-1409">Nya cmdletar för måttbaserad aviseringsregel i GenV2 (inte klassisk)</span><span class="sxs-lookup"><span data-stu-id="7e515-1409">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="7e515-1410">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="7e515-1410">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="7e515-1411">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="7e515-1411">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="7e515-1412">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="7e515-1412">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="7e515-1413">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="7e515-1413">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="7e515-1414">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="7e515-1414">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="7e515-1415">Monitor SDK har uppdaterats till version 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="7e515-1415">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7e515-1416">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7e515-1416">Az.Network</span></span>
* <span data-ttu-id="7e515-1417">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="7e515-1417">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7e515-1418">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="7e515-1418">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="7e515-1419">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="7e515-1419">Az.NotificationHubs</span></span>
* <span data-ttu-id="7e515-1420">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="7e515-1420">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7e515-1421">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7e515-1421">Az.OperationalInsights</span></span>
* <span data-ttu-id="7e515-1422">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="7e515-1422">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="7e515-1423">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="7e515-1423">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="7e515-1424">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="7e515-1424">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7e515-1425">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7e515-1425">Az.RecoveryServices</span></span>
* <span data-ttu-id="7e515-1426">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="7e515-1426">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7e515-1427">Tabellformatet för SQL i virtuella Azure-datorer har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="7e515-1427">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="7e515-1428">En alternativ metod för att hämta platser i AzureFileShare har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e515-1428">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="7e515-1429">ScheduleRunDays i SchedulePolicy-objekt har uppdaterats enligt tidszon</span><span class="sxs-lookup"><span data-stu-id="7e515-1429">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="7e515-1430">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="7e515-1430">Az.RedisCache</span></span>
* <span data-ttu-id="7e515-1431">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="7e515-1431">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7e515-1432">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7e515-1432">Az.Resources</span></span>
* <span data-ttu-id="7e515-1433">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="7e515-1433">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="7e515-1434">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7e515-1434">Az.Sql</span></span>
* <span data-ttu-id="7e515-1435">Ersätt Monitor SDK-beroende med vanlig kod</span><span class="sxs-lookup"><span data-stu-id="7e515-1435">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="7e515-1436">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="7e515-1436">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7e515-1437">Förbättrad process för klassificering av flera kolumner.</span><span class="sxs-lookup"><span data-stu-id="7e515-1437">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="7e515-1438">Inkludera SKU-egenskaper (SKU-namn, serie, kapacitet) i svaret från Get-AzSqlServerServiceObjective och formatera som tabell som standard.</span><span class="sxs-lookup"><span data-stu-id="7e515-1438">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="7e515-1439">Möjlighet att använda Get-AzSqlServerServiceObjective efter plats utan att behöva en redan befintlig server i regionen.</span><span class="sxs-lookup"><span data-stu-id="7e515-1439">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="7e515-1440">Stöd för tidszonsparametern när hanterade instanser skapas.</span><span class="sxs-lookup"><span data-stu-id="7e515-1440">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="7e515-1441">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="7e515-1441">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7e515-1442">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7e515-1442">Az.Websites</span></span>
* <span data-ttu-id="7e515-1443">åtgärdar Set-AzWebApp och Set-AzWebAppSlot så att de inte tar bort taggar vid körning</span><span class="sxs-lookup"><span data-stu-id="7e515-1443">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="7e515-1444">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="7e515-1444">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7e515-1445">SDK för WebSites har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="7e515-1445">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="7e515-1446">Egenskapen AdminSiteName har tagits bort från PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="7e515-1446">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="7e515-1447">1.7.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="7e515-1447">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="7e515-1448">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="7e515-1448">Highlights since the last major release</span></span>
* <span data-ttu-id="7e515-1449">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="7e515-1449">General availability of `Az` module</span></span>
* <span data-ttu-id="7e515-1450">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="7e515-1450">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="7e515-1451">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="7e515-1451">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="7e515-1452">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e515-1452">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="7e515-1453">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e515-1453">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="7e515-1454">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e515-1454">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="7e515-1455">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="7e515-1455">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7e515-1456">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7e515-1456">Az.Accounts</span></span>
* <span data-ttu-id="7e515-1457">Add-AzEnvironment och Set-AzEnvironment har uppdaterats för att godkänna parametern AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="7e515-1457">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="7e515-1458">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="7e515-1458">Az.AnalysisServices</span></span>
* <span data-ttu-id="7e515-1459">ServiceClient används i cmdletar för dataplan och den ursprungliga autentiseringslogiken har tagits bort</span><span class="sxs-lookup"><span data-stu-id="7e515-1459">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="7e515-1460">Add-AzureASAccount används för omslutning av Connect-AzAccount för att undvika en icke-bakåtkompatibel ändring</span><span class="sxs-lookup"><span data-stu-id="7e515-1460">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7e515-1461">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7e515-1461">Az.Automation</span></span>
* <span data-ttu-id="7e515-1462">Buggen för cmdleten New-AzAutomationSoftwareUpdateConfiguration för inkluderingar har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="7e515-1462">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="7e515-1463">Nu bör parametern IncludedKbNumber och IncludedPackageNameMask fungera.</span><span class="sxs-lookup"><span data-stu-id="7e515-1463">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="7e515-1464">Felkorrigering för dynamiska grupper i uppdateringshanteringen för azure automation</span><span class="sxs-lookup"><span data-stu-id="7e515-1464">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7e515-1465">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7e515-1465">Az.Compute</span></span>
* <span data-ttu-id="7e515-1466">Lägg till parametern HyperVGeneration i New-AzDiskConfig och New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="7e515-1466">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="7e515-1467">Tillåt att virtuella datorer skapas med galleribilder från andra klientorganisationer.</span><span class="sxs-lookup"><span data-stu-id="7e515-1467">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="7e515-1468">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="7e515-1468">Az.ContainerInstance</span></span>
* <span data-ttu-id="7e515-1469">Ett problem har åtgärdats i parametern -Command för New-AzContainerGroup som lade till ett avslutande tomt argument</span><span class="sxs-lookup"><span data-stu-id="7e515-1469">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7e515-1470">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7e515-1470">Az.DataFactory</span></span>
* <span data-ttu-id="7e515-1471">ADF .Net SDK-versionen har uppdaterats till 3.0.2</span><span class="sxs-lookup"><span data-stu-id="7e515-1471">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="7e515-1472">Cmdleten Set-AzDataFactoryV2 har uppdaterats med extra parametrar för inställningar som rör RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="7e515-1472">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7e515-1473">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7e515-1473">Az.Resources</span></span>
* <span data-ttu-id="7e515-1474">Förbättra hanteringen av providrar för Get-AzResource när parametrarna -ResourceId eller -ResourceGroupName, -Name och -ResourceType tillhandahålls</span><span class="sxs-lookup"><span data-stu-id="7e515-1474">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="7e515-1475">Förbättra felhanteringen för ”Test-AzDeployment” och ”Test-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="7e515-1475">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="7e515-1476">Hantera fel utanför distributionsvalideringen och ta med dem i kommandoutdata istället</span><span class="sxs-lookup"><span data-stu-id="7e515-1476">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="7e515-1477">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="7e515-1477">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="7e515-1478">Lägg till växlingsparametern -IgnoreDynamicParameters till en uppsättning av cmdletar för distribution för att hoppa över fråga i skript och jobbscenarier</span><span class="sxs-lookup"><span data-stu-id="7e515-1478">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="7e515-1479">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="7e515-1479">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="7e515-1480">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7e515-1480">Az.Sql</span></span>
* <span data-ttu-id="7e515-1481">Stöd för dataklassificering av databaser.</span><span class="sxs-lookup"><span data-stu-id="7e515-1481">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7e515-1482">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7e515-1482">Az.Storage</span></span>
* <span data-ttu-id="7e515-1483">Rapportera detaljfel när lagringskontext skapas med parametern -UseConnectedAccount, men utan inloggning på Azure-kontot</span><span class="sxs-lookup"><span data-stu-id="7e515-1483">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="7e515-1484">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="7e515-1484">New-AzStorageContext</span></span>
* <span data-ttu-id="7e515-1485">Stöd för att hantera Blob Service-egenskaper för ett angivet lagringskonto med API:et för hanteringsplan</span><span class="sxs-lookup"><span data-stu-id="7e515-1485">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="7e515-1486">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="7e515-1486">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="7e515-1487">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="7e515-1487">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="7e515-1488">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="7e515-1488">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="7e515-1489">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="7e515-1489">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="7e515-1490">Stöd för -AsJob-cmdletar för att ladda upp och ladda ned blobar och filer</span><span class="sxs-lookup"><span data-stu-id="7e515-1490">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="7e515-1491">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="7e515-1491">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="7e515-1492">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="7e515-1492">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="7e515-1493">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="7e515-1493">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="7e515-1494">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="7e515-1494">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="7e515-1495">1.6.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="7e515-1495">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="7e515-1496">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="7e515-1496">Highlights since the last major release</span></span>
* <span data-ttu-id="7e515-1497">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="7e515-1497">General availability of `Az` module</span></span>
* <span data-ttu-id="7e515-1498">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="7e515-1498">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="7e515-1499">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="7e515-1499">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="7e515-1500">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e515-1500">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="7e515-1501">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e515-1501">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="7e515-1502">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e515-1502">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="7e515-1503">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="7e515-1503">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7e515-1504">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7e515-1504">Az.Automation</span></span>
* <span data-ttu-id="7e515-1505">Azure Automation – ändring av uppdateringshantering för stöd för de nya funktionerna:</span><span class="sxs-lookup"><span data-stu-id="7e515-1505">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="7e515-1506">Dynamisk gruppering</span><span class="sxs-lookup"><span data-stu-id="7e515-1506">Dynamic grouping</span></span>
    * <span data-ttu-id="7e515-1507">För-/efterskrift</span><span class="sxs-lookup"><span data-stu-id="7e515-1507">Pre-Post script</span></span>
    * <span data-ttu-id="7e515-1508">Inställning för omstart</span><span class="sxs-lookup"><span data-stu-id="7e515-1508">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7e515-1509">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7e515-1509">Az.Compute</span></span>
* <span data-ttu-id="7e515-1510">Åtgärda problem med sökvägsmatchning i Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="7e515-1510">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="7e515-1511">Uppdatera Compute-klientbibliotek till 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="7e515-1511">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7e515-1512">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7e515-1512">Az.KeyVault</span></span>
* <span data-ttu-id="7e515-1513">Stöd för jokertecken för KeyVault-cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e515-1513">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7e515-1514">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7e515-1514">Az.Network</span></span>
* <span data-ttu-id="7e515-1515">Lägg till stöd för Threat Intelligence för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="7e515-1515">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="7e515-1516">Lägg till resurs för brandväggsprincip på översta nivå och anpassade regler för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="7e515-1516">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7e515-1517">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7e515-1517">Az.RecoveryServices</span></span>
* <span data-ttu-id="7e515-1518">SnapshotRetentionInDays har lagts till i Azure-principen för virtuella datorer för stöd av Instant RP</span><span class="sxs-lookup"><span data-stu-id="7e515-1518">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="7e515-1519">Pipe-stöd för avregistrering av container har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e515-1519">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="7e515-1520">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7e515-1520">Az.Resources</span></span>
* <span data-ttu-id="7e515-1521">Uppdatera stöd för jokertecken för Get-AzResource och Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7e515-1521">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="7e515-1522">Uppdatera autentiseringsuppgifter som används vid allmänna anrop till ARM</span><span class="sxs-lookup"><span data-stu-id="7e515-1522">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="7e515-1523">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7e515-1523">Az.Sql</span></span>
* <span data-ttu-id="7e515-1524">Cmdlet-parametern (ExcludeDetectionType) för Hotidentifiering ändrades från DetectionType till sträng[] för att framtidssäkra den när nya DetectionTypes läggs till, och även för att stödja automatisk ifyllning.</span><span class="sxs-lookup"><span data-stu-id="7e515-1524">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7e515-1525">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7e515-1525">Az.Storage</span></span>
* <span data-ttu-id="7e515-1526">Stöd för att hämta/ange/ta bort hanteringsprincip på ett lagringskonto</span><span class="sxs-lookup"><span data-stu-id="7e515-1526">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="7e515-1527">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="7e515-1527">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="7e515-1528">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="7e515-1528">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="7e515-1529">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="7e515-1529">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="7e515-1530">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="7e515-1530">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="7e515-1531">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="7e515-1531">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="7e515-1532">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="7e515-1532">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7e515-1533">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7e515-1533">Az.Websites</span></span>
* <span data-ttu-id="7e515-1534">Åtgärda fel med ARM-mall som avbryter kloning av alla platser med 'New-AzWebApp -IncludeSourceWebAppSlots'</span><span class="sxs-lookup"><span data-stu-id="7e515-1534">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="7e515-1535">1.5.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="7e515-1535">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7e515-1536">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7e515-1536">Az.Accounts</span></span>
* <span data-ttu-id="7e515-1537">Lägg till kommandot Register-AzModule för stöd för AutoRest-genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="7e515-1537">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="7e515-1538">Uppdatera exempel för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="7e515-1538">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7e515-1539">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7e515-1539">Az.Automation</span></span>
* <span data-ttu-id="7e515-1540">Problem med att hämta vissa månadsscheman i flera Azure Automation-cmdletar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="7e515-1540">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="7e515-1541">Åtgärda problem med att Get-AzAutomationDscNode bara returnerar de 20 översta noderna.</span><span class="sxs-lookup"><span data-stu-id="7e515-1541">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="7e515-1542">Nu returneras alla noder</span><span class="sxs-lookup"><span data-stu-id="7e515-1542">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="7e515-1543">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7e515-1543">Az.Cdn</span></span>
* <span data-ttu-id="7e515-1544">Nya Powershell-cmdletar för att aktivera/inaktivera anpassade domän-HTTPS har lagts till och de gamla har gjorts inaktuella</span><span class="sxs-lookup"><span data-stu-id="7e515-1544">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7e515-1545">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7e515-1545">Az.Compute</span></span>
* <span data-ttu-id="7e515-1546">Lägg till stöd för jokertecken för Get-cmdletar</span><span class="sxs-lookup"><span data-stu-id="7e515-1546">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7e515-1547">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7e515-1547">Az.DataFactory</span></span>
* <span data-ttu-id="7e515-1548">ADF .Net SDK-versionen har uppdaterats till 3.0.1</span><span class="sxs-lookup"><span data-stu-id="7e515-1548">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="7e515-1549">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="7e515-1549">Az.LogicApp</span></span>
* <span data-ttu-id="7e515-1550">Åtgärda problemet med att ListWorkflows endast hämtar den första sidan med resultat</span><span class="sxs-lookup"><span data-stu-id="7e515-1550">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7e515-1551">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7e515-1551">Az.Network</span></span>
* <span data-ttu-id="7e515-1552">Lägg till stöd för jokertecken för Network-cmdletar</span><span class="sxs-lookup"><span data-stu-id="7e515-1552">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7e515-1553">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7e515-1553">Az.RecoveryServices</span></span>
* <span data-ttu-id="7e515-1554">Stöd har lagts till för SQL Server i virtuella Azure-datorer</span><span class="sxs-lookup"><span data-stu-id="7e515-1554">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="7e515-1555">SDK-uppdatering</span><span class="sxs-lookup"><span data-stu-id="7e515-1555">SDK Update</span></span>
* <span data-ttu-id="7e515-1556">Get-ProtectableItem-incheckning i VMappContainer har tagits bort</span><span class="sxs-lookup"><span data-stu-id="7e515-1556">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="7e515-1557">Name och ServerName har lagts till som parametrar för Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="7e515-1557">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="7e515-1558">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7e515-1558">Az.Resources</span></span>
* <span data-ttu-id="7e515-1559">Lägg till parametern `-TemplateObject` i cmdletar för distribution</span><span class="sxs-lookup"><span data-stu-id="7e515-1559">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="7e515-1560">Mer information här: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="7e515-1560">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="7e515-1561">Åtgärda problem med piping av resultatet i `Get-AzResource` till `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="7e515-1561">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="7e515-1562">Mer information här: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="7e515-1562">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="7e515-1563">Åtgärda problem med ändring av JSON-datatyp när `Set-AzResource` körs</span><span class="sxs-lookup"><span data-stu-id="7e515-1563">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="7e515-1564">Mer information här: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="7e515-1564">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="7e515-1565">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7e515-1565">Az.Sql</span></span>
* <span data-ttu-id="7e515-1566">AuditingEndpointsCommunicator uppdateras.</span><span class="sxs-lookup"><span data-stu-id="7e515-1566">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="7e515-1567">Åtgärdar beteendet hos ett gränsscenario när nya diagnostikinställningar skapas.</span><span class="sxs-lookup"><span data-stu-id="7e515-1567">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7e515-1568">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7e515-1568">Az.Storage</span></span>
* <span data-ttu-id="7e515-1569">Stöd för BlockBlobStorage när Storage-konto skapas      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7e515-1569">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="7e515-1570">1.4.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="7e515-1570">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="7e515-1571">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="7e515-1571">Az.AnalysisServices</span></span>
* <span data-ttu-id="7e515-1572">Inaktuell AddAzureASAccount-cmdlet</span><span class="sxs-lookup"><span data-stu-id="7e515-1572">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7e515-1573">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7e515-1573">Az.Automation</span></span>
* <span data-ttu-id="7e515-1574">Hjälpen för Import-AzAutomationDscNodeConfiguration har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="7e515-1574">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="7e515-1575">Konfigurationsnamnsvalidering har lagts till i cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="7e515-1575">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="7e515-1576">Förbättrad felhantering för cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="7e515-1576">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="7e515-1577">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7e515-1577">Az.CognitiveServices</span></span>
* <span data-ttu-id="7e515-1578">CustomSubdomainName har lagts till som en ny valfri parameter för New-AzCognitiveServicesAccount, som används för att ange underdomän för resursen.</span><span class="sxs-lookup"><span data-stu-id="7e515-1578">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7e515-1579">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7e515-1579">Az.Compute</span></span>
* <span data-ttu-id="7e515-1580">Problemet med ID-parameteruppsättningar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="7e515-1580">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="7e515-1581">Get-AzVMExtension har uppdaterats så att alla installerade tillägg visas om parametern Name inte har angetts</span><span class="sxs-lookup"><span data-stu-id="7e515-1581">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="7e515-1582">Parametrarna Tag och ResourceId har lagts till i cmdleten Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="7e515-1582">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="7e515-1583">Get-AzVmssVM utan instans-ID och med InstanceView kan visa virtuella VMSS-datorer med instansvyn.</span><span class="sxs-lookup"><span data-stu-id="7e515-1583">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7e515-1584">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7e515-1584">Az.DataLakeStore</span></span>
* <span data-ttu-id="7e515-1585">Cmdletar har lagts till för uppräkning och återställning av borttagna objekt i ADL</span><span class="sxs-lookup"><span data-stu-id="7e515-1585">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="7e515-1586">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7e515-1586">Az.EventHub</span></span>
* <span data-ttu-id="7e515-1587">Ny boolesk egenskap SkipEmptyArchives har lagts till i Skip Empty Archives i CaptureDescription-klassen i Eventhub</span><span class="sxs-lookup"><span data-stu-id="7e515-1587">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="7e515-1588">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7e515-1588">Az.KeyVault</span></span>
* <span data-ttu-id="7e515-1589">Taggning i Set-AzKeyVaultSecret har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="7e515-1589">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="7e515-1590">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="7e515-1590">Az.LogicApp</span></span>
* <span data-ttu-id="7e515-1591">Grundläggande SKU har lagts till för Integrationskonton</span><span class="sxs-lookup"><span data-stu-id="7e515-1591">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="7e515-1592">XSLT 2.0, XSLT 3.0 och Flytande mappningstyper har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e515-1592">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="7e515-1593">Nya cmdletar för integrationskontosammansättningar</span><span class="sxs-lookup"><span data-stu-id="7e515-1593">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="7e515-1594">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="7e515-1594">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="7e515-1595">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="7e515-1595">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="7e515-1596">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="7e515-1596">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="7e515-1597">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="7e515-1597">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="7e515-1598">Nya cmdletar för batchkonfiguration för integrationskonto</span><span class="sxs-lookup"><span data-stu-id="7e515-1598">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="7e515-1599">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="7e515-1599">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="7e515-1600">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="7e515-1600">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="7e515-1601">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="7e515-1601">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="7e515-1602">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="7e515-1602">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="7e515-1603">Logic App-SDK har uppdaterats till version 4.1.0</span><span class="sxs-lookup"><span data-stu-id="7e515-1603">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7e515-1604">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7e515-1604">Az.Monitor</span></span>
* <span data-ttu-id="7e515-1605">Hjälpen för Get-AzMetric har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="7e515-1605">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7e515-1606">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7e515-1606">Az.Network</span></span>
* <span data-ttu-id="7e515-1607">Hjälpexempel för Add-AzApplicationGatewayCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e515-1607">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7e515-1608">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7e515-1608">Az.OperationalInsights</span></span>
* <span data-ttu-id="7e515-1609">Ytterligare stöd för datakällorna New och Get ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="7e515-1609">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="7e515-1610">Ny ApplicationInsights-typ har lagts till för att ge stöd för ”Get specific” och ”Get all” för ApplicationInsights-datakällor för angiven arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="7e515-1610">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="7e515-1611">Cmdleten New-AzOperationalInsightsApplicationInsightsDataSource har lagts till för att skapa datakälla med angivna parametrar för Application Insights-resurs: subscription Id, resourceGroupName och name.</span><span class="sxs-lookup"><span data-stu-id="7e515-1611">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="7e515-1612">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7e515-1612">Az.Resources</span></span>
* <span data-ttu-id="7e515-1613">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="7e515-1613">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="7e515-1614">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="7e515-1614">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="7e515-1615">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="7e515-1615">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="7e515-1616">Fel som gör att KeyCredentials inte kan skapas upprepade gånger har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="7e515-1616">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="7e515-1617">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7e515-1617">Az.Sql</span></span>
* <span data-ttu-id="7e515-1618">Lägg till stöd för hyperskalanivån för SQL DB</span><span class="sxs-lookup"><span data-stu-id="7e515-1618">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="7e515-1619">Ett fel har åtgärdats där återställningen kunde misslyckas på grund av onödiga inställningsegenskaper i restore-förfrågan</span><span class="sxs-lookup"><span data-stu-id="7e515-1619">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7e515-1620">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7e515-1620">Az.Websites</span></span>
* <span data-ttu-id="7e515-1621">Rätt exempel i Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="7e515-1621">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="7e515-1622">1.3.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="7e515-1622">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7e515-1623">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7e515-1623">Az.Accounts</span></span>
* <span data-ttu-id="7e515-1624">Uppdatera till den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="7e515-1624">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="7e515-1625">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="7e515-1625">Az.AnalysisServices</span></span>
<span data-ttu-id="7e515-1626">Allmän tillgänglighet för Az.AnalysisServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="7e515-1626">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7e515-1627">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7e515-1627">Az.Compute</span></span>
* <span data-ttu-id="7e515-1628">AEM-tillägg: Lägg till stöd för UltraSSD-, P60-, P70- och P80-diskar</span><span class="sxs-lookup"><span data-stu-id="7e515-1628">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="7e515-1629">Uppdatera hjälpbeskrivning för Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="7e515-1629">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="7e515-1630">Uppdatera hjälpbeskrivning och exempel för Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="7e515-1630">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7e515-1631">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7e515-1631">Az.RecoveryServices</span></span>
<span data-ttu-id="7e515-1632">Allmän tillgänglighet för Az.RecoveryServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="7e515-1632">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7e515-1633">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7e515-1633">Az.Resources</span></span>
* <span data-ttu-id="7e515-1634">Korrigera taggar för resursgrupper</span><span class="sxs-lookup"><span data-stu-id="7e515-1634">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="7e515-1635">Mer information här: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="7e515-1635">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="7e515-1636">Åtgärda problem där `Get-AzureRmRoleAssignment` inte respekterar -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="7e515-1636">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="7e515-1637">Mer information här: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="7e515-1637">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="7e515-1638">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7e515-1638">Az.Sql</span></span>
* <span data-ttu-id="7e515-1639">Lägga till Get/Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="7e515-1639">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="7e515-1640">Åtgärda problem där ett nullref-undantag uppstår när du kör SQL-cmdletar och inte är inloggad på ett Azure-konto</span><span class="sxs-lookup"><span data-stu-id="7e515-1640">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="7e515-1641">Åtgärda nullref-undantag i Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="7e515-1641">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="7e515-1642">1.2.1 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="7e515-1642">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7e515-1643">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7e515-1643">Az.Accounts</span></span>
* <span data-ttu-id="7e515-1644">Version med rätt version av autentisering</span><span class="sxs-lookup"><span data-stu-id="7e515-1644">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="7e515-1645">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="7e515-1645">Az.AnalysisServices</span></span>
* <span data-ttu-id="7e515-1646">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="7e515-1646">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7e515-1647">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7e515-1647">Az.RecoveryServices</span></span>
* <span data-ttu-id="7e515-1648">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="7e515-1648">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="7e515-1649">1.2.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="7e515-1649">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7e515-1650">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7e515-1650">Az.Accounts</span></span>
* <span data-ttu-id="7e515-1651">Lägga till interaktiv autentisering och autentisering med användarnamn/lösenord för endast Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="7e515-1651">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="7e515-1652">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="7e515-1652">Update incorrect online help URLs</span></span>
* <span data-ttu-id="7e515-1653">Lägga till varningsmeddelande i PS Core för Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="7e515-1653">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="7e515-1654">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="7e515-1654">Az.Aks</span></span>
* <span data-ttu-id="7e515-1655">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="7e515-1655">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7e515-1656">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7e515-1656">Az.Automation</span></span>
* <span data-ttu-id="7e515-1657">Stöd för Python 2-runbookflöden har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e515-1657">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="7e515-1658">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="7e515-1658">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="7e515-1659">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7e515-1659">Az.Cdn</span></span>
* <span data-ttu-id="7e515-1660">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="7e515-1660">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7e515-1661">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7e515-1661">Az.Compute</span></span>
* <span data-ttu-id="7e515-1662">Lägga till cmdleten Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="7e515-1662">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="7e515-1663">Lägga till TempDisk-parameter i Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7e515-1663">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="7e515-1664">Korrigera varningsmeddelande för New-AzVM</span><span class="sxs-lookup"><span data-stu-id="7e515-1664">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="7e515-1665">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="7e515-1665">Az.ContainerRegistry</span></span>
* <span data-ttu-id="7e515-1666">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="7e515-1666">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7e515-1667">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7e515-1667">Az.DataFactory</span></span>
* <span data-ttu-id="7e515-1668">ADF .Net SDK-versionen har uppdaterats till 3.0.0</span><span class="sxs-lookup"><span data-stu-id="7e515-1668">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7e515-1669">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7e515-1669">Az.DataLakeStore</span></span>
* <span data-ttu-id="7e515-1670">Åtgärda problem med ADLS-slutpunkt vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="7e515-1670">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="7e515-1671">Mer information här: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="7e515-1671">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="7e515-1672">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="7e515-1672">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7e515-1673">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7e515-1673">Az.IotHub</span></span>
* <span data-ttu-id="7e515-1674">Lägga till kodningsformat i cmdleten Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="7e515-1674">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7e515-1675">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7e515-1675">Az.KeyVault</span></span>
* <span data-ttu-id="7e515-1676">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="7e515-1676">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7e515-1677">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7e515-1677">Az.Network</span></span>
* <span data-ttu-id="7e515-1678">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="7e515-1678">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="7e515-1679">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7e515-1679">Az.Resources</span></span>
* <span data-ttu-id="7e515-1680">Åtgärda felaktiga exempel i referensdokumentationen ”New-AzADAppCredential” och ”New-AzADSpCredential”</span><span class="sxs-lookup"><span data-stu-id="7e515-1680">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="7e515-1681">Åtgärda problem där sökvägen för parametern ”-TemplateFile” inte omvandlas innan cmdletarna för distribution i resursgruppen körs</span><span class="sxs-lookup"><span data-stu-id="7e515-1681">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="7e515-1682">Az.Resources: Korrigera dokumentationen om standardvärdet för New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="7e515-1682">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="7e515-1683">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="7e515-1683">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="7e515-1684">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="7e515-1684">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="7e515-1685">Åtgärda formateringsproblemet med objektet ”PSResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="7e515-1685">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="7e515-1686">Mer information här: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="7e515-1686">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="7e515-1687">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7e515-1687">Az.ServiceFabric</span></span>
* <span data-ttu-id="7e515-1688">Återställ när ett certifikat läggs till i en Virtual Machine Scale Sets-modell men ett undantag genereras. Detta har gjorts för att åtgärda följande fel: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="7e515-1688">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="7e515-1689">Korrigera några felmeddelanden.</span><span class="sxs-lookup"><span data-stu-id="7e515-1689">Fix some error messages.</span></span>
* <span data-ttu-id="7e515-1690">Korrigering av skapande av kluster med ARM-mall som är standard för New-AzServiceFabriCluster som inte fungerade med migrering till Az.</span><span class="sxs-lookup"><span data-stu-id="7e515-1690">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="7e515-1691">Korrigering av tilläggning av kluster/programcertifikat så att endast VM Scale Sets som motsvarar klustret läggs till genom att kontrollera ID för klustret i tillägget.</span><span class="sxs-lookup"><span data-stu-id="7e515-1691">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="7e515-1692">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="7e515-1692">Az.SignalR</span></span>
* <span data-ttu-id="7e515-1693">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="7e515-1693">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="7e515-1694">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7e515-1694">Az.Sql</span></span>
* <span data-ttu-id="7e515-1695">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="7e515-1695">Update incorrect online help URLs</span></span>
* <span data-ttu-id="7e515-1696">Uppdaterad parameterbeskrivning för LicenseType-parameter med möjliga värden</span><span class="sxs-lookup"><span data-stu-id="7e515-1696">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="7e515-1697">Korrigering för att uppdatera hanterad instansidentitet som inte fungerar när det är den enda uppdaterade egenskapen</span><span class="sxs-lookup"><span data-stu-id="7e515-1697">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="7e515-1698">Stöd för anpassad sortering på hanterad instans</span><span class="sxs-lookup"><span data-stu-id="7e515-1698">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7e515-1699">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7e515-1699">Az.Storage</span></span>
* <span data-ttu-id="7e515-1700">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="7e515-1700">Update incorrect online help URLs</span></span>
* <span data-ttu-id="7e515-1701">Tillhandahåll detaljerat felmeddelande när en användare försöker hämta/konfigurera klassisk loggning/mått på ett Premium Storage-konto eftersom Premium Storage-kontot inte har stöd för klassisk loggning/mått.</span><span class="sxs-lookup"><span data-stu-id="7e515-1701">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="7e515-1702">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="7e515-1702">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="7e515-1703">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="7e515-1703">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="7e515-1704">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="7e515-1704">Az.TrafficManager</span></span>
* <span data-ttu-id="7e515-1705">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="7e515-1705">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7e515-1706">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7e515-1706">Az.Websites</span></span>
* <span data-ttu-id="7e515-1707">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="7e515-1707">Update incorrect online help URLs</span></span>
* <span data-ttu-id="7e515-1708">Korrigerar ”New-AzWebAppSSLBinding” så att certifikatet laddas upp till rätt resursgrupp och plats om appen finns i en ASE.</span><span class="sxs-lookup"><span data-stu-id="7e515-1708">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="7e515-1709">Korrigerar ”New-AzWebAppSSLBinding” så att taggarna inte skrivs över på en bindning av ett SSL-certifikat till en app</span><span class="sxs-lookup"><span data-stu-id="7e515-1709">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="7e515-1710">1.1.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="7e515-1710">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7e515-1711">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7e515-1711">Az.Accounts</span></span>
* <span data-ttu-id="7e515-1712">Lade till omfattningen ”Lokal” till Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="7e515-1712">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7e515-1713">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7e515-1713">Az.Compute</span></span>
* <span data-ttu-id="7e515-1714">Namn är nu valfritt i ID-parametern för Restart/Start/Stop/Remove/Set-AzVM och Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="7e515-1714">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="7e515-1715">Uppdaterade beskrivningen av ID i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="7e515-1715">Updated the description of ID in help files</span></span>
* <span data-ttu-id="7e515-1716">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7e515-1716">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7e515-1717">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7e515-1717">Az.DataLakeStore</span></span>
* <span data-ttu-id="7e515-1718">Uppdatera sdk-versionen av dataplanet till 1.1.14 för SDK-korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="7e515-1718">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="7e515-1719">Korrigerade hanteringen av negativ accesstime och modificationtime för getfilestatus och liststatus; korrigera asynkront annulleringstoken</span><span class="sxs-lookup"><span data-stu-id="7e515-1719">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="7e515-1720">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="7e515-1720">Az.EventGrid</span></span>
* <span data-ttu-id="7e515-1721">Uppdaterat för användning av API-versionen 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="7e515-1721">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="7e515-1722">Uppdaterade följande cmdletar för att stödja nytt scenario i API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="7e515-1722">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="7e515-1723">New-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="7e515-1723">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="7e515-1724">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="7e515-1724">Event Time-To-Live,</span></span>
        - <span data-ttu-id="7e515-1725">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="7e515-1725">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="7e515-1726">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="7e515-1726">Dead letter endpoint.</span></span>
    - <span data-ttu-id="7e515-1727">Update-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="7e515-1727">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="7e515-1728">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="7e515-1728">Event Time-To-Live,</span></span>
        - <span data-ttu-id="7e515-1729">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="7e515-1729">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="7e515-1730">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="7e515-1730">Dead letter endpoint.</span></span>
* <span data-ttu-id="7e515-1731">Lade till nya enum-värden (storageQueue och hybridConnection) för alternativet EndpointType i cmdletarna New-AzureRmEventGridSubscription och Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="7e515-1731">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="7e515-1732">Visa varningsmeddelanden om skapande eller uppdatering av händelseprenumerationen förväntas medföra manuell åtgärd från användaren.</span><span class="sxs-lookup"><span data-stu-id="7e515-1732">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7e515-1733">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7e515-1733">Az.IotHub</span></span>
* <span data-ttu-id="7e515-1734">Har uppdaterats till den senaste versionen av SDK:n lotHub</span><span class="sxs-lookup"><span data-stu-id="7e515-1734">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="7e515-1735">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="7e515-1735">Az.LogicApp</span></span>
* <span data-ttu-id="7e515-1736">Get-AzLogicApp visar en lista över alla som inte har angivet namn</span><span class="sxs-lookup"><span data-stu-id="7e515-1736">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="7e515-1737">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7e515-1737">Az.Resources</span></span>
* <span data-ttu-id="7e515-1738">Åtgärdade problem med parameteruppsättningen när parametrarna -ODataQuery och -ResourceId anges för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="7e515-1738">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="7e515-1739">Mer information här: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="7e515-1739">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="7e515-1740">Åtgärdade hantering av parametern -Custom i New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="7e515-1740">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="7e515-1741">Korrigerade stavfel i New-AzDeployment-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="7e515-1741">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="7e515-1742">Gjorde parametern -MailNickname obligatorisk för New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="7e515-1742">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="7e515-1743">Mer information här: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="7e515-1743">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="7e515-1744">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="7e515-1744">Az.SignalR</span></span>
* <span data-ttu-id="7e515-1745">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7e515-1745">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="7e515-1746">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7e515-1746">Az.Sql</span></span>
* <span data-ttu-id="7e515-1747">Konverterade lagringshanteringsklientens beroende av den normala SDK-implementeringen.</span><span class="sxs-lookup"><span data-stu-id="7e515-1747">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7e515-1748">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7e515-1748">Az.Storage</span></span>
* <span data-ttu-id="7e515-1749">Angav StorageAccountName för lagringskontext som det verkliga namnet på lagringskontot när det skapas med Sas Token, OAuth eller Anonymous</span><span class="sxs-lookup"><span data-stu-id="7e515-1749">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="7e515-1750">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="7e515-1750">New-AzStorageContext</span></span>
* <span data-ttu-id="7e515-1751">Skapade Sas Token för Blob Snapshot-objekt med parametern -FullUri, åtgärdade den returnerade URI:n så att den blir URI för ögonblicksbild</span><span class="sxs-lookup"><span data-stu-id="7e515-1751">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="7e515-1752">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="7e515-1752">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7e515-1753">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7e515-1753">Az.Websites</span></span>
* <span data-ttu-id="7e515-1754">Åtgärdade en bugg i datumparsningen i Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="7e515-1754">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="7e515-1755">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7e515-1755">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="7e515-1756">1.0.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="7e515-1756">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="7e515-1757">Allmänt</span><span class="sxs-lookup"><span data-stu-id="7e515-1757">General</span></span>

- <span data-ttu-id="7e515-1758">Allmän tillgänglighet för Az-modulen</span><span class="sxs-lookup"><span data-stu-id="7e515-1758">General Availability of Az Module</span></span>
- <span data-ttu-id="7e515-1759">Onlinehjälp för varje modul</span><span class="sxs-lookup"><span data-stu-id="7e515-1759">Online help for each module</span></span>
- <span data-ttu-id="7e515-1760">Mer information och en översikt finns på [Az-informationssidan](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="7e515-1760">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="7e515-1761">Information om hur du migrerar från AzureRM finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7e515-1761">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="7e515-1762">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7e515-1762">Az.Accounts</span></span>
- <span data-ttu-id="7e515-1763">Har ändrats från Az.Profile</span><span class="sxs-lookup"><span data-stu-id="7e515-1763">Changed from Az.Profile</span></span>
- <span data-ttu-id="7e515-1764">Fasta tabellformat för profil- och kontexttyper</span><span class="sxs-lookup"><span data-stu-id="7e515-1764">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="7e515-1765">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7e515-1765">Az.ApiManagement</span></span>
- <span data-ttu-id="7e515-1766">Korrigeringar för #7002</span><span class="sxs-lookup"><span data-stu-id="7e515-1766">Fixes for #7002</span></span>
- <span data-ttu-id="7e515-1767">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7e515-1767">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="7e515-1768">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="7e515-1768">Az.Batch</span></span>
- <span data-ttu-id="7e515-1769">Lade till möjligheten att se vilken version av Azure Batch Node Agent som körs på var och en av de virtuella datorerna i en pool, via den nya egenskapen `NodeAgentInformation` på `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="7e515-1769">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="7e515-1770">Standarden `Caching` för `PSDataDisk` är nu `ReadWrite` i stället för `None`.</span><span class="sxs-lookup"><span data-stu-id="7e515-1770">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="7e515-1771">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7e515-1771">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="7e515-1772">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="7e515-1772">Az.Billing</span></span>
- <span data-ttu-id="7e515-1773">Kombinerar cmdletarna för fakturering, förbrukning och UsageAggregates. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7e515-1773">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="7e515-1774">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="7e515-1774">Az.CognitivServices</span></span>
- <span data-ttu-id="7e515-1775">Lade till kompletterare för SkuName och Typem som är tillgängliga i New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="7e515-1775">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="7e515-1776">Tog bort parameteruppsättningen GetSkusWithAccountParamSetName från Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="7e515-1776">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="7e515-1777">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="7e515-1777">Az.ContainerInstance</span></span>
- <span data-ttu-id="7e515-1778">Stöd för ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="7e515-1778">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="7e515-1779">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="7e515-1779">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="7e515-1780">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7e515-1780">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="7e515-1781">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7e515-1781">Az.DataLakeStore</span></span>
- <span data-ttu-id="7e515-1782">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7e515-1782">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="7e515-1783">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7e515-1783">Az.Monitor</span></span>
- <span data-ttu-id="7e515-1784">Döpte om Az.Insights till Az.Monitor och andra mindre icke-bakåtkompatibla ändringar. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7e515-1784">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="7e515-1785">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7e515-1785">Az.KeyVault</span></span>
- <span data-ttu-id="7e515-1786">Tog bort den inaktuella egenskapen PurgeDisabled från utdatatyper</span><span class="sxs-lookup"><span data-stu-id="7e515-1786">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="7e515-1787">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="7e515-1787">Az.MachineLearning</span></span>
- <span data-ttu-id="7e515-1788">Inkluderade cmdletarna från modulen Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="7e515-1788">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="7e515-1789">Az.Media</span><span class="sxs-lookup"><span data-stu-id="7e515-1789">Az.Media</span></span>
- <span data-ttu-id="7e515-1790">Tog bort inaktuella -Tags-alias från New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="7e515-1790">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="7e515-1791">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7e515-1791">Az.Network</span></span>
<span data-ttu-id="7e515-1792">Stöd har lagts till för konfiguration av RewriteRuleSets i Application Gateway</span><span class="sxs-lookup"><span data-stu-id="7e515-1792">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="7e515-1793">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="7e515-1793">New cmdlets added:</span></span>
        - <span data-ttu-id="7e515-1794">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7e515-1794">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="7e515-1795">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7e515-1795">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="7e515-1796">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7e515-1796">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="7e515-1797">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7e515-1797">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="7e515-1798">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7e515-1798">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="7e515-1799">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="7e515-1799">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="7e515-1800">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="7e515-1800">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="7e515-1801">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="7e515-1801">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="7e515-1802">Cmdletar har uppdaterats med den valfria parametern -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7e515-1802">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="7e515-1803">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7e515-1803">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="7e515-1804">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="7e515-1804">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="7e515-1805">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="7e515-1805">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="7e515-1806">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7e515-1806">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="7e515-1807">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7e515-1807">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="7e515-1808">New-AzureRmApplicationGatewayUrlPathMapConfig har lagt till KeyVault-stöd för Application Gateway med Identity.</span><span class="sxs-lookup"><span data-stu-id="7e515-1808">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="7e515-1809">Cmdletar har uppdaterats med den valfria parametern -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="7e515-1809">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="7e515-1810">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7e515-1810">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="7e515-1811">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7e515-1811">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="7e515-1812">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7e515-1812">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="7e515-1813">Cmdleten New-AzApplicationGateway har uppdaterats med den valfria parametern -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="7e515-1813">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="7e515-1814">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7e515-1814">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="7e515-1815">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7e515-1815">Az.OperationalInsights</span></span>
- <span data-ttu-id="7e515-1816">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7e515-1816">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="7e515-1817">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="7e515-1817">Az.Profile</span></span>
- <span data-ttu-id="7e515-1818">Modulnamnet har ändrats till Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7e515-1818">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="7e515-1819">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7e515-1819">Az.RecoveryServices</span></span>
- <span data-ttu-id="7e515-1820">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7e515-1820">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="7e515-1821">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7e515-1821">Az.Resources</span></span>
- <span data-ttu-id="7e515-1822">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7e515-1822">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="7e515-1823">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7e515-1823">Az.ServiceFabric</span></span>
- <span data-ttu-id="7e515-1824">Stöd för specificering av certifikat efter eget namn och tumavtryck</span><span class="sxs-lookup"><span data-stu-id="7e515-1824">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="7e515-1825">Information om fler icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7e515-1825">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="7e515-1826">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="7e515-1826">Az.SIgnalR</span></span>
- <span data-ttu-id="7e515-1827">Allmän tillgänglighet för PowerShell-cmdletar för SIgnalR</span><span class="sxs-lookup"><span data-stu-id="7e515-1827">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="7e515-1828">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7e515-1828">Az.Sql</span></span>
- <span data-ttu-id="7e515-1829">Lade till de nya identifieringstyperna Data_Exfiltration och Unsafe_Action i Threat Detection-cmdletar</span><span class="sxs-lookup"><span data-stu-id="7e515-1829">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="7e515-1830">Uppdaterade dokumentationsexempel för Sql Auditing-cmdletar</span><span class="sxs-lookup"><span data-stu-id="7e515-1830">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="7e515-1831">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7e515-1831">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="7e515-1832">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7e515-1832">Az.Storage</span></span>
- <span data-ttu-id="7e515-1833">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7e515-1833">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="7e515-1834">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7e515-1834">Az.Websites</span></span>
- <span data-ttu-id="7e515-1835">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7e515-1835">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="7e515-1836">0.7.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="7e515-1836">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="7e515-1837">Allmänt</span><span class="sxs-lookup"><span data-stu-id="7e515-1837">General</span></span>

* <span data-ttu-id="7e515-1838">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="7e515-1838">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="7e515-1839">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7e515-1839">Az.Compute</span></span>

* <span data-ttu-id="7e515-1840">Lade till stöd för UltraSSD och Galleriavbildningar i de enkla parameteruppsättningarna för `New-AzVm(ss)`-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="7e515-1840">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="7e515-1841">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7e515-1841">Az.DataLakeStore</span></span>

* <span data-ttu-id="7e515-1842">Åtgärdade avslutande snedstreck i domänen för adls-konto</span><span class="sxs-lookup"><span data-stu-id="7e515-1842">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="7e515-1843">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="7e515-1843">Az.FrontDoor</span></span>

* <span data-ttu-id="7e515-1844">Brutna länkar korrigerades</span><span class="sxs-lookup"><span data-stu-id="7e515-1844">Fixed some broken links</span></span>
    - <span data-ttu-id="7e515-1845">I artiklarna New-AzureRmFrontDoor och Set-AzureRmFrontDoor artiklar korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="7e515-1845">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="7e515-1846">I artikeln New-AzureRmFrontDoorManagedRuleObject korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="7e515-1846">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="7e515-1847">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7e515-1847">Az.RecoveryServices</span></span>

* <span data-ttu-id="7e515-1848">Lade till valideringar på klientsidan för Azure-filresurs med återställningsåtgärder.</span><span class="sxs-lookup"><span data-stu-id="7e515-1848">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="7e515-1849">Gjorde storageAccountName och storageAccountResourceGroupName valfritt för afs-återställning.</span><span class="sxs-lookup"><span data-stu-id="7e515-1849">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="7e515-1850">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7e515-1850">Az.Resources</span></span>

* <span data-ttu-id="7e515-1851">Korrigering för https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="7e515-1851">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="7e515-1852">Uppdaterade Get-AzureRmRoleAssignment så att prenumerationsomfattningen används om den anges vid begäran om klassiska administratörer.</span><span class="sxs-lookup"><span data-stu-id="7e515-1852">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="7e515-1853">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7e515-1853">Az.Sql</span></span>

* <span data-ttu-id="7e515-1854">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="7e515-1854">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="7e515-1855">Korrigerade ett problem med Get-AzureRmSqlDatabaseVulnerabilityAssessment med DotNet-kärna</span><span class="sxs-lookup"><span data-stu-id="7e515-1855">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="7e515-1856">Ändrade dokumentationen för hjälpmeddelanden som rör SQL Auditing-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="7e515-1856">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="7e515-1857">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7e515-1857">Az.Storage</span></span>

* <span data-ttu-id="7e515-1858">Lade till -EnableHierarchicalNamespace i New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7e515-1858">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="7e515-1859">Åtgärdade problemet med att cmdleten Copy File inte kunde återanvända källkontexten på målet om inte -DestContext angetts</span><span class="sxs-lookup"><span data-stu-id="7e515-1859">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="7e515-1860">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="7e515-1860">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="7e515-1861">Stöd för statisk webbplatskonfiguration</span><span class="sxs-lookup"><span data-stu-id="7e515-1861">Support Static Website configuration</span></span>
    - <span data-ttu-id="7e515-1862">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="7e515-1862">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="7e515-1863">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="7e515-1863">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="7e515-1864">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7e515-1864">Az.Websites</span></span>

* <span data-ttu-id="7e515-1865">Set-AzureRmWebApp och Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7e515-1865">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="7e515-1866">Ny parameter (-AzureStoragePath) har lagts till för att ange att Azure Storage-sökvägar ska monteras i containerappar i Windows och Linux.</span><span class="sxs-lookup"><span data-stu-id="7e515-1866">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="7e515-1867">Använder utdata från den nya cmdleten New-AzureRmWebAppAzureStoragePath som en parameter för att ange sökvägar för Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="7e515-1867">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="7e515-1868">0.6.1 – november 2018</span><span class="sxs-lookup"><span data-stu-id="7e515-1868">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="7e515-1869">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7e515-1869">Az.ApiManagement</span></span>
* <span data-ttu-id="7e515-1870">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="7e515-1870">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="7e515-1871">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7e515-1871">Az.Automation</span></span>
* <span data-ttu-id="7e515-1872">Swagger baserade Azure Automation-cmdletar</span><span class="sxs-lookup"><span data-stu-id="7e515-1872">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="7e515-1873">Cmdletar för Uppdateringshantering har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e515-1873">Added Update Management cmdlets</span></span>
* <span data-ttu-id="7e515-1874">Cmdletar för källkontroll har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e515-1874">Added Source Control cmdlets</span></span>
* <span data-ttu-id="7e515-1875">Remove-AzureRmAutomationHybridWorkerGroup-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e515-1875">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="7e515-1876">Kommandot för DSC-registreringsnod har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="7e515-1876">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="7e515-1877">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7e515-1877">Az.Compute</span></span>
* <span data-ttu-id="7e515-1878">Problem med SystemAssigned-identitet har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="7e515-1878">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="7e515-1879">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="7e515-1879">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="7e515-1880">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="7e515-1880">Az.ContainerInstance</span></span>
* <span data-ttu-id="7e515-1881">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="7e515-1881">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="7e515-1882">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="7e515-1882">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="7e515-1883">uppdatera exempelbeskrivningen för marketplace-cmdletar</span><span class="sxs-lookup"><span data-stu-id="7e515-1883">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="7e515-1884">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7e515-1884">Az.Network</span></span>
* <span data-ttu-id="7e515-1885">Cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomErreller Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e515-1885">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="7e515-1886">ICMP tillbaka till stöd för Azure Firewall-nätverksprotokoll har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e515-1886">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="7e515-1887">Uppdatera cmdlet Test-AzureRmNetworkWatcherConnectivity, lägga till verifiering av mål-id, adress och port.</span><span class="sxs-lookup"><span data-stu-id="7e515-1887">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="7e515-1888">Åtgärda problem med minnesanvändning i VirtualNetwork-karta</span><span class="sxs-lookup"><span data-stu-id="7e515-1888">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="7e515-1889">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="7e515-1889">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="7e515-1890">Åtgärda för att ändra principen för en skyddad fildelning.</span><span class="sxs-lookup"><span data-stu-id="7e515-1890">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="7e515-1891">Tidszonsprincipen har konverterats till versaler.</span><span class="sxs-lookup"><span data-stu-id="7e515-1891">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="7e515-1892">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="7e515-1892">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="7e515-1893">Exempel i New-AzureRmRecoveryServicesAsrProtectableItem har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="7e515-1893">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="7e515-1894">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="7e515-1894">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="7e515-1895">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="7e515-1895">Az.Relay</span></span>
* <span data-ttu-id="7e515-1896">Valfri parameter -KeyValue till New-AzureRmRelayKey cmdlet har lagts till, vilket gör det möjligt för användare att tillhandahålla KeyValue.</span><span class="sxs-lookup"><span data-stu-id="7e515-1896">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="7e515-1897">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7e515-1897">Az.Resources</span></span>
* <span data-ttu-id="7e515-1898">Uppdatera hjälpdokumentation för resursidentitet kopplad till parametrar i `New-AzureRmPolicyAssignment` och `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="7e515-1898">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="7e515-1899">Lägg till ett exempel för New-AzureRmPolicyDefinition som använder -Metadata</span><span class="sxs-lookup"><span data-stu-id="7e515-1899">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="7e515-1900">Korrigera så att skiftläge behålls i taggnycklar i NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="7e515-1900">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="7e515-1901">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7e515-1901">Az.ServiceFabric</span></span>
* <span data-ttu-id="7e515-1902">Lägg till utfasningsmeddelanden för kommande icke-kompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="7e515-1902">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="7e515-1903">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7e515-1903">Az.Sql</span></span>
* <span data-ttu-id="7e515-1904">Nya cmdletar för CRUD-åtgärder på Azure Sql Database-hanterad instans och Azure Sql-hanterad databas</span><span class="sxs-lookup"><span data-stu-id="7e515-1904">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="7e515-1905">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="7e515-1905">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="7e515-1906">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="7e515-1906">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="7e515-1907">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="7e515-1907">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="7e515-1908">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="7e515-1908">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="7e515-1909">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="7e515-1909">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="7e515-1910">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="7e515-1910">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="7e515-1911">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="7e515-1911">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="7e515-1912">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="7e515-1912">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="7e515-1913">Hantering av utökad granskningsprincip på en server eller en databas har aktiverats.</span><span class="sxs-lookup"><span data-stu-id="7e515-1913">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="7e515-1914">Ny parameter (PredicateExpression) har lagts till för att aktivera filtrering av granskningsloggar.</span><span class="sxs-lookup"><span data-stu-id="7e515-1914">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="7e515-1915">Cmdletar har ändrats så att de använder SQL-klienter i stället för äldre klienter.</span><span class="sxs-lookup"><span data-stu-id="7e515-1915">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="7e515-1916">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="7e515-1916">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="7e515-1917">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="7e515-1917">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="7e515-1918">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="7e515-1918">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="7e515-1919">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="7e515-1919">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="7e515-1920">Problem med att använda Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings med lagringskontots namnparameter har korrigerats</span><span class="sxs-lookup"><span data-stu-id="7e515-1920">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="7e515-1921">0.5.0 – november 2018</span><span class="sxs-lookup"><span data-stu-id="7e515-1921">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="7e515-1922">Allmänt</span><span class="sxs-lookup"><span data-stu-id="7e515-1922">General</span></span>
* <span data-ttu-id="7e515-1923">Lade till resurskompletterare till många kärn-cmdletar – dessa gör att du kan stega genom befintliga resursnamn med TABB vid interaktiva anrop till cmdletar</span><span class="sxs-lookup"><span data-stu-id="7e515-1923">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="7e515-1924">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="7e515-1924">Az.Profile</span></span>
* <span data-ttu-id="7e515-1925">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="7e515-1925">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="7e515-1926">Bytte namn på parametern TenantId i cmdleten Connect-AzAccount till Tenant och lade till ett alias för TenantId</span><span class="sxs-lookup"><span data-stu-id="7e515-1926">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="7e515-1927">Uppdaterade TenantId-beskrivningen för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="7e515-1927">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="7e515-1928">Åtgärda felmeddelande för misslyckad inloggning när du tillhandahåller klientdomän</span><span class="sxs-lookup"><span data-stu-id="7e515-1928">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="7e515-1929">Åtgärda problem med att kontextnamn hamnar i konflikt för konton utan prenumerationer i klientorganisationen</span><span class="sxs-lookup"><span data-stu-id="7e515-1929">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="7e515-1930">Åtgärda problem med DataLake-slutpunkter vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="7e515-1930">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="7e515-1931">Åtgärdade problem med att Disconnect-AzAccount kastades om den inte anslöts</span><span class="sxs-lookup"><span data-stu-id="7e515-1931">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="7e515-1932">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7e515-1932">Az.CognitiveServices</span></span>
* <span data-ttu-id="7e515-1933">Lade till åtgärden Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="7e515-1933">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7e515-1934">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7e515-1934">Az.Compute</span></span>
* <span data-ttu-id="7e515-1935">Lade till cmdletarna Add-AzVmssVMDataDisk och Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="7e515-1935">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="7e515-1936">Get-AzVMImage visar AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="7e515-1936">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="7e515-1937">Åtgärdade att värdena för alternativen SetAzVMChefExtension -BootstrapOptions och -JsonAttribute inte angavs i json-format.</span><span class="sxs-lookup"><span data-stu-id="7e515-1937">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7e515-1938">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7e515-1938">Az.DataLakeStore</span></span>
* <span data-ttu-id="7e515-1939">Uppdatera DataLake-paketet till 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="7e515-1939">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="7e515-1940">Lägg till standardsamtidighet för flertrådade åtgärder.</span><span class="sxs-lookup"><span data-stu-id="7e515-1940">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="7e515-1941">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="7e515-1941">Az.Insights</span></span>
* <span data-ttu-id="7e515-1942">Åtgärdade problem #7267 (autoskalningsområde)</span><span class="sxs-lookup"><span data-stu-id="7e515-1942">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="7e515-1943">Problem med att uppräknade parametrar inte ställdes in ordentligt när du skapade en ny autoskalningsregel (de ställdes alltid in med standardvärdet).</span><span class="sxs-lookup"><span data-stu-id="7e515-1943">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="7e515-1944">Åtgärdade problem #7513 [Insights] Set-AzDiagnosticSetting kräver uttrycklig specifikation av kategorier när inställningar skapas</span><span class="sxs-lookup"><span data-stu-id="7e515-1944">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="7e515-1945">Nu kräver inte cmdleten uttrycklig anvisning av kategorierna för att aktiveras under skapande, d.v.s. den fungerar enligt beskrivning</span><span class="sxs-lookup"><span data-stu-id="7e515-1945">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7e515-1946">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7e515-1946">Az.Network</span></span>
* <span data-ttu-id="7e515-1947">PeeringType ändrades till en obligatorisk parameter för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="7e515-1947">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="7e515-1948">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="7e515-1948">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="7e515-1949">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="7e515-1949">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="7e515-1950">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="7e515-1950">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="7e515-1951">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="7e515-1951">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="7e515-1952">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="7e515-1952">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="7e515-1953">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="7e515-1953">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="7e515-1954">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="7e515-1954">Az.PolicyInsights</span></span>
* <span data-ttu-id="7e515-1955">Cmdletar för principreparation har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e515-1955">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="7e515-1956">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7e515-1956">Az.Resources</span></span>
* <span data-ttu-id="7e515-1957">Korrigering för https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="7e515-1957">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="7e515-1958">Tillåt att resurser listas med parametern -ResourceId för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="7e515-1958">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="7e515-1959">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="7e515-1959">Az.ServiceBus</span></span>
* <span data-ttu-id="7e515-1960">Skrivskyddad MigrationState-egenskap har lagts till i PSServiceBusMigrationConfigurationAttributes, som hjälper till att hålla koll på migreringstillståndet.</span><span class="sxs-lookup"><span data-stu-id="7e515-1960">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="7e515-1961">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7e515-1961">Az.ServiceFabric</span></span>
* <span data-ttu-id="7e515-1962">Åtgärda att lägga till certifikat till Linux-Vmss.</span><span class="sxs-lookup"><span data-stu-id="7e515-1962">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="7e515-1963">Åtgärdade Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="7e515-1963">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="7e515-1964">Använd rätt tumavtryck från nya certifikat (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="7e515-1964">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="7e515-1965">Visa undantag korrekt (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="7e515-1965">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="7e515-1966">Åtgärdade Update-AzServiceFabricDurability så att klusterkonfigurationen uppdateras innan Vmss-åtgärden CreateOrUpdate påbörjas.</span><span class="sxs-lookup"><span data-stu-id="7e515-1966">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="7e515-1967">0.4.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="7e515-1967">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="7e515-1968">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="7e515-1968">Az.Profile</span></span>
* <span data-ttu-id="7e515-1969">Åtgärdade problemet med Get-AzSubscription i CloudShell</span><span class="sxs-lookup"><span data-stu-id="7e515-1969">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="7e515-1970">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="7e515-1970">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7e515-1971">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7e515-1971">Az.Compute</span></span>
* <span data-ttu-id="7e515-1972">Nya storlekar lades till i listan över godkända VM-storlekar för vilka accelererat nätverk kommer att aktiveras vid användning av den enkla parameteruppsättningen för New-AzVm</span><span class="sxs-lookup"><span data-stu-id="7e515-1972">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="7e515-1973">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="7e515-1973">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7e515-1974">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7e515-1974">Az.DataLakeStore</span></span>
* <span data-ttu-id="7e515-1975">Lägger till stöd för regler för virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="7e515-1975">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="7e515-1976">Get-AzDataLakeStoreVirtualNetworkRule: Hämtar eller listar regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="7e515-1976">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="7e515-1977">Add-AzDataLakeStoreVirtualNetworkRule: Lägger till en regel för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="7e515-1977">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="7e515-1978">Set-AzDataLakeStoreVirtualNetworkRule: Ändrar den angivna regeln för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="7e515-1978">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="7e515-1979">Remove-AzDataLakeStoreVirtualNetworkRule: Tar bort en regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="7e515-1979">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7e515-1980">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7e515-1980">Az.Network</span></span>
* <span data-ttu-id="7e515-1981">Skicka protokollvärdet till serverdelen för att uppdatera cmdleten Test-AzNetworkWatcherConnectivity.</span><span class="sxs-lookup"><span data-stu-id="7e515-1981">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="7e515-1982">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="7e515-1982">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7e515-1983">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7e515-1983">Az.Resources</span></span>
* <span data-ttu-id="7e515-1984">Åtgärdade problem där Get-AzRoleDefinition genererar ett oläsligt undantag (när standardprofilen inte innehåller någon prenumeration och ingen omfattning har angetts) genom att lägga till ett beskrivande undantag i scenariot.</span><span class="sxs-lookup"><span data-stu-id="7e515-1984">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="7e515-1985">Ställ in ”RoleDefinitionNameParameterSet” som standardparameteruppsättning.</span><span class="sxs-lookup"><span data-stu-id="7e515-1985">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="7e515-1986">0.3.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="7e515-1986">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="7e515-1987">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="7e515-1987">Azure.Storage</span></span>
* <span data-ttu-id="7e515-1988">Åtgärda fel där Kopiera blob/fil inte kopierar metadata när målplatsen har ett problem med metadata</span><span class="sxs-lookup"><span data-stu-id="7e515-1988">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="7e515-1989">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="7e515-1989">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="7e515-1990">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="7e515-1990">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="7e515-1991">Stöd för att hämta användningsinformation om en Storage-resurs för en specifik plats och för att lägga till ett varningsmeddelande för att hämta användningsinformation om en global Storage-resurs är inaktuellt.</span><span class="sxs-lookup"><span data-stu-id="7e515-1991">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="7e515-1992">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="7e515-1992">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="7e515-1993">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7e515-1993">Az.CognitiveServices</span></span>
* <span data-ttu-id="7e515-1994">Stöd för Get-AzCognitiveServicesAccountSkus utan ett befintligt konto.</span><span class="sxs-lookup"><span data-stu-id="7e515-1994">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7e515-1995">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7e515-1995">Az.Compute</span></span>
* <span data-ttu-id="7e515-1996">Åtgärdade fel där Get-AzVM -ResourceGroupName <rg> returnerar fler än 50 resultat om det behövs</span><span class="sxs-lookup"><span data-stu-id="7e515-1996">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="7e515-1997">Lade till ett exempel för SimpleParameterSet i hjälpen för cmdleten New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="7e515-1997">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="7e515-1998">Ett stavfel i förloppsmeddelandet för Azure Disk Encryption har korrigerats</span><span class="sxs-lookup"><span data-stu-id="7e515-1998">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="7e515-1999">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="7e515-1999">Az.DataFactoryV2</span></span>
* <span data-ttu-id="7e515-2000">ADF .Net SDK-versionen har uppdaterats till 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="7e515-2000">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7e515-2001">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7e515-2001">Az.Network</span></span>
* <span data-ttu-id="7e515-2002">Funktionalitet för NetworkProfile har lagts till.</span><span class="sxs-lookup"><span data-stu-id="7e515-2002">Added NetworkProfile functionality.</span></span> <span data-ttu-id="7e515-2003">nya cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e515-2003">new cmdlets added</span></span>
    - <span data-ttu-id="7e515-2004">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7e515-2004">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="7e515-2005">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7e515-2005">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="7e515-2006">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7e515-2006">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="7e515-2007">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7e515-2007">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="7e515-2008">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="7e515-2008">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="7e515-2009">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="7e515-2009">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="7e515-2010">Länk för tjänstassociering på modell för undernät har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e515-2010">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="7e515-2011">Cmdletarna New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap och Remove-AzVirtualNetworkTap har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e515-2011">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="7e515-2012">Cmdletarna Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig och Remove-AzNEtworkInterfaceTapConfig har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e515-2012">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="7e515-2013">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="7e515-2013">Az.RedisCache</span></span>
* <span data-ttu-id="7e515-2014">Tillåt att alla strängar används som storleksparametrar framöver.</span><span class="sxs-lookup"><span data-stu-id="7e515-2014">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="7e515-2015">Lägg till P5 i popup-fönstret PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="7e515-2015">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="7e515-2016">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7e515-2016">Az.Resources</span></span>
* <span data-ttu-id="7e515-2017">Parametern -Mode som saknades i Set-AzPolicyDefinition har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e515-2017">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="7e515-2018">Åtgärdade buggen för cmdleten Get-AzProviderOperation för åtgärder med ursprung som innehåller användare</span><span class="sxs-lookup"><span data-stu-id="7e515-2018">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="7e515-2019">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7e515-2019">Az.Sql</span></span>
* <span data-ttu-id="7e515-2020">Ett problem där vissa cmdletar för säkerhetskopiering inte kunde identifiera den aktuella azure-prenumerationen har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="7e515-2020">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7e515-2021">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7e515-2021">Az.Websites</span></span>
* <span data-ttu-id="7e515-2022">Ny cmdlet: Get-AzWebAppContainerContinuousDeploymentUrl – Hämtar webhook-URL:en för kontinuerlig distribution av container</span><span class="sxs-lookup"><span data-stu-id="7e515-2022">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="7e515-2023">Nya cmdletar: New-AzWebAppContainerPSSession och Enter-WebAppContainerPSSession – Startar en PowerShell-fjärrsession i en containerapp för windows</span><span class="sxs-lookup"><span data-stu-id="7e515-2023">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="7e515-2024">0.2.0 – september 2018</span><span class="sxs-lookup"><span data-stu-id="7e515-2024">0.2.0 - September 2018</span></span>
 <span data-ttu-id="7e515-2025">Första versionen</span><span class="sxs-lookup"><span data-stu-id="7e515-2025">Initial Release</span></span>
