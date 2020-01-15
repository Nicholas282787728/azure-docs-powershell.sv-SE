---
title: Viktig information om Azure PowerShell
description: Lär dig mer om alla de senaste uppdateringarna för Azure PowerShell-modulerna.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/09/2020
ms.openlocfilehash: 3806a1c609a71c53c0bddc5bafd51d845c0c296e
ms.sourcegitcommit: 16904e0a72c55fb81248e0252769defb86c50f36
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/10/2020
ms.locfileid: "75831652"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="42f58-103">Viktig information om Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="42f58-103">Azure PowerShell release notes</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="42f58-104">3.3.0 – januari 2020</span><span class="sxs-lookup"><span data-stu-id="42f58-104">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="42f58-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="42f58-105">Az.Accounts</span></span>
* <span data-ttu-id="42f58-106">Nu stöder Add-AzEnvironment och Set-AzEnvironment parametrarna AzureAttestationServiceEndpointResourceId och AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="42f58-106">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="42f58-107">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="42f58-107">Az.Cdn</span></span>
* <span data-ttu-id="42f58-108">Information om felsvar visas i New-AzCdnEndpoint-cmdleten</span><span class="sxs-lookup"><span data-stu-id="42f58-108">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="42f58-109">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="42f58-109">Az.Compute</span></span>
* <span data-ttu-id="42f58-110">Set-AzVMCustomScriptExtension-cmdleten har åtgärdats för en virtuell dator med hanterad OD-disk som inte har någon operativsystemprofil.</span><span class="sxs-lookup"><span data-stu-id="42f58-110">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="42f58-111">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="42f58-111">Az.ContainerInstance</span></span>
* <span data-ttu-id="42f58-112">Parameternamn som används med New-AzContainerGroup-exempel har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="42f58-112">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="42f58-113">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="42f58-113">Az.DataBoxEdge</span></span>
* <span data-ttu-id="42f58-114">Cmdleten ”Get-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="42f58-114">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="42f58-115">Hämta gränslagringscontainern</span><span class="sxs-lookup"><span data-stu-id="42f58-115">Get the Edge Storage Container</span></span>
* <span data-ttu-id="42f58-116">Cmdleten ”New-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="42f58-116">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="42f58-117">Skapa en ny gränslagringscontainer</span><span class="sxs-lookup"><span data-stu-id="42f58-117">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="42f58-118">Cmdleten ”Remove-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="42f58-118">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="42f58-119">Ta bort gränslagringscontainern</span><span class="sxs-lookup"><span data-stu-id="42f58-119">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="42f58-120">Cmdleten ”Invoke-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="42f58-120">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="42f58-121">Anropa åtgärd för att uppdatera data i gränslagringscontainer</span><span class="sxs-lookup"><span data-stu-id="42f58-121">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="42f58-122">Cmdleten ”Get-AzDataBoxEdgeStorageAccount” har lagts till</span><span class="sxs-lookup"><span data-stu-id="42f58-122">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="42f58-123">Hämta gränslagringskontot</span><span class="sxs-lookup"><span data-stu-id="42f58-123">Get the Edge Storage Account</span></span>
* <span data-ttu-id="42f58-124">Cmdleten ”New-AzDataBoxEdgeStorageAccount” har lagts till</span><span class="sxs-lookup"><span data-stu-id="42f58-124">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="42f58-125">Skapa ett nytt gränslagringskonto</span><span class="sxs-lookup"><span data-stu-id="42f58-125">Create new Edge Storage Account</span></span>
* <span data-ttu-id="42f58-126">Cmdleten ”Remove-AzDataBoxEdgeStorageAccount” har lagts till</span><span class="sxs-lookup"><span data-stu-id="42f58-126">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="42f58-127">Ta bort gränslagringskontot</span><span class="sxs-lookup"><span data-stu-id="42f58-127">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="42f58-128">Anropa cmdleten ”Invoke-AzDataBoxEdgeShare”</span><span class="sxs-lookup"><span data-stu-id="42f58-128">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="42f58-129">Anropa åtgärd för att uppdatera resursdata</span><span class="sxs-lookup"><span data-stu-id="42f58-129">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="42f58-130">Cmdleten ”Set-AzDataBoxEdgeStorageAccountCredential” har lagts till</span><span class="sxs-lookup"><span data-stu-id="42f58-130">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="42f58-131">Ange autentiseringsuppgifter för az databoxedge-lagringskonto</span><span class="sxs-lookup"><span data-stu-id="42f58-131">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="42f58-132">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="42f58-132">Az.DataFactory</span></span>
* <span data-ttu-id="42f58-133">Lägg till AutoUpdateETA-, LatestVersion-, PushedVersion-, TaskQueueId- och VersionStatus-egenskaper för Get-AzDataFactoryV2IntegrationRuntime-cmd</span><span class="sxs-lookup"><span data-stu-id="42f58-133">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="42f58-134">Uppdatera ADF .Net SDK-versionen till 4.6.0</span><span class="sxs-lookup"><span data-stu-id="42f58-134">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="42f58-135">Lägg till parametern ”PublicIPs” för ”Set-AzureRmDataFactoryV2IntegrationRuntime”-cmd så att Azure-SSIS IR kan skapas med statiska offentliga IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="42f58-135">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="42f58-136">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="42f58-136">Az.DevTestLabs</span></span>
* <span data-ttu-id="42f58-137">Ta bort den brutna länken i Get-AzDtlAllowedVMSizesPolicy.md</span><span class="sxs-lookup"><span data-stu-id="42f58-137">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="42f58-138">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="42f58-138">Az.EventHub</span></span>
* <span data-ttu-id="42f58-139">Korrigering av problem 10634: Åtgärda referensen till null-objekt för eventhubnamespace-borttagning</span><span class="sxs-lookup"><span data-stu-id="42f58-139">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="42f58-140">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="42f58-140">Az.HDInsight</span></span>
* <span data-ttu-id="42f58-141">Åtgärda Invoke-AzHDInsightHiveJob.md-fel.</span><span class="sxs-lookup"><span data-stu-id="42f58-141">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="42f58-142">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="42f58-142">Az.MachineLearning</span></span>
* <span data-ttu-id="42f58-143">Nedanstående cmdletar har tagits bort eftersom MachineLearningCompute inte längre är tillgängligt</span><span class="sxs-lookup"><span data-stu-id="42f58-143">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="42f58-144">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="42f58-144">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="42f58-145">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="42f58-145">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="42f58-146">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="42f58-146">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="42f58-147">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="42f58-147">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="42f58-148">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="42f58-148">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="42f58-149">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="42f58-149">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="42f58-150">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="42f58-150">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="42f58-151">Az.Network</span><span class="sxs-lookup"><span data-stu-id="42f58-151">Az.Network</span></span>
* <span data-ttu-id="42f58-152">Uppgradera beroende av Microsoft.Azure.Management.Sql från 1.36-preview till 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="42f58-152">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="42f58-153">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="42f58-153">Az.RecoveryServices</span></span>
* <span data-ttu-id="42f58-154">Ändrat Azure Site Recovery-stöd för krypterade vilande data på virtuella datorer med hanterade diskar med kundhanterade nycklar för Azure till Azure-providern.</span><span class="sxs-lookup"><span data-stu-id="42f58-154">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed leys for Azure to Azure provider.</span></span>
* <span data-ttu-id="42f58-155">Azure Site Recovery-stöd för att ange ID för diskkrypteringsuppsättning som valfri inmatning för aktivering av skydd för VMware till Azure.</span><span class="sxs-lookup"><span data-stu-id="42f58-155">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="42f58-156">Azure Site Recovery-stöd för att ange ID för diskkrypteringsuppsättning som valfri inmatning på disknivå för aktivering av skydd för VMware till Azure.</span><span class="sxs-lookup"><span data-stu-id="42f58-156">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="42f58-157">Azure Site Recovery-stöd för att uppdatera replikeringsskyddade objekt med mappning för diskkrypteringsuppsättning för HyperV till Azure.</span><span class="sxs-lookup"><span data-stu-id="42f58-157">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="42f58-158">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="42f58-158">Az.Resources</span></span>
* <span data-ttu-id="42f58-159">Åtgärda ett fel i hjälpdokument för ”Remove-AzTag”.</span><span class="sxs-lookup"><span data-stu-id="42f58-159">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="42f58-160">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="42f58-160">Az.Sql</span></span>
* <span data-ttu-id="42f58-161">Åtgärda funktioner i cmdletar för att ange baslinjen för sårbarhetsbedömning för arbete med huvuddatabasen för Azure-databasen och begränsa den för systemdatabaser på hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="42f58-161">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="42f58-162">Åtgärda ett fel när en redundansgrupp för en SQL-instans skapas</span><span class="sxs-lookup"><span data-stu-id="42f58-162">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="42f58-163">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="42f58-163">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="42f58-164">Lägg till DR som en ny giltig licenstyp</span><span class="sxs-lookup"><span data-stu-id="42f58-164">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="42f58-165">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="42f58-165">Az.Storage</span></span>
* <span data-ttu-id="42f58-166">Lägg till varningsmeddelande om icke-bakåtkompatibel ändring för DefaultAction-värdeändring i en framtida version</span><span class="sxs-lookup"><span data-stu-id="42f58-166">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="42f58-167">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="42f58-167">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="42f58-168">Stöd för att hämta lagringskontots senaste synkroniseringstid genom att köra get-AzureRMStorageAccount med parametern -IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="42f58-168">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span> 
    - <span data-ttu-id="42f58-169">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="42f58-169">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="42f58-170">3.2.0 – December 2019</span><span class="sxs-lookup"><span data-stu-id="42f58-170">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="42f58-171">Allmänt</span><span class="sxs-lookup"><span data-stu-id="42f58-171">General</span></span>
* <span data-ttu-id="42f58-172">Uppdatera referenser i .psd1 för att använda relativa sökvägar för alla moduler</span><span class="sxs-lookup"><span data-stu-id="42f58-172">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="42f58-173">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="42f58-173">Az.Accounts</span></span>
* <span data-ttu-id="42f58-174">Ange rätt UserAgent för telemetri på klientsidan för Az 4.0 preview</span><span class="sxs-lookup"><span data-stu-id="42f58-174">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="42f58-175">Visa användarvänligt felmeddelande när kontexten är null i Az 4.0 preview</span><span class="sxs-lookup"><span data-stu-id="42f58-175">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="42f58-176">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="42f58-176">Az.Batch</span></span>
* <span data-ttu-id="42f58-177">Korrigera problem [#10602](https://github.com/Azure/azure-powershell/issues/10602), där **New-AzBatchPool** skickade VirtualMachineConfiguration.ContainerConfiguration eller VirtualMachineConfiguration.DataDisks på ett felaktigt sätt till servern.</span><span class="sxs-lookup"><span data-stu-id="42f58-177">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="42f58-178">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="42f58-178">Az.DataFactory</span></span>
* <span data-ttu-id="42f58-179">Uppdatera ADF .Net SDK-versionen till 4.5.0</span><span class="sxs-lookup"><span data-stu-id="42f58-179">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="42f58-180">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="42f58-180">Az.FrontDoor</span></span>
* <span data-ttu-id="42f58-181">Stöd har lagts till för undantag för hanterade regler för brandväggen för webbaserade program</span><span class="sxs-lookup"><span data-stu-id="42f58-181">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="42f58-182">Lägg till SocketAddr för automatisk komplettering</span><span class="sxs-lookup"><span data-stu-id="42f58-182">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="42f58-183">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="42f58-183">Az.HealthcareApis</span></span>
* <span data-ttu-id="42f58-184">Undantagshantering</span><span class="sxs-lookup"><span data-stu-id="42f58-184">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="42f58-185">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="42f58-185">Az.KeyVault</span></span>
* <span data-ttu-id="42f58-186">Åtgärdat fel vid åtkomst av värde som kanske inte har angetts</span><span class="sxs-lookup"><span data-stu-id="42f58-186">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="42f58-187">Hantering av ECC-certifikat (Elliptic Curve Cryptography)</span><span class="sxs-lookup"><span data-stu-id="42f58-187">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="42f58-188">Stöd har lagts till för att ange kurvan för certifikatprinciper</span><span class="sxs-lookup"><span data-stu-id="42f58-188">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="42f58-189">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="42f58-189">Az.Monitor</span></span>
* <span data-ttu-id="42f58-190">Lägger till valfritt argument i kommandot Lägg till diagnostikinställningar.</span><span class="sxs-lookup"><span data-stu-id="42f58-190">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="42f58-191">Ett växelargument som om det finns visar att exporten till Log Analytics måste ske till ett fast schema (kallas även</span><span class="sxs-lookup"><span data-stu-id="42f58-191">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="42f58-192">dedikerad, datatyp)</span><span class="sxs-lookup"><span data-stu-id="42f58-192">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="42f58-193">Az.Network</span><span class="sxs-lookup"><span data-stu-id="42f58-193">Az.Network</span></span>
* <span data-ttu-id="42f58-194">Stöd för IpGroups i program-, NAT- och nätverksregler för Azure Firewall.</span><span class="sxs-lookup"><span data-stu-id="42f58-194">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="42f58-195">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="42f58-195">Az.Resources</span></span>
* <span data-ttu-id="42f58-196">Åtgärda ett problem där malldistributionen inte kan läsa en mallparameter om dess namn står i konflikt med ett inbyggt parameternamn.</span><span class="sxs-lookup"><span data-stu-id="42f58-196">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="42f58-197">Uppdaterade princip-cmdletar för att använda den nya API-versionen 2019-09-01 som introducerar grupperingsstöd inom principuppsättningsdefinitioner.</span><span class="sxs-lookup"><span data-stu-id="42f58-197">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="42f58-198">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="42f58-198">Az.Sql</span></span>
* <span data-ttu-id="42f58-199">Uppgraderad funktion för att skapa lagring i automatisk aktivering av sårbarhetsbedömning till StorageV2</span><span class="sxs-lookup"><span data-stu-id="42f58-199">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="42f58-200">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="42f58-200">Az.Storage</span></span>
* <span data-ttu-id="42f58-201">Stöd för generering av blob/container-identitetsbaserad SAS-token med lagringskontextbaserad på OAuth-autentisering</span><span class="sxs-lookup"><span data-stu-id="42f58-201">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="42f58-202">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="42f58-202">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="42f58-203">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="42f58-203">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="42f58-204">Stöd för återkallning av användardelegeringsnycklar för lagringskonto för att återkalla alla SAS-token</span><span class="sxs-lookup"><span data-stu-id="42f58-204">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="42f58-205">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="42f58-205">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="42f58-206">Uppgradera till Microsoft.Azure.Management.Storage 14.2.0 för att stödja den nya API-versionen 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="42f58-206">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="42f58-207">Stöd för QuotaGiB (resurskvot i Gibibye) för värden över 5120 i hanteringsplanet för cmdletar för filresurser och parameteraliaset. Quota har också lagts till för parametern ”QuotaGiB”.</span><span class="sxs-lookup"><span data-stu-id="42f58-207">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span> 
    - <span data-ttu-id="42f58-208">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="42f58-208">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="42f58-209">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="42f58-209">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="42f58-210">Lägg till parameteraliaset QuotaGiB i parametern Quota</span><span class="sxs-lookup"><span data-stu-id="42f58-210">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="42f58-211">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="42f58-211">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="42f58-212">Åtgärda problemet att Set-AzStorageContainerAcl kan rensa den lagrade åtkomstprincipen</span><span class="sxs-lookup"><span data-stu-id="42f58-212">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="42f58-213">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="42f58-213">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="42f58-214">3.1.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="42f58-214">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="42f58-215">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="42f58-215">Highlights since the last major release</span></span>
* <span data-ttu-id="42f58-216">Az.DataBoxEdge 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="42f58-216">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="42f58-217">Az.SqlVirtualMachine 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="42f58-217">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="42f58-218">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="42f58-218">Az.Compute</span></span>
* <span data-ttu-id="42f58-219">Funktion för att använda en virtuell dator igen</span><span class="sxs-lookup"><span data-stu-id="42f58-219">VM Reapply feature</span></span>
    - <span data-ttu-id="42f58-220">Lägg till parameter för att använda igen till cmdleten Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="42f58-220">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="42f58-221">Funktionen AutomaticRepairs i VM-skalningsuppsättningar:</span><span class="sxs-lookup"><span data-stu-id="42f58-221">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="42f58-222">Lägg till parametrarna EnableAutomaticRepair, AutomaticRepairGracePeriod och AutomaticRepairMaxInstanceRepairsPercent till följande cmdletar:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="42f58-222">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="42f58-223">Stöd för galleriavbildningar i flera klientorganisationer för New-AzVM</span><span class="sxs-lookup"><span data-stu-id="42f58-223">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="42f58-224">Lägg till "Spot" till argumentslutföraren i prioritetsparametern i cmdletarna New-AzVM, New-AzVMConfig och New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="42f58-224">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="42f58-225">Lägg till parametrarna DiskIOPSReadWrite och DiskMBpsReadWrite till cmdleten Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="42f58-225">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="42f58-226">Ändra parametern SourceImageId för cmdleten New-AzGalleryImageVersion till valfri</span><span class="sxs-lookup"><span data-stu-id="42f58-226">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="42f58-227">Lägg till parametrarna OSDiskImage och DataDiskImage till cmdleten New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="42f58-227">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="42f58-228">Lägg till parametern HyperVGeneration till cmdleten New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="42f58-228">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="42f58-229">Lägg till parametern SkipExtensionsOnOverprovisionedVMs till cmdletarna New-AzVmss, New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="42f58-229">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="42f58-230">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="42f58-230">Az.DataBoxEdge</span></span>
* <span data-ttu-id="42f58-231">Cmdleten `Get-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="42f58-231">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="42f58-232">Hämta ordning</span><span class="sxs-lookup"><span data-stu-id="42f58-232">Get the Order</span></span>
* <span data-ttu-id="42f58-233">Cmdleten `New-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="42f58-233">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="42f58-234">Skapa ny ordning</span><span class="sxs-lookup"><span data-stu-id="42f58-234">Create new Order</span></span>
* <span data-ttu-id="42f58-235">Cmdleten `Remove-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="42f58-235">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="42f58-236">Ta bort ordning</span><span class="sxs-lookup"><span data-stu-id="42f58-236">Remove the Order</span></span>
* <span data-ttu-id="42f58-237">Cmdleten `New-AzDataBoxEdgeShare` har ändrats</span><span class="sxs-lookup"><span data-stu-id="42f58-237">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="42f58-238">Nu skapas lokal filresurs</span><span class="sxs-lookup"><span data-stu-id="42f58-238">Now creates Local Share</span></span>
* <span data-ttu-id="42f58-239">Cmdleten `Set-AzDataBoxEdgeRole` har lagts till</span><span class="sxs-lookup"><span data-stu-id="42f58-239">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="42f58-240">Nu kan IotRole mappas till filresursen</span><span class="sxs-lookup"><span data-stu-id="42f58-240">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="42f58-241">Cmdleten `Invoke-AzDataBoxEdgeDevice` har lagts till</span><span class="sxs-lookup"><span data-stu-id="42f58-241">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="42f58-242">Anropa genomsökningsuppdatering, ladda ned uppdatering, installera uppdateringar på enheten</span><span class="sxs-lookup"><span data-stu-id="42f58-242">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="42f58-243">Cmdleten `Get-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="42f58-243">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="42f58-244">Hämtar information om utlösare</span><span class="sxs-lookup"><span data-stu-id="42f58-244">Gets the information about Triggers</span></span>
* <span data-ttu-id="42f58-245">Cmdleten `New-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="42f58-245">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="42f58-246">Skapa nya utlösare</span><span class="sxs-lookup"><span data-stu-id="42f58-246">Create new Triggers</span></span>
* <span data-ttu-id="42f58-247">Cmdleten `Remove-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="42f58-247">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="42f58-248">Ta bort utlösare</span><span class="sxs-lookup"><span data-stu-id="42f58-248">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="42f58-249">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="42f58-249">Az.DataFactory</span></span>
* <span data-ttu-id="42f58-250">Uppdatera ADF .Net SDK-versionen till 4.4.0</span><span class="sxs-lookup"><span data-stu-id="42f58-250">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="42f58-251">Lägg till parametern ExpressCustomSetup för kommandot Set-AzureRmDataFactoryV2IntegrationRuntime för att aktivera installationskonfigurationer och komponenter från tredje part utan anpassat konfigurationsskript.</span><span class="sxs-lookup"><span data-stu-id="42f58-251">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="42f58-252">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="42f58-252">Az.DataLakeStore</span></span>
* <span data-ttu-id="42f58-253">Uppdatera dokumentation för Get-AzDataLakeStoreDeletedItem och Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="42f58-253">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="42f58-254">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="42f58-254">Az.EventHub</span></span>
* <span data-ttu-id="42f58-255">Korrigering av problem #10301: Korrigera datumformat för SAS-token</span><span class="sxs-lookup"><span data-stu-id="42f58-255">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="42f58-256">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="42f58-256">Az.FrontDoor</span></span>
* <span data-ttu-id="42f58-257">Lägg till parametern MinimumTlsVersion till Enable-AzFrontDoorCustomDomainHttps och New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="42f58-257">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="42f58-258">Lägg till parametrarna HealthProbeMethod och EnabledState till New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="42f58-258">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="42f58-259">Lägg till en ny cmdlet för att skapa BackendPoolsSettings-objekt som passar i skapande/uppdatering av Front Door</span><span class="sxs-lookup"><span data-stu-id="42f58-259">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="42f58-260">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="42f58-260">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="42f58-261">Az.Network</span><span class="sxs-lookup"><span data-stu-id="42f58-261">Az.Network</span></span>
* <span data-ttu-id="42f58-262">Ändra alternativexemplen Start-AzVirtualNetworkGatewayConnectionPacketCapture.md och Start-AzVirtualnetworkGatewayPacketCapture.md för FilterData.</span><span class="sxs-lookup"><span data-stu-id="42f58-262">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="42f58-263">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="42f58-263">Az.PrivateDns</span></span>
* <span data-ttu-id="42f58-264">Uppdaterade PrivateDns .NET SDK till version 1.0.0</span><span class="sxs-lookup"><span data-stu-id="42f58-264">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="42f58-265">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="42f58-265">Az.RecoveryServices</span></span>
* <span data-ttu-id="42f58-266">Stöd för att välja disktyp vid aktivering av skydd i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="42f58-266">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="42f58-267">Korrigering av bugg för åtgärdsredigering av återställningsplan i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="42f58-267">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="42f58-268">Återställningsstöd för att godkänna filestream-databaser i Azure Backup SQL.</span><span class="sxs-lookup"><span data-stu-id="42f58-268">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="42f58-269">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="42f58-269">Az.RedisCache</span></span>
* <span data-ttu-id="42f58-270">Parametern MinimumTlsVersion har lagts till i cmdletarna New-AzRedisCache och Set-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="42f58-270">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="42f58-271">Dessutom har MinimumTlsVersion lagts till i utdata för cmdleten Get-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="42f58-271">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="42f58-272">Verifiering har lagts till på parametern -Size i cmdletarna Set-AzRedisCache och New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="42f58-272">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="42f58-273">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="42f58-273">Az.Resources</span></span>
- <span data-ttu-id="42f58-274">Uppdaterade policy-cmdletar för att använda den nya API-versionen 2019-06-01 som har en ny EnforcementMode-egenskap i policytilldelningen.</span><span class="sxs-lookup"><span data-stu-id="42f58-274">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="42f58-275">Uppdaterade hjälpexempel för skapandet av policydefinition</span><span class="sxs-lookup"><span data-stu-id="42f58-275">Updated create policy definition help example</span></span>
- <span data-ttu-id="42f58-276">Åtgärda bugg i Remove-AZADServicePrincipal -ServicePrincipalName, utlös null-referens när tjänstens huvudnamn inte hittas.</span><span class="sxs-lookup"><span data-stu-id="42f58-276">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="42f58-277">Åtgärda bugg i New-AZADServicePrincipal, utlös null-referens när klientorganisationen inte har någon prenumeration.</span><span class="sxs-lookup"><span data-stu-id="42f58-277">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="42f58-278">Ändra New-AzAdServicePrincipal för att endast lägga till autentiseringsuppgifter för det associerade programmet.</span><span class="sxs-lookup"><span data-stu-id="42f58-278">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="42f58-279">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="42f58-279">Az.Sql</span></span>
* <span data-ttu-id="42f58-280">Stöd har lagts till för databasen ReadReplicaCount.</span><span class="sxs-lookup"><span data-stu-id="42f58-280">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="42f58-281">Korrigerade Set-AzSqlDatabase när zonredundans inte har angetts</span><span class="sxs-lookup"><span data-stu-id="42f58-281">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="42f58-282">3.0.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="42f58-282">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="42f58-283">Allmänt</span><span class="sxs-lookup"><span data-stu-id="42f58-283">General</span></span>
* <span data-ttu-id="42f58-284">Az. PrivateDns 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="42f58-284">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="42f58-285">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="42f58-285">Az.Accounts</span></span>
* <span data-ttu-id="42f58-286">Lägg till ett utfasningsmeddelande för aliaset Resolve-error.</span><span class="sxs-lookup"><span data-stu-id="42f58-286">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="42f58-287">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="42f58-287">Az.Advisor</span></span>
* <span data-ttu-id="42f58-288">Den nya kategorin Operational Excellence har lagts till i cmdleten Get-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="42f58-288">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="42f58-289">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="42f58-289">Az.Batch</span></span>
* <span data-ttu-id="42f58-290">`CoreQuota` på `BatchAccountContext` har bytt namn till `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="42f58-290">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="42f58-291">Det finns även en ny `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="42f58-291">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="42f58-292">Detta påverkar **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="42f58-292">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="42f58-293">**New-AzBatchTask** `-ResourceFile`-parametern tar nu en samling `PSResourceFile`-objekt som kan skapas med hjälp av den nya cmdleten **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="42f58-293">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="42f58-294">Ny **New-AzBatchResourceFile**-cmdlet för att skapa `PSResourceFile`-objekt.</span><span class="sxs-lookup"><span data-stu-id="42f58-294">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="42f58-295">Dessa kan tillhandahållas till **New-AzBatchTask** på `-ResourceFile`-parametern.</span><span class="sxs-lookup"><span data-stu-id="42f58-295">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="42f58-296">Detta stöder två nya typer av resursfiler förutom det befintliga sättet med `HttpUrl`:</span><span class="sxs-lookup"><span data-stu-id="42f58-296">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="42f58-297">`AutoStorageContainerName`-baserade resursfiler laddar ned en hel container för automatisk lagring till Batch-noden.</span><span class="sxs-lookup"><span data-stu-id="42f58-297">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="42f58-298">`StorageContainerUrl`-baserade resursfiler laddar ned containern som anges i webbadressen till Batch-noden.</span><span class="sxs-lookup"><span data-stu-id="42f58-298">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="42f58-299">Tog bort egenskapen `ApplicationPackages` för `PSApplication` som returnerades av **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="42f58-299">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="42f58-300">Specifika paket i ett program kan nu hämtas med hjälp av **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="42f58-300">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="42f58-301">Till exempel: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="42f58-301">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="42f58-302">Bytt namn på `ApplicationId` till `ApplicationName` på **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** och **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="42f58-302">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="42f58-303">`ApplicationId` är nu ett alias för `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="42f58-303">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="42f58-304">Ny `PSWindowsUserConfiguration`-egenskap till `PSUserAccount` lades till.</span><span class="sxs-lookup"><span data-stu-id="42f58-304">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="42f58-305">Bytte namn på `Version` till `Name` på `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="42f58-305">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="42f58-306">Bytte namn på `BlobSource` till `HttpUrl` på `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="42f58-306">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="42f58-307">Tog bort egenskapen `OSDisk` från `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="42f58-307">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="42f58-308">Tog bort **Set-AzBatchPoolOSVersion**.</span><span class="sxs-lookup"><span data-stu-id="42f58-308">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="42f58-309">Den här åtgärden stöds inte längre.</span><span class="sxs-lookup"><span data-stu-id="42f58-309">This operation is no longer supported.</span></span>
* <span data-ttu-id="42f58-310">`TargetOSVersion` har tagits bort från `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="42f58-310">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="42f58-311">Bytte namn på `CurrentOSVersion` till `OSVersion` på `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="42f58-311">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="42f58-312">`DataEgressGiB` och `DataIngressGiB` har tagits bort från `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="42f58-312">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="42f58-313">Tog bort **Get-AzBatchNodeAgentSku** och ersatte det med **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="42f58-313">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span> 
  - <span data-ttu-id="42f58-314">**Get-AzBatchSupportedImage** returnerar samma data som **Get-AzBatchNodeAgentSku** men i ett mer användarvänligt format.</span><span class="sxs-lookup"><span data-stu-id="42f58-314">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="42f58-315">Nya icke-verifierade avbildningar returneras nu också.</span><span class="sxs-lookup"><span data-stu-id="42f58-315">New non-verified images are also now returned.</span></span> <span data-ttu-id="42f58-316">Ytterligare information om `Capabilities` och `BatchSupportEndOfLife` för varje avbildning inkluderas också.</span><span class="sxs-lookup"><span data-stu-id="42f58-316">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="42f58-317">Lade till möjlighet att montera fjärrfilsystem på varje nod i en pool via den nya parametern `MountConfiguration` för **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="42f58-317">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="42f58-318">Har nu stöd för nätverkssäkerhetsregler som blockerar nätverksåtkomst till en pool baserat på källportens trafik.</span><span class="sxs-lookup"><span data-stu-id="42f58-318">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="42f58-319">Detta görs via egenskapen `SourcePortRanges` på `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="42f58-319">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="42f58-320">När du kör en container stöder nu Batch körningen av uppgiften i arbetskatalogen för containern eller i arbetskatalogen för Batch-uppgiften.</span><span class="sxs-lookup"><span data-stu-id="42f58-320">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="42f58-321">Detta styrs av egenskapen `WorkingDirectory` på `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="42f58-321">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="42f58-322">Lade till en funktion för att ange en samling av offentliga IP-adresser på `PSNetworkConfiguration` via den nya egenskapen `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="42f58-322">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="42f58-323">Detta garanterar att noderna i poolen har en IP-adress från listan över IP-adresser som tillhandahållits av användare.</span><span class="sxs-lookup"><span data-stu-id="42f58-323">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="42f58-324">Om inget värde anges är standardvärdet för `WaitForSuccess` på `PSSTartTask` nu `$True` (var tidigare `$False`).</span><span class="sxs-lookup"><span data-stu-id="42f58-324">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="42f58-325">Om inget värde anges är standardvärdet för `Scope` på `PSAutoUserSpecification` nu `Pool` (var tidigare `Task` på Windows och `Pool` på Linux).</span><span class="sxs-lookup"><span data-stu-id="42f58-325">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="42f58-326">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="42f58-326">Az.Cdn</span></span>
* <span data-ttu-id="42f58-327">Introducerade UrlRewriteAction och CacheKeyQueryStringAction till RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="42f58-327">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="42f58-328">Åtgärdade flera buggar, som saknade indata för ”väljare” i cmdleten New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="42f58-328">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="42f58-329">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="42f58-329">Az.Compute</span></span>
* <span data-ttu-id="42f58-330">Funktion för diskkrypteringsuppsättning</span><span class="sxs-lookup"><span data-stu-id="42f58-330">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="42f58-331">Nya cmdletar:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="42f58-331">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="42f58-332">Parametern DiskEncryptionSetId har lagts till i följande cmdletar: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="42f58-332">DiskEncryptionSetId parameter is added to the following cmdlets: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span></span>        
        <span data-ttu-id="42f58-333">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="42f58-333">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="42f58-334">Parametrarna DiskEncryptionSetId och EncryptionType har lagts till i följande cmdletar:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="42f58-334">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="42f58-335">Lägg till parametern PublicIPAddressVersion i New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="42f58-335">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="42f58-336">Flytta FileUris för anpassat skripttillägg från offentlig inställning till skyddad inställning</span><span class="sxs-lookup"><span data-stu-id="42f58-336">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="42f58-337">Lägg till ScaleInPolicy i cmdletarna New-AzVmss, New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="42f58-337">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="42f58-338">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="42f58-338">Breaking changes</span></span>
    - <span data-ttu-id="42f58-339">Parametern UploadSizeInBytes används istället för DiskSizeGB för New-AzDiskConfig när CreateOption är Uppladdning</span><span class="sxs-lookup"><span data-stu-id="42f58-339">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="42f58-340">PublishingProfile.Source.ManagedImage.Id ersätts med StorageProfile.Source.Id i objektet GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="42f58-340">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="42f58-341">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="42f58-341">Az.DataFactory</span></span>
* <span data-ttu-id="42f58-342">Uppdatera ADF .Net SDK-versionen till 4.3.0</span><span class="sxs-lookup"><span data-stu-id="42f58-342">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="42f58-343">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="42f58-343">Az.DataLakeStore</span></span>
* <span data-ttu-id="42f58-344">Uppdatera ADLS SDK-version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) innehåller följande korrigeringar</span><span class="sxs-lookup"><span data-stu-id="42f58-344">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="42f58-345">Undvik att utlösa undantag när det inte går att deserialisera creationtime för inmatning av papperskorg eller katalog.</span><span class="sxs-lookup"><span data-stu-id="42f58-345">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="42f58-346">Gör inställning tillgänglig per tidsgräns för förfrågan i adlsclient</span><span class="sxs-lookup"><span data-stu-id="42f58-346">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="42f58-347">Korrigera överföringen av ursprunglig syncflag för badoffset-återställning</span><span class="sxs-lookup"><span data-stu-id="42f58-347">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="42f58-348">Korrigera EnumerateDirectory för att hämta fortsättningstoken när svar har kontrollerats</span><span class="sxs-lookup"><span data-stu-id="42f58-348">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="42f58-349">Korrigera bugg i Concat</span><span class="sxs-lookup"><span data-stu-id="42f58-349">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="42f58-350">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="42f58-350">Az.FrontDoor</span></span>
* <span data-ttu-id="42f58-351">Åtgärdade diverse stavfel i modul</span><span class="sxs-lookup"><span data-stu-id="42f58-351">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="42f58-352">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="42f58-352">Az.HDInsight</span></span>
* <span data-ttu-id="42f58-353">Korrigerade buggen att kunder får felet ”inte en giltig Base-64-sträng” vid användning av Get-AzHDInsightCluster för att hämta klustret med ADLSGen1-lagring.</span><span class="sxs-lookup"><span data-stu-id="42f58-353">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="42f58-354">Lägg till en parameter med namnet ”ApplicationId” i de tre cmdletarna Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig och New-AzHDInsightCluster så att kunden kan tillhandahålla tjänstens huvudnamn för program-ID för åtkomst till Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="42f58-354">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="42f58-355">Ändrade Microsoft.Azure.Management.HDInsight från 2.1.0 till 5.1.0</span><span class="sxs-lookup"><span data-stu-id="42f58-355">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="42f58-356">Fem cmdletar har tagits bort:</span><span class="sxs-lookup"><span data-stu-id="42f58-356">Removed five cmdlets:</span></span>
    - <span data-ttu-id="42f58-357">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="42f58-357">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="42f58-358">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="42f58-358">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="42f58-359">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="42f58-359">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="42f58-360">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="42f58-360">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="42f58-361">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="42f58-361">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="42f58-362">Tre cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="42f58-362">Added three cmdlets:</span></span>
    - <span data-ttu-id="42f58-363">Get-AzHDInsightMonitoring som ersätter Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="42f58-363">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="42f58-364">Enable-AzHDInsightMonitoring som ersätter Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="42f58-364">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="42f58-365">Disable-AzHDInsightMonitoring som ersätter Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="42f58-365">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="42f58-366">Korrigerade cmdleten Get-AzHDInsightProperties för att stödja hämtning av funktionsinformation från en viss plats.</span><span class="sxs-lookup"><span data-stu-id="42f58-366">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="42f58-367">Parameteruppsättningarna (Spark1 och Spark2) har tagits bort från Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="42f58-367">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="42f58-368">Lägg till exempel för cmdleten Add-AzHDInsightSecurityProfile till hjälpdokumenten.</span><span class="sxs-lookup"><span data-stu-id="42f58-368">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="42f58-369">Ändrade utdatatyp för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="42f58-369">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="42f58-370">Ändrade utdatatyp för Get-AzHDInsightProperties från CapabilitiesResponse till AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="42f58-370">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="42f58-371">Ändrade utdatatyp för Remove-AzHDInsightCluster från ClusterGetResponse till bool.</span><span class="sxs-lookup"><span data-stu-id="42f58-371">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="42f58-372">Ändrade utdatatyp för Set-AzHDInsightGatewaySettings HttpConnectivitySettings till GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="42f58-372">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="42f58-373">Lade till testfall för vissa scenarier.</span><span class="sxs-lookup"><span data-stu-id="42f58-373">Added some scenario test cases.</span></span>
