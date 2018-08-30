---
title: Ändringslogg för Azure PowerShell | Microsoft Docs
description: Det här är en historik över de ändringar som gjorts i den senaste versionen av Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 5/1/2018
ms.openlocfilehash: 340c1d2d28e1b97cdd2ec98033361eb00b4302da
ms.sourcegitcommit: 72086f8d368ec84bd403e802305acfc336c08978
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/14/2018
ms.locfileid: "43018783"
---
# <a name="release-notes"></a><span data-ttu-id="378f7-103">Viktig information</span><span class="sxs-lookup"><span data-stu-id="378f7-103">Release notes</span></span>

<span data-ttu-id="378f7-104">Det här är en lista över ändringar som har gjorts i Azure PowerShell i den här versionen.</span><span class="sxs-lookup"><span data-stu-id="378f7-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="660---july-2018"></a><span data-ttu-id="378f7-105">6.6.0 – juli 2018</span><span class="sxs-lookup"><span data-stu-id="378f7-105">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="378f7-106">Allmänt</span><span class="sxs-lookup"><span data-stu-id="378f7-106">General</span></span>
* <span data-ttu-id="378f7-107">Alla hjälpfiler har uppdaterats för att ta med fullständiga parametertyper och korrekta indata-/utdatatyper.</span><span class="sxs-lookup"><span data-stu-id="378f7-107">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="378f7-108">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="378f7-108">AzureRM.Profile</span></span>
* <span data-ttu-id="378f7-109">Common.Strategy-biblioteket har uppdaterats för att kunna verifiera att den aktuella konfigurationsfilen för en resurs är kompatibel med målresursen.</span><span class="sxs-lookup"><span data-stu-id="378f7-109">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="378f7-110">ps1xml-typer har lagts till i Common.Storage</span><span class="sxs-lookup"><span data-stu-id="378f7-110">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="378f7-111">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="378f7-111">Azure.Storage</span></span>
* <span data-ttu-id="378f7-112">Lade till stöd för hämtning av lagringskontext från DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="378f7-112">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="378f7-113">Lade till Ps1XmlAttribute till utdatatypegenskaper för cmdletar.</span><span class="sxs-lookup"><span data-stu-id="378f7-113">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="378f7-114">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="378f7-114">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="378f7-115">Åtgärdat problem https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="378f7-115">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="378f7-116">En bugg har åtgärdats i Automapper för att översätta PsApiManagementApi till ApiContract</span><span class="sxs-lookup"><span data-stu-id="378f7-116">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="378f7-117">Åtgärdat problem https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="378f7-117">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="378f7-118">En bugg har åtgärdats i File.Save för att inte överbelasta kodningstypen</span><span class="sxs-lookup"><span data-stu-id="378f7-118">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="378f7-119">Åtgärdat problem https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="378f7-119">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="378f7-120">Har uppgraderats till Nuget-versionen 4.0.3 vilket åtgärdar mönsterundantaget på apiId</span><span class="sxs-lookup"><span data-stu-id="378f7-120">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="378f7-121">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="378f7-121">AzureRM.Compute</span></span>
* <span data-ttu-id="378f7-122">Åtgärda problem med fel vid skapandet av en virtuell dator med hjälp av DiskFileParameterSet i New-AzureRmVm på grund av namnbyte på PremiumLRS-lagringskontotypen.</span><span class="sxs-lookup"><span data-stu-id="378f7-122">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="378f7-123">Åtgärda cmdleten Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="378f7-123">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="378f7-124">Uppdatera Get-AzureRmAvailabilitySet för att aktivera funktionen för att lista alla tillgänglighetsuppsättningar i en prenumeration.</span><span class="sxs-lookup"><span data-stu-id="378f7-124">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="378f7-125">(Parametern ResouceGroupName är nu frivillig.)</span><span class="sxs-lookup"><span data-stu-id="378f7-125">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="378f7-126">Uppdatera SimpleParameterSet för "New-AzureRmVm" för att aktivera accelererat nätverk på berättigade virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="378f7-126">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="378f7-127">Uppdatera den enkla parameteruppsättningen för New-AzureRmVmss så att det inte går att skapa de virtuella datorerna när en användarangiven lastbalanserare redan finns.</span><span class="sxs-lookup"><span data-stu-id="378f7-127">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="378f7-128">Uppdatera exempel för New-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="378f7-128">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="378f7-129">Lägg till exempel för "New-AzureRmVM"</span><span class="sxs-lookup"><span data-stu-id="378f7-129">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="378f7-130">Uppdatera beskrivning för Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="378f7-130">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="378f7-131">Uppdatera Exempel 1 för Set-AzureRmVMBginfoExtension för stavningskontroll och prefix.</span><span class="sxs-lookup"><span data-stu-id="378f7-131">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="378f7-132">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="378f7-132">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="378f7-133">ADF .Net SDK-versionen har uppdaterats till 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="378f7-133">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="378f7-134">Stöd för delning av Integration Runtime (lokal installation) mellan datafabriker.</span><span class="sxs-lookup"><span data-stu-id="378f7-134">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="378f7-135">Lägg till ny parameter – SharedIntegrationRuntimeResourceId i cmdleten Set-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="378f7-135">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="378f7-136">Lägg till ny valfri parameter – LinkedDataFactoryName i cmdleten Remove-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="378f7-136">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="378f7-137">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="378f7-137">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="378f7-138">DataPlane SDK-versionen (Microsoft.Azure.DataLake.Store) har uppdaterats till 1.1.9</span><span class="sxs-lookup"><span data-stu-id="378f7-138">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="378f7-139">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="378f7-139">AzureRM.EventHub</span></span>
* <span data-ttu-id="378f7-140">Piping för InputObject and ResourceId i borttagna cmdletar har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="378f7-140">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="378f7-141">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="378f7-141">AzureRM.Insights</span></span>
* <span data-ttu-id="378f7-142">Formatering har åtgärdats för OutputType i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="378f7-142">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="378f7-143">Använda Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span><span class="sxs-lookup"><span data-stu-id="378f7-143">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="378f7-144">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="378f7-144">AzureRM.KeyVault</span></span>
* <span data-ttu-id="378f7-145">Åtgärda problem med piping i Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="378f7-145">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="378f7-146">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="378f7-146">AzureRM.Network</span></span>
* <span data-ttu-id="378f7-147">Exempel har lagts till för LoadBalancerInboundNatPoolConfig-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="378f7-147">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="378f7-148">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="378f7-148">AzureRM.Resources</span></span>
* <span data-ttu-id="378f7-149">Åtgärda problem när både taggnamn och värde anges för "Get-AzureRmResource"</span><span class="sxs-lookup"><span data-stu-id="378f7-149">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="378f7-150">Åtgärda pipingscenario med "Set-AzureRmResource"</span><span class="sxs-lookup"><span data-stu-id="378f7-150">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="378f7-151">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="378f7-151">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="378f7-152">Piping för InputObject and ResourceId i borttagna cmdletar har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="378f7-152">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="378f7-153">några problem har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="378f7-153">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="378f7-154">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="378f7-154">AzureRM.Sql</span></span>
* <span data-ttu-id="378f7-155">Lägg till stöd för Server Advanced Threat Protection med följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="378f7-155">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="378f7-156">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="378f7-156">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="378f7-157">Lägg till stöd för Sårbarhetsbedömning med följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="378f7-157">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="378f7-158">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="378f7-158">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="378f7-159">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="378f7-159">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="378f7-160">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="378f7-160">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="378f7-161">Exempel i Remove-AzureRmSqlServerFirewallRule har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="378f7-161">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="378f7-162">Åtgärda felaktig hantering av datum och tid för andra kulturer än usa-baserade kulturer i Get-AzureSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="378f7-162">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="378f7-163">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="378f7-163">AzureRM.Storage</span></span>
* <span data-ttu-id="378f7-164">Lägg till Ps1XmlAttribute i utdatatypegenskaper för cmdletar</span><span class="sxs-lookup"><span data-stu-id="378f7-164">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="378f7-165">Visa utdata för cmdleten StorageAccount i tabellvyn</span><span class="sxs-lookup"><span data-stu-id="378f7-165">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="378f7-166">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="378f7-166">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="378f7-167">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="378f7-167">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="378f7-168">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="378f7-168">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="378f7-169">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="378f7-169">AzureRM.Tags</span></span>
* <span data-ttu-id="378f7-170">Ta bort felaktig instruktion från hjälpen för cmdleten Tag</span><span class="sxs-lookup"><span data-stu-id="378f7-170">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="378f7-171">6.5.0 – juli 2018</span><span class="sxs-lookup"><span data-stu-id="378f7-171">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="378f7-172">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="378f7-172">AzureRM.Profile</span></span>
* <span data-ttu-id="378f7-173">Hjälp för ”Get-AzureRmContextAutosaveSetting” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="378f7-173">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="378f7-174">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="378f7-174">Azure.Storage</span></span>
* <span data-ttu-id="378f7-175">Stöd för uppladdning av blob eller fil med lässkyddad SAS-token</span><span class="sxs-lookup"><span data-stu-id="378f7-175">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="378f7-176">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="378f7-176">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="378f7-177">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="378f7-177">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="378f7-178">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="378f7-178">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="378f7-179">Lägg till den nödvändiga egenskapen ResourceGroupName i AS.</span><span class="sxs-lookup"><span data-stu-id="378f7-179">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="378f7-180">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="378f7-180">AzureRM.Automation</span></span>
* <span data-ttu-id="378f7-181">Uppdatera hjälp och lägg till exempel för ”New-AzureRMAutomationSchedule”</span><span class="sxs-lookup"><span data-stu-id="378f7-181">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="378f7-182">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="378f7-182">AzureRM.Compute</span></span>
* <span data-ttu-id="378f7-183">Lägg till parametern -Tag förUpdate/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="378f7-183">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="378f7-184">Lägg till exempel för ”Add-AzureRmVmssExtension”</span><span class="sxs-lookup"><span data-stu-id="378f7-184">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="378f7-185">Lägg till exempel för ”Remove-AzureRmVmssExtension”</span><span class="sxs-lookup"><span data-stu-id="378f7-185">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="378f7-186">Uppdatera hjälp för ”Set-AzureRmVMAccessExtension”</span><span class="sxs-lookup"><span data-stu-id="378f7-186">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="378f7-187">Uppdatera SimpleParameterSet för New-AzureRmVmss för att ställa in SinglePlacementGroup på falskt som standard och lägg till växlingsparametern ”SinglePlacementGroup” som gör att användare kan skapa VMSS i en enda placeringsgrupp.</span><span class="sxs-lookup"><span data-stu-id="378f7-187">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="378f7-188">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="378f7-188">AzureRM.EventHub</span></span>
* <span data-ttu-id="378f7-189">En skrivskyddad egenskap, ”PendingReplicationOperationsCount”, har lagts till för klassen PSEventHubDRConfigurationAttributes som anger antalet väntande replikeringsåtgärder medan replikeringen pågår</span><span class="sxs-lookup"><span data-stu-id="378f7-189">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="378f7-190">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="378f7-190">AzureRM.KeyVault</span></span>
* <span data-ttu-id="378f7-191">Uppdatera felmeddelande för Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="378f7-191">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="378f7-192">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="378f7-192">AzureRM.LogicApp</span></span>
* <span data-ttu-id="378f7-193">Felet ”parameteruppsättningen gick inte att matcha” har korrigerats i New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="378f7-193">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="378f7-194">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="378f7-194">AzureRM.Network</span></span>
* <span data-ttu-id="378f7-195">Aktivera peering mellan virtuella nätverk i flera klienter för Set/Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="378f7-195">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="378f7-196">Nedanstående cmdletar för Application Gateway har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="378f7-196">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="378f7-197">New-AzureRmApplicationGateway: EnableFIPS-flagga har lagts till för stöd för zoner</span><span class="sxs-lookup"><span data-stu-id="378f7-197">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="378f7-198">New-AzureRmApplicationGatewaySku: nya SKU:er, Standard_v2 och WAF_v2, har lagts till</span><span class="sxs-lookup"><span data-stu-id="378f7-198">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="378f7-199">Set-AzureRmApplicationGatewaySku: nya SKU:er, Standard_v2 och WAF_v2, har lagts till</span><span class="sxs-lookup"><span data-stu-id="378f7-199">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="378f7-200">RouteTable-cmdletar har återskapats med den senaste versionen av generatorn</span><span class="sxs-lookup"><span data-stu-id="378f7-200">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="378f7-201">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="378f7-201">AzureRM.Relay</span></span>
* <span data-ttu-id="378f7-202">Markdown-filer har uppdaterats och korrigerar problem med parameternamn i exemplet</span><span class="sxs-lookup"><span data-stu-id="378f7-202">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="378f7-203">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="378f7-203">AzureRM.Resources</span></span>
* <span data-ttu-id="378f7-204">Uppdatera cmdletar för rolltilldelning och rolldefinition:</span><span class="sxs-lookup"><span data-stu-id="378f7-204">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="378f7-205">Ta bort extra anrop för rolldefinitioner som görs som en del av sidindelning.</span><span class="sxs-lookup"><span data-stu-id="378f7-205">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="378f7-206">Åtgärda Get-AzureRMRoleAssignment-cmdlet</span><span class="sxs-lookup"><span data-stu-id="378f7-206">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="378f7-207">Åtgärda parameterfunktioner för kommandot -ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="378f7-207">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="378f7-208">Åtgärda problem med ”Get-AzureRmResource” där ”-ResourceType”-parametern var skiftlägeskänsligt</span><span class="sxs-lookup"><span data-stu-id="378f7-208">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="378f7-209">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="378f7-209">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="378f7-210">Parametrar för att stoppa och hoppa över har lagts till i listan över cmdletar</span><span class="sxs-lookup"><span data-stu-id="378f7-210">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="378f7-211">Cmdletar för migrering från Standard- till Premium-namnområden har lagts till:</span><span class="sxs-lookup"><span data-stu-id="378f7-211">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="378f7-212">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="378f7-212">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="378f7-213">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="378f7-213">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="378f7-214">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="378f7-214">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="378f7-215">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="378f7-215">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="378f7-216">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="378f7-216">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="378f7-217">En skrivskyddad egenskap, ”PendingReplicationOperationsCount” har lagts till för klassen PSServiceBusDRConfigurationAttributes som anger antalet väntande replikeringsåtgärder medan replikeringen pågår</span><span class="sxs-lookup"><span data-stu-id="378f7-217">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="378f7-218">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="378f7-218">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="378f7-219">Uppdatera exempel för ”New-AzureRmServiceFabricCluster”</span><span class="sxs-lookup"><span data-stu-id="378f7-219">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="378f7-220">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="378f7-220">AzureRM.Sql</span></span>
* <span data-ttu-id="378f7-221">Nya cmdletar för Management.Sql som gör att kunderna kan lägga till certifikat för transparent datakryptering till SQL Server-instans eller en hanterad instans har lagts till</span><span class="sxs-lookup"><span data-stu-id="378f7-221">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="378f7-222">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="378f7-222">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="378f7-223">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="378f7-223">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="378f7-224">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="378f7-224">AzureRM.Websites</span></span>
* <span data-ttu-id="378f7-225">När `Set-AzureRmWebApp -AssignIdentity` och `Set-AzureRmWebAppSlot -AssignIdentity` är inställda på falskt tar de nu bort identitetsegenskapen från platsobjektet. Även förhandsgranskningstaggen tas bort.</span><span class="sxs-lookup"><span data-stu-id="378f7-225">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="378f7-226">`Get-AzureRmWebAppMetrics`, `Get-AzureRmAppServicePlanMetrics`-exempel har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="378f7-226">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="378f7-227">`Set-AzureRmWebApp -PhpVersion` har stöd för ”av” som en giltig php-version</span><span class="sxs-lookup"><span data-stu-id="378f7-227">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="378f7-228">6.4.0 – juli 2018</span><span class="sxs-lookup"><span data-stu-id="378f7-228">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="378f7-229">Allmänt</span><span class="sxs-lookup"><span data-stu-id="378f7-229">General</span></span>
* <span data-ttu-id="378f7-230">Formatering av OutputType i hjälpfiler har korrigerats för de flesta moduler</span><span class="sxs-lookup"><span data-stu-id="378f7-230">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="378f7-231">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="378f7-231">AzureRM.Profile</span></span>
* <span data-ttu-id="378f7-232">Ps1Xml-attribut har lagts till för grundläggande utdatatyper</span><span class="sxs-lookup"><span data-stu-id="378f7-232">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="378f7-233">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="378f7-233">AzureRM.Compute</span></span>
* <span data-ttu-id="378f7-234">IP-tagg-funktioner för VMSS</span><span class="sxs-lookup"><span data-stu-id="378f7-234">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="378f7-235">"New-AzureRmVmssIpTagConfig"-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="378f7-235">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="378f7-236">IpTag-parameter har lagts till för New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="378f7-236">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="378f7-237">Automatisk återställningsfunktion för operativsystem för VMSS</span><span class="sxs-lookup"><span data-stu-id="378f7-237">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="378f7-238">DisableAutoRollback-parametrar har lagts till för New-AzureRmVmssConfig och Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="378f7-238">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="378f7-239">Funktion för uppgraderingshistorik för operativsystem för Vmss</span><span class="sxs-lookup"><span data-stu-id="378f7-239">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="378f7-240">OSUpgradeHistory-växlingsparametern har lagts till för Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="378f7-240">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="378f7-241">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="378f7-241">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="378f7-242">Lägg till stöd för katalog-ACL:er med hjälp av följande kommandon:</span><span class="sxs-lookup"><span data-stu-id="378f7-242">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="378f7-243">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="378f7-243">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="378f7-244">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="378f7-244">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="378f7-245">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="378f7-245">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="378f7-246">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="378f7-246">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="378f7-247">Lägg till stöd för annullering och förloppsspårning för Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="378f7-247">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="378f7-248">Lägg till stöd för annullering för Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="378f7-248">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="378f7-249">Åtgärda tömning av felsökningsmeddelanden för cmdletar som gör rekursiva åtgärder</span><span class="sxs-lookup"><span data-stu-id="378f7-249">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="378f7-250">Åtgärda platsen för testning av DataLake-cmdletar</span><span class="sxs-lookup"><span data-stu-id="378f7-250">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="378f7-251">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="378f7-251">AzureRM.EventHub</span></span>
* <span data-ttu-id="378f7-252">Parametrar för optimalt maxantal har lagts till i liståtgärds-cmdletarna Get-AzureRmEventHub och Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="378f7-252">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="378f7-253">Ett problem i New-AzureRmEventHub-cmdleten har åtgärdats där minst en parameter behövdes när du skapade en ny EventHub.</span><span class="sxs-lookup"><span data-stu-id="378f7-253">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="378f7-254">Angiven standardparameter har ställts in.</span><span class="sxs-lookup"><span data-stu-id="378f7-254">Provided Default Parameter set.</span></span>
* <span data-ttu-id="378f7-255">Valfri parameter för KeyValue har lagts till för New-AzureRmEventHubKey-cmdleten, vilket gör det möjligt att ange KeyValue.</span><span class="sxs-lookup"><span data-stu-id="378f7-255">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="378f7-256">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="378f7-256">AzureRM.KeyVault</span></span>
* <span data-ttu-id="378f7-257">Åtgärda problem där alla resurser returnerades av Get-AzureRmKeyVault-taggen</span><span class="sxs-lookup"><span data-stu-id="378f7-257">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="378f7-258">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="378f7-258">AzureRM.Network</span></span>
* <span data-ttu-id="378f7-259">Gör nya SKU:er tillgängliga för zonredundanta VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="378f7-259">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="378f7-260">Nya kommandon har lagts till för funktionen: ExpressRoute Partner APIs via ARM</span><span class="sxs-lookup"><span data-stu-id="378f7-260">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="378f7-261">Get-AzureRmExpressRouteCrossConnection har lagts till</span><span class="sxs-lookup"><span data-stu-id="378f7-261">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="378f7-262">Set-AzureRmExpressRouteCrossConnection har lagts till</span><span class="sxs-lookup"><span data-stu-id="378f7-262">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="378f7-263">Add-AzureRmExpressRouteCrossConnectionPeering har lagts till</span><span class="sxs-lookup"><span data-stu-id="378f7-263">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="378f7-264">Get-AzureRmExpressRouteCrossConnectionPeering har lagts till</span><span class="sxs-lookup"><span data-stu-id="378f7-264">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="378f7-265">Remove-AzureRmExpressRouteCrossConnectionPeering har lagts till</span><span class="sxs-lookup"><span data-stu-id="378f7-265">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="378f7-266">Get-AzureRMExpressRouteCrossConnectionArpTable har lagts till</span><span class="sxs-lookup"><span data-stu-id="378f7-266">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="378f7-267">Get-AzureRMExpressRouteCrossConnectionRouteTable har lagts till</span><span class="sxs-lookup"><span data-stu-id="378f7-267">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="378f7-268">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary har lagts till</span><span class="sxs-lookup"><span data-stu-id="378f7-268">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="378f7-269">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="378f7-269">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="378f7-270">Get-AzureRmRecoveryServicesBackupStatus-cmdlet har lagts till.</span><span class="sxs-lookup"><span data-stu-id="378f7-270">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="378f7-271">Denna cmdlet tar ett ID för virtuell dator och kontrollerar om den virtuella datorn skyddas av ett valv i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="378f7-271">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="378f7-272">Om ett sådant valv finns returnerar cmdleten valvinformationen.</span><span class="sxs-lookup"><span data-stu-id="378f7-272">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="378f7-273">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="378f7-273">AzureRM.Resources</span></span>
* <span data-ttu-id="378f7-274">Uppdatera Get-AzureRmPolicyAssignment-cmdletar:</span><span class="sxs-lookup"><span data-stu-id="378f7-274">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="378f7-275">Lägg till stöd för att lista -Scope-värden på hanteringsgruppsnivå</span><span class="sxs-lookup"><span data-stu-id="378f7-275">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="378f7-276">Lägg till stöd för hämtning av enskilda tilldelningar med -Scope-värden på hanteringsgruppsnivå.</span><span class="sxs-lookup"><span data-stu-id="378f7-276">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="378f7-277">Lägg till växlar för -Effective och -All till kontrollparametrar</span><span class="sxs-lookup"><span data-stu-id="378f7-277">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="378f7-278">Uppdatera Get/New/Remove/Set-AzureRmPolicyDefinition-cmdletar</span><span class="sxs-lookup"><span data-stu-id="378f7-278">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="378f7-279">Lägg till parameter för -ManagementGroupName om du vill tillämpa åtgärder för en viss hanteringsgrupp</span><span class="sxs-lookup"><span data-stu-id="378f7-279">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="378f7-280">Lägg till parameter för -SubscriptionId om du vill tillämpa åtgärder för en viss prenumeration</span><span class="sxs-lookup"><span data-stu-id="378f7-280">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="378f7-281">Uppdatera Get/New/Remove/Set-AzureRmPolicySetDefinition-cmdletar</span><span class="sxs-lookup"><span data-stu-id="378f7-281">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="378f7-282">Lägg till parameter för -ManagementGroupName om du vill tillämpa åtgärder för en viss hanteringsgrupp</span><span class="sxs-lookup"><span data-stu-id="378f7-282">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="378f7-283">Lägg till parameter för -SubscriptionId om du vill tillämpa åtgärder för en viss prenumeration</span><span class="sxs-lookup"><span data-stu-id="378f7-283">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="378f7-284">Lägg till stöd för hemliga KeyVault-referenser i parametrar när du använder "TemplateParameterObject" i "New-AzureRmResourceGroupDeployment"</span><span class="sxs-lookup"><span data-stu-id="378f7-284">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="378f7-285">Åtgärda problem med att "-EndDate"-parametern ignorerades på grund av "New-AzureRmADAppCredential"</span><span class="sxs-lookup"><span data-stu-id="378f7-285">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="378f7-286">Åtgärda problem med att felaktig URL användes i "New-AzureRmADAppCredential" vid begäran</span><span class="sxs-lookup"><span data-stu-id="378f7-286">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="378f7-287">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="378f7-287">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="378f7-288">Valfri parameter för -KeyValue har lagts till för New-AzureRmServiceBusKey-cmdleten, vilket gör det möjligt att ange KeyValue.</span><span class="sxs-lookup"><span data-stu-id="378f7-288">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="378f7-289">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="378f7-289">AzureRM.Sql</span></span>
* <span data-ttu-id="378f7-290">Användardefinierade återställningspunkter har klargjorts för SQLDW i New-AzureRmSqlDatabaseRestorePoint-hjälpen</span><span class="sxs-lookup"><span data-stu-id="378f7-290">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="378f7-291">Dokumentationen om parametern -ComputeGeneration har uppdaterats i fler cmdletar</span><span class="sxs-lookup"><span data-stu-id="378f7-291">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="378f7-292">6.3.0 – juni 2018</span><span class="sxs-lookup"><span data-stu-id="378f7-292">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="378f7-293">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="378f7-293">AzureRM.Profile</span></span>
* <span data-ttu-id="378f7-294">Uppdaterade felmeddelanden för Enable-AzureRmContextAutoSave</span><span class="sxs-lookup"><span data-stu-id="378f7-294">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="378f7-295">Skapa en kontext för varje prenumeration när du kör ”Connect-AzureRmAccount” utan tidigare kontext</span><span class="sxs-lookup"><span data-stu-id="378f7-295">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="378f7-296">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="378f7-296">Azure.Storage</span></span>
* <span data-ttu-id="378f7-297">Ytterligare information om parametern -Permissions har lagts till i hjälpfilerna.</span><span class="sxs-lookup"><span data-stu-id="378f7-297">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="378f7-298">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="378f7-298">AzureRM.Compute</span></span>
* <span data-ttu-id="378f7-299">”Get-AzureRmVmDiskEncryptionStatus” korrigerar ett problem för virtuella datorer utan datadiskar</span><span class="sxs-lookup"><span data-stu-id="378f7-299">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="378f7-300">Uppdatera version av klientbibliotek för Compute för att korrigera följande cmdletar</span><span class="sxs-lookup"><span data-stu-id="378f7-300">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="378f7-301">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="378f7-301">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="378f7-302">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="378f7-302">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="378f7-303">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="378f7-303">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="378f7-304">Följande cmdletar har åtgärdats för att visa ”Åtgärds-ID” och ”Åtgärdsstatus” på ett korrekt sätt:</span><span class="sxs-lookup"><span data-stu-id="378f7-304">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="378f7-305">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="378f7-305">Start-AzureRmVM</span></span>
    - <span data-ttu-id="378f7-306">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="378f7-306">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="378f7-307">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="378f7-307">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="378f7-308">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="378f7-308">Set-AzureRmVM</span></span>
    - <span data-ttu-id="378f7-309">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="378f7-309">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="378f7-310">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="378f7-310">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="378f7-311">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="378f7-311">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="378f7-312">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="378f7-312">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="378f7-313">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="378f7-313">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="378f7-314">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="378f7-314">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="378f7-315">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="378f7-315">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="378f7-316">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="378f7-316">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="378f7-317">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="378f7-317">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="378f7-318">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="378f7-318">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="378f7-319">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="378f7-319">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="378f7-320">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="378f7-320">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="378f7-321">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="378f7-321">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="378f7-322">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="378f7-322">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="378f7-323">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="378f7-323">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="378f7-324">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="378f7-324">AzureRM.EventGrid</span></span>
