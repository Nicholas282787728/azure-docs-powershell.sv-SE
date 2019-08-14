---
ms.openlocfilehash: faf9313d642a3ca45731f4527aafdfd7f5096a78
ms.sourcegitcommit: b02cbcd00748a4a9a4790a5fba229ce53c3bf973
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/09/2019
ms.locfileid: "68861272"
---
## <a name="180---april-2019"></a><span data-ttu-id="c3c75-101">1.8.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="c3c75-101">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="c3c75-102">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="c3c75-102">Highlights since the last major release</span></span>
* <span data-ttu-id="c3c75-103">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="c3c75-103">General availability of `Az` module</span></span>
* <span data-ttu-id="c3c75-104">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="c3c75-104">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="c3c75-105">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="c3c75-105">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="c3c75-106">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="c3c75-106">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="c3c75-107">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="c3c75-107">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="c3c75-108">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="c3c75-108">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="c3c75-109">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="c3c75-109">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="c3c75-110">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c3c75-110">Az.Accounts</span></span>
* <span data-ttu-id="c3c75-111">Uppdatera Uninstall-AzureRm för att ta bort moduler i Mac på ett korrekt sätt</span><span class="sxs-lookup"><span data-stu-id="c3c75-111">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="c3c75-112">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="c3c75-112">Az.Batch</span></span>
* <span data-ttu-id="c3c75-113">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="c3c75-113">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="c3c75-114">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="c3c75-114">Az.Cdn</span></span>
* <span data-ttu-id="c3c75-115">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="c3c75-115">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="c3c75-116">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="c3c75-116">Az.CognitiveServices</span></span>
* <span data-ttu-id="c3c75-117">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="c3c75-117">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c3c75-118">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c3c75-118">Az.Compute</span></span>
* <span data-ttu-id="c3c75-119">Åtgärda problem med AEM-installationen om resurs-ID:n för diskar innehåller resourcegroups i gemener i resurs-ID:n</span><span class="sxs-lookup"><span data-stu-id="c3c75-119">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="c3c75-120">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="c3c75-120">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="c3c75-121">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="c3c75-121">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="c3c75-122">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c3c75-122">Az.DataFactory</span></span>
* <span data-ttu-id="c3c75-123">Lägg till SsisProperties om NodeCount inte är null för hanterad integreringskörning.</span><span class="sxs-lookup"><span data-stu-id="c3c75-123">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="c3c75-124">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c3c75-124">Az.DataLakeStore</span></span>
* <span data-ttu-id="c3c75-125">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="c3c75-125">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="c3c75-126">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="c3c75-126">Az.EventGrid</span></span>
* <span data-ttu-id="c3c75-127">Hjälptexten för slutpunkten har uppdaterats för att visa att resurser ska skapas innan cmdletarna för att skapa/uppdatera händelseprenumerationer används.</span><span class="sxs-lookup"><span data-stu-id="c3c75-127">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="c3c75-128">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="c3c75-128">Az.EventHub</span></span>
* <span data-ttu-id="c3c75-129">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="c3c75-129">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="c3c75-130">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="c3c75-130">Az.HDInsight</span></span>
* <span data-ttu-id="c3c75-131">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="c3c75-131">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="c3c75-132">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="c3c75-132">Az.IotHub</span></span>
* <span data-ttu-id="c3c75-133">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="c3c75-133">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="c3c75-134">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c3c75-134">Az.KeyVault</span></span>
* <span data-ttu-id="c3c75-135">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="c3c75-135">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="c3c75-136">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="c3c75-136">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="c3c75-137">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="c3c75-137">Az.MachineLearning</span></span>
* <span data-ttu-id="c3c75-138">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="c3c75-138">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="c3c75-139">Az.Media</span><span class="sxs-lookup"><span data-stu-id="c3c75-139">Az.Media</span></span>
* <span data-ttu-id="c3c75-140">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="c3c75-140">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="c3c75-141">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="c3c75-141">Az.Monitor</span></span>
  * <span data-ttu-id="c3c75-142">Nya cmdletar för måttbaserad aviseringsregel i GenV2 (inte klassisk)</span><span class="sxs-lookup"><span data-stu-id="c3c75-142">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="c3c75-143">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="c3c75-143">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="c3c75-144">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="c3c75-144">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="c3c75-145">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="c3c75-145">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="c3c75-146">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="c3c75-146">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="c3c75-147">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="c3c75-147">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="c3c75-148">Monitor SDK har uppdaterats till version 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="c3c75-148">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c3c75-149">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c3c75-149">Az.Network</span></span>
