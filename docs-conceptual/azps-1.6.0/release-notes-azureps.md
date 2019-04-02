---
ms.openlocfilehash: 2db9810e20254373a487013de50d4297d4ec50d5
ms.sourcegitcommit: 8f59e11e5c991543964154d63648aa1e6ae22512
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/26/2019
ms.locfileid: "58475637"
---
## <a name="160---march-2019"></a><span data-ttu-id="c6c96-101">1.6.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="c6c96-101">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="c6c96-102">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="c6c96-102">Highlights since the last major release</span></span>
* <span data-ttu-id="c6c96-103">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="c6c96-103">General availability of `Az` module</span></span>
* <span data-ttu-id="c6c96-104">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="c6c96-104">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="c6c96-105">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="c6c96-105">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="c6c96-106">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="c6c96-106">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="c6c96-107">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="c6c96-107">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="c6c96-108">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="c6c96-108">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="c6c96-109">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="c6c96-109">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="c6c96-110">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c6c96-110">Az.Automation</span></span>
* <span data-ttu-id="c6c96-111">Azure Automation – ändring av uppdateringshantering för stöd för de nya funktionerna:</span><span class="sxs-lookup"><span data-stu-id="c6c96-111">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="c6c96-112">Dynamisk gruppering</span><span class="sxs-lookup"><span data-stu-id="c6c96-112">Dynamic grouping</span></span>
    * <span data-ttu-id="c6c96-113">För-/efterskrift</span><span class="sxs-lookup"><span data-stu-id="c6c96-113">Pre-Post script</span></span>
    * <span data-ttu-id="c6c96-114">Inställning för omstart</span><span class="sxs-lookup"><span data-stu-id="c6c96-114">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c6c96-115">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c6c96-115">Az.Compute</span></span>
