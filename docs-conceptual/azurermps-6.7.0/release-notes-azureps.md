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
ms.openlocfilehash: 2a6e20137f12ae9317c7eeed330a2433774e1ea9
ms.sourcegitcommit: f648ac92fafb16cc0e9ca6bc85d00fa327baf396
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/28/2018
ms.locfileid: "43018706"
---
# <a name="release-notes"></a><span data-ttu-id="b56aa-103">Viktig information</span><span class="sxs-lookup"><span data-stu-id="b56aa-103">Release notes</span></span>

<span data-ttu-id="b56aa-104">Det här är en lista över ändringar som har gjorts i Azure PowerShell i den här versionen.</span><span class="sxs-lookup"><span data-stu-id="b56aa-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="670---august-2018"></a><span data-ttu-id="b56aa-105">6.7.0 – augusti 2018</span><span class="sxs-lookup"><span data-stu-id="b56aa-105">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="b56aa-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="b56aa-106">AzureRM.Profile</span></span>
* <span data-ttu-id="b56aa-107">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b56aa-107">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="b56aa-108">Lägg till användar-id i standardkontextnamnet för att undvika kontextkonflikter</span><span class="sxs-lookup"><span data-stu-id="b56aa-108">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="b56aa-109">Åtgärda problem med Clear-AzureRmContext som orsakade problem med att välja en kontext #6398</span><span class="sxs-lookup"><span data-stu-id="b56aa-109">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="b56aa-110">Aktivera den klientorganisationsdomän som ska skickas till parametern -TenantId för Connect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="b56aa-110">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="b56aa-111">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="b56aa-111">Azure.Storage</span></span>
* <span data-ttu-id="b56aa-112">Ta bort begränsningen på 5 TB för Azure-filresurskvoten</span><span class="sxs-lookup"><span data-stu-id="b56aa-112">Remove the 5TB limitation for Azure File Share quota</span></span>
- <span data-ttu-id="b56aa-113">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="b56aa-113">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="b56aa-114">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="b56aa-114">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="b56aa-115">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b56aa-115">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="b56aa-116">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="b56aa-116">Azure.AnalysisServices</span></span>
* <span data-ttu-id="b56aa-117">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b56aa-117">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="b56aa-118">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b56aa-118">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="b56aa-119">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b56aa-119">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="b56aa-120">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="b56aa-120">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="b56aa-121">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b56aa-121">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="b56aa-122">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="b56aa-122">AzureRM.Automation</span></span>
* <span data-ttu-id="b56aa-123">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b56aa-123">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="b56aa-124">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="b56aa-124">AzureRM.Backup</span></span>
* <span data-ttu-id="b56aa-125">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b56aa-125">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="b56aa-126">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="b56aa-126">AzureRM.Batch</span></span>
* <span data-ttu-id="b56aa-127">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b56aa-127">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="b56aa-128">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="b56aa-128">AzureRM.Billing</span></span>
* <span data-ttu-id="b56aa-129">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b56aa-129">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="b56aa-130">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="b56aa-130">AzureRM.Cdn</span></span>
* <span data-ttu-id="b56aa-131">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b56aa-131">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="b56aa-132">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b56aa-132">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="b56aa-133">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b56aa-133">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="b56aa-134">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="b56aa-134">AzureRM.Compute</span></span>
* <span data-ttu-id="b56aa-135">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b56aa-135">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="b56aa-136">Lägg till parametern EvictionPolicy i New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="b56aa-136">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="b56aa-137">Använd standardplatsen i DiskFileParameterSet för New-AzureRmVm om ingen plats har angetts.</span><span class="sxs-lookup"><span data-stu-id="b56aa-137">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="b56aa-138">Korrigera parameterbeskrivningen i Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="b56aa-138">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="b56aa-139">Korrigera cmdleten Get-AzureRmVMDiskEncryptionStatus för vissa singlepass-relaterade scenarier</span><span class="sxs-lookup"><span data-stu-id="b56aa-139">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="b56aa-140">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="b56aa-140">AzureRM.Consumption</span></span>
* <span data-ttu-id="b56aa-141">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b56aa-141">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="b56aa-142">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="b56aa-142">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="b56aa-143">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b56aa-143">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="b56aa-144">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="b56aa-144">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="b56aa-145">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b56aa-145">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="b56aa-146">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="b56aa-146">AzureRM.DataFactories</span></span>
* <span data-ttu-id="b56aa-147">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b56aa-147">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="b56aa-148">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="b56aa-148">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="b56aa-149">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b56aa-149">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="b56aa-150">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="b56aa-150">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="b56aa-151">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b56aa-151">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="b56aa-152">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b56aa-152">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="b56aa-153">Korrigera felsökning när DebugPreference anges från powershell-kommandoraden</span><span class="sxs-lookup"><span data-stu-id="b56aa-153">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="b56aa-154">Uppdatera exemplet för Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="b56aa-154">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="b56aa-155">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b56aa-155">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="b56aa-156">Uppdatera exemplet för Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="b56aa-156">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="b56aa-157">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="b56aa-157">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="b56aa-158">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b56aa-158">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="b56aa-159">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="b56aa-159">AzureRM.Dns</span></span>
* <span data-ttu-id="b56aa-160">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b56aa-160">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="b56aa-161">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="b56aa-161">AzureRM.EventGrid</span></span>
* <span data-ttu-id="b56aa-162">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b56aa-162">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="b56aa-163">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="b56aa-163">AzureRM.EventHub</span></span>
* <span data-ttu-id="b56aa-164">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b56aa-164">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="b56aa-165">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="b56aa-165">AzureRM.HDInsight</span></span>
* <span data-ttu-id="b56aa-166">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b56aa-166">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="b56aa-167">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="b56aa-167">AzureRM.Insights</span></span>
* <span data-ttu-id="b56aa-168">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b56aa-168">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="b56aa-169">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="b56aa-169">AzureRM.IotHub</span></span>
* <span data-ttu-id="b56aa-170">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b56aa-170">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="b56aa-171">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b56aa-171">AzureRM.KeyVault</span></span>
* <span data-ttu-id="b56aa-172">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b56aa-172">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="b56aa-173">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="b56aa-173">AzureRM.LogicApp</span></span>
* <span data-ttu-id="b56aa-174">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b56aa-174">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="b56aa-175">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="b56aa-175">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="b56aa-176">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b56aa-176">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="b56aa-177">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="b56aa-177">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="b56aa-178">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b56aa-178">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="b56aa-179">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="b56aa-179">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="b56aa-180">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b56aa-180">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="b56aa-181">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="b56aa-181">AzureRM.Media</span></span>
* <span data-ttu-id="b56aa-182">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b56aa-182">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="b56aa-183">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="b56aa-183">AzureRM.Network</span></span>
* <span data-ttu-id="b56aa-184">Exempel för Set-AzureRmLocalNetworkGateway har lagts till</span><span class="sxs-lookup"><span data-stu-id="b56aa-184">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="b56aa-185">Exempel och beskrivningar för Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey och New-AzureRmVirtualNetworkGatewayConnection har lagts till</span><span class="sxs-lookup"><span data-stu-id="b56aa-185">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="b56aa-186">Exempel för Remove-AzureRmVirtualNetworkGatewayIpConfig och Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b56aa-186">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="b56aa-187">Exempel för Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey har lagts till</span><span class="sxs-lookup"><span data-stu-id="b56aa-187">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="b56aa-188">Exempel för Set-AzureRmVirtualNetworkGatewayConnectionSharedKey har lagts till</span><span class="sxs-lookup"><span data-stu-id="b56aa-188">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="b56aa-189">Exempel för Set-AzureRmVirtualNetworkGatewayConnection har lagts till</span><span class="sxs-lookup"><span data-stu-id="b56aa-189">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="b56aa-190">Cmdletar för ApplicationSecurityGroup, RouteTable and Usage har genererats om med den senaste kodgeneratorn</span><span class="sxs-lookup"><span data-stu-id="b56aa-190">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="b56aa-191">Förtydligade ett felmeddelande för Get-AzureRmVirtualNetworkSubnetConfig vid försök att hämta ett undernät som inte avslutas</span><span class="sxs-lookup"><span data-stu-id="b56aa-191">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="b56aa-192">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="b56aa-192">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="b56aa-193">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b56aa-193">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="b56aa-194">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b56aa-194">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="b56aa-195">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b56aa-195">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="b56aa-196">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="b56aa-196">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="b56aa-197">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b56aa-197">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="b56aa-198">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="b56aa-198">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="b56aa-199">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b56aa-199">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="b56aa-200">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b56aa-200">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="b56aa-201">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b56aa-201">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="b56aa-202">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b56aa-202">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="b56aa-203">Lade till principfilter i cmdleten Get-AzureRmRecoveryServicesBackItem.</span><span class="sxs-lookup"><span data-stu-id="b56aa-203">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="b56aa-204">Kommandot returnerar listan med säkerhetskopieringsobjekt som skyddas av det angivna princip-ID:t.</span><span class="sxs-lookup"><span data-stu-id="b56aa-204">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="b56aa-205">Microsoft.Azure.Management.RecoveryServices.Backup uppdaterades till förhandsversionen av 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="b56aa-205">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="b56aa-206">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b56aa-206">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="b56aa-207">Parametern TargetResourceGroupName lades till i Restore-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="b56aa-207">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="b56aa-208">Den resursgrupp som de hanterade diskarna återställs till.</span><span class="sxs-lookup"><span data-stu-id="b56aa-208">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="b56aa-209">Gäller för säkerhetskopiering av virtuell dator med hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="b56aa-209">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="b56aa-210">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b56aa-210">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="b56aa-211">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b56aa-211">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="b56aa-212">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="b56aa-212">AzureRM.RedisCache</span></span>
* <span data-ttu-id="b56aa-213">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b56aa-213">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="b56aa-214">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="b56aa-214">AzureRM.Relay</span></span>
* <span data-ttu-id="b56aa-215">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b56aa-215">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="b56aa-216">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="b56aa-216">AzureRM.Resources</span></span>
* <span data-ttu-id="b56aa-217">Distribution av supportmall i prenumerationsomfånget.</span><span class="sxs-lookup"><span data-stu-id="b56aa-217">Support template deployment at subscription scope.</span></span> <span data-ttu-id="b56aa-218">Lägg till nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="b56aa-218">Add new Cmdlets:</span></span>
    - <span data-ttu-id="b56aa-219">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="b56aa-219">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="b56aa-220">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="b56aa-220">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="b56aa-221">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="b56aa-221">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="b56aa-222">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="b56aa-222">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="b56aa-223">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="b56aa-223">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="b56aa-224">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="b56aa-224">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="b56aa-225">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="b56aa-225">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="b56aa-226">Korrigera ett problem där fel inträffar när en kontext skickas till Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="b56aa-226">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="b56aa-227">Korrigera exempel i New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b56aa-227">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="b56aa-228">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b56aa-228">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="b56aa-229">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="b56aa-229">AzureRM.Scheduler</span></span>
