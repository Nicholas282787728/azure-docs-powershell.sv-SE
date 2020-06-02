---
title: Viktig information om Azure PowerShell
description: Lär dig mer om alla de senaste uppdateringarna för Azure PowerShell-modulerna.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 04/30/2019
ms.openlocfilehash: 34b21292ccc47bb53b6609cd637ef18338a45cd3
ms.sourcegitcommit: 9f5c7d231b069ad501729bf015a829f3fe89bc6a
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/28/2020
ms.locfileid: "84121461"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="8ef76-103">Viktig information om Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="8ef76-103">Azure PowerShell release notes</span></span>
## <a name="180---april-2019"></a><span data-ttu-id="8ef76-104">1.8.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="8ef76-104">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="8ef76-105">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="8ef76-105">Highlights since the last major release</span></span>
* <span data-ttu-id="8ef76-106">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="8ef76-106">General availability of `Az` module</span></span>
* <span data-ttu-id="8ef76-107">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="8ef76-107">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="8ef76-108">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="8ef76-108">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="8ef76-109">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="8ef76-109">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="8ef76-110">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="8ef76-110">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="8ef76-111">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="8ef76-111">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="8ef76-112">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="8ef76-112">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="8ef76-113">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8ef76-113">Az.Accounts</span></span>
* <span data-ttu-id="8ef76-114">Uppdatera Uninstall-AzureRm för att ta bort moduler i Mac på ett korrekt sätt</span><span class="sxs-lookup"><span data-stu-id="8ef76-114">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="8ef76-115">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="8ef76-115">Az.Batch</span></span>
* <span data-ttu-id="8ef76-116">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8ef76-116">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="8ef76-117">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="8ef76-117">Az.Cdn</span></span>
* <span data-ttu-id="8ef76-118">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8ef76-118">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="8ef76-119">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8ef76-119">Az.CognitiveServices</span></span>
* <span data-ttu-id="8ef76-120">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8ef76-120">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8ef76-121">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8ef76-121">Az.Compute</span></span>
* <span data-ttu-id="8ef76-122">Åtgärda problem med AEM-installationen om resurs-ID:n för diskar innehåller resourcegroups i gemener i resurs-ID:n</span><span class="sxs-lookup"><span data-stu-id="8ef76-122">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="8ef76-123">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8ef76-123">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8ef76-124">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="8ef76-124">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8ef76-125">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8ef76-125">Az.DataFactory</span></span>
* <span data-ttu-id="8ef76-126">Lägg till SsisProperties om NodeCount inte är null för hanterad integreringskörning.</span><span class="sxs-lookup"><span data-stu-id="8ef76-126">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8ef76-127">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8ef76-127">Az.DataLakeStore</span></span>
* <span data-ttu-id="8ef76-128">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8ef76-128">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="8ef76-129">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="8ef76-129">Az.EventGrid</span></span>
* <span data-ttu-id="8ef76-130">Hjälptexten för slutpunkten har uppdaterats för att visa att resurser ska skapas innan cmdletarna för att skapa/uppdatera händelseprenumerationer används.</span><span class="sxs-lookup"><span data-stu-id="8ef76-130">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="8ef76-131">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8ef76-131">Az.EventHub</span></span>
* <span data-ttu-id="8ef76-132">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="8ef76-132">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="8ef76-133">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8ef76-133">Az.HDInsight</span></span>
* <span data-ttu-id="8ef76-134">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8ef76-134">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8ef76-135">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8ef76-135">Az.IotHub</span></span>
* <span data-ttu-id="8ef76-136">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8ef76-136">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8ef76-137">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8ef76-137">Az.KeyVault</span></span>
* <span data-ttu-id="8ef76-138">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8ef76-138">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8ef76-139">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="8ef76-139">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="8ef76-140">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="8ef76-140">Az.MachineLearning</span></span>
* <span data-ttu-id="8ef76-141">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8ef76-141">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="8ef76-142">Az.Media</span><span class="sxs-lookup"><span data-stu-id="8ef76-142">Az.Media</span></span>
* <span data-ttu-id="8ef76-143">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8ef76-143">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8ef76-144">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8ef76-144">Az.Monitor</span></span>
  * <span data-ttu-id="8ef76-145">Nya cmdletar för måttbaserad aviseringsregel i GenV2 (inte klassisk)</span><span class="sxs-lookup"><span data-stu-id="8ef76-145">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="8ef76-146">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="8ef76-146">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="8ef76-147">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="8ef76-147">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="8ef76-148">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="8ef76-148">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="8ef76-149">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="8ef76-149">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="8ef76-150">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="8ef76-150">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="8ef76-151">Monitor SDK har uppdaterats till version 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="8ef76-151">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8ef76-152">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8ef76-152">Az.Network</span></span>