* <span data-ttu-id="c6c96-116">Åtgärda problem med sökvägsmatchning i Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="c6c96-116">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="c6c96-117">Uppdatera Compute-klientbibliotek till 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="c6c96-117">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="c6c96-118">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c6c96-118">Az.KeyVault</span></span>
* <span data-ttu-id="c6c96-119">Stöd för jokertecken för KeyVault-cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="c6c96-119">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c6c96-120">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c6c96-120">Az.Network</span></span>
* <span data-ttu-id="c6c96-121">Lägg till stöd för Threat Intelligence för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="c6c96-121">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="c6c96-122">Lägg till resurs för brandväggsprincip på översta nivå och anpassade regler för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="c6c96-122">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c6c96-123">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c6c96-123">Az.RecoveryServices</span></span>
* <span data-ttu-id="c6c96-124">SnapshotRetentionInDays har lagts till i Azure-principen för virtuella datorer för stöd av Instant RP</span><span class="sxs-lookup"><span data-stu-id="c6c96-124">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="c6c96-125">Pipe-stöd för avregistrering av container har lagts till</span><span class="sxs-lookup"><span data-stu-id="c6c96-125">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="c6c96-126">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c6c96-126">Az.Resources</span></span>
* <span data-ttu-id="c6c96-127">Uppdatera stöd för jokertecken för Get-AzResource och Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c6c96-127">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="c6c96-128">Uppdatera autentiseringsuppgifter som används vid allmänna anrop till ARM</span><span class="sxs-lookup"><span data-stu-id="c6c96-128">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="c6c96-129">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c6c96-129">Az.Sql</span></span>
* <span data-ttu-id="c6c96-130">Cmdlet-parametern (ExcludeDetectionType) för Hotidentifiering ändrades från DetectionType till sträng[] för att framtidssäkra den när nya DetectionTypes läggs till, och även för att stödja automatisk ifyllning.</span><span class="sxs-lookup"><span data-stu-id="c6c96-130">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c6c96-131">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c6c96-131">Az.Storage</span></span>
* <span data-ttu-id="c6c96-132">Stöd för att hämta/ange/ta bort hanteringsprincip på ett lagringskonto</span><span class="sxs-lookup"><span data-stu-id="c6c96-132">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="c6c96-133">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="c6c96-133">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="c6c96-134">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="c6c96-134">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="c6c96-135">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="c6c96-135">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="c6c96-136">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="c6c96-136">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="c6c96-137">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="c6c96-137">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="c6c96-138">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="c6c96-138">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c6c96-139">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c6c96-139">Az.Websites</span></span>
* <span data-ttu-id="c6c96-140">Åtgärda fel med ARM-mall som avbryter kloning av alla platser med 'New-AzWebApp -IncludeSourceWebAppSlots'</span><span class="sxs-lookup"><span data-stu-id="c6c96-140">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="c6c96-141">1.5.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="c6c96-141">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c6c96-142">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c6c96-142">Az.Accounts</span></span>
* <span data-ttu-id="c6c96-143">Lägg till kommandot Register-AzModule för stöd för AutoRest-genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="c6c96-143">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="c6c96-144">Uppdatera exempel för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="c6c96-144">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="c6c96-145">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c6c96-145">Az.Automation</span></span>
* <span data-ttu-id="c6c96-146">Problem med att hämta vissa månadsscheman i flera Azure Automation-cmdletar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="c6c96-146">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="c6c96-147">Åtgärda problem med att Get-AzAutomationDscNode bara returnerar de 20 översta noderna.</span><span class="sxs-lookup"><span data-stu-id="c6c96-147">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="c6c96-148">Nu returneras alla noder</span><span class="sxs-lookup"><span data-stu-id="c6c96-148">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="c6c96-149">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="c6c96-149">Az.Cdn</span></span>
* <span data-ttu-id="c6c96-150">Nya Powershell-cmdletar för att aktivera/inaktivera anpassade domän-HTTPS har lagts till och de gamla har gjorts inaktuella</span><span class="sxs-lookup"><span data-stu-id="c6c96-150">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c6c96-151">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c6c96-151">Az.Compute</span></span>
* <span data-ttu-id="c6c96-152">Lägg till stöd för jokertecken för Get-cmdletar</span><span class="sxs-lookup"><span data-stu-id="c6c96-152">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="c6c96-153">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c6c96-153">Az.DataFactory</span></span>
* <span data-ttu-id="c6c96-154">ADF .Net SDK-versionen har uppdaterats till 3.0.1</span><span class="sxs-lookup"><span data-stu-id="c6c96-154">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="c6c96-155">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="c6c96-155">Az.LogicApp</span></span>
* <span data-ttu-id="c6c96-156">Åtgärda problemet med att ListWorkflows endast hämtar den första sidan med resultat</span><span class="sxs-lookup"><span data-stu-id="c6c96-156">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c6c96-157">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c6c96-157">Az.Network</span></span>
* <span data-ttu-id="c6c96-158">Lägg till stöd för jokertecken för Network-cmdletar</span><span class="sxs-lookup"><span data-stu-id="c6c96-158">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c6c96-159">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c6c96-159">Az.RecoveryServices</span></span>
* <span data-ttu-id="c6c96-160">Stöd har lagts till för SQL Server i virtuella Azure-datorer</span><span class="sxs-lookup"><span data-stu-id="c6c96-160">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="c6c96-161">SDK-uppdatering</span><span class="sxs-lookup"><span data-stu-id="c6c96-161">SDK Update</span></span>
* <span data-ttu-id="c6c96-162">Get-ProtectableItem-incheckning i VMappContainer har tagits bort</span><span class="sxs-lookup"><span data-stu-id="c6c96-162">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="c6c96-163">Name och ServerName har lagts till som parametrar för Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="c6c96-163">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="c6c96-164">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c6c96-164">Az.Resources</span></span>
* <span data-ttu-id="c6c96-165">Lägg till parametern `-TemplateObject` i cmdletar för distribution</span><span class="sxs-lookup"><span data-stu-id="c6c96-165">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="c6c96-166">Mer information här: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="c6c96-166">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="c6c96-167">Åtgärda problem med piping av resultatet i `Get-AzResource` till `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="c6c96-167">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="c6c96-168">Mer information här: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="c6c96-168">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="c6c96-169">Åtgärda problem med ändring av JSON-datatyp när `Set-AzResource` körs</span><span class="sxs-lookup"><span data-stu-id="c6c96-169">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="c6c96-170">Mer information här: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="c6c96-170">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="c6c96-171">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c6c96-171">Az.Sql</span></span>
* <span data-ttu-id="c6c96-172">AuditingEndpointsCommunicator uppdateras.</span><span class="sxs-lookup"><span data-stu-id="c6c96-172">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="c6c96-173">Åtgärdar beteendet hos ett gränsscenario när nya diagnostikinställningar skapas.</span><span class="sxs-lookup"><span data-stu-id="c6c96-173">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c6c96-174">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c6c96-174">Az.Storage</span></span>
* <span data-ttu-id="c6c96-175">Stöd för BlockBlobStorage när Storage-konto skapas      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c6c96-175">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="c6c96-176">1.4.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="c6c96-176">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="c6c96-177">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="c6c96-177">Az.AnalysisServices</span></span>
* <span data-ttu-id="c6c96-178">Inaktuell AddAzureASAccount-cmdlet</span><span class="sxs-lookup"><span data-stu-id="c6c96-178">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="c6c96-179">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c6c96-179">Az.Automation</span></span>
* <span data-ttu-id="c6c96-180">Hjälpen för Import-AzAutomationDscNodeConfiguration har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="c6c96-180">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="c6c96-181">Konfigurationsnamnsvalidering har lagts till i cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="c6c96-181">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="c6c96-182">Förbättrad felhantering för cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="c6c96-182">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="c6c96-183">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="c6c96-183">Az.CognitiveServices</span></span>
* <span data-ttu-id="c6c96-184">CustomSubdomainName har lagts till som en ny valfri parameter för New-AzCognitiveServicesAccount, som används för att ange underdomän för resursen.</span><span class="sxs-lookup"><span data-stu-id="c6c96-184">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c6c96-185">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c6c96-185">Az.Compute</span></span>
* <span data-ttu-id="c6c96-186">Problemet med ID-parameteruppsättningar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="c6c96-186">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="c6c96-187">Get-AzVMExtension har uppdaterats så att alla installerade tillägg visas om parametern Name inte har angetts</span><span class="sxs-lookup"><span data-stu-id="c6c96-187">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="c6c96-188">Parametrarna Tag och ResourceId har lagts till i cmdleten Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="c6c96-188">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="c6c96-189">Get-AzVmssVM utan instans-ID och med InstanceView kan visa virtuella VMSS-datorer med instansvyn.</span><span class="sxs-lookup"><span data-stu-id="c6c96-189">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="c6c96-190">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c6c96-190">Az.DataLakeStore</span></span>
* <span data-ttu-id="c6c96-191">Cmdletar har lagts till för uppräkning och återställning av borttagna objekt i ADL</span><span class="sxs-lookup"><span data-stu-id="c6c96-191">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="c6c96-192">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="c6c96-192">Az.EventHub</span></span>
* <span data-ttu-id="c6c96-193">Ny boolesk egenskap SkipEmptyArchives har lagts till i Skip Empty Archives i CaptureDescription-klassen i Eventhub</span><span class="sxs-lookup"><span data-stu-id="c6c96-193">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="c6c96-194">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c6c96-194">Az.KeyVault</span></span>
* <span data-ttu-id="c6c96-195">Taggning i Set-AzKeyVaultSecret har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="c6c96-195">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="c6c96-196">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="c6c96-196">Az.LogicApp</span></span>
* <span data-ttu-id="c6c96-197">Grundläggande SKU har lagts till för Integrationskonton</span><span class="sxs-lookup"><span data-stu-id="c6c96-197">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="c6c96-198">XSLT 2.0, XSLT 3.0 och Flytande mappningstyper har lagts till</span><span class="sxs-lookup"><span data-stu-id="c6c96-198">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="c6c96-199">Nya cmdletar för integrationskontosammansättningar</span><span class="sxs-lookup"><span data-stu-id="c6c96-199">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="c6c96-200">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="c6c96-200">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="c6c96-201">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="c6c96-201">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="c6c96-202">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="c6c96-202">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="c6c96-203">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="c6c96-203">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="c6c96-204">Nya cmdletar för batchkonfiguration för integrationskonto</span><span class="sxs-lookup"><span data-stu-id="c6c96-204">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="c6c96-205">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="c6c96-205">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="c6c96-206">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="c6c96-206">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="c6c96-207">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="c6c96-207">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="c6c96-208">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="c6c96-208">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="c6c96-209">Logic App-SDK har uppdaterats till version 4.1.0</span><span class="sxs-lookup"><span data-stu-id="c6c96-209">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="c6c96-210">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="c6c96-210">Az.Monitor</span></span>
* <span data-ttu-id="c6c96-211">Hjälpen för Get-AzMetric har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="c6c96-211">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c6c96-212">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c6c96-212">Az.Network</span></span>
* <span data-ttu-id="c6c96-213">Hjälpexempel för Add-AzApplicationGatewayCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="c6c96-213">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="c6c96-214">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="c6c96-214">Az.OperationalInsights</span></span>
* <span data-ttu-id="c6c96-215">Ytterligare stöd för datakällorna New och Get ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="c6c96-215">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="c6c96-216">Ny ApplicationInsights-typ har lagts till för att ge stöd för ”Get specific” och ”Get all” för ApplicationInsights-datakällor för angiven arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="c6c96-216">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="c6c96-217">Cmdleten New-AzOperationalInsightsApplicationInsightsDataSource har lagts till för att skapa datakälla med angivna parametrar för Application Insights-resurs: subscription Id, resourceGroupName och name.</span><span class="sxs-lookup"><span data-stu-id="c6c96-217">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="c6c96-218">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c6c96-218">Az.Resources</span></span>
* <span data-ttu-id="c6c96-219">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="c6c96-219">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="c6c96-220">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="c6c96-220">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="c6c96-221">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="c6c96-221">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="c6c96-222">Fel som gör att KeyCredentials inte kan skapas upprepade gånger har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="c6c96-222">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="c6c96-223">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c6c96-223">Az.Sql</span></span>
* <span data-ttu-id="c6c96-224">Stöd för nivån SQL DB-hyperskal har lagts till</span><span class="sxs-lookup"><span data-stu-id="c6c96-224">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="c6c96-225">Ett fel har åtgärdats där återställningen kunde misslyckas på grund av onödiga inställningsegenskaper i restore-förfrågan</span><span class="sxs-lookup"><span data-stu-id="c6c96-225">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c6c96-226">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c6c96-226">Az.Websites</span></span>
* <span data-ttu-id="c6c96-227">Rätt exempel i Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="c6c96-227">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="c6c96-228">1.3.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="c6c96-228">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c6c96-229">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c6c96-229">Az.Accounts</span></span>
* <span data-ttu-id="c6c96-230">Uppdatera till den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="c6c96-230">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="c6c96-231">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="c6c96-231">Az.AnalysisServices</span></span>
<span data-ttu-id="c6c96-232">Allmän tillgänglighet för Az.AnalysisServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="c6c96-232">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c6c96-233">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c6c96-233">Az.Compute</span></span>
* <span data-ttu-id="c6c96-234">AEM-tillägg: Lägg till stöd för UltraSSD-, P60-, P70- och P80-diskar</span><span class="sxs-lookup"><span data-stu-id="c6c96-234">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="c6c96-235">Uppdatera hjälpbeskrivning för Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="c6c96-235">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="c6c96-236">Uppdatera hjälpbeskrivning och exempel för Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="c6c96-236">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c6c96-237">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c6c96-237">Az.RecoveryServices</span></span>
<span data-ttu-id="c6c96-238">Allmän tillgänglighet för Az.RecoveryServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="c6c96-238">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="c6c96-239">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c6c96-239">Az.Resources</span></span>
* <span data-ttu-id="c6c96-240">Korrigera taggar för resursgrupper</span><span class="sxs-lookup"><span data-stu-id="c6c96-240">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="c6c96-241">Mer information här: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="c6c96-241">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="c6c96-242">Åtgärda problem där `Get-AzureRmRoleAssignment` inte respekterar -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="c6c96-242">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="c6c96-243">Mer information här: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="c6c96-243">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="c6c96-244">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c6c96-244">Az.Sql</span></span>
* <span data-ttu-id="c6c96-245">Lägga till Get/Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="c6c96-245">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="c6c96-246">Åtgärda problem där ett nullref-undantag uppstår när du kör SQL-cmdletar och inte är inloggad på ett Azure-konto</span><span class="sxs-lookup"><span data-stu-id="c6c96-246">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="c6c96-247">Åtgärda nullref-undantag i Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="c6c96-247">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="c6c96-248">1.2.1 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="c6c96-248">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c6c96-249">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c6c96-249">Az.Accounts</span></span>
* <span data-ttu-id="c6c96-250">Version med rätt version av autentisering</span><span class="sxs-lookup"><span data-stu-id="c6c96-250">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="c6c96-251">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="c6c96-251">Az.AnalysisServices</span></span>
* <span data-ttu-id="c6c96-252">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="c6c96-252">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c6c96-253">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c6c96-253">Az.RecoveryServices</span></span>
* <span data-ttu-id="c6c96-254">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="c6c96-254">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="c6c96-255">1.2.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="c6c96-255">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c6c96-256">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c6c96-256">Az.Accounts</span></span>
* <span data-ttu-id="c6c96-257">Lägga till interaktiv autentisering och autentisering med användarnamn/lösenord för endast Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="c6c96-257">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="c6c96-258">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="c6c96-258">Update incorrect online help URLs</span></span>
* <span data-ttu-id="c6c96-259">Lägga till varningsmeddelande i PS Core för Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="c6c96-259">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="c6c96-260">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="c6c96-260">Az.Aks</span></span>
* <span data-ttu-id="c6c96-261">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="c6c96-261">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="c6c96-262">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c6c96-262">Az.Automation</span></span>
* <span data-ttu-id="c6c96-263">Stöd för Python 2-runbookflöden har lagts till</span><span class="sxs-lookup"><span data-stu-id="c6c96-263">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="c6c96-264">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="c6c96-264">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="c6c96-265">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="c6c96-265">Az.Cdn</span></span>
* <span data-ttu-id="c6c96-266">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="c6c96-266">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c6c96-267">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c6c96-267">Az.Compute</span></span>
* <span data-ttu-id="c6c96-268">Lägga till cmdleten Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="c6c96-268">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="c6c96-269">Lägga till TempDisk-parameter i Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="c6c96-269">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="c6c96-270">Korrigera varningsmeddelande för New-AzVM</span><span class="sxs-lookup"><span data-stu-id="c6c96-270">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="c6c96-271">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c6c96-271">Az.ContainerRegistry</span></span>
* <span data-ttu-id="c6c96-272">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="c6c96-272">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="c6c96-273">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c6c96-273">Az.DataFactory</span></span>
* <span data-ttu-id="c6c96-274">ADF .Net SDK-versionen har uppdaterats till 3.0.0</span><span class="sxs-lookup"><span data-stu-id="c6c96-274">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="c6c96-275">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c6c96-275">Az.DataLakeStore</span></span>
* <span data-ttu-id="c6c96-276">Åtgärda problem med ADLS-slutpunkt vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="c6c96-276">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="c6c96-277">Mer information här: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="c6c96-277">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="c6c96-278">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="c6c96-278">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="c6c96-279">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="c6c96-279">Az.IotHub</span></span>
* <span data-ttu-id="c6c96-280">Lägga till kodningsformat i cmdleten Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="c6c96-280">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="c6c96-281">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c6c96-281">Az.KeyVault</span></span>
* <span data-ttu-id="c6c96-282">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="c6c96-282">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c6c96-283">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c6c96-283">Az.Network</span></span>
* <span data-ttu-id="c6c96-284">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="c6c96-284">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="c6c96-285">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c6c96-285">Az.Resources</span></span>
* <span data-ttu-id="c6c96-286">Åtgärda felaktiga exempel i referensdokumentationen ”New-AzADAppCredential” och ”New-AzADSpCredential”</span><span class="sxs-lookup"><span data-stu-id="c6c96-286">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="c6c96-287">Åtgärda problem där sökvägen för parametern ”-TemplateFile” inte omvandlas innan cmdletarna för distribution i resursgruppen körs</span><span class="sxs-lookup"><span data-stu-id="c6c96-287">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="c6c96-288">Az.Resources: Korrigera dokumentationen om standardvärdet för New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="c6c96-288">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="c6c96-289">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="c6c96-289">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="c6c96-290">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="c6c96-290">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="c6c96-291">Åtgärda formateringsproblemet med objektet ”PSResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="c6c96-291">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="c6c96-292">Mer information här: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="c6c96-292">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="c6c96-293">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c6c96-293">Az.ServiceFabric</span></span>
* <span data-ttu-id="c6c96-294">Återställ när ett certifikat läggs till i en Virtual Machine Scale Sets-modell men ett undantag genereras. Detta har gjorts för att åtgärda följande fel: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="c6c96-294">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="c6c96-295">Korrigera några felmeddelanden.</span><span class="sxs-lookup"><span data-stu-id="c6c96-295">Fix some error messages.</span></span>
* <span data-ttu-id="c6c96-296">Korrigering av skapande av kluster med ARM-mall som är standard för New-AzServiceFabriCluster som inte fungerade med migrering till Az.</span><span class="sxs-lookup"><span data-stu-id="c6c96-296">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="c6c96-297">Korrigering av tilläggning av kluster/programcertifikat så att endast VM Scale Sets som motsvarar klustret läggs till genom att kontrollera ID för klustret i tillägget.</span><span class="sxs-lookup"><span data-stu-id="c6c96-297">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="c6c96-298">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="c6c96-298">Az.SignalR</span></span>
* <span data-ttu-id="c6c96-299">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="c6c96-299">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="c6c96-300">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c6c96-300">Az.Sql</span></span>
* <span data-ttu-id="c6c96-301">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="c6c96-301">Update incorrect online help URLs</span></span>
* <span data-ttu-id="c6c96-302">Uppdaterad parameterbeskrivning för LicenseType-parameter med möjliga värden</span><span class="sxs-lookup"><span data-stu-id="c6c96-302">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="c6c96-303">Korrigering för att uppdatera hanterad instansidentitet som inte fungerar när det är den enda uppdaterade egenskapen</span><span class="sxs-lookup"><span data-stu-id="c6c96-303">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="c6c96-304">Stöd för anpassad sortering på hanterad instans</span><span class="sxs-lookup"><span data-stu-id="c6c96-304">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c6c96-305">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c6c96-305">Az.Storage</span></span>
* <span data-ttu-id="c6c96-306">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="c6c96-306">Update incorrect online help URLs</span></span>
* <span data-ttu-id="c6c96-307">Tillhandahåll detaljerat felmeddelande när en användare försöker hämta/konfigurera klassisk loggning/mått på ett Premium Storage-konto eftersom Premium Storage-kontot inte har stöd för klassisk loggning/mått.</span><span class="sxs-lookup"><span data-stu-id="c6c96-307">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="c6c96-308">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="c6c96-308">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="c6c96-309">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="c6c96-309">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="c6c96-310">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="c6c96-310">Az.TrafficManager</span></span>
* <span data-ttu-id="c6c96-311">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="c6c96-311">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c6c96-312">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c6c96-312">Az.Websites</span></span>
* <span data-ttu-id="c6c96-313">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="c6c96-313">Update incorrect online help URLs</span></span>
* <span data-ttu-id="c6c96-314">Korrigerar ”New-AzWebAppSSLBinding” så att certifikatet laddas upp till rätt resursgrupp och plats om appen finns i en ASE.</span><span class="sxs-lookup"><span data-stu-id="c6c96-314">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="c6c96-315">Korrigerar ”New-AzWebAppSSLBinding” så att taggarna inte skrivs över på en bindning av ett SSL-certifikat till en app</span><span class="sxs-lookup"><span data-stu-id="c6c96-315">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="c6c96-316">1.1.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="c6c96-316">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c6c96-317">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c6c96-317">Az.Accounts</span></span>
* <span data-ttu-id="c6c96-318">Lade till omfattningen ”Lokal” till Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="c6c96-318">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c6c96-319">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c6c96-319">Az.Compute</span></span>
* <span data-ttu-id="c6c96-320">Namn är nu valfritt i ID-parametern för Restart/Start/Stop/Remove/Set-AzVM och Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="c6c96-320">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="c6c96-321">Uppdaterade beskrivningen av ID i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="c6c96-321">Updated the description of ID in help files</span></span>
* <span data-ttu-id="c6c96-322">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c6c96-322">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="c6c96-323">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c6c96-323">Az.DataLakeStore</span></span>
* <span data-ttu-id="c6c96-324">Uppdatera sdk-versionen av dataplanet till 1.1.14 för SDK-korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="c6c96-324">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="c6c96-325">Korrigerade hanteringen av negativ accesstime och modificationtime för getfilestatus och liststatus; korrigera asynkront annulleringstoken</span><span class="sxs-lookup"><span data-stu-id="c6c96-325">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="c6c96-326">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="c6c96-326">Az.EventGrid</span></span>
* <span data-ttu-id="c6c96-327">Uppdaterat för användning av API-versionen 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="c6c96-327">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="c6c96-328">Uppdaterade följande cmdletar för att stödja nytt scenario i API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="c6c96-328">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="c6c96-329">New-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="c6c96-329">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="c6c96-330">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="c6c96-330">Event Time-To-Live,</span></span>
        - <span data-ttu-id="c6c96-331">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="c6c96-331">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="c6c96-332">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="c6c96-332">Dead letter endpoint.</span></span>
    - <span data-ttu-id="c6c96-333">Update-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="c6c96-333">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="c6c96-334">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="c6c96-334">Event Time-To-Live,</span></span>
        - <span data-ttu-id="c6c96-335">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="c6c96-335">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="c6c96-336">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="c6c96-336">Dead letter endpoint.</span></span>
* <span data-ttu-id="c6c96-337">Lade till nya enum-värden (storageQueue och hybridConnection) för alternativet EndpointType i cmdletarna New-AzureRmEventGridSubscription och Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="c6c96-337">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="c6c96-338">Visa varningsmeddelanden om skapande eller uppdatering av händelseprenumerationen förväntas medföra manuell åtgärd från användaren.</span><span class="sxs-lookup"><span data-stu-id="c6c96-338">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="c6c96-339">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="c6c96-339">Az.IotHub</span></span>
* <span data-ttu-id="c6c96-340">Har uppdaterats till den senaste versionen av SDK:n lotHub</span><span class="sxs-lookup"><span data-stu-id="c6c96-340">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="c6c96-341">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="c6c96-341">Az.LogicApp</span></span>
* <span data-ttu-id="c6c96-342">Get-AzLogicApp visar en lista över alla som inte har angivet namn</span><span class="sxs-lookup"><span data-stu-id="c6c96-342">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="c6c96-343">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c6c96-343">Az.Resources</span></span>
* <span data-ttu-id="c6c96-344">Åtgärdade problem med parameteruppsättningen när parametrarna -ODataQuery och -ResourceId anges för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="c6c96-344">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="c6c96-345">Mer information här: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="c6c96-345">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="c6c96-346">Åtgärdade hantering av parametern -Custom i New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c6c96-346">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="c6c96-347">Korrigerade stavfel i New-AzDeployment-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="c6c96-347">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="c6c96-348">Gjorde parametern -MailNickname obligatorisk för New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="c6c96-348">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="c6c96-349">Mer information här: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="c6c96-349">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="c6c96-350">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="c6c96-350">Az.SignalR</span></span>
* <span data-ttu-id="c6c96-351">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c6c96-351">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="c6c96-352">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c6c96-352">Az.Sql</span></span>
* <span data-ttu-id="c6c96-353">Konverterade lagringshanteringsklientens beroende av den normala SDK-implementeringen.</span><span class="sxs-lookup"><span data-stu-id="c6c96-353">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c6c96-354">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c6c96-354">Az.Storage</span></span>
* <span data-ttu-id="c6c96-355">Angav StorageAccountName för lagringskontext som det verkliga namnet på lagringskontot när det skapas med Sas Token, OAuth eller Anonymous</span><span class="sxs-lookup"><span data-stu-id="c6c96-355">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="c6c96-356">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="c6c96-356">New-AzStorageContext</span></span>
* <span data-ttu-id="c6c96-357">Skapade Sas Token för Blob Snapshot-objekt med parametern -FullUri, åtgärdade den returnerade URI:n så att den blir URI för ögonblicksbild</span><span class="sxs-lookup"><span data-stu-id="c6c96-357">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="c6c96-358">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="c6c96-358">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c6c96-359">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c6c96-359">Az.Websites</span></span>
* <span data-ttu-id="c6c96-360">Åtgärdade en bugg i datumparsningen i Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="c6c96-360">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="c6c96-361">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c6c96-361">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="c6c96-362">1.0.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="c6c96-362">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="c6c96-363">Allmänt</span><span class="sxs-lookup"><span data-stu-id="c6c96-363">General</span></span>

- <span data-ttu-id="c6c96-364">Allmän tillgänglighet för Az-modulen</span><span class="sxs-lookup"><span data-stu-id="c6c96-364">General Availability of Az Module</span></span>
- <span data-ttu-id="c6c96-365">Onlinehjälp för varje modul</span><span class="sxs-lookup"><span data-stu-id="c6c96-365">Online help for each module</span></span>
- <span data-ttu-id="c6c96-366">Mer information och en översikt finns på [Az-informationssidan](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="c6c96-366">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="c6c96-367">Information om hur du migrerar från AzureRM finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c6c96-367">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="c6c96-368">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c6c96-368">Az.Accounts</span></span>
- <span data-ttu-id="c6c96-369">Har ändrats från Az.Profile</span><span class="sxs-lookup"><span data-stu-id="c6c96-369">Changed from Az.Profile</span></span>
- <span data-ttu-id="c6c96-370">Fasta tabellformat för profil- och kontexttyper</span><span class="sxs-lookup"><span data-stu-id="c6c96-370">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="c6c96-371">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c6c96-371">Az.ApiManagement</span></span>
- <span data-ttu-id="c6c96-372">Korrigeringar för #7002</span><span class="sxs-lookup"><span data-stu-id="c6c96-372">Fixes for #7002</span></span>
- <span data-ttu-id="c6c96-373">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c6c96-373">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="c6c96-374">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="c6c96-374">Az.Batch</span></span>
- <span data-ttu-id="c6c96-375">Lade till möjligheten att se vilken version av Azure Batch Node Agent som körs på var och en av de virtuella datorerna i en pool, via den nya egenskapen `NodeAgentInformation` på `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="c6c96-375">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="c6c96-376">Standarden `Caching` för `PSDataDisk` är nu `ReadWrite` i stället för `None`.</span><span class="sxs-lookup"><span data-stu-id="c6c96-376">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="c6c96-377">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c6c96-377">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="c6c96-378">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="c6c96-378">Az.Billing</span></span>
- <span data-ttu-id="c6c96-379">Kombinerar cmdletarna för fakturering, förbrukning och UsageAggregates. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c6c96-379">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="c6c96-380">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="c6c96-380">Az.CognitivServices</span></span>
- <span data-ttu-id="c6c96-381">Lade till kompletterare för SkuName och Typem som är tillgängliga i New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="c6c96-381">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="c6c96-382">Tog bort parameteruppsättningen GetSkusWithAccountParamSetName från Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="c6c96-382">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="c6c96-383">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="c6c96-383">Az.ContainerInstance</span></span>
- <span data-ttu-id="c6c96-384">Stöd för ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="c6c96-384">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="c6c96-385">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="c6c96-385">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="c6c96-386">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c6c96-386">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="c6c96-387">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c6c96-387">Az.DataLakeStore</span></span>
- <span data-ttu-id="c6c96-388">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c6c96-388">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="c6c96-389">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="c6c96-389">Az.Monitor</span></span>
- <span data-ttu-id="c6c96-390">Döpte om Az.Insights till Az.Monitor och andra mindre icke-bakåtkompatibla ändringar. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c6c96-390">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="c6c96-391">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c6c96-391">Az.KeyVault</span></span>
- <span data-ttu-id="c6c96-392">Tog bort den inaktuella egenskapen PurgeDisabled från utdatatyper</span><span class="sxs-lookup"><span data-stu-id="c6c96-392">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="c6c96-393">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="c6c96-393">Az.MachineLearning</span></span>
- <span data-ttu-id="c6c96-394">Inkluderade cmdletarna från modulen Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="c6c96-394">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="c6c96-395">Az.Media</span><span class="sxs-lookup"><span data-stu-id="c6c96-395">Az.Media</span></span>
- <span data-ttu-id="c6c96-396">Tog bort inaktuella -Tags-alias från New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="c6c96-396">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="c6c96-397">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c6c96-397">Az.Network</span></span>
<span data-ttu-id="c6c96-398">Stöd har lagts till för konfiguration av RewriteRuleSets i Application Gateway</span><span class="sxs-lookup"><span data-stu-id="c6c96-398">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="c6c96-399">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="c6c96-399">New cmdlets added:</span></span>
        - <span data-ttu-id="c6c96-400">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c6c96-400">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="c6c96-401">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c6c96-401">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="c6c96-402">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c6c96-402">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="c6c96-403">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c6c96-403">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="c6c96-404">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c6c96-404">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="c6c96-405">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="c6c96-405">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="c6c96-406">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="c6c96-406">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="c6c96-407">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="c6c96-407">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="c6c96-408">Cmdletar har uppdaterats med den valfria parametern -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c6c96-408">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="c6c96-409">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c6c96-409">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="c6c96-410">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c6c96-410">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="c6c96-411">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c6c96-411">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="c6c96-412">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c6c96-412">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="c6c96-413">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="c6c96-413">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="c6c96-414">New-AzureRmApplicationGatewayUrlPathMapConfig har lagt till KeyVault-stöd för Application Gateway med Identity.</span><span class="sxs-lookup"><span data-stu-id="c6c96-414">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="c6c96-415">Cmdletar har uppdaterats med den valfria parametern -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="c6c96-415">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="c6c96-416">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c6c96-416">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="c6c96-417">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c6c96-417">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="c6c96-418">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c6c96-418">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="c6c96-419">Cmdleten New-AzApplicationGateway har uppdaterats med den valfria parametern -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="c6c96-419">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="c6c96-420">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c6c96-420">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="c6c96-421">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="c6c96-421">Az.OperationalInsights</span></span>
