---
ms.openlocfilehash: f357a17f698d68c1a29dcb78f83671973fd6ecad
ms.sourcegitcommit: 0b644bfecf4224b2ea83520d1a6a956734d9fba4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/12/2019
ms.locfileid: "67863727"
---
## <a name="240---july-2019"></a><span data-ttu-id="8d5bd-101">2.4.0 – juli 2019</span><span class="sxs-lookup"><span data-stu-id="8d5bd-101">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8d5bd-102">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8d5bd-102">Az.Accounts</span></span>
* <span data-ttu-id="8d5bd-103">Lägg till stöd för profil-cmdletar</span><span class="sxs-lookup"><span data-stu-id="8d5bd-103">Add support for profile cmdlets</span></span>
* <span data-ttu-id="8d5bd-104">Lägg till stöd för miljöer och dataplaner i genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="8d5bd-104">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="8d5bd-105">Åtgärda bugg där fel slutpunkt i vissa fall användes för cmdletar för dataplaner i Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="8d5bd-105">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="8d5bd-106">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="8d5bd-106">Az.Advisor</span></span>
* <span data-ttu-id="8d5bd-107">GA-version av Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="8d5bd-107">GA release of Az.Advisor</span></span>
* <span data-ttu-id="8d5bd-108">Den här modulen ingår nu som en del av `Az`-sammanslagningsmodulen</span><span class="sxs-lookup"><span data-stu-id="8d5bd-108">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="8d5bd-109">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8d5bd-109">Az.ApiManagement</span></span>
* <span data-ttu-id="8d5bd-110">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="8d5bd-110">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="8d5bd-111">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="8d5bd-111">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="8d5bd-112">Stöd för att fråga prenumerationer efter användare och produkt har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d5bd-112">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="8d5bd-113">Stöd för att fråga med hjälp av omfång ”/”, ”/apis”, ”/apis/echo-api” har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d5bd-113">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="8d5bd-114">Korrigering av problem https://github.com/Azure/azure-powershell/issues/9307 och https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="8d5bd-114">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="8d5bd-115">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="8d5bd-115">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="8d5bd-116">Stöd för att ange ”ApiVersion” och ”ApiVersionSetId” när API:er importeras har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d5bd-116">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8d5bd-117">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8d5bd-117">Az.Automation</span></span>
* <span data-ttu-id="8d5bd-118">Bugg med cmdleten Set-AzAutomationConnectionFieldValue för att hantera strängvärde har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-118">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d5bd-119">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d5bd-119">Az.Compute</span></span>
* <span data-ttu-id="8d5bd-120">Lägg till parametern HyperVGeneration i New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="8d5bd-120">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8d5bd-121">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8d5bd-121">Az.DataFactory</span></span>
* <span data-ttu-id="8d5bd-122">Uppdaterar utdata från ADF-cmdletar som hämtar aktivitetskörningar, hämtar pipelinekörningar och hämtar utlösarkörningar för stöd för Select-Object-pipe.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-122">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="8d5bd-123">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="8d5bd-123">Az.EventGrid</span></span>
* <span data-ttu-id="8d5bd-124">Korrigera stavfel i dokumentation om ”New-AzEventGridSubscription”</span><span class="sxs-lookup"><span data-stu-id="8d5bd-124">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8d5bd-125">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8d5bd-125">Az.IotHub</span></span>
* <span data-ttu-id="8d5bd-126">Lägg till stöd för att återskapa principnycklar för auktorisering.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-126">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8d5bd-127">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d5bd-127">Az.Network</span></span>
* <span data-ttu-id="8d5bd-128">”RoutingPreference” har lagts till i offentliga IP-taggar</span><span class="sxs-lookup"><span data-stu-id="8d5bd-128">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="8d5bd-129">Förbättra exempel för referensdokumentation om ”Get-AzNetworkServiceTag”</span><span class="sxs-lookup"><span data-stu-id="8d5bd-129">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="8d5bd-130">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="8d5bd-130">Az.PolicyInsights</span></span>
* <span data-ttu-id="8d5bd-131">Åtgärda problem med null-referens i Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="8d5bd-131">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="8d5bd-132">Mer information här: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="8d5bd-132">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8d5bd-133">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8d5bd-133">Az.OperationalInsights</span></span>
* <span data-ttu-id="8d5bd-134">Modellen för CustomLog-datakälla som returneras i Get-AzOperationalInsightsDataSource har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8d5bd-134">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8d5bd-135">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8d5bd-135">Az.RecoveryServices</span></span>
* <span data-ttu-id="8d5bd-136">Kommandot get-policy för IaaSVM:er har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8d5bd-136">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="8d5bd-137">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d5bd-137">Az.Resources</span></span>
    - <span data-ttu-id="8d5bd-138">Korrigera hjälptext för den översta parametern i Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="8d5bd-138">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="8d5bd-139">Lägg till växlingsstöd på klientsidan för Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="8d5bd-139">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="8d5bd-140">Lägg till nya parametrar för Set-AzPolicyAssignment, -PolicyParameters och -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="8d5bd-140">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="8d5bd-141">En mängd dokument- och exempeluppdateringar för Policy-cmdletar</span><span class="sxs-lookup"><span data-stu-id="8d5bd-141">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="8d5bd-142">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8d5bd-142">Az.ServiceBus</span></span>
* <span data-ttu-id="8d5bd-143">Korrigering av problem #4938 – New-AzureRmServiceBusQueue returnerar BadRequest vid konfiguration av MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="8d5bd-143">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="8d5bd-144">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d5bd-144">Az.Sql</span></span>
* <span data-ttu-id="8d5bd-145">Lägg till cmdletar för instansredundansgrupper från förhandsversion till offentlig version</span><span class="sxs-lookup"><span data-stu-id="8d5bd-145">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="8d5bd-146">Stöd för granskning för Azure SQL Server\Database med nya cmdletar.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-146">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="8d5bd-147">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="8d5bd-147">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="8d5bd-148">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="8d5bd-148">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="8d5bd-149">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="8d5bd-149">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="8d5bd-150">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="8d5bd-150">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="8d5bd-151">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="8d5bd-151">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="8d5bd-152">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="8d5bd-152">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="8d5bd-153">Ta bort begränsningar för e-post från inställningarna för sårbarhetsbedömning</span><span class="sxs-lookup"><span data-stu-id="8d5bd-153">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8d5bd-154">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8d5bd-154">Az.Storage</span></span>
* <span data-ttu-id="8d5bd-155">Ändra två parametrar ”-IndexDocument” och ”-ErrorDocument404Path” från ”krävs” till ”valfri” i cmdlet:</span><span class="sxs-lookup"><span data-stu-id="8d5bd-155">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="8d5bd-156">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="8d5bd-156">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="8d5bd-157">Uppdatera hjälpen för Get-AzStorageBlobContent genom att lägga till ett exempel</span><span class="sxs-lookup"><span data-stu-id="8d5bd-157">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="8d5bd-158">Visa mer felinformation när cmdleten misslyckas med StorageException</span><span class="sxs-lookup"><span data-stu-id="8d5bd-158">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="8d5bd-159">Stöd för att skapa eller uppdatera lagringskonto med Azure Files AAD DS-autentisering</span><span class="sxs-lookup"><span data-stu-id="8d5bd-159">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="8d5bd-160">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8d5bd-160">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="8d5bd-161">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8d5bd-161">Set-AzStorageAccount</span></span>
* <span data-ttu-id="8d5bd-162">Stöd för att lista eller stänga filreferenser för en filresurs, filkatalog eller en fil</span><span class="sxs-lookup"><span data-stu-id="8d5bd-162">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="8d5bd-163">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="8d5bd-163">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="8d5bd-164">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="8d5bd-164">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="8d5bd-165">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="8d5bd-165">Az.StorageSync</span></span>
* <span data-ttu-id="8d5bd-166">Den här modulen ingår nu som en del av `Az`-sammanslagningsmodulen</span><span class="sxs-lookup"><span data-stu-id="8d5bd-166">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="8d5bd-167">2.3.2 – juni 2019</span><span class="sxs-lookup"><span data-stu-id="8d5bd-167">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8d5bd-168">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8d5bd-168">Az.Accounts</span></span>
* <span data-ttu-id="8d5bd-169">Åtgärda bugg med felaktiga webbadresser som i vissa fall användes för Functions-anrop</span><span class="sxs-lookup"><span data-stu-id="8d5bd-169">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="8d5bd-170">Mer information här: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="8d5bd-170">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="8d5bd-171">Åtgärda problem med alias från AzureRM i Az-cmdletar</span><span class="sxs-lookup"><span data-stu-id="8d5bd-171">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="8d5bd-172">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="8d5bd-172">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="8d5bd-173">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="8d5bd-173">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d5bd-174">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d5bd-174">Az.Compute</span></span>
* <span data-ttu-id="8d5bd-175">Parameteruppsättningarna New-AzVm och New-AzVmss accepterar nu parametern ”ProximityPlacementGroup”.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-175">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="8d5bd-176">Stavfel i referensdokumentationen för ”New-AzVM” har korrigerats</span><span class="sxs-lookup"><span data-stu-id="8d5bd-176">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="8d5bd-177">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="8d5bd-177">Az.Dns</span></span>
* <span data-ttu-id="8d5bd-178">Stavfel i hjälpexempel för ”Set-AzDnsZone” har korrigerats.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-178">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="8d5bd-179">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="8d5bd-179">Az.EventGrid</span></span>
* <span data-ttu-id="8d5bd-180">Har uppdaterats för att använda API-versionen 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-180">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="8d5bd-181">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="8d5bd-181">New cmdlets:</span></span>
    - <span data-ttu-id="8d5bd-182">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="8d5bd-182">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="8d5bd-183">Skapar en ny Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-183">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="8d5bd-184">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="8d5bd-184">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="8d5bd-185">Hämtar information om en Event Grid-domän eller hämtar en lista med alla Event Grid-domäner i den aktuella Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-185">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="8d5bd-186">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="8d5bd-186">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="8d5bd-187">Tar bort en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-187">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="8d5bd-188">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="8d5bd-188">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="8d5bd-189">Återskapar nyckeln för delad åtkomst för en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-189">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="8d5bd-190">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="8d5bd-190">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="8d5bd-191">Hämtar de nycklar för delad åtkomst som används för att publicera händelser till en Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-191">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="8d5bd-192">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="8d5bd-192">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="8d5bd-193">Skapar ett nytt Azure Event Grid-domänämne.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-193">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="8d5bd-194">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="8d5bd-194">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="8d5bd-195">Hämtar information om ett Event Grid-domänämne eller hämtar en lista med alla Event Grid-domänämnen under en specifik Event Grid-domän i nuvarande Azure</span><span class="sxs-lookup"><span data-stu-id="8d5bd-195">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="8d5bd-196">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="8d5bd-196">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="8d5bd-197">Tar bort ett befintligt Azure Event Grid-domänämne.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-197">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="8d5bd-198">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="8d5bd-198">Updated cmdlets:</span></span>
    - <span data-ttu-id="8d5bd-199">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="8d5bd-199">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="8d5bd-200">Lägg till nya obligatoriska parametrar för att stödja piping för den nya Event Grid-domänen och Event Grid-domänämnet för att göra det möjligt att skapa nya händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-200">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="8d5bd-201">Lägg till nya obligatoriska parametrar för att ange det nya Event Grid-domännamnet och/eller namnet på Event Grid-domänämnet för att göra det möjligt att skapa nya händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-201">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="8d5bd-202">Lägg till ny parameteruppsättningar för domäner och domänämnen för att göra det möjligt att återanvända befintliga parametrar (t.ex. EndPointType, SubjectBeginsWith osv).</span><span class="sxs-lookup"><span data-stu-id="8d5bd-202">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="8d5bd-203">Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="8d5bd-203">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="8d5bd-204">Förfallodatum för händelseprenumeration</span><span class="sxs-lookup"><span data-stu-id="8d5bd-204">Event subscription expiration date,</span></span>
            - <span data-ttu-id="8d5bd-205">Avancerade filterparametrar.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-205">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="8d5bd-206">Lägg till ny uppräkning för servicebusqueue som mål.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-206">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="8d5bd-207">Tillåt inte användning av ”Alla” i alternativet -IncludedEventType och ersätt det med</span><span class="sxs-lookup"><span data-stu-id="8d5bd-207">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="8d5bd-208">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="8d5bd-208">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="8d5bd-209">Lägg till ny valfria parametrar (Top, ODataQuery och NextLink) för att stödja sidnumrering och filtrering av resultat.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-209">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="8d5bd-210">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="8d5bd-210">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="8d5bd-211">Lägg till nya obligatoriska parametrar för att stödja piping för en Event Grid-domän och Event Grid-domänämnen för att göra det möjligt att ta bort befintliga händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-211">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="8d5bd-212">Lägg till nya obligatoriska parametrar för att ange Event Grid-domännamnet och/eller namnet på Event Grid-domänämnet för att göra det möjligt att ta bort befintliga händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-212">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="8d5bd-213">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="8d5bd-213">Az.FrontDoor</span></span>
