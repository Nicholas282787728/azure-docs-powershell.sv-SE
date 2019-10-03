---
title: Viktig information om Azure PowerShell
description: Lär dig mer om alla de senaste uppdateringarna för Azure PowerShell-modulerna.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 04/30/2019
ms.openlocfilehash: 8a9a399f72ed9e3e9a3cbc09c8a4abaa91339c24
ms.sourcegitcommit: f0f09eee03ef9dd7fe07432252a3dc8ca93e3a7b
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/27/2019
ms.locfileid: "71319293"
---
## <a name="180---april-2019"></a><span data-ttu-id="8282f-103">1.8.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="8282f-103">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="8282f-104">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="8282f-104">Highlights since the last major release</span></span>
* <span data-ttu-id="8282f-105">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="8282f-105">General availability of `Az` module</span></span>
* <span data-ttu-id="8282f-106">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="8282f-106">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="8282f-107">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="8282f-107">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="8282f-108">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="8282f-108">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="8282f-109">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="8282f-109">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="8282f-110">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="8282f-110">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="8282f-111">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="8282f-111">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="8282f-112">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8282f-112">Az.Accounts</span></span>
* <span data-ttu-id="8282f-113">Uppdatera Uninstall-AzureRm för att ta bort moduler i Mac på ett korrekt sätt</span><span class="sxs-lookup"><span data-stu-id="8282f-113">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="8282f-114">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="8282f-114">Az.Batch</span></span>
* <span data-ttu-id="8282f-115">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8282f-115">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="8282f-116">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="8282f-116">Az.Cdn</span></span>
* <span data-ttu-id="8282f-117">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8282f-117">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="8282f-118">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8282f-118">Az.CognitiveServices</span></span>
* <span data-ttu-id="8282f-119">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8282f-119">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8282f-120">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8282f-120">Az.Compute</span></span>
* <span data-ttu-id="8282f-121">Åtgärda problem med AEM-installationen om resurs-ID:n för diskar innehåller resourcegroups i gemener i resurs-ID:n</span><span class="sxs-lookup"><span data-stu-id="8282f-121">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="8282f-122">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8282f-122">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8282f-123">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="8282f-123">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8282f-124">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8282f-124">Az.DataFactory</span></span>
* <span data-ttu-id="8282f-125">Lägg till SsisProperties om NodeCount inte är null för hanterad integreringskörning.</span><span class="sxs-lookup"><span data-stu-id="8282f-125">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8282f-126">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8282f-126">Az.DataLakeStore</span></span>
* <span data-ttu-id="8282f-127">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8282f-127">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="8282f-128">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="8282f-128">Az.EventGrid</span></span>
* <span data-ttu-id="8282f-129">Hjälptexten för slutpunkten har uppdaterats för att visa att resurser ska skapas innan cmdletarna för att skapa/uppdatera händelseprenumerationer används.</span><span class="sxs-lookup"><span data-stu-id="8282f-129">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="8282f-130">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8282f-130">Az.EventHub</span></span>
* <span data-ttu-id="8282f-131">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="8282f-131">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="8282f-132">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8282f-132">Az.HDInsight</span></span>
* <span data-ttu-id="8282f-133">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8282f-133">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8282f-134">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8282f-134">Az.IotHub</span></span>
* <span data-ttu-id="8282f-135">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8282f-135">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8282f-136">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8282f-136">Az.KeyVault</span></span>
* <span data-ttu-id="8282f-137">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8282f-137">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8282f-138">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="8282f-138">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="8282f-139">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="8282f-139">Az.MachineLearning</span></span>
* <span data-ttu-id="8282f-140">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8282f-140">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="8282f-141">Az.Media</span><span class="sxs-lookup"><span data-stu-id="8282f-141">Az.Media</span></span>
* <span data-ttu-id="8282f-142">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8282f-142">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8282f-143">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8282f-143">Az.Monitor</span></span>
  * <span data-ttu-id="8282f-144">Nya cmdletar för måttbaserad aviseringsregel i GenV2 (inte klassisk)</span><span class="sxs-lookup"><span data-stu-id="8282f-144">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="8282f-145">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="8282f-145">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="8282f-146">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="8282f-146">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="8282f-147">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="8282f-147">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="8282f-148">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="8282f-148">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="8282f-149">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="8282f-149">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="8282f-150">Monitor SDK har uppdaterats till version 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="8282f-150">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8282f-151">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8282f-151">Az.Network</span></span>
