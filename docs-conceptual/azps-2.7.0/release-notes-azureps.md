---
ms.openlocfilehash: 96e6d7bc0cc29adc1c0e49ba344d27349454c214
ms.sourcegitcommit: 92722d603b60dc769660e7517da60110133d9959
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/24/2019
ms.locfileid: "71226447"
---
## <a name="270---september-2019"></a><span data-ttu-id="e9175-101">2.7.0 – september 2019</span><span class="sxs-lookup"><span data-stu-id="e9175-101">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="e9175-102">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e9175-102">Az.ApiManagement</span></span>
* <span data-ttu-id="e9175-103">Uppdatera ”-Format”-parameterbeskrivningen i ”Set-AzApiManagementPolicy”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="e9175-103">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="e9175-104">Referenser för den föråldrade cmdleten ”Update-AzApiManagementDeployment” har tagits bort från referensdokumentationen.</span><span class="sxs-lookup"><span data-stu-id="e9175-104">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="e9175-105">Använd ”Set-AzApiManagement” i stället.</span><span class="sxs-lookup"><span data-stu-id="e9175-105">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e9175-106">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e9175-106">Az.Automation</span></span>
* <span data-ttu-id="e9175-107">Stavfel har korrigerats i exempel i referensdokumentationen för ”Register-AzAutomationDscNode”</span><span class="sxs-lookup"><span data-stu-id="e9175-107">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="e9175-108">Klargörande har lagts till om OS-begränsningar för Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="e9175-108">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="e9175-109">Null-referensundantag har korrigerats för -Wait-alternativet i Start-AzAutomationRunbook-cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e9175-109">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e9175-110">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e9175-110">Az.Compute</span></span>
* <span data-ttu-id="e9175-111">Lägg till UploadSizeInBytes-parameter till New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="e9175-111">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="e9175-112">Lägg till Incremental-parameter till New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="e9175-112">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="e9175-113">Lägg till en funktion för virtuella datorer med låg prioritet:</span><span class="sxs-lookup"><span data-stu-id="e9175-113">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="e9175-114">MaxPrice-, EvictionPolicy- och Priority-parametrar har lagts till i New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="e9175-114">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="e9175-115">MaxPrice-parametern har lagts till i New-AzVmssConfig-, Update-AzVM- och Update-AzVmss-cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="e9175-115">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="e9175-116">Åtgärda problem med VM-referenser för Get-AzAvailabilitySet-cmdleten när alla tillgänglighetsuppsättningar i prenumerationen visas.</span><span class="sxs-lookup"><span data-stu-id="e9175-116">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="e9175-117">Korrigera null-undantaget för Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="e9175-117">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="e9175-118">Korrigera VHD-metoden för sökning relativt till slut.</span><span class="sxs-lookup"><span data-stu-id="e9175-118">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="e9175-119">Åtgärda UltraSSD-problem för New-AzVM och Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="e9175-119">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e9175-120">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e9175-120">Az.DataFactory</span></span>
* <span data-ttu-id="e9175-121">Lägger till 3 nya kommandon för ADF V2 – Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription och Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="e9175-121">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="e9175-122">ADF .Net SDK har uppdaterats till 4.1.3</span><span class="sxs-lookup"><span data-stu-id="e9175-122">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="e9175-123">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="e9175-123">Az.HDInsight</span></span>
* <span data-ttu-id="e9175-124">Anrop för icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="e9175-124">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e9175-125">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e9175-125">Az.IotHub</span></span>
* <span data-ttu-id="e9175-126">Lägg till stöd för att anropa redundans för en IotHub till den geo-länkade katastrofåterställningsregionen.</span><span class="sxs-lookup"><span data-stu-id="e9175-126">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="e9175-127">Lägg till stöd för att hantera meddelandeberikning för en IotHub.</span><span class="sxs-lookup"><span data-stu-id="e9175-127">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="e9175-128">Nya cmdlet:ar är:</span><span class="sxs-lookup"><span data-stu-id="e9175-128">New cmdlets are:</span></span>
    - <span data-ttu-id="e9175-129">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="e9175-129">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="e9175-130">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="e9175-130">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="e9175-131">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="e9175-131">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="e9175-132">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="e9175-132">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e9175-133">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e9175-133">Az.Monitor</span></span>
* <span data-ttu-id="e9175-134">Pekar på den senaste Monitor SDK:n, dvs. 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="e9175-134">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="e9175-135">Lägger till bakåtkompatibla ändringar i Metrics-cmdletarna, dvs. enhetsuppräkningen stöder flera nya värden.</span><span class="sxs-lookup"><span data-stu-id="e9175-135">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="e9175-136">Detta är skrivskyddade cmdletar, så det förekommer inga ändringar i inmatningen för cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="e9175-136">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="e9175-137">API-versionen för **ActionGroups**-begäranden är nu **2019-06-01**. Tidigare var den **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="e9175-137">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="e9175-138">Test av scenarier har uppdaterats för att anpassas till den här ändringen.</span><span class="sxs-lookup"><span data-stu-id="e9175-138">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="e9175-139">Ett nytt obligatoriskt argument har lagts till för konstruktorerna för klasserna **EmailReceiver** och **WebhookReceiver** – ett booleskt värde med namnet **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="e9175-139">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="e9175-140">Värdet är för närvarande fast till **false** så att den här icke-bakåtkompatibla ändringen är dold från cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="e9175-140">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="e9175-141">**Obs!** Det här är en tillfällig ändring som måste verifieras av Alerts-teamet.</span><span class="sxs-lookup"><span data-stu-id="e9175-141">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="e9175-142">Ordningen på argumenten för konstruktorn för klassen **Source** (relaterad till klassen **ScheduledQueryRuleSource**) har ändrats från den tidigare SDK:n.</span><span class="sxs-lookup"><span data-stu-id="e9175-142">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="e9175-143">Den här ändringen krävde korrigering av två enhetstest: de kompilerades, men testerna skickades inte.</span><span class="sxs-lookup"><span data-stu-id="e9175-143">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="e9175-144">Ordningen på argumenten för konstruktorn för klassen **AlertingAction** (relaterad till klassen **ScheduledQueryRuleSource**) har ändrats från den tidigare SDK:n.</span><span class="sxs-lookup"><span data-stu-id="e9175-144">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="e9175-145">Den här ändringen krävde korrigering av två enhetstest: de kompilerades, men testerna skickades inte.</span><span class="sxs-lookup"><span data-stu-id="e9175-145">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="e9175-146">Stöd för kriterier för dynamiskt tröskelvärde för måttavisering v2</span><span class="sxs-lookup"><span data-stu-id="e9175-146">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="e9175-147">New-AzMetricAlertRuleV2Criteria: skapar nu även kriterier för dynamiskt tröskelvärde</span><span class="sxs-lookup"><span data-stu-id="e9175-147">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="e9175-148">Add-AzMetricAlertRuleV2: accepterar nu även kriterier för dynamiskt tröskelvärde</span><span class="sxs-lookup"><span data-stu-id="e9175-148">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="e9175-149">Förbättringar i schemalagd frågeregel (SQR)</span><span class="sxs-lookup"><span data-stu-id="e9175-149">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="e9175-150">Cmdletar accepterar ”Location”-parameter i båda formaten, antingen platsen (t.ex. eastus) eller platsens visningsnamn (t.ex. USA, östra)</span><span class="sxs-lookup"><span data-stu-id="e9175-150">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="e9175-151">”Enabled”-parametern illustreras korrekt i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="e9175-151">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="e9175-152">Exempel för den valfria parametern ”ActionGroup” har lagts till</span><span class="sxs-lookup"><span data-stu-id="e9175-152">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="e9175-153">Förbättrade hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="e9175-153">Overall improved help files</span></span>
* <span data-ttu-id="e9175-154">Åtgärda bugg då omfattningstypen fastställs för ”Set-AzActionRule”</span><span class="sxs-lookup"><span data-stu-id="e9175-154">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e9175-155">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e9175-155">Az.Network</span></span>
* <span data-ttu-id="e9175-156">Korrigera felaktigt exempel i referensdokumentationen för ”New-AzApplicationGateway”</span><span class="sxs-lookup"><span data-stu-id="e9175-156">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="e9175-157">Lägg till anmärkning i ”Get-AzNetworkWatcherPacketCapture”-referensdokumentationen om hämtning av alla egenskaper för en paketinsamling</span><span class="sxs-lookup"><span data-stu-id="e9175-157">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="e9175-158">Exempel har korrigerats i ”Test-AzNetworkWatcherIPFlow”-referensdokumentationen för korrekt uppräkning av nätverkskort</span><span class="sxs-lookup"><span data-stu-id="e9175-158">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="e9175-159">Förbättrad tolkning av molnundantag för att visa eventuell ytterligare information</span><span class="sxs-lookup"><span data-stu-id="e9175-159">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="e9175-160">Förbättrad tolkning av molnundantag för att hantera ytterligare en typ av SDK-undantag</span><span class="sxs-lookup"><span data-stu-id="e9175-160">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="e9175-161">Felaktig mappning av säkerhetsregelmodeller har korrigerats</span><span class="sxs-lookup"><span data-stu-id="e9175-161">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="e9175-162">Egenskaper har lagts till för nätverksgränssnittet för funktionen Privat IP</span><span class="sxs-lookup"><span data-stu-id="e9175-162">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="e9175-163">Egenskapen ”PrivateEndpoint” har lagts till som en typ av PSResourceId till PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="e9175-163">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="e9175-164">Egenskapen ”PrivateLinkConnectionProperties” har lagts till som en typ av PSIpConfigurationConnectivityInformation till PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e9175-164">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="e9175-165">Modellklassen PSIpConfigurationConnectivityInformation har lagts till</span><span class="sxs-lookup"><span data-stu-id="e9175-165">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="e9175-166">ApplicationRuleProtocolType ”mssql” har lagts till för Azure Firewall-resurs</span><span class="sxs-lookup"><span data-stu-id="e9175-166">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="e9175-167">MultiLink-stöd i virtuellt WAN</span><span class="sxs-lookup"><span data-stu-id="e9175-167">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="e9175-168">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="e9175-168">New cmdlets</span></span>
        - <span data-ttu-id="e9175-169">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="e9175-169">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="e9175-170">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="e9175-170">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="e9175-171">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="e9175-171">Updated cmdlet:</span></span>
        - <span data-ttu-id="e9175-172">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="e9175-172">New-VpnSite</span></span>
        - <span data-ttu-id="e9175-173">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="e9175-173">Update-VpnSite</span></span>
        - <span data-ttu-id="e9175-174">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="e9175-174">New-VpnConnection</span></span>
        - <span data-ttu-id="e9175-175">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="e9175-175">Update-VpnConnection</span></span>
