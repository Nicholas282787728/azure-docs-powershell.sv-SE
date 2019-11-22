---
title: Viktig information om Azure PowerShell
description: Lär dig mer om alla de senaste uppdateringarna för Azure PowerShell-modulerna.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/15/2019
ms.openlocfilehash: ee3f54e6bc15dbbaeb97cad7463cb1d2e5795e3e
ms.sourcegitcommit: 05431341858d10eb9c345213275c3ccc24c83c9b
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/13/2019
ms.locfileid: "74062147"
---
## <a name="300---november-2019"></a><span data-ttu-id="558f8-103">3.0.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="558f8-103">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="558f8-104">Allmänt</span><span class="sxs-lookup"><span data-stu-id="558f8-104">General</span></span>
* <span data-ttu-id="558f8-105">Az. PrivateDns 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="558f8-105">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="558f8-106">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="558f8-106">Az.Accounts</span></span>
* <span data-ttu-id="558f8-107">Lägg till ett utfasningsmeddelande för aliaset Resolve-error.</span><span class="sxs-lookup"><span data-stu-id="558f8-107">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="558f8-108">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="558f8-108">Az.Advisor</span></span>
* <span data-ttu-id="558f8-109">Den nya kategorin Operational Excellence har lagts till i cmdleten Get-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="558f8-109">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="558f8-110">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="558f8-110">Az.Batch</span></span>
* <span data-ttu-id="558f8-111">`CoreQuota` på `BatchAccountContext` har bytt namn till `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="558f8-111">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="558f8-112">Det finns även en ny `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="558f8-112">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="558f8-113">Detta påverkar **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="558f8-113">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="558f8-114">**New-AzBatchTask** `-ResourceFile`-parameter tar nu en samling `PSResourceFile`-objekt som kan skapas med hjälp av den nya cmdleten **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="558f8-114">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="558f8-115">Ny **New-AzBatchResourceFile**-cmdlet för att skapa `PSResourceFile`-objekt.</span><span class="sxs-lookup"><span data-stu-id="558f8-115">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="558f8-116">Dessa kan tillhandahållas till **New-AzBatchTask** på `-ResourceFile`-parametern.</span><span class="sxs-lookup"><span data-stu-id="558f8-116">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="558f8-117">Detta stöder två nya typer av resursfiler förutom det befintliga sättet med `HttpUrl`:</span><span class="sxs-lookup"><span data-stu-id="558f8-117">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="558f8-118">`AutoStorageContainerName`-baserade resursfiler laddar ned en hel container för automatisk lagring till Batch-noden.</span><span class="sxs-lookup"><span data-stu-id="558f8-118">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="558f8-119">`StorageContainerUrl`-baserade resursfiler laddar ned containern som anges i webbadressen till Batch-noden.</span><span class="sxs-lookup"><span data-stu-id="558f8-119">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="558f8-120">Tog bort egenskapen `ApplicationPackages` för `PSApplication` som returnerades av **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="558f8-120">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="558f8-121">Specifika paket i ett program kan nu hämtas med hjälp av **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="558f8-121">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="558f8-122">Till exempel: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="558f8-122">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="558f8-123">Bytt namn på `ApplicationId` till `ApplicationName` på **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** och **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="558f8-123">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="558f8-124">`ApplicationId` är nu ett alias för `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="558f8-124">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="558f8-125">Ny `PSWindowsUserConfiguration`-egenskap till `PSUserAccount` lades till.</span><span class="sxs-lookup"><span data-stu-id="558f8-125">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="558f8-126">Bytte namn på `Version` till `Name` på `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="558f8-126">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="558f8-127">Bytte namn på `BlobSource` till `HttpUrl` på `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="558f8-127">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="558f8-128">Tog bort egenskapen `OSDisk` från `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="558f8-128">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="558f8-129">Tog bort **Set-AzBatchPoolOSVersion**.</span><span class="sxs-lookup"><span data-stu-id="558f8-129">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="558f8-130">Den här åtgärden stöds inte längre.</span><span class="sxs-lookup"><span data-stu-id="558f8-130">This operation is no longer supported.</span></span>
* <span data-ttu-id="558f8-131">`TargetOSVersion` har tagits bort från `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="558f8-131">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="558f8-132">Bytte namn på `CurrentOSVersion` till `OSVersion` på `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="558f8-132">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="558f8-133">`DataEgressGiB` och `DataIngressGiB` har tagits bort från `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="558f8-133">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="558f8-134">Tog bort **Get-AzBatchNodeAgentSku** och ersatte det med **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="558f8-134">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span> 
  - <span data-ttu-id="558f8-135">**Get-AzBatchSupportedImage** returnerar samma data som **Get-AzBatchNodeAgentSku** men i ett mer användarvänligt format.</span><span class="sxs-lookup"><span data-stu-id="558f8-135">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="558f8-136">Nya icke-verifierade avbildningar returneras nu också.</span><span class="sxs-lookup"><span data-stu-id="558f8-136">New non-verified images are also now returned.</span></span> <span data-ttu-id="558f8-137">Ytterligare information om `Capabilities` och `BatchSupportEndOfLife` för varje avbildning inkluderas också.</span><span class="sxs-lookup"><span data-stu-id="558f8-137">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="558f8-138">Lade till möjlighet att montera fjärrfilsystem på varje nod i en pool via den nya parametern `MountConfiguration` för **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="558f8-138">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="558f8-139">Har nu stöd för nätverkssäkerhetsregler som blockerar nätverksåtkomst till en pool baserat på källportens trafik.</span><span class="sxs-lookup"><span data-stu-id="558f8-139">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="558f8-140">Detta görs via egenskapen `SourcePortRanges` på `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="558f8-140">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="558f8-141">När du kör en container stöder nu Batch körningen av uppgiften i arbetskatalogen för containern eller i arbetskatalogen för Batch-uppgiften.</span><span class="sxs-lookup"><span data-stu-id="558f8-141">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="558f8-142">Detta styrs av egenskapen `WorkingDirectory` på `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="558f8-142">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="558f8-143">Lade till en funktion för att ange en samling av offentliga IP-adresser på `PSNetworkConfiguration` via den nya egenskapen `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="558f8-143">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="558f8-144">Detta garanterar att noderna i poolen har en IP-adress från listan över IP-adresser som tillhandahållits av användare.</span><span class="sxs-lookup"><span data-stu-id="558f8-144">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="558f8-145">Om inget värde anges är standardvärdet för `WaitForSuccess` på `PSSTartTask` nu `$True` (var tidigare `$False`).</span><span class="sxs-lookup"><span data-stu-id="558f8-145">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="558f8-146">Om inget värde anges är standardvärdet för `Scope` på `PSAutoUserSpecification` nu `Pool` (var tidigare `Task` på Windows och `Pool` på Linux).</span><span class="sxs-lookup"><span data-stu-id="558f8-146">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="558f8-147">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="558f8-147">Az.Cdn</span></span>
* <span data-ttu-id="558f8-148">Introducerade UrlRewriteAction och CacheKeyQueryStringAction till RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="558f8-148">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="558f8-149">Åtgärdade flera buggar, som saknade indata för ”väljare” i cmdleten New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="558f8-149">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="558f8-150">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="558f8-150">Az.Compute</span></span>
* <span data-ttu-id="558f8-151">Funktion för diskkrypteringsuppsättning</span><span class="sxs-lookup"><span data-stu-id="558f8-151">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="558f8-152">Nya cmdletar:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="558f8-152">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="558f8-153">Parametern DiskEncryptionSetId har lagts till i följande cmdletar: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="558f8-153">DiskEncryptionSetId parameter is added to the following cmdlets: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span></span>        
        <span data-ttu-id="558f8-154">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="558f8-154">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="558f8-155">Parametrarna DiskEncryptionSetId och EncryptionType har lagts till i följande cmdletar:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="558f8-155">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="558f8-156">Lägg till parametern PublicIPAddressVersion i New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="558f8-156">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="558f8-157">Flytta FileUris för anpassat skripttillägg från offentlig inställning till skyddad inställning</span><span class="sxs-lookup"><span data-stu-id="558f8-157">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="558f8-158">Lägg till ScaleInPolicy i cmdletarna New-AzVmss, New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="558f8-158">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="558f8-159">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="558f8-159">Breaking changes</span></span>
    - <span data-ttu-id="558f8-160">Parametern UploadSizeInBytes används istället för DiskSizeGB för New-AzDiskConfig när CreateOption är Uppladdning</span><span class="sxs-lookup"><span data-stu-id="558f8-160">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="558f8-161">PublishingProfile.Source.ManagedImage.Id ersätts med StorageProfile.Source.Id i objektet GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="558f8-161">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="558f8-162">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="558f8-162">Az.DataFactory</span></span>
* <span data-ttu-id="558f8-163">Uppdatera ADF .Net SDK-versionen till 4.3.0</span><span class="sxs-lookup"><span data-stu-id="558f8-163">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="558f8-164">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="558f8-164">Az.DataLakeStore</span></span>
* <span data-ttu-id="558f8-165">Uppdatera ADLS SDK-version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) innehåller följande korrigeringar</span><span class="sxs-lookup"><span data-stu-id="558f8-165">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="558f8-166">Undvik att utlösa undantag när det inte går att deserialisera creationtime för inmatning av papperskorg eller katalog.</span><span class="sxs-lookup"><span data-stu-id="558f8-166">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="558f8-167">Gör inställning tillgänglig per tidsgräns för förfrågan i adlsclient</span><span class="sxs-lookup"><span data-stu-id="558f8-167">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="558f8-168">Korrigera överföringen av ursprunglig syncflag för badoffset-återställning</span><span class="sxs-lookup"><span data-stu-id="558f8-168">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="558f8-169">Korrigera EnumerateDirectory för att hämta fortsättningstoken när svar har kontrollerats</span><span class="sxs-lookup"><span data-stu-id="558f8-169">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="558f8-170">Korrigera bugg i Concat</span><span class="sxs-lookup"><span data-stu-id="558f8-170">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="558f8-171">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="558f8-171">Az.FrontDoor</span></span>
* <span data-ttu-id="558f8-172">Åtgärdade diverse stavfel i modul</span><span class="sxs-lookup"><span data-stu-id="558f8-172">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="558f8-173">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="558f8-173">Az.HDInsight</span></span>
* <span data-ttu-id="558f8-174">Korrigerade buggen att kunder får felet ”inte en giltig Base-64-sträng” vid användning av Get-AzHDInsightCluster för att hämta klustret med ADLSGen1-lagring.</span><span class="sxs-lookup"><span data-stu-id="558f8-174">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="558f8-175">Lägg till en parameter med namnet ”ApplicationId” i de tre cmdletarna Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig och New-AzHDInsightCluster så att kunden kan tillhandahålla tjänstens huvudnamn för program-ID för åtkomst till Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="558f8-175">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="558f8-176">Ändrade Microsoft.Azure.Management.HDInsight från 2.1.0 till 5.1.0</span><span class="sxs-lookup"><span data-stu-id="558f8-176">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="558f8-177">Fem cmdletar har tagits bort:</span><span class="sxs-lookup"><span data-stu-id="558f8-177">Removed five cmdlets:</span></span>
    - <span data-ttu-id="558f8-178">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="558f8-178">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="558f8-179">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="558f8-179">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="558f8-180">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="558f8-180">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="558f8-181">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="558f8-181">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="558f8-182">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="558f8-182">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="558f8-183">Tre cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="558f8-183">Added three cmdlets:</span></span>
    - <span data-ttu-id="558f8-184">Get-AzHDInsightMonitoring som ersätter Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="558f8-184">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="558f8-185">Enable-AzHDInsightMonitoring som ersätter Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="558f8-185">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="558f8-186">Disable-AzHDInsightMonitoring som ersätter Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="558f8-186">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="558f8-187">Korrigerade cmdleten Get-AzHDInsightProperties för att stödja hämtning av funktionsinformation från en viss plats.</span><span class="sxs-lookup"><span data-stu-id="558f8-187">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="558f8-188">Parameteruppsättningarna (Spark1 och Spark2) har tagits bort från Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="558f8-188">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="558f8-189">Lägg till exempel för cmdleten Add-AzHDInsightSecurityProfile till hjälpdokumenten.</span><span class="sxs-lookup"><span data-stu-id="558f8-189">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="558f8-190">Ändrade utdatatyp för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="558f8-190">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="558f8-191">Ändrade utdatatyp för Get-AzHDInsightProperties från CapabilitiesResponse till AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="558f8-191">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="558f8-192">Ändrade utdatatyp för Remove-AzHDInsightCluster från ClusterGetResponse till bool.</span><span class="sxs-lookup"><span data-stu-id="558f8-192">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="558f8-193">Ändrade utdatatyp för Set-AzHDInsightGatewaySettings HttpConnectivitySettings till GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="558f8-193">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="558f8-194">Lade till testfall för vissa scenarier.</span><span class="sxs-lookup"><span data-stu-id="558f8-194">Added some scenario test cases.</span></span>
* <span data-ttu-id="558f8-195">Ta bort vissa alias: Add-AzHDInsightConfigValues, Get-AzHDInsightProperties.</span><span class="sxs-lookup"><span data-stu-id="558f8-195">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="558f8-196">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="558f8-196">Az.IotHub</span></span>
* <span data-ttu-id="558f8-197">Icke-bakåtkompatibla ändringar:</span><span class="sxs-lookup"><span data-stu-id="558f8-197">Breaking changes:</span></span>
    - <span data-ttu-id="558f8-198">Cmdleten Add-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="558f8-198">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="558f8-199">Parameteruppsättningen __AllParameterSets för cmdleten Add-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="558f8-199">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="558f8-200">Cmdleten Get-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="558f8-200">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="558f8-201">Parameteruppsättningen __AllParameterSets för cmdleten Get-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="558f8-201">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="558f8-202">Egenskapen OperationsMonitoringProperties av typen Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="558f8-202">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="558f8-203">Egenskapen OperationsMonitoringProperties av typen Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="558f8-203">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="558f8-204">Cmdleten New-AzIotHubExportDevice stöder inte längre aliaset New-AzIotHubExportDevices.</span><span class="sxs-lookup"><span data-stu-id="558f8-204">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="558f8-205">Cmdleten New-AzIotHubImportDevice stöder inte längre aliaset New-AzIotHubImportDevices.</span><span class="sxs-lookup"><span data-stu-id="558f8-205">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="558f8-206">Cmdleten Remove-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="558f8-206">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="558f8-207">Parameteruppsättningen __AllParameterSets för cmdleten Remove-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="558f8-207">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="558f8-208">Cmdleten Set-AzIotHub har inte längre stöd för parametern OperationsMonitoringProperties och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="558f8-208">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="558f8-209">Parameteruppsättningen UpdateOperationsMonitoringProperties för cmdleten Set-AzIotHub har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="558f8-209">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="558f8-210">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="558f8-210">Az.RecoveryServices</span></span>
* <span data-ttu-id="558f8-211">Azure Site Recovery-stöd för att konfigurera nätverksresurser som NSG, offentliga IP-adresser och interna lastbalanserare för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="558f8-211">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="558f8-212">Azure Site Recovery-stöd för att skriva till hanterad disk för vMWare till Azure.</span><span class="sxs-lookup"><span data-stu-id="558f8-212">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="558f8-213">Azure Site Recovery-stöd för NIC-reduktion för vMWare till Azure.</span><span class="sxs-lookup"><span data-stu-id="558f8-213">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="558f8-214">Azure Site Recovery-stöd för accelererat nätverk för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="558f8-214">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="558f8-215">Azure Site Recovery-stöd för automatisk uppdatering av agent för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="558f8-215">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="558f8-216">Azure Site Recovery-stöd för Standard SSD för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="558f8-216">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="558f8-217">Azure Site Recovery-stöd för tvåstegskryptering i Azure Disk Encryption för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="558f8-217">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="558f8-218">Azure Site Recovery-stöd för att skydda nyligen tillagda diskar för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="558f8-218">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="558f8-219">En funktion för mjuk borttagning av virtuella datorer samt tester för mjuk borttagning har tagits bort</span><span class="sxs-lookup"><span data-stu-id="558f8-219">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="558f8-220">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="558f8-220">Az.Resources</span></span>
* <span data-ttu-id="558f8-221">Uppdatera beroendesammansättning för Microsoft.Extensions.Caching.Memory från 1.1.1 till 2.2</span><span class="sxs-lookup"><span data-stu-id="558f8-221">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="558f8-222">Az.Network</span><span class="sxs-lookup"><span data-stu-id="558f8-222">Az.Network</span></span>
* <span data-ttu-id="558f8-223">Ändra alla cmdletar för PrivateEndpointConnection så att de stöder generiska tjänstleverantörer.</span><span class="sxs-lookup"><span data-stu-id="558f8-223">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="558f8-224">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="558f8-224">Updated cmdlet:</span></span>
        - <span data-ttu-id="558f8-225">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="558f8-225">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="558f8-226">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="558f8-226">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="558f8-227">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="558f8-227">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="558f8-228">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="558f8-228">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="558f8-229">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="558f8-229">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="558f8-230">Lägg till ny cmdlet för PrivateLinkResource så att det också stöder generiska tjänstleverantörer.</span><span class="sxs-lookup"><span data-stu-id="558f8-230">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="558f8-231">Ny cmdlet:</span><span class="sxs-lookup"><span data-stu-id="558f8-231">New cmdlet:</span></span>
        - <span data-ttu-id="558f8-232">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="558f8-232">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="558f8-233">Lägg till nya fält och parametrar för funktionen Proxy Protocol V2.</span><span class="sxs-lookup"><span data-stu-id="558f8-233">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="558f8-234">Lägg till egenskapen EnableProxyProtocol i PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="558f8-234">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="558f8-235">Lägg till egenskapen LinkIdentifier i PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="558f8-235">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="558f8-236">Uppdaterade New-AzPrivateLinkService för att lägga till den nya valfria parametern EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="558f8-236">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="558f8-237">Korrigera felaktig beskrivning av parameter i referensdokumentationen för New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="558f8-237">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="558f8-238">Nya cmdletar som stöder Azure-brandväggsprincipen</span><span class="sxs-lookup"><span data-stu-id="558f8-238">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="558f8-239">Lägg till stöd för den underordnade resursen RouteTables för VirtualHub</span><span class="sxs-lookup"><span data-stu-id="558f8-239">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="558f8-240">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="558f8-240">New cmdlets added:</span></span>
        - <span data-ttu-id="558f8-241">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="558f8-241">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="558f8-242">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="558f8-242">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="558f8-243">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="558f8-243">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="558f8-244">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="558f8-244">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="558f8-245">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="558f8-245">Set-AzVirtualHub</span></span>
* <span data-ttu-id="558f8-246">Lägg till stöd för ny egenskaps-SKU för VirtualHub och VirtualWANType för VirtualWan</span><span class="sxs-lookup"><span data-stu-id="558f8-246">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="558f8-247">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="558f8-247">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="558f8-248">New-AzVirtualHub: lade till parameter-SKU</span><span class="sxs-lookup"><span data-stu-id="558f8-248">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="558f8-249">Update-AzVirtualHub: lade till parameter-SKU</span><span class="sxs-lookup"><span data-stu-id="558f8-249">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="558f8-250">New-AzVirtualWan: lade till parametern VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="558f8-250">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="558f8-251">Update-AzVirtualWan: lade till parametern VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="558f8-251">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="558f8-252">Lägg till stöd för egenskapen EnableInternetSecurity för HubVnetConnection, VpnConnection och ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="558f8-252">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="558f8-253">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="558f8-253">New cmdlets added:</span></span>
        - <span data-ttu-id="558f8-254">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="558f8-254">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="558f8-255">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="558f8-255">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="558f8-256">New-AzureRmVirtualHubVnetConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="558f8-256">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="558f8-257">New-AzureRmVpnConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="558f8-257">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="558f8-258">Update-AzureRmVpnConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="558f8-258">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="558f8-259">New-AzureRmExpressRouteConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="558f8-259">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="558f8-260">Set-AzureRmExpressRouteConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="558f8-260">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="558f8-261">Lägg till stöd för att konfigurera TopLevel WebApplicationFirewall-princip</span><span class="sxs-lookup"><span data-stu-id="558f8-261">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="558f8-262">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="558f8-262">New cmdlets added:</span></span>
        - <span data-ttu-id="558f8-263">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="558f8-263">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="558f8-264">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="558f8-264">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="558f8-265">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="558f8-265">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="558f8-266">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="558f8-266">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="558f8-267">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="558f8-267">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="558f8-268">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="558f8-268">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="558f8-269">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="558f8-269">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="558f8-270">New-AzApplicationGatewayFirewallPolicy: parametrarna PolicySetting, ManagedRule har lagts till</span><span class="sxs-lookup"><span data-stu-id="558f8-270">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="558f8-271">Stöd för operator för geomatchning har lagts till på CustomRule</span><span class="sxs-lookup"><span data-stu-id="558f8-271">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="558f8-272">Geomatchning har lagts till i operatorn på FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="558f8-272">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="558f8-273">Stöd har lagts till för brandväggsprinciperna perListener och perSite</span><span class="sxs-lookup"><span data-stu-id="558f8-273">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="558f8-274">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="558f8-274">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="558f8-275">New-AzApplicationGatewayHttpListener: parametrarna FirewallPolicy, FirewallPolicyId har lagts till</span><span class="sxs-lookup"><span data-stu-id="558f8-275">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="558f8-276">New-AzApplicationGatewayPathRuleConfig: parametrarna FirewallPolicy, FirewallPolicyId har lagts till</span><span class="sxs-lookup"><span data-stu-id="558f8-276">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="558f8-277">Åtgärdat så att nödvändigt undernät med namnet AzureBastionSubnet i PSBastion kan vara skiftlägesokänsligt</span><span class="sxs-lookup"><span data-stu-id="558f8-277">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="558f8-278">Stöd för mål-FQDN:er i nätverksregler och översatt FQDN i NAT-regler för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="558f8-278">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="558f8-279">Lägg till stöd för resursen RouteTables för IpGroup på den högsta nivån</span><span class="sxs-lookup"><span data-stu-id="558f8-279">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="558f8-280">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="558f8-280">New cmdlets added:</span></span>
        - <span data-ttu-id="558f8-281">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="558f8-281">New-AzIpGroup</span></span>
        - <span data-ttu-id="558f8-282">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="558f8-282">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="558f8-283">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="558f8-283">Get-AzIpGroup</span></span>
        - <span data-ttu-id="558f8-284">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="558f8-284">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="558f8-285">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="558f8-285">Az.ServiceFabric</span></span>
* <span data-ttu-id="558f8-286">Ta bort cmdleten Add-AzServiceFabricApplicationCertificate eftersom det här scenariot omfattas av Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="558f8-286">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="558f8-287">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="558f8-287">Az.Sql</span></span>
* <span data-ttu-id="558f8-288">Stöd har lagts till för återställning av utelämnade databaser på hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="558f8-288">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="558f8-289">Inaktuella gamla cmdletar för granskning från kod.</span><span class="sxs-lookup"><span data-stu-id="558f8-289">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="558f8-290">Tog bort inaktuella alias:</span><span class="sxs-lookup"><span data-stu-id="558f8-290">Removed deprecated aliases:</span></span>
* <span data-ttu-id="558f8-291">Get-AzSqlDatabaseIndexRecommendations (använd Get-AzSqlDatabaseIndexRecommendation istället)</span><span class="sxs-lookup"><span data-stu-id="558f8-291">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="558f8-292">Get-AzSqlDatabaseRestorePoints (använd Get-AzSqlDatabaseRestorePoint istället)</span><span class="sxs-lookup"><span data-stu-id="558f8-292">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="558f8-293">Ta bort cmdleten Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="558f8-293">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="558f8-294">Ta bort alias för inaktuella cmdletar för inställningar för utvärdering av säkerhetsrisk</span><span class="sxs-lookup"><span data-stu-id="558f8-294">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="558f8-295">Inaktualisera cmdletar för inställningar för avancerad hotidentifiering</span><span class="sxs-lookup"><span data-stu-id="558f8-295">Deprecate Advanced Threat Detection Settings cmdlets</span></span> 
* <span data-ttu-id="558f8-296">Lägga till cmdletar för att inaktivera och aktivera känslighetsrekommendationer på kolumner i en databas.</span><span class="sxs-lookup"><span data-stu-id="558f8-296">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="558f8-297">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="558f8-297">Az.Storage</span></span>
* <span data-ttu-id="558f8-298">Stöd för att aktivera stora filresurser vid skapande eller uppdatering av lagringskonto</span><span class="sxs-lookup"><span data-stu-id="558f8-298">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="558f8-299">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="558f8-299">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="558f8-300">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="558f8-300">Set-AzStorageAccount</span></span>
* <span data-ttu-id="558f8-301">När du stänger/hämtar en filreferens kan du hoppa över kontrollen av huruvida indatasökvägen är en filkatalog eller en fil för att undvika problem med objekt som har status DeletePending</span><span class="sxs-lookup"><span data-stu-id="558f8-301">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="558f8-302">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="558f8-302">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="558f8-303">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="558f8-303">Close-AzStorageFileHandle</span></span>
    