* <span data-ttu-id="378f7-325">Ta bort verifieringsvillkoren ValidateNotNullOrEmpty för SubjectBeginsWith/SubjectEndsWith i cmdleten Update-AzureRmEventGridSubscription för att ändra de här parametrarna till en tom sträng om det behövs.</span><span class="sxs-lookup"><span data-stu-id="378f7-325">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="378f7-326">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="378f7-326">AzureRM.KeyVault</span></span>
* <span data-ttu-id="378f7-327">Åtgärda problem där inga taggar returneras när Get-AzureRmKeyVault -Tag körs</span><span class="sxs-lookup"><span data-stu-id="378f7-327">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="378f7-328">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="378f7-328">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="378f7-329">Offentlig lansering av cmdletar för Policy Insights</span><span class="sxs-lookup"><span data-stu-id="378f7-329">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="378f7-330">Använd API-version 2018-04-04</span><span class="sxs-lookup"><span data-stu-id="378f7-330">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="378f7-331">Lägg till PolicyDefinitionReferenceId i resultaten för Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="378f7-331">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="378f7-332">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="378f7-332">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="378f7-333">Parametern -Vault har lagts till i cmdletarna för RecoveryServices.Backup.</span><span class="sxs-lookup"><span data-stu-id="378f7-333">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="378f7-334">När den godkänns åsidosätts cmdleten Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="378f7-334">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="378f7-335">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="378f7-335">AzureRM.Sql</span></span>
* <span data-ttu-id="378f7-336">Exemplet i hjälpfilen för Get-AzureRmSqlDatabaseExpanded har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="378f7-336">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="378f7-337">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="378f7-337">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="378f7-338">Hjälpfilen för Add-AzureRmTrafficManagerEndpointConfig har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="378f7-338">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="378f7-339">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="378f7-339">AzureRM.Websites</span></span>
* <span data-ttu-id="378f7-340">”Set-AzureRmWebApp” har uppdaterats så att den inte skriver över appinställningarna när du använder -AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="378f7-340">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="378f7-341">”New-AzureRMWebAppSlot” har uppdaterats för att visa att AppServicePlan är en valfri parameter</span><span class="sxs-lookup"><span data-stu-id="378f7-341">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="378f7-342">6.2.1 – juni 2018</span><span class="sxs-lookup"><span data-stu-id="378f7-342">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="378f7-343">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="378f7-343">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="378f7-344">PSWorkspace-modellen har uppdaterats för att tillåta att nätverket använder typ som en parameter</span><span class="sxs-lookup"><span data-stu-id="378f7-344">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="378f7-345">6.2.0 – juni 2018</span><span class="sxs-lookup"><span data-stu-id="378f7-345">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="378f7-346">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="378f7-346">AzureRM.Profile</span></span>
* <span data-ttu-id="378f7-347">Åtgärda problemet med att version 10.0.3 av Newtonsoft.Json inte lästes in vid modulimporten</span><span class="sxs-lookup"><span data-stu-id="378f7-347">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="378f7-348">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="378f7-348">AzureRM.Compute</span></span>
* <span data-ttu-id="378f7-349">VMSS VM-uppdateringsfunktion</span><span class="sxs-lookup"><span data-stu-id="378f7-349">VMSS VM Update feature</span></span>
    - <span data-ttu-id="378f7-350">Cmdletarna Update-AzureRmVmssVM och New-AzureRmVMDataDisk har lagts till</span><span class="sxs-lookup"><span data-stu-id="378f7-350">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="378f7-351">Lägg till parametern VirtualMachineScaleSetVM till cmdleten Add-AzureRmVMDataDisk så att det går att lägga till en datadisk i den virtuella Vmss-datorn.</span><span class="sxs-lookup"><span data-stu-id="378f7-351">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="378f7-352">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="378f7-352">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="378f7-353">SDK:n för ADF .Net har uppdaterats till version 0.8.0-preview som innehåller följande ändringar:</span><span class="sxs-lookup"><span data-stu-id="378f7-353">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="378f7-354">Åtgärden för att konfigurera fabrikslagringsplatsen har lagts till</span><span class="sxs-lookup"><span data-stu-id="378f7-354">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="378f7-355">QuickBooks LinkedService har uppdaterats för att visa egenskaperna consumerKey och consumerSecret</span><span class="sxs-lookup"><span data-stu-id="378f7-355">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="378f7-356">Flera modelltyper från SecretBase till Object har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="378f7-356">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="378f7-357">Utlösaren Blob Events har lagts till</span><span class="sxs-lookup"><span data-stu-id="378f7-357">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="378f7-358">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="378f7-358">AzureRM.KeyVault</span></span>
