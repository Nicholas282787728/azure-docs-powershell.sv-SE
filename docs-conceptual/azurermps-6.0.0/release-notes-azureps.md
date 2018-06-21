---
title: Ändringslogg för Azure PowerShell | Microsoft Docs
description: Det här är en historik över de ändringar som gjorts i den senaste versionen av Azure PowerShell.
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 5/1/2018
ms.openlocfilehash: 8515a267e80e5d1f7bb97557efa72b9e86b7b45d
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/08/2018
ms.locfileid: "33912011"
---
# <a name="release-notes"></a><span data-ttu-id="707a7-103">Viktig information</span><span class="sxs-lookup"><span data-stu-id="707a7-103">Release notes</span></span>

<span data-ttu-id="707a7-104">Det här är en lista över ändringar som har gjorts i Azure PowerShell i den här versionen.</span><span class="sxs-lookup"><span data-stu-id="707a7-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---

## <a name="600---may-2018"></a><span data-ttu-id="707a7-105">6.0.0 – Maj 2018</span><span class="sxs-lookup"><span data-stu-id="707a7-105">6.0.0 - May 2018</span></span>

### <a name="general"></a><span data-ttu-id="707a7-106">Allmänt</span><span class="sxs-lookup"><span data-stu-id="707a7-106">General</span></span>
* <span data-ttu-id="707a7-107">Konfigurera minsta beroende för moduler till PowerShell 5.0</span><span class="sxs-lookup"><span data-stu-id="707a7-107">Set minimum dependency of modules to PowerShell 5.0</span></span>

### <a name="azurestorage"></a><span data-ttu-id="707a7-108">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="707a7-108">Azure.Storage</span></span>
* <span data-ttu-id="707a7-109">Stöd som namn på blob-behållare för Storage</span><span class="sxs-lookup"><span data-stu-id="707a7-109">Support  as Storage blob container name</span></span>
    - <span data-ttu-id="707a7-110">New-AzureStorageBlobContainer</span><span class="sxs-lookup"><span data-stu-id="707a7-110">New-AzureStorageBlobContainer</span></span>
    - <span data-ttu-id="707a7-111">Remove-AzureStorageBlobContainer</span><span class="sxs-lookup"><span data-stu-id="707a7-111">Remove-AzureStorageBlobContainer</span></span>
    - <span data-ttu-id="707a7-112">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="707a7-112">Set-AzureStorageBlobContent</span></span>
    - <span data-ttu-id="707a7-113">Get-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="707a7-113">Get-AzureStorageBlobContent</span></span>
* <span data-ttu-id="707a7-114">Åtgärda problemet med att vissa felmeddelanden om Storage-cmdletar inte innehåller information om felet</span><span class="sxs-lookup"><span data-stu-id="707a7-114">Fix the issue that some Storage cmdlets failure output not contain detail failure information</span></span>

### <a name="azurermapimanagement"></a><span data-ttu-id="707a7-115">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="707a7-115">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="707a7-116">Lägger till flera icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="707a7-116">Introduce multiple breaking changes</span></span>
    - <span data-ttu-id="707a7-117">Mer information finns i migreringsguiden</span><span class="sxs-lookup"><span data-stu-id="707a7-117">Please refer to the migration guide for more information</span></span>

### <a name="azurermautomation"></a><span data-ttu-id="707a7-118">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="707a7-118">AzureRM.Automation</span></span>
* <span data-ttu-id="707a7-119">Ta bort inaktuella alias för ”taggar” från cmdletar</span><span class="sxs-lookup"><span data-stu-id="707a7-119">Remove deprecated 'Tags' alias from cmdlets</span></span>
    - <span data-ttu-id="707a7-120">"Set-AzureRmAutomationRunbook"</span><span class="sxs-lookup"><span data-stu-id="707a7-120">'Set-AzureRmAutomationRunbook'</span></span>

### <a name="azurermbatch"></a><span data-ttu-id="707a7-121">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="707a7-121">AzureRM.Batch</span></span>
* <span data-ttu-id="707a7-122">Dokumentationen för New-AzureBatchPool för att ta bort inaktuella exempel har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="707a7-122">Updated New-AzureBatchPool documentation to remove deprecated example</span></span>

