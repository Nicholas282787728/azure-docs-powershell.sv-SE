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
ms.openlocfilehash: 6043d17df1b5e91521bad31e65372c10ee6a5c6a
ms.sourcegitcommit: 9cb98f055a0525c2061f65149965d5e7c3e03ddc
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/30/2018
ms.locfileid: "43117523"
---
# <a name="release-notes"></a><span data-ttu-id="faf11-103">Viktig information</span><span class="sxs-lookup"><span data-stu-id="faf11-103">Release notes</span></span>

<span data-ttu-id="faf11-104">Det här är en lista över ändringar som har gjorts i Azure PowerShell i den här versionen.</span><span class="sxs-lookup"><span data-stu-id="faf11-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="680---august-2018"></a><span data-ttu-id="faf11-105">6.8.0 – augusti 2018</span><span class="sxs-lookup"><span data-stu-id="faf11-105">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="faf11-106">Allmänt</span><span class="sxs-lookup"><span data-stu-id="faf11-106">General</span></span>
* <span data-ttu-id="faf11-107">Problem med standardresursgrupp som inte har konfigurerats har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="faf11-107">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="faf11-108">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="faf11-108">AzureRM.Profile</span></span>
* <span data-ttu-id="faf11-109">Utgångsegenskap har lagts till i token som returneras under Connect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="faf11-109">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="faf11-110">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="faf11-110">AzureRM.Compute</span></span>
* <span data-ttu-id="faf11-111">Ett problem med att mål saknas i felutdata har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="faf11-111">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="faf11-112">Problem med lagringskontotyper för virtuell dator med en hanterad disk har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="faf11-112">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="faf11-113">Åtgärda cmdletar för AEM-tillägg för andra miljöer, till exempel Azure Kina</span><span class="sxs-lookup"><span data-stu-id="faf11-113">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="faf11-114">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="faf11-114">AzureRM.IotHub</span></span>
* <span data-ttu-id="faf11-115">Korrigera exempel för New-AzureRmIotHubExportDevices och New-AzureRmIotHubImportDevices</span><span class="sxs-lookup"><span data-stu-id="faf11-115">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="faf11-116">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="faf11-116">AzureRM.Network</span></span>
* <span data-ttu-id="faf11-117">Standardmodeller har ändrats för att visas i tabellvy</span><span class="sxs-lookup"><span data-stu-id="faf11-117">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="faf11-118">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="faf11-118">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="faf11-119">Åtgärda fel i Update-AzureRmPowerBIEmbeddedCapacity vid försök att skala pausad kapacitet</span><span class="sxs-lookup"><span data-stu-id="faf11-119">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="faf11-120">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="faf11-120">AzureRM.Resources</span></span>
* <span data-ttu-id="faf11-121">Ett problem med att skapa hanterade program från MarketPlace har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="faf11-121">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="faf11-122">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="faf11-122">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="faf11-123">Korrigeringar för problem</span><span class="sxs-lookup"><span data-stu-id="faf11-123">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="faf11-124">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="faf11-124">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="faf11-125">Stöd för trafikroutningsmetoden MultiValue</span><span class="sxs-lookup"><span data-stu-id="faf11-125">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="faf11-126">Ny parameter, ”MaxReturn”, för MultiValue-routning</span><span class="sxs-lookup"><span data-stu-id="faf11-126">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="faf11-127">Stöd för trafikroutningsmetod för undernät</span><span class="sxs-lookup"><span data-stu-id="faf11-127">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="faf11-128">Stöd för IP-adressintervall (undernät) i slutpunkter</span><span class="sxs-lookup"><span data-stu-id="faf11-128">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="faf11-129">Stöd för anpassade rubriker i profiler</span><span class="sxs-lookup"><span data-stu-id="faf11-129">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="faf11-130">Stöd för förväntade statuskodintervall i profiler</span><span class="sxs-lookup"><span data-stu-id="faf11-130">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="faf11-131">Stöd för anpassade rubriker i slutpunkter</span><span class="sxs-lookup"><span data-stu-id="faf11-131">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="faf11-132">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="faf11-132">AzureRM.Websites</span></span>
* <span data-ttu-id="faf11-133">Problem med standardresursgrupp som inte har konfigurerats korrekt har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="faf11-133">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="faf11-134">6.7.0 – augusti 2018</span><span class="sxs-lookup"><span data-stu-id="faf11-134">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="faf11-135">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="faf11-135">AzureRM.Profile</span></span>
* <span data-ttu-id="faf11-136">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="faf11-136">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="faf11-137">Lägg till användar-id i standardkontextnamnet för att undvika kontextkonflikter</span><span class="sxs-lookup"><span data-stu-id="faf11-137">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="faf11-138">Åtgärda problem med Clear-AzureRmContext som orsakade problem med att välja en kontext #6398</span><span class="sxs-lookup"><span data-stu-id="faf11-138">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="faf11-139">Aktivera den klientorganisationsdomän som ska skickas till parametern -TenantId för Connect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="faf11-139">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="faf11-140">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="faf11-140">Azure.Storage</span></span>
* <span data-ttu-id="faf11-141">Ta bort begränsningen på 5 TB för Azure-filresurskvoten</span><span class="sxs-lookup"><span data-stu-id="faf11-141">Remove the 5TB limitation for Azure File Share quota</span></span>
- <span data-ttu-id="faf11-142">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="faf11-142">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="faf11-143">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="faf11-143">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="faf11-144">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="faf11-144">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="faf11-145">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="faf11-145">Azure.AnalysisServices</span></span>
* <span data-ttu-id="faf11-146">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="faf11-146">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="faf11-147">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="faf11-147">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="faf11-148">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="faf11-148">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="faf11-149">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="faf11-149">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="faf11-150">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="faf11-150">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="faf11-151">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="faf11-151">AzureRM.Automation</span></span>
* <span data-ttu-id="faf11-152">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="faf11-152">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="faf11-153">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="faf11-153">AzureRM.Backup</span></span>
* <span data-ttu-id="faf11-154">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="faf11-154">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="faf11-155">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="faf11-155">AzureRM.Batch</span></span>
* <span data-ttu-id="faf11-156">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="faf11-156">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="faf11-157">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="faf11-157">AzureRM.Billing</span></span>
* <span data-ttu-id="faf11-158">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="faf11-158">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="faf11-159">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="faf11-159">AzureRM.Cdn</span></span>
* <span data-ttu-id="faf11-160">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="faf11-160">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="faf11-161">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="faf11-161">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="faf11-162">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="faf11-162">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="faf11-163">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="faf11-163">AzureRM.Compute</span></span>
* <span data-ttu-id="faf11-164">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="faf11-164">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="faf11-165">Lägg till parametern EvictionPolicy i New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="faf11-165">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="faf11-166">Använd standardplatsen i DiskFileParameterSet för New-AzureRmVm om ingen plats har angetts.</span><span class="sxs-lookup"><span data-stu-id="faf11-166">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="faf11-167">Korrigera parameterbeskrivningen i Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="faf11-167">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="faf11-168">Korrigera cmdleten Get-AzureRmVMDiskEncryptionStatus för vissa singlepass-relaterade scenarier</span><span class="sxs-lookup"><span data-stu-id="faf11-168">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="faf11-169">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="faf11-169">AzureRM.Consumption</span></span>
* <span data-ttu-id="faf11-170">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="faf11-170">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="faf11-171">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="faf11-171">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="faf11-172">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="faf11-172">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="faf11-173">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="faf11-173">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="faf11-174">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="faf11-174">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="faf11-175">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="faf11-175">AzureRM.DataFactories</span></span>
* <span data-ttu-id="faf11-176">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="faf11-176">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="faf11-177">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="faf11-177">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="faf11-178">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="faf11-178">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="faf11-179">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="faf11-179">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="faf11-180">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="faf11-180">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="faf11-181">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="faf11-181">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="faf11-182">Korrigera felsökning när DebugPreference anges från powershell-kommandoraden</span><span class="sxs-lookup"><span data-stu-id="faf11-182">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="faf11-183">Uppdatera exemplet för Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="faf11-183">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="faf11-184">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="faf11-184">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="faf11-185">Uppdatera exemplet för Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="faf11-185">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="faf11-186">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="faf11-186">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="faf11-187">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="faf11-187">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="faf11-188">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="faf11-188">AzureRM.Dns</span></span>
* <span data-ttu-id="faf11-189">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="faf11-189">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="faf11-190">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="faf11-190">AzureRM.EventGrid</span></span>
* <span data-ttu-id="faf11-191">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="faf11-191">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="faf11-192">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="faf11-192">AzureRM.EventHub</span></span>
* <span data-ttu-id="faf11-193">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="faf11-193">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="faf11-194">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="faf11-194">AzureRM.HDInsight</span></span>
* <span data-ttu-id="faf11-195">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="faf11-195">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="faf11-196">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="faf11-196">AzureRM.Insights</span></span>
* <span data-ttu-id="faf11-197">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="faf11-197">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="faf11-198">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="faf11-198">AzureRM.IotHub</span></span>
* <span data-ttu-id="faf11-199">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="faf11-199">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="faf11-200">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="faf11-200">AzureRM.KeyVault</span></span>
* <span data-ttu-id="faf11-201">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="faf11-201">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="faf11-202">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="faf11-202">AzureRM.LogicApp</span></span>
* <span data-ttu-id="faf11-203">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="faf11-203">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="faf11-204">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="faf11-204">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="faf11-205">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="faf11-205">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="faf11-206">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="faf11-206">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="faf11-207">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="faf11-207">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="faf11-208">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="faf11-208">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="faf11-209">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="faf11-209">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="faf11-210">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="faf11-210">AzureRM.Media</span></span>
* <span data-ttu-id="faf11-211">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="faf11-211">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="faf11-212">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="faf11-212">AzureRM.Network</span></span>
* <span data-ttu-id="faf11-213">Exempel för Set-AzureRmLocalNetworkGateway har lagts till</span><span class="sxs-lookup"><span data-stu-id="faf11-213">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="faf11-214">Exempel och beskrivningar för Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey och New-AzureRmVirtualNetworkGatewayConnection har lagts till</span><span class="sxs-lookup"><span data-stu-id="faf11-214">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="faf11-215">Exempel för Remove-AzureRmVirtualNetworkGatewayIpConfig och Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="faf11-215">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="faf11-216">Exempel för Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey har lagts till</span><span class="sxs-lookup"><span data-stu-id="faf11-216">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="faf11-217">Exempel för Set-AzureRmVirtualNetworkGatewayConnectionSharedKey har lagts till</span><span class="sxs-lookup"><span data-stu-id="faf11-217">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="faf11-218">Exempel för Set-AzureRmVirtualNetworkGatewayConnection har lagts till</span><span class="sxs-lookup"><span data-stu-id="faf11-218">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="faf11-219">Cmdletar för ApplicationSecurityGroup, RouteTable and Usage har genererats om med den senaste kodgeneratorn</span><span class="sxs-lookup"><span data-stu-id="faf11-219">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="faf11-220">Förtydligade ett felmeddelande för Get-AzureRmVirtualNetworkSubnetConfig vid försök att hämta ett undernät som inte avslutas</span><span class="sxs-lookup"><span data-stu-id="faf11-220">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="faf11-221">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="faf11-221">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="faf11-222">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="faf11-222">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="faf11-223">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="faf11-223">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="faf11-224">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="faf11-224">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="faf11-225">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="faf11-225">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="faf11-226">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="faf11-226">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="faf11-227">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="faf11-227">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="faf11-228">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="faf11-228">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="faf11-229">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="faf11-229">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="faf11-230">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="faf11-230">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="faf11-231">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="faf11-231">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="faf11-232">Lade till principfilter i cmdleten Get-AzureRmRecoveryServicesBackItem.</span><span class="sxs-lookup"><span data-stu-id="faf11-232">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="faf11-233">Kommandot returnerar listan med säkerhetskopieringsobjekt som skyddas av det angivna princip-ID:t.</span><span class="sxs-lookup"><span data-stu-id="faf11-233">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="faf11-234">Microsoft.Azure.Management.RecoveryServices.Backup uppdaterades till förhandsversionen av 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="faf11-234">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="faf11-235">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="faf11-235">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="faf11-236">Parametern TargetResourceGroupName lades till i Restore-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="faf11-236">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="faf11-237">Den resursgrupp som de hanterade diskarna återställs till.</span><span class="sxs-lookup"><span data-stu-id="faf11-237">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="faf11-238">Gäller för säkerhetskopiering av virtuell dator med hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="faf11-238">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="faf11-239">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="faf11-239">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="faf11-240">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="faf11-240">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="faf11-241">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="faf11-241">AzureRM.RedisCache</span></span>
* <span data-ttu-id="faf11-242">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="faf11-242">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="faf11-243">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="faf11-243">AzureRM.Relay</span></span>
* <span data-ttu-id="faf11-244">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="faf11-244">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="faf11-245">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="faf11-245">AzureRM.Resources</span></span>
* <span data-ttu-id="faf11-246">Distribution av supportmall i prenumerationsomfånget.</span><span class="sxs-lookup"><span data-stu-id="faf11-246">Support template deployment at subscription scope.</span></span> <span data-ttu-id="faf11-247">Lägg till nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="faf11-247">Add new Cmdlets:</span></span>
    - <span data-ttu-id="faf11-248">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="faf11-248">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="faf11-249">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="faf11-249">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="faf11-250">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="faf11-250">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="faf11-251">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="faf11-251">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="faf11-252">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="faf11-252">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="faf11-253">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="faf11-253">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="faf11-254">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="faf11-254">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="faf11-255">Korrigera ett problem där fel inträffar när en kontext skickas till Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="faf11-255">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="faf11-256">Korrigera exempel i New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="faf11-256">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="faf11-257">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="faf11-257">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="faf11-258">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="faf11-258">AzureRM.Scheduler</span></span>
