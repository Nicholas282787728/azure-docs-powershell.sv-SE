## <a name="140---february-2019"></a><span data-ttu-id="5938a-101">1.4.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="5938a-101">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="5938a-102">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="5938a-102">Az.AnalysisServices</span></span>
* <span data-ttu-id="5938a-103">Inaktuell AddAzureASAccount-cmdlet</span><span class="sxs-lookup"><span data-stu-id="5938a-103">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="5938a-104">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5938a-104">Az.Automation</span></span>
* <span data-ttu-id="5938a-105">Hjälpen för Import-AzAutomationDscNodeConfiguration har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="5938a-105">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="5938a-106">Konfigurationsnamnsvalidering har lagts till i cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="5938a-106">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="5938a-107">Förbättrad felhantering för cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="5938a-107">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="5938a-108">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="5938a-108">Az.CognitiveServices</span></span>
* <span data-ttu-id="5938a-109">CustomSubdomainName har lagts till som en ny valfri parameter för New-AzCognitiveServicesAccount, som används för att ange underdomän för resursen.</span><span class="sxs-lookup"><span data-stu-id="5938a-109">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5938a-110">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5938a-110">Az.Compute</span></span>
* <span data-ttu-id="5938a-111">Problemet med ID-parameteruppsättningar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="5938a-111">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="5938a-112">Get-AzVMExtension har uppdaterats så att alla installerade tillägg visas om parametern Name inte har angetts</span><span class="sxs-lookup"><span data-stu-id="5938a-112">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="5938a-113">Parametrarna Tag och ResourceId har lagts till i cmdleten Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="5938a-113">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="5938a-114">Get-AzVmssVM utan instans-ID och med InstanceView kan visa virtuella VMSS-datorer med instansvyn.</span><span class="sxs-lookup"><span data-stu-id="5938a-114">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5938a-115">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5938a-115">Az.DataLakeStore</span></span>
* <span data-ttu-id="5938a-116">Cmdletar har lagts till för uppräkning och återställning av borttagna objekt i ADL</span><span class="sxs-lookup"><span data-stu-id="5938a-116">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="5938a-117">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="5938a-117">Az.EventHub</span></span>
* <span data-ttu-id="5938a-118">Ny boolesk egenskap SkipEmptyArchives har lagts till i Skip Empty Archives i CaptureDescription-klassen i Eventhub</span><span class="sxs-lookup"><span data-stu-id="5938a-118">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="5938a-119">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5938a-119">Az.KeyVault</span></span>
* <span data-ttu-id="5938a-120">Taggning i Set-AzKeyVaultSecret har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="5938a-120">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="5938a-121">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="5938a-121">Az.LogicApp</span></span>
* <span data-ttu-id="5938a-122">Grundläggande SKU har lagts till för Integrationskonton</span><span class="sxs-lookup"><span data-stu-id="5938a-122">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="5938a-123">XSLT 2.0, XSLT 3.0 och Flytande mappningstyper har lagts till</span><span class="sxs-lookup"><span data-stu-id="5938a-123">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="5938a-124">Nya cmdletar för integrationskontosammansättningar</span><span class="sxs-lookup"><span data-stu-id="5938a-124">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="5938a-125">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="5938a-125">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="5938a-126">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="5938a-126">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="5938a-127">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="5938a-127">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="5938a-128">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="5938a-128">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="5938a-129">Nya cmdletar för batchkonfiguration för integrationskonto</span><span class="sxs-lookup"><span data-stu-id="5938a-129">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="5938a-130">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="5938a-130">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="5938a-131">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="5938a-131">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="5938a-132">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="5938a-132">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="5938a-133">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="5938a-133">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="5938a-134">Logic App-SDK har uppdaterats till version 4.1.0</span><span class="sxs-lookup"><span data-stu-id="5938a-134">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="5938a-135">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5938a-135">Az.Monitor</span></span>
* <span data-ttu-id="5938a-136">Hjälpen för Get-AzMetric har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="5938a-136">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5938a-137">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5938a-137">Az.Network</span></span>
* <span data-ttu-id="5938a-138">Hjälpexempel för Add-AzApplicationGatewayCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="5938a-138">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="5938a-139">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="5938a-139">Az.OperationalInsights</span></span>
* <span data-ttu-id="5938a-140">Ytterligare stöd för datakällorna New och Get ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="5938a-140">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="5938a-141">Ny ApplicationInsights-typ har lagts till för att ge stöd för ”Get specific” och ”Get all” för ApplicationInsights-datakällor för angiven arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="5938a-141">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="5938a-142">Cmdleten New-AzOperationalInsightsApplicationInsightsDataSource har lagts till för att skapa datakälla med angivna parametrar för Application Insights-resurs: subscription Id, resourceGroupName och name.</span><span class="sxs-lookup"><span data-stu-id="5938a-142">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="5938a-143">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5938a-143">Az.Resources</span></span>
* <span data-ttu-id="5938a-144">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="5938a-144">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="5938a-145">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="5938a-145">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="5938a-146">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="5938a-146">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="5938a-147">Fel som gör att KeyCredentials inte kan skapas upprepade gånger har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="5938a-147">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="5938a-148">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5938a-148">Az.Sql</span></span>
* <span data-ttu-id="5938a-149">Stöd för nivån SQL DB-hyperskal har lagts till</span><span class="sxs-lookup"><span data-stu-id="5938a-149">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="5938a-150">Ett fel har åtgärdats där återställningen kunde misslyckas på grund av onödiga inställningsegenskaper i restore-förfrågan</span><span class="sxs-lookup"><span data-stu-id="5938a-150">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5938a-151">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5938a-151">Az.Websites</span></span>
* <span data-ttu-id="5938a-152">Rätt exempel i Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="5938a-152">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="5938a-153">1.3.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="5938a-153">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5938a-154">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5938a-154">Az.Accounts</span></span>
* <span data-ttu-id="5938a-155">Uppdatera till den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="5938a-155">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="5938a-156">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="5938a-156">Az.AnalysisServices</span></span>
<span data-ttu-id="5938a-157">Allmän tillgänglighet för Az.AnalysisServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="5938a-157">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5938a-158">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5938a-158">Az.Compute</span></span>
* <span data-ttu-id="5938a-159">AEM-tillägg: Lägg till stöd för UltraSSD-, P60-, P70- och P80-diskar</span><span class="sxs-lookup"><span data-stu-id="5938a-159">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="5938a-160">Uppdatera hjälpbeskrivning för Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="5938a-160">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="5938a-161">Uppdatera hjälpbeskrivning och exempel för Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="5938a-161">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5938a-162">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5938a-162">Az.RecoveryServices</span></span>
<span data-ttu-id="5938a-163">Allmän tillgänglighet för Az.RecoveryServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="5938a-163">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="5938a-164">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5938a-164">Az.Resources</span></span>
* <span data-ttu-id="5938a-165">Korrigera taggar för resursgrupper</span><span class="sxs-lookup"><span data-stu-id="5938a-165">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="5938a-166">Mer information här: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="5938a-166">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="5938a-167">Åtgärda problem där `Get-AzureRmRoleAssignment` inte respekterar -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="5938a-167">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="5938a-168">Mer information här: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="5938a-168">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="5938a-169">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5938a-169">Az.Sql</span></span>
* <span data-ttu-id="5938a-170">Lägga till Get/Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="5938a-170">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="5938a-171">Åtgärda problem där ett nullref-undantag uppstår när du kör SQL-cmdletar och inte är inloggad på ett Azure-konto</span><span class="sxs-lookup"><span data-stu-id="5938a-171">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="5938a-172">Åtgärda nullref-undantag i Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="5938a-172">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="5938a-173">1.2.1 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="5938a-173">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5938a-174">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5938a-174">Az.Accounts</span></span>
* <span data-ttu-id="5938a-175">Version med rätt version av autentisering</span><span class="sxs-lookup"><span data-stu-id="5938a-175">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="5938a-176">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="5938a-176">Az.AnalysisServices</span></span>
* <span data-ttu-id="5938a-177">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="5938a-177">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5938a-178">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5938a-178">Az.RecoveryServices</span></span>
* <span data-ttu-id="5938a-179">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="5938a-179">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="5938a-180">1.2.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="5938a-180">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5938a-181">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5938a-181">Az.Accounts</span></span>
* <span data-ttu-id="5938a-182">Lägga till interaktiv autentisering och autentisering med användarnamn/lösenord för endast Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="5938a-182">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="5938a-183">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="5938a-183">Update incorrect online help URLs</span></span>
* <span data-ttu-id="5938a-184">Lägga till varningsmeddelande i PS Core för Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="5938a-184">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="5938a-185">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="5938a-185">Az.Aks</span></span>
* <span data-ttu-id="5938a-186">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="5938a-186">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="5938a-187">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5938a-187">Az.Automation</span></span>
* <span data-ttu-id="5938a-188">Stöd för Python 2-runbookflöden har lagts till</span><span class="sxs-lookup"><span data-stu-id="5938a-188">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="5938a-189">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="5938a-189">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="5938a-190">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="5938a-190">Az.Cdn</span></span>
* <span data-ttu-id="5938a-191">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="5938a-191">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5938a-192">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5938a-192">Az.Compute</span></span>
* <span data-ttu-id="5938a-193">Lägga till cmdleten Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="5938a-193">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="5938a-194">Lägga till TempDisk-parameter i Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="5938a-194">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="5938a-195">Korrigera varningsmeddelande för New-AzVM</span><span class="sxs-lookup"><span data-stu-id="5938a-195">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="5938a-196">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="5938a-196">Az.ContainerRegistry</span></span>
* <span data-ttu-id="5938a-197">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="5938a-197">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5938a-198">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5938a-198">Az.DataFactory</span></span>
* <span data-ttu-id="5938a-199">ADF .Net SDK-versionen har uppdaterats till 3.0.0</span><span class="sxs-lookup"><span data-stu-id="5938a-199">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5938a-200">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5938a-200">Az.DataLakeStore</span></span>
* <span data-ttu-id="5938a-201">Åtgärda problem med ADLS-slutpunkt vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="5938a-201">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="5938a-202">Mer information här: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="5938a-202">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="5938a-203">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="5938a-203">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="5938a-204">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="5938a-204">Az.IotHub</span></span>
* <span data-ttu-id="5938a-205">Lägga till kodningsformat i cmdleten Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="5938a-205">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="5938a-206">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5938a-206">Az.KeyVault</span></span>
* <span data-ttu-id="5938a-207">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="5938a-207">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5938a-208">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5938a-208">Az.Network</span></span>
* <span data-ttu-id="5938a-209">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="5938a-209">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="5938a-210">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5938a-210">Az.Resources</span></span>
* <span data-ttu-id="5938a-211">Åtgärda felaktiga exempel i referensdokumentationen ”New-AzADAppCredential” och ”New-AzADSpCredential”</span><span class="sxs-lookup"><span data-stu-id="5938a-211">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="5938a-212">Åtgärda problem där sökvägen för parametern ”-TemplateFile” inte omvandlas innan cmdletarna för distribution i resursgruppen körs</span><span class="sxs-lookup"><span data-stu-id="5938a-212">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="5938a-213">Az.Resources: Korrigera dokumentationen om standardvärdet för New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="5938a-213">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="5938a-214">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="5938a-214">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="5938a-215">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="5938a-215">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="5938a-216">Åtgärda formateringsproblemet med objektet ”PSResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="5938a-216">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="5938a-217">Mer information här: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="5938a-217">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="5938a-218">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5938a-218">Az.ServiceFabric</span></span>
* <span data-ttu-id="5938a-219">Återställ när ett certifikat läggs till i en Virtual Machine Scale Sets-modell men ett undantag genereras. Detta har gjorts för att åtgärda följande fel: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="5938a-219">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="5938a-220">Korrigera några felmeddelanden.</span><span class="sxs-lookup"><span data-stu-id="5938a-220">Fix some error messages.</span></span>
* <span data-ttu-id="5938a-221">Korrigering av skapande av kluster med ARM-mall som är standard för New-AzServiceFabriCluster som inte fungerade med migrering till Az.</span><span class="sxs-lookup"><span data-stu-id="5938a-221">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="5938a-222">Korrigering av tilläggning av kluster/programcertifikat så att endast VM Scale Sets som motsvarar klustret läggs till genom att kontrollera ID för klustret i tillägget.</span><span class="sxs-lookup"><span data-stu-id="5938a-222">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="5938a-223">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="5938a-223">Az.SignalR</span></span>
* <span data-ttu-id="5938a-224">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="5938a-224">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="5938a-225">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5938a-225">Az.Sql</span></span>
* <span data-ttu-id="5938a-226">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="5938a-226">Update incorrect online help URLs</span></span>
* <span data-ttu-id="5938a-227">Uppdaterad parameterbeskrivning för LicenseType-parameter med möjliga värden</span><span class="sxs-lookup"><span data-stu-id="5938a-227">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="5938a-228">Korrigering för att uppdatera hanterad instansidentitet som inte fungerar när det är den enda uppdaterade egenskapen</span><span class="sxs-lookup"><span data-stu-id="5938a-228">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="5938a-229">Stöd för anpassad sortering på hanterad instans</span><span class="sxs-lookup"><span data-stu-id="5938a-229">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5938a-230">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5938a-230">Az.Storage</span></span>
* <span data-ttu-id="5938a-231">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="5938a-231">Update incorrect online help URLs</span></span>
* <span data-ttu-id="5938a-232">Tillhandahåll detaljerat felmeddelande när en användare försöker hämta/konfigurera klassisk loggning/mått på ett Premium Storage-konto eftersom Premium Storage-kontot inte har stöd för klassisk loggning/mått.</span><span class="sxs-lookup"><span data-stu-id="5938a-232">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="5938a-233">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="5938a-233">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="5938a-234">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="5938a-234">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="5938a-235">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="5938a-235">Az.TrafficManager</span></span>
* <span data-ttu-id="5938a-236">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="5938a-236">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5938a-237">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5938a-237">Az.Websites</span></span>
* <span data-ttu-id="5938a-238">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="5938a-238">Update incorrect online help URLs</span></span>
* <span data-ttu-id="5938a-239">Korrigerar ”New-AzWebAppSSLBinding” så att certifikatet laddas upp till rätt resursgrupp och plats om appen finns i en ASE.</span><span class="sxs-lookup"><span data-stu-id="5938a-239">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="5938a-240">Korrigerar ”New-AzWebAppSSLBinding” så att taggarna inte skrivs över på en bindning av ett SSL-certifikat till en app</span><span class="sxs-lookup"><span data-stu-id="5938a-240">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="5938a-241">1.1.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="5938a-241">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5938a-242">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5938a-242">Az.Accounts</span></span>
* <span data-ttu-id="5938a-243">Lade till omfattningen ”Lokal” till Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="5938a-243">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5938a-244">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5938a-244">Az.Compute</span></span>
* <span data-ttu-id="5938a-245">Namn är nu valfritt i ID-parametern för Restart/Start/Stop/Remove/Set-AzVM och Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="5938a-245">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="5938a-246">Uppdaterade beskrivningen av ID i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="5938a-246">Updated the description of ID in help files</span></span>
* <span data-ttu-id="5938a-247">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5938a-247">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5938a-248">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5938a-248">Az.DataLakeStore</span></span>
* <span data-ttu-id="5938a-249">Uppdatera sdk-versionen av dataplanet till 1.1.14 för SDK-korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="5938a-249">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="5938a-250">Korrigerade hanteringen av negativ accesstime och modificationtime för getfilestatus och liststatus; korrigera asynkront annulleringstoken</span><span class="sxs-lookup"><span data-stu-id="5938a-250">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="5938a-251">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="5938a-251">Az.EventGrid</span></span>
* <span data-ttu-id="5938a-252">Uppdaterat för användning av API-versionen 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="5938a-252">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="5938a-253">Uppdaterade följande cmdletar för att stödja nytt scenario i API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="5938a-253">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="5938a-254">New-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="5938a-254">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="5938a-255">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="5938a-255">Event Time-To-Live,</span></span>
        - <span data-ttu-id="5938a-256">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="5938a-256">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="5938a-257">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="5938a-257">Dead letter endpoint.</span></span>
    - <span data-ttu-id="5938a-258">Update-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="5938a-258">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="5938a-259">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="5938a-259">Event Time-To-Live,</span></span>
        - <span data-ttu-id="5938a-260">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="5938a-260">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="5938a-261">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="5938a-261">Dead letter endpoint.</span></span>