### <a name="azurermcdn"></a><span data-ttu-id="707a7-123">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="707a7-123">AzureRM.Cdn</span></span>
* <span data-ttu-id="707a7-124">Lägger till flera icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="707a7-124">Introduce multiple breaking changes</span></span>
    - <span data-ttu-id="707a7-125">Mer information finns i migreringsguiden</span><span class="sxs-lookup"><span data-stu-id="707a7-125">Please refer to the migration guide for more information</span></span>

### <a name="azurermcompute"></a><span data-ttu-id="707a7-126">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="707a7-126">AzureRM.Compute</span></span>
* <span data-ttu-id="707a7-127">”New-AzureRmVm” och ”New-AzureRmVmss” stöder utförliga utdata för parametrar</span><span class="sxs-lookup"><span data-stu-id="707a7-127">'New-AzureRmVm' and 'New-AzureRmVmss' support verbose output of parameters</span></span>
* <span data-ttu-id="707a7-128">”New-AzureRmVm” och ”New-AzureRmVmss” (enkelt parameteruppsättning) stöder tilldelning av användardefinierade och (eller) systemdefinierade identiteter till virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="707a7-128">'New-AzureRmVm' and 'New-AzureRmVmss' (simple parameter set) support assigning user defined and(or) system defined identities to the VM(s).</span></span>
* <span data-ttu-id="707a7-129">Funktionerna VMSS Redeploy and PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="707a7-129">VMSS Redeploy and PerformMaintenance feature</span></span>
    -  <span data-ttu-id="707a7-130">Lägg till de nya växelparametrarna -Redeploy och -PerformMaintenance till ”Set-AzureRmVmss” och ”Set-AzureRmVmssVM”</span><span class="sxs-lookup"><span data-stu-id="707a7-130">Add new switch parameter -Redeploy and -PerformMaintenance to 'Set-AzureRmVmss' and 'Set-AzureRmVmssVM'</span></span>
* <span data-ttu-id="707a7-131">Lägg till växelparametern DisableVMAgent till cmdleten ”Set-AzureRmVMOperatingSystem”</span><span class="sxs-lookup"><span data-stu-id="707a7-131">Add DisableVMAgent switch parameter to 'Set-AzureRmVMOperatingSystem' cmdlet</span></span>
* <span data-ttu-id="707a7-132">”New-AzureRmVm” och ”New-AzureRmVmss” (enkel parameteruppsättning) stöder en ”Win10”-avbildning.</span><span class="sxs-lookup"><span data-stu-id="707a7-132">'New-AzureRmVm' and 'New-AzureRmVmss' (simple parameter set) support a 'Win10' image.</span></span>
* <span data-ttu-id="707a7-133">Cmdleten ”Repair-AzureRmVmssServiceFabricUpdateDomain” har lagts till.</span><span class="sxs-lookup"><span data-stu-id="707a7-133">'Repair-AzureRmVmssServiceFabricUpdateDomain' cmdlet is added.</span></span>
* <span data-ttu-id="707a7-134">Lägger till flera icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="707a7-134">Introduce multiple breaking changes</span></span>
    - <span data-ttu-id="707a7-135">Mer information finns i guiden för migrering</span><span class="sxs-lookup"><span data-stu-id="707a7-135">Please refer to the migration guide for more details</span></span>
* <span data-ttu-id="707a7-136">”Set-AzureRmVmDiskEncryptionExtension” gör AAD-parametrar valfria</span><span class="sxs-lookup"><span data-stu-id="707a7-136">'Set-AzureRmVmDiskEncryptionExtension' makes AAD parameters optional</span></span>

### <a name="azurermdatafactories"></a><span data-ttu-id="707a7-137">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="707a7-137">AzureRM.DataFactories</span></span>
* <span data-ttu-id="707a7-138">Ta bort inaktuella alias för ”taggar” från cmdletar</span><span class="sxs-lookup"><span data-stu-id="707a7-138">Remove deprecated 'Tags' alias from cmdlets</span></span>
    - <span data-ttu-id="707a7-139">New-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="707a7-139">New-AzureRmDataFactory</span></span>

