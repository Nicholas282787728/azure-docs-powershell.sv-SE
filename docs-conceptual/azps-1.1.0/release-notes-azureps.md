---
ms.openlocfilehash: 179d22fa065944695e4769f2698e3cabc7666b04
ms.sourcegitcommit: c6fd0e490fa0e33b8b768b679682a47d8faae1cf
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/16/2019
ms.locfileid: "54342155"
---
## <a name="110---january-2019"></a><span data-ttu-id="70591-101">1.1.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="70591-101">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="70591-102">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="70591-102">Az.Accounts</span></span>
* <span data-ttu-id="70591-103">Lade till omfattningen ”Lokal” till Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="70591-103">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="70591-104">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="70591-104">Az.Compute</span></span>
* <span data-ttu-id="70591-105">Namn är nu valfritt i ID-parametern för Restart/Start/Stop/Remove/Set-AzVM och Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="70591-105">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="70591-106">Uppdaterade beskrivningen av ID i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="70591-106">Updated the description of ID in help files</span></span>
* <span data-ttu-id="70591-107">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="70591-107">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="70591-108">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="70591-108">Az.DataLakeStore</span></span>
* <span data-ttu-id="70591-109">Uppdatera sdk-versionen av dataplanet till 1.1.14 för SDK-korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="70591-109">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="70591-110">Korrigerade hanteringen av negativ accesstime och modificationtime för getfilestatus och liststatus; korrigera asynkront annulleringstoken</span><span class="sxs-lookup"><span data-stu-id="70591-110">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="70591-111">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="70591-111">Az.EventGrid</span></span>
* <span data-ttu-id="70591-112">Uppdaterat för användning av API-versionen 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="70591-112">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="70591-113">Uppdaterade följande cmdletar för att stödja nytt scenario i API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="70591-113">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="70591-114">New-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="70591-114">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="70591-115">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="70591-115">Event Time-To-Live,</span></span>
        - <span data-ttu-id="70591-116">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="70591-116">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="70591-117">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="70591-117">Dead letter endpoint.</span></span>
    - <span data-ttu-id="70591-118">Update-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="70591-118">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="70591-119">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="70591-119">Event Time-To-Live,</span></span>
        - <span data-ttu-id="70591-120">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="70591-120">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="70591-121">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="70591-121">Dead letter endpoint.</span></span>
* <span data-ttu-id="70591-122">Lade till nya enum-värden (storageQueue och hybridConnection) för alternativet EndpointType i cmdletarna New-AzureRmEventGridSubscription och Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="70591-122">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="70591-123">Visa varningsmeddelanden om skapande eller uppdatering av händelseprenumerationen förväntas medföra manuell åtgärd från användaren.</span><span class="sxs-lookup"><span data-stu-id="70591-123">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="70591-124">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="70591-124">Az.IotHub</span></span>
* <span data-ttu-id="70591-125">Har uppdaterats till den senaste versionen av SDK:n lotHub</span><span class="sxs-lookup"><span data-stu-id="70591-125">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="70591-126">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="70591-126">Az.LogicApp</span></span>
* <span data-ttu-id="70591-127">Get-AzLogicApp visar en lista över alla som inte har angivet namn</span><span class="sxs-lookup"><span data-stu-id="70591-127">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="70591-128">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="70591-128">Az.Resources</span></span>
* <span data-ttu-id="70591-129">Åtgärdade problem med parameteruppsättningen när parametrarna -ODataQuery och -ResourceId anges för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="70591-129">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="70591-130">Mer information här: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="70591-130">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="70591-131">Åtgärdade hantering av parametern -Custom i New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="70591-131">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="70591-132">Korrigerade stavfel i New-AzDeployment-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="70591-132">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="70591-133">Gjorde parametern -MailNickname obligatorisk för New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="70591-133">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="70591-134">Mer information här: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="70591-134">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="70591-135">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="70591-135">Az.SignalR</span></span>
* <span data-ttu-id="70591-136">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="70591-136">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="70591-137">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="70591-137">Az.Sql</span></span>
* <span data-ttu-id="70591-138">Konverterade lagringshanteringsklientens beroende av den normala SDK-implementeringen.</span><span class="sxs-lookup"><span data-stu-id="70591-138">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="70591-139">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="70591-139">Az.Storage</span></span>
* <span data-ttu-id="70591-140">Angav StorageAccountName för lagringskontext som det verkliga namnet på lagringskontot när det skapas med Sas Token, OAuth eller Anonymous</span><span class="sxs-lookup"><span data-stu-id="70591-140">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="70591-141">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="70591-141">New-AzStorageContext</span></span>
* <span data-ttu-id="70591-142">Skapade Sas Token för Blob Snapshot-objekt med parametern -FullUri, åtgärdade den returnerade URI:n så att den blir URI för ögonblicksbild</span><span class="sxs-lookup"><span data-stu-id="70591-142">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="70591-143">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="70591-143">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="70591-144">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="70591-144">Az.Websites</span></span>
* <span data-ttu-id="70591-145">Åtgärdade en bugg i datumparsningen i Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="70591-145">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="70591-146">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="70591-146">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="70591-147">1.0.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="70591-147">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="70591-148">Allmänt</span><span class="sxs-lookup"><span data-stu-id="70591-148">General</span></span>