* <span data-ttu-id="8d5bd-214">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="8d5bd-214">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="8d5bd-215">Lägg till stöd för transformeringar och nytt värde för automatisk komplettering för operatorer (RegEx)</span><span class="sxs-lookup"><span data-stu-id="8d5bd-215">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="8d5bd-216">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="8d5bd-216">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="8d5bd-217">Lägg till nya värden för automatisk komplettering</span><span class="sxs-lookup"><span data-stu-id="8d5bd-217">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8d5bd-218">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d5bd-218">Az.Network</span></span>
* <span data-ttu-id="8d5bd-219">Lägg till stöd för resurs för virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="8d5bd-219">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="8d5bd-220">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="8d5bd-220">New cmdlets</span></span>
        - <span data-ttu-id="8d5bd-221">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="8d5bd-221">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="8d5bd-222">Lägg till AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="8d5bd-222">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="8d5bd-223">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="8d5bd-223">New cmdlets</span></span> 
        - <span data-ttu-id="8d5bd-224">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="8d5bd-224">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="8d5bd-225">Lägg till PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="8d5bd-225">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="8d5bd-226">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="8d5bd-226">New cmdlets</span></span> 
        - <span data-ttu-id="8d5bd-227">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="8d5bd-227">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="8d5bd-228">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="8d5bd-228">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="8d5bd-229">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="8d5bd-229">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="8d5bd-230">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="8d5bd-230">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="8d5bd-231">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8d5bd-231">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="8d5bd-232">Lägg till PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="8d5bd-232">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="8d5bd-233">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="8d5bd-233">New cmdlets</span></span>
        - <span data-ttu-id="8d5bd-234">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="8d5bd-234">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="8d5bd-235">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="8d5bd-235">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="8d5bd-236">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="8d5bd-236">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="8d5bd-237">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="8d5bd-237">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="8d5bd-238">Nedanstående kommandon för funktionen har uppdaterats: Flaggan UseLocalAzureIpAddress på VpnConnection</span><span class="sxs-lookup"><span data-stu-id="8d5bd-238">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="8d5bd-239">New-AzVpnConnection har uppdaterats: Den valfria parametern -UseLocalAzureIpAddress har lagts till för att visa att en lokal IP-adress i Azure ska användas som källadress när anslutningen initieras.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-239">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="8d5bd-240">Set-AzVpnConnection har uppdaterats: Den valfria parametern -UseLocalAzureIpAddress har lagts till för att visa att en lokal IP-adress i Azure ska användas som källadress när anslutningen initieras.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-240">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="8d5bd-241">Det skrivskyddade fältet PeeredConnections har lagts till i ExpressRoute-peering.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-241">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="8d5bd-242">Det skrivskyddade fältet GlobalReachEnabled har lagts till i ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-242">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="8d5bd-243">Ett attribut för icke-bakåtkompatibla ändringar har lagts till för att lyfta fram utfasning av fältet AllowGlobalReach i modellen ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8d5bd-243">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="8d5bd-244">Problem 8756 har åtgärdats: Fel vid användning av TargetListenerID med AzApplicationGatewayRedirectConfiguration-cmdletar</span><span class="sxs-lookup"><span data-stu-id="8d5bd-244">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="8d5bd-245">En bugg i New-AzApplicationGatewayPathRuleConfig som gjorde att regeluppsättningen för att återskapa inte kunde anges har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-245">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="8d5bd-246">Visningen av VirtualNetworkTaps i NetworkInterfaceIpConfiguration har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8d5bd-246">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="8d5bd-247">Cortex Get-cmdletar för att visa en lista med alla delar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8d5bd-247">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="8d5bd-248">Funktionen för att skapa VirtualHub-referenser för ExpressRouteGateways och VpnGateway har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8d5bd-248">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="8d5bd-249">Stöd för tillgänglighetszoner i AzureFirewall och NatGateway har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d5bd-249">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="8d5bd-250">Cmdleten Get-AzNetworkServiceTag har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d5bd-250">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="8d5bd-251">Lägg till stöd för flera offentliga IP-adresser för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="8d5bd-251">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="8d5bd-252">Cmdleten New-AzFirewall har uppdaterats:</span><span class="sxs-lookup"><span data-stu-id="8d5bd-252">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="8d5bd-253">Parametern -PublicIpAddress som accepterar ett eller flera offentliga IP-adressobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d5bd-253">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="8d5bd-254">Parametern -VirtualNetwork som accepterar ett virtuellt nätverksobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d5bd-254">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="8d5bd-255">Metoderna AddPublicIpAddress och RemovePublicIpAddress har lagts till på brandväggsobjekt – dessa accepterar ett offentligt IP-adressobjekt som indata</span><span class="sxs-lookup"><span data-stu-id="8d5bd-255">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="8d5bd-256">Inaktuella parametrar -PublicIpName och -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="8d5bd-256">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="8d5bd-257">Nedanstående kommandon för funktionen har uppdaterats: Ange autentiseringsalternativ för VpnClient AAD till resurser för virtuella nätverksgatewayer.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-257">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="8d5bd-258">New-AzVirtualNetworkGateway har uppdaterats: De valfria parametrarna AadTenantUri, AadAudienceId och AadIssuerUri för att ange VpnClient AAD-autentiseringsalternativ på en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-258">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="8d5bd-259">Set-AzVirtualNetworkGateway har uppdaterats: De valfria parametrarna AadTenantUri, AadAudienceId och AadIssuerUri för att ange VpnClient AAD-autentiseringsalternativ på en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-259">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="8d5bd-260">Set-AzVirtualNetworkGateway har uppdaterats: Den valfria växelparametern RemoveAadAuthentication som tar bort VpnClient AAD-autentiseringsalternativ från en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-260">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8d5bd-261">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8d5bd-261">Az.OperationalInsights</span></span>
* <span data-ttu-id="8d5bd-262">Aktivera prisnivån **pergb2018** i kommandot ”New-AzureRmOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="8d5bd-262">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="8d5bd-263">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d5bd-263">Az.Resources</span></span>
* <span data-ttu-id="8d5bd-264">Stöd för ytterligare alternativ för att exportera en mall</span><span class="sxs-lookup"><span data-stu-id="8d5bd-264">Support for additional Template Export options</span></span>
    - <span data-ttu-id="8d5bd-265">Lägg till parametern ”-SkipResourceNameParameterization” till Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8d5bd-265">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="8d5bd-266">Lägg till parametern ”-SkipAllParameterization” till Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8d5bd-266">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="8d5bd-267">Lägg till parametern ”-Resource” till Export-AzResourceGroup för exporterad resursfiltrering</span><span class="sxs-lookup"><span data-stu-id="8d5bd-267">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8d5bd-268">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8d5bd-268">Az.ServiceFabric</span></span>
