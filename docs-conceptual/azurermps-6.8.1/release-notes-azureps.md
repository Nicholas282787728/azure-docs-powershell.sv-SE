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
ms.openlocfilehash: f4f3141998be14f0b5b223aed1af283534bf061d
ms.sourcegitcommit: bc88e64c494337821274d6a66c1edad656c119c5
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/20/2018
ms.locfileid: "46300841"
---
# <a name="release-notes"></a><span data-ttu-id="c7408-103">Viktig information</span><span class="sxs-lookup"><span data-stu-id="c7408-103">Release notes</span></span>

<span data-ttu-id="c7408-104">Det här är en lista över ändringar som har gjorts i Azure PowerShell i den här versionen.</span><span class="sxs-lookup"><span data-stu-id="c7408-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="681---august-2018"></a><span data-ttu-id="c7408-105">6.8.1 – augusti 2018</span><span class="sxs-lookup"><span data-stu-id="c7408-105">6.8.1 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="c7408-106">Allmänt</span><span class="sxs-lookup"><span data-stu-id="c7408-106">General</span></span>
* <span data-ttu-id="c7408-107">Problem med standardresursgrupp som inte har konfigurerats har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="c7408-107">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="c7408-108">Uppdaterade Common Runtime-sammansättningar</span><span class="sxs-lookup"><span data-stu-id="c7408-108">Updated common runtime assemblies</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="c7408-109">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c7408-109">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="c7408-110">Problem med standardresursgrupp som inte har konfigurerats har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="c7408-110">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="c7408-111">Åtgärdat problem https://github.com/Azure/azure-powershell/issues/6603</span><span class="sxs-lookup"><span data-stu-id="c7408-111">Fixed issue https://github.com/Azure/azure-powershell/issues/6603</span></span>
    - <span data-ttu-id="c7408-112">Import-AzureRmApiManagementApi- och \*-AzureRmApiManagementCertificate-cmdletar kan nu hantera relativa sökvägar</span><span class="sxs-lookup"><span data-stu-id="c7408-112">Import-AzureRmApiManagementApi and \*-AzureRmApiManagementCertificate cmdlets now handle relative Paths</span></span>
* <span data-ttu-id="c7408-113">Åtgärdat problem https://github.com/Azure/azure-powershell/issues/6879</span><span class="sxs-lookup"><span data-stu-id="c7408-113">Fixed issue https://github.com/Azure/azure-powershell/issues/6879</span></span>
    - <span data-ttu-id="c7408-114">CertificateInformation är en inställbar egenskap som gör att Set-AzureRmApiManagement-cmdleten fungerar ordentligt.</span><span class="sxs-lookup"><span data-stu-id="c7408-114">The CertificateInformation is a settable property allowing for Set-AzureRmApiManagement cmdlet to work property.</span></span> <span data-ttu-id="c7408-115">Åtgärdat genom uppgradering till NuGet för 4.0.4-preview</span><span class="sxs-lookup"><span data-stu-id="c7408-115">Fixed by upgrading to 4.0.4-preview nuget</span></span>
* <span data-ttu-id="c7408-116">Åtgärdat problem https://github.com/Azure/azure-powershell/issues/6853</span><span class="sxs-lookup"><span data-stu-id="c7408-116">Fixed issue https://github.com/Azure/azure-powershell/issues/6853</span></span>
    - <span data-ttu-id="c7408-117">Odata-filtret för sökning efter namn på produkt har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="c7408-117">Fixed the Odata filter for Search by Name on Product</span></span>
* <span data-ttu-id="c7408-118">Åtgärdat problem https://github.com/Azure/azure-powershell/issues/6814</span><span class="sxs-lookup"><span data-stu-id="c7408-118">Fixed issue https://github.com/Azure/azure-powershell/issues/6814</span></span>
    - <span data-ttu-id="c7408-119">Odata-filtret för sökning efter namn på API har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="c7408-119">Fixed the Odata filter for Search by Name on Api</span></span>
* <span data-ttu-id="c7408-120">Stöd har lagts till för AzureMonitor-loggare</span><span class="sxs-lookup"><span data-stu-id="c7408-120">Added support for AzureMonitor logger</span></span>


#### <a name="azurermcompute"></a><span data-ttu-id="c7408-121">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c7408-121">AzureRM.Compute</span></span>
* <span data-ttu-id="c7408-122">Ett problem med att mål saknas i felutdata har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="c7408-122">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="c7408-123">Problem med lagringskontotyper för virtuell dator med en hanterad disk har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="c7408-123">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="c7408-124">Problem med standardresursgrupp som inte har konfigurerats har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="c7408-124">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="c7408-125">Åtgärda cmdletar för AEM-tillägg för andra miljöer, till exempel Azure Kina</span><span class="sxs-lookup"><span data-stu-id="c7408-125">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="c7408-126">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c7408-126">AzureRM.Network</span></span>
* <span data-ttu-id="c7408-127">Standardvisning av cmdlet-utdata har ändrats för att visas i tabellvy</span><span class="sxs-lookup"><span data-stu-id="c7408-127">Changed default cmdlet output presentation to table view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="c7408-128">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="c7408-128">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="c7408-129">Åtgärda fel i Update-AzureRmPowerBIEmbeddedCapacity vid försök att skala pausad kapacitet</span><span class="sxs-lookup"><span data-stu-id="c7408-129">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>


#### <a name="azurermresources"></a><span data-ttu-id="c7408-130">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="c7408-130">AzureRM.Resources</span></span>
* <span data-ttu-id="c7408-131">Ett problem med att skapa hanterade program från MarketPlace har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="c7408-131">Fixed issue with creating managed applications from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="c7408-132">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c7408-132">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="c7408-133">Åtgärdade problem</span><span class="sxs-lookup"><span data-stu-id="c7408-133">Fixed issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="c7408-134">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="c7408-134">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="c7408-135">Stöd har lagts till för trafikroutningsmetoden MultiValue</span><span class="sxs-lookup"><span data-stu-id="c7408-135">Added Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="c7408-136">Ny parameter, ”MaxReturn”, för MultiValue-routning</span><span class="sxs-lookup"><span data-stu-id="c7408-136">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="c7408-137">Stöd har lagts till för trafikroutningsmetod för undernät</span><span class="sxs-lookup"><span data-stu-id="c7408-137">Added Support for the Subnet routing method</span></span>
    - <span data-ttu-id="c7408-138">Stöd för IP-adressintervall (undernät) i slutpunkter</span><span class="sxs-lookup"><span data-stu-id="c7408-138">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="c7408-139">Stöd har lagts till för anpassade rubriker i profiler</span><span class="sxs-lookup"><span data-stu-id="c7408-139">Added Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="c7408-140">Stöd har lagts till för förväntade statuskodintervall i profiler</span><span class="sxs-lookup"><span data-stu-id="c7408-140">Added Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="c7408-141">Stöd har lagts till för anpassade rubriker i slutpunkter</span><span class="sxs-lookup"><span data-stu-id="c7408-141">Added Support for Custom Headers in endpoints</span></span>

