---
ms.openlocfilehash: 3848f7fb8e298d137c747405f32a0776c1a8f029
ms.sourcegitcommit: accff0c2cd6035fcda2d917f6051a5b509eb6255
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/06/2019
ms.locfileid: "65048639"
---
## <a name="200---may-2019"></a><span data-ttu-id="576c3-101">2.0.0 – maj 2019</span><span class="sxs-lookup"><span data-stu-id="576c3-101">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="576c3-102">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="576c3-102">Az.Accounts</span></span>
* <span data-ttu-id="576c3-103">Uppdatera autentiseringsbiblioteket för att åtgärda ADFS-problem med autentisering av användarnamn/lösenord</span><span class="sxs-lookup"><span data-stu-id="576c3-103">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="576c3-104">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="576c3-104">Az.CognitiveServices</span></span>
* <span data-ttu-id="576c3-105">Visa endast Bing-ansvarsfriskrivning för Bing-sökningstjänster.</span><span class="sxs-lookup"><span data-stu-id="576c3-105">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="576c3-106">Förbättra felmeddelande när det inte går att skapa konton.</span><span class="sxs-lookup"><span data-stu-id="576c3-106">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="576c3-107">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="576c3-107">Az.Compute</span></span>
* <span data-ttu-id="576c3-108">Funktion för närhetsplaceringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="576c3-108">Proximity placement group feature.</span></span>
    - <span data-ttu-id="576c3-109">Följande nya cmdletar har lagts till:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="576c3-109">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="576c3-110">Den nya parametern ProximityPlacementGroupId har lagts till i följande cmdletar:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="576c3-110">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="576c3-111">Parametern StorageAccountType har lagts till i New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="576c3-111">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="576c3-112">TargetRegion för New-AzGalleryImageVersion kan innehålla StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="576c3-112">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="576c3-113">Växlingsparametern SkipShutdown har lagts till i Stop-AzVM och Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="576c3-113">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="576c3-114">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="576c3-114">Breaking changes</span></span>
    - <span data-ttu-id="576c3-115">Set-AzVMBootDiagnostics har ändrats till Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="576c3-115">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="576c3-116">Export-AzLogAnalyticThrottledRequests har ändrats till Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="576c3-116">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="576c3-117">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="576c3-117">Az.DeploymentManager</span></span>
* <span data-ttu-id="576c3-118">De första allmänt tillgängliga versionerna av cmdletar för Distributionshanteraren i Azure</span><span class="sxs-lookup"><span data-stu-id="576c3-118">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="576c3-119">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="576c3-119">Az.Dns</span></span>
* <span data-ttu-id="576c3-120">Automatisk delegering av DNS för NameServer</span><span class="sxs-lookup"><span data-stu-id="576c3-120">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="576c3-121">Det överordnade zonnamnet kan användas som ytterligare valfri parameter i cmdleten för att skapa DNS-zoner.</span><span class="sxs-lookup"><span data-stu-id="576c3-121">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="576c3-122">Lägger till NS-poster för en nyligen skapad underordnad zon i den överordnade zonen.</span><span class="sxs-lookup"><span data-stu-id="576c3-122">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="576c3-123">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="576c3-123">Az.FrontDoor</span></span>
* <span data-ttu-id="576c3-124">De första allmänt tillgängliga versionerna av cmdletar för Azure FrontDoor</span><span class="sxs-lookup"><span data-stu-id="576c3-124">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="576c3-125">Byt namn på WAF-cmdletar så att de omfattar ”Waf”</span><span class="sxs-lookup"><span data-stu-id="576c3-125">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="576c3-126">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="576c3-126">Az.HDInsight</span></span>
* <span data-ttu-id="576c3-127">Två cmdletar har tagits bort:</span><span class="sxs-lookup"><span data-stu-id="576c3-127">Removed two cmdlets:</span></span>
    - <span data-ttu-id="576c3-128">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="576c3-128">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="576c3-129">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="576c3-129">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="576c3-130">En ny cmdlet har lagts till, Set-AzHDInsightGatewayCredential, som ersätter Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="576c3-130">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="576c3-131">Uppdatera cmdleten Get-AzHDInsightJobOutput för att skilja mellan läsarrollen och HDInsight-operatörsrollen:</span><span class="sxs-lookup"><span data-stu-id="576c3-131">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="576c3-132">Användare med läsarrollen måste uttryckligen ange parametern ”DefaultStorageAccountKey”, annars uppstår fel.</span><span class="sxs-lookup"><span data-stu-id="576c3-132">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="576c3-133">Användare med HDInsight-operatörsrollen påverkas inte.</span><span class="sxs-lookup"><span data-stu-id="576c3-133">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="576c3-134">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="576c3-134">Az.Monitor</span></span>