* <span data-ttu-id="5938a-262">Lade till nya enum-värden (storageQueue och hybridConnection) för alternativet EndpointType i cmdletarna New-AzureRmEventGridSubscription och Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="5938a-262">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="5938a-263">Visa varningsmeddelanden om skapande eller uppdatering av händelseprenumerationen förväntas medföra manuell åtgärd från användaren.</span><span class="sxs-lookup"><span data-stu-id="5938a-263">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="5938a-264">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="5938a-264">Az.IotHub</span></span>
* <span data-ttu-id="5938a-265">Har uppdaterats till den senaste versionen av SDK:n lotHub</span><span class="sxs-lookup"><span data-stu-id="5938a-265">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="5938a-266">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="5938a-266">Az.LogicApp</span></span>
* <span data-ttu-id="5938a-267">Get-AzLogicApp visar en lista över alla som inte har angivet namn</span><span class="sxs-lookup"><span data-stu-id="5938a-267">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="5938a-268">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5938a-268">Az.Resources</span></span>
* <span data-ttu-id="5938a-269">Åtgärdade problem med parameteruppsättningen när parametrarna -ODataQuery och -ResourceId anges för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="5938a-269">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="5938a-270">Mer information här: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="5938a-270">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="5938a-271">Åtgärdade hantering av parametern -Custom i New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="5938a-271">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="5938a-272">Korrigerade stavfel i New-AzDeployment-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="5938a-272">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="5938a-273">Gjorde parametern -MailNickname obligatorisk för New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="5938a-273">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="5938a-274">Mer information här: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="5938a-274">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="5938a-275">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="5938a-275">Az.SignalR</span></span>
* <span data-ttu-id="5938a-276">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5938a-276">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="5938a-277">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5938a-277">Az.Sql</span></span>
* <span data-ttu-id="5938a-278">Konverterade lagringshanteringsklientens beroende av den normala SDK-implementeringen.</span><span class="sxs-lookup"><span data-stu-id="5938a-278">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5938a-279">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5938a-279">Az.Storage</span></span>
* <span data-ttu-id="5938a-280">Angav StorageAccountName för lagringskontext som det verkliga namnet på lagringskontot när det skapas med Sas Token, OAuth eller Anonymous</span><span class="sxs-lookup"><span data-stu-id="5938a-280">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="5938a-281">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="5938a-281">New-AzStorageContext</span></span>
* <span data-ttu-id="5938a-282">Skapade Sas Token för Blob Snapshot-objekt med parametern -FullUri, åtgärdade den returnerade URI:n så att den blir URI för ögonblicksbild</span><span class="sxs-lookup"><span data-stu-id="5938a-282">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="5938a-283">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="5938a-283">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5938a-284">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5938a-284">Az.Websites</span></span>
* <span data-ttu-id="5938a-285">Åtgärdade en bugg i datumparsningen i Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="5938a-285">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="5938a-286">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5938a-286">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="5938a-287">1.0.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="5938a-287">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="5938a-288">Allmänt</span><span class="sxs-lookup"><span data-stu-id="5938a-288">General</span></span>