* <span data-ttu-id="8282f-152">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8282f-152">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8282f-153">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="8282f-153">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="8282f-154">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="8282f-154">Az.NotificationHubs</span></span>
* <span data-ttu-id="8282f-155">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8282f-155">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8282f-156">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8282f-156">Az.OperationalInsights</span></span>
* <span data-ttu-id="8282f-157">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8282f-157">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="8282f-158">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="8282f-158">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="8282f-159">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8282f-159">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8282f-160">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8282f-160">Az.RecoveryServices</span></span>
* <span data-ttu-id="8282f-161">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8282f-161">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8282f-162">Tabellformatet för SQL i virtuella Azure-datorer har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="8282f-162">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="8282f-163">En alternativ metod för att hämta platser i AzureFileShare har lagts till</span><span class="sxs-lookup"><span data-stu-id="8282f-163">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="8282f-164">ScheduleRunDays i SchedulePolicy-objekt har uppdaterats enligt tidszon</span><span class="sxs-lookup"><span data-stu-id="8282f-164">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="8282f-165">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="8282f-165">Az.RedisCache</span></span>
* <span data-ttu-id="8282f-166">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8282f-166">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8282f-167">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8282f-167">Az.Resources</span></span>
* <span data-ttu-id="8282f-168">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="8282f-168">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="8282f-169">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8282f-169">Az.Sql</span></span>
* <span data-ttu-id="8282f-170">Ersätt Monitor SDK-beroende med vanlig kod</span><span class="sxs-lookup"><span data-stu-id="8282f-170">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="8282f-171">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8282f-171">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8282f-172">Förbättrad process för klassificering av flera kolumner.</span><span class="sxs-lookup"><span data-stu-id="8282f-172">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="8282f-173">Inkludera SKU-egenskaper (SKU-namn, serie, kapacitet) i svaret från Get-AzSqlServerServiceObjective och formatera som tabell som standard.</span><span class="sxs-lookup"><span data-stu-id="8282f-173">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="8282f-174">Möjlighet att använda Get-AzSqlServerServiceObjective efter plats utan att behöva en redan befintlig server i regionen.</span><span class="sxs-lookup"><span data-stu-id="8282f-174">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="8282f-175">Stöd för tidszonsparametern när hanterade instanser skapas.</span><span class="sxs-lookup"><span data-stu-id="8282f-175">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="8282f-176">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="8282f-176">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8282f-177">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8282f-177">Az.Websites</span></span>
* <span data-ttu-id="8282f-178">åtgärdar Set-AzWebApp och Set-AzWebAppSlot så att de inte tar bort taggar vid körning</span><span class="sxs-lookup"><span data-stu-id="8282f-178">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="8282f-179">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8282f-179">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8282f-180">SDK för WebSites har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="8282f-180">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="8282f-181">Egenskapen AdminSiteName har tagits bort från PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="8282f-181">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="8282f-182">1.7.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="8282f-182">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="8282f-183">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="8282f-183">Highlights since the last major release</span></span>
* <span data-ttu-id="8282f-184">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="8282f-184">General availability of `Az` module</span></span>
* <span data-ttu-id="8282f-185">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="8282f-185">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="8282f-186">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="8282f-186">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="8282f-187">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="8282f-187">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="8282f-188">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="8282f-188">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="8282f-189">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="8282f-189">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="8282f-190">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="8282f-190">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="8282f-191">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8282f-191">Az.Accounts</span></span>
* <span data-ttu-id="8282f-192">Add-AzEnvironment och Set-AzEnvironment har uppdaterats för att godkänna parametern AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="8282f-192">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="8282f-193">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8282f-193">Az.AnalysisServices</span></span>
* <span data-ttu-id="8282f-194">ServiceClient används i cmdletar för dataplan och den ursprungliga autentiseringslogiken har tagits bort</span><span class="sxs-lookup"><span data-stu-id="8282f-194">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="8282f-195">Add-AzureASAccount används för omslutning av Connect-AzAccount för att undvika en icke-bakåtkompatibel ändring</span><span class="sxs-lookup"><span data-stu-id="8282f-195">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8282f-196">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8282f-196">Az.Automation</span></span>
* <span data-ttu-id="8282f-197">Buggen för cmdleten New-AzAutomationSoftwareUpdateConfiguration för inkluderingar har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="8282f-197">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="8282f-198">Nu bör parametern IncludedKbNumber och IncludedPackageNameMask fungera.</span><span class="sxs-lookup"><span data-stu-id="8282f-198">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="8282f-199">Felkorrigering för dynamiska grupper i uppdateringshanteringen för azure automation</span><span class="sxs-lookup"><span data-stu-id="8282f-199">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8282f-200">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8282f-200">Az.Compute</span></span>
* <span data-ttu-id="8282f-201">Lägg till parametern HyperVGeneration i New-AzDiskConfig och New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="8282f-201">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="8282f-202">Tillåt att virtuella datorer skapas med galleribilder från andra klientorganisationer.</span><span class="sxs-lookup"><span data-stu-id="8282f-202">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="8282f-203">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="8282f-203">Az.ContainerInstance</span></span>
* <span data-ttu-id="8282f-204">Ett problem har åtgärdats i parametern -Command för New-AzContainerGroup som lade till ett avslutande tomt argument</span><span class="sxs-lookup"><span data-stu-id="8282f-204">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8282f-205">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8282f-205">Az.DataFactory</span></span>
* <span data-ttu-id="8282f-206">ADF .Net SDK-versionen har uppdaterats till 3.0.2</span><span class="sxs-lookup"><span data-stu-id="8282f-206">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="8282f-207">Cmdleten Set-AzDataFactoryV2 har uppdaterats med extra parametrar för inställningar som rör RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="8282f-207">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8282f-208">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8282f-208">Az.Resources</span></span>
* <span data-ttu-id="8282f-209">Förbättra hanteringen av providrar för Get-AzResource när parametrarna -ResourceId eller -ResourceGroupName, -Name och -ResourceType tillhandahålls</span><span class="sxs-lookup"><span data-stu-id="8282f-209">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="8282f-210">Förbättra felhanteringen för ”Test-AzDeployment” och ”Test-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="8282f-210">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="8282f-211">Hantera fel utanför distributionsvalideringen och ta med dem i kommandoutdata istället</span><span class="sxs-lookup"><span data-stu-id="8282f-211">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="8282f-212">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="8282f-212">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="8282f-213">Lägg till växlingsparametern -IgnoreDynamicParameters till en uppsättning av cmdletar för distribution för att hoppa över fråga i skript och jobbscenarier</span><span class="sxs-lookup"><span data-stu-id="8282f-213">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="8282f-214">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="8282f-214">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="8282f-215">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8282f-215">Az.Sql</span></span>
* <span data-ttu-id="8282f-216">Stöd för dataklassificering av databaser.</span><span class="sxs-lookup"><span data-stu-id="8282f-216">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8282f-217">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8282f-217">Az.Storage</span></span>
* <span data-ttu-id="8282f-218">Rapportera detaljfel när lagringskontext skapas med parametern -UseConnectedAccount, men utan inloggning på Azure-kontot</span><span class="sxs-lookup"><span data-stu-id="8282f-218">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="8282f-219">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="8282f-219">New-AzStorageContext</span></span>
* <span data-ttu-id="8282f-220">Stöd för att hantera Blob Service-egenskaper för ett angivet lagringskonto med API:et för hanteringsplan</span><span class="sxs-lookup"><span data-stu-id="8282f-220">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="8282f-221">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="8282f-221">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="8282f-222">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="8282f-222">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="8282f-223">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8282f-223">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="8282f-224">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8282f-224">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="8282f-225">Stöd för -AsJob-cmdletar för att ladda upp och ladda ned blobar och filer</span><span class="sxs-lookup"><span data-stu-id="8282f-225">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="8282f-226">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="8282f-226">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="8282f-227">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="8282f-227">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="8282f-228">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="8282f-228">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="8282f-229">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="8282f-229">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="8282f-230">1.6.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="8282f-230">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="8282f-231">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="8282f-231">Highlights since the last major release</span></span>
* <span data-ttu-id="8282f-232">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="8282f-232">General availability of `Az` module</span></span>
* <span data-ttu-id="8282f-233">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="8282f-233">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="8282f-234">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="8282f-234">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="8282f-235">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="8282f-235">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="8282f-236">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="8282f-236">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="8282f-237">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="8282f-237">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="8282f-238">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="8282f-238">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8282f-239">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8282f-239">Az.Automation</span></span>
* <span data-ttu-id="8282f-240">Azure Automation – ändring av uppdateringshantering för stöd för de nya funktionerna:</span><span class="sxs-lookup"><span data-stu-id="8282f-240">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="8282f-241">Dynamisk gruppering</span><span class="sxs-lookup"><span data-stu-id="8282f-241">Dynamic grouping</span></span>
    * <span data-ttu-id="8282f-242">För-/efterskrift</span><span class="sxs-lookup"><span data-stu-id="8282f-242">Pre-Post script</span></span>
    * <span data-ttu-id="8282f-243">Inställning för omstart</span><span class="sxs-lookup"><span data-stu-id="8282f-243">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8282f-244">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8282f-244">Az.Compute</span></span>
