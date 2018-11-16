---
title: Ändringslogg för Azure PowerShell | Microsoft Docs
description: Det här är en historik över de ändringar som gjorts i den senaste versionen av Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 08/28/2018
ms.openlocfilehash: 8a7b184ed06eb078956229fa67d02840014e3aaf
ms.sourcegitcommit: 4afdba3cd7e1d348876ce59f3503fdcd258f79ab
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/15/2018
ms.locfileid: "51574540"
---
# <a name="release-notes"></a><span data-ttu-id="90e55-103">Viktig information</span><span class="sxs-lookup"><span data-stu-id="90e55-103">Release notes</span></span>

<span data-ttu-id="90e55-104">Det här är en lista över ändringar som har gjorts i Azure PowerShell i den här versionen.</span><span class="sxs-lookup"><span data-stu-id="90e55-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="6120---november-2018"></a><span data-ttu-id="90e55-105">6.12.0 – november 2018</span><span class="sxs-lookup"><span data-stu-id="90e55-105">6.12.0 - November 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="90e55-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="90e55-106">AzureRM.Profile</span></span>
* <span data-ttu-id="90e55-107">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="90e55-107">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="90e55-108">Byt namn på parametern TenantId i cmdleten Connect-AzureRmAccount till Tenant och lägg till ett alias för TenantId</span><span class="sxs-lookup"><span data-stu-id="90e55-108">Rename param TenantId in cmdlet Connect-AzureRmAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="90e55-109">Uppdatera TenantId-beskrivning för Connect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="90e55-109">Updated TenantId description for Connect-AzureRmAccount</span></span>
* <span data-ttu-id="90e55-110">Åtgärda felmeddelande för misslyckad inloggning när du tillhandahåller klientdomän</span><span class="sxs-lookup"><span data-stu-id="90e55-110">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="90e55-111">Åtgärda problem med att kontextnamn hamnar i konflikt för konton utan prenumerationer i klientorganisationen</span><span class="sxs-lookup"><span data-stu-id="90e55-111">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="90e55-112">Åtgärda problem med DataLake-slutpunkter vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="90e55-112">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="90e55-113">Åtgärda problem med att Disconnect-AzureRmAccount kastades om den inte anslöts</span><span class="sxs-lookup"><span data-stu-id="90e55-113">Fix issue where 'Disconnect-AzureRmAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azurermautomation"></a><span data-ttu-id="90e55-114">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="90e55-114">AzureRM.Automation</span></span>
* <span data-ttu-id="90e55-115">Bytte namn på cmdlet DLL-filnamnet till Microsoft.Azure.Commands.Automation.dll</span><span class="sxs-lookup"><span data-stu-id="90e55-115">Renamed cmdlet DLL filename to Microsoft.Azure.Commands.Automation.dll</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="90e55-116">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="90e55-116">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="90e55-117">Lägg till åtgärden Get-AzureRmCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="90e55-117">Add Get-AzureRmCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="90e55-118">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="90e55-118">AzureRM.Compute</span></span>
* <span data-ttu-id="90e55-119">Lägg till cmdletarna Add-AzureRmVmssVMDataDisk och Remove-AzureRmVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="90e55-119">Add Add-AzureRmVmssVMDataDisk and Remove-AzureRmVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="90e55-120">Get-AzureRmVMImage visar AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="90e55-120">Get-AzureRmVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="90e55-121">Åtgärdade att alternativvärden för SetAzureRmVMChefExtension -BootstrapOptions och -JsonAttribute inte ställdes in som json-format.</span><span class="sxs-lookup"><span data-stu-id="90e55-121">Fixed SetAzureRmVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="90e55-122">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="90e55-122">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="90e55-123">Uppdatera DataLake-paketet till 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="90e55-123">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="90e55-124">Lägg till standardsamtidighet för flertrådade åtgärder.</span><span class="sxs-lookup"><span data-stu-id="90e55-124">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="90e55-125">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="90e55-125">AzureRM.Insights</span></span>
* <span data-ttu-id="90e55-126">Åtgärdade problem #7267 (autoskalningsområde)</span><span class="sxs-lookup"><span data-stu-id="90e55-126">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="90e55-127">Problem med att uppräknade parametrar inte ställdes in ordentligt när du skapade en ny autoskalningsregel (de ställdes alltid in med standardvärdet).</span><span class="sxs-lookup"><span data-stu-id="90e55-127">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="90e55-128">Åtgärdade problem #7513 [Insights] Set-AzureRMDiagnosticSetting kräver uttrycklig specifikation av kategorier när inställningar skapas</span><span class="sxs-lookup"><span data-stu-id="90e55-128">Fixed issue #7513 [Insights] Set-AzureRMDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="90e55-129">Nu kräver inte cmdleten uttrycklig anvisning av kategorierna för att aktiveras under skapande, d.v.s. den fungerar enligt beskrivning</span><span class="sxs-lookup"><span data-stu-id="90e55-129">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="90e55-130">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="90e55-130">AzureRM.Network</span></span>
* <span data-ttu-id="90e55-131">PeeringType ändrades till en obligatorisk parameter för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="90e55-131">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="90e55-132">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="90e55-132">Get-AzureRmExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="90e55-133">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="90e55-133">Get-AzureRmExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="90e55-134">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="90e55-134">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="90e55-135">Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="90e55-135">Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="90e55-136">Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="90e55-136">Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="90e55-137">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="90e55-137">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="90e55-138">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="90e55-138">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="90e55-139">Cmdletar för principreparation har lagts till</span><span class="sxs-lookup"><span data-stu-id="90e55-139">Added policy remediation cmdlets</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="90e55-140">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="90e55-140">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="90e55-141">Stöd har lagts till för Azure-filresurser i återställningstjänster.</span><span class="sxs-lookup"><span data-stu-id="90e55-141">Added support for azure file shares in recovery services.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="90e55-142">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="90e55-142">AzureRM.Resources</span></span>
* <span data-ttu-id="90e55-143">Korrigering för https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="90e55-143">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="90e55-144">Tillåt att resurser listas med parametern -ResourceId för Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="90e55-144">Allow listing resources using the '-ResourceId' parameter for 'Get-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="90e55-145">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="90e55-145">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="90e55-146">Skrivskyddad MigrationState-egenskap har lagts till i PSServiceBusMigrationConfigurationAttributes, som hjälper till att hålla koll på migreringstillståndet.</span><span class="sxs-lookup"><span data-stu-id="90e55-146">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="90e55-147">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="90e55-147">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="90e55-148">Åtgärda att lägga till certifikat till Linux-Vmss.</span><span class="sxs-lookup"><span data-stu-id="90e55-148">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="90e55-149">Åtgärda Add-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="90e55-149">Fix 'Add-AzureRmServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="90e55-150">Använd rätt tumavtryck från nya certifikat (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="90e55-150">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="90e55-151">Visa undantag korrekt (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="90e55-151">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="90e55-152">Åtgärda Update-AzureRmServiceFabricDurability så att klusterkonfigurationen uppdateras innan Vmss-åtgärden CreateOrUpdate påbörjas.</span><span class="sxs-lookup"><span data-stu-id="90e55-152">Fix 'Update-AzureRmServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="6110---october-2018"></a><span data-ttu-id="90e55-153">6.11.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="90e55-153">6.11.0 - October 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="90e55-154">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="90e55-154">AzureRM.Profile</span></span>
* <span data-ttu-id="90e55-155">Åtgärda problemet med Get-AzureRmSubscription i CloudShell</span><span class="sxs-lookup"><span data-stu-id="90e55-155">Fix issue with Get-AzureRmSubscription in CloudShell</span></span>
* <span data-ttu-id="90e55-156">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="90e55-156">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="90e55-157">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="90e55-157">AzureRM.Backup</span></span>
* <span data-ttu-id="90e55-158">Inaktuella Azure Backup-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="90e55-158">Deprecated Azure Backup cmdlets.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="90e55-159">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="90e55-159">AzureRM.Compute</span></span>
* <span data-ttu-id="90e55-160">Nya storlekar har lagts till i listan över godkända VM-storlekar för vilka accelererat nätverk kommer att aktiveras vid användning av den enkla parameteruppsättningen för ”New-AzureRmVm”</span><span class="sxs-lookup"><span data-stu-id="90e55-160">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzureRmVm'</span></span>
* <span data-ttu-id="90e55-161">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="90e55-161">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="90e55-162">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="90e55-162">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="90e55-163">Lägger till stöd för virtuella nätverksregler</span><span class="sxs-lookup"><span data-stu-id="90e55-163">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="90e55-164">Get-AzureRmDataLakeStoreVirtualNetworkRule: Hämtar eller lägger till regel för virtuellt nätverk i Azure Data Lake Store i en lista.</span><span class="sxs-lookup"><span data-stu-id="90e55-164">Get-AzureRmDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="90e55-165">Add-AzureRmDataLakeStoreVirtualNetworkRule: Lägger till en virtuell nätverksregel till det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="90e55-165">Add-AzureRmDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="90e55-166">Set-AzureRmDataLakeStoreVirtualNetworkRule: Ändrar den angivna virtuella nätverksregeln i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="90e55-166">Set-AzureRmDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="90e55-167">Remove-AzureRmDataLakeStoreVirtualNetworkRule: Tar bort en regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="90e55-167">Remove-AzureRmDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="90e55-168">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="90e55-168">AzureRM.Network</span></span>
* <span data-ttu-id="90e55-169">Skicka protokollvärdet till serverdelen för att uppdatera cmdleten Test-AzureRmNetworkWatcherConnectivity.</span><span class="sxs-lookup"><span data-stu-id="90e55-169">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="90e55-170">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="90e55-170">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="90e55-171">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="90e55-171">AzureRM.Resources</span></span>
* <span data-ttu-id="90e55-172">Åtgärda problem där Get-AzureRMRoleDefinition genererar ett oläsligt undantag (när standardprofilen inte innehåller någon prenumeration och ingen omfattning har angetts) genom att lägga till ett beskrivande undantag i scenariot.</span><span class="sxs-lookup"><span data-stu-id="90e55-172">Fix isssue where Get-AzureRMRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="90e55-173">Ställ in ”RoleDefinitionNameParameterSet” som standardparameteruppsättning.</span><span class="sxs-lookup"><span data-stu-id="90e55-173">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="6100---october-2018"></a><span data-ttu-id="90e55-174">6.10.0 – Oktober 2018</span><span class="sxs-lookup"><span data-stu-id="90e55-174">6.10.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="90e55-175">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="90e55-175">Azure.Storage</span></span>
* <span data-ttu-id="90e55-176">Åtgärda fel där Kopiera blob/fil inte kopierar metadata när målplatsen har ett problem med metadata</span><span class="sxs-lookup"><span data-stu-id="90e55-176">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="90e55-177">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="90e55-177">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="90e55-178">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="90e55-178">Start-AzureStorageFileCopy</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="90e55-179">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="90e55-179">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="90e55-180">Stöd för Get-AzureRmCognitiveServicesAccountSkus utan ett befintligt konto.</span><span class="sxs-lookup"><span data-stu-id="90e55-180">Support Get-AzureRmCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="90e55-181">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="90e55-181">AzureRM.Compute</span></span>
* <span data-ttu-id="90e55-182">Åtgärda fel där Get-AzureRmVM -ResourceGroupName <rg> returnerar fler än 50 resultat om det behövs</span><span class="sxs-lookup"><span data-stu-id="90e55-182">Fix Get-AzureRmVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="90e55-183">Ett exempel för ”SimpleParameterSet” har lagts till i hjälpen för cmdleten New-AzureRmVmss.</span><span class="sxs-lookup"><span data-stu-id="90e55-183">Added an example of the 'SimpleParameterSet' to New-AzureRmVmss cmdlet help.</span></span>
* <span data-ttu-id="90e55-184">Ett stavfel i förloppsmeddelandet för Azure Disk Encryption har korrigerats</span><span class="sxs-lookup"><span data-stu-id="90e55-184">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="90e55-185">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="90e55-185">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="90e55-186">ADF .Net SDK-versionen har uppdaterats till 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="90e55-186">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="90e55-187">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="90e55-187">AzureRM.Network</span></span>
* <span data-ttu-id="90e55-188">Funktionalitet för NetworkProfile har lagts till.</span><span class="sxs-lookup"><span data-stu-id="90e55-188">Added NetworkProfile functionality.</span></span> <span data-ttu-id="90e55-189">nya cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="90e55-189">new cmdlets added</span></span>
    - <span data-ttu-id="90e55-190">Get-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="90e55-190">Get-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="90e55-191">New-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="90e55-191">New-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="90e55-192">Remove-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="90e55-192">Remove-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="90e55-193">Set-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="90e55-193">Set-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="90e55-194">New-AzureRMContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="90e55-194">New-AzureRMContainerNicConfig</span></span>
    - <span data-ttu-id="90e55-195">New-AzureRmContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="90e55-195">New-AzureRmContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="90e55-196">Länk för tjänstassociering på modell för undernät har lagts till</span><span class="sxs-lookup"><span data-stu-id="90e55-196">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="90e55-197">De nya cmdletarna New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap och Remove-AzureRmVirtualNetworkTap har lagts till</span><span class="sxs-lookup"><span data-stu-id="90e55-197">Added cmdlet New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap</span></span>
* <span data-ttu-id="90e55-198">Cmdletarna Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig och Remove-AzureRmNEtworkInterfaceTapConfig har lagts till</span><span class="sxs-lookup"><span data-stu-id="90e55-198">Added cmdlet Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="90e55-199">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="90e55-199">AzureRM.RedisCache</span></span>
* <span data-ttu-id="90e55-200">Tillåt att alla strängar används som storleksparametrar framöver.</span><span class="sxs-lookup"><span data-stu-id="90e55-200">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="90e55-201">Lägg till P5 i popup-fönstret PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="90e55-201">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="90e55-202">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="90e55-202">AzureRM.Resources</span></span>
* <span data-ttu-id="90e55-203">Parametern -Mode som saknades i Set-AzureRmPolicyDefinition har lagts till</span><span class="sxs-lookup"><span data-stu-id="90e55-203">Add missing -Mode parameter to Set-AzureRmPolicyDefinition</span></span>
* <span data-ttu-id="90e55-204">Åtgärda buggen för cmdleten Get-AzureRmProviderOperation för åtgärder med ursprung som innehåller användare</span><span class="sxs-lookup"><span data-stu-id="90e55-204">Fix Get-AzureRmProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="90e55-205">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="90e55-205">AzureRM.Sql</span></span>
* <span data-ttu-id="90e55-206">Ett problem där vissa cmdletar för säkerhetskopiering inte kunde identifiera den aktuella azure-prenumerationen har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="90e55-206">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="90e55-207">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="90e55-207">AzureRM.Storage</span></span>
* <span data-ttu-id="90e55-208">Stöd för att hämta användningsinformation om en Storage-resurs för en specifik plats och för att lägga till ett varningsmeddelande för att hämta användningsinformation om en global Storage-resurs är inaktuellt.</span><span class="sxs-lookup"><span data-stu-id="90e55-208">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="90e55-209">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="90e55-209">Get-AzureRmStorageUsage</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="90e55-210">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="90e55-210">AzureRM.Websites</span></span>
* <span data-ttu-id="90e55-211">Ny cmdlet: Get-AzureRMWebAppContainerContinuousDeploymentUrl – Hämtar webhook-URL:en för kontinuerlig distribution av container</span><span class="sxs-lookup"><span data-stu-id="90e55-211">New Cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="90e55-212">Nya cmdletar: New-AzureRMWebAppContainerPSSession och Enter-WebAppContainerPSSession – Startar en PowerShell-fjärrsession i en containerapp för windows</span><span class="sxs-lookup"><span data-stu-id="90e55-212">New Cmdlets New-AzureRMWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="690---september-2018"></a><span data-ttu-id="90e55-213">6.9.0 – September 2018</span><span class="sxs-lookup"><span data-stu-id="90e55-213">6.9.0 - September 2018</span></span>
#### <a name="general"></a><span data-ttu-id="90e55-214">Allmänt</span><span class="sxs-lookup"><span data-stu-id="90e55-214">General</span></span>
* <span data-ttu-id="90e55-215">AzureRM.SignalR har lagts till i samlingsmodulen för AzureRM</span><span class="sxs-lookup"><span data-stu-id="90e55-215">AzureRM.SignalR was added to the AzureRM rollup module</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="90e55-216">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="90e55-216">AzureRM.Profile</span></span>
* <span data-ttu-id="90e55-217">Mindre ändringar i den gemensamma koden för lagring</span><span class="sxs-lookup"><span data-stu-id="90e55-217">Minor changes to the storage common code</span></span>
* <span data-ttu-id="90e55-218">Hjälpfiler har uppdaterats för att innehålla fullständiga parametertyper.</span><span class="sxs-lookup"><span data-stu-id="90e55-218">Updated help files to include full parameter types.</span></span>
* <span data-ttu-id="90e55-219">-ServicePrincipal har ändrats så att den inte längre är obligatorisk i parameteruppsättningen ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="90e55-219">Changed -ServicePrincipal to non-mandatory in the ServicePrincipalCertificateWithSubscriptionId parameter set</span></span> 

#### <a name="azurestorage"></a><span data-ttu-id="90e55-220">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="90e55-220">Azure.Storage</span></span>
* <span data-ttu-id="90e55-221">Stöd för att skapa lagringskontext med OAuth.</span><span class="sxs-lookup"><span data-stu-id="90e55-221">Support create Storage Context with OAuth.</span></span> 
    - <span data-ttu-id="90e55-222">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="90e55-222">New-AzureStorageContext</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="90e55-223">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="90e55-223">AzureRM.Cdn</span></span>
* <span data-ttu-id="90e55-224">Standard_Microsoft har lagts till i SKU:n för CDN-prissättning.</span><span class="sxs-lookup"><span data-stu-id="90e55-224">Added Standard_Microsoft in Cdn pricing sku.</span></span> 

#### <a name="azurermcompute"></a><span data-ttu-id="90e55-225">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="90e55-225">AzureRM.Compute</span></span>
* <span data-ttu-id="90e55-226">Flytta beroenden i nyckelvalv och minne till de gemensamma beroendena</span><span class="sxs-lookup"><span data-stu-id="90e55-226">Move dependencies on Keyvault and Storage to the common dependencies</span></span>
* <span data-ttu-id="90e55-227">Lägg till stöd för flera storlekar av virtuella datorer i AEM-cmdletar</span><span class="sxs-lookup"><span data-stu-id="90e55-227">Add support for more virutal machine sizes to AEM cmdlets</span></span>
* <span data-ttu-id="90e55-228">Lägg till parametern PublicIPPrefix i New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="90e55-228">Add PublicIPPrefix parameter to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="90e55-229">Lägg till parametern ResourceId till cmdleten Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="90e55-229">Add ResourceId parameter to Invoke-AzureRmVMRunCommand cmdelt</span></span>
* <span data-ttu-id="90e55-230">Lägg till cmdleten Invoke-AzureRmVmssVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="90e55-230">Add Invoke-AzureRmVmssVMRunCommand cmdlet</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="90e55-231">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="90e55-231">AzureRM.Dns</span></span>
* <span data-ttu-id="90e55-232">Stöd har lagts till för aliasposter när DNS-poster skapas</span><span class="sxs-lookup"><span data-stu-id="90e55-232">Added support for alias record during dns record creation</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="90e55-233">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="90e55-233">AzureRM.Insights</span></span>
* <span data-ttu-id="90e55-234">Problem #6833 och #7102 (området Diagnostikinställningar) har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="90e55-234">Fixed issues #6833 and #7102 (Diagnostic Settings area)</span></span>
    - <span data-ttu-id="90e55-235">Problem med standardnamnet, d.v.s. ”tjänsten” när diagnostikinställningar skapas och listas/hämtas</span><span class="sxs-lookup"><span data-stu-id="90e55-235">Issues with the default name, i.e. 'service', during creation and listing/getting of diagnostic settings</span></span>
    - <span data-ttu-id="90e55-236">Problem med att skapa diagnostikinställningar med kategorier</span><span class="sxs-lookup"><span data-stu-id="90e55-236">Issues creating diagnostic settings with categories</span></span>
* <span data-ttu-id="90e55-237">Utfasningsmeddelande har lagts till för tidsintervallsparametrar för mått</span><span class="sxs-lookup"><span data-stu-id="90e55-237">Added deprecation message for metrics time grains parameters</span></span>
    - <span data-ttu-id="90e55-238">Tidsintervallsparametrar går fortfarande att använda (det här är en bakåtkompatibel ändring), men de ignoreras i serverdelen eftersom endast PT1M är giltigt</span><span class="sxs-lookup"><span data-stu-id="90e55-238">Timegrains parameters are still being accepted (this is a non-breaking change,) but they are ignored in the backend since only PT1M is valid</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="90e55-239">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="90e55-239">AzureRM.Network</span></span>
* <span data-ttu-id="90e55-240">Ändringar i LoadBalancer-cmdletar</span><span class="sxs-lookup"><span data-stu-id="90e55-240">Changes to LoadBalancer cmdlets</span></span>
  - <span data-ttu-id="90e55-241">LoadBalancerInboundNatPoolConfig: parametrarna IdleTimeoutInMinutes, EnableFloatingIp och EnableTcpReset har lagts till</span><span class="sxs-lookup"><span data-stu-id="90e55-241">LoadBalancerInboundNatPoolConfig: added parameters IdleTimeoutInMinutes, EnableFloatingIp and EnableTcpReset</span></span>
  - <span data-ttu-id="90e55-242">LoadBalancerInboundNatRuleConfig: parametern EnableTcpReset har lagts till</span><span class="sxs-lookup"><span data-stu-id="90e55-242">LoadBalancerInboundNatRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="90e55-243">LoadBalancerRuleConfig: parametern EnableTcpReset har lagts till</span><span class="sxs-lookup"><span data-stu-id="90e55-243">LoadBalancerRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="90e55-244">LoadBalancerProbeConfig: stöd för värdet ”Https” för parameterprotokoll har lagts till</span><span class="sxs-lookup"><span data-stu-id="90e55-244">LoadBalancerProbeConfig: added support for value "Https" for parameter Protocol</span></span>
* <span data-ttu-id="90e55-245">Nya kommandon för den nya underresursen för LoadBalancers OutboundRule har lagts till</span><span class="sxs-lookup"><span data-stu-id="90e55-245">Added new commands for new LoadBalancer's subresource OutboundRule</span></span>
  - <span data-ttu-id="90e55-246">Add-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="90e55-246">Add-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="90e55-247">Get-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="90e55-247">Get-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="90e55-248">New-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="90e55-248">New-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="90e55-249">Set-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="90e55-249">Set-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="90e55-250">Remove-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="90e55-250">Remove-AzureRmLoadBalancerOutboundRuleConfig</span></span>
* <span data-ttu-id="90e55-251">Ny HostedWorkloads-egenskap har lagts till för PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="90e55-251">Added new HostedWorkloads property for PSNetworkInterface</span></span>
* <span data-ttu-id="90e55-252">Nya cmdletar har lagts till för funktionen: Azure Firewall via ARM</span><span class="sxs-lookup"><span data-stu-id="90e55-252">Added new cmdlets for feature: Azure Firewall via ARM</span></span>
  - <span data-ttu-id="90e55-253">Get-AzureRmFirewall har lagts till</span><span class="sxs-lookup"><span data-stu-id="90e55-253">Added Get-AzureRmFirewall</span></span>
  - <span data-ttu-id="90e55-254">Set-AzureRmFirewall har lagts till</span><span class="sxs-lookup"><span data-stu-id="90e55-254">Added Set-AzureRmFirewall</span></span>
  - <span data-ttu-id="90e55-255">New-AzureRmFirewall har lagts till</span><span class="sxs-lookup"><span data-stu-id="90e55-255">Added New-AzureRmFirewall</span></span>
  - <span data-ttu-id="90e55-256">Remove-AzureRmFirewall har lagts till</span><span class="sxs-lookup"><span data-stu-id="90e55-256">Added Remove-AzureRmFirewall</span></span>
  - <span data-ttu-id="90e55-257">New-AzureRmFirewallApplicationRuleCollection har lagts till</span><span class="sxs-lookup"><span data-stu-id="90e55-257">Added New-AzureRmFirewallApplicationRuleCollection</span></span>
  - <span data-ttu-id="90e55-258">New-AzureRmFirewallApplicationRule har lagts till</span><span class="sxs-lookup"><span data-stu-id="90e55-258">Added New-AzureRmFirewallApplicationRule</span></span>
  - <span data-ttu-id="90e55-259">New-AzureRmFirewallNatRuleCollection har lagts till</span><span class="sxs-lookup"><span data-stu-id="90e55-259">Added New-AzureRmFirewallNatRuleCollection</span></span>
  - <span data-ttu-id="90e55-260">New-AzureRmFirewallNatRule har lagts till</span><span class="sxs-lookup"><span data-stu-id="90e55-260">Added New-AzureRmFirewallNatRule</span></span>
  - <span data-ttu-id="90e55-261">New-AzureRmFirewallNetworkRuleCollection har lagts till</span><span class="sxs-lookup"><span data-stu-id="90e55-261">Added New-AzureRmFirewallNetworkRuleCollection</span></span>
  - <span data-ttu-id="90e55-262">New-AzureRmFirewallNetworkRule har lagts till</span><span class="sxs-lookup"><span data-stu-id="90e55-262">Added New-AzureRmFirewallNetworkRule</span></span>
* <span data-ttu-id="90e55-263">Stöd för betrott rotcertifikat och konfiguration för autoskalning har lagts till i Application Gateway</span><span class="sxs-lookup"><span data-stu-id="90e55-263">Added support for Trusted Root certificate and Autoscale configuration in Application Gateway</span></span>
  - <span data-ttu-id="90e55-264">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="90e55-264">New Cmdlets added:</span></span>
      - <span data-ttu-id="90e55-265">Add-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="90e55-265">Add-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="90e55-266">Get-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="90e55-266">Get-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="90e55-267">New-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="90e55-267">New-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="90e55-268">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="90e55-268">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="90e55-269">Set-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="90e55-269">Set-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="90e55-270">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="90e55-270">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="90e55-271">New-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="90e55-271">New-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="90e55-272">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="90e55-272">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="90e55-273">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="90e55-273">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
  - <span data-ttu-id="90e55-274">Cmdletar har uppdaterats med valfri parameter – TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="90e55-274">Cmdlets updated with optonal parameter -TrustedRootCertificate</span></span>
      - <span data-ttu-id="90e55-275">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="90e55-275">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="90e55-276">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="90e55-276">Set-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="90e55-277">New-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="90e55-277">New-AzureRmApplicationGatewayBackendHttpSetting</span></span>
      - <span data-ttu-id="90e55-278">Set-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="90e55-278">Set-AzureRmApplicationGatewayBackendHttpSetting</span></span>
  - <span data-ttu-id="90e55-279">Cmdletar har uppdaterats med valfri parameter – AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="90e55-279">Cmdlets updated with optonal parameter -AutoscaleConfiguration</span></span>
      - <span data-ttu-id="90e55-280">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="90e55-280">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="90e55-281">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="90e55-281">Set-AzureRmApplicationGateway</span></span>
* <span data-ttu-id="90e55-282">Lägg till cmdlet för gränssnittsslutpunkten Get-AzureInterfaceEndpoint</span><span class="sxs-lookup"><span data-stu-id="90e55-282">Add cmdlet for Interface Endpoint Get-AzureInterfaceEndpoint</span></span>
* <span data-ttu-id="90e55-283">Stöd för flera adressprefix i ett undernät har lagts till.</span><span class="sxs-lookup"><span data-stu-id="90e55-283">Added support for multiple address prefixes in a subnet.</span></span> <span data-ttu-id="90e55-284">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="90e55-284">Updated cmdlets:</span></span>
  - <span data-ttu-id="90e55-285">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="90e55-285">New-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="90e55-286">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="90e55-286">Set-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="90e55-287">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="90e55-287">Add-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="90e55-288">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="90e55-288">Get-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="90e55-289">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="90e55-289">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>
  - <span data-ttu-id="90e55-290">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="90e55-290">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="90e55-291">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="90e55-291">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="90e55-292">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="90e55-292">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="90e55-293">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="90e55-293">Add-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="90e55-294">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="90e55-294">New-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="90e55-295">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="90e55-295">Set-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="90e55-296">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="90e55-296">Add-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="90e55-297">New-AzureRmNetworkInterfaceIpConfig – Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="90e55-297">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="90e55-298">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="90e55-298">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="90e55-299">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="90e55-299">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="90e55-300">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="90e55-300">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="90e55-301">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="90e55-301">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="90e55-302">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="90e55-302">New-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="90e55-303">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="90e55-303">New-AzureRmNetworkInterface</span></span>
* <span data-ttu-id="90e55-304">Lägger till cmdletar för delegering av undernät.</span><span class="sxs-lookup"><span data-stu-id="90e55-304">Adding cmdlets for subnet delegation.</span></span>
  - <span data-ttu-id="90e55-305">New-AzureRmDelegation: Skapar en ny delegering som kan läggas till i ett undernät</span><span class="sxs-lookup"><span data-stu-id="90e55-305">New-AzureRmDelegation: Creates a new delegation, which can be added to a subnet</span></span>
  - <span data-ttu-id="90e55-306">Remove-AzureRmDelegation: Hämtar ett undernät och tar bort det angivna delegeringsnamnet från undernätet</span><span class="sxs-lookup"><span data-stu-id="90e55-306">Remove-AzureRmDelegation: Takes in a subnet and removes the provided delegation name from that subnet</span></span>
  - <span data-ttu-id="90e55-307">Add-AzureRmDelegation: Hämtar ett undernät och lägger till det angivna tjänstnamnet som en delegering till undernätet</span><span class="sxs-lookup"><span data-stu-id="90e55-307">Add-AzureRmDelegation: Takes in a subnet and adds the provided service name as a delegation to that subnet</span></span>
  - <span data-ttu-id="90e55-308">Get-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="90e55-308">Get-AzureRmDelegation</span></span>
  - <span data-ttu-id="90e55-309">Get-AzureRmAvailableServiceDelegations</span><span class="sxs-lookup"><span data-stu-id="90e55-309">Get-AzureRmAvailableServiceDelegations</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="90e55-310">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="90e55-310">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="90e55-311">Stöd för hanterad disk</span><span class="sxs-lookup"><span data-stu-id="90e55-311">Support for managed Managed disk</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="90e55-312">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="90e55-312">AzureRM.RedisCache</span></span>
* <span data-ttu-id="90e55-313">Insights-beroende har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="90e55-313">Updated Insights dependency.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="90e55-314">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="90e55-314">AzureRM.Resources</span></span>
* <span data-ttu-id="90e55-315">Uppdatera New-AzureRmResourceGroupDeployment med den nya parametern RollbackAction</span><span class="sxs-lookup"><span data-stu-id="90e55-315">Update New-AzureRmResourceGroupDeployment with new parameter RollbackAction</span></span>
    - <span data-ttu-id="90e55-316">Lägg till stöd för OnErrorDeployment med den nya parametern.</span><span class="sxs-lookup"><span data-stu-id="90e55-316">Add support for OnErrorDeployment with the new parameter.</span></span>
* <span data-ttu-id="90e55-317">Stöd för hanterad identitet på principtilldelningar.</span><span class="sxs-lookup"><span data-stu-id="90e55-317">Support managed identity on policy assignments.</span></span>
* <span data-ttu-id="90e55-318">Parametrar med standardvärden krävs inte längre när du tilldelar en princip med ”New-AzureRmPolicyAssignment”</span><span class="sxs-lookup"><span data-stu-id="90e55-318">Parameters with default values are no longer requred when assigning a policy with 'New-AzureRmPolicyAssignment'</span></span>
* <span data-ttu-id="90e55-319">Lägg till den nya cmdleten Get-AzureRmPolicyAlias för att hämta principalias</span><span class="sxs-lookup"><span data-stu-id="90e55-319">Add new cmdlet Get-AzureRmPolicyAlias for retrieving policy aliases</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="90e55-320">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="90e55-320">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="90e55-321">Problem #7161 har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="90e55-321">Fixed issue #7161</span></span>

#### <a name="azurermsignalr"></a><span data-ttu-id="90e55-322">AzureRM.SignalR</span><span class="sxs-lookup"><span data-stu-id="90e55-322">AzureRM.SignalR</span></span>
* <span data-ttu-id="90e55-323">Uppdatera SKU-namn till Free_F1 och Standard_S1</span><span class="sxs-lookup"><span data-stu-id="90e55-323">Update SKU names to Free_F1 and Standard_S1</span></span>
* <span data-ttu-id="90e55-324">Lägg till versionsfältet i PSSignalRResource-objektet och en anslutningssträng i PSSignalRKeys-objektet.</span><span class="sxs-lookup"><span data-stu-id="90e55-324">Add version field to the PSSignalRResource object and connection string to the PSSignalRKeys object.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="90e55-325">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="90e55-325">AzureRM.Storage</span></span>
* <span data-ttu-id="90e55-326">Stöd för oföränderlighetsprincip i AzureRm.Storage</span><span class="sxs-lookup"><span data-stu-id="90e55-326">Support Immutability Policy in AzureRm.Storage</span></span> 
    - <span data-ttu-id="90e55-327">Remove-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="90e55-327">Remove-AzureRmStorageAccountNetworkRule</span></span>
    - <span data-ttu-id="90e55-328">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="90e55-328">Get-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="90e55-329">Update-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="90e55-329">Update-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="90e55-330">New-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="90e55-330">New-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="90e55-331">Remove-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="90e55-331">Remove-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="90e55-332">Add-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="90e55-332">Add-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="90e55-333">Remove-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="90e55-333">Remove-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="90e55-334">Set-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="90e55-334">Set-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="90e55-335">Get-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="90e55-335">Get-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="90e55-336">Remove-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="90e55-336">Remove-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="90e55-337">Lock-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="90e55-337">Lock-AzureRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="90e55-338">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="90e55-338">AzureRM.Websites</span></span>
* <span data-ttu-id="90e55-339">Två nya cmdletar har lagts till: Get-AzureRmDeletedWebApp och Restore-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="90e55-339">Added two new cmdlets: Get-AzureRmDeletedWebApp and Restore-AzureRmDeletedWebApp</span></span>
* <span data-ttu-id="90e55-340">New-AzureRmAppServicePlan – En HyperV-växel har lagts till för skapa en app service-plan med Windows-containrar</span><span class="sxs-lookup"><span data-stu-id="90e55-340">New-AzureRmAppServicePlan -HyperV switch is added for create app service plan with windows container</span></span>
* <span data-ttu-id="90e55-341">New-AzureRmWebApp/New-AzureRmWebAppSlot/Set-AzureRmWebApp/Set-AzureRmWebAppSlot – Nya parametrar (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) har lagts till för att skapa och hantera Windows-containerappar</span><span class="sxs-lookup"><span data-stu-id="90e55-341">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - New parameters (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) added for creating and managing windows container app</span></span>

## <a name="681---august-2018"></a><span data-ttu-id="90e55-342">6.8.1 – augusti 2018</span><span class="sxs-lookup"><span data-stu-id="90e55-342">6.8.1 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="90e55-343">Allmänt</span><span class="sxs-lookup"><span data-stu-id="90e55-343">General</span></span>
* <span data-ttu-id="90e55-344">Problem med standardresursgrupp som inte har konfigurerats har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="90e55-344">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="90e55-345">Uppdaterade Common Runtime-sammansättningar</span><span class="sxs-lookup"><span data-stu-id="90e55-345">Updated common runtime assemblies</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="90e55-346">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="90e55-346">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="90e55-347">Problem med standardresursgrupp som inte har konfigurerats har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="90e55-347">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="90e55-348">Åtgärdat problem https://github.com/Azure/azure-powershell/issues/6603</span><span class="sxs-lookup"><span data-stu-id="90e55-348">Fixed issue https://github.com/Azure/azure-powershell/issues/6603</span></span>
    - <span data-ttu-id="90e55-349">Import-AzureRmApiManagementApi- och \*-AzureRmApiManagementCertificate-cmdletar kan nu hantera relativa sökvägar</span><span class="sxs-lookup"><span data-stu-id="90e55-349">Import-AzureRmApiManagementApi and \*-AzureRmApiManagementCertificate cmdlets now handle relative Paths</span></span>
* <span data-ttu-id="90e55-350">Åtgärdat problem https://github.com/Azure/azure-powershell/issues/6879</span><span class="sxs-lookup"><span data-stu-id="90e55-350">Fixed issue https://github.com/Azure/azure-powershell/issues/6879</span></span>
    - <span data-ttu-id="90e55-351">CertificateInformation är en inställbar egenskap som gör att Set-AzureRmApiManagement-cmdleten fungerar ordentligt.</span><span class="sxs-lookup"><span data-stu-id="90e55-351">The CertificateInformation is a settable property allowing for Set-AzureRmApiManagement cmdlet to work property.</span></span> <span data-ttu-id="90e55-352">Åtgärdat genom uppgradering till NuGet för 4.0.4-preview</span><span class="sxs-lookup"><span data-stu-id="90e55-352">Fixed by upgrading to 4.0.4-preview nuget</span></span>
* <span data-ttu-id="90e55-353">Åtgärdat problem https://github.com/Azure/azure-powershell/issues/6853</span><span class="sxs-lookup"><span data-stu-id="90e55-353">Fixed issue https://github.com/Azure/azure-powershell/issues/6853</span></span>
    - <span data-ttu-id="90e55-354">Odata-filtret för sökning efter namn på produkt har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="90e55-354">Fixed the Odata filter for Search by Name on Product</span></span>
* <span data-ttu-id="90e55-355">Åtgärdat problem https://github.com/Azure/azure-powershell/issues/6814</span><span class="sxs-lookup"><span data-stu-id="90e55-355">Fixed issue https://github.com/Azure/azure-powershell/issues/6814</span></span>
    - <span data-ttu-id="90e55-356">Odata-filtret för sökning efter namn på API har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="90e55-356">Fixed the Odata filter for Search by Name on Api</span></span>
* <span data-ttu-id="90e55-357">Stöd har lagts till för AzureMonitor-loggare</span><span class="sxs-lookup"><span data-stu-id="90e55-357">Added support for AzureMonitor logger</span></span>


#### <a name="azurermcompute"></a><span data-ttu-id="90e55-358">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="90e55-358">AzureRM.Compute</span></span>
* <span data-ttu-id="90e55-359">Ett problem med att mål saknas i felutdata har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="90e55-359">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="90e55-360">Problem med lagringskontotyper för virtuell dator med en hanterad disk har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="90e55-360">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="90e55-361">Problem med standardresursgrupp som inte har konfigurerats har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="90e55-361">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="90e55-362">Åtgärda cmdletar för AEM-tillägg för andra miljöer, till exempel Azure Kina</span><span class="sxs-lookup"><span data-stu-id="90e55-362">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="90e55-363">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="90e55-363">AzureRM.Network</span></span>
* <span data-ttu-id="90e55-364">Standardvisning av cmdlet-utdata har ändrats för att visas i tabellvy</span><span class="sxs-lookup"><span data-stu-id="90e55-364">Changed default cmdlet output presentation to table view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="90e55-365">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="90e55-365">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="90e55-366">Åtgärda fel i Update-AzureRmPowerBIEmbeddedCapacity vid försök att skala pausad kapacitet</span><span class="sxs-lookup"><span data-stu-id="90e55-366">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>


#### <a name="azurermresources"></a><span data-ttu-id="90e55-367">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="90e55-367">AzureRM.Resources</span></span>
* <span data-ttu-id="90e55-368">Ett problem med att skapa hanterade program från MarketPlace har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="90e55-368">Fixed issue with creating managed applications from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="90e55-369">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="90e55-369">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="90e55-370">Åtgärdade problem</span><span class="sxs-lookup"><span data-stu-id="90e55-370">Fixed issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="90e55-371">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="90e55-371">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="90e55-372">Stöd har lagts till för trafikroutningsmetoden MultiValue</span><span class="sxs-lookup"><span data-stu-id="90e55-372">Added Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="90e55-373">Ny parameter, ”MaxReturn”, för MultiValue-routning</span><span class="sxs-lookup"><span data-stu-id="90e55-373">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="90e55-374">Stöd har lagts till för trafikroutningsmetod för undernät</span><span class="sxs-lookup"><span data-stu-id="90e55-374">Added Support for the Subnet routing method</span></span>
    - <span data-ttu-id="90e55-375">Stöd för IP-adressintervall (undernät) i slutpunkter</span><span class="sxs-lookup"><span data-stu-id="90e55-375">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="90e55-376">Stöd har lagts till för anpassade rubriker i profiler</span><span class="sxs-lookup"><span data-stu-id="90e55-376">Added Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="90e55-377">Stöd har lagts till för förväntade statuskodintervall i profiler</span><span class="sxs-lookup"><span data-stu-id="90e55-377">Added Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="90e55-378">Stöd har lagts till för anpassade rubriker i slutpunkter</span><span class="sxs-lookup"><span data-stu-id="90e55-378">Added Support for Custom Headers in endpoints</span></span>

## <a name="680---august-2018"></a><span data-ttu-id="90e55-379">6.8.0 – augusti 2018</span><span class="sxs-lookup"><span data-stu-id="90e55-379">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="90e55-380">Allmänt</span><span class="sxs-lookup"><span data-stu-id="90e55-380">General</span></span>
* <span data-ttu-id="90e55-381">Problem med standardresursgrupp som inte har konfigurerats har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="90e55-381">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="90e55-382">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="90e55-382">AzureRM.Profile</span></span>
* <span data-ttu-id="90e55-383">Utgångsegenskap har lagts till i token som returneras under Connect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="90e55-383">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="90e55-384">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="90e55-384">AzureRM.Compute</span></span>
* <span data-ttu-id="90e55-385">Ett problem med att mål saknas i felutdata har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="90e55-385">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="90e55-386">Problem med lagringskontotyper för virtuell dator med en hanterad disk har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="90e55-386">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="90e55-387">Åtgärda cmdletar för AEM-tillägg för andra miljöer, till exempel Azure Kina</span><span class="sxs-lookup"><span data-stu-id="90e55-387">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="90e55-388">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="90e55-388">AzureRM.IotHub</span></span>
* <span data-ttu-id="90e55-389">Korrigera exempel för New-AzureRmIotHubExportDevices och New-AzureRmIotHubImportDevices</span><span class="sxs-lookup"><span data-stu-id="90e55-389">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="90e55-390">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="90e55-390">AzureRM.Network</span></span>
* <span data-ttu-id="90e55-391">Standardmodeller har ändrats för att visas i tabellvy</span><span class="sxs-lookup"><span data-stu-id="90e55-391">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="90e55-392">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="90e55-392">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="90e55-393">Åtgärda fel i Update-AzureRmPowerBIEmbeddedCapacity vid försök att skala pausad kapacitet</span><span class="sxs-lookup"><span data-stu-id="90e55-393">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="90e55-394">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="90e55-394">AzureRM.Resources</span></span>
* <span data-ttu-id="90e55-395">Ett problem med att skapa hanterade program från MarketPlace har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="90e55-395">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="90e55-396">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="90e55-396">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="90e55-397">Korrigeringar för problem</span><span class="sxs-lookup"><span data-stu-id="90e55-397">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="90e55-398">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="90e55-398">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="90e55-399">Stöd för trafikroutningsmetoden MultiValue</span><span class="sxs-lookup"><span data-stu-id="90e55-399">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="90e55-400">Ny parameter, ”MaxReturn”, för MultiValue-routning</span><span class="sxs-lookup"><span data-stu-id="90e55-400">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="90e55-401">Stöd för trafikroutningsmetod för undernät</span><span class="sxs-lookup"><span data-stu-id="90e55-401">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="90e55-402">Stöd för IP-adressintervall (undernät) i slutpunkter</span><span class="sxs-lookup"><span data-stu-id="90e55-402">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="90e55-403">Stöd för anpassade rubriker i profiler</span><span class="sxs-lookup"><span data-stu-id="90e55-403">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="90e55-404">Stöd för förväntade statuskodintervall i profiler</span><span class="sxs-lookup"><span data-stu-id="90e55-404">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="90e55-405">Stöd för anpassade rubriker i slutpunkter</span><span class="sxs-lookup"><span data-stu-id="90e55-405">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="90e55-406">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="90e55-406">AzureRM.Websites</span></span>
* <span data-ttu-id="90e55-407">Problem med standardresursgrupp som inte har konfigurerats korrekt har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="90e55-407">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="90e55-408">6.7.0 – augusti 2018</span><span class="sxs-lookup"><span data-stu-id="90e55-408">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="90e55-409">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="90e55-409">AzureRM.Profile</span></span>
* <span data-ttu-id="90e55-410">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="90e55-410">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="90e55-411">Lägg till användar-id i standardkontextnamnet för att undvika kontextkonflikter</span><span class="sxs-lookup"><span data-stu-id="90e55-411">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="90e55-412">Åtgärda problem med Clear-AzureRmContext som orsakade problem med att välja en kontext #6398</span><span class="sxs-lookup"><span data-stu-id="90e55-412">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="90e55-413">Aktivera den klientorganisationsdomän som ska skickas till parametern -TenantId för Connect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="90e55-413">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="90e55-414">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="90e55-414">Azure.Storage</span></span>
* <span data-ttu-id="90e55-415">Ta bort begränsningen på 5 TB för Azure-filresurskvoten</span><span class="sxs-lookup"><span data-stu-id="90e55-415">Remove the 5TB limitation for Azure File Share quota</span></span>
* <span data-ttu-id="90e55-416">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="90e55-416">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="90e55-417">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="90e55-417">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="90e55-418">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="90e55-418">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="90e55-419">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="90e55-419">Azure.AnalysisServices</span></span>
* <span data-ttu-id="90e55-420">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="90e55-420">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="90e55-421">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="90e55-421">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="90e55-422">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="90e55-422">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="90e55-423">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="90e55-423">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="90e55-424">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="90e55-424">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="90e55-425">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="90e55-425">AzureRM.Automation</span></span>
* <span data-ttu-id="90e55-426">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="90e55-426">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="90e55-427">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="90e55-427">AzureRM.Backup</span></span>
* <span data-ttu-id="90e55-428">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="90e55-428">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="90e55-429">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="90e55-429">AzureRM.Batch</span></span>
* <span data-ttu-id="90e55-430">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="90e55-430">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="90e55-431">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="90e55-431">AzureRM.Billing</span></span>
* <span data-ttu-id="90e55-432">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="90e55-432">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="90e55-433">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="90e55-433">AzureRM.Cdn</span></span>
* <span data-ttu-id="90e55-434">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="90e55-434">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="90e55-435">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="90e55-435">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="90e55-436">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="90e55-436">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="90e55-437">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="90e55-437">AzureRM.Compute</span></span>
* <span data-ttu-id="90e55-438">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="90e55-438">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="90e55-439">Lägg till parametern EvictionPolicy i New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="90e55-439">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="90e55-440">Använd standardplatsen i DiskFileParameterSet för New-AzureRmVm om ingen plats har angetts.</span><span class="sxs-lookup"><span data-stu-id="90e55-440">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="90e55-441">Korrigera parameterbeskrivningen i Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="90e55-441">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="90e55-442">Korrigera cmdleten Get-AzureRmVMDiskEncryptionStatus för vissa singlepass-relaterade scenarier</span><span class="sxs-lookup"><span data-stu-id="90e55-442">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="90e55-443">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="90e55-443">AzureRM.Consumption</span></span>
* <span data-ttu-id="90e55-444">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="90e55-444">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="90e55-445">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="90e55-445">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="90e55-446">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="90e55-446">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="90e55-447">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="90e55-447">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="90e55-448">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="90e55-448">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="90e55-449">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="90e55-449">AzureRM.DataFactories</span></span>
* <span data-ttu-id="90e55-450">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="90e55-450">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="90e55-451">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="90e55-451">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="90e55-452">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="90e55-452">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="90e55-453">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="90e55-453">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="90e55-454">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="90e55-454">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="90e55-455">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="90e55-455">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="90e55-456">Korrigera felsökning när DebugPreference anges från powershell-kommandoraden</span><span class="sxs-lookup"><span data-stu-id="90e55-456">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="90e55-457">Uppdatera exemplet för Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="90e55-457">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="90e55-458">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="90e55-458">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="90e55-459">Uppdatera exemplet för Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="90e55-459">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="90e55-460">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="90e55-460">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="90e55-461">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="90e55-461">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="90e55-462">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="90e55-462">AzureRM.Dns</span></span>
* <span data-ttu-id="90e55-463">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="90e55-463">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="90e55-464">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="90e55-464">AzureRM.EventGrid</span></span>
* <span data-ttu-id="90e55-465">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="90e55-465">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="90e55-466">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="90e55-466">AzureRM.EventHub</span></span>
* <span data-ttu-id="90e55-467">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="90e55-467">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="90e55-468">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="90e55-468">AzureRM.HDInsight</span></span>
* <span data-ttu-id="90e55-469">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="90e55-469">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="90e55-470">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="90e55-470">AzureRM.Insights</span></span>
* <span data-ttu-id="90e55-471">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="90e55-471">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="90e55-472">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="90e55-472">AzureRM.IotHub</span></span>
* <span data-ttu-id="90e55-473">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="90e55-473">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="90e55-474">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="90e55-474">AzureRM.KeyVault</span></span>
* <span data-ttu-id="90e55-475">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="90e55-475">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="90e55-476">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="90e55-476">AzureRM.LogicApp</span></span>
* <span data-ttu-id="90e55-477">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="90e55-477">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="90e55-478">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="90e55-478">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="90e55-479">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="90e55-479">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="90e55-480">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="90e55-480">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="90e55-481">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="90e55-481">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="90e55-482">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="90e55-482">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="90e55-483">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="90e55-483">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="90e55-484">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="90e55-484">AzureRM.Media</span></span>
* <span data-ttu-id="90e55-485">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="90e55-485">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="90e55-486">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="90e55-486">AzureRM.Network</span></span>
* <span data-ttu-id="90e55-487">Exempel för Set-AzureRmLocalNetworkGateway har lagts till</span><span class="sxs-lookup"><span data-stu-id="90e55-487">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="90e55-488">Exempel och beskrivningar för Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey och New-AzureRmVirtualNetworkGatewayConnection har lagts till</span><span class="sxs-lookup"><span data-stu-id="90e55-488">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="90e55-489">Exempel för Remove-AzureRmVirtualNetworkGatewayIpConfig och Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="90e55-489">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="90e55-490">Exempel för Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey har lagts till</span><span class="sxs-lookup"><span data-stu-id="90e55-490">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="90e55-491">Exempel för Set-AzureRmVirtualNetworkGatewayConnectionSharedKey har lagts till</span><span class="sxs-lookup"><span data-stu-id="90e55-491">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="90e55-492">Exempel för Set-AzureRmVirtualNetworkGatewayConnection har lagts till</span><span class="sxs-lookup"><span data-stu-id="90e55-492">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="90e55-493">Cmdletar för ApplicationSecurityGroup, RouteTable and Usage har genererats om med den senaste kodgeneratorn</span><span class="sxs-lookup"><span data-stu-id="90e55-493">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="90e55-494">Förtydligade ett felmeddelande för Get-AzureRmVirtualNetworkSubnetConfig vid försök att hämta ett undernät som inte avslutas</span><span class="sxs-lookup"><span data-stu-id="90e55-494">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="90e55-495">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="90e55-495">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="90e55-496">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="90e55-496">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="90e55-497">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="90e55-497">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="90e55-498">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="90e55-498">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="90e55-499">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="90e55-499">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="90e55-500">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="90e55-500">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="90e55-501">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="90e55-501">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="90e55-502">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="90e55-502">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="90e55-503">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="90e55-503">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="90e55-504">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="90e55-504">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="90e55-505">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="90e55-505">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="90e55-506">Lade till principfilter i cmdleten Get-AzureRmRecoveryServicesBackItem.</span><span class="sxs-lookup"><span data-stu-id="90e55-506">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="90e55-507">Kommandot returnerar listan med säkerhetskopieringsobjekt som skyddas av det angivna princip-ID:t.</span><span class="sxs-lookup"><span data-stu-id="90e55-507">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="90e55-508">Microsoft.Azure.Management.RecoveryServices.Backup uppdaterades till förhandsversionen av 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="90e55-508">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="90e55-509">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="90e55-509">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="90e55-510">Parametern TargetResourceGroupName lades till i Restore-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="90e55-510">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="90e55-511">Den resursgrupp som de hanterade diskarna återställs till.</span><span class="sxs-lookup"><span data-stu-id="90e55-511">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="90e55-512">Gäller för säkerhetskopiering av virtuell dator med hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="90e55-512">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="90e55-513">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="90e55-513">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="90e55-514">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="90e55-514">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="90e55-515">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="90e55-515">AzureRM.RedisCache</span></span>
* <span data-ttu-id="90e55-516">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="90e55-516">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="90e55-517">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="90e55-517">AzureRM.Relay</span></span>
* <span data-ttu-id="90e55-518">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="90e55-518">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="90e55-519">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="90e55-519">AzureRM.Resources</span></span>
* <span data-ttu-id="90e55-520">Distribution av supportmall i prenumerationsomfånget.</span><span class="sxs-lookup"><span data-stu-id="90e55-520">Support template deployment at subscription scope.</span></span> <span data-ttu-id="90e55-521">Lägg till nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="90e55-521">Add new Cmdlets:</span></span>
    - <span data-ttu-id="90e55-522">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="90e55-522">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="90e55-523">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="90e55-523">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="90e55-524">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="90e55-524">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="90e55-525">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="90e55-525">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="90e55-526">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="90e55-526">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="90e55-527">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="90e55-527">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="90e55-528">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="90e55-528">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="90e55-529">Korrigera ett problem där fel inträffar när en kontext skickas till Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="90e55-529">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="90e55-530">Korrigera exempel i New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="90e55-530">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="90e55-531">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="90e55-531">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="90e55-532">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="90e55-532">AzureRM.Scheduler</span></span>
* <span data-ttu-id="90e55-533">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="90e55-533">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="90e55-534">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="90e55-534">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="90e55-535">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="90e55-535">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="90e55-536">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="90e55-536">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="90e55-537">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="90e55-537">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="90e55-538">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="90e55-538">AzureRM.Sql</span></span>
* <span data-ttu-id="90e55-539">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="90e55-539">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="90e55-540">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="90e55-540">AzureRM.Storage</span></span>
* <span data-ttu-id="90e55-541">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="90e55-541">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="90e55-542">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="90e55-542">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="90e55-543">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="90e55-543">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="90e55-544">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="90e55-544">AzureRM.Tags</span></span>
* <span data-ttu-id="90e55-545">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="90e55-545">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="90e55-546">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="90e55-546">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="90e55-547">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="90e55-547">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="90e55-548">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="90e55-548">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="90e55-549">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="90e55-549">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="90e55-550">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="90e55-550">AzureRM.Websites</span></span>
* <span data-ttu-id="90e55-551">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="90e55-551">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="90e55-552">6.6.0 – juli 2018</span><span class="sxs-lookup"><span data-stu-id="90e55-552">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="90e55-553">Allmänt</span><span class="sxs-lookup"><span data-stu-id="90e55-553">General</span></span>
* <span data-ttu-id="90e55-554">Alla hjälpfiler har uppdaterats för att ta med fullständiga parametertyper och korrekta indata-/utdatatyper.</span><span class="sxs-lookup"><span data-stu-id="90e55-554">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="90e55-555">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="90e55-555">AzureRM.Profile</span></span>
* <span data-ttu-id="90e55-556">Common.Strategy-biblioteket har uppdaterats för att kunna verifiera att den aktuella konfigurationsfilen för en resurs är kompatibel med målresursen.</span><span class="sxs-lookup"><span data-stu-id="90e55-556">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="90e55-557">ps1xml-typer har lagts till i Common.Storage</span><span class="sxs-lookup"><span data-stu-id="90e55-557">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="90e55-558">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="90e55-558">Azure.Storage</span></span>
* <span data-ttu-id="90e55-559">Lade till stöd för hämtning av lagringskontext från DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90e55-559">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="90e55-560">Lade till Ps1XmlAttribute till utdatatypegenskaper för cmdletar.</span><span class="sxs-lookup"><span data-stu-id="90e55-560">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="90e55-561">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="90e55-561">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="90e55-562">Åtgärdat problem https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="90e55-562">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="90e55-563">En bugg har åtgärdats i Automapper för att översätta PsApiManagementApi till ApiContract</span><span class="sxs-lookup"><span data-stu-id="90e55-563">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="90e55-564">Åtgärdat problem https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="90e55-564">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="90e55-565">En bugg har åtgärdats i File.Save för att inte överbelasta kodningstypen</span><span class="sxs-lookup"><span data-stu-id="90e55-565">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="90e55-566">Åtgärdat problem https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="90e55-566">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="90e55-567">Har uppgraderats till Nuget-versionen 4.0.3 vilket åtgärdar mönsterundantaget på apiId</span><span class="sxs-lookup"><span data-stu-id="90e55-567">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="90e55-568">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="90e55-568">AzureRM.Compute</span></span>
* <span data-ttu-id="90e55-569">Åtgärda problem med fel vid skapandet av en virtuell dator med hjälp av DiskFileParameterSet i New-AzureRmVm på grund av namnbyte på PremiumLRS-lagringskontotypen.</span><span class="sxs-lookup"><span data-stu-id="90e55-569">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="90e55-570">Åtgärda cmdleten Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="90e55-570">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="90e55-571">Uppdatera Get-AzureRmAvailabilitySet för att aktivera funktionen för att lista alla tillgänglighetsuppsättningar i en prenumeration.</span><span class="sxs-lookup"><span data-stu-id="90e55-571">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="90e55-572">(Parametern ResouceGroupName är nu frivillig.)</span><span class="sxs-lookup"><span data-stu-id="90e55-572">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="90e55-573">Uppdatera SimpleParameterSet för "New-AzureRmVm" för att aktivera accelererat nätverk på berättigade virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="90e55-573">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="90e55-574">Uppdatera den enkla parameteruppsättningen för New-AzureRmVmss så att det inte går att skapa de virtuella datorerna när en användarangiven lastbalanserare redan finns.</span><span class="sxs-lookup"><span data-stu-id="90e55-574">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="90e55-575">Uppdatera exempel för New-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="90e55-575">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="90e55-576">Lägg till exempel för "New-AzureRmVM"</span><span class="sxs-lookup"><span data-stu-id="90e55-576">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="90e55-577">Uppdatera beskrivning för Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="90e55-577">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="90e55-578">Uppdatera Exempel 1 för Set-AzureRmVMBginfoExtension för stavningskontroll och prefix.</span><span class="sxs-lookup"><span data-stu-id="90e55-578">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="90e55-579">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="90e55-579">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="90e55-580">ADF .Net SDK-versionen har uppdaterats till 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="90e55-580">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="90e55-581">Stöd för delning av Integration Runtime (lokal installation) mellan datafabriker.</span><span class="sxs-lookup"><span data-stu-id="90e55-581">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="90e55-582">Lägg till ny parameter – SharedIntegrationRuntimeResourceId i cmdleten Set-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="90e55-582">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="90e55-583">Lägg till ny valfri parameter – LinkedDataFactoryName i cmdleten Remove-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="90e55-583">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="90e55-584">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="90e55-584">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="90e55-585">DataPlane SDK-versionen (Microsoft.Azure.DataLake.Store) har uppdaterats till 1.1.9</span><span class="sxs-lookup"><span data-stu-id="90e55-585">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="90e55-586">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="90e55-586">AzureRM.EventHub</span></span>
* <span data-ttu-id="90e55-587">Piping för InputObject and ResourceId i borttagna cmdletar har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="90e55-587">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="90e55-588">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="90e55-588">AzureRM.Insights</span></span>
* <span data-ttu-id="90e55-589">Formatering har åtgärdats för OutputType i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="90e55-589">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="90e55-590">Använda Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span><span class="sxs-lookup"><span data-stu-id="90e55-590">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="90e55-591">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="90e55-591">AzureRM.KeyVault</span></span>
* <span data-ttu-id="90e55-592">Åtgärda problem med piping i Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="90e55-592">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="90e55-593">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="90e55-593">AzureRM.Network</span></span>
* <span data-ttu-id="90e55-594">Exempel har lagts till för LoadBalancerInboundNatPoolConfig-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="90e55-594">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="90e55-595">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="90e55-595">AzureRM.Resources</span></span>
* <span data-ttu-id="90e55-596">Åtgärda problem när både taggnamn och värde anges för "Get-AzureRmResource"</span><span class="sxs-lookup"><span data-stu-id="90e55-596">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="90e55-597">Åtgärda pipingscenario med "Set-AzureRmResource"</span><span class="sxs-lookup"><span data-stu-id="90e55-597">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="90e55-598">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="90e55-598">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="90e55-599">Piping för InputObject and ResourceId i borttagna cmdletar har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="90e55-599">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="90e55-600">några problem har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="90e55-600">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="90e55-601">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="90e55-601">AzureRM.Sql</span></span>
* <span data-ttu-id="90e55-602">Lägg till stöd för Server Advanced Threat Protection med följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="90e55-602">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="90e55-603">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="90e55-603">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="90e55-604">Lägg till stöd för Sårbarhetsbedömning med följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="90e55-604">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="90e55-605">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="90e55-605">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="90e55-606">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="90e55-606">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="90e55-607">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="90e55-607">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="90e55-608">Exempel i Remove-AzureRmSqlServerFirewallRule har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="90e55-608">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="90e55-609">Åtgärda felaktig hantering av datum och tid för andra kulturer än usa-baserade kulturer i Get-AzureSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="90e55-609">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="90e55-610">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="90e55-610">AzureRM.Storage</span></span>
* <span data-ttu-id="90e55-611">Lägg till Ps1XmlAttribute i utdatatypegenskaper för cmdletar</span><span class="sxs-lookup"><span data-stu-id="90e55-611">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="90e55-612">Visa utdata för cmdleten StorageAccount i tabellvyn</span><span class="sxs-lookup"><span data-stu-id="90e55-612">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="90e55-613">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="90e55-613">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="90e55-614">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="90e55-614">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="90e55-615">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="90e55-615">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="90e55-616">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="90e55-616">AzureRM.Tags</span></span>
* <span data-ttu-id="90e55-617">Ta bort felaktig instruktion från hjälpen för cmdleten Tag</span><span class="sxs-lookup"><span data-stu-id="90e55-617">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="90e55-618">6.5.0 – juli 2018</span><span class="sxs-lookup"><span data-stu-id="90e55-618">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="90e55-619">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="90e55-619">AzureRM.Profile</span></span>
* <span data-ttu-id="90e55-620">Hjälp för ”Get-AzureRmContextAutosaveSetting” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="90e55-620">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="90e55-621">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="90e55-621">Azure.Storage</span></span>
* <span data-ttu-id="90e55-622">Stöd för uppladdning av blob eller fil med lässkyddad SAS-token</span><span class="sxs-lookup"><span data-stu-id="90e55-622">Support Upload Blob or File with write only Sas token</span></span>
* <span data-ttu-id="90e55-623">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="90e55-623">Set-AzureStorageBlobContent</span></span>
* <span data-ttu-id="90e55-624">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="90e55-624">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="90e55-625">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="90e55-625">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="90e55-626">Lägg till den nödvändiga egenskapen ResourceGroupName i AS.</span><span class="sxs-lookup"><span data-stu-id="90e55-626">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="90e55-627">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="90e55-627">AzureRM.Automation</span></span>
* <span data-ttu-id="90e55-628">Uppdatera hjälp och lägg till exempel för ”New-AzureRMAutomationSchedule”</span><span class="sxs-lookup"><span data-stu-id="90e55-628">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="90e55-629">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="90e55-629">AzureRM.Compute</span></span>
* <span data-ttu-id="90e55-630">Lägg till parametern -Tag förUpdate/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="90e55-630">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="90e55-631">Lägg till exempel för ”Add-AzureRmVmssExtension”</span><span class="sxs-lookup"><span data-stu-id="90e55-631">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="90e55-632">Lägg till exempel för ”Remove-AzureRmVmssExtension”</span><span class="sxs-lookup"><span data-stu-id="90e55-632">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="90e55-633">Uppdatera hjälp för ”Set-AzureRmVMAccessExtension”</span><span class="sxs-lookup"><span data-stu-id="90e55-633">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="90e55-634">Uppdatera SimpleParameterSet för New-AzureRmVmss för att ställa in SinglePlacementGroup på falskt som standard och lägg till växlingsparametern ”SinglePlacementGroup” som gör att användare kan skapa VMSS i en enda placeringsgrupp.</span><span class="sxs-lookup"><span data-stu-id="90e55-634">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="90e55-635">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="90e55-635">AzureRM.EventHub</span></span>
* <span data-ttu-id="90e55-636">En skrivskyddad egenskap, ”PendingReplicationOperationsCount”, har lagts till för klassen PSEventHubDRConfigurationAttributes som anger antalet väntande replikeringsåtgärder medan replikeringen pågår</span><span class="sxs-lookup"><span data-stu-id="90e55-636">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="90e55-637">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="90e55-637">AzureRM.KeyVault</span></span>
* <span data-ttu-id="90e55-638">Uppdatera felmeddelande för Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="90e55-638">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="90e55-639">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="90e55-639">AzureRM.LogicApp</span></span>
* <span data-ttu-id="90e55-640">Felet ”parameteruppsättningen gick inte att matcha” har korrigerats i New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="90e55-640">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="90e55-641">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="90e55-641">AzureRM.Network</span></span>
* <span data-ttu-id="90e55-642">Aktivera peering mellan virtuella nätverk i flera klienter för Set/Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="90e55-642">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="90e55-643">Nedanstående cmdletar för Application Gateway har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="90e55-643">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="90e55-644">New-AzureRmApplicationGateway: EnableFIPS-flagga har lagts till för stöd för zoner</span><span class="sxs-lookup"><span data-stu-id="90e55-644">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="90e55-645">New-AzureRmApplicationGatewaySku: nya SKU:er, Standard_v2 och WAF_v2, har lagts till</span><span class="sxs-lookup"><span data-stu-id="90e55-645">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="90e55-646">Set-AzureRmApplicationGatewaySku: nya SKU:er, Standard_v2 och WAF_v2, har lagts till</span><span class="sxs-lookup"><span data-stu-id="90e55-646">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="90e55-647">RouteTable-cmdletar har återskapats med den senaste versionen av generatorn</span><span class="sxs-lookup"><span data-stu-id="90e55-647">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="90e55-648">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="90e55-648">AzureRM.Relay</span></span>
* <span data-ttu-id="90e55-649">Markdown-filer har uppdaterats och korrigerar problem med parameternamn i exemplet</span><span class="sxs-lookup"><span data-stu-id="90e55-649">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="90e55-650">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="90e55-650">AzureRM.Resources</span></span>
* <span data-ttu-id="90e55-651">Uppdatera cmdletar för rolltilldelning och rolldefinition:</span><span class="sxs-lookup"><span data-stu-id="90e55-651">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="90e55-652">Ta bort extra anrop för rolldefinitioner som görs som en del av sidindelning.</span><span class="sxs-lookup"><span data-stu-id="90e55-652">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="90e55-653">Åtgärda Get-AzureRMRoleAssignment-cmdlet</span><span class="sxs-lookup"><span data-stu-id="90e55-653">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="90e55-654">Åtgärda parameterfunktioner för kommandot -ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="90e55-654">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="90e55-655">Åtgärda problem med ”Get-AzureRmResource” där ”-ResourceType”-parametern var skiftlägeskänsligt</span><span class="sxs-lookup"><span data-stu-id="90e55-655">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="90e55-656">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="90e55-656">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="90e55-657">Parametrar för att stoppa och hoppa över har lagts till i listan över cmdletar</span><span class="sxs-lookup"><span data-stu-id="90e55-657">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="90e55-658">Cmdletar för migrering från Standard- till Premium-namnområden har lagts till:</span><span class="sxs-lookup"><span data-stu-id="90e55-658">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="90e55-659">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="90e55-659">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="90e55-660">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="90e55-660">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="90e55-661">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="90e55-661">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="90e55-662">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="90e55-662">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="90e55-663">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="90e55-663">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="90e55-664">En skrivskyddad egenskap, ”PendingReplicationOperationsCount” har lagts till för klassen PSServiceBusDRConfigurationAttributes som anger antalet väntande replikeringsåtgärder medan replikeringen pågår</span><span class="sxs-lookup"><span data-stu-id="90e55-664">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="90e55-665">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="90e55-665">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="90e55-666">Uppdatera exempel för ”New-AzureRmServiceFabricCluster”</span><span class="sxs-lookup"><span data-stu-id="90e55-666">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="90e55-667">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="90e55-667">AzureRM.Sql</span></span>
* <span data-ttu-id="90e55-668">Nya cmdletar för Management.Sql som gör att kunderna kan lägga till certifikat för transparent datakryptering till SQL Server-instans eller en hanterad instans har lagts till</span><span class="sxs-lookup"><span data-stu-id="90e55-668">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="90e55-669">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="90e55-669">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="90e55-670">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="90e55-670">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="90e55-671">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="90e55-671">AzureRM.Websites</span></span>
* <span data-ttu-id="90e55-672">När `Set-AzureRmWebApp -AssignIdentity` och `Set-AzureRmWebAppSlot -AssignIdentity` är inställda på falskt tar de nu bort identitetsegenskapen från platsobjektet. Även förhandsgranskningstaggen tas bort.</span><span class="sxs-lookup"><span data-stu-id="90e55-672">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="90e55-673">`Get-AzureRmWebAppMetrics`, `Get-AzureRmAppServicePlanMetrics`-exempel har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="90e55-673">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="90e55-674">`Set-AzureRmWebApp -PhpVersion` har stöd för ”av” som en giltig php-version</span><span class="sxs-lookup"><span data-stu-id="90e55-674">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="90e55-675">6.4.0 – juli 2018</span><span class="sxs-lookup"><span data-stu-id="90e55-675">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="90e55-676">Allmänt</span><span class="sxs-lookup"><span data-stu-id="90e55-676">General</span></span>
* <span data-ttu-id="90e55-677">Formatering av OutputType i hjälpfiler har korrigerats för de flesta moduler</span><span class="sxs-lookup"><span data-stu-id="90e55-677">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="90e55-678">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="90e55-678">AzureRM.Profile</span></span>
* <span data-ttu-id="90e55-679">Ps1Xml-attribut har lagts till för grundläggande utdatatyper</span><span class="sxs-lookup"><span data-stu-id="90e55-679">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="90e55-680">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="90e55-680">AzureRM.Compute</span></span>
* <span data-ttu-id="90e55-681">IP-tagg-funktioner för VMSS</span><span class="sxs-lookup"><span data-stu-id="90e55-681">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="90e55-682">"New-AzureRmVmssIpTagConfig"-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="90e55-682">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="90e55-683">IpTag-parameter har lagts till för New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="90e55-683">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="90e55-684">Automatisk återställningsfunktion för operativsystem för VMSS</span><span class="sxs-lookup"><span data-stu-id="90e55-684">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="90e55-685">DisableAutoRollback-parametrar har lagts till för New-AzureRmVmssConfig och Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="90e55-685">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="90e55-686">Funktion för uppgraderingshistorik för operativsystem för Vmss</span><span class="sxs-lookup"><span data-stu-id="90e55-686">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="90e55-687">OSUpgradeHistory-växlingsparametern har lagts till för Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="90e55-687">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="90e55-688">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="90e55-688">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="90e55-689">Lägg till stöd för katalog-ACL:er med hjälp av följande kommandon:</span><span class="sxs-lookup"><span data-stu-id="90e55-689">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="90e55-690">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="90e55-690">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="90e55-691">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="90e55-691">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="90e55-692">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="90e55-692">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="90e55-693">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="90e55-693">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="90e55-694">Lägg till stöd för annullering och förloppsspårning för Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="90e55-694">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="90e55-695">Lägg till stöd för annullering för Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="90e55-695">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="90e55-696">Åtgärda tömning av felsökningsmeddelanden för cmdletar som gör rekursiva åtgärder</span><span class="sxs-lookup"><span data-stu-id="90e55-696">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="90e55-697">Åtgärda platsen för testning av DataLake-cmdletar</span><span class="sxs-lookup"><span data-stu-id="90e55-697">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="90e55-698">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="90e55-698">AzureRM.EventHub</span></span>
* <span data-ttu-id="90e55-699">Parametrar för optimalt maxantal har lagts till i liståtgärds-cmdletarna Get-AzureRmEventHub och Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="90e55-699">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="90e55-700">Ett problem i New-AzureRmEventHub-cmdleten har åtgärdats där minst en parameter behövdes när du skapade en ny EventHub.</span><span class="sxs-lookup"><span data-stu-id="90e55-700">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="90e55-701">Angiven standardparameter har ställts in.</span><span class="sxs-lookup"><span data-stu-id="90e55-701">Provided Default Parameter set.</span></span>
* <span data-ttu-id="90e55-702">Valfri parameter för KeyValue har lagts till för New-AzureRmEventHubKey-cmdleten, vilket gör det möjligt att ange KeyValue.</span><span class="sxs-lookup"><span data-stu-id="90e55-702">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="90e55-703">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="90e55-703">AzureRM.KeyVault</span></span>
* <span data-ttu-id="90e55-704">Åtgärda problem där alla resurser returnerades av Get-AzureRmKeyVault-taggen</span><span class="sxs-lookup"><span data-stu-id="90e55-704">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="90e55-705">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="90e55-705">AzureRM.Network</span></span>
* <span data-ttu-id="90e55-706">Gör nya SKU:er tillgängliga för zonredundanta VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="90e55-706">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="90e55-707">Nya kommandon har lagts till för funktionen: ExpressRoute Partner APIs via ARM</span><span class="sxs-lookup"><span data-stu-id="90e55-707">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="90e55-708">Get-AzureRmExpressRouteCrossConnection har lagts till</span><span class="sxs-lookup"><span data-stu-id="90e55-708">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="90e55-709">Set-AzureRmExpressRouteCrossConnection har lagts till</span><span class="sxs-lookup"><span data-stu-id="90e55-709">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="90e55-710">Add-AzureRmExpressRouteCrossConnectionPeering har lagts till</span><span class="sxs-lookup"><span data-stu-id="90e55-710">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="90e55-711">Get-AzureRmExpressRouteCrossConnectionPeering har lagts till</span><span class="sxs-lookup"><span data-stu-id="90e55-711">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="90e55-712">Remove-AzureRmExpressRouteCrossConnectionPeering har lagts till</span><span class="sxs-lookup"><span data-stu-id="90e55-712">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="90e55-713">Get-AzureRMExpressRouteCrossConnectionArpTable har lagts till</span><span class="sxs-lookup"><span data-stu-id="90e55-713">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="90e55-714">Get-AzureRMExpressRouteCrossConnectionRouteTable har lagts till</span><span class="sxs-lookup"><span data-stu-id="90e55-714">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="90e55-715">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary har lagts till</span><span class="sxs-lookup"><span data-stu-id="90e55-715">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="90e55-716">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="90e55-716">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="90e55-717">Get-AzureRmRecoveryServicesBackupStatus-cmdlet har lagts till.</span><span class="sxs-lookup"><span data-stu-id="90e55-717">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="90e55-718">Denna cmdlet tar ett ID för virtuell dator och kontrollerar om den virtuella datorn skyddas av ett valv i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="90e55-718">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="90e55-719">Om ett sådant valv finns returnerar cmdleten valvinformationen.</span><span class="sxs-lookup"><span data-stu-id="90e55-719">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="90e55-720">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="90e55-720">AzureRM.Resources</span></span>
* <span data-ttu-id="90e55-721">Uppdatera Get-AzureRmPolicyAssignment-cmdletar:</span><span class="sxs-lookup"><span data-stu-id="90e55-721">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="90e55-722">Lägg till stöd för att lista -Scope-värden på hanteringsgruppsnivå</span><span class="sxs-lookup"><span data-stu-id="90e55-722">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="90e55-723">Lägg till stöd för hämtning av enskilda tilldelningar med -Scope-värden på hanteringsgruppsnivå.</span><span class="sxs-lookup"><span data-stu-id="90e55-723">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="90e55-724">Lägg till växlar för -Effective och -All till kontrollparametrar</span><span class="sxs-lookup"><span data-stu-id="90e55-724">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="90e55-725">Uppdatera Get/New/Remove/Set-AzureRmPolicyDefinition-cmdletar</span><span class="sxs-lookup"><span data-stu-id="90e55-725">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="90e55-726">Lägg till parameter för -ManagementGroupName om du vill tillämpa åtgärder för en viss hanteringsgrupp</span><span class="sxs-lookup"><span data-stu-id="90e55-726">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="90e55-727">Lägg till parameter för -SubscriptionId om du vill tillämpa åtgärder för en viss prenumeration</span><span class="sxs-lookup"><span data-stu-id="90e55-727">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="90e55-728">Uppdatera Get/New/Remove/Set-AzureRmPolicySetDefinition-cmdletar</span><span class="sxs-lookup"><span data-stu-id="90e55-728">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="90e55-729">Lägg till parameter för -ManagementGroupName om du vill tillämpa åtgärder för en viss hanteringsgrupp</span><span class="sxs-lookup"><span data-stu-id="90e55-729">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="90e55-730">Lägg till parameter för -SubscriptionId om du vill tillämpa åtgärder för en viss prenumeration</span><span class="sxs-lookup"><span data-stu-id="90e55-730">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="90e55-731">Lägg till stöd för hemliga KeyVault-referenser i parametrar när du använder "TemplateParameterObject" i "New-AzureRmResourceGroupDeployment"</span><span class="sxs-lookup"><span data-stu-id="90e55-731">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="90e55-732">Åtgärda problem med att "-EndDate"-parametern ignorerades på grund av "New-AzureRmADAppCredential"</span><span class="sxs-lookup"><span data-stu-id="90e55-732">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="90e55-733">Åtgärda problem med att felaktig URL användes i "New-AzureRmADAppCredential" vid begäran</span><span class="sxs-lookup"><span data-stu-id="90e55-733">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="90e55-734">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="90e55-734">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="90e55-735">Valfri parameter för -KeyValue har lagts till för New-AzureRmServiceBusKey-cmdleten, vilket gör det möjligt att ange KeyValue.</span><span class="sxs-lookup"><span data-stu-id="90e55-735">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="90e55-736">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="90e55-736">AzureRM.Sql</span></span>
* <span data-ttu-id="90e55-737">Användardefinierade återställningspunkter har klargjorts för SQLDW i New-AzureRmSqlDatabaseRestorePoint-hjälpen</span><span class="sxs-lookup"><span data-stu-id="90e55-737">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="90e55-738">Dokumentationen om parametern -ComputeGeneration har uppdaterats i fler cmdletar</span><span class="sxs-lookup"><span data-stu-id="90e55-738">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="90e55-739">6.3.0 – juni 2018</span><span class="sxs-lookup"><span data-stu-id="90e55-739">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="90e55-740">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="90e55-740">AzureRM.Profile</span></span>
* <span data-ttu-id="90e55-741">Uppdaterade felmeddelanden för Enable-AzureRmContextAutoSave</span><span class="sxs-lookup"><span data-stu-id="90e55-741">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="90e55-742">Skapa en kontext för varje prenumeration när du kör ”Connect-AzureRmAccount” utan tidigare kontext</span><span class="sxs-lookup"><span data-stu-id="90e55-742">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="90e55-743">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="90e55-743">Azure.Storage</span></span>
* <span data-ttu-id="90e55-744">Ytterligare information om parametern -Permissions har lagts till i hjälpfilerna.</span><span class="sxs-lookup"><span data-stu-id="90e55-744">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="90e55-745">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="90e55-745">AzureRM.Compute</span></span>
* <span data-ttu-id="90e55-746">”Get-AzureRmVmDiskEncryptionStatus” korrigerar ett problem för virtuella datorer utan datadiskar</span><span class="sxs-lookup"><span data-stu-id="90e55-746">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="90e55-747">Uppdatera version av klientbibliotek för Compute för att korrigera följande cmdletar</span><span class="sxs-lookup"><span data-stu-id="90e55-747">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="90e55-748">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="90e55-748">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="90e55-749">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="90e55-749">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="90e55-750">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="90e55-750">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="90e55-751">Följande cmdletar har åtgärdats för att visa ”Åtgärds-ID” och ”Åtgärdsstatus” på ett korrekt sätt:</span><span class="sxs-lookup"><span data-stu-id="90e55-751">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="90e55-752">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="90e55-752">Start-AzureRmVM</span></span>
    - <span data-ttu-id="90e55-753">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="90e55-753">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="90e55-754">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="90e55-754">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="90e55-755">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="90e55-755">Set-AzureRmVM</span></span>
    - <span data-ttu-id="90e55-756">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="90e55-756">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="90e55-757">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="90e55-757">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="90e55-758">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="90e55-758">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="90e55-759">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="90e55-759">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="90e55-760">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="90e55-760">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="90e55-761">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="90e55-761">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="90e55-762">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="90e55-762">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="90e55-763">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="90e55-763">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="90e55-764">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="90e55-764">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="90e55-765">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="90e55-765">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="90e55-766">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="90e55-766">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="90e55-767">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="90e55-767">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="90e55-768">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="90e55-768">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="90e55-769">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="90e55-769">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="90e55-770">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="90e55-770">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="90e55-771">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="90e55-771">AzureRM.EventGrid</span></span>
* <span data-ttu-id="90e55-772">Ta bort verifieringsvillkoren ValidateNotNullOrEmpty för SubjectBeginsWith/SubjectEndsWith i cmdleten Update-AzureRmEventGridSubscription för att ändra de här parametrarna till en tom sträng om det behövs.</span><span class="sxs-lookup"><span data-stu-id="90e55-772">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="90e55-773">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="90e55-773">AzureRM.KeyVault</span></span>
* <span data-ttu-id="90e55-774">Åtgärda problem där inga taggar returneras när Get-AzureRmKeyVault -Tag körs</span><span class="sxs-lookup"><span data-stu-id="90e55-774">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="90e55-775">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="90e55-775">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="90e55-776">Offentlig lansering av cmdletar för Policy Insights</span><span class="sxs-lookup"><span data-stu-id="90e55-776">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="90e55-777">Använd API-version 2018-04-04</span><span class="sxs-lookup"><span data-stu-id="90e55-777">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="90e55-778">Lägg till PolicyDefinitionReferenceId i resultaten för Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="90e55-778">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="90e55-779">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="90e55-779">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="90e55-780">Parametern -Vault har lagts till i cmdletarna för RecoveryServices.Backup.</span><span class="sxs-lookup"><span data-stu-id="90e55-780">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="90e55-781">När den godkänns åsidosätts cmdleten Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="90e55-781">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="90e55-782">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="90e55-782">AzureRM.Sql</span></span>
* <span data-ttu-id="90e55-783">Exemplet i hjälpfilen för Get-AzureRmSqlDatabaseExpanded har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="90e55-783">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="90e55-784">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="90e55-784">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="90e55-785">Hjälpfilen för Add-AzureRmTrafficManagerEndpointConfig har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="90e55-785">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="90e55-786">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="90e55-786">AzureRM.Websites</span></span>
* <span data-ttu-id="90e55-787">”Set-AzureRmWebApp” har uppdaterats så att den inte skriver över appinställningarna när du använder -AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="90e55-787">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="90e55-788">”New-AzureRMWebAppSlot” har uppdaterats för att visa att AppServicePlan är en valfri parameter</span><span class="sxs-lookup"><span data-stu-id="90e55-788">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="90e55-789">6.2.1 – juni 2018</span><span class="sxs-lookup"><span data-stu-id="90e55-789">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="90e55-790">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="90e55-790">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="90e55-791">PSWorkspace-modellen har uppdaterats för att tillåta att nätverket använder typ som en parameter</span><span class="sxs-lookup"><span data-stu-id="90e55-791">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="90e55-792">6.2.0 – juni 2018</span><span class="sxs-lookup"><span data-stu-id="90e55-792">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="90e55-793">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="90e55-793">AzureRM.Profile</span></span>
* <span data-ttu-id="90e55-794">Åtgärda problemet med att version 10.0.3 av Newtonsoft.Json inte lästes in vid modulimporten</span><span class="sxs-lookup"><span data-stu-id="90e55-794">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="90e55-795">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="90e55-795">AzureRM.Compute</span></span>
* <span data-ttu-id="90e55-796">VMSS VM-uppdateringsfunktion</span><span class="sxs-lookup"><span data-stu-id="90e55-796">VMSS VM Update feature</span></span>
    - <span data-ttu-id="90e55-797">Cmdletarna Update-AzureRmVmssVM och New-AzureRmVMDataDisk har lagts till</span><span class="sxs-lookup"><span data-stu-id="90e55-797">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="90e55-798">Lägg till parametern VirtualMachineScaleSetVM till cmdleten Add-AzureRmVMDataDisk så att det går att lägga till en datadisk i den virtuella Vmss-datorn.</span><span class="sxs-lookup"><span data-stu-id="90e55-798">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="90e55-799">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="90e55-799">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="90e55-800">SDK:n för ADF .Net har uppdaterats till version 0.8.0-preview som innehåller följande ändringar:</span><span class="sxs-lookup"><span data-stu-id="90e55-800">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="90e55-801">Åtgärden för att konfigurera fabrikslagringsplatsen har lagts till</span><span class="sxs-lookup"><span data-stu-id="90e55-801">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="90e55-802">QuickBooks LinkedService har uppdaterats för att visa egenskaperna consumerKey och consumerSecret</span><span class="sxs-lookup"><span data-stu-id="90e55-802">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="90e55-803">Flera modelltyper från SecretBase till Object har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="90e55-803">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="90e55-804">Utlösaren Blob Events har lagts till</span><span class="sxs-lookup"><span data-stu-id="90e55-804">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="90e55-805">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="90e55-805">AzureRM.KeyVault</span></span>
* <span data-ttu-id="90e55-806">Uppdatera dokumentation med exempel på utdata</span><span class="sxs-lookup"><span data-stu-id="90e55-806">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="90e55-807">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="90e55-807">AzureRM.Network</span></span>
* <span data-ttu-id="90e55-808">Aktivera Trafikanalys-parametrar på Network Watcher-cmdletar</span><span class="sxs-lookup"><span data-stu-id="90e55-808">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="90e55-809">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="90e55-809">AzureRM.Resources</span></span>
* <span data-ttu-id="90e55-810">Åtgärda problemet med egenskapen "Properties" för objekt(en) "PSResource" som returneras från "Get-AzureRmResource"</span><span class="sxs-lookup"><span data-stu-id="90e55-810">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="90e55-811">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="90e55-811">AzureRM.Scheduler</span></span>
* <span data-ttu-id="90e55-812">Åtgärda problemet med att nya autentiseringsvärden inte anges vid uppdatering av ServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="90e55-812">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="90e55-813">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="90e55-813">AzureRM.Sql</span></span>
* <span data-ttu-id="90e55-814">Följande cmdletar har uppdaterats med valfri LicenseType-parameter</span><span class="sxs-lookup"><span data-stu-id="90e55-814">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="90e55-815">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="90e55-815">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="90e55-816">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="90e55-816">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="90e55-817">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="90e55-817">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="90e55-818">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="90e55-818">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="90e55-819">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="90e55-819">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="90e55-820">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="90e55-820">AzureRM.Websites</span></span>
* <span data-ttu-id="90e55-821">New-AzureRMWebApp har uppdaterats för att använda vanliga algoritmer från biblioteket Strategy.</span><span class="sxs-lookup"><span data-stu-id="90e55-821">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="90e55-822">6.1.0 – maj 2018</span><span class="sxs-lookup"><span data-stu-id="90e55-822">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="90e55-823">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="90e55-823">AzureRM.Profile</span></span>
* <span data-ttu-id="90e55-824">Åtgärda problem där en körning av Clear-AzureRmContext skulle bevara en tom kontext med namnet på den föregående standardkontexten som gjorde att användaren inte kunde skapa en ny kontext med det gamla namnet</span><span class="sxs-lookup"><span data-stu-id="90e55-824">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="90e55-825">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="90e55-825">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="90e55-826">Aktivera Gateway associerings- och avassocieringsåtgärder på AS.</span><span class="sxs-lookup"><span data-stu-id="90e55-826">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="90e55-827">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="90e55-827">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="90e55-828">Stöd för ApiVersions, ApiReleases och ApiRevisions har lagts till</span><span class="sxs-lookup"><span data-stu-id="90e55-828">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="90e55-829">Stöd för serverdelen på ServiceFabric har lagts till</span><span class="sxs-lookup"><span data-stu-id="90e55-829">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="90e55-830">Stöd för Application Insights-loggare har lagts till</span><span class="sxs-lookup"><span data-stu-id="90e55-830">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="90e55-831">Stöd för att identifiera SKU:n ”Basic” som en giltig SKU för Api Management-tjänsten har lagts till</span><span class="sxs-lookup"><span data-stu-id="90e55-831">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="90e55-832">Stöd för att installera certifikat som utfärdats av privata certifikatutfärdare som rot eller certifikatutfärdare har lagts till</span><span class="sxs-lookup"><span data-stu-id="90e55-832">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="90e55-833">Stöd för att godkänna anpassade SSL-certifikat via KeyVault och flera proxy-värdnamn har lagts till</span><span class="sxs-lookup"><span data-stu-id="90e55-833">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="90e55-834">Stöd för MSI-identitet har lagts till</span><span class="sxs-lookup"><span data-stu-id="90e55-834">Added support for MSI identity</span></span>
* <span data-ttu-id="90e55-835">Stöd för att godkänna principer via URL har lagts till. Obs! Följande cmdletar blir inaktuella i framtida versioner</span><span class="sxs-lookup"><span data-stu-id="90e55-835">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="90e55-836">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="90e55-836">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="90e55-837">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="90e55-837">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="90e55-838">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="90e55-838">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="90e55-839">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="90e55-839">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="90e55-840">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="90e55-840">AzureRM.Batch</span></span>
* <span data-ttu-id="90e55-841">Släpp nya cmdleten Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="90e55-841">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="90e55-842">Släpp nya cmdleten Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="90e55-842">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="90e55-843">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="90e55-843">AzureRM.Consumption</span></span>
* <span data-ttu-id="90e55-844">Lägg till nya parametrar Expand, ResourceGroup, InstanceName, InstanceId, Tags och Top på cmdleten Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="90e55-844">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="90e55-845">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="90e55-845">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="90e55-846">Åtgärda exempel för Export AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="90e55-846">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="90e55-847">Åtgärda undantag för null-parameter för rekursivt ärende i Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="90e55-847">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="90e55-848">Åtgärda hjälpfilerna för Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="90e55-848">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="90e55-849">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="90e55-849">AzureRM.Network</span></span>
* <span data-ttu-id="90e55-850">Öka nätverkets SDK-version från förhandsversionen 18.0.0 till förhandsversionen 19.0.0</span><span class="sxs-lookup"><span data-stu-id="90e55-850">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="90e55-851">Cmdlet har lagts till för att skapa protokollinformation</span><span class="sxs-lookup"><span data-stu-id="90e55-851">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="90e55-852">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="90e55-852">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="90e55-853">Cmdlet har lagts till för att lägga till en ny kretsanslutning till en befintlig expressroute-krets.</span><span class="sxs-lookup"><span data-stu-id="90e55-853">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="90e55-854">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="90e55-854">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="90e55-855">Cmdlet har lagts till för att ta bort en kretsanslutning från en befintlig expressroute-krets.</span><span class="sxs-lookup"><span data-stu-id="90e55-855">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="90e55-856">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="90e55-856">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="90e55-857">Cmdlet har lagts till för att hämta en kretsanslutning</span><span class="sxs-lookup"><span data-stu-id="90e55-857">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="90e55-858">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="90e55-858">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="90e55-859">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="90e55-859">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="90e55-860">Användning med serverautentisering med genererade certifikat (problem #5998) har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="90e55-860">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="90e55-861">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="90e55-861">AzureRM.Sql</span></span>
* <span data-ttu-id="90e55-862">Cmdletar för granskning för att ta bort AuditActions eller AuditActionGroups har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="90e55-862">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="90e55-863">Åtgärdade problem med Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy vid konfigurering av en ny flexibel bevarandeprincip där kommandot misslyckas med ett meddelande om att konfigurering av långsiktig bevarandeprincip med Azure Recovery Service-valv och principen inte längre stöds,</span><span class="sxs-lookup"><span data-stu-id="90e55-863">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="90e55-864">och att en begäran med den nya flexibla bevarandeprincipen ska skickas.</span><span class="sxs-lookup"><span data-stu-id="90e55-864">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="90e55-865">Uppdatera alla Azure Sql Database/ElasticPool Creation/Update-relaterade cmdletar för att använda det nya databas-API:et som stöder SKU-egenskaper för skalnings- och nivårelaterade egenskaper.</span><span class="sxs-lookup"><span data-stu-id="90e55-865">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="90e55-866">Cmdletar har uppdaterats, inklusive:</span><span class="sxs-lookup"><span data-stu-id="90e55-866">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="90e55-867">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="90e55-867">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="90e55-868">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="90e55-868">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="90e55-869">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="90e55-869">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="90e55-870">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="90e55-870">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="90e55-871">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="90e55-871">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="90e55-872">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="90e55-872">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="90e55-873">Uppdatera parametrarna för Get-AzureRmTrafficManagerProfile så att ResourceGroupName-parametern blir obligatorisk när du använder Name-parametern.</span><span class="sxs-lookup"><span data-stu-id="90e55-873">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