* <span data-ttu-id="8ef76-153">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8ef76-153">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8ef76-154">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="8ef76-154">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="8ef76-155">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="8ef76-155">Az.NotificationHubs</span></span>
* <span data-ttu-id="8ef76-156">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8ef76-156">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8ef76-157">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8ef76-157">Az.OperationalInsights</span></span>
* <span data-ttu-id="8ef76-158">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8ef76-158">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="8ef76-159">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="8ef76-159">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="8ef76-160">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8ef76-160">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8ef76-161">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8ef76-161">Az.RecoveryServices</span></span>
* <span data-ttu-id="8ef76-162">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8ef76-162">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8ef76-163">Tabellformatet för SQL i virtuella Azure-datorer har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="8ef76-163">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="8ef76-164">En alternativ metod för att hämta platser i AzureFileShare har lagts till</span><span class="sxs-lookup"><span data-stu-id="8ef76-164">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="8ef76-165">ScheduleRunDays i SchedulePolicy-objekt har uppdaterats enligt tidszon</span><span class="sxs-lookup"><span data-stu-id="8ef76-165">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="8ef76-166">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="8ef76-166">Az.RedisCache</span></span>
* <span data-ttu-id="8ef76-167">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8ef76-167">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8ef76-168">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8ef76-168">Az.Resources</span></span>
* <span data-ttu-id="8ef76-169">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="8ef76-169">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="8ef76-170">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8ef76-170">Az.Sql</span></span>
* <span data-ttu-id="8ef76-171">Ersätt Monitor SDK-beroende med vanlig kod</span><span class="sxs-lookup"><span data-stu-id="8ef76-171">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="8ef76-172">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8ef76-172">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8ef76-173">Förbättrad process för klassificering av flera kolumner.</span><span class="sxs-lookup"><span data-stu-id="8ef76-173">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="8ef76-174">Inkludera SKU-egenskaper (SKU-namn, serie, kapacitet) i svaret från Get-AzSqlServerServiceObjective och formatera som tabell som standard.</span><span class="sxs-lookup"><span data-stu-id="8ef76-174">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="8ef76-175">Möjlighet att använda Get-AzSqlServerServiceObjective efter plats utan att behöva en redan befintlig server i regionen.</span><span class="sxs-lookup"><span data-stu-id="8ef76-175">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="8ef76-176">Stöd för tidszonsparametern när hanterade instanser skapas.</span><span class="sxs-lookup"><span data-stu-id="8ef76-176">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="8ef76-177">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="8ef76-177">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8ef76-178">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8ef76-178">Az.Websites</span></span>
* <span data-ttu-id="8ef76-179">åtgärdar Set-AzWebApp och Set-AzWebAppSlot så att de inte tar bort taggar vid körning</span><span class="sxs-lookup"><span data-stu-id="8ef76-179">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="8ef76-180">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8ef76-180">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8ef76-181">SDK för WebSites har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="8ef76-181">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="8ef76-182">Egenskapen AdminSiteName har tagits bort från PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="8ef76-182">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="8ef76-183">1.7.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="8ef76-183">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="8ef76-184">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="8ef76-184">Highlights since the last major release</span></span>
* <span data-ttu-id="8ef76-185">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="8ef76-185">General availability of `Az` module</span></span>
* <span data-ttu-id="8ef76-186">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="8ef76-186">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="8ef76-187">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="8ef76-187">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="8ef76-188">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="8ef76-188">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="8ef76-189">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="8ef76-189">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="8ef76-190">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="8ef76-190">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="8ef76-191">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="8ef76-191">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="8ef76-192">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8ef76-192">Az.Accounts</span></span>
* <span data-ttu-id="8ef76-193">Add-AzEnvironment och Set-AzEnvironment har uppdaterats för att godkänna parametern AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="8ef76-193">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="8ef76-194">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8ef76-194">Az.AnalysisServices</span></span>
* <span data-ttu-id="8ef76-195">ServiceClient används i cmdletar för dataplan och den ursprungliga autentiseringslogiken har tagits bort</span><span class="sxs-lookup"><span data-stu-id="8ef76-195">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="8ef76-196">Add-AzureASAccount används för omslutning av Connect-AzAccount för att undvika en icke-bakåtkompatibel ändring</span><span class="sxs-lookup"><span data-stu-id="8ef76-196">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8ef76-197">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8ef76-197">Az.Automation</span></span>
* <span data-ttu-id="8ef76-198">Buggen för cmdleten New-AzAutomationSoftwareUpdateConfiguration för inkluderingar har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="8ef76-198">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="8ef76-199">Nu bör parametern IncludedKbNumber och IncludedPackageNameMask fungera.</span><span class="sxs-lookup"><span data-stu-id="8ef76-199">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="8ef76-200">Felkorrigering för dynamiska grupper i uppdateringshanteringen för azure automation</span><span class="sxs-lookup"><span data-stu-id="8ef76-200">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8ef76-201">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8ef76-201">Az.Compute</span></span>
* <span data-ttu-id="8ef76-202">Lägg till parametern HyperVGeneration i New-AzDiskConfig och New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="8ef76-202">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="8ef76-203">Tillåt att virtuella datorer skapas med galleribilder från andra klientorganisationer.</span><span class="sxs-lookup"><span data-stu-id="8ef76-203">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="8ef76-204">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="8ef76-204">Az.ContainerInstance</span></span>
* <span data-ttu-id="8ef76-205">Ett problem har åtgärdats i parametern -Command för New-AzContainerGroup som lade till ett avslutande tomt argument</span><span class="sxs-lookup"><span data-stu-id="8ef76-205">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8ef76-206">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8ef76-206">Az.DataFactory</span></span>
* <span data-ttu-id="8ef76-207">ADF .Net SDK-versionen har uppdaterats till 3.0.2</span><span class="sxs-lookup"><span data-stu-id="8ef76-207">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="8ef76-208">Cmdleten Set-AzDataFactoryV2 har uppdaterats med extra parametrar för inställningar som rör RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="8ef76-208">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8ef76-209">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8ef76-209">Az.Resources</span></span>
* <span data-ttu-id="8ef76-210">Förbättra hanteringen av providrar för Get-AzResource när parametrarna -ResourceId eller -ResourceGroupName, -Name och -ResourceType tillhandahålls</span><span class="sxs-lookup"><span data-stu-id="8ef76-210">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="8ef76-211">Förbättra felhanteringen för ”Test-AzDeployment” och ”Test-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="8ef76-211">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="8ef76-212">Hantera fel utanför distributionsvalideringen och ta med dem i kommandoutdata istället</span><span class="sxs-lookup"><span data-stu-id="8ef76-212">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="8ef76-213">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="8ef76-213">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="8ef76-214">Lägg till växlingsparametern -IgnoreDynamicParameters till en uppsättning av cmdletar för distribution för att hoppa över fråga i skript och jobbscenarier</span><span class="sxs-lookup"><span data-stu-id="8ef76-214">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="8ef76-215">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="8ef76-215">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="8ef76-216">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8ef76-216">Az.Sql</span></span>
* <span data-ttu-id="8ef76-217">Stöd för dataklassificering av databaser.</span><span class="sxs-lookup"><span data-stu-id="8ef76-217">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8ef76-218">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8ef76-218">Az.Storage</span></span>
* <span data-ttu-id="8ef76-219">Rapportera detaljfel när lagringskontext skapas med parametern -UseConnectedAccount, men utan inloggning på Azure-kontot</span><span class="sxs-lookup"><span data-stu-id="8ef76-219">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="8ef76-220">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="8ef76-220">New-AzStorageContext</span></span>
* <span data-ttu-id="8ef76-221">Stöd för att hantera Blob Service-egenskaper för ett angivet lagringskonto med API:et för hanteringsplan</span><span class="sxs-lookup"><span data-stu-id="8ef76-221">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="8ef76-222">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="8ef76-222">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="8ef76-223">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="8ef76-223">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="8ef76-224">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8ef76-224">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="8ef76-225">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8ef76-225">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="8ef76-226">Stöd för -AsJob-cmdletar för att ladda upp och ladda ned blobar och filer</span><span class="sxs-lookup"><span data-stu-id="8ef76-226">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="8ef76-227">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="8ef76-227">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="8ef76-228">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="8ef76-228">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="8ef76-229">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="8ef76-229">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="8ef76-230">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="8ef76-230">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="8ef76-231">1.6.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="8ef76-231">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="8ef76-232">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="8ef76-232">Highlights since the last major release</span></span>
* <span data-ttu-id="8ef76-233">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="8ef76-233">General availability of `Az` module</span></span>
* <span data-ttu-id="8ef76-234">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="8ef76-234">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="8ef76-235">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="8ef76-235">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="8ef76-236">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="8ef76-236">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="8ef76-237">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="8ef76-237">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="8ef76-238">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="8ef76-238">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="8ef76-239">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="8ef76-239">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8ef76-240">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8ef76-240">Az.Automation</span></span>
* <span data-ttu-id="8ef76-241">Azure Automation – ändring av uppdateringshantering för stöd för de nya funktionerna:</span><span class="sxs-lookup"><span data-stu-id="8ef76-241">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="8ef76-242">Dynamisk gruppering</span><span class="sxs-lookup"><span data-stu-id="8ef76-242">Dynamic grouping</span></span>
    * <span data-ttu-id="8ef76-243">För-/efterskrift</span><span class="sxs-lookup"><span data-stu-id="8ef76-243">Pre-Post script</span></span>
    * <span data-ttu-id="8ef76-244">Inställning för omstart</span><span class="sxs-lookup"><span data-stu-id="8ef76-244">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8ef76-245">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8ef76-245">Az.Compute</span></span>