- <span data-ttu-id="c6c96-422">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c6c96-422">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="c6c96-423">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="c6c96-423">Az.Profile</span></span>
- <span data-ttu-id="c6c96-424">Modulnamnet har ändrats till Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c6c96-424">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="c6c96-425">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c6c96-425">Az.RecoveryServices</span></span>
- <span data-ttu-id="c6c96-426">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c6c96-426">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="c6c96-427">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c6c96-427">Az.Resources</span></span>
- <span data-ttu-id="c6c96-428">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c6c96-428">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="c6c96-429">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c6c96-429">Az.ServiceFabric</span></span>
- <span data-ttu-id="c6c96-430">Stöd för specificering av certifikat efter eget namn och tumavtryck</span><span class="sxs-lookup"><span data-stu-id="c6c96-430">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="c6c96-431">Information om fler icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c6c96-431">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="c6c96-432">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="c6c96-432">Az.SIgnalR</span></span>
- <span data-ttu-id="c6c96-433">Allmän tillgänglighet för PowerShell-cmdletar för SIgnalR</span><span class="sxs-lookup"><span data-stu-id="c6c96-433">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="c6c96-434">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c6c96-434">Az.Sql</span></span>
- <span data-ttu-id="c6c96-435">Lade till de nya identifieringstyperna Data_Exfiltration och Unsafe_Action i Threat Detection-cmdletar</span><span class="sxs-lookup"><span data-stu-id="c6c96-435">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="c6c96-436">Uppdaterade dokumentationsexempel för Sql Auditing-cmdletar</span><span class="sxs-lookup"><span data-stu-id="c6c96-436">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="c6c96-437">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c6c96-437">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="c6c96-438">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c6c96-438">Az.Storage</span></span>
- <span data-ttu-id="c6c96-439">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c6c96-439">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="c6c96-440">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c6c96-440">Az.Websites</span></span>
- <span data-ttu-id="c6c96-441">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c6c96-441">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="c6c96-442">0.7.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="c6c96-442">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="c6c96-443">Allmänt</span><span class="sxs-lookup"><span data-stu-id="c6c96-443">General</span></span>