* <span data-ttu-id="b56aa-230">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b56aa-230">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="b56aa-231">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b56aa-231">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="b56aa-232">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b56aa-232">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="b56aa-233">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b56aa-233">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="b56aa-234">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b56aa-234">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="b56aa-235">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="b56aa-235">AzureRM.Sql</span></span>
* <span data-ttu-id="b56aa-236">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b56aa-236">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="b56aa-237">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="b56aa-237">AzureRM.Storage</span></span>
* <span data-ttu-id="b56aa-238">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b56aa-238">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="b56aa-239">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="b56aa-239">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="b56aa-240">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b56aa-240">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="b56aa-241">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="b56aa-241">AzureRM.Tags</span></span>
* <span data-ttu-id="b56aa-242">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b56aa-242">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="b56aa-243">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="b56aa-243">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="b56aa-244">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b56aa-244">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="b56aa-245">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="b56aa-245">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="b56aa-246">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b56aa-246">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="b56aa-247">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="b56aa-247">AzureRM.Websites</span></span>
* <span data-ttu-id="b56aa-248">Har uppdaterats till den senaste versionen av Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b56aa-248">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="b56aa-249">6.6.0 – juli 2018</span><span class="sxs-lookup"><span data-stu-id="b56aa-249">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="b56aa-250">Allmänt</span><span class="sxs-lookup"><span data-stu-id="b56aa-250">General</span></span>
* <span data-ttu-id="b56aa-251">Alla hjälpfiler har uppdaterats för att ta med fullständiga parametertyper och korrekta indata-/utdatatyper.</span><span class="sxs-lookup"><span data-stu-id="b56aa-251">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="b56aa-252">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="b56aa-252">AzureRM.Profile</span></span>
* <span data-ttu-id="b56aa-253">Common.Strategy-biblioteket har uppdaterats för att kunna verifiera att den aktuella konfigurationsfilen för en resurs är kompatibel med målresursen.</span><span class="sxs-lookup"><span data-stu-id="b56aa-253">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="b56aa-254">ps1xml-typer har lagts till i Common.Storage</span><span class="sxs-lookup"><span data-stu-id="b56aa-254">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="b56aa-255">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="b56aa-255">Azure.Storage</span></span>
* <span data-ttu-id="b56aa-256">Lade till stöd för hämtning av lagringskontext från DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b56aa-256">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="b56aa-257">Lade till Ps1XmlAttribute till utdatatypegenskaper för cmdletar.</span><span class="sxs-lookup"><span data-stu-id="b56aa-257">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="b56aa-258">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b56aa-258">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="b56aa-259">Åtgärdat problem https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="b56aa-259">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="b56aa-260">En bugg har åtgärdats i Automapper för att översätta PsApiManagementApi till ApiContract</span><span class="sxs-lookup"><span data-stu-id="b56aa-260">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="b56aa-261">Åtgärdat problem https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="b56aa-261">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="b56aa-262">En bugg har åtgärdats i File.Save för att inte överbelasta kodningstypen</span><span class="sxs-lookup"><span data-stu-id="b56aa-262">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="b56aa-263">Åtgärdat problem https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="b56aa-263">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="b56aa-264">Har uppgraderats till Nuget-versionen 4.0.3 vilket åtgärdar mönsterundantaget på apiId</span><span class="sxs-lookup"><span data-stu-id="b56aa-264">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="b56aa-265">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="b56aa-265">AzureRM.Compute</span></span>
* <span data-ttu-id="b56aa-266">Åtgärda problem med fel vid skapandet av en virtuell dator med hjälp av DiskFileParameterSet i New-AzureRmVm på grund av namnbyte på PremiumLRS-lagringskontotypen.</span><span class="sxs-lookup"><span data-stu-id="b56aa-266">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="b56aa-267">Åtgärda cmdleten Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="b56aa-267">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="b56aa-268">Uppdatera Get-AzureRmAvailabilitySet för att aktivera funktionen för att lista alla tillgänglighetsuppsättningar i en prenumeration.</span><span class="sxs-lookup"><span data-stu-id="b56aa-268">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="b56aa-269">(Parametern ResouceGroupName är nu frivillig.)</span><span class="sxs-lookup"><span data-stu-id="b56aa-269">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="b56aa-270">Uppdatera SimpleParameterSet för "New-AzureRmVm" för att aktivera accelererat nätverk på berättigade virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="b56aa-270">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="b56aa-271">Uppdatera den enkla parameteruppsättningen för New-AzureRmVmss så att det inte går att skapa de virtuella datorerna när en användarangiven lastbalanserare redan finns.</span><span class="sxs-lookup"><span data-stu-id="b56aa-271">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="b56aa-272">Uppdatera exempel för New-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="b56aa-272">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="b56aa-273">Lägg till exempel för "New-AzureRmVM"</span><span class="sxs-lookup"><span data-stu-id="b56aa-273">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="b56aa-274">Uppdatera beskrivning för Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="b56aa-274">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="b56aa-275">Uppdatera Exempel 1 för Set-AzureRmVMBginfoExtension för stavningskontroll och prefix.</span><span class="sxs-lookup"><span data-stu-id="b56aa-275">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="b56aa-276">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="b56aa-276">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="b56aa-277">ADF .Net SDK-versionen har uppdaterats till 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="b56aa-277">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="b56aa-278">Stöd för delning av Integration Runtime (lokal installation) mellan datafabriker.</span><span class="sxs-lookup"><span data-stu-id="b56aa-278">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="b56aa-279">Lägg till ny parameter – SharedIntegrationRuntimeResourceId i cmdleten Set-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="b56aa-279">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="b56aa-280">Lägg till ny valfri parameter – LinkedDataFactoryName i cmdleten Remove-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="b56aa-280">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="b56aa-281">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b56aa-281">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="b56aa-282">DataPlane SDK-versionen (Microsoft.Azure.DataLake.Store) har uppdaterats till 1.1.9</span><span class="sxs-lookup"><span data-stu-id="b56aa-282">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="b56aa-283">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="b56aa-283">AzureRM.EventHub</span></span>
* <span data-ttu-id="b56aa-284">Piping för InputObject and ResourceId i borttagna cmdletar har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="b56aa-284">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="b56aa-285">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="b56aa-285">AzureRM.Insights</span></span>
* <span data-ttu-id="b56aa-286">Formatering har åtgärdats för OutputType i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="b56aa-286">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="b56aa-287">Använda Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span><span class="sxs-lookup"><span data-stu-id="b56aa-287">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="b56aa-288">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b56aa-288">AzureRM.KeyVault</span></span>
* <span data-ttu-id="b56aa-289">Åtgärda problem med piping i Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b56aa-289">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="b56aa-290">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="b56aa-290">AzureRM.Network</span></span>
* <span data-ttu-id="b56aa-291">Exempel har lagts till för LoadBalancerInboundNatPoolConfig-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="b56aa-291">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="b56aa-292">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="b56aa-292">AzureRM.Resources</span></span>
* <span data-ttu-id="b56aa-293">Åtgärda problem när både taggnamn och värde anges för "Get-AzureRmResource"</span><span class="sxs-lookup"><span data-stu-id="b56aa-293">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="b56aa-294">Åtgärda pipingscenario med "Set-AzureRmResource"</span><span class="sxs-lookup"><span data-stu-id="b56aa-294">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="b56aa-295">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b56aa-295">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="b56aa-296">Piping för InputObject and ResourceId i borttagna cmdletar har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="b56aa-296">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="b56aa-297">några problem har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="b56aa-297">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="b56aa-298">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="b56aa-298">AzureRM.Sql</span></span>
* <span data-ttu-id="b56aa-299">Lägg till stöd för Server Advanced Threat Protection med följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="b56aa-299">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="b56aa-300">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b56aa-300">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="b56aa-301">Lägg till stöd för Sårbarhetsbedömning med följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="b56aa-301">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="b56aa-302">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="b56aa-302">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="b56aa-303">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="b56aa-303">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="b56aa-304">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="b56aa-304">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="b56aa-305">Exempel i Remove-AzureRmSqlServerFirewallRule har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="b56aa-305">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="b56aa-306">Åtgärda felaktig hantering av datum och tid för andra kulturer än usa-baserade kulturer i Get-AzureSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="b56aa-306">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="b56aa-307">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="b56aa-307">AzureRM.Storage</span></span>
* <span data-ttu-id="b56aa-308">Lägg till Ps1XmlAttribute i utdatatypegenskaper för cmdletar</span><span class="sxs-lookup"><span data-stu-id="b56aa-308">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="b56aa-309">Visa utdata för cmdleten StorageAccount i tabellvyn</span><span class="sxs-lookup"><span data-stu-id="b56aa-309">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="b56aa-310">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b56aa-310">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="b56aa-311">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b56aa-311">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="b56aa-312">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b56aa-312">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="b56aa-313">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="b56aa-313">AzureRM.Tags</span></span>
* <span data-ttu-id="b56aa-314">Ta bort felaktig instruktion från hjälpen för cmdleten Tag</span><span class="sxs-lookup"><span data-stu-id="b56aa-314">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="b56aa-315">6.5.0 – juli 2018</span><span class="sxs-lookup"><span data-stu-id="b56aa-315">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="b56aa-316">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="b56aa-316">AzureRM.Profile</span></span>
* <span data-ttu-id="b56aa-317">Hjälp för ”Get-AzureRmContextAutosaveSetting” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="b56aa-317">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="b56aa-318">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="b56aa-318">Azure.Storage</span></span>
* <span data-ttu-id="b56aa-319">Stöd för uppladdning av blob eller fil med lässkyddad SAS-token</span><span class="sxs-lookup"><span data-stu-id="b56aa-319">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="b56aa-320">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="b56aa-320">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="b56aa-321">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="b56aa-321">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="b56aa-322">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="b56aa-322">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="b56aa-323">Lägg till den nödvändiga egenskapen ResourceGroupName i AS.</span><span class="sxs-lookup"><span data-stu-id="b56aa-323">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="b56aa-324">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="b56aa-324">AzureRM.Automation</span></span>
* <span data-ttu-id="b56aa-325">Uppdatera hjälp och lägg till exempel för ”New-AzureRMAutomationSchedule”</span><span class="sxs-lookup"><span data-stu-id="b56aa-325">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="b56aa-326">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="b56aa-326">AzureRM.Compute</span></span>
* <span data-ttu-id="b56aa-327">Lägg till parametern -Tag förUpdate/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="b56aa-327">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="b56aa-328">Lägg till exempel för ”Add-AzureRmVmssExtension”</span><span class="sxs-lookup"><span data-stu-id="b56aa-328">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="b56aa-329">Lägg till exempel för ”Remove-AzureRmVmssExtension”</span><span class="sxs-lookup"><span data-stu-id="b56aa-329">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="b56aa-330">Uppdatera hjälp för ”Set-AzureRmVMAccessExtension”</span><span class="sxs-lookup"><span data-stu-id="b56aa-330">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="b56aa-331">Uppdatera SimpleParameterSet för New-AzureRmVmss för att ställa in SinglePlacementGroup på falskt som standard och lägg till växlingsparametern ”SinglePlacementGroup” som gör att användare kan skapa VMSS i en enda placeringsgrupp.</span><span class="sxs-lookup"><span data-stu-id="b56aa-331">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="b56aa-332">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="b56aa-332">AzureRM.EventHub</span></span>
* <span data-ttu-id="b56aa-333">En skrivskyddad egenskap, ”PendingReplicationOperationsCount”, har lagts till för klassen PSEventHubDRConfigurationAttributes som anger antalet väntande replikeringsåtgärder medan replikeringen pågår</span><span class="sxs-lookup"><span data-stu-id="b56aa-333">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="b56aa-334">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b56aa-334">AzureRM.KeyVault</span></span>
* <span data-ttu-id="b56aa-335">Uppdatera felmeddelande för Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b56aa-335">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="b56aa-336">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="b56aa-336">AzureRM.LogicApp</span></span>
* <span data-ttu-id="b56aa-337">Felet ”parameteruppsättningen gick inte att matcha” har korrigerats i New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="b56aa-337">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="b56aa-338">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="b56aa-338">AzureRM.Network</span></span>
* <span data-ttu-id="b56aa-339">Aktivera peering mellan virtuella nätverk i flera klienter för Set/Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="b56aa-339">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="b56aa-340">Nedanstående cmdletar för Application Gateway har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="b56aa-340">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="b56aa-341">New-AzureRmApplicationGateway: EnableFIPS-flagga har lagts till för stöd för zoner</span><span class="sxs-lookup"><span data-stu-id="b56aa-341">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="b56aa-342">New-AzureRmApplicationGatewaySku: nya SKU:er, Standard_v2 och WAF_v2, har lagts till</span><span class="sxs-lookup"><span data-stu-id="b56aa-342">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="b56aa-343">Set-AzureRmApplicationGatewaySku: nya SKU:er, Standard_v2 och WAF_v2, har lagts till</span><span class="sxs-lookup"><span data-stu-id="b56aa-343">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="b56aa-344">RouteTable-cmdletar har återskapats med den senaste versionen av generatorn</span><span class="sxs-lookup"><span data-stu-id="b56aa-344">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="b56aa-345">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="b56aa-345">AzureRM.Relay</span></span>
* <span data-ttu-id="b56aa-346">Markdown-filer har uppdaterats och korrigerar problem med parameternamn i exemplet</span><span class="sxs-lookup"><span data-stu-id="b56aa-346">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="b56aa-347">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="b56aa-347">AzureRM.Resources</span></span>
* <span data-ttu-id="b56aa-348">Uppdatera cmdletar för rolltilldelning och rolldefinition:</span><span class="sxs-lookup"><span data-stu-id="b56aa-348">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="b56aa-349">Ta bort extra anrop för rolldefinitioner som görs som en del av sidindelning.</span><span class="sxs-lookup"><span data-stu-id="b56aa-349">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="b56aa-350">Åtgärda Get-AzureRMRoleAssignment-cmdlet</span><span class="sxs-lookup"><span data-stu-id="b56aa-350">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="b56aa-351">Åtgärda parameterfunktioner för kommandot -ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="b56aa-351">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="b56aa-352">Åtgärda problem med ”Get-AzureRmResource” där ”-ResourceType”-parametern var skiftlägeskänsligt</span><span class="sxs-lookup"><span data-stu-id="b56aa-352">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="b56aa-353">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b56aa-353">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="b56aa-354">Parametrar för att stoppa och hoppa över har lagts till i listan över cmdletar</span><span class="sxs-lookup"><span data-stu-id="b56aa-354">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="b56aa-355">Cmdletar för migrering från Standard- till Premium-namnområden har lagts till:</span><span class="sxs-lookup"><span data-stu-id="b56aa-355">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="b56aa-356">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="b56aa-356">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="b56aa-357">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="b56aa-357">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="b56aa-358">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="b56aa-358">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="b56aa-359">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="b56aa-359">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="b56aa-360">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="b56aa-360">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="b56aa-361">En skrivskyddad egenskap, ”PendingReplicationOperationsCount” har lagts till för klassen PSServiceBusDRConfigurationAttributes som anger antalet väntande replikeringsåtgärder medan replikeringen pågår</span><span class="sxs-lookup"><span data-stu-id="b56aa-361">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="b56aa-362">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b56aa-362">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="b56aa-363">Uppdatera exempel för ”New-AzureRmServiceFabricCluster”</span><span class="sxs-lookup"><span data-stu-id="b56aa-363">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="b56aa-364">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="b56aa-364">AzureRM.Sql</span></span>
* <span data-ttu-id="b56aa-365">Nya cmdletar för Management.Sql som gör att kunderna kan lägga till certifikat för transparent datakryptering till SQL Server-instans eller en hanterad instans har lagts till</span><span class="sxs-lookup"><span data-stu-id="b56aa-365">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="b56aa-366">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="b56aa-366">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="b56aa-367">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="b56aa-367">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="b56aa-368">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="b56aa-368">AzureRM.Websites</span></span>
* <span data-ttu-id="b56aa-369">När `Set-AzureRmWebApp -AssignIdentity` och `Set-AzureRmWebAppSlot -AssignIdentity` är inställda på falskt tar de nu bort identitetsegenskapen från platsobjektet. Även förhandsgranskningstaggen tas bort.</span><span class="sxs-lookup"><span data-stu-id="b56aa-369">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="b56aa-370">`Get-AzureRmWebAppMetrics`, `Get-AzureRmAppServicePlanMetrics`-exempel har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="b56aa-370">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="b56aa-371">`Set-AzureRmWebApp -PhpVersion` har stöd för ”av” som en giltig php-version</span><span class="sxs-lookup"><span data-stu-id="b56aa-371">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="b56aa-372">6.4.0 – juli 2018</span><span class="sxs-lookup"><span data-stu-id="b56aa-372">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="b56aa-373">Allmänt</span><span class="sxs-lookup"><span data-stu-id="b56aa-373">General</span></span>
* <span data-ttu-id="b56aa-374">Formatering av OutputType i hjälpfiler har korrigerats för de flesta moduler</span><span class="sxs-lookup"><span data-stu-id="b56aa-374">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="b56aa-375">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="b56aa-375">AzureRM.Profile</span></span>
* <span data-ttu-id="b56aa-376">Ps1Xml-attribut har lagts till för grundläggande utdatatyper</span><span class="sxs-lookup"><span data-stu-id="b56aa-376">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="b56aa-377">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="b56aa-377">AzureRM.Compute</span></span>
* <span data-ttu-id="b56aa-378">IP-tagg-funktioner för VMSS</span><span class="sxs-lookup"><span data-stu-id="b56aa-378">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="b56aa-379">"New-AzureRmVmssIpTagConfig"-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="b56aa-379">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="b56aa-380">IpTag-parameter har lagts till för New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="b56aa-380">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="b56aa-381">Automatisk återställningsfunktion för operativsystem för VMSS</span><span class="sxs-lookup"><span data-stu-id="b56aa-381">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="b56aa-382">DisableAutoRollback-parametrar har lagts till för New-AzureRmVmssConfig och Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b56aa-382">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="b56aa-383">Funktion för uppgraderingshistorik för operativsystem för Vmss</span><span class="sxs-lookup"><span data-stu-id="b56aa-383">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="b56aa-384">OSUpgradeHistory-växlingsparametern har lagts till för Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b56aa-384">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="b56aa-385">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="b56aa-385">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="b56aa-386">Lägg till stöd för katalog-ACL:er med hjälp av följande kommandon:</span><span class="sxs-lookup"><span data-stu-id="b56aa-386">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="b56aa-387">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="b56aa-387">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="b56aa-388">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="b56aa-388">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="b56aa-389">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="b56aa-389">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="b56aa-390">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b56aa-390">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="b56aa-391">Lägg till stöd för annullering och förloppsspårning för Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="b56aa-391">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="b56aa-392">Lägg till stöd för annullering för Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="b56aa-392">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="b56aa-393">Åtgärda tömning av felsökningsmeddelanden för cmdletar som gör rekursiva åtgärder</span><span class="sxs-lookup"><span data-stu-id="b56aa-393">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="b56aa-394">Åtgärda platsen för testning av DataLake-cmdletar</span><span class="sxs-lookup"><span data-stu-id="b56aa-394">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="b56aa-395">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="b56aa-395">AzureRM.EventHub</span></span>
* <span data-ttu-id="b56aa-396">Parametrar för optimalt maxantal har lagts till i liståtgärds-cmdletarna Get-AzureRmEventHub och Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="b56aa-396">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="b56aa-397">Ett problem i New-AzureRmEventHub-cmdleten har åtgärdats där minst en parameter behövdes när du skapade en ny EventHub.</span><span class="sxs-lookup"><span data-stu-id="b56aa-397">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="b56aa-398">Angiven standardparameter har ställts in.</span><span class="sxs-lookup"><span data-stu-id="b56aa-398">Provided Default Parameter set.</span></span>
* <span data-ttu-id="b56aa-399">Valfri parameter för KeyValue har lagts till för New-AzureRmEventHubKey-cmdleten, vilket gör det möjligt att ange KeyValue.</span><span class="sxs-lookup"><span data-stu-id="b56aa-399">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="b56aa-400">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b56aa-400">AzureRM.KeyVault</span></span>
* <span data-ttu-id="b56aa-401">Åtgärda problem där alla resurser returnerades av Get-AzureRmKeyVault-taggen</span><span class="sxs-lookup"><span data-stu-id="b56aa-401">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="b56aa-402">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="b56aa-402">AzureRM.Network</span></span>
* <span data-ttu-id="b56aa-403">Gör nya SKU:er tillgängliga för zonredundanta VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="b56aa-403">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="b56aa-404">Nya kommandon har lagts till för funktionen: ExpressRoute Partner APIs via ARM</span><span class="sxs-lookup"><span data-stu-id="b56aa-404">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="b56aa-405">Get-AzureRmExpressRouteCrossConnection har lagts till</span><span class="sxs-lookup"><span data-stu-id="b56aa-405">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="b56aa-406">Set-AzureRmExpressRouteCrossConnection har lagts till</span><span class="sxs-lookup"><span data-stu-id="b56aa-406">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="b56aa-407">Add-AzureRmExpressRouteCrossConnectionPeering har lagts till</span><span class="sxs-lookup"><span data-stu-id="b56aa-407">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="b56aa-408">Get-AzureRmExpressRouteCrossConnectionPeering har lagts till</span><span class="sxs-lookup"><span data-stu-id="b56aa-408">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="b56aa-409">Remove-AzureRmExpressRouteCrossConnectionPeering har lagts till</span><span class="sxs-lookup"><span data-stu-id="b56aa-409">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="b56aa-410">Get-AzureRMExpressRouteCrossConnectionArpTable har lagts till</span><span class="sxs-lookup"><span data-stu-id="b56aa-410">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="b56aa-411">Get-AzureRMExpressRouteCrossConnectionRouteTable har lagts till</span><span class="sxs-lookup"><span data-stu-id="b56aa-411">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="b56aa-412">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary har lagts till</span><span class="sxs-lookup"><span data-stu-id="b56aa-412">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="b56aa-413">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b56aa-413">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="b56aa-414">Get-AzureRmRecoveryServicesBackupStatus-cmdlet har lagts till.</span><span class="sxs-lookup"><span data-stu-id="b56aa-414">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="b56aa-415">Denna cmdlet tar ett ID för virtuell dator och kontrollerar om den virtuella datorn skyddas av ett valv i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="b56aa-415">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="b56aa-416">Om ett sådant valv finns returnerar cmdleten valvinformationen.</span><span class="sxs-lookup"><span data-stu-id="b56aa-416">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="b56aa-417">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="b56aa-417">AzureRM.Resources</span></span>
* <span data-ttu-id="b56aa-418">Uppdatera Get-AzureRmPolicyAssignment-cmdletar:</span><span class="sxs-lookup"><span data-stu-id="b56aa-418">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="b56aa-419">Lägg till stöd för att lista -Scope-värden på hanteringsgruppsnivå</span><span class="sxs-lookup"><span data-stu-id="b56aa-419">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="b56aa-420">Lägg till stöd för hämtning av enskilda tilldelningar med -Scope-värden på hanteringsgruppsnivå.</span><span class="sxs-lookup"><span data-stu-id="b56aa-420">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="b56aa-421">Lägg till växlar för -Effective och -All till kontrollparametrar</span><span class="sxs-lookup"><span data-stu-id="b56aa-421">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="b56aa-422">Uppdatera Get/New/Remove/Set-AzureRmPolicyDefinition-cmdletar</span><span class="sxs-lookup"><span data-stu-id="b56aa-422">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="b56aa-423">Lägg till parameter för -ManagementGroupName om du vill tillämpa åtgärder för en viss hanteringsgrupp</span><span class="sxs-lookup"><span data-stu-id="b56aa-423">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="b56aa-424">Lägg till parameter för -SubscriptionId om du vill tillämpa åtgärder för en viss prenumeration</span><span class="sxs-lookup"><span data-stu-id="b56aa-424">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="b56aa-425">Uppdatera Get/New/Remove/Set-AzureRmPolicySetDefinition-cmdletar</span><span class="sxs-lookup"><span data-stu-id="b56aa-425">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="b56aa-426">Lägg till parameter för -ManagementGroupName om du vill tillämpa åtgärder för en viss hanteringsgrupp</span><span class="sxs-lookup"><span data-stu-id="b56aa-426">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="b56aa-427">Lägg till parameter för -SubscriptionId om du vill tillämpa åtgärder för en viss prenumeration</span><span class="sxs-lookup"><span data-stu-id="b56aa-427">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="b56aa-428">Lägg till stöd för hemliga KeyVault-referenser i parametrar när du använder "TemplateParameterObject" i "New-AzureRmResourceGroupDeployment"</span><span class="sxs-lookup"><span data-stu-id="b56aa-428">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="b56aa-429">Åtgärda problem med att "-EndDate"-parametern ignorerades på grund av "New-AzureRmADAppCredential"</span><span class="sxs-lookup"><span data-stu-id="b56aa-429">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="b56aa-430">Åtgärda problem med att felaktig URL användes i "New-AzureRmADAppCredential" vid begäran</span><span class="sxs-lookup"><span data-stu-id="b56aa-430">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="b56aa-431">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b56aa-431">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="b56aa-432">Valfri parameter för -KeyValue har lagts till för New-AzureRmServiceBusKey-cmdleten, vilket gör det möjligt att ange KeyValue.</span><span class="sxs-lookup"><span data-stu-id="b56aa-432">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="b56aa-433">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="b56aa-433">AzureRM.Sql</span></span>
* <span data-ttu-id="b56aa-434">Användardefinierade återställningspunkter har klargjorts för SQLDW i New-AzureRmSqlDatabaseRestorePoint-hjälpen</span><span class="sxs-lookup"><span data-stu-id="b56aa-434">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="b56aa-435">Dokumentationen om parametern -ComputeGeneration har uppdaterats i fler cmdletar</span><span class="sxs-lookup"><span data-stu-id="b56aa-435">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="b56aa-436">6.3.0 – juni 2018</span><span class="sxs-lookup"><span data-stu-id="b56aa-436">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="b56aa-437">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="b56aa-437">AzureRM.Profile</span></span>
* <span data-ttu-id="b56aa-438">Uppdaterade felmeddelanden för Enable-AzureRmContextAutoSave</span><span class="sxs-lookup"><span data-stu-id="b56aa-438">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="b56aa-439">Skapa en kontext för varje prenumeration när du kör ”Connect-AzureRmAccount” utan tidigare kontext</span><span class="sxs-lookup"><span data-stu-id="b56aa-439">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="b56aa-440">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="b56aa-440">Azure.Storage</span></span>
* <span data-ttu-id="b56aa-441">Ytterligare information om parametern -Permissions har lagts till i hjälpfilerna.</span><span class="sxs-lookup"><span data-stu-id="b56aa-441">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="b56aa-442">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="b56aa-442">AzureRM.Compute</span></span>
* <span data-ttu-id="b56aa-443">”Get-AzureRmVmDiskEncryptionStatus” korrigerar ett problem för virtuella datorer utan datadiskar</span><span class="sxs-lookup"><span data-stu-id="b56aa-443">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="b56aa-444">Uppdatera version av klientbibliotek för Compute för att korrigera följande cmdletar</span><span class="sxs-lookup"><span data-stu-id="b56aa-444">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="b56aa-445">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="b56aa-445">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="b56aa-446">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="b56aa-446">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="b56aa-447">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="b56aa-447">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="b56aa-448">Följande cmdletar har åtgärdats för att visa ”Åtgärds-ID” och ”Åtgärdsstatus” på ett korrekt sätt:</span><span class="sxs-lookup"><span data-stu-id="b56aa-448">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="b56aa-449">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b56aa-449">Start-AzureRmVM</span></span>
    - <span data-ttu-id="b56aa-450">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b56aa-450">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="b56aa-451">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b56aa-451">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="b56aa-452">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b56aa-452">Set-AzureRmVM</span></span>
    - <span data-ttu-id="b56aa-453">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="b56aa-453">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="b56aa-454">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b56aa-454">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="b56aa-455">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="b56aa-455">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="b56aa-456">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="b56aa-456">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="b56aa-457">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b56aa-457">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="b56aa-458">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b56aa-458">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="b56aa-459">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b56aa-459">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="b56aa-460">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b56aa-460">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="b56aa-461">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="b56aa-461">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="b56aa-462">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="b56aa-462">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="b56aa-463">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="b56aa-463">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="b56aa-464">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="b56aa-464">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="b56aa-465">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="b56aa-465">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="b56aa-466">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="b56aa-466">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="b56aa-467">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="b56aa-467">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="b56aa-468">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="b56aa-468">AzureRM.EventGrid</span></span>