* <span data-ttu-id="8282f-245">Åtgärda problem med sökvägsmatchning i Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="8282f-245">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="8282f-246">Uppdatera Compute-klientbibliotek till 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="8282f-246">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8282f-247">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8282f-247">Az.KeyVault</span></span>
* <span data-ttu-id="8282f-248">Stöd för jokertecken för KeyVault-cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="8282f-248">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8282f-249">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8282f-249">Az.Network</span></span>
* <span data-ttu-id="8282f-250">Lägg till stöd för Threat Intelligence för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="8282f-250">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="8282f-251">Lägg till resurs för brandväggsprincip på översta nivå och anpassade regler för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="8282f-251">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8282f-252">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8282f-252">Az.RecoveryServices</span></span>
* <span data-ttu-id="8282f-253">SnapshotRetentionInDays har lagts till i Azure-principen för virtuella datorer för stöd av Instant RP</span><span class="sxs-lookup"><span data-stu-id="8282f-253">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="8282f-254">Pipe-stöd för avregistrering av container har lagts till</span><span class="sxs-lookup"><span data-stu-id="8282f-254">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="8282f-255">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8282f-255">Az.Resources</span></span>
* <span data-ttu-id="8282f-256">Uppdatera stöd för jokertecken för Get-AzResource och Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8282f-256">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="8282f-257">Uppdatera autentiseringsuppgifter som används vid allmänna anrop till ARM</span><span class="sxs-lookup"><span data-stu-id="8282f-257">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="8282f-258">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8282f-258">Az.Sql</span></span>
* <span data-ttu-id="8282f-259">Cmdlet-parametern (ExcludeDetectionType) för Hotidentifiering ändrades från DetectionType till sträng[] för att framtidssäkra den när nya DetectionTypes läggs till, och även för att stödja automatisk ifyllning.</span><span class="sxs-lookup"><span data-stu-id="8282f-259">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8282f-260">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8282f-260">Az.Storage</span></span>
* <span data-ttu-id="8282f-261">Stöd för att hämta/ange/ta bort hanteringsprincip på ett lagringskonto</span><span class="sxs-lookup"><span data-stu-id="8282f-261">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="8282f-262">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="8282f-262">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="8282f-263">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="8282f-263">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="8282f-264">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="8282f-264">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="8282f-265">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="8282f-265">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="8282f-266">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="8282f-266">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="8282f-267">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="8282f-267">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8282f-268">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8282f-268">Az.Websites</span></span>
* <span data-ttu-id="8282f-269">Åtgärda fel med ARM-mall som avbryter kloning av alla platser med 'New-AzWebApp -IncludeSourceWebAppSlots'</span><span class="sxs-lookup"><span data-stu-id="8282f-269">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="8282f-270">1.5.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="8282f-270">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8282f-271">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8282f-271">Az.Accounts</span></span>
* <span data-ttu-id="8282f-272">Lägg till kommandot Register-AzModule för stöd för AutoRest-genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="8282f-272">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="8282f-273">Uppdatera exempel för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="8282f-273">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8282f-274">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8282f-274">Az.Automation</span></span>
* <span data-ttu-id="8282f-275">Problem med att hämta vissa månadsscheman i flera Azure Automation-cmdletar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8282f-275">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="8282f-276">Åtgärda problem med att Get-AzAutomationDscNode bara returnerar de 20 översta noderna.</span><span class="sxs-lookup"><span data-stu-id="8282f-276">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="8282f-277">Nu returneras alla noder</span><span class="sxs-lookup"><span data-stu-id="8282f-277">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="8282f-278">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="8282f-278">Az.Cdn</span></span>
* <span data-ttu-id="8282f-279">Nya Powershell-cmdletar för att aktivera/inaktivera anpassade domän-HTTPS har lagts till och de gamla har gjorts inaktuella</span><span class="sxs-lookup"><span data-stu-id="8282f-279">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8282f-280">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8282f-280">Az.Compute</span></span>
* <span data-ttu-id="8282f-281">Lägg till stöd för jokertecken för Get-cmdletar</span><span class="sxs-lookup"><span data-stu-id="8282f-281">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8282f-282">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8282f-282">Az.DataFactory</span></span>
* <span data-ttu-id="8282f-283">ADF .Net SDK-versionen har uppdaterats till 3.0.1</span><span class="sxs-lookup"><span data-stu-id="8282f-283">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="8282f-284">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="8282f-284">Az.LogicApp</span></span>
* <span data-ttu-id="8282f-285">Åtgärda problemet med att ListWorkflows endast hämtar den första sidan med resultat</span><span class="sxs-lookup"><span data-stu-id="8282f-285">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8282f-286">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8282f-286">Az.Network</span></span>
* <span data-ttu-id="8282f-287">Lägg till stöd för jokertecken för Network-cmdletar</span><span class="sxs-lookup"><span data-stu-id="8282f-287">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8282f-288">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8282f-288">Az.RecoveryServices</span></span>
* <span data-ttu-id="8282f-289">Stöd har lagts till för SQL Server i virtuella Azure-datorer</span><span class="sxs-lookup"><span data-stu-id="8282f-289">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="8282f-290">SDK-uppdatering</span><span class="sxs-lookup"><span data-stu-id="8282f-290">SDK Update</span></span>
* <span data-ttu-id="8282f-291">Get-ProtectableItem-incheckning i VMappContainer har tagits bort</span><span class="sxs-lookup"><span data-stu-id="8282f-291">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="8282f-292">Name och ServerName har lagts till som parametrar för Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="8282f-292">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="8282f-293">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8282f-293">Az.Resources</span></span>
* <span data-ttu-id="8282f-294">Lägg till parametern `-TemplateObject` i cmdletar för distribution</span><span class="sxs-lookup"><span data-stu-id="8282f-294">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="8282f-295">Mer information här: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="8282f-295">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="8282f-296">Åtgärda problem med piping av resultatet i `Get-AzResource` till `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="8282f-296">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="8282f-297">Mer information här: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="8282f-297">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="8282f-298">Åtgärda problem med ändring av JSON-datatyp när `Set-AzResource` körs</span><span class="sxs-lookup"><span data-stu-id="8282f-298">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="8282f-299">Mer information här: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="8282f-299">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="8282f-300">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8282f-300">Az.Sql</span></span>
* <span data-ttu-id="8282f-301">AuditingEndpointsCommunicator uppdateras.</span><span class="sxs-lookup"><span data-stu-id="8282f-301">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="8282f-302">Åtgärdar beteendet hos ett gränsscenario när nya diagnostikinställningar skapas.</span><span class="sxs-lookup"><span data-stu-id="8282f-302">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8282f-303">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8282f-303">Az.Storage</span></span>
* <span data-ttu-id="8282f-304">Stöd för BlockBlobStorage när Storage-konto skapas      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8282f-304">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="8282f-305">1.4.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="8282f-305">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="8282f-306">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8282f-306">Az.AnalysisServices</span></span>
* <span data-ttu-id="8282f-307">Inaktuell AddAzureASAccount-cmdlet</span><span class="sxs-lookup"><span data-stu-id="8282f-307">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8282f-308">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8282f-308">Az.Automation</span></span>
* <span data-ttu-id="8282f-309">Hjälpen för Import-AzAutomationDscNodeConfiguration har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="8282f-309">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="8282f-310">Konfigurationsnamnsvalidering har lagts till i cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="8282f-310">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="8282f-311">Förbättrad felhantering för cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="8282f-311">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="8282f-312">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8282f-312">Az.CognitiveServices</span></span>
* <span data-ttu-id="8282f-313">CustomSubdomainName har lagts till som en ny valfri parameter för New-AzCognitiveServicesAccount, som används för att ange underdomän för resursen.</span><span class="sxs-lookup"><span data-stu-id="8282f-313">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8282f-314">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8282f-314">Az.Compute</span></span>
* <span data-ttu-id="8282f-315">Problemet med ID-parameteruppsättningar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8282f-315">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="8282f-316">Get-AzVMExtension har uppdaterats så att alla installerade tillägg visas om parametern Name inte har angetts</span><span class="sxs-lookup"><span data-stu-id="8282f-316">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="8282f-317">Parametrarna Tag och ResourceId har lagts till i cmdleten Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="8282f-317">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="8282f-318">Get-AzVmssVM utan instans-ID och med InstanceView kan visa virtuella VMSS-datorer med instansvyn.</span><span class="sxs-lookup"><span data-stu-id="8282f-318">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8282f-319">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8282f-319">Az.DataLakeStore</span></span>
* <span data-ttu-id="8282f-320">Cmdletar har lagts till för uppräkning och återställning av borttagna objekt i ADL</span><span class="sxs-lookup"><span data-stu-id="8282f-320">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="8282f-321">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8282f-321">Az.EventHub</span></span>
* <span data-ttu-id="8282f-322">Ny boolesk egenskap SkipEmptyArchives har lagts till i Skip Empty Archives i CaptureDescription-klassen i Eventhub</span><span class="sxs-lookup"><span data-stu-id="8282f-322">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="8282f-323">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8282f-323">Az.KeyVault</span></span>
* <span data-ttu-id="8282f-324">Taggning i Set-AzKeyVaultSecret har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8282f-324">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="8282f-325">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="8282f-325">Az.LogicApp</span></span>
* <span data-ttu-id="8282f-326">Grundläggande SKU har lagts till för Integrationskonton</span><span class="sxs-lookup"><span data-stu-id="8282f-326">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="8282f-327">XSLT 2.0, XSLT 3.0 och Flytande mappningstyper har lagts till</span><span class="sxs-lookup"><span data-stu-id="8282f-327">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="8282f-328">Nya cmdletar för integrationskontosammansättningar</span><span class="sxs-lookup"><span data-stu-id="8282f-328">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="8282f-329">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="8282f-329">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="8282f-330">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="8282f-330">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="8282f-331">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="8282f-331">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="8282f-332">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="8282f-332">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="8282f-333">Nya cmdletar för batchkonfiguration för integrationskonto</span><span class="sxs-lookup"><span data-stu-id="8282f-333">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="8282f-334">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="8282f-334">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="8282f-335">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="8282f-335">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="8282f-336">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="8282f-336">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="8282f-337">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="8282f-337">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="8282f-338">Logic App-SDK har uppdaterats till version 4.1.0</span><span class="sxs-lookup"><span data-stu-id="8282f-338">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8282f-339">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8282f-339">Az.Monitor</span></span>
* <span data-ttu-id="8282f-340">Hjälpen för Get-AzMetric har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="8282f-340">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8282f-341">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8282f-341">Az.Network</span></span>
* <span data-ttu-id="8282f-342">Hjälpexempel för Add-AzApplicationGatewayCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="8282f-342">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8282f-343">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8282f-343">Az.OperationalInsights</span></span>
* <span data-ttu-id="8282f-344">Ytterligare stöd för datakällorna New och Get ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="8282f-344">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="8282f-345">Ny ApplicationInsights-typ har lagts till för att ge stöd för ”Get specific” och ”Get all” för ApplicationInsights-datakällor för angiven arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="8282f-345">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="8282f-346">Cmdleten New-AzOperationalInsightsApplicationInsightsDataSource har lagts till för att skapa datakälla med angivna parametrar för Application Insights-resurs: subscription Id, resourceGroupName och name.</span><span class="sxs-lookup"><span data-stu-id="8282f-346">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="8282f-347">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8282f-347">Az.Resources</span></span>
* <span data-ttu-id="8282f-348">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="8282f-348">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="8282f-349">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="8282f-349">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="8282f-350">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="8282f-350">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="8282f-351">Fel som gör att KeyCredentials inte kan skapas upprepade gånger har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8282f-351">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="8282f-352">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8282f-352">Az.Sql</span></span>
* <span data-ttu-id="8282f-353">Lägg till stöd för hyperskalanivån för SQL DB</span><span class="sxs-lookup"><span data-stu-id="8282f-353">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="8282f-354">Ett fel har åtgärdats där återställningen kunde misslyckas på grund av onödiga inställningsegenskaper i restore-förfrågan</span><span class="sxs-lookup"><span data-stu-id="8282f-354">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8282f-355">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8282f-355">Az.Websites</span></span>
* <span data-ttu-id="8282f-356">Rätt exempel i Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="8282f-356">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="8282f-357">1.3.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="8282f-357">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8282f-358">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8282f-358">Az.Accounts</span></span>
* <span data-ttu-id="8282f-359">Uppdatera till den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="8282f-359">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="8282f-360">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8282f-360">Az.AnalysisServices</span></span>
<span data-ttu-id="8282f-361">Allmän tillgänglighet för Az.AnalysisServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="8282f-361">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8282f-362">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8282f-362">Az.Compute</span></span>
* <span data-ttu-id="8282f-363">AEM-tillägg: Lägg till stöd för UltraSSD-, P60-, P70- och P80-diskar</span><span class="sxs-lookup"><span data-stu-id="8282f-363">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="8282f-364">Uppdatera hjälpbeskrivning för Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="8282f-364">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="8282f-365">Uppdatera hjälpbeskrivning och exempel för Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="8282f-365">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8282f-366">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8282f-366">Az.RecoveryServices</span></span>
<span data-ttu-id="8282f-367">Allmän tillgänglighet för Az.RecoveryServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="8282f-367">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8282f-368">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8282f-368">Az.Resources</span></span>
* <span data-ttu-id="8282f-369">Korrigera taggar för resursgrupper</span><span class="sxs-lookup"><span data-stu-id="8282f-369">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="8282f-370">Mer information här: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="8282f-370">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="8282f-371">Åtgärda problem där `Get-AzureRmRoleAssignment` inte respekterar -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="8282f-371">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="8282f-372">Mer information här: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="8282f-372">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="8282f-373">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8282f-373">Az.Sql</span></span>
* <span data-ttu-id="8282f-374">Lägga till Get/Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8282f-374">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="8282f-375">Åtgärda problem där ett nullref-undantag uppstår när du kör SQL-cmdletar och inte är inloggad på ett Azure-konto</span><span class="sxs-lookup"><span data-stu-id="8282f-375">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="8282f-376">Åtgärda nullref-undantag i Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="8282f-376">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="8282f-377">1.2.1 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="8282f-377">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8282f-378">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8282f-378">Az.Accounts</span></span>
* <span data-ttu-id="8282f-379">Version med rätt version av autentisering</span><span class="sxs-lookup"><span data-stu-id="8282f-379">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="8282f-380">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8282f-380">Az.AnalysisServices</span></span>
* <span data-ttu-id="8282f-381">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="8282f-381">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8282f-382">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8282f-382">Az.RecoveryServices</span></span>
* <span data-ttu-id="8282f-383">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="8282f-383">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="8282f-384">1.2.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="8282f-384">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8282f-385">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8282f-385">Az.Accounts</span></span>
* <span data-ttu-id="8282f-386">Lägga till interaktiv autentisering och autentisering med användarnamn/lösenord för endast Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="8282f-386">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="8282f-387">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="8282f-387">Update incorrect online help URLs</span></span>
* <span data-ttu-id="8282f-388">Lägga till varningsmeddelande i PS Core för Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="8282f-388">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="8282f-389">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="8282f-389">Az.Aks</span></span>
* <span data-ttu-id="8282f-390">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="8282f-390">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8282f-391">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8282f-391">Az.Automation</span></span>
* <span data-ttu-id="8282f-392">Stöd för Python 2-runbookflöden har lagts till</span><span class="sxs-lookup"><span data-stu-id="8282f-392">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="8282f-393">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="8282f-393">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="8282f-394">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="8282f-394">Az.Cdn</span></span>
* <span data-ttu-id="8282f-395">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="8282f-395">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8282f-396">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8282f-396">Az.Compute</span></span>
* <span data-ttu-id="8282f-397">Lägga till cmdleten Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="8282f-397">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="8282f-398">Lägga till TempDisk-parameter i Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8282f-398">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="8282f-399">Korrigera varningsmeddelande för New-AzVM</span><span class="sxs-lookup"><span data-stu-id="8282f-399">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="8282f-400">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8282f-400">Az.ContainerRegistry</span></span>
* <span data-ttu-id="8282f-401">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="8282f-401">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8282f-402">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8282f-402">Az.DataFactory</span></span>
* <span data-ttu-id="8282f-403">ADF .Net SDK-versionen har uppdaterats till 3.0.0</span><span class="sxs-lookup"><span data-stu-id="8282f-403">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8282f-404">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8282f-404">Az.DataLakeStore</span></span>
* <span data-ttu-id="8282f-405">Åtgärda problem med ADLS-slutpunkt vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="8282f-405">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="8282f-406">Mer information här: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="8282f-406">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="8282f-407">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="8282f-407">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8282f-408">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8282f-408">Az.IotHub</span></span>
* <span data-ttu-id="8282f-409">Lägga till kodningsformat i cmdleten Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="8282f-409">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8282f-410">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8282f-410">Az.KeyVault</span></span>
* <span data-ttu-id="8282f-411">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="8282f-411">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8282f-412">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8282f-412">Az.Network</span></span>
* <span data-ttu-id="8282f-413">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="8282f-413">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="8282f-414">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8282f-414">Az.Resources</span></span>
* <span data-ttu-id="8282f-415">Åtgärda felaktiga exempel i referensdokumentationen ”New-AzADAppCredential” och ”New-AzADSpCredential”</span><span class="sxs-lookup"><span data-stu-id="8282f-415">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="8282f-416">Åtgärda problem där sökvägen för parametern ”-TemplateFile” inte omvandlas innan cmdletarna för distribution i resursgruppen körs</span><span class="sxs-lookup"><span data-stu-id="8282f-416">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="8282f-417">Az.Resources: Korrigera dokumentationen om standardvärdet för New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="8282f-417">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="8282f-418">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="8282f-418">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="8282f-419">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="8282f-419">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="8282f-420">Åtgärda formateringsproblemet med objektet ”PSResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="8282f-420">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="8282f-421">Mer information här: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="8282f-421">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8282f-422">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8282f-422">Az.ServiceFabric</span></span>
* <span data-ttu-id="8282f-423">Återställ när ett certifikat läggs till i en Virtual Machine Scale Sets-modell men ett undantag genereras. Detta har gjorts för att åtgärda följande fel: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="8282f-423">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="8282f-424">Korrigera några felmeddelanden.</span><span class="sxs-lookup"><span data-stu-id="8282f-424">Fix some error messages.</span></span>
* <span data-ttu-id="8282f-425">Korrigering av skapande av kluster med ARM-mall som är standard för New-AzServiceFabriCluster som inte fungerade med migrering till Az.</span><span class="sxs-lookup"><span data-stu-id="8282f-425">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="8282f-426">Korrigering av tilläggning av kluster/programcertifikat så att endast VM Scale Sets som motsvarar klustret läggs till genom att kontrollera ID för klustret i tillägget.</span><span class="sxs-lookup"><span data-stu-id="8282f-426">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="8282f-427">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="8282f-427">Az.SignalR</span></span>
* <span data-ttu-id="8282f-428">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="8282f-428">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="8282f-429">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8282f-429">Az.Sql</span></span>
* <span data-ttu-id="8282f-430">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="8282f-430">Update incorrect online help URLs</span></span>
* <span data-ttu-id="8282f-431">Uppdaterad parameterbeskrivning för LicenseType-parameter med möjliga värden</span><span class="sxs-lookup"><span data-stu-id="8282f-431">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="8282f-432">Korrigering för att uppdatera hanterad instansidentitet som inte fungerar när det är den enda uppdaterade egenskapen</span><span class="sxs-lookup"><span data-stu-id="8282f-432">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="8282f-433">Stöd för anpassad sortering på hanterad instans</span><span class="sxs-lookup"><span data-stu-id="8282f-433">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8282f-434">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8282f-434">Az.Storage</span></span>
* <span data-ttu-id="8282f-435">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="8282f-435">Update incorrect online help URLs</span></span>
* <span data-ttu-id="8282f-436">Tillhandahåll detaljerat felmeddelande när en användare försöker hämta/konfigurera klassisk loggning/mått på ett Premium Storage-konto eftersom Premium Storage-kontot inte har stöd för klassisk loggning/mått.</span><span class="sxs-lookup"><span data-stu-id="8282f-436">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="8282f-437">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="8282f-437">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="8282f-438">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="8282f-438">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="8282f-439">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="8282f-439">Az.TrafficManager</span></span>
* <span data-ttu-id="8282f-440">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="8282f-440">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8282f-441">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8282f-441">Az.Websites</span></span>
* <span data-ttu-id="8282f-442">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="8282f-442">Update incorrect online help URLs</span></span>
* <span data-ttu-id="8282f-443">Korrigerar ”New-AzWebAppSSLBinding” så att certifikatet laddas upp till rätt resursgrupp och plats om appen finns i en ASE.</span><span class="sxs-lookup"><span data-stu-id="8282f-443">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="8282f-444">Korrigerar ”New-AzWebAppSSLBinding” så att taggarna inte skrivs över på en bindning av ett SSL-certifikat till en app</span><span class="sxs-lookup"><span data-stu-id="8282f-444">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="8282f-445">1.1.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="8282f-445">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8282f-446">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8282f-446">Az.Accounts</span></span>
* <span data-ttu-id="8282f-447">Lade till omfattningen ”Lokal” till Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="8282f-447">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8282f-448">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8282f-448">Az.Compute</span></span>
* <span data-ttu-id="8282f-449">Namn är nu valfritt i ID-parametern för Restart/Start/Stop/Remove/Set-AzVM och Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="8282f-449">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="8282f-450">Uppdaterade beskrivningen av ID i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="8282f-450">Updated the description of ID in help files</span></span>
* <span data-ttu-id="8282f-451">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8282f-451">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8282f-452">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8282f-452">Az.DataLakeStore</span></span>
* <span data-ttu-id="8282f-453">Uppdatera sdk-versionen av dataplanet till 1.1.14 för SDK-korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="8282f-453">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="8282f-454">Korrigerade hanteringen av negativ accesstime och modificationtime för getfilestatus och liststatus; korrigera asynkront annulleringstoken</span><span class="sxs-lookup"><span data-stu-id="8282f-454">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="8282f-455">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="8282f-455">Az.EventGrid</span></span>
* <span data-ttu-id="8282f-456">Uppdaterat för användning av API-versionen 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="8282f-456">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="8282f-457">Uppdaterade följande cmdletar för att stödja nytt scenario i API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="8282f-457">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="8282f-458">New-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="8282f-458">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="8282f-459">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="8282f-459">Event Time-To-Live,</span></span>
        - <span data-ttu-id="8282f-460">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="8282f-460">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="8282f-461">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="8282f-461">Dead letter endpoint.</span></span>
    - <span data-ttu-id="8282f-462">Update-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="8282f-462">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="8282f-463">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="8282f-463">Event Time-To-Live,</span></span>
        - <span data-ttu-id="8282f-464">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="8282f-464">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="8282f-465">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="8282f-465">Dead letter endpoint.</span></span>
* <span data-ttu-id="8282f-466">Lade till nya enum-värden (storageQueue och hybridConnection) för alternativet EndpointType i cmdletarna New-AzureRmEventGridSubscription och Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="8282f-466">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="8282f-467">Visa varningsmeddelanden om skapande eller uppdatering av händelseprenumerationen förväntas medföra manuell åtgärd från användaren.</span><span class="sxs-lookup"><span data-stu-id="8282f-467">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8282f-468">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8282f-468">Az.IotHub</span></span>
* <span data-ttu-id="8282f-469">Har uppdaterats till den senaste versionen av SDK:n lotHub</span><span class="sxs-lookup"><span data-stu-id="8282f-469">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="8282f-470">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="8282f-470">Az.LogicApp</span></span>
* <span data-ttu-id="8282f-471">Get-AzLogicApp visar en lista över alla som inte har angivet namn</span><span class="sxs-lookup"><span data-stu-id="8282f-471">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="8282f-472">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8282f-472">Az.Resources</span></span>
* <span data-ttu-id="8282f-473">Åtgärdade problem med parameteruppsättningen när parametrarna -ODataQuery och -ResourceId anges för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="8282f-473">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="8282f-474">Mer information här: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="8282f-474">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="8282f-475">Åtgärdade hantering av parametern -Custom i New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8282f-475">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="8282f-476">Korrigerade stavfel i New-AzDeployment-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="8282f-476">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="8282f-477">Gjorde parametern -MailNickname obligatorisk för New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="8282f-477">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="8282f-478">Mer information här: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="8282f-478">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="8282f-479">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="8282f-479">Az.SignalR</span></span>
* <span data-ttu-id="8282f-480">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8282f-480">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="8282f-481">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8282f-481">Az.Sql</span></span>
* <span data-ttu-id="8282f-482">Konverterade lagringshanteringsklientens beroende av den normala SDK-implementeringen.</span><span class="sxs-lookup"><span data-stu-id="8282f-482">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8282f-483">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8282f-483">Az.Storage</span></span>
* <span data-ttu-id="8282f-484">Angav StorageAccountName för lagringskontext som det verkliga namnet på lagringskontot när det skapas med Sas Token, OAuth eller Anonymous</span><span class="sxs-lookup"><span data-stu-id="8282f-484">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="8282f-485">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="8282f-485">New-AzStorageContext</span></span>
* <span data-ttu-id="8282f-486">Skapade Sas Token för Blob Snapshot-objekt med parametern -FullUri, åtgärdade den returnerade URI:n så att den blir URI för ögonblicksbild</span><span class="sxs-lookup"><span data-stu-id="8282f-486">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="8282f-487">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="8282f-487">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8282f-488">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8282f-488">Az.Websites</span></span>
* <span data-ttu-id="8282f-489">Åtgärdade en bugg i datumparsningen i Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="8282f-489">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="8282f-490">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8282f-490">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="8282f-491">1.0.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="8282f-491">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="8282f-492">Allmänt</span><span class="sxs-lookup"><span data-stu-id="8282f-492">General</span></span>

- <span data-ttu-id="8282f-493">Allmän tillgänglighet för Az-modulen</span><span class="sxs-lookup"><span data-stu-id="8282f-493">General Availability of Az Module</span></span>
- <span data-ttu-id="8282f-494">Onlinehjälp för varje modul</span><span class="sxs-lookup"><span data-stu-id="8282f-494">Online help for each module</span></span>
- <span data-ttu-id="8282f-495">Mer information och en översikt finns på [Az-informationssidan](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="8282f-495">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="8282f-496">Information om hur du migrerar från AzureRM finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8282f-496">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="8282f-497">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8282f-497">Az.Accounts</span></span>
- <span data-ttu-id="8282f-498">Har ändrats från Az.Profile</span><span class="sxs-lookup"><span data-stu-id="8282f-498">Changed from Az.Profile</span></span>
- <span data-ttu-id="8282f-499">Fasta tabellformat för profil- och kontexttyper</span><span class="sxs-lookup"><span data-stu-id="8282f-499">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="8282f-500">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8282f-500">Az.ApiManagement</span></span>
- <span data-ttu-id="8282f-501">Korrigeringar för #7002</span><span class="sxs-lookup"><span data-stu-id="8282f-501">Fixes for #7002</span></span>
- <span data-ttu-id="8282f-502">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8282f-502">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="8282f-503">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="8282f-503">Az.Batch</span></span>
- <span data-ttu-id="8282f-504">Lade till möjligheten att se vilken version av Azure Batch Node Agent som körs på var och en av de virtuella datorerna i en pool, via den nya egenskapen `NodeAgentInformation` på `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="8282f-504">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="8282f-505">Standarden `Caching` för `PSDataDisk` är nu `ReadWrite` i stället för `None`.</span><span class="sxs-lookup"><span data-stu-id="8282f-505">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="8282f-506">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8282f-506">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="8282f-507">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="8282f-507">Az.Billing</span></span>
- <span data-ttu-id="8282f-508">Kombinerar cmdletarna för fakturering, förbrukning och UsageAggregates. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8282f-508">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="8282f-509">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="8282f-509">Az.CognitivServices</span></span>
- <span data-ttu-id="8282f-510">Lade till kompletterare för SkuName och Typem som är tillgängliga i New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="8282f-510">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="8282f-511">Tog bort parameteruppsättningen GetSkusWithAccountParamSetName från Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="8282f-511">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="8282f-512">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="8282f-512">Az.ContainerInstance</span></span>
- <span data-ttu-id="8282f-513">Stöd för ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="8282f-513">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="8282f-514">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="8282f-514">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="8282f-515">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8282f-515">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="8282f-516">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8282f-516">Az.DataLakeStore</span></span>
- <span data-ttu-id="8282f-517">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8282f-517">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="8282f-518">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8282f-518">Az.Monitor</span></span>
- <span data-ttu-id="8282f-519">Döpte om Az.Insights till Az.Monitor och andra mindre icke-bakåtkompatibla ändringar. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8282f-519">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="8282f-520">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8282f-520">Az.KeyVault</span></span>
- <span data-ttu-id="8282f-521">Tog bort den inaktuella egenskapen PurgeDisabled från utdatatyper</span><span class="sxs-lookup"><span data-stu-id="8282f-521">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="8282f-522">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="8282f-522">Az.MachineLearning</span></span>
- <span data-ttu-id="8282f-523">Inkluderade cmdletarna från modulen Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="8282f-523">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="8282f-524">Az.Media</span><span class="sxs-lookup"><span data-stu-id="8282f-524">Az.Media</span></span>
- <span data-ttu-id="8282f-525">Tog bort inaktuella -Tags-alias från New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="8282f-525">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="8282f-526">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8282f-526">Az.Network</span></span>
<span data-ttu-id="8282f-527">Stöd har lagts till för konfiguration av RewriteRuleSets i Application Gateway</span><span class="sxs-lookup"><span data-stu-id="8282f-527">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="8282f-528">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="8282f-528">New cmdlets added:</span></span>
        - <span data-ttu-id="8282f-529">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8282f-529">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="8282f-530">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8282f-530">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="8282f-531">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8282f-531">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="8282f-532">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8282f-532">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="8282f-533">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8282f-533">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="8282f-534">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="8282f-534">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="8282f-535">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="8282f-535">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="8282f-536">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="8282f-536">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="8282f-537">Cmdletar har uppdaterats med den valfria parametern -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8282f-537">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="8282f-538">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8282f-538">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="8282f-539">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="8282f-539">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="8282f-540">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="8282f-540">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="8282f-541">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8282f-541">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="8282f-542">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="8282f-542">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="8282f-543">New-AzureRmApplicationGatewayUrlPathMapConfig har lagt till KeyVault-stöd för Application Gateway med Identity.</span><span class="sxs-lookup"><span data-stu-id="8282f-543">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="8282f-544">Cmdletar har uppdaterats med den valfria parametern -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="8282f-544">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="8282f-545">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8282f-545">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="8282f-546">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8282f-546">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="8282f-547">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8282f-547">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="8282f-548">Cmdleten New-AzApplicationGateway har uppdaterats med den valfria parametern -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="8282f-548">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="8282f-549">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8282f-549">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="8282f-550">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8282f-550">Az.OperationalInsights</span></span>
