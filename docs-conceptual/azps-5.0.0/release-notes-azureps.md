---
title: Viktig information om Azure PowerShell
description: Lär dig mer om alla de senaste uppdateringarna för Azure PowerShell-modulerna.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 5eac1bee53bfadf57d053ad60d6267657b145d67
ms.sourcegitcommit: 071b8c40c837ed4b2d65ce778339110d9e0899ab
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/01/2020
ms.locfileid: "96427147"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="73fd4-103">Viktig information om Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="73fd4-103">Azure PowerShell release notes</span></span>

## <a name="500---october-2020"></a><span data-ttu-id="73fd4-104">5.0.0 – Oktober 2020</span><span class="sxs-lookup"><span data-stu-id="73fd4-104">5.0.0 - October 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="73fd4-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73fd4-105">Az.Accounts</span></span>
* <span data-ttu-id="73fd4-106">[Icke-bakåtkompatibel ändring] Tog bort ”Get-AzProfile” och ”Select-AzProfile”</span><span class="sxs-lookup"><span data-stu-id="73fd4-106">[Breaking Change] Removed 'Get-AzProfile' and 'Select-AzProfile'</span></span>
* <span data-ttu-id="73fd4-107">Ersatte Azure Directory Authentication Library med Microsoft Authentication Library (MSAL)</span><span class="sxs-lookup"><span data-stu-id="73fd4-107">Replaced Azure Directory Authentication Library with Microsoft Authentication Library(MSAL)</span></span>

#### <a name="azaks"></a><span data-ttu-id="73fd4-108">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="73fd4-108">Az.Aks</span></span>
* <span data-ttu-id="73fd4-109">[Icke-bakåtkompatibel ändring] Tog bort aliaset ”ClientIdAndSecret” i ”New-AzAksCluster” och ”Set-AzAksCluster”.</span><span class="sxs-lookup"><span data-stu-id="73fd4-109">[Breaking Change] Removed parameter alias 'ClientIdAndSecret' in 'New-AzAksCluster' and 'Set-AzAksCluster'.</span></span>
* <span data-ttu-id="73fd4-110">[Icke-bakåtkompatibel ändring] Ändrade standardvärdet för ”NodeVmSetType” i ”New-AzAksCluster” från ”AvailabilitySet” till ”VirtualMachineScaleSets”.</span><span class="sxs-lookup"><span data-stu-id="73fd4-110">[Breaking Change] Changed the default value of 'NodeVmSetType' in 'New-AzAksCluster' from 'AvailabilitySet' to 'VirtualMachineScaleSets'.</span></span>
* <span data-ttu-id="73fd4-111">[Icke-bakåtkompatibel ändring] Ändrade standardvärdet för ”NetworkPlugin” i ”New-AzAksCluster” från ”None” till ”azure”.</span><span class="sxs-lookup"><span data-stu-id="73fd4-111">[Breaking Change] Changed the default value of 'NetworkPlugin' in 'New-AzAksCluster' from 'None' to 'azure'.</span></span>
* <span data-ttu-id="73fd4-112">[Icke-bakåtkompatibel ändring] Tog bort parametern ”NodeOsType” i ”New-AzAksCluster” eftersom den endast har stöd för Linux med ett värde.</span><span class="sxs-lookup"><span data-stu-id="73fd4-112">[Breaking Change] Removed parameter 'NodeOsType' in 'New-AzAksCluster' as it supports only one value Linux.</span></span>

#### <a name="azbilling"></a><span data-ttu-id="73fd4-113">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="73fd4-113">Az.Billing</span></span>
* <span data-ttu-id="73fd4-114">Lade till cmdleten ”Get-AzBillingAccount”</span><span class="sxs-lookup"><span data-stu-id="73fd4-114">Added 'Get-AzBillingAccount' cmdlet</span></span>
* <span data-ttu-id="73fd4-115">Lade till cmdleten ”Get-AzBillingProfile”</span><span class="sxs-lookup"><span data-stu-id="73fd4-115">Added 'Get-AzBillingProfile' cmdlet</span></span>
* <span data-ttu-id="73fd4-116">Lade till cmdleten ”Get-AzInvoiceSection”</span><span class="sxs-lookup"><span data-stu-id="73fd4-116">Added 'Get-AzInvoiceSection' cmdlet</span></span>
* <span data-ttu-id="73fd4-117">Lade till nya parametrar i cmdleten ”Get-AzBillingInvoice”</span><span class="sxs-lookup"><span data-stu-id="73fd4-117">Added new parameters in 'Get-AzBillingInvoice' cmdlet</span></span>
* <span data-ttu-id="73fd4-118">Tog bort egenskaperna ”DownloadUrlExpiry”, ”Type” och ”BillingPeriodNames” från svaret för cmdleten ”Get-AzBillingInvoic”</span><span class="sxs-lookup"><span data-stu-id="73fd4-118">Removed properties DownloadUrlExpiry, Type, BillingPeriodNames from the response of Get-AzBillingInvoice cmdlet</span></span>

#### <a name="azcdn"></a><span data-ttu-id="73fd4-119">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="73fd4-119">Az.Cdn</span></span>
* <span data-ttu-id="73fd4-120">Lade till cmdletar för att stödja funktioner för flera ursprung och privat länk</span><span class="sxs-lookup"><span data-stu-id="73fd4-120">Added cmdlets to support multi-origin and private link functionality</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="73fd4-121">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="73fd4-121">Az.CognitiveServices</span></span>
* <span data-ttu-id="73fd4-122">Uppdaterade SDK till 7.4.0-preview.</span><span class="sxs-lookup"><span data-stu-id="73fd4-122">Updated SDK to 7.4.0-preview.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73fd4-123">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73fd4-123">Az.Compute</span></span>
* <span data-ttu-id="73fd4-124">Lade till parametern ”-VmssId” till ”New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="73fd4-124">Added '-VmssId' parameter to 'New-AzVm'</span></span>
* <span data-ttu-id="73fd4-125">Lade till parametern ”PlatformFaultDomainCount” till cmdleten ”New-AzVmss”.</span><span class="sxs-lookup"><span data-stu-id="73fd4-125">Added 'PlatformFaultDomainCount' parameter to the 'New-AzVmss' cmdlet.</span></span>
* <span data-ttu-id="73fd4-126">Ny cmdlet: ”Get-AzDiskEncryptionSetAssociatedResource”</span><span class="sxs-lookup"><span data-stu-id="73fd4-126">New cmdlet 'Get-AzDiskEncryptionSetAssociatedResource'</span></span>
* <span data-ttu-id="73fd4-127">Lade till de valfria parametrarna ”Tier” och ”LogicalSectorSize” till cmdleten ”New-AzDiskConfig”.</span><span class="sxs-lookup"><span data-stu-id="73fd4-127">Added 'Tier' and 'LogicalSectorSize' optional parameters to the New-AzDiskConfig cmdlet.</span></span> 
* <span data-ttu-id="73fd4-128">Lade till de valfria parametrarna ”Tier”, ”MaxSharesCount”, ”DiskIOPSReadOnly” och ”DiskMBpsReadOnly” till cmdleten ”New-AzDiskUpdateConfig”.</span><span class="sxs-lookup"><span data-stu-id="73fd4-128">Added 'Tier', 'MaxSharesCount', 'DiskIOPSReadOnly', and 'DiskMBpsReadOnly' optional parameters to the 'New-AzDiskUpdateConfig' cmdlet.</span></span> 

#### <a name="azcontainerregistry"></a><span data-ttu-id="73fd4-129">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="73fd4-129">Az.ContainerRegistry</span></span>
* <span data-ttu-id="73fd4-130">[Icke-bakåtkompatibel ändring] Uppdaterar API-versionen till 2019-05-01</span><span class="sxs-lookup"><span data-stu-id="73fd4-130">[Breaking Change] Updates API version to 2019-05-01</span></span>
* <span data-ttu-id="73fd4-131">[Icke-bakåtkompatibel ändring] Tog bort SKU:n ”Classic” och parametern ”StorageAccountName” från ”New-AzContainerRegistry”</span><span class="sxs-lookup"><span data-stu-id="73fd4-131">[Breaking Change] Removed SKU 'Classic' and parameter 'StorageAccountName' from 'New-AzContainerRegistry'</span></span>
* <span data-ttu-id="73fd4-132">Lade till nya cmdletar: ”Connect-AzContainerRegistry”, ”Import-AzContainerRegistry”, ”Get-AzContainerRegistryUsage”, ”New-AzContainerRegistryNetworkRule”, ”Set-AzContainerRegistryNetworkRule”</span><span class="sxs-lookup"><span data-stu-id="73fd4-132">Added New cmdlets: 'Connect-AzContainerRegistry', 'Import-AzContainerRegistry', 'Get-AzContainerRegistryUsage', 'New-AzContainerRegistryNetworkRule', 'Set-AzContainerRegistryNetworkRule'</span></span>
* <span data-ttu-id="73fd4-133">Lade till den nya parametern ”NetworkRuleSet” till ”Update-AzContainerRegistry”</span><span class="sxs-lookup"><span data-stu-id="73fd4-133">Added new parameter 'NetworkRuleSet' to 'Update-AzContainerRegistry'</span></span>

#### <a name="azdatabricks"></a><span data-ttu-id="73fd4-134">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="73fd4-134">Az.Databricks</span></span>
* <span data-ttu-id="73fd4-135">Korrigerade en bugg som kunde leda till att en uppdatering av en Databricks-arbetsyta utan `-EncryptionKeyVersion` misslyckades.</span><span class="sxs-lookup"><span data-stu-id="73fd4-135">Fixed a bug that may cause updating databricks workspace without `-EncryptionKeyVersion` to fail.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="73fd4-136">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="73fd4-136">Az.DataFactory</span></span>
* <span data-ttu-id="73fd4-137">Uppdaterade ADF .Net SDK-versionen till 4.12.0</span><span class="sxs-lookup"><span data-stu-id="73fd4-137">Updated ADF .Net SDK version to 4.12.0</span></span>
* <span data-ttu-id="73fd4-138">Uppdaterade ADF-krypteringsklientens SDK-version till 4.14.7587.7</span><span class="sxs-lookup"><span data-stu-id="73fd4-138">Updated ADF encryption client SDK version to 4.14.7587.7</span></span>
* <span data-ttu-id="73fd4-139">Lade till kommandona ”Stop-AzDataFactoryV2TriggerRun” och ”Invoke-AzDataFactoryV2TriggerRun”</span><span class="sxs-lookup"><span data-stu-id="73fd4-139">Added 'Stop-AzDataFactoryV2TriggerRun' and 'Invoke-AzDataFactoryV2TriggerRun' commands</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="73fd4-140">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="73fd4-140">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="73fd4-141">Kräv egenskapen Plats för att skapa ARM-objekt på högsta nivån.</span><span class="sxs-lookup"><span data-stu-id="73fd4-141">Require Location property for creating top level arm objects.</span></span>
        <span data-ttu-id="73fd4-142">\* Gjorde så att `ApplicationGroupType` krävs för `New-AzWvdApplicationGroup`.</span><span class="sxs-lookup"><span data-stu-id="73fd4-142">\* Made `ApplicationGroupType` required for `New-AzWvdApplicationGroup`.</span></span>
        <span data-ttu-id="73fd4-143">\* Gjorde så att `HostPoolArmPath` krävs för `New-AzWvdApplicationGroup`.</span><span class="sxs-lookup"><span data-stu-id="73fd4-143">\* Made `HostPoolArmPath` required for `New-AzWvdApplicationGroup`.</span></span>
        <span data-ttu-id="73fd4-144">\* `PreferredAppGroupType` har lagts till för `New-AzWvdHostPool`.</span><span class="sxs-lookup"><span data-stu-id="73fd4-144">\* Added `PreferredAppGroupType` for `New-AzWvdHostPool`.</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="73fd4-145">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="73fd4-145">Az.Functions</span></span>
* <span data-ttu-id="73fd4-146">[Icke-bakåtkompatibel ändring] Tog bort växelparametern ”IncludeSlot” från alla förutom en parameteruppsättning i ”Get-AzFunctionApp”.</span><span class="sxs-lookup"><span data-stu-id="73fd4-146">[Breaking Change] Removed 'IncludeSlot' switch parameter from all but one parameter set of 'Get-AzFunctionApp'.</span></span> <span data-ttu-id="73fd4-147">Cmdleten stöder nu hämtning av distributionsfack i resultaten när ”-IncludeSlot” anges.</span><span class="sxs-lookup"><span data-stu-id="73fd4-147">The cmdlet now supports retrieving deployment slots in the results when '-IncludeSlot' is specified.</span></span> 
* <span data-ttu-id="73fd4-148">Uppdaterade ”New-AzFunctionApp”:</span><span class="sxs-lookup"><span data-stu-id="73fd4-148">Updated 'New-AzFunctionApp':</span></span>
  - <span data-ttu-id="73fd4-149">Korrigerade ”-DisableApplicationInsights” så att inga Application Insights-projekt skapas när det här alternativet har angetts.</span><span class="sxs-lookup"><span data-stu-id="73fd4-149">Fixed -DisableApplicationInsights so that no application insights project is created when this option is specified.</span></span> <span data-ttu-id="73fd4-150">[#12728]</span><span class="sxs-lookup"><span data-stu-id="73fd4-150">[#12728]</span></span>
  - <span data-ttu-id="73fd4-151">[Icke-bakåtkompatibel ändring] Tog bort stöd för att skapa PowerShell 6.2-funktionsappar.</span><span class="sxs-lookup"><span data-stu-id="73fd4-151">[Breaking Change] Removed support to create PowerShell 6.2 function apps.</span></span>
  - <span data-ttu-id="73fd4-152">[Icke-bakåtkompatibel ändring] Ändrade körningsversionen som är standard i Functions version 3 i Windows för PowerShell-funktionsappar från 6.2 till 7.0 när parametern RuntimeVersion inte har angetts.</span><span class="sxs-lookup"><span data-stu-id="73fd4-152">[Breaking Change] Changed the default runtime version in Functions version 3 on Windows for PowerShell function apps from 6.2 to 7.0 when the RuntimeVersion parameter is not specified.</span></span>
  - <span data-ttu-id="73fd4-153">[Icke-bakåtkompatibel ändring] Ändrade körningsversionen som är standard i Functions version 3 i Windows och Linux för Node-funktionsappar från 10 till 12 när parametern RuntimeVersion inte har angetts.</span><span class="sxs-lookup"><span data-stu-id="73fd4-153">[Breaking Change] Changed the default runtime version in Functions version 3 on Windows and Linux for Node function apps from 10 to 12 when the RuntimeVersion parameter is not specified.</span></span>
  - <span data-ttu-id="73fd4-154">[Icke-bakåtkompatibel ändring] Ändrade körningsversionen som är standard i Functions version 3 i Linux för Python-funktionsappar från 3.7 till 3.8 när parametern RuntimeVersion inte har angetts.</span><span class="sxs-lookup"><span data-stu-id="73fd4-154">[Breaking Change] Changed the default runtime version in Functions version 3 on Linux for Python function apps from 3.7 to 3.8 when the RuntimeVersion parameter is not specified.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="73fd4-155">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="73fd4-155">Az.HDInsight</span></span>
 * <span data-ttu-id="73fd4-156">För cmdleten New-AzHDInsightCluster:</span><span class="sxs-lookup"><span data-stu-id="73fd4-156">For New-AzHDInsightCluster cmdlet:</span></span>
     - <span data-ttu-id="73fd4-157">Ersatte parametern ”DefaultStorageAccountName” med ”StorageAccountResourceId”</span><span class="sxs-lookup"><span data-stu-id="73fd4-157">Replaced parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
     - <span data-ttu-id="73fd4-158">Ersatte parametern ”DefaultStorageAccountKey” med ”StorageAccountKey”</span><span class="sxs-lookup"><span data-stu-id="73fd4-158">Replaced parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
     - <span data-ttu-id="73fd4-159">Ersatte parametern ”DefaultStorageAccountType” med ”StorageAccountType”</span><span class="sxs-lookup"><span data-stu-id="73fd4-159">Replaced parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
     - <span data-ttu-id="73fd4-160">Tog bort parametern ”PublicNetworkAccessType”</span><span class="sxs-lookup"><span data-stu-id="73fd4-160">Removed parameter 'PublicNetworkAccessType'</span></span>
     - <span data-ttu-id="73fd4-161">Ta bort parametern ”OutboundPublicNetworkAccessType”</span><span class="sxs-lookup"><span data-stu-id="73fd4-161">Removed parameter 'OutboundPublicNetworkAccessType'</span></span>
     - <span data-ttu-id="73fd4-162">Lade till nya parametrar: ”StorageFileSystem” och ”StorageAccountManagedIdentity” för att stödja ADLSGen2</span><span class="sxs-lookup"><span data-stu-id="73fd4-162">Added new parameters: 'StorageFileSystem' and 'StorageAccountManagedIdentity' to support ADLSGen2</span></span>
     - <span data-ttu-id="73fd4-163">Lade till den nya parametern ”EnableIDBroker” för att stödja ID-förmedlaren i HDInsight</span><span class="sxs-lookup"><span data-stu-id="73fd4-163">Added new parameter 'EnableIDBroker' to Support HDInsight ID Broker</span></span>
     - <span data-ttu-id="73fd4-164">Lade till nya parametrar: ”KafkaClientGroupId”, ”KafkaClientGroupName” och ”KafkaManagementNodeSize” för att stödja Kafka REST-proxy</span><span class="sxs-lookup"><span data-stu-id="73fd4-164">Added new parameters: 'KafkaClientGroupId', 'KafkaClientGroupName' and 'KafkaManagementNodeSize' to support Kafka Rest Proxy</span></span>
 * <span data-ttu-id="73fd4-165">För cmdleten New-AzHDInsightClusterConfig:</span><span class="sxs-lookup"><span data-stu-id="73fd4-165">For New-AzHDInsightClusterConfig cmdlet:</span></span>
     - <span data-ttu-id="73fd4-166">Ersatte parametern ”DefaultStorageAccountName” med ”StorageAccountResourceId”</span><span class="sxs-lookup"><span data-stu-id="73fd4-166">Replaced parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
     - <span data-ttu-id="73fd4-167">Ersatte parametern ”DefaultStorageAccountKey” med ”StorageAccountKey”</span><span class="sxs-lookup"><span data-stu-id="73fd4-167">Replaced parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
     - <span data-ttu-id="73fd4-168">Ersatte parametern ”DefaultStorageAccountType” med ”StorageAccountType”</span><span class="sxs-lookup"><span data-stu-id="73fd4-168">Replaced parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
     - <span data-ttu-id="73fd4-169">Tog bort parametern ”PublicNetworkAccessType”</span><span class="sxs-lookup"><span data-stu-id="73fd4-169">Removed parameter 'PublicNetworkAccessType'</span></span>
     - <span data-ttu-id="73fd4-170">Ta bort parametern ”OutboundPublicNetworkAccessType”</span><span class="sxs-lookup"><span data-stu-id="73fd4-170">Removed parameter 'OutboundPublicNetworkAccessType'</span></span>
* <span data-ttu-id="73fd4-171">För cmdleten Set-AzHDInsightDefaultStorage:</span><span class="sxs-lookup"><span data-stu-id="73fd4-171">For Set-AzHDInsightDefaultStorage cmdlet:</span></span>
    - <span data-ttu-id="73fd4-172">Ersatte parametern ”StorageAccountName” med ”StorageAccountResourceId”</span><span class="sxs-lookup"><span data-stu-id="73fd4-172">Replaced parameter 'StorageAccountName' with 'StorageAccountResourceId'</span></span>
* <span data-ttu-id="73fd4-173">För cmdleten Add-AzHDInsightSecurityProfile:</span><span class="sxs-lookup"><span data-stu-id="73fd4-173">For Add-AzHDInsightSecurityProfile cmdlet:</span></span>
    - <span data-ttu-id="73fd4-174">Ersatte parametern ”Domain” med ”DomainResourceId”</span><span class="sxs-lookup"><span data-stu-id="73fd4-174">Replaced parameter 'Domain' with 'DomainResourceId'</span></span>
    - <span data-ttu-id="73fd4-175">Tog bort det obligatoriska kravet för parametern ”OrganizationalUnitDN”</span><span class="sxs-lookup"><span data-stu-id="73fd4-175">Removed the mandatory requirement for parameter 'OrganizationalUnitDN'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="73fd4-176">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="73fd4-176">Az.KeyVault</span></span>
* <span data-ttu-id="73fd4-177">[Icke-bakåtkompatibel ändring] Parametrarna DisableSoftDelete i ”New-AzKeyVault” och EnableSoftDelete i ”Update-AzKeyVault” har gjorts inaktuella</span><span class="sxs-lookup"><span data-stu-id="73fd4-177">[Breaking Change] Deprecated parameter DisableSoftDelete in 'New-AzKeyVault' and EnableSoftDelete in 'Update-AzKeyVault'</span></span>
* <span data-ttu-id="73fd4-178">[Icke-bakåtkompatibel ändring] Tog bort attributet SecretValueText för att undvika att SecretValue visas direkt [#12266]</span><span class="sxs-lookup"><span data-stu-id="73fd4-178">[Breaking Change] Removed attribute SecretValueText to avoid displaying SecretValue directly [#12266]</span></span>
* <span data-ttu-id="73fd4-179">Stöd för ny resurstyp: hanterad HSM</span><span class="sxs-lookup"><span data-stu-id="73fd4-179">Supported new resource type: managed HSM</span></span>
    - <span data-ttu-id="73fd4-180">CRUD för hanterad HSM och cmdleter för att köra nycklar på hanterad HSM</span><span class="sxs-lookup"><span data-stu-id="73fd4-180">CRUD of managed HSM and cmdlets to operate keys on managed HSM</span></span>
    - <span data-ttu-id="73fd4-181">Fullständig HSM-säkerhetskopiering/återställning, skapande av AES-nyckel, säkerhetskopiering/återställning av domän, RBAC</span><span class="sxs-lookup"><span data-stu-id="73fd4-181">Full HSM backup/restore, AES key creation, security domain backup/restore, RBAC</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="73fd4-182">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="73fd4-182">Az.ManagedServices</span></span>
* <span data-ttu-id="73fd4-183">[Icke-bakåtkompatibel ändring] Uppdaterade namngivningskonventioner för parametrar och associerade exempel</span><span class="sxs-lookup"><span data-stu-id="73fd4-183">[Breaking Change] Updated parameters naming conventions and associated examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73fd4-184">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73fd4-184">Az.Network</span></span>
* <span data-ttu-id="73fd4-185">[Icke-bakåtkompatibel ändring] Tog bort parametern ”HostedSubnet” och lade till ”Subnet” i stället</span><span class="sxs-lookup"><span data-stu-id="73fd4-185">[Breaking Change] Removed parameter 'HostedSubnet' and added 'Subnet' instead</span></span>
* <span data-ttu-id="73fd4-186">Lade till nya cmdletar för peeringvägar för virtuella routrar</span><span class="sxs-lookup"><span data-stu-id="73fd4-186">Added new cmdlets for Virtual Router Peer Routes</span></span>
    - <span data-ttu-id="73fd4-187">”Get-AzVirtualRouterPeerLearnedRoute”</span><span class="sxs-lookup"><span data-stu-id="73fd4-187">'Get-AzVirtualRouterPeerLearnedRoute'</span></span>
    - <span data-ttu-id="73fd4-188">”Get-AzVirtualRouterPeerAdvertisedRoute”</span><span class="sxs-lookup"><span data-stu-id="73fd4-188">'Get-AzVirtualRouterPeerAdvertisedRoute'</span></span>
* <span data-ttu-id="73fd4-189">Cmdleten New-AzFirewall har uppdaterats:</span><span class="sxs-lookup"><span data-stu-id="73fd4-189">Updated New-AzFirewall cmdlet:</span></span>
    - <span data-ttu-id="73fd4-190">Lade till parametern ”-SkuTier”</span><span class="sxs-lookup"><span data-stu-id="73fd4-190">Added parameter '-SkuTier'</span></span>
    - <span data-ttu-id="73fd4-191">Lade till parametern ”-SkuName” och gjorde Sku till ett alias för den</span><span class="sxs-lookup"><span data-stu-id="73fd4-191">Added parameter '-SkuName' and made Sku as Alias for this</span></span>
    - <span data-ttu-id="73fd4-192">Tog bort parametern ”-Sku”</span><span class="sxs-lookup"><span data-stu-id="73fd4-192">Removed parameter '-Sku'</span></span>
* <span data-ttu-id="73fd4-193">[Icke-bakåtkompatibel ändring] Gjorde argumentet ”Connectionlink” obligatoriskt i ”Start-AzVpnConnectionPacketCapture” och ”Stop-AzVpnConnectionPacketCapture”</span><span class="sxs-lookup"><span data-stu-id="73fd4-193">[Breaking Change] Made 'Connectionlink' argument mandatory in 'Start-AzVpnConnectionPacketCapture' and 'Stop-AzVpnConnectionPacketCapture'</span></span>
* <span data-ttu-id="73fd4-194">[Icke-bakåtkompatibel ändring] Uppdaterade ”New-AzNetworkWatcherConnectionMonitorEndPointObject” för att ta bort parametern ”-Filter”</span><span class="sxs-lookup"><span data-stu-id="73fd4-194">[Breaking Change] Updated 'New-AzNetworkWatcherConnectionMonitorEndPointObject' to remove parameter '-Filter'</span></span>
* <span data-ttu-id="73fd4-195">[Icke-bakåtkompatibel ändring] Ersatte cmdleten ”New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject” med ”New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject”</span><span class="sxs-lookup"><span data-stu-id="73fd4-195">[Breaking Change] Replaced 'New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject' cmdlet with 'New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject'</span></span>
* <span data-ttu-id="73fd4-196">Uppdaterade cmdleten ”New-AzNetworkWatcherConnectionMonitorEndPointObject”:</span><span class="sxs-lookup"><span data-stu-id="73fd4-196">Updated 'New-AzNetworkWatcherConnectionMonitorEndPointObject' cmdlet:</span></span>
    - <span data-ttu-id="73fd4-197">Lade till parametern ”-Type”</span><span class="sxs-lookup"><span data-stu-id="73fd4-197">Added parameter '-Type'</span></span>
    - <span data-ttu-id="73fd4-198">Lade till parametern ”-CoverageLevel”</span><span class="sxs-lookup"><span data-stu-id="73fd4-198">Added parameter '-CoverageLevel'</span></span>
    - <span data-ttu-id="73fd4-199">Lade till parametern ”-Scope”</span><span class="sxs-lookup"><span data-stu-id="73fd4-199">Added parameter '-Scope'</span></span>
* <span data-ttu-id="73fd4-200">Uppdaterade cmdleten ”New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject” med den nya parametern ”-DestinationPortBehavior”</span><span class="sxs-lookup"><span data-stu-id="73fd4-200">Updated 'New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject' cmdlet with new parameter '-DestinationPortBehavior'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="73fd4-201">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="73fd4-201">Az.RecoveryServices</span></span>
* <span data-ttu-id="73fd4-202">Korrigerar återställning av arbetsbelastningar för behörigheter för deltagare.</span><span class="sxs-lookup"><span data-stu-id="73fd4-202">Fixing Workload Restore for contributor permissions.</span></span>
* <span data-ttu-id="73fd4-203">Lade till nya parameteruppsättningar och valideringar för cmdleten ”Restore-AzRecoveryServicesBackupItem”.</span><span class="sxs-lookup"><span data-stu-id="73fd4-203">Added new parameter sets and validations for Restore-AzRecoveryServicesBackupItem cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="73fd4-204">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73fd4-204">Az.Resources</span></span>
* <span data-ttu-id="73fd4-205">Korrigerade en bugg vid parsning</span><span class="sxs-lookup"><span data-stu-id="73fd4-205">Fixed parsing bug</span></span>
* <span data-ttu-id="73fd4-206">Uppdaterade What-If-cmdletar i ARM-mall för att ta bort förhandsgranskningsmeddelandet från resultaten</span><span class="sxs-lookup"><span data-stu-id="73fd4-206">Updated ARM template What-If cmdlets to remove preview message from results</span></span>
* <span data-ttu-id="73fd4-207">Korrigerade ett problem där cmdletar för mall-distribution kraschar om ”-WhatIf” har ställts in på ett högre omfång [#13038]</span><span class="sxs-lookup"><span data-stu-id="73fd4-207">Fixed an issue where template deployment cmdlets crash if '-WhatIf' is set at a higher scope [#13038]</span></span>
* <span data-ttu-id="73fd4-208">Korrigerade ett problem där cmdletar för malldistribution inte bevarar skiftläget för mallparametrar</span><span class="sxs-lookup"><span data-stu-id="73fd4-208">Fixed an issue where template deployment cmdlets does not preserve case for template parameters</span></span>
* <span data-ttu-id="73fd4-209">Lade till en standard-API-version som kan användas i cmdleten ”Export-AzResourceGroup”</span><span class="sxs-lookup"><span data-stu-id="73fd4-209">Added a default API version to be used in 'Export-AzResourceGroup' cmdlet</span></span>
* <span data-ttu-id="73fd4-210">Lade till cmdletar för mallspecifikationer (”Get-AzTemplateSpec”, ”Set-AzTemplateSpec”, ”New-AzTemplateSpec”, ”Remove-AzTemplateSpec”, ”Export-AzTemplateSpec”)</span><span class="sxs-lookup"><span data-stu-id="73fd4-210">Added cmdlets for Template Specs ('Get-AzTemplateSpec', 'Set-AzTemplateSpec', 'New-AzTemplateSpec', 'Remove-AzTemplateSpec', 'Export-AzTemplateSpec')</span></span>
* <span data-ttu-id="73fd4-211">Lade till stöd för att distribuera mallspecifikationer med befintliga cmdletar för distribution (via den nya parametern ”-TemplateSpecId”)</span><span class="sxs-lookup"><span data-stu-id="73fd4-211">Added support for deploying Template Specs using existing deployment cmdlets (via the new -TemplateSpecId parameter)</span></span> 
* <span data-ttu-id="73fd4-212">Uppdaterade ”Get-AzResourceGroupDeploymentOperation” för att använda SDK.</span><span class="sxs-lookup"><span data-stu-id="73fd4-212">Updated 'Get-AzResourceGroupDeploymentOperation' to use the SDK.</span></span>
* <span data-ttu-id="73fd4-213">Tog bort parametern ”ApiVersion” från cmdletarna ”\*-AzDeployment”.</span><span class="sxs-lookup"><span data-stu-id="73fd4-213">Removed '-ApiVersion' parameter from '\*-AzDeployment' cmdlets.</span></span>

#### <a name="azsql"></a><span data-ttu-id="73fd4-214">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73fd4-214">Az.Sql</span></span>
* <span data-ttu-id="73fd4-215">Korrigerade ett problem där New-AzSqlDatabaseExport misslyckas om networkIsolation inte har angetts [#13097]</span><span class="sxs-lookup"><span data-stu-id="73fd4-215">Fixed issue where New-AzSqlDatabaseExport fails if networkIsolation not specified [#13097]</span></span>
* <span data-ttu-id="73fd4-216">Korrigerade ett problem där New-AzSqlDatabaseExport och New-AzSqlDatabaseImport inte returnerade OperationStatusLink i resultatobjektet [#13097]</span><span class="sxs-lookup"><span data-stu-id="73fd4-216">Fixed issue where New-AzSqlDatabaseExport and New-AzSqlDatabaseImport were not returning OperationStatusLink in the result object [#13097]</span></span>
* <span data-ttu-id="73fd4-217">Uppdatera webbadresser för Azure-kopplade regioner i redundansvarningar för Backup Storage</span><span class="sxs-lookup"><span data-stu-id="73fd4-217">Update Azure Paired Regions URL in Backup Storage Redundancy Warnings</span></span> 

#### <a name="azstorage"></a><span data-ttu-id="73fd4-218">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="73fd4-218">Az.Storage</span></span>
* <span data-ttu-id="73fd4-219">Tog bort den föråldrade egenskapen RestorePolicy.LastEnabledTime</span><span class="sxs-lookup"><span data-stu-id="73fd4-219">Removed obsolete property RestorePolicy.LastEnabledTime</span></span>
    - <span data-ttu-id="73fd4-220">"Enable-AzStorageBlobRestorePolicy"</span><span class="sxs-lookup"><span data-stu-id="73fd4-220">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="73fd4-221">"Disable-AzStorageBlobRestorePolicy"</span><span class="sxs-lookup"><span data-stu-id="73fd4-221">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="73fd4-222">”Get-AzStorageBlobServiceProperty”</span><span class="sxs-lookup"><span data-stu-id="73fd4-222">'Get-AzStorageBlobServiceProperty'</span></span>
    - <span data-ttu-id="73fd4-223">”Update-AzStorageBlobServiceProperty”</span><span class="sxs-lookup"><span data-stu-id="73fd4-223">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="73fd4-224">Vill du ändra typen av DaysAfterModificationGreaterThan från int till int?</span><span class="sxs-lookup"><span data-stu-id="73fd4-224">Change Type of DaysAfterModificationGreaterThan from int to int?</span></span>
    - <span data-ttu-id="73fd4-225">"Set-AzStorageAccountManagementPolicy"</span><span class="sxs-lookup"><span data-stu-id="73fd4-225">'Set-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="73fd4-226">"Get-AzStorageAccountManagementPolicy"</span><span class="sxs-lookup"><span data-stu-id="73fd4-226">'Get-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="73fd4-227">"Add-AzStorageAccountManagementPolicyAction"</span><span class="sxs-lookup"><span data-stu-id="73fd4-227">'Add-AzStorageAccountManagementPolicyAction'</span></span>
    - <span data-ttu-id="73fd4-228">"New-AzStorageAccountManagementPolicyRule"</span><span class="sxs-lookup"><span data-stu-id="73fd4-228">'New-AzStorageAccountManagementPolicyRule'</span></span>
* <span data-ttu-id="73fd4-229">Stöd för skapa/uppdatera filresurs med åtkomstnivå</span><span class="sxs-lookup"><span data-stu-id="73fd4-229">Supported create/update file share with access tier</span></span>
    - <span data-ttu-id="73fd4-230">”New-AzRmStorageShare”</span><span class="sxs-lookup"><span data-stu-id="73fd4-230">'New-AzRmStorageShare'</span></span>
    - <span data-ttu-id="73fd4-231">”Update-AzRmStorageShare”</span><span class="sxs-lookup"><span data-stu-id="73fd4-231">'Update-AzRmStorageShare'</span></span>
* <span data-ttu-id="73fd4-232">Stöd för att konfigurera/uppdatera/ta bort ACL som stöds rekursivt på Datalake Gen2-objekt</span><span class="sxs-lookup"><span data-stu-id="73fd4-232">Supported set/update/remove Acl recursively on Datalake Gen2 item</span></span> 
    -  <span data-ttu-id="73fd4-233">”Set-AzDataLakeGen2AclRecursive”</span><span class="sxs-lookup"><span data-stu-id="73fd4-233">'Set-AzDataLakeGen2AclRecursive'</span></span> 
    -  <span data-ttu-id="73fd4-234">”Update-AzDataLakeGen2AclRecursive”</span><span class="sxs-lookup"><span data-stu-id="73fd4-234">'Update-AzDataLakeGen2AclRecursive'</span></span> 
    -  <span data-ttu-id="73fd4-235">”Remove-AzDataLakeGen2AclRecursive”</span><span class="sxs-lookup"><span data-stu-id="73fd4-235">'Remove-AzDataLakeGen2AclRecursive'</span></span>
* <span data-ttu-id="73fd4-236">Stöd för åtkomstprincip för containrar med de nya behörigheterna x, t</span><span class="sxs-lookup"><span data-stu-id="73fd4-236">Supported Container access policy with new permission x,t</span></span>
    -  <span data-ttu-id="73fd4-237">”New-AzStorageContainerStoredAccessPolicy”</span><span class="sxs-lookup"><span data-stu-id="73fd4-237">'New-AzStorageContainerStoredAccessPolicy'</span></span>
    -  <span data-ttu-id="73fd4-238">"Set-AzStorageContainerStoredAccessPolicy"</span><span class="sxs-lookup"><span data-stu-id="73fd4-238">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
* <span data-ttu-id="73fd4-239">Ändrade utdata från cmdleten hämta/ange åtkomstprincip för containrar genom att ändra behörighetstypen för den underordnade egenskapen från uppräkning till sträng</span><span class="sxs-lookup"><span data-stu-id="73fd4-239">Changed the output of get/set Container access policy cmdlet, by change the child property Permission type from enum to String</span></span>
    -  <span data-ttu-id="73fd4-240">"Get-AzStorageContainerStoredAccessPolicy"</span><span class="sxs-lookup"><span data-stu-id="73fd4-240">'Get-AzStorageContainerStoredAccessPolicy'</span></span>
    -  <span data-ttu-id="73fd4-241">"Set-AzStorageContainerStoredAccessPolicy"</span><span class="sxs-lookup"><span data-stu-id="73fd4-241">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
* <span data-ttu-id="73fd4-242">Korrigerade ett problem med exempelskript för att ange hanteringsprincip med JSON</span><span class="sxs-lookup"><span data-stu-id="73fd4-242">Fixed a sample script issue of set management policy with json</span></span>
    -  <span data-ttu-id="73fd4-243">"Set-AzStorageAccountManagementPolicy"</span><span class="sxs-lookup"><span data-stu-id="73fd4-243">'Set-AzStorageAccountManagementPolicy'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="73fd4-244">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="73fd4-244">Az.Websites</span></span>
* <span data-ttu-id="73fd4-245">Lade till stöd för Premium V3-prisnivån</span><span class="sxs-lookup"><span data-stu-id="73fd4-245">Added support for Premium V3 pricing tier</span></span>
* <span data-ttu-id="73fd4-246">Uppdaterade SDK för WebSites till 3.1.0</span><span class="sxs-lookup"><span data-stu-id="73fd4-246">Updated the WebSites SDK to 3.1.0</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="73fd4-247">Tack till våra community-deltagare</span><span class="sxs-lookup"><span data-stu-id="73fd4-247">Thanks to our community contributors</span></span>
* <span data-ttu-id="73fd4-248">@atul-ram, uppdatera Get-AzDelegation.md (#13176)</span><span class="sxs-lookup"><span data-stu-id="73fd4-248">@atul-ram, Update Get-AzDelegation.md (#13176)</span></span>
* <span data-ttu-id="73fd4-249">@dineshreddy007, hämta approller som har tilldelats korrekt om Stack HCI-registrering använder WAC-token.</span><span class="sxs-lookup"><span data-stu-id="73fd4-249">@dineshreddy007, Get the App Roles assigned correctly in case of Stack HCI registration using WAC token.</span></span> <span data-ttu-id="73fd4-250">(#13249)</span><span class="sxs-lookup"><span data-stu-id="73fd4-250">(#13249)</span></span>
* <span data-ttu-id="73fd4-251">@kongou-ae, uppdatera New-AzOffice365PolicyProperty.md (#13217)</span><span class="sxs-lookup"><span data-stu-id="73fd4-251">@kongou-ae, Update New-AzOffice365PolicyProperty.md (#13217)</span></span>
* <span data-ttu-id="73fd4-252">Lohith Chowdary Chilukuri (@Lochiluk), uppdatera Set-AzApplicationGateway.md (#13150)</span><span class="sxs-lookup"><span data-stu-id="73fd4-252">Lohith Chowdary Chilukuri (@Lochiluk), Update Set-AzApplicationGateway.md (#13150)</span></span>
* <span data-ttu-id="73fd4-253">Matthew Burleigh (@mburleigh)</span><span class="sxs-lookup"><span data-stu-id="73fd4-253">Matthew Burleigh (@mburleigh)</span></span>
  * <span data-ttu-id="73fd4-254">Lägg till länkar till de PowerShell-cmdletar som refereras i dokumentet (#13203)</span><span class="sxs-lookup"><span data-stu-id="73fd4-254">Add links to PowerShell cmdlets referenced in the document (#13203)</span></span>
  * <span data-ttu-id="73fd4-255">Lägg till länkar till de PowerShell-cmdletar som refereras i dokumentet (#13190)</span><span class="sxs-lookup"><span data-stu-id="73fd4-255">Add links to PowerShell cmdlets referenced in the document (#13190)</span></span>
  * <span data-ttu-id="73fd4-256">Lägg till länkar till de PowerShell-cmdletar som refereras i dokumentet (#13189)</span><span class="sxs-lookup"><span data-stu-id="73fd4-256">Add links to PowerShell cmdlets referenced in the document (#13189)</span></span>
  * <span data-ttu-id="73fd4-257">lägg till länkar till cmdletar som refereras (#13137)</span><span class="sxs-lookup"><span data-stu-id="73fd4-257">add links to referenced cmdlets (#13137)</span></span>
  * <span data-ttu-id="73fd4-258">Lägg till länkar till de PowerShell-cmdletar som refereras i dokumentet (#13204)</span><span class="sxs-lookup"><span data-stu-id="73fd4-258">Add links to PowerShell cmdlets referenced in the document (#13204)</span></span>
  * <span data-ttu-id="73fd4-259">Lägg till länkar till de PowerShell-cmdletar som refereras i dokumentet (#13205)</span><span class="sxs-lookup"><span data-stu-id="73fd4-259">Add links to PowerShell cmdlets referenced in the document (#13205)</span></span>

## <a name="480---october-2020"></a><span data-ttu-id="73fd4-260">4.8.0 – oktober 2020</span><span class="sxs-lookup"><span data-stu-id="73fd4-260">4.8.0 - October 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="73fd4-261">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73fd4-261">Az.Accounts</span></span>
* <span data-ttu-id="73fd4-262">Åtgärdat DateTime-parsningsfel i vanliga bibliotek [#13045]</span><span class="sxs-lookup"><span data-stu-id="73fd4-262">Fixed DateTime parse issue in common libraries [#13045]</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="73fd4-263">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="73fd4-263">Az.CognitiveServices</span></span>
* <span data-ttu-id="73fd4-264">Cmdleten New-AzCognitiveServicesAccountApiProperty har lagts till.</span><span class="sxs-lookup"><span data-stu-id="73fd4-264">Added 'New-AzCognitiveServicesAccountApiProperty' cmdlet.</span></span>
* <span data-ttu-id="73fd4-265">Stöd för parametern ApiProperty för New-AzCognitiveServicesAccount och Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="73fd4-265">Supported 'ApiProperty' parameter for 'New-AzCognitiveServicesAccount' and 'Set-AzCognitiveServicesAccount'</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73fd4-266">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73fd4-266">Az.Compute</span></span>
* <span data-ttu-id="73fd4-267">Åtgärdat problem i Update-ASRRecoveryPlan genom att fylla i FailoverTypes</span><span class="sxs-lookup"><span data-stu-id="73fd4-267">Fixed issue in 'Update-ASRRecoveryPlan' by populating FailoverTypes</span></span>
* <span data-ttu-id="73fd4-268">De valfria parametrarna -Top och -OrderBy har lagts till i cmdleten Get-AzVmImage.</span><span class="sxs-lookup"><span data-stu-id="73fd4-268">Added the '-Top' and '-OrderBy' optional parameters to the 'Get-AzVmImage' cmdlet.</span></span> 

#### <a name="azdatabricks"></a><span data-ttu-id="73fd4-269">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="73fd4-269">Az.Databricks</span></span>
* <span data-ttu-id="73fd4-270">Allmän tillgänglighet för modulen Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="73fd4-270">General availability of 'Az.Databricks' module</span></span>
* <span data-ttu-id="73fd4-271">Stöd har lagts till för virtuell nätverkspeering</span><span class="sxs-lookup"><span data-stu-id="73fd4-271">Added support for virtual network peering</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="73fd4-272">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="73fd4-272">Az.DataFactory</span></span>
* <span data-ttu-id="73fd4-273">Skrivfel har åtgärdats i utdatameddelanden</span><span class="sxs-lookup"><span data-stu-id="73fd4-273">Fixed typo in output messages</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="73fd4-274">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="73fd4-274">Az.EventHub</span></span>
* <span data-ttu-id="73fd4-275">Den valfria switchparametern TrustedServiceAccessEnabled har lagts till i cmdleten Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="73fd4-275">Added optional switch parameter 'TrustedServiceAccessEnabled' to 'Set-AzEventHubNetworkRuleSet' cmdlet</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="73fd4-276">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="73fd4-276">Az.HDInsight</span></span>
* <span data-ttu-id="73fd4-277">Ett varningsmeddelande om att parametrarna PublicNetworkAccessType och OutboundPublicNetworkAccessType planeras att göras inaktuella har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-277">Added warning message for planning to deprecate the parameters 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType'</span></span>
* <span data-ttu-id="73fd4-278">Ett varningsmeddelande om att parametern DefaultStorageAccountName planeras att ersättas med StorageAccountResourceId har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-278">Added warning message for planning to replace the parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
* <span data-ttu-id="73fd4-279">Ett varningsmeddelande om att parametern DefaultStorageAccountKey planeras att ersättas med StorageAccountKey har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-279">Added warning message for planning to replace the parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
* <span data-ttu-id="73fd4-280">Ett varningsmeddelande om att parametern DefaultStorageAccountType planeras att ersättas med StorageAccountType har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-280">Added warning message for planning to replace the parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
* <span data-ttu-id="73fd4-281">Ett varningsmeddelande om att parametern DefaultStorageContainer planeras att ersättas med StorageContainer har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-281">Added warning message for planning to replace the parameter 'DefaultStorageContainer' with 'StorageContainer'</span></span>
* <span data-ttu-id="73fd4-282">Ett varningsmeddelande om att parametern DefaultStorageRootPath planeras att ersättas med StorageRootPath har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-282">Added warning message for planning to replace the parameter 'DefaultStorageRootPath' with 'StorageRootPath'</span></span>

#### <a name="aziothub"></a><span data-ttu-id="73fd4-283">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="73fd4-283">Az.IotHub</span></span>
* <span data-ttu-id="73fd4-284">SDK för enheter har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="73fd4-284">Updated devices sdk.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="73fd4-285">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="73fd4-285">Az.KeyVault</span></span>
* <span data-ttu-id="73fd4-286">Detaljerat datum för borttagning av egenskapen SecretValueText har tillhandahållits</span><span class="sxs-lookup"><span data-stu-id="73fd4-286">Provided the detailed date of removing property SecretValueText</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="73fd4-287">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="73fd4-287">Az.ManagedServices</span></span>
* <span data-ttu-id="73fd4-288">Varningar om icke-bakåtkompatibla ändringar för cmdletar för tilldelning och definition av hanterade tjänster har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="73fd4-288">Updated breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="73fd4-289">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="73fd4-289">Az.Monitor</span></span>
* <span data-ttu-id="73fd4-290">Felet som gjorde att ett varningsmeddelande inte kunde ignoreras har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="73fd4-290">Fixed the bug that warning message cannot be suppressed.</span></span> <span data-ttu-id="73fd4-291">[#12889]</span><span class="sxs-lookup"><span data-stu-id="73fd4-291">[#12889]</span></span>
* <span data-ttu-id="73fd4-292">Stöd för parametern SkipMetricValidation i aviseringsregelvillkor.</span><span class="sxs-lookup"><span data-stu-id="73fd4-292">Supported 'SkipMetricValidation' parameter in alert rule criteria.</span></span> <span data-ttu-id="73fd4-293">Tillåter att du skapar en aviseringsregel för ett anpassat mått som inte har genererats än, genom att göra så att måttverifieringen hoppas över.</span><span class="sxs-lookup"><span data-stu-id="73fd4-293">Allows creating an alert rule on a custom metric that isn't yet emitted, by causing the metric validation to be skipped.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73fd4-294">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73fd4-294">Az.Network</span></span>
* <span data-ttu-id="73fd4-295">Office365-princip har lagts till för VPNSite-resurs</span><span class="sxs-lookup"><span data-stu-id="73fd4-295">Added Office365 Policy to VPNSite Resource</span></span>
    - <span data-ttu-id="73fd4-296">New-AzO365PolicyProperty</span><span class="sxs-lookup"><span data-stu-id="73fd4-296">'New-AzO365PolicyProperty'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="73fd4-297">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="73fd4-297">Az.RecoveryServices</span></span>
* <span data-ttu-id="73fd4-298">Verifiering av containernamn har lagts till för arbetsbelastningssäkerhetskopior.</span><span class="sxs-lookup"><span data-stu-id="73fd4-298">Added container name validation for workload backup.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="73fd4-299">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="73fd4-299">Az.RedisCache</span></span>
* <span data-ttu-id="73fd4-300">En korrigering har gjorts så att cmdletarna New-AzRedisCache och Set-AzRedisCache inte misslyckas på grund av behörighetsproblem som rör registrering av Microsoft.Cache RP</span><span class="sxs-lookup"><span data-stu-id="73fd4-300">Made 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets not fail because of permission issue related to registering Microsoft.Cache RP</span></span>

#### <a name="azsql"></a><span data-ttu-id="73fd4-301">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73fd4-301">Az.Sql</span></span>
* <span data-ttu-id="73fd4-302">BackupStorageRedundancy har lagts till i:</span><span class="sxs-lookup"><span data-stu-id="73fd4-302">Added BackupStorageRedundancy to the following:</span></span> 
    - <span data-ttu-id="73fd4-303">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="73fd4-303">'Restore-AzureRmSqlDatabase'</span></span>
    - <span data-ttu-id="73fd4-304">New-AzSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="73fd4-304">'New-AzSqlDatabaseCopy'</span></span>
    - <span data-ttu-id="73fd4-305">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="73fd4-305">'New-AzSqlDatabaseSecondary'</span></span>
* <span data-ttu-id="73fd4-306">Skiftlägeskänslighet har tagits bort för parametern BackupStorageRedundancy för alla SQL DB-referenser</span><span class="sxs-lookup"><span data-stu-id="73fd4-306">Removed case sensitivity for BackupStorageRedundancy parameter for all SQL DB references</span></span> 
* <span data-ttu-id="73fd4-307">Namnen på BackupStorageRedundancy-varningsmeddelanden har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="73fd4-307">Updated BackupStorageRedundancy warning message names</span></span>

#### <a name="azstorage"></a><span data-ttu-id="73fd4-308">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="73fd4-308">Az.Storage</span></span>
* <span data-ttu-id="73fd4-309">Stöd för att aktivera/inaktivera/hämta egenskaper för mjuk borttagning av resurser för filtjänst för ett lagringskonto</span><span class="sxs-lookup"><span data-stu-id="73fd4-309">Supported enable/disable/get share soft delete properties on file Service of a Storage account</span></span>
    - <span data-ttu-id="73fd4-310">Update-AzStorageFileServiceProperty</span><span class="sxs-lookup"><span data-stu-id="73fd4-310">'Update-AzStorageFileServiceProperty'</span></span>
    - <span data-ttu-id="73fd4-311">Get-AzStorageFileServiceProperty</span><span class="sxs-lookup"><span data-stu-id="73fd4-311">'Get-AzStorageFileServiceProperty'</span></span>
* <span data-ttu-id="73fd4-312">Stöd för att visa filresurser inkluderar borttagna filresurser för ett lagringskonto och hämta förbrukning av enskild filresurs</span><span class="sxs-lookup"><span data-stu-id="73fd4-312">Supported list file shares include the deleted ones of a Storage account, and Get single file share usage</span></span>
    - <span data-ttu-id="73fd4-313">”Get-AzRmStorageShare”</span><span class="sxs-lookup"><span data-stu-id="73fd4-313">'Get-AzRmStorageShare'</span></span>
* <span data-ttu-id="73fd4-314">Stöd för återställning av en borttagen filresurs</span><span class="sxs-lookup"><span data-stu-id="73fd4-314">Supported restore a deleted file share</span></span>
    - <span data-ttu-id="73fd4-315">Restore-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="73fd4-315">'Restore-AzRmStorageShare'</span></span>
* <span data-ttu-id="73fd4-316">Cmdletarna för ändring av egenskaper för Blob Service har ändrats. De ursprungliga egenskaperna hämtas inte från servern utan anger bara de ändrade egenskaperna till servern.</span><span class="sxs-lookup"><span data-stu-id="73fd4-316">Changed the cmdlets for modify blob service properties, won't get the original properties from server, but only set the modified properties to server.</span></span>
    - <span data-ttu-id="73fd4-317">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="73fd4-317">'Enable-AzStorageBlobDeleteRetentionPolicy'</span></span>
    - <span data-ttu-id="73fd4-318">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="73fd4-318">'Disable-AzStorageBlobDeleteRetentionPolicy'</span></span>  
    - <span data-ttu-id="73fd4-319">"Enable-AzStorageBlobRestorePolicy"</span><span class="sxs-lookup"><span data-stu-id="73fd4-319">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="73fd4-320">"Disable-AzStorageBlobRestorePolicy"</span><span class="sxs-lookup"><span data-stu-id="73fd4-320">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="73fd4-321">”Update-AzStorageBlobServiceProperty”</span><span class="sxs-lookup"><span data-stu-id="73fd4-321">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="73fd4-322">Åtgärdat hjälpproblem för New-AzStorageAccount-parametern -Kind default value [#12189]</span><span class="sxs-lookup"><span data-stu-id="73fd4-322">Fixed help issue for New-AzStorageAccount parameter -Kind default value [#12189]</span></span>
* <span data-ttu-id="73fd4-323">Åtgärdat problem genom att lägga till exempel som visar hur ContentType anges på korrekt sätt i en blobuppladdning [#12989]</span><span class="sxs-lookup"><span data-stu-id="73fd4-323">Fixed issue by add example to show how to set correct ContentType in blob upload [#12989]</span></span>

## <a name="470---september-2020"></a><span data-ttu-id="73fd4-324">4.7.0 – September 2020</span><span class="sxs-lookup"><span data-stu-id="73fd4-324">4.7.0 - September 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="73fd4-325">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73fd4-325">Az.Accounts</span></span>
* <span data-ttu-id="73fd4-326">Formaterat kommande meddelanden om icke-bakåtkompatibel ändring</span><span class="sxs-lookup"><span data-stu-id="73fd4-326">Formatted the upcoming breaking change messages</span></span>
* <span data-ttu-id="73fd4-327">Uppdaterat Azure.Core till 1.4.1</span><span class="sxs-lookup"><span data-stu-id="73fd4-327">Updated Azure.Core to 1.4.1</span></span>

#### <a name="azaks"></a><span data-ttu-id="73fd4-328">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="73fd4-328">Az.Aks</span></span>
* <span data-ttu-id="73fd4-329">Valideringslogiken för parametern "New-AzAksCluster", "Set-AzAksCluster" och "New-AzAksNodePool" har lagts till på klientsidan.</span><span class="sxs-lookup"><span data-stu-id="73fd4-329">Added client side parameter validation logic for 'New-AzAksCluster', 'Set-AzAksCluster' and 'New-AzAksNodePool'.</span></span> <span data-ttu-id="73fd4-330">[#12372]</span><span class="sxs-lookup"><span data-stu-id="73fd4-330">[#12372]</span></span>
* <span data-ttu-id="73fd4-331">Stöd har lagts till för tillägg i "New-AzAksCluster".</span><span class="sxs-lookup"><span data-stu-id="73fd4-331">Added support for add-ons in 'New-AzAksCluster'.</span></span> <span data-ttu-id="73fd4-332">[#11239]</span><span class="sxs-lookup"><span data-stu-id="73fd4-332">[#11239]</span></span>
* <span data-ttu-id="73fd4-333">Cmdlet:arna "Enable-AzAksAddOn" och "Disable-AzAksAddOn" har lagts till för tillägg.</span><span class="sxs-lookup"><span data-stu-id="73fd4-333">Added cmdlets 'Enable-AzAksAddOn' and 'Disable-AzAksAddOn' for add-ons.</span></span> <span data-ttu-id="73fd4-334">[#11239]</span><span class="sxs-lookup"><span data-stu-id="73fd4-334">[#11239]</span></span>
* <span data-ttu-id="73fd4-335">Parametern "GenerateSshKey" har lagts till för "New-AzAksCluster".</span><span class="sxs-lookup"><span data-stu-id="73fd4-335">Added parameter 'GenerateSshKey' for 'New-AzAksCluster'.</span></span> <span data-ttu-id="73fd4-336">[#12371]</span><span class="sxs-lookup"><span data-stu-id="73fd4-336">[#12371]</span></span>
* <span data-ttu-id="73fd4-337">API-versionen har uppdaterats till 2020-06-01.</span><span class="sxs-lookup"><span data-stu-id="73fd4-337">Updated api version to 2020-06-01.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="73fd4-338">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="73fd4-338">Az.CognitiveServices</span></span>
* <span data-ttu-id="73fd4-339">Visade ytterligare juridiska villkor för vissa API:er.</span><span class="sxs-lookup"><span data-stu-id="73fd4-339">Showed additional legal terms for certain APIs.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73fd4-340">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73fd4-340">Az.Compute</span></span>
* <span data-ttu-id="73fd4-341">Den valfria parametern "EncryptionType" har lagts till i "New-AzVmDiskEncryptionSetConfig"</span><span class="sxs-lookup"><span data-stu-id="73fd4-341">Added the '-EncryptionType' optional parameter to 'New-AzVmDiskEncryptionSetConfig'</span></span>
* <span data-ttu-id="73fd4-342">Nya cmdlet:ar för ny resurs typ: DiskAccess "Get-AzDiskAccess", "New-AzDiskAccess", "Get-AzDiskAccess"</span><span class="sxs-lookup"><span data-stu-id="73fd4-342">New cmdlets for new resource type: DiskAccess 'Get-AzDiskAccess', 'New-AzDiskAccess', 'Get-AzDiskAccess'</span></span>
* <span data-ttu-id="73fd4-343">De valfria parametrarna "-DiskAccessId" och "-NetworkAccessPolicy" har lagts till i "New-AzSnapshotConfig"</span><span class="sxs-lookup"><span data-stu-id="73fd4-343">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzSnapshotConfig'</span></span>
* <span data-ttu-id="73fd4-344">De valfria parametrarna "-DiskAccessId" och "-NetworkAccessPolicy" har lagts till i "New-AzDiskConfig"</span><span class="sxs-lookup"><span data-stu-id="73fd4-344">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzDiskConfig'</span></span>
* <span data-ttu-id="73fd4-345">PatchStatus-egenskapen har lagts till i VirtualMachine-instansvyn</span><span class="sxs-lookup"><span data-stu-id="73fd4-345">Added 'PatchStatus' property to VirtualMachine Instance View</span></span>
* <span data-ttu-id="73fd4-346">Egenskapen "VMHealth" har lagts till i den virtuella datorns instansvy, vilket är det returnerade objektet när "get-AzVm" anropas med "-Status"</span><span class="sxs-lookup"><span data-stu-id="73fd4-346">Added 'VMHealth' property to the virtual machine's instance view, which is the returned object when 'Get-AzVm' is invoked with '-Status'</span></span>
* <span data-ttu-id="73fd4-347">Fältet "AssignedHost" har lagts till i instansvyerna "Get-AzVM" och "Get-AzVmss".</span><span class="sxs-lookup"><span data-stu-id="73fd4-347">Added 'AssignedHost' field to 'Get-AzVM' and 'Get-AzVmss' instance views.</span></span> <span data-ttu-id="73fd4-348">I fältet visas resurs-ID för den virtuella datorinstansen</span><span class="sxs-lookup"><span data-stu-id="73fd4-348">The field shows the resource id of the virtual machine instance</span></span>
* <span data-ttu-id="73fd4-349">Den valfria parametern "-SupportAutomaticPlacement" har lagts till i "New-AzHostGroup"</span><span class="sxs-lookup"><span data-stu-id="73fd4-349">Added optional parameter '-SupportAutomaticPlacement' to 'New-AzHostGroup'</span></span> 
* <span data-ttu-id="73fd4-350">Parametern "-HostGroupId" har lagts till i "New-AzVm" och "New-AzVmss"</span><span class="sxs-lookup"><span data-stu-id="73fd4-350">Added the '-HostGroupId' parameter to 'New-AzVm' and 'New-AzVmss'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="73fd4-351">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="73fd4-351">Az.DataFactory</span></span>
* <span data-ttu-id="73fd4-352">ADF .Net SDK har uppdaterats till version 4.11.0</span><span class="sxs-lookup"><span data-stu-id="73fd4-352">Updated ADF .Net SDK version to 4.11.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="73fd4-353">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="73fd4-353">Az.EventHub</span></span>
* <span data-ttu-id="73fd4-354">Nya kluster-cmdlet:ar – "New-AzEventHubCluster", "Set-AzEventHubCluster", "Get-AzEventHubCluster", "Remove-AzEventHubCluster", "Get-AzEventHubClustersAvailableRegions" har lagts till.</span><span class="sxs-lookup"><span data-stu-id="73fd4-354">Added new Cluster cmdlets - 'New-AzEventHubCluster', 'Set-AzEventHubCluster', 'Get-AzEventHubCluster', 'Remove-AzEventHubCluster', 'Get-AzEventHubClustersAvailableRegions'.</span></span>
* <span data-ttu-id="73fd4-355">Åtgärdat för ärende #10722 : Korrigering för tilldelning av enbart lyssning till AuthorizationRule-rättigheter.</span><span class="sxs-lookup"><span data-stu-id="73fd4-355">Fixed for issue #10722 : Fix for assigning only 'Listen' to AuthorizationRule rights.</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="73fd4-356">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="73fd4-356">Az.Functions</span></span>
* <span data-ttu-id="73fd4-357">Möjligheten att skapa v2-funktioner i regioner som inte stöder det har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="73fd4-357">Removed the ability to create v2 Functions in regions that do not support it.</span></span>
* <span data-ttu-id="73fd4-358">Föråldrad PowerShell 6.2.</span><span class="sxs-lookup"><span data-stu-id="73fd4-358">Deprecated PowerShell 6.2.</span></span> <span data-ttu-id="73fd4-359">En varning har lagts till när en användare skapar en PowerShell 6.2-funktionsapp som uppmanar till att skapa en PowerShell 7.0-funktionsapp i stället.</span><span class="sxs-lookup"><span data-stu-id="73fd4-359">Added a warning for when a user creates a PowerShell 6.2 function app that advises them to create a PowerShell 7.0 function app instead.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="73fd4-360">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="73fd4-360">Az.HDInsight</span></span>
* <span data-ttu-id="73fd4-361">Stöd för att skapa kluster med automatisk skalningskonfiguration</span><span class="sxs-lookup"><span data-stu-id="73fd4-361">Supported creating cluster with Autoscale configuration</span></span>
    - <span data-ttu-id="73fd4-362">Lägg till den nya parametern "AutoscaleConfiguration" till cmdleten ”New-AzHDInsightCluster”</span><span class="sxs-lookup"><span data-stu-id="73fd4-362">Add new parameter 'AutoscaleConfiguration' to the cmdlet 'New-AzHDInsightCluster'</span></span>
* <span data-ttu-id="73fd4-363">Stöd för att använda automatisk skalningskonfiguration i kluster</span><span class="sxs-lookup"><span data-stu-id="73fd4-363">Supported operating cluster's Autoscale configuration</span></span>
    - <span data-ttu-id="73fd4-364">Lägg till ny cmdlet "Get-AzHDInsihgtClusterAutoscaleConfiguration"</span><span class="sxs-lookup"><span data-stu-id="73fd4-364">Add new cmdlet 'Get-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="73fd4-365">Lägg till ny cmdlet "New-AzHDInsihgtClusterAutoscaleConfiguration"</span><span class="sxs-lookup"><span data-stu-id="73fd4-365">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="73fd4-366">Lägg till ny cmdlet "Set-AzHDInsihgtClusterAutoscaleConfiguration"</span><span class="sxs-lookup"><span data-stu-id="73fd4-366">Add new cmdlet 'Set-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="73fd4-367">Lägg till ny cmdlet "Remove-AzHDInsihgtClusterAutoscaleConfiguration"</span><span class="sxs-lookup"><span data-stu-id="73fd4-367">Add new cmdlet 'Remove-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="73fd4-368">Lägg till ny cmdlet "New-AzHDInsihgtClusterAutoscaleScheduleCondition"</span><span class="sxs-lookup"><span data-stu-id="73fd4-368">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleScheduleCondition'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="73fd4-369">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="73fd4-369">Az.KeyVault</span></span>
* <span data-ttu-id="73fd4-370">Stöd har lagts till för RBAC-auktorisering [#10557]</span><span class="sxs-lookup"><span data-stu-id="73fd4-370">Added support for RBAC authorization [#10557]</span></span>
* <span data-ttu-id="73fd4-371">Förbättrad felhantering i "Set-AzKeyVaultAccessPolicy" [#4007]</span><span class="sxs-lookup"><span data-stu-id="73fd4-371">Enhanced error handling in 'Set-AzKeyVaultAccessPolicy' [#4007]</span></span>

#### <a name="azkusto"></a><span data-ttu-id="73fd4-372">Az.Kusto</span><span class="sxs-lookup"><span data-stu-id="73fd4-372">Az.Kusto</span></span>
* <span data-ttu-id="73fd4-373">Allmän tillgänglighet för "Az.Kusto"-modulen</span><span class="sxs-lookup"><span data-stu-id="73fd4-373">General availability of 'Az.Kusto' module</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73fd4-374">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73fd4-374">Az.Network</span></span>
* <span data-ttu-id="73fd4-375">[Viktig ändring] Uppdaterade nedanstående cmdlets för att justera resursens virtuella router och virtuella hubb</span><span class="sxs-lookup"><span data-stu-id="73fd4-375">[Breaking Change] Updated below cmdlets to align resource virtual router and virtual hub</span></span>
    - <span data-ttu-id="73fd4-376">"New-AzVirtualRouter":</span><span class="sxs-lookup"><span data-stu-id="73fd4-376">'New-AzVirtualRouter':</span></span> 
        - <span data-ttu-id="73fd4-377">Parametern-HostedSubnet har lagts till för att stödja underordnad resurs för IP-konfiguration</span><span class="sxs-lookup"><span data-stu-id="73fd4-377">Added -HostedSubnet parameter to support IP configuration child resource</span></span>
        - <span data-ttu-id="73fd4-378">-HostedGateway och -HostedGatewayId har tagits bort</span><span class="sxs-lookup"><span data-stu-id="73fd4-378">deleted -HostedGateway and -HostedGatewayId</span></span>
    - <span data-ttu-id="73fd4-379">'Get-AzVirtualRouter':</span><span class="sxs-lookup"><span data-stu-id="73fd4-379">'Get-AzVirtualRouter':</span></span>
        - <span data-ttu-id="73fd4-380">Parameteruppsättningen har lagts till på prenumerationsnivå</span><span class="sxs-lookup"><span data-stu-id="73fd4-380">Added subscription level parameter set</span></span>
    - <span data-ttu-id="73fd4-381">"Remove-AzVirtualRouter"</span><span class="sxs-lookup"><span data-stu-id="73fd4-381">'Remove-AzVirtualRouter'</span></span>
    - <span data-ttu-id="73fd4-382">"Add-AzVirtualRouterPeer"</span><span class="sxs-lookup"><span data-stu-id="73fd4-382">'Add-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="73fd4-383">"Get-AzVirtualRouterPeer"</span><span class="sxs-lookup"><span data-stu-id="73fd4-383">'Get-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="73fd4-384">"Remove-AzVirtualRouterPeer"</span><span class="sxs-lookup"><span data-stu-id="73fd4-384">'Remove-AzVirtualRouterPeer'</span></span>
* <span data-ttu-id="73fd4-385">Ny cmdlet har lagts till för Azure Express Route-port</span><span class="sxs-lookup"><span data-stu-id="73fd4-385">Added new cmdlet for Azure Express Route Port</span></span>
    - <span data-ttu-id="73fd4-386">"New-AzExpressRoutePortLOA"</span><span class="sxs-lookup"><span data-stu-id="73fd4-386">'New-AzExpressRoutePortLOA'</span></span>
* <span data-ttu-id="73fd4-387">Egenskapen RemoteBgpCommunities har lagts till i VirtualNetwork Peering-resursen</span><span class="sxs-lookup"><span data-stu-id="73fd4-387">Added RemoteBgpCommunities property to the VirtualNetwork Peering Resource</span></span>
* <span data-ttu-id="73fd4-388">Ändrade varningsmeddelandet för ”New-AzLoadBalancerFrontendIpConfig”, ”New-AzPublicIpAddress” och ”New-AzPublicIpPrefix”.</span><span class="sxs-lookup"><span data-stu-id="73fd4-388">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>
* <span data-ttu-id="73fd4-389">Lade till VpnGatewayIpConfigurations till "Get-AzVpnGateway"-utdata</span><span class="sxs-lookup"><span data-stu-id="73fd4-389">Added VpnGatewayIpConfigurations to 'Get-AzVpnGateway' output</span></span>
* <span data-ttu-id="73fd4-390">Åtgärdade bugg för "Set-AzApplicationGatewaySslCertificate" [#9488]</span><span class="sxs-lookup"><span data-stu-id="73fd4-390">Fixed bug for 'Set-AzApplicationGatewaySslCertificate' [#9488]</span></span>
* <span data-ttu-id="73fd4-391">Parametern "AllowActiveFTP" har lagts till i "AzureFirewall"</span><span class="sxs-lookup"><span data-stu-id="73fd4-391">Added 'AllowActiveFTP' parameter to 'AzureFirewall'</span></span>
* <span data-ttu-id="73fd4-392">Nedanstående kommandon för funktionen har uppdaterats: Aktivera konfiguration/borttagning för Internetsäkerhet på VirtualWan P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="73fd4-392">Updated below commands for feature: Enable internet security set/remove on VirtualWan P2SVpnGateway.</span></span>
- <span data-ttu-id="73fd4-393">"New-AzP2sVpnGateway" har uppdaterats": Den valfria växelparametern "EnableInternetSecurityFlag" har lagts till för kunder som anger värdet true för att aktivera Internetsäkerhet på P2SVpnGateway, som ska användas för plats-till-plats-klienter.</span><span class="sxs-lookup"><span data-stu-id="73fd4-393">Updated 'New-AzP2sVpnGateway': Added optional switch parameter 'EnableInternetSecurityFlag' for customers to set true to enable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
- <span data-ttu-id="73fd4-394">"Update-AzP2sVpnGateway" har uppdaterats: De valfria växelparametrarna "EnableInternetSecurityFlag" eller "DisableInternetSecurityFlag" har lagts till för kunder som anger värdet true/false för att aktivera/inaktivera Internetsäkerhet på P2SVpnGateway, som ska användas för plats-till-plats-klienter.</span><span class="sxs-lookup"><span data-stu-id="73fd4-394">Updated 'Update-AzP2sVpnGateway': Added optional switch parameters 'EnableInternetSecurityFlag' or 'DisableInternetSecurityFlag' for customers to set true/false to enable/disable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
* <span data-ttu-id="73fd4-395">Den nya cmdleten "Reset-AzP2sVpnGateway" har lagts till för att kunder ska kunna återställa/starta om sina VirtualWan-P2SVpnGateway för felsökning.</span><span class="sxs-lookup"><span data-stu-id="73fd4-395">Added new cmdlet 'Reset-AzP2sVpnGateway' for customers to reset/reboot their VirtualWan P2SVpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="73fd4-396">Den nya cmdleten "Reset-AzVpnGateway" har lagts till för att kunder ska kunna återställa/starta om VirtualWan VpnGateway för felsökning.</span><span class="sxs-lookup"><span data-stu-id="73fd4-396">Added new cmdlet 'Reset-AzVpnGateway' for customers to reset/reboot their VirtualWan VpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="73fd4-397">"Set-AzVirtualNetworkSubnetConfig" har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="73fd4-397">Updated 'Set-AzVirtualNetworkSubnetConfig'</span></span>
    - <span data-ttu-id="73fd4-398">Ange egenskaper för NSG och routningstabell för undernät till null om det anges explicit i parametrarna [#1548] [#9718]</span><span class="sxs-lookup"><span data-stu-id="73fd4-398">Set NSG and Route Table properties of subnet to null if explicitly set in parameters [#1548][#9718]</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="73fd4-399">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="73fd4-399">Az.RecoveryServices</span></span>
* <span data-ttu-id="73fd4-400">Åtgärdat borttagningstillståndet för säkerhetskopieringsobjekt.</span><span class="sxs-lookup"><span data-stu-id="73fd4-400">Fixed the Delete State for workload Backup Items.</span></span>

#### <a name="azresources"></a><span data-ttu-id="73fd4-401">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73fd4-401">Az.Resources</span></span>
* <span data-ttu-id="73fd4-402">Lagt till saknad kontroll för Set-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="73fd4-402">Added missing check for Set-AzRoleAssignment</span></span>
* <span data-ttu-id="73fd4-403">Attribut som medför icke-bakåtkompatibel ändring har lagts till i parametern "SubscriptionId" i "Get-AzResourceGroupDeploymentOperation"</span><span class="sxs-lookup"><span data-stu-id="73fd4-403">Added breaking change attribute to 'SubscriptionId' parameter of 'Get-AzResourceGroupDeploymentOperation'</span></span>
* <span data-ttu-id="73fd4-404">Uppdaterat What-If-cmdlets i ARM-mall så att resursändringar av typen 'Ignorera' visas sist</span><span class="sxs-lookup"><span data-stu-id="73fd4-404">Updated ARM template What-If cmdlets to show 'Ignore' resource changes last</span></span>
* <span data-ttu-id="73fd4-405">Åtgärdat serialiseringsproblem med säkra parametrar och matrisparametrar för distributionscmdlets [#12773]</span><span class="sxs-lookup"><span data-stu-id="73fd4-405">Fixed secure and array parameter serialization issues for deployment cmdlets [#12773]</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="73fd4-406">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="73fd4-406">Az.ServiceFabric</span></span>
* <span data-ttu-id="73fd4-407">Nya cmdletar har lagts till för hanterade kluster och nodtyper:</span><span class="sxs-lookup"><span data-stu-id="73fd4-407">Added new cmdlets for managed clusters and node types:</span></span>
    - <span data-ttu-id="73fd4-408">"New-AzServiceFabricManagedCluster"</span><span class="sxs-lookup"><span data-stu-id="73fd4-408">'New-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="73fd4-409">"Get-AzServiceFabricManagedCluster"</span><span class="sxs-lookup"><span data-stu-id="73fd4-409">'Get-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="73fd4-410">"Set-AzServiceFabricManagedCluster"</span><span class="sxs-lookup"><span data-stu-id="73fd4-410">'Set-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="73fd4-411">"Remove-AzServiceFabricManagedCluster"</span><span class="sxs-lookup"><span data-stu-id="73fd4-411">'Remove-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="73fd4-412">"Add-AzServiceFabricManagedClusterClientCertificate"</span><span class="sxs-lookup"><span data-stu-id="73fd4-412">'Add-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="73fd4-413">"Remove-AzServiceFabricManagedClusterClientCertificate"</span><span class="sxs-lookup"><span data-stu-id="73fd4-413">'Remove-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="73fd4-414">"New-AzServiceFabricManagedNodeType"</span><span class="sxs-lookup"><span data-stu-id="73fd4-414">'New-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="73fd4-415">"Get-AzServiceFabricManagedNodeType"</span><span class="sxs-lookup"><span data-stu-id="73fd4-415">'Get-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="73fd4-416">"Set-AzServiceFabricManagedNodeType"</span><span class="sxs-lookup"><span data-stu-id="73fd4-416">'Set-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="73fd4-417">"Remove-AzServiceFabricManagedNodeType"</span><span class="sxs-lookup"><span data-stu-id="73fd4-417">'Remove-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="73fd4-418">"Add-AzServiceFabricManagedNodeTypeVMExtension"</span><span class="sxs-lookup"><span data-stu-id="73fd4-418">'Add-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="73fd4-419">"Add-AzServiceFabricManagedNodeTypeVMSecret"</span><span class="sxs-lookup"><span data-stu-id="73fd4-419">'Add-AzServiceFabricManagedNodeTypeVMSecret'</span></span>
    - <span data-ttu-id="73fd4-420">"Remove-AzServiceFabricManagedNodeTypeVMExtension"</span><span class="sxs-lookup"><span data-stu-id="73fd4-420">'Remove-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="73fd4-421">"Restart-AzServiceFabricManagedNodeTyp"</span><span class="sxs-lookup"><span data-stu-id="73fd4-421">'Restart-AzServiceFabricManagedNodeTyp'</span></span>
* <span data-ttu-id="73fd4-422">Service Fabric SDK har uppgraderats till version 1.2.0 som använder Service Fabric-resursprovidern med API-version 2020-03-01 för aktuell modell och 2020-01-01-förhandsversion för hanterade kluster.</span><span class="sxs-lookup"><span data-stu-id="73fd4-422">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2020-03-01 for the current model and 2020-01-01-preview for managed clusters.</span></span>

#### <a name="azsql"></a><span data-ttu-id="73fd4-423">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73fd4-423">Az.Sql</span></span>
* <span data-ttu-id="73fd4-424">BackupStorageRedundancy har lagts till i "New-AzSqlInstance" och "Get-AzSqlInstance"</span><span class="sxs-lookup"><span data-stu-id="73fd4-424">Added BackupStorageRedundancy to 'New-AzSqlInstance' and 'Get-AzSqlInstance'</span></span>
* <span data-ttu-id="73fd4-425">Cmdlet:en "Get-AzSqlServerActiveDirectoryOnlyAuthentication" har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-425">Added cmdlet 'Get-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="73fd4-426">Cmdlet:en "Enable-AzSqlServerActiveDirectoryOnlyAuthentication" har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-426">Added cmdlet 'Enable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="73fd4-427">Force-parametern har lagts till i "New-AzSqlInstance"</span><span class="sxs-lookup"><span data-stu-id="73fd4-427">Added Force parameter to 'New-AzSqlInstance'</span></span>
* <span data-ttu-id="73fd4-428">Cmdlet:ar för logguppspelningstjänst för hanterade databaser har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-428">Added cmdlets for Managed Database Log Replay service</span></span>
    - <span data-ttu-id="73fd4-429">"Start-AzSqlInstanceDatabaseLogReplay"</span><span class="sxs-lookup"><span data-stu-id="73fd4-429">'Start-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="73fd4-430">"Get-AzSqlInstanceDatabaseLogReplay"</span><span class="sxs-lookup"><span data-stu-id="73fd4-430">'Get-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="73fd4-431">"Complete-AzSqlInstanceDatabaseLogReplay"</span><span class="sxs-lookup"><span data-stu-id="73fd4-431">'Complete-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="73fd4-432">"Stop-AzSqlInstanceDatabaseLogReplay"</span><span class="sxs-lookup"><span data-stu-id="73fd4-432">'Stop-AzSqlInstanceDatabaseLogReplay'</span></span>
* <span data-ttu-id="73fd4-433">Cmdlet:en "Get-AzSqlInstanceActiveDirectoryOnlyAuthentication" har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-433">Added cmdlet 'Get-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="73fd4-434">Cmdlet:en "Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication" har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-434">Added cmdlet 'Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="73fd4-435">Cmdlet:en "Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication" har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-435">Added cmdlet 'Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="73fd4-436">Cmdletarna "New-AzSqlDatabaseImport" och "New-AzSqlDatabaseExport" har uppdaterats för att stödja funktioner för nätverksisolering</span><span class="sxs-lookup"><span data-stu-id="73fd4-436">Updated cmdlets 'New-AzSqlDatabaseImport' and 'New-AzSqlDatabaseExport' to support network isolation functionality</span></span>
* <span data-ttu-id="73fd4-437">Cmdleten "New-AzSqlDatabaseImportExisting" har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-437">Added cmdlet 'New-AzSqlDatabaseImportExisting'</span></span>
* <span data-ttu-id="73fd4-438">Uppdaterade databas-cmdlet:ar som stöder typspecifikation av lagringsenhet för säkerhetskopiering</span><span class="sxs-lookup"><span data-stu-id="73fd4-438">Updated Databases cmdlets to support backup storage type specification</span></span>
* <span data-ttu-id="73fd4-439">Force-parametern har lagts till i "New-AzSqlDatabase"</span><span class="sxs-lookup"><span data-stu-id="73fd4-439">Added Force parameter to 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="73fd4-440">Varning för BackupStorageRedundancy-konfiguration har lagts till i utvalda regioner i "New-AzSqlDatabase"</span><span class="sxs-lookup"><span data-stu-id="73fd4-440">Added warning for BackupStorageRedundancy configuration in select regions in 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="73fd4-441">Uppdaterade ActiveDirectoryOnlyAuthentication-cmdletar för server och instans så att de innehåller ResourceId och InputObject</span><span class="sxs-lookup"><span data-stu-id="73fd4-441">Updated ActiveDirectoryOnlyAuthentication cmdlets for server and instance to include ResourceId and InputObject</span></span>

#### <a name="azstorage"></a><span data-ttu-id="73fd4-442">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="73fd4-442">Az.Storage</span></span>
* <span data-ttu-id="73fd4-443">Åtgärdade fel vid uppladdning av blob genom uppgradering till Microsoft.Azure.Storage.DataMovement 2.0.0 [#12220]</span><span class="sxs-lookup"><span data-stu-id="73fd4-443">Fixed upload blob fail by upgrade to Microsoft.Azure.Storage.DataMovement 2.0.0 [#12220]</span></span>
* <span data-ttu-id="73fd4-444">Stöd för återställning baserat på tidpunkt</span><span class="sxs-lookup"><span data-stu-id="73fd4-444">Supported Point In Time Restore</span></span>
    - <span data-ttu-id="73fd4-445">"Enable-AzStorageBlobRestorePolicy"</span><span class="sxs-lookup"><span data-stu-id="73fd4-445">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="73fd4-446">"Disable-AzStorageBlobRestorePolicy"</span><span class="sxs-lookup"><span data-stu-id="73fd4-446">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="73fd4-447">"New-AzStorageBlobRangeToRestore"</span><span class="sxs-lookup"><span data-stu-id="73fd4-447">'New-AzStorageBlobRangeToRestore'</span></span>
    - <span data-ttu-id="73fd4-448">"Restore-AzStorageBlobRange"</span><span class="sxs-lookup"><span data-stu-id="73fd4-448">'Restore-AzStorageBlobRange'</span></span>
* <span data-ttu-id="73fd4-449">Stöd för att hämta status för blobåterställning genom att köra get-AzureRMStorageAccount med parametern -IncludeBlobRestoreStatus</span><span class="sxs-lookup"><span data-stu-id="73fd4-449">Supported get blob restore status of Storage account by run get-AzureRMStorageAccount with parameter -IncludeBlobRestoreStatus</span></span> 
    - <span data-ttu-id="73fd4-450">"Get-AzureRMStorageAccount"</span><span class="sxs-lookup"><span data-stu-id="73fd4-450">'Get-AzureRMStorageAccount'</span></span>
* <span data-ttu-id="73fd4-451">Meddelande om icke-bakåtkompatibel ändring för kommande ändring av cmdlet-utdata har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-451">Added breaking change warning message for upcoming cmdlet output change</span></span>
    - <span data-ttu-id="73fd4-452">"Get-AzStorageContainerStoredAccessPolicy"</span><span class="sxs-lookup"><span data-stu-id="73fd4-452">'Get-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="73fd4-453">"Set-AzStorageContainerStoredAccessPolicy"</span><span class="sxs-lookup"><span data-stu-id="73fd4-453">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="73fd4-454">"Set-AzStorageAccountManagementPolicy"</span><span class="sxs-lookup"><span data-stu-id="73fd4-454">'Set-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="73fd4-455">"Get-AzStorageAccountManagementPolicy"</span><span class="sxs-lookup"><span data-stu-id="73fd4-455">'Get-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="73fd4-456">"Add-AzStorageAccountManagementPolicyAction"</span><span class="sxs-lookup"><span data-stu-id="73fd4-456">'Add-AzStorageAccountManagementPolicyAction'</span></span>
    - <span data-ttu-id="73fd4-457">"New-AzStorageAccountManagementPolicyRule"</span><span class="sxs-lookup"><span data-stu-id="73fd4-457">'New-AzStorageAccountManagementPolicyRule'</span></span>
* <span data-ttu-id="73fd4-458">Uppgraderade Microsoft.Azure.Cosmos.Table SDK till 1.0.8</span><span class="sxs-lookup"><span data-stu-id="73fd4-458">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.8</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="73fd4-459">Tack till våra community-deltagare</span><span class="sxs-lookup"><span data-stu-id="73fd4-459">Thanks to our community contributors</span></span>
* <span data-ttu-id="73fd4-460">Thomas Van Laere (@ThomVanL), Lägg till Dockerfile-alpine-3.10 (#12911)</span><span class="sxs-lookup"><span data-stu-id="73fd4-460">Thomas Van Laere (@ThomVanL), Add Dockerfile-alpine-3.10 (#12911)</span></span> 
* <span data-ttu-id="73fd4-461">Lohith Chowdary Chilukuri (@Lochiluk), Uppdatering av Remove-AzNetworkInterfaceIpConfig.md (#12807)</span><span class="sxs-lookup"><span data-stu-id="73fd4-461">Lohith Chowdary Chilukuri (@Lochiluk), Update Remove-AzNetworkInterfaceIpConfig.md (#12807)</span></span> 
* <span data-ttu-id="73fd4-462">Roberth Strand (@roberthstrand), Get-AzResourceGroup – Nytt exempel och rensning (#12828)</span><span class="sxs-lookup"><span data-stu-id="73fd4-462">Roberth Strand (@roberthstrand), Get-AzResourceGroup - New example, and cleanup (#12828)</span></span> 
* <span data-ttu-id="73fd4-463">Ravi Mishra (@inmishrar), uppdatering av Azure Web App-körningsstack till DOTNETCORE (#12833)</span><span class="sxs-lookup"><span data-stu-id="73fd4-463">Ravi Mishra (@inmishrar), update Azure Web App runtime stack to DOTNETCORE (#12833)</span></span> 
* <span data-ttu-id="73fd4-464">@jack-education, uppdaterat set-AzVirtualNetworkSubnetConfig för att tillåta att NSG och routningstabell tas bort från undernät (#12351)</span><span class="sxs-lookup"><span data-stu-id="73fd4-464">@jack-education, Updated Set-AzVirtualNetworkSubnetConfig to allow NSG and Route Table to be removed from subnet (#12351)</span></span> 
* <span data-ttu-id="73fd4-465">@hagop-globanet, uppdatering av Add-AzApplicationGatewayCustomError.md (#12784)</span><span class="sxs-lookup"><span data-stu-id="73fd4-465">@hagop-globanet, Update Add-AzApplicationGatewayCustomError.md (#12784)</span></span> 
* <span data-ttu-id="73fd4-466">Joshua Van Daalen (@greenSacrifice)</span><span class="sxs-lookup"><span data-stu-id="73fd4-466">Joshua Van Daalen (@greenSacrifice)</span></span>
  * <span data-ttu-id="73fd4-467">Uppdatering av stavning av egenskaper till egenskaper (#12821)</span><span class="sxs-lookup"><span data-stu-id="73fd4-467">Update spelling of Property to Property (#12821)</span></span> 
  * <span data-ttu-id="73fd4-468">Uppdatering av New-AzResourceLock.md-exempel (#12806)</span><span class="sxs-lookup"><span data-stu-id="73fd4-468">Update New-AzResourceLock.md examples (#12806)</span></span>
* <span data-ttu-id="73fd4-469">Eragon Riddle (@eragonriddle), korrigerat fältnamn för parameter i exemplet (#12825)</span><span class="sxs-lookup"><span data-stu-id="73fd4-469">Eragon Riddle (@eragonriddle), Corrected parameter field name in the example (#12825)</span></span> 
* <span data-ttu-id="73fd4-470">@rossifumax, åtgärdat skrivfel i New-AzConfigurationAssignment.md (#12701)</span><span class="sxs-lookup"><span data-stu-id="73fd4-470">@rossifumax, Fix typo in New-AzConfigurationAssignment.md (#12701)</span></span>

## <a name="461---august-2020"></a><span data-ttu-id="73fd4-471">4.6.1 – augusti 2020</span><span class="sxs-lookup"><span data-stu-id="73fd4-471">4.6.1 - August 2020</span></span>
#### <a name="azcompute"></a><span data-ttu-id="73fd4-472">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73fd4-472">Az.Compute</span></span>
* <span data-ttu-id="73fd4-473">Korrigerade EncryptionAtHost-parametern i New-AzVm för att ta bort standardvärdet FALSE [#12776]</span><span class="sxs-lookup"><span data-stu-id="73fd4-473">Patched '-EncryptionAtHost' parameter in 'New-AzVm' to remove default value of false [#12776]</span></span>

## <a name="460---august-2020"></a><span data-ttu-id="73fd4-474">4.6.0 – augusti 2020</span><span class="sxs-lookup"><span data-stu-id="73fd4-474">4.6.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="73fd4-475">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73fd4-475">Az.Accounts</span></span>
* <span data-ttu-id="73fd4-476">Alla offentliga molnmiljöer läses in när slutpunktsidentifieringen inte returnerar AzureCloud (standard) eller andra offentliga miljöer [#12633]</span><span class="sxs-lookup"><span data-stu-id="73fd4-476">Loaded all public cloud environments when discovery endpoint doesn't return default AzureCloud or other public environments [#12633]</span></span>
* <span data-ttu-id="73fd4-477">SubscriptionPolicies har exponerats i Get-AzSubscription [#12551]</span><span class="sxs-lookup"><span data-stu-id="73fd4-477">Exposed SubscriptionPolicies in 'Get-AzSubscription' [#12551]</span></span>

#### <a name="azautomation"></a><span data-ttu-id="73fd4-478">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="73fd4-478">Az.Automation</span></span>
* <span data-ttu-id="73fd4-479">Parametern -RunOn har lagts till i Set-AzAutomationWebhook för att ange en Hybrid Worker-grupp</span><span class="sxs-lookup"><span data-stu-id="73fd4-479">Added '-RunOn' parameters to 'Set-AzAutomationWebhook' to specify a Hybrid Worker Group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73fd4-480">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73fd4-480">Az.Compute</span></span>
* <span data-ttu-id="73fd4-481">Parametern -EncryptionAtHost har lagts till i New-AzVm, New-AzVmss, New-AzVMConfig, New-AzVmssConfig, Update-AzVM och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="73fd4-481">Added '-EncryptionAtHost' parameter to 'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM', and 'Update-AzVmss'</span></span>
* <span data-ttu-id="73fd4-482">SecurityProfile har lagts till i Get-AzVM och Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="73fd4-482">Added 'SecurityProfile' to 'Get-AzVM' and 'Get-AzVmss' return object</span></span>
* <span data-ttu-id="73fd4-483">Växeln -InstanceView har lagts till som valfri parameter i Get-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="73fd4-483">Added '-InstanceView' switch as optional parameter to 'Get-AzHostGroup'</span></span>
* <span data-ttu-id="73fd4-484">En ny cmdlet, Invoke-AzVmPatchAssessment, har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-484">Added new cmdlet 'Invoke-AzVmPatchAssessment'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="73fd4-485">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="73fd4-485">Az.DataFactory</span></span>
* <span data-ttu-id="73fd4-486">Saknade egenskaper har lagts till i klassen PSPipelineRun.</span><span class="sxs-lookup"><span data-stu-id="73fd4-486">Added missing properties to PSPipelineRun class.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="73fd4-487">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="73fd4-487">Az.HDInsight</span></span>
* <span data-ttu-id="73fd4-488">Stöd för att skapa kluster med funktionen för kryptering under överföring.</span><span class="sxs-lookup"><span data-stu-id="73fd4-488">Supported creating cluster with encryption at host feature.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="73fd4-489">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="73fd4-489">Az.KeyVault</span></span>
* <span data-ttu-id="73fd4-490">Varningsmeddelanden har lagts till för planering att inaktivera mjuk borttagning</span><span class="sxs-lookup"><span data-stu-id="73fd4-490">Added warning messages for planning to disable soft delete</span></span>
* <span data-ttu-id="73fd4-491">Varningsmeddelanden har lagts till för planering att ta bort attributet SecretValueText</span><span class="sxs-lookup"><span data-stu-id="73fd4-491">Added warning messages for planning to remove attribute SecretValueText</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="73fd4-492">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="73fd4-492">Az.Maintenance</span></span>
* <span data-ttu-id="73fd4-493">Valfria schemarelaterade fält har lagts till i New-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="73fd4-493">Added optional schedule related fields to 'New-AzMaintenanceConfiguration'</span></span>
* <span data-ttu-id="73fd4-494">En ny cmdlet har lagts till för Get-AzMaintenancePublicConfiguration</span><span class="sxs-lookup"><span data-stu-id="73fd4-494">Added new cmdlet for 'Get-AzMaintenancePublicConfiguration'</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="73fd4-495">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="73fd4-495">Az.ManagedServices</span></span>
* <span data-ttu-id="73fd4-496">Varningar har lagts till om icke-bakåtkompatibla ändringar för cmdletar för tilldelning och definition av hanterade tjänster</span><span class="sxs-lookup"><span data-stu-id="73fd4-496">Added breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="73fd4-497">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="73fd4-497">Az.Monitor</span></span>
* <span data-ttu-id="73fd4-498">Utökade parametern som angetts i Set-AzDiagnosticSetting för separering av aktivering av loggar och mått [#12482]</span><span class="sxs-lookup"><span data-stu-id="73fd4-498">Extended the parameter set in 'Set-AzDiagnosticSetting' for separation of Logs and Metrics enablement [#12482]</span></span>
* <span data-ttu-id="73fd4-499">Åtgärdat fel för Add-AzMetricAlertRuleV2 vid hämtning av måttavisering från pipelinen</span><span class="sxs-lookup"><span data-stu-id="73fd4-499">Fixed bug for 'Add-AzMetricAlertRuleV2' when getting metric alert from pipeline</span></span>

#### <a name="azresources"></a><span data-ttu-id="73fd4-500">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73fd4-500">Az.Resources</span></span>
* <span data-ttu-id="73fd4-501">Get-AzPolicyAlias-svaret har uppdaterats för att ta med information som anger om aliaset kan ändras eller inte av Azure Policy.</span><span class="sxs-lookup"><span data-stu-id="73fd4-501">Updated 'Get-AzPolicyAlias' response to include information indicating whether the alias is modifiable by Azure Policy.</span></span>
* <span data-ttu-id="73fd4-502">Skapade en ny cmdlet, set-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="73fd4-502">Created new cmdlet 'Set-AzRoleAssignment'</span></span>
* <span data-ttu-id="73fd4-503">Get-AzDeploymentManagementGroupWhatIfResult har lagts till för att hämta What-If-resultat för ARM-mall i hanteringsgruppsomfånget</span><span class="sxs-lookup"><span data-stu-id="73fd4-503">Added 'Get-AzDeploymentManagementGroupWhatIfResult' for getting ARM template What-If results at management Group scope</span></span>
* <span data-ttu-id="73fd4-504">En ny cmdlet, Get-AzTenantWhatIfResult, har lagts till för att hämta What-If-resultat för ARM-mall i klientorganisationsomfånget</span><span class="sxs-lookup"><span data-stu-id="73fd4-504">Added 'Get-AzTenantWhatIfResult' new cmdlet for getting ARM template What-If results at tenant scope</span></span>
* <span data-ttu-id="73fd4-505">-WhatIf och -Confirm har åsidosatts för New-AzManagementGroupDeployment och New-AzTenantDeployment för att använda What-If-resultat för ARM-mall</span><span class="sxs-lookup"><span data-stu-id="73fd4-505">Overrode '-WhatIf' and '-Confirm' for 'New-AzManagementGroupDeployment' and 'New-AzTenantDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="73fd4-506">Beteenden har åtgärdats för -WhatIf och -Confirm för nya cmdletar för distribution så att de stämmer överens med False och</span><span class="sxs-lookup"><span data-stu-id="73fd4-506">Fixed the behaviors of '-WhatIf' and '-Confirm' for new deployment cmdlets so they comply with False and</span></span> 
* <span data-ttu-id="73fd4-507">Serialiseringsfel har åtgärdats för -TemplateObject och TemplateParameterObject [#1528] [#6292]</span><span class="sxs-lookup"><span data-stu-id="73fd4-507">Fixed serialization error for '-TemplateObject' and 'TemplateParameterObject' [#1528] [#6292]</span></span>
* <span data-ttu-id="73fd4-508">Attribut som medför icke-bakåtkompatibel ändring har lagts till i Get-AzResourceGroupDeploymentOperation för den kommande ändringen av utdatatyp</span><span class="sxs-lookup"><span data-stu-id="73fd4-508">Added breaking change attribute to 'Get-AzResourceGroupDeploymentOperation' for the upcoming output type change</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="73fd4-509">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="73fd4-509">Az.SignalR</span></span>
* <span data-ttu-id="73fd4-510">Fel i hjälpfilerna Restart-AzSignalR och Update-AzSignalR har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="73fd4-510">Fixed 'Restart-AzSignalR' and 'Update-AzSignalR' help files errors</span></span>
* <span data-ttu-id="73fd4-511">Cmdletarna Update-AzSignalRNetworkAcl och Set-AzSignalRUpstream har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-511">Added cmdlets 'Update-AzSignalRNetworkAcl', 'Set-AzSignalRUpstream'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="73fd4-512">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="73fd4-512">Az.Storage</span></span>
* <span data-ttu-id="73fd4-513">Stöd för blobfrågeacceleration</span><span class="sxs-lookup"><span data-stu-id="73fd4-513">Supported blob query acceleration</span></span>
    -  <span data-ttu-id="73fd4-514">Get-AzStorageBlobQueryResult</span><span class="sxs-lookup"><span data-stu-id="73fd4-514">'Get-AzStorageBlobQueryResult'</span></span>
    -  <span data-ttu-id="73fd4-515">New-AzStorageBlobQueryConfig</span><span class="sxs-lookup"><span data-stu-id="73fd4-515">'New-AzStorageBlobQueryConfig'</span></span>
* <span data-ttu-id="73fd4-516">Hjälpfil har lagts till, ytterligare beskrivning har lagts till och stavfel har korrigerats</span><span class="sxs-lookup"><span data-stu-id="73fd4-516">Updated help file, added more description, and fixed typo</span></span>
    -  <span data-ttu-id="73fd4-517">”Start-AzStorageBlobCopy”</span><span class="sxs-lookup"><span data-stu-id="73fd4-517">'Start-AzStorageBlobCopy'</span></span>
    -  <span data-ttu-id="73fd4-518">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="73fd4-518">'Get-AzDataLakeGen2Item'</span></span>
* <span data-ttu-id="73fd4-519">Problem med att ladda ned blob när relaterad underordnad katalog saknas har åtgärdats [#12592]</span><span class="sxs-lookup"><span data-stu-id="73fd4-519">Fixed download blob fail when related sub directory not exist [#12592]</span></span>
    -  <span data-ttu-id="73fd4-520">”Get-AzStorageBlobContent”</span><span class="sxs-lookup"><span data-stu-id="73fd4-520">'Get-AzStorageBlobContent'</span></span>
* <span data-ttu-id="73fd4-521">Replikeringsprincip för att ange, hämta, ta bort objekt på Storage-konton stöds</span><span class="sxs-lookup"><span data-stu-id="73fd4-521">Supported Set/Get/Remove Object Replication Policy on Storage accounts</span></span>
    - <span data-ttu-id="73fd4-522">New-AzStorageObjectReplicationPolicyRule</span><span class="sxs-lookup"><span data-stu-id="73fd4-522">'New-AzStorageObjectReplicationPolicyRule'</span></span>
    - <span data-ttu-id="73fd4-523">Set-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="73fd4-523">'Set-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="73fd4-524">Get-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="73fd4-524">'Get-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="73fd4-525">Remove-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="73fd4-525">'Remove-AzStorageObjectReplicationPolicy'</span></span>
* <span data-ttu-id="73fd4-526">Stöd har lagts till för att aktivera/inaktivera ChangeFeed i Blob Service för ett Storage-konto</span><span class="sxs-lookup"><span data-stu-id="73fd4-526">Supported enable/disable ChangeFeed on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="73fd4-527">”Update-AzStorageBlobServiceProperty”</span><span class="sxs-lookup"><span data-stu-id="73fd4-527">'Update-AzStorageBlobServiceProperty'</span></span>

## <a name="450---august-2020"></a><span data-ttu-id="73fd4-528">4.5.0 – augusti 2020</span><span class="sxs-lookup"><span data-stu-id="73fd4-528">4.5.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="73fd4-529">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73fd4-529">Az.Accounts</span></span>
* <span data-ttu-id="73fd4-530">Uppdaterade ”Connect-AzAccount” så att det accepterar parametern ”MaxContextPopulation” [#9865]</span><span class="sxs-lookup"><span data-stu-id="73fd4-530">Updated 'Connect-AzAccount' to accept parameter 'MaxContextPopulation' [#9865]</span></span>
* <span data-ttu-id="73fd4-531">Uppdaterade SubscriptionClient-versionen till 2019-06-01 och visa klientdomäner [#9838]</span><span class="sxs-lookup"><span data-stu-id="73fd4-531">Updated SubscriptionClient version to 2019-06-01 and display tenant domains [#9838]</span></span>
* <span data-ttu-id="73fd4-532">Information om hemklientorganisation och managedBy-klientorganisation som stöds för prenumerationen</span><span class="sxs-lookup"><span data-stu-id="73fd4-532">Supported home tenant and managedBy tenant information of subscription</span></span>
* <span data-ttu-id="73fd4-533">Korrigerade modulnamn, versionsinformation i telemetridata</span><span class="sxs-lookup"><span data-stu-id="73fd4-533">Corrected module name, version info in telemetry data</span></span>
* <span data-ttu-id="73fd4-534">Justerade SqlDatabaseDnsSuffix och ServiceManagementUrl om miljöns slutpunkt för metadata returnerar ett inkompatibelt värde</span><span class="sxs-lookup"><span data-stu-id="73fd4-534">Adjusted SqlDatabaseDnsSuffix and ServiceManagementUrl if environment metadata endpoint returns incompatible value</span></span>

#### <a name="azaks"></a><span data-ttu-id="73fd4-535">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="73fd4-535">Az.Aks</span></span>
* <span data-ttu-id="73fd4-536">Tog bort ”ClientIdAndSecret” för ”ServicePrincipalIdAndSecret” och ställde in ”ClientIdAndSecret” som ett alias [#12381].</span><span class="sxs-lookup"><span data-stu-id="73fd4-536">Removed 'ClientIdAndSecret' to 'ServicePrincipalIdAndSecret' and set 'ClientIdAndSecret' as an alias [#12381].</span></span>
* <span data-ttu-id="73fd4-537">Tog bort ”Get-AzAks”/”New-AzAks”/”Remove-AzAks”/”Set-AzAks” för ”Get-AzAksCluster”/”New-AzAksCluster”/”Remove-AzAksCluster”/”Set-AzAksCluster” och ställde in de ursprungliga som alias [#12373].</span><span class="sxs-lookup"><span data-stu-id="73fd4-537">Removed 'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' to 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' and set the original ones as alias [#12373].</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="73fd4-538">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="73fd4-538">Az.ApiManagement</span></span>
* <span data-ttu-id="73fd4-539">Lade till ny cmdlet: ”Add-AzApiManagementApiToGateway”.</span><span class="sxs-lookup"><span data-stu-id="73fd4-539">Added new 'Add-AzApiManagementApiToGateway' cmdlet.</span></span>
* <span data-ttu-id="73fd4-540">Lade till ny cmdlet: ”Get-AzApiManagementGateway”.</span><span class="sxs-lookup"><span data-stu-id="73fd4-540">Added new 'Get-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="73fd4-541">Lade till ny cmdlet: ”Get-AzApiManagementGatewayHostnameConfiguration”.</span><span class="sxs-lookup"><span data-stu-id="73fd4-541">Added new 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="73fd4-542">Lade till ny cmdlet: ”Get-AzApiManagementGatewayKey”.</span><span class="sxs-lookup"><span data-stu-id="73fd4-542">Added new 'Get-AzApiManagementGatewayKey' cmdlet.</span></span>
* <span data-ttu-id="73fd4-543">Lade till ny cmdlet: ”New-AzApiManagementGateway”.</span><span class="sxs-lookup"><span data-stu-id="73fd4-543">Added new 'New-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="73fd4-544">Lade till ny cmdlet: ”New-AzApiManagementGatewayHostnameConfiguration”.</span><span class="sxs-lookup"><span data-stu-id="73fd4-544">Added new 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="73fd4-545">Lade till ny cmdlet: ”New-AzApiManagementResourceLocationObject”.</span><span class="sxs-lookup"><span data-stu-id="73fd4-545">Added new 'New-AzApiManagementResourceLocationObject' cmdlet.</span></span>
* <span data-ttu-id="73fd4-546">Lade till ny cmdlet: ”Remove-AzApiManagementApiFromGateway”.</span><span class="sxs-lookup"><span data-stu-id="73fd4-546">Added new 'Remove-AzApiManagementApiFromGateway' cmdlet.</span></span>
* <span data-ttu-id="73fd4-547">Lade till ny cmdlet: ”Remove-AzApiManagementGateway”.</span><span class="sxs-lookup"><span data-stu-id="73fd4-547">Added new 'Remove-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="73fd4-548">Lade till ny cmdlet: ”Remove-AzApiManagementGatewayHostnameConfiguration”.</span><span class="sxs-lookup"><span data-stu-id="73fd4-548">Added new 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="73fd4-549">Lade till ny cmdlet: ”Update-AzApiManagementGateway”.</span><span class="sxs-lookup"><span data-stu-id="73fd4-549">Added new 'Update-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="73fd4-550">Lade till den nya valfria parametern [-GatewayId] till cmdleten ”Get-AzApiManagementApi”.</span><span class="sxs-lookup"><span data-stu-id="73fd4-550">Added new optional [-GatewayId] parameter to the 'Get-AzApiManagementApi' cmdlet.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="73fd4-551">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="73fd4-551">Az.CognitiveServices</span></span>
* <span data-ttu-id="73fd4-552">Använde ”Neka” som standardåtgärd för NetworkRules.</span><span class="sxs-lookup"><span data-stu-id="73fd4-552">Used 'Deny' specifically as NetworkRules default action.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="73fd4-553">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="73fd4-553">Az.FrontDoor</span></span>
* <span data-ttu-id="73fd4-554">Åtgärdade ett problem där ett undantag uppstår när Enum.Parse försöker att tvinga ett null-värde till aktiverade eller inaktiverade uppräkningsvärden [#12344]</span><span class="sxs-lookup"><span data-stu-id="73fd4-554">Fixed an issue where an exception is being thrown when Enum.Parse tries to coerce a null value to an Enabled or Disabled enum values [#12344]</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="73fd4-555">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="73fd4-555">Az.HDInsight</span></span>
* <span data-ttu-id="73fd4-556">Stöd för att skapa kluster med funktionen Kryptering under överföring.</span><span class="sxs-lookup"><span data-stu-id="73fd4-556">Supported creating cluster with encryption in transit feature.</span></span>
    - <span data-ttu-id="73fd4-557">Lägg till den nya parametern ”EncryptionInTransit” till cmdleten ”New-AzHDInsightCluster”</span><span class="sxs-lookup"><span data-stu-id="73fd4-557">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="73fd4-558">Lägg till den nya parametern ”EncryptionInTransit” till cmdleten ”New-AzHDInsightClusterConfig”</span><span class="sxs-lookup"><span data-stu-id="73fd4-558">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="73fd4-559">Stöd för att skapa kluster med funktionen privat länk:</span><span class="sxs-lookup"><span data-stu-id="73fd4-559">Supported creating cluster with private link feature:</span></span>
    - <span data-ttu-id="73fd4-560">Lägg till de nya parametrarna ”PublicNetworkAccessType” och ”OutboundPublicNetworkAccessType” till cmdleten ”New-AzHDInsightCluster”</span><span class="sxs-lookup"><span data-stu-id="73fd4-560">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="73fd4-561">Lägg till de nya parametrarna ”PublicNetworkAccessType” och ”OutboundPublicNetworkAccessType” till cmdleten ”New-AzHDInsightClusterConfig”</span><span class="sxs-lookup"><span data-stu-id="73fd4-561">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="73fd4-562">Returnerade information om det virtuella nätverket vid anrop till ”New-AzHDInsightCluster” eller ”Get-AzHDInsightCluster”</span><span class="sxs-lookup"><span data-stu-id="73fd4-562">Returned virtual network information when calling 'New-AzHDInsightCluster' or 'Get-AzHDInsightCluster'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73fd4-563">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73fd4-563">Az.Network</span></span>
* <span data-ttu-id="73fd4-564">Stöd har lagts till för parametern AddressPrefixType i ”Remove-AzExpressRouteCircuitConnectionConfig”</span><span class="sxs-lookup"><span data-stu-id="73fd4-564">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="73fd4-565">Lade till bakåtkompatibel ändringar: PeerAddressType-funktioner för privat peering i ”Remove-AzExpressRouteCircutPeeringConfig”.</span><span class="sxs-lookup"><span data-stu-id="73fd4-565">Added non-breaking changes: PeerAddressType functionality for Private Peering in 'Remove-AzExpressRouteCircutPeeringConfig'.</span></span>
* <span data-ttu-id="73fd4-566">Koden ändrades för att ignorera skiftläge för parametrarna AddressPrefixType och PeerAddressType.</span><span class="sxs-lookup"><span data-stu-id="73fd4-566">Code changed to ignore case for AddressPrefixType and PeerAddressType parameter.</span></span>
* <span data-ttu-id="73fd4-567">Ändrade varningsmeddelandet för ”New-AzLoadBalancerFrontendIpConfig”, ”New-AzPublicIpAddress” och ”New-AzPublicIpPrefix”.</span><span class="sxs-lookup"><span data-stu-id="73fd4-567">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="73fd4-568">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="73fd4-568">Az.OperationalInsights</span></span>
* <span data-ttu-id="73fd4-569">Lade till alternativet ”-ForceDelete” för ”Remove-AzOperationalInsightsworkspace”</span><span class="sxs-lookup"><span data-stu-id="73fd4-569">Added '-ForceDelete' option for 'Remove-AzOperationalInsightsworkspace'</span></span>
* <span data-ttu-id="73fd4-570">Lade till ny cmdlet: ”Get-AzOperationalInsightsDeletedWorkspace”</span><span class="sxs-lookup"><span data-stu-id="73fd4-570">Added new cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'</span></span>
* <span data-ttu-id="73fd4-571">Lade till ny cmdlet: ”Restore-AzOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="73fd4-571">Added new cmdlet 'Restore-AzOperationalInsightsWorkspace'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="73fd4-572">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="73fd4-572">Az.RecoveryServices</span></span>
* <span data-ttu-id="73fd4-573">Förbättrade sättet Azure Backup-containrar/objekt identifieras.</span><span class="sxs-lookup"><span data-stu-id="73fd4-573">Improved the Azure Backup container/item discovery experience.</span></span>

#### <a name="azresources"></a><span data-ttu-id="73fd4-574">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73fd4-574">Az.Resources</span></span>
* <span data-ttu-id="73fd4-575">Lade till egenskaperna ”Condition”, ”ConditionVersion” och ”Description” till ”New-AzRoleAssignment”</span><span class="sxs-lookup"><span data-stu-id="73fd4-575">Added properties 'Condition', 'ConditionVersion' and 'Description' to 'New-AzRoleAssignment'</span></span>
    - <span data-ttu-id="73fd4-576">Detta omfattade alla relevanta ändringar av datamodellerna</span><span class="sxs-lookup"><span data-stu-id="73fd4-576">This included all the relevant changes to the data models</span></span>

#### <a name="azsql"></a><span data-ttu-id="73fd4-577">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73fd4-577">Az.Sql</span></span>
* <span data-ttu-id="73fd4-578">Korrigerade ett potentiellt fel med skiftlägesokänsliga servernamn i ”New-AzSqlServer” och ”Set-AzSqlServer”</span><span class="sxs-lookup"><span data-stu-id="73fd4-578">Fixed potential server name case insensitive error in 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="73fd4-579">Korrigerade att fel databasnamn returnerades vid ett befintligt databasfel i ”New-AzSqlDatabaseSecondary”</span><span class="sxs-lookup"><span data-stu-id="73fd4-579">Fixed wrong database name returned on existing database error in 'New-AzSqlDatabaseSecondary'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="73fd4-580">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="73fd4-580">Az.Storage</span></span>
* <span data-ttu-id="73fd4-581">Stöd för att skapa container/blob för SAS-token med de nya behörigheterna x, t</span><span class="sxs-lookup"><span data-stu-id="73fd4-581">Supported create container/blob Sas token with new permission x,t</span></span>
    -  <span data-ttu-id="73fd4-582">”New-AzStorageBlobSASToken”</span><span class="sxs-lookup"><span data-stu-id="73fd4-582">'New-AzStorageBlobSASToken'</span></span>
    -  <span data-ttu-id="73fd4-583">”New-AzStorageContainerSASToken”</span><span class="sxs-lookup"><span data-stu-id="73fd4-583">'New-AzStorageContainerSASToken'</span></span>
* <span data-ttu-id="73fd4-584">Stöd för att skapa konto för SAS-token med de nya behörigheterna x, t, f</span><span class="sxs-lookup"><span data-stu-id="73fd4-584">Supported create account Sas token with new permission x,t,f</span></span>
    -  <span data-ttu-id="73fd4-585">”New-AzStorageAccountSASToken”</span><span class="sxs-lookup"><span data-stu-id="73fd4-585">'New-AzStorageAccountSASToken'</span></span>
* <span data-ttu-id="73fd4-586">Stöd för att hämta förbrukning av enskild filresurs</span><span class="sxs-lookup"><span data-stu-id="73fd4-586">Supported get single file share usage</span></span>
    - <span data-ttu-id="73fd4-587">”Get-AzRmStorageShare”</span><span class="sxs-lookup"><span data-stu-id="73fd4-587">'Get-AzRmStorageShare'</span></span>

## <a name="440---july-2020"></a><span data-ttu-id="73fd4-588">4.4.0 – juli 2020</span><span class="sxs-lookup"><span data-stu-id="73fd4-588">4.4.0 - July 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="73fd4-589">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73fd4-589">Az.Accounts</span></span>
* <span data-ttu-id="73fd4-590">En ny cmdlet, ”Invoke-AzRestMethod”, har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-590">Added new cmdlet 'Invoke-AzRestMethod'</span></span>
* <span data-ttu-id="73fd4-591">Ett problem åtgärdades som kan orsaka autentiseringsfel i scenarier med fler processer, t.ex. när flera Azure PowerShell-cmdletar körs med ”Start-Job” [#9448]</span><span class="sxs-lookup"><span data-stu-id="73fd4-591">Fixed an issue that may cause authentication errors in multi-process scenarios such as running multiple Azure PowerShell cmdlets using 'Start-Job' [#9448]</span></span>

#### <a name="azaks"></a><span data-ttu-id="73fd4-592">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="73fd4-592">Az.Aks</span></span>
* <span data-ttu-id="73fd4-593">Felet som gjorde att ”Get-AzAks” inte hämtade alla kluster har åtgärdats [#12296]</span><span class="sxs-lookup"><span data-stu-id="73fd4-593">Fixed bug 'Get-AzAks' doesn't get all clusters [#12296]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="73fd4-594">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="73fd4-594">Az.AnalysisServices</span></span>
* <span data-ttu-id="73fd4-595">Projektreferensen till autentisering har tagits bort</span><span class="sxs-lookup"><span data-stu-id="73fd4-595">Removed project reference to Authentication</span></span>

#### <a name="azautomation"></a><span data-ttu-id="73fd4-596">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="73fd4-596">Az.Automation</span></span>
* <span data-ttu-id="73fd4-597">Problemet som gjorde att strängar med escape-tecken inte kunde konverteras till JSON-objekt har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="73fd4-597">Fixed the issue that string with escape chars cannot be converted into json object.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73fd4-598">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73fd4-598">Az.Compute</span></span>
* <span data-ttu-id="73fd4-599">En varning har lats till som visas när ”New-AzVmss” används utan den senaste avbildningsversionen</span><span class="sxs-lookup"><span data-stu-id="73fd4-599">Added warning when using 'New-AzVmss' without 'latest' image version</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="73fd4-600">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="73fd4-600">Az.DataFactory</span></span>
* <span data-ttu-id="73fd4-601">Globala parametrar har lagts till för Data Factory.</span><span class="sxs-lookup"><span data-stu-id="73fd4-601">Added global parameters to Data Factory.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="73fd4-602">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="73fd4-602">Az.EventGrid</span></span>
* <span data-ttu-id="73fd4-603">Modulen har uppdaterats så att API-version 2020-06-01 används.</span><span class="sxs-lookup"><span data-stu-id="73fd4-603">Updated to use the 2020-06-01 API version.</span></span>
* <span data-ttu-id="73fd4-604">Nya funktioner har lagts till:</span><span class="sxs-lookup"><span data-stu-id="73fd4-604">Added new features:</span></span>
    - <span data-ttu-id="73fd4-605">Indatamappning</span><span class="sxs-lookup"><span data-stu-id="73fd4-605">Input mapping</span></span>
    - <span data-ttu-id="73fd4-606">Schema för händelseleverans</span><span class="sxs-lookup"><span data-stu-id="73fd4-606">Event Delivery Schema</span></span>
    - <span data-ttu-id="73fd4-607">Private Link</span><span class="sxs-lookup"><span data-stu-id="73fd4-607">Private Link</span></span>
    - <span data-ttu-id="73fd4-608">Cloud Event V10 Schema</span><span class="sxs-lookup"><span data-stu-id="73fd4-608">Cloud Event V10 Schema</span></span>
    - <span data-ttu-id="73fd4-609">Service Bus-ämne som mål</span><span class="sxs-lookup"><span data-stu-id="73fd4-609">Service Bus Topic As Destination</span></span>
    - <span data-ttu-id="73fd4-610">Azure-funktion som mål</span><span class="sxs-lookup"><span data-stu-id="73fd4-610">Azure Function As Destination</span></span>
    - <span data-ttu-id="73fd4-611">Webhook-batchbearbetning</span><span class="sxs-lookup"><span data-stu-id="73fd4-611">WebHook Batching</span></span>
    - <span data-ttu-id="73fd4-612">Säker webhook (AAD-stöd)</span><span class="sxs-lookup"><span data-stu-id="73fd4-612">Secure webhook (AAD support)</span></span>
    - <span data-ttu-id="73fd4-613">IpFiltering</span><span class="sxs-lookup"><span data-stu-id="73fd4-613">IpFiltering</span></span>
* <span data-ttu-id="73fd4-614">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="73fd4-614">Updated cmdlets:</span></span>
    - <span data-ttu-id="73fd4-615">”New-AzEventGridSubscription”/”Update-AzEventGridSubscription”:</span><span class="sxs-lookup"><span data-stu-id="73fd4-615">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span></span>
        - <span data-ttu-id="73fd4-616">Lägg till nya valfria parametrar för att ge stöd för webhook-batchbearbetning.</span><span class="sxs-lookup"><span data-stu-id="73fd4-616">Add new optional parameters to support webhook batching.</span></span>
        - <span data-ttu-id="73fd4-617">Lägg till nya valfria parametrar för att ge stöd för skyddad webhook med AAD.</span><span class="sxs-lookup"><span data-stu-id="73fd4-617">Add new optional parameters to support secured webhook using AAD.</span></span>
        - <span data-ttu-id="73fd4-618">Lägg till ny enum (uppräkning) för EndpointType-parametern för att ge stöd för Azure-funktion och Service Bus-ämne som nya mål.</span><span class="sxs-lookup"><span data-stu-id="73fd4-618">Add new enum for EndpointType parameter to support azure function and service bus topic as new destinations.</span></span>
        - <span data-ttu-id="73fd4-619">Lägg till ny valfri parameter för leveransschema.</span><span class="sxs-lookup"><span data-stu-id="73fd4-619">Add new optional parameter for delivery schema.</span></span>
    - <span data-ttu-id="73fd4-620">”New-AzEventGridTopic”/”Update-AzEventGridTopic” och ”New-AzEventGridDomain”/”Update-AzEventGridDomain”:</span><span class="sxs-lookup"><span data-stu-id="73fd4-620">'New-AzEventGridTopic'/'Update-AzEventGridTopic' and 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span></span>
        - <span data-ttu-id="73fd4-621">Lägg till nya valfria parametrar för att ge stöd för IpFiltering.</span><span class="sxs-lookup"><span data-stu-id="73fd4-621">Add new optional parameters to support IpFiltering.</span></span>
    - <span data-ttu-id="73fd4-622">”New-AzEventGridTopic”/”New-AzEventGridDomain”:</span><span class="sxs-lookup"><span data-stu-id="73fd4-622">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span></span>
        - <span data-ttu-id="73fd4-623">Lägg till nya valfria parametrar för att ge stöd för indatamappning.</span><span class="sxs-lookup"><span data-stu-id="73fd4-623">Add new optional parameters to support Input mapping.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="73fd4-624">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="73fd4-624">Az.FrontDoor</span></span>
* <span data-ttu-id="73fd4-625">Modulen har uppdaterats så att API 2020-05-01 används</span><span class="sxs-lookup"><span data-stu-id="73fd4-625">Updated module to use API 2020-05-01</span></span>
* <span data-ttu-id="73fd4-626">Stöd för privat länk har lagts till för Storage-, KeyVault- och Web App Service-resurser</span><span class="sxs-lookup"><span data-stu-id="73fd4-626">Added Private link support for Storage, Keyvault and Web App Service resources</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="73fd4-627">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="73fd4-627">Az.HDInsight</span></span>
* <span data-ttu-id="73fd4-628">Stöd för att skapa kluster med ADLSGen1/2-lagring i nationella moln.</span><span class="sxs-lookup"><span data-stu-id="73fd4-628">Supported creating cluster with ADLSGen1/2 storage in national clouds.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="73fd4-629">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="73fd4-629">Az.Monitor</span></span>
* <span data-ttu-id="73fd4-630">Bugg som orsakade fel med ”Get-AzDiagnosticSetting” när mått eller loggar var null har åtgärdats [#12272]</span><span class="sxs-lookup"><span data-stu-id="73fd4-630">Fixed bug for 'Get-AzDiagnosticSetting' when metrics or logs are null [#12272]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73fd4-631">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73fd4-631">Az.Network</span></span>
* <span data-ttu-id="73fd4-632">Parameterväxlingen i VWan HubVnet-anslutningar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="73fd4-632">Fixed parameters swap in VWan HubVnet connection</span></span>
* <span data-ttu-id="73fd4-633">Nya cmdletar har lagts till för platser för virtuella installationer i Azure-nätverk</span><span class="sxs-lookup"><span data-stu-id="73fd4-633">Added new cmdlets for Azure Network Virtual Appliance Sites</span></span>
    - <span data-ttu-id="73fd4-634">”Get-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="73fd4-634">'Get-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="73fd4-635">”New-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="73fd4-635">'New-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="73fd4-636">”Remove-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="73fd4-636">'Remove-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="73fd4-637">”Update-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="73fd4-637">'Update-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="73fd4-638">”New-AzOffice365PolicyProperty”</span><span class="sxs-lookup"><span data-stu-id="73fd4-638">'New-AzOffice365PolicyProperty'</span></span>
* <span data-ttu-id="73fd4-639">Nya cmdletar har lagts till för virtuella installationer i Azure-nätverk</span><span class="sxs-lookup"><span data-stu-id="73fd4-639">Added new cmdlets for Azure Network Virtual Appliance</span></span>
    - <span data-ttu-id="73fd4-640">”Get-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="73fd4-640">'Get-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="73fd4-641">”New-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="73fd4-641">'New-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="73fd4-642">”Remove-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="73fd4-642">'Remove-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="73fd4-643">”Update-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="73fd4-643">'Update-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="73fd4-644">”Get-AzNetworkVirtualApplianceSku”</span><span class="sxs-lookup"><span data-stu-id="73fd4-644">'Get-AzNetworkVirtualApplianceSku'</span></span>
    - <span data-ttu-id="73fd4-645">”New-AzVirtualApplianceSkuProperty”</span><span class="sxs-lookup"><span data-stu-id="73fd4-645">'New-AzVirtualApplianceSkuProperty'</span></span>
* <span data-ttu-id="73fd4-646">Application Gateway har introducerats i vanliga cmdletar för Private Link</span><span class="sxs-lookup"><span data-stu-id="73fd4-646">Onboarded Application Gateway to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="73fd4-647">StorageSync har introducerats i vanliga cmdletar för Private Link</span><span class="sxs-lookup"><span data-stu-id="73fd4-647">Onboarded StorageSync to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="73fd4-648">SignalR har introducerats i vanliga cmdletar för Private Link</span><span class="sxs-lookup"><span data-stu-id="73fd4-648">Onboarded SignalR to Private Link Common Cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="73fd4-649">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="73fd4-649">Az.RecoveryServices</span></span>
* <span data-ttu-id="73fd4-650">Projektreferensen till autentisering har tagits bort</span><span class="sxs-lookup"><span data-stu-id="73fd4-650">Removed project reference to Authentication</span></span>
* <span data-ttu-id="73fd4-651">Azure Backup-anpassade cmdletar gör text mer korrekt.</span><span class="sxs-lookup"><span data-stu-id="73fd4-651">Azure Backup tuned cmdlets help text to be more accurate.</span></span>
* <span data-ttu-id="73fd4-652">Stöd har lagts till som gör att Azure Backup kan hämta MAB-agentjobb med cmdleten ”Get-AzRecoveryServicesBackupJob”.</span><span class="sxs-lookup"><span data-stu-id="73fd4-652">Azure Backup added support for fetching MAB agent jobs using 'Get-AzRecoveryServicesBackupJob' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="73fd4-653">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73fd4-653">Az.Resources</span></span>
* <span data-ttu-id="73fd4-654">”Save-AzResourceGroupDeploymentTemplate” har uppdaterats för att använda SDK:n.</span><span class="sxs-lookup"><span data-stu-id="73fd4-654">Updated 'Save-AzResourceGroupDeploymentTemplate' to use the SDK.</span></span>
* <span data-ttu-id="73fd4-655">Cmdleten ”Unregister-AzResourceProvider” har lagts till.</span><span class="sxs-lookup"><span data-stu-id="73fd4-655">Added 'Unregister-AzResourceProvider' cmdlet.</span></span>

#### <a name="azsql"></a><span data-ttu-id="73fd4-656">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73fd4-656">Az.Sql</span></span>
* <span data-ttu-id="73fd4-657">Stöd har lagts till för SPN och gästanvändare i cmdleten ”Set-AzSqlInstanceActiveDirectoryAdministrator”</span><span class="sxs-lookup"><span data-stu-id="73fd4-657">Added support for Service principal and guest users in Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet'</span></span>
* <span data-ttu-id="73fd4-658">En bugg har åtgärdats i cmdletar för dataklassificering.</span><span class="sxs-lookup"><span data-stu-id="73fd4-658">Fixed a bug in Data Classification cmdlets.'</span></span>
* <span data-ttu-id="73fd4-659">Stöd har lagts till för redundansväxling med Azure SQL Managed Instance: ”Invoke-AzSqlInstanceFailover”</span><span class="sxs-lookup"><span data-stu-id="73fd4-659">Added support for Azure SQL Managed Instance failover: 'Invoke-AzSqlInstanceFailover'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="73fd4-660">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="73fd4-660">Az.Storage</span></span>
* <span data-ttu-id="73fd4-661">Problemet som gjorde att UserAgent inte lades till för vissa cmdletar för dataplanet har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="73fd4-661">Fixed the issue that UserAgent is not added for some data plane cmdlets.</span></span>
* <span data-ttu-id="73fd4-662">Stöd har lagts till för att skapa/uppdatera Storage-konto med MinimumTlsVersion och AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="73fd4-662">Supported create/update Storage account with MinimumTlsVersion and AllowBlobPublicAccess</span></span>
    -  <span data-ttu-id="73fd4-663">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="73fd4-663">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="73fd4-664">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="73fd4-664">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="73fd4-665">Stöd har lagts till för att aktivera/inaktivera versionshantering i Blob Service för ett Storage-konto</span><span class="sxs-lookup"><span data-stu-id="73fd4-665">Support enable/disable versioning on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="73fd4-666">”Update-AzStorageBlobServiceProperty”</span><span class="sxs-lookup"><span data-stu-id="73fd4-666">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="73fd4-667">Stöd har lagts till för att visa blobar med blobversioner</span><span class="sxs-lookup"><span data-stu-id="73fd4-667">Support list blobs with blob versions</span></span>
    - <span data-ttu-id="73fd4-668">”Get-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="73fd4-668">'Get-AzStorageBlob'</span></span>
* <span data-ttu-id="73fd4-669">Stöd har lagts till för att hämta/ta bort enskilda ögonblicksbilder av blobar eller blobversioner</span><span class="sxs-lookup"><span data-stu-id="73fd4-669">Support get/remove single blob snapshot or blob version</span></span>
    - <span data-ttu-id="73fd4-670">”Get-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="73fd4-670">'Get-AzStorageBlob'</span></span>
    - <span data-ttu-id="73fd4-671">”Remove-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="73fd4-671">'Remove-AzStorageBlob'</span></span>
* <span data-ttu-id="73fd4-672">Stöd har lagts till för pipelines från blobobjekt genererade av Azure.Storage.Blobs V12</span><span class="sxs-lookup"><span data-stu-id="73fd4-672">Support pipeline from blob object generated from Azure.Storage.Blobs V12</span></span>
    - <span data-ttu-id="73fd4-673">”Get-AzStorageBlobContent”</span><span class="sxs-lookup"><span data-stu-id="73fd4-673">'Get-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="73fd4-674">”New-AzStorageBlobSASToken”</span><span class="sxs-lookup"><span data-stu-id="73fd4-674">'New-AzStorageBlobSASToken'</span></span>
    - <span data-ttu-id="73fd4-675">”Remove-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="73fd4-675">'Remove-AzStorageBlob'</span></span>
    - <span data-ttu-id="73fd4-676">”Set-AzStorageBlobContent”</span><span class="sxs-lookup"><span data-stu-id="73fd4-676">'Set-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="73fd4-677">”Start-AzStorageBlobCopy”</span><span class="sxs-lookup"><span data-stu-id="73fd4-677">'Start-AzStorageBlobCopy'</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="73fd4-678">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="73fd4-678">Az.StorageSync</span></span>
* <span data-ttu-id="73fd4-679">En ny version har lagts till för StorageSync SDK som körs mot ApiVersion 2020-03-01</span><span class="sxs-lookup"><span data-stu-id="73fd4-679">Added a new version StorageSync SDK targeting ApiVersion 2020-03-01</span></span>
* <span data-ttu-id="73fd4-680">En cmdlet för synkroniseringstjänsten för lagringsuppdatering har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-680">Added Update Storage Sync Service cmdlet</span></span>
    - <span data-ttu-id="73fd4-681">”Set-AzStorageSyncService”</span><span class="sxs-lookup"><span data-stu-id="73fd4-681">'Set-AzStorageSyncService'</span></span>
* <span data-ttu-id="73fd4-682">IncomingTrafficPolicy och PrivateEndpointConnections har lagts till för StorageSyncService-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="73fd4-682">Added IncomingTrafficPolicy and PrivateEndpointConnections to StorageSyncService cmdlets.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="73fd4-683">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="73fd4-683">Az.Websites</span></span>
* <span data-ttu-id="73fd4-684">Stöd har lagts till för att utföra åtgärder för platser som inte tillhör samma resursgrupp som App Services-planen</span><span class="sxs-lookup"><span data-stu-id="73fd4-684">Added support to perform operations for Slots not in the same resource group as the App Service Plan</span></span>

## <a name="430---june-2020"></a><span data-ttu-id="73fd4-685">4.3.0 – juni 2020</span><span class="sxs-lookup"><span data-stu-id="73fd4-685">4.3.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="73fd4-686">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73fd4-686">Az.Accounts</span></span>
* <span data-ttu-id="73fd4-687">Stöd för identifiering av miljöinställning som standard och tillägg av miljön via ”Add-AzEnvironment”</span><span class="sxs-lookup"><span data-stu-id="73fd4-687">Supported discovering environment setting by default and adding environment via 'Add-AzEnvironment'</span></span>
* <span data-ttu-id="73fd4-688">Uppdatera förinlästa sammansättningar [#12024], [#11976]</span><span class="sxs-lookup"><span data-stu-id="73fd4-688">Update preloaded assemblies [#12024], [#11976]</span></span>
* <span data-ttu-id="73fd4-689">Uppdaterad Azure.Core-sammansättning</span><span class="sxs-lookup"><span data-stu-id="73fd4-689">Updated Azure.Core assembly</span></span>
* <span data-ttu-id="73fd4-690">Ett problem har åtgärdats som kan orsaka att ”Connect-AzAccount” misslyckas vid körning av flera trådar [#11201]</span><span class="sxs-lookup"><span data-stu-id="73fd4-690">Fixed an issue that may cause 'Connect-AzAccount' to fail in multi-threaded execution [#11201]</span></span>

#### <a name="azaks"></a><span data-ttu-id="73fd4-691">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="73fd4-691">Az.Aks</span></span>
* <span data-ttu-id="73fd4-692">Användning av gamla [AccessProfile API](/rest/api/aks/managedclusters/getaccessprofile) ersattes med anrop till API:erna [ListClusterAdmin](/rest/api/aks/managedclusters/listclusteradmincredentials) och [ListClusterUser](/rest/api/aks/managedclusters/listclusterusercredentials)</span><span class="sxs-lookup"><span data-stu-id="73fd4-692">Replaced usage of old [AccessProfile API](/rest/api/aks/managedclusters/getaccessprofile) with calls to [ListClusterAdmin](/rest/api/aks/managedclusters/listclusteradmincredentials) and [ListClusterUser](/rest/api/aks/managedclusters/listclusterusercredentials) APIs</span></span>

#### <a name="azbatch"></a><span data-ttu-id="73fd4-693">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="73fd4-693">Az.Batch</span></span>
* <span data-ttu-id="73fd4-694">Az.Batch har uppdaterats att använda ”Microsoft.Azure.Management.Batch” SDK till och med version 11.0.0.</span><span class="sxs-lookup"><span data-stu-id="73fd4-694">Updated Az.Batch to use 'Microsoft.Azure.Management.Batch' SDK version to 11.0.0</span></span>
* <span data-ttu-id="73fd4-695">Möjligheten att ange BatchAccount-identiteten har lagts till i cmdleten ”New-AzBatchAccount”</span><span class="sxs-lookup"><span data-stu-id="73fd4-695">Added the ability to set the BatchAccount Identity in the 'New-AzBatchAccount' cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="73fd4-696">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="73fd4-696">Az.CognitiveServices</span></span>
* <span data-ttu-id="73fd4-697">Stöd för att visa kontofunktioner.</span><span class="sxs-lookup"><span data-stu-id="73fd4-697">Supported displaying account capabilities.</span></span>
* <span data-ttu-id="73fd4-698">Stöd för att ändra PublicNetworkAccess.</span><span class="sxs-lookup"><span data-stu-id="73fd4-698">Supported modifying PublicNetworkAccess.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73fd4-699">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73fd4-699">Az.Compute</span></span>
* <span data-ttu-id="73fd4-700">Parametern SimulateEviction har lagts till i cmdletarna set-AzVM och set-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="73fd4-700">Added SimulateEviction parameter to Set-AzVM and Set-AzVmssVM cmdlets.</span></span>
* <span data-ttu-id="73fd4-701">”Premium_LRS” har lagts till i argumentslutföraren för parametern StorageAccountType för cmdleten New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="73fd4-701">Added 'Premium_LRS' to the argument completer of StorageAccountType parameter for New-AzGalleryImageVersion cmdlet.</span></span>
* <span data-ttu-id="73fd4-702">Understatusar har lagts till i VMCustomScriptExtension [#11297]</span><span class="sxs-lookup"><span data-stu-id="73fd4-702">Added Substatuses to VMCustomScriptExtension [#11297]</span></span>
* <span data-ttu-id="73fd4-703">”Delete” har lagts till i argumentslutföraren för parametern EvictionPolicy för cmdletarna New-AzVM och New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="73fd4-703">Added 'Delete' to the argument completer of EvictionPolicy parameter for New-AzVM and New-AzVMConfig cmdlets.</span></span>
* <span data-ttu-id="73fd4-704">Åtgärdat namn för nytt VM-tillägg för SAP</span><span class="sxs-lookup"><span data-stu-id="73fd4-704">Fixed name of new VM Extension for SAP</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="73fd4-705">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="73fd4-705">Az.DataFactory</span></span>
* <span data-ttu-id="73fd4-706">ADF .Net SDK har uppdaterats till 4.9.0</span><span class="sxs-lookup"><span data-stu-id="73fd4-706">Updated ADF .Net SDK version to 4.9.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="73fd4-707">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="73fd4-707">Az.EventHub</span></span>
* <span data-ttu-id="73fd4-708">Parametrar för hanterad identitet har lagts till i cmdletarna ”New-AzEventHubNamespace” och ”set-AzEventHubNamespace”</span><span class="sxs-lookup"><span data-stu-id="73fd4-708">Added Managed Identity parameters to 'New-AzEventHubNamespace' and 'Set-AzEventHubNamespace' cmdlets</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="73fd4-709">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="73fd4-709">Az.Functions</span></span>
* <span data-ttu-id="73fd4-710">Stöd har lagts till för att skapa PowerShell 7.0- och Java 11-funktionsappar</span><span class="sxs-lookup"><span data-stu-id="73fd4-710">Added support to create PowerShell 7.0 and Java 11 function apps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="73fd4-711">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="73fd4-711">Az.HDInsight</span></span>
* <span data-ttu-id="73fd4-712">Stöd för listning av värdar och omstart för specifika värdar i HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="73fd4-712">Supported listing hosts and restart specific hosts of the HDInsight cluster.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="73fd4-713">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="73fd4-713">Az.HealthcareApis</span></span>
* <span data-ttu-id="73fd4-714">Uppdaterade SDK-versionen till 1.1.0</span><span class="sxs-lookup"><span data-stu-id="73fd4-714">Updated the SDK version to 1.1.0</span></span>
* <span data-ttu-id="73fd4-715">Stöd har lagts till för exportinställningar och hanterad identitet</span><span class="sxs-lookup"><span data-stu-id="73fd4-715">Added support for Export settings and Managed Identity</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="73fd4-716">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="73fd4-716">Az.Monitor</span></span>
* <span data-ttu-id="73fd4-717">Parameter för inmatningsobjekt har åtgärdats för ”Set-AzActivityLogAlert”</span><span class="sxs-lookup"><span data-stu-id="73fd4-717">Fixed input object parameter for 'Set-AzActivityLogAlert'</span></span>
* <span data-ttu-id="73fd4-718">Parametern ”InputObject” har åtgärdats för ”Set-AzActionGroup” [#10868]</span><span class="sxs-lookup"><span data-stu-id="73fd4-718">Fixed 'InputObject' parameter for 'Set-AzActionGroup' [#10868]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73fd4-719">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73fd4-719">Az.Network</span></span>
* <span data-ttu-id="73fd4-720">Stöd har lagts till för parametern AddressPrefixType i ”Remove-AzExpressRouteCircuitConnectionConfig”</span><span class="sxs-lookup"><span data-stu-id="73fd4-720">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="73fd4-721">Nya cmdletar har lagts till för Azure FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="73fd4-721">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="73fd4-722">”New-AzFirewallPolicyDnsSetting”</span><span class="sxs-lookup"><span data-stu-id="73fd4-722">'New-AzFirewallPolicyDnsSetting'</span></span>
    - <span data-ttu-id="73fd4-723">Stöd för mål-FQDN i nätverksregler för brandväggsprincip</span><span class="sxs-lookup"><span data-stu-id="73fd4-723">Support for Destination FQDN in Network Rules for Firewall Policy</span></span>
* <span data-ttu-id="73fd4-724">Stöd har lagts till för åtgärder i serverdelsadresspooler</span><span class="sxs-lookup"><span data-stu-id="73fd4-724">Added support for backend address pool operations</span></span>
    - <span data-ttu-id="73fd4-725">”New-AzLoadBalancerBackendAddressConfig”</span><span class="sxs-lookup"><span data-stu-id="73fd4-725">'New-AzLoadBalancerBackendAddressConfig'</span></span>
    - <span data-ttu-id="73fd4-726">”New-AzLoadBalancerBackendAddressPool”</span><span class="sxs-lookup"><span data-stu-id="73fd4-726">'New-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="73fd4-727">”Set-AzLoadBalancerBackendAddressPool”</span><span class="sxs-lookup"><span data-stu-id="73fd4-727">'Set-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="73fd4-728">”Remove-AzLoadBalancerBackendAddressPool”</span><span class="sxs-lookup"><span data-stu-id="73fd4-728">'Remove-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="73fd4-729">”Get-AzLoadBalancerBackendAddressPool”</span><span class="sxs-lookup"><span data-stu-id="73fd4-729">'Get-AzLoadBalancerBackendAddressPool'</span></span>
* <span data-ttu-id="73fd4-730">Namnvalidering har lagts till för ”New-AzIpGroup”</span><span class="sxs-lookup"><span data-stu-id="73fd4-730">Added name validation for 'New-AzIpGroup'</span></span>
* <span data-ttu-id="73fd4-731">Nya cmdletar har lagts till för Azure FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="73fd4-731">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="73fd4-732">”New-AzFirewallPolicyThreatIntelWhitelist”</span><span class="sxs-lookup"><span data-stu-id="73fd4-732">'New-AzFirewallPolicyThreatIntelWhitelist'</span></span>
* <span data-ttu-id="73fd4-733">Nedanstående kommandon för funktionen har uppdaterats: Konfiguration/borttagning av anpassade DNS-servrar på VirtualWan P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="73fd4-733">Updated below commands for feature: Custom dns servers set/remove on VirtualWan P2SVpnGateway.</span></span>
    - <span data-ttu-id="73fd4-734">New-AzP2sVpnGateway har uppdaterats: Den valfria parametern ”-CustomDnsServer” har lagts till för att kunder ska kunna ange att deras DNS-servrar ska konfigureras på P2SVpnGateway, som kan användas av punkt-till-plats-klienter.</span><span class="sxs-lookup"><span data-stu-id="73fd4-734">Updated New-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
    - <span data-ttu-id="73fd4-735">Update-AzP2sVpnGateway har uppdaterats: Den valfria parametern ”-CustomDnsServer” har lagts till för att kunder ska kunna ange att deras DNS-servrar ska konfigureras på P2SVpnGateway, som kan användas av punkt-till-plats-klienter.</span><span class="sxs-lookup"><span data-stu-id="73fd4-735">Updated Update-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
* <span data-ttu-id="73fd4-736">”Update-AzVpnGateway” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="73fd4-736">Updated 'Update-AzVpnGateway'</span></span>
    - <span data-ttu-id="73fd4-737">Den valfria parametern ”-BgpPeeringAddress” har lagts till för att kunder ska kunna ange sina anpassade BGP:er som ska konfigurerar på VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="73fd4-737">Added optional parameter '-BgpPeeringAddress' for customers to specify their custom bgps to set on VpnGateway.</span></span>
* <span data-ttu-id="73fd4-738">Ny cmdlet har lagts till för att stödja återställning av en VirtualHub-resurs routningsstatus:</span><span class="sxs-lookup"><span data-stu-id="73fd4-738">Added new cmdlet to support resetting the routing state of a VirtualHub resource:</span></span>
    - <span data-ttu-id="73fd4-739">”Reset-AzHubRouter”</span><span class="sxs-lookup"><span data-stu-id="73fd4-739">'Reset-AzHubRouter'</span></span>
* <span data-ttu-id="73fd4-740">Nedanstående saker har uppdaterats baserat på den senaste Swagger-ändringen för brandväggspolicyn</span><span class="sxs-lookup"><span data-stu-id="73fd4-740">Updated below things based on recent swagger change for Firewall Policy</span></span>
    - <span data-ttu-id="73fd4-741">Namn ändras för RuleGroup, RuleCollectionGroup och RuleType</span><span class="sxs-lookup"><span data-stu-id="73fd4-741">Changes names for RuleGroup, RuleCollectionGroup and RuleType</span></span>
    - <span data-ttu-id="73fd4-742">Stöd har lagts till för NAT-regelsamlingar för brandväggsprincip så att flera NAT-regelsamlingar stöds</span><span class="sxs-lookup"><span data-stu-id="73fd4-742">Added support for Firewall Policy NAT Rule Collections to support multiple NAT Rule Collection</span></span>
* <span data-ttu-id="73fd4-743">[Icke-bakåtkompatibel ändring] Den obligatoriska parametern ”SourceIpGroup” har lagts till för ”New-AzFirewallPolicyApplicationRule” och ”New-AzFirewallPolicyNetworkRule”.</span><span class="sxs-lookup"><span data-stu-id="73fd4-743">[Breaking Change] Added mandatory parameter 'SourceIpGroup' for 'New-AzFirewallPolicyApplicationRule' and 'New-AzFirewallPolicyNetworkRule'.</span></span>
* <span data-ttu-id="73fd4-744">[Icke-bakåtkompatibel ändring] ”New-AzFirewallPolicyApplicationRule” har åtgärdats, parametern ”SourceAddress” är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="73fd4-744">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="73fd4-745">[Icke-bakåtkompatibel ändring] ”New-AzFirewallPolicyApplicationRule” har åtgärdats, parametern ”SourceAddress” är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="73fd4-745">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="73fd4-746">[Icke-bakåtkompatibel ändring] Obligatoriska parametrar har tagits bort: ”TranslatedAddress”, ”TranslatedPort” för ”New-AzFirewallPolicyNatRuleCollection”.</span><span class="sxs-lookup"><span data-stu-id="73fd4-746">[Breaking Change] Removed mandatory parameters: 'TranslatedAddress', 'TranslatedPort' for 'New-AzFirewallPolicyNatRuleCollection'.</span></span>
* <span data-ttu-id="73fd4-747">Nya cmdletar har lagts till för att stödja PrivateLink på Application Gateway</span><span class="sxs-lookup"><span data-stu-id="73fd4-747">Added new cmdlets to support PrivateLink On Application Gateway</span></span>
    - <span data-ttu-id="73fd4-748">”New-AzApplicationGatewayPrivateLinkConfiguration”</span><span class="sxs-lookup"><span data-stu-id="73fd4-748">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="73fd4-749">”Get-AzApplicationGatewayPrivateLinkConfiguration”</span><span class="sxs-lookup"><span data-stu-id="73fd4-749">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="73fd4-750">”New-AzApplicationGatewayPrivateLinkConfiguration”</span><span class="sxs-lookup"><span data-stu-id="73fd4-750">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="73fd4-751">”Set-AzApplicationGatewayPrivateLinkConfiguration”</span><span class="sxs-lookup"><span data-stu-id="73fd4-751">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="73fd4-752">”Remove-AzApplicationGatewayPrivateLinkConfiguration”</span><span class="sxs-lookup"><span data-stu-id="73fd4-752">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="73fd4-753">”New-AzApplicationGatewayPrivateLinkIpConfiguration”</span><span class="sxs-lookup"><span data-stu-id="73fd4-753">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span></span>
* <span data-ttu-id="73fd4-754">Nya cmdletar har lagts till för VirtualHubs underordnade resurs HubRouteTables.</span><span class="sxs-lookup"><span data-stu-id="73fd4-754">Added new cmdlets for HubRouteTables child resource of VirtualHub.</span></span>
    - <span data-ttu-id="73fd4-755">”New-AzVHubRoute”</span><span class="sxs-lookup"><span data-stu-id="73fd4-755">'New-AzVHubRoute'</span></span>
    - <span data-ttu-id="73fd4-756">”New-AzVHubRouteTable”</span><span class="sxs-lookup"><span data-stu-id="73fd4-756">'New-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="73fd4-757">”Get-AzVHubRouteTable”</span><span class="sxs-lookup"><span data-stu-id="73fd4-757">'Get-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="73fd4-758">”Update-AzVHubRouteTable”</span><span class="sxs-lookup"><span data-stu-id="73fd4-758">'Update-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="73fd4-759">”Remove-AzVHubRouteTable”</span><span class="sxs-lookup"><span data-stu-id="73fd4-759">'Remove-AzVHubRouteTable'</span></span>
* <span data-ttu-id="73fd4-760">Befintliga cmdletar har uppdaterats för att stödja valfri RoutingConfiguration-indataparameter för anpassad routning i VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="73fd4-760">Updated existing cmdlets to support optional RoutingConfiguration input parameter for custom routing in VirtualWan.</span></span>
    - <span data-ttu-id="73fd4-761">”New-AzExpressRouteConnection”</span><span class="sxs-lookup"><span data-stu-id="73fd4-761">'New-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="73fd4-762">”Set-AzExpressRouteConnection”</span><span class="sxs-lookup"><span data-stu-id="73fd4-762">'Set-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="73fd4-763">”New-AzVirtualHubVnetConnection”</span><span class="sxs-lookup"><span data-stu-id="73fd4-763">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="73fd4-764">”Update-AzVirtualHubVnetConnection”</span><span class="sxs-lookup"><span data-stu-id="73fd4-764">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="73fd4-765">”New-AzVpnConnection”</span><span class="sxs-lookup"><span data-stu-id="73fd4-765">'New-AzVpnConnection'</span></span>
    - <span data-ttu-id="73fd4-766">”Update-AzVpnConnection”</span><span class="sxs-lookup"><span data-stu-id="73fd4-766">'Update-AzVpnConnection'</span></span>
    - <span data-ttu-id="73fd4-767">”New-AzP2sVpnGateway”</span><span class="sxs-lookup"><span data-stu-id="73fd4-767">'New-AzP2sVpnGateway'</span></span>
    - <span data-ttu-id="73fd4-768">”Update-AzP2sVpnGateway”</span><span class="sxs-lookup"><span data-stu-id="73fd4-768">'Update-AzP2sVpnGateway'</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="73fd4-769">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="73fd4-769">Az.OperationalInsights</span></span>
* <span data-ttu-id="73fd4-770">Fast fel PSWorkspace implementerar inte IOperationalInsightsWorkspace [#12135]</span><span class="sxs-lookup"><span data-stu-id="73fd4-770">Fixed bug PSWorkspace doesn't implement IOperationalInsightsWorkspace [#12135]</span></span>
* <span data-ttu-id="73fd4-771">”pergb2018” har lagts till i uppsättningen med giltiga värden för parametern ”Sku” i ”Set-AzOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="73fd4-771">Added 'pergb2018' to valid value set of parameter 'Sku' in 'Set-AzOperationalInsightsWorkspace'</span></span> 
* <span data-ttu-id="73fd4-772">Alias ”FunctionParameters” lades till för parametern ”FunctionParameter” till</span><span class="sxs-lookup"><span data-stu-id="73fd4-772">Added alias 'FunctionParameters' for parameter 'FunctionParameter' to</span></span>
    - <span data-ttu-id="73fd4-773">”New-AzOperationalInsightsSavedSearch”</span><span class="sxs-lookup"><span data-stu-id="73fd4-773">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="73fd4-774">”Set-AzOperationalInsightsSavedSearch”</span><span class="sxs-lookup"><span data-stu-id="73fd4-774">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="73fd4-775">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="73fd4-775">Az.RecoveryServices</span></span>
* <span data-ttu-id="73fd4-776">Azure Backup har fått stöd för att hämta MAB-objekt.</span><span class="sxs-lookup"><span data-stu-id="73fd4-776">Azure Backup added support for fetching MAB items.</span></span>
* <span data-ttu-id="73fd4-777">Azure Site Recovery stöder disktypen ”StandardSSD_LRS”</span><span class="sxs-lookup"><span data-stu-id="73fd4-777">Azure Site Recovery supports disk type 'StandardSSD_LRS'</span></span>

#### <a name="azresources"></a><span data-ttu-id="73fd4-778">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73fd4-778">Az.Resources</span></span>
* <span data-ttu-id="73fd4-779">”UsageLocation”, ”GivenName”, ”Surname”, ”AccountEnabled”, ”MailNickname”, ”Mail” på ”PSADUser” lades till [#10526] [#10497]</span><span class="sxs-lookup"><span data-stu-id="73fd4-779">Added 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' on 'PSADUser' [#10526] [#10497]</span></span>
* <span data-ttu-id="73fd4-780">Problem med att ”-Mail” inte fungerar på ”Get-AzADUser” har åtgärdats [#11981]</span><span class="sxs-lookup"><span data-stu-id="73fd4-780">Fixed issue that '-Mail' doesn't work on 'Get-AzADUser' [#11981]</span></span>
* <span data-ttu-id="73fd4-781">Parametern ”-ExcludeChangeType” har lagts till i ”Get-AzDeploymentWhatIfResult” och ”Get-AzResourceGroupDeploymentWhatIfResult”</span><span class="sxs-lookup"><span data-stu-id="73fd4-781">Added '-ExcludeChangeType' parameter to 'Get-AzDeploymentWhatIfResult' and 'Get-AzResourceGroupDeploymentWhatIfResult'</span></span>
* <span data-ttu-id="73fd4-782">Parametern ”-WhatIfExcludeChangeType” har lagts till i ”New-AzDeployment” och ”New-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="73fd4-782">Added '-WhatIfExcludeChangeType' parameter to 'New-AzDeployment' and 'New-AzResourceGroupDeployment'</span></span>
* <span data-ttu-id="73fd4-783">Cmdletar för ”Test-Az\*Deployment” har uppdaterats för att visa bättre felmeddelanden</span><span class="sxs-lookup"><span data-stu-id="73fd4-783">Updated 'Test-Az\*Deployment' cmdlets to show better error messages</span></span>
* <span data-ttu-id="73fd4-784">Hjälpmeddelandet för parametern ”-Name” i distributionsskapande och What If-cmdletar</span><span class="sxs-lookup"><span data-stu-id="73fd4-784">Fixed help message for '-Name' parameter of deployment create and What-If cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="73fd4-785">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73fd4-785">Az.Sql</span></span>
* <span data-ttu-id="73fd4-786">Stöd för tjänsthuvudnamn har lagts till för administratörs-cmdlet för SQL Server Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="73fd4-786">Added support for service principal for Set SQL Server Azure Active Directory Admin cmdlet</span></span>
* <span data-ttu-id="73fd4-787">Synkroniseringsproblem i Data Classification-cmdletar har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="73fd4-787">Fixed sync issue in Data Classification cmdlets.</span></span>
* <span data-ttu-id="73fd4-788">Stöd för att söka efter användare via e-postadress på ”Set-AzSqlServerActiveDirectoryAdministrator” [#12192]</span><span class="sxs-lookup"><span data-stu-id="73fd4-788">Supported searching user by mail on 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span></span>

#### <a name="azstorage"></a><span data-ttu-id="73fd4-789">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="73fd4-789">Az.Storage</span></span>
* <span data-ttu-id="73fd4-790">Skapa lagringskonto med RequireInfrastructureEncryption stöds</span><span class="sxs-lookup"><span data-stu-id="73fd4-790">Supported create Storage account with RequireInfrastructureEncryption</span></span>
    -  <span data-ttu-id="73fd4-791">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="73fd4-791">'New-AzStorageAccount'</span></span>
* <span data-ttu-id="73fd4-792">Logiken för inläsning av Azure.Core flyttades till Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73fd4-792">Moved the logic of loading Azure.Core to Az.Accounts</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="73fd4-793">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="73fd4-793">Az.Websites</span></span>
* <span data-ttu-id="73fd4-794">Skydd för att ta bort skapad webapp om återställningen misslyckades har lagts till i ”Restore-AzDeletedWebApp”</span><span class="sxs-lookup"><span data-stu-id="73fd4-794">Added safeguard to delete created webapp if restore failed in 'Restore-AzDeletedWebApp'</span></span>
* <span data-ttu-id="73fd4-795">”SourceWebApp.Location” har lagts till för ”New-AzWebApp” och ”New-AzWebAppSlot”</span><span class="sxs-lookup"><span data-stu-id="73fd4-795">Added 'SourceWebApp.Location' for 'New-AzWebApp' and 'New-AzWebAppSlot'</span></span>
* <span data-ttu-id="73fd4-796">Fel som förhindrade ändring av containerinställningar i ”Set-AzWebApp” och ”Set-AzWebAppSlot” har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="73fd4-796">Fixed bug that prevented changing Container settings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>
* <span data-ttu-id="73fd4-797">Ett fel för att hämta SiteConfig när -Name inte anges för Get-AzWebApp har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="73fd4-797">Fixed bug to get SiteConfig when -Name is not given for Get-AzWebApp</span></span>
* <span data-ttu-id="73fd4-798">Stöd har lagts till för att skapa ASP för Linux-appar</span><span class="sxs-lookup"><span data-stu-id="73fd4-798">Added a support to create ASP for Linux Apps</span></span>
* <span data-ttu-id="73fd4-799">Undantag har lagts till för kloning över resursgrupper</span><span class="sxs-lookup"><span data-stu-id="73fd4-799">Added exceptions for clone across resource groups</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="73fd4-800">4.2.0 – juni 2020</span><span class="sxs-lookup"><span data-stu-id="73fd4-800">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="73fd4-801">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73fd4-801">Az.Accounts</span></span>
* <span data-ttu-id="73fd4-802">Åtgärdade ett problem som kan få Az att hoppa över loggar i Azure Automation- eller PowerShell-jobb [#11492]</span><span class="sxs-lookup"><span data-stu-id="73fd4-802">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="73fd4-803">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="73fd4-803">Az.AnalysisServices</span></span>
* <span data-ttu-id="73fd4-804">Uppdaterad sammansättningsversion för dataplan-cmdletar</span><span class="sxs-lookup"><span data-stu-id="73fd4-804">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="73fd4-805">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="73fd4-805">Az.ApiManagement</span></span>
* <span data-ttu-id="73fd4-806">Uppdaterad sammansättningsversion för cmdletar för tjänsthantering</span><span class="sxs-lookup"><span data-stu-id="73fd4-806">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="73fd4-807">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="73fd4-807">Az.Billing</span></span>
* <span data-ttu-id="73fd4-808">Uppdaterad sammansättningsversion för förbrukningscmdletar</span><span class="sxs-lookup"><span data-stu-id="73fd4-808">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="73fd4-809">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="73fd4-809">Az.CognitiveServices</span></span>
* <span data-ttu-id="73fd4-810">Stöd för PrivateEndpoint- och PublicNetworkAccess-kontroll.</span><span class="sxs-lookup"><span data-stu-id="73fd4-810">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="73fd4-811">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="73fd4-811">Az.DataFactory</span></span>
* <span data-ttu-id="73fd4-812">Uppdaterad sammansättningsversion för datafabrik V2-cmdletar</span><span class="sxs-lookup"><span data-stu-id="73fd4-812">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="73fd4-813">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="73fd4-813">Az.DataShare</span></span>
* <span data-ttu-id="73fd4-814">Allmän tillgänglighet för modulen ”Az.DataShare”</span><span class="sxs-lookup"><span data-stu-id="73fd4-814">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="73fd4-815">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="73fd4-815">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="73fd4-816">Allmän tillgänglighet för modulen ”Az.DesktopVirtualization”</span><span class="sxs-lookup"><span data-stu-id="73fd4-816">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="73fd4-817">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="73fd4-817">Az.OperationalInsights</span></span>
* <span data-ttu-id="73fd4-818">Uppgraderad SDK till 0.21.0</span><span class="sxs-lookup"><span data-stu-id="73fd4-818">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="73fd4-819">Lade till valfria parametrar till</span><span class="sxs-lookup"><span data-stu-id="73fd4-819">Added optional parameters to</span></span> 
    - <span data-ttu-id="73fd4-820">”New-AzOperationalInsightsSavedSearch”</span><span class="sxs-lookup"><span data-stu-id="73fd4-820">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="73fd4-821">”Set-AzOperationalInsightsSavedSearch”</span><span class="sxs-lookup"><span data-stu-id="73fd4-821">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="73fd4-822">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="73fd4-822">Az.PolicyInsights</span></span>
* <span data-ttu-id="73fd4-823">Korrigerade exempel 3 för ”Start-AzPolicyComplianceScan”</span><span class="sxs-lookup"><span data-stu-id="73fd4-823">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="73fd4-824">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="73fd4-824">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="73fd4-825">Uppdaterad sammansättningsversion för PowerBI-cmdletar</span><span class="sxs-lookup"><span data-stu-id="73fd4-825">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="73fd4-826">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="73fd4-826">Az.PrivateDns</span></span>
* <span data-ttu-id="73fd4-827">Korrigerade formatering av utförlig utdatasträng för Remove-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="73fd4-827">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="73fd4-828">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="73fd4-828">Az.RecoveryServices</span></span>
* <span data-ttu-id="73fd4-829">Azure Site Recovery-stöd för att skapa en återställningsplan för replikering mellan zoner från xml-indata.</span><span class="sxs-lookup"><span data-stu-id="73fd4-829">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="73fd4-830">Uppdaterad sammansättningsversion för cmdletar för SiteRecovery och Backup</span><span class="sxs-lookup"><span data-stu-id="73fd4-830">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="73fd4-831">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73fd4-831">Az.Resources</span></span>
* <span data-ttu-id="73fd4-832">Lade till slutparameter för cmdletarna Get-AzDeploymentScriptLog och Save-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="73fd4-832">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="73fd4-833">Formaterad utdataegenskap så att den kan visas i cmdlet-utdata för Get-AzDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="73fd4-833">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="73fd4-834">Bytte namn på parametern -DeploymentScriptInputObject till -DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="73fd4-834">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="73fd4-835">Åtgärdade saknade fil/målnamn i cmdlet-meddelanden.</span><span class="sxs-lookup"><span data-stu-id="73fd4-835">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="73fd4-836">Uppdaterad sammansättningsversion för cmdletar för resurshanterare och taggar</span><span class="sxs-lookup"><span data-stu-id="73fd4-836">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="73fd4-837">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73fd4-837">Az.Sql</span></span>
* <span data-ttu-id="73fd4-838">Lade till UsePrivateLinkConnection till ”New-AzSqlSyncGroup”, ”Update-AzSqlSyncGroup”, ”New-AzSqlSyncMember” och ”Update-AzSqlSyncMember”</span><span class="sxs-lookup"><span data-stu-id="73fd4-838">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="73fd4-839">Lade till SyncMemberAzureDatabaseResourceId till ”New-AzSqlSyncMember” and ”Update-AzSqlSyncMember”</span><span class="sxs-lookup"><span data-stu-id="73fd4-839">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="73fd4-840">Lade till stöd för att söka efter gästanvändare för att ange administratörs-cmdlet för SQL Server Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="73fd4-840">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="73fd4-841">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="73fd4-841">Az.Storage</span></span>
* <span data-ttu-id="73fd4-842">Uppdaterad sammansättningsversion för dataplan-cmdletar</span><span class="sxs-lookup"><span data-stu-id="73fd4-842">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="73fd4-843">4.1.0 – maj 2020</span><span class="sxs-lookup"><span data-stu-id="73fd4-843">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="73fd4-844">Höjdpunkter sedan den senaste uppdateringen</span><span class="sxs-lookup"><span data-stu-id="73fd4-844">Highlights since the last release</span></span>
* <span data-ttu-id="73fd4-845">PowerShell-versioner som stöds: Windows PowerShell 5.1, PowerShell Core 6.2.4+ och PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="73fd4-845">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="73fd4-846">Allmän tillgänglighet för Az.Functions</span><span class="sxs-lookup"><span data-stu-id="73fd4-846">General availability of Az.Functions</span></span> 
* <span data-ttu-id="73fd4-847">Nya stora uppdateringar har gjorts för Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources och Az.Storage</span><span class="sxs-lookup"><span data-stu-id="73fd4-847">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="73fd4-848">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73fd4-848">Az.Accounts</span></span>
* <span data-ttu-id="73fd4-849">”Add-AzEnvironment” och ”Set-AzEnvironment” har uppdaterats med stöd för parametrarna ”AzureSynapseAnalyticsEndpointResourceId” och ”AzureSynapseAnalyticsEndpointSuffix”</span><span class="sxs-lookup"><span data-stu-id="73fd4-849">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="73fd4-850">Azure.Core-relaterade sammansättningar har lagts till i Az.Accounts; PowerShell-plattformar som stöds är Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span><span class="sxs-lookup"><span data-stu-id="73fd4-850">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="73fd4-851">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="73fd4-851">Az.Aks</span></span>
* <span data-ttu-id="73fd4-852">API-versionen har uppgraderats till 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="73fd4-852">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="73fd4-853">Stöds för att skapa AKS med hjälp av Windows-container</span><span class="sxs-lookup"><span data-stu-id="73fd4-853">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="73fd4-854">Nya cmdletar är tillgängliga: ”New-AzAksNodePool”, ”Update-AzAksNodePool”, ”Remove-AzAksNodePool”,        ”Get-AzAksNodePool”, ”Install-AzAksKubectl”, ”Get-AzAksVersion”</span><span class="sxs-lookup"><span data-stu-id="73fd4-854">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="73fd4-855">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="73fd4-855">Az.ApiManagement</span></span>
* <span data-ttu-id="73fd4-856">Parametrarna ”New-AzApiManagement” och ”Set-AzApiManagement”: [-AssignIdentity] har bytt namn till [-SystemAssignedIdentity]</span><span class="sxs-lookup"><span data-stu-id="73fd4-856">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="73fd4-857">”New-AzApiManagement” och ”Set-AzApiManagement”: En ny parameter har lagts till: [-UserAssignedIdentity <String[]>]</span><span class="sxs-lookup"><span data-stu-id="73fd4-857">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="73fd4-858">”Get-AzApiManagementProperty” har bytt namn till ”Get-AzApiManagementNamedValue”.</span><span class="sxs-lookup"><span data-stu-id="73fd4-858">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="73fd4-859">PropertyId-parametern har bytt namn till NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="73fd4-859">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="73fd4-860">”New-AzApiManagementProperty” har bytt namn till ”New-AzApiManagementNamedValue”.</span><span class="sxs-lookup"><span data-stu-id="73fd4-860">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="73fd4-861">PropertyId-parametern har bytt namn till NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="73fd4-861">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="73fd4-862">”Set-AzApiManagementProperty” har bytt namn till ”Set-AzApiManagementNamedValue”.</span><span class="sxs-lookup"><span data-stu-id="73fd4-862">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="73fd4-863">PropertyId-parametern har bytt namn till NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="73fd4-863">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="73fd4-864">”Remove-AzApiManagementProperty” har bytt namn till ”Remove-AzApiManagementNamedValue”.</span><span class="sxs-lookup"><span data-stu-id="73fd4-864">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="73fd4-865">PropertyId-parametern har bytt namn till NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="73fd4-865">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="73fd4-866">Den nya cmdleten Get-AzApiManagementAuthorizationServerClientSecret gör att ”Get-AzApiManagementAuthorizationServer” inte längre returnerar klienthemligheter.</span><span class="sxs-lookup"><span data-stu-id="73fd4-866">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="73fd4-867">Den nya cmdleten ”Get-AzApiManagementNamedValueSecretValue” gör att ”Get-AzApiManagementNamedValue” inte returnerar värdet för en hemlighet.</span><span class="sxs-lookup"><span data-stu-id="73fd4-867">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="73fd4-868">Den nya cmdleten ”Get-AzApiManagementOpenIdConnectProviderClientSecret” gör att ”Get-AzApiManagementOpenIdConnectProvider” inte längre returnerar klienthemligheter.</span><span class="sxs-lookup"><span data-stu-id="73fd4-868">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="73fd4-869">Den nya cmdleten ”Get-AzApiManagementSubscriptionKey” gör att ”Get-AzApiManagementSubscription” inte längre returnerar prenumerationsnycklar.</span><span class="sxs-lookup"><span data-stu-id="73fd4-869">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="73fd4-870">Den nya cmdleten ”Get-AzApiManagementTenantAccessSecret” gör att ”Get-AzApiManagementTenantAccess” inte längre returnerar nycklar.</span><span class="sxs-lookup"><span data-stu-id="73fd4-870">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="73fd4-871">Den nya cmdleten ”Get-AzApiManagementTenantGitAccessSecret” gör att ”Get-AzApiManagementTenantGitAccess” inte längre returnerar nycklar.</span><span class="sxs-lookup"><span data-stu-id="73fd4-871">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="73fd4-872">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="73fd4-872">Az.ApplicationInsights</span></span>
* <span data-ttu-id="73fd4-873">Tillagda parametrar: ”RetentionInDays” ”PublicNetworkAccessForIngestion” ”PublicNetworkAccessForQuery” för ”New-AzApplicationInsights”</span><span class="sxs-lookup"><span data-stu-id="73fd4-873">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="73fd4-874">Cmdleten ”Update-AzApplicationInsights” har skapats</span><span class="sxs-lookup"><span data-stu-id="73fd4-874">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="73fd4-875">Cmdletar har skapats för länkat lagringskonto</span><span class="sxs-lookup"><span data-stu-id="73fd4-875">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="73fd4-876">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="73fd4-876">Az.Batch</span></span>
* <span data-ttu-id="73fd4-877">Az.Batch har uppdaterats att använda ”Microsoft.Azure.Batch” SDK version 13.0.0 och ”Microsoft.Azure.Management.Batch” SDK version 9.0.0.</span><span class="sxs-lookup"><span data-stu-id="73fd4-877">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="73fd4-878">Nu kan du välja vilken typ av certifikat du lägger till genom att använda den nya parametern ”-CertificateKind” med ”New-AzBatchCertificate”.</span><span class="sxs-lookup"><span data-stu-id="73fd4-878">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="73fd4-879">Egenskapen ”ApplicationPackages” har tagits bort från ”PSApplication”, som tidigare alltid var ''.</span><span class="sxs-lookup"><span data-stu-id="73fd4-879">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="73fd4-880">Specifika paket i ett program kan nu hämtas med hjälp av ”Get-AzBatchApplicationPackage”.</span><span class="sxs-lookup"><span data-stu-id="73fd4-880">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="73fd4-881">Ett exempel: ”Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication”.</span><span class="sxs-lookup"><span data-stu-id="73fd4-881">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="73fd4-882">Nu när du skapar en pool med hjälp av ”New-AzBatchPool” kan egenskapen ”VirtualMachineImageId” för ”PSImageReference” endast referera till en Shared Image Gallery-avbildning.</span><span class="sxs-lookup"><span data-stu-id="73fd4-882">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="73fd4-883">När du skapar en pool med hjälp av ”New-AzBatchPool” kan poolen etableras utan en offentlig IP-adress med hjälp av den nya egenskapen ”PublicIPAddressConfiguration” för ”PSNetworkConfiguration”.</span><span class="sxs-lookup"><span data-stu-id="73fd4-883">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="73fd4-884">Egenskapen ”PublicIPs” för ”PSNetworkConfiguration” har också flyttats till ”PSPublicIPAddressConfiguration”.</span><span class="sxs-lookup"><span data-stu-id="73fd4-884">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="73fd4-885">Den här egenskapen kan bara anges om ”IPAddressProvisioningType” är ”UserManaged”.</span><span class="sxs-lookup"><span data-stu-id="73fd4-885">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73fd4-886">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73fd4-886">Az.Compute</span></span>
* <span data-ttu-id="73fd4-887">Parametern HostId har lagts till för cmdleten ”Update-AzVM”t</span><span class="sxs-lookup"><span data-stu-id="73fd4-887">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="73fd4-888">Hjälpdokumenten har uppdaterats för cmdletarna ”New-AzVMConfig”, ”New-AzVmssConfig”, ”Update-AzVmss”, ”Set-AzVMOperatingSystem” och ”Set-AzVmssOsProfile”.</span><span class="sxs-lookup"><span data-stu-id="73fd4-888">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="73fd4-889">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="73fd4-889">Breaking changes</span></span>
    - <span data-ttu-id="73fd4-890">Parametern FilterExpression tas bort från cmdleten ”Get-AzVMImage”.</span><span class="sxs-lookup"><span data-stu-id="73fd4-890">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="73fd4-891">Parametern AssignIdentity tas bort från cmdletarna ”New-AzVmssConfig”, ”New-AzVMConfig” och ”Update-AzVM”.</span><span class="sxs-lookup"><span data-stu-id="73fd4-891">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="73fd4-892">AutomaticRepairMaxInstanceRepairsPercent tas bort från cmdletarna ”New-AzVmssConfig” och ”Update-AzVmss”.</span><span class="sxs-lookup"><span data-stu-id="73fd4-892">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="73fd4-893">Egenskaperna AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus och VirtualMachineScaleSetsColocationStatus tas bort från ProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="73fd4-893">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="73fd4-894">Egenskapen MaxInstanceRepairsPercent tas bort från AutomaticRepairsPolicy.</span><span class="sxs-lookup"><span data-stu-id="73fd4-894">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="73fd4-895">Typerna AvailabilitySets, VirtualMachines och VirtualMachineScaleSets ändras från IList<SubResource> till IList<SubResourceWithColocationStatus>.</span><span class="sxs-lookup"><span data-stu-id="73fd4-895">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="73fd4-896">Beskrivningen för cmdleten ”Get-AzVM” har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="73fd4-896">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="73fd4-897">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="73fd4-897">Az.DataFactory</span></span>
* <span data-ttu-id="73fd4-898">CRUD-stöd för egenskaper för dataflödeskörning  i hanterad IR.</span><span class="sxs-lookup"><span data-stu-id="73fd4-898">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="73fd4-899">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="73fd4-899">Az.FrontDoor</span></span>
* <span data-ttu-id="73fd4-900">Nya cmdletar har lagts till för att skapa, uppdatera, hämta och ta bort (CRUD) Front Door-regelmotorobjekt</span><span class="sxs-lookup"><span data-stu-id="73fd4-900">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="73fd4-901">Hjälp-cmdletar har lagts till för konstruktion av Front Door-regelmotorobjekt</span><span class="sxs-lookup"><span data-stu-id="73fd4-901">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="73fd4-902">Regelmotorreferens har lagts till för Front Door-hanteringsregelobjekt.</span><span class="sxs-lookup"><span data-stu-id="73fd4-902">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="73fd4-903">Parametrar för Private Link har lagts till för Front Door-serverdelsobjekt</span><span class="sxs-lookup"><span data-stu-id="73fd4-903">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="73fd4-904">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="73fd4-904">Az.Functions</span></span>
* <span data-ttu-id="73fd4-905">Allmän tillgänglighet för ”Az.Functions”-modulen</span><span class="sxs-lookup"><span data-stu-id="73fd4-905">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="73fd4-906">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="73fd4-906">Az.HDInsight</span></span>
* <span data-ttu-id="73fd4-907">Stöd för diskkryptering med kundhanterad nyckel.</span><span class="sxs-lookup"><span data-stu-id="73fd4-907">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="73fd4-908">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="73fd4-908">Az.HealthcareApis</span></span>
* <span data-ttu-id="73fd4-909">Åtkomstprinciper använder inte längre det aktiva huvudkontot som standard</span><span class="sxs-lookup"><span data-stu-id="73fd4-909">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="73fd4-910">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="73fd4-910">Az.IotHub</span></span>
* <span data-ttu-id="73fd4-911">En cmdlet har lagts till som anropar en fråga i en IoT-hubb för att hämta information med ett SQL-liknande språk.</span><span class="sxs-lookup"><span data-stu-id="73fd4-911">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="73fd4-912">Problemet som gjorde att ”Add-AzIotHubDevice” inte skapade en Edge-aktiverad enhet utan underordnade enheter har åtgärdats [#11597]</span><span class="sxs-lookup"><span data-stu-id="73fd4-912">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="73fd4-913">En cmdlet har lagts till för att generera SAS-token för en Iot-hubb, enhet eller modul.</span><span class="sxs-lookup"><span data-stu-id="73fd4-913">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="73fd4-914">En cmdlet har lagts till för att anropa en måttfråga om konfiguration.</span><span class="sxs-lookup"><span data-stu-id="73fd4-914">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="73fd4-915">Hantera automatisk distribution av IoT Edge i stor skala.</span><span class="sxs-lookup"><span data-stu-id="73fd4-915">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="73fd4-916">Nya cmdlet:ar är:</span><span class="sxs-lookup"><span data-stu-id="73fd4-916">New cmdlets are:</span></span>
    - <span data-ttu-id="73fd4-917">”Add-AzIotHubDeployment”</span><span class="sxs-lookup"><span data-stu-id="73fd4-917">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="73fd4-918">”Get-AzIotHubDeployment”</span><span class="sxs-lookup"><span data-stu-id="73fd4-918">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="73fd4-919">”Remove-AzIotHubDeployment”</span><span class="sxs-lookup"><span data-stu-id="73fd4-919">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="73fd4-920">”Set-AzIotHubDeployment”</span><span class="sxs-lookup"><span data-stu-id="73fd4-920">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="73fd4-921">En cmdlet har lagts till för att anropa en måttfråga om IoT Edge-distribution.</span><span class="sxs-lookup"><span data-stu-id="73fd4-921">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="73fd4-922">En cmdlet har lagts till för att tillämpa konfigurationsinnehåll på den angivna gränsenheten.</span><span class="sxs-lookup"><span data-stu-id="73fd4-922">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="73fd4-923">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="73fd4-923">Az.KeyVault</span></span>
* <span data-ttu-id="73fd4-924">Två alias har tagits bort: ”New-AzKeyVaultCertificateAdministratorDetails” och ”New-AzKeyVaultCertificateOrganizationDetails”</span><span class="sxs-lookup"><span data-stu-id="73fd4-924">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="73fd4-925">Nu är mjuk borttagning aktiverat som standard när ett nyckelvalv skapas</span><span class="sxs-lookup"><span data-stu-id="73fd4-925">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="73fd4-926">Nätverksregler kan ställas in för att styra åtkomsten från särskilda nätverksplatser när du skapar ett nyckelvalv</span><span class="sxs-lookup"><span data-stu-id="73fd4-926">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="73fd4-927">Stöd för BYOK (Bring Your Own Key) har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-927">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="73fd4-928">”Add-AzKeyVaultKey” stöder generering av en KeyExchange-nyckel</span><span class="sxs-lookup"><span data-stu-id="73fd4-928">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="73fd4-929">”Get-AzKeyVaultKey” stöder nedladdning av en offentlig nyckel i PEM-format</span><span class="sxs-lookup"><span data-stu-id="73fd4-929">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="73fd4-930">”KeyOps”-delen av hjälpdokumentet för ”Add-AzKeyVaultKey” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="73fd4-930">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="73fd4-931">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="73fd4-931">Az.Monitor</span></span>
* <span data-ttu-id="73fd4-932">Bugg för ”Set-AzDiagnosticSettings” har åtgärdats; kvarhållningsprincipen tillämpas inte på alla kategorier [#11589]</span><span class="sxs-lookup"><span data-stu-id="73fd4-932">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="73fd4-933">Stöd för WebTest-tillgänglighetskriterier för måttavisering V2</span><span class="sxs-lookup"><span data-stu-id="73fd4-933">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="73fd4-934">”New-AzMetricAlertRuleV2Criteria”: ett alternativ för att skapa tillgänglighetskriterier för webbtest har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-934">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="73fd4-935">”Add-AzMetricAlertRuleV2”: stöd för de nya tillgänglighetskriterierna för webbtest</span><span class="sxs-lookup"><span data-stu-id="73fd4-935">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="73fd4-936">Redundant definition har tagits bort för RetentionPolicy i PSLogProfile [#7608]</span><span class="sxs-lookup"><span data-stu-id="73fd4-936">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="73fd4-937">Redundanta egenskaper som definierats i PSEventData har tagits bort [#11353]</span><span class="sxs-lookup"><span data-stu-id="73fd4-937">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="73fd4-938">”Get-AzLog” har bytt namn till ”Get-AzActivityLog”</span><span class="sxs-lookup"><span data-stu-id="73fd4-938">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73fd4-939">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73fd4-939">Az.Network</span></span>
* <span data-ttu-id="73fd4-940">Attribut för icke-bakåtkompatibel ändring har lagts till för att meddela att standardbeteendet för zoner kommer att ändras</span><span class="sxs-lookup"><span data-stu-id="73fd4-940">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="73fd4-941">”New-AzPublicIpAddress”</span><span class="sxs-lookup"><span data-stu-id="73fd4-941">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="73fd4-942">”New-AzPublicIpPrefix”</span><span class="sxs-lookup"><span data-stu-id="73fd4-942">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="73fd4-943">”New-AzLoadBalancerFrontendIpConfig”</span><span class="sxs-lookup"><span data-stu-id="73fd4-943">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="73fd4-944">Stöd har lagts till för en ny resurs på den översta nivån, SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="73fd4-944">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="73fd4-945">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="73fd4-945">New cmdlets added:</span></span>
        - <span data-ttu-id="73fd4-946">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="73fd4-946">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="73fd4-947">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="73fd4-947">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="73fd4-948">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="73fd4-948">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="73fd4-949">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="73fd4-949">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="73fd4-950">”RequiredZoneNames” har lagts till för ”PSPrivateLinkResource” och ”GroupId” för ”PSPrivateEndpointConnection”</span><span class="sxs-lookup"><span data-stu-id="73fd4-950">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="73fd4-951">Fel parametertyp för SuccessThresholdRoundTripTimeMs-parametern för New-AzNetworkWatcherConnectionMonitorTestConfigurationObject har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="73fd4-951">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="73fd4-952">VirtualWan-cmdletar har uppdaterats för att ange AllowVnetToVnetTraffic-argumentets standardvärde till True.</span><span class="sxs-lookup"><span data-stu-id="73fd4-952">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="73fd4-953">”New-AzVirtualWan”</span><span class="sxs-lookup"><span data-stu-id="73fd4-953">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="73fd4-954">”Update-AzVirtualWan”</span><span class="sxs-lookup"><span data-stu-id="73fd4-954">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="73fd4-955">Nya cmdletar har lagts till för att stödja DNS-zongrupp för privat slutpunkt</span><span class="sxs-lookup"><span data-stu-id="73fd4-955">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="73fd4-956">”New-AzPrivateDnsZoneConfig”</span><span class="sxs-lookup"><span data-stu-id="73fd4-956">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="73fd4-957">”Get-AzPrivateDnsZoneGroup”</span><span class="sxs-lookup"><span data-stu-id="73fd4-957">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="73fd4-958">”New-AzPrivateDnsZoneGroup”</span><span class="sxs-lookup"><span data-stu-id="73fd4-958">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="73fd4-959">”Set-AzPrivateDnsZoneGroup”</span><span class="sxs-lookup"><span data-stu-id="73fd4-959">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="73fd4-960">”Remove-AzPrivateDnsZoneGroup”</span><span class="sxs-lookup"><span data-stu-id="73fd4-960">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="73fd4-961">Parametrarna ”DNSEnableProxy”, ”DNSRequireProxyForNetworkRules” och ”DNSServers” har lagts till för ”AzureFirewall”</span><span class="sxs-lookup"><span data-stu-id="73fd4-961">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="73fd4-962">Parametrarna ”EnableDnsProxy”, ”DnsProxyNotRequiredForNetworkRule” och ”DnsServer” har lagts till för ”AzureFirewall”</span><span class="sxs-lookup"><span data-stu-id="73fd4-962">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="73fd4-963">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="73fd4-963">Updated cmdlet:</span></span>
        - <span data-ttu-id="73fd4-964">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="73fd4-964">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="73fd4-965">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="73fd4-965">Az.OperationalInsights</span></span>
* <span data-ttu-id="73fd4-966">Äldre kod har uppdaterats för att tillämpa ny genererad SDK</span><span class="sxs-lookup"><span data-stu-id="73fd4-966">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="73fd4-967">Cmdletar har tagits bort på grund av föråldrade API:er</span><span class="sxs-lookup"><span data-stu-id="73fd4-967">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="73fd4-968">”Get-AzOperationalInsightsSavedSearchResult” (alias ”Get-AzOperationalInsightsSavedSearchResults”)</span><span class="sxs-lookup"><span data-stu-id="73fd4-968">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="73fd4-969">”Get-AzOperationalInsightsSearchResult” (alias ”Get-AzOperationalInsightsSearchResults”)</span><span class="sxs-lookup"><span data-stu-id="73fd4-969">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="73fd4-970">”Get-AzOperationalInsightsLinkTarget” (alias ”Get-AzOperationalInsightsLinkTargets”)</span><span class="sxs-lookup"><span data-stu-id="73fd4-970">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="73fd4-971">Parametrar har lagts till för ”Set-AzOperationalInsightsWorkspace” och ”New-AzOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="73fd4-971">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="73fd4-972">Cmdletar har skapats för länkat lagringskonto</span><span class="sxs-lookup"><span data-stu-id="73fd4-972">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="73fd4-973">Cmdletar har skapats för kluster och länkad tjänst</span><span class="sxs-lookup"><span data-stu-id="73fd4-973">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="73fd4-974">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="73fd4-974">Az.RecoveryServices</span></span>
* <span data-ttu-id="73fd4-975">Azure Site Recovery: Stöd har lagts till för att skydda VM-närhetsplaceringsgrupper för Azure till Azure-provider.</span><span class="sxs-lookup"><span data-stu-id="73fd4-975">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="73fd4-976">Azure Site Recovery: Stöd har lagts till för replikering mellan zoner.</span><span class="sxs-lookup"><span data-stu-id="73fd4-976">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="73fd4-977">Azure Backup: Stöd har lagts till för långsiktig kvarhållning för Azure FileShare-återställningspunkter.</span><span class="sxs-lookup"><span data-stu-id="73fd4-977">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="73fd4-978">Azure Backup: Egenskaper för diskexkludering har lagts till för cmdlet-utdata från ”Get-AzRecoveryServicesBackupItem”.</span><span class="sxs-lookup"><span data-stu-id="73fd4-978">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="73fd4-979">En privat slutpunkt har lagts till för filen med valvets autentiseringsuppgifter för Site Recovery-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="73fd4-979">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="73fd4-980">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73fd4-980">Az.Resources</span></span>
* <span data-ttu-id="73fd4-981">En varning har lagts till om visningsfördröjning när en ny rolldefinition skapas</span><span class="sxs-lookup"><span data-stu-id="73fd4-981">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="73fd4-982">Princip-cmdletar har ändrats för utmatning av starkt typifierade objekt</span><span class="sxs-lookup"><span data-stu-id="73fd4-982">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="73fd4-983">Parametern ”-TenantLevel” har tagits bort för användning med ”Get-AzResourceLock” [#11335]</span><span class="sxs-lookup"><span data-stu-id="73fd4-983">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="73fd4-984">”Remove-AzResourceGroup -Id ResourceId” har åtgärdats [#9882]</span><span class="sxs-lookup"><span data-stu-id="73fd4-984">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="73fd4-985">En ny cmdlet har lagts till för att hämta What-If-resultat för ARM-mallar i omfånget för resursgrupper: ”Get-AzDeploymentResourceGroupWhatIfResult”</span><span class="sxs-lookup"><span data-stu-id="73fd4-985">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="73fd4-986">En ny cmdlet har lagts till för att hämta What-If-resultat för ARM-mallar i prenumerationsomfånget: ”Get-AzDeploymentWhatIfResult”</span><span class="sxs-lookup"><span data-stu-id="73fd4-986">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="73fd4-987">Alias: ”Get-AzSubscriptionDeploymentWhatIf”</span><span class="sxs-lookup"><span data-stu-id="73fd4-987">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="73fd4-988">Parametrarna ”-WhatIf” och ”-Confirm” har åsidosatts för ”New-AzDeployment” och ”New-AzResourceGroupDeployment” för att använda What-If-resultat för ARM-mallar</span><span class="sxs-lookup"><span data-stu-id="73fd4-988">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="73fd4-989">Ett utfasningsmeddelande har lagts till för parametern ”ApiVersion” i distributions-cmdletar</span><span class="sxs-lookup"><span data-stu-id="73fd4-989">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="73fd4-990">En funktion har lagts till för att visa förbättrade felmeddelanden för distributionsfel</span><span class="sxs-lookup"><span data-stu-id="73fd4-990">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="73fd4-991">CorrelationId-loggning har lagts till för distributionsfel</span><span class="sxs-lookup"><span data-stu-id="73fd4-991">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="73fd4-992">Egenskapen ”error” har lagts till i utdata från distributionsskript</span><span class="sxs-lookup"><span data-stu-id="73fd4-992">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="73fd4-993">Nuget Microsoft.Azure.Management.ResourceManager har uppdaterats till ”3.7.1-preview”</span><span class="sxs-lookup"><span data-stu-id="73fd4-993">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="73fd4-994">Specifika testfall har tagits bort då egenskapen Error i DeploymentValidateResult har ändrats till lässkyddad från nuget 3.7.1-preview</span><span class="sxs-lookup"><span data-stu-id="73fd4-994">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="73fd4-995">GenericResourceExpanded har flyttats från SDK ResourceManager 3.7.1-preview</span><span class="sxs-lookup"><span data-stu-id="73fd4-995">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="73fd4-996">Stöd för taggar har lagts till för alla Get-cmdletar för distribution, samt</span><span class="sxs-lookup"><span data-stu-id="73fd4-996">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="73fd4-997">”New-AzDeployment”</span><span class="sxs-lookup"><span data-stu-id="73fd4-997">'New-AzDeployment'</span></span>
    - <span data-ttu-id="73fd4-998">”New-AzManagementGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="73fd4-998">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="73fd4-999">”New-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="73fd4-999">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="73fd4-1000">”New-AzTenantDeployment”</span><span class="sxs-lookup"><span data-stu-id="73fd4-1000">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="73fd4-1001">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="73fd4-1001">Az.ServiceFabric</span></span>
* <span data-ttu-id="73fd4-1002">En bugg har åtgärdats som gjorde att --SecretIdentifier fick fel tumavtryck för certifikat när ett certifikat lades till</span><span class="sxs-lookup"><span data-stu-id="73fd4-1002">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="73fd4-1003">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73fd4-1003">Az.Sql</span></span>
* <span data-ttu-id="73fd4-1004">Förbättrade prestanda för:</span><span class="sxs-lookup"><span data-stu-id="73fd4-1004">Enhance performance of:</span></span>
    - <span data-ttu-id="73fd4-1005">”Set-AzSqlDatabaseSensitivityClassification”</span><span class="sxs-lookup"><span data-stu-id="73fd4-1005">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="73fd4-1006">”Set-AzSqlInstanceDatabaseSensitivityClassification”</span><span class="sxs-lookup"><span data-stu-id="73fd4-1006">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="73fd4-1007">”Remove-AzSqlDatabaseSensitivityClassification”</span><span class="sxs-lookup"><span data-stu-id="73fd4-1007">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="73fd4-1008">”Remove-AzSqlInstanceDatabaseSensitivityClassification”</span><span class="sxs-lookup"><span data-stu-id="73fd4-1008">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="73fd4-1009">”Enable-AzSqlDatabaseSensitivityRecommendation”</span><span class="sxs-lookup"><span data-stu-id="73fd4-1009">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="73fd4-1010">”Enable-AzSqlInstanceDatabaseSensitivityRecommendation”</span><span class="sxs-lookup"><span data-stu-id="73fd4-1010">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="73fd4-1011">”Disable-AzSqlDatabaseSensitivityRecommendation”</span><span class="sxs-lookup"><span data-stu-id="73fd4-1011">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="73fd4-1012">”Disable-AzSqlInstanceDatabaseSensitivityRecommendation”</span><span class="sxs-lookup"><span data-stu-id="73fd4-1012">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="73fd4-1013">Validering på klientsidan har tagits bort för parametern ”RetentionDays” från cmdleten ”Set-AzSqlDatabaseBackupShortTermRetentionPolicy”</span><span class="sxs-lookup"><span data-stu-id="73fd4-1013">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="73fd4-1014">Granskning av ett lagringskonto i Vnet; en bugg har åtgärdats som orsakade fel när en Storage Blob Data-deltagarroll skapades.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1014">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="73fd4-1015">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="73fd4-1015">Az.Storage</span></span>
* <span data-ttu-id="73fd4-1016">”-AsJob” har lagts till för att hämta/lista konto med cmdleten ”Get-AzStorageAccount”</span><span class="sxs-lookup"><span data-stu-id="73fd4-1016">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="73fd4-1017">Gör KeyVersion valfri när lagringskontot uppdateras med KeyvaultEncryption, för att ge stöd för automatisk nyckelrotation</span><span class="sxs-lookup"><span data-stu-id="73fd4-1017">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="73fd4-1018">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="73fd4-1018">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="73fd4-1019">Problemet med borttagning av Azure-filkatalog i pipeline har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="73fd4-1019">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="73fd4-1020">”Remove-AzStorageDirectory”</span><span class="sxs-lookup"><span data-stu-id="73fd4-1020">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="73fd4-1021">Åtgärdat [#9880]: Definitionen av DefaultAction-värdet för NetWorkRule har ändrats för konsekvens med Swagger.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1021">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="73fd4-1022">”Update-AzStorageAccountNetworkRuleSet”</span><span class="sxs-lookup"><span data-stu-id="73fd4-1022">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="73fd4-1023">”Get-AzStorageAccountNetworkRuleSet”</span><span class="sxs-lookup"><span data-stu-id="73fd4-1023">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="73fd4-1024">Åtgärdat [#11624]: Hoppa över dubblettregler när NetworkRules läggs till, för att undvika serverfel</span><span class="sxs-lookup"><span data-stu-id="73fd4-1024">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="73fd4-1025">”Add-AzStorageAccountNetworkRule”</span><span class="sxs-lookup"><span data-stu-id="73fd4-1025">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="73fd4-1026">Microsoft.Azure.Cosmos.Table SDK har uppgraderats till 1.0.7</span><span class="sxs-lookup"><span data-stu-id="73fd4-1026">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="73fd4-1027">Ett varningsmeddelande har lagts till för att påminna användaren om att lista igen med ContinuationToken när endast delobjekt returneras i listan med DataLake Gen2-objekt,</span><span class="sxs-lookup"><span data-stu-id="73fd4-1027">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="73fd4-1028">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="73fd4-1028">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="73fd4-1029">Stöd för att skapa eller uppdatera lagringskonto med Azure Files Active Directory Domain Service-autentisering</span><span class="sxs-lookup"><span data-stu-id="73fd4-1029">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="73fd4-1030">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="73fd4-1030">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="73fd4-1031">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="73fd4-1031">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="73fd4-1032">Stöd för nya eller listade Kerberos-nycklar för lagringskontot</span><span class="sxs-lookup"><span data-stu-id="73fd4-1032">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="73fd4-1033">”New-AzStorageAccountKey”</span><span class="sxs-lookup"><span data-stu-id="73fd4-1033">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="73fd4-1034">”Get-AzStorageAccountKey”</span><span class="sxs-lookup"><span data-stu-id="73fd4-1034">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="73fd4-1035">Stöd för redundans med lagringskonto</span><span class="sxs-lookup"><span data-stu-id="73fd4-1035">Supported failover Storage account</span></span>
    - <span data-ttu-id="73fd4-1036">”Invoke-AzStorageAccountFailover”</span><span class="sxs-lookup"><span data-stu-id="73fd4-1036">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="73fd4-1037">Hjälpen för ”Get-AzStorageBlobCopyState” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="73fd4-1037">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="73fd4-1038">Hjälpen för ”Get-AzStorageFileCopyState” och ”Start-AzStorageBlobCopy” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="73fd4-1038">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="73fd4-1039">Lagringsklientbibliotek v12 har integrerats med Queue- och File-cmdletar</span><span class="sxs-lookup"><span data-stu-id="73fd4-1039">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="73fd4-1040">Utdatatypen har ändrats från CloudFile till AzureStorageFile; ursprungliga utdata blir en underordnad egenskap i den nya utmatningen</span><span class="sxs-lookup"><span data-stu-id="73fd4-1040">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="73fd4-1041">”Get-AzStorageFile”</span><span class="sxs-lookup"><span data-stu-id="73fd4-1041">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="73fd4-1042">”Remove-AzStorageFile”</span><span class="sxs-lookup"><span data-stu-id="73fd4-1042">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="73fd4-1043">”Get-AzStorageFileContent”</span><span class="sxs-lookup"><span data-stu-id="73fd4-1043">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="73fd4-1044">”Set-AzStorageFileContent”</span><span class="sxs-lookup"><span data-stu-id="73fd4-1044">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="73fd4-1045">”Start-AzStorageFileCopy”</span><span class="sxs-lookup"><span data-stu-id="73fd4-1045">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="73fd4-1046">Utdatatypen har ändrats från CloudFileDirectory till AzureStorageFileDirectory; ursprungliga utdata blir en underordnad egenskap i den nya utmatningen</span><span class="sxs-lookup"><span data-stu-id="73fd4-1046">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="73fd4-1047">”New-AzStorageDirectory”</span><span class="sxs-lookup"><span data-stu-id="73fd4-1047">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="73fd4-1048">”Remove-AzStorageDirectory”</span><span class="sxs-lookup"><span data-stu-id="73fd4-1048">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="73fd4-1049">Utdatatypen har ändrats från CloudFileShare till AzureStorageFileShare; ursprungliga utdata blir en underordnad egenskap i den nya utmatningen</span><span class="sxs-lookup"><span data-stu-id="73fd4-1049">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="73fd4-1050">”Get-AzStorageShare”</span><span class="sxs-lookup"><span data-stu-id="73fd4-1050">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="73fd4-1051">”New-AzStorageShare”</span><span class="sxs-lookup"><span data-stu-id="73fd4-1051">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="73fd4-1052">”Remove-AzStorageShare”</span><span class="sxs-lookup"><span data-stu-id="73fd4-1052">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="73fd4-1053">Utdatatypen har ändrats från FileShareProperties till AzureStorageFileShare; ursprungliga utdata blir en underordnad egenskap i den nya utmatningen</span><span class="sxs-lookup"><span data-stu-id="73fd4-1053">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="73fd4-1054">”Set-AzStorageShareQuota”</span><span class="sxs-lookup"><span data-stu-id="73fd4-1054">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="73fd4-1055">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="73fd4-1055">Az.TrafficManager</span></span>
* <span data-ttu-id="73fd4-1056">Felaktigt profilnamn har åtgärdats i utförliga utdata för ”DisableAzureTrafficManagerEndpoint”</span><span class="sxs-lookup"><span data-stu-id="73fd4-1056">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="73fd4-1057">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="73fd4-1057">Az.Websites</span></span>
* <span data-ttu-id="73fd4-1058">Stavfel har åtgärdats i hjälpen för ”Update-AzWebAppAccessRestrictionConfig”.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1058">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="73fd4-1059">3.8.0 – April 2020</span><span class="sxs-lookup"><span data-stu-id="73fd4-1059">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="73fd4-1060">Höjdpunkter sedan den senaste uppdateringen</span><span class="sxs-lookup"><span data-stu-id="73fd4-1060">Highlights since the last release</span></span>
* <span data-ttu-id="73fd4-1061">PowerShell-versioner som Az.Storage stöder: Windows PowerShell 5.1, PowerShell Core 6.2.4+ och PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="73fd4-1061">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="73fd4-1062">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73fd4-1062">Az.Accounts</span></span>
* <span data-ttu-id="73fd4-1063">Uppdaterade URL:en för Azure PowerShell-enkäten i ”Resolve-AzError” [#11507]</span><span class="sxs-lookup"><span data-stu-id="73fd4-1063">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="73fd4-1064">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="73fd4-1064">Az.ApiManagement</span></span>
* <span data-ttu-id="73fd4-1065">Lade till meddelande om icke-bakåtkompatibel ändring vid ändring i utdata för Azure File-cmdletar i en framtida version</span><span class="sxs-lookup"><span data-stu-id="73fd4-1065">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="73fd4-1066">"Set-AzApiManagementGroup" Uppdaterad dokumentation för att ange GroupId-parametern</span><span class="sxs-lookup"><span data-stu-id="73fd4-1066">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="73fd4-1067">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="73fd4-1067">Az.Cdn</span></span>
* <span data-ttu-id="73fd4-1068">Fast ChinaCDN-relaterad prissättning för SKU-visning</span><span class="sxs-lookup"><span data-stu-id="73fd4-1068">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="73fd4-1069">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="73fd4-1069">Az.CognitiveServices</span></span>
* <span data-ttu-id="73fd4-1070">Identitet som stöds, kryptering, UserOwnedStorage</span><span class="sxs-lookup"><span data-stu-id="73fd4-1070">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73fd4-1071">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73fd4-1071">Az.Compute</span></span>
* <span data-ttu-id="73fd4-1072">Cmdleten ”Set-AzVmssOrchestrationServiceState” har lagts till.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1072">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="73fd4-1073">”Get-AzVmss” med -InstanceView visar OrchestrationService-tillstånd.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1073">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="73fd4-1074">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="73fd4-1074">Az.IotHub</span></span>
* <span data-ttu-id="73fd4-1075">Hantera den dubbla konfigurationen för IoT-enheter, nya cmdletar är:</span><span class="sxs-lookup"><span data-stu-id="73fd4-1075">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="73fd4-1076">'Get-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="73fd4-1076">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="73fd4-1077">'Update-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="73fd4-1077">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="73fd4-1078">En cmdlet har lagts till för att anropa direkt metod på en enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1078">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="73fd4-1079">Hantera dubbel konfiguration för IoT-enhetsmodul, nya cmdletar är:</span><span class="sxs-lookup"><span data-stu-id="73fd4-1079">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="73fd4-1080">'Get-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="73fd4-1080">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="73fd4-1081">'Update-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="73fd4-1081">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="73fd4-1082">Hantera IoT-automatisk konfiguration av enhetshantering i stor skala.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1082">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="73fd4-1083">Nya cmdlet:ar är:</span><span class="sxs-lookup"><span data-stu-id="73fd4-1083">New cmdlets are:</span></span>
    - <span data-ttu-id="73fd4-1084">'Add-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="73fd4-1084">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="73fd4-1085">'Get-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="73fd4-1085">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="73fd4-1086">'Remove-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="73fd4-1086">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="73fd4-1087">'Set-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="73fd4-1087">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="73fd4-1088">En cmdlet har lagts till för att anropa en edge-modulmetod i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1088">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="73fd4-1089">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="73fd4-1089">Az.KeyVault</span></span>
* <span data-ttu-id="73fd4-1090">Har lagt till en ny cmdlet, "Update-AzKeyVault", som kan aktivera mjuk borttagning och rensning av skydd i ett valv</span><span class="sxs-lookup"><span data-stu-id="73fd4-1090">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="73fd4-1091">Har lagt till stöd i Microsoft.PowerShell.SecretManagement [#11178]</span><span class="sxs-lookup"><span data-stu-id="73fd4-1091">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="73fd4-1092">Åtgärdat fel i exemplen i 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span><span class="sxs-lookup"><span data-stu-id="73fd4-1092">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="73fd4-1093">Har lagt till stöd för privat slutpunkt</span><span class="sxs-lookup"><span data-stu-id="73fd4-1093">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="73fd4-1094">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="73fd4-1094">Az.Maintenance</span></span>
* <span data-ttu-id="73fd4-1095">Publicerar slutversion av underhålls-cmdletar för GA</span><span class="sxs-lookup"><span data-stu-id="73fd4-1095">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="73fd4-1096">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="73fd4-1096">Az.Monitor</span></span>
* <span data-ttu-id="73fd4-1097">Har lagt till cmdletar för privat länkomfång</span><span class="sxs-lookup"><span data-stu-id="73fd4-1097">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="73fd4-1098">'Get-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="73fd4-1098">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="73fd4-1099">'Remove-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="73fd4-1099">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="73fd4-1100">'New-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="73fd4-1100">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="73fd4-1101">'Update-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="73fd4-1101">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="73fd4-1102">'Get-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="73fd4-1102">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="73fd4-1103">'New-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="73fd4-1103">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="73fd4-1104">'Remove-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="73fd4-1104">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73fd4-1105">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73fd4-1105">Az.Network</span></span>
* <span data-ttu-id="73fd4-1106">Uppdaterade cmdletar för att aktivera anslutning på privat IP för Virtual Network Gateway.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1106">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="73fd4-1107">'New-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="73fd4-1107">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="73fd4-1108">'Set-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="73fd4-1108">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="73fd4-1109">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="73fd4-1109">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="73fd4-1110">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="73fd4-1110">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="73fd4-1111">Uppdaterade cmdletar för att aktivera FQDN-baserade LocalNetworkGateways och VpnSites</span><span class="sxs-lookup"><span data-stu-id="73fd4-1111">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="73fd4-1112">'New-AzLocalNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="73fd4-1112">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="73fd4-1113">'New-AzVpnSiteLink'</span><span class="sxs-lookup"><span data-stu-id="73fd4-1113">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="73fd4-1114">Stöd har lagts till för IPv6-adresstypen i ExpressRouteCircuitConnectionConfig (Global Reach)</span><span class="sxs-lookup"><span data-stu-id="73fd4-1114">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="73fd4-1115">Lade till 'Set-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="73fd4-1115">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="73fd4-1116">tillåter inställning av alla befintliga egenskaper inklusive IPv6CircuitConnectionProperties</span><span class="sxs-lookup"><span data-stu-id="73fd4-1116">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="73fd4-1117">Uppdaterade 'Add-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="73fd4-1117">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="73fd4-1118">Lade till en ytterligare valfri parameter, AddressPrefixType, för att specificera adresstypen för adressprefix</span><span class="sxs-lookup"><span data-stu-id="73fd4-1118">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="73fd4-1119">Uppdaterade cmdletar för att aktivera inställningen för DPD-timeout på Virtual Network Gateway-anslutningar.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1119">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="73fd4-1120">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="73fd4-1120">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="73fd4-1121">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="73fd4-1121">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="73fd4-1122">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="73fd4-1122">Az.PolicyInsights</span></span>
* <span data-ttu-id="73fd4-1123">Cmdleten "Start-AzPolicyComplianceScan" har lagts till för att utlösa genomsökningar av principefterlevnad</span><span class="sxs-lookup"><span data-stu-id="73fd4-1123">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="73fd4-1124">Principdefinition, uppsättningsdefinition och tilldelningsversioner har lagts till i "Get-AzPolicyState"-utdata</span><span class="sxs-lookup"><span data-stu-id="73fd4-1124">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="73fd4-1125">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="73fd4-1125">Az.ServiceFabric</span></span>
* <span data-ttu-id="73fd4-1126">Förbättrad kodformatering och användbarhet för "New-AzServiceFabricCluster"-exempel</span><span class="sxs-lookup"><span data-stu-id="73fd4-1126">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="73fd4-1127">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73fd4-1127">Az.Sql</span></span>
* <span data-ttu-id="73fd4-1128">Lade till cmdletarna "Get-AzSqlInstanceOperation" och "Stop-AzSqlInstanceOperation"</span><span class="sxs-lookup"><span data-stu-id="73fd4-1128">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="73fd4-1129">Stöd för granskning för ett lagringskonto i VNet.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1129">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="73fd4-1130">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="73fd4-1130">Az.Storage</span></span>
* <span data-ttu-id="73fd4-1131">Lade till meddelande om icke-bakåtkompatibel ändring vid ändring i utdata för Azure File-cmdletar i en framtida version</span><span class="sxs-lookup"><span data-stu-id="73fd4-1131">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="73fd4-1132">Stöd för nya SkuName StandardGZRS, StandardRAGZRS när ett lagringskonto skapas/uppdateras</span><span class="sxs-lookup"><span data-stu-id="73fd4-1132">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="73fd4-1133">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="73fd4-1133">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="73fd4-1134">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="73fd4-1134">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="73fd4-1135">Stöd för DataLake Gen2</span><span class="sxs-lookup"><span data-stu-id="73fd4-1135">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="73fd4-1136">'New-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="73fd4-1136">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="73fd4-1137">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="73fd4-1137">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="73fd4-1138">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="73fd4-1138">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="73fd4-1139">'Move-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="73fd4-1139">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="73fd4-1140">'Set-AzDataLakeGen2ItemAclObject'</span><span class="sxs-lookup"><span data-stu-id="73fd4-1140">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="73fd4-1141">'Update-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="73fd4-1141">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="73fd4-1142">'Get-AzDataLakeGen2ItemContent'</span><span class="sxs-lookup"><span data-stu-id="73fd4-1142">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="73fd4-1143">'Remove-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="73fd4-1143">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="73fd4-1144">0.10.0-förhandsversion – April 2020</span><span class="sxs-lookup"><span data-stu-id="73fd4-1144">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="73fd4-1145">Allmänt</span><span class="sxs-lookup"><span data-stu-id="73fd4-1145">General</span></span>
* <span data-ttu-id="73fd4-1146">Az-moduler är nu tillgängliga i förhandsversion på Azure Stack Hub.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1146">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="73fd4-1147">Därmed möjliggörs kompatibilitet för flera plattformar med Linux och macOs.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1147">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="73fd4-1148">Azure Stack Hub stöder nu PowerShell Core med AZ-moduler. Mer information finns [här](/azure-stack/operator/powershell-install-az-module)</span><span class="sxs-lookup"><span data-stu-id="73fd4-1148">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](/azure-stack/operator/powershell-install-az-module)</span></span>
* <span data-ttu-id="73fd4-1149">Supportprofil för AZ-moduler 2019-03-01-hybrid:</span><span class="sxs-lookup"><span data-stu-id="73fd4-1149">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="73fd4-1150">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="73fd4-1150">Az.Billing</span></span>
  - <span data-ttu-id="73fd4-1151">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73fd4-1151">Az.Compute</span></span>
  - <span data-ttu-id="73fd4-1152">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="73fd4-1152">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="73fd4-1153">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="73fd4-1153">Az.EventHub</span></span>
  - <span data-ttu-id="73fd4-1154">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="73fd4-1154">Az.IotHub</span></span>
  - <span data-ttu-id="73fd4-1155">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="73fd4-1155">Az.KeyVault</span></span>
  - <span data-ttu-id="73fd4-1156">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="73fd4-1156">Az.Monitor</span></span>
  - <span data-ttu-id="73fd4-1157">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73fd4-1157">Az.Network</span></span>
  - <span data-ttu-id="73fd4-1158">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73fd4-1158">Az.Resources</span></span>
  - <span data-ttu-id="73fd4-1159">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="73fd4-1159">Az.Storage</span></span>
  - <span data-ttu-id="73fd4-1160">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="73fd4-1160">Az.Websites</span></span>
* <span data-ttu-id="73fd4-1161">Tre nya PowerShell-moduler för AZ har introducerats som fungerar med Azure Stack Hub, och de är Az.Databox, Az.IotHub och Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="73fd4-1161">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="73fd4-1162">Kommandona är i princip oförändrade, med endast mindre ändringar som att AzureRM ändras till AZ</span><span class="sxs-lookup"><span data-stu-id="73fd4-1162">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="73fd4-1163">En uppdaterad länk till PowerShell-dokumentationen för Azure Stack Hub finns [här](/azure-stack/operator/powershell-install-az-module)</span><span class="sxs-lookup"><span data-stu-id="73fd4-1163">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](/azure-stack/operator/powershell-install-az-module)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="73fd4-1164">3.7.0 – mars 2020</span><span class="sxs-lookup"><span data-stu-id="73fd4-1164">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="73fd4-1165">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73fd4-1165">Az.Accounts</span></span>
* <span data-ttu-id="73fd4-1166">Åtgärdade ”Get-AzTenant”/”Get-AzDefault”/”Set-AzDefault”-utlösning av NullReferenceException när du inte är inloggad [#10292]</span><span class="sxs-lookup"><span data-stu-id="73fd4-1166">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73fd4-1167">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73fd4-1167">Az.Compute</span></span>
* <span data-ttu-id="73fd4-1168">Följande parametrar har lagts till i cmdleten ”New-AzDiskConfig”:</span><span class="sxs-lookup"><span data-stu-id="73fd4-1168">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="73fd4-1169">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="73fd4-1169">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="73fd4-1170">Tillåten krypteringsegenskap till målparametern för cmdleten ”New-AzGalleryImageVersion”.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1170">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="73fd4-1171">Åtgärdade tempDisk-problem för cmdletarna ”Set-AzVmss”-Reimage och ”Invoke-AzVMReimage”.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1171">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="73fd4-1172">[#11354]</span><span class="sxs-lookup"><span data-stu-id="73fd4-1172">[#11354]</span></span>
* <span data-ttu-id="73fd4-1173">Stöd har lagts till i nedanstående cmdletar för nytt SAP-tillägg</span><span class="sxs-lookup"><span data-stu-id="73fd4-1173">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="73fd4-1174">”Set-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="73fd4-1174">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="73fd4-1175">”Get-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="73fd4-1175">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="73fd4-1176">”Remove-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="73fd4-1176">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="73fd4-1177">”Update-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="73fd4-1177">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="73fd4-1178">Åtgärdade fel i exempel på hjälpdokument</span><span class="sxs-lookup"><span data-stu-id="73fd4-1178">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="73fd4-1179">Visade det exakta strängvärdet för VM PowerState i tabellformat.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1179">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="73fd4-1180">”New-AzVmssConfig”: den fasta serialiseringen av egenskapen AutomaticRepairs när SinglePlacementGroup är inaktiverad.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1180">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="73fd4-1181">[#11257]</span><span class="sxs-lookup"><span data-stu-id="73fd4-1181">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="73fd4-1182">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="73fd4-1182">Az.DataFactory</span></span>
* <span data-ttu-id="73fd4-1183">ADF .Net SDK har uppdaterats till 4.8.0</span><span class="sxs-lookup"><span data-stu-id="73fd4-1183">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="73fd4-1184">Valfria parametrar har lagts till i kommandot ”Invoke-AzDataFactoryV2Pipeline” för att stödja omkörning</span><span class="sxs-lookup"><span data-stu-id="73fd4-1184">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="73fd4-1185">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="73fd4-1185">Az.DataLakeStore</span></span>
* <span data-ttu-id="73fd4-1186">Lade till beskrivning för icke-bakåtkompatibel ändring för ”Export-AzDataLakeStoreItem” och ”Import-AzDataLakeStoreItem”</span><span class="sxs-lookup"><span data-stu-id="73fd4-1186">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="73fd4-1187">Lade till alternativ för bytekodning för ”New-AzDataLakeStoreItem”, ”Add-AzDAtaLakeStoreItemContent” och ”Get-AzDAtaLakeStoreItemContent”</span><span class="sxs-lookup"><span data-stu-id="73fd4-1187">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="73fd4-1188">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="73fd4-1188">Az.HDInsight</span></span>
* <span data-ttu-id="73fd4-1189">Stöd för att ange en minimal TLS-version som stöds när klustret skapas.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1189">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="73fd4-1190">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="73fd4-1190">Az.IotHub</span></span>
* <span data-ttu-id="73fd4-1191">Stöd har lagts till för att hantera distribuerade inställningar per enhet.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1191">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="73fd4-1192">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="73fd4-1192">New Cmdlets are:</span></span>
    - <span data-ttu-id="73fd4-1193">”Get-AzIotHubDistributedTracing”</span><span class="sxs-lookup"><span data-stu-id="73fd4-1193">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="73fd4-1194">”Set-AzIotHubDistributedTracing”</span><span class="sxs-lookup"><span data-stu-id="73fd4-1194">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="73fd4-1195">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="73fd4-1195">Az.KeyVault</span></span>
* <span data-ttu-id="73fd4-1196">Ändrade attribut för icke-bakåtkompatibel ändring lades till för ”New-AzKeyVault”</span><span class="sxs-lookup"><span data-stu-id="73fd4-1196">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="73fd4-1197">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="73fd4-1197">Az.Monitor</span></span>
* <span data-ttu-id="73fd4-1198">Uppdaterad dokumentation för ”New-AzScheduledQueryRuleLogMetricTrigger”</span><span class="sxs-lookup"><span data-stu-id="73fd4-1198">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73fd4-1199">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73fd4-1199">Az.Network</span></span>
* <span data-ttu-id="73fd4-1200">Uppdaterade cmdletar för att tillåta VirtualHubVnetConnections mellan klienter</span><span class="sxs-lookup"><span data-stu-id="73fd4-1200">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="73fd4-1201">”New-AzVirtualHubVnetConnection”</span><span class="sxs-lookup"><span data-stu-id="73fd4-1201">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="73fd4-1202">”Update-AzVirtualHubVnetConnection”</span><span class="sxs-lookup"><span data-stu-id="73fd4-1202">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="73fd4-1203">”New-AzVirtualHub”</span><span class="sxs-lookup"><span data-stu-id="73fd4-1203">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="73fd4-1204">”Update-AzVirtualHub”</span><span class="sxs-lookup"><span data-stu-id="73fd4-1204">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="73fd4-1205">SQL Management SDK-beroende har tagits bort</span><span class="sxs-lookup"><span data-stu-id="73fd4-1205">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="73fd4-1206">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="73fd4-1206">Az.PolicyInsights</span></span>
* <span data-ttu-id="73fd4-1207">Förbättrade felmeddelanden</span><span class="sxs-lookup"><span data-stu-id="73fd4-1207">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="73fd4-1208">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="73fd4-1208">Az.RecoveryServices</span></span>
* <span data-ttu-id="73fd4-1209">Azure Site Recovery har lagt till stöd för återaktivering av skydd och uppdaterade VM-egenskaper för virtuella Azure-datorer med krypterad disk.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1209">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="73fd4-1210">Lade till Azure Site Recovery VmwareToAzure-egenskaper för DR-övervakning</span><span class="sxs-lookup"><span data-stu-id="73fd4-1210">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="73fd4-1211">Azure Backup har lagt till stöd för att försöka uppdatera principuppdateringen för misslyckade objekt på nytt.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1211">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="73fd4-1212">Azure Backup lagt till stöd för diskundantagsinställningar under säkerhetskopiering och återställning.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1212">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="73fd4-1213">Azure Backup lagt till stöd för att återställa flera filer/mappar i AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="73fd4-1213">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="73fd4-1214">Azure Backup lade till support för användardefinierad Resourcegroup-support vid uppdatering av IaasVM-princip</span><span class="sxs-lookup"><span data-stu-id="73fd4-1214">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="73fd4-1215">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73fd4-1215">Az.Resources</span></span>
* <span data-ttu-id="73fd4-1216">Åtgärdade ”Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType” så att den använder den faktisk apiVersion av resurser i stället för standard-apiVersion [#11267]</span><span class="sxs-lookup"><span data-stu-id="73fd4-1216">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="73fd4-1217">Lade till correlationId-loggning för felscenarier</span><span class="sxs-lookup"><span data-stu-id="73fd4-1217">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="73fd4-1218">Liten dokumentationsändring för ”Get-AzResourceLock”.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1218">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="73fd4-1219">Lade till exempel.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1219">Added example.</span></span>
* <span data-ttu-id="73fd4-1220">Undantaget enkelt citattecken i parametervärde för ”Get-AzADUser” [#11317]</span><span class="sxs-lookup"><span data-stu-id="73fd4-1220">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="73fd4-1221">Nya cmdletar har lagts till för distributionsskript (”Get-AzDeploymentScript”, ”Get-AzDeploymentScriptLog”, ”Save-AzDeploymentScriptLog”, ”Remove-AzDeploymentScript”)</span><span class="sxs-lookup"><span data-stu-id="73fd4-1221">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="73fd4-1222">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73fd4-1222">Az.Sql</span></span>
* <span data-ttu-id="73fd4-1223">En läsbar sekundär parameter har lagts till i Invoke-AzSqlDatabaseFailover</span><span class="sxs-lookup"><span data-stu-id="73fd4-1223">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="73fd4-1224">Cmdleten Disable-AzSqlServerActiveDirectoryOnlyAuthentication har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-1224">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="73fd4-1225">Den sparade känslighet rangordningen när kolumner klassificeras i databasen.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1225">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="73fd4-1226">Az.Support</span><span class="sxs-lookup"><span data-stu-id="73fd4-1226">Az.Support</span></span>
* <span data-ttu-id="73fd4-1227">Allmän tillgänglighet för ”Az.Support”-modulen</span><span class="sxs-lookup"><span data-stu-id="73fd4-1227">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="73fd4-1228">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="73fd4-1228">Az.Websites</span></span>
* <span data-ttu-id="73fd4-1229">Stöd har lagts till för att arbeta med trafikdirigeringsregler för webbappar under nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="73fd4-1229">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="73fd4-1230">”Get-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="73fd4-1230">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="73fd4-1231">”Update-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="73fd4-1231">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="73fd4-1232">”Add-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="73fd4-1232">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="73fd4-1233">”Remove-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="73fd4-1233">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="73fd4-1234">3.6.1 – mars 2020</span><span class="sxs-lookup"><span data-stu-id="73fd4-1234">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="73fd4-1235">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73fd4-1235">Az.Accounts</span></span>
* <span data-ttu-id="73fd4-1236">Öppna sidan med Azure PowerShell-enkäten i ”Send-Feedback” [#11020]</span><span class="sxs-lookup"><span data-stu-id="73fd4-1236">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="73fd4-1237">Visa URL:en för Azure PowerShell-enkäten i ”Resolve-Error” [#11021]</span><span class="sxs-lookup"><span data-stu-id="73fd4-1237">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="73fd4-1238">Az-version har lagts till i UserAgent</span><span class="sxs-lookup"><span data-stu-id="73fd4-1238">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="73fd4-1239">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="73fd4-1239">Az.ApiManagement</span></span>
* <span data-ttu-id="73fd4-1240">Stöd har lagts till för att hämta och konfigurera en anpassad domän på DeveloperPortal-slutpunkten [#11007]</span><span class="sxs-lookup"><span data-stu-id="73fd4-1240">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="73fd4-1241">”Export-AzApiManagementApi” Stöd har lagts till för att ladda ned API-definition i Json-format [#9987]</span><span class="sxs-lookup"><span data-stu-id="73fd4-1241">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="73fd4-1242">”Import-AzApiManagementApi” Stöd har lagts till för att importera OpenApi 3.0-definition från Json-dokument</span><span class="sxs-lookup"><span data-stu-id="73fd4-1242">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="73fd4-1243">”New-AzApiManagementIdentityProvider” och ”Set-AzApiManagementIdentityProvider” Stöd har lagts till för att konfigurera ”Signin Tenant” för AAD B2C-provider [#9784]</span><span class="sxs-lookup"><span data-stu-id="73fd4-1243">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="73fd4-1244">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="73fd4-1244">Az.DataLakeStore</span></span>
* <span data-ttu-id="73fd4-1245">En referens har uttryckligen lagts till för System.Buffers i csproj och psd1.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1245">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="73fd4-1246">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="73fd4-1246">Az.IotHub</span></span>
* <span data-ttu-id="73fd4-1247">Lade till stöd för att hantera enheter i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1247">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="73fd4-1248">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="73fd4-1248">New Cmdlets are:</span></span>
    - <span data-ttu-id="73fd4-1249">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="73fd4-1249">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="73fd4-1250">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="73fd4-1250">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="73fd4-1251">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="73fd4-1251">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="73fd4-1252">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="73fd4-1252">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="73fd4-1253">Stöd har lagts till för att hantera moduler på en mål-IoT-enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1253">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="73fd4-1254">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="73fd4-1254">New Cmdlets are:</span></span>
    - <span data-ttu-id="73fd4-1255">”Add-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="73fd4-1255">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="73fd4-1256">”Get-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="73fd4-1256">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="73fd4-1257">”Remove-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="73fd4-1257">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="73fd4-1258">”Set-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="73fd4-1258">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="73fd4-1259">Cmdlet har lagts till för att hämta anslutningssträngen för en mål-IoT-enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1259">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="73fd4-1260">Cmdlet har lagts till för att hämta anslutningssträngen för en modul på en mål-IoT-enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1260">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="73fd4-1261">Stöd har lagts till för att hämta/ange en överordnad enhet för en IoT-enhet.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1261">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="73fd4-1262">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="73fd4-1262">New Cmdlets are:</span></span>
    - <span data-ttu-id="73fd4-1263">”Get-AzIotHubDeviceParent”</span><span class="sxs-lookup"><span data-stu-id="73fd4-1263">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="73fd4-1264">”Set-AzIotHubDeviceParent”</span><span class="sxs-lookup"><span data-stu-id="73fd4-1264">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="73fd4-1265">Stöd har lagts till för att hantera en enhets överordnade och underordnade relationer.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1265">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="73fd4-1266">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="73fd4-1266">Az.Monitor</span></span>
* <span data-ttu-id="73fd4-1267">Utdatavärdet har åtgärdats för ”Get-AzMetricDefinition” [#9714]</span><span class="sxs-lookup"><span data-stu-id="73fd4-1267">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73fd4-1268">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73fd4-1268">Az.Network</span></span>
* <span data-ttu-id="73fd4-1269">SQL Management SDK har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1269">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="73fd4-1270">Ett problem har åtgärdats med namngivningsskillnader i klassen PrivateLinkServiceConnectionState.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1270">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="73fd4-1271">Fältet ActionsRequired mappar till ActionRequired.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1271">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="73fd4-1272">PublicNetworkAccess har lagts till i ”New-AzSqlServer” och ”Set-AzSqlServer”</span><span class="sxs-lookup"><span data-stu-id="73fd4-1272">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="73fd4-1273">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73fd4-1273">Az.Resources</span></span>
* <span data-ttu-id="73fd4-1274">Null-referensfel har åtgärdats i ”Get-AzRoleAssignment”</span><span class="sxs-lookup"><span data-stu-id="73fd4-1274">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="73fd4-1275">Växlarna ”-Force” och ”-PassThru” är valfria i ”Remove-AzADGroup” [#10849]</span><span class="sxs-lookup"><span data-stu-id="73fd4-1275">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="73fd4-1276">Ett problem har åtgärdats som gjorde att ”MailNickname” inte returnerades i ”Remove-AzADGroup” [#11167]</span><span class="sxs-lookup"><span data-stu-id="73fd4-1276">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="73fd4-1277">Ett problem har åtgärdats som gjorde att pipe-åtgärden ”Remove-AzADGroup” inte fungerar [#11171]</span><span class="sxs-lookup"><span data-stu-id="73fd4-1277">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="73fd4-1278">Ett null-referensfel har åtgärdats i GetAzureRoleAssignmentCommand</span><span class="sxs-lookup"><span data-stu-id="73fd4-1278">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="73fd4-1279">Attribut för icke-bakåtkompatibla ändringar har lagts till för kommande ändringar i cmdlets för principer</span><span class="sxs-lookup"><span data-stu-id="73fd4-1279">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="73fd4-1280">”Get-AzResourceGroup” har uppdaterats för att utföra taggfiltrering för resursgrupper på serversidan</span><span class="sxs-lookup"><span data-stu-id="73fd4-1280">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="73fd4-1281">Utökade Tag-cmdlets stöder -ResourceId</span><span class="sxs-lookup"><span data-stu-id="73fd4-1281">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="73fd4-1282">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="73fd4-1282">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="73fd4-1283">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="73fd4-1283">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="73fd4-1284">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="73fd4-1284">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="73fd4-1285">Ny Tag-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-1285">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="73fd4-1286">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="73fd4-1286">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="73fd4-1287">Flyttade ScopedDeployment från SDK 3.3.0</span><span class="sxs-lookup"><span data-stu-id="73fd4-1287">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="73fd4-1288">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73fd4-1288">Az.Sql</span></span>
* <span data-ttu-id="73fd4-1289">PublicNetworkAccess har lagts till i ”New-AzSqlServer” och ”Set-AzSqlServer”</span><span class="sxs-lookup"><span data-stu-id="73fd4-1289">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="73fd4-1290">Stöd har lagts till för konfiguration av säkerhetskopiering för långsiktig kvarhållning för hanterade databaser</span><span class="sxs-lookup"><span data-stu-id="73fd4-1290">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="73fd4-1291">Hämta/ange LTR-princip på en hanterad databas</span><span class="sxs-lookup"><span data-stu-id="73fd4-1291">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="73fd4-1292">Hämta LTR-säkerhetskopior efter hanterad databas, hanterad instans eller plats</span><span class="sxs-lookup"><span data-stu-id="73fd4-1292">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="73fd4-1293">Ta bort en LTR-säkerhetskopia</span><span class="sxs-lookup"><span data-stu-id="73fd4-1293">Remove an LTR backup</span></span>
    - <span data-ttu-id="73fd4-1294">Återställa en LTR-säkerhetskopia för att skapa en ny hanterad databas</span><span class="sxs-lookup"><span data-stu-id="73fd4-1294">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="73fd4-1295">MinimalTlsVersion har lagts till för New-AzSqlServer och Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="73fd4-1295">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="73fd4-1296">MinimalTlsVersion har lagts till för New-AzSqlInstance och Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="73fd4-1296">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="73fd4-1297">SQL SDK-versionen för Az.Network har ändrats</span><span class="sxs-lookup"><span data-stu-id="73fd4-1297">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="73fd4-1298">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="73fd4-1298">Az.Storage</span></span>
* <span data-ttu-id="73fd4-1299">AllowProtectedAppendWrite stöds i ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="73fd4-1299">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="73fd4-1300">”Set-AzRmStorageContainerImmutabilityPolicy”</span><span class="sxs-lookup"><span data-stu-id="73fd4-1300">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="73fd4-1301">Varningsmeddelande har lagts till om icke-bakåtkompatibel ändring för ändring av typen AzureStorageTable i en senare version</span><span class="sxs-lookup"><span data-stu-id="73fd4-1301">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="73fd4-1302">”New-AzStorageTable”</span><span class="sxs-lookup"><span data-stu-id="73fd4-1302">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="73fd4-1303">”Get-AzStorageTable”</span><span class="sxs-lookup"><span data-stu-id="73fd4-1303">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="73fd4-1304">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="73fd4-1304">Az.Websites</span></span>
* <span data-ttu-id="73fd4-1305">Tag-parametern har lagts till för ”New-AzAppServicePlan” och ”Set-AzAppServicePlan”</span><span class="sxs-lookup"><span data-stu-id="73fd4-1305">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="73fd4-1306">Stoppa cmdlet-körning om ett undantag uppstår när en anpassad domän läggs till på en webbplats</span><span class="sxs-lookup"><span data-stu-id="73fd4-1306">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="73fd4-1307">Stöd har lagts till för att utföra åtgärder för App Services som inte tillhör samma resursgrupp som App Services-planen</span><span class="sxs-lookup"><span data-stu-id="73fd4-1307">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="73fd4-1308">Åtkomstbegränsning har tillämpats på WebApp/Function i olika resursgrupper</span><span class="sxs-lookup"><span data-stu-id="73fd4-1308">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="73fd4-1309">Ett problem har åtgärdats för att ange anpassade värdnamn för WebAppSlots</span><span class="sxs-lookup"><span data-stu-id="73fd4-1309">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="73fd4-1310">3.5.0 – februari 2020</span><span class="sxs-lookup"><span data-stu-id="73fd4-1310">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="73fd4-1311">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="73fd4-1311">Highlights since the last major release</span></span>
* <span data-ttu-id="73fd4-1312">Uppdaterade telemetri på klientsidan.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1312">Updated client side telemetry.</span></span>
* <span data-ttu-id="73fd4-1313">Az.IotHub lade till cmdletar som stöd för att hantera enheter.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1313">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="73fd4-1314">Az.SqlVirtualMachine lade till cmdletar för lyssningsfunktion för tillgänglighetsgrupp.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1314">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="73fd4-1315">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73fd4-1315">Az.Accounts</span></span>
* <span data-ttu-id="73fd4-1316">Lade till SubscriptionId, TenantId och körningstid i data för telemetri på klientsidan</span><span class="sxs-lookup"><span data-stu-id="73fd4-1316">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="73fd4-1317">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="73fd4-1317">Az.Automation</span></span>
* <span data-ttu-id="73fd4-1318">Åtgärdade skrivfel i exempel 1 i referensdokumentation för ”New-AzAutomationSoftwareUpdateConfiguration”</span><span class="sxs-lookup"><span data-stu-id="73fd4-1318">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="73fd4-1319">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="73fd4-1319">Az.CognitiveServices</span></span>
* <span data-ttu-id="73fd4-1320">Uppdaterade SDK till 7.0</span><span class="sxs-lookup"><span data-stu-id="73fd4-1320">Updated SDK to 7.0</span></span>
* <span data-ttu-id="73fd4-1321">Förbättrade felmeddelande vid serversvar om tom brödtext</span><span class="sxs-lookup"><span data-stu-id="73fd4-1321">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73fd4-1322">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73fd4-1322">Az.Compute</span></span>
* <span data-ttu-id="73fd4-1323">Tillät tomt värde för ProximityPlacementGroupId under uppdatering</span><span class="sxs-lookup"><span data-stu-id="73fd4-1323">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="73fd4-1324">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="73fd4-1324">Az.FrontDoor</span></span>
* <span data-ttu-id="73fd4-1325">Lade till cmdlet för att hämta hanterade regeldefinitioner som kan användas i WAF</span><span class="sxs-lookup"><span data-stu-id="73fd4-1325">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="73fd4-1326">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="73fd4-1326">Az.IotHub</span></span>
* <span data-ttu-id="73fd4-1327">Lade till stöd för att hantera enheter i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1327">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="73fd4-1328">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="73fd4-1328">New Cmdlets are:</span></span>
    - <span data-ttu-id="73fd4-1329">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="73fd4-1329">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="73fd4-1330">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="73fd4-1330">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="73fd4-1331">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="73fd4-1331">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="73fd4-1332">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="73fd4-1332">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="73fd4-1333">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="73fd4-1333">Az.KeyVault</span></span>
* <span data-ttu-id="73fd4-1334">Åtgärdade duplicerad text för Add-AzKeyVaultKey.md</span><span class="sxs-lookup"><span data-stu-id="73fd4-1334">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="73fd4-1335">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="73fd4-1335">Az.Monitor</span></span>
* <span data-ttu-id="73fd4-1336">Åtgärdade beskrivning av cmdleten Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1336">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="73fd4-1337">En ny parameter med namnet ActionGroupId har lagts till i kommandot ”New-AzMetricAlertRuleV2”.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1337">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="73fd4-1338">Användaren kan ange ActionGroupId(string) eller ActionGroup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="73fd4-1338">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73fd4-1339">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73fd4-1339">Az.Network</span></span>
* <span data-ttu-id="73fd4-1340">Lade till en extra parameteranteckning för parametern ”-EnableProxyProtocol” för cmdleten ”New-AzPrivateLinkService”.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1340">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="73fd4-1341">Åtgärdade FilterData-exempel i Start-AzVirtualNetworkGatewayConnectionPacketCapture.md och Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1341">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="73fd4-1342">Lade till paketinsamlingsexempel för att samla in alla inre och yttre paket i Start-AzVirtualNetworkGatewayConnectionPacketCapture.md och Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1342">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="73fd4-1343">Lade till stöd för Azure-brandväggsprincip på VNet-brandväggar</span><span class="sxs-lookup"><span data-stu-id="73fd4-1343">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="73fd4-1344">Inga nya cmdletar har lagts till.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1344">No new cmdlets are added.</span></span> <span data-ttu-id="73fd4-1345">Lättar begränsningen för brandväggsprincip på VNet-brandväggar</span><span class="sxs-lookup"><span data-stu-id="73fd4-1345">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="73fd4-1346">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="73fd4-1346">Az.RecoveryServices</span></span>
* <span data-ttu-id="73fd4-1347">Lade till stöd för Restore-as-files för SQL-databaser.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1347">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="73fd4-1348">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73fd4-1348">Az.Resources</span></span>
* <span data-ttu-id="73fd4-1349">Omstrukturerade cmdletar för malldistribution</span><span class="sxs-lookup"><span data-stu-id="73fd4-1349">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="73fd4-1350">Lade till nya cmdletar för att hantera distributioner i hanteringsgruppen: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="73fd4-1350">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="73fd4-1351">Lade till nya cmdletar för att hantera distributioner i klientorganisationsområdet: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="73fd4-1351">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="73fd4-1352">Omstrukturerade \*-AzDeployment-cmdletar för att fungera specifikt i prenumerationsomfattningen</span><span class="sxs-lookup"><span data-stu-id="73fd4-1352">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="73fd4-1353">Skapade alias \*-AzSubscriptionDeployment för \*-AzDeployment-cmdletar</span><span class="sxs-lookup"><span data-stu-id="73fd4-1353">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="73fd4-1354">Åtgärdade ”Update-AzADApplication” när parametern ”AvailableToOtherTenants” inte har angetts</span><span class="sxs-lookup"><span data-stu-id="73fd4-1354">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="73fd4-1355">Tog bort ApplicationObjectWithoutCredentialParameterSet för att undvika AmbiguousParameterSetException.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1355">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="73fd4-1356">Återskapade hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="73fd4-1356">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="73fd4-1357">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73fd4-1357">Az.Sql</span></span>
* <span data-ttu-id="73fd4-1358">Lade till stöd för återställning till tidpunkt mellan prenumerationer på hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1358">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="73fd4-1359">Lade till stöd för att ändra befintlig SQL Managed Instance-maskinvarugenerering</span><span class="sxs-lookup"><span data-stu-id="73fd4-1359">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="73fd4-1360">Åtgärdade ”Update-AzSqlServerVulnerabilityAssessmentSetting”-hjälpexempel: parameter/egenskapsutdata - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="73fd4-1360">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="73fd4-1361">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="73fd4-1361">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="73fd4-1362">Lade till cmdletar för lyssningsfunktion för tillgänglighetsgrupp</span><span class="sxs-lookup"><span data-stu-id="73fd4-1362">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="73fd4-1363">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="73fd4-1363">Az.StorageSync</span></span>
* <span data-ttu-id="73fd4-1364">Uppdaterade teckenuppsättningar som stöds i ”Invoke-AzStorageSyncCompatibilityCheck”.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1364">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="73fd4-1365">3.4.0 – februari 2020</span><span class="sxs-lookup"><span data-stu-id="73fd4-1365">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="73fd4-1366">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="73fd4-1366">Highlights since the last major release</span></span>
* <span data-ttu-id="73fd4-1367">Första Az.CosmosDB-versionen 0.1.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="73fd4-1367">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="73fd4-1368">Stöd för Az.Network ConnectionMonitor V2 har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-1368">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="73fd4-1369">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73fd4-1369">Az.Accounts</span></span>
* <span data-ttu-id="73fd4-1370">Inaktivera automatisk sparande av kontext när AzureRmContext.json inte är tillgängligt</span><span class="sxs-lookup"><span data-stu-id="73fd4-1370">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="73fd4-1371">Uppdatera referensen till Azure Powershell Common till 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="73fd4-1371">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="73fd4-1372">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="73fd4-1372">Az.ApiManagement</span></span>
* <span data-ttu-id="73fd4-1373">**Get-AzApiManagementApiSchema** Hämtning av Open-Api-schema som är associerat med ett API har åtgärdats   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="73fd4-1373">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="73fd4-1374">**New-AzApiManagementProduct** _ och _ *Set-AzApiManagementProduct*\*</span><span class="sxs-lookup"><span data-stu-id="73fd4-1374">**New-AzApiManagementProduct** _ and _ *Set-AzApiManagementProduct*\*</span></span>
  - <span data-ttu-id="73fd4-1375">Åtgärda dokumentation för https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="73fd4-1375">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="73fd4-1376">**Set-AzApiManagementApi** Exempel för att visa hur ServiceUrl uppdateras med hjälp av cmdleten har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-1376">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73fd4-1377">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73fd4-1377">Az.Compute</span></span>
* <span data-ttu-id="73fd4-1378">Begränsa antalet VM-status till 100 för att undvika begränsning när Get-AzVM -Status utförs utan VM-namn.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1378">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="73fd4-1379">Lägg till cmdleten Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="73fd4-1379">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="73fd4-1380">Lägg till parametrarna EncryptionType och DiskEncryptionSetId i följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="73fd4-1380">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="73fd4-1381">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="73fd4-1381">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="73fd4-1382">Lägg till parametern ColocationStatus för cmdleten Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1382">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="73fd4-1383">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="73fd4-1383">Az.DataFactory</span></span>
* <span data-ttu-id="73fd4-1384">Uppdatera ADF .Net SDK-versionen till 4.7.0</span><span class="sxs-lookup"><span data-stu-id="73fd4-1384">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="73fd4-1385">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="73fd4-1385">Az.DeploymentManager</span></span>
* <span data-ttu-id="73fd4-1386">Lägger till LIST-åtgärder för resurser</span><span class="sxs-lookup"><span data-stu-id="73fd4-1386">Adds LIST operations for resources</span></span>
* <span data-ttu-id="73fd4-1387">Lägger till funktion för att utföra åtgärder för hälsokontrollsteg</span><span class="sxs-lookup"><span data-stu-id="73fd4-1387">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="73fd4-1388">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="73fd4-1388">Az.HDInsight</span></span>
* <span data-ttu-id="73fd4-1389">Åtgärda dokumentfel för New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1389">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="73fd4-1390">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="73fd4-1390">Az.KeyVault</span></span>
* <span data-ttu-id="73fd4-1391">Lägg till Name-alias för attributet VaultName så att Remove-AzureKeyVault stämmer överens med New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1391">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73fd4-1392">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73fd4-1392">Az.Network</span></span>
* <span data-ttu-id="73fd4-1393">Nytt exempel har lagts till i Set-AzNetworkWatcherConfigFlowLog.md för att demonstrera ett inaktiveringsscenario för Trafikanalys.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1393">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="73fd4-1394">Lägg till stöd för att tilldela konfiguration av hanterings-IP till Azure Firewall – ett dedikerat undernät och en offentlig IP som brandväggen använder för dess hanteringstrafik</span><span class="sxs-lookup"><span data-stu-id="73fd4-1394">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="73fd4-1395">Cmdleten New-AzFirewall har uppdaterats:</span><span class="sxs-lookup"><span data-stu-id="73fd4-1395">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="73fd4-1396">Parametern -ManagementPublicIpAddress (inte obligatorisk) som accepterar ett offentligt IP-adressobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-1396">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="73fd4-1397">Metoden SetManagementIpConfiguration har lagts till för brandväggsobjekt – kräver ett undernät och en offentlig IP-adress som indata – undernätets namn måste vara ”AzureFirewallManagementSubnet”</span><span class="sxs-lookup"><span data-stu-id="73fd4-1397">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="73fd4-1398">Exempel för Get-AzNetworkSecurityGroup har korrigerats så att exempel visas för NSG:er i stället för nätverksgränssnitt.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1398">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="73fd4-1399">Ett skrivfel har åtgärdats i kommandot New-AzVpnSite som hindrade kompletteraren för resurs-ID från att fylla i en parameter.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1399">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="73fd4-1400">Stöd för Url-konfiguration i åtgärdsuppsättningen för omskrivningsregler i Application Gateway har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-1400">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="73fd4-1401">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="73fd4-1401">New cmdlets added:</span></span>
        - <span data-ttu-id="73fd4-1402">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="73fd4-1402">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="73fd4-1403">Cmdletar har uppdaterats med den valfria parametern -UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="73fd4-1403">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="73fd4-1404">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="73fd4-1404">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="73fd4-1405">Lägg till stöd för resurser för NetworkWatcher ConnectionMonitor version 2</span><span class="sxs-lookup"><span data-stu-id="73fd4-1405">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="73fd4-1406">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="73fd4-1406">Az.PolicyInsights</span></span>
* <span data-ttu-id="73fd4-1407">Stöd för utvärdering av efterlevnad innan fastställande av vilken resurs som ska åtgärdas</span><span class="sxs-lookup"><span data-stu-id="73fd4-1407">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="73fd4-1408">Lägg till parametern ”-ResourceDiscoverMode” för Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="73fd4-1408">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="73fd4-1409">Lägg till cmdleten Get-AzPolicyMetadata för att hämta resurser för principmetadata</span><span class="sxs-lookup"><span data-stu-id="73fd4-1409">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="73fd4-1410">Get-AzPolicyState och Get-AzPolicyStateSummary för API-versionen 2019-10-01 har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="73fd4-1410">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="73fd4-1411">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="73fd4-1411">Az.RecoveryServices</span></span>
* <span data-ttu-id="73fd4-1412">Azure Site Recovery-stöd för att ta bort en replikerad disk.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1412">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="73fd4-1413">Tillagt Azure Backup-stöd för att lägga till taggar när ett Recovery Services-valv skapas.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1413">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="73fd4-1414">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73fd4-1414">Az.Resources</span></span>
* <span data-ttu-id="73fd4-1415">Gör -Scope valfritt i cmdletarna \*-AzPolicyAssignment med standardinställning till kontextprenumeration</span><span class="sxs-lookup"><span data-stu-id="73fd4-1415">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="73fd4-1416">Lägg till exempel på att skapa ADServicePrincipal med lösenord och nyckelautentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="73fd4-1416">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="73fd4-1417">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73fd4-1417">Az.Sql</span></span>
<span data-ttu-id="73fd4-1418">Åtgärda cmdleten New-AzSqlDatabaseSecondary så att existensen PartnerDatabaseName kontrolleras i stället för existensen DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1418">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="73fd4-1419">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="73fd4-1419">Az.Storage</span></span>
* <span data-ttu-id="73fd4-1420">Stöd för angivning av krypteringsnyckeltyp för Tabell/kö i Skapa lagringskonto</span><span class="sxs-lookup"><span data-stu-id="73fd4-1420">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="73fd4-1421">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="73fd4-1421">New-AzStorageAccount</span></span>
* <span data-ttu-id="73fd4-1422">Visa RequestId när StorageException inte har ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="73fd4-1422">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="73fd4-1423">Åtgärda exempel 6 för cmdleten Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="73fd4-1423">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="73fd4-1424">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="73fd4-1424">Az.Websites</span></span>
* <span data-ttu-id="73fd4-1425">Set-AzWebapp och Set-AzWebappSlot stöder egenskaperna AlwaysOn, MinTls och FtpsState</span><span class="sxs-lookup"><span data-stu-id="73fd4-1425">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="73fd4-1426">Åtgärdar problemet där inställning av HttpsOnly samtidigt som AppservicePlan ändrades med det enskilda kommandot Set-AzWebApp återställde HttpsOnly till standardvärdet</span><span class="sxs-lookup"><span data-stu-id="73fd4-1426">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="73fd4-1427">3.3.0 – januari 2020</span><span class="sxs-lookup"><span data-stu-id="73fd4-1427">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="73fd4-1428">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73fd4-1428">Az.Accounts</span></span>
* <span data-ttu-id="73fd4-1429">Nu stöder Add-AzEnvironment och Set-AzEnvironment parametrarna AzureAttestationServiceEndpointResourceId och AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="73fd4-1429">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="73fd4-1430">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="73fd4-1430">Az.Cdn</span></span>
* <span data-ttu-id="73fd4-1431">Information om felsvar visas i New-AzCdnEndpoint-cmdleten</span><span class="sxs-lookup"><span data-stu-id="73fd4-1431">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73fd4-1432">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73fd4-1432">Az.Compute</span></span>
* <span data-ttu-id="73fd4-1433">Set-AzVMCustomScriptExtension-cmdleten har åtgärdats för en virtuell dator med hanterad OD-disk som inte har någon operativsystemprofil.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1433">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="73fd4-1434">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="73fd4-1434">Az.ContainerInstance</span></span>
* <span data-ttu-id="73fd4-1435">Parameternamn som används med New-AzContainerGroup-exempel har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="73fd4-1435">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="73fd4-1436">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="73fd4-1436">Az.DataBoxEdge</span></span>
* <span data-ttu-id="73fd4-1437">Cmdleten ”Get-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-1437">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="73fd4-1438">Hämta gränslagringscontainern</span><span class="sxs-lookup"><span data-stu-id="73fd4-1438">Get the Edge Storage Container</span></span>
* <span data-ttu-id="73fd4-1439">Cmdleten ”New-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-1439">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="73fd4-1440">Skapa en ny gränslagringscontainer</span><span class="sxs-lookup"><span data-stu-id="73fd4-1440">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="73fd4-1441">Cmdleten ”Remove-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-1441">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="73fd4-1442">Ta bort gränslagringscontainern</span><span class="sxs-lookup"><span data-stu-id="73fd4-1442">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="73fd4-1443">Cmdleten ”Invoke-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-1443">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="73fd4-1444">Anropa åtgärd för att uppdatera data i gränslagringscontainer</span><span class="sxs-lookup"><span data-stu-id="73fd4-1444">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="73fd4-1445">Cmdleten ”Get-AzDataBoxEdgeStorageAccount” har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-1445">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="73fd4-1446">Hämta gränslagringskontot</span><span class="sxs-lookup"><span data-stu-id="73fd4-1446">Get the Edge Storage Account</span></span>
* <span data-ttu-id="73fd4-1447">Cmdleten ”New-AzDataBoxEdgeStorageAccount” har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-1447">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="73fd4-1448">Skapa ett nytt gränslagringskonto</span><span class="sxs-lookup"><span data-stu-id="73fd4-1448">Create new Edge Storage Account</span></span>
* <span data-ttu-id="73fd4-1449">Cmdleten ”Remove-AzDataBoxEdgeStorageAccount” har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-1449">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="73fd4-1450">Ta bort gränslagringskontot</span><span class="sxs-lookup"><span data-stu-id="73fd4-1450">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="73fd4-1451">Anropa cmdleten ”Invoke-AzDataBoxEdgeShare”</span><span class="sxs-lookup"><span data-stu-id="73fd4-1451">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="73fd4-1452">Anropa åtgärd för att uppdatera resursdata</span><span class="sxs-lookup"><span data-stu-id="73fd4-1452">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="73fd4-1453">Cmdleten ”Set-AzDataBoxEdgeStorageAccountCredential” har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-1453">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="73fd4-1454">Ange autentiseringsuppgifter för az databoxedge-lagringskonto</span><span class="sxs-lookup"><span data-stu-id="73fd4-1454">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="73fd4-1455">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="73fd4-1455">Az.DataFactory</span></span>
* <span data-ttu-id="73fd4-1456">Lägg till AutoUpdateETA-, LatestVersion-, PushedVersion-, TaskQueueId- och VersionStatus-egenskaper för Get-AzDataFactoryV2IntegrationRuntime-cmd</span><span class="sxs-lookup"><span data-stu-id="73fd4-1456">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="73fd4-1457">Uppdatera ADF .Net SDK-versionen till 4.6.0</span><span class="sxs-lookup"><span data-stu-id="73fd4-1457">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="73fd4-1458">Lägg till parametern ”PublicIPs” för ”Set-AzureRmDataFactoryV2IntegrationRuntime”-cmd så att Azure-SSIS IR kan skapas med statiska offentliga IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1458">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="73fd4-1459">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="73fd4-1459">Az.DevTestLabs</span></span>
* <span data-ttu-id="73fd4-1460">Ta bort den brutna länken i Get-AzDtlAllowedVMSizesPolicy.md</span><span class="sxs-lookup"><span data-stu-id="73fd4-1460">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="73fd4-1461">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="73fd4-1461">Az.EventHub</span></span>
* <span data-ttu-id="73fd4-1462">Korrigering av problem 10634: Åtgärda referensen till null-objekt för eventhubnamespace-borttagning</span><span class="sxs-lookup"><span data-stu-id="73fd4-1462">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="73fd4-1463">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="73fd4-1463">Az.HDInsight</span></span>
* <span data-ttu-id="73fd4-1464">Åtgärda Invoke-AzHDInsightHiveJob.md-fel.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1464">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="73fd4-1465">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="73fd4-1465">Az.MachineLearning</span></span>
* <span data-ttu-id="73fd4-1466">Nedanstående cmdletar har tagits bort eftersom MachineLearningCompute inte längre är tillgängligt</span><span class="sxs-lookup"><span data-stu-id="73fd4-1466">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="73fd4-1467">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="73fd4-1467">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="73fd4-1468">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="73fd4-1468">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="73fd4-1469">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="73fd4-1469">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="73fd4-1470">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="73fd4-1470">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="73fd4-1471">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="73fd4-1471">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="73fd4-1472">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="73fd4-1472">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="73fd4-1473">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="73fd4-1473">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73fd4-1474">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73fd4-1474">Az.Network</span></span>
* <span data-ttu-id="73fd4-1475">Uppgradera beroende av Microsoft.Azure.Management.Sql från 1.36-preview till 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="73fd4-1475">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="73fd4-1476">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="73fd4-1476">Az.RecoveryServices</span></span>
* <span data-ttu-id="73fd4-1477">Ändrat Azure Site Recovery-stöd för krypterade vilande data på virtuella datorer med hanterade diskar med kundhanterade nycklar för Azure till Azure-providern.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1477">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="73fd4-1478">Azure Site Recovery-stöd för att ange ID för diskkrypteringsuppsättning som valfri inmatning för aktivering av skydd för VMware till Azure.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1478">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="73fd4-1479">Azure Site Recovery-stöd för att ange ID för diskkrypteringsuppsättning som valfri inmatning på disknivå för aktivering av skydd för VMware till Azure.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1479">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="73fd4-1480">Azure Site Recovery-stöd för att uppdatera replikeringsskyddade objekt med mappning för diskkrypteringsuppsättning för HyperV till Azure.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1480">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="73fd4-1481">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73fd4-1481">Az.Resources</span></span>
* <span data-ttu-id="73fd4-1482">Åtgärda ett fel i hjälpdokument för ”Remove-AzTag”.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1482">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="73fd4-1483">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73fd4-1483">Az.Sql</span></span>
* <span data-ttu-id="73fd4-1484">Åtgärda funktioner i cmdletar för att ange baslinjen för sårbarhetsbedömning för arbete med huvuddatabasen för Azure-databasen och begränsa den för systemdatabaser på hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1484">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="73fd4-1485">Åtgärda ett fel när en redundansgrupp för en SQL-instans skapas</span><span class="sxs-lookup"><span data-stu-id="73fd4-1485">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="73fd4-1486">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="73fd4-1486">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="73fd4-1487">Lägg till DR som en ny giltig licenstyp</span><span class="sxs-lookup"><span data-stu-id="73fd4-1487">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="73fd4-1488">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="73fd4-1488">Az.Storage</span></span>
* <span data-ttu-id="73fd4-1489">Lägg till varningsmeddelande om icke-bakåtkompatibel ändring för DefaultAction-värdeändring i en framtida version</span><span class="sxs-lookup"><span data-stu-id="73fd4-1489">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="73fd4-1490">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="73fd4-1490">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="73fd4-1491">Stöd för att hämta lagringskontots senaste synkroniseringstid genom att köra get-AzureRMStorageAccount med parametern -IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="73fd4-1491">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="73fd4-1492">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="73fd4-1492">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="73fd4-1493">3.2.0 – December 2019</span><span class="sxs-lookup"><span data-stu-id="73fd4-1493">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="73fd4-1494">Allmänt</span><span class="sxs-lookup"><span data-stu-id="73fd4-1494">General</span></span>
* <span data-ttu-id="73fd4-1495">Uppdatera referenser i .psd1 för att använda relativa sökvägar för alla moduler</span><span class="sxs-lookup"><span data-stu-id="73fd4-1495">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="73fd4-1496">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73fd4-1496">Az.Accounts</span></span>
* <span data-ttu-id="73fd4-1497">Ange rätt UserAgent för telemetri på klientsidan för Az 4.0 preview</span><span class="sxs-lookup"><span data-stu-id="73fd4-1497">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="73fd4-1498">Visa användarvänligt felmeddelande när kontexten är null i Az 4.0 preview</span><span class="sxs-lookup"><span data-stu-id="73fd4-1498">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="73fd4-1499">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="73fd4-1499">Az.Batch</span></span>
* <span data-ttu-id="73fd4-1500">Korrigera problem [#10602](https://github.com/Azure/azure-powershell/issues/10602), där **New-AzBatchPool** skickade VirtualMachineConfiguration.ContainerConfiguration eller VirtualMachineConfiguration.DataDisks på ett felaktigt sätt till servern.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1500">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="73fd4-1501">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="73fd4-1501">Az.DataFactory</span></span>
* <span data-ttu-id="73fd4-1502">Uppdatera ADF .Net SDK-versionen till 4.5.0</span><span class="sxs-lookup"><span data-stu-id="73fd4-1502">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="73fd4-1503">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="73fd4-1503">Az.FrontDoor</span></span>
* <span data-ttu-id="73fd4-1504">Stöd har lagts till för undantag för hanterade regler för brandväggen för webbaserade program</span><span class="sxs-lookup"><span data-stu-id="73fd4-1504">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="73fd4-1505">Lägg till SocketAddr för automatisk komplettering</span><span class="sxs-lookup"><span data-stu-id="73fd4-1505">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="73fd4-1506">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="73fd4-1506">Az.HealthcareApis</span></span>
* <span data-ttu-id="73fd4-1507">Undantagshantering</span><span class="sxs-lookup"><span data-stu-id="73fd4-1507">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="73fd4-1508">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="73fd4-1508">Az.KeyVault</span></span>
* <span data-ttu-id="73fd4-1509">Åtgärdat fel vid åtkomst av värde som kanske inte har angetts</span><span class="sxs-lookup"><span data-stu-id="73fd4-1509">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="73fd4-1510">Hantering av ECC-certifikat (Elliptic Curve Cryptography)</span><span class="sxs-lookup"><span data-stu-id="73fd4-1510">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="73fd4-1511">Stöd har lagts till för att ange kurvan för certifikatprinciper</span><span class="sxs-lookup"><span data-stu-id="73fd4-1511">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="73fd4-1512">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="73fd4-1512">Az.Monitor</span></span>
* <span data-ttu-id="73fd4-1513">Lägger till valfritt argument i kommandot Lägg till diagnostikinställningar.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1513">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="73fd4-1514">Ett växelargument som om det finns visar att exporten till Log Analytics måste ske till ett fast schema (kallas även</span><span class="sxs-lookup"><span data-stu-id="73fd4-1514">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="73fd4-1515">dedikerad, datatyp)</span><span class="sxs-lookup"><span data-stu-id="73fd4-1515">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73fd4-1516">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73fd4-1516">Az.Network</span></span>
* <span data-ttu-id="73fd4-1517">Stöd för IpGroups i program-, NAT- och nätverksregler för Azure Firewall.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1517">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="73fd4-1518">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73fd4-1518">Az.Resources</span></span>
* <span data-ttu-id="73fd4-1519">Åtgärda ett problem där malldistributionen inte kan läsa en mallparameter om dess namn står i konflikt med ett inbyggt parameternamn.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1519">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="73fd4-1520">Uppdaterade princip-cmdletar för att använda den nya API-versionen 2019-09-01 som introducerar grupperingsstöd inom principuppsättningsdefinitioner.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1520">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="73fd4-1521">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73fd4-1521">Az.Sql</span></span>
* <span data-ttu-id="73fd4-1522">Uppgraderad funktion för att skapa lagring i automatisk aktivering av sårbarhetsbedömning till StorageV2</span><span class="sxs-lookup"><span data-stu-id="73fd4-1522">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="73fd4-1523">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="73fd4-1523">Az.Storage</span></span>
* <span data-ttu-id="73fd4-1524">Stöd för generering av blob/container-identitetsbaserad SAS-token med lagringskontextbaserad på OAuth-autentisering</span><span class="sxs-lookup"><span data-stu-id="73fd4-1524">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="73fd4-1525">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="73fd4-1525">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="73fd4-1526">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="73fd4-1526">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="73fd4-1527">Stöd för återkallning av användardelegeringsnycklar för lagringskonto för att återkalla alla SAS-token</span><span class="sxs-lookup"><span data-stu-id="73fd4-1527">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="73fd4-1528">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="73fd4-1528">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="73fd4-1529">Uppgradera till Microsoft.Azure.Management.Storage 14.2.0 för att stödja den nya API-versionen 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1529">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="73fd4-1530">Stöd för QuotaGiB (resurskvot i Gibibye) för värden över 5120 i hanteringsplanet för cmdletar för filresurser och parameteraliaset. Quota har också lagts till för parametern ”QuotaGiB”.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1530">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="73fd4-1531">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="73fd4-1531">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="73fd4-1532">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="73fd4-1532">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="73fd4-1533">Lägg till parameteraliaset QuotaGiB i parametern Quota</span><span class="sxs-lookup"><span data-stu-id="73fd4-1533">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="73fd4-1534">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="73fd4-1534">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="73fd4-1535">Åtgärda problemet att Set-AzStorageContainerAcl kan rensa den lagrade åtkomstprincipen</span><span class="sxs-lookup"><span data-stu-id="73fd4-1535">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="73fd4-1536">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="73fd4-1536">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="73fd4-1537">3.1.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="73fd4-1537">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="73fd4-1538">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="73fd4-1538">Highlights since the last major release</span></span>
* <span data-ttu-id="73fd4-1539">Az.DataBoxEdge 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="73fd4-1539">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="73fd4-1540">Az.SqlVirtualMachine 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="73fd4-1540">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73fd4-1541">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73fd4-1541">Az.Compute</span></span>
* <span data-ttu-id="73fd4-1542">Funktion för att använda en virtuell dator igen</span><span class="sxs-lookup"><span data-stu-id="73fd4-1542">VM Reapply feature</span></span>
    - <span data-ttu-id="73fd4-1543">Lägg till parameter för att använda igen till cmdleten Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="73fd4-1543">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="73fd4-1544">Funktionen AutomaticRepairs i VM-skalningsuppsättningar:</span><span class="sxs-lookup"><span data-stu-id="73fd4-1544">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="73fd4-1545">Lägg till parametrarna EnableAutomaticRepair, AutomaticRepairGracePeriod och AutomaticRepairMaxInstanceRepairsPercent till följande cmdletar:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="73fd4-1545">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="73fd4-1546">Stöd för galleriavbildningar i flera klientorganisationer för New-AzVM</span><span class="sxs-lookup"><span data-stu-id="73fd4-1546">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="73fd4-1547">Lägg till "Spot" till argumentslutföraren i prioritetsparametern i cmdletarna New-AzVM, New-AzVMConfig och New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="73fd4-1547">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="73fd4-1548">Lägg till parametrarna DiskIOPSReadWrite och DiskMBpsReadWrite till cmdleten Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="73fd4-1548">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="73fd4-1549">Ändra parametern SourceImageId för cmdleten New-AzGalleryImageVersion till valfri</span><span class="sxs-lookup"><span data-stu-id="73fd4-1549">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="73fd4-1550">Lägg till parametrarna OSDiskImage och DataDiskImage till cmdleten New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="73fd4-1550">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="73fd4-1551">Lägg till parametern HyperVGeneration till cmdleten New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="73fd4-1551">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="73fd4-1552">Lägg till parametern SkipExtensionsOnOverprovisionedVMs till cmdletarna New-AzVmss, New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="73fd4-1552">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="73fd4-1553">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="73fd4-1553">Az.DataBoxEdge</span></span>
* <span data-ttu-id="73fd4-1554">Cmdleten `Get-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-1554">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="73fd4-1555">Hämta ordning</span><span class="sxs-lookup"><span data-stu-id="73fd4-1555">Get the Order</span></span>
* <span data-ttu-id="73fd4-1556">Cmdleten `New-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-1556">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="73fd4-1557">Skapa ny ordning</span><span class="sxs-lookup"><span data-stu-id="73fd4-1557">Create new Order</span></span>
* <span data-ttu-id="73fd4-1558">Cmdleten `Remove-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-1558">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="73fd4-1559">Ta bort ordning</span><span class="sxs-lookup"><span data-stu-id="73fd4-1559">Remove the Order</span></span>
* <span data-ttu-id="73fd4-1560">Cmdleten `New-AzDataBoxEdgeShare` har ändrats</span><span class="sxs-lookup"><span data-stu-id="73fd4-1560">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="73fd4-1561">Nu skapas lokal filresurs</span><span class="sxs-lookup"><span data-stu-id="73fd4-1561">Now creates Local Share</span></span>
* <span data-ttu-id="73fd4-1562">Cmdleten `Set-AzDataBoxEdgeRole` har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-1562">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="73fd4-1563">Nu kan IotRole mappas till filresursen</span><span class="sxs-lookup"><span data-stu-id="73fd4-1563">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="73fd4-1564">Cmdleten `Invoke-AzDataBoxEdgeDevice` har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-1564">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="73fd4-1565">Anropa genomsökningsuppdatering, ladda ned uppdatering, installera uppdateringar på enheten</span><span class="sxs-lookup"><span data-stu-id="73fd4-1565">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="73fd4-1566">Cmdleten `Get-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-1566">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="73fd4-1567">Hämtar information om utlösare</span><span class="sxs-lookup"><span data-stu-id="73fd4-1567">Gets the information about Triggers</span></span>
* <span data-ttu-id="73fd4-1568">Cmdleten `New-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-1568">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="73fd4-1569">Skapa nya utlösare</span><span class="sxs-lookup"><span data-stu-id="73fd4-1569">Create new Triggers</span></span>
* <span data-ttu-id="73fd4-1570">Cmdleten `Remove-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-1570">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="73fd4-1571">Ta bort utlösare</span><span class="sxs-lookup"><span data-stu-id="73fd4-1571">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="73fd4-1572">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="73fd4-1572">Az.DataFactory</span></span>
* <span data-ttu-id="73fd4-1573">Uppdatera ADF .Net SDK-versionen till 4.4.0</span><span class="sxs-lookup"><span data-stu-id="73fd4-1573">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="73fd4-1574">Lägg till parametern ExpressCustomSetup för kommandot Set-AzureRmDataFactoryV2IntegrationRuntime för att aktivera installationskonfigurationer och komponenter från tredje part utan anpassat konfigurationsskript.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1574">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="73fd4-1575">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="73fd4-1575">Az.DataLakeStore</span></span>
* <span data-ttu-id="73fd4-1576">Uppdatera dokumentation för Get-AzDataLakeStoreDeletedItem och Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="73fd4-1576">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="73fd4-1577">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="73fd4-1577">Az.EventHub</span></span>
* <span data-ttu-id="73fd4-1578">Korrigering av problem #10301: Korrigera datumformat för SAS-token</span><span class="sxs-lookup"><span data-stu-id="73fd4-1578">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="73fd4-1579">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="73fd4-1579">Az.FrontDoor</span></span>
* <span data-ttu-id="73fd4-1580">Lägg till parametern MinimumTlsVersion till Enable-AzFrontDoorCustomDomainHttps och New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="73fd4-1580">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="73fd4-1581">Lägg till parametrarna HealthProbeMethod och EnabledState till New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="73fd4-1581">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="73fd4-1582">Lägg till en ny cmdlet för att skapa BackendPoolsSettings-objekt som passar i skapande/uppdatering av Front Door</span><span class="sxs-lookup"><span data-stu-id="73fd4-1582">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="73fd4-1583">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="73fd4-1583">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73fd4-1584">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73fd4-1584">Az.Network</span></span>
* <span data-ttu-id="73fd4-1585">Ändra alternativexemplen Start-AzVirtualNetworkGatewayConnectionPacketCapture.md och Start-AzVirtualnetworkGatewayPacketCapture.md för FilterData.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1585">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="73fd4-1586">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="73fd4-1586">Az.PrivateDns</span></span>
* <span data-ttu-id="73fd4-1587">Uppdaterade PrivateDns .NET SDK till version 1.0.0</span><span class="sxs-lookup"><span data-stu-id="73fd4-1587">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="73fd4-1588">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="73fd4-1588">Az.RecoveryServices</span></span>
* <span data-ttu-id="73fd4-1589">Stöd för att välja disktyp vid aktivering av skydd i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1589">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="73fd4-1590">Korrigering av bugg för åtgärdsredigering av återställningsplan i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1590">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="73fd4-1591">Återställningsstöd för att godkänna filestream-databaser i Azure Backup SQL.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1591">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="73fd4-1592">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="73fd4-1592">Az.RedisCache</span></span>
* <span data-ttu-id="73fd4-1593">Parametern MinimumTlsVersion har lagts till i cmdletarna New-AzRedisCache och Set-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1593">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="73fd4-1594">Dessutom har MinimumTlsVersion lagts till i utdata för cmdleten Get-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1594">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="73fd4-1595">Verifiering har lagts till på parametern -Size i cmdletarna Set-AzRedisCache och New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="73fd4-1595">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="73fd4-1596">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73fd4-1596">Az.Resources</span></span>
- <span data-ttu-id="73fd4-1597">Uppdaterade policy-cmdletar för att använda den nya API-versionen 2019-06-01 som har en ny EnforcementMode-egenskap i policytilldelningen.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1597">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="73fd4-1598">Uppdaterade hjälpexempel för skapandet av policydefinition</span><span class="sxs-lookup"><span data-stu-id="73fd4-1598">Updated create policy definition help example</span></span>
- <span data-ttu-id="73fd4-1599">Åtgärda bugg i Remove-AZADServicePrincipal -ServicePrincipalName, utlös null-referens när tjänstens huvudnamn inte hittas.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1599">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="73fd4-1600">Åtgärda bugg i New-AZADServicePrincipal, utlös null-referens när klientorganisationen inte har någon prenumeration.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1600">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="73fd4-1601">Ändra New-AzAdServicePrincipal för att endast lägga till autentiseringsuppgifter för det associerade programmet.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1601">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="73fd4-1602">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73fd4-1602">Az.Sql</span></span>
* <span data-ttu-id="73fd4-1603">Stöd har lagts till för databasen ReadReplicaCount.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1603">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="73fd4-1604">Korrigerade Set-AzSqlDatabase när zonredundans inte har angetts</span><span class="sxs-lookup"><span data-stu-id="73fd4-1604">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="73fd4-1605">3.0.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="73fd4-1605">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="73fd4-1606">Allmänt</span><span class="sxs-lookup"><span data-stu-id="73fd4-1606">General</span></span>
* <span data-ttu-id="73fd4-1607">Az. PrivateDns 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="73fd4-1607">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="73fd4-1608">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73fd4-1608">Az.Accounts</span></span>
* <span data-ttu-id="73fd4-1609">Lägg till ett utfasningsmeddelande för aliaset Resolve-error.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1609">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="73fd4-1610">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="73fd4-1610">Az.Advisor</span></span>
* <span data-ttu-id="73fd4-1611">Den nya kategorin Operational Excellence har lagts till i cmdleten Get-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1611">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="73fd4-1612">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="73fd4-1612">Az.Batch</span></span>
* <span data-ttu-id="73fd4-1613">`CoreQuota` på `BatchAccountContext` har bytt namn till `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1613">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="73fd4-1614">Det finns även en ny `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1614">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="73fd4-1615">Detta påverkar **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1615">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="73fd4-1616">**New-AzBatchTask** `-ResourceFile`-parametern tar nu en samling `PSResourceFile`-objekt som kan skapas med hjälp av den nya cmdleten **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1616">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="73fd4-1617">Ny **New-AzBatchResourceFile**-cmdlet för att skapa `PSResourceFile`-objekt.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1617">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="73fd4-1618">Dessa kan tillhandahållas till **New-AzBatchTask** på `-ResourceFile`-parametern.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1618">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="73fd4-1619">Detta stöder två nya typer av resursfiler förutom det befintliga sättet med `HttpUrl`:</span><span class="sxs-lookup"><span data-stu-id="73fd4-1619">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="73fd4-1620">`AutoStorageContainerName`-baserade resursfiler laddar ned en hel container för automatisk lagring till Batch-noden.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1620">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="73fd4-1621">`StorageContainerUrl`-baserade resursfiler laddar ned containern som anges i webbadressen till Batch-noden.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1621">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="73fd4-1622">Tog bort egenskapen `ApplicationPackages` för `PSApplication` som returnerades av **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1622">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="73fd4-1623">Specifika paket i ett program kan nu hämtas med hjälp av **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1623">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="73fd4-1624">Till exempel: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1624">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="73fd4-1625">Bytt namn på `ApplicationId` till `ApplicationName` på **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** och **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1625">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="73fd4-1626">`ApplicationId` är nu ett alias för `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1626">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="73fd4-1627">Ny `PSWindowsUserConfiguration`-egenskap till `PSUserAccount` lades till.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1627">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="73fd4-1628">Bytte namn på `Version` till `Name` på `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1628">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="73fd4-1629">Bytte namn på `BlobSource` till `HttpUrl` på `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1629">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="73fd4-1630">Tog bort egenskapen `OSDisk` från `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1630">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="73fd4-1631">Tog bort **Set-AzBatchPoolOSVersion**.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1631">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="73fd4-1632">Den här åtgärden stöds inte längre.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1632">This operation is no longer supported.</span></span>
* <span data-ttu-id="73fd4-1633">`TargetOSVersion` har tagits bort från `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1633">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="73fd4-1634">Bytte namn på `CurrentOSVersion` till `OSVersion` på `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1634">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="73fd4-1635">`DataEgressGiB` och `DataIngressGiB` har tagits bort från `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1635">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="73fd4-1636">Tog bort **Get-AzBatchNodeAgentSku** och ersatte det med **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1636">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="73fd4-1637">**Get-AzBatchSupportedImage** returnerar samma data som **Get-AzBatchNodeAgentSku** men i ett mer användarvänligt format.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1637">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="73fd4-1638">Nya icke-verifierade avbildningar returneras nu också.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1638">New non-verified images are also now returned.</span></span> <span data-ttu-id="73fd4-1639">Ytterligare information om `Capabilities` och `BatchSupportEndOfLife` för varje avbildning inkluderas också.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1639">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="73fd4-1640">Lade till möjlighet att montera fjärrfilsystem på varje nod i en pool via den nya parametern `MountConfiguration` för **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1640">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="73fd4-1641">Har nu stöd för nätverkssäkerhetsregler som blockerar nätverksåtkomst till en pool baserat på källportens trafik.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1641">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="73fd4-1642">Detta görs via egenskapen `SourcePortRanges` på `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1642">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="73fd4-1643">När du kör en container stöder nu Batch körningen av uppgiften i arbetskatalogen för containern eller i arbetskatalogen för Batch-uppgiften.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1643">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="73fd4-1644">Detta styrs av egenskapen `WorkingDirectory` på `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1644">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="73fd4-1645">Lade till en funktion för att ange en samling av offentliga IP-adresser på `PSNetworkConfiguration` via den nya egenskapen `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1645">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="73fd4-1646">Detta garanterar att noderna i poolen har en IP-adress från listan över IP-adresser som tillhandahållits av användare.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1646">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="73fd4-1647">Om inget värde anges är standardvärdet för `WaitForSuccess` på `PSSTartTask` nu `$True` (var tidigare `$False`).</span><span class="sxs-lookup"><span data-stu-id="73fd4-1647">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="73fd4-1648">Om inget värde anges är standardvärdet för `Scope` på `PSAutoUserSpecification` nu `Pool` (var tidigare `Task` på Windows och `Pool` på Linux).</span><span class="sxs-lookup"><span data-stu-id="73fd4-1648">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="73fd4-1649">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="73fd4-1649">Az.Cdn</span></span>
* <span data-ttu-id="73fd4-1650">Introducerade UrlRewriteAction och CacheKeyQueryStringAction till RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1650">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="73fd4-1651">Åtgärdade flera buggar, som saknade indata för ”väljare” i cmdleten New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1651">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73fd4-1652">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73fd4-1652">Az.Compute</span></span>
* <span data-ttu-id="73fd4-1653">Funktion för diskkrypteringsuppsättning</span><span class="sxs-lookup"><span data-stu-id="73fd4-1653">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="73fd4-1654">Nya cmdletar:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="73fd4-1654">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="73fd4-1655">Parametern DiskEncryptionSetId har lagts till i följande cmdletar:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="73fd4-1655">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="73fd4-1656">Parametrarna DiskEncryptionSetId och EncryptionType har lagts till i följande cmdletar:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="73fd4-1656">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="73fd4-1657">Lägg till parametern PublicIPAddressVersion i New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="73fd4-1657">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="73fd4-1658">Flytta FileUris för anpassat skripttillägg från offentlig inställning till skyddad inställning</span><span class="sxs-lookup"><span data-stu-id="73fd4-1658">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="73fd4-1659">Lägg till ScaleInPolicy i cmdletarna New-AzVmss, New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="73fd4-1659">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="73fd4-1660">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="73fd4-1660">Breaking changes</span></span>
    - <span data-ttu-id="73fd4-1661">Parametern UploadSizeInBytes används istället för DiskSizeGB för New-AzDiskConfig när CreateOption är Uppladdning</span><span class="sxs-lookup"><span data-stu-id="73fd4-1661">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="73fd4-1662">PublishingProfile.Source.ManagedImage.Id ersätts med StorageProfile.Source.Id i objektet GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="73fd4-1662">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="73fd4-1663">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="73fd4-1663">Az.DataFactory</span></span>
* <span data-ttu-id="73fd4-1664">Uppdatera ADF .Net SDK-versionen till 4.3.0</span><span class="sxs-lookup"><span data-stu-id="73fd4-1664">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="73fd4-1665">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="73fd4-1665">Az.DataLakeStore</span></span>
* <span data-ttu-id="73fd4-1666">Uppdatera ADLS SDK-version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) innehåller följande korrigeringar</span><span class="sxs-lookup"><span data-stu-id="73fd4-1666">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="73fd4-1667">Undvik att utlösa undantag när det inte går att deserialisera creationtime för inmatning av papperskorg eller katalog.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1667">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="73fd4-1668">Gör inställning tillgänglig per tidsgräns för förfrågan i adlsclient</span><span class="sxs-lookup"><span data-stu-id="73fd4-1668">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="73fd4-1669">Korrigera överföringen av ursprunglig syncflag för badoffset-återställning</span><span class="sxs-lookup"><span data-stu-id="73fd4-1669">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="73fd4-1670">Korrigera EnumerateDirectory för att hämta fortsättningstoken när svar har kontrollerats</span><span class="sxs-lookup"><span data-stu-id="73fd4-1670">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="73fd4-1671">Korrigera bugg i Concat</span><span class="sxs-lookup"><span data-stu-id="73fd4-1671">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="73fd4-1672">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="73fd4-1672">Az.FrontDoor</span></span>
* <span data-ttu-id="73fd4-1673">Åtgärdade diverse stavfel i modul</span><span class="sxs-lookup"><span data-stu-id="73fd4-1673">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="73fd4-1674">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="73fd4-1674">Az.HDInsight</span></span>
* <span data-ttu-id="73fd4-1675">Korrigerade buggen att kunder får felet ”inte en giltig Base-64-sträng” vid användning av Get-AzHDInsightCluster för att hämta klustret med ADLSGen1-lagring.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1675">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="73fd4-1676">Lägg till en parameter med namnet ”ApplicationId” i de tre cmdletarna Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig och New-AzHDInsightCluster så att kunden kan tillhandahålla tjänstens huvudnamn för program-ID för åtkomst till Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1676">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="73fd4-1677">Ändrade Microsoft.Azure.Management.HDInsight från 2.1.0 till 5.1.0</span><span class="sxs-lookup"><span data-stu-id="73fd4-1677">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="73fd4-1678">Fem cmdletar har tagits bort:</span><span class="sxs-lookup"><span data-stu-id="73fd4-1678">Removed five cmdlets:</span></span>
    - <span data-ttu-id="73fd4-1679">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="73fd4-1679">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="73fd4-1680">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="73fd4-1680">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="73fd4-1681">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="73fd4-1681">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="73fd4-1682">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="73fd4-1682">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="73fd4-1683">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="73fd4-1683">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="73fd4-1684">Tre cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="73fd4-1684">Added three cmdlets:</span></span>
    - <span data-ttu-id="73fd4-1685">Get-AzHDInsightMonitoring som ersätter Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1685">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="73fd4-1686">Enable-AzHDInsightMonitoring som ersätter Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1686">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="73fd4-1687">Disable-AzHDInsightMonitoring som ersätter Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1687">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="73fd4-1688">Korrigerade cmdleten Get-AzHDInsightProperties för att stödja hämtning av funktionsinformation från en viss plats.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1688">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="73fd4-1689">Parameteruppsättningarna (Spark1 och Spark2) har tagits bort från Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1689">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="73fd4-1690">Lägg till exempel för cmdleten Add-AzHDInsightSecurityProfile till hjälpdokumenten.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1690">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="73fd4-1691">Ändrade utdatatyp för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="73fd4-1691">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="73fd4-1692">Ändrade utdatatyp för Get-AzHDInsightProperties från CapabilitiesResponse till AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1692">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="73fd4-1693">Ändrade utdatatyp för Remove-AzHDInsightCluster från ClusterGetResponse till bool.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1693">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="73fd4-1694">Ändrade utdatatyp för Set-AzHDInsightGatewaySettings HttpConnectivitySettings till GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1694">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="73fd4-1695">Lade till testfall för vissa scenarier.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1695">Added some scenario test cases.</span></span>
* <span data-ttu-id="73fd4-1696">Ta bort vissa alias: Add-AzHDInsightConfigValues, Get-AzHDInsightProperties.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1696">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="73fd4-1697">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="73fd4-1697">Az.IotHub</span></span>
* <span data-ttu-id="73fd4-1698">Icke-bakåtkompatibla ändringar:</span><span class="sxs-lookup"><span data-stu-id="73fd4-1698">Breaking changes:</span></span>
    - <span data-ttu-id="73fd4-1699">Cmdleten Add-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1699">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="73fd4-1700">Parameteruppsättningen __AllParameterSets för cmdleten Add-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1700">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="73fd4-1701">Cmdleten Get-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1701">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="73fd4-1702">Parameteruppsättningen __AllParameterSets för cmdleten Get-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1702">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="73fd4-1703">Egenskapen OperationsMonitoringProperties av typen Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1703">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="73fd4-1704">Egenskapen OperationsMonitoringProperties av typen Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1704">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="73fd4-1705">Cmdleten New-AzIotHubExportDevice stöder inte längre aliaset New-AzIotHubExportDevices.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1705">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="73fd4-1706">Cmdleten New-AzIotHubImportDevice stöder inte längre aliaset New-AzIotHubImportDevices.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1706">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="73fd4-1707">Cmdleten Remove-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1707">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="73fd4-1708">Parameteruppsättningen __AllParameterSets för cmdleten Remove-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1708">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="73fd4-1709">Cmdleten Set-AzIotHub har inte längre stöd för parametern OperationsMonitoringProperties och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1709">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="73fd4-1710">Parameteruppsättningen UpdateOperationsMonitoringProperties för cmdleten Set-AzIotHub har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1710">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="73fd4-1711">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="73fd4-1711">Az.RecoveryServices</span></span>
* <span data-ttu-id="73fd4-1712">Azure Site Recovery-stöd för att konfigurera nätverksresurser som NSG, offentliga IP-adresser och interna lastbalanserare för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1712">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="73fd4-1713">Azure Site Recovery-stöd för att skriva till hanterad disk för vMWare till Azure.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1713">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="73fd4-1714">Azure Site Recovery-stöd för NIC-reduktion för vMWare till Azure.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1714">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="73fd4-1715">Azure Site Recovery-stöd för accelererat nätverk för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1715">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="73fd4-1716">Azure Site Recovery-stöd för automatisk uppdatering av agent för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1716">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="73fd4-1717">Azure Site Recovery-stöd för Standard SSD för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1717">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="73fd4-1718">Azure Site Recovery-stöd för tvåstegskryptering i Azure Disk Encryption för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1718">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="73fd4-1719">Azure Site Recovery-stöd för att skydda nyligen tillagda diskar för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1719">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="73fd4-1720">En funktion för mjuk borttagning av virtuella datorer samt tester för mjuk borttagning har tagits bort</span><span class="sxs-lookup"><span data-stu-id="73fd4-1720">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="73fd4-1721">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73fd4-1721">Az.Resources</span></span>
* <span data-ttu-id="73fd4-1722">Uppdatera beroendesammansättning för Microsoft.Extensions.Caching.Memory från 1.1.1 till 2.2</span><span class="sxs-lookup"><span data-stu-id="73fd4-1722">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73fd4-1723">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73fd4-1723">Az.Network</span></span>
* <span data-ttu-id="73fd4-1724">Ändra alla cmdletar för PrivateEndpointConnection så att de stöder generiska tjänstleverantörer.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1724">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="73fd4-1725">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="73fd4-1725">Updated cmdlet:</span></span>
        - <span data-ttu-id="73fd4-1726">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="73fd4-1726">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="73fd4-1727">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="73fd4-1727">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="73fd4-1728">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="73fd4-1728">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="73fd4-1729">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="73fd4-1729">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="73fd4-1730">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="73fd4-1730">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="73fd4-1731">Lägg till ny cmdlet för PrivateLinkResource så att det också stöder generiska tjänstleverantörer.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1731">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="73fd4-1732">Ny cmdlet:</span><span class="sxs-lookup"><span data-stu-id="73fd4-1732">New cmdlet:</span></span>
        - <span data-ttu-id="73fd4-1733">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="73fd4-1733">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="73fd4-1734">Lägg till nya fält och parametrar för funktionen Proxy Protocol V2.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1734">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="73fd4-1735">Lägg till egenskapen EnableProxyProtocol i PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="73fd4-1735">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="73fd4-1736">Lägg till egenskapen LinkIdentifier i PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="73fd4-1736">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="73fd4-1737">Uppdaterade New-AzPrivateLinkService för att lägga till den nya valfria parametern EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1737">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="73fd4-1738">Korrigera felaktig beskrivning av parameter i referensdokumentationen för New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="73fd4-1738">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="73fd4-1739">Nya cmdletar som stöder Azure-brandväggsprincipen</span><span class="sxs-lookup"><span data-stu-id="73fd4-1739">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="73fd4-1740">Lägg till stöd för den underordnade resursen RouteTables för VirtualHub</span><span class="sxs-lookup"><span data-stu-id="73fd4-1740">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="73fd4-1741">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="73fd4-1741">New cmdlets added:</span></span>
        - <span data-ttu-id="73fd4-1742">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="73fd4-1742">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="73fd4-1743">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="73fd4-1743">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="73fd4-1744">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="73fd4-1744">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="73fd4-1745">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="73fd4-1745">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="73fd4-1746">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="73fd4-1746">Set-AzVirtualHub</span></span>
* <span data-ttu-id="73fd4-1747">Lägg till stöd för ny egenskaps-SKU för VirtualHub och VirtualWANType för VirtualWan</span><span class="sxs-lookup"><span data-stu-id="73fd4-1747">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="73fd4-1748">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="73fd4-1748">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="73fd4-1749">New-AzVirtualHub: lade till parameter-SKU</span><span class="sxs-lookup"><span data-stu-id="73fd4-1749">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="73fd4-1750">Update-AzVirtualHub: lade till parameter-SKU</span><span class="sxs-lookup"><span data-stu-id="73fd4-1750">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="73fd4-1751">New-AzVirtualWan: lade till parametern VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="73fd4-1751">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="73fd4-1752">Update-AzVirtualWan: lade till parametern VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="73fd4-1752">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="73fd4-1753">Lägg till stöd för egenskapen EnableInternetSecurity för HubVnetConnection, VpnConnection och ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="73fd4-1753">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="73fd4-1754">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="73fd4-1754">New cmdlets added:</span></span>
        - <span data-ttu-id="73fd4-1755">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="73fd4-1755">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="73fd4-1756">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="73fd4-1756">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="73fd4-1757">New-AzureRmVirtualHubVnetConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-1757">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="73fd4-1758">New-AzureRmVpnConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-1758">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="73fd4-1759">Update-AzureRmVpnConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-1759">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="73fd4-1760">New-AzureRmExpressRouteConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-1760">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="73fd4-1761">Set-AzureRmExpressRouteConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-1761">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="73fd4-1762">Lägg till stöd för att konfigurera TopLevel WebApplicationFirewall-princip</span><span class="sxs-lookup"><span data-stu-id="73fd4-1762">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="73fd4-1763">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="73fd4-1763">New cmdlets added:</span></span>
        - <span data-ttu-id="73fd4-1764">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="73fd4-1764">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="73fd4-1765">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="73fd4-1765">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="73fd4-1766">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="73fd4-1766">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="73fd4-1767">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="73fd4-1767">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="73fd4-1768">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="73fd4-1768">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="73fd4-1769">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="73fd4-1769">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="73fd4-1770">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="73fd4-1770">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="73fd4-1771">New-AzApplicationGatewayFirewallPolicy: parametrarna PolicySetting, ManagedRule har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-1771">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="73fd4-1772">Stöd för operator för geomatchning har lagts till på CustomRule</span><span class="sxs-lookup"><span data-stu-id="73fd4-1772">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="73fd4-1773">Geomatchning har lagts till i operatorn på FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="73fd4-1773">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="73fd4-1774">Stöd har lagts till för brandväggsprinciperna perListener och perSite</span><span class="sxs-lookup"><span data-stu-id="73fd4-1774">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="73fd4-1775">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="73fd4-1775">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="73fd4-1776">New-AzApplicationGatewayHttpListener: parametrarna FirewallPolicy, FirewallPolicyId har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-1776">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="73fd4-1777">New-AzApplicationGatewayPathRuleConfig: parametrarna FirewallPolicy, FirewallPolicyId har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-1777">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="73fd4-1778">Åtgärdat så att nödvändigt undernät med namnet AzureBastionSubnet i PSBastion kan vara skiftlägesokänsligt</span><span class="sxs-lookup"><span data-stu-id="73fd4-1778">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="73fd4-1779">Stöd för mål-FQDN:er i nätverksregler och översatt FQDN i NAT-regler för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="73fd4-1779">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="73fd4-1780">Lägg till stöd för resursen RouteTables för IpGroup på den högsta nivån</span><span class="sxs-lookup"><span data-stu-id="73fd4-1780">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="73fd4-1781">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="73fd4-1781">New cmdlets added:</span></span>
        - <span data-ttu-id="73fd4-1782">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="73fd4-1782">New-AzIpGroup</span></span>
        - <span data-ttu-id="73fd4-1783">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="73fd4-1783">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="73fd4-1784">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="73fd4-1784">Get-AzIpGroup</span></span>
        - <span data-ttu-id="73fd4-1785">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="73fd4-1785">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="73fd4-1786">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="73fd4-1786">Az.ServiceFabric</span></span>
* <span data-ttu-id="73fd4-1787">Ta bort cmdleten Add-AzServiceFabricApplicationCertificate eftersom det här scenariot omfattas av Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1787">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="73fd4-1788">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73fd4-1788">Az.Sql</span></span>
* <span data-ttu-id="73fd4-1789">Stöd har lagts till för återställning av utelämnade databaser på hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1789">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="73fd4-1790">Inaktuella gamla cmdletar för granskning från kod.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1790">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="73fd4-1791">Tog bort inaktuella alias:</span><span class="sxs-lookup"><span data-stu-id="73fd4-1791">Removed deprecated aliases:</span></span>
* <span data-ttu-id="73fd4-1792">Get-AzSqlDatabaseIndexRecommendations (använd Get-AzSqlDatabaseIndexRecommendation istället)</span><span class="sxs-lookup"><span data-stu-id="73fd4-1792">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="73fd4-1793">Get-AzSqlDatabaseRestorePoints (använd Get-AzSqlDatabaseRestorePoint istället)</span><span class="sxs-lookup"><span data-stu-id="73fd4-1793">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="73fd4-1794">Ta bort cmdleten Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="73fd4-1794">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="73fd4-1795">Ta bort alias för inaktuella cmdletar för inställningar för utvärdering av säkerhetsrisk</span><span class="sxs-lookup"><span data-stu-id="73fd4-1795">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="73fd4-1796">Inaktualisera cmdletar för inställningar för avancerad hotidentifiering</span><span class="sxs-lookup"><span data-stu-id="73fd4-1796">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="73fd4-1797">Lägga till cmdletar för att inaktivera och aktivera känslighetsrekommendationer på kolumner i en databas.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1797">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="73fd4-1798">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="73fd4-1798">Az.Storage</span></span>
* <span data-ttu-id="73fd4-1799">Stöd för att aktivera stora filresurser vid skapande eller uppdatering av lagringskonto</span><span class="sxs-lookup"><span data-stu-id="73fd4-1799">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="73fd4-1800">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="73fd4-1800">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="73fd4-1801">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="73fd4-1801">Set-AzStorageAccount</span></span>
* <span data-ttu-id="73fd4-1802">När du stänger/hämtar en filreferens kan du hoppa över kontrollen av huruvida indatasökvägen är en filkatalog eller en fil för att undvika problem med objekt som har status DeletePending</span><span class="sxs-lookup"><span data-stu-id="73fd4-1802">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="73fd4-1803">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="73fd4-1803">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="73fd4-1804">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="73fd4-1804">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="73fd4-1805">2.8.0 – oktober 2019</span><span class="sxs-lookup"><span data-stu-id="73fd4-1805">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="73fd4-1806">Allmänt</span><span class="sxs-lookup"><span data-stu-id="73fd4-1806">General</span></span>
* <span data-ttu-id="73fd4-1807">AZ. HealthcareApis 1.0.0-version</span><span class="sxs-lookup"><span data-stu-id="73fd4-1807">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="73fd4-1808">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73fd4-1808">Az.Accounts</span></span>
* <span data-ttu-id="73fd4-1809">Uppdatera telemetri och URL-omskrivning för genererade moduler, korrigera Windows-enhetstester.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1809">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="73fd4-1810">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="73fd4-1810">Az.ApiManagement</span></span>
* <span data-ttu-id="73fd4-1811">**Set-AzApiManagementApi** – Tillagt stöd för att uppdatera Api till ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="73fd4-1811">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="73fd4-1812">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="73fd4-1812">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="73fd4-1813">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="73fd4-1813">Az.Automation</span></span>
* <span data-ttu-id="73fd4-1814">Åtgärdade cmdleten New-AzureAutomationSoftwareUpdateConfiguration för parametern för inställning av Linux-omstart.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1814">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="73fd4-1815">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="73fd4-1815">Az.Batch</span></span>
* <span data-ttu-id="73fd4-1816">**Get-AzBatchNodeAgentSku** är inaktuell och ersätts av **Get-AzBatchSupportImage** i version 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1816">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73fd4-1817">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73fd4-1817">Az.Compute</span></span>
* <span data-ttu-id="73fd4-1818">Lägg till parametrarna Priority, EvictionPolicy och MaxPrice till cmdletarna New-AzVM och New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="73fd4-1818">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="73fd4-1819">Korrigera varningsmeddelande och hjälpdokument för cmdletarna Add-AzVMAdditionalUnattendContent och Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="73fd4-1819">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="73fd4-1820">Åtgärda – skipVmBackup-undantag för virtuella Linux-datorer med hanterade diskar för Set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1820">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="73fd4-1821">Åtgärda fel i uppdatera krypteringsinställningarna i set-AzVMDiskEncryptionExtension, scenario i två steg.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1821">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="73fd4-1822">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="73fd4-1822">Az.DataFactory</span></span>
* <span data-ttu-id="73fd4-1823">Lägga till CRUD-kommandon för ADF V2-dataflödet: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow och Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1823">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="73fd4-1824">Lägger till åtgärdskommandon för ADF V2-dataflödesfelsökningssession: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand och Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1824">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="73fd4-1825">Uppdatera ADF .Net SDK-versionen till 4.2.0</span><span class="sxs-lookup"><span data-stu-id="73fd4-1825">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="73fd4-1826">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="73fd4-1826">Az.DataLakeStore</span></span>
* <span data-ttu-id="73fd4-1827">Korrigera kontovalidering så att konton med ”-” kan skickas utan domän</span><span class="sxs-lookup"><span data-stu-id="73fd4-1827">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="73fd4-1828">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="73fd4-1828">Az.HealthcareApis</span></span>
* <span data-ttu-id="73fd4-1829">PowerShell-versionen har uppdaterats till 1.0.0</span><span class="sxs-lookup"><span data-stu-id="73fd4-1829">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="73fd4-1830">Uppdaterade SDK-versionen till 1.0.2</span><span class="sxs-lookup"><span data-stu-id="73fd4-1830">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="73fd4-1831">Uppdatera i tester för att referera till en ny SDK-version</span><span class="sxs-lookup"><span data-stu-id="73fd4-1831">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="73fd4-1832">Utdatastrukturen har uppdaterats från kapslad till förenklad.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1832">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="73fd4-1833">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="73fd4-1833">Az.IotHub</span></span>
* <span data-ttu-id="73fd4-1834">Lägg till ny routningskälla: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="73fd4-1834">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="73fd4-1835">Mindre felkorrigering: Get-AzIothub returnerar inte subscriptionId</span><span class="sxs-lookup"><span data-stu-id="73fd4-1835">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="73fd4-1836">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="73fd4-1836">Az.Monitor</span></span>
* <span data-ttu-id="73fd4-1837">Nya åtgärdsgruppsmottagare har lagts till för åtgärdsgrupp   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="73fd4-1837">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="73fd4-1838">Använd vanligt aviseringsschema som är aktiverat för mottagarna.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1838">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="73fd4-1839">Detta gäller inte för SMS, push för Azure-app, ITSM och röstmottagare</span><span class="sxs-lookup"><span data-stu-id="73fd4-1839">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="73fd4-1840">Webhooks har nu stöd för Azure Active Directory-autentisering.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1840">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73fd4-1841">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73fd4-1841">Az.Network</span></span>
* <span data-ttu-id="73fd4-1842">Lägg till ny cmdlet Get-AzAvailableServiceAlias som kan anropas för att hämta de alias som kan användas för tjänstslutpunktsprinciper.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1842">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="73fd4-1843">Stöd för tillägg av trafikväljare har lagts till i gatewayanslutningar för virtuella nätverk</span><span class="sxs-lookup"><span data-stu-id="73fd4-1843">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="73fd4-1844">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="73fd4-1844">New cmdlets added:</span></span>
        - <span data-ttu-id="73fd4-1845">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="73fd4-1845">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="73fd4-1846">Cmdletar har uppdaterats med valfri parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="73fd4-1846">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="73fd4-1847">Lägg till stöd för ESP- och AH-protokoll i konfiguration av nätverkssäkerhetsregler</span><span class="sxs-lookup"><span data-stu-id="73fd4-1847">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="73fd4-1848">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="73fd4-1848">Updated cmdlets:</span></span>
        - <span data-ttu-id="73fd4-1849">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="73fd4-1849">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="73fd4-1850">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="73fd4-1850">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="73fd4-1851">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="73fd4-1851">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="73fd4-1852">Förbättra hanteringen av undantag i Cortex-cmdletar</span><span class="sxs-lookup"><span data-stu-id="73fd4-1852">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="73fd4-1853">Nya generationer och SKU:er för VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="73fd4-1853">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="73fd4-1854">Introducera nya generationer för VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1854">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="73fd4-1855">Introducera nya SKU:er med högt dataflöde för VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1855">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="73fd4-1856">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="73fd4-1856">Az.RedisCache</span></span>
* <span data-ttu-id="73fd4-1857">Uppdaterad referensdokumentation för ”set-AzRedisCache” för att inkludera saknade värden för parametern ”size”</span><span class="sxs-lookup"><span data-stu-id="73fd4-1857">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="73fd4-1858">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73fd4-1858">Az.Sql</span></span>
* <span data-ttu-id="73fd4-1859">Lägg till stöd för inställningen Active Directory administratör på den hanterade instansen</span><span class="sxs-lookup"><span data-stu-id="73fd4-1859">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="73fd4-1860">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="73fd4-1860">Az.Storage</span></span>
* <span data-ttu-id="73fd4-1861">Uppdatera Lagringsklientbibliotek till 11.1.0</span><span class="sxs-lookup"><span data-stu-id="73fd4-1861">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="73fd4-1862">Lista containrar med hanteringsplans-API, kommer att listas med NextPageLink</span><span class="sxs-lookup"><span data-stu-id="73fd4-1862">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="73fd4-1863">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="73fd4-1863">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="73fd4-1864">Lista lagringskonton från prenumerationen, kommer att listas med NextPageLink</span><span class="sxs-lookup"><span data-stu-id="73fd4-1864">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="73fd4-1865">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="73fd4-1865">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="73fd4-1866">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="73fd4-1866">Az.StorageSync</span></span>
* <span data-ttu-id="73fd4-1867">Åtgärda problemet 9810 i Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1867">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="73fd4-1868">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="73fd4-1868">Az.Websites</span></span>
* <span data-ttu-id="73fd4-1869">Set-AzWebApp – uppdatering av ASP för en app misslyckades</span><span class="sxs-lookup"><span data-stu-id="73fd4-1869">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="73fd4-1870">2.7.0 – september 2019</span><span class="sxs-lookup"><span data-stu-id="73fd4-1870">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="73fd4-1871">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="73fd4-1871">Az.ApiManagement</span></span>
* <span data-ttu-id="73fd4-1872">Uppdatera ”-Format”-parameterbeskrivningen i ”Set-AzApiManagementPolicy”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="73fd4-1872">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="73fd4-1873">Referenser för den föråldrade cmdleten ”Update-AzApiManagementDeployment” har tagits bort från referensdokumentationen.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1873">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="73fd4-1874">Använd ”Set-AzApiManagement” i stället.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1874">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="73fd4-1875">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="73fd4-1875">Az.Automation</span></span>
* <span data-ttu-id="73fd4-1876">Stavfel har korrigerats i exempel i referensdokumentationen för ”Register-AzAutomationDscNode”</span><span class="sxs-lookup"><span data-stu-id="73fd4-1876">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="73fd4-1877">Klargörande har lagts till om OS-begränsningar för Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="73fd4-1877">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="73fd4-1878">Null-referensundantag har korrigerats för -Wait-alternativet i Start-AzAutomationRunbook-cmdleten.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1878">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73fd4-1879">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73fd4-1879">Az.Compute</span></span>
* <span data-ttu-id="73fd4-1880">Lägg till UploadSizeInBytes-parameter till New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="73fd4-1880">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="73fd4-1881">Lägg till Incremental-parameter till New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="73fd4-1881">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="73fd4-1882">Lägg till en funktion för virtuella datorer med låg prioritet:</span><span class="sxs-lookup"><span data-stu-id="73fd4-1882">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="73fd4-1883">MaxPrice-, EvictionPolicy- och Priority-parametrar har lagts till i New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1883">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="73fd4-1884">MaxPrice-parametern har lagts till i New-AzVmssConfig-, Update-AzVM- och Update-AzVmss-cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1884">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="73fd4-1885">Åtgärda problem med VM-referenser för Get-AzAvailabilitySet-cmdleten när alla tillgänglighetsuppsättningar i prenumerationen visas.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1885">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="73fd4-1886">Korrigera null-undantaget för Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1886">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="73fd4-1887">Korrigera VHD-metoden för sökning relativt till slut.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1887">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="73fd4-1888">Åtgärda UltraSSD-problem för New-AzVM och Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1888">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="73fd4-1889">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="73fd4-1889">Az.DataFactory</span></span>
* <span data-ttu-id="73fd4-1890">Lägger till 3 nya kommandon för ADF V2 – Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription och Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="73fd4-1890">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="73fd4-1891">ADF .Net SDK har uppdaterats till 4.1.3</span><span class="sxs-lookup"><span data-stu-id="73fd4-1891">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="73fd4-1892">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="73fd4-1892">Az.HDInsight</span></span>
* <span data-ttu-id="73fd4-1893">Anrop för icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="73fd4-1893">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="73fd4-1894">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="73fd4-1894">Az.IotHub</span></span>
* <span data-ttu-id="73fd4-1895">Lägg till stöd för att anropa redundans för en IotHub till den geo-länkade katastrofåterställningsregionen.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1895">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="73fd4-1896">Lägg till stöd för att hantera meddelandeberikning för en IotHub.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1896">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="73fd4-1897">Nya cmdlet:ar är:</span><span class="sxs-lookup"><span data-stu-id="73fd4-1897">New cmdlets are:</span></span>
    - <span data-ttu-id="73fd4-1898">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="73fd4-1898">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="73fd4-1899">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="73fd4-1899">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="73fd4-1900">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="73fd4-1900">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="73fd4-1901">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="73fd4-1901">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="73fd4-1902">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="73fd4-1902">Az.Monitor</span></span>
* <span data-ttu-id="73fd4-1903">Pekar på den senaste Monitor SDK:n, dvs. 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="73fd4-1903">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="73fd4-1904">Lägger till bakåtkompatibla ändringar i Metrics-cmdletarna, dvs. enhetsuppräkningen stöder flera nya värden.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1904">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="73fd4-1905">Detta är skrivskyddade cmdletar, så det förekommer inga ändringar i inmatningen för cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1905">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="73fd4-1906">API-versionen för **ActionGroups**-begäranden är nu **2019-06-01**. Tidigare var den **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1906">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="73fd4-1907">Test av scenarier har uppdaterats för att anpassas till den här ändringen.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1907">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="73fd4-1908">Ett nytt obligatoriskt argument har lagts till för konstruktorerna för klasserna **EmailReceiver** och **WebhookReceiver** – ett booleskt värde med namnet **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1908">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="73fd4-1909">Värdet är för närvarande fast till **false** så att den här icke-bakåtkompatibla ändringen är dold från cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1909">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="73fd4-1910">**Obs!** Det här är en tillfällig ändring som måste verifieras av Alerts-teamet.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1910">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="73fd4-1911">Ordningen på argumenten för konstruktorn för klassen **Source** (relaterad till klassen **ScheduledQueryRuleSource**) har ändrats från den tidigare SDK:n.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1911">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="73fd4-1912">Den här ändringen krävde korrigering av två enhetstest: de kompilerades, men testerna skickades inte.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1912">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="73fd4-1913">Ordningen på argumenten för konstruktorn för klassen **AlertingAction** (relaterad till klassen **ScheduledQueryRuleSource**) har ändrats från den tidigare SDK:n.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1913">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="73fd4-1914">Den här ändringen krävde korrigering av två enhetstest: de kompilerades, men testerna skickades inte.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1914">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="73fd4-1915">Stöd för kriterier för dynamiskt tröskelvärde för måttavisering v2</span><span class="sxs-lookup"><span data-stu-id="73fd4-1915">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="73fd4-1916">New-AzMetricAlertRuleV2Criteria: skapar nu även kriterier för dynamiskt tröskelvärde</span><span class="sxs-lookup"><span data-stu-id="73fd4-1916">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="73fd4-1917">Add-AzMetricAlertRuleV2: accepterar nu även kriterier för dynamiskt tröskelvärde</span><span class="sxs-lookup"><span data-stu-id="73fd4-1917">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="73fd4-1918">Förbättringar i schemalagd frågeregel (SQR)</span><span class="sxs-lookup"><span data-stu-id="73fd4-1918">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="73fd4-1919">Cmdletar accepterar ”Location”-parameter i båda formaten, antingen platsen (t.ex. eastus) eller platsens visningsnamn (t.ex. USA, östra)</span><span class="sxs-lookup"><span data-stu-id="73fd4-1919">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="73fd4-1920">”Enabled”-parametern illustreras korrekt i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="73fd4-1920">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="73fd4-1921">Exempel för den valfria parametern ”ActionGroup” har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-1921">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="73fd4-1922">Förbättrade hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="73fd4-1922">Overall improved help files</span></span>
* <span data-ttu-id="73fd4-1923">Åtgärda bugg då omfattningstypen fastställs för ”Set-AzActionRule”</span><span class="sxs-lookup"><span data-stu-id="73fd4-1923">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73fd4-1924">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73fd4-1924">Az.Network</span></span>
* <span data-ttu-id="73fd4-1925">Korrigera felaktigt exempel i referensdokumentationen för ”New-AzApplicationGateway”</span><span class="sxs-lookup"><span data-stu-id="73fd4-1925">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="73fd4-1926">Lägg till anmärkning i ”Get-AzNetworkWatcherPacketCapture”-referensdokumentationen om hämtning av alla egenskaper för en paketinsamling</span><span class="sxs-lookup"><span data-stu-id="73fd4-1926">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="73fd4-1927">Exempel har korrigerats i ”Test-AzNetworkWatcherIPFlow”-referensdokumentationen för korrekt uppräkning av nätverkskort</span><span class="sxs-lookup"><span data-stu-id="73fd4-1927">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="73fd4-1928">Förbättrad tolkning av molnundantag för att visa eventuell ytterligare information</span><span class="sxs-lookup"><span data-stu-id="73fd4-1928">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="73fd4-1929">Förbättrad tolkning av molnundantag för att hantera ytterligare en typ av SDK-undantag</span><span class="sxs-lookup"><span data-stu-id="73fd4-1929">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="73fd4-1930">Felaktig mappning av säkerhetsregelmodeller har korrigerats</span><span class="sxs-lookup"><span data-stu-id="73fd4-1930">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="73fd4-1931">Egenskaper har lagts till för nätverksgränssnittet för funktionen Privat IP</span><span class="sxs-lookup"><span data-stu-id="73fd4-1931">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="73fd4-1932">Egenskapen ”PrivateEndpoint” har lagts till som en typ av PSResourceId till PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="73fd4-1932">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="73fd4-1933">Egenskapen ”PrivateLinkConnectionProperties” har lagts till som en typ av PSIpConfigurationConnectivityInformation till PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="73fd4-1933">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="73fd4-1934">Modellklassen PSIpConfigurationConnectivityInformation har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-1934">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="73fd4-1935">ApplicationRuleProtocolType ”mssql” har lagts till för Azure Firewall-resurs</span><span class="sxs-lookup"><span data-stu-id="73fd4-1935">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="73fd4-1936">MultiLink-stöd i virtuellt WAN</span><span class="sxs-lookup"><span data-stu-id="73fd4-1936">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="73fd4-1937">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="73fd4-1937">New cmdlets</span></span>
        - <span data-ttu-id="73fd4-1938">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="73fd4-1938">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="73fd4-1939">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="73fd4-1939">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="73fd4-1940">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="73fd4-1940">Updated cmdlet:</span></span>
        - <span data-ttu-id="73fd4-1941">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="73fd4-1941">New-VpnSite</span></span>
        - <span data-ttu-id="73fd4-1942">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="73fd4-1942">Update-VpnSite</span></span>
        - <span data-ttu-id="73fd4-1943">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="73fd4-1943">New-VpnConnection</span></span>
        - <span data-ttu-id="73fd4-1944">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="73fd4-1944">Update-VpnConnection</span></span>
* <span data-ttu-id="73fd4-1945">Dokument för vissa PowerShell-exempel har korrigerats så att Az-cmdletar används i stället för AzureRM-cmdletar</span><span class="sxs-lookup"><span data-stu-id="73fd4-1945">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="73fd4-1946">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="73fd4-1946">Az.RecoveryServices</span></span>
* <span data-ttu-id="73fd4-1947">Uppdatera AzureVMpolicy-objekt med ProtectedItemsCount-attribut</span><span class="sxs-lookup"><span data-stu-id="73fd4-1947">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="73fd4-1948">Ytterligare tester har lagts till för VM-princip och återställning av ursprungligt lagringskonto</span><span class="sxs-lookup"><span data-stu-id="73fd4-1948">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="73fd4-1949">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73fd4-1949">Az.Resources</span></span>
* <span data-ttu-id="73fd4-1950">Åtgärda fel där det inte gick att anropa New-AzRoleAssignment utan parametern Scope.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1950">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="73fd4-1951">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="73fd4-1951">Az.ServiceFabric</span></span>
* <span data-ttu-id="73fd4-1952">Stavfel har korrigerats i exempel för ”Update-AzServiceFabricReliability”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="73fd4-1952">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="73fd4-1953">Lägger till nya cmdletar för att hantera program och tjänster:</span><span class="sxs-lookup"><span data-stu-id="73fd4-1953">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="73fd4-1954">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="73fd4-1954">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="73fd4-1955">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="73fd4-1955">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="73fd4-1956">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="73fd4-1956">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="73fd4-1957">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="73fd4-1957">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="73fd4-1958">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="73fd4-1958">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="73fd4-1959">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="73fd4-1959">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="73fd4-1960">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="73fd4-1960">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="73fd4-1961">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="73fd4-1961">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="73fd4-1962">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="73fd4-1962">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="73fd4-1963">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="73fd4-1963">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="73fd4-1964">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="73fd4-1964">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="73fd4-1965">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="73fd4-1965">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="73fd4-1966">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="73fd4-1966">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="73fd4-1967">Service Fabric SDK har uppgraderats till version 1.2.0 som använder Service Fabric-resursprovidern med API-version 2019-03-01.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1967">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="73fd4-1968">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="73fd4-1968">Az.SignalR</span></span>
* <span data-ttu-id="73fd4-1969">Lägg till Update-, Restart-, CheckNameAvailability- och GetUsage-cmdletar</span><span class="sxs-lookup"><span data-stu-id="73fd4-1969">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="73fd4-1970">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73fd4-1970">Az.Sql</span></span>
* <span data-ttu-id="73fd4-1971">Uppdatera exempel i referensdokumentationen för ”Get-AzSqlElasticPool”</span><span class="sxs-lookup"><span data-stu-id="73fd4-1971">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="73fd4-1972">vCore-exempel för att skapa en elastisk pool (New-AzSqlElasticPool) har lagts till.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1972">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="73fd4-1973">Ta bort verifieringen av EmailAddresses och kontrollen som bekräftar att EmailAdmins inte är falskt när EmailAddresses är tomt i Set-AzSqlServerAdvancedThreatProtectionPolicy och Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="73fd4-1973">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="73fd4-1974">Server-/databasgranskningsinställningar kan tas bort när det finns flera diagnostikinställningar som aktiverar granskningskategorin.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1974">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="73fd4-1975">Åtgärda verifiering av e-postadresser i flera Sql Vulnerability Assessment-cmdletar (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting och Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="73fd4-1975">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="73fd4-1976">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="73fd4-1976">Az.Storage</span></span>
* <span data-ttu-id="73fd4-1977">Exempel i referensdokumentationen för ”Get-AzStorageAccountKey” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="73fd4-1977">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="73fd4-1978">Vid upp- och nedladdning av en Azure-fil kan SMB-egenskaperna för källfilen (t.ex. filattribut, tidpunkten då filen skapades och tidpunkten för den senaste skrivningen) sparas i målfilen</span><span class="sxs-lookup"><span data-stu-id="73fd4-1978">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="73fd4-1979">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="73fd4-1979">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="73fd4-1980">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="73fd4-1980">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="73fd4-1981">Korrigera problem med uppladdningen av blockblob med egenskaper/metadata för ImmutabilityPolicy i containrar.</span><span class="sxs-lookup"><span data-stu-id="73fd4-1981">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="73fd4-1982">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="73fd4-1982">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="73fd4-1983">Stöd för hantering av Azure-filresurser med API för hanteringsplan</span><span class="sxs-lookup"><span data-stu-id="73fd4-1983">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="73fd4-1984">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="73fd4-1984">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="73fd4-1985">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="73fd4-1985">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="73fd4-1986">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="73fd4-1986">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="73fd4-1987">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="73fd4-1987">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="73fd4-1988">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="73fd4-1988">Az.Websites</span></span>
* <span data-ttu-id="73fd4-1989">Åtgärdar problemet där webapp-taggar togs bort när appen migrerades till nya ASP</span><span class="sxs-lookup"><span data-stu-id="73fd4-1989">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="73fd4-1990">Åtgärda Publish-AzureWebapp så att det fungerar i Linux och Windows</span><span class="sxs-lookup"><span data-stu-id="73fd4-1990">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="73fd4-1991">Uppdatera exempel i ”Get-AzWebAppPublishingProfile”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="73fd4-1991">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="73fd4-1992">2.6.0 – augusti 2019</span><span class="sxs-lookup"><span data-stu-id="73fd4-1992">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="73fd4-1993">Allmänt</span><span class="sxs-lookup"><span data-stu-id="73fd4-1993">General</span></span>
* <span data-ttu-id="73fd4-1994">Åtgärdade diverse skrivfel i flera moduler</span><span class="sxs-lookup"><span data-stu-id="73fd4-1994">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="73fd4-1995">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73fd4-1995">Az.Accounts</span></span>
* <span data-ttu-id="73fd4-1996">Stöd för användartilldelat MSI i Azure Functions-autentisering (#9479)</span><span class="sxs-lookup"><span data-stu-id="73fd4-1996">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="73fd4-1997">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="73fd4-1997">Az.Aks</span></span>
* <span data-ttu-id="73fd4-1998">Åtgärda problem med utdata för "Get-AzAks"</span><span class="sxs-lookup"><span data-stu-id="73fd4-1998">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="73fd4-1999">Mer information här: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="73fd4-1999">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="73fd4-2000">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="73fd4-2000">Az.ApiManagement</span></span>
* <span data-ttu-id="73fd4-2001">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="73fd4-2001">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="73fd4-2002">Uppdatera .net-NuGet-versionen, som inte tillämpar begränsningar för productId, apiId och userId</span><span class="sxs-lookup"><span data-stu-id="73fd4-2002">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="73fd4-2003">**Get-AzApiManagementProduct** – Lade till stöd för frågekörning mot produkter via API.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2003">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="73fd4-2004">**New-AzApiManagementApiRevision** – Korrigering för problem där ApiRevisionDescription inte angavs vid skapande av ny API-revision https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="73fd4-2004">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="73fd4-2005">Åtgärdade skrivfel i modellen "PsApiManagementOAuth2AuthrozationServer" till "PsApiManagementOAuth2AuthorizationServer"</span><span class="sxs-lookup"><span data-stu-id="73fd4-2005">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="73fd4-2006">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="73fd4-2006">Az.Batch</span></span>
* <span data-ttu-id="73fd4-2007">Åtgärdade skrivfel i hjälpmeddelande och dokumentation till att skriva Windows med versaler</span><span class="sxs-lookup"><span data-stu-id="73fd4-2007">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="73fd4-2008">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="73fd4-2008">Az.Cdn</span></span>
* <span data-ttu-id="73fd4-2009">Åtgärdade skrivfel i CDN-modulens konverteringshjälp</span><span class="sxs-lookup"><span data-stu-id="73fd4-2009">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73fd4-2010">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73fd4-2010">Az.Compute</span></span>
* <span data-ttu-id="73fd4-2011">Lägg till VmssId i New-AzVMConfig-cmdleten</span><span class="sxs-lookup"><span data-stu-id="73fd4-2011">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="73fd4-2012">Lägg till parametrarna TerminateScheduledEvents och TerminateScheduledEventNotBeforeTimeoutInMinutes i New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="73fd4-2012">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="73fd4-2013">Lägg till egenskapen HyperVGeneration till avbildningsobjekt för virtuell dator</span><span class="sxs-lookup"><span data-stu-id="73fd4-2013">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="73fd4-2014">Lägg till funktioner för Host och HostGroup</span><span class="sxs-lookup"><span data-stu-id="73fd4-2014">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="73fd4-2015">Nya cmdletar:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="73fd4-2015">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="73fd4-2016">HostId-parametern läggs till i New-AzVMConfig och New-AzVM</span><span class="sxs-lookup"><span data-stu-id="73fd4-2016">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="73fd4-2017">Uppdatera exempel i "Invoke-AzVMRunCommand"-dokumentationen till att använda rätt parameternamn</span><span class="sxs-lookup"><span data-stu-id="73fd4-2017">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="73fd4-2018">Uppdatera "-VolumeType"-beskrivningen i referensdokumentationen för "set-AzVMDiskEncryptionExtension" och "set-AzVmssDiskEncryptionExtension"</span><span class="sxs-lookup"><span data-stu-id="73fd4-2018">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="73fd4-2019">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="73fd4-2019">Az.DataFactory</span></span>
* <span data-ttu-id="73fd4-2020">Åtgärda skrivfel till att använda versaler för "Windows" i "New-AzDataFactoryEncryptValue"-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="73fd4-2020">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="73fd4-2021">Uppdaterade ADF .Net SDK-versionen till 4.1.2</span><span class="sxs-lookup"><span data-stu-id="73fd4-2021">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="73fd4-2022">Lägg till parametrarna "DataProxyIntegrationRuntimeName", "DataProxyStagingLinkedServiceName" och "DataProxyStagingPath" för "Set-AzureRmDataFactoryV2IntegrationRuntime"-cmd för att aktivera konfiguration av lokalt installerad integrationskörning som en proxy för SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="73fd4-2022">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="73fd4-2023">Uppdaterade PSTriggerRun till att visa utlöst pipeline, meddelande och egenskaper samt PSActivityRun till att visa aktivitetstypen</span><span class="sxs-lookup"><span data-stu-id="73fd4-2023">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="73fd4-2024">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="73fd4-2024">Az.DataLakeStore</span></span>
* <span data-ttu-id="73fd4-2025">Korrigering av frysning av Get-DataLakeStoreDeletedItem för fel eller fjärrundantag.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2025">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="73fd4-2026">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="73fd4-2026">Az.EventHub</span></span>
* <span data-ttu-id="73fd4-2027">Korrigering av problem #9658 : Skrivfel i parametern VirtualNteworkRule i Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="73fd4-2027">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="73fd4-2028">Korrigering av problem #9558 : Set-AzEventHubNamespace använder PATCH i stället för PUT</span><span class="sxs-lookup"><span data-stu-id="73fd4-2028">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="73fd4-2029">lade till parametern EnableKafka i Set-AzEventHubNamespace-cmdleten</span><span class="sxs-lookup"><span data-stu-id="73fd4-2029">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="73fd4-2030">Korrigering av problem #9786 : kan inte skapa en regel med Endast lyssna-behörighet</span><span class="sxs-lookup"><span data-stu-id="73fd4-2030">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="73fd4-2031">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="73fd4-2031">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="73fd4-2032">Åtgärdade skrivfel i dokumentation där "Azure" skrevs helt med gemener</span><span class="sxs-lookup"><span data-stu-id="73fd4-2032">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="73fd4-2033">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="73fd4-2033">Az.Monitor</span></span>
* <span data-ttu-id="73fd4-2034">Åtgärdade felaktigt parameternamn i hjälpdokumentationen</span><span class="sxs-lookup"><span data-stu-id="73fd4-2034">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73fd4-2035">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73fd4-2035">Az.Network</span></span>
* <span data-ttu-id="73fd4-2036">Uppdaterade New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="73fd4-2036">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="73fd4-2037">Gjorde parametern "PublicIpAddress" inaktuell eftersom den aldrig används på serversidan.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2037">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="73fd4-2038">Lade till den valfria parametern "Primary", som anger huruvida den aktuella IP-konfigurationen är den primära.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2038">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="73fd4-2039">Förbättrade hanteringen av felundantag för begärande från SDK – åtgärdar problemet att tidigare SDK-undantag inte hanteras på rätt sätt, vilket leder till att viktig felinformation inte visas</span><span class="sxs-lookup"><span data-stu-id="73fd4-2039">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="73fd4-2040">Justerade valideringslogiken för IPv6-IP-prefix till att kontrollera korrekt IPv6-prefixlängd.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2040">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="73fd4-2041">Uppdaterade Get-AzVirtualNetworkSubnetConfig: Lade till parameter som anges till get av undernätets resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2041">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="73fd4-2042">Uppdaterade beskrivningen av parametern Location för AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="73fd4-2042">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="73fd4-2043">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="73fd4-2043">Az.OperationalInsights</span></span>
* <span data-ttu-id="73fd4-2044">Uppdaterade dokumentation för "New-AzOperationalInsightsLinuxSyslogDataSource"</span><span class="sxs-lookup"><span data-stu-id="73fd4-2044">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="73fd4-2045">Lade till exempel</span><span class="sxs-lookup"><span data-stu-id="73fd4-2045">Added example</span></span>
    - <span data-ttu-id="73fd4-2046">Uppdaterade beskrivningen av parametern "-Name"</span><span class="sxs-lookup"><span data-stu-id="73fd4-2046">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="73fd4-2047">Lade till ett exempel för New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="73fd4-2047">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="73fd4-2048">Ändrade beskrivningen av parametern -Name för New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="73fd4-2048">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="73fd4-2049">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="73fd4-2049">Az.RecoveryServices</span></span>
* <span data-ttu-id="73fd4-2050">Uppdatera "Get-AzRecoveryServicesBackupJobDetail.md"</span><span class="sxs-lookup"><span data-stu-id="73fd4-2050">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="73fd4-2051">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73fd4-2051">Az.Resources</span></span>
* <span data-ttu-id="73fd4-2052">Lägg till stöd för den nya API-versionen från 2019-05-10 för Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="73fd4-2052">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="73fd4-2053">Lägg till stöd för "copy.count = 0" för variabler, resurser och egenskaper</span><span class="sxs-lookup"><span data-stu-id="73fd4-2053">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="73fd4-2054">Resurser med "condition = false" eller "copy.count = 0" tas bort i complete-läget</span><span class="sxs-lookup"><span data-stu-id="73fd4-2054">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="73fd4-2055">Lägg till ett exempel på tilldelning av princip på prenumerationsnivå i hjälpdokumentationen</span><span class="sxs-lookup"><span data-stu-id="73fd4-2055">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="73fd4-2056">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="73fd4-2056">Az.ServiceBus</span></span>
* <span data-ttu-id="73fd4-2057">Korrigering av problem #9658 : Skrivfel i parametern VirtualNetworkRule i set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="73fd4-2057">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="73fd4-2058">Korrigering av problem #9786 : kan inte skapa en regel med Endast lyssna-behörighet</span><span class="sxs-lookup"><span data-stu-id="73fd4-2058">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="73fd4-2059">Lade till det nya kommandot "Test-AzServiceBusNameAvailability" för att kontrollera namntillgängligheten för kö och ämne</span><span class="sxs-lookup"><span data-stu-id="73fd4-2059">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="73fd4-2060">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="73fd4-2060">Az.ServiceFabric</span></span>
* <span data-ttu-id="73fd4-2061">Åtgärda buggar med tillägg av nodtyps-cmdlet:</span><span class="sxs-lookup"><span data-stu-id="73fd4-2061">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="73fd4-2062">NullReferenceException-bugg när resursgrupp hade annan vmss som inte är relaterad till Service Fabric-klustret.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2062">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="73fd4-2063">Åtgärdar problemet: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="73fd4-2063">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="73fd4-2064">Åtgärda bugg där cmdleten misslyckades om virtualNetwork var i en annan resursgrupp än klustret.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2064">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="73fd4-2065">Åtgärdar problemet: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="73fd4-2065">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="73fd4-2066">AzServiceFabricApplicationCertificate-cmdleten görs inaktuell</span><span class="sxs-lookup"><span data-stu-id="73fd4-2066">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="73fd4-2067">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73fd4-2067">Az.Sql</span></span>
* <span data-ttu-id="73fd4-2068">Uppdatera dokumentation om gamla gransknings-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2068">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="73fd4-2069">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="73fd4-2069">Az.Storage</span></span>
* <span data-ttu-id="73fd4-2070">Uppdatera hjälpen för Get/Close-AzStorageFileHandle genom att lägga till fler scenarier i cmdlet-exempel och uppdatera parameterbeskrivningar</span><span class="sxs-lookup"><span data-stu-id="73fd4-2070">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="73fd4-2071">Stöd för StandardBlobTier i uppladdningsblob och kopieringsblob</span><span class="sxs-lookup"><span data-stu-id="73fd4-2071">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="73fd4-2072">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="73fd4-2072">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="73fd4-2073">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="73fd4-2073">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="73fd4-2074">Stöd för rehydratiseringsprioritet i kopieringsblob</span><span class="sxs-lookup"><span data-stu-id="73fd4-2074">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="73fd4-2075">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="73fd4-2075">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="73fd4-2076">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="73fd4-2076">Az.Websites</span></span>
* <span data-ttu-id="73fd4-2077">Lägg till klargöranden gällande parametern -AppSettings i Set-AzWebApp och Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="73fd4-2077">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="73fd4-2078">2.5.0 – July 2019</span><span class="sxs-lookup"><span data-stu-id="73fd4-2078">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="73fd4-2079">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73fd4-2079">Az.Accounts</span></span>
* <span data-ttu-id="73fd4-2080">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="73fd4-2080">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="73fd4-2081">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="73fd4-2081">Az.ApplicationInsights</span></span>
* <span data-ttu-id="73fd4-2082">Korrigera skrivfel i exempel i dokumentationen för Remove-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="73fd4-2082">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="73fd4-2083">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="73fd4-2083">Az.Automation</span></span>
* <span data-ttu-id="73fd4-2084">Korrigera skrivfel i resurssträng</span><span class="sxs-lookup"><span data-stu-id="73fd4-2084">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="73fd4-2085">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="73fd4-2085">Az.CognitiveServices</span></span>
* <span data-ttu-id="73fd4-2086">Stöd för NetworkRuleSet har lagts till.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2086">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73fd4-2087">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73fd4-2087">Az.Compute</span></span>
* <span data-ttu-id="73fd4-2088">Lägg till saknade egenskaper (ComputerName, OsName, OsVersion och HyperVGeneration) för visningsobjekt i den virtuella datorinstansen.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2088">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="73fd4-2089">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="73fd4-2089">Az.ContainerRegistry</span></span>
* <span data-ttu-id="73fd4-2090">Åtgärda skrivfel i Remove-AzContainerRegistryReplication för parametern Replication</span><span class="sxs-lookup"><span data-stu-id="73fd4-2090">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="73fd4-2091">Mer information finns här: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="73fd4-2091">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="73fd4-2092">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="73fd4-2092">Az.DataFactory</span></span>
* <span data-ttu-id="73fd4-2093">ADF .Net SDK-versionen har uppdaterats till 4.1.0</span><span class="sxs-lookup"><span data-stu-id="73fd4-2093">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="73fd4-2094">Korrigera skrivfel i dokumentationen för Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="73fd4-2094">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="73fd4-2095">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="73fd4-2095">Az.EventHub</span></span>
* <span data-ttu-id="73fd4-2096">Ny cmmdlet har lagts till för att skapa SAS-token: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="73fd4-2096">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="73fd4-2097">verifierings- och felmeddelande har lagts till för authorizationrules-rättigheter om endast "hantera" har tilldelats</span><span class="sxs-lookup"><span data-stu-id="73fd4-2097">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="73fd4-2098">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="73fd4-2098">Az.KeyVault</span></span>
* <span data-ttu-id="73fd4-2099">Stöd har lagts till för att ange KeySize för certifikatprinciper</span><span class="sxs-lookup"><span data-stu-id="73fd4-2099">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="73fd4-2100">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="73fd4-2100">Az.LogicApp</span></span>
* <span data-ttu-id="73fd4-2101">Korrigering för Get-AzIntegrationAccountMap för att lista alla mappningstyper</span><span class="sxs-lookup"><span data-stu-id="73fd4-2101">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="73fd4-2102">Ny MapType-parameter har lagts till för filtrering</span><span class="sxs-lookup"><span data-stu-id="73fd4-2102">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="73fd4-2103">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="73fd4-2103">Az.ManagedServices</span></span>
* <span data-ttu-id="73fd4-2104">Stöd för API-versionen 2019-06-01 (GA) har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-2104">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73fd4-2105">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73fd4-2105">Az.Network</span></span>
* <span data-ttu-id="73fd4-2106">Lägg till stöd för privat slutpunkt och privat länktjänst</span><span class="sxs-lookup"><span data-stu-id="73fd4-2106">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="73fd4-2107">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="73fd4-2107">New cmdlets</span></span>
        - <span data-ttu-id="73fd4-2108">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="73fd4-2108">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="73fd4-2109">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="73fd4-2109">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="73fd4-2110">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="73fd4-2110">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="73fd4-2111">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="73fd4-2111">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="73fd4-2112">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="73fd4-2112">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="73fd4-2113">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="73fd4-2113">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="73fd4-2114">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="73fd4-2114">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="73fd4-2115">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="73fd4-2115">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="73fd4-2116">Nedanstående kommandon för funktionen har uppdaterats: Flaggan PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies på undernätet i VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="73fd4-2116">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="73fd4-2117">Uppdaterade New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="73fd4-2117">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="73fd4-2118">Valfri parameter har lagts till – PrivateEndpointNetworkPoliciesFlag som konfigurerar huruvida nätverksprinciper ska tillämpas på en privat slutpunkt i det här undernätet.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2118">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="73fd4-2119">Valfri parameter har lagts till – PrivateLinkServiceNetworkPoliciesFlag som konfigurerar huruvida nätverksprinciper ska tillämpas på en privat länktjänst i det här undernätet.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2119">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="73fd4-2120">AzPrivateLinkService för cmdlet-parametern ServiceName har bytt namn till Name med aliaset ServiceName för bakåtkompatibilitet</span><span class="sxs-lookup"><span data-stu-id="73fd4-2120">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="73fd4-2121">Aktivera ICMP-protokoll för konfiguration av nätverkssäkerhetsregler</span><span class="sxs-lookup"><span data-stu-id="73fd4-2121">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="73fd4-2122">Uppdaterade cmdletar</span><span class="sxs-lookup"><span data-stu-id="73fd4-2122">Updated cmdlets</span></span>
        - <span data-ttu-id="73fd4-2123">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="73fd4-2123">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="73fd4-2124">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="73fd4-2124">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="73fd4-2125">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="73fd4-2125">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="73fd4-2126">Lägg till ConnectionProtocolType (Ikev1/Ikev2) som en konfigurerbar parameter för New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="73fd4-2126">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="73fd4-2127">Lägg till PrivateIpAddressVersion i LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="73fd4-2127">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="73fd4-2128">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="73fd4-2128">Updated cmdlet:</span></span>
        - <span data-ttu-id="73fd4-2129">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="73fd4-2129">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="73fd4-2130">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="73fd4-2130">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="73fd4-2131">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="73fd4-2131">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="73fd4-2132">Uppdatering av Application Gateway-kommandot New-AzApplicationGatewayProbeConfig för stöd av anpassad port i Probe</span><span class="sxs-lookup"><span data-stu-id="73fd4-2132">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="73fd4-2133">Uppdaterade New-AzApplicationGatewayProbeConfig: Den valfria parametern Port som används för avsökning i serverdelen har lagts till.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2133">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="73fd4-2134">Denna parameter gäller för SKU:erna Standard_V2 och WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2134">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="73fd4-2135">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="73fd4-2135">Az.OperationalInsights</span></span>
* <span data-ttu-id="73fd4-2136">Uppdaterade standardversionen för sparade sökningar till 1.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2136">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="73fd4-2137">Åtgärdade hantering av anpassad log null regex</span><span class="sxs-lookup"><span data-stu-id="73fd4-2137">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="73fd4-2138">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="73fd4-2138">Az.RecoveryServices</span></span>
* <span data-ttu-id="73fd4-2139">Uppdatera Get-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="73fd4-2139">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="73fd4-2140">Uppdatera Get-AzRecoveryServicesBackupContainer.md</span><span class="sxs-lookup"><span data-stu-id="73fd4-2140">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="73fd4-2141">Uppdatera Get-AzRecoveryServicesVault.md</span><span class="sxs-lookup"><span data-stu-id="73fd4-2141">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="73fd4-2142">Uppdatera Wait-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="73fd4-2142">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="73fd4-2143">Uppdatera Set-AzRecoveryServicesVaultContext.md</span><span class="sxs-lookup"><span data-stu-id="73fd4-2143">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="73fd4-2144">Uppdatera Get-AzRecoveryServicesBackupItem.md</span><span class="sxs-lookup"><span data-stu-id="73fd4-2144">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="73fd4-2145">Uppdatera Get-AzRecoveryServicesBackupRecoveryPoint.md</span><span class="sxs-lookup"><span data-stu-id="73fd4-2145">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="73fd4-2146">Uppdatera Restore-AzRecoveryServicesBackupItem.md</span><span class="sxs-lookup"><span data-stu-id="73fd4-2146">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="73fd4-2147">Uppdaterat tjänstanrop för avregistrering av container för Azure-filresurs</span><span class="sxs-lookup"><span data-stu-id="73fd4-2147">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="73fd4-2148">Uppdatera Set-AzRecoveryServicesAsrAlertSetting.md</span><span class="sxs-lookup"><span data-stu-id="73fd4-2148">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="73fd4-2149">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73fd4-2149">Az.Resources</span></span>
- <span data-ttu-id="73fd4-2150">Ta bort den cmdlet som saknas och som refereras i dokumentationen till New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="73fd4-2150">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="73fd4-2151">Princip-cmdletar har uppdaterats så att de använder den nya API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="73fd4-2151">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="73fd4-2152">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="73fd4-2152">Az.ServiceBus</span></span>
* <span data-ttu-id="73fd4-2153">Ny cmmdlet har lagts till för att skapa SAS-token: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="73fd4-2153">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="73fd4-2154">verifierings- och felmeddelande har lagts till för authorizationrules-rättigheter om endast "hantera" har tilldelats</span><span class="sxs-lookup"><span data-stu-id="73fd4-2154">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="73fd4-2155">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73fd4-2155">Az.Sql</span></span>
* <span data-ttu-id="73fd4-2156">Åtgärda saknade exempel för Set-AzSqlDatabaseSecondary cmdlet</span><span class="sxs-lookup"><span data-stu-id="73fd4-2156">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="73fd4-2157">Åtgärda angivna återkommande genomsökningar för bedömning av säkerhetsrisk utan angivna e-postadresser</span><span class="sxs-lookup"><span data-stu-id="73fd4-2157">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="73fd4-2158">Korrigera ett skrivfel i ett varningsmeddelande.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2158">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="73fd4-2159">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="73fd4-2159">Az.Storage</span></span>
* <span data-ttu-id="73fd4-2160">Uppdatera exempel i referensdokumentationen för Get-AzStorageAccount så att rätt parameternamn används</span><span class="sxs-lookup"><span data-stu-id="73fd4-2160">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="73fd4-2161">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="73fd4-2161">Az.StorageSync</span></span>
* <span data-ttu-id="73fd4-2162">Lägger till cmdleten Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2162">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="73fd4-2163">Åtgärda problem 9551 så att TierFilesOlderThanDays föredras</span><span class="sxs-lookup"><span data-stu-id="73fd4-2163">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="73fd4-2164">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="73fd4-2164">Az.Websites</span></span>
* <span data-ttu-id="73fd4-2165">Åtgärdar ett fel där vissa SiteConfig-egenskaper inte returnerades av Get-AzWebApp och Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="73fd4-2165">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="73fd4-2166">Lägger till en ny platsparameter för Get-AzDeletedWebApp och Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="73fd4-2166">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="73fd4-2167">Åtgärdar ett fel i kloning av webbapp-platser som använder New-AzWebApp-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="73fd4-2167">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="73fd4-2168">2.4.0 – juli 2019</span><span class="sxs-lookup"><span data-stu-id="73fd4-2168">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="73fd4-2169">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73fd4-2169">Az.Accounts</span></span>
* <span data-ttu-id="73fd4-2170">Lägg till stöd för profil-cmdletar</span><span class="sxs-lookup"><span data-stu-id="73fd4-2170">Add support for profile cmdlets</span></span>
* <span data-ttu-id="73fd4-2171">Lägg till stöd för miljöer och dataplaner i genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="73fd4-2171">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="73fd4-2172">Åtgärda bugg där fel slutpunkt i vissa fall användes för cmdletar för dataplaner i Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="73fd4-2172">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="73fd4-2173">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="73fd4-2173">Az.Advisor</span></span>
* <span data-ttu-id="73fd4-2174">GA-version av Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="73fd4-2174">GA release of Az.Advisor</span></span>
* <span data-ttu-id="73fd4-2175">Den här modulen ingår nu som en del av `Az`-sammanslagningsmodulen</span><span class="sxs-lookup"><span data-stu-id="73fd4-2175">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="73fd4-2176">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="73fd4-2176">Az.ApiManagement</span></span>
* <span data-ttu-id="73fd4-2177">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="73fd4-2177">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="73fd4-2178">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="73fd4-2178">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="73fd4-2179">Stöd för att fråga prenumerationer efter användare och produkt har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-2179">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="73fd4-2180">Stöd för att fråga med hjälp av omfång ”/”, ”/apis”, ”/apis/echo-api” har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-2180">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="73fd4-2181">Korrigering av problem https://github.com/Azure/azure-powershell/issues/9307 och https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="73fd4-2181">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="73fd4-2182">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="73fd4-2182">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="73fd4-2183">Stöd för att ange ”ApiVersion” och ”ApiVersionSetId” när API:er importeras har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-2183">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="73fd4-2184">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="73fd4-2184">Az.Automation</span></span>
* <span data-ttu-id="73fd4-2185">Bugg med cmdleten Set-AzAutomationConnectionFieldValue för att hantera strängvärde har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2185">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73fd4-2186">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73fd4-2186">Az.Compute</span></span>
* <span data-ttu-id="73fd4-2187">Lägg till parametern HyperVGeneration i New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="73fd4-2187">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="73fd4-2188">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="73fd4-2188">Az.DataFactory</span></span>
* <span data-ttu-id="73fd4-2189">Uppdaterar utdata från ADF-cmdletar som hämtar aktivitetskörningar, hämtar pipelinekörningar och hämtar utlösarkörningar för stöd för Select-Object-pipe.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2189">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="73fd4-2190">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="73fd4-2190">Az.EventGrid</span></span>
* <span data-ttu-id="73fd4-2191">Korrigera stavfel i dokumentation om ”New-AzEventGridSubscription”</span><span class="sxs-lookup"><span data-stu-id="73fd4-2191">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="73fd4-2192">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="73fd4-2192">Az.IotHub</span></span>
* <span data-ttu-id="73fd4-2193">Lägg till stöd för att återskapa principnycklar för auktorisering.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2193">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73fd4-2194">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73fd4-2194">Az.Network</span></span>
* <span data-ttu-id="73fd4-2195">”RoutingPreference” har lagts till i offentliga IP-taggar</span><span class="sxs-lookup"><span data-stu-id="73fd4-2195">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="73fd4-2196">Förbättra exempel för referensdokumentation om ”Get-AzNetworkServiceTag”</span><span class="sxs-lookup"><span data-stu-id="73fd4-2196">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="73fd4-2197">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="73fd4-2197">Az.PolicyInsights</span></span>
* <span data-ttu-id="73fd4-2198">Åtgärda problem med null-referens i Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="73fd4-2198">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="73fd4-2199">Mer information här: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="73fd4-2199">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="73fd4-2200">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="73fd4-2200">Az.OperationalInsights</span></span>
* <span data-ttu-id="73fd4-2201">Modellen för CustomLog-datakälla som returneras i Get-AzOperationalInsightsDataSource har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="73fd4-2201">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="73fd4-2202">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="73fd4-2202">Az.RecoveryServices</span></span>
* <span data-ttu-id="73fd4-2203">Kommandot get-policy för IaaSVM:er har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="73fd4-2203">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="73fd4-2204">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73fd4-2204">Az.Resources</span></span>
    - <span data-ttu-id="73fd4-2205">Korrigera hjälptext för den översta parametern i Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="73fd4-2205">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="73fd4-2206">Lägg till växlingsstöd på klientsidan för Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="73fd4-2206">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="73fd4-2207">Lägg till nya parametrar för Set-AzPolicyAssignment, -PolicyParameters och -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="73fd4-2207">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="73fd4-2208">En mängd dokument- och exempeluppdateringar för Policy-cmdletar</span><span class="sxs-lookup"><span data-stu-id="73fd4-2208">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="73fd4-2209">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="73fd4-2209">Az.ServiceBus</span></span>
* <span data-ttu-id="73fd4-2210">Korrigering av problem #4938 – New-AzureRmServiceBusQueue returnerar BadRequest vid konfiguration av MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="73fd4-2210">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="73fd4-2211">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73fd4-2211">Az.Sql</span></span>
* <span data-ttu-id="73fd4-2212">Lägg till cmdletar för instansredundansgrupper från förhandsversion till offentlig version</span><span class="sxs-lookup"><span data-stu-id="73fd4-2212">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="73fd4-2213">Stöd för granskning för Azure SQL Server\Database med nya cmdletar.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2213">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="73fd4-2214">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="73fd4-2214">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="73fd4-2215">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="73fd4-2215">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="73fd4-2216">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="73fd4-2216">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="73fd4-2217">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="73fd4-2217">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="73fd4-2218">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="73fd4-2218">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="73fd4-2219">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="73fd4-2219">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="73fd4-2220">Ta bort begränsningar för e-post från inställningarna för sårbarhetsbedömning</span><span class="sxs-lookup"><span data-stu-id="73fd4-2220">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="73fd4-2221">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="73fd4-2221">Az.Storage</span></span>
* <span data-ttu-id="73fd4-2222">Ändra två parametrar ”-IndexDocument” och ”-ErrorDocument404Path” från ”krävs” till ”valfri” i cmdlet:</span><span class="sxs-lookup"><span data-stu-id="73fd4-2222">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="73fd4-2223">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="73fd4-2223">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="73fd4-2224">Uppdatera hjälpen för Get-AzStorageBlobContent genom att lägga till ett exempel</span><span class="sxs-lookup"><span data-stu-id="73fd4-2224">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="73fd4-2225">Visa mer felinformation när cmdleten misslyckas med StorageException</span><span class="sxs-lookup"><span data-stu-id="73fd4-2225">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="73fd4-2226">Stöd för att skapa eller uppdatera lagringskonto med Azure Files AAD DS-autentisering</span><span class="sxs-lookup"><span data-stu-id="73fd4-2226">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="73fd4-2227">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="73fd4-2227">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="73fd4-2228">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="73fd4-2228">Set-AzStorageAccount</span></span>
* <span data-ttu-id="73fd4-2229">Stöd för att lista eller stänga filreferenser för en filresurs, filkatalog eller en fil</span><span class="sxs-lookup"><span data-stu-id="73fd4-2229">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="73fd4-2230">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="73fd4-2230">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="73fd4-2231">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="73fd4-2231">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="73fd4-2232">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="73fd4-2232">Az.StorageSync</span></span>
* <span data-ttu-id="73fd4-2233">Den här modulen ingår nu som en del av `Az`-sammanslagningsmodulen</span><span class="sxs-lookup"><span data-stu-id="73fd4-2233">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="73fd4-2234">2.3.2 – juni 2019</span><span class="sxs-lookup"><span data-stu-id="73fd4-2234">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="73fd4-2235">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73fd4-2235">Az.Accounts</span></span>
* <span data-ttu-id="73fd4-2236">Åtgärda bugg med felaktiga webbadresser som i vissa fall användes för Functions-anrop</span><span class="sxs-lookup"><span data-stu-id="73fd4-2236">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="73fd4-2237">Mer information här: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="73fd4-2237">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="73fd4-2238">Åtgärda problem med alias från AzureRM i Az-cmdletar</span><span class="sxs-lookup"><span data-stu-id="73fd4-2238">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="73fd4-2239">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="73fd4-2239">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="73fd4-2240">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="73fd4-2240">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73fd4-2241">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73fd4-2241">Az.Compute</span></span>
* <span data-ttu-id="73fd4-2242">Parameteruppsättningarna New-AzVm och New-AzVmss accepterar nu parametern ”ProximityPlacementGroup”.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2242">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="73fd4-2243">Stavfel i referensdokumentationen för ”New-AzVM” har korrigerats</span><span class="sxs-lookup"><span data-stu-id="73fd4-2243">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="73fd4-2244">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="73fd4-2244">Az.Dns</span></span>
* <span data-ttu-id="73fd4-2245">Stavfel i hjälpexempel för ”Set-AzDnsZone” har korrigerats.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2245">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="73fd4-2246">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="73fd4-2246">Az.EventGrid</span></span>
* <span data-ttu-id="73fd4-2247">Har uppdaterats för att använda API-versionen 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2247">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="73fd4-2248">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="73fd4-2248">New cmdlets:</span></span>
    - <span data-ttu-id="73fd4-2249">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="73fd4-2249">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="73fd4-2250">Skapar en ny Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2250">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="73fd4-2251">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="73fd4-2251">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="73fd4-2252">Hämtar information om en Event Grid-domän eller hämtar en lista med alla Event Grid-domäner i den aktuella Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2252">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="73fd4-2253">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="73fd4-2253">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="73fd4-2254">Tar bort en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2254">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="73fd4-2255">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="73fd4-2255">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="73fd4-2256">Återskapar nyckeln för delad åtkomst för en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2256">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="73fd4-2257">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="73fd4-2257">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="73fd4-2258">Hämtar de nycklar för delad åtkomst som används för att publicera händelser till en Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2258">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="73fd4-2259">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="73fd4-2259">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="73fd4-2260">Skapar ett nytt Azure Event Grid-domänämne.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2260">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="73fd4-2261">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="73fd4-2261">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="73fd4-2262">Hämtar information om ett Event Grid-domänämne eller hämtar en lista med alla Event Grid-domänämnen under en specifik Event Grid-domän i nuvarande Azure</span><span class="sxs-lookup"><span data-stu-id="73fd4-2262">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="73fd4-2263">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="73fd4-2263">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="73fd4-2264">Tar bort ett befintligt Azure Event Grid-domänämne.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2264">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="73fd4-2265">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="73fd4-2265">Updated cmdlets:</span></span>
    - <span data-ttu-id="73fd4-2266">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="73fd4-2266">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="73fd4-2267">Lägg till nya obligatoriska parametrar för att stödja piping för den nya Event Grid-domänen och Event Grid-domänämnet för att göra det möjligt att skapa nya händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2267">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="73fd4-2268">Lägg till nya obligatoriska parametrar för att ange det nya Event Grid-domännamnet och/eller namnet på Event Grid-domänämnet för att göra det möjligt att skapa nya händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2268">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="73fd4-2269">Lägg till ny parameteruppsättningar för domäner och domänämnen för att göra det möjligt att återanvända befintliga parametrar (t.ex. EndPointType, SubjectBeginsWith osv).</span><span class="sxs-lookup"><span data-stu-id="73fd4-2269">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="73fd4-2270">Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="73fd4-2270">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="73fd4-2271">Förfallodatum för händelseprenumeration</span><span class="sxs-lookup"><span data-stu-id="73fd4-2271">Event subscription expiration date,</span></span>
            - <span data-ttu-id="73fd4-2272">Avancerade filterparametrar.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2272">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="73fd4-2273">Lägg till ny uppräkning för servicebusqueue som mål.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2273">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="73fd4-2274">Tillåt inte användning av ”Alla” i alternativet -IncludedEventType och ersätt det med</span><span class="sxs-lookup"><span data-stu-id="73fd4-2274">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="73fd4-2275">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="73fd4-2275">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="73fd4-2276">Lägg till ny valfria parametrar (Top, ODataQuery och NextLink) för att stödja sidnumrering och filtrering av resultat.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2276">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="73fd4-2277">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="73fd4-2277">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="73fd4-2278">Lägg till nya obligatoriska parametrar för att stödja piping för en Event Grid-domän och Event Grid-domänämnen för att göra det möjligt att ta bort befintliga händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2278">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="73fd4-2279">Lägg till nya obligatoriska parametrar för att ange Event Grid-domännamnet och/eller namnet på Event Grid-domänämnet för att göra det möjligt att ta bort befintliga händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2279">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="73fd4-2280">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="73fd4-2280">Az.FrontDoor</span></span>
* <span data-ttu-id="73fd4-2281">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="73fd4-2281">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="73fd4-2282">Lägg till stöd för transformeringar och nytt värde för automatisk komplettering för operatorer (RegEx)</span><span class="sxs-lookup"><span data-stu-id="73fd4-2282">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="73fd4-2283">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="73fd4-2283">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="73fd4-2284">Lägg till nya värden för automatisk komplettering</span><span class="sxs-lookup"><span data-stu-id="73fd4-2284">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73fd4-2285">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73fd4-2285">Az.Network</span></span>
* <span data-ttu-id="73fd4-2286">Lägg till stöd för resurs för virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="73fd4-2286">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="73fd4-2287">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="73fd4-2287">New cmdlets</span></span>
        - <span data-ttu-id="73fd4-2288">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="73fd4-2288">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="73fd4-2289">Lägg till AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="73fd4-2289">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="73fd4-2290">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="73fd4-2290">New cmdlets</span></span>
        - <span data-ttu-id="73fd4-2291">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="73fd4-2291">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="73fd4-2292">Lägg till PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="73fd4-2292">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="73fd4-2293">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="73fd4-2293">New cmdlets</span></span>
        - <span data-ttu-id="73fd4-2294">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="73fd4-2294">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="73fd4-2295">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="73fd4-2295">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="73fd4-2296">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="73fd4-2296">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="73fd4-2297">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="73fd4-2297">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="73fd4-2298">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="73fd4-2298">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="73fd4-2299">Lägg till PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="73fd4-2299">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="73fd4-2300">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="73fd4-2300">New cmdlets</span></span>
        - <span data-ttu-id="73fd4-2301">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="73fd4-2301">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="73fd4-2302">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="73fd4-2302">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="73fd4-2303">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="73fd4-2303">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="73fd4-2304">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="73fd4-2304">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="73fd4-2305">Nedanstående kommandon för funktionen har uppdaterats: Flaggan UseLocalAzureIpAddress på VpnConnection</span><span class="sxs-lookup"><span data-stu-id="73fd4-2305">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="73fd4-2306">New-AzVpnConnection har uppdaterats: Den valfria parametern -UseLocalAzureIpAddress har lagts till för att visa att en lokal IP-adress i Azure ska användas som källadress när anslutningen initieras.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2306">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="73fd4-2307">Set-AzVpnConnection har uppdaterats: Den valfria parametern -UseLocalAzureIpAddress har lagts till för att visa att en lokal IP-adress i Azure ska användas som källadress när anslutningen initieras.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2307">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="73fd4-2308">Det skrivskyddade fältet PeeredConnections har lagts till i ExpressRoute-peering.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2308">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="73fd4-2309">Det skrivskyddade fältet GlobalReachEnabled har lagts till i ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2309">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="73fd4-2310">Ett attribut för icke-bakåtkompatibla ändringar har lagts till för att lyfta fram utfasning av fältet AllowGlobalReach i modellen ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="73fd4-2310">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="73fd4-2311">Problem 8756 har åtgärdats: Fel vid användning av TargetListenerID med AzApplicationGatewayRedirectConfiguration-cmdletar</span><span class="sxs-lookup"><span data-stu-id="73fd4-2311">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="73fd4-2312">En bugg i New-AzApplicationGatewayPathRuleConfig som gjorde att regeluppsättningen för att återskapa inte kunde anges har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2312">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="73fd4-2313">Visningen av VirtualNetworkTaps i NetworkInterfaceIpConfiguration har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="73fd4-2313">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="73fd4-2314">Cortex Get-cmdletar för att visa en lista med alla delar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="73fd4-2314">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="73fd4-2315">Funktionen för att skapa VirtualHub-referenser för ExpressRouteGateways och VpnGateway har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="73fd4-2315">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="73fd4-2316">Stöd för tillgänglighetszoner i AzureFirewall och NatGateway har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-2316">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="73fd4-2317">Cmdleten Get-AzNetworkServiceTag har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-2317">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="73fd4-2318">Lägg till stöd för flera offentliga IP-adresser för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="73fd4-2318">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="73fd4-2319">Cmdleten New-AzFirewall har uppdaterats:</span><span class="sxs-lookup"><span data-stu-id="73fd4-2319">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="73fd4-2320">Parametern -PublicIpAddress som accepterar ett eller flera offentliga IP-adressobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-2320">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="73fd4-2321">Parametern -VirtualNetwork som accepterar ett virtuellt nätverksobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-2321">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="73fd4-2322">Metoderna AddPublicIpAddress och RemovePublicIpAddress har lagts till på brandväggsobjekt – dessa accepterar ett offentligt IP-adressobjekt som indata</span><span class="sxs-lookup"><span data-stu-id="73fd4-2322">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="73fd4-2323">Inaktuella parametrar -PublicIpName och -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="73fd4-2323">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="73fd4-2324">Nedanstående kommandon för funktionen har uppdaterats: Ange autentiseringsalternativ för VpnClient AAD till resurser för virtuella nätverksgatewayer.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2324">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="73fd4-2325">New-AzVirtualNetworkGateway har uppdaterats: De valfria parametrarna AadTenantUri, AadAudienceId och AadIssuerUri för att ange VpnClient AAD-autentiseringsalternativ på en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2325">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="73fd4-2326">Set-AzVirtualNetworkGateway har uppdaterats: De valfria parametrarna AadTenantUri, AadAudienceId och AadIssuerUri för att ange VpnClient AAD-autentiseringsalternativ på en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2326">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="73fd4-2327">Set-AzVirtualNetworkGateway har uppdaterats: Den valfria växelparametern RemoveAadAuthentication som tar bort VpnClient AAD-autentiseringsalternativ från en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2327">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="73fd4-2328">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="73fd4-2328">Az.OperationalInsights</span></span>
* <span data-ttu-id="73fd4-2329">Aktivera prisnivån **pergb2018** i kommandot ”New-AzureRmOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="73fd4-2329">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="73fd4-2330">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73fd4-2330">Az.Resources</span></span>
* <span data-ttu-id="73fd4-2331">Stöd för ytterligare alternativ för att exportera en mall</span><span class="sxs-lookup"><span data-stu-id="73fd4-2331">Support for additional Template Export options</span></span>
    - <span data-ttu-id="73fd4-2332">Lägg till parametern ”-SkipResourceNameParameterization” till Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="73fd4-2332">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="73fd4-2333">Lägg till parametern ”-SkipAllParameterization” till Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="73fd4-2333">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="73fd4-2334">Lägg till parametern ”-Resource” till Export-AzResourceGroup för exporterad resursfiltrering</span><span class="sxs-lookup"><span data-stu-id="73fd4-2334">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="73fd4-2335">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="73fd4-2335">Az.ServiceFabric</span></span>
* <span data-ttu-id="73fd4-2336">Åtgärda att fel tumavtryck används vid tilläggning av certifikat i ByExistingKeyVault i vissa fall</span><span class="sxs-lookup"><span data-stu-id="73fd4-2336">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="73fd4-2337">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73fd4-2337">Az.Sql</span></span>
* <span data-ttu-id="73fd4-2338">Åtgärda suffix för lagringsslutpunkt i Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="73fd4-2338">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="73fd4-2339">Åtgärda att aktivering av Advanced Data Security åsidosätter Advanced Threat Protection-princip</span><span class="sxs-lookup"><span data-stu-id="73fd4-2339">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="73fd4-2340">Nya cmdletar för Management.Sql som gör att kunderna kan lägga till nycklar för transparent datakryptering (TDE) och ange TDE-skydd för hanterade instanser</span><span class="sxs-lookup"><span data-stu-id="73fd4-2340">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="73fd4-2341">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="73fd4-2341">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="73fd4-2342">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="73fd4-2342">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="73fd4-2343">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="73fd4-2343">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="73fd4-2344">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="73fd4-2344">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="73fd4-2345">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="73fd4-2345">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="73fd4-2346">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="73fd4-2346">Az.Storage</span></span>
* <span data-ttu-id="73fd4-2347">Stöd för typerna FileStorage och SkuName Premium_ZRS när lagringskonton skapas</span><span class="sxs-lookup"><span data-stu-id="73fd4-2347">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="73fd4-2348">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="73fd4-2348">New-AzStorageAccount</span></span>
* <span data-ttu-id="73fd4-2349">Beskrivningen av cmdleten för bloboföränderlighet har förtydligats</span><span class="sxs-lookup"><span data-stu-id="73fd4-2349">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="73fd4-2350">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="73fd4-2350">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="73fd4-2351">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="73fd4-2351">Az.Websites</span></span>
* <span data-ttu-id="73fd4-2352">Optimerar Get-AzWebAppCertificate för att filtrera efter resursgrupp på servern i stället för klienten</span><span class="sxs-lookup"><span data-stu-id="73fd4-2352">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="73fd4-2353">Lägger till växlingsparametern -UseDisasterRecovery till Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="73fd4-2353">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="73fd4-2354">2.2.0 – juni 2019</span><span class="sxs-lookup"><span data-stu-id="73fd4-2354">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="73fd4-2355">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="73fd4-2355">Az.Cdn</span></span>
* <span data-ttu-id="73fd4-2356">Uppdaterade cmdletar för att ge stöd för rulesEngine-funktion baserat på API-version 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2356">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73fd4-2357">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73fd4-2357">Az.Compute</span></span>
* <span data-ttu-id="73fd4-2358">Lade till parameter `NoWait` som startar åtgärden och returnerar omedelbart, innan åtgärden har slutförts.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2358">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="73fd4-2359">Uppdaterade cmdletar:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="73fd4-2359">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="73fd4-2360">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="73fd4-2360">Az.EventHub</span></span>
* <span data-ttu-id="73fd4-2361">Korrigering för #9231 – Get-AzEventHubNamespace returnerar inga taggar</span><span class="sxs-lookup"><span data-stu-id="73fd4-2361">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="73fd4-2362">Korrigering för #9230 – Get-AzEventHubNamespace returnerar ResourceGroup istället för ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73fd4-2362">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73fd4-2363">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73fd4-2363">Az.Network</span></span>
* <span data-ttu-id="73fd4-2364">Uppdatera ResourceId och InputObject för NAT-gateway</span><span class="sxs-lookup"><span data-stu-id="73fd4-2364">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="73fd4-2365">Lägg till alias för ResourceId och InputObject</span><span class="sxs-lookup"><span data-stu-id="73fd4-2365">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="73fd4-2366">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="73fd4-2366">Az.PolicyInsights</span></span>
* <span data-ttu-id="73fd4-2367">Åtgärda Null-referensproblem i Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="73fd4-2367">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="73fd4-2368">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="73fd4-2368">Az.RecoveryServices</span></span>
* <span data-ttu-id="73fd4-2369">Minsta kvarhållning för IaaSVM-policy i dagar ändrat till 7 från 1</span><span class="sxs-lookup"><span data-stu-id="73fd4-2369">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="73fd4-2370">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="73fd4-2370">Az.ServiceBus</span></span>
* <span data-ttu-id="73fd4-2371">Korrigering för ärende #9182 – Get-AzServiceBusNamespace returnerar ResourceGroup istället för ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73fd4-2371">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="73fd4-2372">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="73fd4-2372">Az.ServiceFabric</span></span>
* <span data-ttu-id="73fd4-2373">Åtgärda stavfel i felmeddelandet för Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="73fd4-2373">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="73fd4-2374">Åtgärda saknat tecken i Service Fabric-kommandorader</span><span class="sxs-lookup"><span data-stu-id="73fd4-2374">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="73fd4-2375">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73fd4-2375">Az.Sql</span></span>
* <span data-ttu-id="73fd4-2376">Lägg till parametern DnsZonePartner för New-AzureSqlInstance-cmdlet för att ge stöd för AutoDr för hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2376">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="73fd4-2377">Avvecklar cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="73fd4-2377">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="73fd4-2378">Döp om cmdletar för hotidentifiering till Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="73fd4-2378">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="73fd4-2379">Parametrarna New-AzSqlInstance -StorageSizeInGB och -LicenseType är nu valfria.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2379">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="73fd4-2380">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="73fd4-2380">Az.Websites</span></span>
* <span data-ttu-id="73fd4-2381">åtgärdar problemet där användningen av Set-AzWebApp och Set-AzWebAppSlot med -WebApp-egenskap tog bort taggarna</span><span class="sxs-lookup"><span data-stu-id="73fd4-2381">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="73fd4-2382">2.1.0 – maj 2019</span><span class="sxs-lookup"><span data-stu-id="73fd4-2382">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="73fd4-2383">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="73fd4-2383">Az.ApiManagement</span></span>
* <span data-ttu-id="73fd4-2384">Skapade nya cmdletar för att hantera diagnostik för global- och API-omfång</span><span class="sxs-lookup"><span data-stu-id="73fd4-2384">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="73fd4-2385">**Get-AzApiManagementDiagnostic** – Skaffa diagnostik konfigurerad för global- eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="73fd4-2385">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="73fd4-2386">**New-AzApiManagementDiagnostic** – Skapa ny diagnostik för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="73fd4-2386">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="73fd4-2387">**New-AzApiManagementHttpMessageDiagnostic** – Skapa diagnostikinställning om vilka rubriker som ska loggas och storleken på brödtextbyte</span><span class="sxs-lookup"><span data-stu-id="73fd4-2387">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="73fd4-2388">**New-AzApiManagementPipelineDiagnosticSetting** – Skapa diagnostikinställningar för inkommande/utgående HTTP-meddelanden till gatewayen.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2388">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="73fd4-2389">**New-AzApiManagementSamplingSetting** – Skapa samplinginställningar för begäranden/svar för en diagnostik</span><span class="sxs-lookup"><span data-stu-id="73fd4-2389">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="73fd4-2390">**Remove-AzApiManagementDiagnostic** – Ta bort en diagnostikenhet för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="73fd4-2390">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="73fd4-2391">**Set-AzApiManagementDiagnostic** – Uppdatera en diagnostikenhet för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="73fd4-2391">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="73fd4-2392">Skapade nya cmdletar för hantering av cacheminne i ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="73fd4-2392">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="73fd4-2393">**Get-AzApiManagementCache** – Hämta information om cacheminnet som anges av identifierare eller alla cacheminnen</span><span class="sxs-lookup"><span data-stu-id="73fd4-2393">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="73fd4-2394">**New-AzApiManagementCache** – Skapa ett nytt default-cacheminne eller cacheminne i en viss Azure-region</span><span class="sxs-lookup"><span data-stu-id="73fd4-2394">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="73fd4-2395">**Remove-AzApiManagementCache** – Ta bort ett cacheminne</span><span class="sxs-lookup"><span data-stu-id="73fd4-2395">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="73fd4-2396">**Remove-AzApiManagementCache** – Ta bort ett cacheminne</span><span class="sxs-lookup"><span data-stu-id="73fd4-2396">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="73fd4-2397">Skapade nya cmdletar för hantering av API-schema</span><span class="sxs-lookup"><span data-stu-id="73fd4-2397">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="73fd4-2398">**New-AzApiManagementSchema** – Skapa ett nytt schema för ett API</span><span class="sxs-lookup"><span data-stu-id="73fd4-2398">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="73fd4-2399">**Get-AzApiManagementSchema** – Hämta de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="73fd4-2399">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="73fd4-2400">**Remove-AzApiManagementSchema** – Ta bort de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="73fd4-2400">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="73fd4-2401">**Set-AzApiManagementSchema** – Uppdatera de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="73fd4-2401">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="73fd4-2402">Skapa ny cmdlet för att generera en användartoken.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2402">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="73fd4-2403">**New-AzApiManagementUserToken** – Skapa en ny användartoken som enligt standardinställning är giltig i 8 timmar. Token för GIT-användaren kan skapas med den här cmdleten./</span><span class="sxs-lookup"><span data-stu-id="73fd4-2403">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="73fd4-2404">Skapade en ny cmdlet för att hämta nätverksstatus</span><span class="sxs-lookup"><span data-stu-id="73fd4-2404">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="73fd4-2405">**Get-AzApiManagementNetworkStatus** – Hämta nätverksstatusanslutningen för resurserna som API Management-tjänsten är beroende av.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2405">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="73fd4-2406">Det här är användbart när du distribuerar ApiManagement-tjänsten i ett virtuellt nätverk och validerar om något beroende är brutet.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2406">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="73fd4-2407">Uppdaterade cmdlet **New-AzApiManagement** för att hantera ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="73fd4-2407">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="73fd4-2408">Lade till stöd för den nya SKU:n Consumption</span><span class="sxs-lookup"><span data-stu-id="73fd4-2408">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="73fd4-2409">Aktiverade stöd för att slå på flaggan EnableClientCertificate för SKU:n Consumption</span><span class="sxs-lookup"><span data-stu-id="73fd4-2409">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="73fd4-2410">Den nya cmdleten **New-AzApiManagementSslSetting** gör det möjligt att ställa in TLS/SSL-inställningen på ”Backend” och ”Frontend” (serverdel och klientdel).</span><span class="sxs-lookup"><span data-stu-id="73fd4-2410">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="73fd4-2411">Det här kan också användas till att konfigurera chiffer som 3DES och ServerProtocols som Http2 för Frontend för en ApiManagement-tjänst.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2411">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="73fd4-2412">Stöd har lagts till för att konfigurera värdnamnet DeveloperPortal på ApiManagement-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2412">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="73fd4-2413">Uppdaterade cmdletar **Get-AzApiManagementSsoToken** för att ta PsApiManagement-objekt som indata</span><span class="sxs-lookup"><span data-stu-id="73fd4-2413">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="73fd4-2414">Uppdaterad cmdleten för att visa infogade felmeddelanden</span><span class="sxs-lookup"><span data-stu-id="73fd4-2414">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="73fd4-2415">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Felkod: Felmeddelande av typen ValidationError: Ett eller flera fält innehåller felaktiga värden: Felinformation:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="73fd4-2415">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="73fd4-2416">Uppdaterade cmdlet **Export-AzApiManagementApi** för att exportera API:er i OpenApi 3.0-format</span><span class="sxs-lookup"><span data-stu-id="73fd4-2416">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="73fd4-2417">Uppdaterade cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="73fd4-2417">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="73fd4-2418">Importera API från dokumentspecifikationen OpenApi 3.0</span><span class="sxs-lookup"><span data-stu-id="73fd4-2418">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="73fd4-2419">Om du vill åsidosätta egenskapen PsApiManagementSchema specificerad i ett dokument (Swagger, Wadl, Wsdl, OpenApi).</span><span class="sxs-lookup"><span data-stu-id="73fd4-2419">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="73fd4-2420">Åsidosätta egenskapen ServiceUrl som specificeras i ett dokument.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2420">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="73fd4-2421">Uppdaterade cmdlet **Get-AzApiManagementPolicy** för att returnera policy i undantaget format av typen icke-XML med rawxml</span><span class="sxs-lookup"><span data-stu-id="73fd4-2421">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="73fd4-2422">Uppdaterade cmdlet **Set-AzApiManagementPolicy** för att godkänna policy i undantaget format av typen icke-XML med rawxml och XML undantaget med xml</span><span class="sxs-lookup"><span data-stu-id="73fd4-2422">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="73fd4-2423">Uppdaterad cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="73fd4-2423">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="73fd4-2424">Konfigurera API med OpenId auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2424">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="73fd4-2425">Skapa ett API i ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="73fd4-2425">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="73fd4-2426">Klona ett API med SourceApiId och SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2426">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="73fd4-2427">Möjlighet att konfigurera SubscriptionRequired i API-omfattningen.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2427">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="73fd4-2428">Uppdaterad cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="73fd4-2428">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="73fd4-2429">Konfigurera API med OpenId auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2429">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="73fd4-2430">Uppdatera ett API till ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="73fd4-2430">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="73fd4-2431">Möjlighet att konfigurera SubscriptionRequired i API-omfattningen.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2431">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="73fd4-2432">Uppdaterad cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="73fd4-2432">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="73fd4-2433">Klona en befintlig version med hjälp av SourceApiRevision (kopiera taggar, produkter, åtgärder och principer).</span><span class="sxs-lookup"><span data-stu-id="73fd4-2433">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="73fd4-2434">Den nya revisionen antar ApiId från den överordnade instansen.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2434">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="73fd4-2435">Tillhandahålla ApiRevisionDescription</span><span class="sxs-lookup"><span data-stu-id="73fd4-2435">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="73fd4-2436">Åsidosätta ServiceUrl vid kloning av ett API.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2436">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="73fd4-2437">Uppdaterad cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="73fd4-2437">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="73fd4-2438">Konfigurera AAD eller AADB2C med en Authority</span><span class="sxs-lookup"><span data-stu-id="73fd4-2438">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="73fd4-2439">Konfigurera SignupPolicy, SigninPolicy, ProfileEditingPolicy och PasswordResetPolicy</span><span class="sxs-lookup"><span data-stu-id="73fd4-2439">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="73fd4-2440">Uppdaterad cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="73fd4-2440">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="73fd4-2441">Kompensera för ny SubscriptonModel med Scope och UserId</span><span class="sxs-lookup"><span data-stu-id="73fd4-2441">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="73fd4-2442">Kompensera för gammal prenumerationsmodell med ProductId och UserId</span><span class="sxs-lookup"><span data-stu-id="73fd4-2442">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="73fd4-2443">Lägg till funktion för att aktivera AllowTracing på prenumerationsnivå.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2443">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="73fd4-2444">Uppdaterad cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="73fd4-2444">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="73fd4-2445">Kompensera för ny SubscriptonModel med Scope och UserId</span><span class="sxs-lookup"><span data-stu-id="73fd4-2445">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="73fd4-2446">Kompensera för gammal prenumerationsmodell med ProductId och UserId</span><span class="sxs-lookup"><span data-stu-id="73fd4-2446">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="73fd4-2447">Lägg till funktion för att aktivera AllowTracing på prenumerationsnivå.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2447">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="73fd4-2448">Uppdaterade följande cmdletar för att acceptera ResourceId som indata</span><span class="sxs-lookup"><span data-stu-id="73fd4-2448">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="73fd4-2449">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="73fd4-2449">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="73fd4-2450">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="73fd4-2450">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="73fd4-2451">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="73fd4-2451">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="73fd4-2452">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="73fd4-2452">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="73fd4-2453">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="73fd4-2453">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="73fd4-2454">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="73fd4-2454">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="73fd4-2455">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="73fd4-2455">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="73fd4-2456">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="73fd4-2456">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="73fd4-2457">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="73fd4-2457">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="73fd4-2458">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="73fd4-2458">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="73fd4-2459">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="73fd4-2459">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="73fd4-2460">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="73fd4-2460">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="73fd4-2461">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="73fd4-2461">Az.Automation</span></span>
* <span data-ttu-id="73fd4-2462">Uppdaterade Get-AzAutomationJobOutputRecord för att hantera postvärden av typen JSON och Text.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2462">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="73fd4-2463">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="73fd4-2463">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="73fd4-2464">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="73fd4-2464">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="73fd4-2465">Ändrade beteende för Start-AzAutomationDscCompilationJob till att bara starta jobbet istället för att vänta på slutförandet.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2465">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="73fd4-2466">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="73fd4-2466">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="73fd4-2467">Korrigering för Get-AzAutomationDscNode när using -Name returnerar alla noder.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2467">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="73fd4-2468">Nu returnerar den endast den matchande noden.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2468">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73fd4-2469">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73fd4-2469">Az.Compute</span></span>
* <span data-ttu-id="73fd4-2470">Lägg till parametrarna ProtectFromScaleIn och ProtectFromScaleSetAction i cmdleten Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2470">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="73fd4-2471">Nu är standardinställningen att vimpelparametern New-AzVM använder en tillgänglig plats om USA, östra inte stöds</span><span class="sxs-lookup"><span data-stu-id="73fd4-2471">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="73fd4-2472">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="73fd4-2472">Az.DataLakeStore</span></span>
* <span data-ttu-id="73fd4-2473">Uppdatera ADLS-sdk för att använda httpclient, integrera dataplanstestning med Azure-ramverk</span><span class="sxs-lookup"><span data-stu-id="73fd4-2473">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="73fd4-2474">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="73fd4-2474">Az.Monitor</span></span>
* <span data-ttu-id="73fd4-2475">Korrigera felaktiga parameternamn i hjälpexempel</span><span class="sxs-lookup"><span data-stu-id="73fd4-2475">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73fd4-2476">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73fd4-2476">Az.Network</span></span>
* <span data-ttu-id="73fd4-2477">Lägg till flaggan DisableBgpRoutePropagation i utdata för effektiv routningstabell</span><span class="sxs-lookup"><span data-stu-id="73fd4-2477">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="73fd4-2478">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="73fd4-2478">Updated cmdlet:</span></span>
        - <span data-ttu-id="73fd4-2479">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="73fd4-2479">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="73fd4-2480">Åtgärda dubbelstreck i dokumentationen New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="73fd4-2480">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="73fd4-2481">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73fd4-2481">Az.Resources</span></span>
* <span data-ttu-id="73fd4-2482">Lägg till ny cmdlet Get-AzureRmDenyAssignment för att hämta tilldelningsnekanden</span><span class="sxs-lookup"><span data-stu-id="73fd4-2482">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="73fd4-2483">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73fd4-2483">Az.Sql</span></span>
* <span data-ttu-id="73fd4-2484">Döp om Advanced Threat Protection-cmdletar för Advanced Data Security och aktivera Vulnerability Assessment som standard</span><span class="sxs-lookup"><span data-stu-id="73fd4-2484">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="73fd4-2485">2.0.0 – maj 2019</span><span class="sxs-lookup"><span data-stu-id="73fd4-2485">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="73fd4-2486">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73fd4-2486">Az.Accounts</span></span>
* <span data-ttu-id="73fd4-2487">Uppdatera autentiseringsbiblioteket för att åtgärda ADFS-problem med autentisering av användarnamn/lösenord</span><span class="sxs-lookup"><span data-stu-id="73fd4-2487">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="73fd4-2488">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="73fd4-2488">Az.CognitiveServices</span></span>
* <span data-ttu-id="73fd4-2489">Visa endast Bing-ansvarsfriskrivning för Bing-sökningstjänster.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2489">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="73fd4-2490">Förbättra felmeddelande när det inte går att skapa konton.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2490">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73fd4-2491">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73fd4-2491">Az.Compute</span></span>
* <span data-ttu-id="73fd4-2492">Funktion för närhetsplaceringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2492">Proximity placement group feature.</span></span>
    - <span data-ttu-id="73fd4-2493">Följande nya cmdletar har lagts till:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="73fd4-2493">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="73fd4-2494">Den nya parametern ProximityPlacementGroupId har lagts till i följande cmdletar:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="73fd4-2494">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="73fd4-2495">Parametern StorageAccountType har lagts till i New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2495">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="73fd4-2496">TargetRegion för New-AzGalleryImageVersion kan innehålla StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2496">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="73fd4-2497">Växlingsparametern SkipShutdown har lagts till i Stop-AzVM och Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="73fd4-2497">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="73fd4-2498">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="73fd4-2498">Breaking changes</span></span>
    - <span data-ttu-id="73fd4-2499">Set-AzVMBootDiagnostics har ändrats till Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2499">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="73fd4-2500">Export-AzLogAnalyticThrottledRequests har ändrats till Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2500">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="73fd4-2501">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="73fd4-2501">Az.DeploymentManager</span></span>
* <span data-ttu-id="73fd4-2502">De första allmänt tillgängliga versionerna av cmdletar för Distributionshanteraren i Azure</span><span class="sxs-lookup"><span data-stu-id="73fd4-2502">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="73fd4-2503">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="73fd4-2503">Az.Dns</span></span>
* <span data-ttu-id="73fd4-2504">Automatisk delegering av DNS för NameServer</span><span class="sxs-lookup"><span data-stu-id="73fd4-2504">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="73fd4-2505">Det överordnade zonnamnet kan användas som ytterligare valfri parameter i cmdleten för att skapa DNS-zoner.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2505">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="73fd4-2506">Lägger till NS-poster för en nyligen skapad underordnad zon i den överordnade zonen.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2506">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="73fd4-2507">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="73fd4-2507">Az.FrontDoor</span></span>
* <span data-ttu-id="73fd4-2508">De första allmänt tillgängliga versionerna av cmdletar för Azure FrontDoor</span><span class="sxs-lookup"><span data-stu-id="73fd4-2508">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="73fd4-2509">Byt namn på WAF-cmdletar så att de omfattar ”Waf”</span><span class="sxs-lookup"><span data-stu-id="73fd4-2509">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="73fd4-2510">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="73fd4-2510">Az.HDInsight</span></span>
* <span data-ttu-id="73fd4-2511">Två cmdletar har tagits bort:</span><span class="sxs-lookup"><span data-stu-id="73fd4-2511">Removed two cmdlets:</span></span>
    - <span data-ttu-id="73fd4-2512">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="73fd4-2512">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="73fd4-2513">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="73fd4-2513">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="73fd4-2514">En ny cmdlet har lagts till, Set-AzHDInsightGatewayCredential, som ersätter Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="73fd4-2514">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="73fd4-2515">Uppdatera cmdleten Get-AzHDInsightJobOutput för att skilja mellan läsarrollen och HDInsight-operatörsrollen:</span><span class="sxs-lookup"><span data-stu-id="73fd4-2515">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="73fd4-2516">Användare med läsarrollen måste uttryckligen ange parametern ”DefaultStorageAccountKey”, annars uppstår fel.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2516">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="73fd4-2517">Användare med HDInsight-operatörsrollen påverkas inte.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2517">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="73fd4-2518">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="73fd4-2518">Az.Monitor</span></span>
* <span data-ttu-id="73fd4-2519">Nya cmdletar för SQR API (schemalagd frågeregel)</span><span class="sxs-lookup"><span data-stu-id="73fd4-2519">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="73fd4-2520">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="73fd4-2520">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="73fd4-2521">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="73fd4-2521">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="73fd4-2522">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="73fd4-2522">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="73fd4-2523">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="73fd4-2523">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="73fd4-2524">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="73fd4-2524">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="73fd4-2525">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="73fd4-2525">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="73fd4-2526">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="73fd4-2526">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="73fd4-2527">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="73fd4-2527">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="73fd4-2528">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="73fd4-2528">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="73fd4-2529">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="73fd4-2529">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="73fd4-2530">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="73fd4-2530">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="73fd4-2531">[Mer](/rest/api/monitor/scheduledqueryrules) information om SQR API</span><span class="sxs-lookup"><span data-stu-id="73fd4-2531">[More](/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="73fd4-2532">Az.Monitor.md har uppdaterats för att omfatta cmdletar för måttbaserade aviseringsregler i GenV2 (inte klassiska)</span><span class="sxs-lookup"><span data-stu-id="73fd4-2532">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73fd4-2533">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73fd4-2533">Az.Network</span></span>
* <span data-ttu-id="73fd4-2534">Lägg till stöd för NAT Gateway-resurs</span><span class="sxs-lookup"><span data-stu-id="73fd4-2534">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="73fd4-2535">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="73fd4-2535">New cmdlets</span></span>
        - <span data-ttu-id="73fd4-2536">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="73fd4-2536">New-AzNatGateway</span></span>
        - <span data-ttu-id="73fd4-2537">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="73fd4-2537">Get-AzNatGateway</span></span>
        - <span data-ttu-id="73fd4-2538">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="73fd4-2538">Set-AzNatGateway</span></span>
        - <span data-ttu-id="73fd4-2539">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="73fd4-2539">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="73fd4-2540">Uppdaterade cmdletar</span><span class="sxs-lookup"><span data-stu-id="73fd4-2540">Updated cmdlets</span></span>
        - <span data-ttu-id="73fd4-2541">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="73fd4-2541">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="73fd4-2542">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="73fd4-2542">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="73fd4-2543">Nedanstående kommandon för funktionen har uppdaterats: Ange/ta bort anpassade vägar på Brooklyn Gateway.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2543">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="73fd4-2544">New-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ställa in adressprefix som anpassade vägar för att ange gateway.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2544">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="73fd4-2545">Set-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ange adressprefix som anpassade vägar för att ange gateway.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2545">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="73fd4-2546">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="73fd4-2546">Az.PolicyInsights</span></span>
* <span data-ttu-id="73fd4-2547">Stöd för att fråga efter information om principutvärdering.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2547">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="73fd4-2548">Lägg till parametern ”-Expand” för Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2548">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="73fd4-2549">Stöd för -Expand PolicyEvaluationDetails.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2549">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="73fd4-2550">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="73fd4-2550">Az.RecoveryServices</span></span>
* <span data-ttu-id="73fd4-2551">Stöd för att dela prenumeration mellan Azure och Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2551">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="73fd4-2552">Markering av kommande icke-bakåtkompatibla ändringar för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2552">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="73fd4-2553">Korrigering för återställningsplan och åtgärdsplan i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2553">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="73fd4-2554">Korrigering för mappning av uppdateringsnätverk i Azure Site Recovery för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2554">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="73fd4-2555">Korrigering för instruktioner för uppdateringsskydd i Azure Site Recovery för Azure till Azure för hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2555">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="73fd4-2556">Andra mindre korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2556">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="73fd4-2557">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="73fd4-2557">Az.Relay</span></span>
* <span data-ttu-id="73fd4-2558">Korrigera stavfel i kundriktade meddelanden</span><span class="sxs-lookup"><span data-stu-id="73fd4-2558">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="73fd4-2559">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="73fd4-2559">Az.ServiceBus</span></span>
* <span data-ttu-id="73fd4-2560">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="73fd4-2560">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="73fd4-2561">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="73fd4-2561">Az.Storage</span></span>
* <span data-ttu-id="73fd4-2562">Uppgradera till lagringsklientbiblioteket 10.0.1 (namnområdet för alla objekt från detta SDK ändras från ”Microsoft.WindowsAzure.Storage. *till ”Microsoft.Azure.Storage.* ”)</span><span class="sxs-lookup"><span data-stu-id="73fd4-2562">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="73fd4-2563">Uppgradera till Microsoft.Azure.Management.Storage 11.0.0 för att stödja den nya API-versionen 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2563">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="73fd4-2564">Standardlagringskontot i Skapa lagringskonto ändras från ”Storage” till ”StorageV2”</span><span class="sxs-lookup"><span data-stu-id="73fd4-2564">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="73fd4-2565">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="73fd4-2565">New-AzStorageAccount</span></span>
* <span data-ttu-id="73fd4-2566">Ändra lagringskontots cmdlet-utdata Sku.Name för att passa med indata-SkuName genom att lägga till ”-”. Till exempel ändras ”StandardLRS” till ”Standard_LRS”</span><span class="sxs-lookup"><span data-stu-id="73fd4-2566">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="73fd4-2567">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="73fd4-2567">New-AzStorageAccount</span></span>
    - <span data-ttu-id="73fd4-2568">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="73fd4-2568">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="73fd4-2569">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="73fd4-2569">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="73fd4-2570">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="73fd4-2570">Az.Websites</span></span>
* <span data-ttu-id="73fd4-2571">Egenskapen ”typ” konfigureras nu för PSSite-objekt som returneras av Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="73fd4-2571">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="73fd4-2572">Get-AzWebApp\*Metrics och Get-AzAppServicePlanMetrics markeras som inaktuella</span><span class="sxs-lookup"><span data-stu-id="73fd4-2572">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="73fd4-2573">1.8.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="73fd4-2573">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="73fd4-2574">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="73fd4-2574">Highlights since the last major release</span></span>
* <span data-ttu-id="73fd4-2575">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="73fd4-2575">General availability of `Az` module</span></span>
* <span data-ttu-id="73fd4-2576">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="73fd4-2576">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="73fd4-2577">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="73fd4-2577">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="73fd4-2578">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-2578">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="73fd4-2579">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-2579">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="73fd4-2580">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-2580">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="73fd4-2581">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="73fd4-2581">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="73fd4-2582">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73fd4-2582">Az.Accounts</span></span>
* <span data-ttu-id="73fd4-2583">Uppdatera Uninstall-AzureRm för att ta bort moduler i Mac på ett korrekt sätt</span><span class="sxs-lookup"><span data-stu-id="73fd4-2583">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="73fd4-2584">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="73fd4-2584">Az.Batch</span></span>
* <span data-ttu-id="73fd4-2585">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2585">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="73fd4-2586">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="73fd4-2586">Az.Cdn</span></span>
* <span data-ttu-id="73fd4-2587">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2587">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="73fd4-2588">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="73fd4-2588">Az.CognitiveServices</span></span>
* <span data-ttu-id="73fd4-2589">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2589">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73fd4-2590">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73fd4-2590">Az.Compute</span></span>
* <span data-ttu-id="73fd4-2591">Åtgärda problem med AEM-installationen om resurs-ID:n för diskar innehåller resourcegroups i gemener i resurs-ID:n</span><span class="sxs-lookup"><span data-stu-id="73fd4-2591">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="73fd4-2592">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2592">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="73fd4-2593">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="73fd4-2593">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="73fd4-2594">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="73fd4-2594">Az.DataFactory</span></span>
* <span data-ttu-id="73fd4-2595">Lägg till SsisProperties om NodeCount inte är null för hanterad integreringskörning.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2595">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="73fd4-2596">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="73fd4-2596">Az.DataLakeStore</span></span>
* <span data-ttu-id="73fd4-2597">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2597">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="73fd4-2598">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="73fd4-2598">Az.EventGrid</span></span>
* <span data-ttu-id="73fd4-2599">Hjälptexten för slutpunkten har uppdaterats för att visa att resurser ska skapas innan cmdletarna för att skapa/uppdatera händelseprenumerationer används.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2599">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="73fd4-2600">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="73fd4-2600">Az.EventHub</span></span>
* <span data-ttu-id="73fd4-2601">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="73fd4-2601">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="73fd4-2602">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="73fd4-2602">Az.HDInsight</span></span>
* <span data-ttu-id="73fd4-2603">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2603">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="73fd4-2604">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="73fd4-2604">Az.IotHub</span></span>
* <span data-ttu-id="73fd4-2605">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2605">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="73fd4-2606">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="73fd4-2606">Az.KeyVault</span></span>
* <span data-ttu-id="73fd4-2607">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2607">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="73fd4-2608">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="73fd4-2608">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="73fd4-2609">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="73fd4-2609">Az.MachineLearning</span></span>
* <span data-ttu-id="73fd4-2610">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2610">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="73fd4-2611">Az.Media</span><span class="sxs-lookup"><span data-stu-id="73fd4-2611">Az.Media</span></span>
* <span data-ttu-id="73fd4-2612">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2612">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="73fd4-2613">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="73fd4-2613">Az.Monitor</span></span>
  * <span data-ttu-id="73fd4-2614">Nya cmdletar för måttbaserad aviseringsregel i GenV2 (inte klassisk)</span><span class="sxs-lookup"><span data-stu-id="73fd4-2614">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="73fd4-2615">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="73fd4-2615">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="73fd4-2616">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="73fd4-2616">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="73fd4-2617">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="73fd4-2617">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="73fd4-2618">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="73fd4-2618">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="73fd4-2619">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="73fd4-2619">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="73fd4-2620">Monitor SDK har uppdaterats till version 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="73fd4-2620">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73fd4-2621">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73fd4-2621">Az.Network</span></span>
* <span data-ttu-id="73fd4-2622">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2622">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="73fd4-2623">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="73fd4-2623">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="73fd4-2624">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="73fd4-2624">Az.NotificationHubs</span></span>
* <span data-ttu-id="73fd4-2625">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2625">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="73fd4-2626">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="73fd4-2626">Az.OperationalInsights</span></span>
* <span data-ttu-id="73fd4-2627">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2627">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="73fd4-2628">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="73fd4-2628">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="73fd4-2629">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2629">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="73fd4-2630">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="73fd4-2630">Az.RecoveryServices</span></span>
* <span data-ttu-id="73fd4-2631">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2631">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="73fd4-2632">Tabellformatet för SQL i virtuella Azure-datorer har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="73fd4-2632">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="73fd4-2633">En alternativ metod för att hämta platser i AzureFileShare har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-2633">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="73fd4-2634">ScheduleRunDays i SchedulePolicy-objekt har uppdaterats enligt tidszon</span><span class="sxs-lookup"><span data-stu-id="73fd4-2634">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="73fd4-2635">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="73fd4-2635">Az.RedisCache</span></span>
* <span data-ttu-id="73fd4-2636">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2636">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="73fd4-2637">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73fd4-2637">Az.Resources</span></span>
* <span data-ttu-id="73fd4-2638">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="73fd4-2638">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="73fd4-2639">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73fd4-2639">Az.Sql</span></span>
* <span data-ttu-id="73fd4-2640">Ersätt Monitor SDK-beroende med vanlig kod</span><span class="sxs-lookup"><span data-stu-id="73fd4-2640">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="73fd4-2641">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2641">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="73fd4-2642">Förbättrad process för klassificering av flera kolumner.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2642">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="73fd4-2643">Inkludera SKU-egenskaper (SKU-namn, serie, kapacitet) i svaret från Get-AzSqlServerServiceObjective och formatera som tabell som standard.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2643">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="73fd4-2644">Möjlighet att använda Get-AzSqlServerServiceObjective efter plats utan att behöva en redan befintlig server i regionen.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2644">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="73fd4-2645">Stöd för tidszonsparametern när hanterade instanser skapas.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2645">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="73fd4-2646">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="73fd4-2646">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="73fd4-2647">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="73fd4-2647">Az.Websites</span></span>
* <span data-ttu-id="73fd4-2648">åtgärdar Set-AzWebApp och Set-AzWebAppSlot så att de inte tar bort taggar vid körning</span><span class="sxs-lookup"><span data-stu-id="73fd4-2648">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="73fd4-2649">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2649">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="73fd4-2650">SDK för WebSites har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2650">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="73fd4-2651">Egenskapen AdminSiteName har tagits bort från PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2651">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="73fd4-2652">1.7.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="73fd4-2652">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="73fd4-2653">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="73fd4-2653">Highlights since the last major release</span></span>
* <span data-ttu-id="73fd4-2654">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="73fd4-2654">General availability of `Az` module</span></span>
* <span data-ttu-id="73fd4-2655">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="73fd4-2655">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="73fd4-2656">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="73fd4-2656">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="73fd4-2657">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-2657">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="73fd4-2658">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-2658">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="73fd4-2659">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-2659">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="73fd4-2660">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="73fd4-2660">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="73fd4-2661">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73fd4-2661">Az.Accounts</span></span>
* <span data-ttu-id="73fd4-2662">Add-AzEnvironment och Set-AzEnvironment har uppdaterats för att godkänna parametern AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="73fd4-2662">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="73fd4-2663">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="73fd4-2663">Az.AnalysisServices</span></span>
* <span data-ttu-id="73fd4-2664">ServiceClient används i cmdletar för dataplan och den ursprungliga autentiseringslogiken har tagits bort</span><span class="sxs-lookup"><span data-stu-id="73fd4-2664">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="73fd4-2665">Add-AzureASAccount används för omslutning av Connect-AzAccount för att undvika en icke-bakåtkompatibel ändring</span><span class="sxs-lookup"><span data-stu-id="73fd4-2665">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="73fd4-2666">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="73fd4-2666">Az.Automation</span></span>
* <span data-ttu-id="73fd4-2667">Buggen för cmdleten New-AzAutomationSoftwareUpdateConfiguration för inkluderingar har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2667">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="73fd4-2668">Nu bör parametern IncludedKbNumber och IncludedPackageNameMask fungera.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2668">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="73fd4-2669">Felkorrigering för dynamiska grupper i uppdateringshanteringen för azure automation</span><span class="sxs-lookup"><span data-stu-id="73fd4-2669">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73fd4-2670">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73fd4-2670">Az.Compute</span></span>
* <span data-ttu-id="73fd4-2671">Lägg till parametern HyperVGeneration i New-AzDiskConfig och New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="73fd4-2671">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="73fd4-2672">Tillåt att virtuella datorer skapas med galleribilder från andra klientorganisationer.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2672">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="73fd4-2673">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="73fd4-2673">Az.ContainerInstance</span></span>
* <span data-ttu-id="73fd4-2674">Ett problem har åtgärdats i parametern -Command för New-AzContainerGroup som lade till ett avslutande tomt argument</span><span class="sxs-lookup"><span data-stu-id="73fd4-2674">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="73fd4-2675">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="73fd4-2675">Az.DataFactory</span></span>
* <span data-ttu-id="73fd4-2676">ADF .Net SDK-versionen har uppdaterats till 3.0.2</span><span class="sxs-lookup"><span data-stu-id="73fd4-2676">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="73fd4-2677">Cmdleten Set-AzDataFactoryV2 har uppdaterats med extra parametrar för inställningar som rör RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2677">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="73fd4-2678">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73fd4-2678">Az.Resources</span></span>
* <span data-ttu-id="73fd4-2679">Förbättra hanteringen av providrar för Get-AzResource när parametrarna -ResourceId eller -ResourceGroupName, -Name och -ResourceType tillhandahålls</span><span class="sxs-lookup"><span data-stu-id="73fd4-2679">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="73fd4-2680">Förbättra felhanteringen för ”Test-AzDeployment” och ”Test-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="73fd4-2680">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="73fd4-2681">Hantera fel utanför distributionsvalideringen och ta med dem i kommandoutdata istället</span><span class="sxs-lookup"><span data-stu-id="73fd4-2681">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="73fd4-2682">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="73fd4-2682">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="73fd4-2683">Lägg till växlingsparametern -IgnoreDynamicParameters till en uppsättning av cmdletar för distribution för att hoppa över fråga i skript och jobbscenarier</span><span class="sxs-lookup"><span data-stu-id="73fd4-2683">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="73fd4-2684">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="73fd4-2684">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="73fd4-2685">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73fd4-2685">Az.Sql</span></span>
* <span data-ttu-id="73fd4-2686">Stöd för dataklassificering av databaser.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2686">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="73fd4-2687">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="73fd4-2687">Az.Storage</span></span>
* <span data-ttu-id="73fd4-2688">Rapportera detaljfel när lagringskontext skapas med parametern -UseConnectedAccount, men utan inloggning på Azure-kontot</span><span class="sxs-lookup"><span data-stu-id="73fd4-2688">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="73fd4-2689">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="73fd4-2689">New-AzStorageContext</span></span>
* <span data-ttu-id="73fd4-2690">Stöd för att hantera Blob Service-egenskaper för ett angivet lagringskonto med API:et för hanteringsplan</span><span class="sxs-lookup"><span data-stu-id="73fd4-2690">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="73fd4-2691">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="73fd4-2691">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="73fd4-2692">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="73fd4-2692">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="73fd4-2693">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="73fd4-2693">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="73fd4-2694">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="73fd4-2694">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="73fd4-2695">Stöd för -AsJob-cmdletar för att ladda upp och ladda ned blobar och filer</span><span class="sxs-lookup"><span data-stu-id="73fd4-2695">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="73fd4-2696">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="73fd4-2696">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="73fd4-2697">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="73fd4-2697">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="73fd4-2698">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="73fd4-2698">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="73fd4-2699">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="73fd4-2699">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="73fd4-2700">1.6.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="73fd4-2700">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="73fd4-2701">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="73fd4-2701">Highlights since the last major release</span></span>
* <span data-ttu-id="73fd4-2702">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="73fd4-2702">General availability of `Az` module</span></span>
* <span data-ttu-id="73fd4-2703">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="73fd4-2703">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="73fd4-2704">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="73fd4-2704">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="73fd4-2705">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-2705">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="73fd4-2706">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-2706">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="73fd4-2707">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-2707">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="73fd4-2708">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="73fd4-2708">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="73fd4-2709">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="73fd4-2709">Az.Automation</span></span>
* <span data-ttu-id="73fd4-2710">Azure Automation – ändring av uppdateringshantering för stöd för de nya funktionerna:</span><span class="sxs-lookup"><span data-stu-id="73fd4-2710">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="73fd4-2711">Dynamisk gruppering</span><span class="sxs-lookup"><span data-stu-id="73fd4-2711">Dynamic grouping</span></span>
    * <span data-ttu-id="73fd4-2712">För-/efterskrift</span><span class="sxs-lookup"><span data-stu-id="73fd4-2712">Pre-Post script</span></span>
    * <span data-ttu-id="73fd4-2713">Inställning för omstart</span><span class="sxs-lookup"><span data-stu-id="73fd4-2713">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73fd4-2714">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73fd4-2714">Az.Compute</span></span>
* <span data-ttu-id="73fd4-2715">Åtgärda problem med sökvägsmatchning i Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="73fd4-2715">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="73fd4-2716">Uppdatera Compute-klientbibliotek till 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2716">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="73fd4-2717">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="73fd4-2717">Az.KeyVault</span></span>
* <span data-ttu-id="73fd4-2718">Stöd för jokertecken för KeyVault-cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-2718">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73fd4-2719">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73fd4-2719">Az.Network</span></span>
* <span data-ttu-id="73fd4-2720">Lägg till stöd för Threat Intelligence för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="73fd4-2720">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="73fd4-2721">Lägg till resurs för brandväggsprincip på översta nivå och anpassade regler för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="73fd4-2721">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="73fd4-2722">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="73fd4-2722">Az.RecoveryServices</span></span>
* <span data-ttu-id="73fd4-2723">SnapshotRetentionInDays har lagts till i Azure-principen för virtuella datorer för stöd av Instant RP</span><span class="sxs-lookup"><span data-stu-id="73fd4-2723">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="73fd4-2724">Pipe-stöd för avregistrering av container har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-2724">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="73fd4-2725">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73fd4-2725">Az.Resources</span></span>
* <span data-ttu-id="73fd4-2726">Uppdatera stöd för jokertecken för Get-AzResource och Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="73fd4-2726">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="73fd4-2727">Uppdatera autentiseringsuppgifter som används vid allmänna anrop till ARM</span><span class="sxs-lookup"><span data-stu-id="73fd4-2727">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="73fd4-2728">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73fd4-2728">Az.Sql</span></span>
* <span data-ttu-id="73fd4-2729">Cmdlet-parametern (ExcludeDetectionType) för Hotidentifiering ändrades från DetectionType till sträng[] för att framtidssäkra den när nya DetectionTypes läggs till, och även för att stödja automatisk ifyllning.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2729">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="73fd4-2730">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="73fd4-2730">Az.Storage</span></span>
* <span data-ttu-id="73fd4-2731">Stöd för att hämta/ange/ta bort hanteringsprincip på ett lagringskonto</span><span class="sxs-lookup"><span data-stu-id="73fd4-2731">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="73fd4-2732">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="73fd4-2732">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="73fd4-2733">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="73fd4-2733">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="73fd4-2734">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="73fd4-2734">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="73fd4-2735">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="73fd4-2735">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="73fd4-2736">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="73fd4-2736">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="73fd4-2737">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="73fd4-2737">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="73fd4-2738">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="73fd4-2738">Az.Websites</span></span>
* <span data-ttu-id="73fd4-2739">Åtgärda fel med ARM-mall som avbryter kloning av alla platser med 'New-AzWebApp -IncludeSourceWebAppSlots'</span><span class="sxs-lookup"><span data-stu-id="73fd4-2739">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="73fd4-2740">1.5.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="73fd4-2740">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="73fd4-2741">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73fd4-2741">Az.Accounts</span></span>
* <span data-ttu-id="73fd4-2742">Lägg till kommandot Register-AzModule för stöd för AutoRest-genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="73fd4-2742">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="73fd4-2743">Uppdatera exempel för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="73fd4-2743">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="73fd4-2744">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="73fd4-2744">Az.Automation</span></span>
* <span data-ttu-id="73fd4-2745">Problem med att hämta vissa månadsscheman i flera Azure Automation-cmdletar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="73fd4-2745">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="73fd4-2746">Åtgärda problem med att Get-AzAutomationDscNode bara returnerar de 20 översta noderna.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2746">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="73fd4-2747">Nu returneras alla noder</span><span class="sxs-lookup"><span data-stu-id="73fd4-2747">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="73fd4-2748">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="73fd4-2748">Az.Cdn</span></span>
* <span data-ttu-id="73fd4-2749">Nya Powershell-cmdletar för att aktivera/inaktivera anpassade domän-HTTPS har lagts till och de gamla har gjorts inaktuella</span><span class="sxs-lookup"><span data-stu-id="73fd4-2749">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73fd4-2750">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73fd4-2750">Az.Compute</span></span>
* <span data-ttu-id="73fd4-2751">Lägg till stöd för jokertecken för Get-cmdletar</span><span class="sxs-lookup"><span data-stu-id="73fd4-2751">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="73fd4-2752">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="73fd4-2752">Az.DataFactory</span></span>
* <span data-ttu-id="73fd4-2753">ADF .Net SDK-versionen har uppdaterats till 3.0.1</span><span class="sxs-lookup"><span data-stu-id="73fd4-2753">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="73fd4-2754">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="73fd4-2754">Az.LogicApp</span></span>
* <span data-ttu-id="73fd4-2755">Åtgärda problemet med att ListWorkflows endast hämtar den första sidan med resultat</span><span class="sxs-lookup"><span data-stu-id="73fd4-2755">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73fd4-2756">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73fd4-2756">Az.Network</span></span>
* <span data-ttu-id="73fd4-2757">Lägg till stöd för jokertecken för Network-cmdletar</span><span class="sxs-lookup"><span data-stu-id="73fd4-2757">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="73fd4-2758">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="73fd4-2758">Az.RecoveryServices</span></span>
* <span data-ttu-id="73fd4-2759">Stöd har lagts till för SQL Server i virtuella Azure-datorer</span><span class="sxs-lookup"><span data-stu-id="73fd4-2759">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="73fd4-2760">SDK-uppdatering</span><span class="sxs-lookup"><span data-stu-id="73fd4-2760">SDK Update</span></span>
* <span data-ttu-id="73fd4-2761">Get-ProtectableItem-incheckning i VMappContainer har tagits bort</span><span class="sxs-lookup"><span data-stu-id="73fd4-2761">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="73fd4-2762">Name och ServerName har lagts till som parametrar för Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="73fd4-2762">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="73fd4-2763">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73fd4-2763">Az.Resources</span></span>
* <span data-ttu-id="73fd4-2764">Lägg till parametern `-TemplateObject` i cmdletar för distribution</span><span class="sxs-lookup"><span data-stu-id="73fd4-2764">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="73fd4-2765">Mer information här: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="73fd4-2765">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="73fd4-2766">Åtgärda problem med piping av resultatet i `Get-AzResource` till `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="73fd4-2766">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="73fd4-2767">Mer information här: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="73fd4-2767">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="73fd4-2768">Åtgärda problem med ändring av JSON-datatyp när `Set-AzResource` körs</span><span class="sxs-lookup"><span data-stu-id="73fd4-2768">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="73fd4-2769">Mer information här: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="73fd4-2769">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="73fd4-2770">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73fd4-2770">Az.Sql</span></span>
* <span data-ttu-id="73fd4-2771">AuditingEndpointsCommunicator uppdateras.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2771">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="73fd4-2772">Åtgärdar beteendet hos ett gränsscenario när nya diagnostikinställningar skapas.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2772">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="73fd4-2773">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="73fd4-2773">Az.Storage</span></span>
* <span data-ttu-id="73fd4-2774">Stöd för BlockBlobStorage när Storage-konto skapas      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="73fd4-2774">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="73fd4-2775">1.4.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="73fd4-2775">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="73fd4-2776">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="73fd4-2776">Az.AnalysisServices</span></span>
* <span data-ttu-id="73fd4-2777">Inaktuell AddAzureASAccount-cmdlet</span><span class="sxs-lookup"><span data-stu-id="73fd4-2777">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="73fd4-2778">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="73fd4-2778">Az.Automation</span></span>
* <span data-ttu-id="73fd4-2779">Hjälpen för Import-AzAutomationDscNodeConfiguration har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="73fd4-2779">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="73fd4-2780">Konfigurationsnamnsvalidering har lagts till i cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="73fd4-2780">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="73fd4-2781">Förbättrad felhantering för cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="73fd4-2781">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="73fd4-2782">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="73fd4-2782">Az.CognitiveServices</span></span>
* <span data-ttu-id="73fd4-2783">CustomSubdomainName har lagts till som en ny valfri parameter för New-AzCognitiveServicesAccount, som används för att ange underdomän för resursen.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2783">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73fd4-2784">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73fd4-2784">Az.Compute</span></span>
* <span data-ttu-id="73fd4-2785">Problemet med ID-parameteruppsättningar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="73fd4-2785">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="73fd4-2786">Get-AzVMExtension har uppdaterats så att alla installerade tillägg visas om parametern Name inte har angetts</span><span class="sxs-lookup"><span data-stu-id="73fd4-2786">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="73fd4-2787">Parametrarna Tag och ResourceId har lagts till i cmdleten Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="73fd4-2787">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="73fd4-2788">Get-AzVmssVM utan instans-ID och med InstanceView kan visa virtuella VMSS-datorer med instansvyn.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2788">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="73fd4-2789">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="73fd4-2789">Az.DataLakeStore</span></span>
* <span data-ttu-id="73fd4-2790">Cmdletar har lagts till för uppräkning och återställning av borttagna objekt i ADL</span><span class="sxs-lookup"><span data-stu-id="73fd4-2790">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="73fd4-2791">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="73fd4-2791">Az.EventHub</span></span>
* <span data-ttu-id="73fd4-2792">Ny boolesk egenskap SkipEmptyArchives har lagts till i Skip Empty Archives i CaptureDescription-klassen i Eventhub</span><span class="sxs-lookup"><span data-stu-id="73fd4-2792">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="73fd4-2793">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="73fd4-2793">Az.KeyVault</span></span>
* <span data-ttu-id="73fd4-2794">Taggning i Set-AzKeyVaultSecret har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="73fd4-2794">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="73fd4-2795">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="73fd4-2795">Az.LogicApp</span></span>
* <span data-ttu-id="73fd4-2796">Grundläggande SKU har lagts till för Integrationskonton</span><span class="sxs-lookup"><span data-stu-id="73fd4-2796">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="73fd4-2797">XSLT 2.0, XSLT 3.0 och Flytande mappningstyper har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-2797">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="73fd4-2798">Nya cmdletar för integrationskontosammansättningar</span><span class="sxs-lookup"><span data-stu-id="73fd4-2798">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="73fd4-2799">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="73fd4-2799">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="73fd4-2800">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="73fd4-2800">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="73fd4-2801">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="73fd4-2801">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="73fd4-2802">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="73fd4-2802">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="73fd4-2803">Nya cmdletar för batchkonfiguration för integrationskonto</span><span class="sxs-lookup"><span data-stu-id="73fd4-2803">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="73fd4-2804">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="73fd4-2804">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="73fd4-2805">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="73fd4-2805">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="73fd4-2806">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="73fd4-2806">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="73fd4-2807">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="73fd4-2807">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="73fd4-2808">Logic App-SDK har uppdaterats till version 4.1.0</span><span class="sxs-lookup"><span data-stu-id="73fd4-2808">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="73fd4-2809">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="73fd4-2809">Az.Monitor</span></span>
* <span data-ttu-id="73fd4-2810">Hjälpen för Get-AzMetric har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="73fd4-2810">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73fd4-2811">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73fd4-2811">Az.Network</span></span>
* <span data-ttu-id="73fd4-2812">Hjälpexempel för Add-AzApplicationGatewayCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-2812">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="73fd4-2813">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="73fd4-2813">Az.OperationalInsights</span></span>
* <span data-ttu-id="73fd4-2814">Ytterligare stöd för datakällorna New och Get ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2814">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="73fd4-2815">Ny ApplicationInsights-typ har lagts till för att ge stöd för ”Get specific” och ”Get all” för ApplicationInsights-datakällor för angiven arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2815">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="73fd4-2816">Cmdleten New-AzOperationalInsightsApplicationInsightsDataSource har lagts till för att skapa datakälla med angivna parametrar för Application Insights-resurs: subscription Id, resourceGroupName och name.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2816">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="73fd4-2817">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73fd4-2817">Az.Resources</span></span>
* <span data-ttu-id="73fd4-2818">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="73fd4-2818">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="73fd4-2819">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="73fd4-2819">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="73fd4-2820">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="73fd4-2820">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="73fd4-2821">Fel som gör att KeyCredentials inte kan skapas upprepade gånger har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="73fd4-2821">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="73fd4-2822">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73fd4-2822">Az.Sql</span></span>
* <span data-ttu-id="73fd4-2823">Lägg till stöd för hyperskalanivån för SQL DB</span><span class="sxs-lookup"><span data-stu-id="73fd4-2823">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="73fd4-2824">Ett fel har åtgärdats där återställningen kunde misslyckas på grund av onödiga inställningsegenskaper i restore-förfrågan</span><span class="sxs-lookup"><span data-stu-id="73fd4-2824">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="73fd4-2825">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="73fd4-2825">Az.Websites</span></span>
* <span data-ttu-id="73fd4-2826">Rätt exempel i Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="73fd4-2826">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="73fd4-2827">1.3.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="73fd4-2827">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="73fd4-2828">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73fd4-2828">Az.Accounts</span></span>
* <span data-ttu-id="73fd4-2829">Uppdatera till den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="73fd4-2829">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="73fd4-2830">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="73fd4-2830">Az.AnalysisServices</span></span>
<span data-ttu-id="73fd4-2831">Allmän tillgänglighet för Az.AnalysisServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2831">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73fd4-2832">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73fd4-2832">Az.Compute</span></span>
* <span data-ttu-id="73fd4-2833">AEM-tillägg: Lägg till stöd för UltraSSD-, P60-, P70- och P80-diskar</span><span class="sxs-lookup"><span data-stu-id="73fd4-2833">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="73fd4-2834">Uppdatera hjälpbeskrivning för Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="73fd4-2834">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="73fd4-2835">Uppdatera hjälpbeskrivning och exempel för Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="73fd4-2835">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="73fd4-2836">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="73fd4-2836">Az.RecoveryServices</span></span>
<span data-ttu-id="73fd4-2837">Allmän tillgänglighet för Az.RecoveryServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2837">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="73fd4-2838">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73fd4-2838">Az.Resources</span></span>
* <span data-ttu-id="73fd4-2839">Korrigera taggar för resursgrupper</span><span class="sxs-lookup"><span data-stu-id="73fd4-2839">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="73fd4-2840">Mer information här: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="73fd4-2840">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="73fd4-2841">Åtgärda problem där `Get-AzureRmRoleAssignment` inte respekterar -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="73fd4-2841">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="73fd4-2842">Mer information här: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="73fd4-2842">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="73fd4-2843">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73fd4-2843">Az.Sql</span></span>
* <span data-ttu-id="73fd4-2844">Lägga till Get/Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="73fd4-2844">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="73fd4-2845">Åtgärda problem där ett nullref-undantag uppstår när du kör SQL-cmdletar och inte är inloggad på ett Azure-konto</span><span class="sxs-lookup"><span data-stu-id="73fd4-2845">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="73fd4-2846">Åtgärda nullref-undantag i Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="73fd4-2846">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="73fd4-2847">1.2.1 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="73fd4-2847">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="73fd4-2848">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73fd4-2848">Az.Accounts</span></span>
* <span data-ttu-id="73fd4-2849">Version med rätt version av autentisering</span><span class="sxs-lookup"><span data-stu-id="73fd4-2849">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="73fd4-2850">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="73fd4-2850">Az.AnalysisServices</span></span>
* <span data-ttu-id="73fd4-2851">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="73fd4-2851">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="73fd4-2852">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="73fd4-2852">Az.RecoveryServices</span></span>
* <span data-ttu-id="73fd4-2853">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="73fd4-2853">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="73fd4-2854">1.2.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="73fd4-2854">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="73fd4-2855">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73fd4-2855">Az.Accounts</span></span>
* <span data-ttu-id="73fd4-2856">Lägga till interaktiv autentisering och autentisering med användarnamn/lösenord för endast Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="73fd4-2856">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="73fd4-2857">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="73fd4-2857">Update incorrect online help URLs</span></span>
* <span data-ttu-id="73fd4-2858">Lägga till varningsmeddelande i PS Core för Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="73fd4-2858">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="73fd4-2859">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="73fd4-2859">Az.Aks</span></span>
* <span data-ttu-id="73fd4-2860">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="73fd4-2860">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="73fd4-2861">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="73fd4-2861">Az.Automation</span></span>
* <span data-ttu-id="73fd4-2862">Stöd för Python 2-runbookflöden har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-2862">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="73fd4-2863">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="73fd4-2863">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="73fd4-2864">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="73fd4-2864">Az.Cdn</span></span>
* <span data-ttu-id="73fd4-2865">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="73fd4-2865">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73fd4-2866">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73fd4-2866">Az.Compute</span></span>
* <span data-ttu-id="73fd4-2867">Lägga till cmdleten Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="73fd4-2867">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="73fd4-2868">Lägga till TempDisk-parameter i Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="73fd4-2868">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="73fd4-2869">Korrigera varningsmeddelande för New-AzVM</span><span class="sxs-lookup"><span data-stu-id="73fd4-2869">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="73fd4-2870">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="73fd4-2870">Az.ContainerRegistry</span></span>
* <span data-ttu-id="73fd4-2871">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="73fd4-2871">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="73fd4-2872">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="73fd4-2872">Az.DataFactory</span></span>
* <span data-ttu-id="73fd4-2873">ADF .Net SDK-versionen har uppdaterats till 3.0.0</span><span class="sxs-lookup"><span data-stu-id="73fd4-2873">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="73fd4-2874">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="73fd4-2874">Az.DataLakeStore</span></span>
* <span data-ttu-id="73fd4-2875">Åtgärda problem med ADLS-slutpunkt vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="73fd4-2875">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="73fd4-2876">Mer information här: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="73fd4-2876">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="73fd4-2877">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="73fd4-2877">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="73fd4-2878">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="73fd4-2878">Az.IotHub</span></span>
* <span data-ttu-id="73fd4-2879">Lägga till kodningsformat i cmdleten Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2879">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="73fd4-2880">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="73fd4-2880">Az.KeyVault</span></span>
* <span data-ttu-id="73fd4-2881">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="73fd4-2881">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73fd4-2882">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73fd4-2882">Az.Network</span></span>
* <span data-ttu-id="73fd4-2883">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="73fd4-2883">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="73fd4-2884">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73fd4-2884">Az.Resources</span></span>
* <span data-ttu-id="73fd4-2885">Åtgärda felaktiga exempel i referensdokumentationen ”New-AzADAppCredential” och ”New-AzADSpCredential”</span><span class="sxs-lookup"><span data-stu-id="73fd4-2885">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="73fd4-2886">Åtgärda problem där sökvägen för parametern ”-TemplateFile” inte omvandlas innan cmdletarna för distribution i resursgruppen körs</span><span class="sxs-lookup"><span data-stu-id="73fd4-2886">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="73fd4-2887">Az.Resources: Korrigera dokumentationen om standardvärdet för New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="73fd4-2887">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="73fd4-2888">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="73fd4-2888">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="73fd4-2889">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="73fd4-2889">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="73fd4-2890">Åtgärda formateringsproblemet med objektet ”PSResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="73fd4-2890">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="73fd4-2891">Mer information här: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="73fd4-2891">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="73fd4-2892">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="73fd4-2892">Az.ServiceFabric</span></span>
* <span data-ttu-id="73fd4-2893">Återställ när ett certifikat läggs till i en Virtual Machine Scale Sets-modell men ett undantag genereras. Detta har gjorts för att åtgärda följande fel: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="73fd4-2893">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="73fd4-2894">Korrigera några felmeddelanden.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2894">Fix some error messages.</span></span>
* <span data-ttu-id="73fd4-2895">Korrigering av skapande av kluster med ARM-mall som är standard för New-AzServiceFabriCluster som inte fungerade med migrering till Az.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2895">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="73fd4-2896">Korrigering av tilläggning av kluster/programcertifikat så att endast VM Scale Sets som motsvarar klustret läggs till genom att kontrollera ID för klustret i tillägget.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2896">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="73fd4-2897">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="73fd4-2897">Az.SignalR</span></span>
* <span data-ttu-id="73fd4-2898">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="73fd4-2898">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="73fd4-2899">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73fd4-2899">Az.Sql</span></span>
* <span data-ttu-id="73fd4-2900">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="73fd4-2900">Update incorrect online help URLs</span></span>
* <span data-ttu-id="73fd4-2901">Uppdaterad parameterbeskrivning för LicenseType-parameter med möjliga värden</span><span class="sxs-lookup"><span data-stu-id="73fd4-2901">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="73fd4-2902">Korrigering för att uppdatera hanterad instansidentitet som inte fungerar när det är den enda uppdaterade egenskapen</span><span class="sxs-lookup"><span data-stu-id="73fd4-2902">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="73fd4-2903">Stöd för anpassad sortering på hanterad instans</span><span class="sxs-lookup"><span data-stu-id="73fd4-2903">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="73fd4-2904">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="73fd4-2904">Az.Storage</span></span>
* <span data-ttu-id="73fd4-2905">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="73fd4-2905">Update incorrect online help URLs</span></span>
* <span data-ttu-id="73fd4-2906">Tillhandahåll detaljerat felmeddelande när en användare försöker hämta/konfigurera klassisk loggning/mått på ett Premium Storage-konto eftersom Premium Storage-kontot inte har stöd för klassisk loggning/mått.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2906">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="73fd4-2907">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="73fd4-2907">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="73fd4-2908">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="73fd4-2908">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="73fd4-2909">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="73fd4-2909">Az.TrafficManager</span></span>
* <span data-ttu-id="73fd4-2910">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="73fd4-2910">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="73fd4-2911">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="73fd4-2911">Az.Websites</span></span>
* <span data-ttu-id="73fd4-2912">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="73fd4-2912">Update incorrect online help URLs</span></span>
* <span data-ttu-id="73fd4-2913">Korrigerar ”New-AzWebAppSSLBinding” så att certifikatet laddas upp till rätt resursgrupp och plats om appen finns i en ASE.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2913">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="73fd4-2914">Korrigerar ”New-AzWebAppSSLBinding” så att taggarna inte skrivs över på en bindning av ett SSL-certifikat till en app</span><span class="sxs-lookup"><span data-stu-id="73fd4-2914">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="73fd4-2915">1.1.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="73fd4-2915">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="73fd4-2916">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73fd4-2916">Az.Accounts</span></span>
* <span data-ttu-id="73fd4-2917">Lade till omfattningen ”Lokal” till Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="73fd4-2917">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73fd4-2918">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73fd4-2918">Az.Compute</span></span>
* <span data-ttu-id="73fd4-2919">Namn är nu valfritt i ID-parametern för Restart/Start/Stop/Remove/Set-AzVM och Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="73fd4-2919">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="73fd4-2920">Uppdaterade beskrivningen av ID i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="73fd4-2920">Updated the description of ID in help files</span></span>
* <span data-ttu-id="73fd4-2921">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73fd4-2921">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="73fd4-2922">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="73fd4-2922">Az.DataLakeStore</span></span>
* <span data-ttu-id="73fd4-2923">Uppdatera sdk-versionen av dataplanet till 1.1.14 för SDK-korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2923">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="73fd4-2924">Korrigerade hanteringen av negativ accesstime och modificationtime för getfilestatus och liststatus; korrigera asynkront annulleringstoken</span><span class="sxs-lookup"><span data-stu-id="73fd4-2924">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="73fd4-2925">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="73fd4-2925">Az.EventGrid</span></span>
* <span data-ttu-id="73fd4-2926">Uppdaterat för användning av API-versionen 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2926">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="73fd4-2927">Uppdaterade följande cmdletar för att stödja nytt scenario i API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="73fd4-2927">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="73fd4-2928">New-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="73fd4-2928">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="73fd4-2929">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="73fd4-2929">Event Time-To-Live,</span></span>
        - <span data-ttu-id="73fd4-2930">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="73fd4-2930">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="73fd4-2931">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2931">Dead letter endpoint.</span></span>
    - <span data-ttu-id="73fd4-2932">Update-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="73fd4-2932">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="73fd4-2933">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="73fd4-2933">Event Time-To-Live,</span></span>
        - <span data-ttu-id="73fd4-2934">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="73fd4-2934">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="73fd4-2935">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2935">Dead letter endpoint.</span></span>
* <span data-ttu-id="73fd4-2936">Lade till nya enum-värden (storageQueue och hybridConnection) för alternativet EndpointType i cmdletarna New-AzureRmEventGridSubscription och Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2936">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="73fd4-2937">Visa varningsmeddelanden om skapande eller uppdatering av händelseprenumerationen förväntas medföra manuell åtgärd från användaren.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2937">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="73fd4-2938">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="73fd4-2938">Az.IotHub</span></span>
* <span data-ttu-id="73fd4-2939">Har uppdaterats till den senaste versionen av SDK:n lotHub</span><span class="sxs-lookup"><span data-stu-id="73fd4-2939">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="73fd4-2940">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="73fd4-2940">Az.LogicApp</span></span>
* <span data-ttu-id="73fd4-2941">Get-AzLogicApp visar en lista över alla som inte har angivet namn</span><span class="sxs-lookup"><span data-stu-id="73fd4-2941">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="73fd4-2942">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73fd4-2942">Az.Resources</span></span>
* <span data-ttu-id="73fd4-2943">Åtgärdade problem med parameteruppsättningen när parametrarna -ODataQuery och -ResourceId anges för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="73fd4-2943">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="73fd4-2944">Mer information här: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="73fd4-2944">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="73fd4-2945">Åtgärdade hantering av parametern -Custom i New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="73fd4-2945">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="73fd4-2946">Korrigerade stavfel i New-AzDeployment-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="73fd4-2946">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="73fd4-2947">Gjorde parametern -MailNickname obligatorisk för New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="73fd4-2947">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="73fd4-2948">Mer information här: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="73fd4-2948">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="73fd4-2949">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="73fd4-2949">Az.SignalR</span></span>
* <span data-ttu-id="73fd4-2950">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73fd4-2950">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="73fd4-2951">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73fd4-2951">Az.Sql</span></span>
* <span data-ttu-id="73fd4-2952">Konverterade lagringshanteringsklientens beroende av den normala SDK-implementeringen.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2952">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="73fd4-2953">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="73fd4-2953">Az.Storage</span></span>
* <span data-ttu-id="73fd4-2954">Angav StorageAccountName för lagringskontext som det verkliga namnet på lagringskontot när det skapas med Sas Token, OAuth eller Anonymous</span><span class="sxs-lookup"><span data-stu-id="73fd4-2954">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="73fd4-2955">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="73fd4-2955">New-AzStorageContext</span></span>
* <span data-ttu-id="73fd4-2956">Skapade Sas Token för Blob Snapshot-objekt med parametern -FullUri, åtgärdade den returnerade URI:n så att den blir URI för ögonblicksbild</span><span class="sxs-lookup"><span data-stu-id="73fd4-2956">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="73fd4-2957">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="73fd4-2957">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="73fd4-2958">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="73fd4-2958">Az.Websites</span></span>
* <span data-ttu-id="73fd4-2959">Åtgärdade en bugg i datumparsningen i Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="73fd4-2959">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="73fd4-2960">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73fd4-2960">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="73fd4-2961">1.0.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="73fd4-2961">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="73fd4-2962">Allmänt</span><span class="sxs-lookup"><span data-stu-id="73fd4-2962">General</span></span>

- <span data-ttu-id="73fd4-2963">Allmän tillgänglighet för Az-modulen</span><span class="sxs-lookup"><span data-stu-id="73fd4-2963">General Availability of Az Module</span></span>
- <span data-ttu-id="73fd4-2964">Onlinehjälp för varje modul</span><span class="sxs-lookup"><span data-stu-id="73fd4-2964">Online help for each module</span></span>
- <span data-ttu-id="73fd4-2965">Mer information och en översikt finns på [Az-informationssidan](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="73fd4-2965">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="73fd4-2966">Information om hur du migrerar från AzureRM finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="73fd4-2966">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="73fd4-2967">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73fd4-2967">Az.Accounts</span></span>
- <span data-ttu-id="73fd4-2968">Har ändrats från Az.Profile</span><span class="sxs-lookup"><span data-stu-id="73fd4-2968">Changed from Az.Profile</span></span>
- <span data-ttu-id="73fd4-2969">Fasta tabellformat för profil- och kontexttyper</span><span class="sxs-lookup"><span data-stu-id="73fd4-2969">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="73fd4-2970">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="73fd4-2970">Az.ApiManagement</span></span>
- <span data-ttu-id="73fd4-2971">Korrigeringar för #7002</span><span class="sxs-lookup"><span data-stu-id="73fd4-2971">Fixes for #7002</span></span>
- <span data-ttu-id="73fd4-2972">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="73fd4-2972">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="73fd4-2973">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="73fd4-2973">Az.Batch</span></span>
- <span data-ttu-id="73fd4-2974">Lade till möjligheten att se vilken version av Azure Batch Node Agent som körs på var och en av de virtuella datorerna i en pool, via den nya egenskapen `NodeAgentInformation` på `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2974">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="73fd4-2975">Standarden `Caching` för `PSDataDisk` är nu `ReadWrite` i stället för `None`.</span><span class="sxs-lookup"><span data-stu-id="73fd4-2975">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="73fd4-2976">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="73fd4-2976">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="73fd4-2977">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="73fd4-2977">Az.Billing</span></span>
- <span data-ttu-id="73fd4-2978">Kombinerar cmdletarna för fakturering, förbrukning och UsageAggregates. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="73fd4-2978">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="73fd4-2979">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="73fd4-2979">Az.CognitivServices</span></span>
- <span data-ttu-id="73fd4-2980">Lade till kompletterare för SkuName och Typem som är tillgängliga i New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="73fd4-2980">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="73fd4-2981">Tog bort parameteruppsättningen GetSkusWithAccountParamSetName från Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="73fd4-2981">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="73fd4-2982">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="73fd4-2982">Az.ContainerInstance</span></span>
- <span data-ttu-id="73fd4-2983">Stöd för ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="73fd4-2983">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="73fd4-2984">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="73fd4-2984">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="73fd4-2985">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="73fd4-2985">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="73fd4-2986">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="73fd4-2986">Az.DataLakeStore</span></span>
- <span data-ttu-id="73fd4-2987">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="73fd4-2987">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="73fd4-2988">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="73fd4-2988">Az.Monitor</span></span>
- <span data-ttu-id="73fd4-2989">Döpte om Az.Insights till Az.Monitor och andra mindre icke-bakåtkompatibla ändringar. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="73fd4-2989">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="73fd4-2990">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="73fd4-2990">Az.KeyVault</span></span>
- <span data-ttu-id="73fd4-2991">Tog bort den inaktuella egenskapen PurgeDisabled från utdatatyper</span><span class="sxs-lookup"><span data-stu-id="73fd4-2991">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="73fd4-2992">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="73fd4-2992">Az.MachineLearning</span></span>
- <span data-ttu-id="73fd4-2993">Inkluderade cmdletarna från modulen Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="73fd4-2993">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="73fd4-2994">Az.Media</span><span class="sxs-lookup"><span data-stu-id="73fd4-2994">Az.Media</span></span>
- <span data-ttu-id="73fd4-2995">Tog bort inaktuella -Tags-alias från New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="73fd4-2995">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="73fd4-2996">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73fd4-2996">Az.Network</span></span>
<span data-ttu-id="73fd4-2997">Stöd har lagts till för konfiguration av RewriteRuleSets i Application Gateway</span><span class="sxs-lookup"><span data-stu-id="73fd4-2997">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="73fd4-2998">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="73fd4-2998">New cmdlets added:</span></span>
        - <span data-ttu-id="73fd4-2999">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="73fd4-2999">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="73fd4-3000">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="73fd4-3000">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="73fd4-3001">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="73fd4-3001">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="73fd4-3002">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="73fd4-3002">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="73fd4-3003">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="73fd4-3003">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="73fd4-3004">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="73fd4-3004">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="73fd4-3005">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="73fd4-3005">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="73fd4-3006">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="73fd4-3006">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="73fd4-3007">Cmdletar har uppdaterats med den valfria parametern -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="73fd4-3007">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="73fd4-3008">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="73fd4-3008">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="73fd4-3009">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="73fd4-3009">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="73fd4-3010">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="73fd4-3010">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="73fd4-3011">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="73fd4-3011">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="73fd4-3012">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="73fd4-3012">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="73fd4-3013">New-AzureRmApplicationGatewayUrlPathMapConfig har lagt till KeyVault-stöd för Application Gateway med Identity.</span><span class="sxs-lookup"><span data-stu-id="73fd4-3013">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="73fd4-3014">Cmdletar har uppdaterats med den valfria parametern -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="73fd4-3014">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="73fd4-3015">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="73fd4-3015">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="73fd4-3016">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="73fd4-3016">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="73fd4-3017">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="73fd4-3017">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="73fd4-3018">Cmdleten New-AzApplicationGateway har uppdaterats med den valfria parametern -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="73fd4-3018">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="73fd4-3019">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="73fd4-3019">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="73fd4-3020">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="73fd4-3020">Az.OperationalInsights</span></span>
- <span data-ttu-id="73fd4-3021">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="73fd4-3021">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="73fd4-3022">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="73fd4-3022">Az.Profile</span></span>
- <span data-ttu-id="73fd4-3023">Modulnamnet har ändrats till Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73fd4-3023">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="73fd4-3024">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="73fd4-3024">Az.RecoveryServices</span></span>
- <span data-ttu-id="73fd4-3025">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="73fd4-3025">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="73fd4-3026">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73fd4-3026">Az.Resources</span></span>
- <span data-ttu-id="73fd4-3027">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="73fd4-3027">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="73fd4-3028">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="73fd4-3028">Az.ServiceFabric</span></span>
- <span data-ttu-id="73fd4-3029">Stöd för specificering av certifikat efter eget namn och tumavtryck</span><span class="sxs-lookup"><span data-stu-id="73fd4-3029">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="73fd4-3030">Information om fler icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="73fd4-3030">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="73fd4-3031">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="73fd4-3031">Az.SIgnalR</span></span>
- <span data-ttu-id="73fd4-3032">Allmän tillgänglighet för PowerShell-cmdletar för SIgnalR</span><span class="sxs-lookup"><span data-stu-id="73fd4-3032">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="73fd4-3033">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73fd4-3033">Az.Sql</span></span>
- <span data-ttu-id="73fd4-3034">Lade till de nya identifieringstyperna Data_Exfiltration och Unsafe_Action i Threat Detection-cmdletar</span><span class="sxs-lookup"><span data-stu-id="73fd4-3034">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="73fd4-3035">Uppdaterade dokumentationsexempel för Sql Auditing-cmdletar</span><span class="sxs-lookup"><span data-stu-id="73fd4-3035">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="73fd4-3036">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="73fd4-3036">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="73fd4-3037">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="73fd4-3037">Az.Storage</span></span>
- <span data-ttu-id="73fd4-3038">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="73fd4-3038">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="73fd4-3039">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="73fd4-3039">Az.Websites</span></span>
- <span data-ttu-id="73fd4-3040">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="73fd4-3040">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="73fd4-3041">0.7.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="73fd4-3041">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="73fd4-3042">Allmänt</span><span class="sxs-lookup"><span data-stu-id="73fd4-3042">General</span></span>

* <span data-ttu-id="73fd4-3043">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="73fd4-3043">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="73fd4-3044">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73fd4-3044">Az.Compute</span></span>

* <span data-ttu-id="73fd4-3045">Lade till stöd för UltraSSD och Galleriavbildningar i de enkla parameteruppsättningarna för `New-AzVm(ss)`-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="73fd4-3045">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="73fd4-3046">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="73fd4-3046">Az.DataLakeStore</span></span>

* <span data-ttu-id="73fd4-3047">Åtgärdade avslutande snedstreck i domänen för adls-konto</span><span class="sxs-lookup"><span data-stu-id="73fd4-3047">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="73fd4-3048">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="73fd4-3048">Az.FrontDoor</span></span>

* <span data-ttu-id="73fd4-3049">Brutna länkar korrigerades</span><span class="sxs-lookup"><span data-stu-id="73fd4-3049">Fixed some broken links</span></span>
    - <span data-ttu-id="73fd4-3050">I artiklarna New-AzureRmFrontDoor och Set-AzureRmFrontDoor artiklar korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="73fd4-3050">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="73fd4-3051">I artikeln New-AzureRmFrontDoorManagedRuleObject korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="73fd4-3051">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="73fd4-3052">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="73fd4-3052">Az.RecoveryServices</span></span>

* <span data-ttu-id="73fd4-3053">Lade till valideringar på klientsidan för Azure-filresurs med återställningsåtgärder.</span><span class="sxs-lookup"><span data-stu-id="73fd4-3053">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="73fd4-3054">Gjorde storageAccountName och storageAccountResourceGroupName valfritt för afs-återställning.</span><span class="sxs-lookup"><span data-stu-id="73fd4-3054">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="73fd4-3055">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73fd4-3055">Az.Resources</span></span>

* <span data-ttu-id="73fd4-3056">Korrigering för https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="73fd4-3056">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="73fd4-3057">Uppdaterade Get-AzureRmRoleAssignment så att prenumerationsomfattningen används om den anges vid begäran om klassiska administratörer.</span><span class="sxs-lookup"><span data-stu-id="73fd4-3057">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="73fd4-3058">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73fd4-3058">Az.Sql</span></span>

* <span data-ttu-id="73fd4-3059">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="73fd4-3059">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="73fd4-3060">Korrigerade ett problem med Get-AzureRmSqlDatabaseVulnerabilityAssessment med DotNet-kärna</span><span class="sxs-lookup"><span data-stu-id="73fd4-3060">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="73fd4-3061">Ändrade dokumentationen för hjälpmeddelanden som rör SQL Auditing-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="73fd4-3061">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="73fd4-3062">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="73fd4-3062">Az.Storage</span></span>

* <span data-ttu-id="73fd4-3063">Lade till -EnableHierarchicalNamespace i New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="73fd4-3063">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="73fd4-3064">Åtgärdade problemet med att cmdleten Copy File inte kunde återanvända källkontexten på målet om inte -DestContext angetts</span><span class="sxs-lookup"><span data-stu-id="73fd4-3064">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="73fd4-3065">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="73fd4-3065">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="73fd4-3066">Stöd för statisk webbplatskonfiguration</span><span class="sxs-lookup"><span data-stu-id="73fd4-3066">Support Static Website configuration</span></span>
    - <span data-ttu-id="73fd4-3067">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="73fd4-3067">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="73fd4-3068">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="73fd4-3068">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="73fd4-3069">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="73fd4-3069">Az.Websites</span></span>

* <span data-ttu-id="73fd4-3070">Set-AzureRmWebApp och Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="73fd4-3070">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="73fd4-3071">Ny parameter (-AzureStoragePath) har lagts till för att ange att Azure Storage-sökvägar ska monteras i containerappar i Windows och Linux.</span><span class="sxs-lookup"><span data-stu-id="73fd4-3071">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="73fd4-3072">Använder utdata från den nya cmdleten New-AzureRmWebAppAzureStoragePath som en parameter för att ange sökvägar för Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="73fd4-3072">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="73fd4-3073">0.6.1 – november 2018</span><span class="sxs-lookup"><span data-stu-id="73fd4-3073">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="73fd4-3074">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="73fd4-3074">Az.ApiManagement</span></span>
* <span data-ttu-id="73fd4-3075">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="73fd4-3075">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="73fd4-3076">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="73fd4-3076">Az.Automation</span></span>
* <span data-ttu-id="73fd4-3077">Swagger baserade Azure Automation-cmdletar</span><span class="sxs-lookup"><span data-stu-id="73fd4-3077">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="73fd4-3078">Cmdletar för Uppdateringshantering har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-3078">Added Update Management cmdlets</span></span>
* <span data-ttu-id="73fd4-3079">Cmdletar för källkontroll har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-3079">Added Source Control cmdlets</span></span>
* <span data-ttu-id="73fd4-3080">Remove-AzureRmAutomationHybridWorkerGroup-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-3080">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="73fd4-3081">Kommandot för DSC-registreringsnod har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="73fd4-3081">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="73fd4-3082">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73fd4-3082">Az.Compute</span></span>
* <span data-ttu-id="73fd4-3083">Problem med SystemAssigned-identitet har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="73fd4-3083">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="73fd4-3084">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="73fd4-3084">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="73fd4-3085">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="73fd4-3085">Az.ContainerInstance</span></span>
* <span data-ttu-id="73fd4-3086">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="73fd4-3086">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="73fd4-3087">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="73fd4-3087">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="73fd4-3088">uppdatera exempelbeskrivningen för marketplace-cmdletar</span><span class="sxs-lookup"><span data-stu-id="73fd4-3088">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="73fd4-3089">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73fd4-3089">Az.Network</span></span>
* <span data-ttu-id="73fd4-3090">Cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomErreller Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-3090">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="73fd4-3091">ICMP tillbaka till stöd för Azure Firewall-nätverksprotokoll har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-3091">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="73fd4-3092">Uppdatera cmdlet Test-AzureRmNetworkWatcherConnectivity, lägga till verifiering av mål-id, adress och port.</span><span class="sxs-lookup"><span data-stu-id="73fd4-3092">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="73fd4-3093">Åtgärda problem med minnesanvändning i VirtualNetwork-karta</span><span class="sxs-lookup"><span data-stu-id="73fd4-3093">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="73fd4-3094">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="73fd4-3094">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="73fd4-3095">Åtgärda för att ändra principen för en skyddad fildelning.</span><span class="sxs-lookup"><span data-stu-id="73fd4-3095">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="73fd4-3096">Tidszonsprincipen har konverterats till versaler.</span><span class="sxs-lookup"><span data-stu-id="73fd4-3096">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="73fd4-3097">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="73fd4-3097">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="73fd4-3098">Exempel i New-AzureRmRecoveryServicesAsrProtectableItem har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="73fd4-3098">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="73fd4-3099">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="73fd4-3099">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="73fd4-3100">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="73fd4-3100">Az.Relay</span></span>
* <span data-ttu-id="73fd4-3101">Valfri parameter -KeyValue till New-AzureRmRelayKey cmdlet har lagts till, vilket gör det möjligt för användare att tillhandahålla KeyValue.</span><span class="sxs-lookup"><span data-stu-id="73fd4-3101">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="73fd4-3102">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73fd4-3102">Az.Resources</span></span>
* <span data-ttu-id="73fd4-3103">Uppdatera hjälpdokumentation för resursidentitet kopplad till parametrar i `New-AzureRmPolicyAssignment` och `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="73fd4-3103">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="73fd4-3104">Lägg till ett exempel för New-AzureRmPolicyDefinition som använder -Metadata</span><span class="sxs-lookup"><span data-stu-id="73fd4-3104">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="73fd4-3105">Korrigera så att skiftläge behålls i taggnycklar i NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="73fd4-3105">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="73fd4-3106">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="73fd4-3106">Az.ServiceFabric</span></span>
* <span data-ttu-id="73fd4-3107">Lägg till utfasningsmeddelanden för kommande icke-kompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="73fd4-3107">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="73fd4-3108">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73fd4-3108">Az.Sql</span></span>
* <span data-ttu-id="73fd4-3109">Nya cmdletar för CRUD-åtgärder på Azure Sql Database-hanterad instans och Azure Sql-hanterad databas</span><span class="sxs-lookup"><span data-stu-id="73fd4-3109">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="73fd4-3110">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="73fd4-3110">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="73fd4-3111">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="73fd4-3111">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="73fd4-3112">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="73fd4-3112">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="73fd4-3113">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="73fd4-3113">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="73fd4-3114">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="73fd4-3114">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="73fd4-3115">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="73fd4-3115">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="73fd4-3116">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="73fd4-3116">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="73fd4-3117">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="73fd4-3117">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="73fd4-3118">Hantering av utökad granskningsprincip på en server eller en databas har aktiverats.</span><span class="sxs-lookup"><span data-stu-id="73fd4-3118">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="73fd4-3119">Ny parameter (PredicateExpression) har lagts till för att aktivera filtrering av granskningsloggar.</span><span class="sxs-lookup"><span data-stu-id="73fd4-3119">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="73fd4-3120">Cmdletar har ändrats så att de använder SQL-klienter i stället för äldre klienter.</span><span class="sxs-lookup"><span data-stu-id="73fd4-3120">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="73fd4-3121">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="73fd4-3121">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="73fd4-3122">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="73fd4-3122">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="73fd4-3123">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="73fd4-3123">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="73fd4-3124">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="73fd4-3124">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="73fd4-3125">Problem med att använda Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings med lagringskontots namnparameter har korrigerats</span><span class="sxs-lookup"><span data-stu-id="73fd4-3125">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="73fd4-3126">0.5.0 – november 2018</span><span class="sxs-lookup"><span data-stu-id="73fd4-3126">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="73fd4-3127">Allmänt</span><span class="sxs-lookup"><span data-stu-id="73fd4-3127">General</span></span>
* <span data-ttu-id="73fd4-3128">Lade till resurskompletterare till många kärn-cmdletar – dessa gör att du kan stega genom befintliga resursnamn med TABB vid interaktiva anrop till cmdletar</span><span class="sxs-lookup"><span data-stu-id="73fd4-3128">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="73fd4-3129">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="73fd4-3129">Az.Profile</span></span>
* <span data-ttu-id="73fd4-3130">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="73fd4-3130">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="73fd4-3131">Bytte namn på parametern TenantId i cmdleten Connect-AzAccount till Tenant och lade till ett alias för TenantId</span><span class="sxs-lookup"><span data-stu-id="73fd4-3131">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="73fd4-3132">Uppdaterade TenantId-beskrivningen för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="73fd4-3132">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="73fd4-3133">Åtgärda felmeddelande för misslyckad inloggning när du tillhandahåller klientdomän</span><span class="sxs-lookup"><span data-stu-id="73fd4-3133">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="73fd4-3134">Åtgärda problem med att kontextnamn hamnar i konflikt för konton utan prenumerationer i klientorganisationen</span><span class="sxs-lookup"><span data-stu-id="73fd4-3134">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="73fd4-3135">Åtgärda problem med DataLake-slutpunkter vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="73fd4-3135">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="73fd4-3136">Åtgärdade problem med att Disconnect-AzAccount kastades om den inte anslöts</span><span class="sxs-lookup"><span data-stu-id="73fd4-3136">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="73fd4-3137">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="73fd4-3137">Az.CognitiveServices</span></span>
* <span data-ttu-id="73fd4-3138">Lade till åtgärden Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="73fd4-3138">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73fd4-3139">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73fd4-3139">Az.Compute</span></span>
* <span data-ttu-id="73fd4-3140">Lade till cmdletarna Add-AzVmssVMDataDisk och Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="73fd4-3140">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="73fd4-3141">Get-AzVMImage visar AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="73fd4-3141">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="73fd4-3142">Åtgärdade att värdena för alternativen SetAzVMChefExtension -BootstrapOptions och -JsonAttribute inte angavs i json-format.</span><span class="sxs-lookup"><span data-stu-id="73fd4-3142">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="73fd4-3143">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="73fd4-3143">Az.DataLakeStore</span></span>
* <span data-ttu-id="73fd4-3144">Uppdatera DataLake-paketet till 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="73fd4-3144">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="73fd4-3145">Lägg till standardsamtidighet för flertrådade åtgärder.</span><span class="sxs-lookup"><span data-stu-id="73fd4-3145">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="73fd4-3146">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="73fd4-3146">Az.Insights</span></span>
* <span data-ttu-id="73fd4-3147">Åtgärdade problem #7267 (autoskalningsområde)</span><span class="sxs-lookup"><span data-stu-id="73fd4-3147">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="73fd4-3148">Problem med att uppräknade parametrar inte ställdes in ordentligt när du skapade en ny autoskalningsregel (de ställdes alltid in med standardvärdet).</span><span class="sxs-lookup"><span data-stu-id="73fd4-3148">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="73fd4-3149">Åtgärdade problem #7513 [Insights] Set-AzDiagnosticSetting kräver uttrycklig specifikation av kategorier när inställningar skapas</span><span class="sxs-lookup"><span data-stu-id="73fd4-3149">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="73fd4-3150">Nu kräver inte cmdleten uttrycklig anvisning av kategorierna för att aktiveras under skapande, d.v.s. den fungerar enligt beskrivning</span><span class="sxs-lookup"><span data-stu-id="73fd4-3150">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73fd4-3151">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73fd4-3151">Az.Network</span></span>
* <span data-ttu-id="73fd4-3152">PeeringType ändrades till en obligatorisk parameter för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="73fd4-3152">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="73fd4-3153">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="73fd4-3153">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="73fd4-3154">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="73fd4-3154">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="73fd4-3155">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="73fd4-3155">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="73fd4-3156">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="73fd4-3156">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="73fd4-3157">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="73fd4-3157">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="73fd4-3158">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="73fd4-3158">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="73fd4-3159">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="73fd4-3159">Az.PolicyInsights</span></span>
* <span data-ttu-id="73fd4-3160">Cmdletar för principreparation har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-3160">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="73fd4-3161">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73fd4-3161">Az.Resources</span></span>
* <span data-ttu-id="73fd4-3162">Korrigering för https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="73fd4-3162">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="73fd4-3163">Tillåt att resurser listas med parametern -ResourceId för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="73fd4-3163">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="73fd4-3164">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="73fd4-3164">Az.ServiceBus</span></span>
* <span data-ttu-id="73fd4-3165">Skrivskyddad MigrationState-egenskap har lagts till i PSServiceBusMigrationConfigurationAttributes, som hjälper till att hålla koll på migreringstillståndet.</span><span class="sxs-lookup"><span data-stu-id="73fd4-3165">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="73fd4-3166">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="73fd4-3166">Az.ServiceFabric</span></span>
* <span data-ttu-id="73fd4-3167">Åtgärda att lägga till certifikat till Linux-Vmss.</span><span class="sxs-lookup"><span data-stu-id="73fd4-3167">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="73fd4-3168">Åtgärdade Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="73fd4-3168">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="73fd4-3169">Använd rätt tumavtryck från nya certifikat (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="73fd4-3169">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="73fd4-3170">Visa undantag korrekt (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="73fd4-3170">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="73fd4-3171">Åtgärdade Update-AzServiceFabricDurability så att klusterkonfigurationen uppdateras innan Vmss-åtgärden CreateOrUpdate påbörjas.</span><span class="sxs-lookup"><span data-stu-id="73fd4-3171">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="73fd4-3172">0.4.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="73fd4-3172">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="73fd4-3173">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="73fd4-3173">Az.Profile</span></span>
* <span data-ttu-id="73fd4-3174">Åtgärdade problemet med Get-AzSubscription i CloudShell</span><span class="sxs-lookup"><span data-stu-id="73fd4-3174">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="73fd4-3175">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="73fd4-3175">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73fd4-3176">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73fd4-3176">Az.Compute</span></span>
* <span data-ttu-id="73fd4-3177">Nya storlekar lades till i listan över godkända VM-storlekar för vilka accelererat nätverk kommer att aktiveras vid användning av den enkla parameteruppsättningen för New-AzVm</span><span class="sxs-lookup"><span data-stu-id="73fd4-3177">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="73fd4-3178">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="73fd4-3178">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="73fd4-3179">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="73fd4-3179">Az.DataLakeStore</span></span>
* <span data-ttu-id="73fd4-3180">Lägger till stöd för regler för virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="73fd4-3180">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="73fd4-3181">Get-AzDataLakeStoreVirtualNetworkRule: Hämtar eller listar regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="73fd4-3181">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="73fd4-3182">Add-AzDataLakeStoreVirtualNetworkRule: Lägger till en regel för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="73fd4-3182">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="73fd4-3183">Set-AzDataLakeStoreVirtualNetworkRule: Ändrar den angivna regeln för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="73fd4-3183">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="73fd4-3184">Remove-AzDataLakeStoreVirtualNetworkRule: Tar bort en regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="73fd4-3184">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73fd4-3185">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73fd4-3185">Az.Network</span></span>
* <span data-ttu-id="73fd4-3186">Skicka protokollvärdet till serverdelen för att uppdatera cmdleten Test-AzNetworkWatcherConnectivity.</span><span class="sxs-lookup"><span data-stu-id="73fd4-3186">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="73fd4-3187">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="73fd4-3187">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="73fd4-3188">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73fd4-3188">Az.Resources</span></span>
* <span data-ttu-id="73fd4-3189">Åtgärdade problem där Get-AzRoleDefinition genererar ett oläsligt undantag (när standardprofilen inte innehåller någon prenumeration och ingen omfattning har angetts) genom att lägga till ett beskrivande undantag i scenariot.</span><span class="sxs-lookup"><span data-stu-id="73fd4-3189">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="73fd4-3190">Ställ in ”RoleDefinitionNameParameterSet” som standardparameteruppsättning.</span><span class="sxs-lookup"><span data-stu-id="73fd4-3190">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="73fd4-3191">0.3.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="73fd4-3191">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="73fd4-3192">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="73fd4-3192">Azure.Storage</span></span>
* <span data-ttu-id="73fd4-3193">Åtgärda fel där Kopiera blob/fil inte kopierar metadata när målplatsen har ett problem med metadata</span><span class="sxs-lookup"><span data-stu-id="73fd4-3193">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="73fd4-3194">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="73fd4-3194">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="73fd4-3195">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="73fd4-3195">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="73fd4-3196">Stöd för att hämta användningsinformation om en Storage-resurs för en specifik plats och för att lägga till ett varningsmeddelande för att hämta användningsinformation om en global Storage-resurs är inaktuellt.</span><span class="sxs-lookup"><span data-stu-id="73fd4-3196">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="73fd4-3197">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="73fd4-3197">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="73fd4-3198">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="73fd4-3198">Az.CognitiveServices</span></span>
* <span data-ttu-id="73fd4-3199">Stöd för Get-AzCognitiveServicesAccountSkus utan ett befintligt konto.</span><span class="sxs-lookup"><span data-stu-id="73fd4-3199">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73fd4-3200">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73fd4-3200">Az.Compute</span></span>
* <span data-ttu-id="73fd4-3201">Åtgärdade fel där Get-AzVM -ResourceGroupName <rg> returnerar fler än 50 resultat om det behövs</span><span class="sxs-lookup"><span data-stu-id="73fd4-3201">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="73fd4-3202">Lade till ett exempel för SimpleParameterSet i hjälpen för cmdleten New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="73fd4-3202">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="73fd4-3203">Ett stavfel i förloppsmeddelandet för Azure Disk Encryption har korrigerats</span><span class="sxs-lookup"><span data-stu-id="73fd4-3203">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="73fd4-3204">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="73fd4-3204">Az.DataFactoryV2</span></span>
* <span data-ttu-id="73fd4-3205">ADF .Net SDK-versionen har uppdaterats till 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="73fd4-3205">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73fd4-3206">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73fd4-3206">Az.Network</span></span>
* <span data-ttu-id="73fd4-3207">Funktionalitet för NetworkProfile har lagts till.</span><span class="sxs-lookup"><span data-stu-id="73fd4-3207">Added NetworkProfile functionality.</span></span> <span data-ttu-id="73fd4-3208">nya cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-3208">new cmdlets added</span></span>
    - <span data-ttu-id="73fd4-3209">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="73fd4-3209">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="73fd4-3210">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="73fd4-3210">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="73fd4-3211">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="73fd4-3211">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="73fd4-3212">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="73fd4-3212">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="73fd4-3213">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="73fd4-3213">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="73fd4-3214">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="73fd4-3214">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="73fd4-3215">Länk för tjänstassociering på modell för undernät har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-3215">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="73fd4-3216">Cmdletarna New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap och Remove-AzVirtualNetworkTap har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-3216">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="73fd4-3217">Cmdletarna Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig och Remove-AzNEtworkInterfaceTapConfig har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-3217">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="73fd4-3218">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="73fd4-3218">Az.RedisCache</span></span>
* <span data-ttu-id="73fd4-3219">Tillåt att alla strängar används som storleksparametrar framöver.</span><span class="sxs-lookup"><span data-stu-id="73fd4-3219">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="73fd4-3220">Lägg till P5 i popup-fönstret PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="73fd4-3220">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="73fd4-3221">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73fd4-3221">Az.Resources</span></span>
* <span data-ttu-id="73fd4-3222">Parametern -Mode som saknades i Set-AzPolicyDefinition har lagts till</span><span class="sxs-lookup"><span data-stu-id="73fd4-3222">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="73fd4-3223">Åtgärdade buggen för cmdleten Get-AzProviderOperation för åtgärder med ursprung som innehåller användare</span><span class="sxs-lookup"><span data-stu-id="73fd4-3223">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="73fd4-3224">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73fd4-3224">Az.Sql</span></span>
* <span data-ttu-id="73fd4-3225">Ett problem där vissa cmdletar för säkerhetskopiering inte kunde identifiera den aktuella azure-prenumerationen har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="73fd4-3225">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="73fd4-3226">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="73fd4-3226">Az.Websites</span></span>
* <span data-ttu-id="73fd4-3227">Ny cmdlet: Get-AzWebAppContainerContinuousDeploymentUrl – Hämtar webhook-URL:en för kontinuerlig distribution av container</span><span class="sxs-lookup"><span data-stu-id="73fd4-3227">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="73fd4-3228">Nya cmdletar: New-AzWebAppContainerPSSession och Enter-WebAppContainerPSSession – Startar en PowerShell-fjärrsession i en containerapp för windows</span><span class="sxs-lookup"><span data-stu-id="73fd4-3228">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="73fd4-3229">0.2.0 – september 2018</span><span class="sxs-lookup"><span data-stu-id="73fd4-3229">0.2.0 - September 2018</span></span>
 <span data-ttu-id="73fd4-3230">Första versionen</span><span class="sxs-lookup"><span data-stu-id="73fd4-3230">Initial Release</span></span>