### <a name="azurermdatafactoryv2"></a><span data-ttu-id="707a7-140">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="707a7-140">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="707a7-141">SDK:n för ADF .Net har uppdaterats till version 0.7.0-preview som innehåller följande ändringar:</span><span class="sxs-lookup"><span data-stu-id="707a7-141">Updated the ADF .Net SDK version to 0.7.0-preview containing following changes:</span></span>
    - <span data-ttu-id="707a7-142">Körningsparametrar och egenskap för anslutningshantering har lagts till på ExecuteSSISPackage-aktivitet</span><span class="sxs-lookup"><span data-stu-id="707a7-142">Added execution parameters and connection managers property on ExecuteSSISPackage Activity</span></span>
    - <span data-ttu-id="707a7-143">PostgreSql, en MySql-länkad tjänst för att använda en fullständig anslutningssträng istället för server, databas, schema, användarnamn och lösenord har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="707a7-143">Updated PostgreSql, MySql llinked service to use full connection string instead of server, database, schema, username and password</span></span>
    - <span data-ttu-id="707a7-144">Schemat från DB2-länkad tjänst har tagits bort</span><span class="sxs-lookup"><span data-stu-id="707a7-144">Removed the schema from DB2 linked service</span></span>
    - <span data-ttu-id="707a7-145">Schemaegenskap från Teradata-länkad tjänst har tagits bort</span><span class="sxs-lookup"><span data-stu-id="707a7-145">Removed schema property from Teradata linked service</span></span>
    - <span data-ttu-id="707a7-146">LinkedService, Dataset, CopySource för Responsys har lagts till</span><span class="sxs-lookup"><span data-stu-id="707a7-146">Added LinkedService, Dataset, CopySource for Responsys</span></span>

### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="707a7-147">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="707a7-147">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="707a7-148">Ta bort inaktuella alias för ”taggar” från cmdletar</span><span class="sxs-lookup"><span data-stu-id="707a7-148">Remove deprecated 'Tags' alias from cmdlets</span></span>
    - <span data-ttu-id="707a7-149">”New-AzureRmDataLakeAnalyticsAccount”</span><span class="sxs-lookup"><span data-stu-id="707a7-149">'New-AzureRmDataLakeAnalyticsAccount'</span></span>
    - <span data-ttu-id="707a7-150">”Set-AzureRmDataLakeAnalyticsAccount”</span><span class="sxs-lookup"><span data-stu-id="707a7-150">'Set-AzureRmDataLakeAnalyticsAccount'</span></span>

### <a name="azurermdatalakestore"></a><span data-ttu-id="707a7-151">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="707a7-151">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="707a7-152">Lägg till ny funktion för rekursiv Acl-förändring för Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAclEntry och Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="707a7-152">Add new feature of recursive Acl Change to Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="707a7-153">Lägg till ny cmdlet för att hämta en innehållssammanfattning under en katalog</span><span class="sxs-lookup"><span data-stu-id="707a7-153">Add new cmdlet for retrieving the content summary under a directory</span></span>
* <span data-ttu-id="707a7-154">Lägg till ny cmdlet för att hämta dump angående diskanvändning och Acl</span><span class="sxs-lookup"><span data-stu-id="707a7-154">Add new cmdlet for retrieving the disk usage and Acl dump</span></span>
* <span data-ttu-id="707a7-155">Åtgärda returtypen för Set-AzureRmDataLakeStoreItemAcl-verktyget till IEnumerable<DataLakeStoreItemAce></span><span class="sxs-lookup"><span data-stu-id="707a7-155">Correct return type of Set-AzureRmDataLakeStoreItemAcl bool to IEnumerable<DataLakeStoreItemAce></span></span>
* <span data-ttu-id="707a7-156">Åtgärda returtypen för Set-AzureRmDataLakeStoreItemAclEntry-verktyget till IEnumerable<DataLakeStoreItemAce></span><span class="sxs-lookup"><span data-stu-id="707a7-156">Correct return type of Set-AzureRmDataLakeStoreItemAclEntry bool to IEnumerable<DataLakeStoreItemAce></span></span>
* <span data-ttu-id="707a7-157">Icke-bakåtkompatibla ändringar för Export-AzureRmDataLakeStoreItem, Import-AzureRmDataLakeStoreItem, Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="707a7-157">Breaking changes in Export-AzureRmDataLakeStoreItem, Import-AzureRmDataLakeStoreItem, Remove-AzureRmDataLakeStoreItem</span></span>

