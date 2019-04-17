---
ms.openlocfilehash: 54d7a9da878e085e90479fb229876c9be6dafd74
ms.sourcegitcommit: 89066b7c4b527357bb2024e1ad708df84c131804
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/09/2019
ms.locfileid: "59364240"
---
## <a name="170---april-2019"></a><span data-ttu-id="86ccc-101">1.7.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="86ccc-101">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="86ccc-102">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="86ccc-102">Highlights since the last major release</span></span>
* <span data-ttu-id="86ccc-103">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="86ccc-103">General availability of `Az` module</span></span>
* <span data-ttu-id="86ccc-104">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="86ccc-104">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="86ccc-105">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="86ccc-105">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="86ccc-106">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="86ccc-106">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="86ccc-107">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="86ccc-107">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="86ccc-108">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="86ccc-108">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="86ccc-109">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="86ccc-109">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="86ccc-110">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="86ccc-110">Az.Accounts</span></span>
* <span data-ttu-id="86ccc-111">Add-AzEnvironment och Set-AzEnvironment har uppdaterats för att godkänna parametern AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="86ccc-111">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="86ccc-112">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="86ccc-112">Az.AnalysisServices</span></span>
* <span data-ttu-id="86ccc-113">ServiceClient används i cmdletar för dataplan och den ursprungliga autentiseringslogiken har tagits bort</span><span class="sxs-lookup"><span data-stu-id="86ccc-113">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="86ccc-114">Add-AzureASAccount används för omslutning av Connect-AzAccount för att undvika en icke-bakåtkompatibel ändring</span><span class="sxs-lookup"><span data-stu-id="86ccc-114">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="86ccc-115">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="86ccc-115">Az.Automation</span></span>
* <span data-ttu-id="86ccc-116">Buggen för cmdleten New-AzAutomationSoftwareUpdateConfiguration för inkluderingar har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="86ccc-116">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="86ccc-117">Nu bör parametern IncludedKbNumber och IncludedPackageNameMask fungera.</span><span class="sxs-lookup"><span data-stu-id="86ccc-117">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="86ccc-118">Felkorrigering för dynamiska grupper i uppdateringshanteringen för azure automation</span><span class="sxs-lookup"><span data-stu-id="86ccc-118">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="86ccc-119">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="86ccc-119">Az.Compute</span></span>
* <span data-ttu-id="86ccc-120">Lägg till parametern HyperVGeneration i New-AzDiskConfig och New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="86ccc-120">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="86ccc-121">Tillåt att virtuella datorer skapas med galleribilder från andra klientorganisationer.</span><span class="sxs-lookup"><span data-stu-id="86ccc-121">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="86ccc-122">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="86ccc-122">Az.ContainerInstance</span></span>
* <span data-ttu-id="86ccc-123">Ett problem har åtgärdats i parametern -Command för New-AzContainerGroup som lade till ett avslutande tomt argument</span><span class="sxs-lookup"><span data-stu-id="86ccc-123">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="86ccc-124">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="86ccc-124">Az.DataFactory</span></span>
* <span data-ttu-id="86ccc-125">ADF .Net SDK-versionen har uppdaterats till 3.0.2</span><span class="sxs-lookup"><span data-stu-id="86ccc-125">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="86ccc-126">Cmdleten Set-AzDataFactoryV2 har uppdaterats med extra parametrar för inställningar som rör RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="86ccc-126">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="86ccc-127">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="86ccc-127">Az.Resources</span></span>
* <span data-ttu-id="86ccc-128">Förbättra hanteringen av providrar för Get-AzResource när parametrarna -ResourceId eller -ResourceGroupName, -Name och -ResourceType tillhandahålls</span><span class="sxs-lookup"><span data-stu-id="86ccc-128">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="86ccc-129">Förbättra felhanteringen för Test-AzDeployment och Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="86ccc-129">Improve error handling for for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="86ccc-130">Hantera fel utanför distributionsvalideringen och ta med dem i kommandoutdata istället</span><span class="sxs-lookup"><span data-stu-id="86ccc-130">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="86ccc-131">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="86ccc-131">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="86ccc-132">Lägg till växlingsparametern -IgnoreDynamicParameters till en uppsättning av cmdletar för distribution för att hoppa över fråga i skript och jobbscenarier</span><span class="sxs-lookup"><span data-stu-id="86ccc-132">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="86ccc-133">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="86ccc-133">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="86ccc-134">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="86ccc-134">Az.Sql</span></span>
* <span data-ttu-id="86ccc-135">Stöd för dataklassificering av databaser.</span><span class="sxs-lookup"><span data-stu-id="86ccc-135">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="86ccc-136">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="86ccc-136">Az.Storage</span></span>
* <span data-ttu-id="86ccc-137">Rapportera detaljfel när lagringskontext skapas med parametern -UseConnectedAccount, men utan inloggning på Azure-kontot</span><span class="sxs-lookup"><span data-stu-id="86ccc-137">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="86ccc-138">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="86ccc-138">New-AzStorageContext</span></span>
* <span data-ttu-id="86ccc-139">Stöd för att hantera Blob Service-egenskaper för ett angivet lagringskonto med API:et för hanteringsplan</span><span class="sxs-lookup"><span data-stu-id="86ccc-139">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="86ccc-140">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="86ccc-140">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="86ccc-141">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="86ccc-141">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="86ccc-142">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="86ccc-142">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="86ccc-143">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="86ccc-143">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="86ccc-144">Stöd för -AsJob-cmdletar för att ladda upp och ladda ned blobar och filer</span><span class="sxs-lookup"><span data-stu-id="86ccc-144">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="86ccc-145">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="86ccc-145">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="86ccc-146">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="86ccc-146">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="86ccc-147">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="86ccc-147">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="86ccc-148">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="86ccc-148">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="86ccc-149">1.6.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="86ccc-149">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="86ccc-150">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="86ccc-150">Highlights since the last major release</span></span>
* <span data-ttu-id="86ccc-151">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="86ccc-151">General availability of `Az` module</span></span>
* <span data-ttu-id="86ccc-152">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="86ccc-152">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="86ccc-153">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="86ccc-153">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="86ccc-154">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="86ccc-154">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="86ccc-155">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="86ccc-155">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="86ccc-156">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="86ccc-156">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="86ccc-157">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="86ccc-157">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="86ccc-158">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="86ccc-158">Az.Automation</span></span>
* <span data-ttu-id="86ccc-159">Azure Automation – ändring av uppdateringshantering för stöd för de nya funktionerna:</span><span class="sxs-lookup"><span data-stu-id="86ccc-159">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="86ccc-160">Dynamisk gruppering</span><span class="sxs-lookup"><span data-stu-id="86ccc-160">Dynamic grouping</span></span>
    * <span data-ttu-id="86ccc-161">För-/efterskrift</span><span class="sxs-lookup"><span data-stu-id="86ccc-161">Pre-Post script</span></span>
    * <span data-ttu-id="86ccc-162">Inställning för omstart</span><span class="sxs-lookup"><span data-stu-id="86ccc-162">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="86ccc-163">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="86ccc-163">Az.Compute</span></span>