* <span data-ttu-id="378f7-359">Uppdatera dokumentation med exempel på utdata</span><span class="sxs-lookup"><span data-stu-id="378f7-359">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="378f7-360">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="378f7-360">AzureRM.Network</span></span>
* <span data-ttu-id="378f7-361">Aktivera Trafikanalys-parametrar på Network Watcher-cmdletar</span><span class="sxs-lookup"><span data-stu-id="378f7-361">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="378f7-362">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="378f7-362">AzureRM.Resources</span></span>
* <span data-ttu-id="378f7-363">Åtgärda problemet med egenskapen "Properties" för objekt(en) "PSResource" som returneras från "Get-AzureRmResource"</span><span class="sxs-lookup"><span data-stu-id="378f7-363">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="378f7-364">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="378f7-364">AzureRM.Scheduler</span></span>
* <span data-ttu-id="378f7-365">Åtgärda problemet med att nya autentiseringsvärden inte anges vid uppdatering av ServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="378f7-365">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="378f7-366">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="378f7-366">AzureRM.Sql</span></span>
* <span data-ttu-id="378f7-367">Följande cmdletar har uppdaterats med valfri LicenseType-parameter</span><span class="sxs-lookup"><span data-stu-id="378f7-367">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="378f7-368">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="378f7-368">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="378f7-369">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="378f7-369">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="378f7-370">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="378f7-370">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="378f7-371">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="378f7-371">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="378f7-372">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="378f7-372">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="378f7-373">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="378f7-373">AzureRM.Websites</span></span>
* <span data-ttu-id="378f7-374">New-AzureRMWebApp har uppdaterats för att använda vanliga algoritmer från biblioteket Strategy.</span><span class="sxs-lookup"><span data-stu-id="378f7-374">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="378f7-375">6.1.0 – maj 2018</span><span class="sxs-lookup"><span data-stu-id="378f7-375">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="378f7-376">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="378f7-376">AzureRM.Profile</span></span>
* <span data-ttu-id="378f7-377">Åtgärda problem där en körning av Clear-AzureRmContext skulle bevara en tom kontext med namnet på den föregående standardkontexten som gjorde att användaren inte kunde skapa en ny kontext med det gamla namnet</span><span class="sxs-lookup"><span data-stu-id="378f7-377">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="378f7-378">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="378f7-378">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="378f7-379">Aktivera Gateway associerings- och avassocieringsåtgärder på AS.</span><span class="sxs-lookup"><span data-stu-id="378f7-379">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="378f7-380">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="378f7-380">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="378f7-381">Stöd för ApiVersions, ApiReleases och ApiRevisions har lagts till</span><span class="sxs-lookup"><span data-stu-id="378f7-381">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="378f7-382">Stöd för serverdelen på ServiceFabric har lagts till</span><span class="sxs-lookup"><span data-stu-id="378f7-382">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="378f7-383">Stöd för Application Insights-loggare har lagts till</span><span class="sxs-lookup"><span data-stu-id="378f7-383">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="378f7-384">Stöd för att identifiera SKU:n ”Basic” som en giltig SKU för Api Management-tjänsten har lagts till</span><span class="sxs-lookup"><span data-stu-id="378f7-384">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="378f7-385">Stöd för att installera certifikat som utfärdats av privata certifikatutfärdare som rot eller certifikatutfärdare har lagts till</span><span class="sxs-lookup"><span data-stu-id="378f7-385">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="378f7-386">Stöd för att godkänna anpassade SSL-certifikat via KeyVault och flera proxy-värdnamn har lagts till</span><span class="sxs-lookup"><span data-stu-id="378f7-386">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="378f7-387">Stöd för MSI-identitet har lagts till</span><span class="sxs-lookup"><span data-stu-id="378f7-387">Added support for MSI identity</span></span>
* <span data-ttu-id="378f7-388">Stöd för att godkänna principer via URL har lagts till. Obs! Följande cmdletar blir inaktuella i framtida versioner</span><span class="sxs-lookup"><span data-stu-id="378f7-388">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="378f7-389">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="378f7-389">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="378f7-390">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="378f7-390">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="378f7-391">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="378f7-391">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="378f7-392">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="378f7-392">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="378f7-393">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="378f7-393">AzureRM.Batch</span></span>
* <span data-ttu-id="378f7-394">Släpp nya cmdleten Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="378f7-394">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="378f7-395">Släpp nya cmdleten Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="378f7-395">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="378f7-396">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="378f7-396">AzureRM.Consumption</span></span>
* <span data-ttu-id="378f7-397">Lägg till nya parametrar Expand, ResourceGroup, InstanceName, InstanceId, Tags och Top på cmdleten Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="378f7-397">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="378f7-398">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="378f7-398">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="378f7-399">Åtgärda exempel för Export AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="378f7-399">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="378f7-400">Åtgärda undantag för null-parameter för rekursivt ärende i Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="378f7-400">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="378f7-401">Åtgärda hjälpfilerna för Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="378f7-401">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="378f7-402">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="378f7-402">AzureRM.Network</span></span>
* <span data-ttu-id="378f7-403">Öka nätverkets SDK-version från förhandsversionen 18.0.0 till förhandsversionen 19.0.0</span><span class="sxs-lookup"><span data-stu-id="378f7-403">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="378f7-404">Cmdlet har lagts till för att skapa protokollinformation</span><span class="sxs-lookup"><span data-stu-id="378f7-404">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="378f7-405">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="378f7-405">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="378f7-406">Cmdlet har lagts till för att lägga till en ny kretsanslutning till en befintlig expressroute-krets.</span><span class="sxs-lookup"><span data-stu-id="378f7-406">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="378f7-407">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="378f7-407">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="378f7-408">Cmdlet har lagts till för att ta bort en kretsanslutning från en befintlig expressroute-krets.</span><span class="sxs-lookup"><span data-stu-id="378f7-408">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="378f7-409">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="378f7-409">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="378f7-410">Cmdlet har lagts till för att hämta en kretsanslutning</span><span class="sxs-lookup"><span data-stu-id="378f7-410">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="378f7-411">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="378f7-411">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="378f7-412">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="378f7-412">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="378f7-413">Användning med serverautentisering med genererade certifikat (problem #5998) har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="378f7-413">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="378f7-414">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="378f7-414">AzureRM.Sql</span></span>
* <span data-ttu-id="378f7-415">Cmdletar för granskning för att ta bort AuditActions eller AuditActionGroups har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="378f7-415">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="378f7-416">Åtgärdade problem med Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy vid konfigurering av en ny flexibel bevarandeprincip där kommandot misslyckas med ett meddelande om att konfigurering av långsiktig bevarandeprincip med Azure Recovery Service-valv och principen inte längre stöds,</span><span class="sxs-lookup"><span data-stu-id="378f7-416">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="378f7-417">och att en begäran med den nya flexibla bevarandeprincipen ska skickas.</span><span class="sxs-lookup"><span data-stu-id="378f7-417">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="378f7-418">Uppdatera alla Azure Sql Database/ElasticPool Creation/Update-relaterade cmdletar för att använda det nya databas-API:et som stöder SKU-egenskaper för skalnings- och nivårelaterade egenskaper.</span><span class="sxs-lookup"><span data-stu-id="378f7-418">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="378f7-419">Cmdletar har uppdaterats, inklusive:</span><span class="sxs-lookup"><span data-stu-id="378f7-419">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="378f7-420">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="378f7-420">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="378f7-421">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="378f7-421">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="378f7-422">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="378f7-422">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="378f7-423">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="378f7-423">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="378f7-424">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="378f7-424">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="378f7-425">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="378f7-425">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="378f7-426">Uppdatera parametrarna för Get-AzureRmTrafficManagerProfile så att ResourceGroupName-parametern blir obligatorisk när du använder Name-parametern.</span><span class="sxs-lookup"><span data-stu-id="378f7-426">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