* <span data-ttu-id="b56aa-469">Ta bort verifieringsvillkoren ValidateNotNullOrEmpty för SubjectBeginsWith/SubjectEndsWith i cmdleten Update-AzureRmEventGridSubscription för att ändra de här parametrarna till en tom sträng om det behövs.</span><span class="sxs-lookup"><span data-stu-id="b56aa-469">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="b56aa-470">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b56aa-470">AzureRM.KeyVault</span></span>
* <span data-ttu-id="b56aa-471">Åtgärda problem där inga taggar returneras när Get-AzureRmKeyVault -Tag körs</span><span class="sxs-lookup"><span data-stu-id="b56aa-471">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="b56aa-472">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="b56aa-472">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="b56aa-473">Offentlig lansering av cmdletar för Policy Insights</span><span class="sxs-lookup"><span data-stu-id="b56aa-473">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="b56aa-474">Använd API-version 2018-04-04</span><span class="sxs-lookup"><span data-stu-id="b56aa-474">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="b56aa-475">Lägg till PolicyDefinitionReferenceId i resultaten för Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="b56aa-475">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="b56aa-476">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b56aa-476">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="b56aa-477">Parametern -Vault har lagts till i cmdletarna för RecoveryServices.Backup.</span><span class="sxs-lookup"><span data-stu-id="b56aa-477">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="b56aa-478">När den godkänns åsidosätts cmdleten Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="b56aa-478">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="b56aa-479">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="b56aa-479">AzureRM.Sql</span></span>
* <span data-ttu-id="b56aa-480">Exemplet i hjälpfilen för Get-AzureRmSqlDatabaseExpanded har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="b56aa-480">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="b56aa-481">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="b56aa-481">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="b56aa-482">Hjälpfilen för Add-AzureRmTrafficManagerEndpointConfig har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="b56aa-482">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="b56aa-483">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="b56aa-483">AzureRM.Websites</span></span>
* <span data-ttu-id="b56aa-484">”Set-AzureRmWebApp” har uppdaterats så att den inte skriver över appinställningarna när du använder -AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="b56aa-484">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="b56aa-485">”New-AzureRMWebAppSlot” har uppdaterats för att visa att AppServicePlan är en valfri parameter</span><span class="sxs-lookup"><span data-stu-id="b56aa-485">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="b56aa-486">6.2.1 – juni 2018</span><span class="sxs-lookup"><span data-stu-id="b56aa-486">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="b56aa-487">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b56aa-487">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="b56aa-488">PSWorkspace-modellen har uppdaterats för att tillåta att nätverket använder typ som en parameter</span><span class="sxs-lookup"><span data-stu-id="b56aa-488">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="b56aa-489">6.2.0 – juni 2018</span><span class="sxs-lookup"><span data-stu-id="b56aa-489">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="b56aa-490">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="b56aa-490">AzureRM.Profile</span></span>
* <span data-ttu-id="b56aa-491">Åtgärda problemet med att version 10.0.3 av Newtonsoft.Json inte lästes in vid modulimporten</span><span class="sxs-lookup"><span data-stu-id="b56aa-491">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="b56aa-492">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="b56aa-492">AzureRM.Compute</span></span>
* <span data-ttu-id="b56aa-493">VMSS VM-uppdateringsfunktion</span><span class="sxs-lookup"><span data-stu-id="b56aa-493">VMSS VM Update feature</span></span>
    - <span data-ttu-id="b56aa-494">Cmdletarna Update-AzureRmVmssVM och New-AzureRmVMDataDisk har lagts till</span><span class="sxs-lookup"><span data-stu-id="b56aa-494">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="b56aa-495">Lägg till parametern VirtualMachineScaleSetVM till cmdleten Add-AzureRmVMDataDisk så att det går att lägga till en datadisk i den virtuella Vmss-datorn.</span><span class="sxs-lookup"><span data-stu-id="b56aa-495">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="b56aa-496">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="b56aa-496">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="b56aa-497">SDK:n för ADF .Net har uppdaterats till version 0.8.0-preview som innehåller följande ändringar:</span><span class="sxs-lookup"><span data-stu-id="b56aa-497">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="b56aa-498">Åtgärden för att konfigurera fabrikslagringsplatsen har lagts till</span><span class="sxs-lookup"><span data-stu-id="b56aa-498">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="b56aa-499">QuickBooks LinkedService har uppdaterats för att visa egenskaperna consumerKey och consumerSecret</span><span class="sxs-lookup"><span data-stu-id="b56aa-499">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="b56aa-500">Flera modelltyper från SecretBase till Object har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="b56aa-500">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="b56aa-501">Utlösaren Blob Events har lagts till</span><span class="sxs-lookup"><span data-stu-id="b56aa-501">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="b56aa-502">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b56aa-502">AzureRM.KeyVault</span></span>