* <span data-ttu-id="faf11-259">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="faf11-259">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="faf11-260">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="faf11-260">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="faf11-261">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="faf11-261">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="faf11-262">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="faf11-262">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="faf11-263">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="faf11-263">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="faf11-264">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="faf11-264">AzureRM.Sql</span></span>
* <span data-ttu-id="faf11-265">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="faf11-265">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="faf11-266">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="faf11-266">AzureRM.Storage</span></span>
* <span data-ttu-id="faf11-267">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="faf11-267">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="faf11-268">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="faf11-268">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="faf11-269">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="faf11-269">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="faf11-270">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="faf11-270">AzureRM.Tags</span></span>
* <span data-ttu-id="faf11-271">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="faf11-271">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="faf11-272">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="faf11-272">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="faf11-273">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="faf11-273">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="faf11-274">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="faf11-274">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="faf11-275">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="faf11-275">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="faf11-276">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="faf11-276">AzureRM.Websites</span></span>
* <span data-ttu-id="faf11-277">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="faf11-277">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="faf11-278">6.6.0 – juli 2018</span><span class="sxs-lookup"><span data-stu-id="faf11-278">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="faf11-279">Allmänt</span><span class="sxs-lookup"><span data-stu-id="faf11-279">General</span></span>
* <span data-ttu-id="faf11-280">Alla hjälpfiler har uppdaterats för att ta med fullständiga parametertyper och korrekta indata-/utdatatyper.</span><span class="sxs-lookup"><span data-stu-id="faf11-280">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="faf11-281">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="faf11-281">AzureRM.Profile</span></span>
* <span data-ttu-id="faf11-282">Common.Strategy-biblioteket har uppdaterats för att kunna verifiera att den aktuella konfigurationsfilen för en resurs är kompatibel med målresursen.</span><span class="sxs-lookup"><span data-stu-id="faf11-282">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="faf11-283">ps1xml-typer har lagts till i Common.Storage</span><span class="sxs-lookup"><span data-stu-id="faf11-283">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="faf11-284">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="faf11-284">Azure.Storage</span></span>
* <span data-ttu-id="faf11-285">Lade till stöd för hämtning av lagringskontext från DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="faf11-285">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="faf11-286">Lade till Ps1XmlAttribute till utdatatypegenskaper för cmdletar.</span><span class="sxs-lookup"><span data-stu-id="faf11-286">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="faf11-287">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="faf11-287">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="faf11-288">Åtgärdat problem https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="faf11-288">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="faf11-289">En bugg har åtgärdats i Automapper för att översätta PsApiManagementApi till ApiContract</span><span class="sxs-lookup"><span data-stu-id="faf11-289">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="faf11-290">Åtgärdat problem https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="faf11-290">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="faf11-291">En bugg har åtgärdats i File.Save för att inte överbelasta kodningstypen</span><span class="sxs-lookup"><span data-stu-id="faf11-291">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="faf11-292">Åtgärdat problem https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="faf11-292">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="faf11-293">Har uppgraderats till Nuget-versionen 4.0.3 vilket åtgärdar mönsterundantaget på apiId</span><span class="sxs-lookup"><span data-stu-id="faf11-293">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="faf11-294">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="faf11-294">AzureRM.Compute</span></span>
* <span data-ttu-id="faf11-295">Åtgärda problem med fel vid skapandet av en virtuell dator med hjälp av DiskFileParameterSet i New-AzureRmVm på grund av namnbyte på PremiumLRS-lagringskontotypen.</span><span class="sxs-lookup"><span data-stu-id="faf11-295">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="faf11-296">Åtgärda cmdleten Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="faf11-296">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="faf11-297">Uppdatera Get-AzureRmAvailabilitySet för att aktivera funktionen för att lista alla tillgänglighetsuppsättningar i en prenumeration.</span><span class="sxs-lookup"><span data-stu-id="faf11-297">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="faf11-298">(Parametern ResouceGroupName är nu frivillig.)</span><span class="sxs-lookup"><span data-stu-id="faf11-298">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="faf11-299">Uppdatera SimpleParameterSet för "New-AzureRmVm" för att aktivera accelererat nätverk på berättigade virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="faf11-299">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="faf11-300">Uppdatera den enkla parameteruppsättningen för New-AzureRmVmss så att det inte går att skapa de virtuella datorerna när en användarangiven lastbalanserare redan finns.</span><span class="sxs-lookup"><span data-stu-id="faf11-300">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="faf11-301">Uppdatera exempel för New-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="faf11-301">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="faf11-302">Lägg till exempel för "New-AzureRmVM"</span><span class="sxs-lookup"><span data-stu-id="faf11-302">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="faf11-303">Uppdatera beskrivning för Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="faf11-303">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="faf11-304">Uppdatera Exempel 1 för Set-AzureRmVMBginfoExtension för stavningskontroll och prefix.</span><span class="sxs-lookup"><span data-stu-id="faf11-304">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="faf11-305">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="faf11-305">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="faf11-306">ADF .Net SDK-versionen har uppdaterats till 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="faf11-306">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="faf11-307">Stöd för delning av Integration Runtime (lokal installation) mellan datafabriker.</span><span class="sxs-lookup"><span data-stu-id="faf11-307">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="faf11-308">Lägg till ny parameter – SharedIntegrationRuntimeResourceId i cmdleten Set-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="faf11-308">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="faf11-309">Lägg till ny valfri parameter – LinkedDataFactoryName i cmdleten Remove-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="faf11-309">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="faf11-310">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="faf11-310">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="faf11-311">DataPlane SDK-versionen (Microsoft.Azure.DataLake.Store) har uppdaterats till 1.1.9</span><span class="sxs-lookup"><span data-stu-id="faf11-311">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="faf11-312">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="faf11-312">AzureRM.EventHub</span></span>
* <span data-ttu-id="faf11-313">Piping för InputObject and ResourceId i borttagna cmdletar har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="faf11-313">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="faf11-314">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="faf11-314">AzureRM.Insights</span></span>
* <span data-ttu-id="faf11-315">Formatering har åtgärdats för OutputType i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="faf11-315">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="faf11-316">Använda Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span><span class="sxs-lookup"><span data-stu-id="faf11-316">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="faf11-317">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="faf11-317">AzureRM.KeyVault</span></span>
* <span data-ttu-id="faf11-318">Åtgärda problem med piping i Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="faf11-318">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="faf11-319">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="faf11-319">AzureRM.Network</span></span>
* <span data-ttu-id="faf11-320">Exempel har lagts till för LoadBalancerInboundNatPoolConfig-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="faf11-320">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="faf11-321">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="faf11-321">AzureRM.Resources</span></span>
* <span data-ttu-id="faf11-322">Åtgärda problem när både taggnamn och värde anges för "Get-AzureRmResource"</span><span class="sxs-lookup"><span data-stu-id="faf11-322">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="faf11-323">Åtgärda pipingscenario med "Set-AzureRmResource"</span><span class="sxs-lookup"><span data-stu-id="faf11-323">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="faf11-324">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="faf11-324">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="faf11-325">Piping för InputObject and ResourceId i borttagna cmdletar har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="faf11-325">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="faf11-326">några problem har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="faf11-326">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="faf11-327">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="faf11-327">AzureRM.Sql</span></span>
* <span data-ttu-id="faf11-328">Lägg till stöd för Server Advanced Threat Protection med följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="faf11-328">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="faf11-329">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="faf11-329">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="faf11-330">Lägg till stöd för Sårbarhetsbedömning med följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="faf11-330">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="faf11-331">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="faf11-331">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="faf11-332">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="faf11-332">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="faf11-333">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="faf11-333">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="faf11-334">Exempel i Remove-AzureRmSqlServerFirewallRule har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="faf11-334">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="faf11-335">Åtgärda felaktig hantering av datum och tid för andra kulturer än usa-baserade kulturer i Get-AzureSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="faf11-335">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="faf11-336">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="faf11-336">AzureRM.Storage</span></span>
* <span data-ttu-id="faf11-337">Lägg till Ps1XmlAttribute i utdatatypegenskaper för cmdletar</span><span class="sxs-lookup"><span data-stu-id="faf11-337">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="faf11-338">Visa utdata för cmdleten StorageAccount i tabellvyn</span><span class="sxs-lookup"><span data-stu-id="faf11-338">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="faf11-339">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="faf11-339">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="faf11-340">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="faf11-340">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="faf11-341">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="faf11-341">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="faf11-342">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="faf11-342">AzureRM.Tags</span></span>
* <span data-ttu-id="faf11-343">Ta bort felaktig instruktion från hjälpen för cmdleten Tag</span><span class="sxs-lookup"><span data-stu-id="faf11-343">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="faf11-344">6.5.0 – juli 2018</span><span class="sxs-lookup"><span data-stu-id="faf11-344">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="faf11-345">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="faf11-345">AzureRM.Profile</span></span>
* <span data-ttu-id="faf11-346">Hjälp för ”Get-AzureRmContextAutosaveSetting” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="faf11-346">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="faf11-347">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="faf11-347">Azure.Storage</span></span>
* <span data-ttu-id="faf11-348">Stöd för uppladdning av blob eller fil med lässkyddad SAS-token</span><span class="sxs-lookup"><span data-stu-id="faf11-348">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="faf11-349">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="faf11-349">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="faf11-350">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="faf11-350">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="faf11-351">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="faf11-351">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="faf11-352">Lägg till den nödvändiga egenskapen ResourceGroupName i AS.</span><span class="sxs-lookup"><span data-stu-id="faf11-352">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="faf11-353">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="faf11-353">AzureRM.Automation</span></span>
* <span data-ttu-id="faf11-354">Uppdatera hjälp och lägg till exempel för ”New-AzureRMAutomationSchedule”</span><span class="sxs-lookup"><span data-stu-id="faf11-354">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="faf11-355">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="faf11-355">AzureRM.Compute</span></span>
* <span data-ttu-id="faf11-356">Lägg till parametern -Tag förUpdate/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="faf11-356">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="faf11-357">Lägg till exempel för ”Add-AzureRmVmssExtension”</span><span class="sxs-lookup"><span data-stu-id="faf11-357">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="faf11-358">Lägg till exempel för ”Remove-AzureRmVmssExtension”</span><span class="sxs-lookup"><span data-stu-id="faf11-358">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="faf11-359">Uppdatera hjälp för ”Set-AzureRmVMAccessExtension”</span><span class="sxs-lookup"><span data-stu-id="faf11-359">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="faf11-360">Uppdatera SimpleParameterSet för New-AzureRmVmss för att ställa in SinglePlacementGroup på falskt som standard och lägg till växlingsparametern ”SinglePlacementGroup” som gör att användare kan skapa VMSS i en enda placeringsgrupp.</span><span class="sxs-lookup"><span data-stu-id="faf11-360">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="faf11-361">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="faf11-361">AzureRM.EventHub</span></span>
* <span data-ttu-id="faf11-362">En skrivskyddad egenskap, ”PendingReplicationOperationsCount”, har lagts till för klassen PSEventHubDRConfigurationAttributes som anger antalet väntande replikeringsåtgärder medan replikeringen pågår</span><span class="sxs-lookup"><span data-stu-id="faf11-362">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="faf11-363">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="faf11-363">AzureRM.KeyVault</span></span>
* <span data-ttu-id="faf11-364">Uppdatera felmeddelande för Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="faf11-364">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="faf11-365">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="faf11-365">AzureRM.LogicApp</span></span>
* <span data-ttu-id="faf11-366">Felet ”parameteruppsättningen gick inte att matcha” har korrigerats i New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="faf11-366">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="faf11-367">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="faf11-367">AzureRM.Network</span></span>
* <span data-ttu-id="faf11-368">Aktivera peering mellan virtuella nätverk i flera klienter för Set/Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="faf11-368">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="faf11-369">Nedanstående cmdletar för Application Gateway har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="faf11-369">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="faf11-370">New-AzureRmApplicationGateway: EnableFIPS-flagga har lagts till för stöd för zoner</span><span class="sxs-lookup"><span data-stu-id="faf11-370">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="faf11-371">New-AzureRmApplicationGatewaySku: nya SKU:er, Standard_v2 och WAF_v2, har lagts till</span><span class="sxs-lookup"><span data-stu-id="faf11-371">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="faf11-372">Set-AzureRmApplicationGatewaySku: nya SKU:er, Standard_v2 och WAF_v2, har lagts till</span><span class="sxs-lookup"><span data-stu-id="faf11-372">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="faf11-373">RouteTable-cmdletar har återskapats med den senaste versionen av generatorn</span><span class="sxs-lookup"><span data-stu-id="faf11-373">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="faf11-374">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="faf11-374">AzureRM.Relay</span></span>
* <span data-ttu-id="faf11-375">Markdown-filer har uppdaterats och korrigerar problem med parameternamn i exemplet</span><span class="sxs-lookup"><span data-stu-id="faf11-375">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="faf11-376">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="faf11-376">AzureRM.Resources</span></span>
* <span data-ttu-id="faf11-377">Uppdatera cmdletar för rolltilldelning och rolldefinition:</span><span class="sxs-lookup"><span data-stu-id="faf11-377">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="faf11-378">Ta bort extra anrop för rolldefinitioner som görs som en del av sidindelning.</span><span class="sxs-lookup"><span data-stu-id="faf11-378">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="faf11-379">Åtgärda Get-AzureRMRoleAssignment-cmdlet</span><span class="sxs-lookup"><span data-stu-id="faf11-379">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="faf11-380">Åtgärda parameterfunktioner för kommandot -ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="faf11-380">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="faf11-381">Åtgärda problem med ”Get-AzureRmResource” där ”-ResourceType”-parametern var skiftlägeskänsligt</span><span class="sxs-lookup"><span data-stu-id="faf11-381">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="faf11-382">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="faf11-382">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="faf11-383">Parametrar för att stoppa och hoppa över har lagts till i listan över cmdletar</span><span class="sxs-lookup"><span data-stu-id="faf11-383">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="faf11-384">Cmdletar för migrering från Standard- till Premium-namnområden har lagts till:</span><span class="sxs-lookup"><span data-stu-id="faf11-384">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="faf11-385">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="faf11-385">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="faf11-386">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="faf11-386">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="faf11-387">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="faf11-387">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="faf11-388">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="faf11-388">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="faf11-389">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="faf11-389">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="faf11-390">En skrivskyddad egenskap, ”PendingReplicationOperationsCount” har lagts till för klassen PSServiceBusDRConfigurationAttributes som anger antalet väntande replikeringsåtgärder medan replikeringen pågår</span><span class="sxs-lookup"><span data-stu-id="faf11-390">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="faf11-391">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="faf11-391">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="faf11-392">Uppdatera exempel för ”New-AzureRmServiceFabricCluster”</span><span class="sxs-lookup"><span data-stu-id="faf11-392">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="faf11-393">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="faf11-393">AzureRM.Sql</span></span>
* <span data-ttu-id="faf11-394">Nya cmdletar för Management.Sql som gör att kunderna kan lägga till certifikat för transparent datakryptering till SQL Server-instans eller en hanterad instans har lagts till</span><span class="sxs-lookup"><span data-stu-id="faf11-394">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="faf11-395">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="faf11-395">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="faf11-396">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="faf11-396">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="faf11-397">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="faf11-397">AzureRM.Websites</span></span>
* <span data-ttu-id="faf11-398">När `Set-AzureRmWebApp -AssignIdentity` och `Set-AzureRmWebAppSlot -AssignIdentity` är inställda på falskt tar de nu bort identitetsegenskapen från platsobjektet. Även förhandsgranskningstaggen tas bort.</span><span class="sxs-lookup"><span data-stu-id="faf11-398">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="faf11-399">`Get-AzureRmWebAppMetrics`, `Get-AzureRmAppServicePlanMetrics`-exempel har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="faf11-399">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="faf11-400">`Set-AzureRmWebApp -PhpVersion` har stöd för ”av” som en giltig php-version</span><span class="sxs-lookup"><span data-stu-id="faf11-400">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="faf11-401">6.4.0 – juli 2018</span><span class="sxs-lookup"><span data-stu-id="faf11-401">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="faf11-402">Allmänt</span><span class="sxs-lookup"><span data-stu-id="faf11-402">General</span></span>
* <span data-ttu-id="faf11-403">Formatering av OutputType i hjälpfiler har korrigerats för de flesta moduler</span><span class="sxs-lookup"><span data-stu-id="faf11-403">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="faf11-404">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="faf11-404">AzureRM.Profile</span></span>
* <span data-ttu-id="faf11-405">Ps1Xml-attribut har lagts till för grundläggande utdatatyper</span><span class="sxs-lookup"><span data-stu-id="faf11-405">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="faf11-406">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="faf11-406">AzureRM.Compute</span></span>
* <span data-ttu-id="faf11-407">IP-tagg-funktioner för VMSS</span><span class="sxs-lookup"><span data-stu-id="faf11-407">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="faf11-408">"New-AzureRmVmssIpTagConfig"-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="faf11-408">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="faf11-409">IpTag-parameter har lagts till för New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="faf11-409">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="faf11-410">Automatisk återställningsfunktion för operativsystem för VMSS</span><span class="sxs-lookup"><span data-stu-id="faf11-410">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="faf11-411">DisableAutoRollback-parametrar har lagts till för New-AzureRmVmssConfig och Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="faf11-411">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="faf11-412">Funktion för uppgraderingshistorik för operativsystem för Vmss</span><span class="sxs-lookup"><span data-stu-id="faf11-412">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="faf11-413">OSUpgradeHistory-växlingsparametern har lagts till för Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="faf11-413">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="faf11-414">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="faf11-414">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="faf11-415">Lägg till stöd för katalog-ACL:er med hjälp av följande kommandon:</span><span class="sxs-lookup"><span data-stu-id="faf11-415">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="faf11-416">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="faf11-416">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="faf11-417">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="faf11-417">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="faf11-418">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="faf11-418">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="faf11-419">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="faf11-419">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="faf11-420">Lägg till stöd för annullering och förloppsspårning för Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="faf11-420">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="faf11-421">Lägg till stöd för annullering för Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="faf11-421">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="faf11-422">Åtgärda tömning av felsökningsmeddelanden för cmdletar som gör rekursiva åtgärder</span><span class="sxs-lookup"><span data-stu-id="faf11-422">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="faf11-423">Åtgärda platsen för testning av DataLake-cmdletar</span><span class="sxs-lookup"><span data-stu-id="faf11-423">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="faf11-424">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="faf11-424">AzureRM.EventHub</span></span>
* <span data-ttu-id="faf11-425">Parametrar för optimalt maxantal har lagts till i liståtgärds-cmdletarna Get-AzureRmEventHub och Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="faf11-425">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="faf11-426">Ett problem i New-AzureRmEventHub-cmdleten har åtgärdats där minst en parameter behövdes när du skapade en ny EventHub.</span><span class="sxs-lookup"><span data-stu-id="faf11-426">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="faf11-427">Angiven standardparameter har ställts in.</span><span class="sxs-lookup"><span data-stu-id="faf11-427">Provided Default Parameter set.</span></span>
* <span data-ttu-id="faf11-428">Valfri parameter för KeyValue har lagts till för New-AzureRmEventHubKey-cmdleten, vilket gör det möjligt att ange KeyValue.</span><span class="sxs-lookup"><span data-stu-id="faf11-428">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="faf11-429">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="faf11-429">AzureRM.KeyVault</span></span>
* <span data-ttu-id="faf11-430">Åtgärda problem där alla resurser returnerades av Get-AzureRmKeyVault-taggen</span><span class="sxs-lookup"><span data-stu-id="faf11-430">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="faf11-431">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="faf11-431">AzureRM.Network</span></span>
* <span data-ttu-id="faf11-432">Gör nya SKU:er tillgängliga för zonredundanta VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="faf11-432">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="faf11-433">Nya kommandon har lagts till för funktionen: ExpressRoute Partner APIs via ARM</span><span class="sxs-lookup"><span data-stu-id="faf11-433">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="faf11-434">Get-AzureRmExpressRouteCrossConnection har lagts till</span><span class="sxs-lookup"><span data-stu-id="faf11-434">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="faf11-435">Set-AzureRmExpressRouteCrossConnection har lagts till</span><span class="sxs-lookup"><span data-stu-id="faf11-435">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="faf11-436">Add-AzureRmExpressRouteCrossConnectionPeering har lagts till</span><span class="sxs-lookup"><span data-stu-id="faf11-436">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="faf11-437">Get-AzureRmExpressRouteCrossConnectionPeering har lagts till</span><span class="sxs-lookup"><span data-stu-id="faf11-437">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="faf11-438">Remove-AzureRmExpressRouteCrossConnectionPeering har lagts till</span><span class="sxs-lookup"><span data-stu-id="faf11-438">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="faf11-439">Get-AzureRMExpressRouteCrossConnectionArpTable har lagts till</span><span class="sxs-lookup"><span data-stu-id="faf11-439">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="faf11-440">Get-AzureRMExpressRouteCrossConnectionRouteTable har lagts till</span><span class="sxs-lookup"><span data-stu-id="faf11-440">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="faf11-441">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary har lagts till</span><span class="sxs-lookup"><span data-stu-id="faf11-441">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="faf11-442">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="faf11-442">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="faf11-443">Get-AzureRmRecoveryServicesBackupStatus-cmdlet har lagts till.</span><span class="sxs-lookup"><span data-stu-id="faf11-443">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="faf11-444">Denna cmdlet tar ett ID för virtuell dator och kontrollerar om den virtuella datorn skyddas av ett valv i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="faf11-444">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="faf11-445">Om ett sådant valv finns returnerar cmdleten valvinformationen.</span><span class="sxs-lookup"><span data-stu-id="faf11-445">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="faf11-446">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="faf11-446">AzureRM.Resources</span></span>
* <span data-ttu-id="faf11-447">Uppdatera Get-AzureRmPolicyAssignment-cmdletar:</span><span class="sxs-lookup"><span data-stu-id="faf11-447">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="faf11-448">Lägg till stöd för att lista -Scope-värden på hanteringsgruppsnivå</span><span class="sxs-lookup"><span data-stu-id="faf11-448">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="faf11-449">Lägg till stöd för hämtning av enskilda tilldelningar med -Scope-värden på hanteringsgruppsnivå.</span><span class="sxs-lookup"><span data-stu-id="faf11-449">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="faf11-450">Lägg till växlar för -Effective och -All till kontrollparametrar</span><span class="sxs-lookup"><span data-stu-id="faf11-450">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="faf11-451">Uppdatera Get/New/Remove/Set-AzureRmPolicyDefinition-cmdletar</span><span class="sxs-lookup"><span data-stu-id="faf11-451">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="faf11-452">Lägg till parameter för -ManagementGroupName om du vill tillämpa åtgärder för en viss hanteringsgrupp</span><span class="sxs-lookup"><span data-stu-id="faf11-452">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="faf11-453">Lägg till parameter för -SubscriptionId om du vill tillämpa åtgärder för en viss prenumeration</span><span class="sxs-lookup"><span data-stu-id="faf11-453">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="faf11-454">Uppdatera Get/New/Remove/Set-AzureRmPolicySetDefinition-cmdletar</span><span class="sxs-lookup"><span data-stu-id="faf11-454">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="faf11-455">Lägg till parameter för -ManagementGroupName om du vill tillämpa åtgärder för en viss hanteringsgrupp</span><span class="sxs-lookup"><span data-stu-id="faf11-455">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="faf11-456">Lägg till parameter för -SubscriptionId om du vill tillämpa åtgärder för en viss prenumeration</span><span class="sxs-lookup"><span data-stu-id="faf11-456">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="faf11-457">Lägg till stöd för hemliga KeyVault-referenser i parametrar när du använder "TemplateParameterObject" i "New-AzureRmResourceGroupDeployment"</span><span class="sxs-lookup"><span data-stu-id="faf11-457">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="faf11-458">Åtgärda problem med att "-EndDate"-parametern ignorerades på grund av "New-AzureRmADAppCredential"</span><span class="sxs-lookup"><span data-stu-id="faf11-458">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="faf11-459">Åtgärda problem med att felaktig URL användes i "New-AzureRmADAppCredential" vid begäran</span><span class="sxs-lookup"><span data-stu-id="faf11-459">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="faf11-460">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="faf11-460">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="faf11-461">Valfri parameter för -KeyValue har lagts till för New-AzureRmServiceBusKey-cmdleten, vilket gör det möjligt att ange KeyValue.</span><span class="sxs-lookup"><span data-stu-id="faf11-461">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="faf11-462">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="faf11-462">AzureRM.Sql</span></span>
* <span data-ttu-id="faf11-463">Användardefinierade återställningspunkter har klargjorts för SQLDW i New-AzureRmSqlDatabaseRestorePoint-hjälpen</span><span class="sxs-lookup"><span data-stu-id="faf11-463">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="faf11-464">Dokumentationen om parametern -ComputeGeneration har uppdaterats i fler cmdletar</span><span class="sxs-lookup"><span data-stu-id="faf11-464">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="faf11-465">6.3.0 – juni 2018</span><span class="sxs-lookup"><span data-stu-id="faf11-465">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="faf11-466">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="faf11-466">AzureRM.Profile</span></span>
* <span data-ttu-id="faf11-467">Uppdaterade felmeddelanden för Enable-AzureRmContextAutoSave</span><span class="sxs-lookup"><span data-stu-id="faf11-467">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="faf11-468">Skapa en kontext för varje prenumeration när du kör ”Connect-AzureRmAccount” utan tidigare kontext</span><span class="sxs-lookup"><span data-stu-id="faf11-468">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="faf11-469">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="faf11-469">Azure.Storage</span></span>
* <span data-ttu-id="faf11-470">Ytterligare information om parametern -Permissions har lagts till i hjälpfilerna.</span><span class="sxs-lookup"><span data-stu-id="faf11-470">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="faf11-471">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="faf11-471">AzureRM.Compute</span></span>
* <span data-ttu-id="faf11-472">”Get-AzureRmVmDiskEncryptionStatus” korrigerar ett problem för virtuella datorer utan datadiskar</span><span class="sxs-lookup"><span data-stu-id="faf11-472">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="faf11-473">Uppdatera version av klientbibliotek för Compute för att korrigera följande cmdletar</span><span class="sxs-lookup"><span data-stu-id="faf11-473">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="faf11-474">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="faf11-474">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="faf11-475">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="faf11-475">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="faf11-476">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="faf11-476">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="faf11-477">Följande cmdletar har åtgärdats för att visa ”Åtgärds-ID” och ”Åtgärdsstatus” på ett korrekt sätt:</span><span class="sxs-lookup"><span data-stu-id="faf11-477">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="faf11-478">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="faf11-478">Start-AzureRmVM</span></span>
    - <span data-ttu-id="faf11-479">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="faf11-479">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="faf11-480">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="faf11-480">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="faf11-481">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="faf11-481">Set-AzureRmVM</span></span>
    - <span data-ttu-id="faf11-482">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="faf11-482">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="faf11-483">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="faf11-483">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="faf11-484">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="faf11-484">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="faf11-485">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="faf11-485">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="faf11-486">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="faf11-486">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="faf11-487">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="faf11-487">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="faf11-488">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="faf11-488">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="faf11-489">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="faf11-489">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="faf11-490">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="faf11-490">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="faf11-491">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="faf11-491">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="faf11-492">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="faf11-492">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="faf11-493">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="faf11-493">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="faf11-494">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="faf11-494">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="faf11-495">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="faf11-495">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="faf11-496">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="faf11-496">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="faf11-497">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="faf11-497">AzureRM.EventGrid</span></span>