* <span data-ttu-id="c3c75-150">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="c3c75-150">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="c3c75-151">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="c3c75-151">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="c3c75-152">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="c3c75-152">Az.NotificationHubs</span></span>
* <span data-ttu-id="c3c75-153">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="c3c75-153">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="c3c75-154">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="c3c75-154">Az.OperationalInsights</span></span>
* <span data-ttu-id="c3c75-155">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="c3c75-155">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="c3c75-156">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="c3c75-156">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="c3c75-157">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="c3c75-157">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c3c75-158">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c3c75-158">Az.RecoveryServices</span></span>
* <span data-ttu-id="c3c75-159">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="c3c75-159">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="c3c75-160">Tabellformatet för SQL i virtuella Azure-datorer har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="c3c75-160">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="c3c75-161">En alternativ metod för att hämta platser i AzureFileShare har lagts till</span><span class="sxs-lookup"><span data-stu-id="c3c75-161">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="c3c75-162">ScheduleRunDays i SchedulePolicy-objekt har uppdaterats enligt tidszon</span><span class="sxs-lookup"><span data-stu-id="c3c75-162">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="c3c75-163">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="c3c75-163">Az.RedisCache</span></span>
* <span data-ttu-id="c3c75-164">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="c3c75-164">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="c3c75-165">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c3c75-165">Az.Resources</span></span>
* <span data-ttu-id="c3c75-166">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="c3c75-166">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="c3c75-167">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c3c75-167">Az.Sql</span></span>
* <span data-ttu-id="c3c75-168">Ersätt Monitor SDK-beroende med vanlig kod</span><span class="sxs-lookup"><span data-stu-id="c3c75-168">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="c3c75-169">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="c3c75-169">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="c3c75-170">Förbättrad process för klassificering av flera kolumner.</span><span class="sxs-lookup"><span data-stu-id="c3c75-170">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="c3c75-171">Inkludera SKU-egenskaper (SKU-namn, serie, kapacitet) i svaret från Get-AzSqlServerServiceObjective och formatera som tabell som standard.</span><span class="sxs-lookup"><span data-stu-id="c3c75-171">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="c3c75-172">Möjlighet att använda Get-AzSqlServerServiceObjective efter plats utan att behöva en redan befintlig server i regionen.</span><span class="sxs-lookup"><span data-stu-id="c3c75-172">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="c3c75-173">Stöd för tidszonsparametern när hanterade instanser skapas.</span><span class="sxs-lookup"><span data-stu-id="c3c75-173">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="c3c75-174">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="c3c75-174">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c3c75-175">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c3c75-175">Az.Websites</span></span>
* <span data-ttu-id="c3c75-176">åtgärdar Set-AzWebApp och Set-AzWebAppSlot så att de inte tar bort taggar vid körning</span><span class="sxs-lookup"><span data-stu-id="c3c75-176">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="c3c75-177">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="c3c75-177">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="c3c75-178">SDK för WebSites har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="c3c75-178">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="c3c75-179">Egenskapen AdminSiteName har tagits bort från PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="c3c75-179">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="c3c75-180">1.7.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="c3c75-180">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="c3c75-181">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="c3c75-181">Highlights since the last major release</span></span>
* <span data-ttu-id="c3c75-182">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="c3c75-182">General availability of `Az` module</span></span>
* <span data-ttu-id="c3c75-183">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="c3c75-183">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="c3c75-184">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="c3c75-184">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="c3c75-185">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="c3c75-185">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="c3c75-186">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="c3c75-186">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="c3c75-187">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="c3c75-187">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="c3c75-188">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="c3c75-188">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="c3c75-189">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c3c75-189">Az.Accounts</span></span>
* <span data-ttu-id="c3c75-190">Add-AzEnvironment och Set-AzEnvironment har uppdaterats för att godkänna parametern AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="c3c75-190">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="c3c75-191">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="c3c75-191">Az.AnalysisServices</span></span>
* <span data-ttu-id="c3c75-192">ServiceClient används i cmdletar för dataplan och den ursprungliga autentiseringslogiken har tagits bort</span><span class="sxs-lookup"><span data-stu-id="c3c75-192">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="c3c75-193">Add-AzureASAccount används för omslutning av Connect-AzAccount för att undvika en icke-bakåtkompatibel ändring</span><span class="sxs-lookup"><span data-stu-id="c3c75-193">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="c3c75-194">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c3c75-194">Az.Automation</span></span>
* <span data-ttu-id="c3c75-195">Buggen för cmdleten New-AzAutomationSoftwareUpdateConfiguration för inkluderingar har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="c3c75-195">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="c3c75-196">Nu bör parametern IncludedKbNumber och IncludedPackageNameMask fungera.</span><span class="sxs-lookup"><span data-stu-id="c3c75-196">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="c3c75-197">Felkorrigering för dynamiska grupper i uppdateringshanteringen för azure automation</span><span class="sxs-lookup"><span data-stu-id="c3c75-197">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c3c75-198">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c3c75-198">Az.Compute</span></span>
* <span data-ttu-id="c3c75-199">Lägg till parametern HyperVGeneration i New-AzDiskConfig och New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="c3c75-199">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="c3c75-200">Tillåt att virtuella datorer skapas med galleribilder från andra klientorganisationer.</span><span class="sxs-lookup"><span data-stu-id="c3c75-200">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="c3c75-201">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="c3c75-201">Az.ContainerInstance</span></span>
* <span data-ttu-id="c3c75-202">Ett problem har åtgärdats i parametern -Command för New-AzContainerGroup som lade till ett avslutande tomt argument</span><span class="sxs-lookup"><span data-stu-id="c3c75-202">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="c3c75-203">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c3c75-203">Az.DataFactory</span></span>
* <span data-ttu-id="c3c75-204">ADF .Net SDK-versionen har uppdaterats till 3.0.2</span><span class="sxs-lookup"><span data-stu-id="c3c75-204">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="c3c75-205">Cmdleten Set-AzDataFactoryV2 har uppdaterats med extra parametrar för inställningar som rör RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="c3c75-205">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="c3c75-206">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c3c75-206">Az.Resources</span></span>
* <span data-ttu-id="c3c75-207">Förbättra hanteringen av providrar för Get-AzResource när parametrarna -ResourceId eller -ResourceGroupName, -Name och -ResourceType tillhandahålls</span><span class="sxs-lookup"><span data-stu-id="c3c75-207">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="c3c75-208">Förbättra felhanteringen för ”Test-AzDeployment” och ”Test-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="c3c75-208">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="c3c75-209">Hantera fel utanför distributionsvalideringen och ta med dem i kommandoutdata istället</span><span class="sxs-lookup"><span data-stu-id="c3c75-209">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="c3c75-210">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="c3c75-210">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="c3c75-211">Lägg till växlingsparametern -IgnoreDynamicParameters till en uppsättning av cmdletar för distribution för att hoppa över fråga i skript och jobbscenarier</span><span class="sxs-lookup"><span data-stu-id="c3c75-211">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="c3c75-212">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="c3c75-212">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="c3c75-213">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c3c75-213">Az.Sql</span></span>
* <span data-ttu-id="c3c75-214">Stöd för dataklassificering av databaser.</span><span class="sxs-lookup"><span data-stu-id="c3c75-214">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c3c75-215">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c3c75-215">Az.Storage</span></span>
* <span data-ttu-id="c3c75-216">Rapportera detaljfel när lagringskontext skapas med parametern -UseConnectedAccount, men utan inloggning på Azure-kontot</span><span class="sxs-lookup"><span data-stu-id="c3c75-216">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="c3c75-217">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="c3c75-217">New-AzStorageContext</span></span>
* <span data-ttu-id="c3c75-218">Stöd för att hantera Blob Service-egenskaper för ett angivet lagringskonto med API:et för hanteringsplan</span><span class="sxs-lookup"><span data-stu-id="c3c75-218">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="c3c75-219">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="c3c75-219">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="c3c75-220">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="c3c75-220">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="c3c75-221">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="c3c75-221">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="c3c75-222">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="c3c75-222">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="c3c75-223">Stöd för -AsJob-cmdletar för att ladda upp och ladda ned blobar och filer</span><span class="sxs-lookup"><span data-stu-id="c3c75-223">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="c3c75-224">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="c3c75-224">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="c3c75-225">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="c3c75-225">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="c3c75-226">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="c3c75-226">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="c3c75-227">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="c3c75-227">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="c3c75-228">1.6.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="c3c75-228">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="c3c75-229">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="c3c75-229">Highlights since the last major release</span></span>
* <span data-ttu-id="c3c75-230">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="c3c75-230">General availability of `Az` module</span></span>
* <span data-ttu-id="c3c75-231">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="c3c75-231">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="c3c75-232">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="c3c75-232">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="c3c75-233">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="c3c75-233">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="c3c75-234">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="c3c75-234">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="c3c75-235">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="c3c75-235">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="c3c75-236">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="c3c75-236">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="c3c75-237">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c3c75-237">Az.Automation</span></span>
* <span data-ttu-id="c3c75-238">Azure Automation – ändring av uppdateringshantering för stöd för de nya funktionerna:</span><span class="sxs-lookup"><span data-stu-id="c3c75-238">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="c3c75-239">Dynamisk gruppering</span><span class="sxs-lookup"><span data-stu-id="c3c75-239">Dynamic grouping</span></span>
    * <span data-ttu-id="c3c75-240">För-/efterskrift</span><span class="sxs-lookup"><span data-stu-id="c3c75-240">Pre-Post script</span></span>
    * <span data-ttu-id="c3c75-241">Inställning för omstart</span><span class="sxs-lookup"><span data-stu-id="c3c75-241">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c3c75-242">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c3c75-242">Az.Compute</span></span>