* <span data-ttu-id="8d5bd-269">Åtgärda att fel tumavtryck används vid tilläggning av certifikat i ByExistingKeyVault i vissa fall</span><span class="sxs-lookup"><span data-stu-id="8d5bd-269">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="8d5bd-270">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d5bd-270">Az.Sql</span></span>
* <span data-ttu-id="8d5bd-271">Åtgärda suffix för lagringsslutpunkt i Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="8d5bd-271">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="8d5bd-272">Åtgärda att aktivering av Advanced Data Security åsidosätter Advanced Threat Protection-princip</span><span class="sxs-lookup"><span data-stu-id="8d5bd-272">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="8d5bd-273">Nya cmdletar för Management.Sql som gör att kunderna kan lägga till nycklar för transparent datakryptering (TDE) och ange TDE-skydd för hanterade instanser</span><span class="sxs-lookup"><span data-stu-id="8d5bd-273">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="8d5bd-274">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8d5bd-274">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="8d5bd-275">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8d5bd-275">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="8d5bd-276">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8d5bd-276">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="8d5bd-277">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="8d5bd-277">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="8d5bd-278">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="8d5bd-278">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8d5bd-279">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8d5bd-279">Az.Storage</span></span>
* <span data-ttu-id="8d5bd-280">Stöd för typerna FileStorage och SkuName Premium_ZRS när lagringskonton skapas</span><span class="sxs-lookup"><span data-stu-id="8d5bd-280">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="8d5bd-281">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8d5bd-281">New-AzStorageAccount</span></span>
* <span data-ttu-id="8d5bd-282">Beskrivningen av cmdleten för bloboföränderlighet har förtydligats</span><span class="sxs-lookup"><span data-stu-id="8d5bd-282">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="8d5bd-283">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="8d5bd-283">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8d5bd-284">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8d5bd-284">Az.Websites</span></span>
* <span data-ttu-id="8d5bd-285">Optimerar Get-AzWebAppCertificate för att filtrera efter resursgrupp på servern i stället för klienten</span><span class="sxs-lookup"><span data-stu-id="8d5bd-285">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="8d5bd-286">Lägger till växlingsparametern -UseDisasterRecovery till Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="8d5bd-286">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="8d5bd-287">2.2.0 – juni 2019</span><span class="sxs-lookup"><span data-stu-id="8d5bd-287">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="8d5bd-288">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="8d5bd-288">Az.Cdn</span></span>
* <span data-ttu-id="8d5bd-289">Uppdaterade cmdletar för att ge stöd för rulesEngine-funktion baserat på API-version 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-289">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d5bd-290">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d5bd-290">Az.Compute</span></span>
* <span data-ttu-id="8d5bd-291">Lade till parameter `NoWait` som startar åtgärden och returnerar omedelbart, innan åtgärden har slutförts.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-291">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="8d5bd-292">Uppdaterade cmdletar:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="8d5bd-292">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="8d5bd-293">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8d5bd-293">Az.EventHub</span></span>
* <span data-ttu-id="8d5bd-294">Korrigering för #9231 – Get-AzEventHubNamespace returnerar inga taggar</span><span class="sxs-lookup"><span data-stu-id="8d5bd-294">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="8d5bd-295">Korrigering för #9230 – Get-AzEventHubNamespace returnerar ResourceGroup istället för ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d5bd-295">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8d5bd-296">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d5bd-296">Az.Network</span></span>
* <span data-ttu-id="8d5bd-297">Uppdatera ResourceId och InputObject för NAT-gateway</span><span class="sxs-lookup"><span data-stu-id="8d5bd-297">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="8d5bd-298">Lägg till alias för ResourceId och InputObject</span><span class="sxs-lookup"><span data-stu-id="8d5bd-298">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="8d5bd-299">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="8d5bd-299">Az.PolicyInsights</span></span>
* <span data-ttu-id="8d5bd-300">Åtgärda Null-referensproblem i Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="8d5bd-300">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8d5bd-301">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8d5bd-301">Az.RecoveryServices</span></span>
* <span data-ttu-id="8d5bd-302">Minsta kvarhållning för IaaSVM-policy i dagar ändrat till 7 från 1</span><span class="sxs-lookup"><span data-stu-id="8d5bd-302">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="8d5bd-303">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8d5bd-303">Az.ServiceBus</span></span>
* <span data-ttu-id="8d5bd-304">Korrigering för ärende #9182 – Get-AzServiceBusNamespace returnerar ResourceGroup istället för ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d5bd-304">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8d5bd-305">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8d5bd-305">Az.ServiceFabric</span></span>
* <span data-ttu-id="8d5bd-306">Åtgärda stavfel i felmeddelandet för Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="8d5bd-306">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="8d5bd-307">Åtgärda saknat tecken i Service Fabric-kommandorader</span><span class="sxs-lookup"><span data-stu-id="8d5bd-307">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="8d5bd-308">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d5bd-308">Az.Sql</span></span>
* <span data-ttu-id="8d5bd-309">Lägg till parametern DnsZonePartner för New-AzureSqlInstance-cmdlet för att ge stöd för AutoDr för hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-309">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="8d5bd-310">Avvecklar cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="8d5bd-310">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="8d5bd-311">Döp om cmdletar för hotidentifiering till Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="8d5bd-311">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="8d5bd-312">Parametrarna New-AzSqlInstance -StorageSizeInGB och -LicenseType är nu valfria.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-312">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8d5bd-313">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8d5bd-313">Az.Websites</span></span>
* <span data-ttu-id="8d5bd-314">åtgärdar problemet där användningen av Set-AzWebApp och Set-AzWebAppSlot med -WebApp-egenskap tog bort taggarna</span><span class="sxs-lookup"><span data-stu-id="8d5bd-314">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="8d5bd-315">2.1.0 – maj 2019</span><span class="sxs-lookup"><span data-stu-id="8d5bd-315">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="8d5bd-316">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8d5bd-316">Az.ApiManagement</span></span>
* <span data-ttu-id="8d5bd-317">Skapade nya cmdletar för att hantera diagnostik för global- och API-omfång</span><span class="sxs-lookup"><span data-stu-id="8d5bd-317">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="8d5bd-318">**Get-AzApiManagementDiagnostic** – Skaffa diagnostik konfigurerad för global- eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="8d5bd-318">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="8d5bd-319">**New-AzApiManagementDiagnostic** – Skapa ny diagnostik för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="8d5bd-319">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="8d5bd-320">**New-AzApiManagementHttpMessageDiagnostic** – Skapa diagnostikinställning om vilka rubriker som ska loggas och storleken på brödtextbyte</span><span class="sxs-lookup"><span data-stu-id="8d5bd-320">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="8d5bd-321">**New-AzApiManagementPipelineDiagnosticSetting** – Skapa diagnostikinställningar för inkommande/utgående HTTP-meddelanden till gatewayen.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-321">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="8d5bd-322">**New-AzApiManagementSamplingSetting** – Skapa samplinginställningar för begäranden/svar för en diagnostik</span><span class="sxs-lookup"><span data-stu-id="8d5bd-322">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="8d5bd-323">**Remove-AzApiManagementDiagnostic** – Ta bort en diagnostikenhet för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="8d5bd-323">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="8d5bd-324">**Set-AzApiManagementDiagnostic** – Uppdatera en diagnostikenhet för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="8d5bd-324">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="8d5bd-325">Skapade nya cmdletar för hantering av cacheminne i ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="8d5bd-325">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="8d5bd-326">**Get-AzApiManagementCache** – Hämta information om cacheminnet som anges av identifierare eller alla cacheminnen</span><span class="sxs-lookup"><span data-stu-id="8d5bd-326">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="8d5bd-327">**New-AzApiManagementCache** – Skapa ett nytt default-cacheminne eller cacheminne i en viss Azure-region</span><span class="sxs-lookup"><span data-stu-id="8d5bd-327">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="8d5bd-328">**Remove-AzApiManagementCache** – Ta bort ett cacheminne</span><span class="sxs-lookup"><span data-stu-id="8d5bd-328">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="8d5bd-329">**Remove-AzApiManagementCache** – Ta bort ett cacheminne</span><span class="sxs-lookup"><span data-stu-id="8d5bd-329">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="8d5bd-330">Skapade nya cmdletar för hantering av API-schema</span><span class="sxs-lookup"><span data-stu-id="8d5bd-330">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="8d5bd-331">**New-AzApiManagementSchema** – Skapa ett nytt schema för ett API</span><span class="sxs-lookup"><span data-stu-id="8d5bd-331">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="8d5bd-332">**Get-AzApiManagementSchema** – Hämta de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="8d5bd-332">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="8d5bd-333">**Remove-AzApiManagementSchema** – Ta bort de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="8d5bd-333">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="8d5bd-334">**Set-AzApiManagementSchema** – Uppdatera de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="8d5bd-334">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="8d5bd-335">Skapa ny cmdlet för att generera en användartoken.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-335">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="8d5bd-336">**New-AzApiManagementUserToken** – Skapa en ny användartoken som enligt standardinställning är giltig i 8 timmar. Token för GIT-användaren kan skapas med den här cmdleten./</span><span class="sxs-lookup"><span data-stu-id="8d5bd-336">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="8d5bd-337">Skapade en ny cmdlet för att hämta nätverksstatus</span><span class="sxs-lookup"><span data-stu-id="8d5bd-337">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="8d5bd-338">**Get-AzApiManagementNetworkStatus** – Hämta nätverksstatusanslutningen för resurserna som API Management-tjänsten är beroende av.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-338">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="8d5bd-339">Det här är användbart när du distribuerar ApiManagement-tjänsten i ett virtuellt nätverk och validerar om något beroende är brutet.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-339">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="8d5bd-340">Uppdaterade cmdlet **New-AzApiManagement** för att hantera ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="8d5bd-340">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="8d5bd-341">Lade till stöd för den nya SKU:n Consumption</span><span class="sxs-lookup"><span data-stu-id="8d5bd-341">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="8d5bd-342">Aktiverade stöd för att slå på flaggan EnableClientCertificate för SKU:n Consumption</span><span class="sxs-lookup"><span data-stu-id="8d5bd-342">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="8d5bd-343">Den nya cmdleten **New-AzApiManagementSslSetting** gör det möjligt att ställa in TLS/SSL-inställningen på ”Backend” och ”Frontend” (serverdel och klientdel).</span><span class="sxs-lookup"><span data-stu-id="8d5bd-343">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="8d5bd-344">Det här kan också användas till att konfigurera chiffer som 3DES och ServerProtocols som Http2 för Frontend för en ApiManagement-tjänst.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-344">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="8d5bd-345">Stöd har lagts till för att konfigurera värdnamnet DeveloperPortal på ApiManagement-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-345">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="8d5bd-346">Uppdaterade cmdletar **Get-AzApiManagementSsoToken** för att ta PsApiManagement-objekt som indata</span><span class="sxs-lookup"><span data-stu-id="8d5bd-346">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="8d5bd-347">Uppdaterad cmdleten för att visa infogade felmeddelanden</span><span class="sxs-lookup"><span data-stu-id="8d5bd-347">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="8d5bd-348">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Felkod: Felmeddelande av typen ValidationError: Ett eller flera fält innehåller felaktiga värden: Felinformation:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="8d5bd-348">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="8d5bd-349">Uppdaterade cmdlet **Export-AzApiManagementApi** för att exportera API:er i OpenApi 3.0-format</span><span class="sxs-lookup"><span data-stu-id="8d5bd-349">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="8d5bd-350">Uppdaterade cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="8d5bd-350">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="8d5bd-351">Importera API från dokumentspecifikationen OpenApi 3.0</span><span class="sxs-lookup"><span data-stu-id="8d5bd-351">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="8d5bd-352">Om du vill åsidosätta egenskapen PsApiManagementSchema specificerad i ett dokument (Swagger, Wadl, Wsdl, OpenApi).</span><span class="sxs-lookup"><span data-stu-id="8d5bd-352">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="8d5bd-353">Åsidosätta egenskapen ServiceUrl som specificeras i ett dokument.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-353">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="8d5bd-354">Uppdaterade cmdlet **Get-AzApiManagementPolicy** för att returnera policy i undantaget format av typen icke-XML med rawxml</span><span class="sxs-lookup"><span data-stu-id="8d5bd-354">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="8d5bd-355">Uppdaterade cmdlet **Set-AzApiManagementPolicy** för att godkänna policy i undantaget format av typen icke-XML med rawxml och XML undantaget med xml</span><span class="sxs-lookup"><span data-stu-id="8d5bd-355">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="8d5bd-356">Uppdaterad cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="8d5bd-356">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="8d5bd-357">Konfigurera API med OpenId auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-357">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="8d5bd-358">Skapa ett API i ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="8d5bd-358">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="8d5bd-359">Klona ett API med SourceApiId och SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-359">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="8d5bd-360">Möjlighet att konfigurera SubscriptionRequired i API-omfattningen.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-360">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="8d5bd-361">Uppdaterad cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="8d5bd-361">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="8d5bd-362">Konfigurera API med OpenId auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-362">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="8d5bd-363">Uppdatera ett API till ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="8d5bd-363">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="8d5bd-364">Möjlighet att konfigurera SubscriptionRequired i API-omfattningen.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-364">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="8d5bd-365">Uppdaterad cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="8d5bd-365">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="8d5bd-366">Klona en befintlig version med hjälp av SourceApiRevision (kopiera taggar, produkter, åtgärder och principer).</span><span class="sxs-lookup"><span data-stu-id="8d5bd-366">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="8d5bd-367">Den nya revisionen antar ApiId från den överordnade instansen.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-367">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="8d5bd-368">Tillhandahålla ApiRevisionDescription</span><span class="sxs-lookup"><span data-stu-id="8d5bd-368">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="8d5bd-369">Åsidosätta ServiceUrl vid kloning av ett API.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-369">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="8d5bd-370">Uppdaterad cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="8d5bd-370">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="8d5bd-371">Konfigurera AAD eller AADB2C med en Authority</span><span class="sxs-lookup"><span data-stu-id="8d5bd-371">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="8d5bd-372">Konfigurera SignupPolicy, SigninPolicy, ProfileEditingPolicy och PasswordResetPolicy</span><span class="sxs-lookup"><span data-stu-id="8d5bd-372">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="8d5bd-373">Uppdaterad cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="8d5bd-373">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="8d5bd-374">Kompensera för ny SubscriptonModel med Scope och UserId</span><span class="sxs-lookup"><span data-stu-id="8d5bd-374">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="8d5bd-375">Kompensera för gammal prenumerationsmodell med ProductId och UserId</span><span class="sxs-lookup"><span data-stu-id="8d5bd-375">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="8d5bd-376">Lägg till funktion för att aktivera AllowTracing på prenumerationsnivå.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-376">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="8d5bd-377">Uppdaterad cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="8d5bd-377">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="8d5bd-378">Kompensera för ny SubscriptonModel med Scope och UserId</span><span class="sxs-lookup"><span data-stu-id="8d5bd-378">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="8d5bd-379">Kompensera för gammal prenumerationsmodell med ProductId och UserId</span><span class="sxs-lookup"><span data-stu-id="8d5bd-379">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="8d5bd-380">Lägg till funktion för att aktivera AllowTracing på prenumerationsnivå.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-380">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="8d5bd-381">Uppdaterade följande cmdletar för att acceptera ResourceId som indata</span><span class="sxs-lookup"><span data-stu-id="8d5bd-381">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="8d5bd-382">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="8d5bd-382">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="8d5bd-383">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="8d5bd-383">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="8d5bd-384">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="8d5bd-384">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="8d5bd-385">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="8d5bd-385">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="8d5bd-386">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="8d5bd-386">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="8d5bd-387">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="8d5bd-387">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="8d5bd-388">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="8d5bd-388">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="8d5bd-389">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="8d5bd-389">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="8d5bd-390">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="8d5bd-390">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="8d5bd-391">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="8d5bd-391">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="8d5bd-392">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="8d5bd-392">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="8d5bd-393">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="8d5bd-393">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8d5bd-394">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8d5bd-394">Az.Automation</span></span>
* <span data-ttu-id="8d5bd-395">Uppdaterade Get-AzAutomationJobOutputRecord för att hantera postvärden av typen JSON och Text.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-395">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="8d5bd-396">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="8d5bd-396">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="8d5bd-397">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="8d5bd-397">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="8d5bd-398">Ändrade beteende för Start-AzAutomationDscCompilationJob till att bara starta jobbet istället för att vänta på slutförandet.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-398">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="8d5bd-399">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="8d5bd-399">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="8d5bd-400">Korrigering för Get-AzAutomationDscNode när using -Name returnerar alla noder.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-400">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="8d5bd-401">Nu returnerar den endast den matchande noden.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-401">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d5bd-402">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d5bd-402">Az.Compute</span></span>
* <span data-ttu-id="8d5bd-403">Lägg till parametrarna ProtectFromScaleIn och ProtectFromScaleSetAction i cmdleten Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-403">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="8d5bd-404">Nu är standardinställningen att vimpelparametern New-AzVM använder en tillgänglig plats om USA, östra inte stöds</span><span class="sxs-lookup"><span data-stu-id="8d5bd-404">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8d5bd-405">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8d5bd-405">Az.DataLakeStore</span></span>
* <span data-ttu-id="8d5bd-406">Uppdatera ADLS-sdk för att använda httpclient, integrera dataplanstestning med Azure-ramverk</span><span class="sxs-lookup"><span data-stu-id="8d5bd-406">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8d5bd-407">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8d5bd-407">Az.Monitor</span></span>
* <span data-ttu-id="8d5bd-408">Korrigera felaktiga parameternamn i hjälpexempel</span><span class="sxs-lookup"><span data-stu-id="8d5bd-408">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8d5bd-409">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d5bd-409">Az.Network</span></span>
* <span data-ttu-id="8d5bd-410">Lägg till flaggan DisableBgpRoutePropagation i utdata för effektiv routningstabell</span><span class="sxs-lookup"><span data-stu-id="8d5bd-410">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="8d5bd-411">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="8d5bd-411">Updated cmdlet:</span></span>
        - <span data-ttu-id="8d5bd-412">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="8d5bd-412">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="8d5bd-413">Åtgärda dubbelstreck i dokumentationen New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="8d5bd-413">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="8d5bd-414">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d5bd-414">Az.Resources</span></span>
* <span data-ttu-id="8d5bd-415">Lägg till ny cmdlet Get-AzureRmDenyAssignment för att hämta tilldelningsnekanden</span><span class="sxs-lookup"><span data-stu-id="8d5bd-415">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="8d5bd-416">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d5bd-416">Az.Sql</span></span>
* <span data-ttu-id="8d5bd-417">Döp om Advanced Threat Protection-cmdletar för Advanced Data Security och aktivera Vulnerability Assessment som standard</span><span class="sxs-lookup"><span data-stu-id="8d5bd-417">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="8d5bd-418">2.0.0 – maj 2019</span><span class="sxs-lookup"><span data-stu-id="8d5bd-418">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8d5bd-419">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8d5bd-419">Az.Accounts</span></span>
* <span data-ttu-id="8d5bd-420">Uppdatera autentiseringsbiblioteket för att åtgärda ADFS-problem med autentisering av användarnamn/lösenord</span><span class="sxs-lookup"><span data-stu-id="8d5bd-420">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="8d5bd-421">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8d5bd-421">Az.CognitiveServices</span></span>
* <span data-ttu-id="8d5bd-422">Visa endast Bing-ansvarsfriskrivning för Bing-sökningstjänster.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-422">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="8d5bd-423">Förbättra felmeddelande när det inte går att skapa konton.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-423">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d5bd-424">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d5bd-424">Az.Compute</span></span>
* <span data-ttu-id="8d5bd-425">Funktion för närhetsplaceringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-425">Proximity placement group feature.</span></span>
    - <span data-ttu-id="8d5bd-426">Följande nya cmdletar har lagts till:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="8d5bd-426">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="8d5bd-427">Den nya parametern ProximityPlacementGroupId har lagts till i följande cmdletar:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="8d5bd-427">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="8d5bd-428">Parametern StorageAccountType har lagts till i New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-428">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="8d5bd-429">TargetRegion för New-AzGalleryImageVersion kan innehålla StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-429">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="8d5bd-430">Växlingsparametern SkipShutdown har lagts till i Stop-AzVM och Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8d5bd-430">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="8d5bd-431">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="8d5bd-431">Breaking changes</span></span>
    - <span data-ttu-id="8d5bd-432">Set-AzVMBootDiagnostics har ändrats till Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-432">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="8d5bd-433">Export-AzLogAnalyticThrottledRequests har ändrats till Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-433">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="8d5bd-434">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="8d5bd-434">Az.DeploymentManager</span></span>
* <span data-ttu-id="8d5bd-435">De första allmänt tillgängliga versionerna av cmdletar för Distributionshanteraren i Azure</span><span class="sxs-lookup"><span data-stu-id="8d5bd-435">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="8d5bd-436">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="8d5bd-436">Az.Dns</span></span>
* <span data-ttu-id="8d5bd-437">Automatisk delegering av DNS för NameServer</span><span class="sxs-lookup"><span data-stu-id="8d5bd-437">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="8d5bd-438">Det överordnade zonnamnet kan användas som ytterligare valfri parameter i cmdleten för att skapa DNS-zoner.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-438">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="8d5bd-439">Lägger till NS-poster för en nyligen skapad underordnad zon i den överordnade zonen.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-439">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="8d5bd-440">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="8d5bd-440">Az.FrontDoor</span></span>
* <span data-ttu-id="8d5bd-441">De första allmänt tillgängliga versionerna av cmdletar för Azure FrontDoor</span><span class="sxs-lookup"><span data-stu-id="8d5bd-441">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="8d5bd-442">Byt namn på WAF-cmdletar så att de omfattar ”Waf”</span><span class="sxs-lookup"><span data-stu-id="8d5bd-442">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="8d5bd-443">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8d5bd-443">Az.HDInsight</span></span>
* <span data-ttu-id="8d5bd-444">Två cmdletar har tagits bort:</span><span class="sxs-lookup"><span data-stu-id="8d5bd-444">Removed two cmdlets:</span></span>
    - <span data-ttu-id="8d5bd-445">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="8d5bd-445">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="8d5bd-446">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="8d5bd-446">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="8d5bd-447">En ny cmdlet har lagts till, Set-AzHDInsightGatewayCredential, som ersätter Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="8d5bd-447">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="8d5bd-448">Uppdatera cmdleten Get-AzHDInsightJobOutput för att skilja mellan läsarrollen och HDInsight-operatörsrollen:</span><span class="sxs-lookup"><span data-stu-id="8d5bd-448">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="8d5bd-449">Användare med läsarrollen måste uttryckligen ange parametern ”DefaultStorageAccountKey”, annars uppstår fel.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-449">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="8d5bd-450">Användare med HDInsight-operatörsrollen påverkas inte.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-450">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8d5bd-451">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8d5bd-451">Az.Monitor</span></span>
