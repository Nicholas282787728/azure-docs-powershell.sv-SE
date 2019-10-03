---
title: Viktig information om Azure PowerShell
description: Lär dig mer om alla de senaste uppdateringarna för Azure PowerShell-modulerna.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/25/2019
ms.openlocfilehash: b879d970d3237098e481dba0419ee65efa8d51cd
ms.sourcegitcommit: f0f09eee03ef9dd7fe07432252a3dc8ca93e3a7b
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/27/2019
ms.locfileid: "71319317"
---
## <a name="270---september-2019"></a><span data-ttu-id="04954-103">2.7.0 – september 2019</span><span class="sxs-lookup"><span data-stu-id="04954-103">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="04954-104">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="04954-104">Az.ApiManagement</span></span>
* <span data-ttu-id="04954-105">Uppdatera ”-Format”-parameterbeskrivningen i ”Set-AzApiManagementPolicy”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="04954-105">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="04954-106">Referenser för den föråldrade cmdleten ”Update-AzApiManagementDeployment” har tagits bort från referensdokumentationen.</span><span class="sxs-lookup"><span data-stu-id="04954-106">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="04954-107">Använd ”Set-AzApiManagement” i stället.</span><span class="sxs-lookup"><span data-stu-id="04954-107">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="04954-108">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="04954-108">Az.Automation</span></span>
* <span data-ttu-id="04954-109">Stavfel har korrigerats i exempel i referensdokumentationen för ”Register-AzAutomationDscNode”</span><span class="sxs-lookup"><span data-stu-id="04954-109">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="04954-110">Klargörande har lagts till om OS-begränsningar för Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="04954-110">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="04954-111">Null-referensundantag har korrigerats för -Wait-alternativet i Start-AzAutomationRunbook-cmdleten.</span><span class="sxs-lookup"><span data-stu-id="04954-111">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="04954-112">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="04954-112">Az.Compute</span></span>
* <span data-ttu-id="04954-113">Lägg till UploadSizeInBytes-parameter till New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="04954-113">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="04954-114">Lägg till Incremental-parameter till New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="04954-114">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="04954-115">Lägg till en funktion för virtuella datorer med låg prioritet:</span><span class="sxs-lookup"><span data-stu-id="04954-115">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="04954-116">MaxPrice-, EvictionPolicy- och Priority-parametrar har lagts till i New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="04954-116">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="04954-117">MaxPrice-parametern har lagts till i New-AzVmssConfig-, Update-AzVM- och Update-AzVmss-cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="04954-117">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="04954-118">Åtgärda problem med VM-referenser för Get-AzAvailabilitySet-cmdleten när alla tillgänglighetsuppsättningar i prenumerationen visas.</span><span class="sxs-lookup"><span data-stu-id="04954-118">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="04954-119">Korrigera null-undantaget för Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="04954-119">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="04954-120">Korrigera VHD-metoden för sökning relativt till slut.</span><span class="sxs-lookup"><span data-stu-id="04954-120">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="04954-121">Åtgärda UltraSSD-problem för New-AzVM och Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="04954-121">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="04954-122">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="04954-122">Az.DataFactory</span></span>
* <span data-ttu-id="04954-123">Lägger till 3 nya kommandon för ADF V2 – Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription och Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="04954-123">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="04954-124">ADF .Net SDK har uppdaterats till 4.1.3</span><span class="sxs-lookup"><span data-stu-id="04954-124">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="04954-125">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="04954-125">Az.HDInsight</span></span>
* <span data-ttu-id="04954-126">Anrop för icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="04954-126">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="04954-127">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="04954-127">Az.IotHub</span></span>
* <span data-ttu-id="04954-128">Lägg till stöd för att anropa redundans för en IotHub till den geo-länkade katastrofåterställningsregionen.</span><span class="sxs-lookup"><span data-stu-id="04954-128">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="04954-129">Lägg till stöd för att hantera meddelandeberikning för en IotHub.</span><span class="sxs-lookup"><span data-stu-id="04954-129">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="04954-130">Nya cmdlet:ar är:</span><span class="sxs-lookup"><span data-stu-id="04954-130">New cmdlets are:</span></span>
    - <span data-ttu-id="04954-131">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="04954-131">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="04954-132">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="04954-132">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="04954-133">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="04954-133">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="04954-134">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="04954-134">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="04954-135">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="04954-135">Az.Monitor</span></span>
* <span data-ttu-id="04954-136">Pekar på den senaste Monitor SDK:n, dvs. 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="04954-136">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="04954-137">Lägger till bakåtkompatibla ändringar i Metrics-cmdletarna, dvs. enhetsuppräkningen stöder flera nya värden.</span><span class="sxs-lookup"><span data-stu-id="04954-137">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="04954-138">Detta är skrivskyddade cmdletar, så det förekommer inga ändringar i inmatningen för cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="04954-138">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="04954-139">API-versionen för **ActionGroups**-begäranden är nu **2019-06-01**. Tidigare var den **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="04954-139">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="04954-140">Test av scenarier har uppdaterats för att anpassas till den här ändringen.</span><span class="sxs-lookup"><span data-stu-id="04954-140">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="04954-141">Ett nytt obligatoriskt argument har lagts till för konstruktorerna för klasserna **EmailReceiver** och **WebhookReceiver** – ett booleskt värde med namnet **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="04954-141">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="04954-142">Värdet är för närvarande fast till **false** så att den här icke-bakåtkompatibla ändringen är dold från cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="04954-142">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="04954-143">**Obs!** Det här är en tillfällig ändring som måste verifieras av Alerts-teamet.</span><span class="sxs-lookup"><span data-stu-id="04954-143">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="04954-144">Ordningen på argumenten för konstruktorn för klassen **Source** (relaterad till klassen **ScheduledQueryRuleSource**) har ändrats från den tidigare SDK:n.</span><span class="sxs-lookup"><span data-stu-id="04954-144">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="04954-145">Den här ändringen krävde korrigering av två enhetstest: de kompilerades, men testerna skickades inte.</span><span class="sxs-lookup"><span data-stu-id="04954-145">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="04954-146">Ordningen på argumenten för konstruktorn för klassen **AlertingAction** (relaterad till klassen **ScheduledQueryRuleSource**) har ändrats från den tidigare SDK:n.</span><span class="sxs-lookup"><span data-stu-id="04954-146">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="04954-147">Den här ändringen krävde korrigering av två enhetstest: de kompilerades, men testerna skickades inte.</span><span class="sxs-lookup"><span data-stu-id="04954-147">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="04954-148">Stöd för kriterier för dynamiskt tröskelvärde för måttavisering v2</span><span class="sxs-lookup"><span data-stu-id="04954-148">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="04954-149">New-AzMetricAlertRuleV2Criteria: skapar nu även kriterier för dynamiskt tröskelvärde</span><span class="sxs-lookup"><span data-stu-id="04954-149">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="04954-150">Add-AzMetricAlertRuleV2: accepterar nu även kriterier för dynamiskt tröskelvärde</span><span class="sxs-lookup"><span data-stu-id="04954-150">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="04954-151">Förbättringar i schemalagd frågeregel (SQR)</span><span class="sxs-lookup"><span data-stu-id="04954-151">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="04954-152">Cmdletar accepterar ”Location”-parameter i båda formaten, antingen platsen (t.ex. eastus) eller platsens visningsnamn (t.ex. USA, östra)</span><span class="sxs-lookup"><span data-stu-id="04954-152">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="04954-153">”Enabled”-parametern illustreras korrekt i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="04954-153">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="04954-154">Exempel för den valfria parametern ”ActionGroup” har lagts till</span><span class="sxs-lookup"><span data-stu-id="04954-154">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="04954-155">Förbättrade hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="04954-155">Overall improved help files</span></span>
* <span data-ttu-id="04954-156">Åtgärda bugg då omfattningstypen fastställs för ”Set-AzActionRule”</span><span class="sxs-lookup"><span data-stu-id="04954-156">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="04954-157">Az.Network</span><span class="sxs-lookup"><span data-stu-id="04954-157">Az.Network</span></span>
* <span data-ttu-id="04954-158">Korrigera felaktigt exempel i referensdokumentationen för ”New-AzApplicationGateway”</span><span class="sxs-lookup"><span data-stu-id="04954-158">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="04954-159">Lägg till anmärkning i ”Get-AzNetworkWatcherPacketCapture”-referensdokumentationen om hämtning av alla egenskaper för en paketinsamling</span><span class="sxs-lookup"><span data-stu-id="04954-159">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="04954-160">Exempel har korrigerats i ”Test-AzNetworkWatcherIPFlow”-referensdokumentationen för korrekt uppräkning av nätverkskort</span><span class="sxs-lookup"><span data-stu-id="04954-160">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="04954-161">Förbättrad tolkning av molnundantag för att visa eventuell ytterligare information</span><span class="sxs-lookup"><span data-stu-id="04954-161">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="04954-162">Förbättrad tolkning av molnundantag för att hantera ytterligare en typ av SDK-undantag</span><span class="sxs-lookup"><span data-stu-id="04954-162">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="04954-163">Felaktig mappning av säkerhetsregelmodeller har korrigerats</span><span class="sxs-lookup"><span data-stu-id="04954-163">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="04954-164">Egenskaper har lagts till för nätverksgränssnittet för funktionen Privat IP</span><span class="sxs-lookup"><span data-stu-id="04954-164">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="04954-165">Egenskapen ”PrivateEndpoint” har lagts till som en typ av PSResourceId till PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="04954-165">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="04954-166">Egenskapen ”PrivateLinkConnectionProperties” har lagts till som en typ av PSIpConfigurationConnectivityInformation till PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="04954-166">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="04954-167">Modellklassen PSIpConfigurationConnectivityInformation har lagts till</span><span class="sxs-lookup"><span data-stu-id="04954-167">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="04954-168">ApplicationRuleProtocolType ”mssql” har lagts till för Azure Firewall-resurs</span><span class="sxs-lookup"><span data-stu-id="04954-168">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="04954-169">MultiLink-stöd i virtuellt WAN</span><span class="sxs-lookup"><span data-stu-id="04954-169">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="04954-170">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="04954-170">New cmdlets</span></span>
        - <span data-ttu-id="04954-171">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="04954-171">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="04954-172">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="04954-172">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="04954-173">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="04954-173">Updated cmdlet:</span></span>
        - <span data-ttu-id="04954-174">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="04954-174">New-VpnSite</span></span>
        - <span data-ttu-id="04954-175">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="04954-175">Update-VpnSite</span></span>
        - <span data-ttu-id="04954-176">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="04954-176">New-VpnConnection</span></span>
        - <span data-ttu-id="04954-177">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="04954-177">Update-VpnConnection</span></span>