* <span data-ttu-id="c3c75-243">Åtgärda problem med sökvägsmatchning i Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="c3c75-243">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="c3c75-244">Uppdatera Compute-klientbibliotek till 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="c3c75-244">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="c3c75-245">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c3c75-245">Az.KeyVault</span></span>
* <span data-ttu-id="c3c75-246">Stöd för jokertecken för KeyVault-cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="c3c75-246">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c3c75-247">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c3c75-247">Az.Network</span></span>
* <span data-ttu-id="c3c75-248">Lägg till stöd för Threat Intelligence för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="c3c75-248">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="c3c75-249">Lägg till resurs för brandväggsprincip på översta nivå och anpassade regler för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="c3c75-249">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c3c75-250">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c3c75-250">Az.RecoveryServices</span></span>
* <span data-ttu-id="c3c75-251">SnapshotRetentionInDays har lagts till i Azure-principen för virtuella datorer för stöd av Instant RP</span><span class="sxs-lookup"><span data-stu-id="c3c75-251">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="c3c75-252">Pipe-stöd för avregistrering av container har lagts till</span><span class="sxs-lookup"><span data-stu-id="c3c75-252">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="c3c75-253">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c3c75-253">Az.Resources</span></span>
* <span data-ttu-id="c3c75-254">Uppdatera stöd för jokertecken för Get-AzResource och Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c3c75-254">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="c3c75-255">Uppdatera autentiseringsuppgifter som används vid allmänna anrop till ARM</span><span class="sxs-lookup"><span data-stu-id="c3c75-255">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="c3c75-256">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c3c75-256">Az.Sql</span></span>
* <span data-ttu-id="c3c75-257">Cmdlet-parametern (ExcludeDetectionType) för Hotidentifiering ändrades från DetectionType till sträng[] för att framtidssäkra den när nya DetectionTypes läggs till, och även för att stödja automatisk ifyllning.</span><span class="sxs-lookup"><span data-stu-id="c3c75-257">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c3c75-258">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c3c75-258">Az.Storage</span></span>
* <span data-ttu-id="c3c75-259">Stöd för att hämta/ange/ta bort hanteringsprincip på ett lagringskonto</span><span class="sxs-lookup"><span data-stu-id="c3c75-259">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="c3c75-260">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="c3c75-260">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="c3c75-261">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="c3c75-261">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="c3c75-262">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="c3c75-262">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="c3c75-263">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="c3c75-263">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="c3c75-264">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="c3c75-264">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="c3c75-265">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="c3c75-265">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c3c75-266">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c3c75-266">Az.Websites</span></span>
* <span data-ttu-id="c3c75-267">Åtgärda fel med ARM-mall som avbryter kloning av alla platser med 'New-AzWebApp -IncludeSourceWebAppSlots'</span><span class="sxs-lookup"><span data-stu-id="c3c75-267">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="c3c75-268">1.5.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="c3c75-268">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c3c75-269">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c3c75-269">Az.Accounts</span></span>
* <span data-ttu-id="c3c75-270">Lägg till kommandot Register-AzModule för stöd för AutoRest-genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="c3c75-270">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="c3c75-271">Uppdatera exempel för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="c3c75-271">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="c3c75-272">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c3c75-272">Az.Automation</span></span>
* <span data-ttu-id="c3c75-273">Problem med att hämta vissa månadsscheman i flera Azure Automation-cmdletar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="c3c75-273">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="c3c75-274">Åtgärda problem med att Get-AzAutomationDscNode bara returnerar de 20 översta noderna.</span><span class="sxs-lookup"><span data-stu-id="c3c75-274">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="c3c75-275">Nu returneras alla noder</span><span class="sxs-lookup"><span data-stu-id="c3c75-275">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="c3c75-276">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="c3c75-276">Az.Cdn</span></span>
* <span data-ttu-id="c3c75-277">Nya Powershell-cmdletar för att aktivera/inaktivera anpassade domän-HTTPS har lagts till och de gamla har gjorts inaktuella</span><span class="sxs-lookup"><span data-stu-id="c3c75-277">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c3c75-278">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c3c75-278">Az.Compute</span></span>
* <span data-ttu-id="c3c75-279">Lägg till stöd för jokertecken för Get-cmdletar</span><span class="sxs-lookup"><span data-stu-id="c3c75-279">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="c3c75-280">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c3c75-280">Az.DataFactory</span></span>
* <span data-ttu-id="c3c75-281">ADF .Net SDK-versionen har uppdaterats till 3.0.1</span><span class="sxs-lookup"><span data-stu-id="c3c75-281">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="c3c75-282">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="c3c75-282">Az.LogicApp</span></span>
* <span data-ttu-id="c3c75-283">Åtgärda problemet med att ListWorkflows endast hämtar den första sidan med resultat</span><span class="sxs-lookup"><span data-stu-id="c3c75-283">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c3c75-284">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c3c75-284">Az.Network</span></span>
* <span data-ttu-id="c3c75-285">Lägg till stöd för jokertecken för Network-cmdletar</span><span class="sxs-lookup"><span data-stu-id="c3c75-285">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c3c75-286">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c3c75-286">Az.RecoveryServices</span></span>
* <span data-ttu-id="c3c75-287">Stöd har lagts till för SQL Server i virtuella Azure-datorer</span><span class="sxs-lookup"><span data-stu-id="c3c75-287">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="c3c75-288">SDK-uppdatering</span><span class="sxs-lookup"><span data-stu-id="c3c75-288">SDK Update</span></span>
* <span data-ttu-id="c3c75-289">Get-ProtectableItem-incheckning i VMappContainer har tagits bort</span><span class="sxs-lookup"><span data-stu-id="c3c75-289">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="c3c75-290">Name och ServerName har lagts till som parametrar för Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="c3c75-290">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="c3c75-291">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c3c75-291">Az.Resources</span></span>
* <span data-ttu-id="c3c75-292">Lägg till parametern `-TemplateObject` i cmdletar för distribution</span><span class="sxs-lookup"><span data-stu-id="c3c75-292">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="c3c75-293">Mer information här: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="c3c75-293">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="c3c75-294">Åtgärda problem med piping av resultatet i `Get-AzResource` till `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="c3c75-294">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="c3c75-295">Mer information här: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="c3c75-295">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="c3c75-296">Åtgärda problem med ändring av JSON-datatyp när `Set-AzResource` körs</span><span class="sxs-lookup"><span data-stu-id="c3c75-296">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="c3c75-297">Mer information här: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="c3c75-297">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="c3c75-298">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c3c75-298">Az.Sql</span></span>
* <span data-ttu-id="c3c75-299">AuditingEndpointsCommunicator uppdateras.</span><span class="sxs-lookup"><span data-stu-id="c3c75-299">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="c3c75-300">Åtgärdar beteendet hos ett gränsscenario när nya diagnostikinställningar skapas.</span><span class="sxs-lookup"><span data-stu-id="c3c75-300">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c3c75-301">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c3c75-301">Az.Storage</span></span>
* <span data-ttu-id="c3c75-302">Stöd för BlockBlobStorage när Storage-konto skapas      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c3c75-302">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="c3c75-303">1.4.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="c3c75-303">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="c3c75-304">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="c3c75-304">Az.AnalysisServices</span></span>
* <span data-ttu-id="c3c75-305">Inaktuell AddAzureASAccount-cmdlet</span><span class="sxs-lookup"><span data-stu-id="c3c75-305">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="c3c75-306">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c3c75-306">Az.Automation</span></span>
* <span data-ttu-id="c3c75-307">Hjälpen för Import-AzAutomationDscNodeConfiguration har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="c3c75-307">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="c3c75-308">Konfigurationsnamnsvalidering har lagts till i cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="c3c75-308">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="c3c75-309">Förbättrad felhantering för cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="c3c75-309">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="c3c75-310">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="c3c75-310">Az.CognitiveServices</span></span>
* <span data-ttu-id="c3c75-311">CustomSubdomainName har lagts till som en ny valfri parameter för New-AzCognitiveServicesAccount, som används för att ange underdomän för resursen.</span><span class="sxs-lookup"><span data-stu-id="c3c75-311">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c3c75-312">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c3c75-312">Az.Compute</span></span>
* <span data-ttu-id="c3c75-313">Problemet med ID-parameteruppsättningar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="c3c75-313">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="c3c75-314">Get-AzVMExtension har uppdaterats så att alla installerade tillägg visas om parametern Name inte har angetts</span><span class="sxs-lookup"><span data-stu-id="c3c75-314">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="c3c75-315">Parametrarna Tag och ResourceId har lagts till i cmdleten Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="c3c75-315">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="c3c75-316">Get-AzVmssVM utan instans-ID och med InstanceView kan visa virtuella VMSS-datorer med instansvyn.</span><span class="sxs-lookup"><span data-stu-id="c3c75-316">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="c3c75-317">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c3c75-317">Az.DataLakeStore</span></span>
* <span data-ttu-id="c3c75-318">Cmdletar har lagts till för uppräkning och återställning av borttagna objekt i ADL</span><span class="sxs-lookup"><span data-stu-id="c3c75-318">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="c3c75-319">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="c3c75-319">Az.EventHub</span></span>
* <span data-ttu-id="c3c75-320">Ny boolesk egenskap SkipEmptyArchives har lagts till i Skip Empty Archives i CaptureDescription-klassen i Eventhub</span><span class="sxs-lookup"><span data-stu-id="c3c75-320">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="c3c75-321">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c3c75-321">Az.KeyVault</span></span>
* <span data-ttu-id="c3c75-322">Taggning i Set-AzKeyVaultSecret har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="c3c75-322">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="c3c75-323">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="c3c75-323">Az.LogicApp</span></span>
* <span data-ttu-id="c3c75-324">Grundläggande SKU har lagts till för Integrationskonton</span><span class="sxs-lookup"><span data-stu-id="c3c75-324">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="c3c75-325">XSLT 2.0, XSLT 3.0 och Flytande mappningstyper har lagts till</span><span class="sxs-lookup"><span data-stu-id="c3c75-325">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="c3c75-326">Nya cmdletar för integrationskontosammansättningar</span><span class="sxs-lookup"><span data-stu-id="c3c75-326">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="c3c75-327">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="c3c75-327">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="c3c75-328">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="c3c75-328">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="c3c75-329">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="c3c75-329">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="c3c75-330">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="c3c75-330">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="c3c75-331">Nya cmdletar för batchkonfiguration för integrationskonto</span><span class="sxs-lookup"><span data-stu-id="c3c75-331">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="c3c75-332">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="c3c75-332">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="c3c75-333">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="c3c75-333">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="c3c75-334">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="c3c75-334">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="c3c75-335">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="c3c75-335">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="c3c75-336">Logic App-SDK har uppdaterats till version 4.1.0</span><span class="sxs-lookup"><span data-stu-id="c3c75-336">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="c3c75-337">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="c3c75-337">Az.Monitor</span></span>
* <span data-ttu-id="c3c75-338">Hjälpen för Get-AzMetric har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="c3c75-338">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c3c75-339">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c3c75-339">Az.Network</span></span>
* <span data-ttu-id="c3c75-340">Hjälpexempel för Add-AzApplicationGatewayCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="c3c75-340">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="c3c75-341">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="c3c75-341">Az.OperationalInsights</span></span>
* <span data-ttu-id="c3c75-342">Ytterligare stöd för datakällorna New och Get ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="c3c75-342">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="c3c75-343">Ny ApplicationInsights-typ har lagts till för att ge stöd för ”Get specific” och ”Get all” för ApplicationInsights-datakällor för angiven arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="c3c75-343">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="c3c75-344">Cmdleten New-AzOperationalInsightsApplicationInsightsDataSource har lagts till för att skapa datakälla med angivna parametrar för Application Insights-resurs: subscription Id, resourceGroupName och name.</span><span class="sxs-lookup"><span data-stu-id="c3c75-344">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="c3c75-345">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c3c75-345">Az.Resources</span></span>
* <span data-ttu-id="c3c75-346">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="c3c75-346">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="c3c75-347">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="c3c75-347">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="c3c75-348">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="c3c75-348">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="c3c75-349">Fel som gör att KeyCredentials inte kan skapas upprepade gånger har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="c3c75-349">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="c3c75-350">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c3c75-350">Az.Sql</span></span>
* <span data-ttu-id="c3c75-351">Lägg till stöd för hyperskalanivån för SQL DB</span><span class="sxs-lookup"><span data-stu-id="c3c75-351">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="c3c75-352">Ett fel har åtgärdats där återställningen kunde misslyckas på grund av onödiga inställningsegenskaper i restore-förfrågan</span><span class="sxs-lookup"><span data-stu-id="c3c75-352">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c3c75-353">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c3c75-353">Az.Websites</span></span>
* <span data-ttu-id="c3c75-354">Rätt exempel i Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="c3c75-354">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="c3c75-355">1.3.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="c3c75-355">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c3c75-356">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c3c75-356">Az.Accounts</span></span>
* <span data-ttu-id="c3c75-357">Uppdatera till den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="c3c75-357">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="c3c75-358">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="c3c75-358">Az.AnalysisServices</span></span>
<span data-ttu-id="c3c75-359">Allmän tillgänglighet för Az.AnalysisServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="c3c75-359">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c3c75-360">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c3c75-360">Az.Compute</span></span>
* <span data-ttu-id="c3c75-361">AEM-tillägg: Lägg till stöd för UltraSSD-, P60-, P70- och P80-diskar</span><span class="sxs-lookup"><span data-stu-id="c3c75-361">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="c3c75-362">Uppdatera hjälpbeskrivning för Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="c3c75-362">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="c3c75-363">Uppdatera hjälpbeskrivning och exempel för Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="c3c75-363">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c3c75-364">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c3c75-364">Az.RecoveryServices</span></span>
<span data-ttu-id="c3c75-365">Allmän tillgänglighet för Az.RecoveryServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="c3c75-365">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="c3c75-366">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c3c75-366">Az.Resources</span></span>
* <span data-ttu-id="c3c75-367">Korrigera taggar för resursgrupper</span><span class="sxs-lookup"><span data-stu-id="c3c75-367">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="c3c75-368">Mer information här: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="c3c75-368">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="c3c75-369">Åtgärda problem där `Get-AzureRmRoleAssignment` inte respekterar -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="c3c75-369">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="c3c75-370">Mer information här: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="c3c75-370">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="c3c75-371">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c3c75-371">Az.Sql</span></span>
* <span data-ttu-id="c3c75-372">Lägga till Get/Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="c3c75-372">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="c3c75-373">Åtgärda problem där ett nullref-undantag uppstår när du kör SQL-cmdletar och inte är inloggad på ett Azure-konto</span><span class="sxs-lookup"><span data-stu-id="c3c75-373">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="c3c75-374">Åtgärda nullref-undantag i Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="c3c75-374">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="c3c75-375">1.2.1 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="c3c75-375">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c3c75-376">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c3c75-376">Az.Accounts</span></span>
* <span data-ttu-id="c3c75-377">Version med rätt version av autentisering</span><span class="sxs-lookup"><span data-stu-id="c3c75-377">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="c3c75-378">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="c3c75-378">Az.AnalysisServices</span></span>
* <span data-ttu-id="c3c75-379">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="c3c75-379">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c3c75-380">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c3c75-380">Az.RecoveryServices</span></span>
* <span data-ttu-id="c3c75-381">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="c3c75-381">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="c3c75-382">1.2.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="c3c75-382">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c3c75-383">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c3c75-383">Az.Accounts</span></span>
* <span data-ttu-id="c3c75-384">Lägga till interaktiv autentisering och autentisering med användarnamn/lösenord för endast Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="c3c75-384">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="c3c75-385">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="c3c75-385">Update incorrect online help URLs</span></span>
* <span data-ttu-id="c3c75-386">Lägga till varningsmeddelande i PS Core för Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="c3c75-386">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="c3c75-387">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="c3c75-387">Az.Aks</span></span>
* <span data-ttu-id="c3c75-388">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="c3c75-388">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="c3c75-389">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c3c75-389">Az.Automation</span></span>
* <span data-ttu-id="c3c75-390">Stöd för Python 2-runbookflöden har lagts till</span><span class="sxs-lookup"><span data-stu-id="c3c75-390">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="c3c75-391">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="c3c75-391">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="c3c75-392">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="c3c75-392">Az.Cdn</span></span>
* <span data-ttu-id="c3c75-393">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="c3c75-393">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c3c75-394">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c3c75-394">Az.Compute</span></span>
* <span data-ttu-id="c3c75-395">Lägga till cmdleten Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="c3c75-395">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="c3c75-396">Lägga till TempDisk-parameter i Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="c3c75-396">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="c3c75-397">Korrigera varningsmeddelande för New-AzVM</span><span class="sxs-lookup"><span data-stu-id="c3c75-397">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="c3c75-398">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c3c75-398">Az.ContainerRegistry</span></span>
* <span data-ttu-id="c3c75-399">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="c3c75-399">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="c3c75-400">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c3c75-400">Az.DataFactory</span></span>
* <span data-ttu-id="c3c75-401">ADF .Net SDK-versionen har uppdaterats till 3.0.0</span><span class="sxs-lookup"><span data-stu-id="c3c75-401">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="c3c75-402">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c3c75-402">Az.DataLakeStore</span></span>
* <span data-ttu-id="c3c75-403">Åtgärda problem med ADLS-slutpunkt vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="c3c75-403">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="c3c75-404">Mer information här: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="c3c75-404">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="c3c75-405">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="c3c75-405">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="c3c75-406">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="c3c75-406">Az.IotHub</span></span>
* <span data-ttu-id="c3c75-407">Lägga till kodningsformat i cmdleten Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="c3c75-407">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="c3c75-408">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c3c75-408">Az.KeyVault</span></span>
* <span data-ttu-id="c3c75-409">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="c3c75-409">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c3c75-410">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c3c75-410">Az.Network</span></span>
* <span data-ttu-id="c3c75-411">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="c3c75-411">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="c3c75-412">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c3c75-412">Az.Resources</span></span>
* <span data-ttu-id="c3c75-413">Åtgärda felaktiga exempel i referensdokumentationen ”New-AzADAppCredential” och ”New-AzADSpCredential”</span><span class="sxs-lookup"><span data-stu-id="c3c75-413">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="c3c75-414">Åtgärda problem där sökvägen för parametern ”-TemplateFile” inte omvandlas innan cmdletarna för distribution i resursgruppen körs</span><span class="sxs-lookup"><span data-stu-id="c3c75-414">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="c3c75-415">Az.Resources: Korrigera dokumentationen om standardvärdet för New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="c3c75-415">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="c3c75-416">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="c3c75-416">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="c3c75-417">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="c3c75-417">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="c3c75-418">Åtgärda formateringsproblemet med objektet ”PSResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="c3c75-418">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="c3c75-419">Mer information här: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="c3c75-419">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="c3c75-420">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c3c75-420">Az.ServiceFabric</span></span>
* <span data-ttu-id="c3c75-421">Återställ när ett certifikat läggs till i en Virtual Machine Scale Sets-modell men ett undantag genereras. Detta har gjorts för att åtgärda följande fel: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="c3c75-421">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="c3c75-422">Korrigera några felmeddelanden.</span><span class="sxs-lookup"><span data-stu-id="c3c75-422">Fix some error messages.</span></span>
* <span data-ttu-id="c3c75-423">Korrigering av skapande av kluster med ARM-mall som är standard för New-AzServiceFabriCluster som inte fungerade med migrering till Az.</span><span class="sxs-lookup"><span data-stu-id="c3c75-423">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="c3c75-424">Korrigering av tilläggning av kluster/programcertifikat så att endast VM Scale Sets som motsvarar klustret läggs till genom att kontrollera ID för klustret i tillägget.</span><span class="sxs-lookup"><span data-stu-id="c3c75-424">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="c3c75-425">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="c3c75-425">Az.SignalR</span></span>
* <span data-ttu-id="c3c75-426">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="c3c75-426">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="c3c75-427">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c3c75-427">Az.Sql</span></span>
* <span data-ttu-id="c3c75-428">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="c3c75-428">Update incorrect online help URLs</span></span>
* <span data-ttu-id="c3c75-429">Uppdaterad parameterbeskrivning för LicenseType-parameter med möjliga värden</span><span class="sxs-lookup"><span data-stu-id="c3c75-429">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="c3c75-430">Korrigering för att uppdatera hanterad instansidentitet som inte fungerar när det är den enda uppdaterade egenskapen</span><span class="sxs-lookup"><span data-stu-id="c3c75-430">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="c3c75-431">Stöd för anpassad sortering på hanterad instans</span><span class="sxs-lookup"><span data-stu-id="c3c75-431">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c3c75-432">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c3c75-432">Az.Storage</span></span>
* <span data-ttu-id="c3c75-433">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="c3c75-433">Update incorrect online help URLs</span></span>
* <span data-ttu-id="c3c75-434">Tillhandahåll detaljerat felmeddelande när en användare försöker hämta/konfigurera klassisk loggning/mått på ett Premium Storage-konto eftersom Premium Storage-kontot inte har stöd för klassisk loggning/mått.</span><span class="sxs-lookup"><span data-stu-id="c3c75-434">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="c3c75-435">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="c3c75-435">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="c3c75-436">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="c3c75-436">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="c3c75-437">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="c3c75-437">Az.TrafficManager</span></span>
* <span data-ttu-id="c3c75-438">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="c3c75-438">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c3c75-439">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c3c75-439">Az.Websites</span></span>
* <span data-ttu-id="c3c75-440">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="c3c75-440">Update incorrect online help URLs</span></span>
* <span data-ttu-id="c3c75-441">Korrigerar ”New-AzWebAppSSLBinding” så att certifikatet laddas upp till rätt resursgrupp och plats om appen finns i en ASE.</span><span class="sxs-lookup"><span data-stu-id="c3c75-441">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="c3c75-442">Korrigerar ”New-AzWebAppSSLBinding” så att taggarna inte skrivs över på en bindning av ett SSL-certifikat till en app</span><span class="sxs-lookup"><span data-stu-id="c3c75-442">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="c3c75-443">1.1.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="c3c75-443">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c3c75-444">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c3c75-444">Az.Accounts</span></span>
* <span data-ttu-id="c3c75-445">Lade till omfattningen ”Lokal” till Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="c3c75-445">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c3c75-446">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c3c75-446">Az.Compute</span></span>
* <span data-ttu-id="c3c75-447">Namn är nu valfritt i ID-parametern för Restart/Start/Stop/Remove/Set-AzVM och Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="c3c75-447">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="c3c75-448">Uppdaterade beskrivningen av ID i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="c3c75-448">Updated the description of ID in help files</span></span>
* <span data-ttu-id="c3c75-449">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c3c75-449">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="c3c75-450">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c3c75-450">Az.DataLakeStore</span></span>
* <span data-ttu-id="c3c75-451">Uppdatera sdk-versionen av dataplanet till 1.1.14 för SDK-korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="c3c75-451">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="c3c75-452">Korrigerade hanteringen av negativ accesstime och modificationtime för getfilestatus och liststatus; korrigera asynkront annulleringstoken</span><span class="sxs-lookup"><span data-stu-id="c3c75-452">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="c3c75-453">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="c3c75-453">Az.EventGrid</span></span>
* <span data-ttu-id="c3c75-454">Uppdaterat för användning av API-versionen 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="c3c75-454">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="c3c75-455">Uppdaterade följande cmdletar för att stödja nytt scenario i API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="c3c75-455">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="c3c75-456">New-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="c3c75-456">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="c3c75-457">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="c3c75-457">Event Time-To-Live,</span></span>
        - <span data-ttu-id="c3c75-458">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="c3c75-458">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="c3c75-459">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="c3c75-459">Dead letter endpoint.</span></span>
    - <span data-ttu-id="c3c75-460">Update-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="c3c75-460">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="c3c75-461">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="c3c75-461">Event Time-To-Live,</span></span>
        - <span data-ttu-id="c3c75-462">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="c3c75-462">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="c3c75-463">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="c3c75-463">Dead letter endpoint.</span></span>
* <span data-ttu-id="c3c75-464">Lade till nya enum-värden (storageQueue och hybridConnection) för alternativet EndpointType i cmdletarna New-AzureRmEventGridSubscription och Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="c3c75-464">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="c3c75-465">Visa varningsmeddelanden om skapande eller uppdatering av händelseprenumerationen förväntas medföra manuell åtgärd från användaren.</span><span class="sxs-lookup"><span data-stu-id="c3c75-465">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="c3c75-466">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="c3c75-466">Az.IotHub</span></span>
* <span data-ttu-id="c3c75-467">Har uppdaterats till den senaste versionen av SDK:n lotHub</span><span class="sxs-lookup"><span data-stu-id="c3c75-467">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="c3c75-468">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="c3c75-468">Az.LogicApp</span></span>
* <span data-ttu-id="c3c75-469">Get-AzLogicApp visar en lista över alla som inte har angivet namn</span><span class="sxs-lookup"><span data-stu-id="c3c75-469">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="c3c75-470">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c3c75-470">Az.Resources</span></span>
* <span data-ttu-id="c3c75-471">Åtgärdade problem med parameteruppsättningen när parametrarna -ODataQuery och -ResourceId anges för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="c3c75-471">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="c3c75-472">Mer information här: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="c3c75-472">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="c3c75-473">Åtgärdade hantering av parametern -Custom i New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c3c75-473">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="c3c75-474">Korrigerade stavfel i New-AzDeployment-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="c3c75-474">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="c3c75-475">Gjorde parametern -MailNickname obligatorisk för New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="c3c75-475">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="c3c75-476">Mer information här: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="c3c75-476">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="c3c75-477">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="c3c75-477">Az.SignalR</span></span>
* <span data-ttu-id="c3c75-478">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c3c75-478">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="c3c75-479">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c3c75-479">Az.Sql</span></span>
* <span data-ttu-id="c3c75-480">Konverterade lagringshanteringsklientens beroende av den normala SDK-implementeringen.</span><span class="sxs-lookup"><span data-stu-id="c3c75-480">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c3c75-481">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c3c75-481">Az.Storage</span></span>
* <span data-ttu-id="c3c75-482">Angav StorageAccountName för lagringskontext som det verkliga namnet på lagringskontot när det skapas med Sas Token, OAuth eller Anonymous</span><span class="sxs-lookup"><span data-stu-id="c3c75-482">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="c3c75-483">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="c3c75-483">New-AzStorageContext</span></span>
* <span data-ttu-id="c3c75-484">Skapade Sas Token för Blob Snapshot-objekt med parametern -FullUri, åtgärdade den returnerade URI:n så att den blir URI för ögonblicksbild</span><span class="sxs-lookup"><span data-stu-id="c3c75-484">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="c3c75-485">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="c3c75-485">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c3c75-486">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c3c75-486">Az.Websites</span></span>
* <span data-ttu-id="c3c75-487">Åtgärdade en bugg i datumparsningen i Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="c3c75-487">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="c3c75-488">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c3c75-488">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="c3c75-489">1.0.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="c3c75-489">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="c3c75-490">Allmänt</span><span class="sxs-lookup"><span data-stu-id="c3c75-490">General</span></span>

- <span data-ttu-id="c3c75-491">Allmän tillgänglighet för Az-modulen</span><span class="sxs-lookup"><span data-stu-id="c3c75-491">General Availability of Az Module</span></span>
- <span data-ttu-id="c3c75-492">Onlinehjälp för varje modul</span><span class="sxs-lookup"><span data-stu-id="c3c75-492">Online help for each module</span></span>
- <span data-ttu-id="c3c75-493">Mer information och en översikt finns på [Az-informationssidan](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="c3c75-493">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="c3c75-494">Information om hur du migrerar från AzureRM finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c3c75-494">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="c3c75-495">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c3c75-495">Az.Accounts</span></span>
- <span data-ttu-id="c3c75-496">Har ändrats från Az.Profile</span><span class="sxs-lookup"><span data-stu-id="c3c75-496">Changed from Az.Profile</span></span>
- <span data-ttu-id="c3c75-497">Fasta tabellformat för profil- och kontexttyper</span><span class="sxs-lookup"><span data-stu-id="c3c75-497">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="c3c75-498">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c3c75-498">Az.ApiManagement</span></span>
- <span data-ttu-id="c3c75-499">Korrigeringar för #7002</span><span class="sxs-lookup"><span data-stu-id="c3c75-499">Fixes for #7002</span></span>
- <span data-ttu-id="c3c75-500">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c3c75-500">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="c3c75-501">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="c3c75-501">Az.Batch</span></span>
- <span data-ttu-id="c3c75-502">Lade till möjligheten att se vilken version av Azure Batch Node Agent som körs på var och en av de virtuella datorerna i en pool, via den nya egenskapen `NodeAgentInformation` på `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="c3c75-502">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="c3c75-503">Standarden `Caching` för `PSDataDisk` är nu `ReadWrite` i stället för `None`.</span><span class="sxs-lookup"><span data-stu-id="c3c75-503">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="c3c75-504">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c3c75-504">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="c3c75-505">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="c3c75-505">Az.Billing</span></span>
- <span data-ttu-id="c3c75-506">Kombinerar cmdletarna för fakturering, förbrukning och UsageAggregates. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c3c75-506">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="c3c75-507">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="c3c75-507">Az.CognitivServices</span></span>
- <span data-ttu-id="c3c75-508">Lade till kompletterare för SkuName och Typem som är tillgängliga i New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="c3c75-508">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="c3c75-509">Tog bort parameteruppsättningen GetSkusWithAccountParamSetName från Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="c3c75-509">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="c3c75-510">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="c3c75-510">Az.ContainerInstance</span></span>
- <span data-ttu-id="c3c75-511">Stöd för ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="c3c75-511">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="c3c75-512">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="c3c75-512">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="c3c75-513">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c3c75-513">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="c3c75-514">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c3c75-514">Az.DataLakeStore</span></span>
- <span data-ttu-id="c3c75-515">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c3c75-515">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="c3c75-516">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="c3c75-516">Az.Monitor</span></span>
- <span data-ttu-id="c3c75-517">Döpte om Az.Insights till Az.Monitor och andra mindre icke-bakåtkompatibla ändringar. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c3c75-517">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="c3c75-518">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c3c75-518">Az.KeyVault</span></span>
- <span data-ttu-id="c3c75-519">Tog bort den inaktuella egenskapen PurgeDisabled från utdatatyper</span><span class="sxs-lookup"><span data-stu-id="c3c75-519">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="c3c75-520">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="c3c75-520">Az.MachineLearning</span></span>
- <span data-ttu-id="c3c75-521">Inkluderade cmdletarna från modulen Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="c3c75-521">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="c3c75-522">Az.Media</span><span class="sxs-lookup"><span data-stu-id="c3c75-522">Az.Media</span></span>
- <span data-ttu-id="c3c75-523">Tog bort inaktuella -Tags-alias från New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="c3c75-523">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="c3c75-524">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c3c75-524">Az.Network</span></span>
<span data-ttu-id="c3c75-525">Stöd har lagts till för konfiguration av RewriteRuleSets i Application Gateway</span><span class="sxs-lookup"><span data-stu-id="c3c75-525">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="c3c75-526">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="c3c75-526">New cmdlets added:</span></span>
        - <span data-ttu-id="c3c75-527">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c3c75-527">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="c3c75-528">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c3c75-528">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="c3c75-529">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c3c75-529">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="c3c75-530">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c3c75-530">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="c3c75-531">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c3c75-531">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="c3c75-532">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="c3c75-532">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="c3c75-533">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="c3c75-533">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="c3c75-534">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="c3c75-534">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="c3c75-535">Cmdletar har uppdaterats med den valfria parametern -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c3c75-535">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="c3c75-536">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c3c75-536">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="c3c75-537">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c3c75-537">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="c3c75-538">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c3c75-538">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="c3c75-539">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c3c75-539">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="c3c75-540">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="c3c75-540">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="c3c75-541">New-AzureRmApplicationGatewayUrlPathMapConfig har lagt till KeyVault-stöd för Application Gateway med Identity.</span><span class="sxs-lookup"><span data-stu-id="c3c75-541">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="c3c75-542">Cmdletar har uppdaterats med den valfria parametern -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="c3c75-542">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="c3c75-543">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c3c75-543">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="c3c75-544">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c3c75-544">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="c3c75-545">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c3c75-545">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="c3c75-546">Cmdleten New-AzApplicationGateway har uppdaterats med den valfria parametern -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="c3c75-546">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="c3c75-547">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c3c75-547">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="c3c75-548">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="c3c75-548">Az.OperationalInsights</span></span>