- <span data-ttu-id="70591-149">Allmän tillgänglighet för Az-modulen</span><span class="sxs-lookup"><span data-stu-id="70591-149">General Availability of Az Module</span></span>
- <span data-ttu-id="70591-150">Onlinehjälp för varje modul</span><span class="sxs-lookup"><span data-stu-id="70591-150">Online help for each module</span></span>
- <span data-ttu-id="70591-151">Mer information och en översikt finns på [Az-informationssidan](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="70591-151">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="70591-152">Information om hur du migrerar från AzureRM finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="70591-152">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="70591-153">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="70591-153">Az.Accounts</span></span>
- <span data-ttu-id="70591-154">Har ändrats från Az.Profile</span><span class="sxs-lookup"><span data-stu-id="70591-154">Changed from Az.Profile</span></span>
- <span data-ttu-id="70591-155">Fasta tabellformat för profil- och kontexttyper</span><span class="sxs-lookup"><span data-stu-id="70591-155">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="70591-156">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="70591-156">Az.ApiManagement</span></span>
- <span data-ttu-id="70591-157">Korrigeringar för #7002</span><span class="sxs-lookup"><span data-stu-id="70591-157">Fixes for #7002</span></span>
- <span data-ttu-id="70591-158">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="70591-158">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="70591-159">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="70591-159">Az.Batch</span></span>
- <span data-ttu-id="70591-160">Lade till möjligheten att se vilken version av Azure Batch Node Agent som körs på var och en av de virtuella datorerna i en pool, via den nya egenskapen `NodeAgentInformation` på `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="70591-160">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="70591-161">Standarden `Caching` för `PSDataDisk` är nu `ReadWrite` i stället för `None`.</span><span class="sxs-lookup"><span data-stu-id="70591-161">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="70591-162">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="70591-162">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="70591-163">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="70591-163">Az.Billing</span></span>
- <span data-ttu-id="70591-164">Kombinerar cmdletarna för fakturering, förbrukning och UsageAggregates. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="70591-164">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="70591-165">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="70591-165">Az.CognitivServices</span></span>
- <span data-ttu-id="70591-166">Lade till kompletterare för SkuName och Typem som är tillgängliga i New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="70591-166">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="70591-167">Tog bort parameteruppsättningen GetSkusWithAccountParamSetName från Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="70591-167">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="70591-168">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="70591-168">Az.ContainerInstance</span></span>
- <span data-ttu-id="70591-169">Stöd för ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="70591-169">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="70591-170">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="70591-170">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="70591-171">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="70591-171">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="70591-172">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="70591-172">Az.DataLakeStore</span></span>
- <span data-ttu-id="70591-173">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="70591-173">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="70591-174">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="70591-174">Az.Monitor</span></span>
- <span data-ttu-id="70591-175">Döpte om Az.Insights till Az.Monitor och andra mindre icke-bakåtkompatibla ändringar. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="70591-175">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="70591-176">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="70591-176">Az.KeyVault</span></span>
- <span data-ttu-id="70591-177">Tog bort den inaktuella egenskapen PurgeDisabled från utdatatyper</span><span class="sxs-lookup"><span data-stu-id="70591-177">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="70591-178">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="70591-178">Az.MachineLearning</span></span>
- <span data-ttu-id="70591-179">Inkluderade cmdletarna från modulen Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="70591-179">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="70591-180">Az.Media</span><span class="sxs-lookup"><span data-stu-id="70591-180">Az.Media</span></span>
- <span data-ttu-id="70591-181">Tog bort inaktuella -Tags-alias från New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="70591-181">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="70591-182">Az.Network</span><span class="sxs-lookup"><span data-stu-id="70591-182">Az.Network</span></span>
<span data-ttu-id="70591-183">Stöd har lagts till för konfiguration av RewriteRuleSets i Application Gateway</span><span class="sxs-lookup"><span data-stu-id="70591-183">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="70591-184">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="70591-184">New cmdlets added:</span></span>
        - <span data-ttu-id="70591-185">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="70591-185">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="70591-186">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="70591-186">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="70591-187">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="70591-187">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="70591-188">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="70591-188">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="70591-189">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="70591-189">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="70591-190">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="70591-190">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="70591-191">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="70591-191">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="70591-192">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="70591-192">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="70591-193">Cmdletar har uppdaterats med den valfria parametern -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="70591-193">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="70591-194">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="70591-194">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="70591-195">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="70591-195">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="70591-196">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="70591-196">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="70591-197">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="70591-197">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="70591-198">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="70591-198">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="70591-199">New-AzureRmApplicationGatewayUrlPathMapConfig har lagt till KeyVault-stöd för Application Gateway med Identity.</span><span class="sxs-lookup"><span data-stu-id="70591-199">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="70591-200">Cmdletar har uppdaterats med den valfria parametern -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="70591-200">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="70591-201">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="70591-201">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="70591-202">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="70591-202">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="70591-203">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="70591-203">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="70591-204">Cmdleten New-AzApplicationGateway har uppdaterats med den valfria parametern -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="70591-204">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="70591-205">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="70591-205">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="70591-206">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="70591-206">Az.OperationalInsights</span></span>
- <span data-ttu-id="70591-207">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="70591-207">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="70591-208">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="70591-208">Az.Profile</span></span>
- <span data-ttu-id="70591-209">Modulnamnet har ändrats till Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="70591-209">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="70591-210">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="70591-210">Az.RecoveryServices</span></span>
- <span data-ttu-id="70591-211">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="70591-211">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="70591-212">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="70591-212">Az.Resources</span></span>
- <span data-ttu-id="70591-213">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="70591-213">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="70591-214">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="70591-214">Az.ServiceFabric</span></span>
- <span data-ttu-id="70591-215">Stöd för specificering av certifikat efter eget namn och tumavtryck</span><span class="sxs-lookup"><span data-stu-id="70591-215">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="70591-216">Information om fler icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="70591-216">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="70591-217">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="70591-217">Az.SIgnalR</span></span>
- <span data-ttu-id="70591-218">Allmän tillgänglighet för PowerShell-cmdletar för SIgnalR</span><span class="sxs-lookup"><span data-stu-id="70591-218">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="70591-219">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="70591-219">Az.Sql</span></span>
- <span data-ttu-id="70591-220">Lade till de nya identifieringstyperna Data_Exfiltration och Unsafe_Action i Threat Detection-cmdletar</span><span class="sxs-lookup"><span data-stu-id="70591-220">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="70591-221">Uppdaterade dokumentationsexempel för Sql Auditing-cmdletar</span><span class="sxs-lookup"><span data-stu-id="70591-221">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="70591-222">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="70591-222">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="70591-223">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="70591-223">Az.Storage</span></span>
- <span data-ttu-id="70591-224">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="70591-224">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="70591-225">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="70591-225">Az.Websites</span></span>
- <span data-ttu-id="70591-226">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="70591-226">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="70591-227">0.7.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="70591-227">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="70591-228">Allmänt</span><span class="sxs-lookup"><span data-stu-id="70591-228">General</span></span>

* <span data-ttu-id="70591-229">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="70591-229">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="70591-230">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="70591-230">Az.Compute</span></span>

* <span data-ttu-id="70591-231">Lade till stöd för UltraSSD och Galleriavbildningar i de enkla parameteruppsättningarna för `New-AzVm(ss)`-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="70591-231">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="70591-232">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="70591-232">Az.DataLakeStore</span></span>

* <span data-ttu-id="70591-233">Åtgärdade avslutande snedstreck i domänen för adls-konto</span><span class="sxs-lookup"><span data-stu-id="70591-233">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="70591-234">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="70591-234">Az.FrontDoor</span></span>

* <span data-ttu-id="70591-235">Brutna länkar korrigerades</span><span class="sxs-lookup"><span data-stu-id="70591-235">Fixed some broken links</span></span>
    - <span data-ttu-id="70591-236">I artiklarna New-AzureRmFrontDoor och Set-AzureRmFrontDoor artiklar korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="70591-236">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="70591-237">I artikeln New-AzureRmFrontDoorManagedRuleObject korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="70591-237">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="70591-238">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="70591-238">Az.RecoveryServices</span></span>

* <span data-ttu-id="70591-239">Lade till valideringar på klientsidan för Azure-filresurs med återställningsåtgärder.</span><span class="sxs-lookup"><span data-stu-id="70591-239">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="70591-240">Gjorde storageAccountName och storageAccountResourceGroupName valfritt för afs-återställning.</span><span class="sxs-lookup"><span data-stu-id="70591-240">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="70591-241">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="70591-241">Az.Resources</span></span>

* <span data-ttu-id="70591-242">Korrigering för https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="70591-242">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="70591-243">Uppdaterade Get-AzureRmRoleAssignment så att prenumerationsomfattningen används om den anges vid begäran om klassiska administratörer.</span><span class="sxs-lookup"><span data-stu-id="70591-243">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="70591-244">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="70591-244">Az.Sql</span></span>

* <span data-ttu-id="70591-245">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="70591-245">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="70591-246">Korrigerade ett problem med Get-AzureRmSqlDatabaseVulnerabilityAssessment med DotNet-kärna</span><span class="sxs-lookup"><span data-stu-id="70591-246">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="70591-247">Ändrade dokumentationen för hjälpmeddelanden som rör SQL Auditing-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="70591-247">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="70591-248">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="70591-248">Az.Storage</span></span>

* <span data-ttu-id="70591-249">Lade till -EnableHierarchicalNamespace i New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="70591-249">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="70591-250">Åtgärdade problemet med att cmdleten Copy File inte kunde återanvända källkontexten på målet om inte -DestContext angetts</span><span class="sxs-lookup"><span data-stu-id="70591-250">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="70591-251">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="70591-251">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="70591-252">Stöd för statisk webbplatskonfiguration</span><span class="sxs-lookup"><span data-stu-id="70591-252">Support Static Website configuration</span></span>
    - <span data-ttu-id="70591-253">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="70591-253">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="70591-254">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="70591-254">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="70591-255">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="70591-255">Az.Websites</span></span>

* <span data-ttu-id="70591-256">Set-AzureRmWebApp och Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="70591-256">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="70591-257">Ny parameter (-AzureStoragePath) har lagts till för att ange att Azure Storage-sökvägar ska monteras i containerappar i Windows och Linux.</span><span class="sxs-lookup"><span data-stu-id="70591-257">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="70591-258">Använder utdata från den nya cmdleten New-AzureRmWebAppAzureStoragePath som en parameter för att ange sökvägar för Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="70591-258">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="70591-259">0.6.1 – november 2018</span><span class="sxs-lookup"><span data-stu-id="70591-259">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="70591-260">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="70591-260">Az.ApiManagement</span></span>
* <span data-ttu-id="70591-261">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="70591-261">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="70591-262">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="70591-262">Az.Automation</span></span>
* <span data-ttu-id="70591-263">Swagger baserade Azure Automation-cmdletar</span><span class="sxs-lookup"><span data-stu-id="70591-263">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="70591-264">Cmdletar för Uppdateringshantering har lagts till</span><span class="sxs-lookup"><span data-stu-id="70591-264">Added Update Management cmdlets</span></span>
* <span data-ttu-id="70591-265">Cmdletar för källkontroll har lagts till</span><span class="sxs-lookup"><span data-stu-id="70591-265">Added Source Control cmdlets</span></span>
* <span data-ttu-id="70591-266">Remove-AzureRmAutomationHybridWorkerGroup-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="70591-266">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="70591-267">Kommandot för DSC-registreringsnod har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="70591-267">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="70591-268">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="70591-268">Az.Compute</span></span>
* <span data-ttu-id="70591-269">Problem med SystemAssigned-identitet har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="70591-269">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="70591-270">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="70591-270">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="70591-271">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="70591-271">Az.ContainerInstance</span></span>
* <span data-ttu-id="70591-272">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="70591-272">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="70591-273">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="70591-273">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="70591-274">uppdatera exempelbeskrivningen för marketplace-cmdletar</span><span class="sxs-lookup"><span data-stu-id="70591-274">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="70591-275">Az.Network</span><span class="sxs-lookup"><span data-stu-id="70591-275">Az.Network</span></span>
* <span data-ttu-id="70591-276">Cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomErreller Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="70591-276">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="70591-277">ICMP tillbaka till stöd för Azure Firewall-nätverksprotokoll har lagts till</span><span class="sxs-lookup"><span data-stu-id="70591-277">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="70591-278">Uppdatera cmdlet Test-AzureRmNetworkWatcherConnectivity, lägga till verifiering av mål-id, adress och port.</span><span class="sxs-lookup"><span data-stu-id="70591-278">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="70591-279">Åtgärda problem med minnesanvändning i VirtualNetwork-karta</span><span class="sxs-lookup"><span data-stu-id="70591-279">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="70591-280">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="70591-280">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="70591-281">Åtgärda för att ändra principen för en skyddad fildelning.</span><span class="sxs-lookup"><span data-stu-id="70591-281">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="70591-282">Tidszonsprincipen har konverterats till versaler.</span><span class="sxs-lookup"><span data-stu-id="70591-282">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="70591-283">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="70591-283">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="70591-284">Exempel i New-AzureRmRecoveryServicesAsrProtectableItem har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="70591-284">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="70591-285">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="70591-285">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="70591-286">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="70591-286">Az.Relay</span></span>
* <span data-ttu-id="70591-287">Valfri parameter -KeyValue till New-AzureRmRelayKey cmdlet har lagts till, vilket gör det möjligt för användare att tillhandahålla KeyValue.</span><span class="sxs-lookup"><span data-stu-id="70591-287">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="70591-288">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="70591-288">Az.Resources</span></span>
* <span data-ttu-id="70591-289">Uppdatera hjälpdokumentation för resursidentitet kopplad till parametrar i `New-AzureRmPolicyAssignment` och `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="70591-289">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="70591-290">Lägg till ett exempel för New-AzureRmPolicyDefinition som använder -Metadata</span><span class="sxs-lookup"><span data-stu-id="70591-290">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="70591-291">Korrigera så att skiftläge behålls i taggnycklar i NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="70591-291">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="70591-292">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="70591-292">Az.ServiceFabric</span></span>
* <span data-ttu-id="70591-293">Lägg till utfasningsmeddelanden för kommande icke-kompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="70591-293">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="70591-294">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="70591-294">Az.Sql</span></span>
* <span data-ttu-id="70591-295">Nya cmdletar för CRUD-åtgärder på Azure Sql Database-hanterad instans och Azure Sql-hanterad databas</span><span class="sxs-lookup"><span data-stu-id="70591-295">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="70591-296">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="70591-296">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="70591-297">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="70591-297">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="70591-298">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="70591-298">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="70591-299">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="70591-299">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="70591-300">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="70591-300">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="70591-301">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="70591-301">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="70591-302">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="70591-302">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="70591-303">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="70591-303">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="70591-304">Hantering av utökad granskningsprincip på en server eller en databas har aktiverats.</span><span class="sxs-lookup"><span data-stu-id="70591-304">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="70591-305">Ny parameter (PredicateExpression) har lagts till för att aktivera filtrering av granskningsloggar.</span><span class="sxs-lookup"><span data-stu-id="70591-305">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="70591-306">Cmdletar har ändrats så att de använder SQL-klienter i stället för äldre klienter.</span><span class="sxs-lookup"><span data-stu-id="70591-306">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="70591-307">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="70591-307">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="70591-308">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="70591-308">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="70591-309">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="70591-309">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="70591-310">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="70591-310">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="70591-311">Problem med att använda Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings med lagringskontots namnparameter har korrigerats</span><span class="sxs-lookup"><span data-stu-id="70591-311">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="70591-312">0.5.0 – november 2018</span><span class="sxs-lookup"><span data-stu-id="70591-312">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="70591-313">Allmänt</span><span class="sxs-lookup"><span data-stu-id="70591-313">General</span></span>
* <span data-ttu-id="70591-314">Lade till resurskompletterare till många kärn-cmdletar – dessa gör att du kan stega genom befintliga resursnamn med TABB vid interaktiva anrop till cmdletar</span><span class="sxs-lookup"><span data-stu-id="70591-314">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="70591-315">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="70591-315">Az.Profile</span></span>
* <span data-ttu-id="70591-316">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="70591-316">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="70591-317">Bytte namn på parametern TenantId i cmdleten Connect-AzAccount till Tenant och lade till ett alias för TenantId</span><span class="sxs-lookup"><span data-stu-id="70591-317">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="70591-318">Uppdaterade TenantId-beskrivningen för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="70591-318">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="70591-319">Åtgärda felmeddelande för misslyckad inloggning när du tillhandahåller klientdomän</span><span class="sxs-lookup"><span data-stu-id="70591-319">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="70591-320">Åtgärda problem med att kontextnamn hamnar i konflikt för konton utan prenumerationer i klientorganisationen</span><span class="sxs-lookup"><span data-stu-id="70591-320">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="70591-321">Åtgärda problem med DataLake-slutpunkter vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="70591-321">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="70591-322">Åtgärdade problem med att Disconnect-AzAccount kastades om den inte anslöts</span><span class="sxs-lookup"><span data-stu-id="70591-322">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="70591-323">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="70591-323">Az.CognitiveServices</span></span>
* <span data-ttu-id="70591-324">Lade till åtgärden Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="70591-324">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="70591-325">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="70591-325">Az.Compute</span></span>
* <span data-ttu-id="70591-326">Lade till cmdletarna Add-AzVmssVMDataDisk och Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="70591-326">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="70591-327">Get-AzVMImage visar AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="70591-327">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="70591-328">Åtgärdade att värdena för alternativen SetAzVMChefExtension -BootstrapOptions och -JsonAttribute inte angavs i json-format.</span><span class="sxs-lookup"><span data-stu-id="70591-328">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="70591-329">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="70591-329">Az.DataLakeStore</span></span>
* <span data-ttu-id="70591-330">Uppdatera DataLake-paketet till 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="70591-330">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="70591-331">Lägg till standardsamtidighet för flertrådade åtgärder.</span><span class="sxs-lookup"><span data-stu-id="70591-331">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="70591-332">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="70591-332">Az.Insights</span></span>
* <span data-ttu-id="70591-333">Åtgärdade problem #7267 (autoskalningsområde)</span><span class="sxs-lookup"><span data-stu-id="70591-333">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="70591-334">Problem med att uppräknade parametrar inte ställdes in ordentligt när du skapade en ny autoskalningsregel (de ställdes alltid in med standardvärdet).</span><span class="sxs-lookup"><span data-stu-id="70591-334">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="70591-335">Åtgärdade problem #7513 [Insights] Set-AzDiagnosticSetting kräver uttrycklig specifikation av kategorier när inställningar skapas</span><span class="sxs-lookup"><span data-stu-id="70591-335">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="70591-336">Nu kräver inte cmdleten uttrycklig anvisning av kategorierna för att aktiveras under skapande, d.v.s. den fungerar enligt beskrivning</span><span class="sxs-lookup"><span data-stu-id="70591-336">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="70591-337">Az.Network</span><span class="sxs-lookup"><span data-stu-id="70591-337">Az.Network</span></span>
* <span data-ttu-id="70591-338">PeeringType ändrades till en obligatorisk parameter för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="70591-338">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="70591-339">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="70591-339">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="70591-340">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="70591-340">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="70591-341">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="70591-341">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="70591-342">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="70591-342">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="70591-343">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="70591-343">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="70591-344">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="70591-344">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="70591-345">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="70591-345">Az.PolicyInsights</span></span>
* <span data-ttu-id="70591-346">Cmdletar för principreparation har lagts till</span><span class="sxs-lookup"><span data-stu-id="70591-346">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="70591-347">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="70591-347">Az.Resources</span></span>
* <span data-ttu-id="70591-348">Korrigering för https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="70591-348">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="70591-349">Tillåt att resurser listas med parametern -ResourceId för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="70591-349">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="70591-350">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="70591-350">Az.ServiceBus</span></span>
* <span data-ttu-id="70591-351">Skrivskyddad MigrationState-egenskap har lagts till i PSServiceBusMigrationConfigurationAttributes, som hjälper till att hålla koll på migreringstillståndet.</span><span class="sxs-lookup"><span data-stu-id="70591-351">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="70591-352">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="70591-352">Az.ServiceFabric</span></span>
* <span data-ttu-id="70591-353">Åtgärda att lägga till certifikat till Linux-Vmss.</span><span class="sxs-lookup"><span data-stu-id="70591-353">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="70591-354">Åtgärdade Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="70591-354">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="70591-355">Använd rätt tumavtryck från nya certifikat (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="70591-355">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="70591-356">Visa undantag korrekt (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="70591-356">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="70591-357">Åtgärdade Update-AzServiceFabricDurability så att klusterkonfigurationen uppdateras innan Vmss-åtgärden CreateOrUpdate påbörjas.</span><span class="sxs-lookup"><span data-stu-id="70591-357">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="70591-358">0.4.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="70591-358">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="70591-359">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="70591-359">Az.Profile</span></span>
* <span data-ttu-id="70591-360">Åtgärdade problemet med Get-AzSubscription i CloudShell</span><span class="sxs-lookup"><span data-stu-id="70591-360">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="70591-361">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="70591-361">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="70591-362">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="70591-362">Az.Compute</span></span>
* <span data-ttu-id="70591-363">Nya storlekar lades till i listan över godkända VM-storlekar för vilka accelererat nätverk kommer att aktiveras vid användning av den enkla parameteruppsättningen för New-AzVm</span><span class="sxs-lookup"><span data-stu-id="70591-363">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="70591-364">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="70591-364">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="70591-365">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="70591-365">Az.DataLakeStore</span></span>
* <span data-ttu-id="70591-366">Lägger till stöd för virtuella nätverksregler</span><span class="sxs-lookup"><span data-stu-id="70591-366">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="70591-367">Get-AzDataLakeStoreVirtualNetworkRule: Hämtar eller listar regel för virtuellt Azure Data Lake Store-nätverk.</span><span class="sxs-lookup"><span data-stu-id="70591-367">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="70591-368">Add-AzDataLakeStoreVirtualNetworkRule: Lägger till en regel för det virtuella nätverket till det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="70591-368">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="70591-369">Set-AzDataLakeStoreVirtualNetworkRule: Ändrar den angivna regeln för det virtuella nätverket i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="70591-369">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="70591-370">Remove-AzDataLakeStoreVirtualNetworkRule: Tar bort en regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="70591-370">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="70591-371">Az.Network</span><span class="sxs-lookup"><span data-stu-id="70591-371">Az.Network</span></span>
* <span data-ttu-id="70591-372">Skicka protokollvärdet till serverdelen för att uppdatera cmdleten Test-AzNetworkWatcherConnectivity.</span><span class="sxs-lookup"><span data-stu-id="70591-372">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="70591-373">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="70591-373">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="70591-374">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="70591-374">Az.Resources</span></span>
* <span data-ttu-id="70591-375">Åtgärdade problem där Get-AzRoleDefinition genererar ett oläsligt undantag (när standardprofilen inte innehåller någon prenumeration och ingen omfattning har angetts) genom att lägga till ett beskrivande undantag i scenariot.</span><span class="sxs-lookup"><span data-stu-id="70591-375">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="70591-376">Ställ in ”RoleDefinitionNameParameterSet” som standardparameteruppsättning.</span><span class="sxs-lookup"><span data-stu-id="70591-376">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="70591-377">0.3.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="70591-377">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="70591-378">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="70591-378">Azure.Storage</span></span>
* <span data-ttu-id="70591-379">Åtgärda fel där Kopiera blob/fil inte kopierar metadata när målplatsen har ett problem med metadata</span><span class="sxs-lookup"><span data-stu-id="70591-379">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="70591-380">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="70591-380">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="70591-381">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="70591-381">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="70591-382">Stöd för att hämta användningsinformation om en Storage-resurs för en specifik plats och för att lägga till ett varningsmeddelande för att hämta användningsinformation om en global Storage-resurs är inaktuellt.</span><span class="sxs-lookup"><span data-stu-id="70591-382">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="70591-383">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="70591-383">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="70591-384">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="70591-384">Az.CognitiveServices</span></span>
* <span data-ttu-id="70591-385">Stöd för Get-AzCognitiveServicesAccountSkus utan ett befintligt konto.</span><span class="sxs-lookup"><span data-stu-id="70591-385">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="70591-386">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="70591-386">Az.Compute</span></span>
* <span data-ttu-id="70591-387">Åtgärdade fel där Get-AzVM -ResourceGroupName <rg> returnerar fler än 50 resultat om det behövs</span><span class="sxs-lookup"><span data-stu-id="70591-387">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="70591-388">Lade till ett exempel för SimpleParameterSet i hjälpen för cmdleten New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="70591-388">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="70591-389">Ett stavfel i förloppsmeddelandet för Azure Disk Encryption har korrigerats</span><span class="sxs-lookup"><span data-stu-id="70591-389">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="70591-390">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="70591-390">Az.DataFactoryV2</span></span>
* <span data-ttu-id="70591-391">ADF .Net SDK-versionen har uppdaterats till 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="70591-391">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="70591-392">Az.Network</span><span class="sxs-lookup"><span data-stu-id="70591-392">Az.Network</span></span>
* <span data-ttu-id="70591-393">Funktionalitet för NetworkProfile har lagts till.</span><span class="sxs-lookup"><span data-stu-id="70591-393">Added NetworkProfile functionality.</span></span> <span data-ttu-id="70591-394">nya cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="70591-394">new cmdlets added</span></span>
    - <span data-ttu-id="70591-395">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="70591-395">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="70591-396">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="70591-396">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="70591-397">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="70591-397">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="70591-398">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="70591-398">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="70591-399">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="70591-399">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="70591-400">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="70591-400">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="70591-401">Länk för tjänstassociering på modell för undernät har lagts till</span><span class="sxs-lookup"><span data-stu-id="70591-401">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="70591-402">Cmdletarna New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap och Remove-AzVirtualNetworkTap har lagts till</span><span class="sxs-lookup"><span data-stu-id="70591-402">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="70591-403">Cmdletarna Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig och Remove-AzNEtworkInterfaceTapConfig har lagts till</span><span class="sxs-lookup"><span data-stu-id="70591-403">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="70591-404">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="70591-404">Az.RedisCache</span></span>
* <span data-ttu-id="70591-405">Tillåt att alla strängar används som storleksparametrar framöver.</span><span class="sxs-lookup"><span data-stu-id="70591-405">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="70591-406">Lägg till P5 i popup-fönstret PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="70591-406">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="70591-407">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="70591-407">Az.Resources</span></span>
* <span data-ttu-id="70591-408">Parametern -Mode som saknades i Set-AzPolicyDefinition har lagts till</span><span class="sxs-lookup"><span data-stu-id="70591-408">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="70591-409">Åtgärdade buggen för cmdleten Get-AzProviderOperation för åtgärder med ursprung som innehåller användare</span><span class="sxs-lookup"><span data-stu-id="70591-409">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="70591-410">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="70591-410">Az.Sql</span></span>
* <span data-ttu-id="70591-411">Ett problem där vissa cmdletar för säkerhetskopiering inte kunde identifiera den aktuella azure-prenumerationen har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="70591-411">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="70591-412">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="70591-412">Az.Websites</span></span>
* <span data-ttu-id="70591-413">Ny cmdlet: Get-AzWebAppContainerContinuousDeploymentUrl – Hämtar webhook-URL:en för kontinuerlig distribution av container</span><span class="sxs-lookup"><span data-stu-id="70591-413">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="70591-414">Nya cmdletar: New-AzWebAppContainerPSSession och Enter-WebAppContainerPSSession – Startar en PowerShell-fjärrsession i en containerapp för windows</span><span class="sxs-lookup"><span data-stu-id="70591-414">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="70591-415">0.2.0 – september 2018</span><span class="sxs-lookup"><span data-stu-id="70591-415">0.2.0 - September 2018</span></span>
 <span data-ttu-id="70591-416">Första versionen</span><span class="sxs-lookup"><span data-stu-id="70591-416">Initial Release</span></span>