- <span data-ttu-id="8282f-551">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8282f-551">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="8282f-552">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="8282f-552">Az.Profile</span></span>
- <span data-ttu-id="8282f-553">Modulnamnet har ändrats till Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8282f-553">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="8282f-554">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8282f-554">Az.RecoveryServices</span></span>
- <span data-ttu-id="8282f-555">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8282f-555">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="8282f-556">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8282f-556">Az.Resources</span></span>
- <span data-ttu-id="8282f-557">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8282f-557">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="8282f-558">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8282f-558">Az.ServiceFabric</span></span>
- <span data-ttu-id="8282f-559">Stöd för specificering av certifikat efter eget namn och tumavtryck</span><span class="sxs-lookup"><span data-stu-id="8282f-559">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="8282f-560">Information om fler icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8282f-560">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="8282f-561">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="8282f-561">Az.SIgnalR</span></span>
- <span data-ttu-id="8282f-562">Allmän tillgänglighet för PowerShell-cmdletar för SIgnalR</span><span class="sxs-lookup"><span data-stu-id="8282f-562">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="8282f-563">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8282f-563">Az.Sql</span></span>
- <span data-ttu-id="8282f-564">Lade till de nya identifieringstyperna Data_Exfiltration och Unsafe_Action i Threat Detection-cmdletar</span><span class="sxs-lookup"><span data-stu-id="8282f-564">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="8282f-565">Uppdaterade dokumentationsexempel för Sql Auditing-cmdletar</span><span class="sxs-lookup"><span data-stu-id="8282f-565">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="8282f-566">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8282f-566">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="8282f-567">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8282f-567">Az.Storage</span></span>
- <span data-ttu-id="8282f-568">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8282f-568">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="8282f-569">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8282f-569">Az.Websites</span></span>
- <span data-ttu-id="8282f-570">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8282f-570">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="8282f-571">0.7.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="8282f-571">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="8282f-572">Allmänt</span><span class="sxs-lookup"><span data-stu-id="8282f-572">General</span></span>