- <span data-ttu-id="c3c75-549">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c3c75-549">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="c3c75-550">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="c3c75-550">Az.Profile</span></span>
- <span data-ttu-id="c3c75-551">Modulnamnet har ändrats till Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c3c75-551">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="c3c75-552">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c3c75-552">Az.RecoveryServices</span></span>
- <span data-ttu-id="c3c75-553">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c3c75-553">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="c3c75-554">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c3c75-554">Az.Resources</span></span>
- <span data-ttu-id="c3c75-555">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c3c75-555">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="c3c75-556">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c3c75-556">Az.ServiceFabric</span></span>
- <span data-ttu-id="c3c75-557">Stöd för specificering av certifikat efter eget namn och tumavtryck</span><span class="sxs-lookup"><span data-stu-id="c3c75-557">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="c3c75-558">Information om fler icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c3c75-558">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="c3c75-559">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="c3c75-559">Az.SIgnalR</span></span>
- <span data-ttu-id="c3c75-560">Allmän tillgänglighet för PowerShell-cmdletar för SIgnalR</span><span class="sxs-lookup"><span data-stu-id="c3c75-560">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="c3c75-561">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c3c75-561">Az.Sql</span></span>
- <span data-ttu-id="c3c75-562">Lade till de nya identifieringstyperna Data_Exfiltration och Unsafe_Action i Threat Detection-cmdletar</span><span class="sxs-lookup"><span data-stu-id="c3c75-562">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="c3c75-563">Uppdaterade dokumentationsexempel för Sql Auditing-cmdletar</span><span class="sxs-lookup"><span data-stu-id="c3c75-563">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="c3c75-564">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c3c75-564">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="c3c75-565">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c3c75-565">Az.Storage</span></span>
- <span data-ttu-id="c3c75-566">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c3c75-566">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="c3c75-567">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c3c75-567">Az.Websites</span></span>
- <span data-ttu-id="c3c75-568">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c3c75-568">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="c3c75-569">0.7.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="c3c75-569">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="c3c75-570">Allmänt</span><span class="sxs-lookup"><span data-stu-id="c3c75-570">General</span></span>