### <a name="azurermdns"></a><span data-ttu-id="707a7-158">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="707a7-158">AzureRM.Dns</span></span>
* <span data-ttu-id="707a7-159">Lägger till flera icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="707a7-159">Introduce multiple breaking changes</span></span>
    - <span data-ttu-id="707a7-160">Mer information finns i migreringsguiden</span><span class="sxs-lookup"><span data-stu-id="707a7-160">Please refer to the migration guide for more information</span></span>

### <a name="azurermeventhub"></a><span data-ttu-id="707a7-161">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="707a7-161">AzureRM.EventHub</span></span>
* <span data-ttu-id="707a7-162">Hjälp för cmdletar som saknar exempel har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="707a7-162">Updated Help for cmdlets with missing examples</span></span>

### <a name="azurerminsights"></a><span data-ttu-id="707a7-163">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="707a7-163">AzureRM.Insights</span></span>
* <span data-ttu-id="707a7-164">Flera icke-bakåtkompatibla ändringar har introducerats</span><span class="sxs-lookup"><span data-stu-id="707a7-164">Introduced multiple breaking changes</span></span>
    - <span data-ttu-id="707a7-165">Mer information finns i migreringsguiden</span><span class="sxs-lookup"><span data-stu-id="707a7-165">Please refer to the migration guide for more information</span></span>

### <a name="azurermiothub"></a><span data-ttu-id="707a7-166">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="707a7-166">AzureRM.IotHub</span></span>
* <span data-ttu-id="707a7-167">Aktivera taggar och grundläggande SKU för IotHub</span><span class="sxs-lookup"><span data-stu-id="707a7-167">Enable tags and Basic Sku to the IotHub</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="707a7-168">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="707a7-168">AzureRM.KeyVault</span></span>
* <span data-ttu-id="707a7-169">Icke-bakåtkompatibla ändringar för stöd för pipingscenarier</span><span class="sxs-lookup"><span data-stu-id="707a7-169">Breaking changes to support piping scenarios</span></span>
* <span data-ttu-id="707a7-170">Nya cmdletar har lagts till: Backup/Restore-AzureKeyVaultManagedStorageAccount, Backup/Restore-AzureKeyVaultCertificate, Undo-AzureKeyVaultManagedStorageSasDefinitionRemoval och Undo-AzureKeyVaultManagedStorageAccountRemoval</span><span class="sxs-lookup"><span data-stu-id="707a7-170">Added new cmdlets: Backup/Restore-AzureKeyVaultManagedStorageAccount, Backup/Restore-AzureKeyVaultCertificate, Undo-AzureKeyVaultManagedStorageSasDefinitionRemoval, and Undo-AzureKeyVaultManagedStorageAccountRemoval</span></span>

### <a name="azurermmachinelearning"></a><span data-ttu-id="707a7-171">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="707a7-171">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="707a7-172">Ta bort inaktuella alias för ”taggar” från cmdletar</span><span class="sxs-lookup"><span data-stu-id="707a7-172">Remove deprecated 'Tags' alias from cmdlets</span></span>
    - <span data-ttu-id="707a7-173">Update-AzureRmMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="707a7-173">Update-AzureRmMlCommitmentPlan</span></span>

