---
ms.openlocfilehash: 9915ff37e59a73c1d226a216213fd9016b55d3d4
ms.sourcegitcommit: 447276d46ffeeb37f0c07a570536665e36c5ddb8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/14/2019
ms.locfileid: "57882649"
---
## <a name="150---march-2019"></a><span data-ttu-id="4b82b-101">1.5.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="4b82b-101">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4b82b-102">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4b82b-102">Az.Accounts</span></span>
* <span data-ttu-id="4b82b-103">Lägg till kommandot Register-AzModule för stöd för AutoRest-genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="4b82b-103">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="4b82b-104">Uppdatera exempel för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="4b82b-104">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4b82b-105">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4b82b-105">Az.Automation</span></span>
* <span data-ttu-id="4b82b-106">Problem med att hämta vissa månadsscheman i flera Azure Automation-cmdletar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="4b82b-106">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="4b82b-107">Åtgärda problem med att Get-AzAutomationDscNode bara returnerar de 20 översta noderna.</span><span class="sxs-lookup"><span data-stu-id="4b82b-107">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="4b82b-108">Nu returneras alla noder</span><span class="sxs-lookup"><span data-stu-id="4b82b-108">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="4b82b-109">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="4b82b-109">Az.Cdn</span></span>
* <span data-ttu-id="4b82b-110">Nya Powershell-cmdletar för att aktivera/inaktivera anpassade domän-HTTPS har lagts till och de gamla har gjorts inaktuella</span><span class="sxs-lookup"><span data-stu-id="4b82b-110">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4b82b-111">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4b82b-111">Az.Compute</span></span>
* <span data-ttu-id="4b82b-112">Lägg till stöd för jokertecken för Get-cmdletar</span><span class="sxs-lookup"><span data-stu-id="4b82b-112">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4b82b-113">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4b82b-113">Az.DataFactory</span></span>
* <span data-ttu-id="4b82b-114">ADF .Net SDK-versionen har uppdaterats till 3.0.1</span><span class="sxs-lookup"><span data-stu-id="4b82b-114">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="4b82b-115">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="4b82b-115">Az.LogicApp</span></span>
* <span data-ttu-id="4b82b-116">Åtgärda problemet med att ListWorkflows endast hämtar den första sidan med resultat</span><span class="sxs-lookup"><span data-stu-id="4b82b-116">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4b82b-117">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4b82b-117">Az.Network</span></span>
* <span data-ttu-id="4b82b-118">Lägg till stöd för jokertecken för Network-cmdletar</span><span class="sxs-lookup"><span data-stu-id="4b82b-118">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4b82b-119">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4b82b-119">Az.RecoveryServices</span></span>
* <span data-ttu-id="4b82b-120">Stöd har lagts till för SQL Server i virtuella Azure-datorer</span><span class="sxs-lookup"><span data-stu-id="4b82b-120">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="4b82b-121">SDK-uppdatering</span><span class="sxs-lookup"><span data-stu-id="4b82b-121">SDK Update</span></span>
* <span data-ttu-id="4b82b-122">Get-ProtectableItem-incheckning i VMappContainer har tagits bort</span><span class="sxs-lookup"><span data-stu-id="4b82b-122">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="4b82b-123">Name och ServerName har lagts till som parametrar för Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="4b82b-123">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="4b82b-124">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4b82b-124">Az.Resources</span></span>
* <span data-ttu-id="4b82b-125">Lägg till parametern `-TemplateObject` i cmdletar för distribution</span><span class="sxs-lookup"><span data-stu-id="4b82b-125">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="4b82b-126">Mer information här: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="4b82b-126">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="4b82b-127">Åtgärda problem med piping av resultatet i `Get-AzResource` till `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="4b82b-127">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="4b82b-128">Mer information här: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="4b82b-128">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="4b82b-129">Åtgärda problem med ändring av JSON-datatyp när `Set-AzResource` körs</span><span class="sxs-lookup"><span data-stu-id="4b82b-129">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="4b82b-130">Mer information här: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="4b82b-130">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="4b82b-131">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4b82b-131">Az.Sql</span></span>
* <span data-ttu-id="4b82b-132">AuditingEndpointsCommunicator uppdateras.</span><span class="sxs-lookup"><span data-stu-id="4b82b-132">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="4b82b-133">Åtgärdar beteendet hos ett gränsscenario när nya diagnostikinställningar skapas.</span><span class="sxs-lookup"><span data-stu-id="4b82b-133">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4b82b-134">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4b82b-134">Az.Storage</span></span>
* <span data-ttu-id="4b82b-135">Stöd för BlockBlobStorage när Storage-konto skapas      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4b82b-135">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="4b82b-136">1.4.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="4b82b-136">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="4b82b-137">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="4b82b-137">Az.AnalysisServices</span></span>
* <span data-ttu-id="4b82b-138">Inaktuell AddAzureASAccount-cmdlet</span><span class="sxs-lookup"><span data-stu-id="4b82b-138">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4b82b-139">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4b82b-139">Az.Automation</span></span>
* <span data-ttu-id="4b82b-140">Hjälpen för Import-AzAutomationDscNodeConfiguration har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="4b82b-140">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="4b82b-141">Konfigurationsnamnsvalidering har lagts till i cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="4b82b-141">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="4b82b-142">Förbättrad felhantering för cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="4b82b-142">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="4b82b-143">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="4b82b-143">Az.CognitiveServices</span></span>
* <span data-ttu-id="4b82b-144">CustomSubdomainName har lagts till som en ny valfri parameter för New-AzCognitiveServicesAccount, som används för att ange underdomän för resursen.</span><span class="sxs-lookup"><span data-stu-id="4b82b-144">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4b82b-145">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4b82b-145">Az.Compute</span></span>
* <span data-ttu-id="4b82b-146">Problemet med ID-parameteruppsättningar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="4b82b-146">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="4b82b-147">Get-AzVMExtension har uppdaterats så att alla installerade tillägg visas om parametern Name inte har angetts</span><span class="sxs-lookup"><span data-stu-id="4b82b-147">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="4b82b-148">Parametrarna Tag och ResourceId har lagts till i cmdleten Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="4b82b-148">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="4b82b-149">Get-AzVmssVM utan instans-ID och med InstanceView kan visa virtuella VMSS-datorer med instansvyn.</span><span class="sxs-lookup"><span data-stu-id="4b82b-149">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4b82b-150">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4b82b-150">Az.DataLakeStore</span></span>
* <span data-ttu-id="4b82b-151">Cmdletar har lagts till för uppräkning och återställning av borttagna objekt i ADL</span><span class="sxs-lookup"><span data-stu-id="4b82b-151">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="4b82b-152">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="4b82b-152">Az.EventHub</span></span>
* <span data-ttu-id="4b82b-153">Ny boolesk egenskap SkipEmptyArchives har lagts till i Skip Empty Archives i CaptureDescription-klassen i Eventhub</span><span class="sxs-lookup"><span data-stu-id="4b82b-153">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="4b82b-154">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4b82b-154">Az.KeyVault</span></span>
* <span data-ttu-id="4b82b-155">Taggning i Set-AzKeyVaultSecret har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="4b82b-155">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="4b82b-156">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="4b82b-156">Az.LogicApp</span></span>
* <span data-ttu-id="4b82b-157">Grundläggande SKU har lagts till för Integrationskonton</span><span class="sxs-lookup"><span data-stu-id="4b82b-157">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="4b82b-158">XSLT 2.0, XSLT 3.0 och Flytande mappningstyper har lagts till</span><span class="sxs-lookup"><span data-stu-id="4b82b-158">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="4b82b-159">Nya cmdletar för integrationskontosammansättningar</span><span class="sxs-lookup"><span data-stu-id="4b82b-159">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="4b82b-160">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="4b82b-160">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="4b82b-161">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="4b82b-161">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="4b82b-162">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="4b82b-162">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="4b82b-163">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="4b82b-163">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="4b82b-164">Nya cmdletar för batchkonfiguration för integrationskonto</span><span class="sxs-lookup"><span data-stu-id="4b82b-164">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="4b82b-165">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="4b82b-165">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="4b82b-166">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="4b82b-166">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="4b82b-167">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="4b82b-167">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="4b82b-168">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="4b82b-168">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="4b82b-169">Logic App-SDK har uppdaterats till version 4.1.0</span><span class="sxs-lookup"><span data-stu-id="4b82b-169">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4b82b-170">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4b82b-170">Az.Monitor</span></span>
* <span data-ttu-id="4b82b-171">Hjälpen för Get-AzMetric har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="4b82b-171">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4b82b-172">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4b82b-172">Az.Network</span></span>
* <span data-ttu-id="4b82b-173">Hjälpexempel för Add-AzApplicationGatewayCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="4b82b-173">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="4b82b-174">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="4b82b-174">Az.OperationalInsights</span></span>
* <span data-ttu-id="4b82b-175">Ytterligare stöd för datakällorna New och Get ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="4b82b-175">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="4b82b-176">Ny ApplicationInsights-typ har lagts till för att ge stöd för ”Get specific” och ”Get all” för ApplicationInsights-datakällor för angiven arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="4b82b-176">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="4b82b-177">Cmdleten New-AzOperationalInsightsApplicationInsightsDataSource har lagts till för att skapa datakälla med angivna parametrar för Application Insights-resurs: subscription Id, resourceGroupName och name.</span><span class="sxs-lookup"><span data-stu-id="4b82b-177">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="4b82b-178">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4b82b-178">Az.Resources</span></span>
* <span data-ttu-id="4b82b-179">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="4b82b-179">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="4b82b-180">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="4b82b-180">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="4b82b-181">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="4b82b-181">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="4b82b-182">Fel som gör att KeyCredentials inte kan skapas upprepade gånger har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="4b82b-182">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="4b82b-183">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4b82b-183">Az.Sql</span></span>
* <span data-ttu-id="4b82b-184">Stöd för nivån SQL DB-hyperskal har lagts till</span><span class="sxs-lookup"><span data-stu-id="4b82b-184">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="4b82b-185">Ett fel har åtgärdats där återställningen kunde misslyckas på grund av onödiga inställningsegenskaper i restore-förfrågan</span><span class="sxs-lookup"><span data-stu-id="4b82b-185">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4b82b-186">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4b82b-186">Az.Websites</span></span>
* <span data-ttu-id="4b82b-187">Rätt exempel i Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="4b82b-187">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="4b82b-188">1.3.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="4b82b-188">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4b82b-189">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4b82b-189">Az.Accounts</span></span>
* <span data-ttu-id="4b82b-190">Uppdatera till den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="4b82b-190">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="4b82b-191">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="4b82b-191">Az.AnalysisServices</span></span>
<span data-ttu-id="4b82b-192">Allmän tillgänglighet för Az.AnalysisServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="4b82b-192">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4b82b-193">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4b82b-193">Az.Compute</span></span>
* <span data-ttu-id="4b82b-194">AEM-tillägg: Lägg till stöd för UltraSSD-, P60-, P70- och P80-diskar</span><span class="sxs-lookup"><span data-stu-id="4b82b-194">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="4b82b-195">Uppdatera hjälpbeskrivning för Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="4b82b-195">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="4b82b-196">Uppdatera hjälpbeskrivning och exempel för Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="4b82b-196">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4b82b-197">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4b82b-197">Az.RecoveryServices</span></span>
<span data-ttu-id="4b82b-198">Allmän tillgänglighet för Az.RecoveryServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="4b82b-198">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4b82b-199">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4b82b-199">Az.Resources</span></span>
* <span data-ttu-id="4b82b-200">Korrigera taggar för resursgrupper</span><span class="sxs-lookup"><span data-stu-id="4b82b-200">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="4b82b-201">Mer information här: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="4b82b-201">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="4b82b-202">Åtgärda problem där `Get-AzureRmRoleAssignment` inte respekterar -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="4b82b-202">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="4b82b-203">Mer information här: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="4b82b-203">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="4b82b-204">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4b82b-204">Az.Sql</span></span>
* <span data-ttu-id="4b82b-205">Lägga till Get/Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="4b82b-205">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="4b82b-206">Åtgärda problem där ett nullref-undantag uppstår när du kör SQL-cmdletar och inte är inloggad på ett Azure-konto</span><span class="sxs-lookup"><span data-stu-id="4b82b-206">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="4b82b-207">Åtgärda nullref-undantag i Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="4b82b-207">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="4b82b-208">1.2.1 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="4b82b-208">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4b82b-209">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4b82b-209">Az.Accounts</span></span>
* <span data-ttu-id="4b82b-210">Version med rätt version av autentisering</span><span class="sxs-lookup"><span data-stu-id="4b82b-210">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="4b82b-211">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="4b82b-211">Az.AnalysisServices</span></span>
* <span data-ttu-id="4b82b-212">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="4b82b-212">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4b82b-213">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4b82b-213">Az.RecoveryServices</span></span>
* <span data-ttu-id="4b82b-214">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="4b82b-214">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="4b82b-215">1.2.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="4b82b-215">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4b82b-216">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4b82b-216">Az.Accounts</span></span>
* <span data-ttu-id="4b82b-217">Lägga till interaktiv autentisering och autentisering med användarnamn/lösenord för endast Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="4b82b-217">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="4b82b-218">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="4b82b-218">Update incorrect online help URLs</span></span>
* <span data-ttu-id="4b82b-219">Lägga till varningsmeddelande i PS Core för Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="4b82b-219">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="4b82b-220">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="4b82b-220">Az.Aks</span></span>
* <span data-ttu-id="4b82b-221">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="4b82b-221">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4b82b-222">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4b82b-222">Az.Automation</span></span>
* <span data-ttu-id="4b82b-223">Stöd för Python 2-runbookflöden har lagts till</span><span class="sxs-lookup"><span data-stu-id="4b82b-223">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="4b82b-224">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="4b82b-224">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="4b82b-225">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="4b82b-225">Az.Cdn</span></span>
* <span data-ttu-id="4b82b-226">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="4b82b-226">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4b82b-227">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4b82b-227">Az.Compute</span></span>
* <span data-ttu-id="4b82b-228">Lägga till cmdleten Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="4b82b-228">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="4b82b-229">Lägga till TempDisk-parameter i Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4b82b-229">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="4b82b-230">Korrigera varningsmeddelande för New-AzVM</span><span class="sxs-lookup"><span data-stu-id="4b82b-230">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="4b82b-231">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="4b82b-231">Az.ContainerRegistry</span></span>
* <span data-ttu-id="4b82b-232">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="4b82b-232">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4b82b-233">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4b82b-233">Az.DataFactory</span></span>
* <span data-ttu-id="4b82b-234">ADF .Net SDK-versionen har uppdaterats till 3.0.0</span><span class="sxs-lookup"><span data-stu-id="4b82b-234">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4b82b-235">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4b82b-235">Az.DataLakeStore</span></span>
* <span data-ttu-id="4b82b-236">Åtgärda problem med ADLS-slutpunkt vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="4b82b-236">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="4b82b-237">Mer information här: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="4b82b-237">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="4b82b-238">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="4b82b-238">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4b82b-239">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4b82b-239">Az.IotHub</span></span>
* <span data-ttu-id="4b82b-240">Lägga till kodningsformat i cmdleten Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="4b82b-240">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4b82b-241">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4b82b-241">Az.KeyVault</span></span>
* <span data-ttu-id="4b82b-242">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="4b82b-242">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4b82b-243">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4b82b-243">Az.Network</span></span>
* <span data-ttu-id="4b82b-244">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="4b82b-244">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="4b82b-245">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4b82b-245">Az.Resources</span></span>
* <span data-ttu-id="4b82b-246">Åtgärda felaktiga exempel i referensdokumentationen ”New-AzADAppCredential” och ”New-AzADSpCredential”</span><span class="sxs-lookup"><span data-stu-id="4b82b-246">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="4b82b-247">Åtgärda problem där sökvägen för parametern ”-TemplateFile” inte omvandlas innan cmdletarna för distribution i resursgruppen körs</span><span class="sxs-lookup"><span data-stu-id="4b82b-247">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="4b82b-248">Az.Resources: Korrigera dokumentationen om standardvärdet för New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="4b82b-248">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="4b82b-249">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="4b82b-249">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="4b82b-250">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="4b82b-250">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="4b82b-251">Åtgärda formateringsproblemet med objektet ”PSResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="4b82b-251">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="4b82b-252">Mer information här: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="4b82b-252">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="4b82b-253">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4b82b-253">Az.ServiceFabric</span></span>
* <span data-ttu-id="4b82b-254">Återställ när ett certifikat läggs till i en Virtual Machine Scale Sets-modell men ett undantag genereras. Detta har gjorts för att åtgärda följande fel: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="4b82b-254">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="4b82b-255">Korrigera några felmeddelanden.</span><span class="sxs-lookup"><span data-stu-id="4b82b-255">Fix some error messages.</span></span>
* <span data-ttu-id="4b82b-256">Korrigering av skapande av kluster med ARM-mall som är standard för New-AzServiceFabriCluster som inte fungerade med migrering till Az.</span><span class="sxs-lookup"><span data-stu-id="4b82b-256">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="4b82b-257">Korrigering av tilläggning av kluster/programcertifikat så att endast VM Scale Sets som motsvarar klustret läggs till genom att kontrollera ID för klustret i tillägget.</span><span class="sxs-lookup"><span data-stu-id="4b82b-257">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="4b82b-258">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="4b82b-258">Az.SignalR</span></span>
* <span data-ttu-id="4b82b-259">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="4b82b-259">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="4b82b-260">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4b82b-260">Az.Sql</span></span>
* <span data-ttu-id="4b82b-261">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="4b82b-261">Update incorrect online help URLs</span></span>
* <span data-ttu-id="4b82b-262">Uppdaterad parameterbeskrivning för LicenseType-parameter med möjliga värden</span><span class="sxs-lookup"><span data-stu-id="4b82b-262">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="4b82b-263">Korrigering för att uppdatera hanterad instansidentitet som inte fungerar när det är den enda uppdaterade egenskapen</span><span class="sxs-lookup"><span data-stu-id="4b82b-263">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="4b82b-264">Stöd för anpassad sortering på hanterad instans</span><span class="sxs-lookup"><span data-stu-id="4b82b-264">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4b82b-265">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4b82b-265">Az.Storage</span></span>
* <span data-ttu-id="4b82b-266">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="4b82b-266">Update incorrect online help URLs</span></span>
* <span data-ttu-id="4b82b-267">Tillhandahåll detaljerat felmeddelande när en användare försöker hämta/konfigurera klassisk loggning/mått på ett Premium Storage-konto eftersom Premium Storage-kontot inte har stöd för klassisk loggning/mått.</span><span class="sxs-lookup"><span data-stu-id="4b82b-267">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="4b82b-268">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="4b82b-268">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="4b82b-269">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="4b82b-269">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="4b82b-270">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="4b82b-270">Az.TrafficManager</span></span>
* <span data-ttu-id="4b82b-271">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="4b82b-271">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4b82b-272">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4b82b-272">Az.Websites</span></span>
* <span data-ttu-id="4b82b-273">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="4b82b-273">Update incorrect online help URLs</span></span>
* <span data-ttu-id="4b82b-274">Korrigerar ”New-AzWebAppSSLBinding” så att certifikatet laddas upp till rätt resursgrupp och plats om appen finns i en ASE.</span><span class="sxs-lookup"><span data-stu-id="4b82b-274">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="4b82b-275">Korrigerar ”New-AzWebAppSSLBinding” så att taggarna inte skrivs över på en bindning av ett SSL-certifikat till en app</span><span class="sxs-lookup"><span data-stu-id="4b82b-275">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="4b82b-276">1.1.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="4b82b-276">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4b82b-277">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4b82b-277">Az.Accounts</span></span>
* <span data-ttu-id="4b82b-278">Lade till omfattningen ”Lokal” till Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="4b82b-278">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4b82b-279">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4b82b-279">Az.Compute</span></span>
* <span data-ttu-id="4b82b-280">Namn är nu valfritt i ID-parametern för Restart/Start/Stop/Remove/Set-AzVM och Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="4b82b-280">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="4b82b-281">Uppdaterade beskrivningen av ID i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="4b82b-281">Updated the description of ID in help files</span></span>
* <span data-ttu-id="4b82b-282">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4b82b-282">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4b82b-283">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4b82b-283">Az.DataLakeStore</span></span>
* <span data-ttu-id="4b82b-284">Uppdatera sdk-versionen av dataplanet till 1.1.14 för SDK-korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="4b82b-284">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="4b82b-285">Korrigerade hanteringen av negativ accesstime och modificationtime för getfilestatus och liststatus; korrigera asynkront annulleringstoken</span><span class="sxs-lookup"><span data-stu-id="4b82b-285">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="4b82b-286">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="4b82b-286">Az.EventGrid</span></span>
* <span data-ttu-id="4b82b-287">Uppdaterat för användning av API-versionen 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="4b82b-287">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="4b82b-288">Uppdaterade följande cmdletar för att stödja nytt scenario i API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="4b82b-288">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="4b82b-289">New-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="4b82b-289">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="4b82b-290">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="4b82b-290">Event Time-To-Live,</span></span>
        - <span data-ttu-id="4b82b-291">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="4b82b-291">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="4b82b-292">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="4b82b-292">Dead letter endpoint.</span></span>
    - <span data-ttu-id="4b82b-293">Update-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="4b82b-293">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="4b82b-294">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="4b82b-294">Event Time-To-Live,</span></span>
        - <span data-ttu-id="4b82b-295">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="4b82b-295">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="4b82b-296">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="4b82b-296">Dead letter endpoint.</span></span>
* <span data-ttu-id="4b82b-297">Lade till nya enum-värden (storageQueue och hybridConnection) för alternativet EndpointType i cmdletarna New-AzureRmEventGridSubscription och Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="4b82b-297">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="4b82b-298">Visa varningsmeddelanden om skapande eller uppdatering av händelseprenumerationen förväntas medföra manuell åtgärd från användaren.</span><span class="sxs-lookup"><span data-stu-id="4b82b-298">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4b82b-299">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4b82b-299">Az.IotHub</span></span>
* <span data-ttu-id="4b82b-300">Har uppdaterats till den senaste versionen av SDK:n lotHub</span><span class="sxs-lookup"><span data-stu-id="4b82b-300">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="4b82b-301">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="4b82b-301">Az.LogicApp</span></span>
* <span data-ttu-id="4b82b-302">Get-AzLogicApp visar en lista över alla som inte har angivet namn</span><span class="sxs-lookup"><span data-stu-id="4b82b-302">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="4b82b-303">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4b82b-303">Az.Resources</span></span>
* <span data-ttu-id="4b82b-304">Åtgärdade problem med parameteruppsättningen när parametrarna -ODataQuery och -ResourceId anges för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="4b82b-304">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="4b82b-305">Mer information här: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="4b82b-305">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="4b82b-306">Åtgärdade hantering av parametern -Custom i New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4b82b-306">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="4b82b-307">Korrigerade stavfel i New-AzDeployment-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="4b82b-307">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="4b82b-308">Gjorde parametern -MailNickname obligatorisk för New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="4b82b-308">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="4b82b-309">Mer information här: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="4b82b-309">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="4b82b-310">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="4b82b-310">Az.SignalR</span></span>
* <span data-ttu-id="4b82b-311">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4b82b-311">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="4b82b-312">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4b82b-312">Az.Sql</span></span>
* <span data-ttu-id="4b82b-313">Konverterade lagringshanteringsklientens beroende av den normala SDK-implementeringen.</span><span class="sxs-lookup"><span data-stu-id="4b82b-313">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4b82b-314">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4b82b-314">Az.Storage</span></span>
* <span data-ttu-id="4b82b-315">Angav StorageAccountName för lagringskontext som det verkliga namnet på lagringskontot när det skapas med Sas Token, OAuth eller Anonymous</span><span class="sxs-lookup"><span data-stu-id="4b82b-315">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="4b82b-316">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="4b82b-316">New-AzStorageContext</span></span>
* <span data-ttu-id="4b82b-317">Skapade Sas Token för Blob Snapshot-objekt med parametern -FullUri, åtgärdade den returnerade URI:n så att den blir URI för ögonblicksbild</span><span class="sxs-lookup"><span data-stu-id="4b82b-317">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="4b82b-318">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="4b82b-318">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4b82b-319">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4b82b-319">Az.Websites</span></span>
* <span data-ttu-id="4b82b-320">Åtgärdade en bugg i datumparsningen i Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="4b82b-320">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="4b82b-321">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4b82b-321">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="4b82b-322">1.0.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="4b82b-322">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="4b82b-323">Allmänt</span><span class="sxs-lookup"><span data-stu-id="4b82b-323">General</span></span>

- <span data-ttu-id="4b82b-324">Allmän tillgänglighet för Az-modulen</span><span class="sxs-lookup"><span data-stu-id="4b82b-324">General Availability of Az Module</span></span>
- <span data-ttu-id="4b82b-325">Onlinehjälp för varje modul</span><span class="sxs-lookup"><span data-stu-id="4b82b-325">Online help for each module</span></span>
- <span data-ttu-id="4b82b-326">Mer information och en översikt finns på [Az-informationssidan](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="4b82b-326">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="4b82b-327">Information om hur du migrerar från AzureRM finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="4b82b-327">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="4b82b-328">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4b82b-328">Az.Accounts</span></span>
- <span data-ttu-id="4b82b-329">Har ändrats från Az.Profile</span><span class="sxs-lookup"><span data-stu-id="4b82b-329">Changed from Az.Profile</span></span>
- <span data-ttu-id="4b82b-330">Fasta tabellformat för profil- och kontexttyper</span><span class="sxs-lookup"><span data-stu-id="4b82b-330">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="4b82b-331">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4b82b-331">Az.ApiManagement</span></span>
- <span data-ttu-id="4b82b-332">Korrigeringar för #7002</span><span class="sxs-lookup"><span data-stu-id="4b82b-332">Fixes for #7002</span></span>
- <span data-ttu-id="4b82b-333">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="4b82b-333">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="4b82b-334">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="4b82b-334">Az.Batch</span></span>
- <span data-ttu-id="4b82b-335">Lade till möjligheten att se vilken version av Azure Batch Node Agent som körs på var och en av de virtuella datorerna i en pool, via den nya egenskapen `NodeAgentInformation` på `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="4b82b-335">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="4b82b-336">Standarden `Caching` för `PSDataDisk` är nu `ReadWrite` i stället för `None`.</span><span class="sxs-lookup"><span data-stu-id="4b82b-336">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="4b82b-337">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="4b82b-337">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="4b82b-338">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="4b82b-338">Az.Billing</span></span>
- <span data-ttu-id="4b82b-339">Kombinerar cmdletarna för fakturering, förbrukning och UsageAggregates. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="4b82b-339">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="4b82b-340">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="4b82b-340">Az.CognitivServices</span></span>
- <span data-ttu-id="4b82b-341">Lade till kompletterare för SkuName och Typem som är tillgängliga i New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="4b82b-341">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="4b82b-342">Tog bort parameteruppsättningen GetSkusWithAccountParamSetName från Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="4b82b-342">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="4b82b-343">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="4b82b-343">Az.ContainerInstance</span></span>
- <span data-ttu-id="4b82b-344">Stöd för ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="4b82b-344">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="4b82b-345">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="4b82b-345">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="4b82b-346">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="4b82b-346">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="4b82b-347">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4b82b-347">Az.DataLakeStore</span></span>
- <span data-ttu-id="4b82b-348">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="4b82b-348">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="4b82b-349">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4b82b-349">Az.Monitor</span></span>
- <span data-ttu-id="4b82b-350">Döpte om Az.Insights till Az.Monitor och andra mindre icke-bakåtkompatibla ändringar. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="4b82b-350">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="4b82b-351">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4b82b-351">Az.KeyVault</span></span>
- <span data-ttu-id="4b82b-352">Tog bort den inaktuella egenskapen PurgeDisabled från utdatatyper</span><span class="sxs-lookup"><span data-stu-id="4b82b-352">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="4b82b-353">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="4b82b-353">Az.MachineLearning</span></span>
- <span data-ttu-id="4b82b-354">Inkluderade cmdletarna från modulen Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="4b82b-354">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="4b82b-355">Az.Media</span><span class="sxs-lookup"><span data-stu-id="4b82b-355">Az.Media</span></span>
- <span data-ttu-id="4b82b-356">Tog bort inaktuella -Tags-alias från New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="4b82b-356">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="4b82b-357">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4b82b-357">Az.Network</span></span>
<span data-ttu-id="4b82b-358">Stöd har lagts till för konfiguration av RewriteRuleSets i Application Gateway</span><span class="sxs-lookup"><span data-stu-id="4b82b-358">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="4b82b-359">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="4b82b-359">New cmdlets added:</span></span>
        - <span data-ttu-id="4b82b-360">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4b82b-360">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="4b82b-361">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4b82b-361">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="4b82b-362">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4b82b-362">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="4b82b-363">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4b82b-363">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="4b82b-364">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4b82b-364">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="4b82b-365">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="4b82b-365">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="4b82b-366">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="4b82b-366">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="4b82b-367">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="4b82b-367">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="4b82b-368">Cmdletar har uppdaterats med den valfria parametern -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4b82b-368">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="4b82b-369">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4b82b-369">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="4b82b-370">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="4b82b-370">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="4b82b-371">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="4b82b-371">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="4b82b-372">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4b82b-372">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="4b82b-373">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4b82b-373">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="4b82b-374">New-AzureRmApplicationGatewayUrlPathMapConfig har lagt till KeyVault-stöd för Application Gateway med Identity.</span><span class="sxs-lookup"><span data-stu-id="4b82b-374">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="4b82b-375">Cmdletar har uppdaterats med den valfria parametern -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="4b82b-375">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="4b82b-376">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="4b82b-376">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="4b82b-377">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="4b82b-377">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="4b82b-378">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="4b82b-378">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="4b82b-379">Cmdleten New-AzApplicationGateway har uppdaterats med den valfria parametern -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="4b82b-379">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="4b82b-380">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="4b82b-380">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="4b82b-381">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="4b82b-381">Az.OperationalInsights</span></span>