## <a name="280---october-2019"></a><span data-ttu-id="558f8-304">2.8.0 – oktober 2019</span><span class="sxs-lookup"><span data-stu-id="558f8-304">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="558f8-305">Allmänt</span><span class="sxs-lookup"><span data-stu-id="558f8-305">General</span></span>
* <span data-ttu-id="558f8-306">AZ. HealthcareApis 1.0.0-version</span><span class="sxs-lookup"><span data-stu-id="558f8-306">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="558f8-307">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="558f8-307">Az.Accounts</span></span>
* <span data-ttu-id="558f8-308">Uppdatera telemetri och URL-omskrivning för genererade moduler, korrigera Windows-enhetstester.</span><span class="sxs-lookup"><span data-stu-id="558f8-308">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="558f8-309">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="558f8-309">Az.ApiManagement</span></span>
* <span data-ttu-id="558f8-310">**Set-AzApiManagementApi** – Tillagt stöd för att uppdatera Api till ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="558f8-310">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="558f8-311">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="558f8-311">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="558f8-312">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="558f8-312">Az.Automation</span></span>
* <span data-ttu-id="558f8-313">Åtgärdade cmdleten New-AzureAutomationSoftwareUpdateConfiguration för parametern för inställning av Linux-omstart.</span><span class="sxs-lookup"><span data-stu-id="558f8-313">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="558f8-314">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="558f8-314">Az.Batch</span></span>
* <span data-ttu-id="558f8-315">**Get-AzBatchNodeAgentSku** är inaktuell och ersätts av **Get-AzBatchSupportImage** i version 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="558f8-315">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="558f8-316">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="558f8-316">Az.Compute</span></span>
* <span data-ttu-id="558f8-317">Lägg till parametrarna Priority, EvictionPolicy och MaxPrice till cmdletarna New-AzVM och New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="558f8-317">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="558f8-318">Korrigera varningsmeddelande och hjälpdokument för cmdletarna Add-AzVMAdditionalUnattendContent och Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="558f8-318">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="558f8-319">Åtgärda – skipVmBackup-undantag för virtuella Linux-datorer med hanterade diskar för Set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="558f8-319">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="558f8-320">Åtgärda fel i uppdatera krypteringsinställningarna i set-AzVMDiskEncryptionExtension, scenario i två steg.</span><span class="sxs-lookup"><span data-stu-id="558f8-320">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="558f8-321">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="558f8-321">Az.DataFactory</span></span>
* <span data-ttu-id="558f8-322">Lägga till CRUD-kommandon för ADF V2-dataflödet: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow och Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="558f8-322">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="558f8-323">Lägger till åtgärdskommandon för ADF V2-dataflödesfelsökningssession: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand och Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="558f8-323">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="558f8-324">Uppdatera ADF .Net SDK-versionen till 4.2.0</span><span class="sxs-lookup"><span data-stu-id="558f8-324">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="558f8-325">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="558f8-325">Az.DataLakeStore</span></span>
* <span data-ttu-id="558f8-326">Korrigera kontovalidering så att konton med ”-” kan skickas utan domän</span><span class="sxs-lookup"><span data-stu-id="558f8-326">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="558f8-327">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="558f8-327">Az.HealthcareApis</span></span>
* <span data-ttu-id="558f8-328">PowerShell-versionen har uppdaterats till 1.0.0</span><span class="sxs-lookup"><span data-stu-id="558f8-328">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="558f8-329">Uppdaterade SDK-versionen till 1.0.2</span><span class="sxs-lookup"><span data-stu-id="558f8-329">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="558f8-330">Uppdatera i tester för att referera till en ny SDK-version</span><span class="sxs-lookup"><span data-stu-id="558f8-330">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="558f8-331">Utdatastrukturen har uppdaterats från kapslad till förenklad.</span><span class="sxs-lookup"><span data-stu-id="558f8-331">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="558f8-332">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="558f8-332">Az.IotHub</span></span>
* <span data-ttu-id="558f8-333">Lägg till ny routningskälla: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="558f8-333">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="558f8-334">Mindre felkorrigering: Get-AzIothub returnerar inte subscriptionId</span><span class="sxs-lookup"><span data-stu-id="558f8-334">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="558f8-335">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="558f8-335">Az.Monitor</span></span>
* <span data-ttu-id="558f8-336">Nya åtgärdsgruppsmottagare har lagts till för åtgärdsgrupp   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="558f8-336">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="558f8-337">Använd vanligt aviseringsschema som är aktiverat för mottagarna.</span><span class="sxs-lookup"><span data-stu-id="558f8-337">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="558f8-338">Detta gäller inte för SMS, push för Azure-app, ITSM och röstmottagare</span><span class="sxs-lookup"><span data-stu-id="558f8-338">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="558f8-339">Webhooks har nu stöd för Azure Active Directory-autentisering.</span><span class="sxs-lookup"><span data-stu-id="558f8-339">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="558f8-340">Az.Network</span><span class="sxs-lookup"><span data-stu-id="558f8-340">Az.Network</span></span>
* <span data-ttu-id="558f8-341">Lägg till ny cmdlet Get-AzAvailableServiceAlias som kan anropas för att hämta de alias som kan användas för tjänstslutpunktsprinciper.</span><span class="sxs-lookup"><span data-stu-id="558f8-341">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="558f8-342">Stöd för tillägg av trafikväljare har lagts till i gatewayanslutningar för virtuella nätverk</span><span class="sxs-lookup"><span data-stu-id="558f8-342">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="558f8-343">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="558f8-343">New cmdlets added:</span></span>
        - <span data-ttu-id="558f8-344">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="558f8-344">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="558f8-345">Cmdletar har uppdaterats med valfri parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="558f8-345">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="558f8-346">Lägg till stöd för ESP- och AH-protokoll i konfiguration av nätverkssäkerhetsregler</span><span class="sxs-lookup"><span data-stu-id="558f8-346">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="558f8-347">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="558f8-347">Updated cmdlets:</span></span>
        - <span data-ttu-id="558f8-348">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="558f8-348">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="558f8-349">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="558f8-349">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="558f8-350">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="558f8-350">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="558f8-351">Förbättra hanteringen av undantag i Cortex-cmdletar</span><span class="sxs-lookup"><span data-stu-id="558f8-351">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="558f8-352">Nya generationer och SKU:er för VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="558f8-352">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="558f8-353">Introducera nya generationer för VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="558f8-353">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="558f8-354">Introducera nya SKU:er med högt dataflöde för VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="558f8-354">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="558f8-355">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="558f8-355">Az.RedisCache</span></span>
* <span data-ttu-id="558f8-356">Uppdaterad referensdokumentation för ”set-AzRedisCache” för att inkludera saknade värden för parametern ”size”</span><span class="sxs-lookup"><span data-stu-id="558f8-356">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="558f8-357">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="558f8-357">Az.Sql</span></span>
* <span data-ttu-id="558f8-358">Lägg till stöd för inställningen Active Directory administratör på den hanterade instansen</span><span class="sxs-lookup"><span data-stu-id="558f8-358">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="558f8-359">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="558f8-359">Az.Storage</span></span>
* <span data-ttu-id="558f8-360">Uppdatera Lagringsklientbibliotek till 11.1.0</span><span class="sxs-lookup"><span data-stu-id="558f8-360">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="558f8-361">Lista containrar med hanteringsplans-API, kommer att listas med NextPageLink</span><span class="sxs-lookup"><span data-stu-id="558f8-361">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="558f8-362">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="558f8-362">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="558f8-363">Lista lagringskonton från prenumerationen, kommer att listas med NextPageLink</span><span class="sxs-lookup"><span data-stu-id="558f8-363">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="558f8-364">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="558f8-364">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="558f8-365">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="558f8-365">Az.StorageSync</span></span>
* <span data-ttu-id="558f8-366">Åtgärda problemet 9810 i Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="558f8-366">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="558f8-367">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="558f8-367">Az.Websites</span></span>
* <span data-ttu-id="558f8-368">Set-AzWebApp – uppdatering av ASP för en app misslyckades</span><span class="sxs-lookup"><span data-stu-id="558f8-368">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="558f8-369">2.7.0 – september 2019</span><span class="sxs-lookup"><span data-stu-id="558f8-369">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="558f8-370">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="558f8-370">Az.ApiManagement</span></span>
* <span data-ttu-id="558f8-371">Uppdatera ”-Format”-parameterbeskrivningen i ”Set-AzApiManagementPolicy”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="558f8-371">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="558f8-372">Referenser för den föråldrade cmdleten ”Update-AzApiManagementDeployment” har tagits bort från referensdokumentationen.</span><span class="sxs-lookup"><span data-stu-id="558f8-372">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="558f8-373">Använd ”Set-AzApiManagement” i stället.</span><span class="sxs-lookup"><span data-stu-id="558f8-373">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="558f8-374">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="558f8-374">Az.Automation</span></span>
* <span data-ttu-id="558f8-375">Stavfel har korrigerats i exempel i referensdokumentationen för ”Register-AzAutomationDscNode”</span><span class="sxs-lookup"><span data-stu-id="558f8-375">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="558f8-376">Klargörande har lagts till om OS-begränsningar för Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="558f8-376">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="558f8-377">Null-referensundantag har korrigerats för -Wait-alternativet i Start-AzAutomationRunbook-cmdleten.</span><span class="sxs-lookup"><span data-stu-id="558f8-377">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="558f8-378">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="558f8-378">Az.Compute</span></span>
* <span data-ttu-id="558f8-379">Lägg till UploadSizeInBytes-parameter till New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="558f8-379">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="558f8-380">Lägg till Incremental-parameter till New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="558f8-380">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="558f8-381">Lägg till en funktion för virtuella datorer med låg prioritet:</span><span class="sxs-lookup"><span data-stu-id="558f8-381">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="558f8-382">MaxPrice-, EvictionPolicy- och Priority-parametrar har lagts till i New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="558f8-382">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="558f8-383">MaxPrice-parametern har lagts till i New-AzVmssConfig-, Update-AzVM- och Update-AzVmss-cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="558f8-383">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="558f8-384">Åtgärda problem med VM-referenser för Get-AzAvailabilitySet-cmdleten när alla tillgänglighetsuppsättningar i prenumerationen visas.</span><span class="sxs-lookup"><span data-stu-id="558f8-384">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="558f8-385">Korrigera null-undantaget för Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="558f8-385">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="558f8-386">Korrigera VHD-metoden för sökning relativt till slut.</span><span class="sxs-lookup"><span data-stu-id="558f8-386">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="558f8-387">Åtgärda UltraSSD-problem för New-AzVM och Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="558f8-387">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="558f8-388">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="558f8-388">Az.DataFactory</span></span>
* <span data-ttu-id="558f8-389">Lägger till 3 nya kommandon för ADF V2 – Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription och Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="558f8-389">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="558f8-390">ADF .Net SDK har uppdaterats till 4.1.3</span><span class="sxs-lookup"><span data-stu-id="558f8-390">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="558f8-391">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="558f8-391">Az.HDInsight</span></span>
* <span data-ttu-id="558f8-392">Anrop för icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="558f8-392">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="558f8-393">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="558f8-393">Az.IotHub</span></span>
* <span data-ttu-id="558f8-394">Lägg till stöd för att anropa redundans för en IotHub till den geo-länkade katastrofåterställningsregionen.</span><span class="sxs-lookup"><span data-stu-id="558f8-394">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="558f8-395">Lägg till stöd för att hantera meddelandeberikning för en IotHub.</span><span class="sxs-lookup"><span data-stu-id="558f8-395">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="558f8-396">Nya cmdlet:ar är:</span><span class="sxs-lookup"><span data-stu-id="558f8-396">New cmdlets are:</span></span>
    - <span data-ttu-id="558f8-397">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="558f8-397">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="558f8-398">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="558f8-398">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="558f8-399">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="558f8-399">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="558f8-400">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="558f8-400">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="558f8-401">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="558f8-401">Az.Monitor</span></span>
* <span data-ttu-id="558f8-402">Pekar på den senaste Monitor SDK:n, dvs. 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="558f8-402">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="558f8-403">Lägger till bakåtkompatibla ändringar i Metrics-cmdletarna, dvs. enhetsuppräkningen stöder flera nya värden.</span><span class="sxs-lookup"><span data-stu-id="558f8-403">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="558f8-404">Detta är skrivskyddade cmdletar, så det förekommer inga ändringar i inmatningen för cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="558f8-404">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="558f8-405">API-versionen för **ActionGroups**-begäranden är nu **2019-06-01**. Tidigare var den **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="558f8-405">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="558f8-406">Test av scenarier har uppdaterats för att anpassas till den här ändringen.</span><span class="sxs-lookup"><span data-stu-id="558f8-406">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="558f8-407">Ett nytt obligatoriskt argument har lagts till för konstruktorerna för klasserna **EmailReceiver** och **WebhookReceiver** – ett booleskt värde med namnet **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="558f8-407">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="558f8-408">Värdet är för närvarande fast till **false** så att den här icke-bakåtkompatibla ändringen är dold från cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="558f8-408">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="558f8-409">**Obs!** Det här är en tillfällig ändring som måste verifieras av Alerts-teamet.</span><span class="sxs-lookup"><span data-stu-id="558f8-409">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="558f8-410">Ordningen på argumenten för konstruktorn för klassen **Source** (relaterad till klassen **ScheduledQueryRuleSource**) har ändrats från den tidigare SDK:n.</span><span class="sxs-lookup"><span data-stu-id="558f8-410">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="558f8-411">Den här ändringen krävde korrigering av två enhetstest: de kompilerades, men testerna skickades inte.</span><span class="sxs-lookup"><span data-stu-id="558f8-411">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="558f8-412">Ordningen på argumenten för konstruktorn för klassen **AlertingAction** (relaterad till klassen **ScheduledQueryRuleSource**) har ändrats från den tidigare SDK:n.</span><span class="sxs-lookup"><span data-stu-id="558f8-412">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="558f8-413">Den här ändringen krävde korrigering av två enhetstest: de kompilerades, men testerna skickades inte.</span><span class="sxs-lookup"><span data-stu-id="558f8-413">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="558f8-414">Stöd för kriterier för dynamiskt tröskelvärde för måttavisering v2</span><span class="sxs-lookup"><span data-stu-id="558f8-414">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="558f8-415">New-AzMetricAlertRuleV2Criteria: skapar nu även kriterier för dynamiskt tröskelvärde</span><span class="sxs-lookup"><span data-stu-id="558f8-415">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="558f8-416">Add-AzMetricAlertRuleV2: accepterar nu även kriterier för dynamiskt tröskelvärde</span><span class="sxs-lookup"><span data-stu-id="558f8-416">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="558f8-417">Förbättringar i schemalagd frågeregel (SQR)</span><span class="sxs-lookup"><span data-stu-id="558f8-417">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="558f8-418">Cmdletar accepterar ”Location”-parameter i båda formaten, antingen platsen (t.ex. eastus) eller platsens visningsnamn (t.ex. USA, östra)</span><span class="sxs-lookup"><span data-stu-id="558f8-418">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="558f8-419">”Enabled”-parametern illustreras korrekt i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="558f8-419">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="558f8-420">Exempel för den valfria parametern ”ActionGroup” har lagts till</span><span class="sxs-lookup"><span data-stu-id="558f8-420">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="558f8-421">Förbättrade hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="558f8-421">Overall improved help files</span></span>
* <span data-ttu-id="558f8-422">Åtgärda bugg då omfattningstypen fastställs för ”Set-AzActionRule”</span><span class="sxs-lookup"><span data-stu-id="558f8-422">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="558f8-423">Az.Network</span><span class="sxs-lookup"><span data-stu-id="558f8-423">Az.Network</span></span>
* <span data-ttu-id="558f8-424">Korrigera felaktigt exempel i referensdokumentationen för ”New-AzApplicationGateway”</span><span class="sxs-lookup"><span data-stu-id="558f8-424">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="558f8-425">Lägg till anmärkning i ”Get-AzNetworkWatcherPacketCapture”-referensdokumentationen om hämtning av alla egenskaper för en paketinsamling</span><span class="sxs-lookup"><span data-stu-id="558f8-425">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="558f8-426">Exempel har korrigerats i ”Test-AzNetworkWatcherIPFlow”-referensdokumentationen för korrekt uppräkning av nätverkskort</span><span class="sxs-lookup"><span data-stu-id="558f8-426">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="558f8-427">Förbättrad tolkning av molnundantag för att visa eventuell ytterligare information</span><span class="sxs-lookup"><span data-stu-id="558f8-427">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="558f8-428">Förbättrad tolkning av molnundantag för att hantera ytterligare en typ av SDK-undantag</span><span class="sxs-lookup"><span data-stu-id="558f8-428">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="558f8-429">Felaktig mappning av säkerhetsregelmodeller har korrigerats</span><span class="sxs-lookup"><span data-stu-id="558f8-429">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="558f8-430">Egenskaper har lagts till för nätverksgränssnittet för funktionen Privat IP</span><span class="sxs-lookup"><span data-stu-id="558f8-430">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="558f8-431">Egenskapen ”PrivateEndpoint” har lagts till som en typ av PSResourceId till PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="558f8-431">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="558f8-432">Egenskapen ”PrivateLinkConnectionProperties” har lagts till som en typ av PSIpConfigurationConnectivityInformation till PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="558f8-432">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="558f8-433">Modellklassen PSIpConfigurationConnectivityInformation har lagts till</span><span class="sxs-lookup"><span data-stu-id="558f8-433">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="558f8-434">ApplicationRuleProtocolType ”mssql” har lagts till för Azure Firewall-resurs</span><span class="sxs-lookup"><span data-stu-id="558f8-434">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="558f8-435">MultiLink-stöd i virtuellt WAN</span><span class="sxs-lookup"><span data-stu-id="558f8-435">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="558f8-436">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="558f8-436">New cmdlets</span></span>
        - <span data-ttu-id="558f8-437">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="558f8-437">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="558f8-438">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="558f8-438">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="558f8-439">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="558f8-439">Updated cmdlet:</span></span>
        - <span data-ttu-id="558f8-440">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="558f8-440">New-VpnSite</span></span>
        - <span data-ttu-id="558f8-441">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="558f8-441">Update-VpnSite</span></span>
        - <span data-ttu-id="558f8-442">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="558f8-442">New-VpnConnection</span></span>
        - <span data-ttu-id="558f8-443">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="558f8-443">Update-VpnConnection</span></span>