* <span data-ttu-id="42f58-374">Ta bort vissa alias: Add-AzHDInsightConfigValues, Get-AzHDInsightProperties.</span><span class="sxs-lookup"><span data-stu-id="42f58-374">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="42f58-375">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="42f58-375">Az.IotHub</span></span>
* <span data-ttu-id="42f58-376">Icke-bakåtkompatibla ändringar:</span><span class="sxs-lookup"><span data-stu-id="42f58-376">Breaking changes:</span></span>
    - <span data-ttu-id="42f58-377">Cmdleten Add-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="42f58-377">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="42f58-378">Parameteruppsättningen __AllParameterSets för cmdleten Add-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="42f58-378">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="42f58-379">Cmdleten Get-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="42f58-379">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="42f58-380">Parameteruppsättningen __AllParameterSets för cmdleten Get-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="42f58-380">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="42f58-381">Egenskapen OperationsMonitoringProperties av typen Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="42f58-381">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="42f58-382">Egenskapen OperationsMonitoringProperties av typen Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="42f58-382">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="42f58-383">Cmdleten New-AzIotHubExportDevice stöder inte längre aliaset New-AzIotHubExportDevices.</span><span class="sxs-lookup"><span data-stu-id="42f58-383">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="42f58-384">Cmdleten New-AzIotHubImportDevice stöder inte längre aliaset New-AzIotHubImportDevices.</span><span class="sxs-lookup"><span data-stu-id="42f58-384">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="42f58-385">Cmdleten Remove-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="42f58-385">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="42f58-386">Parameteruppsättningen __AllParameterSets för cmdleten Remove-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="42f58-386">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="42f58-387">Cmdleten Set-AzIotHub har inte längre stöd för parametern OperationsMonitoringProperties och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="42f58-387">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="42f58-388">Parameteruppsättningen UpdateOperationsMonitoringProperties för cmdleten Set-AzIotHub har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="42f58-388">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="42f58-389">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="42f58-389">Az.RecoveryServices</span></span>
* <span data-ttu-id="42f58-390">Azure Site Recovery-stöd för att konfigurera nätverksresurser som NSG, offentliga IP-adresser och interna lastbalanserare för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="42f58-390">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="42f58-391">Azure Site Recovery-stöd för att skriva till hanterad disk för vMWare till Azure.</span><span class="sxs-lookup"><span data-stu-id="42f58-391">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="42f58-392">Azure Site Recovery-stöd för NIC-reduktion för vMWare till Azure.</span><span class="sxs-lookup"><span data-stu-id="42f58-392">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="42f58-393">Azure Site Recovery-stöd för accelererat nätverk för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="42f58-393">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="42f58-394">Azure Site Recovery-stöd för automatisk uppdatering av agent för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="42f58-394">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="42f58-395">Azure Site Recovery-stöd för Standard SSD för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="42f58-395">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="42f58-396">Azure Site Recovery-stöd för tvåstegskryptering i Azure Disk Encryption för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="42f58-396">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="42f58-397">Azure Site Recovery-stöd för att skydda nyligen tillagda diskar för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="42f58-397">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="42f58-398">En funktion för mjuk borttagning av virtuella datorer samt tester för mjuk borttagning har tagits bort</span><span class="sxs-lookup"><span data-stu-id="42f58-398">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="42f58-399">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="42f58-399">Az.Resources</span></span>
* <span data-ttu-id="42f58-400">Uppdatera beroendesammansättning för Microsoft.Extensions.Caching.Memory från 1.1.1 till 2.2</span><span class="sxs-lookup"><span data-stu-id="42f58-400">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="42f58-401">Az.Network</span><span class="sxs-lookup"><span data-stu-id="42f58-401">Az.Network</span></span>
* <span data-ttu-id="42f58-402">Ändra alla cmdletar för PrivateEndpointConnection så att de stöder generiska tjänstleverantörer.</span><span class="sxs-lookup"><span data-stu-id="42f58-402">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="42f58-403">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="42f58-403">Updated cmdlet:</span></span>
        - <span data-ttu-id="42f58-404">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="42f58-404">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="42f58-405">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="42f58-405">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="42f58-406">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="42f58-406">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="42f58-407">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="42f58-407">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="42f58-408">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="42f58-408">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="42f58-409">Lägg till ny cmdlet för PrivateLinkResource så att det också stöder generiska tjänstleverantörer.</span><span class="sxs-lookup"><span data-stu-id="42f58-409">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="42f58-410">Ny cmdlet:</span><span class="sxs-lookup"><span data-stu-id="42f58-410">New cmdlet:</span></span>
        - <span data-ttu-id="42f58-411">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="42f58-411">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="42f58-412">Lägg till nya fält och parametrar för funktionen Proxy Protocol V2.</span><span class="sxs-lookup"><span data-stu-id="42f58-412">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="42f58-413">Lägg till egenskapen EnableProxyProtocol i PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="42f58-413">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="42f58-414">Lägg till egenskapen LinkIdentifier i PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="42f58-414">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="42f58-415">Uppdaterade New-AzPrivateLinkService för att lägga till den nya valfria parametern EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="42f58-415">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="42f58-416">Korrigera felaktig beskrivning av parameter i referensdokumentationen för New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="42f58-416">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="42f58-417">Nya cmdletar som stöder Azure-brandväggsprincipen</span><span class="sxs-lookup"><span data-stu-id="42f58-417">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="42f58-418">Lägg till stöd för den underordnade resursen RouteTables för VirtualHub</span><span class="sxs-lookup"><span data-stu-id="42f58-418">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="42f58-419">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="42f58-419">New cmdlets added:</span></span>
        - <span data-ttu-id="42f58-420">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="42f58-420">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="42f58-421">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="42f58-421">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="42f58-422">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="42f58-422">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="42f58-423">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="42f58-423">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="42f58-424">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="42f58-424">Set-AzVirtualHub</span></span>
* <span data-ttu-id="42f58-425">Lägg till stöd för ny egenskaps-SKU för VirtualHub och VirtualWANType för VirtualWan</span><span class="sxs-lookup"><span data-stu-id="42f58-425">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="42f58-426">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="42f58-426">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="42f58-427">New-AzVirtualHub: lade till parameter-SKU</span><span class="sxs-lookup"><span data-stu-id="42f58-427">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="42f58-428">Update-AzVirtualHub: lade till parameter-SKU</span><span class="sxs-lookup"><span data-stu-id="42f58-428">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="42f58-429">New-AzVirtualWan: lade till parametern VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="42f58-429">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="42f58-430">Update-AzVirtualWan: lade till parametern VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="42f58-430">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="42f58-431">Lägg till stöd för egenskapen EnableInternetSecurity för HubVnetConnection, VpnConnection och ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="42f58-431">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="42f58-432">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="42f58-432">New cmdlets added:</span></span>
        - <span data-ttu-id="42f58-433">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="42f58-433">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="42f58-434">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="42f58-434">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="42f58-435">New-AzureRmVirtualHubVnetConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="42f58-435">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="42f58-436">New-AzureRmVpnConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="42f58-436">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="42f58-437">Update-AzureRmVpnConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="42f58-437">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="42f58-438">New-AzureRmExpressRouteConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="42f58-438">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="42f58-439">Set-AzureRmExpressRouteConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="42f58-439">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="42f58-440">Lägg till stöd för att konfigurera TopLevel WebApplicationFirewall-princip</span><span class="sxs-lookup"><span data-stu-id="42f58-440">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="42f58-441">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="42f58-441">New cmdlets added:</span></span>
        - <span data-ttu-id="42f58-442">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="42f58-442">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="42f58-443">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="42f58-443">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="42f58-444">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="42f58-444">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="42f58-445">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="42f58-445">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="42f58-446">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="42f58-446">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="42f58-447">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="42f58-447">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="42f58-448">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="42f58-448">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="42f58-449">New-AzApplicationGatewayFirewallPolicy: parametrarna PolicySetting, ManagedRule har lagts till</span><span class="sxs-lookup"><span data-stu-id="42f58-449">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="42f58-450">Stöd för operator för geomatchning har lagts till på CustomRule</span><span class="sxs-lookup"><span data-stu-id="42f58-450">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="42f58-451">Geomatchning har lagts till i operatorn på FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="42f58-451">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="42f58-452">Stöd har lagts till för brandväggsprinciperna perListener och perSite</span><span class="sxs-lookup"><span data-stu-id="42f58-452">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="42f58-453">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="42f58-453">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="42f58-454">New-AzApplicationGatewayHttpListener: parametrarna FirewallPolicy, FirewallPolicyId har lagts till</span><span class="sxs-lookup"><span data-stu-id="42f58-454">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="42f58-455">New-AzApplicationGatewayPathRuleConfig: parametrarna FirewallPolicy, FirewallPolicyId har lagts till</span><span class="sxs-lookup"><span data-stu-id="42f58-455">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="42f58-456">Åtgärdat så att nödvändigt undernät med namnet AzureBastionSubnet i PSBastion kan vara skiftlägesokänsligt</span><span class="sxs-lookup"><span data-stu-id="42f58-456">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="42f58-457">Stöd för mål-FQDN:er i nätverksregler och översatt FQDN i NAT-regler för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="42f58-457">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="42f58-458">Lägg till stöd för resursen RouteTables för IpGroup på den högsta nivån</span><span class="sxs-lookup"><span data-stu-id="42f58-458">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="42f58-459">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="42f58-459">New cmdlets added:</span></span>
        - <span data-ttu-id="42f58-460">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="42f58-460">New-AzIpGroup</span></span>
        - <span data-ttu-id="42f58-461">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="42f58-461">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="42f58-462">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="42f58-462">Get-AzIpGroup</span></span>
        - <span data-ttu-id="42f58-463">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="42f58-463">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="42f58-464">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="42f58-464">Az.ServiceFabric</span></span>
* <span data-ttu-id="42f58-465">Ta bort cmdleten Add-AzServiceFabricApplicationCertificate eftersom det här scenariot omfattas av Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="42f58-465">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="42f58-466">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="42f58-466">Az.Sql</span></span>
* <span data-ttu-id="42f58-467">Stöd har lagts till för återställning av utelämnade databaser på hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="42f58-467">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="42f58-468">Inaktuella gamla cmdletar för granskning från kod.</span><span class="sxs-lookup"><span data-stu-id="42f58-468">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="42f58-469">Tog bort inaktuella alias:</span><span class="sxs-lookup"><span data-stu-id="42f58-469">Removed deprecated aliases:</span></span>
* <span data-ttu-id="42f58-470">Get-AzSqlDatabaseIndexRecommendations (använd Get-AzSqlDatabaseIndexRecommendation istället)</span><span class="sxs-lookup"><span data-stu-id="42f58-470">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="42f58-471">Get-AzSqlDatabaseRestorePoints (använd Get-AzSqlDatabaseRestorePoint istället)</span><span class="sxs-lookup"><span data-stu-id="42f58-471">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="42f58-472">Ta bort cmdleten Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="42f58-472">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="42f58-473">Ta bort alias för inaktuella cmdletar för inställningar för utvärdering av säkerhetsrisk</span><span class="sxs-lookup"><span data-stu-id="42f58-473">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="42f58-474">Inaktualisera cmdletar för inställningar för avancerad hotidentifiering</span><span class="sxs-lookup"><span data-stu-id="42f58-474">Deprecate Advanced Threat Detection Settings cmdlets</span></span> 
* <span data-ttu-id="42f58-475">Lägga till cmdletar för att inaktivera och aktivera känslighetsrekommendationer på kolumner i en databas.</span><span class="sxs-lookup"><span data-stu-id="42f58-475">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="42f58-476">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="42f58-476">Az.Storage</span></span>
* <span data-ttu-id="42f58-477">Stöd för att aktivera stora filresurser vid skapande eller uppdatering av lagringskonto</span><span class="sxs-lookup"><span data-stu-id="42f58-477">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="42f58-478">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="42f58-478">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="42f58-479">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="42f58-479">Set-AzStorageAccount</span></span>
* <span data-ttu-id="42f58-480">När du stänger/hämtar en filreferens kan du hoppa över kontrollen av huruvida indatasökvägen är en filkatalog eller en fil för att undvika problem med objekt som har status DeletePending</span><span class="sxs-lookup"><span data-stu-id="42f58-480">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="42f58-481">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="42f58-481">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="42f58-482">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="42f58-482">Close-AzStorageFileHandle</span></span>
    
## <a name="280---october-2019"></a><span data-ttu-id="42f58-483">2.8.0 – oktober 2019</span><span class="sxs-lookup"><span data-stu-id="42f58-483">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="42f58-484">Allmänt</span><span class="sxs-lookup"><span data-stu-id="42f58-484">General</span></span>
* <span data-ttu-id="42f58-485">AZ. HealthcareApis 1.0.0-version</span><span class="sxs-lookup"><span data-stu-id="42f58-485">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="42f58-486">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="42f58-486">Az.Accounts</span></span>
* <span data-ttu-id="42f58-487">Uppdatera telemetri och URL-omskrivning för genererade moduler, korrigera Windows-enhetstester.</span><span class="sxs-lookup"><span data-stu-id="42f58-487">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="42f58-488">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="42f58-488">Az.ApiManagement</span></span>
* <span data-ttu-id="42f58-489">**Set-AzApiManagementApi** – Tillagt stöd för att uppdatera Api till ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="42f58-489">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="42f58-490">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="42f58-490">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="42f58-491">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="42f58-491">Az.Automation</span></span>
* <span data-ttu-id="42f58-492">Åtgärdade cmdleten New-AzureAutomationSoftwareUpdateConfiguration för parametern för inställning av Linux-omstart.</span><span class="sxs-lookup"><span data-stu-id="42f58-492">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="42f58-493">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="42f58-493">Az.Batch</span></span>
* <span data-ttu-id="42f58-494">**Get-AzBatchNodeAgentSku** är inaktuell och ersätts av **Get-AzBatchSupportImage** i version 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="42f58-494">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="42f58-495">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="42f58-495">Az.Compute</span></span>
* <span data-ttu-id="42f58-496">Lägg till parametrarna Priority, EvictionPolicy och MaxPrice till cmdletarna New-AzVM och New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="42f58-496">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="42f58-497">Korrigera varningsmeddelande och hjälpdokument för cmdletarna Add-AzVMAdditionalUnattendContent och Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="42f58-497">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="42f58-498">Åtgärda – skipVmBackup-undantag för virtuella Linux-datorer med hanterade diskar för Set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="42f58-498">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="42f58-499">Åtgärda fel i uppdatera krypteringsinställningarna i set-AzVMDiskEncryptionExtension, scenario i två steg.</span><span class="sxs-lookup"><span data-stu-id="42f58-499">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="42f58-500">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="42f58-500">Az.DataFactory</span></span>
* <span data-ttu-id="42f58-501">Lägga till CRUD-kommandon för ADF V2-dataflödet: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow och Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="42f58-501">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="42f58-502">Lägger till åtgärdskommandon för ADF V2-dataflödesfelsökningssession: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand och Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="42f58-502">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="42f58-503">Uppdatera ADF .Net SDK-versionen till 4.2.0</span><span class="sxs-lookup"><span data-stu-id="42f58-503">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="42f58-504">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="42f58-504">Az.DataLakeStore</span></span>
* <span data-ttu-id="42f58-505">Korrigera kontovalidering så att konton med ”-” kan skickas utan domän</span><span class="sxs-lookup"><span data-stu-id="42f58-505">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="42f58-506">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="42f58-506">Az.HealthcareApis</span></span>
* <span data-ttu-id="42f58-507">PowerShell-versionen har uppdaterats till 1.0.0</span><span class="sxs-lookup"><span data-stu-id="42f58-507">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="42f58-508">Uppdaterade SDK-versionen till 1.0.2</span><span class="sxs-lookup"><span data-stu-id="42f58-508">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="42f58-509">Uppdatera i tester för att referera till en ny SDK-version</span><span class="sxs-lookup"><span data-stu-id="42f58-509">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="42f58-510">Utdatastrukturen har uppdaterats från kapslad till förenklad.</span><span class="sxs-lookup"><span data-stu-id="42f58-510">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="42f58-511">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="42f58-511">Az.IotHub</span></span>
* <span data-ttu-id="42f58-512">Lägg till ny routningskälla: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="42f58-512">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="42f58-513">Mindre felkorrigering: Get-AzIothub returnerar inte subscriptionId</span><span class="sxs-lookup"><span data-stu-id="42f58-513">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="42f58-514">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="42f58-514">Az.Monitor</span></span>
* <span data-ttu-id="42f58-515">Nya åtgärdsgruppsmottagare har lagts till för åtgärdsgrupp   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="42f58-515">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="42f58-516">Använd vanligt aviseringsschema som är aktiverat för mottagarna.</span><span class="sxs-lookup"><span data-stu-id="42f58-516">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="42f58-517">Detta gäller inte för SMS, push för Azure-app, ITSM och röstmottagare</span><span class="sxs-lookup"><span data-stu-id="42f58-517">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="42f58-518">Webhooks har nu stöd för Azure Active Directory-autentisering.</span><span class="sxs-lookup"><span data-stu-id="42f58-518">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="42f58-519">Az.Network</span><span class="sxs-lookup"><span data-stu-id="42f58-519">Az.Network</span></span>
* <span data-ttu-id="42f58-520">Lägg till ny cmdlet Get-AzAvailableServiceAlias som kan anropas för att hämta de alias som kan användas för tjänstslutpunktsprinciper.</span><span class="sxs-lookup"><span data-stu-id="42f58-520">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="42f58-521">Stöd för tillägg av trafikväljare har lagts till i gatewayanslutningar för virtuella nätverk</span><span class="sxs-lookup"><span data-stu-id="42f58-521">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="42f58-522">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="42f58-522">New cmdlets added:</span></span>
        - <span data-ttu-id="42f58-523">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="42f58-523">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="42f58-524">Cmdletar har uppdaterats med valfri parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="42f58-524">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="42f58-525">Lägg till stöd för ESP- och AH-protokoll i konfiguration av nätverkssäkerhetsregler</span><span class="sxs-lookup"><span data-stu-id="42f58-525">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="42f58-526">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="42f58-526">Updated cmdlets:</span></span>
        - <span data-ttu-id="42f58-527">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="42f58-527">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="42f58-528">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="42f58-528">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="42f58-529">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="42f58-529">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="42f58-530">Förbättra hanteringen av undantag i Cortex-cmdletar</span><span class="sxs-lookup"><span data-stu-id="42f58-530">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="42f58-531">Nya generationer och SKU:er för VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="42f58-531">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="42f58-532">Introducera nya generationer för VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="42f58-532">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="42f58-533">Introducera nya SKU:er med högt dataflöde för VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="42f58-533">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="42f58-534">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="42f58-534">Az.RedisCache</span></span>