* <span data-ttu-id="8282f-573">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="8282f-573">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="8282f-574">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8282f-574">Az.Compute</span></span>

* <span data-ttu-id="8282f-575">Lade till stöd för UltraSSD och Galleriavbildningar i de enkla parameteruppsättningarna för `New-AzVm(ss)`-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="8282f-575">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="8282f-576">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8282f-576">Az.DataLakeStore</span></span>

* <span data-ttu-id="8282f-577">Åtgärdade avslutande snedstreck i domänen för adls-konto</span><span class="sxs-lookup"><span data-stu-id="8282f-577">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="8282f-578">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="8282f-578">Az.FrontDoor</span></span>

* <span data-ttu-id="8282f-579">Brutna länkar korrigerades</span><span class="sxs-lookup"><span data-stu-id="8282f-579">Fixed some broken links</span></span>
    - <span data-ttu-id="8282f-580">I artiklarna New-AzureRmFrontDoor och Set-AzureRmFrontDoor artiklar korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="8282f-580">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="8282f-581">I artikeln New-AzureRmFrontDoorManagedRuleObject korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="8282f-581">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="8282f-582">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8282f-582">Az.RecoveryServices</span></span>

* <span data-ttu-id="8282f-583">Lade till valideringar på klientsidan för Azure-filresurs med återställningsåtgärder.</span><span class="sxs-lookup"><span data-stu-id="8282f-583">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="8282f-584">Gjorde storageAccountName och storageAccountResourceGroupName valfritt för afs-återställning.</span><span class="sxs-lookup"><span data-stu-id="8282f-584">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="8282f-585">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8282f-585">Az.Resources</span></span>

