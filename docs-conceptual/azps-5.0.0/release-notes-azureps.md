---
title: Viktig information om Azure PowerShell
description: Lär dig mer om alla de senaste uppdateringarna för Azure PowerShell-modulerna.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 4ab5639cfb997c5f9ee1286e6eacb97ef775239a
ms.sourcegitcommit: 63181e0af0e4468b0530fdb0495ed4d44bdfd1c8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/31/2020
ms.locfileid: "93134870"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="8d428-103">Viktig information om Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="8d428-103">Azure PowerShell release notes</span></span>

## <a name="500---october-2020"></a><span data-ttu-id="8d428-104">5.0.0 – Oktober 2020</span><span class="sxs-lookup"><span data-stu-id="8d428-104">5.0.0 - October 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8d428-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8d428-105">Az.Accounts</span></span>
* <span data-ttu-id="8d428-106">[Icke-bakåtkompatibel ändring] Tog bort ”Get-AzProfile” och ”Select-AzProfile”</span><span class="sxs-lookup"><span data-stu-id="8d428-106">[Breaking Change] Removed 'Get-AzProfile' and 'Select-AzProfile'</span></span>
* <span data-ttu-id="8d428-107">Ersatte Azure Directory Authentication Library med Microsoft Authentication Library (MSAL)</span><span class="sxs-lookup"><span data-stu-id="8d428-107">Replaced Azure Directory Authentication Library with Microsoft Authentication Library(MSAL)</span></span>

#### <a name="azaks"></a><span data-ttu-id="8d428-108">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="8d428-108">Az.Aks</span></span>
* <span data-ttu-id="8d428-109">[Icke-bakåtkompatibel ändring] Tog bort aliaset ”ClientIdAndSecret” i ”New-AzAksCluster” och ”Set-AzAksCluster”.</span><span class="sxs-lookup"><span data-stu-id="8d428-109">[Breaking Change] Removed parameter alias 'ClientIdAndSecret' in 'New-AzAksCluster' and 'Set-AzAksCluster'.</span></span>
* <span data-ttu-id="8d428-110">[Icke-bakåtkompatibel ändring] Ändrade standardvärdet för ”NodeVmSetType” i ”New-AzAksCluster” från ”AvailabilitySet” till ”VirtualMachineScaleSets”.</span><span class="sxs-lookup"><span data-stu-id="8d428-110">[Breaking Change] Changed the default value of 'NodeVmSetType' in 'New-AzAksCluster' from 'AvailabilitySet' to 'VirtualMachineScaleSets'.</span></span>
* <span data-ttu-id="8d428-111">[Icke-bakåtkompatibel ändring] Ändrade standardvärdet för ”NetworkPlugin” i ”New-AzAksCluster” från ”None” till ”azure”.</span><span class="sxs-lookup"><span data-stu-id="8d428-111">[Breaking Change] Changed the default value of 'NetworkPlugin' in 'New-AzAksCluster' from 'None' to 'azure'.</span></span>
* <span data-ttu-id="8d428-112">[Icke-bakåtkompatibel ändring] Tog bort parametern ”NodeOsType” i ”New-AzAksCluster” eftersom den endast har stöd för Linux med ett värde.</span><span class="sxs-lookup"><span data-stu-id="8d428-112">[Breaking Change] Removed parameter 'NodeOsType' in 'New-AzAksCluster' as it supports only one value Linux.</span></span>

#### <a name="azbilling"></a><span data-ttu-id="8d428-113">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="8d428-113">Az.Billing</span></span>
* <span data-ttu-id="8d428-114">Lade till cmdleten ”Get-AzBillingAccount”</span><span class="sxs-lookup"><span data-stu-id="8d428-114">Added 'Get-AzBillingAccount' cmdlet</span></span>
* <span data-ttu-id="8d428-115">Lade till cmdleten ”Get-AzBillingProfile”</span><span class="sxs-lookup"><span data-stu-id="8d428-115">Added 'Get-AzBillingProfile' cmdlet</span></span>
* <span data-ttu-id="8d428-116">Lade till cmdleten ”Get-AzInvoiceSection”</span><span class="sxs-lookup"><span data-stu-id="8d428-116">Added 'Get-AzInvoiceSection' cmdlet</span></span>
* <span data-ttu-id="8d428-117">Lade till nya parametrar i cmdleten ”Get-AzBillingInvoice”</span><span class="sxs-lookup"><span data-stu-id="8d428-117">Added new parameters in 'Get-AzBillingInvoice' cmdlet</span></span>
* <span data-ttu-id="8d428-118">Tog bort egenskaperna ”DownloadUrlExpiry”, ”Type” och ”BillingPeriodNames” från svaret för cmdleten ”Get-AzBillingInvoic”</span><span class="sxs-lookup"><span data-stu-id="8d428-118">Removed properties DownloadUrlExpiry, Type, BillingPeriodNames from the response of Get-AzBillingInvoice cmdlet</span></span>

#### <a name="azcdn"></a><span data-ttu-id="8d428-119">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="8d428-119">Az.Cdn</span></span>
* <span data-ttu-id="8d428-120">Lade till cmdletar för att stödja funktioner för flera ursprung och privat länk</span><span class="sxs-lookup"><span data-stu-id="8d428-120">Added cmdlets to support multi-origin and private link functionality</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="8d428-121">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8d428-121">Az.CognitiveServices</span></span>
* <span data-ttu-id="8d428-122">Uppdaterade SDK till 7.4.0-preview.</span><span class="sxs-lookup"><span data-stu-id="8d428-122">Updated SDK to 7.4.0-preview.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d428-123">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d428-123">Az.Compute</span></span>
* <span data-ttu-id="8d428-124">Lade till parametern ”-VmssId” till ”New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="8d428-124">Added '-VmssId' parameter to 'New-AzVm'</span></span>
* <span data-ttu-id="8d428-125">Lade till parametern ”PlatformFaultDomainCount” till cmdleten ”New-AzVmss”.</span><span class="sxs-lookup"><span data-stu-id="8d428-125">Added 'PlatformFaultDomainCount' parameter to the 'New-AzVmss' cmdlet.</span></span>
* <span data-ttu-id="8d428-126">Ny cmdlet: ”Get-AzDiskEncryptionSetAssociatedResource”</span><span class="sxs-lookup"><span data-stu-id="8d428-126">New cmdlet 'Get-AzDiskEncryptionSetAssociatedResource'</span></span>
* <span data-ttu-id="8d428-127">Lade till de valfria parametrarna ”Tier” och ”LogicalSectorSize” till cmdleten ”New-AzDiskConfig”.</span><span class="sxs-lookup"><span data-stu-id="8d428-127">Added 'Tier' and 'LogicalSectorSize' optional parameters to the New-AzDiskConfig cmdlet.</span></span> 
* <span data-ttu-id="8d428-128">Lade till de valfria parametrarna ”Tier”, ”MaxSharesCount”, ”DiskIOPSReadOnly” och ”DiskMBpsReadOnly” till cmdleten ”New-AzDiskUpdateConfig”.</span><span class="sxs-lookup"><span data-stu-id="8d428-128">Added 'Tier', 'MaxSharesCount', 'DiskIOPSReadOnly', and 'DiskMBpsReadOnly' optional parameters to the 'New-AzDiskUpdateConfig' cmdlet.</span></span> 

#### <a name="azcontainerregistry"></a><span data-ttu-id="8d428-129">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8d428-129">Az.ContainerRegistry</span></span>
* <span data-ttu-id="8d428-130">[Icke-bakåtkompatibel ändring] Uppdaterar API-versionen till 2019-05-01</span><span class="sxs-lookup"><span data-stu-id="8d428-130">[Breaking Change] Updates API version to 2019-05-01</span></span>
* <span data-ttu-id="8d428-131">[Icke-bakåtkompatibel ändring] Tog bort SKU:n ”Classic” och parametern ”StorageAccountName” från ”New-AzContainerRegistry”</span><span class="sxs-lookup"><span data-stu-id="8d428-131">[Breaking Change] Removed SKU 'Classic' and parameter 'StorageAccountName' from 'New-AzContainerRegistry'</span></span>
* <span data-ttu-id="8d428-132">Lade till nya cmdletar: ”Connect-AzContainerRegistry”, ”Import-AzContainerRegistry”, ”Get-AzContainerRegistryUsage”, ”New-AzContainerRegistryNetworkRule”, ”Set-AzContainerRegistryNetworkRule”</span><span class="sxs-lookup"><span data-stu-id="8d428-132">Added New cmdlets: 'Connect-AzContainerRegistry', 'Import-AzContainerRegistry', 'Get-AzContainerRegistryUsage', 'New-AzContainerRegistryNetworkRule', 'Set-AzContainerRegistryNetworkRule'</span></span>
* <span data-ttu-id="8d428-133">Lade till den nya parametern ”NetworkRuleSet” till ”Update-AzContainerRegistry”</span><span class="sxs-lookup"><span data-stu-id="8d428-133">Added new parameter 'NetworkRuleSet' to 'Update-AzContainerRegistry'</span></span>

#### <a name="azdatabricks"></a><span data-ttu-id="8d428-134">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="8d428-134">Az.Databricks</span></span>
* <span data-ttu-id="8d428-135">Korrigerade en bugg som kunde leda till att en uppdatering av en Databricks-arbetsyta utan `-EncryptionKeyVersion` misslyckades.</span><span class="sxs-lookup"><span data-stu-id="8d428-135">Fixed a bug that may cause updating databricks workspace without `-EncryptionKeyVersion` to fail.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8d428-136">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8d428-136">Az.DataFactory</span></span>
* <span data-ttu-id="8d428-137">Uppdaterade ADF .Net SDK-versionen till 4.12.0</span><span class="sxs-lookup"><span data-stu-id="8d428-137">Updated ADF .Net SDK version to 4.12.0</span></span>
* <span data-ttu-id="8d428-138">Uppdaterade ADF-krypteringsklientens SDK-version till 4.14.7587.7</span><span class="sxs-lookup"><span data-stu-id="8d428-138">Updated ADF encryption client SDK version to 4.14.7587.7</span></span>
* <span data-ttu-id="8d428-139">Lade till kommandona ”Stop-AzDataFactoryV2TriggerRun” och ”Invoke-AzDataFactoryV2TriggerRun”</span><span class="sxs-lookup"><span data-stu-id="8d428-139">Added 'Stop-AzDataFactoryV2TriggerRun' and 'Invoke-AzDataFactoryV2TriggerRun' commands</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="8d428-140">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="8d428-140">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="8d428-141">Kräv egenskapen Plats för att skapa ARM-objekt på högsta nivån.</span><span class="sxs-lookup"><span data-stu-id="8d428-141">Require Location property for creating top level arm objects.</span></span>
        <span data-ttu-id="8d428-142">\* Gjorde så att `ApplicationGroupType` krävs för `New-AzWvdApplicationGroup`.</span><span class="sxs-lookup"><span data-stu-id="8d428-142">\* Made `ApplicationGroupType` required for `New-AzWvdApplicationGroup`.</span></span>
        <span data-ttu-id="8d428-143">\* Gjorde så att `HostPoolArmPath` krävs för `New-AzWvdApplicationGroup`.</span><span class="sxs-lookup"><span data-stu-id="8d428-143">\* Made `HostPoolArmPath` required for `New-AzWvdApplicationGroup`.</span></span>
        <span data-ttu-id="8d428-144">\* `PreferredAppGroupType` har lagts till för `New-AzWvdHostPool`.</span><span class="sxs-lookup"><span data-stu-id="8d428-144">\* Added `PreferredAppGroupType` for `New-AzWvdHostPool`.</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="8d428-145">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="8d428-145">Az.Functions</span></span>
* <span data-ttu-id="8d428-146">[Icke-bakåtkompatibel ändring] Tog bort växelparametern ”IncludeSlot” från alla förutom en parameteruppsättning i ”Get-AzFunctionApp”.</span><span class="sxs-lookup"><span data-stu-id="8d428-146">[Breaking Change] Removed 'IncludeSlot' switch parameter from all but one parameter set of 'Get-AzFunctionApp'.</span></span> <span data-ttu-id="8d428-147">Cmdleten stöder nu hämtning av distributionsfack i resultaten när ”-IncludeSlot” anges.</span><span class="sxs-lookup"><span data-stu-id="8d428-147">The cmdlet now supports retrieving deployment slots in the results when '-IncludeSlot' is specified.</span></span> 
* <span data-ttu-id="8d428-148">Uppdaterade ”New-AzFunctionApp”:</span><span class="sxs-lookup"><span data-stu-id="8d428-148">Updated 'New-AzFunctionApp':</span></span>
  - <span data-ttu-id="8d428-149">Korrigerade ”-DisableApplicationInsights” så att inga Application Insights-projekt skapas när det här alternativet har angetts.</span><span class="sxs-lookup"><span data-stu-id="8d428-149">Fixed -DisableApplicationInsights so that no application insights project is created when this option is specified.</span></span> <span data-ttu-id="8d428-150">[#12728]</span><span class="sxs-lookup"><span data-stu-id="8d428-150">[#12728]</span></span>
  - <span data-ttu-id="8d428-151">[Icke-bakåtkompatibel ändring] Tog bort stöd för att skapa PowerShell 6.2-funktionsappar.</span><span class="sxs-lookup"><span data-stu-id="8d428-151">[Breaking Change] Removed support to create PowerShell 6.2 function apps.</span></span>
  - <span data-ttu-id="8d428-152">[Icke-bakåtkompatibel ändring] Ändrade körningsversionen som är standard i Functions version 3 i Windows för PowerShell-funktionsappar från 6.2 till 7.0 när parametern RuntimeVersion inte har angetts.</span><span class="sxs-lookup"><span data-stu-id="8d428-152">[Breaking Change] Changed the default runtime version in Functions version 3 on Windows for PowerShell function apps from 6.2 to 7.0 when the RuntimeVersion parameter is not specified.</span></span>
  - <span data-ttu-id="8d428-153">[Icke-bakåtkompatibel ändring] Ändrade körningsversionen som är standard i Functions version 3 i Windows och Linux för Node-funktionsappar från 10 till 12 när parametern RuntimeVersion inte har angetts.</span><span class="sxs-lookup"><span data-stu-id="8d428-153">[Breaking Change] Changed the default runtime version in Functions version 3 on Windows and Linux for Node function apps from 10 to 12 when the RuntimeVersion parameter is not specified.</span></span>
  - <span data-ttu-id="8d428-154">[Icke-bakåtkompatibel ändring] Ändrade körningsversionen som är standard i Functions version 3 i Linux för Python-funktionsappar från 3.7 till 3.8 när parametern RuntimeVersion inte har angetts.</span><span class="sxs-lookup"><span data-stu-id="8d428-154">[Breaking Change] Changed the default runtime version in Functions version 3 on Linux for Python function apps from 3.7 to 3.8 when the RuntimeVersion parameter is not specified.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="8d428-155">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8d428-155">Az.HDInsight</span></span>
 * <span data-ttu-id="8d428-156">För cmdleten New-AzHDInsightCluster:</span><span class="sxs-lookup"><span data-stu-id="8d428-156">For New-AzHDInsightCluster cmdlet:</span></span>
     - <span data-ttu-id="8d428-157">Ersatte parametern ”DefaultStorageAccountName” med ”StorageAccountResourceId”</span><span class="sxs-lookup"><span data-stu-id="8d428-157">Replaced parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
     - <span data-ttu-id="8d428-158">Ersatte parametern ”DefaultStorageAccountKey” med ”StorageAccountKey”</span><span class="sxs-lookup"><span data-stu-id="8d428-158">Replaced parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
     - <span data-ttu-id="8d428-159">Ersatte parametern ”DefaultStorageAccountType” med ”StorageAccountType”</span><span class="sxs-lookup"><span data-stu-id="8d428-159">Replaced parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
     - <span data-ttu-id="8d428-160">Tog bort parametern ”PublicNetworkAccessType”</span><span class="sxs-lookup"><span data-stu-id="8d428-160">Removed parameter 'PublicNetworkAccessType'</span></span>
     - <span data-ttu-id="8d428-161">Ta bort parametern ”OutboundPublicNetworkAccessType”</span><span class="sxs-lookup"><span data-stu-id="8d428-161">Removed parameter 'OutboundPublicNetworkAccessType'</span></span>
     - <span data-ttu-id="8d428-162">Lade till nya parametrar: ”StorageFileSystem” och ”StorageAccountManagedIdentity” för att stödja ADLSGen2</span><span class="sxs-lookup"><span data-stu-id="8d428-162">Added new parameters: 'StorageFileSystem' and 'StorageAccountManagedIdentity' to support ADLSGen2</span></span>
     - <span data-ttu-id="8d428-163">Lade till den nya parametern ”EnableIDBroker” för att stödja ID-förmedlaren i HDInsight</span><span class="sxs-lookup"><span data-stu-id="8d428-163">Added new parameter 'EnableIDBroker' to Support HDInsight ID Broker</span></span>
     - <span data-ttu-id="8d428-164">Lade till nya parametrar: ”KafkaClientGroupId”, ”KafkaClientGroupName” och ”KafkaManagementNodeSize” för att stödja Kafka REST-proxy</span><span class="sxs-lookup"><span data-stu-id="8d428-164">Added new parameters: 'KafkaClientGroupId', 'KafkaClientGroupName' and 'KafkaManagementNodeSize' to support Kafka Rest Proxy</span></span>
 * <span data-ttu-id="8d428-165">För cmdleten New-AzHDInsightClusterConfig:</span><span class="sxs-lookup"><span data-stu-id="8d428-165">For New-AzHDInsightClusterConfig cmdlet:</span></span>
     - <span data-ttu-id="8d428-166">Ersatte parametern ”DefaultStorageAccountName” med ”StorageAccountResourceId”</span><span class="sxs-lookup"><span data-stu-id="8d428-166">Replaced parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
     - <span data-ttu-id="8d428-167">Ersatte parametern ”DefaultStorageAccountKey” med ”StorageAccountKey”</span><span class="sxs-lookup"><span data-stu-id="8d428-167">Replaced parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
     - <span data-ttu-id="8d428-168">Ersatte parametern ”DefaultStorageAccountType” med ”StorageAccountType”</span><span class="sxs-lookup"><span data-stu-id="8d428-168">Replaced parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
     - <span data-ttu-id="8d428-169">Tog bort parametern ”PublicNetworkAccessType”</span><span class="sxs-lookup"><span data-stu-id="8d428-169">Removed parameter 'PublicNetworkAccessType'</span></span>
     - <span data-ttu-id="8d428-170">Ta bort parametern ”OutboundPublicNetworkAccessType”</span><span class="sxs-lookup"><span data-stu-id="8d428-170">Removed parameter 'OutboundPublicNetworkAccessType'</span></span>
* <span data-ttu-id="8d428-171">För cmdleten Set-AzHDInsightDefaultStorage:</span><span class="sxs-lookup"><span data-stu-id="8d428-171">For Set-AzHDInsightDefaultStorage cmdlet:</span></span>
    - <span data-ttu-id="8d428-172">Ersatte parametern ”StorageAccountName” med ”StorageAccountResourceId”</span><span class="sxs-lookup"><span data-stu-id="8d428-172">Replaced parameter 'StorageAccountName' with 'StorageAccountResourceId'</span></span>
* <span data-ttu-id="8d428-173">För cmdleten Add-AzHDInsightSecurityProfile:</span><span class="sxs-lookup"><span data-stu-id="8d428-173">For Add-AzHDInsightSecurityProfile cmdlet:</span></span>
    - <span data-ttu-id="8d428-174">Ersatte parametern ”Domain” med ”DomainResourceId”</span><span class="sxs-lookup"><span data-stu-id="8d428-174">Replaced parameter 'Domain' with 'DomainResourceId'</span></span>
    - <span data-ttu-id="8d428-175">Tog bort det obligatoriska kravet för parametern ”OrganizationalUnitDN”</span><span class="sxs-lookup"><span data-stu-id="8d428-175">Removed the mandatory requirement for parameter 'OrganizationalUnitDN'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8d428-176">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8d428-176">Az.KeyVault</span></span>
* <span data-ttu-id="8d428-177">[Icke-bakåtkompatibel ändring] Parametrarna DisableSoftDelete i ”New-AzKeyVault” och EnableSoftDelete i ”Update-AzKeyVault” har gjorts inaktuella</span><span class="sxs-lookup"><span data-stu-id="8d428-177">[Breaking Change] Deprecated parameter DisableSoftDelete in 'New-AzKeyVault' and EnableSoftDelete in 'Update-AzKeyVault'</span></span>
* <span data-ttu-id="8d428-178">[Icke-bakåtkompatibel ändring] Tog bort attributet SecretValueText för att undvika att SecretValue visas direkt [#12266]</span><span class="sxs-lookup"><span data-stu-id="8d428-178">[Breaking Change] Removed attribute SecretValueText to avoid displaying SecretValue directly [#12266]</span></span>
* <span data-ttu-id="8d428-179">Stöd för ny resurstyp: hanterad HSM</span><span class="sxs-lookup"><span data-stu-id="8d428-179">Supported new resource type: managed HSM</span></span>
    - <span data-ttu-id="8d428-180">CRUD för hanterad HSM och cmdleter för att köra nycklar på hanterad HSM</span><span class="sxs-lookup"><span data-stu-id="8d428-180">CRUD of managed HSM and cmdlets to operate keys on managed HSM</span></span>
    - <span data-ttu-id="8d428-181">Fullständig HSM-säkerhetskopiering/återställning, skapande av AES-nyckel, säkerhetskopiering/återställning av domän, RBAC</span><span class="sxs-lookup"><span data-stu-id="8d428-181">Full HSM backup/restore, AES key creation, security domain backup/restore, RBAC</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="8d428-182">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="8d428-182">Az.ManagedServices</span></span>
* <span data-ttu-id="8d428-183">[Icke-bakåtkompatibel ändring] Uppdaterade namngivningskonventioner för parametrar och associerade exempel</span><span class="sxs-lookup"><span data-stu-id="8d428-183">[Breaking Change] Updated parameters naming conventions and associated examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8d428-184">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d428-184">Az.Network</span></span>
* <span data-ttu-id="8d428-185">[Icke-bakåtkompatibel ändring] Tog bort parametern ”HostedSubnet” och lade till ”Subnet” i stället</span><span class="sxs-lookup"><span data-stu-id="8d428-185">[Breaking Change] Removed parameter 'HostedSubnet' and added 'Subnet' instead</span></span>
* <span data-ttu-id="8d428-186">Lade till nya cmdletar för peeringvägar för virtuella routrar</span><span class="sxs-lookup"><span data-stu-id="8d428-186">Added new cmdlets for Virtual Router Peer Routes</span></span>
    - <span data-ttu-id="8d428-187">”Get-AzVirtualRouterPeerLearnedRoute”</span><span class="sxs-lookup"><span data-stu-id="8d428-187">'Get-AzVirtualRouterPeerLearnedRoute'</span></span>
    - <span data-ttu-id="8d428-188">”Get-AzVirtualRouterPeerAdvertisedRoute”</span><span class="sxs-lookup"><span data-stu-id="8d428-188">'Get-AzVirtualRouterPeerAdvertisedRoute'</span></span>
* <span data-ttu-id="8d428-189">Cmdleten New-AzFirewall har uppdaterats:</span><span class="sxs-lookup"><span data-stu-id="8d428-189">Updated New-AzFirewall cmdlet:</span></span>
    - <span data-ttu-id="8d428-190">Lade till parametern ”-SkuTier”</span><span class="sxs-lookup"><span data-stu-id="8d428-190">Added parameter '-SkuTier'</span></span>
    - <span data-ttu-id="8d428-191">Lade till parametern ”-SkuName” och gjorde Sku till ett alias för den</span><span class="sxs-lookup"><span data-stu-id="8d428-191">Added parameter '-SkuName' and made Sku as Alias for this</span></span>
    - <span data-ttu-id="8d428-192">Tog bort parametern ”-Sku”</span><span class="sxs-lookup"><span data-stu-id="8d428-192">Removed parameter '-Sku'</span></span>
* <span data-ttu-id="8d428-193">[Icke-bakåtkompatibel ändring] Gjorde argumentet ”Connectionlink” obligatoriskt i ”Start-AzVpnConnectionPacketCapture” och ”Stop-AzVpnConnectionPacketCapture”</span><span class="sxs-lookup"><span data-stu-id="8d428-193">[Breaking Change] Made 'Connectionlink' argument mandatory in 'Start-AzVpnConnectionPacketCapture' and 'Stop-AzVpnConnectionPacketCapture'</span></span>
* <span data-ttu-id="8d428-194">[Icke-bakåtkompatibel ändring] Uppdaterade ”New-AzNetworkWatcherConnectionMonitorEndPointObject” för att ta bort parametern ”-Filter”</span><span class="sxs-lookup"><span data-stu-id="8d428-194">[Breaking Change] Updated 'New-AzNetworkWatcherConnectionMonitorEndPointObject' to remove parameter '-Filter'</span></span>
* <span data-ttu-id="8d428-195">[Icke-bakåtkompatibel ändring] Ersatte cmdleten ”New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject” med ”New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject”</span><span class="sxs-lookup"><span data-stu-id="8d428-195">[Breaking Change] Replaced 'New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject' cmdlet with 'New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject'</span></span>
* <span data-ttu-id="8d428-196">Uppdaterade cmdleten ”New-AzNetworkWatcherConnectionMonitorEndPointObject”:</span><span class="sxs-lookup"><span data-stu-id="8d428-196">Updated 'New-AzNetworkWatcherConnectionMonitorEndPointObject' cmdlet:</span></span>
    - <span data-ttu-id="8d428-197">Lade till parametern ”-Type”</span><span class="sxs-lookup"><span data-stu-id="8d428-197">Added parameter '-Type'</span></span>
    - <span data-ttu-id="8d428-198">Lade till parametern ”-CoverageLevel”</span><span class="sxs-lookup"><span data-stu-id="8d428-198">Added parameter '-CoverageLevel'</span></span>
    - <span data-ttu-id="8d428-199">Lade till parametern ”-Scope”</span><span class="sxs-lookup"><span data-stu-id="8d428-199">Added parameter '-Scope'</span></span>
* <span data-ttu-id="8d428-200">Uppdaterade cmdleten ”New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject” med den nya parametern ”-DestinationPortBehavior”</span><span class="sxs-lookup"><span data-stu-id="8d428-200">Updated 'New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject' cmdlet with new parameter '-DestinationPortBehavior'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8d428-201">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8d428-201">Az.RecoveryServices</span></span>
* <span data-ttu-id="8d428-202">Korrigerar återställning av arbetsbelastningar för behörigheter för deltagare.</span><span class="sxs-lookup"><span data-stu-id="8d428-202">Fixing Workload Restore for contributor permissions.</span></span>
* <span data-ttu-id="8d428-203">Lade till nya parameteruppsättningar och valideringar för cmdleten ”Restore-AzRecoveryServicesBackupItem”.</span><span class="sxs-lookup"><span data-stu-id="8d428-203">Added new parameter sets and validations for Restore-AzRecoveryServicesBackupItem cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8d428-204">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d428-204">Az.Resources</span></span>
* <span data-ttu-id="8d428-205">Korrigerade en bugg vid parsning</span><span class="sxs-lookup"><span data-stu-id="8d428-205">Fixed parsing bug</span></span>
* <span data-ttu-id="8d428-206">Uppdaterade What-If-cmdletar i ARM-mall för att ta bort förhandsgranskningsmeddelandet från resultaten</span><span class="sxs-lookup"><span data-stu-id="8d428-206">Updated ARM template What-If cmdlets to remove preview message from results</span></span>
* <span data-ttu-id="8d428-207">Korrigerade ett problem där cmdletar för mall-distribution kraschar om ”-WhatIf” har ställts in på ett högre omfång [#13038]</span><span class="sxs-lookup"><span data-stu-id="8d428-207">Fixed an issue where template deployment cmdlets crash if '-WhatIf' is set at a higher scope [#13038]</span></span>
* <span data-ttu-id="8d428-208">Korrigerade ett problem där cmdletar för malldistribution inte bevarar skiftläget för mallparametrar</span><span class="sxs-lookup"><span data-stu-id="8d428-208">Fixed an issue where template deployment cmdlets does not preserve case for template parameters</span></span>
* <span data-ttu-id="8d428-209">Lade till en standard-API-version som kan användas i cmdleten ”Export-AzResourceGroup”</span><span class="sxs-lookup"><span data-stu-id="8d428-209">Added a default API version to be used in 'Export-AzResourceGroup' cmdlet</span></span>
* <span data-ttu-id="8d428-210">Lade till cmdletar för mallspecifikationer (”Get-AzTemplateSpec”, ”Set-AzTemplateSpec”, ”New-AzTemplateSpec”, ”Remove-AzTemplateSpec”, ”Export-AzTemplateSpec”)</span><span class="sxs-lookup"><span data-stu-id="8d428-210">Added cmdlets for Template Specs ('Get-AzTemplateSpec', 'Set-AzTemplateSpec', 'New-AzTemplateSpec', 'Remove-AzTemplateSpec', 'Export-AzTemplateSpec')</span></span>
* <span data-ttu-id="8d428-211">Lade till stöd för att distribuera mallspecifikationer med befintliga cmdletar för distribution (via den nya parametern ”-TemplateSpecId”)</span><span class="sxs-lookup"><span data-stu-id="8d428-211">Added support for deploying Template Specs using existing deployment cmdlets (via the new -TemplateSpecId parameter)</span></span> 
* <span data-ttu-id="8d428-212">Uppdaterade ”Get-AzResourceGroupDeploymentOperation” för att använda SDK.</span><span class="sxs-lookup"><span data-stu-id="8d428-212">Updated 'Get-AzResourceGroupDeploymentOperation' to use the SDK.</span></span>
* <span data-ttu-id="8d428-213">Tog bort parametern ”ApiVersion” från cmdletarna ”\*-AzDeployment”.</span><span class="sxs-lookup"><span data-stu-id="8d428-213">Removed '-ApiVersion' parameter from '\*-AzDeployment' cmdlets.</span></span>

#### <a name="azsql"></a><span data-ttu-id="8d428-214">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d428-214">Az.Sql</span></span>
* <span data-ttu-id="8d428-215">Lade till DiffBackupIntervalInHours till ”Set-AzSqlDatabaseBackupShortTermRetentionPolicy”</span><span class="sxs-lookup"><span data-stu-id="8d428-215">Added DiffBackupIntervalInHours to 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span> 
* <span data-ttu-id="8d428-216">Korrigerade ett problem där New-AzSqlDatabaseExport misslyckas om networkIsolation inte har angetts [#13097]</span><span class="sxs-lookup"><span data-stu-id="8d428-216">Fixed issue where New-AzSqlDatabaseExport fails if networkIsolation not specified [#13097]</span></span>
* <span data-ttu-id="8d428-217">Korrigerade ett problem där New-AzSqlDatabaseExport och New-AzSqlDatabaseImport inte returnerade OperationStatusLink i resultatobjektet [#13097]</span><span class="sxs-lookup"><span data-stu-id="8d428-217">Fixed issue where New-AzSqlDatabaseExport and New-AzSqlDatabaseImport were not returning OperationStatusLink in the result object [#13097]</span></span>
* <span data-ttu-id="8d428-218">Uppdatera webbadresser för Azure-kopplade regioner i redundansvarningar för Backup Storage</span><span class="sxs-lookup"><span data-stu-id="8d428-218">Update Azure Paired Regions URL in Backup Storage Redundancy Warnings</span></span> 

#### <a name="azstorage"></a><span data-ttu-id="8d428-219">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8d428-219">Az.Storage</span></span>
* <span data-ttu-id="8d428-220">Tog bort den föråldrade egenskapen RestorePolicy.LastEnabledTime</span><span class="sxs-lookup"><span data-stu-id="8d428-220">Removed obsolete property RestorePolicy.LastEnabledTime</span></span>
    - <span data-ttu-id="8d428-221">"Enable-AzStorageBlobRestorePolicy"</span><span class="sxs-lookup"><span data-stu-id="8d428-221">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="8d428-222">"Disable-AzStorageBlobRestorePolicy"</span><span class="sxs-lookup"><span data-stu-id="8d428-222">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="8d428-223">”Get-AzStorageBlobServiceProperty”</span><span class="sxs-lookup"><span data-stu-id="8d428-223">'Get-AzStorageBlobServiceProperty'</span></span>
    - <span data-ttu-id="8d428-224">”Update-AzStorageBlobServiceProperty”</span><span class="sxs-lookup"><span data-stu-id="8d428-224">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="8d428-225">Vill du ändra typen av DaysAfterModificationGreaterThan från int till int?</span><span class="sxs-lookup"><span data-stu-id="8d428-225">Change Type of DaysAfterModificationGreaterThan from int to int?</span></span>
    - <span data-ttu-id="8d428-226">"Set-AzStorageAccountManagementPolicy"</span><span class="sxs-lookup"><span data-stu-id="8d428-226">'Set-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="8d428-227">"Get-AzStorageAccountManagementPolicy"</span><span class="sxs-lookup"><span data-stu-id="8d428-227">'Get-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="8d428-228">"Add-AzStorageAccountManagementPolicyAction"</span><span class="sxs-lookup"><span data-stu-id="8d428-228">'Add-AzStorageAccountManagementPolicyAction'</span></span>
    - <span data-ttu-id="8d428-229">"New-AzStorageAccountManagementPolicyRule"</span><span class="sxs-lookup"><span data-stu-id="8d428-229">'New-AzStorageAccountManagementPolicyRule'</span></span>
* <span data-ttu-id="8d428-230">Stöd för skapa/uppdatera filresurs med åtkomstnivå</span><span class="sxs-lookup"><span data-stu-id="8d428-230">Supported create/update file share with access tier</span></span>
    - <span data-ttu-id="8d428-231">”New-AzRmStorageShare”</span><span class="sxs-lookup"><span data-stu-id="8d428-231">'New-AzRmStorageShare'</span></span>
    - <span data-ttu-id="8d428-232">”Update-AzRmStorageShare”</span><span class="sxs-lookup"><span data-stu-id="8d428-232">'Update-AzRmStorageShare'</span></span>
* <span data-ttu-id="8d428-233">Stöd för att konfigurera/uppdatera/ta bort ACL som stöds rekursivt på Datalake Gen2-objekt</span><span class="sxs-lookup"><span data-stu-id="8d428-233">Supported set/update/remove Acl recursively on Datalake Gen2 item</span></span> 
    -  <span data-ttu-id="8d428-234">”Set-AzDataLakeGen2AclRecursive”</span><span class="sxs-lookup"><span data-stu-id="8d428-234">'Set-AzDataLakeGen2AclRecursive'</span></span> 
    -  <span data-ttu-id="8d428-235">”Update-AzDataLakeGen2AclRecursive”</span><span class="sxs-lookup"><span data-stu-id="8d428-235">'Update-AzDataLakeGen2AclRecursive'</span></span> 
    -  <span data-ttu-id="8d428-236">”Remove-AzDataLakeGen2AclRecursive”</span><span class="sxs-lookup"><span data-stu-id="8d428-236">'Remove-AzDataLakeGen2AclRecursive'</span></span>
* <span data-ttu-id="8d428-237">Stöd för åtkomstprincip för containrar med de nya behörigheterna x, t</span><span class="sxs-lookup"><span data-stu-id="8d428-237">Supported Container access policy with new permission x,t</span></span>
    -  <span data-ttu-id="8d428-238">”New-AzStorageContainerStoredAccessPolicy”</span><span class="sxs-lookup"><span data-stu-id="8d428-238">'New-AzStorageContainerStoredAccessPolicy'</span></span>
    -  <span data-ttu-id="8d428-239">"Set-AzStorageContainerStoredAccessPolicy"</span><span class="sxs-lookup"><span data-stu-id="8d428-239">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
* <span data-ttu-id="8d428-240">Ändrade utdata från cmdleten hämta/ange åtkomstprincip för containrar genom att ändra behörighetstypen för den underordnade egenskapen från uppräkning till sträng</span><span class="sxs-lookup"><span data-stu-id="8d428-240">Changed the output of get/set Container access policy cmdlet, by change the child property Permission type from enum to String</span></span>
    -  <span data-ttu-id="8d428-241">"Get-AzStorageContainerStoredAccessPolicy"</span><span class="sxs-lookup"><span data-stu-id="8d428-241">'Get-AzStorageContainerStoredAccessPolicy'</span></span>
    -  <span data-ttu-id="8d428-242">"Set-AzStorageContainerStoredAccessPolicy"</span><span class="sxs-lookup"><span data-stu-id="8d428-242">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
* <span data-ttu-id="8d428-243">Korrigerade ett problem med exempelskript för att ange hanteringsprincip med JSON</span><span class="sxs-lookup"><span data-stu-id="8d428-243">Fixed a sample script issue of set management policy with json</span></span>
    -  <span data-ttu-id="8d428-244">"Set-AzStorageAccountManagementPolicy"</span><span class="sxs-lookup"><span data-stu-id="8d428-244">'Set-AzStorageAccountManagementPolicy'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8d428-245">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8d428-245">Az.Websites</span></span>
* <span data-ttu-id="8d428-246">Lade till stöd för Premium V3-prisnivån</span><span class="sxs-lookup"><span data-stu-id="8d428-246">Added support for Premium V3 pricing tier</span></span>
* <span data-ttu-id="8d428-247">Uppdaterade SDK för WebSites till 3.1.0</span><span class="sxs-lookup"><span data-stu-id="8d428-247">Updated the WebSites SDK to 3.1.0</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="8d428-248">Tack till våra community-deltagare</span><span class="sxs-lookup"><span data-stu-id="8d428-248">Thanks to our community contributors</span></span>
* <span data-ttu-id="8d428-249">@atul-ram, uppdatera Get-AzDelegation.md (#13176)</span><span class="sxs-lookup"><span data-stu-id="8d428-249">@atul-ram, Update Get-AzDelegation.md (#13176)</span></span>
* <span data-ttu-id="8d428-250">@dineshreddy007, hämta approller som har tilldelats korrekt om Stack HCI-registrering använder WAC-token.</span><span class="sxs-lookup"><span data-stu-id="8d428-250">@dineshreddy007, Get the App Roles assigned correctly in case of Stack HCI registration using WAC token.</span></span> <span data-ttu-id="8d428-251">(#13249)</span><span class="sxs-lookup"><span data-stu-id="8d428-251">(#13249)</span></span>
* <span data-ttu-id="8d428-252">@kongou-ae, uppdatera New-AzOffice365PolicyProperty.md (#13217)</span><span class="sxs-lookup"><span data-stu-id="8d428-252">@kongou-ae, Update New-AzOffice365PolicyProperty.md (#13217)</span></span>
* <span data-ttu-id="8d428-253">Lohith Chowdary Chilukuri (@Lochiluk), uppdatera Set-AzApplicationGateway.md (#13150)</span><span class="sxs-lookup"><span data-stu-id="8d428-253">Lohith Chowdary Chilukuri (@Lochiluk), Update Set-AzApplicationGateway.md (#13150)</span></span>
* <span data-ttu-id="8d428-254">Matthew Burleigh (@mburleigh)</span><span class="sxs-lookup"><span data-stu-id="8d428-254">Matthew Burleigh (@mburleigh)</span></span>
  * <span data-ttu-id="8d428-255">Lägg till länkar till de PowerShell-cmdletar som refereras i dokumentet (#13203)</span><span class="sxs-lookup"><span data-stu-id="8d428-255">Add links to PowerShell cmdlets referenced in the document (#13203)</span></span>
  * <span data-ttu-id="8d428-256">Lägg till länkar till de PowerShell-cmdletar som refereras i dokumentet (#13190)</span><span class="sxs-lookup"><span data-stu-id="8d428-256">Add links to PowerShell cmdlets referenced in the document (#13190)</span></span>
  * <span data-ttu-id="8d428-257">Lägg till länkar till de PowerShell-cmdletar som refereras i dokumentet (#13189)</span><span class="sxs-lookup"><span data-stu-id="8d428-257">Add links to PowerShell cmdlets referenced in the document (#13189)</span></span>
  * <span data-ttu-id="8d428-258">lägg till länkar till cmdletar som refereras (#13137)</span><span class="sxs-lookup"><span data-stu-id="8d428-258">add links to referenced cmdlets (#13137)</span></span>
  * <span data-ttu-id="8d428-259">Lägg till länkar till de PowerShell-cmdletar som refereras i dokumentet (#13204)</span><span class="sxs-lookup"><span data-stu-id="8d428-259">Add links to PowerShell cmdlets referenced in the document (#13204)</span></span>
  * <span data-ttu-id="8d428-260">Lägg till länkar till de PowerShell-cmdletar som refereras i dokumentet (#13205)</span><span class="sxs-lookup"><span data-stu-id="8d428-260">Add links to PowerShell cmdlets referenced in the document (#13205)</span></span>

## <a name="480---october-2020"></a><span data-ttu-id="8d428-261">4.8.0 – oktober 2020</span><span class="sxs-lookup"><span data-stu-id="8d428-261">4.8.0 - October 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8d428-262">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8d428-262">Az.Accounts</span></span>
* <span data-ttu-id="8d428-263">Åtgärdat DateTime-parsningsfel i vanliga bibliotek [#13045]</span><span class="sxs-lookup"><span data-stu-id="8d428-263">Fixed DateTime parse issue in common libraries [#13045]</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="8d428-264">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8d428-264">Az.CognitiveServices</span></span>
* <span data-ttu-id="8d428-265">Cmdleten New-AzCognitiveServicesAccountApiProperty har lagts till.</span><span class="sxs-lookup"><span data-stu-id="8d428-265">Added 'New-AzCognitiveServicesAccountApiProperty' cmdlet.</span></span>
* <span data-ttu-id="8d428-266">Stöd för parametern ApiProperty för New-AzCognitiveServicesAccount och Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="8d428-266">Supported 'ApiProperty' parameter for 'New-AzCognitiveServicesAccount' and 'Set-AzCognitiveServicesAccount'</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d428-267">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d428-267">Az.Compute</span></span>
* <span data-ttu-id="8d428-268">Åtgärdat problem i Update-ASRRecoveryPlan genom att fylla i FailoverTypes</span><span class="sxs-lookup"><span data-stu-id="8d428-268">Fixed issue in 'Update-ASRRecoveryPlan' by populating FailoverTypes</span></span>
* <span data-ttu-id="8d428-269">De valfria parametrarna -Top och -OrderBy har lagts till i cmdleten Get-AzVmImage.</span><span class="sxs-lookup"><span data-stu-id="8d428-269">Added the '-Top' and '-OrderBy' optional parameters to the 'Get-AzVmImage' cmdlet.</span></span> 

#### <a name="azdatabricks"></a><span data-ttu-id="8d428-270">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="8d428-270">Az.Databricks</span></span>
* <span data-ttu-id="8d428-271">Allmän tillgänglighet för modulen Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="8d428-271">General availability of 'Az.Databricks' module</span></span>
* <span data-ttu-id="8d428-272">Stöd har lagts till för virtuell nätverkspeering</span><span class="sxs-lookup"><span data-stu-id="8d428-272">Added support for virtual network peering</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8d428-273">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8d428-273">Az.DataFactory</span></span>
* <span data-ttu-id="8d428-274">Skrivfel har åtgärdats i utdatameddelanden</span><span class="sxs-lookup"><span data-stu-id="8d428-274">Fixed typo in output messages</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="8d428-275">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8d428-275">Az.EventHub</span></span>
* <span data-ttu-id="8d428-276">Den valfria switchparametern TrustedServiceAccessEnabled har lagts till i cmdleten Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="8d428-276">Added optional switch parameter 'TrustedServiceAccessEnabled' to 'Set-AzEventHubNetworkRuleSet' cmdlet</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="8d428-277">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8d428-277">Az.HDInsight</span></span>
* <span data-ttu-id="8d428-278">Ett varningsmeddelande om att parametrarna PublicNetworkAccessType och OutboundPublicNetworkAccessType planeras att göras inaktuella har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-278">Added warning message for planning to deprecate the parameters 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType'</span></span>
* <span data-ttu-id="8d428-279">Ett varningsmeddelande om att parametern DefaultStorageAccountName planeras att ersättas med StorageAccountResourceId har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-279">Added warning message for planning to replace the parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
* <span data-ttu-id="8d428-280">Ett varningsmeddelande om att parametern DefaultStorageAccountKey planeras att ersättas med StorageAccountKey har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-280">Added warning message for planning to replace the parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
* <span data-ttu-id="8d428-281">Ett varningsmeddelande om att parametern DefaultStorageAccountType planeras att ersättas med StorageAccountType har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-281">Added warning message for planning to replace the parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
* <span data-ttu-id="8d428-282">Ett varningsmeddelande om att parametern DefaultStorageContainer planeras att ersättas med StorageContainer har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-282">Added warning message for planning to replace the parameter 'DefaultStorageContainer' with 'StorageContainer'</span></span>
* <span data-ttu-id="8d428-283">Ett varningsmeddelande om att parametern DefaultStorageRootPath planeras att ersättas med StorageRootPath har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-283">Added warning message for planning to replace the parameter 'DefaultStorageRootPath' with 'StorageRootPath'</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8d428-284">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8d428-284">Az.IotHub</span></span>
* <span data-ttu-id="8d428-285">SDK för enheter har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="8d428-285">Updated devices sdk.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8d428-286">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8d428-286">Az.KeyVault</span></span>
* <span data-ttu-id="8d428-287">Detaljerat datum för borttagning av egenskapen SecretValueText har tillhandahållits</span><span class="sxs-lookup"><span data-stu-id="8d428-287">Provided the detailed date of removing property SecretValueText</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="8d428-288">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="8d428-288">Az.ManagedServices</span></span>
* <span data-ttu-id="8d428-289">Varningar om icke-bakåtkompatibla ändringar för cmdletar för tilldelning och definition av hanterade tjänster har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="8d428-289">Updated breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8d428-290">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8d428-290">Az.Monitor</span></span>
* <span data-ttu-id="8d428-291">Felet som gjorde att ett varningsmeddelande inte kunde ignoreras har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="8d428-291">Fixed the bug that warning message cannot be suppressed.</span></span> <span data-ttu-id="8d428-292">[#12889]</span><span class="sxs-lookup"><span data-stu-id="8d428-292">[#12889]</span></span>
* <span data-ttu-id="8d428-293">Stöd för parametern SkipMetricValidation i aviseringsregelvillkor.</span><span class="sxs-lookup"><span data-stu-id="8d428-293">Supported 'SkipMetricValidation' parameter in alert rule criteria.</span></span> <span data-ttu-id="8d428-294">Tillåter att du skapar en aviseringsregel för ett anpassat mått som inte har genererats än, genom att göra så att måttverifieringen hoppas över.</span><span class="sxs-lookup"><span data-stu-id="8d428-294">Allows creating an alert rule on a custom metric that isn't yet emitted, by causing the metric validation to be skipped.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8d428-295">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d428-295">Az.Network</span></span>
* <span data-ttu-id="8d428-296">Office365-princip har lagts till för VPNSite-resurs</span><span class="sxs-lookup"><span data-stu-id="8d428-296">Added Office365 Policy to VPNSite Resource</span></span>
    - <span data-ttu-id="8d428-297">New-AzO365PolicyProperty</span><span class="sxs-lookup"><span data-stu-id="8d428-297">'New-AzO365PolicyProperty'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8d428-298">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8d428-298">Az.RecoveryServices</span></span>
* <span data-ttu-id="8d428-299">Verifiering av containernamn har lagts till för arbetsbelastningssäkerhetskopior.</span><span class="sxs-lookup"><span data-stu-id="8d428-299">Added container name validation for workload backup.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="8d428-300">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="8d428-300">Az.RedisCache</span></span>
* <span data-ttu-id="8d428-301">En korrigering har gjorts så att cmdletarna New-AzRedisCache och Set-AzRedisCache inte misslyckas på grund av behörighetsproblem som rör registrering av Microsoft.Cache RP</span><span class="sxs-lookup"><span data-stu-id="8d428-301">Made 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets not fail because of permission issue related to registering Microsoft.Cache RP</span></span>

#### <a name="azsql"></a><span data-ttu-id="8d428-302">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d428-302">Az.Sql</span></span>
* <span data-ttu-id="8d428-303">BackupStorageRedundancy har lagts till i:</span><span class="sxs-lookup"><span data-stu-id="8d428-303">Added BackupStorageRedundancy to the following:</span></span> 
    - <span data-ttu-id="8d428-304">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8d428-304">'Restore-AzureRmSqlDatabase'</span></span>
    - <span data-ttu-id="8d428-305">New-AzSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="8d428-305">'New-AzSqlDatabaseCopy'</span></span>
    - <span data-ttu-id="8d428-306">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="8d428-306">'New-AzSqlDatabaseSecondary'</span></span>
* <span data-ttu-id="8d428-307">Skiftlägeskänslighet har tagits bort för parametern BackupStorageRedundancy för alla SQL DB-referenser</span><span class="sxs-lookup"><span data-stu-id="8d428-307">Removed case sensitivity for BackupStorageRedundancy parameter for all SQL DB references</span></span> 
* <span data-ttu-id="8d428-308">Namnen på BackupStorageRedundancy-varningsmeddelanden har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="8d428-308">Updated BackupStorageRedundancy warning message names</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8d428-309">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8d428-309">Az.Storage</span></span>
* <span data-ttu-id="8d428-310">Stöd för att aktivera/inaktivera/hämta egenskaper för mjuk borttagning av resurser för filtjänst för ett lagringskonto</span><span class="sxs-lookup"><span data-stu-id="8d428-310">Supported enable/disable/get share soft delete properties on file Service of a Storage account</span></span>
    - <span data-ttu-id="8d428-311">Update-AzStorageFileServiceProperty</span><span class="sxs-lookup"><span data-stu-id="8d428-311">'Update-AzStorageFileServiceProperty'</span></span>
    - <span data-ttu-id="8d428-312">Get-AzStorageFileServiceProperty</span><span class="sxs-lookup"><span data-stu-id="8d428-312">'Get-AzStorageFileServiceProperty'</span></span>
* <span data-ttu-id="8d428-313">Stöd för att visa filresurser inkluderar borttagna filresurser för ett lagringskonto och hämta förbrukning av enskild filresurs</span><span class="sxs-lookup"><span data-stu-id="8d428-313">Supported list file shares include the deleted ones of a Storage account, and Get single file share usage</span></span>
    - <span data-ttu-id="8d428-314">”Get-AzRmStorageShare”</span><span class="sxs-lookup"><span data-stu-id="8d428-314">'Get-AzRmStorageShare'</span></span>
* <span data-ttu-id="8d428-315">Stöd för återställning av en borttagen filresurs</span><span class="sxs-lookup"><span data-stu-id="8d428-315">Supported restore a deleted file share</span></span>
    - <span data-ttu-id="8d428-316">Restore-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="8d428-316">'Restore-AzRmStorageShare'</span></span>
* <span data-ttu-id="8d428-317">Cmdletarna för ändring av egenskaper för Blob Service har ändrats. De ursprungliga egenskaperna hämtas inte från servern utan anger bara de ändrade egenskaperna till servern.</span><span class="sxs-lookup"><span data-stu-id="8d428-317">Changed the cmdlets for modify blob service properties, won't get the original properties from server, but only set the modified properties to server.</span></span>
    - <span data-ttu-id="8d428-318">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8d428-318">'Enable-AzStorageBlobDeleteRetentionPolicy'</span></span>
    - <span data-ttu-id="8d428-319">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8d428-319">'Disable-AzStorageBlobDeleteRetentionPolicy'</span></span>  
    - <span data-ttu-id="8d428-320">"Enable-AzStorageBlobRestorePolicy"</span><span class="sxs-lookup"><span data-stu-id="8d428-320">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="8d428-321">"Disable-AzStorageBlobRestorePolicy"</span><span class="sxs-lookup"><span data-stu-id="8d428-321">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="8d428-322">”Update-AzStorageBlobServiceProperty”</span><span class="sxs-lookup"><span data-stu-id="8d428-322">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="8d428-323">Åtgärdat hjälpproblem för New-AzStorageAccount-parametern -Kind default value [#12189]</span><span class="sxs-lookup"><span data-stu-id="8d428-323">Fixed help issue for New-AzStorageAccount parameter -Kind default value [#12189]</span></span>
* <span data-ttu-id="8d428-324">Åtgärdat problem genom att lägga till exempel som visar hur ContentType anges på korrekt sätt i en blobuppladdning [#12989]</span><span class="sxs-lookup"><span data-stu-id="8d428-324">Fixed issue by add example to show how to set correct ContentType in blob upload [#12989]</span></span>

## <a name="470---september-2020"></a><span data-ttu-id="8d428-325">4.7.0 – September 2020</span><span class="sxs-lookup"><span data-stu-id="8d428-325">4.7.0 - September 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8d428-326">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8d428-326">Az.Accounts</span></span>
* <span data-ttu-id="8d428-327">Formaterat kommande meddelanden om icke-bakåtkompatibel ändring</span><span class="sxs-lookup"><span data-stu-id="8d428-327">Formatted the upcoming breaking change messages</span></span>
* <span data-ttu-id="8d428-328">Uppdaterat Azure.Core till 1.4.1</span><span class="sxs-lookup"><span data-stu-id="8d428-328">Updated Azure.Core to 1.4.1</span></span>

#### <a name="azaks"></a><span data-ttu-id="8d428-329">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="8d428-329">Az.Aks</span></span>
* <span data-ttu-id="8d428-330">Valideringslogiken för parametern "New-AzAksCluster", "Set-AzAksCluster" och "New-AzAksNodePool" har lagts till på klientsidan.</span><span class="sxs-lookup"><span data-stu-id="8d428-330">Added client side parameter validation logic for 'New-AzAksCluster', 'Set-AzAksCluster' and 'New-AzAksNodePool'.</span></span> <span data-ttu-id="8d428-331">[#12372]</span><span class="sxs-lookup"><span data-stu-id="8d428-331">[#12372]</span></span>
* <span data-ttu-id="8d428-332">Stöd har lagts till för tillägg i "New-AzAksCluster".</span><span class="sxs-lookup"><span data-stu-id="8d428-332">Added support for add-ons in 'New-AzAksCluster'.</span></span> <span data-ttu-id="8d428-333">[#11239]</span><span class="sxs-lookup"><span data-stu-id="8d428-333">[#11239]</span></span>
* <span data-ttu-id="8d428-334">Cmdlet:arna "Enable-AzAksAddOn" och "Disable-AzAksAddOn" har lagts till för tillägg.</span><span class="sxs-lookup"><span data-stu-id="8d428-334">Added cmdlets 'Enable-AzAksAddOn' and 'Disable-AzAksAddOn' for add-ons.</span></span> <span data-ttu-id="8d428-335">[#11239]</span><span class="sxs-lookup"><span data-stu-id="8d428-335">[#11239]</span></span>
* <span data-ttu-id="8d428-336">Parametern "GenerateSshKey" har lagts till för "New-AzAksCluster".</span><span class="sxs-lookup"><span data-stu-id="8d428-336">Added parameter 'GenerateSshKey' for 'New-AzAksCluster'.</span></span> <span data-ttu-id="8d428-337">[#12371]</span><span class="sxs-lookup"><span data-stu-id="8d428-337">[#12371]</span></span>
* <span data-ttu-id="8d428-338">API-versionen har uppdaterats till 2020-06-01.</span><span class="sxs-lookup"><span data-stu-id="8d428-338">Updated api version to 2020-06-01.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="8d428-339">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8d428-339">Az.CognitiveServices</span></span>
* <span data-ttu-id="8d428-340">Visade ytterligare juridiska villkor för vissa API:er.</span><span class="sxs-lookup"><span data-stu-id="8d428-340">Showed additional legal terms for certain APIs.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d428-341">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d428-341">Az.Compute</span></span>
* <span data-ttu-id="8d428-342">Den valfria parametern "EncryptionType" har lagts till i "New-AzVmDiskEncryptionSetConfig"</span><span class="sxs-lookup"><span data-stu-id="8d428-342">Added the '-EncryptionType' optional parameter to 'New-AzVmDiskEncryptionSetConfig'</span></span>
* <span data-ttu-id="8d428-343">Nya cmdlet:ar för ny resurs typ: DiskAccess "Get-AzDiskAccess", "New-AzDiskAccess", "Get-AzDiskAccess"</span><span class="sxs-lookup"><span data-stu-id="8d428-343">New cmdlets for new resource type: DiskAccess 'Get-AzDiskAccess', 'New-AzDiskAccess', 'Get-AzDiskAccess'</span></span>
* <span data-ttu-id="8d428-344">De valfria parametrarna "-DiskAccessId" och "-NetworkAccessPolicy" har lagts till i "New-AzSnapshotConfig"</span><span class="sxs-lookup"><span data-stu-id="8d428-344">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzSnapshotConfig'</span></span>
* <span data-ttu-id="8d428-345">De valfria parametrarna "-DiskAccessId" och "-NetworkAccessPolicy" har lagts till i "New-AzDiskConfig"</span><span class="sxs-lookup"><span data-stu-id="8d428-345">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzDiskConfig'</span></span>
* <span data-ttu-id="8d428-346">PatchStatus-egenskapen har lagts till i VirtualMachine-instansvyn</span><span class="sxs-lookup"><span data-stu-id="8d428-346">Added 'PatchStatus' property to VirtualMachine Instance View</span></span>
* <span data-ttu-id="8d428-347">Egenskapen "VMHealth" har lagts till i den virtuella datorns instansvy, vilket är det returnerade objektet när "get-AzVm" anropas med "-Status"</span><span class="sxs-lookup"><span data-stu-id="8d428-347">Added 'VMHealth' property to the virtual machine's instance view, which is the returned object when 'Get-AzVm' is invoked with '-Status'</span></span>
* <span data-ttu-id="8d428-348">Fältet "AssignedHost" har lagts till i instansvyerna "Get-AzVM" och "Get-AzVmss".</span><span class="sxs-lookup"><span data-stu-id="8d428-348">Added 'AssignedHost' field to 'Get-AzVM' and 'Get-AzVmss' instance views.</span></span> <span data-ttu-id="8d428-349">I fältet visas resurs-ID för den virtuella datorinstansen</span><span class="sxs-lookup"><span data-stu-id="8d428-349">The field shows the resource id of the virtual machine instance</span></span>
* <span data-ttu-id="8d428-350">Den valfria parametern "-SupportAutomaticPlacement" har lagts till i "New-AzHostGroup"</span><span class="sxs-lookup"><span data-stu-id="8d428-350">Added optional parameter '-SupportAutomaticPlacement' to 'New-AzHostGroup'</span></span> 
* <span data-ttu-id="8d428-351">Parametern "-HostGroupId" har lagts till i "New-AzVm" och "New-AzVmss"</span><span class="sxs-lookup"><span data-stu-id="8d428-351">Added the '-HostGroupId' parameter to 'New-AzVm' and 'New-AzVmss'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8d428-352">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8d428-352">Az.DataFactory</span></span>
* <span data-ttu-id="8d428-353">ADF .Net SDK har uppdaterats till version 4.11.0</span><span class="sxs-lookup"><span data-stu-id="8d428-353">Updated ADF .Net SDK version to 4.11.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="8d428-354">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8d428-354">Az.EventHub</span></span>
* <span data-ttu-id="8d428-355">Nya kluster-cmdlet:ar – "New-AzEventHubCluster", "Set-AzEventHubCluster", "Get-AzEventHubCluster", "Remove-AzEventHubCluster", "Get-AzEventHubClustersAvailableRegions" har lagts till.</span><span class="sxs-lookup"><span data-stu-id="8d428-355">Added new Cluster cmdlets - 'New-AzEventHubCluster', 'Set-AzEventHubCluster', 'Get-AzEventHubCluster', 'Remove-AzEventHubCluster', 'Get-AzEventHubClustersAvailableRegions'.</span></span>
* <span data-ttu-id="8d428-356">Åtgärdat för ärende #10722 : Korrigering för tilldelning av enbart lyssning till AuthorizationRule-rättigheter.</span><span class="sxs-lookup"><span data-stu-id="8d428-356">Fixed for issue #10722 : Fix for assigning only 'Listen' to AuthorizationRule rights.</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="8d428-357">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="8d428-357">Az.Functions</span></span>
* <span data-ttu-id="8d428-358">Möjligheten att skapa v2-funktioner i regioner som inte stöder det har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="8d428-358">Removed the ability to create v2 Functions in regions that do not support it.</span></span>
* <span data-ttu-id="8d428-359">Föråldrad PowerShell 6.2.</span><span class="sxs-lookup"><span data-stu-id="8d428-359">Deprecated PowerShell 6.2.</span></span> <span data-ttu-id="8d428-360">En varning har lagts till när en användare skapar en PowerShell 6.2-funktionsapp som uppmanar till att skapa en PowerShell 7.0-funktionsapp i stället.</span><span class="sxs-lookup"><span data-stu-id="8d428-360">Added a warning for when a user creates a PowerShell 6.2 function app that advises them to create a PowerShell 7.0 function app instead.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="8d428-361">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8d428-361">Az.HDInsight</span></span>
* <span data-ttu-id="8d428-362">Stöd för att skapa kluster med automatisk skalningskonfiguration</span><span class="sxs-lookup"><span data-stu-id="8d428-362">Supported creating cluster with Autoscale configuration</span></span>
    - <span data-ttu-id="8d428-363">Lägg till den nya parametern "AutoscaleConfiguration" till cmdleten ”New-AzHDInsightCluster”</span><span class="sxs-lookup"><span data-stu-id="8d428-363">Add new parameter 'AutoscaleConfiguration' to the cmdlet 'New-AzHDInsightCluster'</span></span>
* <span data-ttu-id="8d428-364">Stöd för att använda automatisk skalningskonfiguration i kluster</span><span class="sxs-lookup"><span data-stu-id="8d428-364">Supported operating cluster's Autoscale configuration</span></span>
    - <span data-ttu-id="8d428-365">Lägg till ny cmdlet "Get-AzHDInsihgtClusterAutoscaleConfiguration"</span><span class="sxs-lookup"><span data-stu-id="8d428-365">Add new cmdlet 'Get-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="8d428-366">Lägg till ny cmdlet "New-AzHDInsihgtClusterAutoscaleConfiguration"</span><span class="sxs-lookup"><span data-stu-id="8d428-366">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="8d428-367">Lägg till ny cmdlet "Set-AzHDInsihgtClusterAutoscaleConfiguration"</span><span class="sxs-lookup"><span data-stu-id="8d428-367">Add new cmdlet 'Set-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="8d428-368">Lägg till ny cmdlet "Remove-AzHDInsihgtClusterAutoscaleConfiguration"</span><span class="sxs-lookup"><span data-stu-id="8d428-368">Add new cmdlet 'Remove-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="8d428-369">Lägg till ny cmdlet "New-AzHDInsihgtClusterAutoscaleScheduleCondition"</span><span class="sxs-lookup"><span data-stu-id="8d428-369">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleScheduleCondition'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8d428-370">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8d428-370">Az.KeyVault</span></span>
* <span data-ttu-id="8d428-371">Stöd har lagts till för RBAC-auktorisering [#10557]</span><span class="sxs-lookup"><span data-stu-id="8d428-371">Added support for RBAC authorization [#10557]</span></span>
* <span data-ttu-id="8d428-372">Förbättrad felhantering i "Set-AzKeyVaultAccessPolicy" [#4007]</span><span class="sxs-lookup"><span data-stu-id="8d428-372">Enhanced error handling in 'Set-AzKeyVaultAccessPolicy' [#4007]</span></span>

#### <a name="azkusto"></a><span data-ttu-id="8d428-373">Az.Kusto</span><span class="sxs-lookup"><span data-stu-id="8d428-373">Az.Kusto</span></span>
* <span data-ttu-id="8d428-374">Allmän tillgänglighet för "Az.Kusto"-modulen</span><span class="sxs-lookup"><span data-stu-id="8d428-374">General availability of 'Az.Kusto' module</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8d428-375">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d428-375">Az.Network</span></span>
* <span data-ttu-id="8d428-376">[Viktig ändring] Uppdaterade nedanstående cmdlets för att justera resursens virtuella router och virtuella hubb</span><span class="sxs-lookup"><span data-stu-id="8d428-376">[Breaking Change] Updated below cmdlets to align resource virtual router and virtual hub</span></span>
    - <span data-ttu-id="8d428-377">"New-AzVirtualRouter":</span><span class="sxs-lookup"><span data-stu-id="8d428-377">'New-AzVirtualRouter':</span></span> 
        - <span data-ttu-id="8d428-378">Parametern-HostedSubnet har lagts till för att stödja underordnad resurs för IP-konfiguration</span><span class="sxs-lookup"><span data-stu-id="8d428-378">Added -HostedSubnet parameter to support IP configuration child resource</span></span>
        - <span data-ttu-id="8d428-379">-HostedGateway och -HostedGatewayId har tagits bort</span><span class="sxs-lookup"><span data-stu-id="8d428-379">deleted -HostedGateway and -HostedGatewayId</span></span>
    - <span data-ttu-id="8d428-380">'Get-AzVirtualRouter':</span><span class="sxs-lookup"><span data-stu-id="8d428-380">'Get-AzVirtualRouter':</span></span>
        - <span data-ttu-id="8d428-381">Parameteruppsättningen har lagts till på prenumerationsnivå</span><span class="sxs-lookup"><span data-stu-id="8d428-381">Added subscription level parameter set</span></span>
    - <span data-ttu-id="8d428-382">"Remove-AzVirtualRouter"</span><span class="sxs-lookup"><span data-stu-id="8d428-382">'Remove-AzVirtualRouter'</span></span>
    - <span data-ttu-id="8d428-383">"Add-AzVirtualRouterPeer"</span><span class="sxs-lookup"><span data-stu-id="8d428-383">'Add-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="8d428-384">"Get-AzVirtualRouterPeer"</span><span class="sxs-lookup"><span data-stu-id="8d428-384">'Get-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="8d428-385">"Remove-AzVirtualRouterPeer"</span><span class="sxs-lookup"><span data-stu-id="8d428-385">'Remove-AzVirtualRouterPeer'</span></span>
* <span data-ttu-id="8d428-386">Ny cmdlet har lagts till för Azure Express Route-port</span><span class="sxs-lookup"><span data-stu-id="8d428-386">Added new cmdlet for Azure Express Route Port</span></span>
    - <span data-ttu-id="8d428-387">"New-AzExpressRoutePortLOA"</span><span class="sxs-lookup"><span data-stu-id="8d428-387">'New-AzExpressRoutePortLOA'</span></span>
* <span data-ttu-id="8d428-388">Egenskapen RemoteBgpCommunities har lagts till i VirtualNetwork Peering-resursen</span><span class="sxs-lookup"><span data-stu-id="8d428-388">Added RemoteBgpCommunities property to the VirtualNetwork Peering Resource</span></span>
* <span data-ttu-id="8d428-389">Ändrade varningsmeddelandet för ”New-AzLoadBalancerFrontendIpConfig”, ”New-AzPublicIpAddress” och ”New-AzPublicIpPrefix”.</span><span class="sxs-lookup"><span data-stu-id="8d428-389">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>
* <span data-ttu-id="8d428-390">Lade till VpnGatewayIpConfigurations till "Get-AzVpnGateway"-utdata</span><span class="sxs-lookup"><span data-stu-id="8d428-390">Added VpnGatewayIpConfigurations to 'Get-AzVpnGateway' output</span></span>
* <span data-ttu-id="8d428-391">Åtgärdade bugg för "Set-AzApplicationGatewaySslCertificate" [#9488]</span><span class="sxs-lookup"><span data-stu-id="8d428-391">Fixed bug for 'Set-AzApplicationGatewaySslCertificate' [#9488]</span></span>
* <span data-ttu-id="8d428-392">Parametern "AllowActiveFTP" har lagts till i "AzureFirewall"</span><span class="sxs-lookup"><span data-stu-id="8d428-392">Added 'AllowActiveFTP' parameter to 'AzureFirewall'</span></span>
* <span data-ttu-id="8d428-393">Nedanstående kommandon för funktionen har uppdaterats: Aktivera konfiguration/borttagning för Internetsäkerhet på VirtualWan P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="8d428-393">Updated below commands for feature: Enable internet security set/remove on VirtualWan P2SVpnGateway.</span></span>
- <span data-ttu-id="8d428-394">"New-AzP2sVpnGateway" har uppdaterats": Den valfria växelparametern "EnableInternetSecurityFlag" har lagts till för kunder som anger värdet true för att aktivera Internetsäkerhet på P2SVpnGateway, som ska användas för plats-till-plats-klienter.</span><span class="sxs-lookup"><span data-stu-id="8d428-394">Updated 'New-AzP2sVpnGateway': Added optional switch parameter 'EnableInternetSecurityFlag' for customers to set true to enable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
- <span data-ttu-id="8d428-395">"Update-AzP2sVpnGateway" har uppdaterats: De valfria växelparametrarna "EnableInternetSecurityFlag" eller "DisableInternetSecurityFlag" har lagts till för kunder som anger värdet true/false för att aktivera/inaktivera Internetsäkerhet på P2SVpnGateway, som ska användas för plats-till-plats-klienter.</span><span class="sxs-lookup"><span data-stu-id="8d428-395">Updated 'Update-AzP2sVpnGateway': Added optional switch parameters 'EnableInternetSecurityFlag' or 'DisableInternetSecurityFlag' for customers to set true/false to enable/disable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
* <span data-ttu-id="8d428-396">Den nya cmdleten "Reset-AzP2sVpnGateway" har lagts till för att kunder ska kunna återställa/starta om sina VirtualWan-P2SVpnGateway för felsökning.</span><span class="sxs-lookup"><span data-stu-id="8d428-396">Added new cmdlet 'Reset-AzP2sVpnGateway' for customers to reset/reboot their VirtualWan P2SVpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="8d428-397">Den nya cmdleten "Reset-AzVpnGateway" har lagts till för att kunder ska kunna återställa/starta om VirtualWan VpnGateway för felsökning.</span><span class="sxs-lookup"><span data-stu-id="8d428-397">Added new cmdlet 'Reset-AzVpnGateway' for customers to reset/reboot their VirtualWan VpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="8d428-398">"Set-AzVirtualNetworkSubnetConfig" har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="8d428-398">Updated 'Set-AzVirtualNetworkSubnetConfig'</span></span>
    - <span data-ttu-id="8d428-399">Ange egenskaper för NSG och routningstabell för undernät till null om det anges explicit i parametrarna [#1548] [#9718]</span><span class="sxs-lookup"><span data-stu-id="8d428-399">Set NSG and Route Table properties of subnet to null if explicitly set in parameters [#1548][#9718]</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8d428-400">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8d428-400">Az.RecoveryServices</span></span>
* <span data-ttu-id="8d428-401">Åtgärdat borttagningstillståndet för säkerhetskopieringsobjekt.</span><span class="sxs-lookup"><span data-stu-id="8d428-401">Fixed the Delete State for workload Backup Items.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8d428-402">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d428-402">Az.Resources</span></span>
* <span data-ttu-id="8d428-403">Lagt till saknad kontroll för Set-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="8d428-403">Added missing check for Set-AzRoleAssignment</span></span>
* <span data-ttu-id="8d428-404">Attribut som medför icke-bakåtkompatibel ändring har lagts till i parametern "SubscriptionId" i "Get-AzResourceGroupDeploymentOperation"</span><span class="sxs-lookup"><span data-stu-id="8d428-404">Added breaking change attribute to 'SubscriptionId' parameter of 'Get-AzResourceGroupDeploymentOperation'</span></span>
* <span data-ttu-id="8d428-405">Uppdaterat What-If-cmdlets i ARM-mall så att resursändringar av typen 'Ignorera' visas sist</span><span class="sxs-lookup"><span data-stu-id="8d428-405">Updated ARM template What-If cmdlets to show 'Ignore' resource changes last</span></span>
* <span data-ttu-id="8d428-406">Åtgärdat serialiseringsproblem med säkra parametrar och matrisparametrar för distributionscmdlets [#12773]</span><span class="sxs-lookup"><span data-stu-id="8d428-406">Fixed secure and array parameter serialization issues for deployment cmdlets [#12773]</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8d428-407">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8d428-407">Az.ServiceFabric</span></span>
* <span data-ttu-id="8d428-408">Nya cmdletar har lagts till för hanterade kluster och nodtyper:</span><span class="sxs-lookup"><span data-stu-id="8d428-408">Added new cmdlets for managed clusters and node types:</span></span>
    - <span data-ttu-id="8d428-409">"New-AzServiceFabricManagedCluster"</span><span class="sxs-lookup"><span data-stu-id="8d428-409">'New-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="8d428-410">"Get-AzServiceFabricManagedCluster"</span><span class="sxs-lookup"><span data-stu-id="8d428-410">'Get-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="8d428-411">"Set-AzServiceFabricManagedCluster"</span><span class="sxs-lookup"><span data-stu-id="8d428-411">'Set-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="8d428-412">"Remove-AzServiceFabricManagedCluster"</span><span class="sxs-lookup"><span data-stu-id="8d428-412">'Remove-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="8d428-413">"Add-AzServiceFabricManagedClusterClientCertificate"</span><span class="sxs-lookup"><span data-stu-id="8d428-413">'Add-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="8d428-414">"Remove-AzServiceFabricManagedClusterClientCertificate"</span><span class="sxs-lookup"><span data-stu-id="8d428-414">'Remove-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="8d428-415">"New-AzServiceFabricManagedNodeType"</span><span class="sxs-lookup"><span data-stu-id="8d428-415">'New-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="8d428-416">"Get-AzServiceFabricManagedNodeType"</span><span class="sxs-lookup"><span data-stu-id="8d428-416">'Get-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="8d428-417">"Set-AzServiceFabricManagedNodeType"</span><span class="sxs-lookup"><span data-stu-id="8d428-417">'Set-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="8d428-418">"Remove-AzServiceFabricManagedNodeType"</span><span class="sxs-lookup"><span data-stu-id="8d428-418">'Remove-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="8d428-419">"Add-AzServiceFabricManagedNodeTypeVMExtension"</span><span class="sxs-lookup"><span data-stu-id="8d428-419">'Add-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="8d428-420">"Add-AzServiceFabricManagedNodeTypeVMSecret"</span><span class="sxs-lookup"><span data-stu-id="8d428-420">'Add-AzServiceFabricManagedNodeTypeVMSecret'</span></span>
    - <span data-ttu-id="8d428-421">"Remove-AzServiceFabricManagedNodeTypeVMExtension"</span><span class="sxs-lookup"><span data-stu-id="8d428-421">'Remove-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="8d428-422">"Restart-AzServiceFabricManagedNodeTyp"</span><span class="sxs-lookup"><span data-stu-id="8d428-422">'Restart-AzServiceFabricManagedNodeTyp'</span></span>
* <span data-ttu-id="8d428-423">Service Fabric SDK har uppgraderats till version 1.2.0 som använder Service Fabric-resursprovidern med API-version 2020-03-01 för aktuell modell och 2020-01-01-förhandsversion för hanterade kluster.</span><span class="sxs-lookup"><span data-stu-id="8d428-423">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2020-03-01 for the current model and 2020-01-01-preview for managed clusters.</span></span>

#### <a name="azsql"></a><span data-ttu-id="8d428-424">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d428-424">Az.Sql</span></span>
* <span data-ttu-id="8d428-425">BackupStorageRedundancy har lagts till i "New-AzSqlInstance" och "Get-AzSqlInstance"</span><span class="sxs-lookup"><span data-stu-id="8d428-425">Added BackupStorageRedundancy to 'New-AzSqlInstance' and 'Get-AzSqlInstance'</span></span>
* <span data-ttu-id="8d428-426">Cmdlet:en "Get-AzSqlServerActiveDirectoryOnlyAuthentication" har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-426">Added cmdlet 'Get-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="8d428-427">Cmdlet:en "Enable-AzSqlServerActiveDirectoryOnlyAuthentication" har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-427">Added cmdlet 'Enable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="8d428-428">Force-parametern har lagts till i "New-AzSqlInstance"</span><span class="sxs-lookup"><span data-stu-id="8d428-428">Added Force parameter to 'New-AzSqlInstance'</span></span>
* <span data-ttu-id="8d428-429">Cmdlet:ar för logguppspelningstjänst för hanterade databaser har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-429">Added cmdlets for Managed Database Log Replay service</span></span>
    - <span data-ttu-id="8d428-430">"Start-AzSqlInstanceDatabaseLogReplay"</span><span class="sxs-lookup"><span data-stu-id="8d428-430">'Start-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="8d428-431">"Get-AzSqlInstanceDatabaseLogReplay"</span><span class="sxs-lookup"><span data-stu-id="8d428-431">'Get-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="8d428-432">"Complete-AzSqlInstanceDatabaseLogReplay"</span><span class="sxs-lookup"><span data-stu-id="8d428-432">'Complete-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="8d428-433">"Stop-AzSqlInstanceDatabaseLogReplay"</span><span class="sxs-lookup"><span data-stu-id="8d428-433">'Stop-AzSqlInstanceDatabaseLogReplay'</span></span>
* <span data-ttu-id="8d428-434">Cmdlet:en "Get-AzSqlInstanceActiveDirectoryOnlyAuthentication" har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-434">Added cmdlet 'Get-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="8d428-435">Cmdlet:en "Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication" har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-435">Added cmdlet 'Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="8d428-436">Cmdlet:en "Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication" har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-436">Added cmdlet 'Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="8d428-437">Cmdletarna "New-AzSqlDatabaseImport" och "New-AzSqlDatabaseExport" har uppdaterats för att stödja funktioner för nätverksisolering</span><span class="sxs-lookup"><span data-stu-id="8d428-437">Updated cmdlets 'New-AzSqlDatabaseImport' and 'New-AzSqlDatabaseExport' to support network isolation functionality</span></span>
* <span data-ttu-id="8d428-438">Cmdleten "New-AzSqlDatabaseImportExisting" har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-438">Added cmdlet 'New-AzSqlDatabaseImportExisting'</span></span>
* <span data-ttu-id="8d428-439">Uppdaterade databas-cmdlet:ar som stöder typspecifikation av lagringsenhet för säkerhetskopiering</span><span class="sxs-lookup"><span data-stu-id="8d428-439">Updated Databases cmdlets to support backup storage type specification</span></span>
* <span data-ttu-id="8d428-440">Force-parametern har lagts till i "New-AzSqlDatabase"</span><span class="sxs-lookup"><span data-stu-id="8d428-440">Added Force parameter to 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="8d428-441">Varning för BackupStorageRedundancy-konfiguration har lagts till i utvalda regioner i "New-AzSqlDatabase"</span><span class="sxs-lookup"><span data-stu-id="8d428-441">Added warning for BackupStorageRedundancy configuration in select regions in 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="8d428-442">Uppdaterade ActiveDirectoryOnlyAuthentication-cmdletar för server och instans så att de innehåller ResourceId och InputObject</span><span class="sxs-lookup"><span data-stu-id="8d428-442">Updated ActiveDirectoryOnlyAuthentication cmdlets for server and instance to include ResourceId and InputObject</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8d428-443">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8d428-443">Az.Storage</span></span>
* <span data-ttu-id="8d428-444">Åtgärdade fel vid uppladdning av blob genom uppgradering till Microsoft.Azure.Storage.DataMovement 2.0.0 [#12220]</span><span class="sxs-lookup"><span data-stu-id="8d428-444">Fixed upload blob fail by upgrade to Microsoft.Azure.Storage.DataMovement 2.0.0 [#12220]</span></span>
* <span data-ttu-id="8d428-445">Stöd för återställning baserat på tidpunkt</span><span class="sxs-lookup"><span data-stu-id="8d428-445">Supported Point In Time Restore</span></span>
    - <span data-ttu-id="8d428-446">"Enable-AzStorageBlobRestorePolicy"</span><span class="sxs-lookup"><span data-stu-id="8d428-446">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="8d428-447">"Disable-AzStorageBlobRestorePolicy"</span><span class="sxs-lookup"><span data-stu-id="8d428-447">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="8d428-448">"New-AzStorageBlobRangeToRestore"</span><span class="sxs-lookup"><span data-stu-id="8d428-448">'New-AzStorageBlobRangeToRestore'</span></span>
    - <span data-ttu-id="8d428-449">"Restore-AzStorageBlobRange"</span><span class="sxs-lookup"><span data-stu-id="8d428-449">'Restore-AzStorageBlobRange'</span></span>
* <span data-ttu-id="8d428-450">Stöd för att hämta status för blobåterställning genom att köra get-AzureRMStorageAccount med parametern -IncludeBlobRestoreStatus</span><span class="sxs-lookup"><span data-stu-id="8d428-450">Supported get blob restore status of Storage account by run get-AzureRMStorageAccount with parameter -IncludeBlobRestoreStatus</span></span> 
    - <span data-ttu-id="8d428-451">"Get-AzureRMStorageAccount"</span><span class="sxs-lookup"><span data-stu-id="8d428-451">'Get-AzureRMStorageAccount'</span></span>
* <span data-ttu-id="8d428-452">Meddelande om icke-bakåtkompatibel ändring för kommande ändring av cmdlet-utdata har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-452">Added breaking change warning message for upcoming cmdlet output change</span></span>
    - <span data-ttu-id="8d428-453">"Get-AzStorageContainerStoredAccessPolicy"</span><span class="sxs-lookup"><span data-stu-id="8d428-453">'Get-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="8d428-454">"Set-AzStorageContainerStoredAccessPolicy"</span><span class="sxs-lookup"><span data-stu-id="8d428-454">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="8d428-455">"Set-AzStorageAccountManagementPolicy"</span><span class="sxs-lookup"><span data-stu-id="8d428-455">'Set-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="8d428-456">"Get-AzStorageAccountManagementPolicy"</span><span class="sxs-lookup"><span data-stu-id="8d428-456">'Get-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="8d428-457">"Add-AzStorageAccountManagementPolicyAction"</span><span class="sxs-lookup"><span data-stu-id="8d428-457">'Add-AzStorageAccountManagementPolicyAction'</span></span>
    - <span data-ttu-id="8d428-458">"New-AzStorageAccountManagementPolicyRule"</span><span class="sxs-lookup"><span data-stu-id="8d428-458">'New-AzStorageAccountManagementPolicyRule'</span></span>
* <span data-ttu-id="8d428-459">Uppgraderade Microsoft.Azure.Cosmos.Table SDK till 1.0.8</span><span class="sxs-lookup"><span data-stu-id="8d428-459">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.8</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="8d428-460">Tack till våra community-deltagare</span><span class="sxs-lookup"><span data-stu-id="8d428-460">Thanks to our community contributors</span></span>
* <span data-ttu-id="8d428-461">Thomas Van Laere (@ThomVanL), Lägg till Dockerfile-alpine-3.10 (#12911)</span><span class="sxs-lookup"><span data-stu-id="8d428-461">Thomas Van Laere (@ThomVanL), Add Dockerfile-alpine-3.10 (#12911)</span></span> 
* <span data-ttu-id="8d428-462">Lohith Chowdary Chilukuri (@Lochiluk), Uppdatering av Remove-AzNetworkInterfaceIpConfig.md (#12807)</span><span class="sxs-lookup"><span data-stu-id="8d428-462">Lohith Chowdary Chilukuri (@Lochiluk), Update Remove-AzNetworkInterfaceIpConfig.md (#12807)</span></span> 
* <span data-ttu-id="8d428-463">Roberth Strand (@roberthstrand), Get-AzResourceGroup – Nytt exempel och rensning (#12828)</span><span class="sxs-lookup"><span data-stu-id="8d428-463">Roberth Strand (@roberthstrand), Get-AzResourceGroup - New example, and cleanup (#12828)</span></span> 
* <span data-ttu-id="8d428-464">Ravi Mishra (@inmishrar), uppdatering av Azure Web App-körningsstack till DOTNETCORE (#12833)</span><span class="sxs-lookup"><span data-stu-id="8d428-464">Ravi Mishra (@inmishrar), update Azure Web App runtime stack to DOTNETCORE (#12833)</span></span> 
* <span data-ttu-id="8d428-465">@jack-education, uppdaterat set-AzVirtualNetworkSubnetConfig för att tillåta att NSG och routningstabell tas bort från undernät (#12351)</span><span class="sxs-lookup"><span data-stu-id="8d428-465">@jack-education, Updated Set-AzVirtualNetworkSubnetConfig to allow NSG and Route Table to be removed from subnet (#12351)</span></span> 
* <span data-ttu-id="8d428-466">@hagop-globanet, uppdatering av Add-AzApplicationGatewayCustomError.md (#12784)</span><span class="sxs-lookup"><span data-stu-id="8d428-466">@hagop-globanet, Update Add-AzApplicationGatewayCustomError.md (#12784)</span></span> 
* <span data-ttu-id="8d428-467">Joshua Van Daalen (@greenSacrifice)</span><span class="sxs-lookup"><span data-stu-id="8d428-467">Joshua Van Daalen (@greenSacrifice)</span></span>
  * <span data-ttu-id="8d428-468">Uppdatering av stavning av egenskaper till egenskaper (#12821)</span><span class="sxs-lookup"><span data-stu-id="8d428-468">Update spelling of Property to Property (#12821)</span></span> 
  * <span data-ttu-id="8d428-469">Uppdatering av New-AzResourceLock.md-exempel (#12806)</span><span class="sxs-lookup"><span data-stu-id="8d428-469">Update New-AzResourceLock.md examples (#12806)</span></span>
* <span data-ttu-id="8d428-470">Eragon Riddle (@eragonriddle), korrigerat fältnamn för parameter i exemplet (#12825)</span><span class="sxs-lookup"><span data-stu-id="8d428-470">Eragon Riddle (@eragonriddle), Corrected parameter field name in the example (#12825)</span></span> 
* <span data-ttu-id="8d428-471">@rossifumax, åtgärdat skrivfel i New-AzConfigurationAssignment.md (#12701)</span><span class="sxs-lookup"><span data-stu-id="8d428-471">@rossifumax, Fix typo in New-AzConfigurationAssignment.md (#12701)</span></span>

## <a name="461---august-2020"></a><span data-ttu-id="8d428-472">4.6.1 – augusti 2020</span><span class="sxs-lookup"><span data-stu-id="8d428-472">4.6.1 - August 2020</span></span>
#### <a name="azcompute"></a><span data-ttu-id="8d428-473">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d428-473">Az.Compute</span></span>
* <span data-ttu-id="8d428-474">Korrigerade EncryptionAtHost-parametern i New-AzVm för att ta bort standardvärdet FALSE [#12776]</span><span class="sxs-lookup"><span data-stu-id="8d428-474">Patched '-EncryptionAtHost' parameter in 'New-AzVm' to remove default value of false [#12776]</span></span>

## <a name="460---august-2020"></a><span data-ttu-id="8d428-475">4.6.0 – augusti 2020</span><span class="sxs-lookup"><span data-stu-id="8d428-475">4.6.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8d428-476">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8d428-476">Az.Accounts</span></span>
* <span data-ttu-id="8d428-477">Alla offentliga molnmiljöer läses in när slutpunktsidentifieringen inte returnerar AzureCloud (standard) eller andra offentliga miljöer [#12633]</span><span class="sxs-lookup"><span data-stu-id="8d428-477">Loaded all public cloud environments when discovery endpoint doesn't return default AzureCloud or other public environments [#12633]</span></span>
* <span data-ttu-id="8d428-478">SubscriptionPolicies har exponerats i Get-AzSubscription [#12551]</span><span class="sxs-lookup"><span data-stu-id="8d428-478">Exposed SubscriptionPolicies in 'Get-AzSubscription' [#12551]</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8d428-479">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8d428-479">Az.Automation</span></span>
* <span data-ttu-id="8d428-480">Parametern -RunOn har lagts till i Set-AzAutomationWebhook för att ange en Hybrid Worker-grupp</span><span class="sxs-lookup"><span data-stu-id="8d428-480">Added '-RunOn' parameters to 'Set-AzAutomationWebhook' to specify a Hybrid Worker Group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d428-481">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d428-481">Az.Compute</span></span>
* <span data-ttu-id="8d428-482">Parametern -EncryptionAtHost har lagts till i New-AzVm, New-AzVmss, New-AzVMConfig, New-AzVmssConfig, Update-AzVM och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8d428-482">Added '-EncryptionAtHost' parameter to 'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM', and 'Update-AzVmss'</span></span>
* <span data-ttu-id="8d428-483">SecurityProfile har lagts till i Get-AzVM och Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8d428-483">Added 'SecurityProfile' to 'Get-AzVM' and 'Get-AzVmss' return object</span></span>
* <span data-ttu-id="8d428-484">Växeln -InstanceView har lagts till som valfri parameter i Get-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="8d428-484">Added '-InstanceView' switch as optional parameter to 'Get-AzHostGroup'</span></span>
* <span data-ttu-id="8d428-485">En ny cmdlet, Invoke-AzVmPatchAssessment, har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-485">Added new cmdlet 'Invoke-AzVmPatchAssessment'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8d428-486">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8d428-486">Az.DataFactory</span></span>
* <span data-ttu-id="8d428-487">Saknade egenskaper har lagts till i klassen PSPipelineRun.</span><span class="sxs-lookup"><span data-stu-id="8d428-487">Added missing properties to PSPipelineRun class.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="8d428-488">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8d428-488">Az.HDInsight</span></span>
* <span data-ttu-id="8d428-489">Stöd för att skapa kluster med funktionen för kryptering under överföring.</span><span class="sxs-lookup"><span data-stu-id="8d428-489">Supported creating cluster with encryption at host feature.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8d428-490">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8d428-490">Az.KeyVault</span></span>
* <span data-ttu-id="8d428-491">Varningsmeddelanden har lagts till för planering att inaktivera mjuk borttagning</span><span class="sxs-lookup"><span data-stu-id="8d428-491">Added warning messages for planning to disable soft delete</span></span>
* <span data-ttu-id="8d428-492">Varningsmeddelanden har lagts till för planering att ta bort attributet SecretValueText</span><span class="sxs-lookup"><span data-stu-id="8d428-492">Added warning messages for planning to remove attribute SecretValueText</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="8d428-493">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="8d428-493">Az.Maintenance</span></span>
* <span data-ttu-id="8d428-494">Valfria schemarelaterade fält har lagts till i New-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="8d428-494">Added optional schedule related fields to 'New-AzMaintenanceConfiguration'</span></span>
* <span data-ttu-id="8d428-495">En ny cmdlet har lagts till för Get-AzMaintenancePublicConfiguration</span><span class="sxs-lookup"><span data-stu-id="8d428-495">Added new cmdlet for 'Get-AzMaintenancePublicConfiguration'</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="8d428-496">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="8d428-496">Az.ManagedServices</span></span>
* <span data-ttu-id="8d428-497">Varningar har lagts till om icke-bakåtkompatibla ändringar för cmdletar för tilldelning och definition av hanterade tjänster</span><span class="sxs-lookup"><span data-stu-id="8d428-497">Added breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8d428-498">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8d428-498">Az.Monitor</span></span>
* <span data-ttu-id="8d428-499">Utökade parametern som angetts i Set-AzDiagnosticSetting för separering av aktivering av loggar och mått [#12482]</span><span class="sxs-lookup"><span data-stu-id="8d428-499">Extended the parameter set in 'Set-AzDiagnosticSetting' for separation of Logs and Metrics enablement [#12482]</span></span>
* <span data-ttu-id="8d428-500">Åtgärdat fel för Add-AzMetricAlertRuleV2 vid hämtning av måttavisering från pipelinen</span><span class="sxs-lookup"><span data-stu-id="8d428-500">Fixed bug for 'Add-AzMetricAlertRuleV2' when getting metric alert from pipeline</span></span>

#### <a name="azresources"></a><span data-ttu-id="8d428-501">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d428-501">Az.Resources</span></span>
* <span data-ttu-id="8d428-502">Get-AzPolicyAlias-svaret har uppdaterats för att ta med information som anger om aliaset kan ändras eller inte av Azure Policy.</span><span class="sxs-lookup"><span data-stu-id="8d428-502">Updated 'Get-AzPolicyAlias' response to include information indicating whether the alias is modifiable by Azure Policy.</span></span>
* <span data-ttu-id="8d428-503">Skapade en ny cmdlet, set-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="8d428-503">Created new cmdlet 'Set-AzRoleAssignment'</span></span>
* <span data-ttu-id="8d428-504">Get-AzDeploymentManagementGroupWhatIfResult har lagts till för att hämta What-If-resultat för ARM-mall i hanteringsgruppsomfånget</span><span class="sxs-lookup"><span data-stu-id="8d428-504">Added 'Get-AzDeploymentManagementGroupWhatIfResult' for getting ARM template What-If results at management Group scope</span></span>
* <span data-ttu-id="8d428-505">En ny cmdlet, Get-AzTenantWhatIfResult, har lagts till för att hämta What-If-resultat för ARM-mall i klientorganisationsomfånget</span><span class="sxs-lookup"><span data-stu-id="8d428-505">Added 'Get-AzTenantWhatIfResult' new cmdlet for getting ARM template What-If results at tenant scope</span></span>
* <span data-ttu-id="8d428-506">-WhatIf och -Confirm har åsidosatts för New-AzManagementGroupDeployment och New-AzTenantDeployment för att använda What-If-resultat för ARM-mall</span><span class="sxs-lookup"><span data-stu-id="8d428-506">Overrode '-WhatIf' and '-Confirm' for 'New-AzManagementGroupDeployment' and 'New-AzTenantDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="8d428-507">Beteenden har åtgärdats för -WhatIf och -Confirm för nya cmdletar för distribution så att de stämmer överens med False och</span><span class="sxs-lookup"><span data-stu-id="8d428-507">Fixed the behaviors of '-WhatIf' and '-Confirm' for new deployment cmdlets so they comply with False and</span></span> 
* <span data-ttu-id="8d428-508">Serialiseringsfel har åtgärdats för -TemplateObject och TemplateParameterObject [#1528] [#6292]</span><span class="sxs-lookup"><span data-stu-id="8d428-508">Fixed serialization error for '-TemplateObject' and 'TemplateParameterObject' [#1528] [#6292]</span></span>
* <span data-ttu-id="8d428-509">Attribut som medför icke-bakåtkompatibel ändring har lagts till i Get-AzResourceGroupDeploymentOperation för den kommande ändringen av utdatatyp</span><span class="sxs-lookup"><span data-stu-id="8d428-509">Added breaking change attribute to 'Get-AzResourceGroupDeploymentOperation' for the upcoming output type change</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="8d428-510">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="8d428-510">Az.SignalR</span></span>
* <span data-ttu-id="8d428-511">Fel i hjälpfilerna Restart-AzSignalR och Update-AzSignalR har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8d428-511">Fixed 'Restart-AzSignalR' and 'Update-AzSignalR' help files errors</span></span>
* <span data-ttu-id="8d428-512">Cmdletarna Update-AzSignalRNetworkAcl och Set-AzSignalRUpstream har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-512">Added cmdlets 'Update-AzSignalRNetworkAcl', 'Set-AzSignalRUpstream'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8d428-513">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8d428-513">Az.Storage</span></span>
* <span data-ttu-id="8d428-514">Stöd för blobfrågeacceleration</span><span class="sxs-lookup"><span data-stu-id="8d428-514">Supported blob query acceleration</span></span>
    -  <span data-ttu-id="8d428-515">Get-AzStorageBlobQueryResult</span><span class="sxs-lookup"><span data-stu-id="8d428-515">'Get-AzStorageBlobQueryResult'</span></span>
    -  <span data-ttu-id="8d428-516">New-AzStorageBlobQueryConfig</span><span class="sxs-lookup"><span data-stu-id="8d428-516">'New-AzStorageBlobQueryConfig'</span></span>
* <span data-ttu-id="8d428-517">Hjälpfil har lagts till, ytterligare beskrivning har lagts till och stavfel har korrigerats</span><span class="sxs-lookup"><span data-stu-id="8d428-517">Updated help file, added more description, and fixed typo</span></span>
    -  <span data-ttu-id="8d428-518">”Start-AzStorageBlobCopy”</span><span class="sxs-lookup"><span data-stu-id="8d428-518">'Start-AzStorageBlobCopy'</span></span>
    -  <span data-ttu-id="8d428-519">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="8d428-519">'Get-AzDataLakeGen2Item'</span></span>
* <span data-ttu-id="8d428-520">Problem med att ladda ned blob när relaterad underordnad katalog saknas har åtgärdats [#12592]</span><span class="sxs-lookup"><span data-stu-id="8d428-520">Fixed download blob fail when related sub directory not exist [#12592]</span></span>
    -  <span data-ttu-id="8d428-521">”Get-AzStorageBlobContent”</span><span class="sxs-lookup"><span data-stu-id="8d428-521">'Get-AzStorageBlobContent'</span></span>
* <span data-ttu-id="8d428-522">Replikeringsprincip för att ange, hämta, ta bort objekt på Storage-konton stöds</span><span class="sxs-lookup"><span data-stu-id="8d428-522">Supported Set/Get/Remove Object Replication Policy on Storage accounts</span></span>
    - <span data-ttu-id="8d428-523">New-AzStorageObjectReplicationPolicyRule</span><span class="sxs-lookup"><span data-stu-id="8d428-523">'New-AzStorageObjectReplicationPolicyRule'</span></span>
    - <span data-ttu-id="8d428-524">Set-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="8d428-524">'Set-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="8d428-525">Get-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="8d428-525">'Get-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="8d428-526">Remove-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="8d428-526">'Remove-AzStorageObjectReplicationPolicy'</span></span>
* <span data-ttu-id="8d428-527">Stöd har lagts till för att aktivera/inaktivera ChangeFeed i Blob Service för ett Storage-konto</span><span class="sxs-lookup"><span data-stu-id="8d428-527">Supported enable/disable ChangeFeed on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="8d428-528">”Update-AzStorageBlobServiceProperty”</span><span class="sxs-lookup"><span data-stu-id="8d428-528">'Update-AzStorageBlobServiceProperty'</span></span>

## <a name="450---august-2020"></a><span data-ttu-id="8d428-529">4.5.0 – augusti 2020</span><span class="sxs-lookup"><span data-stu-id="8d428-529">4.5.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8d428-530">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8d428-530">Az.Accounts</span></span>
* <span data-ttu-id="8d428-531">Uppdaterade ”Connect-AzAccount” så att det accepterar parametern ”MaxContextPopulation” [#9865]</span><span class="sxs-lookup"><span data-stu-id="8d428-531">Updated 'Connect-AzAccount' to accept parameter 'MaxContextPopulation' [#9865]</span></span>
* <span data-ttu-id="8d428-532">Uppdaterade SubscriptionClient-versionen till 2019-06-01 och visa klientdomäner [#9838]</span><span class="sxs-lookup"><span data-stu-id="8d428-532">Updated SubscriptionClient version to 2019-06-01 and display tenant domains [#9838]</span></span>
* <span data-ttu-id="8d428-533">Information om hemklientorganisation och managedBy-klientorganisation som stöds för prenumerationen</span><span class="sxs-lookup"><span data-stu-id="8d428-533">Supported home tenant and managedBy tenant information of subscription</span></span>
* <span data-ttu-id="8d428-534">Korrigerade modulnamn, versionsinformation i telemetridata</span><span class="sxs-lookup"><span data-stu-id="8d428-534">Corrected module name, version info in telemetry data</span></span>
* <span data-ttu-id="8d428-535">Justerade SqlDatabaseDnsSuffix och ServiceManagementUrl om miljöns slutpunkt för metadata returnerar ett inkompatibelt värde</span><span class="sxs-lookup"><span data-stu-id="8d428-535">Adjusted SqlDatabaseDnsSuffix and ServiceManagementUrl if environment metadata endpoint returns incompatible value</span></span>

#### <a name="azaks"></a><span data-ttu-id="8d428-536">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="8d428-536">Az.Aks</span></span>
* <span data-ttu-id="8d428-537">Tog bort ”ClientIdAndSecret” för ”ServicePrincipalIdAndSecret” och ställde in ”ClientIdAndSecret” som ett alias [#12381].</span><span class="sxs-lookup"><span data-stu-id="8d428-537">Removed 'ClientIdAndSecret' to 'ServicePrincipalIdAndSecret' and set 'ClientIdAndSecret' as an alias [#12381].</span></span>
* <span data-ttu-id="8d428-538">Tog bort ”Get-AzAks”/”New-AzAks”/”Remove-AzAks”/”Set-AzAks” för ”Get-AzAksCluster”/”New-AzAksCluster”/”Remove-AzAksCluster”/”Set-AzAksCluster” och ställde in de ursprungliga som alias [#12373].</span><span class="sxs-lookup"><span data-stu-id="8d428-538">Removed 'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' to 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' and set the original ones as alias [#12373].</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="8d428-539">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8d428-539">Az.ApiManagement</span></span>
* <span data-ttu-id="8d428-540">Lade till ny cmdlet: ”Add-AzApiManagementApiToGateway”.</span><span class="sxs-lookup"><span data-stu-id="8d428-540">Added new 'Add-AzApiManagementApiToGateway' cmdlet.</span></span>
* <span data-ttu-id="8d428-541">Lade till ny cmdlet: ”Get-AzApiManagementGateway”.</span><span class="sxs-lookup"><span data-stu-id="8d428-541">Added new 'Get-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="8d428-542">Lade till ny cmdlet: ”Get-AzApiManagementGatewayHostnameConfiguration”.</span><span class="sxs-lookup"><span data-stu-id="8d428-542">Added new 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="8d428-543">Lade till ny cmdlet: ”Get-AzApiManagementGatewayKey”.</span><span class="sxs-lookup"><span data-stu-id="8d428-543">Added new 'Get-AzApiManagementGatewayKey' cmdlet.</span></span>
* <span data-ttu-id="8d428-544">Lade till ny cmdlet: ”New-AzApiManagementGateway”.</span><span class="sxs-lookup"><span data-stu-id="8d428-544">Added new 'New-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="8d428-545">Lade till ny cmdlet: ”New-AzApiManagementGatewayHostnameConfiguration”.</span><span class="sxs-lookup"><span data-stu-id="8d428-545">Added new 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="8d428-546">Lade till ny cmdlet: ”New-AzApiManagementResourceLocationObject”.</span><span class="sxs-lookup"><span data-stu-id="8d428-546">Added new 'New-AzApiManagementResourceLocationObject' cmdlet.</span></span>
* <span data-ttu-id="8d428-547">Lade till ny cmdlet: ”Remove-AzApiManagementApiFromGateway”.</span><span class="sxs-lookup"><span data-stu-id="8d428-547">Added new 'Remove-AzApiManagementApiFromGateway' cmdlet.</span></span>
* <span data-ttu-id="8d428-548">Lade till ny cmdlet: ”Remove-AzApiManagementGateway”.</span><span class="sxs-lookup"><span data-stu-id="8d428-548">Added new 'Remove-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="8d428-549">Lade till ny cmdlet: ”Remove-AzApiManagementGatewayHostnameConfiguration”.</span><span class="sxs-lookup"><span data-stu-id="8d428-549">Added new 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="8d428-550">Lade till ny cmdlet: ”Update-AzApiManagementGateway”.</span><span class="sxs-lookup"><span data-stu-id="8d428-550">Added new 'Update-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="8d428-551">Lade till den nya valfria parametern [-GatewayId] till cmdleten ”Get-AzApiManagementApi”.</span><span class="sxs-lookup"><span data-stu-id="8d428-551">Added new optional [-GatewayId] parameter to the 'Get-AzApiManagementApi' cmdlet.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="8d428-552">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8d428-552">Az.CognitiveServices</span></span>
* <span data-ttu-id="8d428-553">Använde ”Neka” som standardåtgärd för NetworkRules.</span><span class="sxs-lookup"><span data-stu-id="8d428-553">Used 'Deny' specifically as NetworkRules default action.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="8d428-554">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="8d428-554">Az.FrontDoor</span></span>
* <span data-ttu-id="8d428-555">Åtgärdade ett problem där ett undantag uppstår när Enum.Parse försöker att tvinga ett null-värde till aktiverade eller inaktiverade uppräkningsvärden [#12344]</span><span class="sxs-lookup"><span data-stu-id="8d428-555">Fixed an issue where an exception is being thrown when Enum.Parse tries to coerce a null value to an Enabled or Disabled enum values [#12344]</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="8d428-556">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8d428-556">Az.HDInsight</span></span>
* <span data-ttu-id="8d428-557">Stöd för att skapa kluster med funktionen Kryptering under överföring.</span><span class="sxs-lookup"><span data-stu-id="8d428-557">Supported creating cluster with encryption in transit feature.</span></span>
    - <span data-ttu-id="8d428-558">Lägg till den nya parametern ”EncryptionInTransit” till cmdleten ”New-AzHDInsightCluster”</span><span class="sxs-lookup"><span data-stu-id="8d428-558">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="8d428-559">Lägg till den nya parametern ”EncryptionInTransit” till cmdleten ”New-AzHDInsightClusterConfig”</span><span class="sxs-lookup"><span data-stu-id="8d428-559">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="8d428-560">Stöd för att skapa kluster med funktionen privat länk:</span><span class="sxs-lookup"><span data-stu-id="8d428-560">Supported creating cluster with private link feature:</span></span>
    - <span data-ttu-id="8d428-561">Lägg till de nya parametrarna ”PublicNetworkAccessType” och ”OutboundPublicNetworkAccessType” till cmdleten ”New-AzHDInsightCluster”</span><span class="sxs-lookup"><span data-stu-id="8d428-561">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="8d428-562">Lägg till de nya parametrarna ”PublicNetworkAccessType” och ”OutboundPublicNetworkAccessType” till cmdleten ”New-AzHDInsightClusterConfig”</span><span class="sxs-lookup"><span data-stu-id="8d428-562">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="8d428-563">Returnerade information om det virtuella nätverket vid anrop till ”New-AzHDInsightCluster” eller ”Get-AzHDInsightCluster”</span><span class="sxs-lookup"><span data-stu-id="8d428-563">Returned virtual network information when calling 'New-AzHDInsightCluster' or 'Get-AzHDInsightCluster'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8d428-564">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d428-564">Az.Network</span></span>
* <span data-ttu-id="8d428-565">Stöd har lagts till för parametern AddressPrefixType i ”Remove-AzExpressRouteCircuitConnectionConfig”</span><span class="sxs-lookup"><span data-stu-id="8d428-565">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="8d428-566">Lade till bakåtkompatibel ändringar: PeerAddressType-funktioner för privat peering i ”Remove-AzExpressRouteCircutPeeringConfig”.</span><span class="sxs-lookup"><span data-stu-id="8d428-566">Added non-breaking changes: PeerAddressType functionality for Private Peering in 'Remove-AzExpressRouteCircutPeeringConfig'.</span></span>
* <span data-ttu-id="8d428-567">Koden ändrades för att ignorera skiftläge för parametrarna AddressPrefixType och PeerAddressType.</span><span class="sxs-lookup"><span data-stu-id="8d428-567">Code changed to ignore case for AddressPrefixType and PeerAddressType parameter.</span></span>
* <span data-ttu-id="8d428-568">Ändrade varningsmeddelandet för ”New-AzLoadBalancerFrontendIpConfig”, ”New-AzPublicIpAddress” och ”New-AzPublicIpPrefix”.</span><span class="sxs-lookup"><span data-stu-id="8d428-568">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8d428-569">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8d428-569">Az.OperationalInsights</span></span>
* <span data-ttu-id="8d428-570">Lade till alternativet ”-ForceDelete” för ”Remove-AzOperationalInsightsworkspace”</span><span class="sxs-lookup"><span data-stu-id="8d428-570">Added '-ForceDelete' option for 'Remove-AzOperationalInsightsworkspace'</span></span>
* <span data-ttu-id="8d428-571">Lade till ny cmdlet: ”Get-AzOperationalInsightsDeletedWorkspace”</span><span class="sxs-lookup"><span data-stu-id="8d428-571">Added new cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'</span></span>
* <span data-ttu-id="8d428-572">Lade till ny cmdlet: ”Restore-AzOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="8d428-572">Added new cmdlet 'Restore-AzOperationalInsightsWorkspace'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8d428-573">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8d428-573">Az.RecoveryServices</span></span>
* <span data-ttu-id="8d428-574">Förbättrade sättet Azure Backup-containrar/objekt identifieras.</span><span class="sxs-lookup"><span data-stu-id="8d428-574">Improved the Azure Backup container/item discovery experience.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8d428-575">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d428-575">Az.Resources</span></span>
* <span data-ttu-id="8d428-576">Lade till egenskaperna ”Condition”, ”ConditionVersion” och ”Description” till ”New-AzRoleAssignment”</span><span class="sxs-lookup"><span data-stu-id="8d428-576">Added properties 'Condition', 'ConditionVersion' and 'Description' to 'New-AzRoleAssignment'</span></span>
    - <span data-ttu-id="8d428-577">Detta omfattade alla relevanta ändringar av datamodellerna</span><span class="sxs-lookup"><span data-stu-id="8d428-577">This included all the relevant changes to the data models</span></span>

#### <a name="azsql"></a><span data-ttu-id="8d428-578">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d428-578">Az.Sql</span></span>
* <span data-ttu-id="8d428-579">Korrigerade ett potentiellt fel med skiftlägesokänsliga servernamn i ”New-AzSqlServer” och ”Set-AzSqlServer”</span><span class="sxs-lookup"><span data-stu-id="8d428-579">Fixed potential server name case insensitive error in 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="8d428-580">Korrigerade att fel databasnamn returnerades vid ett befintligt databasfel i ”New-AzSqlDatabaseSecondary”</span><span class="sxs-lookup"><span data-stu-id="8d428-580">Fixed wrong database name returned on existing database error in 'New-AzSqlDatabaseSecondary'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8d428-581">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8d428-581">Az.Storage</span></span>
* <span data-ttu-id="8d428-582">Stöd för att skapa container/blob för SAS-token med de nya behörigheterna x, t</span><span class="sxs-lookup"><span data-stu-id="8d428-582">Supported create container/blob Sas token with new permission x,t</span></span>
    -  <span data-ttu-id="8d428-583">”New-AzStorageBlobSASToken”</span><span class="sxs-lookup"><span data-stu-id="8d428-583">'New-AzStorageBlobSASToken'</span></span>
    -  <span data-ttu-id="8d428-584">”New-AzStorageContainerSASToken”</span><span class="sxs-lookup"><span data-stu-id="8d428-584">'New-AzStorageContainerSASToken'</span></span>
* <span data-ttu-id="8d428-585">Stöd för att skapa konto för SAS-token med de nya behörigheterna x, t, f</span><span class="sxs-lookup"><span data-stu-id="8d428-585">Supported create account Sas token with new permission x,t,f</span></span>
    -  <span data-ttu-id="8d428-586">”New-AzStorageAccountSASToken”</span><span class="sxs-lookup"><span data-stu-id="8d428-586">'New-AzStorageAccountSASToken'</span></span>
* <span data-ttu-id="8d428-587">Stöd för att hämta förbrukning av enskild filresurs</span><span class="sxs-lookup"><span data-stu-id="8d428-587">Supported get single file share usage</span></span>
    - <span data-ttu-id="8d428-588">”Get-AzRmStorageShare”</span><span class="sxs-lookup"><span data-stu-id="8d428-588">'Get-AzRmStorageShare'</span></span>

## <a name="440---july-2020"></a><span data-ttu-id="8d428-589">4.4.0 – juli 2020</span><span class="sxs-lookup"><span data-stu-id="8d428-589">4.4.0 - July 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8d428-590">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8d428-590">Az.Accounts</span></span>
* <span data-ttu-id="8d428-591">En ny cmdlet, ”Invoke-AzRestMethod”, har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-591">Added new cmdlet 'Invoke-AzRestMethod'</span></span>
* <span data-ttu-id="8d428-592">Ett problem åtgärdades som kan orsaka autentiseringsfel i scenarier med fler processer, t.ex. när flera Azure PowerShell-cmdletar körs med ”Start-Job” [#9448]</span><span class="sxs-lookup"><span data-stu-id="8d428-592">Fixed an issue that may cause authentication errors in multi-process scenarios such as running multiple Azure PowerShell cmdlets using 'Start-Job' [#9448]</span></span>

#### <a name="azaks"></a><span data-ttu-id="8d428-593">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="8d428-593">Az.Aks</span></span>
* <span data-ttu-id="8d428-594">Felet som gjorde att ”Get-AzAks” inte hämtade alla kluster har åtgärdats [#12296]</span><span class="sxs-lookup"><span data-stu-id="8d428-594">Fixed bug 'Get-AzAks' doesn't get all clusters [#12296]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="8d428-595">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8d428-595">Az.AnalysisServices</span></span>
* <span data-ttu-id="8d428-596">Projektreferensen till autentisering har tagits bort</span><span class="sxs-lookup"><span data-stu-id="8d428-596">Removed project reference to Authentication</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8d428-597">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8d428-597">Az.Automation</span></span>
* <span data-ttu-id="8d428-598">Problemet som gjorde att strängar med escape-tecken inte kunde konverteras till JSON-objekt har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="8d428-598">Fixed the issue that string with escape chars cannot be converted into json object.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d428-599">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d428-599">Az.Compute</span></span>
* <span data-ttu-id="8d428-600">En varning har lats till som visas när ”New-AzVmss” används utan den senaste avbildningsversionen</span><span class="sxs-lookup"><span data-stu-id="8d428-600">Added warning when using 'New-AzVmss' without 'latest' image version</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8d428-601">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8d428-601">Az.DataFactory</span></span>
* <span data-ttu-id="8d428-602">Globala parametrar har lagts till för Data Factory.</span><span class="sxs-lookup"><span data-stu-id="8d428-602">Added global parameters to Data Factory.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="8d428-603">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="8d428-603">Az.EventGrid</span></span>
* <span data-ttu-id="8d428-604">Modulen har uppdaterats så att API-version 2020-06-01 används.</span><span class="sxs-lookup"><span data-stu-id="8d428-604">Updated to use the 2020-06-01 API version.</span></span>
* <span data-ttu-id="8d428-605">Nya funktioner har lagts till:</span><span class="sxs-lookup"><span data-stu-id="8d428-605">Added new features:</span></span>
    - <span data-ttu-id="8d428-606">Indatamappning</span><span class="sxs-lookup"><span data-stu-id="8d428-606">Input mapping</span></span>
    - <span data-ttu-id="8d428-607">Schema för händelseleverans</span><span class="sxs-lookup"><span data-stu-id="8d428-607">Event Delivery Schema</span></span>
    - <span data-ttu-id="8d428-608">Private Link</span><span class="sxs-lookup"><span data-stu-id="8d428-608">Private Link</span></span>
    - <span data-ttu-id="8d428-609">Cloud Event V10 Schema</span><span class="sxs-lookup"><span data-stu-id="8d428-609">Cloud Event V10 Schema</span></span>
    - <span data-ttu-id="8d428-610">Service Bus-ämne som mål</span><span class="sxs-lookup"><span data-stu-id="8d428-610">Service Bus Topic As Destination</span></span>
    - <span data-ttu-id="8d428-611">Azure-funktion som mål</span><span class="sxs-lookup"><span data-stu-id="8d428-611">Azure Function As Destination</span></span>
    - <span data-ttu-id="8d428-612">Webhook-batchbearbetning</span><span class="sxs-lookup"><span data-stu-id="8d428-612">WebHook Batching</span></span>
    - <span data-ttu-id="8d428-613">Säker webhook (AAD-stöd)</span><span class="sxs-lookup"><span data-stu-id="8d428-613">Secure webhook (AAD support)</span></span>
    - <span data-ttu-id="8d428-614">IpFiltering</span><span class="sxs-lookup"><span data-stu-id="8d428-614">IpFiltering</span></span>
* <span data-ttu-id="8d428-615">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="8d428-615">Updated cmdlets:</span></span>
    - <span data-ttu-id="8d428-616">”New-AzEventGridSubscription”/”Update-AzEventGridSubscription”:</span><span class="sxs-lookup"><span data-stu-id="8d428-616">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span></span>
        - <span data-ttu-id="8d428-617">Lägg till nya valfria parametrar för att ge stöd för webhook-batchbearbetning.</span><span class="sxs-lookup"><span data-stu-id="8d428-617">Add new optional parameters to support webhook batching.</span></span>
        - <span data-ttu-id="8d428-618">Lägg till nya valfria parametrar för att ge stöd för skyddad webhook med AAD.</span><span class="sxs-lookup"><span data-stu-id="8d428-618">Add new optional parameters to support secured webhook using AAD.</span></span>
        - <span data-ttu-id="8d428-619">Lägg till ny enum (uppräkning) för EndpointType-parametern för att ge stöd för Azure-funktion och Service Bus-ämne som nya mål.</span><span class="sxs-lookup"><span data-stu-id="8d428-619">Add new enum for EndpointType parameter to support azure function and service bus topic as new destinations.</span></span>
        - <span data-ttu-id="8d428-620">Lägg till ny valfri parameter för leveransschema.</span><span class="sxs-lookup"><span data-stu-id="8d428-620">Add new optional parameter for delivery schema.</span></span>
    - <span data-ttu-id="8d428-621">”New-AzEventGridTopic”/”Update-AzEventGridTopic” och ”New-AzEventGridDomain”/”Update-AzEventGridDomain”:</span><span class="sxs-lookup"><span data-stu-id="8d428-621">'New-AzEventGridTopic'/'Update-AzEventGridTopic' and 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span></span>
        - <span data-ttu-id="8d428-622">Lägg till nya valfria parametrar för att ge stöd för IpFiltering.</span><span class="sxs-lookup"><span data-stu-id="8d428-622">Add new optional parameters to support IpFiltering.</span></span>
    - <span data-ttu-id="8d428-623">”New-AzEventGridTopic”/”New-AzEventGridDomain”:</span><span class="sxs-lookup"><span data-stu-id="8d428-623">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span></span>
        - <span data-ttu-id="8d428-624">Lägg till nya valfria parametrar för att ge stöd för indatamappning.</span><span class="sxs-lookup"><span data-stu-id="8d428-624">Add new optional parameters to support Input mapping.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="8d428-625">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="8d428-625">Az.FrontDoor</span></span>
* <span data-ttu-id="8d428-626">Modulen har uppdaterats så att API 2020-05-01 används</span><span class="sxs-lookup"><span data-stu-id="8d428-626">Updated module to use API 2020-05-01</span></span>
* <span data-ttu-id="8d428-627">Stöd för privat länk har lagts till för Storage-, KeyVault- och Web App Service-resurser</span><span class="sxs-lookup"><span data-stu-id="8d428-627">Added Private link support for Storage, Keyvault and Web App Service resources</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="8d428-628">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8d428-628">Az.HDInsight</span></span>
* <span data-ttu-id="8d428-629">Stöd för att skapa kluster med ADLSGen1/2-lagring i nationella moln.</span><span class="sxs-lookup"><span data-stu-id="8d428-629">Supported creating cluster with ADLSGen1/2 storage in national clouds.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8d428-630">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8d428-630">Az.Monitor</span></span>
* <span data-ttu-id="8d428-631">Bugg som orsakade fel med ”Get-AzDiagnosticSetting” när mått eller loggar var null har åtgärdats [#12272]</span><span class="sxs-lookup"><span data-stu-id="8d428-631">Fixed bug for 'Get-AzDiagnosticSetting' when metrics or logs are null [#12272]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8d428-632">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d428-632">Az.Network</span></span>
* <span data-ttu-id="8d428-633">Parameterväxlingen i VWan HubVnet-anslutningar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8d428-633">Fixed parameters swap in VWan HubVnet connection</span></span>
* <span data-ttu-id="8d428-634">Nya cmdletar har lagts till för platser för virtuella installationer i Azure-nätverk</span><span class="sxs-lookup"><span data-stu-id="8d428-634">Added new cmdlets for Azure Network Virtual Appliance Sites</span></span>
    - <span data-ttu-id="8d428-635">”Get-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="8d428-635">'Get-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="8d428-636">”New-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="8d428-636">'New-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="8d428-637">”Remove-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="8d428-637">'Remove-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="8d428-638">”Update-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="8d428-638">'Update-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="8d428-639">”New-AzOffice365PolicyProperty”</span><span class="sxs-lookup"><span data-stu-id="8d428-639">'New-AzOffice365PolicyProperty'</span></span>
* <span data-ttu-id="8d428-640">Nya cmdletar har lagts till för virtuella installationer i Azure-nätverk</span><span class="sxs-lookup"><span data-stu-id="8d428-640">Added new cmdlets for Azure Network Virtual Appliance</span></span>
    - <span data-ttu-id="8d428-641">”Get-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="8d428-641">'Get-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="8d428-642">”New-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="8d428-642">'New-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="8d428-643">”Remove-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="8d428-643">'Remove-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="8d428-644">”Update-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="8d428-644">'Update-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="8d428-645">”Get-AzNetworkVirtualApplianceSku”</span><span class="sxs-lookup"><span data-stu-id="8d428-645">'Get-AzNetworkVirtualApplianceSku'</span></span>
    - <span data-ttu-id="8d428-646">”New-AzVirtualApplianceSkuProperty”</span><span class="sxs-lookup"><span data-stu-id="8d428-646">'New-AzVirtualApplianceSkuProperty'</span></span>
* <span data-ttu-id="8d428-647">Application Gateway har introducerats i vanliga cmdletar för Private Link</span><span class="sxs-lookup"><span data-stu-id="8d428-647">Onboarded Application Gateway to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="8d428-648">StorageSync har introducerats i vanliga cmdletar för Private Link</span><span class="sxs-lookup"><span data-stu-id="8d428-648">Onboarded StorageSync to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="8d428-649">SignalR har introducerats i vanliga cmdletar för Private Link</span><span class="sxs-lookup"><span data-stu-id="8d428-649">Onboarded SignalR to Private Link Common Cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8d428-650">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8d428-650">Az.RecoveryServices</span></span>
* <span data-ttu-id="8d428-651">Projektreferensen till autentisering har tagits bort</span><span class="sxs-lookup"><span data-stu-id="8d428-651">Removed project reference to Authentication</span></span>
* <span data-ttu-id="8d428-652">Azure Backup-anpassade cmdletar gör text mer korrekt.</span><span class="sxs-lookup"><span data-stu-id="8d428-652">Azure Backup tuned cmdlets help text to be more accurate.</span></span>
* <span data-ttu-id="8d428-653">Stöd har lagts till som gör att Azure Backup kan hämta MAB-agentjobb med cmdleten ”Get-AzRecoveryServicesBackupJob”.</span><span class="sxs-lookup"><span data-stu-id="8d428-653">Azure Backup added support for fetching MAB agent jobs using 'Get-AzRecoveryServicesBackupJob' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8d428-654">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d428-654">Az.Resources</span></span>
* <span data-ttu-id="8d428-655">”Save-AzResourceGroupDeploymentTemplate” har uppdaterats för att använda SDK:n.</span><span class="sxs-lookup"><span data-stu-id="8d428-655">Updated 'Save-AzResourceGroupDeploymentTemplate' to use the SDK.</span></span>
* <span data-ttu-id="8d428-656">Cmdleten ”Unregister-AzResourceProvider” har lagts till.</span><span class="sxs-lookup"><span data-stu-id="8d428-656">Added 'Unregister-AzResourceProvider' cmdlet.</span></span>

#### <a name="azsql"></a><span data-ttu-id="8d428-657">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d428-657">Az.Sql</span></span>
* <span data-ttu-id="8d428-658">Stöd har lagts till för SPN och gästanvändare i cmdleten ”Set-AzSqlInstanceActiveDirectoryAdministrator”</span><span class="sxs-lookup"><span data-stu-id="8d428-658">Added support for Service principal and guest users in Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet'</span></span>
* <span data-ttu-id="8d428-659">En bugg har åtgärdats i cmdletar för dataklassificering.</span><span class="sxs-lookup"><span data-stu-id="8d428-659">Fixed a bug in Data Classification cmdlets.'</span></span>
* <span data-ttu-id="8d428-660">Stöd har lagts till för redundansväxling med Azure SQL Managed Instance: ”Invoke-AzSqlInstanceFailover”</span><span class="sxs-lookup"><span data-stu-id="8d428-660">Added support for Azure SQL Managed Instance failover: 'Invoke-AzSqlInstanceFailover'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8d428-661">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8d428-661">Az.Storage</span></span>
* <span data-ttu-id="8d428-662">Problemet som gjorde att UserAgent inte lades till för vissa cmdletar för dataplanet har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="8d428-662">Fixed the issue that UserAgent is not added for some data plane cmdlets.</span></span>
* <span data-ttu-id="8d428-663">Stöd har lagts till för att skapa/uppdatera Storage-konto med MinimumTlsVersion och AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="8d428-663">Supported create/update Storage account with MinimumTlsVersion and AllowBlobPublicAccess</span></span>
    -  <span data-ttu-id="8d428-664">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="8d428-664">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="8d428-665">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="8d428-665">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="8d428-666">Stöd har lagts till för att aktivera/inaktivera versionshantering i Blob Service för ett Storage-konto</span><span class="sxs-lookup"><span data-stu-id="8d428-666">Support enable/disable versioning on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="8d428-667">”Update-AzStorageBlobServiceProperty”</span><span class="sxs-lookup"><span data-stu-id="8d428-667">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="8d428-668">Stöd har lagts till för att visa blobar med blobversioner</span><span class="sxs-lookup"><span data-stu-id="8d428-668">Support list blobs with blob versions</span></span>
    - <span data-ttu-id="8d428-669">”Get-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="8d428-669">'Get-AzStorageBlob'</span></span>
* <span data-ttu-id="8d428-670">Stöd har lagts till för att hämta/ta bort enskilda ögonblicksbilder av blobar eller blobversioner</span><span class="sxs-lookup"><span data-stu-id="8d428-670">Support get/remove single blob snapshot or blob version</span></span>
    - <span data-ttu-id="8d428-671">”Get-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="8d428-671">'Get-AzStorageBlob'</span></span>
    - <span data-ttu-id="8d428-672">”Remove-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="8d428-672">'Remove-AzStorageBlob'</span></span>
* <span data-ttu-id="8d428-673">Stöd har lagts till för pipelines från blobobjekt genererade av Azure.Storage.Blobs V12</span><span class="sxs-lookup"><span data-stu-id="8d428-673">Support pipeline from blob object generated from Azure.Storage.Blobs V12</span></span>
    - <span data-ttu-id="8d428-674">”Get-AzStorageBlobContent”</span><span class="sxs-lookup"><span data-stu-id="8d428-674">'Get-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="8d428-675">”New-AzStorageBlobSASToken”</span><span class="sxs-lookup"><span data-stu-id="8d428-675">'New-AzStorageBlobSASToken'</span></span>
    - <span data-ttu-id="8d428-676">”Remove-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="8d428-676">'Remove-AzStorageBlob'</span></span>
    - <span data-ttu-id="8d428-677">”Set-AzStorageBlobContent”</span><span class="sxs-lookup"><span data-stu-id="8d428-677">'Set-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="8d428-678">”Start-AzStorageBlobCopy”</span><span class="sxs-lookup"><span data-stu-id="8d428-678">'Start-AzStorageBlobCopy'</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="8d428-679">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="8d428-679">Az.StorageSync</span></span>
* <span data-ttu-id="8d428-680">En ny version har lagts till för StorageSync SDK som körs mot ApiVersion 2020-03-01</span><span class="sxs-lookup"><span data-stu-id="8d428-680">Added a new version StorageSync SDK targeting ApiVersion 2020-03-01</span></span>
* <span data-ttu-id="8d428-681">En cmdlet för synkroniseringstjänsten för lagringsuppdatering har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-681">Added Update Storage Sync Service cmdlet</span></span>
    - <span data-ttu-id="8d428-682">”Set-AzStorageSyncService”</span><span class="sxs-lookup"><span data-stu-id="8d428-682">'Set-AzStorageSyncService'</span></span>
* <span data-ttu-id="8d428-683">IncomingTrafficPolicy och PrivateEndpointConnections har lagts till för StorageSyncService-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="8d428-683">Added IncomingTrafficPolicy and PrivateEndpointConnections to StorageSyncService cmdlets.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8d428-684">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8d428-684">Az.Websites</span></span>
* <span data-ttu-id="8d428-685">Stöd har lagts till för att utföra åtgärder för platser som inte tillhör samma resursgrupp som App Services-planen</span><span class="sxs-lookup"><span data-stu-id="8d428-685">Added support to perform operations for Slots not in the same resource group as the App Service Plan</span></span>

## <a name="430---june-2020"></a><span data-ttu-id="8d428-686">4.3.0 – juni 2020</span><span class="sxs-lookup"><span data-stu-id="8d428-686">4.3.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8d428-687">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8d428-687">Az.Accounts</span></span>
* <span data-ttu-id="8d428-688">Stöd för identifiering av miljöinställning som standard och tillägg av miljön via ”Add-AzEnvironment”</span><span class="sxs-lookup"><span data-stu-id="8d428-688">Supported discovering environment setting by default and adding environment via 'Add-AzEnvironment'</span></span>
* <span data-ttu-id="8d428-689">Uppdatera förinlästa sammansättningar [#12024], [#11976]</span><span class="sxs-lookup"><span data-stu-id="8d428-689">Update preloaded assemblies [#12024], [#11976]</span></span>
* <span data-ttu-id="8d428-690">Uppdaterad Azure.Core-sammansättning</span><span class="sxs-lookup"><span data-stu-id="8d428-690">Updated Azure.Core assembly</span></span>
* <span data-ttu-id="8d428-691">Ett problem har åtgärdats som kan orsaka att ”Connect-AzAccount” misslyckas vid körning av flera trådar [#11201]</span><span class="sxs-lookup"><span data-stu-id="8d428-691">Fixed an issue that may cause 'Connect-AzAccount' to fail in multi-threaded execution [#11201]</span></span>

#### <a name="azaks"></a><span data-ttu-id="8d428-692">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="8d428-692">Az.Aks</span></span>
* <span data-ttu-id="8d428-693">Användning av gamla [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) ersattes med anrop till API:erna [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) och [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials)</span><span class="sxs-lookup"><span data-stu-id="8d428-693">Replaced usage of old [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) with calls to [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) and [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) APIs</span></span>

#### <a name="azbatch"></a><span data-ttu-id="8d428-694">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="8d428-694">Az.Batch</span></span>
* <span data-ttu-id="8d428-695">Az.Batch har uppdaterats att använda ”Microsoft.Azure.Management.Batch” SDK till och med version 11.0.0.</span><span class="sxs-lookup"><span data-stu-id="8d428-695">Updated Az.Batch to use 'Microsoft.Azure.Management.Batch' SDK version to 11.0.0</span></span>
* <span data-ttu-id="8d428-696">Möjligheten att ange BatchAccount-identiteten har lagts till i cmdleten ”New-AzBatchAccount”</span><span class="sxs-lookup"><span data-stu-id="8d428-696">Added the ability to set the BatchAccount Identity in the 'New-AzBatchAccount' cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="8d428-697">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8d428-697">Az.CognitiveServices</span></span>
* <span data-ttu-id="8d428-698">Stöd för att visa kontofunktioner.</span><span class="sxs-lookup"><span data-stu-id="8d428-698">Supported displaying account capabilities.</span></span>
* <span data-ttu-id="8d428-699">Stöd för att ändra PublicNetworkAccess.</span><span class="sxs-lookup"><span data-stu-id="8d428-699">Supported modifying PublicNetworkAccess.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d428-700">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d428-700">Az.Compute</span></span>
* <span data-ttu-id="8d428-701">Parametern SimulateEviction har lagts till i cmdletarna set-AzVM och set-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="8d428-701">Added SimulateEviction parameter to Set-AzVM and Set-AzVmssVM cmdlets.</span></span>
* <span data-ttu-id="8d428-702">”Premium_LRS” har lagts till i argumentslutföraren för parametern StorageAccountType för cmdleten New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="8d428-702">Added 'Premium_LRS' to the argument completer of StorageAccountType parameter for New-AzGalleryImageVersion cmdlet.</span></span>
* <span data-ttu-id="8d428-703">Understatusar har lagts till i VMCustomScriptExtension [#11297]</span><span class="sxs-lookup"><span data-stu-id="8d428-703">Added Substatuses to VMCustomScriptExtension [#11297]</span></span>
* <span data-ttu-id="8d428-704">”Delete” har lagts till i argumentslutföraren för parametern EvictionPolicy för cmdletarna New-AzVM och New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="8d428-704">Added 'Delete' to the argument completer of EvictionPolicy parameter for New-AzVM and New-AzVMConfig cmdlets.</span></span>
* <span data-ttu-id="8d428-705">Åtgärdat namn för nytt VM-tillägg för SAP</span><span class="sxs-lookup"><span data-stu-id="8d428-705">Fixed name of new VM Extension for SAP</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8d428-706">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8d428-706">Az.DataFactory</span></span>
* <span data-ttu-id="8d428-707">ADF .Net SDK har uppdaterats till 4.9.0</span><span class="sxs-lookup"><span data-stu-id="8d428-707">Updated ADF .Net SDK version to 4.9.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="8d428-708">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8d428-708">Az.EventHub</span></span>
* <span data-ttu-id="8d428-709">Parametrar för hanterad identitet har lagts till i cmdletarna ”New-AzEventHubNamespace” och ”set-AzEventHubNamespace”</span><span class="sxs-lookup"><span data-stu-id="8d428-709">Added Managed Identity parameters to 'New-AzEventHubNamespace' and 'Set-AzEventHubNamespace' cmdlets</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="8d428-710">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="8d428-710">Az.Functions</span></span>
* <span data-ttu-id="8d428-711">Stöd har lagts till för att skapa PowerShell 7.0- och Java 11-funktionsappar</span><span class="sxs-lookup"><span data-stu-id="8d428-711">Added support to create PowerShell 7.0 and Java 11 function apps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="8d428-712">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8d428-712">Az.HDInsight</span></span>
* <span data-ttu-id="8d428-713">Stöd för listning av värdar och omstart för specifika värdar i HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="8d428-713">Supported listing hosts and restart specific hosts of the HDInsight cluster.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="8d428-714">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="8d428-714">Az.HealthcareApis</span></span>
* <span data-ttu-id="8d428-715">Uppdaterade SDK-versionen till 1.1.0</span><span class="sxs-lookup"><span data-stu-id="8d428-715">Updated the SDK version to 1.1.0</span></span>
* <span data-ttu-id="8d428-716">Stöd har lagts till för exportinställningar och hanterad identitet</span><span class="sxs-lookup"><span data-stu-id="8d428-716">Added support for Export settings and Managed Identity</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8d428-717">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8d428-717">Az.Monitor</span></span>
* <span data-ttu-id="8d428-718">Parameter för inmatningsobjekt har åtgärdats för ”Set-AzActivityLogAlert”</span><span class="sxs-lookup"><span data-stu-id="8d428-718">Fixed input object parameter for 'Set-AzActivityLogAlert'</span></span>
* <span data-ttu-id="8d428-719">Parametern ”InputObject” har åtgärdats för ”Set-AzActionGroup” [#10868]</span><span class="sxs-lookup"><span data-stu-id="8d428-719">Fixed 'InputObject' parameter for 'Set-AzActionGroup' [#10868]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8d428-720">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d428-720">Az.Network</span></span>
* <span data-ttu-id="8d428-721">Stöd har lagts till för parametern AddressPrefixType i ”Remove-AzExpressRouteCircuitConnectionConfig”</span><span class="sxs-lookup"><span data-stu-id="8d428-721">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="8d428-722">Nya cmdletar har lagts till för Azure FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="8d428-722">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="8d428-723">”New-AzFirewallPolicyDnsSetting”</span><span class="sxs-lookup"><span data-stu-id="8d428-723">'New-AzFirewallPolicyDnsSetting'</span></span>
    - <span data-ttu-id="8d428-724">Stöd för mål-FQDN i nätverksregler för brandväggsprincip</span><span class="sxs-lookup"><span data-stu-id="8d428-724">Support for Destination FQDN in Network Rules for Firewall Policy</span></span>
* <span data-ttu-id="8d428-725">Stöd har lagts till för åtgärder i serverdelsadresspooler</span><span class="sxs-lookup"><span data-stu-id="8d428-725">Added support for backend address pool operations</span></span>
    - <span data-ttu-id="8d428-726">”New-AzLoadBalancerBackendAddressConfig”</span><span class="sxs-lookup"><span data-stu-id="8d428-726">'New-AzLoadBalancerBackendAddressConfig'</span></span>
    - <span data-ttu-id="8d428-727">”New-AzLoadBalancerBackendAddressPool”</span><span class="sxs-lookup"><span data-stu-id="8d428-727">'New-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="8d428-728">”Set-AzLoadBalancerBackendAddressPool”</span><span class="sxs-lookup"><span data-stu-id="8d428-728">'Set-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="8d428-729">”Remove-AzLoadBalancerBackendAddressPool”</span><span class="sxs-lookup"><span data-stu-id="8d428-729">'Remove-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="8d428-730">”Get-AzLoadBalancerBackendAddressPool”</span><span class="sxs-lookup"><span data-stu-id="8d428-730">'Get-AzLoadBalancerBackendAddressPool'</span></span>
* <span data-ttu-id="8d428-731">Namnvalidering har lagts till för ”New-AzIpGroup”</span><span class="sxs-lookup"><span data-stu-id="8d428-731">Added name validation for 'New-AzIpGroup'</span></span>
* <span data-ttu-id="8d428-732">Nya cmdletar har lagts till för Azure FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="8d428-732">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="8d428-733">”New-AzFirewallPolicyThreatIntelWhitelist”</span><span class="sxs-lookup"><span data-stu-id="8d428-733">'New-AzFirewallPolicyThreatIntelWhitelist'</span></span>
* <span data-ttu-id="8d428-734">Nedanstående kommandon för funktionen har uppdaterats: Konfiguration/borttagning av anpassade DNS-servrar på VirtualWan P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="8d428-734">Updated below commands for feature: Custom dns servers set/remove on VirtualWan P2SVpnGateway.</span></span>
    - <span data-ttu-id="8d428-735">New-AzP2sVpnGateway har uppdaterats: Den valfria parametern ”-CustomDnsServer” har lagts till för att kunder ska kunna ange att deras DNS-servrar ska konfigureras på P2SVpnGateway, som kan användas av punkt-till-plats-klienter.</span><span class="sxs-lookup"><span data-stu-id="8d428-735">Updated New-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
    - <span data-ttu-id="8d428-736">Update-AzP2sVpnGateway har uppdaterats: Den valfria parametern ”-CustomDnsServer” har lagts till för att kunder ska kunna ange att deras DNS-servrar ska konfigureras på P2SVpnGateway, som kan användas av punkt-till-plats-klienter.</span><span class="sxs-lookup"><span data-stu-id="8d428-736">Updated Update-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
* <span data-ttu-id="8d428-737">”Update-AzVpnGateway” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="8d428-737">Updated 'Update-AzVpnGateway'</span></span>
    - <span data-ttu-id="8d428-738">Den valfria parametern ”-BgpPeeringAddress” har lagts till för att kunder ska kunna ange sina anpassade BGP:er som ska konfigurerar på VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="8d428-738">Added optional parameter '-BgpPeeringAddress' for customers to specify their custom bgps to set on VpnGateway.</span></span>
* <span data-ttu-id="8d428-739">Ny cmdlet har lagts till för att stödja återställning av en VirtualHub-resurs routningsstatus:</span><span class="sxs-lookup"><span data-stu-id="8d428-739">Added new cmdlet to support resetting the routing state of a VirtualHub resource:</span></span>
    - <span data-ttu-id="8d428-740">”Reset-AzHubRouter”</span><span class="sxs-lookup"><span data-stu-id="8d428-740">'Reset-AzHubRouter'</span></span>
* <span data-ttu-id="8d428-741">Nedanstående saker har uppdaterats baserat på den senaste Swagger-ändringen för brandväggspolicyn</span><span class="sxs-lookup"><span data-stu-id="8d428-741">Updated below things based on recent swagger change for Firewall Policy</span></span>
    - <span data-ttu-id="8d428-742">Namn ändras för RuleGroup, RuleCollectionGroup och RuleType</span><span class="sxs-lookup"><span data-stu-id="8d428-742">Changes names for RuleGroup, RuleCollectionGroup and RuleType</span></span>
    - <span data-ttu-id="8d428-743">Stöd har lagts till för NAT-regelsamlingar för brandväggsprincip så att flera NAT-regelsamlingar stöds</span><span class="sxs-lookup"><span data-stu-id="8d428-743">Added support for Firewall Policy NAT Rule Collections to support multiple NAT Rule Collection</span></span>
* <span data-ttu-id="8d428-744">[Icke-bakåtkompatibel ändring] Den obligatoriska parametern ”SourceIpGroup” har lagts till för ”New-AzFirewallPolicyApplicationRule” och ”New-AzFirewallPolicyNetworkRule”.</span><span class="sxs-lookup"><span data-stu-id="8d428-744">[Breaking Change] Added mandatory parameter 'SourceIpGroup' for 'New-AzFirewallPolicyApplicationRule' and 'New-AzFirewallPolicyNetworkRule'.</span></span>
* <span data-ttu-id="8d428-745">[Icke-bakåtkompatibel ändring] ”New-AzFirewallPolicyApplicationRule” har åtgärdats, parametern ”SourceAddress” är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="8d428-745">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="8d428-746">[Icke-bakåtkompatibel ändring] ”New-AzFirewallPolicyApplicationRule” har åtgärdats, parametern ”SourceAddress” är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="8d428-746">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="8d428-747">[Icke-bakåtkompatibel ändring] Obligatoriska parametrar har tagits bort: ”TranslatedAddress”, ”TranslatedPort” för ”New-AzFirewallPolicyNatRuleCollection”.</span><span class="sxs-lookup"><span data-stu-id="8d428-747">[Breaking Change] Removed mandatory parameters: 'TranslatedAddress', 'TranslatedPort' for 'New-AzFirewallPolicyNatRuleCollection'.</span></span>
* <span data-ttu-id="8d428-748">Nya cmdletar har lagts till för att stödja PrivateLink på Application Gateway</span><span class="sxs-lookup"><span data-stu-id="8d428-748">Added new cmdlets to support PrivateLink On Application Gateway</span></span>
    - <span data-ttu-id="8d428-749">”New-AzApplicationGatewayPrivateLinkConfiguration”</span><span class="sxs-lookup"><span data-stu-id="8d428-749">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="8d428-750">”Get-AzApplicationGatewayPrivateLinkConfiguration”</span><span class="sxs-lookup"><span data-stu-id="8d428-750">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="8d428-751">”New-AzApplicationGatewayPrivateLinkConfiguration”</span><span class="sxs-lookup"><span data-stu-id="8d428-751">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="8d428-752">”Set-AzApplicationGatewayPrivateLinkConfiguration”</span><span class="sxs-lookup"><span data-stu-id="8d428-752">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="8d428-753">”Remove-AzApplicationGatewayPrivateLinkConfiguration”</span><span class="sxs-lookup"><span data-stu-id="8d428-753">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="8d428-754">”New-AzApplicationGatewayPrivateLinkIpConfiguration”</span><span class="sxs-lookup"><span data-stu-id="8d428-754">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span></span>
* <span data-ttu-id="8d428-755">Nya cmdletar har lagts till för VirtualHubs underordnade resurs HubRouteTables.</span><span class="sxs-lookup"><span data-stu-id="8d428-755">Added new cmdlets for HubRouteTables child resource of VirtualHub.</span></span>
    - <span data-ttu-id="8d428-756">”New-AzVHubRoute”</span><span class="sxs-lookup"><span data-stu-id="8d428-756">'New-AzVHubRoute'</span></span>
    - <span data-ttu-id="8d428-757">”New-AzVHubRouteTable”</span><span class="sxs-lookup"><span data-stu-id="8d428-757">'New-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="8d428-758">”Get-AzVHubRouteTable”</span><span class="sxs-lookup"><span data-stu-id="8d428-758">'Get-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="8d428-759">”Update-AzVHubRouteTable”</span><span class="sxs-lookup"><span data-stu-id="8d428-759">'Update-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="8d428-760">”Remove-AzVHubRouteTable”</span><span class="sxs-lookup"><span data-stu-id="8d428-760">'Remove-AzVHubRouteTable'</span></span>
* <span data-ttu-id="8d428-761">Befintliga cmdletar har uppdaterats för att stödja valfri RoutingConfiguration-indataparameter för anpassad routning i VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="8d428-761">Updated existing cmdlets to support optional RoutingConfiguration input parameter for custom routing in VirtualWan.</span></span>
    - <span data-ttu-id="8d428-762">”New-AzExpressRouteConnection”</span><span class="sxs-lookup"><span data-stu-id="8d428-762">'New-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="8d428-763">”Set-AzExpressRouteConnection”</span><span class="sxs-lookup"><span data-stu-id="8d428-763">'Set-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="8d428-764">”New-AzVirtualHubVnetConnection”</span><span class="sxs-lookup"><span data-stu-id="8d428-764">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="8d428-765">”Update-AzVirtualHubVnetConnection”</span><span class="sxs-lookup"><span data-stu-id="8d428-765">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="8d428-766">”New-AzVpnConnection”</span><span class="sxs-lookup"><span data-stu-id="8d428-766">'New-AzVpnConnection'</span></span>
    - <span data-ttu-id="8d428-767">”Update-AzVpnConnection”</span><span class="sxs-lookup"><span data-stu-id="8d428-767">'Update-AzVpnConnection'</span></span>
    - <span data-ttu-id="8d428-768">”New-AzP2sVpnGateway”</span><span class="sxs-lookup"><span data-stu-id="8d428-768">'New-AzP2sVpnGateway'</span></span>
    - <span data-ttu-id="8d428-769">”Update-AzP2sVpnGateway”</span><span class="sxs-lookup"><span data-stu-id="8d428-769">'Update-AzP2sVpnGateway'</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8d428-770">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8d428-770">Az.OperationalInsights</span></span>
* <span data-ttu-id="8d428-771">Fast fel PSWorkspace implementerar inte IOperationalInsightsWorkspace [#12135]</span><span class="sxs-lookup"><span data-stu-id="8d428-771">Fixed bug PSWorkspace doesn't implement IOperationalInsightsWorkspace [#12135]</span></span>
* <span data-ttu-id="8d428-772">”pergb2018” har lagts till i uppsättningen med giltiga värden för parametern ”Sku” i ”Set-AzOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="8d428-772">Added 'pergb2018' to valid value set of parameter 'Sku' in 'Set-AzOperationalInsightsWorkspace'</span></span> 
* <span data-ttu-id="8d428-773">Alias ”FunctionParameters” lades till för parametern ”FunctionParameter” till</span><span class="sxs-lookup"><span data-stu-id="8d428-773">Added alias 'FunctionParameters' for parameter 'FunctionParameter' to</span></span>
    - <span data-ttu-id="8d428-774">”New-AzOperationalInsightsSavedSearch”</span><span class="sxs-lookup"><span data-stu-id="8d428-774">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="8d428-775">”Set-AzOperationalInsightsSavedSearch”</span><span class="sxs-lookup"><span data-stu-id="8d428-775">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8d428-776">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8d428-776">Az.RecoveryServices</span></span>
* <span data-ttu-id="8d428-777">Azure Backup har fått stöd för att hämta MAB-objekt.</span><span class="sxs-lookup"><span data-stu-id="8d428-777">Azure Backup added support for fetching MAB items.</span></span>
* <span data-ttu-id="8d428-778">Azure Site Recovery stöder disktypen ”StandardSSD_LRS”</span><span class="sxs-lookup"><span data-stu-id="8d428-778">Azure Site Recovery supports disk type 'StandardSSD_LRS'</span></span>

#### <a name="azresources"></a><span data-ttu-id="8d428-779">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d428-779">Az.Resources</span></span>
* <span data-ttu-id="8d428-780">”UsageLocation”, ”GivenName”, ”Surname”, ”AccountEnabled”, ”MailNickname”, ”Mail” på ”PSADUser” lades till [#10526] [#10497]</span><span class="sxs-lookup"><span data-stu-id="8d428-780">Added 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' on 'PSADUser' [#10526] [#10497]</span></span>
* <span data-ttu-id="8d428-781">Problem med att ”-Mail” inte fungerar på ”Get-AzADUser” har åtgärdats [#11981]</span><span class="sxs-lookup"><span data-stu-id="8d428-781">Fixed issue that '-Mail' doesn't work on 'Get-AzADUser' [#11981]</span></span>
* <span data-ttu-id="8d428-782">Parametern ”-ExcludeChangeType” har lagts till i ”Get-AzDeploymentWhatIfResult” och ”Get-AzResourceGroupDeploymentWhatIfResult”</span><span class="sxs-lookup"><span data-stu-id="8d428-782">Added '-ExcludeChangeType' parameter to 'Get-AzDeploymentWhatIfResult' and 'Get-AzResourceGroupDeploymentWhatIfResult'</span></span>
* <span data-ttu-id="8d428-783">Parametern ”-WhatIfExcludeChangeType” har lagts till i ”New-AzDeployment” och ”New-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="8d428-783">Added '-WhatIfExcludeChangeType' parameter to 'New-AzDeployment' and 'New-AzResourceGroupDeployment'</span></span>
* <span data-ttu-id="8d428-784">Cmdletar för ”Test-Az\*Deployment” har uppdaterats för att visa bättre felmeddelanden</span><span class="sxs-lookup"><span data-stu-id="8d428-784">Updated 'Test-Az\*Deployment' cmdlets to show better error messages</span></span>
* <span data-ttu-id="8d428-785">Hjälpmeddelandet för parametern ”-Name” i distributionsskapande och What If-cmdletar</span><span class="sxs-lookup"><span data-stu-id="8d428-785">Fixed help message for '-Name' parameter of deployment create and What-If cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="8d428-786">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d428-786">Az.Sql</span></span>
* <span data-ttu-id="8d428-787">Stöd för tjänsthuvudnamn har lagts till för administratörs-cmdlet för SQL Server Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="8d428-787">Added support for service principal for Set SQL Server Azure Active Directory Admin cmdlet</span></span>
* <span data-ttu-id="8d428-788">Synkroniseringsproblem i Data Classification-cmdletar har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="8d428-788">Fixed sync issue in Data Classification cmdlets.</span></span>
* <span data-ttu-id="8d428-789">Stöd för att söka efter användare via e-postadress på ”Set-AzSqlServerActiveDirectoryAdministrator” [#12192]</span><span class="sxs-lookup"><span data-stu-id="8d428-789">Supported searching user by mail on 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8d428-790">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8d428-790">Az.Storage</span></span>
* <span data-ttu-id="8d428-791">Skapa lagringskonto med RequireInfrastructureEncryption stöds</span><span class="sxs-lookup"><span data-stu-id="8d428-791">Supported create Storage account with RequireInfrastructureEncryption</span></span>
    -  <span data-ttu-id="8d428-792">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="8d428-792">'New-AzStorageAccount'</span></span>
* <span data-ttu-id="8d428-793">Logiken för inläsning av Azure.Core flyttades till Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8d428-793">Moved the logic of loading Azure.Core to Az.Accounts</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8d428-794">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8d428-794">Az.Websites</span></span>
* <span data-ttu-id="8d428-795">Skydd för att ta bort skapad webapp om återställningen misslyckades har lagts till i ”Restore-AzDeletedWebApp”</span><span class="sxs-lookup"><span data-stu-id="8d428-795">Added safeguard to delete created webapp if restore failed in 'Restore-AzDeletedWebApp'</span></span>
* <span data-ttu-id="8d428-796">”SourceWebApp.Location” har lagts till för ”New-AzWebApp” och ”New-AzWebAppSlot”</span><span class="sxs-lookup"><span data-stu-id="8d428-796">Added 'SourceWebApp.Location' for 'New-AzWebApp' and 'New-AzWebAppSlot'</span></span>
* <span data-ttu-id="8d428-797">Fel som förhindrade ändring av containerinställningar i ”Set-AzWebApp” och ”Set-AzWebAppSlot” har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8d428-797">Fixed bug that prevented changing Container settings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>
* <span data-ttu-id="8d428-798">Ett fel för att hämta SiteConfig när -Name inte anges för Get-AzWebApp har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8d428-798">Fixed bug to get SiteConfig when -Name is not given for Get-AzWebApp</span></span>
* <span data-ttu-id="8d428-799">Stöd har lagts till för att skapa ASP för Linux-appar</span><span class="sxs-lookup"><span data-stu-id="8d428-799">Added a support to create ASP for Linux Apps</span></span>
* <span data-ttu-id="8d428-800">Undantag har lagts till för kloning över resursgrupper</span><span class="sxs-lookup"><span data-stu-id="8d428-800">Added exceptions for clone across resource groups</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="8d428-801">4.2.0 – juni 2020</span><span class="sxs-lookup"><span data-stu-id="8d428-801">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8d428-802">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8d428-802">Az.Accounts</span></span>
* <span data-ttu-id="8d428-803">Åtgärdade ett problem som kan få Az att hoppa över loggar i Azure Automation- eller PowerShell-jobb [#11492]</span><span class="sxs-lookup"><span data-stu-id="8d428-803">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="8d428-804">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8d428-804">Az.AnalysisServices</span></span>
* <span data-ttu-id="8d428-805">Uppdaterad sammansättningsversion för dataplan-cmdletar</span><span class="sxs-lookup"><span data-stu-id="8d428-805">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="8d428-806">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8d428-806">Az.ApiManagement</span></span>
* <span data-ttu-id="8d428-807">Uppdaterad sammansättningsversion för cmdletar för tjänsthantering</span><span class="sxs-lookup"><span data-stu-id="8d428-807">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="8d428-808">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="8d428-808">Az.Billing</span></span>
* <span data-ttu-id="8d428-809">Uppdaterad sammansättningsversion för förbrukningscmdletar</span><span class="sxs-lookup"><span data-stu-id="8d428-809">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="8d428-810">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8d428-810">Az.CognitiveServices</span></span>
* <span data-ttu-id="8d428-811">Stöd för PrivateEndpoint- och PublicNetworkAccess-kontroll.</span><span class="sxs-lookup"><span data-stu-id="8d428-811">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="8d428-812">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8d428-812">Az.DataFactory</span></span>
* <span data-ttu-id="8d428-813">Uppdaterad sammansättningsversion för datafabrik V2-cmdletar</span><span class="sxs-lookup"><span data-stu-id="8d428-813">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="8d428-814">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="8d428-814">Az.DataShare</span></span>
* <span data-ttu-id="8d428-815">Allmän tillgänglighet för modulen ”Az.DataShare”</span><span class="sxs-lookup"><span data-stu-id="8d428-815">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="8d428-816">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="8d428-816">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="8d428-817">Allmän tillgänglighet för modulen ”Az.DesktopVirtualization”</span><span class="sxs-lookup"><span data-stu-id="8d428-817">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8d428-818">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8d428-818">Az.OperationalInsights</span></span>
* <span data-ttu-id="8d428-819">Uppgraderad SDK till 0.21.0</span><span class="sxs-lookup"><span data-stu-id="8d428-819">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="8d428-820">Lade till valfria parametrar till</span><span class="sxs-lookup"><span data-stu-id="8d428-820">Added optional parameters to</span></span> 
    - <span data-ttu-id="8d428-821">”New-AzOperationalInsightsSavedSearch”</span><span class="sxs-lookup"><span data-stu-id="8d428-821">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="8d428-822">”Set-AzOperationalInsightsSavedSearch”</span><span class="sxs-lookup"><span data-stu-id="8d428-822">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="8d428-823">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="8d428-823">Az.PolicyInsights</span></span>
* <span data-ttu-id="8d428-824">Korrigerade exempel 3 för ”Start-AzPolicyComplianceScan”</span><span class="sxs-lookup"><span data-stu-id="8d428-824">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="8d428-825">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="8d428-825">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="8d428-826">Uppdaterad sammansättningsversion för PowerBI-cmdletar</span><span class="sxs-lookup"><span data-stu-id="8d428-826">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="8d428-827">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="8d428-827">Az.PrivateDns</span></span>
* <span data-ttu-id="8d428-828">Korrigerade formatering av utförlig utdatasträng för Remove-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="8d428-828">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8d428-829">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8d428-829">Az.RecoveryServices</span></span>
* <span data-ttu-id="8d428-830">Azure Site Recovery-stöd för att skapa en återställningsplan för replikering mellan zoner från xml-indata.</span><span class="sxs-lookup"><span data-stu-id="8d428-830">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="8d428-831">Uppdaterad sammansättningsversion för cmdletar för SiteRecovery och Backup</span><span class="sxs-lookup"><span data-stu-id="8d428-831">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="8d428-832">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d428-832">Az.Resources</span></span>
* <span data-ttu-id="8d428-833">Lade till slutparameter för cmdletarna Get-AzDeploymentScriptLog och Save-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="8d428-833">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="8d428-834">Formaterad utdataegenskap så att den kan visas i cmdlet-utdata för Get-AzDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="8d428-834">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="8d428-835">Bytte namn på parametern -DeploymentScriptInputObject till -DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="8d428-835">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="8d428-836">Åtgärdade saknade fil/målnamn i cmdlet-meddelanden.</span><span class="sxs-lookup"><span data-stu-id="8d428-836">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="8d428-837">Uppdaterad sammansättningsversion för cmdletar för resurshanterare och taggar</span><span class="sxs-lookup"><span data-stu-id="8d428-837">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="8d428-838">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d428-838">Az.Sql</span></span>
* <span data-ttu-id="8d428-839">Lade till UsePrivateLinkConnection till ”New-AzSqlSyncGroup”, ”Update-AzSqlSyncGroup”, ”New-AzSqlSyncMember” och ”Update-AzSqlSyncMember”</span><span class="sxs-lookup"><span data-stu-id="8d428-839">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="8d428-840">Lade till SyncMemberAzureDatabaseResourceId till ”New-AzSqlSyncMember” and ”Update-AzSqlSyncMember”</span><span class="sxs-lookup"><span data-stu-id="8d428-840">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="8d428-841">Lade till stöd för att söka efter gästanvändare för att ange administratörs-cmdlet för SQL Server Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="8d428-841">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8d428-842">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8d428-842">Az.Storage</span></span>
* <span data-ttu-id="8d428-843">Uppdaterad sammansättningsversion för dataplan-cmdletar</span><span class="sxs-lookup"><span data-stu-id="8d428-843">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="8d428-844">4.1.0 – maj 2020</span><span class="sxs-lookup"><span data-stu-id="8d428-844">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="8d428-845">Höjdpunkter sedan den senaste uppdateringen</span><span class="sxs-lookup"><span data-stu-id="8d428-845">Highlights since the last release</span></span>
* <span data-ttu-id="8d428-846">PowerShell-versioner som stöds: Windows PowerShell 5.1, PowerShell Core 6.2.4+ och PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="8d428-846">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="8d428-847">Allmän tillgänglighet för Az.Functions</span><span class="sxs-lookup"><span data-stu-id="8d428-847">General availability of Az.Functions</span></span> 
* <span data-ttu-id="8d428-848">Nya stora uppdateringar har gjorts för Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources och Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8d428-848">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="8d428-849">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8d428-849">Az.Accounts</span></span>
* <span data-ttu-id="8d428-850">”Add-AzEnvironment” och ”Set-AzEnvironment” har uppdaterats med stöd för parametrarna ”AzureSynapseAnalyticsEndpointResourceId” och ”AzureSynapseAnalyticsEndpointSuffix”</span><span class="sxs-lookup"><span data-stu-id="8d428-850">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="8d428-851">Azure.Core-relaterade sammansättningar har lagts till i Az.Accounts; PowerShell-plattformar som stöds är Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span><span class="sxs-lookup"><span data-stu-id="8d428-851">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="8d428-852">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="8d428-852">Az.Aks</span></span>
* <span data-ttu-id="8d428-853">API-versionen har uppgraderats till 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="8d428-853">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="8d428-854">Stöds för att skapa AKS med hjälp av Windows-container</span><span class="sxs-lookup"><span data-stu-id="8d428-854">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="8d428-855">Nya cmdletar är tillgängliga: ”New-AzAksNodePool”, ”Update-AzAksNodePool”, ”Remove-AzAksNodePool”,        ”Get-AzAksNodePool”, ”Install-AzAksKubectl”, ”Get-AzAksVersion”</span><span class="sxs-lookup"><span data-stu-id="8d428-855">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="8d428-856">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8d428-856">Az.ApiManagement</span></span>
* <span data-ttu-id="8d428-857">Parametrarna ”New-AzApiManagement” och ”Set-AzApiManagement”: [-AssignIdentity] har bytt namn till [-SystemAssignedIdentity]</span><span class="sxs-lookup"><span data-stu-id="8d428-857">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="8d428-858">”New-AzApiManagement” och ”Set-AzApiManagement”: En ny parameter har lagts till: [-UserAssignedIdentity <String[]>]</span><span class="sxs-lookup"><span data-stu-id="8d428-858">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="8d428-859">”Get-AzApiManagementProperty” har bytt namn till ”Get-AzApiManagementNamedValue”.</span><span class="sxs-lookup"><span data-stu-id="8d428-859">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="8d428-860">PropertyId-parametern har bytt namn till NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="8d428-860">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="8d428-861">”New-AzApiManagementProperty” har bytt namn till ”New-AzApiManagementNamedValue”.</span><span class="sxs-lookup"><span data-stu-id="8d428-861">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="8d428-862">PropertyId-parametern har bytt namn till NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="8d428-862">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="8d428-863">”Set-AzApiManagementProperty” har bytt namn till ”Set-AzApiManagementNamedValue”.</span><span class="sxs-lookup"><span data-stu-id="8d428-863">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="8d428-864">PropertyId-parametern har bytt namn till NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="8d428-864">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="8d428-865">”Remove-AzApiManagementProperty” har bytt namn till ”Remove-AzApiManagementNamedValue”.</span><span class="sxs-lookup"><span data-stu-id="8d428-865">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="8d428-866">PropertyId-parametern har bytt namn till NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="8d428-866">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="8d428-867">Den nya cmdleten Get-AzApiManagementAuthorizationServerClientSecret gör att ”Get-AzApiManagementAuthorizationServer” inte längre returnerar klienthemligheter.</span><span class="sxs-lookup"><span data-stu-id="8d428-867">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="8d428-868">Den nya cmdleten ”Get-AzApiManagementNamedValueSecretValue” gör att ”Get-AzApiManagementNamedValue” inte returnerar värdet för en hemlighet.</span><span class="sxs-lookup"><span data-stu-id="8d428-868">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="8d428-869">Den nya cmdleten ”Get-AzApiManagementOpenIdConnectProviderClientSecret” gör att ”Get-AzApiManagementOpenIdConnectProvider” inte längre returnerar klienthemligheter.</span><span class="sxs-lookup"><span data-stu-id="8d428-869">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="8d428-870">Den nya cmdleten ”Get-AzApiManagementSubscriptionKey” gör att ”Get-AzApiManagementSubscription” inte längre returnerar prenumerationsnycklar.</span><span class="sxs-lookup"><span data-stu-id="8d428-870">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="8d428-871">Den nya cmdleten ”Get-AzApiManagementTenantAccessSecret” gör att ”Get-AzApiManagementTenantAccess” inte längre returnerar nycklar.</span><span class="sxs-lookup"><span data-stu-id="8d428-871">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="8d428-872">Den nya cmdleten ”Get-AzApiManagementTenantGitAccessSecret” gör att ”Get-AzApiManagementTenantGitAccess” inte längre returnerar nycklar.</span><span class="sxs-lookup"><span data-stu-id="8d428-872">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="8d428-873">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="8d428-873">Az.ApplicationInsights</span></span>
* <span data-ttu-id="8d428-874">Tillagda parametrar: ”RetentionInDays” ”PublicNetworkAccessForIngestion” ”PublicNetworkAccessForQuery” för ”New-AzApplicationInsights”</span><span class="sxs-lookup"><span data-stu-id="8d428-874">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="8d428-875">Cmdleten ”Update-AzApplicationInsights” har skapats</span><span class="sxs-lookup"><span data-stu-id="8d428-875">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="8d428-876">Cmdletar har skapats för länkat lagringskonto</span><span class="sxs-lookup"><span data-stu-id="8d428-876">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="8d428-877">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="8d428-877">Az.Batch</span></span>
* <span data-ttu-id="8d428-878">Az.Batch har uppdaterats att använda ”Microsoft.Azure.Batch” SDK version 13.0.0 och ”Microsoft.Azure.Management.Batch” SDK version 9.0.0.</span><span class="sxs-lookup"><span data-stu-id="8d428-878">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="8d428-879">Nu kan du välja vilken typ av certifikat du lägger till genom att använda den nya parametern ”-CertificateKind” med ”New-AzBatchCertificate”.</span><span class="sxs-lookup"><span data-stu-id="8d428-879">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="8d428-880">Egenskapen ”ApplicationPackages” har tagits bort från ”PSApplication”, som tidigare alltid var ''.</span><span class="sxs-lookup"><span data-stu-id="8d428-880">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="8d428-881">Specifika paket i ett program kan nu hämtas med hjälp av ”Get-AzBatchApplicationPackage”.</span><span class="sxs-lookup"><span data-stu-id="8d428-881">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="8d428-882">Ett exempel: ”Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication”.</span><span class="sxs-lookup"><span data-stu-id="8d428-882">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="8d428-883">Nu när du skapar en pool med hjälp av ”New-AzBatchPool” kan egenskapen ”VirtualMachineImageId” för ”PSImageReference” endast referera till en Shared Image Gallery-avbildning.</span><span class="sxs-lookup"><span data-stu-id="8d428-883">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="8d428-884">När du skapar en pool med hjälp av ”New-AzBatchPool” kan poolen etableras utan en offentlig IP-adress med hjälp av den nya egenskapen ”PublicIPAddressConfiguration” för ”PSNetworkConfiguration”.</span><span class="sxs-lookup"><span data-stu-id="8d428-884">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="8d428-885">Egenskapen ”PublicIPs” för ”PSNetworkConfiguration” har också flyttats till ”PSPublicIPAddressConfiguration”.</span><span class="sxs-lookup"><span data-stu-id="8d428-885">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="8d428-886">Den här egenskapen kan bara anges om ”IPAddressProvisioningType” är ”UserManaged”.</span><span class="sxs-lookup"><span data-stu-id="8d428-886">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d428-887">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d428-887">Az.Compute</span></span>
* <span data-ttu-id="8d428-888">Parametern HostId har lagts till för cmdleten ”Update-AzVM”t</span><span class="sxs-lookup"><span data-stu-id="8d428-888">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="8d428-889">Hjälpdokumenten har uppdaterats för cmdletarna ”New-AzVMConfig”, ”New-AzVmssConfig”, ”Update-AzVmss”, ”Set-AzVMOperatingSystem” och ”Set-AzVmssOsProfile”.</span><span class="sxs-lookup"><span data-stu-id="8d428-889">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="8d428-890">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="8d428-890">Breaking changes</span></span>
    - <span data-ttu-id="8d428-891">Parametern FilterExpression tas bort från cmdleten ”Get-AzVMImage”.</span><span class="sxs-lookup"><span data-stu-id="8d428-891">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="8d428-892">Parametern AssignIdentity tas bort från cmdletarna ”New-AzVmssConfig”, ”New-AzVMConfig” och ”Update-AzVM”.</span><span class="sxs-lookup"><span data-stu-id="8d428-892">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="8d428-893">AutomaticRepairMaxInstanceRepairsPercent tas bort från cmdletarna ”New-AzVmssConfig” och ”Update-AzVmss”.</span><span class="sxs-lookup"><span data-stu-id="8d428-893">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="8d428-894">Egenskaperna AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus och VirtualMachineScaleSetsColocationStatus tas bort från ProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="8d428-894">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="8d428-895">Egenskapen MaxInstanceRepairsPercent tas bort från AutomaticRepairsPolicy.</span><span class="sxs-lookup"><span data-stu-id="8d428-895">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="8d428-896">Typerna AvailabilitySets, VirtualMachines och VirtualMachineScaleSets ändras från IList<SubResource> till IList<SubResourceWithColocationStatus>.</span><span class="sxs-lookup"><span data-stu-id="8d428-896">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="8d428-897">Beskrivningen för cmdleten ”Get-AzVM” har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="8d428-897">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="8d428-898">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8d428-898">Az.DataFactory</span></span>
* <span data-ttu-id="8d428-899">CRUD-stöd för egenskaper för dataflödeskörning  i hanterad IR.</span><span class="sxs-lookup"><span data-stu-id="8d428-899">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="8d428-900">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="8d428-900">Az.FrontDoor</span></span>
* <span data-ttu-id="8d428-901">Nya cmdletar har lagts till för att skapa, uppdatera, hämta och ta bort (CRUD) Front Door-regelmotorobjekt</span><span class="sxs-lookup"><span data-stu-id="8d428-901">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="8d428-902">Hjälp-cmdletar har lagts till för konstruktion av Front Door-regelmotorobjekt</span><span class="sxs-lookup"><span data-stu-id="8d428-902">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="8d428-903">Regelmotorreferens har lagts till för Front Door-hanteringsregelobjekt.</span><span class="sxs-lookup"><span data-stu-id="8d428-903">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="8d428-904">Parametrar för Private Link har lagts till för Front Door-serverdelsobjekt</span><span class="sxs-lookup"><span data-stu-id="8d428-904">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="8d428-905">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="8d428-905">Az.Functions</span></span>
* <span data-ttu-id="8d428-906">Allmän tillgänglighet för ”Az.Functions”-modulen</span><span class="sxs-lookup"><span data-stu-id="8d428-906">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="8d428-907">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8d428-907">Az.HDInsight</span></span>
* <span data-ttu-id="8d428-908">Stöd för diskkryptering med kundhanterad nyckel.</span><span class="sxs-lookup"><span data-stu-id="8d428-908">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="8d428-909">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="8d428-909">Az.HealthcareApis</span></span>
* <span data-ttu-id="8d428-910">Åtkomstprinciper använder inte längre det aktiva huvudkontot som standard</span><span class="sxs-lookup"><span data-stu-id="8d428-910">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8d428-911">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8d428-911">Az.IotHub</span></span>
* <span data-ttu-id="8d428-912">En cmdlet har lagts till som anropar en fråga i en IoT-hubb för att hämta information med ett SQL-liknande språk.</span><span class="sxs-lookup"><span data-stu-id="8d428-912">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="8d428-913">Problemet som gjorde att ”Add-AzIotHubDevice” inte skapade en Edge-aktiverad enhet utan underordnade enheter har åtgärdats [#11597]</span><span class="sxs-lookup"><span data-stu-id="8d428-913">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="8d428-914">En cmdlet har lagts till för att generera SAS-token för en Iot-hubb, enhet eller modul.</span><span class="sxs-lookup"><span data-stu-id="8d428-914">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="8d428-915">En cmdlet har lagts till för att anropa en måttfråga om konfiguration.</span><span class="sxs-lookup"><span data-stu-id="8d428-915">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="8d428-916">Hantera automatisk distribution av IoT Edge i stor skala.</span><span class="sxs-lookup"><span data-stu-id="8d428-916">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="8d428-917">Nya cmdlet:ar är:</span><span class="sxs-lookup"><span data-stu-id="8d428-917">New cmdlets are:</span></span>
    - <span data-ttu-id="8d428-918">”Add-AzIotHubDeployment”</span><span class="sxs-lookup"><span data-stu-id="8d428-918">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="8d428-919">”Get-AzIotHubDeployment”</span><span class="sxs-lookup"><span data-stu-id="8d428-919">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="8d428-920">”Remove-AzIotHubDeployment”</span><span class="sxs-lookup"><span data-stu-id="8d428-920">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="8d428-921">”Set-AzIotHubDeployment”</span><span class="sxs-lookup"><span data-stu-id="8d428-921">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="8d428-922">En cmdlet har lagts till för att anropa en måttfråga om IoT Edge-distribution.</span><span class="sxs-lookup"><span data-stu-id="8d428-922">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="8d428-923">En cmdlet har lagts till för att tillämpa konfigurationsinnehåll på den angivna gränsenheten.</span><span class="sxs-lookup"><span data-stu-id="8d428-923">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8d428-924">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8d428-924">Az.KeyVault</span></span>
* <span data-ttu-id="8d428-925">Två alias har tagits bort: ”New-AzKeyVaultCertificateAdministratorDetails” och ”New-AzKeyVaultCertificateOrganizationDetails”</span><span class="sxs-lookup"><span data-stu-id="8d428-925">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="8d428-926">Nu är mjuk borttagning aktiverat som standard när ett nyckelvalv skapas</span><span class="sxs-lookup"><span data-stu-id="8d428-926">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="8d428-927">Nätverksregler kan ställas in för att styra åtkomsten från särskilda nätverksplatser när du skapar ett nyckelvalv</span><span class="sxs-lookup"><span data-stu-id="8d428-927">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="8d428-928">Stöd för BYOK (Bring Your Own Key) har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-928">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="8d428-929">”Add-AzKeyVaultKey” stöder generering av en KeyExchange-nyckel</span><span class="sxs-lookup"><span data-stu-id="8d428-929">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="8d428-930">”Get-AzKeyVaultKey” stöder nedladdning av en offentlig nyckel i PEM-format</span><span class="sxs-lookup"><span data-stu-id="8d428-930">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="8d428-931">”KeyOps”-delen av hjälpdokumentet för ”Add-AzKeyVaultKey” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="8d428-931">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8d428-932">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8d428-932">Az.Monitor</span></span>
* <span data-ttu-id="8d428-933">Bugg för ”Set-AzDiagnosticSettings” har åtgärdats; kvarhållningsprincipen tillämpas inte på alla kategorier [#11589]</span><span class="sxs-lookup"><span data-stu-id="8d428-933">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="8d428-934">Stöd för WebTest-tillgänglighetskriterier för måttavisering V2</span><span class="sxs-lookup"><span data-stu-id="8d428-934">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="8d428-935">”New-AzMetricAlertRuleV2Criteria”: ett alternativ för att skapa tillgänglighetskriterier för webbtest har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-935">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="8d428-936">”Add-AzMetricAlertRuleV2”: stöd för de nya tillgänglighetskriterierna för webbtest</span><span class="sxs-lookup"><span data-stu-id="8d428-936">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="8d428-937">Redundant definition har tagits bort för RetentionPolicy i PSLogProfile [#7608]</span><span class="sxs-lookup"><span data-stu-id="8d428-937">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="8d428-938">Redundanta egenskaper som definierats i PSEventData har tagits bort [#11353]</span><span class="sxs-lookup"><span data-stu-id="8d428-938">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="8d428-939">”Get-AzLog” har bytt namn till ”Get-AzActivityLog”</span><span class="sxs-lookup"><span data-stu-id="8d428-939">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8d428-940">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d428-940">Az.Network</span></span>
* <span data-ttu-id="8d428-941">Attribut för icke-bakåtkompatibel ändring har lagts till för att meddela att standardbeteendet för zoner kommer att ändras</span><span class="sxs-lookup"><span data-stu-id="8d428-941">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="8d428-942">”New-AzPublicIpAddress”</span><span class="sxs-lookup"><span data-stu-id="8d428-942">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="8d428-943">”New-AzPublicIpPrefix”</span><span class="sxs-lookup"><span data-stu-id="8d428-943">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="8d428-944">”New-AzLoadBalancerFrontendIpConfig”</span><span class="sxs-lookup"><span data-stu-id="8d428-944">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="8d428-945">Stöd har lagts till för en ny resurs på den översta nivån, SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="8d428-945">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="8d428-946">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="8d428-946">New cmdlets added:</span></span>
        - <span data-ttu-id="8d428-947">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="8d428-947">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="8d428-948">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="8d428-948">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="8d428-949">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="8d428-949">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="8d428-950">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="8d428-950">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="8d428-951">”RequiredZoneNames” har lagts till för ”PSPrivateLinkResource” och ”GroupId” för ”PSPrivateEndpointConnection”</span><span class="sxs-lookup"><span data-stu-id="8d428-951">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="8d428-952">Fel parametertyp för SuccessThresholdRoundTripTimeMs-parametern för New-AzNetworkWatcherConnectionMonitorTestConfigurationObject har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8d428-952">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="8d428-953">VirtualWan-cmdletar har uppdaterats för att ange AllowVnetToVnetTraffic-argumentets standardvärde till True.</span><span class="sxs-lookup"><span data-stu-id="8d428-953">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="8d428-954">”New-AzVirtualWan”</span><span class="sxs-lookup"><span data-stu-id="8d428-954">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="8d428-955">”Update-AzVirtualWan”</span><span class="sxs-lookup"><span data-stu-id="8d428-955">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="8d428-956">Nya cmdletar har lagts till för att stödja DNS-zongrupp för privat slutpunkt</span><span class="sxs-lookup"><span data-stu-id="8d428-956">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="8d428-957">”New-AzPrivateDnsZoneConfig”</span><span class="sxs-lookup"><span data-stu-id="8d428-957">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="8d428-958">”Get-AzPrivateDnsZoneGroup”</span><span class="sxs-lookup"><span data-stu-id="8d428-958">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="8d428-959">”New-AzPrivateDnsZoneGroup”</span><span class="sxs-lookup"><span data-stu-id="8d428-959">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="8d428-960">”Set-AzPrivateDnsZoneGroup”</span><span class="sxs-lookup"><span data-stu-id="8d428-960">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="8d428-961">”Remove-AzPrivateDnsZoneGroup”</span><span class="sxs-lookup"><span data-stu-id="8d428-961">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="8d428-962">Parametrarna ”DNSEnableProxy”, ”DNSRequireProxyForNetworkRules” och ”DNSServers” har lagts till för ”AzureFirewall”</span><span class="sxs-lookup"><span data-stu-id="8d428-962">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="8d428-963">Parametrarna ”EnableDnsProxy”, ”DnsProxyNotRequiredForNetworkRule” och ”DnsServer” har lagts till för ”AzureFirewall”</span><span class="sxs-lookup"><span data-stu-id="8d428-963">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="8d428-964">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="8d428-964">Updated cmdlet:</span></span>
        - <span data-ttu-id="8d428-965">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="8d428-965">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8d428-966">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8d428-966">Az.OperationalInsights</span></span>
* <span data-ttu-id="8d428-967">Äldre kod har uppdaterats för att tillämpa ny genererad SDK</span><span class="sxs-lookup"><span data-stu-id="8d428-967">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="8d428-968">Cmdletar har tagits bort på grund av föråldrade API:er</span><span class="sxs-lookup"><span data-stu-id="8d428-968">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="8d428-969">”Get-AzOperationalInsightsSavedSearchResult” (alias ”Get-AzOperationalInsightsSavedSearchResults”)</span><span class="sxs-lookup"><span data-stu-id="8d428-969">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="8d428-970">”Get-AzOperationalInsightsSearchResult” (alias ”Get-AzOperationalInsightsSearchResults”)</span><span class="sxs-lookup"><span data-stu-id="8d428-970">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="8d428-971">”Get-AzOperationalInsightsLinkTarget” (alias ”Get-AzOperationalInsightsLinkTargets”)</span><span class="sxs-lookup"><span data-stu-id="8d428-971">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="8d428-972">Parametrar har lagts till för ”Set-AzOperationalInsightsWorkspace” och ”New-AzOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="8d428-972">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="8d428-973">Cmdletar har skapats för länkat lagringskonto</span><span class="sxs-lookup"><span data-stu-id="8d428-973">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="8d428-974">Cmdletar har skapats för kluster och länkad tjänst</span><span class="sxs-lookup"><span data-stu-id="8d428-974">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8d428-975">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8d428-975">Az.RecoveryServices</span></span>
* <span data-ttu-id="8d428-976">Azure Site Recovery: Stöd har lagts till för att skydda VM-närhetsplaceringsgrupper för Azure till Azure-provider.</span><span class="sxs-lookup"><span data-stu-id="8d428-976">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="8d428-977">Azure Site Recovery: Stöd har lagts till för replikering mellan zoner.</span><span class="sxs-lookup"><span data-stu-id="8d428-977">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="8d428-978">Azure Backup: Stöd har lagts till för långsiktig kvarhållning för Azure FileShare-återställningspunkter.</span><span class="sxs-lookup"><span data-stu-id="8d428-978">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="8d428-979">Azure Backup: Egenskaper för diskexkludering har lagts till för cmdlet-utdata från ”Get-AzRecoveryServicesBackupItem”.</span><span class="sxs-lookup"><span data-stu-id="8d428-979">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="8d428-980">En privat slutpunkt har lagts till för filen med valvets autentiseringsuppgifter för Site Recovery-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="8d428-980">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8d428-981">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d428-981">Az.Resources</span></span>
* <span data-ttu-id="8d428-982">En varning har lagts till om visningsfördröjning när en ny rolldefinition skapas</span><span class="sxs-lookup"><span data-stu-id="8d428-982">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="8d428-983">Princip-cmdletar har ändrats för utmatning av starkt typifierade objekt</span><span class="sxs-lookup"><span data-stu-id="8d428-983">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="8d428-984">Parametern ”-TenantLevel” har tagits bort för användning med ”Get-AzResourceLock” [#11335]</span><span class="sxs-lookup"><span data-stu-id="8d428-984">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="8d428-985">”Remove-AzResourceGroup -Id ResourceId” har åtgärdats [#9882]</span><span class="sxs-lookup"><span data-stu-id="8d428-985">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="8d428-986">En ny cmdlet har lagts till för att hämta What-If-resultat för ARM-mallar i omfånget för resursgrupper: ”Get-AzDeploymentResourceGroupWhatIfResult”</span><span class="sxs-lookup"><span data-stu-id="8d428-986">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="8d428-987">En ny cmdlet har lagts till för att hämta What-If-resultat för ARM-mallar i prenumerationsomfånget: ”Get-AzDeploymentWhatIfResult”</span><span class="sxs-lookup"><span data-stu-id="8d428-987">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="8d428-988">Alias: ”Get-AzSubscriptionDeploymentWhatIf”</span><span class="sxs-lookup"><span data-stu-id="8d428-988">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="8d428-989">Parametrarna ”-WhatIf” och ”-Confirm” har åsidosatts för ”New-AzDeployment” och ”New-AzResourceGroupDeployment” för att använda What-If-resultat för ARM-mallar</span><span class="sxs-lookup"><span data-stu-id="8d428-989">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="8d428-990">Ett utfasningsmeddelande har lagts till för parametern ”ApiVersion” i distributions-cmdletar</span><span class="sxs-lookup"><span data-stu-id="8d428-990">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="8d428-991">En funktion har lagts till för att visa förbättrade felmeddelanden för distributionsfel</span><span class="sxs-lookup"><span data-stu-id="8d428-991">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="8d428-992">CorrelationId-loggning har lagts till för distributionsfel</span><span class="sxs-lookup"><span data-stu-id="8d428-992">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="8d428-993">Egenskapen ”error” har lagts till i utdata från distributionsskript</span><span class="sxs-lookup"><span data-stu-id="8d428-993">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="8d428-994">Nuget Microsoft.Azure.Management.ResourceManager har uppdaterats till ”3.7.1-preview”</span><span class="sxs-lookup"><span data-stu-id="8d428-994">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="8d428-995">Specifika testfall har tagits bort då egenskapen Error i DeploymentValidateResult har ändrats till lässkyddad från nuget 3.7.1-preview</span><span class="sxs-lookup"><span data-stu-id="8d428-995">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="8d428-996">GenericResourceExpanded har flyttats från SDK ResourceManager 3.7.1-preview</span><span class="sxs-lookup"><span data-stu-id="8d428-996">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="8d428-997">Stöd för taggar har lagts till för alla Get-cmdletar för distribution, samt</span><span class="sxs-lookup"><span data-stu-id="8d428-997">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="8d428-998">”New-AzDeployment”</span><span class="sxs-lookup"><span data-stu-id="8d428-998">'New-AzDeployment'</span></span>
    - <span data-ttu-id="8d428-999">”New-AzManagementGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="8d428-999">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="8d428-1000">”New-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="8d428-1000">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="8d428-1001">”New-AzTenantDeployment”</span><span class="sxs-lookup"><span data-stu-id="8d428-1001">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8d428-1002">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8d428-1002">Az.ServiceFabric</span></span>
* <span data-ttu-id="8d428-1003">En bugg har åtgärdats som gjorde att --SecretIdentifier fick fel tumavtryck för certifikat när ett certifikat lades till</span><span class="sxs-lookup"><span data-stu-id="8d428-1003">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="8d428-1004">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d428-1004">Az.Sql</span></span>
* <span data-ttu-id="8d428-1005">Förbättrade prestanda för:</span><span class="sxs-lookup"><span data-stu-id="8d428-1005">Enhance performance of:</span></span>
    - <span data-ttu-id="8d428-1006">”Set-AzSqlDatabaseSensitivityClassification”</span><span class="sxs-lookup"><span data-stu-id="8d428-1006">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="8d428-1007">”Set-AzSqlInstanceDatabaseSensitivityClassification”</span><span class="sxs-lookup"><span data-stu-id="8d428-1007">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="8d428-1008">”Remove-AzSqlDatabaseSensitivityClassification”</span><span class="sxs-lookup"><span data-stu-id="8d428-1008">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="8d428-1009">”Remove-AzSqlInstanceDatabaseSensitivityClassification”</span><span class="sxs-lookup"><span data-stu-id="8d428-1009">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="8d428-1010">”Enable-AzSqlDatabaseSensitivityRecommendation”</span><span class="sxs-lookup"><span data-stu-id="8d428-1010">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="8d428-1011">”Enable-AzSqlInstanceDatabaseSensitivityRecommendation”</span><span class="sxs-lookup"><span data-stu-id="8d428-1011">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="8d428-1012">”Disable-AzSqlDatabaseSensitivityRecommendation”</span><span class="sxs-lookup"><span data-stu-id="8d428-1012">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="8d428-1013">”Disable-AzSqlInstanceDatabaseSensitivityRecommendation”</span><span class="sxs-lookup"><span data-stu-id="8d428-1013">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="8d428-1014">Validering på klientsidan har tagits bort för parametern ”RetentionDays” från cmdleten ”Set-AzSqlDatabaseBackupShortTermRetentionPolicy”</span><span class="sxs-lookup"><span data-stu-id="8d428-1014">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="8d428-1015">Granskning av ett lagringskonto i Vnet; en bugg har åtgärdats som orsakade fel när en Storage Blob Data-deltagarroll skapades.</span><span class="sxs-lookup"><span data-stu-id="8d428-1015">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8d428-1016">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8d428-1016">Az.Storage</span></span>
* <span data-ttu-id="8d428-1017">”-AsJob” har lagts till för att hämta/lista konto med cmdleten ”Get-AzStorageAccount”</span><span class="sxs-lookup"><span data-stu-id="8d428-1017">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="8d428-1018">Gör KeyVersion valfri när lagringskontot uppdateras med KeyvaultEncryption, för att ge stöd för automatisk nyckelrotation</span><span class="sxs-lookup"><span data-stu-id="8d428-1018">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="8d428-1019">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="8d428-1019">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="8d428-1020">Problemet med borttagning av Azure-filkatalog i pipeline har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8d428-1020">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="8d428-1021">”Remove-AzStorageDirectory”</span><span class="sxs-lookup"><span data-stu-id="8d428-1021">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="8d428-1022">Åtgärdat [#9880]: Definitionen av DefaultAction-värdet för NetWorkRule har ändrats för konsekvens med Swagger.</span><span class="sxs-lookup"><span data-stu-id="8d428-1022">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="8d428-1023">”Update-AzStorageAccountNetworkRuleSet”</span><span class="sxs-lookup"><span data-stu-id="8d428-1023">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="8d428-1024">”Get-AzStorageAccountNetworkRuleSet”</span><span class="sxs-lookup"><span data-stu-id="8d428-1024">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="8d428-1025">Åtgärdat [#11624]: Hoppa över dubblettregler när NetworkRules läggs till, för att undvika serverfel</span><span class="sxs-lookup"><span data-stu-id="8d428-1025">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="8d428-1026">”Add-AzStorageAccountNetworkRule”</span><span class="sxs-lookup"><span data-stu-id="8d428-1026">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="8d428-1027">Microsoft.Azure.Cosmos.Table SDK har uppgraderats till 1.0.7</span><span class="sxs-lookup"><span data-stu-id="8d428-1027">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="8d428-1028">Ett varningsmeddelande har lagts till för att påminna användaren om att lista igen med ContinuationToken när endast delobjekt returneras i listan med DataLake Gen2-objekt,</span><span class="sxs-lookup"><span data-stu-id="8d428-1028">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="8d428-1029">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="8d428-1029">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="8d428-1030">Stöd för att skapa eller uppdatera lagringskonto med Azure Files Active Directory Domain Service-autentisering</span><span class="sxs-lookup"><span data-stu-id="8d428-1030">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="8d428-1031">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="8d428-1031">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="8d428-1032">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="8d428-1032">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="8d428-1033">Stöd för nya eller listade Kerberos-nycklar för lagringskontot</span><span class="sxs-lookup"><span data-stu-id="8d428-1033">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="8d428-1034">”New-AzStorageAccountKey”</span><span class="sxs-lookup"><span data-stu-id="8d428-1034">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="8d428-1035">”Get-AzStorageAccountKey”</span><span class="sxs-lookup"><span data-stu-id="8d428-1035">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="8d428-1036">Stöd för redundans med lagringskonto</span><span class="sxs-lookup"><span data-stu-id="8d428-1036">Supported failover Storage account</span></span>
    - <span data-ttu-id="8d428-1037">”Invoke-AzStorageAccountFailover”</span><span class="sxs-lookup"><span data-stu-id="8d428-1037">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="8d428-1038">Hjälpen för ”Get-AzStorageBlobCopyState” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="8d428-1038">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="8d428-1039">Hjälpen för ”Get-AzStorageFileCopyState” och ”Start-AzStorageBlobCopy” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="8d428-1039">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="8d428-1040">Lagringsklientbibliotek v12 har integrerats med Queue- och File-cmdletar</span><span class="sxs-lookup"><span data-stu-id="8d428-1040">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="8d428-1041">Utdatatypen har ändrats från CloudFile till AzureStorageFile; ursprungliga utdata blir en underordnad egenskap i den nya utmatningen</span><span class="sxs-lookup"><span data-stu-id="8d428-1041">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="8d428-1042">”Get-AzStorageFile”</span><span class="sxs-lookup"><span data-stu-id="8d428-1042">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="8d428-1043">”Remove-AzStorageFile”</span><span class="sxs-lookup"><span data-stu-id="8d428-1043">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="8d428-1044">”Get-AzStorageFileContent”</span><span class="sxs-lookup"><span data-stu-id="8d428-1044">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="8d428-1045">”Set-AzStorageFileContent”</span><span class="sxs-lookup"><span data-stu-id="8d428-1045">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="8d428-1046">”Start-AzStorageFileCopy”</span><span class="sxs-lookup"><span data-stu-id="8d428-1046">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="8d428-1047">Utdatatypen har ändrats från CloudFileDirectory till AzureStorageFileDirectory; ursprungliga utdata blir en underordnad egenskap i den nya utmatningen</span><span class="sxs-lookup"><span data-stu-id="8d428-1047">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="8d428-1048">”New-AzStorageDirectory”</span><span class="sxs-lookup"><span data-stu-id="8d428-1048">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="8d428-1049">”Remove-AzStorageDirectory”</span><span class="sxs-lookup"><span data-stu-id="8d428-1049">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="8d428-1050">Utdatatypen har ändrats från CloudFileShare till AzureStorageFileShare; ursprungliga utdata blir en underordnad egenskap i den nya utmatningen</span><span class="sxs-lookup"><span data-stu-id="8d428-1050">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="8d428-1051">”Get-AzStorageShare”</span><span class="sxs-lookup"><span data-stu-id="8d428-1051">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="8d428-1052">”New-AzStorageShare”</span><span class="sxs-lookup"><span data-stu-id="8d428-1052">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="8d428-1053">”Remove-AzStorageShare”</span><span class="sxs-lookup"><span data-stu-id="8d428-1053">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="8d428-1054">Utdatatypen har ändrats från FileShareProperties till AzureStorageFileShare; ursprungliga utdata blir en underordnad egenskap i den nya utmatningen</span><span class="sxs-lookup"><span data-stu-id="8d428-1054">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="8d428-1055">”Set-AzStorageShareQuota”</span><span class="sxs-lookup"><span data-stu-id="8d428-1055">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="8d428-1056">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="8d428-1056">Az.TrafficManager</span></span>
* <span data-ttu-id="8d428-1057">Felaktigt profilnamn har åtgärdats i utförliga utdata för ”DisableAzureTrafficManagerEndpoint”</span><span class="sxs-lookup"><span data-stu-id="8d428-1057">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8d428-1058">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8d428-1058">Az.Websites</span></span>
* <span data-ttu-id="8d428-1059">Stavfel har åtgärdats i hjälpen för ”Update-AzWebAppAccessRestrictionConfig”.</span><span class="sxs-lookup"><span data-stu-id="8d428-1059">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="8d428-1060">3.8.0 – April 2020</span><span class="sxs-lookup"><span data-stu-id="8d428-1060">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="8d428-1061">Höjdpunkter sedan den senaste uppdateringen</span><span class="sxs-lookup"><span data-stu-id="8d428-1061">Highlights since the last release</span></span>
* <span data-ttu-id="8d428-1062">PowerShell-versioner som Az.Storage stöder: Windows PowerShell 5.1, PowerShell Core 6.2.4+ och PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="8d428-1062">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="8d428-1063">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8d428-1063">Az.Accounts</span></span>
* <span data-ttu-id="8d428-1064">Uppdaterade URL:en för Azure PowerShell-enkäten i ”Resolve-AzError” [#11507]</span><span class="sxs-lookup"><span data-stu-id="8d428-1064">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="8d428-1065">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8d428-1065">Az.ApiManagement</span></span>
* <span data-ttu-id="8d428-1066">Lade till meddelande om icke-bakåtkompatibel ändring vid ändring i utdata för Azure File-cmdletar i en framtida version</span><span class="sxs-lookup"><span data-stu-id="8d428-1066">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="8d428-1067">"Set-AzApiManagementGroup" Uppdaterad dokumentation för att ange GroupId-parametern</span><span class="sxs-lookup"><span data-stu-id="8d428-1067">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="8d428-1068">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="8d428-1068">Az.Cdn</span></span>
* <span data-ttu-id="8d428-1069">Fast ChinaCDN-relaterad prissättning för SKU-visning</span><span class="sxs-lookup"><span data-stu-id="8d428-1069">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="8d428-1070">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8d428-1070">Az.CognitiveServices</span></span>
* <span data-ttu-id="8d428-1071">Identitet som stöds, kryptering, UserOwnedStorage</span><span class="sxs-lookup"><span data-stu-id="8d428-1071">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d428-1072">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d428-1072">Az.Compute</span></span>
* <span data-ttu-id="8d428-1073">Cmdleten ”Set-AzVmssOrchestrationServiceState” har lagts till.</span><span class="sxs-lookup"><span data-stu-id="8d428-1073">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="8d428-1074">”Get-AzVmss” med -InstanceView visar OrchestrationService-tillstånd.</span><span class="sxs-lookup"><span data-stu-id="8d428-1074">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8d428-1075">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8d428-1075">Az.IotHub</span></span>
* <span data-ttu-id="8d428-1076">Hantera den dubbla konfigurationen för IoT-enheter, nya cmdletar är:</span><span class="sxs-lookup"><span data-stu-id="8d428-1076">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="8d428-1077">'Get-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="8d428-1077">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="8d428-1078">'Update-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="8d428-1078">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="8d428-1079">En cmdlet har lagts till för att anropa direkt metod på en enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="8d428-1079">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="8d428-1080">Hantera dubbel konfiguration för IoT-enhetsmodul, nya cmdletar är:</span><span class="sxs-lookup"><span data-stu-id="8d428-1080">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="8d428-1081">'Get-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="8d428-1081">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="8d428-1082">'Update-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="8d428-1082">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="8d428-1083">Hantera IoT-automatisk konfiguration av enhetshantering i stor skala.</span><span class="sxs-lookup"><span data-stu-id="8d428-1083">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="8d428-1084">Nya cmdlet:ar är:</span><span class="sxs-lookup"><span data-stu-id="8d428-1084">New cmdlets are:</span></span>
    - <span data-ttu-id="8d428-1085">'Add-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="8d428-1085">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="8d428-1086">'Get-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="8d428-1086">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="8d428-1087">'Remove-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="8d428-1087">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="8d428-1088">'Set-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="8d428-1088">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="8d428-1089">En cmdlet har lagts till för att anropa en edge-modulmetod i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="8d428-1089">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8d428-1090">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8d428-1090">Az.KeyVault</span></span>
* <span data-ttu-id="8d428-1091">Har lagt till en ny cmdlet, "Update-AzKeyVault", som kan aktivera mjuk borttagning och rensning av skydd i ett valv</span><span class="sxs-lookup"><span data-stu-id="8d428-1091">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="8d428-1092">Har lagt till stöd i Microsoft.PowerShell.SecretManagement [#11178]</span><span class="sxs-lookup"><span data-stu-id="8d428-1092">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="8d428-1093">Åtgärdat fel i exemplen i 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span><span class="sxs-lookup"><span data-stu-id="8d428-1093">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="8d428-1094">Har lagt till stöd för privat slutpunkt</span><span class="sxs-lookup"><span data-stu-id="8d428-1094">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="8d428-1095">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="8d428-1095">Az.Maintenance</span></span>
* <span data-ttu-id="8d428-1096">Publicerar slutversion av underhålls-cmdletar för GA</span><span class="sxs-lookup"><span data-stu-id="8d428-1096">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8d428-1097">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8d428-1097">Az.Monitor</span></span>
* <span data-ttu-id="8d428-1098">Har lagt till cmdletar för privat länkomfång</span><span class="sxs-lookup"><span data-stu-id="8d428-1098">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="8d428-1099">'Get-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="8d428-1099">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="8d428-1100">'Remove-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="8d428-1100">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="8d428-1101">'New-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="8d428-1101">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="8d428-1102">'Update-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="8d428-1102">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="8d428-1103">'Get-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="8d428-1103">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="8d428-1104">'New-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="8d428-1104">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="8d428-1105">'Remove-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="8d428-1105">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8d428-1106">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d428-1106">Az.Network</span></span>
* <span data-ttu-id="8d428-1107">Uppdaterade cmdletar för att aktivera anslutning på privat IP för Virtual Network Gateway.</span><span class="sxs-lookup"><span data-stu-id="8d428-1107">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="8d428-1108">'New-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="8d428-1108">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="8d428-1109">'Set-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="8d428-1109">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="8d428-1110">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="8d428-1110">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="8d428-1111">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="8d428-1111">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="8d428-1112">Uppdaterade cmdletar för att aktivera FQDN-baserade LocalNetworkGateways och VpnSites</span><span class="sxs-lookup"><span data-stu-id="8d428-1112">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="8d428-1113">'New-AzLocalNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="8d428-1113">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="8d428-1114">'New-AzVpnSiteLink'</span><span class="sxs-lookup"><span data-stu-id="8d428-1114">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="8d428-1115">Stöd har lagts till för IPv6-adresstypen i ExpressRouteCircuitConnectionConfig (Global Reach)</span><span class="sxs-lookup"><span data-stu-id="8d428-1115">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="8d428-1116">Lade till 'Set-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="8d428-1116">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="8d428-1117">tillåter inställning av alla befintliga egenskaper inklusive IPv6CircuitConnectionProperties</span><span class="sxs-lookup"><span data-stu-id="8d428-1117">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="8d428-1118">Uppdaterade 'Add-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="8d428-1118">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="8d428-1119">Lade till en ytterligare valfri parameter, AddressPrefixType, för att specificera adresstypen för adressprefix</span><span class="sxs-lookup"><span data-stu-id="8d428-1119">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="8d428-1120">Uppdaterade cmdletar för att aktivera inställningen för DPD-timeout på Virtual Network Gateway-anslutningar.</span><span class="sxs-lookup"><span data-stu-id="8d428-1120">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="8d428-1121">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="8d428-1121">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="8d428-1122">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="8d428-1122">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="8d428-1123">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="8d428-1123">Az.PolicyInsights</span></span>
* <span data-ttu-id="8d428-1124">Cmdleten "Start-AzPolicyComplianceScan" har lagts till för att utlösa genomsökningar av principefterlevnad</span><span class="sxs-lookup"><span data-stu-id="8d428-1124">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="8d428-1125">Principdefinition, uppsättningsdefinition och tilldelningsversioner har lagts till i "Get-AzPolicyState"-utdata</span><span class="sxs-lookup"><span data-stu-id="8d428-1125">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8d428-1126">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8d428-1126">Az.ServiceFabric</span></span>
* <span data-ttu-id="8d428-1127">Förbättrad kodformatering och användbarhet för "New-AzServiceFabricCluster"-exempel</span><span class="sxs-lookup"><span data-stu-id="8d428-1127">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="8d428-1128">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d428-1128">Az.Sql</span></span>
* <span data-ttu-id="8d428-1129">Lade till cmdletarna "Get-AzSqlInstanceOperation" och "Stop-AzSqlInstanceOperation"</span><span class="sxs-lookup"><span data-stu-id="8d428-1129">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="8d428-1130">Stöd för granskning för ett lagringskonto i VNet.</span><span class="sxs-lookup"><span data-stu-id="8d428-1130">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8d428-1131">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8d428-1131">Az.Storage</span></span>
* <span data-ttu-id="8d428-1132">Lade till meddelande om icke-bakåtkompatibel ändring vid ändring i utdata för Azure File-cmdletar i en framtida version</span><span class="sxs-lookup"><span data-stu-id="8d428-1132">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="8d428-1133">Stöd för nya SkuName StandardGZRS, StandardRAGZRS när ett lagringskonto skapas/uppdateras</span><span class="sxs-lookup"><span data-stu-id="8d428-1133">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="8d428-1134">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="8d428-1134">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="8d428-1135">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="8d428-1135">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="8d428-1136">Stöd för DataLake Gen2</span><span class="sxs-lookup"><span data-stu-id="8d428-1136">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="8d428-1137">'New-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="8d428-1137">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="8d428-1138">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="8d428-1138">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="8d428-1139">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="8d428-1139">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="8d428-1140">'Move-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="8d428-1140">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="8d428-1141">'Set-AzDataLakeGen2ItemAclObject'</span><span class="sxs-lookup"><span data-stu-id="8d428-1141">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="8d428-1142">'Update-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="8d428-1142">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="8d428-1143">'Get-AzDataLakeGen2ItemContent'</span><span class="sxs-lookup"><span data-stu-id="8d428-1143">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="8d428-1144">'Remove-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="8d428-1144">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="8d428-1145">0.10.0-förhandsversion – April 2020</span><span class="sxs-lookup"><span data-stu-id="8d428-1145">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="8d428-1146">Allmänt</span><span class="sxs-lookup"><span data-stu-id="8d428-1146">General</span></span>
* <span data-ttu-id="8d428-1147">Az-moduler är nu tillgängliga i förhandsversion på Azure Stack Hub.</span><span class="sxs-lookup"><span data-stu-id="8d428-1147">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="8d428-1148">Därmed möjliggörs kompatibilitet för flera plattformar med Linux och macOs.</span><span class="sxs-lookup"><span data-stu-id="8d428-1148">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="8d428-1149">Azure Stack Hub stöder nu PowerShell Core med AZ-moduler. Mer information finns [här](https://aka.ms/az4AzureStack)</span><span class="sxs-lookup"><span data-stu-id="8d428-1149">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="8d428-1150">Supportprofil för AZ-moduler 2019-03-01-hybrid:</span><span class="sxs-lookup"><span data-stu-id="8d428-1150">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="8d428-1151">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="8d428-1151">Az.Billing</span></span>
  - <span data-ttu-id="8d428-1152">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d428-1152">Az.Compute</span></span>
  - <span data-ttu-id="8d428-1153">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="8d428-1153">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="8d428-1154">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8d428-1154">Az.EventHub</span></span>
  - <span data-ttu-id="8d428-1155">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8d428-1155">Az.IotHub</span></span>
  - <span data-ttu-id="8d428-1156">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8d428-1156">Az.KeyVault</span></span>
  - <span data-ttu-id="8d428-1157">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8d428-1157">Az.Monitor</span></span>
  - <span data-ttu-id="8d428-1158">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d428-1158">Az.Network</span></span>
  - <span data-ttu-id="8d428-1159">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d428-1159">Az.Resources</span></span>
  - <span data-ttu-id="8d428-1160">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8d428-1160">Az.Storage</span></span>
  - <span data-ttu-id="8d428-1161">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8d428-1161">Az.Websites</span></span>
* <span data-ttu-id="8d428-1162">Tre nya PowerShell-moduler för AZ har introducerats som fungerar med Azure Stack Hub, och de är Az.Databox, Az.IotHub och Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8d428-1162">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="8d428-1163">Kommandona är i princip oförändrade, med endast mindre ändringar som att AzureRM ändras till AZ</span><span class="sxs-lookup"><span data-stu-id="8d428-1163">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="8d428-1164">En uppdaterad länk till PowerShell-dokumentationen för Azure Stack Hub finns [här](https://aka.ms/InstallASHPowerShell)</span><span class="sxs-lookup"><span data-stu-id="8d428-1164">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="8d428-1165">3.7.0 – mars 2020</span><span class="sxs-lookup"><span data-stu-id="8d428-1165">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8d428-1166">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8d428-1166">Az.Accounts</span></span>
* <span data-ttu-id="8d428-1167">Åtgärdade ”Get-AzTenant”/”Get-AzDefault”/”Set-AzDefault”-utlösning av NullReferenceException när du inte är inloggad [#10292]</span><span class="sxs-lookup"><span data-stu-id="8d428-1167">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d428-1168">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d428-1168">Az.Compute</span></span>
* <span data-ttu-id="8d428-1169">Följande parametrar har lagts till i cmdleten ”New-AzDiskConfig”:</span><span class="sxs-lookup"><span data-stu-id="8d428-1169">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="8d428-1170">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="8d428-1170">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="8d428-1171">Tillåten krypteringsegenskap till målparametern för cmdleten ”New-AzGalleryImageVersion”.</span><span class="sxs-lookup"><span data-stu-id="8d428-1171">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="8d428-1172">Åtgärdade tempDisk-problem för cmdletarna ”Set-AzVmss”-Reimage och ”Invoke-AzVMReimage”.</span><span class="sxs-lookup"><span data-stu-id="8d428-1172">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="8d428-1173">[#11354]</span><span class="sxs-lookup"><span data-stu-id="8d428-1173">[#11354]</span></span>
* <span data-ttu-id="8d428-1174">Stöd har lagts till i nedanstående cmdletar för nytt SAP-tillägg</span><span class="sxs-lookup"><span data-stu-id="8d428-1174">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="8d428-1175">”Set-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="8d428-1175">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="8d428-1176">”Get-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="8d428-1176">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="8d428-1177">”Remove-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="8d428-1177">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="8d428-1178">”Update-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="8d428-1178">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="8d428-1179">Åtgärdade fel i exempel på hjälpdokument</span><span class="sxs-lookup"><span data-stu-id="8d428-1179">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="8d428-1180">Visade det exakta strängvärdet för VM PowerState i tabellformat.</span><span class="sxs-lookup"><span data-stu-id="8d428-1180">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="8d428-1181">”New-AzVmssConfig”: den fasta serialiseringen av egenskapen AutomaticRepairs när SinglePlacementGroup är inaktiverad.</span><span class="sxs-lookup"><span data-stu-id="8d428-1181">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="8d428-1182">[#11257]</span><span class="sxs-lookup"><span data-stu-id="8d428-1182">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8d428-1183">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8d428-1183">Az.DataFactory</span></span>
* <span data-ttu-id="8d428-1184">ADF .Net SDK har uppdaterats till 4.8.0</span><span class="sxs-lookup"><span data-stu-id="8d428-1184">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="8d428-1185">Valfria parametrar har lagts till i kommandot ”Invoke-AzDataFactoryV2Pipeline” för att stödja omkörning</span><span class="sxs-lookup"><span data-stu-id="8d428-1185">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8d428-1186">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8d428-1186">Az.DataLakeStore</span></span>
* <span data-ttu-id="8d428-1187">Lade till beskrivning för icke-bakåtkompatibel ändring för ”Export-AzDataLakeStoreItem” och ”Import-AzDataLakeStoreItem”</span><span class="sxs-lookup"><span data-stu-id="8d428-1187">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="8d428-1188">Lade till alternativ för bytekodning för ”New-AzDataLakeStoreItem”, ”Add-AzDAtaLakeStoreItemContent” och ”Get-AzDAtaLakeStoreItemContent”</span><span class="sxs-lookup"><span data-stu-id="8d428-1188">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="8d428-1189">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8d428-1189">Az.HDInsight</span></span>
* <span data-ttu-id="8d428-1190">Stöd för att ange en minimal TLS-version som stöds när klustret skapas.</span><span class="sxs-lookup"><span data-stu-id="8d428-1190">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8d428-1191">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8d428-1191">Az.IotHub</span></span>
* <span data-ttu-id="8d428-1192">Stöd har lagts till för att hantera distribuerade inställningar per enhet.</span><span class="sxs-lookup"><span data-stu-id="8d428-1192">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="8d428-1193">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="8d428-1193">New Cmdlets are:</span></span>
    - <span data-ttu-id="8d428-1194">”Get-AzIotHubDistributedTracing”</span><span class="sxs-lookup"><span data-stu-id="8d428-1194">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="8d428-1195">”Set-AzIotHubDistributedTracing”</span><span class="sxs-lookup"><span data-stu-id="8d428-1195">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8d428-1196">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8d428-1196">Az.KeyVault</span></span>
* <span data-ttu-id="8d428-1197">Ändrade attribut för icke-bakåtkompatibel ändring lades till för ”New-AzKeyVault”</span><span class="sxs-lookup"><span data-stu-id="8d428-1197">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8d428-1198">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8d428-1198">Az.Monitor</span></span>
* <span data-ttu-id="8d428-1199">Uppdaterad dokumentation för ”New-AzScheduledQueryRuleLogMetricTrigger”</span><span class="sxs-lookup"><span data-stu-id="8d428-1199">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8d428-1200">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d428-1200">Az.Network</span></span>
* <span data-ttu-id="8d428-1201">Uppdaterade cmdletar för att tillåta VirtualHubVnetConnections mellan klienter</span><span class="sxs-lookup"><span data-stu-id="8d428-1201">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="8d428-1202">”New-AzVirtualHubVnetConnection”</span><span class="sxs-lookup"><span data-stu-id="8d428-1202">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="8d428-1203">”Update-AzVirtualHubVnetConnection”</span><span class="sxs-lookup"><span data-stu-id="8d428-1203">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="8d428-1204">”New-AzVirtualHub”</span><span class="sxs-lookup"><span data-stu-id="8d428-1204">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="8d428-1205">”Update-AzVirtualHub”</span><span class="sxs-lookup"><span data-stu-id="8d428-1205">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="8d428-1206">SQL Management SDK-beroende har tagits bort</span><span class="sxs-lookup"><span data-stu-id="8d428-1206">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="8d428-1207">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="8d428-1207">Az.PolicyInsights</span></span>
* <span data-ttu-id="8d428-1208">Förbättrade felmeddelanden</span><span class="sxs-lookup"><span data-stu-id="8d428-1208">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8d428-1209">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8d428-1209">Az.RecoveryServices</span></span>
* <span data-ttu-id="8d428-1210">Azure Site Recovery har lagt till stöd för återaktivering av skydd och uppdaterade VM-egenskaper för virtuella Azure-datorer med krypterad disk.</span><span class="sxs-lookup"><span data-stu-id="8d428-1210">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="8d428-1211">Lade till Azure Site Recovery VmwareToAzure-egenskaper för DR-övervakning</span><span class="sxs-lookup"><span data-stu-id="8d428-1211">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="8d428-1212">Azure Backup har lagt till stöd för att försöka uppdatera principuppdateringen för misslyckade objekt på nytt.</span><span class="sxs-lookup"><span data-stu-id="8d428-1212">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="8d428-1213">Azure Backup lagt till stöd för diskundantagsinställningar under säkerhetskopiering och återställning.</span><span class="sxs-lookup"><span data-stu-id="8d428-1213">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="8d428-1214">Azure Backup lagt till stöd för att återställa flera filer/mappar i AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="8d428-1214">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="8d428-1215">Azure Backup lade till support för användardefinierad Resourcegroup-support vid uppdatering av IaasVM-princip</span><span class="sxs-lookup"><span data-stu-id="8d428-1215">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="8d428-1216">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d428-1216">Az.Resources</span></span>
* <span data-ttu-id="8d428-1217">Åtgärdade ”Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType” så att den använder den faktisk apiVersion av resurser i stället för standard-apiVersion [#11267]</span><span class="sxs-lookup"><span data-stu-id="8d428-1217">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="8d428-1218">Lade till correlationId-loggning för felscenarier</span><span class="sxs-lookup"><span data-stu-id="8d428-1218">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="8d428-1219">Liten dokumentationsändring för ”Get-AzResourceLock”.</span><span class="sxs-lookup"><span data-stu-id="8d428-1219">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="8d428-1220">Lade till exempel.</span><span class="sxs-lookup"><span data-stu-id="8d428-1220">Added example.</span></span>
* <span data-ttu-id="8d428-1221">Undantaget enkelt citattecken i parametervärde för ”Get-AzADUser” [#11317]</span><span class="sxs-lookup"><span data-stu-id="8d428-1221">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="8d428-1222">Nya cmdletar har lagts till för distributionsskript (”Get-AzDeploymentScript”, ”Get-AzDeploymentScriptLog”, ”Save-AzDeploymentScriptLog”, ”Remove-AzDeploymentScript”)</span><span class="sxs-lookup"><span data-stu-id="8d428-1222">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="8d428-1223">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d428-1223">Az.Sql</span></span>
* <span data-ttu-id="8d428-1224">En läsbar sekundär parameter har lagts till i Invoke-AzSqlDatabaseFailover</span><span class="sxs-lookup"><span data-stu-id="8d428-1224">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="8d428-1225">Cmdleten Disable-AzSqlServerActiveDirectoryOnlyAuthentication har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-1225">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="8d428-1226">Den sparade känslighet rangordningen när kolumner klassificeras i databasen.</span><span class="sxs-lookup"><span data-stu-id="8d428-1226">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="8d428-1227">Az.Support</span><span class="sxs-lookup"><span data-stu-id="8d428-1227">Az.Support</span></span>
* <span data-ttu-id="8d428-1228">Allmän tillgänglighet för ”Az.Support”-modulen</span><span class="sxs-lookup"><span data-stu-id="8d428-1228">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8d428-1229">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8d428-1229">Az.Websites</span></span>
* <span data-ttu-id="8d428-1230">Stöd har lagts till för att arbeta med trafikdirigeringsregler för webbappar under nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="8d428-1230">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="8d428-1231">”Get-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="8d428-1231">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="8d428-1232">”Update-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="8d428-1232">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="8d428-1233">”Add-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="8d428-1233">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="8d428-1234">”Remove-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="8d428-1234">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="8d428-1235">3.6.1 – mars 2020</span><span class="sxs-lookup"><span data-stu-id="8d428-1235">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8d428-1236">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8d428-1236">Az.Accounts</span></span>
* <span data-ttu-id="8d428-1237">Öppna sidan med Azure PowerShell-enkäten i ”Send-Feedback” [#11020]</span><span class="sxs-lookup"><span data-stu-id="8d428-1237">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="8d428-1238">Visa URL:en för Azure PowerShell-enkäten i ”Resolve-Error” [#11021]</span><span class="sxs-lookup"><span data-stu-id="8d428-1238">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="8d428-1239">Az-version har lagts till i UserAgent</span><span class="sxs-lookup"><span data-stu-id="8d428-1239">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="8d428-1240">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8d428-1240">Az.ApiManagement</span></span>
* <span data-ttu-id="8d428-1241">Stöd har lagts till för att hämta och konfigurera en anpassad domän på DeveloperPortal-slutpunkten [#11007]</span><span class="sxs-lookup"><span data-stu-id="8d428-1241">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="8d428-1242">”Export-AzApiManagementApi” Stöd har lagts till för att ladda ned API-definition i Json-format [#9987]</span><span class="sxs-lookup"><span data-stu-id="8d428-1242">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="8d428-1243">”Import-AzApiManagementApi” Stöd har lagts till för att importera OpenApi 3.0-definition från Json-dokument</span><span class="sxs-lookup"><span data-stu-id="8d428-1243">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="8d428-1244">”New-AzApiManagementIdentityProvider” och ”Set-AzApiManagementIdentityProvider” Stöd har lagts till för att konfigurera ”Signin Tenant” för AAD B2C-provider [#9784]</span><span class="sxs-lookup"><span data-stu-id="8d428-1244">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8d428-1245">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8d428-1245">Az.DataLakeStore</span></span>
* <span data-ttu-id="8d428-1246">En referens har uttryckligen lagts till för System.Buffers i csproj och psd1.</span><span class="sxs-lookup"><span data-stu-id="8d428-1246">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8d428-1247">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8d428-1247">Az.IotHub</span></span>
* <span data-ttu-id="8d428-1248">Lade till stöd för att hantera enheter i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="8d428-1248">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="8d428-1249">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="8d428-1249">New Cmdlets are:</span></span>
    - <span data-ttu-id="8d428-1250">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="8d428-1250">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="8d428-1251">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="8d428-1251">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="8d428-1252">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="8d428-1252">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="8d428-1253">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="8d428-1253">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="8d428-1254">Stöd har lagts till för att hantera moduler på en mål-IoT-enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="8d428-1254">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="8d428-1255">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="8d428-1255">New Cmdlets are:</span></span>
    - <span data-ttu-id="8d428-1256">”Add-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="8d428-1256">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="8d428-1257">”Get-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="8d428-1257">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="8d428-1258">”Remove-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="8d428-1258">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="8d428-1259">”Set-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="8d428-1259">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="8d428-1260">Cmdlet har lagts till för att hämta anslutningssträngen för en mål-IoT-enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="8d428-1260">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="8d428-1261">Cmdlet har lagts till för att hämta anslutningssträngen för en modul på en mål-IoT-enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="8d428-1261">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="8d428-1262">Stöd har lagts till för att hämta/ange en överordnad enhet för en IoT-enhet.</span><span class="sxs-lookup"><span data-stu-id="8d428-1262">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="8d428-1263">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="8d428-1263">New Cmdlets are:</span></span>
    - <span data-ttu-id="8d428-1264">”Get-AzIotHubDeviceParent”</span><span class="sxs-lookup"><span data-stu-id="8d428-1264">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="8d428-1265">”Set-AzIotHubDeviceParent”</span><span class="sxs-lookup"><span data-stu-id="8d428-1265">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="8d428-1266">Stöd har lagts till för att hantera en enhets överordnade och underordnade relationer.</span><span class="sxs-lookup"><span data-stu-id="8d428-1266">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8d428-1267">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8d428-1267">Az.Monitor</span></span>
* <span data-ttu-id="8d428-1268">Utdatavärdet har åtgärdats för ”Get-AzMetricDefinition” [#9714]</span><span class="sxs-lookup"><span data-stu-id="8d428-1268">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8d428-1269">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d428-1269">Az.Network</span></span>
* <span data-ttu-id="8d428-1270">SQL Management SDK har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="8d428-1270">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="8d428-1271">Ett problem har åtgärdats med namngivningsskillnader i klassen PrivateLinkServiceConnectionState.</span><span class="sxs-lookup"><span data-stu-id="8d428-1271">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="8d428-1272">Fältet ActionsRequired mappar till ActionRequired.</span><span class="sxs-lookup"><span data-stu-id="8d428-1272">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="8d428-1273">PublicNetworkAccess har lagts till i ”New-AzSqlServer” och ”Set-AzSqlServer”</span><span class="sxs-lookup"><span data-stu-id="8d428-1273">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="8d428-1274">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d428-1274">Az.Resources</span></span>
* <span data-ttu-id="8d428-1275">Null-referensfel har åtgärdats i ”Get-AzRoleAssignment”</span><span class="sxs-lookup"><span data-stu-id="8d428-1275">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="8d428-1276">Växlarna ”-Force” och ”-PassThru” är valfria i ”Remove-AzADGroup” [#10849]</span><span class="sxs-lookup"><span data-stu-id="8d428-1276">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="8d428-1277">Ett problem har åtgärdats som gjorde att ”MailNickname” inte returnerades i ”Remove-AzADGroup” [#11167]</span><span class="sxs-lookup"><span data-stu-id="8d428-1277">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="8d428-1278">Ett problem har åtgärdats som gjorde att pipe-åtgärden ”Remove-AzADGroup” inte fungerar [#11171]</span><span class="sxs-lookup"><span data-stu-id="8d428-1278">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="8d428-1279">Ett null-referensfel har åtgärdats i GetAzureRoleAssignmentCommand</span><span class="sxs-lookup"><span data-stu-id="8d428-1279">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="8d428-1280">Attribut för icke-bakåtkompatibla ändringar har lagts till för kommande ändringar i cmdlets för principer</span><span class="sxs-lookup"><span data-stu-id="8d428-1280">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="8d428-1281">”Get-AzResourceGroup” har uppdaterats för att utföra taggfiltrering för resursgrupper på serversidan</span><span class="sxs-lookup"><span data-stu-id="8d428-1281">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="8d428-1282">Utökade Tag-cmdlets stöder -ResourceId</span><span class="sxs-lookup"><span data-stu-id="8d428-1282">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="8d428-1283">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="8d428-1283">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="8d428-1284">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="8d428-1284">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="8d428-1285">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="8d428-1285">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="8d428-1286">Ny Tag-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-1286">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="8d428-1287">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="8d428-1287">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="8d428-1288">Flyttade ScopedDeployment från SDK 3.3.0</span><span class="sxs-lookup"><span data-stu-id="8d428-1288">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="8d428-1289">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d428-1289">Az.Sql</span></span>
* <span data-ttu-id="8d428-1290">PublicNetworkAccess har lagts till i ”New-AzSqlServer” och ”Set-AzSqlServer”</span><span class="sxs-lookup"><span data-stu-id="8d428-1290">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="8d428-1291">Stöd har lagts till för konfiguration av säkerhetskopiering för långsiktig kvarhållning för hanterade databaser</span><span class="sxs-lookup"><span data-stu-id="8d428-1291">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="8d428-1292">Hämta/ange LTR-princip på en hanterad databas</span><span class="sxs-lookup"><span data-stu-id="8d428-1292">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="8d428-1293">Hämta LTR-säkerhetskopior efter hanterad databas, hanterad instans eller plats</span><span class="sxs-lookup"><span data-stu-id="8d428-1293">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="8d428-1294">Ta bort en LTR-säkerhetskopia</span><span class="sxs-lookup"><span data-stu-id="8d428-1294">Remove an LTR backup</span></span>
    - <span data-ttu-id="8d428-1295">Återställa en LTR-säkerhetskopia för att skapa en ny hanterad databas</span><span class="sxs-lookup"><span data-stu-id="8d428-1295">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="8d428-1296">MinimalTlsVersion har lagts till för New-AzSqlServer och Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="8d428-1296">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="8d428-1297">MinimalTlsVersion har lagts till för New-AzSqlInstance och Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="8d428-1297">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="8d428-1298">SQL SDK-versionen för Az.Network har ändrats</span><span class="sxs-lookup"><span data-stu-id="8d428-1298">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8d428-1299">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8d428-1299">Az.Storage</span></span>
* <span data-ttu-id="8d428-1300">AllowProtectedAppendWrite stöds i ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="8d428-1300">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="8d428-1301">”Set-AzRmStorageContainerImmutabilityPolicy”</span><span class="sxs-lookup"><span data-stu-id="8d428-1301">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="8d428-1302">Varningsmeddelande har lagts till om icke-bakåtkompatibel ändring för ändring av typen AzureStorageTable i en senare version</span><span class="sxs-lookup"><span data-stu-id="8d428-1302">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="8d428-1303">”New-AzStorageTable”</span><span class="sxs-lookup"><span data-stu-id="8d428-1303">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="8d428-1304">”Get-AzStorageTable”</span><span class="sxs-lookup"><span data-stu-id="8d428-1304">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8d428-1305">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8d428-1305">Az.Websites</span></span>
* <span data-ttu-id="8d428-1306">Tag-parametern har lagts till för ”New-AzAppServicePlan” och ”Set-AzAppServicePlan”</span><span class="sxs-lookup"><span data-stu-id="8d428-1306">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="8d428-1307">Stoppa cmdlet-körning om ett undantag uppstår när en anpassad domän läggs till på en webbplats</span><span class="sxs-lookup"><span data-stu-id="8d428-1307">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="8d428-1308">Stöd har lagts till för att utföra åtgärder för App Services som inte tillhör samma resursgrupp som App Services-planen</span><span class="sxs-lookup"><span data-stu-id="8d428-1308">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="8d428-1309">Åtkomstbegränsning har tillämpats på WebApp/Function i olika resursgrupper</span><span class="sxs-lookup"><span data-stu-id="8d428-1309">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="8d428-1310">Ett problem har åtgärdats för att ange anpassade värdnamn för WebAppSlots</span><span class="sxs-lookup"><span data-stu-id="8d428-1310">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="8d428-1311">3.5.0 – februari 2020</span><span class="sxs-lookup"><span data-stu-id="8d428-1311">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="8d428-1312">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="8d428-1312">Highlights since the last major release</span></span>
* <span data-ttu-id="8d428-1313">Uppdaterade telemetri på klientsidan.</span><span class="sxs-lookup"><span data-stu-id="8d428-1313">Updated client side telemetry.</span></span>
* <span data-ttu-id="8d428-1314">Az.IotHub lade till cmdletar som stöd för att hantera enheter.</span><span class="sxs-lookup"><span data-stu-id="8d428-1314">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="8d428-1315">Az.SqlVirtualMachine lade till cmdletar för lyssningsfunktion för tillgänglighetsgrupp.</span><span class="sxs-lookup"><span data-stu-id="8d428-1315">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="8d428-1316">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8d428-1316">Az.Accounts</span></span>
* <span data-ttu-id="8d428-1317">Lade till SubscriptionId, TenantId och körningstid i data för telemetri på klientsidan</span><span class="sxs-lookup"><span data-stu-id="8d428-1317">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8d428-1318">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8d428-1318">Az.Automation</span></span>
* <span data-ttu-id="8d428-1319">Åtgärdade skrivfel i exempel 1 i referensdokumentation för ”New-AzAutomationSoftwareUpdateConfiguration”</span><span class="sxs-lookup"><span data-stu-id="8d428-1319">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="8d428-1320">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8d428-1320">Az.CognitiveServices</span></span>
* <span data-ttu-id="8d428-1321">Uppdaterade SDK till 7.0</span><span class="sxs-lookup"><span data-stu-id="8d428-1321">Updated SDK to 7.0</span></span>
* <span data-ttu-id="8d428-1322">Förbättrade felmeddelande vid serversvar om tom brödtext</span><span class="sxs-lookup"><span data-stu-id="8d428-1322">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d428-1323">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d428-1323">Az.Compute</span></span>
* <span data-ttu-id="8d428-1324">Tillät tomt värde för ProximityPlacementGroupId under uppdatering</span><span class="sxs-lookup"><span data-stu-id="8d428-1324">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="8d428-1325">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="8d428-1325">Az.FrontDoor</span></span>
* <span data-ttu-id="8d428-1326">Lade till cmdlet för att hämta hanterade regeldefinitioner som kan användas i WAF</span><span class="sxs-lookup"><span data-stu-id="8d428-1326">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8d428-1327">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8d428-1327">Az.IotHub</span></span>
* <span data-ttu-id="8d428-1328">Lade till stöd för att hantera enheter i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="8d428-1328">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="8d428-1329">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="8d428-1329">New Cmdlets are:</span></span>
    - <span data-ttu-id="8d428-1330">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="8d428-1330">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="8d428-1331">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="8d428-1331">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="8d428-1332">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="8d428-1332">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="8d428-1333">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="8d428-1333">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8d428-1334">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8d428-1334">Az.KeyVault</span></span>
* <span data-ttu-id="8d428-1335">Åtgärdade duplicerad text för Add-AzKeyVaultKey.md</span><span class="sxs-lookup"><span data-stu-id="8d428-1335">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8d428-1336">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8d428-1336">Az.Monitor</span></span>
* <span data-ttu-id="8d428-1337">Åtgärdade beskrivning av cmdleten Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="8d428-1337">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="8d428-1338">En ny parameter med namnet ActionGroupId har lagts till i kommandot ”New-AzMetricAlertRuleV2”.</span><span class="sxs-lookup"><span data-stu-id="8d428-1338">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="8d428-1339">Användaren kan ange ActionGroupId(string) eller ActionGroup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="8d428-1339">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8d428-1340">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d428-1340">Az.Network</span></span>
* <span data-ttu-id="8d428-1341">Lade till en extra parameteranteckning för parametern ”-EnableProxyProtocol” för cmdleten ”New-AzPrivateLinkService”.</span><span class="sxs-lookup"><span data-stu-id="8d428-1341">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="8d428-1342">Åtgärdade FilterData-exempel i Start-AzVirtualNetworkGatewayConnectionPacketCapture.md och Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="8d428-1342">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="8d428-1343">Lade till paketinsamlingsexempel för att samla in alla inre och yttre paket i Start-AzVirtualNetworkGatewayConnectionPacketCapture.md och Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="8d428-1343">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="8d428-1344">Lade till stöd för Azure-brandväggsprincip på VNet-brandväggar</span><span class="sxs-lookup"><span data-stu-id="8d428-1344">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="8d428-1345">Inga nya cmdletar har lagts till.</span><span class="sxs-lookup"><span data-stu-id="8d428-1345">No new cmdlets are added.</span></span> <span data-ttu-id="8d428-1346">Lättar begränsningen för brandväggsprincip på VNet-brandväggar</span><span class="sxs-lookup"><span data-stu-id="8d428-1346">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8d428-1347">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8d428-1347">Az.RecoveryServices</span></span>
* <span data-ttu-id="8d428-1348">Lade till stöd för Restore-as-files för SQL-databaser.</span><span class="sxs-lookup"><span data-stu-id="8d428-1348">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8d428-1349">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d428-1349">Az.Resources</span></span>
* <span data-ttu-id="8d428-1350">Omstrukturerade cmdletar för malldistribution</span><span class="sxs-lookup"><span data-stu-id="8d428-1350">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="8d428-1351">Lade till nya cmdletar för att hantera distributioner i hanteringsgruppen: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8d428-1351">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="8d428-1352">Lade till nya cmdletar för att hantera distributioner i klientorganisationsområdet: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="8d428-1352">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="8d428-1353">Omstrukturerade \*-AzDeployment-cmdletar för att fungera specifikt i prenumerationsomfattningen</span><span class="sxs-lookup"><span data-stu-id="8d428-1353">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="8d428-1354">Skapade alias \*-AzSubscriptionDeployment för \*-AzDeployment-cmdletar</span><span class="sxs-lookup"><span data-stu-id="8d428-1354">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="8d428-1355">Åtgärdade ”Update-AzADApplication” när parametern ”AvailableToOtherTenants” inte har angetts</span><span class="sxs-lookup"><span data-stu-id="8d428-1355">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="8d428-1356">Tog bort ApplicationObjectWithoutCredentialParameterSet för att undvika AmbiguousParameterSetException.</span><span class="sxs-lookup"><span data-stu-id="8d428-1356">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="8d428-1357">Återskapade hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="8d428-1357">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="8d428-1358">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d428-1358">Az.Sql</span></span>
* <span data-ttu-id="8d428-1359">Lade till stöd för återställning till tidpunkt mellan prenumerationer på hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="8d428-1359">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="8d428-1360">Lade till stöd för att ändra befintlig SQL Managed Instance-maskinvarugenerering</span><span class="sxs-lookup"><span data-stu-id="8d428-1360">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="8d428-1361">Åtgärdade ”Update-AzSqlServerVulnerabilityAssessmentSetting”-hjälpexempel: parameter/egenskapsutdata - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="8d428-1361">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="8d428-1362">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="8d428-1362">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="8d428-1363">Lade till cmdletar för lyssningsfunktion för tillgänglighetsgrupp</span><span class="sxs-lookup"><span data-stu-id="8d428-1363">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="8d428-1364">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="8d428-1364">Az.StorageSync</span></span>
* <span data-ttu-id="8d428-1365">Uppdaterade teckenuppsättningar som stöds i ”Invoke-AzStorageSyncCompatibilityCheck”.</span><span class="sxs-lookup"><span data-stu-id="8d428-1365">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="8d428-1366">3.4.0 – februari 2020</span><span class="sxs-lookup"><span data-stu-id="8d428-1366">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="8d428-1367">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="8d428-1367">Highlights since the last major release</span></span>
* <span data-ttu-id="8d428-1368">Första Az.CosmosDB-versionen 0.1.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="8d428-1368">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="8d428-1369">Stöd för Az.Network ConnectionMonitor V2 har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-1369">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="8d428-1370">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8d428-1370">Az.Accounts</span></span>
* <span data-ttu-id="8d428-1371">Inaktivera automatisk sparande av kontext när AzureRmContext.json inte är tillgängligt</span><span class="sxs-lookup"><span data-stu-id="8d428-1371">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="8d428-1372">Uppdatera referensen till Azure Powershell Common till 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="8d428-1372">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="8d428-1373">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8d428-1373">Az.ApiManagement</span></span>
* <span data-ttu-id="8d428-1374">**Get-AzApiManagementApiSchema** Hämtning av Open-Api-schema som är associerat med ett API har åtgärdats   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="8d428-1374">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="8d428-1375">**New-AzApiManagementProduct** _ och _ *Set-AzApiManagementProduct*\*</span><span class="sxs-lookup"><span data-stu-id="8d428-1375">**New-AzApiManagementProduct** _ and _ *Set-AzApiManagementProduct*\*</span></span>
  - <span data-ttu-id="8d428-1376">Åtgärda dokumentation för https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="8d428-1376">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="8d428-1377">**Set-AzApiManagementApi** Exempel för att visa hur ServiceUrl uppdateras med hjälp av cmdleten har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-1377">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d428-1378">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d428-1378">Az.Compute</span></span>
* <span data-ttu-id="8d428-1379">Begränsa antalet VM-status till 100 för att undvika begränsning när Get-AzVM -Status utförs utan VM-namn.</span><span class="sxs-lookup"><span data-stu-id="8d428-1379">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="8d428-1380">Lägg till cmdleten Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="8d428-1380">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="8d428-1381">Lägg till parametrarna EncryptionType och DiskEncryptionSetId i följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="8d428-1381">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="8d428-1382">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="8d428-1382">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="8d428-1383">Lägg till parametern ColocationStatus för cmdleten Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="8d428-1383">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8d428-1384">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8d428-1384">Az.DataFactory</span></span>
* <span data-ttu-id="8d428-1385">Uppdatera ADF .Net SDK-versionen till 4.7.0</span><span class="sxs-lookup"><span data-stu-id="8d428-1385">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="8d428-1386">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="8d428-1386">Az.DeploymentManager</span></span>
* <span data-ttu-id="8d428-1387">Lägger till LIST-åtgärder för resurser</span><span class="sxs-lookup"><span data-stu-id="8d428-1387">Adds LIST operations for resources</span></span>
* <span data-ttu-id="8d428-1388">Lägger till funktion för att utföra åtgärder för hälsokontrollsteg</span><span class="sxs-lookup"><span data-stu-id="8d428-1388">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="8d428-1389">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8d428-1389">Az.HDInsight</span></span>
* <span data-ttu-id="8d428-1390">Åtgärda dokumentfel för New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="8d428-1390">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8d428-1391">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8d428-1391">Az.KeyVault</span></span>
* <span data-ttu-id="8d428-1392">Lägg till Name-alias för attributet VaultName så att Remove-AzureKeyVault stämmer överens med New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="8d428-1392">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8d428-1393">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d428-1393">Az.Network</span></span>
* <span data-ttu-id="8d428-1394">Nytt exempel har lagts till i Set-AzNetworkWatcherConfigFlowLog.md för att demonstrera ett inaktiveringsscenario för Trafikanalys.</span><span class="sxs-lookup"><span data-stu-id="8d428-1394">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="8d428-1395">Lägg till stöd för att tilldela konfiguration av hanterings-IP till Azure Firewall – ett dedikerat undernät och en offentlig IP som brandväggen använder för dess hanteringstrafik</span><span class="sxs-lookup"><span data-stu-id="8d428-1395">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="8d428-1396">Cmdleten New-AzFirewall har uppdaterats:</span><span class="sxs-lookup"><span data-stu-id="8d428-1396">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="8d428-1397">Parametern -ManagementPublicIpAddress (inte obligatorisk) som accepterar ett offentligt IP-adressobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-1397">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="8d428-1398">Metoden SetManagementIpConfiguration har lagts till för brandväggsobjekt – kräver ett undernät och en offentlig IP-adress som indata – undernätets namn måste vara ”AzureFirewallManagementSubnet”</span><span class="sxs-lookup"><span data-stu-id="8d428-1398">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="8d428-1399">Exempel för Get-AzNetworkSecurityGroup har korrigerats så att exempel visas för NSG:er i stället för nätverksgränssnitt.</span><span class="sxs-lookup"><span data-stu-id="8d428-1399">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="8d428-1400">Ett skrivfel har åtgärdats i kommandot New-AzVpnSite som hindrade kompletteraren för resurs-ID från att fylla i en parameter.</span><span class="sxs-lookup"><span data-stu-id="8d428-1400">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="8d428-1401">Stöd för Url-konfiguration i åtgärdsuppsättningen för omskrivningsregler i Application Gateway har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-1401">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="8d428-1402">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="8d428-1402">New cmdlets added:</span></span>
        - <span data-ttu-id="8d428-1403">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="8d428-1403">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="8d428-1404">Cmdletar har uppdaterats med den valfria parametern -UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="8d428-1404">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="8d428-1405">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="8d428-1405">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="8d428-1406">Lägg till stöd för resurser för NetworkWatcher ConnectionMonitor version 2</span><span class="sxs-lookup"><span data-stu-id="8d428-1406">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="8d428-1407">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="8d428-1407">Az.PolicyInsights</span></span>
* <span data-ttu-id="8d428-1408">Stöd för utvärdering av efterlevnad innan fastställande av vilken resurs som ska åtgärdas</span><span class="sxs-lookup"><span data-stu-id="8d428-1408">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="8d428-1409">Lägg till parametern ”-ResourceDiscoverMode” för Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="8d428-1409">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="8d428-1410">Lägg till cmdleten Get-AzPolicyMetadata för att hämta resurser för principmetadata</span><span class="sxs-lookup"><span data-stu-id="8d428-1410">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="8d428-1411">Get-AzPolicyState och Get-AzPolicyStateSummary för API-versionen 2019-10-01 har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="8d428-1411">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8d428-1412">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8d428-1412">Az.RecoveryServices</span></span>
* <span data-ttu-id="8d428-1413">Azure Site Recovery-stöd för att ta bort en replikerad disk.</span><span class="sxs-lookup"><span data-stu-id="8d428-1413">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="8d428-1414">Tillagt Azure Backup-stöd för att lägga till taggar när ett Recovery Services-valv skapas.</span><span class="sxs-lookup"><span data-stu-id="8d428-1414">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8d428-1415">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d428-1415">Az.Resources</span></span>
* <span data-ttu-id="8d428-1416">Gör -Scope valfritt i cmdletarna \*-AzPolicyAssignment med standardinställning till kontextprenumeration</span><span class="sxs-lookup"><span data-stu-id="8d428-1416">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="8d428-1417">Lägg till exempel på att skapa ADServicePrincipal med lösenord och nyckelautentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="8d428-1417">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="8d428-1418">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d428-1418">Az.Sql</span></span>
<span data-ttu-id="8d428-1419">Åtgärda cmdleten New-AzSqlDatabaseSecondary så att existensen PartnerDatabaseName kontrolleras i stället för existensen DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="8d428-1419">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8d428-1420">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8d428-1420">Az.Storage</span></span>
* <span data-ttu-id="8d428-1421">Stöd för angivning av krypteringsnyckeltyp för Tabell/kö i Skapa lagringskonto</span><span class="sxs-lookup"><span data-stu-id="8d428-1421">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="8d428-1422">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8d428-1422">New-AzStorageAccount</span></span>
* <span data-ttu-id="8d428-1423">Visa RequestId när StorageException inte har ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="8d428-1423">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="8d428-1424">Åtgärda exempel 6 för cmdleten Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="8d428-1424">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8d428-1425">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8d428-1425">Az.Websites</span></span>
* <span data-ttu-id="8d428-1426">Set-AzWebapp och Set-AzWebappSlot stöder egenskaperna AlwaysOn, MinTls och FtpsState</span><span class="sxs-lookup"><span data-stu-id="8d428-1426">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="8d428-1427">Åtgärdar problemet där inställning av HttpsOnly samtidigt som AppservicePlan ändrades med det enskilda kommandot Set-AzWebApp återställde HttpsOnly till standardvärdet</span><span class="sxs-lookup"><span data-stu-id="8d428-1427">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="8d428-1428">3.3.0 – januari 2020</span><span class="sxs-lookup"><span data-stu-id="8d428-1428">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8d428-1429">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8d428-1429">Az.Accounts</span></span>
* <span data-ttu-id="8d428-1430">Nu stöder Add-AzEnvironment och Set-AzEnvironment parametrarna AzureAttestationServiceEndpointResourceId och AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="8d428-1430">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="8d428-1431">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="8d428-1431">Az.Cdn</span></span>
* <span data-ttu-id="8d428-1432">Information om felsvar visas i New-AzCdnEndpoint-cmdleten</span><span class="sxs-lookup"><span data-stu-id="8d428-1432">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d428-1433">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d428-1433">Az.Compute</span></span>
* <span data-ttu-id="8d428-1434">Set-AzVMCustomScriptExtension-cmdleten har åtgärdats för en virtuell dator med hanterad OD-disk som inte har någon operativsystemprofil.</span><span class="sxs-lookup"><span data-stu-id="8d428-1434">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="8d428-1435">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="8d428-1435">Az.ContainerInstance</span></span>
* <span data-ttu-id="8d428-1436">Parameternamn som används med New-AzContainerGroup-exempel har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8d428-1436">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="8d428-1437">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="8d428-1437">Az.DataBoxEdge</span></span>
* <span data-ttu-id="8d428-1438">Cmdleten ”Get-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-1438">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="8d428-1439">Hämta gränslagringscontainern</span><span class="sxs-lookup"><span data-stu-id="8d428-1439">Get the Edge Storage Container</span></span>
* <span data-ttu-id="8d428-1440">Cmdleten ”New-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-1440">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="8d428-1441">Skapa en ny gränslagringscontainer</span><span class="sxs-lookup"><span data-stu-id="8d428-1441">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="8d428-1442">Cmdleten ”Remove-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-1442">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="8d428-1443">Ta bort gränslagringscontainern</span><span class="sxs-lookup"><span data-stu-id="8d428-1443">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="8d428-1444">Cmdleten ”Invoke-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-1444">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="8d428-1445">Anropa åtgärd för att uppdatera data i gränslagringscontainer</span><span class="sxs-lookup"><span data-stu-id="8d428-1445">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="8d428-1446">Cmdleten ”Get-AzDataBoxEdgeStorageAccount” har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-1446">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="8d428-1447">Hämta gränslagringskontot</span><span class="sxs-lookup"><span data-stu-id="8d428-1447">Get the Edge Storage Account</span></span>
* <span data-ttu-id="8d428-1448">Cmdleten ”New-AzDataBoxEdgeStorageAccount” har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-1448">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="8d428-1449">Skapa ett nytt gränslagringskonto</span><span class="sxs-lookup"><span data-stu-id="8d428-1449">Create new Edge Storage Account</span></span>
* <span data-ttu-id="8d428-1450">Cmdleten ”Remove-AzDataBoxEdgeStorageAccount” har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-1450">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="8d428-1451">Ta bort gränslagringskontot</span><span class="sxs-lookup"><span data-stu-id="8d428-1451">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="8d428-1452">Anropa cmdleten ”Invoke-AzDataBoxEdgeShare”</span><span class="sxs-lookup"><span data-stu-id="8d428-1452">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="8d428-1453">Anropa åtgärd för att uppdatera resursdata</span><span class="sxs-lookup"><span data-stu-id="8d428-1453">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="8d428-1454">Cmdleten ”Set-AzDataBoxEdgeStorageAccountCredential” har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-1454">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="8d428-1455">Ange autentiseringsuppgifter för az databoxedge-lagringskonto</span><span class="sxs-lookup"><span data-stu-id="8d428-1455">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8d428-1456">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8d428-1456">Az.DataFactory</span></span>
* <span data-ttu-id="8d428-1457">Lägg till AutoUpdateETA-, LatestVersion-, PushedVersion-, TaskQueueId- och VersionStatus-egenskaper för Get-AzDataFactoryV2IntegrationRuntime-cmd</span><span class="sxs-lookup"><span data-stu-id="8d428-1457">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="8d428-1458">Uppdatera ADF .Net SDK-versionen till 4.6.0</span><span class="sxs-lookup"><span data-stu-id="8d428-1458">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="8d428-1459">Lägg till parametern ”PublicIPs” för ”Set-AzureRmDataFactoryV2IntegrationRuntime”-cmd så att Azure-SSIS IR kan skapas med statiska offentliga IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="8d428-1459">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="8d428-1460">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="8d428-1460">Az.DevTestLabs</span></span>
* <span data-ttu-id="8d428-1461">Ta bort den brutna länken i Get-AzDtlAllowedVMSizesPolicy.md</span><span class="sxs-lookup"><span data-stu-id="8d428-1461">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="8d428-1462">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8d428-1462">Az.EventHub</span></span>
* <span data-ttu-id="8d428-1463">Korrigering av problem 10634: Åtgärda referensen till null-objekt för eventhubnamespace-borttagning</span><span class="sxs-lookup"><span data-stu-id="8d428-1463">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="8d428-1464">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8d428-1464">Az.HDInsight</span></span>
* <span data-ttu-id="8d428-1465">Åtgärda Invoke-AzHDInsightHiveJob.md-fel.</span><span class="sxs-lookup"><span data-stu-id="8d428-1465">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="8d428-1466">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="8d428-1466">Az.MachineLearning</span></span>
* <span data-ttu-id="8d428-1467">Nedanstående cmdletar har tagits bort eftersom MachineLearningCompute inte längre är tillgängligt</span><span class="sxs-lookup"><span data-stu-id="8d428-1467">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="8d428-1468">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="8d428-1468">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="8d428-1469">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="8d428-1469">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="8d428-1470">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="8d428-1470">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="8d428-1471">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="8d428-1471">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="8d428-1472">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="8d428-1472">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="8d428-1473">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="8d428-1473">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="8d428-1474">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="8d428-1474">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8d428-1475">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d428-1475">Az.Network</span></span>
* <span data-ttu-id="8d428-1476">Uppgradera beroende av Microsoft.Azure.Management.Sql från 1.36-preview till 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="8d428-1476">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8d428-1477">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8d428-1477">Az.RecoveryServices</span></span>
* <span data-ttu-id="8d428-1478">Ändrat Azure Site Recovery-stöd för krypterade vilande data på virtuella datorer med hanterade diskar med kundhanterade nycklar för Azure till Azure-providern.</span><span class="sxs-lookup"><span data-stu-id="8d428-1478">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="8d428-1479">Azure Site Recovery-stöd för att ange ID för diskkrypteringsuppsättning som valfri inmatning för aktivering av skydd för VMware till Azure.</span><span class="sxs-lookup"><span data-stu-id="8d428-1479">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="8d428-1480">Azure Site Recovery-stöd för att ange ID för diskkrypteringsuppsättning som valfri inmatning på disknivå för aktivering av skydd för VMware till Azure.</span><span class="sxs-lookup"><span data-stu-id="8d428-1480">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="8d428-1481">Azure Site Recovery-stöd för att uppdatera replikeringsskyddade objekt med mappning för diskkrypteringsuppsättning för HyperV till Azure.</span><span class="sxs-lookup"><span data-stu-id="8d428-1481">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8d428-1482">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d428-1482">Az.Resources</span></span>
* <span data-ttu-id="8d428-1483">Åtgärda ett fel i hjälpdokument för ”Remove-AzTag”.</span><span class="sxs-lookup"><span data-stu-id="8d428-1483">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="8d428-1484">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d428-1484">Az.Sql</span></span>
* <span data-ttu-id="8d428-1485">Åtgärda funktioner i cmdletar för att ange baslinjen för sårbarhetsbedömning för arbete med huvuddatabasen för Azure-databasen och begränsa den för systemdatabaser på hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="8d428-1485">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="8d428-1486">Åtgärda ett fel när en redundansgrupp för en SQL-instans skapas</span><span class="sxs-lookup"><span data-stu-id="8d428-1486">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="8d428-1487">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="8d428-1487">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="8d428-1488">Lägg till DR som en ny giltig licenstyp</span><span class="sxs-lookup"><span data-stu-id="8d428-1488">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8d428-1489">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8d428-1489">Az.Storage</span></span>
* <span data-ttu-id="8d428-1490">Lägg till varningsmeddelande om icke-bakåtkompatibel ändring för DefaultAction-värdeändring i en framtida version</span><span class="sxs-lookup"><span data-stu-id="8d428-1490">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="8d428-1491">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="8d428-1491">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="8d428-1492">Stöd för att hämta lagringskontots senaste synkroniseringstid genom att köra get-AzureRMStorageAccount med parametern -IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="8d428-1492">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="8d428-1493">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8d428-1493">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="8d428-1494">3.2.0 – December 2019</span><span class="sxs-lookup"><span data-stu-id="8d428-1494">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="8d428-1495">Allmänt</span><span class="sxs-lookup"><span data-stu-id="8d428-1495">General</span></span>
* <span data-ttu-id="8d428-1496">Uppdatera referenser i .psd1 för att använda relativa sökvägar för alla moduler</span><span class="sxs-lookup"><span data-stu-id="8d428-1496">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="8d428-1497">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8d428-1497">Az.Accounts</span></span>
* <span data-ttu-id="8d428-1498">Ange rätt UserAgent för telemetri på klientsidan för Az 4.0 preview</span><span class="sxs-lookup"><span data-stu-id="8d428-1498">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="8d428-1499">Visa användarvänligt felmeddelande när kontexten är null i Az 4.0 preview</span><span class="sxs-lookup"><span data-stu-id="8d428-1499">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="8d428-1500">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="8d428-1500">Az.Batch</span></span>
* <span data-ttu-id="8d428-1501">Korrigera problem [#10602](https://github.com/Azure/azure-powershell/issues/10602), där **New-AzBatchPool** skickade VirtualMachineConfiguration.ContainerConfiguration eller VirtualMachineConfiguration.DataDisks på ett felaktigt sätt till servern.</span><span class="sxs-lookup"><span data-stu-id="8d428-1501">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8d428-1502">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8d428-1502">Az.DataFactory</span></span>
* <span data-ttu-id="8d428-1503">Uppdatera ADF .Net SDK-versionen till 4.5.0</span><span class="sxs-lookup"><span data-stu-id="8d428-1503">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="8d428-1504">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="8d428-1504">Az.FrontDoor</span></span>
* <span data-ttu-id="8d428-1505">Stöd har lagts till för undantag för hanterade regler för brandväggen för webbaserade program</span><span class="sxs-lookup"><span data-stu-id="8d428-1505">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="8d428-1506">Lägg till SocketAddr för automatisk komplettering</span><span class="sxs-lookup"><span data-stu-id="8d428-1506">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="8d428-1507">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="8d428-1507">Az.HealthcareApis</span></span>
* <span data-ttu-id="8d428-1508">Undantagshantering</span><span class="sxs-lookup"><span data-stu-id="8d428-1508">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8d428-1509">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8d428-1509">Az.KeyVault</span></span>
* <span data-ttu-id="8d428-1510">Åtgärdat fel vid åtkomst av värde som kanske inte har angetts</span><span class="sxs-lookup"><span data-stu-id="8d428-1510">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="8d428-1511">Hantering av ECC-certifikat (Elliptic Curve Cryptography)</span><span class="sxs-lookup"><span data-stu-id="8d428-1511">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="8d428-1512">Stöd har lagts till för att ange kurvan för certifikatprinciper</span><span class="sxs-lookup"><span data-stu-id="8d428-1512">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8d428-1513">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8d428-1513">Az.Monitor</span></span>
* <span data-ttu-id="8d428-1514">Lägger till valfritt argument i kommandot Lägg till diagnostikinställningar.</span><span class="sxs-lookup"><span data-stu-id="8d428-1514">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="8d428-1515">Ett växelargument som om det finns visar att exporten till Log Analytics måste ske till ett fast schema (kallas även</span><span class="sxs-lookup"><span data-stu-id="8d428-1515">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="8d428-1516">dedikerad, datatyp)</span><span class="sxs-lookup"><span data-stu-id="8d428-1516">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8d428-1517">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d428-1517">Az.Network</span></span>
* <span data-ttu-id="8d428-1518">Stöd för IpGroups i program-, NAT- och nätverksregler för Azure Firewall.</span><span class="sxs-lookup"><span data-stu-id="8d428-1518">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8d428-1519">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d428-1519">Az.Resources</span></span>
* <span data-ttu-id="8d428-1520">Åtgärda ett problem där malldistributionen inte kan läsa en mallparameter om dess namn står i konflikt med ett inbyggt parameternamn.</span><span class="sxs-lookup"><span data-stu-id="8d428-1520">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="8d428-1521">Uppdaterade princip-cmdletar för att använda den nya API-versionen 2019-09-01 som introducerar grupperingsstöd inom principuppsättningsdefinitioner.</span><span class="sxs-lookup"><span data-stu-id="8d428-1521">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="8d428-1522">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d428-1522">Az.Sql</span></span>
* <span data-ttu-id="8d428-1523">Uppgraderad funktion för att skapa lagring i automatisk aktivering av sårbarhetsbedömning till StorageV2</span><span class="sxs-lookup"><span data-stu-id="8d428-1523">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8d428-1524">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8d428-1524">Az.Storage</span></span>
* <span data-ttu-id="8d428-1525">Stöd för generering av blob/container-identitetsbaserad SAS-token med lagringskontextbaserad på OAuth-autentisering</span><span class="sxs-lookup"><span data-stu-id="8d428-1525">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="8d428-1526">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="8d428-1526">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="8d428-1527">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="8d428-1527">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="8d428-1528">Stöd för återkallning av användardelegeringsnycklar för lagringskonto för att återkalla alla SAS-token</span><span class="sxs-lookup"><span data-stu-id="8d428-1528">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="8d428-1529">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="8d428-1529">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="8d428-1530">Uppgradera till Microsoft.Azure.Management.Storage 14.2.0 för att stödja den nya API-versionen 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="8d428-1530">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="8d428-1531">Stöd för QuotaGiB (resurskvot i Gibibye) för värden över 5120 i hanteringsplanet för cmdletar för filresurser och parameteraliaset. Quota har också lagts till för parametern ”QuotaGiB”.</span><span class="sxs-lookup"><span data-stu-id="8d428-1531">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="8d428-1532">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="8d428-1532">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="8d428-1533">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="8d428-1533">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="8d428-1534">Lägg till parameteraliaset QuotaGiB i parametern Quota</span><span class="sxs-lookup"><span data-stu-id="8d428-1534">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="8d428-1535">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="8d428-1535">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="8d428-1536">Åtgärda problemet att Set-AzStorageContainerAcl kan rensa den lagrade åtkomstprincipen</span><span class="sxs-lookup"><span data-stu-id="8d428-1536">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="8d428-1537">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="8d428-1537">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="8d428-1538">3.1.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="8d428-1538">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="8d428-1539">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="8d428-1539">Highlights since the last major release</span></span>
* <span data-ttu-id="8d428-1540">Az.DataBoxEdge 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="8d428-1540">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="8d428-1541">Az.SqlVirtualMachine 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="8d428-1541">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d428-1542">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d428-1542">Az.Compute</span></span>
* <span data-ttu-id="8d428-1543">Funktion för att använda en virtuell dator igen</span><span class="sxs-lookup"><span data-stu-id="8d428-1543">VM Reapply feature</span></span>
    - <span data-ttu-id="8d428-1544">Lägg till parameter för att använda igen till cmdleten Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="8d428-1544">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="8d428-1545">Funktionen AutomaticRepairs i VM-skalningsuppsättningar:</span><span class="sxs-lookup"><span data-stu-id="8d428-1545">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="8d428-1546">Lägg till parametrarna EnableAutomaticRepair, AutomaticRepairGracePeriod och AutomaticRepairMaxInstanceRepairsPercent till följande cmdletar:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8d428-1546">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="8d428-1547">Stöd för galleriavbildningar i flera klientorganisationer för New-AzVM</span><span class="sxs-lookup"><span data-stu-id="8d428-1547">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="8d428-1548">Lägg till "Spot" till argumentslutföraren i prioritetsparametern i cmdletarna New-AzVM, New-AzVMConfig och New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8d428-1548">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="8d428-1549">Lägg till parametrarna DiskIOPSReadWrite och DiskMBpsReadWrite till cmdleten Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="8d428-1549">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="8d428-1550">Ändra parametern SourceImageId för cmdleten New-AzGalleryImageVersion till valfri</span><span class="sxs-lookup"><span data-stu-id="8d428-1550">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="8d428-1551">Lägg till parametrarna OSDiskImage och DataDiskImage till cmdleten New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="8d428-1551">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="8d428-1552">Lägg till parametern HyperVGeneration till cmdleten New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="8d428-1552">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="8d428-1553">Lägg till parametern SkipExtensionsOnOverprovisionedVMs till cmdletarna New-AzVmss, New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8d428-1553">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="8d428-1554">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="8d428-1554">Az.DataBoxEdge</span></span>
* <span data-ttu-id="8d428-1555">Cmdleten `Get-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-1555">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="8d428-1556">Hämta ordning</span><span class="sxs-lookup"><span data-stu-id="8d428-1556">Get the Order</span></span>
* <span data-ttu-id="8d428-1557">Cmdleten `New-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-1557">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="8d428-1558">Skapa ny ordning</span><span class="sxs-lookup"><span data-stu-id="8d428-1558">Create new Order</span></span>
* <span data-ttu-id="8d428-1559">Cmdleten `Remove-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-1559">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="8d428-1560">Ta bort ordning</span><span class="sxs-lookup"><span data-stu-id="8d428-1560">Remove the Order</span></span>
* <span data-ttu-id="8d428-1561">Cmdleten `New-AzDataBoxEdgeShare` har ändrats</span><span class="sxs-lookup"><span data-stu-id="8d428-1561">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="8d428-1562">Nu skapas lokal filresurs</span><span class="sxs-lookup"><span data-stu-id="8d428-1562">Now creates Local Share</span></span>
* <span data-ttu-id="8d428-1563">Cmdleten `Set-AzDataBoxEdgeRole` har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-1563">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="8d428-1564">Nu kan IotRole mappas till filresursen</span><span class="sxs-lookup"><span data-stu-id="8d428-1564">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="8d428-1565">Cmdleten `Invoke-AzDataBoxEdgeDevice` har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-1565">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="8d428-1566">Anropa genomsökningsuppdatering, ladda ned uppdatering, installera uppdateringar på enheten</span><span class="sxs-lookup"><span data-stu-id="8d428-1566">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="8d428-1567">Cmdleten `Get-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-1567">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="8d428-1568">Hämtar information om utlösare</span><span class="sxs-lookup"><span data-stu-id="8d428-1568">Gets the information about Triggers</span></span>
* <span data-ttu-id="8d428-1569">Cmdleten `New-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-1569">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="8d428-1570">Skapa nya utlösare</span><span class="sxs-lookup"><span data-stu-id="8d428-1570">Create new Triggers</span></span>
* <span data-ttu-id="8d428-1571">Cmdleten `Remove-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-1571">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="8d428-1572">Ta bort utlösare</span><span class="sxs-lookup"><span data-stu-id="8d428-1572">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8d428-1573">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8d428-1573">Az.DataFactory</span></span>
* <span data-ttu-id="8d428-1574">Uppdatera ADF .Net SDK-versionen till 4.4.0</span><span class="sxs-lookup"><span data-stu-id="8d428-1574">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="8d428-1575">Lägg till parametern ExpressCustomSetup för kommandot Set-AzureRmDataFactoryV2IntegrationRuntime för att aktivera installationskonfigurationer och komponenter från tredje part utan anpassat konfigurationsskript.</span><span class="sxs-lookup"><span data-stu-id="8d428-1575">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8d428-1576">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8d428-1576">Az.DataLakeStore</span></span>
* <span data-ttu-id="8d428-1577">Uppdatera dokumentation för Get-AzDataLakeStoreDeletedItem och Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="8d428-1577">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="8d428-1578">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8d428-1578">Az.EventHub</span></span>
* <span data-ttu-id="8d428-1579">Korrigering av problem #10301: Korrigera datumformat för SAS-token</span><span class="sxs-lookup"><span data-stu-id="8d428-1579">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="8d428-1580">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="8d428-1580">Az.FrontDoor</span></span>
* <span data-ttu-id="8d428-1581">Lägg till parametern MinimumTlsVersion till Enable-AzFrontDoorCustomDomainHttps och New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="8d428-1581">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="8d428-1582">Lägg till parametrarna HealthProbeMethod och EnabledState till New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="8d428-1582">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="8d428-1583">Lägg till en ny cmdlet för att skapa BackendPoolsSettings-objekt som passar i skapande/uppdatering av Front Door</span><span class="sxs-lookup"><span data-stu-id="8d428-1583">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="8d428-1584">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="8d428-1584">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8d428-1585">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d428-1585">Az.Network</span></span>
* <span data-ttu-id="8d428-1586">Ändra alternativexemplen Start-AzVirtualNetworkGatewayConnectionPacketCapture.md och Start-AzVirtualnetworkGatewayPacketCapture.md för FilterData.</span><span class="sxs-lookup"><span data-stu-id="8d428-1586">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="8d428-1587">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="8d428-1587">Az.PrivateDns</span></span>
* <span data-ttu-id="8d428-1588">Uppdaterade PrivateDns .NET SDK till version 1.0.0</span><span class="sxs-lookup"><span data-stu-id="8d428-1588">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8d428-1589">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8d428-1589">Az.RecoveryServices</span></span>
* <span data-ttu-id="8d428-1590">Stöd för att välja disktyp vid aktivering av skydd i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="8d428-1590">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="8d428-1591">Korrigering av bugg för åtgärdsredigering av återställningsplan i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="8d428-1591">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="8d428-1592">Återställningsstöd för att godkänna filestream-databaser i Azure Backup SQL.</span><span class="sxs-lookup"><span data-stu-id="8d428-1592">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="8d428-1593">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="8d428-1593">Az.RedisCache</span></span>
* <span data-ttu-id="8d428-1594">Parametern MinimumTlsVersion har lagts till i cmdletarna New-AzRedisCache och Set-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="8d428-1594">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="8d428-1595">Dessutom har MinimumTlsVersion lagts till i utdata för cmdleten Get-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="8d428-1595">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="8d428-1596">Verifiering har lagts till på parametern -Size i cmdletarna Set-AzRedisCache och New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="8d428-1596">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="8d428-1597">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d428-1597">Az.Resources</span></span>
- <span data-ttu-id="8d428-1598">Uppdaterade policy-cmdletar för att använda den nya API-versionen 2019-06-01 som har en ny EnforcementMode-egenskap i policytilldelningen.</span><span class="sxs-lookup"><span data-stu-id="8d428-1598">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="8d428-1599">Uppdaterade hjälpexempel för skapandet av policydefinition</span><span class="sxs-lookup"><span data-stu-id="8d428-1599">Updated create policy definition help example</span></span>
- <span data-ttu-id="8d428-1600">Åtgärda bugg i Remove-AZADServicePrincipal -ServicePrincipalName, utlös null-referens när tjänstens huvudnamn inte hittas.</span><span class="sxs-lookup"><span data-stu-id="8d428-1600">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="8d428-1601">Åtgärda bugg i New-AZADServicePrincipal, utlös null-referens när klientorganisationen inte har någon prenumeration.</span><span class="sxs-lookup"><span data-stu-id="8d428-1601">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="8d428-1602">Ändra New-AzAdServicePrincipal för att endast lägga till autentiseringsuppgifter för det associerade programmet.</span><span class="sxs-lookup"><span data-stu-id="8d428-1602">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="8d428-1603">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d428-1603">Az.Sql</span></span>
* <span data-ttu-id="8d428-1604">Stöd har lagts till för databasen ReadReplicaCount.</span><span class="sxs-lookup"><span data-stu-id="8d428-1604">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="8d428-1605">Korrigerade Set-AzSqlDatabase när zonredundans inte har angetts</span><span class="sxs-lookup"><span data-stu-id="8d428-1605">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="8d428-1606">3.0.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="8d428-1606">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="8d428-1607">Allmänt</span><span class="sxs-lookup"><span data-stu-id="8d428-1607">General</span></span>
* <span data-ttu-id="8d428-1608">Az. PrivateDns 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="8d428-1608">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="8d428-1609">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8d428-1609">Az.Accounts</span></span>
* <span data-ttu-id="8d428-1610">Lägg till ett utfasningsmeddelande för aliaset Resolve-error.</span><span class="sxs-lookup"><span data-stu-id="8d428-1610">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="8d428-1611">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="8d428-1611">Az.Advisor</span></span>
* <span data-ttu-id="8d428-1612">Den nya kategorin Operational Excellence har lagts till i cmdleten Get-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="8d428-1612">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="8d428-1613">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="8d428-1613">Az.Batch</span></span>
* <span data-ttu-id="8d428-1614">`CoreQuota` på `BatchAccountContext` har bytt namn till `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="8d428-1614">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="8d428-1615">Det finns även en ny `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="8d428-1615">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="8d428-1616">Detta påverkar **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="8d428-1616">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="8d428-1617">**New-AzBatchTask** `-ResourceFile`-parametern tar nu en samling `PSResourceFile`-objekt som kan skapas med hjälp av den nya cmdleten **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="8d428-1617">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="8d428-1618">Ny **New-AzBatchResourceFile** -cmdlet för att skapa `PSResourceFile`-objekt.</span><span class="sxs-lookup"><span data-stu-id="8d428-1618">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="8d428-1619">Dessa kan tillhandahållas till **New-AzBatchTask** på `-ResourceFile`-parametern.</span><span class="sxs-lookup"><span data-stu-id="8d428-1619">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="8d428-1620">Detta stöder två nya typer av resursfiler förutom det befintliga sättet med `HttpUrl`:</span><span class="sxs-lookup"><span data-stu-id="8d428-1620">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="8d428-1621">`AutoStorageContainerName`-baserade resursfiler laddar ned en hel container för automatisk lagring till Batch-noden.</span><span class="sxs-lookup"><span data-stu-id="8d428-1621">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="8d428-1622">`StorageContainerUrl`-baserade resursfiler laddar ned containern som anges i webbadressen till Batch-noden.</span><span class="sxs-lookup"><span data-stu-id="8d428-1622">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="8d428-1623">Tog bort egenskapen `ApplicationPackages` för `PSApplication` som returnerades av **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="8d428-1623">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="8d428-1624">Specifika paket i ett program kan nu hämtas med hjälp av **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="8d428-1624">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="8d428-1625">Till exempel: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="8d428-1625">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="8d428-1626">Bytt namn på `ApplicationId` till `ApplicationName` på **Get-AzBatchApplicationPackage** , **New-AzBatchApplicationPackage** , **Remove-AzBatchApplicationPackage** , **Get-AzBatchApplication** , **New-AzBatchApplication** , **Remove-AzBatchApplication** och **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="8d428-1626">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage** , **New-AzBatchApplicationPackage** , **Remove-AzBatchApplicationPackage** , **Get-AzBatchApplication** , **New-AzBatchApplication** , **Remove-AzBatchApplication** , and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="8d428-1627">`ApplicationId` är nu ett alias för `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="8d428-1627">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="8d428-1628">Ny `PSWindowsUserConfiguration`-egenskap till `PSUserAccount` lades till.</span><span class="sxs-lookup"><span data-stu-id="8d428-1628">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="8d428-1629">Bytte namn på `Version` till `Name` på `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="8d428-1629">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="8d428-1630">Bytte namn på `BlobSource` till `HttpUrl` på `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="8d428-1630">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="8d428-1631">Tog bort egenskapen `OSDisk` från `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="8d428-1631">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="8d428-1632">Tog bort **Set-AzBatchPoolOSVersion**.</span><span class="sxs-lookup"><span data-stu-id="8d428-1632">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="8d428-1633">Den här åtgärden stöds inte längre.</span><span class="sxs-lookup"><span data-stu-id="8d428-1633">This operation is no longer supported.</span></span>
* <span data-ttu-id="8d428-1634">`TargetOSVersion` har tagits bort från `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="8d428-1634">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="8d428-1635">Bytte namn på `CurrentOSVersion` till `OSVersion` på `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="8d428-1635">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="8d428-1636">`DataEgressGiB` och `DataIngressGiB` har tagits bort från `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="8d428-1636">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="8d428-1637">Tog bort **Get-AzBatchNodeAgentSku** och ersatte det med **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="8d428-1637">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="8d428-1638">**Get-AzBatchSupportedImage** returnerar samma data som **Get-AzBatchNodeAgentSku** men i ett mer användarvänligt format.</span><span class="sxs-lookup"><span data-stu-id="8d428-1638">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="8d428-1639">Nya icke-verifierade avbildningar returneras nu också.</span><span class="sxs-lookup"><span data-stu-id="8d428-1639">New non-verified images are also now returned.</span></span> <span data-ttu-id="8d428-1640">Ytterligare information om `Capabilities` och `BatchSupportEndOfLife` för varje avbildning inkluderas också.</span><span class="sxs-lookup"><span data-stu-id="8d428-1640">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="8d428-1641">Lade till möjlighet att montera fjärrfilsystem på varje nod i en pool via den nya parametern `MountConfiguration` för **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="8d428-1641">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="8d428-1642">Har nu stöd för nätverkssäkerhetsregler som blockerar nätverksåtkomst till en pool baserat på källportens trafik.</span><span class="sxs-lookup"><span data-stu-id="8d428-1642">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="8d428-1643">Detta görs via egenskapen `SourcePortRanges` på `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="8d428-1643">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="8d428-1644">När du kör en container stöder nu Batch körningen av uppgiften i arbetskatalogen för containern eller i arbetskatalogen för Batch-uppgiften.</span><span class="sxs-lookup"><span data-stu-id="8d428-1644">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="8d428-1645">Detta styrs av egenskapen `WorkingDirectory` på `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="8d428-1645">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="8d428-1646">Lade till en funktion för att ange en samling av offentliga IP-adresser på `PSNetworkConfiguration` via den nya egenskapen `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="8d428-1646">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="8d428-1647">Detta garanterar att noderna i poolen har en IP-adress från listan över IP-adresser som tillhandahållits av användare.</span><span class="sxs-lookup"><span data-stu-id="8d428-1647">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="8d428-1648">Om inget värde anges är standardvärdet för `WaitForSuccess` på `PSSTartTask` nu `$True` (var tidigare `$False`).</span><span class="sxs-lookup"><span data-stu-id="8d428-1648">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="8d428-1649">Om inget värde anges är standardvärdet för `Scope` på `PSAutoUserSpecification` nu `Pool` (var tidigare `Task` på Windows och `Pool` på Linux).</span><span class="sxs-lookup"><span data-stu-id="8d428-1649">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="8d428-1650">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="8d428-1650">Az.Cdn</span></span>
* <span data-ttu-id="8d428-1651">Introducerade UrlRewriteAction och CacheKeyQueryStringAction till RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="8d428-1651">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="8d428-1652">Åtgärdade flera buggar, som saknade indata för ”väljare” i cmdleten New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="8d428-1652">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d428-1653">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d428-1653">Az.Compute</span></span>
* <span data-ttu-id="8d428-1654">Funktion för diskkrypteringsuppsättning</span><span class="sxs-lookup"><span data-stu-id="8d428-1654">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="8d428-1655">Nya cmdletar:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="8d428-1655">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="8d428-1656">Parametern DiskEncryptionSetId har lagts till i följande cmdletar:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="8d428-1656">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="8d428-1657">Parametrarna DiskEncryptionSetId och EncryptionType har lagts till i följande cmdletar:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="8d428-1657">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="8d428-1658">Lägg till parametern PublicIPAddressVersion i New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="8d428-1658">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="8d428-1659">Flytta FileUris för anpassat skripttillägg från offentlig inställning till skyddad inställning</span><span class="sxs-lookup"><span data-stu-id="8d428-1659">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="8d428-1660">Lägg till ScaleInPolicy i cmdletarna New-AzVmss, New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8d428-1660">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="8d428-1661">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="8d428-1661">Breaking changes</span></span>
    - <span data-ttu-id="8d428-1662">Parametern UploadSizeInBytes används istället för DiskSizeGB för New-AzDiskConfig när CreateOption är Uppladdning</span><span class="sxs-lookup"><span data-stu-id="8d428-1662">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="8d428-1663">PublishingProfile.Source.ManagedImage.Id ersätts med StorageProfile.Source.Id i objektet GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="8d428-1663">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8d428-1664">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8d428-1664">Az.DataFactory</span></span>
* <span data-ttu-id="8d428-1665">Uppdatera ADF .Net SDK-versionen till 4.3.0</span><span class="sxs-lookup"><span data-stu-id="8d428-1665">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8d428-1666">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8d428-1666">Az.DataLakeStore</span></span>
* <span data-ttu-id="8d428-1667">Uppdatera ADLS SDK-version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) innehåller följande korrigeringar</span><span class="sxs-lookup"><span data-stu-id="8d428-1667">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="8d428-1668">Undvik att utlösa undantag när det inte går att deserialisera creationtime för inmatning av papperskorg eller katalog.</span><span class="sxs-lookup"><span data-stu-id="8d428-1668">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="8d428-1669">Gör inställning tillgänglig per tidsgräns för förfrågan i adlsclient</span><span class="sxs-lookup"><span data-stu-id="8d428-1669">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="8d428-1670">Korrigera överföringen av ursprunglig syncflag för badoffset-återställning</span><span class="sxs-lookup"><span data-stu-id="8d428-1670">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="8d428-1671">Korrigera EnumerateDirectory för att hämta fortsättningstoken när svar har kontrollerats</span><span class="sxs-lookup"><span data-stu-id="8d428-1671">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="8d428-1672">Korrigera bugg i Concat</span><span class="sxs-lookup"><span data-stu-id="8d428-1672">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="8d428-1673">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="8d428-1673">Az.FrontDoor</span></span>
* <span data-ttu-id="8d428-1674">Åtgärdade diverse stavfel i modul</span><span class="sxs-lookup"><span data-stu-id="8d428-1674">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="8d428-1675">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8d428-1675">Az.HDInsight</span></span>
* <span data-ttu-id="8d428-1676">Korrigerade buggen att kunder får felet ”inte en giltig Base-64-sträng” vid användning av Get-AzHDInsightCluster för att hämta klustret med ADLSGen1-lagring.</span><span class="sxs-lookup"><span data-stu-id="8d428-1676">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="8d428-1677">Lägg till en parameter med namnet ”ApplicationId” i de tre cmdletarna Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig och New-AzHDInsightCluster så att kunden kan tillhandahålla tjänstens huvudnamn för program-ID för åtkomst till Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="8d428-1677">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="8d428-1678">Ändrade Microsoft.Azure.Management.HDInsight från 2.1.0 till 5.1.0</span><span class="sxs-lookup"><span data-stu-id="8d428-1678">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="8d428-1679">Fem cmdletar har tagits bort:</span><span class="sxs-lookup"><span data-stu-id="8d428-1679">Removed five cmdlets:</span></span>
    - <span data-ttu-id="8d428-1680">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="8d428-1680">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="8d428-1681">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="8d428-1681">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="8d428-1682">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="8d428-1682">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="8d428-1683">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="8d428-1683">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="8d428-1684">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="8d428-1684">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="8d428-1685">Tre cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="8d428-1685">Added three cmdlets:</span></span>
    - <span data-ttu-id="8d428-1686">Get-AzHDInsightMonitoring som ersätter Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="8d428-1686">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="8d428-1687">Enable-AzHDInsightMonitoring som ersätter Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="8d428-1687">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="8d428-1688">Disable-AzHDInsightMonitoring som ersätter Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="8d428-1688">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="8d428-1689">Korrigerade cmdleten Get-AzHDInsightProperties för att stödja hämtning av funktionsinformation från en viss plats.</span><span class="sxs-lookup"><span data-stu-id="8d428-1689">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="8d428-1690">Parameteruppsättningarna (Spark1 och Spark2) har tagits bort från Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="8d428-1690">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="8d428-1691">Lägg till exempel för cmdleten Add-AzHDInsightSecurityProfile till hjälpdokumenten.</span><span class="sxs-lookup"><span data-stu-id="8d428-1691">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="8d428-1692">Ändrade utdatatyp för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="8d428-1692">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="8d428-1693">Ändrade utdatatyp för Get-AzHDInsightProperties från CapabilitiesResponse till AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="8d428-1693">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="8d428-1694">Ändrade utdatatyp för Remove-AzHDInsightCluster från ClusterGetResponse till bool.</span><span class="sxs-lookup"><span data-stu-id="8d428-1694">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="8d428-1695">Ändrade utdatatyp för Set-AzHDInsightGatewaySettings HttpConnectivitySettings till GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="8d428-1695">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="8d428-1696">Lade till testfall för vissa scenarier.</span><span class="sxs-lookup"><span data-stu-id="8d428-1696">Added some scenario test cases.</span></span>
* <span data-ttu-id="8d428-1697">Ta bort vissa alias: Add-AzHDInsightConfigValues, Get-AzHDInsightProperties.</span><span class="sxs-lookup"><span data-stu-id="8d428-1697">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8d428-1698">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8d428-1698">Az.IotHub</span></span>
* <span data-ttu-id="8d428-1699">Icke-bakåtkompatibla ändringar:</span><span class="sxs-lookup"><span data-stu-id="8d428-1699">Breaking changes:</span></span>
    - <span data-ttu-id="8d428-1700">Cmdleten Add-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="8d428-1700">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="8d428-1701">Parameteruppsättningen __AllParameterSets för cmdleten Add-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="8d428-1701">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="8d428-1702">Cmdleten Get-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="8d428-1702">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="8d428-1703">Parameteruppsättningen __AllParameterSets för cmdleten Get-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="8d428-1703">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="8d428-1704">Egenskapen OperationsMonitoringProperties av typen Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="8d428-1704">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="8d428-1705">Egenskapen OperationsMonitoringProperties av typen Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="8d428-1705">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="8d428-1706">Cmdleten New-AzIotHubExportDevice stöder inte längre aliaset New-AzIotHubExportDevices.</span><span class="sxs-lookup"><span data-stu-id="8d428-1706">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="8d428-1707">Cmdleten New-AzIotHubImportDevice stöder inte längre aliaset New-AzIotHubImportDevices.</span><span class="sxs-lookup"><span data-stu-id="8d428-1707">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="8d428-1708">Cmdleten Remove-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="8d428-1708">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="8d428-1709">Parameteruppsättningen __AllParameterSets för cmdleten Remove-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="8d428-1709">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="8d428-1710">Cmdleten Set-AzIotHub har inte längre stöd för parametern OperationsMonitoringProperties och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="8d428-1710">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="8d428-1711">Parameteruppsättningen UpdateOperationsMonitoringProperties för cmdleten Set-AzIotHub har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="8d428-1711">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8d428-1712">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8d428-1712">Az.RecoveryServices</span></span>
* <span data-ttu-id="8d428-1713">Azure Site Recovery-stöd för att konfigurera nätverksresurser som NSG, offentliga IP-adresser och interna lastbalanserare för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="8d428-1713">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="8d428-1714">Azure Site Recovery-stöd för att skriva till hanterad disk för vMWare till Azure.</span><span class="sxs-lookup"><span data-stu-id="8d428-1714">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="8d428-1715">Azure Site Recovery-stöd för NIC-reduktion för vMWare till Azure.</span><span class="sxs-lookup"><span data-stu-id="8d428-1715">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="8d428-1716">Azure Site Recovery-stöd för accelererat nätverk för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="8d428-1716">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="8d428-1717">Azure Site Recovery-stöd för automatisk uppdatering av agent för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="8d428-1717">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="8d428-1718">Azure Site Recovery-stöd för Standard SSD för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="8d428-1718">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="8d428-1719">Azure Site Recovery-stöd för tvåstegskryptering i Azure Disk Encryption för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="8d428-1719">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="8d428-1720">Azure Site Recovery-stöd för att skydda nyligen tillagda diskar för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="8d428-1720">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="8d428-1721">En funktion för mjuk borttagning av virtuella datorer samt tester för mjuk borttagning har tagits bort</span><span class="sxs-lookup"><span data-stu-id="8d428-1721">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="8d428-1722">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d428-1722">Az.Resources</span></span>
* <span data-ttu-id="8d428-1723">Uppdatera beroendesammansättning för Microsoft.Extensions.Caching.Memory från 1.1.1 till 2.2</span><span class="sxs-lookup"><span data-stu-id="8d428-1723">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8d428-1724">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d428-1724">Az.Network</span></span>
* <span data-ttu-id="8d428-1725">Ändra alla cmdletar för PrivateEndpointConnection så att de stöder generiska tjänstleverantörer.</span><span class="sxs-lookup"><span data-stu-id="8d428-1725">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="8d428-1726">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="8d428-1726">Updated cmdlet:</span></span>
        - <span data-ttu-id="8d428-1727">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8d428-1727">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="8d428-1728">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8d428-1728">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="8d428-1729">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8d428-1729">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="8d428-1730">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8d428-1730">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="8d428-1731">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8d428-1731">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="8d428-1732">Lägg till ny cmdlet för PrivateLinkResource så att det också stöder generiska tjänstleverantörer.</span><span class="sxs-lookup"><span data-stu-id="8d428-1732">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="8d428-1733">Ny cmdlet:</span><span class="sxs-lookup"><span data-stu-id="8d428-1733">New cmdlet:</span></span>
        - <span data-ttu-id="8d428-1734">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="8d428-1734">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="8d428-1735">Lägg till nya fält och parametrar för funktionen Proxy Protocol V2.</span><span class="sxs-lookup"><span data-stu-id="8d428-1735">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="8d428-1736">Lägg till egenskapen EnableProxyProtocol i PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="8d428-1736">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="8d428-1737">Lägg till egenskapen LinkIdentifier i PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8d428-1737">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="8d428-1738">Uppdaterade New-AzPrivateLinkService för att lägga till den nya valfria parametern EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="8d428-1738">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="8d428-1739">Korrigera felaktig beskrivning av parameter i referensdokumentationen för New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="8d428-1739">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="8d428-1740">Nya cmdletar som stöder Azure-brandväggsprincipen</span><span class="sxs-lookup"><span data-stu-id="8d428-1740">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="8d428-1741">Lägg till stöd för den underordnade resursen RouteTables för VirtualHub</span><span class="sxs-lookup"><span data-stu-id="8d428-1741">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="8d428-1742">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="8d428-1742">New cmdlets added:</span></span>
        - <span data-ttu-id="8d428-1743">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="8d428-1743">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="8d428-1744">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="8d428-1744">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="8d428-1745">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="8d428-1745">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="8d428-1746">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="8d428-1746">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="8d428-1747">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="8d428-1747">Set-AzVirtualHub</span></span>
* <span data-ttu-id="8d428-1748">Lägg till stöd för ny egenskaps-SKU för VirtualHub och VirtualWANType för VirtualWan</span><span class="sxs-lookup"><span data-stu-id="8d428-1748">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="8d428-1749">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="8d428-1749">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="8d428-1750">New-AzVirtualHub: lade till parameter-SKU</span><span class="sxs-lookup"><span data-stu-id="8d428-1750">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="8d428-1751">Update-AzVirtualHub: lade till parameter-SKU</span><span class="sxs-lookup"><span data-stu-id="8d428-1751">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="8d428-1752">New-AzVirtualWan: lade till parametern VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="8d428-1752">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="8d428-1753">Update-AzVirtualWan: lade till parametern VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="8d428-1753">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="8d428-1754">Lägg till stöd för egenskapen EnableInternetSecurity för HubVnetConnection, VpnConnection och ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="8d428-1754">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="8d428-1755">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="8d428-1755">New cmdlets added:</span></span>
        - <span data-ttu-id="8d428-1756">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="8d428-1756">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="8d428-1757">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="8d428-1757">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="8d428-1758">New-AzureRmVirtualHubVnetConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-1758">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="8d428-1759">New-AzureRmVpnConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-1759">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="8d428-1760">Update-AzureRmVpnConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-1760">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="8d428-1761">New-AzureRmExpressRouteConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-1761">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="8d428-1762">Set-AzureRmExpressRouteConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-1762">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="8d428-1763">Lägg till stöd för att konfigurera TopLevel WebApplicationFirewall-princip</span><span class="sxs-lookup"><span data-stu-id="8d428-1763">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="8d428-1764">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="8d428-1764">New cmdlets added:</span></span>
        - <span data-ttu-id="8d428-1765">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="8d428-1765">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="8d428-1766">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="8d428-1766">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="8d428-1767">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="8d428-1767">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="8d428-1768">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="8d428-1768">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="8d428-1769">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="8d428-1769">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="8d428-1770">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="8d428-1770">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="8d428-1771">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="8d428-1771">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="8d428-1772">New-AzApplicationGatewayFirewallPolicy: parametrarna PolicySetting, ManagedRule har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-1772">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="8d428-1773">Stöd för operator för geomatchning har lagts till på CustomRule</span><span class="sxs-lookup"><span data-stu-id="8d428-1773">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="8d428-1774">Geomatchning har lagts till i operatorn på FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="8d428-1774">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="8d428-1775">Stöd har lagts till för brandväggsprinciperna perListener och perSite</span><span class="sxs-lookup"><span data-stu-id="8d428-1775">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="8d428-1776">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="8d428-1776">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="8d428-1777">New-AzApplicationGatewayHttpListener: parametrarna FirewallPolicy, FirewallPolicyId har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-1777">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="8d428-1778">New-AzApplicationGatewayPathRuleConfig: parametrarna FirewallPolicy, FirewallPolicyId har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-1778">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="8d428-1779">Åtgärdat så att nödvändigt undernät med namnet AzureBastionSubnet i PSBastion kan vara skiftlägesokänsligt</span><span class="sxs-lookup"><span data-stu-id="8d428-1779">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="8d428-1780">Stöd för mål-FQDN:er i nätverksregler och översatt FQDN i NAT-regler för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="8d428-1780">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="8d428-1781">Lägg till stöd för resursen RouteTables för IpGroup på den högsta nivån</span><span class="sxs-lookup"><span data-stu-id="8d428-1781">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="8d428-1782">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="8d428-1782">New cmdlets added:</span></span>
        - <span data-ttu-id="8d428-1783">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="8d428-1783">New-AzIpGroup</span></span>
        - <span data-ttu-id="8d428-1784">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="8d428-1784">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="8d428-1785">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="8d428-1785">Get-AzIpGroup</span></span>
        - <span data-ttu-id="8d428-1786">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="8d428-1786">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8d428-1787">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8d428-1787">Az.ServiceFabric</span></span>
* <span data-ttu-id="8d428-1788">Ta bort cmdleten Add-AzServiceFabricApplicationCertificate eftersom det här scenariot omfattas av Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="8d428-1788">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="8d428-1789">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d428-1789">Az.Sql</span></span>
* <span data-ttu-id="8d428-1790">Stöd har lagts till för återställning av utelämnade databaser på hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="8d428-1790">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="8d428-1791">Inaktuella gamla cmdletar för granskning från kod.</span><span class="sxs-lookup"><span data-stu-id="8d428-1791">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="8d428-1792">Tog bort inaktuella alias:</span><span class="sxs-lookup"><span data-stu-id="8d428-1792">Removed deprecated aliases:</span></span>
* <span data-ttu-id="8d428-1793">Get-AzSqlDatabaseIndexRecommendations (använd Get-AzSqlDatabaseIndexRecommendation istället)</span><span class="sxs-lookup"><span data-stu-id="8d428-1793">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="8d428-1794">Get-AzSqlDatabaseRestorePoints (använd Get-AzSqlDatabaseRestorePoint istället)</span><span class="sxs-lookup"><span data-stu-id="8d428-1794">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="8d428-1795">Ta bort cmdleten Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="8d428-1795">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="8d428-1796">Ta bort alias för inaktuella cmdletar för inställningar för utvärdering av säkerhetsrisk</span><span class="sxs-lookup"><span data-stu-id="8d428-1796">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="8d428-1797">Inaktualisera cmdletar för inställningar för avancerad hotidentifiering</span><span class="sxs-lookup"><span data-stu-id="8d428-1797">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="8d428-1798">Lägga till cmdletar för att inaktivera och aktivera känslighetsrekommendationer på kolumner i en databas.</span><span class="sxs-lookup"><span data-stu-id="8d428-1798">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8d428-1799">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8d428-1799">Az.Storage</span></span>
* <span data-ttu-id="8d428-1800">Stöd för att aktivera stora filresurser vid skapande eller uppdatering av lagringskonto</span><span class="sxs-lookup"><span data-stu-id="8d428-1800">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="8d428-1801">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8d428-1801">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="8d428-1802">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8d428-1802">Set-AzStorageAccount</span></span>
* <span data-ttu-id="8d428-1803">När du stänger/hämtar en filreferens kan du hoppa över kontrollen av huruvida indatasökvägen är en filkatalog eller en fil för att undvika problem med objekt som har status DeletePending</span><span class="sxs-lookup"><span data-stu-id="8d428-1803">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="8d428-1804">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="8d428-1804">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="8d428-1805">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="8d428-1805">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="8d428-1806">2.8.0 – oktober 2019</span><span class="sxs-lookup"><span data-stu-id="8d428-1806">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="8d428-1807">Allmänt</span><span class="sxs-lookup"><span data-stu-id="8d428-1807">General</span></span>
* <span data-ttu-id="8d428-1808">AZ. HealthcareApis 1.0.0-version</span><span class="sxs-lookup"><span data-stu-id="8d428-1808">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="8d428-1809">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8d428-1809">Az.Accounts</span></span>
* <span data-ttu-id="8d428-1810">Uppdatera telemetri och URL-omskrivning för genererade moduler, korrigera Windows-enhetstester.</span><span class="sxs-lookup"><span data-stu-id="8d428-1810">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="8d428-1811">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8d428-1811">Az.ApiManagement</span></span>
* <span data-ttu-id="8d428-1812">**Set-AzApiManagementApi** – Tillagt stöd för att uppdatera Api till ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="8d428-1812">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="8d428-1813">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="8d428-1813">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8d428-1814">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8d428-1814">Az.Automation</span></span>
* <span data-ttu-id="8d428-1815">Åtgärdade cmdleten New-AzureAutomationSoftwareUpdateConfiguration för parametern för inställning av Linux-omstart.</span><span class="sxs-lookup"><span data-stu-id="8d428-1815">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="8d428-1816">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="8d428-1816">Az.Batch</span></span>
* <span data-ttu-id="8d428-1817">**Get-AzBatchNodeAgentSku** är inaktuell och ersätts av **Get-AzBatchSupportImage** i version 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="8d428-1817">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d428-1818">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d428-1818">Az.Compute</span></span>
* <span data-ttu-id="8d428-1819">Lägg till parametrarna Priority, EvictionPolicy och MaxPrice till cmdletarna New-AzVM och New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8d428-1819">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="8d428-1820">Korrigera varningsmeddelande och hjälpdokument för cmdletarna Add-AzVMAdditionalUnattendContent och Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="8d428-1820">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="8d428-1821">Åtgärda – skipVmBackup-undantag för virtuella Linux-datorer med hanterade diskar för Set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="8d428-1821">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="8d428-1822">Åtgärda fel i uppdatera krypteringsinställningarna i set-AzVMDiskEncryptionExtension, scenario i två steg.</span><span class="sxs-lookup"><span data-stu-id="8d428-1822">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8d428-1823">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8d428-1823">Az.DataFactory</span></span>
* <span data-ttu-id="8d428-1824">Lägga till CRUD-kommandon för ADF V2-dataflödet: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow och Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="8d428-1824">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="8d428-1825">Lägger till åtgärdskommandon för ADF V2-dataflödesfelsökningssession: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand och Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="8d428-1825">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="8d428-1826">Uppdatera ADF .Net SDK-versionen till 4.2.0</span><span class="sxs-lookup"><span data-stu-id="8d428-1826">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8d428-1827">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8d428-1827">Az.DataLakeStore</span></span>
* <span data-ttu-id="8d428-1828">Korrigera kontovalidering så att konton med ”-” kan skickas utan domän</span><span class="sxs-lookup"><span data-stu-id="8d428-1828">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="8d428-1829">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="8d428-1829">Az.HealthcareApis</span></span>
* <span data-ttu-id="8d428-1830">PowerShell-versionen har uppdaterats till 1.0.0</span><span class="sxs-lookup"><span data-stu-id="8d428-1830">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="8d428-1831">Uppdaterade SDK-versionen till 1.0.2</span><span class="sxs-lookup"><span data-stu-id="8d428-1831">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="8d428-1832">Uppdatera i tester för att referera till en ny SDK-version</span><span class="sxs-lookup"><span data-stu-id="8d428-1832">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="8d428-1833">Utdatastrukturen har uppdaterats från kapslad till förenklad.</span><span class="sxs-lookup"><span data-stu-id="8d428-1833">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8d428-1834">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8d428-1834">Az.IotHub</span></span>
* <span data-ttu-id="8d428-1835">Lägg till ny routningskälla: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="8d428-1835">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="8d428-1836">Mindre felkorrigering: Get-AzIothub returnerar inte subscriptionId</span><span class="sxs-lookup"><span data-stu-id="8d428-1836">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8d428-1837">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8d428-1837">Az.Monitor</span></span>
* <span data-ttu-id="8d428-1838">Nya åtgärdsgruppsmottagare har lagts till för åtgärdsgrupp   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="8d428-1838">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="8d428-1839">Använd vanligt aviseringsschema som är aktiverat för mottagarna.</span><span class="sxs-lookup"><span data-stu-id="8d428-1839">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="8d428-1840">Detta gäller inte för SMS, push för Azure-app, ITSM och röstmottagare</span><span class="sxs-lookup"><span data-stu-id="8d428-1840">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="8d428-1841">Webhooks har nu stöd för Azure Active Directory-autentisering.</span><span class="sxs-lookup"><span data-stu-id="8d428-1841">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8d428-1842">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d428-1842">Az.Network</span></span>
* <span data-ttu-id="8d428-1843">Lägg till ny cmdlet Get-AzAvailableServiceAlias som kan anropas för att hämta de alias som kan användas för tjänstslutpunktsprinciper.</span><span class="sxs-lookup"><span data-stu-id="8d428-1843">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="8d428-1844">Stöd för tillägg av trafikväljare har lagts till i gatewayanslutningar för virtuella nätverk</span><span class="sxs-lookup"><span data-stu-id="8d428-1844">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="8d428-1845">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="8d428-1845">New cmdlets added:</span></span>
        - <span data-ttu-id="8d428-1846">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="8d428-1846">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="8d428-1847">Cmdletar har uppdaterats med valfri parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="8d428-1847">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="8d428-1848">Lägg till stöd för ESP- och AH-protokoll i konfiguration av nätverkssäkerhetsregler</span><span class="sxs-lookup"><span data-stu-id="8d428-1848">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="8d428-1849">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="8d428-1849">Updated cmdlets:</span></span>
        - <span data-ttu-id="8d428-1850">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8d428-1850">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="8d428-1851">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8d428-1851">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="8d428-1852">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8d428-1852">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="8d428-1853">Förbättra hanteringen av undantag i Cortex-cmdletar</span><span class="sxs-lookup"><span data-stu-id="8d428-1853">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="8d428-1854">Nya generationer och SKU:er för VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="8d428-1854">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="8d428-1855">Introducera nya generationer för VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="8d428-1855">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="8d428-1856">Introducera nya SKU:er med högt dataflöde för VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="8d428-1856">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="8d428-1857">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="8d428-1857">Az.RedisCache</span></span>
* <span data-ttu-id="8d428-1858">Uppdaterad referensdokumentation för ”set-AzRedisCache” för att inkludera saknade värden för parametern ”size”</span><span class="sxs-lookup"><span data-stu-id="8d428-1858">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="8d428-1859">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d428-1859">Az.Sql</span></span>
* <span data-ttu-id="8d428-1860">Lägg till stöd för inställningen Active Directory administratör på den hanterade instansen</span><span class="sxs-lookup"><span data-stu-id="8d428-1860">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8d428-1861">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8d428-1861">Az.Storage</span></span>
* <span data-ttu-id="8d428-1862">Uppdatera Lagringsklientbibliotek till 11.1.0</span><span class="sxs-lookup"><span data-stu-id="8d428-1862">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="8d428-1863">Lista containrar med hanteringsplans-API, kommer att listas med NextPageLink</span><span class="sxs-lookup"><span data-stu-id="8d428-1863">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="8d428-1864">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="8d428-1864">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="8d428-1865">Lista lagringskonton från prenumerationen, kommer att listas med NextPageLink</span><span class="sxs-lookup"><span data-stu-id="8d428-1865">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="8d428-1866">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8d428-1866">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="8d428-1867">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="8d428-1867">Az.StorageSync</span></span>
* <span data-ttu-id="8d428-1868">Åtgärda problemet 9810 i Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="8d428-1868">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8d428-1869">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8d428-1869">Az.Websites</span></span>
* <span data-ttu-id="8d428-1870">Set-AzWebApp – uppdatering av ASP för en app misslyckades</span><span class="sxs-lookup"><span data-stu-id="8d428-1870">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="8d428-1871">2.7.0 – september 2019</span><span class="sxs-lookup"><span data-stu-id="8d428-1871">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="8d428-1872">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8d428-1872">Az.ApiManagement</span></span>
* <span data-ttu-id="8d428-1873">Uppdatera ”-Format”-parameterbeskrivningen i ”Set-AzApiManagementPolicy”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="8d428-1873">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="8d428-1874">Referenser för den föråldrade cmdleten ”Update-AzApiManagementDeployment” har tagits bort från referensdokumentationen.</span><span class="sxs-lookup"><span data-stu-id="8d428-1874">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="8d428-1875">Använd ”Set-AzApiManagement” i stället.</span><span class="sxs-lookup"><span data-stu-id="8d428-1875">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8d428-1876">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8d428-1876">Az.Automation</span></span>
* <span data-ttu-id="8d428-1877">Stavfel har korrigerats i exempel i referensdokumentationen för ”Register-AzAutomationDscNode”</span><span class="sxs-lookup"><span data-stu-id="8d428-1877">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="8d428-1878">Klargörande har lagts till om OS-begränsningar för Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="8d428-1878">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="8d428-1879">Null-referensundantag har korrigerats för -Wait-alternativet i Start-AzAutomationRunbook-cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8d428-1879">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d428-1880">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d428-1880">Az.Compute</span></span>
* <span data-ttu-id="8d428-1881">Lägg till UploadSizeInBytes-parameter till New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="8d428-1881">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="8d428-1882">Lägg till Incremental-parameter till New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="8d428-1882">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="8d428-1883">Lägg till en funktion för virtuella datorer med låg prioritet:</span><span class="sxs-lookup"><span data-stu-id="8d428-1883">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="8d428-1884">MaxPrice-, EvictionPolicy- och Priority-parametrar har lagts till i New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="8d428-1884">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="8d428-1885">MaxPrice-parametern har lagts till i New-AzVmssConfig-, Update-AzVM- och Update-AzVmss-cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="8d428-1885">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="8d428-1886">Åtgärda problem med VM-referenser för Get-AzAvailabilitySet-cmdleten när alla tillgänglighetsuppsättningar i prenumerationen visas.</span><span class="sxs-lookup"><span data-stu-id="8d428-1886">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="8d428-1887">Korrigera null-undantaget för Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="8d428-1887">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="8d428-1888">Korrigera VHD-metoden för sökning relativt till slut.</span><span class="sxs-lookup"><span data-stu-id="8d428-1888">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="8d428-1889">Åtgärda UltraSSD-problem för New-AzVM och Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="8d428-1889">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8d428-1890">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8d428-1890">Az.DataFactory</span></span>
* <span data-ttu-id="8d428-1891">Lägger till 3 nya kommandon för ADF V2 – Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription och Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="8d428-1891">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="8d428-1892">ADF .Net SDK har uppdaterats till 4.1.3</span><span class="sxs-lookup"><span data-stu-id="8d428-1892">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="8d428-1893">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8d428-1893">Az.HDInsight</span></span>
* <span data-ttu-id="8d428-1894">Anrop för icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="8d428-1894">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8d428-1895">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8d428-1895">Az.IotHub</span></span>
* <span data-ttu-id="8d428-1896">Lägg till stöd för att anropa redundans för en IotHub till den geo-länkade katastrofåterställningsregionen.</span><span class="sxs-lookup"><span data-stu-id="8d428-1896">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="8d428-1897">Lägg till stöd för att hantera meddelandeberikning för en IotHub.</span><span class="sxs-lookup"><span data-stu-id="8d428-1897">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="8d428-1898">Nya cmdlet:ar är:</span><span class="sxs-lookup"><span data-stu-id="8d428-1898">New cmdlets are:</span></span>
    - <span data-ttu-id="8d428-1899">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="8d428-1899">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="8d428-1900">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="8d428-1900">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="8d428-1901">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="8d428-1901">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="8d428-1902">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="8d428-1902">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8d428-1903">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8d428-1903">Az.Monitor</span></span>
* <span data-ttu-id="8d428-1904">Pekar på den senaste Monitor SDK:n, dvs. 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="8d428-1904">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="8d428-1905">Lägger till bakåtkompatibla ändringar i Metrics-cmdletarna, dvs. enhetsuppräkningen stöder flera nya värden.</span><span class="sxs-lookup"><span data-stu-id="8d428-1905">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="8d428-1906">Detta är skrivskyddade cmdletar, så det förekommer inga ändringar i inmatningen för cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="8d428-1906">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="8d428-1907">API-versionen för **ActionGroups** -begäranden är nu **2019-06-01**. Tidigare var den **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="8d428-1907">The api-version of the **ActionGroups** requests is now **2019-06-01** , before it was **2018-03-01**.</span></span> <span data-ttu-id="8d428-1908">Test av scenarier har uppdaterats för att anpassas till den här ändringen.</span><span class="sxs-lookup"><span data-stu-id="8d428-1908">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="8d428-1909">Ett nytt obligatoriskt argument har lagts till för konstruktorerna för klasserna **EmailReceiver** och **WebhookReceiver** – ett booleskt värde med namnet **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="8d428-1909">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="8d428-1910">Värdet är för närvarande fast till **false** så att den här icke-bakåtkompatibla ändringen är dold från cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="8d428-1910">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="8d428-1911">**Obs!** Det här är en tillfällig ändring som måste verifieras av Alerts-teamet.</span><span class="sxs-lookup"><span data-stu-id="8d428-1911">**NOTE** : this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="8d428-1912">Ordningen på argumenten för konstruktorn för klassen **Source** (relaterad till klassen **ScheduledQueryRuleSource** ) har ändrats från den tidigare SDK:n.</span><span class="sxs-lookup"><span data-stu-id="8d428-1912">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="8d428-1913">Den här ändringen krävde korrigering av två enhetstest: de kompilerades, men testerna skickades inte.</span><span class="sxs-lookup"><span data-stu-id="8d428-1913">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="8d428-1914">Ordningen på argumenten för konstruktorn för klassen **AlertingAction** (relaterad till klassen **ScheduledQueryRuleSource** ) har ändrats från den tidigare SDK:n.</span><span class="sxs-lookup"><span data-stu-id="8d428-1914">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="8d428-1915">Den här ändringen krävde korrigering av två enhetstest: de kompilerades, men testerna skickades inte.</span><span class="sxs-lookup"><span data-stu-id="8d428-1915">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="8d428-1916">Stöd för kriterier för dynamiskt tröskelvärde för måttavisering v2</span><span class="sxs-lookup"><span data-stu-id="8d428-1916">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="8d428-1917">New-AzMetricAlertRuleV2Criteria: skapar nu även kriterier för dynamiskt tröskelvärde</span><span class="sxs-lookup"><span data-stu-id="8d428-1917">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="8d428-1918">Add-AzMetricAlertRuleV2: accepterar nu även kriterier för dynamiskt tröskelvärde</span><span class="sxs-lookup"><span data-stu-id="8d428-1918">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="8d428-1919">Förbättringar i schemalagd frågeregel (SQR)</span><span class="sxs-lookup"><span data-stu-id="8d428-1919">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="8d428-1920">Cmdletar accepterar ”Location”-parameter i båda formaten, antingen platsen (t.ex. eastus) eller platsens visningsnamn (t.ex. USA, östra)</span><span class="sxs-lookup"><span data-stu-id="8d428-1920">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="8d428-1921">”Enabled”-parametern illustreras korrekt i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="8d428-1921">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="8d428-1922">Exempel för den valfria parametern ”ActionGroup” har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-1922">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="8d428-1923">Förbättrade hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="8d428-1923">Overall improved help files</span></span>
* <span data-ttu-id="8d428-1924">Åtgärda bugg då omfattningstypen fastställs för ”Set-AzActionRule”</span><span class="sxs-lookup"><span data-stu-id="8d428-1924">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8d428-1925">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d428-1925">Az.Network</span></span>
* <span data-ttu-id="8d428-1926">Korrigera felaktigt exempel i referensdokumentationen för ”New-AzApplicationGateway”</span><span class="sxs-lookup"><span data-stu-id="8d428-1926">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="8d428-1927">Lägg till anmärkning i ”Get-AzNetworkWatcherPacketCapture”-referensdokumentationen om hämtning av alla egenskaper för en paketinsamling</span><span class="sxs-lookup"><span data-stu-id="8d428-1927">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="8d428-1928">Exempel har korrigerats i ”Test-AzNetworkWatcherIPFlow”-referensdokumentationen för korrekt uppräkning av nätverkskort</span><span class="sxs-lookup"><span data-stu-id="8d428-1928">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="8d428-1929">Förbättrad tolkning av molnundantag för att visa eventuell ytterligare information</span><span class="sxs-lookup"><span data-stu-id="8d428-1929">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="8d428-1930">Förbättrad tolkning av molnundantag för att hantera ytterligare en typ av SDK-undantag</span><span class="sxs-lookup"><span data-stu-id="8d428-1930">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="8d428-1931">Felaktig mappning av säkerhetsregelmodeller har korrigerats</span><span class="sxs-lookup"><span data-stu-id="8d428-1931">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="8d428-1932">Egenskaper har lagts till för nätverksgränssnittet för funktionen Privat IP</span><span class="sxs-lookup"><span data-stu-id="8d428-1932">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="8d428-1933">Egenskapen ”PrivateEndpoint” har lagts till som en typ av PSResourceId till PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="8d428-1933">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="8d428-1934">Egenskapen ”PrivateLinkConnectionProperties” har lagts till som en typ av PSIpConfigurationConnectivityInformation till PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="8d428-1934">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="8d428-1935">Modellklassen PSIpConfigurationConnectivityInformation har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-1935">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="8d428-1936">ApplicationRuleProtocolType ”mssql” har lagts till för Azure Firewall-resurs</span><span class="sxs-lookup"><span data-stu-id="8d428-1936">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="8d428-1937">MultiLink-stöd i virtuellt WAN</span><span class="sxs-lookup"><span data-stu-id="8d428-1937">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="8d428-1938">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="8d428-1938">New cmdlets</span></span>
        - <span data-ttu-id="8d428-1939">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="8d428-1939">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="8d428-1940">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="8d428-1940">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="8d428-1941">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="8d428-1941">Updated cmdlet:</span></span>
        - <span data-ttu-id="8d428-1942">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="8d428-1942">New-VpnSite</span></span>
        - <span data-ttu-id="8d428-1943">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="8d428-1943">Update-VpnSite</span></span>
        - <span data-ttu-id="8d428-1944">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="8d428-1944">New-VpnConnection</span></span>
        - <span data-ttu-id="8d428-1945">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="8d428-1945">Update-VpnConnection</span></span>
* <span data-ttu-id="8d428-1946">Dokument för vissa PowerShell-exempel har korrigerats så att Az-cmdletar används i stället för AzureRM-cmdletar</span><span class="sxs-lookup"><span data-stu-id="8d428-1946">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8d428-1947">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8d428-1947">Az.RecoveryServices</span></span>
* <span data-ttu-id="8d428-1948">Uppdatera AzureVMpolicy-objekt med ProtectedItemsCount-attribut</span><span class="sxs-lookup"><span data-stu-id="8d428-1948">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="8d428-1949">Ytterligare tester har lagts till för VM-princip och återställning av ursprungligt lagringskonto</span><span class="sxs-lookup"><span data-stu-id="8d428-1949">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="8d428-1950">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d428-1950">Az.Resources</span></span>
* <span data-ttu-id="8d428-1951">Åtgärda fel där det inte gick att anropa New-AzRoleAssignment utan parametern Scope.</span><span class="sxs-lookup"><span data-stu-id="8d428-1951">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8d428-1952">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8d428-1952">Az.ServiceFabric</span></span>
* <span data-ttu-id="8d428-1953">Stavfel har korrigerats i exempel för ”Update-AzServiceFabricReliability”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="8d428-1953">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="8d428-1954">Lägger till nya cmdletar för att hantera program och tjänster:</span><span class="sxs-lookup"><span data-stu-id="8d428-1954">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="8d428-1955">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="8d428-1955">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="8d428-1956">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="8d428-1956">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="8d428-1957">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="8d428-1957">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="8d428-1958">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="8d428-1958">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="8d428-1959">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="8d428-1959">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="8d428-1960">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="8d428-1960">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="8d428-1961">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="8d428-1961">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="8d428-1962">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="8d428-1962">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="8d428-1963">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="8d428-1963">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="8d428-1964">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="8d428-1964">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="8d428-1965">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="8d428-1965">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="8d428-1966">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="8d428-1966">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="8d428-1967">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="8d428-1967">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="8d428-1968">Service Fabric SDK har uppgraderats till version 1.2.0 som använder Service Fabric-resursprovidern med API-version 2019-03-01.</span><span class="sxs-lookup"><span data-stu-id="8d428-1968">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="8d428-1969">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="8d428-1969">Az.SignalR</span></span>
* <span data-ttu-id="8d428-1970">Lägg till Update-, Restart-, CheckNameAvailability- och GetUsage-cmdletar</span><span class="sxs-lookup"><span data-stu-id="8d428-1970">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="8d428-1971">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d428-1971">Az.Sql</span></span>
* <span data-ttu-id="8d428-1972">Uppdatera exempel i referensdokumentationen för ”Get-AzSqlElasticPool”</span><span class="sxs-lookup"><span data-stu-id="8d428-1972">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="8d428-1973">vCore-exempel för att skapa en elastisk pool (New-AzSqlElasticPool) har lagts till.</span><span class="sxs-lookup"><span data-stu-id="8d428-1973">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="8d428-1974">Ta bort verifieringen av EmailAddresses och kontrollen som bekräftar att EmailAdmins inte är falskt när EmailAddresses är tomt i Set-AzSqlServerAdvancedThreatProtectionPolicy och Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="8d428-1974">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="8d428-1975">Server-/databasgranskningsinställningar kan tas bort när det finns flera diagnostikinställningar som aktiverar granskningskategorin.</span><span class="sxs-lookup"><span data-stu-id="8d428-1975">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="8d428-1976">Åtgärda verifiering av e-postadresser i flera Sql Vulnerability Assessment-cmdletar (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting och Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="8d428-1976">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8d428-1977">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8d428-1977">Az.Storage</span></span>
* <span data-ttu-id="8d428-1978">Exempel i referensdokumentationen för ”Get-AzStorageAccountKey” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="8d428-1978">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="8d428-1979">Vid upp- och nedladdning av en Azure-fil kan SMB-egenskaperna för källfilen (t.ex. filattribut, tidpunkten då filen skapades och tidpunkten för den senaste skrivningen) sparas i målfilen</span><span class="sxs-lookup"><span data-stu-id="8d428-1979">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="8d428-1980">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="8d428-1980">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="8d428-1981">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="8d428-1981">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="8d428-1982">Korrigera problem med uppladdningen av blockblob med egenskaper/metadata för ImmutabilityPolicy i containrar.</span><span class="sxs-lookup"><span data-stu-id="8d428-1982">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="8d428-1983">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="8d428-1983">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="8d428-1984">Stöd för hantering av Azure-filresurser med API för hanteringsplan</span><span class="sxs-lookup"><span data-stu-id="8d428-1984">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="8d428-1985">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="8d428-1985">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="8d428-1986">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="8d428-1986">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="8d428-1987">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="8d428-1987">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="8d428-1988">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="8d428-1988">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8d428-1989">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8d428-1989">Az.Websites</span></span>
* <span data-ttu-id="8d428-1990">Åtgärdar problemet där webapp-taggar togs bort när appen migrerades till nya ASP</span><span class="sxs-lookup"><span data-stu-id="8d428-1990">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="8d428-1991">Åtgärda Publish-AzureWebapp så att det fungerar i Linux och Windows</span><span class="sxs-lookup"><span data-stu-id="8d428-1991">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="8d428-1992">Uppdatera exempel i ”Get-AzWebAppPublishingProfile”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="8d428-1992">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="8d428-1993">2.6.0 – augusti 2019</span><span class="sxs-lookup"><span data-stu-id="8d428-1993">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="8d428-1994">Allmänt</span><span class="sxs-lookup"><span data-stu-id="8d428-1994">General</span></span>
* <span data-ttu-id="8d428-1995">Åtgärdade diverse skrivfel i flera moduler</span><span class="sxs-lookup"><span data-stu-id="8d428-1995">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="8d428-1996">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8d428-1996">Az.Accounts</span></span>
* <span data-ttu-id="8d428-1997">Stöd för användartilldelat MSI i Azure Functions-autentisering (#9479)</span><span class="sxs-lookup"><span data-stu-id="8d428-1997">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="8d428-1998">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="8d428-1998">Az.Aks</span></span>
* <span data-ttu-id="8d428-1999">Åtgärda problem med utdata för "Get-AzAks"</span><span class="sxs-lookup"><span data-stu-id="8d428-1999">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="8d428-2000">Mer information här: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="8d428-2000">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="8d428-2001">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8d428-2001">Az.ApiManagement</span></span>
* <span data-ttu-id="8d428-2002">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="8d428-2002">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="8d428-2003">Uppdatera .net-NuGet-versionen, som inte tillämpar begränsningar för productId, apiId och userId</span><span class="sxs-lookup"><span data-stu-id="8d428-2003">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="8d428-2004">**Get-AzApiManagementProduct** – Lade till stöd för frågekörning mot produkter via API.</span><span class="sxs-lookup"><span data-stu-id="8d428-2004">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="8d428-2005">**New-AzApiManagementApiRevision** – Korrigering för problem där ApiRevisionDescription inte angavs vid skapande av ny API-revision https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="8d428-2005">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="8d428-2006">Åtgärdade skrivfel i modellen "PsApiManagementOAuth2AuthrozationServer" till "PsApiManagementOAuth2AuthorizationServer"</span><span class="sxs-lookup"><span data-stu-id="8d428-2006">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="8d428-2007">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="8d428-2007">Az.Batch</span></span>
* <span data-ttu-id="8d428-2008">Åtgärdade skrivfel i hjälpmeddelande och dokumentation till att skriva Windows med versaler</span><span class="sxs-lookup"><span data-stu-id="8d428-2008">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="8d428-2009">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="8d428-2009">Az.Cdn</span></span>
* <span data-ttu-id="8d428-2010">Åtgärdade skrivfel i CDN-modulens konverteringshjälp</span><span class="sxs-lookup"><span data-stu-id="8d428-2010">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d428-2011">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d428-2011">Az.Compute</span></span>
* <span data-ttu-id="8d428-2012">Lägg till VmssId i New-AzVMConfig-cmdleten</span><span class="sxs-lookup"><span data-stu-id="8d428-2012">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="8d428-2013">Lägg till parametrarna TerminateScheduledEvents och TerminateScheduledEventNotBeforeTimeoutInMinutes i New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8d428-2013">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="8d428-2014">Lägg till egenskapen HyperVGeneration till avbildningsobjekt för virtuell dator</span><span class="sxs-lookup"><span data-stu-id="8d428-2014">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="8d428-2015">Lägg till funktioner för Host och HostGroup</span><span class="sxs-lookup"><span data-stu-id="8d428-2015">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="8d428-2016">Nya cmdletar:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="8d428-2016">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="8d428-2017">HostId-parametern läggs till i New-AzVMConfig och New-AzVM</span><span class="sxs-lookup"><span data-stu-id="8d428-2017">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="8d428-2018">Uppdatera exempel i "Invoke-AzVMRunCommand"-dokumentationen till att använda rätt parameternamn</span><span class="sxs-lookup"><span data-stu-id="8d428-2018">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="8d428-2019">Uppdatera "-VolumeType"-beskrivningen i referensdokumentationen för "set-AzVMDiskEncryptionExtension" och "set-AzVmssDiskEncryptionExtension"</span><span class="sxs-lookup"><span data-stu-id="8d428-2019">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8d428-2020">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8d428-2020">Az.DataFactory</span></span>
* <span data-ttu-id="8d428-2021">Åtgärda skrivfel till att använda versaler för "Windows" i "New-AzDataFactoryEncryptValue"-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="8d428-2021">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="8d428-2022">Uppdaterade ADF .Net SDK-versionen till 4.1.2</span><span class="sxs-lookup"><span data-stu-id="8d428-2022">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="8d428-2023">Lägg till parametrarna "DataProxyIntegrationRuntimeName", "DataProxyStagingLinkedServiceName" och "DataProxyStagingPath" för "Set-AzureRmDataFactoryV2IntegrationRuntime"-cmd för att aktivera konfiguration av lokalt installerad integrationskörning som en proxy för SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="8d428-2023">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="8d428-2024">Uppdaterade PSTriggerRun till att visa utlöst pipeline, meddelande och egenskaper samt PSActivityRun till att visa aktivitetstypen</span><span class="sxs-lookup"><span data-stu-id="8d428-2024">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8d428-2025">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8d428-2025">Az.DataLakeStore</span></span>
* <span data-ttu-id="8d428-2026">Korrigering av frysning av Get-DataLakeStoreDeletedItem för fel eller fjärrundantag.</span><span class="sxs-lookup"><span data-stu-id="8d428-2026">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="8d428-2027">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8d428-2027">Az.EventHub</span></span>
* <span data-ttu-id="8d428-2028">Korrigering av problem #9658 : Skrivfel i parametern VirtualNteworkRule i Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="8d428-2028">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="8d428-2029">Korrigering av problem #9558 : Set-AzEventHubNamespace använder PATCH i stället för PUT</span><span class="sxs-lookup"><span data-stu-id="8d428-2029">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="8d428-2030">lade till parametern EnableKafka i Set-AzEventHubNamespace-cmdleten</span><span class="sxs-lookup"><span data-stu-id="8d428-2030">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="8d428-2031">Korrigering av problem #9786 : kan inte skapa en regel med Endast lyssna-behörighet</span><span class="sxs-lookup"><span data-stu-id="8d428-2031">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="8d428-2032">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="8d428-2032">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="8d428-2033">Åtgärdade skrivfel i dokumentation där "Azure" skrevs helt med gemener</span><span class="sxs-lookup"><span data-stu-id="8d428-2033">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8d428-2034">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8d428-2034">Az.Monitor</span></span>
* <span data-ttu-id="8d428-2035">Åtgärdade felaktigt parameternamn i hjälpdokumentationen</span><span class="sxs-lookup"><span data-stu-id="8d428-2035">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8d428-2036">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d428-2036">Az.Network</span></span>
* <span data-ttu-id="8d428-2037">Uppdaterade New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="8d428-2037">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="8d428-2038">Gjorde parametern "PublicIpAddress" inaktuell eftersom den aldrig används på serversidan.</span><span class="sxs-lookup"><span data-stu-id="8d428-2038">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="8d428-2039">Lade till den valfria parametern "Primary", som anger huruvida den aktuella IP-konfigurationen är den primära.</span><span class="sxs-lookup"><span data-stu-id="8d428-2039">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="8d428-2040">Förbättrade hanteringen av felundantag för begärande från SDK – åtgärdar problemet att tidigare SDK-undantag inte hanteras på rätt sätt, vilket leder till att viktig felinformation inte visas</span><span class="sxs-lookup"><span data-stu-id="8d428-2040">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="8d428-2041">Justerade valideringslogiken för IPv6-IP-prefix till att kontrollera korrekt IPv6-prefixlängd.</span><span class="sxs-lookup"><span data-stu-id="8d428-2041">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="8d428-2042">Uppdaterade Get-AzVirtualNetworkSubnetConfig: Lade till parameter som anges till get av undernätets resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="8d428-2042">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="8d428-2043">Uppdaterade beskrivningen av parametern Location för AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="8d428-2043">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8d428-2044">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8d428-2044">Az.OperationalInsights</span></span>
* <span data-ttu-id="8d428-2045">Uppdaterade dokumentation för "New-AzOperationalInsightsLinuxSyslogDataSource"</span><span class="sxs-lookup"><span data-stu-id="8d428-2045">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="8d428-2046">Lade till exempel</span><span class="sxs-lookup"><span data-stu-id="8d428-2046">Added example</span></span>
    - <span data-ttu-id="8d428-2047">Uppdaterade beskrivningen av parametern "-Name"</span><span class="sxs-lookup"><span data-stu-id="8d428-2047">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="8d428-2048">Lade till ett exempel för New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="8d428-2048">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="8d428-2049">Ändrade beskrivningen av parametern -Name för New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="8d428-2049">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8d428-2050">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8d428-2050">Az.RecoveryServices</span></span>
* <span data-ttu-id="8d428-2051">Uppdatera "Get-AzRecoveryServicesBackupJobDetail.md"</span><span class="sxs-lookup"><span data-stu-id="8d428-2051">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="8d428-2052">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d428-2052">Az.Resources</span></span>
* <span data-ttu-id="8d428-2053">Lägg till stöd för den nya API-versionen från 2019-05-10 för Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="8d428-2053">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="8d428-2054">Lägg till stöd för "copy.count = 0" för variabler, resurser och egenskaper</span><span class="sxs-lookup"><span data-stu-id="8d428-2054">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="8d428-2055">Resurser med "condition = false" eller "copy.count = 0" tas bort i complete-läget</span><span class="sxs-lookup"><span data-stu-id="8d428-2055">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="8d428-2056">Lägg till ett exempel på tilldelning av princip på prenumerationsnivå i hjälpdokumentationen</span><span class="sxs-lookup"><span data-stu-id="8d428-2056">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="8d428-2057">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8d428-2057">Az.ServiceBus</span></span>
* <span data-ttu-id="8d428-2058">Korrigering av problem #9658 : Skrivfel i parametern VirtualNetworkRule i set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="8d428-2058">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="8d428-2059">Korrigering av problem #9786 : kan inte skapa en regel med Endast lyssna-behörighet</span><span class="sxs-lookup"><span data-stu-id="8d428-2059">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="8d428-2060">Lade till det nya kommandot "Test-AzServiceBusNameAvailability" för att kontrollera namntillgängligheten för kö och ämne</span><span class="sxs-lookup"><span data-stu-id="8d428-2060">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8d428-2061">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8d428-2061">Az.ServiceFabric</span></span>
* <span data-ttu-id="8d428-2062">Åtgärda buggar med tillägg av nodtyps-cmdlet:</span><span class="sxs-lookup"><span data-stu-id="8d428-2062">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="8d428-2063">NullReferenceException-bugg när resursgrupp hade annan vmss som inte är relaterad till Service Fabric-klustret.</span><span class="sxs-lookup"><span data-stu-id="8d428-2063">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="8d428-2064">Åtgärdar problemet: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="8d428-2064">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="8d428-2065">Åtgärda bugg där cmdleten misslyckades om virtualNetwork var i en annan resursgrupp än klustret.</span><span class="sxs-lookup"><span data-stu-id="8d428-2065">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="8d428-2066">Åtgärdar problemet: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="8d428-2066">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="8d428-2067">AzServiceFabricApplicationCertificate-cmdleten görs inaktuell</span><span class="sxs-lookup"><span data-stu-id="8d428-2067">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="8d428-2068">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d428-2068">Az.Sql</span></span>
* <span data-ttu-id="8d428-2069">Uppdatera dokumentation om gamla gransknings-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="8d428-2069">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8d428-2070">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8d428-2070">Az.Storage</span></span>
* <span data-ttu-id="8d428-2071">Uppdatera hjälpen för Get/Close-AzStorageFileHandle genom att lägga till fler scenarier i cmdlet-exempel och uppdatera parameterbeskrivningar</span><span class="sxs-lookup"><span data-stu-id="8d428-2071">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="8d428-2072">Stöd för StandardBlobTier i uppladdningsblob och kopieringsblob</span><span class="sxs-lookup"><span data-stu-id="8d428-2072">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="8d428-2073">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="8d428-2073">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="8d428-2074">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="8d428-2074">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="8d428-2075">Stöd för rehydratiseringsprioritet i kopieringsblob</span><span class="sxs-lookup"><span data-stu-id="8d428-2075">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="8d428-2076">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="8d428-2076">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8d428-2077">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8d428-2077">Az.Websites</span></span>
* <span data-ttu-id="8d428-2078">Lägg till klargöranden gällande parametern -AppSettings i Set-AzWebApp och Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8d428-2078">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="8d428-2079">2.5.0 – July 2019</span><span class="sxs-lookup"><span data-stu-id="8d428-2079">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8d428-2080">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8d428-2080">Az.Accounts</span></span>
* <span data-ttu-id="8d428-2081">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="8d428-2081">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="8d428-2082">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="8d428-2082">Az.ApplicationInsights</span></span>
* <span data-ttu-id="8d428-2083">Korrigera skrivfel i exempel i dokumentationen för Remove-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="8d428-2083">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8d428-2084">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8d428-2084">Az.Automation</span></span>
* <span data-ttu-id="8d428-2085">Korrigera skrivfel i resurssträng</span><span class="sxs-lookup"><span data-stu-id="8d428-2085">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="8d428-2086">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8d428-2086">Az.CognitiveServices</span></span>
* <span data-ttu-id="8d428-2087">Stöd för NetworkRuleSet har lagts till.</span><span class="sxs-lookup"><span data-stu-id="8d428-2087">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d428-2088">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d428-2088">Az.Compute</span></span>
* <span data-ttu-id="8d428-2089">Lägg till saknade egenskaper (ComputerName, OsName, OsVersion och HyperVGeneration) för visningsobjekt i den virtuella datorinstansen.</span><span class="sxs-lookup"><span data-stu-id="8d428-2089">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="8d428-2090">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8d428-2090">Az.ContainerRegistry</span></span>
* <span data-ttu-id="8d428-2091">Åtgärda skrivfel i Remove-AzContainerRegistryReplication för parametern Replication</span><span class="sxs-lookup"><span data-stu-id="8d428-2091">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="8d428-2092">Mer information finns här: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="8d428-2092">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8d428-2093">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8d428-2093">Az.DataFactory</span></span>
* <span data-ttu-id="8d428-2094">ADF .Net SDK-versionen har uppdaterats till 4.1.0</span><span class="sxs-lookup"><span data-stu-id="8d428-2094">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="8d428-2095">Korrigera skrivfel i dokumentationen för Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="8d428-2095">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="8d428-2096">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8d428-2096">Az.EventHub</span></span>
* <span data-ttu-id="8d428-2097">Ny cmmdlet har lagts till för att skapa SAS-token: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="8d428-2097">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="8d428-2098">verifierings- och felmeddelande har lagts till för authorizationrules-rättigheter om endast "hantera" har tilldelats</span><span class="sxs-lookup"><span data-stu-id="8d428-2098">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8d428-2099">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8d428-2099">Az.KeyVault</span></span>
* <span data-ttu-id="8d428-2100">Stöd har lagts till för att ange KeySize för certifikatprinciper</span><span class="sxs-lookup"><span data-stu-id="8d428-2100">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="8d428-2101">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="8d428-2101">Az.LogicApp</span></span>
* <span data-ttu-id="8d428-2102">Korrigering för Get-AzIntegrationAccountMap för att lista alla mappningstyper</span><span class="sxs-lookup"><span data-stu-id="8d428-2102">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="8d428-2103">Ny MapType-parameter har lagts till för filtrering</span><span class="sxs-lookup"><span data-stu-id="8d428-2103">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="8d428-2104">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="8d428-2104">Az.ManagedServices</span></span>
* <span data-ttu-id="8d428-2105">Stöd för API-versionen 2019-06-01 (GA) har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-2105">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8d428-2106">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d428-2106">Az.Network</span></span>
* <span data-ttu-id="8d428-2107">Lägg till stöd för privat slutpunkt och privat länktjänst</span><span class="sxs-lookup"><span data-stu-id="8d428-2107">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="8d428-2108">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="8d428-2108">New cmdlets</span></span>
        - <span data-ttu-id="8d428-2109">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="8d428-2109">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="8d428-2110">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="8d428-2110">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="8d428-2111">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8d428-2111">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="8d428-2112">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8d428-2112">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="8d428-2113">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8d428-2113">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="8d428-2114">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8d428-2114">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="8d428-2115">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="8d428-2115">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="8d428-2116">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="8d428-2116">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="8d428-2117">Nedanstående kommandon för funktionen har uppdaterats: Flaggan PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies på undernätet i VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="8d428-2117">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="8d428-2118">Uppdaterade New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="8d428-2118">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="8d428-2119">Valfri parameter har lagts till – PrivateEndpointNetworkPoliciesFlag som konfigurerar huruvida nätverksprinciper ska tillämpas på en privat slutpunkt i det här undernätet.</span><span class="sxs-lookup"><span data-stu-id="8d428-2119">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="8d428-2120">Valfri parameter har lagts till – PrivateLinkServiceNetworkPoliciesFlag som konfigurerar huruvida nätverksprinciper ska tillämpas på en privat länktjänst i det här undernätet.</span><span class="sxs-lookup"><span data-stu-id="8d428-2120">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="8d428-2121">AzPrivateLinkService för cmdlet-parametern ServiceName har bytt namn till Name med aliaset ServiceName för bakåtkompatibilitet</span><span class="sxs-lookup"><span data-stu-id="8d428-2121">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="8d428-2122">Aktivera ICMP-protokoll för konfiguration av nätverkssäkerhetsregler</span><span class="sxs-lookup"><span data-stu-id="8d428-2122">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="8d428-2123">Uppdaterade cmdletar</span><span class="sxs-lookup"><span data-stu-id="8d428-2123">Updated cmdlets</span></span>
        - <span data-ttu-id="8d428-2124">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8d428-2124">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="8d428-2125">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8d428-2125">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="8d428-2126">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8d428-2126">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="8d428-2127">Lägg till ConnectionProtocolType (Ikev1/Ikev2) som en konfigurerbar parameter för New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="8d428-2127">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="8d428-2128">Lägg till PrivateIpAddressVersion i LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="8d428-2128">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="8d428-2129">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="8d428-2129">Updated cmdlet:</span></span>
        - <span data-ttu-id="8d428-2130">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="8d428-2130">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="8d428-2131">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="8d428-2131">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="8d428-2132">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="8d428-2132">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="8d428-2133">Uppdatering av Application Gateway-kommandot New-AzApplicationGatewayProbeConfig för stöd av anpassad port i Probe</span><span class="sxs-lookup"><span data-stu-id="8d428-2133">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="8d428-2134">Uppdaterade New-AzApplicationGatewayProbeConfig: Den valfria parametern Port som används för avsökning i serverdelen har lagts till.</span><span class="sxs-lookup"><span data-stu-id="8d428-2134">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="8d428-2135">Denna parameter gäller för SKU:erna Standard_V2 och WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="8d428-2135">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8d428-2136">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8d428-2136">Az.OperationalInsights</span></span>
* <span data-ttu-id="8d428-2137">Uppdaterade standardversionen för sparade sökningar till 1.</span><span class="sxs-lookup"><span data-stu-id="8d428-2137">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="8d428-2138">Åtgärdade hantering av anpassad log null regex</span><span class="sxs-lookup"><span data-stu-id="8d428-2138">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8d428-2139">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8d428-2139">Az.RecoveryServices</span></span>
* <span data-ttu-id="8d428-2140">Uppdatera Get-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="8d428-2140">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="8d428-2141">Uppdatera Get-AzRecoveryServicesBackupContainer.md</span><span class="sxs-lookup"><span data-stu-id="8d428-2141">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="8d428-2142">Uppdatera Get-AzRecoveryServicesVault.md</span><span class="sxs-lookup"><span data-stu-id="8d428-2142">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="8d428-2143">Uppdatera Wait-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="8d428-2143">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="8d428-2144">Uppdatera Set-AzRecoveryServicesVaultContext.md</span><span class="sxs-lookup"><span data-stu-id="8d428-2144">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="8d428-2145">Uppdatera Get-AzRecoveryServicesBackupItem.md</span><span class="sxs-lookup"><span data-stu-id="8d428-2145">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="8d428-2146">Uppdatera Get-AzRecoveryServicesBackupRecoveryPoint.md</span><span class="sxs-lookup"><span data-stu-id="8d428-2146">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="8d428-2147">Uppdatera Restore-AzRecoveryServicesBackupItem.md</span><span class="sxs-lookup"><span data-stu-id="8d428-2147">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="8d428-2148">Uppdaterat tjänstanrop för avregistrering av container för Azure-filresurs</span><span class="sxs-lookup"><span data-stu-id="8d428-2148">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="8d428-2149">Uppdatera Set-AzRecoveryServicesAsrAlertSetting.md</span><span class="sxs-lookup"><span data-stu-id="8d428-2149">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="8d428-2150">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d428-2150">Az.Resources</span></span>
- <span data-ttu-id="8d428-2151">Ta bort den cmdlet som saknas och som refereras i dokumentationen till New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8d428-2151">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="8d428-2152">Princip-cmdletar har uppdaterats så att de använder den nya API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="8d428-2152">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="8d428-2153">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8d428-2153">Az.ServiceBus</span></span>
* <span data-ttu-id="8d428-2154">Ny cmmdlet har lagts till för att skapa SAS-token: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="8d428-2154">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="8d428-2155">verifierings- och felmeddelande har lagts till för authorizationrules-rättigheter om endast "hantera" har tilldelats</span><span class="sxs-lookup"><span data-stu-id="8d428-2155">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="8d428-2156">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d428-2156">Az.Sql</span></span>
* <span data-ttu-id="8d428-2157">Åtgärda saknade exempel för Set-AzSqlDatabaseSecondary cmdlet</span><span class="sxs-lookup"><span data-stu-id="8d428-2157">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="8d428-2158">Åtgärda angivna återkommande genomsökningar för bedömning av säkerhetsrisk utan angivna e-postadresser</span><span class="sxs-lookup"><span data-stu-id="8d428-2158">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="8d428-2159">Korrigera ett skrivfel i ett varningsmeddelande.</span><span class="sxs-lookup"><span data-stu-id="8d428-2159">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8d428-2160">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8d428-2160">Az.Storage</span></span>
* <span data-ttu-id="8d428-2161">Uppdatera exempel i referensdokumentationen för Get-AzStorageAccount så att rätt parameternamn används</span><span class="sxs-lookup"><span data-stu-id="8d428-2161">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="8d428-2162">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="8d428-2162">Az.StorageSync</span></span>
* <span data-ttu-id="8d428-2163">Lägger till cmdleten Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="8d428-2163">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="8d428-2164">Åtgärda problem 9551 så att TierFilesOlderThanDays föredras</span><span class="sxs-lookup"><span data-stu-id="8d428-2164">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8d428-2165">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8d428-2165">Az.Websites</span></span>
* <span data-ttu-id="8d428-2166">Åtgärdar ett fel där vissa SiteConfig-egenskaper inte returnerades av Get-AzWebApp och Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8d428-2166">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="8d428-2167">Lägger till en ny platsparameter för Get-AzDeletedWebApp och Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="8d428-2167">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="8d428-2168">Åtgärdar ett fel i kloning av webbapp-platser som använder New-AzWebApp-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="8d428-2168">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="8d428-2169">2.4.0 – juli 2019</span><span class="sxs-lookup"><span data-stu-id="8d428-2169">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8d428-2170">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8d428-2170">Az.Accounts</span></span>
* <span data-ttu-id="8d428-2171">Lägg till stöd för profil-cmdletar</span><span class="sxs-lookup"><span data-stu-id="8d428-2171">Add support for profile cmdlets</span></span>
* <span data-ttu-id="8d428-2172">Lägg till stöd för miljöer och dataplaner i genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="8d428-2172">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="8d428-2173">Åtgärda bugg där fel slutpunkt i vissa fall användes för cmdletar för dataplaner i Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="8d428-2173">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="8d428-2174">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="8d428-2174">Az.Advisor</span></span>
* <span data-ttu-id="8d428-2175">GA-version av Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="8d428-2175">GA release of Az.Advisor</span></span>
* <span data-ttu-id="8d428-2176">Den här modulen ingår nu som en del av `Az`-sammanslagningsmodulen</span><span class="sxs-lookup"><span data-stu-id="8d428-2176">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="8d428-2177">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8d428-2177">Az.ApiManagement</span></span>
* <span data-ttu-id="8d428-2178">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="8d428-2178">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="8d428-2179">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="8d428-2179">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="8d428-2180">Stöd för att fråga prenumerationer efter användare och produkt har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-2180">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="8d428-2181">Stöd för att fråga med hjälp av omfång ”/”, ”/apis”, ”/apis/echo-api” har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-2181">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="8d428-2182">Korrigering av problem https://github.com/Azure/azure-powershell/issues/9307 och https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="8d428-2182">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="8d428-2183">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="8d428-2183">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="8d428-2184">Stöd för att ange ”ApiVersion” och ”ApiVersionSetId” när API:er importeras har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-2184">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8d428-2185">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8d428-2185">Az.Automation</span></span>
* <span data-ttu-id="8d428-2186">Bugg med cmdleten Set-AzAutomationConnectionFieldValue för att hantera strängvärde har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="8d428-2186">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d428-2187">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d428-2187">Az.Compute</span></span>
* <span data-ttu-id="8d428-2188">Lägg till parametern HyperVGeneration i New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="8d428-2188">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8d428-2189">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8d428-2189">Az.DataFactory</span></span>
* <span data-ttu-id="8d428-2190">Uppdaterar utdata från ADF-cmdletar som hämtar aktivitetskörningar, hämtar pipelinekörningar och hämtar utlösarkörningar för stöd för Select-Object-pipe.</span><span class="sxs-lookup"><span data-stu-id="8d428-2190">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="8d428-2191">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="8d428-2191">Az.EventGrid</span></span>
* <span data-ttu-id="8d428-2192">Korrigera stavfel i dokumentation om ”New-AzEventGridSubscription”</span><span class="sxs-lookup"><span data-stu-id="8d428-2192">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8d428-2193">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8d428-2193">Az.IotHub</span></span>
* <span data-ttu-id="8d428-2194">Lägg till stöd för att återskapa principnycklar för auktorisering.</span><span class="sxs-lookup"><span data-stu-id="8d428-2194">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8d428-2195">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d428-2195">Az.Network</span></span>
* <span data-ttu-id="8d428-2196">”RoutingPreference” har lagts till i offentliga IP-taggar</span><span class="sxs-lookup"><span data-stu-id="8d428-2196">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="8d428-2197">Förbättra exempel för referensdokumentation om ”Get-AzNetworkServiceTag”</span><span class="sxs-lookup"><span data-stu-id="8d428-2197">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="8d428-2198">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="8d428-2198">Az.PolicyInsights</span></span>
* <span data-ttu-id="8d428-2199">Åtgärda problem med null-referens i Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="8d428-2199">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="8d428-2200">Mer information här: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="8d428-2200">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8d428-2201">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8d428-2201">Az.OperationalInsights</span></span>
* <span data-ttu-id="8d428-2202">Modellen för CustomLog-datakälla som returneras i Get-AzOperationalInsightsDataSource har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8d428-2202">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8d428-2203">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8d428-2203">Az.RecoveryServices</span></span>
* <span data-ttu-id="8d428-2204">Kommandot get-policy för IaaSVM:er har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8d428-2204">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="8d428-2205">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d428-2205">Az.Resources</span></span>
    - <span data-ttu-id="8d428-2206">Korrigera hjälptext för den översta parametern i Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="8d428-2206">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="8d428-2207">Lägg till växlingsstöd på klientsidan för Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="8d428-2207">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="8d428-2208">Lägg till nya parametrar för Set-AzPolicyAssignment, -PolicyParameters och -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="8d428-2208">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="8d428-2209">En mängd dokument- och exempeluppdateringar för Policy-cmdletar</span><span class="sxs-lookup"><span data-stu-id="8d428-2209">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="8d428-2210">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8d428-2210">Az.ServiceBus</span></span>
* <span data-ttu-id="8d428-2211">Korrigering av problem #4938 – New-AzureRmServiceBusQueue returnerar BadRequest vid konfiguration av MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="8d428-2211">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="8d428-2212">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d428-2212">Az.Sql</span></span>
* <span data-ttu-id="8d428-2213">Lägg till cmdletar för instansredundansgrupper från förhandsversion till offentlig version</span><span class="sxs-lookup"><span data-stu-id="8d428-2213">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="8d428-2214">Stöd för granskning för Azure SQL Server\Database med nya cmdletar.</span><span class="sxs-lookup"><span data-stu-id="8d428-2214">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="8d428-2215">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="8d428-2215">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="8d428-2216">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="8d428-2216">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="8d428-2217">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="8d428-2217">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="8d428-2218">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="8d428-2218">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="8d428-2219">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="8d428-2219">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="8d428-2220">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="8d428-2220">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="8d428-2221">Ta bort begränsningar för e-post från inställningarna för sårbarhetsbedömning</span><span class="sxs-lookup"><span data-stu-id="8d428-2221">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8d428-2222">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8d428-2222">Az.Storage</span></span>
* <span data-ttu-id="8d428-2223">Ändra två parametrar ”-IndexDocument” och ”-ErrorDocument404Path” från ”krävs” till ”valfri” i cmdlet:</span><span class="sxs-lookup"><span data-stu-id="8d428-2223">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="8d428-2224">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="8d428-2224">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="8d428-2225">Uppdatera hjälpen för Get-AzStorageBlobContent genom att lägga till ett exempel</span><span class="sxs-lookup"><span data-stu-id="8d428-2225">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="8d428-2226">Visa mer felinformation när cmdleten misslyckas med StorageException</span><span class="sxs-lookup"><span data-stu-id="8d428-2226">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="8d428-2227">Stöd för att skapa eller uppdatera lagringskonto med Azure Files AAD DS-autentisering</span><span class="sxs-lookup"><span data-stu-id="8d428-2227">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="8d428-2228">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8d428-2228">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="8d428-2229">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8d428-2229">Set-AzStorageAccount</span></span>
* <span data-ttu-id="8d428-2230">Stöd för att lista eller stänga filreferenser för en filresurs, filkatalog eller en fil</span><span class="sxs-lookup"><span data-stu-id="8d428-2230">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="8d428-2231">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="8d428-2231">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="8d428-2232">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="8d428-2232">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="8d428-2233">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="8d428-2233">Az.StorageSync</span></span>
* <span data-ttu-id="8d428-2234">Den här modulen ingår nu som en del av `Az`-sammanslagningsmodulen</span><span class="sxs-lookup"><span data-stu-id="8d428-2234">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="8d428-2235">2.3.2 – juni 2019</span><span class="sxs-lookup"><span data-stu-id="8d428-2235">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8d428-2236">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8d428-2236">Az.Accounts</span></span>
* <span data-ttu-id="8d428-2237">Åtgärda bugg med felaktiga webbadresser som i vissa fall användes för Functions-anrop</span><span class="sxs-lookup"><span data-stu-id="8d428-2237">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="8d428-2238">Mer information här: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="8d428-2238">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="8d428-2239">Åtgärda problem med alias från AzureRM i Az-cmdletar</span><span class="sxs-lookup"><span data-stu-id="8d428-2239">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="8d428-2240">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="8d428-2240">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="8d428-2241">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="8d428-2241">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d428-2242">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d428-2242">Az.Compute</span></span>
* <span data-ttu-id="8d428-2243">Parameteruppsättningarna New-AzVm och New-AzVmss accepterar nu parametern ”ProximityPlacementGroup”.</span><span class="sxs-lookup"><span data-stu-id="8d428-2243">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="8d428-2244">Stavfel i referensdokumentationen för ”New-AzVM” har korrigerats</span><span class="sxs-lookup"><span data-stu-id="8d428-2244">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="8d428-2245">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="8d428-2245">Az.Dns</span></span>
* <span data-ttu-id="8d428-2246">Stavfel i hjälpexempel för ”Set-AzDnsZone” har korrigerats.</span><span class="sxs-lookup"><span data-stu-id="8d428-2246">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="8d428-2247">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="8d428-2247">Az.EventGrid</span></span>
* <span data-ttu-id="8d428-2248">Har uppdaterats för att använda API-versionen 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="8d428-2248">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="8d428-2249">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="8d428-2249">New cmdlets:</span></span>
    - <span data-ttu-id="8d428-2250">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="8d428-2250">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="8d428-2251">Skapar en ny Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="8d428-2251">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="8d428-2252">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="8d428-2252">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="8d428-2253">Hämtar information om en Event Grid-domän eller hämtar en lista med alla Event Grid-domäner i den aktuella Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="8d428-2253">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="8d428-2254">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="8d428-2254">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="8d428-2255">Tar bort en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="8d428-2255">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="8d428-2256">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="8d428-2256">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="8d428-2257">Återskapar nyckeln för delad åtkomst för en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="8d428-2257">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="8d428-2258">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="8d428-2258">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="8d428-2259">Hämtar de nycklar för delad åtkomst som används för att publicera händelser till en Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="8d428-2259">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="8d428-2260">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="8d428-2260">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="8d428-2261">Skapar ett nytt Azure Event Grid-domänämne.</span><span class="sxs-lookup"><span data-stu-id="8d428-2261">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="8d428-2262">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="8d428-2262">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="8d428-2263">Hämtar information om ett Event Grid-domänämne eller hämtar en lista med alla Event Grid-domänämnen under en specifik Event Grid-domän i nuvarande Azure</span><span class="sxs-lookup"><span data-stu-id="8d428-2263">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="8d428-2264">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="8d428-2264">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="8d428-2265">Tar bort ett befintligt Azure Event Grid-domänämne.</span><span class="sxs-lookup"><span data-stu-id="8d428-2265">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="8d428-2266">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="8d428-2266">Updated cmdlets:</span></span>
    - <span data-ttu-id="8d428-2267">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="8d428-2267">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="8d428-2268">Lägg till nya obligatoriska parametrar för att stödja piping för den nya Event Grid-domänen och Event Grid-domänämnet för att göra det möjligt att skapa nya händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="8d428-2268">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="8d428-2269">Lägg till nya obligatoriska parametrar för att ange det nya Event Grid-domännamnet och/eller namnet på Event Grid-domänämnet för att göra det möjligt att skapa nya händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="8d428-2269">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="8d428-2270">Lägg till ny parameteruppsättningar för domäner och domänämnen för att göra det möjligt att återanvända befintliga parametrar (t.ex. EndPointType, SubjectBeginsWith osv).</span><span class="sxs-lookup"><span data-stu-id="8d428-2270">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="8d428-2271">Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="8d428-2271">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="8d428-2272">Förfallodatum för händelseprenumeration</span><span class="sxs-lookup"><span data-stu-id="8d428-2272">Event subscription expiration date,</span></span>
            - <span data-ttu-id="8d428-2273">Avancerade filterparametrar.</span><span class="sxs-lookup"><span data-stu-id="8d428-2273">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="8d428-2274">Lägg till ny uppräkning för servicebusqueue som mål.</span><span class="sxs-lookup"><span data-stu-id="8d428-2274">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="8d428-2275">Tillåt inte användning av ”Alla” i alternativet -IncludedEventType och ersätt det med</span><span class="sxs-lookup"><span data-stu-id="8d428-2275">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="8d428-2276">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="8d428-2276">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="8d428-2277">Lägg till ny valfria parametrar (Top, ODataQuery och NextLink) för att stödja sidnumrering och filtrering av resultat.</span><span class="sxs-lookup"><span data-stu-id="8d428-2277">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="8d428-2278">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="8d428-2278">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="8d428-2279">Lägg till nya obligatoriska parametrar för att stödja piping för en Event Grid-domän och Event Grid-domänämnen för att göra det möjligt att ta bort befintliga händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="8d428-2279">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="8d428-2280">Lägg till nya obligatoriska parametrar för att ange Event Grid-domännamnet och/eller namnet på Event Grid-domänämnet för att göra det möjligt att ta bort befintliga händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="8d428-2280">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="8d428-2281">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="8d428-2281">Az.FrontDoor</span></span>
* <span data-ttu-id="8d428-2282">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="8d428-2282">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="8d428-2283">Lägg till stöd för transformeringar och nytt värde för automatisk komplettering för operatorer (RegEx)</span><span class="sxs-lookup"><span data-stu-id="8d428-2283">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="8d428-2284">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="8d428-2284">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="8d428-2285">Lägg till nya värden för automatisk komplettering</span><span class="sxs-lookup"><span data-stu-id="8d428-2285">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8d428-2286">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d428-2286">Az.Network</span></span>
* <span data-ttu-id="8d428-2287">Lägg till stöd för resurs för virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="8d428-2287">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="8d428-2288">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="8d428-2288">New cmdlets</span></span>
        - <span data-ttu-id="8d428-2289">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="8d428-2289">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="8d428-2290">Lägg till AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="8d428-2290">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="8d428-2291">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="8d428-2291">New cmdlets</span></span>
        - <span data-ttu-id="8d428-2292">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="8d428-2292">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="8d428-2293">Lägg till PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="8d428-2293">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="8d428-2294">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="8d428-2294">New cmdlets</span></span>
        - <span data-ttu-id="8d428-2295">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="8d428-2295">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="8d428-2296">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="8d428-2296">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="8d428-2297">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="8d428-2297">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="8d428-2298">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="8d428-2298">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="8d428-2299">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8d428-2299">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="8d428-2300">Lägg till PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="8d428-2300">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="8d428-2301">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="8d428-2301">New cmdlets</span></span>
        - <span data-ttu-id="8d428-2302">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="8d428-2302">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="8d428-2303">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="8d428-2303">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="8d428-2304">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="8d428-2304">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="8d428-2305">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="8d428-2305">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="8d428-2306">Nedanstående kommandon för funktionen har uppdaterats: Flaggan UseLocalAzureIpAddress på VpnConnection</span><span class="sxs-lookup"><span data-stu-id="8d428-2306">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="8d428-2307">New-AzVpnConnection har uppdaterats: Den valfria parametern -UseLocalAzureIpAddress har lagts till för att visa att en lokal IP-adress i Azure ska användas som källadress när anslutningen initieras.</span><span class="sxs-lookup"><span data-stu-id="8d428-2307">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="8d428-2308">Set-AzVpnConnection har uppdaterats: Den valfria parametern -UseLocalAzureIpAddress har lagts till för att visa att en lokal IP-adress i Azure ska användas som källadress när anslutningen initieras.</span><span class="sxs-lookup"><span data-stu-id="8d428-2308">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="8d428-2309">Det skrivskyddade fältet PeeredConnections har lagts till i ExpressRoute-peering.</span><span class="sxs-lookup"><span data-stu-id="8d428-2309">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="8d428-2310">Det skrivskyddade fältet GlobalReachEnabled har lagts till i ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="8d428-2310">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="8d428-2311">Ett attribut för icke-bakåtkompatibla ändringar har lagts till för att lyfta fram utfasning av fältet AllowGlobalReach i modellen ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8d428-2311">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="8d428-2312">Problem 8756 har åtgärdats: Fel vid användning av TargetListenerID med AzApplicationGatewayRedirectConfiguration-cmdletar</span><span class="sxs-lookup"><span data-stu-id="8d428-2312">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="8d428-2313">En bugg i New-AzApplicationGatewayPathRuleConfig som gjorde att regeluppsättningen för att återskapa inte kunde anges har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="8d428-2313">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="8d428-2314">Visningen av VirtualNetworkTaps i NetworkInterfaceIpConfiguration har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8d428-2314">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="8d428-2315">Cortex Get-cmdletar för att visa en lista med alla delar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8d428-2315">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="8d428-2316">Funktionen för att skapa VirtualHub-referenser för ExpressRouteGateways och VpnGateway har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8d428-2316">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="8d428-2317">Stöd för tillgänglighetszoner i AzureFirewall och NatGateway har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-2317">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="8d428-2318">Cmdleten Get-AzNetworkServiceTag har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-2318">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="8d428-2319">Lägg till stöd för flera offentliga IP-adresser för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="8d428-2319">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="8d428-2320">Cmdleten New-AzFirewall har uppdaterats:</span><span class="sxs-lookup"><span data-stu-id="8d428-2320">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="8d428-2321">Parametern -PublicIpAddress som accepterar ett eller flera offentliga IP-adressobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-2321">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="8d428-2322">Parametern -VirtualNetwork som accepterar ett virtuellt nätverksobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-2322">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="8d428-2323">Metoderna AddPublicIpAddress och RemovePublicIpAddress har lagts till på brandväggsobjekt – dessa accepterar ett offentligt IP-adressobjekt som indata</span><span class="sxs-lookup"><span data-stu-id="8d428-2323">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="8d428-2324">Inaktuella parametrar -PublicIpName och -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="8d428-2324">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="8d428-2325">Nedanstående kommandon för funktionen har uppdaterats: Ange autentiseringsalternativ för VpnClient AAD till resurser för virtuella nätverksgatewayer.</span><span class="sxs-lookup"><span data-stu-id="8d428-2325">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="8d428-2326">New-AzVirtualNetworkGateway har uppdaterats: De valfria parametrarna AadTenantUri, AadAudienceId och AadIssuerUri för att ange VpnClient AAD-autentiseringsalternativ på en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="8d428-2326">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="8d428-2327">Set-AzVirtualNetworkGateway har uppdaterats: De valfria parametrarna AadTenantUri, AadAudienceId och AadIssuerUri för att ange VpnClient AAD-autentiseringsalternativ på en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="8d428-2327">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="8d428-2328">Set-AzVirtualNetworkGateway har uppdaterats: Den valfria växelparametern RemoveAadAuthentication som tar bort VpnClient AAD-autentiseringsalternativ från en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="8d428-2328">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8d428-2329">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8d428-2329">Az.OperationalInsights</span></span>
* <span data-ttu-id="8d428-2330">Aktivera prisnivån **pergb2018** i kommandot ”New-AzureRmOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="8d428-2330">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="8d428-2331">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d428-2331">Az.Resources</span></span>
* <span data-ttu-id="8d428-2332">Stöd för ytterligare alternativ för att exportera en mall</span><span class="sxs-lookup"><span data-stu-id="8d428-2332">Support for additional Template Export options</span></span>
    - <span data-ttu-id="8d428-2333">Lägg till parametern ”-SkipResourceNameParameterization” till Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8d428-2333">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="8d428-2334">Lägg till parametern ”-SkipAllParameterization” till Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8d428-2334">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="8d428-2335">Lägg till parametern ”-Resource” till Export-AzResourceGroup för exporterad resursfiltrering</span><span class="sxs-lookup"><span data-stu-id="8d428-2335">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8d428-2336">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8d428-2336">Az.ServiceFabric</span></span>
* <span data-ttu-id="8d428-2337">Åtgärda att fel tumavtryck används vid tilläggning av certifikat i ByExistingKeyVault i vissa fall</span><span class="sxs-lookup"><span data-stu-id="8d428-2337">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="8d428-2338">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d428-2338">Az.Sql</span></span>
* <span data-ttu-id="8d428-2339">Åtgärda suffix för lagringsslutpunkt i Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="8d428-2339">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="8d428-2340">Åtgärda att aktivering av Advanced Data Security åsidosätter Advanced Threat Protection-princip</span><span class="sxs-lookup"><span data-stu-id="8d428-2340">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="8d428-2341">Nya cmdletar för Management.Sql som gör att kunderna kan lägga till nycklar för transparent datakryptering (TDE) och ange TDE-skydd för hanterade instanser</span><span class="sxs-lookup"><span data-stu-id="8d428-2341">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="8d428-2342">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8d428-2342">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="8d428-2343">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8d428-2343">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="8d428-2344">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8d428-2344">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="8d428-2345">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="8d428-2345">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="8d428-2346">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="8d428-2346">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8d428-2347">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8d428-2347">Az.Storage</span></span>
* <span data-ttu-id="8d428-2348">Stöd för typerna FileStorage och SkuName Premium_ZRS när lagringskonton skapas</span><span class="sxs-lookup"><span data-stu-id="8d428-2348">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="8d428-2349">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8d428-2349">New-AzStorageAccount</span></span>
* <span data-ttu-id="8d428-2350">Beskrivningen av cmdleten för bloboföränderlighet har förtydligats</span><span class="sxs-lookup"><span data-stu-id="8d428-2350">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="8d428-2351">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="8d428-2351">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8d428-2352">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8d428-2352">Az.Websites</span></span>
* <span data-ttu-id="8d428-2353">Optimerar Get-AzWebAppCertificate för att filtrera efter resursgrupp på servern i stället för klienten</span><span class="sxs-lookup"><span data-stu-id="8d428-2353">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="8d428-2354">Lägger till växlingsparametern -UseDisasterRecovery till Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="8d428-2354">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="8d428-2355">2.2.0 – juni 2019</span><span class="sxs-lookup"><span data-stu-id="8d428-2355">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="8d428-2356">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="8d428-2356">Az.Cdn</span></span>
* <span data-ttu-id="8d428-2357">Uppdaterade cmdletar för att ge stöd för rulesEngine-funktion baserat på API-version 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="8d428-2357">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d428-2358">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d428-2358">Az.Compute</span></span>
* <span data-ttu-id="8d428-2359">Lade till parameter `NoWait` som startar åtgärden och returnerar omedelbart, innan åtgärden har slutförts.</span><span class="sxs-lookup"><span data-stu-id="8d428-2359">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="8d428-2360">Uppdaterade cmdletar:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="8d428-2360">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="8d428-2361">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8d428-2361">Az.EventHub</span></span>
* <span data-ttu-id="8d428-2362">Korrigering för #9231 – Get-AzEventHubNamespace returnerar inga taggar</span><span class="sxs-lookup"><span data-stu-id="8d428-2362">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="8d428-2363">Korrigering för #9230 – Get-AzEventHubNamespace returnerar ResourceGroup istället för ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d428-2363">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8d428-2364">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d428-2364">Az.Network</span></span>
* <span data-ttu-id="8d428-2365">Uppdatera ResourceId och InputObject för NAT-gateway</span><span class="sxs-lookup"><span data-stu-id="8d428-2365">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="8d428-2366">Lägg till alias för ResourceId och InputObject</span><span class="sxs-lookup"><span data-stu-id="8d428-2366">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="8d428-2367">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="8d428-2367">Az.PolicyInsights</span></span>
* <span data-ttu-id="8d428-2368">Åtgärda Null-referensproblem i Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="8d428-2368">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8d428-2369">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8d428-2369">Az.RecoveryServices</span></span>
* <span data-ttu-id="8d428-2370">Minsta kvarhållning för IaaSVM-policy i dagar ändrat till 7 från 1</span><span class="sxs-lookup"><span data-stu-id="8d428-2370">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="8d428-2371">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8d428-2371">Az.ServiceBus</span></span>
* <span data-ttu-id="8d428-2372">Korrigering för ärende #9182 – Get-AzServiceBusNamespace returnerar ResourceGroup istället för ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d428-2372">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8d428-2373">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8d428-2373">Az.ServiceFabric</span></span>
* <span data-ttu-id="8d428-2374">Åtgärda stavfel i felmeddelandet för Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="8d428-2374">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="8d428-2375">Åtgärda saknat tecken i Service Fabric-kommandorader</span><span class="sxs-lookup"><span data-stu-id="8d428-2375">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="8d428-2376">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d428-2376">Az.Sql</span></span>
* <span data-ttu-id="8d428-2377">Lägg till parametern DnsZonePartner för New-AzureSqlInstance-cmdlet för att ge stöd för AutoDr för hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="8d428-2377">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="8d428-2378">Avvecklar cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="8d428-2378">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="8d428-2379">Döp om cmdletar för hotidentifiering till Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="8d428-2379">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="8d428-2380">Parametrarna New-AzSqlInstance -StorageSizeInGB och -LicenseType är nu valfria.</span><span class="sxs-lookup"><span data-stu-id="8d428-2380">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8d428-2381">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8d428-2381">Az.Websites</span></span>
* <span data-ttu-id="8d428-2382">åtgärdar problemet där användningen av Set-AzWebApp och Set-AzWebAppSlot med -WebApp-egenskap tog bort taggarna</span><span class="sxs-lookup"><span data-stu-id="8d428-2382">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="8d428-2383">2.1.0 – maj 2019</span><span class="sxs-lookup"><span data-stu-id="8d428-2383">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="8d428-2384">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8d428-2384">Az.ApiManagement</span></span>
* <span data-ttu-id="8d428-2385">Skapade nya cmdletar för att hantera diagnostik för global- och API-omfång</span><span class="sxs-lookup"><span data-stu-id="8d428-2385">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="8d428-2386">**Get-AzApiManagementDiagnostic** – Skaffa diagnostik konfigurerad för global- eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="8d428-2386">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="8d428-2387">**New-AzApiManagementDiagnostic** – Skapa ny diagnostik för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="8d428-2387">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="8d428-2388">**New-AzApiManagementHttpMessageDiagnostic** – Skapa diagnostikinställning om vilka rubriker som ska loggas och storleken på brödtextbyte</span><span class="sxs-lookup"><span data-stu-id="8d428-2388">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="8d428-2389">**New-AzApiManagementPipelineDiagnosticSetting** – Skapa diagnostikinställningar för inkommande/utgående HTTP-meddelanden till gatewayen.</span><span class="sxs-lookup"><span data-stu-id="8d428-2389">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="8d428-2390">**New-AzApiManagementSamplingSetting** – Skapa samplinginställningar för begäranden/svar för en diagnostik</span><span class="sxs-lookup"><span data-stu-id="8d428-2390">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="8d428-2391">**Remove-AzApiManagementDiagnostic** – Ta bort en diagnostikenhet för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="8d428-2391">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="8d428-2392">**Set-AzApiManagementDiagnostic** – Uppdatera en diagnostikenhet för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="8d428-2392">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="8d428-2393">Skapade nya cmdletar för hantering av cacheminne i ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="8d428-2393">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="8d428-2394">**Get-AzApiManagementCache** – Hämta information om cacheminnet som anges av identifierare eller alla cacheminnen</span><span class="sxs-lookup"><span data-stu-id="8d428-2394">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="8d428-2395">**New-AzApiManagementCache** – Skapa ett nytt default-cacheminne eller cacheminne i en viss Azure-region</span><span class="sxs-lookup"><span data-stu-id="8d428-2395">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="8d428-2396">**Remove-AzApiManagementCache** – Ta bort ett cacheminne</span><span class="sxs-lookup"><span data-stu-id="8d428-2396">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="8d428-2397">**Remove-AzApiManagementCache** – Ta bort ett cacheminne</span><span class="sxs-lookup"><span data-stu-id="8d428-2397">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="8d428-2398">Skapade nya cmdletar för hantering av API-schema</span><span class="sxs-lookup"><span data-stu-id="8d428-2398">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="8d428-2399">**New-AzApiManagementSchema** – Skapa ett nytt schema för ett API</span><span class="sxs-lookup"><span data-stu-id="8d428-2399">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="8d428-2400">**Get-AzApiManagementSchema** – Hämta de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="8d428-2400">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="8d428-2401">**Remove-AzApiManagementSchema** – Ta bort de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="8d428-2401">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="8d428-2402">**Set-AzApiManagementSchema** – Uppdatera de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="8d428-2402">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="8d428-2403">Skapa ny cmdlet för att generera en användartoken.</span><span class="sxs-lookup"><span data-stu-id="8d428-2403">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="8d428-2404">**New-AzApiManagementUserToken** – Skapa en ny användartoken som enligt standardinställning är giltig i 8 timmar. Token för GIT-användaren kan skapas med den här cmdleten./</span><span class="sxs-lookup"><span data-stu-id="8d428-2404">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="8d428-2405">Skapade en ny cmdlet för att hämta nätverksstatus</span><span class="sxs-lookup"><span data-stu-id="8d428-2405">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="8d428-2406">**Get-AzApiManagementNetworkStatus** – Hämta nätverksstatusanslutningen för resurserna som API Management-tjänsten är beroende av.</span><span class="sxs-lookup"><span data-stu-id="8d428-2406">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="8d428-2407">Det här är användbart när du distribuerar ApiManagement-tjänsten i ett virtuellt nätverk och validerar om något beroende är brutet.</span><span class="sxs-lookup"><span data-stu-id="8d428-2407">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="8d428-2408">Uppdaterade cmdlet **New-AzApiManagement** för att hantera ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="8d428-2408">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="8d428-2409">Lade till stöd för den nya SKU:n Consumption</span><span class="sxs-lookup"><span data-stu-id="8d428-2409">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="8d428-2410">Aktiverade stöd för att slå på flaggan EnableClientCertificate för SKU:n Consumption</span><span class="sxs-lookup"><span data-stu-id="8d428-2410">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="8d428-2411">Den nya cmdleten **New-AzApiManagementSslSetting** gör det möjligt att ställa in TLS/SSL-inställningen på ”Backend” och ”Frontend” (serverdel och klientdel).</span><span class="sxs-lookup"><span data-stu-id="8d428-2411">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="8d428-2412">Det här kan också användas till att konfigurera chiffer som 3DES och ServerProtocols som Http2 för Frontend för en ApiManagement-tjänst.</span><span class="sxs-lookup"><span data-stu-id="8d428-2412">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="8d428-2413">Stöd har lagts till för att konfigurera värdnamnet DeveloperPortal på ApiManagement-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="8d428-2413">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="8d428-2414">Uppdaterade cmdletar **Get-AzApiManagementSsoToken** för att ta PsApiManagement-objekt som indata</span><span class="sxs-lookup"><span data-stu-id="8d428-2414">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="8d428-2415">Uppdaterad cmdleten för att visa infogade felmeddelanden</span><span class="sxs-lookup"><span data-stu-id="8d428-2415">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="8d428-2416">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Felkod: Felmeddelande av typen ValidationError: Ett eller flera fält innehåller felaktiga värden: Felinformation:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="8d428-2416">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="8d428-2417">Uppdaterade cmdlet **Export-AzApiManagementApi** för att exportera API:er i OpenApi 3.0-format</span><span class="sxs-lookup"><span data-stu-id="8d428-2417">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="8d428-2418">Uppdaterade cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="8d428-2418">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="8d428-2419">Importera API från dokumentspecifikationen OpenApi 3.0</span><span class="sxs-lookup"><span data-stu-id="8d428-2419">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="8d428-2420">Om du vill åsidosätta egenskapen PsApiManagementSchema specificerad i ett dokument (Swagger, Wadl, Wsdl, OpenApi).</span><span class="sxs-lookup"><span data-stu-id="8d428-2420">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="8d428-2421">Åsidosätta egenskapen ServiceUrl som specificeras i ett dokument.</span><span class="sxs-lookup"><span data-stu-id="8d428-2421">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="8d428-2422">Uppdaterade cmdlet **Get-AzApiManagementPolicy** för att returnera policy i undantaget format av typen icke-XML med rawxml</span><span class="sxs-lookup"><span data-stu-id="8d428-2422">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="8d428-2423">Uppdaterade cmdlet **Set-AzApiManagementPolicy** för att godkänna policy i undantaget format av typen icke-XML med rawxml och XML undantaget med xml</span><span class="sxs-lookup"><span data-stu-id="8d428-2423">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="8d428-2424">Uppdaterad cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="8d428-2424">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="8d428-2425">Konfigurera API med OpenId auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="8d428-2425">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="8d428-2426">Skapa ett API i ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="8d428-2426">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="8d428-2427">Klona ett API med SourceApiId och SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="8d428-2427">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="8d428-2428">Möjlighet att konfigurera SubscriptionRequired i API-omfattningen.</span><span class="sxs-lookup"><span data-stu-id="8d428-2428">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="8d428-2429">Uppdaterad cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="8d428-2429">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="8d428-2430">Konfigurera API med OpenId auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="8d428-2430">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="8d428-2431">Uppdatera ett API till ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="8d428-2431">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="8d428-2432">Möjlighet att konfigurera SubscriptionRequired i API-omfattningen.</span><span class="sxs-lookup"><span data-stu-id="8d428-2432">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="8d428-2433">Uppdaterad cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="8d428-2433">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="8d428-2434">Klona en befintlig version med hjälp av SourceApiRevision (kopiera taggar, produkter, åtgärder och principer).</span><span class="sxs-lookup"><span data-stu-id="8d428-2434">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="8d428-2435">Den nya revisionen antar ApiId från den överordnade instansen.</span><span class="sxs-lookup"><span data-stu-id="8d428-2435">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="8d428-2436">Tillhandahålla ApiRevisionDescription</span><span class="sxs-lookup"><span data-stu-id="8d428-2436">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="8d428-2437">Åsidosätta ServiceUrl vid kloning av ett API.</span><span class="sxs-lookup"><span data-stu-id="8d428-2437">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="8d428-2438">Uppdaterad cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="8d428-2438">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="8d428-2439">Konfigurera AAD eller AADB2C med en Authority</span><span class="sxs-lookup"><span data-stu-id="8d428-2439">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="8d428-2440">Konfigurera SignupPolicy, SigninPolicy, ProfileEditingPolicy och PasswordResetPolicy</span><span class="sxs-lookup"><span data-stu-id="8d428-2440">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="8d428-2441">Uppdaterad cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="8d428-2441">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="8d428-2442">Kompensera för ny SubscriptonModel med Scope och UserId</span><span class="sxs-lookup"><span data-stu-id="8d428-2442">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="8d428-2443">Kompensera för gammal prenumerationsmodell med ProductId och UserId</span><span class="sxs-lookup"><span data-stu-id="8d428-2443">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="8d428-2444">Lägg till funktion för att aktivera AllowTracing på prenumerationsnivå.</span><span class="sxs-lookup"><span data-stu-id="8d428-2444">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="8d428-2445">Uppdaterad cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="8d428-2445">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="8d428-2446">Kompensera för ny SubscriptonModel med Scope och UserId</span><span class="sxs-lookup"><span data-stu-id="8d428-2446">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="8d428-2447">Kompensera för gammal prenumerationsmodell med ProductId och UserId</span><span class="sxs-lookup"><span data-stu-id="8d428-2447">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="8d428-2448">Lägg till funktion för att aktivera AllowTracing på prenumerationsnivå.</span><span class="sxs-lookup"><span data-stu-id="8d428-2448">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="8d428-2449">Uppdaterade följande cmdletar för att acceptera ResourceId som indata</span><span class="sxs-lookup"><span data-stu-id="8d428-2449">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="8d428-2450">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="8d428-2450">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="8d428-2451">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="8d428-2451">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="8d428-2452">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="8d428-2452">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="8d428-2453">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="8d428-2453">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="8d428-2454">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="8d428-2454">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="8d428-2455">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="8d428-2455">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="8d428-2456">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="8d428-2456">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="8d428-2457">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="8d428-2457">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="8d428-2458">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="8d428-2458">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="8d428-2459">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="8d428-2459">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="8d428-2460">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="8d428-2460">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="8d428-2461">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="8d428-2461">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8d428-2462">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8d428-2462">Az.Automation</span></span>
* <span data-ttu-id="8d428-2463">Uppdaterade Get-AzAutomationJobOutputRecord för att hantera postvärden av typen JSON och Text.</span><span class="sxs-lookup"><span data-stu-id="8d428-2463">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="8d428-2464">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="8d428-2464">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="8d428-2465">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="8d428-2465">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="8d428-2466">Ändrade beteende för Start-AzAutomationDscCompilationJob till att bara starta jobbet istället för att vänta på slutförandet.</span><span class="sxs-lookup"><span data-stu-id="8d428-2466">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="8d428-2467">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="8d428-2467">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="8d428-2468">Korrigering för Get-AzAutomationDscNode när using -Name returnerar alla noder.</span><span class="sxs-lookup"><span data-stu-id="8d428-2468">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="8d428-2469">Nu returnerar den endast den matchande noden.</span><span class="sxs-lookup"><span data-stu-id="8d428-2469">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d428-2470">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d428-2470">Az.Compute</span></span>
* <span data-ttu-id="8d428-2471">Lägg till parametrarna ProtectFromScaleIn och ProtectFromScaleSetAction i cmdleten Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="8d428-2471">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="8d428-2472">Nu är standardinställningen att vimpelparametern New-AzVM använder en tillgänglig plats om USA, östra inte stöds</span><span class="sxs-lookup"><span data-stu-id="8d428-2472">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8d428-2473">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8d428-2473">Az.DataLakeStore</span></span>
* <span data-ttu-id="8d428-2474">Uppdatera ADLS-sdk för att använda httpclient, integrera dataplanstestning med Azure-ramverk</span><span class="sxs-lookup"><span data-stu-id="8d428-2474">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8d428-2475">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8d428-2475">Az.Monitor</span></span>
* <span data-ttu-id="8d428-2476">Korrigera felaktiga parameternamn i hjälpexempel</span><span class="sxs-lookup"><span data-stu-id="8d428-2476">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8d428-2477">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d428-2477">Az.Network</span></span>
* <span data-ttu-id="8d428-2478">Lägg till flaggan DisableBgpRoutePropagation i utdata för effektiv routningstabell</span><span class="sxs-lookup"><span data-stu-id="8d428-2478">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="8d428-2479">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="8d428-2479">Updated cmdlet:</span></span>
        - <span data-ttu-id="8d428-2480">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="8d428-2480">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="8d428-2481">Åtgärda dubbelstreck i dokumentationen New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="8d428-2481">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="8d428-2482">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d428-2482">Az.Resources</span></span>
* <span data-ttu-id="8d428-2483">Lägg till ny cmdlet Get-AzureRmDenyAssignment för att hämta tilldelningsnekanden</span><span class="sxs-lookup"><span data-stu-id="8d428-2483">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="8d428-2484">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d428-2484">Az.Sql</span></span>
* <span data-ttu-id="8d428-2485">Döp om Advanced Threat Protection-cmdletar för Advanced Data Security och aktivera Vulnerability Assessment som standard</span><span class="sxs-lookup"><span data-stu-id="8d428-2485">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="8d428-2486">2.0.0 – maj 2019</span><span class="sxs-lookup"><span data-stu-id="8d428-2486">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8d428-2487">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8d428-2487">Az.Accounts</span></span>
* <span data-ttu-id="8d428-2488">Uppdatera autentiseringsbiblioteket för att åtgärda ADFS-problem med autentisering av användarnamn/lösenord</span><span class="sxs-lookup"><span data-stu-id="8d428-2488">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="8d428-2489">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8d428-2489">Az.CognitiveServices</span></span>
* <span data-ttu-id="8d428-2490">Visa endast Bing-ansvarsfriskrivning för Bing-sökningstjänster.</span><span class="sxs-lookup"><span data-stu-id="8d428-2490">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="8d428-2491">Förbättra felmeddelande när det inte går att skapa konton.</span><span class="sxs-lookup"><span data-stu-id="8d428-2491">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d428-2492">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d428-2492">Az.Compute</span></span>
* <span data-ttu-id="8d428-2493">Funktion för närhetsplaceringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="8d428-2493">Proximity placement group feature.</span></span>
    - <span data-ttu-id="8d428-2494">Följande nya cmdletar har lagts till:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="8d428-2494">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="8d428-2495">Den nya parametern ProximityPlacementGroupId har lagts till i följande cmdletar:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="8d428-2495">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="8d428-2496">Parametern StorageAccountType har lagts till i New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="8d428-2496">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="8d428-2497">TargetRegion för New-AzGalleryImageVersion kan innehålla StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="8d428-2497">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="8d428-2498">Växlingsparametern SkipShutdown har lagts till i Stop-AzVM och Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8d428-2498">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="8d428-2499">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="8d428-2499">Breaking changes</span></span>
    - <span data-ttu-id="8d428-2500">Set-AzVMBootDiagnostics har ändrats till Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="8d428-2500">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="8d428-2501">Export-AzLogAnalyticThrottledRequests har ändrats till Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="8d428-2501">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="8d428-2502">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="8d428-2502">Az.DeploymentManager</span></span>
* <span data-ttu-id="8d428-2503">De första allmänt tillgängliga versionerna av cmdletar för Distributionshanteraren i Azure</span><span class="sxs-lookup"><span data-stu-id="8d428-2503">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="8d428-2504">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="8d428-2504">Az.Dns</span></span>
* <span data-ttu-id="8d428-2505">Automatisk delegering av DNS för NameServer</span><span class="sxs-lookup"><span data-stu-id="8d428-2505">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="8d428-2506">Det överordnade zonnamnet kan användas som ytterligare valfri parameter i cmdleten för att skapa DNS-zoner.</span><span class="sxs-lookup"><span data-stu-id="8d428-2506">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="8d428-2507">Lägger till NS-poster för en nyligen skapad underordnad zon i den överordnade zonen.</span><span class="sxs-lookup"><span data-stu-id="8d428-2507">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="8d428-2508">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="8d428-2508">Az.FrontDoor</span></span>
* <span data-ttu-id="8d428-2509">De första allmänt tillgängliga versionerna av cmdletar för Azure FrontDoor</span><span class="sxs-lookup"><span data-stu-id="8d428-2509">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="8d428-2510">Byt namn på WAF-cmdletar så att de omfattar ”Waf”</span><span class="sxs-lookup"><span data-stu-id="8d428-2510">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="8d428-2511">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8d428-2511">Az.HDInsight</span></span>
* <span data-ttu-id="8d428-2512">Två cmdletar har tagits bort:</span><span class="sxs-lookup"><span data-stu-id="8d428-2512">Removed two cmdlets:</span></span>
    - <span data-ttu-id="8d428-2513">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="8d428-2513">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="8d428-2514">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="8d428-2514">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="8d428-2515">En ny cmdlet har lagts till, Set-AzHDInsightGatewayCredential, som ersätter Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="8d428-2515">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="8d428-2516">Uppdatera cmdleten Get-AzHDInsightJobOutput för att skilja mellan läsarrollen och HDInsight-operatörsrollen:</span><span class="sxs-lookup"><span data-stu-id="8d428-2516">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="8d428-2517">Användare med läsarrollen måste uttryckligen ange parametern ”DefaultStorageAccountKey”, annars uppstår fel.</span><span class="sxs-lookup"><span data-stu-id="8d428-2517">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="8d428-2518">Användare med HDInsight-operatörsrollen påverkas inte.</span><span class="sxs-lookup"><span data-stu-id="8d428-2518">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8d428-2519">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8d428-2519">Az.Monitor</span></span>
* <span data-ttu-id="8d428-2520">Nya cmdletar för SQR API (schemalagd frågeregel)</span><span class="sxs-lookup"><span data-stu-id="8d428-2520">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="8d428-2521">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="8d428-2521">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="8d428-2522">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="8d428-2522">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="8d428-2523">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="8d428-2523">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="8d428-2524">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="8d428-2524">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="8d428-2525">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="8d428-2525">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="8d428-2526">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="8d428-2526">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="8d428-2527">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="8d428-2527">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="8d428-2528">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="8d428-2528">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="8d428-2529">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="8d428-2529">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="8d428-2530">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="8d428-2530">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="8d428-2531">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="8d428-2531">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="8d428-2532">[Mer](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information om SQR API</span><span class="sxs-lookup"><span data-stu-id="8d428-2532">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="8d428-2533">Az.Monitor.md har uppdaterats för att omfatta cmdletar för måttbaserade aviseringsregler i GenV2 (inte klassiska)</span><span class="sxs-lookup"><span data-stu-id="8d428-2533">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8d428-2534">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d428-2534">Az.Network</span></span>
* <span data-ttu-id="8d428-2535">Lägg till stöd för NAT Gateway-resurs</span><span class="sxs-lookup"><span data-stu-id="8d428-2535">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="8d428-2536">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="8d428-2536">New cmdlets</span></span>
        - <span data-ttu-id="8d428-2537">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="8d428-2537">New-AzNatGateway</span></span>
        - <span data-ttu-id="8d428-2538">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="8d428-2538">Get-AzNatGateway</span></span>
        - <span data-ttu-id="8d428-2539">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="8d428-2539">Set-AzNatGateway</span></span>
        - <span data-ttu-id="8d428-2540">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="8d428-2540">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="8d428-2541">Uppdaterade cmdletar</span><span class="sxs-lookup"><span data-stu-id="8d428-2541">Updated cmdlets</span></span>
        - <span data-ttu-id="8d428-2542">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="8d428-2542">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="8d428-2543">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="8d428-2543">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="8d428-2544">Nedanstående kommandon för funktionen har uppdaterats: Ange/ta bort anpassade vägar på Brooklyn Gateway.</span><span class="sxs-lookup"><span data-stu-id="8d428-2544">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="8d428-2545">New-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ställa in adressprefix som anpassade vägar för att ange gateway.</span><span class="sxs-lookup"><span data-stu-id="8d428-2545">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="8d428-2546">Set-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ange adressprefix som anpassade vägar för att ange gateway.</span><span class="sxs-lookup"><span data-stu-id="8d428-2546">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="8d428-2547">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="8d428-2547">Az.PolicyInsights</span></span>
* <span data-ttu-id="8d428-2548">Stöd för att fråga efter information om principutvärdering.</span><span class="sxs-lookup"><span data-stu-id="8d428-2548">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="8d428-2549">Lägg till parametern ”-Expand” för Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="8d428-2549">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="8d428-2550">Stöd för -Expand PolicyEvaluationDetails.</span><span class="sxs-lookup"><span data-stu-id="8d428-2550">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8d428-2551">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8d428-2551">Az.RecoveryServices</span></span>
* <span data-ttu-id="8d428-2552">Stöd för att dela prenumeration mellan Azure och Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="8d428-2552">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="8d428-2553">Markering av kommande icke-bakåtkompatibla ändringar för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="8d428-2553">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="8d428-2554">Korrigering för återställningsplan och åtgärdsplan i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="8d428-2554">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="8d428-2555">Korrigering för mappning av uppdateringsnätverk i Azure Site Recovery för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="8d428-2555">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="8d428-2556">Korrigering för instruktioner för uppdateringsskydd i Azure Site Recovery för Azure till Azure för hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="8d428-2556">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="8d428-2557">Andra mindre korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="8d428-2557">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="8d428-2558">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="8d428-2558">Az.Relay</span></span>
* <span data-ttu-id="8d428-2559">Korrigera stavfel i kundriktade meddelanden</span><span class="sxs-lookup"><span data-stu-id="8d428-2559">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="8d428-2560">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8d428-2560">Az.ServiceBus</span></span>
* <span data-ttu-id="8d428-2561">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="8d428-2561">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8d428-2562">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8d428-2562">Az.Storage</span></span>
* <span data-ttu-id="8d428-2563">Uppgradera till lagringsklientbiblioteket 10.0.1 (namnområdet för alla objekt från detta SDK ändras från ”Microsoft.WindowsAzure.Storage. *till ”Microsoft.Azure.Storage.* ”)</span><span class="sxs-lookup"><span data-stu-id="8d428-2563">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage. *' to 'Microsoft.Azure.Storage.* ')</span></span>
* <span data-ttu-id="8d428-2564">Uppgradera till Microsoft.Azure.Management.Storage 11.0.0 för att stödja den nya API-versionen 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="8d428-2564">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="8d428-2565">Standardlagringskontot i Skapa lagringskonto ändras från ”Storage” till ”StorageV2”</span><span class="sxs-lookup"><span data-stu-id="8d428-2565">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="8d428-2566">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8d428-2566">New-AzStorageAccount</span></span>
* <span data-ttu-id="8d428-2567">Ändra lagringskontots cmdlet-utdata Sku.Name för att passa med indata-SkuName genom att lägga till ”-”. Till exempel ändras ”StandardLRS” till ”Standard_LRS”</span><span class="sxs-lookup"><span data-stu-id="8d428-2567">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="8d428-2568">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8d428-2568">New-AzStorageAccount</span></span>
    - <span data-ttu-id="8d428-2569">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8d428-2569">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="8d428-2570">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8d428-2570">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8d428-2571">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8d428-2571">Az.Websites</span></span>
* <span data-ttu-id="8d428-2572">Egenskapen ”typ” konfigureras nu för PSSite-objekt som returneras av Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8d428-2572">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="8d428-2573">Get-AzWebApp\*Metrics och Get-AzAppServicePlanMetrics markeras som inaktuella</span><span class="sxs-lookup"><span data-stu-id="8d428-2573">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="8d428-2574">1.8.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="8d428-2574">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="8d428-2575">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="8d428-2575">Highlights since the last major release</span></span>
* <span data-ttu-id="8d428-2576">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="8d428-2576">General availability of `Az` module</span></span>
* <span data-ttu-id="8d428-2577">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="8d428-2577">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="8d428-2578">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="8d428-2578">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="8d428-2579">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-2579">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="8d428-2580">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-2580">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="8d428-2581">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-2581">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="8d428-2582">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="8d428-2582">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="8d428-2583">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8d428-2583">Az.Accounts</span></span>
* <span data-ttu-id="8d428-2584">Uppdatera Uninstall-AzureRm för att ta bort moduler i Mac på ett korrekt sätt</span><span class="sxs-lookup"><span data-stu-id="8d428-2584">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="8d428-2585">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="8d428-2585">Az.Batch</span></span>
* <span data-ttu-id="8d428-2586">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8d428-2586">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="8d428-2587">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="8d428-2587">Az.Cdn</span></span>
* <span data-ttu-id="8d428-2588">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8d428-2588">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="8d428-2589">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8d428-2589">Az.CognitiveServices</span></span>
* <span data-ttu-id="8d428-2590">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8d428-2590">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d428-2591">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d428-2591">Az.Compute</span></span>
* <span data-ttu-id="8d428-2592">Åtgärda problem med AEM-installationen om resurs-ID:n för diskar innehåller resourcegroups i gemener i resurs-ID:n</span><span class="sxs-lookup"><span data-stu-id="8d428-2592">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="8d428-2593">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8d428-2593">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8d428-2594">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="8d428-2594">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8d428-2595">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8d428-2595">Az.DataFactory</span></span>
* <span data-ttu-id="8d428-2596">Lägg till SsisProperties om NodeCount inte är null för hanterad integreringskörning.</span><span class="sxs-lookup"><span data-stu-id="8d428-2596">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8d428-2597">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8d428-2597">Az.DataLakeStore</span></span>
* <span data-ttu-id="8d428-2598">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8d428-2598">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="8d428-2599">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="8d428-2599">Az.EventGrid</span></span>
* <span data-ttu-id="8d428-2600">Hjälptexten för slutpunkten har uppdaterats för att visa att resurser ska skapas innan cmdletarna för att skapa/uppdatera händelseprenumerationer används.</span><span class="sxs-lookup"><span data-stu-id="8d428-2600">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="8d428-2601">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8d428-2601">Az.EventHub</span></span>
* <span data-ttu-id="8d428-2602">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="8d428-2602">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="8d428-2603">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8d428-2603">Az.HDInsight</span></span>
* <span data-ttu-id="8d428-2604">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8d428-2604">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8d428-2605">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8d428-2605">Az.IotHub</span></span>
* <span data-ttu-id="8d428-2606">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8d428-2606">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8d428-2607">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8d428-2607">Az.KeyVault</span></span>
* <span data-ttu-id="8d428-2608">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8d428-2608">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8d428-2609">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="8d428-2609">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="8d428-2610">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="8d428-2610">Az.MachineLearning</span></span>
* <span data-ttu-id="8d428-2611">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8d428-2611">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="8d428-2612">Az.Media</span><span class="sxs-lookup"><span data-stu-id="8d428-2612">Az.Media</span></span>
* <span data-ttu-id="8d428-2613">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8d428-2613">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8d428-2614">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8d428-2614">Az.Monitor</span></span>
  * <span data-ttu-id="8d428-2615">Nya cmdletar för måttbaserad aviseringsregel i GenV2 (inte klassisk)</span><span class="sxs-lookup"><span data-stu-id="8d428-2615">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="8d428-2616">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="8d428-2616">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="8d428-2617">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="8d428-2617">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="8d428-2618">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="8d428-2618">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="8d428-2619">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="8d428-2619">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="8d428-2620">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="8d428-2620">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="8d428-2621">Monitor SDK har uppdaterats till version 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="8d428-2621">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8d428-2622">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d428-2622">Az.Network</span></span>
* <span data-ttu-id="8d428-2623">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8d428-2623">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8d428-2624">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="8d428-2624">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="8d428-2625">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="8d428-2625">Az.NotificationHubs</span></span>
* <span data-ttu-id="8d428-2626">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8d428-2626">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8d428-2627">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8d428-2627">Az.OperationalInsights</span></span>
* <span data-ttu-id="8d428-2628">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8d428-2628">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="8d428-2629">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="8d428-2629">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="8d428-2630">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8d428-2630">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8d428-2631">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8d428-2631">Az.RecoveryServices</span></span>
* <span data-ttu-id="8d428-2632">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8d428-2632">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8d428-2633">Tabellformatet för SQL i virtuella Azure-datorer har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="8d428-2633">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="8d428-2634">En alternativ metod för att hämta platser i AzureFileShare har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-2634">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="8d428-2635">ScheduleRunDays i SchedulePolicy-objekt har uppdaterats enligt tidszon</span><span class="sxs-lookup"><span data-stu-id="8d428-2635">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="8d428-2636">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="8d428-2636">Az.RedisCache</span></span>
* <span data-ttu-id="8d428-2637">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8d428-2637">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8d428-2638">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d428-2638">Az.Resources</span></span>
* <span data-ttu-id="8d428-2639">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="8d428-2639">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="8d428-2640">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d428-2640">Az.Sql</span></span>
* <span data-ttu-id="8d428-2641">Ersätt Monitor SDK-beroende med vanlig kod</span><span class="sxs-lookup"><span data-stu-id="8d428-2641">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="8d428-2642">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8d428-2642">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8d428-2643">Förbättrad process för klassificering av flera kolumner.</span><span class="sxs-lookup"><span data-stu-id="8d428-2643">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="8d428-2644">Inkludera SKU-egenskaper (SKU-namn, serie, kapacitet) i svaret från Get-AzSqlServerServiceObjective och formatera som tabell som standard.</span><span class="sxs-lookup"><span data-stu-id="8d428-2644">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="8d428-2645">Möjlighet att använda Get-AzSqlServerServiceObjective efter plats utan att behöva en redan befintlig server i regionen.</span><span class="sxs-lookup"><span data-stu-id="8d428-2645">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="8d428-2646">Stöd för tidszonsparametern när hanterade instanser skapas.</span><span class="sxs-lookup"><span data-stu-id="8d428-2646">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="8d428-2647">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="8d428-2647">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8d428-2648">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8d428-2648">Az.Websites</span></span>
* <span data-ttu-id="8d428-2649">åtgärdar Set-AzWebApp och Set-AzWebAppSlot så att de inte tar bort taggar vid körning</span><span class="sxs-lookup"><span data-stu-id="8d428-2649">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="8d428-2650">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="8d428-2650">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8d428-2651">SDK för WebSites har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="8d428-2651">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="8d428-2652">Egenskapen AdminSiteName har tagits bort från PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="8d428-2652">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="8d428-2653">1.7.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="8d428-2653">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="8d428-2654">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="8d428-2654">Highlights since the last major release</span></span>
* <span data-ttu-id="8d428-2655">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="8d428-2655">General availability of `Az` module</span></span>
* <span data-ttu-id="8d428-2656">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="8d428-2656">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="8d428-2657">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="8d428-2657">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="8d428-2658">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-2658">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="8d428-2659">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-2659">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="8d428-2660">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-2660">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="8d428-2661">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="8d428-2661">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="8d428-2662">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8d428-2662">Az.Accounts</span></span>
* <span data-ttu-id="8d428-2663">Add-AzEnvironment och Set-AzEnvironment har uppdaterats för att godkänna parametern AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="8d428-2663">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="8d428-2664">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8d428-2664">Az.AnalysisServices</span></span>
* <span data-ttu-id="8d428-2665">ServiceClient används i cmdletar för dataplan och den ursprungliga autentiseringslogiken har tagits bort</span><span class="sxs-lookup"><span data-stu-id="8d428-2665">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="8d428-2666">Add-AzureASAccount används för omslutning av Connect-AzAccount för att undvika en icke-bakåtkompatibel ändring</span><span class="sxs-lookup"><span data-stu-id="8d428-2666">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8d428-2667">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8d428-2667">Az.Automation</span></span>
* <span data-ttu-id="8d428-2668">Buggen för cmdleten New-AzAutomationSoftwareUpdateConfiguration för inkluderingar har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="8d428-2668">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="8d428-2669">Nu bör parametern IncludedKbNumber och IncludedPackageNameMask fungera.</span><span class="sxs-lookup"><span data-stu-id="8d428-2669">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="8d428-2670">Felkorrigering för dynamiska grupper i uppdateringshanteringen för azure automation</span><span class="sxs-lookup"><span data-stu-id="8d428-2670">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d428-2671">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d428-2671">Az.Compute</span></span>
* <span data-ttu-id="8d428-2672">Lägg till parametern HyperVGeneration i New-AzDiskConfig och New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="8d428-2672">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="8d428-2673">Tillåt att virtuella datorer skapas med galleribilder från andra klientorganisationer.</span><span class="sxs-lookup"><span data-stu-id="8d428-2673">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="8d428-2674">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="8d428-2674">Az.ContainerInstance</span></span>
* <span data-ttu-id="8d428-2675">Ett problem har åtgärdats i parametern -Command för New-AzContainerGroup som lade till ett avslutande tomt argument</span><span class="sxs-lookup"><span data-stu-id="8d428-2675">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8d428-2676">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8d428-2676">Az.DataFactory</span></span>
* <span data-ttu-id="8d428-2677">ADF .Net SDK-versionen har uppdaterats till 3.0.2</span><span class="sxs-lookup"><span data-stu-id="8d428-2677">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="8d428-2678">Cmdleten Set-AzDataFactoryV2 har uppdaterats med extra parametrar för inställningar som rör RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="8d428-2678">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8d428-2679">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d428-2679">Az.Resources</span></span>
* <span data-ttu-id="8d428-2680">Förbättra hanteringen av providrar för Get-AzResource när parametrarna -ResourceId eller -ResourceGroupName, -Name och -ResourceType tillhandahålls</span><span class="sxs-lookup"><span data-stu-id="8d428-2680">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="8d428-2681">Förbättra felhanteringen för ”Test-AzDeployment” och ”Test-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="8d428-2681">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="8d428-2682">Hantera fel utanför distributionsvalideringen och ta med dem i kommandoutdata istället</span><span class="sxs-lookup"><span data-stu-id="8d428-2682">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="8d428-2683">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="8d428-2683">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="8d428-2684">Lägg till växlingsparametern -IgnoreDynamicParameters till en uppsättning av cmdletar för distribution för att hoppa över fråga i skript och jobbscenarier</span><span class="sxs-lookup"><span data-stu-id="8d428-2684">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="8d428-2685">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="8d428-2685">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="8d428-2686">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d428-2686">Az.Sql</span></span>
* <span data-ttu-id="8d428-2687">Stöd för dataklassificering av databaser.</span><span class="sxs-lookup"><span data-stu-id="8d428-2687">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8d428-2688">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8d428-2688">Az.Storage</span></span>
* <span data-ttu-id="8d428-2689">Rapportera detaljfel när lagringskontext skapas med parametern -UseConnectedAccount, men utan inloggning på Azure-kontot</span><span class="sxs-lookup"><span data-stu-id="8d428-2689">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="8d428-2690">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="8d428-2690">New-AzStorageContext</span></span>
* <span data-ttu-id="8d428-2691">Stöd för att hantera Blob Service-egenskaper för ett angivet lagringskonto med API:et för hanteringsplan</span><span class="sxs-lookup"><span data-stu-id="8d428-2691">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="8d428-2692">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="8d428-2692">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="8d428-2693">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="8d428-2693">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="8d428-2694">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8d428-2694">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="8d428-2695">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8d428-2695">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="8d428-2696">Stöd för -AsJob-cmdletar för att ladda upp och ladda ned blobar och filer</span><span class="sxs-lookup"><span data-stu-id="8d428-2696">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="8d428-2697">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="8d428-2697">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="8d428-2698">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="8d428-2698">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="8d428-2699">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="8d428-2699">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="8d428-2700">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="8d428-2700">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="8d428-2701">1.6.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="8d428-2701">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="8d428-2702">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="8d428-2702">Highlights since the last major release</span></span>
* <span data-ttu-id="8d428-2703">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="8d428-2703">General availability of `Az` module</span></span>
* <span data-ttu-id="8d428-2704">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="8d428-2704">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="8d428-2705">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="8d428-2705">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="8d428-2706">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-2706">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="8d428-2707">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-2707">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="8d428-2708">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-2708">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="8d428-2709">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="8d428-2709">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8d428-2710">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8d428-2710">Az.Automation</span></span>
* <span data-ttu-id="8d428-2711">Azure Automation – ändring av uppdateringshantering för stöd för de nya funktionerna:</span><span class="sxs-lookup"><span data-stu-id="8d428-2711">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="8d428-2712">Dynamisk gruppering</span><span class="sxs-lookup"><span data-stu-id="8d428-2712">Dynamic grouping</span></span>
    * <span data-ttu-id="8d428-2713">För-/efterskrift</span><span class="sxs-lookup"><span data-stu-id="8d428-2713">Pre-Post script</span></span>
    * <span data-ttu-id="8d428-2714">Inställning för omstart</span><span class="sxs-lookup"><span data-stu-id="8d428-2714">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d428-2715">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d428-2715">Az.Compute</span></span>
* <span data-ttu-id="8d428-2716">Åtgärda problem med sökvägsmatchning i Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="8d428-2716">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="8d428-2717">Uppdatera Compute-klientbibliotek till 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="8d428-2717">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8d428-2718">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8d428-2718">Az.KeyVault</span></span>
* <span data-ttu-id="8d428-2719">Stöd för jokertecken för KeyVault-cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-2719">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8d428-2720">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d428-2720">Az.Network</span></span>
* <span data-ttu-id="8d428-2721">Lägg till stöd för Threat Intelligence för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="8d428-2721">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="8d428-2722">Lägg till resurs för brandväggsprincip på översta nivå och anpassade regler för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="8d428-2722">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8d428-2723">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8d428-2723">Az.RecoveryServices</span></span>
* <span data-ttu-id="8d428-2724">SnapshotRetentionInDays har lagts till i Azure-principen för virtuella datorer för stöd av Instant RP</span><span class="sxs-lookup"><span data-stu-id="8d428-2724">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="8d428-2725">Pipe-stöd för avregistrering av container har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-2725">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="8d428-2726">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d428-2726">Az.Resources</span></span>
* <span data-ttu-id="8d428-2727">Uppdatera stöd för jokertecken för Get-AzResource och Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8d428-2727">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="8d428-2728">Uppdatera autentiseringsuppgifter som används vid allmänna anrop till ARM</span><span class="sxs-lookup"><span data-stu-id="8d428-2728">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="8d428-2729">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d428-2729">Az.Sql</span></span>
* <span data-ttu-id="8d428-2730">Cmdlet-parametern (ExcludeDetectionType) för Hotidentifiering ändrades från DetectionType till sträng[] för att framtidssäkra den när nya DetectionTypes läggs till, och även för att stödja automatisk ifyllning.</span><span class="sxs-lookup"><span data-stu-id="8d428-2730">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8d428-2731">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8d428-2731">Az.Storage</span></span>
* <span data-ttu-id="8d428-2732">Stöd för att hämta/ange/ta bort hanteringsprincip på ett lagringskonto</span><span class="sxs-lookup"><span data-stu-id="8d428-2732">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="8d428-2733">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="8d428-2733">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="8d428-2734">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="8d428-2734">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="8d428-2735">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="8d428-2735">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="8d428-2736">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="8d428-2736">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="8d428-2737">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="8d428-2737">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="8d428-2738">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="8d428-2738">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8d428-2739">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8d428-2739">Az.Websites</span></span>
* <span data-ttu-id="8d428-2740">Åtgärda fel med ARM-mall som avbryter kloning av alla platser med 'New-AzWebApp -IncludeSourceWebAppSlots'</span><span class="sxs-lookup"><span data-stu-id="8d428-2740">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="8d428-2741">1.5.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="8d428-2741">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8d428-2742">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8d428-2742">Az.Accounts</span></span>
* <span data-ttu-id="8d428-2743">Lägg till kommandot Register-AzModule för stöd för AutoRest-genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="8d428-2743">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="8d428-2744">Uppdatera exempel för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="8d428-2744">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8d428-2745">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8d428-2745">Az.Automation</span></span>
* <span data-ttu-id="8d428-2746">Problem med att hämta vissa månadsscheman i flera Azure Automation-cmdletar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8d428-2746">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="8d428-2747">Åtgärda problem med att Get-AzAutomationDscNode bara returnerar de 20 översta noderna.</span><span class="sxs-lookup"><span data-stu-id="8d428-2747">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="8d428-2748">Nu returneras alla noder</span><span class="sxs-lookup"><span data-stu-id="8d428-2748">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="8d428-2749">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="8d428-2749">Az.Cdn</span></span>
* <span data-ttu-id="8d428-2750">Nya Powershell-cmdletar för att aktivera/inaktivera anpassade domän-HTTPS har lagts till och de gamla har gjorts inaktuella</span><span class="sxs-lookup"><span data-stu-id="8d428-2750">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d428-2751">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d428-2751">Az.Compute</span></span>
* <span data-ttu-id="8d428-2752">Lägg till stöd för jokertecken för Get-cmdletar</span><span class="sxs-lookup"><span data-stu-id="8d428-2752">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8d428-2753">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8d428-2753">Az.DataFactory</span></span>
* <span data-ttu-id="8d428-2754">ADF .Net SDK-versionen har uppdaterats till 3.0.1</span><span class="sxs-lookup"><span data-stu-id="8d428-2754">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="8d428-2755">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="8d428-2755">Az.LogicApp</span></span>
* <span data-ttu-id="8d428-2756">Åtgärda problemet med att ListWorkflows endast hämtar den första sidan med resultat</span><span class="sxs-lookup"><span data-stu-id="8d428-2756">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8d428-2757">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d428-2757">Az.Network</span></span>
* <span data-ttu-id="8d428-2758">Lägg till stöd för jokertecken för Network-cmdletar</span><span class="sxs-lookup"><span data-stu-id="8d428-2758">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8d428-2759">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8d428-2759">Az.RecoveryServices</span></span>
* <span data-ttu-id="8d428-2760">Stöd har lagts till för SQL Server i virtuella Azure-datorer</span><span class="sxs-lookup"><span data-stu-id="8d428-2760">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="8d428-2761">SDK-uppdatering</span><span class="sxs-lookup"><span data-stu-id="8d428-2761">SDK Update</span></span>
* <span data-ttu-id="8d428-2762">Get-ProtectableItem-incheckning i VMappContainer har tagits bort</span><span class="sxs-lookup"><span data-stu-id="8d428-2762">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="8d428-2763">Name och ServerName har lagts till som parametrar för Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="8d428-2763">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="8d428-2764">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d428-2764">Az.Resources</span></span>
* <span data-ttu-id="8d428-2765">Lägg till parametern `-TemplateObject` i cmdletar för distribution</span><span class="sxs-lookup"><span data-stu-id="8d428-2765">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="8d428-2766">Mer information här: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="8d428-2766">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="8d428-2767">Åtgärda problem med piping av resultatet i `Get-AzResource` till `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="8d428-2767">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="8d428-2768">Mer information här: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="8d428-2768">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="8d428-2769">Åtgärda problem med ändring av JSON-datatyp när `Set-AzResource` körs</span><span class="sxs-lookup"><span data-stu-id="8d428-2769">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="8d428-2770">Mer information här: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="8d428-2770">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="8d428-2771">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d428-2771">Az.Sql</span></span>
* <span data-ttu-id="8d428-2772">AuditingEndpointsCommunicator uppdateras.</span><span class="sxs-lookup"><span data-stu-id="8d428-2772">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="8d428-2773">Åtgärdar beteendet hos ett gränsscenario när nya diagnostikinställningar skapas.</span><span class="sxs-lookup"><span data-stu-id="8d428-2773">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8d428-2774">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8d428-2774">Az.Storage</span></span>
* <span data-ttu-id="8d428-2775">Stöd för BlockBlobStorage när Storage-konto skapas      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8d428-2775">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="8d428-2776">1.4.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="8d428-2776">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="8d428-2777">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8d428-2777">Az.AnalysisServices</span></span>
* <span data-ttu-id="8d428-2778">Inaktuell AddAzureASAccount-cmdlet</span><span class="sxs-lookup"><span data-stu-id="8d428-2778">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8d428-2779">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8d428-2779">Az.Automation</span></span>
* <span data-ttu-id="8d428-2780">Hjälpen för Import-AzAutomationDscNodeConfiguration har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="8d428-2780">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="8d428-2781">Konfigurationsnamnsvalidering har lagts till i cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="8d428-2781">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="8d428-2782">Förbättrad felhantering för cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="8d428-2782">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="8d428-2783">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8d428-2783">Az.CognitiveServices</span></span>
* <span data-ttu-id="8d428-2784">CustomSubdomainName har lagts till som en ny valfri parameter för New-AzCognitiveServicesAccount, som används för att ange underdomän för resursen.</span><span class="sxs-lookup"><span data-stu-id="8d428-2784">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d428-2785">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d428-2785">Az.Compute</span></span>
* <span data-ttu-id="8d428-2786">Problemet med ID-parameteruppsättningar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8d428-2786">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="8d428-2787">Get-AzVMExtension har uppdaterats så att alla installerade tillägg visas om parametern Name inte har angetts</span><span class="sxs-lookup"><span data-stu-id="8d428-2787">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="8d428-2788">Parametrarna Tag och ResourceId har lagts till i cmdleten Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="8d428-2788">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="8d428-2789">Get-AzVmssVM utan instans-ID och med InstanceView kan visa virtuella VMSS-datorer med instansvyn.</span><span class="sxs-lookup"><span data-stu-id="8d428-2789">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8d428-2790">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8d428-2790">Az.DataLakeStore</span></span>
* <span data-ttu-id="8d428-2791">Cmdletar har lagts till för uppräkning och återställning av borttagna objekt i ADL</span><span class="sxs-lookup"><span data-stu-id="8d428-2791">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="8d428-2792">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8d428-2792">Az.EventHub</span></span>
* <span data-ttu-id="8d428-2793">Ny boolesk egenskap SkipEmptyArchives har lagts till i Skip Empty Archives i CaptureDescription-klassen i Eventhub</span><span class="sxs-lookup"><span data-stu-id="8d428-2793">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8d428-2794">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8d428-2794">Az.KeyVault</span></span>
* <span data-ttu-id="8d428-2795">Taggning i Set-AzKeyVaultSecret har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8d428-2795">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="8d428-2796">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="8d428-2796">Az.LogicApp</span></span>
* <span data-ttu-id="8d428-2797">Grundläggande SKU har lagts till för Integrationskonton</span><span class="sxs-lookup"><span data-stu-id="8d428-2797">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="8d428-2798">XSLT 2.0, XSLT 3.0 och Flytande mappningstyper har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-2798">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="8d428-2799">Nya cmdletar för integrationskontosammansättningar</span><span class="sxs-lookup"><span data-stu-id="8d428-2799">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="8d428-2800">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="8d428-2800">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="8d428-2801">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="8d428-2801">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="8d428-2802">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="8d428-2802">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="8d428-2803">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="8d428-2803">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="8d428-2804">Nya cmdletar för batchkonfiguration för integrationskonto</span><span class="sxs-lookup"><span data-stu-id="8d428-2804">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="8d428-2805">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="8d428-2805">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="8d428-2806">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="8d428-2806">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="8d428-2807">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="8d428-2807">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="8d428-2808">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="8d428-2808">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="8d428-2809">Logic App-SDK har uppdaterats till version 4.1.0</span><span class="sxs-lookup"><span data-stu-id="8d428-2809">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8d428-2810">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8d428-2810">Az.Monitor</span></span>
* <span data-ttu-id="8d428-2811">Hjälpen för Get-AzMetric har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="8d428-2811">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8d428-2812">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d428-2812">Az.Network</span></span>
* <span data-ttu-id="8d428-2813">Hjälpexempel för Add-AzApplicationGatewayCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-2813">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8d428-2814">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8d428-2814">Az.OperationalInsights</span></span>
* <span data-ttu-id="8d428-2815">Ytterligare stöd för datakällorna New och Get ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="8d428-2815">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="8d428-2816">Ny ApplicationInsights-typ har lagts till för att ge stöd för ”Get specific” och ”Get all” för ApplicationInsights-datakällor för angiven arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="8d428-2816">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="8d428-2817">Cmdleten New-AzOperationalInsightsApplicationInsightsDataSource har lagts till för att skapa datakälla med angivna parametrar för Application Insights-resurs: subscription Id, resourceGroupName och name.</span><span class="sxs-lookup"><span data-stu-id="8d428-2817">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8d428-2818">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d428-2818">Az.Resources</span></span>
* <span data-ttu-id="8d428-2819">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="8d428-2819">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="8d428-2820">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="8d428-2820">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="8d428-2821">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="8d428-2821">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="8d428-2822">Fel som gör att KeyCredentials inte kan skapas upprepade gånger har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8d428-2822">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="8d428-2823">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d428-2823">Az.Sql</span></span>
* <span data-ttu-id="8d428-2824">Lägg till stöd för hyperskalanivån för SQL DB</span><span class="sxs-lookup"><span data-stu-id="8d428-2824">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="8d428-2825">Ett fel har åtgärdats där återställningen kunde misslyckas på grund av onödiga inställningsegenskaper i restore-förfrågan</span><span class="sxs-lookup"><span data-stu-id="8d428-2825">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8d428-2826">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8d428-2826">Az.Websites</span></span>
* <span data-ttu-id="8d428-2827">Rätt exempel i Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="8d428-2827">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="8d428-2828">1.3.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="8d428-2828">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8d428-2829">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8d428-2829">Az.Accounts</span></span>
* <span data-ttu-id="8d428-2830">Uppdatera till den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="8d428-2830">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="8d428-2831">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8d428-2831">Az.AnalysisServices</span></span>
<span data-ttu-id="8d428-2832">Allmän tillgänglighet för Az.AnalysisServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="8d428-2832">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d428-2833">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d428-2833">Az.Compute</span></span>
* <span data-ttu-id="8d428-2834">AEM-tillägg: Lägg till stöd för UltraSSD-, P60-, P70- och P80-diskar</span><span class="sxs-lookup"><span data-stu-id="8d428-2834">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="8d428-2835">Uppdatera hjälpbeskrivning för Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="8d428-2835">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="8d428-2836">Uppdatera hjälpbeskrivning och exempel för Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="8d428-2836">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8d428-2837">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8d428-2837">Az.RecoveryServices</span></span>
<span data-ttu-id="8d428-2838">Allmän tillgänglighet för Az.RecoveryServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="8d428-2838">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8d428-2839">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d428-2839">Az.Resources</span></span>
* <span data-ttu-id="8d428-2840">Korrigera taggar för resursgrupper</span><span class="sxs-lookup"><span data-stu-id="8d428-2840">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="8d428-2841">Mer information här: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="8d428-2841">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="8d428-2842">Åtgärda problem där `Get-AzureRmRoleAssignment` inte respekterar -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="8d428-2842">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="8d428-2843">Mer information här: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="8d428-2843">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="8d428-2844">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d428-2844">Az.Sql</span></span>
* <span data-ttu-id="8d428-2845">Lägga till Get/Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8d428-2845">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="8d428-2846">Åtgärda problem där ett nullref-undantag uppstår när du kör SQL-cmdletar och inte är inloggad på ett Azure-konto</span><span class="sxs-lookup"><span data-stu-id="8d428-2846">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="8d428-2847">Åtgärda nullref-undantag i Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="8d428-2847">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="8d428-2848">1.2.1 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="8d428-2848">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8d428-2849">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8d428-2849">Az.Accounts</span></span>
* <span data-ttu-id="8d428-2850">Version med rätt version av autentisering</span><span class="sxs-lookup"><span data-stu-id="8d428-2850">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="8d428-2851">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8d428-2851">Az.AnalysisServices</span></span>
* <span data-ttu-id="8d428-2852">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="8d428-2852">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8d428-2853">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8d428-2853">Az.RecoveryServices</span></span>
* <span data-ttu-id="8d428-2854">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="8d428-2854">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="8d428-2855">1.2.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="8d428-2855">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8d428-2856">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8d428-2856">Az.Accounts</span></span>
* <span data-ttu-id="8d428-2857">Lägga till interaktiv autentisering och autentisering med användarnamn/lösenord för endast Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="8d428-2857">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="8d428-2858">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="8d428-2858">Update incorrect online help URLs</span></span>
* <span data-ttu-id="8d428-2859">Lägga till varningsmeddelande i PS Core för Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="8d428-2859">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="8d428-2860">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="8d428-2860">Az.Aks</span></span>
* <span data-ttu-id="8d428-2861">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="8d428-2861">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8d428-2862">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8d428-2862">Az.Automation</span></span>
* <span data-ttu-id="8d428-2863">Stöd för Python 2-runbookflöden har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-2863">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="8d428-2864">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="8d428-2864">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="8d428-2865">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="8d428-2865">Az.Cdn</span></span>
* <span data-ttu-id="8d428-2866">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="8d428-2866">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d428-2867">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d428-2867">Az.Compute</span></span>
* <span data-ttu-id="8d428-2868">Lägga till cmdleten Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="8d428-2868">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="8d428-2869">Lägga till TempDisk-parameter i Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8d428-2869">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="8d428-2870">Korrigera varningsmeddelande för New-AzVM</span><span class="sxs-lookup"><span data-stu-id="8d428-2870">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="8d428-2871">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8d428-2871">Az.ContainerRegistry</span></span>
* <span data-ttu-id="8d428-2872">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="8d428-2872">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8d428-2873">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8d428-2873">Az.DataFactory</span></span>
* <span data-ttu-id="8d428-2874">ADF .Net SDK-versionen har uppdaterats till 3.0.0</span><span class="sxs-lookup"><span data-stu-id="8d428-2874">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8d428-2875">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8d428-2875">Az.DataLakeStore</span></span>
* <span data-ttu-id="8d428-2876">Åtgärda problem med ADLS-slutpunkt vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="8d428-2876">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="8d428-2877">Mer information här: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="8d428-2877">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="8d428-2878">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="8d428-2878">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8d428-2879">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8d428-2879">Az.IotHub</span></span>
* <span data-ttu-id="8d428-2880">Lägga till kodningsformat i cmdleten Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="8d428-2880">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8d428-2881">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8d428-2881">Az.KeyVault</span></span>
* <span data-ttu-id="8d428-2882">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="8d428-2882">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8d428-2883">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d428-2883">Az.Network</span></span>
* <span data-ttu-id="8d428-2884">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="8d428-2884">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="8d428-2885">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d428-2885">Az.Resources</span></span>
* <span data-ttu-id="8d428-2886">Åtgärda felaktiga exempel i referensdokumentationen ”New-AzADAppCredential” och ”New-AzADSpCredential”</span><span class="sxs-lookup"><span data-stu-id="8d428-2886">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="8d428-2887">Åtgärda problem där sökvägen för parametern ”-TemplateFile” inte omvandlas innan cmdletarna för distribution i resursgruppen körs</span><span class="sxs-lookup"><span data-stu-id="8d428-2887">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="8d428-2888">Az.Resources: Korrigera dokumentationen om standardvärdet för New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="8d428-2888">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="8d428-2889">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="8d428-2889">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="8d428-2890">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="8d428-2890">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="8d428-2891">Åtgärda formateringsproblemet med objektet ”PSResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="8d428-2891">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="8d428-2892">Mer information här: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="8d428-2892">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8d428-2893">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8d428-2893">Az.ServiceFabric</span></span>
* <span data-ttu-id="8d428-2894">Återställ när ett certifikat läggs till i en Virtual Machine Scale Sets-modell men ett undantag genereras. Detta har gjorts för att åtgärda följande fel: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="8d428-2894">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="8d428-2895">Korrigera några felmeddelanden.</span><span class="sxs-lookup"><span data-stu-id="8d428-2895">Fix some error messages.</span></span>
* <span data-ttu-id="8d428-2896">Korrigering av skapande av kluster med ARM-mall som är standard för New-AzServiceFabriCluster som inte fungerade med migrering till Az.</span><span class="sxs-lookup"><span data-stu-id="8d428-2896">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="8d428-2897">Korrigering av tilläggning av kluster/programcertifikat så att endast VM Scale Sets som motsvarar klustret läggs till genom att kontrollera ID för klustret i tillägget.</span><span class="sxs-lookup"><span data-stu-id="8d428-2897">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="8d428-2898">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="8d428-2898">Az.SignalR</span></span>
* <span data-ttu-id="8d428-2899">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="8d428-2899">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="8d428-2900">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d428-2900">Az.Sql</span></span>
* <span data-ttu-id="8d428-2901">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="8d428-2901">Update incorrect online help URLs</span></span>
* <span data-ttu-id="8d428-2902">Uppdaterad parameterbeskrivning för LicenseType-parameter med möjliga värden</span><span class="sxs-lookup"><span data-stu-id="8d428-2902">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="8d428-2903">Korrigering för att uppdatera hanterad instansidentitet som inte fungerar när det är den enda uppdaterade egenskapen</span><span class="sxs-lookup"><span data-stu-id="8d428-2903">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="8d428-2904">Stöd för anpassad sortering på hanterad instans</span><span class="sxs-lookup"><span data-stu-id="8d428-2904">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8d428-2905">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8d428-2905">Az.Storage</span></span>
* <span data-ttu-id="8d428-2906">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="8d428-2906">Update incorrect online help URLs</span></span>
* <span data-ttu-id="8d428-2907">Tillhandahåll detaljerat felmeddelande när en användare försöker hämta/konfigurera klassisk loggning/mått på ett Premium Storage-konto eftersom Premium Storage-kontot inte har stöd för klassisk loggning/mått.</span><span class="sxs-lookup"><span data-stu-id="8d428-2907">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="8d428-2908">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="8d428-2908">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="8d428-2909">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="8d428-2909">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="8d428-2910">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="8d428-2910">Az.TrafficManager</span></span>
* <span data-ttu-id="8d428-2911">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="8d428-2911">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8d428-2912">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8d428-2912">Az.Websites</span></span>
* <span data-ttu-id="8d428-2913">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="8d428-2913">Update incorrect online help URLs</span></span>
* <span data-ttu-id="8d428-2914">Korrigerar ”New-AzWebAppSSLBinding” så att certifikatet laddas upp till rätt resursgrupp och plats om appen finns i en ASE.</span><span class="sxs-lookup"><span data-stu-id="8d428-2914">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="8d428-2915">Korrigerar ”New-AzWebAppSSLBinding” så att taggarna inte skrivs över på en bindning av ett SSL-certifikat till en app</span><span class="sxs-lookup"><span data-stu-id="8d428-2915">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="8d428-2916">1.1.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="8d428-2916">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8d428-2917">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8d428-2917">Az.Accounts</span></span>
* <span data-ttu-id="8d428-2918">Lade till omfattningen ”Lokal” till Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="8d428-2918">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d428-2919">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d428-2919">Az.Compute</span></span>
* <span data-ttu-id="8d428-2920">Namn är nu valfritt i ID-parametern för Restart/Start/Stop/Remove/Set-AzVM och Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="8d428-2920">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="8d428-2921">Uppdaterade beskrivningen av ID i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="8d428-2921">Updated the description of ID in help files</span></span>
* <span data-ttu-id="8d428-2922">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8d428-2922">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8d428-2923">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8d428-2923">Az.DataLakeStore</span></span>
* <span data-ttu-id="8d428-2924">Uppdatera sdk-versionen av dataplanet till 1.1.14 för SDK-korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="8d428-2924">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="8d428-2925">Korrigerade hanteringen av negativ accesstime och modificationtime för getfilestatus och liststatus; korrigera asynkront annulleringstoken</span><span class="sxs-lookup"><span data-stu-id="8d428-2925">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="8d428-2926">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="8d428-2926">Az.EventGrid</span></span>
* <span data-ttu-id="8d428-2927">Uppdaterat för användning av API-versionen 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="8d428-2927">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="8d428-2928">Uppdaterade följande cmdletar för att stödja nytt scenario i API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="8d428-2928">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="8d428-2929">New-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="8d428-2929">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="8d428-2930">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="8d428-2930">Event Time-To-Live,</span></span>
        - <span data-ttu-id="8d428-2931">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="8d428-2931">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="8d428-2932">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="8d428-2932">Dead letter endpoint.</span></span>
    - <span data-ttu-id="8d428-2933">Update-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="8d428-2933">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="8d428-2934">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="8d428-2934">Event Time-To-Live,</span></span>
        - <span data-ttu-id="8d428-2935">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="8d428-2935">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="8d428-2936">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="8d428-2936">Dead letter endpoint.</span></span>
* <span data-ttu-id="8d428-2937">Lade till nya enum-värden (storageQueue och hybridConnection) för alternativet EndpointType i cmdletarna New-AzureRmEventGridSubscription och Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="8d428-2937">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="8d428-2938">Visa varningsmeddelanden om skapande eller uppdatering av händelseprenumerationen förväntas medföra manuell åtgärd från användaren.</span><span class="sxs-lookup"><span data-stu-id="8d428-2938">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8d428-2939">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8d428-2939">Az.IotHub</span></span>
* <span data-ttu-id="8d428-2940">Har uppdaterats till den senaste versionen av SDK:n lotHub</span><span class="sxs-lookup"><span data-stu-id="8d428-2940">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="8d428-2941">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="8d428-2941">Az.LogicApp</span></span>
* <span data-ttu-id="8d428-2942">Get-AzLogicApp visar en lista över alla som inte har angivet namn</span><span class="sxs-lookup"><span data-stu-id="8d428-2942">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="8d428-2943">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d428-2943">Az.Resources</span></span>
* <span data-ttu-id="8d428-2944">Åtgärdade problem med parameteruppsättningen när parametrarna -ODataQuery och -ResourceId anges för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="8d428-2944">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="8d428-2945">Mer information här: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="8d428-2945">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="8d428-2946">Åtgärdade hantering av parametern -Custom i New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8d428-2946">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="8d428-2947">Korrigerade stavfel i New-AzDeployment-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="8d428-2947">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="8d428-2948">Gjorde parametern -MailNickname obligatorisk för New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="8d428-2948">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="8d428-2949">Mer information här: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="8d428-2949">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="8d428-2950">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="8d428-2950">Az.SignalR</span></span>
* <span data-ttu-id="8d428-2951">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8d428-2951">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="8d428-2952">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d428-2952">Az.Sql</span></span>
* <span data-ttu-id="8d428-2953">Konverterade lagringshanteringsklientens beroende av den normala SDK-implementeringen.</span><span class="sxs-lookup"><span data-stu-id="8d428-2953">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8d428-2954">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8d428-2954">Az.Storage</span></span>
* <span data-ttu-id="8d428-2955">Angav StorageAccountName för lagringskontext som det verkliga namnet på lagringskontot när det skapas med Sas Token, OAuth eller Anonymous</span><span class="sxs-lookup"><span data-stu-id="8d428-2955">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="8d428-2956">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="8d428-2956">New-AzStorageContext</span></span>
* <span data-ttu-id="8d428-2957">Skapade Sas Token för Blob Snapshot-objekt med parametern -FullUri, åtgärdade den returnerade URI:n så att den blir URI för ögonblicksbild</span><span class="sxs-lookup"><span data-stu-id="8d428-2957">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="8d428-2958">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="8d428-2958">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8d428-2959">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8d428-2959">Az.Websites</span></span>
* <span data-ttu-id="8d428-2960">Åtgärdade en bugg i datumparsningen i Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="8d428-2960">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="8d428-2961">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8d428-2961">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="8d428-2962">1.0.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="8d428-2962">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="8d428-2963">Allmänt</span><span class="sxs-lookup"><span data-stu-id="8d428-2963">General</span></span>

- <span data-ttu-id="8d428-2964">Allmän tillgänglighet för Az-modulen</span><span class="sxs-lookup"><span data-stu-id="8d428-2964">General Availability of Az Module</span></span>
- <span data-ttu-id="8d428-2965">Onlinehjälp för varje modul</span><span class="sxs-lookup"><span data-stu-id="8d428-2965">Online help for each module</span></span>
- <span data-ttu-id="8d428-2966">Mer information och en översikt finns på [Az-informationssidan](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="8d428-2966">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="8d428-2967">Information om hur du migrerar från AzureRM finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8d428-2967">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="8d428-2968">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8d428-2968">Az.Accounts</span></span>
- <span data-ttu-id="8d428-2969">Har ändrats från Az.Profile</span><span class="sxs-lookup"><span data-stu-id="8d428-2969">Changed from Az.Profile</span></span>
- <span data-ttu-id="8d428-2970">Fasta tabellformat för profil- och kontexttyper</span><span class="sxs-lookup"><span data-stu-id="8d428-2970">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="8d428-2971">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8d428-2971">Az.ApiManagement</span></span>
- <span data-ttu-id="8d428-2972">Korrigeringar för #7002</span><span class="sxs-lookup"><span data-stu-id="8d428-2972">Fixes for #7002</span></span>
- <span data-ttu-id="8d428-2973">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8d428-2973">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="8d428-2974">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="8d428-2974">Az.Batch</span></span>
- <span data-ttu-id="8d428-2975">Lade till möjligheten att se vilken version av Azure Batch Node Agent som körs på var och en av de virtuella datorerna i en pool, via den nya egenskapen `NodeAgentInformation` på `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="8d428-2975">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="8d428-2976">Standarden `Caching` för `PSDataDisk` är nu `ReadWrite` i stället för `None`.</span><span class="sxs-lookup"><span data-stu-id="8d428-2976">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="8d428-2977">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8d428-2977">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="8d428-2978">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="8d428-2978">Az.Billing</span></span>
- <span data-ttu-id="8d428-2979">Kombinerar cmdletarna för fakturering, förbrukning och UsageAggregates. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8d428-2979">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="8d428-2980">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="8d428-2980">Az.CognitivServices</span></span>
- <span data-ttu-id="8d428-2981">Lade till kompletterare för SkuName och Typem som är tillgängliga i New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="8d428-2981">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="8d428-2982">Tog bort parameteruppsättningen GetSkusWithAccountParamSetName från Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="8d428-2982">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="8d428-2983">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="8d428-2983">Az.ContainerInstance</span></span>
- <span data-ttu-id="8d428-2984">Stöd för ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="8d428-2984">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="8d428-2985">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="8d428-2985">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="8d428-2986">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8d428-2986">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="8d428-2987">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8d428-2987">Az.DataLakeStore</span></span>
- <span data-ttu-id="8d428-2988">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8d428-2988">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="8d428-2989">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8d428-2989">Az.Monitor</span></span>
- <span data-ttu-id="8d428-2990">Döpte om Az.Insights till Az.Monitor och andra mindre icke-bakåtkompatibla ändringar. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8d428-2990">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="8d428-2991">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8d428-2991">Az.KeyVault</span></span>
- <span data-ttu-id="8d428-2992">Tog bort den inaktuella egenskapen PurgeDisabled från utdatatyper</span><span class="sxs-lookup"><span data-stu-id="8d428-2992">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="8d428-2993">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="8d428-2993">Az.MachineLearning</span></span>
- <span data-ttu-id="8d428-2994">Inkluderade cmdletarna från modulen Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="8d428-2994">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="8d428-2995">Az.Media</span><span class="sxs-lookup"><span data-stu-id="8d428-2995">Az.Media</span></span>
- <span data-ttu-id="8d428-2996">Tog bort inaktuella -Tags-alias från New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="8d428-2996">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="8d428-2997">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d428-2997">Az.Network</span></span>
<span data-ttu-id="8d428-2998">Stöd har lagts till för konfiguration av RewriteRuleSets i Application Gateway</span><span class="sxs-lookup"><span data-stu-id="8d428-2998">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="8d428-2999">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="8d428-2999">New cmdlets added:</span></span>
        - <span data-ttu-id="8d428-3000">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8d428-3000">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="8d428-3001">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8d428-3001">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="8d428-3002">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8d428-3002">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="8d428-3003">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8d428-3003">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="8d428-3004">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8d428-3004">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="8d428-3005">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="8d428-3005">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="8d428-3006">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="8d428-3006">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="8d428-3007">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="8d428-3007">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="8d428-3008">Cmdletar har uppdaterats med den valfria parametern -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8d428-3008">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="8d428-3009">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8d428-3009">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="8d428-3010">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="8d428-3010">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="8d428-3011">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="8d428-3011">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="8d428-3012">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8d428-3012">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="8d428-3013">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="8d428-3013">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="8d428-3014">New-AzureRmApplicationGatewayUrlPathMapConfig har lagt till KeyVault-stöd för Application Gateway med Identity.</span><span class="sxs-lookup"><span data-stu-id="8d428-3014">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="8d428-3015">Cmdletar har uppdaterats med den valfria parametern -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="8d428-3015">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="8d428-3016">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8d428-3016">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="8d428-3017">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8d428-3017">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="8d428-3018">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8d428-3018">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="8d428-3019">Cmdleten New-AzApplicationGateway har uppdaterats med den valfria parametern -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="8d428-3019">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="8d428-3020">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8d428-3020">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="8d428-3021">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8d428-3021">Az.OperationalInsights</span></span>
- <span data-ttu-id="8d428-3022">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8d428-3022">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="8d428-3023">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="8d428-3023">Az.Profile</span></span>
- <span data-ttu-id="8d428-3024">Modulnamnet har ändrats till Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8d428-3024">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="8d428-3025">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8d428-3025">Az.RecoveryServices</span></span>
- <span data-ttu-id="8d428-3026">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8d428-3026">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="8d428-3027">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d428-3027">Az.Resources</span></span>
- <span data-ttu-id="8d428-3028">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8d428-3028">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="8d428-3029">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8d428-3029">Az.ServiceFabric</span></span>
- <span data-ttu-id="8d428-3030">Stöd för specificering av certifikat efter eget namn och tumavtryck</span><span class="sxs-lookup"><span data-stu-id="8d428-3030">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="8d428-3031">Information om fler icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8d428-3031">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="8d428-3032">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="8d428-3032">Az.SIgnalR</span></span>
- <span data-ttu-id="8d428-3033">Allmän tillgänglighet för PowerShell-cmdletar för SIgnalR</span><span class="sxs-lookup"><span data-stu-id="8d428-3033">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="8d428-3034">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d428-3034">Az.Sql</span></span>
- <span data-ttu-id="8d428-3035">Lade till de nya identifieringstyperna Data_Exfiltration och Unsafe_Action i Threat Detection-cmdletar</span><span class="sxs-lookup"><span data-stu-id="8d428-3035">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="8d428-3036">Uppdaterade dokumentationsexempel för Sql Auditing-cmdletar</span><span class="sxs-lookup"><span data-stu-id="8d428-3036">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="8d428-3037">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8d428-3037">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="8d428-3038">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8d428-3038">Az.Storage</span></span>
- <span data-ttu-id="8d428-3039">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8d428-3039">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="8d428-3040">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8d428-3040">Az.Websites</span></span>
- <span data-ttu-id="8d428-3041">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8d428-3041">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="8d428-3042">0.7.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="8d428-3042">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="8d428-3043">Allmänt</span><span class="sxs-lookup"><span data-stu-id="8d428-3043">General</span></span>

* <span data-ttu-id="8d428-3044">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="8d428-3044">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="8d428-3045">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d428-3045">Az.Compute</span></span>

* <span data-ttu-id="8d428-3046">Lade till stöd för UltraSSD och Galleriavbildningar i de enkla parameteruppsättningarna för `New-AzVm(ss)`-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="8d428-3046">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="8d428-3047">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8d428-3047">Az.DataLakeStore</span></span>

* <span data-ttu-id="8d428-3048">Åtgärdade avslutande snedstreck i domänen för adls-konto</span><span class="sxs-lookup"><span data-stu-id="8d428-3048">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="8d428-3049">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="8d428-3049">Az.FrontDoor</span></span>

* <span data-ttu-id="8d428-3050">Brutna länkar korrigerades</span><span class="sxs-lookup"><span data-stu-id="8d428-3050">Fixed some broken links</span></span>
    - <span data-ttu-id="8d428-3051">I artiklarna New-AzureRmFrontDoor och Set-AzureRmFrontDoor artiklar korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="8d428-3051">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="8d428-3052">I artikeln New-AzureRmFrontDoorManagedRuleObject korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="8d428-3052">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="8d428-3053">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8d428-3053">Az.RecoveryServices</span></span>

* <span data-ttu-id="8d428-3054">Lade till valideringar på klientsidan för Azure-filresurs med återställningsåtgärder.</span><span class="sxs-lookup"><span data-stu-id="8d428-3054">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="8d428-3055">Gjorde storageAccountName och storageAccountResourceGroupName valfritt för afs-återställning.</span><span class="sxs-lookup"><span data-stu-id="8d428-3055">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="8d428-3056">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d428-3056">Az.Resources</span></span>

* <span data-ttu-id="8d428-3057">Korrigering för https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="8d428-3057">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="8d428-3058">Uppdaterade Get-AzureRmRoleAssignment så att prenumerationsomfattningen används om den anges vid begäran om klassiska administratörer.</span><span class="sxs-lookup"><span data-stu-id="8d428-3058">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="8d428-3059">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d428-3059">Az.Sql</span></span>

* <span data-ttu-id="8d428-3060">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="8d428-3060">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="8d428-3061">Korrigerade ett problem med Get-AzureRmSqlDatabaseVulnerabilityAssessment med DotNet-kärna</span><span class="sxs-lookup"><span data-stu-id="8d428-3061">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="8d428-3062">Ändrade dokumentationen för hjälpmeddelanden som rör SQL Auditing-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="8d428-3062">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="8d428-3063">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8d428-3063">Az.Storage</span></span>

* <span data-ttu-id="8d428-3064">Lade till -EnableHierarchicalNamespace i New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8d428-3064">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="8d428-3065">Åtgärdade problemet med att cmdleten Copy File inte kunde återanvända källkontexten på målet om inte -DestContext angetts</span><span class="sxs-lookup"><span data-stu-id="8d428-3065">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="8d428-3066">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="8d428-3066">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="8d428-3067">Stöd för statisk webbplatskonfiguration</span><span class="sxs-lookup"><span data-stu-id="8d428-3067">Support Static Website configuration</span></span>
    - <span data-ttu-id="8d428-3068">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="8d428-3068">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="8d428-3069">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="8d428-3069">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="8d428-3070">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8d428-3070">Az.Websites</span></span>

* <span data-ttu-id="8d428-3071">Set-AzureRmWebApp och Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8d428-3071">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="8d428-3072">Ny parameter (-AzureStoragePath) har lagts till för att ange att Azure Storage-sökvägar ska monteras i containerappar i Windows och Linux.</span><span class="sxs-lookup"><span data-stu-id="8d428-3072">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="8d428-3073">Använder utdata från den nya cmdleten New-AzureRmWebAppAzureStoragePath som en parameter för att ange sökvägar för Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="8d428-3073">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="8d428-3074">0.6.1 – november 2018</span><span class="sxs-lookup"><span data-stu-id="8d428-3074">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="8d428-3075">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8d428-3075">Az.ApiManagement</span></span>
* <span data-ttu-id="8d428-3076">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="8d428-3076">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="8d428-3077">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8d428-3077">Az.Automation</span></span>
* <span data-ttu-id="8d428-3078">Swagger baserade Azure Automation-cmdletar</span><span class="sxs-lookup"><span data-stu-id="8d428-3078">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="8d428-3079">Cmdletar för Uppdateringshantering har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-3079">Added Update Management cmdlets</span></span>
* <span data-ttu-id="8d428-3080">Cmdletar för källkontroll har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-3080">Added Source Control cmdlets</span></span>
* <span data-ttu-id="8d428-3081">Remove-AzureRmAutomationHybridWorkerGroup-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-3081">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="8d428-3082">Kommandot för DSC-registreringsnod har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8d428-3082">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="8d428-3083">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d428-3083">Az.Compute</span></span>
* <span data-ttu-id="8d428-3084">Problem med SystemAssigned-identitet har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8d428-3084">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="8d428-3085">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="8d428-3085">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="8d428-3086">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="8d428-3086">Az.ContainerInstance</span></span>
* <span data-ttu-id="8d428-3087">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="8d428-3087">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="8d428-3088">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="8d428-3088">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="8d428-3089">uppdatera exempelbeskrivningen för marketplace-cmdletar</span><span class="sxs-lookup"><span data-stu-id="8d428-3089">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="8d428-3090">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d428-3090">Az.Network</span></span>
* <span data-ttu-id="8d428-3091">Cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomErreller Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-3091">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="8d428-3092">ICMP tillbaka till stöd för Azure Firewall-nätverksprotokoll har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-3092">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="8d428-3093">Uppdatera cmdlet Test-AzureRmNetworkWatcherConnectivity, lägga till verifiering av mål-id, adress och port.</span><span class="sxs-lookup"><span data-stu-id="8d428-3093">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="8d428-3094">Åtgärda problem med minnesanvändning i VirtualNetwork-karta</span><span class="sxs-lookup"><span data-stu-id="8d428-3094">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="8d428-3095">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="8d428-3095">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="8d428-3096">Åtgärda för att ändra principen för en skyddad fildelning.</span><span class="sxs-lookup"><span data-stu-id="8d428-3096">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="8d428-3097">Tidszonsprincipen har konverterats till versaler.</span><span class="sxs-lookup"><span data-stu-id="8d428-3097">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="8d428-3098">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="8d428-3098">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="8d428-3099">Exempel i New-AzureRmRecoveryServicesAsrProtectableItem har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8d428-3099">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="8d428-3100">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="8d428-3100">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="8d428-3101">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="8d428-3101">Az.Relay</span></span>
* <span data-ttu-id="8d428-3102">Valfri parameter -KeyValue till New-AzureRmRelayKey cmdlet har lagts till, vilket gör det möjligt för användare att tillhandahålla KeyValue.</span><span class="sxs-lookup"><span data-stu-id="8d428-3102">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="8d428-3103">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d428-3103">Az.Resources</span></span>
* <span data-ttu-id="8d428-3104">Uppdatera hjälpdokumentation för resursidentitet kopplad till parametrar i `New-AzureRmPolicyAssignment` och `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="8d428-3104">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="8d428-3105">Lägg till ett exempel för New-AzureRmPolicyDefinition som använder -Metadata</span><span class="sxs-lookup"><span data-stu-id="8d428-3105">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="8d428-3106">Korrigera så att skiftläge behålls i taggnycklar i NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="8d428-3106">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="8d428-3107">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8d428-3107">Az.ServiceFabric</span></span>
* <span data-ttu-id="8d428-3108">Lägg till utfasningsmeddelanden för kommande icke-kompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="8d428-3108">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="8d428-3109">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d428-3109">Az.Sql</span></span>
* <span data-ttu-id="8d428-3110">Nya cmdletar för CRUD-åtgärder på Azure Sql Database-hanterad instans och Azure Sql-hanterad databas</span><span class="sxs-lookup"><span data-stu-id="8d428-3110">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="8d428-3111">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="8d428-3111">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="8d428-3112">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="8d428-3112">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="8d428-3113">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="8d428-3113">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="8d428-3114">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="8d428-3114">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="8d428-3115">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="8d428-3115">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="8d428-3116">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="8d428-3116">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="8d428-3117">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="8d428-3117">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="8d428-3118">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="8d428-3118">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="8d428-3119">Hantering av utökad granskningsprincip på en server eller en databas har aktiverats.</span><span class="sxs-lookup"><span data-stu-id="8d428-3119">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="8d428-3120">Ny parameter (PredicateExpression) har lagts till för att aktivera filtrering av granskningsloggar.</span><span class="sxs-lookup"><span data-stu-id="8d428-3120">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="8d428-3121">Cmdletar har ändrats så att de använder SQL-klienter i stället för äldre klienter.</span><span class="sxs-lookup"><span data-stu-id="8d428-3121">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="8d428-3122">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="8d428-3122">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="8d428-3123">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="8d428-3123">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="8d428-3124">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="8d428-3124">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="8d428-3125">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="8d428-3125">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="8d428-3126">Problem med att använda Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings med lagringskontots namnparameter har korrigerats</span><span class="sxs-lookup"><span data-stu-id="8d428-3126">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="8d428-3127">0.5.0 – november 2018</span><span class="sxs-lookup"><span data-stu-id="8d428-3127">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="8d428-3128">Allmänt</span><span class="sxs-lookup"><span data-stu-id="8d428-3128">General</span></span>
* <span data-ttu-id="8d428-3129">Lade till resurskompletterare till många kärn-cmdletar – dessa gör att du kan stega genom befintliga resursnamn med TABB vid interaktiva anrop till cmdletar</span><span class="sxs-lookup"><span data-stu-id="8d428-3129">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="8d428-3130">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="8d428-3130">Az.Profile</span></span>
* <span data-ttu-id="8d428-3131">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="8d428-3131">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="8d428-3132">Bytte namn på parametern TenantId i cmdleten Connect-AzAccount till Tenant och lade till ett alias för TenantId</span><span class="sxs-lookup"><span data-stu-id="8d428-3132">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="8d428-3133">Uppdaterade TenantId-beskrivningen för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="8d428-3133">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="8d428-3134">Åtgärda felmeddelande för misslyckad inloggning när du tillhandahåller klientdomän</span><span class="sxs-lookup"><span data-stu-id="8d428-3134">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="8d428-3135">Åtgärda problem med att kontextnamn hamnar i konflikt för konton utan prenumerationer i klientorganisationen</span><span class="sxs-lookup"><span data-stu-id="8d428-3135">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="8d428-3136">Åtgärda problem med DataLake-slutpunkter vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="8d428-3136">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="8d428-3137">Åtgärdade problem med att Disconnect-AzAccount kastades om den inte anslöts</span><span class="sxs-lookup"><span data-stu-id="8d428-3137">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="8d428-3138">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8d428-3138">Az.CognitiveServices</span></span>
* <span data-ttu-id="8d428-3139">Lade till åtgärden Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="8d428-3139">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d428-3140">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d428-3140">Az.Compute</span></span>
* <span data-ttu-id="8d428-3141">Lade till cmdletarna Add-AzVmssVMDataDisk och Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="8d428-3141">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="8d428-3142">Get-AzVMImage visar AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="8d428-3142">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="8d428-3143">Åtgärdade att värdena för alternativen SetAzVMChefExtension -BootstrapOptions och -JsonAttribute inte angavs i json-format.</span><span class="sxs-lookup"><span data-stu-id="8d428-3143">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8d428-3144">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8d428-3144">Az.DataLakeStore</span></span>
* <span data-ttu-id="8d428-3145">Uppdatera DataLake-paketet till 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="8d428-3145">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="8d428-3146">Lägg till standardsamtidighet för flertrådade åtgärder.</span><span class="sxs-lookup"><span data-stu-id="8d428-3146">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="8d428-3147">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="8d428-3147">Az.Insights</span></span>
* <span data-ttu-id="8d428-3148">Åtgärdade problem #7267 (autoskalningsområde)</span><span class="sxs-lookup"><span data-stu-id="8d428-3148">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="8d428-3149">Problem med att uppräknade parametrar inte ställdes in ordentligt när du skapade en ny autoskalningsregel (de ställdes alltid in med standardvärdet).</span><span class="sxs-lookup"><span data-stu-id="8d428-3149">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="8d428-3150">Åtgärdade problem #7513 [Insights] Set-AzDiagnosticSetting kräver uttrycklig specifikation av kategorier när inställningar skapas</span><span class="sxs-lookup"><span data-stu-id="8d428-3150">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="8d428-3151">Nu kräver inte cmdleten uttrycklig anvisning av kategorierna för att aktiveras under skapande, d.v.s. den fungerar enligt beskrivning</span><span class="sxs-lookup"><span data-stu-id="8d428-3151">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8d428-3152">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d428-3152">Az.Network</span></span>
* <span data-ttu-id="8d428-3153">PeeringType ändrades till en obligatorisk parameter för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="8d428-3153">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="8d428-3154">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="8d428-3154">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="8d428-3155">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="8d428-3155">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="8d428-3156">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="8d428-3156">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="8d428-3157">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="8d428-3157">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="8d428-3158">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="8d428-3158">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="8d428-3159">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="8d428-3159">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="8d428-3160">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="8d428-3160">Az.PolicyInsights</span></span>
* <span data-ttu-id="8d428-3161">Cmdletar för principreparation har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-3161">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="8d428-3162">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d428-3162">Az.Resources</span></span>
* <span data-ttu-id="8d428-3163">Korrigering för https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="8d428-3163">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="8d428-3164">Tillåt att resurser listas med parametern -ResourceId för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="8d428-3164">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="8d428-3165">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8d428-3165">Az.ServiceBus</span></span>
* <span data-ttu-id="8d428-3166">Skrivskyddad MigrationState-egenskap har lagts till i PSServiceBusMigrationConfigurationAttributes, som hjälper till att hålla koll på migreringstillståndet.</span><span class="sxs-lookup"><span data-stu-id="8d428-3166">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8d428-3167">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8d428-3167">Az.ServiceFabric</span></span>
* <span data-ttu-id="8d428-3168">Åtgärda att lägga till certifikat till Linux-Vmss.</span><span class="sxs-lookup"><span data-stu-id="8d428-3168">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="8d428-3169">Åtgärdade Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="8d428-3169">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="8d428-3170">Använd rätt tumavtryck från nya certifikat (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="8d428-3170">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="8d428-3171">Visa undantag korrekt (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="8d428-3171">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="8d428-3172">Åtgärdade Update-AzServiceFabricDurability så att klusterkonfigurationen uppdateras innan Vmss-åtgärden CreateOrUpdate påbörjas.</span><span class="sxs-lookup"><span data-stu-id="8d428-3172">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="8d428-3173">0.4.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="8d428-3173">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="8d428-3174">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="8d428-3174">Az.Profile</span></span>
* <span data-ttu-id="8d428-3175">Åtgärdade problemet med Get-AzSubscription i CloudShell</span><span class="sxs-lookup"><span data-stu-id="8d428-3175">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="8d428-3176">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="8d428-3176">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d428-3177">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d428-3177">Az.Compute</span></span>
* <span data-ttu-id="8d428-3178">Nya storlekar lades till i listan över godkända VM-storlekar för vilka accelererat nätverk kommer att aktiveras vid användning av den enkla parameteruppsättningen för New-AzVm</span><span class="sxs-lookup"><span data-stu-id="8d428-3178">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="8d428-3179">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="8d428-3179">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8d428-3180">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8d428-3180">Az.DataLakeStore</span></span>
* <span data-ttu-id="8d428-3181">Lägger till stöd för regler för virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="8d428-3181">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="8d428-3182">Get-AzDataLakeStoreVirtualNetworkRule: Hämtar eller listar regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8d428-3182">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="8d428-3183">Add-AzDataLakeStoreVirtualNetworkRule: Lägger till en regel för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="8d428-3183">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="8d428-3184">Set-AzDataLakeStoreVirtualNetworkRule: Ändrar den angivna regeln för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="8d428-3184">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="8d428-3185">Remove-AzDataLakeStoreVirtualNetworkRule: Tar bort en regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8d428-3185">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8d428-3186">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d428-3186">Az.Network</span></span>
* <span data-ttu-id="8d428-3187">Skicka protokollvärdet till serverdelen för att uppdatera cmdleten Test-AzNetworkWatcherConnectivity.</span><span class="sxs-lookup"><span data-stu-id="8d428-3187">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="8d428-3188">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="8d428-3188">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8d428-3189">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d428-3189">Az.Resources</span></span>
* <span data-ttu-id="8d428-3190">Åtgärdade problem där Get-AzRoleDefinition genererar ett oläsligt undantag (när standardprofilen inte innehåller någon prenumeration och ingen omfattning har angetts) genom att lägga till ett beskrivande undantag i scenariot.</span><span class="sxs-lookup"><span data-stu-id="8d428-3190">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="8d428-3191">Ställ in ”RoleDefinitionNameParameterSet” som standardparameteruppsättning.</span><span class="sxs-lookup"><span data-stu-id="8d428-3191">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="8d428-3192">0.3.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="8d428-3192">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="8d428-3193">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="8d428-3193">Azure.Storage</span></span>
* <span data-ttu-id="8d428-3194">Åtgärda fel där Kopiera blob/fil inte kopierar metadata när målplatsen har ett problem med metadata</span><span class="sxs-lookup"><span data-stu-id="8d428-3194">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="8d428-3195">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="8d428-3195">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="8d428-3196">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="8d428-3196">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="8d428-3197">Stöd för att hämta användningsinformation om en Storage-resurs för en specifik plats och för att lägga till ett varningsmeddelande för att hämta användningsinformation om en global Storage-resurs är inaktuellt.</span><span class="sxs-lookup"><span data-stu-id="8d428-3197">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="8d428-3198">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="8d428-3198">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="8d428-3199">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8d428-3199">Az.CognitiveServices</span></span>
* <span data-ttu-id="8d428-3200">Stöd för Get-AzCognitiveServicesAccountSkus utan ett befintligt konto.</span><span class="sxs-lookup"><span data-stu-id="8d428-3200">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d428-3201">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d428-3201">Az.Compute</span></span>
* <span data-ttu-id="8d428-3202">Åtgärdade fel där Get-AzVM -ResourceGroupName <rg> returnerar fler än 50 resultat om det behövs</span><span class="sxs-lookup"><span data-stu-id="8d428-3202">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="8d428-3203">Lade till ett exempel för SimpleParameterSet i hjälpen för cmdleten New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="8d428-3203">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="8d428-3204">Ett stavfel i förloppsmeddelandet för Azure Disk Encryption har korrigerats</span><span class="sxs-lookup"><span data-stu-id="8d428-3204">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="8d428-3205">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="8d428-3205">Az.DataFactoryV2</span></span>
* <span data-ttu-id="8d428-3206">ADF .Net SDK-versionen har uppdaterats till 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="8d428-3206">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8d428-3207">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d428-3207">Az.Network</span></span>
* <span data-ttu-id="8d428-3208">Funktionalitet för NetworkProfile har lagts till.</span><span class="sxs-lookup"><span data-stu-id="8d428-3208">Added NetworkProfile functionality.</span></span> <span data-ttu-id="8d428-3209">nya cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-3209">new cmdlets added</span></span>
    - <span data-ttu-id="8d428-3210">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8d428-3210">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="8d428-3211">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8d428-3211">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="8d428-3212">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8d428-3212">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="8d428-3213">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8d428-3213">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="8d428-3214">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="8d428-3214">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="8d428-3215">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="8d428-3215">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="8d428-3216">Länk för tjänstassociering på modell för undernät har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-3216">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="8d428-3217">Cmdletarna New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap och Remove-AzVirtualNetworkTap har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-3217">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="8d428-3218">Cmdletarna Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig och Remove-AzNEtworkInterfaceTapConfig har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-3218">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="8d428-3219">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="8d428-3219">Az.RedisCache</span></span>
* <span data-ttu-id="8d428-3220">Tillåt att alla strängar används som storleksparametrar framöver.</span><span class="sxs-lookup"><span data-stu-id="8d428-3220">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="8d428-3221">Lägg till P5 i popup-fönstret PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="8d428-3221">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="8d428-3222">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d428-3222">Az.Resources</span></span>
* <span data-ttu-id="8d428-3223">Parametern -Mode som saknades i Set-AzPolicyDefinition har lagts till</span><span class="sxs-lookup"><span data-stu-id="8d428-3223">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="8d428-3224">Åtgärdade buggen för cmdleten Get-AzProviderOperation för åtgärder med ursprung som innehåller användare</span><span class="sxs-lookup"><span data-stu-id="8d428-3224">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="8d428-3225">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d428-3225">Az.Sql</span></span>
* <span data-ttu-id="8d428-3226">Ett problem där vissa cmdletar för säkerhetskopiering inte kunde identifiera den aktuella azure-prenumerationen har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8d428-3226">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8d428-3227">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8d428-3227">Az.Websites</span></span>
* <span data-ttu-id="8d428-3228">Ny cmdlet: Get-AzWebAppContainerContinuousDeploymentUrl – Hämtar webhook-URL:en för kontinuerlig distribution av container</span><span class="sxs-lookup"><span data-stu-id="8d428-3228">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="8d428-3229">Nya cmdletar: New-AzWebAppContainerPSSession och Enter-WebAppContainerPSSession – Startar en PowerShell-fjärrsession i en containerapp för windows</span><span class="sxs-lookup"><span data-stu-id="8d428-3229">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="8d428-3230">0.2.0 – september 2018</span><span class="sxs-lookup"><span data-stu-id="8d428-3230">0.2.0 - September 2018</span></span>
 <span data-ttu-id="8d428-3231">Första versionen</span><span class="sxs-lookup"><span data-stu-id="8d428-3231">Initial Release</span></span>