- <span data-ttu-id="4b82b-382">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="4b82b-382">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="4b82b-383">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="4b82b-383">Az.Profile</span></span>
- <span data-ttu-id="4b82b-384">Modulnamnet har ändrats till Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4b82b-384">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="4b82b-385">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4b82b-385">Az.RecoveryServices</span></span>
- <span data-ttu-id="4b82b-386">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="4b82b-386">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="4b82b-387">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4b82b-387">Az.Resources</span></span>
- <span data-ttu-id="4b82b-388">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="4b82b-388">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="4b82b-389">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4b82b-389">Az.ServiceFabric</span></span>
- <span data-ttu-id="4b82b-390">Stöd för specificering av certifikat efter eget namn och tumavtryck</span><span class="sxs-lookup"><span data-stu-id="4b82b-390">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="4b82b-391">Information om fler icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="4b82b-391">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="4b82b-392">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="4b82b-392">Az.SIgnalR</span></span>
- <span data-ttu-id="4b82b-393">Allmän tillgänglighet för PowerShell-cmdletar för SIgnalR</span><span class="sxs-lookup"><span data-stu-id="4b82b-393">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="4b82b-394">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4b82b-394">Az.Sql</span></span>
- <span data-ttu-id="4b82b-395">Lade till de nya identifieringstyperna Data_Exfiltration och Unsafe_Action i Threat Detection-cmdletar</span><span class="sxs-lookup"><span data-stu-id="4b82b-395">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="4b82b-396">Uppdaterade dokumentationsexempel för Sql Auditing-cmdletar</span><span class="sxs-lookup"><span data-stu-id="4b82b-396">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="4b82b-397">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="4b82b-397">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="4b82b-398">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4b82b-398">Az.Storage</span></span>
- <span data-ttu-id="4b82b-399">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="4b82b-399">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="4b82b-400">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4b82b-400">Az.Websites</span></span>
- <span data-ttu-id="4b82b-401">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="4b82b-401">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="4b82b-402">0.7.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="4b82b-402">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="4b82b-403">Allmänt</span><span class="sxs-lookup"><span data-stu-id="4b82b-403">General</span></span>

