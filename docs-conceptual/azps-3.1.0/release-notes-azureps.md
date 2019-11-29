---
title: Viktig information om Azure PowerShell
description: Lär dig mer om alla de senaste uppdateringarna för Azure PowerShell-modulerna.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/15/2019
ms.openlocfilehash: 2280b594ee9f525b2fa3175c917f6365cea354ba
ms.sourcegitcommit: 45e1823aa1a792840aa4829831b5f67a9d5d24a0
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/26/2019
ms.locfileid: "74537129"
---
## <a name="310---november-2019"></a><span data-ttu-id="17a3f-103">3.1.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="17a3f-103">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="17a3f-104">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="17a3f-104">Highlights since the last major release</span></span>
* <span data-ttu-id="17a3f-105">Az.DataBoxEdge 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="17a3f-105">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="17a3f-106">Az.SqlVirtualMachine 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="17a3f-106">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="17a3f-107">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="17a3f-107">Az.Compute</span></span>
* <span data-ttu-id="17a3f-108">Funktion för att använda en virtuell dator igen</span><span class="sxs-lookup"><span data-stu-id="17a3f-108">VM Reapply feature</span></span>
    - <span data-ttu-id="17a3f-109">Lägg till parameter för att använda igen till cmdleten Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="17a3f-109">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="17a3f-110">Funktionen AutomaticRepairs i VM-skalningsuppsättningar:</span><span class="sxs-lookup"><span data-stu-id="17a3f-110">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="17a3f-111">Lägg till parametrarna EnableAutomaticRepair, AutomaticRepairGracePeriod och AutomaticRepairMaxInstanceRepairsPercent till följande cmdletar:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="17a3f-111">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="17a3f-112">Stöd för galleriavbildningar i flera klientorganisationer för New-AzVM</span><span class="sxs-lookup"><span data-stu-id="17a3f-112">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="17a3f-113">Lägg till "Spot" till argumentslutföraren i prioritetsparametern i cmdletarna New-AzVM, New-AzVMConfig och New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="17a3f-113">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="17a3f-114">Lägg till parametrarna DiskIOPSReadWrite och DiskMBpsReadWrite till cmdleten Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="17a3f-114">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="17a3f-115">Ändra parametern SourceImageId för cmdleten New-AzGalleryImageVersion till valfri</span><span class="sxs-lookup"><span data-stu-id="17a3f-115">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="17a3f-116">Lägg till parametrarna OSDiskImage och DataDiskImage till cmdleten New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="17a3f-116">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="17a3f-117">Lägg till parametern HyperVGeneration till cmdleten New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="17a3f-117">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="17a3f-118">Lägg till parametern SkipExtensionsOnOverprovisionedVMs till cmdletarna New-AzVmss, New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="17a3f-118">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="17a3f-119">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="17a3f-119">Az.DataBoxEdge</span></span>
* <span data-ttu-id="17a3f-120">Cmdleten `Get-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="17a3f-120">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="17a3f-121">Hämta ordning</span><span class="sxs-lookup"><span data-stu-id="17a3f-121">Get the Order</span></span>
* <span data-ttu-id="17a3f-122">Cmdleten `New-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="17a3f-122">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="17a3f-123">Skapa ny ordning</span><span class="sxs-lookup"><span data-stu-id="17a3f-123">Create new Order</span></span>
* <span data-ttu-id="17a3f-124">Cmdleten `Remove-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="17a3f-124">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="17a3f-125">Ta bort ordning</span><span class="sxs-lookup"><span data-stu-id="17a3f-125">Remove the Order</span></span>
* <span data-ttu-id="17a3f-126">Cmdleten `New-AzDataBoxEdgeShare` har ändrats</span><span class="sxs-lookup"><span data-stu-id="17a3f-126">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="17a3f-127">Nu skapas lokal filresurs</span><span class="sxs-lookup"><span data-stu-id="17a3f-127">Now creates Local Share</span></span>
* <span data-ttu-id="17a3f-128">Cmdleten `Set-AzDataBoxEdgeRole` har lagts till</span><span class="sxs-lookup"><span data-stu-id="17a3f-128">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="17a3f-129">Nu kan IotRole mappas till filresursen</span><span class="sxs-lookup"><span data-stu-id="17a3f-129">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="17a3f-130">Cmdleten `Invoke-AzDataBoxEdgeDevice` har lagts till</span><span class="sxs-lookup"><span data-stu-id="17a3f-130">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="17a3f-131">Anropa genomsökningsuppdatering, ladda ned uppdatering, installera uppdateringar på enheten</span><span class="sxs-lookup"><span data-stu-id="17a3f-131">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="17a3f-132">Cmdleten `Get-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="17a3f-132">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="17a3f-133">Hämtar information om utlösare</span><span class="sxs-lookup"><span data-stu-id="17a3f-133">Gets the information about Triggers</span></span>
* <span data-ttu-id="17a3f-134">Cmdleten `New-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="17a3f-134">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="17a3f-135">Skapa nya utlösare</span><span class="sxs-lookup"><span data-stu-id="17a3f-135">Create new Triggers</span></span>
* <span data-ttu-id="17a3f-136">Cmdleten `Remove-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="17a3f-136">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="17a3f-137">Ta bort utlösare</span><span class="sxs-lookup"><span data-stu-id="17a3f-137">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="17a3f-138">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="17a3f-138">Az.DataFactory</span></span>
* <span data-ttu-id="17a3f-139">Uppdatera ADF .Net SDK-versionen till 4.4.0</span><span class="sxs-lookup"><span data-stu-id="17a3f-139">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="17a3f-140">Lägg till parametern ExpressCustomSetup för kommandot Set-AzureRmDataFactoryV2IntegrationRuntime för att aktivera installationskonfigurationer och komponenter från tredje part utan anpassat konfigurationsskript.</span><span class="sxs-lookup"><span data-stu-id="17a3f-140">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="17a3f-141">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="17a3f-141">Az.DataLakeStore</span></span>
* <span data-ttu-id="17a3f-142">Uppdatera dokumentation för Get-AzDataLakeStoreDeletedItem och Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="17a3f-142">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="17a3f-143">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="17a3f-143">Az.EventHub</span></span>
* <span data-ttu-id="17a3f-144">Korrigering av problem #10301: Korrigera datumformat för SAS-token</span><span class="sxs-lookup"><span data-stu-id="17a3f-144">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="17a3f-145">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="17a3f-145">Az.FrontDoor</span></span>
* <span data-ttu-id="17a3f-146">Lägg till parametern MinimumTlsVersion till Enable-AzFrontDoorCustomDomainHttps och New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="17a3f-146">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="17a3f-147">Lägg till parametrarna HealthProbeMethod och EnabledState till New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="17a3f-147">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="17a3f-148">Lägg till en ny cmdlet för att skapa BackendPoolsSettings-objekt som passar i skapande/uppdatering av Front Door</span><span class="sxs-lookup"><span data-stu-id="17a3f-148">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="17a3f-149">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="17a3f-149">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="17a3f-150">Az.Network</span><span class="sxs-lookup"><span data-stu-id="17a3f-150">Az.Network</span></span>
* <span data-ttu-id="17a3f-151">Ändra alternativexemplen Start-AzVirtualNetworkGatewayConnectionPacketCapture.md och Start-AzVirtualnetworkGatewayPacketCapture.md för FilterData.</span><span class="sxs-lookup"><span data-stu-id="17a3f-151">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="17a3f-152">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="17a3f-152">Az.PrivateDns</span></span>
* <span data-ttu-id="17a3f-153">Uppdaterade PrivateDns .NET SDK till version 1.0.0</span><span class="sxs-lookup"><span data-stu-id="17a3f-153">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="17a3f-154">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="17a3f-154">Az.RecoveryServices</span></span>
* <span data-ttu-id="17a3f-155">Stöd för att välja disktyp vid aktivering av skydd i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="17a3f-155">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="17a3f-156">Korrigering av bugg för åtgärdsredigering av återställningsplan i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="17a3f-156">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="17a3f-157">Återställningsstöd för att godkänna filestream-databaser i Azure Backup SQL.</span><span class="sxs-lookup"><span data-stu-id="17a3f-157">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="17a3f-158">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="17a3f-158">Az.RedisCache</span></span>
* <span data-ttu-id="17a3f-159">Parametern MinimumTlsVersion har lagts till i cmdletarna New-AzRedisCache och Set-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="17a3f-159">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="17a3f-160">Dessutom har MinimumTlsVersion lagts till i utdata för cmdleten Get-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="17a3f-160">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="17a3f-161">Verifiering har lagts till på parametern -Size i cmdletarna Set-AzRedisCache och New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="17a3f-161">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="17a3f-162">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="17a3f-162">Az.Resources</span></span>
- <span data-ttu-id="17a3f-163">Uppdaterade policy-cmdletar för att använda den nya API-versionen 2019-06-01 som har en ny EnforcementMode-egenskap i policytilldelningen.</span><span class="sxs-lookup"><span data-stu-id="17a3f-163">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="17a3f-164">Uppdaterade hjälpexempel för skapandet av policydefinition</span><span class="sxs-lookup"><span data-stu-id="17a3f-164">Updated create policy definition help example</span></span>
- <span data-ttu-id="17a3f-165">Åtgärda bugg i Remove-AZADServicePrincipal -ServicePrincipalName, utlös null-referens när tjänstens huvudnamn inte hittas.</span><span class="sxs-lookup"><span data-stu-id="17a3f-165">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="17a3f-166">Åtgärda bugg i New-AZADServicePrincipal, utlös null-referens när klientorganisationen inte har någon prenumeration.</span><span class="sxs-lookup"><span data-stu-id="17a3f-166">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="17a3f-167">Ändra New-AzAdServicePrincipal för att endast lägga till autentiseringsuppgifter för det associerade programmet.</span><span class="sxs-lookup"><span data-stu-id="17a3f-167">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="17a3f-168">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="17a3f-168">Az.Sql</span></span>
* <span data-ttu-id="17a3f-169">Stöd har lagts till för databasen ReadReplicaCount.</span><span class="sxs-lookup"><span data-stu-id="17a3f-169">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="17a3f-170">Korrigerade Set-AzSqlDatabase när zonredundans inte har angetts</span><span class="sxs-lookup"><span data-stu-id="17a3f-170">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="17a3f-171">3.0.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="17a3f-171">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="17a3f-172">Allmänt</span><span class="sxs-lookup"><span data-stu-id="17a3f-172">General</span></span>
* <span data-ttu-id="17a3f-173">Az. PrivateDns 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="17a3f-173">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="17a3f-174">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="17a3f-174">Az.Accounts</span></span>
* <span data-ttu-id="17a3f-175">Lägg till ett utfasningsmeddelande för aliaset Resolve-error.</span><span class="sxs-lookup"><span data-stu-id="17a3f-175">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="17a3f-176">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="17a3f-176">Az.Advisor</span></span>
* <span data-ttu-id="17a3f-177">Den nya kategorin Operational Excellence har lagts till i cmdleten Get-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="17a3f-177">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="17a3f-178">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="17a3f-178">Az.Batch</span></span>
* <span data-ttu-id="17a3f-179">`CoreQuota` på `BatchAccountContext` har bytt namn till `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="17a3f-179">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="17a3f-180">Det finns även en ny `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="17a3f-180">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="17a3f-181">Detta påverkar **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="17a3f-181">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="17a3f-182">**New-AzBatchTask** `-ResourceFile`-parameter tar nu en samling `PSResourceFile`-objekt som kan skapas med hjälp av den nya cmdleten **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="17a3f-182">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="17a3f-183">Ny **New-AzBatchResourceFile**-cmdlet för att skapa `PSResourceFile`-objekt.</span><span class="sxs-lookup"><span data-stu-id="17a3f-183">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="17a3f-184">Dessa kan tillhandahållas till **New-AzBatchTask** på `-ResourceFile`-parametern.</span><span class="sxs-lookup"><span data-stu-id="17a3f-184">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="17a3f-185">Detta stöder två nya typer av resursfiler förutom det befintliga sättet med `HttpUrl`:</span><span class="sxs-lookup"><span data-stu-id="17a3f-185">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="17a3f-186">`AutoStorageContainerName`-baserade resursfiler laddar ned en hel container för automatisk lagring till Batch-noden.</span><span class="sxs-lookup"><span data-stu-id="17a3f-186">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="17a3f-187">`StorageContainerUrl`-baserade resursfiler laddar ned containern som anges i webbadressen till Batch-noden.</span><span class="sxs-lookup"><span data-stu-id="17a3f-187">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="17a3f-188">Tog bort egenskapen `ApplicationPackages` för `PSApplication` som returnerades av **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="17a3f-188">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="17a3f-189">Specifika paket i ett program kan nu hämtas med hjälp av **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="17a3f-189">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="17a3f-190">Till exempel: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="17a3f-190">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="17a3f-191">Bytt namn på `ApplicationId` till `ApplicationName` på **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** och **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="17a3f-191">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="17a3f-192">`ApplicationId` är nu ett alias för `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="17a3f-192">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="17a3f-193">Ny `PSWindowsUserConfiguration`-egenskap till `PSUserAccount` lades till.</span><span class="sxs-lookup"><span data-stu-id="17a3f-193">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="17a3f-194">Bytte namn på `Version` till `Name` på `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="17a3f-194">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="17a3f-195">Bytte namn på `BlobSource` till `HttpUrl` på `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="17a3f-195">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="17a3f-196">Tog bort egenskapen `OSDisk` från `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="17a3f-196">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="17a3f-197">Tog bort **Set-AzBatchPoolOSVersion**.</span><span class="sxs-lookup"><span data-stu-id="17a3f-197">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="17a3f-198">Den här åtgärden stöds inte längre.</span><span class="sxs-lookup"><span data-stu-id="17a3f-198">This operation is no longer supported.</span></span>
* <span data-ttu-id="17a3f-199">`TargetOSVersion` har tagits bort från `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="17a3f-199">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="17a3f-200">Bytte namn på `CurrentOSVersion` till `OSVersion` på `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="17a3f-200">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="17a3f-201">`DataEgressGiB` och `DataIngressGiB` har tagits bort från `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="17a3f-201">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="17a3f-202">Tog bort **Get-AzBatchNodeAgentSku** och ersatte det med **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="17a3f-202">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span> 
  - <span data-ttu-id="17a3f-203">**Get-AzBatchSupportedImage** returnerar samma data som **Get-AzBatchNodeAgentSku** men i ett mer användarvänligt format.</span><span class="sxs-lookup"><span data-stu-id="17a3f-203">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="17a3f-204">Nya icke-verifierade avbildningar returneras nu också.</span><span class="sxs-lookup"><span data-stu-id="17a3f-204">New non-verified images are also now returned.</span></span> <span data-ttu-id="17a3f-205">Ytterligare information om `Capabilities` och `BatchSupportEndOfLife` för varje avbildning inkluderas också.</span><span class="sxs-lookup"><span data-stu-id="17a3f-205">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="17a3f-206">Lade till möjlighet att montera fjärrfilsystem på varje nod i en pool via den nya parametern `MountConfiguration` för **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="17a3f-206">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="17a3f-207">Har nu stöd för nätverkssäkerhetsregler som blockerar nätverksåtkomst till en pool baserat på källportens trafik.</span><span class="sxs-lookup"><span data-stu-id="17a3f-207">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="17a3f-208">Detta görs via egenskapen `SourcePortRanges` på `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="17a3f-208">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="17a3f-209">När du kör en container stöder nu Batch körningen av uppgiften i arbetskatalogen för containern eller i arbetskatalogen för Batch-uppgiften.</span><span class="sxs-lookup"><span data-stu-id="17a3f-209">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="17a3f-210">Detta styrs av egenskapen `WorkingDirectory` på `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="17a3f-210">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="17a3f-211">Lade till en funktion för att ange en samling av offentliga IP-adresser på `PSNetworkConfiguration` via den nya egenskapen `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="17a3f-211">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="17a3f-212">Detta garanterar att noderna i poolen har en IP-adress från listan över IP-adresser som tillhandahållits av användare.</span><span class="sxs-lookup"><span data-stu-id="17a3f-212">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="17a3f-213">Om inget värde anges är standardvärdet för `WaitForSuccess` på `PSSTartTask` nu `$True` (var tidigare `$False`).</span><span class="sxs-lookup"><span data-stu-id="17a3f-213">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="17a3f-214">Om inget värde anges är standardvärdet för `Scope` på `PSAutoUserSpecification` nu `Pool` (var tidigare `Task` på Windows och `Pool` på Linux).</span><span class="sxs-lookup"><span data-stu-id="17a3f-214">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="17a3f-215">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="17a3f-215">Az.Cdn</span></span>
* <span data-ttu-id="17a3f-216">Introducerade UrlRewriteAction och CacheKeyQueryStringAction till RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="17a3f-216">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="17a3f-217">Åtgärdade flera buggar, som saknade indata för ”väljare” i cmdleten New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="17a3f-217">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="17a3f-218">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="17a3f-218">Az.Compute</span></span>
* <span data-ttu-id="17a3f-219">Funktion för diskkrypteringsuppsättning</span><span class="sxs-lookup"><span data-stu-id="17a3f-219">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="17a3f-220">Nya cmdletar:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="17a3f-220">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="17a3f-221">Parametern DiskEncryptionSetId har lagts till i följande cmdletar: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="17a3f-221">DiskEncryptionSetId parameter is added to the following cmdlets: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span></span>        
        <span data-ttu-id="17a3f-222">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="17a3f-222">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="17a3f-223">Parametrarna DiskEncryptionSetId och EncryptionType har lagts till i följande cmdletar:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="17a3f-223">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="17a3f-224">Lägg till parametern PublicIPAddressVersion i New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="17a3f-224">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="17a3f-225">Flytta FileUris för anpassat skripttillägg från offentlig inställning till skyddad inställning</span><span class="sxs-lookup"><span data-stu-id="17a3f-225">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="17a3f-226">Lägg till ScaleInPolicy i cmdletarna New-AzVmss, New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="17a3f-226">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="17a3f-227">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="17a3f-227">Breaking changes</span></span>
    - <span data-ttu-id="17a3f-228">Parametern UploadSizeInBytes används istället för DiskSizeGB för New-AzDiskConfig när CreateOption är Uppladdning</span><span class="sxs-lookup"><span data-stu-id="17a3f-228">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="17a3f-229">PublishingProfile.Source.ManagedImage.Id ersätts med StorageProfile.Source.Id i objektet GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="17a3f-229">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="17a3f-230">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="17a3f-230">Az.DataFactory</span></span>
* <span data-ttu-id="17a3f-231">Uppdatera ADF .Net SDK-versionen till 4.3.0</span><span class="sxs-lookup"><span data-stu-id="17a3f-231">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="17a3f-232">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="17a3f-232">Az.DataLakeStore</span></span>
* <span data-ttu-id="17a3f-233">Uppdatera ADLS SDK-version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) innehåller följande korrigeringar</span><span class="sxs-lookup"><span data-stu-id="17a3f-233">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="17a3f-234">Undvik att utlösa undantag när det inte går att deserialisera creationtime för inmatning av papperskorg eller katalog.</span><span class="sxs-lookup"><span data-stu-id="17a3f-234">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="17a3f-235">Gör inställning tillgänglig per tidsgräns för förfrågan i adlsclient</span><span class="sxs-lookup"><span data-stu-id="17a3f-235">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="17a3f-236">Korrigera överföringen av ursprunglig syncflag för badoffset-återställning</span><span class="sxs-lookup"><span data-stu-id="17a3f-236">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="17a3f-237">Korrigera EnumerateDirectory för att hämta fortsättningstoken när svar har kontrollerats</span><span class="sxs-lookup"><span data-stu-id="17a3f-237">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="17a3f-238">Korrigera bugg i Concat</span><span class="sxs-lookup"><span data-stu-id="17a3f-238">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="17a3f-239">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="17a3f-239">Az.FrontDoor</span></span>
* <span data-ttu-id="17a3f-240">Åtgärdade diverse stavfel i modul</span><span class="sxs-lookup"><span data-stu-id="17a3f-240">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="17a3f-241">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="17a3f-241">Az.HDInsight</span></span>
* <span data-ttu-id="17a3f-242">Korrigerade buggen att kunder får felet ”inte en giltig Base-64-sträng” vid användning av Get-AzHDInsightCluster för att hämta klustret med ADLSGen1-lagring.</span><span class="sxs-lookup"><span data-stu-id="17a3f-242">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="17a3f-243">Lägg till en parameter med namnet ”ApplicationId” i de tre cmdletarna Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig och New-AzHDInsightCluster så att kunden kan tillhandahålla tjänstens huvudnamn för program-ID för åtkomst till Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="17a3f-243">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="17a3f-244">Ändrade Microsoft.Azure.Management.HDInsight från 2.1.0 till 5.1.0</span><span class="sxs-lookup"><span data-stu-id="17a3f-244">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="17a3f-245">Fem cmdletar har tagits bort:</span><span class="sxs-lookup"><span data-stu-id="17a3f-245">Removed five cmdlets:</span></span>
    - <span data-ttu-id="17a3f-246">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="17a3f-246">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="17a3f-247">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="17a3f-247">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="17a3f-248">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="17a3f-248">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="17a3f-249">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="17a3f-249">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="17a3f-250">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="17a3f-250">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="17a3f-251">Tre cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="17a3f-251">Added three cmdlets:</span></span>
    - <span data-ttu-id="17a3f-252">Get-AzHDInsightMonitoring som ersätter Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="17a3f-252">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="17a3f-253">Enable-AzHDInsightMonitoring som ersätter Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="17a3f-253">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="17a3f-254">Disable-AzHDInsightMonitoring som ersätter Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="17a3f-254">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="17a3f-255">Korrigerade cmdleten Get-AzHDInsightProperties för att stödja hämtning av funktionsinformation från en viss plats.</span><span class="sxs-lookup"><span data-stu-id="17a3f-255">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="17a3f-256">Parameteruppsättningarna (Spark1 och Spark2) har tagits bort från Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="17a3f-256">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="17a3f-257">Lägg till exempel för cmdleten Add-AzHDInsightSecurityProfile till hjälpdokumenten.</span><span class="sxs-lookup"><span data-stu-id="17a3f-257">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="17a3f-258">Ändrade utdatatyp för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="17a3f-258">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="17a3f-259">Ändrade utdatatyp för Get-AzHDInsightProperties från CapabilitiesResponse till AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="17a3f-259">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="17a3f-260">Ändrade utdatatyp för Remove-AzHDInsightCluster från ClusterGetResponse till bool.</span><span class="sxs-lookup"><span data-stu-id="17a3f-260">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="17a3f-261">Ändrade utdatatyp för Set-AzHDInsightGatewaySettings HttpConnectivitySettings till GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="17a3f-261">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="17a3f-262">Lade till testfall för vissa scenarier.</span><span class="sxs-lookup"><span data-stu-id="17a3f-262">Added some scenario test cases.</span></span>
* <span data-ttu-id="17a3f-263">Ta bort vissa alias: Add-AzHDInsightConfigValues, Get-AzHDInsightProperties.</span><span class="sxs-lookup"><span data-stu-id="17a3f-263">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="17a3f-264">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="17a3f-264">Az.IotHub</span></span>
* <span data-ttu-id="17a3f-265">Icke-bakåtkompatibla ändringar:</span><span class="sxs-lookup"><span data-stu-id="17a3f-265">Breaking changes:</span></span>
    - <span data-ttu-id="17a3f-266">Cmdleten Add-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="17a3f-266">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="17a3f-267">Parameteruppsättningen __AllParameterSets för cmdleten Add-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="17a3f-267">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="17a3f-268">Cmdleten Get-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="17a3f-268">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="17a3f-269">Parameteruppsättningen __AllParameterSets för cmdleten Get-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="17a3f-269">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="17a3f-270">Egenskapen OperationsMonitoringProperties av typen Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="17a3f-270">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="17a3f-271">Egenskapen OperationsMonitoringProperties av typen Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="17a3f-271">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="17a3f-272">Cmdleten New-AzIotHubExportDevice stöder inte längre aliaset New-AzIotHubExportDevices.</span><span class="sxs-lookup"><span data-stu-id="17a3f-272">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="17a3f-273">Cmdleten New-AzIotHubImportDevice stöder inte längre aliaset New-AzIotHubImportDevices.</span><span class="sxs-lookup"><span data-stu-id="17a3f-273">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="17a3f-274">Cmdleten Remove-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="17a3f-274">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="17a3f-275">Parameteruppsättningen __AllParameterSets för cmdleten Remove-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="17a3f-275">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="17a3f-276">Cmdleten Set-AzIotHub har inte längre stöd för parametern OperationsMonitoringProperties och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="17a3f-276">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="17a3f-277">Parameteruppsättningen UpdateOperationsMonitoringProperties för cmdleten Set-AzIotHub har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="17a3f-277">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="17a3f-278">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="17a3f-278">Az.RecoveryServices</span></span>