* <span data-ttu-id="8ef76-246">Åtgärda problem med sökvägsmatchning i Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="8ef76-246">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="8ef76-247">Uppdatera Compute-klientbibliotek till 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="8ef76-247">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8ef76-248">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8ef76-248">Az.KeyVault</span></span>
* <span data-ttu-id="8ef76-249">Stöd för jokertecken för KeyVault-cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="8ef76-249">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8ef76-250">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8ef76-250">Az.Network</span></span>
* <span data-ttu-id="8ef76-251">Lägg till stöd för Threat Intelligence för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="8ef76-251">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="8ef76-252">Lägg till resurs för brandväggsprincip på översta nivå och anpassade regler för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="8ef76-252">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8ef76-253">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8ef76-253">Az.RecoveryServices</span></span>
* <span data-ttu-id="8ef76-254">SnapshotRetentionInDays har lagts till i Azure-principen för virtuella datorer för stöd av Instant RP</span><span class="sxs-lookup"><span data-stu-id="8ef76-254">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="8ef76-255">Pipe-stöd för avregistrering av container har lagts till</span><span class="sxs-lookup"><span data-stu-id="8ef76-255">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="8ef76-256">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8ef76-256">Az.Resources</span></span>
* <span data-ttu-id="8ef76-257">Uppdatera stöd för jokertecken för Get-AzResource och Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8ef76-257">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="8ef76-258">Uppdatera autentiseringsuppgifter som används vid allmänna anrop till ARM</span><span class="sxs-lookup"><span data-stu-id="8ef76-258">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="8ef76-259">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8ef76-259">Az.Sql</span></span>
* <span data-ttu-id="8ef76-260">Cmdlet-parametern (ExcludeDetectionType) för Hotidentifiering ändrades från DetectionType till sträng[] för att framtidssäkra den när nya DetectionTypes läggs till, och även för att stödja automatisk ifyllning.</span><span class="sxs-lookup"><span data-stu-id="8ef76-260">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8ef76-261">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8ef76-261">Az.Storage</span></span>
* <span data-ttu-id="8ef76-262">Stöd för att hämta/ange/ta bort hanteringsprincip på ett lagringskonto</span><span class="sxs-lookup"><span data-stu-id="8ef76-262">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="8ef76-263">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="8ef76-263">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="8ef76-264">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="8ef76-264">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="8ef76-265">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="8ef76-265">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="8ef76-266">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="8ef76-266">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="8ef76-267">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="8ef76-267">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="8ef76-268">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="8ef76-268">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8ef76-269">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8ef76-269">Az.Websites</span></span>
* <span data-ttu-id="8ef76-270">Åtgärda fel med ARM-mall som avbryter kloning av alla platser med 'New-AzWebApp -IncludeSourceWebAppSlots'</span><span class="sxs-lookup"><span data-stu-id="8ef76-270">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="8ef76-271">1.5.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="8ef76-271">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8ef76-272">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8ef76-272">Az.Accounts</span></span>
* <span data-ttu-id="8ef76-273">Lägg till kommandot Register-AzModule för stöd för AutoRest-genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="8ef76-273">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="8ef76-274">Uppdatera exempel för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="8ef76-274">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8ef76-275">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8ef76-275">Az.Automation</span></span>
* <span data-ttu-id="8ef76-276">Problem med att hämta vissa månadsscheman i flera Azure Automation-cmdletar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8ef76-276">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="8ef76-277">Åtgärda problem med att Get-AzAutomationDscNode bara returnerar de 20 översta noderna.</span><span class="sxs-lookup"><span data-stu-id="8ef76-277">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="8ef76-278">Nu returneras alla noder</span><span class="sxs-lookup"><span data-stu-id="8ef76-278">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="8ef76-279">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="8ef76-279">Az.Cdn</span></span>
* <span data-ttu-id="8ef76-280">Nya Powershell-cmdletar för att aktivera/inaktivera anpassade domän-HTTPS har lagts till och de gamla har gjorts inaktuella</span><span class="sxs-lookup"><span data-stu-id="8ef76-280">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8ef76-281">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8ef76-281">Az.Compute</span></span>
* <span data-ttu-id="8ef76-282">Lägg till stöd för jokertecken för Get-cmdletar</span><span class="sxs-lookup"><span data-stu-id="8ef76-282">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8ef76-283">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8ef76-283">Az.DataFactory</span></span>
* <span data-ttu-id="8ef76-284">ADF .Net SDK-versionen har uppdaterats till 3.0.1</span><span class="sxs-lookup"><span data-stu-id="8ef76-284">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="8ef76-285">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="8ef76-285">Az.LogicApp</span></span>
* <span data-ttu-id="8ef76-286">Åtgärda problemet med att ListWorkflows endast hämtar den första sidan med resultat</span><span class="sxs-lookup"><span data-stu-id="8ef76-286">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8ef76-287">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8ef76-287">Az.Network</span></span>
* <span data-ttu-id="8ef76-288">Lägg till stöd för jokertecken för Network-cmdletar</span><span class="sxs-lookup"><span data-stu-id="8ef76-288">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8ef76-289">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8ef76-289">Az.RecoveryServices</span></span>
* <span data-ttu-id="8ef76-290">Stöd har lagts till för SQL Server i virtuella Azure-datorer</span><span class="sxs-lookup"><span data-stu-id="8ef76-290">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="8ef76-291">SDK-uppdatering</span><span class="sxs-lookup"><span data-stu-id="8ef76-291">SDK Update</span></span>
* <span data-ttu-id="8ef76-292">Get-ProtectableItem-incheckning i VMappContainer har tagits bort</span><span class="sxs-lookup"><span data-stu-id="8ef76-292">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="8ef76-293">Name och ServerName har lagts till som parametrar för Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="8ef76-293">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="8ef76-294">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8ef76-294">Az.Resources</span></span>
* <span data-ttu-id="8ef76-295">Lägg till parametern `-TemplateObject` i cmdletar för distribution</span><span class="sxs-lookup"><span data-stu-id="8ef76-295">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="8ef76-296">Mer information här: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="8ef76-296">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="8ef76-297">Åtgärda problem med piping av resultatet i `Get-AzResource` till `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="8ef76-297">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="8ef76-298">Mer information här: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="8ef76-298">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="8ef76-299">Åtgärda problem med ändring av JSON-datatyp när `Set-AzResource` körs</span><span class="sxs-lookup"><span data-stu-id="8ef76-299">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="8ef76-300">Mer information här: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="8ef76-300">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="8ef76-301">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8ef76-301">Az.Sql</span></span>
* <span data-ttu-id="8ef76-302">AuditingEndpointsCommunicator uppdateras.</span><span class="sxs-lookup"><span data-stu-id="8ef76-302">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="8ef76-303">Åtgärdar beteendet hos ett gränsscenario när nya diagnostikinställningar skapas.</span><span class="sxs-lookup"><span data-stu-id="8ef76-303">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8ef76-304">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8ef76-304">Az.Storage</span></span>
* <span data-ttu-id="8ef76-305">Stöd för BlockBlobStorage när Storage-konto skapas      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8ef76-305">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="8ef76-306">1.4.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="8ef76-306">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="8ef76-307">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8ef76-307">Az.AnalysisServices</span></span>
* <span data-ttu-id="8ef76-308">Inaktuell AddAzureASAccount-cmdlet</span><span class="sxs-lookup"><span data-stu-id="8ef76-308">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8ef76-309">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8ef76-309">Az.Automation</span></span>
* <span data-ttu-id="8ef76-310">Hjälpen för Import-AzAutomationDscNodeConfiguration har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="8ef76-310">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="8ef76-311">Konfigurationsnamnsvalidering har lagts till i cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="8ef76-311">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="8ef76-312">Förbättrad felhantering för cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="8ef76-312">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="8ef76-313">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8ef76-313">Az.CognitiveServices</span></span>
* <span data-ttu-id="8ef76-314">CustomSubdomainName har lagts till som en ny valfri parameter för New-AzCognitiveServicesAccount, som används för att ange underdomän för resursen.</span><span class="sxs-lookup"><span data-stu-id="8ef76-314">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8ef76-315">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8ef76-315">Az.Compute</span></span>
* <span data-ttu-id="8ef76-316">Problemet med ID-parameteruppsättningar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8ef76-316">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="8ef76-317">Get-AzVMExtension har uppdaterats så att alla installerade tillägg visas om parametern Name inte har angetts</span><span class="sxs-lookup"><span data-stu-id="8ef76-317">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="8ef76-318">Parametrarna Tag och ResourceId har lagts till i cmdleten Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="8ef76-318">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="8ef76-319">Get-AzVmssVM utan instans-ID och med InstanceView kan visa virtuella VMSS-datorer med instansvyn.</span><span class="sxs-lookup"><span data-stu-id="8ef76-319">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8ef76-320">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8ef76-320">Az.DataLakeStore</span></span>
* <span data-ttu-id="8ef76-321">Cmdletar har lagts till för uppräkning och återställning av borttagna objekt i ADL</span><span class="sxs-lookup"><span data-stu-id="8ef76-321">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="8ef76-322">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8ef76-322">Az.EventHub</span></span>
* <span data-ttu-id="8ef76-323">Ny boolesk egenskap SkipEmptyArchives har lagts till i Skip Empty Archives i CaptureDescription-klassen i Eventhub</span><span class="sxs-lookup"><span data-stu-id="8ef76-323">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8ef76-324">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8ef76-324">Az.KeyVault</span></span>
* <span data-ttu-id="8ef76-325">Taggning i Set-AzKeyVaultSecret har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8ef76-325">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="8ef76-326">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="8ef76-326">Az.LogicApp</span></span>
* <span data-ttu-id="8ef76-327">Grundläggande SKU har lagts till för Integrationskonton</span><span class="sxs-lookup"><span data-stu-id="8ef76-327">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="8ef76-328">XSLT 2.0, XSLT 3.0 och Flytande mappningstyper har lagts till</span><span class="sxs-lookup"><span data-stu-id="8ef76-328">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="8ef76-329">Nya cmdletar för integrationskontosammansättningar</span><span class="sxs-lookup"><span data-stu-id="8ef76-329">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="8ef76-330">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="8ef76-330">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="8ef76-331">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="8ef76-331">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="8ef76-332">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="8ef76-332">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="8ef76-333">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="8ef76-333">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="8ef76-334">Nya cmdletar för batchkonfiguration för integrationskonto</span><span class="sxs-lookup"><span data-stu-id="8ef76-334">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="8ef76-335">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="8ef76-335">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="8ef76-336">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="8ef76-336">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="8ef76-337">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="8ef76-337">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="8ef76-338">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="8ef76-338">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="8ef76-339">Logic App-SDK har uppdaterats till version 4.1.0</span><span class="sxs-lookup"><span data-stu-id="8ef76-339">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8ef76-340">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8ef76-340">Az.Monitor</span></span>
* <span data-ttu-id="8ef76-341">Hjälpen för Get-AzMetric har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="8ef76-341">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8ef76-342">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8ef76-342">Az.Network</span></span>
* <span data-ttu-id="8ef76-343">Hjälpexempel för Add-AzApplicationGatewayCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="8ef76-343">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8ef76-344">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8ef76-344">Az.OperationalInsights</span></span>
* <span data-ttu-id="8ef76-345">Ytterligare stöd för datakällorna New och Get ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="8ef76-345">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="8ef76-346">Ny ApplicationInsights-typ har lagts till för att ge stöd för ”Get specific” och ”Get all” för ApplicationInsights-datakällor för angiven arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="8ef76-346">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="8ef76-347">Cmdleten New-AzOperationalInsightsApplicationInsightsDataSource har lagts till för att skapa datakälla med angivna parametrar för Application Insights-resurs: subscription Id, resourceGroupName och name.</span><span class="sxs-lookup"><span data-stu-id="8ef76-347">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8ef76-348">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8ef76-348">Az.Resources</span></span>
* <span data-ttu-id="8ef76-349">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="8ef76-349">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="8ef76-350">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="8ef76-350">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="8ef76-351">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="8ef76-351">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="8ef76-352">Fel som gör att KeyCredentials inte kan skapas upprepade gånger har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8ef76-352">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="8ef76-353">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8ef76-353">Az.Sql</span></span>
* <span data-ttu-id="8ef76-354">Lägg till stöd för hyperskalanivån för SQL DB</span><span class="sxs-lookup"><span data-stu-id="8ef76-354">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="8ef76-355">Ett fel har åtgärdats där återställningen kunde misslyckas på grund av onödiga inställningsegenskaper i restore-förfrågan</span><span class="sxs-lookup"><span data-stu-id="8ef76-355">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8ef76-356">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8ef76-356">Az.Websites</span></span>
* <span data-ttu-id="8ef76-357">Rätt exempel i Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="8ef76-357">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="8ef76-358">1.3.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="8ef76-358">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8ef76-359">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8ef76-359">Az.Accounts</span></span>
* <span data-ttu-id="8ef76-360">Uppdatera till den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="8ef76-360">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="8ef76-361">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8ef76-361">Az.AnalysisServices</span></span>
<span data-ttu-id="8ef76-362">Allmän tillgänglighet för Az.AnalysisServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="8ef76-362">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8ef76-363">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8ef76-363">Az.Compute</span></span>
* <span data-ttu-id="8ef76-364">AEM-tillägg: Lägg till stöd för UltraSSD-, P60-, P70- och P80-diskar</span><span class="sxs-lookup"><span data-stu-id="8ef76-364">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="8ef76-365">Uppdatera hjälpbeskrivning för Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="8ef76-365">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="8ef76-366">Uppdatera hjälpbeskrivning och exempel för Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="8ef76-366">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8ef76-367">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8ef76-367">Az.RecoveryServices</span></span>
<span data-ttu-id="8ef76-368">Allmän tillgänglighet för Az.RecoveryServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="8ef76-368">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8ef76-369">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8ef76-369">Az.Resources</span></span>
* <span data-ttu-id="8ef76-370">Korrigera taggar för resursgrupper</span><span class="sxs-lookup"><span data-stu-id="8ef76-370">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="8ef76-371">Mer information här: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="8ef76-371">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="8ef76-372">Åtgärda problem där `Get-AzureRmRoleAssignment` inte respekterar -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="8ef76-372">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="8ef76-373">Mer information här: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="8ef76-373">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="8ef76-374">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8ef76-374">Az.Sql</span></span>
* <span data-ttu-id="8ef76-375">Lägga till Get/Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8ef76-375">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="8ef76-376">Åtgärda problem där ett nullref-undantag uppstår när du kör SQL-cmdletar och inte är inloggad på ett Azure-konto</span><span class="sxs-lookup"><span data-stu-id="8ef76-376">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="8ef76-377">Åtgärda nullref-undantag i Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="8ef76-377">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="8ef76-378">1.2.1 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="8ef76-378">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8ef76-379">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8ef76-379">Az.Accounts</span></span>
* <span data-ttu-id="8ef76-380">Version med rätt version av autentisering</span><span class="sxs-lookup"><span data-stu-id="8ef76-380">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="8ef76-381">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8ef76-381">Az.AnalysisServices</span></span>
* <span data-ttu-id="8ef76-382">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="8ef76-382">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8ef76-383">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8ef76-383">Az.RecoveryServices</span></span>
* <span data-ttu-id="8ef76-384">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="8ef76-384">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="8ef76-385">1.2.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="8ef76-385">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8ef76-386">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8ef76-386">Az.Accounts</span></span>
* <span data-ttu-id="8ef76-387">Lägga till interaktiv autentisering och autentisering med användarnamn/lösenord för endast Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="8ef76-387">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="8ef76-388">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="8ef76-388">Update incorrect online help URLs</span></span>
* <span data-ttu-id="8ef76-389">Lägga till varningsmeddelande i PS Core för Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="8ef76-389">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="8ef76-390">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="8ef76-390">Az.Aks</span></span>
* <span data-ttu-id="8ef76-391">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="8ef76-391">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8ef76-392">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8ef76-392">Az.Automation</span></span>
* <span data-ttu-id="8ef76-393">Stöd för Python 2-runbookflöden har lagts till</span><span class="sxs-lookup"><span data-stu-id="8ef76-393">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="8ef76-394">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="8ef76-394">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="8ef76-395">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="8ef76-395">Az.Cdn</span></span>
* <span data-ttu-id="8ef76-396">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="8ef76-396">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8ef76-397">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8ef76-397">Az.Compute</span></span>
* <span data-ttu-id="8ef76-398">Lägga till cmdleten Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="8ef76-398">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="8ef76-399">Lägga till TempDisk-parameter i Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8ef76-399">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="8ef76-400">Korrigera varningsmeddelande för New-AzVM</span><span class="sxs-lookup"><span data-stu-id="8ef76-400">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="8ef76-401">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8ef76-401">Az.ContainerRegistry</span></span>
* <span data-ttu-id="8ef76-402">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="8ef76-402">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8ef76-403">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8ef76-403">Az.DataFactory</span></span>
* <span data-ttu-id="8ef76-404">ADF .Net SDK-versionen har uppdaterats till 3.0.0</span><span class="sxs-lookup"><span data-stu-id="8ef76-404">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8ef76-405">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8ef76-405">Az.DataLakeStore</span></span>
* <span data-ttu-id="8ef76-406">Åtgärda problem med ADLS-slutpunkt vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="8ef76-406">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="8ef76-407">Mer information här: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="8ef76-407">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="8ef76-408">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="8ef76-408">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8ef76-409">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8ef76-409">Az.IotHub</span></span>
* <span data-ttu-id="8ef76-410">Lägga till kodningsformat i cmdleten Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="8ef76-410">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8ef76-411">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8ef76-411">Az.KeyVault</span></span>
* <span data-ttu-id="8ef76-412">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="8ef76-412">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8ef76-413">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8ef76-413">Az.Network</span></span>
* <span data-ttu-id="8ef76-414">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="8ef76-414">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="8ef76-415">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8ef76-415">Az.Resources</span></span>
* <span data-ttu-id="8ef76-416">Åtgärda felaktiga exempel i referensdokumentationen ”New-AzADAppCredential” och ”New-AzADSpCredential”</span><span class="sxs-lookup"><span data-stu-id="8ef76-416">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="8ef76-417">Åtgärda problem där sökvägen för parametern ”-TemplateFile” inte omvandlas innan cmdletarna för distribution i resursgruppen körs</span><span class="sxs-lookup"><span data-stu-id="8ef76-417">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="8ef76-418">Az.Resources: Korrigera dokumentationen om standardvärdet för New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="8ef76-418">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="8ef76-419">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="8ef76-419">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="8ef76-420">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="8ef76-420">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="8ef76-421">Åtgärda formateringsproblemet med objektet ”PSResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="8ef76-421">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="8ef76-422">Mer information här: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="8ef76-422">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8ef76-423">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8ef76-423">Az.ServiceFabric</span></span>
* <span data-ttu-id="8ef76-424">Återställ när ett certifikat läggs till i en Virtual Machine Scale Sets-modell men ett undantag genereras. Detta har gjorts för att åtgärda följande fel: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="8ef76-424">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="8ef76-425">Korrigera några felmeddelanden.</span><span class="sxs-lookup"><span data-stu-id="8ef76-425">Fix some error messages.</span></span>
* <span data-ttu-id="8ef76-426">Korrigering av skapande av kluster med ARM-mall som är standard för New-AzServiceFabriCluster som inte fungerade med migrering till Az.</span><span class="sxs-lookup"><span data-stu-id="8ef76-426">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="8ef76-427">Korrigering av tilläggning av kluster/programcertifikat så att endast VM Scale Sets som motsvarar klustret läggs till genom att kontrollera ID för klustret i tillägget.</span><span class="sxs-lookup"><span data-stu-id="8ef76-427">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="8ef76-428">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="8ef76-428">Az.SignalR</span></span>
* <span data-ttu-id="8ef76-429">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="8ef76-429">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="8ef76-430">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8ef76-430">Az.Sql</span></span>
* <span data-ttu-id="8ef76-431">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="8ef76-431">Update incorrect online help URLs</span></span>
* <span data-ttu-id="8ef76-432">Uppdaterad parameterbeskrivning för LicenseType-parameter med möjliga värden</span><span class="sxs-lookup"><span data-stu-id="8ef76-432">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="8ef76-433">Korrigering för att uppdatera hanterad instansidentitet som inte fungerar när det är den enda uppdaterade egenskapen</span><span class="sxs-lookup"><span data-stu-id="8ef76-433">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="8ef76-434">Stöd för anpassad sortering på hanterad instans</span><span class="sxs-lookup"><span data-stu-id="8ef76-434">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8ef76-435">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8ef76-435">Az.Storage</span></span>
* <span data-ttu-id="8ef76-436">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="8ef76-436">Update incorrect online help URLs</span></span>
* <span data-ttu-id="8ef76-437">Tillhandahåll detaljerat felmeddelande när en användare försöker hämta/konfigurera klassisk loggning/mått på ett Premium Storage-konto eftersom Premium Storage-kontot inte har stöd för klassisk loggning/mått.</span><span class="sxs-lookup"><span data-stu-id="8ef76-437">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="8ef76-438">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="8ef76-438">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="8ef76-439">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="8ef76-439">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="8ef76-440">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="8ef76-440">Az.TrafficManager</span></span>
* <span data-ttu-id="8ef76-441">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="8ef76-441">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8ef76-442">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8ef76-442">Az.Websites</span></span>
* <span data-ttu-id="8ef76-443">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="8ef76-443">Update incorrect online help URLs</span></span>
* <span data-ttu-id="8ef76-444">Korrigerar ”New-AzWebAppSSLBinding” så att certifikatet laddas upp till rätt resursgrupp och plats om appen finns i en ASE.</span><span class="sxs-lookup"><span data-stu-id="8ef76-444">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="8ef76-445">Korrigerar ”New-AzWebAppSSLBinding” så att taggarna inte skrivs över på en bindning av ett SSL-certifikat till en app</span><span class="sxs-lookup"><span data-stu-id="8ef76-445">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="8ef76-446">1.1.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="8ef76-446">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8ef76-447">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8ef76-447">Az.Accounts</span></span>
* <span data-ttu-id="8ef76-448">Lade till omfattningen ”Lokal” till Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="8ef76-448">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8ef76-449">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8ef76-449">Az.Compute</span></span>
* <span data-ttu-id="8ef76-450">Namn är nu valfritt i ID-parametern för Restart/Start/Stop/Remove/Set-AzVM och Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="8ef76-450">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="8ef76-451">Uppdaterade beskrivningen av ID i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="8ef76-451">Updated the description of ID in help files</span></span>
* <span data-ttu-id="8ef76-452">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8ef76-452">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8ef76-453">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8ef76-453">Az.DataLakeStore</span></span>
* <span data-ttu-id="8ef76-454">Uppdatera sdk-versionen av dataplanet till 1.1.14 för SDK-korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="8ef76-454">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="8ef76-455">Korrigerade hanteringen av negativ accesstime och modificationtime för getfilestatus och liststatus; korrigera asynkront annulleringstoken</span><span class="sxs-lookup"><span data-stu-id="8ef76-455">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="8ef76-456">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="8ef76-456">Az.EventGrid</span></span>
* <span data-ttu-id="8ef76-457">Uppdaterat för användning av API-versionen 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="8ef76-457">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="8ef76-458">Uppdaterade följande cmdletar för att stödja nytt scenario i API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="8ef76-458">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="8ef76-459">New-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="8ef76-459">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="8ef76-460">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="8ef76-460">Event Time-To-Live,</span></span>
        - <span data-ttu-id="8ef76-461">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="8ef76-461">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="8ef76-462">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="8ef76-462">Dead letter endpoint.</span></span>
    - <span data-ttu-id="8ef76-463">Update-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="8ef76-463">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="8ef76-464">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="8ef76-464">Event Time-To-Live,</span></span>
        - <span data-ttu-id="8ef76-465">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="8ef76-465">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="8ef76-466">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="8ef76-466">Dead letter endpoint.</span></span>
* <span data-ttu-id="8ef76-467">Lade till nya enum-värden (storageQueue och hybridConnection) för alternativet EndpointType i cmdletarna New-AzureRmEventGridSubscription och Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="8ef76-467">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="8ef76-468">Visa varningsmeddelanden om skapande eller uppdatering av händelseprenumerationen förväntas medföra manuell åtgärd från användaren.</span><span class="sxs-lookup"><span data-stu-id="8ef76-468">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8ef76-469">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8ef76-469">Az.IotHub</span></span>
* <span data-ttu-id="8ef76-470">Har uppdaterats till den senaste versionen av SDK:n lotHub</span><span class="sxs-lookup"><span data-stu-id="8ef76-470">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="8ef76-471">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="8ef76-471">Az.LogicApp</span></span>
* <span data-ttu-id="8ef76-472">Get-AzLogicApp visar en lista över alla som inte har angivet namn</span><span class="sxs-lookup"><span data-stu-id="8ef76-472">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="8ef76-473">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8ef76-473">Az.Resources</span></span>
* <span data-ttu-id="8ef76-474">Åtgärdade problem med parameteruppsättningen när parametrarna -ODataQuery och -ResourceId anges för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="8ef76-474">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="8ef76-475">Mer information här: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="8ef76-475">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="8ef76-476">Åtgärdade hantering av parametern -Custom i New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8ef76-476">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="8ef76-477">Korrigerade stavfel i New-AzDeployment-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="8ef76-477">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="8ef76-478">Gjorde parametern -MailNickname obligatorisk för New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="8ef76-478">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="8ef76-479">Mer information här: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="8ef76-479">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="8ef76-480">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="8ef76-480">Az.SignalR</span></span>
* <span data-ttu-id="8ef76-481">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8ef76-481">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="8ef76-482">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8ef76-482">Az.Sql</span></span>
* <span data-ttu-id="8ef76-483">Konverterade lagringshanteringsklientens beroende av den normala SDK-implementeringen.</span><span class="sxs-lookup"><span data-stu-id="8ef76-483">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8ef76-484">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8ef76-484">Az.Storage</span></span>
* <span data-ttu-id="8ef76-485">Angav StorageAccountName för lagringskontext som det verkliga namnet på lagringskontot när det skapas med Sas Token, OAuth eller Anonymous</span><span class="sxs-lookup"><span data-stu-id="8ef76-485">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="8ef76-486">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="8ef76-486">New-AzStorageContext</span></span>
* <span data-ttu-id="8ef76-487">Skapade Sas Token för Blob Snapshot-objekt med parametern -FullUri, åtgärdade den returnerade URI:n så att den blir URI för ögonblicksbild</span><span class="sxs-lookup"><span data-stu-id="8ef76-487">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="8ef76-488">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="8ef76-488">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8ef76-489">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8ef76-489">Az.Websites</span></span>
* <span data-ttu-id="8ef76-490">Åtgärdade en bugg i datumparsningen i Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="8ef76-490">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="8ef76-491">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8ef76-491">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="8ef76-492">1.0.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="8ef76-492">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="8ef76-493">Allmänt</span><span class="sxs-lookup"><span data-stu-id="8ef76-493">General</span></span>

- <span data-ttu-id="8ef76-494">Allmän tillgänglighet för Az-modulen</span><span class="sxs-lookup"><span data-stu-id="8ef76-494">General Availability of Az Module</span></span>
- <span data-ttu-id="8ef76-495">Onlinehjälp för varje modul</span><span class="sxs-lookup"><span data-stu-id="8ef76-495">Online help for each module</span></span>
- <span data-ttu-id="8ef76-496">Mer information och en översikt finns på [Az-informationssidan](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="8ef76-496">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="8ef76-497">Information om hur du migrerar från AzureRM finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8ef76-497">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="8ef76-498">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8ef76-498">Az.Accounts</span></span>
- <span data-ttu-id="8ef76-499">Har ändrats från Az.Profile</span><span class="sxs-lookup"><span data-stu-id="8ef76-499">Changed from Az.Profile</span></span>
- <span data-ttu-id="8ef76-500">Fasta tabellformat för profil- och kontexttyper</span><span class="sxs-lookup"><span data-stu-id="8ef76-500">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="8ef76-501">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8ef76-501">Az.ApiManagement</span></span>
- <span data-ttu-id="8ef76-502">Korrigeringar för #7002</span><span class="sxs-lookup"><span data-stu-id="8ef76-502">Fixes for #7002</span></span>
- <span data-ttu-id="8ef76-503">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8ef76-503">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="8ef76-504">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="8ef76-504">Az.Batch</span></span>
- <span data-ttu-id="8ef76-505">Lade till möjligheten att se vilken version av Azure Batch Node Agent som körs på var och en av de virtuella datorerna i en pool, via den nya egenskapen `NodeAgentInformation` på `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="8ef76-505">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="8ef76-506">Standarden `Caching` för `PSDataDisk` är nu `ReadWrite` i stället för `None`.</span><span class="sxs-lookup"><span data-stu-id="8ef76-506">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="8ef76-507">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8ef76-507">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="8ef76-508">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="8ef76-508">Az.Billing</span></span>
- <span data-ttu-id="8ef76-509">Kombinerar cmdletarna för fakturering, förbrukning och UsageAggregates. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8ef76-509">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="8ef76-510">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="8ef76-510">Az.CognitivServices</span></span>
- <span data-ttu-id="8ef76-511">Lade till kompletterare för SkuName och Typem som är tillgängliga i New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="8ef76-511">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="8ef76-512">Tog bort parameteruppsättningen GetSkusWithAccountParamSetName från Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="8ef76-512">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="8ef76-513">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="8ef76-513">Az.ContainerInstance</span></span>
- <span data-ttu-id="8ef76-514">Stöd för ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="8ef76-514">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="8ef76-515">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="8ef76-515">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="8ef76-516">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8ef76-516">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="8ef76-517">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8ef76-517">Az.DataLakeStore</span></span>
- <span data-ttu-id="8ef76-518">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8ef76-518">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="8ef76-519">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8ef76-519">Az.Monitor</span></span>
- <span data-ttu-id="8ef76-520">Döpte om Az.Insights till Az.Monitor och andra mindre icke-bakåtkompatibla ändringar. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8ef76-520">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="8ef76-521">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8ef76-521">Az.KeyVault</span></span>
- <span data-ttu-id="8ef76-522">Tog bort den inaktuella egenskapen PurgeDisabled från utdatatyper</span><span class="sxs-lookup"><span data-stu-id="8ef76-522">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="8ef76-523">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="8ef76-523">Az.MachineLearning</span></span>
- <span data-ttu-id="8ef76-524">Inkluderade cmdletarna från modulen Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="8ef76-524">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="8ef76-525">Az.Media</span><span class="sxs-lookup"><span data-stu-id="8ef76-525">Az.Media</span></span>
- <span data-ttu-id="8ef76-526">Tog bort inaktuella -Tags-alias från New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="8ef76-526">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="8ef76-527">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8ef76-527">Az.Network</span></span>
<span data-ttu-id="8ef76-528">Stöd har lagts till för konfiguration av RewriteRuleSets i Application Gateway</span><span class="sxs-lookup"><span data-stu-id="8ef76-528">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="8ef76-529">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="8ef76-529">New cmdlets added:</span></span>
        - <span data-ttu-id="8ef76-530">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8ef76-530">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="8ef76-531">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8ef76-531">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="8ef76-532">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8ef76-532">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="8ef76-533">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8ef76-533">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="8ef76-534">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8ef76-534">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="8ef76-535">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="8ef76-535">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="8ef76-536">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="8ef76-536">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="8ef76-537">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="8ef76-537">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="8ef76-538">Cmdletar har uppdaterats med den valfria parametern -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8ef76-538">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="8ef76-539">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8ef76-539">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="8ef76-540">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="8ef76-540">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="8ef76-541">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="8ef76-541">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="8ef76-542">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8ef76-542">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="8ef76-543">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="8ef76-543">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="8ef76-544">New-AzureRmApplicationGatewayUrlPathMapConfig har lagt till KeyVault-stöd för Application Gateway med Identity.</span><span class="sxs-lookup"><span data-stu-id="8ef76-544">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="8ef76-545">Cmdletar har uppdaterats med den valfria parametern -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="8ef76-545">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="8ef76-546">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8ef76-546">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="8ef76-547">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8ef76-547">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="8ef76-548">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8ef76-548">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="8ef76-549">Cmdleten New-AzApplicationGateway har uppdaterats med den valfria parametern -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="8ef76-549">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="8ef76-550">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8ef76-550">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="8ef76-551">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8ef76-551">Az.OperationalInsights</span></span>