* <span data-ttu-id="576c3-135">Nya cmdletar för SQR API (schemalagd frågeregel)</span><span class="sxs-lookup"><span data-stu-id="576c3-135">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="576c3-136">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="576c3-136">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="576c3-137">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="576c3-137">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="576c3-138">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="576c3-138">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="576c3-139">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="576c3-139">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="576c3-140">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="576c3-140">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="576c3-141">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="576c3-141">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="576c3-142">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="576c3-142">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="576c3-143">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="576c3-143">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="576c3-144">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="576c3-144">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="576c3-145">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="576c3-145">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="576c3-146">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="576c3-146">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="576c3-147">[Mer](https://docs.microsoft.com/en-us/rest/api/monitor/scheduledqueryrules) information om SQR API</span><span class="sxs-lookup"><span data-stu-id="576c3-147">[More](https://docs.microsoft.com/en-us/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="576c3-148">Az.Monitor.md har uppdaterats för att omfatta cmdletar för måttbaserade aviseringsregler i GenV2 (inte klassiska)</span><span class="sxs-lookup"><span data-stu-id="576c3-148">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="576c3-149">Az.Network</span><span class="sxs-lookup"><span data-stu-id="576c3-149">Az.Network</span></span>
* <span data-ttu-id="576c3-150">Lägg till stöd för NAT Gateway-resurs</span><span class="sxs-lookup"><span data-stu-id="576c3-150">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="576c3-151">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="576c3-151">New cmdlets</span></span>
        - <span data-ttu-id="576c3-152">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="576c3-152">New-AzNatGateway</span></span>
        - <span data-ttu-id="576c3-153">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="576c3-153">Get-AzNatGateway</span></span>
        - <span data-ttu-id="576c3-154">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="576c3-154">Set-AzNatGateway</span></span>
        - <span data-ttu-id="576c3-155">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="576c3-155">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="576c3-156">Uppdaterade cmdletar</span><span class="sxs-lookup"><span data-stu-id="576c3-156">Updated cmdlets</span></span>
        - <span data-ttu-id="576c3-157">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="576c3-157">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="576c3-158">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="576c3-158">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="576c3-159">Nedanstående kommandon för funktionen har uppdaterats: Ange/ta bort anpassade vägar på Brooklyn Gateway.</span><span class="sxs-lookup"><span data-stu-id="576c3-159">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="576c3-160">New-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ställa in adressprefix som anpassade vägar för att ange gateway.</span><span class="sxs-lookup"><span data-stu-id="576c3-160">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="576c3-161">Set-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ange adressprefix som anpassade vägar för att ange gateway.</span><span class="sxs-lookup"><span data-stu-id="576c3-161">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="576c3-162">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="576c3-162">Az.PolicyInsights</span></span>
* <span data-ttu-id="576c3-163">Stöd för att fråga efter information om principutvärdering.</span><span class="sxs-lookup"><span data-stu-id="576c3-163">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="576c3-164">Lägg till parametern ”-Expand” för Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="576c3-164">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="576c3-165">Stöd för -Expand PolicyEvaluationDetails.</span><span class="sxs-lookup"><span data-stu-id="576c3-165">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="576c3-166">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="576c3-166">Az.RecoveryServices</span></span>
* <span data-ttu-id="576c3-167">Stöd för att dela prenumeration mellan Azure och Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="576c3-167">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="576c3-168">Markering av kommande icke-bakåtkompatibla ändringar för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="576c3-168">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="576c3-169">Korrigering för återställningsplan och åtgärdsplan i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="576c3-169">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="576c3-170">Korrigering för mappning av uppdateringsnätverk i Azure Site Recovery för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="576c3-170">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="576c3-171">Korrigering för instruktioner för uppdateringsskydd i Azure Site Recovery för Azure till Azure för hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="576c3-171">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="576c3-172">Andra mindre korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="576c3-172">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="576c3-173">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="576c3-173">Az.Relay</span></span>
* <span data-ttu-id="576c3-174">Korrigera stavfel i kundriktade meddelanden</span><span class="sxs-lookup"><span data-stu-id="576c3-174">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="576c3-175">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="576c3-175">Az.ServiceBus</span></span>
* <span data-ttu-id="576c3-176">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="576c3-176">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="576c3-177">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="576c3-177">Az.Storage</span></span>
* <span data-ttu-id="576c3-178">Uppgradera till lagringsklientbiblioteket 10.0.1 (namnområdet för alla objekt från detta SDK ändras från ”Microsoft.WindowsAzure.Storage. *till ”Microsoft.Azure.Storage.*”)</span><span class="sxs-lookup"><span data-stu-id="576c3-178">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="576c3-179">Uppgradera till Microsoft.Azure.Management.Storage 11.0.0 för att stödja den nya API-versionen 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="576c3-179">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="576c3-180">Standardlagringskontot i Skapa lagringskonto ändras från ”Storage” till ”StorageV2”</span><span class="sxs-lookup"><span data-stu-id="576c3-180">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="576c3-181">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="576c3-181">New-AzStorageAccount</span></span>
* <span data-ttu-id="576c3-182">Ändra lagringskontots cmdlet-utdata Sku.Name för att passa med indata-SkuName genom att lägga till ”-”. Till exempel ändras ”StandardLRS” till ”Standard_LRS”</span><span class="sxs-lookup"><span data-stu-id="576c3-182">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="576c3-183">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="576c3-183">New-AzStorageAccount</span></span>
    - <span data-ttu-id="576c3-184">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="576c3-184">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="576c3-185">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="576c3-185">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="576c3-186">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="576c3-186">Az.Websites</span></span>
* <span data-ttu-id="576c3-187">Egenskapen ”typ” konfigureras nu för PSSite-objekt som returneras av Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="576c3-187">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="576c3-188">Get-AzWebApp\*Metrics och Get-AzAppServicePlanMetrics markeras som inaktuella</span><span class="sxs-lookup"><span data-stu-id="576c3-188">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="576c3-189">1.8.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="576c3-189">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="576c3-190">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="576c3-190">Highlights since the last major release</span></span>
* <span data-ttu-id="576c3-191">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="576c3-191">General availability of `Az` module</span></span>
* <span data-ttu-id="576c3-192">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="576c3-192">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="576c3-193">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="576c3-193">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="576c3-194">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="576c3-194">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="576c3-195">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="576c3-195">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="576c3-196">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="576c3-196">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="576c3-197">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="576c3-197">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="576c3-198">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="576c3-198">Az.Accounts</span></span>
* <span data-ttu-id="576c3-199">Uppdatera Uninstall-AzureRm för att ta bort moduler i Mac på ett korrekt sätt</span><span class="sxs-lookup"><span data-stu-id="576c3-199">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="576c3-200">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="576c3-200">Az.Batch</span></span>
* <span data-ttu-id="576c3-201">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="576c3-201">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="576c3-202">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="576c3-202">Az.Cdn</span></span>
* <span data-ttu-id="576c3-203">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="576c3-203">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="576c3-204">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="576c3-204">Az.CognitiveServices</span></span>
* <span data-ttu-id="576c3-205">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="576c3-205">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="576c3-206">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="576c3-206">Az.Compute</span></span>
* <span data-ttu-id="576c3-207">Åtgärda problem med AEM-installationen om resurs-ID:n för diskar innehåller resourcegroups i gemener i resurs-ID:n</span><span class="sxs-lookup"><span data-stu-id="576c3-207">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="576c3-208">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="576c3-208">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="576c3-209">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="576c3-209">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="576c3-210">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="576c3-210">Az.DataFactory</span></span>
* <span data-ttu-id="576c3-211">Lägg till SsisProperties om NodeCount inte är null för hanterad integreringskörning.</span><span class="sxs-lookup"><span data-stu-id="576c3-211">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="576c3-212">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="576c3-212">Az.DataLakeStore</span></span>
* <span data-ttu-id="576c3-213">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="576c3-213">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="576c3-214">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="576c3-214">Az.EventGrid</span></span>
* <span data-ttu-id="576c3-215">Hjälptexten för slutpunkten har uppdaterats för att visa att resurser ska skapas innan cmdletarna för att skapa/uppdatera händelseprenumerationer används.</span><span class="sxs-lookup"><span data-stu-id="576c3-215">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="576c3-216">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="576c3-216">Az.EventHub</span></span>
* <span data-ttu-id="576c3-217">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="576c3-217">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="576c3-218">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="576c3-218">Az.HDInsight</span></span>
* <span data-ttu-id="576c3-219">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="576c3-219">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="576c3-220">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="576c3-220">Az.IotHub</span></span>
* <span data-ttu-id="576c3-221">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="576c3-221">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="576c3-222">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="576c3-222">Az.KeyVault</span></span>
* <span data-ttu-id="576c3-223">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="576c3-223">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="576c3-224">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="576c3-224">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="576c3-225">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="576c3-225">Az.MachineLearning</span></span>
* <span data-ttu-id="576c3-226">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="576c3-226">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="576c3-227">Az.Media</span><span class="sxs-lookup"><span data-stu-id="576c3-227">Az.Media</span></span>
* <span data-ttu-id="576c3-228">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="576c3-228">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="576c3-229">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="576c3-229">Az.Monitor</span></span>
  * <span data-ttu-id="576c3-230">Nya cmdletar för måttbaserad aviseringsregel i GenV2 (inte klassisk)</span><span class="sxs-lookup"><span data-stu-id="576c3-230">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="576c3-231">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="576c3-231">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="576c3-232">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="576c3-232">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="576c3-233">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="576c3-233">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="576c3-234">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="576c3-234">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="576c3-235">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="576c3-235">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="576c3-236">Monitor SDK har uppdaterats till version 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="576c3-236">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="576c3-237">Az.Network</span><span class="sxs-lookup"><span data-stu-id="576c3-237">Az.Network</span></span>
* <span data-ttu-id="576c3-238">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="576c3-238">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="576c3-239">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="576c3-239">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="576c3-240">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="576c3-240">Az.NotificationHubs</span></span>
* <span data-ttu-id="576c3-241">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="576c3-241">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="576c3-242">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="576c3-242">Az.OperationalInsights</span></span>
* <span data-ttu-id="576c3-243">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="576c3-243">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="576c3-244">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="576c3-244">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="576c3-245">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="576c3-245">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="576c3-246">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="576c3-246">Az.RecoveryServices</span></span>
* <span data-ttu-id="576c3-247">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="576c3-247">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="576c3-248">Tabellformatet för SQL i virtuella Azure-datorer har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="576c3-248">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="576c3-249">En alternativ metod för att hämta platser i AzureFileShare har lagts till</span><span class="sxs-lookup"><span data-stu-id="576c3-249">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="576c3-250">ScheduleRunDays i SchedulePolicy-objekt har uppdaterats enligt tidszon</span><span class="sxs-lookup"><span data-stu-id="576c3-250">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="576c3-251">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="576c3-251">Az.RedisCache</span></span>
* <span data-ttu-id="576c3-252">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="576c3-252">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="576c3-253">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="576c3-253">Az.Resources</span></span>
* <span data-ttu-id="576c3-254">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="576c3-254">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="576c3-255">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="576c3-255">Az.Sql</span></span>
* <span data-ttu-id="576c3-256">Ersätt Monitor SDK-beroende med vanlig kod</span><span class="sxs-lookup"><span data-stu-id="576c3-256">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="576c3-257">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="576c3-257">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="576c3-258">Förbättrad process för klassificering av flera kolumner.</span><span class="sxs-lookup"><span data-stu-id="576c3-258">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="576c3-259">Inkludera SKU-egenskaper (SKU-namn, serie, kapacitet) i svaret från Get-AzSqlServerServiceObjective och formatera som tabell som standard.</span><span class="sxs-lookup"><span data-stu-id="576c3-259">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="576c3-260">Möjlighet att använda Get-AzSqlServerServiceObjective efter plats utan att behöva en redan befintlig server i regionen.</span><span class="sxs-lookup"><span data-stu-id="576c3-260">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="576c3-261">Stöd för tidszonsparametern när hanterade instanser skapas.</span><span class="sxs-lookup"><span data-stu-id="576c3-261">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="576c3-262">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="576c3-262">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="576c3-263">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="576c3-263">Az.Websites</span></span>
* <span data-ttu-id="576c3-264">åtgärdar Set-AzWebApp och Set-AzWebAppSlot så att de inte tar bort taggar vid körning</span><span class="sxs-lookup"><span data-stu-id="576c3-264">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="576c3-265">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="576c3-265">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="576c3-266">SDK för WebSites har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="576c3-266">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="576c3-267">Egenskapen AdminSiteName har tagits bort från PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="576c3-267">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="576c3-268">1.7.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="576c3-268">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="576c3-269">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="576c3-269">Highlights since the last major release</span></span>
* <span data-ttu-id="576c3-270">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="576c3-270">General availability of `Az` module</span></span>
* <span data-ttu-id="576c3-271">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="576c3-271">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="576c3-272">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="576c3-272">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="576c3-273">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="576c3-273">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="576c3-274">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="576c3-274">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="576c3-275">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="576c3-275">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="576c3-276">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="576c3-276">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="576c3-277">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="576c3-277">Az.Accounts</span></span>
* <span data-ttu-id="576c3-278">Add-AzEnvironment och Set-AzEnvironment har uppdaterats för att godkänna parametern AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="576c3-278">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="576c3-279">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="576c3-279">Az.AnalysisServices</span></span>
* <span data-ttu-id="576c3-280">ServiceClient används i cmdletar för dataplan och den ursprungliga autentiseringslogiken har tagits bort</span><span class="sxs-lookup"><span data-stu-id="576c3-280">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="576c3-281">Add-AzureASAccount används för omslutning av Connect-AzAccount för att undvika en icke-bakåtkompatibel ändring</span><span class="sxs-lookup"><span data-stu-id="576c3-281">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="576c3-282">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="576c3-282">Az.Automation</span></span>
* <span data-ttu-id="576c3-283">Buggen för cmdleten New-AzAutomationSoftwareUpdateConfiguration för inkluderingar har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="576c3-283">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="576c3-284">Nu bör parametern IncludedKbNumber och IncludedPackageNameMask fungera.</span><span class="sxs-lookup"><span data-stu-id="576c3-284">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="576c3-285">Felkorrigering för dynamiska grupper i uppdateringshanteringen för azure automation</span><span class="sxs-lookup"><span data-stu-id="576c3-285">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="576c3-286">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="576c3-286">Az.Compute</span></span>
* <span data-ttu-id="576c3-287">Lägg till parametern HyperVGeneration i New-AzDiskConfig och New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="576c3-287">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="576c3-288">Tillåt att virtuella datorer skapas med galleribilder från andra klientorganisationer.</span><span class="sxs-lookup"><span data-stu-id="576c3-288">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="576c3-289">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="576c3-289">Az.ContainerInstance</span></span>
* <span data-ttu-id="576c3-290">Ett problem har åtgärdats i parametern -Command för New-AzContainerGroup som lade till ett avslutande tomt argument</span><span class="sxs-lookup"><span data-stu-id="576c3-290">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="576c3-291">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="576c3-291">Az.DataFactory</span></span>
* <span data-ttu-id="576c3-292">ADF .Net SDK-versionen har uppdaterats till 3.0.2</span><span class="sxs-lookup"><span data-stu-id="576c3-292">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="576c3-293">Cmdleten Set-AzDataFactoryV2 har uppdaterats med extra parametrar för inställningar som rör RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="576c3-293">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="576c3-294">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="576c3-294">Az.Resources</span></span>
* <span data-ttu-id="576c3-295">Förbättra hanteringen av providrar för Get-AzResource när parametrarna -ResourceId eller -ResourceGroupName, -Name och -ResourceType tillhandahålls</span><span class="sxs-lookup"><span data-stu-id="576c3-295">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="576c3-296">Förbättra felhanteringen för Test-AzDeployment och Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="576c3-296">Improve error handling for for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="576c3-297">Hantera fel utanför distributionsvalideringen och ta med dem i kommandoutdata istället</span><span class="sxs-lookup"><span data-stu-id="576c3-297">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="576c3-298">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="576c3-298">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="576c3-299">Lägg till växlingsparametern -IgnoreDynamicParameters till en uppsättning av cmdletar för distribution för att hoppa över fråga i skript och jobbscenarier</span><span class="sxs-lookup"><span data-stu-id="576c3-299">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="576c3-300">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="576c3-300">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="576c3-301">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="576c3-301">Az.Sql</span></span>
* <span data-ttu-id="576c3-302">Stöd för dataklassificering av databaser.</span><span class="sxs-lookup"><span data-stu-id="576c3-302">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="576c3-303">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="576c3-303">Az.Storage</span></span>
* <span data-ttu-id="576c3-304">Rapportera detaljfel när lagringskontext skapas med parametern -UseConnectedAccount, men utan inloggning på Azure-kontot</span><span class="sxs-lookup"><span data-stu-id="576c3-304">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="576c3-305">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="576c3-305">New-AzStorageContext</span></span>
* <span data-ttu-id="576c3-306">Stöd för att hantera Blob Service-egenskaper för ett angivet lagringskonto med API:et för hanteringsplan</span><span class="sxs-lookup"><span data-stu-id="576c3-306">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="576c3-307">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="576c3-307">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="576c3-308">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="576c3-308">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="576c3-309">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="576c3-309">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="576c3-310">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="576c3-310">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="576c3-311">Stöd för -AsJob-cmdletar för att ladda upp och ladda ned blobar och filer</span><span class="sxs-lookup"><span data-stu-id="576c3-311">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="576c3-312">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="576c3-312">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="576c3-313">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="576c3-313">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="576c3-314">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="576c3-314">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="576c3-315">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="576c3-315">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="576c3-316">1.6.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="576c3-316">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="576c3-317">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="576c3-317">Highlights since the last major release</span></span>
* <span data-ttu-id="576c3-318">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="576c3-318">General availability of `Az` module</span></span>
* <span data-ttu-id="576c3-319">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="576c3-319">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="576c3-320">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="576c3-320">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="576c3-321">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="576c3-321">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="576c3-322">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="576c3-322">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="576c3-323">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="576c3-323">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="576c3-324">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="576c3-324">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="576c3-325">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="576c3-325">Az.Automation</span></span>
* <span data-ttu-id="576c3-326">Azure Automation – ändring av uppdateringshantering för stöd för de nya funktionerna:</span><span class="sxs-lookup"><span data-stu-id="576c3-326">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="576c3-327">Dynamisk gruppering</span><span class="sxs-lookup"><span data-stu-id="576c3-327">Dynamic grouping</span></span>
    * <span data-ttu-id="576c3-328">För-/efterskrift</span><span class="sxs-lookup"><span data-stu-id="576c3-328">Pre-Post script</span></span>
    * <span data-ttu-id="576c3-329">Inställning för omstart</span><span class="sxs-lookup"><span data-stu-id="576c3-329">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="576c3-330">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="576c3-330">Az.Compute</span></span>
* <span data-ttu-id="576c3-331">Åtgärda problem med sökvägsmatchning i Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="576c3-331">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="576c3-332">Uppdatera Compute-klientbibliotek till 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="576c3-332">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="576c3-333">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="576c3-333">Az.KeyVault</span></span>
* <span data-ttu-id="576c3-334">Stöd för jokertecken för KeyVault-cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="576c3-334">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="576c3-335">Az.Network</span><span class="sxs-lookup"><span data-stu-id="576c3-335">Az.Network</span></span>
* <span data-ttu-id="576c3-336">Lägg till stöd för Threat Intelligence för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="576c3-336">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="576c3-337">Lägg till resurs för brandväggsprincip på översta nivå och anpassade regler för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="576c3-337">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="576c3-338">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="576c3-338">Az.RecoveryServices</span></span>
* <span data-ttu-id="576c3-339">SnapshotRetentionInDays har lagts till i Azure-principen för virtuella datorer för stöd av Instant RP</span><span class="sxs-lookup"><span data-stu-id="576c3-339">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="576c3-340">Pipe-stöd för avregistrering av container har lagts till</span><span class="sxs-lookup"><span data-stu-id="576c3-340">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="576c3-341">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="576c3-341">Az.Resources</span></span>
* <span data-ttu-id="576c3-342">Uppdatera stöd för jokertecken för Get-AzResource och Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="576c3-342">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="576c3-343">Uppdatera autentiseringsuppgifter som används vid allmänna anrop till ARM</span><span class="sxs-lookup"><span data-stu-id="576c3-343">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="576c3-344">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="576c3-344">Az.Sql</span></span>
* <span data-ttu-id="576c3-345">Cmdlet-parametern (ExcludeDetectionType) för Hotidentifiering ändrades från DetectionType till sträng[] för att framtidssäkra den när nya DetectionTypes läggs till, och även för att stödja automatisk ifyllning.</span><span class="sxs-lookup"><span data-stu-id="576c3-345">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="576c3-346">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="576c3-346">Az.Storage</span></span>
* <span data-ttu-id="576c3-347">Stöd för att hämta/ange/ta bort hanteringsprincip på ett lagringskonto</span><span class="sxs-lookup"><span data-stu-id="576c3-347">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="576c3-348">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="576c3-348">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="576c3-349">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="576c3-349">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="576c3-350">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="576c3-350">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="576c3-351">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="576c3-351">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="576c3-352">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="576c3-352">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="576c3-353">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="576c3-353">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="576c3-354">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="576c3-354">Az.Websites</span></span>
* <span data-ttu-id="576c3-355">Åtgärda fel med ARM-mall som avbryter kloning av alla platser med 'New-AzWebApp -IncludeSourceWebAppSlots'</span><span class="sxs-lookup"><span data-stu-id="576c3-355">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="576c3-356">1.5.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="576c3-356">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="576c3-357">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="576c3-357">Az.Accounts</span></span>
* <span data-ttu-id="576c3-358">Lägg till kommandot Register-AzModule för stöd för AutoRest-genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="576c3-358">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="576c3-359">Uppdatera exempel för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="576c3-359">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="576c3-360">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="576c3-360">Az.Automation</span></span>
* <span data-ttu-id="576c3-361">Problem med att hämta vissa månadsscheman i flera Azure Automation-cmdletar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="576c3-361">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="576c3-362">Åtgärda problem med att Get-AzAutomationDscNode bara returnerar de 20 översta noderna.</span><span class="sxs-lookup"><span data-stu-id="576c3-362">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="576c3-363">Nu returneras alla noder</span><span class="sxs-lookup"><span data-stu-id="576c3-363">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="576c3-364">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="576c3-364">Az.Cdn</span></span>
* <span data-ttu-id="576c3-365">Nya Powershell-cmdletar för att aktivera/inaktivera anpassade domän-HTTPS har lagts till och de gamla har gjorts inaktuella</span><span class="sxs-lookup"><span data-stu-id="576c3-365">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="576c3-366">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="576c3-366">Az.Compute</span></span>
* <span data-ttu-id="576c3-367">Lägg till stöd för jokertecken för Get-cmdletar</span><span class="sxs-lookup"><span data-stu-id="576c3-367">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="576c3-368">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="576c3-368">Az.DataFactory</span></span>
* <span data-ttu-id="576c3-369">ADF .Net SDK-versionen har uppdaterats till 3.0.1</span><span class="sxs-lookup"><span data-stu-id="576c3-369">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="576c3-370">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="576c3-370">Az.LogicApp</span></span>
* <span data-ttu-id="576c3-371">Åtgärda problemet med att ListWorkflows endast hämtar den första sidan med resultat</span><span class="sxs-lookup"><span data-stu-id="576c3-371">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="576c3-372">Az.Network</span><span class="sxs-lookup"><span data-stu-id="576c3-372">Az.Network</span></span>
* <span data-ttu-id="576c3-373">Lägg till stöd för jokertecken för Network-cmdletar</span><span class="sxs-lookup"><span data-stu-id="576c3-373">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="576c3-374">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="576c3-374">Az.RecoveryServices</span></span>
* <span data-ttu-id="576c3-375">Stöd har lagts till för SQL Server i virtuella Azure-datorer</span><span class="sxs-lookup"><span data-stu-id="576c3-375">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="576c3-376">SDK-uppdatering</span><span class="sxs-lookup"><span data-stu-id="576c3-376">SDK Update</span></span>
* <span data-ttu-id="576c3-377">Get-ProtectableItem-incheckning i VMappContainer har tagits bort</span><span class="sxs-lookup"><span data-stu-id="576c3-377">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="576c3-378">Name och ServerName har lagts till som parametrar för Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="576c3-378">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="576c3-379">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="576c3-379">Az.Resources</span></span>
* <span data-ttu-id="576c3-380">Lägg till parametern `-TemplateObject` i cmdletar för distribution</span><span class="sxs-lookup"><span data-stu-id="576c3-380">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="576c3-381">Mer information här: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="576c3-381">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="576c3-382">Åtgärda problem med piping av resultatet i `Get-AzResource` till `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="576c3-382">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="576c3-383">Mer information här: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="576c3-383">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="576c3-384">Åtgärda problem med ändring av JSON-datatyp när `Set-AzResource` körs</span><span class="sxs-lookup"><span data-stu-id="576c3-384">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="576c3-385">Mer information här: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="576c3-385">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="576c3-386">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="576c3-386">Az.Sql</span></span>
* <span data-ttu-id="576c3-387">AuditingEndpointsCommunicator uppdateras.</span><span class="sxs-lookup"><span data-stu-id="576c3-387">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="576c3-388">Åtgärdar beteendet hos ett gränsscenario när nya diagnostikinställningar skapas.</span><span class="sxs-lookup"><span data-stu-id="576c3-388">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="576c3-389">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="576c3-389">Az.Storage</span></span>
* <span data-ttu-id="576c3-390">Stöd för BlockBlobStorage när Storage-konto skapas      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="576c3-390">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="576c3-391">1.4.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="576c3-391">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="576c3-392">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="576c3-392">Az.AnalysisServices</span></span>
* <span data-ttu-id="576c3-393">Inaktuell AddAzureASAccount-cmdlet</span><span class="sxs-lookup"><span data-stu-id="576c3-393">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="576c3-394">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="576c3-394">Az.Automation</span></span>
* <span data-ttu-id="576c3-395">Hjälpen för Import-AzAutomationDscNodeConfiguration har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="576c3-395">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="576c3-396">Konfigurationsnamnsvalidering har lagts till i cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="576c3-396">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="576c3-397">Förbättrad felhantering för cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="576c3-397">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="576c3-398">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="576c3-398">Az.CognitiveServices</span></span>
* <span data-ttu-id="576c3-399">CustomSubdomainName har lagts till som en ny valfri parameter för New-AzCognitiveServicesAccount, som används för att ange underdomän för resursen.</span><span class="sxs-lookup"><span data-stu-id="576c3-399">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="576c3-400">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="576c3-400">Az.Compute</span></span>
* <span data-ttu-id="576c3-401">Problemet med ID-parameteruppsättningar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="576c3-401">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="576c3-402">Get-AzVMExtension har uppdaterats så att alla installerade tillägg visas om parametern Name inte har angetts</span><span class="sxs-lookup"><span data-stu-id="576c3-402">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="576c3-403">Parametrarna Tag och ResourceId har lagts till i cmdleten Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="576c3-403">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="576c3-404">Get-AzVmssVM utan instans-ID och med InstanceView kan visa virtuella VMSS-datorer med instansvyn.</span><span class="sxs-lookup"><span data-stu-id="576c3-404">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="576c3-405">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="576c3-405">Az.DataLakeStore</span></span>
* <span data-ttu-id="576c3-406">Cmdletar har lagts till för uppräkning och återställning av borttagna objekt i ADL</span><span class="sxs-lookup"><span data-stu-id="576c3-406">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="576c3-407">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="576c3-407">Az.EventHub</span></span>
* <span data-ttu-id="576c3-408">Ny boolesk egenskap SkipEmptyArchives har lagts till i Skip Empty Archives i CaptureDescription-klassen i Eventhub</span><span class="sxs-lookup"><span data-stu-id="576c3-408">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="576c3-409">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="576c3-409">Az.KeyVault</span></span>
* <span data-ttu-id="576c3-410">Taggning i Set-AzKeyVaultSecret har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="576c3-410">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="576c3-411">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="576c3-411">Az.LogicApp</span></span>
* <span data-ttu-id="576c3-412">Grundläggande SKU har lagts till för Integrationskonton</span><span class="sxs-lookup"><span data-stu-id="576c3-412">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="576c3-413">XSLT 2.0, XSLT 3.0 och Flytande mappningstyper har lagts till</span><span class="sxs-lookup"><span data-stu-id="576c3-413">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="576c3-414">Nya cmdletar för integrationskontosammansättningar</span><span class="sxs-lookup"><span data-stu-id="576c3-414">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="576c3-415">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="576c3-415">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="576c3-416">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="576c3-416">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="576c3-417">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="576c3-417">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="576c3-418">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="576c3-418">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="576c3-419">Nya cmdletar för batchkonfiguration för integrationskonto</span><span class="sxs-lookup"><span data-stu-id="576c3-419">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="576c3-420">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="576c3-420">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="576c3-421">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="576c3-421">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="576c3-422">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="576c3-422">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="576c3-423">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="576c3-423">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="576c3-424">Logic App-SDK har uppdaterats till version 4.1.0</span><span class="sxs-lookup"><span data-stu-id="576c3-424">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="576c3-425">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="576c3-425">Az.Monitor</span></span>
* <span data-ttu-id="576c3-426">Hjälpen för Get-AzMetric har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="576c3-426">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="576c3-427">Az.Network</span><span class="sxs-lookup"><span data-stu-id="576c3-427">Az.Network</span></span>
* <span data-ttu-id="576c3-428">Hjälpexempel för Add-AzApplicationGatewayCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="576c3-428">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="576c3-429">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="576c3-429">Az.OperationalInsights</span></span>
* <span data-ttu-id="576c3-430">Ytterligare stöd för datakällorna New och Get ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="576c3-430">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="576c3-431">Ny ApplicationInsights-typ har lagts till för att ge stöd för ”Get specific” och ”Get all” för ApplicationInsights-datakällor för angiven arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="576c3-431">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="576c3-432">Cmdleten New-AzOperationalInsightsApplicationInsightsDataSource har lagts till för att skapa datakälla med angivna parametrar för Application Insights-resurs: subscription Id, resourceGroupName och name.</span><span class="sxs-lookup"><span data-stu-id="576c3-432">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="576c3-433">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="576c3-433">Az.Resources</span></span>
* <span data-ttu-id="576c3-434">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="576c3-434">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="576c3-435">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="576c3-435">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="576c3-436">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="576c3-436">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="576c3-437">Fel som gör att KeyCredentials inte kan skapas upprepade gånger har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="576c3-437">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="576c3-438">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="576c3-438">Az.Sql</span></span>
* <span data-ttu-id="576c3-439">Lägg till stöd för hyperskalanivån för SQL DB</span><span class="sxs-lookup"><span data-stu-id="576c3-439">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="576c3-440">Ett fel har åtgärdats där återställningen kunde misslyckas på grund av onödiga inställningsegenskaper i restore-förfrågan</span><span class="sxs-lookup"><span data-stu-id="576c3-440">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="576c3-441">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="576c3-441">Az.Websites</span></span>
* <span data-ttu-id="576c3-442">Rätt exempel i Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="576c3-442">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="576c3-443">1.3.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="576c3-443">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="576c3-444">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="576c3-444">Az.Accounts</span></span>
* <span data-ttu-id="576c3-445">Uppdatera till den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="576c3-445">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="576c3-446">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="576c3-446">Az.AnalysisServices</span></span>
<span data-ttu-id="576c3-447">Allmän tillgänglighet för Az.AnalysisServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="576c3-447">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="576c3-448">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="576c3-448">Az.Compute</span></span>
* <span data-ttu-id="576c3-449">AEM-tillägg: Lägg till stöd för UltraSSD-, P60-, P70- och P80-diskar</span><span class="sxs-lookup"><span data-stu-id="576c3-449">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="576c3-450">Uppdatera hjälpbeskrivning för Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="576c3-450">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="576c3-451">Uppdatera hjälpbeskrivning och exempel för Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="576c3-451">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="576c3-452">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="576c3-452">Az.RecoveryServices</span></span>
<span data-ttu-id="576c3-453">Allmän tillgänglighet för Az.RecoveryServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="576c3-453">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="576c3-454">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="576c3-454">Az.Resources</span></span>
* <span data-ttu-id="576c3-455">Korrigera taggar för resursgrupper</span><span class="sxs-lookup"><span data-stu-id="576c3-455">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="576c3-456">Mer information här: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="576c3-456">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="576c3-457">Åtgärda problem där `Get-AzureRmRoleAssignment` inte respekterar -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="576c3-457">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="576c3-458">Mer information här: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="576c3-458">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="576c3-459">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="576c3-459">Az.Sql</span></span>
* <span data-ttu-id="576c3-460">Lägga till Get/Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="576c3-460">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="576c3-461">Åtgärda problem där ett nullref-undantag uppstår när du kör SQL-cmdletar och inte är inloggad på ett Azure-konto</span><span class="sxs-lookup"><span data-stu-id="576c3-461">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="576c3-462">Åtgärda nullref-undantag i Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="576c3-462">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="576c3-463">1.2.1 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="576c3-463">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="576c3-464">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="576c3-464">Az.Accounts</span></span>
* <span data-ttu-id="576c3-465">Version med rätt version av autentisering</span><span class="sxs-lookup"><span data-stu-id="576c3-465">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="576c3-466">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="576c3-466">Az.AnalysisServices</span></span>
* <span data-ttu-id="576c3-467">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="576c3-467">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="576c3-468">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="576c3-468">Az.RecoveryServices</span></span>
* <span data-ttu-id="576c3-469">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="576c3-469">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="576c3-470">1.2.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="576c3-470">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="576c3-471">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="576c3-471">Az.Accounts</span></span>
* <span data-ttu-id="576c3-472">Lägga till interaktiv autentisering och autentisering med användarnamn/lösenord för endast Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="576c3-472">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="576c3-473">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="576c3-473">Update incorrect online help URLs</span></span>
* <span data-ttu-id="576c3-474">Lägga till varningsmeddelande i PS Core för Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="576c3-474">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="576c3-475">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="576c3-475">Az.Aks</span></span>
* <span data-ttu-id="576c3-476">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="576c3-476">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="576c3-477">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="576c3-477">Az.Automation</span></span>
* <span data-ttu-id="576c3-478">Stöd för Python 2-runbookflöden har lagts till</span><span class="sxs-lookup"><span data-stu-id="576c3-478">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="576c3-479">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="576c3-479">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="576c3-480">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="576c3-480">Az.Cdn</span></span>
* <span data-ttu-id="576c3-481">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="576c3-481">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="576c3-482">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="576c3-482">Az.Compute</span></span>
* <span data-ttu-id="576c3-483">Lägga till cmdleten Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="576c3-483">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="576c3-484">Lägga till TempDisk-parameter i Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="576c3-484">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="576c3-485">Korrigera varningsmeddelande för New-AzVM</span><span class="sxs-lookup"><span data-stu-id="576c3-485">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="576c3-486">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="576c3-486">Az.ContainerRegistry</span></span>
* <span data-ttu-id="576c3-487">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="576c3-487">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="576c3-488">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="576c3-488">Az.DataFactory</span></span>
* <span data-ttu-id="576c3-489">ADF .Net SDK-versionen har uppdaterats till 3.0.0</span><span class="sxs-lookup"><span data-stu-id="576c3-489">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="576c3-490">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="576c3-490">Az.DataLakeStore</span></span>
* <span data-ttu-id="576c3-491">Åtgärda problem med ADLS-slutpunkt vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="576c3-491">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="576c3-492">Mer information här: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="576c3-492">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="576c3-493">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="576c3-493">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="576c3-494">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="576c3-494">Az.IotHub</span></span>
* <span data-ttu-id="576c3-495">Lägga till kodningsformat i cmdleten Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="576c3-495">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="576c3-496">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="576c3-496">Az.KeyVault</span></span>
* <span data-ttu-id="576c3-497">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="576c3-497">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="576c3-498">Az.Network</span><span class="sxs-lookup"><span data-stu-id="576c3-498">Az.Network</span></span>
* <span data-ttu-id="576c3-499">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="576c3-499">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="576c3-500">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="576c3-500">Az.Resources</span></span>
* <span data-ttu-id="576c3-501">Åtgärda felaktiga exempel i referensdokumentationen ”New-AzADAppCredential” och ”New-AzADSpCredential”</span><span class="sxs-lookup"><span data-stu-id="576c3-501">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="576c3-502">Åtgärda problem där sökvägen för parametern ”-TemplateFile” inte omvandlas innan cmdletarna för distribution i resursgruppen körs</span><span class="sxs-lookup"><span data-stu-id="576c3-502">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="576c3-503">Az.Resources: Korrigera dokumentationen om standardvärdet för New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="576c3-503">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="576c3-504">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="576c3-504">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="576c3-505">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="576c3-505">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="576c3-506">Åtgärda formateringsproblemet med objektet ”PSResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="576c3-506">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="576c3-507">Mer information här: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="576c3-507">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="576c3-508">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="576c3-508">Az.ServiceFabric</span></span>
* <span data-ttu-id="576c3-509">Återställ när ett certifikat läggs till i en Virtual Machine Scale Sets-modell men ett undantag genereras. Detta har gjorts för att åtgärda följande fel: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="576c3-509">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="576c3-510">Korrigera några felmeddelanden.</span><span class="sxs-lookup"><span data-stu-id="576c3-510">Fix some error messages.</span></span>
* <span data-ttu-id="576c3-511">Korrigering av skapande av kluster med ARM-mall som är standard för New-AzServiceFabriCluster som inte fungerade med migrering till Az.</span><span class="sxs-lookup"><span data-stu-id="576c3-511">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="576c3-512">Korrigering av tilläggning av kluster/programcertifikat så att endast VM Scale Sets som motsvarar klustret läggs till genom att kontrollera ID för klustret i tillägget.</span><span class="sxs-lookup"><span data-stu-id="576c3-512">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="576c3-513">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="576c3-513">Az.SignalR</span></span>
* <span data-ttu-id="576c3-514">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="576c3-514">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="576c3-515">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="576c3-515">Az.Sql</span></span>
* <span data-ttu-id="576c3-516">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="576c3-516">Update incorrect online help URLs</span></span>
* <span data-ttu-id="576c3-517">Uppdaterad parameterbeskrivning för LicenseType-parameter med möjliga värden</span><span class="sxs-lookup"><span data-stu-id="576c3-517">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="576c3-518">Korrigering för att uppdatera hanterad instansidentitet som inte fungerar när det är den enda uppdaterade egenskapen</span><span class="sxs-lookup"><span data-stu-id="576c3-518">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="576c3-519">Stöd för anpassad sortering på hanterad instans</span><span class="sxs-lookup"><span data-stu-id="576c3-519">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="576c3-520">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="576c3-520">Az.Storage</span></span>
* <span data-ttu-id="576c3-521">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="576c3-521">Update incorrect online help URLs</span></span>
* <span data-ttu-id="576c3-522">Tillhandahåll detaljerat felmeddelande när en användare försöker hämta/konfigurera klassisk loggning/mått på ett Premium Storage-konto eftersom Premium Storage-kontot inte har stöd för klassisk loggning/mått.</span><span class="sxs-lookup"><span data-stu-id="576c3-522">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="576c3-523">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="576c3-523">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="576c3-524">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="576c3-524">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="576c3-525">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="576c3-525">Az.TrafficManager</span></span>
* <span data-ttu-id="576c3-526">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="576c3-526">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="576c3-527">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="576c3-527">Az.Websites</span></span>
* <span data-ttu-id="576c3-528">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="576c3-528">Update incorrect online help URLs</span></span>
* <span data-ttu-id="576c3-529">Korrigerar ”New-AzWebAppSSLBinding” så att certifikatet laddas upp till rätt resursgrupp och plats om appen finns i en ASE.</span><span class="sxs-lookup"><span data-stu-id="576c3-529">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="576c3-530">Korrigerar ”New-AzWebAppSSLBinding” så att taggarna inte skrivs över på en bindning av ett SSL-certifikat till en app</span><span class="sxs-lookup"><span data-stu-id="576c3-530">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="576c3-531">1.1.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="576c3-531">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="576c3-532">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="576c3-532">Az.Accounts</span></span>
* <span data-ttu-id="576c3-533">Lade till omfattningen ”Lokal” till Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="576c3-533">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="576c3-534">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="576c3-534">Az.Compute</span></span>
* <span data-ttu-id="576c3-535">Namn är nu valfritt i ID-parametern för Restart/Start/Stop/Remove/Set-AzVM och Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="576c3-535">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="576c3-536">Uppdaterade beskrivningen av ID i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="576c3-536">Updated the description of ID in help files</span></span>
* <span data-ttu-id="576c3-537">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="576c3-537">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="576c3-538">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="576c3-538">Az.DataLakeStore</span></span>
* <span data-ttu-id="576c3-539">Uppdatera sdk-versionen av dataplanet till 1.1.14 för SDK-korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="576c3-539">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="576c3-540">Korrigerade hanteringen av negativ accesstime och modificationtime för getfilestatus och liststatus; korrigera asynkront annulleringstoken</span><span class="sxs-lookup"><span data-stu-id="576c3-540">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="576c3-541">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="576c3-541">Az.EventGrid</span></span>
* <span data-ttu-id="576c3-542">Uppdaterat för användning av API-versionen 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="576c3-542">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="576c3-543">Uppdaterade följande cmdletar för att stödja nytt scenario i API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="576c3-543">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="576c3-544">New-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="576c3-544">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="576c3-545">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="576c3-545">Event Time-To-Live,</span></span>
        - <span data-ttu-id="576c3-546">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="576c3-546">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="576c3-547">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="576c3-547">Dead letter endpoint.</span></span>
    - <span data-ttu-id="576c3-548">Update-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="576c3-548">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="576c3-549">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="576c3-549">Event Time-To-Live,</span></span>
        - <span data-ttu-id="576c3-550">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="576c3-550">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="576c3-551">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="576c3-551">Dead letter endpoint.</span></span>
* <span data-ttu-id="576c3-552">Lade till nya enum-värden (storageQueue och hybridConnection) för alternativet EndpointType i cmdletarna New-AzureRmEventGridSubscription och Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="576c3-552">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="576c3-553">Visa varningsmeddelanden om skapande eller uppdatering av händelseprenumerationen förväntas medföra manuell åtgärd från användaren.</span><span class="sxs-lookup"><span data-stu-id="576c3-553">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="576c3-554">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="576c3-554">Az.IotHub</span></span>
* <span data-ttu-id="576c3-555">Har uppdaterats till den senaste versionen av SDK:n lotHub</span><span class="sxs-lookup"><span data-stu-id="576c3-555">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="576c3-556">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="576c3-556">Az.LogicApp</span></span>
* <span data-ttu-id="576c3-557">Get-AzLogicApp visar en lista över alla som inte har angivet namn</span><span class="sxs-lookup"><span data-stu-id="576c3-557">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="576c3-558">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="576c3-558">Az.Resources</span></span>
* <span data-ttu-id="576c3-559">Åtgärdade problem med parameteruppsättningen när parametrarna -ODataQuery och -ResourceId anges för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="576c3-559">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="576c3-560">Mer information här: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="576c3-560">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="576c3-561">Åtgärdade hantering av parametern -Custom i New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="576c3-561">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="576c3-562">Korrigerade stavfel i New-AzDeployment-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="576c3-562">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="576c3-563">Gjorde parametern -MailNickname obligatorisk för New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="576c3-563">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="576c3-564">Mer information här: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="576c3-564">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="576c3-565">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="576c3-565">Az.SignalR</span></span>
* <span data-ttu-id="576c3-566">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="576c3-566">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="576c3-567">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="576c3-567">Az.Sql</span></span>
* <span data-ttu-id="576c3-568">Konverterade lagringshanteringsklientens beroende av den normala SDK-implementeringen.</span><span class="sxs-lookup"><span data-stu-id="576c3-568">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="576c3-569">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="576c3-569">Az.Storage</span></span>
* <span data-ttu-id="576c3-570">Angav StorageAccountName för lagringskontext som det verkliga namnet på lagringskontot när det skapas med Sas Token, OAuth eller Anonymous</span><span class="sxs-lookup"><span data-stu-id="576c3-570">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="576c3-571">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="576c3-571">New-AzStorageContext</span></span>
* <span data-ttu-id="576c3-572">Skapade Sas Token för Blob Snapshot-objekt med parametern -FullUri, åtgärdade den returnerade URI:n så att den blir URI för ögonblicksbild</span><span class="sxs-lookup"><span data-stu-id="576c3-572">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="576c3-573">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="576c3-573">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="576c3-574">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="576c3-574">Az.Websites</span></span>
* <span data-ttu-id="576c3-575">Åtgärdade en bugg i datumparsningen i Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="576c3-575">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="576c3-576">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="576c3-576">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="576c3-577">1.0.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="576c3-577">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="576c3-578">Allmänt</span><span class="sxs-lookup"><span data-stu-id="576c3-578">General</span></span>

- <span data-ttu-id="576c3-579">Allmän tillgänglighet för Az-modulen</span><span class="sxs-lookup"><span data-stu-id="576c3-579">General Availability of Az Module</span></span>
- <span data-ttu-id="576c3-580">Onlinehjälp för varje modul</span><span class="sxs-lookup"><span data-stu-id="576c3-580">Online help for each module</span></span>
- <span data-ttu-id="576c3-581">Mer information och en översikt finns på [Az-informationssidan](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="576c3-581">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="576c3-582">Information om hur du migrerar från AzureRM finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="576c3-582">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="576c3-583">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="576c3-583">Az.Accounts</span></span>
- <span data-ttu-id="576c3-584">Har ändrats från Az.Profile</span><span class="sxs-lookup"><span data-stu-id="576c3-584">Changed from Az.Profile</span></span>
- <span data-ttu-id="576c3-585">Fasta tabellformat för profil- och kontexttyper</span><span class="sxs-lookup"><span data-stu-id="576c3-585">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="576c3-586">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="576c3-586">Az.ApiManagement</span></span>
- <span data-ttu-id="576c3-587">Korrigeringar för #7002</span><span class="sxs-lookup"><span data-stu-id="576c3-587">Fixes for #7002</span></span>
- <span data-ttu-id="576c3-588">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="576c3-588">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="576c3-589">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="576c3-589">Az.Batch</span></span>
- <span data-ttu-id="576c3-590">Lade till möjligheten att se vilken version av Azure Batch Node Agent som körs på var och en av de virtuella datorerna i en pool, via den nya egenskapen `NodeAgentInformation` på `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="576c3-590">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="576c3-591">Standarden `Caching` för `PSDataDisk` är nu `ReadWrite` i stället för `None`.</span><span class="sxs-lookup"><span data-stu-id="576c3-591">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="576c3-592">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="576c3-592">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="576c3-593">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="576c3-593">Az.Billing</span></span>
- <span data-ttu-id="576c3-594">Kombinerar cmdletarna för fakturering, förbrukning och UsageAggregates. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="576c3-594">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="576c3-595">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="576c3-595">Az.CognitivServices</span></span>
- <span data-ttu-id="576c3-596">Lade till kompletterare för SkuName och Typem som är tillgängliga i New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="576c3-596">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="576c3-597">Tog bort parameteruppsättningen GetSkusWithAccountParamSetName från Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="576c3-597">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="576c3-598">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="576c3-598">Az.ContainerInstance</span></span>
- <span data-ttu-id="576c3-599">Stöd för ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="576c3-599">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="576c3-600">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="576c3-600">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="576c3-601">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="576c3-601">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="576c3-602">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="576c3-602">Az.DataLakeStore</span></span>
- <span data-ttu-id="576c3-603">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="576c3-603">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="576c3-604">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="576c3-604">Az.Monitor</span></span>
- <span data-ttu-id="576c3-605">Döpte om Az.Insights till Az.Monitor och andra mindre icke-bakåtkompatibla ändringar. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="576c3-605">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="576c3-606">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="576c3-606">Az.KeyVault</span></span>
- <span data-ttu-id="576c3-607">Tog bort den inaktuella egenskapen PurgeDisabled från utdatatyper</span><span class="sxs-lookup"><span data-stu-id="576c3-607">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="576c3-608">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="576c3-608">Az.MachineLearning</span></span>
- <span data-ttu-id="576c3-609">Inkluderade cmdletarna från modulen Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="576c3-609">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="576c3-610">Az.Media</span><span class="sxs-lookup"><span data-stu-id="576c3-610">Az.Media</span></span>
- <span data-ttu-id="576c3-611">Tog bort inaktuella -Tags-alias från New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="576c3-611">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="576c3-612">Az.Network</span><span class="sxs-lookup"><span data-stu-id="576c3-612">Az.Network</span></span>
<span data-ttu-id="576c3-613">Stöd har lagts till för konfiguration av RewriteRuleSets i Application Gateway</span><span class="sxs-lookup"><span data-stu-id="576c3-613">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="576c3-614">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="576c3-614">New cmdlets added:</span></span>
        - <span data-ttu-id="576c3-615">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="576c3-615">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="576c3-616">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="576c3-616">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="576c3-617">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="576c3-617">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="576c3-618">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="576c3-618">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="576c3-619">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="576c3-619">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="576c3-620">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="576c3-620">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="576c3-621">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="576c3-621">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="576c3-622">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="576c3-622">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="576c3-623">Cmdletar har uppdaterats med den valfria parametern -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="576c3-623">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="576c3-624">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="576c3-624">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="576c3-625">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="576c3-625">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="576c3-626">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="576c3-626">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="576c3-627">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="576c3-627">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="576c3-628">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="576c3-628">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="576c3-629">New-AzureRmApplicationGatewayUrlPathMapConfig har lagt till KeyVault-stöd för Application Gateway med Identity.</span><span class="sxs-lookup"><span data-stu-id="576c3-629">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="576c3-630">Cmdletar har uppdaterats med den valfria parametern -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="576c3-630">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="576c3-631">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="576c3-631">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="576c3-632">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="576c3-632">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="576c3-633">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="576c3-633">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="576c3-634">Cmdleten New-AzApplicationGateway har uppdaterats med den valfria parametern -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="576c3-634">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="576c3-635">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="576c3-635">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="576c3-636">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="576c3-636">Az.OperationalInsights</span></span>
- <span data-ttu-id="576c3-637">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="576c3-637">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="576c3-638">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="576c3-638">Az.Profile</span></span>
- <span data-ttu-id="576c3-639">Modulnamnet har ändrats till Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="576c3-639">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="576c3-640">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="576c3-640">Az.RecoveryServices</span></span>
- <span data-ttu-id="576c3-641">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="576c3-641">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="576c3-642">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="576c3-642">Az.Resources</span></span>
- <span data-ttu-id="576c3-643">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="576c3-643">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="576c3-644">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="576c3-644">Az.ServiceFabric</span></span>
- <span data-ttu-id="576c3-645">Stöd för specificering av certifikat efter eget namn och tumavtryck</span><span class="sxs-lookup"><span data-stu-id="576c3-645">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="576c3-646">Information om fler icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="576c3-646">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="576c3-647">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="576c3-647">Az.SIgnalR</span></span>
- <span data-ttu-id="576c3-648">Allmän tillgänglighet för PowerShell-cmdletar för SIgnalR</span><span class="sxs-lookup"><span data-stu-id="576c3-648">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="576c3-649">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="576c3-649">Az.Sql</span></span>
- <span data-ttu-id="576c3-650">Lade till de nya identifieringstyperna Data_Exfiltration och Unsafe_Action i Threat Detection-cmdletar</span><span class="sxs-lookup"><span data-stu-id="576c3-650">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="576c3-651">Uppdaterade dokumentationsexempel för Sql Auditing-cmdletar</span><span class="sxs-lookup"><span data-stu-id="576c3-651">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="576c3-652">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="576c3-652">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="576c3-653">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="576c3-653">Az.Storage</span></span>
- <span data-ttu-id="576c3-654">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="576c3-654">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="576c3-655">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="576c3-655">Az.Websites</span></span>
- <span data-ttu-id="576c3-656">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="576c3-656">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="576c3-657">0.7.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="576c3-657">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="576c3-658">Allmänt</span><span class="sxs-lookup"><span data-stu-id="576c3-658">General</span></span>

* <span data-ttu-id="576c3-659">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="576c3-659">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="576c3-660">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="576c3-660">Az.Compute</span></span>

* <span data-ttu-id="576c3-661">Lade till stöd för UltraSSD och Galleriavbildningar i de enkla parameteruppsättningarna för `New-AzVm(ss)`-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="576c3-661">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="576c3-662">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="576c3-662">Az.DataLakeStore</span></span>

* <span data-ttu-id="576c3-663">Åtgärdade avslutande snedstreck i domänen för adls-konto</span><span class="sxs-lookup"><span data-stu-id="576c3-663">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="576c3-664">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="576c3-664">Az.FrontDoor</span></span>

* <span data-ttu-id="576c3-665">Brutna länkar korrigerades</span><span class="sxs-lookup"><span data-stu-id="576c3-665">Fixed some broken links</span></span>
    - <span data-ttu-id="576c3-666">I artiklarna New-AzureRmFrontDoor och Set-AzureRmFrontDoor artiklar korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="576c3-666">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="576c3-667">I artikeln New-AzureRmFrontDoorManagedRuleObject korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="576c3-667">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="576c3-668">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="576c3-668">Az.RecoveryServices</span></span>

* <span data-ttu-id="576c3-669">Lade till valideringar på klientsidan för Azure-filresurs med återställningsåtgärder.</span><span class="sxs-lookup"><span data-stu-id="576c3-669">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="576c3-670">Gjorde storageAccountName och storageAccountResourceGroupName valfritt för afs-återställning.</span><span class="sxs-lookup"><span data-stu-id="576c3-670">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="576c3-671">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="576c3-671">Az.Resources</span></span>

* <span data-ttu-id="576c3-672">Korrigering för https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="576c3-672">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="576c3-673">Uppdaterade Get-AzureRmRoleAssignment så att prenumerationsomfattningen används om den anges vid begäran om klassiska administratörer.</span><span class="sxs-lookup"><span data-stu-id="576c3-673">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="576c3-674">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="576c3-674">Az.Sql</span></span>

* <span data-ttu-id="576c3-675">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="576c3-675">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="576c3-676">Korrigerade ett problem med Get-AzureRmSqlDatabaseVulnerabilityAssessment med DotNet-kärna</span><span class="sxs-lookup"><span data-stu-id="576c3-676">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="576c3-677">Ändrade dokumentationen för hjälpmeddelanden som rör SQL Auditing-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="576c3-677">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="576c3-678">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="576c3-678">Az.Storage</span></span>

* <span data-ttu-id="576c3-679">Lade till -EnableHierarchicalNamespace i New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="576c3-679">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="576c3-680">Åtgärdade problemet med att cmdleten Copy File inte kunde återanvända källkontexten på målet om inte -DestContext angetts</span><span class="sxs-lookup"><span data-stu-id="576c3-680">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="576c3-681">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="576c3-681">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="576c3-682">Stöd för statisk webbplatskonfiguration</span><span class="sxs-lookup"><span data-stu-id="576c3-682">Support Static Website configuration</span></span>
    - <span data-ttu-id="576c3-683">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="576c3-683">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="576c3-684">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="576c3-684">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="576c3-685">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="576c3-685">Az.Websites</span></span>

* <span data-ttu-id="576c3-686">Set-AzureRmWebApp och Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="576c3-686">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="576c3-687">Ny parameter (-AzureStoragePath) har lagts till för att ange att Azure Storage-sökvägar ska monteras i containerappar i Windows och Linux.</span><span class="sxs-lookup"><span data-stu-id="576c3-687">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="576c3-688">Använder utdata från den nya cmdleten New-AzureRmWebAppAzureStoragePath som en parameter för att ange sökvägar för Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="576c3-688">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="576c3-689">0.6.1 – november 2018</span><span class="sxs-lookup"><span data-stu-id="576c3-689">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="576c3-690">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="576c3-690">Az.ApiManagement</span></span>
* <span data-ttu-id="576c3-691">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="576c3-691">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="576c3-692">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="576c3-692">Az.Automation</span></span>
* <span data-ttu-id="576c3-693">Swagger baserade Azure Automation-cmdletar</span><span class="sxs-lookup"><span data-stu-id="576c3-693">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="576c3-694">Cmdletar för Uppdateringshantering har lagts till</span><span class="sxs-lookup"><span data-stu-id="576c3-694">Added Update Management cmdlets</span></span>
* <span data-ttu-id="576c3-695">Cmdletar för källkontroll har lagts till</span><span class="sxs-lookup"><span data-stu-id="576c3-695">Added Source Control cmdlets</span></span>
* <span data-ttu-id="576c3-696">Remove-AzureRmAutomationHybridWorkerGroup-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="576c3-696">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="576c3-697">Kommandot för DSC-registreringsnod har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="576c3-697">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="576c3-698">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="576c3-698">Az.Compute</span></span>
* <span data-ttu-id="576c3-699">Problem med SystemAssigned-identitet har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="576c3-699">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="576c3-700">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="576c3-700">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="576c3-701">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="576c3-701">Az.ContainerInstance</span></span>
* <span data-ttu-id="576c3-702">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="576c3-702">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="576c3-703">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="576c3-703">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="576c3-704">uppdatera exempelbeskrivningen för marketplace-cmdletar</span><span class="sxs-lookup"><span data-stu-id="576c3-704">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="576c3-705">Az.Network</span><span class="sxs-lookup"><span data-stu-id="576c3-705">Az.Network</span></span>
* <span data-ttu-id="576c3-706">Cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomErreller Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="576c3-706">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="576c3-707">ICMP tillbaka till stöd för Azure Firewall-nätverksprotokoll har lagts till</span><span class="sxs-lookup"><span data-stu-id="576c3-707">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="576c3-708">Uppdatera cmdlet Test-AzureRmNetworkWatcherConnectivity, lägga till verifiering av mål-id, adress och port.</span><span class="sxs-lookup"><span data-stu-id="576c3-708">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="576c3-709">Åtgärda problem med minnesanvändning i VirtualNetwork-karta</span><span class="sxs-lookup"><span data-stu-id="576c3-709">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="576c3-710">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="576c3-710">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="576c3-711">Åtgärda för att ändra principen för en skyddad fildelning.</span><span class="sxs-lookup"><span data-stu-id="576c3-711">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="576c3-712">Tidszonsprincipen har konverterats till versaler.</span><span class="sxs-lookup"><span data-stu-id="576c3-712">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="576c3-713">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="576c3-713">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="576c3-714">Exempel i New-AzureRmRecoveryServicesAsrProtectableItem har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="576c3-714">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="576c3-715">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="576c3-715">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="576c3-716">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="576c3-716">Az.Relay</span></span>
* <span data-ttu-id="576c3-717">Valfri parameter -KeyValue till New-AzureRmRelayKey cmdlet har lagts till, vilket gör det möjligt för användare att tillhandahålla KeyValue.</span><span class="sxs-lookup"><span data-stu-id="576c3-717">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="576c3-718">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="576c3-718">Az.Resources</span></span>
* <span data-ttu-id="576c3-719">Uppdatera hjälpdokumentation för resursidentitet kopplad till parametrar i `New-AzureRmPolicyAssignment` och `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="576c3-719">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="576c3-720">Lägg till ett exempel för New-AzureRmPolicyDefinition som använder -Metadata</span><span class="sxs-lookup"><span data-stu-id="576c3-720">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="576c3-721">Korrigera så att skiftläge behålls i taggnycklar i NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="576c3-721">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="576c3-722">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="576c3-722">Az.ServiceFabric</span></span>
* <span data-ttu-id="576c3-723">Lägg till utfasningsmeddelanden för kommande icke-kompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="576c3-723">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="576c3-724">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="576c3-724">Az.Sql</span></span>
* <span data-ttu-id="576c3-725">Nya cmdletar för CRUD-åtgärder på Azure Sql Database-hanterad instans och Azure Sql-hanterad databas</span><span class="sxs-lookup"><span data-stu-id="576c3-725">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="576c3-726">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="576c3-726">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="576c3-727">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="576c3-727">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="576c3-728">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="576c3-728">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="576c3-729">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="576c3-729">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="576c3-730">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="576c3-730">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="576c3-731">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="576c3-731">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="576c3-732">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="576c3-732">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="576c3-733">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="576c3-733">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="576c3-734">Hantering av utökad granskningsprincip på en server eller en databas har aktiverats.</span><span class="sxs-lookup"><span data-stu-id="576c3-734">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="576c3-735">Ny parameter (PredicateExpression) har lagts till för att aktivera filtrering av granskningsloggar.</span><span class="sxs-lookup"><span data-stu-id="576c3-735">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="576c3-736">Cmdletar har ändrats så att de använder SQL-klienter i stället för äldre klienter.</span><span class="sxs-lookup"><span data-stu-id="576c3-736">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="576c3-737">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="576c3-737">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="576c3-738">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="576c3-738">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="576c3-739">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="576c3-739">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="576c3-740">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="576c3-740">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="576c3-741">Problem med att använda Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings med lagringskontots namnparameter har korrigerats</span><span class="sxs-lookup"><span data-stu-id="576c3-741">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="576c3-742">0.5.0 – november 2018</span><span class="sxs-lookup"><span data-stu-id="576c3-742">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="576c3-743">Allmänt</span><span class="sxs-lookup"><span data-stu-id="576c3-743">General</span></span>
* <span data-ttu-id="576c3-744">Lade till resurskompletterare till många kärn-cmdletar – dessa gör att du kan stega genom befintliga resursnamn med TABB vid interaktiva anrop till cmdletar</span><span class="sxs-lookup"><span data-stu-id="576c3-744">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="576c3-745">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="576c3-745">Az.Profile</span></span>
* <span data-ttu-id="576c3-746">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="576c3-746">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="576c3-747">Bytte namn på parametern TenantId i cmdleten Connect-AzAccount till Tenant och lade till ett alias för TenantId</span><span class="sxs-lookup"><span data-stu-id="576c3-747">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="576c3-748">Uppdaterade TenantId-beskrivningen för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="576c3-748">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="576c3-749">Åtgärda felmeddelande för misslyckad inloggning när du tillhandahåller klientdomän</span><span class="sxs-lookup"><span data-stu-id="576c3-749">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="576c3-750">Åtgärda problem med att kontextnamn hamnar i konflikt för konton utan prenumerationer i klientorganisationen</span><span class="sxs-lookup"><span data-stu-id="576c3-750">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="576c3-751">Åtgärda problem med DataLake-slutpunkter vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="576c3-751">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="576c3-752">Åtgärdade problem med att Disconnect-AzAccount kastades om den inte anslöts</span><span class="sxs-lookup"><span data-stu-id="576c3-752">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="576c3-753">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="576c3-753">Az.CognitiveServices</span></span>
* <span data-ttu-id="576c3-754">Lade till åtgärden Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="576c3-754">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="576c3-755">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="576c3-755">Az.Compute</span></span>
* <span data-ttu-id="576c3-756">Lade till cmdletarna Add-AzVmssVMDataDisk och Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="576c3-756">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="576c3-757">Get-AzVMImage visar AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="576c3-757">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="576c3-758">Åtgärdade att värdena för alternativen SetAzVMChefExtension -BootstrapOptions och -JsonAttribute inte angavs i json-format.</span><span class="sxs-lookup"><span data-stu-id="576c3-758">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="576c3-759">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="576c3-759">Az.DataLakeStore</span></span>
* <span data-ttu-id="576c3-760">Uppdatera DataLake-paketet till 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="576c3-760">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="576c3-761">Lägg till standardsamtidighet för flertrådade åtgärder.</span><span class="sxs-lookup"><span data-stu-id="576c3-761">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="576c3-762">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="576c3-762">Az.Insights</span></span>
* <span data-ttu-id="576c3-763">Åtgärdade problem #7267 (autoskalningsområde)</span><span class="sxs-lookup"><span data-stu-id="576c3-763">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="576c3-764">Problem med att uppräknade parametrar inte ställdes in ordentligt när du skapade en ny autoskalningsregel (de ställdes alltid in med standardvärdet).</span><span class="sxs-lookup"><span data-stu-id="576c3-764">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="576c3-765">Åtgärdade problem #7513 [Insights] Set-AzDiagnosticSetting kräver uttrycklig specifikation av kategorier när inställningar skapas</span><span class="sxs-lookup"><span data-stu-id="576c3-765">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="576c3-766">Nu kräver inte cmdleten uttrycklig anvisning av kategorierna för att aktiveras under skapande, d.v.s. den fungerar enligt beskrivning</span><span class="sxs-lookup"><span data-stu-id="576c3-766">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="576c3-767">Az.Network</span><span class="sxs-lookup"><span data-stu-id="576c3-767">Az.Network</span></span>
* <span data-ttu-id="576c3-768">PeeringType ändrades till en obligatorisk parameter för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="576c3-768">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="576c3-769">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="576c3-769">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="576c3-770">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="576c3-770">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="576c3-771">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="576c3-771">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="576c3-772">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="576c3-772">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="576c3-773">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="576c3-773">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="576c3-774">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="576c3-774">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="576c3-775">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="576c3-775">Az.PolicyInsights</span></span>
* <span data-ttu-id="576c3-776">Cmdletar för principreparation har lagts till</span><span class="sxs-lookup"><span data-stu-id="576c3-776">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="576c3-777">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="576c3-777">Az.Resources</span></span>
* <span data-ttu-id="576c3-778">Korrigering för https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="576c3-778">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="576c3-779">Tillåt att resurser listas med parametern -ResourceId för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="576c3-779">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="576c3-780">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="576c3-780">Az.ServiceBus</span></span>
* <span data-ttu-id="576c3-781">Skrivskyddad MigrationState-egenskap har lagts till i PSServiceBusMigrationConfigurationAttributes, som hjälper till att hålla koll på migreringstillståndet.</span><span class="sxs-lookup"><span data-stu-id="576c3-781">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="576c3-782">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="576c3-782">Az.ServiceFabric</span></span>
* <span data-ttu-id="576c3-783">Åtgärda att lägga till certifikat till Linux-Vmss.</span><span class="sxs-lookup"><span data-stu-id="576c3-783">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="576c3-784">Åtgärdade Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="576c3-784">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="576c3-785">Använd rätt tumavtryck från nya certifikat (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="576c3-785">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="576c3-786">Visa undantag korrekt (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="576c3-786">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="576c3-787">Åtgärdade Update-AzServiceFabricDurability så att klusterkonfigurationen uppdateras innan Vmss-åtgärden CreateOrUpdate påbörjas.</span><span class="sxs-lookup"><span data-stu-id="576c3-787">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="576c3-788">0.4.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="576c3-788">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="576c3-789">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="576c3-789">Az.Profile</span></span>
* <span data-ttu-id="576c3-790">Åtgärdade problemet med Get-AzSubscription i CloudShell</span><span class="sxs-lookup"><span data-stu-id="576c3-790">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="576c3-791">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="576c3-791">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="576c3-792">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="576c3-792">Az.Compute</span></span>
* <span data-ttu-id="576c3-793">Nya storlekar lades till i listan över godkända VM-storlekar för vilka accelererat nätverk kommer att aktiveras vid användning av den enkla parameteruppsättningen för New-AzVm</span><span class="sxs-lookup"><span data-stu-id="576c3-793">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="576c3-794">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="576c3-794">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="576c3-795">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="576c3-795">Az.DataLakeStore</span></span>
* <span data-ttu-id="576c3-796">Lägger till stöd för regler för virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="576c3-796">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="576c3-797">Get-AzDataLakeStoreVirtualNetworkRule: Hämtar eller listar regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="576c3-797">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="576c3-798">Add-AzDataLakeStoreVirtualNetworkRule: Lägger till en regel för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="576c3-798">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="576c3-799">Set-AzDataLakeStoreVirtualNetworkRule: Ändrar den angivna regeln för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="576c3-799">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="576c3-800">Remove-AzDataLakeStoreVirtualNetworkRule: Tar bort en regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="576c3-800">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="576c3-801">Az.Network</span><span class="sxs-lookup"><span data-stu-id="576c3-801">Az.Network</span></span>
* <span data-ttu-id="576c3-802">Skicka protokollvärdet till serverdelen för att uppdatera cmdleten Test-AzNetworkWatcherConnectivity.</span><span class="sxs-lookup"><span data-stu-id="576c3-802">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="576c3-803">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="576c3-803">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="576c3-804">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="576c3-804">Az.Resources</span></span>
* <span data-ttu-id="576c3-805">Åtgärdade problem där Get-AzRoleDefinition genererar ett oläsligt undantag (när standardprofilen inte innehåller någon prenumeration och ingen omfattning har angetts) genom att lägga till ett beskrivande undantag i scenariot.</span><span class="sxs-lookup"><span data-stu-id="576c3-805">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="576c3-806">Ställ in ”RoleDefinitionNameParameterSet” som standardparameteruppsättning.</span><span class="sxs-lookup"><span data-stu-id="576c3-806">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="576c3-807">0.3.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="576c3-807">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="576c3-808">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="576c3-808">Azure.Storage</span></span>
* <span data-ttu-id="576c3-809">Åtgärda fel där Kopiera blob/fil inte kopierar metadata när målplatsen har ett problem med metadata</span><span class="sxs-lookup"><span data-stu-id="576c3-809">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="576c3-810">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="576c3-810">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="576c3-811">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="576c3-811">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="576c3-812">Stöd för att hämta användningsinformation om en Storage-resurs för en specifik plats och för att lägga till ett varningsmeddelande för att hämta användningsinformation om en global Storage-resurs är inaktuellt.</span><span class="sxs-lookup"><span data-stu-id="576c3-812">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="576c3-813">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="576c3-813">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="576c3-814">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="576c3-814">Az.CognitiveServices</span></span>
* <span data-ttu-id="576c3-815">Stöd för Get-AzCognitiveServicesAccountSkus utan ett befintligt konto.</span><span class="sxs-lookup"><span data-stu-id="576c3-815">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="576c3-816">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="576c3-816">Az.Compute</span></span>
* <span data-ttu-id="576c3-817">Åtgärdade fel där Get-AzVM -ResourceGroupName <rg> returnerar fler än 50 resultat om det behövs</span><span class="sxs-lookup"><span data-stu-id="576c3-817">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="576c3-818">Lade till ett exempel för SimpleParameterSet i hjälpen för cmdleten New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="576c3-818">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="576c3-819">Ett stavfel i förloppsmeddelandet för Azure Disk Encryption har korrigerats</span><span class="sxs-lookup"><span data-stu-id="576c3-819">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="576c3-820">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="576c3-820">Az.DataFactoryV2</span></span>
* <span data-ttu-id="576c3-821">ADF .Net SDK-versionen har uppdaterats till 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="576c3-821">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="576c3-822">Az.Network</span><span class="sxs-lookup"><span data-stu-id="576c3-822">Az.Network</span></span>
* <span data-ttu-id="576c3-823">Funktionalitet för NetworkProfile har lagts till.</span><span class="sxs-lookup"><span data-stu-id="576c3-823">Added NetworkProfile functionality.</span></span> <span data-ttu-id="576c3-824">nya cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="576c3-824">new cmdlets added</span></span>
    - <span data-ttu-id="576c3-825">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="576c3-825">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="576c3-826">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="576c3-826">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="576c3-827">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="576c3-827">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="576c3-828">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="576c3-828">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="576c3-829">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="576c3-829">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="576c3-830">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="576c3-830">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="576c3-831">Länk för tjänstassociering på modell för undernät har lagts till</span><span class="sxs-lookup"><span data-stu-id="576c3-831">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="576c3-832">Cmdletarna New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap och Remove-AzVirtualNetworkTap har lagts till</span><span class="sxs-lookup"><span data-stu-id="576c3-832">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="576c3-833">Cmdletarna Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig och Remove-AzNEtworkInterfaceTapConfig har lagts till</span><span class="sxs-lookup"><span data-stu-id="576c3-833">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="576c3-834">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="576c3-834">Az.RedisCache</span></span>
* <span data-ttu-id="576c3-835">Tillåt att alla strängar används som storleksparametrar framöver.</span><span class="sxs-lookup"><span data-stu-id="576c3-835">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="576c3-836">Lägg till P5 i popup-fönstret PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="576c3-836">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="576c3-837">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="576c3-837">Az.Resources</span></span>
* <span data-ttu-id="576c3-838">Parametern -Mode som saknades i Set-AzPolicyDefinition har lagts till</span><span class="sxs-lookup"><span data-stu-id="576c3-838">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="576c3-839">Åtgärdade buggen för cmdleten Get-AzProviderOperation för åtgärder med ursprung som innehåller användare</span><span class="sxs-lookup"><span data-stu-id="576c3-839">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="576c3-840">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="576c3-840">Az.Sql</span></span>
* <span data-ttu-id="576c3-841">Ett problem där vissa cmdletar för säkerhetskopiering inte kunde identifiera den aktuella azure-prenumerationen har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="576c3-841">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="576c3-842">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="576c3-842">Az.Websites</span></span>
* <span data-ttu-id="576c3-843">Ny cmdlet: Get-AzWebAppContainerContinuousDeploymentUrl – Hämtar webhook-URL:en för kontinuerlig distribution av container</span><span class="sxs-lookup"><span data-stu-id="576c3-843">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="576c3-844">Nya cmdletar: New-AzWebAppContainerPSSession och Enter-WebAppContainerPSSession – Startar en PowerShell-fjärrsession i en containerapp för windows</span><span class="sxs-lookup"><span data-stu-id="576c3-844">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="576c3-845">0.2.0 – september 2018</span><span class="sxs-lookup"><span data-stu-id="576c3-845">0.2.0 - September 2018</span></span>
 <span data-ttu-id="576c3-846">Första versionen</span><span class="sxs-lookup"><span data-stu-id="576c3-846">Initial Release</span></span>