* <span data-ttu-id="17a3f-279">Azure Site Recovery-stöd för att konfigurera nätverksresurser som NSG, offentliga IP-adresser och interna lastbalanserare för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="17a3f-279">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="17a3f-280">Azure Site Recovery-stöd för att skriva till hanterad disk för vMWare till Azure.</span><span class="sxs-lookup"><span data-stu-id="17a3f-280">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="17a3f-281">Azure Site Recovery-stöd för NIC-reduktion för vMWare till Azure.</span><span class="sxs-lookup"><span data-stu-id="17a3f-281">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="17a3f-282">Azure Site Recovery-stöd för accelererat nätverk för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="17a3f-282">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="17a3f-283">Azure Site Recovery-stöd för automatisk uppdatering av agent för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="17a3f-283">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="17a3f-284">Azure Site Recovery-stöd för Standard SSD för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="17a3f-284">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="17a3f-285">Azure Site Recovery-stöd för tvåstegskryptering i Azure Disk Encryption för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="17a3f-285">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="17a3f-286">Azure Site Recovery-stöd för att skydda nyligen tillagda diskar för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="17a3f-286">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="17a3f-287">En funktion för mjuk borttagning av virtuella datorer samt tester för mjuk borttagning har tagits bort</span><span class="sxs-lookup"><span data-stu-id="17a3f-287">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="17a3f-288">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="17a3f-288">Az.Resources</span></span>
* <span data-ttu-id="17a3f-289">Uppdatera beroendesammansättning för Microsoft.Extensions.Caching.Memory från 1.1.1 till 2.2</span><span class="sxs-lookup"><span data-stu-id="17a3f-289">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="17a3f-290">Az.Network</span><span class="sxs-lookup"><span data-stu-id="17a3f-290">Az.Network</span></span>
* <span data-ttu-id="17a3f-291">Ändra alla cmdletar för PrivateEndpointConnection så att de stöder generiska tjänstleverantörer.</span><span class="sxs-lookup"><span data-stu-id="17a3f-291">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="17a3f-292">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="17a3f-292">Updated cmdlet:</span></span>
        - <span data-ttu-id="17a3f-293">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="17a3f-293">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="17a3f-294">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="17a3f-294">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="17a3f-295">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="17a3f-295">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="17a3f-296">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="17a3f-296">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="17a3f-297">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="17a3f-297">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="17a3f-298">Lägg till ny cmdlet för PrivateLinkResource så att det också stöder generiska tjänstleverantörer.</span><span class="sxs-lookup"><span data-stu-id="17a3f-298">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="17a3f-299">Ny cmdlet:</span><span class="sxs-lookup"><span data-stu-id="17a3f-299">New cmdlet:</span></span>
        - <span data-ttu-id="17a3f-300">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="17a3f-300">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="17a3f-301">Lägg till nya fält och parametrar för funktionen Proxy Protocol V2.</span><span class="sxs-lookup"><span data-stu-id="17a3f-301">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="17a3f-302">Lägg till egenskapen EnableProxyProtocol i PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="17a3f-302">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="17a3f-303">Lägg till egenskapen LinkIdentifier i PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="17a3f-303">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="17a3f-304">Uppdaterade New-AzPrivateLinkService för att lägga till den nya valfria parametern EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="17a3f-304">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="17a3f-305">Korrigera felaktig beskrivning av parameter i referensdokumentationen för New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="17a3f-305">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="17a3f-306">Nya cmdletar som stöder Azure-brandväggsprincipen</span><span class="sxs-lookup"><span data-stu-id="17a3f-306">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="17a3f-307">Lägg till stöd för den underordnade resursen RouteTables för VirtualHub</span><span class="sxs-lookup"><span data-stu-id="17a3f-307">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="17a3f-308">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="17a3f-308">New cmdlets added:</span></span>
        - <span data-ttu-id="17a3f-309">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="17a3f-309">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="17a3f-310">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="17a3f-310">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="17a3f-311">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="17a3f-311">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="17a3f-312">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="17a3f-312">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="17a3f-313">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="17a3f-313">Set-AzVirtualHub</span></span>
* <span data-ttu-id="17a3f-314">Lägg till stöd för ny egenskaps-SKU för VirtualHub och VirtualWANType för VirtualWan</span><span class="sxs-lookup"><span data-stu-id="17a3f-314">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="17a3f-315">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="17a3f-315">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="17a3f-316">New-AzVirtualHub: lade till parameter-SKU</span><span class="sxs-lookup"><span data-stu-id="17a3f-316">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="17a3f-317">Update-AzVirtualHub: lade till parameter-SKU</span><span class="sxs-lookup"><span data-stu-id="17a3f-317">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="17a3f-318">New-AzVirtualWan: lade till parametern VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="17a3f-318">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="17a3f-319">Update-AzVirtualWan: lade till parametern VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="17a3f-319">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="17a3f-320">Lägg till stöd för egenskapen EnableInternetSecurity för HubVnetConnection, VpnConnection och ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="17a3f-320">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="17a3f-321">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="17a3f-321">New cmdlets added:</span></span>
        - <span data-ttu-id="17a3f-322">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="17a3f-322">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="17a3f-323">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="17a3f-323">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="17a3f-324">New-AzureRmVirtualHubVnetConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="17a3f-324">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="17a3f-325">New-AzureRmVpnConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="17a3f-325">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="17a3f-326">Update-AzureRmVpnConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="17a3f-326">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="17a3f-327">New-AzureRmExpressRouteConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="17a3f-327">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="17a3f-328">Set-AzureRmExpressRouteConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="17a3f-328">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="17a3f-329">Lägg till stöd för att konfigurera TopLevel WebApplicationFirewall-princip</span><span class="sxs-lookup"><span data-stu-id="17a3f-329">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="17a3f-330">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="17a3f-330">New cmdlets added:</span></span>
        - <span data-ttu-id="17a3f-331">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="17a3f-331">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="17a3f-332">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="17a3f-332">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="17a3f-333">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="17a3f-333">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="17a3f-334">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="17a3f-334">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="17a3f-335">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="17a3f-335">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="17a3f-336">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="17a3f-336">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="17a3f-337">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="17a3f-337">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="17a3f-338">New-AzApplicationGatewayFirewallPolicy: parametrarna PolicySetting, ManagedRule har lagts till</span><span class="sxs-lookup"><span data-stu-id="17a3f-338">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="17a3f-339">Stöd för operator för geomatchning har lagts till på CustomRule</span><span class="sxs-lookup"><span data-stu-id="17a3f-339">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="17a3f-340">Geomatchning har lagts till i operatorn på FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="17a3f-340">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="17a3f-341">Stöd har lagts till för brandväggsprinciperna perListener och perSite</span><span class="sxs-lookup"><span data-stu-id="17a3f-341">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="17a3f-342">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="17a3f-342">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="17a3f-343">New-AzApplicationGatewayHttpListener: parametrarna FirewallPolicy, FirewallPolicyId har lagts till</span><span class="sxs-lookup"><span data-stu-id="17a3f-343">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="17a3f-344">New-AzApplicationGatewayPathRuleConfig: parametrarna FirewallPolicy, FirewallPolicyId har lagts till</span><span class="sxs-lookup"><span data-stu-id="17a3f-344">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="17a3f-345">Åtgärdat så att nödvändigt undernät med namnet AzureBastionSubnet i PSBastion kan vara skiftlägesokänsligt</span><span class="sxs-lookup"><span data-stu-id="17a3f-345">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="17a3f-346">Stöd för mål-FQDN:er i nätverksregler och översatt FQDN i NAT-regler för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="17a3f-346">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="17a3f-347">Lägg till stöd för resursen RouteTables för IpGroup på den högsta nivån</span><span class="sxs-lookup"><span data-stu-id="17a3f-347">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="17a3f-348">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="17a3f-348">New cmdlets added:</span></span>
        - <span data-ttu-id="17a3f-349">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="17a3f-349">New-AzIpGroup</span></span>
        - <span data-ttu-id="17a3f-350">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="17a3f-350">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="17a3f-351">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="17a3f-351">Get-AzIpGroup</span></span>
        - <span data-ttu-id="17a3f-352">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="17a3f-352">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="17a3f-353">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="17a3f-353">Az.ServiceFabric</span></span>
* <span data-ttu-id="17a3f-354">Ta bort cmdleten Add-AzServiceFabricApplicationCertificate eftersom det här scenariot omfattas av Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="17a3f-354">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="17a3f-355">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="17a3f-355">Az.Sql</span></span>
* <span data-ttu-id="17a3f-356">Stöd har lagts till för återställning av utelämnade databaser på hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="17a3f-356">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="17a3f-357">Inaktuella gamla cmdletar för granskning från kod.</span><span class="sxs-lookup"><span data-stu-id="17a3f-357">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="17a3f-358">Tog bort inaktuella alias:</span><span class="sxs-lookup"><span data-stu-id="17a3f-358">Removed deprecated aliases:</span></span>
* <span data-ttu-id="17a3f-359">Get-AzSqlDatabaseIndexRecommendations (använd Get-AzSqlDatabaseIndexRecommendation istället)</span><span class="sxs-lookup"><span data-stu-id="17a3f-359">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="17a3f-360">Get-AzSqlDatabaseRestorePoints (använd Get-AzSqlDatabaseRestorePoint istället)</span><span class="sxs-lookup"><span data-stu-id="17a3f-360">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="17a3f-361">Ta bort cmdleten Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="17a3f-361">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="17a3f-362">Ta bort alias för inaktuella cmdletar för inställningar för utvärdering av säkerhetsrisk</span><span class="sxs-lookup"><span data-stu-id="17a3f-362">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="17a3f-363">Inaktualisera cmdletar för inställningar för avancerad hotidentifiering</span><span class="sxs-lookup"><span data-stu-id="17a3f-363">Deprecate Advanced Threat Detection Settings cmdlets</span></span> 
* <span data-ttu-id="17a3f-364">Lägga till cmdletar för att inaktivera och aktivera känslighetsrekommendationer på kolumner i en databas.</span><span class="sxs-lookup"><span data-stu-id="17a3f-364">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="17a3f-365">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="17a3f-365">Az.Storage</span></span>
* <span data-ttu-id="17a3f-366">Stöd för att aktivera stora filresurser vid skapande eller uppdatering av lagringskonto</span><span class="sxs-lookup"><span data-stu-id="17a3f-366">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="17a3f-367">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="17a3f-367">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="17a3f-368">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="17a3f-368">Set-AzStorageAccount</span></span>
* <span data-ttu-id="17a3f-369">När du stänger/hämtar en filreferens kan du hoppa över kontrollen av huruvida indatasökvägen är en filkatalog eller en fil för att undvika problem med objekt som har status DeletePending</span><span class="sxs-lookup"><span data-stu-id="17a3f-369">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="17a3f-370">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="17a3f-370">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="17a3f-371">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="17a3f-371">Close-AzStorageFileHandle</span></span>
    
## <a name="280---october-2019"></a><span data-ttu-id="17a3f-372">2.8.0 – oktober 2019</span><span class="sxs-lookup"><span data-stu-id="17a3f-372">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="17a3f-373">Allmänt</span><span class="sxs-lookup"><span data-stu-id="17a3f-373">General</span></span>
* <span data-ttu-id="17a3f-374">AZ. HealthcareApis 1.0.0-version</span><span class="sxs-lookup"><span data-stu-id="17a3f-374">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="17a3f-375">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="17a3f-375">Az.Accounts</span></span>
* <span data-ttu-id="17a3f-376">Uppdatera telemetri och URL-omskrivning för genererade moduler, korrigera Windows-enhetstester.</span><span class="sxs-lookup"><span data-stu-id="17a3f-376">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="17a3f-377">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="17a3f-377">Az.ApiManagement</span></span>
* <span data-ttu-id="17a3f-378">**Set-AzApiManagementApi** – Tillagt stöd för att uppdatera Api till ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="17a3f-378">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="17a3f-379">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="17a3f-379">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="17a3f-380">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="17a3f-380">Az.Automation</span></span>
* <span data-ttu-id="17a3f-381">Åtgärdade cmdleten New-AzureAutomationSoftwareUpdateConfiguration för parametern för inställning av Linux-omstart.</span><span class="sxs-lookup"><span data-stu-id="17a3f-381">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="17a3f-382">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="17a3f-382">Az.Batch</span></span>
* <span data-ttu-id="17a3f-383">**Get-AzBatchNodeAgentSku** är inaktuell och ersätts av **Get-AzBatchSupportImage** i version 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="17a3f-383">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="17a3f-384">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="17a3f-384">Az.Compute</span></span>
* <span data-ttu-id="17a3f-385">Lägg till parametrarna Priority, EvictionPolicy och MaxPrice till cmdletarna New-AzVM och New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="17a3f-385">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="17a3f-386">Korrigera varningsmeddelande och hjälpdokument för cmdletarna Add-AzVMAdditionalUnattendContent och Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="17a3f-386">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="17a3f-387">Åtgärda – skipVmBackup-undantag för virtuella Linux-datorer med hanterade diskar för Set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="17a3f-387">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="17a3f-388">Åtgärda fel i uppdatera krypteringsinställningarna i set-AzVMDiskEncryptionExtension, scenario i två steg.</span><span class="sxs-lookup"><span data-stu-id="17a3f-388">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="17a3f-389">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="17a3f-389">Az.DataFactory</span></span>
* <span data-ttu-id="17a3f-390">Lägga till CRUD-kommandon för ADF V2-dataflödet: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow och Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="17a3f-390">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="17a3f-391">Lägger till åtgärdskommandon för ADF V2-dataflödesfelsökningssession: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand och Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="17a3f-391">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="17a3f-392">Uppdatera ADF .Net SDK-versionen till 4.2.0</span><span class="sxs-lookup"><span data-stu-id="17a3f-392">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="17a3f-393">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="17a3f-393">Az.DataLakeStore</span></span>
* <span data-ttu-id="17a3f-394">Korrigera kontovalidering så att konton med ”-” kan skickas utan domän</span><span class="sxs-lookup"><span data-stu-id="17a3f-394">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="17a3f-395">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="17a3f-395">Az.HealthcareApis</span></span>
* <span data-ttu-id="17a3f-396">PowerShell-versionen har uppdaterats till 1.0.0</span><span class="sxs-lookup"><span data-stu-id="17a3f-396">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="17a3f-397">Uppdaterade SDK-versionen till 1.0.2</span><span class="sxs-lookup"><span data-stu-id="17a3f-397">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="17a3f-398">Uppdatera i tester för att referera till en ny SDK-version</span><span class="sxs-lookup"><span data-stu-id="17a3f-398">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="17a3f-399">Utdatastrukturen har uppdaterats från kapslad till förenklad.</span><span class="sxs-lookup"><span data-stu-id="17a3f-399">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="17a3f-400">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="17a3f-400">Az.IotHub</span></span>
* <span data-ttu-id="17a3f-401">Lägg till ny routningskälla: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="17a3f-401">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="17a3f-402">Mindre felkorrigering: Get-AzIothub returnerar inte subscriptionId</span><span class="sxs-lookup"><span data-stu-id="17a3f-402">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="17a3f-403">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="17a3f-403">Az.Monitor</span></span>
* <span data-ttu-id="17a3f-404">Nya åtgärdsgruppsmottagare har lagts till för åtgärdsgrupp   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="17a3f-404">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="17a3f-405">Använd vanligt aviseringsschema som är aktiverat för mottagarna.</span><span class="sxs-lookup"><span data-stu-id="17a3f-405">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="17a3f-406">Detta gäller inte för SMS, push för Azure-app, ITSM och röstmottagare</span><span class="sxs-lookup"><span data-stu-id="17a3f-406">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="17a3f-407">Webhooks har nu stöd för Azure Active Directory-autentisering.</span><span class="sxs-lookup"><span data-stu-id="17a3f-407">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="17a3f-408">Az.Network</span><span class="sxs-lookup"><span data-stu-id="17a3f-408">Az.Network</span></span>
* <span data-ttu-id="17a3f-409">Lägg till ny cmdlet Get-AzAvailableServiceAlias som kan anropas för att hämta de alias som kan användas för tjänstslutpunktsprinciper.</span><span class="sxs-lookup"><span data-stu-id="17a3f-409">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="17a3f-410">Stöd för tillägg av trafikväljare har lagts till i gatewayanslutningar för virtuella nätverk</span><span class="sxs-lookup"><span data-stu-id="17a3f-410">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="17a3f-411">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="17a3f-411">New cmdlets added:</span></span>
        - <span data-ttu-id="17a3f-412">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="17a3f-412">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="17a3f-413">Cmdletar har uppdaterats med valfri parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="17a3f-413">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="17a3f-414">Lägg till stöd för ESP- och AH-protokoll i konfiguration av nätverkssäkerhetsregler</span><span class="sxs-lookup"><span data-stu-id="17a3f-414">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="17a3f-415">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="17a3f-415">Updated cmdlets:</span></span>
        - <span data-ttu-id="17a3f-416">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="17a3f-416">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="17a3f-417">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="17a3f-417">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="17a3f-418">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="17a3f-418">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="17a3f-419">Förbättra hanteringen av undantag i Cortex-cmdletar</span><span class="sxs-lookup"><span data-stu-id="17a3f-419">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="17a3f-420">Nya generationer och SKU:er för VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="17a3f-420">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="17a3f-421">Introducera nya generationer för VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="17a3f-421">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="17a3f-422">Introducera nya SKU:er med högt dataflöde för VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="17a3f-422">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="17a3f-423">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="17a3f-423">Az.RedisCache</span></span>
* <span data-ttu-id="17a3f-424">Uppdaterad referensdokumentation för ”set-AzRedisCache” för att inkludera saknade värden för parametern ”size”</span><span class="sxs-lookup"><span data-stu-id="17a3f-424">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="17a3f-425">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="17a3f-425">Az.Sql</span></span>
* <span data-ttu-id="17a3f-426">Lägg till stöd för inställningen Active Directory administratör på den hanterade instansen</span><span class="sxs-lookup"><span data-stu-id="17a3f-426">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="17a3f-427">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="17a3f-427">Az.Storage</span></span>
* <span data-ttu-id="17a3f-428">Uppdatera Lagringsklientbibliotek till 11.1.0</span><span class="sxs-lookup"><span data-stu-id="17a3f-428">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="17a3f-429">Lista containrar med hanteringsplans-API, kommer att listas med NextPageLink</span><span class="sxs-lookup"><span data-stu-id="17a3f-429">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="17a3f-430">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="17a3f-430">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="17a3f-431">Lista lagringskonton från prenumerationen, kommer att listas med NextPageLink</span><span class="sxs-lookup"><span data-stu-id="17a3f-431">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="17a3f-432">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="17a3f-432">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="17a3f-433">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="17a3f-433">Az.StorageSync</span></span>
* <span data-ttu-id="17a3f-434">Åtgärda problemet 9810 i Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="17a3f-434">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="17a3f-435">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="17a3f-435">Az.Websites</span></span>
* <span data-ttu-id="17a3f-436">Set-AzWebApp – uppdatering av ASP för en app misslyckades</span><span class="sxs-lookup"><span data-stu-id="17a3f-436">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="17a3f-437">2.7.0 – september 2019</span><span class="sxs-lookup"><span data-stu-id="17a3f-437">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="17a3f-438">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="17a3f-438">Az.ApiManagement</span></span>
* <span data-ttu-id="17a3f-439">Uppdatera ”-Format”-parameterbeskrivningen i ”Set-AzApiManagementPolicy”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="17a3f-439">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="17a3f-440">Referenser för den föråldrade cmdleten ”Update-AzApiManagementDeployment” har tagits bort från referensdokumentationen.</span><span class="sxs-lookup"><span data-stu-id="17a3f-440">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="17a3f-441">Använd ”Set-AzApiManagement” i stället.</span><span class="sxs-lookup"><span data-stu-id="17a3f-441">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="17a3f-442">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="17a3f-442">Az.Automation</span></span>
* <span data-ttu-id="17a3f-443">Stavfel har korrigerats i exempel i referensdokumentationen för ”Register-AzAutomationDscNode”</span><span class="sxs-lookup"><span data-stu-id="17a3f-443">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="17a3f-444">Klargörande har lagts till om OS-begränsningar för Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="17a3f-444">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="17a3f-445">Null-referensundantag har korrigerats för -Wait-alternativet i Start-AzAutomationRunbook-cmdleten.</span><span class="sxs-lookup"><span data-stu-id="17a3f-445">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="17a3f-446">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="17a3f-446">Az.Compute</span></span>
* <span data-ttu-id="17a3f-447">Lägg till UploadSizeInBytes-parameter till New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="17a3f-447">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="17a3f-448">Lägg till Incremental-parameter till New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="17a3f-448">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="17a3f-449">Lägg till en funktion för virtuella datorer med låg prioritet:</span><span class="sxs-lookup"><span data-stu-id="17a3f-449">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="17a3f-450">MaxPrice-, EvictionPolicy- och Priority-parametrar har lagts till i New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="17a3f-450">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="17a3f-451">MaxPrice-parametern har lagts till i New-AzVmssConfig-, Update-AzVM- och Update-AzVmss-cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="17a3f-451">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="17a3f-452">Åtgärda problem med VM-referenser för Get-AzAvailabilitySet-cmdleten när alla tillgänglighetsuppsättningar i prenumerationen visas.</span><span class="sxs-lookup"><span data-stu-id="17a3f-452">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="17a3f-453">Korrigera null-undantaget för Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="17a3f-453">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="17a3f-454">Korrigera VHD-metoden för sökning relativt till slut.</span><span class="sxs-lookup"><span data-stu-id="17a3f-454">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="17a3f-455">Åtgärda UltraSSD-problem för New-AzVM och Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="17a3f-455">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="17a3f-456">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="17a3f-456">Az.DataFactory</span></span>
* <span data-ttu-id="17a3f-457">Lägger till 3 nya kommandon för ADF V2 – Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription och Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="17a3f-457">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="17a3f-458">ADF .Net SDK har uppdaterats till 4.1.3</span><span class="sxs-lookup"><span data-stu-id="17a3f-458">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="17a3f-459">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="17a3f-459">Az.HDInsight</span></span>
* <span data-ttu-id="17a3f-460">Anrop för icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="17a3f-460">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="17a3f-461">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="17a3f-461">Az.IotHub</span></span>
* <span data-ttu-id="17a3f-462">Lägg till stöd för att anropa redundans för en IotHub till den geo-länkade katastrofåterställningsregionen.</span><span class="sxs-lookup"><span data-stu-id="17a3f-462">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="17a3f-463">Lägg till stöd för att hantera meddelandeberikning för en IotHub.</span><span class="sxs-lookup"><span data-stu-id="17a3f-463">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="17a3f-464">Nya cmdlet:ar är:</span><span class="sxs-lookup"><span data-stu-id="17a3f-464">New cmdlets are:</span></span>
    - <span data-ttu-id="17a3f-465">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="17a3f-465">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="17a3f-466">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="17a3f-466">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="17a3f-467">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="17a3f-467">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="17a3f-468">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="17a3f-468">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="17a3f-469">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="17a3f-469">Az.Monitor</span></span>