* <span data-ttu-id="8d5bd-452">Nya cmdletar för SQR API (schemalagd frågeregel)</span><span class="sxs-lookup"><span data-stu-id="8d5bd-452">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="8d5bd-453">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="8d5bd-453">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="8d5bd-454">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="8d5bd-454">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="8d5bd-455">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="8d5bd-455">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="8d5bd-456">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="8d5bd-456">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="8d5bd-457">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="8d5bd-457">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="8d5bd-458">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="8d5bd-458">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="8d5bd-459">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="8d5bd-459">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="8d5bd-460">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="8d5bd-460">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="8d5bd-461">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="8d5bd-461">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="8d5bd-462">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="8d5bd-462">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="8d5bd-463">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="8d5bd-463">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="8d5bd-464">[Mer](https://docs.microsoft.com/en-us/rest/api/monitor/scheduledqueryrules) information om SQR API</span><span class="sxs-lookup"><span data-stu-id="8d5bd-464">[More](https://docs.microsoft.com/en-us/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="8d5bd-465">Az.Monitor.md har uppdaterats för att omfatta cmdletar för måttbaserade aviseringsregler i GenV2 (inte klassiska)</span><span class="sxs-lookup"><span data-stu-id="8d5bd-465">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8d5bd-466">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d5bd-466">Az.Network</span></span>
* <span data-ttu-id="8d5bd-467">Lägg till stöd för NAT Gateway-resurs</span><span class="sxs-lookup"><span data-stu-id="8d5bd-467">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="8d5bd-468">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="8d5bd-468">New cmdlets</span></span>
        - <span data-ttu-id="8d5bd-469">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="8d5bd-469">New-AzNatGateway</span></span>
        - <span data-ttu-id="8d5bd-470">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="8d5bd-470">Get-AzNatGateway</span></span>
        - <span data-ttu-id="8d5bd-471">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="8d5bd-471">Set-AzNatGateway</span></span>
        - <span data-ttu-id="8d5bd-472">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="8d5bd-472">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="8d5bd-473">Uppdaterade cmdletar</span><span class="sxs-lookup"><span data-stu-id="8d5bd-473">Updated cmdlets</span></span>
        - <span data-ttu-id="8d5bd-474">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="8d5bd-474">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="8d5bd-475">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="8d5bd-475">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="8d5bd-476">Nedanstående kommandon för funktionen har uppdaterats: Ange/ta bort anpassade vägar på Brooklyn Gateway.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-476">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="8d5bd-477">New-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ställa in adressprefix som anpassade vägar för att ange gateway.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-477">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="8d5bd-478">Set-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ange adressprefix som anpassade vägar för att ange gateway.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-478">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="8d5bd-479">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="8d5bd-479">Az.PolicyInsights</span></span>
* <span data-ttu-id="8d5bd-480">Stöd för att fråga efter information om principutvärdering.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-480">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="8d5bd-481">Lägg till parametern ”-Expand” för Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-481">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="8d5bd-482">Stöd för -Expand PolicyEvaluationDetails.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-482">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8d5bd-483">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8d5bd-483">Az.RecoveryServices</span></span>
* <span data-ttu-id="8d5bd-484">Stöd för att dela prenumeration mellan Azure och Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-484">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="8d5bd-485">Markering av kommande icke-bakåtkompatibla ändringar för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-485">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="8d5bd-486">Korrigering för återställningsplan och åtgärdsplan i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-486">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="8d5bd-487">Korrigering för mappning av uppdateringsnätverk i Azure Site Recovery för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-487">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="8d5bd-488">Korrigering för instruktioner för uppdateringsskydd i Azure Site Recovery för Azure till Azure för hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-488">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="8d5bd-489">Andra mindre korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-489">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="8d5bd-490">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="8d5bd-490">Az.Relay</span></span>
* <span data-ttu-id="8d5bd-491">Korrigera stavfel i kundriktade meddelanden</span><span class="sxs-lookup"><span data-stu-id="8d5bd-491">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="8d5bd-492">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8d5bd-492">Az.ServiceBus</span></span>
* <span data-ttu-id="8d5bd-493">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="8d5bd-493">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8d5bd-494">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8d5bd-494">Az.Storage</span></span>
* <span data-ttu-id="8d5bd-495">Uppgradera till lagringsklientbiblioteket 10.0.1 (namnområdet för alla objekt från detta SDK ändras från ”Microsoft.WindowsAzure.Storage. *till ”Microsoft.Azure.Storage.* ”)</span><span class="sxs-lookup"><span data-stu-id="8d5bd-495">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="8d5bd-496">Uppgradera till Microsoft.Azure.Management.Storage 11.0.0 för att stödja den nya API-versionen 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-496">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="8d5bd-497">Standardlagringskontot i Skapa lagringskonto ändras från ”Storage” till ”StorageV2”</span><span class="sxs-lookup"><span data-stu-id="8d5bd-497">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="8d5bd-498">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8d5bd-498">New-AzStorageAccount</span></span>
* <span data-ttu-id="8d5bd-499">Ändra lagringskontots cmdlet-utdata Sku.Name för att passa med indata-SkuName genom att lägga till ”-”. Till exempel ändras ”StandardLRS” till ”Standard_LRS”</span><span class="sxs-lookup"><span data-stu-id="8d5bd-499">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="8d5bd-500">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8d5bd-500">New-AzStorageAccount</span></span>
    - <span data-ttu-id="8d5bd-501">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8d5bd-501">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="8d5bd-502">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8d5bd-502">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8d5bd-503">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8d5bd-503">Az.Websites</span></span>
* <span data-ttu-id="8d5bd-504">Egenskapen ”typ” konfigureras nu för PSSite-objekt som returneras av Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8d5bd-504">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="8d5bd-505">Get-AzWebApp\*Metrics och Get-AzAppServicePlanMetrics markeras som inaktuella</span><span class="sxs-lookup"><span data-stu-id="8d5bd-505">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="8d5bd-506">1.8.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="8d5bd-506">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="8d5bd-507">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="8d5bd-507">Highlights since the last major release</span></span>
* <span data-ttu-id="8d5bd-508">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="8d5bd-508">General availability of `Az` module</span></span>
* <span data-ttu-id="8d5bd-509">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="8d5bd-509">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="8d5bd-510">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="8d5bd-510">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="8d5bd-511">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d5bd-511">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="8d5bd-512">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d5bd-512">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="8d5bd-513">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d5bd-513">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="8d5bd-514">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="8d5bd-514">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="8d5bd-515">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8d5bd-515">Az.Accounts</span></span>
* <span data-ttu-id="8d5bd-516">Uppdatera Uninstall-AzureRm för att ta bort moduler i Mac på ett korrekt sätt</span><span class="sxs-lookup"><span data-stu-id="8d5bd-516">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="8d5bd-517">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="8d5bd-517">Az.Batch</span></span>
* <span data-ttu-id="8d5bd-518">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-518">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="8d5bd-519">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="8d5bd-519">Az.Cdn</span></span>
* <span data-ttu-id="8d5bd-520">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-520">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="8d5bd-521">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8d5bd-521">Az.CognitiveServices</span></span>
* <span data-ttu-id="8d5bd-522">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-522">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d5bd-523">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d5bd-523">Az.Compute</span></span>
* <span data-ttu-id="8d5bd-524">Åtgärda problem med AEM-installationen om resurs-ID:n för diskar innehåller resourcegroups i gemener i resurs-ID:n</span><span class="sxs-lookup"><span data-stu-id="8d5bd-524">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="8d5bd-525">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-525">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8d5bd-526">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="8d5bd-526">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8d5bd-527">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8d5bd-527">Az.DataFactory</span></span>
* <span data-ttu-id="8d5bd-528">Lägg till SsisProperties om NodeCount inte är null för hanterad integreringskörning.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-528">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8d5bd-529">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8d5bd-529">Az.DataLakeStore</span></span>
* <span data-ttu-id="8d5bd-530">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-530">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="8d5bd-531">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="8d5bd-531">Az.EventGrid</span></span>
* <span data-ttu-id="8d5bd-532">Hjälptexten för slutpunkten har uppdaterats för att visa att resurser ska skapas innan cmdletarna för att skapa/uppdatera händelseprenumerationer används.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-532">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="8d5bd-533">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8d5bd-533">Az.EventHub</span></span>
* <span data-ttu-id="8d5bd-534">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="8d5bd-534">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="8d5bd-535">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8d5bd-535">Az.HDInsight</span></span>
* <span data-ttu-id="8d5bd-536">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-536">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8d5bd-537">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8d5bd-537">Az.IotHub</span></span>
* <span data-ttu-id="8d5bd-538">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-538">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8d5bd-539">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8d5bd-539">Az.KeyVault</span></span>
* <span data-ttu-id="8d5bd-540">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-540">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8d5bd-541">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="8d5bd-541">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="8d5bd-542">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="8d5bd-542">Az.MachineLearning</span></span>
* <span data-ttu-id="8d5bd-543">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-543">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="8d5bd-544">Az.Media</span><span class="sxs-lookup"><span data-stu-id="8d5bd-544">Az.Media</span></span>
* <span data-ttu-id="8d5bd-545">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-545">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8d5bd-546">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8d5bd-546">Az.Monitor</span></span>
  * <span data-ttu-id="8d5bd-547">Nya cmdletar för måttbaserad aviseringsregel i GenV2 (inte klassisk)</span><span class="sxs-lookup"><span data-stu-id="8d5bd-547">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="8d5bd-548">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="8d5bd-548">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="8d5bd-549">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="8d5bd-549">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="8d5bd-550">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="8d5bd-550">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="8d5bd-551">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="8d5bd-551">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="8d5bd-552">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="8d5bd-552">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="8d5bd-553">Monitor SDK har uppdaterats till version 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="8d5bd-553">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8d5bd-554">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d5bd-554">Az.Network</span></span>
* <span data-ttu-id="8d5bd-555">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-555">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8d5bd-556">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="8d5bd-556">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="8d5bd-557">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="8d5bd-557">Az.NotificationHubs</span></span>
* <span data-ttu-id="8d5bd-558">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-558">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8d5bd-559">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8d5bd-559">Az.OperationalInsights</span></span>
* <span data-ttu-id="8d5bd-560">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-560">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="8d5bd-561">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="8d5bd-561">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="8d5bd-562">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-562">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8d5bd-563">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8d5bd-563">Az.RecoveryServices</span></span>
* <span data-ttu-id="8d5bd-564">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-564">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8d5bd-565">Tabellformatet för SQL i virtuella Azure-datorer har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="8d5bd-565">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="8d5bd-566">En alternativ metod för att hämta platser i AzureFileShare har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d5bd-566">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="8d5bd-567">ScheduleRunDays i SchedulePolicy-objekt har uppdaterats enligt tidszon</span><span class="sxs-lookup"><span data-stu-id="8d5bd-567">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="8d5bd-568">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="8d5bd-568">Az.RedisCache</span></span>
* <span data-ttu-id="8d5bd-569">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-569">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8d5bd-570">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d5bd-570">Az.Resources</span></span>
* <span data-ttu-id="8d5bd-571">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="8d5bd-571">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="8d5bd-572">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d5bd-572">Az.Sql</span></span>
* <span data-ttu-id="8d5bd-573">Ersätt Monitor SDK-beroende med vanlig kod</span><span class="sxs-lookup"><span data-stu-id="8d5bd-573">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="8d5bd-574">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-574">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8d5bd-575">Förbättrad process för klassificering av flera kolumner.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-575">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="8d5bd-576">Inkludera SKU-egenskaper (SKU-namn, serie, kapacitet) i svaret från Get-AzSqlServerServiceObjective och formatera som tabell som standard.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-576">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="8d5bd-577">Möjlighet att använda Get-AzSqlServerServiceObjective efter plats utan att behöva en redan befintlig server i regionen.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-577">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="8d5bd-578">Stöd för tidszonsparametern när hanterade instanser skapas.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-578">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="8d5bd-579">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="8d5bd-579">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8d5bd-580">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8d5bd-580">Az.Websites</span></span>
* <span data-ttu-id="8d5bd-581">åtgärdar Set-AzWebApp och Set-AzWebAppSlot så att de inte tar bort taggar vid körning</span><span class="sxs-lookup"><span data-stu-id="8d5bd-581">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="8d5bd-582">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-582">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8d5bd-583">SDK för WebSites har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-583">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="8d5bd-584">Egenskapen AdminSiteName har tagits bort från PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-584">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="8d5bd-585">1.7.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="8d5bd-585">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="8d5bd-586">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="8d5bd-586">Highlights since the last major release</span></span>
* <span data-ttu-id="8d5bd-587">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="8d5bd-587">General availability of `Az` module</span></span>
* <span data-ttu-id="8d5bd-588">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="8d5bd-588">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="8d5bd-589">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="8d5bd-589">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="8d5bd-590">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d5bd-590">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="8d5bd-591">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d5bd-591">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="8d5bd-592">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d5bd-592">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="8d5bd-593">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="8d5bd-593">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="8d5bd-594">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8d5bd-594">Az.Accounts</span></span>
* <span data-ttu-id="8d5bd-595">Add-AzEnvironment och Set-AzEnvironment har uppdaterats för att godkänna parametern AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="8d5bd-595">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="8d5bd-596">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8d5bd-596">Az.AnalysisServices</span></span>
* <span data-ttu-id="8d5bd-597">ServiceClient används i cmdletar för dataplan och den ursprungliga autentiseringslogiken har tagits bort</span><span class="sxs-lookup"><span data-stu-id="8d5bd-597">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="8d5bd-598">Add-AzureASAccount används för omslutning av Connect-AzAccount för att undvika en icke-bakåtkompatibel ändring</span><span class="sxs-lookup"><span data-stu-id="8d5bd-598">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8d5bd-599">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8d5bd-599">Az.Automation</span></span>
* <span data-ttu-id="8d5bd-600">Buggen för cmdleten New-AzAutomationSoftwareUpdateConfiguration för inkluderingar har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-600">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="8d5bd-601">Nu bör parametern IncludedKbNumber och IncludedPackageNameMask fungera.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-601">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="8d5bd-602">Felkorrigering för dynamiska grupper i uppdateringshanteringen för azure automation</span><span class="sxs-lookup"><span data-stu-id="8d5bd-602">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d5bd-603">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d5bd-603">Az.Compute</span></span>
* <span data-ttu-id="8d5bd-604">Lägg till parametern HyperVGeneration i New-AzDiskConfig och New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="8d5bd-604">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="8d5bd-605">Tillåt att virtuella datorer skapas med galleribilder från andra klientorganisationer.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-605">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="8d5bd-606">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="8d5bd-606">Az.ContainerInstance</span></span>
* <span data-ttu-id="8d5bd-607">Ett problem har åtgärdats i parametern -Command för New-AzContainerGroup som lade till ett avslutande tomt argument</span><span class="sxs-lookup"><span data-stu-id="8d5bd-607">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8d5bd-608">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8d5bd-608">Az.DataFactory</span></span>
* <span data-ttu-id="8d5bd-609">ADF .Net SDK-versionen har uppdaterats till 3.0.2</span><span class="sxs-lookup"><span data-stu-id="8d5bd-609">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="8d5bd-610">Cmdleten Set-AzDataFactoryV2 har uppdaterats med extra parametrar för inställningar som rör RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-610">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8d5bd-611">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d5bd-611">Az.Resources</span></span>
* <span data-ttu-id="8d5bd-612">Förbättra hanteringen av providrar för Get-AzResource när parametrarna -ResourceId eller -ResourceGroupName, -Name och -ResourceType tillhandahålls</span><span class="sxs-lookup"><span data-stu-id="8d5bd-612">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="8d5bd-613">Förbättra felhanteringen för ”Test-AzDeployment” och ”Test-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="8d5bd-613">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="8d5bd-614">Hantera fel utanför distributionsvalideringen och ta med dem i kommandoutdata istället</span><span class="sxs-lookup"><span data-stu-id="8d5bd-614">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="8d5bd-615">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="8d5bd-615">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="8d5bd-616">Lägg till växlingsparametern -IgnoreDynamicParameters till en uppsättning av cmdletar för distribution för att hoppa över fråga i skript och jobbscenarier</span><span class="sxs-lookup"><span data-stu-id="8d5bd-616">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="8d5bd-617">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="8d5bd-617">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="8d5bd-618">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d5bd-618">Az.Sql</span></span>
* <span data-ttu-id="8d5bd-619">Stöd för dataklassificering av databaser.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-619">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8d5bd-620">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8d5bd-620">Az.Storage</span></span>
* <span data-ttu-id="8d5bd-621">Rapportera detaljfel när lagringskontext skapas med parametern -UseConnectedAccount, men utan inloggning på Azure-kontot</span><span class="sxs-lookup"><span data-stu-id="8d5bd-621">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="8d5bd-622">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="8d5bd-622">New-AzStorageContext</span></span>
* <span data-ttu-id="8d5bd-623">Stöd för att hantera Blob Service-egenskaper för ett angivet lagringskonto med API:et för hanteringsplan</span><span class="sxs-lookup"><span data-stu-id="8d5bd-623">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="8d5bd-624">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="8d5bd-624">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="8d5bd-625">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="8d5bd-625">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="8d5bd-626">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8d5bd-626">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="8d5bd-627">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8d5bd-627">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="8d5bd-628">Stöd för -AsJob-cmdletar för att ladda upp och ladda ned blobar och filer</span><span class="sxs-lookup"><span data-stu-id="8d5bd-628">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="8d5bd-629">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="8d5bd-629">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="8d5bd-630">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="8d5bd-630">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="8d5bd-631">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="8d5bd-631">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="8d5bd-632">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="8d5bd-632">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="8d5bd-633">1.6.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="8d5bd-633">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="8d5bd-634">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="8d5bd-634">Highlights since the last major release</span></span>
* <span data-ttu-id="8d5bd-635">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="8d5bd-635">General availability of `Az` module</span></span>
* <span data-ttu-id="8d5bd-636">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="8d5bd-636">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="8d5bd-637">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="8d5bd-637">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="8d5bd-638">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d5bd-638">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="8d5bd-639">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d5bd-639">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="8d5bd-640">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d5bd-640">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="8d5bd-641">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="8d5bd-641">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8d5bd-642">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8d5bd-642">Az.Automation</span></span>
* <span data-ttu-id="8d5bd-643">Azure Automation – ändring av uppdateringshantering för stöd för de nya funktionerna:</span><span class="sxs-lookup"><span data-stu-id="8d5bd-643">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="8d5bd-644">Dynamisk gruppering</span><span class="sxs-lookup"><span data-stu-id="8d5bd-644">Dynamic grouping</span></span>
    * <span data-ttu-id="8d5bd-645">För-/efterskrift</span><span class="sxs-lookup"><span data-stu-id="8d5bd-645">Pre-Post script</span></span>
    * <span data-ttu-id="8d5bd-646">Inställning för omstart</span><span class="sxs-lookup"><span data-stu-id="8d5bd-646">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d5bd-647">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d5bd-647">Az.Compute</span></span>
* <span data-ttu-id="8d5bd-648">Åtgärda problem med sökvägsmatchning i Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="8d5bd-648">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="8d5bd-649">Uppdatera Compute-klientbibliotek till 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-649">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8d5bd-650">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8d5bd-650">Az.KeyVault</span></span>
* <span data-ttu-id="8d5bd-651">Stöd för jokertecken för KeyVault-cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d5bd-651">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8d5bd-652">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d5bd-652">Az.Network</span></span>
* <span data-ttu-id="8d5bd-653">Lägg till stöd för Threat Intelligence för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="8d5bd-653">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="8d5bd-654">Lägg till resurs för brandväggsprincip på översta nivå och anpassade regler för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="8d5bd-654">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8d5bd-655">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8d5bd-655">Az.RecoveryServices</span></span>
* <span data-ttu-id="8d5bd-656">SnapshotRetentionInDays har lagts till i Azure-principen för virtuella datorer för stöd av Instant RP</span><span class="sxs-lookup"><span data-stu-id="8d5bd-656">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="8d5bd-657">Pipe-stöd för avregistrering av container har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d5bd-657">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="8d5bd-658">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d5bd-658">Az.Resources</span></span>
* <span data-ttu-id="8d5bd-659">Uppdatera stöd för jokertecken för Get-AzResource och Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8d5bd-659">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="8d5bd-660">Uppdatera autentiseringsuppgifter som används vid allmänna anrop till ARM</span><span class="sxs-lookup"><span data-stu-id="8d5bd-660">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="8d5bd-661">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d5bd-661">Az.Sql</span></span>
* <span data-ttu-id="8d5bd-662">Cmdlet-parametern (ExcludeDetectionType) för Hotidentifiering ändrades från DetectionType till sträng[] för att framtidssäkra den när nya DetectionTypes läggs till, och även för att stödja automatisk ifyllning.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-662">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8d5bd-663">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8d5bd-663">Az.Storage</span></span>
* <span data-ttu-id="8d5bd-664">Stöd för att hämta/ange/ta bort hanteringsprincip på ett lagringskonto</span><span class="sxs-lookup"><span data-stu-id="8d5bd-664">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="8d5bd-665">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="8d5bd-665">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="8d5bd-666">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="8d5bd-666">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="8d5bd-667">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="8d5bd-667">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="8d5bd-668">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="8d5bd-668">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="8d5bd-669">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="8d5bd-669">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="8d5bd-670">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="8d5bd-670">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8d5bd-671">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8d5bd-671">Az.Websites</span></span>
* <span data-ttu-id="8d5bd-672">Åtgärda fel med ARM-mall som avbryter kloning av alla platser med 'New-AzWebApp -IncludeSourceWebAppSlots'</span><span class="sxs-lookup"><span data-stu-id="8d5bd-672">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="8d5bd-673">1.5.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="8d5bd-673">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8d5bd-674">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8d5bd-674">Az.Accounts</span></span>
* <span data-ttu-id="8d5bd-675">Lägg till kommandot Register-AzModule för stöd för AutoRest-genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="8d5bd-675">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="8d5bd-676">Uppdatera exempel för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="8d5bd-676">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8d5bd-677">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8d5bd-677">Az.Automation</span></span>
* <span data-ttu-id="8d5bd-678">Problem med att hämta vissa månadsscheman i flera Azure Automation-cmdletar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8d5bd-678">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="8d5bd-679">Åtgärda problem med att Get-AzAutomationDscNode bara returnerar de 20 översta noderna.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-679">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="8d5bd-680">Nu returneras alla noder</span><span class="sxs-lookup"><span data-stu-id="8d5bd-680">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="8d5bd-681">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="8d5bd-681">Az.Cdn</span></span>
* <span data-ttu-id="8d5bd-682">Nya Powershell-cmdletar för att aktivera/inaktivera anpassade domän-HTTPS har lagts till och de gamla har gjorts inaktuella</span><span class="sxs-lookup"><span data-stu-id="8d5bd-682">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d5bd-683">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d5bd-683">Az.Compute</span></span>
* <span data-ttu-id="8d5bd-684">Lägg till stöd för jokertecken för Get-cmdletar</span><span class="sxs-lookup"><span data-stu-id="8d5bd-684">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8d5bd-685">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8d5bd-685">Az.DataFactory</span></span>
* <span data-ttu-id="8d5bd-686">ADF .Net SDK-versionen har uppdaterats till 3.0.1</span><span class="sxs-lookup"><span data-stu-id="8d5bd-686">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="8d5bd-687">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="8d5bd-687">Az.LogicApp</span></span>
* <span data-ttu-id="8d5bd-688">Åtgärda problemet med att ListWorkflows endast hämtar den första sidan med resultat</span><span class="sxs-lookup"><span data-stu-id="8d5bd-688">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8d5bd-689">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d5bd-689">Az.Network</span></span>
* <span data-ttu-id="8d5bd-690">Lägg till stöd för jokertecken för Network-cmdletar</span><span class="sxs-lookup"><span data-stu-id="8d5bd-690">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8d5bd-691">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8d5bd-691">Az.RecoveryServices</span></span>
* <span data-ttu-id="8d5bd-692">Stöd har lagts till för SQL Server i virtuella Azure-datorer</span><span class="sxs-lookup"><span data-stu-id="8d5bd-692">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="8d5bd-693">SDK-uppdatering</span><span class="sxs-lookup"><span data-stu-id="8d5bd-693">SDK Update</span></span>
* <span data-ttu-id="8d5bd-694">Get-ProtectableItem-incheckning i VMappContainer har tagits bort</span><span class="sxs-lookup"><span data-stu-id="8d5bd-694">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="8d5bd-695">Name och ServerName har lagts till som parametrar för Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="8d5bd-695">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="8d5bd-696">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d5bd-696">Az.Resources</span></span>
* <span data-ttu-id="8d5bd-697">Lägg till parametern `-TemplateObject` i cmdletar för distribution</span><span class="sxs-lookup"><span data-stu-id="8d5bd-697">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="8d5bd-698">Mer information här: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="8d5bd-698">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="8d5bd-699">Åtgärda problem med piping av resultatet i `Get-AzResource` till `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="8d5bd-699">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="8d5bd-700">Mer information här: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="8d5bd-700">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="8d5bd-701">Åtgärda problem med ändring av JSON-datatyp när `Set-AzResource` körs</span><span class="sxs-lookup"><span data-stu-id="8d5bd-701">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="8d5bd-702">Mer information här: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="8d5bd-702">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="8d5bd-703">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d5bd-703">Az.Sql</span></span>
* <span data-ttu-id="8d5bd-704">AuditingEndpointsCommunicator uppdateras.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-704">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="8d5bd-705">Åtgärdar beteendet hos ett gränsscenario när nya diagnostikinställningar skapas.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-705">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8d5bd-706">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8d5bd-706">Az.Storage</span></span>
* <span data-ttu-id="8d5bd-707">Stöd för BlockBlobStorage när Storage-konto skapas      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8d5bd-707">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="8d5bd-708">1.4.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="8d5bd-708">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="8d5bd-709">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8d5bd-709">Az.AnalysisServices</span></span>
* <span data-ttu-id="8d5bd-710">Inaktuell AddAzureASAccount-cmdlet</span><span class="sxs-lookup"><span data-stu-id="8d5bd-710">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8d5bd-711">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8d5bd-711">Az.Automation</span></span>
* <span data-ttu-id="8d5bd-712">Hjälpen för Import-AzAutomationDscNodeConfiguration har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="8d5bd-712">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="8d5bd-713">Konfigurationsnamnsvalidering har lagts till i cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="8d5bd-713">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="8d5bd-714">Förbättrad felhantering för cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="8d5bd-714">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="8d5bd-715">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8d5bd-715">Az.CognitiveServices</span></span>
* <span data-ttu-id="8d5bd-716">CustomSubdomainName har lagts till som en ny valfri parameter för New-AzCognitiveServicesAccount, som används för att ange underdomän för resursen.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-716">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d5bd-717">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d5bd-717">Az.Compute</span></span>
* <span data-ttu-id="8d5bd-718">Problemet med ID-parameteruppsättningar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8d5bd-718">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="8d5bd-719">Get-AzVMExtension har uppdaterats så att alla installerade tillägg visas om parametern Name inte har angetts</span><span class="sxs-lookup"><span data-stu-id="8d5bd-719">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="8d5bd-720">Parametrarna Tag och ResourceId har lagts till i cmdleten Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="8d5bd-720">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="8d5bd-721">Get-AzVmssVM utan instans-ID och med InstanceView kan visa virtuella VMSS-datorer med instansvyn.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-721">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8d5bd-722">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8d5bd-722">Az.DataLakeStore</span></span>
* <span data-ttu-id="8d5bd-723">Cmdletar har lagts till för uppräkning och återställning av borttagna objekt i ADL</span><span class="sxs-lookup"><span data-stu-id="8d5bd-723">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="8d5bd-724">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8d5bd-724">Az.EventHub</span></span>
* <span data-ttu-id="8d5bd-725">Ny boolesk egenskap SkipEmptyArchives har lagts till i Skip Empty Archives i CaptureDescription-klassen i Eventhub</span><span class="sxs-lookup"><span data-stu-id="8d5bd-725">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="8d5bd-726">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8d5bd-726">Az.KeyVault</span></span>
* <span data-ttu-id="8d5bd-727">Taggning i Set-AzKeyVaultSecret har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8d5bd-727">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="8d5bd-728">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="8d5bd-728">Az.LogicApp</span></span>
* <span data-ttu-id="8d5bd-729">Grundläggande SKU har lagts till för Integrationskonton</span><span class="sxs-lookup"><span data-stu-id="8d5bd-729">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="8d5bd-730">XSLT 2.0, XSLT 3.0 och Flytande mappningstyper har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d5bd-730">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="8d5bd-731">Nya cmdletar för integrationskontosammansättningar</span><span class="sxs-lookup"><span data-stu-id="8d5bd-731">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="8d5bd-732">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="8d5bd-732">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="8d5bd-733">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="8d5bd-733">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="8d5bd-734">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="8d5bd-734">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="8d5bd-735">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="8d5bd-735">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="8d5bd-736">Nya cmdletar för batchkonfiguration för integrationskonto</span><span class="sxs-lookup"><span data-stu-id="8d5bd-736">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="8d5bd-737">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="8d5bd-737">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="8d5bd-738">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="8d5bd-738">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="8d5bd-739">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="8d5bd-739">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="8d5bd-740">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="8d5bd-740">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="8d5bd-741">Logic App-SDK har uppdaterats till version 4.1.0</span><span class="sxs-lookup"><span data-stu-id="8d5bd-741">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8d5bd-742">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8d5bd-742">Az.Monitor</span></span>
* <span data-ttu-id="8d5bd-743">Hjälpen för Get-AzMetric har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="8d5bd-743">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8d5bd-744">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d5bd-744">Az.Network</span></span>
* <span data-ttu-id="8d5bd-745">Hjälpexempel för Add-AzApplicationGatewayCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d5bd-745">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8d5bd-746">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8d5bd-746">Az.OperationalInsights</span></span>
* <span data-ttu-id="8d5bd-747">Ytterligare stöd för datakällorna New och Get ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-747">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="8d5bd-748">Ny ApplicationInsights-typ har lagts till för att ge stöd för ”Get specific” och ”Get all” för ApplicationInsights-datakällor för angiven arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-748">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="8d5bd-749">Cmdleten New-AzOperationalInsightsApplicationInsightsDataSource har lagts till för att skapa datakälla med angivna parametrar för Application Insights-resurs: subscription Id, resourceGroupName och name.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-749">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="8d5bd-750">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d5bd-750">Az.Resources</span></span>
* <span data-ttu-id="8d5bd-751">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="8d5bd-751">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="8d5bd-752">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="8d5bd-752">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="8d5bd-753">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="8d5bd-753">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="8d5bd-754">Fel som gör att KeyCredentials inte kan skapas upprepade gånger har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8d5bd-754">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="8d5bd-755">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d5bd-755">Az.Sql</span></span>
* <span data-ttu-id="8d5bd-756">Lägg till stöd för hyperskalanivån för SQL DB</span><span class="sxs-lookup"><span data-stu-id="8d5bd-756">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="8d5bd-757">Ett fel har åtgärdats där återställningen kunde misslyckas på grund av onödiga inställningsegenskaper i restore-förfrågan</span><span class="sxs-lookup"><span data-stu-id="8d5bd-757">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8d5bd-758">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8d5bd-758">Az.Websites</span></span>
* <span data-ttu-id="8d5bd-759">Rätt exempel i Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="8d5bd-759">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="8d5bd-760">1.3.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="8d5bd-760">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8d5bd-761">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8d5bd-761">Az.Accounts</span></span>
* <span data-ttu-id="8d5bd-762">Uppdatera till den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="8d5bd-762">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="8d5bd-763">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8d5bd-763">Az.AnalysisServices</span></span>
<span data-ttu-id="8d5bd-764">Allmän tillgänglighet för Az.AnalysisServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-764">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d5bd-765">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d5bd-765">Az.Compute</span></span>
* <span data-ttu-id="8d5bd-766">AEM-tillägg: Lägg till stöd för UltraSSD-, P60-, P70- och P80-diskar</span><span class="sxs-lookup"><span data-stu-id="8d5bd-766">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="8d5bd-767">Uppdatera hjälpbeskrivning för Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="8d5bd-767">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="8d5bd-768">Uppdatera hjälpbeskrivning och exempel för Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="8d5bd-768">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8d5bd-769">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8d5bd-769">Az.RecoveryServices</span></span>
<span data-ttu-id="8d5bd-770">Allmän tillgänglighet för Az.RecoveryServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-770">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8d5bd-771">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d5bd-771">Az.Resources</span></span>
* <span data-ttu-id="8d5bd-772">Korrigera taggar för resursgrupper</span><span class="sxs-lookup"><span data-stu-id="8d5bd-772">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="8d5bd-773">Mer information här: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="8d5bd-773">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="8d5bd-774">Åtgärda problem där `Get-AzureRmRoleAssignment` inte respekterar -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="8d5bd-774">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="8d5bd-775">Mer information här: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="8d5bd-775">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="8d5bd-776">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d5bd-776">Az.Sql</span></span>
* <span data-ttu-id="8d5bd-777">Lägga till Get/Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8d5bd-777">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="8d5bd-778">Åtgärda problem där ett nullref-undantag uppstår när du kör SQL-cmdletar och inte är inloggad på ett Azure-konto</span><span class="sxs-lookup"><span data-stu-id="8d5bd-778">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="8d5bd-779">Åtgärda nullref-undantag i Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="8d5bd-779">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="8d5bd-780">1.2.1 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="8d5bd-780">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8d5bd-781">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8d5bd-781">Az.Accounts</span></span>
* <span data-ttu-id="8d5bd-782">Version med rätt version av autentisering</span><span class="sxs-lookup"><span data-stu-id="8d5bd-782">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="8d5bd-783">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8d5bd-783">Az.AnalysisServices</span></span>
* <span data-ttu-id="8d5bd-784">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="8d5bd-784">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8d5bd-785">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8d5bd-785">Az.RecoveryServices</span></span>
* <span data-ttu-id="8d5bd-786">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="8d5bd-786">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="8d5bd-787">1.2.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="8d5bd-787">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8d5bd-788">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8d5bd-788">Az.Accounts</span></span>
* <span data-ttu-id="8d5bd-789">Lägga till interaktiv autentisering och autentisering med användarnamn/lösenord för endast Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="8d5bd-789">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="8d5bd-790">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="8d5bd-790">Update incorrect online help URLs</span></span>
* <span data-ttu-id="8d5bd-791">Lägga till varningsmeddelande i PS Core för Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="8d5bd-791">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="8d5bd-792">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="8d5bd-792">Az.Aks</span></span>
* <span data-ttu-id="8d5bd-793">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="8d5bd-793">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8d5bd-794">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8d5bd-794">Az.Automation</span></span>
* <span data-ttu-id="8d5bd-795">Stöd för Python 2-runbookflöden har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d5bd-795">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="8d5bd-796">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="8d5bd-796">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="8d5bd-797">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="8d5bd-797">Az.Cdn</span></span>
* <span data-ttu-id="8d5bd-798">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="8d5bd-798">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d5bd-799">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d5bd-799">Az.Compute</span></span>
* <span data-ttu-id="8d5bd-800">Lägga till cmdleten Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="8d5bd-800">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="8d5bd-801">Lägga till TempDisk-parameter i Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8d5bd-801">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="8d5bd-802">Korrigera varningsmeddelande för New-AzVM</span><span class="sxs-lookup"><span data-stu-id="8d5bd-802">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="8d5bd-803">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8d5bd-803">Az.ContainerRegistry</span></span>
* <span data-ttu-id="8d5bd-804">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="8d5bd-804">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8d5bd-805">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8d5bd-805">Az.DataFactory</span></span>
* <span data-ttu-id="8d5bd-806">ADF .Net SDK-versionen har uppdaterats till 3.0.0</span><span class="sxs-lookup"><span data-stu-id="8d5bd-806">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8d5bd-807">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8d5bd-807">Az.DataLakeStore</span></span>
* <span data-ttu-id="8d5bd-808">Åtgärda problem med ADLS-slutpunkt vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="8d5bd-808">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="8d5bd-809">Mer information här: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="8d5bd-809">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="8d5bd-810">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="8d5bd-810">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8d5bd-811">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8d5bd-811">Az.IotHub</span></span>
* <span data-ttu-id="8d5bd-812">Lägga till kodningsformat i cmdleten Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-812">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8d5bd-813">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8d5bd-813">Az.KeyVault</span></span>
* <span data-ttu-id="8d5bd-814">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="8d5bd-814">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8d5bd-815">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d5bd-815">Az.Network</span></span>
* <span data-ttu-id="8d5bd-816">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="8d5bd-816">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="8d5bd-817">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d5bd-817">Az.Resources</span></span>
* <span data-ttu-id="8d5bd-818">Åtgärda felaktiga exempel i referensdokumentationen ”New-AzADAppCredential” och ”New-AzADSpCredential”</span><span class="sxs-lookup"><span data-stu-id="8d5bd-818">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="8d5bd-819">Åtgärda problem där sökvägen för parametern ”-TemplateFile” inte omvandlas innan cmdletarna för distribution i resursgruppen körs</span><span class="sxs-lookup"><span data-stu-id="8d5bd-819">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="8d5bd-820">Az.Resources: Korrigera dokumentationen om standardvärdet för New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="8d5bd-820">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="8d5bd-821">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="8d5bd-821">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="8d5bd-822">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="8d5bd-822">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="8d5bd-823">Åtgärda formateringsproblemet med objektet ”PSResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="8d5bd-823">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="8d5bd-824">Mer information här: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="8d5bd-824">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8d5bd-825">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8d5bd-825">Az.ServiceFabric</span></span>
* <span data-ttu-id="8d5bd-826">Återställ när ett certifikat läggs till i en Virtual Machine Scale Sets-modell men ett undantag genereras. Detta har gjorts för att åtgärda följande fel: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="8d5bd-826">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="8d5bd-827">Korrigera några felmeddelanden.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-827">Fix some error messages.</span></span>
* <span data-ttu-id="8d5bd-828">Korrigering av skapande av kluster med ARM-mall som är standard för New-AzServiceFabriCluster som inte fungerade med migrering till Az.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-828">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="8d5bd-829">Korrigering av tilläggning av kluster/programcertifikat så att endast VM Scale Sets som motsvarar klustret läggs till genom att kontrollera ID för klustret i tillägget.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-829">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="8d5bd-830">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="8d5bd-830">Az.SignalR</span></span>
* <span data-ttu-id="8d5bd-831">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="8d5bd-831">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="8d5bd-832">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d5bd-832">Az.Sql</span></span>
* <span data-ttu-id="8d5bd-833">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="8d5bd-833">Update incorrect online help URLs</span></span>
* <span data-ttu-id="8d5bd-834">Uppdaterad parameterbeskrivning för LicenseType-parameter med möjliga värden</span><span class="sxs-lookup"><span data-stu-id="8d5bd-834">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="8d5bd-835">Korrigering för att uppdatera hanterad instansidentitet som inte fungerar när det är den enda uppdaterade egenskapen</span><span class="sxs-lookup"><span data-stu-id="8d5bd-835">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="8d5bd-836">Stöd för anpassad sortering på hanterad instans</span><span class="sxs-lookup"><span data-stu-id="8d5bd-836">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8d5bd-837">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8d5bd-837">Az.Storage</span></span>
* <span data-ttu-id="8d5bd-838">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="8d5bd-838">Update incorrect online help URLs</span></span>
* <span data-ttu-id="8d5bd-839">Tillhandahåll detaljerat felmeddelande när en användare försöker hämta/konfigurera klassisk loggning/mått på ett Premium Storage-konto eftersom Premium Storage-kontot inte har stöd för klassisk loggning/mått.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-839">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="8d5bd-840">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="8d5bd-840">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="8d5bd-841">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="8d5bd-841">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="8d5bd-842">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="8d5bd-842">Az.TrafficManager</span></span>
* <span data-ttu-id="8d5bd-843">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="8d5bd-843">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8d5bd-844">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8d5bd-844">Az.Websites</span></span>
* <span data-ttu-id="8d5bd-845">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="8d5bd-845">Update incorrect online help URLs</span></span>
* <span data-ttu-id="8d5bd-846">Korrigerar ”New-AzWebAppSSLBinding” så att certifikatet laddas upp till rätt resursgrupp och plats om appen finns i en ASE.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-846">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="8d5bd-847">Korrigerar ”New-AzWebAppSSLBinding” så att taggarna inte skrivs över på en bindning av ett SSL-certifikat till en app</span><span class="sxs-lookup"><span data-stu-id="8d5bd-847">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="8d5bd-848">1.1.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="8d5bd-848">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8d5bd-849">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8d5bd-849">Az.Accounts</span></span>
* <span data-ttu-id="8d5bd-850">Lade till omfattningen ”Lokal” till Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="8d5bd-850">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d5bd-851">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d5bd-851">Az.Compute</span></span>
* <span data-ttu-id="8d5bd-852">Namn är nu valfritt i ID-parametern för Restart/Start/Stop/Remove/Set-AzVM och Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="8d5bd-852">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="8d5bd-853">Uppdaterade beskrivningen av ID i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="8d5bd-853">Updated the description of ID in help files</span></span>
* <span data-ttu-id="8d5bd-854">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8d5bd-854">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8d5bd-855">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8d5bd-855">Az.DataLakeStore</span></span>
* <span data-ttu-id="8d5bd-856">Uppdatera sdk-versionen av dataplanet till 1.1.14 för SDK-korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-856">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="8d5bd-857">Korrigerade hanteringen av negativ accesstime och modificationtime för getfilestatus och liststatus; korrigera asynkront annulleringstoken</span><span class="sxs-lookup"><span data-stu-id="8d5bd-857">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="8d5bd-858">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="8d5bd-858">Az.EventGrid</span></span>
* <span data-ttu-id="8d5bd-859">Uppdaterat för användning av API-versionen 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-859">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="8d5bd-860">Uppdaterade följande cmdletar för att stödja nytt scenario i API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="8d5bd-860">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="8d5bd-861">New-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="8d5bd-861">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="8d5bd-862">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="8d5bd-862">Event Time-To-Live,</span></span>
        - <span data-ttu-id="8d5bd-863">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="8d5bd-863">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="8d5bd-864">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-864">Dead letter endpoint.</span></span>
    - <span data-ttu-id="8d5bd-865">Update-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="8d5bd-865">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="8d5bd-866">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="8d5bd-866">Event Time-To-Live,</span></span>
        - <span data-ttu-id="8d5bd-867">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="8d5bd-867">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="8d5bd-868">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-868">Dead letter endpoint.</span></span>
* <span data-ttu-id="8d5bd-869">Lade till nya enum-värden (storageQueue och hybridConnection) för alternativet EndpointType i cmdletarna New-AzureRmEventGridSubscription och Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-869">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="8d5bd-870">Visa varningsmeddelanden om skapande eller uppdatering av händelseprenumerationen förväntas medföra manuell åtgärd från användaren.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-870">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8d5bd-871">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8d5bd-871">Az.IotHub</span></span>
* <span data-ttu-id="8d5bd-872">Har uppdaterats till den senaste versionen av SDK:n lotHub</span><span class="sxs-lookup"><span data-stu-id="8d5bd-872">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="8d5bd-873">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="8d5bd-873">Az.LogicApp</span></span>
* <span data-ttu-id="8d5bd-874">Get-AzLogicApp visar en lista över alla som inte har angivet namn</span><span class="sxs-lookup"><span data-stu-id="8d5bd-874">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="8d5bd-875">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d5bd-875">Az.Resources</span></span>
* <span data-ttu-id="8d5bd-876">Åtgärdade problem med parameteruppsättningen när parametrarna -ODataQuery och -ResourceId anges för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="8d5bd-876">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="8d5bd-877">Mer information här: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="8d5bd-877">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="8d5bd-878">Åtgärdade hantering av parametern -Custom i New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8d5bd-878">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="8d5bd-879">Korrigerade stavfel i New-AzDeployment-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="8d5bd-879">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="8d5bd-880">Gjorde parametern -MailNickname obligatorisk för New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="8d5bd-880">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="8d5bd-881">Mer information här: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="8d5bd-881">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="8d5bd-882">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="8d5bd-882">Az.SignalR</span></span>
* <span data-ttu-id="8d5bd-883">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8d5bd-883">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="8d5bd-884">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d5bd-884">Az.Sql</span></span>
* <span data-ttu-id="8d5bd-885">Konverterade lagringshanteringsklientens beroende av den normala SDK-implementeringen.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-885">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8d5bd-886">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8d5bd-886">Az.Storage</span></span>
* <span data-ttu-id="8d5bd-887">Angav StorageAccountName för lagringskontext som det verkliga namnet på lagringskontot när det skapas med Sas Token, OAuth eller Anonymous</span><span class="sxs-lookup"><span data-stu-id="8d5bd-887">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="8d5bd-888">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="8d5bd-888">New-AzStorageContext</span></span>
* <span data-ttu-id="8d5bd-889">Skapade Sas Token för Blob Snapshot-objekt med parametern -FullUri, åtgärdade den returnerade URI:n så att den blir URI för ögonblicksbild</span><span class="sxs-lookup"><span data-stu-id="8d5bd-889">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="8d5bd-890">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="8d5bd-890">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8d5bd-891">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8d5bd-891">Az.Websites</span></span>
* <span data-ttu-id="8d5bd-892">Åtgärdade en bugg i datumparsningen i Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="8d5bd-892">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="8d5bd-893">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8d5bd-893">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="8d5bd-894">1.0.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="8d5bd-894">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="8d5bd-895">Allmänt</span><span class="sxs-lookup"><span data-stu-id="8d5bd-895">General</span></span>

- <span data-ttu-id="8d5bd-896">Allmän tillgänglighet för Az-modulen</span><span class="sxs-lookup"><span data-stu-id="8d5bd-896">General Availability of Az Module</span></span>
- <span data-ttu-id="8d5bd-897">Onlinehjälp för varje modul</span><span class="sxs-lookup"><span data-stu-id="8d5bd-897">Online help for each module</span></span>
- <span data-ttu-id="8d5bd-898">Mer information och en översikt finns på [Az-informationssidan](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="8d5bd-898">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="8d5bd-899">Information om hur du migrerar från AzureRM finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8d5bd-899">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="8d5bd-900">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8d5bd-900">Az.Accounts</span></span>
- <span data-ttu-id="8d5bd-901">Har ändrats från Az.Profile</span><span class="sxs-lookup"><span data-stu-id="8d5bd-901">Changed from Az.Profile</span></span>
- <span data-ttu-id="8d5bd-902">Fasta tabellformat för profil- och kontexttyper</span><span class="sxs-lookup"><span data-stu-id="8d5bd-902">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="8d5bd-903">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8d5bd-903">Az.ApiManagement</span></span>
- <span data-ttu-id="8d5bd-904">Korrigeringar för #7002</span><span class="sxs-lookup"><span data-stu-id="8d5bd-904">Fixes for #7002</span></span>
- <span data-ttu-id="8d5bd-905">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8d5bd-905">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="8d5bd-906">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="8d5bd-906">Az.Batch</span></span>
- <span data-ttu-id="8d5bd-907">Lade till möjligheten att se vilken version av Azure Batch Node Agent som körs på var och en av de virtuella datorerna i en pool, via den nya egenskapen `NodeAgentInformation` på `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-907">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="8d5bd-908">Standarden `Caching` för `PSDataDisk` är nu `ReadWrite` i stället för `None`.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-908">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="8d5bd-909">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8d5bd-909">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="8d5bd-910">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="8d5bd-910">Az.Billing</span></span>
- <span data-ttu-id="8d5bd-911">Kombinerar cmdletarna för fakturering, förbrukning och UsageAggregates. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8d5bd-911">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="8d5bd-912">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="8d5bd-912">Az.CognitivServices</span></span>
- <span data-ttu-id="8d5bd-913">Lade till kompletterare för SkuName och Typem som är tillgängliga i New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="8d5bd-913">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="8d5bd-914">Tog bort parameteruppsättningen GetSkusWithAccountParamSetName från Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="8d5bd-914">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="8d5bd-915">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="8d5bd-915">Az.ContainerInstance</span></span>
- <span data-ttu-id="8d5bd-916">Stöd för ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="8d5bd-916">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="8d5bd-917">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="8d5bd-917">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="8d5bd-918">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8d5bd-918">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="8d5bd-919">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8d5bd-919">Az.DataLakeStore</span></span>
- <span data-ttu-id="8d5bd-920">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8d5bd-920">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="8d5bd-921">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8d5bd-921">Az.Monitor</span></span>
- <span data-ttu-id="8d5bd-922">Döpte om Az.Insights till Az.Monitor och andra mindre icke-bakåtkompatibla ändringar. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8d5bd-922">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="8d5bd-923">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8d5bd-923">Az.KeyVault</span></span>
- <span data-ttu-id="8d5bd-924">Tog bort den inaktuella egenskapen PurgeDisabled från utdatatyper</span><span class="sxs-lookup"><span data-stu-id="8d5bd-924">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="8d5bd-925">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="8d5bd-925">Az.MachineLearning</span></span>
- <span data-ttu-id="8d5bd-926">Inkluderade cmdletarna från modulen Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="8d5bd-926">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="8d5bd-927">Az.Media</span><span class="sxs-lookup"><span data-stu-id="8d5bd-927">Az.Media</span></span>
- <span data-ttu-id="8d5bd-928">Tog bort inaktuella -Tags-alias från New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="8d5bd-928">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="8d5bd-929">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d5bd-929">Az.Network</span></span>
<span data-ttu-id="8d5bd-930">Stöd har lagts till för konfiguration av RewriteRuleSets i Application Gateway</span><span class="sxs-lookup"><span data-stu-id="8d5bd-930">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="8d5bd-931">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="8d5bd-931">New cmdlets added:</span></span>
        - <span data-ttu-id="8d5bd-932">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8d5bd-932">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="8d5bd-933">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8d5bd-933">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="8d5bd-934">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8d5bd-934">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="8d5bd-935">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8d5bd-935">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="8d5bd-936">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8d5bd-936">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="8d5bd-937">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="8d5bd-937">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="8d5bd-938">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="8d5bd-938">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="8d5bd-939">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="8d5bd-939">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="8d5bd-940">Cmdletar har uppdaterats med den valfria parametern -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8d5bd-940">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="8d5bd-941">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8d5bd-941">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="8d5bd-942">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="8d5bd-942">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="8d5bd-943">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="8d5bd-943">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="8d5bd-944">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8d5bd-944">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="8d5bd-945">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="8d5bd-945">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="8d5bd-946">New-AzureRmApplicationGatewayUrlPathMapConfig har lagt till KeyVault-stöd för Application Gateway med Identity.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-946">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="8d5bd-947">Cmdletar har uppdaterats med den valfria parametern -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="8d5bd-947">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="8d5bd-948">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8d5bd-948">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="8d5bd-949">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8d5bd-949">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="8d5bd-950">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8d5bd-950">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="8d5bd-951">Cmdleten New-AzApplicationGateway har uppdaterats med den valfria parametern -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="8d5bd-951">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="8d5bd-952">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8d5bd-952">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="8d5bd-953">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8d5bd-953">Az.OperationalInsights</span></span>
- <span data-ttu-id="8d5bd-954">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8d5bd-954">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="8d5bd-955">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="8d5bd-955">Az.Profile</span></span>
- <span data-ttu-id="8d5bd-956">Modulnamnet har ändrats till Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8d5bd-956">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="8d5bd-957">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8d5bd-957">Az.RecoveryServices</span></span>
- <span data-ttu-id="8d5bd-958">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8d5bd-958">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="8d5bd-959">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d5bd-959">Az.Resources</span></span>
- <span data-ttu-id="8d5bd-960">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8d5bd-960">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="8d5bd-961">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8d5bd-961">Az.ServiceFabric</span></span>
- <span data-ttu-id="8d5bd-962">Stöd för specificering av certifikat efter eget namn och tumavtryck</span><span class="sxs-lookup"><span data-stu-id="8d5bd-962">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="8d5bd-963">Information om fler icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8d5bd-963">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="8d5bd-964">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="8d5bd-964">Az.SIgnalR</span></span>
- <span data-ttu-id="8d5bd-965">Allmän tillgänglighet för PowerShell-cmdletar för SIgnalR</span><span class="sxs-lookup"><span data-stu-id="8d5bd-965">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="8d5bd-966">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d5bd-966">Az.Sql</span></span>
- <span data-ttu-id="8d5bd-967">Lade till de nya identifieringstyperna Data_Exfiltration och Unsafe_Action i Threat Detection-cmdletar</span><span class="sxs-lookup"><span data-stu-id="8d5bd-967">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="8d5bd-968">Uppdaterade dokumentationsexempel för Sql Auditing-cmdletar</span><span class="sxs-lookup"><span data-stu-id="8d5bd-968">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="8d5bd-969">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8d5bd-969">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="8d5bd-970">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8d5bd-970">Az.Storage</span></span>
- <span data-ttu-id="8d5bd-971">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8d5bd-971">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="8d5bd-972">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8d5bd-972">Az.Websites</span></span>
- <span data-ttu-id="8d5bd-973">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8d5bd-973">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="8d5bd-974">0.7.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="8d5bd-974">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="8d5bd-975">Allmänt</span><span class="sxs-lookup"><span data-stu-id="8d5bd-975">General</span></span>

* <span data-ttu-id="8d5bd-976">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="8d5bd-976">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="8d5bd-977">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d5bd-977">Az.Compute</span></span>

* <span data-ttu-id="8d5bd-978">Lade till stöd för UltraSSD och Galleriavbildningar i de enkla parameteruppsättningarna för `New-AzVm(ss)`-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-978">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="8d5bd-979">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8d5bd-979">Az.DataLakeStore</span></span>

* <span data-ttu-id="8d5bd-980">Åtgärdade avslutande snedstreck i domänen för adls-konto</span><span class="sxs-lookup"><span data-stu-id="8d5bd-980">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="8d5bd-981">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="8d5bd-981">Az.FrontDoor</span></span>

* <span data-ttu-id="8d5bd-982">Brutna länkar korrigerades</span><span class="sxs-lookup"><span data-stu-id="8d5bd-982">Fixed some broken links</span></span>
    - <span data-ttu-id="8d5bd-983">I artiklarna New-AzureRmFrontDoor och Set-AzureRmFrontDoor artiklar korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-983">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="8d5bd-984">I artikeln New-AzureRmFrontDoorManagedRuleObject korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-984">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="8d5bd-985">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8d5bd-985">Az.RecoveryServices</span></span>

* <span data-ttu-id="8d5bd-986">Lade till valideringar på klientsidan för Azure-filresurs med återställningsåtgärder.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-986">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="8d5bd-987">Gjorde storageAccountName och storageAccountResourceGroupName valfritt för afs-återställning.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-987">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="8d5bd-988">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d5bd-988">Az.Resources</span></span>

* <span data-ttu-id="8d5bd-989">Korrigering för https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="8d5bd-989">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="8d5bd-990">Uppdaterade Get-AzureRmRoleAssignment så att prenumerationsomfattningen används om den anges vid begäran om klassiska administratörer.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-990">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="8d5bd-991">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d5bd-991">Az.Sql</span></span>

* <span data-ttu-id="8d5bd-992">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="8d5bd-992">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="8d5bd-993">Korrigerade ett problem med Get-AzureRmSqlDatabaseVulnerabilityAssessment med DotNet-kärna</span><span class="sxs-lookup"><span data-stu-id="8d5bd-993">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="8d5bd-994">Ändrade dokumentationen för hjälpmeddelanden som rör SQL Auditing-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-994">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="8d5bd-995">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8d5bd-995">Az.Storage</span></span>

* <span data-ttu-id="8d5bd-996">Lade till -EnableHierarchicalNamespace i New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8d5bd-996">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="8d5bd-997">Åtgärdade problemet med att cmdleten Copy File inte kunde återanvända källkontexten på målet om inte -DestContext angetts</span><span class="sxs-lookup"><span data-stu-id="8d5bd-997">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="8d5bd-998">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="8d5bd-998">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="8d5bd-999">Stöd för statisk webbplatskonfiguration</span><span class="sxs-lookup"><span data-stu-id="8d5bd-999">Support Static Website configuration</span></span>
    - <span data-ttu-id="8d5bd-1000">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1000">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="8d5bd-1001">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1001">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="8d5bd-1002">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1002">Az.Websites</span></span>

* <span data-ttu-id="8d5bd-1003">Set-AzureRmWebApp och Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1003">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="8d5bd-1004">Ny parameter (-AzureStoragePath) har lagts till för att ange att Azure Storage-sökvägar ska monteras i containerappar i Windows och Linux.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1004">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="8d5bd-1005">Använder utdata från den nya cmdleten New-AzureRmWebAppAzureStoragePath som en parameter för att ange sökvägar för Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1005">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="8d5bd-1006">0.6.1 – november 2018</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1006">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="8d5bd-1007">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1007">Az.ApiManagement</span></span>
* <span data-ttu-id="8d5bd-1008">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1008">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="8d5bd-1009">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1009">Az.Automation</span></span>
* <span data-ttu-id="8d5bd-1010">Swagger baserade Azure Automation-cmdletar</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1010">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="8d5bd-1011">Cmdletar för Uppdateringshantering har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1011">Added Update Management cmdlets</span></span>
* <span data-ttu-id="8d5bd-1012">Cmdletar för källkontroll har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1012">Added Source Control cmdlets</span></span>
* <span data-ttu-id="8d5bd-1013">Remove-AzureRmAutomationHybridWorkerGroup-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1013">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="8d5bd-1014">Kommandot för DSC-registreringsnod har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1014">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="8d5bd-1015">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1015">Az.Compute</span></span>
* <span data-ttu-id="8d5bd-1016">Problem med SystemAssigned-identitet har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1016">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="8d5bd-1017">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1017">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="8d5bd-1018">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1018">Az.ContainerInstance</span></span>
* <span data-ttu-id="8d5bd-1019">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1019">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="8d5bd-1020">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1020">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="8d5bd-1021">uppdatera exempelbeskrivningen för marketplace-cmdletar</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1021">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="8d5bd-1022">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1022">Az.Network</span></span>
* <span data-ttu-id="8d5bd-1023">Cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomErreller Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1023">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="8d5bd-1024">ICMP tillbaka till stöd för Azure Firewall-nätverksprotokoll har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1024">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="8d5bd-1025">Uppdatera cmdlet Test-AzureRmNetworkWatcherConnectivity, lägga till verifiering av mål-id, adress och port.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1025">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="8d5bd-1026">Åtgärda problem med minnesanvändning i VirtualNetwork-karta</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1026">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="8d5bd-1027">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1027">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="8d5bd-1028">Åtgärda för att ändra principen för en skyddad fildelning.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1028">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="8d5bd-1029">Tidszonsprincipen har konverterats till versaler.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1029">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="8d5bd-1030">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1030">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="8d5bd-1031">Exempel i New-AzureRmRecoveryServicesAsrProtectableItem har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1031">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="8d5bd-1032">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1032">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="8d5bd-1033">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1033">Az.Relay</span></span>
* <span data-ttu-id="8d5bd-1034">Valfri parameter -KeyValue till New-AzureRmRelayKey cmdlet har lagts till, vilket gör det möjligt för användare att tillhandahålla KeyValue.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1034">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="8d5bd-1035">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1035">Az.Resources</span></span>
* <span data-ttu-id="8d5bd-1036">Uppdatera hjälpdokumentation för resursidentitet kopplad till parametrar i `New-AzureRmPolicyAssignment` och `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1036">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="8d5bd-1037">Lägg till ett exempel för New-AzureRmPolicyDefinition som använder -Metadata</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1037">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="8d5bd-1038">Korrigera så att skiftläge behålls i taggnycklar i NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1038">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="8d5bd-1039">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1039">Az.ServiceFabric</span></span>
* <span data-ttu-id="8d5bd-1040">Lägg till utfasningsmeddelanden för kommande icke-kompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1040">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="8d5bd-1041">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1041">Az.Sql</span></span>
* <span data-ttu-id="8d5bd-1042">Nya cmdletar för CRUD-åtgärder på Azure Sql Database-hanterad instans och Azure Sql-hanterad databas</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1042">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="8d5bd-1043">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1043">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="8d5bd-1044">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1044">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="8d5bd-1045">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1045">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="8d5bd-1046">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1046">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="8d5bd-1047">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1047">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="8d5bd-1048">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1048">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="8d5bd-1049">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1049">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="8d5bd-1050">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1050">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="8d5bd-1051">Hantering av utökad granskningsprincip på en server eller en databas har aktiverats.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1051">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="8d5bd-1052">Ny parameter (PredicateExpression) har lagts till för att aktivera filtrering av granskningsloggar.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1052">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="8d5bd-1053">Cmdletar har ändrats så att de använder SQL-klienter i stället för äldre klienter.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1053">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="8d5bd-1054">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1054">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="8d5bd-1055">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1055">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="8d5bd-1056">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1056">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="8d5bd-1057">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1057">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="8d5bd-1058">Problem med att använda Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings med lagringskontots namnparameter har korrigerats</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1058">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="8d5bd-1059">0.5.0 – november 2018</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1059">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="8d5bd-1060">Allmänt</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1060">General</span></span>
* <span data-ttu-id="8d5bd-1061">Lade till resurskompletterare till många kärn-cmdletar – dessa gör att du kan stega genom befintliga resursnamn med TABB vid interaktiva anrop till cmdletar</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1061">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="8d5bd-1062">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1062">Az.Profile</span></span>
* <span data-ttu-id="8d5bd-1063">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1063">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="8d5bd-1064">Bytte namn på parametern TenantId i cmdleten Connect-AzAccount till Tenant och lade till ett alias för TenantId</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1064">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="8d5bd-1065">Uppdaterade TenantId-beskrivningen för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1065">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="8d5bd-1066">Åtgärda felmeddelande för misslyckad inloggning när du tillhandahåller klientdomän</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1066">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="8d5bd-1067">Åtgärda problem med att kontextnamn hamnar i konflikt för konton utan prenumerationer i klientorganisationen</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1067">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="8d5bd-1068">Åtgärda problem med DataLake-slutpunkter vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1068">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="8d5bd-1069">Åtgärdade problem med att Disconnect-AzAccount kastades om den inte anslöts</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1069">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="8d5bd-1070">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1070">Az.CognitiveServices</span></span>
* <span data-ttu-id="8d5bd-1071">Lade till åtgärden Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1071">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d5bd-1072">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1072">Az.Compute</span></span>
* <span data-ttu-id="8d5bd-1073">Lade till cmdletarna Add-AzVmssVMDataDisk och Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1073">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="8d5bd-1074">Get-AzVMImage visar AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1074">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="8d5bd-1075">Åtgärdade att värdena för alternativen SetAzVMChefExtension -BootstrapOptions och -JsonAttribute inte angavs i json-format.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1075">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8d5bd-1076">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1076">Az.DataLakeStore</span></span>
* <span data-ttu-id="8d5bd-1077">Uppdatera DataLake-paketet till 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1077">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="8d5bd-1078">Lägg till standardsamtidighet för flertrådade åtgärder.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1078">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="8d5bd-1079">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1079">Az.Insights</span></span>
* <span data-ttu-id="8d5bd-1080">Åtgärdade problem #7267 (autoskalningsområde)</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1080">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="8d5bd-1081">Problem med att uppräknade parametrar inte ställdes in ordentligt när du skapade en ny autoskalningsregel (de ställdes alltid in med standardvärdet).</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1081">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="8d5bd-1082">Åtgärdade problem #7513 [Insights] Set-AzDiagnosticSetting kräver uttrycklig specifikation av kategorier när inställningar skapas</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1082">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="8d5bd-1083">Nu kräver inte cmdleten uttrycklig anvisning av kategorierna för att aktiveras under skapande, d.v.s. den fungerar enligt beskrivning</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1083">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8d5bd-1084">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1084">Az.Network</span></span>
* <span data-ttu-id="8d5bd-1085">PeeringType ändrades till en obligatorisk parameter för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1085">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="8d5bd-1086">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1086">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="8d5bd-1087">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1087">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="8d5bd-1088">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1088">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="8d5bd-1089">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1089">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="8d5bd-1090">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1090">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="8d5bd-1091">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1091">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="8d5bd-1092">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1092">Az.PolicyInsights</span></span>
* <span data-ttu-id="8d5bd-1093">Cmdletar för principreparation har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1093">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="8d5bd-1094">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1094">Az.Resources</span></span>
* <span data-ttu-id="8d5bd-1095">Korrigering för https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1095">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="8d5bd-1096">Tillåt att resurser listas med parametern -ResourceId för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1096">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="8d5bd-1097">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1097">Az.ServiceBus</span></span>
* <span data-ttu-id="8d5bd-1098">Skrivskyddad MigrationState-egenskap har lagts till i PSServiceBusMigrationConfigurationAttributes, som hjälper till att hålla koll på migreringstillståndet.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1098">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8d5bd-1099">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1099">Az.ServiceFabric</span></span>
* <span data-ttu-id="8d5bd-1100">Åtgärda att lägga till certifikat till Linux-Vmss.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1100">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="8d5bd-1101">Åtgärdade Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1101">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="8d5bd-1102">Använd rätt tumavtryck från nya certifikat (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1102">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="8d5bd-1103">Visa undantag korrekt (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1103">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="8d5bd-1104">Åtgärdade Update-AzServiceFabricDurability så att klusterkonfigurationen uppdateras innan Vmss-åtgärden CreateOrUpdate påbörjas.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1104">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="8d5bd-1105">0.4.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1105">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="8d5bd-1106">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1106">Az.Profile</span></span>
* <span data-ttu-id="8d5bd-1107">Åtgärdade problemet med Get-AzSubscription i CloudShell</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1107">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="8d5bd-1108">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1108">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d5bd-1109">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1109">Az.Compute</span></span>
* <span data-ttu-id="8d5bd-1110">Nya storlekar lades till i listan över godkända VM-storlekar för vilka accelererat nätverk kommer att aktiveras vid användning av den enkla parameteruppsättningen för New-AzVm</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1110">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="8d5bd-1111">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1111">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8d5bd-1112">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1112">Az.DataLakeStore</span></span>
* <span data-ttu-id="8d5bd-1113">Lägger till stöd för regler för virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1113">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="8d5bd-1114">Get-AzDataLakeStoreVirtualNetworkRule: Hämtar eller listar regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1114">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="8d5bd-1115">Add-AzDataLakeStoreVirtualNetworkRule: Lägger till en regel för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1115">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="8d5bd-1116">Set-AzDataLakeStoreVirtualNetworkRule: Ändrar den angivna regeln för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1116">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="8d5bd-1117">Remove-AzDataLakeStoreVirtualNetworkRule: Tar bort en regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1117">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8d5bd-1118">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1118">Az.Network</span></span>
* <span data-ttu-id="8d5bd-1119">Skicka protokollvärdet till serverdelen för att uppdatera cmdleten Test-AzNetworkWatcherConnectivity.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1119">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="8d5bd-1120">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1120">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8d5bd-1121">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1121">Az.Resources</span></span>
* <span data-ttu-id="8d5bd-1122">Åtgärdade problem där Get-AzRoleDefinition genererar ett oläsligt undantag (när standardprofilen inte innehåller någon prenumeration och ingen omfattning har angetts) genom att lägga till ett beskrivande undantag i scenariot.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1122">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="8d5bd-1123">Ställ in ”RoleDefinitionNameParameterSet” som standardparameteruppsättning.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1123">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="8d5bd-1124">0.3.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1124">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="8d5bd-1125">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1125">Azure.Storage</span></span>
* <span data-ttu-id="8d5bd-1126">Åtgärda fel där Kopiera blob/fil inte kopierar metadata när målplatsen har ett problem med metadata</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1126">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="8d5bd-1127">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1127">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="8d5bd-1128">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1128">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="8d5bd-1129">Stöd för att hämta användningsinformation om en Storage-resurs för en specifik plats och för att lägga till ett varningsmeddelande för att hämta användningsinformation om en global Storage-resurs är inaktuellt.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1129">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="8d5bd-1130">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1130">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="8d5bd-1131">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1131">Az.CognitiveServices</span></span>
* <span data-ttu-id="8d5bd-1132">Stöd för Get-AzCognitiveServicesAccountSkus utan ett befintligt konto.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1132">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d5bd-1133">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1133">Az.Compute</span></span>
* <span data-ttu-id="8d5bd-1134">Åtgärdade fel där Get-AzVM -ResourceGroupName <rg> returnerar fler än 50 resultat om det behövs</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1134">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="8d5bd-1135">Lade till ett exempel för SimpleParameterSet i hjälpen för cmdleten New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1135">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="8d5bd-1136">Ett stavfel i förloppsmeddelandet för Azure Disk Encryption har korrigerats</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1136">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="8d5bd-1137">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1137">Az.DataFactoryV2</span></span>
* <span data-ttu-id="8d5bd-1138">ADF .Net SDK-versionen har uppdaterats till 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1138">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8d5bd-1139">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1139">Az.Network</span></span>
* <span data-ttu-id="8d5bd-1140">Funktionalitet för NetworkProfile har lagts till.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1140">Added NetworkProfile functionality.</span></span> <span data-ttu-id="8d5bd-1141">nya cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1141">new cmdlets added</span></span>
    - <span data-ttu-id="8d5bd-1142">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1142">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="8d5bd-1143">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1143">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="8d5bd-1144">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1144">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="8d5bd-1145">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1145">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="8d5bd-1146">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1146">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="8d5bd-1147">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1147">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="8d5bd-1148">Länk för tjänstassociering på modell för undernät har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1148">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="8d5bd-1149">Cmdletarna New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap och Remove-AzVirtualNetworkTap har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1149">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="8d5bd-1150">Cmdletarna Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig och Remove-AzNEtworkInterfaceTapConfig har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1150">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="8d5bd-1151">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1151">Az.RedisCache</span></span>
* <span data-ttu-id="8d5bd-1152">Tillåt att alla strängar används som storleksparametrar framöver.</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1152">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="8d5bd-1153">Lägg till P5 i popup-fönstret PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1153">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="8d5bd-1154">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1154">Az.Resources</span></span>
* <span data-ttu-id="8d5bd-1155">Parametern -Mode som saknades i Set-AzPolicyDefinition har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1155">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="8d5bd-1156">Åtgärdade buggen för cmdleten Get-AzProviderOperation för åtgärder med ursprung som innehåller användare</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1156">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="8d5bd-1157">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1157">Az.Sql</span></span>
* <span data-ttu-id="8d5bd-1158">Ett problem där vissa cmdletar för säkerhetskopiering inte kunde identifiera den aktuella azure-prenumerationen har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1158">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8d5bd-1159">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1159">Az.Websites</span></span>
* <span data-ttu-id="8d5bd-1160">Ny cmdlet: Get-AzWebAppContainerContinuousDeploymentUrl – Hämtar webhook-URL:en för kontinuerlig distribution av container</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1160">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="8d5bd-1161">Nya cmdletar: New-AzWebAppContainerPSSession och Enter-WebAppContainerPSSession – Startar en PowerShell-fjärrsession i en containerapp för windows</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1161">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="8d5bd-1162">0.2.0 – september 2018</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1162">0.2.0 - September 2018</span></span>
 <span data-ttu-id="8d5bd-1163">Första versionen</span><span class="sxs-lookup"><span data-stu-id="8d5bd-1163">Initial Release</span></span>