* <span data-ttu-id="b56aa-503">Uppdatera dokumentation med exempel på utdata</span><span class="sxs-lookup"><span data-stu-id="b56aa-503">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="b56aa-504">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="b56aa-504">AzureRM.Network</span></span>
* <span data-ttu-id="b56aa-505">Aktivera Trafikanalys-parametrar på Network Watcher-cmdletar</span><span class="sxs-lookup"><span data-stu-id="b56aa-505">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="b56aa-506">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="b56aa-506">AzureRM.Resources</span></span>
* <span data-ttu-id="b56aa-507">Åtgärda problemet med egenskapen "Properties" för objekt(en) "PSResource" som returneras från "Get-AzureRmResource"</span><span class="sxs-lookup"><span data-stu-id="b56aa-507">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="b56aa-508">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="b56aa-508">AzureRM.Scheduler</span></span>
* <span data-ttu-id="b56aa-509">Åtgärda problemet med att nya autentiseringsvärden inte anges vid uppdatering av ServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="b56aa-509">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="b56aa-510">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="b56aa-510">AzureRM.Sql</span></span>
* <span data-ttu-id="b56aa-511">Följande cmdletar har uppdaterats med valfri LicenseType-parameter</span><span class="sxs-lookup"><span data-stu-id="b56aa-511">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="b56aa-512">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b56aa-512">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="b56aa-513">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="b56aa-513">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="b56aa-514">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="b56aa-514">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="b56aa-515">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="b56aa-515">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="b56aa-516">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b56aa-516">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="b56aa-517">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="b56aa-517">AzureRM.Websites</span></span>
* <span data-ttu-id="b56aa-518">New-AzureRMWebApp har uppdaterats för att använda vanliga algoritmer från biblioteket Strategy.</span><span class="sxs-lookup"><span data-stu-id="b56aa-518">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="b56aa-519">6.1.0 – maj 2018</span><span class="sxs-lookup"><span data-stu-id="b56aa-519">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="b56aa-520">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="b56aa-520">AzureRM.Profile</span></span>
* <span data-ttu-id="b56aa-521">Åtgärda problem där en körning av Clear-AzureRmContext skulle bevara en tom kontext med namnet på den föregående standardkontexten som gjorde att användaren inte kunde skapa en ny kontext med det gamla namnet</span><span class="sxs-lookup"><span data-stu-id="b56aa-521">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="b56aa-522">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="b56aa-522">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="b56aa-523">Aktivera Gateway associerings- och avassocieringsåtgärder på AS.</span><span class="sxs-lookup"><span data-stu-id="b56aa-523">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="b56aa-524">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b56aa-524">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="b56aa-525">Stöd för ApiVersions, ApiReleases och ApiRevisions har lagts till</span><span class="sxs-lookup"><span data-stu-id="b56aa-525">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="b56aa-526">Stöd för serverdelen på ServiceFabric har lagts till</span><span class="sxs-lookup"><span data-stu-id="b56aa-526">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="b56aa-527">Stöd för Application Insights-loggare har lagts till</span><span class="sxs-lookup"><span data-stu-id="b56aa-527">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="b56aa-528">Stöd för att identifiera SKU:n ”Basic” som en giltig SKU för Api Management-tjänsten har lagts till</span><span class="sxs-lookup"><span data-stu-id="b56aa-528">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="b56aa-529">Stöd för att installera certifikat som utfärdats av privata certifikatutfärdare som rot eller certifikatutfärdare har lagts till</span><span class="sxs-lookup"><span data-stu-id="b56aa-529">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="b56aa-530">Stöd för att godkänna anpassade SSL-certifikat via KeyVault och flera proxy-värdnamn har lagts till</span><span class="sxs-lookup"><span data-stu-id="b56aa-530">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="b56aa-531">Stöd för MSI-identitet har lagts till</span><span class="sxs-lookup"><span data-stu-id="b56aa-531">Added support for MSI identity</span></span>
* <span data-ttu-id="b56aa-532">Stöd för att godkänna principer via URL har lagts till. Obs! Följande cmdletar blir inaktuella i framtida versioner</span><span class="sxs-lookup"><span data-stu-id="b56aa-532">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="b56aa-533">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="b56aa-533">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="b56aa-534">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="b56aa-534">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="b56aa-535">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="b56aa-535">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="b56aa-536">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="b56aa-536">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="b56aa-537">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="b56aa-537">AzureRM.Batch</span></span>
* <span data-ttu-id="b56aa-538">Släpp nya cmdleten Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="b56aa-538">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="b56aa-539">Släpp nya cmdleten Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="b56aa-539">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="b56aa-540">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="b56aa-540">AzureRM.Consumption</span></span>
* <span data-ttu-id="b56aa-541">Lägg till nya parametrar Expand, ResourceGroup, InstanceName, InstanceId, Tags och Top på cmdleten Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="b56aa-541">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="b56aa-542">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b56aa-542">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="b56aa-543">Åtgärda exempel för Export AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="b56aa-543">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="b56aa-544">Åtgärda undantag för null-parameter för rekursivt ärende i Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="b56aa-544">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="b56aa-545">Åtgärda hjälpfilerna för Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="b56aa-545">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="b56aa-546">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="b56aa-546">AzureRM.Network</span></span>
* <span data-ttu-id="b56aa-547">Öka nätverkets SDK-version från förhandsversionen 18.0.0 till förhandsversionen 19.0.0</span><span class="sxs-lookup"><span data-stu-id="b56aa-547">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="b56aa-548">Cmdlet har lagts till för att skapa protokollinformation</span><span class="sxs-lookup"><span data-stu-id="b56aa-548">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="b56aa-549">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="b56aa-549">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="b56aa-550">Cmdlet har lagts till för att lägga till en ny kretsanslutning till en befintlig expressroute-krets.</span><span class="sxs-lookup"><span data-stu-id="b56aa-550">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="b56aa-551">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="b56aa-551">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="b56aa-552">Cmdlet har lagts till för att ta bort en kretsanslutning från en befintlig expressroute-krets.</span><span class="sxs-lookup"><span data-stu-id="b56aa-552">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="b56aa-553">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="b56aa-553">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="b56aa-554">Cmdlet har lagts till för att hämta en kretsanslutning</span><span class="sxs-lookup"><span data-stu-id="b56aa-554">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="b56aa-555">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="b56aa-555">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="b56aa-556">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b56aa-556">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="b56aa-557">Användning med serverautentisering med genererade certifikat (problem #5998) har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="b56aa-557">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="b56aa-558">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="b56aa-558">AzureRM.Sql</span></span>
* <span data-ttu-id="b56aa-559">Cmdletar för granskning för att ta bort AuditActions eller AuditActionGroups har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="b56aa-559">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="b56aa-560">Åtgärdade problem med Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy vid konfigurering av en ny flexibel bevarandeprincip där kommandot misslyckas med ett meddelande om att konfigurering av långsiktig bevarandeprincip med Azure Recovery Service-valv och principen inte längre stöds,</span><span class="sxs-lookup"><span data-stu-id="b56aa-560">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="b56aa-561">och att en begäran med den nya flexibla bevarandeprincipen ska skickas.</span><span class="sxs-lookup"><span data-stu-id="b56aa-561">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="b56aa-562">Uppdatera alla Azure Sql Database/ElasticPool Creation/Update-relaterade cmdletar för att använda det nya databas-API:et som stöder SKU-egenskaper för skalnings- och nivårelaterade egenskaper.</span><span class="sxs-lookup"><span data-stu-id="b56aa-562">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="b56aa-563">Cmdletar har uppdaterats, inklusive:</span><span class="sxs-lookup"><span data-stu-id="b56aa-563">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="b56aa-564">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b56aa-564">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="b56aa-565">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="b56aa-565">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="b56aa-566">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="b56aa-566">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="b56aa-567">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="b56aa-567">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="b56aa-568">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b56aa-568">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="b56aa-569">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="b56aa-569">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="b56aa-570">Uppdatera parametrarna för Get-AzureRmTrafficManagerProfile så att ResourceGroupName-parametern blir obligatorisk när du använder Name-parametern.</span><span class="sxs-lookup"><span data-stu-id="b56aa-570">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