* <span data-ttu-id="86ccc-164">Åtgärda problem med sökvägsmatchning i Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="86ccc-164">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="86ccc-165">Uppdatera Compute-klientbibliotek till 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="86ccc-165">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="86ccc-166">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="86ccc-166">Az.KeyVault</span></span>
* <span data-ttu-id="86ccc-167">Stöd för jokertecken för KeyVault-cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="86ccc-167">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="86ccc-168">Az.Network</span><span class="sxs-lookup"><span data-stu-id="86ccc-168">Az.Network</span></span>
* <span data-ttu-id="86ccc-169">Lägg till stöd för Threat Intelligence för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="86ccc-169">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="86ccc-170">Lägg till resurs för brandväggsprincip på översta nivå och anpassade regler för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="86ccc-170">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="86ccc-171">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="86ccc-171">Az.RecoveryServices</span></span>
* <span data-ttu-id="86ccc-172">SnapshotRetentionInDays har lagts till i Azure-principen för virtuella datorer för stöd av Instant RP</span><span class="sxs-lookup"><span data-stu-id="86ccc-172">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="86ccc-173">Pipe-stöd för avregistrering av container har lagts till</span><span class="sxs-lookup"><span data-stu-id="86ccc-173">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="86ccc-174">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="86ccc-174">Az.Resources</span></span>
* <span data-ttu-id="86ccc-175">Uppdatera stöd för jokertecken för Get-AzResource och Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="86ccc-175">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="86ccc-176">Uppdatera autentiseringsuppgifter som används vid allmänna anrop till ARM</span><span class="sxs-lookup"><span data-stu-id="86ccc-176">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="86ccc-177">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="86ccc-177">Az.Sql</span></span>
* <span data-ttu-id="86ccc-178">Cmdlet-parametern (ExcludeDetectionType) för Hotidentifiering ändrades från DetectionType till sträng[] för att framtidssäkra den när nya DetectionTypes läggs till, och även för att stödja automatisk ifyllning.</span><span class="sxs-lookup"><span data-stu-id="86ccc-178">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="86ccc-179">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="86ccc-179">Az.Storage</span></span>
* <span data-ttu-id="86ccc-180">Stöd för att hämta/ange/ta bort hanteringsprincip på ett lagringskonto</span><span class="sxs-lookup"><span data-stu-id="86ccc-180">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="86ccc-181">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="86ccc-181">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="86ccc-182">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="86ccc-182">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="86ccc-183">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="86ccc-183">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="86ccc-184">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="86ccc-184">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="86ccc-185">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="86ccc-185">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="86ccc-186">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="86ccc-186">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="86ccc-187">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="86ccc-187">Az.Websites</span></span>
* <span data-ttu-id="86ccc-188">Åtgärda fel med ARM-mall som avbryter kloning av alla platser med 'New-AzWebApp -IncludeSourceWebAppSlots'</span><span class="sxs-lookup"><span data-stu-id="86ccc-188">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="86ccc-189">1.5.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="86ccc-189">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="86ccc-190">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="86ccc-190">Az.Accounts</span></span>
* <span data-ttu-id="86ccc-191">Lägg till kommandot Register-AzModule för stöd för AutoRest-genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="86ccc-191">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="86ccc-192">Uppdatera exempel för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="86ccc-192">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="86ccc-193">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="86ccc-193">Az.Automation</span></span>
* <span data-ttu-id="86ccc-194">Problem med att hämta vissa månadsscheman i flera Azure Automation-cmdletar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="86ccc-194">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="86ccc-195">Åtgärda problem med att Get-AzAutomationDscNode bara returnerar de 20 översta noderna.</span><span class="sxs-lookup"><span data-stu-id="86ccc-195">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="86ccc-196">Nu returneras alla noder</span><span class="sxs-lookup"><span data-stu-id="86ccc-196">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="86ccc-197">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="86ccc-197">Az.Cdn</span></span>
* <span data-ttu-id="86ccc-198">Nya Powershell-cmdletar för att aktivera/inaktivera anpassade domän-HTTPS har lagts till och de gamla har gjorts inaktuella</span><span class="sxs-lookup"><span data-stu-id="86ccc-198">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="86ccc-199">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="86ccc-199">Az.Compute</span></span>
* <span data-ttu-id="86ccc-200">Lägg till stöd för jokertecken för Get-cmdletar</span><span class="sxs-lookup"><span data-stu-id="86ccc-200">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="86ccc-201">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="86ccc-201">Az.DataFactory</span></span>
* <span data-ttu-id="86ccc-202">ADF .Net SDK-versionen har uppdaterats till 3.0.1</span><span class="sxs-lookup"><span data-stu-id="86ccc-202">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="86ccc-203">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="86ccc-203">Az.LogicApp</span></span>
* <span data-ttu-id="86ccc-204">Åtgärda problemet med att ListWorkflows endast hämtar den första sidan med resultat</span><span class="sxs-lookup"><span data-stu-id="86ccc-204">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="86ccc-205">Az.Network</span><span class="sxs-lookup"><span data-stu-id="86ccc-205">Az.Network</span></span>
* <span data-ttu-id="86ccc-206">Lägg till stöd för jokertecken för Network-cmdletar</span><span class="sxs-lookup"><span data-stu-id="86ccc-206">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="86ccc-207">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="86ccc-207">Az.RecoveryServices</span></span>
* <span data-ttu-id="86ccc-208">Stöd har lagts till för SQL Server i virtuella Azure-datorer</span><span class="sxs-lookup"><span data-stu-id="86ccc-208">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="86ccc-209">SDK-uppdatering</span><span class="sxs-lookup"><span data-stu-id="86ccc-209">SDK Update</span></span>
* <span data-ttu-id="86ccc-210">Get-ProtectableItem-incheckning i VMappContainer har tagits bort</span><span class="sxs-lookup"><span data-stu-id="86ccc-210">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="86ccc-211">Name och ServerName har lagts till som parametrar för Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="86ccc-211">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="86ccc-212">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="86ccc-212">Az.Resources</span></span>
* <span data-ttu-id="86ccc-213">Lägg till parametern `-TemplateObject` i cmdletar för distribution</span><span class="sxs-lookup"><span data-stu-id="86ccc-213">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="86ccc-214">Mer information här: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="86ccc-214">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="86ccc-215">Åtgärda problem med piping av resultatet i `Get-AzResource` till</span><span class="sxs-lookup"><span data-stu-id="86ccc-215">Fix issue when piping the result of `Get-AzResource` to</span></span> `Set-AzResource`
    - <span data-ttu-id="86ccc-216">Mer information här: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="86ccc-216">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="86ccc-217">Åtgärda problem med ändring av JSON-datatyp vid körning</span><span class="sxs-lookup"><span data-stu-id="86ccc-217">Fix issue with JSON data type change when running</span></span> `Set-AzResource`
    - <span data-ttu-id="86ccc-218">Mer information här: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="86ccc-218">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="86ccc-219">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="86ccc-219">Az.Sql</span></span>