* <span data-ttu-id="faf11-498">Ta bort verifieringsvillkoren ValidateNotNullOrEmpty för SubjectBeginsWith/SubjectEndsWith i cmdleten Update-AzureRmEventGridSubscription för att ändra de här parametrarna till en tom sträng om det behövs.</span><span class="sxs-lookup"><span data-stu-id="faf11-498">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="faf11-499">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="faf11-499">AzureRM.KeyVault</span></span>
* <span data-ttu-id="faf11-500">Åtgärda problem där inga taggar returneras när Get-AzureRmKeyVault -Tag körs</span><span class="sxs-lookup"><span data-stu-id="faf11-500">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="faf11-501">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="faf11-501">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="faf11-502">Offentlig lansering av cmdletar för Policy Insights</span><span class="sxs-lookup"><span data-stu-id="faf11-502">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="faf11-503">Använd API-version 2018-04-04</span><span class="sxs-lookup"><span data-stu-id="faf11-503">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="faf11-504">Lägg till PolicyDefinitionReferenceId i resultaten för Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="faf11-504">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="faf11-505">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="faf11-505">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="faf11-506">Parametern -Vault har lagts till i cmdletarna för RecoveryServices.Backup.</span><span class="sxs-lookup"><span data-stu-id="faf11-506">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="faf11-507">När den godkänns åsidosätts cmdleten Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="faf11-507">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="faf11-508">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="faf11-508">AzureRM.Sql</span></span>
* <span data-ttu-id="faf11-509">Exemplet i hjälpfilen för Get-AzureRmSqlDatabaseExpanded har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="faf11-509">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="faf11-510">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="faf11-510">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="faf11-511">Hjälpfilen för Add-AzureRmTrafficManagerEndpointConfig har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="faf11-511">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="faf11-512">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="faf11-512">AzureRM.Websites</span></span>
* <span data-ttu-id="faf11-513">”Set-AzureRmWebApp” har uppdaterats så att den inte skriver över appinställningarna när du använder -AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="faf11-513">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="faf11-514">”New-AzureRMWebAppSlot” har uppdaterats för att visa att AppServicePlan är en valfri parameter</span><span class="sxs-lookup"><span data-stu-id="faf11-514">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="faf11-515">6.2.1 – juni 2018</span><span class="sxs-lookup"><span data-stu-id="faf11-515">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="faf11-516">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="faf11-516">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="faf11-517">PSWorkspace-modellen har uppdaterats för att tillåta att nätverket använder typ som en parameter</span><span class="sxs-lookup"><span data-stu-id="faf11-517">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="faf11-518">6.2.0 – juni 2018</span><span class="sxs-lookup"><span data-stu-id="faf11-518">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="faf11-519">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="faf11-519">AzureRM.Profile</span></span>
* <span data-ttu-id="faf11-520">Åtgärda problemet med att version 10.0.3 av Newtonsoft.Json inte lästes in vid modulimporten</span><span class="sxs-lookup"><span data-stu-id="faf11-520">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="faf11-521">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="faf11-521">AzureRM.Compute</span></span>
* <span data-ttu-id="faf11-522">VMSS VM-uppdateringsfunktion</span><span class="sxs-lookup"><span data-stu-id="faf11-522">VMSS VM Update feature</span></span>
    - <span data-ttu-id="faf11-523">Cmdletarna Update-AzureRmVmssVM och New-AzureRmVMDataDisk har lagts till</span><span class="sxs-lookup"><span data-stu-id="faf11-523">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="faf11-524">Lägg till parametern VirtualMachineScaleSetVM till cmdleten Add-AzureRmVMDataDisk så att det går att lägga till en datadisk i den virtuella Vmss-datorn.</span><span class="sxs-lookup"><span data-stu-id="faf11-524">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="faf11-525">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="faf11-525">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="faf11-526">SDK:n för ADF .Net har uppdaterats till version 0.8.0-preview som innehåller följande ändringar:</span><span class="sxs-lookup"><span data-stu-id="faf11-526">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="faf11-527">Åtgärden för att konfigurera fabrikslagringsplatsen har lagts till</span><span class="sxs-lookup"><span data-stu-id="faf11-527">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="faf11-528">QuickBooks LinkedService har uppdaterats för att visa egenskaperna consumerKey och consumerSecret</span><span class="sxs-lookup"><span data-stu-id="faf11-528">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="faf11-529">Flera modelltyper från SecretBase till Object har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="faf11-529">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="faf11-530">Utlösaren Blob Events har lagts till</span><span class="sxs-lookup"><span data-stu-id="faf11-530">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="faf11-531">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="faf11-531">AzureRM.KeyVault</span></span>