- <span data-ttu-id="8ef76-552">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8ef76-552">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="8ef76-553">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="8ef76-553">Az.Profile</span></span>
- <span data-ttu-id="8ef76-554">Modulnamnet har ändrats till Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8ef76-554">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="8ef76-555">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8ef76-555">Az.RecoveryServices</span></span>
- <span data-ttu-id="8ef76-556">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8ef76-556">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="8ef76-557">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8ef76-557">Az.Resources</span></span>
- <span data-ttu-id="8ef76-558">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8ef76-558">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="8ef76-559">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8ef76-559">Az.ServiceFabric</span></span>
- <span data-ttu-id="8ef76-560">Stöd för specificering av certifikat efter eget namn och tumavtryck</span><span class="sxs-lookup"><span data-stu-id="8ef76-560">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="8ef76-561">Information om fler icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8ef76-561">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="8ef76-562">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="8ef76-562">Az.SIgnalR</span></span>
- <span data-ttu-id="8ef76-563">Allmän tillgänglighet för PowerShell-cmdletar för SIgnalR</span><span class="sxs-lookup"><span data-stu-id="8ef76-563">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="8ef76-564">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8ef76-564">Az.Sql</span></span>
- <span data-ttu-id="8ef76-565">Lade till de nya identifieringstyperna Data_Exfiltration och Unsafe_Action i Threat Detection-cmdletar</span><span class="sxs-lookup"><span data-stu-id="8ef76-565">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="8ef76-566">Uppdaterade dokumentationsexempel för Sql Auditing-cmdletar</span><span class="sxs-lookup"><span data-stu-id="8ef76-566">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="8ef76-567">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8ef76-567">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="8ef76-568">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8ef76-568">Az.Storage</span></span>
- <span data-ttu-id="8ef76-569">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8ef76-569">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="8ef76-570">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8ef76-570">Az.Websites</span></span>
- <span data-ttu-id="8ef76-571">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8ef76-571">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="8ef76-572">0.7.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="8ef76-572">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="8ef76-573">Allmänt</span><span class="sxs-lookup"><span data-stu-id="8ef76-573">General</span></span>