* <span data-ttu-id="04954-178">Dokument för vissa PowerShell-exempel har korrigerats så att Az-cmdletar används i stället för AzureRM-cmdletar</span><span class="sxs-lookup"><span data-stu-id="04954-178">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="04954-179">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="04954-179">Az.RecoveryServices</span></span>
* <span data-ttu-id="04954-180">Uppdatera AzureVMpolicy-objekt med ProtectedItemsCount-attribut</span><span class="sxs-lookup"><span data-stu-id="04954-180">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="04954-181">Ytterligare tester har lagts till för VM-princip och återställning av ursprungligt lagringskonto</span><span class="sxs-lookup"><span data-stu-id="04954-181">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="04954-182">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="04954-182">Az.Resources</span></span>
* <span data-ttu-id="04954-183">Åtgärda fel där det inte gick att anropa New-AzRoleAssignment utan parametern Scope.</span><span class="sxs-lookup"><span data-stu-id="04954-183">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="04954-184">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="04954-184">Az.ServiceFabric</span></span>
* <span data-ttu-id="04954-185">Stavfel har korrigerats i exempel för ”Update-AzServiceFabricReliability”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="04954-185">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="04954-186">Lägger till nya cmdletar för att hantera program och tjänster:</span><span class="sxs-lookup"><span data-stu-id="04954-186">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="04954-187">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="04954-187">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="04954-188">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="04954-188">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="04954-189">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="04954-189">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="04954-190">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="04954-190">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="04954-191">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="04954-191">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="04954-192">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="04954-192">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="04954-193">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="04954-193">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="04954-194">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="04954-194">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="04954-195">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="04954-195">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="04954-196">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="04954-196">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="04954-197">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="04954-197">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="04954-198">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="04954-198">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="04954-199">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="04954-199">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="04954-200">Service Fabric SDK har uppgraderats till version 1.2.0 som använder Service Fabric-resursprovidern med API-version 2019-03-01.</span><span class="sxs-lookup"><span data-stu-id="04954-200">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="04954-201">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="04954-201">Az.SignalR</span></span>
* <span data-ttu-id="04954-202">Lägg till Update-, Restart-, CheckNameAvailability- och GetUsage-cmdletar</span><span class="sxs-lookup"><span data-stu-id="04954-202">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="04954-203">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="04954-203">Az.Sql</span></span>
* <span data-ttu-id="04954-204">Uppdatera exempel i referensdokumentationen för ”Get-AzSqlElasticPool”</span><span class="sxs-lookup"><span data-stu-id="04954-204">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="04954-205">vCore-exempel för att skapa en elastisk pool (New-AzSqlElasticPool) har lagts till.</span><span class="sxs-lookup"><span data-stu-id="04954-205">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="04954-206">Ta bort verifieringen av EmailAddresses och kontrollen som bekräftar att EmailAdmins inte är falskt när EmailAddresses är tomt i Set-AzSqlServerAdvancedThreatProtectionPolicy och Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="04954-206">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="04954-207">Server-/databasgranskningsinställningar kan tas bort när det finns flera diagnostikinställningar som aktiverar granskningskategorin.</span><span class="sxs-lookup"><span data-stu-id="04954-207">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="04954-208">Åtgärda verifiering av e-postadresser i flera Sql Vulnerability Assessment-cmdletar (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting och Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="04954-208">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="04954-209">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="04954-209">Az.Storage</span></span>
* <span data-ttu-id="04954-210">Exempel i referensdokumentationen för ”Get-AzStorageAccountKey” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="04954-210">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="04954-211">Vid upp- och nedladdning av en Azure-fil kan SMB-egenskaperna för källfilen (t.ex. filattribut, tidpunkten då filen skapades och tidpunkten för den senaste skrivningen) sparas i målfilen</span><span class="sxs-lookup"><span data-stu-id="04954-211">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="04954-212">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="04954-212">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="04954-213">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="04954-213">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="04954-214">Korrigera problem med uppladdningen av blockblob med egenskaper/metadata för ImmutabilityPolicy i containrar.</span><span class="sxs-lookup"><span data-stu-id="04954-214">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="04954-215">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="04954-215">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="04954-216">Stöd för hantering av Azure-filresurser med API för hanteringsplan</span><span class="sxs-lookup"><span data-stu-id="04954-216">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="04954-217">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="04954-217">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="04954-218">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="04954-218">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="04954-219">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="04954-219">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="04954-220">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="04954-220">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="04954-221">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="04954-221">Az.Websites</span></span>
* <span data-ttu-id="04954-222">Åtgärdar problemet där webapp-taggar togs bort när appen migrerades till nya ASP</span><span class="sxs-lookup"><span data-stu-id="04954-222">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="04954-223">Åtgärda Publish-AzureWebapp så att det fungerar i Linux och Windows</span><span class="sxs-lookup"><span data-stu-id="04954-223">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="04954-224">Uppdatera exempel i ”Get-AzWebAppPublishingProfile”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="04954-224">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="04954-225">2.6.0 – augusti 2019</span><span class="sxs-lookup"><span data-stu-id="04954-225">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="04954-226">Allmänt</span><span class="sxs-lookup"><span data-stu-id="04954-226">General</span></span>
* <span data-ttu-id="04954-227">Åtgärdade diverse skrivfel i flera moduler</span><span class="sxs-lookup"><span data-stu-id="04954-227">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="04954-228">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="04954-228">Az.Accounts</span></span>
* <span data-ttu-id="04954-229">Stöd för användartilldelat MSI i Azure Functions-autentisering (#9479)</span><span class="sxs-lookup"><span data-stu-id="04954-229">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="04954-230">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="04954-230">Az.Aks</span></span>
* <span data-ttu-id="04954-231">Åtgärda problem med utdata för "Get-AzAks"</span><span class="sxs-lookup"><span data-stu-id="04954-231">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="04954-232">Mer information här: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="04954-232">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="04954-233">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="04954-233">Az.ApiManagement</span></span>
* <span data-ttu-id="04954-234">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="04954-234">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="04954-235">Uppdatera .net-NuGet-versionen, som inte tillämpar begränsningar för productId, apiId och userId</span><span class="sxs-lookup"><span data-stu-id="04954-235">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="04954-236">**Get-AzApiManagementProduct** – Lade till stöd för frågekörning mot produkter via API.</span><span class="sxs-lookup"><span data-stu-id="04954-236">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="04954-237">**New-AzApiManagementApiRevision** – Korrigering för problem där ApiRevisionDescription inte angavs vid skapande av ny API-revision https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="04954-237">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="04954-238">Åtgärdade skrivfel i modellen "PsApiManagementOAuth2AuthrozationServer" till "PsApiManagementOAuth2AuthorizationServer"</span><span class="sxs-lookup"><span data-stu-id="04954-238">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="04954-239">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="04954-239">Az.Batch</span></span>
* <span data-ttu-id="04954-240">Åtgärdade skrivfel i hjälpmeddelande och dokumentation till att skriva Windows med versaler</span><span class="sxs-lookup"><span data-stu-id="04954-240">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="04954-241">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="04954-241">Az.Cdn</span></span>
* <span data-ttu-id="04954-242">Åtgärdade skrivfel i CDN-modulens konverteringshjälp</span><span class="sxs-lookup"><span data-stu-id="04954-242">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="04954-243">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="04954-243">Az.Compute</span></span>
* <span data-ttu-id="04954-244">Lägg till VmssId i New-AzVMConfig-cmdleten</span><span class="sxs-lookup"><span data-stu-id="04954-244">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="04954-245">Lägg till parametrarna TerminateScheduledEvents och TerminateScheduledEventNotBeforeTimeoutInMinutes i New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="04954-245">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="04954-246">Lägg till egenskapen HyperVGeneration till avbildningsobjekt för virtuell dator</span><span class="sxs-lookup"><span data-stu-id="04954-246">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="04954-247">Lägg till funktioner för Host och HostGroup</span><span class="sxs-lookup"><span data-stu-id="04954-247">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="04954-248">Nya cmdletar:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="04954-248">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="04954-249">HostId-parametern läggs till i New-AzVMConfig och New-AzVM</span><span class="sxs-lookup"><span data-stu-id="04954-249">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="04954-250">Uppdatera exempel i "Invoke-AzVMRunCommand"-dokumentationen till att använda rätt parameternamn</span><span class="sxs-lookup"><span data-stu-id="04954-250">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="04954-251">Uppdatera "-VolumeType"-beskrivningen i referensdokumentationen för "set-AzVMDiskEncryptionExtension" och "set-AzVmssDiskEncryptionExtension"</span><span class="sxs-lookup"><span data-stu-id="04954-251">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="04954-252">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="04954-252">Az.DataFactory</span></span>
* <span data-ttu-id="04954-253">Åtgärda skrivfel till att använda versaler för "Windows" i "New-AzDataFactoryEncryptValue"-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="04954-253">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="04954-254">Uppdaterade ADF .Net SDK-versionen till 4.1.2</span><span class="sxs-lookup"><span data-stu-id="04954-254">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="04954-255">Lägg till parametrarna "DataProxyIntegrationRuntimeName", "DataProxyStagingLinkedServiceName" och "DataProxyStagingPath" för "Set-AzureRmDataFactoryV2IntegrationRuntime"-cmd för att aktivera konfiguration av lokalt installerad integrationskörning som en proxy för SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="04954-255">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="04954-256">Uppdaterade PSTriggerRun till att visa utlöst pipeline, meddelande och egenskaper samt PSActivityRun till att visa aktivitetstypen</span><span class="sxs-lookup"><span data-stu-id="04954-256">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="04954-257">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="04954-257">Az.DataLakeStore</span></span>
* <span data-ttu-id="04954-258">Korrigering av frysning av Get-DataLakeStoreDeletedItem för fel eller fjärrundantag.</span><span class="sxs-lookup"><span data-stu-id="04954-258">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="04954-259">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="04954-259">Az.EventHub</span></span>
* <span data-ttu-id="04954-260">Korrigering av problem #9658 : Skrivfel i parametern VirtualNteworkRule i Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="04954-260">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="04954-261">Korrigering av problem #9558 : Set-AzEventHubNamespace använder PATCH i stället för PUT</span><span class="sxs-lookup"><span data-stu-id="04954-261">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="04954-262">lade till parametern EnableKafka i Set-AzEventHubNamespace-cmdleten</span><span class="sxs-lookup"><span data-stu-id="04954-262">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="04954-263">Korrigering av problem #9786 : kan inte skapa en regel med Endast lyssna-behörighet</span><span class="sxs-lookup"><span data-stu-id="04954-263">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="04954-264">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="04954-264">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="04954-265">Åtgärdade skrivfel i dokumentation där "Azure" skrevs helt med gemener</span><span class="sxs-lookup"><span data-stu-id="04954-265">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="04954-266">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="04954-266">Az.Monitor</span></span>
* <span data-ttu-id="04954-267">Åtgärdade felaktigt parameternamn i hjälpdokumentationen</span><span class="sxs-lookup"><span data-stu-id="04954-267">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="04954-268">Az.Network</span><span class="sxs-lookup"><span data-stu-id="04954-268">Az.Network</span></span>
* <span data-ttu-id="04954-269">Uppdaterade New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="04954-269">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="04954-270">Gjorde parametern "PublicIpAddress" inaktuell eftersom den aldrig används på serversidan.</span><span class="sxs-lookup"><span data-stu-id="04954-270">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="04954-271">Lade till den valfria parametern "Primary", som anger huruvida den aktuella IP-konfigurationen är den primära.</span><span class="sxs-lookup"><span data-stu-id="04954-271">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="04954-272">Förbättrade hanteringen av felundantag för begärande från SDK – åtgärdar problemet att tidigare SDK-undantag inte hanteras på rätt sätt, vilket leder till att viktig felinformation inte visas</span><span class="sxs-lookup"><span data-stu-id="04954-272">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="04954-273">Justerade valideringslogiken för IPv6-IP-prefix till att kontrollera korrekt IPv6-prefixlängd.</span><span class="sxs-lookup"><span data-stu-id="04954-273">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="04954-274">Uppdaterade Get-AzVirtualNetworkSubnetConfig: Lade till parameter som anges till get av undernätets resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="04954-274">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="04954-275">Uppdaterade beskrivningen av parametern Location för AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="04954-275">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="04954-276">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="04954-276">Az.OperationalInsights</span></span>
* <span data-ttu-id="04954-277">Uppdaterade dokumentation för "New-AzOperationalInsightsLinuxSyslogDataSource"</span><span class="sxs-lookup"><span data-stu-id="04954-277">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="04954-278">Lade till exempel</span><span class="sxs-lookup"><span data-stu-id="04954-278">Added example</span></span>
    - <span data-ttu-id="04954-279">Uppdaterade beskrivningen av parametern "-Name"</span><span class="sxs-lookup"><span data-stu-id="04954-279">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="04954-280">Lade till ett exempel för New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="04954-280">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="04954-281">Ändrade beskrivningen av parametern -Name för New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="04954-281">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="04954-282">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="04954-282">Az.RecoveryServices</span></span>
* <span data-ttu-id="04954-283">Uppdatera "Get-AzRecoveryServicesBackupJobDetail.md"</span><span class="sxs-lookup"><span data-stu-id="04954-283">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="04954-284">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="04954-284">Az.Resources</span></span>
* <span data-ttu-id="04954-285">Lägg till stöd för den nya API-versionen från 2019-05-10 för Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="04954-285">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="04954-286">Lägg till stöd för "copy.count = 0" för variabler, resurser och egenskaper</span><span class="sxs-lookup"><span data-stu-id="04954-286">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="04954-287">Resurser med "condition = false" eller "copy.count = 0" tas bort i complete-läget</span><span class="sxs-lookup"><span data-stu-id="04954-287">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="04954-288">Lägg till ett exempel på tilldelning av princip på prenumerationsnivå i hjälpdokumentationen</span><span class="sxs-lookup"><span data-stu-id="04954-288">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="04954-289">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="04954-289">Az.ServiceBus</span></span>
* <span data-ttu-id="04954-290">Korrigering av problem #9658 : Skrivfel i parametern VirtualNetworkRule i set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="04954-290">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="04954-291">Korrigering av problem #9786 : kan inte skapa en regel med Endast lyssna-behörighet</span><span class="sxs-lookup"><span data-stu-id="04954-291">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="04954-292">Lade till det nya kommandot "Test-AzServiceBusNameAvailability" för att kontrollera namntillgängligheten för kö och ämne</span><span class="sxs-lookup"><span data-stu-id="04954-292">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="04954-293">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="04954-293">Az.ServiceFabric</span></span>
* <span data-ttu-id="04954-294">Åtgärda buggar med tillägg av nodtyps-cmdlet:</span><span class="sxs-lookup"><span data-stu-id="04954-294">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="04954-295">NullReferenceException-bugg när resursgrupp hade annan vmss som inte är relaterad till Service Fabric-klustret.</span><span class="sxs-lookup"><span data-stu-id="04954-295">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="04954-296">Åtgärdar problemet: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="04954-296">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="04954-297">Åtgärda bugg där cmdleten misslyckades om virtualNetwork var i en annan resursgrupp än klustret.</span><span class="sxs-lookup"><span data-stu-id="04954-297">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="04954-298">Åtgärdar problemet: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="04954-298">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="04954-299">AzServiceFabricApplicationCertificate-cmdleten görs inaktuell</span><span class="sxs-lookup"><span data-stu-id="04954-299">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="04954-300">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="04954-300">Az.Sql</span></span>
* <span data-ttu-id="04954-301">Uppdatera dokumentation om gamla gransknings-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="04954-301">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="04954-302">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="04954-302">Az.Storage</span></span>
* <span data-ttu-id="04954-303">Uppdatera hjälpen för Get/Close-AzStorageFileHandle genom att lägga till fler scenarier i cmdlet-exempel och uppdatera parameterbeskrivningar</span><span class="sxs-lookup"><span data-stu-id="04954-303">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="04954-304">Stöd för StandardBlobTier i uppladdningsblob och kopieringsblob</span><span class="sxs-lookup"><span data-stu-id="04954-304">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="04954-305">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="04954-305">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="04954-306">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="04954-306">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="04954-307">Stöd för rehydratiseringsprioritet i kopieringsblob</span><span class="sxs-lookup"><span data-stu-id="04954-307">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="04954-308">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="04954-308">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="04954-309">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="04954-309">Az.Websites</span></span>
* <span data-ttu-id="04954-310">Lägg till klargöranden gällande parametern -AppSettings i Set-AzWebApp och Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="04954-310">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="04954-311">2.5.0 – July 2019</span><span class="sxs-lookup"><span data-stu-id="04954-311">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="04954-312">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="04954-312">Az.Accounts</span></span>
* <span data-ttu-id="04954-313">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="04954-313">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="04954-314">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="04954-314">Az.ApplicationInsights</span></span>
* <span data-ttu-id="04954-315">Korrigera skrivfel i exempel i dokumentationen för Remove-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="04954-315">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="04954-316">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="04954-316">Az.Automation</span></span>
* <span data-ttu-id="04954-317">Korrigera skrivfel i resurssträng</span><span class="sxs-lookup"><span data-stu-id="04954-317">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="04954-318">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="04954-318">Az.CognitiveServices</span></span>
* <span data-ttu-id="04954-319">Stöd för NetworkRuleSet har lagts till.</span><span class="sxs-lookup"><span data-stu-id="04954-319">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="04954-320">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="04954-320">Az.Compute</span></span>
* <span data-ttu-id="04954-321">Lägg till saknade egenskaper (ComputerName, OsName, OsVersion och HyperVGeneration) för visningsobjekt i den virtuella datorinstansen.</span><span class="sxs-lookup"><span data-stu-id="04954-321">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="04954-322">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="04954-322">Az.ContainerRegistry</span></span>
* <span data-ttu-id="04954-323">Åtgärda skrivfel i Remove-AzContainerRegistryReplication för parametern Replication</span><span class="sxs-lookup"><span data-stu-id="04954-323">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="04954-324">Mer information finns här: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="04954-324">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="04954-325">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="04954-325">Az.DataFactory</span></span>
* <span data-ttu-id="04954-326">ADF .Net SDK-versionen har uppdaterats till 4.1.0</span><span class="sxs-lookup"><span data-stu-id="04954-326">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="04954-327">Korrigera skrivfel i dokumentationen för Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="04954-327">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="04954-328">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="04954-328">Az.EventHub</span></span>
* <span data-ttu-id="04954-329">Ny cmmdlet har lagts till för att skapa SAS-token: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="04954-329">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="04954-330">verifierings- och felmeddelande har lagts till för authorizationrules-rättigheter om endast "hantera" har tilldelats</span><span class="sxs-lookup"><span data-stu-id="04954-330">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="04954-331">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="04954-331">Az.KeyVault</span></span>
* <span data-ttu-id="04954-332">Stöd har lagts till för att ange KeySize för certifikatprinciper</span><span class="sxs-lookup"><span data-stu-id="04954-332">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="04954-333">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="04954-333">Az.LogicApp</span></span>
* <span data-ttu-id="04954-334">Korrigering för Get-AzIntegrationAccountMap för att lista alla mappningstyper</span><span class="sxs-lookup"><span data-stu-id="04954-334">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="04954-335">Ny MapType-parameter har lagts till för filtrering</span><span class="sxs-lookup"><span data-stu-id="04954-335">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="04954-336">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="04954-336">Az.ManagedServices</span></span>
* <span data-ttu-id="04954-337">Stöd för API-versionen 2019-06-01 (GA) har lagts till</span><span class="sxs-lookup"><span data-stu-id="04954-337">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="04954-338">Az.Network</span><span class="sxs-lookup"><span data-stu-id="04954-338">Az.Network</span></span>
* <span data-ttu-id="04954-339">Lägg till stöd för privat slutpunkt och privat länktjänst</span><span class="sxs-lookup"><span data-stu-id="04954-339">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="04954-340">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="04954-340">New cmdlets</span></span>
        - <span data-ttu-id="04954-341">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="04954-341">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="04954-342">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="04954-342">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="04954-343">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="04954-343">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="04954-344">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="04954-344">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="04954-345">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="04954-345">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="04954-346">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="04954-346">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="04954-347">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="04954-347">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="04954-348">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="04954-348">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="04954-349">Nedanstående kommandon för funktionen har uppdaterats: Flaggan PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies på undernätet i VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="04954-349">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="04954-350">Uppdaterade New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="04954-350">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="04954-351">Valfri parameter har lagts till – PrivateEndpointNetworkPoliciesFlag som konfigurerar huruvida nätverksprinciper ska tillämpas på en privat slutpunkt i det här undernätet.</span><span class="sxs-lookup"><span data-stu-id="04954-351">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="04954-352">Valfri parameter har lagts till – PrivateLinkServiceNetworkPoliciesFlag som konfigurerar huruvida nätverksprinciper ska tillämpas på en privat länktjänst i det här undernätet.</span><span class="sxs-lookup"><span data-stu-id="04954-352">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="04954-353">AzPrivateLinkService för cmdlet-parametern ServiceName har bytt namn till Name med aliaset ServiceName för bakåtkompatibilitet</span><span class="sxs-lookup"><span data-stu-id="04954-353">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="04954-354">Aktivera ICMP-protokoll för konfiguration av nätverkssäkerhetsregler</span><span class="sxs-lookup"><span data-stu-id="04954-354">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="04954-355">Uppdaterade cmdletar</span><span class="sxs-lookup"><span data-stu-id="04954-355">Updated cmdlets</span></span>
        - <span data-ttu-id="04954-356">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="04954-356">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="04954-357">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="04954-357">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="04954-358">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="04954-358">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="04954-359">Lägg till ConnectionProtocolType (Ikev1/Ikev2) som en konfigurerbar parameter för New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="04954-359">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="04954-360">Lägg till PrivateIpAddressVersion i LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="04954-360">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="04954-361">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="04954-361">Updated cmdlet:</span></span>
        - <span data-ttu-id="04954-362">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="04954-362">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="04954-363">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="04954-363">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="04954-364">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="04954-364">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="04954-365">Uppdatering av Application Gateway-kommandot New-AzApplicationGatewayProbeConfig för stöd av anpassad port i Probe</span><span class="sxs-lookup"><span data-stu-id="04954-365">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="04954-366">Uppdaterade New-AzApplicationGatewayProbeConfig: Den valfria parametern Port som används för avsökning i serverdelen har lagts till.</span><span class="sxs-lookup"><span data-stu-id="04954-366">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="04954-367">Denna parameter gäller för SKU:erna Standard_V2 och WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="04954-367">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="04954-368">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="04954-368">Az.OperationalInsights</span></span>
* <span data-ttu-id="04954-369">Uppdaterade standardversionen för sparade sökningar till 1.</span><span class="sxs-lookup"><span data-stu-id="04954-369">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="04954-370">Åtgärdade hantering av anpassad log null regex</span><span class="sxs-lookup"><span data-stu-id="04954-370">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="04954-371">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="04954-371">Az.RecoveryServices</span></span>
* <span data-ttu-id="04954-372">Uppdatera Get-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="04954-372">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="04954-373">Uppdatera Get-AzRecoveryServicesBackupContainer.md</span><span class="sxs-lookup"><span data-stu-id="04954-373">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="04954-374">Uppdatera Get-AzRecoveryServicesVault.md</span><span class="sxs-lookup"><span data-stu-id="04954-374">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="04954-375">Uppdatera Wait-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="04954-375">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="04954-376">Uppdatera Set-AzRecoveryServicesVaultContext.md</span><span class="sxs-lookup"><span data-stu-id="04954-376">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="04954-377">Uppdatera Get-AzRecoveryServicesBackupItem.md</span><span class="sxs-lookup"><span data-stu-id="04954-377">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="04954-378">Uppdatera Get-AzRecoveryServicesBackupRecoveryPoint.md</span><span class="sxs-lookup"><span data-stu-id="04954-378">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="04954-379">Uppdatera Restore-AzRecoveryServicesBackupItem.md</span><span class="sxs-lookup"><span data-stu-id="04954-379">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="04954-380">Uppdaterat tjänstanrop för avregistrering av container för Azure-filresurs</span><span class="sxs-lookup"><span data-stu-id="04954-380">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="04954-381">Uppdatera Set-AzRecoveryServicesAsrAlertSetting.md</span><span class="sxs-lookup"><span data-stu-id="04954-381">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="04954-382">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="04954-382">Az.Resources</span></span>
- <span data-ttu-id="04954-383">Ta bort den cmdlet som saknas och som refereras i dokumentationen till New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="04954-383">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="04954-384">Princip-cmdletar har uppdaterats så att de använder den nya API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="04954-384">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="04954-385">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="04954-385">Az.ServiceBus</span></span>
* <span data-ttu-id="04954-386">Ny cmmdlet har lagts till för att skapa SAS-token: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="04954-386">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="04954-387">verifierings- och felmeddelande har lagts till för authorizationrules-rättigheter om endast "hantera" har tilldelats</span><span class="sxs-lookup"><span data-stu-id="04954-387">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="04954-388">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="04954-388">Az.Sql</span></span>
* <span data-ttu-id="04954-389">Åtgärda saknade exempel för Set-AzSqlDatabaseSecondary cmdlet</span><span class="sxs-lookup"><span data-stu-id="04954-389">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="04954-390">Åtgärda angivna återkommande genomsökningar för bedömning av säkerhetsrisk utan angivna e-postadresser</span><span class="sxs-lookup"><span data-stu-id="04954-390">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="04954-391">Korrigera ett skrivfel i ett varningsmeddelande.</span><span class="sxs-lookup"><span data-stu-id="04954-391">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="04954-392">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="04954-392">Az.Storage</span></span>
* <span data-ttu-id="04954-393">Uppdatera exempel i referensdokumentationen för Get-AzStorageAccount så att rätt parameternamn används</span><span class="sxs-lookup"><span data-stu-id="04954-393">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="04954-394">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="04954-394">Az.StorageSync</span></span>
* <span data-ttu-id="04954-395">Lägger till cmdleten Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="04954-395">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="04954-396">Åtgärda problem 9551 så att TierFilesOlderThanDays föredras</span><span class="sxs-lookup"><span data-stu-id="04954-396">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="04954-397">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="04954-397">Az.Websites</span></span>
* <span data-ttu-id="04954-398">Åtgärdar ett fel där vissa SiteConfig-egenskaper inte returnerades av Get-AzWebApp och Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="04954-398">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="04954-399">Lägger till en ny platsparameter för Get-AzDeletedWebApp och Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="04954-399">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="04954-400">Åtgärdar ett fel i kloning av webbapp-platser som använder New-AzWebApp-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="04954-400">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="04954-401">2.4.0 – juli 2019</span><span class="sxs-lookup"><span data-stu-id="04954-401">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="04954-402">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="04954-402">Az.Accounts</span></span>
* <span data-ttu-id="04954-403">Lägg till stöd för profil-cmdletar</span><span class="sxs-lookup"><span data-stu-id="04954-403">Add support for profile cmdlets</span></span>
* <span data-ttu-id="04954-404">Lägg till stöd för miljöer och dataplaner i genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="04954-404">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="04954-405">Åtgärda bugg där fel slutpunkt i vissa fall användes för cmdletar för dataplaner i Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="04954-405">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="04954-406">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="04954-406">Az.Advisor</span></span>
* <span data-ttu-id="04954-407">GA-version av Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="04954-407">GA release of Az.Advisor</span></span>
* <span data-ttu-id="04954-408">Den här modulen ingår nu som en del av `Az`-sammanslagningsmodulen</span><span class="sxs-lookup"><span data-stu-id="04954-408">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="04954-409">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="04954-409">Az.ApiManagement</span></span>
* <span data-ttu-id="04954-410">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="04954-410">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="04954-411">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="04954-411">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="04954-412">Stöd för att fråga prenumerationer efter användare och produkt har lagts till</span><span class="sxs-lookup"><span data-stu-id="04954-412">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="04954-413">Stöd för att fråga med hjälp av omfång ”/”, ”/apis”, ”/apis/echo-api” har lagts till</span><span class="sxs-lookup"><span data-stu-id="04954-413">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="04954-414">Korrigering av problem https://github.com/Azure/azure-powershell/issues/9307 och https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="04954-414">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="04954-415">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="04954-415">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="04954-416">Stöd för att ange ”ApiVersion” och ”ApiVersionSetId” när API:er importeras har lagts till</span><span class="sxs-lookup"><span data-stu-id="04954-416">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="04954-417">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="04954-417">Az.Automation</span></span>
* <span data-ttu-id="04954-418">Bugg med cmdleten Set-AzAutomationConnectionFieldValue för att hantera strängvärde har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="04954-418">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="04954-419">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="04954-419">Az.Compute</span></span>
* <span data-ttu-id="04954-420">Lägg till parametern HyperVGeneration i New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="04954-420">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="04954-421">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="04954-421">Az.DataFactory</span></span>
* <span data-ttu-id="04954-422">Uppdaterar utdata från ADF-cmdletar som hämtar aktivitetskörningar, hämtar pipelinekörningar och hämtar utlösarkörningar för stöd för Select-Object-pipe.</span><span class="sxs-lookup"><span data-stu-id="04954-422">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="04954-423">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="04954-423">Az.EventGrid</span></span>
* <span data-ttu-id="04954-424">Korrigera stavfel i dokumentation om ”New-AzEventGridSubscription”</span><span class="sxs-lookup"><span data-stu-id="04954-424">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="04954-425">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="04954-425">Az.IotHub</span></span>
* <span data-ttu-id="04954-426">Lägg till stöd för att återskapa principnycklar för auktorisering.</span><span class="sxs-lookup"><span data-stu-id="04954-426">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="04954-427">Az.Network</span><span class="sxs-lookup"><span data-stu-id="04954-427">Az.Network</span></span>
* <span data-ttu-id="04954-428">”RoutingPreference” har lagts till i offentliga IP-taggar</span><span class="sxs-lookup"><span data-stu-id="04954-428">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="04954-429">Förbättra exempel för referensdokumentation om ”Get-AzNetworkServiceTag”</span><span class="sxs-lookup"><span data-stu-id="04954-429">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="04954-430">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="04954-430">Az.PolicyInsights</span></span>
* <span data-ttu-id="04954-431">Åtgärda problem med null-referens i Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="04954-431">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="04954-432">Mer information här: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="04954-432">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="04954-433">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="04954-433">Az.OperationalInsights</span></span>
* <span data-ttu-id="04954-434">Modellen för CustomLog-datakälla som returneras i Get-AzOperationalInsightsDataSource har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="04954-434">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="04954-435">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="04954-435">Az.RecoveryServices</span></span>
* <span data-ttu-id="04954-436">Kommandot get-policy för IaaSVM:er har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="04954-436">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="04954-437">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="04954-437">Az.Resources</span></span>
    - <span data-ttu-id="04954-438">Korrigera hjälptext för den översta parametern i Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="04954-438">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="04954-439">Lägg till växlingsstöd på klientsidan för Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="04954-439">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="04954-440">Lägg till nya parametrar för Set-AzPolicyAssignment, -PolicyParameters och -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="04954-440">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="04954-441">En mängd dokument- och exempeluppdateringar för Policy-cmdletar</span><span class="sxs-lookup"><span data-stu-id="04954-441">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="04954-442">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="04954-442">Az.ServiceBus</span></span>
* <span data-ttu-id="04954-443">Korrigering av problem #4938 – New-AzureRmServiceBusQueue returnerar BadRequest vid konfiguration av MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="04954-443">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="04954-444">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="04954-444">Az.Sql</span></span>
* <span data-ttu-id="04954-445">Lägg till cmdletar för instansredundansgrupper från förhandsversion till offentlig version</span><span class="sxs-lookup"><span data-stu-id="04954-445">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="04954-446">Stöd för granskning för Azure SQL Server\Database med nya cmdletar.</span><span class="sxs-lookup"><span data-stu-id="04954-446">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="04954-447">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="04954-447">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="04954-448">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="04954-448">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="04954-449">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="04954-449">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="04954-450">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="04954-450">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="04954-451">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="04954-451">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="04954-452">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="04954-452">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="04954-453">Ta bort begränsningar för e-post från inställningarna för sårbarhetsbedömning</span><span class="sxs-lookup"><span data-stu-id="04954-453">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="04954-454">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="04954-454">Az.Storage</span></span>
* <span data-ttu-id="04954-455">Ändra två parametrar ”-IndexDocument” och ”-ErrorDocument404Path” från ”krävs” till ”valfri” i cmdlet:</span><span class="sxs-lookup"><span data-stu-id="04954-455">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="04954-456">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="04954-456">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="04954-457">Uppdatera hjälpen för Get-AzStorageBlobContent genom att lägga till ett exempel</span><span class="sxs-lookup"><span data-stu-id="04954-457">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="04954-458">Visa mer felinformation när cmdleten misslyckas med StorageException</span><span class="sxs-lookup"><span data-stu-id="04954-458">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="04954-459">Stöd för att skapa eller uppdatera lagringskonto med Azure Files AAD DS-autentisering</span><span class="sxs-lookup"><span data-stu-id="04954-459">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="04954-460">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="04954-460">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="04954-461">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="04954-461">Set-AzStorageAccount</span></span>
* <span data-ttu-id="04954-462">Stöd för att lista eller stänga filreferenser för en filresurs, filkatalog eller en fil</span><span class="sxs-lookup"><span data-stu-id="04954-462">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="04954-463">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="04954-463">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="04954-464">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="04954-464">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="04954-465">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="04954-465">Az.StorageSync</span></span>
* <span data-ttu-id="04954-466">Den här modulen ingår nu som en del av `Az`-sammanslagningsmodulen</span><span class="sxs-lookup"><span data-stu-id="04954-466">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="04954-467">2.3.2 – juni 2019</span><span class="sxs-lookup"><span data-stu-id="04954-467">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="04954-468">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="04954-468">Az.Accounts</span></span>
* <span data-ttu-id="04954-469">Åtgärda bugg med felaktiga webbadresser som i vissa fall användes för Functions-anrop</span><span class="sxs-lookup"><span data-stu-id="04954-469">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="04954-470">Mer information här: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="04954-470">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="04954-471">Åtgärda problem med alias från AzureRM i Az-cmdletar</span><span class="sxs-lookup"><span data-stu-id="04954-471">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="04954-472">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="04954-472">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="04954-473">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="04954-473">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="04954-474">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="04954-474">Az.Compute</span></span>
* <span data-ttu-id="04954-475">Parameteruppsättningarna New-AzVm och New-AzVmss accepterar nu parametern ”ProximityPlacementGroup”.</span><span class="sxs-lookup"><span data-stu-id="04954-475">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="04954-476">Stavfel i referensdokumentationen för ”New-AzVM” har korrigerats</span><span class="sxs-lookup"><span data-stu-id="04954-476">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="04954-477">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="04954-477">Az.Dns</span></span>
* <span data-ttu-id="04954-478">Stavfel i hjälpexempel för ”Set-AzDnsZone” har korrigerats.</span><span class="sxs-lookup"><span data-stu-id="04954-478">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="04954-479">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="04954-479">Az.EventGrid</span></span>
* <span data-ttu-id="04954-480">Har uppdaterats för att använda API-versionen 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="04954-480">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="04954-481">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="04954-481">New cmdlets:</span></span>
    - <span data-ttu-id="04954-482">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="04954-482">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="04954-483">Skapar en ny Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="04954-483">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="04954-484">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="04954-484">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="04954-485">Hämtar information om en Event Grid-domän eller hämtar en lista med alla Event Grid-domäner i den aktuella Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="04954-485">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="04954-486">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="04954-486">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="04954-487">Tar bort en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="04954-487">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="04954-488">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="04954-488">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="04954-489">Återskapar nyckeln för delad åtkomst för en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="04954-489">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="04954-490">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="04954-490">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="04954-491">Hämtar de nycklar för delad åtkomst som används för att publicera händelser till en Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="04954-491">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="04954-492">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="04954-492">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="04954-493">Skapar ett nytt Azure Event Grid-domänämne.</span><span class="sxs-lookup"><span data-stu-id="04954-493">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="04954-494">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="04954-494">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="04954-495">Hämtar information om ett Event Grid-domänämne eller hämtar en lista med alla Event Grid-domänämnen under en specifik Event Grid-domän i nuvarande Azure</span><span class="sxs-lookup"><span data-stu-id="04954-495">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="04954-496">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="04954-496">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="04954-497">Tar bort ett befintligt Azure Event Grid-domänämne.</span><span class="sxs-lookup"><span data-stu-id="04954-497">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="04954-498">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="04954-498">Updated cmdlets:</span></span>
    - <span data-ttu-id="04954-499">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="04954-499">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="04954-500">Lägg till nya obligatoriska parametrar för att stödja piping för den nya Event Grid-domänen och Event Grid-domänämnet för att göra det möjligt att skapa nya händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="04954-500">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="04954-501">Lägg till nya obligatoriska parametrar för att ange det nya Event Grid-domännamnet och/eller namnet på Event Grid-domänämnet för att göra det möjligt att skapa nya händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="04954-501">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="04954-502">Lägg till ny parameteruppsättningar för domäner och domänämnen för att göra det möjligt att återanvända befintliga parametrar (t.ex. EndPointType, SubjectBeginsWith osv).</span><span class="sxs-lookup"><span data-stu-id="04954-502">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="04954-503">Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="04954-503">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="04954-504">Förfallodatum för händelseprenumeration</span><span class="sxs-lookup"><span data-stu-id="04954-504">Event subscription expiration date,</span></span>
            - <span data-ttu-id="04954-505">Avancerade filterparametrar.</span><span class="sxs-lookup"><span data-stu-id="04954-505">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="04954-506">Lägg till ny uppräkning för servicebusqueue som mål.</span><span class="sxs-lookup"><span data-stu-id="04954-506">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="04954-507">Tillåt inte användning av ”Alla” i alternativet -IncludedEventType och ersätt det med</span><span class="sxs-lookup"><span data-stu-id="04954-507">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="04954-508">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="04954-508">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="04954-509">Lägg till ny valfria parametrar (Top, ODataQuery och NextLink) för att stödja sidnumrering och filtrering av resultat.</span><span class="sxs-lookup"><span data-stu-id="04954-509">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="04954-510">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="04954-510">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="04954-511">Lägg till nya obligatoriska parametrar för att stödja piping för en Event Grid-domän och Event Grid-domänämnen för att göra det möjligt att ta bort befintliga händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="04954-511">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="04954-512">Lägg till nya obligatoriska parametrar för att ange Event Grid-domännamnet och/eller namnet på Event Grid-domänämnet för att göra det möjligt att ta bort befintliga händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="04954-512">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="04954-513">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="04954-513">Az.FrontDoor</span></span>
* <span data-ttu-id="04954-514">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="04954-514">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="04954-515">Lägg till stöd för transformeringar och nytt värde för automatisk komplettering för operatorer (RegEx)</span><span class="sxs-lookup"><span data-stu-id="04954-515">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="04954-516">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="04954-516">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="04954-517">Lägg till nya värden för automatisk komplettering</span><span class="sxs-lookup"><span data-stu-id="04954-517">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="04954-518">Az.Network</span><span class="sxs-lookup"><span data-stu-id="04954-518">Az.Network</span></span>
* <span data-ttu-id="04954-519">Lägg till stöd för resurs för virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="04954-519">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="04954-520">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="04954-520">New cmdlets</span></span>
        - <span data-ttu-id="04954-521">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="04954-521">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="04954-522">Lägg till AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="04954-522">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="04954-523">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="04954-523">New cmdlets</span></span> 
        - <span data-ttu-id="04954-524">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="04954-524">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="04954-525">Lägg till PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="04954-525">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="04954-526">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="04954-526">New cmdlets</span></span> 
        - <span data-ttu-id="04954-527">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="04954-527">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="04954-528">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="04954-528">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="04954-529">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="04954-529">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="04954-530">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="04954-530">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="04954-531">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="04954-531">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="04954-532">Lägg till PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="04954-532">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="04954-533">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="04954-533">New cmdlets</span></span>
        - <span data-ttu-id="04954-534">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="04954-534">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="04954-535">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="04954-535">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="04954-536">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="04954-536">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="04954-537">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="04954-537">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="04954-538">Nedanstående kommandon för funktionen har uppdaterats: Flaggan UseLocalAzureIpAddress på VpnConnection</span><span class="sxs-lookup"><span data-stu-id="04954-538">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="04954-539">New-AzVpnConnection har uppdaterats: Den valfria parametern -UseLocalAzureIpAddress har lagts till för att visa att en lokal IP-adress i Azure ska användas som källadress när anslutningen initieras.</span><span class="sxs-lookup"><span data-stu-id="04954-539">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="04954-540">Set-AzVpnConnection har uppdaterats: Den valfria parametern -UseLocalAzureIpAddress har lagts till för att visa att en lokal IP-adress i Azure ska användas som källadress när anslutningen initieras.</span><span class="sxs-lookup"><span data-stu-id="04954-540">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="04954-541">Det skrivskyddade fältet PeeredConnections har lagts till i ExpressRoute-peering.</span><span class="sxs-lookup"><span data-stu-id="04954-541">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="04954-542">Det skrivskyddade fältet GlobalReachEnabled har lagts till i ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="04954-542">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="04954-543">Ett attribut för icke-bakåtkompatibla ändringar har lagts till för att lyfta fram utfasning av fältet AllowGlobalReach i modellen ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="04954-543">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="04954-544">Problem 8756 har åtgärdats: Fel vid användning av TargetListenerID med AzApplicationGatewayRedirectConfiguration-cmdletar</span><span class="sxs-lookup"><span data-stu-id="04954-544">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="04954-545">En bugg i New-AzApplicationGatewayPathRuleConfig som gjorde att regeluppsättningen för att återskapa inte kunde anges har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="04954-545">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="04954-546">Visningen av VirtualNetworkTaps i NetworkInterfaceIpConfiguration har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="04954-546">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="04954-547">Cortex Get-cmdletar för att visa en lista med alla delar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="04954-547">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="04954-548">Funktionen för att skapa VirtualHub-referenser för ExpressRouteGateways och VpnGateway har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="04954-548">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="04954-549">Stöd för tillgänglighetszoner i AzureFirewall och NatGateway har lagts till</span><span class="sxs-lookup"><span data-stu-id="04954-549">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="04954-550">Cmdleten Get-AzNetworkServiceTag har lagts till</span><span class="sxs-lookup"><span data-stu-id="04954-550">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="04954-551">Lägg till stöd för flera offentliga IP-adresser för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="04954-551">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="04954-552">Cmdleten New-AzFirewall har uppdaterats:</span><span class="sxs-lookup"><span data-stu-id="04954-552">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="04954-553">Parametern -PublicIpAddress som accepterar ett eller flera offentliga IP-adressobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="04954-553">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="04954-554">Parametern -VirtualNetwork som accepterar ett virtuellt nätverksobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="04954-554">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="04954-555">Metoderna AddPublicIpAddress och RemovePublicIpAddress har lagts till på brandväggsobjekt – dessa accepterar ett offentligt IP-adressobjekt som indata</span><span class="sxs-lookup"><span data-stu-id="04954-555">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="04954-556">Inaktuella parametrar -PublicIpName och -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="04954-556">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="04954-557">Nedanstående kommandon för funktionen har uppdaterats: Ange autentiseringsalternativ för VpnClient AAD till resurser för virtuella nätverksgatewayer.</span><span class="sxs-lookup"><span data-stu-id="04954-557">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="04954-558">New-AzVirtualNetworkGateway har uppdaterats: De valfria parametrarna AadTenantUri, AadAudienceId och AadIssuerUri för att ange VpnClient AAD-autentiseringsalternativ på en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="04954-558">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="04954-559">Set-AzVirtualNetworkGateway har uppdaterats: De valfria parametrarna AadTenantUri, AadAudienceId och AadIssuerUri för att ange VpnClient AAD-autentiseringsalternativ på en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="04954-559">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="04954-560">Set-AzVirtualNetworkGateway har uppdaterats: Den valfria växelparametern RemoveAadAuthentication som tar bort VpnClient AAD-autentiseringsalternativ från en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="04954-560">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="04954-561">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="04954-561">Az.OperationalInsights</span></span>
* <span data-ttu-id="04954-562">Aktivera prisnivån **pergb2018** i kommandot ”New-AzureRmOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="04954-562">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="04954-563">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="04954-563">Az.Resources</span></span>
* <span data-ttu-id="04954-564">Stöd för ytterligare alternativ för att exportera en mall</span><span class="sxs-lookup"><span data-stu-id="04954-564">Support for additional Template Export options</span></span>
    - <span data-ttu-id="04954-565">Lägg till parametern ”-SkipResourceNameParameterization” till Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="04954-565">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="04954-566">Lägg till parametern ”-SkipAllParameterization” till Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="04954-566">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="04954-567">Lägg till parametern ”-Resource” till Export-AzResourceGroup för exporterad resursfiltrering</span><span class="sxs-lookup"><span data-stu-id="04954-567">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="04954-568">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="04954-568">Az.ServiceFabric</span></span>
* <span data-ttu-id="04954-569">Åtgärda att fel tumavtryck används vid tilläggning av certifikat i ByExistingKeyVault i vissa fall</span><span class="sxs-lookup"><span data-stu-id="04954-569">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="04954-570">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="04954-570">Az.Sql</span></span>
* <span data-ttu-id="04954-571">Åtgärda suffix för lagringsslutpunkt i Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="04954-571">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="04954-572">Åtgärda att aktivering av Advanced Data Security åsidosätter Advanced Threat Protection-princip</span><span class="sxs-lookup"><span data-stu-id="04954-572">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="04954-573">Nya cmdletar för Management.Sql som gör att kunderna kan lägga till nycklar för transparent datakryptering (TDE) och ange TDE-skydd för hanterade instanser</span><span class="sxs-lookup"><span data-stu-id="04954-573">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="04954-574">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="04954-574">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="04954-575">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="04954-575">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="04954-576">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="04954-576">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="04954-577">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="04954-577">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="04954-578">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="04954-578">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="04954-579">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="04954-579">Az.Storage</span></span>
* <span data-ttu-id="04954-580">Stöd för typerna FileStorage och SkuName Premium_ZRS när lagringskonton skapas</span><span class="sxs-lookup"><span data-stu-id="04954-580">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="04954-581">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="04954-581">New-AzStorageAccount</span></span>
* <span data-ttu-id="04954-582">Beskrivningen av cmdleten för bloboföränderlighet har förtydligats</span><span class="sxs-lookup"><span data-stu-id="04954-582">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="04954-583">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="04954-583">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="04954-584">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="04954-584">Az.Websites</span></span>
* <span data-ttu-id="04954-585">Optimerar Get-AzWebAppCertificate för att filtrera efter resursgrupp på servern i stället för klienten</span><span class="sxs-lookup"><span data-stu-id="04954-585">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="04954-586">Lägger till växlingsparametern -UseDisasterRecovery till Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="04954-586">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="04954-587">2.2.0 – juni 2019</span><span class="sxs-lookup"><span data-stu-id="04954-587">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="04954-588">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="04954-588">Az.Cdn</span></span>
* <span data-ttu-id="04954-589">Uppdaterade cmdletar för att ge stöd för rulesEngine-funktion baserat på API-version 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="04954-589">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="04954-590">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="04954-590">Az.Compute</span></span>
* <span data-ttu-id="04954-591">Lade till parameter `NoWait` som startar åtgärden och returnerar omedelbart, innan åtgärden har slutförts.</span><span class="sxs-lookup"><span data-stu-id="04954-591">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="04954-592">Uppdaterade cmdletar:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="04954-592">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="04954-593">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="04954-593">Az.EventHub</span></span>
* <span data-ttu-id="04954-594">Korrigering för #9231 – Get-AzEventHubNamespace returnerar inga taggar</span><span class="sxs-lookup"><span data-stu-id="04954-594">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="04954-595">Korrigering för #9230 – Get-AzEventHubNamespace returnerar ResourceGroup istället för ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04954-595">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="04954-596">Az.Network</span><span class="sxs-lookup"><span data-stu-id="04954-596">Az.Network</span></span>
* <span data-ttu-id="04954-597">Uppdatera ResourceId och InputObject för NAT-gateway</span><span class="sxs-lookup"><span data-stu-id="04954-597">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="04954-598">Lägg till alias för ResourceId och InputObject</span><span class="sxs-lookup"><span data-stu-id="04954-598">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="04954-599">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="04954-599">Az.PolicyInsights</span></span>
* <span data-ttu-id="04954-600">Åtgärda Null-referensproblem i Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="04954-600">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="04954-601">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="04954-601">Az.RecoveryServices</span></span>
* <span data-ttu-id="04954-602">Minsta kvarhållning för IaaSVM-policy i dagar ändrat till 7 från 1</span><span class="sxs-lookup"><span data-stu-id="04954-602">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="04954-603">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="04954-603">Az.ServiceBus</span></span>
* <span data-ttu-id="04954-604">Korrigering för ärende #9182 – Get-AzServiceBusNamespace returnerar ResourceGroup istället för ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04954-604">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="04954-605">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="04954-605">Az.ServiceFabric</span></span>
* <span data-ttu-id="04954-606">Åtgärda stavfel i felmeddelandet för Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="04954-606">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="04954-607">Åtgärda saknat tecken i Service Fabric-kommandorader</span><span class="sxs-lookup"><span data-stu-id="04954-607">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="04954-608">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="04954-608">Az.Sql</span></span>
* <span data-ttu-id="04954-609">Lägg till parametern DnsZonePartner för New-AzureSqlInstance-cmdlet för att ge stöd för AutoDr för hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="04954-609">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="04954-610">Avvecklar cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="04954-610">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="04954-611">Döp om cmdletar för hotidentifiering till Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="04954-611">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="04954-612">Parametrarna New-AzSqlInstance -StorageSizeInGB och -LicenseType är nu valfria.</span><span class="sxs-lookup"><span data-stu-id="04954-612">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="04954-613">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="04954-613">Az.Websites</span></span>
* <span data-ttu-id="04954-614">åtgärdar problemet där användningen av Set-AzWebApp och Set-AzWebAppSlot med -WebApp-egenskap tog bort taggarna</span><span class="sxs-lookup"><span data-stu-id="04954-614">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="04954-615">2.1.0 – maj 2019</span><span class="sxs-lookup"><span data-stu-id="04954-615">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="04954-616">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="04954-616">Az.ApiManagement</span></span>
* <span data-ttu-id="04954-617">Skapade nya cmdletar för att hantera diagnostik för global- och API-omfång</span><span class="sxs-lookup"><span data-stu-id="04954-617">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="04954-618">**Get-AzApiManagementDiagnostic** – Skaffa diagnostik konfigurerad för global- eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="04954-618">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="04954-619">**New-AzApiManagementDiagnostic** – Skapa ny diagnostik för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="04954-619">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="04954-620">**New-AzApiManagementHttpMessageDiagnostic** – Skapa diagnostikinställning om vilka rubriker som ska loggas och storleken på brödtextbyte</span><span class="sxs-lookup"><span data-stu-id="04954-620">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="04954-621">**New-AzApiManagementPipelineDiagnosticSetting** – Skapa diagnostikinställningar för inkommande/utgående HTTP-meddelanden till gatewayen.</span><span class="sxs-lookup"><span data-stu-id="04954-621">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="04954-622">**New-AzApiManagementSamplingSetting** – Skapa samplinginställningar för begäranden/svar för en diagnostik</span><span class="sxs-lookup"><span data-stu-id="04954-622">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="04954-623">**Remove-AzApiManagementDiagnostic** – Ta bort en diagnostikenhet för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="04954-623">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="04954-624">**Set-AzApiManagementDiagnostic** – Uppdatera en diagnostikenhet för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="04954-624">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="04954-625">Skapade nya cmdletar för hantering av cacheminne i ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="04954-625">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="04954-626">**Get-AzApiManagementCache** – Hämta information om cacheminnet som anges av identifierare eller alla cacheminnen</span><span class="sxs-lookup"><span data-stu-id="04954-626">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="04954-627">**New-AzApiManagementCache** – Skapa ett nytt default-cacheminne eller cacheminne i en viss Azure-region</span><span class="sxs-lookup"><span data-stu-id="04954-627">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="04954-628">**Remove-AzApiManagementCache** – Ta bort ett cacheminne</span><span class="sxs-lookup"><span data-stu-id="04954-628">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="04954-629">**Remove-AzApiManagementCache** – Ta bort ett cacheminne</span><span class="sxs-lookup"><span data-stu-id="04954-629">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="04954-630">Skapade nya cmdletar för hantering av API-schema</span><span class="sxs-lookup"><span data-stu-id="04954-630">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="04954-631">**New-AzApiManagementSchema** – Skapa ett nytt schema för ett API</span><span class="sxs-lookup"><span data-stu-id="04954-631">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="04954-632">**Get-AzApiManagementSchema** – Hämta de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="04954-632">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="04954-633">**Remove-AzApiManagementSchema** – Ta bort de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="04954-633">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="04954-634">**Set-AzApiManagementSchema** – Uppdatera de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="04954-634">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="04954-635">Skapa ny cmdlet för att generera en användartoken.</span><span class="sxs-lookup"><span data-stu-id="04954-635">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="04954-636">**New-AzApiManagementUserToken** – Skapa en ny användartoken som enligt standardinställning är giltig i 8 timmar. Token för GIT-användaren kan skapas med den här cmdleten./</span><span class="sxs-lookup"><span data-stu-id="04954-636">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="04954-637">Skapade en ny cmdlet för att hämta nätverksstatus</span><span class="sxs-lookup"><span data-stu-id="04954-637">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="04954-638">**Get-AzApiManagementNetworkStatus** – Hämta nätverksstatusanslutningen för resurserna som API Management-tjänsten är beroende av.</span><span class="sxs-lookup"><span data-stu-id="04954-638">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="04954-639">Det här är användbart när du distribuerar ApiManagement-tjänsten i ett virtuellt nätverk och validerar om något beroende är brutet.</span><span class="sxs-lookup"><span data-stu-id="04954-639">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="04954-640">Uppdaterade cmdlet **New-AzApiManagement** för att hantera ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="04954-640">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="04954-641">Lade till stöd för den nya SKU:n Consumption</span><span class="sxs-lookup"><span data-stu-id="04954-641">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="04954-642">Aktiverade stöd för att slå på flaggan EnableClientCertificate för SKU:n Consumption</span><span class="sxs-lookup"><span data-stu-id="04954-642">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="04954-643">Den nya cmdleten **New-AzApiManagementSslSetting** gör det möjligt att ställa in TLS/SSL-inställningen på ”Backend” och ”Frontend” (serverdel och klientdel).</span><span class="sxs-lookup"><span data-stu-id="04954-643">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="04954-644">Det här kan också användas till att konfigurera chiffer som 3DES och ServerProtocols som Http2 för Frontend för en ApiManagement-tjänst.</span><span class="sxs-lookup"><span data-stu-id="04954-644">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="04954-645">Stöd har lagts till för att konfigurera värdnamnet DeveloperPortal på ApiManagement-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="04954-645">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="04954-646">Uppdaterade cmdletar **Get-AzApiManagementSsoToken** för att ta PsApiManagement-objekt som indata</span><span class="sxs-lookup"><span data-stu-id="04954-646">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="04954-647">Uppdaterad cmdleten för att visa infogade felmeddelanden</span><span class="sxs-lookup"><span data-stu-id="04954-647">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="04954-648">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Felkod: Felmeddelande av typen ValidationError: Ett eller flera fält innehåller felaktiga värden: Felinformation:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="04954-648">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="04954-649">Uppdaterade cmdlet **Export-AzApiManagementApi** för att exportera API:er i OpenApi 3.0-format</span><span class="sxs-lookup"><span data-stu-id="04954-649">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="04954-650">Uppdaterade cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="04954-650">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="04954-651">Importera API från dokumentspecifikationen OpenApi 3.0</span><span class="sxs-lookup"><span data-stu-id="04954-651">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="04954-652">Om du vill åsidosätta egenskapen PsApiManagementSchema specificerad i ett dokument (Swagger, Wadl, Wsdl, OpenApi).</span><span class="sxs-lookup"><span data-stu-id="04954-652">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="04954-653">Åsidosätta egenskapen ServiceUrl som specificeras i ett dokument.</span><span class="sxs-lookup"><span data-stu-id="04954-653">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="04954-654">Uppdaterade cmdlet **Get-AzApiManagementPolicy** för att returnera policy i undantaget format av typen icke-XML med rawxml</span><span class="sxs-lookup"><span data-stu-id="04954-654">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="04954-655">Uppdaterade cmdlet **Set-AzApiManagementPolicy** för att godkänna policy i undantaget format av typen icke-XML med rawxml och XML undantaget med xml</span><span class="sxs-lookup"><span data-stu-id="04954-655">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="04954-656">Uppdaterad cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="04954-656">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="04954-657">Konfigurera API med OpenId auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="04954-657">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="04954-658">Skapa ett API i ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="04954-658">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="04954-659">Klona ett API med SourceApiId och SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="04954-659">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="04954-660">Möjlighet att konfigurera SubscriptionRequired i API-omfattningen.</span><span class="sxs-lookup"><span data-stu-id="04954-660">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="04954-661">Uppdaterad cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="04954-661">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="04954-662">Konfigurera API med OpenId auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="04954-662">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="04954-663">Uppdatera ett API till ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="04954-663">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="04954-664">Möjlighet att konfigurera SubscriptionRequired i API-omfattningen.</span><span class="sxs-lookup"><span data-stu-id="04954-664">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="04954-665">Uppdaterad cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="04954-665">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="04954-666">Klona en befintlig version med hjälp av SourceApiRevision (kopiera taggar, produkter, åtgärder och principer).</span><span class="sxs-lookup"><span data-stu-id="04954-666">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="04954-667">Den nya revisionen antar ApiId från den överordnade instansen.</span><span class="sxs-lookup"><span data-stu-id="04954-667">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="04954-668">Tillhandahålla ApiRevisionDescription</span><span class="sxs-lookup"><span data-stu-id="04954-668">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="04954-669">Åsidosätta ServiceUrl vid kloning av ett API.</span><span class="sxs-lookup"><span data-stu-id="04954-669">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="04954-670">Uppdaterad cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="04954-670">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="04954-671">Konfigurera AAD eller AADB2C med en Authority</span><span class="sxs-lookup"><span data-stu-id="04954-671">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="04954-672">Konfigurera SignupPolicy, SigninPolicy, ProfileEditingPolicy och PasswordResetPolicy</span><span class="sxs-lookup"><span data-stu-id="04954-672">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="04954-673">Uppdaterad cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="04954-673">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="04954-674">Kompensera för ny SubscriptonModel med Scope och UserId</span><span class="sxs-lookup"><span data-stu-id="04954-674">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="04954-675">Kompensera för gammal prenumerationsmodell med ProductId och UserId</span><span class="sxs-lookup"><span data-stu-id="04954-675">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="04954-676">Lägg till funktion för att aktivera AllowTracing på prenumerationsnivå.</span><span class="sxs-lookup"><span data-stu-id="04954-676">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="04954-677">Uppdaterad cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="04954-677">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="04954-678">Kompensera för ny SubscriptonModel med Scope och UserId</span><span class="sxs-lookup"><span data-stu-id="04954-678">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="04954-679">Kompensera för gammal prenumerationsmodell med ProductId och UserId</span><span class="sxs-lookup"><span data-stu-id="04954-679">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="04954-680">Lägg till funktion för att aktivera AllowTracing på prenumerationsnivå.</span><span class="sxs-lookup"><span data-stu-id="04954-680">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="04954-681">Uppdaterade följande cmdletar för att acceptera ResourceId som indata</span><span class="sxs-lookup"><span data-stu-id="04954-681">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="04954-682">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="04954-682">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="04954-683">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="04954-683">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="04954-684">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="04954-684">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="04954-685">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="04954-685">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="04954-686">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="04954-686">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="04954-687">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="04954-687">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="04954-688">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="04954-688">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="04954-689">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="04954-689">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="04954-690">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="04954-690">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="04954-691">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="04954-691">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="04954-692">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="04954-692">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="04954-693">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="04954-693">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="04954-694">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="04954-694">Az.Automation</span></span>
* <span data-ttu-id="04954-695">Uppdaterade Get-AzAutomationJobOutputRecord för att hantera postvärden av typen JSON och Text.</span><span class="sxs-lookup"><span data-stu-id="04954-695">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="04954-696">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="04954-696">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="04954-697">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="04954-697">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="04954-698">Ändrade beteende för Start-AzAutomationDscCompilationJob till att bara starta jobbet istället för att vänta på slutförandet.</span><span class="sxs-lookup"><span data-stu-id="04954-698">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="04954-699">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="04954-699">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="04954-700">Korrigering för Get-AzAutomationDscNode när using -Name returnerar alla noder.</span><span class="sxs-lookup"><span data-stu-id="04954-700">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="04954-701">Nu returnerar den endast den matchande noden.</span><span class="sxs-lookup"><span data-stu-id="04954-701">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="04954-702">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="04954-702">Az.Compute</span></span>
* <span data-ttu-id="04954-703">Lägg till parametrarna ProtectFromScaleIn och ProtectFromScaleSetAction i cmdleten Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="04954-703">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="04954-704">Nu är standardinställningen att vimpelparametern New-AzVM använder en tillgänglig plats om USA, östra inte stöds</span><span class="sxs-lookup"><span data-stu-id="04954-704">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="04954-705">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="04954-705">Az.DataLakeStore</span></span>
* <span data-ttu-id="04954-706">Uppdatera ADLS-sdk för att använda httpclient, integrera dataplanstestning med Azure-ramverk</span><span class="sxs-lookup"><span data-stu-id="04954-706">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="04954-707">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="04954-707">Az.Monitor</span></span>
* <span data-ttu-id="04954-708">Korrigera felaktiga parameternamn i hjälpexempel</span><span class="sxs-lookup"><span data-stu-id="04954-708">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="04954-709">Az.Network</span><span class="sxs-lookup"><span data-stu-id="04954-709">Az.Network</span></span>
* <span data-ttu-id="04954-710">Lägg till flaggan DisableBgpRoutePropagation i utdata för effektiv routningstabell</span><span class="sxs-lookup"><span data-stu-id="04954-710">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="04954-711">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="04954-711">Updated cmdlet:</span></span>
        - <span data-ttu-id="04954-712">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="04954-712">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="04954-713">Åtgärda dubbelstreck i dokumentationen New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="04954-713">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="04954-714">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="04954-714">Az.Resources</span></span>
* <span data-ttu-id="04954-715">Lägg till ny cmdlet Get-AzureRmDenyAssignment för att hämta tilldelningsnekanden</span><span class="sxs-lookup"><span data-stu-id="04954-715">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="04954-716">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="04954-716">Az.Sql</span></span>
* <span data-ttu-id="04954-717">Döp om Advanced Threat Protection-cmdletar för Advanced Data Security och aktivera Vulnerability Assessment som standard</span><span class="sxs-lookup"><span data-stu-id="04954-717">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="04954-718">2.0.0 – maj 2019</span><span class="sxs-lookup"><span data-stu-id="04954-718">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="04954-719">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="04954-719">Az.Accounts</span></span>
* <span data-ttu-id="04954-720">Uppdatera autentiseringsbiblioteket för att åtgärda ADFS-problem med autentisering av användarnamn/lösenord</span><span class="sxs-lookup"><span data-stu-id="04954-720">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="04954-721">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="04954-721">Az.CognitiveServices</span></span>
* <span data-ttu-id="04954-722">Visa endast Bing-ansvarsfriskrivning för Bing-sökningstjänster.</span><span class="sxs-lookup"><span data-stu-id="04954-722">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="04954-723">Förbättra felmeddelande när det inte går att skapa konton.</span><span class="sxs-lookup"><span data-stu-id="04954-723">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="04954-724">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="04954-724">Az.Compute</span></span>
* <span data-ttu-id="04954-725">Funktion för närhetsplaceringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="04954-725">Proximity placement group feature.</span></span>
    - <span data-ttu-id="04954-726">Följande nya cmdletar har lagts till:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="04954-726">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="04954-727">Den nya parametern ProximityPlacementGroupId har lagts till i följande cmdletar:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="04954-727">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="04954-728">Parametern StorageAccountType har lagts till i New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="04954-728">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="04954-729">TargetRegion för New-AzGalleryImageVersion kan innehålla StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="04954-729">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="04954-730">Växlingsparametern SkipShutdown har lagts till i Stop-AzVM och Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="04954-730">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="04954-731">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="04954-731">Breaking changes</span></span>
    - <span data-ttu-id="04954-732">Set-AzVMBootDiagnostics har ändrats till Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="04954-732">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="04954-733">Export-AzLogAnalyticThrottledRequests har ändrats till Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="04954-733">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="04954-734">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="04954-734">Az.DeploymentManager</span></span>
* <span data-ttu-id="04954-735">De första allmänt tillgängliga versionerna av cmdletar för Distributionshanteraren i Azure</span><span class="sxs-lookup"><span data-stu-id="04954-735">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="04954-736">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="04954-736">Az.Dns</span></span>
* <span data-ttu-id="04954-737">Automatisk delegering av DNS för NameServer</span><span class="sxs-lookup"><span data-stu-id="04954-737">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="04954-738">Det överordnade zonnamnet kan användas som ytterligare valfri parameter i cmdleten för att skapa DNS-zoner.</span><span class="sxs-lookup"><span data-stu-id="04954-738">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="04954-739">Lägger till NS-poster för en nyligen skapad underordnad zon i den överordnade zonen.</span><span class="sxs-lookup"><span data-stu-id="04954-739">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="04954-740">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="04954-740">Az.FrontDoor</span></span>
* <span data-ttu-id="04954-741">De första allmänt tillgängliga versionerna av cmdletar för Azure FrontDoor</span><span class="sxs-lookup"><span data-stu-id="04954-741">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="04954-742">Byt namn på WAF-cmdletar så att de omfattar ”Waf”</span><span class="sxs-lookup"><span data-stu-id="04954-742">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="04954-743">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="04954-743">Az.HDInsight</span></span>
* <span data-ttu-id="04954-744">Två cmdletar har tagits bort:</span><span class="sxs-lookup"><span data-stu-id="04954-744">Removed two cmdlets:</span></span>
    - <span data-ttu-id="04954-745">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="04954-745">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="04954-746">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="04954-746">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="04954-747">En ny cmdlet har lagts till, Set-AzHDInsightGatewayCredential, som ersätter Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="04954-747">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="04954-748">Uppdatera cmdleten Get-AzHDInsightJobOutput för att skilja mellan läsarrollen och HDInsight-operatörsrollen:</span><span class="sxs-lookup"><span data-stu-id="04954-748">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="04954-749">Användare med läsarrollen måste uttryckligen ange parametern ”DefaultStorageAccountKey”, annars uppstår fel.</span><span class="sxs-lookup"><span data-stu-id="04954-749">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="04954-750">Användare med HDInsight-operatörsrollen påverkas inte.</span><span class="sxs-lookup"><span data-stu-id="04954-750">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="04954-751">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="04954-751">Az.Monitor</span></span>
* <span data-ttu-id="04954-752">Nya cmdletar för SQR API (schemalagd frågeregel)</span><span class="sxs-lookup"><span data-stu-id="04954-752">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="04954-753">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="04954-753">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="04954-754">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="04954-754">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="04954-755">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="04954-755">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="04954-756">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="04954-756">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="04954-757">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="04954-757">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="04954-758">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="04954-758">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="04954-759">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="04954-759">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="04954-760">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="04954-760">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="04954-761">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="04954-761">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="04954-762">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="04954-762">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="04954-763">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="04954-763">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="04954-764">[Mer](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information om SQR API</span><span class="sxs-lookup"><span data-stu-id="04954-764">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="04954-765">Az.Monitor.md har uppdaterats för att omfatta cmdletar för måttbaserade aviseringsregler i GenV2 (inte klassiska)</span><span class="sxs-lookup"><span data-stu-id="04954-765">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="04954-766">Az.Network</span><span class="sxs-lookup"><span data-stu-id="04954-766">Az.Network</span></span>
* <span data-ttu-id="04954-767">Lägg till stöd för NAT Gateway-resurs</span><span class="sxs-lookup"><span data-stu-id="04954-767">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="04954-768">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="04954-768">New cmdlets</span></span>
        - <span data-ttu-id="04954-769">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="04954-769">New-AzNatGateway</span></span>
        - <span data-ttu-id="04954-770">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="04954-770">Get-AzNatGateway</span></span>
        - <span data-ttu-id="04954-771">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="04954-771">Set-AzNatGateway</span></span>
        - <span data-ttu-id="04954-772">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="04954-772">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="04954-773">Uppdaterade cmdletar</span><span class="sxs-lookup"><span data-stu-id="04954-773">Updated cmdlets</span></span>
        - <span data-ttu-id="04954-774">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="04954-774">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="04954-775">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="04954-775">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="04954-776">Nedanstående kommandon för funktionen har uppdaterats: Ange/ta bort anpassade vägar på Brooklyn Gateway.</span><span class="sxs-lookup"><span data-stu-id="04954-776">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="04954-777">New-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ställa in adressprefix som anpassade vägar för att ange gateway.</span><span class="sxs-lookup"><span data-stu-id="04954-777">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="04954-778">Set-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ange adressprefix som anpassade vägar för att ange gateway.</span><span class="sxs-lookup"><span data-stu-id="04954-778">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="04954-779">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="04954-779">Az.PolicyInsights</span></span>
* <span data-ttu-id="04954-780">Stöd för att fråga efter information om principutvärdering.</span><span class="sxs-lookup"><span data-stu-id="04954-780">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="04954-781">Lägg till parametern ”-Expand” för Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="04954-781">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="04954-782">Stöd för -Expand PolicyEvaluationDetails.</span><span class="sxs-lookup"><span data-stu-id="04954-782">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="04954-783">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="04954-783">Az.RecoveryServices</span></span>
* <span data-ttu-id="04954-784">Stöd för att dela prenumeration mellan Azure och Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="04954-784">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="04954-785">Markering av kommande icke-bakåtkompatibla ändringar för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="04954-785">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="04954-786">Korrigering för återställningsplan och åtgärdsplan i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="04954-786">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="04954-787">Korrigering för mappning av uppdateringsnätverk i Azure Site Recovery för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="04954-787">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="04954-788">Korrigering för instruktioner för uppdateringsskydd i Azure Site Recovery för Azure till Azure för hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="04954-788">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="04954-789">Andra mindre korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="04954-789">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="04954-790">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="04954-790">Az.Relay</span></span>
* <span data-ttu-id="04954-791">Korrigera stavfel i kundriktade meddelanden</span><span class="sxs-lookup"><span data-stu-id="04954-791">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="04954-792">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="04954-792">Az.ServiceBus</span></span>
* <span data-ttu-id="04954-793">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="04954-793">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="04954-794">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="04954-794">Az.Storage</span></span>
* <span data-ttu-id="04954-795">Uppgradera till lagringsklientbiblioteket 10.0.1 (namnområdet för alla objekt från detta SDK ändras från ”Microsoft.WindowsAzure.Storage. *till ”Microsoft.Azure.Storage.* ”)</span><span class="sxs-lookup"><span data-stu-id="04954-795">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="04954-796">Uppgradera till Microsoft.Azure.Management.Storage 11.0.0 för att stödja den nya API-versionen 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="04954-796">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="04954-797">Standardlagringskontot i Skapa lagringskonto ändras från ”Storage” till ”StorageV2”</span><span class="sxs-lookup"><span data-stu-id="04954-797">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="04954-798">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="04954-798">New-AzStorageAccount</span></span>
* <span data-ttu-id="04954-799">Ändra lagringskontots cmdlet-utdata Sku.Name för att passa med indata-SkuName genom att lägga till ”-”. Till exempel ändras ”StandardLRS” till ”Standard_LRS”</span><span class="sxs-lookup"><span data-stu-id="04954-799">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="04954-800">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="04954-800">New-AzStorageAccount</span></span>
    - <span data-ttu-id="04954-801">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="04954-801">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="04954-802">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="04954-802">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="04954-803">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="04954-803">Az.Websites</span></span>
* <span data-ttu-id="04954-804">Egenskapen ”typ” konfigureras nu för PSSite-objekt som returneras av Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="04954-804">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="04954-805">Get-AzWebApp\*Metrics och Get-AzAppServicePlanMetrics markeras som inaktuella</span><span class="sxs-lookup"><span data-stu-id="04954-805">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="04954-806">1.8.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="04954-806">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="04954-807">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="04954-807">Highlights since the last major release</span></span>
* <span data-ttu-id="04954-808">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="04954-808">General availability of `Az` module</span></span>
* <span data-ttu-id="04954-809">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="04954-809">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="04954-810">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="04954-810">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="04954-811">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="04954-811">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="04954-812">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="04954-812">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="04954-813">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="04954-813">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="04954-814">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="04954-814">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="04954-815">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="04954-815">Az.Accounts</span></span>
* <span data-ttu-id="04954-816">Uppdatera Uninstall-AzureRm för att ta bort moduler i Mac på ett korrekt sätt</span><span class="sxs-lookup"><span data-stu-id="04954-816">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="04954-817">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="04954-817">Az.Batch</span></span>
* <span data-ttu-id="04954-818">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="04954-818">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="04954-819">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="04954-819">Az.Cdn</span></span>
* <span data-ttu-id="04954-820">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="04954-820">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="04954-821">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="04954-821">Az.CognitiveServices</span></span>
* <span data-ttu-id="04954-822">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="04954-822">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="04954-823">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="04954-823">Az.Compute</span></span>
* <span data-ttu-id="04954-824">Åtgärda problem med AEM-installationen om resurs-ID:n för diskar innehåller resourcegroups i gemener i resurs-ID:n</span><span class="sxs-lookup"><span data-stu-id="04954-824">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="04954-825">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="04954-825">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="04954-826">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="04954-826">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="04954-827">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="04954-827">Az.DataFactory</span></span>
* <span data-ttu-id="04954-828">Lägg till SsisProperties om NodeCount inte är null för hanterad integreringskörning.</span><span class="sxs-lookup"><span data-stu-id="04954-828">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="04954-829">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="04954-829">Az.DataLakeStore</span></span>
* <span data-ttu-id="04954-830">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="04954-830">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="04954-831">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="04954-831">Az.EventGrid</span></span>
* <span data-ttu-id="04954-832">Hjälptexten för slutpunkten har uppdaterats för att visa att resurser ska skapas innan cmdletarna för att skapa/uppdatera händelseprenumerationer används.</span><span class="sxs-lookup"><span data-stu-id="04954-832">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="04954-833">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="04954-833">Az.EventHub</span></span>
* <span data-ttu-id="04954-834">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="04954-834">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="04954-835">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="04954-835">Az.HDInsight</span></span>
* <span data-ttu-id="04954-836">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="04954-836">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="04954-837">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="04954-837">Az.IotHub</span></span>
* <span data-ttu-id="04954-838">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="04954-838">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="04954-839">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="04954-839">Az.KeyVault</span></span>
* <span data-ttu-id="04954-840">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="04954-840">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="04954-841">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="04954-841">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="04954-842">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="04954-842">Az.MachineLearning</span></span>
* <span data-ttu-id="04954-843">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="04954-843">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="04954-844">Az.Media</span><span class="sxs-lookup"><span data-stu-id="04954-844">Az.Media</span></span>
* <span data-ttu-id="04954-845">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="04954-845">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="04954-846">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="04954-846">Az.Monitor</span></span>
  * <span data-ttu-id="04954-847">Nya cmdletar för måttbaserad aviseringsregel i GenV2 (inte klassisk)</span><span class="sxs-lookup"><span data-stu-id="04954-847">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="04954-848">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="04954-848">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="04954-849">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="04954-849">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="04954-850">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="04954-850">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="04954-851">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="04954-851">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="04954-852">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="04954-852">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="04954-853">Monitor SDK har uppdaterats till version 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="04954-853">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="04954-854">Az.Network</span><span class="sxs-lookup"><span data-stu-id="04954-854">Az.Network</span></span>
* <span data-ttu-id="04954-855">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="04954-855">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="04954-856">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="04954-856">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="04954-857">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="04954-857">Az.NotificationHubs</span></span>
* <span data-ttu-id="04954-858">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="04954-858">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="04954-859">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="04954-859">Az.OperationalInsights</span></span>
* <span data-ttu-id="04954-860">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="04954-860">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="04954-861">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="04954-861">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="04954-862">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="04954-862">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="04954-863">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="04954-863">Az.RecoveryServices</span></span>
* <span data-ttu-id="04954-864">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="04954-864">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="04954-865">Tabellformatet för SQL i virtuella Azure-datorer har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="04954-865">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="04954-866">En alternativ metod för att hämta platser i AzureFileShare har lagts till</span><span class="sxs-lookup"><span data-stu-id="04954-866">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="04954-867">ScheduleRunDays i SchedulePolicy-objekt har uppdaterats enligt tidszon</span><span class="sxs-lookup"><span data-stu-id="04954-867">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="04954-868">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="04954-868">Az.RedisCache</span></span>
* <span data-ttu-id="04954-869">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="04954-869">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="04954-870">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="04954-870">Az.Resources</span></span>
* <span data-ttu-id="04954-871">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="04954-871">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="04954-872">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="04954-872">Az.Sql</span></span>
* <span data-ttu-id="04954-873">Ersätt Monitor SDK-beroende med vanlig kod</span><span class="sxs-lookup"><span data-stu-id="04954-873">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="04954-874">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="04954-874">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="04954-875">Förbättrad process för klassificering av flera kolumner.</span><span class="sxs-lookup"><span data-stu-id="04954-875">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="04954-876">Inkludera SKU-egenskaper (SKU-namn, serie, kapacitet) i svaret från Get-AzSqlServerServiceObjective och formatera som tabell som standard.</span><span class="sxs-lookup"><span data-stu-id="04954-876">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="04954-877">Möjlighet att använda Get-AzSqlServerServiceObjective efter plats utan att behöva en redan befintlig server i regionen.</span><span class="sxs-lookup"><span data-stu-id="04954-877">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="04954-878">Stöd för tidszonsparametern när hanterade instanser skapas.</span><span class="sxs-lookup"><span data-stu-id="04954-878">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="04954-879">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="04954-879">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="04954-880">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="04954-880">Az.Websites</span></span>
* <span data-ttu-id="04954-881">åtgärdar Set-AzWebApp och Set-AzWebAppSlot så att de inte tar bort taggar vid körning</span><span class="sxs-lookup"><span data-stu-id="04954-881">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="04954-882">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="04954-882">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="04954-883">SDK för WebSites har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="04954-883">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="04954-884">Egenskapen AdminSiteName har tagits bort från PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="04954-884">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="04954-885">1.7.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="04954-885">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="04954-886">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="04954-886">Highlights since the last major release</span></span>
* <span data-ttu-id="04954-887">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="04954-887">General availability of `Az` module</span></span>
* <span data-ttu-id="04954-888">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="04954-888">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="04954-889">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="04954-889">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="04954-890">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="04954-890">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="04954-891">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="04954-891">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="04954-892">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="04954-892">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="04954-893">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="04954-893">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="04954-894">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="04954-894">Az.Accounts</span></span>
* <span data-ttu-id="04954-895">Add-AzEnvironment och Set-AzEnvironment har uppdaterats för att godkänna parametern AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="04954-895">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="04954-896">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="04954-896">Az.AnalysisServices</span></span>
* <span data-ttu-id="04954-897">ServiceClient används i cmdletar för dataplan och den ursprungliga autentiseringslogiken har tagits bort</span><span class="sxs-lookup"><span data-stu-id="04954-897">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="04954-898">Add-AzureASAccount används för omslutning av Connect-AzAccount för att undvika en icke-bakåtkompatibel ändring</span><span class="sxs-lookup"><span data-stu-id="04954-898">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="04954-899">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="04954-899">Az.Automation</span></span>
* <span data-ttu-id="04954-900">Buggen för cmdleten New-AzAutomationSoftwareUpdateConfiguration för inkluderingar har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="04954-900">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="04954-901">Nu bör parametern IncludedKbNumber och IncludedPackageNameMask fungera.</span><span class="sxs-lookup"><span data-stu-id="04954-901">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="04954-902">Felkorrigering för dynamiska grupper i uppdateringshanteringen för azure automation</span><span class="sxs-lookup"><span data-stu-id="04954-902">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="04954-903">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="04954-903">Az.Compute</span></span>
* <span data-ttu-id="04954-904">Lägg till parametern HyperVGeneration i New-AzDiskConfig och New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="04954-904">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="04954-905">Tillåt att virtuella datorer skapas med galleribilder från andra klientorganisationer.</span><span class="sxs-lookup"><span data-stu-id="04954-905">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="04954-906">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="04954-906">Az.ContainerInstance</span></span>
* <span data-ttu-id="04954-907">Ett problem har åtgärdats i parametern -Command för New-AzContainerGroup som lade till ett avslutande tomt argument</span><span class="sxs-lookup"><span data-stu-id="04954-907">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="04954-908">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="04954-908">Az.DataFactory</span></span>
* <span data-ttu-id="04954-909">ADF .Net SDK-versionen har uppdaterats till 3.0.2</span><span class="sxs-lookup"><span data-stu-id="04954-909">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="04954-910">Cmdleten Set-AzDataFactoryV2 har uppdaterats med extra parametrar för inställningar som rör RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="04954-910">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="04954-911">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="04954-911">Az.Resources</span></span>
* <span data-ttu-id="04954-912">Förbättra hanteringen av providrar för Get-AzResource när parametrarna -ResourceId eller -ResourceGroupName, -Name och -ResourceType tillhandahålls</span><span class="sxs-lookup"><span data-stu-id="04954-912">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="04954-913">Förbättra felhanteringen för ”Test-AzDeployment” och ”Test-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="04954-913">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="04954-914">Hantera fel utanför distributionsvalideringen och ta med dem i kommandoutdata istället</span><span class="sxs-lookup"><span data-stu-id="04954-914">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="04954-915">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="04954-915">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="04954-916">Lägg till växlingsparametern -IgnoreDynamicParameters till en uppsättning av cmdletar för distribution för att hoppa över fråga i skript och jobbscenarier</span><span class="sxs-lookup"><span data-stu-id="04954-916">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="04954-917">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="04954-917">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="04954-918">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="04954-918">Az.Sql</span></span>
* <span data-ttu-id="04954-919">Stöd för dataklassificering av databaser.</span><span class="sxs-lookup"><span data-stu-id="04954-919">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="04954-920">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="04954-920">Az.Storage</span></span>
* <span data-ttu-id="04954-921">Rapportera detaljfel när lagringskontext skapas med parametern -UseConnectedAccount, men utan inloggning på Azure-kontot</span><span class="sxs-lookup"><span data-stu-id="04954-921">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="04954-922">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="04954-922">New-AzStorageContext</span></span>
* <span data-ttu-id="04954-923">Stöd för att hantera Blob Service-egenskaper för ett angivet lagringskonto med API:et för hanteringsplan</span><span class="sxs-lookup"><span data-stu-id="04954-923">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="04954-924">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="04954-924">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="04954-925">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="04954-925">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="04954-926">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="04954-926">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="04954-927">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="04954-927">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="04954-928">Stöd för -AsJob-cmdletar för att ladda upp och ladda ned blobar och filer</span><span class="sxs-lookup"><span data-stu-id="04954-928">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="04954-929">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="04954-929">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="04954-930">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="04954-930">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="04954-931">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="04954-931">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="04954-932">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="04954-932">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="04954-933">1.6.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="04954-933">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="04954-934">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="04954-934">Highlights since the last major release</span></span>
* <span data-ttu-id="04954-935">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="04954-935">General availability of `Az` module</span></span>
* <span data-ttu-id="04954-936">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="04954-936">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="04954-937">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="04954-937">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="04954-938">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="04954-938">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="04954-939">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="04954-939">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="04954-940">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="04954-940">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="04954-941">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="04954-941">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="04954-942">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="04954-942">Az.Automation</span></span>
* <span data-ttu-id="04954-943">Azure Automation – ändring av uppdateringshantering för stöd för de nya funktionerna:</span><span class="sxs-lookup"><span data-stu-id="04954-943">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="04954-944">Dynamisk gruppering</span><span class="sxs-lookup"><span data-stu-id="04954-944">Dynamic grouping</span></span>
    * <span data-ttu-id="04954-945">För-/efterskrift</span><span class="sxs-lookup"><span data-stu-id="04954-945">Pre-Post script</span></span>
    * <span data-ttu-id="04954-946">Inställning för omstart</span><span class="sxs-lookup"><span data-stu-id="04954-946">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="04954-947">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="04954-947">Az.Compute</span></span>
* <span data-ttu-id="04954-948">Åtgärda problem med sökvägsmatchning i Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="04954-948">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="04954-949">Uppdatera Compute-klientbibliotek till 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="04954-949">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="04954-950">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="04954-950">Az.KeyVault</span></span>
* <span data-ttu-id="04954-951">Stöd för jokertecken för KeyVault-cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="04954-951">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="04954-952">Az.Network</span><span class="sxs-lookup"><span data-stu-id="04954-952">Az.Network</span></span>
* <span data-ttu-id="04954-953">Lägg till stöd för Threat Intelligence för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="04954-953">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="04954-954">Lägg till resurs för brandväggsprincip på översta nivå och anpassade regler för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="04954-954">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="04954-955">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="04954-955">Az.RecoveryServices</span></span>
* <span data-ttu-id="04954-956">SnapshotRetentionInDays har lagts till i Azure-principen för virtuella datorer för stöd av Instant RP</span><span class="sxs-lookup"><span data-stu-id="04954-956">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="04954-957">Pipe-stöd för avregistrering av container har lagts till</span><span class="sxs-lookup"><span data-stu-id="04954-957">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="04954-958">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="04954-958">Az.Resources</span></span>
* <span data-ttu-id="04954-959">Uppdatera stöd för jokertecken för Get-AzResource och Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="04954-959">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="04954-960">Uppdatera autentiseringsuppgifter som används vid allmänna anrop till ARM</span><span class="sxs-lookup"><span data-stu-id="04954-960">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="04954-961">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="04954-961">Az.Sql</span></span>
* <span data-ttu-id="04954-962">Cmdlet-parametern (ExcludeDetectionType) för Hotidentifiering ändrades från DetectionType till sträng[] för att framtidssäkra den när nya DetectionTypes läggs till, och även för att stödja automatisk ifyllning.</span><span class="sxs-lookup"><span data-stu-id="04954-962">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="04954-963">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="04954-963">Az.Storage</span></span>
* <span data-ttu-id="04954-964">Stöd för att hämta/ange/ta bort hanteringsprincip på ett lagringskonto</span><span class="sxs-lookup"><span data-stu-id="04954-964">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="04954-965">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="04954-965">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="04954-966">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="04954-966">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="04954-967">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="04954-967">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="04954-968">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="04954-968">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="04954-969">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="04954-969">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="04954-970">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="04954-970">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="04954-971">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="04954-971">Az.Websites</span></span>
* <span data-ttu-id="04954-972">Åtgärda fel med ARM-mall som avbryter kloning av alla platser med 'New-AzWebApp -IncludeSourceWebAppSlots'</span><span class="sxs-lookup"><span data-stu-id="04954-972">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="04954-973">1.5.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="04954-973">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="04954-974">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="04954-974">Az.Accounts</span></span>
* <span data-ttu-id="04954-975">Lägg till kommandot Register-AzModule för stöd för AutoRest-genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="04954-975">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="04954-976">Uppdatera exempel för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="04954-976">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="04954-977">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="04954-977">Az.Automation</span></span>
* <span data-ttu-id="04954-978">Problem med att hämta vissa månadsscheman i flera Azure Automation-cmdletar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="04954-978">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="04954-979">Åtgärda problem med att Get-AzAutomationDscNode bara returnerar de 20 översta noderna.</span><span class="sxs-lookup"><span data-stu-id="04954-979">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="04954-980">Nu returneras alla noder</span><span class="sxs-lookup"><span data-stu-id="04954-980">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="04954-981">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="04954-981">Az.Cdn</span></span>
* <span data-ttu-id="04954-982">Nya Powershell-cmdletar för att aktivera/inaktivera anpassade domän-HTTPS har lagts till och de gamla har gjorts inaktuella</span><span class="sxs-lookup"><span data-stu-id="04954-982">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="04954-983">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="04954-983">Az.Compute</span></span>
* <span data-ttu-id="04954-984">Lägg till stöd för jokertecken för Get-cmdletar</span><span class="sxs-lookup"><span data-stu-id="04954-984">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="04954-985">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="04954-985">Az.DataFactory</span></span>
* <span data-ttu-id="04954-986">ADF .Net SDK-versionen har uppdaterats till 3.0.1</span><span class="sxs-lookup"><span data-stu-id="04954-986">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="04954-987">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="04954-987">Az.LogicApp</span></span>
* <span data-ttu-id="04954-988">Åtgärda problemet med att ListWorkflows endast hämtar den första sidan med resultat</span><span class="sxs-lookup"><span data-stu-id="04954-988">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="04954-989">Az.Network</span><span class="sxs-lookup"><span data-stu-id="04954-989">Az.Network</span></span>
* <span data-ttu-id="04954-990">Lägg till stöd för jokertecken för Network-cmdletar</span><span class="sxs-lookup"><span data-stu-id="04954-990">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="04954-991">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="04954-991">Az.RecoveryServices</span></span>
* <span data-ttu-id="04954-992">Stöd har lagts till för SQL Server i virtuella Azure-datorer</span><span class="sxs-lookup"><span data-stu-id="04954-992">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="04954-993">SDK-uppdatering</span><span class="sxs-lookup"><span data-stu-id="04954-993">SDK Update</span></span>
* <span data-ttu-id="04954-994">Get-ProtectableItem-incheckning i VMappContainer har tagits bort</span><span class="sxs-lookup"><span data-stu-id="04954-994">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="04954-995">Name och ServerName har lagts till som parametrar för Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="04954-995">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="04954-996">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="04954-996">Az.Resources</span></span>
* <span data-ttu-id="04954-997">Lägg till parametern `-TemplateObject` i cmdletar för distribution</span><span class="sxs-lookup"><span data-stu-id="04954-997">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="04954-998">Mer information här: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="04954-998">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="04954-999">Åtgärda problem med piping av resultatet i `Get-AzResource` till `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="04954-999">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="04954-1000">Mer information här: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="04954-1000">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="04954-1001">Åtgärda problem med ändring av JSON-datatyp när `Set-AzResource` körs</span><span class="sxs-lookup"><span data-stu-id="04954-1001">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="04954-1002">Mer information här: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="04954-1002">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="04954-1003">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="04954-1003">Az.Sql</span></span>
* <span data-ttu-id="04954-1004">AuditingEndpointsCommunicator uppdateras.</span><span class="sxs-lookup"><span data-stu-id="04954-1004">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="04954-1005">Åtgärdar beteendet hos ett gränsscenario när nya diagnostikinställningar skapas.</span><span class="sxs-lookup"><span data-stu-id="04954-1005">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="04954-1006">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="04954-1006">Az.Storage</span></span>
* <span data-ttu-id="04954-1007">Stöd för BlockBlobStorage när Storage-konto skapas      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="04954-1007">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="04954-1008">1.4.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="04954-1008">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="04954-1009">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="04954-1009">Az.AnalysisServices</span></span>
* <span data-ttu-id="04954-1010">Inaktuell AddAzureASAccount-cmdlet</span><span class="sxs-lookup"><span data-stu-id="04954-1010">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="04954-1011">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="04954-1011">Az.Automation</span></span>
* <span data-ttu-id="04954-1012">Hjälpen för Import-AzAutomationDscNodeConfiguration har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="04954-1012">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="04954-1013">Konfigurationsnamnsvalidering har lagts till i cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="04954-1013">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="04954-1014">Förbättrad felhantering för cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="04954-1014">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="04954-1015">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="04954-1015">Az.CognitiveServices</span></span>
* <span data-ttu-id="04954-1016">CustomSubdomainName har lagts till som en ny valfri parameter för New-AzCognitiveServicesAccount, som används för att ange underdomän för resursen.</span><span class="sxs-lookup"><span data-stu-id="04954-1016">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="04954-1017">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="04954-1017">Az.Compute</span></span>
* <span data-ttu-id="04954-1018">Problemet med ID-parameteruppsättningar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="04954-1018">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="04954-1019">Get-AzVMExtension har uppdaterats så att alla installerade tillägg visas om parametern Name inte har angetts</span><span class="sxs-lookup"><span data-stu-id="04954-1019">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="04954-1020">Parametrarna Tag och ResourceId har lagts till i cmdleten Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="04954-1020">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="04954-1021">Get-AzVmssVM utan instans-ID och med InstanceView kan visa virtuella VMSS-datorer med instansvyn.</span><span class="sxs-lookup"><span data-stu-id="04954-1021">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="04954-1022">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="04954-1022">Az.DataLakeStore</span></span>
* <span data-ttu-id="04954-1023">Cmdletar har lagts till för uppräkning och återställning av borttagna objekt i ADL</span><span class="sxs-lookup"><span data-stu-id="04954-1023">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="04954-1024">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="04954-1024">Az.EventHub</span></span>
* <span data-ttu-id="04954-1025">Ny boolesk egenskap SkipEmptyArchives har lagts till i Skip Empty Archives i CaptureDescription-klassen i Eventhub</span><span class="sxs-lookup"><span data-stu-id="04954-1025">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="04954-1026">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="04954-1026">Az.KeyVault</span></span>
* <span data-ttu-id="04954-1027">Taggning i Set-AzKeyVaultSecret har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="04954-1027">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="04954-1028">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="04954-1028">Az.LogicApp</span></span>
* <span data-ttu-id="04954-1029">Grundläggande SKU har lagts till för Integrationskonton</span><span class="sxs-lookup"><span data-stu-id="04954-1029">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="04954-1030">XSLT 2.0, XSLT 3.0 och Flytande mappningstyper har lagts till</span><span class="sxs-lookup"><span data-stu-id="04954-1030">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="04954-1031">Nya cmdletar för integrationskontosammansättningar</span><span class="sxs-lookup"><span data-stu-id="04954-1031">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="04954-1032">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="04954-1032">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="04954-1033">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="04954-1033">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="04954-1034">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="04954-1034">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="04954-1035">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="04954-1035">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="04954-1036">Nya cmdletar för batchkonfiguration för integrationskonto</span><span class="sxs-lookup"><span data-stu-id="04954-1036">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="04954-1037">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="04954-1037">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="04954-1038">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="04954-1038">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="04954-1039">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="04954-1039">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="04954-1040">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="04954-1040">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="04954-1041">Logic App-SDK har uppdaterats till version 4.1.0</span><span class="sxs-lookup"><span data-stu-id="04954-1041">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="04954-1042">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="04954-1042">Az.Monitor</span></span>
* <span data-ttu-id="04954-1043">Hjälpen för Get-AzMetric har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="04954-1043">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="04954-1044">Az.Network</span><span class="sxs-lookup"><span data-stu-id="04954-1044">Az.Network</span></span>
* <span data-ttu-id="04954-1045">Hjälpexempel för Add-AzApplicationGatewayCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="04954-1045">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="04954-1046">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="04954-1046">Az.OperationalInsights</span></span>
* <span data-ttu-id="04954-1047">Ytterligare stöd för datakällorna New och Get ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="04954-1047">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="04954-1048">Ny ApplicationInsights-typ har lagts till för att ge stöd för ”Get specific” och ”Get all” för ApplicationInsights-datakällor för angiven arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="04954-1048">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="04954-1049">Cmdleten New-AzOperationalInsightsApplicationInsightsDataSource har lagts till för att skapa datakälla med angivna parametrar för Application Insights-resurs: subscription Id, resourceGroupName och name.</span><span class="sxs-lookup"><span data-stu-id="04954-1049">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="04954-1050">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="04954-1050">Az.Resources</span></span>
* <span data-ttu-id="04954-1051">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="04954-1051">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="04954-1052">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="04954-1052">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="04954-1053">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="04954-1053">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="04954-1054">Fel som gör att KeyCredentials inte kan skapas upprepade gånger har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="04954-1054">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="04954-1055">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="04954-1055">Az.Sql</span></span>
* <span data-ttu-id="04954-1056">Lägg till stöd för hyperskalanivån för SQL DB</span><span class="sxs-lookup"><span data-stu-id="04954-1056">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="04954-1057">Ett fel har åtgärdats där återställningen kunde misslyckas på grund av onödiga inställningsegenskaper i restore-förfrågan</span><span class="sxs-lookup"><span data-stu-id="04954-1057">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="04954-1058">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="04954-1058">Az.Websites</span></span>
* <span data-ttu-id="04954-1059">Rätt exempel i Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="04954-1059">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="04954-1060">1.3.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="04954-1060">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="04954-1061">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="04954-1061">Az.Accounts</span></span>
* <span data-ttu-id="04954-1062">Uppdatera till den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="04954-1062">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="04954-1063">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="04954-1063">Az.AnalysisServices</span></span>
<span data-ttu-id="04954-1064">Allmän tillgänglighet för Az.AnalysisServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="04954-1064">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="04954-1065">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="04954-1065">Az.Compute</span></span>
* <span data-ttu-id="04954-1066">AEM-tillägg: Lägg till stöd för UltraSSD-, P60-, P70- och P80-diskar</span><span class="sxs-lookup"><span data-stu-id="04954-1066">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="04954-1067">Uppdatera hjälpbeskrivning för Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="04954-1067">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="04954-1068">Uppdatera hjälpbeskrivning och exempel för Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="04954-1068">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="04954-1069">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="04954-1069">Az.RecoveryServices</span></span>
<span data-ttu-id="04954-1070">Allmän tillgänglighet för Az.RecoveryServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="04954-1070">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="04954-1071">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="04954-1071">Az.Resources</span></span>
* <span data-ttu-id="04954-1072">Korrigera taggar för resursgrupper</span><span class="sxs-lookup"><span data-stu-id="04954-1072">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="04954-1073">Mer information här: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="04954-1073">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="04954-1074">Åtgärda problem där `Get-AzureRmRoleAssignment` inte respekterar -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="04954-1074">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="04954-1075">Mer information här: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="04954-1075">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="04954-1076">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="04954-1076">Az.Sql</span></span>
* <span data-ttu-id="04954-1077">Lägga till Get/Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="04954-1077">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="04954-1078">Åtgärda problem där ett nullref-undantag uppstår när du kör SQL-cmdletar och inte är inloggad på ett Azure-konto</span><span class="sxs-lookup"><span data-stu-id="04954-1078">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="04954-1079">Åtgärda nullref-undantag i Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="04954-1079">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="04954-1080">1.2.1 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="04954-1080">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="04954-1081">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="04954-1081">Az.Accounts</span></span>
* <span data-ttu-id="04954-1082">Version med rätt version av autentisering</span><span class="sxs-lookup"><span data-stu-id="04954-1082">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="04954-1083">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="04954-1083">Az.AnalysisServices</span></span>
* <span data-ttu-id="04954-1084">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="04954-1084">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="04954-1085">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="04954-1085">Az.RecoveryServices</span></span>
* <span data-ttu-id="04954-1086">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="04954-1086">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="04954-1087">1.2.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="04954-1087">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="04954-1088">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="04954-1088">Az.Accounts</span></span>
* <span data-ttu-id="04954-1089">Lägga till interaktiv autentisering och autentisering med användarnamn/lösenord för endast Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="04954-1089">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="04954-1090">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="04954-1090">Update incorrect online help URLs</span></span>
* <span data-ttu-id="04954-1091">Lägga till varningsmeddelande i PS Core för Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="04954-1091">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="04954-1092">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="04954-1092">Az.Aks</span></span>
* <span data-ttu-id="04954-1093">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="04954-1093">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="04954-1094">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="04954-1094">Az.Automation</span></span>
* <span data-ttu-id="04954-1095">Stöd för Python 2-runbookflöden har lagts till</span><span class="sxs-lookup"><span data-stu-id="04954-1095">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="04954-1096">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="04954-1096">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="04954-1097">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="04954-1097">Az.Cdn</span></span>
* <span data-ttu-id="04954-1098">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="04954-1098">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="04954-1099">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="04954-1099">Az.Compute</span></span>
* <span data-ttu-id="04954-1100">Lägga till cmdleten Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="04954-1100">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="04954-1101">Lägga till TempDisk-parameter i Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="04954-1101">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="04954-1102">Korrigera varningsmeddelande för New-AzVM</span><span class="sxs-lookup"><span data-stu-id="04954-1102">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="04954-1103">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="04954-1103">Az.ContainerRegistry</span></span>
* <span data-ttu-id="04954-1104">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="04954-1104">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="04954-1105">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="04954-1105">Az.DataFactory</span></span>
* <span data-ttu-id="04954-1106">ADF .Net SDK-versionen har uppdaterats till 3.0.0</span><span class="sxs-lookup"><span data-stu-id="04954-1106">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="04954-1107">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="04954-1107">Az.DataLakeStore</span></span>
* <span data-ttu-id="04954-1108">Åtgärda problem med ADLS-slutpunkt vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="04954-1108">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="04954-1109">Mer information här: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="04954-1109">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="04954-1110">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="04954-1110">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="04954-1111">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="04954-1111">Az.IotHub</span></span>
* <span data-ttu-id="04954-1112">Lägga till kodningsformat i cmdleten Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="04954-1112">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="04954-1113">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="04954-1113">Az.KeyVault</span></span>
* <span data-ttu-id="04954-1114">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="04954-1114">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="04954-1115">Az.Network</span><span class="sxs-lookup"><span data-stu-id="04954-1115">Az.Network</span></span>
* <span data-ttu-id="04954-1116">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="04954-1116">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="04954-1117">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="04954-1117">Az.Resources</span></span>
* <span data-ttu-id="04954-1118">Åtgärda felaktiga exempel i referensdokumentationen ”New-AzADAppCredential” och ”New-AzADSpCredential”</span><span class="sxs-lookup"><span data-stu-id="04954-1118">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="04954-1119">Åtgärda problem där sökvägen för parametern ”-TemplateFile” inte omvandlas innan cmdletarna för distribution i resursgruppen körs</span><span class="sxs-lookup"><span data-stu-id="04954-1119">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="04954-1120">Az.Resources: Korrigera dokumentationen om standardvärdet för New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="04954-1120">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="04954-1121">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="04954-1121">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="04954-1122">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="04954-1122">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="04954-1123">Åtgärda formateringsproblemet med objektet ”PSResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="04954-1123">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="04954-1124">Mer information här: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="04954-1124">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="04954-1125">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="04954-1125">Az.ServiceFabric</span></span>
* <span data-ttu-id="04954-1126">Återställ när ett certifikat läggs till i en Virtual Machine Scale Sets-modell men ett undantag genereras. Detta har gjorts för att åtgärda följande fel: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="04954-1126">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="04954-1127">Korrigera några felmeddelanden.</span><span class="sxs-lookup"><span data-stu-id="04954-1127">Fix some error messages.</span></span>
* <span data-ttu-id="04954-1128">Korrigering av skapande av kluster med ARM-mall som är standard för New-AzServiceFabriCluster som inte fungerade med migrering till Az.</span><span class="sxs-lookup"><span data-stu-id="04954-1128">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="04954-1129">Korrigering av tilläggning av kluster/programcertifikat så att endast VM Scale Sets som motsvarar klustret läggs till genom att kontrollera ID för klustret i tillägget.</span><span class="sxs-lookup"><span data-stu-id="04954-1129">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="04954-1130">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="04954-1130">Az.SignalR</span></span>
* <span data-ttu-id="04954-1131">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="04954-1131">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="04954-1132">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="04954-1132">Az.Sql</span></span>
* <span data-ttu-id="04954-1133">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="04954-1133">Update incorrect online help URLs</span></span>
* <span data-ttu-id="04954-1134">Uppdaterad parameterbeskrivning för LicenseType-parameter med möjliga värden</span><span class="sxs-lookup"><span data-stu-id="04954-1134">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="04954-1135">Korrigering för att uppdatera hanterad instansidentitet som inte fungerar när det är den enda uppdaterade egenskapen</span><span class="sxs-lookup"><span data-stu-id="04954-1135">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="04954-1136">Stöd för anpassad sortering på hanterad instans</span><span class="sxs-lookup"><span data-stu-id="04954-1136">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="04954-1137">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="04954-1137">Az.Storage</span></span>
* <span data-ttu-id="04954-1138">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="04954-1138">Update incorrect online help URLs</span></span>
* <span data-ttu-id="04954-1139">Tillhandahåll detaljerat felmeddelande när en användare försöker hämta/konfigurera klassisk loggning/mått på ett Premium Storage-konto eftersom Premium Storage-kontot inte har stöd för klassisk loggning/mått.</span><span class="sxs-lookup"><span data-stu-id="04954-1139">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="04954-1140">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="04954-1140">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="04954-1141">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="04954-1141">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="04954-1142">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="04954-1142">Az.TrafficManager</span></span>
* <span data-ttu-id="04954-1143">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="04954-1143">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="04954-1144">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="04954-1144">Az.Websites</span></span>
* <span data-ttu-id="04954-1145">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="04954-1145">Update incorrect online help URLs</span></span>
* <span data-ttu-id="04954-1146">Korrigerar ”New-AzWebAppSSLBinding” så att certifikatet laddas upp till rätt resursgrupp och plats om appen finns i en ASE.</span><span class="sxs-lookup"><span data-stu-id="04954-1146">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="04954-1147">Korrigerar ”New-AzWebAppSSLBinding” så att taggarna inte skrivs över på en bindning av ett SSL-certifikat till en app</span><span class="sxs-lookup"><span data-stu-id="04954-1147">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="04954-1148">1.1.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="04954-1148">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="04954-1149">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="04954-1149">Az.Accounts</span></span>
* <span data-ttu-id="04954-1150">Lade till omfattningen ”Lokal” till Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="04954-1150">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="04954-1151">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="04954-1151">Az.Compute</span></span>
* <span data-ttu-id="04954-1152">Namn är nu valfritt i ID-parametern för Restart/Start/Stop/Remove/Set-AzVM och Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="04954-1152">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="04954-1153">Uppdaterade beskrivningen av ID i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="04954-1153">Updated the description of ID in help files</span></span>
* <span data-ttu-id="04954-1154">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="04954-1154">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="04954-1155">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="04954-1155">Az.DataLakeStore</span></span>
* <span data-ttu-id="04954-1156">Uppdatera sdk-versionen av dataplanet till 1.1.14 för SDK-korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="04954-1156">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="04954-1157">Korrigerade hanteringen av negativ accesstime och modificationtime för getfilestatus och liststatus; korrigera asynkront annulleringstoken</span><span class="sxs-lookup"><span data-stu-id="04954-1157">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="04954-1158">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="04954-1158">Az.EventGrid</span></span>
* <span data-ttu-id="04954-1159">Uppdaterat för användning av API-versionen 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="04954-1159">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="04954-1160">Uppdaterade följande cmdletar för att stödja nytt scenario i API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="04954-1160">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="04954-1161">New-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="04954-1161">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="04954-1162">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="04954-1162">Event Time-To-Live,</span></span>
        - <span data-ttu-id="04954-1163">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="04954-1163">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="04954-1164">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="04954-1164">Dead letter endpoint.</span></span>
    - <span data-ttu-id="04954-1165">Update-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="04954-1165">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="04954-1166">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="04954-1166">Event Time-To-Live,</span></span>
        - <span data-ttu-id="04954-1167">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="04954-1167">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="04954-1168">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="04954-1168">Dead letter endpoint.</span></span>
* <span data-ttu-id="04954-1169">Lade till nya enum-värden (storageQueue och hybridConnection) för alternativet EndpointType i cmdletarna New-AzureRmEventGridSubscription och Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="04954-1169">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="04954-1170">Visa varningsmeddelanden om skapande eller uppdatering av händelseprenumerationen förväntas medföra manuell åtgärd från användaren.</span><span class="sxs-lookup"><span data-stu-id="04954-1170">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="04954-1171">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="04954-1171">Az.IotHub</span></span>
* <span data-ttu-id="04954-1172">Har uppdaterats till den senaste versionen av SDK:n lotHub</span><span class="sxs-lookup"><span data-stu-id="04954-1172">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="04954-1173">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="04954-1173">Az.LogicApp</span></span>
* <span data-ttu-id="04954-1174">Get-AzLogicApp visar en lista över alla som inte har angivet namn</span><span class="sxs-lookup"><span data-stu-id="04954-1174">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="04954-1175">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="04954-1175">Az.Resources</span></span>
* <span data-ttu-id="04954-1176">Åtgärdade problem med parameteruppsättningen när parametrarna -ODataQuery och -ResourceId anges för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="04954-1176">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="04954-1177">Mer information här: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="04954-1177">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="04954-1178">Åtgärdade hantering av parametern -Custom i New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="04954-1178">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="04954-1179">Korrigerade stavfel i New-AzDeployment-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="04954-1179">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="04954-1180">Gjorde parametern -MailNickname obligatorisk för New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="04954-1180">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="04954-1181">Mer information här: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="04954-1181">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="04954-1182">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="04954-1182">Az.SignalR</span></span>
* <span data-ttu-id="04954-1183">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="04954-1183">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="04954-1184">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="04954-1184">Az.Sql</span></span>
* <span data-ttu-id="04954-1185">Konverterade lagringshanteringsklientens beroende av den normala SDK-implementeringen.</span><span class="sxs-lookup"><span data-stu-id="04954-1185">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="04954-1186">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="04954-1186">Az.Storage</span></span>
* <span data-ttu-id="04954-1187">Angav StorageAccountName för lagringskontext som det verkliga namnet på lagringskontot när det skapas med Sas Token, OAuth eller Anonymous</span><span class="sxs-lookup"><span data-stu-id="04954-1187">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="04954-1188">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="04954-1188">New-AzStorageContext</span></span>
* <span data-ttu-id="04954-1189">Skapade Sas Token för Blob Snapshot-objekt med parametern -FullUri, åtgärdade den returnerade URI:n så att den blir URI för ögonblicksbild</span><span class="sxs-lookup"><span data-stu-id="04954-1189">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="04954-1190">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="04954-1190">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="04954-1191">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="04954-1191">Az.Websites</span></span>
* <span data-ttu-id="04954-1192">Åtgärdade en bugg i datumparsningen i Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="04954-1192">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="04954-1193">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="04954-1193">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="04954-1194">1.0.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="04954-1194">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="04954-1195">Allmänt</span><span class="sxs-lookup"><span data-stu-id="04954-1195">General</span></span>

- <span data-ttu-id="04954-1196">Allmän tillgänglighet för Az-modulen</span><span class="sxs-lookup"><span data-stu-id="04954-1196">General Availability of Az Module</span></span>
- <span data-ttu-id="04954-1197">Onlinehjälp för varje modul</span><span class="sxs-lookup"><span data-stu-id="04954-1197">Online help for each module</span></span>
- <span data-ttu-id="04954-1198">Mer information och en översikt finns på [Az-informationssidan](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="04954-1198">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="04954-1199">Information om hur du migrerar från AzureRM finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="04954-1199">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="04954-1200">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="04954-1200">Az.Accounts</span></span>
- <span data-ttu-id="04954-1201">Har ändrats från Az.Profile</span><span class="sxs-lookup"><span data-stu-id="04954-1201">Changed from Az.Profile</span></span>
- <span data-ttu-id="04954-1202">Fasta tabellformat för profil- och kontexttyper</span><span class="sxs-lookup"><span data-stu-id="04954-1202">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="04954-1203">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="04954-1203">Az.ApiManagement</span></span>
- <span data-ttu-id="04954-1204">Korrigeringar för #7002</span><span class="sxs-lookup"><span data-stu-id="04954-1204">Fixes for #7002</span></span>
- <span data-ttu-id="04954-1205">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="04954-1205">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="04954-1206">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="04954-1206">Az.Batch</span></span>
- <span data-ttu-id="04954-1207">Lade till möjligheten att se vilken version av Azure Batch Node Agent som körs på var och en av de virtuella datorerna i en pool, via den nya egenskapen `NodeAgentInformation` på `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="04954-1207">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="04954-1208">Standarden `Caching` för `PSDataDisk` är nu `ReadWrite` i stället för `None`.</span><span class="sxs-lookup"><span data-stu-id="04954-1208">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="04954-1209">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="04954-1209">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="04954-1210">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="04954-1210">Az.Billing</span></span>
- <span data-ttu-id="04954-1211">Kombinerar cmdletarna för fakturering, förbrukning och UsageAggregates. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="04954-1211">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="04954-1212">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="04954-1212">Az.CognitivServices</span></span>
- <span data-ttu-id="04954-1213">Lade till kompletterare för SkuName och Typem som är tillgängliga i New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="04954-1213">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="04954-1214">Tog bort parameteruppsättningen GetSkusWithAccountParamSetName från Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="04954-1214">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="04954-1215">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="04954-1215">Az.ContainerInstance</span></span>
- <span data-ttu-id="04954-1216">Stöd för ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="04954-1216">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="04954-1217">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="04954-1217">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="04954-1218">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="04954-1218">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="04954-1219">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="04954-1219">Az.DataLakeStore</span></span>
- <span data-ttu-id="04954-1220">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="04954-1220">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="04954-1221">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="04954-1221">Az.Monitor</span></span>
- <span data-ttu-id="04954-1222">Döpte om Az.Insights till Az.Monitor och andra mindre icke-bakåtkompatibla ändringar. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="04954-1222">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="04954-1223">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="04954-1223">Az.KeyVault</span></span>
- <span data-ttu-id="04954-1224">Tog bort den inaktuella egenskapen PurgeDisabled från utdatatyper</span><span class="sxs-lookup"><span data-stu-id="04954-1224">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="04954-1225">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="04954-1225">Az.MachineLearning</span></span>
- <span data-ttu-id="04954-1226">Inkluderade cmdletarna från modulen Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="04954-1226">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="04954-1227">Az.Media</span><span class="sxs-lookup"><span data-stu-id="04954-1227">Az.Media</span></span>
- <span data-ttu-id="04954-1228">Tog bort inaktuella -Tags-alias från New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="04954-1228">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="04954-1229">Az.Network</span><span class="sxs-lookup"><span data-stu-id="04954-1229">Az.Network</span></span>
<span data-ttu-id="04954-1230">Stöd har lagts till för konfiguration av RewriteRuleSets i Application Gateway</span><span class="sxs-lookup"><span data-stu-id="04954-1230">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="04954-1231">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="04954-1231">New cmdlets added:</span></span>
        - <span data-ttu-id="04954-1232">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="04954-1232">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="04954-1233">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="04954-1233">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="04954-1234">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="04954-1234">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="04954-1235">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="04954-1235">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="04954-1236">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="04954-1236">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="04954-1237">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="04954-1237">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="04954-1238">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="04954-1238">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="04954-1239">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="04954-1239">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="04954-1240">Cmdletar har uppdaterats med den valfria parametern -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="04954-1240">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="04954-1241">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="04954-1241">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="04954-1242">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="04954-1242">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="04954-1243">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="04954-1243">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="04954-1244">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="04954-1244">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="04954-1245">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="04954-1245">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="04954-1246">New-AzureRmApplicationGatewayUrlPathMapConfig har lagt till KeyVault-stöd för Application Gateway med Identity.</span><span class="sxs-lookup"><span data-stu-id="04954-1246">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="04954-1247">Cmdletar har uppdaterats med den valfria parametern -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="04954-1247">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="04954-1248">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="04954-1248">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="04954-1249">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="04954-1249">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="04954-1250">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="04954-1250">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="04954-1251">Cmdleten New-AzApplicationGateway har uppdaterats med den valfria parametern -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="04954-1251">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="04954-1252">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="04954-1252">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="04954-1253">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="04954-1253">Az.OperationalInsights</span></span>
- <span data-ttu-id="04954-1254">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="04954-1254">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="04954-1255">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="04954-1255">Az.Profile</span></span>
- <span data-ttu-id="04954-1256">Modulnamnet har ändrats till Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="04954-1256">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="04954-1257">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="04954-1257">Az.RecoveryServices</span></span>
- <span data-ttu-id="04954-1258">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="04954-1258">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="04954-1259">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="04954-1259">Az.Resources</span></span>
- <span data-ttu-id="04954-1260">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="04954-1260">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="04954-1261">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="04954-1261">Az.ServiceFabric</span></span>
- <span data-ttu-id="04954-1262">Stöd för specificering av certifikat efter eget namn och tumavtryck</span><span class="sxs-lookup"><span data-stu-id="04954-1262">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="04954-1263">Information om fler icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="04954-1263">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="04954-1264">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="04954-1264">Az.SIgnalR</span></span>
- <span data-ttu-id="04954-1265">Allmän tillgänglighet för PowerShell-cmdletar för SIgnalR</span><span class="sxs-lookup"><span data-stu-id="04954-1265">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="04954-1266">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="04954-1266">Az.Sql</span></span>
- <span data-ttu-id="04954-1267">Lade till de nya identifieringstyperna Data_Exfiltration och Unsafe_Action i Threat Detection-cmdletar</span><span class="sxs-lookup"><span data-stu-id="04954-1267">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="04954-1268">Uppdaterade dokumentationsexempel för Sql Auditing-cmdletar</span><span class="sxs-lookup"><span data-stu-id="04954-1268">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="04954-1269">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="04954-1269">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="04954-1270">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="04954-1270">Az.Storage</span></span>
- <span data-ttu-id="04954-1271">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="04954-1271">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="04954-1272">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="04954-1272">Az.Websites</span></span>
- <span data-ttu-id="04954-1273">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="04954-1273">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="04954-1274">0.7.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="04954-1274">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="04954-1275">Allmänt</span><span class="sxs-lookup"><span data-stu-id="04954-1275">General</span></span>

* <span data-ttu-id="04954-1276">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="04954-1276">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="04954-1277">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="04954-1277">Az.Compute</span></span>

* <span data-ttu-id="04954-1278">Lade till stöd för UltraSSD och Galleriavbildningar i de enkla parameteruppsättningarna för `New-AzVm(ss)`-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="04954-1278">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="04954-1279">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="04954-1279">Az.DataLakeStore</span></span>

* <span data-ttu-id="04954-1280">Åtgärdade avslutande snedstreck i domänen för adls-konto</span><span class="sxs-lookup"><span data-stu-id="04954-1280">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="04954-1281">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="04954-1281">Az.FrontDoor</span></span>

* <span data-ttu-id="04954-1282">Brutna länkar korrigerades</span><span class="sxs-lookup"><span data-stu-id="04954-1282">Fixed some broken links</span></span>
    - <span data-ttu-id="04954-1283">I artiklarna New-AzureRmFrontDoor och Set-AzureRmFrontDoor artiklar korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="04954-1283">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="04954-1284">I artikeln New-AzureRmFrontDoorManagedRuleObject korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="04954-1284">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="04954-1285">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="04954-1285">Az.RecoveryServices</span></span>

* <span data-ttu-id="04954-1286">Lade till valideringar på klientsidan för Azure-filresurs med återställningsåtgärder.</span><span class="sxs-lookup"><span data-stu-id="04954-1286">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="04954-1287">Gjorde storageAccountName och storageAccountResourceGroupName valfritt för afs-återställning.</span><span class="sxs-lookup"><span data-stu-id="04954-1287">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="04954-1288">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="04954-1288">Az.Resources</span></span>

* <span data-ttu-id="04954-1289">Korrigering för https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="04954-1289">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="04954-1290">Uppdaterade Get-AzureRmRoleAssignment så att prenumerationsomfattningen används om den anges vid begäran om klassiska administratörer.</span><span class="sxs-lookup"><span data-stu-id="04954-1290">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="04954-1291">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="04954-1291">Az.Sql</span></span>

* <span data-ttu-id="04954-1292">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="04954-1292">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="04954-1293">Korrigerade ett problem med Get-AzureRmSqlDatabaseVulnerabilityAssessment med DotNet-kärna</span><span class="sxs-lookup"><span data-stu-id="04954-1293">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="04954-1294">Ändrade dokumentationen för hjälpmeddelanden som rör SQL Auditing-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="04954-1294">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="04954-1295">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="04954-1295">Az.Storage</span></span>

* <span data-ttu-id="04954-1296">Lade till -EnableHierarchicalNamespace i New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="04954-1296">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="04954-1297">Åtgärdade problemet med att cmdleten Copy File inte kunde återanvända källkontexten på målet om inte -DestContext angetts</span><span class="sxs-lookup"><span data-stu-id="04954-1297">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="04954-1298">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="04954-1298">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="04954-1299">Stöd för statisk webbplatskonfiguration</span><span class="sxs-lookup"><span data-stu-id="04954-1299">Support Static Website configuration</span></span>
    - <span data-ttu-id="04954-1300">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="04954-1300">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="04954-1301">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="04954-1301">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="04954-1302">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="04954-1302">Az.Websites</span></span>

* <span data-ttu-id="04954-1303">Set-AzureRmWebApp och Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="04954-1303">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="04954-1304">Ny parameter (-AzureStoragePath) har lagts till för att ange att Azure Storage-sökvägar ska monteras i containerappar i Windows och Linux.</span><span class="sxs-lookup"><span data-stu-id="04954-1304">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="04954-1305">Använder utdata från den nya cmdleten New-AzureRmWebAppAzureStoragePath som en parameter för att ange sökvägar för Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="04954-1305">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="04954-1306">0.6.1 – november 2018</span><span class="sxs-lookup"><span data-stu-id="04954-1306">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="04954-1307">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="04954-1307">Az.ApiManagement</span></span>
* <span data-ttu-id="04954-1308">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="04954-1308">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="04954-1309">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="04954-1309">Az.Automation</span></span>
* <span data-ttu-id="04954-1310">Swagger baserade Azure Automation-cmdletar</span><span class="sxs-lookup"><span data-stu-id="04954-1310">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="04954-1311">Cmdletar för Uppdateringshantering har lagts till</span><span class="sxs-lookup"><span data-stu-id="04954-1311">Added Update Management cmdlets</span></span>
* <span data-ttu-id="04954-1312">Cmdletar för källkontroll har lagts till</span><span class="sxs-lookup"><span data-stu-id="04954-1312">Added Source Control cmdlets</span></span>
* <span data-ttu-id="04954-1313">Remove-AzureRmAutomationHybridWorkerGroup-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="04954-1313">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="04954-1314">Kommandot för DSC-registreringsnod har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="04954-1314">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="04954-1315">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="04954-1315">Az.Compute</span></span>
* <span data-ttu-id="04954-1316">Problem med SystemAssigned-identitet har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="04954-1316">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="04954-1317">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="04954-1317">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="04954-1318">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="04954-1318">Az.ContainerInstance</span></span>
* <span data-ttu-id="04954-1319">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="04954-1319">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="04954-1320">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="04954-1320">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="04954-1321">uppdatera exempelbeskrivningen för marketplace-cmdletar</span><span class="sxs-lookup"><span data-stu-id="04954-1321">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="04954-1322">Az.Network</span><span class="sxs-lookup"><span data-stu-id="04954-1322">Az.Network</span></span>
* <span data-ttu-id="04954-1323">Cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomErreller Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="04954-1323">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="04954-1324">ICMP tillbaka till stöd för Azure Firewall-nätverksprotokoll har lagts till</span><span class="sxs-lookup"><span data-stu-id="04954-1324">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="04954-1325">Uppdatera cmdlet Test-AzureRmNetworkWatcherConnectivity, lägga till verifiering av mål-id, adress och port.</span><span class="sxs-lookup"><span data-stu-id="04954-1325">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="04954-1326">Åtgärda problem med minnesanvändning i VirtualNetwork-karta</span><span class="sxs-lookup"><span data-stu-id="04954-1326">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="04954-1327">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="04954-1327">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="04954-1328">Åtgärda för att ändra principen för en skyddad fildelning.</span><span class="sxs-lookup"><span data-stu-id="04954-1328">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="04954-1329">Tidszonsprincipen har konverterats till versaler.</span><span class="sxs-lookup"><span data-stu-id="04954-1329">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="04954-1330">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="04954-1330">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="04954-1331">Exempel i New-AzureRmRecoveryServicesAsrProtectableItem har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="04954-1331">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="04954-1332">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="04954-1332">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="04954-1333">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="04954-1333">Az.Relay</span></span>
* <span data-ttu-id="04954-1334">Valfri parameter -KeyValue till New-AzureRmRelayKey cmdlet har lagts till, vilket gör det möjligt för användare att tillhandahålla KeyValue.</span><span class="sxs-lookup"><span data-stu-id="04954-1334">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="04954-1335">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="04954-1335">Az.Resources</span></span>
* <span data-ttu-id="04954-1336">Uppdatera hjälpdokumentation för resursidentitet kopplad till parametrar i `New-AzureRmPolicyAssignment` och `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="04954-1336">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="04954-1337">Lägg till ett exempel för New-AzureRmPolicyDefinition som använder -Metadata</span><span class="sxs-lookup"><span data-stu-id="04954-1337">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="04954-1338">Korrigera så att skiftläge behålls i taggnycklar i NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="04954-1338">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="04954-1339">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="04954-1339">Az.ServiceFabric</span></span>
* <span data-ttu-id="04954-1340">Lägg till utfasningsmeddelanden för kommande icke-kompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="04954-1340">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="04954-1341">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="04954-1341">Az.Sql</span></span>
* <span data-ttu-id="04954-1342">Nya cmdletar för CRUD-åtgärder på Azure Sql Database-hanterad instans och Azure Sql-hanterad databas</span><span class="sxs-lookup"><span data-stu-id="04954-1342">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="04954-1343">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="04954-1343">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="04954-1344">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="04954-1344">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="04954-1345">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="04954-1345">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="04954-1346">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="04954-1346">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="04954-1347">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="04954-1347">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="04954-1348">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="04954-1348">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="04954-1349">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="04954-1349">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="04954-1350">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="04954-1350">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="04954-1351">Hantering av utökad granskningsprincip på en server eller en databas har aktiverats.</span><span class="sxs-lookup"><span data-stu-id="04954-1351">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="04954-1352">Ny parameter (PredicateExpression) har lagts till för att aktivera filtrering av granskningsloggar.</span><span class="sxs-lookup"><span data-stu-id="04954-1352">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="04954-1353">Cmdletar har ändrats så att de använder SQL-klienter i stället för äldre klienter.</span><span class="sxs-lookup"><span data-stu-id="04954-1353">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="04954-1354">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="04954-1354">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="04954-1355">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="04954-1355">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="04954-1356">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="04954-1356">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="04954-1357">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="04954-1357">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="04954-1358">Problem med att använda Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings med lagringskontots namnparameter har korrigerats</span><span class="sxs-lookup"><span data-stu-id="04954-1358">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="04954-1359">0.5.0 – november 2018</span><span class="sxs-lookup"><span data-stu-id="04954-1359">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="04954-1360">Allmänt</span><span class="sxs-lookup"><span data-stu-id="04954-1360">General</span></span>
* <span data-ttu-id="04954-1361">Lade till resurskompletterare till många kärn-cmdletar – dessa gör att du kan stega genom befintliga resursnamn med TABB vid interaktiva anrop till cmdletar</span><span class="sxs-lookup"><span data-stu-id="04954-1361">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="04954-1362">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="04954-1362">Az.Profile</span></span>
* <span data-ttu-id="04954-1363">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="04954-1363">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="04954-1364">Bytte namn på parametern TenantId i cmdleten Connect-AzAccount till Tenant och lade till ett alias för TenantId</span><span class="sxs-lookup"><span data-stu-id="04954-1364">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="04954-1365">Uppdaterade TenantId-beskrivningen för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="04954-1365">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="04954-1366">Åtgärda felmeddelande för misslyckad inloggning när du tillhandahåller klientdomän</span><span class="sxs-lookup"><span data-stu-id="04954-1366">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="04954-1367">Åtgärda problem med att kontextnamn hamnar i konflikt för konton utan prenumerationer i klientorganisationen</span><span class="sxs-lookup"><span data-stu-id="04954-1367">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="04954-1368">Åtgärda problem med DataLake-slutpunkter vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="04954-1368">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="04954-1369">Åtgärdade problem med att Disconnect-AzAccount kastades om den inte anslöts</span><span class="sxs-lookup"><span data-stu-id="04954-1369">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="04954-1370">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="04954-1370">Az.CognitiveServices</span></span>
* <span data-ttu-id="04954-1371">Lade till åtgärden Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="04954-1371">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="04954-1372">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="04954-1372">Az.Compute</span></span>
* <span data-ttu-id="04954-1373">Lade till cmdletarna Add-AzVmssVMDataDisk och Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="04954-1373">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="04954-1374">Get-AzVMImage visar AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="04954-1374">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="04954-1375">Åtgärdade att värdena för alternativen SetAzVMChefExtension -BootstrapOptions och -JsonAttribute inte angavs i json-format.</span><span class="sxs-lookup"><span data-stu-id="04954-1375">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="04954-1376">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="04954-1376">Az.DataLakeStore</span></span>
* <span data-ttu-id="04954-1377">Uppdatera DataLake-paketet till 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="04954-1377">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="04954-1378">Lägg till standardsamtidighet för flertrådade åtgärder.</span><span class="sxs-lookup"><span data-stu-id="04954-1378">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="04954-1379">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="04954-1379">Az.Insights</span></span>
* <span data-ttu-id="04954-1380">Åtgärdade problem #7267 (autoskalningsområde)</span><span class="sxs-lookup"><span data-stu-id="04954-1380">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="04954-1381">Problem med att uppräknade parametrar inte ställdes in ordentligt när du skapade en ny autoskalningsregel (de ställdes alltid in med standardvärdet).</span><span class="sxs-lookup"><span data-stu-id="04954-1381">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="04954-1382">Åtgärdade problem #7513 [Insights] Set-AzDiagnosticSetting kräver uttrycklig specifikation av kategorier när inställningar skapas</span><span class="sxs-lookup"><span data-stu-id="04954-1382">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="04954-1383">Nu kräver inte cmdleten uttrycklig anvisning av kategorierna för att aktiveras under skapande, d.v.s. den fungerar enligt beskrivning</span><span class="sxs-lookup"><span data-stu-id="04954-1383">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="04954-1384">Az.Network</span><span class="sxs-lookup"><span data-stu-id="04954-1384">Az.Network</span></span>
* <span data-ttu-id="04954-1385">PeeringType ändrades till en obligatorisk parameter för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="04954-1385">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="04954-1386">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="04954-1386">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="04954-1387">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="04954-1387">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="04954-1388">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="04954-1388">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="04954-1389">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="04954-1389">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="04954-1390">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="04954-1390">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="04954-1391">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="04954-1391">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="04954-1392">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="04954-1392">Az.PolicyInsights</span></span>
* <span data-ttu-id="04954-1393">Cmdletar för principreparation har lagts till</span><span class="sxs-lookup"><span data-stu-id="04954-1393">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="04954-1394">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="04954-1394">Az.Resources</span></span>
* <span data-ttu-id="04954-1395">Korrigering för https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="04954-1395">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="04954-1396">Tillåt att resurser listas med parametern -ResourceId för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="04954-1396">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="04954-1397">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="04954-1397">Az.ServiceBus</span></span>
* <span data-ttu-id="04954-1398">Skrivskyddad MigrationState-egenskap har lagts till i PSServiceBusMigrationConfigurationAttributes, som hjälper till att hålla koll på migreringstillståndet.</span><span class="sxs-lookup"><span data-stu-id="04954-1398">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="04954-1399">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="04954-1399">Az.ServiceFabric</span></span>
* <span data-ttu-id="04954-1400">Åtgärda att lägga till certifikat till Linux-Vmss.</span><span class="sxs-lookup"><span data-stu-id="04954-1400">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="04954-1401">Åtgärdade Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="04954-1401">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="04954-1402">Använd rätt tumavtryck från nya certifikat (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="04954-1402">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="04954-1403">Visa undantag korrekt (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="04954-1403">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="04954-1404">Åtgärdade Update-AzServiceFabricDurability så att klusterkonfigurationen uppdateras innan Vmss-åtgärden CreateOrUpdate påbörjas.</span><span class="sxs-lookup"><span data-stu-id="04954-1404">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="04954-1405">0.4.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="04954-1405">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="04954-1406">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="04954-1406">Az.Profile</span></span>
* <span data-ttu-id="04954-1407">Åtgärdade problemet med Get-AzSubscription i CloudShell</span><span class="sxs-lookup"><span data-stu-id="04954-1407">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="04954-1408">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="04954-1408">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="04954-1409">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="04954-1409">Az.Compute</span></span>
* <span data-ttu-id="04954-1410">Nya storlekar lades till i listan över godkända VM-storlekar för vilka accelererat nätverk kommer att aktiveras vid användning av den enkla parameteruppsättningen för New-AzVm</span><span class="sxs-lookup"><span data-stu-id="04954-1410">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="04954-1411">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="04954-1411">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="04954-1412">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="04954-1412">Az.DataLakeStore</span></span>
* <span data-ttu-id="04954-1413">Lägger till stöd för regler för virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="04954-1413">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="04954-1414">Get-AzDataLakeStoreVirtualNetworkRule: Hämtar eller listar regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="04954-1414">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="04954-1415">Add-AzDataLakeStoreVirtualNetworkRule: Lägger till en regel för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="04954-1415">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="04954-1416">Set-AzDataLakeStoreVirtualNetworkRule: Ändrar den angivna regeln för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="04954-1416">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="04954-1417">Remove-AzDataLakeStoreVirtualNetworkRule: Tar bort en regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="04954-1417">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="04954-1418">Az.Network</span><span class="sxs-lookup"><span data-stu-id="04954-1418">Az.Network</span></span>
* <span data-ttu-id="04954-1419">Skicka protokollvärdet till serverdelen för att uppdatera cmdleten Test-AzNetworkWatcherConnectivity.</span><span class="sxs-lookup"><span data-stu-id="04954-1419">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="04954-1420">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="04954-1420">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="04954-1421">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="04954-1421">Az.Resources</span></span>
* <span data-ttu-id="04954-1422">Åtgärdade problem där Get-AzRoleDefinition genererar ett oläsligt undantag (när standardprofilen inte innehåller någon prenumeration och ingen omfattning har angetts) genom att lägga till ett beskrivande undantag i scenariot.</span><span class="sxs-lookup"><span data-stu-id="04954-1422">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="04954-1423">Ställ in ”RoleDefinitionNameParameterSet” som standardparameteruppsättning.</span><span class="sxs-lookup"><span data-stu-id="04954-1423">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="04954-1424">0.3.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="04954-1424">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="04954-1425">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="04954-1425">Azure.Storage</span></span>
* <span data-ttu-id="04954-1426">Åtgärda fel där Kopiera blob/fil inte kopierar metadata när målplatsen har ett problem med metadata</span><span class="sxs-lookup"><span data-stu-id="04954-1426">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="04954-1427">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="04954-1427">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="04954-1428">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="04954-1428">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="04954-1429">Stöd för att hämta användningsinformation om en Storage-resurs för en specifik plats och för att lägga till ett varningsmeddelande för att hämta användningsinformation om en global Storage-resurs är inaktuellt.</span><span class="sxs-lookup"><span data-stu-id="04954-1429">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="04954-1430">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="04954-1430">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="04954-1431">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="04954-1431">Az.CognitiveServices</span></span>
* <span data-ttu-id="04954-1432">Stöd för Get-AzCognitiveServicesAccountSkus utan ett befintligt konto.</span><span class="sxs-lookup"><span data-stu-id="04954-1432">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="04954-1433">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="04954-1433">Az.Compute</span></span>
* <span data-ttu-id="04954-1434">Åtgärdade fel där Get-AzVM -ResourceGroupName <rg> returnerar fler än 50 resultat om det behövs</span><span class="sxs-lookup"><span data-stu-id="04954-1434">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="04954-1435">Lade till ett exempel för SimpleParameterSet i hjälpen för cmdleten New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="04954-1435">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="04954-1436">Ett stavfel i förloppsmeddelandet för Azure Disk Encryption har korrigerats</span><span class="sxs-lookup"><span data-stu-id="04954-1436">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="04954-1437">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="04954-1437">Az.DataFactoryV2</span></span>
* <span data-ttu-id="04954-1438">ADF .Net SDK-versionen har uppdaterats till 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="04954-1438">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="04954-1439">Az.Network</span><span class="sxs-lookup"><span data-stu-id="04954-1439">Az.Network</span></span>
* <span data-ttu-id="04954-1440">Funktionalitet för NetworkProfile har lagts till.</span><span class="sxs-lookup"><span data-stu-id="04954-1440">Added NetworkProfile functionality.</span></span> <span data-ttu-id="04954-1441">nya cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="04954-1441">new cmdlets added</span></span>
    - <span data-ttu-id="04954-1442">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="04954-1442">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="04954-1443">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="04954-1443">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="04954-1444">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="04954-1444">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="04954-1445">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="04954-1445">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="04954-1446">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="04954-1446">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="04954-1447">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="04954-1447">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="04954-1448">Länk för tjänstassociering på modell för undernät har lagts till</span><span class="sxs-lookup"><span data-stu-id="04954-1448">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="04954-1449">Cmdletarna New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap och Remove-AzVirtualNetworkTap har lagts till</span><span class="sxs-lookup"><span data-stu-id="04954-1449">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="04954-1450">Cmdletarna Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig och Remove-AzNEtworkInterfaceTapConfig har lagts till</span><span class="sxs-lookup"><span data-stu-id="04954-1450">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="04954-1451">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="04954-1451">Az.RedisCache</span></span>
* <span data-ttu-id="04954-1452">Tillåt att alla strängar används som storleksparametrar framöver.</span><span class="sxs-lookup"><span data-stu-id="04954-1452">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="04954-1453">Lägg till P5 i popup-fönstret PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="04954-1453">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="04954-1454">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="04954-1454">Az.Resources</span></span>
* <span data-ttu-id="04954-1455">Parametern -Mode som saknades i Set-AzPolicyDefinition har lagts till</span><span class="sxs-lookup"><span data-stu-id="04954-1455">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="04954-1456">Åtgärdade buggen för cmdleten Get-AzProviderOperation för åtgärder med ursprung som innehåller användare</span><span class="sxs-lookup"><span data-stu-id="04954-1456">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="04954-1457">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="04954-1457">Az.Sql</span></span>
* <span data-ttu-id="04954-1458">Ett problem där vissa cmdletar för säkerhetskopiering inte kunde identifiera den aktuella azure-prenumerationen har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="04954-1458">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="04954-1459">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="04954-1459">Az.Websites</span></span>
* <span data-ttu-id="04954-1460">Ny cmdlet: Get-AzWebAppContainerContinuousDeploymentUrl – Hämtar webhook-URL:en för kontinuerlig distribution av container</span><span class="sxs-lookup"><span data-stu-id="04954-1460">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="04954-1461">Nya cmdletar: New-AzWebAppContainerPSSession och Enter-WebAppContainerPSSession – Startar en PowerShell-fjärrsession i en containerapp för windows</span><span class="sxs-lookup"><span data-stu-id="04954-1461">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="04954-1462">0.2.0 – september 2018</span><span class="sxs-lookup"><span data-stu-id="04954-1462">0.2.0 - September 2018</span></span>
 <span data-ttu-id="04954-1463">Första versionen</span><span class="sxs-lookup"><span data-stu-id="04954-1463">Initial Release</span></span>