* <span data-ttu-id="17a3f-470">Pekar på den senaste Monitor SDK:n, dvs. 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="17a3f-470">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="17a3f-471">Lägger till bakåtkompatibla ändringar i Metrics-cmdletarna, dvs. enhetsuppräkningen stöder flera nya värden.</span><span class="sxs-lookup"><span data-stu-id="17a3f-471">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="17a3f-472">Detta är skrivskyddade cmdletar, så det förekommer inga ändringar i inmatningen för cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="17a3f-472">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="17a3f-473">API-versionen för **ActionGroups**-begäranden är nu **2019-06-01**. Tidigare var den **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="17a3f-473">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="17a3f-474">Test av scenarier har uppdaterats för att anpassas till den här ändringen.</span><span class="sxs-lookup"><span data-stu-id="17a3f-474">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="17a3f-475">Ett nytt obligatoriskt argument har lagts till för konstruktorerna för klasserna **EmailReceiver** och **WebhookReceiver** – ett booleskt värde med namnet **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="17a3f-475">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="17a3f-476">Värdet är för närvarande fast till **false** så att den här icke-bakåtkompatibla ändringen är dold från cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="17a3f-476">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="17a3f-477">**Obs!** Det här är en tillfällig ändring som måste verifieras av Alerts-teamet.</span><span class="sxs-lookup"><span data-stu-id="17a3f-477">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="17a3f-478">Ordningen på argumenten för konstruktorn för klassen **Source** (relaterad till klassen **ScheduledQueryRuleSource**) har ändrats från den tidigare SDK:n.</span><span class="sxs-lookup"><span data-stu-id="17a3f-478">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="17a3f-479">Den här ändringen krävde korrigering av två enhetstest: de kompilerades, men testerna skickades inte.</span><span class="sxs-lookup"><span data-stu-id="17a3f-479">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="17a3f-480">Ordningen på argumenten för konstruktorn för klassen **AlertingAction** (relaterad till klassen **ScheduledQueryRuleSource**) har ändrats från den tidigare SDK:n.</span><span class="sxs-lookup"><span data-stu-id="17a3f-480">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="17a3f-481">Den här ändringen krävde korrigering av två enhetstest: de kompilerades, men testerna skickades inte.</span><span class="sxs-lookup"><span data-stu-id="17a3f-481">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="17a3f-482">Stöd för kriterier för dynamiskt tröskelvärde för måttavisering v2</span><span class="sxs-lookup"><span data-stu-id="17a3f-482">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="17a3f-483">New-AzMetricAlertRuleV2Criteria: skapar nu även kriterier för dynamiskt tröskelvärde</span><span class="sxs-lookup"><span data-stu-id="17a3f-483">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="17a3f-484">Add-AzMetricAlertRuleV2: accepterar nu även kriterier för dynamiskt tröskelvärde</span><span class="sxs-lookup"><span data-stu-id="17a3f-484">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="17a3f-485">Förbättringar i schemalagd frågeregel (SQR)</span><span class="sxs-lookup"><span data-stu-id="17a3f-485">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="17a3f-486">Cmdletar accepterar ”Location”-parameter i båda formaten, antingen platsen (t.ex. eastus) eller platsens visningsnamn (t.ex. USA, östra)</span><span class="sxs-lookup"><span data-stu-id="17a3f-486">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="17a3f-487">”Enabled”-parametern illustreras korrekt i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="17a3f-487">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="17a3f-488">Exempel för den valfria parametern ”ActionGroup” har lagts till</span><span class="sxs-lookup"><span data-stu-id="17a3f-488">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="17a3f-489">Förbättrade hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="17a3f-489">Overall improved help files</span></span>
* <span data-ttu-id="17a3f-490">Åtgärda bugg då omfattningstypen fastställs för ”Set-AzActionRule”</span><span class="sxs-lookup"><span data-stu-id="17a3f-490">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="17a3f-491">Az.Network</span><span class="sxs-lookup"><span data-stu-id="17a3f-491">Az.Network</span></span>
* <span data-ttu-id="17a3f-492">Korrigera felaktigt exempel i referensdokumentationen för ”New-AzApplicationGateway”</span><span class="sxs-lookup"><span data-stu-id="17a3f-492">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="17a3f-493">Lägg till anmärkning i ”Get-AzNetworkWatcherPacketCapture”-referensdokumentationen om hämtning av alla egenskaper för en paketinsamling</span><span class="sxs-lookup"><span data-stu-id="17a3f-493">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="17a3f-494">Exempel har korrigerats i ”Test-AzNetworkWatcherIPFlow”-referensdokumentationen för korrekt uppräkning av nätverkskort</span><span class="sxs-lookup"><span data-stu-id="17a3f-494">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="17a3f-495">Förbättrad tolkning av molnundantag för att visa eventuell ytterligare information</span><span class="sxs-lookup"><span data-stu-id="17a3f-495">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="17a3f-496">Förbättrad tolkning av molnundantag för att hantera ytterligare en typ av SDK-undantag</span><span class="sxs-lookup"><span data-stu-id="17a3f-496">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="17a3f-497">Felaktig mappning av säkerhetsregelmodeller har korrigerats</span><span class="sxs-lookup"><span data-stu-id="17a3f-497">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="17a3f-498">Egenskaper har lagts till för nätverksgränssnittet för funktionen Privat IP</span><span class="sxs-lookup"><span data-stu-id="17a3f-498">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="17a3f-499">Egenskapen ”PrivateEndpoint” har lagts till som en typ av PSResourceId till PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="17a3f-499">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="17a3f-500">Egenskapen ”PrivateLinkConnectionProperties” har lagts till som en typ av PSIpConfigurationConnectivityInformation till PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="17a3f-500">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="17a3f-501">Modellklassen PSIpConfigurationConnectivityInformation har lagts till</span><span class="sxs-lookup"><span data-stu-id="17a3f-501">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="17a3f-502">ApplicationRuleProtocolType ”mssql” har lagts till för Azure Firewall-resurs</span><span class="sxs-lookup"><span data-stu-id="17a3f-502">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="17a3f-503">MultiLink-stöd i virtuellt WAN</span><span class="sxs-lookup"><span data-stu-id="17a3f-503">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="17a3f-504">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="17a3f-504">New cmdlets</span></span>
        - <span data-ttu-id="17a3f-505">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="17a3f-505">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="17a3f-506">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="17a3f-506">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="17a3f-507">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="17a3f-507">Updated cmdlet:</span></span>
        - <span data-ttu-id="17a3f-508">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="17a3f-508">New-VpnSite</span></span>
        - <span data-ttu-id="17a3f-509">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="17a3f-509">Update-VpnSite</span></span>
        - <span data-ttu-id="17a3f-510">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="17a3f-510">New-VpnConnection</span></span>
        - <span data-ttu-id="17a3f-511">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="17a3f-511">Update-VpnConnection</span></span>
