---
title: Migreringsguide för Az 5.0.0
description: Den här migreringsguiden innehåller en lista över icke-bakåtkompatibla ändringar som gjorts i Az version 5.0.0 av Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/27/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 3a82e738bcb652ddc38886f7064e7373b5fb8cc1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92754129"
---
# <a name="migration-guide-for-az-500"></a><span data-ttu-id="bf05c-103">Migreringsguide för Az 5.0.0</span><span class="sxs-lookup"><span data-stu-id="bf05c-103">Migration Guide for Az 5.0.0</span></span>

<span data-ttu-id="bf05c-104">I det här dokumentet beskrivs ändringarna mellan Az-versionerna 4.0.0 och 5.0.0.</span><span class="sxs-lookup"><span data-stu-id="bf05c-104">This document describes the changes between the 4.0.0 and 5.0.0 versions of Az.</span></span>

- [<span data-ttu-id="bf05c-105">Migreringsguide för Az 5.0.0</span><span class="sxs-lookup"><span data-stu-id="bf05c-105">Migration Guide for Az 5.0.0</span></span>](#migration-guide-for-az-500)
  - [<span data-ttu-id="bf05c-106">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="bf05c-106">Az.Aks</span></span>](#azaks)
    - [<span data-ttu-id="bf05c-107">New-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="bf05c-107">New-AzAksCluster</span></span>](#new-azakscluster)
    - [<span data-ttu-id="bf05c-108">Set-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="bf05c-108">Set-AzAksCluster</span></span>](#set-azakscluster)
  - [<span data-ttu-id="bf05c-109">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="bf05c-109">Az.ContainerRegistry</span></span>](#azcontainerregistry)
    - [<span data-ttu-id="bf05c-110">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="bf05c-110">New-AzContainerRegistry</span></span>](#new-azcontainerregistry)
  - [<span data-ttu-id="bf05c-111">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="bf05c-111">Az.Functions</span></span>](#azfunctions)
    - [<span data-ttu-id="bf05c-112">Get-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="bf05c-112">Get-AzFunctionApp</span></span>](#get-azfunctionapp)
    - [<span data-ttu-id="bf05c-113">New-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="bf05c-113">New-AzFunctionApp</span></span>](#new-azfunctionapp)
  - [<span data-ttu-id="bf05c-114">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="bf05c-114">Az.KeyVault</span></span>](#azkeyvault)
    - [<span data-ttu-id="bf05c-115">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="bf05c-115">New-AzKeyVault</span></span>](#new-azkeyvault)
    - [<span data-ttu-id="bf05c-116">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="bf05c-116">Update-AzKeyVault</span></span>](#update-azkeyvault)
    - [<span data-ttu-id="bf05c-117">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="bf05c-117">Get-AzKeyVaultSecret</span></span>](#get-azkeyvaultsecret)
  - [<span data-ttu-id="bf05c-118">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="bf05c-118">Az.ManagedServices</span></span>](#azmanagedservices)
    - [<span data-ttu-id="bf05c-119">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="bf05c-119">Get-AzManagedServicesDefinition</span></span>](#get-azmanagedservicesdefinition)
    - [<span data-ttu-id="bf05c-120">New-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="bf05c-120">New-AzManagedServicesAssignment</span></span>](#new-azmanagedservicesassignment)
    - [<span data-ttu-id="bf05c-121">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="bf05c-121">Remove-AzManagedServicesAssignment</span></span>](#remove-azmanagedservicesassignment)
    - [<span data-ttu-id="bf05c-122">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="bf05c-122">Remove-AzManagedServicesDefinition</span></span>](#remove-azmanagedservicesdefinition)
  - [<span data-ttu-id="bf05c-123">Az.ResourceManager</span><span class="sxs-lookup"><span data-stu-id="bf05c-123">Az.ResourceManager</span></span>](#azresourcemanager)
    - [<span data-ttu-id="bf05c-124">Get-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="bf05c-124">Get-AzManagementGroupDeployment</span></span>](#get-azmanagementgroupdeployment)
    - [<span data-ttu-id="bf05c-125">Get-AzManagementGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="bf05c-125">Get-AzManagementGroupDeploymentOperation</span></span>](#get-azmanagementgroupdeploymentoperation)
    - [<span data-ttu-id="bf05c-126">Get-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="bf05c-126">Get-AzDeployment</span></span>](#get-azdeployment)
    - [<span data-ttu-id="bf05c-127">Get-AzDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="bf05c-127">Get-AzDeploymentOperation</span></span>](#get-azdeploymentoperation)
    - [<span data-ttu-id="bf05c-128">Get-AzDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="bf05c-128">Get-AzDeploymentWhatIfResult</span></span>](#get-azdeploymentwhatifresult)
    - [<span data-ttu-id="bf05c-129">Get-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="bf05c-129">Get-AzTenantDeployment</span></span>](#get-aztenantdeployment)
    - [<span data-ttu-id="bf05c-130">Get-AzTenantDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="bf05c-130">Get-AzTenantDeploymentOperation</span></span>](#get-aztenantdeploymentoperation)
    - [<span data-ttu-id="bf05c-131">New-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="bf05c-131">New-AzManagementGroupDeployment</span></span>](#new-azmanagementgroupdeployment)
    - [<span data-ttu-id="bf05c-132">New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="bf05c-132">New-AzDeployment</span></span>](#new-azdeployment)
    - [<span data-ttu-id="bf05c-133">New-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="bf05c-133">New-AzTenantDeployment</span></span>](#new-aztenantdeployment)
    - [<span data-ttu-id="bf05c-134">Remove-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="bf05c-134">Remove-AzManagementGroupDeployment</span></span>](#remove-azmanagementgroupdeployment)
    - [<span data-ttu-id="bf05c-135">Remove-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="bf05c-135">Remove-AzDeployment</span></span>](#remove-azdeployment)
    - [<span data-ttu-id="bf05c-136">Remove-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="bf05c-136">Remove-AzTenantDeployment</span></span>](#remove-aztenantdeployment)
    - [<span data-ttu-id="bf05c-137">Save-AzManagementGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="bf05c-137">Save-AzManagementGroupDeploymentTemplate</span></span>](#save-azmanagementgroupdeploymenttemplate)
    - [<span data-ttu-id="bf05c-138">Save-AzDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="bf05c-138">Save-AzDeploymentTemplate</span></span>](#save-azdeploymenttemplate)
    - [<span data-ttu-id="bf05c-139">Save-AzTenantDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="bf05c-139">Save-AzTenantDeploymentTemplate</span></span>](#save-aztenantdeploymenttemplate)
    - [<span data-ttu-id="bf05c-140">Stop-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="bf05c-140">Stop-AzManagementGroupDeployment</span></span>](#stop-azmanagementgroupdeployment)
    - [<span data-ttu-id="bf05c-141">Stop-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="bf05c-141">Stop-AzDeployment</span></span>](#stop-azdeployment)
    - [<span data-ttu-id="bf05c-142">Stop-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="bf05c-142">Stop-AzTenantDeployment</span></span>](#stop-aztenantdeployment)
    - [<span data-ttu-id="bf05c-143">Test-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="bf05c-143">Test-AzManagementGroupDeployment</span></span>](#test-azmanagementgroupdeployment)
    - [<span data-ttu-id="bf05c-144">Test-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="bf05c-144">Test-AzDeployment</span></span>](#test-azdeployment)
    - [<span data-ttu-id="bf05c-145">Test-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="bf05c-145">Test-AzTenantDeployment</span></span>](#test-aztenantdeployment)
    - [<span data-ttu-id="bf05c-146">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="bf05c-146">Get-AzResourceGroupDeployment</span></span>](#get-azresourcegroupdeployment)
    - [<span data-ttu-id="bf05c-147">Get-AzResourceGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="bf05c-147">Get-AzResourceGroupDeploymentOperation</span></span>](#get-azresourcegroupdeploymentoperation)
    - [<span data-ttu-id="bf05c-148">Get-AzResourceGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="bf05c-148">Get-AzResourceGroupDeploymentWhatIfResult</span></span>](#get-azresourcegroupdeploymentwhatifresult)
    - [<span data-ttu-id="bf05c-149">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="bf05c-149">New-AzResourceGroupDeployment</span></span>](#new-azresourcegroupdeployment)
    - [<span data-ttu-id="bf05c-150">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="bf05c-150">Remove-AzResourceGroupDeployment</span></span>](#remove-azresourcegroupdeployment)
    - [<span data-ttu-id="bf05c-151">Save-AzResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="bf05c-151">Save-AzResourceGroupDeploymentTemplate</span></span>](#save-azresourcegroupdeploymenttemplate)
    - [<span data-ttu-id="bf05c-152">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="bf05c-152">Stop-AzResourceGroupDeployment</span></span>](#stop-azresourcegroupdeployment)
    - [<span data-ttu-id="bf05c-153">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="bf05c-153">Test-AzResourceGroupDeployment</span></span>](#test-azresourcegroupdeployment)
    - [<span data-ttu-id="bf05c-154">Get-AzManagementGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="bf05c-154">Get-AzManagementGroupDeploymentWhatIfResult</span></span>](#get-azmanagementgroupdeploymentwhatifresult)
    - [<span data-ttu-id="bf05c-155">Get-AzTenantDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="bf05c-155">Get-AzTenantDeploymentWhatIfResult</span></span>](#get-aztenantdeploymentwhatifresult)
  - [<span data-ttu-id="bf05c-156">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bf05c-156">Az.Sql</span></span>](#azsql)
    - [<span data-ttu-id="bf05c-157">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="bf05c-157">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](#set-azsqlserveractivedirectoryadministrator)
  - [<span data-ttu-id="bf05c-158">Az.Synapse</span><span class="sxs-lookup"><span data-stu-id="bf05c-158">Az.Synapse</span></span>](#azsynapse)
    - [<span data-ttu-id="bf05c-159">New-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="bf05c-159">New-AzSynapseSqlPool</span></span>](#new-azsynapsesqlpool)
    - [<span data-ttu-id="bf05c-160">Update-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="bf05c-160">Update-AzSynapseSqlPool</span></span>](#update-azsynapsesqlpool)
  - [<span data-ttu-id="bf05c-161">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bf05c-161">Az.Network</span></span>](#aznetwork)
    - [<span data-ttu-id="bf05c-162">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="bf05c-162">Approve-AzPrivateEndpointConnection</span></span>](#approve-azprivateendpointconnection)
    - [<span data-ttu-id="bf05c-163">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="bf05c-163">Deny-AzPrivateEndpointConnection</span></span>](#deny-azprivateendpointconnection)
    - [<span data-ttu-id="bf05c-164">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="bf05c-164">Get-AzPrivateEndpointConnection</span></span>](#get-azprivateendpointconnection)
    - [<span data-ttu-id="bf05c-165">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="bf05c-165">Remove-AzPrivateEndpointConnection</span></span>](#remove-azprivateendpointconnection)
    - [<span data-ttu-id="bf05c-166">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="bf05c-166">Set-AzPrivateEndpointConnection</span></span>](#set-azprivateendpointconnection)
    - [<span data-ttu-id="bf05c-167">New-AzNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="bf05c-167">New-AzNetworkWatcherConnectionMonitorEndpointObject</span></span>](#new-aznetworkwatcherconnectionmonitorendpointobject)

## <a name="azaks"></a><span data-ttu-id="bf05c-168">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="bf05c-168">Az.Aks</span></span>

### <a name="new-azakscluster"></a><span data-ttu-id="bf05c-169">New-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="bf05c-169">New-AzAksCluster</span></span>

- <span data-ttu-id="bf05c-170">Stöder inte längre parametern `NodeOsType` och inget alias hittades för det ursprungliga parameternamnet, som alltid kommer att vara `Linux`.</span><span class="sxs-lookup"><span data-stu-id="bf05c-170">No longer supports the parameter `NodeOsType` and no alias was found for the original parameter name, it will always be `Linux`.</span></span>
- <span data-ttu-id="bf05c-171">Stöder inte längre aliaset `ClientIdAndSecret` för parametern `ServicePrincipalIdAndSecret`.</span><span class="sxs-lookup"><span data-stu-id="bf05c-171">No longer supports the alias `ClientIdAndSecret` for parameter `ServicePrincipalIdAndSecret`.</span></span>
- <span data-ttu-id="bf05c-172">Standardvärdet för `NodeVmSetType` har ändrats från `AvailabilitySet` till `VirtualMachineScaleSets`.</span><span class="sxs-lookup"><span data-stu-id="bf05c-172">The default value of `NodeVmSetType` is changed from `AvailabilitySet` to `VirtualMachineScaleSets`.</span></span>
- <span data-ttu-id="bf05c-173">Standardvärdet för `NetworkPlugin` har ändrats från `none` till `azure`.</span><span class="sxs-lookup"><span data-stu-id="bf05c-173">The default value of `NetworkPlugin` is changed from `none` to `azure`.</span></span>

#### <a name="before"></a><span data-ttu-id="bf05c-174">Före</span><span class="sxs-lookup"><span data-stu-id="bf05c-174">Before</span></span>

```powershell
New-AzAksCluster -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeOsType Linux -ClientIdAndSecret xxx
```

#### <a name="after"></a><span data-ttu-id="bf05c-175">Efter</span><span class="sxs-lookup"><span data-stu-id="bf05c-175">After</span></span>

```powershell
New-AzAksCluster -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NodeVmSetType AvailabilitySet  -ServicePrincipalIdAndSecret xxx
```

### <a name="set-azakscluster"></a><span data-ttu-id="bf05c-176">Set-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="bf05c-176">Set-AzAksCluster</span></span>

<span data-ttu-id="bf05c-177">Stöder inte längre aliaset `ClientIdAndSecret` för parametern `ServicePrincipalIdAndSecret`.</span><span class="sxs-lookup"><span data-stu-id="bf05c-177">No longer supports the alias `ClientIdAndSecret` for parameter `ServicePrincipalIdAndSecret`.</span></span>

#### <a name="before"></a><span data-ttu-id="bf05c-178">Före</span><span class="sxs-lookup"><span data-stu-id="bf05c-178">Before</span></span>

```powershell
Get-AzAksCluster -ResourceGroupName xxx -Name xxx | Set-AzAksCluster -ClientIdAndSecret xxx
```

#### <a name="after"></a><span data-ttu-id="bf05c-179">Efter</span><span class="sxs-lookup"><span data-stu-id="bf05c-179">After</span></span>

```powershell
Get-AzAksCluster -ResourceGroupName xxx -Name xxx | Set-AzAksCluster -ServicePrincipalIdAndSecret xxx
```

## <a name="azcontainerregistry"></a><span data-ttu-id="bf05c-180">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="bf05c-180">Az.ContainerRegistry</span></span>

### <a name="new-azcontainerregistry"></a><span data-ttu-id="bf05c-181">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="bf05c-181">New-AzContainerRegistry</span></span>

<span data-ttu-id="bf05c-182">Stöder inte längre parametern `StorageAccountName` och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="bf05c-182">No longer supports the parameter `StorageAccountName` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="bf05c-183">Före</span><span class="sxs-lookup"><span data-stu-id="bf05c-183">Before</span></span>

```powershell
New-AzContainerRegistry -Name $name -ResourceGroupName $rg -Location $location -SKU Classic -StorageAccountName $storage
```

#### <a name="after"></a><span data-ttu-id="bf05c-184">Efter</span><span class="sxs-lookup"><span data-stu-id="bf05c-184">After</span></span>

<span data-ttu-id="bf05c-185">`Classic` är inaktuell och `StorageAccountName` har tagits bort eftersom den endast fungerar med klassiska Container Registry.</span><span class="sxs-lookup"><span data-stu-id="bf05c-185">`Classic` was deprecated and `StorageAccountName` was removed since it only works with Classic Container Registry.</span></span>

## <a name="azfunctions"></a><span data-ttu-id="bf05c-186">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="bf05c-186">Az.Functions</span></span>

### <a name="get-azfunctionapp"></a><span data-ttu-id="bf05c-187">Get-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="bf05c-187">Get-AzFunctionApp</span></span>

<span data-ttu-id="bf05c-188">Tog bort växelparametern `IncludeSlot` från alla förutom en parameteruppsättning av `Get-AzFunctionApp`.</span><span class="sxs-lookup"><span data-stu-id="bf05c-188">Removed `IncludeSlot` switch parameter from all but one parameter set of `Get-AzFunctionApp`.</span></span> <span data-ttu-id="bf05c-189">Cmdleten stöder nu hämtning av distributionsfack i resultaten när `-IncludeSlot` anges.</span><span class="sxs-lookup"><span data-stu-id="bf05c-189">The cmdlet now supports retrieving deployment slots in the results when `-IncludeSlot` is specified.</span></span>
<span data-ttu-id="bf05c-190">Den här funktionen fungerade inte i den tidigare cmdlet-versionen.</span><span class="sxs-lookup"><span data-stu-id="bf05c-190">This functionality was broken in the previous cmdlet version.</span></span> <span data-ttu-id="bf05c-191">Detta är dock åtgärdat nu.</span><span class="sxs-lookup"><span data-stu-id="bf05c-191">However, this is now fixed.</span></span>

### <a name="new-azfunctionapp"></a><span data-ttu-id="bf05c-192">New-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="bf05c-192">New-AzFunctionApp</span></span>

- <span data-ttu-id="bf05c-193">Korrigerade `-DisableApplicationInsights` i `New-AzFunctionApp` så att inga Application Insights-projekt skapas när det här alternativet har angetts.</span><span class="sxs-lookup"><span data-stu-id="bf05c-193">Fixed `-DisableApplicationInsights` in `New-AzFunctionApp` so that no application insights project is created when this option is specified.</span></span>
- <span data-ttu-id="bf05c-194">Tog bort stöd för att skapa PowerShell 6.2-funktionsappar eftersom PowerShell 6.2 är EOL.</span><span class="sxs-lookup"><span data-stu-id="bf05c-194">Removed support to create PowerShell 6.2 function apps since PowerShell 6.2 is EOL.</span></span> <span data-ttu-id="bf05c-195">Vi rekommenderar för närvarande att kunder skapar PowerShell 7.0-funktionsappar i stället.</span><span class="sxs-lookup"><span data-stu-id="bf05c-195">The current guidance for customers is to create PowerShell 7.0 function apps instead.</span></span>
- <span data-ttu-id="bf05c-196">Ändrade körningsversionen som är standard i Functions version 3 i Windows för PowerShell-funktionsppar från 6.2 till 7.0 när parametern `RuntimeVersion` inte har angetts.</span><span class="sxs-lookup"><span data-stu-id="bf05c-196">Changed the default runtime version in Functions version 3 on Windows for PowerShell function apps from 6.2 to 7.0 when the `RuntimeVersion` parameter is not specified.</span></span>
- <span data-ttu-id="bf05c-197">Ändrade körningsversionen som är standard i Functions version 3 i Windows och Linux för Node-funktionsppar från 10 till 12 när parametern `RuntimeVersion` inte har angetts.</span><span class="sxs-lookup"><span data-stu-id="bf05c-197">Changed the default runtime version in Functions version 3 on Windows and Linux for Node function apps from 10 to 12 when the `RuntimeVersion` parameter is not specified.</span></span> <span data-ttu-id="bf05c-198">Användare kan dock fortfarande skapa Node 10-funktionsappar genom att ange `-Runtime Node` och `-RuntimeVersion 10`.</span><span class="sxs-lookup"><span data-stu-id="bf05c-198">However, users can still create Node 10 function apps by specifying `-Runtime Node` and `-RuntimeVersion 10`.</span></span> <span data-ttu-id="bf05c-199">Ändrade körningsversionen som är standard i Functions version 3 i Linux för Python-funktionsppar från 3.7 till 3.8 när parametern `RuntimeVersion` inte har angetts.</span><span class="sxs-lookup"><span data-stu-id="bf05c-199">Changed the default runtime version in Functions version 3 on Linux for Python function apps from 3.7 to 3.8 when the `RuntimeVersion` parameter is not specified.</span></span> <span data-ttu-id="bf05c-200">Användare kan dock fortfarande skapa Python 3.7-funktionsappar genom att ange `-Runtime Python` och `-RuntimeVersion 3.7`.</span><span class="sxs-lookup"><span data-stu-id="bf05c-200">However, users can still create Python 3.7 function apps by specifying `-Runtime Python` and `-RuntimeVersion 3.7`.</span></span>

#### <a name="before"></a><span data-ttu-id="bf05c-201">Före</span><span class="sxs-lookup"><span data-stu-id="bf05c-201">Before</span></span>

```powershell
# Create a Node 10 function app on Linux
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Linux `
                  -Runtime Node

# Create a Node 10 function app on Windows
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Windows `
                  -Runtime Node

# Create a Python 3.7 function app on Linux
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Linux `
                  -Runtime Python
```

#### <a name="after"></a><span data-ttu-id="bf05c-202">Efter</span><span class="sxs-lookup"><span data-stu-id="bf05c-202">After</span></span>

```powershell
# Create a Node 10 function app on Linux
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Linux `
                  -Runtime Node `
                  -RuntimeVersion 10

# Create a Node 10 function app on Windows
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Windows `
                  -Runtime Node

# Create a Python 3.7 function app on Linux
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Linux `
                  -Runtime Python `
                  -RuntimeVersion 3.7
```

## <a name="azkeyvault"></a><span data-ttu-id="bf05c-203">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="bf05c-203">Az.KeyVault</span></span>

### <a name="new-azkeyvault"></a><span data-ttu-id="bf05c-204">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="bf05c-204">New-AzKeyVault</span></span>

<span data-ttu-id="bf05c-205">Stöder inte längre parametern `DisableSoftDelete` och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="bf05c-205">No longer supports the parameter `DisableSoftDelete` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="bf05c-206">Före</span><span class="sxs-lookup"><span data-stu-id="bf05c-206">Before</span></span>

```powershell
# Opt out soft delete while creating a key vault
New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -DisableSoftDelete
```

#### <a name="after"></a><span data-ttu-id="bf05c-207">Efter</span><span class="sxs-lookup"><span data-stu-id="bf05c-207">After</span></span>

<span data-ttu-id="bf05c-208">Möjligheten att uppdatera inställningen för mjuk borttagning är inaktuell i Az.KeyVault 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="bf05c-208">The ability to update soft-delete setting is deprecated in Az.KeyVault 3.0.0.</span></span> <span data-ttu-id="bf05c-209">Läs mer: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change</span><span class="sxs-lookup"><span data-stu-id="bf05c-209">Read more: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change</span></span>

### <a name="update-azkeyvault"></a><span data-ttu-id="bf05c-210">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="bf05c-210">Update-AzKeyVault</span></span>

<span data-ttu-id="bf05c-211">Stöder inte längre parametrarna `EnableSoftDelete`, `SoftDeleteRetentionInDays`, och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="bf05c-211">No longer supports the parameter `EnableSoftDelete`, `SoftDeleteRetentionInDays`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="bf05c-212">Före</span><span class="sxs-lookup"><span data-stu-id="bf05c-212">Before</span></span>

```powershell
Update-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnableSoftDelete -SoftDeleteRetentionInDays 15
```

#### <a name="after"></a><span data-ttu-id="bf05c-213">Efter</span><span class="sxs-lookup"><span data-stu-id="bf05c-213">After</span></span>

<span data-ttu-id="bf05c-214">Möjligheten att uppdatera inställningen för mjuk borttagning är inaktuell i Az.KeyVault 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="bf05c-214">The ability to update soft-delete setting is deprecated in Az.KeyVault 3.0.0.</span></span> <span data-ttu-id="bf05c-215">Läs mer: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change</span><span class="sxs-lookup"><span data-stu-id="bf05c-215">Read more: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change</span></span>

### <a name="get-azkeyvaultsecret"></a><span data-ttu-id="bf05c-216">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="bf05c-216">Get-AzKeyVaultSecret</span></span>

<span data-ttu-id="bf05c-217">Egenskapen `SecretValueText` av typen `Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret` har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="bf05c-217">The property `SecretValueText` of type `Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret` has been removed.</span></span> <span data-ttu-id="bf05c-218">Egenskapen `SecretValueText` har ersatts av `SecretValue`.</span><span class="sxs-lookup"><span data-stu-id="bf05c-218">The `SecretValueText` property has been replaced with `SecretValue`.</span></span>

#### <a name="before"></a><span data-ttu-id="bf05c-219">Före</span><span class="sxs-lookup"><span data-stu-id="bf05c-219">Before</span></span>

```powershell
$secret = Get-AzKeyVaultSecret -VaultName myVault -Name mySecret
$secretInPlainText = $secret.SecretValueText
```

#### <a name="after"></a><span data-ttu-id="bf05c-220">Efter</span><span class="sxs-lookup"><span data-stu-id="bf05c-220">After</span></span>

```powershell
# PowerShell 7 or newer
$secret = Get-AzKeyVaultSecret -VaultName myVault -Name mySecret
$secretInPlainText = ConvertFrom-SecureString -SecureString $secret.SecretValue -AsPlainText

# Prior to PowerShell 7, or Windows PowerShell
$secret = Get-AzKeyVaultSecret -VaultName myVault -Name mySecret
$secretInPlainText = [System.Runtime.InteropServices.Marshal]::PtrToStringBSTR([System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($secret.SecretValue))
```

## <a name="azmanagedservices"></a><span data-ttu-id="bf05c-221">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="bf05c-221">Az.ManagedServices</span></span>

### <a name="get-azmanagedservicesdefinition"></a><span data-ttu-id="bf05c-222">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="bf05c-222">Get-AzManagedServicesDefinition</span></span>

<span data-ttu-id="bf05c-223">Stöder inte längre parametern `ResourceId` och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="bf05c-223">No longer supports the parameter `ResourceId` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="bf05c-224">Före</span><span class="sxs-lookup"><span data-stu-id="bf05c-224">Before</span></span>

```powershell
Get-AzManagedServicesDefinition -ResourceId xxx
```

#### <a name="after"></a><span data-ttu-id="bf05c-225">Efter</span><span class="sxs-lookup"><span data-stu-id="bf05c-225">After</span></span>

```powershell
Get-AzManagedServicesDefinition -Id xxx
```

### <a name="new-azmanagedservicesassignment"></a><span data-ttu-id="bf05c-226">New-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="bf05c-226">New-AzManagedServicesAssignment</span></span>

<span data-ttu-id="bf05c-227">Stöder inte längre parametrarna `RegistrationDefinitionName`, `RegistrationDefinitionResourceId`, och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="bf05c-227">No longer supports the parameter `RegistrationDefinitionName`, `RegistrationDefinitionResourceId`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="bf05c-228">Före</span><span class="sxs-lookup"><span data-stu-id="bf05c-228">Before</span></span>

```powershell
New-AzManagedServicesAssignment -RegistrationDefinitionName xxx -Scope xxx
```

#### <a name="after"></a><span data-ttu-id="bf05c-229">Efter</span><span class="sxs-lookup"><span data-stu-id="bf05c-229">After</span></span>

```powershell
New-AzManagedServicesAssignment -Scope xxx -RegistrationDefinition xxx
```

### <a name="remove-azmanagedservicesassignment"></a><span data-ttu-id="bf05c-230">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="bf05c-230">Remove-AzManagedServicesAssignment</span></span>

<span data-ttu-id="bf05c-231">Stöder inte längre parametrarna `Id`, `ResourceId`, och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="bf05c-231">No longer supports the parameter `Id`, `ResourceId`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="bf05c-232">Före</span><span class="sxs-lookup"><span data-stu-id="bf05c-232">Before</span></span>

```powershell
Remove-AzManagedServicesAssignment -ResourceId xxx
```

#### <a name="after"></a><span data-ttu-id="bf05c-233">Efter</span><span class="sxs-lookup"><span data-stu-id="bf05c-233">After</span></span>

```powershell
Get-AzManagedServicesAssignment -Scope xxx | Remove-AzManagedServicesAssignment
```

### <a name="remove-azmanagedservicesdefinition"></a><span data-ttu-id="bf05c-234">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="bf05c-234">Remove-AzManagedServicesDefinition</span></span>

<span data-ttu-id="bf05c-235">Stöder inte längre parametrarna `Id`, `ResourceId`, och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="bf05c-235">No longer supports the parameter `Id`, `ResourceId`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="bf05c-236">Före</span><span class="sxs-lookup"><span data-stu-id="bf05c-236">Before</span></span>

```powershell
Remove-AzManagedServicesDefinition -ResourceId xxx
```

#### <a name="after"></a><span data-ttu-id="bf05c-237">Efter</span><span class="sxs-lookup"><span data-stu-id="bf05c-237">After</span></span>

```powershell
Get-AzManagedServicesDefinition -Scope xxx | Remove-AzManagedServicesDefinition
```

## <a name="azresourcemanager"></a><span data-ttu-id="bf05c-238">Az.ResourceManager</span><span class="sxs-lookup"><span data-stu-id="bf05c-238">Az.ResourceManager</span></span>

### <a name="get-azmanagementgroupdeployment"></a><span data-ttu-id="bf05c-239">Get-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="bf05c-239">Get-AzManagementGroupDeployment</span></span>

<span data-ttu-id="bf05c-240">Stöder inte längre parametern `ApiVersion` och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="bf05c-240">No longer supports the parameter `ApiVersion` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="bf05c-241">Före</span><span class="sxs-lookup"><span data-stu-id="bf05c-241">Before</span></span>

```powershell
Get-AzManagementGroupDeployment -ManagementGroupId xxx -Name xxx -ApiVersion xxx
```

#### <a name="after"></a><span data-ttu-id="bf05c-242">Efter</span><span class="sxs-lookup"><span data-stu-id="bf05c-242">After</span></span>

```powershell
Get-AzManagementGroupDeployment -ManagementGroupId xxx -Name xxx
```

### <a name="get-azmanagementgroupdeploymentoperation"></a><span data-ttu-id="bf05c-243">Get-AzManagementGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="bf05c-243">Get-AzManagementGroupDeploymentOperation</span></span>

<span data-ttu-id="bf05c-244">Detsamma gäller för `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="bf05c-244">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azdeployment"></a><span data-ttu-id="bf05c-245">Get-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="bf05c-245">Get-AzDeployment</span></span>

<span data-ttu-id="bf05c-246">Detsamma gäller för `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="bf05c-246">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azdeploymentoperation"></a><span data-ttu-id="bf05c-247">Get-AzDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="bf05c-247">Get-AzDeploymentOperation</span></span>

<span data-ttu-id="bf05c-248">Detsamma gäller för `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="bf05c-248">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azdeploymentwhatifresult"></a><span data-ttu-id="bf05c-249">Get-AzDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="bf05c-249">Get-AzDeploymentWhatIfResult</span></span>

<span data-ttu-id="bf05c-250">Detsamma gäller för `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="bf05c-250">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-aztenantdeployment"></a><span data-ttu-id="bf05c-251">Get-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="bf05c-251">Get-AzTenantDeployment</span></span>

<span data-ttu-id="bf05c-252">Detsamma gäller för `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="bf05c-252">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-aztenantdeploymentoperation"></a><span data-ttu-id="bf05c-253">Get-AzTenantDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="bf05c-253">Get-AzTenantDeploymentOperation</span></span>

<span data-ttu-id="bf05c-254">Detsamma gäller för `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="bf05c-254">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="new-azmanagementgroupdeployment"></a><span data-ttu-id="bf05c-255">New-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="bf05c-255">New-AzManagementGroupDeployment</span></span>

<span data-ttu-id="bf05c-256">Detsamma gäller för `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="bf05c-256">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="new-azdeployment"></a><span data-ttu-id="bf05c-257">New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="bf05c-257">New-AzDeployment</span></span>

<span data-ttu-id="bf05c-258">Detsamma gäller för `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="bf05c-258">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="new-aztenantdeployment"></a><span data-ttu-id="bf05c-259">New-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="bf05c-259">New-AzTenantDeployment</span></span>

<span data-ttu-id="bf05c-260">Detsamma gäller för `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="bf05c-260">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="remove-azmanagementgroupdeployment"></a><span data-ttu-id="bf05c-261">Remove-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="bf05c-261">Remove-AzManagementGroupDeployment</span></span>

<span data-ttu-id="bf05c-262">Detsamma gäller för `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="bf05c-262">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="remove-azdeployment"></a><span data-ttu-id="bf05c-263">Remove-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="bf05c-263">Remove-AzDeployment</span></span>

<span data-ttu-id="bf05c-264">Detsamma gäller för `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="bf05c-264">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="remove-aztenantdeployment"></a><span data-ttu-id="bf05c-265">Remove-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="bf05c-265">Remove-AzTenantDeployment</span></span>

<span data-ttu-id="bf05c-266">Detsamma gäller för `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="bf05c-266">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="save-azmanagementgroupdeploymenttemplate"></a><span data-ttu-id="bf05c-267">Save-AzManagementGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="bf05c-267">Save-AzManagementGroupDeploymentTemplate</span></span>

<span data-ttu-id="bf05c-268">Detsamma gäller för `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="bf05c-268">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="save-azdeploymenttemplate"></a><span data-ttu-id="bf05c-269">Save-AzDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="bf05c-269">Save-AzDeploymentTemplate</span></span>

<span data-ttu-id="bf05c-270">Detsamma gäller för `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="bf05c-270">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="save-aztenantdeploymenttemplate"></a><span data-ttu-id="bf05c-271">Save-AzTenantDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="bf05c-271">Save-AzTenantDeploymentTemplate</span></span>

<span data-ttu-id="bf05c-272">Detsamma gäller för `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="bf05c-272">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="stop-azmanagementgroupdeployment"></a><span data-ttu-id="bf05c-273">Stop-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="bf05c-273">Stop-AzManagementGroupDeployment</span></span>

<span data-ttu-id="bf05c-274">Detsamma gäller för `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="bf05c-274">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="stop-azdeployment"></a><span data-ttu-id="bf05c-275">Stop-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="bf05c-275">Stop-AzDeployment</span></span>

<span data-ttu-id="bf05c-276">Detsamma gäller för `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="bf05c-276">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="stop-aztenantdeployment"></a><span data-ttu-id="bf05c-277">Stop-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="bf05c-277">Stop-AzTenantDeployment</span></span>

<span data-ttu-id="bf05c-278">Detsamma gäller för `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="bf05c-278">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="test-azmanagementgroupdeployment"></a><span data-ttu-id="bf05c-279">Test-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="bf05c-279">Test-AzManagementGroupDeployment</span></span>

<span data-ttu-id="bf05c-280">Detsamma gäller för `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="bf05c-280">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="test-azdeployment"></a><span data-ttu-id="bf05c-281">Test-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="bf05c-281">Test-AzDeployment</span></span>

<span data-ttu-id="bf05c-282">Detsamma gäller för `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="bf05c-282">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="test-aztenantdeployment"></a><span data-ttu-id="bf05c-283">Test-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="bf05c-283">Test-AzTenantDeployment</span></span>

<span data-ttu-id="bf05c-284">Detsamma gäller för `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="bf05c-284">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azresourcegroupdeployment"></a><span data-ttu-id="bf05c-285">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="bf05c-285">Get-AzResourceGroupDeployment</span></span>

<span data-ttu-id="bf05c-286">Detsamma gäller för `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="bf05c-286">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azresourcegroupdeploymentoperation"></a><span data-ttu-id="bf05c-287">Get-AzResourceGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="bf05c-287">Get-AzResourceGroupDeploymentOperation</span></span>

<span data-ttu-id="bf05c-288">Detsamma gäller för `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="bf05c-288">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azresourcegroupdeploymentwhatifresult"></a><span data-ttu-id="bf05c-289">Get-AzResourceGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="bf05c-289">Get-AzResourceGroupDeploymentWhatIfResult</span></span>

<span data-ttu-id="bf05c-290">Detsamma gäller för `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="bf05c-290">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="new-azresourcegroupdeployment"></a><span data-ttu-id="bf05c-291">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="bf05c-291">New-AzResourceGroupDeployment</span></span>

<span data-ttu-id="bf05c-292">Detsamma gäller för `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="bf05c-292">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="remove-azresourcegroupdeployment"></a><span data-ttu-id="bf05c-293">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="bf05c-293">Remove-AzResourceGroupDeployment</span></span>

<span data-ttu-id="bf05c-294">Detsamma gäller för `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="bf05c-294">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="save-azresourcegroupdeploymenttemplate"></a><span data-ttu-id="bf05c-295">Save-AzResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="bf05c-295">Save-AzResourceGroupDeploymentTemplate</span></span>

<span data-ttu-id="bf05c-296">Detsamma gäller för `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="bf05c-296">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="stop-azresourcegroupdeployment"></a><span data-ttu-id="bf05c-297">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="bf05c-297">Stop-AzResourceGroupDeployment</span></span>

<span data-ttu-id="bf05c-298">Detsamma gäller för `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="bf05c-298">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="test-azresourcegroupdeployment"></a><span data-ttu-id="bf05c-299">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="bf05c-299">Test-AzResourceGroupDeployment</span></span>

<span data-ttu-id="bf05c-300">Detsamma gäller för `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="bf05c-300">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azmanagementgroupdeploymentwhatifresult"></a><span data-ttu-id="bf05c-301">Get-AzManagementGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="bf05c-301">Get-AzManagementGroupDeploymentWhatIfResult</span></span>

<span data-ttu-id="bf05c-302">Detsamma gäller för `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="bf05c-302">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-aztenantdeploymentwhatifresult"></a><span data-ttu-id="bf05c-303">Get-AzTenantDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="bf05c-303">Get-AzTenantDeploymentWhatIfResult</span></span>

<span data-ttu-id="bf05c-304">Detsamma gäller för `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="bf05c-304">Same with `Get-AzManagementGroupDeployment`.</span></span>

## <a name="azsql"></a><span data-ttu-id="bf05c-305">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bf05c-305">Az.Sql</span></span>

### <a name="set-azsqlserveractivedirectoryadministrator"></a><span data-ttu-id="bf05c-306">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="bf05c-306">Set-AzSqlServerActiveDirectoryAdministrator</span></span>

<span data-ttu-id="bf05c-307">Stöder inte längre parametern `IsAzureADOnlyAuthentication` och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="bf05c-307">No longer supports the parameter `IsAzureADOnlyAuthentication` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="bf05c-308">Före</span><span class="sxs-lookup"><span data-stu-id="bf05c-308">Before</span></span>

```powershell
Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01' -DisplayName 'DBAs' -IsAzureADOnlyAuthentication
```

#### <a name="after"></a><span data-ttu-id="bf05c-309">Efter</span><span class="sxs-lookup"><span data-stu-id="bf05c-309">After</span></span>

```powershell
Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01' -DisplayName 'DBAs'
```

## <a name="azsynapse"></a><span data-ttu-id="bf05c-310">Az.Synapse</span><span class="sxs-lookup"><span data-stu-id="bf05c-310">Az.Synapse</span></span>

### <a name="new-azsynapsesqlpool"></a><span data-ttu-id="bf05c-311">New-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="bf05c-311">New-AzSynapseSqlPool</span></span>

<span data-ttu-id="bf05c-312">Stöder inte längre parametrarna `FromBackup`, `FromRestorePoint`, `BackupResourceGroupName`, `BackupWorkspaceName`, `BackupSqlPoolName`, `BackupSqlPoolObject`, `BackupResourceId`, `SourceResourceGroupName`, `SourceWorkspaceName`, `SourceSqlPoolName`, `SourceSqlPoolObject`, `SourceResourceId`, `RestorePoint`, och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="bf05c-312">No longer supports the parameter `FromBackup`, `FromRestorePoint`, `BackupResourceGroupName`, `BackupWorkspaceName`, `BackupSqlPoolName`, `BackupSqlPoolObject`, `BackupResourceId`, `SourceResourceGroupName`, `SourceWorkspaceName`, `SourceSqlPoolName`, `SourceSqlPoolObject`, `SourceResourceId`, `RestorePoint`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="bf05c-313">Före</span><span class="sxs-lookup"><span data-stu-id="bf05c-313">Before</span></span>

```powershell
New-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupWorkspaceName ContosoWorkspace -BackupSqlPoolName ExistingContosoSqlPool
```

#### <a name="after"></a><span data-ttu-id="bf05c-314">Efter</span><span class="sxs-lookup"><span data-stu-id="bf05c-314">After</span></span>

```powershell
PS C:\> New-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c
```

### <a name="update-azsynapsesqlpool"></a><span data-ttu-id="bf05c-315">Update-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="bf05c-315">Update-AzSynapseSqlPool</span></span>

<span data-ttu-id="bf05c-316">Stöder inte längre parametrarna `Suspend`, `Resume`, och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="bf05c-316">No longer supports the parameter `Suspend`, `Resume`, and no alias was found for the original parameter name.</span></span>

## <a name="aznetwork"></a><span data-ttu-id="bf05c-317">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bf05c-317">Az.Network</span></span>

### <a name="approve-azprivateendpointconnection"></a><span data-ttu-id="bf05c-318">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="bf05c-318">Approve-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="bf05c-319">Stöder inte längre parametern `PrivateLinkResourceType` och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="bf05c-319">No longer supports the parameter `PrivateLinkResourceType` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="bf05c-320">Före</span><span class="sxs-lookup"><span data-stu-id="bf05c-320">Before</span></span>

```powershell
Approve-AzPrivateEndpointConnection -ResourceGroupName xxx -ServiceName xxx -Name xxx -PrivateLinkResourceType 'Microsoft.Network/privateLinkServices' -Description xxx
```

#### <a name="after"></a><span data-ttu-id="bf05c-321">Efter</span><span class="sxs-lookup"><span data-stu-id="bf05c-321">After</span></span>

```powershell
Approve-AzPrivateEndpointConnection -ResourceGroupName xxx -ServiceName xxx -Name xxx -Description xxx
```

### <a name="deny-azprivateendpointconnection"></a><span data-ttu-id="bf05c-322">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="bf05c-322">Deny-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="bf05c-323">Detsamma gäller för `Approve-AzPrivateEndpointConnection`.</span><span class="sxs-lookup"><span data-stu-id="bf05c-323">Same with `Approve-AzPrivateEndpointConnection`.</span></span>

### <a name="get-azprivateendpointconnection"></a><span data-ttu-id="bf05c-324">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="bf05c-324">Get-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="bf05c-325">Detsamma gäller för `Approve-AzPrivateEndpointConnection`.</span><span class="sxs-lookup"><span data-stu-id="bf05c-325">Same with `Approve-AzPrivateEndpointConnection`.</span></span>

### <a name="remove-azprivateendpointconnection"></a><span data-ttu-id="bf05c-326">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="bf05c-326">Remove-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="bf05c-327">Detsamma gäller för `Approve-AzPrivateEndpointConnection`.</span><span class="sxs-lookup"><span data-stu-id="bf05c-327">Same with `Approve-AzPrivateEndpointConnection`.</span></span>

### <a name="set-azprivateendpointconnection"></a><span data-ttu-id="bf05c-328">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="bf05c-328">Set-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="bf05c-329">Detsamma gäller för `Approve-AzPrivateEndpointConnection`.</span><span class="sxs-lookup"><span data-stu-id="bf05c-329">Same with `Approve-AzPrivateEndpointConnection`.</span></span>

### <a name="new-aznetworkwatcherconnectionmonitorendpointobject"></a><span data-ttu-id="bf05c-330">New-AzNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="bf05c-330">New-AzNetworkWatcherConnectionMonitorEndpointObject</span></span>

<span data-ttu-id="bf05c-331">Stöder inte längre parametrarna `FilterType`, `FilterItem`, och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="bf05c-331">No longer supports the parameter `FilterType`, `FilterItem`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="bf05c-332">Före</span><span class="sxs-lookup"><span data-stu-id="bf05c-332">Before</span></span>

```powershell
$MySrcResourceId1 = '/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace'
$SrcEndpointFilterItem1 =New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject -Type 'AgentAddress' -Address 'WIN-P0HGNDO2S1B'
$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndPointObject -Name 'workspaceEndpoint' -ResourceId $MySrcResourceId1 -FilterType Include -FilterItem $SrcEndpointFilterItem1
```

#### <a name="after"></a><span data-ttu-id="bf05c-333">Efter</span><span class="sxs-lookup"><span data-stu-id="bf05c-333">After</span></span>

```powershell
MySrcResourceId1 = '/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace'
$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndPointObject -Name 'workspaceEndpoint' -ResourceId $MySrcResourceId1
```
