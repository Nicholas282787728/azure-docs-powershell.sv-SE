---
title: Migreringsguide för Az 2.0.0
description: Den här migreringsguiden innehåller en lista över icke-bakåtkompatibla ändringar som gjorts i Az version 2.0 av Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/24/2019
ms.openlocfilehash: 5f15d1a4f1e8416d7214aceb78494867fe4aad52
ms.sourcegitcommit: 0b94b9566124331d0b15eb7f5a811305c254172e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/15/2019
ms.locfileid: "72370300"
---
# <a name="migration-guide-for-az-200"></a><span data-ttu-id="98041-103">Migreringsguide för Az 2.0.0</span><span class="sxs-lookup"><span data-stu-id="98041-103">Migration Guide for Az 2.0.0</span></span>

<span data-ttu-id="98041-104">I det här dokumentet beskriver vi ändringarna mellan Az-versionerna 1.0.0 och 2.0.0</span><span class="sxs-lookup"><span data-stu-id="98041-104">This document describes the changes between the 1.0.0 and 2.0.0 versions of Az</span></span> 

## <a name="table-of-contents"></a><span data-ttu-id="98041-105">Innehållsförteckning</span><span class="sxs-lookup"><span data-stu-id="98041-105">Table of Contents</span></span>
- [<span data-ttu-id="98041-106">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="98041-106">Module breaking changes</span></span>](#module-breaking-changes)
  - [<span data-ttu-id="98041-107">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="98041-107">Az.Compute</span></span>](#azcompute)
  - [<span data-ttu-id="98041-108">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="98041-108">Az.HDInsight</span></span>](#azhdinsight)
  - [<span data-ttu-id="98041-109">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="98041-109">Az.Storage</span></span>](#azstorage)

## <a name="module-breaking-changes"></a><span data-ttu-id="98041-110">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="98041-110">Module breaking changes</span></span>

### <a name="azcompute"></a><span data-ttu-id="98041-111">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="98041-111">Az.Compute</span></span>

- <span data-ttu-id="98041-112">Tog bort parametern `Managed` från `New-AzAvailabilitySet` och cmdletarna `Update-AzAvailabilitySet` för att använda ```Sku = Aligned```</span><span class="sxs-lookup"><span data-stu-id="98041-112">Removed `Managed` Parameter from `New-AzAvailabilitySet` and `Update-AzAvailabilitySet` cmdlets in favor of using ```Sku = Aligned```</span></span>

  #### <a name="before"></a><span data-ttu-id="98041-113">Före</span><span class="sxs-lookup"><span data-stu-id="98041-113">Before</span></span>

  ```powershell
  Update-AzAvailabilitySet -Managed
  ```

  #### <a name="after"></a><span data-ttu-id="98041-114">Efter</span><span class="sxs-lookup"><span data-stu-id="98041-114">After</span></span>

  ```powershell
  Update-AzAvailabilitySet -Sku Aligned
  ```
- <span data-ttu-id="98041-115">Tog för konsekvens bort parametern `Image` från parameteruppsättningarna ByName och ByResourceId i `Update-AzImage`</span><span class="sxs-lookup"><span data-stu-id="98041-115">For consistency, removed `Image` parameter from 'ByName' and 'ByResourceId' parameter sets in `Update-AzImage`</span></span> 
  
  #### <a name="before"></a><span data-ttu-id="98041-116">Före</span><span class="sxs-lookup"><span data-stu-id="98041-116">Before</span></span>

  <span data-ttu-id="98041-117">Obs! Nedanstående kod fungerar men det inskickade ImageName-namnet används inte. Det ger ingen funktionell påverkan att ta bort den här parametern.</span><span class="sxs-lookup"><span data-stu-id="98041-117">Note that the below code is functional, but the passed-in ImageName is not used, so removing this parameter has no functional impact.</span></span>

  ```powershell
  Update-AzImage -ResourceGroupName $Rg -ImageName $Name -Image $Image -Tag $tags

  Update-AzImage -ResourceId $Id -Image $Image -Tag $tags
  ```

  #### <a name="after"></a><span data-ttu-id="98041-118">Efter</span><span class="sxs-lookup"><span data-stu-id="98041-118">After</span></span>

  ```powershell
  Update-AzImage -ResourceGroupName $Rg -ImageName $Name -Tag $tags

  Update-AzImage -ResourceId $Id -Tag $tags
  ```

- <span data-ttu-id="98041-119">Tog för konsekvens bort parametern `Name` från parameteruppsättningarna ByObject and ByResourceId i `Restart-AzVM`</span><span class="sxs-lookup"><span data-stu-id="98041-119">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Restart-AzVM`</span></span>
  
  #### <a name="before"></a><span data-ttu-id="98041-120">Före</span><span class="sxs-lookup"><span data-stu-id="98041-120">Before</span></span>

  <span data-ttu-id="98041-121">Obs! Nedanstående kod fungerar men det inskickade namnet används inte. Det ger ingen funktionell påverkan att ta bort den här parametern.</span><span class="sxs-lookup"><span data-stu-id="98041-121">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>
  ```powershell
  Restart-AzVM -InputObject $VM -Name $Name 

  Restart-AzVM -ResourceId $Id -Name $Name
  ```

  #### <a name="after"></a><span data-ttu-id="98041-122">Efter</span><span class="sxs-lookup"><span data-stu-id="98041-122">After</span></span>

  ```powershell
  Restart-AzVM -InputObject $VM

  Restart-AzVM -ResourceId $Id
  ```

- <span data-ttu-id="98041-123">Tog för konsekvens bort parametern `Name` från parameteruppsättningarna ByObject and ByResourceId i `Start-AzVM`</span><span class="sxs-lookup"><span data-stu-id="98041-123">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Start-AzVM`</span></span>
  
  #### <a name="before"></a><span data-ttu-id="98041-124">Före</span><span class="sxs-lookup"><span data-stu-id="98041-124">Before</span></span>

  <span data-ttu-id="98041-125">Obs! Nedanstående kod fungerar men det inskickade namnet används inte. Det ger ingen funktionell påverkan att ta bort den här parametern.</span><span class="sxs-lookup"><span data-stu-id="98041-125">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>

  ```powershell
  Start-AzVM -InputObject $VM -Name $Name 

  Start-AzVM -ResourceId $Id -Name $Name
  ```

  #### <a name="after"></a><span data-ttu-id="98041-126">Efter</span><span class="sxs-lookup"><span data-stu-id="98041-126">After</span></span>

  ```powershell
  Start-AzVM -InputObject $VM

  Start-AzVM -ResourceId $Id
  ```

- <span data-ttu-id="98041-127">Tog för konsekvens bort parametern `Name` från parameteruppsättningarna ByObject and ByResourceId i `Stop-AzVM`</span><span class="sxs-lookup"><span data-stu-id="98041-127">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Stop-AzVM`</span></span>
  
  #### <a name="before"></a><span data-ttu-id="98041-128">Före</span><span class="sxs-lookup"><span data-stu-id="98041-128">Before</span></span>

  <span data-ttu-id="98041-129">Obs! Nedanstående kod fungerar men det inskickade namnet används inte. Det ger ingen funktionell påverkan att ta bort den här parametern.</span><span class="sxs-lookup"><span data-stu-id="98041-129">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>

  ```powershell
  Stop-AzVM -InputObject $VM -Name $Name 

  Stop-AzVM -ResourceId $Id -Name $Name
  ```

  #### <a name="after"></a><span data-ttu-id="98041-130">Efter</span><span class="sxs-lookup"><span data-stu-id="98041-130">After</span></span>

  ```powershell
  Stop-AzVM -InputObject $VM

  Stop-AzVM -ResourceId $Id
  ```

- <span data-ttu-id="98041-131">Tog för konsekvens bort parametern `Name` från parameteruppsättningarna ByObject and ByResourceId i `Remove-AzVM`</span><span class="sxs-lookup"><span data-stu-id="98041-131">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Remove-AzVM`</span></span>
  
  #### <a name="before"></a><span data-ttu-id="98041-132">Före</span><span class="sxs-lookup"><span data-stu-id="98041-132">Before</span></span>

  <span data-ttu-id="98041-133">Obs! Nedanstående kod fungerar men det inskickade namnet används inte. Det ger ingen funktionell påverkan att ta bort den här parametern.</span><span class="sxs-lookup"><span data-stu-id="98041-133">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>

  ```powershell
  Remove-AzVM -InputObject $VM -Name $Name

  Remove-AzVM -ResourceId $Id -Name $Name 
  ```

  #### <a name="after"></a><span data-ttu-id="98041-134">Efter</span><span class="sxs-lookup"><span data-stu-id="98041-134">After</span></span>

  ```powershell
  Remove-AzVM -InputObject $VM 

  Remove-AzVM -ResourceId $Id 
  ```

- <span data-ttu-id="98041-135">Tog för konsekvens bort parametern `Name` från parameteruppsättningarna ByObject and ByResourceId i `Set-AzVM`</span><span class="sxs-lookup"><span data-stu-id="98041-135">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Set-AzVM`</span></span>
  
  #### <a name="before"></a><span data-ttu-id="98041-136">Före</span><span class="sxs-lookup"><span data-stu-id="98041-136">Before</span></span>

  <span data-ttu-id="98041-137">Obs! Nedanstående kod fungerar men det inskickade namnet används inte. Det ger ingen funktionell påverkan att ta bort den här parametern.</span><span class="sxs-lookup"><span data-stu-id="98041-137">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>

  ```powershell
  Set-AzVM -InputObject $VM -Name $Name ...

  Set-AzVM -ResourceId $Id -Name $Name ...
  ```

  #### <a name="after"></a><span data-ttu-id="98041-138">Efter</span><span class="sxs-lookup"><span data-stu-id="98041-138">After</span></span>

  ```powershell
  Set-AzVM -InputObject $VM ...

  Set-AzVM -ResourceId $Id ...
  ```

- <span data-ttu-id="98041-139">Tog för konsekvens bort parametern `Name` från parameteruppsättningarna ByObject and ByResourceId i `Save-AzVMImage`</span><span class="sxs-lookup"><span data-stu-id="98041-139">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Save-AzVMImage`</span></span> 
  
  #### <a name="before"></a><span data-ttu-id="98041-140">Före</span><span class="sxs-lookup"><span data-stu-id="98041-140">Before</span></span>
  <span data-ttu-id="98041-141">Obs! Nedanstående kod fungerar men det inskickade namnet används inte. Det ger ingen funktionell påverkan att ta bort den här parametern.</span><span class="sxs-lookup"><span data-stu-id="98041-141">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>
  ```powershell
  Save-AzVMImage -InputObject $VM -Name $Name ...

  Save-AzVMImage -ResourceId $Id -Name $Name ...
  ```
  #### <a name="after"></a><span data-ttu-id="98041-142">Efter</span><span class="sxs-lookup"><span data-stu-id="98041-142">After</span></span>
  ```powershell
  Save-AzVMImage -InputObject $VM ...

  Save-AzVMImage -ResourceId $Id ...
  ```

- <span data-ttu-id="98041-143">Lade till ProtectionPolicy-egenskap för att kapsla in egenskapen `ProtectFromScaleIn` i `PSVirtualMachineScaleSetVM`</span><span class="sxs-lookup"><span data-stu-id="98041-143">Added ProtectionPolicy property to encapsulate `ProtectFromScaleIn` property in `PSVirtualMachineScaleSetVM`</span></span>

  #### <a name="before"></a><span data-ttu-id="98041-144">Före</span><span class="sxs-lookup"><span data-stu-id="98041-144">Before</span></span>

  ```powershell
  $vmss = Get-AzVMssVM ...
  $vmss.ProtectFromScaleIn = $true

  $vmss = Update-AzVMssVM ...
  $vmss.ProtectFromScaleIn = $true

  $vmss = Remove-AzVMssVMDataDisk ...
  $vmss.ProtectFromScaleIn = $true
  ```

  #### <a name="after"></a><span data-ttu-id="98041-145">Efter</span><span class="sxs-lookup"><span data-stu-id="98041-145">After</span></span>

  ```powershell
  $vmss = Get-AzVMssVM ...
  $vmss.ProtectionPolicy.ProtectFromScaleIn = $true

  $vmss = Update-AzVMssVM ...
  $vmss.ProtectionPolicy.ProtectFromScaleIn = $true

  $vmss = Remove-AzVMssVMDataDisk ...
  $vmss.ProtectionPolicy.ProtectFromScaleIn = $true

  ```

- <span data-ttu-id="98041-146">Lade till egenskapen ```EncryptionSettingsCollection``` för att kapsla in egenskapen `EncryptionSettings` i `PSDisk`</span><span class="sxs-lookup"><span data-stu-id="98041-146">Added ```EncryptionSettingsCollection``` Property to enclose `EncryptionSettings` property in `PSDisk`</span></span>

  #### <a name="before"></a><span data-ttu-id="98041-147">Före</span><span class="sxs-lookup"><span data-stu-id="98041-147">Before</span></span>

  ```powershell
  $disk = New-AzDisk ... | Set-AzDiskDiskEncrytionKey ...
  $disk.EncryptionSettings

  $disk = New-AzDisk ... | Set-AzDiskKeyEncrytionKey ...
  $disk.EncryptionSettings

  $update = New-AzDiskUpdateConfig | Set-AzDiskUpdateDiskEncryptionKey ...
  $update.EncryptionSettings

  $update = New-AzDiskUpdateConfig | Set-AzDiskUpdateKeyEncryptionKey ...
  $update.EncryptionSettings
  ```

  #### <a name="after"></a><span data-ttu-id="98041-148">Efter</span><span class="sxs-lookup"><span data-stu-id="98041-148">After</span></span>

  ```powershell
  $disk = New-AzDisk ... | Set-AzDiskDiskEncrytionKey ...
  $disk.EncryptionSettingsCollection.EncryptionSettings

  $disk = New-AzDisk ... | Set-AzDiskKeyEncrytionKey ...
  $disk.EncryptionSettingsCollection.EncryptionSettings

  $update = New-AzDiskUpdateConfig | Set-AzDiskUpdateDiskEncryptionKey ...
  $update.EncryptionSettingsCollection.EncryptionSettings

  $update = New-AzDiskUpdateConfig | Set-AzDiskUpdateKeyEncryptionKey ...
  $update.EncryptionSettingsCollection.EncryptionSettings
  ```

- <span data-ttu-id="98041-149">Lade till egenskapen ```EncryptionSettingsCollection``` för att kapsla in egenskapen `EncryptionSettings` i `PSSnapshot`</span><span class="sxs-lookup"><span data-stu-id="98041-149">Added ```EncryptionSettingsCollection``` Property to enclose `EncryptionSettings` property in `PSSnapshot`</span></span>

  #### <a name="before"></a><span data-ttu-id="98041-150">Före</span><span class="sxs-lookup"><span data-stu-id="98041-150">Before</span></span>

  ```powershell
  $snap = New-AzSnapshotConfig ... | Set-AzSnapshotDiskEncryptionKey ...
  $snap.EncryptionSettings

  $snap = New-AzSnapshotConfig ... | Set-AzSnapshotKeyEncryptionKey ...
  $snap.EncryptionSettings

  $update = New-AzSnapshotUpdateConfig ... | Set-AzSnapshotUpdateDiskEncryptionKey ...
  $update.EncryptionSettings

  $update = New-AzSnapshotUpdateConfig ... | Set-AzSnapshotUpdateKeyEncryptionKey ...
  $update.EncryptionSettings
  ```

  #### <a name="after"></a><span data-ttu-id="98041-151">Efter</span><span class="sxs-lookup"><span data-stu-id="98041-151">After</span></span>

  ```powershell
  $snap = New-AzSnapshotConfig ... | Set-AzSnapshotDiskEncryptionKey ...
  $snap.EncryptionSettingsCollection.EncryptionSettings

  $snap = New-AzSnapshotConfig ... | Set-AzSnapshotKeyEncryptionKey ...
  $snap.EncryptionSettingsCollection.EncryptionSettings

  $update = New-AzSnapshotUpdateConfig ... | Set-AzSnapshotUpdateDiskEncryptionKey ...
  $update.EncryptionSettingsCollection.EncryptionSettings

  $update = New-AzSnapshotUpdateConfig ... | Set-AzSnapshotUpdateKeyEncryptionKey ...
  $update.EncryptionSettingsCollection.EncryptionSettings
  ```

- <span data-ttu-id="98041-152">Tog bort egenskapen `VirtualMachineProfile` från `PSVirtualMachineScaleSet`</span><span class="sxs-lookup"><span data-stu-id="98041-152">Removed `VirtualMachineProfile` property from `PSVirtualMachineScaleSet`</span></span>

  #### <a name="before"></a><span data-ttu-id="98041-153">Före</span><span class="sxs-lookup"><span data-stu-id="98041-153">Before</span></span>

  ```powershell
  $vmss = New-AzVMSSConfig ...
  $vmss.VirtualMachineProfile.AdditionalCapabilities.UltraSSDEnabled = $true
  ```

  #### <a name="after"></a><span data-ttu-id="98041-154">Efter</span><span class="sxs-lookup"><span data-stu-id="98041-154">After</span></span>

  ```powershell
  $vmss = New-AzVMSSConfig ...
  $vmss.AdditionalCapabilities.UltraSSDEnabled = $true
  ```

- <span data-ttu-id="98041-155">Cmdleten `Set-AzVMBootDiagnostic` tog bort alias till `Set-AzVMBootDiagnostics`</span><span class="sxs-lookup"><span data-stu-id="98041-155">Cmdlet `Set-AzVMBootDiagnostic` removed alias to `Set-AzVMBootDiagnostics`</span></span>

  #### <a name="before"></a><span data-ttu-id="98041-156">Före</span><span class="sxs-lookup"><span data-stu-id="98041-156">Before</span></span>

  <span data-ttu-id="98041-157">Använda inaktuellt alias</span><span class="sxs-lookup"><span data-stu-id="98041-157">Using deprecated alias</span></span>

  ```powershell
  Set-AzVMBootDiagnostics
  ```

  #### <a name="after"></a><span data-ttu-id="98041-158">Efter</span><span class="sxs-lookup"><span data-stu-id="98041-158">After</span></span>

  ```powershell
  Set-AzVMBootDIagnostic
  ```

- <span data-ttu-id="98041-159">Cmdleten `Export-AzLogAnalyticThrottledRequest` tog bort alias till `Export-AzLogAnalyticThrottledRequests`</span><span class="sxs-lookup"><span data-stu-id="98041-159">Cmdlet `Export-AzLogAnalyticThrottledRequest` removed alias to `Export-AzLogAnalyticThrottledRequests`</span></span>

  #### <a name="before"></a><span data-ttu-id="98041-160">Före</span><span class="sxs-lookup"><span data-stu-id="98041-160">Before</span></span>

  <span data-ttu-id="98041-161">Använda inaktuellt alias</span><span class="sxs-lookup"><span data-stu-id="98041-161">Using deprectaed alias</span></span>

  ```powershell
  Export-AzLogAnalyticThrottledRequests
  ```

  #### <a name="after"></a><span data-ttu-id="98041-162">Efter</span><span class="sxs-lookup"><span data-stu-id="98041-162">After</span></span>

  ```powershell
  Export-AzLogAnalyticThrottledRequest
  ```

### <a name="azhdinsight"></a><span data-ttu-id="98041-163">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="98041-163">Az.HDInsight</span></span>

- <span data-ttu-id="98041-164">Tog bort cmdletarna `Grant-AzHDInsightHttpServicesAccess` och `Revoke-AzHDInsightHttpServicesAccess`.</span><span class="sxs-lookup"><span data-stu-id="98041-164">Removed the `Grant-AzHDInsightHttpServicesAccess` and `Revoke-AzHDInsightHttpServicesAccess` cmdlets.</span></span> <span data-ttu-id="98041-165">De här behövs inte längre eftersom HTTP-åtkomst alltid är aktiverat i alla HDInsight-kluster.</span><span class="sxs-lookup"><span data-stu-id="98041-165">These are no longer necessary because HTTP access is always enabled on all HDInsight clusters.</span></span>
- <span data-ttu-id="98041-166">Lade till ny `Set-AzHDInsightGatewayCredential`-cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98041-166">Added a new `Set-AzHDInsightGatewayCredential`  cmdlet.</span></span> <span data-ttu-id="98041-167">Med den här cmdleten ändrar du HTTP-användarnamnet och lösenordet för nätverksgateway (ersätter `Grant-AzHDInsightHttpServicesAccess`).</span><span class="sxs-lookup"><span data-stu-id="98041-167">Use this cmdlet to change the gateway HTTP username and password (replaces `Grant-AzHDInsightHttpServicesAccess`).</span></span>
- <span data-ttu-id="98041-168">Uppdaterade cmdleten `Get-AzHDInsightJobOutput` för att ge stöd för detaljerad rollbaserad åtkomst till lagringsnyckeln.</span><span class="sxs-lookup"><span data-stu-id="98041-168">Updated the `Get-AzHDInsightJobOutput` cmdlet to support granular role-based access to the storage key.</span></span>
    - <span data-ttu-id="98041-169">Användare med rollerna	HDInsight-klusteroperator, Deltagare och Ägare påverkas inte.</span><span class="sxs-lookup"><span data-stu-id="98041-169">Users with HDInsight Cluster Operator, Contributor, or Owner roles will not be affected.</span></span>
    - <span data-ttu-id="98041-170">Användare med skrivskyddad åtkomst behöver ange parametern `DefaultStorageAccountKey` uttryckligen.</span><span class="sxs-lookup"><span data-stu-id="98041-170">Users with only the Reader role will need to specify `DefaultStorageAccountKey` parameter explicitly.</span></span>

<span data-ttu-id="98041-171">Mer information om de här ändringarna av den rollbaserade åtkomsten finns i [aka.ms/hdi-config-update](http://aka.ms/hdi-config-update)</span><span class="sxs-lookup"><span data-stu-id="98041-171">For more information about these role-based access changes, see [aka.ms/hdi-config-update](http://aka.ms/hdi-config-update)</span></span>

  #### <a name="before"></a><span data-ttu-id="98041-172">Före</span><span class="sxs-lookup"><span data-stu-id="98041-172">Before</span></span>

  ```powershell
  Grant-AzHDInsightHttpServicesAccess -ClusterName $cluster -HttpCredential $credential
  ```

  #### <a name="after"></a><span data-ttu-id="98041-173">Efter</span><span class="sxs-lookup"><span data-stu-id="98041-173">After</span></span>

  ```powershell
  Set-AzHDInsightGatewayCredential -ClusterName $cluster -HttpCredential $credential
  ```

###  <a name="users-with-only-reader-role-for-cmdlet-get-azhdinsightjoboutput"></a><span data-ttu-id="98041-174">Användare med skrivskyddad roll för cmdlet Get-AzHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="98041-174">Users with only Reader role for cmdlet Get-AzHDInsightJobOutput</span></span>

  ####  <a name="before"></a><span data-ttu-id="98041-175">Före</span><span class="sxs-lookup"><span data-stu-id="98041-175">Before</span></span>

  ```powershell
  Get-AzHDInsightJobOutput  -ClusterName $clusterName -JobId $jobId
  ```

  #### <a name="after"></a><span data-ttu-id="98041-176">Efter</span><span class="sxs-lookup"><span data-stu-id="98041-176">After</span></span>

  ```powershell
  Get-AzHDInsightJobOutput  -ClusterName $clusterName -JobId $jobId -DefaultStorageAccountKey $storageAccountKey
  ```

### <a name="azstorage"></a><span data-ttu-id="98041-177">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="98041-177">Az.Storage</span></span>

- <span data-ttu-id="98041-178">Namnområden för typer returnerade från cmdletarna Blob, Queue och File har ändrat sin namnrymd från `Microsoft.WindowsAzure.Storage` till `Microsoft.Azure.Storage`.</span><span class="sxs-lookup"><span data-stu-id="98041-178">Namespaces for types returned from Blob, Queue, and File cmdlets have changed their namespace from `Microsoft.WindowsAzure.Storage` to `Microsoft.Azure.Storage`.</span></span>  <span data-ttu-id="98041-179">Det kan vara så att en ändring inte tekniskt sett är icke-bakåtkompatibel men att den kräver ändringar i koden som använder metoderna från arkivet .Net SDK för att kunna interagera med objekten som returneras från cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="98041-179">While this is not technically a breaking change according to the breaking change policy, it may require some changes in code that uses the methods from the Storage .Net SDK to interact with the objects returned from these cmdlets.</span></span>

  #### <a name="example-1--add-a-message-to-a-queue-change-cloudqueuemessage-object-namespace"></a><span data-ttu-id="98041-180">Exempel 1:  Lägg till ett meddelande i en kö (ändra objektnamnområdet för CloudQueueMessage)</span><span class="sxs-lookup"><span data-stu-id="98041-180">Example 1:  Add a message to a Queue (change CloudQueueMessage object namespace)</span></span>

  <span data-ttu-id="98041-181">Innan:</span><span class="sxs-lookup"><span data-stu-id="98041-181">Before:</span></span> 

  ```powershell
  $queue = Get-AzStorageQueue –Name $queueName –Context $ctx
  $queueMessage = New-Object -TypeName "Microsoft.WindowsAzure.Storage.Queue.CloudQueueMessage,$($queue.CloudQueue.GetType().Assembly.FullName)" -ArgumentList "This is message 1"
  $queue.CloudQueue.AddMessageAsync($QueueMessage)
  ```

  <span data-ttu-id="98041-182">Efter:</span><span class="sxs-lookup"><span data-stu-id="98041-182">After:</span></span>

  ```powershell
  $queue = Get-AzStorageQueue –Name $queueName –Context $ctx
  $queueMessage = New-Object -TypeName "Microsoft.Azure.Storage.Queue.CloudQueueMessage,$($queue.CloudQueue.GetType().Assembly.FullName)"  -ArgumentList "This is message 1"
  $queue.CloudQueue.AddMessageAsync($QueueMessage)
  ```

  #### <a name="example-2--fetch-blobfile-attributes-with-accesscondition-change-accesscondition-object-namespace"></a><span data-ttu-id="98041-183">Exempel 2:  Hämta blob-/filattribut med AccessCondition (ändra AccessCondition-objektnamnområdet)</span><span class="sxs-lookup"><span data-stu-id="98041-183">Example 2:  Fetch Blob/File Attributes with AccessCondition (change AccessCondition object namespace)</span></span>

  <span data-ttu-id="98041-184">Innan:</span><span class="sxs-lookup"><span data-stu-id="98041-184">Before:</span></span> 

  ```powershell
  $accessCondition= New-Object Microsoft.WindowsAzure.Storage.AccessCondition

  $blob = Get-AzureStorageBlob -Container $containerName -Blob $blobName
  $blob.ICloudBlob.FetchAttributes($accessCondition)

  $file = Get-AzureStorageFile -ShareName $shareName -Path $filepath
  $file.FetchAttributes($accessCondition)
  ```

  <span data-ttu-id="98041-185">Efter:</span><span class="sxs-lookup"><span data-stu-id="98041-185">After:</span></span>

  ```powershell
  $accessCondition= New-Object Microsoft.Azure.Storage.AccessCondition

  $blob = Get-AzureStorageBlob -Container $containerName -Blob $blobName
  $blob.ICloudBlob.FetchAttributes($accessCondition)

  $file = Get-AzureStorageFile -ShareName $shareName -Path $filepath
  $file.FetchAttributes($accessCondition)
  ```

- <span data-ttu-id="98041-186">Det här är tekniskt sett inte en icke-bakåtkompatibel ändring, men du ser skillnader i utdata i egenskapen Sku.Name för de lagringskonton som returneras från `New/Get/Set-AzStorageAccount` enligt följande.</span><span class="sxs-lookup"><span data-stu-id="98041-186">While not technically a breaking change, you will notice output differences in the Sku.Name property of Storage Accounts returned from  `New/Get/Set-AzStorageAccount` changes are as follows.</span></span> <span data-ttu-id="98041-187">(Efter ändringen justeras utgående och inkommande SkuName.)</span><span class="sxs-lookup"><span data-stu-id="98041-187">(After the change, output and input SkuName are aligned.)</span></span>
  - <span data-ttu-id="98041-188">StandardLRS -> Standard_LRS;</span><span class="sxs-lookup"><span data-stu-id="98041-188">"StandardLRS" -> "Standard_LRS";</span></span>
  - <span data-ttu-id="98041-189">StandardGRS -> Standard_GRS;</span><span class="sxs-lookup"><span data-stu-id="98041-189">"StandardGRS" -> "Standard_GRS";</span></span>
  - <span data-ttu-id="98041-190">StandardRAGRS -> Standard_RAGRS;</span><span class="sxs-lookup"><span data-stu-id="98041-190">"StandardRAGRS" -> "Standard_RAGRS";</span></span>
  - <span data-ttu-id="98041-191">StandardZRS -> Standard_ZRS;</span><span class="sxs-lookup"><span data-stu-id="98041-191">"StandardZRS" -> "Standard_ZRS";</span></span>
  - <span data-ttu-id="98041-192">PremiumLRS -> Premium_LRS;</span><span class="sxs-lookup"><span data-stu-id="98041-192">"PremiumLRS" -> "Premium_LRS";</span></span>

- <span data-ttu-id="98041-193">Standardbeteendet för tjänsten när du skapar ett lagringskonto utan att specificera att värdet för Kind har ändrats.</span><span class="sxs-lookup"><span data-stu-id="98041-193">The default service behavior when creating a storage account withous specifying a Kind has changed.</span></span>  <span data-ttu-id="98041-194">När ett lagringskonto i tidigare versioner skapades utan angivet värde för `Kind` användes lagringskontotypen `Storage`. I den nya versionen är `StorageV2` standardvärdet för `Kind`.</span><span class="sxs-lookup"><span data-stu-id="98041-194">In previous versions, when a storage account was created with no `Kind` specified, the Storage account Kind of `Storage` was used, in the new version `StorageV2` is the default `Kind` value.</span></span> <span data-ttu-id="98041-195">Om du behöver skapa ett V1 Storage-konto med Kind-värde Storage lägger du till parametern -Kind Storage</span><span class="sxs-lookup"><span data-stu-id="98041-195">If you need to create a V1 Storage account with Kind 'Storage', add parameter '-Kind Storage'</span></span>

  #### <a name="example--create-a-storage-account-default-kind-change"></a><span data-ttu-id="98041-196">Exempel: Skapa ett lagringskonto (ändring av standardvärde för Kind)</span><span class="sxs-lookup"><span data-stu-id="98041-196">Example : Create a storage Account (Default Kind change)</span></span>  

  <span data-ttu-id="98041-197">Innan:</span><span class="sxs-lookup"><span data-stu-id="98041-197">Before:</span></span>

  ```powershell
  PS c:\> New-AzStorageAccount -ResourceGroupName groupname -Name accountname -SkuName Standard_LRS -Location "westus"

  StorageAccountName ResourceGroupName Location SkuName     Kind      AccessTier CreationTime          ProvisioningState EnableHttpsTrafficOnly
  ------------------ ----------------- -------- -------     ----      ---------- ------------          ----------------- ----------------------
  accountname        groupname         westus   StandardLRS Storage   Hot        4/17/2018 10:34:32 AM Succeeded         False
  ```

  <span data-ttu-id="98041-198">Efter:</span><span class="sxs-lookup"><span data-stu-id="98041-198">After:</span></span>

  ```powershell
  PS c:\> New-AzStorageAccount -ResourceGroupName groupname -Name accountname -SkuName Standard_LRS -Location "westus"

  StorageAccountName ResourceGroupName Location SkuName      Kind      AccessTier CreationTime          ProvisioningState EnableHttpsTrafficOnly
  ------------------ ----------------- -------- -------      ----      ----------  ------------          ----------------- ----------------------
  accountname        groupname         westus   Standard_LRS StorageV2 Hot        4/17/2018 10:34:32 AM Succeeded         False
  ```