* <span data-ttu-id="c6c96-444">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="c6c96-444">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="c6c96-445">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c6c96-445">Az.Compute</span></span>

* <span data-ttu-id="c6c96-446">Lade till stöd för UltraSSD och Galleriavbildningar i de enkla parameteruppsättningarna för `New-AzVm(ss)`-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="c6c96-446">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="c6c96-447">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c6c96-447">Az.DataLakeStore</span></span>

* <span data-ttu-id="c6c96-448">Åtgärdade avslutande snedstreck i domänen för adls-konto</span><span class="sxs-lookup"><span data-stu-id="c6c96-448">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="c6c96-449">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="c6c96-449">Az.FrontDoor</span></span>

* <span data-ttu-id="c6c96-450">Brutna länkar korrigerades</span><span class="sxs-lookup"><span data-stu-id="c6c96-450">Fixed some broken links</span></span>
    - <span data-ttu-id="c6c96-451">I artiklarna New-AzureRmFrontDoor och Set-AzureRmFrontDoor artiklar korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="c6c96-451">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="c6c96-452">I artikeln New-AzureRmFrontDoorManagedRuleObject korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="c6c96-452">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="c6c96-453">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c6c96-453">Az.RecoveryServices</span></span>

* <span data-ttu-id="c6c96-454">Lade till valideringar på klientsidan för Azure-filresurs med återställningsåtgärder.</span><span class="sxs-lookup"><span data-stu-id="c6c96-454">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="c6c96-455">Gjorde storageAccountName och storageAccountResourceGroupName valfritt för afs-återställning.</span><span class="sxs-lookup"><span data-stu-id="c6c96-455">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="c6c96-456">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c6c96-456">Az.Resources</span></span>

