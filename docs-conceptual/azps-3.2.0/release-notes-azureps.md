---
title: Viktig information om Azure PowerShell
description: Lär dig mer om alla de senaste uppdateringarna för Azure PowerShell-modulerna.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/15/2019
ms.openlocfilehash: f77d901169b0d98b2425a2e50d33a1789150b770
ms.sourcegitcommit: e598dc45a26ff5a71112383252b350d750144a47
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2019
ms.locfileid: "75182561"
---
## <a name="320---december-2019"></a><span data-ttu-id="1e9d3-103">3.2.0 – December 2019</span><span class="sxs-lookup"><span data-stu-id="1e9d3-103">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="1e9d3-104">Allmänt</span><span class="sxs-lookup"><span data-stu-id="1e9d3-104">General</span></span>
* <span data-ttu-id="1e9d3-105">Uppdatera referenser i .psd1 för att använda relativa sökvägar för alla moduler</span><span class="sxs-lookup"><span data-stu-id="1e9d3-105">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="1e9d3-106">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1e9d3-106">Az.Accounts</span></span>
* <span data-ttu-id="1e9d3-107">Ange rätt UserAgent för telemetri på klientsidan för Az 4.0 preview</span><span class="sxs-lookup"><span data-stu-id="1e9d3-107">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="1e9d3-108">Visa användarvänligt felmeddelande när kontexten är null i Az 4.0 preview</span><span class="sxs-lookup"><span data-stu-id="1e9d3-108">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="1e9d3-109">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="1e9d3-109">Az.Batch</span></span>
* <span data-ttu-id="1e9d3-110">Korrigera problem [#10602](https://github.com/Azure/azure-powershell/issues/10602), där **New-AzBatchPool** skickade VirtualMachineConfiguration.ContainerConfiguration eller VirtualMachineConfiguration.DataDisks på ett felaktigt sätt till servern.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-110">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1e9d3-111">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1e9d3-111">Az.DataFactory</span></span>
* <span data-ttu-id="1e9d3-112">Uppdatera ADF .Net SDK-versionen till 4.5.0</span><span class="sxs-lookup"><span data-stu-id="1e9d3-112">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="1e9d3-113">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="1e9d3-113">Az.FrontDoor</span></span>
* <span data-ttu-id="1e9d3-114">Stöd har lagts till för undantag för hanterade regler för brandväggen för webbaserade program</span><span class="sxs-lookup"><span data-stu-id="1e9d3-114">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="1e9d3-115">Lägg till SocketAddr för automatisk komplettering</span><span class="sxs-lookup"><span data-stu-id="1e9d3-115">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="1e9d3-116">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="1e9d3-116">Az.HealthcareApis</span></span>
* <span data-ttu-id="1e9d3-117">Undantagshantering</span><span class="sxs-lookup"><span data-stu-id="1e9d3-117">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="1e9d3-118">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1e9d3-118">Az.KeyVault</span></span>
* <span data-ttu-id="1e9d3-119">Åtgärdat fel vid åtkomst av värde som kanske inte har angetts</span><span class="sxs-lookup"><span data-stu-id="1e9d3-119">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="1e9d3-120">Hantering av ECC-certifikat (Elliptic Curve Cryptography)</span><span class="sxs-lookup"><span data-stu-id="1e9d3-120">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="1e9d3-121">Stöd har lagts till för att ange kurvan för certifikatprinciper</span><span class="sxs-lookup"><span data-stu-id="1e9d3-121">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="1e9d3-122">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="1e9d3-122">Az.Monitor</span></span>
* <span data-ttu-id="1e9d3-123">Lägger till valfritt argument i kommandot Lägg till diagnostikinställningar.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-123">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="1e9d3-124">Ett växelargument som om det finns visar att exporten till Log Analytics måste ske till ett fast schema (kallas även</span><span class="sxs-lookup"><span data-stu-id="1e9d3-124">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="1e9d3-125">dedikerad, datatyp)</span><span class="sxs-lookup"><span data-stu-id="1e9d3-125">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1e9d3-126">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1e9d3-126">Az.Network</span></span>
* <span data-ttu-id="1e9d3-127">Stöd för IpGroups i program-, NAT- och nätverksregler för Azure Firewall.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-127">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="1e9d3-128">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1e9d3-128">Az.Resources</span></span>
* <span data-ttu-id="1e9d3-129">Åtgärda ett problem där malldistributionen inte kan läsa en mallparameter om dess namn står i konflikt med ett inbyggt parameternamn.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-129">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="1e9d3-130">Uppdaterade princip-cmdletar för att använda den nya API-versionen 2019-09-01 som introducerar grupperingsstöd inom principuppsättningsdefinitioner.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-130">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="1e9d3-131">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1e9d3-131">Az.Sql</span></span>
* <span data-ttu-id="1e9d3-132">Uppgraderad funktion för att skapa lagring i automatisk aktivering av sårbarhetsbedömning till StorageV2</span><span class="sxs-lookup"><span data-stu-id="1e9d3-132">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1e9d3-133">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1e9d3-133">Az.Storage</span></span>
* <span data-ttu-id="1e9d3-134">Stöd för generering av blob/container-identitetsbaserad SAS-token med lagringskontextbaserad på OAuth-autentisering</span><span class="sxs-lookup"><span data-stu-id="1e9d3-134">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="1e9d3-135">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="1e9d3-135">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="1e9d3-136">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="1e9d3-136">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="1e9d3-137">Stöd för återkallning av användardelegeringsnycklar för lagringskonto för att återkalla alla SAS-token</span><span class="sxs-lookup"><span data-stu-id="1e9d3-137">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="1e9d3-138">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="1e9d3-138">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="1e9d3-139">Uppgradera till Microsoft.Azure.Management.Storage 14.2.0 för att stödja den nya API-versionen 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-139">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="1e9d3-140">Stöd för att dela QuotaGiB över 5120 i filresurs-cmdletar i hanteringsplan och lägga till parameteraliaset Quota i parametern QuotaGiB</span><span class="sxs-lookup"><span data-stu-id="1e9d3-140">Support Share QuotaGiB more than 5120 in Management plane File Share cmdlets, and add parameter alias 'Quota' to parameter 'QuotaGiB'</span></span> 
    - <span data-ttu-id="1e9d3-141">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="1e9d3-141">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="1e9d3-142">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="1e9d3-142">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="1e9d3-143">Lägg till parameteraliaset QuotaGiB i parametern Quota</span><span class="sxs-lookup"><span data-stu-id="1e9d3-143">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="1e9d3-144">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="1e9d3-144">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="1e9d3-145">Åtgärda problemet att Set-AzStorageContainerAcl kan rensa den lagrade åtkomstprincipen</span><span class="sxs-lookup"><span data-stu-id="1e9d3-145">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="1e9d3-146">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="1e9d3-146">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="1e9d3-147">3.1.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="1e9d3-147">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="1e9d3-148">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="1e9d3-148">Highlights since the last major release</span></span>
* <span data-ttu-id="1e9d3-149">Az.DataBoxEdge 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="1e9d3-149">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="1e9d3-150">Az.SqlVirtualMachine 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="1e9d3-150">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1e9d3-151">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1e9d3-151">Az.Compute</span></span>
* <span data-ttu-id="1e9d3-152">Funktion för att använda en virtuell dator igen</span><span class="sxs-lookup"><span data-stu-id="1e9d3-152">VM Reapply feature</span></span>
    - <span data-ttu-id="1e9d3-153">Lägg till parameter för att använda igen till cmdleten Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="1e9d3-153">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="1e9d3-154">Funktionen AutomaticRepairs i VM-skalningsuppsättningar:</span><span class="sxs-lookup"><span data-stu-id="1e9d3-154">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="1e9d3-155">Lägg till parametrarna EnableAutomaticRepair, AutomaticRepairGracePeriod och AutomaticRepairMaxInstanceRepairsPercent till följande cmdletar:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="1e9d3-155">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="1e9d3-156">Stöd för galleriavbildningar i flera klientorganisationer för New-AzVM</span><span class="sxs-lookup"><span data-stu-id="1e9d3-156">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="1e9d3-157">Lägg till "Spot" till argumentslutföraren i prioritetsparametern i cmdletarna New-AzVM, New-AzVMConfig och New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="1e9d3-157">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="1e9d3-158">Lägg till parametrarna DiskIOPSReadWrite och DiskMBpsReadWrite till cmdleten Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="1e9d3-158">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="1e9d3-159">Ändra parametern SourceImageId för cmdleten New-AzGalleryImageVersion till valfri</span><span class="sxs-lookup"><span data-stu-id="1e9d3-159">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="1e9d3-160">Lägg till parametrarna OSDiskImage och DataDiskImage till cmdleten New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="1e9d3-160">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="1e9d3-161">Lägg till parametern HyperVGeneration till cmdleten New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="1e9d3-161">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="1e9d3-162">Lägg till parametern SkipExtensionsOnOverprovisionedVMs till cmdletarna New-AzVmss, New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="1e9d3-162">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="1e9d3-163">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="1e9d3-163">Az.DataBoxEdge</span></span>
* <span data-ttu-id="1e9d3-164">Cmdleten `Get-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="1e9d3-164">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="1e9d3-165">Hämta ordning</span><span class="sxs-lookup"><span data-stu-id="1e9d3-165">Get the Order</span></span>
* <span data-ttu-id="1e9d3-166">Cmdleten `New-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="1e9d3-166">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="1e9d3-167">Skapa ny ordning</span><span class="sxs-lookup"><span data-stu-id="1e9d3-167">Create new Order</span></span>
* <span data-ttu-id="1e9d3-168">Cmdleten `Remove-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="1e9d3-168">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="1e9d3-169">Ta bort ordning</span><span class="sxs-lookup"><span data-stu-id="1e9d3-169">Remove the Order</span></span>
* <span data-ttu-id="1e9d3-170">Cmdleten `New-AzDataBoxEdgeShare` har ändrats</span><span class="sxs-lookup"><span data-stu-id="1e9d3-170">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="1e9d3-171">Nu skapas lokal filresurs</span><span class="sxs-lookup"><span data-stu-id="1e9d3-171">Now creates Local Share</span></span>
* <span data-ttu-id="1e9d3-172">Cmdleten `Set-AzDataBoxEdgeRole` har lagts till</span><span class="sxs-lookup"><span data-stu-id="1e9d3-172">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="1e9d3-173">Nu kan IotRole mappas till filresursen</span><span class="sxs-lookup"><span data-stu-id="1e9d3-173">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="1e9d3-174">Cmdleten `Invoke-AzDataBoxEdgeDevice` har lagts till</span><span class="sxs-lookup"><span data-stu-id="1e9d3-174">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="1e9d3-175">Anropa genomsökningsuppdatering, ladda ned uppdatering, installera uppdateringar på enheten</span><span class="sxs-lookup"><span data-stu-id="1e9d3-175">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="1e9d3-176">Cmdleten `Get-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="1e9d3-176">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="1e9d3-177">Hämtar information om utlösare</span><span class="sxs-lookup"><span data-stu-id="1e9d3-177">Gets the information about Triggers</span></span>
* <span data-ttu-id="1e9d3-178">Cmdleten `New-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="1e9d3-178">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="1e9d3-179">Skapa nya utlösare</span><span class="sxs-lookup"><span data-stu-id="1e9d3-179">Create new Triggers</span></span>
* <span data-ttu-id="1e9d3-180">Cmdleten `Remove-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="1e9d3-180">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="1e9d3-181">Ta bort utlösare</span><span class="sxs-lookup"><span data-stu-id="1e9d3-181">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1e9d3-182">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1e9d3-182">Az.DataFactory</span></span>
* <span data-ttu-id="1e9d3-183">Uppdatera ADF .Net SDK-versionen till 4.4.0</span><span class="sxs-lookup"><span data-stu-id="1e9d3-183">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="1e9d3-184">Lägg till parametern ExpressCustomSetup för kommandot Set-AzureRmDataFactoryV2IntegrationRuntime för att aktivera installationskonfigurationer och komponenter från tredje part utan anpassat konfigurationsskript.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-184">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="1e9d3-185">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1e9d3-185">Az.DataLakeStore</span></span>
* <span data-ttu-id="1e9d3-186">Uppdatera dokumentation för Get-AzDataLakeStoreDeletedItem och Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="1e9d3-186">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="1e9d3-187">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="1e9d3-187">Az.EventHub</span></span>
* <span data-ttu-id="1e9d3-188">Korrigering av problem #10301: Korrigera datumformat för SAS-token</span><span class="sxs-lookup"><span data-stu-id="1e9d3-188">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="1e9d3-189">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="1e9d3-189">Az.FrontDoor</span></span>
* <span data-ttu-id="1e9d3-190">Lägg till parametern MinimumTlsVersion till Enable-AzFrontDoorCustomDomainHttps och New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="1e9d3-190">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="1e9d3-191">Lägg till parametrarna HealthProbeMethod och EnabledState till New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="1e9d3-191">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="1e9d3-192">Lägg till en ny cmdlet för att skapa BackendPoolsSettings-objekt som passar i skapande/uppdatering av Front Door</span><span class="sxs-lookup"><span data-stu-id="1e9d3-192">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="1e9d3-193">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="1e9d3-193">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1e9d3-194">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1e9d3-194">Az.Network</span></span>
* <span data-ttu-id="1e9d3-195">Ändra alternativexemplen Start-AzVirtualNetworkGatewayConnectionPacketCapture.md och Start-AzVirtualnetworkGatewayPacketCapture.md för FilterData.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-195">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="1e9d3-196">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="1e9d3-196">Az.PrivateDns</span></span>
* <span data-ttu-id="1e9d3-197">Uppdaterade PrivateDns .NET SDK till version 1.0.0</span><span class="sxs-lookup"><span data-stu-id="1e9d3-197">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1e9d3-198">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1e9d3-198">Az.RecoveryServices</span></span>
* <span data-ttu-id="1e9d3-199">Stöd för att välja disktyp vid aktivering av skydd i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-199">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="1e9d3-200">Korrigering av bugg för åtgärdsredigering av återställningsplan i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-200">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="1e9d3-201">Återställningsstöd för att godkänna filestream-databaser i Azure Backup SQL.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-201">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="1e9d3-202">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="1e9d3-202">Az.RedisCache</span></span>
* <span data-ttu-id="1e9d3-203">Parametern MinimumTlsVersion har lagts till i cmdletarna New-AzRedisCache och Set-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-203">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="1e9d3-204">Dessutom har MinimumTlsVersion lagts till i utdata för cmdleten Get-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-204">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="1e9d3-205">Verifiering har lagts till på parametern -Size i cmdletarna Set-AzRedisCache och New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="1e9d3-205">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="1e9d3-206">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1e9d3-206">Az.Resources</span></span>
- <span data-ttu-id="1e9d3-207">Uppdaterade policy-cmdletar för att använda den nya API-versionen 2019-06-01 som har en ny EnforcementMode-egenskap i policytilldelningen.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-207">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="1e9d3-208">Uppdaterade hjälpexempel för skapandet av policydefinition</span><span class="sxs-lookup"><span data-stu-id="1e9d3-208">Updated create policy definition help example</span></span>
- <span data-ttu-id="1e9d3-209">Åtgärda bugg i Remove-AZADServicePrincipal -ServicePrincipalName, utlös null-referens när tjänstens huvudnamn inte hittas.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-209">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="1e9d3-210">Åtgärda bugg i New-AZADServicePrincipal, utlös null-referens när klientorganisationen inte har någon prenumeration.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-210">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="1e9d3-211">Ändra New-AzAdServicePrincipal för att endast lägga till autentiseringsuppgifter för det associerade programmet.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-211">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="1e9d3-212">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1e9d3-212">Az.Sql</span></span>
* <span data-ttu-id="1e9d3-213">Stöd har lagts till för databasen ReadReplicaCount.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-213">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="1e9d3-214">Korrigerade Set-AzSqlDatabase när zonredundans inte har angetts</span><span class="sxs-lookup"><span data-stu-id="1e9d3-214">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="1e9d3-215">3.0.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="1e9d3-215">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="1e9d3-216">Allmänt</span><span class="sxs-lookup"><span data-stu-id="1e9d3-216">General</span></span>
* <span data-ttu-id="1e9d3-217">Az. PrivateDns 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="1e9d3-217">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="1e9d3-218">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1e9d3-218">Az.Accounts</span></span>
* <span data-ttu-id="1e9d3-219">Lägg till ett utfasningsmeddelande för aliaset Resolve-error.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-219">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="1e9d3-220">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="1e9d3-220">Az.Advisor</span></span>
* <span data-ttu-id="1e9d3-221">Den nya kategorin Operational Excellence har lagts till i cmdleten Get-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-221">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="1e9d3-222">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="1e9d3-222">Az.Batch</span></span>
* <span data-ttu-id="1e9d3-223">`CoreQuota` på `BatchAccountContext` har bytt namn till `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-223">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="1e9d3-224">Det finns även en ny `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-224">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="1e9d3-225">Detta påverkar **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-225">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="1e9d3-226">**New-AzBatchTask** `-ResourceFile`-parameter tar nu en samling `PSResourceFile`-objekt som kan skapas med hjälp av den nya cmdleten **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-226">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="1e9d3-227">Ny **New-AzBatchResourceFile**-cmdlet för att skapa `PSResourceFile`-objekt.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-227">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="1e9d3-228">Dessa kan tillhandahållas till **New-AzBatchTask** på `-ResourceFile`-parametern.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-228">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="1e9d3-229">Detta stöder två nya typer av resursfiler förutom det befintliga sättet med `HttpUrl`:</span><span class="sxs-lookup"><span data-stu-id="1e9d3-229">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="1e9d3-230">`AutoStorageContainerName`-baserade resursfiler laddar ned en hel container för automatisk lagring till Batch-noden.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-230">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="1e9d3-231">`StorageContainerUrl`-baserade resursfiler laddar ned containern som anges i webbadressen till Batch-noden.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-231">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="1e9d3-232">Tog bort egenskapen `ApplicationPackages` för `PSApplication` som returnerades av **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-232">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="1e9d3-233">Specifika paket i ett program kan nu hämtas med hjälp av **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-233">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="1e9d3-234">Till exempel: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-234">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="1e9d3-235">Bytt namn på `ApplicationId` till `ApplicationName` på **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** och **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-235">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="1e9d3-236">`ApplicationId` är nu ett alias för `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-236">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="1e9d3-237">Ny `PSWindowsUserConfiguration`-egenskap till `PSUserAccount` lades till.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-237">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="1e9d3-238">Bytte namn på `Version` till `Name` på `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-238">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="1e9d3-239">Bytte namn på `BlobSource` till `HttpUrl` på `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-239">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="1e9d3-240">Tog bort egenskapen `OSDisk` från `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-240">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="1e9d3-241">Tog bort **Set-AzBatchPoolOSVersion**.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-241">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="1e9d3-242">Den här åtgärden stöds inte längre.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-242">This operation is no longer supported.</span></span>
* <span data-ttu-id="1e9d3-243">`TargetOSVersion` har tagits bort från `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-243">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="1e9d3-244">Bytte namn på `CurrentOSVersion` till `OSVersion` på `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-244">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="1e9d3-245">`DataEgressGiB` och `DataIngressGiB` har tagits bort från `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-245">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="1e9d3-246">Tog bort **Get-AzBatchNodeAgentSku** och ersatte det med **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-246">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span> 
  - <span data-ttu-id="1e9d3-247">**Get-AzBatchSupportedImage** returnerar samma data som **Get-AzBatchNodeAgentSku** men i ett mer användarvänligt format.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-247">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="1e9d3-248">Nya icke-verifierade avbildningar returneras nu också.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-248">New non-verified images are also now returned.</span></span> <span data-ttu-id="1e9d3-249">Ytterligare information om `Capabilities` och `BatchSupportEndOfLife` för varje avbildning inkluderas också.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-249">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="1e9d3-250">Lade till möjlighet att montera fjärrfilsystem på varje nod i en pool via den nya parametern `MountConfiguration` för **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-250">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="1e9d3-251">Har nu stöd för nätverkssäkerhetsregler som blockerar nätverksåtkomst till en pool baserat på källportens trafik.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-251">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="1e9d3-252">Detta görs via egenskapen `SourcePortRanges` på `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-252">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="1e9d3-253">När du kör en container stöder nu Batch körningen av uppgiften i arbetskatalogen för containern eller i arbetskatalogen för Batch-uppgiften.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-253">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="1e9d3-254">Detta styrs av egenskapen `WorkingDirectory` på `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-254">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="1e9d3-255">Lade till en funktion för att ange en samling av offentliga IP-adresser på `PSNetworkConfiguration` via den nya egenskapen `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-255">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="1e9d3-256">Detta garanterar att noderna i poolen har en IP-adress från listan över IP-adresser som tillhandahållits av användare.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-256">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="1e9d3-257">Om inget värde anges är standardvärdet för `WaitForSuccess` på `PSSTartTask` nu `$True` (var tidigare `$False`).</span><span class="sxs-lookup"><span data-stu-id="1e9d3-257">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="1e9d3-258">Om inget värde anges är standardvärdet för `Scope` på `PSAutoUserSpecification` nu `Pool` (var tidigare `Task` på Windows och `Pool` på Linux).</span><span class="sxs-lookup"><span data-stu-id="1e9d3-258">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="1e9d3-259">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="1e9d3-259">Az.Cdn</span></span>
* <span data-ttu-id="1e9d3-260">Introducerade UrlRewriteAction och CacheKeyQueryStringAction till RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-260">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="1e9d3-261">Åtgärdade flera buggar, som saknade indata för ”väljare” i cmdleten New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-261">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1e9d3-262">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1e9d3-262">Az.Compute</span></span>
* <span data-ttu-id="1e9d3-263">Funktion för diskkrypteringsuppsättning</span><span class="sxs-lookup"><span data-stu-id="1e9d3-263">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="1e9d3-264">Nya cmdletar:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="1e9d3-264">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="1e9d3-265">Parametern DiskEncryptionSetId har lagts till i följande cmdletar: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="1e9d3-265">DiskEncryptionSetId parameter is added to the following cmdlets: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span></span>        
        <span data-ttu-id="1e9d3-266">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="1e9d3-266">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="1e9d3-267">Parametrarna DiskEncryptionSetId och EncryptionType har lagts till i följande cmdletar:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="1e9d3-267">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="1e9d3-268">Lägg till parametern PublicIPAddressVersion i New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="1e9d3-268">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="1e9d3-269">Flytta FileUris för anpassat skripttillägg från offentlig inställning till skyddad inställning</span><span class="sxs-lookup"><span data-stu-id="1e9d3-269">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="1e9d3-270">Lägg till ScaleInPolicy i cmdletarna New-AzVmss, New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="1e9d3-270">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="1e9d3-271">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="1e9d3-271">Breaking changes</span></span>
    - <span data-ttu-id="1e9d3-272">Parametern UploadSizeInBytes används istället för DiskSizeGB för New-AzDiskConfig när CreateOption är Uppladdning</span><span class="sxs-lookup"><span data-stu-id="1e9d3-272">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="1e9d3-273">PublishingProfile.Source.ManagedImage.Id ersätts med StorageProfile.Source.Id i objektet GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="1e9d3-273">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1e9d3-274">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1e9d3-274">Az.DataFactory</span></span>
* <span data-ttu-id="1e9d3-275">Uppdatera ADF .Net SDK-versionen till 4.3.0</span><span class="sxs-lookup"><span data-stu-id="1e9d3-275">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="1e9d3-276">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1e9d3-276">Az.DataLakeStore</span></span>
* <span data-ttu-id="1e9d3-277">Uppdatera ADLS SDK-version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) innehåller följande korrigeringar</span><span class="sxs-lookup"><span data-stu-id="1e9d3-277">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="1e9d3-278">Undvik att utlösa undantag när det inte går att deserialisera creationtime för inmatning av papperskorg eller katalog.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-278">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="1e9d3-279">Gör inställning tillgänglig per tidsgräns för förfrågan i adlsclient</span><span class="sxs-lookup"><span data-stu-id="1e9d3-279">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="1e9d3-280">Korrigera överföringen av ursprunglig syncflag för badoffset-återställning</span><span class="sxs-lookup"><span data-stu-id="1e9d3-280">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="1e9d3-281">Korrigera EnumerateDirectory för att hämta fortsättningstoken när svar har kontrollerats</span><span class="sxs-lookup"><span data-stu-id="1e9d3-281">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="1e9d3-282">Korrigera bugg i Concat</span><span class="sxs-lookup"><span data-stu-id="1e9d3-282">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="1e9d3-283">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="1e9d3-283">Az.FrontDoor</span></span>
* <span data-ttu-id="1e9d3-284">Åtgärdade diverse stavfel i modul</span><span class="sxs-lookup"><span data-stu-id="1e9d3-284">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="1e9d3-285">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="1e9d3-285">Az.HDInsight</span></span>
* <span data-ttu-id="1e9d3-286">Korrigerade buggen att kunder får felet ”inte en giltig Base-64-sträng” vid användning av Get-AzHDInsightCluster för att hämta klustret med ADLSGen1-lagring.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-286">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="1e9d3-287">Lägg till en parameter med namnet ”ApplicationId” i de tre cmdletarna Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig och New-AzHDInsightCluster så att kunden kan tillhandahålla tjänstens huvudnamn för program-ID för åtkomst till Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-287">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="1e9d3-288">Ändrade Microsoft.Azure.Management.HDInsight från 2.1.0 till 5.1.0</span><span class="sxs-lookup"><span data-stu-id="1e9d3-288">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="1e9d3-289">Fem cmdletar har tagits bort:</span><span class="sxs-lookup"><span data-stu-id="1e9d3-289">Removed five cmdlets:</span></span>
    - <span data-ttu-id="1e9d3-290">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="1e9d3-290">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="1e9d3-291">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="1e9d3-291">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="1e9d3-292">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="1e9d3-292">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="1e9d3-293">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="1e9d3-293">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="1e9d3-294">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="1e9d3-294">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="1e9d3-295">Tre cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="1e9d3-295">Added three cmdlets:</span></span>
    - <span data-ttu-id="1e9d3-296">Get-AzHDInsightMonitoring som ersätter Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-296">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="1e9d3-297">Enable-AzHDInsightMonitoring som ersätter Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-297">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="1e9d3-298">Disable-AzHDInsightMonitoring som ersätter Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-298">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="1e9d3-299">Korrigerade cmdleten Get-AzHDInsightProperties för att stödja hämtning av funktionsinformation från en viss plats.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-299">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="1e9d3-300">Parameteruppsättningarna (Spark1 och Spark2) har tagits bort från Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-300">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="1e9d3-301">Lägg till exempel för cmdleten Add-AzHDInsightSecurityProfile till hjälpdokumenten.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-301">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="1e9d3-302">Ändrade utdatatyp för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="1e9d3-302">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="1e9d3-303">Ändrade utdatatyp för Get-AzHDInsightProperties från CapabilitiesResponse till AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-303">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="1e9d3-304">Ändrade utdatatyp för Remove-AzHDInsightCluster från ClusterGetResponse till bool.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-304">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="1e9d3-305">Ändrade utdatatyp för Set-AzHDInsightGatewaySettings HttpConnectivitySettings till GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-305">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="1e9d3-306">Lade till testfall för vissa scenarier.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-306">Added some scenario test cases.</span></span>
* <span data-ttu-id="1e9d3-307">Ta bort vissa alias: Add-AzHDInsightConfigValues, Get-AzHDInsightProperties.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-307">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="1e9d3-308">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="1e9d3-308">Az.IotHub</span></span>
* <span data-ttu-id="1e9d3-309">Icke-bakåtkompatibla ändringar:</span><span class="sxs-lookup"><span data-stu-id="1e9d3-309">Breaking changes:</span></span>
    - <span data-ttu-id="1e9d3-310">Cmdleten Add-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-310">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="1e9d3-311">Parameteruppsättningen __AllParameterSets för cmdleten Add-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-311">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="1e9d3-312">Cmdleten Get-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-312">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="1e9d3-313">Parameteruppsättningen __AllParameterSets för cmdleten Get-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-313">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="1e9d3-314">Egenskapen OperationsMonitoringProperties av typen Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-314">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="1e9d3-315">Egenskapen OperationsMonitoringProperties av typen Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-315">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="1e9d3-316">Cmdleten New-AzIotHubExportDevice stöder inte längre aliaset New-AzIotHubExportDevices.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-316">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="1e9d3-317">Cmdleten New-AzIotHubImportDevice stöder inte längre aliaset New-AzIotHubImportDevices.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-317">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="1e9d3-318">Cmdleten Remove-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-318">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="1e9d3-319">Parameteruppsättningen __AllParameterSets för cmdleten Remove-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-319">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="1e9d3-320">Cmdleten Set-AzIotHub har inte längre stöd för parametern OperationsMonitoringProperties och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-320">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="1e9d3-321">Parameteruppsättningen UpdateOperationsMonitoringProperties för cmdleten Set-AzIotHub har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-321">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1e9d3-322">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1e9d3-322">Az.RecoveryServices</span></span>
* <span data-ttu-id="1e9d3-323">Azure Site Recovery-stöd för att konfigurera nätverksresurser som NSG, offentliga IP-adresser och interna lastbalanserare för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-323">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="1e9d3-324">Azure Site Recovery-stöd för att skriva till hanterad disk för vMWare till Azure.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-324">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="1e9d3-325">Azure Site Recovery-stöd för NIC-reduktion för vMWare till Azure.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-325">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="1e9d3-326">Azure Site Recovery-stöd för accelererat nätverk för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-326">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="1e9d3-327">Azure Site Recovery-stöd för automatisk uppdatering av agent för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-327">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="1e9d3-328">Azure Site Recovery-stöd för Standard SSD för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-328">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="1e9d3-329">Azure Site Recovery-stöd för tvåstegskryptering i Azure Disk Encryption för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-329">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="1e9d3-330">Azure Site Recovery-stöd för att skydda nyligen tillagda diskar för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-330">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="1e9d3-331">En funktion för mjuk borttagning av virtuella datorer samt tester för mjuk borttagning har tagits bort</span><span class="sxs-lookup"><span data-stu-id="1e9d3-331">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="1e9d3-332">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1e9d3-332">Az.Resources</span></span>
* <span data-ttu-id="1e9d3-333">Uppdatera beroendesammansättning för Microsoft.Extensions.Caching.Memory från 1.1.1 till 2.2</span><span class="sxs-lookup"><span data-stu-id="1e9d3-333">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1e9d3-334">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1e9d3-334">Az.Network</span></span>
* <span data-ttu-id="1e9d3-335">Ändra alla cmdletar för PrivateEndpointConnection så att de stöder generiska tjänstleverantörer.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-335">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="1e9d3-336">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="1e9d3-336">Updated cmdlet:</span></span>
        - <span data-ttu-id="1e9d3-337">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="1e9d3-337">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="1e9d3-338">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="1e9d3-338">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="1e9d3-339">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="1e9d3-339">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="1e9d3-340">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="1e9d3-340">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="1e9d3-341">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="1e9d3-341">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="1e9d3-342">Lägg till ny cmdlet för PrivateLinkResource så att det också stöder generiska tjänstleverantörer.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-342">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="1e9d3-343">Ny cmdlet:</span><span class="sxs-lookup"><span data-stu-id="1e9d3-343">New cmdlet:</span></span>
        - <span data-ttu-id="1e9d3-344">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="1e9d3-344">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="1e9d3-345">Lägg till nya fält och parametrar för funktionen Proxy Protocol V2.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-345">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="1e9d3-346">Lägg till egenskapen EnableProxyProtocol i PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="1e9d3-346">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="1e9d3-347">Lägg till egenskapen LinkIdentifier i PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="1e9d3-347">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="1e9d3-348">Uppdaterade New-AzPrivateLinkService för att lägga till den nya valfria parametern EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-348">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="1e9d3-349">Korrigera felaktig beskrivning av parameter i referensdokumentationen för New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="1e9d3-349">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="1e9d3-350">Nya cmdletar som stöder Azure-brandväggsprincipen</span><span class="sxs-lookup"><span data-stu-id="1e9d3-350">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="1e9d3-351">Lägg till stöd för den underordnade resursen RouteTables för VirtualHub</span><span class="sxs-lookup"><span data-stu-id="1e9d3-351">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="1e9d3-352">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="1e9d3-352">New cmdlets added:</span></span>
        - <span data-ttu-id="1e9d3-353">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="1e9d3-353">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="1e9d3-354">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="1e9d3-354">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="1e9d3-355">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="1e9d3-355">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="1e9d3-356">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="1e9d3-356">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="1e9d3-357">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="1e9d3-357">Set-AzVirtualHub</span></span>
* <span data-ttu-id="1e9d3-358">Lägg till stöd för ny egenskaps-SKU för VirtualHub och VirtualWANType för VirtualWan</span><span class="sxs-lookup"><span data-stu-id="1e9d3-358">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="1e9d3-359">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="1e9d3-359">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="1e9d3-360">New-AzVirtualHub: lade till parameter-SKU</span><span class="sxs-lookup"><span data-stu-id="1e9d3-360">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="1e9d3-361">Update-AzVirtualHub: lade till parameter-SKU</span><span class="sxs-lookup"><span data-stu-id="1e9d3-361">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="1e9d3-362">New-AzVirtualWan: lade till parametern VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="1e9d3-362">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="1e9d3-363">Update-AzVirtualWan: lade till parametern VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="1e9d3-363">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="1e9d3-364">Lägg till stöd för egenskapen EnableInternetSecurity för HubVnetConnection, VpnConnection och ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="1e9d3-364">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="1e9d3-365">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="1e9d3-365">New cmdlets added:</span></span>
        - <span data-ttu-id="1e9d3-366">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="1e9d3-366">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="1e9d3-367">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="1e9d3-367">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="1e9d3-368">New-AzureRmVirtualHubVnetConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="1e9d3-368">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="1e9d3-369">New-AzureRmVpnConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="1e9d3-369">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="1e9d3-370">Update-AzureRmVpnConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="1e9d3-370">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="1e9d3-371">New-AzureRmExpressRouteConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="1e9d3-371">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="1e9d3-372">Set-AzureRmExpressRouteConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="1e9d3-372">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="1e9d3-373">Lägg till stöd för att konfigurera TopLevel WebApplicationFirewall-princip</span><span class="sxs-lookup"><span data-stu-id="1e9d3-373">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="1e9d3-374">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="1e9d3-374">New cmdlets added:</span></span>
        - <span data-ttu-id="1e9d3-375">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="1e9d3-375">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="1e9d3-376">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="1e9d3-376">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="1e9d3-377">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="1e9d3-377">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="1e9d3-378">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="1e9d3-378">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="1e9d3-379">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="1e9d3-379">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="1e9d3-380">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="1e9d3-380">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="1e9d3-381">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="1e9d3-381">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="1e9d3-382">New-AzApplicationGatewayFirewallPolicy: parametrarna PolicySetting, ManagedRule har lagts till</span><span class="sxs-lookup"><span data-stu-id="1e9d3-382">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="1e9d3-383">Stöd för operator för geomatchning har lagts till på CustomRule</span><span class="sxs-lookup"><span data-stu-id="1e9d3-383">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="1e9d3-384">Geomatchning har lagts till i operatorn på FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="1e9d3-384">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="1e9d3-385">Stöd har lagts till för brandväggsprinciperna perListener och perSite</span><span class="sxs-lookup"><span data-stu-id="1e9d3-385">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="1e9d3-386">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="1e9d3-386">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="1e9d3-387">New-AzApplicationGatewayHttpListener: parametrarna FirewallPolicy, FirewallPolicyId har lagts till</span><span class="sxs-lookup"><span data-stu-id="1e9d3-387">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="1e9d3-388">New-AzApplicationGatewayPathRuleConfig: parametrarna FirewallPolicy, FirewallPolicyId har lagts till</span><span class="sxs-lookup"><span data-stu-id="1e9d3-388">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="1e9d3-389">Åtgärdat så att nödvändigt undernät med namnet AzureBastionSubnet i PSBastion kan vara skiftlägesokänsligt</span><span class="sxs-lookup"><span data-stu-id="1e9d3-389">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="1e9d3-390">Stöd för mål-FQDN:er i nätverksregler och översatt FQDN i NAT-regler för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="1e9d3-390">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="1e9d3-391">Lägg till stöd för resursen RouteTables för IpGroup på den högsta nivån</span><span class="sxs-lookup"><span data-stu-id="1e9d3-391">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="1e9d3-392">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="1e9d3-392">New cmdlets added:</span></span>
        - <span data-ttu-id="1e9d3-393">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="1e9d3-393">New-AzIpGroup</span></span>
        - <span data-ttu-id="1e9d3-394">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="1e9d3-394">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="1e9d3-395">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="1e9d3-395">Get-AzIpGroup</span></span>
        - <span data-ttu-id="1e9d3-396">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="1e9d3-396">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="1e9d3-397">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1e9d3-397">Az.ServiceFabric</span></span>
* <span data-ttu-id="1e9d3-398">Ta bort cmdleten Add-AzServiceFabricApplicationCertificate eftersom det här scenariot omfattas av Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-398">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="1e9d3-399">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1e9d3-399">Az.Sql</span></span>
* <span data-ttu-id="1e9d3-400">Stöd har lagts till för återställning av utelämnade databaser på hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-400">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="1e9d3-401">Inaktuella gamla cmdletar för granskning från kod.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-401">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="1e9d3-402">Tog bort inaktuella alias:</span><span class="sxs-lookup"><span data-stu-id="1e9d3-402">Removed deprecated aliases:</span></span>
* <span data-ttu-id="1e9d3-403">Get-AzSqlDatabaseIndexRecommendations (använd Get-AzSqlDatabaseIndexRecommendation istället)</span><span class="sxs-lookup"><span data-stu-id="1e9d3-403">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="1e9d3-404">Get-AzSqlDatabaseRestorePoints (använd Get-AzSqlDatabaseRestorePoint istället)</span><span class="sxs-lookup"><span data-stu-id="1e9d3-404">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="1e9d3-405">Ta bort cmdleten Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="1e9d3-405">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="1e9d3-406">Ta bort alias för inaktuella cmdletar för inställningar för utvärdering av säkerhetsrisk</span><span class="sxs-lookup"><span data-stu-id="1e9d3-406">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="1e9d3-407">Inaktualisera cmdletar för inställningar för avancerad hotidentifiering</span><span class="sxs-lookup"><span data-stu-id="1e9d3-407">Deprecate Advanced Threat Detection Settings cmdlets</span></span> 
* <span data-ttu-id="1e9d3-408">Lägga till cmdletar för att inaktivera och aktivera känslighetsrekommendationer på kolumner i en databas.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-408">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1e9d3-409">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1e9d3-409">Az.Storage</span></span>
* <span data-ttu-id="1e9d3-410">Stöd för att aktivera stora filresurser vid skapande eller uppdatering av lagringskonto</span><span class="sxs-lookup"><span data-stu-id="1e9d3-410">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="1e9d3-411">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1e9d3-411">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="1e9d3-412">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1e9d3-412">Set-AzStorageAccount</span></span>
* <span data-ttu-id="1e9d3-413">När du stänger/hämtar en filreferens kan du hoppa över kontrollen av huruvida indatasökvägen är en filkatalog eller en fil för att undvika problem med objekt som har status DeletePending</span><span class="sxs-lookup"><span data-stu-id="1e9d3-413">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="1e9d3-414">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="1e9d3-414">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="1e9d3-415">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="1e9d3-415">Close-AzStorageFileHandle</span></span>
    
## <a name="280---october-2019"></a><span data-ttu-id="1e9d3-416">2.8.0 – oktober 2019</span><span class="sxs-lookup"><span data-stu-id="1e9d3-416">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="1e9d3-417">Allmänt</span><span class="sxs-lookup"><span data-stu-id="1e9d3-417">General</span></span>
* <span data-ttu-id="1e9d3-418">AZ. HealthcareApis 1.0.0-version</span><span class="sxs-lookup"><span data-stu-id="1e9d3-418">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="1e9d3-419">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1e9d3-419">Az.Accounts</span></span>
* <span data-ttu-id="1e9d3-420">Uppdatera telemetri och URL-omskrivning för genererade moduler, korrigera Windows-enhetstester.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-420">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="1e9d3-421">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="1e9d3-421">Az.ApiManagement</span></span>
* <span data-ttu-id="1e9d3-422">**Set-AzApiManagementApi** – Tillagt stöd för att uppdatera Api till ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="1e9d3-422">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="1e9d3-423">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="1e9d3-423">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="1e9d3-424">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1e9d3-424">Az.Automation</span></span>
* <span data-ttu-id="1e9d3-425">Åtgärdade cmdleten New-AzureAutomationSoftwareUpdateConfiguration för parametern för inställning av Linux-omstart.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-425">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="1e9d3-426">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="1e9d3-426">Az.Batch</span></span>
* <span data-ttu-id="1e9d3-427">**Get-AzBatchNodeAgentSku** är inaktuell och ersätts av **Get-AzBatchSupportImage** i version 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-427">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1e9d3-428">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1e9d3-428">Az.Compute</span></span>
* <span data-ttu-id="1e9d3-429">Lägg till parametrarna Priority, EvictionPolicy och MaxPrice till cmdletarna New-AzVM och New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="1e9d3-429">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="1e9d3-430">Korrigera varningsmeddelande och hjälpdokument för cmdletarna Add-AzVMAdditionalUnattendContent och Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="1e9d3-430">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="1e9d3-431">Åtgärda – skipVmBackup-undantag för virtuella Linux-datorer med hanterade diskar för Set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-431">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="1e9d3-432">Åtgärda fel i uppdatera krypteringsinställningarna i set-AzVMDiskEncryptionExtension, scenario i två steg.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-432">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1e9d3-433">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1e9d3-433">Az.DataFactory</span></span>
* <span data-ttu-id="1e9d3-434">Lägga till CRUD-kommandon för ADF V2-dataflödet: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow och Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-434">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="1e9d3-435">Lägger till åtgärdskommandon för ADF V2-dataflödesfelsökningssession: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand och Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-435">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="1e9d3-436">Uppdatera ADF .Net SDK-versionen till 4.2.0</span><span class="sxs-lookup"><span data-stu-id="1e9d3-436">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="1e9d3-437">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1e9d3-437">Az.DataLakeStore</span></span>
* <span data-ttu-id="1e9d3-438">Korrigera kontovalidering så att konton med ”-” kan skickas utan domän</span><span class="sxs-lookup"><span data-stu-id="1e9d3-438">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="1e9d3-439">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="1e9d3-439">Az.HealthcareApis</span></span>
* <span data-ttu-id="1e9d3-440">PowerShell-versionen har uppdaterats till 1.0.0</span><span class="sxs-lookup"><span data-stu-id="1e9d3-440">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="1e9d3-441">Uppdaterade SDK-versionen till 1.0.2</span><span class="sxs-lookup"><span data-stu-id="1e9d3-441">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="1e9d3-442">Uppdatera i tester för att referera till en ny SDK-version</span><span class="sxs-lookup"><span data-stu-id="1e9d3-442">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="1e9d3-443">Utdatastrukturen har uppdaterats från kapslad till förenklad.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-443">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="1e9d3-444">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="1e9d3-444">Az.IotHub</span></span>
* <span data-ttu-id="1e9d3-445">Lägg till ny routningskälla: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="1e9d3-445">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="1e9d3-446">Mindre felkorrigering: Get-AzIothub returnerar inte subscriptionId</span><span class="sxs-lookup"><span data-stu-id="1e9d3-446">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="1e9d3-447">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="1e9d3-447">Az.Monitor</span></span>
* <span data-ttu-id="1e9d3-448">Nya åtgärdsgruppsmottagare har lagts till för åtgärdsgrupp   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="1e9d3-448">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="1e9d3-449">Använd vanligt aviseringsschema som är aktiverat för mottagarna.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-449">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="1e9d3-450">Detta gäller inte för SMS, push för Azure-app, ITSM och röstmottagare</span><span class="sxs-lookup"><span data-stu-id="1e9d3-450">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="1e9d3-451">Webhooks har nu stöd för Azure Active Directory-autentisering.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-451">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1e9d3-452">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1e9d3-452">Az.Network</span></span>
* <span data-ttu-id="1e9d3-453">Lägg till ny cmdlet Get-AzAvailableServiceAlias som kan anropas för att hämta de alias som kan användas för tjänstslutpunktsprinciper.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-453">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="1e9d3-454">Stöd för tillägg av trafikväljare har lagts till i gatewayanslutningar för virtuella nätverk</span><span class="sxs-lookup"><span data-stu-id="1e9d3-454">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="1e9d3-455">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="1e9d3-455">New cmdlets added:</span></span>
        - <span data-ttu-id="1e9d3-456">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="1e9d3-456">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="1e9d3-457">Cmdletar har uppdaterats med valfri parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="1e9d3-457">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="1e9d3-458">Lägg till stöd för ESP- och AH-protokoll i konfiguration av nätverkssäkerhetsregler</span><span class="sxs-lookup"><span data-stu-id="1e9d3-458">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="1e9d3-459">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="1e9d3-459">Updated cmdlets:</span></span>
        - <span data-ttu-id="1e9d3-460">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1e9d3-460">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="1e9d3-461">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1e9d3-461">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="1e9d3-462">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1e9d3-462">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="1e9d3-463">Förbättra hanteringen av undantag i Cortex-cmdletar</span><span class="sxs-lookup"><span data-stu-id="1e9d3-463">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="1e9d3-464">Nya generationer och SKU:er för VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="1e9d3-464">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="1e9d3-465">Introducera nya generationer för VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-465">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="1e9d3-466">Introducera nya SKU:er med högt dataflöde för VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-466">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="1e9d3-467">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="1e9d3-467">Az.RedisCache</span></span>
* <span data-ttu-id="1e9d3-468">Uppdaterad referensdokumentation för ”set-AzRedisCache” för att inkludera saknade värden för parametern ”size”</span><span class="sxs-lookup"><span data-stu-id="1e9d3-468">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="1e9d3-469">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1e9d3-469">Az.Sql</span></span>
* <span data-ttu-id="1e9d3-470">Lägg till stöd för inställningen Active Directory administratör på den hanterade instansen</span><span class="sxs-lookup"><span data-stu-id="1e9d3-470">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1e9d3-471">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1e9d3-471">Az.Storage</span></span>
* <span data-ttu-id="1e9d3-472">Uppdatera Lagringsklientbibliotek till 11.1.0</span><span class="sxs-lookup"><span data-stu-id="1e9d3-472">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="1e9d3-473">Lista containrar med hanteringsplans-API, kommer att listas med NextPageLink</span><span class="sxs-lookup"><span data-stu-id="1e9d3-473">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="1e9d3-474">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="1e9d3-474">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="1e9d3-475">Lista lagringskonton från prenumerationen, kommer att listas med NextPageLink</span><span class="sxs-lookup"><span data-stu-id="1e9d3-475">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="1e9d3-476">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1e9d3-476">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="1e9d3-477">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="1e9d3-477">Az.StorageSync</span></span>
* <span data-ttu-id="1e9d3-478">Åtgärda problemet 9810 i Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-478">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1e9d3-479">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1e9d3-479">Az.Websites</span></span>
* <span data-ttu-id="1e9d3-480">Set-AzWebApp – uppdatering av ASP för en app misslyckades</span><span class="sxs-lookup"><span data-stu-id="1e9d3-480">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="1e9d3-481">2.7.0 – september 2019</span><span class="sxs-lookup"><span data-stu-id="1e9d3-481">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="1e9d3-482">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="1e9d3-482">Az.ApiManagement</span></span>
* <span data-ttu-id="1e9d3-483">Uppdatera ”-Format”-parameterbeskrivningen i ”Set-AzApiManagementPolicy”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="1e9d3-483">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="1e9d3-484">Referenser för den föråldrade cmdleten ”Update-AzApiManagementDeployment” har tagits bort från referensdokumentationen.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-484">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="1e9d3-485">Använd ”Set-AzApiManagement” i stället.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-485">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="1e9d3-486">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1e9d3-486">Az.Automation</span></span>
* <span data-ttu-id="1e9d3-487">Stavfel har korrigerats i exempel i referensdokumentationen för ”Register-AzAutomationDscNode”</span><span class="sxs-lookup"><span data-stu-id="1e9d3-487">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="1e9d3-488">Klargörande har lagts till om OS-begränsningar för Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="1e9d3-488">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="1e9d3-489">Null-referensundantag har korrigerats för -Wait-alternativet i Start-AzAutomationRunbook-cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-489">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1e9d3-490">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1e9d3-490">Az.Compute</span></span>
* <span data-ttu-id="1e9d3-491">Lägg till UploadSizeInBytes-parameter till New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="1e9d3-491">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="1e9d3-492">Lägg till Incremental-parameter till New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="1e9d3-492">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="1e9d3-493">Lägg till en funktion för virtuella datorer med låg prioritet:</span><span class="sxs-lookup"><span data-stu-id="1e9d3-493">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="1e9d3-494">MaxPrice-, EvictionPolicy- och Priority-parametrar har lagts till i New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-494">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="1e9d3-495">MaxPrice-parametern har lagts till i New-AzVmssConfig-, Update-AzVM- och Update-AzVmss-cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-495">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="1e9d3-496">Åtgärda problem med VM-referenser för Get-AzAvailabilitySet-cmdleten när alla tillgänglighetsuppsättningar i prenumerationen visas.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-496">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="1e9d3-497">Korrigera null-undantaget för Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-497">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="1e9d3-498">Korrigera VHD-metoden för sökning relativt till slut.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-498">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="1e9d3-499">Åtgärda UltraSSD-problem för New-AzVM och Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-499">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1e9d3-500">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1e9d3-500">Az.DataFactory</span></span>
* <span data-ttu-id="1e9d3-501">Lägger till 3 nya kommandon för ADF V2 – Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription och Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="1e9d3-501">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="1e9d3-502">ADF .Net SDK har uppdaterats till 4.1.3</span><span class="sxs-lookup"><span data-stu-id="1e9d3-502">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="1e9d3-503">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="1e9d3-503">Az.HDInsight</span></span>
* <span data-ttu-id="1e9d3-504">Anrop för icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="1e9d3-504">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="1e9d3-505">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="1e9d3-505">Az.IotHub</span></span>
* <span data-ttu-id="1e9d3-506">Lägg till stöd för att anropa redundans för en IotHub till den geo-länkade katastrofåterställningsregionen.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-506">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="1e9d3-507">Lägg till stöd för att hantera meddelandeberikning för en IotHub.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-507">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="1e9d3-508">Nya cmdlet:ar är:</span><span class="sxs-lookup"><span data-stu-id="1e9d3-508">New cmdlets are:</span></span>
    - <span data-ttu-id="1e9d3-509">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="1e9d3-509">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="1e9d3-510">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="1e9d3-510">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="1e9d3-511">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="1e9d3-511">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="1e9d3-512">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="1e9d3-512">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="1e9d3-513">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="1e9d3-513">Az.Monitor</span></span>
* <span data-ttu-id="1e9d3-514">Pekar på den senaste Monitor SDK:n, dvs. 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="1e9d3-514">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="1e9d3-515">Lägger till bakåtkompatibla ändringar i Metrics-cmdletarna, dvs. enhetsuppräkningen stöder flera nya värden.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-515">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="1e9d3-516">Detta är skrivskyddade cmdletar, så det förekommer inga ändringar i inmatningen för cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-516">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="1e9d3-517">API-versionen för **ActionGroups**-begäranden är nu **2019-06-01**. Tidigare var den **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-517">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="1e9d3-518">Test av scenarier har uppdaterats för att anpassas till den här ändringen.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-518">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="1e9d3-519">Ett nytt obligatoriskt argument har lagts till för konstruktorerna för klasserna **EmailReceiver** och **WebhookReceiver** – ett booleskt värde med namnet **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-519">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="1e9d3-520">Värdet är för närvarande fast till **false** så att den här icke-bakåtkompatibla ändringen är dold från cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-520">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="1e9d3-521">**Obs!** Det här är en tillfällig ändring som måste verifieras av Alerts-teamet.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-521">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="1e9d3-522">Ordningen på argumenten för konstruktorn för klassen **Source** (relaterad till klassen **ScheduledQueryRuleSource**) har ändrats från den tidigare SDK:n.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-522">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="1e9d3-523">Den här ändringen krävde korrigering av två enhetstest: de kompilerades, men testerna skickades inte.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-523">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="1e9d3-524">Ordningen på argumenten för konstruktorn för klassen **AlertingAction** (relaterad till klassen **ScheduledQueryRuleSource**) har ändrats från den tidigare SDK:n.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-524">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="1e9d3-525">Den här ändringen krävde korrigering av två enhetstest: de kompilerades, men testerna skickades inte.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-525">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="1e9d3-526">Stöd för kriterier för dynamiskt tröskelvärde för måttavisering v2</span><span class="sxs-lookup"><span data-stu-id="1e9d3-526">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="1e9d3-527">New-AzMetricAlertRuleV2Criteria: skapar nu även kriterier för dynamiskt tröskelvärde</span><span class="sxs-lookup"><span data-stu-id="1e9d3-527">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="1e9d3-528">Add-AzMetricAlertRuleV2: accepterar nu även kriterier för dynamiskt tröskelvärde</span><span class="sxs-lookup"><span data-stu-id="1e9d3-528">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="1e9d3-529">Förbättringar i schemalagd frågeregel (SQR)</span><span class="sxs-lookup"><span data-stu-id="1e9d3-529">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="1e9d3-530">Cmdletar accepterar ”Location”-parameter i båda formaten, antingen platsen (t.ex. eastus) eller platsens visningsnamn (t.ex. USA, östra)</span><span class="sxs-lookup"><span data-stu-id="1e9d3-530">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="1e9d3-531">”Enabled”-parametern illustreras korrekt i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="1e9d3-531">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="1e9d3-532">Exempel för den valfria parametern ”ActionGroup” har lagts till</span><span class="sxs-lookup"><span data-stu-id="1e9d3-532">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="1e9d3-533">Förbättrade hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="1e9d3-533">Overall improved help files</span></span>
* <span data-ttu-id="1e9d3-534">Åtgärda bugg då omfattningstypen fastställs för ”Set-AzActionRule”</span><span class="sxs-lookup"><span data-stu-id="1e9d3-534">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1e9d3-535">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1e9d3-535">Az.Network</span></span>
* <span data-ttu-id="1e9d3-536">Korrigera felaktigt exempel i referensdokumentationen för ”New-AzApplicationGateway”</span><span class="sxs-lookup"><span data-stu-id="1e9d3-536">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="1e9d3-537">Lägg till anmärkning i ”Get-AzNetworkWatcherPacketCapture”-referensdokumentationen om hämtning av alla egenskaper för en paketinsamling</span><span class="sxs-lookup"><span data-stu-id="1e9d3-537">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="1e9d3-538">Exempel har korrigerats i ”Test-AzNetworkWatcherIPFlow”-referensdokumentationen för korrekt uppräkning av nätverkskort</span><span class="sxs-lookup"><span data-stu-id="1e9d3-538">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="1e9d3-539">Förbättrad tolkning av molnundantag för att visa eventuell ytterligare information</span><span class="sxs-lookup"><span data-stu-id="1e9d3-539">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="1e9d3-540">Förbättrad tolkning av molnundantag för att hantera ytterligare en typ av SDK-undantag</span><span class="sxs-lookup"><span data-stu-id="1e9d3-540">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="1e9d3-541">Felaktig mappning av säkerhetsregelmodeller har korrigerats</span><span class="sxs-lookup"><span data-stu-id="1e9d3-541">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="1e9d3-542">Egenskaper har lagts till för nätverksgränssnittet för funktionen Privat IP</span><span class="sxs-lookup"><span data-stu-id="1e9d3-542">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="1e9d3-543">Egenskapen ”PrivateEndpoint” har lagts till som en typ av PSResourceId till PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="1e9d3-543">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="1e9d3-544">Egenskapen ”PrivateLinkConnectionProperties” har lagts till som en typ av PSIpConfigurationConnectivityInformation till PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="1e9d3-544">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="1e9d3-545">Modellklassen PSIpConfigurationConnectivityInformation har lagts till</span><span class="sxs-lookup"><span data-stu-id="1e9d3-545">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="1e9d3-546">ApplicationRuleProtocolType ”mssql” har lagts till för Azure Firewall-resurs</span><span class="sxs-lookup"><span data-stu-id="1e9d3-546">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="1e9d3-547">MultiLink-stöd i virtuellt WAN</span><span class="sxs-lookup"><span data-stu-id="1e9d3-547">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="1e9d3-548">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="1e9d3-548">New cmdlets</span></span>
        - <span data-ttu-id="1e9d3-549">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="1e9d3-549">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="1e9d3-550">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="1e9d3-550">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="1e9d3-551">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="1e9d3-551">Updated cmdlet:</span></span>
        - <span data-ttu-id="1e9d3-552">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="1e9d3-552">New-VpnSite</span></span>
        - <span data-ttu-id="1e9d3-553">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="1e9d3-553">Update-VpnSite</span></span>
        - <span data-ttu-id="1e9d3-554">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="1e9d3-554">New-VpnConnection</span></span>
        - <span data-ttu-id="1e9d3-555">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="1e9d3-555">Update-VpnConnection</span></span>
* <span data-ttu-id="1e9d3-556">Dokument för vissa PowerShell-exempel har korrigerats så att Az-cmdletar används i stället för AzureRM-cmdletar</span><span class="sxs-lookup"><span data-stu-id="1e9d3-556">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1e9d3-557">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1e9d3-557">Az.RecoveryServices</span></span>
* <span data-ttu-id="1e9d3-558">Uppdatera AzureVMpolicy-objekt med ProtectedItemsCount-attribut</span><span class="sxs-lookup"><span data-stu-id="1e9d3-558">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="1e9d3-559">Ytterligare tester har lagts till för VM-princip och återställning av ursprungligt lagringskonto</span><span class="sxs-lookup"><span data-stu-id="1e9d3-559">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="1e9d3-560">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1e9d3-560">Az.Resources</span></span>
* <span data-ttu-id="1e9d3-561">Åtgärda fel där det inte gick att anropa New-AzRoleAssignment utan parametern Scope.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-561">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="1e9d3-562">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1e9d3-562">Az.ServiceFabric</span></span>
* <span data-ttu-id="1e9d3-563">Stavfel har korrigerats i exempel för ”Update-AzServiceFabricReliability”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="1e9d3-563">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="1e9d3-564">Lägger till nya cmdletar för att hantera program och tjänster:</span><span class="sxs-lookup"><span data-stu-id="1e9d3-564">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="1e9d3-565">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="1e9d3-565">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="1e9d3-566">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="1e9d3-566">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="1e9d3-567">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="1e9d3-567">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="1e9d3-568">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="1e9d3-568">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="1e9d3-569">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="1e9d3-569">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="1e9d3-570">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="1e9d3-570">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="1e9d3-571">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="1e9d3-571">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="1e9d3-572">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="1e9d3-572">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="1e9d3-573">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="1e9d3-573">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="1e9d3-574">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="1e9d3-574">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="1e9d3-575">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="1e9d3-575">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="1e9d3-576">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="1e9d3-576">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="1e9d3-577">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="1e9d3-577">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="1e9d3-578">Service Fabric SDK har uppgraderats till version 1.2.0 som använder Service Fabric-resursprovidern med API-version 2019-03-01.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-578">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="1e9d3-579">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="1e9d3-579">Az.SignalR</span></span>
* <span data-ttu-id="1e9d3-580">Lägg till Update-, Restart-, CheckNameAvailability- och GetUsage-cmdletar</span><span class="sxs-lookup"><span data-stu-id="1e9d3-580">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="1e9d3-581">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1e9d3-581">Az.Sql</span></span>
* <span data-ttu-id="1e9d3-582">Uppdatera exempel i referensdokumentationen för ”Get-AzSqlElasticPool”</span><span class="sxs-lookup"><span data-stu-id="1e9d3-582">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="1e9d3-583">vCore-exempel för att skapa en elastisk pool (New-AzSqlElasticPool) har lagts till.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-583">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="1e9d3-584">Ta bort verifieringen av EmailAddresses och kontrollen som bekräftar att EmailAdmins inte är falskt när EmailAddresses är tomt i Set-AzSqlServerAdvancedThreatProtectionPolicy och Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="1e9d3-584">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="1e9d3-585">Server-/databasgranskningsinställningar kan tas bort när det finns flera diagnostikinställningar som aktiverar granskningskategorin.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-585">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="1e9d3-586">Åtgärda verifiering av e-postadresser i flera Sql Vulnerability Assessment-cmdletar (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting och Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="1e9d3-586">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1e9d3-587">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1e9d3-587">Az.Storage</span></span>
* <span data-ttu-id="1e9d3-588">Exempel i referensdokumentationen för ”Get-AzStorageAccountKey” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="1e9d3-588">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="1e9d3-589">Vid upp- och nedladdning av en Azure-fil kan SMB-egenskaperna för källfilen (t.ex. filattribut, tidpunkten då filen skapades och tidpunkten för den senaste skrivningen) sparas i målfilen</span><span class="sxs-lookup"><span data-stu-id="1e9d3-589">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="1e9d3-590">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="1e9d3-590">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="1e9d3-591">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="1e9d3-591">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="1e9d3-592">Korrigera problem med uppladdningen av blockblob med egenskaper/metadata för ImmutabilityPolicy i containrar.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-592">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="1e9d3-593">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="1e9d3-593">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="1e9d3-594">Stöd för hantering av Azure-filresurser med API för hanteringsplan</span><span class="sxs-lookup"><span data-stu-id="1e9d3-594">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="1e9d3-595">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="1e9d3-595">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="1e9d3-596">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="1e9d3-596">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="1e9d3-597">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="1e9d3-597">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="1e9d3-598">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="1e9d3-598">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1e9d3-599">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1e9d3-599">Az.Websites</span></span>
* <span data-ttu-id="1e9d3-600">Åtgärdar problemet där webapp-taggar togs bort när appen migrerades till nya ASP</span><span class="sxs-lookup"><span data-stu-id="1e9d3-600">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="1e9d3-601">Åtgärda Publish-AzureWebapp så att det fungerar i Linux och Windows</span><span class="sxs-lookup"><span data-stu-id="1e9d3-601">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="1e9d3-602">Uppdatera exempel i ”Get-AzWebAppPublishingProfile”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="1e9d3-602">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="1e9d3-603">2.6.0 – augusti 2019</span><span class="sxs-lookup"><span data-stu-id="1e9d3-603">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="1e9d3-604">Allmänt</span><span class="sxs-lookup"><span data-stu-id="1e9d3-604">General</span></span>
* <span data-ttu-id="1e9d3-605">Åtgärdade diverse skrivfel i flera moduler</span><span class="sxs-lookup"><span data-stu-id="1e9d3-605">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="1e9d3-606">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1e9d3-606">Az.Accounts</span></span>
* <span data-ttu-id="1e9d3-607">Stöd för användartilldelat MSI i Azure Functions-autentisering (#9479)</span><span class="sxs-lookup"><span data-stu-id="1e9d3-607">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="1e9d3-608">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="1e9d3-608">Az.Aks</span></span>
* <span data-ttu-id="1e9d3-609">Åtgärda problem med utdata för "Get-AzAks"</span><span class="sxs-lookup"><span data-stu-id="1e9d3-609">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="1e9d3-610">Mer information här: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="1e9d3-610">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="1e9d3-611">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="1e9d3-611">Az.ApiManagement</span></span>
* <span data-ttu-id="1e9d3-612">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="1e9d3-612">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="1e9d3-613">Uppdatera .net-NuGet-versionen, som inte tillämpar begränsningar för productId, apiId och userId</span><span class="sxs-lookup"><span data-stu-id="1e9d3-613">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="1e9d3-614">**Get-AzApiManagementProduct** – Lade till stöd för frågekörning mot produkter via API.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-614">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="1e9d3-615">**New-AzApiManagementApiRevision** – Korrigering för problem där ApiRevisionDescription inte angavs vid skapande av ny API-revision https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="1e9d3-615">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="1e9d3-616">Åtgärdade skrivfel i modellen "PsApiManagementOAuth2AuthrozationServer" till "PsApiManagementOAuth2AuthorizationServer"</span><span class="sxs-lookup"><span data-stu-id="1e9d3-616">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="1e9d3-617">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="1e9d3-617">Az.Batch</span></span>
* <span data-ttu-id="1e9d3-618">Åtgärdade skrivfel i hjälpmeddelande och dokumentation till att skriva Windows med versaler</span><span class="sxs-lookup"><span data-stu-id="1e9d3-618">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="1e9d3-619">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="1e9d3-619">Az.Cdn</span></span>
* <span data-ttu-id="1e9d3-620">Åtgärdade skrivfel i CDN-modulens konverteringshjälp</span><span class="sxs-lookup"><span data-stu-id="1e9d3-620">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1e9d3-621">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1e9d3-621">Az.Compute</span></span>
* <span data-ttu-id="1e9d3-622">Lägg till VmssId i New-AzVMConfig-cmdleten</span><span class="sxs-lookup"><span data-stu-id="1e9d3-622">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="1e9d3-623">Lägg till parametrarna TerminateScheduledEvents och TerminateScheduledEventNotBeforeTimeoutInMinutes i New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="1e9d3-623">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="1e9d3-624">Lägg till egenskapen HyperVGeneration till avbildningsobjekt för virtuell dator</span><span class="sxs-lookup"><span data-stu-id="1e9d3-624">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="1e9d3-625">Lägg till funktioner för Host och HostGroup</span><span class="sxs-lookup"><span data-stu-id="1e9d3-625">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="1e9d3-626">Nya cmdletar:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="1e9d3-626">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="1e9d3-627">HostId-parametern läggs till i New-AzVMConfig och New-AzVM</span><span class="sxs-lookup"><span data-stu-id="1e9d3-627">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="1e9d3-628">Uppdatera exempel i "Invoke-AzVMRunCommand"-dokumentationen till att använda rätt parameternamn</span><span class="sxs-lookup"><span data-stu-id="1e9d3-628">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="1e9d3-629">Uppdatera "-VolumeType"-beskrivningen i referensdokumentationen för "set-AzVMDiskEncryptionExtension" och "set-AzVmssDiskEncryptionExtension"</span><span class="sxs-lookup"><span data-stu-id="1e9d3-629">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1e9d3-630">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1e9d3-630">Az.DataFactory</span></span>
* <span data-ttu-id="1e9d3-631">Åtgärda skrivfel till att använda versaler för "Windows" i "New-AzDataFactoryEncryptValue"-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="1e9d3-631">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="1e9d3-632">Uppdaterade ADF .Net SDK-versionen till 4.1.2</span><span class="sxs-lookup"><span data-stu-id="1e9d3-632">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="1e9d3-633">Lägg till parametrarna "DataProxyIntegrationRuntimeName", "DataProxyStagingLinkedServiceName" och "DataProxyStagingPath" för "Set-AzureRmDataFactoryV2IntegrationRuntime"-cmd för att aktivera konfiguration av lokalt installerad integrationskörning som en proxy för SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="1e9d3-633">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="1e9d3-634">Uppdaterade PSTriggerRun till att visa utlöst pipeline, meddelande och egenskaper samt PSActivityRun till att visa aktivitetstypen</span><span class="sxs-lookup"><span data-stu-id="1e9d3-634">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="1e9d3-635">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1e9d3-635">Az.DataLakeStore</span></span>
* <span data-ttu-id="1e9d3-636">Korrigering av frysning av Get-DataLakeStoreDeletedItem för fel eller fjärrundantag.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-636">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="1e9d3-637">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="1e9d3-637">Az.EventHub</span></span>
* <span data-ttu-id="1e9d3-638">Korrigering av problem #9658 : Skrivfel i parametern VirtualNteworkRule i Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="1e9d3-638">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="1e9d3-639">Korrigering av problem #9558 : Set-AzEventHubNamespace använder PATCH i stället för PUT</span><span class="sxs-lookup"><span data-stu-id="1e9d3-639">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="1e9d3-640">lade till parametern EnableKafka i Set-AzEventHubNamespace-cmdleten</span><span class="sxs-lookup"><span data-stu-id="1e9d3-640">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="1e9d3-641">Korrigering av problem #9786 : kan inte skapa en regel med Endast lyssna-behörighet</span><span class="sxs-lookup"><span data-stu-id="1e9d3-641">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="1e9d3-642">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="1e9d3-642">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="1e9d3-643">Åtgärdade skrivfel i dokumentation där "Azure" skrevs helt med gemener</span><span class="sxs-lookup"><span data-stu-id="1e9d3-643">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="1e9d3-644">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="1e9d3-644">Az.Monitor</span></span>
* <span data-ttu-id="1e9d3-645">Åtgärdade felaktigt parameternamn i hjälpdokumentationen</span><span class="sxs-lookup"><span data-stu-id="1e9d3-645">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1e9d3-646">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1e9d3-646">Az.Network</span></span>
* <span data-ttu-id="1e9d3-647">Uppdaterade New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="1e9d3-647">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="1e9d3-648">Gjorde parametern "PublicIpAddress" inaktuell eftersom den aldrig används på serversidan.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-648">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="1e9d3-649">Lade till den valfria parametern "Primary", som anger huruvida den aktuella IP-konfigurationen är den primära.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-649">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="1e9d3-650">Förbättrade hanteringen av felundantag för begärande från SDK – åtgärdar problemet att tidigare SDK-undantag inte hanteras på rätt sätt, vilket leder till att viktig felinformation inte visas</span><span class="sxs-lookup"><span data-stu-id="1e9d3-650">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="1e9d3-651">Justerade valideringslogiken för IPv6-IP-prefix till att kontrollera korrekt IPv6-prefixlängd.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-651">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="1e9d3-652">Uppdaterade Get-AzVirtualNetworkSubnetConfig: Lade till parameter som anges till get av undernätets resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-652">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="1e9d3-653">Uppdaterade beskrivningen av parametern Location för AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="1e9d3-653">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="1e9d3-654">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="1e9d3-654">Az.OperationalInsights</span></span>
* <span data-ttu-id="1e9d3-655">Uppdaterade dokumentation för "New-AzOperationalInsightsLinuxSyslogDataSource"</span><span class="sxs-lookup"><span data-stu-id="1e9d3-655">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="1e9d3-656">Lade till exempel</span><span class="sxs-lookup"><span data-stu-id="1e9d3-656">Added example</span></span>
    - <span data-ttu-id="1e9d3-657">Uppdaterade beskrivningen av parametern "-Name"</span><span class="sxs-lookup"><span data-stu-id="1e9d3-657">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="1e9d3-658">Lade till ett exempel för New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="1e9d3-658">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="1e9d3-659">Ändrade beskrivningen av parametern -Name för New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="1e9d3-659">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1e9d3-660">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1e9d3-660">Az.RecoveryServices</span></span>
* <span data-ttu-id="1e9d3-661">Uppdatera "Get-AzRecoveryServicesBackupJobDetail.md"</span><span class="sxs-lookup"><span data-stu-id="1e9d3-661">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="1e9d3-662">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1e9d3-662">Az.Resources</span></span>
* <span data-ttu-id="1e9d3-663">Lägg till stöd för den nya API-versionen från 2019-05-10 för Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="1e9d3-663">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="1e9d3-664">Lägg till stöd för "copy.count = 0" för variabler, resurser och egenskaper</span><span class="sxs-lookup"><span data-stu-id="1e9d3-664">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="1e9d3-665">Resurser med "condition = false" eller "copy.count = 0" tas bort i complete-läget</span><span class="sxs-lookup"><span data-stu-id="1e9d3-665">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="1e9d3-666">Lägg till ett exempel på tilldelning av princip på prenumerationsnivå i hjälpdokumentationen</span><span class="sxs-lookup"><span data-stu-id="1e9d3-666">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="1e9d3-667">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="1e9d3-667">Az.ServiceBus</span></span>
* <span data-ttu-id="1e9d3-668">Korrigering av problem #9658 : Skrivfel i parametern VirtualNetworkRule i set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="1e9d3-668">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="1e9d3-669">Korrigering av problem #9786 : kan inte skapa en regel med Endast lyssna-behörighet</span><span class="sxs-lookup"><span data-stu-id="1e9d3-669">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="1e9d3-670">Lade till det nya kommandot "Test-AzServiceBusNameAvailability" för att kontrollera namntillgängligheten för kö och ämne</span><span class="sxs-lookup"><span data-stu-id="1e9d3-670">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="1e9d3-671">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1e9d3-671">Az.ServiceFabric</span></span>
* <span data-ttu-id="1e9d3-672">Åtgärda buggar med tillägg av nodtyps-cmdlet:</span><span class="sxs-lookup"><span data-stu-id="1e9d3-672">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="1e9d3-673">NullReferenceException-bugg när resursgrupp hade annan vmss som inte är relaterad till Service Fabric-klustret.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-673">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="1e9d3-674">Åtgärdar problemet: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="1e9d3-674">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="1e9d3-675">Åtgärda bugg där cmdleten misslyckades om virtualNetwork var i en annan resursgrupp än klustret.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-675">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="1e9d3-676">Åtgärdar problemet: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="1e9d3-676">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="1e9d3-677">AzServiceFabricApplicationCertificate-cmdleten görs inaktuell</span><span class="sxs-lookup"><span data-stu-id="1e9d3-677">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="1e9d3-678">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1e9d3-678">Az.Sql</span></span>
* <span data-ttu-id="1e9d3-679">Uppdatera dokumentation om gamla gransknings-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-679">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1e9d3-680">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1e9d3-680">Az.Storage</span></span>
* <span data-ttu-id="1e9d3-681">Uppdatera hjälpen för Get/Close-AzStorageFileHandle genom att lägga till fler scenarier i cmdlet-exempel och uppdatera parameterbeskrivningar</span><span class="sxs-lookup"><span data-stu-id="1e9d3-681">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="1e9d3-682">Stöd för StandardBlobTier i uppladdningsblob och kopieringsblob</span><span class="sxs-lookup"><span data-stu-id="1e9d3-682">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="1e9d3-683">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="1e9d3-683">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="1e9d3-684">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="1e9d3-684">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="1e9d3-685">Stöd för rehydratiseringsprioritet i kopieringsblob</span><span class="sxs-lookup"><span data-stu-id="1e9d3-685">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="1e9d3-686">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="1e9d3-686">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1e9d3-687">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1e9d3-687">Az.Websites</span></span>
* <span data-ttu-id="1e9d3-688">Lägg till klargöranden gällande parametern -AppSettings i Set-AzWebApp och Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="1e9d3-688">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="1e9d3-689">2.5.0 – July 2019</span><span class="sxs-lookup"><span data-stu-id="1e9d3-689">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1e9d3-690">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1e9d3-690">Az.Accounts</span></span>
* <span data-ttu-id="1e9d3-691">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="1e9d3-691">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="1e9d3-692">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="1e9d3-692">Az.ApplicationInsights</span></span>
* <span data-ttu-id="1e9d3-693">Korrigera skrivfel i exempel i dokumentationen för Remove-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="1e9d3-693">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="1e9d3-694">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1e9d3-694">Az.Automation</span></span>
* <span data-ttu-id="1e9d3-695">Korrigera skrivfel i resurssträng</span><span class="sxs-lookup"><span data-stu-id="1e9d3-695">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="1e9d3-696">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="1e9d3-696">Az.CognitiveServices</span></span>
* <span data-ttu-id="1e9d3-697">Stöd för NetworkRuleSet har lagts till.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-697">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1e9d3-698">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1e9d3-698">Az.Compute</span></span>
* <span data-ttu-id="1e9d3-699">Lägg till saknade egenskaper (ComputerName, OsName, OsVersion och HyperVGeneration) för visningsobjekt i den virtuella datorinstansen.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-699">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="1e9d3-700">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1e9d3-700">Az.ContainerRegistry</span></span>
* <span data-ttu-id="1e9d3-701">Åtgärda skrivfel i Remove-AzContainerRegistryReplication för parametern Replication</span><span class="sxs-lookup"><span data-stu-id="1e9d3-701">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="1e9d3-702">Mer information finns här: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="1e9d3-702">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1e9d3-703">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1e9d3-703">Az.DataFactory</span></span>
* <span data-ttu-id="1e9d3-704">ADF .Net SDK-versionen har uppdaterats till 4.1.0</span><span class="sxs-lookup"><span data-stu-id="1e9d3-704">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="1e9d3-705">Korrigera skrivfel i dokumentationen för Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="1e9d3-705">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="1e9d3-706">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="1e9d3-706">Az.EventHub</span></span>
* <span data-ttu-id="1e9d3-707">Ny cmmdlet har lagts till för att skapa SAS-token: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="1e9d3-707">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="1e9d3-708">verifierings- och felmeddelande har lagts till för authorizationrules-rättigheter om endast "hantera" har tilldelats</span><span class="sxs-lookup"><span data-stu-id="1e9d3-708">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="1e9d3-709">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1e9d3-709">Az.KeyVault</span></span>
* <span data-ttu-id="1e9d3-710">Stöd har lagts till för att ange KeySize för certifikatprinciper</span><span class="sxs-lookup"><span data-stu-id="1e9d3-710">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="1e9d3-711">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="1e9d3-711">Az.LogicApp</span></span>
* <span data-ttu-id="1e9d3-712">Korrigering för Get-AzIntegrationAccountMap för att lista alla mappningstyper</span><span class="sxs-lookup"><span data-stu-id="1e9d3-712">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="1e9d3-713">Ny MapType-parameter har lagts till för filtrering</span><span class="sxs-lookup"><span data-stu-id="1e9d3-713">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="1e9d3-714">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="1e9d3-714">Az.ManagedServices</span></span>
* <span data-ttu-id="1e9d3-715">Stöd för API-versionen 2019-06-01 (GA) har lagts till</span><span class="sxs-lookup"><span data-stu-id="1e9d3-715">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1e9d3-716">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1e9d3-716">Az.Network</span></span>
* <span data-ttu-id="1e9d3-717">Lägg till stöd för privat slutpunkt och privat länktjänst</span><span class="sxs-lookup"><span data-stu-id="1e9d3-717">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="1e9d3-718">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="1e9d3-718">New cmdlets</span></span>
        - <span data-ttu-id="1e9d3-719">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="1e9d3-719">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="1e9d3-720">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="1e9d3-720">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="1e9d3-721">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="1e9d3-721">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="1e9d3-722">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="1e9d3-722">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="1e9d3-723">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="1e9d3-723">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="1e9d3-724">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="1e9d3-724">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="1e9d3-725">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="1e9d3-725">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="1e9d3-726">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="1e9d3-726">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="1e9d3-727">Nedanstående kommandon för funktionen har uppdaterats: Flaggan PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies på undernätet i VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="1e9d3-727">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="1e9d3-728">Uppdaterade New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="1e9d3-728">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="1e9d3-729">Valfri parameter har lagts till – PrivateEndpointNetworkPoliciesFlag som konfigurerar huruvida nätverksprinciper ska tillämpas på en privat slutpunkt i det här undernätet.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-729">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="1e9d3-730">Valfri parameter har lagts till – PrivateLinkServiceNetworkPoliciesFlag som konfigurerar huruvida nätverksprinciper ska tillämpas på en privat länktjänst i det här undernätet.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-730">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="1e9d3-731">AzPrivateLinkService för cmdlet-parametern ServiceName har bytt namn till Name med aliaset ServiceName för bakåtkompatibilitet</span><span class="sxs-lookup"><span data-stu-id="1e9d3-731">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="1e9d3-732">Aktivera ICMP-protokoll för konfiguration av nätverkssäkerhetsregler</span><span class="sxs-lookup"><span data-stu-id="1e9d3-732">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="1e9d3-733">Uppdaterade cmdletar</span><span class="sxs-lookup"><span data-stu-id="1e9d3-733">Updated cmdlets</span></span>
        - <span data-ttu-id="1e9d3-734">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1e9d3-734">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="1e9d3-735">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1e9d3-735">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="1e9d3-736">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1e9d3-736">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="1e9d3-737">Lägg till ConnectionProtocolType (Ikev1/Ikev2) som en konfigurerbar parameter för New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="1e9d3-737">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="1e9d3-738">Lägg till PrivateIpAddressVersion i LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="1e9d3-738">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="1e9d3-739">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="1e9d3-739">Updated cmdlet:</span></span>
        - <span data-ttu-id="1e9d3-740">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="1e9d3-740">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="1e9d3-741">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="1e9d3-741">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="1e9d3-742">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="1e9d3-742">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="1e9d3-743">Uppdatering av Application Gateway-kommandot New-AzApplicationGatewayProbeConfig för stöd av anpassad port i Probe</span><span class="sxs-lookup"><span data-stu-id="1e9d3-743">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="1e9d3-744">Uppdaterade New-AzApplicationGatewayProbeConfig: Den valfria parametern Port som används för avsökning i serverdelen har lagts till.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-744">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="1e9d3-745">Denna parameter gäller för SKU:erna Standard_V2 och WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-745">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="1e9d3-746">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="1e9d3-746">Az.OperationalInsights</span></span>
* <span data-ttu-id="1e9d3-747">Uppdaterade standardversionen för sparade sökningar till 1.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-747">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="1e9d3-748">Åtgärdade hantering av anpassad log null regex</span><span class="sxs-lookup"><span data-stu-id="1e9d3-748">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1e9d3-749">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1e9d3-749">Az.RecoveryServices</span></span>
* <span data-ttu-id="1e9d3-750">Uppdatera Get-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="1e9d3-750">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="1e9d3-751">Uppdatera Get-AzRecoveryServicesBackupContainer.md</span><span class="sxs-lookup"><span data-stu-id="1e9d3-751">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="1e9d3-752">Uppdatera Get-AzRecoveryServicesVault.md</span><span class="sxs-lookup"><span data-stu-id="1e9d3-752">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="1e9d3-753">Uppdatera Wait-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="1e9d3-753">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="1e9d3-754">Uppdatera Set-AzRecoveryServicesVaultContext.md</span><span class="sxs-lookup"><span data-stu-id="1e9d3-754">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="1e9d3-755">Uppdatera Get-AzRecoveryServicesBackupItem.md</span><span class="sxs-lookup"><span data-stu-id="1e9d3-755">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="1e9d3-756">Uppdatera Get-AzRecoveryServicesBackupRecoveryPoint.md</span><span class="sxs-lookup"><span data-stu-id="1e9d3-756">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="1e9d3-757">Uppdatera Restore-AzRecoveryServicesBackupItem.md</span><span class="sxs-lookup"><span data-stu-id="1e9d3-757">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="1e9d3-758">Uppdaterat tjänstanrop för avregistrering av container för Azure-filresurs</span><span class="sxs-lookup"><span data-stu-id="1e9d3-758">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="1e9d3-759">Uppdatera Set-AzRecoveryServicesAsrAlertSetting.md</span><span class="sxs-lookup"><span data-stu-id="1e9d3-759">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="1e9d3-760">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1e9d3-760">Az.Resources</span></span>
- <span data-ttu-id="1e9d3-761">Ta bort den cmdlet som saknas och som refereras i dokumentationen till New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="1e9d3-761">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="1e9d3-762">Princip-cmdletar har uppdaterats så att de använder den nya API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="1e9d3-762">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="1e9d3-763">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="1e9d3-763">Az.ServiceBus</span></span>
* <span data-ttu-id="1e9d3-764">Ny cmmdlet har lagts till för att skapa SAS-token: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="1e9d3-764">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="1e9d3-765">verifierings- och felmeddelande har lagts till för authorizationrules-rättigheter om endast "hantera" har tilldelats</span><span class="sxs-lookup"><span data-stu-id="1e9d3-765">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="1e9d3-766">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1e9d3-766">Az.Sql</span></span>
* <span data-ttu-id="1e9d3-767">Åtgärda saknade exempel för Set-AzSqlDatabaseSecondary cmdlet</span><span class="sxs-lookup"><span data-stu-id="1e9d3-767">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="1e9d3-768">Åtgärda angivna återkommande genomsökningar för bedömning av säkerhetsrisk utan angivna e-postadresser</span><span class="sxs-lookup"><span data-stu-id="1e9d3-768">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="1e9d3-769">Korrigera ett skrivfel i ett varningsmeddelande.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-769">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1e9d3-770">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1e9d3-770">Az.Storage</span></span>
* <span data-ttu-id="1e9d3-771">Uppdatera exempel i referensdokumentationen för Get-AzStorageAccount så att rätt parameternamn används</span><span class="sxs-lookup"><span data-stu-id="1e9d3-771">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="1e9d3-772">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="1e9d3-772">Az.StorageSync</span></span>
* <span data-ttu-id="1e9d3-773">Lägger till cmdleten Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-773">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="1e9d3-774">Åtgärda problem 9551 så att TierFilesOlderThanDays föredras</span><span class="sxs-lookup"><span data-stu-id="1e9d3-774">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1e9d3-775">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1e9d3-775">Az.Websites</span></span>
* <span data-ttu-id="1e9d3-776">Åtgärdar ett fel där vissa SiteConfig-egenskaper inte returnerades av Get-AzWebApp och Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="1e9d3-776">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="1e9d3-777">Lägger till en ny platsparameter för Get-AzDeletedWebApp och Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="1e9d3-777">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="1e9d3-778">Åtgärdar ett fel i kloning av webbapp-platser som använder New-AzWebApp-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="1e9d3-778">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="1e9d3-779">2.4.0 – juli 2019</span><span class="sxs-lookup"><span data-stu-id="1e9d3-779">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1e9d3-780">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1e9d3-780">Az.Accounts</span></span>
* <span data-ttu-id="1e9d3-781">Lägg till stöd för profil-cmdletar</span><span class="sxs-lookup"><span data-stu-id="1e9d3-781">Add support for profile cmdlets</span></span>
* <span data-ttu-id="1e9d3-782">Lägg till stöd för miljöer och dataplaner i genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="1e9d3-782">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="1e9d3-783">Åtgärda bugg där fel slutpunkt i vissa fall användes för cmdletar för dataplaner i Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="1e9d3-783">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="1e9d3-784">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="1e9d3-784">Az.Advisor</span></span>
* <span data-ttu-id="1e9d3-785">GA-version av Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="1e9d3-785">GA release of Az.Advisor</span></span>
* <span data-ttu-id="1e9d3-786">Den här modulen ingår nu som en del av `Az`-sammanslagningsmodulen</span><span class="sxs-lookup"><span data-stu-id="1e9d3-786">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="1e9d3-787">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="1e9d3-787">Az.ApiManagement</span></span>
* <span data-ttu-id="1e9d3-788">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="1e9d3-788">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="1e9d3-789">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="1e9d3-789">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="1e9d3-790">Stöd för att fråga prenumerationer efter användare och produkt har lagts till</span><span class="sxs-lookup"><span data-stu-id="1e9d3-790">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="1e9d3-791">Stöd för att fråga med hjälp av omfång ”/”, ”/apis”, ”/apis/echo-api” har lagts till</span><span class="sxs-lookup"><span data-stu-id="1e9d3-791">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="1e9d3-792">Korrigering av problem https://github.com/Azure/azure-powershell/issues/9307 och https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="1e9d3-792">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="1e9d3-793">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="1e9d3-793">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="1e9d3-794">Stöd för att ange ”ApiVersion” och ”ApiVersionSetId” när API:er importeras har lagts till</span><span class="sxs-lookup"><span data-stu-id="1e9d3-794">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="1e9d3-795">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1e9d3-795">Az.Automation</span></span>
* <span data-ttu-id="1e9d3-796">Bugg med cmdleten Set-AzAutomationConnectionFieldValue för att hantera strängvärde har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-796">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1e9d3-797">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1e9d3-797">Az.Compute</span></span>
* <span data-ttu-id="1e9d3-798">Lägg till parametern HyperVGeneration i New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="1e9d3-798">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1e9d3-799">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1e9d3-799">Az.DataFactory</span></span>
* <span data-ttu-id="1e9d3-800">Uppdaterar utdata från ADF-cmdletar som hämtar aktivitetskörningar, hämtar pipelinekörningar och hämtar utlösarkörningar för stöd för Select-Object-pipe.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-800">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="1e9d3-801">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="1e9d3-801">Az.EventGrid</span></span>
* <span data-ttu-id="1e9d3-802">Korrigera stavfel i dokumentation om ”New-AzEventGridSubscription”</span><span class="sxs-lookup"><span data-stu-id="1e9d3-802">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="1e9d3-803">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="1e9d3-803">Az.IotHub</span></span>
* <span data-ttu-id="1e9d3-804">Lägg till stöd för att återskapa principnycklar för auktorisering.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-804">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1e9d3-805">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1e9d3-805">Az.Network</span></span>
* <span data-ttu-id="1e9d3-806">”RoutingPreference” har lagts till i offentliga IP-taggar</span><span class="sxs-lookup"><span data-stu-id="1e9d3-806">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="1e9d3-807">Förbättra exempel för referensdokumentation om ”Get-AzNetworkServiceTag”</span><span class="sxs-lookup"><span data-stu-id="1e9d3-807">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="1e9d3-808">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="1e9d3-808">Az.PolicyInsights</span></span>
* <span data-ttu-id="1e9d3-809">Åtgärda problem med null-referens i Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="1e9d3-809">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="1e9d3-810">Mer information här: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="1e9d3-810">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="1e9d3-811">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="1e9d3-811">Az.OperationalInsights</span></span>
* <span data-ttu-id="1e9d3-812">Modellen för CustomLog-datakälla som returneras i Get-AzOperationalInsightsDataSource har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="1e9d3-812">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1e9d3-813">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1e9d3-813">Az.RecoveryServices</span></span>
* <span data-ttu-id="1e9d3-814">Kommandot get-policy för IaaSVM:er har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="1e9d3-814">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="1e9d3-815">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1e9d3-815">Az.Resources</span></span>
    - <span data-ttu-id="1e9d3-816">Korrigera hjälptext för den översta parametern i Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="1e9d3-816">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="1e9d3-817">Lägg till växlingsstöd på klientsidan för Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="1e9d3-817">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="1e9d3-818">Lägg till nya parametrar för Set-AzPolicyAssignment, -PolicyParameters och -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="1e9d3-818">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="1e9d3-819">En mängd dokument- och exempeluppdateringar för Policy-cmdletar</span><span class="sxs-lookup"><span data-stu-id="1e9d3-819">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="1e9d3-820">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="1e9d3-820">Az.ServiceBus</span></span>
* <span data-ttu-id="1e9d3-821">Korrigering av problem #4938 – New-AzureRmServiceBusQueue returnerar BadRequest vid konfiguration av MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="1e9d3-821">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="1e9d3-822">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1e9d3-822">Az.Sql</span></span>
* <span data-ttu-id="1e9d3-823">Lägg till cmdletar för instansredundansgrupper från förhandsversion till offentlig version</span><span class="sxs-lookup"><span data-stu-id="1e9d3-823">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="1e9d3-824">Stöd för granskning för Azure SQL Server\Database med nya cmdletar.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-824">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="1e9d3-825">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="1e9d3-825">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="1e9d3-826">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="1e9d3-826">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="1e9d3-827">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="1e9d3-827">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="1e9d3-828">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="1e9d3-828">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="1e9d3-829">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="1e9d3-829">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="1e9d3-830">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="1e9d3-830">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="1e9d3-831">Ta bort begränsningar för e-post från inställningarna för sårbarhetsbedömning</span><span class="sxs-lookup"><span data-stu-id="1e9d3-831">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1e9d3-832">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1e9d3-832">Az.Storage</span></span>
* <span data-ttu-id="1e9d3-833">Ändra två parametrar ”-IndexDocument” och ”-ErrorDocument404Path” från ”krävs” till ”valfri” i cmdlet:</span><span class="sxs-lookup"><span data-stu-id="1e9d3-833">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="1e9d3-834">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="1e9d3-834">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="1e9d3-835">Uppdatera hjälpen för Get-AzStorageBlobContent genom att lägga till ett exempel</span><span class="sxs-lookup"><span data-stu-id="1e9d3-835">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="1e9d3-836">Visa mer felinformation när cmdleten misslyckas med StorageException</span><span class="sxs-lookup"><span data-stu-id="1e9d3-836">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="1e9d3-837">Stöd för att skapa eller uppdatera lagringskonto med Azure Files AAD DS-autentisering</span><span class="sxs-lookup"><span data-stu-id="1e9d3-837">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="1e9d3-838">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1e9d3-838">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="1e9d3-839">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1e9d3-839">Set-AzStorageAccount</span></span>
* <span data-ttu-id="1e9d3-840">Stöd för att lista eller stänga filreferenser för en filresurs, filkatalog eller en fil</span><span class="sxs-lookup"><span data-stu-id="1e9d3-840">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="1e9d3-841">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="1e9d3-841">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="1e9d3-842">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="1e9d3-842">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="1e9d3-843">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="1e9d3-843">Az.StorageSync</span></span>
* <span data-ttu-id="1e9d3-844">Den här modulen ingår nu som en del av `Az`-sammanslagningsmodulen</span><span class="sxs-lookup"><span data-stu-id="1e9d3-844">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="1e9d3-845">2.3.2 – juni 2019</span><span class="sxs-lookup"><span data-stu-id="1e9d3-845">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1e9d3-846">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1e9d3-846">Az.Accounts</span></span>
* <span data-ttu-id="1e9d3-847">Åtgärda bugg med felaktiga webbadresser som i vissa fall användes för Functions-anrop</span><span class="sxs-lookup"><span data-stu-id="1e9d3-847">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="1e9d3-848">Mer information här: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="1e9d3-848">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="1e9d3-849">Åtgärda problem med alias från AzureRM i Az-cmdletar</span><span class="sxs-lookup"><span data-stu-id="1e9d3-849">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="1e9d3-850">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="1e9d3-850">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="1e9d3-851">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="1e9d3-851">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1e9d3-852">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1e9d3-852">Az.Compute</span></span>
* <span data-ttu-id="1e9d3-853">Parameteruppsättningarna New-AzVm och New-AzVmss accepterar nu parametern ”ProximityPlacementGroup”.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-853">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="1e9d3-854">Stavfel i referensdokumentationen för ”New-AzVM” har korrigerats</span><span class="sxs-lookup"><span data-stu-id="1e9d3-854">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="1e9d3-855">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="1e9d3-855">Az.Dns</span></span>
* <span data-ttu-id="1e9d3-856">Stavfel i hjälpexempel för ”Set-AzDnsZone” har korrigerats.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-856">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="1e9d3-857">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="1e9d3-857">Az.EventGrid</span></span>
* <span data-ttu-id="1e9d3-858">Har uppdaterats för att använda API-versionen 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-858">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="1e9d3-859">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="1e9d3-859">New cmdlets:</span></span>
    - <span data-ttu-id="1e9d3-860">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="1e9d3-860">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="1e9d3-861">Skapar en ny Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-861">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="1e9d3-862">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="1e9d3-862">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="1e9d3-863">Hämtar information om en Event Grid-domän eller hämtar en lista med alla Event Grid-domäner i den aktuella Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-863">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="1e9d3-864">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="1e9d3-864">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="1e9d3-865">Tar bort en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-865">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="1e9d3-866">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="1e9d3-866">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="1e9d3-867">Återskapar nyckeln för delad åtkomst för en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-867">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="1e9d3-868">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="1e9d3-868">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="1e9d3-869">Hämtar de nycklar för delad åtkomst som används för att publicera händelser till en Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-869">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="1e9d3-870">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="1e9d3-870">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="1e9d3-871">Skapar ett nytt Azure Event Grid-domänämne.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-871">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="1e9d3-872">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="1e9d3-872">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="1e9d3-873">Hämtar information om ett Event Grid-domänämne eller hämtar en lista med alla Event Grid-domänämnen under en specifik Event Grid-domän i nuvarande Azure</span><span class="sxs-lookup"><span data-stu-id="1e9d3-873">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="1e9d3-874">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="1e9d3-874">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="1e9d3-875">Tar bort ett befintligt Azure Event Grid-domänämne.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-875">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="1e9d3-876">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="1e9d3-876">Updated cmdlets:</span></span>
    - <span data-ttu-id="1e9d3-877">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="1e9d3-877">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="1e9d3-878">Lägg till nya obligatoriska parametrar för att stödja piping för den nya Event Grid-domänen och Event Grid-domänämnet för att göra det möjligt att skapa nya händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-878">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="1e9d3-879">Lägg till nya obligatoriska parametrar för att ange det nya Event Grid-domännamnet och/eller namnet på Event Grid-domänämnet för att göra det möjligt att skapa nya händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-879">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="1e9d3-880">Lägg till ny parameteruppsättningar för domäner och domänämnen för att göra det möjligt att återanvända befintliga parametrar (t.ex. EndPointType, SubjectBeginsWith osv).</span><span class="sxs-lookup"><span data-stu-id="1e9d3-880">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="1e9d3-881">Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="1e9d3-881">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="1e9d3-882">Förfallodatum för händelseprenumeration</span><span class="sxs-lookup"><span data-stu-id="1e9d3-882">Event subscription expiration date,</span></span>
            - <span data-ttu-id="1e9d3-883">Avancerade filterparametrar.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-883">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="1e9d3-884">Lägg till ny uppräkning för servicebusqueue som mål.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-884">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="1e9d3-885">Tillåt inte användning av ”Alla” i alternativet -IncludedEventType och ersätt det med</span><span class="sxs-lookup"><span data-stu-id="1e9d3-885">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="1e9d3-886">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="1e9d3-886">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="1e9d3-887">Lägg till ny valfria parametrar (Top, ODataQuery och NextLink) för att stödja sidnumrering och filtrering av resultat.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-887">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="1e9d3-888">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="1e9d3-888">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="1e9d3-889">Lägg till nya obligatoriska parametrar för att stödja piping för en Event Grid-domän och Event Grid-domänämnen för att göra det möjligt att ta bort befintliga händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-889">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="1e9d3-890">Lägg till nya obligatoriska parametrar för att ange Event Grid-domännamnet och/eller namnet på Event Grid-domänämnet för att göra det möjligt att ta bort befintliga händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-890">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="1e9d3-891">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="1e9d3-891">Az.FrontDoor</span></span>
* <span data-ttu-id="1e9d3-892">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="1e9d3-892">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="1e9d3-893">Lägg till stöd för transformeringar och nytt värde för automatisk komplettering för operatorer (RegEx)</span><span class="sxs-lookup"><span data-stu-id="1e9d3-893">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="1e9d3-894">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="1e9d3-894">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="1e9d3-895">Lägg till nya värden för automatisk komplettering</span><span class="sxs-lookup"><span data-stu-id="1e9d3-895">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1e9d3-896">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1e9d3-896">Az.Network</span></span>
* <span data-ttu-id="1e9d3-897">Lägg till stöd för resurs för virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="1e9d3-897">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="1e9d3-898">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="1e9d3-898">New cmdlets</span></span>
        - <span data-ttu-id="1e9d3-899">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="1e9d3-899">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="1e9d3-900">Lägg till AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="1e9d3-900">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="1e9d3-901">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="1e9d3-901">New cmdlets</span></span> 
        - <span data-ttu-id="1e9d3-902">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="1e9d3-902">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="1e9d3-903">Lägg till PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="1e9d3-903">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="1e9d3-904">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="1e9d3-904">New cmdlets</span></span> 
        - <span data-ttu-id="1e9d3-905">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="1e9d3-905">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="1e9d3-906">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="1e9d3-906">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="1e9d3-907">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="1e9d3-907">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="1e9d3-908">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="1e9d3-908">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="1e9d3-909">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="1e9d3-909">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="1e9d3-910">Lägg till PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="1e9d3-910">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="1e9d3-911">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="1e9d3-911">New cmdlets</span></span>
        - <span data-ttu-id="1e9d3-912">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="1e9d3-912">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="1e9d3-913">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="1e9d3-913">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="1e9d3-914">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="1e9d3-914">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="1e9d3-915">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="1e9d3-915">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="1e9d3-916">Nedanstående kommandon för funktionen har uppdaterats: Flaggan UseLocalAzureIpAddress på VpnConnection</span><span class="sxs-lookup"><span data-stu-id="1e9d3-916">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="1e9d3-917">New-AzVpnConnection har uppdaterats: Den valfria parametern -UseLocalAzureIpAddress har lagts till för att visa att en lokal IP-adress i Azure ska användas som källadress när anslutningen initieras.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-917">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="1e9d3-918">Set-AzVpnConnection har uppdaterats: Den valfria parametern -UseLocalAzureIpAddress har lagts till för att visa att en lokal IP-adress i Azure ska användas som källadress när anslutningen initieras.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-918">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="1e9d3-919">Det skrivskyddade fältet PeeredConnections har lagts till i ExpressRoute-peering.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-919">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="1e9d3-920">Det skrivskyddade fältet GlobalReachEnabled har lagts till i ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-920">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="1e9d3-921">Ett attribut för icke-bakåtkompatibla ändringar har lagts till för att lyfta fram utfasning av fältet AllowGlobalReach i modellen ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1e9d3-921">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="1e9d3-922">Problem 8756 har åtgärdats: Fel vid användning av TargetListenerID med AzApplicationGatewayRedirectConfiguration-cmdletar</span><span class="sxs-lookup"><span data-stu-id="1e9d3-922">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="1e9d3-923">En bugg i New-AzApplicationGatewayPathRuleConfig som gjorde att regeluppsättningen för att återskapa inte kunde anges har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-923">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="1e9d3-924">Visningen av VirtualNetworkTaps i NetworkInterfaceIpConfiguration har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="1e9d3-924">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="1e9d3-925">Cortex Get-cmdletar för att visa en lista med alla delar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="1e9d3-925">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="1e9d3-926">Funktionen för att skapa VirtualHub-referenser för ExpressRouteGateways och VpnGateway har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="1e9d3-926">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="1e9d3-927">Stöd för tillgänglighetszoner i AzureFirewall och NatGateway har lagts till</span><span class="sxs-lookup"><span data-stu-id="1e9d3-927">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="1e9d3-928">Cmdleten Get-AzNetworkServiceTag har lagts till</span><span class="sxs-lookup"><span data-stu-id="1e9d3-928">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="1e9d3-929">Lägg till stöd för flera offentliga IP-adresser för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="1e9d3-929">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="1e9d3-930">Cmdleten New-AzFirewall har uppdaterats:</span><span class="sxs-lookup"><span data-stu-id="1e9d3-930">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="1e9d3-931">Parametern -PublicIpAddress som accepterar ett eller flera offentliga IP-adressobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="1e9d3-931">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="1e9d3-932">Parametern -VirtualNetwork som accepterar ett virtuellt nätverksobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="1e9d3-932">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="1e9d3-933">Metoderna AddPublicIpAddress och RemovePublicIpAddress har lagts till på brandväggsobjekt – dessa accepterar ett offentligt IP-adressobjekt som indata</span><span class="sxs-lookup"><span data-stu-id="1e9d3-933">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="1e9d3-934">Inaktuella parametrar -PublicIpName och -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="1e9d3-934">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="1e9d3-935">Nedanstående kommandon för funktionen har uppdaterats: Ange autentiseringsalternativ för VpnClient AAD till resurser för virtuella nätverksgatewayer.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-935">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="1e9d3-936">New-AzVirtualNetworkGateway har uppdaterats: De valfria parametrarna AadTenantUri, AadAudienceId och AadIssuerUri för att ange VpnClient AAD-autentiseringsalternativ på en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-936">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="1e9d3-937">Set-AzVirtualNetworkGateway har uppdaterats: De valfria parametrarna AadTenantUri, AadAudienceId och AadIssuerUri för att ange VpnClient AAD-autentiseringsalternativ på en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-937">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="1e9d3-938">Set-AzVirtualNetworkGateway har uppdaterats: Den valfria växelparametern RemoveAadAuthentication som tar bort VpnClient AAD-autentiseringsalternativ från en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-938">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="1e9d3-939">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="1e9d3-939">Az.OperationalInsights</span></span>
* <span data-ttu-id="1e9d3-940">Aktivera prisnivån **pergb2018** i kommandot ”New-AzureRmOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="1e9d3-940">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="1e9d3-941">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1e9d3-941">Az.Resources</span></span>
* <span data-ttu-id="1e9d3-942">Stöd för ytterligare alternativ för att exportera en mall</span><span class="sxs-lookup"><span data-stu-id="1e9d3-942">Support for additional Template Export options</span></span>
    - <span data-ttu-id="1e9d3-943">Lägg till parametern ”-SkipResourceNameParameterization” till Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1e9d3-943">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="1e9d3-944">Lägg till parametern ”-SkipAllParameterization” till Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1e9d3-944">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="1e9d3-945">Lägg till parametern ”-Resource” till Export-AzResourceGroup för exporterad resursfiltrering</span><span class="sxs-lookup"><span data-stu-id="1e9d3-945">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="1e9d3-946">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1e9d3-946">Az.ServiceFabric</span></span>
* <span data-ttu-id="1e9d3-947">Åtgärda att fel tumavtryck används vid tilläggning av certifikat i ByExistingKeyVault i vissa fall</span><span class="sxs-lookup"><span data-stu-id="1e9d3-947">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="1e9d3-948">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1e9d3-948">Az.Sql</span></span>
* <span data-ttu-id="1e9d3-949">Åtgärda suffix för lagringsslutpunkt i Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="1e9d3-949">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="1e9d3-950">Åtgärda att aktivering av Advanced Data Security åsidosätter Advanced Threat Protection-princip</span><span class="sxs-lookup"><span data-stu-id="1e9d3-950">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="1e9d3-951">Nya cmdletar för Management.Sql som gör att kunderna kan lägga till nycklar för transparent datakryptering (TDE) och ange TDE-skydd för hanterade instanser</span><span class="sxs-lookup"><span data-stu-id="1e9d3-951">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="1e9d3-952">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1e9d3-952">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="1e9d3-953">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1e9d3-953">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="1e9d3-954">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1e9d3-954">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="1e9d3-955">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="1e9d3-955">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="1e9d3-956">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="1e9d3-956">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1e9d3-957">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1e9d3-957">Az.Storage</span></span>
* <span data-ttu-id="1e9d3-958">Stöd för typerna FileStorage och SkuName Premium_ZRS när lagringskonton skapas</span><span class="sxs-lookup"><span data-stu-id="1e9d3-958">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="1e9d3-959">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1e9d3-959">New-AzStorageAccount</span></span>
* <span data-ttu-id="1e9d3-960">Beskrivningen av cmdleten för bloboföränderlighet har förtydligats</span><span class="sxs-lookup"><span data-stu-id="1e9d3-960">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="1e9d3-961">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="1e9d3-961">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1e9d3-962">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1e9d3-962">Az.Websites</span></span>
* <span data-ttu-id="1e9d3-963">Optimerar Get-AzWebAppCertificate för att filtrera efter resursgrupp på servern i stället för klienten</span><span class="sxs-lookup"><span data-stu-id="1e9d3-963">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="1e9d3-964">Lägger till växlingsparametern -UseDisasterRecovery till Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="1e9d3-964">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="1e9d3-965">2.2.0 – juni 2019</span><span class="sxs-lookup"><span data-stu-id="1e9d3-965">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="1e9d3-966">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="1e9d3-966">Az.Cdn</span></span>
* <span data-ttu-id="1e9d3-967">Uppdaterade cmdletar för att ge stöd för rulesEngine-funktion baserat på API-version 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-967">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1e9d3-968">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1e9d3-968">Az.Compute</span></span>
* <span data-ttu-id="1e9d3-969">Lade till parameter `NoWait` som startar åtgärden och returnerar omedelbart, innan åtgärden har slutförts.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-969">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="1e9d3-970">Uppdaterade cmdletar:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="1e9d3-970">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="1e9d3-971">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="1e9d3-971">Az.EventHub</span></span>
* <span data-ttu-id="1e9d3-972">Korrigering för #9231 – Get-AzEventHubNamespace returnerar inga taggar</span><span class="sxs-lookup"><span data-stu-id="1e9d3-972">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="1e9d3-973">Korrigering för #9230 – Get-AzEventHubNamespace returnerar ResourceGroup istället för ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e9d3-973">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1e9d3-974">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1e9d3-974">Az.Network</span></span>
* <span data-ttu-id="1e9d3-975">Uppdatera ResourceId och InputObject för NAT-gateway</span><span class="sxs-lookup"><span data-stu-id="1e9d3-975">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="1e9d3-976">Lägg till alias för ResourceId och InputObject</span><span class="sxs-lookup"><span data-stu-id="1e9d3-976">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="1e9d3-977">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="1e9d3-977">Az.PolicyInsights</span></span>
* <span data-ttu-id="1e9d3-978">Åtgärda Null-referensproblem i Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="1e9d3-978">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1e9d3-979">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1e9d3-979">Az.RecoveryServices</span></span>
* <span data-ttu-id="1e9d3-980">Minsta kvarhållning för IaaSVM-policy i dagar ändrat till 7 från 1</span><span class="sxs-lookup"><span data-stu-id="1e9d3-980">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="1e9d3-981">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="1e9d3-981">Az.ServiceBus</span></span>
* <span data-ttu-id="1e9d3-982">Korrigering för ärende #9182 – Get-AzServiceBusNamespace returnerar ResourceGroup istället för ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e9d3-982">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="1e9d3-983">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1e9d3-983">Az.ServiceFabric</span></span>
* <span data-ttu-id="1e9d3-984">Åtgärda stavfel i felmeddelandet för Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="1e9d3-984">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="1e9d3-985">Åtgärda saknat tecken i Service Fabric-kommandorader</span><span class="sxs-lookup"><span data-stu-id="1e9d3-985">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="1e9d3-986">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1e9d3-986">Az.Sql</span></span>
* <span data-ttu-id="1e9d3-987">Lägg till parametern DnsZonePartner för New-AzureSqlInstance-cmdlet för att ge stöd för AutoDr för hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-987">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="1e9d3-988">Avvecklar cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="1e9d3-988">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="1e9d3-989">Döp om cmdletar för hotidentifiering till Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="1e9d3-989">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="1e9d3-990">Parametrarna New-AzSqlInstance -StorageSizeInGB och -LicenseType är nu valfria.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-990">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1e9d3-991">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1e9d3-991">Az.Websites</span></span>
* <span data-ttu-id="1e9d3-992">åtgärdar problemet där användningen av Set-AzWebApp och Set-AzWebAppSlot med -WebApp-egenskap tog bort taggarna</span><span class="sxs-lookup"><span data-stu-id="1e9d3-992">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="1e9d3-993">2.1.0 – maj 2019</span><span class="sxs-lookup"><span data-stu-id="1e9d3-993">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="1e9d3-994">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="1e9d3-994">Az.ApiManagement</span></span>
* <span data-ttu-id="1e9d3-995">Skapade nya cmdletar för att hantera diagnostik för global- och API-omfång</span><span class="sxs-lookup"><span data-stu-id="1e9d3-995">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="1e9d3-996">**Get-AzApiManagementDiagnostic** – Skaffa diagnostik konfigurerad för global- eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="1e9d3-996">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="1e9d3-997">**New-AzApiManagementDiagnostic** – Skapa ny diagnostik för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="1e9d3-997">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="1e9d3-998">**New-AzApiManagementHttpMessageDiagnostic** – Skapa diagnostikinställning om vilka rubriker som ska loggas och storleken på brödtextbyte</span><span class="sxs-lookup"><span data-stu-id="1e9d3-998">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="1e9d3-999">**New-AzApiManagementPipelineDiagnosticSetting** – Skapa diagnostikinställningar för inkommande/utgående HTTP-meddelanden till gatewayen.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-999">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="1e9d3-1000">**New-AzApiManagementSamplingSetting** – Skapa samplinginställningar för begäranden/svar för en diagnostik</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1000">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="1e9d3-1001">**Remove-AzApiManagementDiagnostic** – Ta bort en diagnostikenhet för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1001">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="1e9d3-1002">**Set-AzApiManagementDiagnostic** – Uppdatera en diagnostikenhet för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1002">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="1e9d3-1003">Skapade nya cmdletar för hantering av cacheminne i ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1003">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="1e9d3-1004">**Get-AzApiManagementCache** – Hämta information om cacheminnet som anges av identifierare eller alla cacheminnen</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1004">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="1e9d3-1005">**New-AzApiManagementCache** – Skapa ett nytt default-cacheminne eller cacheminne i en viss Azure-region</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1005">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="1e9d3-1006">**Remove-AzApiManagementCache** – Ta bort ett cacheminne</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1006">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="1e9d3-1007">**Remove-AzApiManagementCache** – Ta bort ett cacheminne</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1007">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="1e9d3-1008">Skapade nya cmdletar för hantering av API-schema</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1008">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="1e9d3-1009">**New-AzApiManagementSchema** – Skapa ett nytt schema för ett API</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1009">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="1e9d3-1010">**Get-AzApiManagementSchema** – Hämta de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1010">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="1e9d3-1011">**Remove-AzApiManagementSchema** – Ta bort de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1011">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="1e9d3-1012">**Set-AzApiManagementSchema** – Uppdatera de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1012">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="1e9d3-1013">Skapa ny cmdlet för att generera en användartoken.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1013">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="1e9d3-1014">**New-AzApiManagementUserToken** – Skapa en ny användartoken som enligt standardinställning är giltig i 8 timmar. Token för GIT-användaren kan skapas med den här cmdleten./</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1014">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="1e9d3-1015">Skapade en ny cmdlet för att hämta nätverksstatus</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1015">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="1e9d3-1016">**Get-AzApiManagementNetworkStatus** – Hämta nätverksstatusanslutningen för resurserna som API Management-tjänsten är beroende av.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1016">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="1e9d3-1017">Det här är användbart när du distribuerar ApiManagement-tjänsten i ett virtuellt nätverk och validerar om något beroende är brutet.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1017">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="1e9d3-1018">Uppdaterade cmdlet **New-AzApiManagement** för att hantera ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1018">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="1e9d3-1019">Lade till stöd för den nya SKU:n Consumption</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1019">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="1e9d3-1020">Aktiverade stöd för att slå på flaggan EnableClientCertificate för SKU:n Consumption</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1020">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="1e9d3-1021">Den nya cmdleten **New-AzApiManagementSslSetting** gör det möjligt att ställa in TLS/SSL-inställningen på ”Backend” och ”Frontend” (serverdel och klientdel).</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1021">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="1e9d3-1022">Det här kan också användas till att konfigurera chiffer som 3DES och ServerProtocols som Http2 för Frontend för en ApiManagement-tjänst.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1022">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="1e9d3-1023">Stöd har lagts till för att konfigurera värdnamnet DeveloperPortal på ApiManagement-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1023">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="1e9d3-1024">Uppdaterade cmdletar **Get-AzApiManagementSsoToken** för att ta PsApiManagement-objekt som indata</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1024">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="1e9d3-1025">Uppdaterad cmdleten för att visa infogade felmeddelanden</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1025">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="1e9d3-1026">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Felkod: Felmeddelande av typen ValidationError: Ett eller flera fält innehåller felaktiga värden: Felinformation:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1026">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="1e9d3-1027">Uppdaterade cmdlet **Export-AzApiManagementApi** för att exportera API:er i OpenApi 3.0-format</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1027">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="1e9d3-1028">Uppdaterade cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1028">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="1e9d3-1029">Importera API från dokumentspecifikationen OpenApi 3.0</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1029">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="1e9d3-1030">Om du vill åsidosätta egenskapen PsApiManagementSchema specificerad i ett dokument (Swagger, Wadl, Wsdl, OpenApi).</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1030">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="1e9d3-1031">Åsidosätta egenskapen ServiceUrl som specificeras i ett dokument.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1031">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="1e9d3-1032">Uppdaterade cmdlet **Get-AzApiManagementPolicy** för att returnera policy i undantaget format av typen icke-XML med rawxml</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1032">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="1e9d3-1033">Uppdaterade cmdlet **Set-AzApiManagementPolicy** för att godkänna policy i undantaget format av typen icke-XML med rawxml och XML undantaget med xml</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1033">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="1e9d3-1034">Uppdaterad cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1034">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="1e9d3-1035">Konfigurera API med OpenId auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1035">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="1e9d3-1036">Skapa ett API i ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1036">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="1e9d3-1037">Klona ett API med SourceApiId och SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1037">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="1e9d3-1038">Möjlighet att konfigurera SubscriptionRequired i API-omfattningen.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1038">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="1e9d3-1039">Uppdaterad cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1039">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="1e9d3-1040">Konfigurera API med OpenId auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1040">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="1e9d3-1041">Uppdatera ett API till ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1041">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="1e9d3-1042">Möjlighet att konfigurera SubscriptionRequired i API-omfattningen.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1042">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="1e9d3-1043">Uppdaterad cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1043">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="1e9d3-1044">Klona en befintlig version med hjälp av SourceApiRevision (kopiera taggar, produkter, åtgärder och principer).</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1044">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="1e9d3-1045">Den nya revisionen antar ApiId från den överordnade instansen.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1045">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="1e9d3-1046">Tillhandahålla ApiRevisionDescription</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1046">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="1e9d3-1047">Åsidosätta ServiceUrl vid kloning av ett API.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1047">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="1e9d3-1048">Uppdaterad cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1048">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="1e9d3-1049">Konfigurera AAD eller AADB2C med en Authority</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1049">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="1e9d3-1050">Konfigurera SignupPolicy, SigninPolicy, ProfileEditingPolicy och PasswordResetPolicy</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1050">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="1e9d3-1051">Uppdaterad cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1051">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="1e9d3-1052">Kompensera för ny SubscriptonModel med Scope och UserId</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1052">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="1e9d3-1053">Kompensera för gammal prenumerationsmodell med ProductId och UserId</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1053">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="1e9d3-1054">Lägg till funktion för att aktivera AllowTracing på prenumerationsnivå.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1054">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="1e9d3-1055">Uppdaterad cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1055">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="1e9d3-1056">Kompensera för ny SubscriptonModel med Scope och UserId</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1056">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="1e9d3-1057">Kompensera för gammal prenumerationsmodell med ProductId och UserId</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1057">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="1e9d3-1058">Lägg till funktion för att aktivera AllowTracing på prenumerationsnivå.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1058">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="1e9d3-1059">Uppdaterade följande cmdletar för att acceptera ResourceId som indata</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1059">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="1e9d3-1060">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1060">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="1e9d3-1061">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1061">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="1e9d3-1062">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1062">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="1e9d3-1063">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1063">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="1e9d3-1064">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1064">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="1e9d3-1065">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1065">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="1e9d3-1066">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1066">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="1e9d3-1067">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1067">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="1e9d3-1068">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1068">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="1e9d3-1069">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1069">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="1e9d3-1070">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1070">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="1e9d3-1071">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1071">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="1e9d3-1072">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1072">Az.Automation</span></span>
* <span data-ttu-id="1e9d3-1073">Uppdaterade Get-AzAutomationJobOutputRecord för att hantera postvärden av typen JSON och Text.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1073">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="1e9d3-1074">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1074">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="1e9d3-1075">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1075">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="1e9d3-1076">Ändrade beteende för Start-AzAutomationDscCompilationJob till att bara starta jobbet istället för att vänta på slutförandet.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1076">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="1e9d3-1077">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1077">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="1e9d3-1078">Korrigering för Get-AzAutomationDscNode när using -Name returnerar alla noder.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1078">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="1e9d3-1079">Nu returnerar den endast den matchande noden.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1079">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1e9d3-1080">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1080">Az.Compute</span></span>
* <span data-ttu-id="1e9d3-1081">Lägg till parametrarna ProtectFromScaleIn och ProtectFromScaleSetAction i cmdleten Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1081">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="1e9d3-1082">Nu är standardinställningen att vimpelparametern New-AzVM använder en tillgänglig plats om USA, östra inte stöds</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1082">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="1e9d3-1083">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1083">Az.DataLakeStore</span></span>
* <span data-ttu-id="1e9d3-1084">Uppdatera ADLS-sdk för att använda httpclient, integrera dataplanstestning med Azure-ramverk</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1084">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="1e9d3-1085">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1085">Az.Monitor</span></span>
* <span data-ttu-id="1e9d3-1086">Korrigera felaktiga parameternamn i hjälpexempel</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1086">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1e9d3-1087">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1087">Az.Network</span></span>
* <span data-ttu-id="1e9d3-1088">Lägg till flaggan DisableBgpRoutePropagation i utdata för effektiv routningstabell</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1088">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="1e9d3-1089">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1089">Updated cmdlet:</span></span>
        - <span data-ttu-id="1e9d3-1090">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1090">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="1e9d3-1091">Åtgärda dubbelstreck i dokumentationen New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1091">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="1e9d3-1092">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1092">Az.Resources</span></span>
* <span data-ttu-id="1e9d3-1093">Lägg till ny cmdlet Get-AzureRmDenyAssignment för att hämta tilldelningsnekanden</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1093">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="1e9d3-1094">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1094">Az.Sql</span></span>
* <span data-ttu-id="1e9d3-1095">Döp om Advanced Threat Protection-cmdletar för Advanced Data Security och aktivera Vulnerability Assessment som standard</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1095">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="1e9d3-1096">2.0.0 – maj 2019</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1096">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1e9d3-1097">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1097">Az.Accounts</span></span>
* <span data-ttu-id="1e9d3-1098">Uppdatera autentiseringsbiblioteket för att åtgärda ADFS-problem med autentisering av användarnamn/lösenord</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1098">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="1e9d3-1099">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1099">Az.CognitiveServices</span></span>
* <span data-ttu-id="1e9d3-1100">Visa endast Bing-ansvarsfriskrivning för Bing-sökningstjänster.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1100">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="1e9d3-1101">Förbättra felmeddelande när det inte går att skapa konton.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1101">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1e9d3-1102">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1102">Az.Compute</span></span>
* <span data-ttu-id="1e9d3-1103">Funktion för närhetsplaceringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1103">Proximity placement group feature.</span></span>
    - <span data-ttu-id="1e9d3-1104">Följande nya cmdletar har lagts till:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1104">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="1e9d3-1105">Den nya parametern ProximityPlacementGroupId har lagts till i följande cmdletar:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1105">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="1e9d3-1106">Parametern StorageAccountType har lagts till i New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1106">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="1e9d3-1107">TargetRegion för New-AzGalleryImageVersion kan innehålla StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1107">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="1e9d3-1108">Växlingsparametern SkipShutdown har lagts till i Stop-AzVM och Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1108">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="1e9d3-1109">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1109">Breaking changes</span></span>
    - <span data-ttu-id="1e9d3-1110">Set-AzVMBootDiagnostics har ändrats till Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1110">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="1e9d3-1111">Export-AzLogAnalyticThrottledRequests har ändrats till Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1111">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="1e9d3-1112">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1112">Az.DeploymentManager</span></span>
* <span data-ttu-id="1e9d3-1113">De första allmänt tillgängliga versionerna av cmdletar för Distributionshanteraren i Azure</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1113">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="1e9d3-1114">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1114">Az.Dns</span></span>
* <span data-ttu-id="1e9d3-1115">Automatisk delegering av DNS för NameServer</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1115">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="1e9d3-1116">Det överordnade zonnamnet kan användas som ytterligare valfri parameter i cmdleten för att skapa DNS-zoner.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1116">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="1e9d3-1117">Lägger till NS-poster för en nyligen skapad underordnad zon i den överordnade zonen.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1117">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="1e9d3-1118">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1118">Az.FrontDoor</span></span>
* <span data-ttu-id="1e9d3-1119">De första allmänt tillgängliga versionerna av cmdletar för Azure FrontDoor</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1119">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="1e9d3-1120">Byt namn på WAF-cmdletar så att de omfattar ”Waf”</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1120">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="1e9d3-1121">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1121">Az.HDInsight</span></span>
* <span data-ttu-id="1e9d3-1122">Två cmdletar har tagits bort:</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1122">Removed two cmdlets:</span></span>
    - <span data-ttu-id="1e9d3-1123">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1123">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="1e9d3-1124">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1124">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="1e9d3-1125">En ny cmdlet har lagts till, Set-AzHDInsightGatewayCredential, som ersätter Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1125">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="1e9d3-1126">Uppdatera cmdleten Get-AzHDInsightJobOutput för att skilja mellan läsarrollen och HDInsight-operatörsrollen:</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1126">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="1e9d3-1127">Användare med läsarrollen måste uttryckligen ange parametern ”DefaultStorageAccountKey”, annars uppstår fel.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1127">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="1e9d3-1128">Användare med HDInsight-operatörsrollen påverkas inte.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1128">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="1e9d3-1129">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1129">Az.Monitor</span></span>
* <span data-ttu-id="1e9d3-1130">Nya cmdletar för SQR API (schemalagd frågeregel)</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1130">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="1e9d3-1131">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1131">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="1e9d3-1132">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1132">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="1e9d3-1133">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1133">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="1e9d3-1134">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1134">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="1e9d3-1135">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1135">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="1e9d3-1136">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1136">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="1e9d3-1137">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1137">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="1e9d3-1138">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1138">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="1e9d3-1139">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1139">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="1e9d3-1140">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1140">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="1e9d3-1141">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1141">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="1e9d3-1142">[Mer](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information om SQR API</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1142">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="1e9d3-1143">Az.Monitor.md har uppdaterats för att omfatta cmdletar för måttbaserade aviseringsregler i GenV2 (inte klassiska)</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1143">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1e9d3-1144">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1144">Az.Network</span></span>
* <span data-ttu-id="1e9d3-1145">Lägg till stöd för NAT Gateway-resurs</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1145">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="1e9d3-1146">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1146">New cmdlets</span></span>
        - <span data-ttu-id="1e9d3-1147">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1147">New-AzNatGateway</span></span>
        - <span data-ttu-id="1e9d3-1148">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1148">Get-AzNatGateway</span></span>
        - <span data-ttu-id="1e9d3-1149">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1149">Set-AzNatGateway</span></span>
        - <span data-ttu-id="1e9d3-1150">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1150">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="1e9d3-1151">Uppdaterade cmdletar</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1151">Updated cmdlets</span></span>
        - <span data-ttu-id="1e9d3-1152">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1152">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="1e9d3-1153">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1153">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="1e9d3-1154">Nedanstående kommandon för funktionen har uppdaterats: Ange/ta bort anpassade vägar på Brooklyn Gateway.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1154">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="1e9d3-1155">New-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ställa in adressprefix som anpassade vägar för att ange gateway.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1155">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="1e9d3-1156">Set-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ange adressprefix som anpassade vägar för att ange gateway.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1156">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="1e9d3-1157">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1157">Az.PolicyInsights</span></span>
* <span data-ttu-id="1e9d3-1158">Stöd för att fråga efter information om principutvärdering.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1158">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="1e9d3-1159">Lägg till parametern ”-Expand” för Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1159">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="1e9d3-1160">Stöd för -Expand PolicyEvaluationDetails.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1160">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1e9d3-1161">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1161">Az.RecoveryServices</span></span>
* <span data-ttu-id="1e9d3-1162">Stöd för att dela prenumeration mellan Azure och Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1162">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="1e9d3-1163">Markering av kommande icke-bakåtkompatibla ändringar för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1163">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="1e9d3-1164">Korrigering för återställningsplan och åtgärdsplan i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1164">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="1e9d3-1165">Korrigering för mappning av uppdateringsnätverk i Azure Site Recovery för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1165">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="1e9d3-1166">Korrigering för instruktioner för uppdateringsskydd i Azure Site Recovery för Azure till Azure för hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1166">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="1e9d3-1167">Andra mindre korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1167">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="1e9d3-1168">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1168">Az.Relay</span></span>
* <span data-ttu-id="1e9d3-1169">Korrigera stavfel i kundriktade meddelanden</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1169">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="1e9d3-1170">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1170">Az.ServiceBus</span></span>
* <span data-ttu-id="1e9d3-1171">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1171">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1e9d3-1172">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1172">Az.Storage</span></span>
* <span data-ttu-id="1e9d3-1173">Uppgradera till lagringsklientbiblioteket 10.0.1 (namnområdet för alla objekt från detta SDK ändras från ”Microsoft.WindowsAzure.Storage. *till ”Microsoft.Azure.Storage.* ”)</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1173">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="1e9d3-1174">Uppgradera till Microsoft.Azure.Management.Storage 11.0.0 för att stödja den nya API-versionen 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1174">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="1e9d3-1175">Standardlagringskontot i Skapa lagringskonto ändras från ”Storage” till ”StorageV2”</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1175">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="1e9d3-1176">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1176">New-AzStorageAccount</span></span>
* <span data-ttu-id="1e9d3-1177">Ändra lagringskontots cmdlet-utdata Sku.Name för att passa med indata-SkuName genom att lägga till ”-”. Till exempel ändras ”StandardLRS” till ”Standard_LRS”</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1177">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="1e9d3-1178">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1178">New-AzStorageAccount</span></span>
    - <span data-ttu-id="1e9d3-1179">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1179">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="1e9d3-1180">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1180">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1e9d3-1181">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1181">Az.Websites</span></span>
* <span data-ttu-id="1e9d3-1182">Egenskapen ”typ” konfigureras nu för PSSite-objekt som returneras av Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1182">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="1e9d3-1183">Get-AzWebApp\*Metrics och Get-AzAppServicePlanMetrics markeras som inaktuella</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1183">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="1e9d3-1184">1.8.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1184">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="1e9d3-1185">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1185">Highlights since the last major release</span></span>
* <span data-ttu-id="1e9d3-1186">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1186">General availability of `Az` module</span></span>
* <span data-ttu-id="1e9d3-1187">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1187">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="1e9d3-1188">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1188">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="1e9d3-1189">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1189">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="1e9d3-1190">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1190">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="1e9d3-1191">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1191">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="1e9d3-1192">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1192">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="1e9d3-1193">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1193">Az.Accounts</span></span>
* <span data-ttu-id="1e9d3-1194">Uppdatera Uninstall-AzureRm för att ta bort moduler i Mac på ett korrekt sätt</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1194">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="1e9d3-1195">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1195">Az.Batch</span></span>
* <span data-ttu-id="1e9d3-1196">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1196">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="1e9d3-1197">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1197">Az.Cdn</span></span>
* <span data-ttu-id="1e9d3-1198">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1198">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="1e9d3-1199">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1199">Az.CognitiveServices</span></span>
* <span data-ttu-id="1e9d3-1200">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1200">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1e9d3-1201">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1201">Az.Compute</span></span>
* <span data-ttu-id="1e9d3-1202">Åtgärda problem med AEM-installationen om resurs-ID:n för diskar innehåller resourcegroups i gemener i resurs-ID:n</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1202">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="1e9d3-1203">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1203">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="1e9d3-1204">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1204">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1e9d3-1205">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1205">Az.DataFactory</span></span>
* <span data-ttu-id="1e9d3-1206">Lägg till SsisProperties om NodeCount inte är null för hanterad integreringskörning.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1206">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="1e9d3-1207">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1207">Az.DataLakeStore</span></span>
* <span data-ttu-id="1e9d3-1208">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1208">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="1e9d3-1209">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1209">Az.EventGrid</span></span>
* <span data-ttu-id="1e9d3-1210">Hjälptexten för slutpunkten har uppdaterats för att visa att resurser ska skapas innan cmdletarna för att skapa/uppdatera händelseprenumerationer används.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1210">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="1e9d3-1211">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1211">Az.EventHub</span></span>
* <span data-ttu-id="1e9d3-1212">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1212">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="1e9d3-1213">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1213">Az.HDInsight</span></span>
* <span data-ttu-id="1e9d3-1214">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1214">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="1e9d3-1215">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1215">Az.IotHub</span></span>
* <span data-ttu-id="1e9d3-1216">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1216">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="1e9d3-1217">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1217">Az.KeyVault</span></span>
* <span data-ttu-id="1e9d3-1218">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1218">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="1e9d3-1219">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1219">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="1e9d3-1220">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1220">Az.MachineLearning</span></span>
* <span data-ttu-id="1e9d3-1221">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1221">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="1e9d3-1222">Az.Media</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1222">Az.Media</span></span>
* <span data-ttu-id="1e9d3-1223">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1223">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="1e9d3-1224">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1224">Az.Monitor</span></span>
  * <span data-ttu-id="1e9d3-1225">Nya cmdletar för måttbaserad aviseringsregel i GenV2 (inte klassisk)</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1225">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="1e9d3-1226">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1226">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="1e9d3-1227">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1227">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="1e9d3-1228">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1228">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="1e9d3-1229">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1229">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="1e9d3-1230">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1230">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="1e9d3-1231">Monitor SDK har uppdaterats till version 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1231">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1e9d3-1232">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1232">Az.Network</span></span>
* <span data-ttu-id="1e9d3-1233">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1233">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="1e9d3-1234">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1234">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="1e9d3-1235">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1235">Az.NotificationHubs</span></span>
* <span data-ttu-id="1e9d3-1236">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1236">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="1e9d3-1237">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1237">Az.OperationalInsights</span></span>
* <span data-ttu-id="1e9d3-1238">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1238">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="1e9d3-1239">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1239">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="1e9d3-1240">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1240">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1e9d3-1241">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1241">Az.RecoveryServices</span></span>
* <span data-ttu-id="1e9d3-1242">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1242">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="1e9d3-1243">Tabellformatet för SQL i virtuella Azure-datorer har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1243">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="1e9d3-1244">En alternativ metod för att hämta platser i AzureFileShare har lagts till</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1244">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="1e9d3-1245">ScheduleRunDays i SchedulePolicy-objekt har uppdaterats enligt tidszon</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1245">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="1e9d3-1246">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1246">Az.RedisCache</span></span>
* <span data-ttu-id="1e9d3-1247">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1247">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="1e9d3-1248">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1248">Az.Resources</span></span>
* <span data-ttu-id="1e9d3-1249">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1249">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="1e9d3-1250">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1250">Az.Sql</span></span>
* <span data-ttu-id="1e9d3-1251">Ersätt Monitor SDK-beroende med vanlig kod</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1251">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="1e9d3-1252">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1252">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="1e9d3-1253">Förbättrad process för klassificering av flera kolumner.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1253">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="1e9d3-1254">Inkludera SKU-egenskaper (SKU-namn, serie, kapacitet) i svaret från Get-AzSqlServerServiceObjective och formatera som tabell som standard.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1254">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="1e9d3-1255">Möjlighet att använda Get-AzSqlServerServiceObjective efter plats utan att behöva en redan befintlig server i regionen.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1255">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="1e9d3-1256">Stöd för tidszonsparametern när hanterade instanser skapas.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1256">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="1e9d3-1257">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1257">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1e9d3-1258">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1258">Az.Websites</span></span>
* <span data-ttu-id="1e9d3-1259">åtgärdar Set-AzWebApp och Set-AzWebAppSlot så att de inte tar bort taggar vid körning</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1259">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="1e9d3-1260">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1260">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="1e9d3-1261">SDK för WebSites har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1261">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="1e9d3-1262">Egenskapen AdminSiteName har tagits bort från PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1262">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="1e9d3-1263">1.7.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1263">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="1e9d3-1264">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1264">Highlights since the last major release</span></span>
* <span data-ttu-id="1e9d3-1265">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1265">General availability of `Az` module</span></span>
* <span data-ttu-id="1e9d3-1266">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1266">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="1e9d3-1267">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1267">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="1e9d3-1268">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1268">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="1e9d3-1269">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1269">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="1e9d3-1270">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1270">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="1e9d3-1271">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1271">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="1e9d3-1272">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1272">Az.Accounts</span></span>
* <span data-ttu-id="1e9d3-1273">Add-AzEnvironment och Set-AzEnvironment har uppdaterats för att godkänna parametern AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1273">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="1e9d3-1274">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1274">Az.AnalysisServices</span></span>
* <span data-ttu-id="1e9d3-1275">ServiceClient används i cmdletar för dataplan och den ursprungliga autentiseringslogiken har tagits bort</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1275">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="1e9d3-1276">Add-AzureASAccount används för omslutning av Connect-AzAccount för att undvika en icke-bakåtkompatibel ändring</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1276">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="1e9d3-1277">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1277">Az.Automation</span></span>
* <span data-ttu-id="1e9d3-1278">Buggen för cmdleten New-AzAutomationSoftwareUpdateConfiguration för inkluderingar har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1278">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="1e9d3-1279">Nu bör parametern IncludedKbNumber och IncludedPackageNameMask fungera.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1279">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="1e9d3-1280">Felkorrigering för dynamiska grupper i uppdateringshanteringen för azure automation</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1280">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1e9d3-1281">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1281">Az.Compute</span></span>
* <span data-ttu-id="1e9d3-1282">Lägg till parametern HyperVGeneration i New-AzDiskConfig och New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1282">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="1e9d3-1283">Tillåt att virtuella datorer skapas med galleribilder från andra klientorganisationer.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1283">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="1e9d3-1284">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1284">Az.ContainerInstance</span></span>
* <span data-ttu-id="1e9d3-1285">Ett problem har åtgärdats i parametern -Command för New-AzContainerGroup som lade till ett avslutande tomt argument</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1285">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1e9d3-1286">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1286">Az.DataFactory</span></span>
* <span data-ttu-id="1e9d3-1287">ADF .Net SDK-versionen har uppdaterats till 3.0.2</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1287">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="1e9d3-1288">Cmdleten Set-AzDataFactoryV2 har uppdaterats med extra parametrar för inställningar som rör RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1288">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="1e9d3-1289">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1289">Az.Resources</span></span>
* <span data-ttu-id="1e9d3-1290">Förbättra hanteringen av providrar för Get-AzResource när parametrarna -ResourceId eller -ResourceGroupName, -Name och -ResourceType tillhandahålls</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1290">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="1e9d3-1291">Förbättra felhanteringen för ”Test-AzDeployment” och ”Test-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1291">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="1e9d3-1292">Hantera fel utanför distributionsvalideringen och ta med dem i kommandoutdata istället</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1292">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="1e9d3-1293">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1293">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="1e9d3-1294">Lägg till växlingsparametern -IgnoreDynamicParameters till en uppsättning av cmdletar för distribution för att hoppa över fråga i skript och jobbscenarier</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1294">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="1e9d3-1295">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1295">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="1e9d3-1296">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1296">Az.Sql</span></span>
* <span data-ttu-id="1e9d3-1297">Stöd för dataklassificering av databaser.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1297">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1e9d3-1298">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1298">Az.Storage</span></span>
* <span data-ttu-id="1e9d3-1299">Rapportera detaljfel när lagringskontext skapas med parametern -UseConnectedAccount, men utan inloggning på Azure-kontot</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1299">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="1e9d3-1300">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1300">New-AzStorageContext</span></span>
* <span data-ttu-id="1e9d3-1301">Stöd för att hantera Blob Service-egenskaper för ett angivet lagringskonto med API:et för hanteringsplan</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1301">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="1e9d3-1302">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1302">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="1e9d3-1303">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1303">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="1e9d3-1304">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1304">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="1e9d3-1305">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1305">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="1e9d3-1306">Stöd för -AsJob-cmdletar för att ladda upp och ladda ned blobar och filer</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1306">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="1e9d3-1307">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1307">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="1e9d3-1308">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1308">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="1e9d3-1309">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1309">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="1e9d3-1310">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1310">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="1e9d3-1311">1.6.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1311">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="1e9d3-1312">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1312">Highlights since the last major release</span></span>
* <span data-ttu-id="1e9d3-1313">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1313">General availability of `Az` module</span></span>
* <span data-ttu-id="1e9d3-1314">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1314">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="1e9d3-1315">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1315">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="1e9d3-1316">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1316">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="1e9d3-1317">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1317">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="1e9d3-1318">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1318">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="1e9d3-1319">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1319">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="1e9d3-1320">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1320">Az.Automation</span></span>
* <span data-ttu-id="1e9d3-1321">Azure Automation – ändring av uppdateringshantering för stöd för de nya funktionerna:</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1321">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="1e9d3-1322">Dynamisk gruppering</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1322">Dynamic grouping</span></span>
    * <span data-ttu-id="1e9d3-1323">För-/efterskrift</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1323">Pre-Post script</span></span>
    * <span data-ttu-id="1e9d3-1324">Inställning för omstart</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1324">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1e9d3-1325">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1325">Az.Compute</span></span>
* <span data-ttu-id="1e9d3-1326">Åtgärda problem med sökvägsmatchning i Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1326">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="1e9d3-1327">Uppdatera Compute-klientbibliotek till 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1327">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="1e9d3-1328">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1328">Az.KeyVault</span></span>
* <span data-ttu-id="1e9d3-1329">Stöd för jokertecken för KeyVault-cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1329">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1e9d3-1330">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1330">Az.Network</span></span>
* <span data-ttu-id="1e9d3-1331">Lägg till stöd för Threat Intelligence för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1331">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="1e9d3-1332">Lägg till resurs för brandväggsprincip på översta nivå och anpassade regler för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1332">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1e9d3-1333">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1333">Az.RecoveryServices</span></span>
* <span data-ttu-id="1e9d3-1334">SnapshotRetentionInDays har lagts till i Azure-principen för virtuella datorer för stöd av Instant RP</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1334">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="1e9d3-1335">Pipe-stöd för avregistrering av container har lagts till</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1335">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="1e9d3-1336">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1336">Az.Resources</span></span>
* <span data-ttu-id="1e9d3-1337">Uppdatera stöd för jokertecken för Get-AzResource och Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1337">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="1e9d3-1338">Uppdatera autentiseringsuppgifter som används vid allmänna anrop till ARM</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1338">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="1e9d3-1339">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1339">Az.Sql</span></span>
* <span data-ttu-id="1e9d3-1340">Cmdlet-parametern (ExcludeDetectionType) för Hotidentifiering ändrades från DetectionType till sträng[] för att framtidssäkra den när nya DetectionTypes läggs till, och även för att stödja automatisk ifyllning.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1340">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1e9d3-1341">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1341">Az.Storage</span></span>
* <span data-ttu-id="1e9d3-1342">Stöd för att hämta/ange/ta bort hanteringsprincip på ett lagringskonto</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1342">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="1e9d3-1343">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1343">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="1e9d3-1344">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1344">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="1e9d3-1345">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1345">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="1e9d3-1346">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1346">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="1e9d3-1347">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1347">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="1e9d3-1348">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1348">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1e9d3-1349">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1349">Az.Websites</span></span>
* <span data-ttu-id="1e9d3-1350">Åtgärda fel med ARM-mall som avbryter kloning av alla platser med 'New-AzWebApp -IncludeSourceWebAppSlots'</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1350">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="1e9d3-1351">1.5.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1351">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1e9d3-1352">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1352">Az.Accounts</span></span>
* <span data-ttu-id="1e9d3-1353">Lägg till kommandot Register-AzModule för stöd för AutoRest-genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1353">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="1e9d3-1354">Uppdatera exempel för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1354">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="1e9d3-1355">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1355">Az.Automation</span></span>
* <span data-ttu-id="1e9d3-1356">Problem med att hämta vissa månadsscheman i flera Azure Automation-cmdletar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1356">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="1e9d3-1357">Åtgärda problem med att Get-AzAutomationDscNode bara returnerar de 20 översta noderna.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1357">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="1e9d3-1358">Nu returneras alla noder</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1358">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="1e9d3-1359">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1359">Az.Cdn</span></span>
* <span data-ttu-id="1e9d3-1360">Nya Powershell-cmdletar för att aktivera/inaktivera anpassade domän-HTTPS har lagts till och de gamla har gjorts inaktuella</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1360">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1e9d3-1361">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1361">Az.Compute</span></span>
* <span data-ttu-id="1e9d3-1362">Lägg till stöd för jokertecken för Get-cmdletar</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1362">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1e9d3-1363">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1363">Az.DataFactory</span></span>
* <span data-ttu-id="1e9d3-1364">ADF .Net SDK-versionen har uppdaterats till 3.0.1</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1364">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="1e9d3-1365">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1365">Az.LogicApp</span></span>
* <span data-ttu-id="1e9d3-1366">Åtgärda problemet med att ListWorkflows endast hämtar den första sidan med resultat</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1366">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1e9d3-1367">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1367">Az.Network</span></span>
* <span data-ttu-id="1e9d3-1368">Lägg till stöd för jokertecken för Network-cmdletar</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1368">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1e9d3-1369">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1369">Az.RecoveryServices</span></span>
* <span data-ttu-id="1e9d3-1370">Stöd har lagts till för SQL Server i virtuella Azure-datorer</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1370">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="1e9d3-1371">SDK-uppdatering</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1371">SDK Update</span></span>
* <span data-ttu-id="1e9d3-1372">Get-ProtectableItem-incheckning i VMappContainer har tagits bort</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1372">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="1e9d3-1373">Name och ServerName har lagts till som parametrar för Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1373">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="1e9d3-1374">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1374">Az.Resources</span></span>
* <span data-ttu-id="1e9d3-1375">Lägg till parametern `-TemplateObject` i cmdletar för distribution</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1375">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="1e9d3-1376">Mer information här: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1376">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="1e9d3-1377">Åtgärda problem med piping av resultatet i `Get-AzResource` till `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1377">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="1e9d3-1378">Mer information här: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1378">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="1e9d3-1379">Åtgärda problem med ändring av JSON-datatyp när `Set-AzResource` körs</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1379">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="1e9d3-1380">Mer information här: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1380">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="1e9d3-1381">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1381">Az.Sql</span></span>
* <span data-ttu-id="1e9d3-1382">AuditingEndpointsCommunicator uppdateras.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1382">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="1e9d3-1383">Åtgärdar beteendet hos ett gränsscenario när nya diagnostikinställningar skapas.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1383">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1e9d3-1384">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1384">Az.Storage</span></span>
* <span data-ttu-id="1e9d3-1385">Stöd för BlockBlobStorage när Storage-konto skapas      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1385">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="1e9d3-1386">1.4.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1386">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="1e9d3-1387">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1387">Az.AnalysisServices</span></span>
* <span data-ttu-id="1e9d3-1388">Inaktuell AddAzureASAccount-cmdlet</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1388">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="1e9d3-1389">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1389">Az.Automation</span></span>
* <span data-ttu-id="1e9d3-1390">Hjälpen för Import-AzAutomationDscNodeConfiguration har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1390">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="1e9d3-1391">Konfigurationsnamnsvalidering har lagts till i cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1391">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="1e9d3-1392">Förbättrad felhantering för cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1392">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="1e9d3-1393">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1393">Az.CognitiveServices</span></span>
* <span data-ttu-id="1e9d3-1394">CustomSubdomainName har lagts till som en ny valfri parameter för New-AzCognitiveServicesAccount, som används för att ange underdomän för resursen.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1394">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1e9d3-1395">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1395">Az.Compute</span></span>
* <span data-ttu-id="1e9d3-1396">Problemet med ID-parameteruppsättningar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1396">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="1e9d3-1397">Get-AzVMExtension har uppdaterats så att alla installerade tillägg visas om parametern Name inte har angetts</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1397">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="1e9d3-1398">Parametrarna Tag och ResourceId har lagts till i cmdleten Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1398">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="1e9d3-1399">Get-AzVmssVM utan instans-ID och med InstanceView kan visa virtuella VMSS-datorer med instansvyn.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1399">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="1e9d3-1400">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1400">Az.DataLakeStore</span></span>
* <span data-ttu-id="1e9d3-1401">Cmdletar har lagts till för uppräkning och återställning av borttagna objekt i ADL</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1401">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="1e9d3-1402">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1402">Az.EventHub</span></span>
* <span data-ttu-id="1e9d3-1403">Ny boolesk egenskap SkipEmptyArchives har lagts till i Skip Empty Archives i CaptureDescription-klassen i Eventhub</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1403">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="1e9d3-1404">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1404">Az.KeyVault</span></span>
* <span data-ttu-id="1e9d3-1405">Taggning i Set-AzKeyVaultSecret har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1405">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="1e9d3-1406">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1406">Az.LogicApp</span></span>
* <span data-ttu-id="1e9d3-1407">Grundläggande SKU har lagts till för Integrationskonton</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1407">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="1e9d3-1408">XSLT 2.0, XSLT 3.0 och Flytande mappningstyper har lagts till</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1408">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="1e9d3-1409">Nya cmdletar för integrationskontosammansättningar</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1409">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="1e9d3-1410">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1410">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="1e9d3-1411">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1411">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="1e9d3-1412">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1412">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="1e9d3-1413">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1413">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="1e9d3-1414">Nya cmdletar för batchkonfiguration för integrationskonto</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1414">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="1e9d3-1415">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1415">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="1e9d3-1416">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1416">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="1e9d3-1417">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1417">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="1e9d3-1418">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1418">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="1e9d3-1419">Logic App-SDK har uppdaterats till version 4.1.0</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1419">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="1e9d3-1420">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1420">Az.Monitor</span></span>
* <span data-ttu-id="1e9d3-1421">Hjälpen för Get-AzMetric har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1421">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1e9d3-1422">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1422">Az.Network</span></span>
* <span data-ttu-id="1e9d3-1423">Hjälpexempel för Add-AzApplicationGatewayCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1423">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="1e9d3-1424">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1424">Az.OperationalInsights</span></span>
* <span data-ttu-id="1e9d3-1425">Ytterligare stöd för datakällorna New och Get ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1425">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="1e9d3-1426">Ny ApplicationInsights-typ har lagts till för att ge stöd för ”Get specific” och ”Get all” för ApplicationInsights-datakällor för angiven arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1426">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="1e9d3-1427">Cmdleten New-AzOperationalInsightsApplicationInsightsDataSource har lagts till för att skapa datakälla med angivna parametrar för Application Insights-resurs: subscription Id, resourceGroupName och name.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1427">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="1e9d3-1428">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1428">Az.Resources</span></span>
* <span data-ttu-id="1e9d3-1429">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1429">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="1e9d3-1430">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1430">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="1e9d3-1431">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1431">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="1e9d3-1432">Fel som gör att KeyCredentials inte kan skapas upprepade gånger har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1432">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="1e9d3-1433">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1433">Az.Sql</span></span>
* <span data-ttu-id="1e9d3-1434">Lägg till stöd för hyperskalanivån för SQL DB</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1434">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="1e9d3-1435">Ett fel har åtgärdats där återställningen kunde misslyckas på grund av onödiga inställningsegenskaper i restore-förfrågan</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1435">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1e9d3-1436">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1436">Az.Websites</span></span>
* <span data-ttu-id="1e9d3-1437">Rätt exempel i Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1437">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="1e9d3-1438">1.3.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1438">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1e9d3-1439">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1439">Az.Accounts</span></span>
* <span data-ttu-id="1e9d3-1440">Uppdatera till den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1440">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="1e9d3-1441">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1441">Az.AnalysisServices</span></span>
<span data-ttu-id="1e9d3-1442">Allmän tillgänglighet för Az.AnalysisServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1442">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1e9d3-1443">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1443">Az.Compute</span></span>
* <span data-ttu-id="1e9d3-1444">AEM-tillägg: Lägg till stöd för UltraSSD-, P60-, P70- och P80-diskar</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1444">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="1e9d3-1445">Uppdatera hjälpbeskrivning för Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1445">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="1e9d3-1446">Uppdatera hjälpbeskrivning och exempel för Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1446">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1e9d3-1447">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1447">Az.RecoveryServices</span></span>
<span data-ttu-id="1e9d3-1448">Allmän tillgänglighet för Az.RecoveryServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1448">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="1e9d3-1449">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1449">Az.Resources</span></span>
* <span data-ttu-id="1e9d3-1450">Korrigera taggar för resursgrupper</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1450">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="1e9d3-1451">Mer information här: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1451">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="1e9d3-1452">Åtgärda problem där `Get-AzureRmRoleAssignment` inte respekterar -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1452">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="1e9d3-1453">Mer information här: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1453">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="1e9d3-1454">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1454">Az.Sql</span></span>
* <span data-ttu-id="1e9d3-1455">Lägga till Get/Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1455">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="1e9d3-1456">Åtgärda problem där ett nullref-undantag uppstår när du kör SQL-cmdletar och inte är inloggad på ett Azure-konto</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1456">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="1e9d3-1457">Åtgärda nullref-undantag i Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1457">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="1e9d3-1458">1.2.1 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1458">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1e9d3-1459">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1459">Az.Accounts</span></span>
* <span data-ttu-id="1e9d3-1460">Version med rätt version av autentisering</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1460">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="1e9d3-1461">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1461">Az.AnalysisServices</span></span>
* <span data-ttu-id="1e9d3-1462">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1462">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1e9d3-1463">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1463">Az.RecoveryServices</span></span>
* <span data-ttu-id="1e9d3-1464">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1464">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="1e9d3-1465">1.2.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1465">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1e9d3-1466">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1466">Az.Accounts</span></span>
* <span data-ttu-id="1e9d3-1467">Lägga till interaktiv autentisering och autentisering med användarnamn/lösenord för endast Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1467">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="1e9d3-1468">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1468">Update incorrect online help URLs</span></span>
* <span data-ttu-id="1e9d3-1469">Lägga till varningsmeddelande i PS Core för Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1469">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="1e9d3-1470">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1470">Az.Aks</span></span>
* <span data-ttu-id="1e9d3-1471">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1471">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="1e9d3-1472">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1472">Az.Automation</span></span>
* <span data-ttu-id="1e9d3-1473">Stöd för Python 2-runbookflöden har lagts till</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1473">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="1e9d3-1474">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1474">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="1e9d3-1475">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1475">Az.Cdn</span></span>
* <span data-ttu-id="1e9d3-1476">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1476">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1e9d3-1477">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1477">Az.Compute</span></span>
* <span data-ttu-id="1e9d3-1478">Lägga till cmdleten Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1478">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="1e9d3-1479">Lägga till TempDisk-parameter i Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1479">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="1e9d3-1480">Korrigera varningsmeddelande för New-AzVM</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1480">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="1e9d3-1481">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1481">Az.ContainerRegistry</span></span>
* <span data-ttu-id="1e9d3-1482">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1482">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1e9d3-1483">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1483">Az.DataFactory</span></span>
* <span data-ttu-id="1e9d3-1484">ADF .Net SDK-versionen har uppdaterats till 3.0.0</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1484">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="1e9d3-1485">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1485">Az.DataLakeStore</span></span>
* <span data-ttu-id="1e9d3-1486">Åtgärda problem med ADLS-slutpunkt vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1486">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="1e9d3-1487">Mer information här: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1487">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="1e9d3-1488">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1488">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="1e9d3-1489">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1489">Az.IotHub</span></span>
* <span data-ttu-id="1e9d3-1490">Lägga till kodningsformat i cmdleten Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1490">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="1e9d3-1491">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1491">Az.KeyVault</span></span>
* <span data-ttu-id="1e9d3-1492">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1492">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1e9d3-1493">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1493">Az.Network</span></span>
* <span data-ttu-id="1e9d3-1494">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1494">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="1e9d3-1495">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1495">Az.Resources</span></span>
* <span data-ttu-id="1e9d3-1496">Åtgärda felaktiga exempel i referensdokumentationen ”New-AzADAppCredential” och ”New-AzADSpCredential”</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1496">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="1e9d3-1497">Åtgärda problem där sökvägen för parametern ”-TemplateFile” inte omvandlas innan cmdletarna för distribution i resursgruppen körs</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1497">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="1e9d3-1498">Az.Resources: Korrigera dokumentationen om standardvärdet för New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1498">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="1e9d3-1499">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1499">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="1e9d3-1500">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1500">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="1e9d3-1501">Åtgärda formateringsproblemet med objektet ”PSResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1501">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="1e9d3-1502">Mer information här: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1502">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="1e9d3-1503">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1503">Az.ServiceFabric</span></span>
* <span data-ttu-id="1e9d3-1504">Återställ när ett certifikat läggs till i en Virtual Machine Scale Sets-modell men ett undantag genereras. Detta har gjorts för att åtgärda följande fel: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1504">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="1e9d3-1505">Korrigera några felmeddelanden.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1505">Fix some error messages.</span></span>
* <span data-ttu-id="1e9d3-1506">Korrigering av skapande av kluster med ARM-mall som är standard för New-AzServiceFabriCluster som inte fungerade med migrering till Az.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1506">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="1e9d3-1507">Korrigering av tilläggning av kluster/programcertifikat så att endast VM Scale Sets som motsvarar klustret läggs till genom att kontrollera ID för klustret i tillägget.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1507">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="1e9d3-1508">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1508">Az.SignalR</span></span>
* <span data-ttu-id="1e9d3-1509">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1509">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="1e9d3-1510">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1510">Az.Sql</span></span>
* <span data-ttu-id="1e9d3-1511">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1511">Update incorrect online help URLs</span></span>
* <span data-ttu-id="1e9d3-1512">Uppdaterad parameterbeskrivning för LicenseType-parameter med möjliga värden</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1512">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="1e9d3-1513">Korrigering för att uppdatera hanterad instansidentitet som inte fungerar när det är den enda uppdaterade egenskapen</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1513">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="1e9d3-1514">Stöd för anpassad sortering på hanterad instans</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1514">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1e9d3-1515">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1515">Az.Storage</span></span>
* <span data-ttu-id="1e9d3-1516">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1516">Update incorrect online help URLs</span></span>
* <span data-ttu-id="1e9d3-1517">Tillhandahåll detaljerat felmeddelande när en användare försöker hämta/konfigurera klassisk loggning/mått på ett Premium Storage-konto eftersom Premium Storage-kontot inte har stöd för klassisk loggning/mått.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1517">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="1e9d3-1518">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1518">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="1e9d3-1519">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1519">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="1e9d3-1520">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1520">Az.TrafficManager</span></span>
* <span data-ttu-id="1e9d3-1521">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1521">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1e9d3-1522">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1522">Az.Websites</span></span>
* <span data-ttu-id="1e9d3-1523">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1523">Update incorrect online help URLs</span></span>
* <span data-ttu-id="1e9d3-1524">Korrigerar ”New-AzWebAppSSLBinding” så att certifikatet laddas upp till rätt resursgrupp och plats om appen finns i en ASE.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1524">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="1e9d3-1525">Korrigerar ”New-AzWebAppSSLBinding” så att taggarna inte skrivs över på en bindning av ett SSL-certifikat till en app</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1525">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="1e9d3-1526">1.1.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1526">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1e9d3-1527">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1527">Az.Accounts</span></span>
* <span data-ttu-id="1e9d3-1528">Lade till omfattningen ”Lokal” till Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1528">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1e9d3-1529">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1529">Az.Compute</span></span>
* <span data-ttu-id="1e9d3-1530">Namn är nu valfritt i ID-parametern för Restart/Start/Stop/Remove/Set-AzVM och Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1530">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="1e9d3-1531">Uppdaterade beskrivningen av ID i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1531">Updated the description of ID in help files</span></span>
* <span data-ttu-id="1e9d3-1532">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1532">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="1e9d3-1533">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1533">Az.DataLakeStore</span></span>
* <span data-ttu-id="1e9d3-1534">Uppdatera sdk-versionen av dataplanet till 1.1.14 för SDK-korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1534">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="1e9d3-1535">Korrigerade hanteringen av negativ accesstime och modificationtime för getfilestatus och liststatus; korrigera asynkront annulleringstoken</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1535">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="1e9d3-1536">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1536">Az.EventGrid</span></span>
* <span data-ttu-id="1e9d3-1537">Uppdaterat för användning av API-versionen 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1537">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="1e9d3-1538">Uppdaterade följande cmdletar för att stödja nytt scenario i API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1538">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="1e9d3-1539">New-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1539">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="1e9d3-1540">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1540">Event Time-To-Live,</span></span>
        - <span data-ttu-id="1e9d3-1541">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1541">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="1e9d3-1542">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1542">Dead letter endpoint.</span></span>
    - <span data-ttu-id="1e9d3-1543">Update-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1543">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="1e9d3-1544">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1544">Event Time-To-Live,</span></span>
        - <span data-ttu-id="1e9d3-1545">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1545">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="1e9d3-1546">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1546">Dead letter endpoint.</span></span>
* <span data-ttu-id="1e9d3-1547">Lade till nya enum-värden (storageQueue och hybridConnection) för alternativet EndpointType i cmdletarna New-AzureRmEventGridSubscription och Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1547">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="1e9d3-1548">Visa varningsmeddelanden om skapande eller uppdatering av händelseprenumerationen förväntas medföra manuell åtgärd från användaren.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1548">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="1e9d3-1549">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1549">Az.IotHub</span></span>
* <span data-ttu-id="1e9d3-1550">Har uppdaterats till den senaste versionen av SDK:n lotHub</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1550">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="1e9d3-1551">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1551">Az.LogicApp</span></span>
* <span data-ttu-id="1e9d3-1552">Get-AzLogicApp visar en lista över alla som inte har angivet namn</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1552">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="1e9d3-1553">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1553">Az.Resources</span></span>
* <span data-ttu-id="1e9d3-1554">Åtgärdade problem med parameteruppsättningen när parametrarna -ODataQuery och -ResourceId anges för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1554">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="1e9d3-1555">Mer information här: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1555">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="1e9d3-1556">Åtgärdade hantering av parametern -Custom i New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1556">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="1e9d3-1557">Korrigerade stavfel i New-AzDeployment-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1557">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="1e9d3-1558">Gjorde parametern -MailNickname obligatorisk för New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1558">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="1e9d3-1559">Mer information här: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1559">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="1e9d3-1560">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1560">Az.SignalR</span></span>
* <span data-ttu-id="1e9d3-1561">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1561">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="1e9d3-1562">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1562">Az.Sql</span></span>
* <span data-ttu-id="1e9d3-1563">Konverterade lagringshanteringsklientens beroende av den normala SDK-implementeringen.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1563">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1e9d3-1564">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1564">Az.Storage</span></span>
* <span data-ttu-id="1e9d3-1565">Angav StorageAccountName för lagringskontext som det verkliga namnet på lagringskontot när det skapas med Sas Token, OAuth eller Anonymous</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1565">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="1e9d3-1566">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1566">New-AzStorageContext</span></span>
* <span data-ttu-id="1e9d3-1567">Skapade Sas Token för Blob Snapshot-objekt med parametern -FullUri, åtgärdade den returnerade URI:n så att den blir URI för ögonblicksbild</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1567">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="1e9d3-1568">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1568">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1e9d3-1569">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1569">Az.Websites</span></span>
* <span data-ttu-id="1e9d3-1570">Åtgärdade en bugg i datumparsningen i Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1570">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="1e9d3-1571">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1571">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="1e9d3-1572">1.0.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1572">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="1e9d3-1573">Allmänt</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1573">General</span></span>

- <span data-ttu-id="1e9d3-1574">Allmän tillgänglighet för Az-modulen</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1574">General Availability of Az Module</span></span>
- <span data-ttu-id="1e9d3-1575">Onlinehjälp för varje modul</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1575">Online help for each module</span></span>
- <span data-ttu-id="1e9d3-1576">Mer information och en översikt finns på [Az-informationssidan](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1576">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="1e9d3-1577">Information om hur du migrerar från AzureRM finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1577">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="1e9d3-1578">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1578">Az.Accounts</span></span>
- <span data-ttu-id="1e9d3-1579">Har ändrats från Az.Profile</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1579">Changed from Az.Profile</span></span>
- <span data-ttu-id="1e9d3-1580">Fasta tabellformat för profil- och kontexttyper</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1580">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="1e9d3-1581">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1581">Az.ApiManagement</span></span>
- <span data-ttu-id="1e9d3-1582">Korrigeringar för #7002</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1582">Fixes for #7002</span></span>
- <span data-ttu-id="1e9d3-1583">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1583">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="1e9d3-1584">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1584">Az.Batch</span></span>
- <span data-ttu-id="1e9d3-1585">Lade till möjligheten att se vilken version av Azure Batch Node Agent som körs på var och en av de virtuella datorerna i en pool, via den nya egenskapen `NodeAgentInformation` på `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1585">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="1e9d3-1586">Standarden `Caching` för `PSDataDisk` är nu `ReadWrite` i stället för `None`.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1586">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="1e9d3-1587">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1587">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="1e9d3-1588">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1588">Az.Billing</span></span>
- <span data-ttu-id="1e9d3-1589">Kombinerar cmdletarna för fakturering, förbrukning och UsageAggregates. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1589">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="1e9d3-1590">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1590">Az.CognitivServices</span></span>
- <span data-ttu-id="1e9d3-1591">Lade till kompletterare för SkuName och Typem som är tillgängliga i New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1591">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="1e9d3-1592">Tog bort parameteruppsättningen GetSkusWithAccountParamSetName från Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1592">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="1e9d3-1593">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1593">Az.ContainerInstance</span></span>
- <span data-ttu-id="1e9d3-1594">Stöd för ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1594">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="1e9d3-1595">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1595">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="1e9d3-1596">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1596">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="1e9d3-1597">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1597">Az.DataLakeStore</span></span>
- <span data-ttu-id="1e9d3-1598">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1598">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="1e9d3-1599">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1599">Az.Monitor</span></span>
- <span data-ttu-id="1e9d3-1600">Döpte om Az.Insights till Az.Monitor och andra mindre icke-bakåtkompatibla ändringar. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1600">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="1e9d3-1601">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1601">Az.KeyVault</span></span>
- <span data-ttu-id="1e9d3-1602">Tog bort den inaktuella egenskapen PurgeDisabled från utdatatyper</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1602">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="1e9d3-1603">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1603">Az.MachineLearning</span></span>
- <span data-ttu-id="1e9d3-1604">Inkluderade cmdletarna från modulen Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1604">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="1e9d3-1605">Az.Media</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1605">Az.Media</span></span>
- <span data-ttu-id="1e9d3-1606">Tog bort inaktuella -Tags-alias från New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1606">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="1e9d3-1607">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1607">Az.Network</span></span>
<span data-ttu-id="1e9d3-1608">Stöd har lagts till för konfiguration av RewriteRuleSets i Application Gateway</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1608">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="1e9d3-1609">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1609">New cmdlets added:</span></span>
        - <span data-ttu-id="1e9d3-1610">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1610">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="1e9d3-1611">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1611">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="1e9d3-1612">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1612">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="1e9d3-1613">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1613">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="1e9d3-1614">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1614">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="1e9d3-1615">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1615">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="1e9d3-1616">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1616">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="1e9d3-1617">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1617">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="1e9d3-1618">Cmdletar har uppdaterats med den valfria parametern -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1618">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="1e9d3-1619">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1619">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="1e9d3-1620">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1620">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="1e9d3-1621">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1621">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="1e9d3-1622">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1622">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="1e9d3-1623">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1623">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="1e9d3-1624">New-AzureRmApplicationGatewayUrlPathMapConfig har lagt till KeyVault-stöd för Application Gateway med Identity.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1624">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="1e9d3-1625">Cmdletar har uppdaterats med den valfria parametern -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1625">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="1e9d3-1626">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1626">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="1e9d3-1627">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1627">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="1e9d3-1628">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1628">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="1e9d3-1629">Cmdleten New-AzApplicationGateway har uppdaterats med den valfria parametern -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1629">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="1e9d3-1630">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1630">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="1e9d3-1631">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1631">Az.OperationalInsights</span></span>
- <span data-ttu-id="1e9d3-1632">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1632">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="1e9d3-1633">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1633">Az.Profile</span></span>
- <span data-ttu-id="1e9d3-1634">Modulnamnet har ändrats till Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1634">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="1e9d3-1635">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1635">Az.RecoveryServices</span></span>
- <span data-ttu-id="1e9d3-1636">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1636">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="1e9d3-1637">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1637">Az.Resources</span></span>
- <span data-ttu-id="1e9d3-1638">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1638">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="1e9d3-1639">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1639">Az.ServiceFabric</span></span>
- <span data-ttu-id="1e9d3-1640">Stöd för specificering av certifikat efter eget namn och tumavtryck</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1640">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="1e9d3-1641">Information om fler icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1641">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="1e9d3-1642">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1642">Az.SIgnalR</span></span>
- <span data-ttu-id="1e9d3-1643">Allmän tillgänglighet för PowerShell-cmdletar för SIgnalR</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1643">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="1e9d3-1644">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1644">Az.Sql</span></span>
- <span data-ttu-id="1e9d3-1645">Lade till de nya identifieringstyperna Data_Exfiltration och Unsafe_Action i Threat Detection-cmdletar</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1645">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="1e9d3-1646">Uppdaterade dokumentationsexempel för Sql Auditing-cmdletar</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1646">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="1e9d3-1647">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1647">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="1e9d3-1648">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1648">Az.Storage</span></span>
- <span data-ttu-id="1e9d3-1649">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1649">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="1e9d3-1650">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1650">Az.Websites</span></span>
- <span data-ttu-id="1e9d3-1651">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1651">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="1e9d3-1652">0.7.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1652">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="1e9d3-1653">Allmänt</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1653">General</span></span>

* <span data-ttu-id="1e9d3-1654">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1654">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="1e9d3-1655">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1655">Az.Compute</span></span>

* <span data-ttu-id="1e9d3-1656">Lade till stöd för UltraSSD och Galleriavbildningar i de enkla parameteruppsättningarna för `New-AzVm(ss)`-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1656">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="1e9d3-1657">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1657">Az.DataLakeStore</span></span>

* <span data-ttu-id="1e9d3-1658">Åtgärdade avslutande snedstreck i domänen för adls-konto</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1658">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="1e9d3-1659">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1659">Az.FrontDoor</span></span>

* <span data-ttu-id="1e9d3-1660">Brutna länkar korrigerades</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1660">Fixed some broken links</span></span>
    - <span data-ttu-id="1e9d3-1661">I artiklarna New-AzureRmFrontDoor och Set-AzureRmFrontDoor artiklar korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1661">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="1e9d3-1662">I artikeln New-AzureRmFrontDoorManagedRuleObject korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1662">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="1e9d3-1663">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1663">Az.RecoveryServices</span></span>

* <span data-ttu-id="1e9d3-1664">Lade till valideringar på klientsidan för Azure-filresurs med återställningsåtgärder.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1664">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="1e9d3-1665">Gjorde storageAccountName och storageAccountResourceGroupName valfritt för afs-återställning.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1665">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="1e9d3-1666">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1666">Az.Resources</span></span>

* <span data-ttu-id="1e9d3-1667">Korrigering för https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1667">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="1e9d3-1668">Uppdaterade Get-AzureRmRoleAssignment så att prenumerationsomfattningen används om den anges vid begäran om klassiska administratörer.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1668">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="1e9d3-1669">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1669">Az.Sql</span></span>

* <span data-ttu-id="1e9d3-1670">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1670">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="1e9d3-1671">Korrigerade ett problem med Get-AzureRmSqlDatabaseVulnerabilityAssessment med DotNet-kärna</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1671">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="1e9d3-1672">Ändrade dokumentationen för hjälpmeddelanden som rör SQL Auditing-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1672">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="1e9d3-1673">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1673">Az.Storage</span></span>

* <span data-ttu-id="1e9d3-1674">Lade till -EnableHierarchicalNamespace i New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1674">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="1e9d3-1675">Åtgärdade problemet med att cmdleten Copy File inte kunde återanvända källkontexten på målet om inte -DestContext angetts</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1675">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="1e9d3-1676">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1676">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="1e9d3-1677">Stöd för statisk webbplatskonfiguration</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1677">Support Static Website configuration</span></span>
    - <span data-ttu-id="1e9d3-1678">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1678">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="1e9d3-1679">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1679">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="1e9d3-1680">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1680">Az.Websites</span></span>

* <span data-ttu-id="1e9d3-1681">Set-AzureRmWebApp och Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1681">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="1e9d3-1682">Ny parameter (-AzureStoragePath) har lagts till för att ange att Azure Storage-sökvägar ska monteras i containerappar i Windows och Linux.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1682">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="1e9d3-1683">Använder utdata från den nya cmdleten New-AzureRmWebAppAzureStoragePath som en parameter för att ange sökvägar för Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1683">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="1e9d3-1684">0.6.1 – november 2018</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1684">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="1e9d3-1685">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1685">Az.ApiManagement</span></span>
* <span data-ttu-id="1e9d3-1686">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1686">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="1e9d3-1687">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1687">Az.Automation</span></span>
* <span data-ttu-id="1e9d3-1688">Swagger baserade Azure Automation-cmdletar</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1688">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="1e9d3-1689">Cmdletar för Uppdateringshantering har lagts till</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1689">Added Update Management cmdlets</span></span>
* <span data-ttu-id="1e9d3-1690">Cmdletar för källkontroll har lagts till</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1690">Added Source Control cmdlets</span></span>
* <span data-ttu-id="1e9d3-1691">Remove-AzureRmAutomationHybridWorkerGroup-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1691">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="1e9d3-1692">Kommandot för DSC-registreringsnod har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1692">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="1e9d3-1693">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1693">Az.Compute</span></span>
* <span data-ttu-id="1e9d3-1694">Problem med SystemAssigned-identitet har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1694">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="1e9d3-1695">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1695">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="1e9d3-1696">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1696">Az.ContainerInstance</span></span>
* <span data-ttu-id="1e9d3-1697">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1697">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="1e9d3-1698">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1698">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="1e9d3-1699">uppdatera exempelbeskrivningen för marketplace-cmdletar</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1699">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="1e9d3-1700">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1700">Az.Network</span></span>
* <span data-ttu-id="1e9d3-1701">Cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomErreller Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1701">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="1e9d3-1702">ICMP tillbaka till stöd för Azure Firewall-nätverksprotokoll har lagts till</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1702">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="1e9d3-1703">Uppdatera cmdlet Test-AzureRmNetworkWatcherConnectivity, lägga till verifiering av mål-id, adress och port.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1703">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="1e9d3-1704">Åtgärda problem med minnesanvändning i VirtualNetwork-karta</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1704">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="1e9d3-1705">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1705">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="1e9d3-1706">Åtgärda för att ändra principen för en skyddad fildelning.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1706">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="1e9d3-1707">Tidszonsprincipen har konverterats till versaler.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1707">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="1e9d3-1708">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1708">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="1e9d3-1709">Exempel i New-AzureRmRecoveryServicesAsrProtectableItem har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1709">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="1e9d3-1710">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1710">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="1e9d3-1711">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1711">Az.Relay</span></span>
* <span data-ttu-id="1e9d3-1712">Valfri parameter -KeyValue till New-AzureRmRelayKey cmdlet har lagts till, vilket gör det möjligt för användare att tillhandahålla KeyValue.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1712">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="1e9d3-1713">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1713">Az.Resources</span></span>
* <span data-ttu-id="1e9d3-1714">Uppdatera hjälpdokumentation för resursidentitet kopplad till parametrar i `New-AzureRmPolicyAssignment` och `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1714">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="1e9d3-1715">Lägg till ett exempel för New-AzureRmPolicyDefinition som använder -Metadata</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1715">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="1e9d3-1716">Korrigera så att skiftläge behålls i taggnycklar i NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1716">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="1e9d3-1717">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1717">Az.ServiceFabric</span></span>
* <span data-ttu-id="1e9d3-1718">Lägg till utfasningsmeddelanden för kommande icke-kompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1718">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="1e9d3-1719">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1719">Az.Sql</span></span>
* <span data-ttu-id="1e9d3-1720">Nya cmdletar för CRUD-åtgärder på Azure Sql Database-hanterad instans och Azure Sql-hanterad databas</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1720">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="1e9d3-1721">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1721">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="1e9d3-1722">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1722">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="1e9d3-1723">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1723">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="1e9d3-1724">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1724">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="1e9d3-1725">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1725">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="1e9d3-1726">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1726">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="1e9d3-1727">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1727">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="1e9d3-1728">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1728">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="1e9d3-1729">Hantering av utökad granskningsprincip på en server eller en databas har aktiverats.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1729">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="1e9d3-1730">Ny parameter (PredicateExpression) har lagts till för att aktivera filtrering av granskningsloggar.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1730">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="1e9d3-1731">Cmdletar har ändrats så att de använder SQL-klienter i stället för äldre klienter.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1731">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="1e9d3-1732">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1732">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="1e9d3-1733">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1733">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="1e9d3-1734">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1734">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="1e9d3-1735">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1735">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="1e9d3-1736">Problem med att använda Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings med lagringskontots namnparameter har korrigerats</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1736">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="1e9d3-1737">0.5.0 – november 2018</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1737">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="1e9d3-1738">Allmänt</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1738">General</span></span>
* <span data-ttu-id="1e9d3-1739">Lade till resurskompletterare till många kärn-cmdletar – dessa gör att du kan stega genom befintliga resursnamn med TABB vid interaktiva anrop till cmdletar</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1739">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="1e9d3-1740">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1740">Az.Profile</span></span>
* <span data-ttu-id="1e9d3-1741">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1741">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="1e9d3-1742">Bytte namn på parametern TenantId i cmdleten Connect-AzAccount till Tenant och lade till ett alias för TenantId</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1742">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="1e9d3-1743">Uppdaterade TenantId-beskrivningen för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1743">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="1e9d3-1744">Åtgärda felmeddelande för misslyckad inloggning när du tillhandahåller klientdomän</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1744">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="1e9d3-1745">Åtgärda problem med att kontextnamn hamnar i konflikt för konton utan prenumerationer i klientorganisationen</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1745">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="1e9d3-1746">Åtgärda problem med DataLake-slutpunkter vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1746">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="1e9d3-1747">Åtgärdade problem med att Disconnect-AzAccount kastades om den inte anslöts</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1747">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="1e9d3-1748">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1748">Az.CognitiveServices</span></span>
* <span data-ttu-id="1e9d3-1749">Lade till åtgärden Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1749">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1e9d3-1750">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1750">Az.Compute</span></span>
* <span data-ttu-id="1e9d3-1751">Lade till cmdletarna Add-AzVmssVMDataDisk och Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1751">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="1e9d3-1752">Get-AzVMImage visar AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1752">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="1e9d3-1753">Åtgärdade att värdena för alternativen SetAzVMChefExtension -BootstrapOptions och -JsonAttribute inte angavs i json-format.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1753">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="1e9d3-1754">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1754">Az.DataLakeStore</span></span>
* <span data-ttu-id="1e9d3-1755">Uppdatera DataLake-paketet till 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1755">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="1e9d3-1756">Lägg till standardsamtidighet för flertrådade åtgärder.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1756">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="1e9d3-1757">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1757">Az.Insights</span></span>
* <span data-ttu-id="1e9d3-1758">Åtgärdade problem #7267 (autoskalningsområde)</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1758">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="1e9d3-1759">Problem med att uppräknade parametrar inte ställdes in ordentligt när du skapade en ny autoskalningsregel (de ställdes alltid in med standardvärdet).</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1759">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="1e9d3-1760">Åtgärdade problem #7513 [Insights] Set-AzDiagnosticSetting kräver uttrycklig specifikation av kategorier när inställningar skapas</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1760">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="1e9d3-1761">Nu kräver inte cmdleten uttrycklig anvisning av kategorierna för att aktiveras under skapande, d.v.s. den fungerar enligt beskrivning</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1761">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1e9d3-1762">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1762">Az.Network</span></span>
* <span data-ttu-id="1e9d3-1763">PeeringType ändrades till en obligatorisk parameter för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1763">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="1e9d3-1764">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1764">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="1e9d3-1765">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1765">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="1e9d3-1766">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1766">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="1e9d3-1767">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1767">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="1e9d3-1768">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1768">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="1e9d3-1769">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1769">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="1e9d3-1770">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1770">Az.PolicyInsights</span></span>
* <span data-ttu-id="1e9d3-1771">Cmdletar för principreparation har lagts till</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1771">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="1e9d3-1772">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1772">Az.Resources</span></span>
* <span data-ttu-id="1e9d3-1773">Korrigering för https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1773">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="1e9d3-1774">Tillåt att resurser listas med parametern -ResourceId för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1774">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="1e9d3-1775">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1775">Az.ServiceBus</span></span>
* <span data-ttu-id="1e9d3-1776">Skrivskyddad MigrationState-egenskap har lagts till i PSServiceBusMigrationConfigurationAttributes, som hjälper till att hålla koll på migreringstillståndet.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1776">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="1e9d3-1777">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1777">Az.ServiceFabric</span></span>
* <span data-ttu-id="1e9d3-1778">Åtgärda att lägga till certifikat till Linux-Vmss.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1778">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="1e9d3-1779">Åtgärdade Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1779">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="1e9d3-1780">Använd rätt tumavtryck från nya certifikat (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1780">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="1e9d3-1781">Visa undantag korrekt (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1781">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="1e9d3-1782">Åtgärdade Update-AzServiceFabricDurability så att klusterkonfigurationen uppdateras innan Vmss-åtgärden CreateOrUpdate påbörjas.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1782">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="1e9d3-1783">0.4.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1783">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="1e9d3-1784">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1784">Az.Profile</span></span>
* <span data-ttu-id="1e9d3-1785">Åtgärdade problemet med Get-AzSubscription i CloudShell</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1785">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="1e9d3-1786">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1786">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1e9d3-1787">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1787">Az.Compute</span></span>
* <span data-ttu-id="1e9d3-1788">Nya storlekar lades till i listan över godkända VM-storlekar för vilka accelererat nätverk kommer att aktiveras vid användning av den enkla parameteruppsättningen för New-AzVm</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1788">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="1e9d3-1789">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1789">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="1e9d3-1790">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1790">Az.DataLakeStore</span></span>
* <span data-ttu-id="1e9d3-1791">Lägger till stöd för regler för virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1791">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="1e9d3-1792">Get-AzDataLakeStoreVirtualNetworkRule: Hämtar eller listar regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1792">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="1e9d3-1793">Add-AzDataLakeStoreVirtualNetworkRule: Lägger till en regel för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1793">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="1e9d3-1794">Set-AzDataLakeStoreVirtualNetworkRule: Ändrar den angivna regeln för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1794">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="1e9d3-1795">Remove-AzDataLakeStoreVirtualNetworkRule: Tar bort en regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1795">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1e9d3-1796">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1796">Az.Network</span></span>
* <span data-ttu-id="1e9d3-1797">Skicka protokollvärdet till serverdelen för att uppdatera cmdleten Test-AzNetworkWatcherConnectivity.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1797">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="1e9d3-1798">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1798">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="1e9d3-1799">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1799">Az.Resources</span></span>
* <span data-ttu-id="1e9d3-1800">Åtgärdade problem där Get-AzRoleDefinition genererar ett oläsligt undantag (när standardprofilen inte innehåller någon prenumeration och ingen omfattning har angetts) genom att lägga till ett beskrivande undantag i scenariot.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1800">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="1e9d3-1801">Ställ in ”RoleDefinitionNameParameterSet” som standardparameteruppsättning.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1801">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="1e9d3-1802">0.3.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1802">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="1e9d3-1803">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1803">Azure.Storage</span></span>
* <span data-ttu-id="1e9d3-1804">Åtgärda fel där Kopiera blob/fil inte kopierar metadata när målplatsen har ett problem med metadata</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1804">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="1e9d3-1805">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1805">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="1e9d3-1806">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1806">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="1e9d3-1807">Stöd för att hämta användningsinformation om en Storage-resurs för en specifik plats och för att lägga till ett varningsmeddelande för att hämta användningsinformation om en global Storage-resurs är inaktuellt.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1807">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="1e9d3-1808">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1808">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="1e9d3-1809">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1809">Az.CognitiveServices</span></span>
* <span data-ttu-id="1e9d3-1810">Stöd för Get-AzCognitiveServicesAccountSkus utan ett befintligt konto.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1810">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1e9d3-1811">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1811">Az.Compute</span></span>
* <span data-ttu-id="1e9d3-1812">Åtgärdade fel där Get-AzVM -ResourceGroupName <rg> returnerar fler än 50 resultat om det behövs</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1812">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="1e9d3-1813">Lade till ett exempel för SimpleParameterSet i hjälpen för cmdleten New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1813">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="1e9d3-1814">Ett stavfel i förloppsmeddelandet för Azure Disk Encryption har korrigerats</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1814">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="1e9d3-1815">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1815">Az.DataFactoryV2</span></span>
* <span data-ttu-id="1e9d3-1816">ADF .Net SDK-versionen har uppdaterats till 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1816">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1e9d3-1817">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1817">Az.Network</span></span>
* <span data-ttu-id="1e9d3-1818">Funktionalitet för NetworkProfile har lagts till.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1818">Added NetworkProfile functionality.</span></span> <span data-ttu-id="1e9d3-1819">nya cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1819">new cmdlets added</span></span>
    - <span data-ttu-id="1e9d3-1820">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1820">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="1e9d3-1821">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1821">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="1e9d3-1822">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1822">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="1e9d3-1823">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1823">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="1e9d3-1824">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1824">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="1e9d3-1825">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1825">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="1e9d3-1826">Länk för tjänstassociering på modell för undernät har lagts till</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1826">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="1e9d3-1827">Cmdletarna New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap och Remove-AzVirtualNetworkTap har lagts till</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1827">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="1e9d3-1828">Cmdletarna Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig och Remove-AzNEtworkInterfaceTapConfig har lagts till</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1828">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="1e9d3-1829">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1829">Az.RedisCache</span></span>
* <span data-ttu-id="1e9d3-1830">Tillåt att alla strängar används som storleksparametrar framöver.</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1830">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="1e9d3-1831">Lägg till P5 i popup-fönstret PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1831">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="1e9d3-1832">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1832">Az.Resources</span></span>
* <span data-ttu-id="1e9d3-1833">Parametern -Mode som saknades i Set-AzPolicyDefinition har lagts till</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1833">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="1e9d3-1834">Åtgärdade buggen för cmdleten Get-AzProviderOperation för åtgärder med ursprung som innehåller användare</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1834">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="1e9d3-1835">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1835">Az.Sql</span></span>
* <span data-ttu-id="1e9d3-1836">Ett problem där vissa cmdletar för säkerhetskopiering inte kunde identifiera den aktuella azure-prenumerationen har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1836">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1e9d3-1837">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1837">Az.Websites</span></span>
* <span data-ttu-id="1e9d3-1838">Ny cmdlet: Get-AzWebAppContainerContinuousDeploymentUrl – Hämtar webhook-URL:en för kontinuerlig distribution av container</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1838">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="1e9d3-1839">Nya cmdletar: New-AzWebAppContainerPSSession och Enter-WebAppContainerPSSession – Startar en PowerShell-fjärrsession i en containerapp för windows</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1839">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="1e9d3-1840">0.2.0 – september 2018</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1840">0.2.0 - September 2018</span></span>
 <span data-ttu-id="1e9d3-1841">Första versionen</span><span class="sxs-lookup"><span data-stu-id="1e9d3-1841">Initial Release</span></span>