* <span data-ttu-id="c3c75-571">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="c3c75-571">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="c3c75-572">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c3c75-572">Az.Compute</span></span>

* <span data-ttu-id="c3c75-573">Lade till stöd för UltraSSD och Galleriavbildningar i de enkla parameteruppsättningarna för `New-AzVm(ss)`-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="c3c75-573">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="c3c75-574">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c3c75-574">Az.DataLakeStore</span></span>

* <span data-ttu-id="c3c75-575">Åtgärdade avslutande snedstreck i domänen för adls-konto</span><span class="sxs-lookup"><span data-stu-id="c3c75-575">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="c3c75-576">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="c3c75-576">Az.FrontDoor</span></span>

* <span data-ttu-id="c3c75-577">Brutna länkar korrigerades</span><span class="sxs-lookup"><span data-stu-id="c3c75-577">Fixed some broken links</span></span>
    - <span data-ttu-id="c3c75-578">I artiklarna New-AzureRmFrontDoor och Set-AzureRmFrontDoor artiklar korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="c3c75-578">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="c3c75-579">I artikeln New-AzureRmFrontDoorManagedRuleObject korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="c3c75-579">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="c3c75-580">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c3c75-580">Az.RecoveryServices</span></span>

* <span data-ttu-id="c3c75-581">Lade till valideringar på klientsidan för Azure-filresurs med återställningsåtgärder.</span><span class="sxs-lookup"><span data-stu-id="c3c75-581">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="c3c75-582">Gjorde storageAccountName och storageAccountResourceGroupName valfritt för afs-återställning.</span><span class="sxs-lookup"><span data-stu-id="c3c75-582">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="c3c75-583">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c3c75-583">Az.Resources</span></span>