* <span data-ttu-id="faf11-532">Uppdatera dokumentation med exempel på utdata</span><span class="sxs-lookup"><span data-stu-id="faf11-532">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="faf11-533">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="faf11-533">AzureRM.Network</span></span>
* <span data-ttu-id="faf11-534">Aktivera Trafikanalys-parametrar på Network Watcher-cmdletar</span><span class="sxs-lookup"><span data-stu-id="faf11-534">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="faf11-535">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="faf11-535">AzureRM.Resources</span></span>
* <span data-ttu-id="faf11-536">Åtgärda problemet med egenskapen "Properties" för objekt(en) "PSResource" som returneras från "Get-AzureRmResource"</span><span class="sxs-lookup"><span data-stu-id="faf11-536">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="faf11-537">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="faf11-537">AzureRM.Scheduler</span></span>
* <span data-ttu-id="faf11-538">Åtgärda problemet med att nya autentiseringsvärden inte anges vid uppdatering av ServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="faf11-538">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="faf11-539">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="faf11-539">AzureRM.Sql</span></span>
* <span data-ttu-id="faf11-540">Följande cmdletar har uppdaterats med valfri LicenseType-parameter</span><span class="sxs-lookup"><span data-stu-id="faf11-540">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="faf11-541">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="faf11-541">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="faf11-542">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="faf11-542">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="faf11-543">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="faf11-543">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="faf11-544">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="faf11-544">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="faf11-545">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="faf11-545">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="faf11-546">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="faf11-546">AzureRM.Websites</span></span>
* <span data-ttu-id="faf11-547">New-AzureRMWebApp har uppdaterats för att använda vanliga algoritmer från biblioteket Strategy.</span><span class="sxs-lookup"><span data-stu-id="faf11-547">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="faf11-548">6.1.0 – maj 2018</span><span class="sxs-lookup"><span data-stu-id="faf11-548">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="faf11-549">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="faf11-549">AzureRM.Profile</span></span>
* <span data-ttu-id="faf11-550">Åtgärda problem där en körning av Clear-AzureRmContext skulle bevara en tom kontext med namnet på den föregående standardkontexten som gjorde att användaren inte kunde skapa en ny kontext med det gamla namnet</span><span class="sxs-lookup"><span data-stu-id="faf11-550">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="faf11-551">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="faf11-551">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="faf11-552">Aktivera Gateway associerings- och avassocieringsåtgärder på AS.</span><span class="sxs-lookup"><span data-stu-id="faf11-552">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="faf11-553">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="faf11-553">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="faf11-554">Stöd för ApiVersions, ApiReleases och ApiRevisions har lagts till</span><span class="sxs-lookup"><span data-stu-id="faf11-554">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="faf11-555">Stöd för serverdelen på ServiceFabric har lagts till</span><span class="sxs-lookup"><span data-stu-id="faf11-555">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="faf11-556">Stöd för Application Insights-loggare har lagts till</span><span class="sxs-lookup"><span data-stu-id="faf11-556">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="faf11-557">Stöd för att identifiera SKU:n ”Basic” som en giltig SKU för Api Management-tjänsten har lagts till</span><span class="sxs-lookup"><span data-stu-id="faf11-557">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="faf11-558">Stöd för att installera certifikat som utfärdats av privata certifikatutfärdare som rot eller certifikatutfärdare har lagts till</span><span class="sxs-lookup"><span data-stu-id="faf11-558">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="faf11-559">Stöd för att godkänna anpassade SSL-certifikat via KeyVault och flera proxy-värdnamn har lagts till</span><span class="sxs-lookup"><span data-stu-id="faf11-559">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="faf11-560">Stöd för MSI-identitet har lagts till</span><span class="sxs-lookup"><span data-stu-id="faf11-560">Added support for MSI identity</span></span>
* <span data-ttu-id="faf11-561">Stöd för att godkänna principer via URL har lagts till. Obs! Följande cmdletar blir inaktuella i framtida versioner</span><span class="sxs-lookup"><span data-stu-id="faf11-561">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="faf11-562">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="faf11-562">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="faf11-563">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="faf11-563">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="faf11-564">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="faf11-564">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="faf11-565">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="faf11-565">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="faf11-566">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="faf11-566">AzureRM.Batch</span></span>
* <span data-ttu-id="faf11-567">Släpp nya cmdleten Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="faf11-567">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="faf11-568">Släpp nya cmdleten Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="faf11-568">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="faf11-569">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="faf11-569">AzureRM.Consumption</span></span>
* <span data-ttu-id="faf11-570">Lägg till nya parametrar Expand, ResourceGroup, InstanceName, InstanceId, Tags och Top på cmdleten Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="faf11-570">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="faf11-571">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="faf11-571">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="faf11-572">Åtgärda exempel för Export AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="faf11-572">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="faf11-573">Åtgärda undantag för null-parameter för rekursivt ärende i Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="faf11-573">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="faf11-574">Åtgärda hjälpfilerna för Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="faf11-574">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="faf11-575">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="faf11-575">AzureRM.Network</span></span>
* <span data-ttu-id="faf11-576">Öka nätverkets SDK-version från förhandsversionen 18.0.0 till förhandsversionen 19.0.0</span><span class="sxs-lookup"><span data-stu-id="faf11-576">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="faf11-577">Cmdlet har lagts till för att skapa protokollinformation</span><span class="sxs-lookup"><span data-stu-id="faf11-577">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="faf11-578">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="faf11-578">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="faf11-579">Cmdlet har lagts till för att lägga till en ny kretsanslutning till en befintlig expressroute-krets.</span><span class="sxs-lookup"><span data-stu-id="faf11-579">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="faf11-580">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="faf11-580">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="faf11-581">Cmdlet har lagts till för att ta bort en kretsanslutning från en befintlig expressroute-krets.</span><span class="sxs-lookup"><span data-stu-id="faf11-581">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="faf11-582">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="faf11-582">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="faf11-583">Cmdlet har lagts till för att hämta en kretsanslutning</span><span class="sxs-lookup"><span data-stu-id="faf11-583">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="faf11-584">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="faf11-584">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="faf11-585">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="faf11-585">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="faf11-586">Användning med serverautentisering med genererade certifikat (problem #5998) har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="faf11-586">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="faf11-587">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="faf11-587">AzureRM.Sql</span></span>
* <span data-ttu-id="faf11-588">Cmdletar för granskning för att ta bort AuditActions eller AuditActionGroups har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="faf11-588">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="faf11-589">Åtgärdade problem med Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy vid konfigurering av en ny flexibel bevarandeprincip där kommandot misslyckas med ett meddelande om att konfigurering av långsiktig bevarandeprincip med Azure Recovery Service-valv och principen inte längre stöds,</span><span class="sxs-lookup"><span data-stu-id="faf11-589">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="faf11-590">och att en begäran med den nya flexibla bevarandeprincipen ska skickas.</span><span class="sxs-lookup"><span data-stu-id="faf11-590">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="faf11-591">Uppdatera alla Azure Sql Database/ElasticPool Creation/Update-relaterade cmdletar för att använda det nya databas-API:et som stöder SKU-egenskaper för skalnings- och nivårelaterade egenskaper.</span><span class="sxs-lookup"><span data-stu-id="faf11-591">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="faf11-592">Cmdletar har uppdaterats, inklusive:</span><span class="sxs-lookup"><span data-stu-id="faf11-592">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="faf11-593">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="faf11-593">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="faf11-594">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="faf11-594">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="faf11-595">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="faf11-595">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="faf11-596">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="faf11-596">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="faf11-597">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="faf11-597">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="faf11-598">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="faf11-598">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="faf11-599">Uppdatera parametrarna för Get-AzureRmTrafficManagerProfile så att ResourceGroupName-parametern blir obligatorisk när du använder Name-parametern.</span><span class="sxs-lookup"><span data-stu-id="faf11-599">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
