---
title: Migreringsguide för Az 5.0.0
description: Den här migreringsguiden innehåller en lista över icke-bakåtkompatibla ändringar som gjorts i Az version 5.0.0 av Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/27/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 35d562db72e37a630fce8530d715e783412add2e
ms.sourcegitcommit: d81c3b0f0f7289104be03869eb675128b61db7d3
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/17/2020
ms.locfileid: "94715638"
---
# <a name="migration-guide-for-az-500"></a><span data-ttu-id="d85fd-103">Migreringsguide för Az 5.0.0</span><span class="sxs-lookup"><span data-stu-id="d85fd-103">Migration Guide for Az 5.0.0</span></span>

<span data-ttu-id="d85fd-104">I det här dokumentet beskrivs ändringarna mellan Az-versionerna 4.0.0 och 5.0.0.</span><span class="sxs-lookup"><span data-stu-id="d85fd-104">This document describes the changes between the 4.0.0 and 5.0.0 versions of Az.</span></span>

- [<span data-ttu-id="d85fd-105">Migreringsguide för Az 5.0.0</span><span class="sxs-lookup"><span data-stu-id="d85fd-105">Migration Guide for Az 5.0.0</span></span>](#migration-guide-for-az-500)
  - [<span data-ttu-id="d85fd-106">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="d85fd-106">Az.Aks</span></span>](#azaks)
    - [<span data-ttu-id="d85fd-107">New-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="d85fd-107">New-AzAksCluster</span></span>](#new-azakscluster)
    - [<span data-ttu-id="d85fd-108">Set-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="d85fd-108">Set-AzAksCluster</span></span>](#set-azakscluster)
  - [<span data-ttu-id="d85fd-109">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d85fd-109">Az.ContainerRegistry</span></span>](#azcontainerregistry)
    - [<span data-ttu-id="d85fd-110">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d85fd-110">New-AzContainerRegistry</span></span>](#new-azcontainerregistry)
  - [<span data-ttu-id="d85fd-111">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="d85fd-111">Az.Functions</span></span>](#azfunctions)
    - [<span data-ttu-id="d85fd-112">Get-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="d85fd-112">Get-AzFunctionApp</span></span>](#get-azfunctionapp)
    - [<span data-ttu-id="d85fd-113">New-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="d85fd-113">New-AzFunctionApp</span></span>](#new-azfunctionapp)
  - [<span data-ttu-id="d85fd-114">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d85fd-114">Az.KeyVault</span></span>](#azkeyvault)
    - [<span data-ttu-id="d85fd-115">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="d85fd-115">New-AzKeyVault</span></span>](#new-azkeyvault)
    - [<span data-ttu-id="d85fd-116">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="d85fd-116">Update-AzKeyVault</span></span>](#update-azkeyvault)
    - [<span data-ttu-id="d85fd-117">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="d85fd-117">Get-AzKeyVaultSecret</span></span>](#get-azkeyvaultsecret)
  - [<span data-ttu-id="d85fd-118">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="d85fd-118">Az.ManagedServices</span></span>](#azmanagedservices)
    - [<span data-ttu-id="d85fd-119">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="d85fd-119">Get-AzManagedServicesDefinition</span></span>](#get-azmanagedservicesdefinition)
    - [<span data-ttu-id="d85fd-120">New-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="d85fd-120">New-AzManagedServicesAssignment</span></span>](#new-azmanagedservicesassignment)
    - [<span data-ttu-id="d85fd-121">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="d85fd-121">Remove-AzManagedServicesAssignment</span></span>](#remove-azmanagedservicesassignment)
    - [<span data-ttu-id="d85fd-122">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="d85fd-122">Remove-AzManagedServicesDefinition</span></span>](#remove-azmanagedservicesdefinition)
  - [<span data-ttu-id="d85fd-123">Az.ResourceManager</span><span class="sxs-lookup"><span data-stu-id="d85fd-123">Az.ResourceManager</span></span>](#azresourcemanager)
    - [<span data-ttu-id="d85fd-124">Get-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d85fd-124">Get-AzManagementGroupDeployment</span></span>](#get-azmanagementgroupdeployment)
    - [<span data-ttu-id="d85fd-125">Get-AzManagementGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="d85fd-125">Get-AzManagementGroupDeploymentOperation</span></span>](#get-azmanagementgroupdeploymentoperation)
    - [<span data-ttu-id="d85fd-126">Get-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="d85fd-126">Get-AzDeployment</span></span>](#get-azdeployment)
    - [<span data-ttu-id="d85fd-127">Get-AzDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="d85fd-127">Get-AzDeploymentOperation</span></span>](#get-azdeploymentoperation)
    - [<span data-ttu-id="d85fd-128">Get-AzDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="d85fd-128">Get-AzDeploymentWhatIfResult</span></span>](#get-azdeploymentwhatifresult)
    - [<span data-ttu-id="d85fd-129">Get-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="d85fd-129">Get-AzTenantDeployment</span></span>](#get-aztenantdeployment)
    - [<span data-ttu-id="d85fd-130">Get-AzTenantDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="d85fd-130">Get-AzTenantDeploymentOperation</span></span>](#get-aztenantdeploymentoperation)
    - [<span data-ttu-id="d85fd-131">New-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d85fd-131">New-AzManagementGroupDeployment</span></span>](#new-azmanagementgroupdeployment)
    - [<span data-ttu-id="d85fd-132">New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="d85fd-132">New-AzDeployment</span></span>](#new-azdeployment)
    - [<span data-ttu-id="d85fd-133">New-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="d85fd-133">New-AzTenantDeployment</span></span>](#new-aztenantdeployment)
    - [<span data-ttu-id="d85fd-134">Remove-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d85fd-134">Remove-AzManagementGroupDeployment</span></span>](#remove-azmanagementgroupdeployment)
    - [<span data-ttu-id="d85fd-135">Remove-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="d85fd-135">Remove-AzDeployment</span></span>](#remove-azdeployment)
    - [<span data-ttu-id="d85fd-136">Remove-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="d85fd-136">Remove-AzTenantDeployment</span></span>](#remove-aztenantdeployment)
    - [<span data-ttu-id="d85fd-137">Save-AzManagementGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="d85fd-137">Save-AzManagementGroupDeploymentTemplate</span></span>](#save-azmanagementgroupdeploymenttemplate)
    - [<span data-ttu-id="d85fd-138">Save-AzDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="d85fd-138">Save-AzDeploymentTemplate</span></span>](#save-azdeploymenttemplate)
    - [<span data-ttu-id="d85fd-139">Save-AzTenantDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="d85fd-139">Save-AzTenantDeploymentTemplate</span></span>](#save-aztenantdeploymenttemplate)
    - [<span data-ttu-id="d85fd-140">Stop-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d85fd-140">Stop-AzManagementGroupDeployment</span></span>](#stop-azmanagementgroupdeployment)
    - [<span data-ttu-id="d85fd-141">Stop-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="d85fd-141">Stop-AzDeployment</span></span>](#stop-azdeployment)
    - [<span data-ttu-id="d85fd-142">Stop-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="d85fd-142">Stop-AzTenantDeployment</span></span>](#stop-aztenantdeployment)
    - [<span data-ttu-id="d85fd-143">Test-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d85fd-143">Test-AzManagementGroupDeployment</span></span>](#test-azmanagementgroupdeployment)
    - [<span data-ttu-id="d85fd-144">Test-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="d85fd-144">Test-AzDeployment</span></span>](#test-azdeployment)
    - [<span data-ttu-id="d85fd-145">Test-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="d85fd-145">Test-AzTenantDeployment</span></span>](#test-aztenantdeployment)
    - [<span data-ttu-id="d85fd-146">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d85fd-146">Get-AzResourceGroupDeployment</span></span>](#get-azresourcegroupdeployment)
    - [<span data-ttu-id="d85fd-147">Get-AzResourceGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="d85fd-147">Get-AzResourceGroupDeploymentOperation</span></span>](#get-azresourcegroupdeploymentoperation)
    - [<span data-ttu-id="d85fd-148">Get-AzResourceGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="d85fd-148">Get-AzResourceGroupDeploymentWhatIfResult</span></span>](#get-azresourcegroupdeploymentwhatifresult)
    - [<span data-ttu-id="d85fd-149">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d85fd-149">New-AzResourceGroupDeployment</span></span>](#new-azresourcegroupdeployment)
    - [<span data-ttu-id="d85fd-150">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d85fd-150">Remove-AzResourceGroupDeployment</span></span>](#remove-azresourcegroupdeployment)
    - [<span data-ttu-id="d85fd-151">Save-AzResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="d85fd-151">Save-AzResourceGroupDeploymentTemplate</span></span>](#save-azresourcegroupdeploymenttemplate)
    - [<span data-ttu-id="d85fd-152">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d85fd-152">Stop-AzResourceGroupDeployment</span></span>](#stop-azresourcegroupdeployment)
    - [<span data-ttu-id="d85fd-153">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d85fd-153">Test-AzResourceGroupDeployment</span></span>](#test-azresourcegroupdeployment)
    - [<span data-ttu-id="d85fd-154">Get-AzManagementGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="d85fd-154">Get-AzManagementGroupDeploymentWhatIfResult</span></span>](#get-azmanagementgroupdeploymentwhatifresult)
    - [<span data-ttu-id="d85fd-155">Get-AzTenantDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="d85fd-155">Get-AzTenantDeploymentWhatIfResult</span></span>](#get-aztenantdeploymentwhatifresult)
  - [<span data-ttu-id="d85fd-156">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d85fd-156">Az.Sql</span></span>](#azsql)
    - [<span data-ttu-id="d85fd-157">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="d85fd-157">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](#set-azsqlserveractivedirectoryadministrator)
  - [<span data-ttu-id="d85fd-158">Az.Synapse</span><span class="sxs-lookup"><span data-stu-id="d85fd-158">Az.Synapse</span></span>](#azsynapse)
    - [<span data-ttu-id="d85fd-159">New-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="d85fd-159">New-AzSynapseSqlPool</span></span>](#new-azsynapsesqlpool)
    - [<span data-ttu-id="d85fd-160">Update-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="d85fd-160">Update-AzSynapseSqlPool</span></span>](#update-azsynapsesqlpool)
  - [<span data-ttu-id="d85fd-161">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d85fd-161">Az.Network</span></span>](#aznetwork)
    - [<span data-ttu-id="d85fd-162">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d85fd-162">Approve-AzPrivateEndpointConnection</span></span>](#approve-azprivateendpointconnection)
    - [<span data-ttu-id="d85fd-163">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d85fd-163">Deny-AzPrivateEndpointConnection</span></span>](#deny-azprivateendpointconnection)
    - [<span data-ttu-id="d85fd-164">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d85fd-164">Get-AzPrivateEndpointConnection</span></span>](#get-azprivateendpointconnection)
    - [<span data-ttu-id="d85fd-165">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d85fd-165">Remove-AzPrivateEndpointConnection</span></span>](#remove-azprivateendpointconnection)
    - [<span data-ttu-id="d85fd-166">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d85fd-166">Set-AzPrivateEndpointConnection</span></span>](#set-azprivateendpointconnection)
    - [<span data-ttu-id="d85fd-167">New-AzNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="d85fd-167">New-AzNetworkWatcherConnectionMonitorEndpointObject</span></span>](#new-aznetworkwatcherconnectionmonitorendpointobject)

## <a name="azaks"></a><span data-ttu-id="d85fd-168">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="d85fd-168">Az.Aks</span></span>

### <a name="new-azakscluster"></a><span data-ttu-id="d85fd-169">New-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="d85fd-169">New-AzAksCluster</span></span>

- <span data-ttu-id="d85fd-170">Stöder inte längre parametern `NodeOsType` och inget alias hittades för det ursprungliga parameternamnet, som alltid kommer att vara `Linux`.</span><span class="sxs-lookup"><span data-stu-id="d85fd-170">No longer supports the parameter `NodeOsType` and no alias was found for the original parameter name, it will always be `Linux`.</span></span>
- <span data-ttu-id="d85fd-171">Stöder inte längre aliaset `ClientIdAndSecret` för parametern `ServicePrincipalIdAndSecret`.</span><span class="sxs-lookup"><span data-stu-id="d85fd-171">No longer supports the alias `ClientIdAndSecret` for parameter `ServicePrincipalIdAndSecret`.</span></span>
- <span data-ttu-id="d85fd-172">Standardvärdet för `NodeVmSetType` har ändrats från `AvailabilitySet` till `VirtualMachineScaleSets`.</span><span class="sxs-lookup"><span data-stu-id="d85fd-172">The default value of `NodeVmSetType` is changed from `AvailabilitySet` to `VirtualMachineScaleSets`.</span></span>
- <span data-ttu-id="d85fd-173">Standardvärdet för `NetworkPlugin` har ändrats från `none` till `azure`.</span><span class="sxs-lookup"><span data-stu-id="d85fd-173">The default value of `NetworkPlugin` is changed from `none` to `azure`.</span></span>

#### <a name="before"></a><span data-ttu-id="d85fd-174">Före</span><span class="sxs-lookup"><span data-stu-id="d85fd-174">Before</span></span>

```powershell
New-AzAksCluster -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeOsType Linux -ClientIdAndSecret xxx
```

#### <a name="after"></a><span data-ttu-id="d85fd-175">Efter</span><span class="sxs-lookup"><span data-stu-id="d85fd-175">After</span></span>

```powershell
New-AzAksCluster -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NodeVmSetType AvailabilitySet  -ServicePrincipalIdAndSecret xxx
```

### <a name="set-azakscluster"></a><span data-ttu-id="d85fd-176">Set-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="d85fd-176">Set-AzAksCluster</span></span>

<span data-ttu-id="d85fd-177">Stöder inte längre aliaset `ClientIdAndSecret` för parametern `ServicePrincipalIdAndSecret`.</span><span class="sxs-lookup"><span data-stu-id="d85fd-177">No longer supports the alias `ClientIdAndSecret` for parameter `ServicePrincipalIdAndSecret`.</span></span>

#### <a name="before"></a><span data-ttu-id="d85fd-178">Före</span><span class="sxs-lookup"><span data-stu-id="d85fd-178">Before</span></span>

```powershell
Get-AzAksCluster -ResourceGroupName xxx -Name xxx | Set-AzAksCluster -ClientIdAndSecret xxx
```

#### <a name="after"></a><span data-ttu-id="d85fd-179">Efter</span><span class="sxs-lookup"><span data-stu-id="d85fd-179">After</span></span>

```powershell
Get-AzAksCluster -ResourceGroupName xxx -Name xxx | Set-AzAksCluster -ServicePrincipalIdAndSecret xxx
```

## <a name="azcontainerregistry"></a><span data-ttu-id="d85fd-180">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d85fd-180">Az.ContainerRegistry</span></span>

### <a name="new-azcontainerregistry"></a><span data-ttu-id="d85fd-181">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d85fd-181">New-AzContainerRegistry</span></span>

<span data-ttu-id="d85fd-182">Stöder inte längre parametern `StorageAccountName` och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="d85fd-182">No longer supports the parameter `StorageAccountName` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="d85fd-183">Före</span><span class="sxs-lookup"><span data-stu-id="d85fd-183">Before</span></span>

```powershell
New-AzContainerRegistry -Name $name -ResourceGroupName $rg -Location $location -SKU Classic -StorageAccountName $storage
```

#### <a name="after"></a><span data-ttu-id="d85fd-184">Efter</span><span class="sxs-lookup"><span data-stu-id="d85fd-184">After</span></span>

<span data-ttu-id="d85fd-185">`Classic` är inaktuell och `StorageAccountName` har tagits bort eftersom den endast fungerar med klassiska Container Registry.</span><span class="sxs-lookup"><span data-stu-id="d85fd-185">`Classic` was deprecated and `StorageAccountName` was removed since it only works with Classic Container Registry.</span></span>

## <a name="azfunctions"></a><span data-ttu-id="d85fd-186">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="d85fd-186">Az.Functions</span></span>

### <a name="get-azfunctionapp"></a><span data-ttu-id="d85fd-187">Get-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="d85fd-187">Get-AzFunctionApp</span></span>

<span data-ttu-id="d85fd-188">Tog bort växelparametern `IncludeSlot` från alla förutom en parameteruppsättning av `Get-AzFunctionApp`.</span><span class="sxs-lookup"><span data-stu-id="d85fd-188">Removed `IncludeSlot` switch parameter from all but one parameter set of `Get-AzFunctionApp`.</span></span> <span data-ttu-id="d85fd-189">Cmdleten stöder nu hämtning av distributionsfack i resultaten när `-IncludeSlot` anges.</span><span class="sxs-lookup"><span data-stu-id="d85fd-189">The cmdlet now supports retrieving deployment slots in the results when `-IncludeSlot` is specified.</span></span>
<span data-ttu-id="d85fd-190">Den här funktionen fungerade inte i den tidigare cmdlet-versionen.</span><span class="sxs-lookup"><span data-stu-id="d85fd-190">This functionality was broken in the previous cmdlet version.</span></span> <span data-ttu-id="d85fd-191">Detta är dock åtgärdat nu.</span><span class="sxs-lookup"><span data-stu-id="d85fd-191">However, this is now fixed.</span></span>

### <a name="new-azfunctionapp"></a><span data-ttu-id="d85fd-192">New-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="d85fd-192">New-AzFunctionApp</span></span>

- <span data-ttu-id="d85fd-193">Korrigerade `-DisableApplicationInsights` i `New-AzFunctionApp` så att inga Application Insights-projekt skapas när det här alternativet har angetts.</span><span class="sxs-lookup"><span data-stu-id="d85fd-193">Fixed `-DisableApplicationInsights` in `New-AzFunctionApp` so that no application insights project is created when this option is specified.</span></span>
- <span data-ttu-id="d85fd-194">Tog bort stöd för att skapa PowerShell 6.2-funktionsappar eftersom PowerShell 6.2 är EOL.</span><span class="sxs-lookup"><span data-stu-id="d85fd-194">Removed support to create PowerShell 6.2 function apps since PowerShell 6.2 is EOL.</span></span> <span data-ttu-id="d85fd-195">Vi rekommenderar för närvarande att kunder skapar PowerShell 7.0-funktionsappar i stället.</span><span class="sxs-lookup"><span data-stu-id="d85fd-195">The current guidance for customers is to create PowerShell 7.0 function apps instead.</span></span>
- <span data-ttu-id="d85fd-196">Ändrade körningsversionen som är standard i Functions version 3 i Windows för PowerShell-funktionsppar från 6.2 till 7.0 när parametern `RuntimeVersion` inte har angetts.</span><span class="sxs-lookup"><span data-stu-id="d85fd-196">Changed the default runtime version in Functions version 3 on Windows for PowerShell function apps from 6.2 to 7.0 when the `RuntimeVersion` parameter is not specified.</span></span>
- <span data-ttu-id="d85fd-197">Ändrade körningsversionen som är standard i Functions version 3 i Windows och Linux för Node-funktionsppar från 10 till 12 när parametern `RuntimeVersion` inte har angetts.</span><span class="sxs-lookup"><span data-stu-id="d85fd-197">Changed the default runtime version in Functions version 3 on Windows and Linux for Node function apps from 10 to 12 when the `RuntimeVersion` parameter is not specified.</span></span> <span data-ttu-id="d85fd-198">Användare kan dock fortfarande skapa Node 10-funktionsappar genom att ange `-Runtime Node` och `-RuntimeVersion 10`.</span><span class="sxs-lookup"><span data-stu-id="d85fd-198">However, users can still create Node 10 function apps by specifying `-Runtime Node` and `-RuntimeVersion 10`.</span></span> <span data-ttu-id="d85fd-199">Ändrade körningsversionen som är standard i Functions version 3 i Linux för Python-funktionsppar från 3.7 till 3.8 när parametern `RuntimeVersion` inte har angetts.</span><span class="sxs-lookup"><span data-stu-id="d85fd-199">Changed the default runtime version in Functions version 3 on Linux for Python function apps from 3.7 to 3.8 when the `RuntimeVersion` parameter is not specified.</span></span> <span data-ttu-id="d85fd-200">Användare kan dock fortfarande skapa Python 3.7-funktionsappar genom att ange `-Runtime Python` och `-RuntimeVersion 3.7`.</span><span class="sxs-lookup"><span data-stu-id="d85fd-200">However, users can still create Python 3.7 function apps by specifying `-Runtime Python` and `-RuntimeVersion 3.7`.</span></span>

#### <a name="before"></a><span data-ttu-id="d85fd-201">Före</span><span class="sxs-lookup"><span data-stu-id="d85fd-201">Before</span></span>

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

#### <a name="after"></a><span data-ttu-id="d85fd-202">Efter</span><span class="sxs-lookup"><span data-stu-id="d85fd-202">After</span></span>

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

## <a name="azkeyvault"></a><span data-ttu-id="d85fd-203">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d85fd-203">Az.KeyVault</span></span>

### <a name="new-azkeyvault"></a><span data-ttu-id="d85fd-204">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="d85fd-204">New-AzKeyVault</span></span>

<span data-ttu-id="d85fd-205">Stöder inte längre parametern `DisableSoftDelete` och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="d85fd-205">No longer supports the parameter `DisableSoftDelete` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="d85fd-206">Före</span><span class="sxs-lookup"><span data-stu-id="d85fd-206">Before</span></span>

```powershell
# Opt out soft delete while creating a key vault
New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -DisableSoftDelete
```

#### <a name="after"></a><span data-ttu-id="d85fd-207">Efter</span><span class="sxs-lookup"><span data-stu-id="d85fd-207">After</span></span>

<span data-ttu-id="d85fd-208">Möjligheten att uppdatera inställningen för mjuk borttagning är inaktuell i Az.KeyVault 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="d85fd-208">The ability to update soft-delete setting is deprecated in Az.KeyVault 3.0.0.</span></span> <span data-ttu-id="d85fd-209">Läs mer: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change</span><span class="sxs-lookup"><span data-stu-id="d85fd-209">Read more: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change</span></span>

### <a name="update-azkeyvault"></a><span data-ttu-id="d85fd-210">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="d85fd-210">Update-AzKeyVault</span></span>

<span data-ttu-id="d85fd-211">Stöder inte längre parametrarna `EnableSoftDelete`, `SoftDeleteRetentionInDays`, och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="d85fd-211">No longer supports the parameter `EnableSoftDelete`, `SoftDeleteRetentionInDays`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="d85fd-212">Före</span><span class="sxs-lookup"><span data-stu-id="d85fd-212">Before</span></span>

```powershell
Update-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnableSoftDelete -SoftDeleteRetentionInDays 15
```

#### <a name="after"></a><span data-ttu-id="d85fd-213">Efter</span><span class="sxs-lookup"><span data-stu-id="d85fd-213">After</span></span>

<span data-ttu-id="d85fd-214">Möjligheten att uppdatera inställningen för mjuk borttagning är inaktuell i Az.KeyVault 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="d85fd-214">The ability to update soft-delete setting is deprecated in Az.KeyVault 3.0.0.</span></span> <span data-ttu-id="d85fd-215">Läs mer: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change</span><span class="sxs-lookup"><span data-stu-id="d85fd-215">Read more: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change</span></span>

### <a name="get-azkeyvaultsecret"></a><span data-ttu-id="d85fd-216">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="d85fd-216">Get-AzKeyVaultSecret</span></span>

<span data-ttu-id="d85fd-217">Egenskapen `SecretValueText` av typen `Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret` har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="d85fd-217">The property `SecretValueText` of type `Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret` has been removed.</span></span> <span data-ttu-id="d85fd-218">Egenskapen `SecretValueText` har ersatts av `SecretValue`.</span><span class="sxs-lookup"><span data-stu-id="d85fd-218">The `SecretValueText` property has been replaced with `SecretValue`.</span></span>

#### <a name="before"></a><span data-ttu-id="d85fd-219">Före</span><span class="sxs-lookup"><span data-stu-id="d85fd-219">Before</span></span>

```powershell
$secret = Get-AzKeyVaultSecret -VaultName myVault -Name mySecret
$secretInPlainText = $secret.SecretValueText
```

#### <a name="after"></a><span data-ttu-id="d85fd-220">Efter</span><span class="sxs-lookup"><span data-stu-id="d85fd-220">After</span></span>

```powershell
# PowerShell 7 or newer
$secret = Get-AzKeyVaultSecret -VaultName myVault -Name mySecret
$secretInPlainText = ConvertFrom-SecureString -SecureString $secret.SecretValue -AsPlainText

# Prior to PowerShell 7, or Windows PowerShell
$secret = Get-AzKeyVaultSecret -VaultName myVault -Name mySecret
$secretInPlainText = [System.Runtime.InteropServices.Marshal]::PtrToStringBSTR([System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($secret.SecretValue))
```

## <a name="azmanagedservices"></a><span data-ttu-id="d85fd-221">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="d85fd-221">Az.ManagedServices</span></span>

### <a name="get-azmanagedservicesdefinition"></a><span data-ttu-id="d85fd-222">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="d85fd-222">Get-AzManagedServicesDefinition</span></span>

<span data-ttu-id="d85fd-223">Stöder inte längre parametern `ResourceId` och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="d85fd-223">No longer supports the parameter `ResourceId` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="d85fd-224">Före</span><span class="sxs-lookup"><span data-stu-id="d85fd-224">Before</span></span>

```powershell
Get-AzManagedServicesDefinition -ResourceId xxx
```

#### <a name="after"></a><span data-ttu-id="d85fd-225">Efter</span><span class="sxs-lookup"><span data-stu-id="d85fd-225">After</span></span>

```powershell
Get-AzManagedServicesDefinition -Id xxx
```

### <a name="new-azmanagedservicesassignment"></a><span data-ttu-id="d85fd-226">New-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="d85fd-226">New-AzManagedServicesAssignment</span></span>

<span data-ttu-id="d85fd-227">Stöder inte längre parametrarna `RegistrationDefinitionName`, `RegistrationDefinitionResourceId`, och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="d85fd-227">No longer supports the parameter `RegistrationDefinitionName`, `RegistrationDefinitionResourceId`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="d85fd-228">Före</span><span class="sxs-lookup"><span data-stu-id="d85fd-228">Before</span></span>

```powershell
New-AzManagedServicesAssignment -RegistrationDefinitionName xxx -Scope xxx
```

#### <a name="after"></a><span data-ttu-id="d85fd-229">Efter</span><span class="sxs-lookup"><span data-stu-id="d85fd-229">After</span></span>

```powershell
New-AzManagedServicesAssignment -Scope xxx -RegistrationDefinition xxx
```

### <a name="remove-azmanagedservicesassignment"></a><span data-ttu-id="d85fd-230">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="d85fd-230">Remove-AzManagedServicesAssignment</span></span>

<span data-ttu-id="d85fd-231">Stöder inte längre parametrarna `Id`, `ResourceId`, och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="d85fd-231">No longer supports the parameter `Id`, `ResourceId`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="d85fd-232">Före</span><span class="sxs-lookup"><span data-stu-id="d85fd-232">Before</span></span>

```powershell
Remove-AzManagedServicesAssignment -ResourceId xxx
```

#### <a name="after"></a><span data-ttu-id="d85fd-233">Efter</span><span class="sxs-lookup"><span data-stu-id="d85fd-233">After</span></span>

```powershell
Get-AzManagedServicesAssignment -Scope xxx | Remove-AzManagedServicesAssignment
```

### <a name="remove-azmanagedservicesdefinition"></a><span data-ttu-id="d85fd-234">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="d85fd-234">Remove-AzManagedServicesDefinition</span></span>

<span data-ttu-id="d85fd-235">Stöder inte längre parametrarna `Id`, `ResourceId`, och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="d85fd-235">No longer supports the parameter `Id`, `ResourceId`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="d85fd-236">Före</span><span class="sxs-lookup"><span data-stu-id="d85fd-236">Before</span></span>

```powershell
Remove-AzManagedServicesDefinition -ResourceId xxx
```

#### <a name="after"></a><span data-ttu-id="d85fd-237">Efter</span><span class="sxs-lookup"><span data-stu-id="d85fd-237">After</span></span>

```powershell
Get-AzManagedServicesDefinition -Scope xxx | Remove-AzManagedServicesDefinition
```

## <a name="azresourcemanager"></a><span data-ttu-id="d85fd-238">Az.ResourceManager</span><span class="sxs-lookup"><span data-stu-id="d85fd-238">Az.ResourceManager</span></span>

### <a name="get-azmanagementgroupdeployment"></a><span data-ttu-id="d85fd-239">Get-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d85fd-239">Get-AzManagementGroupDeployment</span></span>

<span data-ttu-id="d85fd-240">Stöder inte längre parametern `ApiVersion` och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="d85fd-240">No longer supports the parameter `ApiVersion` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="d85fd-241">Före</span><span class="sxs-lookup"><span data-stu-id="d85fd-241">Before</span></span>

```powershell
Get-AzManagementGroupDeployment -ManagementGroupId xxx -Name xxx -ApiVersion xxx
```

#### <a name="after"></a><span data-ttu-id="d85fd-242">Efter</span><span class="sxs-lookup"><span data-stu-id="d85fd-242">After</span></span>

```powershell
Get-AzManagementGroupDeployment -ManagementGroupId xxx -Name xxx
```

### <a name="get-azmanagementgroupdeploymentoperation"></a><span data-ttu-id="d85fd-243">Get-AzManagementGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="d85fd-243">Get-AzManagementGroupDeploymentOperation</span></span>

<span data-ttu-id="d85fd-244">Detsamma gäller för `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="d85fd-244">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azdeployment"></a><span data-ttu-id="d85fd-245">Get-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="d85fd-245">Get-AzDeployment</span></span>

<span data-ttu-id="d85fd-246">Detsamma gäller för `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="d85fd-246">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azdeploymentoperation"></a><span data-ttu-id="d85fd-247">Get-AzDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="d85fd-247">Get-AzDeploymentOperation</span></span>

<span data-ttu-id="d85fd-248">Detsamma gäller för `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="d85fd-248">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azdeploymentwhatifresult"></a><span data-ttu-id="d85fd-249">Get-AzDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="d85fd-249">Get-AzDeploymentWhatIfResult</span></span>

<span data-ttu-id="d85fd-250">Detsamma gäller för `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="d85fd-250">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-aztenantdeployment"></a><span data-ttu-id="d85fd-251">Get-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="d85fd-251">Get-AzTenantDeployment</span></span>

<span data-ttu-id="d85fd-252">Detsamma gäller för `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="d85fd-252">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-aztenantdeploymentoperation"></a><span data-ttu-id="d85fd-253">Get-AzTenantDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="d85fd-253">Get-AzTenantDeploymentOperation</span></span>

<span data-ttu-id="d85fd-254">Detsamma gäller för `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="d85fd-254">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="new-azmanagementgroupdeployment"></a><span data-ttu-id="d85fd-255">New-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d85fd-255">New-AzManagementGroupDeployment</span></span>

<span data-ttu-id="d85fd-256">Detsamma gäller för `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="d85fd-256">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="new-azdeployment"></a><span data-ttu-id="d85fd-257">New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="d85fd-257">New-AzDeployment</span></span>

<span data-ttu-id="d85fd-258">Detsamma gäller för `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="d85fd-258">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="new-aztenantdeployment"></a><span data-ttu-id="d85fd-259">New-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="d85fd-259">New-AzTenantDeployment</span></span>

<span data-ttu-id="d85fd-260">Detsamma gäller för `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="d85fd-260">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="remove-azmanagementgroupdeployment"></a><span data-ttu-id="d85fd-261">Remove-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d85fd-261">Remove-AzManagementGroupDeployment</span></span>

<span data-ttu-id="d85fd-262">Detsamma gäller för `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="d85fd-262">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="remove-azdeployment"></a><span data-ttu-id="d85fd-263">Remove-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="d85fd-263">Remove-AzDeployment</span></span>

<span data-ttu-id="d85fd-264">Detsamma gäller för `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="d85fd-264">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="remove-aztenantdeployment"></a><span data-ttu-id="d85fd-265">Remove-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="d85fd-265">Remove-AzTenantDeployment</span></span>

<span data-ttu-id="d85fd-266">Detsamma gäller för `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="d85fd-266">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="save-azmanagementgroupdeploymenttemplate"></a><span data-ttu-id="d85fd-267">Save-AzManagementGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="d85fd-267">Save-AzManagementGroupDeploymentTemplate</span></span>

<span data-ttu-id="d85fd-268">Detsamma gäller för `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="d85fd-268">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="save-azdeploymenttemplate"></a><span data-ttu-id="d85fd-269">Save-AzDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="d85fd-269">Save-AzDeploymentTemplate</span></span>

<span data-ttu-id="d85fd-270">Detsamma gäller för `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="d85fd-270">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="save-aztenantdeploymenttemplate"></a><span data-ttu-id="d85fd-271">Save-AzTenantDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="d85fd-271">Save-AzTenantDeploymentTemplate</span></span>

<span data-ttu-id="d85fd-272">Detsamma gäller för `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="d85fd-272">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="stop-azmanagementgroupdeployment"></a><span data-ttu-id="d85fd-273">Stop-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d85fd-273">Stop-AzManagementGroupDeployment</span></span>

<span data-ttu-id="d85fd-274">Detsamma gäller för `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="d85fd-274">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="stop-azdeployment"></a><span data-ttu-id="d85fd-275">Stop-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="d85fd-275">Stop-AzDeployment</span></span>

<span data-ttu-id="d85fd-276">Detsamma gäller för `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="d85fd-276">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="stop-aztenantdeployment"></a><span data-ttu-id="d85fd-277">Stop-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="d85fd-277">Stop-AzTenantDeployment</span></span>

<span data-ttu-id="d85fd-278">Detsamma gäller för `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="d85fd-278">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="test-azmanagementgroupdeployment"></a><span data-ttu-id="d85fd-279">Test-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d85fd-279">Test-AzManagementGroupDeployment</span></span>

<span data-ttu-id="d85fd-280">Detsamma gäller för `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="d85fd-280">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="test-azdeployment"></a><span data-ttu-id="d85fd-281">Test-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="d85fd-281">Test-AzDeployment</span></span>

<span data-ttu-id="d85fd-282">Detsamma gäller för `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="d85fd-282">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="test-aztenantdeployment"></a><span data-ttu-id="d85fd-283">Test-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="d85fd-283">Test-AzTenantDeployment</span></span>

<span data-ttu-id="d85fd-284">Detsamma gäller för `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="d85fd-284">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azresourcegroupdeployment"></a><span data-ttu-id="d85fd-285">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d85fd-285">Get-AzResourceGroupDeployment</span></span>

<span data-ttu-id="d85fd-286">Detsamma gäller för `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="d85fd-286">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azresourcegroupdeploymentoperation"></a><span data-ttu-id="d85fd-287">Get-AzResourceGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="d85fd-287">Get-AzResourceGroupDeploymentOperation</span></span>

<span data-ttu-id="d85fd-288">Detsamma gäller för `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="d85fd-288">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azresourcegroupdeploymentwhatifresult"></a><span data-ttu-id="d85fd-289">Get-AzResourceGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="d85fd-289">Get-AzResourceGroupDeploymentWhatIfResult</span></span>

<span data-ttu-id="d85fd-290">Detsamma gäller för `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="d85fd-290">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="new-azresourcegroupdeployment"></a><span data-ttu-id="d85fd-291">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d85fd-291">New-AzResourceGroupDeployment</span></span>

<span data-ttu-id="d85fd-292">Detsamma gäller för `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="d85fd-292">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="remove-azresourcegroupdeployment"></a><span data-ttu-id="d85fd-293">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d85fd-293">Remove-AzResourceGroupDeployment</span></span>

<span data-ttu-id="d85fd-294">Detsamma gäller för `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="d85fd-294">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="save-azresourcegroupdeploymenttemplate"></a><span data-ttu-id="d85fd-295">Save-AzResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="d85fd-295">Save-AzResourceGroupDeploymentTemplate</span></span>

<span data-ttu-id="d85fd-296">Detsamma gäller för `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="d85fd-296">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="stop-azresourcegroupdeployment"></a><span data-ttu-id="d85fd-297">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d85fd-297">Stop-AzResourceGroupDeployment</span></span>

<span data-ttu-id="d85fd-298">Detsamma gäller för `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="d85fd-298">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="test-azresourcegroupdeployment"></a><span data-ttu-id="d85fd-299">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d85fd-299">Test-AzResourceGroupDeployment</span></span>

<span data-ttu-id="d85fd-300">Detsamma gäller för `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="d85fd-300">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azmanagementgroupdeploymentwhatifresult"></a><span data-ttu-id="d85fd-301">Get-AzManagementGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="d85fd-301">Get-AzManagementGroupDeploymentWhatIfResult</span></span>

<span data-ttu-id="d85fd-302">Detsamma gäller för `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="d85fd-302">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-aztenantdeploymentwhatifresult"></a><span data-ttu-id="d85fd-303">Get-AzTenantDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="d85fd-303">Get-AzTenantDeploymentWhatIfResult</span></span>

<span data-ttu-id="d85fd-304">Detsamma gäller för `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="d85fd-304">Same with `Get-AzManagementGroupDeployment`.</span></span>

## <a name="azsql"></a><span data-ttu-id="d85fd-305">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d85fd-305">Az.Sql</span></span>

### <a name="set-azsqlserveractivedirectoryadministrator"></a><span data-ttu-id="d85fd-306">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="d85fd-306">Set-AzSqlServerActiveDirectoryAdministrator</span></span>

<span data-ttu-id="d85fd-307">Stöder inte längre parametern `IsAzureADOnlyAuthentication` och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="d85fd-307">No longer supports the parameter `IsAzureADOnlyAuthentication` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="d85fd-308">Före</span><span class="sxs-lookup"><span data-stu-id="d85fd-308">Before</span></span>

```powershell
Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01' -DisplayName 'DBAs' -IsAzureADOnlyAuthentication
```

#### <a name="after"></a><span data-ttu-id="d85fd-309">Efter</span><span class="sxs-lookup"><span data-stu-id="d85fd-309">After</span></span>

```powershell
Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01' -DisplayName 'DBAs'
```

## <a name="azsynapse"></a><span data-ttu-id="d85fd-310">Az.Synapse</span><span class="sxs-lookup"><span data-stu-id="d85fd-310">Az.Synapse</span></span>

### <a name="new-azsynapsesqlpool"></a><span data-ttu-id="d85fd-311">New-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="d85fd-311">New-AzSynapseSqlPool</span></span>

<span data-ttu-id="d85fd-312">Stöder inte längre parametrarna `FromBackup`, `FromRestorePoint`, `BackupResourceGroupName`, `BackupWorkspaceName`, `BackupSqlPoolName`, `BackupSqlPoolObject`, `BackupResourceId`, `SourceResourceGroupName`, `SourceWorkspaceName`, `SourceSqlPoolName`, `SourceSqlPoolObject`, `SourceResourceId`, `RestorePoint`, och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="d85fd-312">No longer supports the parameter `FromBackup`, `FromRestorePoint`, `BackupResourceGroupName`, `BackupWorkspaceName`, `BackupSqlPoolName`, `BackupSqlPoolObject`, `BackupResourceId`, `SourceResourceGroupName`, `SourceWorkspaceName`, `SourceSqlPoolName`, `SourceSqlPoolObject`, `SourceResourceId`, `RestorePoint`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="d85fd-313">Före</span><span class="sxs-lookup"><span data-stu-id="d85fd-313">Before</span></span>

```powershell
New-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupWorkspaceName ContosoWorkspace -BackupSqlPoolName ExistingContosoSqlPool
```

#### <a name="after"></a><span data-ttu-id="d85fd-314">Efter</span><span class="sxs-lookup"><span data-stu-id="d85fd-314">After</span></span>

```powershell
PS C:\> New-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c
```

### <a name="update-azsynapsesqlpool"></a><span data-ttu-id="d85fd-315">Update-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="d85fd-315">Update-AzSynapseSqlPool</span></span>

<span data-ttu-id="d85fd-316">Stöder inte längre parametrarna `Suspend`, `Resume`, och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="d85fd-316">No longer supports the parameter `Suspend`, `Resume`, and no alias was found for the original parameter name.</span></span>

## <a name="aznetwork"></a><span data-ttu-id="d85fd-317">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d85fd-317">Az.Network</span></span>

### <a name="approve-azprivateendpointconnection"></a><span data-ttu-id="d85fd-318">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d85fd-318">Approve-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="d85fd-319">Stöder inte längre parametern `PrivateLinkResourceType` och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="d85fd-319">No longer supports the parameter `PrivateLinkResourceType` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="d85fd-320">Före</span><span class="sxs-lookup"><span data-stu-id="d85fd-320">Before</span></span>

```powershell
Approve-AzPrivateEndpointConnection -ResourceGroupName xxx -ServiceName xxx -Name xxx -PrivateLinkResourceType 'Microsoft.Network/privateLinkServices' -Description xxx
```

#### <a name="after"></a><span data-ttu-id="d85fd-321">Efter</span><span class="sxs-lookup"><span data-stu-id="d85fd-321">After</span></span>

```powershell
Approve-AzPrivateEndpointConnection -ResourceGroupName xxx -ServiceName xxx -Name xxx -Description xxx
```

### <a name="deny-azprivateendpointconnection"></a><span data-ttu-id="d85fd-322">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d85fd-322">Deny-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="d85fd-323">Detsamma gäller för `Approve-AzPrivateEndpointConnection`.</span><span class="sxs-lookup"><span data-stu-id="d85fd-323">Same with `Approve-AzPrivateEndpointConnection`.</span></span>

### <a name="get-azprivateendpointconnection"></a><span data-ttu-id="d85fd-324">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d85fd-324">Get-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="d85fd-325">Detsamma gäller för `Approve-AzPrivateEndpointConnection`.</span><span class="sxs-lookup"><span data-stu-id="d85fd-325">Same with `Approve-AzPrivateEndpointConnection`.</span></span>

### <a name="remove-azprivateendpointconnection"></a><span data-ttu-id="d85fd-326">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d85fd-326">Remove-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="d85fd-327">Detsamma gäller för `Approve-AzPrivateEndpointConnection`.</span><span class="sxs-lookup"><span data-stu-id="d85fd-327">Same with `Approve-AzPrivateEndpointConnection`.</span></span>

### <a name="set-azprivateendpointconnection"></a><span data-ttu-id="d85fd-328">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d85fd-328">Set-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="d85fd-329">Detsamma gäller för `Approve-AzPrivateEndpointConnection`.</span><span class="sxs-lookup"><span data-stu-id="d85fd-329">Same with `Approve-AzPrivateEndpointConnection`.</span></span>

### <a name="new-aznetworkwatcherconnectionmonitorendpointobject"></a><span data-ttu-id="d85fd-330">New-AzNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="d85fd-330">New-AzNetworkWatcherConnectionMonitorEndpointObject</span></span>

<span data-ttu-id="d85fd-331">Stöder inte längre parametrarna `FilterType`, `FilterItem`, och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="d85fd-331">No longer supports the parameter `FilterType`, `FilterItem`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="d85fd-332">Före</span><span class="sxs-lookup"><span data-stu-id="d85fd-332">Before</span></span>

```powershell
$MySrcResourceId1 = '/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace'
$SrcEndpointFilterItem1 =New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject -Type 'AgentAddress' -Address 'WIN-P0HGNDO2S1B'
$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndPointObject -Name 'workspaceEndpoint' -ResourceId $MySrcResourceId1 -FilterType Include -FilterItem $SrcEndpointFilterItem1
```

#### <a name="after"></a><span data-ttu-id="d85fd-333">Efter</span><span class="sxs-lookup"><span data-stu-id="d85fd-333">After</span></span>

```powershell
MySrcResourceId1 = '/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace'
$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndPointObject -Name 'workspaceEndpoint' -ResourceId $MySrcResourceId1
```