* <span data-ttu-id="c3c75-584">Korrigering för https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="c3c75-584">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="c3c75-585">Uppdaterade Get-AzureRmRoleAssignment så att prenumerationsomfattningen används om den anges vid begäran om klassiska administratörer.</span><span class="sxs-lookup"><span data-stu-id="c3c75-585">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="c3c75-586">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c3c75-586">Az.Sql</span></span>

* <span data-ttu-id="c3c75-587">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="c3c75-587">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="c3c75-588">Korrigerade ett problem med Get-AzureRmSqlDatabaseVulnerabilityAssessment med DotNet-kärna</span><span class="sxs-lookup"><span data-stu-id="c3c75-588">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="c3c75-589">Ändrade dokumentationen för hjälpmeddelanden som rör SQL Auditing-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="c3c75-589">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="c3c75-590">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c3c75-590">Az.Storage</span></span>

* <span data-ttu-id="c3c75-591">Lade till -EnableHierarchicalNamespace i New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c3c75-591">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="c3c75-592">Åtgärdade problemet med att cmdleten Copy File inte kunde återanvända källkontexten på målet om inte -DestContext angetts</span><span class="sxs-lookup"><span data-stu-id="c3c75-592">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="c3c75-593">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="c3c75-593">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="c3c75-594">Stöd för statisk webbplatskonfiguration</span><span class="sxs-lookup"><span data-stu-id="c3c75-594">Support Static Website configuration</span></span>
    - <span data-ttu-id="c3c75-595">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="c3c75-595">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="c3c75-596">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="c3c75-596">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="c3c75-597">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c3c75-597">Az.Websites</span></span>