## <a name="680---august-2018"></a><span data-ttu-id="c7408-142">6.8.0 – augusti 2018</span><span class="sxs-lookup"><span data-stu-id="c7408-142">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="c7408-143">Allmänt</span><span class="sxs-lookup"><span data-stu-id="c7408-143">General</span></span>
* <span data-ttu-id="c7408-144">Problem med standardresursgrupp som inte har konfigurerats har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="c7408-144">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="c7408-145">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c7408-145">AzureRM.Profile</span></span>
* <span data-ttu-id="c7408-146">Utgångsegenskap har lagts till i token som returneras under Connect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="c7408-146">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="c7408-147">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c7408-147">AzureRM.Compute</span></span>
* <span data-ttu-id="c7408-148">Ett problem med att mål saknas i felutdata har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="c7408-148">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="c7408-149">Problem med lagringskontotyper för virtuell dator med en hanterad disk har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="c7408-149">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="c7408-150">Åtgärda cmdletar för AEM-tillägg för andra miljöer, till exempel Azure Kina</span><span class="sxs-lookup"><span data-stu-id="c7408-150">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="c7408-151">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="c7408-151">AzureRM.IotHub</span></span>
* <span data-ttu-id="c7408-152">Korrigera exempel för New-AzureRmIotHubExportDevices och New-AzureRmIotHubImportDevices</span><span class="sxs-lookup"><span data-stu-id="c7408-152">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="c7408-153">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c7408-153">AzureRM.Network</span></span>
* <span data-ttu-id="c7408-154">Standardmodeller har ändrats för att visas i tabellvy</span><span class="sxs-lookup"><span data-stu-id="c7408-154">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="c7408-155">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="c7408-155">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="c7408-156">Åtgärda fel i Update-AzureRmPowerBIEmbeddedCapacity vid försök att skala pausad kapacitet</span><span class="sxs-lookup"><span data-stu-id="c7408-156">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="c7408-157">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="c7408-157">AzureRM.Resources</span></span>
* <span data-ttu-id="c7408-158">Ett problem med att skapa hanterade program från MarketPlace har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="c7408-158">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="c7408-159">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c7408-159">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="c7408-160">Korrigeringar för problem</span><span class="sxs-lookup"><span data-stu-id="c7408-160">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="c7408-161">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="c7408-161">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="c7408-162">Stöd för trafikroutningsmetoden MultiValue</span><span class="sxs-lookup"><span data-stu-id="c7408-162">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="c7408-163">Ny parameter, ”MaxReturn”, för MultiValue-routning</span><span class="sxs-lookup"><span data-stu-id="c7408-163">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="c7408-164">Stöd för trafikroutningsmetod för undernät</span><span class="sxs-lookup"><span data-stu-id="c7408-164">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="c7408-165">Stöd för IP-adressintervall (undernät) i slutpunkter</span><span class="sxs-lookup"><span data-stu-id="c7408-165">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="c7408-166">Stöd för anpassade rubriker i profiler</span><span class="sxs-lookup"><span data-stu-id="c7408-166">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="c7408-167">Stöd för förväntade statuskodintervall i profiler</span><span class="sxs-lookup"><span data-stu-id="c7408-167">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="c7408-168">Stöd för anpassade rubriker i slutpunkter</span><span class="sxs-lookup"><span data-stu-id="c7408-168">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="c7408-169">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="c7408-169">AzureRM.Websites</span></span>
* <span data-ttu-id="c7408-170">Problem med standardresursgrupp som inte har konfigurerats korrekt har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="c7408-170">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="c7408-171">6.7.0 – augusti 2018</span><span class="sxs-lookup"><span data-stu-id="c7408-171">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="c7408-172">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c7408-172">AzureRM.Profile</span></span>
* <span data-ttu-id="c7408-173">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c7408-173">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="c7408-174">Lägg till användar-id i standardkontextnamnet för att undvika kontextkonflikter</span><span class="sxs-lookup"><span data-stu-id="c7408-174">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="c7408-175">Åtgärda problem med Clear-AzureRmContext som orsakade problem med att välja en kontext #6398</span><span class="sxs-lookup"><span data-stu-id="c7408-175">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="c7408-176">Aktivera den klientorganisationsdomän som ska skickas till parametern -TenantId för Connect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="c7408-176">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="c7408-177">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="c7408-177">Azure.Storage</span></span>
* <span data-ttu-id="c7408-178">Ta bort begränsningen på 5 TB för Azure-filresurskvoten</span><span class="sxs-lookup"><span data-stu-id="c7408-178">Remove the 5TB limitation for Azure File Share quota</span></span>
- <span data-ttu-id="c7408-179">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="c7408-179">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="c7408-180">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="c7408-180">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="c7408-181">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c7408-181">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="c7408-182">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="c7408-182">Azure.AnalysisServices</span></span>
* <span data-ttu-id="c7408-183">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c7408-183">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="c7408-184">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c7408-184">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="c7408-185">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c7408-185">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="c7408-186">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="c7408-186">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="c7408-187">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c7408-187">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="c7408-188">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="c7408-188">AzureRM.Automation</span></span>
* <span data-ttu-id="c7408-189">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c7408-189">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="c7408-190">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="c7408-190">AzureRM.Backup</span></span>
* <span data-ttu-id="c7408-191">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c7408-191">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="c7408-192">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="c7408-192">AzureRM.Batch</span></span>
* <span data-ttu-id="c7408-193">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c7408-193">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="c7408-194">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="c7408-194">AzureRM.Billing</span></span>
* <span data-ttu-id="c7408-195">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c7408-195">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="c7408-196">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="c7408-196">AzureRM.Cdn</span></span>
* <span data-ttu-id="c7408-197">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c7408-197">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="c7408-198">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="c7408-198">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="c7408-199">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c7408-199">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="c7408-200">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c7408-200">AzureRM.Compute</span></span>
* <span data-ttu-id="c7408-201">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c7408-201">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="c7408-202">Lägg till parametern EvictionPolicy i New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="c7408-202">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="c7408-203">Använd standardplatsen i DiskFileParameterSet för New-AzureRmVm om ingen plats har angetts.</span><span class="sxs-lookup"><span data-stu-id="c7408-203">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="c7408-204">Korrigera parameterbeskrivningen i Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="c7408-204">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="c7408-205">Korrigera cmdleten Get-AzureRmVMDiskEncryptionStatus för vissa singlepass-relaterade scenarier</span><span class="sxs-lookup"><span data-stu-id="c7408-205">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="c7408-206">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="c7408-206">AzureRM.Consumption</span></span>
* <span data-ttu-id="c7408-207">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c7408-207">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="c7408-208">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="c7408-208">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="c7408-209">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c7408-209">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="c7408-210">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c7408-210">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="c7408-211">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c7408-211">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="c7408-212">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="c7408-212">AzureRM.DataFactories</span></span>
* <span data-ttu-id="c7408-213">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c7408-213">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="c7408-214">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="c7408-214">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="c7408-215">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c7408-215">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="c7408-216">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="c7408-216">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="c7408-217">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c7408-217">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="c7408-218">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c7408-218">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="c7408-219">Korrigera felsökning när DebugPreference anges från powershell-kommandoraden</span><span class="sxs-lookup"><span data-stu-id="c7408-219">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="c7408-220">Uppdatera exemplet för Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="c7408-220">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="c7408-221">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c7408-221">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="c7408-222">Uppdatera exemplet för Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="c7408-222">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="c7408-223">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="c7408-223">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="c7408-224">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c7408-224">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="c7408-225">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="c7408-225">AzureRM.Dns</span></span>
* <span data-ttu-id="c7408-226">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c7408-226">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="c7408-227">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="c7408-227">AzureRM.EventGrid</span></span>
* <span data-ttu-id="c7408-228">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c7408-228">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="c7408-229">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="c7408-229">AzureRM.EventHub</span></span>
* <span data-ttu-id="c7408-230">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c7408-230">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="c7408-231">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="c7408-231">AzureRM.HDInsight</span></span>
* <span data-ttu-id="c7408-232">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c7408-232">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="c7408-233">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="c7408-233">AzureRM.Insights</span></span>
* <span data-ttu-id="c7408-234">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c7408-234">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="c7408-235">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="c7408-235">AzureRM.IotHub</span></span>
* <span data-ttu-id="c7408-236">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c7408-236">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="c7408-237">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c7408-237">AzureRM.KeyVault</span></span>
* <span data-ttu-id="c7408-238">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c7408-238">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="c7408-239">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="c7408-239">AzureRM.LogicApp</span></span>
* <span data-ttu-id="c7408-240">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c7408-240">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="c7408-241">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="c7408-241">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="c7408-242">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c7408-242">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="c7408-243">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="c7408-243">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="c7408-244">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c7408-244">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="c7408-245">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="c7408-245">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="c7408-246">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c7408-246">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="c7408-247">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="c7408-247">AzureRM.Media</span></span>
* <span data-ttu-id="c7408-248">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c7408-248">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="c7408-249">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c7408-249">AzureRM.Network</span></span>
* <span data-ttu-id="c7408-250">Exempel för Set-AzureRmLocalNetworkGateway har lagts till</span><span class="sxs-lookup"><span data-stu-id="c7408-250">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="c7408-251">Exempel och beskrivningar för Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey och New-AzureRmVirtualNetworkGatewayConnection har lagts till</span><span class="sxs-lookup"><span data-stu-id="c7408-251">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="c7408-252">Exempel för Remove-AzureRmVirtualNetworkGatewayIpConfig och Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c7408-252">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="c7408-253">Exempel för Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey har lagts till</span><span class="sxs-lookup"><span data-stu-id="c7408-253">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="c7408-254">Exempel för Set-AzureRmVirtualNetworkGatewayConnectionSharedKey har lagts till</span><span class="sxs-lookup"><span data-stu-id="c7408-254">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="c7408-255">Exempel för Set-AzureRmVirtualNetworkGatewayConnection har lagts till</span><span class="sxs-lookup"><span data-stu-id="c7408-255">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="c7408-256">Cmdletar för ApplicationSecurityGroup, RouteTable and Usage har genererats om med den senaste kodgeneratorn</span><span class="sxs-lookup"><span data-stu-id="c7408-256">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="c7408-257">Förtydligade ett felmeddelande för Get-AzureRmVirtualNetworkSubnetConfig vid försök att hämta ett undernät som inte avslutas</span><span class="sxs-lookup"><span data-stu-id="c7408-257">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="c7408-258">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="c7408-258">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="c7408-259">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c7408-259">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="c7408-260">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="c7408-260">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="c7408-261">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c7408-261">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="c7408-262">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="c7408-262">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="c7408-263">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c7408-263">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="c7408-264">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="c7408-264">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="c7408-265">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c7408-265">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="c7408-266">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c7408-266">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="c7408-267">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c7408-267">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="c7408-268">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c7408-268">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="c7408-269">Lade till principfilter i cmdleten Get-AzureRmRecoveryServicesBackItem.</span><span class="sxs-lookup"><span data-stu-id="c7408-269">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="c7408-270">Kommandot returnerar listan med säkerhetskopieringsobjekt som skyddas av det angivna princip-ID:t.</span><span class="sxs-lookup"><span data-stu-id="c7408-270">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="c7408-271">Microsoft.Azure.Management.RecoveryServices.Backup uppdaterades till förhandsversionen av 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="c7408-271">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="c7408-272">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c7408-272">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="c7408-273">Parametern TargetResourceGroupName lades till i Restore-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="c7408-273">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="c7408-274">Den resursgrupp som de hanterade diskarna återställs till.</span><span class="sxs-lookup"><span data-stu-id="c7408-274">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="c7408-275">Gäller för säkerhetskopiering av virtuell dator med hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="c7408-275">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="c7408-276">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c7408-276">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="c7408-277">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c7408-277">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="c7408-278">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="c7408-278">AzureRM.RedisCache</span></span>
* <span data-ttu-id="c7408-279">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c7408-279">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="c7408-280">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="c7408-280">AzureRM.Relay</span></span>
* <span data-ttu-id="c7408-281">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c7408-281">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="c7408-282">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="c7408-282">AzureRM.Resources</span></span>
* <span data-ttu-id="c7408-283">Distribution av supportmall i prenumerationsomfånget.</span><span class="sxs-lookup"><span data-stu-id="c7408-283">Support template deployment at subscription scope.</span></span> <span data-ttu-id="c7408-284">Lägg till nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="c7408-284">Add new Cmdlets:</span></span>
    - <span data-ttu-id="c7408-285">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="c7408-285">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="c7408-286">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="c7408-286">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="c7408-287">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="c7408-287">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="c7408-288">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="c7408-288">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="c7408-289">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="c7408-289">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="c7408-290">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="c7408-290">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="c7408-291">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="c7408-291">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="c7408-292">Korrigera ett problem där fel inträffar när en kontext skickas till Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="c7408-292">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="c7408-293">Korrigera exempel i New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="c7408-293">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="c7408-294">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c7408-294">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="c7408-295">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="c7408-295">AzureRM.Scheduler</span></span>