* <span data-ttu-id="558f8-444">Dokument för vissa PowerShell-exempel har korrigerats så att Az-cmdletar används i stället för AzureRM-cmdletar</span><span class="sxs-lookup"><span data-stu-id="558f8-444">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="558f8-445">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="558f8-445">Az.RecoveryServices</span></span>
* <span data-ttu-id="558f8-446">Uppdatera AzureVMpolicy-objekt med ProtectedItemsCount-attribut</span><span class="sxs-lookup"><span data-stu-id="558f8-446">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="558f8-447">Ytterligare tester har lagts till för VM-princip och återställning av ursprungligt lagringskonto</span><span class="sxs-lookup"><span data-stu-id="558f8-447">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="558f8-448">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="558f8-448">Az.Resources</span></span>
* <span data-ttu-id="558f8-449">Åtgärda fel där det inte gick att anropa New-AzRoleAssignment utan parametern Scope.</span><span class="sxs-lookup"><span data-stu-id="558f8-449">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="558f8-450">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="558f8-450">Az.ServiceFabric</span></span>
* <span data-ttu-id="558f8-451">Stavfel har korrigerats i exempel för ”Update-AzServiceFabricReliability”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="558f8-451">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="558f8-452">Lägger till nya cmdletar för att hantera program och tjänster:</span><span class="sxs-lookup"><span data-stu-id="558f8-452">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="558f8-453">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="558f8-453">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="558f8-454">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="558f8-454">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="558f8-455">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="558f8-455">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="558f8-456">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="558f8-456">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="558f8-457">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="558f8-457">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="558f8-458">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="558f8-458">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="558f8-459">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="558f8-459">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="558f8-460">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="558f8-460">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="558f8-461">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="558f8-461">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="558f8-462">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="558f8-462">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="558f8-463">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="558f8-463">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="558f8-464">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="558f8-464">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="558f8-465">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="558f8-465">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="558f8-466">Service Fabric SDK har uppgraderats till version 1.2.0 som använder Service Fabric-resursprovidern med API-version 2019-03-01.</span><span class="sxs-lookup"><span data-stu-id="558f8-466">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="558f8-467">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="558f8-467">Az.SignalR</span></span>
* <span data-ttu-id="558f8-468">Lägg till Update-, Restart-, CheckNameAvailability- och GetUsage-cmdletar</span><span class="sxs-lookup"><span data-stu-id="558f8-468">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="558f8-469">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="558f8-469">Az.Sql</span></span>
* <span data-ttu-id="558f8-470">Uppdatera exempel i referensdokumentationen för ”Get-AzSqlElasticPool”</span><span class="sxs-lookup"><span data-stu-id="558f8-470">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="558f8-471">vCore-exempel för att skapa en elastisk pool (New-AzSqlElasticPool) har lagts till.</span><span class="sxs-lookup"><span data-stu-id="558f8-471">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="558f8-472">Ta bort verifieringen av EmailAddresses och kontrollen som bekräftar att EmailAdmins inte är falskt när EmailAddresses är tomt i Set-AzSqlServerAdvancedThreatProtectionPolicy och Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="558f8-472">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="558f8-473">Server-/databasgranskningsinställningar kan tas bort när det finns flera diagnostikinställningar som aktiverar granskningskategorin.</span><span class="sxs-lookup"><span data-stu-id="558f8-473">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="558f8-474">Åtgärda verifiering av e-postadresser i flera Sql Vulnerability Assessment-cmdletar (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting och Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="558f8-474">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="558f8-475">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="558f8-475">Az.Storage</span></span>
* <span data-ttu-id="558f8-476">Exempel i referensdokumentationen för ”Get-AzStorageAccountKey” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="558f8-476">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="558f8-477">Vid upp- och nedladdning av en Azure-fil kan SMB-egenskaperna för källfilen (t.ex. filattribut, tidpunkten då filen skapades och tidpunkten för den senaste skrivningen) sparas i målfilen</span><span class="sxs-lookup"><span data-stu-id="558f8-477">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="558f8-478">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="558f8-478">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="558f8-479">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="558f8-479">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="558f8-480">Korrigera problem med uppladdningen av blockblob med egenskaper/metadata för ImmutabilityPolicy i containrar.</span><span class="sxs-lookup"><span data-stu-id="558f8-480">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="558f8-481">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="558f8-481">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="558f8-482">Stöd för hantering av Azure-filresurser med API för hanteringsplan</span><span class="sxs-lookup"><span data-stu-id="558f8-482">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="558f8-483">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="558f8-483">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="558f8-484">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="558f8-484">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="558f8-485">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="558f8-485">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="558f8-486">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="558f8-486">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="558f8-487">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="558f8-487">Az.Websites</span></span>
* <span data-ttu-id="558f8-488">Åtgärdar problemet där webapp-taggar togs bort när appen migrerades till nya ASP</span><span class="sxs-lookup"><span data-stu-id="558f8-488">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="558f8-489">Åtgärda Publish-AzureWebapp så att det fungerar i Linux och Windows</span><span class="sxs-lookup"><span data-stu-id="558f8-489">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="558f8-490">Uppdatera exempel i ”Get-AzWebAppPublishingProfile”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="558f8-490">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="558f8-491">2.6.0 – augusti 2019</span><span class="sxs-lookup"><span data-stu-id="558f8-491">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="558f8-492">Allmänt</span><span class="sxs-lookup"><span data-stu-id="558f8-492">General</span></span>
* <span data-ttu-id="558f8-493">Åtgärdade diverse skrivfel i flera moduler</span><span class="sxs-lookup"><span data-stu-id="558f8-493">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="558f8-494">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="558f8-494">Az.Accounts</span></span>
* <span data-ttu-id="558f8-495">Stöd för användartilldelat MSI i Azure Functions-autentisering (#9479)</span><span class="sxs-lookup"><span data-stu-id="558f8-495">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="558f8-496">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="558f8-496">Az.Aks</span></span>
* <span data-ttu-id="558f8-497">Åtgärda problem med utdata för "Get-AzAks"</span><span class="sxs-lookup"><span data-stu-id="558f8-497">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="558f8-498">Mer information här: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="558f8-498">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="558f8-499">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="558f8-499">Az.ApiManagement</span></span>
* <span data-ttu-id="558f8-500">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="558f8-500">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="558f8-501">Uppdatera .net-NuGet-versionen, som inte tillämpar begränsningar för productId, apiId och userId</span><span class="sxs-lookup"><span data-stu-id="558f8-501">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="558f8-502">**Get-AzApiManagementProduct** – Lade till stöd för frågekörning mot produkter via API.</span><span class="sxs-lookup"><span data-stu-id="558f8-502">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="558f8-503">**New-AzApiManagementApiRevision** – Korrigering för problem där ApiRevisionDescription inte angavs vid skapande av ny API-revision https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="558f8-503">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="558f8-504">Åtgärdade skrivfel i modellen "PsApiManagementOAuth2AuthrozationServer" till "PsApiManagementOAuth2AuthorizationServer"</span><span class="sxs-lookup"><span data-stu-id="558f8-504">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="558f8-505">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="558f8-505">Az.Batch</span></span>
* <span data-ttu-id="558f8-506">Åtgärdade skrivfel i hjälpmeddelande och dokumentation till att skriva Windows med versaler</span><span class="sxs-lookup"><span data-stu-id="558f8-506">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="558f8-507">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="558f8-507">Az.Cdn</span></span>
* <span data-ttu-id="558f8-508">Åtgärdade skrivfel i CDN-modulens konverteringshjälp</span><span class="sxs-lookup"><span data-stu-id="558f8-508">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="558f8-509">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="558f8-509">Az.Compute</span></span>
* <span data-ttu-id="558f8-510">Lägg till VmssId i New-AzVMConfig-cmdleten</span><span class="sxs-lookup"><span data-stu-id="558f8-510">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="558f8-511">Lägg till parametrarna TerminateScheduledEvents och TerminateScheduledEventNotBeforeTimeoutInMinutes i New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="558f8-511">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="558f8-512">Lägg till egenskapen HyperVGeneration till avbildningsobjekt för virtuell dator</span><span class="sxs-lookup"><span data-stu-id="558f8-512">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="558f8-513">Lägg till funktioner för Host och HostGroup</span><span class="sxs-lookup"><span data-stu-id="558f8-513">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="558f8-514">Nya cmdletar:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="558f8-514">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="558f8-515">HostId-parametern läggs till i New-AzVMConfig och New-AzVM</span><span class="sxs-lookup"><span data-stu-id="558f8-515">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="558f8-516">Uppdatera exempel i "Invoke-AzVMRunCommand"-dokumentationen till att använda rätt parameternamn</span><span class="sxs-lookup"><span data-stu-id="558f8-516">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="558f8-517">Uppdatera "-VolumeType"-beskrivningen i referensdokumentationen för "set-AzVMDiskEncryptionExtension" och "set-AzVmssDiskEncryptionExtension"</span><span class="sxs-lookup"><span data-stu-id="558f8-517">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="558f8-518">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="558f8-518">Az.DataFactory</span></span>
* <span data-ttu-id="558f8-519">Åtgärda skrivfel till att använda versaler för "Windows" i "New-AzDataFactoryEncryptValue"-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="558f8-519">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="558f8-520">Uppdaterade ADF .Net SDK-versionen till 4.1.2</span><span class="sxs-lookup"><span data-stu-id="558f8-520">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="558f8-521">Lägg till parametrarna "DataProxyIntegrationRuntimeName", "DataProxyStagingLinkedServiceName" och "DataProxyStagingPath" för "Set-AzureRmDataFactoryV2IntegrationRuntime"-cmd för att aktivera konfiguration av lokalt installerad integrationskörning som en proxy för SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="558f8-521">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="558f8-522">Uppdaterade PSTriggerRun till att visa utlöst pipeline, meddelande och egenskaper samt PSActivityRun till att visa aktivitetstypen</span><span class="sxs-lookup"><span data-stu-id="558f8-522">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="558f8-523">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="558f8-523">Az.DataLakeStore</span></span>
* <span data-ttu-id="558f8-524">Korrigering av frysning av Get-DataLakeStoreDeletedItem för fel eller fjärrundantag.</span><span class="sxs-lookup"><span data-stu-id="558f8-524">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="558f8-525">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="558f8-525">Az.EventHub</span></span>
* <span data-ttu-id="558f8-526">Korrigering av problem #9658 : Skrivfel i parametern VirtualNteworkRule i Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="558f8-526">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="558f8-527">Korrigering av problem #9558 : Set-AzEventHubNamespace använder PATCH i stället för PUT</span><span class="sxs-lookup"><span data-stu-id="558f8-527">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="558f8-528">lade till parametern EnableKafka i Set-AzEventHubNamespace-cmdleten</span><span class="sxs-lookup"><span data-stu-id="558f8-528">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="558f8-529">Korrigering av problem #9786 : kan inte skapa en regel med Endast lyssna-behörighet</span><span class="sxs-lookup"><span data-stu-id="558f8-529">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="558f8-530">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="558f8-530">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="558f8-531">Åtgärdade skrivfel i dokumentation där "Azure" skrevs helt med gemener</span><span class="sxs-lookup"><span data-stu-id="558f8-531">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="558f8-532">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="558f8-532">Az.Monitor</span></span>
* <span data-ttu-id="558f8-533">Åtgärdade felaktigt parameternamn i hjälpdokumentationen</span><span class="sxs-lookup"><span data-stu-id="558f8-533">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="558f8-534">Az.Network</span><span class="sxs-lookup"><span data-stu-id="558f8-534">Az.Network</span></span>
* <span data-ttu-id="558f8-535">Uppdaterade New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="558f8-535">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="558f8-536">Gjorde parametern "PublicIpAddress" inaktuell eftersom den aldrig används på serversidan.</span><span class="sxs-lookup"><span data-stu-id="558f8-536">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="558f8-537">Lade till den valfria parametern "Primary", som anger huruvida den aktuella IP-konfigurationen är den primära.</span><span class="sxs-lookup"><span data-stu-id="558f8-537">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="558f8-538">Förbättrade hanteringen av felundantag för begärande från SDK – åtgärdar problemet att tidigare SDK-undantag inte hanteras på rätt sätt, vilket leder till att viktig felinformation inte visas</span><span class="sxs-lookup"><span data-stu-id="558f8-538">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="558f8-539">Justerade valideringslogiken för IPv6-IP-prefix till att kontrollera korrekt IPv6-prefixlängd.</span><span class="sxs-lookup"><span data-stu-id="558f8-539">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="558f8-540">Uppdaterade Get-AzVirtualNetworkSubnetConfig: Lade till parameter som anges till get av undernätets resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="558f8-540">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="558f8-541">Uppdaterade beskrivningen av parametern Location för AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="558f8-541">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="558f8-542">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="558f8-542">Az.OperationalInsights</span></span>
* <span data-ttu-id="558f8-543">Uppdaterade dokumentation för "New-AzOperationalInsightsLinuxSyslogDataSource"</span><span class="sxs-lookup"><span data-stu-id="558f8-543">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="558f8-544">Lade till exempel</span><span class="sxs-lookup"><span data-stu-id="558f8-544">Added example</span></span>
    - <span data-ttu-id="558f8-545">Uppdaterade beskrivningen av parametern "-Name"</span><span class="sxs-lookup"><span data-stu-id="558f8-545">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="558f8-546">Lade till ett exempel för New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="558f8-546">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="558f8-547">Ändrade beskrivningen av parametern -Name för New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="558f8-547">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="558f8-548">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="558f8-548">Az.RecoveryServices</span></span>
* <span data-ttu-id="558f8-549">Uppdatera "Get-AzRecoveryServicesBackupJobDetail.md"</span><span class="sxs-lookup"><span data-stu-id="558f8-549">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="558f8-550">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="558f8-550">Az.Resources</span></span>
* <span data-ttu-id="558f8-551">Lägg till stöd för den nya API-versionen från 2019-05-10 för Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="558f8-551">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="558f8-552">Lägg till stöd för "copy.count = 0" för variabler, resurser och egenskaper</span><span class="sxs-lookup"><span data-stu-id="558f8-552">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="558f8-553">Resurser med "condition = false" eller "copy.count = 0" tas bort i complete-läget</span><span class="sxs-lookup"><span data-stu-id="558f8-553">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="558f8-554">Lägg till ett exempel på tilldelning av princip på prenumerationsnivå i hjälpdokumentationen</span><span class="sxs-lookup"><span data-stu-id="558f8-554">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="558f8-555">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="558f8-555">Az.ServiceBus</span></span>
* <span data-ttu-id="558f8-556">Korrigering av problem #9658 : Skrivfel i parametern VirtualNetworkRule i set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="558f8-556">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="558f8-557">Korrigering av problem #9786 : kan inte skapa en regel med Endast lyssna-behörighet</span><span class="sxs-lookup"><span data-stu-id="558f8-557">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="558f8-558">Lade till det nya kommandot "Test-AzServiceBusNameAvailability" för att kontrollera namntillgängligheten för kö och ämne</span><span class="sxs-lookup"><span data-stu-id="558f8-558">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="558f8-559">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="558f8-559">Az.ServiceFabric</span></span>
* <span data-ttu-id="558f8-560">Åtgärda buggar med tillägg av nodtyps-cmdlet:</span><span class="sxs-lookup"><span data-stu-id="558f8-560">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="558f8-561">NullReferenceException-bugg när resursgrupp hade annan vmss som inte är relaterad till Service Fabric-klustret.</span><span class="sxs-lookup"><span data-stu-id="558f8-561">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="558f8-562">Åtgärdar problemet: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="558f8-562">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="558f8-563">Åtgärda bugg där cmdleten misslyckades om virtualNetwork var i en annan resursgrupp än klustret.</span><span class="sxs-lookup"><span data-stu-id="558f8-563">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="558f8-564">Åtgärdar problemet: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="558f8-564">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="558f8-565">AzServiceFabricApplicationCertificate-cmdleten görs inaktuell</span><span class="sxs-lookup"><span data-stu-id="558f8-565">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="558f8-566">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="558f8-566">Az.Sql</span></span>
* <span data-ttu-id="558f8-567">Uppdatera dokumentation om gamla gransknings-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="558f8-567">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="558f8-568">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="558f8-568">Az.Storage</span></span>
* <span data-ttu-id="558f8-569">Uppdatera hjälpen för Get/Close-AzStorageFileHandle genom att lägga till fler scenarier i cmdlet-exempel och uppdatera parameterbeskrivningar</span><span class="sxs-lookup"><span data-stu-id="558f8-569">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="558f8-570">Stöd för StandardBlobTier i uppladdningsblob och kopieringsblob</span><span class="sxs-lookup"><span data-stu-id="558f8-570">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="558f8-571">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="558f8-571">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="558f8-572">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="558f8-572">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="558f8-573">Stöd för rehydratiseringsprioritet i kopieringsblob</span><span class="sxs-lookup"><span data-stu-id="558f8-573">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="558f8-574">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="558f8-574">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="558f8-575">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="558f8-575">Az.Websites</span></span>
* <span data-ttu-id="558f8-576">Lägg till klargöranden gällande parametern -AppSettings i Set-AzWebApp och Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="558f8-576">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="558f8-577">2.5.0 – July 2019</span><span class="sxs-lookup"><span data-stu-id="558f8-577">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="558f8-578">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="558f8-578">Az.Accounts</span></span>
* <span data-ttu-id="558f8-579">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="558f8-579">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="558f8-580">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="558f8-580">Az.ApplicationInsights</span></span>
* <span data-ttu-id="558f8-581">Korrigera skrivfel i exempel i dokumentationen för Remove-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="558f8-581">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="558f8-582">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="558f8-582">Az.Automation</span></span>
* <span data-ttu-id="558f8-583">Korrigera skrivfel i resurssträng</span><span class="sxs-lookup"><span data-stu-id="558f8-583">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="558f8-584">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="558f8-584">Az.CognitiveServices</span></span>
* <span data-ttu-id="558f8-585">Stöd för NetworkRuleSet har lagts till.</span><span class="sxs-lookup"><span data-stu-id="558f8-585">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="558f8-586">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="558f8-586">Az.Compute</span></span>
* <span data-ttu-id="558f8-587">Lägg till saknade egenskaper (ComputerName, OsName, OsVersion och HyperVGeneration) för visningsobjekt i den virtuella datorinstansen.</span><span class="sxs-lookup"><span data-stu-id="558f8-587">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="558f8-588">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="558f8-588">Az.ContainerRegistry</span></span>
* <span data-ttu-id="558f8-589">Åtgärda skrivfel i Remove-AzContainerRegistryReplication för parametern Replication</span><span class="sxs-lookup"><span data-stu-id="558f8-589">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="558f8-590">Mer information finns här: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="558f8-590">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="558f8-591">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="558f8-591">Az.DataFactory</span></span>
* <span data-ttu-id="558f8-592">ADF .Net SDK-versionen har uppdaterats till 4.1.0</span><span class="sxs-lookup"><span data-stu-id="558f8-592">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="558f8-593">Korrigera skrivfel i dokumentationen för Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="558f8-593">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="558f8-594">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="558f8-594">Az.EventHub</span></span>
* <span data-ttu-id="558f8-595">Ny cmmdlet har lagts till för att skapa SAS-token: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="558f8-595">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="558f8-596">verifierings- och felmeddelande har lagts till för authorizationrules-rättigheter om endast "hantera" har tilldelats</span><span class="sxs-lookup"><span data-stu-id="558f8-596">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="558f8-597">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="558f8-597">Az.KeyVault</span></span>
* <span data-ttu-id="558f8-598">Stöd har lagts till för att ange KeySize för certifikatprinciper</span><span class="sxs-lookup"><span data-stu-id="558f8-598">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="558f8-599">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="558f8-599">Az.LogicApp</span></span>
* <span data-ttu-id="558f8-600">Korrigering för Get-AzIntegrationAccountMap för att lista alla mappningstyper</span><span class="sxs-lookup"><span data-stu-id="558f8-600">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="558f8-601">Ny MapType-parameter har lagts till för filtrering</span><span class="sxs-lookup"><span data-stu-id="558f8-601">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="558f8-602">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="558f8-602">Az.ManagedServices</span></span>
* <span data-ttu-id="558f8-603">Stöd för API-versionen 2019-06-01 (GA) har lagts till</span><span class="sxs-lookup"><span data-stu-id="558f8-603">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="558f8-604">Az.Network</span><span class="sxs-lookup"><span data-stu-id="558f8-604">Az.Network</span></span>
* <span data-ttu-id="558f8-605">Lägg till stöd för privat slutpunkt och privat länktjänst</span><span class="sxs-lookup"><span data-stu-id="558f8-605">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="558f8-606">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="558f8-606">New cmdlets</span></span>
        - <span data-ttu-id="558f8-607">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="558f8-607">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="558f8-608">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="558f8-608">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="558f8-609">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="558f8-609">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="558f8-610">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="558f8-610">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="558f8-611">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="558f8-611">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="558f8-612">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="558f8-612">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="558f8-613">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="558f8-613">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="558f8-614">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="558f8-614">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="558f8-615">Nedanstående kommandon för funktionen har uppdaterats: Flaggan PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies på undernätet i VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="558f8-615">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="558f8-616">Uppdaterade New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="558f8-616">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="558f8-617">Valfri parameter har lagts till – PrivateEndpointNetworkPoliciesFlag som konfigurerar huruvida nätverksprinciper ska tillämpas på en privat slutpunkt i det här undernätet.</span><span class="sxs-lookup"><span data-stu-id="558f8-617">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="558f8-618">Valfri parameter har lagts till – PrivateLinkServiceNetworkPoliciesFlag som konfigurerar huruvida nätverksprinciper ska tillämpas på en privat länktjänst i det här undernätet.</span><span class="sxs-lookup"><span data-stu-id="558f8-618">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="558f8-619">AzPrivateLinkService för cmdlet-parametern ServiceName har bytt namn till Name med aliaset ServiceName för bakåtkompatibilitet</span><span class="sxs-lookup"><span data-stu-id="558f8-619">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="558f8-620">Aktivera ICMP-protokoll för konfiguration av nätverkssäkerhetsregler</span><span class="sxs-lookup"><span data-stu-id="558f8-620">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="558f8-621">Uppdaterade cmdletar</span><span class="sxs-lookup"><span data-stu-id="558f8-621">Updated cmdlets</span></span>
        - <span data-ttu-id="558f8-622">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="558f8-622">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="558f8-623">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="558f8-623">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="558f8-624">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="558f8-624">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="558f8-625">Lägg till ConnectionProtocolType (Ikev1/Ikev2) som en konfigurerbar parameter för New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="558f8-625">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="558f8-626">Lägg till PrivateIpAddressVersion i LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="558f8-626">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="558f8-627">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="558f8-627">Updated cmdlet:</span></span>
        - <span data-ttu-id="558f8-628">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="558f8-628">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="558f8-629">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="558f8-629">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="558f8-630">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="558f8-630">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="558f8-631">Uppdatering av Application Gateway-kommandot New-AzApplicationGatewayProbeConfig för stöd av anpassad port i Probe</span><span class="sxs-lookup"><span data-stu-id="558f8-631">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="558f8-632">Uppdaterade New-AzApplicationGatewayProbeConfig: Den valfria parametern Port som används för avsökning i serverdelen har lagts till.</span><span class="sxs-lookup"><span data-stu-id="558f8-632">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="558f8-633">Denna parameter gäller för SKU:erna Standard_V2 och WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="558f8-633">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="558f8-634">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="558f8-634">Az.OperationalInsights</span></span>
* <span data-ttu-id="558f8-635">Uppdaterade standardversionen för sparade sökningar till 1.</span><span class="sxs-lookup"><span data-stu-id="558f8-635">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="558f8-636">Åtgärdade hantering av anpassad log null regex</span><span class="sxs-lookup"><span data-stu-id="558f8-636">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="558f8-637">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="558f8-637">Az.RecoveryServices</span></span>
* <span data-ttu-id="558f8-638">Uppdatera Get-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="558f8-638">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="558f8-639">Uppdatera Get-AzRecoveryServicesBackupContainer.md</span><span class="sxs-lookup"><span data-stu-id="558f8-639">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="558f8-640">Uppdatera Get-AzRecoveryServicesVault.md</span><span class="sxs-lookup"><span data-stu-id="558f8-640">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="558f8-641">Uppdatera Wait-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="558f8-641">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="558f8-642">Uppdatera Set-AzRecoveryServicesVaultContext.md</span><span class="sxs-lookup"><span data-stu-id="558f8-642">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="558f8-643">Uppdatera Get-AzRecoveryServicesBackupItem.md</span><span class="sxs-lookup"><span data-stu-id="558f8-643">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="558f8-644">Uppdatera Get-AzRecoveryServicesBackupRecoveryPoint.md</span><span class="sxs-lookup"><span data-stu-id="558f8-644">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="558f8-645">Uppdatera Restore-AzRecoveryServicesBackupItem.md</span><span class="sxs-lookup"><span data-stu-id="558f8-645">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="558f8-646">Uppdaterat tjänstanrop för avregistrering av container för Azure-filresurs</span><span class="sxs-lookup"><span data-stu-id="558f8-646">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="558f8-647">Uppdatera Set-AzRecoveryServicesAsrAlertSetting.md</span><span class="sxs-lookup"><span data-stu-id="558f8-647">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="558f8-648">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="558f8-648">Az.Resources</span></span>
- <span data-ttu-id="558f8-649">Ta bort den cmdlet som saknas och som refereras i dokumentationen till New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="558f8-649">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="558f8-650">Princip-cmdletar har uppdaterats så att de använder den nya API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="558f8-650">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="558f8-651">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="558f8-651">Az.ServiceBus</span></span>
* <span data-ttu-id="558f8-652">Ny cmmdlet har lagts till för att skapa SAS-token: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="558f8-652">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="558f8-653">verifierings- och felmeddelande har lagts till för authorizationrules-rättigheter om endast "hantera" har tilldelats</span><span class="sxs-lookup"><span data-stu-id="558f8-653">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="558f8-654">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="558f8-654">Az.Sql</span></span>
* <span data-ttu-id="558f8-655">Åtgärda saknade exempel för Set-AzSqlDatabaseSecondary cmdlet</span><span class="sxs-lookup"><span data-stu-id="558f8-655">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="558f8-656">Åtgärda angivna återkommande genomsökningar för bedömning av säkerhetsrisk utan angivna e-postadresser</span><span class="sxs-lookup"><span data-stu-id="558f8-656">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="558f8-657">Korrigera ett skrivfel i ett varningsmeddelande.</span><span class="sxs-lookup"><span data-stu-id="558f8-657">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="558f8-658">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="558f8-658">Az.Storage</span></span>
* <span data-ttu-id="558f8-659">Uppdatera exempel i referensdokumentationen för Get-AzStorageAccount så att rätt parameternamn används</span><span class="sxs-lookup"><span data-stu-id="558f8-659">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="558f8-660">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="558f8-660">Az.StorageSync</span></span>
* <span data-ttu-id="558f8-661">Lägger till cmdleten Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="558f8-661">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="558f8-662">Åtgärda problem 9551 så att TierFilesOlderThanDays föredras</span><span class="sxs-lookup"><span data-stu-id="558f8-662">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="558f8-663">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="558f8-663">Az.Websites</span></span>
* <span data-ttu-id="558f8-664">Åtgärdar ett fel där vissa SiteConfig-egenskaper inte returnerades av Get-AzWebApp och Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="558f8-664">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="558f8-665">Lägger till en ny platsparameter för Get-AzDeletedWebApp och Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="558f8-665">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="558f8-666">Åtgärdar ett fel i kloning av webbapp-platser som använder New-AzWebApp-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="558f8-666">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="558f8-667">2.4.0 – juli 2019</span><span class="sxs-lookup"><span data-stu-id="558f8-667">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="558f8-668">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="558f8-668">Az.Accounts</span></span>
* <span data-ttu-id="558f8-669">Lägg till stöd för profil-cmdletar</span><span class="sxs-lookup"><span data-stu-id="558f8-669">Add support for profile cmdlets</span></span>
* <span data-ttu-id="558f8-670">Lägg till stöd för miljöer och dataplaner i genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="558f8-670">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="558f8-671">Åtgärda bugg där fel slutpunkt i vissa fall användes för cmdletar för dataplaner i Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="558f8-671">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="558f8-672">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="558f8-672">Az.Advisor</span></span>
* <span data-ttu-id="558f8-673">GA-version av Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="558f8-673">GA release of Az.Advisor</span></span>
* <span data-ttu-id="558f8-674">Den här modulen ingår nu som en del av `Az`-sammanslagningsmodulen</span><span class="sxs-lookup"><span data-stu-id="558f8-674">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="558f8-675">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="558f8-675">Az.ApiManagement</span></span>
* <span data-ttu-id="558f8-676">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="558f8-676">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="558f8-677">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="558f8-677">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="558f8-678">Stöd för att fråga prenumerationer efter användare och produkt har lagts till</span><span class="sxs-lookup"><span data-stu-id="558f8-678">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="558f8-679">Stöd för att fråga med hjälp av omfång ”/”, ”/apis”, ”/apis/echo-api” har lagts till</span><span class="sxs-lookup"><span data-stu-id="558f8-679">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="558f8-680">Korrigering av problem https://github.com/Azure/azure-powershell/issues/9307 och https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="558f8-680">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="558f8-681">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="558f8-681">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="558f8-682">Stöd för att ange ”ApiVersion” och ”ApiVersionSetId” när API:er importeras har lagts till</span><span class="sxs-lookup"><span data-stu-id="558f8-682">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="558f8-683">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="558f8-683">Az.Automation</span></span>
* <span data-ttu-id="558f8-684">Bugg med cmdleten Set-AzAutomationConnectionFieldValue för att hantera strängvärde har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="558f8-684">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="558f8-685">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="558f8-685">Az.Compute</span></span>
* <span data-ttu-id="558f8-686">Lägg till parametern HyperVGeneration i New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="558f8-686">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="558f8-687">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="558f8-687">Az.DataFactory</span></span>
* <span data-ttu-id="558f8-688">Uppdaterar utdata från ADF-cmdletar som hämtar aktivitetskörningar, hämtar pipelinekörningar och hämtar utlösarkörningar för stöd för Select-Object-pipe.</span><span class="sxs-lookup"><span data-stu-id="558f8-688">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="558f8-689">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="558f8-689">Az.EventGrid</span></span>
* <span data-ttu-id="558f8-690">Korrigera stavfel i dokumentation om ”New-AzEventGridSubscription”</span><span class="sxs-lookup"><span data-stu-id="558f8-690">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="558f8-691">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="558f8-691">Az.IotHub</span></span>
* <span data-ttu-id="558f8-692">Lägg till stöd för att återskapa principnycklar för auktorisering.</span><span class="sxs-lookup"><span data-stu-id="558f8-692">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="558f8-693">Az.Network</span><span class="sxs-lookup"><span data-stu-id="558f8-693">Az.Network</span></span>
* <span data-ttu-id="558f8-694">”RoutingPreference” har lagts till i offentliga IP-taggar</span><span class="sxs-lookup"><span data-stu-id="558f8-694">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="558f8-695">Förbättra exempel för referensdokumentation om ”Get-AzNetworkServiceTag”</span><span class="sxs-lookup"><span data-stu-id="558f8-695">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="558f8-696">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="558f8-696">Az.PolicyInsights</span></span>
* <span data-ttu-id="558f8-697">Åtgärda problem med null-referens i Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="558f8-697">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="558f8-698">Mer information här: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="558f8-698">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="558f8-699">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="558f8-699">Az.OperationalInsights</span></span>
* <span data-ttu-id="558f8-700">Modellen för CustomLog-datakälla som returneras i Get-AzOperationalInsightsDataSource har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="558f8-700">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="558f8-701">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="558f8-701">Az.RecoveryServices</span></span>
* <span data-ttu-id="558f8-702">Kommandot get-policy för IaaSVM:er har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="558f8-702">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="558f8-703">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="558f8-703">Az.Resources</span></span>
    - <span data-ttu-id="558f8-704">Korrigera hjälptext för den översta parametern i Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="558f8-704">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="558f8-705">Lägg till växlingsstöd på klientsidan för Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="558f8-705">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="558f8-706">Lägg till nya parametrar för Set-AzPolicyAssignment, -PolicyParameters och -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="558f8-706">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="558f8-707">En mängd dokument- och exempeluppdateringar för Policy-cmdletar</span><span class="sxs-lookup"><span data-stu-id="558f8-707">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="558f8-708">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="558f8-708">Az.ServiceBus</span></span>
* <span data-ttu-id="558f8-709">Korrigering av problem #4938 – New-AzureRmServiceBusQueue returnerar BadRequest vid konfiguration av MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="558f8-709">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="558f8-710">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="558f8-710">Az.Sql</span></span>
* <span data-ttu-id="558f8-711">Lägg till cmdletar för instansredundansgrupper från förhandsversion till offentlig version</span><span class="sxs-lookup"><span data-stu-id="558f8-711">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="558f8-712">Stöd för granskning för Azure SQL Server\Database med nya cmdletar.</span><span class="sxs-lookup"><span data-stu-id="558f8-712">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="558f8-713">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="558f8-713">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="558f8-714">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="558f8-714">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="558f8-715">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="558f8-715">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="558f8-716">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="558f8-716">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="558f8-717">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="558f8-717">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="558f8-718">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="558f8-718">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="558f8-719">Ta bort begränsningar för e-post från inställningarna för sårbarhetsbedömning</span><span class="sxs-lookup"><span data-stu-id="558f8-719">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="558f8-720">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="558f8-720">Az.Storage</span></span>
* <span data-ttu-id="558f8-721">Ändra två parametrar ”-IndexDocument” och ”-ErrorDocument404Path” från ”krävs” till ”valfri” i cmdlet:</span><span class="sxs-lookup"><span data-stu-id="558f8-721">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="558f8-722">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="558f8-722">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="558f8-723">Uppdatera hjälpen för Get-AzStorageBlobContent genom att lägga till ett exempel</span><span class="sxs-lookup"><span data-stu-id="558f8-723">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="558f8-724">Visa mer felinformation när cmdleten misslyckas med StorageException</span><span class="sxs-lookup"><span data-stu-id="558f8-724">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="558f8-725">Stöd för att skapa eller uppdatera lagringskonto med Azure Files AAD DS-autentisering</span><span class="sxs-lookup"><span data-stu-id="558f8-725">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="558f8-726">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="558f8-726">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="558f8-727">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="558f8-727">Set-AzStorageAccount</span></span>
* <span data-ttu-id="558f8-728">Stöd för att lista eller stänga filreferenser för en filresurs, filkatalog eller en fil</span><span class="sxs-lookup"><span data-stu-id="558f8-728">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="558f8-729">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="558f8-729">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="558f8-730">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="558f8-730">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="558f8-731">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="558f8-731">Az.StorageSync</span></span>
* <span data-ttu-id="558f8-732">Den här modulen ingår nu som en del av `Az`-sammanslagningsmodulen</span><span class="sxs-lookup"><span data-stu-id="558f8-732">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="558f8-733">2.3.2 – juni 2019</span><span class="sxs-lookup"><span data-stu-id="558f8-733">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="558f8-734">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="558f8-734">Az.Accounts</span></span>
* <span data-ttu-id="558f8-735">Åtgärda bugg med felaktiga webbadresser som i vissa fall användes för Functions-anrop</span><span class="sxs-lookup"><span data-stu-id="558f8-735">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="558f8-736">Mer information här: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="558f8-736">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="558f8-737">Åtgärda problem med alias från AzureRM i Az-cmdletar</span><span class="sxs-lookup"><span data-stu-id="558f8-737">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="558f8-738">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="558f8-738">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="558f8-739">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="558f8-739">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="558f8-740">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="558f8-740">Az.Compute</span></span>
* <span data-ttu-id="558f8-741">Parameteruppsättningarna New-AzVm och New-AzVmss accepterar nu parametern ”ProximityPlacementGroup”.</span><span class="sxs-lookup"><span data-stu-id="558f8-741">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="558f8-742">Stavfel i referensdokumentationen för ”New-AzVM” har korrigerats</span><span class="sxs-lookup"><span data-stu-id="558f8-742">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="558f8-743">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="558f8-743">Az.Dns</span></span>
* <span data-ttu-id="558f8-744">Stavfel i hjälpexempel för ”Set-AzDnsZone” har korrigerats.</span><span class="sxs-lookup"><span data-stu-id="558f8-744">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="558f8-745">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="558f8-745">Az.EventGrid</span></span>
* <span data-ttu-id="558f8-746">Har uppdaterats för att använda API-versionen 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="558f8-746">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="558f8-747">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="558f8-747">New cmdlets:</span></span>
    - <span data-ttu-id="558f8-748">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="558f8-748">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="558f8-749">Skapar en ny Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="558f8-749">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="558f8-750">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="558f8-750">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="558f8-751">Hämtar information om en Event Grid-domän eller hämtar en lista med alla Event Grid-domäner i den aktuella Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="558f8-751">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="558f8-752">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="558f8-752">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="558f8-753">Tar bort en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="558f8-753">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="558f8-754">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="558f8-754">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="558f8-755">Återskapar nyckeln för delad åtkomst för en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="558f8-755">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="558f8-756">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="558f8-756">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="558f8-757">Hämtar de nycklar för delad åtkomst som används för att publicera händelser till en Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="558f8-757">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="558f8-758">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="558f8-758">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="558f8-759">Skapar ett nytt Azure Event Grid-domänämne.</span><span class="sxs-lookup"><span data-stu-id="558f8-759">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="558f8-760">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="558f8-760">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="558f8-761">Hämtar information om ett Event Grid-domänämne eller hämtar en lista med alla Event Grid-domänämnen under en specifik Event Grid-domän i nuvarande Azure</span><span class="sxs-lookup"><span data-stu-id="558f8-761">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="558f8-762">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="558f8-762">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="558f8-763">Tar bort ett befintligt Azure Event Grid-domänämne.</span><span class="sxs-lookup"><span data-stu-id="558f8-763">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="558f8-764">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="558f8-764">Updated cmdlets:</span></span>
    - <span data-ttu-id="558f8-765">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="558f8-765">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="558f8-766">Lägg till nya obligatoriska parametrar för att stödja piping för den nya Event Grid-domänen och Event Grid-domänämnet för att göra det möjligt att skapa nya händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="558f8-766">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="558f8-767">Lägg till nya obligatoriska parametrar för att ange det nya Event Grid-domännamnet och/eller namnet på Event Grid-domänämnet för att göra det möjligt att skapa nya händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="558f8-767">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="558f8-768">Lägg till ny parameteruppsättningar för domäner och domänämnen för att göra det möjligt att återanvända befintliga parametrar (t.ex. EndPointType, SubjectBeginsWith osv).</span><span class="sxs-lookup"><span data-stu-id="558f8-768">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="558f8-769">Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="558f8-769">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="558f8-770">Förfallodatum för händelseprenumeration</span><span class="sxs-lookup"><span data-stu-id="558f8-770">Event subscription expiration date,</span></span>
            - <span data-ttu-id="558f8-771">Avancerade filterparametrar.</span><span class="sxs-lookup"><span data-stu-id="558f8-771">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="558f8-772">Lägg till ny uppräkning för servicebusqueue som mål.</span><span class="sxs-lookup"><span data-stu-id="558f8-772">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="558f8-773">Tillåt inte användning av ”Alla” i alternativet -IncludedEventType och ersätt det med</span><span class="sxs-lookup"><span data-stu-id="558f8-773">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="558f8-774">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="558f8-774">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="558f8-775">Lägg till ny valfria parametrar (Top, ODataQuery och NextLink) för att stödja sidnumrering och filtrering av resultat.</span><span class="sxs-lookup"><span data-stu-id="558f8-775">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="558f8-776">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="558f8-776">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="558f8-777">Lägg till nya obligatoriska parametrar för att stödja piping för en Event Grid-domän och Event Grid-domänämnen för att göra det möjligt att ta bort befintliga händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="558f8-777">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="558f8-778">Lägg till nya obligatoriska parametrar för att ange Event Grid-domännamnet och/eller namnet på Event Grid-domänämnet för att göra det möjligt att ta bort befintliga händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="558f8-778">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="558f8-779">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="558f8-779">Az.FrontDoor</span></span>
* <span data-ttu-id="558f8-780">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="558f8-780">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="558f8-781">Lägg till stöd för transformeringar och nytt värde för automatisk komplettering för operatorer (RegEx)</span><span class="sxs-lookup"><span data-stu-id="558f8-781">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="558f8-782">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="558f8-782">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="558f8-783">Lägg till nya värden för automatisk komplettering</span><span class="sxs-lookup"><span data-stu-id="558f8-783">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="558f8-784">Az.Network</span><span class="sxs-lookup"><span data-stu-id="558f8-784">Az.Network</span></span>
* <span data-ttu-id="558f8-785">Lägg till stöd för resurs för virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="558f8-785">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="558f8-786">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="558f8-786">New cmdlets</span></span>
        - <span data-ttu-id="558f8-787">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="558f8-787">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="558f8-788">Lägg till AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="558f8-788">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="558f8-789">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="558f8-789">New cmdlets</span></span> 
        - <span data-ttu-id="558f8-790">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="558f8-790">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="558f8-791">Lägg till PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="558f8-791">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="558f8-792">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="558f8-792">New cmdlets</span></span> 
        - <span data-ttu-id="558f8-793">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="558f8-793">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="558f8-794">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="558f8-794">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="558f8-795">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="558f8-795">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="558f8-796">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="558f8-796">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="558f8-797">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="558f8-797">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="558f8-798">Lägg till PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="558f8-798">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="558f8-799">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="558f8-799">New cmdlets</span></span>
        - <span data-ttu-id="558f8-800">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="558f8-800">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="558f8-801">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="558f8-801">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="558f8-802">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="558f8-802">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="558f8-803">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="558f8-803">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="558f8-804">Nedanstående kommandon för funktionen har uppdaterats: Flaggan UseLocalAzureIpAddress på VpnConnection</span><span class="sxs-lookup"><span data-stu-id="558f8-804">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="558f8-805">New-AzVpnConnection har uppdaterats: Den valfria parametern -UseLocalAzureIpAddress har lagts till för att visa att en lokal IP-adress i Azure ska användas som källadress när anslutningen initieras.</span><span class="sxs-lookup"><span data-stu-id="558f8-805">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="558f8-806">Set-AzVpnConnection har uppdaterats: Den valfria parametern -UseLocalAzureIpAddress har lagts till för att visa att en lokal IP-adress i Azure ska användas som källadress när anslutningen initieras.</span><span class="sxs-lookup"><span data-stu-id="558f8-806">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="558f8-807">Det skrivskyddade fältet PeeredConnections har lagts till i ExpressRoute-peering.</span><span class="sxs-lookup"><span data-stu-id="558f8-807">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="558f8-808">Det skrivskyddade fältet GlobalReachEnabled har lagts till i ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="558f8-808">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="558f8-809">Ett attribut för icke-bakåtkompatibla ändringar har lagts till för att lyfta fram utfasning av fältet AllowGlobalReach i modellen ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="558f8-809">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="558f8-810">Problem 8756 har åtgärdats: Fel vid användning av TargetListenerID med AzApplicationGatewayRedirectConfiguration-cmdletar</span><span class="sxs-lookup"><span data-stu-id="558f8-810">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="558f8-811">En bugg i New-AzApplicationGatewayPathRuleConfig som gjorde att regeluppsättningen för att återskapa inte kunde anges har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="558f8-811">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="558f8-812">Visningen av VirtualNetworkTaps i NetworkInterfaceIpConfiguration har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="558f8-812">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="558f8-813">Cortex Get-cmdletar för att visa en lista med alla delar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="558f8-813">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="558f8-814">Funktionen för att skapa VirtualHub-referenser för ExpressRouteGateways och VpnGateway har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="558f8-814">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="558f8-815">Stöd för tillgänglighetszoner i AzureFirewall och NatGateway har lagts till</span><span class="sxs-lookup"><span data-stu-id="558f8-815">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="558f8-816">Cmdleten Get-AzNetworkServiceTag har lagts till</span><span class="sxs-lookup"><span data-stu-id="558f8-816">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="558f8-817">Lägg till stöd för flera offentliga IP-adresser för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="558f8-817">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="558f8-818">Cmdleten New-AzFirewall har uppdaterats:</span><span class="sxs-lookup"><span data-stu-id="558f8-818">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="558f8-819">Parametern -PublicIpAddress som accepterar ett eller flera offentliga IP-adressobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="558f8-819">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="558f8-820">Parametern -VirtualNetwork som accepterar ett virtuellt nätverksobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="558f8-820">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="558f8-821">Metoderna AddPublicIpAddress och RemovePublicIpAddress har lagts till på brandväggsobjekt – dessa accepterar ett offentligt IP-adressobjekt som indata</span><span class="sxs-lookup"><span data-stu-id="558f8-821">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="558f8-822">Inaktuella parametrar -PublicIpName och -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="558f8-822">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="558f8-823">Nedanstående kommandon för funktionen har uppdaterats: Ange autentiseringsalternativ för VpnClient AAD till resurser för virtuella nätverksgatewayer.</span><span class="sxs-lookup"><span data-stu-id="558f8-823">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="558f8-824">New-AzVirtualNetworkGateway har uppdaterats: De valfria parametrarna AadTenantUri, AadAudienceId och AadIssuerUri för att ange VpnClient AAD-autentiseringsalternativ på en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="558f8-824">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="558f8-825">Set-AzVirtualNetworkGateway har uppdaterats: De valfria parametrarna AadTenantUri, AadAudienceId och AadIssuerUri för att ange VpnClient AAD-autentiseringsalternativ på en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="558f8-825">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="558f8-826">Set-AzVirtualNetworkGateway har uppdaterats: Den valfria växelparametern RemoveAadAuthentication som tar bort VpnClient AAD-autentiseringsalternativ från en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="558f8-826">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="558f8-827">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="558f8-827">Az.OperationalInsights</span></span>
* <span data-ttu-id="558f8-828">Aktivera prisnivån **pergb2018** i kommandot ”New-AzureRmOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="558f8-828">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="558f8-829">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="558f8-829">Az.Resources</span></span>
* <span data-ttu-id="558f8-830">Stöd för ytterligare alternativ för att exportera en mall</span><span class="sxs-lookup"><span data-stu-id="558f8-830">Support for additional Template Export options</span></span>
    - <span data-ttu-id="558f8-831">Lägg till parametern ”-SkipResourceNameParameterization” till Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="558f8-831">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="558f8-832">Lägg till parametern ”-SkipAllParameterization” till Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="558f8-832">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="558f8-833">Lägg till parametern ”-Resource” till Export-AzResourceGroup för exporterad resursfiltrering</span><span class="sxs-lookup"><span data-stu-id="558f8-833">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="558f8-834">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="558f8-834">Az.ServiceFabric</span></span>
* <span data-ttu-id="558f8-835">Åtgärda att fel tumavtryck används vid tilläggning av certifikat i ByExistingKeyVault i vissa fall</span><span class="sxs-lookup"><span data-stu-id="558f8-835">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="558f8-836">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="558f8-836">Az.Sql</span></span>
* <span data-ttu-id="558f8-837">Åtgärda suffix för lagringsslutpunkt i Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="558f8-837">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="558f8-838">Åtgärda att aktivering av Advanced Data Security åsidosätter Advanced Threat Protection-princip</span><span class="sxs-lookup"><span data-stu-id="558f8-838">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="558f8-839">Nya cmdletar för Management.Sql som gör att kunderna kan lägga till nycklar för transparent datakryptering (TDE) och ange TDE-skydd för hanterade instanser</span><span class="sxs-lookup"><span data-stu-id="558f8-839">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="558f8-840">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="558f8-840">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="558f8-841">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="558f8-841">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="558f8-842">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="558f8-842">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="558f8-843">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="558f8-843">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="558f8-844">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="558f8-844">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="558f8-845">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="558f8-845">Az.Storage</span></span>
* <span data-ttu-id="558f8-846">Stöd för typerna FileStorage och SkuName Premium_ZRS när lagringskonton skapas</span><span class="sxs-lookup"><span data-stu-id="558f8-846">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="558f8-847">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="558f8-847">New-AzStorageAccount</span></span>
* <span data-ttu-id="558f8-848">Beskrivningen av cmdleten för bloboföränderlighet har förtydligats</span><span class="sxs-lookup"><span data-stu-id="558f8-848">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="558f8-849">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="558f8-849">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="558f8-850">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="558f8-850">Az.Websites</span></span>
* <span data-ttu-id="558f8-851">Optimerar Get-AzWebAppCertificate för att filtrera efter resursgrupp på servern i stället för klienten</span><span class="sxs-lookup"><span data-stu-id="558f8-851">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="558f8-852">Lägger till växlingsparametern -UseDisasterRecovery till Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="558f8-852">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="558f8-853">2.2.0 – juni 2019</span><span class="sxs-lookup"><span data-stu-id="558f8-853">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="558f8-854">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="558f8-854">Az.Cdn</span></span>
* <span data-ttu-id="558f8-855">Uppdaterade cmdletar för att ge stöd för rulesEngine-funktion baserat på API-version 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="558f8-855">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="558f8-856">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="558f8-856">Az.Compute</span></span>
* <span data-ttu-id="558f8-857">Lade till parameter `NoWait` som startar åtgärden och returnerar omedelbart, innan åtgärden har slutförts.</span><span class="sxs-lookup"><span data-stu-id="558f8-857">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="558f8-858">Uppdaterade cmdletar:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="558f8-858">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="558f8-859">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="558f8-859">Az.EventHub</span></span>
* <span data-ttu-id="558f8-860">Korrigering för #9231 – Get-AzEventHubNamespace returnerar inga taggar</span><span class="sxs-lookup"><span data-stu-id="558f8-860">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="558f8-861">Korrigering för #9230 – Get-AzEventHubNamespace returnerar ResourceGroup istället för ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="558f8-861">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="558f8-862">Az.Network</span><span class="sxs-lookup"><span data-stu-id="558f8-862">Az.Network</span></span>
* <span data-ttu-id="558f8-863">Uppdatera ResourceId och InputObject för NAT-gateway</span><span class="sxs-lookup"><span data-stu-id="558f8-863">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="558f8-864">Lägg till alias för ResourceId och InputObject</span><span class="sxs-lookup"><span data-stu-id="558f8-864">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="558f8-865">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="558f8-865">Az.PolicyInsights</span></span>
* <span data-ttu-id="558f8-866">Åtgärda Null-referensproblem i Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="558f8-866">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="558f8-867">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="558f8-867">Az.RecoveryServices</span></span>
* <span data-ttu-id="558f8-868">Minsta kvarhållning för IaaSVM-policy i dagar ändrat till 7 från 1</span><span class="sxs-lookup"><span data-stu-id="558f8-868">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="558f8-869">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="558f8-869">Az.ServiceBus</span></span>
* <span data-ttu-id="558f8-870">Korrigering för ärende #9182 – Get-AzServiceBusNamespace returnerar ResourceGroup istället för ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="558f8-870">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="558f8-871">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="558f8-871">Az.ServiceFabric</span></span>
* <span data-ttu-id="558f8-872">Åtgärda stavfel i felmeddelandet för Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="558f8-872">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="558f8-873">Åtgärda saknat tecken i Service Fabric-kommandorader</span><span class="sxs-lookup"><span data-stu-id="558f8-873">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="558f8-874">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="558f8-874">Az.Sql</span></span>
* <span data-ttu-id="558f8-875">Lägg till parametern DnsZonePartner för New-AzureSqlInstance-cmdlet för att ge stöd för AutoDr för hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="558f8-875">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="558f8-876">Avvecklar cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="558f8-876">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="558f8-877">Döp om cmdletar för hotidentifiering till Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="558f8-877">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="558f8-878">Parametrarna New-AzSqlInstance -StorageSizeInGB och -LicenseType är nu valfria.</span><span class="sxs-lookup"><span data-stu-id="558f8-878">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="558f8-879">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="558f8-879">Az.Websites</span></span>
* <span data-ttu-id="558f8-880">åtgärdar problemet där användningen av Set-AzWebApp och Set-AzWebAppSlot med -WebApp-egenskap tog bort taggarna</span><span class="sxs-lookup"><span data-stu-id="558f8-880">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="558f8-881">2.1.0 – maj 2019</span><span class="sxs-lookup"><span data-stu-id="558f8-881">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="558f8-882">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="558f8-882">Az.ApiManagement</span></span>
* <span data-ttu-id="558f8-883">Skapade nya cmdletar för att hantera diagnostik för global- och API-omfång</span><span class="sxs-lookup"><span data-stu-id="558f8-883">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="558f8-884">**Get-AzApiManagementDiagnostic** – Skaffa diagnostik konfigurerad för global- eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="558f8-884">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="558f8-885">**New-AzApiManagementDiagnostic** – Skapa ny diagnostik för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="558f8-885">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="558f8-886">**New-AzApiManagementHttpMessageDiagnostic** – Skapa diagnostikinställning om vilka rubriker som ska loggas och storleken på brödtextbyte</span><span class="sxs-lookup"><span data-stu-id="558f8-886">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="558f8-887">**New-AzApiManagementPipelineDiagnosticSetting** – Skapa diagnostikinställningar för inkommande/utgående HTTP-meddelanden till gatewayen.</span><span class="sxs-lookup"><span data-stu-id="558f8-887">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="558f8-888">**New-AzApiManagementSamplingSetting** – Skapa samplinginställningar för begäranden/svar för en diagnostik</span><span class="sxs-lookup"><span data-stu-id="558f8-888">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="558f8-889">**Remove-AzApiManagementDiagnostic** – Ta bort en diagnostikenhet för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="558f8-889">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="558f8-890">**Set-AzApiManagementDiagnostic** – Uppdatera en diagnostikenhet för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="558f8-890">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="558f8-891">Skapade nya cmdletar för hantering av cacheminne i ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="558f8-891">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="558f8-892">**Get-AzApiManagementCache** – Hämta information om cacheminnet som anges av identifierare eller alla cacheminnen</span><span class="sxs-lookup"><span data-stu-id="558f8-892">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="558f8-893">**New-AzApiManagementCache** – Skapa ett nytt default-cacheminne eller cacheminne i en viss Azure-region</span><span class="sxs-lookup"><span data-stu-id="558f8-893">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="558f8-894">**Remove-AzApiManagementCache** – Ta bort ett cacheminne</span><span class="sxs-lookup"><span data-stu-id="558f8-894">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="558f8-895">**Remove-AzApiManagementCache** – Ta bort ett cacheminne</span><span class="sxs-lookup"><span data-stu-id="558f8-895">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="558f8-896">Skapade nya cmdletar för hantering av API-schema</span><span class="sxs-lookup"><span data-stu-id="558f8-896">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="558f8-897">**New-AzApiManagementSchema** – Skapa ett nytt schema för ett API</span><span class="sxs-lookup"><span data-stu-id="558f8-897">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="558f8-898">**Get-AzApiManagementSchema** – Hämta de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="558f8-898">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="558f8-899">**Remove-AzApiManagementSchema** – Ta bort de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="558f8-899">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="558f8-900">**Set-AzApiManagementSchema** – Uppdatera de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="558f8-900">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="558f8-901">Skapa ny cmdlet för att generera en användartoken.</span><span class="sxs-lookup"><span data-stu-id="558f8-901">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="558f8-902">**New-AzApiManagementUserToken** – Skapa en ny användartoken som enligt standardinställning är giltig i 8 timmar. Token för GIT-användaren kan skapas med den här cmdleten./</span><span class="sxs-lookup"><span data-stu-id="558f8-902">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="558f8-903">Skapade en ny cmdlet för att hämta nätverksstatus</span><span class="sxs-lookup"><span data-stu-id="558f8-903">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="558f8-904">**Get-AzApiManagementNetworkStatus** – Hämta nätverksstatusanslutningen för resurserna som API Management-tjänsten är beroende av.</span><span class="sxs-lookup"><span data-stu-id="558f8-904">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="558f8-905">Det här är användbart när du distribuerar ApiManagement-tjänsten i ett virtuellt nätverk och validerar om något beroende är brutet.</span><span class="sxs-lookup"><span data-stu-id="558f8-905">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="558f8-906">Uppdaterade cmdlet **New-AzApiManagement** för att hantera ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="558f8-906">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="558f8-907">Lade till stöd för den nya SKU:n Consumption</span><span class="sxs-lookup"><span data-stu-id="558f8-907">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="558f8-908">Aktiverade stöd för att slå på flaggan EnableClientCertificate för SKU:n Consumption</span><span class="sxs-lookup"><span data-stu-id="558f8-908">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="558f8-909">Den nya cmdleten **New-AzApiManagementSslSetting** gör det möjligt att ställa in TLS/SSL-inställningen på ”Backend” och ”Frontend” (serverdel och klientdel).</span><span class="sxs-lookup"><span data-stu-id="558f8-909">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="558f8-910">Det här kan också användas till att konfigurera chiffer som 3DES och ServerProtocols som Http2 för Frontend för en ApiManagement-tjänst.</span><span class="sxs-lookup"><span data-stu-id="558f8-910">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="558f8-911">Stöd har lagts till för att konfigurera värdnamnet DeveloperPortal på ApiManagement-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="558f8-911">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="558f8-912">Uppdaterade cmdletar **Get-AzApiManagementSsoToken** för att ta PsApiManagement-objekt som indata</span><span class="sxs-lookup"><span data-stu-id="558f8-912">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="558f8-913">Uppdaterad cmdleten för att visa infogade felmeddelanden</span><span class="sxs-lookup"><span data-stu-id="558f8-913">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="558f8-914">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Felkod: Felmeddelande av typen ValidationError: Ett eller flera fält innehåller felaktiga värden: Felinformation:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="558f8-914">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="558f8-915">Uppdaterade cmdlet **Export-AzApiManagementApi** för att exportera API:er i OpenApi 3.0-format</span><span class="sxs-lookup"><span data-stu-id="558f8-915">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="558f8-916">Uppdaterade cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="558f8-916">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="558f8-917">Importera API från dokumentspecifikationen OpenApi 3.0</span><span class="sxs-lookup"><span data-stu-id="558f8-917">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="558f8-918">Om du vill åsidosätta egenskapen PsApiManagementSchema specificerad i ett dokument (Swagger, Wadl, Wsdl, OpenApi).</span><span class="sxs-lookup"><span data-stu-id="558f8-918">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="558f8-919">Åsidosätta egenskapen ServiceUrl som specificeras i ett dokument.</span><span class="sxs-lookup"><span data-stu-id="558f8-919">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="558f8-920">Uppdaterade cmdlet **Get-AzApiManagementPolicy** för att returnera policy i undantaget format av typen icke-XML med rawxml</span><span class="sxs-lookup"><span data-stu-id="558f8-920">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="558f8-921">Uppdaterade cmdlet **Set-AzApiManagementPolicy** för att godkänna policy i undantaget format av typen icke-XML med rawxml och XML undantaget med xml</span><span class="sxs-lookup"><span data-stu-id="558f8-921">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="558f8-922">Uppdaterad cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="558f8-922">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="558f8-923">Konfigurera API med OpenId auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="558f8-923">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="558f8-924">Skapa ett API i ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="558f8-924">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="558f8-925">Klona ett API med SourceApiId och SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="558f8-925">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="558f8-926">Möjlighet att konfigurera SubscriptionRequired i API-omfattningen.</span><span class="sxs-lookup"><span data-stu-id="558f8-926">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="558f8-927">Uppdaterad cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="558f8-927">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="558f8-928">Konfigurera API med OpenId auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="558f8-928">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="558f8-929">Uppdatera ett API till ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="558f8-929">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="558f8-930">Möjlighet att konfigurera SubscriptionRequired i API-omfattningen.</span><span class="sxs-lookup"><span data-stu-id="558f8-930">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="558f8-931">Uppdaterad cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="558f8-931">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="558f8-932">Klona en befintlig version med hjälp av SourceApiRevision (kopiera taggar, produkter, åtgärder och principer).</span><span class="sxs-lookup"><span data-stu-id="558f8-932">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="558f8-933">Den nya revisionen antar ApiId från den överordnade instansen.</span><span class="sxs-lookup"><span data-stu-id="558f8-933">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="558f8-934">Tillhandahålla ApiRevisionDescription</span><span class="sxs-lookup"><span data-stu-id="558f8-934">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="558f8-935">Åsidosätta ServiceUrl vid kloning av ett API.</span><span class="sxs-lookup"><span data-stu-id="558f8-935">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="558f8-936">Uppdaterad cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="558f8-936">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="558f8-937">Konfigurera AAD eller AADB2C med en Authority</span><span class="sxs-lookup"><span data-stu-id="558f8-937">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="558f8-938">Konfigurera SignupPolicy, SigninPolicy, ProfileEditingPolicy och PasswordResetPolicy</span><span class="sxs-lookup"><span data-stu-id="558f8-938">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="558f8-939">Uppdaterad cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="558f8-939">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="558f8-940">Kompensera för ny SubscriptonModel med Scope och UserId</span><span class="sxs-lookup"><span data-stu-id="558f8-940">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="558f8-941">Kompensera för gammal prenumerationsmodell med ProductId och UserId</span><span class="sxs-lookup"><span data-stu-id="558f8-941">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="558f8-942">Lägg till funktion för att aktivera AllowTracing på prenumerationsnivå.</span><span class="sxs-lookup"><span data-stu-id="558f8-942">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="558f8-943">Uppdaterad cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="558f8-943">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="558f8-944">Kompensera för ny SubscriptonModel med Scope och UserId</span><span class="sxs-lookup"><span data-stu-id="558f8-944">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="558f8-945">Kompensera för gammal prenumerationsmodell med ProductId och UserId</span><span class="sxs-lookup"><span data-stu-id="558f8-945">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="558f8-946">Lägg till funktion för att aktivera AllowTracing på prenumerationsnivå.</span><span class="sxs-lookup"><span data-stu-id="558f8-946">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="558f8-947">Uppdaterade följande cmdletar för att acceptera ResourceId som indata</span><span class="sxs-lookup"><span data-stu-id="558f8-947">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="558f8-948">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="558f8-948">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="558f8-949">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="558f8-949">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="558f8-950">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="558f8-950">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="558f8-951">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="558f8-951">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="558f8-952">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="558f8-952">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="558f8-953">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="558f8-953">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="558f8-954">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="558f8-954">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="558f8-955">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="558f8-955">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="558f8-956">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="558f8-956">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="558f8-957">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="558f8-957">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="558f8-958">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="558f8-958">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="558f8-959">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="558f8-959">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="558f8-960">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="558f8-960">Az.Automation</span></span>
* <span data-ttu-id="558f8-961">Uppdaterade Get-AzAutomationJobOutputRecord för att hantera postvärden av typen JSON och Text.</span><span class="sxs-lookup"><span data-stu-id="558f8-961">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="558f8-962">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="558f8-962">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="558f8-963">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="558f8-963">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="558f8-964">Ändrade beteende för Start-AzAutomationDscCompilationJob till att bara starta jobbet istället för att vänta på slutförandet.</span><span class="sxs-lookup"><span data-stu-id="558f8-964">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="558f8-965">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="558f8-965">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="558f8-966">Korrigering för Get-AzAutomationDscNode när using -Name returnerar alla noder.</span><span class="sxs-lookup"><span data-stu-id="558f8-966">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="558f8-967">Nu returnerar den endast den matchande noden.</span><span class="sxs-lookup"><span data-stu-id="558f8-967">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="558f8-968">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="558f8-968">Az.Compute</span></span>
* <span data-ttu-id="558f8-969">Lägg till parametrarna ProtectFromScaleIn och ProtectFromScaleSetAction i cmdleten Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="558f8-969">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="558f8-970">Nu är standardinställningen att vimpelparametern New-AzVM använder en tillgänglig plats om USA, östra inte stöds</span><span class="sxs-lookup"><span data-stu-id="558f8-970">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="558f8-971">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="558f8-971">Az.DataLakeStore</span></span>
* <span data-ttu-id="558f8-972">Uppdatera ADLS-sdk för att använda httpclient, integrera dataplanstestning med Azure-ramverk</span><span class="sxs-lookup"><span data-stu-id="558f8-972">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="558f8-973">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="558f8-973">Az.Monitor</span></span>
* <span data-ttu-id="558f8-974">Korrigera felaktiga parameternamn i hjälpexempel</span><span class="sxs-lookup"><span data-stu-id="558f8-974">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="558f8-975">Az.Network</span><span class="sxs-lookup"><span data-stu-id="558f8-975">Az.Network</span></span>
* <span data-ttu-id="558f8-976">Lägg till flaggan DisableBgpRoutePropagation i utdata för effektiv routningstabell</span><span class="sxs-lookup"><span data-stu-id="558f8-976">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="558f8-977">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="558f8-977">Updated cmdlet:</span></span>
        - <span data-ttu-id="558f8-978">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="558f8-978">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="558f8-979">Åtgärda dubbelstreck i dokumentationen New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="558f8-979">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="558f8-980">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="558f8-980">Az.Resources</span></span>
* <span data-ttu-id="558f8-981">Lägg till ny cmdlet Get-AzureRmDenyAssignment för att hämta tilldelningsnekanden</span><span class="sxs-lookup"><span data-stu-id="558f8-981">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="558f8-982">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="558f8-982">Az.Sql</span></span>
* <span data-ttu-id="558f8-983">Döp om Advanced Threat Protection-cmdletar för Advanced Data Security och aktivera Vulnerability Assessment som standard</span><span class="sxs-lookup"><span data-stu-id="558f8-983">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="558f8-984">2.0.0 – maj 2019</span><span class="sxs-lookup"><span data-stu-id="558f8-984">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="558f8-985">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="558f8-985">Az.Accounts</span></span>
* <span data-ttu-id="558f8-986">Uppdatera autentiseringsbiblioteket för att åtgärda ADFS-problem med autentisering av användarnamn/lösenord</span><span class="sxs-lookup"><span data-stu-id="558f8-986">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="558f8-987">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="558f8-987">Az.CognitiveServices</span></span>
* <span data-ttu-id="558f8-988">Visa endast Bing-ansvarsfriskrivning för Bing-sökningstjänster.</span><span class="sxs-lookup"><span data-stu-id="558f8-988">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="558f8-989">Förbättra felmeddelande när det inte går att skapa konton.</span><span class="sxs-lookup"><span data-stu-id="558f8-989">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="558f8-990">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="558f8-990">Az.Compute</span></span>
* <span data-ttu-id="558f8-991">Funktion för närhetsplaceringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="558f8-991">Proximity placement group feature.</span></span>
    - <span data-ttu-id="558f8-992">Följande nya cmdletar har lagts till:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="558f8-992">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="558f8-993">Den nya parametern ProximityPlacementGroupId har lagts till i följande cmdletar:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="558f8-993">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="558f8-994">Parametern StorageAccountType har lagts till i New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="558f8-994">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="558f8-995">TargetRegion för New-AzGalleryImageVersion kan innehålla StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="558f8-995">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="558f8-996">Växlingsparametern SkipShutdown har lagts till i Stop-AzVM och Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="558f8-996">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="558f8-997">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="558f8-997">Breaking changes</span></span>
    - <span data-ttu-id="558f8-998">Set-AzVMBootDiagnostics har ändrats till Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="558f8-998">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="558f8-999">Export-AzLogAnalyticThrottledRequests har ändrats till Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="558f8-999">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="558f8-1000">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="558f8-1000">Az.DeploymentManager</span></span>
* <span data-ttu-id="558f8-1001">De första allmänt tillgängliga versionerna av cmdletar för Distributionshanteraren i Azure</span><span class="sxs-lookup"><span data-stu-id="558f8-1001">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="558f8-1002">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="558f8-1002">Az.Dns</span></span>
* <span data-ttu-id="558f8-1003">Automatisk delegering av DNS för NameServer</span><span class="sxs-lookup"><span data-stu-id="558f8-1003">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="558f8-1004">Det överordnade zonnamnet kan användas som ytterligare valfri parameter i cmdleten för att skapa DNS-zoner.</span><span class="sxs-lookup"><span data-stu-id="558f8-1004">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="558f8-1005">Lägger till NS-poster för en nyligen skapad underordnad zon i den överordnade zonen.</span><span class="sxs-lookup"><span data-stu-id="558f8-1005">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="558f8-1006">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="558f8-1006">Az.FrontDoor</span></span>
* <span data-ttu-id="558f8-1007">De första allmänt tillgängliga versionerna av cmdletar för Azure FrontDoor</span><span class="sxs-lookup"><span data-stu-id="558f8-1007">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="558f8-1008">Byt namn på WAF-cmdletar så att de omfattar ”Waf”</span><span class="sxs-lookup"><span data-stu-id="558f8-1008">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="558f8-1009">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="558f8-1009">Az.HDInsight</span></span>
* <span data-ttu-id="558f8-1010">Två cmdletar har tagits bort:</span><span class="sxs-lookup"><span data-stu-id="558f8-1010">Removed two cmdlets:</span></span>
    - <span data-ttu-id="558f8-1011">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="558f8-1011">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="558f8-1012">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="558f8-1012">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="558f8-1013">En ny cmdlet har lagts till, Set-AzHDInsightGatewayCredential, som ersätter Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="558f8-1013">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="558f8-1014">Uppdatera cmdleten Get-AzHDInsightJobOutput för att skilja mellan läsarrollen och HDInsight-operatörsrollen:</span><span class="sxs-lookup"><span data-stu-id="558f8-1014">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="558f8-1015">Användare med läsarrollen måste uttryckligen ange parametern ”DefaultStorageAccountKey”, annars uppstår fel.</span><span class="sxs-lookup"><span data-stu-id="558f8-1015">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="558f8-1016">Användare med HDInsight-operatörsrollen påverkas inte.</span><span class="sxs-lookup"><span data-stu-id="558f8-1016">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="558f8-1017">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="558f8-1017">Az.Monitor</span></span>
* <span data-ttu-id="558f8-1018">Nya cmdletar för SQR API (schemalagd frågeregel)</span><span class="sxs-lookup"><span data-stu-id="558f8-1018">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="558f8-1019">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="558f8-1019">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="558f8-1020">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="558f8-1020">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="558f8-1021">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="558f8-1021">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="558f8-1022">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="558f8-1022">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="558f8-1023">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="558f8-1023">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="558f8-1024">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="558f8-1024">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="558f8-1025">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="558f8-1025">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="558f8-1026">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="558f8-1026">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="558f8-1027">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="558f8-1027">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="558f8-1028">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="558f8-1028">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="558f8-1029">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="558f8-1029">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="558f8-1030">[Mer](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information om SQR API</span><span class="sxs-lookup"><span data-stu-id="558f8-1030">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="558f8-1031">Az.Monitor.md har uppdaterats för att omfatta cmdletar för måttbaserade aviseringsregler i GenV2 (inte klassiska)</span><span class="sxs-lookup"><span data-stu-id="558f8-1031">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="558f8-1032">Az.Network</span><span class="sxs-lookup"><span data-stu-id="558f8-1032">Az.Network</span></span>
* <span data-ttu-id="558f8-1033">Lägg till stöd för NAT Gateway-resurs</span><span class="sxs-lookup"><span data-stu-id="558f8-1033">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="558f8-1034">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="558f8-1034">New cmdlets</span></span>
        - <span data-ttu-id="558f8-1035">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="558f8-1035">New-AzNatGateway</span></span>
        - <span data-ttu-id="558f8-1036">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="558f8-1036">Get-AzNatGateway</span></span>
        - <span data-ttu-id="558f8-1037">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="558f8-1037">Set-AzNatGateway</span></span>
        - <span data-ttu-id="558f8-1038">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="558f8-1038">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="558f8-1039">Uppdaterade cmdletar</span><span class="sxs-lookup"><span data-stu-id="558f8-1039">Updated cmdlets</span></span>
        - <span data-ttu-id="558f8-1040">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="558f8-1040">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="558f8-1041">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="558f8-1041">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="558f8-1042">Nedanstående kommandon för funktionen har uppdaterats: Ange/ta bort anpassade vägar på Brooklyn Gateway.</span><span class="sxs-lookup"><span data-stu-id="558f8-1042">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="558f8-1043">New-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ställa in adressprefix som anpassade vägar för att ange gateway.</span><span class="sxs-lookup"><span data-stu-id="558f8-1043">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="558f8-1044">Set-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ange adressprefix som anpassade vägar för att ange gateway.</span><span class="sxs-lookup"><span data-stu-id="558f8-1044">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="558f8-1045">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="558f8-1045">Az.PolicyInsights</span></span>
* <span data-ttu-id="558f8-1046">Stöd för att fråga efter information om principutvärdering.</span><span class="sxs-lookup"><span data-stu-id="558f8-1046">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="558f8-1047">Lägg till parametern ”-Expand” för Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="558f8-1047">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="558f8-1048">Stöd för -Expand PolicyEvaluationDetails.</span><span class="sxs-lookup"><span data-stu-id="558f8-1048">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="558f8-1049">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="558f8-1049">Az.RecoveryServices</span></span>
* <span data-ttu-id="558f8-1050">Stöd för att dela prenumeration mellan Azure och Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="558f8-1050">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="558f8-1051">Markering av kommande icke-bakåtkompatibla ändringar för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="558f8-1051">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="558f8-1052">Korrigering för återställningsplan och åtgärdsplan i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="558f8-1052">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="558f8-1053">Korrigering för mappning av uppdateringsnätverk i Azure Site Recovery för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="558f8-1053">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="558f8-1054">Korrigering för instruktioner för uppdateringsskydd i Azure Site Recovery för Azure till Azure för hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="558f8-1054">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="558f8-1055">Andra mindre korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="558f8-1055">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="558f8-1056">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="558f8-1056">Az.Relay</span></span>
* <span data-ttu-id="558f8-1057">Korrigera stavfel i kundriktade meddelanden</span><span class="sxs-lookup"><span data-stu-id="558f8-1057">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="558f8-1058">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="558f8-1058">Az.ServiceBus</span></span>
* <span data-ttu-id="558f8-1059">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="558f8-1059">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="558f8-1060">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="558f8-1060">Az.Storage</span></span>
* <span data-ttu-id="558f8-1061">Uppgradera till lagringsklientbiblioteket 10.0.1 (namnområdet för alla objekt från detta SDK ändras från ”Microsoft.WindowsAzure.Storage. *till ”Microsoft.Azure.Storage.* ”)</span><span class="sxs-lookup"><span data-stu-id="558f8-1061">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="558f8-1062">Uppgradera till Microsoft.Azure.Management.Storage 11.0.0 för att stödja den nya API-versionen 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="558f8-1062">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="558f8-1063">Standardlagringskontot i Skapa lagringskonto ändras från ”Storage” till ”StorageV2”</span><span class="sxs-lookup"><span data-stu-id="558f8-1063">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="558f8-1064">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="558f8-1064">New-AzStorageAccount</span></span>
* <span data-ttu-id="558f8-1065">Ändra lagringskontots cmdlet-utdata Sku.Name för att passa med indata-SkuName genom att lägga till ”-”. Till exempel ändras ”StandardLRS” till ”Standard_LRS”</span><span class="sxs-lookup"><span data-stu-id="558f8-1065">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="558f8-1066">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="558f8-1066">New-AzStorageAccount</span></span>
    - <span data-ttu-id="558f8-1067">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="558f8-1067">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="558f8-1068">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="558f8-1068">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="558f8-1069">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="558f8-1069">Az.Websites</span></span>
* <span data-ttu-id="558f8-1070">Egenskapen ”typ” konfigureras nu för PSSite-objekt som returneras av Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="558f8-1070">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="558f8-1071">Get-AzWebApp\*Metrics och Get-AzAppServicePlanMetrics markeras som inaktuella</span><span class="sxs-lookup"><span data-stu-id="558f8-1071">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="558f8-1072">1.8.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="558f8-1072">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="558f8-1073">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="558f8-1073">Highlights since the last major release</span></span>
* <span data-ttu-id="558f8-1074">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="558f8-1074">General availability of `Az` module</span></span>
* <span data-ttu-id="558f8-1075">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="558f8-1075">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="558f8-1076">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="558f8-1076">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="558f8-1077">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="558f8-1077">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="558f8-1078">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="558f8-1078">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="558f8-1079">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="558f8-1079">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="558f8-1080">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="558f8-1080">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="558f8-1081">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="558f8-1081">Az.Accounts</span></span>
* <span data-ttu-id="558f8-1082">Uppdatera Uninstall-AzureRm för att ta bort moduler i Mac på ett korrekt sätt</span><span class="sxs-lookup"><span data-stu-id="558f8-1082">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="558f8-1083">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="558f8-1083">Az.Batch</span></span>
* <span data-ttu-id="558f8-1084">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="558f8-1084">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="558f8-1085">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="558f8-1085">Az.Cdn</span></span>
* <span data-ttu-id="558f8-1086">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="558f8-1086">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="558f8-1087">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="558f8-1087">Az.CognitiveServices</span></span>
* <span data-ttu-id="558f8-1088">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="558f8-1088">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="558f8-1089">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="558f8-1089">Az.Compute</span></span>
* <span data-ttu-id="558f8-1090">Åtgärda problem med AEM-installationen om resurs-ID:n för diskar innehåller resourcegroups i gemener i resurs-ID:n</span><span class="sxs-lookup"><span data-stu-id="558f8-1090">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="558f8-1091">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="558f8-1091">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="558f8-1092">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="558f8-1092">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="558f8-1093">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="558f8-1093">Az.DataFactory</span></span>
* <span data-ttu-id="558f8-1094">Lägg till SsisProperties om NodeCount inte är null för hanterad integreringskörning.</span><span class="sxs-lookup"><span data-stu-id="558f8-1094">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="558f8-1095">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="558f8-1095">Az.DataLakeStore</span></span>
* <span data-ttu-id="558f8-1096">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="558f8-1096">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="558f8-1097">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="558f8-1097">Az.EventGrid</span></span>
* <span data-ttu-id="558f8-1098">Hjälptexten för slutpunkten har uppdaterats för att visa att resurser ska skapas innan cmdletarna för att skapa/uppdatera händelseprenumerationer används.</span><span class="sxs-lookup"><span data-stu-id="558f8-1098">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="558f8-1099">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="558f8-1099">Az.EventHub</span></span>
* <span data-ttu-id="558f8-1100">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="558f8-1100">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="558f8-1101">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="558f8-1101">Az.HDInsight</span></span>
* <span data-ttu-id="558f8-1102">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="558f8-1102">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="558f8-1103">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="558f8-1103">Az.IotHub</span></span>
* <span data-ttu-id="558f8-1104">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="558f8-1104">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="558f8-1105">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="558f8-1105">Az.KeyVault</span></span>
* <span data-ttu-id="558f8-1106">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="558f8-1106">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="558f8-1107">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="558f8-1107">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="558f8-1108">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="558f8-1108">Az.MachineLearning</span></span>
* <span data-ttu-id="558f8-1109">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="558f8-1109">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="558f8-1110">Az.Media</span><span class="sxs-lookup"><span data-stu-id="558f8-1110">Az.Media</span></span>
* <span data-ttu-id="558f8-1111">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="558f8-1111">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="558f8-1112">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="558f8-1112">Az.Monitor</span></span>
  * <span data-ttu-id="558f8-1113">Nya cmdletar för måttbaserad aviseringsregel i GenV2 (inte klassisk)</span><span class="sxs-lookup"><span data-stu-id="558f8-1113">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="558f8-1114">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="558f8-1114">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="558f8-1115">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="558f8-1115">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="558f8-1116">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="558f8-1116">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="558f8-1117">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="558f8-1117">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="558f8-1118">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="558f8-1118">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="558f8-1119">Monitor SDK har uppdaterats till version 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="558f8-1119">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="558f8-1120">Az.Network</span><span class="sxs-lookup"><span data-stu-id="558f8-1120">Az.Network</span></span>
* <span data-ttu-id="558f8-1121">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="558f8-1121">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="558f8-1122">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="558f8-1122">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="558f8-1123">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="558f8-1123">Az.NotificationHubs</span></span>
* <span data-ttu-id="558f8-1124">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="558f8-1124">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="558f8-1125">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="558f8-1125">Az.OperationalInsights</span></span>
* <span data-ttu-id="558f8-1126">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="558f8-1126">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="558f8-1127">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="558f8-1127">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="558f8-1128">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="558f8-1128">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="558f8-1129">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="558f8-1129">Az.RecoveryServices</span></span>
* <span data-ttu-id="558f8-1130">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="558f8-1130">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="558f8-1131">Tabellformatet för SQL i virtuella Azure-datorer har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="558f8-1131">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="558f8-1132">En alternativ metod för att hämta platser i AzureFileShare har lagts till</span><span class="sxs-lookup"><span data-stu-id="558f8-1132">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="558f8-1133">ScheduleRunDays i SchedulePolicy-objekt har uppdaterats enligt tidszon</span><span class="sxs-lookup"><span data-stu-id="558f8-1133">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="558f8-1134">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="558f8-1134">Az.RedisCache</span></span>
* <span data-ttu-id="558f8-1135">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="558f8-1135">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="558f8-1136">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="558f8-1136">Az.Resources</span></span>
* <span data-ttu-id="558f8-1137">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="558f8-1137">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="558f8-1138">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="558f8-1138">Az.Sql</span></span>
* <span data-ttu-id="558f8-1139">Ersätt Monitor SDK-beroende med vanlig kod</span><span class="sxs-lookup"><span data-stu-id="558f8-1139">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="558f8-1140">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="558f8-1140">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="558f8-1141">Förbättrad process för klassificering av flera kolumner.</span><span class="sxs-lookup"><span data-stu-id="558f8-1141">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="558f8-1142">Inkludera SKU-egenskaper (SKU-namn, serie, kapacitet) i svaret från Get-AzSqlServerServiceObjective och formatera som tabell som standard.</span><span class="sxs-lookup"><span data-stu-id="558f8-1142">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="558f8-1143">Möjlighet att använda Get-AzSqlServerServiceObjective efter plats utan att behöva en redan befintlig server i regionen.</span><span class="sxs-lookup"><span data-stu-id="558f8-1143">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="558f8-1144">Stöd för tidszonsparametern när hanterade instanser skapas.</span><span class="sxs-lookup"><span data-stu-id="558f8-1144">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="558f8-1145">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="558f8-1145">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="558f8-1146">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="558f8-1146">Az.Websites</span></span>
* <span data-ttu-id="558f8-1147">åtgärdar Set-AzWebApp och Set-AzWebAppSlot så att de inte tar bort taggar vid körning</span><span class="sxs-lookup"><span data-stu-id="558f8-1147">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="558f8-1148">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="558f8-1148">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="558f8-1149">SDK för WebSites har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="558f8-1149">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="558f8-1150">Egenskapen AdminSiteName har tagits bort från PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="558f8-1150">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="558f8-1151">1.7.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="558f8-1151">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="558f8-1152">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="558f8-1152">Highlights since the last major release</span></span>
* <span data-ttu-id="558f8-1153">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="558f8-1153">General availability of `Az` module</span></span>
* <span data-ttu-id="558f8-1154">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="558f8-1154">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="558f8-1155">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="558f8-1155">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="558f8-1156">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="558f8-1156">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="558f8-1157">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="558f8-1157">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="558f8-1158">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="558f8-1158">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="558f8-1159">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="558f8-1159">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="558f8-1160">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="558f8-1160">Az.Accounts</span></span>
* <span data-ttu-id="558f8-1161">Add-AzEnvironment och Set-AzEnvironment har uppdaterats för att godkänna parametern AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="558f8-1161">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="558f8-1162">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="558f8-1162">Az.AnalysisServices</span></span>
* <span data-ttu-id="558f8-1163">ServiceClient används i cmdletar för dataplan och den ursprungliga autentiseringslogiken har tagits bort</span><span class="sxs-lookup"><span data-stu-id="558f8-1163">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="558f8-1164">Add-AzureASAccount används för omslutning av Connect-AzAccount för att undvika en icke-bakåtkompatibel ändring</span><span class="sxs-lookup"><span data-stu-id="558f8-1164">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="558f8-1165">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="558f8-1165">Az.Automation</span></span>
* <span data-ttu-id="558f8-1166">Buggen för cmdleten New-AzAutomationSoftwareUpdateConfiguration för inkluderingar har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="558f8-1166">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="558f8-1167">Nu bör parametern IncludedKbNumber och IncludedPackageNameMask fungera.</span><span class="sxs-lookup"><span data-stu-id="558f8-1167">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="558f8-1168">Felkorrigering för dynamiska grupper i uppdateringshanteringen för azure automation</span><span class="sxs-lookup"><span data-stu-id="558f8-1168">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="558f8-1169">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="558f8-1169">Az.Compute</span></span>
* <span data-ttu-id="558f8-1170">Lägg till parametern HyperVGeneration i New-AzDiskConfig och New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="558f8-1170">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="558f8-1171">Tillåt att virtuella datorer skapas med galleribilder från andra klientorganisationer.</span><span class="sxs-lookup"><span data-stu-id="558f8-1171">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="558f8-1172">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="558f8-1172">Az.ContainerInstance</span></span>
* <span data-ttu-id="558f8-1173">Ett problem har åtgärdats i parametern -Command för New-AzContainerGroup som lade till ett avslutande tomt argument</span><span class="sxs-lookup"><span data-stu-id="558f8-1173">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="558f8-1174">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="558f8-1174">Az.DataFactory</span></span>
* <span data-ttu-id="558f8-1175">ADF .Net SDK-versionen har uppdaterats till 3.0.2</span><span class="sxs-lookup"><span data-stu-id="558f8-1175">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="558f8-1176">Cmdleten Set-AzDataFactoryV2 har uppdaterats med extra parametrar för inställningar som rör RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="558f8-1176">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="558f8-1177">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="558f8-1177">Az.Resources</span></span>
* <span data-ttu-id="558f8-1178">Förbättra hanteringen av providrar för Get-AzResource när parametrarna -ResourceId eller -ResourceGroupName, -Name och -ResourceType tillhandahålls</span><span class="sxs-lookup"><span data-stu-id="558f8-1178">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="558f8-1179">Förbättra felhanteringen för ”Test-AzDeployment” och ”Test-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="558f8-1179">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="558f8-1180">Hantera fel utanför distributionsvalideringen och ta med dem i kommandoutdata istället</span><span class="sxs-lookup"><span data-stu-id="558f8-1180">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="558f8-1181">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="558f8-1181">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="558f8-1182">Lägg till växlingsparametern -IgnoreDynamicParameters till en uppsättning av cmdletar för distribution för att hoppa över fråga i skript och jobbscenarier</span><span class="sxs-lookup"><span data-stu-id="558f8-1182">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="558f8-1183">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="558f8-1183">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="558f8-1184">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="558f8-1184">Az.Sql</span></span>
* <span data-ttu-id="558f8-1185">Stöd för dataklassificering av databaser.</span><span class="sxs-lookup"><span data-stu-id="558f8-1185">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="558f8-1186">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="558f8-1186">Az.Storage</span></span>
* <span data-ttu-id="558f8-1187">Rapportera detaljfel när lagringskontext skapas med parametern -UseConnectedAccount, men utan inloggning på Azure-kontot</span><span class="sxs-lookup"><span data-stu-id="558f8-1187">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="558f8-1188">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="558f8-1188">New-AzStorageContext</span></span>
* <span data-ttu-id="558f8-1189">Stöd för att hantera Blob Service-egenskaper för ett angivet lagringskonto med API:et för hanteringsplan</span><span class="sxs-lookup"><span data-stu-id="558f8-1189">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="558f8-1190">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="558f8-1190">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="558f8-1191">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="558f8-1191">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="558f8-1192">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="558f8-1192">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="558f8-1193">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="558f8-1193">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="558f8-1194">Stöd för -AsJob-cmdletar för att ladda upp och ladda ned blobar och filer</span><span class="sxs-lookup"><span data-stu-id="558f8-1194">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="558f8-1195">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="558f8-1195">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="558f8-1196">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="558f8-1196">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="558f8-1197">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="558f8-1197">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="558f8-1198">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="558f8-1198">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="558f8-1199">1.6.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="558f8-1199">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="558f8-1200">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="558f8-1200">Highlights since the last major release</span></span>
* <span data-ttu-id="558f8-1201">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="558f8-1201">General availability of `Az` module</span></span>
* <span data-ttu-id="558f8-1202">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="558f8-1202">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="558f8-1203">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="558f8-1203">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="558f8-1204">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="558f8-1204">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="558f8-1205">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="558f8-1205">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="558f8-1206">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="558f8-1206">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="558f8-1207">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="558f8-1207">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="558f8-1208">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="558f8-1208">Az.Automation</span></span>
* <span data-ttu-id="558f8-1209">Azure Automation – ändring av uppdateringshantering för stöd för de nya funktionerna:</span><span class="sxs-lookup"><span data-stu-id="558f8-1209">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="558f8-1210">Dynamisk gruppering</span><span class="sxs-lookup"><span data-stu-id="558f8-1210">Dynamic grouping</span></span>
    * <span data-ttu-id="558f8-1211">För-/efterskrift</span><span class="sxs-lookup"><span data-stu-id="558f8-1211">Pre-Post script</span></span>
    * <span data-ttu-id="558f8-1212">Inställning för omstart</span><span class="sxs-lookup"><span data-stu-id="558f8-1212">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="558f8-1213">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="558f8-1213">Az.Compute</span></span>
* <span data-ttu-id="558f8-1214">Åtgärda problem med sökvägsmatchning i Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="558f8-1214">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="558f8-1215">Uppdatera Compute-klientbibliotek till 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="558f8-1215">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="558f8-1216">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="558f8-1216">Az.KeyVault</span></span>
* <span data-ttu-id="558f8-1217">Stöd för jokertecken för KeyVault-cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="558f8-1217">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="558f8-1218">Az.Network</span><span class="sxs-lookup"><span data-stu-id="558f8-1218">Az.Network</span></span>
* <span data-ttu-id="558f8-1219">Lägg till stöd för Threat Intelligence för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="558f8-1219">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="558f8-1220">Lägg till resurs för brandväggsprincip på översta nivå och anpassade regler för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="558f8-1220">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="558f8-1221">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="558f8-1221">Az.RecoveryServices</span></span>
* <span data-ttu-id="558f8-1222">SnapshotRetentionInDays har lagts till i Azure-principen för virtuella datorer för stöd av Instant RP</span><span class="sxs-lookup"><span data-stu-id="558f8-1222">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="558f8-1223">Pipe-stöd för avregistrering av container har lagts till</span><span class="sxs-lookup"><span data-stu-id="558f8-1223">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="558f8-1224">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="558f8-1224">Az.Resources</span></span>
* <span data-ttu-id="558f8-1225">Uppdatera stöd för jokertecken för Get-AzResource och Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="558f8-1225">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="558f8-1226">Uppdatera autentiseringsuppgifter som används vid allmänna anrop till ARM</span><span class="sxs-lookup"><span data-stu-id="558f8-1226">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="558f8-1227">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="558f8-1227">Az.Sql</span></span>
* <span data-ttu-id="558f8-1228">Cmdlet-parametern (ExcludeDetectionType) för Hotidentifiering ändrades från DetectionType till sträng[] för att framtidssäkra den när nya DetectionTypes läggs till, och även för att stödja automatisk ifyllning.</span><span class="sxs-lookup"><span data-stu-id="558f8-1228">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="558f8-1229">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="558f8-1229">Az.Storage</span></span>
* <span data-ttu-id="558f8-1230">Stöd för att hämta/ange/ta bort hanteringsprincip på ett lagringskonto</span><span class="sxs-lookup"><span data-stu-id="558f8-1230">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="558f8-1231">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="558f8-1231">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="558f8-1232">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="558f8-1232">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="558f8-1233">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="558f8-1233">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="558f8-1234">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="558f8-1234">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="558f8-1235">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="558f8-1235">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="558f8-1236">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="558f8-1236">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="558f8-1237">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="558f8-1237">Az.Websites</span></span>
* <span data-ttu-id="558f8-1238">Åtgärda fel med ARM-mall som avbryter kloning av alla platser med 'New-AzWebApp -IncludeSourceWebAppSlots'</span><span class="sxs-lookup"><span data-stu-id="558f8-1238">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="558f8-1239">1.5.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="558f8-1239">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="558f8-1240">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="558f8-1240">Az.Accounts</span></span>
* <span data-ttu-id="558f8-1241">Lägg till kommandot Register-AzModule för stöd för AutoRest-genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="558f8-1241">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="558f8-1242">Uppdatera exempel för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="558f8-1242">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="558f8-1243">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="558f8-1243">Az.Automation</span></span>
* <span data-ttu-id="558f8-1244">Problem med att hämta vissa månadsscheman i flera Azure Automation-cmdletar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="558f8-1244">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="558f8-1245">Åtgärda problem med att Get-AzAutomationDscNode bara returnerar de 20 översta noderna.</span><span class="sxs-lookup"><span data-stu-id="558f8-1245">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="558f8-1246">Nu returneras alla noder</span><span class="sxs-lookup"><span data-stu-id="558f8-1246">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="558f8-1247">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="558f8-1247">Az.Cdn</span></span>
* <span data-ttu-id="558f8-1248">Nya Powershell-cmdletar för att aktivera/inaktivera anpassade domän-HTTPS har lagts till och de gamla har gjorts inaktuella</span><span class="sxs-lookup"><span data-stu-id="558f8-1248">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="558f8-1249">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="558f8-1249">Az.Compute</span></span>
* <span data-ttu-id="558f8-1250">Lägg till stöd för jokertecken för Get-cmdletar</span><span class="sxs-lookup"><span data-stu-id="558f8-1250">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="558f8-1251">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="558f8-1251">Az.DataFactory</span></span>
* <span data-ttu-id="558f8-1252">ADF .Net SDK-versionen har uppdaterats till 3.0.1</span><span class="sxs-lookup"><span data-stu-id="558f8-1252">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="558f8-1253">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="558f8-1253">Az.LogicApp</span></span>
* <span data-ttu-id="558f8-1254">Åtgärda problemet med att ListWorkflows endast hämtar den första sidan med resultat</span><span class="sxs-lookup"><span data-stu-id="558f8-1254">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="558f8-1255">Az.Network</span><span class="sxs-lookup"><span data-stu-id="558f8-1255">Az.Network</span></span>
* <span data-ttu-id="558f8-1256">Lägg till stöd för jokertecken för Network-cmdletar</span><span class="sxs-lookup"><span data-stu-id="558f8-1256">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="558f8-1257">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="558f8-1257">Az.RecoveryServices</span></span>
* <span data-ttu-id="558f8-1258">Stöd har lagts till för SQL Server i virtuella Azure-datorer</span><span class="sxs-lookup"><span data-stu-id="558f8-1258">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="558f8-1259">SDK-uppdatering</span><span class="sxs-lookup"><span data-stu-id="558f8-1259">SDK Update</span></span>
* <span data-ttu-id="558f8-1260">Get-ProtectableItem-incheckning i VMappContainer har tagits bort</span><span class="sxs-lookup"><span data-stu-id="558f8-1260">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="558f8-1261">Name och ServerName har lagts till som parametrar för Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="558f8-1261">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="558f8-1262">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="558f8-1262">Az.Resources</span></span>
* <span data-ttu-id="558f8-1263">Lägg till parametern `-TemplateObject` i cmdletar för distribution</span><span class="sxs-lookup"><span data-stu-id="558f8-1263">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="558f8-1264">Mer information här: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="558f8-1264">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="558f8-1265">Åtgärda problem med piping av resultatet i `Get-AzResource` till `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="558f8-1265">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="558f8-1266">Mer information här: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="558f8-1266">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="558f8-1267">Åtgärda problem med ändring av JSON-datatyp när `Set-AzResource` körs</span><span class="sxs-lookup"><span data-stu-id="558f8-1267">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="558f8-1268">Mer information här: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="558f8-1268">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="558f8-1269">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="558f8-1269">Az.Sql</span></span>
* <span data-ttu-id="558f8-1270">AuditingEndpointsCommunicator uppdateras.</span><span class="sxs-lookup"><span data-stu-id="558f8-1270">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="558f8-1271">Åtgärdar beteendet hos ett gränsscenario när nya diagnostikinställningar skapas.</span><span class="sxs-lookup"><span data-stu-id="558f8-1271">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="558f8-1272">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="558f8-1272">Az.Storage</span></span>
* <span data-ttu-id="558f8-1273">Stöd för BlockBlobStorage när Storage-konto skapas      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="558f8-1273">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="558f8-1274">1.4.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="558f8-1274">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="558f8-1275">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="558f8-1275">Az.AnalysisServices</span></span>
* <span data-ttu-id="558f8-1276">Inaktuell AddAzureASAccount-cmdlet</span><span class="sxs-lookup"><span data-stu-id="558f8-1276">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="558f8-1277">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="558f8-1277">Az.Automation</span></span>
* <span data-ttu-id="558f8-1278">Hjälpen för Import-AzAutomationDscNodeConfiguration har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="558f8-1278">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="558f8-1279">Konfigurationsnamnsvalidering har lagts till i cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="558f8-1279">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="558f8-1280">Förbättrad felhantering för cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="558f8-1280">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="558f8-1281">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="558f8-1281">Az.CognitiveServices</span></span>
* <span data-ttu-id="558f8-1282">CustomSubdomainName har lagts till som en ny valfri parameter för New-AzCognitiveServicesAccount, som används för att ange underdomän för resursen.</span><span class="sxs-lookup"><span data-stu-id="558f8-1282">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="558f8-1283">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="558f8-1283">Az.Compute</span></span>
* <span data-ttu-id="558f8-1284">Problemet med ID-parameteruppsättningar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="558f8-1284">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="558f8-1285">Get-AzVMExtension har uppdaterats så att alla installerade tillägg visas om parametern Name inte har angetts</span><span class="sxs-lookup"><span data-stu-id="558f8-1285">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="558f8-1286">Parametrarna Tag och ResourceId har lagts till i cmdleten Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="558f8-1286">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="558f8-1287">Get-AzVmssVM utan instans-ID och med InstanceView kan visa virtuella VMSS-datorer med instansvyn.</span><span class="sxs-lookup"><span data-stu-id="558f8-1287">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="558f8-1288">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="558f8-1288">Az.DataLakeStore</span></span>
* <span data-ttu-id="558f8-1289">Cmdletar har lagts till för uppräkning och återställning av borttagna objekt i ADL</span><span class="sxs-lookup"><span data-stu-id="558f8-1289">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="558f8-1290">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="558f8-1290">Az.EventHub</span></span>
* <span data-ttu-id="558f8-1291">Ny boolesk egenskap SkipEmptyArchives har lagts till i Skip Empty Archives i CaptureDescription-klassen i Eventhub</span><span class="sxs-lookup"><span data-stu-id="558f8-1291">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="558f8-1292">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="558f8-1292">Az.KeyVault</span></span>
* <span data-ttu-id="558f8-1293">Taggning i Set-AzKeyVaultSecret har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="558f8-1293">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="558f8-1294">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="558f8-1294">Az.LogicApp</span></span>
* <span data-ttu-id="558f8-1295">Grundläggande SKU har lagts till för Integrationskonton</span><span class="sxs-lookup"><span data-stu-id="558f8-1295">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="558f8-1296">XSLT 2.0, XSLT 3.0 och Flytande mappningstyper har lagts till</span><span class="sxs-lookup"><span data-stu-id="558f8-1296">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="558f8-1297">Nya cmdletar för integrationskontosammansättningar</span><span class="sxs-lookup"><span data-stu-id="558f8-1297">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="558f8-1298">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="558f8-1298">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="558f8-1299">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="558f8-1299">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="558f8-1300">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="558f8-1300">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="558f8-1301">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="558f8-1301">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="558f8-1302">Nya cmdletar för batchkonfiguration för integrationskonto</span><span class="sxs-lookup"><span data-stu-id="558f8-1302">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="558f8-1303">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="558f8-1303">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="558f8-1304">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="558f8-1304">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="558f8-1305">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="558f8-1305">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="558f8-1306">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="558f8-1306">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="558f8-1307">Logic App-SDK har uppdaterats till version 4.1.0</span><span class="sxs-lookup"><span data-stu-id="558f8-1307">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="558f8-1308">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="558f8-1308">Az.Monitor</span></span>
* <span data-ttu-id="558f8-1309">Hjälpen för Get-AzMetric har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="558f8-1309">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="558f8-1310">Az.Network</span><span class="sxs-lookup"><span data-stu-id="558f8-1310">Az.Network</span></span>
* <span data-ttu-id="558f8-1311">Hjälpexempel för Add-AzApplicationGatewayCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="558f8-1311">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="558f8-1312">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="558f8-1312">Az.OperationalInsights</span></span>
* <span data-ttu-id="558f8-1313">Ytterligare stöd för datakällorna New och Get ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="558f8-1313">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="558f8-1314">Ny ApplicationInsights-typ har lagts till för att ge stöd för ”Get specific” och ”Get all” för ApplicationInsights-datakällor för angiven arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="558f8-1314">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="558f8-1315">Cmdleten New-AzOperationalInsightsApplicationInsightsDataSource har lagts till för att skapa datakälla med angivna parametrar för Application Insights-resurs: subscription Id, resourceGroupName och name.</span><span class="sxs-lookup"><span data-stu-id="558f8-1315">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="558f8-1316">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="558f8-1316">Az.Resources</span></span>
* <span data-ttu-id="558f8-1317">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="558f8-1317">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="558f8-1318">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="558f8-1318">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="558f8-1319">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="558f8-1319">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="558f8-1320">Fel som gör att KeyCredentials inte kan skapas upprepade gånger har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="558f8-1320">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="558f8-1321">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="558f8-1321">Az.Sql</span></span>
* <span data-ttu-id="558f8-1322">Lägg till stöd för hyperskalanivån för SQL DB</span><span class="sxs-lookup"><span data-stu-id="558f8-1322">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="558f8-1323">Ett fel har åtgärdats där återställningen kunde misslyckas på grund av onödiga inställningsegenskaper i restore-förfrågan</span><span class="sxs-lookup"><span data-stu-id="558f8-1323">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="558f8-1324">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="558f8-1324">Az.Websites</span></span>
* <span data-ttu-id="558f8-1325">Rätt exempel i Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="558f8-1325">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="558f8-1326">1.3.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="558f8-1326">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="558f8-1327">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="558f8-1327">Az.Accounts</span></span>
* <span data-ttu-id="558f8-1328">Uppdatera till den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="558f8-1328">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="558f8-1329">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="558f8-1329">Az.AnalysisServices</span></span>
<span data-ttu-id="558f8-1330">Allmän tillgänglighet för Az.AnalysisServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="558f8-1330">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="558f8-1331">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="558f8-1331">Az.Compute</span></span>
* <span data-ttu-id="558f8-1332">AEM-tillägg: Lägg till stöd för UltraSSD-, P60-, P70- och P80-diskar</span><span class="sxs-lookup"><span data-stu-id="558f8-1332">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="558f8-1333">Uppdatera hjälpbeskrivning för Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="558f8-1333">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="558f8-1334">Uppdatera hjälpbeskrivning och exempel för Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="558f8-1334">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="558f8-1335">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="558f8-1335">Az.RecoveryServices</span></span>
<span data-ttu-id="558f8-1336">Allmän tillgänglighet för Az.RecoveryServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="558f8-1336">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="558f8-1337">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="558f8-1337">Az.Resources</span></span>
* <span data-ttu-id="558f8-1338">Korrigera taggar för resursgrupper</span><span class="sxs-lookup"><span data-stu-id="558f8-1338">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="558f8-1339">Mer information här: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="558f8-1339">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="558f8-1340">Åtgärda problem där `Get-AzureRmRoleAssignment` inte respekterar -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="558f8-1340">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="558f8-1341">Mer information här: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="558f8-1341">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="558f8-1342">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="558f8-1342">Az.Sql</span></span>
* <span data-ttu-id="558f8-1343">Lägga till Get/Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="558f8-1343">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="558f8-1344">Åtgärda problem där ett nullref-undantag uppstår när du kör SQL-cmdletar och inte är inloggad på ett Azure-konto</span><span class="sxs-lookup"><span data-stu-id="558f8-1344">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="558f8-1345">Åtgärda nullref-undantag i Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="558f8-1345">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="558f8-1346">1.2.1 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="558f8-1346">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="558f8-1347">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="558f8-1347">Az.Accounts</span></span>
* <span data-ttu-id="558f8-1348">Version med rätt version av autentisering</span><span class="sxs-lookup"><span data-stu-id="558f8-1348">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="558f8-1349">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="558f8-1349">Az.AnalysisServices</span></span>
* <span data-ttu-id="558f8-1350">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="558f8-1350">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="558f8-1351">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="558f8-1351">Az.RecoveryServices</span></span>
* <span data-ttu-id="558f8-1352">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="558f8-1352">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="558f8-1353">1.2.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="558f8-1353">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="558f8-1354">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="558f8-1354">Az.Accounts</span></span>
* <span data-ttu-id="558f8-1355">Lägga till interaktiv autentisering och autentisering med användarnamn/lösenord för endast Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="558f8-1355">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="558f8-1356">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="558f8-1356">Update incorrect online help URLs</span></span>
* <span data-ttu-id="558f8-1357">Lägga till varningsmeddelande i PS Core för Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="558f8-1357">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="558f8-1358">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="558f8-1358">Az.Aks</span></span>
* <span data-ttu-id="558f8-1359">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="558f8-1359">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="558f8-1360">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="558f8-1360">Az.Automation</span></span>
* <span data-ttu-id="558f8-1361">Stöd för Python 2-runbookflöden har lagts till</span><span class="sxs-lookup"><span data-stu-id="558f8-1361">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="558f8-1362">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="558f8-1362">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="558f8-1363">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="558f8-1363">Az.Cdn</span></span>
* <span data-ttu-id="558f8-1364">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="558f8-1364">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="558f8-1365">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="558f8-1365">Az.Compute</span></span>
* <span data-ttu-id="558f8-1366">Lägga till cmdleten Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="558f8-1366">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="558f8-1367">Lägga till TempDisk-parameter i Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="558f8-1367">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="558f8-1368">Korrigera varningsmeddelande för New-AzVM</span><span class="sxs-lookup"><span data-stu-id="558f8-1368">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="558f8-1369">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="558f8-1369">Az.ContainerRegistry</span></span>
* <span data-ttu-id="558f8-1370">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="558f8-1370">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="558f8-1371">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="558f8-1371">Az.DataFactory</span></span>
* <span data-ttu-id="558f8-1372">ADF .Net SDK-versionen har uppdaterats till 3.0.0</span><span class="sxs-lookup"><span data-stu-id="558f8-1372">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="558f8-1373">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="558f8-1373">Az.DataLakeStore</span></span>
* <span data-ttu-id="558f8-1374">Åtgärda problem med ADLS-slutpunkt vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="558f8-1374">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="558f8-1375">Mer information här: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="558f8-1375">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="558f8-1376">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="558f8-1376">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="558f8-1377">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="558f8-1377">Az.IotHub</span></span>
* <span data-ttu-id="558f8-1378">Lägga till kodningsformat i cmdleten Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="558f8-1378">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="558f8-1379">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="558f8-1379">Az.KeyVault</span></span>
* <span data-ttu-id="558f8-1380">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="558f8-1380">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="558f8-1381">Az.Network</span><span class="sxs-lookup"><span data-stu-id="558f8-1381">Az.Network</span></span>
* <span data-ttu-id="558f8-1382">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="558f8-1382">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="558f8-1383">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="558f8-1383">Az.Resources</span></span>
* <span data-ttu-id="558f8-1384">Åtgärda felaktiga exempel i referensdokumentationen ”New-AzADAppCredential” och ”New-AzADSpCredential”</span><span class="sxs-lookup"><span data-stu-id="558f8-1384">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="558f8-1385">Åtgärda problem där sökvägen för parametern ”-TemplateFile” inte omvandlas innan cmdletarna för distribution i resursgruppen körs</span><span class="sxs-lookup"><span data-stu-id="558f8-1385">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="558f8-1386">Az.Resources: Korrigera dokumentationen om standardvärdet för New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="558f8-1386">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="558f8-1387">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="558f8-1387">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="558f8-1388">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="558f8-1388">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="558f8-1389">Åtgärda formateringsproblemet med objektet ”PSResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="558f8-1389">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="558f8-1390">Mer information här: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="558f8-1390">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="558f8-1391">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="558f8-1391">Az.ServiceFabric</span></span>
* <span data-ttu-id="558f8-1392">Återställ när ett certifikat läggs till i en Virtual Machine Scale Sets-modell men ett undantag genereras. Detta har gjorts för att åtgärda följande fel: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="558f8-1392">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="558f8-1393">Korrigera några felmeddelanden.</span><span class="sxs-lookup"><span data-stu-id="558f8-1393">Fix some error messages.</span></span>
* <span data-ttu-id="558f8-1394">Korrigering av skapande av kluster med ARM-mall som är standard för New-AzServiceFabriCluster som inte fungerade med migrering till Az.</span><span class="sxs-lookup"><span data-stu-id="558f8-1394">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="558f8-1395">Korrigering av tilläggning av kluster/programcertifikat så att endast VM Scale Sets som motsvarar klustret läggs till genom att kontrollera ID för klustret i tillägget.</span><span class="sxs-lookup"><span data-stu-id="558f8-1395">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="558f8-1396">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="558f8-1396">Az.SignalR</span></span>
* <span data-ttu-id="558f8-1397">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="558f8-1397">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="558f8-1398">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="558f8-1398">Az.Sql</span></span>
* <span data-ttu-id="558f8-1399">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="558f8-1399">Update incorrect online help URLs</span></span>
* <span data-ttu-id="558f8-1400">Uppdaterad parameterbeskrivning för LicenseType-parameter med möjliga värden</span><span class="sxs-lookup"><span data-stu-id="558f8-1400">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="558f8-1401">Korrigering för att uppdatera hanterad instansidentitet som inte fungerar när det är den enda uppdaterade egenskapen</span><span class="sxs-lookup"><span data-stu-id="558f8-1401">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="558f8-1402">Stöd för anpassad sortering på hanterad instans</span><span class="sxs-lookup"><span data-stu-id="558f8-1402">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="558f8-1403">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="558f8-1403">Az.Storage</span></span>
* <span data-ttu-id="558f8-1404">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="558f8-1404">Update incorrect online help URLs</span></span>
* <span data-ttu-id="558f8-1405">Tillhandahåll detaljerat felmeddelande när en användare försöker hämta/konfigurera klassisk loggning/mått på ett Premium Storage-konto eftersom Premium Storage-kontot inte har stöd för klassisk loggning/mått.</span><span class="sxs-lookup"><span data-stu-id="558f8-1405">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="558f8-1406">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="558f8-1406">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="558f8-1407">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="558f8-1407">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="558f8-1408">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="558f8-1408">Az.TrafficManager</span></span>
* <span data-ttu-id="558f8-1409">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="558f8-1409">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="558f8-1410">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="558f8-1410">Az.Websites</span></span>
* <span data-ttu-id="558f8-1411">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="558f8-1411">Update incorrect online help URLs</span></span>
* <span data-ttu-id="558f8-1412">Korrigerar ”New-AzWebAppSSLBinding” så att certifikatet laddas upp till rätt resursgrupp och plats om appen finns i en ASE.</span><span class="sxs-lookup"><span data-stu-id="558f8-1412">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="558f8-1413">Korrigerar ”New-AzWebAppSSLBinding” så att taggarna inte skrivs över på en bindning av ett SSL-certifikat till en app</span><span class="sxs-lookup"><span data-stu-id="558f8-1413">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="558f8-1414">1.1.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="558f8-1414">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="558f8-1415">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="558f8-1415">Az.Accounts</span></span>
* <span data-ttu-id="558f8-1416">Lade till omfattningen ”Lokal” till Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="558f8-1416">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="558f8-1417">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="558f8-1417">Az.Compute</span></span>
* <span data-ttu-id="558f8-1418">Namn är nu valfritt i ID-parametern för Restart/Start/Stop/Remove/Set-AzVM och Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="558f8-1418">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="558f8-1419">Uppdaterade beskrivningen av ID i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="558f8-1419">Updated the description of ID in help files</span></span>
* <span data-ttu-id="558f8-1420">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="558f8-1420">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="558f8-1421">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="558f8-1421">Az.DataLakeStore</span></span>
* <span data-ttu-id="558f8-1422">Uppdatera sdk-versionen av dataplanet till 1.1.14 för SDK-korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="558f8-1422">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="558f8-1423">Korrigerade hanteringen av negativ accesstime och modificationtime för getfilestatus och liststatus; korrigera asynkront annulleringstoken</span><span class="sxs-lookup"><span data-stu-id="558f8-1423">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="558f8-1424">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="558f8-1424">Az.EventGrid</span></span>
* <span data-ttu-id="558f8-1425">Uppdaterat för användning av API-versionen 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="558f8-1425">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="558f8-1426">Uppdaterade följande cmdletar för att stödja nytt scenario i API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="558f8-1426">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="558f8-1427">New-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="558f8-1427">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="558f8-1428">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="558f8-1428">Event Time-To-Live,</span></span>
        - <span data-ttu-id="558f8-1429">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="558f8-1429">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="558f8-1430">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="558f8-1430">Dead letter endpoint.</span></span>
    - <span data-ttu-id="558f8-1431">Update-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="558f8-1431">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="558f8-1432">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="558f8-1432">Event Time-To-Live,</span></span>
        - <span data-ttu-id="558f8-1433">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="558f8-1433">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="558f8-1434">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="558f8-1434">Dead letter endpoint.</span></span>
* <span data-ttu-id="558f8-1435">Lade till nya enum-värden (storageQueue och hybridConnection) för alternativet EndpointType i cmdletarna New-AzureRmEventGridSubscription och Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="558f8-1435">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="558f8-1436">Visa varningsmeddelanden om skapande eller uppdatering av händelseprenumerationen förväntas medföra manuell åtgärd från användaren.</span><span class="sxs-lookup"><span data-stu-id="558f8-1436">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="558f8-1437">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="558f8-1437">Az.IotHub</span></span>
* <span data-ttu-id="558f8-1438">Har uppdaterats till den senaste versionen av SDK:n lotHub</span><span class="sxs-lookup"><span data-stu-id="558f8-1438">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="558f8-1439">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="558f8-1439">Az.LogicApp</span></span>
* <span data-ttu-id="558f8-1440">Get-AzLogicApp visar en lista över alla som inte har angivet namn</span><span class="sxs-lookup"><span data-stu-id="558f8-1440">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="558f8-1441">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="558f8-1441">Az.Resources</span></span>
* <span data-ttu-id="558f8-1442">Åtgärdade problem med parameteruppsättningen när parametrarna -ODataQuery och -ResourceId anges för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="558f8-1442">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="558f8-1443">Mer information här: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="558f8-1443">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="558f8-1444">Åtgärdade hantering av parametern -Custom i New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="558f8-1444">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="558f8-1445">Korrigerade stavfel i New-AzDeployment-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="558f8-1445">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="558f8-1446">Gjorde parametern -MailNickname obligatorisk för New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="558f8-1446">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="558f8-1447">Mer information här: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="558f8-1447">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="558f8-1448">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="558f8-1448">Az.SignalR</span></span>
* <span data-ttu-id="558f8-1449">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="558f8-1449">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="558f8-1450">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="558f8-1450">Az.Sql</span></span>
* <span data-ttu-id="558f8-1451">Konverterade lagringshanteringsklientens beroende av den normala SDK-implementeringen.</span><span class="sxs-lookup"><span data-stu-id="558f8-1451">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="558f8-1452">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="558f8-1452">Az.Storage</span></span>
* <span data-ttu-id="558f8-1453">Angav StorageAccountName för lagringskontext som det verkliga namnet på lagringskontot när det skapas med Sas Token, OAuth eller Anonymous</span><span class="sxs-lookup"><span data-stu-id="558f8-1453">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="558f8-1454">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="558f8-1454">New-AzStorageContext</span></span>
* <span data-ttu-id="558f8-1455">Skapade Sas Token för Blob Snapshot-objekt med parametern -FullUri, åtgärdade den returnerade URI:n så att den blir URI för ögonblicksbild</span><span class="sxs-lookup"><span data-stu-id="558f8-1455">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="558f8-1456">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="558f8-1456">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="558f8-1457">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="558f8-1457">Az.Websites</span></span>
* <span data-ttu-id="558f8-1458">Åtgärdade en bugg i datumparsningen i Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="558f8-1458">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="558f8-1459">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="558f8-1459">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="558f8-1460">1.0.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="558f8-1460">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="558f8-1461">Allmänt</span><span class="sxs-lookup"><span data-stu-id="558f8-1461">General</span></span>

- <span data-ttu-id="558f8-1462">Allmän tillgänglighet för Az-modulen</span><span class="sxs-lookup"><span data-stu-id="558f8-1462">General Availability of Az Module</span></span>
- <span data-ttu-id="558f8-1463">Onlinehjälp för varje modul</span><span class="sxs-lookup"><span data-stu-id="558f8-1463">Online help for each module</span></span>
- <span data-ttu-id="558f8-1464">Mer information och en översikt finns på [Az-informationssidan](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="558f8-1464">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="558f8-1465">Information om hur du migrerar från AzureRM finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="558f8-1465">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="558f8-1466">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="558f8-1466">Az.Accounts</span></span>
- <span data-ttu-id="558f8-1467">Har ändrats från Az.Profile</span><span class="sxs-lookup"><span data-stu-id="558f8-1467">Changed from Az.Profile</span></span>
- <span data-ttu-id="558f8-1468">Fasta tabellformat för profil- och kontexttyper</span><span class="sxs-lookup"><span data-stu-id="558f8-1468">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="558f8-1469">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="558f8-1469">Az.ApiManagement</span></span>
- <span data-ttu-id="558f8-1470">Korrigeringar för #7002</span><span class="sxs-lookup"><span data-stu-id="558f8-1470">Fixes for #7002</span></span>
- <span data-ttu-id="558f8-1471">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="558f8-1471">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="558f8-1472">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="558f8-1472">Az.Batch</span></span>
- <span data-ttu-id="558f8-1473">Lade till möjligheten att se vilken version av Azure Batch Node Agent som körs på var och en av de virtuella datorerna i en pool, via den nya egenskapen `NodeAgentInformation` på `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="558f8-1473">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="558f8-1474">Standarden `Caching` för `PSDataDisk` är nu `ReadWrite` i stället för `None`.</span><span class="sxs-lookup"><span data-stu-id="558f8-1474">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="558f8-1475">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="558f8-1475">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="558f8-1476">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="558f8-1476">Az.Billing</span></span>
- <span data-ttu-id="558f8-1477">Kombinerar cmdletarna för fakturering, förbrukning och UsageAggregates. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="558f8-1477">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="558f8-1478">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="558f8-1478">Az.CognitivServices</span></span>
- <span data-ttu-id="558f8-1479">Lade till kompletterare för SkuName och Typem som är tillgängliga i New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="558f8-1479">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="558f8-1480">Tog bort parameteruppsättningen GetSkusWithAccountParamSetName från Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="558f8-1480">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="558f8-1481">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="558f8-1481">Az.ContainerInstance</span></span>
- <span data-ttu-id="558f8-1482">Stöd för ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="558f8-1482">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="558f8-1483">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="558f8-1483">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="558f8-1484">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="558f8-1484">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="558f8-1485">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="558f8-1485">Az.DataLakeStore</span></span>
- <span data-ttu-id="558f8-1486">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="558f8-1486">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="558f8-1487">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="558f8-1487">Az.Monitor</span></span>
- <span data-ttu-id="558f8-1488">Döpte om Az.Insights till Az.Monitor och andra mindre icke-bakåtkompatibla ändringar. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="558f8-1488">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="558f8-1489">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="558f8-1489">Az.KeyVault</span></span>
- <span data-ttu-id="558f8-1490">Tog bort den inaktuella egenskapen PurgeDisabled från utdatatyper</span><span class="sxs-lookup"><span data-stu-id="558f8-1490">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="558f8-1491">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="558f8-1491">Az.MachineLearning</span></span>
- <span data-ttu-id="558f8-1492">Inkluderade cmdletarna från modulen Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="558f8-1492">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="558f8-1493">Az.Media</span><span class="sxs-lookup"><span data-stu-id="558f8-1493">Az.Media</span></span>
- <span data-ttu-id="558f8-1494">Tog bort inaktuella -Tags-alias från New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="558f8-1494">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="558f8-1495">Az.Network</span><span class="sxs-lookup"><span data-stu-id="558f8-1495">Az.Network</span></span>
<span data-ttu-id="558f8-1496">Stöd har lagts till för konfiguration av RewriteRuleSets i Application Gateway</span><span class="sxs-lookup"><span data-stu-id="558f8-1496">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="558f8-1497">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="558f8-1497">New cmdlets added:</span></span>
        - <span data-ttu-id="558f8-1498">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="558f8-1498">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="558f8-1499">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="558f8-1499">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="558f8-1500">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="558f8-1500">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="558f8-1501">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="558f8-1501">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="558f8-1502">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="558f8-1502">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="558f8-1503">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="558f8-1503">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="558f8-1504">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="558f8-1504">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="558f8-1505">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="558f8-1505">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="558f8-1506">Cmdletar har uppdaterats med den valfria parametern -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="558f8-1506">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="558f8-1507">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="558f8-1507">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="558f8-1508">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="558f8-1508">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="558f8-1509">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="558f8-1509">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="558f8-1510">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="558f8-1510">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="558f8-1511">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="558f8-1511">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="558f8-1512">New-AzureRmApplicationGatewayUrlPathMapConfig har lagt till KeyVault-stöd för Application Gateway med Identity.</span><span class="sxs-lookup"><span data-stu-id="558f8-1512">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="558f8-1513">Cmdletar har uppdaterats med den valfria parametern -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="558f8-1513">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="558f8-1514">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="558f8-1514">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="558f8-1515">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="558f8-1515">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="558f8-1516">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="558f8-1516">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="558f8-1517">Cmdleten New-AzApplicationGateway har uppdaterats med den valfria parametern -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="558f8-1517">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="558f8-1518">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="558f8-1518">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="558f8-1519">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="558f8-1519">Az.OperationalInsights</span></span>
- <span data-ttu-id="558f8-1520">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="558f8-1520">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="558f8-1521">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="558f8-1521">Az.Profile</span></span>
- <span data-ttu-id="558f8-1522">Modulnamnet har ändrats till Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="558f8-1522">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="558f8-1523">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="558f8-1523">Az.RecoveryServices</span></span>
- <span data-ttu-id="558f8-1524">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="558f8-1524">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="558f8-1525">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="558f8-1525">Az.Resources</span></span>
- <span data-ttu-id="558f8-1526">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="558f8-1526">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="558f8-1527">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="558f8-1527">Az.ServiceFabric</span></span>
- <span data-ttu-id="558f8-1528">Stöd för specificering av certifikat efter eget namn och tumavtryck</span><span class="sxs-lookup"><span data-stu-id="558f8-1528">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="558f8-1529">Information om fler icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="558f8-1529">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="558f8-1530">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="558f8-1530">Az.SIgnalR</span></span>
- <span data-ttu-id="558f8-1531">Allmän tillgänglighet för PowerShell-cmdletar för SIgnalR</span><span class="sxs-lookup"><span data-stu-id="558f8-1531">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="558f8-1532">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="558f8-1532">Az.Sql</span></span>
- <span data-ttu-id="558f8-1533">Lade till de nya identifieringstyperna Data_Exfiltration och Unsafe_Action i Threat Detection-cmdletar</span><span class="sxs-lookup"><span data-stu-id="558f8-1533">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="558f8-1534">Uppdaterade dokumentationsexempel för Sql Auditing-cmdletar</span><span class="sxs-lookup"><span data-stu-id="558f8-1534">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="558f8-1535">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="558f8-1535">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="558f8-1536">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="558f8-1536">Az.Storage</span></span>
- <span data-ttu-id="558f8-1537">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="558f8-1537">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="558f8-1538">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="558f8-1538">Az.Websites</span></span>
- <span data-ttu-id="558f8-1539">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="558f8-1539">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="558f8-1540">0.7.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="558f8-1540">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="558f8-1541">Allmänt</span><span class="sxs-lookup"><span data-stu-id="558f8-1541">General</span></span>

* <span data-ttu-id="558f8-1542">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="558f8-1542">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="558f8-1543">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="558f8-1543">Az.Compute</span></span>

* <span data-ttu-id="558f8-1544">Lade till stöd för UltraSSD och Galleriavbildningar i de enkla parameteruppsättningarna för `New-AzVm(ss)`-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="558f8-1544">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="558f8-1545">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="558f8-1545">Az.DataLakeStore</span></span>

* <span data-ttu-id="558f8-1546">Åtgärdade avslutande snedstreck i domänen för adls-konto</span><span class="sxs-lookup"><span data-stu-id="558f8-1546">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="558f8-1547">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="558f8-1547">Az.FrontDoor</span></span>

* <span data-ttu-id="558f8-1548">Brutna länkar korrigerades</span><span class="sxs-lookup"><span data-stu-id="558f8-1548">Fixed some broken links</span></span>
    - <span data-ttu-id="558f8-1549">I artiklarna New-AzureRmFrontDoor och Set-AzureRmFrontDoor artiklar korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="558f8-1549">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="558f8-1550">I artikeln New-AzureRmFrontDoorManagedRuleObject korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="558f8-1550">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="558f8-1551">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="558f8-1551">Az.RecoveryServices</span></span>

* <span data-ttu-id="558f8-1552">Lade till valideringar på klientsidan för Azure-filresurs med återställningsåtgärder.</span><span class="sxs-lookup"><span data-stu-id="558f8-1552">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="558f8-1553">Gjorde storageAccountName och storageAccountResourceGroupName valfritt för afs-återställning.</span><span class="sxs-lookup"><span data-stu-id="558f8-1553">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="558f8-1554">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="558f8-1554">Az.Resources</span></span>

* <span data-ttu-id="558f8-1555">Korrigering för https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="558f8-1555">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="558f8-1556">Uppdaterade Get-AzureRmRoleAssignment så att prenumerationsomfattningen används om den anges vid begäran om klassiska administratörer.</span><span class="sxs-lookup"><span data-stu-id="558f8-1556">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="558f8-1557">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="558f8-1557">Az.Sql</span></span>

* <span data-ttu-id="558f8-1558">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="558f8-1558">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="558f8-1559">Korrigerade ett problem med Get-AzureRmSqlDatabaseVulnerabilityAssessment med DotNet-kärna</span><span class="sxs-lookup"><span data-stu-id="558f8-1559">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="558f8-1560">Ändrade dokumentationen för hjälpmeddelanden som rör SQL Auditing-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="558f8-1560">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="558f8-1561">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="558f8-1561">Az.Storage</span></span>

* <span data-ttu-id="558f8-1562">Lade till -EnableHierarchicalNamespace i New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="558f8-1562">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="558f8-1563">Åtgärdade problemet med att cmdleten Copy File inte kunde återanvända källkontexten på målet om inte -DestContext angetts</span><span class="sxs-lookup"><span data-stu-id="558f8-1563">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="558f8-1564">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="558f8-1564">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="558f8-1565">Stöd för statisk webbplatskonfiguration</span><span class="sxs-lookup"><span data-stu-id="558f8-1565">Support Static Website configuration</span></span>
    - <span data-ttu-id="558f8-1566">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="558f8-1566">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="558f8-1567">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="558f8-1567">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="558f8-1568">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="558f8-1568">Az.Websites</span></span>

* <span data-ttu-id="558f8-1569">Set-AzureRmWebApp och Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="558f8-1569">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="558f8-1570">Ny parameter (-AzureStoragePath) har lagts till för att ange att Azure Storage-sökvägar ska monteras i containerappar i Windows och Linux.</span><span class="sxs-lookup"><span data-stu-id="558f8-1570">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="558f8-1571">Använder utdata från den nya cmdleten New-AzureRmWebAppAzureStoragePath som en parameter för att ange sökvägar för Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="558f8-1571">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="558f8-1572">0.6.1 – november 2018</span><span class="sxs-lookup"><span data-stu-id="558f8-1572">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="558f8-1573">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="558f8-1573">Az.ApiManagement</span></span>
* <span data-ttu-id="558f8-1574">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="558f8-1574">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="558f8-1575">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="558f8-1575">Az.Automation</span></span>
* <span data-ttu-id="558f8-1576">Swagger baserade Azure Automation-cmdletar</span><span class="sxs-lookup"><span data-stu-id="558f8-1576">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="558f8-1577">Cmdletar för Uppdateringshantering har lagts till</span><span class="sxs-lookup"><span data-stu-id="558f8-1577">Added Update Management cmdlets</span></span>
* <span data-ttu-id="558f8-1578">Cmdletar för källkontroll har lagts till</span><span class="sxs-lookup"><span data-stu-id="558f8-1578">Added Source Control cmdlets</span></span>
* <span data-ttu-id="558f8-1579">Remove-AzureRmAutomationHybridWorkerGroup-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="558f8-1579">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="558f8-1580">Kommandot för DSC-registreringsnod har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="558f8-1580">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="558f8-1581">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="558f8-1581">Az.Compute</span></span>
* <span data-ttu-id="558f8-1582">Problem med SystemAssigned-identitet har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="558f8-1582">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="558f8-1583">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="558f8-1583">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="558f8-1584">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="558f8-1584">Az.ContainerInstance</span></span>
* <span data-ttu-id="558f8-1585">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="558f8-1585">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="558f8-1586">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="558f8-1586">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="558f8-1587">uppdatera exempelbeskrivningen för marketplace-cmdletar</span><span class="sxs-lookup"><span data-stu-id="558f8-1587">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="558f8-1588">Az.Network</span><span class="sxs-lookup"><span data-stu-id="558f8-1588">Az.Network</span></span>
* <span data-ttu-id="558f8-1589">Cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomErreller Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="558f8-1589">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="558f8-1590">ICMP tillbaka till stöd för Azure Firewall-nätverksprotokoll har lagts till</span><span class="sxs-lookup"><span data-stu-id="558f8-1590">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="558f8-1591">Uppdatera cmdlet Test-AzureRmNetworkWatcherConnectivity, lägga till verifiering av mål-id, adress och port.</span><span class="sxs-lookup"><span data-stu-id="558f8-1591">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="558f8-1592">Åtgärda problem med minnesanvändning i VirtualNetwork-karta</span><span class="sxs-lookup"><span data-stu-id="558f8-1592">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="558f8-1593">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="558f8-1593">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="558f8-1594">Åtgärda för att ändra principen för en skyddad fildelning.</span><span class="sxs-lookup"><span data-stu-id="558f8-1594">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="558f8-1595">Tidszonsprincipen har konverterats till versaler.</span><span class="sxs-lookup"><span data-stu-id="558f8-1595">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="558f8-1596">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="558f8-1596">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="558f8-1597">Exempel i New-AzureRmRecoveryServicesAsrProtectableItem har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="558f8-1597">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="558f8-1598">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="558f8-1598">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="558f8-1599">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="558f8-1599">Az.Relay</span></span>
* <span data-ttu-id="558f8-1600">Valfri parameter -KeyValue till New-AzureRmRelayKey cmdlet har lagts till, vilket gör det möjligt för användare att tillhandahålla KeyValue.</span><span class="sxs-lookup"><span data-stu-id="558f8-1600">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="558f8-1601">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="558f8-1601">Az.Resources</span></span>
* <span data-ttu-id="558f8-1602">Uppdatera hjälpdokumentation för resursidentitet kopplad till parametrar i `New-AzureRmPolicyAssignment` och `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="558f8-1602">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="558f8-1603">Lägg till ett exempel för New-AzureRmPolicyDefinition som använder -Metadata</span><span class="sxs-lookup"><span data-stu-id="558f8-1603">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="558f8-1604">Korrigera så att skiftläge behålls i taggnycklar i NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="558f8-1604">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="558f8-1605">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="558f8-1605">Az.ServiceFabric</span></span>
* <span data-ttu-id="558f8-1606">Lägg till utfasningsmeddelanden för kommande icke-kompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="558f8-1606">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="558f8-1607">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="558f8-1607">Az.Sql</span></span>
* <span data-ttu-id="558f8-1608">Nya cmdletar för CRUD-åtgärder på Azure Sql Database-hanterad instans och Azure Sql-hanterad databas</span><span class="sxs-lookup"><span data-stu-id="558f8-1608">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="558f8-1609">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="558f8-1609">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="558f8-1610">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="558f8-1610">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="558f8-1611">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="558f8-1611">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="558f8-1612">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="558f8-1612">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="558f8-1613">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="558f8-1613">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="558f8-1614">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="558f8-1614">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="558f8-1615">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="558f8-1615">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="558f8-1616">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="558f8-1616">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="558f8-1617">Hantering av utökad granskningsprincip på en server eller en databas har aktiverats.</span><span class="sxs-lookup"><span data-stu-id="558f8-1617">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="558f8-1618">Ny parameter (PredicateExpression) har lagts till för att aktivera filtrering av granskningsloggar.</span><span class="sxs-lookup"><span data-stu-id="558f8-1618">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="558f8-1619">Cmdletar har ändrats så att de använder SQL-klienter i stället för äldre klienter.</span><span class="sxs-lookup"><span data-stu-id="558f8-1619">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="558f8-1620">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="558f8-1620">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="558f8-1621">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="558f8-1621">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="558f8-1622">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="558f8-1622">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="558f8-1623">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="558f8-1623">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="558f8-1624">Problem med att använda Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings med lagringskontots namnparameter har korrigerats</span><span class="sxs-lookup"><span data-stu-id="558f8-1624">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="558f8-1625">0.5.0 – november 2018</span><span class="sxs-lookup"><span data-stu-id="558f8-1625">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="558f8-1626">Allmänt</span><span class="sxs-lookup"><span data-stu-id="558f8-1626">General</span></span>
* <span data-ttu-id="558f8-1627">Lade till resurskompletterare till många kärn-cmdletar – dessa gör att du kan stega genom befintliga resursnamn med TABB vid interaktiva anrop till cmdletar</span><span class="sxs-lookup"><span data-stu-id="558f8-1627">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="558f8-1628">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="558f8-1628">Az.Profile</span></span>
* <span data-ttu-id="558f8-1629">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="558f8-1629">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="558f8-1630">Bytte namn på parametern TenantId i cmdleten Connect-AzAccount till Tenant och lade till ett alias för TenantId</span><span class="sxs-lookup"><span data-stu-id="558f8-1630">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="558f8-1631">Uppdaterade TenantId-beskrivningen för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="558f8-1631">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="558f8-1632">Åtgärda felmeddelande för misslyckad inloggning när du tillhandahåller klientdomän</span><span class="sxs-lookup"><span data-stu-id="558f8-1632">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="558f8-1633">Åtgärda problem med att kontextnamn hamnar i konflikt för konton utan prenumerationer i klientorganisationen</span><span class="sxs-lookup"><span data-stu-id="558f8-1633">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="558f8-1634">Åtgärda problem med DataLake-slutpunkter vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="558f8-1634">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="558f8-1635">Åtgärdade problem med att Disconnect-AzAccount kastades om den inte anslöts</span><span class="sxs-lookup"><span data-stu-id="558f8-1635">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="558f8-1636">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="558f8-1636">Az.CognitiveServices</span></span>
* <span data-ttu-id="558f8-1637">Lade till åtgärden Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="558f8-1637">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="558f8-1638">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="558f8-1638">Az.Compute</span></span>
* <span data-ttu-id="558f8-1639">Lade till cmdletarna Add-AzVmssVMDataDisk och Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="558f8-1639">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="558f8-1640">Get-AzVMImage visar AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="558f8-1640">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="558f8-1641">Åtgärdade att värdena för alternativen SetAzVMChefExtension -BootstrapOptions och -JsonAttribute inte angavs i json-format.</span><span class="sxs-lookup"><span data-stu-id="558f8-1641">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="558f8-1642">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="558f8-1642">Az.DataLakeStore</span></span>
* <span data-ttu-id="558f8-1643">Uppdatera DataLake-paketet till 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="558f8-1643">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="558f8-1644">Lägg till standardsamtidighet för flertrådade åtgärder.</span><span class="sxs-lookup"><span data-stu-id="558f8-1644">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="558f8-1645">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="558f8-1645">Az.Insights</span></span>
* <span data-ttu-id="558f8-1646">Åtgärdade problem #7267 (autoskalningsområde)</span><span class="sxs-lookup"><span data-stu-id="558f8-1646">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="558f8-1647">Problem med att uppräknade parametrar inte ställdes in ordentligt när du skapade en ny autoskalningsregel (de ställdes alltid in med standardvärdet).</span><span class="sxs-lookup"><span data-stu-id="558f8-1647">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="558f8-1648">Åtgärdade problem #7513 [Insights] Set-AzDiagnosticSetting kräver uttrycklig specifikation av kategorier när inställningar skapas</span><span class="sxs-lookup"><span data-stu-id="558f8-1648">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="558f8-1649">Nu kräver inte cmdleten uttrycklig anvisning av kategorierna för att aktiveras under skapande, d.v.s. den fungerar enligt beskrivning</span><span class="sxs-lookup"><span data-stu-id="558f8-1649">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="558f8-1650">Az.Network</span><span class="sxs-lookup"><span data-stu-id="558f8-1650">Az.Network</span></span>
* <span data-ttu-id="558f8-1651">PeeringType ändrades till en obligatorisk parameter för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="558f8-1651">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="558f8-1652">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="558f8-1652">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="558f8-1653">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="558f8-1653">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="558f8-1654">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="558f8-1654">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="558f8-1655">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="558f8-1655">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="558f8-1656">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="558f8-1656">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="558f8-1657">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="558f8-1657">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="558f8-1658">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="558f8-1658">Az.PolicyInsights</span></span>
* <span data-ttu-id="558f8-1659">Cmdletar för principreparation har lagts till</span><span class="sxs-lookup"><span data-stu-id="558f8-1659">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="558f8-1660">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="558f8-1660">Az.Resources</span></span>
* <span data-ttu-id="558f8-1661">Korrigering för https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="558f8-1661">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="558f8-1662">Tillåt att resurser listas med parametern -ResourceId för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="558f8-1662">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="558f8-1663">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="558f8-1663">Az.ServiceBus</span></span>
* <span data-ttu-id="558f8-1664">Skrivskyddad MigrationState-egenskap har lagts till i PSServiceBusMigrationConfigurationAttributes, som hjälper till att hålla koll på migreringstillståndet.</span><span class="sxs-lookup"><span data-stu-id="558f8-1664">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="558f8-1665">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="558f8-1665">Az.ServiceFabric</span></span>
* <span data-ttu-id="558f8-1666">Åtgärda att lägga till certifikat till Linux-Vmss.</span><span class="sxs-lookup"><span data-stu-id="558f8-1666">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="558f8-1667">Åtgärdade Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="558f8-1667">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="558f8-1668">Använd rätt tumavtryck från nya certifikat (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="558f8-1668">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="558f8-1669">Visa undantag korrekt (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="558f8-1669">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="558f8-1670">Åtgärdade Update-AzServiceFabricDurability så att klusterkonfigurationen uppdateras innan Vmss-åtgärden CreateOrUpdate påbörjas.</span><span class="sxs-lookup"><span data-stu-id="558f8-1670">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="558f8-1671">0.4.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="558f8-1671">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="558f8-1672">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="558f8-1672">Az.Profile</span></span>
* <span data-ttu-id="558f8-1673">Åtgärdade problemet med Get-AzSubscription i CloudShell</span><span class="sxs-lookup"><span data-stu-id="558f8-1673">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="558f8-1674">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="558f8-1674">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="558f8-1675">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="558f8-1675">Az.Compute</span></span>
* <span data-ttu-id="558f8-1676">Nya storlekar lades till i listan över godkända VM-storlekar för vilka accelererat nätverk kommer att aktiveras vid användning av den enkla parameteruppsättningen för New-AzVm</span><span class="sxs-lookup"><span data-stu-id="558f8-1676">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="558f8-1677">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="558f8-1677">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="558f8-1678">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="558f8-1678">Az.DataLakeStore</span></span>
* <span data-ttu-id="558f8-1679">Lägger till stöd för regler för virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="558f8-1679">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="558f8-1680">Get-AzDataLakeStoreVirtualNetworkRule: Hämtar eller listar regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="558f8-1680">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="558f8-1681">Add-AzDataLakeStoreVirtualNetworkRule: Lägger till en regel för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="558f8-1681">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="558f8-1682">Set-AzDataLakeStoreVirtualNetworkRule: Ändrar den angivna regeln för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="558f8-1682">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="558f8-1683">Remove-AzDataLakeStoreVirtualNetworkRule: Tar bort en regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="558f8-1683">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="558f8-1684">Az.Network</span><span class="sxs-lookup"><span data-stu-id="558f8-1684">Az.Network</span></span>
* <span data-ttu-id="558f8-1685">Skicka protokollvärdet till serverdelen för att uppdatera cmdleten Test-AzNetworkWatcherConnectivity.</span><span class="sxs-lookup"><span data-stu-id="558f8-1685">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="558f8-1686">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="558f8-1686">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="558f8-1687">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="558f8-1687">Az.Resources</span></span>
* <span data-ttu-id="558f8-1688">Åtgärdade problem där Get-AzRoleDefinition genererar ett oläsligt undantag (när standardprofilen inte innehåller någon prenumeration och ingen omfattning har angetts) genom att lägga till ett beskrivande undantag i scenariot.</span><span class="sxs-lookup"><span data-stu-id="558f8-1688">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="558f8-1689">Ställ in ”RoleDefinitionNameParameterSet” som standardparameteruppsättning.</span><span class="sxs-lookup"><span data-stu-id="558f8-1689">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="558f8-1690">0.3.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="558f8-1690">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="558f8-1691">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="558f8-1691">Azure.Storage</span></span>
* <span data-ttu-id="558f8-1692">Åtgärda fel där Kopiera blob/fil inte kopierar metadata när målplatsen har ett problem med metadata</span><span class="sxs-lookup"><span data-stu-id="558f8-1692">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="558f8-1693">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="558f8-1693">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="558f8-1694">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="558f8-1694">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="558f8-1695">Stöd för att hämta användningsinformation om en Storage-resurs för en specifik plats och för att lägga till ett varningsmeddelande för att hämta användningsinformation om en global Storage-resurs är inaktuellt.</span><span class="sxs-lookup"><span data-stu-id="558f8-1695">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="558f8-1696">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="558f8-1696">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="558f8-1697">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="558f8-1697">Az.CognitiveServices</span></span>
* <span data-ttu-id="558f8-1698">Stöd för Get-AzCognitiveServicesAccountSkus utan ett befintligt konto.</span><span class="sxs-lookup"><span data-stu-id="558f8-1698">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="558f8-1699">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="558f8-1699">Az.Compute</span></span>
* <span data-ttu-id="558f8-1700">Åtgärdade fel där Get-AzVM -ResourceGroupName <rg> returnerar fler än 50 resultat om det behövs</span><span class="sxs-lookup"><span data-stu-id="558f8-1700">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="558f8-1701">Lade till ett exempel för SimpleParameterSet i hjälpen för cmdleten New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="558f8-1701">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="558f8-1702">Ett stavfel i förloppsmeddelandet för Azure Disk Encryption har korrigerats</span><span class="sxs-lookup"><span data-stu-id="558f8-1702">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="558f8-1703">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="558f8-1703">Az.DataFactoryV2</span></span>
* <span data-ttu-id="558f8-1704">ADF .Net SDK-versionen har uppdaterats till 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="558f8-1704">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="558f8-1705">Az.Network</span><span class="sxs-lookup"><span data-stu-id="558f8-1705">Az.Network</span></span>
* <span data-ttu-id="558f8-1706">Funktionalitet för NetworkProfile har lagts till.</span><span class="sxs-lookup"><span data-stu-id="558f8-1706">Added NetworkProfile functionality.</span></span> <span data-ttu-id="558f8-1707">nya cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="558f8-1707">new cmdlets added</span></span>
    - <span data-ttu-id="558f8-1708">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="558f8-1708">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="558f8-1709">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="558f8-1709">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="558f8-1710">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="558f8-1710">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="558f8-1711">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="558f8-1711">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="558f8-1712">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="558f8-1712">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="558f8-1713">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="558f8-1713">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="558f8-1714">Länk för tjänstassociering på modell för undernät har lagts till</span><span class="sxs-lookup"><span data-stu-id="558f8-1714">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="558f8-1715">Cmdletarna New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap och Remove-AzVirtualNetworkTap har lagts till</span><span class="sxs-lookup"><span data-stu-id="558f8-1715">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="558f8-1716">Cmdletarna Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig och Remove-AzNEtworkInterfaceTapConfig har lagts till</span><span class="sxs-lookup"><span data-stu-id="558f8-1716">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="558f8-1717">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="558f8-1717">Az.RedisCache</span></span>
* <span data-ttu-id="558f8-1718">Tillåt att alla strängar används som storleksparametrar framöver.</span><span class="sxs-lookup"><span data-stu-id="558f8-1718">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="558f8-1719">Lägg till P5 i popup-fönstret PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="558f8-1719">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="558f8-1720">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="558f8-1720">Az.Resources</span></span>
* <span data-ttu-id="558f8-1721">Parametern -Mode som saknades i Set-AzPolicyDefinition har lagts till</span><span class="sxs-lookup"><span data-stu-id="558f8-1721">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="558f8-1722">Åtgärdade buggen för cmdleten Get-AzProviderOperation för åtgärder med ursprung som innehåller användare</span><span class="sxs-lookup"><span data-stu-id="558f8-1722">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="558f8-1723">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="558f8-1723">Az.Sql</span></span>
* <span data-ttu-id="558f8-1724">Ett problem där vissa cmdletar för säkerhetskopiering inte kunde identifiera den aktuella azure-prenumerationen har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="558f8-1724">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="558f8-1725">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="558f8-1725">Az.Websites</span></span>
* <span data-ttu-id="558f8-1726">Ny cmdlet: Get-AzWebAppContainerContinuousDeploymentUrl – Hämtar webhook-URL:en för kontinuerlig distribution av container</span><span class="sxs-lookup"><span data-stu-id="558f8-1726">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="558f8-1727">Nya cmdletar: New-AzWebAppContainerPSSession och Enter-WebAppContainerPSSession – Startar en PowerShell-fjärrsession i en containerapp för windows</span><span class="sxs-lookup"><span data-stu-id="558f8-1727">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="558f8-1728">0.2.0 – september 2018</span><span class="sxs-lookup"><span data-stu-id="558f8-1728">0.2.0 - September 2018</span></span>
 <span data-ttu-id="558f8-1729">Första versionen</span><span class="sxs-lookup"><span data-stu-id="558f8-1729">Initial Release</span></span>