* <span data-ttu-id="c3c75-598">Set-AzureRmWebApp och Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c3c75-598">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="c3c75-599">Ny parameter (-AzureStoragePath) har lagts till för att ange att Azure Storage-sökvägar ska monteras i containerappar i Windows och Linux.</span><span class="sxs-lookup"><span data-stu-id="c3c75-599">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="c3c75-600">Använder utdata från den nya cmdleten New-AzureRmWebAppAzureStoragePath som en parameter för att ange sökvägar för Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="c3c75-600">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="c3c75-601">0.6.1 – november 2018</span><span class="sxs-lookup"><span data-stu-id="c3c75-601">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="c3c75-602">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c3c75-602">Az.ApiManagement</span></span>
* <span data-ttu-id="c3c75-603">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="c3c75-603">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="c3c75-604">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c3c75-604">Az.Automation</span></span>
* <span data-ttu-id="c3c75-605">Swagger baserade Azure Automation-cmdletar</span><span class="sxs-lookup"><span data-stu-id="c3c75-605">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="c3c75-606">Cmdletar för Uppdateringshantering har lagts till</span><span class="sxs-lookup"><span data-stu-id="c3c75-606">Added Update Management cmdlets</span></span>
* <span data-ttu-id="c3c75-607">Cmdletar för källkontroll har lagts till</span><span class="sxs-lookup"><span data-stu-id="c3c75-607">Added Source Control cmdlets</span></span>
* <span data-ttu-id="c3c75-608">Remove-AzureRmAutomationHybridWorkerGroup-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="c3c75-608">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="c3c75-609">Kommandot för DSC-registreringsnod har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="c3c75-609">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="c3c75-610">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c3c75-610">Az.Compute</span></span>
* <span data-ttu-id="c3c75-611">Problem med SystemAssigned-identitet har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="c3c75-611">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="c3c75-612">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="c3c75-612">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="c3c75-613">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="c3c75-613">Az.ContainerInstance</span></span>
* <span data-ttu-id="c3c75-614">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="c3c75-614">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="c3c75-615">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="c3c75-615">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="c3c75-616">uppdatera exempelbeskrivningen för marketplace-cmdletar</span><span class="sxs-lookup"><span data-stu-id="c3c75-616">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="c3c75-617">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c3c75-617">Az.Network</span></span>
* <span data-ttu-id="c3c75-618">Cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomErreller Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="c3c75-618">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="c3c75-619">ICMP tillbaka till stöd för Azure Firewall-nätverksprotokoll har lagts till</span><span class="sxs-lookup"><span data-stu-id="c3c75-619">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="c3c75-620">Uppdatera cmdlet Test-AzureRmNetworkWatcherConnectivity, lägga till verifiering av mål-id, adress och port.</span><span class="sxs-lookup"><span data-stu-id="c3c75-620">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="c3c75-621">Åtgärda problem med minnesanvändning i VirtualNetwork-karta</span><span class="sxs-lookup"><span data-stu-id="c3c75-621">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="c3c75-622">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="c3c75-622">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="c3c75-623">Åtgärda för att ändra principen för en skyddad fildelning.</span><span class="sxs-lookup"><span data-stu-id="c3c75-623">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="c3c75-624">Tidszonsprincipen har konverterats till versaler.</span><span class="sxs-lookup"><span data-stu-id="c3c75-624">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="c3c75-625">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="c3c75-625">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="c3c75-626">Exempel i New-AzureRmRecoveryServicesAsrProtectableItem har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="c3c75-626">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="c3c75-627">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="c3c75-627">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="c3c75-628">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="c3c75-628">Az.Relay</span></span>
* <span data-ttu-id="c3c75-629">Valfri parameter -KeyValue till New-AzureRmRelayKey cmdlet har lagts till, vilket gör det möjligt för användare att tillhandahålla KeyValue.</span><span class="sxs-lookup"><span data-stu-id="c3c75-629">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="c3c75-630">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c3c75-630">Az.Resources</span></span>
* <span data-ttu-id="c3c75-631">Uppdatera hjälpdokumentation för resursidentitet kopplad till parametrar i `New-AzureRmPolicyAssignment` och `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="c3c75-631">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="c3c75-632">Lägg till ett exempel för New-AzureRmPolicyDefinition som använder -Metadata</span><span class="sxs-lookup"><span data-stu-id="c3c75-632">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="c3c75-633">Korrigera så att skiftläge behålls i taggnycklar i NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="c3c75-633">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="c3c75-634">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c3c75-634">Az.ServiceFabric</span></span>
* <span data-ttu-id="c3c75-635">Lägg till utfasningsmeddelanden för kommande icke-kompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="c3c75-635">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="c3c75-636">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c3c75-636">Az.Sql</span></span>
* <span data-ttu-id="c3c75-637">Nya cmdletar för CRUD-åtgärder på Azure Sql Database-hanterad instans och Azure Sql-hanterad databas</span><span class="sxs-lookup"><span data-stu-id="c3c75-637">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="c3c75-638">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="c3c75-638">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="c3c75-639">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="c3c75-639">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="c3c75-640">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="c3c75-640">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="c3c75-641">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="c3c75-641">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="c3c75-642">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="c3c75-642">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="c3c75-643">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="c3c75-643">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="c3c75-644">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="c3c75-644">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="c3c75-645">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="c3c75-645">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="c3c75-646">Hantering av utökad granskningsprincip på en server eller en databas har aktiverats.</span><span class="sxs-lookup"><span data-stu-id="c3c75-646">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="c3c75-647">Ny parameter (PredicateExpression) har lagts till för att aktivera filtrering av granskningsloggar.</span><span class="sxs-lookup"><span data-stu-id="c3c75-647">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="c3c75-648">Cmdletar har ändrats så att de använder SQL-klienter i stället för äldre klienter.</span><span class="sxs-lookup"><span data-stu-id="c3c75-648">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="c3c75-649">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="c3c75-649">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="c3c75-650">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="c3c75-650">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="c3c75-651">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="c3c75-651">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="c3c75-652">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="c3c75-652">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="c3c75-653">Problem med att använda Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings med lagringskontots namnparameter har korrigerats</span><span class="sxs-lookup"><span data-stu-id="c3c75-653">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="c3c75-654">0.5.0 – november 2018</span><span class="sxs-lookup"><span data-stu-id="c3c75-654">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="c3c75-655">Allmänt</span><span class="sxs-lookup"><span data-stu-id="c3c75-655">General</span></span>
* <span data-ttu-id="c3c75-656">Lade till resurskompletterare till många kärn-cmdletar – dessa gör att du kan stega genom befintliga resursnamn med TABB vid interaktiva anrop till cmdletar</span><span class="sxs-lookup"><span data-stu-id="c3c75-656">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="c3c75-657">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="c3c75-657">Az.Profile</span></span>
* <span data-ttu-id="c3c75-658">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="c3c75-658">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="c3c75-659">Bytte namn på parametern TenantId i cmdleten Connect-AzAccount till Tenant och lade till ett alias för TenantId</span><span class="sxs-lookup"><span data-stu-id="c3c75-659">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="c3c75-660">Uppdaterade TenantId-beskrivningen för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="c3c75-660">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="c3c75-661">Åtgärda felmeddelande för misslyckad inloggning när du tillhandahåller klientdomän</span><span class="sxs-lookup"><span data-stu-id="c3c75-661">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="c3c75-662">Åtgärda problem med att kontextnamn hamnar i konflikt för konton utan prenumerationer i klientorganisationen</span><span class="sxs-lookup"><span data-stu-id="c3c75-662">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="c3c75-663">Åtgärda problem med DataLake-slutpunkter vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="c3c75-663">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="c3c75-664">Åtgärdade problem med att Disconnect-AzAccount kastades om den inte anslöts</span><span class="sxs-lookup"><span data-stu-id="c3c75-664">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="c3c75-665">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="c3c75-665">Az.CognitiveServices</span></span>
* <span data-ttu-id="c3c75-666">Lade till åtgärden Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="c3c75-666">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c3c75-667">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c3c75-667">Az.Compute</span></span>
* <span data-ttu-id="c3c75-668">Lade till cmdletarna Add-AzVmssVMDataDisk och Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="c3c75-668">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="c3c75-669">Get-AzVMImage visar AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="c3c75-669">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="c3c75-670">Åtgärdade att värdena för alternativen SetAzVMChefExtension -BootstrapOptions och -JsonAttribute inte angavs i json-format.</span><span class="sxs-lookup"><span data-stu-id="c3c75-670">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="c3c75-671">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c3c75-671">Az.DataLakeStore</span></span>
* <span data-ttu-id="c3c75-672">Uppdatera DataLake-paketet till 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="c3c75-672">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="c3c75-673">Lägg till standardsamtidighet för flertrådade åtgärder.</span><span class="sxs-lookup"><span data-stu-id="c3c75-673">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="c3c75-674">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="c3c75-674">Az.Insights</span></span>
* <span data-ttu-id="c3c75-675">Åtgärdade problem #7267 (autoskalningsområde)</span><span class="sxs-lookup"><span data-stu-id="c3c75-675">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="c3c75-676">Problem med att uppräknade parametrar inte ställdes in ordentligt när du skapade en ny autoskalningsregel (de ställdes alltid in med standardvärdet).</span><span class="sxs-lookup"><span data-stu-id="c3c75-676">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="c3c75-677">Åtgärdade problem #7513 [Insights] Set-AzDiagnosticSetting kräver uttrycklig specifikation av kategorier när inställningar skapas</span><span class="sxs-lookup"><span data-stu-id="c3c75-677">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="c3c75-678">Nu kräver inte cmdleten uttrycklig anvisning av kategorierna för att aktiveras under skapande, d.v.s. den fungerar enligt beskrivning</span><span class="sxs-lookup"><span data-stu-id="c3c75-678">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c3c75-679">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c3c75-679">Az.Network</span></span>
* <span data-ttu-id="c3c75-680">PeeringType ändrades till en obligatorisk parameter för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="c3c75-680">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="c3c75-681">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="c3c75-681">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="c3c75-682">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="c3c75-682">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="c3c75-683">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="c3c75-683">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="c3c75-684">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="c3c75-684">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="c3c75-685">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="c3c75-685">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="c3c75-686">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="c3c75-686">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="c3c75-687">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="c3c75-687">Az.PolicyInsights</span></span>
* <span data-ttu-id="c3c75-688">Cmdletar för principreparation har lagts till</span><span class="sxs-lookup"><span data-stu-id="c3c75-688">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="c3c75-689">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c3c75-689">Az.Resources</span></span>
* <span data-ttu-id="c3c75-690">Korrigering för https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="c3c75-690">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="c3c75-691">Tillåt att resurser listas med parametern -ResourceId för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="c3c75-691">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="c3c75-692">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c3c75-692">Az.ServiceBus</span></span>
* <span data-ttu-id="c3c75-693">Skrivskyddad MigrationState-egenskap har lagts till i PSServiceBusMigrationConfigurationAttributes, som hjälper till att hålla koll på migreringstillståndet.</span><span class="sxs-lookup"><span data-stu-id="c3c75-693">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="c3c75-694">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c3c75-694">Az.ServiceFabric</span></span>
* <span data-ttu-id="c3c75-695">Åtgärda att lägga till certifikat till Linux-Vmss.</span><span class="sxs-lookup"><span data-stu-id="c3c75-695">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="c3c75-696">Åtgärdade Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="c3c75-696">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="c3c75-697">Använd rätt tumavtryck från nya certifikat (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="c3c75-697">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="c3c75-698">Visa undantag korrekt (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="c3c75-698">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="c3c75-699">Åtgärdade Update-AzServiceFabricDurability så att klusterkonfigurationen uppdateras innan Vmss-åtgärden CreateOrUpdate påbörjas.</span><span class="sxs-lookup"><span data-stu-id="c3c75-699">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="c3c75-700">0.4.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="c3c75-700">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="c3c75-701">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="c3c75-701">Az.Profile</span></span>
* <span data-ttu-id="c3c75-702">Åtgärdade problemet med Get-AzSubscription i CloudShell</span><span class="sxs-lookup"><span data-stu-id="c3c75-702">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="c3c75-703">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="c3c75-703">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c3c75-704">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c3c75-704">Az.Compute</span></span>
* <span data-ttu-id="c3c75-705">Nya storlekar lades till i listan över godkända VM-storlekar för vilka accelererat nätverk kommer att aktiveras vid användning av den enkla parameteruppsättningen för New-AzVm</span><span class="sxs-lookup"><span data-stu-id="c3c75-705">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="c3c75-706">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="c3c75-706">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="c3c75-707">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c3c75-707">Az.DataLakeStore</span></span>
* <span data-ttu-id="c3c75-708">Lägger till stöd för regler för virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="c3c75-708">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="c3c75-709">Get-AzDataLakeStoreVirtualNetworkRule: Hämtar eller listar regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c3c75-709">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="c3c75-710">Add-AzDataLakeStoreVirtualNetworkRule: Lägger till en regel för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="c3c75-710">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="c3c75-711">Set-AzDataLakeStoreVirtualNetworkRule: Ändrar den angivna regeln för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="c3c75-711">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="c3c75-712">Remove-AzDataLakeStoreVirtualNetworkRule: Tar bort en regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c3c75-712">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c3c75-713">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c3c75-713">Az.Network</span></span>
* <span data-ttu-id="c3c75-714">Skicka protokollvärdet till serverdelen för att uppdatera cmdleten Test-AzNetworkWatcherConnectivity.</span><span class="sxs-lookup"><span data-stu-id="c3c75-714">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="c3c75-715">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="c3c75-715">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="c3c75-716">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c3c75-716">Az.Resources</span></span>
* <span data-ttu-id="c3c75-717">Åtgärdade problem där Get-AzRoleDefinition genererar ett oläsligt undantag (när standardprofilen inte innehåller någon prenumeration och ingen omfattning har angetts) genom att lägga till ett beskrivande undantag i scenariot.</span><span class="sxs-lookup"><span data-stu-id="c3c75-717">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="c3c75-718">Ställ in ”RoleDefinitionNameParameterSet” som standardparameteruppsättning.</span><span class="sxs-lookup"><span data-stu-id="c3c75-718">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="c3c75-719">0.3.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="c3c75-719">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="c3c75-720">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="c3c75-720">Azure.Storage</span></span>
* <span data-ttu-id="c3c75-721">Åtgärda fel där Kopiera blob/fil inte kopierar metadata när målplatsen har ett problem med metadata</span><span class="sxs-lookup"><span data-stu-id="c3c75-721">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="c3c75-722">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="c3c75-722">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="c3c75-723">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="c3c75-723">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="c3c75-724">Stöd för att hämta användningsinformation om en Storage-resurs för en specifik plats och för att lägga till ett varningsmeddelande för att hämta användningsinformation om en global Storage-resurs är inaktuellt.</span><span class="sxs-lookup"><span data-stu-id="c3c75-724">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="c3c75-725">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="c3c75-725">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="c3c75-726">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="c3c75-726">Az.CognitiveServices</span></span>
* <span data-ttu-id="c3c75-727">Stöd för Get-AzCognitiveServicesAccountSkus utan ett befintligt konto.</span><span class="sxs-lookup"><span data-stu-id="c3c75-727">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c3c75-728">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c3c75-728">Az.Compute</span></span>
* <span data-ttu-id="c3c75-729">Åtgärdade fel där Get-AzVM -ResourceGroupName <rg> returnerar fler än 50 resultat om det behövs</span><span class="sxs-lookup"><span data-stu-id="c3c75-729">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="c3c75-730">Lade till ett exempel för SimpleParameterSet i hjälpen för cmdleten New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="c3c75-730">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="c3c75-731">Ett stavfel i förloppsmeddelandet för Azure Disk Encryption har korrigerats</span><span class="sxs-lookup"><span data-stu-id="c3c75-731">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="c3c75-732">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="c3c75-732">Az.DataFactoryV2</span></span>
* <span data-ttu-id="c3c75-733">ADF .Net SDK-versionen har uppdaterats till 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="c3c75-733">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c3c75-734">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c3c75-734">Az.Network</span></span>
* <span data-ttu-id="c3c75-735">Funktionalitet för NetworkProfile har lagts till.</span><span class="sxs-lookup"><span data-stu-id="c3c75-735">Added NetworkProfile functionality.</span></span> <span data-ttu-id="c3c75-736">nya cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="c3c75-736">new cmdlets added</span></span>
    - <span data-ttu-id="c3c75-737">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c3c75-737">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="c3c75-738">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c3c75-738">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="c3c75-739">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c3c75-739">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="c3c75-740">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c3c75-740">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="c3c75-741">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="c3c75-741">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="c3c75-742">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="c3c75-742">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="c3c75-743">Länk för tjänstassociering på modell för undernät har lagts till</span><span class="sxs-lookup"><span data-stu-id="c3c75-743">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="c3c75-744">Cmdletarna New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap och Remove-AzVirtualNetworkTap har lagts till</span><span class="sxs-lookup"><span data-stu-id="c3c75-744">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="c3c75-745">Cmdletarna Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig och Remove-AzNEtworkInterfaceTapConfig har lagts till</span><span class="sxs-lookup"><span data-stu-id="c3c75-745">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="c3c75-746">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="c3c75-746">Az.RedisCache</span></span>
* <span data-ttu-id="c3c75-747">Tillåt att alla strängar används som storleksparametrar framöver.</span><span class="sxs-lookup"><span data-stu-id="c3c75-747">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="c3c75-748">Lägg till P5 i popup-fönstret PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="c3c75-748">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="c3c75-749">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c3c75-749">Az.Resources</span></span>
* <span data-ttu-id="c3c75-750">Parametern -Mode som saknades i Set-AzPolicyDefinition har lagts till</span><span class="sxs-lookup"><span data-stu-id="c3c75-750">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="c3c75-751">Åtgärdade buggen för cmdleten Get-AzProviderOperation för åtgärder med ursprung som innehåller användare</span><span class="sxs-lookup"><span data-stu-id="c3c75-751">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="c3c75-752">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c3c75-752">Az.Sql</span></span>
* <span data-ttu-id="c3c75-753">Ett problem där vissa cmdletar för säkerhetskopiering inte kunde identifiera den aktuella azure-prenumerationen har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="c3c75-753">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c3c75-754">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c3c75-754">Az.Websites</span></span>
* <span data-ttu-id="c3c75-755">Ny cmdlet: Get-AzWebAppContainerContinuousDeploymentUrl – Hämtar webhook-URL:en för kontinuerlig distribution av container</span><span class="sxs-lookup"><span data-stu-id="c3c75-755">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="c3c75-756">Nya cmdletar: New-AzWebAppContainerPSSession och Enter-WebAppContainerPSSession – Startar en PowerShell-fjärrsession i en containerapp för windows</span><span class="sxs-lookup"><span data-stu-id="c3c75-756">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="c3c75-757">0.2.0 – september 2018</span><span class="sxs-lookup"><span data-stu-id="c3c75-757">0.2.0 - September 2018</span></span>
 <span data-ttu-id="c3c75-758">Första versionen</span><span class="sxs-lookup"><span data-stu-id="c3c75-758">Initial Release</span></span>