* <span data-ttu-id="c7408-296">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c7408-296">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="c7408-297">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c7408-297">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="c7408-298">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c7408-298">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="c7408-299">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c7408-299">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="c7408-300">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c7408-300">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="c7408-301">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="c7408-301">AzureRM.Sql</span></span>
* <span data-ttu-id="c7408-302">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c7408-302">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="c7408-303">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="c7408-303">AzureRM.Storage</span></span>
* <span data-ttu-id="c7408-304">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c7408-304">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="c7408-305">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="c7408-305">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="c7408-306">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c7408-306">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="c7408-307">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="c7408-307">AzureRM.Tags</span></span>
* <span data-ttu-id="c7408-308">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c7408-308">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="c7408-309">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="c7408-309">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="c7408-310">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c7408-310">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="c7408-311">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="c7408-311">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="c7408-312">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c7408-312">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="c7408-313">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="c7408-313">AzureRM.Websites</span></span>
* <span data-ttu-id="c7408-314">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c7408-314">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="c7408-315">6.6.0 – juli 2018</span><span class="sxs-lookup"><span data-stu-id="c7408-315">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="c7408-316">Allmänt</span><span class="sxs-lookup"><span data-stu-id="c7408-316">General</span></span>
* <span data-ttu-id="c7408-317">Alla hjälpfiler har uppdaterats för att ta med fullständiga parametertyper och korrekta indata-/utdatatyper.</span><span class="sxs-lookup"><span data-stu-id="c7408-317">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="c7408-318">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c7408-318">AzureRM.Profile</span></span>
* <span data-ttu-id="c7408-319">Common.Strategy-biblioteket har uppdaterats för att kunna verifiera att den aktuella konfigurationsfilen för en resurs är kompatibel med målresursen.</span><span class="sxs-lookup"><span data-stu-id="c7408-319">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="c7408-320">ps1xml-typer har lagts till i Common.Storage</span><span class="sxs-lookup"><span data-stu-id="c7408-320">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="c7408-321">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="c7408-321">Azure.Storage</span></span>
* <span data-ttu-id="c7408-322">Lade till stöd för hämtning av lagringskontext från DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7408-322">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="c7408-323">Lade till Ps1XmlAttribute till utdatatypegenskaper för cmdletar.</span><span class="sxs-lookup"><span data-stu-id="c7408-323">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="c7408-324">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c7408-324">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="c7408-325">Åtgärdat problem https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="c7408-325">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="c7408-326">En bugg har åtgärdats i Automapper för att översätta PsApiManagementApi till ApiContract</span><span class="sxs-lookup"><span data-stu-id="c7408-326">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="c7408-327">Åtgärdat problem https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="c7408-327">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="c7408-328">En bugg har åtgärdats i File.Save för att inte överbelasta kodningstypen</span><span class="sxs-lookup"><span data-stu-id="c7408-328">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="c7408-329">Åtgärdat problem https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="c7408-329">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="c7408-330">Har uppgraderats till Nuget-versionen 4.0.3 vilket åtgärdar mönsterundantaget på apiId</span><span class="sxs-lookup"><span data-stu-id="c7408-330">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="c7408-331">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c7408-331">AzureRM.Compute</span></span>
* <span data-ttu-id="c7408-332">Åtgärda problem med fel vid skapandet av en virtuell dator med hjälp av DiskFileParameterSet i New-AzureRmVm på grund av namnbyte på PremiumLRS-lagringskontotypen.</span><span class="sxs-lookup"><span data-stu-id="c7408-332">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="c7408-333">Åtgärda cmdleten Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="c7408-333">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="c7408-334">Uppdatera Get-AzureRmAvailabilitySet för att aktivera funktionen för att lista alla tillgänglighetsuppsättningar i en prenumeration.</span><span class="sxs-lookup"><span data-stu-id="c7408-334">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="c7408-335">(Parametern ResouceGroupName är nu frivillig.)</span><span class="sxs-lookup"><span data-stu-id="c7408-335">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="c7408-336">Uppdatera SimpleParameterSet för "New-AzureRmVm" för att aktivera accelererat nätverk på berättigade virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="c7408-336">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="c7408-337">Uppdatera den enkla parameteruppsättningen för New-AzureRmVmss så att det inte går att skapa de virtuella datorerna när en användarangiven lastbalanserare redan finns.</span><span class="sxs-lookup"><span data-stu-id="c7408-337">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="c7408-338">Uppdatera exempel för New-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="c7408-338">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="c7408-339">Lägg till exempel för "New-AzureRmVM"</span><span class="sxs-lookup"><span data-stu-id="c7408-339">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="c7408-340">Uppdatera beskrivning för Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="c7408-340">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="c7408-341">Uppdatera Exempel 1 för Set-AzureRmVMBginfoExtension för stavningskontroll och prefix.</span><span class="sxs-lookup"><span data-stu-id="c7408-341">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="c7408-342">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="c7408-342">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="c7408-343">ADF .Net SDK-versionen har uppdaterats till 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="c7408-343">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="c7408-344">Stöd för delning av Integration Runtime (lokal installation) mellan datafabriker.</span><span class="sxs-lookup"><span data-stu-id="c7408-344">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="c7408-345">Lägg till ny parameter – SharedIntegrationRuntimeResourceId i cmdleten Set-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="c7408-345">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="c7408-346">Lägg till ny valfri parameter – LinkedDataFactoryName i cmdleten Remove-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="c7408-346">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="c7408-347">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c7408-347">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="c7408-348">DataPlane SDK-versionen (Microsoft.Azure.DataLake.Store) har uppdaterats till 1.1.9</span><span class="sxs-lookup"><span data-stu-id="c7408-348">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="c7408-349">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="c7408-349">AzureRM.EventHub</span></span>
* <span data-ttu-id="c7408-350">Piping för InputObject and ResourceId i borttagna cmdletar har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="c7408-350">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="c7408-351">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="c7408-351">AzureRM.Insights</span></span>
* <span data-ttu-id="c7408-352">Formatering har åtgärdats för OutputType i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="c7408-352">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="c7408-353">Använda Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span><span class="sxs-lookup"><span data-stu-id="c7408-353">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="c7408-354">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c7408-354">AzureRM.KeyVault</span></span>
* <span data-ttu-id="c7408-355">Åtgärda problem med piping i Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c7408-355">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="c7408-356">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c7408-356">AzureRM.Network</span></span>
* <span data-ttu-id="c7408-357">Exempel har lagts till för LoadBalancerInboundNatPoolConfig-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="c7408-357">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="c7408-358">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="c7408-358">AzureRM.Resources</span></span>
* <span data-ttu-id="c7408-359">Åtgärda problem när både taggnamn och värde anges för "Get-AzureRmResource"</span><span class="sxs-lookup"><span data-stu-id="c7408-359">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="c7408-360">Åtgärda pipingscenario med "Set-AzureRmResource"</span><span class="sxs-lookup"><span data-stu-id="c7408-360">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="c7408-361">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c7408-361">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="c7408-362">Piping för InputObject and ResourceId i borttagna cmdletar har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="c7408-362">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="c7408-363">några problem har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="c7408-363">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="c7408-364">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="c7408-364">AzureRM.Sql</span></span>
* <span data-ttu-id="c7408-365">Lägg till stöd för Server Advanced Threat Protection med följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="c7408-365">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="c7408-366">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="c7408-366">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="c7408-367">Lägg till stöd för Sårbarhetsbedömning med följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="c7408-367">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="c7408-368">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="c7408-368">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="c7408-369">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="c7408-369">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="c7408-370">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="c7408-370">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="c7408-371">Exempel i Remove-AzureRmSqlServerFirewallRule har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="c7408-371">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="c7408-372">Åtgärda felaktig hantering av datum och tid för andra kulturer än usa-baserade kulturer i Get-AzureSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="c7408-372">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="c7408-373">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="c7408-373">AzureRM.Storage</span></span>
* <span data-ttu-id="c7408-374">Lägg till Ps1XmlAttribute i utdatatypegenskaper för cmdletar</span><span class="sxs-lookup"><span data-stu-id="c7408-374">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="c7408-375">Visa utdata för cmdleten StorageAccount i tabellvyn</span><span class="sxs-lookup"><span data-stu-id="c7408-375">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="c7408-376">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c7408-376">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="c7408-377">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c7408-377">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="c7408-378">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c7408-378">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="c7408-379">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="c7408-379">AzureRM.Tags</span></span>
* <span data-ttu-id="c7408-380">Ta bort felaktig instruktion från hjälpen för cmdleten Tag</span><span class="sxs-lookup"><span data-stu-id="c7408-380">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="c7408-381">6.5.0 – juli 2018</span><span class="sxs-lookup"><span data-stu-id="c7408-381">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="c7408-382">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c7408-382">AzureRM.Profile</span></span>
* <span data-ttu-id="c7408-383">Hjälp för ”Get-AzureRmContextAutosaveSetting” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="c7408-383">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="c7408-384">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="c7408-384">Azure.Storage</span></span>
* <span data-ttu-id="c7408-385">Stöd för uppladdning av blob eller fil med lässkyddad SAS-token</span><span class="sxs-lookup"><span data-stu-id="c7408-385">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="c7408-386">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="c7408-386">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="c7408-387">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="c7408-387">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="c7408-388">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="c7408-388">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="c7408-389">Lägg till den nödvändiga egenskapen ResourceGroupName i AS.</span><span class="sxs-lookup"><span data-stu-id="c7408-389">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="c7408-390">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="c7408-390">AzureRM.Automation</span></span>
* <span data-ttu-id="c7408-391">Uppdatera hjälp och lägg till exempel för ”New-AzureRMAutomationSchedule”</span><span class="sxs-lookup"><span data-stu-id="c7408-391">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="c7408-392">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c7408-392">AzureRM.Compute</span></span>
* <span data-ttu-id="c7408-393">Lägg till parametern -Tag förUpdate/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="c7408-393">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="c7408-394">Lägg till exempel för ”Add-AzureRmVmssExtension”</span><span class="sxs-lookup"><span data-stu-id="c7408-394">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="c7408-395">Lägg till exempel för ”Remove-AzureRmVmssExtension”</span><span class="sxs-lookup"><span data-stu-id="c7408-395">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="c7408-396">Uppdatera hjälp för ”Set-AzureRmVMAccessExtension”</span><span class="sxs-lookup"><span data-stu-id="c7408-396">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="c7408-397">Uppdatera SimpleParameterSet för New-AzureRmVmss för att ställa in SinglePlacementGroup på falskt som standard och lägg till växlingsparametern ”SinglePlacementGroup” som gör att användare kan skapa VMSS i en enda placeringsgrupp.</span><span class="sxs-lookup"><span data-stu-id="c7408-397">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="c7408-398">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="c7408-398">AzureRM.EventHub</span></span>
* <span data-ttu-id="c7408-399">En skrivskyddad egenskap, ”PendingReplicationOperationsCount”, har lagts till för klassen PSEventHubDRConfigurationAttributes som anger antalet väntande replikeringsåtgärder medan replikeringen pågår</span><span class="sxs-lookup"><span data-stu-id="c7408-399">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="c7408-400">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c7408-400">AzureRM.KeyVault</span></span>
* <span data-ttu-id="c7408-401">Uppdatera felmeddelande för Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c7408-401">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="c7408-402">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="c7408-402">AzureRM.LogicApp</span></span>
* <span data-ttu-id="c7408-403">Felet ”parameteruppsättningen gick inte att matcha” har korrigerats i New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="c7408-403">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="c7408-404">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c7408-404">AzureRM.Network</span></span>
* <span data-ttu-id="c7408-405">Aktivera peering mellan virtuella nätverk i flera klienter för Set/Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="c7408-405">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="c7408-406">Nedanstående cmdletar för Application Gateway har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="c7408-406">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="c7408-407">New-AzureRmApplicationGateway: EnableFIPS-flagga har lagts till för stöd för zoner</span><span class="sxs-lookup"><span data-stu-id="c7408-407">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="c7408-408">New-AzureRmApplicationGatewaySku: nya SKU:er, Standard_v2 och WAF_v2, har lagts till</span><span class="sxs-lookup"><span data-stu-id="c7408-408">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="c7408-409">Set-AzureRmApplicationGatewaySku: nya SKU:er, Standard_v2 och WAF_v2, har lagts till</span><span class="sxs-lookup"><span data-stu-id="c7408-409">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="c7408-410">RouteTable-cmdletar har återskapats med den senaste versionen av generatorn</span><span class="sxs-lookup"><span data-stu-id="c7408-410">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="c7408-411">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="c7408-411">AzureRM.Relay</span></span>
* <span data-ttu-id="c7408-412">Markdown-filer har uppdaterats och korrigerar problem med parameternamn i exemplet</span><span class="sxs-lookup"><span data-stu-id="c7408-412">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="c7408-413">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="c7408-413">AzureRM.Resources</span></span>
* <span data-ttu-id="c7408-414">Uppdatera cmdletar för rolltilldelning och rolldefinition:</span><span class="sxs-lookup"><span data-stu-id="c7408-414">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="c7408-415">Ta bort extra anrop för rolldefinitioner som görs som en del av sidindelning.</span><span class="sxs-lookup"><span data-stu-id="c7408-415">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="c7408-416">Åtgärda Get-AzureRMRoleAssignment-cmdlet</span><span class="sxs-lookup"><span data-stu-id="c7408-416">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="c7408-417">Åtgärda parameterfunktioner för kommandot -ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="c7408-417">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="c7408-418">Åtgärda problem med ”Get-AzureRmResource” där ”-ResourceType”-parametern var skiftlägeskänsligt</span><span class="sxs-lookup"><span data-stu-id="c7408-418">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="c7408-419">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c7408-419">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="c7408-420">Parametrar för att stoppa och hoppa över har lagts till i listan över cmdletar</span><span class="sxs-lookup"><span data-stu-id="c7408-420">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="c7408-421">Cmdletar för migrering från Standard- till Premium-namnområden har lagts till:</span><span class="sxs-lookup"><span data-stu-id="c7408-421">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="c7408-422">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="c7408-422">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="c7408-423">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="c7408-423">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="c7408-424">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="c7408-424">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="c7408-425">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="c7408-425">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="c7408-426">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="c7408-426">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="c7408-427">En skrivskyddad egenskap, ”PendingReplicationOperationsCount” har lagts till för klassen PSServiceBusDRConfigurationAttributes som anger antalet väntande replikeringsåtgärder medan replikeringen pågår</span><span class="sxs-lookup"><span data-stu-id="c7408-427">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="c7408-428">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c7408-428">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="c7408-429">Uppdatera exempel för ”New-AzureRmServiceFabricCluster”</span><span class="sxs-lookup"><span data-stu-id="c7408-429">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="c7408-430">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="c7408-430">AzureRM.Sql</span></span>
* <span data-ttu-id="c7408-431">Nya cmdletar för Management.Sql som gör att kunderna kan lägga till certifikat för transparent datakryptering till SQL Server-instans eller en hanterad instans har lagts till</span><span class="sxs-lookup"><span data-stu-id="c7408-431">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="c7408-432">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="c7408-432">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="c7408-433">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="c7408-433">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="c7408-434">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="c7408-434">AzureRM.Websites</span></span>
* <span data-ttu-id="c7408-435">När `Set-AzureRmWebApp -AssignIdentity` och `Set-AzureRmWebAppSlot -AssignIdentity` är inställda på falskt tar de nu bort identitetsegenskapen från platsobjektet. Även förhandsgranskningstaggen tas bort.</span><span class="sxs-lookup"><span data-stu-id="c7408-435">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="c7408-436">`Get-AzureRmWebAppMetrics`, `Get-AzureRmAppServicePlanMetrics`-exempel har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="c7408-436">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="c7408-437">`Set-AzureRmWebApp -PhpVersion` har stöd för ”av” som en giltig php-version</span><span class="sxs-lookup"><span data-stu-id="c7408-437">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="c7408-438">6.4.0 – juli 2018</span><span class="sxs-lookup"><span data-stu-id="c7408-438">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="c7408-439">Allmänt</span><span class="sxs-lookup"><span data-stu-id="c7408-439">General</span></span>
* <span data-ttu-id="c7408-440">Formatering av OutputType i hjälpfiler har korrigerats för de flesta moduler</span><span class="sxs-lookup"><span data-stu-id="c7408-440">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="c7408-441">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c7408-441">AzureRM.Profile</span></span>
* <span data-ttu-id="c7408-442">Ps1Xml-attribut har lagts till för grundläggande utdatatyper</span><span class="sxs-lookup"><span data-stu-id="c7408-442">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="c7408-443">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c7408-443">AzureRM.Compute</span></span>
* <span data-ttu-id="c7408-444">IP-tagg-funktioner för VMSS</span><span class="sxs-lookup"><span data-stu-id="c7408-444">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="c7408-445">"New-AzureRmVmssIpTagConfig"-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="c7408-445">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="c7408-446">IpTag-parameter har lagts till för New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="c7408-446">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="c7408-447">Automatisk återställningsfunktion för operativsystem för VMSS</span><span class="sxs-lookup"><span data-stu-id="c7408-447">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="c7408-448">DisableAutoRollback-parametrar har lagts till för New-AzureRmVmssConfig och Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c7408-448">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="c7408-449">Funktion för uppgraderingshistorik för operativsystem för Vmss</span><span class="sxs-lookup"><span data-stu-id="c7408-449">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="c7408-450">OSUpgradeHistory-växlingsparametern har lagts till för Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c7408-450">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="c7408-451">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="c7408-451">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="c7408-452">Lägg till stöd för katalog-ACL:er med hjälp av följande kommandon:</span><span class="sxs-lookup"><span data-stu-id="c7408-452">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="c7408-453">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="c7408-453">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="c7408-454">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="c7408-454">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="c7408-455">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="c7408-455">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="c7408-456">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c7408-456">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="c7408-457">Lägg till stöd för annullering och förloppsspårning för Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="c7408-457">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="c7408-458">Lägg till stöd för annullering för Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="c7408-458">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="c7408-459">Åtgärda tömning av felsökningsmeddelanden för cmdletar som gör rekursiva åtgärder</span><span class="sxs-lookup"><span data-stu-id="c7408-459">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="c7408-460">Åtgärda platsen för testning av DataLake-cmdletar</span><span class="sxs-lookup"><span data-stu-id="c7408-460">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="c7408-461">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="c7408-461">AzureRM.EventHub</span></span>
* <span data-ttu-id="c7408-462">Parametrar för optimalt maxantal har lagts till i liståtgärds-cmdletarna Get-AzureRmEventHub och Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="c7408-462">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="c7408-463">Ett problem i New-AzureRmEventHub-cmdleten har åtgärdats där minst en parameter behövdes när du skapade en ny EventHub.</span><span class="sxs-lookup"><span data-stu-id="c7408-463">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="c7408-464">Angiven standardparameter har ställts in.</span><span class="sxs-lookup"><span data-stu-id="c7408-464">Provided Default Parameter set.</span></span>
* <span data-ttu-id="c7408-465">Valfri parameter för KeyValue har lagts till för New-AzureRmEventHubKey-cmdleten, vilket gör det möjligt att ange KeyValue.</span><span class="sxs-lookup"><span data-stu-id="c7408-465">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="c7408-466">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c7408-466">AzureRM.KeyVault</span></span>
* <span data-ttu-id="c7408-467">Åtgärda problem där alla resurser returnerades av Get-AzureRmKeyVault-taggen</span><span class="sxs-lookup"><span data-stu-id="c7408-467">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="c7408-468">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c7408-468">AzureRM.Network</span></span>
* <span data-ttu-id="c7408-469">Gör nya SKU:er tillgängliga för zonredundanta VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="c7408-469">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="c7408-470">Nya kommandon har lagts till för funktionen: ExpressRoute Partner APIs via ARM</span><span class="sxs-lookup"><span data-stu-id="c7408-470">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="c7408-471">Get-AzureRmExpressRouteCrossConnection har lagts till</span><span class="sxs-lookup"><span data-stu-id="c7408-471">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="c7408-472">Set-AzureRmExpressRouteCrossConnection har lagts till</span><span class="sxs-lookup"><span data-stu-id="c7408-472">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="c7408-473">Add-AzureRmExpressRouteCrossConnectionPeering har lagts till</span><span class="sxs-lookup"><span data-stu-id="c7408-473">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="c7408-474">Get-AzureRmExpressRouteCrossConnectionPeering har lagts till</span><span class="sxs-lookup"><span data-stu-id="c7408-474">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="c7408-475">Remove-AzureRmExpressRouteCrossConnectionPeering har lagts till</span><span class="sxs-lookup"><span data-stu-id="c7408-475">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="c7408-476">Get-AzureRMExpressRouteCrossConnectionArpTable har lagts till</span><span class="sxs-lookup"><span data-stu-id="c7408-476">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="c7408-477">Get-AzureRMExpressRouteCrossConnectionRouteTable har lagts till</span><span class="sxs-lookup"><span data-stu-id="c7408-477">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="c7408-478">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary har lagts till</span><span class="sxs-lookup"><span data-stu-id="c7408-478">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="c7408-479">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c7408-479">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="c7408-480">Get-AzureRmRecoveryServicesBackupStatus-cmdlet har lagts till.</span><span class="sxs-lookup"><span data-stu-id="c7408-480">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="c7408-481">Denna cmdlet tar ett ID för virtuell dator och kontrollerar om den virtuella datorn skyddas av ett valv i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="c7408-481">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="c7408-482">Om ett sådant valv finns returnerar cmdleten valvinformationen.</span><span class="sxs-lookup"><span data-stu-id="c7408-482">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="c7408-483">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="c7408-483">AzureRM.Resources</span></span>
* <span data-ttu-id="c7408-484">Uppdatera Get-AzureRmPolicyAssignment-cmdletar:</span><span class="sxs-lookup"><span data-stu-id="c7408-484">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="c7408-485">Lägg till stöd för att lista -Scope-värden på hanteringsgruppsnivå</span><span class="sxs-lookup"><span data-stu-id="c7408-485">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="c7408-486">Lägg till stöd för hämtning av enskilda tilldelningar med -Scope-värden på hanteringsgruppsnivå.</span><span class="sxs-lookup"><span data-stu-id="c7408-486">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="c7408-487">Lägg till växlar för -Effective och -All till kontrollparametrar</span><span class="sxs-lookup"><span data-stu-id="c7408-487">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="c7408-488">Uppdatera Get/New/Remove/Set-AzureRmPolicyDefinition-cmdletar</span><span class="sxs-lookup"><span data-stu-id="c7408-488">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="c7408-489">Lägg till parameter för -ManagementGroupName om du vill tillämpa åtgärder för en viss hanteringsgrupp</span><span class="sxs-lookup"><span data-stu-id="c7408-489">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="c7408-490">Lägg till parameter för -SubscriptionId om du vill tillämpa åtgärder för en viss prenumeration</span><span class="sxs-lookup"><span data-stu-id="c7408-490">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="c7408-491">Uppdatera Get/New/Remove/Set-AzureRmPolicySetDefinition-cmdletar</span><span class="sxs-lookup"><span data-stu-id="c7408-491">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="c7408-492">Lägg till parameter för -ManagementGroupName om du vill tillämpa åtgärder för en viss hanteringsgrupp</span><span class="sxs-lookup"><span data-stu-id="c7408-492">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="c7408-493">Lägg till parameter för -SubscriptionId om du vill tillämpa åtgärder för en viss prenumeration</span><span class="sxs-lookup"><span data-stu-id="c7408-493">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="c7408-494">Lägg till stöd för hemliga KeyVault-referenser i parametrar när du använder "TemplateParameterObject" i "New-AzureRmResourceGroupDeployment"</span><span class="sxs-lookup"><span data-stu-id="c7408-494">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="c7408-495">Åtgärda problem med att "-EndDate"-parametern ignorerades på grund av "New-AzureRmADAppCredential"</span><span class="sxs-lookup"><span data-stu-id="c7408-495">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="c7408-496">Åtgärda problem med att felaktig URL användes i "New-AzureRmADAppCredential" vid begäran</span><span class="sxs-lookup"><span data-stu-id="c7408-496">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="c7408-497">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c7408-497">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="c7408-498">Valfri parameter för -KeyValue har lagts till för New-AzureRmServiceBusKey-cmdleten, vilket gör det möjligt att ange KeyValue.</span><span class="sxs-lookup"><span data-stu-id="c7408-498">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="c7408-499">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="c7408-499">AzureRM.Sql</span></span>
* <span data-ttu-id="c7408-500">Användardefinierade återställningspunkter har klargjorts för SQLDW i New-AzureRmSqlDatabaseRestorePoint-hjälpen</span><span class="sxs-lookup"><span data-stu-id="c7408-500">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="c7408-501">Dokumentationen om parametern -ComputeGeneration har uppdaterats i fler cmdletar</span><span class="sxs-lookup"><span data-stu-id="c7408-501">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="c7408-502">6.3.0 – juni 2018</span><span class="sxs-lookup"><span data-stu-id="c7408-502">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="c7408-503">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c7408-503">AzureRM.Profile</span></span>
* <span data-ttu-id="c7408-504">Uppdaterade felmeddelanden för Enable-AzureRmContextAutoSave</span><span class="sxs-lookup"><span data-stu-id="c7408-504">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="c7408-505">Skapa en kontext för varje prenumeration när du kör ”Connect-AzureRmAccount” utan tidigare kontext</span><span class="sxs-lookup"><span data-stu-id="c7408-505">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="c7408-506">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="c7408-506">Azure.Storage</span></span>
* <span data-ttu-id="c7408-507">Ytterligare information om parametern -Permissions har lagts till i hjälpfilerna.</span><span class="sxs-lookup"><span data-stu-id="c7408-507">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="c7408-508">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c7408-508">AzureRM.Compute</span></span>
* <span data-ttu-id="c7408-509">”Get-AzureRmVmDiskEncryptionStatus” korrigerar ett problem för virtuella datorer utan datadiskar</span><span class="sxs-lookup"><span data-stu-id="c7408-509">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="c7408-510">Uppdatera version av klientbibliotek för Compute för att korrigera följande cmdletar</span><span class="sxs-lookup"><span data-stu-id="c7408-510">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="c7408-511">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="c7408-511">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="c7408-512">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="c7408-512">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="c7408-513">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="c7408-513">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="c7408-514">Följande cmdletar har åtgärdats för att visa ”Åtgärds-ID” och ”Åtgärdsstatus” på ett korrekt sätt:</span><span class="sxs-lookup"><span data-stu-id="c7408-514">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="c7408-515">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="c7408-515">Start-AzureRmVM</span></span>
    - <span data-ttu-id="c7408-516">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="c7408-516">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="c7408-517">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="c7408-517">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="c7408-518">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="c7408-518">Set-AzureRmVM</span></span>
    - <span data-ttu-id="c7408-519">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="c7408-519">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="c7408-520">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c7408-520">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="c7408-521">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="c7408-521">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="c7408-522">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="c7408-522">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="c7408-523">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c7408-523">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="c7408-524">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c7408-524">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="c7408-525">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c7408-525">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="c7408-526">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c7408-526">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="c7408-527">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="c7408-527">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="c7408-528">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="c7408-528">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="c7408-529">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="c7408-529">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="c7408-530">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="c7408-530">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="c7408-531">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="c7408-531">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="c7408-532">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="c7408-532">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="c7408-533">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="c7408-533">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="c7408-534">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="c7408-534">AzureRM.EventGrid</span></span>