* <span data-ttu-id="8282f-586">Korrigering för https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="8282f-586">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="8282f-587">Uppdaterade Get-AzureRmRoleAssignment så att prenumerationsomfattningen används om den anges vid begäran om klassiska administratörer.</span><span class="sxs-lookup"><span data-stu-id="8282f-587">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="8282f-588">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8282f-588">Az.Sql</span></span>

* <span data-ttu-id="8282f-589">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="8282f-589">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="8282f-590">Korrigerade ett problem med Get-AzureRmSqlDatabaseVulnerabilityAssessment med DotNet-kärna</span><span class="sxs-lookup"><span data-stu-id="8282f-590">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="8282f-591">Ändrade dokumentationen för hjälpmeddelanden som rör SQL Auditing-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="8282f-591">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="8282f-592">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8282f-592">Az.Storage</span></span>

* <span data-ttu-id="8282f-593">Lade till -EnableHierarchicalNamespace i New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8282f-593">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="8282f-594">Åtgärdade problemet med att cmdleten Copy File inte kunde återanvända källkontexten på målet om inte -DestContext angetts</span><span class="sxs-lookup"><span data-stu-id="8282f-594">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="8282f-595">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="8282f-595">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="8282f-596">Stöd för statisk webbplatskonfiguration</span><span class="sxs-lookup"><span data-stu-id="8282f-596">Support Static Website configuration</span></span>
    - <span data-ttu-id="8282f-597">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="8282f-597">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="8282f-598">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="8282f-598">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="8282f-599">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8282f-599">Az.Websites</span></span>