### <a name="azurermmedia"></a><span data-ttu-id="707a7-174">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="707a7-174">AzureRM.Media</span></span>
* <span data-ttu-id="707a7-175">Ta bort inaktuella alias för ”taggar” från cmdletar</span><span class="sxs-lookup"><span data-stu-id="707a7-175">Remove deprecated 'Tags' alias from cmdlets</span></span>
    - <span data-ttu-id="707a7-176">”Set-AzureRmMediaService”</span><span class="sxs-lookup"><span data-stu-id="707a7-176">'Set-AzureRmMediaService'</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="707a7-177">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="707a7-177">AzureRM.Network</span></span>
* <span data-ttu-id="707a7-178">Lägg till stöd för planresurs för DDoS-skydd</span><span class="sxs-lookup"><span data-stu-id="707a7-178">Add support for DDoS protection plan resource</span></span>
* <span data-ttu-id="707a7-179">Flera icke-bakåtkompatibla ändringar har introducerats</span><span class="sxs-lookup"><span data-stu-id="707a7-179">Introduced multiple breaking changes</span></span>
    - <span data-ttu-id="707a7-180">Mer information finns i migreringsguiden</span><span class="sxs-lookup"><span data-stu-id="707a7-180">Please refer to the migration guide for more information</span></span>

### <a name="azurermnotificationhubs"></a><span data-ttu-id="707a7-181">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="707a7-181">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="707a7-182">Presentation av flera icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="707a7-182">Introduce multiple breaking changes</span></span>
    - <span data-ttu-id="707a7-183">Mer information finns i migreringsguiden</span><span class="sxs-lookup"><span data-stu-id="707a7-183">Please refer to the migration guide for more information</span></span>

### <a name="azurermoperationalinsights"></a><span data-ttu-id="707a7-184">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="707a7-184">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="707a7-185">Presentation av flera icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="707a7-185">Introduce multiple breaking changes</span></span>
    - <span data-ttu-id="707a7-186">Mer information finns i migreringsguiden</span><span class="sxs-lookup"><span data-stu-id="707a7-186">Please refer to the migration guide for more information</span></span>

### <a name="azurermprofile"></a><span data-ttu-id="707a7-187">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="707a7-187">AzureRM.Profile</span></span>
* <span data-ttu-id="707a7-188">Aktivera automatiskt sparande av kontext som standard</span><span class="sxs-lookup"><span data-stu-id="707a7-188">Enable context autosave by default</span></span>
* <span data-ttu-id="707a7-189">Lägg till egenskaperna USGovernmentOperationalInsightsEndpoint och USGovernmentOperationalInsightsEndpointResourceId i en Azure-miljö för US Gov.</span><span class="sxs-lookup"><span data-stu-id="707a7-189">Add USGovernmentOperationalInsightsEndpoint and USGovernmentOperationalInsightsEndpointResourceId properties to Azure environment for US Gov.</span></span>

### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="707a7-190">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="707a7-190">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="707a7-191">Autentiseringsrubriken i SiteRecovery-scenarier har korrigerats</span><span class="sxs-lookup"><span data-stu-id="707a7-191">Fixed Authentication Header in SiteRecovery scenarios</span></span>

### <a name="azurermrediscache"></a><span data-ttu-id="707a7-192">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="707a7-192">AzureRM.RedisCache</span></span>
* <span data-ttu-id="707a7-193">Flera icke-bakåtkompatibla ändringar har introducerats</span><span class="sxs-lookup"><span data-stu-id="707a7-193">Introduced multiple breaking changes</span></span>
    - <span data-ttu-id="707a7-194">Mer information finns i migreringsguiden</span><span class="sxs-lookup"><span data-stu-id="707a7-194">Please refer to the migration guide for more information</span></span>