* <span data-ttu-id="c7408-535">Ta bort verifieringsvillkoren ValidateNotNullOrEmpty för SubjectBeginsWith/SubjectEndsWith i cmdleten Update-AzureRmEventGridSubscription för att ändra de här parametrarna till en tom sträng om det behövs.</span><span class="sxs-lookup"><span data-stu-id="c7408-535">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="c7408-536">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c7408-536">AzureRM.KeyVault</span></span>
* <span data-ttu-id="c7408-537">Åtgärda problem där inga taggar returneras när Get-AzureRmKeyVault -Tag körs</span><span class="sxs-lookup"><span data-stu-id="c7408-537">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="c7408-538">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="c7408-538">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="c7408-539">Offentlig lansering av cmdletar för Policy Insights</span><span class="sxs-lookup"><span data-stu-id="c7408-539">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="c7408-540">Använd API-version 2018-04-04</span><span class="sxs-lookup"><span data-stu-id="c7408-540">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="c7408-541">Lägg till PolicyDefinitionReferenceId i resultaten för Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="c7408-541">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="c7408-542">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c7408-542">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="c7408-543">Parametern -Vault har lagts till i cmdletarna för RecoveryServices.Backup.</span><span class="sxs-lookup"><span data-stu-id="c7408-543">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="c7408-544">När den godkänns åsidosätts cmdleten Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="c7408-544">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="c7408-545">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="c7408-545">AzureRM.Sql</span></span>
* <span data-ttu-id="c7408-546">Exemplet i hjälpfilen för Get-AzureRmSqlDatabaseExpanded har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="c7408-546">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="c7408-547">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="c7408-547">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="c7408-548">Hjälpfilen för Add-AzureRmTrafficManagerEndpointConfig har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="c7408-548">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="c7408-549">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="c7408-549">AzureRM.Websites</span></span>
* <span data-ttu-id="c7408-550">”Set-AzureRmWebApp” har uppdaterats så att den inte skriver över appinställningarna när du använder -AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="c7408-550">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="c7408-551">”New-AzureRMWebAppSlot” har uppdaterats för att visa att AppServicePlan är en valfri parameter</span><span class="sxs-lookup"><span data-stu-id="c7408-551">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="c7408-552">6.2.1 – juni 2018</span><span class="sxs-lookup"><span data-stu-id="c7408-552">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="c7408-553">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="c7408-553">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="c7408-554">PSWorkspace-modellen har uppdaterats för att tillåta att nätverket använder typ som en parameter</span><span class="sxs-lookup"><span data-stu-id="c7408-554">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="c7408-555">6.2.0 – juni 2018</span><span class="sxs-lookup"><span data-stu-id="c7408-555">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="c7408-556">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c7408-556">AzureRM.Profile</span></span>
* <span data-ttu-id="c7408-557">Åtgärda problemet med att version 10.0.3 av Newtonsoft.Json inte lästes in vid modulimporten</span><span class="sxs-lookup"><span data-stu-id="c7408-557">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="c7408-558">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c7408-558">AzureRM.Compute</span></span>
* <span data-ttu-id="c7408-559">VMSS VM-uppdateringsfunktion</span><span class="sxs-lookup"><span data-stu-id="c7408-559">VMSS VM Update feature</span></span>
    - <span data-ttu-id="c7408-560">Cmdletarna Update-AzureRmVmssVM och New-AzureRmVMDataDisk har lagts till</span><span class="sxs-lookup"><span data-stu-id="c7408-560">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="c7408-561">Lägg till parametern VirtualMachineScaleSetVM till cmdleten Add-AzureRmVMDataDisk så att det går att lägga till en datadisk i den virtuella Vmss-datorn.</span><span class="sxs-lookup"><span data-stu-id="c7408-561">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="c7408-562">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="c7408-562">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="c7408-563">SDK:n för ADF .Net har uppdaterats till version 0.8.0-preview som innehåller följande ändringar:</span><span class="sxs-lookup"><span data-stu-id="c7408-563">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="c7408-564">Åtgärden för att konfigurera fabrikslagringsplatsen har lagts till</span><span class="sxs-lookup"><span data-stu-id="c7408-564">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="c7408-565">QuickBooks LinkedService har uppdaterats för att visa egenskaperna consumerKey och consumerSecret</span><span class="sxs-lookup"><span data-stu-id="c7408-565">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="c7408-566">Flera modelltyper från SecretBase till Object har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="c7408-566">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="c7408-567">Utlösaren Blob Events har lagts till</span><span class="sxs-lookup"><span data-stu-id="c7408-567">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="c7408-568">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c7408-568">AzureRM.KeyVault</span></span>