* <span data-ttu-id="8ef76-574">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="8ef76-574">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="8ef76-575">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8ef76-575">Az.Compute</span></span>

* <span data-ttu-id="8ef76-576">Lade till stöd för UltraSSD och Galleriavbildningar i de enkla parameteruppsättningarna för `New-AzVm(ss)`-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="8ef76-576">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="8ef76-577">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8ef76-577">Az.DataLakeStore</span></span>

* <span data-ttu-id="8ef76-578">Åtgärdade avslutande snedstreck i domänen för adls-konto</span><span class="sxs-lookup"><span data-stu-id="8ef76-578">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="8ef76-579">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="8ef76-579">Az.FrontDoor</span></span>

* <span data-ttu-id="8ef76-580">Brutna länkar korrigerades</span><span class="sxs-lookup"><span data-stu-id="8ef76-580">Fixed some broken links</span></span>
    - <span data-ttu-id="8ef76-581">I artiklarna New-AzureRmFrontDoor och Set-AzureRmFrontDoor artiklar korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="8ef76-581">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="8ef76-582">I artikeln New-AzureRmFrontDoorManagedRuleObject korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="8ef76-582">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="8ef76-583">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8ef76-583">Az.RecoveryServices</span></span>

* <span data-ttu-id="8ef76-584">Lade till valideringar på klientsidan för Azure-filresurs med återställningsåtgärder.</span><span class="sxs-lookup"><span data-stu-id="8ef76-584">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="8ef76-585">Gjorde storageAccountName och storageAccountResourceGroupName valfritt för afs-återställning.</span><span class="sxs-lookup"><span data-stu-id="8ef76-585">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="8ef76-586">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8ef76-586">Az.Resources</span></span>