* <span data-ttu-id="86ccc-220">AuditingEndpointsCommunicator uppdateras.</span><span class="sxs-lookup"><span data-stu-id="86ccc-220">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="86ccc-221">Åtgärdar beteendet hos ett gränsscenario när nya diagnostikinställningar skapas.</span><span class="sxs-lookup"><span data-stu-id="86ccc-221">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="86ccc-222">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="86ccc-222">Az.Storage</span></span>
* <span data-ttu-id="86ccc-223">Stöd för BlockBlobStorage när Storage-konto skapas      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="86ccc-223">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="86ccc-224">1.4.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="86ccc-224">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="86ccc-225">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="86ccc-225">Az.AnalysisServices</span></span>
* <span data-ttu-id="86ccc-226">Inaktuell AddAzureASAccount-cmdlet</span><span class="sxs-lookup"><span data-stu-id="86ccc-226">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="86ccc-227">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="86ccc-227">Az.Automation</span></span>
* <span data-ttu-id="86ccc-228">Hjälpen för Import-AzAutomationDscNodeConfiguration har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="86ccc-228">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="86ccc-229">Konfigurationsnamnsvalidering har lagts till i cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="86ccc-229">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="86ccc-230">Förbättrad felhantering för cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="86ccc-230">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="86ccc-231">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="86ccc-231">Az.CognitiveServices</span></span>
* <span data-ttu-id="86ccc-232">CustomSubdomainName har lagts till som en ny valfri parameter för New-AzCognitiveServicesAccount, som används för att ange underdomän för resursen.</span><span class="sxs-lookup"><span data-stu-id="86ccc-232">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="86ccc-233">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="86ccc-233">Az.Compute</span></span>
* <span data-ttu-id="86ccc-234">Problemet med ID-parameteruppsättningar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="86ccc-234">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="86ccc-235">Get-AzVMExtension har uppdaterats så att alla installerade tillägg visas om parametern Name inte har angetts</span><span class="sxs-lookup"><span data-stu-id="86ccc-235">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="86ccc-236">Parametrarna Tag och ResourceId har lagts till i cmdleten Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="86ccc-236">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="86ccc-237">Get-AzVmssVM utan instans-ID och med InstanceView kan visa virtuella VMSS-datorer med instansvyn.</span><span class="sxs-lookup"><span data-stu-id="86ccc-237">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="86ccc-238">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="86ccc-238">Az.DataLakeStore</span></span>
* <span data-ttu-id="86ccc-239">Cmdletar har lagts till för uppräkning och återställning av borttagna objekt i ADL</span><span class="sxs-lookup"><span data-stu-id="86ccc-239">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="86ccc-240">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="86ccc-240">Az.EventHub</span></span>
* <span data-ttu-id="86ccc-241">Ny boolesk egenskap SkipEmptyArchives har lagts till i Skip Empty Archives i CaptureDescription-klassen i Eventhub</span><span class="sxs-lookup"><span data-stu-id="86ccc-241">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="86ccc-242">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="86ccc-242">Az.KeyVault</span></span>
* <span data-ttu-id="86ccc-243">Taggning i Set-AzKeyVaultSecret har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="86ccc-243">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="86ccc-244">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="86ccc-244">Az.LogicApp</span></span>
* <span data-ttu-id="86ccc-245">Grundläggande SKU har lagts till för Integrationskonton</span><span class="sxs-lookup"><span data-stu-id="86ccc-245">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="86ccc-246">XSLT 2.0, XSLT 3.0 och Flytande mappningstyper har lagts till</span><span class="sxs-lookup"><span data-stu-id="86ccc-246">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="86ccc-247">Nya cmdletar för integrationskontosammansättningar</span><span class="sxs-lookup"><span data-stu-id="86ccc-247">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="86ccc-248">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="86ccc-248">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="86ccc-249">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="86ccc-249">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="86ccc-250">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="86ccc-250">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="86ccc-251">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="86ccc-251">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="86ccc-252">Nya cmdletar för batchkonfiguration för integrationskonto</span><span class="sxs-lookup"><span data-stu-id="86ccc-252">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="86ccc-253">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="86ccc-253">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="86ccc-254">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="86ccc-254">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="86ccc-255">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="86ccc-255">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="86ccc-256">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="86ccc-256">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="86ccc-257">Logic App-SDK har uppdaterats till version 4.1.0</span><span class="sxs-lookup"><span data-stu-id="86ccc-257">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="86ccc-258">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="86ccc-258">Az.Monitor</span></span>
* <span data-ttu-id="86ccc-259">Hjälpen för Get-AzMetric har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="86ccc-259">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="86ccc-260">Az.Network</span><span class="sxs-lookup"><span data-stu-id="86ccc-260">Az.Network</span></span>
* <span data-ttu-id="86ccc-261">Hjälpexempel för Add-AzApplicationGatewayCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="86ccc-261">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="86ccc-262">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="86ccc-262">Az.OperationalInsights</span></span>
* <span data-ttu-id="86ccc-263">Ytterligare stöd för datakällorna New och Get ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="86ccc-263">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="86ccc-264">Ny ApplicationInsights-typ har lagts till för att ge stöd för ”Get specific” och ”Get all” för ApplicationInsights-datakällor för angiven arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="86ccc-264">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="86ccc-265">Cmdleten New-AzOperationalInsightsApplicationInsightsDataSource har lagts till för att skapa datakälla med angivna parametrar för Application Insights-resurs: subscription Id, resourceGroupName och name.</span><span class="sxs-lookup"><span data-stu-id="86ccc-265">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="86ccc-266">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="86ccc-266">Az.Resources</span></span>
* <span data-ttu-id="86ccc-267">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="86ccc-267">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="86ccc-268">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="86ccc-268">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="86ccc-269">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="86ccc-269">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="86ccc-270">Fel som gör att KeyCredentials inte kan skapas upprepade gånger har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="86ccc-270">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="86ccc-271">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="86ccc-271">Az.Sql</span></span>
* <span data-ttu-id="86ccc-272">Stöd för nivån SQL DB-hyperskal har lagts till</span><span class="sxs-lookup"><span data-stu-id="86ccc-272">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="86ccc-273">Ett fel har åtgärdats där återställningen kunde misslyckas på grund av onödiga inställningsegenskaper i restore-förfrågan</span><span class="sxs-lookup"><span data-stu-id="86ccc-273">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="86ccc-274">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="86ccc-274">Az.Websites</span></span>
* <span data-ttu-id="86ccc-275">Rätt exempel i Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="86ccc-275">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="86ccc-276">1.3.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="86ccc-276">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="86ccc-277">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="86ccc-277">Az.Accounts</span></span>
* <span data-ttu-id="86ccc-278">Uppdatera till den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="86ccc-278">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="86ccc-279">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="86ccc-279">Az.AnalysisServices</span></span>
<span data-ttu-id="86ccc-280">Allmän tillgänglighet för Az.AnalysisServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="86ccc-280">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="86ccc-281">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="86ccc-281">Az.Compute</span></span>
* <span data-ttu-id="86ccc-282">AEM-tillägg: Lägg till stöd för UltraSSD-, P60-, P70- och P80-diskar</span><span class="sxs-lookup"><span data-stu-id="86ccc-282">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="86ccc-283">Uppdatera hjälpbeskrivning för Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="86ccc-283">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="86ccc-284">Uppdatera hjälpbeskrivning och exempel för Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="86ccc-284">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="86ccc-285">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="86ccc-285">Az.RecoveryServices</span></span>
<span data-ttu-id="86ccc-286">Allmän tillgänglighet för Az.RecoveryServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="86ccc-286">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="86ccc-287">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="86ccc-287">Az.Resources</span></span>
* <span data-ttu-id="86ccc-288">Korrigera taggar för resursgrupper</span><span class="sxs-lookup"><span data-stu-id="86ccc-288">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="86ccc-289">Mer information här: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="86ccc-289">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="86ccc-290">Åtgärda problem där `Get-AzureRmRoleAssignment` inte respekterar -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="86ccc-290">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="86ccc-291">Mer information här: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="86ccc-291">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="86ccc-292">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="86ccc-292">Az.Sql</span></span>
* <span data-ttu-id="86ccc-293">Lägga till Get/Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="86ccc-293">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="86ccc-294">Åtgärda problem där ett nullref-undantag uppstår när du kör SQL-cmdletar och inte är inloggad på ett Azure-konto</span><span class="sxs-lookup"><span data-stu-id="86ccc-294">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="86ccc-295">Åtgärda nullref-undantag i Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="86ccc-295">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="86ccc-296">1.2.1 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="86ccc-296">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="86ccc-297">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="86ccc-297">Az.Accounts</span></span>
* <span data-ttu-id="86ccc-298">Version med rätt version av autentisering</span><span class="sxs-lookup"><span data-stu-id="86ccc-298">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="86ccc-299">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="86ccc-299">Az.AnalysisServices</span></span>
* <span data-ttu-id="86ccc-300">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="86ccc-300">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="86ccc-301">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="86ccc-301">Az.RecoveryServices</span></span>
* <span data-ttu-id="86ccc-302">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="86ccc-302">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="86ccc-303">1.2.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="86ccc-303">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="86ccc-304">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="86ccc-304">Az.Accounts</span></span>
* <span data-ttu-id="86ccc-305">Lägga till interaktiv autentisering och autentisering med användarnamn/lösenord för endast Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="86ccc-305">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="86ccc-306">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="86ccc-306">Update incorrect online help URLs</span></span>
* <span data-ttu-id="86ccc-307">Lägga till varningsmeddelande i PS Core för Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="86ccc-307">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="86ccc-308">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="86ccc-308">Az.Aks</span></span>
* <span data-ttu-id="86ccc-309">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="86ccc-309">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="86ccc-310">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="86ccc-310">Az.Automation</span></span>
* <span data-ttu-id="86ccc-311">Stöd för Python 2-runbookflöden har lagts till</span><span class="sxs-lookup"><span data-stu-id="86ccc-311">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="86ccc-312">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="86ccc-312">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="86ccc-313">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="86ccc-313">Az.Cdn</span></span>
* <span data-ttu-id="86ccc-314">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="86ccc-314">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="86ccc-315">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="86ccc-315">Az.Compute</span></span>
* <span data-ttu-id="86ccc-316">Lägga till cmdleten Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="86ccc-316">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="86ccc-317">Lägga till TempDisk-parameter i Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="86ccc-317">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="86ccc-318">Korrigera varningsmeddelande för New-AzVM</span><span class="sxs-lookup"><span data-stu-id="86ccc-318">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="86ccc-319">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="86ccc-319">Az.ContainerRegistry</span></span>
* <span data-ttu-id="86ccc-320">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="86ccc-320">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="86ccc-321">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="86ccc-321">Az.DataFactory</span></span>
* <span data-ttu-id="86ccc-322">ADF .Net SDK-versionen har uppdaterats till 3.0.0</span><span class="sxs-lookup"><span data-stu-id="86ccc-322">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="86ccc-323">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="86ccc-323">Az.DataLakeStore</span></span>
* <span data-ttu-id="86ccc-324">Åtgärda problem med ADLS-slutpunkt vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="86ccc-324">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="86ccc-325">Mer information här: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="86ccc-325">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="86ccc-326">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="86ccc-326">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="86ccc-327">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="86ccc-327">Az.IotHub</span></span>
* <span data-ttu-id="86ccc-328">Lägga till kodningsformat i cmdleten Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="86ccc-328">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="86ccc-329">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="86ccc-329">Az.KeyVault</span></span>
* <span data-ttu-id="86ccc-330">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="86ccc-330">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="86ccc-331">Az.Network</span><span class="sxs-lookup"><span data-stu-id="86ccc-331">Az.Network</span></span>
* <span data-ttu-id="86ccc-332">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="86ccc-332">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="86ccc-333">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="86ccc-333">Az.Resources</span></span>
* <span data-ttu-id="86ccc-334">Åtgärda felaktiga exempel i referensdokumentationen ”New-AzADAppCredential” och ”New-AzADSpCredential”</span><span class="sxs-lookup"><span data-stu-id="86ccc-334">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="86ccc-335">Åtgärda problem där sökvägen för parametern ”-TemplateFile” inte omvandlas innan cmdletarna för distribution i resursgruppen körs</span><span class="sxs-lookup"><span data-stu-id="86ccc-335">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="86ccc-336">Az.Resources: Korrigera dokumentationen om standardvärdet för New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="86ccc-336">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="86ccc-337">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="86ccc-337">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="86ccc-338">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="86ccc-338">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="86ccc-339">Åtgärda formateringsproblemet med objektet ”PSResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="86ccc-339">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="86ccc-340">Mer information här: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="86ccc-340">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="86ccc-341">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="86ccc-341">Az.ServiceFabric</span></span>
* <span data-ttu-id="86ccc-342">Återställ när ett certifikat läggs till i en Virtual Machine Scale Sets-modell men ett undantag genereras. Detta har gjorts för att åtgärda följande fel: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="86ccc-342">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="86ccc-343">Korrigera några felmeddelanden.</span><span class="sxs-lookup"><span data-stu-id="86ccc-343">Fix some error messages.</span></span>
* <span data-ttu-id="86ccc-344">Korrigering av skapande av kluster med ARM-mall som är standard för New-AzServiceFabriCluster som inte fungerade med migrering till Az.</span><span class="sxs-lookup"><span data-stu-id="86ccc-344">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="86ccc-345">Korrigering av tilläggning av kluster/programcertifikat så att endast VM Scale Sets som motsvarar klustret läggs till genom att kontrollera ID för klustret i tillägget.</span><span class="sxs-lookup"><span data-stu-id="86ccc-345">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="86ccc-346">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="86ccc-346">Az.SignalR</span></span>
* <span data-ttu-id="86ccc-347">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="86ccc-347">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="86ccc-348">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="86ccc-348">Az.Sql</span></span>
* <span data-ttu-id="86ccc-349">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="86ccc-349">Update incorrect online help URLs</span></span>
* <span data-ttu-id="86ccc-350">Uppdaterad parameterbeskrivning för LicenseType-parameter med möjliga värden</span><span class="sxs-lookup"><span data-stu-id="86ccc-350">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="86ccc-351">Korrigering för att uppdatera hanterad instansidentitet som inte fungerar när det är den enda uppdaterade egenskapen</span><span class="sxs-lookup"><span data-stu-id="86ccc-351">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="86ccc-352">Stöd för anpassad sortering på hanterad instans</span><span class="sxs-lookup"><span data-stu-id="86ccc-352">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="86ccc-353">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="86ccc-353">Az.Storage</span></span>
* <span data-ttu-id="86ccc-354">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="86ccc-354">Update incorrect online help URLs</span></span>
* <span data-ttu-id="86ccc-355">Tillhandahåll detaljerat felmeddelande när en användare försöker hämta/konfigurera klassisk loggning/mått på ett Premium Storage-konto eftersom Premium Storage-kontot inte har stöd för klassisk loggning/mått.</span><span class="sxs-lookup"><span data-stu-id="86ccc-355">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="86ccc-356">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="86ccc-356">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="86ccc-357">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="86ccc-357">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="86ccc-358">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="86ccc-358">Az.TrafficManager</span></span>
* <span data-ttu-id="86ccc-359">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="86ccc-359">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="86ccc-360">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="86ccc-360">Az.Websites</span></span>
* <span data-ttu-id="86ccc-361">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="86ccc-361">Update incorrect online help URLs</span></span>
* <span data-ttu-id="86ccc-362">Korrigerar ”New-AzWebAppSSLBinding” så att certifikatet laddas upp till rätt resursgrupp och plats om appen finns i en ASE.</span><span class="sxs-lookup"><span data-stu-id="86ccc-362">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="86ccc-363">Korrigerar ”New-AzWebAppSSLBinding” så att taggarna inte skrivs över på en bindning av ett SSL-certifikat till en app</span><span class="sxs-lookup"><span data-stu-id="86ccc-363">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="86ccc-364">1.1.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="86ccc-364">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="86ccc-365">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="86ccc-365">Az.Accounts</span></span>
* <span data-ttu-id="86ccc-366">Lade till omfattningen ”Lokal” till Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="86ccc-366">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="86ccc-367">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="86ccc-367">Az.Compute</span></span>
* <span data-ttu-id="86ccc-368">Namn är nu valfritt i ID-parametern för Restart/Start/Stop/Remove/Set-AzVM och Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="86ccc-368">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="86ccc-369">Uppdaterade beskrivningen av ID i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="86ccc-369">Updated the description of ID in help files</span></span>
* <span data-ttu-id="86ccc-370">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="86ccc-370">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="86ccc-371">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="86ccc-371">Az.DataLakeStore</span></span>
* <span data-ttu-id="86ccc-372">Uppdatera sdk-versionen av dataplanet till 1.1.14 för SDK-korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="86ccc-372">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="86ccc-373">Korrigerade hanteringen av negativ accesstime och modificationtime för getfilestatus och liststatus; korrigera asynkront annulleringstoken</span><span class="sxs-lookup"><span data-stu-id="86ccc-373">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="86ccc-374">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="86ccc-374">Az.EventGrid</span></span>
* <span data-ttu-id="86ccc-375">Uppdaterat för användning av API-versionen 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="86ccc-375">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="86ccc-376">Uppdaterade följande cmdletar för att stödja nytt scenario i API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="86ccc-376">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="86ccc-377">New-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="86ccc-377">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="86ccc-378">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="86ccc-378">Event Time-To-Live,</span></span>
        - <span data-ttu-id="86ccc-379">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="86ccc-379">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="86ccc-380">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="86ccc-380">Dead letter endpoint.</span></span>
    - <span data-ttu-id="86ccc-381">Update-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="86ccc-381">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="86ccc-382">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="86ccc-382">Event Time-To-Live,</span></span>
        - <span data-ttu-id="86ccc-383">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="86ccc-383">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="86ccc-384">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="86ccc-384">Dead letter endpoint.</span></span>