* <span data-ttu-id="4b82b-404">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="4b82b-404">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="4b82b-405">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4b82b-405">Az.Compute</span></span>

* <span data-ttu-id="4b82b-406">Lade till stöd för UltraSSD och Galleriavbildningar i de enkla parameteruppsättningarna för `New-AzVm(ss)`-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="4b82b-406">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="4b82b-407">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4b82b-407">Az.DataLakeStore</span></span>

* <span data-ttu-id="4b82b-408">Åtgärdade avslutande snedstreck i domänen för adls-konto</span><span class="sxs-lookup"><span data-stu-id="4b82b-408">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="4b82b-409">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="4b82b-409">Az.FrontDoor</span></span>

* <span data-ttu-id="4b82b-410">Brutna länkar korrigerades</span><span class="sxs-lookup"><span data-stu-id="4b82b-410">Fixed some broken links</span></span>
    - <span data-ttu-id="4b82b-411">I artiklarna New-AzureRmFrontDoor och Set-AzureRmFrontDoor artiklar korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="4b82b-411">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="4b82b-412">I artikeln New-AzureRmFrontDoorManagedRuleObject korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="4b82b-412">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="4b82b-413">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4b82b-413">Az.RecoveryServices</span></span>

* <span data-ttu-id="4b82b-414">Lade till valideringar på klientsidan för Azure-filresurs med återställningsåtgärder.</span><span class="sxs-lookup"><span data-stu-id="4b82b-414">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="4b82b-415">Gjorde storageAccountName och storageAccountResourceGroupName valfritt för afs-återställning.</span><span class="sxs-lookup"><span data-stu-id="4b82b-415">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="4b82b-416">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4b82b-416">Az.Resources</span></span>