* <span data-ttu-id="c6c96-457">Korrigering för https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="c6c96-457">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="c6c96-458">Uppdaterade Get-AzureRmRoleAssignment så att prenumerationsomfattningen används om den anges vid begäran om klassiska administratörer.</span><span class="sxs-lookup"><span data-stu-id="c6c96-458">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="c6c96-459">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c6c96-459">Az.Sql</span></span>

* <span data-ttu-id="c6c96-460">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="c6c96-460">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="c6c96-461">Korrigerade ett problem med Get-AzureRmSqlDatabaseVulnerabilityAssessment med DotNet-kärna</span><span class="sxs-lookup"><span data-stu-id="c6c96-461">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="c6c96-462">Ändrade dokumentationen för hjälpmeddelanden som rör SQL Auditing-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="c6c96-462">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="c6c96-463">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c6c96-463">Az.Storage</span></span>

* <span data-ttu-id="c6c96-464">Lade till -EnableHierarchicalNamespace i New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c6c96-464">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="c6c96-465">Åtgärdade problemet med att cmdleten Copy File inte kunde återanvända källkontexten på målet om inte -DestContext angetts</span><span class="sxs-lookup"><span data-stu-id="c6c96-465">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="c6c96-466">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="c6c96-466">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="c6c96-467">Stöd för statisk webbplatskonfiguration</span><span class="sxs-lookup"><span data-stu-id="c6c96-467">Support Static Website configuration</span></span>
    - <span data-ttu-id="c6c96-468">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="c6c96-468">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="c6c96-469">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="c6c96-469">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="c6c96-470">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c6c96-470">Az.Websites</span></span>