* <span data-ttu-id="8ef76-587">Korrigering för https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="8ef76-587">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="8ef76-588">Uppdaterade Get-AzureRmRoleAssignment så att prenumerationsomfattningen används om den anges vid begäran om klassiska administratörer.</span><span class="sxs-lookup"><span data-stu-id="8ef76-588">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="8ef76-589">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8ef76-589">Az.Sql</span></span>

* <span data-ttu-id="8ef76-590">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="8ef76-590">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="8ef76-591">Korrigerade ett problem med Get-AzureRmSqlDatabaseVulnerabilityAssessment med DotNet-kärna</span><span class="sxs-lookup"><span data-stu-id="8ef76-591">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="8ef76-592">Ändrade dokumentationen för hjälpmeddelanden som rör SQL Auditing-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="8ef76-592">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="8ef76-593">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8ef76-593">Az.Storage</span></span>

* <span data-ttu-id="8ef76-594">Lade till -EnableHierarchicalNamespace i New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8ef76-594">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="8ef76-595">Åtgärdade problemet med att cmdleten Copy File inte kunde återanvända källkontexten på målet om inte -DestContext angetts</span><span class="sxs-lookup"><span data-stu-id="8ef76-595">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="8ef76-596">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="8ef76-596">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="8ef76-597">Stöd för statisk webbplatskonfiguration</span><span class="sxs-lookup"><span data-stu-id="8ef76-597">Support Static Website configuration</span></span>
    - <span data-ttu-id="8ef76-598">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="8ef76-598">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="8ef76-599">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="8ef76-599">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="8ef76-600">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8ef76-600">Az.Websites</span></span>