* <span data-ttu-id="e9175-176">Dokument för vissa PowerShell-exempel har korrigerats så att Az-cmdletar används i stället för AzureRM-cmdletar</span><span class="sxs-lookup"><span data-stu-id="e9175-176">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e9175-177">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e9175-177">Az.RecoveryServices</span></span>
* <span data-ttu-id="e9175-178">Uppdatera AzureVMpolicy-objekt med ProtectedItemsCount-attribut</span><span class="sxs-lookup"><span data-stu-id="e9175-178">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="e9175-179">Ytterligare tester har lagts till för VM-princip och återställning av ursprungligt lagringskonto</span><span class="sxs-lookup"><span data-stu-id="e9175-179">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="e9175-180">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e9175-180">Az.Resources</span></span>
* <span data-ttu-id="e9175-181">Åtgärda fel där det inte gick att anropa New-AzRoleAssignment utan parametern Scope.</span><span class="sxs-lookup"><span data-stu-id="e9175-181">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e9175-182">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e9175-182">Az.ServiceFabric</span></span>
* <span data-ttu-id="e9175-183">Stavfel har korrigerats i exempel för ”Update-AzServiceFabricReliability”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="e9175-183">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="e9175-184">Lägger till nya cmdletar för att hantera program och tjänster:</span><span class="sxs-lookup"><span data-stu-id="e9175-184">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="e9175-185">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="e9175-185">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="e9175-186">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="e9175-186">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="e9175-187">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="e9175-187">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="e9175-188">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="e9175-188">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="e9175-189">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="e9175-189">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="e9175-190">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="e9175-190">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="e9175-191">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="e9175-191">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="e9175-192">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="e9175-192">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="e9175-193">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="e9175-193">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="e9175-194">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="e9175-194">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="e9175-195">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="e9175-195">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="e9175-196">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="e9175-196">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="e9175-197">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="e9175-197">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="e9175-198">Service Fabric SDK har uppgraderats till version 1.2.0 som använder Service Fabric-resursprovidern med API-version 2019-03-01.</span><span class="sxs-lookup"><span data-stu-id="e9175-198">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="e9175-199">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="e9175-199">Az.SignalR</span></span>
* <span data-ttu-id="e9175-200">Lägg till Update-, Restart-, CheckNameAvailability- och GetUsage-cmdletar</span><span class="sxs-lookup"><span data-stu-id="e9175-200">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="e9175-201">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e9175-201">Az.Sql</span></span>
* <span data-ttu-id="e9175-202">Uppdatera exempel i referensdokumentationen för ”Get-AzSqlElasticPool”</span><span class="sxs-lookup"><span data-stu-id="e9175-202">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="e9175-203">vCore-exempel för att skapa en elastisk pool (New-AzSqlElasticPool) har lagts till.</span><span class="sxs-lookup"><span data-stu-id="e9175-203">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="e9175-204">Ta bort verifieringen av EmailAddresses och kontrollen som bekräftar att EmailAdmins inte är falskt när EmailAddresses är tomt i Set-AzSqlServerAdvancedThreatProtectionPolicy och Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e9175-204">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="e9175-205">Server-/databasgranskningsinställningar kan tas bort när det finns flera diagnostikinställningar som aktiverar granskningskategorin.</span><span class="sxs-lookup"><span data-stu-id="e9175-205">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="e9175-206">Åtgärda verifiering av e-postadresser i flera Sql Vulnerability Assessment-cmdletar (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting och Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="e9175-206">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e9175-207">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e9175-207">Az.Storage</span></span>
* <span data-ttu-id="e9175-208">Exempel i referensdokumentationen för ”Get-AzStorageAccountKey” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="e9175-208">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="e9175-209">Vid upp- och nedladdning av en Azure-fil kan SMB-egenskaperna för källfilen (t.ex. filattribut, tidpunkten då filen skapades och tidpunkten för den senaste skrivningen) sparas i målfilen</span><span class="sxs-lookup"><span data-stu-id="e9175-209">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="e9175-210">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="e9175-210">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="e9175-211">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="e9175-211">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="e9175-212">Korrigera problem med uppladdningen av blockblob med egenskaper/metadata för ImmutabilityPolicy i containrar.</span><span class="sxs-lookup"><span data-stu-id="e9175-212">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="e9175-213">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="e9175-213">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="e9175-214">Stöd för hantering av Azure-filresurser med API för hanteringsplan</span><span class="sxs-lookup"><span data-stu-id="e9175-214">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="e9175-215">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="e9175-215">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="e9175-216">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="e9175-216">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="e9175-217">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="e9175-217">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="e9175-218">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="e9175-218">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e9175-219">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e9175-219">Az.Websites</span></span>
* <span data-ttu-id="e9175-220">Åtgärdar problemet där webapp-taggar togs bort när appen migrerades till nya ASP</span><span class="sxs-lookup"><span data-stu-id="e9175-220">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="e9175-221">Åtgärda Publish-AzureWebapp så att det fungerar i Linux och Windows</span><span class="sxs-lookup"><span data-stu-id="e9175-221">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="e9175-222">Uppdatera exempel i ”Get-AzWebAppPublishingProfile”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="e9175-222">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="e9175-223">2.6.0 – augusti 2019</span><span class="sxs-lookup"><span data-stu-id="e9175-223">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="e9175-224">Allmänt</span><span class="sxs-lookup"><span data-stu-id="e9175-224">General</span></span>
* <span data-ttu-id="e9175-225">Åtgärdade diverse skrivfel i flera moduler</span><span class="sxs-lookup"><span data-stu-id="e9175-225">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="e9175-226">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e9175-226">Az.Accounts</span></span>
* <span data-ttu-id="e9175-227">Stöd för användartilldelat MSI i Azure Functions-autentisering (#9479)</span><span class="sxs-lookup"><span data-stu-id="e9175-227">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="e9175-228">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="e9175-228">Az.Aks</span></span>
* <span data-ttu-id="e9175-229">Åtgärda problem med utdata för "Get-AzAks"</span><span class="sxs-lookup"><span data-stu-id="e9175-229">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="e9175-230">Mer information här: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="e9175-230">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="e9175-231">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e9175-231">Az.ApiManagement</span></span>
* <span data-ttu-id="e9175-232">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="e9175-232">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="e9175-233">Uppdatera .net-NuGet-versionen, som inte tillämpar begränsningar för productId, apiId och userId</span><span class="sxs-lookup"><span data-stu-id="e9175-233">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="e9175-234">**Get-AzApiManagementProduct** – Lade till stöd för frågekörning mot produkter via API.</span><span class="sxs-lookup"><span data-stu-id="e9175-234">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="e9175-235">**New-AzApiManagementApiRevision** – Korrigering för problem där ApiRevisionDescription inte angavs vid skapande av ny API-revision https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="e9175-235">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="e9175-236">Åtgärdade skrivfel i modellen "PsApiManagementOAuth2AuthrozationServer" till "PsApiManagementOAuth2AuthorizationServer"</span><span class="sxs-lookup"><span data-stu-id="e9175-236">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="e9175-237">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="e9175-237">Az.Batch</span></span>
* <span data-ttu-id="e9175-238">Åtgärdade skrivfel i hjälpmeddelande och dokumentation till att skriva Windows med versaler</span><span class="sxs-lookup"><span data-stu-id="e9175-238">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="e9175-239">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e9175-239">Az.Cdn</span></span>
* <span data-ttu-id="e9175-240">Åtgärdade skrivfel i CDN-modulens konverteringshjälp</span><span class="sxs-lookup"><span data-stu-id="e9175-240">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e9175-241">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e9175-241">Az.Compute</span></span>
* <span data-ttu-id="e9175-242">Lägg till VmssId i New-AzVMConfig-cmdleten</span><span class="sxs-lookup"><span data-stu-id="e9175-242">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="e9175-243">Lägg till parametrarna TerminateScheduledEvents och TerminateScheduledEventNotBeforeTimeoutInMinutes i New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e9175-243">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="e9175-244">Lägg till egenskapen HyperVGeneration till avbildningsobjekt för virtuell dator</span><span class="sxs-lookup"><span data-stu-id="e9175-244">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="e9175-245">Lägg till funktioner för Host och HostGroup</span><span class="sxs-lookup"><span data-stu-id="e9175-245">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="e9175-246">Nya cmdletar:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="e9175-246">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="e9175-247">HostId-parametern läggs till i New-AzVMConfig och New-AzVM</span><span class="sxs-lookup"><span data-stu-id="e9175-247">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="e9175-248">Uppdatera exempel i "Invoke-AzVMRunCommand"-dokumentationen till att använda rätt parameternamn</span><span class="sxs-lookup"><span data-stu-id="e9175-248">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="e9175-249">Uppdatera "-VolumeType"-beskrivningen i referensdokumentationen för "set-AzVMDiskEncryptionExtension" och "set-AzVmssDiskEncryptionExtension"</span><span class="sxs-lookup"><span data-stu-id="e9175-249">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e9175-250">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e9175-250">Az.DataFactory</span></span>
* <span data-ttu-id="e9175-251">Åtgärda skrivfel till att använda versaler för "Windows" i "New-AzDataFactoryEncryptValue"-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="e9175-251">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="e9175-252">Uppdaterade ADF .Net SDK-versionen till 4.1.2</span><span class="sxs-lookup"><span data-stu-id="e9175-252">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="e9175-253">Lägg till parametrarna "DataProxyIntegrationRuntimeName", "DataProxyStagingLinkedServiceName" och "DataProxyStagingPath" för "Set-AzureRmDataFactoryV2IntegrationRuntime"-cmd för att aktivera konfiguration av lokalt installerad integrationskörning som en proxy för SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="e9175-253">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="e9175-254">Uppdaterade PSTriggerRun till att visa utlöst pipeline, meddelande och egenskaper samt PSActivityRun till att visa aktivitetstypen</span><span class="sxs-lookup"><span data-stu-id="e9175-254">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e9175-255">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e9175-255">Az.DataLakeStore</span></span>
* <span data-ttu-id="e9175-256">Korrigering av frysning av Get-DataLakeStoreDeletedItem för fel eller fjärrundantag.</span><span class="sxs-lookup"><span data-stu-id="e9175-256">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="e9175-257">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e9175-257">Az.EventHub</span></span>
* <span data-ttu-id="e9175-258">Korrigering av problem #9658 : Skrivfel i parametern VirtualNteworkRule i Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="e9175-258">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="e9175-259">Korrigering av problem #9558 : Set-AzEventHubNamespace använder PATCH i stället för PUT</span><span class="sxs-lookup"><span data-stu-id="e9175-259">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="e9175-260">lade till parametern EnableKafka i Set-AzEventHubNamespace-cmdleten</span><span class="sxs-lookup"><span data-stu-id="e9175-260">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="e9175-261">Korrigering av problem #9786 : kan inte skapa en regel med Endast lyssna-behörighet</span><span class="sxs-lookup"><span data-stu-id="e9175-261">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="e9175-262">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="e9175-262">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="e9175-263">Åtgärdade skrivfel i dokumentation där "Azure" skrevs helt med gemener</span><span class="sxs-lookup"><span data-stu-id="e9175-263">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e9175-264">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e9175-264">Az.Monitor</span></span>
* <span data-ttu-id="e9175-265">Åtgärdade felaktigt parameternamn i hjälpdokumentationen</span><span class="sxs-lookup"><span data-stu-id="e9175-265">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e9175-266">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e9175-266">Az.Network</span></span>
* <span data-ttu-id="e9175-267">Uppdaterade New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e9175-267">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="e9175-268">Gjorde parametern "PublicIpAddress" inaktuell eftersom den aldrig används på serversidan.</span><span class="sxs-lookup"><span data-stu-id="e9175-268">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="e9175-269">Lade till den valfria parametern "Primary", som anger huruvida den aktuella IP-konfigurationen är den primära.</span><span class="sxs-lookup"><span data-stu-id="e9175-269">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="e9175-270">Förbättrade hanteringen av felundantag för begärande från SDK – åtgärdar problemet att tidigare SDK-undantag inte hanteras på rätt sätt, vilket leder till att viktig felinformation inte visas</span><span class="sxs-lookup"><span data-stu-id="e9175-270">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="e9175-271">Justerade valideringslogiken för IPv6-IP-prefix till att kontrollera korrekt IPv6-prefixlängd.</span><span class="sxs-lookup"><span data-stu-id="e9175-271">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="e9175-272">Uppdaterade Get-AzVirtualNetworkSubnetConfig: Lade till parameter som anges till get av undernätets resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="e9175-272">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="e9175-273">Uppdaterade beskrivningen av parametern Location för AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="e9175-273">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e9175-274">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e9175-274">Az.OperationalInsights</span></span>
* <span data-ttu-id="e9175-275">Uppdaterade dokumentation för "New-AzOperationalInsightsLinuxSyslogDataSource"</span><span class="sxs-lookup"><span data-stu-id="e9175-275">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="e9175-276">Lade till exempel</span><span class="sxs-lookup"><span data-stu-id="e9175-276">Added example</span></span>
    - <span data-ttu-id="e9175-277">Uppdaterade beskrivningen av parametern "-Name"</span><span class="sxs-lookup"><span data-stu-id="e9175-277">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="e9175-278">Lade till ett exempel för New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="e9175-278">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="e9175-279">Ändrade beskrivningen av parametern -Name för New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="e9175-279">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e9175-280">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e9175-280">Az.RecoveryServices</span></span>
* <span data-ttu-id="e9175-281">Uppdatera "Get-AzRecoveryServicesBackupJobDetail.md"</span><span class="sxs-lookup"><span data-stu-id="e9175-281">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="e9175-282">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e9175-282">Az.Resources</span></span>
* <span data-ttu-id="e9175-283">Lägg till stöd för den nya API-versionen från 2019-05-10 för Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="e9175-283">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="e9175-284">Lägg till stöd för "copy.count = 0" för variabler, resurser och egenskaper</span><span class="sxs-lookup"><span data-stu-id="e9175-284">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="e9175-285">Resurser med "condition = false" eller "copy.count = 0" tas bort i complete-läget</span><span class="sxs-lookup"><span data-stu-id="e9175-285">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="e9175-286">Lägg till ett exempel på tilldelning av princip på prenumerationsnivå i hjälpdokumentationen</span><span class="sxs-lookup"><span data-stu-id="e9175-286">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="e9175-287">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e9175-287">Az.ServiceBus</span></span>
* <span data-ttu-id="e9175-288">Korrigering av problem #9658 : Skrivfel i parametern VirtualNetworkRule i set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="e9175-288">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="e9175-289">Korrigering av problem #9786 : kan inte skapa en regel med Endast lyssna-behörighet</span><span class="sxs-lookup"><span data-stu-id="e9175-289">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="e9175-290">Lade till det nya kommandot "Test-AzServiceBusNameAvailability" för att kontrollera namntillgängligheten för kö och ämne</span><span class="sxs-lookup"><span data-stu-id="e9175-290">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="e9175-291">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e9175-291">Az.ServiceFabric</span></span>
* <span data-ttu-id="e9175-292">Åtgärda buggar med tillägg av nodtyps-cmdlet:</span><span class="sxs-lookup"><span data-stu-id="e9175-292">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="e9175-293">NullReferenceException-bugg när resursgrupp hade annan vmss som inte är relaterad till Service Fabric-klustret.</span><span class="sxs-lookup"><span data-stu-id="e9175-293">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="e9175-294">Åtgärdar problemet: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="e9175-294">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="e9175-295">Åtgärda bugg där cmdleten misslyckades om virtualNetwork var i en annan resursgrupp än klustret.</span><span class="sxs-lookup"><span data-stu-id="e9175-295">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="e9175-296">Åtgärdar problemet: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="e9175-296">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="e9175-297">AzServiceFabricApplicationCertificate-cmdleten görs inaktuell</span><span class="sxs-lookup"><span data-stu-id="e9175-297">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="e9175-298">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e9175-298">Az.Sql</span></span>
* <span data-ttu-id="e9175-299">Uppdatera dokumentation om gamla gransknings-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="e9175-299">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e9175-300">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e9175-300">Az.Storage</span></span>
* <span data-ttu-id="e9175-301">Uppdatera hjälpen för Get/Close-AzStorageFileHandle genom att lägga till fler scenarier i cmdlet-exempel och uppdatera parameterbeskrivningar</span><span class="sxs-lookup"><span data-stu-id="e9175-301">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="e9175-302">Stöd för StandardBlobTier i uppladdningsblob och kopieringsblob</span><span class="sxs-lookup"><span data-stu-id="e9175-302">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="e9175-303">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="e9175-303">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="e9175-304">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="e9175-304">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="e9175-305">Stöd för rehydratiseringsprioritet i kopieringsblob</span><span class="sxs-lookup"><span data-stu-id="e9175-305">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="e9175-306">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="e9175-306">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e9175-307">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e9175-307">Az.Websites</span></span>
* <span data-ttu-id="e9175-308">Lägg till klargöranden gällande parametern -AppSettings i Set-AzWebApp och Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e9175-308">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="e9175-309">2.5.0 – July 2019</span><span class="sxs-lookup"><span data-stu-id="e9175-309">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e9175-310">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e9175-310">Az.Accounts</span></span>
* <span data-ttu-id="e9175-311">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="e9175-311">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="e9175-312">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="e9175-312">Az.ApplicationInsights</span></span>
* <span data-ttu-id="e9175-313">Korrigera skrivfel i exempel i dokumentationen för Remove-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="e9175-313">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="e9175-314">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e9175-314">Az.Automation</span></span>
* <span data-ttu-id="e9175-315">Korrigera skrivfel i resurssträng</span><span class="sxs-lookup"><span data-stu-id="e9175-315">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="e9175-316">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e9175-316">Az.CognitiveServices</span></span>
* <span data-ttu-id="e9175-317">Stöd för NetworkRuleSet har lagts till.</span><span class="sxs-lookup"><span data-stu-id="e9175-317">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e9175-318">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e9175-318">Az.Compute</span></span>
* <span data-ttu-id="e9175-319">Lägg till saknade egenskaper (ComputerName, OsName, OsVersion och HyperVGeneration) för visningsobjekt i den virtuella datorinstansen.</span><span class="sxs-lookup"><span data-stu-id="e9175-319">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="e9175-320">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e9175-320">Az.ContainerRegistry</span></span>
* <span data-ttu-id="e9175-321">Åtgärda skrivfel i Remove-AzContainerRegistryReplication för parametern Replication</span><span class="sxs-lookup"><span data-stu-id="e9175-321">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="e9175-322">Mer information finns här: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="e9175-322">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e9175-323">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e9175-323">Az.DataFactory</span></span>
* <span data-ttu-id="e9175-324">ADF .Net SDK-versionen har uppdaterats till 4.1.0</span><span class="sxs-lookup"><span data-stu-id="e9175-324">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="e9175-325">Korrigera skrivfel i dokumentationen för Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="e9175-325">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="e9175-326">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e9175-326">Az.EventHub</span></span>
* <span data-ttu-id="e9175-327">Ny cmmdlet har lagts till för att skapa SAS-token: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="e9175-327">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="e9175-328">verifierings- och felmeddelande har lagts till för authorizationrules-rättigheter om endast "hantera" har tilldelats</span><span class="sxs-lookup"><span data-stu-id="e9175-328">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e9175-329">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e9175-329">Az.KeyVault</span></span>
* <span data-ttu-id="e9175-330">Stöd har lagts till för att ange KeySize för certifikatprinciper</span><span class="sxs-lookup"><span data-stu-id="e9175-330">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="e9175-331">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="e9175-331">Az.LogicApp</span></span>
* <span data-ttu-id="e9175-332">Korrigering för Get-AzIntegrationAccountMap för att lista alla mappningstyper</span><span class="sxs-lookup"><span data-stu-id="e9175-332">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="e9175-333">Ny MapType-parameter har lagts till för filtrering</span><span class="sxs-lookup"><span data-stu-id="e9175-333">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="e9175-334">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="e9175-334">Az.ManagedServices</span></span>
* <span data-ttu-id="e9175-335">Stöd för API-versionen 2019-06-01 (GA) har lagts till</span><span class="sxs-lookup"><span data-stu-id="e9175-335">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e9175-336">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e9175-336">Az.Network</span></span>
* <span data-ttu-id="e9175-337">Lägg till stöd för privat slutpunkt och privat länktjänst</span><span class="sxs-lookup"><span data-stu-id="e9175-337">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="e9175-338">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="e9175-338">New cmdlets</span></span>
        - <span data-ttu-id="e9175-339">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="e9175-339">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="e9175-340">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e9175-340">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="e9175-341">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e9175-341">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="e9175-342">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e9175-342">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="e9175-343">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e9175-343">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="e9175-344">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e9175-344">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="e9175-345">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="e9175-345">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="e9175-346">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e9175-346">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="e9175-347">Nedanstående kommandon för funktionen har uppdaterats: Flaggan PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies på undernätet i VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e9175-347">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="e9175-348">Uppdaterade New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="e9175-348">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="e9175-349">Valfri parameter har lagts till – PrivateEndpointNetworkPoliciesFlag som konfigurerar huruvida nätverksprinciper ska tillämpas på en privat slutpunkt i det här undernätet.</span><span class="sxs-lookup"><span data-stu-id="e9175-349">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="e9175-350">Valfri parameter har lagts till – PrivateLinkServiceNetworkPoliciesFlag som konfigurerar huruvida nätverksprinciper ska tillämpas på en privat länktjänst i det här undernätet.</span><span class="sxs-lookup"><span data-stu-id="e9175-350">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="e9175-351">AzPrivateLinkService för cmdlet-parametern ServiceName har bytt namn till Name med aliaset ServiceName för bakåtkompatibilitet</span><span class="sxs-lookup"><span data-stu-id="e9175-351">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="e9175-352">Aktivera ICMP-protokoll för konfiguration av nätverkssäkerhetsregler</span><span class="sxs-lookup"><span data-stu-id="e9175-352">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="e9175-353">Uppdaterade cmdletar</span><span class="sxs-lookup"><span data-stu-id="e9175-353">Updated cmdlets</span></span>
        - <span data-ttu-id="e9175-354">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e9175-354">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="e9175-355">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e9175-355">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="e9175-356">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e9175-356">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="e9175-357">Lägg till ConnectionProtocolType (Ikev1/Ikev2) som en konfigurerbar parameter för New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="e9175-357">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="e9175-358">Lägg till PrivateIpAddressVersion i LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="e9175-358">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="e9175-359">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="e9175-359">Updated cmdlet:</span></span>
        - <span data-ttu-id="e9175-360">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="e9175-360">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="e9175-361">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="e9175-361">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="e9175-362">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="e9175-362">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="e9175-363">Uppdatering av Application Gateway-kommandot New-AzApplicationGatewayProbeConfig för stöd av anpassad port i Probe</span><span class="sxs-lookup"><span data-stu-id="e9175-363">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="e9175-364">Uppdaterade New-AzApplicationGatewayProbeConfig: Den valfria parametern Port som används för avsökning i serverdelen har lagts till.</span><span class="sxs-lookup"><span data-stu-id="e9175-364">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="e9175-365">Denna parameter gäller för SKU:erna Standard_V2 och WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="e9175-365">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e9175-366">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e9175-366">Az.OperationalInsights</span></span>
* <span data-ttu-id="e9175-367">Uppdaterade standardversionen för sparade sökningar till 1.</span><span class="sxs-lookup"><span data-stu-id="e9175-367">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="e9175-368">Åtgärdade hantering av anpassad log null regex</span><span class="sxs-lookup"><span data-stu-id="e9175-368">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e9175-369">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e9175-369">Az.RecoveryServices</span></span>
* <span data-ttu-id="e9175-370">Uppdatera Get-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="e9175-370">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="e9175-371">Uppdatera Get-AzRecoveryServicesBackupContainer.md</span><span class="sxs-lookup"><span data-stu-id="e9175-371">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="e9175-372">Uppdatera Get-AzRecoveryServicesVault.md</span><span class="sxs-lookup"><span data-stu-id="e9175-372">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="e9175-373">Uppdatera Wait-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="e9175-373">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="e9175-374">Uppdatera Set-AzRecoveryServicesVaultContext.md</span><span class="sxs-lookup"><span data-stu-id="e9175-374">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="e9175-375">Uppdatera Get-AzRecoveryServicesBackupItem.md</span><span class="sxs-lookup"><span data-stu-id="e9175-375">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="e9175-376">Uppdatera Get-AzRecoveryServicesBackupRecoveryPoint.md</span><span class="sxs-lookup"><span data-stu-id="e9175-376">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="e9175-377">Uppdatera Restore-AzRecoveryServicesBackupItem.md</span><span class="sxs-lookup"><span data-stu-id="e9175-377">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="e9175-378">Uppdaterat tjänstanrop för avregistrering av container för Azure-filresurs</span><span class="sxs-lookup"><span data-stu-id="e9175-378">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="e9175-379">Uppdatera Set-AzRecoveryServicesAsrAlertSetting.md</span><span class="sxs-lookup"><span data-stu-id="e9175-379">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="e9175-380">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e9175-380">Az.Resources</span></span>
- <span data-ttu-id="e9175-381">Ta bort den cmdlet som saknas och som refereras i dokumentationen till New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e9175-381">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="e9175-382">Princip-cmdletar har uppdaterats så att de använder den nya API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="e9175-382">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="e9175-383">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e9175-383">Az.ServiceBus</span></span>
* <span data-ttu-id="e9175-384">Ny cmmdlet har lagts till för att skapa SAS-token: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="e9175-384">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="e9175-385">verifierings- och felmeddelande har lagts till för authorizationrules-rättigheter om endast "hantera" har tilldelats</span><span class="sxs-lookup"><span data-stu-id="e9175-385">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="e9175-386">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e9175-386">Az.Sql</span></span>
* <span data-ttu-id="e9175-387">Åtgärda saknade exempel för Set-AzSqlDatabaseSecondary cmdlet</span><span class="sxs-lookup"><span data-stu-id="e9175-387">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="e9175-388">Åtgärda angivna återkommande genomsökningar för bedömning av säkerhetsrisk utan angivna e-postadresser</span><span class="sxs-lookup"><span data-stu-id="e9175-388">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="e9175-389">Korrigera ett skrivfel i ett varningsmeddelande.</span><span class="sxs-lookup"><span data-stu-id="e9175-389">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e9175-390">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e9175-390">Az.Storage</span></span>
* <span data-ttu-id="e9175-391">Uppdatera exempel i referensdokumentationen för Get-AzStorageAccount så att rätt parameternamn används</span><span class="sxs-lookup"><span data-stu-id="e9175-391">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="e9175-392">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="e9175-392">Az.StorageSync</span></span>
* <span data-ttu-id="e9175-393">Lägger till cmdleten Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="e9175-393">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="e9175-394">Åtgärda problem 9551 så att TierFilesOlderThanDays föredras</span><span class="sxs-lookup"><span data-stu-id="e9175-394">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e9175-395">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e9175-395">Az.Websites</span></span>
* <span data-ttu-id="e9175-396">Åtgärdar ett fel där vissa SiteConfig-egenskaper inte returnerades av Get-AzWebApp och Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e9175-396">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="e9175-397">Lägger till en ny platsparameter för Get-AzDeletedWebApp och Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="e9175-397">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="e9175-398">Åtgärdar ett fel i kloning av webbapp-platser som använder New-AzWebApp-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="e9175-398">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="e9175-399">2.4.0 – juli 2019</span><span class="sxs-lookup"><span data-stu-id="e9175-399">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e9175-400">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e9175-400">Az.Accounts</span></span>
* <span data-ttu-id="e9175-401">Lägg till stöd för profil-cmdletar</span><span class="sxs-lookup"><span data-stu-id="e9175-401">Add support for profile cmdlets</span></span>
* <span data-ttu-id="e9175-402">Lägg till stöd för miljöer och dataplaner i genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="e9175-402">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="e9175-403">Åtgärda bugg där fel slutpunkt i vissa fall användes för cmdletar för dataplaner i Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="e9175-403">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="e9175-404">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="e9175-404">Az.Advisor</span></span>
* <span data-ttu-id="e9175-405">GA-version av Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="e9175-405">GA release of Az.Advisor</span></span>
* <span data-ttu-id="e9175-406">Den här modulen ingår nu som en del av `Az`-sammanslagningsmodulen</span><span class="sxs-lookup"><span data-stu-id="e9175-406">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="e9175-407">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e9175-407">Az.ApiManagement</span></span>
* <span data-ttu-id="e9175-408">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="e9175-408">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="e9175-409">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="e9175-409">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="e9175-410">Stöd för att fråga prenumerationer efter användare och produkt har lagts till</span><span class="sxs-lookup"><span data-stu-id="e9175-410">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="e9175-411">Stöd för att fråga med hjälp av omfång ”/”, ”/apis”, ”/apis/echo-api” har lagts till</span><span class="sxs-lookup"><span data-stu-id="e9175-411">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="e9175-412">Korrigering av problem https://github.com/Azure/azure-powershell/issues/9307 och https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="e9175-412">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="e9175-413">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="e9175-413">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="e9175-414">Stöd för att ange ”ApiVersion” och ”ApiVersionSetId” när API:er importeras har lagts till</span><span class="sxs-lookup"><span data-stu-id="e9175-414">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e9175-415">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e9175-415">Az.Automation</span></span>
* <span data-ttu-id="e9175-416">Bugg med cmdleten Set-AzAutomationConnectionFieldValue för att hantera strängvärde har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="e9175-416">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e9175-417">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e9175-417">Az.Compute</span></span>
* <span data-ttu-id="e9175-418">Lägg till parametern HyperVGeneration i New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="e9175-418">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e9175-419">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e9175-419">Az.DataFactory</span></span>
* <span data-ttu-id="e9175-420">Uppdaterar utdata från ADF-cmdletar som hämtar aktivitetskörningar, hämtar pipelinekörningar och hämtar utlösarkörningar för stöd för Select-Object-pipe.</span><span class="sxs-lookup"><span data-stu-id="e9175-420">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="e9175-421">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="e9175-421">Az.EventGrid</span></span>
* <span data-ttu-id="e9175-422">Korrigera stavfel i dokumentation om ”New-AzEventGridSubscription”</span><span class="sxs-lookup"><span data-stu-id="e9175-422">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e9175-423">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e9175-423">Az.IotHub</span></span>
* <span data-ttu-id="e9175-424">Lägg till stöd för att återskapa principnycklar för auktorisering.</span><span class="sxs-lookup"><span data-stu-id="e9175-424">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e9175-425">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e9175-425">Az.Network</span></span>
* <span data-ttu-id="e9175-426">”RoutingPreference” har lagts till i offentliga IP-taggar</span><span class="sxs-lookup"><span data-stu-id="e9175-426">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="e9175-427">Förbättra exempel för referensdokumentation om ”Get-AzNetworkServiceTag”</span><span class="sxs-lookup"><span data-stu-id="e9175-427">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="e9175-428">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="e9175-428">Az.PolicyInsights</span></span>
* <span data-ttu-id="e9175-429">Åtgärda problem med null-referens i Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="e9175-429">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="e9175-430">Mer information här: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="e9175-430">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e9175-431">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e9175-431">Az.OperationalInsights</span></span>
* <span data-ttu-id="e9175-432">Modellen för CustomLog-datakälla som returneras i Get-AzOperationalInsightsDataSource har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="e9175-432">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e9175-433">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e9175-433">Az.RecoveryServices</span></span>
* <span data-ttu-id="e9175-434">Kommandot get-policy för IaaSVM:er har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="e9175-434">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="e9175-435">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e9175-435">Az.Resources</span></span>
    - <span data-ttu-id="e9175-436">Korrigera hjälptext för den översta parametern i Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="e9175-436">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="e9175-437">Lägg till växlingsstöd på klientsidan för Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="e9175-437">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="e9175-438">Lägg till nya parametrar för Set-AzPolicyAssignment, -PolicyParameters och -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="e9175-438">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="e9175-439">En mängd dokument- och exempeluppdateringar för Policy-cmdletar</span><span class="sxs-lookup"><span data-stu-id="e9175-439">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="e9175-440">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e9175-440">Az.ServiceBus</span></span>
* <span data-ttu-id="e9175-441">Korrigering av problem #4938 – New-AzureRmServiceBusQueue returnerar BadRequest vid konfiguration av MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="e9175-441">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="e9175-442">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e9175-442">Az.Sql</span></span>
* <span data-ttu-id="e9175-443">Lägg till cmdletar för instansredundansgrupper från förhandsversion till offentlig version</span><span class="sxs-lookup"><span data-stu-id="e9175-443">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="e9175-444">Stöd för granskning för Azure SQL Server\Database med nya cmdletar.</span><span class="sxs-lookup"><span data-stu-id="e9175-444">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="e9175-445">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="e9175-445">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="e9175-446">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="e9175-446">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="e9175-447">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="e9175-447">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="e9175-448">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="e9175-448">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="e9175-449">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="e9175-449">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="e9175-450">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="e9175-450">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="e9175-451">Ta bort begränsningar för e-post från inställningarna för sårbarhetsbedömning</span><span class="sxs-lookup"><span data-stu-id="e9175-451">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e9175-452">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e9175-452">Az.Storage</span></span>
* <span data-ttu-id="e9175-453">Ändra två parametrar ”-IndexDocument” och ”-ErrorDocument404Path” från ”krävs” till ”valfri” i cmdlet:</span><span class="sxs-lookup"><span data-stu-id="e9175-453">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="e9175-454">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="e9175-454">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="e9175-455">Uppdatera hjälpen för Get-AzStorageBlobContent genom att lägga till ett exempel</span><span class="sxs-lookup"><span data-stu-id="e9175-455">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="e9175-456">Visa mer felinformation när cmdleten misslyckas med StorageException</span><span class="sxs-lookup"><span data-stu-id="e9175-456">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="e9175-457">Stöd för att skapa eller uppdatera lagringskonto med Azure Files AAD DS-autentisering</span><span class="sxs-lookup"><span data-stu-id="e9175-457">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="e9175-458">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e9175-458">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="e9175-459">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e9175-459">Set-AzStorageAccount</span></span>
* <span data-ttu-id="e9175-460">Stöd för att lista eller stänga filreferenser för en filresurs, filkatalog eller en fil</span><span class="sxs-lookup"><span data-stu-id="e9175-460">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="e9175-461">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="e9175-461">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="e9175-462">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="e9175-462">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="e9175-463">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="e9175-463">Az.StorageSync</span></span>
* <span data-ttu-id="e9175-464">Den här modulen ingår nu som en del av `Az`-sammanslagningsmodulen</span><span class="sxs-lookup"><span data-stu-id="e9175-464">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="e9175-465">2.3.2 – juni 2019</span><span class="sxs-lookup"><span data-stu-id="e9175-465">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e9175-466">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e9175-466">Az.Accounts</span></span>
* <span data-ttu-id="e9175-467">Åtgärda bugg med felaktiga webbadresser som i vissa fall användes för Functions-anrop</span><span class="sxs-lookup"><span data-stu-id="e9175-467">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="e9175-468">Mer information här: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="e9175-468">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="e9175-469">Åtgärda problem med alias från AzureRM i Az-cmdletar</span><span class="sxs-lookup"><span data-stu-id="e9175-469">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="e9175-470">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="e9175-470">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="e9175-471">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="e9175-471">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e9175-472">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e9175-472">Az.Compute</span></span>
* <span data-ttu-id="e9175-473">Parameteruppsättningarna New-AzVm och New-AzVmss accepterar nu parametern ”ProximityPlacementGroup”.</span><span class="sxs-lookup"><span data-stu-id="e9175-473">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="e9175-474">Stavfel i referensdokumentationen för ”New-AzVM” har korrigerats</span><span class="sxs-lookup"><span data-stu-id="e9175-474">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="e9175-475">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="e9175-475">Az.Dns</span></span>
* <span data-ttu-id="e9175-476">Stavfel i hjälpexempel för ”Set-AzDnsZone” har korrigerats.</span><span class="sxs-lookup"><span data-stu-id="e9175-476">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="e9175-477">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="e9175-477">Az.EventGrid</span></span>
* <span data-ttu-id="e9175-478">Har uppdaterats för att använda API-versionen 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="e9175-478">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="e9175-479">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="e9175-479">New cmdlets:</span></span>
    - <span data-ttu-id="e9175-480">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="e9175-480">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="e9175-481">Skapar en ny Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="e9175-481">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="e9175-482">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="e9175-482">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="e9175-483">Hämtar information om en Event Grid-domän eller hämtar en lista med alla Event Grid-domäner i den aktuella Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="e9175-483">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="e9175-484">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="e9175-484">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="e9175-485">Tar bort en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="e9175-485">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="e9175-486">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="e9175-486">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="e9175-487">Återskapar nyckeln för delad åtkomst för en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="e9175-487">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="e9175-488">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="e9175-488">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="e9175-489">Hämtar de nycklar för delad åtkomst som används för att publicera händelser till en Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="e9175-489">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="e9175-490">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="e9175-490">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="e9175-491">Skapar ett nytt Azure Event Grid-domänämne.</span><span class="sxs-lookup"><span data-stu-id="e9175-491">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="e9175-492">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="e9175-492">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="e9175-493">Hämtar information om ett Event Grid-domänämne eller hämtar en lista med alla Event Grid-domänämnen under en specifik Event Grid-domän i nuvarande Azure</span><span class="sxs-lookup"><span data-stu-id="e9175-493">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="e9175-494">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="e9175-494">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="e9175-495">Tar bort ett befintligt Azure Event Grid-domänämne.</span><span class="sxs-lookup"><span data-stu-id="e9175-495">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="e9175-496">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="e9175-496">Updated cmdlets:</span></span>
    - <span data-ttu-id="e9175-497">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="e9175-497">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="e9175-498">Lägg till nya obligatoriska parametrar för att stödja piping för den nya Event Grid-domänen och Event Grid-domänämnet för att göra det möjligt att skapa nya händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="e9175-498">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="e9175-499">Lägg till nya obligatoriska parametrar för att ange det nya Event Grid-domännamnet och/eller namnet på Event Grid-domänämnet för att göra det möjligt att skapa nya händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="e9175-499">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="e9175-500">Lägg till ny parameteruppsättningar för domäner och domänämnen för att göra det möjligt att återanvända befintliga parametrar (t.ex. EndPointType, SubjectBeginsWith osv).</span><span class="sxs-lookup"><span data-stu-id="e9175-500">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="e9175-501">Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="e9175-501">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="e9175-502">Förfallodatum för händelseprenumeration</span><span class="sxs-lookup"><span data-stu-id="e9175-502">Event subscription expiration date,</span></span>
            - <span data-ttu-id="e9175-503">Avancerade filterparametrar.</span><span class="sxs-lookup"><span data-stu-id="e9175-503">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="e9175-504">Lägg till ny uppräkning för servicebusqueue som mål.</span><span class="sxs-lookup"><span data-stu-id="e9175-504">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="e9175-505">Tillåt inte användning av ”Alla” i alternativet -IncludedEventType och ersätt det med</span><span class="sxs-lookup"><span data-stu-id="e9175-505">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="e9175-506">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="e9175-506">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="e9175-507">Lägg till ny valfria parametrar (Top, ODataQuery och NextLink) för att stödja sidnumrering och filtrering av resultat.</span><span class="sxs-lookup"><span data-stu-id="e9175-507">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="e9175-508">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="e9175-508">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="e9175-509">Lägg till nya obligatoriska parametrar för att stödja piping för en Event Grid-domän och Event Grid-domänämnen för att göra det möjligt att ta bort befintliga händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="e9175-509">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="e9175-510">Lägg till nya obligatoriska parametrar för att ange Event Grid-domännamnet och/eller namnet på Event Grid-domänämnet för att göra det möjligt att ta bort befintliga händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="e9175-510">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="e9175-511">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="e9175-511">Az.FrontDoor</span></span>
* <span data-ttu-id="e9175-512">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="e9175-512">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="e9175-513">Lägg till stöd för transformeringar och nytt värde för automatisk komplettering för operatorer (RegEx)</span><span class="sxs-lookup"><span data-stu-id="e9175-513">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="e9175-514">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="e9175-514">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="e9175-515">Lägg till nya värden för automatisk komplettering</span><span class="sxs-lookup"><span data-stu-id="e9175-515">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e9175-516">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e9175-516">Az.Network</span></span>
* <span data-ttu-id="e9175-517">Lägg till stöd för resurs för virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="e9175-517">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="e9175-518">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="e9175-518">New cmdlets</span></span>
        - <span data-ttu-id="e9175-519">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="e9175-519">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="e9175-520">Lägg till AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="e9175-520">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="e9175-521">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="e9175-521">New cmdlets</span></span> 
        - <span data-ttu-id="e9175-522">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="e9175-522">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="e9175-523">Lägg till PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e9175-523">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="e9175-524">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="e9175-524">New cmdlets</span></span> 
        - <span data-ttu-id="e9175-525">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e9175-525">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="e9175-526">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e9175-526">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="e9175-527">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e9175-527">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="e9175-528">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e9175-528">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="e9175-529">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e9175-529">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="e9175-530">Lägg till PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="e9175-530">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="e9175-531">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="e9175-531">New cmdlets</span></span>
        - <span data-ttu-id="e9175-532">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="e9175-532">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="e9175-533">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="e9175-533">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="e9175-534">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="e9175-534">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="e9175-535">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="e9175-535">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="e9175-536">Nedanstående kommandon för funktionen har uppdaterats: Flaggan UseLocalAzureIpAddress på VpnConnection</span><span class="sxs-lookup"><span data-stu-id="e9175-536">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="e9175-537">New-AzVpnConnection har uppdaterats: Den valfria parametern -UseLocalAzureIpAddress har lagts till för att visa att en lokal IP-adress i Azure ska användas som källadress när anslutningen initieras.</span><span class="sxs-lookup"><span data-stu-id="e9175-537">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="e9175-538">Set-AzVpnConnection har uppdaterats: Den valfria parametern -UseLocalAzureIpAddress har lagts till för att visa att en lokal IP-adress i Azure ska användas som källadress när anslutningen initieras.</span><span class="sxs-lookup"><span data-stu-id="e9175-538">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="e9175-539">Det skrivskyddade fältet PeeredConnections har lagts till i ExpressRoute-peering.</span><span class="sxs-lookup"><span data-stu-id="e9175-539">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="e9175-540">Det skrivskyddade fältet GlobalReachEnabled har lagts till i ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="e9175-540">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="e9175-541">Ett attribut för icke-bakåtkompatibla ändringar har lagts till för att lyfta fram utfasning av fältet AllowGlobalReach i modellen ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e9175-541">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="e9175-542">Problem 8756 har åtgärdats: Fel vid användning av TargetListenerID med AzApplicationGatewayRedirectConfiguration-cmdletar</span><span class="sxs-lookup"><span data-stu-id="e9175-542">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="e9175-543">En bugg i New-AzApplicationGatewayPathRuleConfig som gjorde att regeluppsättningen för att återskapa inte kunde anges har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="e9175-543">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="e9175-544">Visningen av VirtualNetworkTaps i NetworkInterfaceIpConfiguration har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="e9175-544">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="e9175-545">Cortex Get-cmdletar för att visa en lista med alla delar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="e9175-545">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="e9175-546">Funktionen för att skapa VirtualHub-referenser för ExpressRouteGateways och VpnGateway har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="e9175-546">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="e9175-547">Stöd för tillgänglighetszoner i AzureFirewall och NatGateway har lagts till</span><span class="sxs-lookup"><span data-stu-id="e9175-547">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="e9175-548">Cmdleten Get-AzNetworkServiceTag har lagts till</span><span class="sxs-lookup"><span data-stu-id="e9175-548">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="e9175-549">Lägg till stöd för flera offentliga IP-adresser för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="e9175-549">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="e9175-550">Cmdleten New-AzFirewall har uppdaterats:</span><span class="sxs-lookup"><span data-stu-id="e9175-550">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="e9175-551">Parametern -PublicIpAddress som accepterar ett eller flera offentliga IP-adressobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="e9175-551">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="e9175-552">Parametern -VirtualNetwork som accepterar ett virtuellt nätverksobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="e9175-552">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="e9175-553">Metoderna AddPublicIpAddress och RemovePublicIpAddress har lagts till på brandväggsobjekt – dessa accepterar ett offentligt IP-adressobjekt som indata</span><span class="sxs-lookup"><span data-stu-id="e9175-553">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="e9175-554">Inaktuella parametrar -PublicIpName och -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="e9175-554">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="e9175-555">Nedanstående kommandon för funktionen har uppdaterats: Ange autentiseringsalternativ för VpnClient AAD till resurser för virtuella nätverksgatewayer.</span><span class="sxs-lookup"><span data-stu-id="e9175-555">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="e9175-556">New-AzVirtualNetworkGateway har uppdaterats: De valfria parametrarna AadTenantUri, AadAudienceId och AadIssuerUri för att ange VpnClient AAD-autentiseringsalternativ på en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="e9175-556">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="e9175-557">Set-AzVirtualNetworkGateway har uppdaterats: De valfria parametrarna AadTenantUri, AadAudienceId och AadIssuerUri för att ange VpnClient AAD-autentiseringsalternativ på en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="e9175-557">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="e9175-558">Set-AzVirtualNetworkGateway har uppdaterats: Den valfria växelparametern RemoveAadAuthentication som tar bort VpnClient AAD-autentiseringsalternativ från en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="e9175-558">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e9175-559">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e9175-559">Az.OperationalInsights</span></span>
* <span data-ttu-id="e9175-560">Aktivera prisnivån **pergb2018** i kommandot ”New-AzureRmOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="e9175-560">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="e9175-561">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e9175-561">Az.Resources</span></span>
* <span data-ttu-id="e9175-562">Stöd för ytterligare alternativ för att exportera en mall</span><span class="sxs-lookup"><span data-stu-id="e9175-562">Support for additional Template Export options</span></span>
    - <span data-ttu-id="e9175-563">Lägg till parametern ”-SkipResourceNameParameterization” till Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e9175-563">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="e9175-564">Lägg till parametern ”-SkipAllParameterization” till Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e9175-564">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="e9175-565">Lägg till parametern ”-Resource” till Export-AzResourceGroup för exporterad resursfiltrering</span><span class="sxs-lookup"><span data-stu-id="e9175-565">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e9175-566">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e9175-566">Az.ServiceFabric</span></span>
* <span data-ttu-id="e9175-567">Åtgärda att fel tumavtryck används vid tilläggning av certifikat i ByExistingKeyVault i vissa fall</span><span class="sxs-lookup"><span data-stu-id="e9175-567">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="e9175-568">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e9175-568">Az.Sql</span></span>
* <span data-ttu-id="e9175-569">Åtgärda suffix för lagringsslutpunkt i Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="e9175-569">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="e9175-570">Åtgärda att aktivering av Advanced Data Security åsidosätter Advanced Threat Protection-princip</span><span class="sxs-lookup"><span data-stu-id="e9175-570">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="e9175-571">Nya cmdletar för Management.Sql som gör att kunderna kan lägga till nycklar för transparent datakryptering (TDE) och ange TDE-skydd för hanterade instanser</span><span class="sxs-lookup"><span data-stu-id="e9175-571">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="e9175-572">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e9175-572">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="e9175-573">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e9175-573">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="e9175-574">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e9175-574">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="e9175-575">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="e9175-575">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="e9175-576">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="e9175-576">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e9175-577">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e9175-577">Az.Storage</span></span>
* <span data-ttu-id="e9175-578">Stöd för typerna FileStorage och SkuName Premium_ZRS när lagringskonton skapas</span><span class="sxs-lookup"><span data-stu-id="e9175-578">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="e9175-579">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e9175-579">New-AzStorageAccount</span></span>
* <span data-ttu-id="e9175-580">Beskrivningen av cmdleten för bloboföränderlighet har förtydligats</span><span class="sxs-lookup"><span data-stu-id="e9175-580">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="e9175-581">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="e9175-581">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e9175-582">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e9175-582">Az.Websites</span></span>
* <span data-ttu-id="e9175-583">Optimerar Get-AzWebAppCertificate för att filtrera efter resursgrupp på servern i stället för klienten</span><span class="sxs-lookup"><span data-stu-id="e9175-583">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="e9175-584">Lägger till växlingsparametern -UseDisasterRecovery till Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="e9175-584">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="e9175-585">2.2.0 – juni 2019</span><span class="sxs-lookup"><span data-stu-id="e9175-585">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="e9175-586">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e9175-586">Az.Cdn</span></span>
* <span data-ttu-id="e9175-587">Uppdaterade cmdletar för att ge stöd för rulesEngine-funktion baserat på API-version 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="e9175-587">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e9175-588">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e9175-588">Az.Compute</span></span>
* <span data-ttu-id="e9175-589">Lade till parameter `NoWait` som startar åtgärden och returnerar omedelbart, innan åtgärden har slutförts.</span><span class="sxs-lookup"><span data-stu-id="e9175-589">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="e9175-590">Uppdaterade cmdletar:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="e9175-590">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="e9175-591">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e9175-591">Az.EventHub</span></span>
* <span data-ttu-id="e9175-592">Korrigering för #9231 – Get-AzEventHubNamespace returnerar inga taggar</span><span class="sxs-lookup"><span data-stu-id="e9175-592">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="e9175-593">Korrigering för #9230 – Get-AzEventHubNamespace returnerar ResourceGroup istället för ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9175-593">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e9175-594">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e9175-594">Az.Network</span></span>
* <span data-ttu-id="e9175-595">Uppdatera ResourceId och InputObject för NAT-gateway</span><span class="sxs-lookup"><span data-stu-id="e9175-595">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="e9175-596">Lägg till alias för ResourceId och InputObject</span><span class="sxs-lookup"><span data-stu-id="e9175-596">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="e9175-597">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="e9175-597">Az.PolicyInsights</span></span>
* <span data-ttu-id="e9175-598">Åtgärda Null-referensproblem i Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="e9175-598">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e9175-599">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e9175-599">Az.RecoveryServices</span></span>
* <span data-ttu-id="e9175-600">Minsta kvarhållning för IaaSVM-policy i dagar ändrat till 7 från 1</span><span class="sxs-lookup"><span data-stu-id="e9175-600">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="e9175-601">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e9175-601">Az.ServiceBus</span></span>
* <span data-ttu-id="e9175-602">Korrigering för ärende #9182 – Get-AzServiceBusNamespace returnerar ResourceGroup istället för ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9175-602">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e9175-603">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e9175-603">Az.ServiceFabric</span></span>
* <span data-ttu-id="e9175-604">Åtgärda stavfel i felmeddelandet för Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="e9175-604">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="e9175-605">Åtgärda saknat tecken i Service Fabric-kommandorader</span><span class="sxs-lookup"><span data-stu-id="e9175-605">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="e9175-606">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e9175-606">Az.Sql</span></span>
* <span data-ttu-id="e9175-607">Lägg till parametern DnsZonePartner för New-AzureSqlInstance-cmdlet för att ge stöd för AutoDr för hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="e9175-607">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="e9175-608">Avvecklar cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e9175-608">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="e9175-609">Döp om cmdletar för hotidentifiering till Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="e9175-609">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="e9175-610">Parametrarna New-AzSqlInstance -StorageSizeInGB och -LicenseType är nu valfria.</span><span class="sxs-lookup"><span data-stu-id="e9175-610">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e9175-611">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e9175-611">Az.Websites</span></span>
* <span data-ttu-id="e9175-612">åtgärdar problemet där användningen av Set-AzWebApp och Set-AzWebAppSlot med -WebApp-egenskap tog bort taggarna</span><span class="sxs-lookup"><span data-stu-id="e9175-612">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="e9175-613">2.1.0 – maj 2019</span><span class="sxs-lookup"><span data-stu-id="e9175-613">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="e9175-614">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e9175-614">Az.ApiManagement</span></span>
* <span data-ttu-id="e9175-615">Skapade nya cmdletar för att hantera diagnostik för global- och API-omfång</span><span class="sxs-lookup"><span data-stu-id="e9175-615">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="e9175-616">**Get-AzApiManagementDiagnostic** – Skaffa diagnostik konfigurerad för global- eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="e9175-616">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="e9175-617">**New-AzApiManagementDiagnostic** – Skapa ny diagnostik för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="e9175-617">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="e9175-618">**New-AzApiManagementHttpMessageDiagnostic** – Skapa diagnostikinställning om vilka rubriker som ska loggas och storleken på brödtextbyte</span><span class="sxs-lookup"><span data-stu-id="e9175-618">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="e9175-619">**New-AzApiManagementPipelineDiagnosticSetting** – Skapa diagnostikinställningar för inkommande/utgående HTTP-meddelanden till gatewayen.</span><span class="sxs-lookup"><span data-stu-id="e9175-619">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="e9175-620">**New-AzApiManagementSamplingSetting** – Skapa samplinginställningar för begäranden/svar för en diagnostik</span><span class="sxs-lookup"><span data-stu-id="e9175-620">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="e9175-621">**Remove-AzApiManagementDiagnostic** – Ta bort en diagnostikenhet för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="e9175-621">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="e9175-622">**Set-AzApiManagementDiagnostic** – Uppdatera en diagnostikenhet för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="e9175-622">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="e9175-623">Skapade nya cmdletar för hantering av cacheminne i ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="e9175-623">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="e9175-624">**Get-AzApiManagementCache** – Hämta information om cacheminnet som anges av identifierare eller alla cacheminnen</span><span class="sxs-lookup"><span data-stu-id="e9175-624">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="e9175-625">**New-AzApiManagementCache** – Skapa ett nytt default-cacheminne eller cacheminne i en viss Azure-region</span><span class="sxs-lookup"><span data-stu-id="e9175-625">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="e9175-626">**Remove-AzApiManagementCache** – Ta bort ett cacheminne</span><span class="sxs-lookup"><span data-stu-id="e9175-626">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="e9175-627">**Remove-AzApiManagementCache** – Ta bort ett cacheminne</span><span class="sxs-lookup"><span data-stu-id="e9175-627">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="e9175-628">Skapade nya cmdletar för hantering av API-schema</span><span class="sxs-lookup"><span data-stu-id="e9175-628">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="e9175-629">**New-AzApiManagementSchema** – Skapa ett nytt schema för ett API</span><span class="sxs-lookup"><span data-stu-id="e9175-629">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="e9175-630">**Get-AzApiManagementSchema** – Hämta de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="e9175-630">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="e9175-631">**Remove-AzApiManagementSchema** – Ta bort de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="e9175-631">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="e9175-632">**Set-AzApiManagementSchema** – Uppdatera de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="e9175-632">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="e9175-633">Skapa ny cmdlet för att generera en användartoken.</span><span class="sxs-lookup"><span data-stu-id="e9175-633">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="e9175-634">**New-AzApiManagementUserToken** – Skapa en ny användartoken som enligt standardinställning är giltig i 8 timmar. Token för GIT-användaren kan skapas med den här cmdleten./</span><span class="sxs-lookup"><span data-stu-id="e9175-634">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="e9175-635">Skapade en ny cmdlet för att hämta nätverksstatus</span><span class="sxs-lookup"><span data-stu-id="e9175-635">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="e9175-636">**Get-AzApiManagementNetworkStatus** – Hämta nätverksstatusanslutningen för resurserna som API Management-tjänsten är beroende av.</span><span class="sxs-lookup"><span data-stu-id="e9175-636">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="e9175-637">Det här är användbart när du distribuerar ApiManagement-tjänsten i ett virtuellt nätverk och validerar om något beroende är brutet.</span><span class="sxs-lookup"><span data-stu-id="e9175-637">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="e9175-638">Uppdaterade cmdlet **New-AzApiManagement** för att hantera ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="e9175-638">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="e9175-639">Lade till stöd för den nya SKU:n Consumption</span><span class="sxs-lookup"><span data-stu-id="e9175-639">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="e9175-640">Aktiverade stöd för att slå på flaggan EnableClientCertificate för SKU:n Consumption</span><span class="sxs-lookup"><span data-stu-id="e9175-640">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="e9175-641">Den nya cmdleten **New-AzApiManagementSslSetting** gör det möjligt att ställa in TLS/SSL-inställningen på ”Backend” och ”Frontend” (serverdel och klientdel).</span><span class="sxs-lookup"><span data-stu-id="e9175-641">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="e9175-642">Det här kan också användas till att konfigurera chiffer som 3DES och ServerProtocols som Http2 för Frontend för en ApiManagement-tjänst.</span><span class="sxs-lookup"><span data-stu-id="e9175-642">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="e9175-643">Stöd har lagts till för att konfigurera värdnamnet DeveloperPortal på ApiManagement-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="e9175-643">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="e9175-644">Uppdaterade cmdletar **Get-AzApiManagementSsoToken** för att ta PsApiManagement-objekt som indata</span><span class="sxs-lookup"><span data-stu-id="e9175-644">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="e9175-645">Uppdaterad cmdleten för att visa infogade felmeddelanden</span><span class="sxs-lookup"><span data-stu-id="e9175-645">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="e9175-646">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Felkod: Felmeddelande av typen ValidationError: Ett eller flera fält innehåller felaktiga värden: Felinformation:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="e9175-646">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="e9175-647">Uppdaterade cmdlet **Export-AzApiManagementApi** för att exportera API:er i OpenApi 3.0-format</span><span class="sxs-lookup"><span data-stu-id="e9175-647">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="e9175-648">Uppdaterade cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="e9175-648">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="e9175-649">Importera API från dokumentspecifikationen OpenApi 3.0</span><span class="sxs-lookup"><span data-stu-id="e9175-649">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="e9175-650">Om du vill åsidosätta egenskapen PsApiManagementSchema specificerad i ett dokument (Swagger, Wadl, Wsdl, OpenApi).</span><span class="sxs-lookup"><span data-stu-id="e9175-650">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="e9175-651">Åsidosätta egenskapen ServiceUrl som specificeras i ett dokument.</span><span class="sxs-lookup"><span data-stu-id="e9175-651">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="e9175-652">Uppdaterade cmdlet **Get-AzApiManagementPolicy** för att returnera policy i undantaget format av typen icke-XML med rawxml</span><span class="sxs-lookup"><span data-stu-id="e9175-652">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="e9175-653">Uppdaterade cmdlet **Set-AzApiManagementPolicy** för att godkänna policy i undantaget format av typen icke-XML med rawxml och XML undantaget med xml</span><span class="sxs-lookup"><span data-stu-id="e9175-653">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="e9175-654">Uppdaterad cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="e9175-654">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="e9175-655">Konfigurera API med OpenId auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="e9175-655">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="e9175-656">Skapa ett API i ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="e9175-656">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="e9175-657">Klona ett API med SourceApiId och SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="e9175-657">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="e9175-658">Möjlighet att konfigurera SubscriptionRequired i API-omfattningen.</span><span class="sxs-lookup"><span data-stu-id="e9175-658">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="e9175-659">Uppdaterad cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="e9175-659">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="e9175-660">Konfigurera API med OpenId auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="e9175-660">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="e9175-661">Uppdatera ett API till ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="e9175-661">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="e9175-662">Möjlighet att konfigurera SubscriptionRequired i API-omfattningen.</span><span class="sxs-lookup"><span data-stu-id="e9175-662">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="e9175-663">Uppdaterad cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="e9175-663">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="e9175-664">Klona en befintlig version med hjälp av SourceApiRevision (kopiera taggar, produkter, åtgärder och principer).</span><span class="sxs-lookup"><span data-stu-id="e9175-664">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="e9175-665">Den nya revisionen antar ApiId från den överordnade instansen.</span><span class="sxs-lookup"><span data-stu-id="e9175-665">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="e9175-666">Tillhandahålla ApiRevisionDescription</span><span class="sxs-lookup"><span data-stu-id="e9175-666">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="e9175-667">Åsidosätta ServiceUrl vid kloning av ett API.</span><span class="sxs-lookup"><span data-stu-id="e9175-667">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="e9175-668">Uppdaterad cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="e9175-668">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="e9175-669">Konfigurera AAD eller AADB2C med en Authority</span><span class="sxs-lookup"><span data-stu-id="e9175-669">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="e9175-670">Konfigurera SignupPolicy, SigninPolicy, ProfileEditingPolicy och PasswordResetPolicy</span><span class="sxs-lookup"><span data-stu-id="e9175-670">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="e9175-671">Uppdaterad cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="e9175-671">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="e9175-672">Kompensera för ny SubscriptonModel med Scope och UserId</span><span class="sxs-lookup"><span data-stu-id="e9175-672">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="e9175-673">Kompensera för gammal prenumerationsmodell med ProductId och UserId</span><span class="sxs-lookup"><span data-stu-id="e9175-673">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="e9175-674">Lägg till funktion för att aktivera AllowTracing på prenumerationsnivå.</span><span class="sxs-lookup"><span data-stu-id="e9175-674">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="e9175-675">Uppdaterad cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="e9175-675">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="e9175-676">Kompensera för ny SubscriptonModel med Scope och UserId</span><span class="sxs-lookup"><span data-stu-id="e9175-676">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="e9175-677">Kompensera för gammal prenumerationsmodell med ProductId och UserId</span><span class="sxs-lookup"><span data-stu-id="e9175-677">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="e9175-678">Lägg till funktion för att aktivera AllowTracing på prenumerationsnivå.</span><span class="sxs-lookup"><span data-stu-id="e9175-678">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="e9175-679">Uppdaterade följande cmdletar för att acceptera ResourceId som indata</span><span class="sxs-lookup"><span data-stu-id="e9175-679">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="e9175-680">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e9175-680">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="e9175-681">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="e9175-681">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="e9175-682">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="e9175-682">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="e9175-683">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="e9175-683">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="e9175-684">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="e9175-684">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="e9175-685">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="e9175-685">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="e9175-686">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="e9175-686">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="e9175-687">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e9175-687">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="e9175-688">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="e9175-688">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="e9175-689">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="e9175-689">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="e9175-690">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="e9175-690">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="e9175-691">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="e9175-691">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e9175-692">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e9175-692">Az.Automation</span></span>
* <span data-ttu-id="e9175-693">Uppdaterade Get-AzAutomationJobOutputRecord för att hantera postvärden av typen JSON och Text.</span><span class="sxs-lookup"><span data-stu-id="e9175-693">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="e9175-694">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="e9175-694">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="e9175-695">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="e9175-695">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="e9175-696">Ändrade beteende för Start-AzAutomationDscCompilationJob till att bara starta jobbet istället för att vänta på slutförandet.</span><span class="sxs-lookup"><span data-stu-id="e9175-696">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="e9175-697">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="e9175-697">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="e9175-698">Korrigering för Get-AzAutomationDscNode när using -Name returnerar alla noder.</span><span class="sxs-lookup"><span data-stu-id="e9175-698">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="e9175-699">Nu returnerar den endast den matchande noden.</span><span class="sxs-lookup"><span data-stu-id="e9175-699">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e9175-700">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e9175-700">Az.Compute</span></span>
* <span data-ttu-id="e9175-701">Lägg till parametrarna ProtectFromScaleIn och ProtectFromScaleSetAction i cmdleten Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="e9175-701">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="e9175-702">Nu är standardinställningen att vimpelparametern New-AzVM använder en tillgänglig plats om USA, östra inte stöds</span><span class="sxs-lookup"><span data-stu-id="e9175-702">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e9175-703">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e9175-703">Az.DataLakeStore</span></span>
* <span data-ttu-id="e9175-704">Uppdatera ADLS-sdk för att använda httpclient, integrera dataplanstestning med Azure-ramverk</span><span class="sxs-lookup"><span data-stu-id="e9175-704">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e9175-705">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e9175-705">Az.Monitor</span></span>
* <span data-ttu-id="e9175-706">Korrigera felaktiga parameternamn i hjälpexempel</span><span class="sxs-lookup"><span data-stu-id="e9175-706">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e9175-707">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e9175-707">Az.Network</span></span>
* <span data-ttu-id="e9175-708">Lägg till flaggan DisableBgpRoutePropagation i utdata för effektiv routningstabell</span><span class="sxs-lookup"><span data-stu-id="e9175-708">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="e9175-709">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="e9175-709">Updated cmdlet:</span></span>
        - <span data-ttu-id="e9175-710">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="e9175-710">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="e9175-711">Åtgärda dubbelstreck i dokumentationen New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="e9175-711">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="e9175-712">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e9175-712">Az.Resources</span></span>
* <span data-ttu-id="e9175-713">Lägg till ny cmdlet Get-AzureRmDenyAssignment för att hämta tilldelningsnekanden</span><span class="sxs-lookup"><span data-stu-id="e9175-713">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="e9175-714">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e9175-714">Az.Sql</span></span>
* <span data-ttu-id="e9175-715">Döp om Advanced Threat Protection-cmdletar för Advanced Data Security och aktivera Vulnerability Assessment som standard</span><span class="sxs-lookup"><span data-stu-id="e9175-715">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="e9175-716">2.0.0 – maj 2019</span><span class="sxs-lookup"><span data-stu-id="e9175-716">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e9175-717">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e9175-717">Az.Accounts</span></span>
* <span data-ttu-id="e9175-718">Uppdatera autentiseringsbiblioteket för att åtgärda ADFS-problem med autentisering av användarnamn/lösenord</span><span class="sxs-lookup"><span data-stu-id="e9175-718">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="e9175-719">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e9175-719">Az.CognitiveServices</span></span>
* <span data-ttu-id="e9175-720">Visa endast Bing-ansvarsfriskrivning för Bing-sökningstjänster.</span><span class="sxs-lookup"><span data-stu-id="e9175-720">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="e9175-721">Förbättra felmeddelande när det inte går att skapa konton.</span><span class="sxs-lookup"><span data-stu-id="e9175-721">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e9175-722">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e9175-722">Az.Compute</span></span>
* <span data-ttu-id="e9175-723">Funktion för närhetsplaceringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="e9175-723">Proximity placement group feature.</span></span>
    - <span data-ttu-id="e9175-724">Följande nya cmdletar har lagts till:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="e9175-724">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="e9175-725">Den nya parametern ProximityPlacementGroupId har lagts till i följande cmdletar:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="e9175-725">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="e9175-726">Parametern StorageAccountType har lagts till i New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="e9175-726">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="e9175-727">TargetRegion för New-AzGalleryImageVersion kan innehålla StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="e9175-727">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="e9175-728">Växlingsparametern SkipShutdown har lagts till i Stop-AzVM och Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e9175-728">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="e9175-729">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="e9175-729">Breaking changes</span></span>
    - <span data-ttu-id="e9175-730">Set-AzVMBootDiagnostics har ändrats till Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="e9175-730">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="e9175-731">Export-AzLogAnalyticThrottledRequests har ändrats till Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="e9175-731">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="e9175-732">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="e9175-732">Az.DeploymentManager</span></span>
* <span data-ttu-id="e9175-733">De första allmänt tillgängliga versionerna av cmdletar för Distributionshanteraren i Azure</span><span class="sxs-lookup"><span data-stu-id="e9175-733">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="e9175-734">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="e9175-734">Az.Dns</span></span>
* <span data-ttu-id="e9175-735">Automatisk delegering av DNS för NameServer</span><span class="sxs-lookup"><span data-stu-id="e9175-735">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="e9175-736">Det överordnade zonnamnet kan användas som ytterligare valfri parameter i cmdleten för att skapa DNS-zoner.</span><span class="sxs-lookup"><span data-stu-id="e9175-736">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="e9175-737">Lägger till NS-poster för en nyligen skapad underordnad zon i den överordnade zonen.</span><span class="sxs-lookup"><span data-stu-id="e9175-737">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="e9175-738">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="e9175-738">Az.FrontDoor</span></span>
* <span data-ttu-id="e9175-739">De första allmänt tillgängliga versionerna av cmdletar för Azure FrontDoor</span><span class="sxs-lookup"><span data-stu-id="e9175-739">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="e9175-740">Byt namn på WAF-cmdletar så att de omfattar ”Waf”</span><span class="sxs-lookup"><span data-stu-id="e9175-740">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="e9175-741">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="e9175-741">Az.HDInsight</span></span>
* <span data-ttu-id="e9175-742">Två cmdletar har tagits bort:</span><span class="sxs-lookup"><span data-stu-id="e9175-742">Removed two cmdlets:</span></span>
    - <span data-ttu-id="e9175-743">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="e9175-743">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="e9175-744">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="e9175-744">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="e9175-745">En ny cmdlet har lagts till, Set-AzHDInsightGatewayCredential, som ersätter Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="e9175-745">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="e9175-746">Uppdatera cmdleten Get-AzHDInsightJobOutput för att skilja mellan läsarrollen och HDInsight-operatörsrollen:</span><span class="sxs-lookup"><span data-stu-id="e9175-746">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="e9175-747">Användare med läsarrollen måste uttryckligen ange parametern ”DefaultStorageAccountKey”, annars uppstår fel.</span><span class="sxs-lookup"><span data-stu-id="e9175-747">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="e9175-748">Användare med HDInsight-operatörsrollen påverkas inte.</span><span class="sxs-lookup"><span data-stu-id="e9175-748">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e9175-749">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e9175-749">Az.Monitor</span></span>
* <span data-ttu-id="e9175-750">Nya cmdletar för SQR API (schemalagd frågeregel)</span><span class="sxs-lookup"><span data-stu-id="e9175-750">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="e9175-751">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="e9175-751">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="e9175-752">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="e9175-752">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="e9175-753">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="e9175-753">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="e9175-754">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="e9175-754">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="e9175-755">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="e9175-755">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="e9175-756">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="e9175-756">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="e9175-757">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="e9175-757">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="e9175-758">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="e9175-758">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="e9175-759">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="e9175-759">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="e9175-760">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="e9175-760">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="e9175-761">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="e9175-761">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="e9175-762">[Mer](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information om SQR API</span><span class="sxs-lookup"><span data-stu-id="e9175-762">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="e9175-763">Az.Monitor.md har uppdaterats för att omfatta cmdletar för måttbaserade aviseringsregler i GenV2 (inte klassiska)</span><span class="sxs-lookup"><span data-stu-id="e9175-763">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e9175-764">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e9175-764">Az.Network</span></span>
* <span data-ttu-id="e9175-765">Lägg till stöd för NAT Gateway-resurs</span><span class="sxs-lookup"><span data-stu-id="e9175-765">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="e9175-766">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="e9175-766">New cmdlets</span></span>
        - <span data-ttu-id="e9175-767">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="e9175-767">New-AzNatGateway</span></span>
        - <span data-ttu-id="e9175-768">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="e9175-768">Get-AzNatGateway</span></span>
        - <span data-ttu-id="e9175-769">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="e9175-769">Set-AzNatGateway</span></span>
        - <span data-ttu-id="e9175-770">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="e9175-770">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="e9175-771">Uppdaterade cmdletar</span><span class="sxs-lookup"><span data-stu-id="e9175-771">Updated cmdlets</span></span>
        - <span data-ttu-id="e9175-772">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="e9175-772">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="e9175-773">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="e9175-773">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="e9175-774">Nedanstående kommandon för funktionen har uppdaterats: Ange/ta bort anpassade vägar på Brooklyn Gateway.</span><span class="sxs-lookup"><span data-stu-id="e9175-774">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="e9175-775">New-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ställa in adressprefix som anpassade vägar för att ange gateway.</span><span class="sxs-lookup"><span data-stu-id="e9175-775">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="e9175-776">Set-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ange adressprefix som anpassade vägar för att ange gateway.</span><span class="sxs-lookup"><span data-stu-id="e9175-776">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="e9175-777">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="e9175-777">Az.PolicyInsights</span></span>
* <span data-ttu-id="e9175-778">Stöd för att fråga efter information om principutvärdering.</span><span class="sxs-lookup"><span data-stu-id="e9175-778">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="e9175-779">Lägg till parametern ”-Expand” för Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="e9175-779">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="e9175-780">Stöd för -Expand PolicyEvaluationDetails.</span><span class="sxs-lookup"><span data-stu-id="e9175-780">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e9175-781">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e9175-781">Az.RecoveryServices</span></span>
* <span data-ttu-id="e9175-782">Stöd för att dela prenumeration mellan Azure och Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="e9175-782">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="e9175-783">Markering av kommande icke-bakåtkompatibla ändringar för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="e9175-783">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="e9175-784">Korrigering för återställningsplan och åtgärdsplan i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="e9175-784">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="e9175-785">Korrigering för mappning av uppdateringsnätverk i Azure Site Recovery för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="e9175-785">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="e9175-786">Korrigering för instruktioner för uppdateringsskydd i Azure Site Recovery för Azure till Azure för hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="e9175-786">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="e9175-787">Andra mindre korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="e9175-787">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="e9175-788">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="e9175-788">Az.Relay</span></span>
* <span data-ttu-id="e9175-789">Korrigera stavfel i kundriktade meddelanden</span><span class="sxs-lookup"><span data-stu-id="e9175-789">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="e9175-790">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e9175-790">Az.ServiceBus</span></span>
* <span data-ttu-id="e9175-791">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="e9175-791">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e9175-792">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e9175-792">Az.Storage</span></span>
* <span data-ttu-id="e9175-793">Uppgradera till lagringsklientbiblioteket 10.0.1 (namnområdet för alla objekt från detta SDK ändras från ”Microsoft.WindowsAzure.Storage. *till ”Microsoft.Azure.Storage.* ”)</span><span class="sxs-lookup"><span data-stu-id="e9175-793">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="e9175-794">Uppgradera till Microsoft.Azure.Management.Storage 11.0.0 för att stödja den nya API-versionen 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="e9175-794">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="e9175-795">Standardlagringskontot i Skapa lagringskonto ändras från ”Storage” till ”StorageV2”</span><span class="sxs-lookup"><span data-stu-id="e9175-795">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="e9175-796">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e9175-796">New-AzStorageAccount</span></span>
* <span data-ttu-id="e9175-797">Ändra lagringskontots cmdlet-utdata Sku.Name för att passa med indata-SkuName genom att lägga till ”-”. Till exempel ändras ”StandardLRS” till ”Standard_LRS”</span><span class="sxs-lookup"><span data-stu-id="e9175-797">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="e9175-798">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e9175-798">New-AzStorageAccount</span></span>
    - <span data-ttu-id="e9175-799">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e9175-799">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="e9175-800">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e9175-800">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e9175-801">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e9175-801">Az.Websites</span></span>
* <span data-ttu-id="e9175-802">Egenskapen ”typ” konfigureras nu för PSSite-objekt som returneras av Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e9175-802">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="e9175-803">Get-AzWebApp\*Metrics och Get-AzAppServicePlanMetrics markeras som inaktuella</span><span class="sxs-lookup"><span data-stu-id="e9175-803">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="e9175-804">1.8.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="e9175-804">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="e9175-805">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="e9175-805">Highlights since the last major release</span></span>
* <span data-ttu-id="e9175-806">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="e9175-806">General availability of `Az` module</span></span>
* <span data-ttu-id="e9175-807">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="e9175-807">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="e9175-808">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="e9175-808">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="e9175-809">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="e9175-809">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="e9175-810">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="e9175-810">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="e9175-811">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="e9175-811">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="e9175-812">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="e9175-812">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="e9175-813">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e9175-813">Az.Accounts</span></span>
* <span data-ttu-id="e9175-814">Uppdatera Uninstall-AzureRm för att ta bort moduler i Mac på ett korrekt sätt</span><span class="sxs-lookup"><span data-stu-id="e9175-814">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="e9175-815">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="e9175-815">Az.Batch</span></span>
* <span data-ttu-id="e9175-816">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="e9175-816">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="e9175-817">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e9175-817">Az.Cdn</span></span>
* <span data-ttu-id="e9175-818">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="e9175-818">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="e9175-819">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e9175-819">Az.CognitiveServices</span></span>
* <span data-ttu-id="e9175-820">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="e9175-820">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e9175-821">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e9175-821">Az.Compute</span></span>
* <span data-ttu-id="e9175-822">Åtgärda problem med AEM-installationen om resurs-ID:n för diskar innehåller resourcegroups i gemener i resurs-ID:n</span><span class="sxs-lookup"><span data-stu-id="e9175-822">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="e9175-823">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="e9175-823">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e9175-824">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="e9175-824">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e9175-825">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e9175-825">Az.DataFactory</span></span>
* <span data-ttu-id="e9175-826">Lägg till SsisProperties om NodeCount inte är null för hanterad integreringskörning.</span><span class="sxs-lookup"><span data-stu-id="e9175-826">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e9175-827">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e9175-827">Az.DataLakeStore</span></span>
* <span data-ttu-id="e9175-828">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="e9175-828">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="e9175-829">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="e9175-829">Az.EventGrid</span></span>
* <span data-ttu-id="e9175-830">Hjälptexten för slutpunkten har uppdaterats för att visa att resurser ska skapas innan cmdletarna för att skapa/uppdatera händelseprenumerationer används.</span><span class="sxs-lookup"><span data-stu-id="e9175-830">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="e9175-831">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e9175-831">Az.EventHub</span></span>
* <span data-ttu-id="e9175-832">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="e9175-832">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="e9175-833">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="e9175-833">Az.HDInsight</span></span>
* <span data-ttu-id="e9175-834">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="e9175-834">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e9175-835">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e9175-835">Az.IotHub</span></span>
* <span data-ttu-id="e9175-836">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="e9175-836">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e9175-837">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e9175-837">Az.KeyVault</span></span>
* <span data-ttu-id="e9175-838">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="e9175-838">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e9175-839">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="e9175-839">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="e9175-840">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="e9175-840">Az.MachineLearning</span></span>
* <span data-ttu-id="e9175-841">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="e9175-841">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="e9175-842">Az.Media</span><span class="sxs-lookup"><span data-stu-id="e9175-842">Az.Media</span></span>
* <span data-ttu-id="e9175-843">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="e9175-843">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e9175-844">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e9175-844">Az.Monitor</span></span>
  * <span data-ttu-id="e9175-845">Nya cmdletar för måttbaserad aviseringsregel i GenV2 (inte klassisk)</span><span class="sxs-lookup"><span data-stu-id="e9175-845">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="e9175-846">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="e9175-846">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="e9175-847">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="e9175-847">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="e9175-848">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="e9175-848">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="e9175-849">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="e9175-849">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="e9175-850">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="e9175-850">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="e9175-851">Monitor SDK har uppdaterats till version 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="e9175-851">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e9175-852">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e9175-852">Az.Network</span></span>
* <span data-ttu-id="e9175-853">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="e9175-853">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e9175-854">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="e9175-854">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="e9175-855">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="e9175-855">Az.NotificationHubs</span></span>
* <span data-ttu-id="e9175-856">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="e9175-856">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e9175-857">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e9175-857">Az.OperationalInsights</span></span>
* <span data-ttu-id="e9175-858">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="e9175-858">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="e9175-859">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="e9175-859">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="e9175-860">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="e9175-860">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e9175-861">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e9175-861">Az.RecoveryServices</span></span>
* <span data-ttu-id="e9175-862">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="e9175-862">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e9175-863">Tabellformatet för SQL i virtuella Azure-datorer har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="e9175-863">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="e9175-864">En alternativ metod för att hämta platser i AzureFileShare har lagts till</span><span class="sxs-lookup"><span data-stu-id="e9175-864">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="e9175-865">ScheduleRunDays i SchedulePolicy-objekt har uppdaterats enligt tidszon</span><span class="sxs-lookup"><span data-stu-id="e9175-865">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="e9175-866">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="e9175-866">Az.RedisCache</span></span>
* <span data-ttu-id="e9175-867">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="e9175-867">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e9175-868">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e9175-868">Az.Resources</span></span>
* <span data-ttu-id="e9175-869">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="e9175-869">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="e9175-870">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e9175-870">Az.Sql</span></span>
* <span data-ttu-id="e9175-871">Ersätt Monitor SDK-beroende med vanlig kod</span><span class="sxs-lookup"><span data-stu-id="e9175-871">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="e9175-872">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="e9175-872">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e9175-873">Förbättrad process för klassificering av flera kolumner.</span><span class="sxs-lookup"><span data-stu-id="e9175-873">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="e9175-874">Inkludera SKU-egenskaper (SKU-namn, serie, kapacitet) i svaret från Get-AzSqlServerServiceObjective och formatera som tabell som standard.</span><span class="sxs-lookup"><span data-stu-id="e9175-874">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="e9175-875">Möjlighet att använda Get-AzSqlServerServiceObjective efter plats utan att behöva en redan befintlig server i regionen.</span><span class="sxs-lookup"><span data-stu-id="e9175-875">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="e9175-876">Stöd för tidszonsparametern när hanterade instanser skapas.</span><span class="sxs-lookup"><span data-stu-id="e9175-876">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="e9175-877">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="e9175-877">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e9175-878">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e9175-878">Az.Websites</span></span>
* <span data-ttu-id="e9175-879">åtgärdar Set-AzWebApp och Set-AzWebAppSlot så att de inte tar bort taggar vid körning</span><span class="sxs-lookup"><span data-stu-id="e9175-879">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="e9175-880">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="e9175-880">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e9175-881">SDK för WebSites har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="e9175-881">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="e9175-882">Egenskapen AdminSiteName har tagits bort från PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="e9175-882">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="e9175-883">1.7.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="e9175-883">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="e9175-884">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="e9175-884">Highlights since the last major release</span></span>
* <span data-ttu-id="e9175-885">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="e9175-885">General availability of `Az` module</span></span>
* <span data-ttu-id="e9175-886">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="e9175-886">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="e9175-887">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="e9175-887">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="e9175-888">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="e9175-888">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="e9175-889">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="e9175-889">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="e9175-890">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="e9175-890">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="e9175-891">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="e9175-891">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="e9175-892">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e9175-892">Az.Accounts</span></span>
* <span data-ttu-id="e9175-893">Add-AzEnvironment och Set-AzEnvironment har uppdaterats för att godkänna parametern AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="e9175-893">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="e9175-894">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e9175-894">Az.AnalysisServices</span></span>
* <span data-ttu-id="e9175-895">ServiceClient används i cmdletar för dataplan och den ursprungliga autentiseringslogiken har tagits bort</span><span class="sxs-lookup"><span data-stu-id="e9175-895">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="e9175-896">Add-AzureASAccount används för omslutning av Connect-AzAccount för att undvika en icke-bakåtkompatibel ändring</span><span class="sxs-lookup"><span data-stu-id="e9175-896">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e9175-897">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e9175-897">Az.Automation</span></span>
* <span data-ttu-id="e9175-898">Buggen för cmdleten New-AzAutomationSoftwareUpdateConfiguration för inkluderingar har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="e9175-898">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="e9175-899">Nu bör parametern IncludedKbNumber och IncludedPackageNameMask fungera.</span><span class="sxs-lookup"><span data-stu-id="e9175-899">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="e9175-900">Felkorrigering för dynamiska grupper i uppdateringshanteringen för azure automation</span><span class="sxs-lookup"><span data-stu-id="e9175-900">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e9175-901">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e9175-901">Az.Compute</span></span>
* <span data-ttu-id="e9175-902">Lägg till parametern HyperVGeneration i New-AzDiskConfig och New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="e9175-902">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="e9175-903">Tillåt att virtuella datorer skapas med galleribilder från andra klientorganisationer.</span><span class="sxs-lookup"><span data-stu-id="e9175-903">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="e9175-904">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="e9175-904">Az.ContainerInstance</span></span>
* <span data-ttu-id="e9175-905">Ett problem har åtgärdats i parametern -Command för New-AzContainerGroup som lade till ett avslutande tomt argument</span><span class="sxs-lookup"><span data-stu-id="e9175-905">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e9175-906">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e9175-906">Az.DataFactory</span></span>
* <span data-ttu-id="e9175-907">ADF .Net SDK-versionen har uppdaterats till 3.0.2</span><span class="sxs-lookup"><span data-stu-id="e9175-907">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="e9175-908">Cmdleten Set-AzDataFactoryV2 har uppdaterats med extra parametrar för inställningar som rör RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="e9175-908">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e9175-909">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e9175-909">Az.Resources</span></span>
* <span data-ttu-id="e9175-910">Förbättra hanteringen av providrar för Get-AzResource när parametrarna -ResourceId eller -ResourceGroupName, -Name och -ResourceType tillhandahålls</span><span class="sxs-lookup"><span data-stu-id="e9175-910">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="e9175-911">Förbättra felhanteringen för ”Test-AzDeployment” och ”Test-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="e9175-911">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="e9175-912">Hantera fel utanför distributionsvalideringen och ta med dem i kommandoutdata istället</span><span class="sxs-lookup"><span data-stu-id="e9175-912">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="e9175-913">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="e9175-913">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="e9175-914">Lägg till växlingsparametern -IgnoreDynamicParameters till en uppsättning av cmdletar för distribution för att hoppa över fråga i skript och jobbscenarier</span><span class="sxs-lookup"><span data-stu-id="e9175-914">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="e9175-915">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="e9175-915">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="e9175-916">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e9175-916">Az.Sql</span></span>
* <span data-ttu-id="e9175-917">Stöd för dataklassificering av databaser.</span><span class="sxs-lookup"><span data-stu-id="e9175-917">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e9175-918">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e9175-918">Az.Storage</span></span>
* <span data-ttu-id="e9175-919">Rapportera detaljfel när lagringskontext skapas med parametern -UseConnectedAccount, men utan inloggning på Azure-kontot</span><span class="sxs-lookup"><span data-stu-id="e9175-919">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="e9175-920">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="e9175-920">New-AzStorageContext</span></span>
* <span data-ttu-id="e9175-921">Stöd för att hantera Blob Service-egenskaper för ett angivet lagringskonto med API:et för hanteringsplan</span><span class="sxs-lookup"><span data-stu-id="e9175-921">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="e9175-922">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="e9175-922">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="e9175-923">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="e9175-923">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="e9175-924">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="e9175-924">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="e9175-925">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="e9175-925">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="e9175-926">Stöd för -AsJob-cmdletar för att ladda upp och ladda ned blobar och filer</span><span class="sxs-lookup"><span data-stu-id="e9175-926">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="e9175-927">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="e9175-927">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="e9175-928">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="e9175-928">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="e9175-929">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="e9175-929">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="e9175-930">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="e9175-930">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="e9175-931">1.6.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="e9175-931">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="e9175-932">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="e9175-932">Highlights since the last major release</span></span>
* <span data-ttu-id="e9175-933">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="e9175-933">General availability of `Az` module</span></span>
* <span data-ttu-id="e9175-934">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="e9175-934">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="e9175-935">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="e9175-935">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="e9175-936">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="e9175-936">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="e9175-937">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="e9175-937">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="e9175-938">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="e9175-938">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="e9175-939">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="e9175-939">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e9175-940">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e9175-940">Az.Automation</span></span>
* <span data-ttu-id="e9175-941">Azure Automation – ändring av uppdateringshantering för stöd för de nya funktionerna:</span><span class="sxs-lookup"><span data-stu-id="e9175-941">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="e9175-942">Dynamisk gruppering</span><span class="sxs-lookup"><span data-stu-id="e9175-942">Dynamic grouping</span></span>
    * <span data-ttu-id="e9175-943">För-/efterskrift</span><span class="sxs-lookup"><span data-stu-id="e9175-943">Pre-Post script</span></span>
    * <span data-ttu-id="e9175-944">Inställning för omstart</span><span class="sxs-lookup"><span data-stu-id="e9175-944">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e9175-945">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e9175-945">Az.Compute</span></span>
* <span data-ttu-id="e9175-946">Åtgärda problem med sökvägsmatchning i Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="e9175-946">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="e9175-947">Uppdatera Compute-klientbibliotek till 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="e9175-947">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e9175-948">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e9175-948">Az.KeyVault</span></span>
* <span data-ttu-id="e9175-949">Stöd för jokertecken för KeyVault-cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="e9175-949">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e9175-950">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e9175-950">Az.Network</span></span>
* <span data-ttu-id="e9175-951">Lägg till stöd för Threat Intelligence för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="e9175-951">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="e9175-952">Lägg till resurs för brandväggsprincip på översta nivå och anpassade regler för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="e9175-952">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e9175-953">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e9175-953">Az.RecoveryServices</span></span>
* <span data-ttu-id="e9175-954">SnapshotRetentionInDays har lagts till i Azure-principen för virtuella datorer för stöd av Instant RP</span><span class="sxs-lookup"><span data-stu-id="e9175-954">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="e9175-955">Pipe-stöd för avregistrering av container har lagts till</span><span class="sxs-lookup"><span data-stu-id="e9175-955">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="e9175-956">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e9175-956">Az.Resources</span></span>
* <span data-ttu-id="e9175-957">Uppdatera stöd för jokertecken för Get-AzResource och Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e9175-957">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="e9175-958">Uppdatera autentiseringsuppgifter som används vid allmänna anrop till ARM</span><span class="sxs-lookup"><span data-stu-id="e9175-958">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="e9175-959">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e9175-959">Az.Sql</span></span>
* <span data-ttu-id="e9175-960">Cmdlet-parametern (ExcludeDetectionType) för Hotidentifiering ändrades från DetectionType till sträng[] för att framtidssäkra den när nya DetectionTypes läggs till, och även för att stödja automatisk ifyllning.</span><span class="sxs-lookup"><span data-stu-id="e9175-960">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e9175-961">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e9175-961">Az.Storage</span></span>
* <span data-ttu-id="e9175-962">Stöd för att hämta/ange/ta bort hanteringsprincip på ett lagringskonto</span><span class="sxs-lookup"><span data-stu-id="e9175-962">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="e9175-963">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="e9175-963">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="e9175-964">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="e9175-964">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="e9175-965">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="e9175-965">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="e9175-966">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="e9175-966">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="e9175-967">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="e9175-967">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="e9175-968">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="e9175-968">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e9175-969">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e9175-969">Az.Websites</span></span>
* <span data-ttu-id="e9175-970">Åtgärda fel med ARM-mall som avbryter kloning av alla platser med 'New-AzWebApp -IncludeSourceWebAppSlots'</span><span class="sxs-lookup"><span data-stu-id="e9175-970">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="e9175-971">1.5.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="e9175-971">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e9175-972">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e9175-972">Az.Accounts</span></span>
* <span data-ttu-id="e9175-973">Lägg till kommandot Register-AzModule för stöd för AutoRest-genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="e9175-973">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="e9175-974">Uppdatera exempel för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="e9175-974">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e9175-975">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e9175-975">Az.Automation</span></span>
* <span data-ttu-id="e9175-976">Problem med att hämta vissa månadsscheman i flera Azure Automation-cmdletar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="e9175-976">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="e9175-977">Åtgärda problem med att Get-AzAutomationDscNode bara returnerar de 20 översta noderna.</span><span class="sxs-lookup"><span data-stu-id="e9175-977">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="e9175-978">Nu returneras alla noder</span><span class="sxs-lookup"><span data-stu-id="e9175-978">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="e9175-979">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e9175-979">Az.Cdn</span></span>
* <span data-ttu-id="e9175-980">Nya Powershell-cmdletar för att aktivera/inaktivera anpassade domän-HTTPS har lagts till och de gamla har gjorts inaktuella</span><span class="sxs-lookup"><span data-stu-id="e9175-980">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e9175-981">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e9175-981">Az.Compute</span></span>
* <span data-ttu-id="e9175-982">Lägg till stöd för jokertecken för Get-cmdletar</span><span class="sxs-lookup"><span data-stu-id="e9175-982">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e9175-983">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e9175-983">Az.DataFactory</span></span>
* <span data-ttu-id="e9175-984">ADF .Net SDK-versionen har uppdaterats till 3.0.1</span><span class="sxs-lookup"><span data-stu-id="e9175-984">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="e9175-985">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="e9175-985">Az.LogicApp</span></span>
* <span data-ttu-id="e9175-986">Åtgärda problemet med att ListWorkflows endast hämtar den första sidan med resultat</span><span class="sxs-lookup"><span data-stu-id="e9175-986">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e9175-987">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e9175-987">Az.Network</span></span>
* <span data-ttu-id="e9175-988">Lägg till stöd för jokertecken för Network-cmdletar</span><span class="sxs-lookup"><span data-stu-id="e9175-988">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e9175-989">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e9175-989">Az.RecoveryServices</span></span>
* <span data-ttu-id="e9175-990">Stöd har lagts till för SQL Server i virtuella Azure-datorer</span><span class="sxs-lookup"><span data-stu-id="e9175-990">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="e9175-991">SDK-uppdatering</span><span class="sxs-lookup"><span data-stu-id="e9175-991">SDK Update</span></span>
* <span data-ttu-id="e9175-992">Get-ProtectableItem-incheckning i VMappContainer har tagits bort</span><span class="sxs-lookup"><span data-stu-id="e9175-992">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="e9175-993">Name och ServerName har lagts till som parametrar för Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="e9175-993">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="e9175-994">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e9175-994">Az.Resources</span></span>
* <span data-ttu-id="e9175-995">Lägg till parametern `-TemplateObject` i cmdletar för distribution</span><span class="sxs-lookup"><span data-stu-id="e9175-995">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="e9175-996">Mer information här: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="e9175-996">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="e9175-997">Åtgärda problem med piping av resultatet i `Get-AzResource` till `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="e9175-997">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="e9175-998">Mer information här: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="e9175-998">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="e9175-999">Åtgärda problem med ändring av JSON-datatyp när `Set-AzResource` körs</span><span class="sxs-lookup"><span data-stu-id="e9175-999">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="e9175-1000">Mer information här: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="e9175-1000">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="e9175-1001">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e9175-1001">Az.Sql</span></span>
* <span data-ttu-id="e9175-1002">AuditingEndpointsCommunicator uppdateras.</span><span class="sxs-lookup"><span data-stu-id="e9175-1002">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="e9175-1003">Åtgärdar beteendet hos ett gränsscenario när nya diagnostikinställningar skapas.</span><span class="sxs-lookup"><span data-stu-id="e9175-1003">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e9175-1004">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e9175-1004">Az.Storage</span></span>
* <span data-ttu-id="e9175-1005">Stöd för BlockBlobStorage när Storage-konto skapas      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e9175-1005">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="e9175-1006">1.4.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="e9175-1006">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="e9175-1007">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e9175-1007">Az.AnalysisServices</span></span>
* <span data-ttu-id="e9175-1008">Inaktuell AddAzureASAccount-cmdlet</span><span class="sxs-lookup"><span data-stu-id="e9175-1008">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e9175-1009">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e9175-1009">Az.Automation</span></span>
* <span data-ttu-id="e9175-1010">Hjälpen för Import-AzAutomationDscNodeConfiguration har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="e9175-1010">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="e9175-1011">Konfigurationsnamnsvalidering har lagts till i cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="e9175-1011">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="e9175-1012">Förbättrad felhantering för cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="e9175-1012">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="e9175-1013">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e9175-1013">Az.CognitiveServices</span></span>
* <span data-ttu-id="e9175-1014">CustomSubdomainName har lagts till som en ny valfri parameter för New-AzCognitiveServicesAccount, som används för att ange underdomän för resursen.</span><span class="sxs-lookup"><span data-stu-id="e9175-1014">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e9175-1015">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e9175-1015">Az.Compute</span></span>
* <span data-ttu-id="e9175-1016">Problemet med ID-parameteruppsättningar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="e9175-1016">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="e9175-1017">Get-AzVMExtension har uppdaterats så att alla installerade tillägg visas om parametern Name inte har angetts</span><span class="sxs-lookup"><span data-stu-id="e9175-1017">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="e9175-1018">Parametrarna Tag och ResourceId har lagts till i cmdleten Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="e9175-1018">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="e9175-1019">Get-AzVmssVM utan instans-ID och med InstanceView kan visa virtuella VMSS-datorer med instansvyn.</span><span class="sxs-lookup"><span data-stu-id="e9175-1019">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e9175-1020">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e9175-1020">Az.DataLakeStore</span></span>
* <span data-ttu-id="e9175-1021">Cmdletar har lagts till för uppräkning och återställning av borttagna objekt i ADL</span><span class="sxs-lookup"><span data-stu-id="e9175-1021">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="e9175-1022">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e9175-1022">Az.EventHub</span></span>
* <span data-ttu-id="e9175-1023">Ny boolesk egenskap SkipEmptyArchives har lagts till i Skip Empty Archives i CaptureDescription-klassen i Eventhub</span><span class="sxs-lookup"><span data-stu-id="e9175-1023">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="e9175-1024">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e9175-1024">Az.KeyVault</span></span>
* <span data-ttu-id="e9175-1025">Taggning i Set-AzKeyVaultSecret har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="e9175-1025">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="e9175-1026">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="e9175-1026">Az.LogicApp</span></span>
* <span data-ttu-id="e9175-1027">Grundläggande SKU har lagts till för Integrationskonton</span><span class="sxs-lookup"><span data-stu-id="e9175-1027">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="e9175-1028">XSLT 2.0, XSLT 3.0 och Flytande mappningstyper har lagts till</span><span class="sxs-lookup"><span data-stu-id="e9175-1028">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="e9175-1029">Nya cmdletar för integrationskontosammansättningar</span><span class="sxs-lookup"><span data-stu-id="e9175-1029">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="e9175-1030">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="e9175-1030">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="e9175-1031">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="e9175-1031">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="e9175-1032">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="e9175-1032">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="e9175-1033">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="e9175-1033">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="e9175-1034">Nya cmdletar för batchkonfiguration för integrationskonto</span><span class="sxs-lookup"><span data-stu-id="e9175-1034">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="e9175-1035">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="e9175-1035">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="e9175-1036">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="e9175-1036">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="e9175-1037">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="e9175-1037">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="e9175-1038">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="e9175-1038">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="e9175-1039">Logic App-SDK har uppdaterats till version 4.1.0</span><span class="sxs-lookup"><span data-stu-id="e9175-1039">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e9175-1040">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e9175-1040">Az.Monitor</span></span>
* <span data-ttu-id="e9175-1041">Hjälpen för Get-AzMetric har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="e9175-1041">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e9175-1042">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e9175-1042">Az.Network</span></span>
* <span data-ttu-id="e9175-1043">Hjälpexempel för Add-AzApplicationGatewayCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="e9175-1043">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e9175-1044">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e9175-1044">Az.OperationalInsights</span></span>
* <span data-ttu-id="e9175-1045">Ytterligare stöd för datakällorna New och Get ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="e9175-1045">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="e9175-1046">Ny ApplicationInsights-typ har lagts till för att ge stöd för ”Get specific” och ”Get all” för ApplicationInsights-datakällor för angiven arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="e9175-1046">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="e9175-1047">Cmdleten New-AzOperationalInsightsApplicationInsightsDataSource har lagts till för att skapa datakälla med angivna parametrar för Application Insights-resurs: subscription Id, resourceGroupName och name.</span><span class="sxs-lookup"><span data-stu-id="e9175-1047">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="e9175-1048">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e9175-1048">Az.Resources</span></span>
* <span data-ttu-id="e9175-1049">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="e9175-1049">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="e9175-1050">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="e9175-1050">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="e9175-1051">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="e9175-1051">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="e9175-1052">Fel som gör att KeyCredentials inte kan skapas upprepade gånger har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="e9175-1052">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="e9175-1053">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e9175-1053">Az.Sql</span></span>
* <span data-ttu-id="e9175-1054">Lägg till stöd för hyperskalanivån för SQL DB</span><span class="sxs-lookup"><span data-stu-id="e9175-1054">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="e9175-1055">Ett fel har åtgärdats där återställningen kunde misslyckas på grund av onödiga inställningsegenskaper i restore-förfrågan</span><span class="sxs-lookup"><span data-stu-id="e9175-1055">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e9175-1056">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e9175-1056">Az.Websites</span></span>
* <span data-ttu-id="e9175-1057">Rätt exempel i Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="e9175-1057">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="e9175-1058">1.3.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="e9175-1058">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e9175-1059">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e9175-1059">Az.Accounts</span></span>
* <span data-ttu-id="e9175-1060">Uppdatera till den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="e9175-1060">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="e9175-1061">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e9175-1061">Az.AnalysisServices</span></span>
<span data-ttu-id="e9175-1062">Allmän tillgänglighet för Az.AnalysisServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="e9175-1062">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e9175-1063">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e9175-1063">Az.Compute</span></span>
* <span data-ttu-id="e9175-1064">AEM-tillägg: Lägg till stöd för UltraSSD-, P60-, P70- och P80-diskar</span><span class="sxs-lookup"><span data-stu-id="e9175-1064">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="e9175-1065">Uppdatera hjälpbeskrivning för Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="e9175-1065">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="e9175-1066">Uppdatera hjälpbeskrivning och exempel för Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="e9175-1066">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e9175-1067">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e9175-1067">Az.RecoveryServices</span></span>
<span data-ttu-id="e9175-1068">Allmän tillgänglighet för Az.RecoveryServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="e9175-1068">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e9175-1069">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e9175-1069">Az.Resources</span></span>
* <span data-ttu-id="e9175-1070">Korrigera taggar för resursgrupper</span><span class="sxs-lookup"><span data-stu-id="e9175-1070">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="e9175-1071">Mer information här: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="e9175-1071">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="e9175-1072">Åtgärda problem där `Get-AzureRmRoleAssignment` inte respekterar -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="e9175-1072">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="e9175-1073">Mer information här: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="e9175-1073">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="e9175-1074">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e9175-1074">Az.Sql</span></span>
* <span data-ttu-id="e9175-1075">Lägga till Get/Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="e9175-1075">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="e9175-1076">Åtgärda problem där ett nullref-undantag uppstår när du kör SQL-cmdletar och inte är inloggad på ett Azure-konto</span><span class="sxs-lookup"><span data-stu-id="e9175-1076">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="e9175-1077">Åtgärda nullref-undantag i Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="e9175-1077">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="e9175-1078">1.2.1 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="e9175-1078">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e9175-1079">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e9175-1079">Az.Accounts</span></span>
* <span data-ttu-id="e9175-1080">Version med rätt version av autentisering</span><span class="sxs-lookup"><span data-stu-id="e9175-1080">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="e9175-1081">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e9175-1081">Az.AnalysisServices</span></span>
* <span data-ttu-id="e9175-1082">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="e9175-1082">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e9175-1083">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e9175-1083">Az.RecoveryServices</span></span>
* <span data-ttu-id="e9175-1084">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="e9175-1084">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="e9175-1085">1.2.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="e9175-1085">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e9175-1086">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e9175-1086">Az.Accounts</span></span>
* <span data-ttu-id="e9175-1087">Lägga till interaktiv autentisering och autentisering med användarnamn/lösenord för endast Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="e9175-1087">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="e9175-1088">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="e9175-1088">Update incorrect online help URLs</span></span>
* <span data-ttu-id="e9175-1089">Lägga till varningsmeddelande i PS Core för Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="e9175-1089">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="e9175-1090">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="e9175-1090">Az.Aks</span></span>
* <span data-ttu-id="e9175-1091">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="e9175-1091">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e9175-1092">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e9175-1092">Az.Automation</span></span>
* <span data-ttu-id="e9175-1093">Stöd för Python 2-runbookflöden har lagts till</span><span class="sxs-lookup"><span data-stu-id="e9175-1093">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="e9175-1094">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="e9175-1094">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="e9175-1095">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e9175-1095">Az.Cdn</span></span>
* <span data-ttu-id="e9175-1096">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="e9175-1096">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e9175-1097">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e9175-1097">Az.Compute</span></span>
* <span data-ttu-id="e9175-1098">Lägga till cmdleten Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="e9175-1098">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="e9175-1099">Lägga till TempDisk-parameter i Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e9175-1099">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="e9175-1100">Korrigera varningsmeddelande för New-AzVM</span><span class="sxs-lookup"><span data-stu-id="e9175-1100">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="e9175-1101">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e9175-1101">Az.ContainerRegistry</span></span>
* <span data-ttu-id="e9175-1102">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="e9175-1102">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e9175-1103">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e9175-1103">Az.DataFactory</span></span>
* <span data-ttu-id="e9175-1104">ADF .Net SDK-versionen har uppdaterats till 3.0.0</span><span class="sxs-lookup"><span data-stu-id="e9175-1104">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e9175-1105">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e9175-1105">Az.DataLakeStore</span></span>
* <span data-ttu-id="e9175-1106">Åtgärda problem med ADLS-slutpunkt vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="e9175-1106">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="e9175-1107">Mer information här: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="e9175-1107">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="e9175-1108">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="e9175-1108">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e9175-1109">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e9175-1109">Az.IotHub</span></span>
* <span data-ttu-id="e9175-1110">Lägga till kodningsformat i cmdleten Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="e9175-1110">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e9175-1111">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e9175-1111">Az.KeyVault</span></span>
* <span data-ttu-id="e9175-1112">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="e9175-1112">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e9175-1113">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e9175-1113">Az.Network</span></span>
* <span data-ttu-id="e9175-1114">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="e9175-1114">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="e9175-1115">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e9175-1115">Az.Resources</span></span>
* <span data-ttu-id="e9175-1116">Åtgärda felaktiga exempel i referensdokumentationen ”New-AzADAppCredential” och ”New-AzADSpCredential”</span><span class="sxs-lookup"><span data-stu-id="e9175-1116">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="e9175-1117">Åtgärda problem där sökvägen för parametern ”-TemplateFile” inte omvandlas innan cmdletarna för distribution i resursgruppen körs</span><span class="sxs-lookup"><span data-stu-id="e9175-1117">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="e9175-1118">Az.Resources: Korrigera dokumentationen om standardvärdet för New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="e9175-1118">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="e9175-1119">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="e9175-1119">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="e9175-1120">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="e9175-1120">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="e9175-1121">Åtgärda formateringsproblemet med objektet ”PSResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="e9175-1121">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="e9175-1122">Mer information här: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="e9175-1122">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e9175-1123">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e9175-1123">Az.ServiceFabric</span></span>
* <span data-ttu-id="e9175-1124">Återställ när ett certifikat läggs till i en Virtual Machine Scale Sets-modell men ett undantag genereras. Detta har gjorts för att åtgärda följande fel: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="e9175-1124">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="e9175-1125">Korrigera några felmeddelanden.</span><span class="sxs-lookup"><span data-stu-id="e9175-1125">Fix some error messages.</span></span>
* <span data-ttu-id="e9175-1126">Korrigering av skapande av kluster med ARM-mall som är standard för New-AzServiceFabriCluster som inte fungerade med migrering till Az.</span><span class="sxs-lookup"><span data-stu-id="e9175-1126">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="e9175-1127">Korrigering av tilläggning av kluster/programcertifikat så att endast VM Scale Sets som motsvarar klustret läggs till genom att kontrollera ID för klustret i tillägget.</span><span class="sxs-lookup"><span data-stu-id="e9175-1127">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="e9175-1128">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="e9175-1128">Az.SignalR</span></span>
* <span data-ttu-id="e9175-1129">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="e9175-1129">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="e9175-1130">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e9175-1130">Az.Sql</span></span>
* <span data-ttu-id="e9175-1131">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="e9175-1131">Update incorrect online help URLs</span></span>
* <span data-ttu-id="e9175-1132">Uppdaterad parameterbeskrivning för LicenseType-parameter med möjliga värden</span><span class="sxs-lookup"><span data-stu-id="e9175-1132">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="e9175-1133">Korrigering för att uppdatera hanterad instansidentitet som inte fungerar när det är den enda uppdaterade egenskapen</span><span class="sxs-lookup"><span data-stu-id="e9175-1133">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="e9175-1134">Stöd för anpassad sortering på hanterad instans</span><span class="sxs-lookup"><span data-stu-id="e9175-1134">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e9175-1135">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e9175-1135">Az.Storage</span></span>
* <span data-ttu-id="e9175-1136">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="e9175-1136">Update incorrect online help URLs</span></span>
* <span data-ttu-id="e9175-1137">Tillhandahåll detaljerat felmeddelande när en användare försöker hämta/konfigurera klassisk loggning/mått på ett Premium Storage-konto eftersom Premium Storage-kontot inte har stöd för klassisk loggning/mått.</span><span class="sxs-lookup"><span data-stu-id="e9175-1137">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="e9175-1138">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="e9175-1138">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="e9175-1139">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="e9175-1139">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="e9175-1140">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="e9175-1140">Az.TrafficManager</span></span>
* <span data-ttu-id="e9175-1141">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="e9175-1141">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e9175-1142">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e9175-1142">Az.Websites</span></span>
* <span data-ttu-id="e9175-1143">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="e9175-1143">Update incorrect online help URLs</span></span>
* <span data-ttu-id="e9175-1144">Korrigerar ”New-AzWebAppSSLBinding” så att certifikatet laddas upp till rätt resursgrupp och plats om appen finns i en ASE.</span><span class="sxs-lookup"><span data-stu-id="e9175-1144">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="e9175-1145">Korrigerar ”New-AzWebAppSSLBinding” så att taggarna inte skrivs över på en bindning av ett SSL-certifikat till en app</span><span class="sxs-lookup"><span data-stu-id="e9175-1145">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="e9175-1146">1.1.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="e9175-1146">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e9175-1147">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e9175-1147">Az.Accounts</span></span>
* <span data-ttu-id="e9175-1148">Lade till omfattningen ”Lokal” till Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="e9175-1148">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e9175-1149">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e9175-1149">Az.Compute</span></span>
* <span data-ttu-id="e9175-1150">Namn är nu valfritt i ID-parametern för Restart/Start/Stop/Remove/Set-AzVM och Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="e9175-1150">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="e9175-1151">Uppdaterade beskrivningen av ID i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="e9175-1151">Updated the description of ID in help files</span></span>
* <span data-ttu-id="e9175-1152">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e9175-1152">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e9175-1153">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e9175-1153">Az.DataLakeStore</span></span>
* <span data-ttu-id="e9175-1154">Uppdatera sdk-versionen av dataplanet till 1.1.14 för SDK-korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="e9175-1154">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="e9175-1155">Korrigerade hanteringen av negativ accesstime och modificationtime för getfilestatus och liststatus; korrigera asynkront annulleringstoken</span><span class="sxs-lookup"><span data-stu-id="e9175-1155">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="e9175-1156">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="e9175-1156">Az.EventGrid</span></span>
* <span data-ttu-id="e9175-1157">Uppdaterat för användning av API-versionen 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="e9175-1157">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="e9175-1158">Uppdaterade följande cmdletar för att stödja nytt scenario i API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="e9175-1158">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="e9175-1159">New-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="e9175-1159">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="e9175-1160">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="e9175-1160">Event Time-To-Live,</span></span>
        - <span data-ttu-id="e9175-1161">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="e9175-1161">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="e9175-1162">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="e9175-1162">Dead letter endpoint.</span></span>
    - <span data-ttu-id="e9175-1163">Update-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="e9175-1163">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="e9175-1164">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="e9175-1164">Event Time-To-Live,</span></span>
        - <span data-ttu-id="e9175-1165">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="e9175-1165">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="e9175-1166">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="e9175-1166">Dead letter endpoint.</span></span>
* <span data-ttu-id="e9175-1167">Lade till nya enum-värden (storageQueue och hybridConnection) för alternativet EndpointType i cmdletarna New-AzureRmEventGridSubscription och Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="e9175-1167">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="e9175-1168">Visa varningsmeddelanden om skapande eller uppdatering av händelseprenumerationen förväntas medföra manuell åtgärd från användaren.</span><span class="sxs-lookup"><span data-stu-id="e9175-1168">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e9175-1169">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e9175-1169">Az.IotHub</span></span>
* <span data-ttu-id="e9175-1170">Har uppdaterats till den senaste versionen av SDK:n lotHub</span><span class="sxs-lookup"><span data-stu-id="e9175-1170">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="e9175-1171">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="e9175-1171">Az.LogicApp</span></span>
* <span data-ttu-id="e9175-1172">Get-AzLogicApp visar en lista över alla som inte har angivet namn</span><span class="sxs-lookup"><span data-stu-id="e9175-1172">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="e9175-1173">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e9175-1173">Az.Resources</span></span>
* <span data-ttu-id="e9175-1174">Åtgärdade problem med parameteruppsättningen när parametrarna -ODataQuery och -ResourceId anges för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="e9175-1174">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="e9175-1175">Mer information här: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="e9175-1175">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="e9175-1176">Åtgärdade hantering av parametern -Custom i New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e9175-1176">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="e9175-1177">Korrigerade stavfel i New-AzDeployment-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="e9175-1177">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="e9175-1178">Gjorde parametern -MailNickname obligatorisk för New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="e9175-1178">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="e9175-1179">Mer information här: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="e9175-1179">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="e9175-1180">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="e9175-1180">Az.SignalR</span></span>
* <span data-ttu-id="e9175-1181">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e9175-1181">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="e9175-1182">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e9175-1182">Az.Sql</span></span>
* <span data-ttu-id="e9175-1183">Konverterade lagringshanteringsklientens beroende av den normala SDK-implementeringen.</span><span class="sxs-lookup"><span data-stu-id="e9175-1183">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e9175-1184">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e9175-1184">Az.Storage</span></span>
* <span data-ttu-id="e9175-1185">Angav StorageAccountName för lagringskontext som det verkliga namnet på lagringskontot när det skapas med Sas Token, OAuth eller Anonymous</span><span class="sxs-lookup"><span data-stu-id="e9175-1185">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="e9175-1186">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="e9175-1186">New-AzStorageContext</span></span>
* <span data-ttu-id="e9175-1187">Skapade Sas Token för Blob Snapshot-objekt med parametern -FullUri, åtgärdade den returnerade URI:n så att den blir URI för ögonblicksbild</span><span class="sxs-lookup"><span data-stu-id="e9175-1187">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="e9175-1188">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="e9175-1188">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e9175-1189">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e9175-1189">Az.Websites</span></span>
* <span data-ttu-id="e9175-1190">Åtgärdade en bugg i datumparsningen i Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="e9175-1190">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="e9175-1191">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e9175-1191">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="e9175-1192">1.0.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="e9175-1192">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="e9175-1193">Allmänt</span><span class="sxs-lookup"><span data-stu-id="e9175-1193">General</span></span>

- <span data-ttu-id="e9175-1194">Allmän tillgänglighet för Az-modulen</span><span class="sxs-lookup"><span data-stu-id="e9175-1194">General Availability of Az Module</span></span>
- <span data-ttu-id="e9175-1195">Onlinehjälp för varje modul</span><span class="sxs-lookup"><span data-stu-id="e9175-1195">Online help for each module</span></span>
- <span data-ttu-id="e9175-1196">Mer information och en översikt finns på [Az-informationssidan](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="e9175-1196">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="e9175-1197">Information om hur du migrerar från AzureRM finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e9175-1197">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="e9175-1198">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e9175-1198">Az.Accounts</span></span>
- <span data-ttu-id="e9175-1199">Har ändrats från Az.Profile</span><span class="sxs-lookup"><span data-stu-id="e9175-1199">Changed from Az.Profile</span></span>
- <span data-ttu-id="e9175-1200">Fasta tabellformat för profil- och kontexttyper</span><span class="sxs-lookup"><span data-stu-id="e9175-1200">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="e9175-1201">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e9175-1201">Az.ApiManagement</span></span>
- <span data-ttu-id="e9175-1202">Korrigeringar för #7002</span><span class="sxs-lookup"><span data-stu-id="e9175-1202">Fixes for #7002</span></span>
- <span data-ttu-id="e9175-1203">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e9175-1203">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="e9175-1204">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="e9175-1204">Az.Batch</span></span>
- <span data-ttu-id="e9175-1205">Lade till möjligheten att se vilken version av Azure Batch Node Agent som körs på var och en av de virtuella datorerna i en pool, via den nya egenskapen `NodeAgentInformation` på `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="e9175-1205">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="e9175-1206">Standarden `Caching` för `PSDataDisk` är nu `ReadWrite` i stället för `None`.</span><span class="sxs-lookup"><span data-stu-id="e9175-1206">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="e9175-1207">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e9175-1207">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="e9175-1208">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="e9175-1208">Az.Billing</span></span>
- <span data-ttu-id="e9175-1209">Kombinerar cmdletarna för fakturering, förbrukning och UsageAggregates. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e9175-1209">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="e9175-1210">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="e9175-1210">Az.CognitivServices</span></span>
- <span data-ttu-id="e9175-1211">Lade till kompletterare för SkuName och Typem som är tillgängliga i New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="e9175-1211">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="e9175-1212">Tog bort parameteruppsättningen GetSkusWithAccountParamSetName från Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="e9175-1212">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="e9175-1213">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="e9175-1213">Az.ContainerInstance</span></span>
- <span data-ttu-id="e9175-1214">Stöd för ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="e9175-1214">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="e9175-1215">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="e9175-1215">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="e9175-1216">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e9175-1216">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="e9175-1217">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e9175-1217">Az.DataLakeStore</span></span>
- <span data-ttu-id="e9175-1218">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e9175-1218">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="e9175-1219">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e9175-1219">Az.Monitor</span></span>
- <span data-ttu-id="e9175-1220">Döpte om Az.Insights till Az.Monitor och andra mindre icke-bakåtkompatibla ändringar. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e9175-1220">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="e9175-1221">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e9175-1221">Az.KeyVault</span></span>
- <span data-ttu-id="e9175-1222">Tog bort den inaktuella egenskapen PurgeDisabled från utdatatyper</span><span class="sxs-lookup"><span data-stu-id="e9175-1222">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="e9175-1223">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="e9175-1223">Az.MachineLearning</span></span>
- <span data-ttu-id="e9175-1224">Inkluderade cmdletarna från modulen Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="e9175-1224">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="e9175-1225">Az.Media</span><span class="sxs-lookup"><span data-stu-id="e9175-1225">Az.Media</span></span>
- <span data-ttu-id="e9175-1226">Tog bort inaktuella -Tags-alias från New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="e9175-1226">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="e9175-1227">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e9175-1227">Az.Network</span></span>
<span data-ttu-id="e9175-1228">Stöd har lagts till för konfiguration av RewriteRuleSets i Application Gateway</span><span class="sxs-lookup"><span data-stu-id="e9175-1228">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="e9175-1229">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="e9175-1229">New cmdlets added:</span></span>
        - <span data-ttu-id="e9175-1230">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e9175-1230">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e9175-1231">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e9175-1231">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e9175-1232">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e9175-1232">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e9175-1233">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e9175-1233">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e9175-1234">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e9175-1234">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e9175-1235">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="e9175-1235">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="e9175-1236">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="e9175-1236">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="e9175-1237">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="e9175-1237">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="e9175-1238">Cmdletar har uppdaterats med den valfria parametern -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e9175-1238">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="e9175-1239">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e9175-1239">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="e9175-1240">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e9175-1240">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="e9175-1241">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e9175-1241">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="e9175-1242">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e9175-1242">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="e9175-1243">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e9175-1243">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="e9175-1244">New-AzureRmApplicationGatewayUrlPathMapConfig har lagt till KeyVault-stöd för Application Gateway med Identity.</span><span class="sxs-lookup"><span data-stu-id="e9175-1244">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="e9175-1245">Cmdletar har uppdaterats med den valfria parametern -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="e9175-1245">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="e9175-1246">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e9175-1246">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="e9175-1247">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e9175-1247">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="e9175-1248">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e9175-1248">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="e9175-1249">Cmdleten New-AzApplicationGateway har uppdaterats med den valfria parametern -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="e9175-1249">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="e9175-1250">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e9175-1250">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="e9175-1251">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e9175-1251">Az.OperationalInsights</span></span>
- <span data-ttu-id="e9175-1252">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e9175-1252">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="e9175-1253">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="e9175-1253">Az.Profile</span></span>
- <span data-ttu-id="e9175-1254">Modulnamnet har ändrats till Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e9175-1254">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="e9175-1255">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e9175-1255">Az.RecoveryServices</span></span>
- <span data-ttu-id="e9175-1256">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e9175-1256">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="e9175-1257">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e9175-1257">Az.Resources</span></span>
- <span data-ttu-id="e9175-1258">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e9175-1258">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="e9175-1259">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e9175-1259">Az.ServiceFabric</span></span>
- <span data-ttu-id="e9175-1260">Stöd för specificering av certifikat efter eget namn och tumavtryck</span><span class="sxs-lookup"><span data-stu-id="e9175-1260">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="e9175-1261">Information om fler icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e9175-1261">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="e9175-1262">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="e9175-1262">Az.SIgnalR</span></span>
- <span data-ttu-id="e9175-1263">Allmän tillgänglighet för PowerShell-cmdletar för SIgnalR</span><span class="sxs-lookup"><span data-stu-id="e9175-1263">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="e9175-1264">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e9175-1264">Az.Sql</span></span>
- <span data-ttu-id="e9175-1265">Lade till de nya identifieringstyperna Data_Exfiltration och Unsafe_Action i Threat Detection-cmdletar</span><span class="sxs-lookup"><span data-stu-id="e9175-1265">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="e9175-1266">Uppdaterade dokumentationsexempel för Sql Auditing-cmdletar</span><span class="sxs-lookup"><span data-stu-id="e9175-1266">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="e9175-1267">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e9175-1267">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="e9175-1268">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e9175-1268">Az.Storage</span></span>
- <span data-ttu-id="e9175-1269">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e9175-1269">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="e9175-1270">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e9175-1270">Az.Websites</span></span>
- <span data-ttu-id="e9175-1271">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e9175-1271">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="e9175-1272">0.7.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="e9175-1272">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="e9175-1273">Allmänt</span><span class="sxs-lookup"><span data-stu-id="e9175-1273">General</span></span>

* <span data-ttu-id="e9175-1274">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="e9175-1274">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="e9175-1275">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e9175-1275">Az.Compute</span></span>

* <span data-ttu-id="e9175-1276">Lade till stöd för UltraSSD och Galleriavbildningar i de enkla parameteruppsättningarna för `New-AzVm(ss)`-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="e9175-1276">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="e9175-1277">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e9175-1277">Az.DataLakeStore</span></span>

* <span data-ttu-id="e9175-1278">Åtgärdade avslutande snedstreck i domänen för adls-konto</span><span class="sxs-lookup"><span data-stu-id="e9175-1278">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="e9175-1279">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="e9175-1279">Az.FrontDoor</span></span>

* <span data-ttu-id="e9175-1280">Brutna länkar korrigerades</span><span class="sxs-lookup"><span data-stu-id="e9175-1280">Fixed some broken links</span></span>
    - <span data-ttu-id="e9175-1281">I artiklarna New-AzureRmFrontDoor och Set-AzureRmFrontDoor artiklar korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="e9175-1281">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="e9175-1282">I artikeln New-AzureRmFrontDoorManagedRuleObject korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="e9175-1282">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="e9175-1283">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e9175-1283">Az.RecoveryServices</span></span>

* <span data-ttu-id="e9175-1284">Lade till valideringar på klientsidan för Azure-filresurs med återställningsåtgärder.</span><span class="sxs-lookup"><span data-stu-id="e9175-1284">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="e9175-1285">Gjorde storageAccountName och storageAccountResourceGroupName valfritt för afs-återställning.</span><span class="sxs-lookup"><span data-stu-id="e9175-1285">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="e9175-1286">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e9175-1286">Az.Resources</span></span>

* <span data-ttu-id="e9175-1287">Korrigering för https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="e9175-1287">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="e9175-1288">Uppdaterade Get-AzureRmRoleAssignment så att prenumerationsomfattningen används om den anges vid begäran om klassiska administratörer.</span><span class="sxs-lookup"><span data-stu-id="e9175-1288">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="e9175-1289">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e9175-1289">Az.Sql</span></span>

* <span data-ttu-id="e9175-1290">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="e9175-1290">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="e9175-1291">Korrigerade ett problem med Get-AzureRmSqlDatabaseVulnerabilityAssessment med DotNet-kärna</span><span class="sxs-lookup"><span data-stu-id="e9175-1291">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="e9175-1292">Ändrade dokumentationen för hjälpmeddelanden som rör SQL Auditing-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="e9175-1292">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="e9175-1293">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e9175-1293">Az.Storage</span></span>

* <span data-ttu-id="e9175-1294">Lade till -EnableHierarchicalNamespace i New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e9175-1294">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="e9175-1295">Åtgärdade problemet med att cmdleten Copy File inte kunde återanvända källkontexten på målet om inte -DestContext angetts</span><span class="sxs-lookup"><span data-stu-id="e9175-1295">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="e9175-1296">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="e9175-1296">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="e9175-1297">Stöd för statisk webbplatskonfiguration</span><span class="sxs-lookup"><span data-stu-id="e9175-1297">Support Static Website configuration</span></span>
    - <span data-ttu-id="e9175-1298">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="e9175-1298">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="e9175-1299">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="e9175-1299">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="e9175-1300">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e9175-1300">Az.Websites</span></span>

* <span data-ttu-id="e9175-1301">Set-AzureRmWebApp och Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e9175-1301">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="e9175-1302">Ny parameter (-AzureStoragePath) har lagts till för att ange att Azure Storage-sökvägar ska monteras i containerappar i Windows och Linux.</span><span class="sxs-lookup"><span data-stu-id="e9175-1302">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="e9175-1303">Använder utdata från den nya cmdleten New-AzureRmWebAppAzureStoragePath som en parameter för att ange sökvägar för Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="e9175-1303">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="e9175-1304">0.6.1 – november 2018</span><span class="sxs-lookup"><span data-stu-id="e9175-1304">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="e9175-1305">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e9175-1305">Az.ApiManagement</span></span>
* <span data-ttu-id="e9175-1306">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="e9175-1306">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="e9175-1307">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e9175-1307">Az.Automation</span></span>
* <span data-ttu-id="e9175-1308">Swagger baserade Azure Automation-cmdletar</span><span class="sxs-lookup"><span data-stu-id="e9175-1308">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="e9175-1309">Cmdletar för Uppdateringshantering har lagts till</span><span class="sxs-lookup"><span data-stu-id="e9175-1309">Added Update Management cmdlets</span></span>
* <span data-ttu-id="e9175-1310">Cmdletar för källkontroll har lagts till</span><span class="sxs-lookup"><span data-stu-id="e9175-1310">Added Source Control cmdlets</span></span>
* <span data-ttu-id="e9175-1311">Remove-AzureRmAutomationHybridWorkerGroup-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="e9175-1311">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="e9175-1312">Kommandot för DSC-registreringsnod har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="e9175-1312">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="e9175-1313">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e9175-1313">Az.Compute</span></span>
* <span data-ttu-id="e9175-1314">Problem med SystemAssigned-identitet har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="e9175-1314">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="e9175-1315">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="e9175-1315">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="e9175-1316">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="e9175-1316">Az.ContainerInstance</span></span>
* <span data-ttu-id="e9175-1317">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="e9175-1317">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="e9175-1318">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="e9175-1318">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="e9175-1319">uppdatera exempelbeskrivningen för marketplace-cmdletar</span><span class="sxs-lookup"><span data-stu-id="e9175-1319">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="e9175-1320">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e9175-1320">Az.Network</span></span>
* <span data-ttu-id="e9175-1321">Cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomErreller Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="e9175-1321">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="e9175-1322">ICMP tillbaka till stöd för Azure Firewall-nätverksprotokoll har lagts till</span><span class="sxs-lookup"><span data-stu-id="e9175-1322">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="e9175-1323">Uppdatera cmdlet Test-AzureRmNetworkWatcherConnectivity, lägga till verifiering av mål-id, adress och port.</span><span class="sxs-lookup"><span data-stu-id="e9175-1323">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="e9175-1324">Åtgärda problem med minnesanvändning i VirtualNetwork-karta</span><span class="sxs-lookup"><span data-stu-id="e9175-1324">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="e9175-1325">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="e9175-1325">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="e9175-1326">Åtgärda för att ändra principen för en skyddad fildelning.</span><span class="sxs-lookup"><span data-stu-id="e9175-1326">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="e9175-1327">Tidszonsprincipen har konverterats till versaler.</span><span class="sxs-lookup"><span data-stu-id="e9175-1327">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="e9175-1328">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="e9175-1328">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="e9175-1329">Exempel i New-AzureRmRecoveryServicesAsrProtectableItem har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="e9175-1329">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="e9175-1330">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="e9175-1330">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="e9175-1331">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="e9175-1331">Az.Relay</span></span>
* <span data-ttu-id="e9175-1332">Valfri parameter -KeyValue till New-AzureRmRelayKey cmdlet har lagts till, vilket gör det möjligt för användare att tillhandahålla KeyValue.</span><span class="sxs-lookup"><span data-stu-id="e9175-1332">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="e9175-1333">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e9175-1333">Az.Resources</span></span>
* <span data-ttu-id="e9175-1334">Uppdatera hjälpdokumentation för resursidentitet kopplad till parametrar i `New-AzureRmPolicyAssignment` och `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="e9175-1334">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="e9175-1335">Lägg till ett exempel för New-AzureRmPolicyDefinition som använder -Metadata</span><span class="sxs-lookup"><span data-stu-id="e9175-1335">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="e9175-1336">Korrigera så att skiftläge behålls i taggnycklar i NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="e9175-1336">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="e9175-1337">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e9175-1337">Az.ServiceFabric</span></span>
* <span data-ttu-id="e9175-1338">Lägg till utfasningsmeddelanden för kommande icke-kompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="e9175-1338">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="e9175-1339">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e9175-1339">Az.Sql</span></span>
* <span data-ttu-id="e9175-1340">Nya cmdletar för CRUD-åtgärder på Azure Sql Database-hanterad instans och Azure Sql-hanterad databas</span><span class="sxs-lookup"><span data-stu-id="e9175-1340">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="e9175-1341">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="e9175-1341">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="e9175-1342">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="e9175-1342">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="e9175-1343">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="e9175-1343">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="e9175-1344">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="e9175-1344">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="e9175-1345">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="e9175-1345">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="e9175-1346">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="e9175-1346">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="e9175-1347">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="e9175-1347">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="e9175-1348">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="e9175-1348">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="e9175-1349">Hantering av utökad granskningsprincip på en server eller en databas har aktiverats.</span><span class="sxs-lookup"><span data-stu-id="e9175-1349">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="e9175-1350">Ny parameter (PredicateExpression) har lagts till för att aktivera filtrering av granskningsloggar.</span><span class="sxs-lookup"><span data-stu-id="e9175-1350">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="e9175-1351">Cmdletar har ändrats så att de använder SQL-klienter i stället för äldre klienter.</span><span class="sxs-lookup"><span data-stu-id="e9175-1351">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="e9175-1352">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="e9175-1352">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="e9175-1353">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="e9175-1353">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="e9175-1354">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="e9175-1354">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="e9175-1355">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="e9175-1355">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="e9175-1356">Problem med att använda Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings med lagringskontots namnparameter har korrigerats</span><span class="sxs-lookup"><span data-stu-id="e9175-1356">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="e9175-1357">0.5.0 – november 2018</span><span class="sxs-lookup"><span data-stu-id="e9175-1357">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="e9175-1358">Allmänt</span><span class="sxs-lookup"><span data-stu-id="e9175-1358">General</span></span>
* <span data-ttu-id="e9175-1359">Lade till resurskompletterare till många kärn-cmdletar – dessa gör att du kan stega genom befintliga resursnamn med TABB vid interaktiva anrop till cmdletar</span><span class="sxs-lookup"><span data-stu-id="e9175-1359">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="e9175-1360">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="e9175-1360">Az.Profile</span></span>
* <span data-ttu-id="e9175-1361">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="e9175-1361">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="e9175-1362">Bytte namn på parametern TenantId i cmdleten Connect-AzAccount till Tenant och lade till ett alias för TenantId</span><span class="sxs-lookup"><span data-stu-id="e9175-1362">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="e9175-1363">Uppdaterade TenantId-beskrivningen för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="e9175-1363">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="e9175-1364">Åtgärda felmeddelande för misslyckad inloggning när du tillhandahåller klientdomän</span><span class="sxs-lookup"><span data-stu-id="e9175-1364">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="e9175-1365">Åtgärda problem med att kontextnamn hamnar i konflikt för konton utan prenumerationer i klientorganisationen</span><span class="sxs-lookup"><span data-stu-id="e9175-1365">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="e9175-1366">Åtgärda problem med DataLake-slutpunkter vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="e9175-1366">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="e9175-1367">Åtgärdade problem med att Disconnect-AzAccount kastades om den inte anslöts</span><span class="sxs-lookup"><span data-stu-id="e9175-1367">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="e9175-1368">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e9175-1368">Az.CognitiveServices</span></span>
* <span data-ttu-id="e9175-1369">Lade till åtgärden Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="e9175-1369">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e9175-1370">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e9175-1370">Az.Compute</span></span>
* <span data-ttu-id="e9175-1371">Lade till cmdletarna Add-AzVmssVMDataDisk och Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="e9175-1371">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="e9175-1372">Get-AzVMImage visar AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="e9175-1372">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="e9175-1373">Åtgärdade att värdena för alternativen SetAzVMChefExtension -BootstrapOptions och -JsonAttribute inte angavs i json-format.</span><span class="sxs-lookup"><span data-stu-id="e9175-1373">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e9175-1374">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e9175-1374">Az.DataLakeStore</span></span>
* <span data-ttu-id="e9175-1375">Uppdatera DataLake-paketet till 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="e9175-1375">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="e9175-1376">Lägg till standardsamtidighet för flertrådade åtgärder.</span><span class="sxs-lookup"><span data-stu-id="e9175-1376">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="e9175-1377">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="e9175-1377">Az.Insights</span></span>
* <span data-ttu-id="e9175-1378">Åtgärdade problem #7267 (autoskalningsområde)</span><span class="sxs-lookup"><span data-stu-id="e9175-1378">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="e9175-1379">Problem med att uppräknade parametrar inte ställdes in ordentligt när du skapade en ny autoskalningsregel (de ställdes alltid in med standardvärdet).</span><span class="sxs-lookup"><span data-stu-id="e9175-1379">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="e9175-1380">Åtgärdade problem #7513 [Insights] Set-AzDiagnosticSetting kräver uttrycklig specifikation av kategorier när inställningar skapas</span><span class="sxs-lookup"><span data-stu-id="e9175-1380">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="e9175-1381">Nu kräver inte cmdleten uttrycklig anvisning av kategorierna för att aktiveras under skapande, d.v.s. den fungerar enligt beskrivning</span><span class="sxs-lookup"><span data-stu-id="e9175-1381">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e9175-1382">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e9175-1382">Az.Network</span></span>
* <span data-ttu-id="e9175-1383">PeeringType ändrades till en obligatorisk parameter för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="e9175-1383">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="e9175-1384">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="e9175-1384">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="e9175-1385">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="e9175-1385">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="e9175-1386">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="e9175-1386">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="e9175-1387">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="e9175-1387">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="e9175-1388">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="e9175-1388">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="e9175-1389">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="e9175-1389">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="e9175-1390">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="e9175-1390">Az.PolicyInsights</span></span>
* <span data-ttu-id="e9175-1391">Cmdletar för principreparation har lagts till</span><span class="sxs-lookup"><span data-stu-id="e9175-1391">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="e9175-1392">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e9175-1392">Az.Resources</span></span>
* <span data-ttu-id="e9175-1393">Korrigering för https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="e9175-1393">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="e9175-1394">Tillåt att resurser listas med parametern -ResourceId för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="e9175-1394">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="e9175-1395">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e9175-1395">Az.ServiceBus</span></span>
* <span data-ttu-id="e9175-1396">Skrivskyddad MigrationState-egenskap har lagts till i PSServiceBusMigrationConfigurationAttributes, som hjälper till att hålla koll på migreringstillståndet.</span><span class="sxs-lookup"><span data-stu-id="e9175-1396">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e9175-1397">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e9175-1397">Az.ServiceFabric</span></span>
* <span data-ttu-id="e9175-1398">Åtgärda att lägga till certifikat till Linux-Vmss.</span><span class="sxs-lookup"><span data-stu-id="e9175-1398">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="e9175-1399">Åtgärdade Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="e9175-1399">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="e9175-1400">Använd rätt tumavtryck från nya certifikat (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="e9175-1400">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="e9175-1401">Visa undantag korrekt (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="e9175-1401">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="e9175-1402">Åtgärdade Update-AzServiceFabricDurability så att klusterkonfigurationen uppdateras innan Vmss-åtgärden CreateOrUpdate påbörjas.</span><span class="sxs-lookup"><span data-stu-id="e9175-1402">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="e9175-1403">0.4.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="e9175-1403">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="e9175-1404">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="e9175-1404">Az.Profile</span></span>
* <span data-ttu-id="e9175-1405">Åtgärdade problemet med Get-AzSubscription i CloudShell</span><span class="sxs-lookup"><span data-stu-id="e9175-1405">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="e9175-1406">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="e9175-1406">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e9175-1407">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e9175-1407">Az.Compute</span></span>
* <span data-ttu-id="e9175-1408">Nya storlekar lades till i listan över godkända VM-storlekar för vilka accelererat nätverk kommer att aktiveras vid användning av den enkla parameteruppsättningen för New-AzVm</span><span class="sxs-lookup"><span data-stu-id="e9175-1408">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="e9175-1409">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="e9175-1409">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e9175-1410">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e9175-1410">Az.DataLakeStore</span></span>
* <span data-ttu-id="e9175-1411">Lägger till stöd för regler för virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="e9175-1411">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="e9175-1412">Get-AzDataLakeStoreVirtualNetworkRule: Hämtar eller listar regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e9175-1412">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="e9175-1413">Add-AzDataLakeStoreVirtualNetworkRule: Lägger till en regel för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="e9175-1413">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="e9175-1414">Set-AzDataLakeStoreVirtualNetworkRule: Ändrar den angivna regeln för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="e9175-1414">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="e9175-1415">Remove-AzDataLakeStoreVirtualNetworkRule: Tar bort en regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e9175-1415">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e9175-1416">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e9175-1416">Az.Network</span></span>
* <span data-ttu-id="e9175-1417">Skicka protokollvärdet till serverdelen för att uppdatera cmdleten Test-AzNetworkWatcherConnectivity.</span><span class="sxs-lookup"><span data-stu-id="e9175-1417">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="e9175-1418">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="e9175-1418">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e9175-1419">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e9175-1419">Az.Resources</span></span>
* <span data-ttu-id="e9175-1420">Åtgärdade problem där Get-AzRoleDefinition genererar ett oläsligt undantag (när standardprofilen inte innehåller någon prenumeration och ingen omfattning har angetts) genom att lägga till ett beskrivande undantag i scenariot.</span><span class="sxs-lookup"><span data-stu-id="e9175-1420">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="e9175-1421">Ställ in ”RoleDefinitionNameParameterSet” som standardparameteruppsättning.</span><span class="sxs-lookup"><span data-stu-id="e9175-1421">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="e9175-1422">0.3.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="e9175-1422">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="e9175-1423">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="e9175-1423">Azure.Storage</span></span>
* <span data-ttu-id="e9175-1424">Åtgärda fel där Kopiera blob/fil inte kopierar metadata när målplatsen har ett problem med metadata</span><span class="sxs-lookup"><span data-stu-id="e9175-1424">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="e9175-1425">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="e9175-1425">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="e9175-1426">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="e9175-1426">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="e9175-1427">Stöd för att hämta användningsinformation om en Storage-resurs för en specifik plats och för att lägga till ett varningsmeddelande för att hämta användningsinformation om en global Storage-resurs är inaktuellt.</span><span class="sxs-lookup"><span data-stu-id="e9175-1427">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="e9175-1428">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="e9175-1428">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="e9175-1429">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e9175-1429">Az.CognitiveServices</span></span>
* <span data-ttu-id="e9175-1430">Stöd för Get-AzCognitiveServicesAccountSkus utan ett befintligt konto.</span><span class="sxs-lookup"><span data-stu-id="e9175-1430">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e9175-1431">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e9175-1431">Az.Compute</span></span>
* <span data-ttu-id="e9175-1432">Åtgärdade fel där Get-AzVM -ResourceGroupName <rg> returnerar fler än 50 resultat om det behövs</span><span class="sxs-lookup"><span data-stu-id="e9175-1432">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="e9175-1433">Lade till ett exempel för SimpleParameterSet i hjälpen för cmdleten New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="e9175-1433">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="e9175-1434">Ett stavfel i förloppsmeddelandet för Azure Disk Encryption har korrigerats</span><span class="sxs-lookup"><span data-stu-id="e9175-1434">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="e9175-1435">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="e9175-1435">Az.DataFactoryV2</span></span>
* <span data-ttu-id="e9175-1436">ADF .Net SDK-versionen har uppdaterats till 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="e9175-1436">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e9175-1437">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e9175-1437">Az.Network</span></span>
* <span data-ttu-id="e9175-1438">Funktionalitet för NetworkProfile har lagts till.</span><span class="sxs-lookup"><span data-stu-id="e9175-1438">Added NetworkProfile functionality.</span></span> <span data-ttu-id="e9175-1439">nya cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="e9175-1439">new cmdlets added</span></span>
    - <span data-ttu-id="e9175-1440">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e9175-1440">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="e9175-1441">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e9175-1441">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="e9175-1442">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e9175-1442">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="e9175-1443">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e9175-1443">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="e9175-1444">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="e9175-1444">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="e9175-1445">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="e9175-1445">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="e9175-1446">Länk för tjänstassociering på modell för undernät har lagts till</span><span class="sxs-lookup"><span data-stu-id="e9175-1446">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="e9175-1447">Cmdletarna New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap och Remove-AzVirtualNetworkTap har lagts till</span><span class="sxs-lookup"><span data-stu-id="e9175-1447">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="e9175-1448">Cmdletarna Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig och Remove-AzNEtworkInterfaceTapConfig har lagts till</span><span class="sxs-lookup"><span data-stu-id="e9175-1448">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="e9175-1449">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="e9175-1449">Az.RedisCache</span></span>
* <span data-ttu-id="e9175-1450">Tillåt att alla strängar används som storleksparametrar framöver.</span><span class="sxs-lookup"><span data-stu-id="e9175-1450">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="e9175-1451">Lägg till P5 i popup-fönstret PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="e9175-1451">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="e9175-1452">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e9175-1452">Az.Resources</span></span>
* <span data-ttu-id="e9175-1453">Parametern -Mode som saknades i Set-AzPolicyDefinition har lagts till</span><span class="sxs-lookup"><span data-stu-id="e9175-1453">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="e9175-1454">Åtgärdade buggen för cmdleten Get-AzProviderOperation för åtgärder med ursprung som innehåller användare</span><span class="sxs-lookup"><span data-stu-id="e9175-1454">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="e9175-1455">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e9175-1455">Az.Sql</span></span>
* <span data-ttu-id="e9175-1456">Ett problem där vissa cmdletar för säkerhetskopiering inte kunde identifiera den aktuella azure-prenumerationen har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="e9175-1456">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e9175-1457">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e9175-1457">Az.Websites</span></span>
* <span data-ttu-id="e9175-1458">Ny cmdlet: Get-AzWebAppContainerContinuousDeploymentUrl – Hämtar webhook-URL:en för kontinuerlig distribution av container</span><span class="sxs-lookup"><span data-stu-id="e9175-1458">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="e9175-1459">Nya cmdletar: New-AzWebAppContainerPSSession och Enter-WebAppContainerPSSession – Startar en PowerShell-fjärrsession i en containerapp för windows</span><span class="sxs-lookup"><span data-stu-id="e9175-1459">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="e9175-1460">0.2.0 – september 2018</span><span class="sxs-lookup"><span data-stu-id="e9175-1460">0.2.0 - September 2018</span></span>
 <span data-ttu-id="e9175-1461">Första versionen</span><span class="sxs-lookup"><span data-stu-id="e9175-1461">Initial Release</span></span>