## <a name="100---december-2018"></a><span data-ttu-id="abad8-101">1.0.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="abad8-101">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="abad8-102">Allmänt</span><span class="sxs-lookup"><span data-stu-id="abad8-102">General</span></span>

- <span data-ttu-id="abad8-103">Allmän tillgänglighet för Az-modulen</span><span class="sxs-lookup"><span data-stu-id="abad8-103">General Availability of Az Module</span></span>
- <span data-ttu-id="abad8-104">Onlinehjälp för varje modul</span><span class="sxs-lookup"><span data-stu-id="abad8-104">Online help for each module</span></span>
- <span data-ttu-id="abad8-105">Mer information och en översikt finns på [Az-informationssidan](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="abad8-105">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="abad8-106">Information om hur du migrerar från AzureRM finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="abad8-106">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="abad8-107">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="abad8-107">Az.Accounts</span></span>
- <span data-ttu-id="abad8-108">Har ändrats från Az.Profile</span><span class="sxs-lookup"><span data-stu-id="abad8-108">Changed from Az.Profile</span></span>
- <span data-ttu-id="abad8-109">Fasta tabellformat för profil- och kontexttyper</span><span class="sxs-lookup"><span data-stu-id="abad8-109">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="abad8-110">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="abad8-110">Az.ApiManagement</span></span>
- <span data-ttu-id="abad8-111">Korrigeringar för #7002</span><span class="sxs-lookup"><span data-stu-id="abad8-111">Fixes for #7002</span></span>
- <span data-ttu-id="abad8-112">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="abad8-112">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="abad8-113">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="abad8-113">Az.Batch</span></span>
- <span data-ttu-id="abad8-114">Lade till möjligheten att se vilken version av Azure Batch Node Agent som körs på var och en av de virtuella datorerna i en pool, via den nya egenskapen `NodeAgentInformation` på `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="abad8-114">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="abad8-115">Standarden `Caching` för `PSDataDisk` är nu `ReadWrite` i stället för `None`.</span><span class="sxs-lookup"><span data-stu-id="abad8-115">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="abad8-116">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="abad8-116">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="abad8-117">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="abad8-117">Az.Billing</span></span>
- <span data-ttu-id="abad8-118">Kombinerar cmdletarna för fakturering, förbrukning och UsageAggregates. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="abad8-118">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="abad8-119">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="abad8-119">Az.CognitivServices</span></span>
- <span data-ttu-id="abad8-120">Lade till kompletterare för SkuName och Typem som är tillgängliga i New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="abad8-120">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="abad8-121">Tog bort parameteruppsättningen GetSkusWithAccountParamSetName från Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="abad8-121">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="abad8-122">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="abad8-122">Az.ContainerInstance</span></span>
- <span data-ttu-id="abad8-123">Stöd för ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="abad8-123">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="abad8-124">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="abad8-124">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="abad8-125">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="abad8-125">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="abad8-126">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="abad8-126">Az.DataLakeStore</span></span>
- <span data-ttu-id="abad8-127">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="abad8-127">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="abad8-128">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="abad8-128">Az.Monitor</span></span>
- <span data-ttu-id="abad8-129">Döpte om Az.Insights till Az.Monitor och andra mindre icke-bakåtkompatibla ändringar. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="abad8-129">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="abad8-130">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="abad8-130">Az.KeyVault</span></span>
- <span data-ttu-id="abad8-131">Tog bort den inaktuella egenskapen PurgeDisabled från utdatatyper</span><span class="sxs-lookup"><span data-stu-id="abad8-131">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="abad8-132">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="abad8-132">Az.MachineLearning</span></span>
- <span data-ttu-id="abad8-133">Inkluderade cmdletarna från modulen Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="abad8-133">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="abad8-134">Az.Media</span><span class="sxs-lookup"><span data-stu-id="abad8-134">Az.Media</span></span>
- <span data-ttu-id="abad8-135">Tog bort inaktuella -Tags-alias från New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="abad8-135">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="abad8-136">Az.Network</span><span class="sxs-lookup"><span data-stu-id="abad8-136">Az.Network</span></span>
<span data-ttu-id="abad8-137">Stöd har lagts till för konfiguration av RewriteRuleSets i Application Gateway</span><span class="sxs-lookup"><span data-stu-id="abad8-137">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="abad8-138">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="abad8-138">New cmdlets added:</span></span>
        - <span data-ttu-id="abad8-139">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="abad8-139">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="abad8-140">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="abad8-140">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="abad8-141">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="abad8-141">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="abad8-142">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="abad8-142">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="abad8-143">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="abad8-143">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="abad8-144">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="abad8-144">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="abad8-145">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="abad8-145">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="abad8-146">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="abad8-146">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="abad8-147">Cmdletar har uppdaterats med den valfria parametern -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="abad8-147">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="abad8-148">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="abad8-148">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="abad8-149">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="abad8-149">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="abad8-150">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="abad8-150">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="abad8-151">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="abad8-151">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="abad8-152">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="abad8-152">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="abad8-153">New-AzureRmApplicationGatewayUrlPathMapConfig har lagt till KeyVault-stöd för Application Gateway med Identity.</span><span class="sxs-lookup"><span data-stu-id="abad8-153">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="abad8-154">Cmdletar har uppdaterats med den valfria parametern -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="abad8-154">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="abad8-155">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="abad8-155">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="abad8-156">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="abad8-156">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="abad8-157">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="abad8-157">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="abad8-158">Cmdleten New-AzApplicationGateway har uppdaterats med den valfria parametern -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="abad8-158">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="abad8-159">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="abad8-159">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="abad8-160">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="abad8-160">Az.OperationalInsights</span></span>
- <span data-ttu-id="abad8-161">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="abad8-161">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="abad8-162">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="abad8-162">Az.Profile</span></span>
- <span data-ttu-id="abad8-163">Modulnamnet har ändrats till Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="abad8-163">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="abad8-164">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="abad8-164">Az.RecoveryServices</span></span>
- <span data-ttu-id="abad8-165">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="abad8-165">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="abad8-166">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="abad8-166">Az.Resources</span></span>
- <span data-ttu-id="abad8-167">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="abad8-167">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="abad8-168">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="abad8-168">Az.ServiceFabric</span></span>
- <span data-ttu-id="abad8-169">Stöd för specificering av certifikat efter eget namn och tumavtryck</span><span class="sxs-lookup"><span data-stu-id="abad8-169">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="abad8-170">Information om fler icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="abad8-170">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="abad8-171">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="abad8-171">Az.SIgnalR</span></span>
- <span data-ttu-id="abad8-172">Allmän tillgänglighet för PowerShell-cmdletar för SIgnalR</span><span class="sxs-lookup"><span data-stu-id="abad8-172">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="abad8-173">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="abad8-173">Az.Sql</span></span>
- <span data-ttu-id="abad8-174">Lade till de nya identifieringstyperna Data_Exfiltration och Unsafe_Action i Threat Detection-cmdletar</span><span class="sxs-lookup"><span data-stu-id="abad8-174">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="abad8-175">Uppdaterade dokumentationsexempel för Sql Auditing-cmdletar</span><span class="sxs-lookup"><span data-stu-id="abad8-175">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="abad8-176">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="abad8-176">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="abad8-177">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="abad8-177">Az.Storage</span></span>
- <span data-ttu-id="abad8-178">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="abad8-178">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="abad8-179">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="abad8-179">Az.Websites</span></span>
- <span data-ttu-id="abad8-180">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="abad8-180">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="abad8-181">0.7.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="abad8-181">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="abad8-182">Allmänt</span><span class="sxs-lookup"><span data-stu-id="abad8-182">General</span></span>

* <span data-ttu-id="abad8-183">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="abad8-183">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="abad8-184">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="abad8-184">Az.Compute</span></span>

* <span data-ttu-id="abad8-185">Lade till stöd för UltraSSD och Galleriavbildningar i de enkla parameteruppsättningarna för `New-AzVm(ss)`-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="abad8-185">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="abad8-186">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="abad8-186">Az.DataLakeStore</span></span>

* <span data-ttu-id="abad8-187">Åtgärdade avslutande snedstreck i domänen för adls-konto</span><span class="sxs-lookup"><span data-stu-id="abad8-187">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="abad8-188">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="abad8-188">Az.FrontDoor</span></span>

* <span data-ttu-id="abad8-189">Brutna länkar korrigerades</span><span class="sxs-lookup"><span data-stu-id="abad8-189">Fixed some broken links</span></span>
    - <span data-ttu-id="abad8-190">I artiklarna New-AzureRmFrontDoor och Set-AzureRmFrontDoor artiklar korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="abad8-190">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="abad8-191">I artikeln New-AzureRmFrontDoorManagedRuleObject korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="abad8-191">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="abad8-192">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="abad8-192">Az.RecoveryServices</span></span>

* <span data-ttu-id="abad8-193">Lade till valideringar på klientsidan för Azure-filresurs med återställningsåtgärder.</span><span class="sxs-lookup"><span data-stu-id="abad8-193">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="abad8-194">Gjorde storageAccountName och storageAccountResourceGroupName valfritt för afs-återställning.</span><span class="sxs-lookup"><span data-stu-id="abad8-194">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="abad8-195">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="abad8-195">Az.Resources</span></span>

* <span data-ttu-id="abad8-196">Korrigering för https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="abad8-196">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="abad8-197">Uppdaterade Get-AzureRmRoleAssignment så att prenumerationsomfattningen används om den anges vid begäran om klassiska administratörer.</span><span class="sxs-lookup"><span data-stu-id="abad8-197">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="abad8-198">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="abad8-198">Az.Sql</span></span>

* <span data-ttu-id="abad8-199">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="abad8-199">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="abad8-200">Korrigerade ett problem med Get-AzureRmSqlDatabaseVulnerabilityAssessment med DotNet-kärna</span><span class="sxs-lookup"><span data-stu-id="abad8-200">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="abad8-201">Ändrade dokumentationen för hjälpmeddelanden som rör SQL Auditing-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="abad8-201">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="abad8-202">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="abad8-202">Az.Storage</span></span>

* <span data-ttu-id="abad8-203">Lade till -EnableHierarchicalNamespace i New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="abad8-203">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="abad8-204">Åtgärdade problemet med att cmdleten Copy File inte kunde återanvända källkontexten på målet om inte -DestContext angetts</span><span class="sxs-lookup"><span data-stu-id="abad8-204">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="abad8-205">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="abad8-205">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="abad8-206">Stöd för statisk webbplatskonfiguration</span><span class="sxs-lookup"><span data-stu-id="abad8-206">Support Static Website configuration</span></span>
    - <span data-ttu-id="abad8-207">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="abad8-207">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="abad8-208">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="abad8-208">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="abad8-209">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="abad8-209">Az.Websites</span></span>

* <span data-ttu-id="abad8-210">Set-AzureRmWebApp och Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="abad8-210">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="abad8-211">Ny parameter (-AzureStoragePath) har lagts till för att ange att Azure Storage-sökvägar ska monteras i containerappar i Windows och Linux.</span><span class="sxs-lookup"><span data-stu-id="abad8-211">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="abad8-212">Använder utdata från den nya cmdleten New-AzureRmWebAppAzureStoragePath som en parameter för att ange sökvägar för Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="abad8-212">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="abad8-213">0.6.1 – november 2018</span><span class="sxs-lookup"><span data-stu-id="abad8-213">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="abad8-214">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="abad8-214">Az.ApiManagement</span></span>
* <span data-ttu-id="abad8-215">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="abad8-215">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="abad8-216">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="abad8-216">Az.Automation</span></span>
* <span data-ttu-id="abad8-217">Swagger baserade Azure Automation-cmdletar</span><span class="sxs-lookup"><span data-stu-id="abad8-217">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="abad8-218">Cmdletar för Uppdateringshantering har lagts till</span><span class="sxs-lookup"><span data-stu-id="abad8-218">Added Update Management cmdlets</span></span>
* <span data-ttu-id="abad8-219">Cmdletar för källkontroll har lagts till</span><span class="sxs-lookup"><span data-stu-id="abad8-219">Added Source Control cmdlets</span></span>
* <span data-ttu-id="abad8-220">Remove-AzureRmAutomationHybridWorkerGroup-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="abad8-220">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="abad8-221">Kommandot för DSC-registreringsnod har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="abad8-221">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="abad8-222">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="abad8-222">Az.Compute</span></span>
* <span data-ttu-id="abad8-223">Problem med SystemAssigned-identitet har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="abad8-223">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="abad8-224">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="abad8-224">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="abad8-225">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="abad8-225">Az.ContainerInstance</span></span>
* <span data-ttu-id="abad8-226">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="abad8-226">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="abad8-227">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="abad8-227">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="abad8-228">uppdatera exempelbeskrivningen för marketplace-cmdletar</span><span class="sxs-lookup"><span data-stu-id="abad8-228">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="abad8-229">Az.Network</span><span class="sxs-lookup"><span data-stu-id="abad8-229">Az.Network</span></span>
* <span data-ttu-id="abad8-230">Cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomErreller Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="abad8-230">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="abad8-231">ICMP tillbaka till stöd för Azure Firewall-nätverksprotokoll har lagts till</span><span class="sxs-lookup"><span data-stu-id="abad8-231">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="abad8-232">Uppdatera cmdlet Test-AzureRmNetworkWatcherConnectivity, lägga till verifiering av mål-id, adress och port.</span><span class="sxs-lookup"><span data-stu-id="abad8-232">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="abad8-233">Åtgärda problem med minnesanvändning i VirtualNetwork-karta</span><span class="sxs-lookup"><span data-stu-id="abad8-233">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="abad8-234">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="abad8-234">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="abad8-235">Åtgärda för att ändra principen för en skyddad fildelning.</span><span class="sxs-lookup"><span data-stu-id="abad8-235">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="abad8-236">Tidszonsprincipen har konverterats till versaler.</span><span class="sxs-lookup"><span data-stu-id="abad8-236">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="abad8-237">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="abad8-237">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="abad8-238">Exempel i New-AzureRmRecoveryServicesAsrProtectableItem har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="abad8-238">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="abad8-239">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="abad8-239">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="abad8-240">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="abad8-240">Az.Relay</span></span>
* <span data-ttu-id="abad8-241">Valfri parameter -KeyValue till New-AzureRmRelayKey cmdlet har lagts till, vilket gör det möjligt för användare att tillhandahålla KeyValue.</span><span class="sxs-lookup"><span data-stu-id="abad8-241">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="abad8-242">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="abad8-242">Az.Resources</span></span>
* <span data-ttu-id="abad8-243">Uppdatera hjälpdokumentation för resursidentitet kopplad till parametrar i `New-AzureRmPolicyAssignment` och `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="abad8-243">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="abad8-244">Lägg till ett exempel för New-AzureRmPolicyDefinition som använder -Metadata</span><span class="sxs-lookup"><span data-stu-id="abad8-244">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="abad8-245">Korrigera så att skiftläge behålls i taggnycklar i NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="abad8-245">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="abad8-246">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="abad8-246">Az.ServiceFabric</span></span>
* <span data-ttu-id="abad8-247">Lägg till utfasningsmeddelanden för kommande icke-kompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="abad8-247">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="abad8-248">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="abad8-248">Az.Sql</span></span>
* <span data-ttu-id="abad8-249">Nya cmdletar för CRUD-åtgärder på Azure Sql Database-hanterad instans och Azure Sql-hanterad databas</span><span class="sxs-lookup"><span data-stu-id="abad8-249">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="abad8-250">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="abad8-250">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="abad8-251">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="abad8-251">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="abad8-252">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="abad8-252">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="abad8-253">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="abad8-253">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="abad8-254">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="abad8-254">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="abad8-255">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="abad8-255">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="abad8-256">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="abad8-256">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="abad8-257">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="abad8-257">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="abad8-258">Hantering av utökad granskningsprincip på en server eller en databas har aktiverats.</span><span class="sxs-lookup"><span data-stu-id="abad8-258">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="abad8-259">Ny parameter (PredicateExpression) har lagts till för att aktivera filtrering av granskningsloggar.</span><span class="sxs-lookup"><span data-stu-id="abad8-259">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="abad8-260">Cmdletar har ändrats så att de använder SQL-klienter i stället för äldre klienter.</span><span class="sxs-lookup"><span data-stu-id="abad8-260">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="abad8-261">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="abad8-261">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="abad8-262">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="abad8-262">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="abad8-263">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="abad8-263">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="abad8-264">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="abad8-264">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="abad8-265">Problem med att använda Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings med lagringskontots namnparameter har korrigerats</span><span class="sxs-lookup"><span data-stu-id="abad8-265">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="abad8-266">0.5.0 – november 2018</span><span class="sxs-lookup"><span data-stu-id="abad8-266">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="abad8-267">Allmänt</span><span class="sxs-lookup"><span data-stu-id="abad8-267">General</span></span>
* <span data-ttu-id="abad8-268">Lade till resurskompletterare till många kärn-cmdletar – dessa gör att du kan stega genom befintliga resursnamn med TABB vid interaktiva anrop till cmdletar</span><span class="sxs-lookup"><span data-stu-id="abad8-268">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="abad8-269">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="abad8-269">Az.Profile</span></span>
* <span data-ttu-id="abad8-270">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="abad8-270">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="abad8-271">Bytte namn på parametern TenantId i cmdleten Connect-AzAccount till Tenant och lade till ett alias för TenantId</span><span class="sxs-lookup"><span data-stu-id="abad8-271">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="abad8-272">Uppdaterade TenantId-beskrivningen för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="abad8-272">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="abad8-273">Åtgärda felmeddelande för misslyckad inloggning när du tillhandahåller klientdomän</span><span class="sxs-lookup"><span data-stu-id="abad8-273">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="abad8-274">Åtgärda problem med att kontextnamn hamnar i konflikt för konton utan prenumerationer i klientorganisationen</span><span class="sxs-lookup"><span data-stu-id="abad8-274">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="abad8-275">Åtgärda problem med DataLake-slutpunkter vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="abad8-275">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="abad8-276">Åtgärdade problem med att Disconnect-AzAccount kastades om den inte anslöts</span><span class="sxs-lookup"><span data-stu-id="abad8-276">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="abad8-277">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="abad8-277">Az.CognitiveServices</span></span>
* <span data-ttu-id="abad8-278">Lade till åtgärden Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="abad8-278">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="abad8-279">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="abad8-279">Az.Compute</span></span>
* <span data-ttu-id="abad8-280">Lade till cmdletarna Add-AzVmssVMDataDisk och Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="abad8-280">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="abad8-281">Get-AzVMImage visar AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="abad8-281">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="abad8-282">Åtgärdade att värdena för alternativen SetAzVMChefExtension -BootstrapOptions och -JsonAttribute inte angavs i json-format.</span><span class="sxs-lookup"><span data-stu-id="abad8-282">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="abad8-283">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="abad8-283">Az.DataLakeStore</span></span>
* <span data-ttu-id="abad8-284">Uppdatera DataLake-paketet till 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="abad8-284">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="abad8-285">Lägg till standardsamtidighet för flertrådade åtgärder.</span><span class="sxs-lookup"><span data-stu-id="abad8-285">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="abad8-286">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="abad8-286">Az.Insights</span></span>
* <span data-ttu-id="abad8-287">Åtgärdade problem #7267 (autoskalningsområde)</span><span class="sxs-lookup"><span data-stu-id="abad8-287">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="abad8-288">Problem med att uppräknade parametrar inte ställdes in ordentligt när du skapade en ny autoskalningsregel (de ställdes alltid in med standardvärdet).</span><span class="sxs-lookup"><span data-stu-id="abad8-288">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="abad8-289">Åtgärdade problem #7513 [Insights] Set-AzDiagnosticSetting kräver uttrycklig specifikation av kategorier när inställningar skapas</span><span class="sxs-lookup"><span data-stu-id="abad8-289">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="abad8-290">Nu kräver inte cmdleten uttrycklig anvisning av kategorierna för att aktiveras under skapande, d.v.s. den fungerar enligt beskrivning</span><span class="sxs-lookup"><span data-stu-id="abad8-290">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="abad8-291">Az.Network</span><span class="sxs-lookup"><span data-stu-id="abad8-291">Az.Network</span></span>
* <span data-ttu-id="abad8-292">PeeringType ändrades till en obligatorisk parameter för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="abad8-292">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="abad8-293">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="abad8-293">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="abad8-294">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="abad8-294">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="abad8-295">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="abad8-295">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="abad8-296">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="abad8-296">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="abad8-297">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="abad8-297">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="abad8-298">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="abad8-298">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="abad8-299">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="abad8-299">Az.PolicyInsights</span></span>
* <span data-ttu-id="abad8-300">Cmdletar för principreparation har lagts till</span><span class="sxs-lookup"><span data-stu-id="abad8-300">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="abad8-301">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="abad8-301">Az.Resources</span></span>
* <span data-ttu-id="abad8-302">Korrigering för https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="abad8-302">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="abad8-303">Tillåt att resurser listas med parametern -ResourceId för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="abad8-303">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="abad8-304">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="abad8-304">Az.ServiceBus</span></span>
* <span data-ttu-id="abad8-305">Skrivskyddad MigrationState-egenskap har lagts till i PSServiceBusMigrationConfigurationAttributes, som hjälper till att hålla koll på migreringstillståndet.</span><span class="sxs-lookup"><span data-stu-id="abad8-305">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="abad8-306">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="abad8-306">Az.ServiceFabric</span></span>
* <span data-ttu-id="abad8-307">Åtgärda att lägga till certifikat till Linux-Vmss.</span><span class="sxs-lookup"><span data-stu-id="abad8-307">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="abad8-308">Åtgärdade Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="abad8-308">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="abad8-309">Använd rätt tumavtryck från nya certifikat (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="abad8-309">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="abad8-310">Visa undantag korrekt (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="abad8-310">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="abad8-311">Åtgärdade Update-AzServiceFabricDurability så att klusterkonfigurationen uppdateras innan Vmss-åtgärden CreateOrUpdate påbörjas.</span><span class="sxs-lookup"><span data-stu-id="abad8-311">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="abad8-312">0.4.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="abad8-312">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="abad8-313">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="abad8-313">Az.Profile</span></span>
* <span data-ttu-id="abad8-314">Åtgärdade problemet med Get-AzSubscription i CloudShell</span><span class="sxs-lookup"><span data-stu-id="abad8-314">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="abad8-315">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="abad8-315">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="abad8-316">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="abad8-316">Az.Compute</span></span>
* <span data-ttu-id="abad8-317">Nya storlekar lades till i listan över godkända VM-storlekar för vilka accelererat nätverk kommer att aktiveras vid användning av den enkla parameteruppsättningen för New-AzVm</span><span class="sxs-lookup"><span data-stu-id="abad8-317">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="abad8-318">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="abad8-318">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="abad8-319">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="abad8-319">Az.DataLakeStore</span></span>
* <span data-ttu-id="abad8-320">Lägger till stöd för virtuella nätverksregler</span><span class="sxs-lookup"><span data-stu-id="abad8-320">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="abad8-321">Get-AzDataLakeStoreVirtualNetworkRule: Hämtar eller listar regel för virtuellt Azure Data Lake Store-nätverk.</span><span class="sxs-lookup"><span data-stu-id="abad8-321">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="abad8-322">Add-AzDataLakeStoreVirtualNetworkRule: Lägger till en regel för det virtuella nätverket till det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="abad8-322">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="abad8-323">Set-AzDataLakeStoreVirtualNetworkRule: Ändrar den angivna regeln för det virtuella nätverket i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="abad8-323">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="abad8-324">Remove-AzDataLakeStoreVirtualNetworkRule: Tar bort en regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="abad8-324">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="abad8-325">Az.Network</span><span class="sxs-lookup"><span data-stu-id="abad8-325">Az.Network</span></span>
* <span data-ttu-id="abad8-326">Skicka protokollvärdet till serverdelen för att uppdatera cmdleten Test-AzNetworkWatcherConnectivity.</span><span class="sxs-lookup"><span data-stu-id="abad8-326">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="abad8-327">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="abad8-327">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="abad8-328">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="abad8-328">Az.Resources</span></span>
* <span data-ttu-id="abad8-329">Åtgärdade problem där Get-AzRoleDefinition genererar ett oläsligt undantag (när standardprofilen inte innehåller någon prenumeration och ingen omfattning har angetts) genom att lägga till ett beskrivande undantag i scenariot.</span><span class="sxs-lookup"><span data-stu-id="abad8-329">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="abad8-330">Ställ in ”RoleDefinitionNameParameterSet” som standardparameteruppsättning.</span><span class="sxs-lookup"><span data-stu-id="abad8-330">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="abad8-331">0.3.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="abad8-331">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="abad8-332">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="abad8-332">Azure.Storage</span></span>
* <span data-ttu-id="abad8-333">Åtgärda fel där Kopiera blob/fil inte kopierar metadata när målplatsen har ett problem med metadata</span><span class="sxs-lookup"><span data-stu-id="abad8-333">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="abad8-334">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="abad8-334">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="abad8-335">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="abad8-335">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="abad8-336">Stöd för att hämta användningsinformation om en Storage-resurs för en specifik plats och för att lägga till ett varningsmeddelande för att hämta användningsinformation om en global Storage-resurs är inaktuellt.</span><span class="sxs-lookup"><span data-stu-id="abad8-336">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="abad8-337">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="abad8-337">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="abad8-338">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="abad8-338">Az.CognitiveServices</span></span>
* <span data-ttu-id="abad8-339">Stöd för Get-AzCognitiveServicesAccountSkus utan ett befintligt konto.</span><span class="sxs-lookup"><span data-stu-id="abad8-339">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="abad8-340">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="abad8-340">Az.Compute</span></span>
* <span data-ttu-id="abad8-341">Åtgärdade fel där Get-AzVM -ResourceGroupName <rg> returnerar fler än 50 resultat om det behövs</span><span class="sxs-lookup"><span data-stu-id="abad8-341">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="abad8-342">Lade till ett exempel för SimpleParameterSet i hjälpen för cmdleten New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="abad8-342">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="abad8-343">Ett stavfel i förloppsmeddelandet för Azure Disk Encryption har korrigerats</span><span class="sxs-lookup"><span data-stu-id="abad8-343">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="abad8-344">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="abad8-344">Az.DataFactoryV2</span></span>
* <span data-ttu-id="abad8-345">ADF .Net SDK-versionen har uppdaterats till 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="abad8-345">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="abad8-346">Az.Network</span><span class="sxs-lookup"><span data-stu-id="abad8-346">Az.Network</span></span>
* <span data-ttu-id="abad8-347">Funktionalitet för NetworkProfile har lagts till.</span><span class="sxs-lookup"><span data-stu-id="abad8-347">Added NetworkProfile functionality.</span></span> <span data-ttu-id="abad8-348">nya cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="abad8-348">new cmdlets added</span></span>
    - <span data-ttu-id="abad8-349">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="abad8-349">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="abad8-350">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="abad8-350">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="abad8-351">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="abad8-351">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="abad8-352">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="abad8-352">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="abad8-353">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="abad8-353">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="abad8-354">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="abad8-354">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="abad8-355">Länk för tjänstassociering på modell för undernät har lagts till</span><span class="sxs-lookup"><span data-stu-id="abad8-355">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="abad8-356">Cmdletarna New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap och Remove-AzVirtualNetworkTap har lagts till</span><span class="sxs-lookup"><span data-stu-id="abad8-356">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="abad8-357">Cmdletarna Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig och Remove-AzNEtworkInterfaceTapConfig har lagts till</span><span class="sxs-lookup"><span data-stu-id="abad8-357">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="abad8-358">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="abad8-358">Az.RedisCache</span></span>
* <span data-ttu-id="abad8-359">Tillåt att alla strängar används som storleksparametrar framöver.</span><span class="sxs-lookup"><span data-stu-id="abad8-359">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="abad8-360">Lägg till P5 i popup-fönstret PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="abad8-360">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="abad8-361">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="abad8-361">Az.Resources</span></span>
* <span data-ttu-id="abad8-362">Parametern -Mode som saknades i Set-AzPolicyDefinition har lagts till</span><span class="sxs-lookup"><span data-stu-id="abad8-362">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="abad8-363">Åtgärdade buggen för cmdleten Get-AzProviderOperation för åtgärder med ursprung som innehåller användare</span><span class="sxs-lookup"><span data-stu-id="abad8-363">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="abad8-364">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="abad8-364">Az.Sql</span></span>
* <span data-ttu-id="abad8-365">Ett problem där vissa cmdletar för säkerhetskopiering inte kunde identifiera den aktuella azure-prenumerationen har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="abad8-365">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="abad8-366">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="abad8-366">Az.Websites</span></span>
* <span data-ttu-id="abad8-367">Ny cmdlet: Get-AzWebAppContainerContinuousDeploymentUrl – Hämtar webhook-URL:en för kontinuerlig distribution av container</span><span class="sxs-lookup"><span data-stu-id="abad8-367">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="abad8-368">Nya cmdletar: New-AzWebAppContainerPSSession och Enter-WebAppContainerPSSession – Startar en PowerShell-fjärrsession i en containerapp för windows</span><span class="sxs-lookup"><span data-stu-id="abad8-368">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="abad8-369">0.2.0 – september 2018</span><span class="sxs-lookup"><span data-stu-id="abad8-369">0.2.0 - September 2018</span></span>
 <span data-ttu-id="abad8-370">Första versionen</span><span class="sxs-lookup"><span data-stu-id="abad8-370">Initial Release</span></span>