### <a name="azurermresources"></a><span data-ttu-id="707a7-195">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="707a7-195">AzureRM.Resources</span></span>
* <span data-ttu-id="707a7-196">Ta bort den inaktuella parametern -AtScopeAndBelow från anropet Get-AzureRmRoledefinition</span><span class="sxs-lookup"><span data-stu-id="707a7-196">Remove obsolete parameter -AtScopeAndBelow from Get-AzureRmRoledefinition call</span></span>
* <span data-ttu-id="707a7-197">Inkludera tilldelningar till borttagna användare/grupper/huvudnamn för tjänsten i resultat för Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="707a7-197">Include assignments to deleted USers/Groups/ServicePrincipals in Get-AzureRmRoleAssignment result</span></span>
* <span data-ttu-id="707a7-198">Lägg till tabbifyllning för Scope och ResourceType</span><span class="sxs-lookup"><span data-stu-id="707a7-198">Add Tab completers for Scope and ResourceType</span></span>
* <span data-ttu-id="707a7-199">Lägg till bekväm cmdlet för att skapa huvudnamn för tjänst</span><span class="sxs-lookup"><span data-stu-id="707a7-199">Add convenience cmdlet for creating ServicePrincipals</span></span>
* <span data-ttu-id="707a7-200">Sammanfoga funktioner för att hämta och hitta med Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="707a7-200">Merge Get- and Find- functionality in Get-AzureRmResource</span></span>
* <span data-ttu-id="707a7-201">Lägg till AD-cmdletar:</span><span class="sxs-lookup"><span data-stu-id="707a7-201">Add AD Cmdlets:</span></span>
  - <span data-ttu-id="707a7-202">Remove-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="707a7-202">Remove-AzureRmADGroupMember</span></span>
  - <span data-ttu-id="707a7-203">Get-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="707a7-203">Get-AzureRmADGroup</span></span>
  - <span data-ttu-id="707a7-204">New-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="707a7-204">New-AzureRmADGroup</span></span>
  - <span data-ttu-id="707a7-205">Remove-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="707a7-205">Remove-AzureRmADGroup</span></span>
  - <span data-ttu-id="707a7-206">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="707a7-206">Remove-AzureRmADUser</span></span>
  - <span data-ttu-id="707a7-207">Update-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="707a7-207">Update-AzureRmADApplication</span></span>
  - <span data-ttu-id="707a7-208">Update-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="707a7-208">Update-AzureRmADServicePrincipal</span></span>
  - <span data-ttu-id="707a7-209">Update-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="707a7-209">Update-AzureRmADUser</span></span>

### <a name="azurermservicefabric"></a><span data-ttu-id="707a7-210">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="707a7-210">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="707a7-211">Uppdatera SKU för version av Linux-avbildning som är standard</span><span class="sxs-lookup"><span data-stu-id="707a7-211">Update default Linux image version sku</span></span>
  - <span data-ttu-id="707a7-212">SKU-uppdatering för UbuntuServer1604 som är standard för NewAzureServiceFabricCluster.cs</span><span class="sxs-lookup"><span data-stu-id="707a7-212">NewAzureServiceFabricCluster.cs default UbuntuServer1604 Sku update</span></span>

### <a name="azurermstorage"></a><span data-ttu-id="707a7-213">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="707a7-213">AzureRM.Storage</span></span>
* <span data-ttu-id="707a7-214">Flera icke-bakåtkompatibla ändringar har introducerats</span><span class="sxs-lookup"><span data-stu-id="707a7-214">Introduced multiple breaking changes</span></span>
    - <span data-ttu-id="707a7-215">Mer information finns i migreringsguiden</span><span class="sxs-lookup"><span data-stu-id="707a7-215">Please refer to the migration guide for more information</span></span>

### <a name="azurermwebsites"></a><span data-ttu-id="707a7-216">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="707a7-216">AzureRM.Websites</span></span>
* <span data-ttu-id="707a7-217">Uppgradera till den senaste versionen av Websites-SDK</span><span class="sxs-lookup"><span data-stu-id="707a7-217">Upgrade to latest version of the Websites SDK</span></span>
* <span data-ttu-id="707a7-218">Egenskaperna -AssignIdentity och -Httpsonly har lagts till för Set-AzureRmWebApp och Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="707a7-218">Added -AssignIdentity & -Httpsonly properties for Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
* <span data-ttu-id="707a7-219">Två nya cmdletar har lagts till: Get-AzureRmWebAppSnapshots och Restore-AzureRmWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="707a7-219">Added two new cmdlets: Get-AzureRmWebAppSnapshots and Restore-AzureRmWebAppSnapshot</span></span>