* <span data-ttu-id="42f58-535">Uppdaterad referensdokumentation för ”set-AzRedisCache” för att inkludera saknade värden för parametern ”size”</span><span class="sxs-lookup"><span data-stu-id="42f58-535">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="42f58-536">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="42f58-536">Az.Sql</span></span>
* <span data-ttu-id="42f58-537">Lägg till stöd för inställningen Active Directory administratör på den hanterade instansen</span><span class="sxs-lookup"><span data-stu-id="42f58-537">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="42f58-538">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="42f58-538">Az.Storage</span></span>
* <span data-ttu-id="42f58-539">Uppdatera Lagringsklientbibliotek till 11.1.0</span><span class="sxs-lookup"><span data-stu-id="42f58-539">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="42f58-540">Lista containrar med hanteringsplans-API, kommer att listas med NextPageLink</span><span class="sxs-lookup"><span data-stu-id="42f58-540">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="42f58-541">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="42f58-541">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="42f58-542">Lista lagringskonton från prenumerationen, kommer att listas med NextPageLink</span><span class="sxs-lookup"><span data-stu-id="42f58-542">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="42f58-543">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="42f58-543">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="42f58-544">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="42f58-544">Az.StorageSync</span></span>
* <span data-ttu-id="42f58-545">Åtgärda problemet 9810 i Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="42f58-545">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="42f58-546">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="42f58-546">Az.Websites</span></span>
* <span data-ttu-id="42f58-547">Set-AzWebApp – uppdatering av ASP för en app misslyckades</span><span class="sxs-lookup"><span data-stu-id="42f58-547">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="42f58-548">2.7.0 – september 2019</span><span class="sxs-lookup"><span data-stu-id="42f58-548">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="42f58-549">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="42f58-549">Az.ApiManagement</span></span>
* <span data-ttu-id="42f58-550">Uppdatera ”-Format”-parameterbeskrivningen i ”Set-AzApiManagementPolicy”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="42f58-550">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="42f58-551">Referenser för den föråldrade cmdleten ”Update-AzApiManagementDeployment” har tagits bort från referensdokumentationen.</span><span class="sxs-lookup"><span data-stu-id="42f58-551">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="42f58-552">Använd ”Set-AzApiManagement” i stället.</span><span class="sxs-lookup"><span data-stu-id="42f58-552">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="42f58-553">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="42f58-553">Az.Automation</span></span>
* <span data-ttu-id="42f58-554">Stavfel har korrigerats i exempel i referensdokumentationen för ”Register-AzAutomationDscNode”</span><span class="sxs-lookup"><span data-stu-id="42f58-554">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="42f58-555">Klargörande har lagts till om OS-begränsningar för Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="42f58-555">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="42f58-556">Null-referensundantag har korrigerats för -Wait-alternativet i Start-AzAutomationRunbook-cmdleten.</span><span class="sxs-lookup"><span data-stu-id="42f58-556">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="42f58-557">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="42f58-557">Az.Compute</span></span>
* <span data-ttu-id="42f58-558">Lägg till UploadSizeInBytes-parameter till New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="42f58-558">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="42f58-559">Lägg till Incremental-parameter till New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="42f58-559">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="42f58-560">Lägg till en funktion för virtuella datorer med låg prioritet:</span><span class="sxs-lookup"><span data-stu-id="42f58-560">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="42f58-561">MaxPrice-, EvictionPolicy- och Priority-parametrar har lagts till i New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="42f58-561">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="42f58-562">MaxPrice-parametern har lagts till i New-AzVmssConfig-, Update-AzVM- och Update-AzVmss-cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="42f58-562">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="42f58-563">Åtgärda problem med VM-referenser för Get-AzAvailabilitySet-cmdleten när alla tillgänglighetsuppsättningar i prenumerationen visas.</span><span class="sxs-lookup"><span data-stu-id="42f58-563">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="42f58-564">Korrigera null-undantaget för Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="42f58-564">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="42f58-565">Korrigera VHD-metoden för sökning relativt till slut.</span><span class="sxs-lookup"><span data-stu-id="42f58-565">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="42f58-566">Åtgärda UltraSSD-problem för New-AzVM och Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="42f58-566">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="42f58-567">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="42f58-567">Az.DataFactory</span></span>
* <span data-ttu-id="42f58-568">Lägger till 3 nya kommandon för ADF V2 – Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription och Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="42f58-568">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="42f58-569">ADF .Net SDK har uppdaterats till 4.1.3</span><span class="sxs-lookup"><span data-stu-id="42f58-569">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="42f58-570">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="42f58-570">Az.HDInsight</span></span>
* <span data-ttu-id="42f58-571">Anrop för icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="42f58-571">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="42f58-572">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="42f58-572">Az.IotHub</span></span>
* <span data-ttu-id="42f58-573">Lägg till stöd för att anropa redundans för en IotHub till den geo-länkade katastrofåterställningsregionen.</span><span class="sxs-lookup"><span data-stu-id="42f58-573">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="42f58-574">Lägg till stöd för att hantera meddelandeberikning för en IotHub.</span><span class="sxs-lookup"><span data-stu-id="42f58-574">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="42f58-575">Nya cmdlet:ar är:</span><span class="sxs-lookup"><span data-stu-id="42f58-575">New cmdlets are:</span></span>
    - <span data-ttu-id="42f58-576">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="42f58-576">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="42f58-577">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="42f58-577">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="42f58-578">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="42f58-578">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="42f58-579">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="42f58-579">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="42f58-580">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="42f58-580">Az.Monitor</span></span>
* <span data-ttu-id="42f58-581">Pekar på den senaste Monitor SDK:n, dvs. 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="42f58-581">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="42f58-582">Lägger till bakåtkompatibla ändringar i Metrics-cmdletarna, dvs. enhetsuppräkningen stöder flera nya värden.</span><span class="sxs-lookup"><span data-stu-id="42f58-582">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="42f58-583">Detta är skrivskyddade cmdletar, så det förekommer inga ändringar i inmatningen för cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="42f58-583">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="42f58-584">API-versionen för **ActionGroups**-begäranden är nu **2019-06-01**. Tidigare var den **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="42f58-584">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="42f58-585">Test av scenarier har uppdaterats för att anpassas till den här ändringen.</span><span class="sxs-lookup"><span data-stu-id="42f58-585">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="42f58-586">Ett nytt obligatoriskt argument har lagts till för konstruktorerna för klasserna **EmailReceiver** och **WebhookReceiver** – ett booleskt värde med namnet **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="42f58-586">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="42f58-587">Värdet är för närvarande fast till **false** så att den här icke-bakåtkompatibla ändringen är dold från cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="42f58-587">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="42f58-588">**Obs!** Det här är en tillfällig ändring som måste verifieras av Alerts-teamet.</span><span class="sxs-lookup"><span data-stu-id="42f58-588">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="42f58-589">Ordningen på argumenten för konstruktorn för klassen **Source** (relaterad till klassen **ScheduledQueryRuleSource**) har ändrats från den tidigare SDK:n.</span><span class="sxs-lookup"><span data-stu-id="42f58-589">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="42f58-590">Den här ändringen krävde korrigering av två enhetstest: de kompilerades, men testerna skickades inte.</span><span class="sxs-lookup"><span data-stu-id="42f58-590">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="42f58-591">Ordningen på argumenten för konstruktorn för klassen **AlertingAction** (relaterad till klassen **ScheduledQueryRuleSource**) har ändrats från den tidigare SDK:n.</span><span class="sxs-lookup"><span data-stu-id="42f58-591">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="42f58-592">Den här ändringen krävde korrigering av två enhetstest: de kompilerades, men testerna skickades inte.</span><span class="sxs-lookup"><span data-stu-id="42f58-592">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="42f58-593">Stöd för kriterier för dynamiskt tröskelvärde för måttavisering v2</span><span class="sxs-lookup"><span data-stu-id="42f58-593">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="42f58-594">New-AzMetricAlertRuleV2Criteria: skapar nu även kriterier för dynamiskt tröskelvärde</span><span class="sxs-lookup"><span data-stu-id="42f58-594">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="42f58-595">Add-AzMetricAlertRuleV2: accepterar nu även kriterier för dynamiskt tröskelvärde</span><span class="sxs-lookup"><span data-stu-id="42f58-595">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="42f58-596">Förbättringar i schemalagd frågeregel (SQR)</span><span class="sxs-lookup"><span data-stu-id="42f58-596">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="42f58-597">Cmdletar accepterar ”Location”-parameter i båda formaten, antingen platsen (t.ex. eastus) eller platsens visningsnamn (t.ex. USA, östra)</span><span class="sxs-lookup"><span data-stu-id="42f58-597">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="42f58-598">”Enabled”-parametern illustreras korrekt i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="42f58-598">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="42f58-599">Exempel för den valfria parametern ”ActionGroup” har lagts till</span><span class="sxs-lookup"><span data-stu-id="42f58-599">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="42f58-600">Förbättrade hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="42f58-600">Overall improved help files</span></span>
* <span data-ttu-id="42f58-601">Åtgärda bugg då omfattningstypen fastställs för ”Set-AzActionRule”</span><span class="sxs-lookup"><span data-stu-id="42f58-601">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="42f58-602">Az.Network</span><span class="sxs-lookup"><span data-stu-id="42f58-602">Az.Network</span></span>
* <span data-ttu-id="42f58-603">Korrigera felaktigt exempel i referensdokumentationen för ”New-AzApplicationGateway”</span><span class="sxs-lookup"><span data-stu-id="42f58-603">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="42f58-604">Lägg till anmärkning i ”Get-AzNetworkWatcherPacketCapture”-referensdokumentationen om hämtning av alla egenskaper för en paketinsamling</span><span class="sxs-lookup"><span data-stu-id="42f58-604">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="42f58-605">Exempel har korrigerats i ”Test-AzNetworkWatcherIPFlow”-referensdokumentationen för korrekt uppräkning av nätverkskort</span><span class="sxs-lookup"><span data-stu-id="42f58-605">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="42f58-606">Förbättrad tolkning av molnundantag för att visa eventuell ytterligare information</span><span class="sxs-lookup"><span data-stu-id="42f58-606">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="42f58-607">Förbättrad tolkning av molnundantag för att hantera ytterligare en typ av SDK-undantag</span><span class="sxs-lookup"><span data-stu-id="42f58-607">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="42f58-608">Felaktig mappning av säkerhetsregelmodeller har korrigerats</span><span class="sxs-lookup"><span data-stu-id="42f58-608">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="42f58-609">Egenskaper har lagts till för nätverksgränssnittet för funktionen Privat IP</span><span class="sxs-lookup"><span data-stu-id="42f58-609">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="42f58-610">Egenskapen ”PrivateEndpoint” har lagts till som en typ av PSResourceId till PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="42f58-610">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="42f58-611">Egenskapen ”PrivateLinkConnectionProperties” har lagts till som en typ av PSIpConfigurationConnectivityInformation till PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="42f58-611">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="42f58-612">Modellklassen PSIpConfigurationConnectivityInformation har lagts till</span><span class="sxs-lookup"><span data-stu-id="42f58-612">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="42f58-613">ApplicationRuleProtocolType ”mssql” har lagts till för Azure Firewall-resurs</span><span class="sxs-lookup"><span data-stu-id="42f58-613">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="42f58-614">MultiLink-stöd i virtuellt WAN</span><span class="sxs-lookup"><span data-stu-id="42f58-614">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="42f58-615">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="42f58-615">New cmdlets</span></span>
        - <span data-ttu-id="42f58-616">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="42f58-616">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="42f58-617">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="42f58-617">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="42f58-618">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="42f58-618">Updated cmdlet:</span></span>
        - <span data-ttu-id="42f58-619">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="42f58-619">New-VpnSite</span></span>
        - <span data-ttu-id="42f58-620">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="42f58-620">Update-VpnSite</span></span>
        - <span data-ttu-id="42f58-621">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="42f58-621">New-VpnConnection</span></span>
        - <span data-ttu-id="42f58-622">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="42f58-622">Update-VpnConnection</span></span>