* <span data-ttu-id="4b82b-417">Korrigering för https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="4b82b-417">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="4b82b-418">Uppdaterade Get-AzureRmRoleAssignment så att prenumerationsomfattningen används om den anges vid begäran om klassiska administratörer.</span><span class="sxs-lookup"><span data-stu-id="4b82b-418">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="4b82b-419">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4b82b-419">Az.Sql</span></span>

* <span data-ttu-id="4b82b-420">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="4b82b-420">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="4b82b-421">Korrigerade ett problem med Get-AzureRmSqlDatabaseVulnerabilityAssessment med DotNet-kärna</span><span class="sxs-lookup"><span data-stu-id="4b82b-421">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="4b82b-422">Ändrade dokumentationen för hjälpmeddelanden som rör SQL Auditing-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="4b82b-422">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="4b82b-423">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4b82b-423">Az.Storage</span></span>

* <span data-ttu-id="4b82b-424">Lade till -EnableHierarchicalNamespace i New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4b82b-424">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="4b82b-425">Åtgärdade problemet med att cmdleten Copy File inte kunde återanvända källkontexten på målet om inte -DestContext angetts</span><span class="sxs-lookup"><span data-stu-id="4b82b-425">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="4b82b-426">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="4b82b-426">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="4b82b-427">Stöd för statisk webbplatskonfiguration</span><span class="sxs-lookup"><span data-stu-id="4b82b-427">Support Static Website configuration</span></span>
    - <span data-ttu-id="4b82b-428">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="4b82b-428">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="4b82b-429">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="4b82b-429">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="4b82b-430">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4b82b-430">Az.Websites</span></span>