* <span data-ttu-id="8ef76-601">Set-AzureRmWebApp och Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8ef76-601">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="8ef76-602">Ny parameter (-AzureStoragePath) har lagts till för att ange att Azure Storage-sökvägar ska monteras i containerappar i Windows och Linux.</span><span class="sxs-lookup"><span data-stu-id="8ef76-602">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="8ef76-603">Använder utdata från den nya cmdleten New-AzureRmWebAppAzureStoragePath som en parameter för att ange sökvägar för Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="8ef76-603">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="8ef76-604">0.6.1 – november 2018</span><span class="sxs-lookup"><span data-stu-id="8ef76-604">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="8ef76-605">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8ef76-605">Az.ApiManagement</span></span>
* <span data-ttu-id="8ef76-606">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="8ef76-606">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="8ef76-607">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8ef76-607">Az.Automation</span></span>
* <span data-ttu-id="8ef76-608">Swagger baserade Azure Automation-cmdletar</span><span class="sxs-lookup"><span data-stu-id="8ef76-608">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="8ef76-609">Cmdletar för Uppdateringshantering har lagts till</span><span class="sxs-lookup"><span data-stu-id="8ef76-609">Added Update Management cmdlets</span></span>
* <span data-ttu-id="8ef76-610">Cmdletar för källkontroll har lagts till</span><span class="sxs-lookup"><span data-stu-id="8ef76-610">Added Source Control cmdlets</span></span>
* <span data-ttu-id="8ef76-611">Remove-AzureRmAutomationHybridWorkerGroup-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="8ef76-611">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="8ef76-612">Kommandot för DSC-registreringsnod har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8ef76-612">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="8ef76-613">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8ef76-613">Az.Compute</span></span>
* <span data-ttu-id="8ef76-614">Problem med SystemAssigned-identitet har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8ef76-614">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="8ef76-615">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="8ef76-615">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="8ef76-616">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="8ef76-616">Az.ContainerInstance</span></span>
* <span data-ttu-id="8ef76-617">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="8ef76-617">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="8ef76-618">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="8ef76-618">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="8ef76-619">uppdatera exempelbeskrivningen för marketplace-cmdletar</span><span class="sxs-lookup"><span data-stu-id="8ef76-619">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="8ef76-620">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8ef76-620">Az.Network</span></span>
* <span data-ttu-id="8ef76-621">Cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomErreller Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="8ef76-621">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="8ef76-622">ICMP tillbaka till stöd för Azure Firewall-nätverksprotokoll har lagts till</span><span class="sxs-lookup"><span data-stu-id="8ef76-622">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="8ef76-623">Uppdatera cmdlet Test-AzureRmNetworkWatcherConnectivity, lägga till verifiering av mål-id, adress och port.</span><span class="sxs-lookup"><span data-stu-id="8ef76-623">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="8ef76-624">Åtgärda problem med minnesanvändning i VirtualNetwork-karta</span><span class="sxs-lookup"><span data-stu-id="8ef76-624">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="8ef76-625">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="8ef76-625">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="8ef76-626">Åtgärda för att ändra principen för en skyddad fildelning.</span><span class="sxs-lookup"><span data-stu-id="8ef76-626">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="8ef76-627">Tidszonsprincipen har konverterats till versaler.</span><span class="sxs-lookup"><span data-stu-id="8ef76-627">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="8ef76-628">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="8ef76-628">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="8ef76-629">Exempel i New-AzureRmRecoveryServicesAsrProtectableItem har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8ef76-629">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="8ef76-630">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="8ef76-630">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="8ef76-631">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="8ef76-631">Az.Relay</span></span>
* <span data-ttu-id="8ef76-632">Valfri parameter -KeyValue till New-AzureRmRelayKey cmdlet har lagts till, vilket gör det möjligt för användare att tillhandahålla KeyValue.</span><span class="sxs-lookup"><span data-stu-id="8ef76-632">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="8ef76-633">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8ef76-633">Az.Resources</span></span>
* <span data-ttu-id="8ef76-634">Uppdatera hjälpdokumentation för resursidentitet kopplad till parametrar i `New-AzureRmPolicyAssignment` och `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="8ef76-634">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="8ef76-635">Lägg till ett exempel för New-AzureRmPolicyDefinition som använder -Metadata</span><span class="sxs-lookup"><span data-stu-id="8ef76-635">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="8ef76-636">Korrigera så att skiftläge behålls i taggnycklar i NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="8ef76-636">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="8ef76-637">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8ef76-637">Az.ServiceFabric</span></span>
* <span data-ttu-id="8ef76-638">Lägg till utfasningsmeddelanden för kommande icke-kompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="8ef76-638">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="8ef76-639">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8ef76-639">Az.Sql</span></span>
* <span data-ttu-id="8ef76-640">Nya cmdletar för CRUD-åtgärder på Azure Sql Database-hanterad instans och Azure Sql-hanterad databas</span><span class="sxs-lookup"><span data-stu-id="8ef76-640">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="8ef76-641">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="8ef76-641">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="8ef76-642">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="8ef76-642">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="8ef76-643">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="8ef76-643">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="8ef76-644">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="8ef76-644">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="8ef76-645">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="8ef76-645">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="8ef76-646">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="8ef76-646">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="8ef76-647">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="8ef76-647">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="8ef76-648">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="8ef76-648">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="8ef76-649">Hantering av utökad granskningsprincip på en server eller en databas har aktiverats.</span><span class="sxs-lookup"><span data-stu-id="8ef76-649">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="8ef76-650">Ny parameter (PredicateExpression) har lagts till för att aktivera filtrering av granskningsloggar.</span><span class="sxs-lookup"><span data-stu-id="8ef76-650">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="8ef76-651">Cmdletar har ändrats så att de använder SQL-klienter i stället för äldre klienter.</span><span class="sxs-lookup"><span data-stu-id="8ef76-651">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="8ef76-652">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="8ef76-652">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="8ef76-653">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="8ef76-653">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="8ef76-654">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="8ef76-654">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="8ef76-655">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="8ef76-655">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="8ef76-656">Problem med att använda Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings med lagringskontots namnparameter har korrigerats</span><span class="sxs-lookup"><span data-stu-id="8ef76-656">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="8ef76-657">0.5.0 – november 2018</span><span class="sxs-lookup"><span data-stu-id="8ef76-657">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="8ef76-658">Allmänt</span><span class="sxs-lookup"><span data-stu-id="8ef76-658">General</span></span>
* <span data-ttu-id="8ef76-659">Lade till resurskompletterare till många kärn-cmdletar – dessa gör att du kan stega genom befintliga resursnamn med TABB vid interaktiva anrop till cmdletar</span><span class="sxs-lookup"><span data-stu-id="8ef76-659">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="8ef76-660">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="8ef76-660">Az.Profile</span></span>
* <span data-ttu-id="8ef76-661">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="8ef76-661">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="8ef76-662">Bytte namn på parametern TenantId i cmdleten Connect-AzAccount till Tenant och lade till ett alias för TenantId</span><span class="sxs-lookup"><span data-stu-id="8ef76-662">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="8ef76-663">Uppdaterade TenantId-beskrivningen för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="8ef76-663">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="8ef76-664">Åtgärda felmeddelande för misslyckad inloggning när du tillhandahåller klientdomän</span><span class="sxs-lookup"><span data-stu-id="8ef76-664">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="8ef76-665">Åtgärda problem med att kontextnamn hamnar i konflikt för konton utan prenumerationer i klientorganisationen</span><span class="sxs-lookup"><span data-stu-id="8ef76-665">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="8ef76-666">Åtgärda problem med DataLake-slutpunkter vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="8ef76-666">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="8ef76-667">Åtgärdade problem med att Disconnect-AzAccount kastades om den inte anslöts</span><span class="sxs-lookup"><span data-stu-id="8ef76-667">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="8ef76-668">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8ef76-668">Az.CognitiveServices</span></span>
* <span data-ttu-id="8ef76-669">Lade till åtgärden Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="8ef76-669">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8ef76-670">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8ef76-670">Az.Compute</span></span>
* <span data-ttu-id="8ef76-671">Lade till cmdletarna Add-AzVmssVMDataDisk och Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="8ef76-671">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="8ef76-672">Get-AzVMImage visar AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="8ef76-672">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="8ef76-673">Åtgärdade att värdena för alternativen SetAzVMChefExtension -BootstrapOptions och -JsonAttribute inte angavs i json-format.</span><span class="sxs-lookup"><span data-stu-id="8ef76-673">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8ef76-674">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8ef76-674">Az.DataLakeStore</span></span>
* <span data-ttu-id="8ef76-675">Uppdatera DataLake-paketet till 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="8ef76-675">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="8ef76-676">Lägg till standardsamtidighet för flertrådade åtgärder.</span><span class="sxs-lookup"><span data-stu-id="8ef76-676">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="8ef76-677">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="8ef76-677">Az.Insights</span></span>
* <span data-ttu-id="8ef76-678">Åtgärdade problem #7267 (autoskalningsområde)</span><span class="sxs-lookup"><span data-stu-id="8ef76-678">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="8ef76-679">Problem med att uppräknade parametrar inte ställdes in ordentligt när du skapade en ny autoskalningsregel (de ställdes alltid in med standardvärdet).</span><span class="sxs-lookup"><span data-stu-id="8ef76-679">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="8ef76-680">Åtgärdade problem #7513 [Insights] Set-AzDiagnosticSetting kräver uttrycklig specifikation av kategorier när inställningar skapas</span><span class="sxs-lookup"><span data-stu-id="8ef76-680">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="8ef76-681">Nu kräver inte cmdleten uttrycklig anvisning av kategorierna för att aktiveras under skapande, d.v.s. den fungerar enligt beskrivning</span><span class="sxs-lookup"><span data-stu-id="8ef76-681">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8ef76-682">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8ef76-682">Az.Network</span></span>
* <span data-ttu-id="8ef76-683">PeeringType ändrades till en obligatorisk parameter för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="8ef76-683">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="8ef76-684">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="8ef76-684">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="8ef76-685">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="8ef76-685">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="8ef76-686">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="8ef76-686">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="8ef76-687">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="8ef76-687">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="8ef76-688">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="8ef76-688">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="8ef76-689">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="8ef76-689">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="8ef76-690">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="8ef76-690">Az.PolicyInsights</span></span>
* <span data-ttu-id="8ef76-691">Cmdletar för principreparation har lagts till</span><span class="sxs-lookup"><span data-stu-id="8ef76-691">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="8ef76-692">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8ef76-692">Az.Resources</span></span>
* <span data-ttu-id="8ef76-693">Korrigering för https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="8ef76-693">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="8ef76-694">Tillåt att resurser listas med parametern -ResourceId för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="8ef76-694">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="8ef76-695">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8ef76-695">Az.ServiceBus</span></span>
* <span data-ttu-id="8ef76-696">Skrivskyddad MigrationState-egenskap har lagts till i PSServiceBusMigrationConfigurationAttributes, som hjälper till att hålla koll på migreringstillståndet.</span><span class="sxs-lookup"><span data-stu-id="8ef76-696">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8ef76-697">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8ef76-697">Az.ServiceFabric</span></span>
* <span data-ttu-id="8ef76-698">Åtgärda att lägga till certifikat till Linux-Vmss.</span><span class="sxs-lookup"><span data-stu-id="8ef76-698">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="8ef76-699">Åtgärdade Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="8ef76-699">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="8ef76-700">Använd rätt tumavtryck från nya certifikat (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="8ef76-700">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="8ef76-701">Visa undantag korrekt (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="8ef76-701">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="8ef76-702">Åtgärdade Update-AzServiceFabricDurability så att klusterkonfigurationen uppdateras innan Vmss-åtgärden CreateOrUpdate påbörjas.</span><span class="sxs-lookup"><span data-stu-id="8ef76-702">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="8ef76-703">0.4.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="8ef76-703">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="8ef76-704">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="8ef76-704">Az.Profile</span></span>
* <span data-ttu-id="8ef76-705">Åtgärdade problemet med Get-AzSubscription i CloudShell</span><span class="sxs-lookup"><span data-stu-id="8ef76-705">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="8ef76-706">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="8ef76-706">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8ef76-707">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8ef76-707">Az.Compute</span></span>
* <span data-ttu-id="8ef76-708">Nya storlekar lades till i listan över godkända VM-storlekar för vilka accelererat nätverk kommer att aktiveras vid användning av den enkla parameteruppsättningen för New-AzVm</span><span class="sxs-lookup"><span data-stu-id="8ef76-708">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="8ef76-709">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="8ef76-709">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8ef76-710">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8ef76-710">Az.DataLakeStore</span></span>
* <span data-ttu-id="8ef76-711">Lägger till stöd för regler för virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="8ef76-711">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="8ef76-712">Get-AzDataLakeStoreVirtualNetworkRule: Hämtar eller listar regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8ef76-712">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="8ef76-713">Add-AzDataLakeStoreVirtualNetworkRule: Lägger till en regel för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="8ef76-713">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="8ef76-714">Set-AzDataLakeStoreVirtualNetworkRule: Ändrar den angivna regeln för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="8ef76-714">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="8ef76-715">Remove-AzDataLakeStoreVirtualNetworkRule: Tar bort en regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8ef76-715">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8ef76-716">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8ef76-716">Az.Network</span></span>
* <span data-ttu-id="8ef76-717">Skicka protokollvärdet till serverdelen för att uppdatera cmdleten Test-AzNetworkWatcherConnectivity.</span><span class="sxs-lookup"><span data-stu-id="8ef76-717">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="8ef76-718">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="8ef76-718">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8ef76-719">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8ef76-719">Az.Resources</span></span>
* <span data-ttu-id="8ef76-720">Åtgärdade problem där Get-AzRoleDefinition genererar ett oläsligt undantag (när standardprofilen inte innehåller någon prenumeration och ingen omfattning har angetts) genom att lägga till ett beskrivande undantag i scenariot.</span><span class="sxs-lookup"><span data-stu-id="8ef76-720">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="8ef76-721">Ställ in ”RoleDefinitionNameParameterSet” som standardparameteruppsättning.</span><span class="sxs-lookup"><span data-stu-id="8ef76-721">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="8ef76-722">0.3.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="8ef76-722">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="8ef76-723">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="8ef76-723">Azure.Storage</span></span>
* <span data-ttu-id="8ef76-724">Åtgärda fel där Kopiera blob/fil inte kopierar metadata när målplatsen har ett problem med metadata</span><span class="sxs-lookup"><span data-stu-id="8ef76-724">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="8ef76-725">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="8ef76-725">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="8ef76-726">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="8ef76-726">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="8ef76-727">Stöd för att hämta användningsinformation om en Storage-resurs för en specifik plats och för att lägga till ett varningsmeddelande för att hämta användningsinformation om en global Storage-resurs är inaktuellt.</span><span class="sxs-lookup"><span data-stu-id="8ef76-727">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="8ef76-728">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="8ef76-728">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="8ef76-729">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8ef76-729">Az.CognitiveServices</span></span>
* <span data-ttu-id="8ef76-730">Stöd för Get-AzCognitiveServicesAccountSkus utan ett befintligt konto.</span><span class="sxs-lookup"><span data-stu-id="8ef76-730">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8ef76-731">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8ef76-731">Az.Compute</span></span>
* <span data-ttu-id="8ef76-732">Åtgärdade fel där Get-AzVM -ResourceGroupName <rg> returnerar fler än 50 resultat om det behövs</span><span class="sxs-lookup"><span data-stu-id="8ef76-732">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="8ef76-733">Lade till ett exempel för SimpleParameterSet i hjälpen för cmdleten New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="8ef76-733">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="8ef76-734">Ett stavfel i förloppsmeddelandet för Azure Disk Encryption har korrigerats</span><span class="sxs-lookup"><span data-stu-id="8ef76-734">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="8ef76-735">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="8ef76-735">Az.DataFactoryV2</span></span>
* <span data-ttu-id="8ef76-736">ADF .Net SDK-versionen har uppdaterats till 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="8ef76-736">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8ef76-737">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8ef76-737">Az.Network</span></span>
* <span data-ttu-id="8ef76-738">Funktionalitet för NetworkProfile har lagts till.</span><span class="sxs-lookup"><span data-stu-id="8ef76-738">Added NetworkProfile functionality.</span></span> <span data-ttu-id="8ef76-739">nya cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="8ef76-739">new cmdlets added</span></span>
    - <span data-ttu-id="8ef76-740">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8ef76-740">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="8ef76-741">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8ef76-741">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="8ef76-742">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8ef76-742">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="8ef76-743">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8ef76-743">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="8ef76-744">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="8ef76-744">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="8ef76-745">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="8ef76-745">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="8ef76-746">Länk för tjänstassociering på modell för undernät har lagts till</span><span class="sxs-lookup"><span data-stu-id="8ef76-746">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="8ef76-747">Cmdletarna New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap och Remove-AzVirtualNetworkTap har lagts till</span><span class="sxs-lookup"><span data-stu-id="8ef76-747">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="8ef76-748">Cmdletarna Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig och Remove-AzNEtworkInterfaceTapConfig har lagts till</span><span class="sxs-lookup"><span data-stu-id="8ef76-748">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="8ef76-749">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="8ef76-749">Az.RedisCache</span></span>
* <span data-ttu-id="8ef76-750">Tillåt att alla strängar används som storleksparametrar framöver.</span><span class="sxs-lookup"><span data-stu-id="8ef76-750">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="8ef76-751">Lägg till P5 i popup-fönstret PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="8ef76-751">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="8ef76-752">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8ef76-752">Az.Resources</span></span>
* <span data-ttu-id="8ef76-753">Parametern -Mode som saknades i Set-AzPolicyDefinition har lagts till</span><span class="sxs-lookup"><span data-stu-id="8ef76-753">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="8ef76-754">Åtgärdade buggen för cmdleten Get-AzProviderOperation för åtgärder med ursprung som innehåller användare</span><span class="sxs-lookup"><span data-stu-id="8ef76-754">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="8ef76-755">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8ef76-755">Az.Sql</span></span>
* <span data-ttu-id="8ef76-756">Ett problem där vissa cmdletar för säkerhetskopiering inte kunde identifiera den aktuella azure-prenumerationen har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8ef76-756">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8ef76-757">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8ef76-757">Az.Websites</span></span>
* <span data-ttu-id="8ef76-758">Ny cmdlet: Get-AzWebAppContainerContinuousDeploymentUrl – Hämtar webhook-URL:en för kontinuerlig distribution av container</span><span class="sxs-lookup"><span data-stu-id="8ef76-758">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="8ef76-759">Nya cmdletar: New-AzWebAppContainerPSSession och Enter-WebAppContainerPSSession – Startar en PowerShell-fjärrsession i en containerapp för windows</span><span class="sxs-lookup"><span data-stu-id="8ef76-759">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="8ef76-760">0.2.0 – september 2018</span><span class="sxs-lookup"><span data-stu-id="8ef76-760">0.2.0 - September 2018</span></span>
 <span data-ttu-id="8ef76-761">Första versionen</span><span class="sxs-lookup"><span data-stu-id="8ef76-761">Initial Release</span></span>