* <span data-ttu-id="c6c96-471">Set-AzureRmWebApp och Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c6c96-471">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="c6c96-472">Ny parameter (-AzureStoragePath) har lagts till för att ange att Azure Storage-sökvägar ska monteras i containerappar i Windows och Linux.</span><span class="sxs-lookup"><span data-stu-id="c6c96-472">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="c6c96-473">Använder utdata från den nya cmdleten New-AzureRmWebAppAzureStoragePath som en parameter för att ange sökvägar för Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="c6c96-473">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="c6c96-474">0.6.1 – november 2018</span><span class="sxs-lookup"><span data-stu-id="c6c96-474">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="c6c96-475">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c6c96-475">Az.ApiManagement</span></span>
* <span data-ttu-id="c6c96-476">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="c6c96-476">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="c6c96-477">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c6c96-477">Az.Automation</span></span>
* <span data-ttu-id="c6c96-478">Swagger baserade Azure Automation-cmdletar</span><span class="sxs-lookup"><span data-stu-id="c6c96-478">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="c6c96-479">Cmdletar för Uppdateringshantering har lagts till</span><span class="sxs-lookup"><span data-stu-id="c6c96-479">Added Update Management cmdlets</span></span>
* <span data-ttu-id="c6c96-480">Cmdletar för källkontroll har lagts till</span><span class="sxs-lookup"><span data-stu-id="c6c96-480">Added Source Control cmdlets</span></span>
* <span data-ttu-id="c6c96-481">Remove-AzureRmAutomationHybridWorkerGroup-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="c6c96-481">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="c6c96-482">Kommandot för DSC-registreringsnod har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="c6c96-482">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="c6c96-483">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c6c96-483">Az.Compute</span></span>
* <span data-ttu-id="c6c96-484">Problem med SystemAssigned-identitet har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="c6c96-484">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="c6c96-485">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="c6c96-485">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="c6c96-486">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="c6c96-486">Az.ContainerInstance</span></span>
* <span data-ttu-id="c6c96-487">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="c6c96-487">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="c6c96-488">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="c6c96-488">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="c6c96-489">uppdatera exempelbeskrivningen för marketplace-cmdletar</span><span class="sxs-lookup"><span data-stu-id="c6c96-489">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="c6c96-490">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c6c96-490">Az.Network</span></span>
* <span data-ttu-id="c6c96-491">Cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomErreller Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="c6c96-491">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="c6c96-492">ICMP tillbaka till stöd för Azure Firewall-nätverksprotokoll har lagts till</span><span class="sxs-lookup"><span data-stu-id="c6c96-492">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="c6c96-493">Uppdatera cmdlet Test-AzureRmNetworkWatcherConnectivity, lägga till verifiering av mål-id, adress och port.</span><span class="sxs-lookup"><span data-stu-id="c6c96-493">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="c6c96-494">Åtgärda problem med minnesanvändning i VirtualNetwork-karta</span><span class="sxs-lookup"><span data-stu-id="c6c96-494">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="c6c96-495">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="c6c96-495">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="c6c96-496">Åtgärda för att ändra principen för en skyddad fildelning.</span><span class="sxs-lookup"><span data-stu-id="c6c96-496">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="c6c96-497">Tidszonsprincipen har konverterats till versaler.</span><span class="sxs-lookup"><span data-stu-id="c6c96-497">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="c6c96-498">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="c6c96-498">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="c6c96-499">Exempel i New-AzureRmRecoveryServicesAsrProtectableItem har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="c6c96-499">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="c6c96-500">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="c6c96-500">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="c6c96-501">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="c6c96-501">Az.Relay</span></span>
* <span data-ttu-id="c6c96-502">Valfri parameter -KeyValue till New-AzureRmRelayKey cmdlet har lagts till, vilket gör det möjligt för användare att tillhandahålla KeyValue.</span><span class="sxs-lookup"><span data-stu-id="c6c96-502">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="c6c96-503">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c6c96-503">Az.Resources</span></span>
* <span data-ttu-id="c6c96-504">Uppdatera hjälpdokumentation för resursidentitet kopplad till parametrar i `New-AzureRmPolicyAssignment` och `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="c6c96-504">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="c6c96-505">Lägg till ett exempel för New-AzureRmPolicyDefinition som använder -Metadata</span><span class="sxs-lookup"><span data-stu-id="c6c96-505">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="c6c96-506">Korrigera så att skiftläge behålls i taggnycklar i NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="c6c96-506">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="c6c96-507">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c6c96-507">Az.ServiceFabric</span></span>
* <span data-ttu-id="c6c96-508">Lägg till utfasningsmeddelanden för kommande icke-kompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="c6c96-508">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="c6c96-509">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c6c96-509">Az.Sql</span></span>
* <span data-ttu-id="c6c96-510">Nya cmdletar för CRUD-åtgärder på Azure Sql Database-hanterad instans och Azure Sql-hanterad databas</span><span class="sxs-lookup"><span data-stu-id="c6c96-510">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="c6c96-511">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="c6c96-511">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="c6c96-512">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="c6c96-512">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="c6c96-513">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="c6c96-513">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="c6c96-514">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="c6c96-514">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="c6c96-515">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="c6c96-515">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="c6c96-516">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="c6c96-516">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="c6c96-517">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="c6c96-517">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="c6c96-518">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="c6c96-518">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="c6c96-519">Hantering av utökad granskningsprincip på en server eller en databas har aktiverats.</span><span class="sxs-lookup"><span data-stu-id="c6c96-519">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="c6c96-520">Ny parameter (PredicateExpression) har lagts till för att aktivera filtrering av granskningsloggar.</span><span class="sxs-lookup"><span data-stu-id="c6c96-520">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="c6c96-521">Cmdletar har ändrats så att de använder SQL-klienter i stället för äldre klienter.</span><span class="sxs-lookup"><span data-stu-id="c6c96-521">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="c6c96-522">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="c6c96-522">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="c6c96-523">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="c6c96-523">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="c6c96-524">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="c6c96-524">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="c6c96-525">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="c6c96-525">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="c6c96-526">Problem med att använda Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings med lagringskontots namnparameter har korrigerats</span><span class="sxs-lookup"><span data-stu-id="c6c96-526">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="c6c96-527">0.5.0 – november 2018</span><span class="sxs-lookup"><span data-stu-id="c6c96-527">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="c6c96-528">Allmänt</span><span class="sxs-lookup"><span data-stu-id="c6c96-528">General</span></span>
* <span data-ttu-id="c6c96-529">Lade till resurskompletterare till många kärn-cmdletar – dessa gör att du kan stega genom befintliga resursnamn med TABB vid interaktiva anrop till cmdletar</span><span class="sxs-lookup"><span data-stu-id="c6c96-529">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="c6c96-530">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="c6c96-530">Az.Profile</span></span>
* <span data-ttu-id="c6c96-531">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="c6c96-531">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="c6c96-532">Bytte namn på parametern TenantId i cmdleten Connect-AzAccount till Tenant och lade till ett alias för TenantId</span><span class="sxs-lookup"><span data-stu-id="c6c96-532">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="c6c96-533">Uppdaterade TenantId-beskrivningen för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="c6c96-533">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="c6c96-534">Åtgärda felmeddelande för misslyckad inloggning när du tillhandahåller klientdomän</span><span class="sxs-lookup"><span data-stu-id="c6c96-534">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="c6c96-535">Åtgärda problem med att kontextnamn hamnar i konflikt för konton utan prenumerationer i klientorganisationen</span><span class="sxs-lookup"><span data-stu-id="c6c96-535">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="c6c96-536">Åtgärda problem med DataLake-slutpunkter vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="c6c96-536">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="c6c96-537">Åtgärdade problem med att Disconnect-AzAccount kastades om den inte anslöts</span><span class="sxs-lookup"><span data-stu-id="c6c96-537">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="c6c96-538">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="c6c96-538">Az.CognitiveServices</span></span>
* <span data-ttu-id="c6c96-539">Lade till åtgärden Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="c6c96-539">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c6c96-540">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c6c96-540">Az.Compute</span></span>
* <span data-ttu-id="c6c96-541">Lade till cmdletarna Add-AzVmssVMDataDisk och Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="c6c96-541">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="c6c96-542">Get-AzVMImage visar AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="c6c96-542">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="c6c96-543">Åtgärdade att värdena för alternativen SetAzVMChefExtension -BootstrapOptions och -JsonAttribute inte angavs i json-format.</span><span class="sxs-lookup"><span data-stu-id="c6c96-543">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="c6c96-544">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c6c96-544">Az.DataLakeStore</span></span>
* <span data-ttu-id="c6c96-545">Uppdatera DataLake-paketet till 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="c6c96-545">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="c6c96-546">Lägg till standardsamtidighet för flertrådade åtgärder.</span><span class="sxs-lookup"><span data-stu-id="c6c96-546">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="c6c96-547">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="c6c96-547">Az.Insights</span></span>
* <span data-ttu-id="c6c96-548">Åtgärdade problem #7267 (autoskalningsområde)</span><span class="sxs-lookup"><span data-stu-id="c6c96-548">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="c6c96-549">Problem med att uppräknade parametrar inte ställdes in ordentligt när du skapade en ny autoskalningsregel (de ställdes alltid in med standardvärdet).</span><span class="sxs-lookup"><span data-stu-id="c6c96-549">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="c6c96-550">Åtgärdade problem #7513 [Insights] Set-AzDiagnosticSetting kräver uttrycklig specifikation av kategorier när inställningar skapas</span><span class="sxs-lookup"><span data-stu-id="c6c96-550">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="c6c96-551">Nu kräver inte cmdleten uttrycklig anvisning av kategorierna för att aktiveras under skapande, d.v.s. den fungerar enligt beskrivning</span><span class="sxs-lookup"><span data-stu-id="c6c96-551">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c6c96-552">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c6c96-552">Az.Network</span></span>
* <span data-ttu-id="c6c96-553">PeeringType ändrades till en obligatorisk parameter för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="c6c96-553">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="c6c96-554">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="c6c96-554">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="c6c96-555">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="c6c96-555">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="c6c96-556">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="c6c96-556">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="c6c96-557">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="c6c96-557">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="c6c96-558">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="c6c96-558">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="c6c96-559">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="c6c96-559">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="c6c96-560">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="c6c96-560">Az.PolicyInsights</span></span>
* <span data-ttu-id="c6c96-561">Cmdletar för principreparation har lagts till</span><span class="sxs-lookup"><span data-stu-id="c6c96-561">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="c6c96-562">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c6c96-562">Az.Resources</span></span>
* <span data-ttu-id="c6c96-563">Korrigering för https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="c6c96-563">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="c6c96-564">Tillåt att resurser listas med parametern -ResourceId för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="c6c96-564">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="c6c96-565">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c6c96-565">Az.ServiceBus</span></span>
* <span data-ttu-id="c6c96-566">Skrivskyddad MigrationState-egenskap har lagts till i PSServiceBusMigrationConfigurationAttributes, som hjälper till att hålla koll på migreringstillståndet.</span><span class="sxs-lookup"><span data-stu-id="c6c96-566">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="c6c96-567">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c6c96-567">Az.ServiceFabric</span></span>
* <span data-ttu-id="c6c96-568">Åtgärda att lägga till certifikat till Linux-Vmss.</span><span class="sxs-lookup"><span data-stu-id="c6c96-568">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="c6c96-569">Åtgärdade Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="c6c96-569">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="c6c96-570">Använd rätt tumavtryck från nya certifikat (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="c6c96-570">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="c6c96-571">Visa undantag korrekt (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="c6c96-571">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="c6c96-572">Åtgärdade Update-AzServiceFabricDurability så att klusterkonfigurationen uppdateras innan Vmss-åtgärden CreateOrUpdate påbörjas.</span><span class="sxs-lookup"><span data-stu-id="c6c96-572">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="c6c96-573">0.4.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="c6c96-573">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="c6c96-574">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="c6c96-574">Az.Profile</span></span>
* <span data-ttu-id="c6c96-575">Åtgärdade problemet med Get-AzSubscription i CloudShell</span><span class="sxs-lookup"><span data-stu-id="c6c96-575">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="c6c96-576">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="c6c96-576">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c6c96-577">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c6c96-577">Az.Compute</span></span>
* <span data-ttu-id="c6c96-578">Nya storlekar lades till i listan över godkända VM-storlekar för vilka accelererat nätverk kommer att aktiveras vid användning av den enkla parameteruppsättningen för New-AzVm</span><span class="sxs-lookup"><span data-stu-id="c6c96-578">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="c6c96-579">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="c6c96-579">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="c6c96-580">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c6c96-580">Az.DataLakeStore</span></span>
* <span data-ttu-id="c6c96-581">Lägger till stöd för virtuella nätverksregler</span><span class="sxs-lookup"><span data-stu-id="c6c96-581">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="c6c96-582">Get-AzDataLakeStoreVirtualNetworkRule: Hämtar eller listar regel för virtuellt Azure Data Lake Store-nätverk.</span><span class="sxs-lookup"><span data-stu-id="c6c96-582">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="c6c96-583">Add-AzDataLakeStoreVirtualNetworkRule: Lägger till en regel för det virtuella nätverket till det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="c6c96-583">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="c6c96-584">Set-AzDataLakeStoreVirtualNetworkRule: Ändrar den angivna regeln för det virtuella nätverket i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="c6c96-584">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="c6c96-585">Remove-AzDataLakeStoreVirtualNetworkRule: Tar bort en regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c6c96-585">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c6c96-586">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c6c96-586">Az.Network</span></span>
* <span data-ttu-id="c6c96-587">Skicka protokollvärdet till serverdelen för att uppdatera cmdleten Test-AzNetworkWatcherConnectivity.</span><span class="sxs-lookup"><span data-stu-id="c6c96-587">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="c6c96-588">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="c6c96-588">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="c6c96-589">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c6c96-589">Az.Resources</span></span>
* <span data-ttu-id="c6c96-590">Åtgärdade problem där Get-AzRoleDefinition genererar ett oläsligt undantag (när standardprofilen inte innehåller någon prenumeration och ingen omfattning har angetts) genom att lägga till ett beskrivande undantag i scenariot.</span><span class="sxs-lookup"><span data-stu-id="c6c96-590">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="c6c96-591">Ställ in ”RoleDefinitionNameParameterSet” som standardparameteruppsättning.</span><span class="sxs-lookup"><span data-stu-id="c6c96-591">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="c6c96-592">0.3.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="c6c96-592">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="c6c96-593">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="c6c96-593">Azure.Storage</span></span>
* <span data-ttu-id="c6c96-594">Åtgärda fel där Kopiera blob/fil inte kopierar metadata när målplatsen har ett problem med metadata</span><span class="sxs-lookup"><span data-stu-id="c6c96-594">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="c6c96-595">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="c6c96-595">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="c6c96-596">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="c6c96-596">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="c6c96-597">Stöd för att hämta användningsinformation om en Storage-resurs för en specifik plats och för att lägga till ett varningsmeddelande för att hämta användningsinformation om en global Storage-resurs är inaktuellt.</span><span class="sxs-lookup"><span data-stu-id="c6c96-597">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="c6c96-598">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="c6c96-598">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="c6c96-599">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="c6c96-599">Az.CognitiveServices</span></span>
* <span data-ttu-id="c6c96-600">Stöd för Get-AzCognitiveServicesAccountSkus utan ett befintligt konto.</span><span class="sxs-lookup"><span data-stu-id="c6c96-600">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c6c96-601">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c6c96-601">Az.Compute</span></span>
* <span data-ttu-id="c6c96-602">Åtgärdade fel där Get-AzVM -ResourceGroupName <rg> returnerar fler än 50 resultat om det behövs</span><span class="sxs-lookup"><span data-stu-id="c6c96-602">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="c6c96-603">Lade till ett exempel för SimpleParameterSet i hjälpen för cmdleten New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="c6c96-603">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="c6c96-604">Ett stavfel i förloppsmeddelandet för Azure Disk Encryption har korrigerats</span><span class="sxs-lookup"><span data-stu-id="c6c96-604">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="c6c96-605">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="c6c96-605">Az.DataFactoryV2</span></span>
* <span data-ttu-id="c6c96-606">ADF .Net SDK-versionen har uppdaterats till 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="c6c96-606">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c6c96-607">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c6c96-607">Az.Network</span></span>
* <span data-ttu-id="c6c96-608">Funktionalitet för NetworkProfile har lagts till.</span><span class="sxs-lookup"><span data-stu-id="c6c96-608">Added NetworkProfile functionality.</span></span> <span data-ttu-id="c6c96-609">nya cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="c6c96-609">new cmdlets added</span></span>
    - <span data-ttu-id="c6c96-610">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c6c96-610">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="c6c96-611">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c6c96-611">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="c6c96-612">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c6c96-612">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="c6c96-613">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c6c96-613">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="c6c96-614">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="c6c96-614">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="c6c96-615">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="c6c96-615">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="c6c96-616">Länk för tjänstassociering på modell för undernät har lagts till</span><span class="sxs-lookup"><span data-stu-id="c6c96-616">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="c6c96-617">Cmdletarna New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap och Remove-AzVirtualNetworkTap har lagts till</span><span class="sxs-lookup"><span data-stu-id="c6c96-617">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="c6c96-618">Cmdletarna Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig och Remove-AzNEtworkInterfaceTapConfig har lagts till</span><span class="sxs-lookup"><span data-stu-id="c6c96-618">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="c6c96-619">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="c6c96-619">Az.RedisCache</span></span>
* <span data-ttu-id="c6c96-620">Tillåt att alla strängar används som storleksparametrar framöver.</span><span class="sxs-lookup"><span data-stu-id="c6c96-620">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="c6c96-621">Lägg till P5 i popup-fönstret PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="c6c96-621">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="c6c96-622">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c6c96-622">Az.Resources</span></span>
* <span data-ttu-id="c6c96-623">Parametern -Mode som saknades i Set-AzPolicyDefinition har lagts till</span><span class="sxs-lookup"><span data-stu-id="c6c96-623">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="c6c96-624">Åtgärdade buggen för cmdleten Get-AzProviderOperation för åtgärder med ursprung som innehåller användare</span><span class="sxs-lookup"><span data-stu-id="c6c96-624">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="c6c96-625">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c6c96-625">Az.Sql</span></span>
* <span data-ttu-id="c6c96-626">Ett problem där vissa cmdletar för säkerhetskopiering inte kunde identifiera den aktuella azure-prenumerationen har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="c6c96-626">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c6c96-627">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c6c96-627">Az.Websites</span></span>
* <span data-ttu-id="c6c96-628">Ny cmdlet: Get-AzWebAppContainerContinuousDeploymentUrl – Hämtar webhook-URL:en för kontinuerlig distribution av container</span><span class="sxs-lookup"><span data-stu-id="c6c96-628">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="c6c96-629">Nya cmdletar: New-AzWebAppContainerPSSession och Enter-WebAppContainerPSSession – Startar en PowerShell-fjärrsession i en containerapp för windows</span><span class="sxs-lookup"><span data-stu-id="c6c96-629">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="c6c96-630">0.2.0 – september 2018</span><span class="sxs-lookup"><span data-stu-id="c6c96-630">0.2.0 - September 2018</span></span>
 <span data-ttu-id="c6c96-631">Första versionen</span><span class="sxs-lookup"><span data-stu-id="c6c96-631">Initial Release</span></span>