* <span data-ttu-id="8282f-600">Set-AzureRmWebApp och Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8282f-600">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="8282f-601">Ny parameter (-AzureStoragePath) har lagts till för att ange att Azure Storage-sökvägar ska monteras i containerappar i Windows och Linux.</span><span class="sxs-lookup"><span data-stu-id="8282f-601">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="8282f-602">Använder utdata från den nya cmdleten New-AzureRmWebAppAzureStoragePath som en parameter för att ange sökvägar för Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="8282f-602">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="8282f-603">0.6.1 – november 2018</span><span class="sxs-lookup"><span data-stu-id="8282f-603">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="8282f-604">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8282f-604">Az.ApiManagement</span></span>
* <span data-ttu-id="8282f-605">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="8282f-605">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="8282f-606">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8282f-606">Az.Automation</span></span>
* <span data-ttu-id="8282f-607">Swagger baserade Azure Automation-cmdletar</span><span class="sxs-lookup"><span data-stu-id="8282f-607">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="8282f-608">Cmdletar för Uppdateringshantering har lagts till</span><span class="sxs-lookup"><span data-stu-id="8282f-608">Added Update Management cmdlets</span></span>
* <span data-ttu-id="8282f-609">Cmdletar för källkontroll har lagts till</span><span class="sxs-lookup"><span data-stu-id="8282f-609">Added Source Control cmdlets</span></span>
* <span data-ttu-id="8282f-610">Remove-AzureRmAutomationHybridWorkerGroup-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="8282f-610">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="8282f-611">Kommandot för DSC-registreringsnod har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8282f-611">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="8282f-612">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8282f-612">Az.Compute</span></span>
* <span data-ttu-id="8282f-613">Problem med SystemAssigned-identitet har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8282f-613">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="8282f-614">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="8282f-614">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="8282f-615">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="8282f-615">Az.ContainerInstance</span></span>
* <span data-ttu-id="8282f-616">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="8282f-616">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="8282f-617">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="8282f-617">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="8282f-618">uppdatera exempelbeskrivningen för marketplace-cmdletar</span><span class="sxs-lookup"><span data-stu-id="8282f-618">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="8282f-619">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8282f-619">Az.Network</span></span>
* <span data-ttu-id="8282f-620">Cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomErreller Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="8282f-620">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="8282f-621">ICMP tillbaka till stöd för Azure Firewall-nätverksprotokoll har lagts till</span><span class="sxs-lookup"><span data-stu-id="8282f-621">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="8282f-622">Uppdatera cmdlet Test-AzureRmNetworkWatcherConnectivity, lägga till verifiering av mål-id, adress och port.</span><span class="sxs-lookup"><span data-stu-id="8282f-622">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="8282f-623">Åtgärda problem med minnesanvändning i VirtualNetwork-karta</span><span class="sxs-lookup"><span data-stu-id="8282f-623">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="8282f-624">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="8282f-624">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="8282f-625">Åtgärda för att ändra principen för en skyddad fildelning.</span><span class="sxs-lookup"><span data-stu-id="8282f-625">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="8282f-626">Tidszonsprincipen har konverterats till versaler.</span><span class="sxs-lookup"><span data-stu-id="8282f-626">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="8282f-627">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="8282f-627">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="8282f-628">Exempel i New-AzureRmRecoveryServicesAsrProtectableItem har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8282f-628">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="8282f-629">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="8282f-629">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="8282f-630">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="8282f-630">Az.Relay</span></span>
* <span data-ttu-id="8282f-631">Valfri parameter -KeyValue till New-AzureRmRelayKey cmdlet har lagts till, vilket gör det möjligt för användare att tillhandahålla KeyValue.</span><span class="sxs-lookup"><span data-stu-id="8282f-631">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="8282f-632">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8282f-632">Az.Resources</span></span>
* <span data-ttu-id="8282f-633">Uppdatera hjälpdokumentation för resursidentitet kopplad till parametrar i `New-AzureRmPolicyAssignment` och `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="8282f-633">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="8282f-634">Lägg till ett exempel för New-AzureRmPolicyDefinition som använder -Metadata</span><span class="sxs-lookup"><span data-stu-id="8282f-634">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="8282f-635">Korrigera så att skiftläge behålls i taggnycklar i NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="8282f-635">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="8282f-636">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8282f-636">Az.ServiceFabric</span></span>
* <span data-ttu-id="8282f-637">Lägg till utfasningsmeddelanden för kommande icke-kompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="8282f-637">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="8282f-638">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8282f-638">Az.Sql</span></span>
* <span data-ttu-id="8282f-639">Nya cmdletar för CRUD-åtgärder på Azure Sql Database-hanterad instans och Azure Sql-hanterad databas</span><span class="sxs-lookup"><span data-stu-id="8282f-639">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="8282f-640">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="8282f-640">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="8282f-641">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="8282f-641">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="8282f-642">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="8282f-642">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="8282f-643">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="8282f-643">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="8282f-644">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="8282f-644">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="8282f-645">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="8282f-645">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="8282f-646">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="8282f-646">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="8282f-647">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="8282f-647">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="8282f-648">Hantering av utökad granskningsprincip på en server eller en databas har aktiverats.</span><span class="sxs-lookup"><span data-stu-id="8282f-648">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="8282f-649">Ny parameter (PredicateExpression) har lagts till för att aktivera filtrering av granskningsloggar.</span><span class="sxs-lookup"><span data-stu-id="8282f-649">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="8282f-650">Cmdletar har ändrats så att de använder SQL-klienter i stället för äldre klienter.</span><span class="sxs-lookup"><span data-stu-id="8282f-650">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="8282f-651">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="8282f-651">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="8282f-652">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="8282f-652">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="8282f-653">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="8282f-653">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="8282f-654">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="8282f-654">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="8282f-655">Problem med att använda Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings med lagringskontots namnparameter har korrigerats</span><span class="sxs-lookup"><span data-stu-id="8282f-655">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="8282f-656">0.5.0 – november 2018</span><span class="sxs-lookup"><span data-stu-id="8282f-656">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="8282f-657">Allmänt</span><span class="sxs-lookup"><span data-stu-id="8282f-657">General</span></span>
* <span data-ttu-id="8282f-658">Lade till resurskompletterare till många kärn-cmdletar – dessa gör att du kan stega genom befintliga resursnamn med TABB vid interaktiva anrop till cmdletar</span><span class="sxs-lookup"><span data-stu-id="8282f-658">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="8282f-659">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="8282f-659">Az.Profile</span></span>
* <span data-ttu-id="8282f-660">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="8282f-660">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="8282f-661">Bytte namn på parametern TenantId i cmdleten Connect-AzAccount till Tenant och lade till ett alias för TenantId</span><span class="sxs-lookup"><span data-stu-id="8282f-661">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="8282f-662">Uppdaterade TenantId-beskrivningen för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="8282f-662">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="8282f-663">Åtgärda felmeddelande för misslyckad inloggning när du tillhandahåller klientdomän</span><span class="sxs-lookup"><span data-stu-id="8282f-663">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="8282f-664">Åtgärda problem med att kontextnamn hamnar i konflikt för konton utan prenumerationer i klientorganisationen</span><span class="sxs-lookup"><span data-stu-id="8282f-664">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="8282f-665">Åtgärda problem med DataLake-slutpunkter vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="8282f-665">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="8282f-666">Åtgärdade problem med att Disconnect-AzAccount kastades om den inte anslöts</span><span class="sxs-lookup"><span data-stu-id="8282f-666">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="8282f-667">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8282f-667">Az.CognitiveServices</span></span>
* <span data-ttu-id="8282f-668">Lade till åtgärden Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="8282f-668">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8282f-669">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8282f-669">Az.Compute</span></span>
* <span data-ttu-id="8282f-670">Lade till cmdletarna Add-AzVmssVMDataDisk och Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="8282f-670">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="8282f-671">Get-AzVMImage visar AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="8282f-671">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="8282f-672">Åtgärdade att värdena för alternativen SetAzVMChefExtension -BootstrapOptions och -JsonAttribute inte angavs i json-format.</span><span class="sxs-lookup"><span data-stu-id="8282f-672">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8282f-673">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8282f-673">Az.DataLakeStore</span></span>
* <span data-ttu-id="8282f-674">Uppdatera DataLake-paketet till 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="8282f-674">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="8282f-675">Lägg till standardsamtidighet för flertrådade åtgärder.</span><span class="sxs-lookup"><span data-stu-id="8282f-675">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="8282f-676">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="8282f-676">Az.Insights</span></span>
* <span data-ttu-id="8282f-677">Åtgärdade problem #7267 (autoskalningsområde)</span><span class="sxs-lookup"><span data-stu-id="8282f-677">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="8282f-678">Problem med att uppräknade parametrar inte ställdes in ordentligt när du skapade en ny autoskalningsregel (de ställdes alltid in med standardvärdet).</span><span class="sxs-lookup"><span data-stu-id="8282f-678">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="8282f-679">Åtgärdade problem #7513 [Insights] Set-AzDiagnosticSetting kräver uttrycklig specifikation av kategorier när inställningar skapas</span><span class="sxs-lookup"><span data-stu-id="8282f-679">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="8282f-680">Nu kräver inte cmdleten uttrycklig anvisning av kategorierna för att aktiveras under skapande, d.v.s. den fungerar enligt beskrivning</span><span class="sxs-lookup"><span data-stu-id="8282f-680">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8282f-681">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8282f-681">Az.Network</span></span>
* <span data-ttu-id="8282f-682">PeeringType ändrades till en obligatorisk parameter för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="8282f-682">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="8282f-683">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="8282f-683">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="8282f-684">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="8282f-684">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="8282f-685">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="8282f-685">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="8282f-686">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="8282f-686">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="8282f-687">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="8282f-687">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="8282f-688">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="8282f-688">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="8282f-689">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="8282f-689">Az.PolicyInsights</span></span>
* <span data-ttu-id="8282f-690">Cmdletar för principreparation har lagts till</span><span class="sxs-lookup"><span data-stu-id="8282f-690">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="8282f-691">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8282f-691">Az.Resources</span></span>
* <span data-ttu-id="8282f-692">Korrigering för https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="8282f-692">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="8282f-693">Tillåt att resurser listas med parametern -ResourceId för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="8282f-693">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="8282f-694">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8282f-694">Az.ServiceBus</span></span>
* <span data-ttu-id="8282f-695">Skrivskyddad MigrationState-egenskap har lagts till i PSServiceBusMigrationConfigurationAttributes, som hjälper till att hålla koll på migreringstillståndet.</span><span class="sxs-lookup"><span data-stu-id="8282f-695">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8282f-696">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8282f-696">Az.ServiceFabric</span></span>
* <span data-ttu-id="8282f-697">Åtgärda att lägga till certifikat till Linux-Vmss.</span><span class="sxs-lookup"><span data-stu-id="8282f-697">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="8282f-698">Åtgärdade Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="8282f-698">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="8282f-699">Använd rätt tumavtryck från nya certifikat (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="8282f-699">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="8282f-700">Visa undantag korrekt (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="8282f-700">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="8282f-701">Åtgärdade Update-AzServiceFabricDurability så att klusterkonfigurationen uppdateras innan Vmss-åtgärden CreateOrUpdate påbörjas.</span><span class="sxs-lookup"><span data-stu-id="8282f-701">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="8282f-702">0.4.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="8282f-702">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="8282f-703">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="8282f-703">Az.Profile</span></span>
* <span data-ttu-id="8282f-704">Åtgärdade problemet med Get-AzSubscription i CloudShell</span><span class="sxs-lookup"><span data-stu-id="8282f-704">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="8282f-705">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="8282f-705">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8282f-706">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8282f-706">Az.Compute</span></span>
* <span data-ttu-id="8282f-707">Nya storlekar lades till i listan över godkända VM-storlekar för vilka accelererat nätverk kommer att aktiveras vid användning av den enkla parameteruppsättningen för New-AzVm</span><span class="sxs-lookup"><span data-stu-id="8282f-707">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="8282f-708">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="8282f-708">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8282f-709">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8282f-709">Az.DataLakeStore</span></span>
* <span data-ttu-id="8282f-710">Lägger till stöd för regler för virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="8282f-710">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="8282f-711">Get-AzDataLakeStoreVirtualNetworkRule: Hämtar eller listar regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8282f-711">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="8282f-712">Add-AzDataLakeStoreVirtualNetworkRule: Lägger till en regel för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="8282f-712">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="8282f-713">Set-AzDataLakeStoreVirtualNetworkRule: Ändrar den angivna regeln för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="8282f-713">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="8282f-714">Remove-AzDataLakeStoreVirtualNetworkRule: Tar bort en regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8282f-714">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8282f-715">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8282f-715">Az.Network</span></span>
* <span data-ttu-id="8282f-716">Skicka protokollvärdet till serverdelen för att uppdatera cmdleten Test-AzNetworkWatcherConnectivity.</span><span class="sxs-lookup"><span data-stu-id="8282f-716">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="8282f-717">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="8282f-717">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8282f-718">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8282f-718">Az.Resources</span></span>
* <span data-ttu-id="8282f-719">Åtgärdade problem där Get-AzRoleDefinition genererar ett oläsligt undantag (när standardprofilen inte innehåller någon prenumeration och ingen omfattning har angetts) genom att lägga till ett beskrivande undantag i scenariot.</span><span class="sxs-lookup"><span data-stu-id="8282f-719">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="8282f-720">Ställ in ”RoleDefinitionNameParameterSet” som standardparameteruppsättning.</span><span class="sxs-lookup"><span data-stu-id="8282f-720">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="8282f-721">0.3.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="8282f-721">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="8282f-722">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="8282f-722">Azure.Storage</span></span>
* <span data-ttu-id="8282f-723">Åtgärda fel där Kopiera blob/fil inte kopierar metadata när målplatsen har ett problem med metadata</span><span class="sxs-lookup"><span data-stu-id="8282f-723">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="8282f-724">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="8282f-724">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="8282f-725">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="8282f-725">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="8282f-726">Stöd för att hämta användningsinformation om en Storage-resurs för en specifik plats och för att lägga till ett varningsmeddelande för att hämta användningsinformation om en global Storage-resurs är inaktuellt.</span><span class="sxs-lookup"><span data-stu-id="8282f-726">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="8282f-727">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="8282f-727">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="8282f-728">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8282f-728">Az.CognitiveServices</span></span>
* <span data-ttu-id="8282f-729">Stöd för Get-AzCognitiveServicesAccountSkus utan ett befintligt konto.</span><span class="sxs-lookup"><span data-stu-id="8282f-729">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8282f-730">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8282f-730">Az.Compute</span></span>
* <span data-ttu-id="8282f-731">Åtgärdade fel där Get-AzVM -ResourceGroupName <rg> returnerar fler än 50 resultat om det behövs</span><span class="sxs-lookup"><span data-stu-id="8282f-731">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="8282f-732">Lade till ett exempel för SimpleParameterSet i hjälpen för cmdleten New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="8282f-732">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="8282f-733">Ett stavfel i förloppsmeddelandet för Azure Disk Encryption har korrigerats</span><span class="sxs-lookup"><span data-stu-id="8282f-733">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="8282f-734">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="8282f-734">Az.DataFactoryV2</span></span>
* <span data-ttu-id="8282f-735">ADF .Net SDK-versionen har uppdaterats till 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="8282f-735">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8282f-736">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8282f-736">Az.Network</span></span>
* <span data-ttu-id="8282f-737">Funktionalitet för NetworkProfile har lagts till.</span><span class="sxs-lookup"><span data-stu-id="8282f-737">Added NetworkProfile functionality.</span></span> <span data-ttu-id="8282f-738">nya cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="8282f-738">new cmdlets added</span></span>
    - <span data-ttu-id="8282f-739">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8282f-739">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="8282f-740">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8282f-740">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="8282f-741">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8282f-741">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="8282f-742">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8282f-742">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="8282f-743">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="8282f-743">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="8282f-744">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="8282f-744">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="8282f-745">Länk för tjänstassociering på modell för undernät har lagts till</span><span class="sxs-lookup"><span data-stu-id="8282f-745">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="8282f-746">Cmdletarna New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap och Remove-AzVirtualNetworkTap har lagts till</span><span class="sxs-lookup"><span data-stu-id="8282f-746">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="8282f-747">Cmdletarna Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig och Remove-AzNEtworkInterfaceTapConfig har lagts till</span><span class="sxs-lookup"><span data-stu-id="8282f-747">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="8282f-748">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="8282f-748">Az.RedisCache</span></span>
* <span data-ttu-id="8282f-749">Tillåt att alla strängar används som storleksparametrar framöver.</span><span class="sxs-lookup"><span data-stu-id="8282f-749">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="8282f-750">Lägg till P5 i popup-fönstret PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="8282f-750">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="8282f-751">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8282f-751">Az.Resources</span></span>
* <span data-ttu-id="8282f-752">Parametern -Mode som saknades i Set-AzPolicyDefinition har lagts till</span><span class="sxs-lookup"><span data-stu-id="8282f-752">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="8282f-753">Åtgärdade buggen för cmdleten Get-AzProviderOperation för åtgärder med ursprung som innehåller användare</span><span class="sxs-lookup"><span data-stu-id="8282f-753">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="8282f-754">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8282f-754">Az.Sql</span></span>
* <span data-ttu-id="8282f-755">Ett problem där vissa cmdletar för säkerhetskopiering inte kunde identifiera den aktuella azure-prenumerationen har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8282f-755">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8282f-756">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8282f-756">Az.Websites</span></span>
* <span data-ttu-id="8282f-757">Ny cmdlet: Get-AzWebAppContainerContinuousDeploymentUrl – Hämtar webhook-URL:en för kontinuerlig distribution av container</span><span class="sxs-lookup"><span data-stu-id="8282f-757">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="8282f-758">Nya cmdletar: New-AzWebAppContainerPSSession och Enter-WebAppContainerPSSession – Startar en PowerShell-fjärrsession i en containerapp för windows</span><span class="sxs-lookup"><span data-stu-id="8282f-758">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="8282f-759">0.2.0 – september 2018</span><span class="sxs-lookup"><span data-stu-id="8282f-759">0.2.0 - September 2018</span></span>
 <span data-ttu-id="8282f-760">Första versionen</span><span class="sxs-lookup"><span data-stu-id="8282f-760">Initial Release</span></span>