* <span data-ttu-id="42f58-623">Dokument för vissa PowerShell-exempel har korrigerats så att Az-cmdletar används i stället för AzureRM-cmdletar</span><span class="sxs-lookup"><span data-stu-id="42f58-623">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="42f58-624">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="42f58-624">Az.RecoveryServices</span></span>
* <span data-ttu-id="42f58-625">Uppdatera AzureVMpolicy-objekt med ProtectedItemsCount-attribut</span><span class="sxs-lookup"><span data-stu-id="42f58-625">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="42f58-626">Ytterligare tester har lagts till för VM-princip och återställning av ursprungligt lagringskonto</span><span class="sxs-lookup"><span data-stu-id="42f58-626">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="42f58-627">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="42f58-627">Az.Resources</span></span>
* <span data-ttu-id="42f58-628">Åtgärda fel där det inte gick att anropa New-AzRoleAssignment utan parametern Scope.</span><span class="sxs-lookup"><span data-stu-id="42f58-628">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="42f58-629">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="42f58-629">Az.ServiceFabric</span></span>
* <span data-ttu-id="42f58-630">Stavfel har korrigerats i exempel för ”Update-AzServiceFabricReliability”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="42f58-630">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="42f58-631">Lägger till nya cmdletar för att hantera program och tjänster:</span><span class="sxs-lookup"><span data-stu-id="42f58-631">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="42f58-632">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="42f58-632">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="42f58-633">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="42f58-633">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="42f58-634">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="42f58-634">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="42f58-635">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="42f58-635">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="42f58-636">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="42f58-636">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="42f58-637">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="42f58-637">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="42f58-638">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="42f58-638">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="42f58-639">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="42f58-639">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="42f58-640">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="42f58-640">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="42f58-641">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="42f58-641">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="42f58-642">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="42f58-642">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="42f58-643">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="42f58-643">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="42f58-644">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="42f58-644">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="42f58-645">Service Fabric SDK har uppgraderats till version 1.2.0 som använder Service Fabric-resursprovidern med API-version 2019-03-01.</span><span class="sxs-lookup"><span data-stu-id="42f58-645">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="42f58-646">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="42f58-646">Az.SignalR</span></span>
* <span data-ttu-id="42f58-647">Lägg till Update-, Restart-, CheckNameAvailability- och GetUsage-cmdletar</span><span class="sxs-lookup"><span data-stu-id="42f58-647">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="42f58-648">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="42f58-648">Az.Sql</span></span>
* <span data-ttu-id="42f58-649">Uppdatera exempel i referensdokumentationen för ”Get-AzSqlElasticPool”</span><span class="sxs-lookup"><span data-stu-id="42f58-649">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="42f58-650">vCore-exempel för att skapa en elastisk pool (New-AzSqlElasticPool) har lagts till.</span><span class="sxs-lookup"><span data-stu-id="42f58-650">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="42f58-651">Ta bort verifieringen av EmailAddresses och kontrollen som bekräftar att EmailAdmins inte är falskt när EmailAddresses är tomt i Set-AzSqlServerAdvancedThreatProtectionPolicy och Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="42f58-651">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="42f58-652">Server-/databasgranskningsinställningar kan tas bort när det finns flera diagnostikinställningar som aktiverar granskningskategorin.</span><span class="sxs-lookup"><span data-stu-id="42f58-652">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="42f58-653">Åtgärda verifiering av e-postadresser i flera Sql Vulnerability Assessment-cmdletar (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting och Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="42f58-653">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="42f58-654">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="42f58-654">Az.Storage</span></span>
* <span data-ttu-id="42f58-655">Exempel i referensdokumentationen för ”Get-AzStorageAccountKey” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="42f58-655">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="42f58-656">Vid upp- och nedladdning av en Azure-fil kan SMB-egenskaperna för källfilen (t.ex. filattribut, tidpunkten då filen skapades och tidpunkten för den senaste skrivningen) sparas i målfilen</span><span class="sxs-lookup"><span data-stu-id="42f58-656">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="42f58-657">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="42f58-657">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="42f58-658">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="42f58-658">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="42f58-659">Korrigera problem med uppladdningen av blockblob med egenskaper/metadata för ImmutabilityPolicy i containrar.</span><span class="sxs-lookup"><span data-stu-id="42f58-659">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="42f58-660">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="42f58-660">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="42f58-661">Stöd för hantering av Azure-filresurser med API för hanteringsplan</span><span class="sxs-lookup"><span data-stu-id="42f58-661">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="42f58-662">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="42f58-662">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="42f58-663">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="42f58-663">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="42f58-664">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="42f58-664">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="42f58-665">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="42f58-665">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="42f58-666">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="42f58-666">Az.Websites</span></span>
* <span data-ttu-id="42f58-667">Åtgärdar problemet där webapp-taggar togs bort när appen migrerades till nya ASP</span><span class="sxs-lookup"><span data-stu-id="42f58-667">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="42f58-668">Åtgärda Publish-AzureWebapp så att det fungerar i Linux och Windows</span><span class="sxs-lookup"><span data-stu-id="42f58-668">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="42f58-669">Uppdatera exempel i ”Get-AzWebAppPublishingProfile”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="42f58-669">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="42f58-670">2.6.0 – augusti 2019</span><span class="sxs-lookup"><span data-stu-id="42f58-670">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="42f58-671">Allmänt</span><span class="sxs-lookup"><span data-stu-id="42f58-671">General</span></span>
* <span data-ttu-id="42f58-672">Åtgärdade diverse skrivfel i flera moduler</span><span class="sxs-lookup"><span data-stu-id="42f58-672">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="42f58-673">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="42f58-673">Az.Accounts</span></span>
* <span data-ttu-id="42f58-674">Stöd för användartilldelat MSI i Azure Functions-autentisering (#9479)</span><span class="sxs-lookup"><span data-stu-id="42f58-674">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="42f58-675">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="42f58-675">Az.Aks</span></span>
* <span data-ttu-id="42f58-676">Åtgärda problem med utdata för "Get-AzAks"</span><span class="sxs-lookup"><span data-stu-id="42f58-676">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="42f58-677">Mer information här: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="42f58-677">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="42f58-678">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="42f58-678">Az.ApiManagement</span></span>
* <span data-ttu-id="42f58-679">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="42f58-679">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="42f58-680">Uppdatera .net-NuGet-versionen, som inte tillämpar begränsningar för productId, apiId och userId</span><span class="sxs-lookup"><span data-stu-id="42f58-680">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="42f58-681">**Get-AzApiManagementProduct** – Lade till stöd för frågekörning mot produkter via API.</span><span class="sxs-lookup"><span data-stu-id="42f58-681">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="42f58-682">**New-AzApiManagementApiRevision** – Korrigering för problem där ApiRevisionDescription inte angavs vid skapande av ny API-revision https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="42f58-682">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="42f58-683">Åtgärdade skrivfel i modellen "PsApiManagementOAuth2AuthrozationServer" till "PsApiManagementOAuth2AuthorizationServer"</span><span class="sxs-lookup"><span data-stu-id="42f58-683">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="42f58-684">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="42f58-684">Az.Batch</span></span>
* <span data-ttu-id="42f58-685">Åtgärdade skrivfel i hjälpmeddelande och dokumentation till att skriva Windows med versaler</span><span class="sxs-lookup"><span data-stu-id="42f58-685">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="42f58-686">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="42f58-686">Az.Cdn</span></span>
* <span data-ttu-id="42f58-687">Åtgärdade skrivfel i CDN-modulens konverteringshjälp</span><span class="sxs-lookup"><span data-stu-id="42f58-687">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="42f58-688">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="42f58-688">Az.Compute</span></span>
* <span data-ttu-id="42f58-689">Lägg till VmssId i New-AzVMConfig-cmdleten</span><span class="sxs-lookup"><span data-stu-id="42f58-689">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="42f58-690">Lägg till parametrarna TerminateScheduledEvents och TerminateScheduledEventNotBeforeTimeoutInMinutes i New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="42f58-690">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="42f58-691">Lägg till egenskapen HyperVGeneration till avbildningsobjekt för virtuell dator</span><span class="sxs-lookup"><span data-stu-id="42f58-691">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="42f58-692">Lägg till funktioner för Host och HostGroup</span><span class="sxs-lookup"><span data-stu-id="42f58-692">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="42f58-693">Nya cmdletar:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="42f58-693">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="42f58-694">HostId-parametern läggs till i New-AzVMConfig och New-AzVM</span><span class="sxs-lookup"><span data-stu-id="42f58-694">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="42f58-695">Uppdatera exempel i "Invoke-AzVMRunCommand"-dokumentationen till att använda rätt parameternamn</span><span class="sxs-lookup"><span data-stu-id="42f58-695">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="42f58-696">Uppdatera "-VolumeType"-beskrivningen i referensdokumentationen för "set-AzVMDiskEncryptionExtension" och "set-AzVmssDiskEncryptionExtension"</span><span class="sxs-lookup"><span data-stu-id="42f58-696">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="42f58-697">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="42f58-697">Az.DataFactory</span></span>
* <span data-ttu-id="42f58-698">Åtgärda skrivfel till att använda versaler för "Windows" i "New-AzDataFactoryEncryptValue"-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="42f58-698">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="42f58-699">Uppdaterade ADF .Net SDK-versionen till 4.1.2</span><span class="sxs-lookup"><span data-stu-id="42f58-699">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="42f58-700">Lägg till parametrarna "DataProxyIntegrationRuntimeName", "DataProxyStagingLinkedServiceName" och "DataProxyStagingPath" för "Set-AzureRmDataFactoryV2IntegrationRuntime"-cmd för att aktivera konfiguration av lokalt installerad integrationskörning som en proxy för SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="42f58-700">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="42f58-701">Uppdaterade PSTriggerRun till att visa utlöst pipeline, meddelande och egenskaper samt PSActivityRun till att visa aktivitetstypen</span><span class="sxs-lookup"><span data-stu-id="42f58-701">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="42f58-702">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="42f58-702">Az.DataLakeStore</span></span>
* <span data-ttu-id="42f58-703">Korrigering av frysning av Get-DataLakeStoreDeletedItem för fel eller fjärrundantag.</span><span class="sxs-lookup"><span data-stu-id="42f58-703">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="42f58-704">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="42f58-704">Az.EventHub</span></span>
* <span data-ttu-id="42f58-705">Korrigering av problem #9658 : Skrivfel i parametern VirtualNteworkRule i Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="42f58-705">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="42f58-706">Korrigering av problem #9558 : Set-AzEventHubNamespace använder PATCH i stället för PUT</span><span class="sxs-lookup"><span data-stu-id="42f58-706">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="42f58-707">lade till parametern EnableKafka i Set-AzEventHubNamespace-cmdleten</span><span class="sxs-lookup"><span data-stu-id="42f58-707">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="42f58-708">Korrigering av problem #9786 : kan inte skapa en regel med Endast lyssna-behörighet</span><span class="sxs-lookup"><span data-stu-id="42f58-708">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="42f58-709">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="42f58-709">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="42f58-710">Åtgärdade skrivfel i dokumentation där "Azure" skrevs helt med gemener</span><span class="sxs-lookup"><span data-stu-id="42f58-710">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="42f58-711">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="42f58-711">Az.Monitor</span></span>
* <span data-ttu-id="42f58-712">Åtgärdade felaktigt parameternamn i hjälpdokumentationen</span><span class="sxs-lookup"><span data-stu-id="42f58-712">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="42f58-713">Az.Network</span><span class="sxs-lookup"><span data-stu-id="42f58-713">Az.Network</span></span>
* <span data-ttu-id="42f58-714">Uppdaterade New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="42f58-714">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="42f58-715">Gjorde parametern "PublicIpAddress" inaktuell eftersom den aldrig används på serversidan.</span><span class="sxs-lookup"><span data-stu-id="42f58-715">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="42f58-716">Lade till den valfria parametern "Primary", som anger huruvida den aktuella IP-konfigurationen är den primära.</span><span class="sxs-lookup"><span data-stu-id="42f58-716">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="42f58-717">Förbättrade hanteringen av felundantag för begärande från SDK – åtgärdar problemet att tidigare SDK-undantag inte hanteras på rätt sätt, vilket leder till att viktig felinformation inte visas</span><span class="sxs-lookup"><span data-stu-id="42f58-717">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="42f58-718">Justerade valideringslogiken för IPv6-IP-prefix till att kontrollera korrekt IPv6-prefixlängd.</span><span class="sxs-lookup"><span data-stu-id="42f58-718">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="42f58-719">Uppdaterade Get-AzVirtualNetworkSubnetConfig: Lade till parameter som anges till get av undernätets resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="42f58-719">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="42f58-720">Uppdaterade beskrivningen av parametern Location för AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="42f58-720">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="42f58-721">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="42f58-721">Az.OperationalInsights</span></span>
* <span data-ttu-id="42f58-722">Uppdaterade dokumentation för "New-AzOperationalInsightsLinuxSyslogDataSource"</span><span class="sxs-lookup"><span data-stu-id="42f58-722">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="42f58-723">Lade till exempel</span><span class="sxs-lookup"><span data-stu-id="42f58-723">Added example</span></span>
    - <span data-ttu-id="42f58-724">Uppdaterade beskrivningen av parametern "-Name"</span><span class="sxs-lookup"><span data-stu-id="42f58-724">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="42f58-725">Lade till ett exempel för New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="42f58-725">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="42f58-726">Ändrade beskrivningen av parametern -Name för New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="42f58-726">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="42f58-727">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="42f58-727">Az.RecoveryServices</span></span>
* <span data-ttu-id="42f58-728">Uppdatera "Get-AzRecoveryServicesBackupJobDetail.md"</span><span class="sxs-lookup"><span data-stu-id="42f58-728">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="42f58-729">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="42f58-729">Az.Resources</span></span>
* <span data-ttu-id="42f58-730">Lägg till stöd för den nya API-versionen från 2019-05-10 för Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="42f58-730">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="42f58-731">Lägg till stöd för "copy.count = 0" för variabler, resurser och egenskaper</span><span class="sxs-lookup"><span data-stu-id="42f58-731">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="42f58-732">Resurser med "condition = false" eller "copy.count = 0" tas bort i complete-läget</span><span class="sxs-lookup"><span data-stu-id="42f58-732">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="42f58-733">Lägg till ett exempel på tilldelning av princip på prenumerationsnivå i hjälpdokumentationen</span><span class="sxs-lookup"><span data-stu-id="42f58-733">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="42f58-734">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="42f58-734">Az.ServiceBus</span></span>
* <span data-ttu-id="42f58-735">Korrigering av problem #9658 : Skrivfel i parametern VirtualNetworkRule i set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="42f58-735">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="42f58-736">Korrigering av problem #9786 : kan inte skapa en regel med Endast lyssna-behörighet</span><span class="sxs-lookup"><span data-stu-id="42f58-736">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="42f58-737">Lade till det nya kommandot "Test-AzServiceBusNameAvailability" för att kontrollera namntillgängligheten för kö och ämne</span><span class="sxs-lookup"><span data-stu-id="42f58-737">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="42f58-738">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="42f58-738">Az.ServiceFabric</span></span>
* <span data-ttu-id="42f58-739">Åtgärda buggar med tillägg av nodtyps-cmdlet:</span><span class="sxs-lookup"><span data-stu-id="42f58-739">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="42f58-740">NullReferenceException-bugg när resursgrupp hade annan vmss som inte är relaterad till Service Fabric-klustret.</span><span class="sxs-lookup"><span data-stu-id="42f58-740">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="42f58-741">Åtgärdar problemet: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="42f58-741">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="42f58-742">Åtgärda bugg där cmdleten misslyckades om virtualNetwork var i en annan resursgrupp än klustret.</span><span class="sxs-lookup"><span data-stu-id="42f58-742">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="42f58-743">Åtgärdar problemet: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="42f58-743">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="42f58-744">AzServiceFabricApplicationCertificate-cmdleten görs inaktuell</span><span class="sxs-lookup"><span data-stu-id="42f58-744">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="42f58-745">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="42f58-745">Az.Sql</span></span>
* <span data-ttu-id="42f58-746">Uppdatera dokumentation om gamla gransknings-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="42f58-746">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="42f58-747">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="42f58-747">Az.Storage</span></span>
* <span data-ttu-id="42f58-748">Uppdatera hjälpen för Get/Close-AzStorageFileHandle genom att lägga till fler scenarier i cmdlet-exempel och uppdatera parameterbeskrivningar</span><span class="sxs-lookup"><span data-stu-id="42f58-748">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="42f58-749">Stöd för StandardBlobTier i uppladdningsblob och kopieringsblob</span><span class="sxs-lookup"><span data-stu-id="42f58-749">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="42f58-750">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="42f58-750">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="42f58-751">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="42f58-751">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="42f58-752">Stöd för rehydratiseringsprioritet i kopieringsblob</span><span class="sxs-lookup"><span data-stu-id="42f58-752">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="42f58-753">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="42f58-753">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="42f58-754">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="42f58-754">Az.Websites</span></span>
* <span data-ttu-id="42f58-755">Lägg till klargöranden gällande parametern -AppSettings i Set-AzWebApp och Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="42f58-755">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="42f58-756">2.5.0 – July 2019</span><span class="sxs-lookup"><span data-stu-id="42f58-756">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="42f58-757">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="42f58-757">Az.Accounts</span></span>
* <span data-ttu-id="42f58-758">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="42f58-758">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="42f58-759">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="42f58-759">Az.ApplicationInsights</span></span>
* <span data-ttu-id="42f58-760">Korrigera skrivfel i exempel i dokumentationen för Remove-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="42f58-760">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="42f58-761">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="42f58-761">Az.Automation</span></span>
* <span data-ttu-id="42f58-762">Korrigera skrivfel i resurssträng</span><span class="sxs-lookup"><span data-stu-id="42f58-762">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="42f58-763">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="42f58-763">Az.CognitiveServices</span></span>
* <span data-ttu-id="42f58-764">Stöd för NetworkRuleSet har lagts till.</span><span class="sxs-lookup"><span data-stu-id="42f58-764">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="42f58-765">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="42f58-765">Az.Compute</span></span>
* <span data-ttu-id="42f58-766">Lägg till saknade egenskaper (ComputerName, OsName, OsVersion och HyperVGeneration) för visningsobjekt i den virtuella datorinstansen.</span><span class="sxs-lookup"><span data-stu-id="42f58-766">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="42f58-767">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="42f58-767">Az.ContainerRegistry</span></span>
* <span data-ttu-id="42f58-768">Åtgärda skrivfel i Remove-AzContainerRegistryReplication för parametern Replication</span><span class="sxs-lookup"><span data-stu-id="42f58-768">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="42f58-769">Mer information finns här: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="42f58-769">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="42f58-770">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="42f58-770">Az.DataFactory</span></span>
* <span data-ttu-id="42f58-771">ADF .Net SDK-versionen har uppdaterats till 4.1.0</span><span class="sxs-lookup"><span data-stu-id="42f58-771">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="42f58-772">Korrigera skrivfel i dokumentationen för Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="42f58-772">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="42f58-773">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="42f58-773">Az.EventHub</span></span>
* <span data-ttu-id="42f58-774">Ny cmmdlet har lagts till för att skapa SAS-token: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="42f58-774">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="42f58-775">verifierings- och felmeddelande har lagts till för authorizationrules-rättigheter om endast "hantera" har tilldelats</span><span class="sxs-lookup"><span data-stu-id="42f58-775">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="42f58-776">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="42f58-776">Az.KeyVault</span></span>
* <span data-ttu-id="42f58-777">Stöd har lagts till för att ange KeySize för certifikatprinciper</span><span class="sxs-lookup"><span data-stu-id="42f58-777">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="42f58-778">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="42f58-778">Az.LogicApp</span></span>
* <span data-ttu-id="42f58-779">Korrigering för Get-AzIntegrationAccountMap för att lista alla mappningstyper</span><span class="sxs-lookup"><span data-stu-id="42f58-779">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="42f58-780">Ny MapType-parameter har lagts till för filtrering</span><span class="sxs-lookup"><span data-stu-id="42f58-780">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="42f58-781">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="42f58-781">Az.ManagedServices</span></span>
* <span data-ttu-id="42f58-782">Stöd för API-versionen 2019-06-01 (GA) har lagts till</span><span class="sxs-lookup"><span data-stu-id="42f58-782">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="42f58-783">Az.Network</span><span class="sxs-lookup"><span data-stu-id="42f58-783">Az.Network</span></span>
* <span data-ttu-id="42f58-784">Lägg till stöd för privat slutpunkt och privat länktjänst</span><span class="sxs-lookup"><span data-stu-id="42f58-784">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="42f58-785">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="42f58-785">New cmdlets</span></span>
        - <span data-ttu-id="42f58-786">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="42f58-786">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="42f58-787">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="42f58-787">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="42f58-788">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="42f58-788">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="42f58-789">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="42f58-789">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="42f58-790">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="42f58-790">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="42f58-791">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="42f58-791">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="42f58-792">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="42f58-792">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="42f58-793">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="42f58-793">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="42f58-794">Nedanstående kommandon för funktionen har uppdaterats: Flaggan PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies på undernätet i VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="42f58-794">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="42f58-795">Uppdaterade New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="42f58-795">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="42f58-796">Valfri parameter har lagts till – PrivateEndpointNetworkPoliciesFlag som konfigurerar huruvida nätverksprinciper ska tillämpas på en privat slutpunkt i det här undernätet.</span><span class="sxs-lookup"><span data-stu-id="42f58-796">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="42f58-797">Valfri parameter har lagts till – PrivateLinkServiceNetworkPoliciesFlag som konfigurerar huruvida nätverksprinciper ska tillämpas på en privat länktjänst i det här undernätet.</span><span class="sxs-lookup"><span data-stu-id="42f58-797">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="42f58-798">AzPrivateLinkService för cmdlet-parametern ServiceName har bytt namn till Name med aliaset ServiceName för bakåtkompatibilitet</span><span class="sxs-lookup"><span data-stu-id="42f58-798">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="42f58-799">Aktivera ICMP-protokoll för konfiguration av nätverkssäkerhetsregler</span><span class="sxs-lookup"><span data-stu-id="42f58-799">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="42f58-800">Uppdaterade cmdletar</span><span class="sxs-lookup"><span data-stu-id="42f58-800">Updated cmdlets</span></span>
        - <span data-ttu-id="42f58-801">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="42f58-801">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="42f58-802">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="42f58-802">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="42f58-803">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="42f58-803">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="42f58-804">Lägg till ConnectionProtocolType (Ikev1/Ikev2) som en konfigurerbar parameter för New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="42f58-804">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="42f58-805">Lägg till PrivateIpAddressVersion i LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="42f58-805">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="42f58-806">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="42f58-806">Updated cmdlet:</span></span>
        - <span data-ttu-id="42f58-807">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="42f58-807">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="42f58-808">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="42f58-808">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="42f58-809">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="42f58-809">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="42f58-810">Uppdatering av Application Gateway-kommandot New-AzApplicationGatewayProbeConfig för stöd av anpassad port i Probe</span><span class="sxs-lookup"><span data-stu-id="42f58-810">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="42f58-811">Uppdaterade New-AzApplicationGatewayProbeConfig: Den valfria parametern Port som används för avsökning i serverdelen har lagts till.</span><span class="sxs-lookup"><span data-stu-id="42f58-811">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="42f58-812">Denna parameter gäller för SKU:erna Standard_V2 och WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="42f58-812">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="42f58-813">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="42f58-813">Az.OperationalInsights</span></span>
* <span data-ttu-id="42f58-814">Uppdaterade standardversionen för sparade sökningar till 1.</span><span class="sxs-lookup"><span data-stu-id="42f58-814">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="42f58-815">Åtgärdade hantering av anpassad log null regex</span><span class="sxs-lookup"><span data-stu-id="42f58-815">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="42f58-816">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="42f58-816">Az.RecoveryServices</span></span>
* <span data-ttu-id="42f58-817">Uppdatera Get-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="42f58-817">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="42f58-818">Uppdatera Get-AzRecoveryServicesBackupContainer.md</span><span class="sxs-lookup"><span data-stu-id="42f58-818">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="42f58-819">Uppdatera Get-AzRecoveryServicesVault.md</span><span class="sxs-lookup"><span data-stu-id="42f58-819">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="42f58-820">Uppdatera Wait-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="42f58-820">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="42f58-821">Uppdatera Set-AzRecoveryServicesVaultContext.md</span><span class="sxs-lookup"><span data-stu-id="42f58-821">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="42f58-822">Uppdatera Get-AzRecoveryServicesBackupItem.md</span><span class="sxs-lookup"><span data-stu-id="42f58-822">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="42f58-823">Uppdatera Get-AzRecoveryServicesBackupRecoveryPoint.md</span><span class="sxs-lookup"><span data-stu-id="42f58-823">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="42f58-824">Uppdatera Restore-AzRecoveryServicesBackupItem.md</span><span class="sxs-lookup"><span data-stu-id="42f58-824">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="42f58-825">Uppdaterat tjänstanrop för avregistrering av container för Azure-filresurs</span><span class="sxs-lookup"><span data-stu-id="42f58-825">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="42f58-826">Uppdatera Set-AzRecoveryServicesAsrAlertSetting.md</span><span class="sxs-lookup"><span data-stu-id="42f58-826">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="42f58-827">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="42f58-827">Az.Resources</span></span>
- <span data-ttu-id="42f58-828">Ta bort den cmdlet som saknas och som refereras i dokumentationen till New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="42f58-828">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="42f58-829">Princip-cmdletar har uppdaterats så att de använder den nya API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="42f58-829">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="42f58-830">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="42f58-830">Az.ServiceBus</span></span>
* <span data-ttu-id="42f58-831">Ny cmmdlet har lagts till för att skapa SAS-token: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="42f58-831">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="42f58-832">verifierings- och felmeddelande har lagts till för authorizationrules-rättigheter om endast "hantera" har tilldelats</span><span class="sxs-lookup"><span data-stu-id="42f58-832">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="42f58-833">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="42f58-833">Az.Sql</span></span>
* <span data-ttu-id="42f58-834">Åtgärda saknade exempel för Set-AzSqlDatabaseSecondary cmdlet</span><span class="sxs-lookup"><span data-stu-id="42f58-834">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="42f58-835">Åtgärda angivna återkommande genomsökningar för bedömning av säkerhetsrisk utan angivna e-postadresser</span><span class="sxs-lookup"><span data-stu-id="42f58-835">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="42f58-836">Korrigera ett skrivfel i ett varningsmeddelande.</span><span class="sxs-lookup"><span data-stu-id="42f58-836">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="42f58-837">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="42f58-837">Az.Storage</span></span>
* <span data-ttu-id="42f58-838">Uppdatera exempel i referensdokumentationen för Get-AzStorageAccount så att rätt parameternamn används</span><span class="sxs-lookup"><span data-stu-id="42f58-838">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="42f58-839">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="42f58-839">Az.StorageSync</span></span>
* <span data-ttu-id="42f58-840">Lägger till cmdleten Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="42f58-840">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="42f58-841">Åtgärda problem 9551 så att TierFilesOlderThanDays föredras</span><span class="sxs-lookup"><span data-stu-id="42f58-841">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="42f58-842">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="42f58-842">Az.Websites</span></span>
* <span data-ttu-id="42f58-843">Åtgärdar ett fel där vissa SiteConfig-egenskaper inte returnerades av Get-AzWebApp och Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="42f58-843">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="42f58-844">Lägger till en ny platsparameter för Get-AzDeletedWebApp och Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="42f58-844">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="42f58-845">Åtgärdar ett fel i kloning av webbapp-platser som använder New-AzWebApp-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="42f58-845">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="42f58-846">2.4.0 – juli 2019</span><span class="sxs-lookup"><span data-stu-id="42f58-846">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="42f58-847">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="42f58-847">Az.Accounts</span></span>
* <span data-ttu-id="42f58-848">Lägg till stöd för profil-cmdletar</span><span class="sxs-lookup"><span data-stu-id="42f58-848">Add support for profile cmdlets</span></span>
* <span data-ttu-id="42f58-849">Lägg till stöd för miljöer och dataplaner i genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="42f58-849">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="42f58-850">Åtgärda bugg där fel slutpunkt i vissa fall användes för cmdletar för dataplaner i Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="42f58-850">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="42f58-851">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="42f58-851">Az.Advisor</span></span>
* <span data-ttu-id="42f58-852">GA-version av Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="42f58-852">GA release of Az.Advisor</span></span>
* <span data-ttu-id="42f58-853">Den här modulen ingår nu som en del av `Az`-sammanslagningsmodulen</span><span class="sxs-lookup"><span data-stu-id="42f58-853">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="42f58-854">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="42f58-854">Az.ApiManagement</span></span>
* <span data-ttu-id="42f58-855">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="42f58-855">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="42f58-856">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="42f58-856">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="42f58-857">Stöd för att fråga prenumerationer efter användare och produkt har lagts till</span><span class="sxs-lookup"><span data-stu-id="42f58-857">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="42f58-858">Stöd för att fråga med hjälp av omfång ”/”, ”/apis”, ”/apis/echo-api” har lagts till</span><span class="sxs-lookup"><span data-stu-id="42f58-858">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="42f58-859">Korrigering av problem https://github.com/Azure/azure-powershell/issues/9307 och https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="42f58-859">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="42f58-860">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="42f58-860">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="42f58-861">Stöd för att ange ”ApiVersion” och ”ApiVersionSetId” när API:er importeras har lagts till</span><span class="sxs-lookup"><span data-stu-id="42f58-861">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="42f58-862">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="42f58-862">Az.Automation</span></span>
* <span data-ttu-id="42f58-863">Bugg med cmdleten Set-AzAutomationConnectionFieldValue för att hantera strängvärde har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="42f58-863">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="42f58-864">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="42f58-864">Az.Compute</span></span>
* <span data-ttu-id="42f58-865">Lägg till parametern HyperVGeneration i New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="42f58-865">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="42f58-866">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="42f58-866">Az.DataFactory</span></span>
* <span data-ttu-id="42f58-867">Uppdaterar utdata från ADF-cmdletar som hämtar aktivitetskörningar, hämtar pipelinekörningar och hämtar utlösarkörningar för stöd för Select-Object-pipe.</span><span class="sxs-lookup"><span data-stu-id="42f58-867">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="42f58-868">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="42f58-868">Az.EventGrid</span></span>
* <span data-ttu-id="42f58-869">Korrigera stavfel i dokumentation om ”New-AzEventGridSubscription”</span><span class="sxs-lookup"><span data-stu-id="42f58-869">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="42f58-870">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="42f58-870">Az.IotHub</span></span>
* <span data-ttu-id="42f58-871">Lägg till stöd för att återskapa principnycklar för auktorisering.</span><span class="sxs-lookup"><span data-stu-id="42f58-871">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="42f58-872">Az.Network</span><span class="sxs-lookup"><span data-stu-id="42f58-872">Az.Network</span></span>
* <span data-ttu-id="42f58-873">”RoutingPreference” har lagts till i offentliga IP-taggar</span><span class="sxs-lookup"><span data-stu-id="42f58-873">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="42f58-874">Förbättra exempel för referensdokumentation om ”Get-AzNetworkServiceTag”</span><span class="sxs-lookup"><span data-stu-id="42f58-874">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="42f58-875">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="42f58-875">Az.PolicyInsights</span></span>
* <span data-ttu-id="42f58-876">Åtgärda problem med null-referens i Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="42f58-876">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="42f58-877">Mer information här: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="42f58-877">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="42f58-878">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="42f58-878">Az.OperationalInsights</span></span>
* <span data-ttu-id="42f58-879">Modellen för CustomLog-datakälla som returneras i Get-AzOperationalInsightsDataSource har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="42f58-879">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="42f58-880">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="42f58-880">Az.RecoveryServices</span></span>
* <span data-ttu-id="42f58-881">Kommandot get-policy för IaaSVM:er har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="42f58-881">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="42f58-882">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="42f58-882">Az.Resources</span></span>
    - <span data-ttu-id="42f58-883">Korrigera hjälptext för den översta parametern i Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="42f58-883">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="42f58-884">Lägg till växlingsstöd på klientsidan för Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="42f58-884">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="42f58-885">Lägg till nya parametrar för Set-AzPolicyAssignment, -PolicyParameters och -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="42f58-885">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="42f58-886">En mängd dokument- och exempeluppdateringar för Policy-cmdletar</span><span class="sxs-lookup"><span data-stu-id="42f58-886">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="42f58-887">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="42f58-887">Az.ServiceBus</span></span>
* <span data-ttu-id="42f58-888">Korrigering av problem #4938 – New-AzureRmServiceBusQueue returnerar BadRequest vid konfiguration av MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="42f58-888">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="42f58-889">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="42f58-889">Az.Sql</span></span>
* <span data-ttu-id="42f58-890">Lägg till cmdletar för instansredundansgrupper från förhandsversion till offentlig version</span><span class="sxs-lookup"><span data-stu-id="42f58-890">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="42f58-891">Stöd för granskning för Azure SQL Server\Database med nya cmdletar.</span><span class="sxs-lookup"><span data-stu-id="42f58-891">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="42f58-892">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="42f58-892">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="42f58-893">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="42f58-893">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="42f58-894">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="42f58-894">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="42f58-895">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="42f58-895">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="42f58-896">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="42f58-896">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="42f58-897">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="42f58-897">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="42f58-898">Ta bort begränsningar för e-post från inställningarna för sårbarhetsbedömning</span><span class="sxs-lookup"><span data-stu-id="42f58-898">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="42f58-899">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="42f58-899">Az.Storage</span></span>
* <span data-ttu-id="42f58-900">Ändra två parametrar ”-IndexDocument” och ”-ErrorDocument404Path” från ”krävs” till ”valfri” i cmdlet:</span><span class="sxs-lookup"><span data-stu-id="42f58-900">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="42f58-901">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="42f58-901">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="42f58-902">Uppdatera hjälpen för Get-AzStorageBlobContent genom att lägga till ett exempel</span><span class="sxs-lookup"><span data-stu-id="42f58-902">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="42f58-903">Visa mer felinformation när cmdleten misslyckas med StorageException</span><span class="sxs-lookup"><span data-stu-id="42f58-903">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="42f58-904">Stöd för att skapa eller uppdatera lagringskonto med Azure Files AAD DS-autentisering</span><span class="sxs-lookup"><span data-stu-id="42f58-904">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="42f58-905">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="42f58-905">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="42f58-906">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="42f58-906">Set-AzStorageAccount</span></span>
* <span data-ttu-id="42f58-907">Stöd för att lista eller stänga filreferenser för en filresurs, filkatalog eller en fil</span><span class="sxs-lookup"><span data-stu-id="42f58-907">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="42f58-908">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="42f58-908">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="42f58-909">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="42f58-909">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="42f58-910">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="42f58-910">Az.StorageSync</span></span>
* <span data-ttu-id="42f58-911">Den här modulen ingår nu som en del av `Az`-sammanslagningsmodulen</span><span class="sxs-lookup"><span data-stu-id="42f58-911">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="42f58-912">2.3.2 – juni 2019</span><span class="sxs-lookup"><span data-stu-id="42f58-912">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="42f58-913">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="42f58-913">Az.Accounts</span></span>
* <span data-ttu-id="42f58-914">Åtgärda bugg med felaktiga webbadresser som i vissa fall användes för Functions-anrop</span><span class="sxs-lookup"><span data-stu-id="42f58-914">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="42f58-915">Mer information här: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="42f58-915">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="42f58-916">Åtgärda problem med alias från AzureRM i Az-cmdletar</span><span class="sxs-lookup"><span data-stu-id="42f58-916">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="42f58-917">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="42f58-917">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="42f58-918">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="42f58-918">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="42f58-919">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="42f58-919">Az.Compute</span></span>
* <span data-ttu-id="42f58-920">Parameteruppsättningarna New-AzVm och New-AzVmss accepterar nu parametern ”ProximityPlacementGroup”.</span><span class="sxs-lookup"><span data-stu-id="42f58-920">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="42f58-921">Stavfel i referensdokumentationen för ”New-AzVM” har korrigerats</span><span class="sxs-lookup"><span data-stu-id="42f58-921">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="42f58-922">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="42f58-922">Az.Dns</span></span>
* <span data-ttu-id="42f58-923">Stavfel i hjälpexempel för ”Set-AzDnsZone” har korrigerats.</span><span class="sxs-lookup"><span data-stu-id="42f58-923">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="42f58-924">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="42f58-924">Az.EventGrid</span></span>
* <span data-ttu-id="42f58-925">Har uppdaterats för att använda API-versionen 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="42f58-925">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="42f58-926">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="42f58-926">New cmdlets:</span></span>
    - <span data-ttu-id="42f58-927">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="42f58-927">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="42f58-928">Skapar en ny Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="42f58-928">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="42f58-929">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="42f58-929">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="42f58-930">Hämtar information om en Event Grid-domän eller hämtar en lista med alla Event Grid-domäner i den aktuella Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="42f58-930">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="42f58-931">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="42f58-931">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="42f58-932">Tar bort en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="42f58-932">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="42f58-933">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="42f58-933">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="42f58-934">Återskapar nyckeln för delad åtkomst för en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="42f58-934">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="42f58-935">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="42f58-935">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="42f58-936">Hämtar de nycklar för delad åtkomst som används för att publicera händelser till en Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="42f58-936">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="42f58-937">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="42f58-937">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="42f58-938">Skapar ett nytt Azure Event Grid-domänämne.</span><span class="sxs-lookup"><span data-stu-id="42f58-938">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="42f58-939">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="42f58-939">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="42f58-940">Hämtar information om ett Event Grid-domänämne eller hämtar en lista med alla Event Grid-domänämnen under en specifik Event Grid-domän i nuvarande Azure</span><span class="sxs-lookup"><span data-stu-id="42f58-940">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="42f58-941">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="42f58-941">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="42f58-942">Tar bort ett befintligt Azure Event Grid-domänämne.</span><span class="sxs-lookup"><span data-stu-id="42f58-942">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="42f58-943">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="42f58-943">Updated cmdlets:</span></span>
    - <span data-ttu-id="42f58-944">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="42f58-944">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="42f58-945">Lägg till nya obligatoriska parametrar för att stödja piping för den nya Event Grid-domänen och Event Grid-domänämnet för att göra det möjligt att skapa nya händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="42f58-945">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="42f58-946">Lägg till nya obligatoriska parametrar för att ange det nya Event Grid-domännamnet och/eller namnet på Event Grid-domänämnet för att göra det möjligt att skapa nya händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="42f58-946">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="42f58-947">Lägg till ny parameteruppsättningar för domäner och domänämnen för att göra det möjligt att återanvända befintliga parametrar (t.ex. EndPointType, SubjectBeginsWith osv).</span><span class="sxs-lookup"><span data-stu-id="42f58-947">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="42f58-948">Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="42f58-948">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="42f58-949">Förfallodatum för händelseprenumeration</span><span class="sxs-lookup"><span data-stu-id="42f58-949">Event subscription expiration date,</span></span>
            - <span data-ttu-id="42f58-950">Avancerade filterparametrar.</span><span class="sxs-lookup"><span data-stu-id="42f58-950">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="42f58-951">Lägg till ny uppräkning för servicebusqueue som mål.</span><span class="sxs-lookup"><span data-stu-id="42f58-951">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="42f58-952">Tillåt inte användning av ”Alla” i alternativet -IncludedEventType och ersätt det med</span><span class="sxs-lookup"><span data-stu-id="42f58-952">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="42f58-953">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="42f58-953">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="42f58-954">Lägg till ny valfria parametrar (Top, ODataQuery och NextLink) för att stödja sidnumrering och filtrering av resultat.</span><span class="sxs-lookup"><span data-stu-id="42f58-954">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="42f58-955">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="42f58-955">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="42f58-956">Lägg till nya obligatoriska parametrar för att stödja piping för en Event Grid-domän och Event Grid-domänämnen för att göra det möjligt att ta bort befintliga händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="42f58-956">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="42f58-957">Lägg till nya obligatoriska parametrar för att ange Event Grid-domännamnet och/eller namnet på Event Grid-domänämnet för att göra det möjligt att ta bort befintliga händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="42f58-957">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="42f58-958">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="42f58-958">Az.FrontDoor</span></span>
* <span data-ttu-id="42f58-959">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="42f58-959">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="42f58-960">Lägg till stöd för transformeringar och nytt värde för automatisk komplettering för operatorer (RegEx)</span><span class="sxs-lookup"><span data-stu-id="42f58-960">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="42f58-961">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="42f58-961">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="42f58-962">Lägg till nya värden för automatisk komplettering</span><span class="sxs-lookup"><span data-stu-id="42f58-962">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="42f58-963">Az.Network</span><span class="sxs-lookup"><span data-stu-id="42f58-963">Az.Network</span></span>
* <span data-ttu-id="42f58-964">Lägg till stöd för resurs för virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="42f58-964">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="42f58-965">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="42f58-965">New cmdlets</span></span>
        - <span data-ttu-id="42f58-966">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="42f58-966">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="42f58-967">Lägg till AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="42f58-967">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="42f58-968">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="42f58-968">New cmdlets</span></span> 
        - <span data-ttu-id="42f58-969">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="42f58-969">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="42f58-970">Lägg till PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="42f58-970">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="42f58-971">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="42f58-971">New cmdlets</span></span> 
        - <span data-ttu-id="42f58-972">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="42f58-972">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="42f58-973">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="42f58-973">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="42f58-974">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="42f58-974">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="42f58-975">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="42f58-975">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="42f58-976">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="42f58-976">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="42f58-977">Lägg till PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="42f58-977">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="42f58-978">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="42f58-978">New cmdlets</span></span>
        - <span data-ttu-id="42f58-979">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="42f58-979">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="42f58-980">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="42f58-980">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="42f58-981">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="42f58-981">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="42f58-982">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="42f58-982">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="42f58-983">Nedanstående kommandon för funktionen har uppdaterats: Flaggan UseLocalAzureIpAddress på VpnConnection</span><span class="sxs-lookup"><span data-stu-id="42f58-983">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="42f58-984">New-AzVpnConnection har uppdaterats: Den valfria parametern -UseLocalAzureIpAddress har lagts till för att visa att en lokal IP-adress i Azure ska användas som källadress när anslutningen initieras.</span><span class="sxs-lookup"><span data-stu-id="42f58-984">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="42f58-985">Set-AzVpnConnection har uppdaterats: Den valfria parametern -UseLocalAzureIpAddress har lagts till för att visa att en lokal IP-adress i Azure ska användas som källadress när anslutningen initieras.</span><span class="sxs-lookup"><span data-stu-id="42f58-985">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="42f58-986">Det skrivskyddade fältet PeeredConnections har lagts till i ExpressRoute-peering.</span><span class="sxs-lookup"><span data-stu-id="42f58-986">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="42f58-987">Det skrivskyddade fältet GlobalReachEnabled har lagts till i ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="42f58-987">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="42f58-988">Ett attribut för icke-bakåtkompatibla ändringar har lagts till för att lyfta fram utfasning av fältet AllowGlobalReach i modellen ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="42f58-988">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="42f58-989">Problem 8756 har åtgärdats: Fel vid användning av TargetListenerID med AzApplicationGatewayRedirectConfiguration-cmdletar</span><span class="sxs-lookup"><span data-stu-id="42f58-989">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="42f58-990">En bugg i New-AzApplicationGatewayPathRuleConfig som gjorde att regeluppsättningen för att återskapa inte kunde anges har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="42f58-990">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="42f58-991">Visningen av VirtualNetworkTaps i NetworkInterfaceIpConfiguration har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="42f58-991">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="42f58-992">Cortex Get-cmdletar för att visa en lista med alla delar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="42f58-992">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="42f58-993">Funktionen för att skapa VirtualHub-referenser för ExpressRouteGateways och VpnGateway har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="42f58-993">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="42f58-994">Stöd för tillgänglighetszoner i AzureFirewall och NatGateway har lagts till</span><span class="sxs-lookup"><span data-stu-id="42f58-994">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="42f58-995">Cmdleten Get-AzNetworkServiceTag har lagts till</span><span class="sxs-lookup"><span data-stu-id="42f58-995">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="42f58-996">Lägg till stöd för flera offentliga IP-adresser för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="42f58-996">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="42f58-997">Cmdleten New-AzFirewall har uppdaterats:</span><span class="sxs-lookup"><span data-stu-id="42f58-997">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="42f58-998">Parametern -PublicIpAddress som accepterar ett eller flera offentliga IP-adressobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="42f58-998">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="42f58-999">Parametern -VirtualNetwork som accepterar ett virtuellt nätverksobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="42f58-999">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="42f58-1000">Metoderna AddPublicIpAddress och RemovePublicIpAddress har lagts till på brandväggsobjekt – dessa accepterar ett offentligt IP-adressobjekt som indata</span><span class="sxs-lookup"><span data-stu-id="42f58-1000">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="42f58-1001">Inaktuella parametrar -PublicIpName och -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="42f58-1001">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="42f58-1002">Nedanstående kommandon för funktionen har uppdaterats: Ange autentiseringsalternativ för VpnClient AAD till resurser för virtuella nätverksgatewayer.</span><span class="sxs-lookup"><span data-stu-id="42f58-1002">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="42f58-1003">New-AzVirtualNetworkGateway har uppdaterats: De valfria parametrarna AadTenantUri, AadAudienceId och AadIssuerUri för att ange VpnClient AAD-autentiseringsalternativ på en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="42f58-1003">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="42f58-1004">Set-AzVirtualNetworkGateway har uppdaterats: De valfria parametrarna AadTenantUri, AadAudienceId och AadIssuerUri för att ange VpnClient AAD-autentiseringsalternativ på en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="42f58-1004">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="42f58-1005">Set-AzVirtualNetworkGateway har uppdaterats: Den valfria växelparametern RemoveAadAuthentication som tar bort VpnClient AAD-autentiseringsalternativ från en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="42f58-1005">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="42f58-1006">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="42f58-1006">Az.OperationalInsights</span></span>
* <span data-ttu-id="42f58-1007">Aktivera prisnivån **pergb2018** i kommandot ”New-AzureRmOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="42f58-1007">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="42f58-1008">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="42f58-1008">Az.Resources</span></span>
* <span data-ttu-id="42f58-1009">Stöd för ytterligare alternativ för att exportera en mall</span><span class="sxs-lookup"><span data-stu-id="42f58-1009">Support for additional Template Export options</span></span>
    - <span data-ttu-id="42f58-1010">Lägg till parametern ”-SkipResourceNameParameterization” till Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="42f58-1010">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="42f58-1011">Lägg till parametern ”-SkipAllParameterization” till Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="42f58-1011">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="42f58-1012">Lägg till parametern ”-Resource” till Export-AzResourceGroup för exporterad resursfiltrering</span><span class="sxs-lookup"><span data-stu-id="42f58-1012">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="42f58-1013">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="42f58-1013">Az.ServiceFabric</span></span>
* <span data-ttu-id="42f58-1014">Åtgärda att fel tumavtryck används vid tilläggning av certifikat i ByExistingKeyVault i vissa fall</span><span class="sxs-lookup"><span data-stu-id="42f58-1014">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="42f58-1015">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="42f58-1015">Az.Sql</span></span>
* <span data-ttu-id="42f58-1016">Åtgärda suffix för lagringsslutpunkt i Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="42f58-1016">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="42f58-1017">Åtgärda att aktivering av Advanced Data Security åsidosätter Advanced Threat Protection-princip</span><span class="sxs-lookup"><span data-stu-id="42f58-1017">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="42f58-1018">Nya cmdletar för Management.Sql som gör att kunderna kan lägga till nycklar för transparent datakryptering (TDE) och ange TDE-skydd för hanterade instanser</span><span class="sxs-lookup"><span data-stu-id="42f58-1018">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="42f58-1019">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="42f58-1019">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="42f58-1020">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="42f58-1020">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="42f58-1021">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="42f58-1021">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="42f58-1022">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="42f58-1022">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="42f58-1023">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="42f58-1023">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="42f58-1024">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="42f58-1024">Az.Storage</span></span>
* <span data-ttu-id="42f58-1025">Stöd för typerna FileStorage och SkuName Premium_ZRS när lagringskonton skapas</span><span class="sxs-lookup"><span data-stu-id="42f58-1025">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="42f58-1026">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="42f58-1026">New-AzStorageAccount</span></span>
* <span data-ttu-id="42f58-1027">Beskrivningen av cmdleten för bloboföränderlighet har förtydligats</span><span class="sxs-lookup"><span data-stu-id="42f58-1027">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="42f58-1028">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="42f58-1028">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="42f58-1029">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="42f58-1029">Az.Websites</span></span>
* <span data-ttu-id="42f58-1030">Optimerar Get-AzWebAppCertificate för att filtrera efter resursgrupp på servern i stället för klienten</span><span class="sxs-lookup"><span data-stu-id="42f58-1030">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="42f58-1031">Lägger till växlingsparametern -UseDisasterRecovery till Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="42f58-1031">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="42f58-1032">2.2.0 – juni 2019</span><span class="sxs-lookup"><span data-stu-id="42f58-1032">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="42f58-1033">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="42f58-1033">Az.Cdn</span></span>
* <span data-ttu-id="42f58-1034">Uppdaterade cmdletar för att ge stöd för rulesEngine-funktion baserat på API-version 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="42f58-1034">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="42f58-1035">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="42f58-1035">Az.Compute</span></span>
* <span data-ttu-id="42f58-1036">Lade till parameter `NoWait` som startar åtgärden och returnerar omedelbart, innan åtgärden har slutförts.</span><span class="sxs-lookup"><span data-stu-id="42f58-1036">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="42f58-1037">Uppdaterade cmdletar:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="42f58-1037">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="42f58-1038">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="42f58-1038">Az.EventHub</span></span>
* <span data-ttu-id="42f58-1039">Korrigering för #9231 – Get-AzEventHubNamespace returnerar inga taggar</span><span class="sxs-lookup"><span data-stu-id="42f58-1039">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="42f58-1040">Korrigering för #9230 – Get-AzEventHubNamespace returnerar ResourceGroup istället för ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42f58-1040">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="42f58-1041">Az.Network</span><span class="sxs-lookup"><span data-stu-id="42f58-1041">Az.Network</span></span>
* <span data-ttu-id="42f58-1042">Uppdatera ResourceId och InputObject för NAT-gateway</span><span class="sxs-lookup"><span data-stu-id="42f58-1042">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="42f58-1043">Lägg till alias för ResourceId och InputObject</span><span class="sxs-lookup"><span data-stu-id="42f58-1043">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="42f58-1044">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="42f58-1044">Az.PolicyInsights</span></span>
* <span data-ttu-id="42f58-1045">Åtgärda Null-referensproblem i Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="42f58-1045">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="42f58-1046">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="42f58-1046">Az.RecoveryServices</span></span>
* <span data-ttu-id="42f58-1047">Minsta kvarhållning för IaaSVM-policy i dagar ändrat till 7 från 1</span><span class="sxs-lookup"><span data-stu-id="42f58-1047">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="42f58-1048">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="42f58-1048">Az.ServiceBus</span></span>
* <span data-ttu-id="42f58-1049">Korrigering för ärende #9182 – Get-AzServiceBusNamespace returnerar ResourceGroup istället för ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42f58-1049">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="42f58-1050">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="42f58-1050">Az.ServiceFabric</span></span>
* <span data-ttu-id="42f58-1051">Åtgärda stavfel i felmeddelandet för Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="42f58-1051">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="42f58-1052">Åtgärda saknat tecken i Service Fabric-kommandorader</span><span class="sxs-lookup"><span data-stu-id="42f58-1052">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="42f58-1053">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="42f58-1053">Az.Sql</span></span>
* <span data-ttu-id="42f58-1054">Lägg till parametern DnsZonePartner för New-AzureSqlInstance-cmdlet för att ge stöd för AutoDr för hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="42f58-1054">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="42f58-1055">Avvecklar cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="42f58-1055">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="42f58-1056">Döp om cmdletar för hotidentifiering till Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="42f58-1056">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="42f58-1057">Parametrarna New-AzSqlInstance -StorageSizeInGB och -LicenseType är nu valfria.</span><span class="sxs-lookup"><span data-stu-id="42f58-1057">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="42f58-1058">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="42f58-1058">Az.Websites</span></span>
* <span data-ttu-id="42f58-1059">åtgärdar problemet där användningen av Set-AzWebApp och Set-AzWebAppSlot med -WebApp-egenskap tog bort taggarna</span><span class="sxs-lookup"><span data-stu-id="42f58-1059">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="42f58-1060">2.1.0 – maj 2019</span><span class="sxs-lookup"><span data-stu-id="42f58-1060">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="42f58-1061">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="42f58-1061">Az.ApiManagement</span></span>
* <span data-ttu-id="42f58-1062">Skapade nya cmdletar för att hantera diagnostik för global- och API-omfång</span><span class="sxs-lookup"><span data-stu-id="42f58-1062">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="42f58-1063">**Get-AzApiManagementDiagnostic** – Skaffa diagnostik konfigurerad för global- eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="42f58-1063">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="42f58-1064">**New-AzApiManagementDiagnostic** – Skapa ny diagnostik för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="42f58-1064">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="42f58-1065">**New-AzApiManagementHttpMessageDiagnostic** – Skapa diagnostikinställning om vilka rubriker som ska loggas och storleken på brödtextbyte</span><span class="sxs-lookup"><span data-stu-id="42f58-1065">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="42f58-1066">**New-AzApiManagementPipelineDiagnosticSetting** – Skapa diagnostikinställningar för inkommande/utgående HTTP-meddelanden till gatewayen.</span><span class="sxs-lookup"><span data-stu-id="42f58-1066">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="42f58-1067">**New-AzApiManagementSamplingSetting** – Skapa samplinginställningar för begäranden/svar för en diagnostik</span><span class="sxs-lookup"><span data-stu-id="42f58-1067">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="42f58-1068">**Remove-AzApiManagementDiagnostic** – Ta bort en diagnostikenhet för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="42f58-1068">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="42f58-1069">**Set-AzApiManagementDiagnostic** – Uppdatera en diagnostikenhet för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="42f58-1069">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="42f58-1070">Skapade nya cmdletar för hantering av cacheminne i ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="42f58-1070">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="42f58-1071">**Get-AzApiManagementCache** – Hämta information om cacheminnet som anges av identifierare eller alla cacheminnen</span><span class="sxs-lookup"><span data-stu-id="42f58-1071">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="42f58-1072">**New-AzApiManagementCache** – Skapa ett nytt default-cacheminne eller cacheminne i en viss Azure-region</span><span class="sxs-lookup"><span data-stu-id="42f58-1072">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="42f58-1073">**Remove-AzApiManagementCache** – Ta bort ett cacheminne</span><span class="sxs-lookup"><span data-stu-id="42f58-1073">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="42f58-1074">**Remove-AzApiManagementCache** – Ta bort ett cacheminne</span><span class="sxs-lookup"><span data-stu-id="42f58-1074">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="42f58-1075">Skapade nya cmdletar för hantering av API-schema</span><span class="sxs-lookup"><span data-stu-id="42f58-1075">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="42f58-1076">**New-AzApiManagementSchema** – Skapa ett nytt schema för ett API</span><span class="sxs-lookup"><span data-stu-id="42f58-1076">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="42f58-1077">**Get-AzApiManagementSchema** – Hämta de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="42f58-1077">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="42f58-1078">**Remove-AzApiManagementSchema** – Ta bort de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="42f58-1078">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="42f58-1079">**Set-AzApiManagementSchema** – Uppdatera de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="42f58-1079">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="42f58-1080">Skapa ny cmdlet för att generera en användartoken.</span><span class="sxs-lookup"><span data-stu-id="42f58-1080">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="42f58-1081">**New-AzApiManagementUserToken** – Skapa en ny användartoken som enligt standardinställning är giltig i 8 timmar. Token för GIT-användaren kan skapas med den här cmdleten./</span><span class="sxs-lookup"><span data-stu-id="42f58-1081">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="42f58-1082">Skapade en ny cmdlet för att hämta nätverksstatus</span><span class="sxs-lookup"><span data-stu-id="42f58-1082">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="42f58-1083">**Get-AzApiManagementNetworkStatus** – Hämta nätverksstatusanslutningen för resurserna som API Management-tjänsten är beroende av.</span><span class="sxs-lookup"><span data-stu-id="42f58-1083">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="42f58-1084">Det här är användbart när du distribuerar ApiManagement-tjänsten i ett virtuellt nätverk och validerar om något beroende är brutet.</span><span class="sxs-lookup"><span data-stu-id="42f58-1084">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="42f58-1085">Uppdaterade cmdlet **New-AzApiManagement** för att hantera ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="42f58-1085">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="42f58-1086">Lade till stöd för den nya SKU:n Consumption</span><span class="sxs-lookup"><span data-stu-id="42f58-1086">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="42f58-1087">Aktiverade stöd för att slå på flaggan EnableClientCertificate för SKU:n Consumption</span><span class="sxs-lookup"><span data-stu-id="42f58-1087">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="42f58-1088">Den nya cmdleten **New-AzApiManagementSslSetting** gör det möjligt att ställa in TLS/SSL-inställningen på ”Backend” och ”Frontend” (serverdel och klientdel).</span><span class="sxs-lookup"><span data-stu-id="42f58-1088">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="42f58-1089">Det här kan också användas till att konfigurera chiffer som 3DES och ServerProtocols som Http2 för Frontend för en ApiManagement-tjänst.</span><span class="sxs-lookup"><span data-stu-id="42f58-1089">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="42f58-1090">Stöd har lagts till för att konfigurera värdnamnet DeveloperPortal på ApiManagement-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="42f58-1090">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="42f58-1091">Uppdaterade cmdletar **Get-AzApiManagementSsoToken** för att ta PsApiManagement-objekt som indata</span><span class="sxs-lookup"><span data-stu-id="42f58-1091">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="42f58-1092">Uppdaterad cmdleten för att visa infogade felmeddelanden</span><span class="sxs-lookup"><span data-stu-id="42f58-1092">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="42f58-1093">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Felkod: Felmeddelande av typen ValidationError: Ett eller flera fält innehåller felaktiga värden: Felinformation:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="42f58-1093">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="42f58-1094">Uppdaterade cmdlet **Export-AzApiManagementApi** för att exportera API:er i OpenApi 3.0-format</span><span class="sxs-lookup"><span data-stu-id="42f58-1094">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="42f58-1095">Uppdaterade cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="42f58-1095">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="42f58-1096">Importera API från dokumentspecifikationen OpenApi 3.0</span><span class="sxs-lookup"><span data-stu-id="42f58-1096">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="42f58-1097">Om du vill åsidosätta egenskapen PsApiManagementSchema specificerad i ett dokument (Swagger, Wadl, Wsdl, OpenApi).</span><span class="sxs-lookup"><span data-stu-id="42f58-1097">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="42f58-1098">Åsidosätta egenskapen ServiceUrl som specificeras i ett dokument.</span><span class="sxs-lookup"><span data-stu-id="42f58-1098">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="42f58-1099">Uppdaterade cmdlet **Get-AzApiManagementPolicy** för att returnera policy i undantaget format av typen icke-XML med rawxml</span><span class="sxs-lookup"><span data-stu-id="42f58-1099">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="42f58-1100">Uppdaterade cmdlet **Set-AzApiManagementPolicy** för att godkänna policy i undantaget format av typen icke-XML med rawxml och XML undantaget med xml</span><span class="sxs-lookup"><span data-stu-id="42f58-1100">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="42f58-1101">Uppdaterad cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="42f58-1101">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="42f58-1102">Konfigurera API med OpenId auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="42f58-1102">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="42f58-1103">Skapa ett API i ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="42f58-1103">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="42f58-1104">Klona ett API med SourceApiId och SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="42f58-1104">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="42f58-1105">Möjlighet att konfigurera SubscriptionRequired i API-omfattningen.</span><span class="sxs-lookup"><span data-stu-id="42f58-1105">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="42f58-1106">Uppdaterad cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="42f58-1106">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="42f58-1107">Konfigurera API med OpenId auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="42f58-1107">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="42f58-1108">Uppdatera ett API till ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="42f58-1108">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="42f58-1109">Möjlighet att konfigurera SubscriptionRequired i API-omfattningen.</span><span class="sxs-lookup"><span data-stu-id="42f58-1109">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="42f58-1110">Uppdaterad cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="42f58-1110">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="42f58-1111">Klona en befintlig version med hjälp av SourceApiRevision (kopiera taggar, produkter, åtgärder och principer).</span><span class="sxs-lookup"><span data-stu-id="42f58-1111">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="42f58-1112">Den nya revisionen antar ApiId från den överordnade instansen.</span><span class="sxs-lookup"><span data-stu-id="42f58-1112">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="42f58-1113">Tillhandahålla ApiRevisionDescription</span><span class="sxs-lookup"><span data-stu-id="42f58-1113">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="42f58-1114">Åsidosätta ServiceUrl vid kloning av ett API.</span><span class="sxs-lookup"><span data-stu-id="42f58-1114">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="42f58-1115">Uppdaterad cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="42f58-1115">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="42f58-1116">Konfigurera AAD eller AADB2C med en Authority</span><span class="sxs-lookup"><span data-stu-id="42f58-1116">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="42f58-1117">Konfigurera SignupPolicy, SigninPolicy, ProfileEditingPolicy och PasswordResetPolicy</span><span class="sxs-lookup"><span data-stu-id="42f58-1117">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="42f58-1118">Uppdaterad cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="42f58-1118">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="42f58-1119">Kompensera för ny SubscriptonModel med Scope och UserId</span><span class="sxs-lookup"><span data-stu-id="42f58-1119">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="42f58-1120">Kompensera för gammal prenumerationsmodell med ProductId och UserId</span><span class="sxs-lookup"><span data-stu-id="42f58-1120">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="42f58-1121">Lägg till funktion för att aktivera AllowTracing på prenumerationsnivå.</span><span class="sxs-lookup"><span data-stu-id="42f58-1121">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="42f58-1122">Uppdaterad cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="42f58-1122">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="42f58-1123">Kompensera för ny SubscriptonModel med Scope och UserId</span><span class="sxs-lookup"><span data-stu-id="42f58-1123">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="42f58-1124">Kompensera för gammal prenumerationsmodell med ProductId och UserId</span><span class="sxs-lookup"><span data-stu-id="42f58-1124">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="42f58-1125">Lägg till funktion för att aktivera AllowTracing på prenumerationsnivå.</span><span class="sxs-lookup"><span data-stu-id="42f58-1125">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="42f58-1126">Uppdaterade följande cmdletar för att acceptera ResourceId som indata</span><span class="sxs-lookup"><span data-stu-id="42f58-1126">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="42f58-1127">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="42f58-1127">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="42f58-1128">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="42f58-1128">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="42f58-1129">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="42f58-1129">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="42f58-1130">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="42f58-1130">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="42f58-1131">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="42f58-1131">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="42f58-1132">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="42f58-1132">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="42f58-1133">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="42f58-1133">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="42f58-1134">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="42f58-1134">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="42f58-1135">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="42f58-1135">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="42f58-1136">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="42f58-1136">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="42f58-1137">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="42f58-1137">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="42f58-1138">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="42f58-1138">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="42f58-1139">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="42f58-1139">Az.Automation</span></span>
* <span data-ttu-id="42f58-1140">Uppdaterade Get-AzAutomationJobOutputRecord för att hantera postvärden av typen JSON och Text.</span><span class="sxs-lookup"><span data-stu-id="42f58-1140">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="42f58-1141">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="42f58-1141">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="42f58-1142">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="42f58-1142">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="42f58-1143">Ändrade beteende för Start-AzAutomationDscCompilationJob till att bara starta jobbet istället för att vänta på slutförandet.</span><span class="sxs-lookup"><span data-stu-id="42f58-1143">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="42f58-1144">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="42f58-1144">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="42f58-1145">Korrigering för Get-AzAutomationDscNode när using -Name returnerar alla noder.</span><span class="sxs-lookup"><span data-stu-id="42f58-1145">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="42f58-1146">Nu returnerar den endast den matchande noden.</span><span class="sxs-lookup"><span data-stu-id="42f58-1146">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="42f58-1147">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="42f58-1147">Az.Compute</span></span>
* <span data-ttu-id="42f58-1148">Lägg till parametrarna ProtectFromScaleIn och ProtectFromScaleSetAction i cmdleten Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="42f58-1148">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="42f58-1149">Nu är standardinställningen att vimpelparametern New-AzVM använder en tillgänglig plats om USA, östra inte stöds</span><span class="sxs-lookup"><span data-stu-id="42f58-1149">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="42f58-1150">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="42f58-1150">Az.DataLakeStore</span></span>
* <span data-ttu-id="42f58-1151">Uppdatera ADLS-sdk för att använda httpclient, integrera dataplanstestning med Azure-ramverk</span><span class="sxs-lookup"><span data-stu-id="42f58-1151">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="42f58-1152">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="42f58-1152">Az.Monitor</span></span>
* <span data-ttu-id="42f58-1153">Korrigera felaktiga parameternamn i hjälpexempel</span><span class="sxs-lookup"><span data-stu-id="42f58-1153">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="42f58-1154">Az.Network</span><span class="sxs-lookup"><span data-stu-id="42f58-1154">Az.Network</span></span>
* <span data-ttu-id="42f58-1155">Lägg till flaggan DisableBgpRoutePropagation i utdata för effektiv routningstabell</span><span class="sxs-lookup"><span data-stu-id="42f58-1155">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="42f58-1156">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="42f58-1156">Updated cmdlet:</span></span>
        - <span data-ttu-id="42f58-1157">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="42f58-1157">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="42f58-1158">Åtgärda dubbelstreck i dokumentationen New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="42f58-1158">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="42f58-1159">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="42f58-1159">Az.Resources</span></span>
* <span data-ttu-id="42f58-1160">Lägg till ny cmdlet Get-AzureRmDenyAssignment för att hämta tilldelningsnekanden</span><span class="sxs-lookup"><span data-stu-id="42f58-1160">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="42f58-1161">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="42f58-1161">Az.Sql</span></span>
* <span data-ttu-id="42f58-1162">Döp om Advanced Threat Protection-cmdletar för Advanced Data Security och aktivera Vulnerability Assessment som standard</span><span class="sxs-lookup"><span data-stu-id="42f58-1162">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="42f58-1163">2.0.0 – maj 2019</span><span class="sxs-lookup"><span data-stu-id="42f58-1163">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="42f58-1164">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="42f58-1164">Az.Accounts</span></span>
* <span data-ttu-id="42f58-1165">Uppdatera autentiseringsbiblioteket för att åtgärda ADFS-problem med autentisering av användarnamn/lösenord</span><span class="sxs-lookup"><span data-stu-id="42f58-1165">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="42f58-1166">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="42f58-1166">Az.CognitiveServices</span></span>
* <span data-ttu-id="42f58-1167">Visa endast Bing-ansvarsfriskrivning för Bing-sökningstjänster.</span><span class="sxs-lookup"><span data-stu-id="42f58-1167">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="42f58-1168">Förbättra felmeddelande när det inte går att skapa konton.</span><span class="sxs-lookup"><span data-stu-id="42f58-1168">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="42f58-1169">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="42f58-1169">Az.Compute</span></span>
* <span data-ttu-id="42f58-1170">Funktion för närhetsplaceringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="42f58-1170">Proximity placement group feature.</span></span>
    - <span data-ttu-id="42f58-1171">Följande nya cmdletar har lagts till:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="42f58-1171">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="42f58-1172">Den nya parametern ProximityPlacementGroupId har lagts till i följande cmdletar:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="42f58-1172">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="42f58-1173">Parametern StorageAccountType har lagts till i New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="42f58-1173">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="42f58-1174">TargetRegion för New-AzGalleryImageVersion kan innehålla StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="42f58-1174">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="42f58-1175">Växlingsparametern SkipShutdown har lagts till i Stop-AzVM och Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="42f58-1175">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="42f58-1176">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="42f58-1176">Breaking changes</span></span>
    - <span data-ttu-id="42f58-1177">Set-AzVMBootDiagnostics har ändrats till Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="42f58-1177">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="42f58-1178">Export-AzLogAnalyticThrottledRequests har ändrats till Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="42f58-1178">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="42f58-1179">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="42f58-1179">Az.DeploymentManager</span></span>
* <span data-ttu-id="42f58-1180">De första allmänt tillgängliga versionerna av cmdletar för Distributionshanteraren i Azure</span><span class="sxs-lookup"><span data-stu-id="42f58-1180">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="42f58-1181">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="42f58-1181">Az.Dns</span></span>
* <span data-ttu-id="42f58-1182">Automatisk delegering av DNS för NameServer</span><span class="sxs-lookup"><span data-stu-id="42f58-1182">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="42f58-1183">Det överordnade zonnamnet kan användas som ytterligare valfri parameter i cmdleten för att skapa DNS-zoner.</span><span class="sxs-lookup"><span data-stu-id="42f58-1183">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="42f58-1184">Lägger till NS-poster för en nyligen skapad underordnad zon i den överordnade zonen.</span><span class="sxs-lookup"><span data-stu-id="42f58-1184">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="42f58-1185">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="42f58-1185">Az.FrontDoor</span></span>
* <span data-ttu-id="42f58-1186">De första allmänt tillgängliga versionerna av cmdletar för Azure FrontDoor</span><span class="sxs-lookup"><span data-stu-id="42f58-1186">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="42f58-1187">Byt namn på WAF-cmdletar så att de omfattar ”Waf”</span><span class="sxs-lookup"><span data-stu-id="42f58-1187">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="42f58-1188">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="42f58-1188">Az.HDInsight</span></span>
* <span data-ttu-id="42f58-1189">Två cmdletar har tagits bort:</span><span class="sxs-lookup"><span data-stu-id="42f58-1189">Removed two cmdlets:</span></span>
    - <span data-ttu-id="42f58-1190">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="42f58-1190">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="42f58-1191">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="42f58-1191">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="42f58-1192">En ny cmdlet har lagts till, Set-AzHDInsightGatewayCredential, som ersätter Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="42f58-1192">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="42f58-1193">Uppdatera cmdleten Get-AzHDInsightJobOutput för att skilja mellan läsarrollen och HDInsight-operatörsrollen:</span><span class="sxs-lookup"><span data-stu-id="42f58-1193">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="42f58-1194">Användare med läsarrollen måste uttryckligen ange parametern ”DefaultStorageAccountKey”, annars uppstår fel.</span><span class="sxs-lookup"><span data-stu-id="42f58-1194">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="42f58-1195">Användare med HDInsight-operatörsrollen påverkas inte.</span><span class="sxs-lookup"><span data-stu-id="42f58-1195">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="42f58-1196">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="42f58-1196">Az.Monitor</span></span>
* <span data-ttu-id="42f58-1197">Nya cmdletar för SQR API (schemalagd frågeregel)</span><span class="sxs-lookup"><span data-stu-id="42f58-1197">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="42f58-1198">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="42f58-1198">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="42f58-1199">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="42f58-1199">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="42f58-1200">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="42f58-1200">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="42f58-1201">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="42f58-1201">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="42f58-1202">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="42f58-1202">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="42f58-1203">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="42f58-1203">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="42f58-1204">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="42f58-1204">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="42f58-1205">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="42f58-1205">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="42f58-1206">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="42f58-1206">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="42f58-1207">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="42f58-1207">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="42f58-1208">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="42f58-1208">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="42f58-1209">[Mer](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information om SQR API</span><span class="sxs-lookup"><span data-stu-id="42f58-1209">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="42f58-1210">Az.Monitor.md har uppdaterats för att omfatta cmdletar för måttbaserade aviseringsregler i GenV2 (inte klassiska)</span><span class="sxs-lookup"><span data-stu-id="42f58-1210">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="42f58-1211">Az.Network</span><span class="sxs-lookup"><span data-stu-id="42f58-1211">Az.Network</span></span>
* <span data-ttu-id="42f58-1212">Lägg till stöd för NAT Gateway-resurs</span><span class="sxs-lookup"><span data-stu-id="42f58-1212">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="42f58-1213">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="42f58-1213">New cmdlets</span></span>
        - <span data-ttu-id="42f58-1214">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="42f58-1214">New-AzNatGateway</span></span>
        - <span data-ttu-id="42f58-1215">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="42f58-1215">Get-AzNatGateway</span></span>
        - <span data-ttu-id="42f58-1216">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="42f58-1216">Set-AzNatGateway</span></span>
        - <span data-ttu-id="42f58-1217">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="42f58-1217">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="42f58-1218">Uppdaterade cmdletar</span><span class="sxs-lookup"><span data-stu-id="42f58-1218">Updated cmdlets</span></span>
        - <span data-ttu-id="42f58-1219">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="42f58-1219">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="42f58-1220">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="42f58-1220">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="42f58-1221">Nedanstående kommandon för funktionen har uppdaterats: Ange/ta bort anpassade vägar på Brooklyn Gateway.</span><span class="sxs-lookup"><span data-stu-id="42f58-1221">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="42f58-1222">New-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ställa in adressprefix som anpassade vägar för att ange gateway.</span><span class="sxs-lookup"><span data-stu-id="42f58-1222">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="42f58-1223">Set-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ange adressprefix som anpassade vägar för att ange gateway.</span><span class="sxs-lookup"><span data-stu-id="42f58-1223">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="42f58-1224">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="42f58-1224">Az.PolicyInsights</span></span>
* <span data-ttu-id="42f58-1225">Stöd för att fråga efter information om principutvärdering.</span><span class="sxs-lookup"><span data-stu-id="42f58-1225">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="42f58-1226">Lägg till parametern ”-Expand” för Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="42f58-1226">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="42f58-1227">Stöd för -Expand PolicyEvaluationDetails.</span><span class="sxs-lookup"><span data-stu-id="42f58-1227">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="42f58-1228">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="42f58-1228">Az.RecoveryServices</span></span>
* <span data-ttu-id="42f58-1229">Stöd för att dela prenumeration mellan Azure och Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="42f58-1229">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="42f58-1230">Markering av kommande icke-bakåtkompatibla ändringar för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="42f58-1230">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="42f58-1231">Korrigering för återställningsplan och åtgärdsplan i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="42f58-1231">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="42f58-1232">Korrigering för mappning av uppdateringsnätverk i Azure Site Recovery för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="42f58-1232">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="42f58-1233">Korrigering för instruktioner för uppdateringsskydd i Azure Site Recovery för Azure till Azure för hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="42f58-1233">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="42f58-1234">Andra mindre korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="42f58-1234">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="42f58-1235">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="42f58-1235">Az.Relay</span></span>
* <span data-ttu-id="42f58-1236">Korrigera stavfel i kundriktade meddelanden</span><span class="sxs-lookup"><span data-stu-id="42f58-1236">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="42f58-1237">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="42f58-1237">Az.ServiceBus</span></span>
* <span data-ttu-id="42f58-1238">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="42f58-1238">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="42f58-1239">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="42f58-1239">Az.Storage</span></span>
* <span data-ttu-id="42f58-1240">Uppgradera till lagringsklientbiblioteket 10.0.1 (namnområdet för alla objekt från detta SDK ändras från ”Microsoft.WindowsAzure.Storage. *till ”Microsoft.Azure.Storage.* ”)</span><span class="sxs-lookup"><span data-stu-id="42f58-1240">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="42f58-1241">Uppgradera till Microsoft.Azure.Management.Storage 11.0.0 för att stödja den nya API-versionen 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="42f58-1241">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="42f58-1242">Standardlagringskontot i Skapa lagringskonto ändras från ”Storage” till ”StorageV2”</span><span class="sxs-lookup"><span data-stu-id="42f58-1242">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="42f58-1243">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="42f58-1243">New-AzStorageAccount</span></span>
* <span data-ttu-id="42f58-1244">Ändra lagringskontots cmdlet-utdata Sku.Name för att passa med indata-SkuName genom att lägga till ”-”. Till exempel ändras ”StandardLRS” till ”Standard_LRS”</span><span class="sxs-lookup"><span data-stu-id="42f58-1244">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="42f58-1245">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="42f58-1245">New-AzStorageAccount</span></span>
    - <span data-ttu-id="42f58-1246">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="42f58-1246">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="42f58-1247">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="42f58-1247">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="42f58-1248">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="42f58-1248">Az.Websites</span></span>
* <span data-ttu-id="42f58-1249">Egenskapen ”typ” konfigureras nu för PSSite-objekt som returneras av Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="42f58-1249">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="42f58-1250">Get-AzWebApp\*Metrics och Get-AzAppServicePlanMetrics markeras som inaktuella</span><span class="sxs-lookup"><span data-stu-id="42f58-1250">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="42f58-1251">1.8.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="42f58-1251">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="42f58-1252">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="42f58-1252">Highlights since the last major release</span></span>
* <span data-ttu-id="42f58-1253">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="42f58-1253">General availability of `Az` module</span></span>
* <span data-ttu-id="42f58-1254">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="42f58-1254">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="42f58-1255">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="42f58-1255">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="42f58-1256">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="42f58-1256">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="42f58-1257">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="42f58-1257">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="42f58-1258">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="42f58-1258">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="42f58-1259">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="42f58-1259">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="42f58-1260">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="42f58-1260">Az.Accounts</span></span>
* <span data-ttu-id="42f58-1261">Uppdatera Uninstall-AzureRm för att ta bort moduler i Mac på ett korrekt sätt</span><span class="sxs-lookup"><span data-stu-id="42f58-1261">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="42f58-1262">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="42f58-1262">Az.Batch</span></span>
* <span data-ttu-id="42f58-1263">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="42f58-1263">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="42f58-1264">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="42f58-1264">Az.Cdn</span></span>
* <span data-ttu-id="42f58-1265">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="42f58-1265">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="42f58-1266">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="42f58-1266">Az.CognitiveServices</span></span>
* <span data-ttu-id="42f58-1267">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="42f58-1267">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="42f58-1268">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="42f58-1268">Az.Compute</span></span>
* <span data-ttu-id="42f58-1269">Åtgärda problem med AEM-installationen om resurs-ID:n för diskar innehåller resourcegroups i gemener i resurs-ID:n</span><span class="sxs-lookup"><span data-stu-id="42f58-1269">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="42f58-1270">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="42f58-1270">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="42f58-1271">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="42f58-1271">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="42f58-1272">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="42f58-1272">Az.DataFactory</span></span>
* <span data-ttu-id="42f58-1273">Lägg till SsisProperties om NodeCount inte är null för hanterad integreringskörning.</span><span class="sxs-lookup"><span data-stu-id="42f58-1273">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="42f58-1274">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="42f58-1274">Az.DataLakeStore</span></span>
* <span data-ttu-id="42f58-1275">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="42f58-1275">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="42f58-1276">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="42f58-1276">Az.EventGrid</span></span>
* <span data-ttu-id="42f58-1277">Hjälptexten för slutpunkten har uppdaterats för att visa att resurser ska skapas innan cmdletarna för att skapa/uppdatera händelseprenumerationer används.</span><span class="sxs-lookup"><span data-stu-id="42f58-1277">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="42f58-1278">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="42f58-1278">Az.EventHub</span></span>
* <span data-ttu-id="42f58-1279">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="42f58-1279">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="42f58-1280">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="42f58-1280">Az.HDInsight</span></span>
* <span data-ttu-id="42f58-1281">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="42f58-1281">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="42f58-1282">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="42f58-1282">Az.IotHub</span></span>
* <span data-ttu-id="42f58-1283">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="42f58-1283">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="42f58-1284">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="42f58-1284">Az.KeyVault</span></span>
* <span data-ttu-id="42f58-1285">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="42f58-1285">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="42f58-1286">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="42f58-1286">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="42f58-1287">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="42f58-1287">Az.MachineLearning</span></span>
* <span data-ttu-id="42f58-1288">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="42f58-1288">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="42f58-1289">Az.Media</span><span class="sxs-lookup"><span data-stu-id="42f58-1289">Az.Media</span></span>
* <span data-ttu-id="42f58-1290">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="42f58-1290">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="42f58-1291">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="42f58-1291">Az.Monitor</span></span>
  * <span data-ttu-id="42f58-1292">Nya cmdletar för måttbaserad aviseringsregel i GenV2 (inte klassisk)</span><span class="sxs-lookup"><span data-stu-id="42f58-1292">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="42f58-1293">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="42f58-1293">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="42f58-1294">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="42f58-1294">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="42f58-1295">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="42f58-1295">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="42f58-1296">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="42f58-1296">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="42f58-1297">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="42f58-1297">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="42f58-1298">Monitor SDK har uppdaterats till version 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="42f58-1298">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="42f58-1299">Az.Network</span><span class="sxs-lookup"><span data-stu-id="42f58-1299">Az.Network</span></span>
* <span data-ttu-id="42f58-1300">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="42f58-1300">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="42f58-1301">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="42f58-1301">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="42f58-1302">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="42f58-1302">Az.NotificationHubs</span></span>
* <span data-ttu-id="42f58-1303">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="42f58-1303">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="42f58-1304">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="42f58-1304">Az.OperationalInsights</span></span>
* <span data-ttu-id="42f58-1305">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="42f58-1305">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="42f58-1306">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="42f58-1306">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="42f58-1307">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="42f58-1307">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="42f58-1308">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="42f58-1308">Az.RecoveryServices</span></span>
* <span data-ttu-id="42f58-1309">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="42f58-1309">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="42f58-1310">Tabellformatet för SQL i virtuella Azure-datorer har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="42f58-1310">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="42f58-1311">En alternativ metod för att hämta platser i AzureFileShare har lagts till</span><span class="sxs-lookup"><span data-stu-id="42f58-1311">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="42f58-1312">ScheduleRunDays i SchedulePolicy-objekt har uppdaterats enligt tidszon</span><span class="sxs-lookup"><span data-stu-id="42f58-1312">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="42f58-1313">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="42f58-1313">Az.RedisCache</span></span>
* <span data-ttu-id="42f58-1314">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="42f58-1314">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="42f58-1315">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="42f58-1315">Az.Resources</span></span>
* <span data-ttu-id="42f58-1316">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="42f58-1316">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="42f58-1317">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="42f58-1317">Az.Sql</span></span>
* <span data-ttu-id="42f58-1318">Ersätt Monitor SDK-beroende med vanlig kod</span><span class="sxs-lookup"><span data-stu-id="42f58-1318">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="42f58-1319">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="42f58-1319">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="42f58-1320">Förbättrad process för klassificering av flera kolumner.</span><span class="sxs-lookup"><span data-stu-id="42f58-1320">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="42f58-1321">Inkludera SKU-egenskaper (SKU-namn, serie, kapacitet) i svaret från Get-AzSqlServerServiceObjective och formatera som tabell som standard.</span><span class="sxs-lookup"><span data-stu-id="42f58-1321">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="42f58-1322">Möjlighet att använda Get-AzSqlServerServiceObjective efter plats utan att behöva en redan befintlig server i regionen.</span><span class="sxs-lookup"><span data-stu-id="42f58-1322">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="42f58-1323">Stöd för tidszonsparametern när hanterade instanser skapas.</span><span class="sxs-lookup"><span data-stu-id="42f58-1323">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="42f58-1324">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="42f58-1324">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="42f58-1325">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="42f58-1325">Az.Websites</span></span>
* <span data-ttu-id="42f58-1326">åtgärdar Set-AzWebApp och Set-AzWebAppSlot så att de inte tar bort taggar vid körning</span><span class="sxs-lookup"><span data-stu-id="42f58-1326">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="42f58-1327">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="42f58-1327">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="42f58-1328">SDK för WebSites har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="42f58-1328">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="42f58-1329">Egenskapen AdminSiteName har tagits bort från PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="42f58-1329">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="42f58-1330">1.7.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="42f58-1330">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="42f58-1331">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="42f58-1331">Highlights since the last major release</span></span>
* <span data-ttu-id="42f58-1332">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="42f58-1332">General availability of `Az` module</span></span>
* <span data-ttu-id="42f58-1333">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="42f58-1333">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="42f58-1334">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="42f58-1334">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="42f58-1335">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="42f58-1335">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="42f58-1336">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="42f58-1336">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="42f58-1337">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="42f58-1337">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="42f58-1338">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="42f58-1338">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="42f58-1339">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="42f58-1339">Az.Accounts</span></span>
* <span data-ttu-id="42f58-1340">Add-AzEnvironment och Set-AzEnvironment har uppdaterats för att godkänna parametern AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="42f58-1340">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="42f58-1341">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="42f58-1341">Az.AnalysisServices</span></span>
* <span data-ttu-id="42f58-1342">ServiceClient används i cmdletar för dataplan och den ursprungliga autentiseringslogiken har tagits bort</span><span class="sxs-lookup"><span data-stu-id="42f58-1342">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="42f58-1343">Add-AzureASAccount används för omslutning av Connect-AzAccount för att undvika en icke-bakåtkompatibel ändring</span><span class="sxs-lookup"><span data-stu-id="42f58-1343">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="42f58-1344">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="42f58-1344">Az.Automation</span></span>
* <span data-ttu-id="42f58-1345">Buggen för cmdleten New-AzAutomationSoftwareUpdateConfiguration för inkluderingar har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="42f58-1345">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="42f58-1346">Nu bör parametern IncludedKbNumber och IncludedPackageNameMask fungera.</span><span class="sxs-lookup"><span data-stu-id="42f58-1346">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="42f58-1347">Felkorrigering för dynamiska grupper i uppdateringshanteringen för azure automation</span><span class="sxs-lookup"><span data-stu-id="42f58-1347">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="42f58-1348">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="42f58-1348">Az.Compute</span></span>
* <span data-ttu-id="42f58-1349">Lägg till parametern HyperVGeneration i New-AzDiskConfig och New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="42f58-1349">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="42f58-1350">Tillåt att virtuella datorer skapas med galleribilder från andra klientorganisationer.</span><span class="sxs-lookup"><span data-stu-id="42f58-1350">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="42f58-1351">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="42f58-1351">Az.ContainerInstance</span></span>
* <span data-ttu-id="42f58-1352">Ett problem har åtgärdats i parametern -Command för New-AzContainerGroup som lade till ett avslutande tomt argument</span><span class="sxs-lookup"><span data-stu-id="42f58-1352">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="42f58-1353">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="42f58-1353">Az.DataFactory</span></span>
* <span data-ttu-id="42f58-1354">ADF .Net SDK-versionen har uppdaterats till 3.0.2</span><span class="sxs-lookup"><span data-stu-id="42f58-1354">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="42f58-1355">Cmdleten Set-AzDataFactoryV2 har uppdaterats med extra parametrar för inställningar som rör RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="42f58-1355">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="42f58-1356">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="42f58-1356">Az.Resources</span></span>
* <span data-ttu-id="42f58-1357">Förbättra hanteringen av providrar för Get-AzResource när parametrarna -ResourceId eller -ResourceGroupName, -Name och -ResourceType tillhandahålls</span><span class="sxs-lookup"><span data-stu-id="42f58-1357">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="42f58-1358">Förbättra felhanteringen för ”Test-AzDeployment” och ”Test-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="42f58-1358">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="42f58-1359">Hantera fel utanför distributionsvalideringen och ta med dem i kommandoutdata istället</span><span class="sxs-lookup"><span data-stu-id="42f58-1359">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="42f58-1360">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="42f58-1360">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="42f58-1361">Lägg till växlingsparametern -IgnoreDynamicParameters till en uppsättning av cmdletar för distribution för att hoppa över fråga i skript och jobbscenarier</span><span class="sxs-lookup"><span data-stu-id="42f58-1361">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="42f58-1362">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="42f58-1362">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="42f58-1363">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="42f58-1363">Az.Sql</span></span>
* <span data-ttu-id="42f58-1364">Stöd för dataklassificering av databaser.</span><span class="sxs-lookup"><span data-stu-id="42f58-1364">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="42f58-1365">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="42f58-1365">Az.Storage</span></span>
* <span data-ttu-id="42f58-1366">Rapportera detaljfel när lagringskontext skapas med parametern -UseConnectedAccount, men utan inloggning på Azure-kontot</span><span class="sxs-lookup"><span data-stu-id="42f58-1366">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="42f58-1367">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="42f58-1367">New-AzStorageContext</span></span>
* <span data-ttu-id="42f58-1368">Stöd för att hantera Blob Service-egenskaper för ett angivet lagringskonto med API:et för hanteringsplan</span><span class="sxs-lookup"><span data-stu-id="42f58-1368">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="42f58-1369">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="42f58-1369">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="42f58-1370">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="42f58-1370">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="42f58-1371">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="42f58-1371">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="42f58-1372">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="42f58-1372">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="42f58-1373">Stöd för -AsJob-cmdletar för att ladda upp och ladda ned blobar och filer</span><span class="sxs-lookup"><span data-stu-id="42f58-1373">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="42f58-1374">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="42f58-1374">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="42f58-1375">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="42f58-1375">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="42f58-1376">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="42f58-1376">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="42f58-1377">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="42f58-1377">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="42f58-1378">1.6.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="42f58-1378">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="42f58-1379">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="42f58-1379">Highlights since the last major release</span></span>
* <span data-ttu-id="42f58-1380">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="42f58-1380">General availability of `Az` module</span></span>
* <span data-ttu-id="42f58-1381">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="42f58-1381">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="42f58-1382">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="42f58-1382">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="42f58-1383">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="42f58-1383">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="42f58-1384">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="42f58-1384">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="42f58-1385">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="42f58-1385">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="42f58-1386">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="42f58-1386">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="42f58-1387">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="42f58-1387">Az.Automation</span></span>
* <span data-ttu-id="42f58-1388">Azure Automation – ändring av uppdateringshantering för stöd för de nya funktionerna:</span><span class="sxs-lookup"><span data-stu-id="42f58-1388">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="42f58-1389">Dynamisk gruppering</span><span class="sxs-lookup"><span data-stu-id="42f58-1389">Dynamic grouping</span></span>
    * <span data-ttu-id="42f58-1390">För-/efterskrift</span><span class="sxs-lookup"><span data-stu-id="42f58-1390">Pre-Post script</span></span>
    * <span data-ttu-id="42f58-1391">Inställning för omstart</span><span class="sxs-lookup"><span data-stu-id="42f58-1391">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="42f58-1392">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="42f58-1392">Az.Compute</span></span>
* <span data-ttu-id="42f58-1393">Åtgärda problem med sökvägsmatchning i Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="42f58-1393">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="42f58-1394">Uppdatera Compute-klientbibliotek till 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="42f58-1394">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="42f58-1395">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="42f58-1395">Az.KeyVault</span></span>
* <span data-ttu-id="42f58-1396">Stöd för jokertecken för KeyVault-cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="42f58-1396">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="42f58-1397">Az.Network</span><span class="sxs-lookup"><span data-stu-id="42f58-1397">Az.Network</span></span>
* <span data-ttu-id="42f58-1398">Lägg till stöd för Threat Intelligence för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="42f58-1398">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="42f58-1399">Lägg till resurs för brandväggsprincip på översta nivå och anpassade regler för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="42f58-1399">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="42f58-1400">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="42f58-1400">Az.RecoveryServices</span></span>
* <span data-ttu-id="42f58-1401">SnapshotRetentionInDays har lagts till i Azure-principen för virtuella datorer för stöd av Instant RP</span><span class="sxs-lookup"><span data-stu-id="42f58-1401">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="42f58-1402">Pipe-stöd för avregistrering av container har lagts till</span><span class="sxs-lookup"><span data-stu-id="42f58-1402">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="42f58-1403">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="42f58-1403">Az.Resources</span></span>
* <span data-ttu-id="42f58-1404">Uppdatera stöd för jokertecken för Get-AzResource och Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="42f58-1404">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="42f58-1405">Uppdatera autentiseringsuppgifter som används vid allmänna anrop till ARM</span><span class="sxs-lookup"><span data-stu-id="42f58-1405">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="42f58-1406">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="42f58-1406">Az.Sql</span></span>
* <span data-ttu-id="42f58-1407">Cmdlet-parametern (ExcludeDetectionType) för Hotidentifiering ändrades från DetectionType till sträng[] för att framtidssäkra den när nya DetectionTypes läggs till, och även för att stödja automatisk ifyllning.</span><span class="sxs-lookup"><span data-stu-id="42f58-1407">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="42f58-1408">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="42f58-1408">Az.Storage</span></span>
* <span data-ttu-id="42f58-1409">Stöd för att hämta/ange/ta bort hanteringsprincip på ett lagringskonto</span><span class="sxs-lookup"><span data-stu-id="42f58-1409">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="42f58-1410">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="42f58-1410">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="42f58-1411">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="42f58-1411">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="42f58-1412">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="42f58-1412">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="42f58-1413">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="42f58-1413">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="42f58-1414">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="42f58-1414">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="42f58-1415">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="42f58-1415">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="42f58-1416">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="42f58-1416">Az.Websites</span></span>
* <span data-ttu-id="42f58-1417">Åtgärda fel med ARM-mall som avbryter kloning av alla platser med 'New-AzWebApp -IncludeSourceWebAppSlots'</span><span class="sxs-lookup"><span data-stu-id="42f58-1417">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="42f58-1418">1.5.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="42f58-1418">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="42f58-1419">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="42f58-1419">Az.Accounts</span></span>
* <span data-ttu-id="42f58-1420">Lägg till kommandot Register-AzModule för stöd för AutoRest-genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="42f58-1420">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="42f58-1421">Uppdatera exempel för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="42f58-1421">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="42f58-1422">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="42f58-1422">Az.Automation</span></span>
* <span data-ttu-id="42f58-1423">Problem med att hämta vissa månadsscheman i flera Azure Automation-cmdletar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="42f58-1423">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="42f58-1424">Åtgärda problem med att Get-AzAutomationDscNode bara returnerar de 20 översta noderna.</span><span class="sxs-lookup"><span data-stu-id="42f58-1424">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="42f58-1425">Nu returneras alla noder</span><span class="sxs-lookup"><span data-stu-id="42f58-1425">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="42f58-1426">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="42f58-1426">Az.Cdn</span></span>
* <span data-ttu-id="42f58-1427">Nya Powershell-cmdletar för att aktivera/inaktivera anpassade domän-HTTPS har lagts till och de gamla har gjorts inaktuella</span><span class="sxs-lookup"><span data-stu-id="42f58-1427">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="42f58-1428">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="42f58-1428">Az.Compute</span></span>
* <span data-ttu-id="42f58-1429">Lägg till stöd för jokertecken för Get-cmdletar</span><span class="sxs-lookup"><span data-stu-id="42f58-1429">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="42f58-1430">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="42f58-1430">Az.DataFactory</span></span>
* <span data-ttu-id="42f58-1431">ADF .Net SDK-versionen har uppdaterats till 3.0.1</span><span class="sxs-lookup"><span data-stu-id="42f58-1431">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="42f58-1432">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="42f58-1432">Az.LogicApp</span></span>
* <span data-ttu-id="42f58-1433">Åtgärda problemet med att ListWorkflows endast hämtar den första sidan med resultat</span><span class="sxs-lookup"><span data-stu-id="42f58-1433">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="42f58-1434">Az.Network</span><span class="sxs-lookup"><span data-stu-id="42f58-1434">Az.Network</span></span>
* <span data-ttu-id="42f58-1435">Lägg till stöd för jokertecken för Network-cmdletar</span><span class="sxs-lookup"><span data-stu-id="42f58-1435">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="42f58-1436">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="42f58-1436">Az.RecoveryServices</span></span>
* <span data-ttu-id="42f58-1437">Stöd har lagts till för SQL Server i virtuella Azure-datorer</span><span class="sxs-lookup"><span data-stu-id="42f58-1437">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="42f58-1438">SDK-uppdatering</span><span class="sxs-lookup"><span data-stu-id="42f58-1438">SDK Update</span></span>
* <span data-ttu-id="42f58-1439">Get-ProtectableItem-incheckning i VMappContainer har tagits bort</span><span class="sxs-lookup"><span data-stu-id="42f58-1439">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="42f58-1440">Name och ServerName har lagts till som parametrar för Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="42f58-1440">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="42f58-1441">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="42f58-1441">Az.Resources</span></span>
* <span data-ttu-id="42f58-1442">Lägg till parametern `-TemplateObject` i cmdletar för distribution</span><span class="sxs-lookup"><span data-stu-id="42f58-1442">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="42f58-1443">Mer information här: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="42f58-1443">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="42f58-1444">Åtgärda problem med piping av resultatet i `Get-AzResource` till `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="42f58-1444">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="42f58-1445">Mer information här: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="42f58-1445">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="42f58-1446">Åtgärda problem med ändring av JSON-datatyp när `Set-AzResource` körs</span><span class="sxs-lookup"><span data-stu-id="42f58-1446">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="42f58-1447">Mer information här: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="42f58-1447">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="42f58-1448">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="42f58-1448">Az.Sql</span></span>
* <span data-ttu-id="42f58-1449">AuditingEndpointsCommunicator uppdateras.</span><span class="sxs-lookup"><span data-stu-id="42f58-1449">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="42f58-1450">Åtgärdar beteendet hos ett gränsscenario när nya diagnostikinställningar skapas.</span><span class="sxs-lookup"><span data-stu-id="42f58-1450">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="42f58-1451">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="42f58-1451">Az.Storage</span></span>
* <span data-ttu-id="42f58-1452">Stöd för BlockBlobStorage när Storage-konto skapas      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="42f58-1452">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="42f58-1453">1.4.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="42f58-1453">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="42f58-1454">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="42f58-1454">Az.AnalysisServices</span></span>
* <span data-ttu-id="42f58-1455">Inaktuell AddAzureASAccount-cmdlet</span><span class="sxs-lookup"><span data-stu-id="42f58-1455">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="42f58-1456">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="42f58-1456">Az.Automation</span></span>
* <span data-ttu-id="42f58-1457">Hjälpen för Import-AzAutomationDscNodeConfiguration har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="42f58-1457">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="42f58-1458">Konfigurationsnamnsvalidering har lagts till i cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="42f58-1458">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="42f58-1459">Förbättrad felhantering för cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="42f58-1459">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="42f58-1460">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="42f58-1460">Az.CognitiveServices</span></span>
* <span data-ttu-id="42f58-1461">CustomSubdomainName har lagts till som en ny valfri parameter för New-AzCognitiveServicesAccount, som används för att ange underdomän för resursen.</span><span class="sxs-lookup"><span data-stu-id="42f58-1461">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="42f58-1462">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="42f58-1462">Az.Compute</span></span>
* <span data-ttu-id="42f58-1463">Problemet med ID-parameteruppsättningar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="42f58-1463">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="42f58-1464">Get-AzVMExtension har uppdaterats så att alla installerade tillägg visas om parametern Name inte har angetts</span><span class="sxs-lookup"><span data-stu-id="42f58-1464">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="42f58-1465">Parametrarna Tag och ResourceId har lagts till i cmdleten Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="42f58-1465">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="42f58-1466">Get-AzVmssVM utan instans-ID och med InstanceView kan visa virtuella VMSS-datorer med instansvyn.</span><span class="sxs-lookup"><span data-stu-id="42f58-1466">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="42f58-1467">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="42f58-1467">Az.DataLakeStore</span></span>
* <span data-ttu-id="42f58-1468">Cmdletar har lagts till för uppräkning och återställning av borttagna objekt i ADL</span><span class="sxs-lookup"><span data-stu-id="42f58-1468">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="42f58-1469">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="42f58-1469">Az.EventHub</span></span>
* <span data-ttu-id="42f58-1470">Ny boolesk egenskap SkipEmptyArchives har lagts till i Skip Empty Archives i CaptureDescription-klassen i Eventhub</span><span class="sxs-lookup"><span data-stu-id="42f58-1470">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="42f58-1471">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="42f58-1471">Az.KeyVault</span></span>
* <span data-ttu-id="42f58-1472">Taggning i Set-AzKeyVaultSecret har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="42f58-1472">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="42f58-1473">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="42f58-1473">Az.LogicApp</span></span>
* <span data-ttu-id="42f58-1474">Grundläggande SKU har lagts till för Integrationskonton</span><span class="sxs-lookup"><span data-stu-id="42f58-1474">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="42f58-1475">XSLT 2.0, XSLT 3.0 och Flytande mappningstyper har lagts till</span><span class="sxs-lookup"><span data-stu-id="42f58-1475">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="42f58-1476">Nya cmdletar för integrationskontosammansättningar</span><span class="sxs-lookup"><span data-stu-id="42f58-1476">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="42f58-1477">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="42f58-1477">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="42f58-1478">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="42f58-1478">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="42f58-1479">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="42f58-1479">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="42f58-1480">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="42f58-1480">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="42f58-1481">Nya cmdletar för batchkonfiguration för integrationskonto</span><span class="sxs-lookup"><span data-stu-id="42f58-1481">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="42f58-1482">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="42f58-1482">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="42f58-1483">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="42f58-1483">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="42f58-1484">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="42f58-1484">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="42f58-1485">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="42f58-1485">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="42f58-1486">Logic App-SDK har uppdaterats till version 4.1.0</span><span class="sxs-lookup"><span data-stu-id="42f58-1486">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="42f58-1487">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="42f58-1487">Az.Monitor</span></span>
* <span data-ttu-id="42f58-1488">Hjälpen för Get-AzMetric har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="42f58-1488">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="42f58-1489">Az.Network</span><span class="sxs-lookup"><span data-stu-id="42f58-1489">Az.Network</span></span>
* <span data-ttu-id="42f58-1490">Hjälpexempel för Add-AzApplicationGatewayCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="42f58-1490">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="42f58-1491">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="42f58-1491">Az.OperationalInsights</span></span>
* <span data-ttu-id="42f58-1492">Ytterligare stöd för datakällorna New och Get ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="42f58-1492">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="42f58-1493">Ny ApplicationInsights-typ har lagts till för att ge stöd för ”Get specific” och ”Get all” för ApplicationInsights-datakällor för angiven arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="42f58-1493">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="42f58-1494">Cmdleten New-AzOperationalInsightsApplicationInsightsDataSource har lagts till för att skapa datakälla med angivna parametrar för Application Insights-resurs: subscription Id, resourceGroupName och name.</span><span class="sxs-lookup"><span data-stu-id="42f58-1494">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="42f58-1495">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="42f58-1495">Az.Resources</span></span>
* <span data-ttu-id="42f58-1496">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="42f58-1496">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="42f58-1497">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="42f58-1497">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="42f58-1498">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="42f58-1498">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="42f58-1499">Fel som gör att KeyCredentials inte kan skapas upprepade gånger har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="42f58-1499">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="42f58-1500">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="42f58-1500">Az.Sql</span></span>
* <span data-ttu-id="42f58-1501">Lägg till stöd för hyperskalanivån för SQL DB</span><span class="sxs-lookup"><span data-stu-id="42f58-1501">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="42f58-1502">Ett fel har åtgärdats där återställningen kunde misslyckas på grund av onödiga inställningsegenskaper i restore-förfrågan</span><span class="sxs-lookup"><span data-stu-id="42f58-1502">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="42f58-1503">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="42f58-1503">Az.Websites</span></span>
* <span data-ttu-id="42f58-1504">Rätt exempel i Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="42f58-1504">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="42f58-1505">1.3.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="42f58-1505">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="42f58-1506">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="42f58-1506">Az.Accounts</span></span>
* <span data-ttu-id="42f58-1507">Uppdatera till den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="42f58-1507">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="42f58-1508">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="42f58-1508">Az.AnalysisServices</span></span>
<span data-ttu-id="42f58-1509">Allmän tillgänglighet för Az.AnalysisServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="42f58-1509">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="42f58-1510">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="42f58-1510">Az.Compute</span></span>
* <span data-ttu-id="42f58-1511">AEM-tillägg: Lägg till stöd för UltraSSD-, P60-, P70- och P80-diskar</span><span class="sxs-lookup"><span data-stu-id="42f58-1511">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="42f58-1512">Uppdatera hjälpbeskrivning för Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="42f58-1512">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="42f58-1513">Uppdatera hjälpbeskrivning och exempel för Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="42f58-1513">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="42f58-1514">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="42f58-1514">Az.RecoveryServices</span></span>
<span data-ttu-id="42f58-1515">Allmän tillgänglighet för Az.RecoveryServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="42f58-1515">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="42f58-1516">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="42f58-1516">Az.Resources</span></span>
* <span data-ttu-id="42f58-1517">Korrigera taggar för resursgrupper</span><span class="sxs-lookup"><span data-stu-id="42f58-1517">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="42f58-1518">Mer information här: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="42f58-1518">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="42f58-1519">Åtgärda problem där `Get-AzureRmRoleAssignment` inte respekterar -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="42f58-1519">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="42f58-1520">Mer information här: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="42f58-1520">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="42f58-1521">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="42f58-1521">Az.Sql</span></span>
* <span data-ttu-id="42f58-1522">Lägga till Get/Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="42f58-1522">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="42f58-1523">Åtgärda problem där ett nullref-undantag uppstår när du kör SQL-cmdletar och inte är inloggad på ett Azure-konto</span><span class="sxs-lookup"><span data-stu-id="42f58-1523">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="42f58-1524">Åtgärda nullref-undantag i Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="42f58-1524">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="42f58-1525">1.2.1 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="42f58-1525">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="42f58-1526">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="42f58-1526">Az.Accounts</span></span>
* <span data-ttu-id="42f58-1527">Version med rätt version av autentisering</span><span class="sxs-lookup"><span data-stu-id="42f58-1527">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="42f58-1528">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="42f58-1528">Az.AnalysisServices</span></span>
* <span data-ttu-id="42f58-1529">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="42f58-1529">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="42f58-1530">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="42f58-1530">Az.RecoveryServices</span></span>
* <span data-ttu-id="42f58-1531">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="42f58-1531">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="42f58-1532">1.2.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="42f58-1532">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="42f58-1533">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="42f58-1533">Az.Accounts</span></span>
* <span data-ttu-id="42f58-1534">Lägga till interaktiv autentisering och autentisering med användarnamn/lösenord för endast Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="42f58-1534">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="42f58-1535">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="42f58-1535">Update incorrect online help URLs</span></span>
* <span data-ttu-id="42f58-1536">Lägga till varningsmeddelande i PS Core för Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="42f58-1536">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="42f58-1537">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="42f58-1537">Az.Aks</span></span>
* <span data-ttu-id="42f58-1538">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="42f58-1538">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="42f58-1539">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="42f58-1539">Az.Automation</span></span>
* <span data-ttu-id="42f58-1540">Stöd för Python 2-runbookflöden har lagts till</span><span class="sxs-lookup"><span data-stu-id="42f58-1540">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="42f58-1541">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="42f58-1541">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="42f58-1542">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="42f58-1542">Az.Cdn</span></span>
* <span data-ttu-id="42f58-1543">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="42f58-1543">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="42f58-1544">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="42f58-1544">Az.Compute</span></span>
* <span data-ttu-id="42f58-1545">Lägga till cmdleten Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="42f58-1545">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="42f58-1546">Lägga till TempDisk-parameter i Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="42f58-1546">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="42f58-1547">Korrigera varningsmeddelande för New-AzVM</span><span class="sxs-lookup"><span data-stu-id="42f58-1547">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="42f58-1548">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="42f58-1548">Az.ContainerRegistry</span></span>
* <span data-ttu-id="42f58-1549">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="42f58-1549">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="42f58-1550">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="42f58-1550">Az.DataFactory</span></span>
* <span data-ttu-id="42f58-1551">ADF .Net SDK-versionen har uppdaterats till 3.0.0</span><span class="sxs-lookup"><span data-stu-id="42f58-1551">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="42f58-1552">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="42f58-1552">Az.DataLakeStore</span></span>
* <span data-ttu-id="42f58-1553">Åtgärda problem med ADLS-slutpunkt vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="42f58-1553">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="42f58-1554">Mer information här: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="42f58-1554">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="42f58-1555">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="42f58-1555">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="42f58-1556">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="42f58-1556">Az.IotHub</span></span>
* <span data-ttu-id="42f58-1557">Lägga till kodningsformat i cmdleten Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="42f58-1557">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="42f58-1558">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="42f58-1558">Az.KeyVault</span></span>
* <span data-ttu-id="42f58-1559">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="42f58-1559">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="42f58-1560">Az.Network</span><span class="sxs-lookup"><span data-stu-id="42f58-1560">Az.Network</span></span>
* <span data-ttu-id="42f58-1561">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="42f58-1561">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="42f58-1562">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="42f58-1562">Az.Resources</span></span>
* <span data-ttu-id="42f58-1563">Åtgärda felaktiga exempel i referensdokumentationen ”New-AzADAppCredential” och ”New-AzADSpCredential”</span><span class="sxs-lookup"><span data-stu-id="42f58-1563">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="42f58-1564">Åtgärda problem där sökvägen för parametern ”-TemplateFile” inte omvandlas innan cmdletarna för distribution i resursgruppen körs</span><span class="sxs-lookup"><span data-stu-id="42f58-1564">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="42f58-1565">Az.Resources: Korrigera dokumentationen om standardvärdet för New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="42f58-1565">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="42f58-1566">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="42f58-1566">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="42f58-1567">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="42f58-1567">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="42f58-1568">Åtgärda formateringsproblemet med objektet ”PSResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="42f58-1568">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="42f58-1569">Mer information här: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="42f58-1569">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="42f58-1570">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="42f58-1570">Az.ServiceFabric</span></span>
* <span data-ttu-id="42f58-1571">Återställ när ett certifikat läggs till i en Virtual Machine Scale Sets-modell men ett undantag genereras. Detta har gjorts för att åtgärda följande fel: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="42f58-1571">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="42f58-1572">Korrigera några felmeddelanden.</span><span class="sxs-lookup"><span data-stu-id="42f58-1572">Fix some error messages.</span></span>
* <span data-ttu-id="42f58-1573">Korrigering av skapande av kluster med ARM-mall som är standard för New-AzServiceFabriCluster som inte fungerade med migrering till Az.</span><span class="sxs-lookup"><span data-stu-id="42f58-1573">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="42f58-1574">Korrigering av tilläggning av kluster/programcertifikat så att endast VM Scale Sets som motsvarar klustret läggs till genom att kontrollera ID för klustret i tillägget.</span><span class="sxs-lookup"><span data-stu-id="42f58-1574">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="42f58-1575">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="42f58-1575">Az.SignalR</span></span>
* <span data-ttu-id="42f58-1576">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="42f58-1576">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="42f58-1577">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="42f58-1577">Az.Sql</span></span>
* <span data-ttu-id="42f58-1578">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="42f58-1578">Update incorrect online help URLs</span></span>
* <span data-ttu-id="42f58-1579">Uppdaterad parameterbeskrivning för LicenseType-parameter med möjliga värden</span><span class="sxs-lookup"><span data-stu-id="42f58-1579">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="42f58-1580">Korrigering för att uppdatera hanterad instansidentitet som inte fungerar när det är den enda uppdaterade egenskapen</span><span class="sxs-lookup"><span data-stu-id="42f58-1580">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="42f58-1581">Stöd för anpassad sortering på hanterad instans</span><span class="sxs-lookup"><span data-stu-id="42f58-1581">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="42f58-1582">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="42f58-1582">Az.Storage</span></span>
* <span data-ttu-id="42f58-1583">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="42f58-1583">Update incorrect online help URLs</span></span>
* <span data-ttu-id="42f58-1584">Tillhandahåll detaljerat felmeddelande när en användare försöker hämta/konfigurera klassisk loggning/mått på ett Premium Storage-konto eftersom Premium Storage-kontot inte har stöd för klassisk loggning/mått.</span><span class="sxs-lookup"><span data-stu-id="42f58-1584">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="42f58-1585">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="42f58-1585">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="42f58-1586">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="42f58-1586">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="42f58-1587">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="42f58-1587">Az.TrafficManager</span></span>
* <span data-ttu-id="42f58-1588">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="42f58-1588">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="42f58-1589">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="42f58-1589">Az.Websites</span></span>
* <span data-ttu-id="42f58-1590">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="42f58-1590">Update incorrect online help URLs</span></span>
* <span data-ttu-id="42f58-1591">Korrigerar ”New-AzWebAppSSLBinding” så att certifikatet laddas upp till rätt resursgrupp och plats om appen finns i en ASE.</span><span class="sxs-lookup"><span data-stu-id="42f58-1591">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="42f58-1592">Korrigerar ”New-AzWebAppSSLBinding” så att taggarna inte skrivs över på en bindning av ett SSL-certifikat till en app</span><span class="sxs-lookup"><span data-stu-id="42f58-1592">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="42f58-1593">1.1.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="42f58-1593">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="42f58-1594">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="42f58-1594">Az.Accounts</span></span>
* <span data-ttu-id="42f58-1595">Lade till omfattningen ”Lokal” till Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="42f58-1595">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="42f58-1596">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="42f58-1596">Az.Compute</span></span>
* <span data-ttu-id="42f58-1597">Namn är nu valfritt i ID-parametern för Restart/Start/Stop/Remove/Set-AzVM och Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="42f58-1597">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="42f58-1598">Uppdaterade beskrivningen av ID i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="42f58-1598">Updated the description of ID in help files</span></span>
* <span data-ttu-id="42f58-1599">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="42f58-1599">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="42f58-1600">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="42f58-1600">Az.DataLakeStore</span></span>
* <span data-ttu-id="42f58-1601">Uppdatera sdk-versionen av dataplanet till 1.1.14 för SDK-korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="42f58-1601">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="42f58-1602">Korrigerade hanteringen av negativ accesstime och modificationtime för getfilestatus och liststatus; korrigera asynkront annulleringstoken</span><span class="sxs-lookup"><span data-stu-id="42f58-1602">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="42f58-1603">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="42f58-1603">Az.EventGrid</span></span>
* <span data-ttu-id="42f58-1604">Uppdaterat för användning av API-versionen 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="42f58-1604">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="42f58-1605">Uppdaterade följande cmdletar för att stödja nytt scenario i API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="42f58-1605">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="42f58-1606">New-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="42f58-1606">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="42f58-1607">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="42f58-1607">Event Time-To-Live,</span></span>
        - <span data-ttu-id="42f58-1608">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="42f58-1608">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="42f58-1609">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="42f58-1609">Dead letter endpoint.</span></span>
    - <span data-ttu-id="42f58-1610">Update-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="42f58-1610">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="42f58-1611">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="42f58-1611">Event Time-To-Live,</span></span>
        - <span data-ttu-id="42f58-1612">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="42f58-1612">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="42f58-1613">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="42f58-1613">Dead letter endpoint.</span></span>
* <span data-ttu-id="42f58-1614">Lade till nya enum-värden (storageQueue och hybridConnection) för alternativet EndpointType i cmdletarna New-AzureRmEventGridSubscription och Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="42f58-1614">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="42f58-1615">Visa varningsmeddelanden om skapande eller uppdatering av händelseprenumerationen förväntas medföra manuell åtgärd från användaren.</span><span class="sxs-lookup"><span data-stu-id="42f58-1615">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="42f58-1616">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="42f58-1616">Az.IotHub</span></span>
* <span data-ttu-id="42f58-1617">Har uppdaterats till den senaste versionen av SDK:n lotHub</span><span class="sxs-lookup"><span data-stu-id="42f58-1617">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="42f58-1618">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="42f58-1618">Az.LogicApp</span></span>
* <span data-ttu-id="42f58-1619">Get-AzLogicApp visar en lista över alla som inte har angivet namn</span><span class="sxs-lookup"><span data-stu-id="42f58-1619">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="42f58-1620">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="42f58-1620">Az.Resources</span></span>
* <span data-ttu-id="42f58-1621">Åtgärdade problem med parameteruppsättningen när parametrarna -ODataQuery och -ResourceId anges för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="42f58-1621">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="42f58-1622">Mer information här: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="42f58-1622">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="42f58-1623">Åtgärdade hantering av parametern -Custom i New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="42f58-1623">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="42f58-1624">Korrigerade stavfel i New-AzDeployment-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="42f58-1624">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="42f58-1625">Gjorde parametern -MailNickname obligatorisk för New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="42f58-1625">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="42f58-1626">Mer information här: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="42f58-1626">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="42f58-1627">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="42f58-1627">Az.SignalR</span></span>
* <span data-ttu-id="42f58-1628">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="42f58-1628">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="42f58-1629">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="42f58-1629">Az.Sql</span></span>
* <span data-ttu-id="42f58-1630">Konverterade lagringshanteringsklientens beroende av den normala SDK-implementeringen.</span><span class="sxs-lookup"><span data-stu-id="42f58-1630">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="42f58-1631">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="42f58-1631">Az.Storage</span></span>
* <span data-ttu-id="42f58-1632">Angav StorageAccountName för lagringskontext som det verkliga namnet på lagringskontot när det skapas med Sas Token, OAuth eller Anonymous</span><span class="sxs-lookup"><span data-stu-id="42f58-1632">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="42f58-1633">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="42f58-1633">New-AzStorageContext</span></span>
* <span data-ttu-id="42f58-1634">Skapade Sas Token för Blob Snapshot-objekt med parametern -FullUri, åtgärdade den returnerade URI:n så att den blir URI för ögonblicksbild</span><span class="sxs-lookup"><span data-stu-id="42f58-1634">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="42f58-1635">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="42f58-1635">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="42f58-1636">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="42f58-1636">Az.Websites</span></span>
* <span data-ttu-id="42f58-1637">Åtgärdade en bugg i datumparsningen i Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="42f58-1637">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="42f58-1638">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="42f58-1638">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="42f58-1639">1.0.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="42f58-1639">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="42f58-1640">Allmänt</span><span class="sxs-lookup"><span data-stu-id="42f58-1640">General</span></span>

- <span data-ttu-id="42f58-1641">Allmän tillgänglighet för Az-modulen</span><span class="sxs-lookup"><span data-stu-id="42f58-1641">General Availability of Az Module</span></span>
- <span data-ttu-id="42f58-1642">Onlinehjälp för varje modul</span><span class="sxs-lookup"><span data-stu-id="42f58-1642">Online help for each module</span></span>
- <span data-ttu-id="42f58-1643">Mer information och en översikt finns på [Az-informationssidan](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="42f58-1643">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="42f58-1644">Information om hur du migrerar från AzureRM finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="42f58-1644">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="42f58-1645">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="42f58-1645">Az.Accounts</span></span>
- <span data-ttu-id="42f58-1646">Har ändrats från Az.Profile</span><span class="sxs-lookup"><span data-stu-id="42f58-1646">Changed from Az.Profile</span></span>
- <span data-ttu-id="42f58-1647">Fasta tabellformat för profil- och kontexttyper</span><span class="sxs-lookup"><span data-stu-id="42f58-1647">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="42f58-1648">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="42f58-1648">Az.ApiManagement</span></span>
- <span data-ttu-id="42f58-1649">Korrigeringar för #7002</span><span class="sxs-lookup"><span data-stu-id="42f58-1649">Fixes for #7002</span></span>
- <span data-ttu-id="42f58-1650">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="42f58-1650">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="42f58-1651">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="42f58-1651">Az.Batch</span></span>
- <span data-ttu-id="42f58-1652">Lade till möjligheten att se vilken version av Azure Batch Node Agent som körs på var och en av de virtuella datorerna i en pool, via den nya egenskapen `NodeAgentInformation` på `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="42f58-1652">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="42f58-1653">Standarden `Caching` för `PSDataDisk` är nu `ReadWrite` i stället för `None`.</span><span class="sxs-lookup"><span data-stu-id="42f58-1653">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="42f58-1654">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="42f58-1654">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="42f58-1655">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="42f58-1655">Az.Billing</span></span>
- <span data-ttu-id="42f58-1656">Kombinerar cmdletarna för fakturering, förbrukning och UsageAggregates. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="42f58-1656">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="42f58-1657">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="42f58-1657">Az.CognitivServices</span></span>
- <span data-ttu-id="42f58-1658">Lade till kompletterare för SkuName och Typem som är tillgängliga i New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="42f58-1658">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="42f58-1659">Tog bort parameteruppsättningen GetSkusWithAccountParamSetName från Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="42f58-1659">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="42f58-1660">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="42f58-1660">Az.ContainerInstance</span></span>
- <span data-ttu-id="42f58-1661">Stöd för ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="42f58-1661">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="42f58-1662">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="42f58-1662">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="42f58-1663">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="42f58-1663">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="42f58-1664">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="42f58-1664">Az.DataLakeStore</span></span>
- <span data-ttu-id="42f58-1665">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="42f58-1665">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="42f58-1666">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="42f58-1666">Az.Monitor</span></span>
- <span data-ttu-id="42f58-1667">Döpte om Az.Insights till Az.Monitor och andra mindre icke-bakåtkompatibla ändringar. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="42f58-1667">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="42f58-1668">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="42f58-1668">Az.KeyVault</span></span>
- <span data-ttu-id="42f58-1669">Tog bort den inaktuella egenskapen PurgeDisabled från utdatatyper</span><span class="sxs-lookup"><span data-stu-id="42f58-1669">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="42f58-1670">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="42f58-1670">Az.MachineLearning</span></span>
- <span data-ttu-id="42f58-1671">Inkluderade cmdletarna från modulen Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="42f58-1671">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="42f58-1672">Az.Media</span><span class="sxs-lookup"><span data-stu-id="42f58-1672">Az.Media</span></span>
- <span data-ttu-id="42f58-1673">Tog bort inaktuella -Tags-alias från New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="42f58-1673">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="42f58-1674">Az.Network</span><span class="sxs-lookup"><span data-stu-id="42f58-1674">Az.Network</span></span>
<span data-ttu-id="42f58-1675">Stöd har lagts till för konfiguration av RewriteRuleSets i Application Gateway</span><span class="sxs-lookup"><span data-stu-id="42f58-1675">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="42f58-1676">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="42f58-1676">New cmdlets added:</span></span>
        - <span data-ttu-id="42f58-1677">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="42f58-1677">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="42f58-1678">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="42f58-1678">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="42f58-1679">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="42f58-1679">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="42f58-1680">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="42f58-1680">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="42f58-1681">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="42f58-1681">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="42f58-1682">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="42f58-1682">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="42f58-1683">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="42f58-1683">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="42f58-1684">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="42f58-1684">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="42f58-1685">Cmdletar har uppdaterats med den valfria parametern -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="42f58-1685">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="42f58-1686">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="42f58-1686">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="42f58-1687">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="42f58-1687">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="42f58-1688">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="42f58-1688">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="42f58-1689">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="42f58-1689">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="42f58-1690">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="42f58-1690">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="42f58-1691">New-AzureRmApplicationGatewayUrlPathMapConfig har lagt till KeyVault-stöd för Application Gateway med Identity.</span><span class="sxs-lookup"><span data-stu-id="42f58-1691">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="42f58-1692">Cmdletar har uppdaterats med den valfria parametern -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="42f58-1692">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="42f58-1693">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="42f58-1693">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="42f58-1694">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="42f58-1694">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="42f58-1695">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="42f58-1695">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="42f58-1696">Cmdleten New-AzApplicationGateway har uppdaterats med den valfria parametern -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="42f58-1696">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="42f58-1697">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="42f58-1697">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="42f58-1698">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="42f58-1698">Az.OperationalInsights</span></span>
- <span data-ttu-id="42f58-1699">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="42f58-1699">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="42f58-1700">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="42f58-1700">Az.Profile</span></span>
- <span data-ttu-id="42f58-1701">Modulnamnet har ändrats till Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="42f58-1701">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="42f58-1702">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="42f58-1702">Az.RecoveryServices</span></span>
- <span data-ttu-id="42f58-1703">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="42f58-1703">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="42f58-1704">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="42f58-1704">Az.Resources</span></span>
- <span data-ttu-id="42f58-1705">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="42f58-1705">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="42f58-1706">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="42f58-1706">Az.ServiceFabric</span></span>
- <span data-ttu-id="42f58-1707">Stöd för specificering av certifikat efter eget namn och tumavtryck</span><span class="sxs-lookup"><span data-stu-id="42f58-1707">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="42f58-1708">Information om fler icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="42f58-1708">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="42f58-1709">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="42f58-1709">Az.SIgnalR</span></span>
- <span data-ttu-id="42f58-1710">Allmän tillgänglighet för PowerShell-cmdletar för SIgnalR</span><span class="sxs-lookup"><span data-stu-id="42f58-1710">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="42f58-1711">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="42f58-1711">Az.Sql</span></span>
- <span data-ttu-id="42f58-1712">Lade till de nya identifieringstyperna Data_Exfiltration och Unsafe_Action i Threat Detection-cmdletar</span><span class="sxs-lookup"><span data-stu-id="42f58-1712">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="42f58-1713">Uppdaterade dokumentationsexempel för Sql Auditing-cmdletar</span><span class="sxs-lookup"><span data-stu-id="42f58-1713">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="42f58-1714">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="42f58-1714">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="42f58-1715">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="42f58-1715">Az.Storage</span></span>
- <span data-ttu-id="42f58-1716">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="42f58-1716">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="42f58-1717">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="42f58-1717">Az.Websites</span></span>
- <span data-ttu-id="42f58-1718">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="42f58-1718">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="42f58-1719">0.7.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="42f58-1719">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="42f58-1720">Allmänt</span><span class="sxs-lookup"><span data-stu-id="42f58-1720">General</span></span>

* <span data-ttu-id="42f58-1721">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="42f58-1721">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="42f58-1722">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="42f58-1722">Az.Compute</span></span>

* <span data-ttu-id="42f58-1723">Lade till stöd för UltraSSD och Galleriavbildningar i de enkla parameteruppsättningarna för `New-AzVm(ss)`-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="42f58-1723">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="42f58-1724">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="42f58-1724">Az.DataLakeStore</span></span>

* <span data-ttu-id="42f58-1725">Åtgärdade avslutande snedstreck i domänen för adls-konto</span><span class="sxs-lookup"><span data-stu-id="42f58-1725">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="42f58-1726">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="42f58-1726">Az.FrontDoor</span></span>

* <span data-ttu-id="42f58-1727">Brutna länkar korrigerades</span><span class="sxs-lookup"><span data-stu-id="42f58-1727">Fixed some broken links</span></span>
    - <span data-ttu-id="42f58-1728">I artiklarna New-AzureRmFrontDoor och Set-AzureRmFrontDoor artiklar korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="42f58-1728">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="42f58-1729">I artikeln New-AzureRmFrontDoorManagedRuleObject korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="42f58-1729">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="42f58-1730">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="42f58-1730">Az.RecoveryServices</span></span>

* <span data-ttu-id="42f58-1731">Lade till valideringar på klientsidan för Azure-filresurs med återställningsåtgärder.</span><span class="sxs-lookup"><span data-stu-id="42f58-1731">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="42f58-1732">Gjorde storageAccountName och storageAccountResourceGroupName valfritt för afs-återställning.</span><span class="sxs-lookup"><span data-stu-id="42f58-1732">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="42f58-1733">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="42f58-1733">Az.Resources</span></span>

* <span data-ttu-id="42f58-1734">Korrigering för https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="42f58-1734">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="42f58-1735">Uppdaterade Get-AzureRmRoleAssignment så att prenumerationsomfattningen används om den anges vid begäran om klassiska administratörer.</span><span class="sxs-lookup"><span data-stu-id="42f58-1735">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="42f58-1736">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="42f58-1736">Az.Sql</span></span>

* <span data-ttu-id="42f58-1737">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="42f58-1737">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="42f58-1738">Korrigerade ett problem med Get-AzureRmSqlDatabaseVulnerabilityAssessment med DotNet-kärna</span><span class="sxs-lookup"><span data-stu-id="42f58-1738">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="42f58-1739">Ändrade dokumentationen för hjälpmeddelanden som rör SQL Auditing-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="42f58-1739">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="42f58-1740">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="42f58-1740">Az.Storage</span></span>

* <span data-ttu-id="42f58-1741">Lade till -EnableHierarchicalNamespace i New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="42f58-1741">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="42f58-1742">Åtgärdade problemet med att cmdleten Copy File inte kunde återanvända källkontexten på målet om inte -DestContext angetts</span><span class="sxs-lookup"><span data-stu-id="42f58-1742">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="42f58-1743">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="42f58-1743">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="42f58-1744">Stöd för statisk webbplatskonfiguration</span><span class="sxs-lookup"><span data-stu-id="42f58-1744">Support Static Website configuration</span></span>
    - <span data-ttu-id="42f58-1745">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="42f58-1745">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="42f58-1746">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="42f58-1746">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="42f58-1747">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="42f58-1747">Az.Websites</span></span>

* <span data-ttu-id="42f58-1748">Set-AzureRmWebApp och Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="42f58-1748">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="42f58-1749">Ny parameter (-AzureStoragePath) har lagts till för att ange att Azure Storage-sökvägar ska monteras i containerappar i Windows och Linux.</span><span class="sxs-lookup"><span data-stu-id="42f58-1749">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="42f58-1750">Använder utdata från den nya cmdleten New-AzureRmWebAppAzureStoragePath som en parameter för att ange sökvägar för Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="42f58-1750">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="42f58-1751">0.6.1 – november 2018</span><span class="sxs-lookup"><span data-stu-id="42f58-1751">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="42f58-1752">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="42f58-1752">Az.ApiManagement</span></span>
* <span data-ttu-id="42f58-1753">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="42f58-1753">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="42f58-1754">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="42f58-1754">Az.Automation</span></span>
* <span data-ttu-id="42f58-1755">Swagger baserade Azure Automation-cmdletar</span><span class="sxs-lookup"><span data-stu-id="42f58-1755">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="42f58-1756">Cmdletar för Uppdateringshantering har lagts till</span><span class="sxs-lookup"><span data-stu-id="42f58-1756">Added Update Management cmdlets</span></span>
* <span data-ttu-id="42f58-1757">Cmdletar för källkontroll har lagts till</span><span class="sxs-lookup"><span data-stu-id="42f58-1757">Added Source Control cmdlets</span></span>
* <span data-ttu-id="42f58-1758">Remove-AzureRmAutomationHybridWorkerGroup-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="42f58-1758">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="42f58-1759">Kommandot för DSC-registreringsnod har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="42f58-1759">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="42f58-1760">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="42f58-1760">Az.Compute</span></span>
* <span data-ttu-id="42f58-1761">Problem med SystemAssigned-identitet har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="42f58-1761">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="42f58-1762">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="42f58-1762">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="42f58-1763">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="42f58-1763">Az.ContainerInstance</span></span>
* <span data-ttu-id="42f58-1764">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="42f58-1764">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="42f58-1765">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="42f58-1765">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="42f58-1766">uppdatera exempelbeskrivningen för marketplace-cmdletar</span><span class="sxs-lookup"><span data-stu-id="42f58-1766">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="42f58-1767">Az.Network</span><span class="sxs-lookup"><span data-stu-id="42f58-1767">Az.Network</span></span>
* <span data-ttu-id="42f58-1768">Cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomErreller Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="42f58-1768">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="42f58-1769">ICMP tillbaka till stöd för Azure Firewall-nätverksprotokoll har lagts till</span><span class="sxs-lookup"><span data-stu-id="42f58-1769">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="42f58-1770">Uppdatera cmdlet Test-AzureRmNetworkWatcherConnectivity, lägga till verifiering av mål-id, adress och port.</span><span class="sxs-lookup"><span data-stu-id="42f58-1770">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="42f58-1771">Åtgärda problem med minnesanvändning i VirtualNetwork-karta</span><span class="sxs-lookup"><span data-stu-id="42f58-1771">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="42f58-1772">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="42f58-1772">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="42f58-1773">Åtgärda för att ändra principen för en skyddad fildelning.</span><span class="sxs-lookup"><span data-stu-id="42f58-1773">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="42f58-1774">Tidszonsprincipen har konverterats till versaler.</span><span class="sxs-lookup"><span data-stu-id="42f58-1774">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="42f58-1775">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="42f58-1775">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="42f58-1776">Exempel i New-AzureRmRecoveryServicesAsrProtectableItem har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="42f58-1776">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="42f58-1777">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="42f58-1777">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="42f58-1778">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="42f58-1778">Az.Relay</span></span>
* <span data-ttu-id="42f58-1779">Valfri parameter -KeyValue till New-AzureRmRelayKey cmdlet har lagts till, vilket gör det möjligt för användare att tillhandahålla KeyValue.</span><span class="sxs-lookup"><span data-stu-id="42f58-1779">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="42f58-1780">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="42f58-1780">Az.Resources</span></span>
* <span data-ttu-id="42f58-1781">Uppdatera hjälpdokumentation för resursidentitet kopplad till parametrar i `New-AzureRmPolicyAssignment` och `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="42f58-1781">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="42f58-1782">Lägg till ett exempel för New-AzureRmPolicyDefinition som använder -Metadata</span><span class="sxs-lookup"><span data-stu-id="42f58-1782">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="42f58-1783">Korrigera så att skiftläge behålls i taggnycklar i NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="42f58-1783">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="42f58-1784">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="42f58-1784">Az.ServiceFabric</span></span>
* <span data-ttu-id="42f58-1785">Lägg till utfasningsmeddelanden för kommande icke-kompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="42f58-1785">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="42f58-1786">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="42f58-1786">Az.Sql</span></span>
* <span data-ttu-id="42f58-1787">Nya cmdletar för CRUD-åtgärder på Azure Sql Database-hanterad instans och Azure Sql-hanterad databas</span><span class="sxs-lookup"><span data-stu-id="42f58-1787">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="42f58-1788">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="42f58-1788">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="42f58-1789">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="42f58-1789">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="42f58-1790">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="42f58-1790">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="42f58-1791">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="42f58-1791">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="42f58-1792">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="42f58-1792">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="42f58-1793">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="42f58-1793">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="42f58-1794">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="42f58-1794">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="42f58-1795">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="42f58-1795">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="42f58-1796">Hantering av utökad granskningsprincip på en server eller en databas har aktiverats.</span><span class="sxs-lookup"><span data-stu-id="42f58-1796">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="42f58-1797">Ny parameter (PredicateExpression) har lagts till för att aktivera filtrering av granskningsloggar.</span><span class="sxs-lookup"><span data-stu-id="42f58-1797">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="42f58-1798">Cmdletar har ändrats så att de använder SQL-klienter i stället för äldre klienter.</span><span class="sxs-lookup"><span data-stu-id="42f58-1798">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="42f58-1799">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="42f58-1799">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="42f58-1800">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="42f58-1800">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="42f58-1801">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="42f58-1801">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="42f58-1802">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="42f58-1802">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="42f58-1803">Problem med att använda Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings med lagringskontots namnparameter har korrigerats</span><span class="sxs-lookup"><span data-stu-id="42f58-1803">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="42f58-1804">0.5.0 – november 2018</span><span class="sxs-lookup"><span data-stu-id="42f58-1804">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="42f58-1805">Allmänt</span><span class="sxs-lookup"><span data-stu-id="42f58-1805">General</span></span>
* <span data-ttu-id="42f58-1806">Lade till resurskompletterare till många kärn-cmdletar – dessa gör att du kan stega genom befintliga resursnamn med TABB vid interaktiva anrop till cmdletar</span><span class="sxs-lookup"><span data-stu-id="42f58-1806">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="42f58-1807">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="42f58-1807">Az.Profile</span></span>
* <span data-ttu-id="42f58-1808">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="42f58-1808">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="42f58-1809">Bytte namn på parametern TenantId i cmdleten Connect-AzAccount till Tenant och lade till ett alias för TenantId</span><span class="sxs-lookup"><span data-stu-id="42f58-1809">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="42f58-1810">Uppdaterade TenantId-beskrivningen för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="42f58-1810">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="42f58-1811">Åtgärda felmeddelande för misslyckad inloggning när du tillhandahåller klientdomän</span><span class="sxs-lookup"><span data-stu-id="42f58-1811">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="42f58-1812">Åtgärda problem med att kontextnamn hamnar i konflikt för konton utan prenumerationer i klientorganisationen</span><span class="sxs-lookup"><span data-stu-id="42f58-1812">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="42f58-1813">Åtgärda problem med DataLake-slutpunkter vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="42f58-1813">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="42f58-1814">Åtgärdade problem med att Disconnect-AzAccount kastades om den inte anslöts</span><span class="sxs-lookup"><span data-stu-id="42f58-1814">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="42f58-1815">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="42f58-1815">Az.CognitiveServices</span></span>
* <span data-ttu-id="42f58-1816">Lade till åtgärden Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="42f58-1816">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="42f58-1817">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="42f58-1817">Az.Compute</span></span>
* <span data-ttu-id="42f58-1818">Lade till cmdletarna Add-AzVmssVMDataDisk och Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="42f58-1818">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="42f58-1819">Get-AzVMImage visar AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="42f58-1819">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="42f58-1820">Åtgärdade att värdena för alternativen SetAzVMChefExtension -BootstrapOptions och -JsonAttribute inte angavs i json-format.</span><span class="sxs-lookup"><span data-stu-id="42f58-1820">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="42f58-1821">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="42f58-1821">Az.DataLakeStore</span></span>
* <span data-ttu-id="42f58-1822">Uppdatera DataLake-paketet till 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="42f58-1822">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="42f58-1823">Lägg till standardsamtidighet för flertrådade åtgärder.</span><span class="sxs-lookup"><span data-stu-id="42f58-1823">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="42f58-1824">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="42f58-1824">Az.Insights</span></span>
* <span data-ttu-id="42f58-1825">Åtgärdade problem #7267 (autoskalningsområde)</span><span class="sxs-lookup"><span data-stu-id="42f58-1825">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="42f58-1826">Problem med att uppräknade parametrar inte ställdes in ordentligt när du skapade en ny autoskalningsregel (de ställdes alltid in med standardvärdet).</span><span class="sxs-lookup"><span data-stu-id="42f58-1826">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="42f58-1827">Åtgärdade problem #7513 [Insights] Set-AzDiagnosticSetting kräver uttrycklig specifikation av kategorier när inställningar skapas</span><span class="sxs-lookup"><span data-stu-id="42f58-1827">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="42f58-1828">Nu kräver inte cmdleten uttrycklig anvisning av kategorierna för att aktiveras under skapande, d.v.s. den fungerar enligt beskrivning</span><span class="sxs-lookup"><span data-stu-id="42f58-1828">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="42f58-1829">Az.Network</span><span class="sxs-lookup"><span data-stu-id="42f58-1829">Az.Network</span></span>
* <span data-ttu-id="42f58-1830">PeeringType ändrades till en obligatorisk parameter för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="42f58-1830">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="42f58-1831">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="42f58-1831">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="42f58-1832">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="42f58-1832">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="42f58-1833">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="42f58-1833">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="42f58-1834">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="42f58-1834">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="42f58-1835">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="42f58-1835">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="42f58-1836">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="42f58-1836">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="42f58-1837">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="42f58-1837">Az.PolicyInsights</span></span>
* <span data-ttu-id="42f58-1838">Cmdletar för principreparation har lagts till</span><span class="sxs-lookup"><span data-stu-id="42f58-1838">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="42f58-1839">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="42f58-1839">Az.Resources</span></span>
* <span data-ttu-id="42f58-1840">Korrigering för https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="42f58-1840">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="42f58-1841">Tillåt att resurser listas med parametern -ResourceId för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="42f58-1841">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="42f58-1842">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="42f58-1842">Az.ServiceBus</span></span>
* <span data-ttu-id="42f58-1843">Skrivskyddad MigrationState-egenskap har lagts till i PSServiceBusMigrationConfigurationAttributes, som hjälper till att hålla koll på migreringstillståndet.</span><span class="sxs-lookup"><span data-stu-id="42f58-1843">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="42f58-1844">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="42f58-1844">Az.ServiceFabric</span></span>
* <span data-ttu-id="42f58-1845">Åtgärda att lägga till certifikat till Linux-Vmss.</span><span class="sxs-lookup"><span data-stu-id="42f58-1845">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="42f58-1846">Åtgärdade Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="42f58-1846">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="42f58-1847">Använd rätt tumavtryck från nya certifikat (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="42f58-1847">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="42f58-1848">Visa undantag korrekt (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="42f58-1848">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="42f58-1849">Åtgärdade Update-AzServiceFabricDurability så att klusterkonfigurationen uppdateras innan Vmss-åtgärden CreateOrUpdate påbörjas.</span><span class="sxs-lookup"><span data-stu-id="42f58-1849">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="42f58-1850">0.4.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="42f58-1850">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="42f58-1851">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="42f58-1851">Az.Profile</span></span>
* <span data-ttu-id="42f58-1852">Åtgärdade problemet med Get-AzSubscription i CloudShell</span><span class="sxs-lookup"><span data-stu-id="42f58-1852">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="42f58-1853">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="42f58-1853">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="42f58-1854">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="42f58-1854">Az.Compute</span></span>
* <span data-ttu-id="42f58-1855">Nya storlekar lades till i listan över godkända VM-storlekar för vilka accelererat nätverk kommer att aktiveras vid användning av den enkla parameteruppsättningen för New-AzVm</span><span class="sxs-lookup"><span data-stu-id="42f58-1855">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="42f58-1856">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="42f58-1856">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="42f58-1857">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="42f58-1857">Az.DataLakeStore</span></span>
* <span data-ttu-id="42f58-1858">Lägger till stöd för regler för virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="42f58-1858">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="42f58-1859">Get-AzDataLakeStoreVirtualNetworkRule: Hämtar eller listar regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="42f58-1859">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="42f58-1860">Add-AzDataLakeStoreVirtualNetworkRule: Lägger till en regel för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="42f58-1860">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="42f58-1861">Set-AzDataLakeStoreVirtualNetworkRule: Ändrar den angivna regeln för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="42f58-1861">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="42f58-1862">Remove-AzDataLakeStoreVirtualNetworkRule: Tar bort en regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="42f58-1862">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="42f58-1863">Az.Network</span><span class="sxs-lookup"><span data-stu-id="42f58-1863">Az.Network</span></span>
* <span data-ttu-id="42f58-1864">Skicka protokollvärdet till serverdelen för att uppdatera cmdleten Test-AzNetworkWatcherConnectivity.</span><span class="sxs-lookup"><span data-stu-id="42f58-1864">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="42f58-1865">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="42f58-1865">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="42f58-1866">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="42f58-1866">Az.Resources</span></span>
* <span data-ttu-id="42f58-1867">Åtgärdade problem där Get-AzRoleDefinition genererar ett oläsligt undantag (när standardprofilen inte innehåller någon prenumeration och ingen omfattning har angetts) genom att lägga till ett beskrivande undantag i scenariot.</span><span class="sxs-lookup"><span data-stu-id="42f58-1867">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="42f58-1868">Ställ in ”RoleDefinitionNameParameterSet” som standardparameteruppsättning.</span><span class="sxs-lookup"><span data-stu-id="42f58-1868">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="42f58-1869">0.3.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="42f58-1869">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="42f58-1870">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="42f58-1870">Azure.Storage</span></span>
* <span data-ttu-id="42f58-1871">Åtgärda fel där Kopiera blob/fil inte kopierar metadata när målplatsen har ett problem med metadata</span><span class="sxs-lookup"><span data-stu-id="42f58-1871">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="42f58-1872">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="42f58-1872">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="42f58-1873">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="42f58-1873">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="42f58-1874">Stöd för att hämta användningsinformation om en Storage-resurs för en specifik plats och för att lägga till ett varningsmeddelande för att hämta användningsinformation om en global Storage-resurs är inaktuellt.</span><span class="sxs-lookup"><span data-stu-id="42f58-1874">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="42f58-1875">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="42f58-1875">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="42f58-1876">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="42f58-1876">Az.CognitiveServices</span></span>
* <span data-ttu-id="42f58-1877">Stöd för Get-AzCognitiveServicesAccountSkus utan ett befintligt konto.</span><span class="sxs-lookup"><span data-stu-id="42f58-1877">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="42f58-1878">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="42f58-1878">Az.Compute</span></span>
* <span data-ttu-id="42f58-1879">Åtgärdade fel där Get-AzVM -ResourceGroupName <rg> returnerar fler än 50 resultat om det behövs</span><span class="sxs-lookup"><span data-stu-id="42f58-1879">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="42f58-1880">Lade till ett exempel för SimpleParameterSet i hjälpen för cmdleten New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="42f58-1880">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="42f58-1881">Ett stavfel i förloppsmeddelandet för Azure Disk Encryption har korrigerats</span><span class="sxs-lookup"><span data-stu-id="42f58-1881">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="42f58-1882">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="42f58-1882">Az.DataFactoryV2</span></span>
* <span data-ttu-id="42f58-1883">ADF .Net SDK-versionen har uppdaterats till 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="42f58-1883">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="42f58-1884">Az.Network</span><span class="sxs-lookup"><span data-stu-id="42f58-1884">Az.Network</span></span>
* <span data-ttu-id="42f58-1885">Funktionalitet för NetworkProfile har lagts till.</span><span class="sxs-lookup"><span data-stu-id="42f58-1885">Added NetworkProfile functionality.</span></span> <span data-ttu-id="42f58-1886">nya cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="42f58-1886">new cmdlets added</span></span>
    - <span data-ttu-id="42f58-1887">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="42f58-1887">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="42f58-1888">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="42f58-1888">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="42f58-1889">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="42f58-1889">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="42f58-1890">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="42f58-1890">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="42f58-1891">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="42f58-1891">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="42f58-1892">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="42f58-1892">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="42f58-1893">Länk för tjänstassociering på modell för undernät har lagts till</span><span class="sxs-lookup"><span data-stu-id="42f58-1893">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="42f58-1894">Cmdletarna New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap och Remove-AzVirtualNetworkTap har lagts till</span><span class="sxs-lookup"><span data-stu-id="42f58-1894">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="42f58-1895">Cmdletarna Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig och Remove-AzNEtworkInterfaceTapConfig har lagts till</span><span class="sxs-lookup"><span data-stu-id="42f58-1895">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="42f58-1896">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="42f58-1896">Az.RedisCache</span></span>
* <span data-ttu-id="42f58-1897">Tillåt att alla strängar används som storleksparametrar framöver.</span><span class="sxs-lookup"><span data-stu-id="42f58-1897">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="42f58-1898">Lägg till P5 i popup-fönstret PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="42f58-1898">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="42f58-1899">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="42f58-1899">Az.Resources</span></span>
* <span data-ttu-id="42f58-1900">Parametern -Mode som saknades i Set-AzPolicyDefinition har lagts till</span><span class="sxs-lookup"><span data-stu-id="42f58-1900">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="42f58-1901">Åtgärdade buggen för cmdleten Get-AzProviderOperation för åtgärder med ursprung som innehåller användare</span><span class="sxs-lookup"><span data-stu-id="42f58-1901">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="42f58-1902">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="42f58-1902">Az.Sql</span></span>
* <span data-ttu-id="42f58-1903">Ett problem där vissa cmdletar för säkerhetskopiering inte kunde identifiera den aktuella azure-prenumerationen har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="42f58-1903">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="42f58-1904">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="42f58-1904">Az.Websites</span></span>
* <span data-ttu-id="42f58-1905">Ny cmdlet: Get-AzWebAppContainerContinuousDeploymentUrl – Hämtar webhook-URL:en för kontinuerlig distribution av container</span><span class="sxs-lookup"><span data-stu-id="42f58-1905">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="42f58-1906">Nya cmdletar: New-AzWebAppContainerPSSession och Enter-WebAppContainerPSSession – Startar en PowerShell-fjärrsession i en containerapp för windows</span><span class="sxs-lookup"><span data-stu-id="42f58-1906">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="42f58-1907">0.2.0 – september 2018</span><span class="sxs-lookup"><span data-stu-id="42f58-1907">0.2.0 - September 2018</span></span>
 <span data-ttu-id="42f58-1908">Första versionen</span><span class="sxs-lookup"><span data-stu-id="42f58-1908">Initial Release</span></span>