* <span data-ttu-id="4b82b-431">Set-AzureRmWebApp och Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4b82b-431">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="4b82b-432">Ny parameter (-AzureStoragePath) har lagts till för att ange att Azure Storage-sökvägar ska monteras i containerappar i Windows och Linux.</span><span class="sxs-lookup"><span data-stu-id="4b82b-432">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="4b82b-433">Använder utdata från den nya cmdleten New-AzureRmWebAppAzureStoragePath som en parameter för att ange sökvägar för Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="4b82b-433">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="4b82b-434">0.6.1 – november 2018</span><span class="sxs-lookup"><span data-stu-id="4b82b-434">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="4b82b-435">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4b82b-435">Az.ApiManagement</span></span>
* <span data-ttu-id="4b82b-436">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="4b82b-436">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="4b82b-437">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4b82b-437">Az.Automation</span></span>
* <span data-ttu-id="4b82b-438">Swagger baserade Azure Automation-cmdletar</span><span class="sxs-lookup"><span data-stu-id="4b82b-438">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="4b82b-439">Cmdletar för Uppdateringshantering har lagts till</span><span class="sxs-lookup"><span data-stu-id="4b82b-439">Added Update Management cmdlets</span></span>
* <span data-ttu-id="4b82b-440">Cmdletar för källkontroll har lagts till</span><span class="sxs-lookup"><span data-stu-id="4b82b-440">Added Source Control cmdlets</span></span>
* <span data-ttu-id="4b82b-441">Remove-AzureRmAutomationHybridWorkerGroup-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="4b82b-441">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="4b82b-442">Kommandot för DSC-registreringsnod har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="4b82b-442">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="4b82b-443">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4b82b-443">Az.Compute</span></span>
* <span data-ttu-id="4b82b-444">Problem med SystemAssigned-identitet har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="4b82b-444">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="4b82b-445">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="4b82b-445">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="4b82b-446">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="4b82b-446">Az.ContainerInstance</span></span>
* <span data-ttu-id="4b82b-447">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="4b82b-447">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="4b82b-448">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="4b82b-448">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="4b82b-449">uppdatera exempelbeskrivningen för marketplace-cmdletar</span><span class="sxs-lookup"><span data-stu-id="4b82b-449">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="4b82b-450">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4b82b-450">Az.Network</span></span>
* <span data-ttu-id="4b82b-451">Cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomErreller Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="4b82b-451">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="4b82b-452">ICMP tillbaka till stöd för Azure Firewall-nätverksprotokoll har lagts till</span><span class="sxs-lookup"><span data-stu-id="4b82b-452">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="4b82b-453">Uppdatera cmdlet Test-AzureRmNetworkWatcherConnectivity, lägga till verifiering av mål-id, adress och port.</span><span class="sxs-lookup"><span data-stu-id="4b82b-453">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="4b82b-454">Åtgärda problem med minnesanvändning i VirtualNetwork-karta</span><span class="sxs-lookup"><span data-stu-id="4b82b-454">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="4b82b-455">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="4b82b-455">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="4b82b-456">Åtgärda för att ändra principen för en skyddad fildelning.</span><span class="sxs-lookup"><span data-stu-id="4b82b-456">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="4b82b-457">Tidszonsprincipen har konverterats till versaler.</span><span class="sxs-lookup"><span data-stu-id="4b82b-457">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="4b82b-458">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="4b82b-458">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="4b82b-459">Exempel i New-AzureRmRecoveryServicesAsrProtectableItem har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="4b82b-459">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="4b82b-460">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="4b82b-460">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="4b82b-461">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="4b82b-461">Az.Relay</span></span>
* <span data-ttu-id="4b82b-462">Valfri parameter -KeyValue till New-AzureRmRelayKey cmdlet har lagts till, vilket gör det möjligt för användare att tillhandahålla KeyValue.</span><span class="sxs-lookup"><span data-stu-id="4b82b-462">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="4b82b-463">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4b82b-463">Az.Resources</span></span>
* <span data-ttu-id="4b82b-464">Uppdatera hjälpdokumentation för resursidentitet kopplad till parametrar i `New-AzureRmPolicyAssignment` och `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="4b82b-464">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="4b82b-465">Lägg till ett exempel för New-AzureRmPolicyDefinition som använder -Metadata</span><span class="sxs-lookup"><span data-stu-id="4b82b-465">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="4b82b-466">Korrigera så att skiftläge behålls i taggnycklar i NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="4b82b-466">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="4b82b-467">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4b82b-467">Az.ServiceFabric</span></span>
* <span data-ttu-id="4b82b-468">Lägg till utfasningsmeddelanden för kommande icke-kompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="4b82b-468">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="4b82b-469">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4b82b-469">Az.Sql</span></span>
* <span data-ttu-id="4b82b-470">Nya cmdletar för CRUD-åtgärder på Azure Sql Database-hanterad instans och Azure Sql-hanterad databas</span><span class="sxs-lookup"><span data-stu-id="4b82b-470">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="4b82b-471">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="4b82b-471">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="4b82b-472">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="4b82b-472">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="4b82b-473">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="4b82b-473">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="4b82b-474">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="4b82b-474">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="4b82b-475">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="4b82b-475">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="4b82b-476">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="4b82b-476">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="4b82b-477">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="4b82b-477">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="4b82b-478">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="4b82b-478">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="4b82b-479">Hantering av utökad granskningsprincip på en server eller en databas har aktiverats.</span><span class="sxs-lookup"><span data-stu-id="4b82b-479">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="4b82b-480">Ny parameter (PredicateExpression) har lagts till för att aktivera filtrering av granskningsloggar.</span><span class="sxs-lookup"><span data-stu-id="4b82b-480">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="4b82b-481">Cmdletar har ändrats så att de använder SQL-klienter i stället för äldre klienter.</span><span class="sxs-lookup"><span data-stu-id="4b82b-481">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="4b82b-482">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="4b82b-482">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="4b82b-483">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="4b82b-483">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="4b82b-484">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="4b82b-484">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="4b82b-485">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="4b82b-485">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="4b82b-486">Problem med att använda Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings med lagringskontots namnparameter har korrigerats</span><span class="sxs-lookup"><span data-stu-id="4b82b-486">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="4b82b-487">0.5.0 – november 2018</span><span class="sxs-lookup"><span data-stu-id="4b82b-487">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="4b82b-488">Allmänt</span><span class="sxs-lookup"><span data-stu-id="4b82b-488">General</span></span>
* <span data-ttu-id="4b82b-489">Lade till resurskompletterare till många kärn-cmdletar – dessa gör att du kan stega genom befintliga resursnamn med TABB vid interaktiva anrop till cmdletar</span><span class="sxs-lookup"><span data-stu-id="4b82b-489">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="4b82b-490">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="4b82b-490">Az.Profile</span></span>
* <span data-ttu-id="4b82b-491">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="4b82b-491">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="4b82b-492">Bytte namn på parametern TenantId i cmdleten Connect-AzAccount till Tenant och lade till ett alias för TenantId</span><span class="sxs-lookup"><span data-stu-id="4b82b-492">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="4b82b-493">Uppdaterade TenantId-beskrivningen för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="4b82b-493">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="4b82b-494">Åtgärda felmeddelande för misslyckad inloggning när du tillhandahåller klientdomän</span><span class="sxs-lookup"><span data-stu-id="4b82b-494">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="4b82b-495">Åtgärda problem med att kontextnamn hamnar i konflikt för konton utan prenumerationer i klientorganisationen</span><span class="sxs-lookup"><span data-stu-id="4b82b-495">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="4b82b-496">Åtgärda problem med DataLake-slutpunkter vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="4b82b-496">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="4b82b-497">Åtgärdade problem med att Disconnect-AzAccount kastades om den inte anslöts</span><span class="sxs-lookup"><span data-stu-id="4b82b-497">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="4b82b-498">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="4b82b-498">Az.CognitiveServices</span></span>
* <span data-ttu-id="4b82b-499">Lade till åtgärden Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="4b82b-499">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4b82b-500">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4b82b-500">Az.Compute</span></span>
* <span data-ttu-id="4b82b-501">Lade till cmdletarna Add-AzVmssVMDataDisk och Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="4b82b-501">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="4b82b-502">Get-AzVMImage visar AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="4b82b-502">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="4b82b-503">Åtgärdade att värdena för alternativen SetAzVMChefExtension -BootstrapOptions och -JsonAttribute inte angavs i json-format.</span><span class="sxs-lookup"><span data-stu-id="4b82b-503">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4b82b-504">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4b82b-504">Az.DataLakeStore</span></span>
* <span data-ttu-id="4b82b-505">Uppdatera DataLake-paketet till 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="4b82b-505">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="4b82b-506">Lägg till standardsamtidighet för flertrådade åtgärder.</span><span class="sxs-lookup"><span data-stu-id="4b82b-506">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="4b82b-507">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="4b82b-507">Az.Insights</span></span>
* <span data-ttu-id="4b82b-508">Åtgärdade problem #7267 (autoskalningsområde)</span><span class="sxs-lookup"><span data-stu-id="4b82b-508">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="4b82b-509">Problem med att uppräknade parametrar inte ställdes in ordentligt när du skapade en ny autoskalningsregel (de ställdes alltid in med standardvärdet).</span><span class="sxs-lookup"><span data-stu-id="4b82b-509">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="4b82b-510">Åtgärdade problem #7513 [Insights] Set-AzDiagnosticSetting kräver uttrycklig specifikation av kategorier när inställningar skapas</span><span class="sxs-lookup"><span data-stu-id="4b82b-510">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="4b82b-511">Nu kräver inte cmdleten uttrycklig anvisning av kategorierna för att aktiveras under skapande, d.v.s. den fungerar enligt beskrivning</span><span class="sxs-lookup"><span data-stu-id="4b82b-511">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4b82b-512">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4b82b-512">Az.Network</span></span>
* <span data-ttu-id="4b82b-513">PeeringType ändrades till en obligatorisk parameter för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="4b82b-513">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="4b82b-514">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="4b82b-514">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="4b82b-515">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="4b82b-515">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="4b82b-516">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="4b82b-516">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="4b82b-517">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="4b82b-517">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="4b82b-518">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="4b82b-518">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="4b82b-519">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="4b82b-519">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="4b82b-520">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="4b82b-520">Az.PolicyInsights</span></span>
* <span data-ttu-id="4b82b-521">Cmdletar för principreparation har lagts till</span><span class="sxs-lookup"><span data-stu-id="4b82b-521">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="4b82b-522">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4b82b-522">Az.Resources</span></span>
* <span data-ttu-id="4b82b-523">Korrigering för https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="4b82b-523">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="4b82b-524">Tillåt att resurser listas med parametern -ResourceId för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="4b82b-524">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="4b82b-525">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="4b82b-525">Az.ServiceBus</span></span>
* <span data-ttu-id="4b82b-526">Skrivskyddad MigrationState-egenskap har lagts till i PSServiceBusMigrationConfigurationAttributes, som hjälper till att hålla koll på migreringstillståndet.</span><span class="sxs-lookup"><span data-stu-id="4b82b-526">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="4b82b-527">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4b82b-527">Az.ServiceFabric</span></span>
* <span data-ttu-id="4b82b-528">Åtgärda att lägga till certifikat till Linux-Vmss.</span><span class="sxs-lookup"><span data-stu-id="4b82b-528">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="4b82b-529">Åtgärdade Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="4b82b-529">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="4b82b-530">Använd rätt tumavtryck från nya certifikat (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="4b82b-530">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="4b82b-531">Visa undantag korrekt (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="4b82b-531">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="4b82b-532">Åtgärdade Update-AzServiceFabricDurability så att klusterkonfigurationen uppdateras innan Vmss-åtgärden CreateOrUpdate påbörjas.</span><span class="sxs-lookup"><span data-stu-id="4b82b-532">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="4b82b-533">0.4.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="4b82b-533">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="4b82b-534">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="4b82b-534">Az.Profile</span></span>
* <span data-ttu-id="4b82b-535">Åtgärdade problemet med Get-AzSubscription i CloudShell</span><span class="sxs-lookup"><span data-stu-id="4b82b-535">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="4b82b-536">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="4b82b-536">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4b82b-537">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4b82b-537">Az.Compute</span></span>
* <span data-ttu-id="4b82b-538">Nya storlekar lades till i listan över godkända VM-storlekar för vilka accelererat nätverk kommer att aktiveras vid användning av den enkla parameteruppsättningen för New-AzVm</span><span class="sxs-lookup"><span data-stu-id="4b82b-538">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="4b82b-539">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="4b82b-539">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4b82b-540">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4b82b-540">Az.DataLakeStore</span></span>
* <span data-ttu-id="4b82b-541">Lägger till stöd för virtuella nätverksregler</span><span class="sxs-lookup"><span data-stu-id="4b82b-541">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="4b82b-542">Get-AzDataLakeStoreVirtualNetworkRule: Hämtar eller listar regel för virtuellt Azure Data Lake Store-nätverk.</span><span class="sxs-lookup"><span data-stu-id="4b82b-542">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="4b82b-543">Add-AzDataLakeStoreVirtualNetworkRule: Lägger till en regel för det virtuella nätverket till det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="4b82b-543">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="4b82b-544">Set-AzDataLakeStoreVirtualNetworkRule: Ändrar den angivna regeln för det virtuella nätverket i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="4b82b-544">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="4b82b-545">Remove-AzDataLakeStoreVirtualNetworkRule: Tar bort en regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4b82b-545">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4b82b-546">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4b82b-546">Az.Network</span></span>
* <span data-ttu-id="4b82b-547">Skicka protokollvärdet till serverdelen för att uppdatera cmdleten Test-AzNetworkWatcherConnectivity.</span><span class="sxs-lookup"><span data-stu-id="4b82b-547">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="4b82b-548">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="4b82b-548">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4b82b-549">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4b82b-549">Az.Resources</span></span>
* <span data-ttu-id="4b82b-550">Åtgärdade problem där Get-AzRoleDefinition genererar ett oläsligt undantag (när standardprofilen inte innehåller någon prenumeration och ingen omfattning har angetts) genom att lägga till ett beskrivande undantag i scenariot.</span><span class="sxs-lookup"><span data-stu-id="4b82b-550">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="4b82b-551">Ställ in ”RoleDefinitionNameParameterSet” som standardparameteruppsättning.</span><span class="sxs-lookup"><span data-stu-id="4b82b-551">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="4b82b-552">0.3.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="4b82b-552">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="4b82b-553">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="4b82b-553">Azure.Storage</span></span>
* <span data-ttu-id="4b82b-554">Åtgärda fel där Kopiera blob/fil inte kopierar metadata när målplatsen har ett problem med metadata</span><span class="sxs-lookup"><span data-stu-id="4b82b-554">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="4b82b-555">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="4b82b-555">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="4b82b-556">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="4b82b-556">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="4b82b-557">Stöd för att hämta användningsinformation om en Storage-resurs för en specifik plats och för att lägga till ett varningsmeddelande för att hämta användningsinformation om en global Storage-resurs är inaktuellt.</span><span class="sxs-lookup"><span data-stu-id="4b82b-557">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="4b82b-558">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="4b82b-558">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="4b82b-559">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="4b82b-559">Az.CognitiveServices</span></span>
* <span data-ttu-id="4b82b-560">Stöd för Get-AzCognitiveServicesAccountSkus utan ett befintligt konto.</span><span class="sxs-lookup"><span data-stu-id="4b82b-560">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4b82b-561">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4b82b-561">Az.Compute</span></span>
* <span data-ttu-id="4b82b-562">Åtgärdade fel där Get-AzVM -ResourceGroupName <rg> returnerar fler än 50 resultat om det behövs</span><span class="sxs-lookup"><span data-stu-id="4b82b-562">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="4b82b-563">Lade till ett exempel för SimpleParameterSet i hjälpen för cmdleten New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="4b82b-563">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="4b82b-564">Ett stavfel i förloppsmeddelandet för Azure Disk Encryption har korrigerats</span><span class="sxs-lookup"><span data-stu-id="4b82b-564">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="4b82b-565">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="4b82b-565">Az.DataFactoryV2</span></span>
* <span data-ttu-id="4b82b-566">ADF .Net SDK-versionen har uppdaterats till 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="4b82b-566">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4b82b-567">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4b82b-567">Az.Network</span></span>
* <span data-ttu-id="4b82b-568">Funktionalitet för NetworkProfile har lagts till.</span><span class="sxs-lookup"><span data-stu-id="4b82b-568">Added NetworkProfile functionality.</span></span> <span data-ttu-id="4b82b-569">nya cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="4b82b-569">new cmdlets added</span></span>
    - <span data-ttu-id="4b82b-570">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="4b82b-570">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="4b82b-571">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="4b82b-571">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="4b82b-572">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="4b82b-572">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="4b82b-573">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="4b82b-573">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="4b82b-574">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="4b82b-574">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="4b82b-575">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="4b82b-575">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="4b82b-576">Länk för tjänstassociering på modell för undernät har lagts till</span><span class="sxs-lookup"><span data-stu-id="4b82b-576">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="4b82b-577">Cmdletarna New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap och Remove-AzVirtualNetworkTap har lagts till</span><span class="sxs-lookup"><span data-stu-id="4b82b-577">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="4b82b-578">Cmdletarna Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig och Remove-AzNEtworkInterfaceTapConfig har lagts till</span><span class="sxs-lookup"><span data-stu-id="4b82b-578">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="4b82b-579">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="4b82b-579">Az.RedisCache</span></span>
* <span data-ttu-id="4b82b-580">Tillåt att alla strängar används som storleksparametrar framöver.</span><span class="sxs-lookup"><span data-stu-id="4b82b-580">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="4b82b-581">Lägg till P5 i popup-fönstret PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="4b82b-581">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="4b82b-582">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4b82b-582">Az.Resources</span></span>
* <span data-ttu-id="4b82b-583">Parametern -Mode som saknades i Set-AzPolicyDefinition har lagts till</span><span class="sxs-lookup"><span data-stu-id="4b82b-583">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="4b82b-584">Åtgärdade buggen för cmdleten Get-AzProviderOperation för åtgärder med ursprung som innehåller användare</span><span class="sxs-lookup"><span data-stu-id="4b82b-584">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="4b82b-585">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4b82b-585">Az.Sql</span></span>
* <span data-ttu-id="4b82b-586">Ett problem där vissa cmdletar för säkerhetskopiering inte kunde identifiera den aktuella azure-prenumerationen har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="4b82b-586">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4b82b-587">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4b82b-587">Az.Websites</span></span>
* <span data-ttu-id="4b82b-588">Ny cmdlet: Get-AzWebAppContainerContinuousDeploymentUrl – Hämtar webhook-URL:en för kontinuerlig distribution av container</span><span class="sxs-lookup"><span data-stu-id="4b82b-588">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="4b82b-589">Nya cmdletar: New-AzWebAppContainerPSSession och Enter-WebAppContainerPSSession – Startar en PowerShell-fjärrsession i en containerapp för windows</span><span class="sxs-lookup"><span data-stu-id="4b82b-589">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="4b82b-590">0.2.0 – september 2018</span><span class="sxs-lookup"><span data-stu-id="4b82b-590">0.2.0 - September 2018</span></span>
 <span data-ttu-id="4b82b-591">Första versionen</span><span class="sxs-lookup"><span data-stu-id="4b82b-591">Initial Release</span></span>