* <span data-ttu-id="17a3f-512">Dokument för vissa PowerShell-exempel har korrigerats så att Az-cmdletar används i stället för AzureRM-cmdletar</span><span class="sxs-lookup"><span data-stu-id="17a3f-512">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="17a3f-513">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="17a3f-513">Az.RecoveryServices</span></span>
* <span data-ttu-id="17a3f-514">Uppdatera AzureVMpolicy-objekt med ProtectedItemsCount-attribut</span><span class="sxs-lookup"><span data-stu-id="17a3f-514">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="17a3f-515">Ytterligare tester har lagts till för VM-princip och återställning av ursprungligt lagringskonto</span><span class="sxs-lookup"><span data-stu-id="17a3f-515">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="17a3f-516">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="17a3f-516">Az.Resources</span></span>
* <span data-ttu-id="17a3f-517">Åtgärda fel där det inte gick att anropa New-AzRoleAssignment utan parametern Scope.</span><span class="sxs-lookup"><span data-stu-id="17a3f-517">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="17a3f-518">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="17a3f-518">Az.ServiceFabric</span></span>
* <span data-ttu-id="17a3f-519">Stavfel har korrigerats i exempel för ”Update-AzServiceFabricReliability”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="17a3f-519">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="17a3f-520">Lägger till nya cmdletar för att hantera program och tjänster:</span><span class="sxs-lookup"><span data-stu-id="17a3f-520">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="17a3f-521">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="17a3f-521">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="17a3f-522">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="17a3f-522">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="17a3f-523">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="17a3f-523">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="17a3f-524">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="17a3f-524">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="17a3f-525">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="17a3f-525">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="17a3f-526">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="17a3f-526">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="17a3f-527">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="17a3f-527">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="17a3f-528">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="17a3f-528">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="17a3f-529">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="17a3f-529">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="17a3f-530">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="17a3f-530">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="17a3f-531">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="17a3f-531">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="17a3f-532">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="17a3f-532">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="17a3f-533">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="17a3f-533">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="17a3f-534">Service Fabric SDK har uppgraderats till version 1.2.0 som använder Service Fabric-resursprovidern med API-version 2019-03-01.</span><span class="sxs-lookup"><span data-stu-id="17a3f-534">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="17a3f-535">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="17a3f-535">Az.SignalR</span></span>
* <span data-ttu-id="17a3f-536">Lägg till Update-, Restart-, CheckNameAvailability- och GetUsage-cmdletar</span><span class="sxs-lookup"><span data-stu-id="17a3f-536">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="17a3f-537">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="17a3f-537">Az.Sql</span></span>
* <span data-ttu-id="17a3f-538">Uppdatera exempel i referensdokumentationen för ”Get-AzSqlElasticPool”</span><span class="sxs-lookup"><span data-stu-id="17a3f-538">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="17a3f-539">vCore-exempel för att skapa en elastisk pool (New-AzSqlElasticPool) har lagts till.</span><span class="sxs-lookup"><span data-stu-id="17a3f-539">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="17a3f-540">Ta bort verifieringen av EmailAddresses och kontrollen som bekräftar att EmailAdmins inte är falskt när EmailAddresses är tomt i Set-AzSqlServerAdvancedThreatProtectionPolicy och Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="17a3f-540">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="17a3f-541">Server-/databasgranskningsinställningar kan tas bort när det finns flera diagnostikinställningar som aktiverar granskningskategorin.</span><span class="sxs-lookup"><span data-stu-id="17a3f-541">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="17a3f-542">Åtgärda verifiering av e-postadresser i flera Sql Vulnerability Assessment-cmdletar (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting och Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="17a3f-542">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="17a3f-543">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="17a3f-543">Az.Storage</span></span>
* <span data-ttu-id="17a3f-544">Exempel i referensdokumentationen för ”Get-AzStorageAccountKey” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="17a3f-544">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="17a3f-545">Vid upp- och nedladdning av en Azure-fil kan SMB-egenskaperna för källfilen (t.ex. filattribut, tidpunkten då filen skapades och tidpunkten för den senaste skrivningen) sparas i målfilen</span><span class="sxs-lookup"><span data-stu-id="17a3f-545">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="17a3f-546">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="17a3f-546">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="17a3f-547">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="17a3f-547">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="17a3f-548">Korrigera problem med uppladdningen av blockblob med egenskaper/metadata för ImmutabilityPolicy i containrar.</span><span class="sxs-lookup"><span data-stu-id="17a3f-548">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="17a3f-549">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="17a3f-549">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="17a3f-550">Stöd för hantering av Azure-filresurser med API för hanteringsplan</span><span class="sxs-lookup"><span data-stu-id="17a3f-550">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="17a3f-551">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="17a3f-551">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="17a3f-552">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="17a3f-552">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="17a3f-553">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="17a3f-553">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="17a3f-554">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="17a3f-554">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="17a3f-555">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="17a3f-555">Az.Websites</span></span>
* <span data-ttu-id="17a3f-556">Åtgärdar problemet där webapp-taggar togs bort när appen migrerades till nya ASP</span><span class="sxs-lookup"><span data-stu-id="17a3f-556">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="17a3f-557">Åtgärda Publish-AzureWebapp så att det fungerar i Linux och Windows</span><span class="sxs-lookup"><span data-stu-id="17a3f-557">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="17a3f-558">Uppdatera exempel i ”Get-AzWebAppPublishingProfile”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="17a3f-558">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="17a3f-559">2.6.0 – augusti 2019</span><span class="sxs-lookup"><span data-stu-id="17a3f-559">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="17a3f-560">Allmänt</span><span class="sxs-lookup"><span data-stu-id="17a3f-560">General</span></span>
* <span data-ttu-id="17a3f-561">Åtgärdade diverse skrivfel i flera moduler</span><span class="sxs-lookup"><span data-stu-id="17a3f-561">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="17a3f-562">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="17a3f-562">Az.Accounts</span></span>
* <span data-ttu-id="17a3f-563">Stöd för användartilldelat MSI i Azure Functions-autentisering (#9479)</span><span class="sxs-lookup"><span data-stu-id="17a3f-563">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="17a3f-564">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="17a3f-564">Az.Aks</span></span>
* <span data-ttu-id="17a3f-565">Åtgärda problem med utdata för "Get-AzAks"</span><span class="sxs-lookup"><span data-stu-id="17a3f-565">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="17a3f-566">Mer information här: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="17a3f-566">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="17a3f-567">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="17a3f-567">Az.ApiManagement</span></span>
* <span data-ttu-id="17a3f-568">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="17a3f-568">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="17a3f-569">Uppdatera .net-NuGet-versionen, som inte tillämpar begränsningar för productId, apiId och userId</span><span class="sxs-lookup"><span data-stu-id="17a3f-569">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="17a3f-570">**Get-AzApiManagementProduct** – Lade till stöd för frågekörning mot produkter via API.</span><span class="sxs-lookup"><span data-stu-id="17a3f-570">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="17a3f-571">**New-AzApiManagementApiRevision** – Korrigering för problem där ApiRevisionDescription inte angavs vid skapande av ny API-revision https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="17a3f-571">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="17a3f-572">Åtgärdade skrivfel i modellen "PsApiManagementOAuth2AuthrozationServer" till "PsApiManagementOAuth2AuthorizationServer"</span><span class="sxs-lookup"><span data-stu-id="17a3f-572">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="17a3f-573">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="17a3f-573">Az.Batch</span></span>
* <span data-ttu-id="17a3f-574">Åtgärdade skrivfel i hjälpmeddelande och dokumentation till att skriva Windows med versaler</span><span class="sxs-lookup"><span data-stu-id="17a3f-574">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="17a3f-575">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="17a3f-575">Az.Cdn</span></span>
* <span data-ttu-id="17a3f-576">Åtgärdade skrivfel i CDN-modulens konverteringshjälp</span><span class="sxs-lookup"><span data-stu-id="17a3f-576">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="17a3f-577">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="17a3f-577">Az.Compute</span></span>
* <span data-ttu-id="17a3f-578">Lägg till VmssId i New-AzVMConfig-cmdleten</span><span class="sxs-lookup"><span data-stu-id="17a3f-578">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="17a3f-579">Lägg till parametrarna TerminateScheduledEvents och TerminateScheduledEventNotBeforeTimeoutInMinutes i New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="17a3f-579">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="17a3f-580">Lägg till egenskapen HyperVGeneration till avbildningsobjekt för virtuell dator</span><span class="sxs-lookup"><span data-stu-id="17a3f-580">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="17a3f-581">Lägg till funktioner för Host och HostGroup</span><span class="sxs-lookup"><span data-stu-id="17a3f-581">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="17a3f-582">Nya cmdletar:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="17a3f-582">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="17a3f-583">HostId-parametern läggs till i New-AzVMConfig och New-AzVM</span><span class="sxs-lookup"><span data-stu-id="17a3f-583">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="17a3f-584">Uppdatera exempel i "Invoke-AzVMRunCommand"-dokumentationen till att använda rätt parameternamn</span><span class="sxs-lookup"><span data-stu-id="17a3f-584">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="17a3f-585">Uppdatera "-VolumeType"-beskrivningen i referensdokumentationen för "set-AzVMDiskEncryptionExtension" och "set-AzVmssDiskEncryptionExtension"</span><span class="sxs-lookup"><span data-stu-id="17a3f-585">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="17a3f-586">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="17a3f-586">Az.DataFactory</span></span>
* <span data-ttu-id="17a3f-587">Åtgärda skrivfel till att använda versaler för "Windows" i "New-AzDataFactoryEncryptValue"-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="17a3f-587">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="17a3f-588">Uppdaterade ADF .Net SDK-versionen till 4.1.2</span><span class="sxs-lookup"><span data-stu-id="17a3f-588">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="17a3f-589">Lägg till parametrarna "DataProxyIntegrationRuntimeName", "DataProxyStagingLinkedServiceName" och "DataProxyStagingPath" för "Set-AzureRmDataFactoryV2IntegrationRuntime"-cmd för att aktivera konfiguration av lokalt installerad integrationskörning som en proxy för SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="17a3f-589">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="17a3f-590">Uppdaterade PSTriggerRun till att visa utlöst pipeline, meddelande och egenskaper samt PSActivityRun till att visa aktivitetstypen</span><span class="sxs-lookup"><span data-stu-id="17a3f-590">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="17a3f-591">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="17a3f-591">Az.DataLakeStore</span></span>
* <span data-ttu-id="17a3f-592">Korrigering av frysning av Get-DataLakeStoreDeletedItem för fel eller fjärrundantag.</span><span class="sxs-lookup"><span data-stu-id="17a3f-592">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="17a3f-593">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="17a3f-593">Az.EventHub</span></span>
* <span data-ttu-id="17a3f-594">Korrigering av problem #9658 : Skrivfel i parametern VirtualNteworkRule i Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="17a3f-594">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="17a3f-595">Korrigering av problem #9558 : Set-AzEventHubNamespace använder PATCH i stället för PUT</span><span class="sxs-lookup"><span data-stu-id="17a3f-595">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="17a3f-596">lade till parametern EnableKafka i Set-AzEventHubNamespace-cmdleten</span><span class="sxs-lookup"><span data-stu-id="17a3f-596">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="17a3f-597">Korrigering av problem #9786 : kan inte skapa en regel med Endast lyssna-behörighet</span><span class="sxs-lookup"><span data-stu-id="17a3f-597">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="17a3f-598">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="17a3f-598">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="17a3f-599">Åtgärdade skrivfel i dokumentation där "Azure" skrevs helt med gemener</span><span class="sxs-lookup"><span data-stu-id="17a3f-599">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="17a3f-600">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="17a3f-600">Az.Monitor</span></span>
* <span data-ttu-id="17a3f-601">Åtgärdade felaktigt parameternamn i hjälpdokumentationen</span><span class="sxs-lookup"><span data-stu-id="17a3f-601">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="17a3f-602">Az.Network</span><span class="sxs-lookup"><span data-stu-id="17a3f-602">Az.Network</span></span>
* <span data-ttu-id="17a3f-603">Uppdaterade New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="17a3f-603">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="17a3f-604">Gjorde parametern "PublicIpAddress" inaktuell eftersom den aldrig används på serversidan.</span><span class="sxs-lookup"><span data-stu-id="17a3f-604">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="17a3f-605">Lade till den valfria parametern "Primary", som anger huruvida den aktuella IP-konfigurationen är den primära.</span><span class="sxs-lookup"><span data-stu-id="17a3f-605">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="17a3f-606">Förbättrade hanteringen av felundantag för begärande från SDK – åtgärdar problemet att tidigare SDK-undantag inte hanteras på rätt sätt, vilket leder till att viktig felinformation inte visas</span><span class="sxs-lookup"><span data-stu-id="17a3f-606">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="17a3f-607">Justerade valideringslogiken för IPv6-IP-prefix till att kontrollera korrekt IPv6-prefixlängd.</span><span class="sxs-lookup"><span data-stu-id="17a3f-607">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="17a3f-608">Uppdaterade Get-AzVirtualNetworkSubnetConfig: Lade till parameter som anges till get av undernätets resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="17a3f-608">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="17a3f-609">Uppdaterade beskrivningen av parametern Location för AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="17a3f-609">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="17a3f-610">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="17a3f-610">Az.OperationalInsights</span></span>
* <span data-ttu-id="17a3f-611">Uppdaterade dokumentation för "New-AzOperationalInsightsLinuxSyslogDataSource"</span><span class="sxs-lookup"><span data-stu-id="17a3f-611">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="17a3f-612">Lade till exempel</span><span class="sxs-lookup"><span data-stu-id="17a3f-612">Added example</span></span>
    - <span data-ttu-id="17a3f-613">Uppdaterade beskrivningen av parametern "-Name"</span><span class="sxs-lookup"><span data-stu-id="17a3f-613">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="17a3f-614">Lade till ett exempel för New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="17a3f-614">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="17a3f-615">Ändrade beskrivningen av parametern -Name för New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="17a3f-615">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="17a3f-616">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="17a3f-616">Az.RecoveryServices</span></span>
* <span data-ttu-id="17a3f-617">Uppdatera "Get-AzRecoveryServicesBackupJobDetail.md"</span><span class="sxs-lookup"><span data-stu-id="17a3f-617">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="17a3f-618">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="17a3f-618">Az.Resources</span></span>
* <span data-ttu-id="17a3f-619">Lägg till stöd för den nya API-versionen från 2019-05-10 för Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="17a3f-619">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="17a3f-620">Lägg till stöd för "copy.count = 0" för variabler, resurser och egenskaper</span><span class="sxs-lookup"><span data-stu-id="17a3f-620">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="17a3f-621">Resurser med "condition = false" eller "copy.count = 0" tas bort i complete-läget</span><span class="sxs-lookup"><span data-stu-id="17a3f-621">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="17a3f-622">Lägg till ett exempel på tilldelning av princip på prenumerationsnivå i hjälpdokumentationen</span><span class="sxs-lookup"><span data-stu-id="17a3f-622">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="17a3f-623">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="17a3f-623">Az.ServiceBus</span></span>
* <span data-ttu-id="17a3f-624">Korrigering av problem #9658 : Skrivfel i parametern VirtualNetworkRule i set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="17a3f-624">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="17a3f-625">Korrigering av problem #9786 : kan inte skapa en regel med Endast lyssna-behörighet</span><span class="sxs-lookup"><span data-stu-id="17a3f-625">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="17a3f-626">Lade till det nya kommandot "Test-AzServiceBusNameAvailability" för att kontrollera namntillgängligheten för kö och ämne</span><span class="sxs-lookup"><span data-stu-id="17a3f-626">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="17a3f-627">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="17a3f-627">Az.ServiceFabric</span></span>
* <span data-ttu-id="17a3f-628">Åtgärda buggar med tillägg av nodtyps-cmdlet:</span><span class="sxs-lookup"><span data-stu-id="17a3f-628">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="17a3f-629">NullReferenceException-bugg när resursgrupp hade annan vmss som inte är relaterad till Service Fabric-klustret.</span><span class="sxs-lookup"><span data-stu-id="17a3f-629">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="17a3f-630">Åtgärdar problemet: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="17a3f-630">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="17a3f-631">Åtgärda bugg där cmdleten misslyckades om virtualNetwork var i en annan resursgrupp än klustret.</span><span class="sxs-lookup"><span data-stu-id="17a3f-631">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="17a3f-632">Åtgärdar problemet: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="17a3f-632">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="17a3f-633">AzServiceFabricApplicationCertificate-cmdleten görs inaktuell</span><span class="sxs-lookup"><span data-stu-id="17a3f-633">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="17a3f-634">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="17a3f-634">Az.Sql</span></span>
* <span data-ttu-id="17a3f-635">Uppdatera dokumentation om gamla gransknings-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="17a3f-635">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="17a3f-636">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="17a3f-636">Az.Storage</span></span>
* <span data-ttu-id="17a3f-637">Uppdatera hjälpen för Get/Close-AzStorageFileHandle genom att lägga till fler scenarier i cmdlet-exempel och uppdatera parameterbeskrivningar</span><span class="sxs-lookup"><span data-stu-id="17a3f-637">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="17a3f-638">Stöd för StandardBlobTier i uppladdningsblob och kopieringsblob</span><span class="sxs-lookup"><span data-stu-id="17a3f-638">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="17a3f-639">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="17a3f-639">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="17a3f-640">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="17a3f-640">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="17a3f-641">Stöd för rehydratiseringsprioritet i kopieringsblob</span><span class="sxs-lookup"><span data-stu-id="17a3f-641">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="17a3f-642">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="17a3f-642">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="17a3f-643">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="17a3f-643">Az.Websites</span></span>
* <span data-ttu-id="17a3f-644">Lägg till klargöranden gällande parametern -AppSettings i Set-AzWebApp och Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="17a3f-644">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="17a3f-645">2.5.0 – July 2019</span><span class="sxs-lookup"><span data-stu-id="17a3f-645">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="17a3f-646">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="17a3f-646">Az.Accounts</span></span>
* <span data-ttu-id="17a3f-647">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="17a3f-647">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="17a3f-648">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="17a3f-648">Az.ApplicationInsights</span></span>
* <span data-ttu-id="17a3f-649">Korrigera skrivfel i exempel i dokumentationen för Remove-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="17a3f-649">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="17a3f-650">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="17a3f-650">Az.Automation</span></span>
* <span data-ttu-id="17a3f-651">Korrigera skrivfel i resurssträng</span><span class="sxs-lookup"><span data-stu-id="17a3f-651">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="17a3f-652">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="17a3f-652">Az.CognitiveServices</span></span>
* <span data-ttu-id="17a3f-653">Stöd för NetworkRuleSet har lagts till.</span><span class="sxs-lookup"><span data-stu-id="17a3f-653">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="17a3f-654">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="17a3f-654">Az.Compute</span></span>
* <span data-ttu-id="17a3f-655">Lägg till saknade egenskaper (ComputerName, OsName, OsVersion och HyperVGeneration) för visningsobjekt i den virtuella datorinstansen.</span><span class="sxs-lookup"><span data-stu-id="17a3f-655">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="17a3f-656">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="17a3f-656">Az.ContainerRegistry</span></span>
* <span data-ttu-id="17a3f-657">Åtgärda skrivfel i Remove-AzContainerRegistryReplication för parametern Replication</span><span class="sxs-lookup"><span data-stu-id="17a3f-657">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="17a3f-658">Mer information finns här: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="17a3f-658">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="17a3f-659">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="17a3f-659">Az.DataFactory</span></span>
* <span data-ttu-id="17a3f-660">ADF .Net SDK-versionen har uppdaterats till 4.1.0</span><span class="sxs-lookup"><span data-stu-id="17a3f-660">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="17a3f-661">Korrigera skrivfel i dokumentationen för Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="17a3f-661">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="17a3f-662">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="17a3f-662">Az.EventHub</span></span>
* <span data-ttu-id="17a3f-663">Ny cmmdlet har lagts till för att skapa SAS-token: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="17a3f-663">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="17a3f-664">verifierings- och felmeddelande har lagts till för authorizationrules-rättigheter om endast "hantera" har tilldelats</span><span class="sxs-lookup"><span data-stu-id="17a3f-664">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="17a3f-665">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="17a3f-665">Az.KeyVault</span></span>
* <span data-ttu-id="17a3f-666">Stöd har lagts till för att ange KeySize för certifikatprinciper</span><span class="sxs-lookup"><span data-stu-id="17a3f-666">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="17a3f-667">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="17a3f-667">Az.LogicApp</span></span>
* <span data-ttu-id="17a3f-668">Korrigering för Get-AzIntegrationAccountMap för att lista alla mappningstyper</span><span class="sxs-lookup"><span data-stu-id="17a3f-668">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="17a3f-669">Ny MapType-parameter har lagts till för filtrering</span><span class="sxs-lookup"><span data-stu-id="17a3f-669">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="17a3f-670">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="17a3f-670">Az.ManagedServices</span></span>
* <span data-ttu-id="17a3f-671">Stöd för API-versionen 2019-06-01 (GA) har lagts till</span><span class="sxs-lookup"><span data-stu-id="17a3f-671">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="17a3f-672">Az.Network</span><span class="sxs-lookup"><span data-stu-id="17a3f-672">Az.Network</span></span>
* <span data-ttu-id="17a3f-673">Lägg till stöd för privat slutpunkt och privat länktjänst</span><span class="sxs-lookup"><span data-stu-id="17a3f-673">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="17a3f-674">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="17a3f-674">New cmdlets</span></span>
        - <span data-ttu-id="17a3f-675">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="17a3f-675">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="17a3f-676">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="17a3f-676">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="17a3f-677">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="17a3f-677">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="17a3f-678">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="17a3f-678">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="17a3f-679">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="17a3f-679">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="17a3f-680">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="17a3f-680">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="17a3f-681">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="17a3f-681">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="17a3f-682">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="17a3f-682">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="17a3f-683">Nedanstående kommandon för funktionen har uppdaterats: Flaggan PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies på undernätet i VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="17a3f-683">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="17a3f-684">Uppdaterade New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="17a3f-684">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="17a3f-685">Valfri parameter har lagts till – PrivateEndpointNetworkPoliciesFlag som konfigurerar huruvida nätverksprinciper ska tillämpas på en privat slutpunkt i det här undernätet.</span><span class="sxs-lookup"><span data-stu-id="17a3f-685">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="17a3f-686">Valfri parameter har lagts till – PrivateLinkServiceNetworkPoliciesFlag som konfigurerar huruvida nätverksprinciper ska tillämpas på en privat länktjänst i det här undernätet.</span><span class="sxs-lookup"><span data-stu-id="17a3f-686">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="17a3f-687">AzPrivateLinkService för cmdlet-parametern ServiceName har bytt namn till Name med aliaset ServiceName för bakåtkompatibilitet</span><span class="sxs-lookup"><span data-stu-id="17a3f-687">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="17a3f-688">Aktivera ICMP-protokoll för konfiguration av nätverkssäkerhetsregler</span><span class="sxs-lookup"><span data-stu-id="17a3f-688">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="17a3f-689">Uppdaterade cmdletar</span><span class="sxs-lookup"><span data-stu-id="17a3f-689">Updated cmdlets</span></span>
        - <span data-ttu-id="17a3f-690">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="17a3f-690">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="17a3f-691">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="17a3f-691">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="17a3f-692">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="17a3f-692">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="17a3f-693">Lägg till ConnectionProtocolType (Ikev1/Ikev2) som en konfigurerbar parameter för New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="17a3f-693">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="17a3f-694">Lägg till PrivateIpAddressVersion i LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="17a3f-694">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="17a3f-695">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="17a3f-695">Updated cmdlet:</span></span>
        - <span data-ttu-id="17a3f-696">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="17a3f-696">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="17a3f-697">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="17a3f-697">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="17a3f-698">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="17a3f-698">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="17a3f-699">Uppdatering av Application Gateway-kommandot New-AzApplicationGatewayProbeConfig för stöd av anpassad port i Probe</span><span class="sxs-lookup"><span data-stu-id="17a3f-699">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="17a3f-700">Uppdaterade New-AzApplicationGatewayProbeConfig: Den valfria parametern Port som används för avsökning i serverdelen har lagts till.</span><span class="sxs-lookup"><span data-stu-id="17a3f-700">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="17a3f-701">Denna parameter gäller för SKU:erna Standard_V2 och WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="17a3f-701">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="17a3f-702">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="17a3f-702">Az.OperationalInsights</span></span>
* <span data-ttu-id="17a3f-703">Uppdaterade standardversionen för sparade sökningar till 1.</span><span class="sxs-lookup"><span data-stu-id="17a3f-703">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="17a3f-704">Åtgärdade hantering av anpassad log null regex</span><span class="sxs-lookup"><span data-stu-id="17a3f-704">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="17a3f-705">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="17a3f-705">Az.RecoveryServices</span></span>
* <span data-ttu-id="17a3f-706">Uppdatera Get-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="17a3f-706">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="17a3f-707">Uppdatera Get-AzRecoveryServicesBackupContainer.md</span><span class="sxs-lookup"><span data-stu-id="17a3f-707">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="17a3f-708">Uppdatera Get-AzRecoveryServicesVault.md</span><span class="sxs-lookup"><span data-stu-id="17a3f-708">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="17a3f-709">Uppdatera Wait-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="17a3f-709">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="17a3f-710">Uppdatera Set-AzRecoveryServicesVaultContext.md</span><span class="sxs-lookup"><span data-stu-id="17a3f-710">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="17a3f-711">Uppdatera Get-AzRecoveryServicesBackupItem.md</span><span class="sxs-lookup"><span data-stu-id="17a3f-711">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="17a3f-712">Uppdatera Get-AzRecoveryServicesBackupRecoveryPoint.md</span><span class="sxs-lookup"><span data-stu-id="17a3f-712">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="17a3f-713">Uppdatera Restore-AzRecoveryServicesBackupItem.md</span><span class="sxs-lookup"><span data-stu-id="17a3f-713">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="17a3f-714">Uppdaterat tjänstanrop för avregistrering av container för Azure-filresurs</span><span class="sxs-lookup"><span data-stu-id="17a3f-714">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="17a3f-715">Uppdatera Set-AzRecoveryServicesAsrAlertSetting.md</span><span class="sxs-lookup"><span data-stu-id="17a3f-715">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="17a3f-716">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="17a3f-716">Az.Resources</span></span>
- <span data-ttu-id="17a3f-717">Ta bort den cmdlet som saknas och som refereras i dokumentationen till New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="17a3f-717">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="17a3f-718">Princip-cmdletar har uppdaterats så att de använder den nya API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="17a3f-718">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="17a3f-719">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="17a3f-719">Az.ServiceBus</span></span>
* <span data-ttu-id="17a3f-720">Ny cmmdlet har lagts till för att skapa SAS-token: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="17a3f-720">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="17a3f-721">verifierings- och felmeddelande har lagts till för authorizationrules-rättigheter om endast "hantera" har tilldelats</span><span class="sxs-lookup"><span data-stu-id="17a3f-721">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="17a3f-722">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="17a3f-722">Az.Sql</span></span>
* <span data-ttu-id="17a3f-723">Åtgärda saknade exempel för Set-AzSqlDatabaseSecondary cmdlet</span><span class="sxs-lookup"><span data-stu-id="17a3f-723">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="17a3f-724">Åtgärda angivna återkommande genomsökningar för bedömning av säkerhetsrisk utan angivna e-postadresser</span><span class="sxs-lookup"><span data-stu-id="17a3f-724">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="17a3f-725">Korrigera ett skrivfel i ett varningsmeddelande.</span><span class="sxs-lookup"><span data-stu-id="17a3f-725">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="17a3f-726">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="17a3f-726">Az.Storage</span></span>
* <span data-ttu-id="17a3f-727">Uppdatera exempel i referensdokumentationen för Get-AzStorageAccount så att rätt parameternamn används</span><span class="sxs-lookup"><span data-stu-id="17a3f-727">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="17a3f-728">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="17a3f-728">Az.StorageSync</span></span>
* <span data-ttu-id="17a3f-729">Lägger till cmdleten Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="17a3f-729">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="17a3f-730">Åtgärda problem 9551 så att TierFilesOlderThanDays föredras</span><span class="sxs-lookup"><span data-stu-id="17a3f-730">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="17a3f-731">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="17a3f-731">Az.Websites</span></span>
* <span data-ttu-id="17a3f-732">Åtgärdar ett fel där vissa SiteConfig-egenskaper inte returnerades av Get-AzWebApp och Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="17a3f-732">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="17a3f-733">Lägger till en ny platsparameter för Get-AzDeletedWebApp och Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="17a3f-733">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="17a3f-734">Åtgärdar ett fel i kloning av webbapp-platser som använder New-AzWebApp-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="17a3f-734">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="17a3f-735">2.4.0 – juli 2019</span><span class="sxs-lookup"><span data-stu-id="17a3f-735">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="17a3f-736">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="17a3f-736">Az.Accounts</span></span>
* <span data-ttu-id="17a3f-737">Lägg till stöd för profil-cmdletar</span><span class="sxs-lookup"><span data-stu-id="17a3f-737">Add support for profile cmdlets</span></span>
* <span data-ttu-id="17a3f-738">Lägg till stöd för miljöer och dataplaner i genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="17a3f-738">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="17a3f-739">Åtgärda bugg där fel slutpunkt i vissa fall användes för cmdletar för dataplaner i Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="17a3f-739">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="17a3f-740">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="17a3f-740">Az.Advisor</span></span>
* <span data-ttu-id="17a3f-741">GA-version av Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="17a3f-741">GA release of Az.Advisor</span></span>
* <span data-ttu-id="17a3f-742">Den här modulen ingår nu som en del av `Az`-sammanslagningsmodulen</span><span class="sxs-lookup"><span data-stu-id="17a3f-742">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="17a3f-743">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="17a3f-743">Az.ApiManagement</span></span>
* <span data-ttu-id="17a3f-744">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="17a3f-744">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="17a3f-745">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="17a3f-745">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="17a3f-746">Stöd för att fråga prenumerationer efter användare och produkt har lagts till</span><span class="sxs-lookup"><span data-stu-id="17a3f-746">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="17a3f-747">Stöd för att fråga med hjälp av omfång ”/”, ”/apis”, ”/apis/echo-api” har lagts till</span><span class="sxs-lookup"><span data-stu-id="17a3f-747">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="17a3f-748">Korrigering av problem https://github.com/Azure/azure-powershell/issues/9307 och https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="17a3f-748">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="17a3f-749">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="17a3f-749">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="17a3f-750">Stöd för att ange ”ApiVersion” och ”ApiVersionSetId” när API:er importeras har lagts till</span><span class="sxs-lookup"><span data-stu-id="17a3f-750">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="17a3f-751">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="17a3f-751">Az.Automation</span></span>
* <span data-ttu-id="17a3f-752">Bugg med cmdleten Set-AzAutomationConnectionFieldValue för att hantera strängvärde har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="17a3f-752">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="17a3f-753">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="17a3f-753">Az.Compute</span></span>
* <span data-ttu-id="17a3f-754">Lägg till parametern HyperVGeneration i New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="17a3f-754">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="17a3f-755">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="17a3f-755">Az.DataFactory</span></span>
* <span data-ttu-id="17a3f-756">Uppdaterar utdata från ADF-cmdletar som hämtar aktivitetskörningar, hämtar pipelinekörningar och hämtar utlösarkörningar för stöd för Select-Object-pipe.</span><span class="sxs-lookup"><span data-stu-id="17a3f-756">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="17a3f-757">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="17a3f-757">Az.EventGrid</span></span>
* <span data-ttu-id="17a3f-758">Korrigera stavfel i dokumentation om ”New-AzEventGridSubscription”</span><span class="sxs-lookup"><span data-stu-id="17a3f-758">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="17a3f-759">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="17a3f-759">Az.IotHub</span></span>
* <span data-ttu-id="17a3f-760">Lägg till stöd för att återskapa principnycklar för auktorisering.</span><span class="sxs-lookup"><span data-stu-id="17a3f-760">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="17a3f-761">Az.Network</span><span class="sxs-lookup"><span data-stu-id="17a3f-761">Az.Network</span></span>
* <span data-ttu-id="17a3f-762">”RoutingPreference” har lagts till i offentliga IP-taggar</span><span class="sxs-lookup"><span data-stu-id="17a3f-762">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="17a3f-763">Förbättra exempel för referensdokumentation om ”Get-AzNetworkServiceTag”</span><span class="sxs-lookup"><span data-stu-id="17a3f-763">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="17a3f-764">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="17a3f-764">Az.PolicyInsights</span></span>
* <span data-ttu-id="17a3f-765">Åtgärda problem med null-referens i Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="17a3f-765">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="17a3f-766">Mer information här: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="17a3f-766">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="17a3f-767">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="17a3f-767">Az.OperationalInsights</span></span>
* <span data-ttu-id="17a3f-768">Modellen för CustomLog-datakälla som returneras i Get-AzOperationalInsightsDataSource har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="17a3f-768">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="17a3f-769">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="17a3f-769">Az.RecoveryServices</span></span>
* <span data-ttu-id="17a3f-770">Kommandot get-policy för IaaSVM:er har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="17a3f-770">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="17a3f-771">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="17a3f-771">Az.Resources</span></span>
    - <span data-ttu-id="17a3f-772">Korrigera hjälptext för den översta parametern i Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="17a3f-772">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="17a3f-773">Lägg till växlingsstöd på klientsidan för Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="17a3f-773">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="17a3f-774">Lägg till nya parametrar för Set-AzPolicyAssignment, -PolicyParameters och -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="17a3f-774">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="17a3f-775">En mängd dokument- och exempeluppdateringar för Policy-cmdletar</span><span class="sxs-lookup"><span data-stu-id="17a3f-775">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="17a3f-776">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="17a3f-776">Az.ServiceBus</span></span>
* <span data-ttu-id="17a3f-777">Korrigering av problem #4938 – New-AzureRmServiceBusQueue returnerar BadRequest vid konfiguration av MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="17a3f-777">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="17a3f-778">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="17a3f-778">Az.Sql</span></span>
* <span data-ttu-id="17a3f-779">Lägg till cmdletar för instansredundansgrupper från förhandsversion till offentlig version</span><span class="sxs-lookup"><span data-stu-id="17a3f-779">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="17a3f-780">Stöd för granskning för Azure SQL Server\Database med nya cmdletar.</span><span class="sxs-lookup"><span data-stu-id="17a3f-780">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="17a3f-781">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="17a3f-781">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="17a3f-782">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="17a3f-782">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="17a3f-783">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="17a3f-783">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="17a3f-784">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="17a3f-784">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="17a3f-785">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="17a3f-785">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="17a3f-786">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="17a3f-786">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="17a3f-787">Ta bort begränsningar för e-post från inställningarna för sårbarhetsbedömning</span><span class="sxs-lookup"><span data-stu-id="17a3f-787">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="17a3f-788">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="17a3f-788">Az.Storage</span></span>
* <span data-ttu-id="17a3f-789">Ändra två parametrar ”-IndexDocument” och ”-ErrorDocument404Path” från ”krävs” till ”valfri” i cmdlet:</span><span class="sxs-lookup"><span data-stu-id="17a3f-789">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="17a3f-790">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="17a3f-790">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="17a3f-791">Uppdatera hjälpen för Get-AzStorageBlobContent genom att lägga till ett exempel</span><span class="sxs-lookup"><span data-stu-id="17a3f-791">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="17a3f-792">Visa mer felinformation när cmdleten misslyckas med StorageException</span><span class="sxs-lookup"><span data-stu-id="17a3f-792">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="17a3f-793">Stöd för att skapa eller uppdatera lagringskonto med Azure Files AAD DS-autentisering</span><span class="sxs-lookup"><span data-stu-id="17a3f-793">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="17a3f-794">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="17a3f-794">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="17a3f-795">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="17a3f-795">Set-AzStorageAccount</span></span>
* <span data-ttu-id="17a3f-796">Stöd för att lista eller stänga filreferenser för en filresurs, filkatalog eller en fil</span><span class="sxs-lookup"><span data-stu-id="17a3f-796">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="17a3f-797">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="17a3f-797">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="17a3f-798">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="17a3f-798">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="17a3f-799">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="17a3f-799">Az.StorageSync</span></span>
* <span data-ttu-id="17a3f-800">Den här modulen ingår nu som en del av `Az`-sammanslagningsmodulen</span><span class="sxs-lookup"><span data-stu-id="17a3f-800">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="17a3f-801">2.3.2 – juni 2019</span><span class="sxs-lookup"><span data-stu-id="17a3f-801">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="17a3f-802">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="17a3f-802">Az.Accounts</span></span>
* <span data-ttu-id="17a3f-803">Åtgärda bugg med felaktiga webbadresser som i vissa fall användes för Functions-anrop</span><span class="sxs-lookup"><span data-stu-id="17a3f-803">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="17a3f-804">Mer information här: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="17a3f-804">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="17a3f-805">Åtgärda problem med alias från AzureRM i Az-cmdletar</span><span class="sxs-lookup"><span data-stu-id="17a3f-805">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="17a3f-806">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="17a3f-806">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="17a3f-807">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="17a3f-807">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="17a3f-808">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="17a3f-808">Az.Compute</span></span>
* <span data-ttu-id="17a3f-809">Parameteruppsättningarna New-AzVm och New-AzVmss accepterar nu parametern ”ProximityPlacementGroup”.</span><span class="sxs-lookup"><span data-stu-id="17a3f-809">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="17a3f-810">Stavfel i referensdokumentationen för ”New-AzVM” har korrigerats</span><span class="sxs-lookup"><span data-stu-id="17a3f-810">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="17a3f-811">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="17a3f-811">Az.Dns</span></span>
* <span data-ttu-id="17a3f-812">Stavfel i hjälpexempel för ”Set-AzDnsZone” har korrigerats.</span><span class="sxs-lookup"><span data-stu-id="17a3f-812">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="17a3f-813">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="17a3f-813">Az.EventGrid</span></span>
* <span data-ttu-id="17a3f-814">Har uppdaterats för att använda API-versionen 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="17a3f-814">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="17a3f-815">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="17a3f-815">New cmdlets:</span></span>
    - <span data-ttu-id="17a3f-816">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="17a3f-816">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="17a3f-817">Skapar en ny Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="17a3f-817">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="17a3f-818">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="17a3f-818">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="17a3f-819">Hämtar information om en Event Grid-domän eller hämtar en lista med alla Event Grid-domäner i den aktuella Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="17a3f-819">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="17a3f-820">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="17a3f-820">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="17a3f-821">Tar bort en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="17a3f-821">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="17a3f-822">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="17a3f-822">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="17a3f-823">Återskapar nyckeln för delad åtkomst för en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="17a3f-823">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="17a3f-824">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="17a3f-824">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="17a3f-825">Hämtar de nycklar för delad åtkomst som används för att publicera händelser till en Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="17a3f-825">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="17a3f-826">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="17a3f-826">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="17a3f-827">Skapar ett nytt Azure Event Grid-domänämne.</span><span class="sxs-lookup"><span data-stu-id="17a3f-827">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="17a3f-828">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="17a3f-828">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="17a3f-829">Hämtar information om ett Event Grid-domänämne eller hämtar en lista med alla Event Grid-domänämnen under en specifik Event Grid-domän i nuvarande Azure</span><span class="sxs-lookup"><span data-stu-id="17a3f-829">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="17a3f-830">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="17a3f-830">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="17a3f-831">Tar bort ett befintligt Azure Event Grid-domänämne.</span><span class="sxs-lookup"><span data-stu-id="17a3f-831">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="17a3f-832">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="17a3f-832">Updated cmdlets:</span></span>
    - <span data-ttu-id="17a3f-833">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="17a3f-833">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="17a3f-834">Lägg till nya obligatoriska parametrar för att stödja piping för den nya Event Grid-domänen och Event Grid-domänämnet för att göra det möjligt att skapa nya händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="17a3f-834">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="17a3f-835">Lägg till nya obligatoriska parametrar för att ange det nya Event Grid-domännamnet och/eller namnet på Event Grid-domänämnet för att göra det möjligt att skapa nya händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="17a3f-835">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="17a3f-836">Lägg till ny parameteruppsättningar för domäner och domänämnen för att göra det möjligt att återanvända befintliga parametrar (t.ex. EndPointType, SubjectBeginsWith osv).</span><span class="sxs-lookup"><span data-stu-id="17a3f-836">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="17a3f-837">Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="17a3f-837">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="17a3f-838">Förfallodatum för händelseprenumeration</span><span class="sxs-lookup"><span data-stu-id="17a3f-838">Event subscription expiration date,</span></span>
            - <span data-ttu-id="17a3f-839">Avancerade filterparametrar.</span><span class="sxs-lookup"><span data-stu-id="17a3f-839">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="17a3f-840">Lägg till ny uppräkning för servicebusqueue som mål.</span><span class="sxs-lookup"><span data-stu-id="17a3f-840">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="17a3f-841">Tillåt inte användning av ”Alla” i alternativet -IncludedEventType och ersätt det med</span><span class="sxs-lookup"><span data-stu-id="17a3f-841">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="17a3f-842">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="17a3f-842">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="17a3f-843">Lägg till ny valfria parametrar (Top, ODataQuery och NextLink) för att stödja sidnumrering och filtrering av resultat.</span><span class="sxs-lookup"><span data-stu-id="17a3f-843">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="17a3f-844">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="17a3f-844">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="17a3f-845">Lägg till nya obligatoriska parametrar för att stödja piping för en Event Grid-domän och Event Grid-domänämnen för att göra det möjligt att ta bort befintliga händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="17a3f-845">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="17a3f-846">Lägg till nya obligatoriska parametrar för att ange Event Grid-domännamnet och/eller namnet på Event Grid-domänämnet för att göra det möjligt att ta bort befintliga händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="17a3f-846">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="17a3f-847">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="17a3f-847">Az.FrontDoor</span></span>
* <span data-ttu-id="17a3f-848">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="17a3f-848">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="17a3f-849">Lägg till stöd för transformeringar och nytt värde för automatisk komplettering för operatorer (RegEx)</span><span class="sxs-lookup"><span data-stu-id="17a3f-849">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="17a3f-850">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="17a3f-850">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="17a3f-851">Lägg till nya värden för automatisk komplettering</span><span class="sxs-lookup"><span data-stu-id="17a3f-851">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="17a3f-852">Az.Network</span><span class="sxs-lookup"><span data-stu-id="17a3f-852">Az.Network</span></span>
* <span data-ttu-id="17a3f-853">Lägg till stöd för resurs för virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="17a3f-853">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="17a3f-854">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="17a3f-854">New cmdlets</span></span>
        - <span data-ttu-id="17a3f-855">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="17a3f-855">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="17a3f-856">Lägg till AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="17a3f-856">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="17a3f-857">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="17a3f-857">New cmdlets</span></span> 
        - <span data-ttu-id="17a3f-858">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="17a3f-858">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="17a3f-859">Lägg till PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="17a3f-859">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="17a3f-860">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="17a3f-860">New cmdlets</span></span> 
        - <span data-ttu-id="17a3f-861">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="17a3f-861">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="17a3f-862">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="17a3f-862">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="17a3f-863">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="17a3f-863">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="17a3f-864">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="17a3f-864">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="17a3f-865">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="17a3f-865">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="17a3f-866">Lägg till PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="17a3f-866">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="17a3f-867">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="17a3f-867">New cmdlets</span></span>
        - <span data-ttu-id="17a3f-868">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="17a3f-868">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="17a3f-869">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="17a3f-869">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="17a3f-870">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="17a3f-870">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="17a3f-871">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="17a3f-871">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="17a3f-872">Nedanstående kommandon för funktionen har uppdaterats: Flaggan UseLocalAzureIpAddress på VpnConnection</span><span class="sxs-lookup"><span data-stu-id="17a3f-872">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="17a3f-873">New-AzVpnConnection har uppdaterats: Den valfria parametern -UseLocalAzureIpAddress har lagts till för att visa att en lokal IP-adress i Azure ska användas som källadress när anslutningen initieras.</span><span class="sxs-lookup"><span data-stu-id="17a3f-873">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="17a3f-874">Set-AzVpnConnection har uppdaterats: Den valfria parametern -UseLocalAzureIpAddress har lagts till för att visa att en lokal IP-adress i Azure ska användas som källadress när anslutningen initieras.</span><span class="sxs-lookup"><span data-stu-id="17a3f-874">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="17a3f-875">Det skrivskyddade fältet PeeredConnections har lagts till i ExpressRoute-peering.</span><span class="sxs-lookup"><span data-stu-id="17a3f-875">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="17a3f-876">Det skrivskyddade fältet GlobalReachEnabled har lagts till i ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="17a3f-876">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="17a3f-877">Ett attribut för icke-bakåtkompatibla ändringar har lagts till för att lyfta fram utfasning av fältet AllowGlobalReach i modellen ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="17a3f-877">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="17a3f-878">Problem 8756 har åtgärdats: Fel vid användning av TargetListenerID med AzApplicationGatewayRedirectConfiguration-cmdletar</span><span class="sxs-lookup"><span data-stu-id="17a3f-878">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="17a3f-879">En bugg i New-AzApplicationGatewayPathRuleConfig som gjorde att regeluppsättningen för att återskapa inte kunde anges har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="17a3f-879">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="17a3f-880">Visningen av VirtualNetworkTaps i NetworkInterfaceIpConfiguration har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="17a3f-880">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="17a3f-881">Cortex Get-cmdletar för att visa en lista med alla delar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="17a3f-881">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="17a3f-882">Funktionen för att skapa VirtualHub-referenser för ExpressRouteGateways och VpnGateway har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="17a3f-882">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="17a3f-883">Stöd för tillgänglighetszoner i AzureFirewall och NatGateway har lagts till</span><span class="sxs-lookup"><span data-stu-id="17a3f-883">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="17a3f-884">Cmdleten Get-AzNetworkServiceTag har lagts till</span><span class="sxs-lookup"><span data-stu-id="17a3f-884">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="17a3f-885">Lägg till stöd för flera offentliga IP-adresser för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="17a3f-885">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="17a3f-886">Cmdleten New-AzFirewall har uppdaterats:</span><span class="sxs-lookup"><span data-stu-id="17a3f-886">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="17a3f-887">Parametern -PublicIpAddress som accepterar ett eller flera offentliga IP-adressobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="17a3f-887">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="17a3f-888">Parametern -VirtualNetwork som accepterar ett virtuellt nätverksobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="17a3f-888">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="17a3f-889">Metoderna AddPublicIpAddress och RemovePublicIpAddress har lagts till på brandväggsobjekt – dessa accepterar ett offentligt IP-adressobjekt som indata</span><span class="sxs-lookup"><span data-stu-id="17a3f-889">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="17a3f-890">Inaktuella parametrar -PublicIpName och -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="17a3f-890">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="17a3f-891">Nedanstående kommandon för funktionen har uppdaterats: Ange autentiseringsalternativ för VpnClient AAD till resurser för virtuella nätverksgatewayer.</span><span class="sxs-lookup"><span data-stu-id="17a3f-891">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="17a3f-892">New-AzVirtualNetworkGateway har uppdaterats: De valfria parametrarna AadTenantUri, AadAudienceId och AadIssuerUri för att ange VpnClient AAD-autentiseringsalternativ på en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="17a3f-892">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="17a3f-893">Set-AzVirtualNetworkGateway har uppdaterats: De valfria parametrarna AadTenantUri, AadAudienceId och AadIssuerUri för att ange VpnClient AAD-autentiseringsalternativ på en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="17a3f-893">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="17a3f-894">Set-AzVirtualNetworkGateway har uppdaterats: Den valfria växelparametern RemoveAadAuthentication som tar bort VpnClient AAD-autentiseringsalternativ från en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="17a3f-894">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="17a3f-895">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="17a3f-895">Az.OperationalInsights</span></span>
* <span data-ttu-id="17a3f-896">Aktivera prisnivån **pergb2018** i kommandot ”New-AzureRmOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="17a3f-896">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="17a3f-897">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="17a3f-897">Az.Resources</span></span>
* <span data-ttu-id="17a3f-898">Stöd för ytterligare alternativ för att exportera en mall</span><span class="sxs-lookup"><span data-stu-id="17a3f-898">Support for additional Template Export options</span></span>
    - <span data-ttu-id="17a3f-899">Lägg till parametern ”-SkipResourceNameParameterization” till Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="17a3f-899">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="17a3f-900">Lägg till parametern ”-SkipAllParameterization” till Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="17a3f-900">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="17a3f-901">Lägg till parametern ”-Resource” till Export-AzResourceGroup för exporterad resursfiltrering</span><span class="sxs-lookup"><span data-stu-id="17a3f-901">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="17a3f-902">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="17a3f-902">Az.ServiceFabric</span></span>
* <span data-ttu-id="17a3f-903">Åtgärda att fel tumavtryck används vid tilläggning av certifikat i ByExistingKeyVault i vissa fall</span><span class="sxs-lookup"><span data-stu-id="17a3f-903">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="17a3f-904">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="17a3f-904">Az.Sql</span></span>
* <span data-ttu-id="17a3f-905">Åtgärda suffix för lagringsslutpunkt i Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="17a3f-905">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="17a3f-906">Åtgärda att aktivering av Advanced Data Security åsidosätter Advanced Threat Protection-princip</span><span class="sxs-lookup"><span data-stu-id="17a3f-906">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="17a3f-907">Nya cmdletar för Management.Sql som gör att kunderna kan lägga till nycklar för transparent datakryptering (TDE) och ange TDE-skydd för hanterade instanser</span><span class="sxs-lookup"><span data-stu-id="17a3f-907">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="17a3f-908">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="17a3f-908">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="17a3f-909">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="17a3f-909">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="17a3f-910">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="17a3f-910">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="17a3f-911">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="17a3f-911">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="17a3f-912">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="17a3f-912">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="17a3f-913">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="17a3f-913">Az.Storage</span></span>
* <span data-ttu-id="17a3f-914">Stöd för typerna FileStorage och SkuName Premium_ZRS när lagringskonton skapas</span><span class="sxs-lookup"><span data-stu-id="17a3f-914">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="17a3f-915">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="17a3f-915">New-AzStorageAccount</span></span>
* <span data-ttu-id="17a3f-916">Beskrivningen av cmdleten för bloboföränderlighet har förtydligats</span><span class="sxs-lookup"><span data-stu-id="17a3f-916">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="17a3f-917">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="17a3f-917">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="17a3f-918">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="17a3f-918">Az.Websites</span></span>
* <span data-ttu-id="17a3f-919">Optimerar Get-AzWebAppCertificate för att filtrera efter resursgrupp på servern i stället för klienten</span><span class="sxs-lookup"><span data-stu-id="17a3f-919">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="17a3f-920">Lägger till växlingsparametern -UseDisasterRecovery till Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="17a3f-920">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="17a3f-921">2.2.0 – juni 2019</span><span class="sxs-lookup"><span data-stu-id="17a3f-921">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="17a3f-922">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="17a3f-922">Az.Cdn</span></span>
* <span data-ttu-id="17a3f-923">Uppdaterade cmdletar för att ge stöd för rulesEngine-funktion baserat på API-version 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="17a3f-923">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="17a3f-924">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="17a3f-924">Az.Compute</span></span>
* <span data-ttu-id="17a3f-925">Lade till parameter `NoWait` som startar åtgärden och returnerar omedelbart, innan åtgärden har slutförts.</span><span class="sxs-lookup"><span data-stu-id="17a3f-925">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="17a3f-926">Uppdaterade cmdletar:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="17a3f-926">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="17a3f-927">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="17a3f-927">Az.EventHub</span></span>
* <span data-ttu-id="17a3f-928">Korrigering för #9231 – Get-AzEventHubNamespace returnerar inga taggar</span><span class="sxs-lookup"><span data-stu-id="17a3f-928">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="17a3f-929">Korrigering för #9230 – Get-AzEventHubNamespace returnerar ResourceGroup istället för ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17a3f-929">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="17a3f-930">Az.Network</span><span class="sxs-lookup"><span data-stu-id="17a3f-930">Az.Network</span></span>
* <span data-ttu-id="17a3f-931">Uppdatera ResourceId och InputObject för NAT-gateway</span><span class="sxs-lookup"><span data-stu-id="17a3f-931">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="17a3f-932">Lägg till alias för ResourceId och InputObject</span><span class="sxs-lookup"><span data-stu-id="17a3f-932">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="17a3f-933">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="17a3f-933">Az.PolicyInsights</span></span>
* <span data-ttu-id="17a3f-934">Åtgärda Null-referensproblem i Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="17a3f-934">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="17a3f-935">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="17a3f-935">Az.RecoveryServices</span></span>
* <span data-ttu-id="17a3f-936">Minsta kvarhållning för IaaSVM-policy i dagar ändrat till 7 från 1</span><span class="sxs-lookup"><span data-stu-id="17a3f-936">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="17a3f-937">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="17a3f-937">Az.ServiceBus</span></span>
* <span data-ttu-id="17a3f-938">Korrigering för ärende #9182 – Get-AzServiceBusNamespace returnerar ResourceGroup istället för ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17a3f-938">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="17a3f-939">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="17a3f-939">Az.ServiceFabric</span></span>
* <span data-ttu-id="17a3f-940">Åtgärda stavfel i felmeddelandet för Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="17a3f-940">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="17a3f-941">Åtgärda saknat tecken i Service Fabric-kommandorader</span><span class="sxs-lookup"><span data-stu-id="17a3f-941">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="17a3f-942">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="17a3f-942">Az.Sql</span></span>
* <span data-ttu-id="17a3f-943">Lägg till parametern DnsZonePartner för New-AzureSqlInstance-cmdlet för att ge stöd för AutoDr för hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="17a3f-943">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="17a3f-944">Avvecklar cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="17a3f-944">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="17a3f-945">Döp om cmdletar för hotidentifiering till Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="17a3f-945">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="17a3f-946">Parametrarna New-AzSqlInstance -StorageSizeInGB och -LicenseType är nu valfria.</span><span class="sxs-lookup"><span data-stu-id="17a3f-946">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="17a3f-947">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="17a3f-947">Az.Websites</span></span>
* <span data-ttu-id="17a3f-948">åtgärdar problemet där användningen av Set-AzWebApp och Set-AzWebAppSlot med -WebApp-egenskap tog bort taggarna</span><span class="sxs-lookup"><span data-stu-id="17a3f-948">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="17a3f-949">2.1.0 – maj 2019</span><span class="sxs-lookup"><span data-stu-id="17a3f-949">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="17a3f-950">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="17a3f-950">Az.ApiManagement</span></span>
* <span data-ttu-id="17a3f-951">Skapade nya cmdletar för att hantera diagnostik för global- och API-omfång</span><span class="sxs-lookup"><span data-stu-id="17a3f-951">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="17a3f-952">**Get-AzApiManagementDiagnostic** – Skaffa diagnostik konfigurerad för global- eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="17a3f-952">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="17a3f-953">**New-AzApiManagementDiagnostic** – Skapa ny diagnostik för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="17a3f-953">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="17a3f-954">**New-AzApiManagementHttpMessageDiagnostic** – Skapa diagnostikinställning om vilka rubriker som ska loggas och storleken på brödtextbyte</span><span class="sxs-lookup"><span data-stu-id="17a3f-954">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="17a3f-955">**New-AzApiManagementPipelineDiagnosticSetting** – Skapa diagnostikinställningar för inkommande/utgående HTTP-meddelanden till gatewayen.</span><span class="sxs-lookup"><span data-stu-id="17a3f-955">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="17a3f-956">**New-AzApiManagementSamplingSetting** – Skapa samplinginställningar för begäranden/svar för en diagnostik</span><span class="sxs-lookup"><span data-stu-id="17a3f-956">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="17a3f-957">**Remove-AzApiManagementDiagnostic** – Ta bort en diagnostikenhet för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="17a3f-957">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="17a3f-958">**Set-AzApiManagementDiagnostic** – Uppdatera en diagnostikenhet för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="17a3f-958">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="17a3f-959">Skapade nya cmdletar för hantering av cacheminne i ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="17a3f-959">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="17a3f-960">**Get-AzApiManagementCache** – Hämta information om cacheminnet som anges av identifierare eller alla cacheminnen</span><span class="sxs-lookup"><span data-stu-id="17a3f-960">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="17a3f-961">**New-AzApiManagementCache** – Skapa ett nytt default-cacheminne eller cacheminne i en viss Azure-region</span><span class="sxs-lookup"><span data-stu-id="17a3f-961">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="17a3f-962">**Remove-AzApiManagementCache** – Ta bort ett cacheminne</span><span class="sxs-lookup"><span data-stu-id="17a3f-962">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="17a3f-963">**Remove-AzApiManagementCache** – Ta bort ett cacheminne</span><span class="sxs-lookup"><span data-stu-id="17a3f-963">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="17a3f-964">Skapade nya cmdletar för hantering av API-schema</span><span class="sxs-lookup"><span data-stu-id="17a3f-964">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="17a3f-965">**New-AzApiManagementSchema** – Skapa ett nytt schema för ett API</span><span class="sxs-lookup"><span data-stu-id="17a3f-965">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="17a3f-966">**Get-AzApiManagementSchema** – Hämta de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="17a3f-966">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="17a3f-967">**Remove-AzApiManagementSchema** – Ta bort de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="17a3f-967">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="17a3f-968">**Set-AzApiManagementSchema** – Uppdatera de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="17a3f-968">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="17a3f-969">Skapa ny cmdlet för att generera en användartoken.</span><span class="sxs-lookup"><span data-stu-id="17a3f-969">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="17a3f-970">**New-AzApiManagementUserToken** – Skapa en ny användartoken som enligt standardinställning är giltig i 8 timmar. Token för GIT-användaren kan skapas med den här cmdleten./</span><span class="sxs-lookup"><span data-stu-id="17a3f-970">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="17a3f-971">Skapade en ny cmdlet för att hämta nätverksstatus</span><span class="sxs-lookup"><span data-stu-id="17a3f-971">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="17a3f-972">**Get-AzApiManagementNetworkStatus** – Hämta nätverksstatusanslutningen för resurserna som API Management-tjänsten är beroende av.</span><span class="sxs-lookup"><span data-stu-id="17a3f-972">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="17a3f-973">Det här är användbart när du distribuerar ApiManagement-tjänsten i ett virtuellt nätverk och validerar om något beroende är brutet.</span><span class="sxs-lookup"><span data-stu-id="17a3f-973">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="17a3f-974">Uppdaterade cmdlet **New-AzApiManagement** för att hantera ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="17a3f-974">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="17a3f-975">Lade till stöd för den nya SKU:n Consumption</span><span class="sxs-lookup"><span data-stu-id="17a3f-975">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="17a3f-976">Aktiverade stöd för att slå på flaggan EnableClientCertificate för SKU:n Consumption</span><span class="sxs-lookup"><span data-stu-id="17a3f-976">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="17a3f-977">Den nya cmdleten **New-AzApiManagementSslSetting** gör det möjligt att ställa in TLS/SSL-inställningen på ”Backend” och ”Frontend” (serverdel och klientdel).</span><span class="sxs-lookup"><span data-stu-id="17a3f-977">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="17a3f-978">Det här kan också användas till att konfigurera chiffer som 3DES och ServerProtocols som Http2 för Frontend för en ApiManagement-tjänst.</span><span class="sxs-lookup"><span data-stu-id="17a3f-978">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="17a3f-979">Stöd har lagts till för att konfigurera värdnamnet DeveloperPortal på ApiManagement-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="17a3f-979">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="17a3f-980">Uppdaterade cmdletar **Get-AzApiManagementSsoToken** för att ta PsApiManagement-objekt som indata</span><span class="sxs-lookup"><span data-stu-id="17a3f-980">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="17a3f-981">Uppdaterad cmdleten för att visa infogade felmeddelanden</span><span class="sxs-lookup"><span data-stu-id="17a3f-981">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="17a3f-982">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Felkod: Felmeddelande av typen ValidationError: Ett eller flera fält innehåller felaktiga värden: Felinformation:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="17a3f-982">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="17a3f-983">Uppdaterade cmdlet **Export-AzApiManagementApi** för att exportera API:er i OpenApi 3.0-format</span><span class="sxs-lookup"><span data-stu-id="17a3f-983">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="17a3f-984">Uppdaterade cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="17a3f-984">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="17a3f-985">Importera API från dokumentspecifikationen OpenApi 3.0</span><span class="sxs-lookup"><span data-stu-id="17a3f-985">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="17a3f-986">Om du vill åsidosätta egenskapen PsApiManagementSchema specificerad i ett dokument (Swagger, Wadl, Wsdl, OpenApi).</span><span class="sxs-lookup"><span data-stu-id="17a3f-986">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="17a3f-987">Åsidosätta egenskapen ServiceUrl som specificeras i ett dokument.</span><span class="sxs-lookup"><span data-stu-id="17a3f-987">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="17a3f-988">Uppdaterade cmdlet **Get-AzApiManagementPolicy** för att returnera policy i undantaget format av typen icke-XML med rawxml</span><span class="sxs-lookup"><span data-stu-id="17a3f-988">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="17a3f-989">Uppdaterade cmdlet **Set-AzApiManagementPolicy** för att godkänna policy i undantaget format av typen icke-XML med rawxml och XML undantaget med xml</span><span class="sxs-lookup"><span data-stu-id="17a3f-989">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="17a3f-990">Uppdaterad cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="17a3f-990">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="17a3f-991">Konfigurera API med OpenId auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="17a3f-991">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="17a3f-992">Skapa ett API i ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="17a3f-992">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="17a3f-993">Klona ett API med SourceApiId och SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="17a3f-993">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="17a3f-994">Möjlighet att konfigurera SubscriptionRequired i API-omfattningen.</span><span class="sxs-lookup"><span data-stu-id="17a3f-994">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="17a3f-995">Uppdaterad cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="17a3f-995">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="17a3f-996">Konfigurera API med OpenId auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="17a3f-996">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="17a3f-997">Uppdatera ett API till ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="17a3f-997">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="17a3f-998">Möjlighet att konfigurera SubscriptionRequired i API-omfattningen.</span><span class="sxs-lookup"><span data-stu-id="17a3f-998">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="17a3f-999">Uppdaterad cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="17a3f-999">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="17a3f-1000">Klona en befintlig version med hjälp av SourceApiRevision (kopiera taggar, produkter, åtgärder och principer).</span><span class="sxs-lookup"><span data-stu-id="17a3f-1000">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="17a3f-1001">Den nya revisionen antar ApiId från den överordnade instansen.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1001">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="17a3f-1002">Tillhandahålla ApiRevisionDescription</span><span class="sxs-lookup"><span data-stu-id="17a3f-1002">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="17a3f-1003">Åsidosätta ServiceUrl vid kloning av ett API.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1003">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="17a3f-1004">Uppdaterad cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="17a3f-1004">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="17a3f-1005">Konfigurera AAD eller AADB2C med en Authority</span><span class="sxs-lookup"><span data-stu-id="17a3f-1005">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="17a3f-1006">Konfigurera SignupPolicy, SigninPolicy, ProfileEditingPolicy och PasswordResetPolicy</span><span class="sxs-lookup"><span data-stu-id="17a3f-1006">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="17a3f-1007">Uppdaterad cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="17a3f-1007">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="17a3f-1008">Kompensera för ny SubscriptonModel med Scope och UserId</span><span class="sxs-lookup"><span data-stu-id="17a3f-1008">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="17a3f-1009">Kompensera för gammal prenumerationsmodell med ProductId och UserId</span><span class="sxs-lookup"><span data-stu-id="17a3f-1009">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="17a3f-1010">Lägg till funktion för att aktivera AllowTracing på prenumerationsnivå.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1010">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="17a3f-1011">Uppdaterad cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="17a3f-1011">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="17a3f-1012">Kompensera för ny SubscriptonModel med Scope och UserId</span><span class="sxs-lookup"><span data-stu-id="17a3f-1012">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="17a3f-1013">Kompensera för gammal prenumerationsmodell med ProductId och UserId</span><span class="sxs-lookup"><span data-stu-id="17a3f-1013">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="17a3f-1014">Lägg till funktion för att aktivera AllowTracing på prenumerationsnivå.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1014">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="17a3f-1015">Uppdaterade följande cmdletar för att acceptera ResourceId som indata</span><span class="sxs-lookup"><span data-stu-id="17a3f-1015">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="17a3f-1016">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="17a3f-1016">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="17a3f-1017">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="17a3f-1017">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="17a3f-1018">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="17a3f-1018">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="17a3f-1019">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="17a3f-1019">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="17a3f-1020">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="17a3f-1020">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="17a3f-1021">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="17a3f-1021">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="17a3f-1022">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="17a3f-1022">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="17a3f-1023">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="17a3f-1023">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="17a3f-1024">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="17a3f-1024">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="17a3f-1025">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="17a3f-1025">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="17a3f-1026">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="17a3f-1026">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="17a3f-1027">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="17a3f-1027">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="17a3f-1028">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="17a3f-1028">Az.Automation</span></span>
* <span data-ttu-id="17a3f-1029">Uppdaterade Get-AzAutomationJobOutputRecord för att hantera postvärden av typen JSON och Text.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1029">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="17a3f-1030">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="17a3f-1030">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="17a3f-1031">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="17a3f-1031">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="17a3f-1032">Ändrade beteende för Start-AzAutomationDscCompilationJob till att bara starta jobbet istället för att vänta på slutförandet.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1032">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="17a3f-1033">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="17a3f-1033">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="17a3f-1034">Korrigering för Get-AzAutomationDscNode när using -Name returnerar alla noder.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1034">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="17a3f-1035">Nu returnerar den endast den matchande noden.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1035">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="17a3f-1036">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="17a3f-1036">Az.Compute</span></span>
* <span data-ttu-id="17a3f-1037">Lägg till parametrarna ProtectFromScaleIn och ProtectFromScaleSetAction i cmdleten Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1037">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="17a3f-1038">Nu är standardinställningen att vimpelparametern New-AzVM använder en tillgänglig plats om USA, östra inte stöds</span><span class="sxs-lookup"><span data-stu-id="17a3f-1038">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="17a3f-1039">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="17a3f-1039">Az.DataLakeStore</span></span>
* <span data-ttu-id="17a3f-1040">Uppdatera ADLS-sdk för att använda httpclient, integrera dataplanstestning med Azure-ramverk</span><span class="sxs-lookup"><span data-stu-id="17a3f-1040">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="17a3f-1041">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="17a3f-1041">Az.Monitor</span></span>
* <span data-ttu-id="17a3f-1042">Korrigera felaktiga parameternamn i hjälpexempel</span><span class="sxs-lookup"><span data-stu-id="17a3f-1042">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="17a3f-1043">Az.Network</span><span class="sxs-lookup"><span data-stu-id="17a3f-1043">Az.Network</span></span>
* <span data-ttu-id="17a3f-1044">Lägg till flaggan DisableBgpRoutePropagation i utdata för effektiv routningstabell</span><span class="sxs-lookup"><span data-stu-id="17a3f-1044">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="17a3f-1045">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="17a3f-1045">Updated cmdlet:</span></span>
        - <span data-ttu-id="17a3f-1046">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="17a3f-1046">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="17a3f-1047">Åtgärda dubbelstreck i dokumentationen New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="17a3f-1047">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="17a3f-1048">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="17a3f-1048">Az.Resources</span></span>
* <span data-ttu-id="17a3f-1049">Lägg till ny cmdlet Get-AzureRmDenyAssignment för att hämta tilldelningsnekanden</span><span class="sxs-lookup"><span data-stu-id="17a3f-1049">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="17a3f-1050">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="17a3f-1050">Az.Sql</span></span>
* <span data-ttu-id="17a3f-1051">Döp om Advanced Threat Protection-cmdletar för Advanced Data Security och aktivera Vulnerability Assessment som standard</span><span class="sxs-lookup"><span data-stu-id="17a3f-1051">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="17a3f-1052">2.0.0 – maj 2019</span><span class="sxs-lookup"><span data-stu-id="17a3f-1052">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="17a3f-1053">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="17a3f-1053">Az.Accounts</span></span>
* <span data-ttu-id="17a3f-1054">Uppdatera autentiseringsbiblioteket för att åtgärda ADFS-problem med autentisering av användarnamn/lösenord</span><span class="sxs-lookup"><span data-stu-id="17a3f-1054">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="17a3f-1055">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="17a3f-1055">Az.CognitiveServices</span></span>
* <span data-ttu-id="17a3f-1056">Visa endast Bing-ansvarsfriskrivning för Bing-sökningstjänster.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1056">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="17a3f-1057">Förbättra felmeddelande när det inte går att skapa konton.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1057">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="17a3f-1058">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="17a3f-1058">Az.Compute</span></span>
* <span data-ttu-id="17a3f-1059">Funktion för närhetsplaceringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1059">Proximity placement group feature.</span></span>
    - <span data-ttu-id="17a3f-1060">Följande nya cmdletar har lagts till:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="17a3f-1060">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="17a3f-1061">Den nya parametern ProximityPlacementGroupId har lagts till i följande cmdletar:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="17a3f-1061">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="17a3f-1062">Parametern StorageAccountType har lagts till i New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1062">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="17a3f-1063">TargetRegion för New-AzGalleryImageVersion kan innehålla StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1063">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="17a3f-1064">Växlingsparametern SkipShutdown har lagts till i Stop-AzVM och Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="17a3f-1064">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="17a3f-1065">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="17a3f-1065">Breaking changes</span></span>
    - <span data-ttu-id="17a3f-1066">Set-AzVMBootDiagnostics har ändrats till Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1066">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="17a3f-1067">Export-AzLogAnalyticThrottledRequests har ändrats till Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1067">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="17a3f-1068">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="17a3f-1068">Az.DeploymentManager</span></span>
* <span data-ttu-id="17a3f-1069">De första allmänt tillgängliga versionerna av cmdletar för Distributionshanteraren i Azure</span><span class="sxs-lookup"><span data-stu-id="17a3f-1069">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="17a3f-1070">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="17a3f-1070">Az.Dns</span></span>
* <span data-ttu-id="17a3f-1071">Automatisk delegering av DNS för NameServer</span><span class="sxs-lookup"><span data-stu-id="17a3f-1071">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="17a3f-1072">Det överordnade zonnamnet kan användas som ytterligare valfri parameter i cmdleten för att skapa DNS-zoner.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1072">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="17a3f-1073">Lägger till NS-poster för en nyligen skapad underordnad zon i den överordnade zonen.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1073">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="17a3f-1074">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="17a3f-1074">Az.FrontDoor</span></span>
* <span data-ttu-id="17a3f-1075">De första allmänt tillgängliga versionerna av cmdletar för Azure FrontDoor</span><span class="sxs-lookup"><span data-stu-id="17a3f-1075">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="17a3f-1076">Byt namn på WAF-cmdletar så att de omfattar ”Waf”</span><span class="sxs-lookup"><span data-stu-id="17a3f-1076">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="17a3f-1077">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="17a3f-1077">Az.HDInsight</span></span>
* <span data-ttu-id="17a3f-1078">Två cmdletar har tagits bort:</span><span class="sxs-lookup"><span data-stu-id="17a3f-1078">Removed two cmdlets:</span></span>
    - <span data-ttu-id="17a3f-1079">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="17a3f-1079">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="17a3f-1080">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="17a3f-1080">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="17a3f-1081">En ny cmdlet har lagts till, Set-AzHDInsightGatewayCredential, som ersätter Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="17a3f-1081">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="17a3f-1082">Uppdatera cmdleten Get-AzHDInsightJobOutput för att skilja mellan läsarrollen och HDInsight-operatörsrollen:</span><span class="sxs-lookup"><span data-stu-id="17a3f-1082">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="17a3f-1083">Användare med läsarrollen måste uttryckligen ange parametern ”DefaultStorageAccountKey”, annars uppstår fel.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1083">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="17a3f-1084">Användare med HDInsight-operatörsrollen påverkas inte.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1084">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="17a3f-1085">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="17a3f-1085">Az.Monitor</span></span>
* <span data-ttu-id="17a3f-1086">Nya cmdletar för SQR API (schemalagd frågeregel)</span><span class="sxs-lookup"><span data-stu-id="17a3f-1086">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="17a3f-1087">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="17a3f-1087">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="17a3f-1088">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="17a3f-1088">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="17a3f-1089">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="17a3f-1089">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="17a3f-1090">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="17a3f-1090">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="17a3f-1091">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="17a3f-1091">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="17a3f-1092">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="17a3f-1092">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="17a3f-1093">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="17a3f-1093">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="17a3f-1094">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="17a3f-1094">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="17a3f-1095">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="17a3f-1095">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="17a3f-1096">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="17a3f-1096">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="17a3f-1097">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="17a3f-1097">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="17a3f-1098">[Mer](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information om SQR API</span><span class="sxs-lookup"><span data-stu-id="17a3f-1098">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="17a3f-1099">Az.Monitor.md har uppdaterats för att omfatta cmdletar för måttbaserade aviseringsregler i GenV2 (inte klassiska)</span><span class="sxs-lookup"><span data-stu-id="17a3f-1099">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="17a3f-1100">Az.Network</span><span class="sxs-lookup"><span data-stu-id="17a3f-1100">Az.Network</span></span>
* <span data-ttu-id="17a3f-1101">Lägg till stöd för NAT Gateway-resurs</span><span class="sxs-lookup"><span data-stu-id="17a3f-1101">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="17a3f-1102">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="17a3f-1102">New cmdlets</span></span>
        - <span data-ttu-id="17a3f-1103">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="17a3f-1103">New-AzNatGateway</span></span>
        - <span data-ttu-id="17a3f-1104">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="17a3f-1104">Get-AzNatGateway</span></span>
        - <span data-ttu-id="17a3f-1105">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="17a3f-1105">Set-AzNatGateway</span></span>
        - <span data-ttu-id="17a3f-1106">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="17a3f-1106">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="17a3f-1107">Uppdaterade cmdletar</span><span class="sxs-lookup"><span data-stu-id="17a3f-1107">Updated cmdlets</span></span>
        - <span data-ttu-id="17a3f-1108">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="17a3f-1108">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="17a3f-1109">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="17a3f-1109">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="17a3f-1110">Nedanstående kommandon för funktionen har uppdaterats: Ange/ta bort anpassade vägar på Brooklyn Gateway.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1110">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="17a3f-1111">New-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ställa in adressprefix som anpassade vägar för att ange gateway.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1111">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="17a3f-1112">Set-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ange adressprefix som anpassade vägar för att ange gateway.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1112">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="17a3f-1113">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="17a3f-1113">Az.PolicyInsights</span></span>
* <span data-ttu-id="17a3f-1114">Stöd för att fråga efter information om principutvärdering.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1114">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="17a3f-1115">Lägg till parametern ”-Expand” för Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1115">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="17a3f-1116">Stöd för -Expand PolicyEvaluationDetails.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1116">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="17a3f-1117">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="17a3f-1117">Az.RecoveryServices</span></span>
* <span data-ttu-id="17a3f-1118">Stöd för att dela prenumeration mellan Azure och Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1118">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="17a3f-1119">Markering av kommande icke-bakåtkompatibla ändringar för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1119">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="17a3f-1120">Korrigering för återställningsplan och åtgärdsplan i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1120">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="17a3f-1121">Korrigering för mappning av uppdateringsnätverk i Azure Site Recovery för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1121">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="17a3f-1122">Korrigering för instruktioner för uppdateringsskydd i Azure Site Recovery för Azure till Azure för hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1122">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="17a3f-1123">Andra mindre korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1123">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="17a3f-1124">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="17a3f-1124">Az.Relay</span></span>
* <span data-ttu-id="17a3f-1125">Korrigera stavfel i kundriktade meddelanden</span><span class="sxs-lookup"><span data-stu-id="17a3f-1125">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="17a3f-1126">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="17a3f-1126">Az.ServiceBus</span></span>
* <span data-ttu-id="17a3f-1127">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="17a3f-1127">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="17a3f-1128">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="17a3f-1128">Az.Storage</span></span>
* <span data-ttu-id="17a3f-1129">Uppgradera till lagringsklientbiblioteket 10.0.1 (namnområdet för alla objekt från detta SDK ändras från ”Microsoft.WindowsAzure.Storage. *till ”Microsoft.Azure.Storage.* ”)</span><span class="sxs-lookup"><span data-stu-id="17a3f-1129">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="17a3f-1130">Uppgradera till Microsoft.Azure.Management.Storage 11.0.0 för att stödja den nya API-versionen 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1130">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="17a3f-1131">Standardlagringskontot i Skapa lagringskonto ändras från ”Storage” till ”StorageV2”</span><span class="sxs-lookup"><span data-stu-id="17a3f-1131">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="17a3f-1132">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="17a3f-1132">New-AzStorageAccount</span></span>
* <span data-ttu-id="17a3f-1133">Ändra lagringskontots cmdlet-utdata Sku.Name för att passa med indata-SkuName genom att lägga till ”-”. Till exempel ändras ”StandardLRS” till ”Standard_LRS”</span><span class="sxs-lookup"><span data-stu-id="17a3f-1133">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="17a3f-1134">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="17a3f-1134">New-AzStorageAccount</span></span>
    - <span data-ttu-id="17a3f-1135">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="17a3f-1135">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="17a3f-1136">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="17a3f-1136">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="17a3f-1137">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="17a3f-1137">Az.Websites</span></span>
* <span data-ttu-id="17a3f-1138">Egenskapen ”typ” konfigureras nu för PSSite-objekt som returneras av Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="17a3f-1138">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="17a3f-1139">Get-AzWebApp\*Metrics och Get-AzAppServicePlanMetrics markeras som inaktuella</span><span class="sxs-lookup"><span data-stu-id="17a3f-1139">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="17a3f-1140">1.8.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="17a3f-1140">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="17a3f-1141">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="17a3f-1141">Highlights since the last major release</span></span>
* <span data-ttu-id="17a3f-1142">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="17a3f-1142">General availability of `Az` module</span></span>
* <span data-ttu-id="17a3f-1143">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="17a3f-1143">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="17a3f-1144">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="17a3f-1144">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="17a3f-1145">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="17a3f-1145">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="17a3f-1146">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="17a3f-1146">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="17a3f-1147">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="17a3f-1147">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="17a3f-1148">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="17a3f-1148">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="17a3f-1149">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="17a3f-1149">Az.Accounts</span></span>
* <span data-ttu-id="17a3f-1150">Uppdatera Uninstall-AzureRm för att ta bort moduler i Mac på ett korrekt sätt</span><span class="sxs-lookup"><span data-stu-id="17a3f-1150">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="17a3f-1151">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="17a3f-1151">Az.Batch</span></span>
* <span data-ttu-id="17a3f-1152">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1152">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="17a3f-1153">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="17a3f-1153">Az.Cdn</span></span>
* <span data-ttu-id="17a3f-1154">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1154">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="17a3f-1155">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="17a3f-1155">Az.CognitiveServices</span></span>
* <span data-ttu-id="17a3f-1156">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1156">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="17a3f-1157">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="17a3f-1157">Az.Compute</span></span>
* <span data-ttu-id="17a3f-1158">Åtgärda problem med AEM-installationen om resurs-ID:n för diskar innehåller resourcegroups i gemener i resurs-ID:n</span><span class="sxs-lookup"><span data-stu-id="17a3f-1158">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="17a3f-1159">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1159">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="17a3f-1160">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="17a3f-1160">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="17a3f-1161">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="17a3f-1161">Az.DataFactory</span></span>
* <span data-ttu-id="17a3f-1162">Lägg till SsisProperties om NodeCount inte är null för hanterad integreringskörning.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1162">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="17a3f-1163">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="17a3f-1163">Az.DataLakeStore</span></span>
* <span data-ttu-id="17a3f-1164">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1164">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="17a3f-1165">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="17a3f-1165">Az.EventGrid</span></span>
* <span data-ttu-id="17a3f-1166">Hjälptexten för slutpunkten har uppdaterats för att visa att resurser ska skapas innan cmdletarna för att skapa/uppdatera händelseprenumerationer används.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1166">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="17a3f-1167">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="17a3f-1167">Az.EventHub</span></span>
* <span data-ttu-id="17a3f-1168">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="17a3f-1168">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="17a3f-1169">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="17a3f-1169">Az.HDInsight</span></span>
* <span data-ttu-id="17a3f-1170">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1170">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="17a3f-1171">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="17a3f-1171">Az.IotHub</span></span>
* <span data-ttu-id="17a3f-1172">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1172">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="17a3f-1173">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="17a3f-1173">Az.KeyVault</span></span>
* <span data-ttu-id="17a3f-1174">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1174">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="17a3f-1175">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="17a3f-1175">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="17a3f-1176">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="17a3f-1176">Az.MachineLearning</span></span>
* <span data-ttu-id="17a3f-1177">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1177">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="17a3f-1178">Az.Media</span><span class="sxs-lookup"><span data-stu-id="17a3f-1178">Az.Media</span></span>
* <span data-ttu-id="17a3f-1179">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1179">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="17a3f-1180">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="17a3f-1180">Az.Monitor</span></span>
  * <span data-ttu-id="17a3f-1181">Nya cmdletar för måttbaserad aviseringsregel i GenV2 (inte klassisk)</span><span class="sxs-lookup"><span data-stu-id="17a3f-1181">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="17a3f-1182">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="17a3f-1182">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="17a3f-1183">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="17a3f-1183">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="17a3f-1184">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="17a3f-1184">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="17a3f-1185">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="17a3f-1185">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="17a3f-1186">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="17a3f-1186">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="17a3f-1187">Monitor SDK har uppdaterats till version 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="17a3f-1187">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="17a3f-1188">Az.Network</span><span class="sxs-lookup"><span data-stu-id="17a3f-1188">Az.Network</span></span>
* <span data-ttu-id="17a3f-1189">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1189">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="17a3f-1190">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="17a3f-1190">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="17a3f-1191">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="17a3f-1191">Az.NotificationHubs</span></span>
* <span data-ttu-id="17a3f-1192">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1192">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="17a3f-1193">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="17a3f-1193">Az.OperationalInsights</span></span>
* <span data-ttu-id="17a3f-1194">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1194">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="17a3f-1195">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="17a3f-1195">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="17a3f-1196">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1196">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="17a3f-1197">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="17a3f-1197">Az.RecoveryServices</span></span>
* <span data-ttu-id="17a3f-1198">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1198">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="17a3f-1199">Tabellformatet för SQL i virtuella Azure-datorer har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="17a3f-1199">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="17a3f-1200">En alternativ metod för att hämta platser i AzureFileShare har lagts till</span><span class="sxs-lookup"><span data-stu-id="17a3f-1200">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="17a3f-1201">ScheduleRunDays i SchedulePolicy-objekt har uppdaterats enligt tidszon</span><span class="sxs-lookup"><span data-stu-id="17a3f-1201">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="17a3f-1202">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="17a3f-1202">Az.RedisCache</span></span>
* <span data-ttu-id="17a3f-1203">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1203">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="17a3f-1204">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="17a3f-1204">Az.Resources</span></span>
* <span data-ttu-id="17a3f-1205">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="17a3f-1205">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="17a3f-1206">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="17a3f-1206">Az.Sql</span></span>
* <span data-ttu-id="17a3f-1207">Ersätt Monitor SDK-beroende med vanlig kod</span><span class="sxs-lookup"><span data-stu-id="17a3f-1207">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="17a3f-1208">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1208">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="17a3f-1209">Förbättrad process för klassificering av flera kolumner.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1209">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="17a3f-1210">Inkludera SKU-egenskaper (SKU-namn, serie, kapacitet) i svaret från Get-AzSqlServerServiceObjective och formatera som tabell som standard.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1210">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="17a3f-1211">Möjlighet att använda Get-AzSqlServerServiceObjective efter plats utan att behöva en redan befintlig server i regionen.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1211">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="17a3f-1212">Stöd för tidszonsparametern när hanterade instanser skapas.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1212">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="17a3f-1213">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="17a3f-1213">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="17a3f-1214">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="17a3f-1214">Az.Websites</span></span>
* <span data-ttu-id="17a3f-1215">åtgärdar Set-AzWebApp och Set-AzWebAppSlot så att de inte tar bort taggar vid körning</span><span class="sxs-lookup"><span data-stu-id="17a3f-1215">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="17a3f-1216">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1216">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="17a3f-1217">SDK för WebSites har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1217">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="17a3f-1218">Egenskapen AdminSiteName har tagits bort från PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1218">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="17a3f-1219">1.7.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="17a3f-1219">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="17a3f-1220">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="17a3f-1220">Highlights since the last major release</span></span>
* <span data-ttu-id="17a3f-1221">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="17a3f-1221">General availability of `Az` module</span></span>
* <span data-ttu-id="17a3f-1222">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="17a3f-1222">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="17a3f-1223">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="17a3f-1223">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="17a3f-1224">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="17a3f-1224">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="17a3f-1225">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="17a3f-1225">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="17a3f-1226">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="17a3f-1226">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="17a3f-1227">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="17a3f-1227">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="17a3f-1228">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="17a3f-1228">Az.Accounts</span></span>
* <span data-ttu-id="17a3f-1229">Add-AzEnvironment och Set-AzEnvironment har uppdaterats för att godkänna parametern AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="17a3f-1229">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="17a3f-1230">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="17a3f-1230">Az.AnalysisServices</span></span>
* <span data-ttu-id="17a3f-1231">ServiceClient används i cmdletar för dataplan och den ursprungliga autentiseringslogiken har tagits bort</span><span class="sxs-lookup"><span data-stu-id="17a3f-1231">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="17a3f-1232">Add-AzureASAccount används för omslutning av Connect-AzAccount för att undvika en icke-bakåtkompatibel ändring</span><span class="sxs-lookup"><span data-stu-id="17a3f-1232">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="17a3f-1233">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="17a3f-1233">Az.Automation</span></span>
* <span data-ttu-id="17a3f-1234">Buggen för cmdleten New-AzAutomationSoftwareUpdateConfiguration för inkluderingar har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1234">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="17a3f-1235">Nu bör parametern IncludedKbNumber och IncludedPackageNameMask fungera.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1235">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="17a3f-1236">Felkorrigering för dynamiska grupper i uppdateringshanteringen för azure automation</span><span class="sxs-lookup"><span data-stu-id="17a3f-1236">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="17a3f-1237">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="17a3f-1237">Az.Compute</span></span>
* <span data-ttu-id="17a3f-1238">Lägg till parametern HyperVGeneration i New-AzDiskConfig och New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="17a3f-1238">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="17a3f-1239">Tillåt att virtuella datorer skapas med galleribilder från andra klientorganisationer.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1239">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="17a3f-1240">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="17a3f-1240">Az.ContainerInstance</span></span>
* <span data-ttu-id="17a3f-1241">Ett problem har åtgärdats i parametern -Command för New-AzContainerGroup som lade till ett avslutande tomt argument</span><span class="sxs-lookup"><span data-stu-id="17a3f-1241">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="17a3f-1242">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="17a3f-1242">Az.DataFactory</span></span>
* <span data-ttu-id="17a3f-1243">ADF .Net SDK-versionen har uppdaterats till 3.0.2</span><span class="sxs-lookup"><span data-stu-id="17a3f-1243">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="17a3f-1244">Cmdleten Set-AzDataFactoryV2 har uppdaterats med extra parametrar för inställningar som rör RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1244">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="17a3f-1245">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="17a3f-1245">Az.Resources</span></span>
* <span data-ttu-id="17a3f-1246">Förbättra hanteringen av providrar för Get-AzResource när parametrarna -ResourceId eller -ResourceGroupName, -Name och -ResourceType tillhandahålls</span><span class="sxs-lookup"><span data-stu-id="17a3f-1246">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="17a3f-1247">Förbättra felhanteringen för ”Test-AzDeployment” och ”Test-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="17a3f-1247">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="17a3f-1248">Hantera fel utanför distributionsvalideringen och ta med dem i kommandoutdata istället</span><span class="sxs-lookup"><span data-stu-id="17a3f-1248">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="17a3f-1249">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="17a3f-1249">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="17a3f-1250">Lägg till växlingsparametern -IgnoreDynamicParameters till en uppsättning av cmdletar för distribution för att hoppa över fråga i skript och jobbscenarier</span><span class="sxs-lookup"><span data-stu-id="17a3f-1250">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="17a3f-1251">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="17a3f-1251">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="17a3f-1252">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="17a3f-1252">Az.Sql</span></span>
* <span data-ttu-id="17a3f-1253">Stöd för dataklassificering av databaser.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1253">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="17a3f-1254">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="17a3f-1254">Az.Storage</span></span>
* <span data-ttu-id="17a3f-1255">Rapportera detaljfel när lagringskontext skapas med parametern -UseConnectedAccount, men utan inloggning på Azure-kontot</span><span class="sxs-lookup"><span data-stu-id="17a3f-1255">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="17a3f-1256">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="17a3f-1256">New-AzStorageContext</span></span>
* <span data-ttu-id="17a3f-1257">Stöd för att hantera Blob Service-egenskaper för ett angivet lagringskonto med API:et för hanteringsplan</span><span class="sxs-lookup"><span data-stu-id="17a3f-1257">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="17a3f-1258">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="17a3f-1258">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="17a3f-1259">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="17a3f-1259">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="17a3f-1260">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="17a3f-1260">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="17a3f-1261">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="17a3f-1261">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="17a3f-1262">Stöd för -AsJob-cmdletar för att ladda upp och ladda ned blobar och filer</span><span class="sxs-lookup"><span data-stu-id="17a3f-1262">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="17a3f-1263">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="17a3f-1263">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="17a3f-1264">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="17a3f-1264">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="17a3f-1265">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="17a3f-1265">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="17a3f-1266">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="17a3f-1266">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="17a3f-1267">1.6.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="17a3f-1267">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="17a3f-1268">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="17a3f-1268">Highlights since the last major release</span></span>
* <span data-ttu-id="17a3f-1269">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="17a3f-1269">General availability of `Az` module</span></span>
* <span data-ttu-id="17a3f-1270">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="17a3f-1270">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="17a3f-1271">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="17a3f-1271">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="17a3f-1272">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="17a3f-1272">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="17a3f-1273">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="17a3f-1273">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="17a3f-1274">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="17a3f-1274">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="17a3f-1275">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="17a3f-1275">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="17a3f-1276">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="17a3f-1276">Az.Automation</span></span>
* <span data-ttu-id="17a3f-1277">Azure Automation – ändring av uppdateringshantering för stöd för de nya funktionerna:</span><span class="sxs-lookup"><span data-stu-id="17a3f-1277">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="17a3f-1278">Dynamisk gruppering</span><span class="sxs-lookup"><span data-stu-id="17a3f-1278">Dynamic grouping</span></span>
    * <span data-ttu-id="17a3f-1279">För-/efterskrift</span><span class="sxs-lookup"><span data-stu-id="17a3f-1279">Pre-Post script</span></span>
    * <span data-ttu-id="17a3f-1280">Inställning för omstart</span><span class="sxs-lookup"><span data-stu-id="17a3f-1280">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="17a3f-1281">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="17a3f-1281">Az.Compute</span></span>
* <span data-ttu-id="17a3f-1282">Åtgärda problem med sökvägsmatchning i Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="17a3f-1282">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="17a3f-1283">Uppdatera Compute-klientbibliotek till 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1283">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="17a3f-1284">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="17a3f-1284">Az.KeyVault</span></span>
* <span data-ttu-id="17a3f-1285">Stöd för jokertecken för KeyVault-cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="17a3f-1285">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="17a3f-1286">Az.Network</span><span class="sxs-lookup"><span data-stu-id="17a3f-1286">Az.Network</span></span>
* <span data-ttu-id="17a3f-1287">Lägg till stöd för Threat Intelligence för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="17a3f-1287">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="17a3f-1288">Lägg till resurs för brandväggsprincip på översta nivå och anpassade regler för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="17a3f-1288">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="17a3f-1289">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="17a3f-1289">Az.RecoveryServices</span></span>
* <span data-ttu-id="17a3f-1290">SnapshotRetentionInDays har lagts till i Azure-principen för virtuella datorer för stöd av Instant RP</span><span class="sxs-lookup"><span data-stu-id="17a3f-1290">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="17a3f-1291">Pipe-stöd för avregistrering av container har lagts till</span><span class="sxs-lookup"><span data-stu-id="17a3f-1291">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="17a3f-1292">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="17a3f-1292">Az.Resources</span></span>
* <span data-ttu-id="17a3f-1293">Uppdatera stöd för jokertecken för Get-AzResource och Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="17a3f-1293">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="17a3f-1294">Uppdatera autentiseringsuppgifter som används vid allmänna anrop till ARM</span><span class="sxs-lookup"><span data-stu-id="17a3f-1294">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="17a3f-1295">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="17a3f-1295">Az.Sql</span></span>
* <span data-ttu-id="17a3f-1296">Cmdlet-parametern (ExcludeDetectionType) för Hotidentifiering ändrades från DetectionType till sträng[] för att framtidssäkra den när nya DetectionTypes läggs till, och även för att stödja automatisk ifyllning.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1296">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="17a3f-1297">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="17a3f-1297">Az.Storage</span></span>
* <span data-ttu-id="17a3f-1298">Stöd för att hämta/ange/ta bort hanteringsprincip på ett lagringskonto</span><span class="sxs-lookup"><span data-stu-id="17a3f-1298">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="17a3f-1299">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="17a3f-1299">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="17a3f-1300">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="17a3f-1300">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="17a3f-1301">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="17a3f-1301">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="17a3f-1302">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="17a3f-1302">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="17a3f-1303">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="17a3f-1303">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="17a3f-1304">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="17a3f-1304">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="17a3f-1305">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="17a3f-1305">Az.Websites</span></span>
* <span data-ttu-id="17a3f-1306">Åtgärda fel med ARM-mall som avbryter kloning av alla platser med 'New-AzWebApp -IncludeSourceWebAppSlots'</span><span class="sxs-lookup"><span data-stu-id="17a3f-1306">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="17a3f-1307">1.5.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="17a3f-1307">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="17a3f-1308">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="17a3f-1308">Az.Accounts</span></span>
* <span data-ttu-id="17a3f-1309">Lägg till kommandot Register-AzModule för stöd för AutoRest-genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="17a3f-1309">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="17a3f-1310">Uppdatera exempel för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="17a3f-1310">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="17a3f-1311">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="17a3f-1311">Az.Automation</span></span>
* <span data-ttu-id="17a3f-1312">Problem med att hämta vissa månadsscheman i flera Azure Automation-cmdletar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="17a3f-1312">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="17a3f-1313">Åtgärda problem med att Get-AzAutomationDscNode bara returnerar de 20 översta noderna.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1313">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="17a3f-1314">Nu returneras alla noder</span><span class="sxs-lookup"><span data-stu-id="17a3f-1314">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="17a3f-1315">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="17a3f-1315">Az.Cdn</span></span>
* <span data-ttu-id="17a3f-1316">Nya Powershell-cmdletar för att aktivera/inaktivera anpassade domän-HTTPS har lagts till och de gamla har gjorts inaktuella</span><span class="sxs-lookup"><span data-stu-id="17a3f-1316">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="17a3f-1317">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="17a3f-1317">Az.Compute</span></span>
* <span data-ttu-id="17a3f-1318">Lägg till stöd för jokertecken för Get-cmdletar</span><span class="sxs-lookup"><span data-stu-id="17a3f-1318">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="17a3f-1319">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="17a3f-1319">Az.DataFactory</span></span>
* <span data-ttu-id="17a3f-1320">ADF .Net SDK-versionen har uppdaterats till 3.0.1</span><span class="sxs-lookup"><span data-stu-id="17a3f-1320">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="17a3f-1321">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="17a3f-1321">Az.LogicApp</span></span>
* <span data-ttu-id="17a3f-1322">Åtgärda problemet med att ListWorkflows endast hämtar den första sidan med resultat</span><span class="sxs-lookup"><span data-stu-id="17a3f-1322">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="17a3f-1323">Az.Network</span><span class="sxs-lookup"><span data-stu-id="17a3f-1323">Az.Network</span></span>
* <span data-ttu-id="17a3f-1324">Lägg till stöd för jokertecken för Network-cmdletar</span><span class="sxs-lookup"><span data-stu-id="17a3f-1324">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="17a3f-1325">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="17a3f-1325">Az.RecoveryServices</span></span>
* <span data-ttu-id="17a3f-1326">Stöd har lagts till för SQL Server i virtuella Azure-datorer</span><span class="sxs-lookup"><span data-stu-id="17a3f-1326">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="17a3f-1327">SDK-uppdatering</span><span class="sxs-lookup"><span data-stu-id="17a3f-1327">SDK Update</span></span>
* <span data-ttu-id="17a3f-1328">Get-ProtectableItem-incheckning i VMappContainer har tagits bort</span><span class="sxs-lookup"><span data-stu-id="17a3f-1328">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="17a3f-1329">Name och ServerName har lagts till som parametrar för Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="17a3f-1329">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="17a3f-1330">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="17a3f-1330">Az.Resources</span></span>
* <span data-ttu-id="17a3f-1331">Lägg till parametern `-TemplateObject` i cmdletar för distribution</span><span class="sxs-lookup"><span data-stu-id="17a3f-1331">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="17a3f-1332">Mer information här: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="17a3f-1332">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="17a3f-1333">Åtgärda problem med piping av resultatet i `Get-AzResource` till `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="17a3f-1333">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="17a3f-1334">Mer information här: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="17a3f-1334">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="17a3f-1335">Åtgärda problem med ändring av JSON-datatyp när `Set-AzResource` körs</span><span class="sxs-lookup"><span data-stu-id="17a3f-1335">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="17a3f-1336">Mer information här: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="17a3f-1336">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="17a3f-1337">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="17a3f-1337">Az.Sql</span></span>
* <span data-ttu-id="17a3f-1338">AuditingEndpointsCommunicator uppdateras.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1338">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="17a3f-1339">Åtgärdar beteendet hos ett gränsscenario när nya diagnostikinställningar skapas.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1339">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="17a3f-1340">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="17a3f-1340">Az.Storage</span></span>
* <span data-ttu-id="17a3f-1341">Stöd för BlockBlobStorage när Storage-konto skapas      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="17a3f-1341">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="17a3f-1342">1.4.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="17a3f-1342">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="17a3f-1343">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="17a3f-1343">Az.AnalysisServices</span></span>
* <span data-ttu-id="17a3f-1344">Inaktuell AddAzureASAccount-cmdlet</span><span class="sxs-lookup"><span data-stu-id="17a3f-1344">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="17a3f-1345">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="17a3f-1345">Az.Automation</span></span>
* <span data-ttu-id="17a3f-1346">Hjälpen för Import-AzAutomationDscNodeConfiguration har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="17a3f-1346">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="17a3f-1347">Konfigurationsnamnsvalidering har lagts till i cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="17a3f-1347">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="17a3f-1348">Förbättrad felhantering för cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="17a3f-1348">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="17a3f-1349">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="17a3f-1349">Az.CognitiveServices</span></span>
* <span data-ttu-id="17a3f-1350">CustomSubdomainName har lagts till som en ny valfri parameter för New-AzCognitiveServicesAccount, som används för att ange underdomän för resursen.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1350">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="17a3f-1351">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="17a3f-1351">Az.Compute</span></span>
* <span data-ttu-id="17a3f-1352">Problemet med ID-parameteruppsättningar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="17a3f-1352">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="17a3f-1353">Get-AzVMExtension har uppdaterats så att alla installerade tillägg visas om parametern Name inte har angetts</span><span class="sxs-lookup"><span data-stu-id="17a3f-1353">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="17a3f-1354">Parametrarna Tag och ResourceId har lagts till i cmdleten Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="17a3f-1354">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="17a3f-1355">Get-AzVmssVM utan instans-ID och med InstanceView kan visa virtuella VMSS-datorer med instansvyn.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1355">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="17a3f-1356">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="17a3f-1356">Az.DataLakeStore</span></span>
* <span data-ttu-id="17a3f-1357">Cmdletar har lagts till för uppräkning och återställning av borttagna objekt i ADL</span><span class="sxs-lookup"><span data-stu-id="17a3f-1357">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="17a3f-1358">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="17a3f-1358">Az.EventHub</span></span>
* <span data-ttu-id="17a3f-1359">Ny boolesk egenskap SkipEmptyArchives har lagts till i Skip Empty Archives i CaptureDescription-klassen i Eventhub</span><span class="sxs-lookup"><span data-stu-id="17a3f-1359">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="17a3f-1360">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="17a3f-1360">Az.KeyVault</span></span>
* <span data-ttu-id="17a3f-1361">Taggning i Set-AzKeyVaultSecret har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="17a3f-1361">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="17a3f-1362">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="17a3f-1362">Az.LogicApp</span></span>
* <span data-ttu-id="17a3f-1363">Grundläggande SKU har lagts till för Integrationskonton</span><span class="sxs-lookup"><span data-stu-id="17a3f-1363">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="17a3f-1364">XSLT 2.0, XSLT 3.0 och Flytande mappningstyper har lagts till</span><span class="sxs-lookup"><span data-stu-id="17a3f-1364">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="17a3f-1365">Nya cmdletar för integrationskontosammansättningar</span><span class="sxs-lookup"><span data-stu-id="17a3f-1365">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="17a3f-1366">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="17a3f-1366">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="17a3f-1367">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="17a3f-1367">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="17a3f-1368">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="17a3f-1368">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="17a3f-1369">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="17a3f-1369">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="17a3f-1370">Nya cmdletar för batchkonfiguration för integrationskonto</span><span class="sxs-lookup"><span data-stu-id="17a3f-1370">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="17a3f-1371">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="17a3f-1371">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="17a3f-1372">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="17a3f-1372">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="17a3f-1373">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="17a3f-1373">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="17a3f-1374">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="17a3f-1374">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="17a3f-1375">Logic App-SDK har uppdaterats till version 4.1.0</span><span class="sxs-lookup"><span data-stu-id="17a3f-1375">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="17a3f-1376">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="17a3f-1376">Az.Monitor</span></span>
* <span data-ttu-id="17a3f-1377">Hjälpen för Get-AzMetric har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="17a3f-1377">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="17a3f-1378">Az.Network</span><span class="sxs-lookup"><span data-stu-id="17a3f-1378">Az.Network</span></span>
* <span data-ttu-id="17a3f-1379">Hjälpexempel för Add-AzApplicationGatewayCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="17a3f-1379">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="17a3f-1380">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="17a3f-1380">Az.OperationalInsights</span></span>
* <span data-ttu-id="17a3f-1381">Ytterligare stöd för datakällorna New och Get ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1381">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="17a3f-1382">Ny ApplicationInsights-typ har lagts till för att ge stöd för ”Get specific” och ”Get all” för ApplicationInsights-datakällor för angiven arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1382">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="17a3f-1383">Cmdleten New-AzOperationalInsightsApplicationInsightsDataSource har lagts till för att skapa datakälla med angivna parametrar för Application Insights-resurs: subscription Id, resourceGroupName och name.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1383">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="17a3f-1384">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="17a3f-1384">Az.Resources</span></span>
* <span data-ttu-id="17a3f-1385">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="17a3f-1385">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="17a3f-1386">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="17a3f-1386">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="17a3f-1387">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="17a3f-1387">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="17a3f-1388">Fel som gör att KeyCredentials inte kan skapas upprepade gånger har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="17a3f-1388">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="17a3f-1389">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="17a3f-1389">Az.Sql</span></span>
* <span data-ttu-id="17a3f-1390">Lägg till stöd för hyperskalanivån för SQL DB</span><span class="sxs-lookup"><span data-stu-id="17a3f-1390">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="17a3f-1391">Ett fel har åtgärdats där återställningen kunde misslyckas på grund av onödiga inställningsegenskaper i restore-förfrågan</span><span class="sxs-lookup"><span data-stu-id="17a3f-1391">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="17a3f-1392">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="17a3f-1392">Az.Websites</span></span>
* <span data-ttu-id="17a3f-1393">Rätt exempel i Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="17a3f-1393">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="17a3f-1394">1.3.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="17a3f-1394">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="17a3f-1395">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="17a3f-1395">Az.Accounts</span></span>
* <span data-ttu-id="17a3f-1396">Uppdatera till den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="17a3f-1396">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="17a3f-1397">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="17a3f-1397">Az.AnalysisServices</span></span>
<span data-ttu-id="17a3f-1398">Allmän tillgänglighet för Az.AnalysisServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1398">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="17a3f-1399">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="17a3f-1399">Az.Compute</span></span>
* <span data-ttu-id="17a3f-1400">AEM-tillägg: Lägg till stöd för UltraSSD-, P60-, P70- och P80-diskar</span><span class="sxs-lookup"><span data-stu-id="17a3f-1400">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="17a3f-1401">Uppdatera hjälpbeskrivning för Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="17a3f-1401">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="17a3f-1402">Uppdatera hjälpbeskrivning och exempel för Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="17a3f-1402">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="17a3f-1403">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="17a3f-1403">Az.RecoveryServices</span></span>
<span data-ttu-id="17a3f-1404">Allmän tillgänglighet för Az.RecoveryServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1404">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="17a3f-1405">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="17a3f-1405">Az.Resources</span></span>
* <span data-ttu-id="17a3f-1406">Korrigera taggar för resursgrupper</span><span class="sxs-lookup"><span data-stu-id="17a3f-1406">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="17a3f-1407">Mer information här: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="17a3f-1407">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="17a3f-1408">Åtgärda problem där `Get-AzureRmRoleAssignment` inte respekterar -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="17a3f-1408">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="17a3f-1409">Mer information här: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="17a3f-1409">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="17a3f-1410">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="17a3f-1410">Az.Sql</span></span>
* <span data-ttu-id="17a3f-1411">Lägga till Get/Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="17a3f-1411">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="17a3f-1412">Åtgärda problem där ett nullref-undantag uppstår när du kör SQL-cmdletar och inte är inloggad på ett Azure-konto</span><span class="sxs-lookup"><span data-stu-id="17a3f-1412">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="17a3f-1413">Åtgärda nullref-undantag i Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="17a3f-1413">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="17a3f-1414">1.2.1 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="17a3f-1414">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="17a3f-1415">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="17a3f-1415">Az.Accounts</span></span>
* <span data-ttu-id="17a3f-1416">Version med rätt version av autentisering</span><span class="sxs-lookup"><span data-stu-id="17a3f-1416">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="17a3f-1417">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="17a3f-1417">Az.AnalysisServices</span></span>
* <span data-ttu-id="17a3f-1418">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="17a3f-1418">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="17a3f-1419">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="17a3f-1419">Az.RecoveryServices</span></span>
* <span data-ttu-id="17a3f-1420">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="17a3f-1420">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="17a3f-1421">1.2.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="17a3f-1421">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="17a3f-1422">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="17a3f-1422">Az.Accounts</span></span>
* <span data-ttu-id="17a3f-1423">Lägga till interaktiv autentisering och autentisering med användarnamn/lösenord för endast Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="17a3f-1423">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="17a3f-1424">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="17a3f-1424">Update incorrect online help URLs</span></span>
* <span data-ttu-id="17a3f-1425">Lägga till varningsmeddelande i PS Core för Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="17a3f-1425">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="17a3f-1426">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="17a3f-1426">Az.Aks</span></span>
* <span data-ttu-id="17a3f-1427">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="17a3f-1427">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="17a3f-1428">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="17a3f-1428">Az.Automation</span></span>
* <span data-ttu-id="17a3f-1429">Stöd för Python 2-runbookflöden har lagts till</span><span class="sxs-lookup"><span data-stu-id="17a3f-1429">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="17a3f-1430">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="17a3f-1430">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="17a3f-1431">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="17a3f-1431">Az.Cdn</span></span>
* <span data-ttu-id="17a3f-1432">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="17a3f-1432">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="17a3f-1433">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="17a3f-1433">Az.Compute</span></span>
* <span data-ttu-id="17a3f-1434">Lägga till cmdleten Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="17a3f-1434">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="17a3f-1435">Lägga till TempDisk-parameter i Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="17a3f-1435">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="17a3f-1436">Korrigera varningsmeddelande för New-AzVM</span><span class="sxs-lookup"><span data-stu-id="17a3f-1436">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="17a3f-1437">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="17a3f-1437">Az.ContainerRegistry</span></span>
* <span data-ttu-id="17a3f-1438">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="17a3f-1438">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="17a3f-1439">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="17a3f-1439">Az.DataFactory</span></span>
* <span data-ttu-id="17a3f-1440">ADF .Net SDK-versionen har uppdaterats till 3.0.0</span><span class="sxs-lookup"><span data-stu-id="17a3f-1440">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="17a3f-1441">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="17a3f-1441">Az.DataLakeStore</span></span>
* <span data-ttu-id="17a3f-1442">Åtgärda problem med ADLS-slutpunkt vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="17a3f-1442">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="17a3f-1443">Mer information här: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="17a3f-1443">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="17a3f-1444">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="17a3f-1444">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="17a3f-1445">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="17a3f-1445">Az.IotHub</span></span>
* <span data-ttu-id="17a3f-1446">Lägga till kodningsformat i cmdleten Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1446">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="17a3f-1447">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="17a3f-1447">Az.KeyVault</span></span>
* <span data-ttu-id="17a3f-1448">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="17a3f-1448">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="17a3f-1449">Az.Network</span><span class="sxs-lookup"><span data-stu-id="17a3f-1449">Az.Network</span></span>
* <span data-ttu-id="17a3f-1450">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="17a3f-1450">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="17a3f-1451">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="17a3f-1451">Az.Resources</span></span>
* <span data-ttu-id="17a3f-1452">Åtgärda felaktiga exempel i referensdokumentationen ”New-AzADAppCredential” och ”New-AzADSpCredential”</span><span class="sxs-lookup"><span data-stu-id="17a3f-1452">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="17a3f-1453">Åtgärda problem där sökvägen för parametern ”-TemplateFile” inte omvandlas innan cmdletarna för distribution i resursgruppen körs</span><span class="sxs-lookup"><span data-stu-id="17a3f-1453">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="17a3f-1454">Az.Resources: Korrigera dokumentationen om standardvärdet för New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="17a3f-1454">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="17a3f-1455">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="17a3f-1455">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="17a3f-1456">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="17a3f-1456">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="17a3f-1457">Åtgärda formateringsproblemet med objektet ”PSResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="17a3f-1457">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="17a3f-1458">Mer information här: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="17a3f-1458">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="17a3f-1459">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="17a3f-1459">Az.ServiceFabric</span></span>
* <span data-ttu-id="17a3f-1460">Återställ när ett certifikat läggs till i en Virtual Machine Scale Sets-modell men ett undantag genereras. Detta har gjorts för att åtgärda följande fel: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="17a3f-1460">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="17a3f-1461">Korrigera några felmeddelanden.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1461">Fix some error messages.</span></span>
* <span data-ttu-id="17a3f-1462">Korrigering av skapande av kluster med ARM-mall som är standard för New-AzServiceFabriCluster som inte fungerade med migrering till Az.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1462">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="17a3f-1463">Korrigering av tilläggning av kluster/programcertifikat så att endast VM Scale Sets som motsvarar klustret läggs till genom att kontrollera ID för klustret i tillägget.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1463">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="17a3f-1464">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="17a3f-1464">Az.SignalR</span></span>
* <span data-ttu-id="17a3f-1465">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="17a3f-1465">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="17a3f-1466">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="17a3f-1466">Az.Sql</span></span>
* <span data-ttu-id="17a3f-1467">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="17a3f-1467">Update incorrect online help URLs</span></span>
* <span data-ttu-id="17a3f-1468">Uppdaterad parameterbeskrivning för LicenseType-parameter med möjliga värden</span><span class="sxs-lookup"><span data-stu-id="17a3f-1468">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="17a3f-1469">Korrigering för att uppdatera hanterad instansidentitet som inte fungerar när det är den enda uppdaterade egenskapen</span><span class="sxs-lookup"><span data-stu-id="17a3f-1469">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="17a3f-1470">Stöd för anpassad sortering på hanterad instans</span><span class="sxs-lookup"><span data-stu-id="17a3f-1470">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="17a3f-1471">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="17a3f-1471">Az.Storage</span></span>
* <span data-ttu-id="17a3f-1472">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="17a3f-1472">Update incorrect online help URLs</span></span>
* <span data-ttu-id="17a3f-1473">Tillhandahåll detaljerat felmeddelande när en användare försöker hämta/konfigurera klassisk loggning/mått på ett Premium Storage-konto eftersom Premium Storage-kontot inte har stöd för klassisk loggning/mått.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1473">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="17a3f-1474">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="17a3f-1474">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="17a3f-1475">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="17a3f-1475">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="17a3f-1476">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="17a3f-1476">Az.TrafficManager</span></span>
* <span data-ttu-id="17a3f-1477">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="17a3f-1477">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="17a3f-1478">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="17a3f-1478">Az.Websites</span></span>
* <span data-ttu-id="17a3f-1479">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="17a3f-1479">Update incorrect online help URLs</span></span>
* <span data-ttu-id="17a3f-1480">Korrigerar ”New-AzWebAppSSLBinding” så att certifikatet laddas upp till rätt resursgrupp och plats om appen finns i en ASE.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1480">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="17a3f-1481">Korrigerar ”New-AzWebAppSSLBinding” så att taggarna inte skrivs över på en bindning av ett SSL-certifikat till en app</span><span class="sxs-lookup"><span data-stu-id="17a3f-1481">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="17a3f-1482">1.1.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="17a3f-1482">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="17a3f-1483">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="17a3f-1483">Az.Accounts</span></span>
* <span data-ttu-id="17a3f-1484">Lade till omfattningen ”Lokal” till Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="17a3f-1484">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="17a3f-1485">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="17a3f-1485">Az.Compute</span></span>
* <span data-ttu-id="17a3f-1486">Namn är nu valfritt i ID-parametern för Restart/Start/Stop/Remove/Set-AzVM och Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="17a3f-1486">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="17a3f-1487">Uppdaterade beskrivningen av ID i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="17a3f-1487">Updated the description of ID in help files</span></span>
* <span data-ttu-id="17a3f-1488">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="17a3f-1488">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="17a3f-1489">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="17a3f-1489">Az.DataLakeStore</span></span>
* <span data-ttu-id="17a3f-1490">Uppdatera sdk-versionen av dataplanet till 1.1.14 för SDK-korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1490">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="17a3f-1491">Korrigerade hanteringen av negativ accesstime och modificationtime för getfilestatus och liststatus; korrigera asynkront annulleringstoken</span><span class="sxs-lookup"><span data-stu-id="17a3f-1491">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="17a3f-1492">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="17a3f-1492">Az.EventGrid</span></span>
* <span data-ttu-id="17a3f-1493">Uppdaterat för användning av API-versionen 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1493">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="17a3f-1494">Uppdaterade följande cmdletar för att stödja nytt scenario i API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="17a3f-1494">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="17a3f-1495">New-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="17a3f-1495">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="17a3f-1496">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="17a3f-1496">Event Time-To-Live,</span></span>
        - <span data-ttu-id="17a3f-1497">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="17a3f-1497">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="17a3f-1498">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1498">Dead letter endpoint.</span></span>
    - <span data-ttu-id="17a3f-1499">Update-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="17a3f-1499">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="17a3f-1500">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="17a3f-1500">Event Time-To-Live,</span></span>
        - <span data-ttu-id="17a3f-1501">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="17a3f-1501">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="17a3f-1502">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1502">Dead letter endpoint.</span></span>
* <span data-ttu-id="17a3f-1503">Lade till nya enum-värden (storageQueue och hybridConnection) för alternativet EndpointType i cmdletarna New-AzureRmEventGridSubscription och Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1503">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="17a3f-1504">Visa varningsmeddelanden om skapande eller uppdatering av händelseprenumerationen förväntas medföra manuell åtgärd från användaren.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1504">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="17a3f-1505">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="17a3f-1505">Az.IotHub</span></span>
* <span data-ttu-id="17a3f-1506">Har uppdaterats till den senaste versionen av SDK:n lotHub</span><span class="sxs-lookup"><span data-stu-id="17a3f-1506">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="17a3f-1507">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="17a3f-1507">Az.LogicApp</span></span>
* <span data-ttu-id="17a3f-1508">Get-AzLogicApp visar en lista över alla som inte har angivet namn</span><span class="sxs-lookup"><span data-stu-id="17a3f-1508">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="17a3f-1509">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="17a3f-1509">Az.Resources</span></span>
* <span data-ttu-id="17a3f-1510">Åtgärdade problem med parameteruppsättningen när parametrarna -ODataQuery och -ResourceId anges för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="17a3f-1510">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="17a3f-1511">Mer information här: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="17a3f-1511">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="17a3f-1512">Åtgärdade hantering av parametern -Custom i New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="17a3f-1512">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="17a3f-1513">Korrigerade stavfel i New-AzDeployment-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="17a3f-1513">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="17a3f-1514">Gjorde parametern -MailNickname obligatorisk för New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="17a3f-1514">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="17a3f-1515">Mer information här: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="17a3f-1515">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="17a3f-1516">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="17a3f-1516">Az.SignalR</span></span>
* <span data-ttu-id="17a3f-1517">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="17a3f-1517">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="17a3f-1518">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="17a3f-1518">Az.Sql</span></span>
* <span data-ttu-id="17a3f-1519">Konverterade lagringshanteringsklientens beroende av den normala SDK-implementeringen.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1519">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="17a3f-1520">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="17a3f-1520">Az.Storage</span></span>
* <span data-ttu-id="17a3f-1521">Angav StorageAccountName för lagringskontext som det verkliga namnet på lagringskontot när det skapas med Sas Token, OAuth eller Anonymous</span><span class="sxs-lookup"><span data-stu-id="17a3f-1521">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="17a3f-1522">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="17a3f-1522">New-AzStorageContext</span></span>
* <span data-ttu-id="17a3f-1523">Skapade Sas Token för Blob Snapshot-objekt med parametern -FullUri, åtgärdade den returnerade URI:n så att den blir URI för ögonblicksbild</span><span class="sxs-lookup"><span data-stu-id="17a3f-1523">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="17a3f-1524">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="17a3f-1524">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="17a3f-1525">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="17a3f-1525">Az.Websites</span></span>
* <span data-ttu-id="17a3f-1526">Åtgärdade en bugg i datumparsningen i Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="17a3f-1526">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="17a3f-1527">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="17a3f-1527">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="17a3f-1528">1.0.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="17a3f-1528">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="17a3f-1529">Allmänt</span><span class="sxs-lookup"><span data-stu-id="17a3f-1529">General</span></span>

- <span data-ttu-id="17a3f-1530">Allmän tillgänglighet för Az-modulen</span><span class="sxs-lookup"><span data-stu-id="17a3f-1530">General Availability of Az Module</span></span>
- <span data-ttu-id="17a3f-1531">Onlinehjälp för varje modul</span><span class="sxs-lookup"><span data-stu-id="17a3f-1531">Online help for each module</span></span>
- <span data-ttu-id="17a3f-1532">Mer information och en översikt finns på [Az-informationssidan](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="17a3f-1532">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="17a3f-1533">Information om hur du migrerar från AzureRM finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="17a3f-1533">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="17a3f-1534">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="17a3f-1534">Az.Accounts</span></span>
- <span data-ttu-id="17a3f-1535">Har ändrats från Az.Profile</span><span class="sxs-lookup"><span data-stu-id="17a3f-1535">Changed from Az.Profile</span></span>
- <span data-ttu-id="17a3f-1536">Fasta tabellformat för profil- och kontexttyper</span><span class="sxs-lookup"><span data-stu-id="17a3f-1536">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="17a3f-1537">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="17a3f-1537">Az.ApiManagement</span></span>
- <span data-ttu-id="17a3f-1538">Korrigeringar för #7002</span><span class="sxs-lookup"><span data-stu-id="17a3f-1538">Fixes for #7002</span></span>
- <span data-ttu-id="17a3f-1539">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="17a3f-1539">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="17a3f-1540">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="17a3f-1540">Az.Batch</span></span>
- <span data-ttu-id="17a3f-1541">Lade till möjligheten att se vilken version av Azure Batch Node Agent som körs på var och en av de virtuella datorerna i en pool, via den nya egenskapen `NodeAgentInformation` på `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1541">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="17a3f-1542">Standarden `Caching` för `PSDataDisk` är nu `ReadWrite` i stället för `None`.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1542">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="17a3f-1543">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="17a3f-1543">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="17a3f-1544">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="17a3f-1544">Az.Billing</span></span>
- <span data-ttu-id="17a3f-1545">Kombinerar cmdletarna för fakturering, förbrukning och UsageAggregates. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="17a3f-1545">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="17a3f-1546">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="17a3f-1546">Az.CognitivServices</span></span>
- <span data-ttu-id="17a3f-1547">Lade till kompletterare för SkuName och Typem som är tillgängliga i New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="17a3f-1547">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="17a3f-1548">Tog bort parameteruppsättningen GetSkusWithAccountParamSetName från Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="17a3f-1548">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="17a3f-1549">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="17a3f-1549">Az.ContainerInstance</span></span>
- <span data-ttu-id="17a3f-1550">Stöd för ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="17a3f-1550">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="17a3f-1551">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="17a3f-1551">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="17a3f-1552">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="17a3f-1552">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="17a3f-1553">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="17a3f-1553">Az.DataLakeStore</span></span>
- <span data-ttu-id="17a3f-1554">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="17a3f-1554">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="17a3f-1555">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="17a3f-1555">Az.Monitor</span></span>
- <span data-ttu-id="17a3f-1556">Döpte om Az.Insights till Az.Monitor och andra mindre icke-bakåtkompatibla ändringar. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="17a3f-1556">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="17a3f-1557">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="17a3f-1557">Az.KeyVault</span></span>
- <span data-ttu-id="17a3f-1558">Tog bort den inaktuella egenskapen PurgeDisabled från utdatatyper</span><span class="sxs-lookup"><span data-stu-id="17a3f-1558">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="17a3f-1559">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="17a3f-1559">Az.MachineLearning</span></span>
- <span data-ttu-id="17a3f-1560">Inkluderade cmdletarna från modulen Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="17a3f-1560">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="17a3f-1561">Az.Media</span><span class="sxs-lookup"><span data-stu-id="17a3f-1561">Az.Media</span></span>
- <span data-ttu-id="17a3f-1562">Tog bort inaktuella -Tags-alias från New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="17a3f-1562">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="17a3f-1563">Az.Network</span><span class="sxs-lookup"><span data-stu-id="17a3f-1563">Az.Network</span></span>
<span data-ttu-id="17a3f-1564">Stöd har lagts till för konfiguration av RewriteRuleSets i Application Gateway</span><span class="sxs-lookup"><span data-stu-id="17a3f-1564">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="17a3f-1565">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="17a3f-1565">New cmdlets added:</span></span>
        - <span data-ttu-id="17a3f-1566">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="17a3f-1566">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="17a3f-1567">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="17a3f-1567">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="17a3f-1568">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="17a3f-1568">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="17a3f-1569">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="17a3f-1569">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="17a3f-1570">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="17a3f-1570">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="17a3f-1571">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="17a3f-1571">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="17a3f-1572">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="17a3f-1572">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="17a3f-1573">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="17a3f-1573">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="17a3f-1574">Cmdletar har uppdaterats med den valfria parametern -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="17a3f-1574">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="17a3f-1575">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="17a3f-1575">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="17a3f-1576">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="17a3f-1576">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="17a3f-1577">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="17a3f-1577">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="17a3f-1578">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="17a3f-1578">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="17a3f-1579">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="17a3f-1579">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="17a3f-1580">New-AzureRmApplicationGatewayUrlPathMapConfig har lagt till KeyVault-stöd för Application Gateway med Identity.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1580">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="17a3f-1581">Cmdletar har uppdaterats med den valfria parametern -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="17a3f-1581">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="17a3f-1582">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="17a3f-1582">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="17a3f-1583">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="17a3f-1583">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="17a3f-1584">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="17a3f-1584">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="17a3f-1585">Cmdleten New-AzApplicationGateway har uppdaterats med den valfria parametern -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="17a3f-1585">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="17a3f-1586">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="17a3f-1586">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="17a3f-1587">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="17a3f-1587">Az.OperationalInsights</span></span>
- <span data-ttu-id="17a3f-1588">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="17a3f-1588">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="17a3f-1589">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="17a3f-1589">Az.Profile</span></span>
- <span data-ttu-id="17a3f-1590">Modulnamnet har ändrats till Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="17a3f-1590">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="17a3f-1591">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="17a3f-1591">Az.RecoveryServices</span></span>
- <span data-ttu-id="17a3f-1592">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="17a3f-1592">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="17a3f-1593">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="17a3f-1593">Az.Resources</span></span>
- <span data-ttu-id="17a3f-1594">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="17a3f-1594">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="17a3f-1595">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="17a3f-1595">Az.ServiceFabric</span></span>
- <span data-ttu-id="17a3f-1596">Stöd för specificering av certifikat efter eget namn och tumavtryck</span><span class="sxs-lookup"><span data-stu-id="17a3f-1596">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="17a3f-1597">Information om fler icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="17a3f-1597">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="17a3f-1598">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="17a3f-1598">Az.SIgnalR</span></span>
- <span data-ttu-id="17a3f-1599">Allmän tillgänglighet för PowerShell-cmdletar för SIgnalR</span><span class="sxs-lookup"><span data-stu-id="17a3f-1599">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="17a3f-1600">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="17a3f-1600">Az.Sql</span></span>
- <span data-ttu-id="17a3f-1601">Lade till de nya identifieringstyperna Data_Exfiltration och Unsafe_Action i Threat Detection-cmdletar</span><span class="sxs-lookup"><span data-stu-id="17a3f-1601">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="17a3f-1602">Uppdaterade dokumentationsexempel för Sql Auditing-cmdletar</span><span class="sxs-lookup"><span data-stu-id="17a3f-1602">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="17a3f-1603">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="17a3f-1603">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="17a3f-1604">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="17a3f-1604">Az.Storage</span></span>
- <span data-ttu-id="17a3f-1605">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="17a3f-1605">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="17a3f-1606">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="17a3f-1606">Az.Websites</span></span>
- <span data-ttu-id="17a3f-1607">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="17a3f-1607">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="17a3f-1608">0.7.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="17a3f-1608">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="17a3f-1609">Allmänt</span><span class="sxs-lookup"><span data-stu-id="17a3f-1609">General</span></span>

* <span data-ttu-id="17a3f-1610">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="17a3f-1610">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="17a3f-1611">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="17a3f-1611">Az.Compute</span></span>

* <span data-ttu-id="17a3f-1612">Lade till stöd för UltraSSD och Galleriavbildningar i de enkla parameteruppsättningarna för `New-AzVm(ss)`-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1612">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="17a3f-1613">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="17a3f-1613">Az.DataLakeStore</span></span>

* <span data-ttu-id="17a3f-1614">Åtgärdade avslutande snedstreck i domänen för adls-konto</span><span class="sxs-lookup"><span data-stu-id="17a3f-1614">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="17a3f-1615">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="17a3f-1615">Az.FrontDoor</span></span>

* <span data-ttu-id="17a3f-1616">Brutna länkar korrigerades</span><span class="sxs-lookup"><span data-stu-id="17a3f-1616">Fixed some broken links</span></span>
    - <span data-ttu-id="17a3f-1617">I artiklarna New-AzureRmFrontDoor och Set-AzureRmFrontDoor artiklar korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1617">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="17a3f-1618">I artikeln New-AzureRmFrontDoorManagedRuleObject korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1618">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="17a3f-1619">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="17a3f-1619">Az.RecoveryServices</span></span>

* <span data-ttu-id="17a3f-1620">Lade till valideringar på klientsidan för Azure-filresurs med återställningsåtgärder.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1620">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="17a3f-1621">Gjorde storageAccountName och storageAccountResourceGroupName valfritt för afs-återställning.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1621">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="17a3f-1622">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="17a3f-1622">Az.Resources</span></span>

* <span data-ttu-id="17a3f-1623">Korrigering för https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="17a3f-1623">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="17a3f-1624">Uppdaterade Get-AzureRmRoleAssignment så att prenumerationsomfattningen används om den anges vid begäran om klassiska administratörer.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1624">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="17a3f-1625">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="17a3f-1625">Az.Sql</span></span>

* <span data-ttu-id="17a3f-1626">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="17a3f-1626">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="17a3f-1627">Korrigerade ett problem med Get-AzureRmSqlDatabaseVulnerabilityAssessment med DotNet-kärna</span><span class="sxs-lookup"><span data-stu-id="17a3f-1627">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="17a3f-1628">Ändrade dokumentationen för hjälpmeddelanden som rör SQL Auditing-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1628">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="17a3f-1629">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="17a3f-1629">Az.Storage</span></span>

* <span data-ttu-id="17a3f-1630">Lade till -EnableHierarchicalNamespace i New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="17a3f-1630">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="17a3f-1631">Åtgärdade problemet med att cmdleten Copy File inte kunde återanvända källkontexten på målet om inte -DestContext angetts</span><span class="sxs-lookup"><span data-stu-id="17a3f-1631">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="17a3f-1632">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="17a3f-1632">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="17a3f-1633">Stöd för statisk webbplatskonfiguration</span><span class="sxs-lookup"><span data-stu-id="17a3f-1633">Support Static Website configuration</span></span>
    - <span data-ttu-id="17a3f-1634">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="17a3f-1634">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="17a3f-1635">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="17a3f-1635">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="17a3f-1636">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="17a3f-1636">Az.Websites</span></span>

* <span data-ttu-id="17a3f-1637">Set-AzureRmWebApp och Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="17a3f-1637">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="17a3f-1638">Ny parameter (-AzureStoragePath) har lagts till för att ange att Azure Storage-sökvägar ska monteras i containerappar i Windows och Linux.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1638">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="17a3f-1639">Använder utdata från den nya cmdleten New-AzureRmWebAppAzureStoragePath som en parameter för att ange sökvägar för Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1639">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="17a3f-1640">0.6.1 – november 2018</span><span class="sxs-lookup"><span data-stu-id="17a3f-1640">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="17a3f-1641">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="17a3f-1641">Az.ApiManagement</span></span>
* <span data-ttu-id="17a3f-1642">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="17a3f-1642">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="17a3f-1643">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="17a3f-1643">Az.Automation</span></span>
* <span data-ttu-id="17a3f-1644">Swagger baserade Azure Automation-cmdletar</span><span class="sxs-lookup"><span data-stu-id="17a3f-1644">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="17a3f-1645">Cmdletar för Uppdateringshantering har lagts till</span><span class="sxs-lookup"><span data-stu-id="17a3f-1645">Added Update Management cmdlets</span></span>
* <span data-ttu-id="17a3f-1646">Cmdletar för källkontroll har lagts till</span><span class="sxs-lookup"><span data-stu-id="17a3f-1646">Added Source Control cmdlets</span></span>
* <span data-ttu-id="17a3f-1647">Remove-AzureRmAutomationHybridWorkerGroup-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="17a3f-1647">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="17a3f-1648">Kommandot för DSC-registreringsnod har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="17a3f-1648">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="17a3f-1649">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="17a3f-1649">Az.Compute</span></span>
* <span data-ttu-id="17a3f-1650">Problem med SystemAssigned-identitet har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="17a3f-1650">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="17a3f-1651">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="17a3f-1651">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="17a3f-1652">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="17a3f-1652">Az.ContainerInstance</span></span>
* <span data-ttu-id="17a3f-1653">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="17a3f-1653">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="17a3f-1654">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="17a3f-1654">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="17a3f-1655">uppdatera exempelbeskrivningen för marketplace-cmdletar</span><span class="sxs-lookup"><span data-stu-id="17a3f-1655">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="17a3f-1656">Az.Network</span><span class="sxs-lookup"><span data-stu-id="17a3f-1656">Az.Network</span></span>
* <span data-ttu-id="17a3f-1657">Cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomErreller Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="17a3f-1657">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="17a3f-1658">ICMP tillbaka till stöd för Azure Firewall-nätverksprotokoll har lagts till</span><span class="sxs-lookup"><span data-stu-id="17a3f-1658">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="17a3f-1659">Uppdatera cmdlet Test-AzureRmNetworkWatcherConnectivity, lägga till verifiering av mål-id, adress och port.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1659">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="17a3f-1660">Åtgärda problem med minnesanvändning i VirtualNetwork-karta</span><span class="sxs-lookup"><span data-stu-id="17a3f-1660">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="17a3f-1661">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="17a3f-1661">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="17a3f-1662">Åtgärda för att ändra principen för en skyddad fildelning.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1662">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="17a3f-1663">Tidszonsprincipen har konverterats till versaler.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1663">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="17a3f-1664">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="17a3f-1664">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="17a3f-1665">Exempel i New-AzureRmRecoveryServicesAsrProtectableItem har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="17a3f-1665">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="17a3f-1666">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="17a3f-1666">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="17a3f-1667">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="17a3f-1667">Az.Relay</span></span>
* <span data-ttu-id="17a3f-1668">Valfri parameter -KeyValue till New-AzureRmRelayKey cmdlet har lagts till, vilket gör det möjligt för användare att tillhandahålla KeyValue.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1668">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="17a3f-1669">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="17a3f-1669">Az.Resources</span></span>
* <span data-ttu-id="17a3f-1670">Uppdatera hjälpdokumentation för resursidentitet kopplad till parametrar i `New-AzureRmPolicyAssignment` och `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="17a3f-1670">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="17a3f-1671">Lägg till ett exempel för New-AzureRmPolicyDefinition som använder -Metadata</span><span class="sxs-lookup"><span data-stu-id="17a3f-1671">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="17a3f-1672">Korrigera så att skiftläge behålls i taggnycklar i NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="17a3f-1672">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="17a3f-1673">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="17a3f-1673">Az.ServiceFabric</span></span>
* <span data-ttu-id="17a3f-1674">Lägg till utfasningsmeddelanden för kommande icke-kompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="17a3f-1674">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="17a3f-1675">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="17a3f-1675">Az.Sql</span></span>
* <span data-ttu-id="17a3f-1676">Nya cmdletar för CRUD-åtgärder på Azure Sql Database-hanterad instans och Azure Sql-hanterad databas</span><span class="sxs-lookup"><span data-stu-id="17a3f-1676">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="17a3f-1677">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="17a3f-1677">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="17a3f-1678">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="17a3f-1678">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="17a3f-1679">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="17a3f-1679">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="17a3f-1680">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="17a3f-1680">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="17a3f-1681">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="17a3f-1681">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="17a3f-1682">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="17a3f-1682">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="17a3f-1683">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="17a3f-1683">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="17a3f-1684">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="17a3f-1684">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="17a3f-1685">Hantering av utökad granskningsprincip på en server eller en databas har aktiverats.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1685">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="17a3f-1686">Ny parameter (PredicateExpression) har lagts till för att aktivera filtrering av granskningsloggar.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1686">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="17a3f-1687">Cmdletar har ändrats så att de använder SQL-klienter i stället för äldre klienter.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1687">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="17a3f-1688">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1688">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="17a3f-1689">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1689">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="17a3f-1690">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1690">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="17a3f-1691">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1691">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="17a3f-1692">Problem med att använda Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings med lagringskontots namnparameter har korrigerats</span><span class="sxs-lookup"><span data-stu-id="17a3f-1692">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="17a3f-1693">0.5.0 – november 2018</span><span class="sxs-lookup"><span data-stu-id="17a3f-1693">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="17a3f-1694">Allmänt</span><span class="sxs-lookup"><span data-stu-id="17a3f-1694">General</span></span>
* <span data-ttu-id="17a3f-1695">Lade till resurskompletterare till många kärn-cmdletar – dessa gör att du kan stega genom befintliga resursnamn med TABB vid interaktiva anrop till cmdletar</span><span class="sxs-lookup"><span data-stu-id="17a3f-1695">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="17a3f-1696">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="17a3f-1696">Az.Profile</span></span>
* <span data-ttu-id="17a3f-1697">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="17a3f-1697">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="17a3f-1698">Bytte namn på parametern TenantId i cmdleten Connect-AzAccount till Tenant och lade till ett alias för TenantId</span><span class="sxs-lookup"><span data-stu-id="17a3f-1698">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="17a3f-1699">Uppdaterade TenantId-beskrivningen för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="17a3f-1699">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="17a3f-1700">Åtgärda felmeddelande för misslyckad inloggning när du tillhandahåller klientdomän</span><span class="sxs-lookup"><span data-stu-id="17a3f-1700">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="17a3f-1701">Åtgärda problem med att kontextnamn hamnar i konflikt för konton utan prenumerationer i klientorganisationen</span><span class="sxs-lookup"><span data-stu-id="17a3f-1701">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="17a3f-1702">Åtgärda problem med DataLake-slutpunkter vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="17a3f-1702">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="17a3f-1703">Åtgärdade problem med att Disconnect-AzAccount kastades om den inte anslöts</span><span class="sxs-lookup"><span data-stu-id="17a3f-1703">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="17a3f-1704">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="17a3f-1704">Az.CognitiveServices</span></span>
* <span data-ttu-id="17a3f-1705">Lade till åtgärden Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1705">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="17a3f-1706">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="17a3f-1706">Az.Compute</span></span>
* <span data-ttu-id="17a3f-1707">Lade till cmdletarna Add-AzVmssVMDataDisk och Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="17a3f-1707">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="17a3f-1708">Get-AzVMImage visar AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="17a3f-1708">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="17a3f-1709">Åtgärdade att värdena för alternativen SetAzVMChefExtension -BootstrapOptions och -JsonAttribute inte angavs i json-format.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1709">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="17a3f-1710">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="17a3f-1710">Az.DataLakeStore</span></span>
* <span data-ttu-id="17a3f-1711">Uppdatera DataLake-paketet till 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1711">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="17a3f-1712">Lägg till standardsamtidighet för flertrådade åtgärder.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1712">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="17a3f-1713">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="17a3f-1713">Az.Insights</span></span>
* <span data-ttu-id="17a3f-1714">Åtgärdade problem #7267 (autoskalningsområde)</span><span class="sxs-lookup"><span data-stu-id="17a3f-1714">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="17a3f-1715">Problem med att uppräknade parametrar inte ställdes in ordentligt när du skapade en ny autoskalningsregel (de ställdes alltid in med standardvärdet).</span><span class="sxs-lookup"><span data-stu-id="17a3f-1715">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="17a3f-1716">Åtgärdade problem #7513 [Insights] Set-AzDiagnosticSetting kräver uttrycklig specifikation av kategorier när inställningar skapas</span><span class="sxs-lookup"><span data-stu-id="17a3f-1716">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="17a3f-1717">Nu kräver inte cmdleten uttrycklig anvisning av kategorierna för att aktiveras under skapande, d.v.s. den fungerar enligt beskrivning</span><span class="sxs-lookup"><span data-stu-id="17a3f-1717">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="17a3f-1718">Az.Network</span><span class="sxs-lookup"><span data-stu-id="17a3f-1718">Az.Network</span></span>
* <span data-ttu-id="17a3f-1719">PeeringType ändrades till en obligatorisk parameter för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="17a3f-1719">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="17a3f-1720">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="17a3f-1720">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="17a3f-1721">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="17a3f-1721">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="17a3f-1722">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="17a3f-1722">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="17a3f-1723">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="17a3f-1723">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="17a3f-1724">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="17a3f-1724">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="17a3f-1725">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="17a3f-1725">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="17a3f-1726">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="17a3f-1726">Az.PolicyInsights</span></span>
* <span data-ttu-id="17a3f-1727">Cmdletar för principreparation har lagts till</span><span class="sxs-lookup"><span data-stu-id="17a3f-1727">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="17a3f-1728">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="17a3f-1728">Az.Resources</span></span>
* <span data-ttu-id="17a3f-1729">Korrigering för https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="17a3f-1729">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="17a3f-1730">Tillåt att resurser listas med parametern -ResourceId för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="17a3f-1730">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="17a3f-1731">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="17a3f-1731">Az.ServiceBus</span></span>
* <span data-ttu-id="17a3f-1732">Skrivskyddad MigrationState-egenskap har lagts till i PSServiceBusMigrationConfigurationAttributes, som hjälper till att hålla koll på migreringstillståndet.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1732">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="17a3f-1733">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="17a3f-1733">Az.ServiceFabric</span></span>
* <span data-ttu-id="17a3f-1734">Åtgärda att lägga till certifikat till Linux-Vmss.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1734">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="17a3f-1735">Åtgärdade Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="17a3f-1735">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="17a3f-1736">Använd rätt tumavtryck från nya certifikat (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="17a3f-1736">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="17a3f-1737">Visa undantag korrekt (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="17a3f-1737">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="17a3f-1738">Åtgärdade Update-AzServiceFabricDurability så att klusterkonfigurationen uppdateras innan Vmss-åtgärden CreateOrUpdate påbörjas.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1738">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="17a3f-1739">0.4.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="17a3f-1739">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="17a3f-1740">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="17a3f-1740">Az.Profile</span></span>
* <span data-ttu-id="17a3f-1741">Åtgärdade problemet med Get-AzSubscription i CloudShell</span><span class="sxs-lookup"><span data-stu-id="17a3f-1741">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="17a3f-1742">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="17a3f-1742">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="17a3f-1743">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="17a3f-1743">Az.Compute</span></span>
* <span data-ttu-id="17a3f-1744">Nya storlekar lades till i listan över godkända VM-storlekar för vilka accelererat nätverk kommer att aktiveras vid användning av den enkla parameteruppsättningen för New-AzVm</span><span class="sxs-lookup"><span data-stu-id="17a3f-1744">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="17a3f-1745">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1745">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="17a3f-1746">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="17a3f-1746">Az.DataLakeStore</span></span>
* <span data-ttu-id="17a3f-1747">Lägger till stöd för regler för virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="17a3f-1747">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="17a3f-1748">Get-AzDataLakeStoreVirtualNetworkRule: Hämtar eller listar regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1748">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="17a3f-1749">Add-AzDataLakeStoreVirtualNetworkRule: Lägger till en regel för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1749">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="17a3f-1750">Set-AzDataLakeStoreVirtualNetworkRule: Ändrar den angivna regeln för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1750">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="17a3f-1751">Remove-AzDataLakeStoreVirtualNetworkRule: Tar bort en regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1751">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="17a3f-1752">Az.Network</span><span class="sxs-lookup"><span data-stu-id="17a3f-1752">Az.Network</span></span>
* <span data-ttu-id="17a3f-1753">Skicka protokollvärdet till serverdelen för att uppdatera cmdleten Test-AzNetworkWatcherConnectivity.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1753">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="17a3f-1754">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1754">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="17a3f-1755">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="17a3f-1755">Az.Resources</span></span>
* <span data-ttu-id="17a3f-1756">Åtgärdade problem där Get-AzRoleDefinition genererar ett oläsligt undantag (när standardprofilen inte innehåller någon prenumeration och ingen omfattning har angetts) genom att lägga till ett beskrivande undantag i scenariot.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1756">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="17a3f-1757">Ställ in ”RoleDefinitionNameParameterSet” som standardparameteruppsättning.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1757">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="17a3f-1758">0.3.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="17a3f-1758">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="17a3f-1759">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="17a3f-1759">Azure.Storage</span></span>
* <span data-ttu-id="17a3f-1760">Åtgärda fel där Kopiera blob/fil inte kopierar metadata när målplatsen har ett problem med metadata</span><span class="sxs-lookup"><span data-stu-id="17a3f-1760">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="17a3f-1761">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="17a3f-1761">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="17a3f-1762">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="17a3f-1762">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="17a3f-1763">Stöd för att hämta användningsinformation om en Storage-resurs för en specifik plats och för att lägga till ett varningsmeddelande för att hämta användningsinformation om en global Storage-resurs är inaktuellt.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1763">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="17a3f-1764">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="17a3f-1764">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="17a3f-1765">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="17a3f-1765">Az.CognitiveServices</span></span>
* <span data-ttu-id="17a3f-1766">Stöd för Get-AzCognitiveServicesAccountSkus utan ett befintligt konto.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1766">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="17a3f-1767">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="17a3f-1767">Az.Compute</span></span>
* <span data-ttu-id="17a3f-1768">Åtgärdade fel där Get-AzVM -ResourceGroupName <rg> returnerar fler än 50 resultat om det behövs</span><span class="sxs-lookup"><span data-stu-id="17a3f-1768">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="17a3f-1769">Lade till ett exempel för SimpleParameterSet i hjälpen för cmdleten New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1769">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="17a3f-1770">Ett stavfel i förloppsmeddelandet för Azure Disk Encryption har korrigerats</span><span class="sxs-lookup"><span data-stu-id="17a3f-1770">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="17a3f-1771">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="17a3f-1771">Az.DataFactoryV2</span></span>
* <span data-ttu-id="17a3f-1772">ADF .Net SDK-versionen har uppdaterats till 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1772">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="17a3f-1773">Az.Network</span><span class="sxs-lookup"><span data-stu-id="17a3f-1773">Az.Network</span></span>
* <span data-ttu-id="17a3f-1774">Funktionalitet för NetworkProfile har lagts till.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1774">Added NetworkProfile functionality.</span></span> <span data-ttu-id="17a3f-1775">nya cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="17a3f-1775">new cmdlets added</span></span>
    - <span data-ttu-id="17a3f-1776">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="17a3f-1776">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="17a3f-1777">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="17a3f-1777">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="17a3f-1778">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="17a3f-1778">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="17a3f-1779">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="17a3f-1779">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="17a3f-1780">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="17a3f-1780">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="17a3f-1781">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="17a3f-1781">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="17a3f-1782">Länk för tjänstassociering på modell för undernät har lagts till</span><span class="sxs-lookup"><span data-stu-id="17a3f-1782">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="17a3f-1783">Cmdletarna New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap och Remove-AzVirtualNetworkTap har lagts till</span><span class="sxs-lookup"><span data-stu-id="17a3f-1783">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="17a3f-1784">Cmdletarna Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig och Remove-AzNEtworkInterfaceTapConfig har lagts till</span><span class="sxs-lookup"><span data-stu-id="17a3f-1784">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="17a3f-1785">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="17a3f-1785">Az.RedisCache</span></span>
* <span data-ttu-id="17a3f-1786">Tillåt att alla strängar används som storleksparametrar framöver.</span><span class="sxs-lookup"><span data-stu-id="17a3f-1786">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="17a3f-1787">Lägg till P5 i popup-fönstret PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="17a3f-1787">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="17a3f-1788">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="17a3f-1788">Az.Resources</span></span>
* <span data-ttu-id="17a3f-1789">Parametern -Mode som saknades i Set-AzPolicyDefinition har lagts till</span><span class="sxs-lookup"><span data-stu-id="17a3f-1789">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="17a3f-1790">Åtgärdade buggen för cmdleten Get-AzProviderOperation för åtgärder med ursprung som innehåller användare</span><span class="sxs-lookup"><span data-stu-id="17a3f-1790">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="17a3f-1791">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="17a3f-1791">Az.Sql</span></span>
* <span data-ttu-id="17a3f-1792">Ett problem där vissa cmdletar för säkerhetskopiering inte kunde identifiera den aktuella azure-prenumerationen har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="17a3f-1792">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="17a3f-1793">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="17a3f-1793">Az.Websites</span></span>
* <span data-ttu-id="17a3f-1794">Ny cmdlet: Get-AzWebAppContainerContinuousDeploymentUrl – Hämtar webhook-URL:en för kontinuerlig distribution av container</span><span class="sxs-lookup"><span data-stu-id="17a3f-1794">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="17a3f-1795">Nya cmdletar: New-AzWebAppContainerPSSession och Enter-WebAppContainerPSSession – Startar en PowerShell-fjärrsession i en containerapp för windows</span><span class="sxs-lookup"><span data-stu-id="17a3f-1795">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="17a3f-1796">0.2.0 – september 2018</span><span class="sxs-lookup"><span data-stu-id="17a3f-1796">0.2.0 - September 2018</span></span>
 <span data-ttu-id="17a3f-1797">Första versionen</span><span class="sxs-lookup"><span data-stu-id="17a3f-1797">Initial Release</span></span>