- <span data-ttu-id="5938a-289">Allmän tillgänglighet för Az-modulen</span><span class="sxs-lookup"><span data-stu-id="5938a-289">General Availability of Az Module</span></span>
- <span data-ttu-id="5938a-290">Onlinehjälp för varje modul</span><span class="sxs-lookup"><span data-stu-id="5938a-290">Online help for each module</span></span>
- <span data-ttu-id="5938a-291">Mer information och en översikt finns på [Az-informationssidan](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="5938a-291">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="5938a-292">Information om hur du migrerar från AzureRM finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="5938a-292">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="5938a-293">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5938a-293">Az.Accounts</span></span>
- <span data-ttu-id="5938a-294">Har ändrats från Az.Profile</span><span class="sxs-lookup"><span data-stu-id="5938a-294">Changed from Az.Profile</span></span>
- <span data-ttu-id="5938a-295">Fasta tabellformat för profil- och kontexttyper</span><span class="sxs-lookup"><span data-stu-id="5938a-295">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="5938a-296">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5938a-296">Az.ApiManagement</span></span>
- <span data-ttu-id="5938a-297">Korrigeringar för #7002</span><span class="sxs-lookup"><span data-stu-id="5938a-297">Fixes for #7002</span></span>
- <span data-ttu-id="5938a-298">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="5938a-298">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="5938a-299">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="5938a-299">Az.Batch</span></span>
- <span data-ttu-id="5938a-300">Lade till möjligheten att se vilken version av Azure Batch Node Agent som körs på var och en av de virtuella datorerna i en pool, via den nya egenskapen `NodeAgentInformation` på `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="5938a-300">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="5938a-301">Standarden `Caching` för `PSDataDisk` är nu `ReadWrite` i stället för `None`.</span><span class="sxs-lookup"><span data-stu-id="5938a-301">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="5938a-302">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="5938a-302">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="5938a-303">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="5938a-303">Az.Billing</span></span>
- <span data-ttu-id="5938a-304">Kombinerar cmdletarna för fakturering, förbrukning och UsageAggregates. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="5938a-304">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="5938a-305">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="5938a-305">Az.CognitivServices</span></span>
- <span data-ttu-id="5938a-306">Lade till kompletterare för SkuName och Typem som är tillgängliga i New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="5938a-306">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="5938a-307">Tog bort parameteruppsättningen GetSkusWithAccountParamSetName från Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="5938a-307">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="5938a-308">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="5938a-308">Az.ContainerInstance</span></span>
- <span data-ttu-id="5938a-309">Stöd för ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="5938a-309">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="5938a-310">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="5938a-310">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="5938a-311">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="5938a-311">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="5938a-312">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5938a-312">Az.DataLakeStore</span></span>
- <span data-ttu-id="5938a-313">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="5938a-313">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="5938a-314">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5938a-314">Az.Monitor</span></span>
- <span data-ttu-id="5938a-315">Döpte om Az.Insights till Az.Monitor och andra mindre icke-bakåtkompatibla ändringar. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="5938a-315">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="5938a-316">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5938a-316">Az.KeyVault</span></span>
- <span data-ttu-id="5938a-317">Tog bort den inaktuella egenskapen PurgeDisabled från utdatatyper</span><span class="sxs-lookup"><span data-stu-id="5938a-317">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="5938a-318">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="5938a-318">Az.MachineLearning</span></span>
- <span data-ttu-id="5938a-319">Inkluderade cmdletarna från modulen Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="5938a-319">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="5938a-320">Az.Media</span><span class="sxs-lookup"><span data-stu-id="5938a-320">Az.Media</span></span>
- <span data-ttu-id="5938a-321">Tog bort inaktuella -Tags-alias från New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="5938a-321">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="5938a-322">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5938a-322">Az.Network</span></span>
<span data-ttu-id="5938a-323">Stöd har lagts till för konfiguration av RewriteRuleSets i Application Gateway</span><span class="sxs-lookup"><span data-stu-id="5938a-323">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="5938a-324">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="5938a-324">New cmdlets added:</span></span>
        - <span data-ttu-id="5938a-325">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5938a-325">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="5938a-326">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5938a-326">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="5938a-327">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5938a-327">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="5938a-328">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5938a-328">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="5938a-329">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5938a-329">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="5938a-330">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="5938a-330">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="5938a-331">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="5938a-331">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="5938a-332">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="5938a-332">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="5938a-333">Cmdletar har uppdaterats med den valfria parametern -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5938a-333">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="5938a-334">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5938a-334">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="5938a-335">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="5938a-335">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="5938a-336">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="5938a-336">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="5938a-337">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5938a-337">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="5938a-338">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5938a-338">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="5938a-339">New-AzureRmApplicationGatewayUrlPathMapConfig har lagt till KeyVault-stöd för Application Gateway med Identity.</span><span class="sxs-lookup"><span data-stu-id="5938a-339">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="5938a-340">Cmdletar har uppdaterats med den valfria parametern -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="5938a-340">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="5938a-341">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5938a-341">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="5938a-342">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5938a-342">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="5938a-343">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5938a-343">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="5938a-344">Cmdleten New-AzApplicationGateway har uppdaterats med den valfria parametern -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="5938a-344">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="5938a-345">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="5938a-345">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="5938a-346">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="5938a-346">Az.OperationalInsights</span></span>
- <span data-ttu-id="5938a-347">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="5938a-347">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="5938a-348">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="5938a-348">Az.Profile</span></span>
- <span data-ttu-id="5938a-349">Modulnamnet har ändrats till Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5938a-349">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="5938a-350">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5938a-350">Az.RecoveryServices</span></span>
- <span data-ttu-id="5938a-351">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="5938a-351">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="5938a-352">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5938a-352">Az.Resources</span></span>
- <span data-ttu-id="5938a-353">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="5938a-353">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="5938a-354">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5938a-354">Az.ServiceFabric</span></span>
- <span data-ttu-id="5938a-355">Stöd för specificering av certifikat efter eget namn och tumavtryck</span><span class="sxs-lookup"><span data-stu-id="5938a-355">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="5938a-356">Information om fler icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="5938a-356">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="5938a-357">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="5938a-357">Az.SIgnalR</span></span>
- <span data-ttu-id="5938a-358">Allmän tillgänglighet för PowerShell-cmdletar för SIgnalR</span><span class="sxs-lookup"><span data-stu-id="5938a-358">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="5938a-359">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5938a-359">Az.Sql</span></span>
- <span data-ttu-id="5938a-360">Lade till de nya identifieringstyperna Data_Exfiltration och Unsafe_Action i Threat Detection-cmdletar</span><span class="sxs-lookup"><span data-stu-id="5938a-360">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="5938a-361">Uppdaterade dokumentationsexempel för Sql Auditing-cmdletar</span><span class="sxs-lookup"><span data-stu-id="5938a-361">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="5938a-362">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="5938a-362">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="5938a-363">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5938a-363">Az.Storage</span></span>
- <span data-ttu-id="5938a-364">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="5938a-364">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="5938a-365">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5938a-365">Az.Websites</span></span>
- <span data-ttu-id="5938a-366">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="5938a-366">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="5938a-367">0.7.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="5938a-367">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="5938a-368">Allmänt</span><span class="sxs-lookup"><span data-stu-id="5938a-368">General</span></span>

* <span data-ttu-id="5938a-369">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="5938a-369">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="5938a-370">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5938a-370">Az.Compute</span></span>

* <span data-ttu-id="5938a-371">Lade till stöd för UltraSSD och Galleriavbildningar i de enkla parameteruppsättningarna för `New-AzVm(ss)`-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="5938a-371">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="5938a-372">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5938a-372">Az.DataLakeStore</span></span>

* <span data-ttu-id="5938a-373">Åtgärdade avslutande snedstreck i domänen för adls-konto</span><span class="sxs-lookup"><span data-stu-id="5938a-373">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="5938a-374">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="5938a-374">Az.FrontDoor</span></span>

* <span data-ttu-id="5938a-375">Brutna länkar korrigerades</span><span class="sxs-lookup"><span data-stu-id="5938a-375">Fixed some broken links</span></span>
    - <span data-ttu-id="5938a-376">I artiklarna New-AzureRmFrontDoor och Set-AzureRmFrontDoor artiklar korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="5938a-376">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="5938a-377">I artikeln New-AzureRmFrontDoorManagedRuleObject korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="5938a-377">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="5938a-378">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5938a-378">Az.RecoveryServices</span></span>

* <span data-ttu-id="5938a-379">Lade till valideringar på klientsidan för Azure-filresurs med återställningsåtgärder.</span><span class="sxs-lookup"><span data-stu-id="5938a-379">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="5938a-380">Gjorde storageAccountName och storageAccountResourceGroupName valfritt för afs-återställning.</span><span class="sxs-lookup"><span data-stu-id="5938a-380">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="5938a-381">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5938a-381">Az.Resources</span></span>

* <span data-ttu-id="5938a-382">Korrigering för https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="5938a-382">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="5938a-383">Uppdaterade Get-AzureRmRoleAssignment så att prenumerationsomfattningen används om den anges vid begäran om klassiska administratörer.</span><span class="sxs-lookup"><span data-stu-id="5938a-383">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="5938a-384">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5938a-384">Az.Sql</span></span>

* <span data-ttu-id="5938a-385">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="5938a-385">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="5938a-386">Korrigerade ett problem med Get-AzureRmSqlDatabaseVulnerabilityAssessment med DotNet-kärna</span><span class="sxs-lookup"><span data-stu-id="5938a-386">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="5938a-387">Ändrade dokumentationen för hjälpmeddelanden som rör SQL Auditing-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="5938a-387">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="5938a-388">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5938a-388">Az.Storage</span></span>

* <span data-ttu-id="5938a-389">Lade till -EnableHierarchicalNamespace i New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5938a-389">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="5938a-390">Åtgärdade problemet med att cmdleten Copy File inte kunde återanvända källkontexten på målet om inte -DestContext angetts</span><span class="sxs-lookup"><span data-stu-id="5938a-390">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="5938a-391">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="5938a-391">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="5938a-392">Stöd för statisk webbplatskonfiguration</span><span class="sxs-lookup"><span data-stu-id="5938a-392">Support Static Website configuration</span></span>
    - <span data-ttu-id="5938a-393">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="5938a-393">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="5938a-394">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="5938a-394">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="5938a-395">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5938a-395">Az.Websites</span></span>

* <span data-ttu-id="5938a-396">Set-AzureRmWebApp och Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="5938a-396">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="5938a-397">Ny parameter (-AzureStoragePath) har lagts till för att ange att Azure Storage-sökvägar ska monteras i containerappar i Windows och Linux.</span><span class="sxs-lookup"><span data-stu-id="5938a-397">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="5938a-398">Använder utdata från den nya cmdleten New-AzureRmWebAppAzureStoragePath som en parameter för att ange sökvägar för Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="5938a-398">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="5938a-399">0.6.1 – november 2018</span><span class="sxs-lookup"><span data-stu-id="5938a-399">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="5938a-400">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5938a-400">Az.ApiManagement</span></span>
* <span data-ttu-id="5938a-401">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="5938a-401">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="5938a-402">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5938a-402">Az.Automation</span></span>
* <span data-ttu-id="5938a-403">Swagger baserade Azure Automation-cmdletar</span><span class="sxs-lookup"><span data-stu-id="5938a-403">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="5938a-404">Cmdletar för Uppdateringshantering har lagts till</span><span class="sxs-lookup"><span data-stu-id="5938a-404">Added Update Management cmdlets</span></span>
* <span data-ttu-id="5938a-405">Cmdletar för källkontroll har lagts till</span><span class="sxs-lookup"><span data-stu-id="5938a-405">Added Source Control cmdlets</span></span>
* <span data-ttu-id="5938a-406">Remove-AzureRmAutomationHybridWorkerGroup-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="5938a-406">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="5938a-407">Kommandot för DSC-registreringsnod har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="5938a-407">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="5938a-408">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5938a-408">Az.Compute</span></span>
* <span data-ttu-id="5938a-409">Problem med SystemAssigned-identitet har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="5938a-409">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="5938a-410">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="5938a-410">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="5938a-411">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="5938a-411">Az.ContainerInstance</span></span>
* <span data-ttu-id="5938a-412">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="5938a-412">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="5938a-413">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="5938a-413">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="5938a-414">uppdatera exempelbeskrivningen för marketplace-cmdletar</span><span class="sxs-lookup"><span data-stu-id="5938a-414">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="5938a-415">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5938a-415">Az.Network</span></span>
* <span data-ttu-id="5938a-416">Cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomErreller Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="5938a-416">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="5938a-417">ICMP tillbaka till stöd för Azure Firewall-nätverksprotokoll har lagts till</span><span class="sxs-lookup"><span data-stu-id="5938a-417">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="5938a-418">Uppdatera cmdlet Test-AzureRmNetworkWatcherConnectivity, lägga till verifiering av mål-id, adress och port.</span><span class="sxs-lookup"><span data-stu-id="5938a-418">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="5938a-419">Åtgärda problem med minnesanvändning i VirtualNetwork-karta</span><span class="sxs-lookup"><span data-stu-id="5938a-419">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="5938a-420">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="5938a-420">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="5938a-421">Åtgärda för att ändra principen för en skyddad fildelning.</span><span class="sxs-lookup"><span data-stu-id="5938a-421">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="5938a-422">Tidszonsprincipen har konverterats till versaler.</span><span class="sxs-lookup"><span data-stu-id="5938a-422">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="5938a-423">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="5938a-423">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="5938a-424">Exempel i New-AzureRmRecoveryServicesAsrProtectableItem har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="5938a-424">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="5938a-425">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="5938a-425">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="5938a-426">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="5938a-426">Az.Relay</span></span>
* <span data-ttu-id="5938a-427">Valfri parameter -KeyValue till New-AzureRmRelayKey cmdlet har lagts till, vilket gör det möjligt för användare att tillhandahålla KeyValue.</span><span class="sxs-lookup"><span data-stu-id="5938a-427">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="5938a-428">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5938a-428">Az.Resources</span></span>
* <span data-ttu-id="5938a-429">Uppdatera hjälpdokumentation för resursidentitet kopplad till parametrar i `New-AzureRmPolicyAssignment` och `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="5938a-429">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="5938a-430">Lägg till ett exempel för New-AzureRmPolicyDefinition som använder -Metadata</span><span class="sxs-lookup"><span data-stu-id="5938a-430">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="5938a-431">Korrigera så att skiftläge behålls i taggnycklar i NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="5938a-431">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="5938a-432">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5938a-432">Az.ServiceFabric</span></span>
* <span data-ttu-id="5938a-433">Lägg till utfasningsmeddelanden för kommande icke-kompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="5938a-433">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="5938a-434">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5938a-434">Az.Sql</span></span>
* <span data-ttu-id="5938a-435">Nya cmdletar för CRUD-åtgärder på Azure Sql Database-hanterad instans och Azure Sql-hanterad databas</span><span class="sxs-lookup"><span data-stu-id="5938a-435">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="5938a-436">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="5938a-436">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="5938a-437">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="5938a-437">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="5938a-438">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="5938a-438">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="5938a-439">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="5938a-439">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="5938a-440">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="5938a-440">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="5938a-441">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="5938a-441">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="5938a-442">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="5938a-442">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="5938a-443">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="5938a-443">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="5938a-444">Hantering av utökad granskningsprincip på en server eller en databas har aktiverats.</span><span class="sxs-lookup"><span data-stu-id="5938a-444">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="5938a-445">Ny parameter (PredicateExpression) har lagts till för att aktivera filtrering av granskningsloggar.</span><span class="sxs-lookup"><span data-stu-id="5938a-445">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="5938a-446">Cmdletar har ändrats så att de använder SQL-klienter i stället för äldre klienter.</span><span class="sxs-lookup"><span data-stu-id="5938a-446">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="5938a-447">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="5938a-447">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="5938a-448">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="5938a-448">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="5938a-449">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="5938a-449">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="5938a-450">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="5938a-450">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="5938a-451">Problem med att använda Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings med lagringskontots namnparameter har korrigerats</span><span class="sxs-lookup"><span data-stu-id="5938a-451">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="5938a-452">0.5.0 – november 2018</span><span class="sxs-lookup"><span data-stu-id="5938a-452">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="5938a-453">Allmänt</span><span class="sxs-lookup"><span data-stu-id="5938a-453">General</span></span>
* <span data-ttu-id="5938a-454">Lade till resurskompletterare till många kärn-cmdletar – dessa gör att du kan stega genom befintliga resursnamn med TABB vid interaktiva anrop till cmdletar</span><span class="sxs-lookup"><span data-stu-id="5938a-454">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="5938a-455">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="5938a-455">Az.Profile</span></span>
* <span data-ttu-id="5938a-456">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="5938a-456">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="5938a-457">Bytte namn på parametern TenantId i cmdleten Connect-AzAccount till Tenant och lade till ett alias för TenantId</span><span class="sxs-lookup"><span data-stu-id="5938a-457">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="5938a-458">Uppdaterade TenantId-beskrivningen för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="5938a-458">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="5938a-459">Åtgärda felmeddelande för misslyckad inloggning när du tillhandahåller klientdomän</span><span class="sxs-lookup"><span data-stu-id="5938a-459">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="5938a-460">Åtgärda problem med att kontextnamn hamnar i konflikt för konton utan prenumerationer i klientorganisationen</span><span class="sxs-lookup"><span data-stu-id="5938a-460">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="5938a-461">Åtgärda problem med DataLake-slutpunkter vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="5938a-461">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="5938a-462">Åtgärdade problem med att Disconnect-AzAccount kastades om den inte anslöts</span><span class="sxs-lookup"><span data-stu-id="5938a-462">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="5938a-463">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="5938a-463">Az.CognitiveServices</span></span>
* <span data-ttu-id="5938a-464">Lade till åtgärden Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="5938a-464">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5938a-465">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5938a-465">Az.Compute</span></span>
* <span data-ttu-id="5938a-466">Lade till cmdletarna Add-AzVmssVMDataDisk och Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="5938a-466">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="5938a-467">Get-AzVMImage visar AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="5938a-467">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="5938a-468">Åtgärdade att värdena för alternativen SetAzVMChefExtension -BootstrapOptions och -JsonAttribute inte angavs i json-format.</span><span class="sxs-lookup"><span data-stu-id="5938a-468">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5938a-469">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5938a-469">Az.DataLakeStore</span></span>
* <span data-ttu-id="5938a-470">Uppdatera DataLake-paketet till 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="5938a-470">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="5938a-471">Lägg till standardsamtidighet för flertrådade åtgärder.</span><span class="sxs-lookup"><span data-stu-id="5938a-471">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="5938a-472">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="5938a-472">Az.Insights</span></span>
* <span data-ttu-id="5938a-473">Åtgärdade problem #7267 (autoskalningsområde)</span><span class="sxs-lookup"><span data-stu-id="5938a-473">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="5938a-474">Problem med att uppräknade parametrar inte ställdes in ordentligt när du skapade en ny autoskalningsregel (de ställdes alltid in med standardvärdet).</span><span class="sxs-lookup"><span data-stu-id="5938a-474">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="5938a-475">Åtgärdade problem #7513 [Insights] Set-AzDiagnosticSetting kräver uttrycklig specifikation av kategorier när inställningar skapas</span><span class="sxs-lookup"><span data-stu-id="5938a-475">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="5938a-476">Nu kräver inte cmdleten uttrycklig anvisning av kategorierna för att aktiveras under skapande, d.v.s. den fungerar enligt beskrivning</span><span class="sxs-lookup"><span data-stu-id="5938a-476">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5938a-477">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5938a-477">Az.Network</span></span>
* <span data-ttu-id="5938a-478">PeeringType ändrades till en obligatorisk parameter för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="5938a-478">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="5938a-479">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="5938a-479">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="5938a-480">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="5938a-480">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="5938a-481">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="5938a-481">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="5938a-482">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="5938a-482">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="5938a-483">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="5938a-483">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="5938a-484">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="5938a-484">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="5938a-485">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="5938a-485">Az.PolicyInsights</span></span>
* <span data-ttu-id="5938a-486">Cmdletar för principreparation har lagts till</span><span class="sxs-lookup"><span data-stu-id="5938a-486">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="5938a-487">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5938a-487">Az.Resources</span></span>
* <span data-ttu-id="5938a-488">Korrigering för https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="5938a-488">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="5938a-489">Tillåt att resurser listas med parametern -ResourceId för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="5938a-489">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="5938a-490">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="5938a-490">Az.ServiceBus</span></span>
* <span data-ttu-id="5938a-491">Skrivskyddad MigrationState-egenskap har lagts till i PSServiceBusMigrationConfigurationAttributes, som hjälper till att hålla koll på migreringstillståndet.</span><span class="sxs-lookup"><span data-stu-id="5938a-491">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="5938a-492">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5938a-492">Az.ServiceFabric</span></span>
* <span data-ttu-id="5938a-493">Åtgärda att lägga till certifikat till Linux-Vmss.</span><span class="sxs-lookup"><span data-stu-id="5938a-493">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="5938a-494">Åtgärdade Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="5938a-494">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="5938a-495">Använd rätt tumavtryck från nya certifikat (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="5938a-495">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="5938a-496">Visa undantag korrekt (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="5938a-496">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="5938a-497">Åtgärdade Update-AzServiceFabricDurability så att klusterkonfigurationen uppdateras innan Vmss-åtgärden CreateOrUpdate påbörjas.</span><span class="sxs-lookup"><span data-stu-id="5938a-497">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="5938a-498">0.4.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="5938a-498">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="5938a-499">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="5938a-499">Az.Profile</span></span>
* <span data-ttu-id="5938a-500">Åtgärdade problemet med Get-AzSubscription i CloudShell</span><span class="sxs-lookup"><span data-stu-id="5938a-500">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="5938a-501">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="5938a-501">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5938a-502">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5938a-502">Az.Compute</span></span>
* <span data-ttu-id="5938a-503">Nya storlekar lades till i listan över godkända VM-storlekar för vilka accelererat nätverk kommer att aktiveras vid användning av den enkla parameteruppsättningen för New-AzVm</span><span class="sxs-lookup"><span data-stu-id="5938a-503">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="5938a-504">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="5938a-504">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5938a-505">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5938a-505">Az.DataLakeStore</span></span>
* <span data-ttu-id="5938a-506">Lägger till stöd för virtuella nätverksregler</span><span class="sxs-lookup"><span data-stu-id="5938a-506">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="5938a-507">Get-AzDataLakeStoreVirtualNetworkRule: Hämtar eller listar regel för virtuellt Azure Data Lake Store-nätverk.</span><span class="sxs-lookup"><span data-stu-id="5938a-507">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="5938a-508">Add-AzDataLakeStoreVirtualNetworkRule: Lägger till en regel för det virtuella nätverket till det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="5938a-508">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="5938a-509">Set-AzDataLakeStoreVirtualNetworkRule: Ändrar den angivna regeln för det virtuella nätverket i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="5938a-509">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="5938a-510">Remove-AzDataLakeStoreVirtualNetworkRule: Tar bort en regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="5938a-510">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5938a-511">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5938a-511">Az.Network</span></span>
* <span data-ttu-id="5938a-512">Skicka protokollvärdet till serverdelen för att uppdatera cmdleten Test-AzNetworkWatcherConnectivity.</span><span class="sxs-lookup"><span data-stu-id="5938a-512">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="5938a-513">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="5938a-513">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="5938a-514">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5938a-514">Az.Resources</span></span>
* <span data-ttu-id="5938a-515">Åtgärdade problem där Get-AzRoleDefinition genererar ett oläsligt undantag (när standardprofilen inte innehåller någon prenumeration och ingen omfattning har angetts) genom att lägga till ett beskrivande undantag i scenariot.</span><span class="sxs-lookup"><span data-stu-id="5938a-515">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="5938a-516">Ställ in ”RoleDefinitionNameParameterSet” som standardparameteruppsättning.</span><span class="sxs-lookup"><span data-stu-id="5938a-516">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="5938a-517">0.3.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="5938a-517">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="5938a-518">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="5938a-518">Azure.Storage</span></span>
* <span data-ttu-id="5938a-519">Åtgärda fel där Kopiera blob/fil inte kopierar metadata när målplatsen har ett problem med metadata</span><span class="sxs-lookup"><span data-stu-id="5938a-519">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="5938a-520">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="5938a-520">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="5938a-521">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="5938a-521">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="5938a-522">Stöd för att hämta användningsinformation om en Storage-resurs för en specifik plats och för att lägga till ett varningsmeddelande för att hämta användningsinformation om en global Storage-resurs är inaktuellt.</span><span class="sxs-lookup"><span data-stu-id="5938a-522">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="5938a-523">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="5938a-523">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="5938a-524">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="5938a-524">Az.CognitiveServices</span></span>
* <span data-ttu-id="5938a-525">Stöd för Get-AzCognitiveServicesAccountSkus utan ett befintligt konto.</span><span class="sxs-lookup"><span data-stu-id="5938a-525">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5938a-526">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5938a-526">Az.Compute</span></span>
* <span data-ttu-id="5938a-527">Åtgärdade fel där Get-AzVM -ResourceGroupName <rg> returnerar fler än 50 resultat om det behövs</span><span class="sxs-lookup"><span data-stu-id="5938a-527">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="5938a-528">Lade till ett exempel för SimpleParameterSet i hjälpen för cmdleten New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="5938a-528">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="5938a-529">Ett stavfel i förloppsmeddelandet för Azure Disk Encryption har korrigerats</span><span class="sxs-lookup"><span data-stu-id="5938a-529">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="5938a-530">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="5938a-530">Az.DataFactoryV2</span></span>
* <span data-ttu-id="5938a-531">ADF .Net SDK-versionen har uppdaterats till 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="5938a-531">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5938a-532">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5938a-532">Az.Network</span></span>
* <span data-ttu-id="5938a-533">Funktionalitet för NetworkProfile har lagts till.</span><span class="sxs-lookup"><span data-stu-id="5938a-533">Added NetworkProfile functionality.</span></span> <span data-ttu-id="5938a-534">nya cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="5938a-534">new cmdlets added</span></span>
    - <span data-ttu-id="5938a-535">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="5938a-535">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="5938a-536">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="5938a-536">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="5938a-537">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="5938a-537">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="5938a-538">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="5938a-538">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="5938a-539">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="5938a-539">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="5938a-540">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="5938a-540">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="5938a-541">Länk för tjänstassociering på modell för undernät har lagts till</span><span class="sxs-lookup"><span data-stu-id="5938a-541">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="5938a-542">Cmdletarna New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap och Remove-AzVirtualNetworkTap har lagts till</span><span class="sxs-lookup"><span data-stu-id="5938a-542">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="5938a-543">Cmdletarna Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig och Remove-AzNEtworkInterfaceTapConfig har lagts till</span><span class="sxs-lookup"><span data-stu-id="5938a-543">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="5938a-544">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="5938a-544">Az.RedisCache</span></span>
* <span data-ttu-id="5938a-545">Tillåt att alla strängar används som storleksparametrar framöver.</span><span class="sxs-lookup"><span data-stu-id="5938a-545">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="5938a-546">Lägg till P5 i popup-fönstret PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="5938a-546">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="5938a-547">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5938a-547">Az.Resources</span></span>
* <span data-ttu-id="5938a-548">Parametern -Mode som saknades i Set-AzPolicyDefinition har lagts till</span><span class="sxs-lookup"><span data-stu-id="5938a-548">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="5938a-549">Åtgärdade buggen för cmdleten Get-AzProviderOperation för åtgärder med ursprung som innehåller användare</span><span class="sxs-lookup"><span data-stu-id="5938a-549">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="5938a-550">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5938a-550">Az.Sql</span></span>
* <span data-ttu-id="5938a-551">Ett problem där vissa cmdletar för säkerhetskopiering inte kunde identifiera den aktuella azure-prenumerationen har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="5938a-551">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5938a-552">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5938a-552">Az.Websites</span></span>
* <span data-ttu-id="5938a-553">Ny cmdlet: Get-AzWebAppContainerContinuousDeploymentUrl – Hämtar webhook-URL:en för kontinuerlig distribution av container</span><span class="sxs-lookup"><span data-stu-id="5938a-553">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="5938a-554">Nya cmdletar: New-AzWebAppContainerPSSession och Enter-WebAppContainerPSSession – Startar en PowerShell-fjärrsession i en containerapp för windows</span><span class="sxs-lookup"><span data-stu-id="5938a-554">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="5938a-555">0.2.0 – september 2018</span><span class="sxs-lookup"><span data-stu-id="5938a-555">0.2.0 - September 2018</span></span>
 <span data-ttu-id="5938a-556">Första versionen</span><span class="sxs-lookup"><span data-stu-id="5938a-556">Initial Release</span></span>