* <span data-ttu-id="86ccc-385">Lade till nya enum-värden (storageQueue och hybridConnection) för alternativet EndpointType i cmdletarna New-AzureRmEventGridSubscription och Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="86ccc-385">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="86ccc-386">Visa varningsmeddelanden om skapande eller uppdatering av händelseprenumerationen förväntas medföra manuell åtgärd från användaren.</span><span class="sxs-lookup"><span data-stu-id="86ccc-386">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="86ccc-387">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="86ccc-387">Az.IotHub</span></span>
* <span data-ttu-id="86ccc-388">Har uppdaterats till den senaste versionen av SDK:n lotHub</span><span class="sxs-lookup"><span data-stu-id="86ccc-388">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="86ccc-389">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="86ccc-389">Az.LogicApp</span></span>
* <span data-ttu-id="86ccc-390">Get-AzLogicApp visar en lista över alla som inte har angivet namn</span><span class="sxs-lookup"><span data-stu-id="86ccc-390">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="86ccc-391">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="86ccc-391">Az.Resources</span></span>
* <span data-ttu-id="86ccc-392">Åtgärdade problem med parameteruppsättningen när parametrarna -ODataQuery och -ResourceId anges för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="86ccc-392">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="86ccc-393">Mer information här: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="86ccc-393">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="86ccc-394">Åtgärdade hantering av parametern -Custom i New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="86ccc-394">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="86ccc-395">Korrigerade stavfel i New-AzDeployment-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="86ccc-395">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="86ccc-396">Gjorde parametern -MailNickname obligatorisk för New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="86ccc-396">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="86ccc-397">Mer information här: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="86ccc-397">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="86ccc-398">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="86ccc-398">Az.SignalR</span></span>
* <span data-ttu-id="86ccc-399">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="86ccc-399">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="86ccc-400">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="86ccc-400">Az.Sql</span></span>
* <span data-ttu-id="86ccc-401">Konverterade lagringshanteringsklientens beroende av den normala SDK-implementeringen.</span><span class="sxs-lookup"><span data-stu-id="86ccc-401">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="86ccc-402">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="86ccc-402">Az.Storage</span></span>
* <span data-ttu-id="86ccc-403">Angav StorageAccountName för lagringskontext som det verkliga namnet på lagringskontot när det skapas med Sas Token, OAuth eller Anonymous</span><span class="sxs-lookup"><span data-stu-id="86ccc-403">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="86ccc-404">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="86ccc-404">New-AzStorageContext</span></span>
* <span data-ttu-id="86ccc-405">Skapade Sas Token för Blob Snapshot-objekt med parametern -FullUri, åtgärdade den returnerade URI:n så att den blir URI för ögonblicksbild</span><span class="sxs-lookup"><span data-stu-id="86ccc-405">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="86ccc-406">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="86ccc-406">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="86ccc-407">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="86ccc-407">Az.Websites</span></span>
* <span data-ttu-id="86ccc-408">Åtgärdade en bugg i datumparsningen i Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="86ccc-408">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="86ccc-409">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="86ccc-409">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="86ccc-410">1.0.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="86ccc-410">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="86ccc-411">Allmänt</span><span class="sxs-lookup"><span data-stu-id="86ccc-411">General</span></span>