* <span data-ttu-id="c7408-569">Uppdatera dokumentation med exempel på utdata</span><span class="sxs-lookup"><span data-stu-id="c7408-569">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="c7408-570">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c7408-570">AzureRM.Network</span></span>
* <span data-ttu-id="c7408-571">Aktivera Trafikanalys-parametrar på Network Watcher-cmdletar</span><span class="sxs-lookup"><span data-stu-id="c7408-571">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="c7408-572">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="c7408-572">AzureRM.Resources</span></span>
* <span data-ttu-id="c7408-573">Åtgärda problemet med egenskapen "Properties" för objekt(en) "PSResource" som returneras från "Get-AzureRmResource"</span><span class="sxs-lookup"><span data-stu-id="c7408-573">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="c7408-574">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="c7408-574">AzureRM.Scheduler</span></span>
* <span data-ttu-id="c7408-575">Åtgärda problemet med att nya autentiseringsvärden inte anges vid uppdatering av ServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="c7408-575">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="c7408-576">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="c7408-576">AzureRM.Sql</span></span>
* <span data-ttu-id="c7408-577">Följande cmdletar har uppdaterats med valfri LicenseType-parameter</span><span class="sxs-lookup"><span data-stu-id="c7408-577">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="c7408-578">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c7408-578">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="c7408-579">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="c7408-579">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="c7408-580">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="c7408-580">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="c7408-581">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="c7408-581">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="c7408-582">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c7408-582">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="c7408-583">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="c7408-583">AzureRM.Websites</span></span>
* <span data-ttu-id="c7408-584">New-AzureRMWebApp har uppdaterats för att använda vanliga algoritmer från biblioteket Strategy.</span><span class="sxs-lookup"><span data-stu-id="c7408-584">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="c7408-585">6.1.0 – maj 2018</span><span class="sxs-lookup"><span data-stu-id="c7408-585">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="c7408-586">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c7408-586">AzureRM.Profile</span></span>
* <span data-ttu-id="c7408-587">Åtgärda problem där en körning av Clear-AzureRmContext skulle bevara en tom kontext med namnet på den föregående standardkontexten som gjorde att användaren inte kunde skapa en ny kontext med det gamla namnet</span><span class="sxs-lookup"><span data-stu-id="c7408-587">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="c7408-588">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="c7408-588">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="c7408-589">Aktivera Gateway associerings- och avassocieringsåtgärder på AS.</span><span class="sxs-lookup"><span data-stu-id="c7408-589">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="c7408-590">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c7408-590">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="c7408-591">Stöd för ApiVersions, ApiReleases och ApiRevisions har lagts till</span><span class="sxs-lookup"><span data-stu-id="c7408-591">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="c7408-592">Stöd för serverdelen på ServiceFabric har lagts till</span><span class="sxs-lookup"><span data-stu-id="c7408-592">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="c7408-593">Stöd för Application Insights-loggare har lagts till</span><span class="sxs-lookup"><span data-stu-id="c7408-593">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="c7408-594">Stöd för att identifiera SKU:n ”Basic” som en giltig SKU för Api Management-tjänsten har lagts till</span><span class="sxs-lookup"><span data-stu-id="c7408-594">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="c7408-595">Stöd för att installera certifikat som utfärdats av privata certifikatutfärdare som rot eller certifikatutfärdare har lagts till</span><span class="sxs-lookup"><span data-stu-id="c7408-595">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="c7408-596">Stöd för att godkänna anpassade SSL-certifikat via KeyVault och flera proxy-värdnamn har lagts till</span><span class="sxs-lookup"><span data-stu-id="c7408-596">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="c7408-597">Stöd för MSI-identitet har lagts till</span><span class="sxs-lookup"><span data-stu-id="c7408-597">Added support for MSI identity</span></span>
* <span data-ttu-id="c7408-598">Stöd för att godkänna principer via URL har lagts till. Obs! Följande cmdletar blir inaktuella i framtida versioner</span><span class="sxs-lookup"><span data-stu-id="c7408-598">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="c7408-599">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="c7408-599">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="c7408-600">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="c7408-600">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="c7408-601">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="c7408-601">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="c7408-602">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="c7408-602">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="c7408-603">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="c7408-603">AzureRM.Batch</span></span>
* <span data-ttu-id="c7408-604">Släpp nya cmdleten Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="c7408-604">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="c7408-605">Släpp nya cmdleten Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="c7408-605">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="c7408-606">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="c7408-606">AzureRM.Consumption</span></span>
* <span data-ttu-id="c7408-607">Lägg till nya parametrar Expand, ResourceGroup, InstanceName, InstanceId, Tags och Top på cmdleten Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="c7408-607">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="c7408-608">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c7408-608">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="c7408-609">Åtgärda exempel för Export AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="c7408-609">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="c7408-610">Åtgärda undantag för null-parameter för rekursivt ärende i Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="c7408-610">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="c7408-611">Åtgärda hjälpfilerna för Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="c7408-611">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="c7408-612">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c7408-612">AzureRM.Network</span></span>
* <span data-ttu-id="c7408-613">Öka nätverkets SDK-version från förhandsversionen 18.0.0 till förhandsversionen 19.0.0</span><span class="sxs-lookup"><span data-stu-id="c7408-613">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="c7408-614">Cmdlet har lagts till för att skapa protokollinformation</span><span class="sxs-lookup"><span data-stu-id="c7408-614">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="c7408-615">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="c7408-615">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="c7408-616">Cmdlet har lagts till för att lägga till en ny kretsanslutning till en befintlig expressroute-krets.</span><span class="sxs-lookup"><span data-stu-id="c7408-616">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="c7408-617">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="c7408-617">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="c7408-618">Cmdlet har lagts till för att ta bort en kretsanslutning från en befintlig expressroute-krets.</span><span class="sxs-lookup"><span data-stu-id="c7408-618">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="c7408-619">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="c7408-619">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="c7408-620">Cmdlet har lagts till för att hämta en kretsanslutning</span><span class="sxs-lookup"><span data-stu-id="c7408-620">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="c7408-621">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="c7408-621">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="c7408-622">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c7408-622">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="c7408-623">Användning med serverautentisering med genererade certifikat (problem #5998) har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="c7408-623">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="c7408-624">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="c7408-624">AzureRM.Sql</span></span>
* <span data-ttu-id="c7408-625">Cmdletar för granskning för att ta bort AuditActions eller AuditActionGroups har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="c7408-625">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="c7408-626">Åtgärdade problem med Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy vid konfigurering av en ny flexibel bevarandeprincip där kommandot misslyckas med ett meddelande om att konfigurering av långsiktig bevarandeprincip med Azure Recovery Service-valv och principen inte längre stöds,</span><span class="sxs-lookup"><span data-stu-id="c7408-626">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="c7408-627">och att en begäran med den nya flexibla bevarandeprincipen ska skickas.</span><span class="sxs-lookup"><span data-stu-id="c7408-627">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="c7408-628">Uppdatera alla Azure Sql Database/ElasticPool Creation/Update-relaterade cmdletar för att använda det nya databas-API:et som stöder SKU-egenskaper för skalnings- och nivårelaterade egenskaper.</span><span class="sxs-lookup"><span data-stu-id="c7408-628">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="c7408-629">Cmdletar har uppdaterats, inklusive:</span><span class="sxs-lookup"><span data-stu-id="c7408-629">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="c7408-630">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c7408-630">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="c7408-631">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="c7408-631">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="c7408-632">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="c7408-632">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="c7408-633">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="c7408-633">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="c7408-634">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c7408-634">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="c7408-635">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="c7408-635">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="c7408-636">Uppdatera parametrarna för Get-AzureRmTrafficManagerProfile så att ResourceGroupName-parametern blir obligatorisk när du använder Name-parametern.</span><span class="sxs-lookup"><span data-stu-id="c7408-636">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