- <span data-ttu-id="86ccc-412">Allmän tillgänglighet för Az-modulen</span><span class="sxs-lookup"><span data-stu-id="86ccc-412">General Availability of Az Module</span></span>
- <span data-ttu-id="86ccc-413">Onlinehjälp för varje modul</span><span class="sxs-lookup"><span data-stu-id="86ccc-413">Online help for each module</span></span>
- <span data-ttu-id="86ccc-414">Mer information och en översikt finns på [Az-informationssidan](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="86ccc-414">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="86ccc-415">Information om hur du migrerar från AzureRM finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="86ccc-415">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="86ccc-416">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="86ccc-416">Az.Accounts</span></span>
- <span data-ttu-id="86ccc-417">Har ändrats från Az.Profile</span><span class="sxs-lookup"><span data-stu-id="86ccc-417">Changed from Az.Profile</span></span>
- <span data-ttu-id="86ccc-418">Fasta tabellformat för profil- och kontexttyper</span><span class="sxs-lookup"><span data-stu-id="86ccc-418">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="86ccc-419">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="86ccc-419">Az.ApiManagement</span></span>
- <span data-ttu-id="86ccc-420">Korrigeringar för #7002</span><span class="sxs-lookup"><span data-stu-id="86ccc-420">Fixes for #7002</span></span>
- <span data-ttu-id="86ccc-421">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="86ccc-421">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="86ccc-422">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="86ccc-422">Az.Batch</span></span>
- <span data-ttu-id="86ccc-423">Lade till möjligheten att se vilken version av Azure Batch Node Agent som körs på var och en av de virtuella datorerna i en pool, via den nya egenskapen `NodeAgentInformation` på `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="86ccc-423">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="86ccc-424">Standarden `Caching` för `PSDataDisk` är nu `ReadWrite` i stället för `None`.</span><span class="sxs-lookup"><span data-stu-id="86ccc-424">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="86ccc-425">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="86ccc-425">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="86ccc-426">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="86ccc-426">Az.Billing</span></span>
- <span data-ttu-id="86ccc-427">Kombinerar cmdletarna för fakturering, förbrukning och UsageAggregates. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="86ccc-427">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="86ccc-428">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="86ccc-428">Az.CognitivServices</span></span>
- <span data-ttu-id="86ccc-429">Lade till kompletterare för SkuName och Typem som är tillgängliga i New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="86ccc-429">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="86ccc-430">Tog bort parameteruppsättningen GetSkusWithAccountParamSetName från Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="86ccc-430">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="86ccc-431">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="86ccc-431">Az.ContainerInstance</span></span>
- <span data-ttu-id="86ccc-432">Stöd för ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="86ccc-432">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="86ccc-433">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="86ccc-433">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="86ccc-434">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="86ccc-434">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="86ccc-435">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="86ccc-435">Az.DataLakeStore</span></span>
- <span data-ttu-id="86ccc-436">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="86ccc-436">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="86ccc-437">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="86ccc-437">Az.Monitor</span></span>
- <span data-ttu-id="86ccc-438">Döpte om Az.Insights till Az.Monitor och andra mindre icke-bakåtkompatibla ändringar. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="86ccc-438">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="86ccc-439">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="86ccc-439">Az.KeyVault</span></span>
- <span data-ttu-id="86ccc-440">Tog bort den inaktuella egenskapen PurgeDisabled från utdatatyper</span><span class="sxs-lookup"><span data-stu-id="86ccc-440">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="86ccc-441">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="86ccc-441">Az.MachineLearning</span></span>
- <span data-ttu-id="86ccc-442">Inkluderade cmdletarna från modulen Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="86ccc-442">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="86ccc-443">Az.Media</span><span class="sxs-lookup"><span data-stu-id="86ccc-443">Az.Media</span></span>
- <span data-ttu-id="86ccc-444">Tog bort inaktuella -Tags-alias från New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="86ccc-444">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="86ccc-445">Az.Network</span><span class="sxs-lookup"><span data-stu-id="86ccc-445">Az.Network</span></span>
<span data-ttu-id="86ccc-446">Stöd har lagts till för konfiguration av RewriteRuleSets i Application Gateway</span><span class="sxs-lookup"><span data-stu-id="86ccc-446">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="86ccc-447">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="86ccc-447">New cmdlets added:</span></span>
        - <span data-ttu-id="86ccc-448">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="86ccc-448">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="86ccc-449">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="86ccc-449">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="86ccc-450">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="86ccc-450">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="86ccc-451">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="86ccc-451">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="86ccc-452">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="86ccc-452">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="86ccc-453">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="86ccc-453">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="86ccc-454">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="86ccc-454">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="86ccc-455">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="86ccc-455">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="86ccc-456">Cmdletar har uppdaterats med den valfria parametern -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="86ccc-456">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="86ccc-457">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="86ccc-457">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="86ccc-458">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="86ccc-458">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="86ccc-459">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="86ccc-459">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="86ccc-460">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="86ccc-460">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="86ccc-461">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="86ccc-461">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="86ccc-462">New-AzureRmApplicationGatewayUrlPathMapConfig har lagt till KeyVault-stöd för Application Gateway med Identity.</span><span class="sxs-lookup"><span data-stu-id="86ccc-462">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="86ccc-463">Cmdletar har uppdaterats med den valfria parametern -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="86ccc-463">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="86ccc-464">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="86ccc-464">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="86ccc-465">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="86ccc-465">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="86ccc-466">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="86ccc-466">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="86ccc-467">Cmdleten New-AzApplicationGateway har uppdaterats med den valfria parametern -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="86ccc-467">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="86ccc-468">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="86ccc-468">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="86ccc-469">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="86ccc-469">Az.OperationalInsights</span></span>
- <span data-ttu-id="86ccc-470">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="86ccc-470">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="86ccc-471">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="86ccc-471">Az.Profile</span></span>
- <span data-ttu-id="86ccc-472">Modulnamnet har ändrats till Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="86ccc-472">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="86ccc-473">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="86ccc-473">Az.RecoveryServices</span></span>
- <span data-ttu-id="86ccc-474">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="86ccc-474">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="86ccc-475">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="86ccc-475">Az.Resources</span></span>
- <span data-ttu-id="86ccc-476">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="86ccc-476">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="86ccc-477">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="86ccc-477">Az.ServiceFabric</span></span>
- <span data-ttu-id="86ccc-478">Stöd för specificering av certifikat efter eget namn och tumavtryck</span><span class="sxs-lookup"><span data-stu-id="86ccc-478">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="86ccc-479">Information om fler icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="86ccc-479">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="86ccc-480">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="86ccc-480">Az.SIgnalR</span></span>
- <span data-ttu-id="86ccc-481">Allmän tillgänglighet för PowerShell-cmdletar för SIgnalR</span><span class="sxs-lookup"><span data-stu-id="86ccc-481">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="86ccc-482">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="86ccc-482">Az.Sql</span></span>
- <span data-ttu-id="86ccc-483">Lade till de nya identifieringstyperna Data_Exfiltration och Unsafe_Action i Threat Detection-cmdletar</span><span class="sxs-lookup"><span data-stu-id="86ccc-483">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="86ccc-484">Uppdaterade dokumentationsexempel för Sql Auditing-cmdletar</span><span class="sxs-lookup"><span data-stu-id="86ccc-484">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="86ccc-485">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="86ccc-485">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="86ccc-486">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="86ccc-486">Az.Storage</span></span>
- <span data-ttu-id="86ccc-487">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="86ccc-487">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="86ccc-488">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="86ccc-488">Az.Websites</span></span>
- <span data-ttu-id="86ccc-489">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="86ccc-489">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="86ccc-490">0.7.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="86ccc-490">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="86ccc-491">Allmänt</span><span class="sxs-lookup"><span data-stu-id="86ccc-491">General</span></span>

* <span data-ttu-id="86ccc-492">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="86ccc-492">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="86ccc-493">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="86ccc-493">Az.Compute</span></span>

* <span data-ttu-id="86ccc-494">Lade till stöd för UltraSSD och Galleriavbildningar i de enkla parameteruppsättningarna för `New-AzVm(ss)`-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="86ccc-494">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="86ccc-495">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="86ccc-495">Az.DataLakeStore</span></span>

* <span data-ttu-id="86ccc-496">Åtgärdade avslutande snedstreck i domänen för adls-konto</span><span class="sxs-lookup"><span data-stu-id="86ccc-496">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="86ccc-497">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="86ccc-497">Az.FrontDoor</span></span>

* <span data-ttu-id="86ccc-498">Brutna länkar korrigerades</span><span class="sxs-lookup"><span data-stu-id="86ccc-498">Fixed some broken links</span></span>
    - <span data-ttu-id="86ccc-499">I artiklarna New-AzureRmFrontDoor och Set-AzureRmFrontDoor artiklar korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="86ccc-499">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="86ccc-500">I artikeln New-AzureRmFrontDoorManagedRuleObject korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="86ccc-500">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="86ccc-501">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="86ccc-501">Az.RecoveryServices</span></span>

* <span data-ttu-id="86ccc-502">Lade till valideringar på klientsidan för Azure-filresurs med återställningsåtgärder.</span><span class="sxs-lookup"><span data-stu-id="86ccc-502">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="86ccc-503">Gjorde storageAccountName och storageAccountResourceGroupName valfritt för afs-återställning.</span><span class="sxs-lookup"><span data-stu-id="86ccc-503">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="86ccc-504">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="86ccc-504">Az.Resources</span></span>

* <span data-ttu-id="86ccc-505">Korrigering för https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="86ccc-505">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="86ccc-506">Uppdaterade Get-AzureRmRoleAssignment så att prenumerationsomfattningen används om den anges vid begäran om klassiska administratörer.</span><span class="sxs-lookup"><span data-stu-id="86ccc-506">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="86ccc-507">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="86ccc-507">Az.Sql</span></span>

* <span data-ttu-id="86ccc-508">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="86ccc-508">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="86ccc-509">Korrigerade ett problem med Get-AzureRmSqlDatabaseVulnerabilityAssessment med DotNet-kärna</span><span class="sxs-lookup"><span data-stu-id="86ccc-509">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="86ccc-510">Ändrade dokumentationen för hjälpmeddelanden som rör SQL Auditing-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="86ccc-510">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="86ccc-511">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="86ccc-511">Az.Storage</span></span>

* <span data-ttu-id="86ccc-512">Lade till -EnableHierarchicalNamespace i New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="86ccc-512">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="86ccc-513">Åtgärdade problemet med att cmdleten Copy File inte kunde återanvända källkontexten på målet om inte -DestContext angetts</span><span class="sxs-lookup"><span data-stu-id="86ccc-513">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="86ccc-514">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="86ccc-514">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="86ccc-515">Stöd för statisk webbplatskonfiguration</span><span class="sxs-lookup"><span data-stu-id="86ccc-515">Support Static Website configuration</span></span>
    - <span data-ttu-id="86ccc-516">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="86ccc-516">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="86ccc-517">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="86ccc-517">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="86ccc-518">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="86ccc-518">Az.Websites</span></span>

* <span data-ttu-id="86ccc-519">Set-AzureRmWebApp och Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="86ccc-519">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="86ccc-520">Ny parameter (-AzureStoragePath) har lagts till för att ange att Azure Storage-sökvägar ska monteras i containerappar i Windows och Linux.</span><span class="sxs-lookup"><span data-stu-id="86ccc-520">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="86ccc-521">Använder utdata från den nya cmdleten New-AzureRmWebAppAzureStoragePath som en parameter för att ange sökvägar för Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="86ccc-521">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="86ccc-522">0.6.1 – november 2018</span><span class="sxs-lookup"><span data-stu-id="86ccc-522">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="86ccc-523">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="86ccc-523">Az.ApiManagement</span></span>
* <span data-ttu-id="86ccc-524">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="86ccc-524">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="86ccc-525">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="86ccc-525">Az.Automation</span></span>
* <span data-ttu-id="86ccc-526">Swagger baserade Azure Automation-cmdletar</span><span class="sxs-lookup"><span data-stu-id="86ccc-526">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="86ccc-527">Cmdletar för Uppdateringshantering har lagts till</span><span class="sxs-lookup"><span data-stu-id="86ccc-527">Added Update Management cmdlets</span></span>
* <span data-ttu-id="86ccc-528">Cmdletar för källkontroll har lagts till</span><span class="sxs-lookup"><span data-stu-id="86ccc-528">Added Source Control cmdlets</span></span>
* <span data-ttu-id="86ccc-529">Remove-AzureRmAutomationHybridWorkerGroup-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="86ccc-529">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="86ccc-530">Kommandot för DSC-registreringsnod har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="86ccc-530">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="86ccc-531">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="86ccc-531">Az.Compute</span></span>
* <span data-ttu-id="86ccc-532">Problem med SystemAssigned-identitet har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="86ccc-532">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="86ccc-533">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="86ccc-533">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="86ccc-534">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="86ccc-534">Az.ContainerInstance</span></span>
* <span data-ttu-id="86ccc-535">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="86ccc-535">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="86ccc-536">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="86ccc-536">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="86ccc-537">uppdatera exempelbeskrivningen för marketplace-cmdletar</span><span class="sxs-lookup"><span data-stu-id="86ccc-537">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="86ccc-538">Az.Network</span><span class="sxs-lookup"><span data-stu-id="86ccc-538">Az.Network</span></span>
* <span data-ttu-id="86ccc-539">Cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomErreller Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="86ccc-539">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="86ccc-540">ICMP tillbaka till stöd för Azure Firewall-nätverksprotokoll har lagts till</span><span class="sxs-lookup"><span data-stu-id="86ccc-540">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="86ccc-541">Uppdatera cmdlet Test-AzureRmNetworkWatcherConnectivity, lägga till verifiering av mål-id, adress och port.</span><span class="sxs-lookup"><span data-stu-id="86ccc-541">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="86ccc-542">Åtgärda problem med minnesanvändning i VirtualNetwork-karta</span><span class="sxs-lookup"><span data-stu-id="86ccc-542">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="86ccc-543">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="86ccc-543">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="86ccc-544">Åtgärda för att ändra principen för en skyddad fildelning.</span><span class="sxs-lookup"><span data-stu-id="86ccc-544">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="86ccc-545">Tidszonsprincipen har konverterats till versaler.</span><span class="sxs-lookup"><span data-stu-id="86ccc-545">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="86ccc-546">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="86ccc-546">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="86ccc-547">Exempel i New-AzureRmRecoveryServicesAsrProtectableItem har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="86ccc-547">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="86ccc-548">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="86ccc-548">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="86ccc-549">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="86ccc-549">Az.Relay</span></span>
* <span data-ttu-id="86ccc-550">Valfri parameter -KeyValue till New-AzureRmRelayKey cmdlet har lagts till, vilket gör det möjligt för användare att tillhandahålla KeyValue.</span><span class="sxs-lookup"><span data-stu-id="86ccc-550">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="86ccc-551">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="86ccc-551">Az.Resources</span></span>
* <span data-ttu-id="86ccc-552">Uppdatera hjälpdokumentationen för resursidentitet kopplad till parametrar i `New-AzureRmPolicyAssignment` och</span><span class="sxs-lookup"><span data-stu-id="86ccc-552">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and</span></span> `Set-AzureRmPolicyAssignment`
* <span data-ttu-id="86ccc-553">Lägg till ett exempel för New-AzureRmPolicyDefinition som använder -Metadata</span><span class="sxs-lookup"><span data-stu-id="86ccc-553">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="86ccc-554">Korrigera så att skiftläge behålls i taggnycklar i NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="86ccc-554">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="86ccc-555">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="86ccc-555">Az.ServiceFabric</span></span>
* <span data-ttu-id="86ccc-556">Lägg till utfasningsmeddelanden för kommande icke-kompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="86ccc-556">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="86ccc-557">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="86ccc-557">Az.Sql</span></span>
* <span data-ttu-id="86ccc-558">Nya cmdletar för CRUD-åtgärder på Azure Sql Database-hanterad instans och Azure Sql-hanterad databas</span><span class="sxs-lookup"><span data-stu-id="86ccc-558">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="86ccc-559">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="86ccc-559">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="86ccc-560">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="86ccc-560">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="86ccc-561">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="86ccc-561">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="86ccc-562">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="86ccc-562">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="86ccc-563">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="86ccc-563">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="86ccc-564">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="86ccc-564">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="86ccc-565">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="86ccc-565">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="86ccc-566">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="86ccc-566">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="86ccc-567">Hantering av utökad granskningsprincip på en server eller en databas har aktiverats.</span><span class="sxs-lookup"><span data-stu-id="86ccc-567">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="86ccc-568">Ny parameter (PredicateExpression) har lagts till för att aktivera filtrering av granskningsloggar.</span><span class="sxs-lookup"><span data-stu-id="86ccc-568">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="86ccc-569">Cmdletar har ändrats så att de använder SQL-klienter i stället för äldre klienter.</span><span class="sxs-lookup"><span data-stu-id="86ccc-569">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="86ccc-570">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="86ccc-570">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="86ccc-571">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="86ccc-571">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="86ccc-572">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="86ccc-572">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="86ccc-573">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="86ccc-573">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="86ccc-574">Problem med att använda Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings med lagringskontots namnparameter har korrigerats</span><span class="sxs-lookup"><span data-stu-id="86ccc-574">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="86ccc-575">0.5.0 – november 2018</span><span class="sxs-lookup"><span data-stu-id="86ccc-575">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="86ccc-576">Allmänt</span><span class="sxs-lookup"><span data-stu-id="86ccc-576">General</span></span>
* <span data-ttu-id="86ccc-577">Lade till resurskompletterare till många kärn-cmdletar – dessa gör att du kan stega genom befintliga resursnamn med TABB vid interaktiva anrop till cmdletar</span><span class="sxs-lookup"><span data-stu-id="86ccc-577">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="86ccc-578">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="86ccc-578">Az.Profile</span></span>
* <span data-ttu-id="86ccc-579">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="86ccc-579">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="86ccc-580">Bytte namn på parametern TenantId i cmdleten Connect-AzAccount till Tenant och lade till ett alias för TenantId</span><span class="sxs-lookup"><span data-stu-id="86ccc-580">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="86ccc-581">Uppdaterade TenantId-beskrivningen för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="86ccc-581">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="86ccc-582">Åtgärda felmeddelande för misslyckad inloggning när du tillhandahåller klientdomän</span><span class="sxs-lookup"><span data-stu-id="86ccc-582">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="86ccc-583">Åtgärda problem med att kontextnamn hamnar i konflikt för konton utan prenumerationer i klientorganisationen</span><span class="sxs-lookup"><span data-stu-id="86ccc-583">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="86ccc-584">Åtgärda problem med DataLake-slutpunkter vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="86ccc-584">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="86ccc-585">Åtgärdade problem med att Disconnect-AzAccount kastades om den inte anslöts</span><span class="sxs-lookup"><span data-stu-id="86ccc-585">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="86ccc-586">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="86ccc-586">Az.CognitiveServices</span></span>
* <span data-ttu-id="86ccc-587">Lade till åtgärden Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="86ccc-587">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="86ccc-588">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="86ccc-588">Az.Compute</span></span>
* <span data-ttu-id="86ccc-589">Lade till cmdletarna Add-AzVmssVMDataDisk och Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="86ccc-589">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="86ccc-590">Get-AzVMImage visar AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="86ccc-590">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="86ccc-591">Åtgärdade att värdena för alternativen SetAzVMChefExtension -BootstrapOptions och -JsonAttribute inte angavs i json-format.</span><span class="sxs-lookup"><span data-stu-id="86ccc-591">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="86ccc-592">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="86ccc-592">Az.DataLakeStore</span></span>
* <span data-ttu-id="86ccc-593">Uppdatera DataLake-paketet till 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="86ccc-593">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="86ccc-594">Lägg till standardsamtidighet för flertrådade åtgärder.</span><span class="sxs-lookup"><span data-stu-id="86ccc-594">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="86ccc-595">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="86ccc-595">Az.Insights</span></span>
* <span data-ttu-id="86ccc-596">Åtgärdade problem #7267 (autoskalningsområde)</span><span class="sxs-lookup"><span data-stu-id="86ccc-596">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="86ccc-597">Problem med att uppräknade parametrar inte ställdes in ordentligt när du skapade en ny autoskalningsregel (de ställdes alltid in med standardvärdet).</span><span class="sxs-lookup"><span data-stu-id="86ccc-597">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="86ccc-598">Åtgärdade problem #7513 [Insights] Set-AzDiagnosticSetting kräver uttrycklig specifikation av kategorier när inställningar skapas</span><span class="sxs-lookup"><span data-stu-id="86ccc-598">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="86ccc-599">Nu kräver inte cmdleten uttrycklig anvisning av kategorierna för att aktiveras under skapande, d.v.s. den fungerar enligt beskrivning</span><span class="sxs-lookup"><span data-stu-id="86ccc-599">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="86ccc-600">Az.Network</span><span class="sxs-lookup"><span data-stu-id="86ccc-600">Az.Network</span></span>
* <span data-ttu-id="86ccc-601">PeeringType ändrades till en obligatorisk parameter för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="86ccc-601">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="86ccc-602">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="86ccc-602">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="86ccc-603">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="86ccc-603">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="86ccc-604">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="86ccc-604">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="86ccc-605">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="86ccc-605">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="86ccc-606">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="86ccc-606">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="86ccc-607">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="86ccc-607">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="86ccc-608">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="86ccc-608">Az.PolicyInsights</span></span>
* <span data-ttu-id="86ccc-609">Cmdletar för principreparation har lagts till</span><span class="sxs-lookup"><span data-stu-id="86ccc-609">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="86ccc-610">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="86ccc-610">Az.Resources</span></span>
* <span data-ttu-id="86ccc-611">Korrigering för https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="86ccc-611">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="86ccc-612">Tillåt att resurser listas med parametern -ResourceId för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="86ccc-612">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="86ccc-613">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="86ccc-613">Az.ServiceBus</span></span>
* <span data-ttu-id="86ccc-614">Skrivskyddad MigrationState-egenskap har lagts till i PSServiceBusMigrationConfigurationAttributes, som hjälper till att hålla koll på migreringstillståndet.</span><span class="sxs-lookup"><span data-stu-id="86ccc-614">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="86ccc-615">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="86ccc-615">Az.ServiceFabric</span></span>
* <span data-ttu-id="86ccc-616">Åtgärda att lägga till certifikat till Linux-Vmss.</span><span class="sxs-lookup"><span data-stu-id="86ccc-616">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="86ccc-617">Åtgärdade Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="86ccc-617">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="86ccc-618">Använd rätt tumavtryck från nya certifikat (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="86ccc-618">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="86ccc-619">Visa undantag korrekt (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="86ccc-619">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="86ccc-620">Åtgärdade Update-AzServiceFabricDurability så att klusterkonfigurationen uppdateras innan Vmss-åtgärden CreateOrUpdate påbörjas.</span><span class="sxs-lookup"><span data-stu-id="86ccc-620">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="86ccc-621">0.4.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="86ccc-621">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="86ccc-622">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="86ccc-622">Az.Profile</span></span>
* <span data-ttu-id="86ccc-623">Åtgärdade problemet med Get-AzSubscription i CloudShell</span><span class="sxs-lookup"><span data-stu-id="86ccc-623">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="86ccc-624">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="86ccc-624">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="86ccc-625">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="86ccc-625">Az.Compute</span></span>
* <span data-ttu-id="86ccc-626">Nya storlekar lades till i listan över godkända VM-storlekar för vilka accelererat nätverk kommer att aktiveras vid användning av den enkla parameteruppsättningen för New-AzVm</span><span class="sxs-lookup"><span data-stu-id="86ccc-626">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="86ccc-627">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="86ccc-627">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="86ccc-628">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="86ccc-628">Az.DataLakeStore</span></span>
* <span data-ttu-id="86ccc-629">Lägger till stöd för virtuella nätverksregler</span><span class="sxs-lookup"><span data-stu-id="86ccc-629">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="86ccc-630">Get-AzDataLakeStoreVirtualNetworkRule: Hämtar eller listar regel för virtuellt Azure Data Lake Store-nätverk.</span><span class="sxs-lookup"><span data-stu-id="86ccc-630">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="86ccc-631">Add-AzDataLakeStoreVirtualNetworkRule: Lägger till en regel för det virtuella nätverket till det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="86ccc-631">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="86ccc-632">Set-AzDataLakeStoreVirtualNetworkRule: Ändrar den angivna regeln för det virtuella nätverket i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="86ccc-632">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="86ccc-633">Remove-AzDataLakeStoreVirtualNetworkRule: Tar bort en regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="86ccc-633">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="86ccc-634">Az.Network</span><span class="sxs-lookup"><span data-stu-id="86ccc-634">Az.Network</span></span>
* <span data-ttu-id="86ccc-635">Skicka protokollvärdet till serverdelen för att uppdatera cmdleten Test-AzNetworkWatcherConnectivity.</span><span class="sxs-lookup"><span data-stu-id="86ccc-635">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="86ccc-636">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="86ccc-636">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="86ccc-637">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="86ccc-637">Az.Resources</span></span>
* <span data-ttu-id="86ccc-638">Åtgärdade problem där Get-AzRoleDefinition genererar ett oläsligt undantag (när standardprofilen inte innehåller någon prenumeration och ingen omfattning har angetts) genom att lägga till ett beskrivande undantag i scenariot.</span><span class="sxs-lookup"><span data-stu-id="86ccc-638">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="86ccc-639">Ställ in ”RoleDefinitionNameParameterSet” som standardparameteruppsättning.</span><span class="sxs-lookup"><span data-stu-id="86ccc-639">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="86ccc-640">0.3.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="86ccc-640">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="86ccc-641">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="86ccc-641">Azure.Storage</span></span>
* <span data-ttu-id="86ccc-642">Åtgärda fel där Kopiera blob/fil inte kopierar metadata när målplatsen har ett problem med metadata</span><span class="sxs-lookup"><span data-stu-id="86ccc-642">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="86ccc-643">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="86ccc-643">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="86ccc-644">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="86ccc-644">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="86ccc-645">Stöd för att hämta användningsinformation om en Storage-resurs för en specifik plats och för att lägga till ett varningsmeddelande för att hämta användningsinformation om en global Storage-resurs är inaktuellt.</span><span class="sxs-lookup"><span data-stu-id="86ccc-645">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="86ccc-646">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="86ccc-646">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="86ccc-647">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="86ccc-647">Az.CognitiveServices</span></span>
* <span data-ttu-id="86ccc-648">Stöd för Get-AzCognitiveServicesAccountSkus utan ett befintligt konto.</span><span class="sxs-lookup"><span data-stu-id="86ccc-648">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="86ccc-649">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="86ccc-649">Az.Compute</span></span>
* <span data-ttu-id="86ccc-650">Åtgärdade fel där Get-AzVM -ResourceGroupName <rg> returnerar fler än 50 resultat om det behövs</span><span class="sxs-lookup"><span data-stu-id="86ccc-650">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="86ccc-651">Lade till ett exempel för SimpleParameterSet i hjälpen för cmdleten New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="86ccc-651">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="86ccc-652">Ett stavfel i förloppsmeddelandet för Azure Disk Encryption har korrigerats</span><span class="sxs-lookup"><span data-stu-id="86ccc-652">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="86ccc-653">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="86ccc-653">Az.DataFactoryV2</span></span>
* <span data-ttu-id="86ccc-654">ADF .Net SDK-versionen har uppdaterats till 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="86ccc-654">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="86ccc-655">Az.Network</span><span class="sxs-lookup"><span data-stu-id="86ccc-655">Az.Network</span></span>
* <span data-ttu-id="86ccc-656">Funktionalitet för NetworkProfile har lagts till.</span><span class="sxs-lookup"><span data-stu-id="86ccc-656">Added NetworkProfile functionality.</span></span> <span data-ttu-id="86ccc-657">nya cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="86ccc-657">new cmdlets added</span></span>
    - <span data-ttu-id="86ccc-658">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="86ccc-658">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="86ccc-659">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="86ccc-659">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="86ccc-660">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="86ccc-660">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="86ccc-661">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="86ccc-661">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="86ccc-662">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="86ccc-662">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="86ccc-663">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="86ccc-663">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="86ccc-664">Länk för tjänstassociering på modell för undernät har lagts till</span><span class="sxs-lookup"><span data-stu-id="86ccc-664">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="86ccc-665">Cmdletarna New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap och Remove-AzVirtualNetworkTap har lagts till</span><span class="sxs-lookup"><span data-stu-id="86ccc-665">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="86ccc-666">Cmdletarna Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig och Remove-AzNEtworkInterfaceTapConfig har lagts till</span><span class="sxs-lookup"><span data-stu-id="86ccc-666">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="86ccc-667">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="86ccc-667">Az.RedisCache</span></span>
* <span data-ttu-id="86ccc-668">Tillåt att alla strängar används som storleksparametrar framöver.</span><span class="sxs-lookup"><span data-stu-id="86ccc-668">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="86ccc-669">Lägg till P5 i popup-fönstret PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="86ccc-669">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="86ccc-670">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="86ccc-670">Az.Resources</span></span>
* <span data-ttu-id="86ccc-671">Parametern -Mode som saknades i Set-AzPolicyDefinition har lagts till</span><span class="sxs-lookup"><span data-stu-id="86ccc-671">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="86ccc-672">Åtgärdade buggen för cmdleten Get-AzProviderOperation för åtgärder med ursprung som innehåller användare</span><span class="sxs-lookup"><span data-stu-id="86ccc-672">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="86ccc-673">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="86ccc-673">Az.Sql</span></span>
* <span data-ttu-id="86ccc-674">Ett problem där vissa cmdletar för säkerhetskopiering inte kunde identifiera den aktuella azure-prenumerationen har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="86ccc-674">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="86ccc-675">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="86ccc-675">Az.Websites</span></span>
* <span data-ttu-id="86ccc-676">Ny cmdlet: Get-AzWebAppContainerContinuousDeploymentUrl – Hämtar webhook-URL:en för kontinuerlig distribution av container</span><span class="sxs-lookup"><span data-stu-id="86ccc-676">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="86ccc-677">Nya cmdletar: New-AzWebAppContainerPSSession och Enter-WebAppContainerPSSession – Startar en PowerShell-fjärrsession i en containerapp för windows</span><span class="sxs-lookup"><span data-stu-id="86ccc-677">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="86ccc-678">0.2.0 – september 2018</span><span class="sxs-lookup"><span data-stu-id="86ccc-678">0.2.0 - September 2018</span></span>
 <span data-ttu-id="86ccc-679">Första versionen</span><span class="sxs-lookup"><span data-stu-id="86ccc-679">Initial Release</span></span>