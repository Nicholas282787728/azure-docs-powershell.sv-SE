---
title: Viktig information om Azure PowerShell
description: Lär dig mer om alla de senaste uppdateringarna för Azure PowerShell-modulerna.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: bee24af99da4b36e89cff9852c77214e2e09a542
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "81740549"
---
## <a name="380---april-2020"></a><span data-ttu-id="ced70-103">3.8.0 – April 2020</span><span class="sxs-lookup"><span data-stu-id="ced70-103">3.8.0 - April 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ced70-104">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ced70-104">Az.Accounts</span></span>
* <span data-ttu-id="ced70-105">Uppdaterade URL:en för Azure PowerShell-enkäten i ”Resolve-AzError” [#11507]</span><span class="sxs-lookup"><span data-stu-id="ced70-105">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="ced70-106">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ced70-106">Az.ApiManagement</span></span>
* <span data-ttu-id="ced70-107">Lade till meddelande om icke-bakåtkompatibel ändring vid ändring i utdata för Azure File-cmdletar i en framtida version</span><span class="sxs-lookup"><span data-stu-id="ced70-107">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="ced70-108">"Set-AzApiManagementGroup" Uppdaterad dokumentation för att ange GroupId-parametern</span><span class="sxs-lookup"><span data-stu-id="ced70-108">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="ced70-109">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="ced70-109">Az.Cdn</span></span>
* <span data-ttu-id="ced70-110">Fast ChinaCDN-relaterad prissättning för SKU-visning</span><span class="sxs-lookup"><span data-stu-id="ced70-110">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="ced70-111">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ced70-111">Az.CognitiveServices</span></span>
* <span data-ttu-id="ced70-112">Identitet som stöds, kryptering, UserOwnedStorage</span><span class="sxs-lookup"><span data-stu-id="ced70-112">Supported Identity, Encryption, UserOwnedStorage</span></span> 

#### <a name="azcompute"></a><span data-ttu-id="ced70-113">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ced70-113">Az.Compute</span></span>
* <span data-ttu-id="ced70-114">Cmdleten ”Set-AzVmssOrchestrationServiceState” har lagts till.</span><span class="sxs-lookup"><span data-stu-id="ced70-114">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="ced70-115">”Get-AzVmss” med -InstanceView visar OrchestrationService-tillstånd.</span><span class="sxs-lookup"><span data-stu-id="ced70-115">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ced70-116">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ced70-116">Az.IotHub</span></span>
* <span data-ttu-id="ced70-117">Hantera den dubbla konfigurationen för IoT-enheter, nya cmdletar är:</span><span class="sxs-lookup"><span data-stu-id="ced70-117">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="ced70-118">'Get-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="ced70-118">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="ced70-119">'Update-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="ced70-119">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="ced70-120">En cmdlet har lagts till för att anropa direkt metod på en enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="ced70-120">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="ced70-121">Hantera dubbel konfiguration för IoT-enhetsmodul, nya cmdletar är:</span><span class="sxs-lookup"><span data-stu-id="ced70-121">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="ced70-122">'Get-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="ced70-122">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="ced70-123">'Update-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="ced70-123">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="ced70-124">Hantera IoT-automatisk konfiguration av enhetshantering i stor skala.</span><span class="sxs-lookup"><span data-stu-id="ced70-124">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="ced70-125">Nya cmdlet:ar är:</span><span class="sxs-lookup"><span data-stu-id="ced70-125">New cmdlets are:</span></span>
    - <span data-ttu-id="ced70-126">'Add-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="ced70-126">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="ced70-127">'Get-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="ced70-127">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="ced70-128">'Remove-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="ced70-128">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="ced70-129">'Set-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="ced70-129">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="ced70-130">En cmdlet har lagts till för att anropa en edge-modulmetod i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="ced70-130">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ced70-131">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ced70-131">Az.KeyVault</span></span>
* <span data-ttu-id="ced70-132">Har lagt till en ny cmdlet, "Update-AzKeyVault", som kan aktivera mjuk borttagning och rensning av skydd i ett valv</span><span class="sxs-lookup"><span data-stu-id="ced70-132">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="ced70-133">Har lagt till stöd i Microsoft.PowerShell.SecretManagement [#11178]</span><span class="sxs-lookup"><span data-stu-id="ced70-133">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="ced70-134">Åtgärdat fel i exemplen i 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span><span class="sxs-lookup"><span data-stu-id="ced70-134">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="ced70-135">Har lagt till stöd för privat slutpunkt</span><span class="sxs-lookup"><span data-stu-id="ced70-135">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="ced70-136">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="ced70-136">Az.Maintenance</span></span>
* <span data-ttu-id="ced70-137">Publicerar slutversion av underhålls-cmdletar för GA</span><span class="sxs-lookup"><span data-stu-id="ced70-137">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ced70-138">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ced70-138">Az.Monitor</span></span>
* <span data-ttu-id="ced70-139">Har lagt till cmdletar för privat länkomfång</span><span class="sxs-lookup"><span data-stu-id="ced70-139">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="ced70-140">'Get-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="ced70-140">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="ced70-141">'Remove-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="ced70-141">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="ced70-142">'New-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="ced70-142">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="ced70-143">'Update-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="ced70-143">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="ced70-144">'Get-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="ced70-144">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="ced70-145">'New-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="ced70-145">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="ced70-146">'Remove-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="ced70-146">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ced70-147">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ced70-147">Az.Network</span></span>
* <span data-ttu-id="ced70-148">Uppdaterade cmdletar för att aktivera anslutning på privat IP för Virtual Network Gateway.</span><span class="sxs-lookup"><span data-stu-id="ced70-148">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="ced70-149">'New-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="ced70-149">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="ced70-150">'Set-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="ced70-150">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="ced70-151">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="ced70-151">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="ced70-152">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="ced70-152">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="ced70-153">Uppdaterade cmdletar för att aktivera FQDN-baserade LocalNetworkGateways och VpnSites</span><span class="sxs-lookup"><span data-stu-id="ced70-153">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="ced70-154">'New-AzLocalNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="ced70-154">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="ced70-155">'New-AzVpnSiteLink'</span><span class="sxs-lookup"><span data-stu-id="ced70-155">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="ced70-156">Stöd har lagts till för IPv6-adresstypen i ExpressRouteCircuitConnectionConfig (Global Reach)</span><span class="sxs-lookup"><span data-stu-id="ced70-156">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="ced70-157">Lade till 'Set-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="ced70-157">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="ced70-158">tillåter inställning av alla befintliga egenskaper inklusive IPv6CircuitConnectionProperties</span><span class="sxs-lookup"><span data-stu-id="ced70-158">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="ced70-159">Uppdaterade 'Add-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="ced70-159">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="ced70-160">Lade till en ytterligare valfri parameter, AddressPrefixType, för att specificera adresstypen för adressprefix</span><span class="sxs-lookup"><span data-stu-id="ced70-160">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="ced70-161">Uppdaterade cmdletar för att aktivera inställningen för DPD-timeout på Virtual Network Gateway-anslutningar.</span><span class="sxs-lookup"><span data-stu-id="ced70-161">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="ced70-162">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ced70-162">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="ced70-163">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ced70-163">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="ced70-164">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ced70-164">Az.PolicyInsights</span></span>
* <span data-ttu-id="ced70-165">Cmdleten "Start-AzPolicyComplianceScan" har lagts till för att utlösa genomsökningar av principefterlevnad</span><span class="sxs-lookup"><span data-stu-id="ced70-165">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="ced70-166">Principdefinition, uppsättningsdefinition och tilldelningsversioner har lagts till i "Get-AzPolicyState"-utdata</span><span class="sxs-lookup"><span data-stu-id="ced70-166">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ced70-167">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ced70-167">Az.ServiceFabric</span></span>
* <span data-ttu-id="ced70-168">Förbättrad kodformatering och användbarhet för "New-AzServiceFabricCluster"-exempel</span><span class="sxs-lookup"><span data-stu-id="ced70-168">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="ced70-169">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ced70-169">Az.Sql</span></span>
* <span data-ttu-id="ced70-170">Lade till cmdletarna "Get-AzSqlInstanceOperation" och "Stop-AzSqlInstanceOperation"</span><span class="sxs-lookup"><span data-stu-id="ced70-170">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="ced70-171">Stöd för granskning för ett lagringskonto i VNet.</span><span class="sxs-lookup"><span data-stu-id="ced70-171">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ced70-172">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ced70-172">Az.Storage</span></span>
* <span data-ttu-id="ced70-173">Lade till meddelande om icke-bakåtkompatibel ändring vid ändring i utdata för Azure File-cmdletar i en framtida version</span><span class="sxs-lookup"><span data-stu-id="ced70-173">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="ced70-174">Stöd för nya SkuName StandardGZRS, StandardRAGZRS när ett lagringskonto skapas/uppdateras</span><span class="sxs-lookup"><span data-stu-id="ced70-174">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="ced70-175">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="ced70-175">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="ced70-176">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="ced70-176">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="ced70-177">Stöd för DataLake Gen2</span><span class="sxs-lookup"><span data-stu-id="ced70-177">Supported DataLake Gen2</span></span> 
    - <span data-ttu-id="ced70-178">'New-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="ced70-178">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="ced70-179">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="ced70-179">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="ced70-180">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="ced70-180">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="ced70-181">'Move-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="ced70-181">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="ced70-182">'Set-AzDataLakeGen2ItemAclObject'</span><span class="sxs-lookup"><span data-stu-id="ced70-182">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="ced70-183">'Update-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="ced70-183">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="ced70-184">'Get-AzDataLakeGen2ItemContent'</span><span class="sxs-lookup"><span data-stu-id="ced70-184">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="ced70-185">'Remove-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="ced70-185">'Remove-AzDataLakeGen2Item'</span></span>

# <a name="azure-powershell-release-notes"></a><span data-ttu-id="ced70-186">Viktig information om Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="ced70-186">Azure PowerShell release notes</span></span>
## <a name="370---march-2020"></a><span data-ttu-id="ced70-187">3.7.0 – mars 2020</span><span class="sxs-lookup"><span data-stu-id="ced70-187">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ced70-188">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ced70-188">Az.Accounts</span></span>
* <span data-ttu-id="ced70-189">Åtgärdade ”Get-AzTenant”/”Get-AzDefault”/”Set-AzDefault”-utlösning av NullReferenceException när du inte är inloggad [#10292]</span><span class="sxs-lookup"><span data-stu-id="ced70-189">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ced70-190">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ced70-190">Az.Compute</span></span>
* <span data-ttu-id="ced70-191">Följande parametrar har lagts till i cmdleten ”New-AzDiskConfig”:</span><span class="sxs-lookup"><span data-stu-id="ced70-191">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span> 
    - <span data-ttu-id="ced70-192">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="ced70-192">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="ced70-193">Tillåten krypteringsegenskap till målparametern för cmdleten ”New-AzGalleryImageVersion”.</span><span class="sxs-lookup"><span data-stu-id="ced70-193">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="ced70-194">Åtgärdade tempDisk-problem för cmdletarna ”Set-AzVmss”-Reimage och ”Invoke-AzVMReimage”.</span><span class="sxs-lookup"><span data-stu-id="ced70-194">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="ced70-195">[#11354]</span><span class="sxs-lookup"><span data-stu-id="ced70-195">[#11354]</span></span>
* <span data-ttu-id="ced70-196">Stöd har lagts till i nedanstående cmdletar för nytt SAP-tillägg</span><span class="sxs-lookup"><span data-stu-id="ced70-196">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="ced70-197">”Set-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="ced70-197">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="ced70-198">”Get-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="ced70-198">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="ced70-199">”Remove-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="ced70-199">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="ced70-200">”Update-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="ced70-200">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="ced70-201">Åtgärdade fel i exempel på hjälpdokument</span><span class="sxs-lookup"><span data-stu-id="ced70-201">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="ced70-202">Visade det exakta strängvärdet för VM PowerState i tabellformat.</span><span class="sxs-lookup"><span data-stu-id="ced70-202">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="ced70-203">”New-AzVmssConfig”: den fasta serialiseringen av egenskapen AutomaticRepairs när SinglePlacementGroup är inaktiverad.</span><span class="sxs-lookup"><span data-stu-id="ced70-203">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="ced70-204">[#11257]</span><span class="sxs-lookup"><span data-stu-id="ced70-204">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ced70-205">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ced70-205">Az.DataFactory</span></span>
* <span data-ttu-id="ced70-206">ADF .Net SDK har uppdaterats till 4.8.0</span><span class="sxs-lookup"><span data-stu-id="ced70-206">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="ced70-207">Valfria parametrar har lagts till i kommandot ”Invoke-AzDataFactoryV2Pipeline” för att stödja omkörning</span><span class="sxs-lookup"><span data-stu-id="ced70-207">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ced70-208">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ced70-208">Az.DataLakeStore</span></span>
* <span data-ttu-id="ced70-209">Lade till beskrivning för icke-bakåtkompatibel ändring för ”Export-AzDataLakeStoreItem” och ”Import-AzDataLakeStoreItem”</span><span class="sxs-lookup"><span data-stu-id="ced70-209">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="ced70-210">Lade till alternativ för bytekodning för ”New-AzDataLakeStoreItem”, ”Add-AzDAtaLakeStoreItemContent” och ”Get-AzDAtaLakeStoreItemContent”</span><span class="sxs-lookup"><span data-stu-id="ced70-210">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="ced70-211">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="ced70-211">Az.HDInsight</span></span>
* <span data-ttu-id="ced70-212">Stöd för att ange en minimal TLS-version som stöds när klustret skapas.</span><span class="sxs-lookup"><span data-stu-id="ced70-212">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ced70-213">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ced70-213">Az.IotHub</span></span>
* <span data-ttu-id="ced70-214">Stöd har lagts till för att hantera distribuerade inställningar per enhet.</span><span class="sxs-lookup"><span data-stu-id="ced70-214">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="ced70-215">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="ced70-215">New Cmdlets are:</span></span>
    - <span data-ttu-id="ced70-216">”Get-AzIotHubDistributedTracing”</span><span class="sxs-lookup"><span data-stu-id="ced70-216">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="ced70-217">”Set-AzIotHubDistributedTracing”</span><span class="sxs-lookup"><span data-stu-id="ced70-217">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ced70-218">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ced70-218">Az.KeyVault</span></span>
* <span data-ttu-id="ced70-219">Ändrade attribut för icke-bakåtkompatibel ändring lades till för ”New-AzKeyVault”</span><span class="sxs-lookup"><span data-stu-id="ced70-219">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ced70-220">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ced70-220">Az.Monitor</span></span>
* <span data-ttu-id="ced70-221">Uppdaterad dokumentation för ”New-AzScheduledQueryRuleLogMetricTrigger”</span><span class="sxs-lookup"><span data-stu-id="ced70-221">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ced70-222">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ced70-222">Az.Network</span></span>
* <span data-ttu-id="ced70-223">Uppdaterade cmdletar för att tillåta VirtualHubVnetConnections mellan klienter</span><span class="sxs-lookup"><span data-stu-id="ced70-223">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="ced70-224">”New-AzVirtualHubVnetConnection”</span><span class="sxs-lookup"><span data-stu-id="ced70-224">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="ced70-225">”Update-AzVirtualHubVnetConnection”</span><span class="sxs-lookup"><span data-stu-id="ced70-225">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="ced70-226">”New-AzVirtualHub”</span><span class="sxs-lookup"><span data-stu-id="ced70-226">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="ced70-227">”Update-AzVirtualHub”</span><span class="sxs-lookup"><span data-stu-id="ced70-227">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="ced70-228">SQL Management SDK-beroende har tagits bort</span><span class="sxs-lookup"><span data-stu-id="ced70-228">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="ced70-229">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ced70-229">Az.PolicyInsights</span></span>
* <span data-ttu-id="ced70-230">Förbättrade felmeddelanden</span><span class="sxs-lookup"><span data-stu-id="ced70-230">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ced70-231">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ced70-231">Az.RecoveryServices</span></span>
* <span data-ttu-id="ced70-232">Azure Site Recovery har lagt till stöd för återaktivering av skydd och uppdaterade VM-egenskaper för virtuella Azure-datorer med krypterad disk.</span><span class="sxs-lookup"><span data-stu-id="ced70-232">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="ced70-233">Lade till Azure Site Recovery VmwareToAzure-egenskaper för DR-övervakning</span><span class="sxs-lookup"><span data-stu-id="ced70-233">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="ced70-234">Azure Backup har lagt till stöd för att försöka uppdatera principuppdateringen för misslyckade objekt på nytt.</span><span class="sxs-lookup"><span data-stu-id="ced70-234">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="ced70-235">Azure Backup lagt till stöd för diskundantagsinställningar under säkerhetskopiering och återställning.</span><span class="sxs-lookup"><span data-stu-id="ced70-235">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="ced70-236">Azure Backup lagt till stöd för att återställa flera filer/mappar i AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="ced70-236">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="ced70-237">Azure Backup lade till support för användardefinierad Resourcegroup-support vid uppdatering av IaasVM-princip</span><span class="sxs-lookup"><span data-stu-id="ced70-237">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="ced70-238">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ced70-238">Az.Resources</span></span>
* <span data-ttu-id="ced70-239">Åtgärdade ”Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType” så att den använder den faktisk apiVersion av resurser i stället för standard-apiVersion [#11267]</span><span class="sxs-lookup"><span data-stu-id="ced70-239">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="ced70-240">Lade till correlationId-loggning för felscenarier</span><span class="sxs-lookup"><span data-stu-id="ced70-240">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="ced70-241">Liten dokumentationsändring för ”Get-AzResourceLock”.</span><span class="sxs-lookup"><span data-stu-id="ced70-241">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="ced70-242">Lade till exempel.</span><span class="sxs-lookup"><span data-stu-id="ced70-242">Added example.</span></span>
* <span data-ttu-id="ced70-243">Undantaget enkelt citattecken i parametervärde för ”Get-AzADUser” [#11317]</span><span class="sxs-lookup"><span data-stu-id="ced70-243">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="ced70-244">Nya cmdletar har lagts till för distributionsskript (”Get-AzDeploymentScript”, ”Get-AzDeploymentScriptLog”, ”Save-AzDeploymentScriptLog”, ”Remove-AzDeploymentScript”)</span><span class="sxs-lookup"><span data-stu-id="ced70-244">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="ced70-245">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ced70-245">Az.Sql</span></span>
* <span data-ttu-id="ced70-246">En läsbar sekundär parameter har lagts till i Invoke-AzSqlDatabaseFailover</span><span class="sxs-lookup"><span data-stu-id="ced70-246">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="ced70-247">Cmdleten Disable-AzSqlServerActiveDirectoryOnlyAuthentication har lagts till</span><span class="sxs-lookup"><span data-stu-id="ced70-247">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="ced70-248">Den sparade känslighet rangordningen när kolumner klassificeras i databasen.</span><span class="sxs-lookup"><span data-stu-id="ced70-248">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="ced70-249">Az.Support</span><span class="sxs-lookup"><span data-stu-id="ced70-249">Az.Support</span></span>
* <span data-ttu-id="ced70-250">Allmän tillgänglighet för ”Az.Support”-modulen</span><span class="sxs-lookup"><span data-stu-id="ced70-250">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ced70-251">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ced70-251">Az.Websites</span></span>
* <span data-ttu-id="ced70-252">Stöd har lagts till för att arbeta med trafikdirigeringsregler för webbappar under nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="ced70-252">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="ced70-253">”Get-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="ced70-253">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="ced70-254">”Update-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="ced70-254">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="ced70-255">”Add-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="ced70-255">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="ced70-256">”Remove-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="ced70-256">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="ced70-257">3.6.1 – mars 2020</span><span class="sxs-lookup"><span data-stu-id="ced70-257">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ced70-258">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ced70-258">Az.Accounts</span></span>
* <span data-ttu-id="ced70-259">Öppna sidan med Azure PowerShell-enkäten i ”Send-Feedback” [#11020]</span><span class="sxs-lookup"><span data-stu-id="ced70-259">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="ced70-260">Visa URL:en för Azure PowerShell-enkäten i ”Resolve-Error” [#11021]</span><span class="sxs-lookup"><span data-stu-id="ced70-260">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="ced70-261">Az-version har lagts till i UserAgent</span><span class="sxs-lookup"><span data-stu-id="ced70-261">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="ced70-262">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ced70-262">Az.ApiManagement</span></span>
* <span data-ttu-id="ced70-263">Stöd har lagts till för att hämta och konfigurera en anpassad domän på DeveloperPortal-slutpunkten [#11007]</span><span class="sxs-lookup"><span data-stu-id="ced70-263">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="ced70-264">”Export-AzApiManagementApi” Stöd har lagts till för att ladda ned API-definition i Json-format [#9987]</span><span class="sxs-lookup"><span data-stu-id="ced70-264">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="ced70-265">”Import-AzApiManagementApi” Stöd har lagts till för att importera OpenApi 3.0-definition från Json-dokument</span><span class="sxs-lookup"><span data-stu-id="ced70-265">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="ced70-266">”New-AzApiManagementIdentityProvider” och ”Set-AzApiManagementIdentityProvider” Stöd har lagts till för att konfigurera ”Signin Tenant” för AAD B2C-provider [#9784]</span><span class="sxs-lookup"><span data-stu-id="ced70-266">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ced70-267">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ced70-267">Az.DataLakeStore</span></span>
* <span data-ttu-id="ced70-268">En referens har uttryckligen lagts till för System.Buffers i csproj och psd1.</span><span class="sxs-lookup"><span data-stu-id="ced70-268">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ced70-269">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ced70-269">Az.IotHub</span></span>
* <span data-ttu-id="ced70-270">Lade till stöd för att hantera enheter i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="ced70-270">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="ced70-271">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="ced70-271">New Cmdlets are:</span></span>
    - <span data-ttu-id="ced70-272">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="ced70-272">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="ced70-273">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="ced70-273">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="ced70-274">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="ced70-274">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="ced70-275">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="ced70-275">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="ced70-276">Stöd har lagts till för att hantera moduler på en mål-IoT-enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="ced70-276">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="ced70-277">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="ced70-277">New Cmdlets are:</span></span>
    - <span data-ttu-id="ced70-278">”Add-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="ced70-278">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="ced70-279">”Get-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="ced70-279">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="ced70-280">”Remove-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="ced70-280">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="ced70-281">”Set-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="ced70-281">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="ced70-282">Cmdlet har lagts till för att hämta anslutningssträngen för en mål-IoT-enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="ced70-282">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="ced70-283">Cmdlet har lagts till för att hämta anslutningssträngen för en modul på en mål-IoT-enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="ced70-283">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="ced70-284">Stöd har lagts till för att hämta/ange en överordnad enhet för en IoT-enhet.</span><span class="sxs-lookup"><span data-stu-id="ced70-284">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="ced70-285">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="ced70-285">New Cmdlets are:</span></span>
    - <span data-ttu-id="ced70-286">”Get-AzIotHubDeviceParent”</span><span class="sxs-lookup"><span data-stu-id="ced70-286">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="ced70-287">”Set-AzIotHubDeviceParent”</span><span class="sxs-lookup"><span data-stu-id="ced70-287">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="ced70-288">Stöd har lagts till för att hantera en enhets överordnade och underordnade relationer.</span><span class="sxs-lookup"><span data-stu-id="ced70-288">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ced70-289">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ced70-289">Az.Monitor</span></span>
* <span data-ttu-id="ced70-290">Utdatavärdet har åtgärdats för ”Get-AzMetricDefinition” [#9714]</span><span class="sxs-lookup"><span data-stu-id="ced70-290">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ced70-291">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ced70-291">Az.Network</span></span>
* <span data-ttu-id="ced70-292">SQL Management SDK har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="ced70-292">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="ced70-293">Ett problem har åtgärdats med namngivningsskillnader i klassen PrivateLinkServiceConnectionState.</span><span class="sxs-lookup"><span data-stu-id="ced70-293">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="ced70-294">Fältet ActionsRequired mappar till ActionRequired.</span><span class="sxs-lookup"><span data-stu-id="ced70-294">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="ced70-295">PublicNetworkAccess har lagts till i ”New-AzSqlServer” och ”Set-AzSqlServer”</span><span class="sxs-lookup"><span data-stu-id="ced70-295">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="ced70-296">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ced70-296">Az.Resources</span></span>
* <span data-ttu-id="ced70-297">Null-referensfel har åtgärdats i ”Get-AzRoleAssignment”</span><span class="sxs-lookup"><span data-stu-id="ced70-297">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="ced70-298">Växlarna ”-Force” och ”-PassThru” är valfria i ”Remove-AzADGroup” [#10849]</span><span class="sxs-lookup"><span data-stu-id="ced70-298">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="ced70-299">Ett problem har åtgärdats som gjorde att ”MailNickname” inte returnerades i ”Remove-AzADGroup” [#11167]</span><span class="sxs-lookup"><span data-stu-id="ced70-299">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="ced70-300">Ett problem har åtgärdats som gjorde att pipe-åtgärden ”Remove-AzADGroup” inte fungerar [#11171]</span><span class="sxs-lookup"><span data-stu-id="ced70-300">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="ced70-301">Ett null-referensfel har åtgärdats i GetAzureRoleAssignmentCommand</span><span class="sxs-lookup"><span data-stu-id="ced70-301">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="ced70-302">Attribut för icke-bakåtkompatibla ändringar har lagts till för kommande ändringar i cmdlets för principer</span><span class="sxs-lookup"><span data-stu-id="ced70-302">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="ced70-303">”Get-AzResourceGroup” har uppdaterats för att utföra taggfiltrering för resursgrupper på serversidan</span><span class="sxs-lookup"><span data-stu-id="ced70-303">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="ced70-304">Utökade Tag-cmdlets stöder -ResourceId</span><span class="sxs-lookup"><span data-stu-id="ced70-304">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="ced70-305">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="ced70-305">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="ced70-306">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="ced70-306">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="ced70-307">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="ced70-307">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="ced70-308">Ny Tag-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="ced70-308">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="ced70-309">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="ced70-309">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="ced70-310">Flyttade ScopedDeployment från SDK 3.3.0</span><span class="sxs-lookup"><span data-stu-id="ced70-310">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="ced70-311">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ced70-311">Az.Sql</span></span>
* <span data-ttu-id="ced70-312">PublicNetworkAccess har lagts till i ”New-AzSqlServer” och ”Set-AzSqlServer”</span><span class="sxs-lookup"><span data-stu-id="ced70-312">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="ced70-313">Stöd har lagts till för konfiguration av säkerhetskopiering för långsiktig kvarhållning för hanterade databaser</span><span class="sxs-lookup"><span data-stu-id="ced70-313">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="ced70-314">Hämta/ange LTR-princip på en hanterad databas</span><span class="sxs-lookup"><span data-stu-id="ced70-314">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="ced70-315">Hämta LTR-säkerhetskopior efter hanterad databas, hanterad instans eller plats</span><span class="sxs-lookup"><span data-stu-id="ced70-315">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="ced70-316">Ta bort en LTR-säkerhetskopia</span><span class="sxs-lookup"><span data-stu-id="ced70-316">Remove an LTR backup</span></span>
    - <span data-ttu-id="ced70-317">Återställa en LTR-säkerhetskopia för att skapa en ny hanterad databas</span><span class="sxs-lookup"><span data-stu-id="ced70-317">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="ced70-318">MinimalTlsVersion har lagts till för New-AzSqlServer och Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="ced70-318">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="ced70-319">MinimalTlsVersion har lagts till för New-AzSqlInstance och Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="ced70-319">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="ced70-320">SQL SDK-versionen för Az.Network har ändrats</span><span class="sxs-lookup"><span data-stu-id="ced70-320">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ced70-321">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ced70-321">Az.Storage</span></span>
* <span data-ttu-id="ced70-322">AllowProtectedAppendWrite stöds i ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="ced70-322">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="ced70-323">”Set-AzRmStorageContainerImmutabilityPolicy”</span><span class="sxs-lookup"><span data-stu-id="ced70-323">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="ced70-324">Varningsmeddelande har lagts till om icke-bakåtkompatibel ändring för ändring av typen AzureStorageTable i en senare version</span><span class="sxs-lookup"><span data-stu-id="ced70-324">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="ced70-325">”New-AzStorageTable”</span><span class="sxs-lookup"><span data-stu-id="ced70-325">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="ced70-326">”Get-AzStorageTable”</span><span class="sxs-lookup"><span data-stu-id="ced70-326">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ced70-327">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ced70-327">Az.Websites</span></span>
* <span data-ttu-id="ced70-328">Tag-parametern har lagts till för ”New-AzAppServicePlan” och ”Set-AzAppServicePlan”</span><span class="sxs-lookup"><span data-stu-id="ced70-328">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="ced70-329">Stoppa cmdlet-körning om ett undantag uppstår när en anpassad domän läggs till på en webbplats</span><span class="sxs-lookup"><span data-stu-id="ced70-329">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="ced70-330">Stöd har lagts till för att utföra åtgärder för App Services som inte tillhör samma resursgrupp som App Services-planen</span><span class="sxs-lookup"><span data-stu-id="ced70-330">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="ced70-331">Åtkomstbegränsning har tillämpats på WebApp/Function i olika resursgrupper</span><span class="sxs-lookup"><span data-stu-id="ced70-331">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="ced70-332">Ett problem har åtgärdats för att ange anpassade värdnamn för WebAppSlots</span><span class="sxs-lookup"><span data-stu-id="ced70-332">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="ced70-333">3.5.0 – februari 2020</span><span class="sxs-lookup"><span data-stu-id="ced70-333">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="ced70-334">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="ced70-334">Highlights since the last major release</span></span>
* <span data-ttu-id="ced70-335">Uppdaterade telemetri på klientsidan.</span><span class="sxs-lookup"><span data-stu-id="ced70-335">Updated client side telemetry.</span></span>
* <span data-ttu-id="ced70-336">Az.IotHub lade till cmdletar som stöd för att hantera enheter.</span><span class="sxs-lookup"><span data-stu-id="ced70-336">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="ced70-337">Az.SqlVirtualMachine lade till cmdletar för lyssningsfunktion för tillgänglighetsgrupp.</span><span class="sxs-lookup"><span data-stu-id="ced70-337">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="ced70-338">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ced70-338">Az.Accounts</span></span>
* <span data-ttu-id="ced70-339">Lade till SubscriptionId, TenantId och körningstid i data för telemetri på klientsidan</span><span class="sxs-lookup"><span data-stu-id="ced70-339">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ced70-340">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ced70-340">Az.Automation</span></span>
* <span data-ttu-id="ced70-341">Åtgärdade skrivfel i exempel 1 i referensdokumentation för ”New-AzAutomationSoftwareUpdateConfiguration”</span><span class="sxs-lookup"><span data-stu-id="ced70-341">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="ced70-342">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ced70-342">Az.CognitiveServices</span></span>
* <span data-ttu-id="ced70-343">Uppdaterade SDK till 7.0</span><span class="sxs-lookup"><span data-stu-id="ced70-343">Updated SDK to 7.0</span></span>
* <span data-ttu-id="ced70-344">Förbättrade felmeddelande vid serversvar om tom brödtext</span><span class="sxs-lookup"><span data-stu-id="ced70-344">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ced70-345">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ced70-345">Az.Compute</span></span>
* <span data-ttu-id="ced70-346">Tillät tomt värde för ProximityPlacementGroupId under uppdatering</span><span class="sxs-lookup"><span data-stu-id="ced70-346">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="ced70-347">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="ced70-347">Az.FrontDoor</span></span>
* <span data-ttu-id="ced70-348">Lade till cmdlet för att hämta hanterade regeldefinitioner som kan användas i WAF</span><span class="sxs-lookup"><span data-stu-id="ced70-348">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ced70-349">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ced70-349">Az.IotHub</span></span>
* <span data-ttu-id="ced70-350">Lade till stöd för att hantera enheter i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="ced70-350">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="ced70-351">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="ced70-351">New Cmdlets are:</span></span>
    - <span data-ttu-id="ced70-352">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="ced70-352">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="ced70-353">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="ced70-353">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="ced70-354">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="ced70-354">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="ced70-355">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="ced70-355">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ced70-356">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ced70-356">Az.KeyVault</span></span>
* <span data-ttu-id="ced70-357">Åtgärdade duplicerad text för Add-AzKeyVaultKey.md</span><span class="sxs-lookup"><span data-stu-id="ced70-357">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ced70-358">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ced70-358">Az.Monitor</span></span>
* <span data-ttu-id="ced70-359">Åtgärdade beskrivning av cmdleten Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="ced70-359">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="ced70-360">En ny parameter med namnet ActionGroupId har lagts till i kommandot ”New-AzMetricAlertRuleV2”.</span><span class="sxs-lookup"><span data-stu-id="ced70-360">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="ced70-361">Användaren kan ange ActionGroupId(string) eller ActionGroup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="ced70-361">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ced70-362">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ced70-362">Az.Network</span></span>
* <span data-ttu-id="ced70-363">Lade till en extra parameteranteckning för parametern ”-EnableProxyProtocol” för cmdleten ”New-AzPrivateLinkService”.</span><span class="sxs-lookup"><span data-stu-id="ced70-363">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="ced70-364">Åtgärdade FilterData-exempel i Start-AzVirtualNetworkGatewayConnectionPacketCapture.md och Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="ced70-364">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="ced70-365">Lade till paketinsamlingsexempel för att samla in alla inre och yttre paket i Start-AzVirtualNetworkGatewayConnectionPacketCapture.md och Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="ced70-365">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="ced70-366">Lade till stöd för Azure-brandväggsprincip på VNet-brandväggar</span><span class="sxs-lookup"><span data-stu-id="ced70-366">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="ced70-367">Inga nya cmdletar har lagts till.</span><span class="sxs-lookup"><span data-stu-id="ced70-367">No new cmdlets are added.</span></span> <span data-ttu-id="ced70-368">Lättar begränsningen för brandväggsprincip på VNet-brandväggar</span><span class="sxs-lookup"><span data-stu-id="ced70-368">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ced70-369">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ced70-369">Az.RecoveryServices</span></span>
* <span data-ttu-id="ced70-370">Lade till stöd för Restore-as-files för SQL-databaser.</span><span class="sxs-lookup"><span data-stu-id="ced70-370">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ced70-371">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ced70-371">Az.Resources</span></span>
* <span data-ttu-id="ced70-372">Omstrukturerade cmdletar för malldistribution</span><span class="sxs-lookup"><span data-stu-id="ced70-372">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="ced70-373">Lade till nya cmdletar för att hantera distributioner i hanteringsgruppen: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ced70-373">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="ced70-374">Lade till nya cmdletar för att hantera distributioner i klientorganisationsområdet: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="ced70-374">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="ced70-375">Omstrukturerade \*-AzDeployment-cmdletar för att fungera specifikt i prenumerationsomfattningen</span><span class="sxs-lookup"><span data-stu-id="ced70-375">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="ced70-376">Skapade alias \*-AzSubscriptionDeployment för \*-AzDeployment-cmdletar</span><span class="sxs-lookup"><span data-stu-id="ced70-376">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="ced70-377">Åtgärdade ”Update-AzADApplication” när parametern ”AvailableToOtherTenants” inte har angetts</span><span class="sxs-lookup"><span data-stu-id="ced70-377">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="ced70-378">Tog bort ApplicationObjectWithoutCredentialParameterSet för att undvika AmbiguousParameterSetException.</span><span class="sxs-lookup"><span data-stu-id="ced70-378">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="ced70-379">Återskapade hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="ced70-379">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="ced70-380">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ced70-380">Az.Sql</span></span>
* <span data-ttu-id="ced70-381">Lade till stöd för återställning till tidpunkt mellan prenumerationer på hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="ced70-381">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="ced70-382">Lade till stöd för att ändra befintlig SQL Managed Instance-maskinvarugenerering</span><span class="sxs-lookup"><span data-stu-id="ced70-382">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="ced70-383">Åtgärdade ”Update-AzSqlServerVulnerabilityAssessmentSetting”-hjälpexempel: parameter/egenskapsutdata - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="ced70-383">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="ced70-384">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="ced70-384">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="ced70-385">Lade till cmdletar för lyssningsfunktion för tillgänglighetsgrupp</span><span class="sxs-lookup"><span data-stu-id="ced70-385">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="ced70-386">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="ced70-386">Az.StorageSync</span></span>
* <span data-ttu-id="ced70-387">Uppdaterade teckenuppsättningar som stöds i ”Invoke-AzStorageSyncCompatibilityCheck”.</span><span class="sxs-lookup"><span data-stu-id="ced70-387">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="ced70-388">3.4.0 – februari 2020</span><span class="sxs-lookup"><span data-stu-id="ced70-388">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="ced70-389">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="ced70-389">Highlights since the last major release</span></span>
* <span data-ttu-id="ced70-390">Första Az.CosmosDB-versionen 0.1.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="ced70-390">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="ced70-391">Stöd för Az.Network ConnectionMonitor V2 har lagts till</span><span class="sxs-lookup"><span data-stu-id="ced70-391">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="ced70-392">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ced70-392">Az.Accounts</span></span>
* <span data-ttu-id="ced70-393">Inaktivera automatisk sparande av kontext när AzureRmContext.json inte är tillgängligt</span><span class="sxs-lookup"><span data-stu-id="ced70-393">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="ced70-394">Uppdatera referensen till Azure Powershell Common till 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="ced70-394">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="ced70-395">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ced70-395">Az.ApiManagement</span></span>
* <span data-ttu-id="ced70-396">**Get-AzApiManagementApiSchema** Hämtning av Open-Api-schema som är associerat med ett API har åtgärdats   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="ced70-396">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="ced70-397">**New-AzApiManagementProduct**\* och **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="ced70-397">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="ced70-398">Åtgärda dokumentation för https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="ced70-398">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="ced70-399">**Set-AzApiManagementApi** Exempel för att visa hur ServiceUrl uppdateras med hjälp av cmdleten har lagts till</span><span class="sxs-lookup"><span data-stu-id="ced70-399">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ced70-400">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ced70-400">Az.Compute</span></span>
* <span data-ttu-id="ced70-401">Begränsa antalet VM-status till 100 för att undvika begränsning när Get-AzVM -Status utförs utan VM-namn.</span><span class="sxs-lookup"><span data-stu-id="ced70-401">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="ced70-402">Lägg till cmdleten Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="ced70-402">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="ced70-403">Lägg till parametrarna EncryptionType och DiskEncryptionSetId i följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="ced70-403">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="ced70-404">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="ced70-404">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="ced70-405">Lägg till parametern ColocationStatus för cmdleten Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="ced70-405">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ced70-406">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ced70-406">Az.DataFactory</span></span>
* <span data-ttu-id="ced70-407">Uppdatera ADF .Net SDK-versionen till 4.7.0</span><span class="sxs-lookup"><span data-stu-id="ced70-407">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="ced70-408">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="ced70-408">Az.DeploymentManager</span></span>
* <span data-ttu-id="ced70-409">Lägger till LIST-åtgärder för resurser</span><span class="sxs-lookup"><span data-stu-id="ced70-409">Adds LIST operations for resources</span></span>
* <span data-ttu-id="ced70-410">Lägger till funktion för att utföra åtgärder för hälsokontrollsteg</span><span class="sxs-lookup"><span data-stu-id="ced70-410">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="ced70-411">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="ced70-411">Az.HDInsight</span></span>
* <span data-ttu-id="ced70-412">Åtgärda dokumentfel för New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="ced70-412">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ced70-413">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ced70-413">Az.KeyVault</span></span>
* <span data-ttu-id="ced70-414">Lägg till Name-alias för attributet VaultName så att Remove-AzureKeyVault stämmer överens med New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="ced70-414">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ced70-415">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ced70-415">Az.Network</span></span>
* <span data-ttu-id="ced70-416">Nytt exempel har lagts till i Set-AzNetworkWatcherConfigFlowLog.md för att demonstrera ett inaktiveringsscenario för Trafikanalys.</span><span class="sxs-lookup"><span data-stu-id="ced70-416">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="ced70-417">Lägg till stöd för att tilldela konfiguration av hanterings-IP till Azure Firewall – ett dedikerat undernät och en offentlig IP som brandväggen använder för dess hanteringstrafik</span><span class="sxs-lookup"><span data-stu-id="ced70-417">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="ced70-418">Cmdleten New-AzFirewall har uppdaterats:</span><span class="sxs-lookup"><span data-stu-id="ced70-418">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="ced70-419">Parametern -ManagementPublicIpAddress (inte obligatorisk) som accepterar ett offentligt IP-adressobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="ced70-419">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="ced70-420">Metoden SetManagementIpConfiguration har lagts till för brandväggsobjekt – kräver ett undernät och en offentlig IP-adress som indata – undernätets namn måste vara ”AzureFirewallManagementSubnet”</span><span class="sxs-lookup"><span data-stu-id="ced70-420">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="ced70-421">Exempel för Get-AzNetworkSecurityGroup har korrigerats så att exempel visas för NSG:er i stället för nätverksgränssnitt.</span><span class="sxs-lookup"><span data-stu-id="ced70-421">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="ced70-422">Ett skrivfel har åtgärdats i kommandot New-AzVpnSite som hindrade kompletteraren för resurs-ID från att fylla i en parameter.</span><span class="sxs-lookup"><span data-stu-id="ced70-422">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="ced70-423">Stöd för Url-konfiguration i åtgärdsuppsättningen för omskrivningsregler i Application Gateway har lagts till</span><span class="sxs-lookup"><span data-stu-id="ced70-423">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="ced70-424">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="ced70-424">New cmdlets added:</span></span>
        - <span data-ttu-id="ced70-425">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="ced70-425">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="ced70-426">Cmdletar har uppdaterats med den valfria parametern -UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="ced70-426">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="ced70-427">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="ced70-427">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="ced70-428">Lägg till stöd för resurser för NetworkWatcher ConnectionMonitor version 2</span><span class="sxs-lookup"><span data-stu-id="ced70-428">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="ced70-429">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ced70-429">Az.PolicyInsights</span></span>
* <span data-ttu-id="ced70-430">Stöd för utvärdering av efterlevnad innan fastställande av vilken resurs som ska åtgärdas</span><span class="sxs-lookup"><span data-stu-id="ced70-430">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="ced70-431">Lägg till parametern ”-ResourceDiscoverMode” för Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="ced70-431">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="ced70-432">Lägg till cmdleten Get-AzPolicyMetadata för att hämta resurser för principmetadata</span><span class="sxs-lookup"><span data-stu-id="ced70-432">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="ced70-433">Get-AzPolicyState och Get-AzPolicyStateSummary för API-versionen 2019-10-01 har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="ced70-433">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ced70-434">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ced70-434">Az.RecoveryServices</span></span>
* <span data-ttu-id="ced70-435">Azure Site Recovery-stöd för att ta bort en replikerad disk.</span><span class="sxs-lookup"><span data-stu-id="ced70-435">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="ced70-436">Tillagt Azure Backup-stöd för att lägga till taggar när ett Recovery Services-valv skapas.</span><span class="sxs-lookup"><span data-stu-id="ced70-436">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ced70-437">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ced70-437">Az.Resources</span></span>
* <span data-ttu-id="ced70-438">Gör -Scope valfritt i cmdletarna \*-AzPolicyAssignment med standardinställning till kontextprenumeration</span><span class="sxs-lookup"><span data-stu-id="ced70-438">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="ced70-439">Lägg till exempel på att skapa ADServicePrincipal med lösenord och nyckelautentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="ced70-439">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="ced70-440">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ced70-440">Az.Sql</span></span>
<span data-ttu-id="ced70-441">Åtgärda cmdleten New-AzSqlDatabaseSecondary så att existensen PartnerDatabaseName kontrolleras i stället för existensen DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="ced70-441">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ced70-442">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ced70-442">Az.Storage</span></span>
* <span data-ttu-id="ced70-443">Stöd för angivning av krypteringsnyckeltyp för Tabell/kö i Skapa lagringskonto</span><span class="sxs-lookup"><span data-stu-id="ced70-443">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="ced70-444">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ced70-444">New-AzStorageAccount</span></span>
* <span data-ttu-id="ced70-445">Visa RequestId när StorageException inte har ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="ced70-445">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="ced70-446">Åtgärda exempel 6 för cmdleten Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="ced70-446">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ced70-447">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ced70-447">Az.Websites</span></span>
* <span data-ttu-id="ced70-448">Set-AzWebapp och Set-AzWebappSlot stöder egenskaperna AlwaysOn, MinTls och FtpsState</span><span class="sxs-lookup"><span data-stu-id="ced70-448">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="ced70-449">Åtgärdar problemet där inställning av HttpsOnly samtidigt som AppservicePlan ändrades med det enskilda kommandot Set-AzWebApp återställde HttpsOnly till standardvärdet</span><span class="sxs-lookup"><span data-stu-id="ced70-449">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="ced70-450">3.3.0 – januari 2020</span><span class="sxs-lookup"><span data-stu-id="ced70-450">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ced70-451">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ced70-451">Az.Accounts</span></span>
* <span data-ttu-id="ced70-452">Nu stöder Add-AzEnvironment och Set-AzEnvironment parametrarna AzureAttestationServiceEndpointResourceId och AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="ced70-452">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="ced70-453">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="ced70-453">Az.Cdn</span></span>
* <span data-ttu-id="ced70-454">Information om felsvar visas i New-AzCdnEndpoint-cmdleten</span><span class="sxs-lookup"><span data-stu-id="ced70-454">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ced70-455">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ced70-455">Az.Compute</span></span>
* <span data-ttu-id="ced70-456">Set-AzVMCustomScriptExtension-cmdleten har åtgärdats för en virtuell dator med hanterad OD-disk som inte har någon operativsystemprofil.</span><span class="sxs-lookup"><span data-stu-id="ced70-456">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="ced70-457">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="ced70-457">Az.ContainerInstance</span></span>
* <span data-ttu-id="ced70-458">Parameternamn som används med New-AzContainerGroup-exempel har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="ced70-458">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="ced70-459">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="ced70-459">Az.DataBoxEdge</span></span>
* <span data-ttu-id="ced70-460">Cmdleten ”Get-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="ced70-460">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="ced70-461">Hämta gränslagringscontainern</span><span class="sxs-lookup"><span data-stu-id="ced70-461">Get the Edge Storage Container</span></span>
* <span data-ttu-id="ced70-462">Cmdleten ”New-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="ced70-462">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="ced70-463">Skapa en ny gränslagringscontainer</span><span class="sxs-lookup"><span data-stu-id="ced70-463">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="ced70-464">Cmdleten ”Remove-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="ced70-464">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="ced70-465">Ta bort gränslagringscontainern</span><span class="sxs-lookup"><span data-stu-id="ced70-465">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="ced70-466">Cmdleten ”Invoke-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="ced70-466">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="ced70-467">Anropa åtgärd för att uppdatera data i gränslagringscontainer</span><span class="sxs-lookup"><span data-stu-id="ced70-467">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="ced70-468">Cmdleten ”Get-AzDataBoxEdgeStorageAccount” har lagts till</span><span class="sxs-lookup"><span data-stu-id="ced70-468">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="ced70-469">Hämta gränslagringskontot</span><span class="sxs-lookup"><span data-stu-id="ced70-469">Get the Edge Storage Account</span></span>
* <span data-ttu-id="ced70-470">Cmdleten ”New-AzDataBoxEdgeStorageAccount” har lagts till</span><span class="sxs-lookup"><span data-stu-id="ced70-470">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="ced70-471">Skapa ett nytt gränslagringskonto</span><span class="sxs-lookup"><span data-stu-id="ced70-471">Create new Edge Storage Account</span></span>
* <span data-ttu-id="ced70-472">Cmdleten ”Remove-AzDataBoxEdgeStorageAccount” har lagts till</span><span class="sxs-lookup"><span data-stu-id="ced70-472">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="ced70-473">Ta bort gränslagringskontot</span><span class="sxs-lookup"><span data-stu-id="ced70-473">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="ced70-474">Anropa cmdleten ”Invoke-AzDataBoxEdgeShare”</span><span class="sxs-lookup"><span data-stu-id="ced70-474">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="ced70-475">Anropa åtgärd för att uppdatera resursdata</span><span class="sxs-lookup"><span data-stu-id="ced70-475">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="ced70-476">Cmdleten ”Set-AzDataBoxEdgeStorageAccountCredential” har lagts till</span><span class="sxs-lookup"><span data-stu-id="ced70-476">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="ced70-477">Ange autentiseringsuppgifter för az databoxedge-lagringskonto</span><span class="sxs-lookup"><span data-stu-id="ced70-477">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ced70-478">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ced70-478">Az.DataFactory</span></span>
* <span data-ttu-id="ced70-479">Lägg till AutoUpdateETA-, LatestVersion-, PushedVersion-, TaskQueueId- och VersionStatus-egenskaper för Get-AzDataFactoryV2IntegrationRuntime-cmd</span><span class="sxs-lookup"><span data-stu-id="ced70-479">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="ced70-480">Uppdatera ADF .Net SDK-versionen till 4.6.0</span><span class="sxs-lookup"><span data-stu-id="ced70-480">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="ced70-481">Lägg till parametern ”PublicIPs” för ”Set-AzureRmDataFactoryV2IntegrationRuntime”-cmd så att Azure-SSIS IR kan skapas med statiska offentliga IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="ced70-481">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="ced70-482">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="ced70-482">Az.DevTestLabs</span></span>
* <span data-ttu-id="ced70-483">Ta bort den brutna länken i Get-AzDtlAllowedVMSizesPolicy.md</span><span class="sxs-lookup"><span data-stu-id="ced70-483">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="ced70-484">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="ced70-484">Az.EventHub</span></span>
* <span data-ttu-id="ced70-485">Korrigering av problem 10634: Åtgärda referensen till null-objekt för eventhubnamespace-borttagning</span><span class="sxs-lookup"><span data-stu-id="ced70-485">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="ced70-486">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="ced70-486">Az.HDInsight</span></span>
* <span data-ttu-id="ced70-487">Åtgärda Invoke-AzHDInsightHiveJob.md-fel.</span><span class="sxs-lookup"><span data-stu-id="ced70-487">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="ced70-488">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="ced70-488">Az.MachineLearning</span></span>
* <span data-ttu-id="ced70-489">Nedanstående cmdletar har tagits bort eftersom MachineLearningCompute inte längre är tillgängligt</span><span class="sxs-lookup"><span data-stu-id="ced70-489">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="ced70-490">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="ced70-490">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="ced70-491">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="ced70-491">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="ced70-492">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="ced70-492">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="ced70-493">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="ced70-493">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="ced70-494">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="ced70-494">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="ced70-495">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="ced70-495">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="ced70-496">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="ced70-496">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ced70-497">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ced70-497">Az.Network</span></span>
* <span data-ttu-id="ced70-498">Uppgradera beroende av Microsoft.Azure.Management.Sql från 1.36-preview till 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="ced70-498">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ced70-499">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ced70-499">Az.RecoveryServices</span></span>
* <span data-ttu-id="ced70-500">Ändrat Azure Site Recovery-stöd för krypterade vilande data på virtuella datorer med hanterade diskar med kundhanterade nycklar för Azure till Azure-providern.</span><span class="sxs-lookup"><span data-stu-id="ced70-500">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="ced70-501">Azure Site Recovery-stöd för att ange ID för diskkrypteringsuppsättning som valfri inmatning för aktivering av skydd för VMware till Azure.</span><span class="sxs-lookup"><span data-stu-id="ced70-501">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="ced70-502">Azure Site Recovery-stöd för att ange ID för diskkrypteringsuppsättning som valfri inmatning på disknivå för aktivering av skydd för VMware till Azure.</span><span class="sxs-lookup"><span data-stu-id="ced70-502">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="ced70-503">Azure Site Recovery-stöd för att uppdatera replikeringsskyddade objekt med mappning för diskkrypteringsuppsättning för HyperV till Azure.</span><span class="sxs-lookup"><span data-stu-id="ced70-503">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ced70-504">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ced70-504">Az.Resources</span></span>
* <span data-ttu-id="ced70-505">Åtgärda ett fel i hjälpdokument för ”Remove-AzTag”.</span><span class="sxs-lookup"><span data-stu-id="ced70-505">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="ced70-506">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ced70-506">Az.Sql</span></span>
* <span data-ttu-id="ced70-507">Åtgärda funktioner i cmdletar för att ange baslinjen för sårbarhetsbedömning för arbete med huvuddatabasen för Azure-databasen och begränsa den för systemdatabaser på hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="ced70-507">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="ced70-508">Åtgärda ett fel när en redundansgrupp för en SQL-instans skapas</span><span class="sxs-lookup"><span data-stu-id="ced70-508">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="ced70-509">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="ced70-509">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="ced70-510">Lägg till DR som en ny giltig licenstyp</span><span class="sxs-lookup"><span data-stu-id="ced70-510">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ced70-511">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ced70-511">Az.Storage</span></span>
* <span data-ttu-id="ced70-512">Lägg till varningsmeddelande om icke-bakåtkompatibel ändring för DefaultAction-värdeändring i en framtida version</span><span class="sxs-lookup"><span data-stu-id="ced70-512">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="ced70-513">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="ced70-513">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="ced70-514">Stöd för att hämta lagringskontots senaste synkroniseringstid genom att köra get-AzureRMStorageAccount med parametern -IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="ced70-514">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="ced70-515">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ced70-515">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="ced70-516">3.2.0 – December 2019</span><span class="sxs-lookup"><span data-stu-id="ced70-516">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="ced70-517">Allmänt</span><span class="sxs-lookup"><span data-stu-id="ced70-517">General</span></span>
* <span data-ttu-id="ced70-518">Uppdatera referenser i .psd1 för att använda relativa sökvägar för alla moduler</span><span class="sxs-lookup"><span data-stu-id="ced70-518">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="ced70-519">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ced70-519">Az.Accounts</span></span>
* <span data-ttu-id="ced70-520">Ange rätt UserAgent för telemetri på klientsidan för Az 4.0 preview</span><span class="sxs-lookup"><span data-stu-id="ced70-520">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="ced70-521">Visa användarvänligt felmeddelande när kontexten är null i Az 4.0 preview</span><span class="sxs-lookup"><span data-stu-id="ced70-521">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="ced70-522">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="ced70-522">Az.Batch</span></span>
* <span data-ttu-id="ced70-523">Korrigera problem [#10602](https://github.com/Azure/azure-powershell/issues/10602), där **New-AzBatchPool** skickade VirtualMachineConfiguration.ContainerConfiguration eller VirtualMachineConfiguration.DataDisks på ett felaktigt sätt till servern.</span><span class="sxs-lookup"><span data-stu-id="ced70-523">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ced70-524">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ced70-524">Az.DataFactory</span></span>
* <span data-ttu-id="ced70-525">Uppdatera ADF .Net SDK-versionen till 4.5.0</span><span class="sxs-lookup"><span data-stu-id="ced70-525">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="ced70-526">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="ced70-526">Az.FrontDoor</span></span>
* <span data-ttu-id="ced70-527">Stöd har lagts till för undantag för hanterade regler för brandväggen för webbaserade program</span><span class="sxs-lookup"><span data-stu-id="ced70-527">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="ced70-528">Lägg till SocketAddr för automatisk komplettering</span><span class="sxs-lookup"><span data-stu-id="ced70-528">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="ced70-529">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="ced70-529">Az.HealthcareApis</span></span>
* <span data-ttu-id="ced70-530">Undantagshantering</span><span class="sxs-lookup"><span data-stu-id="ced70-530">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ced70-531">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ced70-531">Az.KeyVault</span></span>
* <span data-ttu-id="ced70-532">Åtgärdat fel vid åtkomst av värde som kanske inte har angetts</span><span class="sxs-lookup"><span data-stu-id="ced70-532">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="ced70-533">Hantering av ECC-certifikat (Elliptic Curve Cryptography)</span><span class="sxs-lookup"><span data-stu-id="ced70-533">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="ced70-534">Stöd har lagts till för att ange kurvan för certifikatprinciper</span><span class="sxs-lookup"><span data-stu-id="ced70-534">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ced70-535">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ced70-535">Az.Monitor</span></span>
* <span data-ttu-id="ced70-536">Lägger till valfritt argument i kommandot Lägg till diagnostikinställningar.</span><span class="sxs-lookup"><span data-stu-id="ced70-536">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="ced70-537">Ett växelargument som om det finns visar att exporten till Log Analytics måste ske till ett fast schema (kallas även</span><span class="sxs-lookup"><span data-stu-id="ced70-537">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="ced70-538">dedikerad, datatyp)</span><span class="sxs-lookup"><span data-stu-id="ced70-538">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ced70-539">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ced70-539">Az.Network</span></span>
* <span data-ttu-id="ced70-540">Stöd för IpGroups i program-, NAT- och nätverksregler för Azure Firewall.</span><span class="sxs-lookup"><span data-stu-id="ced70-540">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ced70-541">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ced70-541">Az.Resources</span></span>
* <span data-ttu-id="ced70-542">Åtgärda ett problem där malldistributionen inte kan läsa en mallparameter om dess namn står i konflikt med ett inbyggt parameternamn.</span><span class="sxs-lookup"><span data-stu-id="ced70-542">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="ced70-543">Uppdaterade princip-cmdletar för att använda den nya API-versionen 2019-09-01 som introducerar grupperingsstöd inom principuppsättningsdefinitioner.</span><span class="sxs-lookup"><span data-stu-id="ced70-543">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="ced70-544">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ced70-544">Az.Sql</span></span>
* <span data-ttu-id="ced70-545">Uppgraderad funktion för att skapa lagring i automatisk aktivering av sårbarhetsbedömning till StorageV2</span><span class="sxs-lookup"><span data-stu-id="ced70-545">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ced70-546">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ced70-546">Az.Storage</span></span>
* <span data-ttu-id="ced70-547">Stöd för generering av blob/container-identitetsbaserad SAS-token med lagringskontextbaserad på OAuth-autentisering</span><span class="sxs-lookup"><span data-stu-id="ced70-547">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="ced70-548">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="ced70-548">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="ced70-549">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="ced70-549">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="ced70-550">Stöd för återkallning av användardelegeringsnycklar för lagringskonto för att återkalla alla SAS-token</span><span class="sxs-lookup"><span data-stu-id="ced70-550">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="ced70-551">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="ced70-551">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="ced70-552">Uppgradera till Microsoft.Azure.Management.Storage 14.2.0 för att stödja den nya API-versionen 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="ced70-552">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="ced70-553">Stöd för QuotaGiB (resurskvot i Gibibye) för värden över 5120 i hanteringsplanet för cmdletar för filresurser och parameteraliaset. Quota har också lagts till för parametern ”QuotaGiB”.</span><span class="sxs-lookup"><span data-stu-id="ced70-553">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="ced70-554">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="ced70-554">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="ced70-555">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="ced70-555">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="ced70-556">Lägg till parameteraliaset QuotaGiB i parametern Quota</span><span class="sxs-lookup"><span data-stu-id="ced70-556">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="ced70-557">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="ced70-557">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="ced70-558">Åtgärda problemet att Set-AzStorageContainerAcl kan rensa den lagrade åtkomstprincipen</span><span class="sxs-lookup"><span data-stu-id="ced70-558">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="ced70-559">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="ced70-559">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="ced70-560">3.1.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="ced70-560">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="ced70-561">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="ced70-561">Highlights since the last major release</span></span>
* <span data-ttu-id="ced70-562">Az.DataBoxEdge 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="ced70-562">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="ced70-563">Az.SqlVirtualMachine 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="ced70-563">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ced70-564">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ced70-564">Az.Compute</span></span>
* <span data-ttu-id="ced70-565">Funktion för att använda en virtuell dator igen</span><span class="sxs-lookup"><span data-stu-id="ced70-565">VM Reapply feature</span></span>
    - <span data-ttu-id="ced70-566">Lägg till parameter för att använda igen till cmdleten Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="ced70-566">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="ced70-567">Funktionen AutomaticRepairs i VM-skalningsuppsättningar:</span><span class="sxs-lookup"><span data-stu-id="ced70-567">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="ced70-568">Lägg till parametrarna EnableAutomaticRepair, AutomaticRepairGracePeriod och AutomaticRepairMaxInstanceRepairsPercent till följande cmdletar:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ced70-568">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="ced70-569">Stöd för galleriavbildningar i flera klientorganisationer för New-AzVM</span><span class="sxs-lookup"><span data-stu-id="ced70-569">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="ced70-570">Lägg till "Spot" till argumentslutföraren i prioritetsparametern i cmdletarna New-AzVM, New-AzVMConfig och New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ced70-570">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="ced70-571">Lägg till parametrarna DiskIOPSReadWrite och DiskMBpsReadWrite till cmdleten Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="ced70-571">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="ced70-572">Ändra parametern SourceImageId för cmdleten New-AzGalleryImageVersion till valfri</span><span class="sxs-lookup"><span data-stu-id="ced70-572">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="ced70-573">Lägg till parametrarna OSDiskImage och DataDiskImage till cmdleten New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="ced70-573">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="ced70-574">Lägg till parametern HyperVGeneration till cmdleten New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="ced70-574">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="ced70-575">Lägg till parametern SkipExtensionsOnOverprovisionedVMs till cmdletarna New-AzVmss, New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ced70-575">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="ced70-576">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="ced70-576">Az.DataBoxEdge</span></span>
* <span data-ttu-id="ced70-577">Cmdleten `Get-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="ced70-577">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="ced70-578">Hämta ordning</span><span class="sxs-lookup"><span data-stu-id="ced70-578">Get the Order</span></span>
* <span data-ttu-id="ced70-579">Cmdleten `New-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="ced70-579">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="ced70-580">Skapa ny ordning</span><span class="sxs-lookup"><span data-stu-id="ced70-580">Create new Order</span></span>
* <span data-ttu-id="ced70-581">Cmdleten `Remove-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="ced70-581">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="ced70-582">Ta bort ordning</span><span class="sxs-lookup"><span data-stu-id="ced70-582">Remove the Order</span></span>
* <span data-ttu-id="ced70-583">Cmdleten `New-AzDataBoxEdgeShare` har ändrats</span><span class="sxs-lookup"><span data-stu-id="ced70-583">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="ced70-584">Nu skapas lokal filresurs</span><span class="sxs-lookup"><span data-stu-id="ced70-584">Now creates Local Share</span></span>
* <span data-ttu-id="ced70-585">Cmdleten `Set-AzDataBoxEdgeRole` har lagts till</span><span class="sxs-lookup"><span data-stu-id="ced70-585">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="ced70-586">Nu kan IotRole mappas till filresursen</span><span class="sxs-lookup"><span data-stu-id="ced70-586">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="ced70-587">Cmdleten `Invoke-AzDataBoxEdgeDevice` har lagts till</span><span class="sxs-lookup"><span data-stu-id="ced70-587">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="ced70-588">Anropa genomsökningsuppdatering, ladda ned uppdatering, installera uppdateringar på enheten</span><span class="sxs-lookup"><span data-stu-id="ced70-588">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="ced70-589">Cmdleten `Get-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="ced70-589">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="ced70-590">Hämtar information om utlösare</span><span class="sxs-lookup"><span data-stu-id="ced70-590">Gets the information about Triggers</span></span>
* <span data-ttu-id="ced70-591">Cmdleten `New-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="ced70-591">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="ced70-592">Skapa nya utlösare</span><span class="sxs-lookup"><span data-stu-id="ced70-592">Create new Triggers</span></span>
* <span data-ttu-id="ced70-593">Cmdleten `Remove-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="ced70-593">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="ced70-594">Ta bort utlösare</span><span class="sxs-lookup"><span data-stu-id="ced70-594">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ced70-595">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ced70-595">Az.DataFactory</span></span>
* <span data-ttu-id="ced70-596">Uppdatera ADF .Net SDK-versionen till 4.4.0</span><span class="sxs-lookup"><span data-stu-id="ced70-596">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="ced70-597">Lägg till parametern ExpressCustomSetup för kommandot Set-AzureRmDataFactoryV2IntegrationRuntime för att aktivera installationskonfigurationer och komponenter från tredje part utan anpassat konfigurationsskript.</span><span class="sxs-lookup"><span data-stu-id="ced70-597">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ced70-598">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ced70-598">Az.DataLakeStore</span></span>
* <span data-ttu-id="ced70-599">Uppdatera dokumentation för Get-AzDataLakeStoreDeletedItem och Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="ced70-599">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="ced70-600">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="ced70-600">Az.EventHub</span></span>
* <span data-ttu-id="ced70-601">Korrigering av problem #10301: Korrigera datumformat för SAS-token</span><span class="sxs-lookup"><span data-stu-id="ced70-601">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="ced70-602">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="ced70-602">Az.FrontDoor</span></span>
* <span data-ttu-id="ced70-603">Lägg till parametern MinimumTlsVersion till Enable-AzFrontDoorCustomDomainHttps och New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="ced70-603">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="ced70-604">Lägg till parametrarna HealthProbeMethod och EnabledState till New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="ced70-604">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="ced70-605">Lägg till en ny cmdlet för att skapa BackendPoolsSettings-objekt som passar i skapande/uppdatering av Front Door</span><span class="sxs-lookup"><span data-stu-id="ced70-605">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="ced70-606">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="ced70-606">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ced70-607">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ced70-607">Az.Network</span></span>
* <span data-ttu-id="ced70-608">Ändra alternativexemplen Start-AzVirtualNetworkGatewayConnectionPacketCapture.md och Start-AzVirtualnetworkGatewayPacketCapture.md för FilterData.</span><span class="sxs-lookup"><span data-stu-id="ced70-608">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="ced70-609">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="ced70-609">Az.PrivateDns</span></span>
* <span data-ttu-id="ced70-610">Uppdaterade PrivateDns .NET SDK till version 1.0.0</span><span class="sxs-lookup"><span data-stu-id="ced70-610">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ced70-611">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ced70-611">Az.RecoveryServices</span></span>
* <span data-ttu-id="ced70-612">Stöd för att välja disktyp vid aktivering av skydd i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="ced70-612">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="ced70-613">Korrigering av bugg för åtgärdsredigering av återställningsplan i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="ced70-613">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="ced70-614">Återställningsstöd för att godkänna filestream-databaser i Azure Backup SQL.</span><span class="sxs-lookup"><span data-stu-id="ced70-614">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="ced70-615">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="ced70-615">Az.RedisCache</span></span>
* <span data-ttu-id="ced70-616">Parametern MinimumTlsVersion har lagts till i cmdletarna New-AzRedisCache och Set-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="ced70-616">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="ced70-617">Dessutom har MinimumTlsVersion lagts till i utdata för cmdleten Get-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="ced70-617">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="ced70-618">Verifiering har lagts till på parametern -Size i cmdletarna Set-AzRedisCache och New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="ced70-618">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="ced70-619">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ced70-619">Az.Resources</span></span>
- <span data-ttu-id="ced70-620">Uppdaterade policy-cmdletar för att använda den nya API-versionen 2019-06-01 som har en ny EnforcementMode-egenskap i policytilldelningen.</span><span class="sxs-lookup"><span data-stu-id="ced70-620">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="ced70-621">Uppdaterade hjälpexempel för skapandet av policydefinition</span><span class="sxs-lookup"><span data-stu-id="ced70-621">Updated create policy definition help example</span></span>
- <span data-ttu-id="ced70-622">Åtgärda bugg i Remove-AZADServicePrincipal -ServicePrincipalName, utlös null-referens när tjänstens huvudnamn inte hittas.</span><span class="sxs-lookup"><span data-stu-id="ced70-622">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="ced70-623">Åtgärda bugg i New-AZADServicePrincipal, utlös null-referens när klientorganisationen inte har någon prenumeration.</span><span class="sxs-lookup"><span data-stu-id="ced70-623">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="ced70-624">Ändra New-AzAdServicePrincipal för att endast lägga till autentiseringsuppgifter för det associerade programmet.</span><span class="sxs-lookup"><span data-stu-id="ced70-624">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="ced70-625">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ced70-625">Az.Sql</span></span>
* <span data-ttu-id="ced70-626">Stöd har lagts till för databasen ReadReplicaCount.</span><span class="sxs-lookup"><span data-stu-id="ced70-626">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="ced70-627">Korrigerade Set-AzSqlDatabase när zonredundans inte har angetts</span><span class="sxs-lookup"><span data-stu-id="ced70-627">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="ced70-628">3.0.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="ced70-628">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="ced70-629">Allmänt</span><span class="sxs-lookup"><span data-stu-id="ced70-629">General</span></span>
* <span data-ttu-id="ced70-630">Az. PrivateDns 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="ced70-630">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="ced70-631">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ced70-631">Az.Accounts</span></span>
* <span data-ttu-id="ced70-632">Lägg till ett utfasningsmeddelande för aliaset Resolve-error.</span><span class="sxs-lookup"><span data-stu-id="ced70-632">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="ced70-633">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="ced70-633">Az.Advisor</span></span>
* <span data-ttu-id="ced70-634">Den nya kategorin Operational Excellence har lagts till i cmdleten Get-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="ced70-634">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="ced70-635">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="ced70-635">Az.Batch</span></span>
* <span data-ttu-id="ced70-636">`CoreQuota` på `BatchAccountContext` har bytt namn till `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="ced70-636">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="ced70-637">Det finns även en ny `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="ced70-637">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="ced70-638">Detta påverkar **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="ced70-638">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="ced70-639">**New-AzBatchTask** `-ResourceFile`-parametern tar nu en samling `PSResourceFile`-objekt som kan skapas med hjälp av den nya cmdleten **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="ced70-639">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="ced70-640">Ny **New-AzBatchResourceFile**-cmdlet för att skapa `PSResourceFile`-objekt.</span><span class="sxs-lookup"><span data-stu-id="ced70-640">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="ced70-641">Dessa kan tillhandahållas till **New-AzBatchTask** på `-ResourceFile`-parametern.</span><span class="sxs-lookup"><span data-stu-id="ced70-641">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="ced70-642">Detta stöder två nya typer av resursfiler förutom det befintliga sättet med `HttpUrl`:</span><span class="sxs-lookup"><span data-stu-id="ced70-642">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="ced70-643">`AutoStorageContainerName`-baserade resursfiler laddar ned en hel container för automatisk lagring till Batch-noden.</span><span class="sxs-lookup"><span data-stu-id="ced70-643">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="ced70-644">`StorageContainerUrl`-baserade resursfiler laddar ned containern som anges i webbadressen till Batch-noden.</span><span class="sxs-lookup"><span data-stu-id="ced70-644">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="ced70-645">Tog bort egenskapen `ApplicationPackages` för `PSApplication` som returnerades av **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="ced70-645">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="ced70-646">Specifika paket i ett program kan nu hämtas med hjälp av **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="ced70-646">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="ced70-647">Till exempel: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="ced70-647">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="ced70-648">Bytt namn på `ApplicationId` till `ApplicationName` på **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** och **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="ced70-648">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="ced70-649">`ApplicationId` är nu ett alias för `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="ced70-649">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="ced70-650">Ny `PSWindowsUserConfiguration`-egenskap till `PSUserAccount` lades till.</span><span class="sxs-lookup"><span data-stu-id="ced70-650">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="ced70-651">Bytte namn på `Version` till `Name` på `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="ced70-651">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="ced70-652">Bytte namn på `BlobSource` till `HttpUrl` på `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="ced70-652">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="ced70-653">Tog bort egenskapen `OSDisk` från `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="ced70-653">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="ced70-654">Tog bort **Set-AzBatchPoolOSVersion**.</span><span class="sxs-lookup"><span data-stu-id="ced70-654">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="ced70-655">Den här åtgärden stöds inte längre.</span><span class="sxs-lookup"><span data-stu-id="ced70-655">This operation is no longer supported.</span></span>
* <span data-ttu-id="ced70-656">`TargetOSVersion` har tagits bort från `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="ced70-656">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="ced70-657">Bytte namn på `CurrentOSVersion` till `OSVersion` på `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="ced70-657">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="ced70-658">`DataEgressGiB` och `DataIngressGiB` har tagits bort från `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="ced70-658">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="ced70-659">Tog bort **Get-AzBatchNodeAgentSku** och ersatte det med **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="ced70-659">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="ced70-660">**Get-AzBatchSupportedImage** returnerar samma data som **Get-AzBatchNodeAgentSku** men i ett mer användarvänligt format.</span><span class="sxs-lookup"><span data-stu-id="ced70-660">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="ced70-661">Nya icke-verifierade avbildningar returneras nu också.</span><span class="sxs-lookup"><span data-stu-id="ced70-661">New non-verified images are also now returned.</span></span> <span data-ttu-id="ced70-662">Ytterligare information om `Capabilities` och `BatchSupportEndOfLife` för varje avbildning inkluderas också.</span><span class="sxs-lookup"><span data-stu-id="ced70-662">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="ced70-663">Lade till möjlighet att montera fjärrfilsystem på varje nod i en pool via den nya parametern `MountConfiguration` för **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="ced70-663">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="ced70-664">Har nu stöd för nätverkssäkerhetsregler som blockerar nätverksåtkomst till en pool baserat på källportens trafik.</span><span class="sxs-lookup"><span data-stu-id="ced70-664">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="ced70-665">Detta görs via egenskapen `SourcePortRanges` på `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="ced70-665">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="ced70-666">När du kör en container stöder nu Batch körningen av uppgiften i arbetskatalogen för containern eller i arbetskatalogen för Batch-uppgiften.</span><span class="sxs-lookup"><span data-stu-id="ced70-666">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="ced70-667">Detta styrs av egenskapen `WorkingDirectory` på `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="ced70-667">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="ced70-668">Lade till en funktion för att ange en samling av offentliga IP-adresser på `PSNetworkConfiguration` via den nya egenskapen `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="ced70-668">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="ced70-669">Detta garanterar att noderna i poolen har en IP-adress från listan över IP-adresser som tillhandahållits av användare.</span><span class="sxs-lookup"><span data-stu-id="ced70-669">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="ced70-670">Om inget värde anges är standardvärdet för `WaitForSuccess` på `PSSTartTask` nu `$True` (var tidigare `$False`).</span><span class="sxs-lookup"><span data-stu-id="ced70-670">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="ced70-671">Om inget värde anges är standardvärdet för `Scope` på `PSAutoUserSpecification` nu `Pool` (var tidigare `Task` på Windows och `Pool` på Linux).</span><span class="sxs-lookup"><span data-stu-id="ced70-671">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="ced70-672">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="ced70-672">Az.Cdn</span></span>
* <span data-ttu-id="ced70-673">Introducerade UrlRewriteAction och CacheKeyQueryStringAction till RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="ced70-673">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="ced70-674">Åtgärdade flera buggar, som saknade indata för ”väljare” i cmdleten New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="ced70-674">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ced70-675">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ced70-675">Az.Compute</span></span>
* <span data-ttu-id="ced70-676">Funktion för diskkrypteringsuppsättning</span><span class="sxs-lookup"><span data-stu-id="ced70-676">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="ced70-677">Nya cmdletar:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="ced70-677">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="ced70-678">Parametern DiskEncryptionSetId har lagts till i följande cmdletar:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="ced70-678">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="ced70-679">Parametrarna DiskEncryptionSetId och EncryptionType har lagts till i följande cmdletar:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="ced70-679">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="ced70-680">Lägg till parametern PublicIPAddressVersion i New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="ced70-680">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="ced70-681">Flytta FileUris för anpassat skripttillägg från offentlig inställning till skyddad inställning</span><span class="sxs-lookup"><span data-stu-id="ced70-681">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="ced70-682">Lägg till ScaleInPolicy i cmdletarna New-AzVmss, New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ced70-682">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="ced70-683">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="ced70-683">Breaking changes</span></span>
    - <span data-ttu-id="ced70-684">Parametern UploadSizeInBytes används istället för DiskSizeGB för New-AzDiskConfig när CreateOption är Uppladdning</span><span class="sxs-lookup"><span data-stu-id="ced70-684">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="ced70-685">PublishingProfile.Source.ManagedImage.Id ersätts med StorageProfile.Source.Id i objektet GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="ced70-685">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ced70-686">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ced70-686">Az.DataFactory</span></span>
* <span data-ttu-id="ced70-687">Uppdatera ADF .Net SDK-versionen till 4.3.0</span><span class="sxs-lookup"><span data-stu-id="ced70-687">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ced70-688">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ced70-688">Az.DataLakeStore</span></span>
* <span data-ttu-id="ced70-689">Uppdatera ADLS SDK-version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) innehåller följande korrigeringar</span><span class="sxs-lookup"><span data-stu-id="ced70-689">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="ced70-690">Undvik att utlösa undantag när det inte går att deserialisera creationtime för inmatning av papperskorg eller katalog.</span><span class="sxs-lookup"><span data-stu-id="ced70-690">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="ced70-691">Gör inställning tillgänglig per tidsgräns för förfrågan i adlsclient</span><span class="sxs-lookup"><span data-stu-id="ced70-691">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="ced70-692">Korrigera överföringen av ursprunglig syncflag för badoffset-återställning</span><span class="sxs-lookup"><span data-stu-id="ced70-692">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="ced70-693">Korrigera EnumerateDirectory för att hämta fortsättningstoken när svar har kontrollerats</span><span class="sxs-lookup"><span data-stu-id="ced70-693">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="ced70-694">Korrigera bugg i Concat</span><span class="sxs-lookup"><span data-stu-id="ced70-694">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="ced70-695">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="ced70-695">Az.FrontDoor</span></span>
* <span data-ttu-id="ced70-696">Åtgärdade diverse stavfel i modul</span><span class="sxs-lookup"><span data-stu-id="ced70-696">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="ced70-697">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="ced70-697">Az.HDInsight</span></span>
* <span data-ttu-id="ced70-698">Korrigerade buggen att kunder får felet ”inte en giltig Base-64-sträng” vid användning av Get-AzHDInsightCluster för att hämta klustret med ADLSGen1-lagring.</span><span class="sxs-lookup"><span data-stu-id="ced70-698">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="ced70-699">Lägg till en parameter med namnet ”ApplicationId” i de tre cmdletarna Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig och New-AzHDInsightCluster så att kunden kan tillhandahålla tjänstens huvudnamn för program-ID för åtkomst till Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="ced70-699">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="ced70-700">Ändrade Microsoft.Azure.Management.HDInsight från 2.1.0 till 5.1.0</span><span class="sxs-lookup"><span data-stu-id="ced70-700">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="ced70-701">Fem cmdletar har tagits bort:</span><span class="sxs-lookup"><span data-stu-id="ced70-701">Removed five cmdlets:</span></span>
    - <span data-ttu-id="ced70-702">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="ced70-702">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="ced70-703">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="ced70-703">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="ced70-704">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="ced70-704">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="ced70-705">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="ced70-705">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="ced70-706">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="ced70-706">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="ced70-707">Tre cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="ced70-707">Added three cmdlets:</span></span>
    - <span data-ttu-id="ced70-708">Get-AzHDInsightMonitoring som ersätter Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="ced70-708">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="ced70-709">Enable-AzHDInsightMonitoring som ersätter Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="ced70-709">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="ced70-710">Disable-AzHDInsightMonitoring som ersätter Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="ced70-710">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="ced70-711">Korrigerade cmdleten Get-AzHDInsightProperties för att stödja hämtning av funktionsinformation från en viss plats.</span><span class="sxs-lookup"><span data-stu-id="ced70-711">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="ced70-712">Parameteruppsättningarna (Spark1 och Spark2) har tagits bort från Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="ced70-712">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="ced70-713">Lägg till exempel för cmdleten Add-AzHDInsightSecurityProfile till hjälpdokumenten.</span><span class="sxs-lookup"><span data-stu-id="ced70-713">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="ced70-714">Ändrade utdatatyp för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="ced70-714">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="ced70-715">Ändrade utdatatyp för Get-AzHDInsightProperties från CapabilitiesResponse till AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="ced70-715">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="ced70-716">Ändrade utdatatyp för Remove-AzHDInsightCluster från ClusterGetResponse till bool.</span><span class="sxs-lookup"><span data-stu-id="ced70-716">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="ced70-717">Ändrade utdatatyp för Set-AzHDInsightGatewaySettings HttpConnectivitySettings till GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="ced70-717">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="ced70-718">Lade till testfall för vissa scenarier.</span><span class="sxs-lookup"><span data-stu-id="ced70-718">Added some scenario test cases.</span></span>
* <span data-ttu-id="ced70-719">Ta bort vissa alias: Add-AzHDInsightConfigValues, Get-AzHDInsightProperties.</span><span class="sxs-lookup"><span data-stu-id="ced70-719">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ced70-720">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ced70-720">Az.IotHub</span></span>
* <span data-ttu-id="ced70-721">Icke-bakåtkompatibla ändringar:</span><span class="sxs-lookup"><span data-stu-id="ced70-721">Breaking changes:</span></span>
    - <span data-ttu-id="ced70-722">Cmdleten Add-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="ced70-722">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="ced70-723">Parameteruppsättningen __AllParameterSets för cmdleten Add-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="ced70-723">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="ced70-724">Cmdleten Get-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="ced70-724">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="ced70-725">Parameteruppsättningen __AllParameterSets för cmdleten Get-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="ced70-725">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="ced70-726">Egenskapen OperationsMonitoringProperties av typen Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="ced70-726">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="ced70-727">Egenskapen OperationsMonitoringProperties av typen Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="ced70-727">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="ced70-728">Cmdleten New-AzIotHubExportDevice stöder inte längre aliaset New-AzIotHubExportDevices.</span><span class="sxs-lookup"><span data-stu-id="ced70-728">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="ced70-729">Cmdleten New-AzIotHubImportDevice stöder inte längre aliaset New-AzIotHubImportDevices.</span><span class="sxs-lookup"><span data-stu-id="ced70-729">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="ced70-730">Cmdleten Remove-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="ced70-730">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="ced70-731">Parameteruppsättningen __AllParameterSets för cmdleten Remove-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="ced70-731">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="ced70-732">Cmdleten Set-AzIotHub har inte längre stöd för parametern OperationsMonitoringProperties och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="ced70-732">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="ced70-733">Parameteruppsättningen UpdateOperationsMonitoringProperties för cmdleten Set-AzIotHub har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="ced70-733">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ced70-734">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ced70-734">Az.RecoveryServices</span></span>
* <span data-ttu-id="ced70-735">Azure Site Recovery-stöd för att konfigurera nätverksresurser som NSG, offentliga IP-adresser och interna lastbalanserare för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="ced70-735">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="ced70-736">Azure Site Recovery-stöd för att skriva till hanterad disk för vMWare till Azure.</span><span class="sxs-lookup"><span data-stu-id="ced70-736">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="ced70-737">Azure Site Recovery-stöd för NIC-reduktion för vMWare till Azure.</span><span class="sxs-lookup"><span data-stu-id="ced70-737">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="ced70-738">Azure Site Recovery-stöd för accelererat nätverk för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="ced70-738">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="ced70-739">Azure Site Recovery-stöd för automatisk uppdatering av agent för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="ced70-739">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="ced70-740">Azure Site Recovery-stöd för Standard SSD för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="ced70-740">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="ced70-741">Azure Site Recovery-stöd för tvåstegskryptering i Azure Disk Encryption för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="ced70-741">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="ced70-742">Azure Site Recovery-stöd för att skydda nyligen tillagda diskar för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="ced70-742">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="ced70-743">En funktion för mjuk borttagning av virtuella datorer samt tester för mjuk borttagning har tagits bort</span><span class="sxs-lookup"><span data-stu-id="ced70-743">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="ced70-744">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ced70-744">Az.Resources</span></span>
* <span data-ttu-id="ced70-745">Uppdatera beroendesammansättning för Microsoft.Extensions.Caching.Memory från 1.1.1 till 2.2</span><span class="sxs-lookup"><span data-stu-id="ced70-745">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ced70-746">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ced70-746">Az.Network</span></span>
* <span data-ttu-id="ced70-747">Ändra alla cmdletar för PrivateEndpointConnection så att de stöder generiska tjänstleverantörer.</span><span class="sxs-lookup"><span data-stu-id="ced70-747">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="ced70-748">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="ced70-748">Updated cmdlet:</span></span>
        - <span data-ttu-id="ced70-749">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ced70-749">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="ced70-750">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ced70-750">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="ced70-751">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ced70-751">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="ced70-752">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ced70-752">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="ced70-753">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ced70-753">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="ced70-754">Lägg till ny cmdlet för PrivateLinkResource så att det också stöder generiska tjänstleverantörer.</span><span class="sxs-lookup"><span data-stu-id="ced70-754">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="ced70-755">Ny cmdlet:</span><span class="sxs-lookup"><span data-stu-id="ced70-755">New cmdlet:</span></span>
        - <span data-ttu-id="ced70-756">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="ced70-756">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="ced70-757">Lägg till nya fält och parametrar för funktionen Proxy Protocol V2.</span><span class="sxs-lookup"><span data-stu-id="ced70-757">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="ced70-758">Lägg till egenskapen EnableProxyProtocol i PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ced70-758">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="ced70-759">Lägg till egenskapen LinkIdentifier i PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ced70-759">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="ced70-760">Uppdaterade New-AzPrivateLinkService för att lägga till den nya valfria parametern EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="ced70-760">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="ced70-761">Korrigera felaktig beskrivning av parameter i referensdokumentationen för New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="ced70-761">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="ced70-762">Nya cmdletar som stöder Azure-brandväggsprincipen</span><span class="sxs-lookup"><span data-stu-id="ced70-762">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="ced70-763">Lägg till stöd för den underordnade resursen RouteTables för VirtualHub</span><span class="sxs-lookup"><span data-stu-id="ced70-763">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="ced70-764">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="ced70-764">New cmdlets added:</span></span>
        - <span data-ttu-id="ced70-765">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="ced70-765">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="ced70-766">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="ced70-766">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="ced70-767">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="ced70-767">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="ced70-768">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="ced70-768">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="ced70-769">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="ced70-769">Set-AzVirtualHub</span></span>
* <span data-ttu-id="ced70-770">Lägg till stöd för ny egenskaps-SKU för VirtualHub och VirtualWANType för VirtualWan</span><span class="sxs-lookup"><span data-stu-id="ced70-770">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="ced70-771">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="ced70-771">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="ced70-772">New-AzVirtualHub: lade till parameter-SKU</span><span class="sxs-lookup"><span data-stu-id="ced70-772">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="ced70-773">Update-AzVirtualHub: lade till parameter-SKU</span><span class="sxs-lookup"><span data-stu-id="ced70-773">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="ced70-774">New-AzVirtualWan: lade till parametern VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="ced70-774">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="ced70-775">Update-AzVirtualWan: lade till parametern VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="ced70-775">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="ced70-776">Lägg till stöd för egenskapen EnableInternetSecurity för HubVnetConnection, VpnConnection och ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="ced70-776">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="ced70-777">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="ced70-777">New cmdlets added:</span></span>
        - <span data-ttu-id="ced70-778">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="ced70-778">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="ced70-779">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="ced70-779">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="ced70-780">New-AzureRmVirtualHubVnetConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="ced70-780">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="ced70-781">New-AzureRmVpnConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="ced70-781">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="ced70-782">Update-AzureRmVpnConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="ced70-782">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="ced70-783">New-AzureRmExpressRouteConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="ced70-783">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="ced70-784">Set-AzureRmExpressRouteConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="ced70-784">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="ced70-785">Lägg till stöd för att konfigurera TopLevel WebApplicationFirewall-princip</span><span class="sxs-lookup"><span data-stu-id="ced70-785">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="ced70-786">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="ced70-786">New cmdlets added:</span></span>
        - <span data-ttu-id="ced70-787">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="ced70-787">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="ced70-788">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="ced70-788">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="ced70-789">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="ced70-789">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="ced70-790">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="ced70-790">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="ced70-791">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="ced70-791">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="ced70-792">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="ced70-792">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="ced70-793">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="ced70-793">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="ced70-794">New-AzApplicationGatewayFirewallPolicy: parametrarna PolicySetting, ManagedRule har lagts till</span><span class="sxs-lookup"><span data-stu-id="ced70-794">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="ced70-795">Stöd för operator för geomatchning har lagts till på CustomRule</span><span class="sxs-lookup"><span data-stu-id="ced70-795">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="ced70-796">Geomatchning har lagts till i operatorn på FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="ced70-796">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="ced70-797">Stöd har lagts till för brandväggsprinciperna perListener och perSite</span><span class="sxs-lookup"><span data-stu-id="ced70-797">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="ced70-798">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="ced70-798">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="ced70-799">New-AzApplicationGatewayHttpListener: parametrarna FirewallPolicy, FirewallPolicyId har lagts till</span><span class="sxs-lookup"><span data-stu-id="ced70-799">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="ced70-800">New-AzApplicationGatewayPathRuleConfig: parametrarna FirewallPolicy, FirewallPolicyId har lagts till</span><span class="sxs-lookup"><span data-stu-id="ced70-800">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="ced70-801">Åtgärdat så att nödvändigt undernät med namnet AzureBastionSubnet i PSBastion kan vara skiftlägesokänsligt</span><span class="sxs-lookup"><span data-stu-id="ced70-801">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="ced70-802">Stöd för mål-FQDN:er i nätverksregler och översatt FQDN i NAT-regler för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="ced70-802">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="ced70-803">Lägg till stöd för resursen RouteTables för IpGroup på den högsta nivån</span><span class="sxs-lookup"><span data-stu-id="ced70-803">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="ced70-804">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="ced70-804">New cmdlets added:</span></span>
        - <span data-ttu-id="ced70-805">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="ced70-805">New-AzIpGroup</span></span>
        - <span data-ttu-id="ced70-806">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="ced70-806">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="ced70-807">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="ced70-807">Get-AzIpGroup</span></span>
        - <span data-ttu-id="ced70-808">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="ced70-808">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ced70-809">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ced70-809">Az.ServiceFabric</span></span>
* <span data-ttu-id="ced70-810">Ta bort cmdleten Add-AzServiceFabricApplicationCertificate eftersom det här scenariot omfattas av Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="ced70-810">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="ced70-811">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ced70-811">Az.Sql</span></span>
* <span data-ttu-id="ced70-812">Stöd har lagts till för återställning av utelämnade databaser på hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="ced70-812">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="ced70-813">Inaktuella gamla cmdletar för granskning från kod.</span><span class="sxs-lookup"><span data-stu-id="ced70-813">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="ced70-814">Tog bort inaktuella alias:</span><span class="sxs-lookup"><span data-stu-id="ced70-814">Removed deprecated aliases:</span></span>
* <span data-ttu-id="ced70-815">Get-AzSqlDatabaseIndexRecommendations (använd Get-AzSqlDatabaseIndexRecommendation istället)</span><span class="sxs-lookup"><span data-stu-id="ced70-815">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="ced70-816">Get-AzSqlDatabaseRestorePoints (använd Get-AzSqlDatabaseRestorePoint istället)</span><span class="sxs-lookup"><span data-stu-id="ced70-816">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="ced70-817">Ta bort cmdleten Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="ced70-817">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="ced70-818">Ta bort alias för inaktuella cmdletar för inställningar för utvärdering av säkerhetsrisk</span><span class="sxs-lookup"><span data-stu-id="ced70-818">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="ced70-819">Inaktualisera cmdletar för inställningar för avancerad hotidentifiering</span><span class="sxs-lookup"><span data-stu-id="ced70-819">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="ced70-820">Lägga till cmdletar för att inaktivera och aktivera känslighetsrekommendationer på kolumner i en databas.</span><span class="sxs-lookup"><span data-stu-id="ced70-820">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ced70-821">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ced70-821">Az.Storage</span></span>
* <span data-ttu-id="ced70-822">Stöd för att aktivera stora filresurser vid skapande eller uppdatering av lagringskonto</span><span class="sxs-lookup"><span data-stu-id="ced70-822">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="ced70-823">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ced70-823">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="ced70-824">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ced70-824">Set-AzStorageAccount</span></span>
* <span data-ttu-id="ced70-825">När du stänger/hämtar en filreferens kan du hoppa över kontrollen av huruvida indatasökvägen är en filkatalog eller en fil för att undvika problem med objekt som har status DeletePending</span><span class="sxs-lookup"><span data-stu-id="ced70-825">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="ced70-826">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="ced70-826">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="ced70-827">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="ced70-827">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="ced70-828">2.8.0 – oktober 2019</span><span class="sxs-lookup"><span data-stu-id="ced70-828">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="ced70-829">Allmänt</span><span class="sxs-lookup"><span data-stu-id="ced70-829">General</span></span>
* <span data-ttu-id="ced70-830">AZ. HealthcareApis 1.0.0-version</span><span class="sxs-lookup"><span data-stu-id="ced70-830">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="ced70-831">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ced70-831">Az.Accounts</span></span>
* <span data-ttu-id="ced70-832">Uppdatera telemetri och URL-omskrivning för genererade moduler, korrigera Windows-enhetstester.</span><span class="sxs-lookup"><span data-stu-id="ced70-832">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="ced70-833">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ced70-833">Az.ApiManagement</span></span>
* <span data-ttu-id="ced70-834">**Set-AzApiManagementApi** – Tillagt stöd för att uppdatera Api till ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="ced70-834">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="ced70-835">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="ced70-835">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ced70-836">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ced70-836">Az.Automation</span></span>
* <span data-ttu-id="ced70-837">Åtgärdade cmdleten New-AzureAutomationSoftwareUpdateConfiguration för parametern för inställning av Linux-omstart.</span><span class="sxs-lookup"><span data-stu-id="ced70-837">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="ced70-838">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="ced70-838">Az.Batch</span></span>
* <span data-ttu-id="ced70-839">**Get-AzBatchNodeAgentSku** är inaktuell och ersätts av **Get-AzBatchSupportImage** i version 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="ced70-839">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ced70-840">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ced70-840">Az.Compute</span></span>
* <span data-ttu-id="ced70-841">Lägg till parametrarna Priority, EvictionPolicy och MaxPrice till cmdletarna New-AzVM och New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ced70-841">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="ced70-842">Korrigera varningsmeddelande och hjälpdokument för cmdletarna Add-AzVMAdditionalUnattendContent och Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="ced70-842">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="ced70-843">Åtgärda – skipVmBackup-undantag för virtuella Linux-datorer med hanterade diskar för Set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="ced70-843">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="ced70-844">Åtgärda fel i uppdatera krypteringsinställningarna i set-AzVMDiskEncryptionExtension, scenario i två steg.</span><span class="sxs-lookup"><span data-stu-id="ced70-844">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ced70-845">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ced70-845">Az.DataFactory</span></span>
* <span data-ttu-id="ced70-846">Lägga till CRUD-kommandon för ADF V2-dataflödet: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow och Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="ced70-846">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="ced70-847">Lägger till åtgärdskommandon för ADF V2-dataflödesfelsökningssession: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand och Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="ced70-847">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="ced70-848">Uppdatera ADF .Net SDK-versionen till 4.2.0</span><span class="sxs-lookup"><span data-stu-id="ced70-848">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ced70-849">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ced70-849">Az.DataLakeStore</span></span>
* <span data-ttu-id="ced70-850">Korrigera kontovalidering så att konton med ”-” kan skickas utan domän</span><span class="sxs-lookup"><span data-stu-id="ced70-850">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="ced70-851">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="ced70-851">Az.HealthcareApis</span></span>
* <span data-ttu-id="ced70-852">PowerShell-versionen har uppdaterats till 1.0.0</span><span class="sxs-lookup"><span data-stu-id="ced70-852">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="ced70-853">Uppdaterade SDK-versionen till 1.0.2</span><span class="sxs-lookup"><span data-stu-id="ced70-853">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="ced70-854">Uppdatera i tester för att referera till en ny SDK-version</span><span class="sxs-lookup"><span data-stu-id="ced70-854">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="ced70-855">Utdatastrukturen har uppdaterats från kapslad till förenklad.</span><span class="sxs-lookup"><span data-stu-id="ced70-855">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ced70-856">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ced70-856">Az.IotHub</span></span>
* <span data-ttu-id="ced70-857">Lägg till ny routningskälla: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="ced70-857">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="ced70-858">Mindre felkorrigering: Get-AzIothub returnerar inte subscriptionId</span><span class="sxs-lookup"><span data-stu-id="ced70-858">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ced70-859">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ced70-859">Az.Monitor</span></span>
* <span data-ttu-id="ced70-860">Nya åtgärdsgruppsmottagare har lagts till för åtgärdsgrupp   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="ced70-860">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="ced70-861">Använd vanligt aviseringsschema som är aktiverat för mottagarna.</span><span class="sxs-lookup"><span data-stu-id="ced70-861">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="ced70-862">Detta gäller inte för SMS, push för Azure-app, ITSM och röstmottagare</span><span class="sxs-lookup"><span data-stu-id="ced70-862">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="ced70-863">Webhooks har nu stöd för Azure Active Directory-autentisering.</span><span class="sxs-lookup"><span data-stu-id="ced70-863">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ced70-864">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ced70-864">Az.Network</span></span>
* <span data-ttu-id="ced70-865">Lägg till ny cmdlet Get-AzAvailableServiceAlias som kan anropas för att hämta de alias som kan användas för tjänstslutpunktsprinciper.</span><span class="sxs-lookup"><span data-stu-id="ced70-865">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="ced70-866">Stöd för tillägg av trafikväljare har lagts till i gatewayanslutningar för virtuella nätverk</span><span class="sxs-lookup"><span data-stu-id="ced70-866">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="ced70-867">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="ced70-867">New cmdlets added:</span></span>
        - <span data-ttu-id="ced70-868">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="ced70-868">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="ced70-869">Cmdletar har uppdaterats med valfri parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ced70-869">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="ced70-870">Lägg till stöd för ESP- och AH-protokoll i konfiguration av nätverkssäkerhetsregler</span><span class="sxs-lookup"><span data-stu-id="ced70-870">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="ced70-871">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="ced70-871">Updated cmdlets:</span></span>
        - <span data-ttu-id="ced70-872">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ced70-872">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="ced70-873">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ced70-873">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="ced70-874">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ced70-874">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="ced70-875">Förbättra hanteringen av undantag i Cortex-cmdletar</span><span class="sxs-lookup"><span data-stu-id="ced70-875">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="ced70-876">Nya generationer och SKU:er för VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="ced70-876">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="ced70-877">Introducera nya generationer för VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="ced70-877">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="ced70-878">Introducera nya SKU:er med högt dataflöde för VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="ced70-878">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="ced70-879">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="ced70-879">Az.RedisCache</span></span>
* <span data-ttu-id="ced70-880">Uppdaterad referensdokumentation för ”set-AzRedisCache” för att inkludera saknade värden för parametern ”size”</span><span class="sxs-lookup"><span data-stu-id="ced70-880">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="ced70-881">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ced70-881">Az.Sql</span></span>
* <span data-ttu-id="ced70-882">Lägg till stöd för inställningen Active Directory administratör på den hanterade instansen</span><span class="sxs-lookup"><span data-stu-id="ced70-882">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ced70-883">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ced70-883">Az.Storage</span></span>
* <span data-ttu-id="ced70-884">Uppdatera Lagringsklientbibliotek till 11.1.0</span><span class="sxs-lookup"><span data-stu-id="ced70-884">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="ced70-885">Lista containrar med hanteringsplans-API, kommer att listas med NextPageLink</span><span class="sxs-lookup"><span data-stu-id="ced70-885">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="ced70-886">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ced70-886">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="ced70-887">Lista lagringskonton från prenumerationen, kommer att listas med NextPageLink</span><span class="sxs-lookup"><span data-stu-id="ced70-887">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="ced70-888">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ced70-888">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="ced70-889">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="ced70-889">Az.StorageSync</span></span>
* <span data-ttu-id="ced70-890">Åtgärda problemet 9810 i Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="ced70-890">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ced70-891">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ced70-891">Az.Websites</span></span>
* <span data-ttu-id="ced70-892">Set-AzWebApp – uppdatering av ASP för en app misslyckades</span><span class="sxs-lookup"><span data-stu-id="ced70-892">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="ced70-893">2.7.0 – september 2019</span><span class="sxs-lookup"><span data-stu-id="ced70-893">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="ced70-894">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ced70-894">Az.ApiManagement</span></span>
* <span data-ttu-id="ced70-895">Uppdatera ”-Format”-parameterbeskrivningen i ”Set-AzApiManagementPolicy”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="ced70-895">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="ced70-896">Referenser för den föråldrade cmdleten ”Update-AzApiManagementDeployment” har tagits bort från referensdokumentationen.</span><span class="sxs-lookup"><span data-stu-id="ced70-896">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="ced70-897">Använd ”Set-AzApiManagement” i stället.</span><span class="sxs-lookup"><span data-stu-id="ced70-897">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ced70-898">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ced70-898">Az.Automation</span></span>
* <span data-ttu-id="ced70-899">Stavfel har korrigerats i exempel i referensdokumentationen för ”Register-AzAutomationDscNode”</span><span class="sxs-lookup"><span data-stu-id="ced70-899">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="ced70-900">Klargörande har lagts till om OS-begränsningar för Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="ced70-900">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="ced70-901">Null-referensundantag har korrigerats för -Wait-alternativet i Start-AzAutomationRunbook-cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ced70-901">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ced70-902">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ced70-902">Az.Compute</span></span>
* <span data-ttu-id="ced70-903">Lägg till UploadSizeInBytes-parameter till New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="ced70-903">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="ced70-904">Lägg till Incremental-parameter till New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="ced70-904">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="ced70-905">Lägg till en funktion för virtuella datorer med låg prioritet:</span><span class="sxs-lookup"><span data-stu-id="ced70-905">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="ced70-906">MaxPrice-, EvictionPolicy- och Priority-parametrar har lagts till i New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="ced70-906">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="ced70-907">MaxPrice-parametern har lagts till i New-AzVmssConfig-, Update-AzVM- och Update-AzVmss-cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="ced70-907">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="ced70-908">Åtgärda problem med VM-referenser för Get-AzAvailabilitySet-cmdleten när alla tillgänglighetsuppsättningar i prenumerationen visas.</span><span class="sxs-lookup"><span data-stu-id="ced70-908">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="ced70-909">Korrigera null-undantaget för Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="ced70-909">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="ced70-910">Korrigera VHD-metoden för sökning relativt till slut.</span><span class="sxs-lookup"><span data-stu-id="ced70-910">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="ced70-911">Åtgärda UltraSSD-problem för New-AzVM och Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="ced70-911">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ced70-912">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ced70-912">Az.DataFactory</span></span>
* <span data-ttu-id="ced70-913">Lägger till 3 nya kommandon för ADF V2 – Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription och Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="ced70-913">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="ced70-914">ADF .Net SDK har uppdaterats till 4.1.3</span><span class="sxs-lookup"><span data-stu-id="ced70-914">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="ced70-915">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="ced70-915">Az.HDInsight</span></span>
* <span data-ttu-id="ced70-916">Anrop för icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="ced70-916">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ced70-917">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ced70-917">Az.IotHub</span></span>
* <span data-ttu-id="ced70-918">Lägg till stöd för att anropa redundans för en IotHub till den geo-länkade katastrofåterställningsregionen.</span><span class="sxs-lookup"><span data-stu-id="ced70-918">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="ced70-919">Lägg till stöd för att hantera meddelandeberikning för en IotHub.</span><span class="sxs-lookup"><span data-stu-id="ced70-919">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="ced70-920">Nya cmdlet:ar är:</span><span class="sxs-lookup"><span data-stu-id="ced70-920">New cmdlets are:</span></span>
    - <span data-ttu-id="ced70-921">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="ced70-921">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="ced70-922">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="ced70-922">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="ced70-923">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="ced70-923">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="ced70-924">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="ced70-924">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ced70-925">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ced70-925">Az.Monitor</span></span>
* <span data-ttu-id="ced70-926">Pekar på den senaste Monitor SDK:n, dvs. 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="ced70-926">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="ced70-927">Lägger till bakåtkompatibla ändringar i Metrics-cmdletarna, dvs. enhetsuppräkningen stöder flera nya värden.</span><span class="sxs-lookup"><span data-stu-id="ced70-927">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="ced70-928">Detta är skrivskyddade cmdletar, så det förekommer inga ändringar i inmatningen för cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="ced70-928">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="ced70-929">API-versionen för **ActionGroups**-begäranden är nu **2019-06-01**. Tidigare var den **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="ced70-929">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="ced70-930">Test av scenarier har uppdaterats för att anpassas till den här ändringen.</span><span class="sxs-lookup"><span data-stu-id="ced70-930">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="ced70-931">Ett nytt obligatoriskt argument har lagts till för konstruktorerna för klasserna **EmailReceiver** och **WebhookReceiver** – ett booleskt värde med namnet **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="ced70-931">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="ced70-932">Värdet är för närvarande fast till **false** så att den här icke-bakåtkompatibla ändringen är dold från cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="ced70-932">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="ced70-933">**Obs!** Det här är en tillfällig ändring som måste verifieras av Alerts-teamet.</span><span class="sxs-lookup"><span data-stu-id="ced70-933">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="ced70-934">Ordningen på argumenten för konstruktorn för klassen **Source** (relaterad till klassen **ScheduledQueryRuleSource**) har ändrats från den tidigare SDK:n.</span><span class="sxs-lookup"><span data-stu-id="ced70-934">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="ced70-935">Den här ändringen krävde korrigering av två enhetstest: de kompilerades, men testerna skickades inte.</span><span class="sxs-lookup"><span data-stu-id="ced70-935">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="ced70-936">Ordningen på argumenten för konstruktorn för klassen **AlertingAction** (relaterad till klassen **ScheduledQueryRuleSource**) har ändrats från den tidigare SDK:n.</span><span class="sxs-lookup"><span data-stu-id="ced70-936">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="ced70-937">Den här ändringen krävde korrigering av två enhetstest: de kompilerades, men testerna skickades inte.</span><span class="sxs-lookup"><span data-stu-id="ced70-937">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="ced70-938">Stöd för kriterier för dynamiskt tröskelvärde för måttavisering v2</span><span class="sxs-lookup"><span data-stu-id="ced70-938">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="ced70-939">New-AzMetricAlertRuleV2Criteria: skapar nu även kriterier för dynamiskt tröskelvärde</span><span class="sxs-lookup"><span data-stu-id="ced70-939">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="ced70-940">Add-AzMetricAlertRuleV2: accepterar nu även kriterier för dynamiskt tröskelvärde</span><span class="sxs-lookup"><span data-stu-id="ced70-940">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="ced70-941">Förbättringar i schemalagd frågeregel (SQR)</span><span class="sxs-lookup"><span data-stu-id="ced70-941">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="ced70-942">Cmdletar accepterar ”Location”-parameter i båda formaten, antingen platsen (t.ex. eastus) eller platsens visningsnamn (t.ex. USA, östra)</span><span class="sxs-lookup"><span data-stu-id="ced70-942">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="ced70-943">”Enabled”-parametern illustreras korrekt i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="ced70-943">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="ced70-944">Exempel för den valfria parametern ”ActionGroup” har lagts till</span><span class="sxs-lookup"><span data-stu-id="ced70-944">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="ced70-945">Förbättrade hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="ced70-945">Overall improved help files</span></span>
* <span data-ttu-id="ced70-946">Åtgärda bugg då omfattningstypen fastställs för ”Set-AzActionRule”</span><span class="sxs-lookup"><span data-stu-id="ced70-946">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ced70-947">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ced70-947">Az.Network</span></span>
* <span data-ttu-id="ced70-948">Korrigera felaktigt exempel i referensdokumentationen för ”New-AzApplicationGateway”</span><span class="sxs-lookup"><span data-stu-id="ced70-948">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="ced70-949">Lägg till anmärkning i ”Get-AzNetworkWatcherPacketCapture”-referensdokumentationen om hämtning av alla egenskaper för en paketinsamling</span><span class="sxs-lookup"><span data-stu-id="ced70-949">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="ced70-950">Exempel har korrigerats i ”Test-AzNetworkWatcherIPFlow”-referensdokumentationen för korrekt uppräkning av nätverkskort</span><span class="sxs-lookup"><span data-stu-id="ced70-950">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="ced70-951">Förbättrad tolkning av molnundantag för att visa eventuell ytterligare information</span><span class="sxs-lookup"><span data-stu-id="ced70-951">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="ced70-952">Förbättrad tolkning av molnundantag för att hantera ytterligare en typ av SDK-undantag</span><span class="sxs-lookup"><span data-stu-id="ced70-952">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="ced70-953">Felaktig mappning av säkerhetsregelmodeller har korrigerats</span><span class="sxs-lookup"><span data-stu-id="ced70-953">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="ced70-954">Egenskaper har lagts till för nätverksgränssnittet för funktionen Privat IP</span><span class="sxs-lookup"><span data-stu-id="ced70-954">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="ced70-955">Egenskapen ”PrivateEndpoint” har lagts till som en typ av PSResourceId till PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="ced70-955">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="ced70-956">Egenskapen ”PrivateLinkConnectionProperties” har lagts till som en typ av PSIpConfigurationConnectivityInformation till PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ced70-956">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="ced70-957">Modellklassen PSIpConfigurationConnectivityInformation har lagts till</span><span class="sxs-lookup"><span data-stu-id="ced70-957">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="ced70-958">ApplicationRuleProtocolType ”mssql” har lagts till för Azure Firewall-resurs</span><span class="sxs-lookup"><span data-stu-id="ced70-958">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="ced70-959">MultiLink-stöd i virtuellt WAN</span><span class="sxs-lookup"><span data-stu-id="ced70-959">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="ced70-960">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="ced70-960">New cmdlets</span></span>
        - <span data-ttu-id="ced70-961">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="ced70-961">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="ced70-962">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="ced70-962">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="ced70-963">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="ced70-963">Updated cmdlet:</span></span>
        - <span data-ttu-id="ced70-964">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="ced70-964">New-VpnSite</span></span>
        - <span data-ttu-id="ced70-965">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="ced70-965">Update-VpnSite</span></span>
        - <span data-ttu-id="ced70-966">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="ced70-966">New-VpnConnection</span></span>
        - <span data-ttu-id="ced70-967">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="ced70-967">Update-VpnConnection</span></span>
* <span data-ttu-id="ced70-968">Dokument för vissa PowerShell-exempel har korrigerats så att Az-cmdletar används i stället för AzureRM-cmdletar</span><span class="sxs-lookup"><span data-stu-id="ced70-968">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ced70-969">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ced70-969">Az.RecoveryServices</span></span>
* <span data-ttu-id="ced70-970">Uppdatera AzureVMpolicy-objekt med ProtectedItemsCount-attribut</span><span class="sxs-lookup"><span data-stu-id="ced70-970">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="ced70-971">Ytterligare tester har lagts till för VM-princip och återställning av ursprungligt lagringskonto</span><span class="sxs-lookup"><span data-stu-id="ced70-971">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="ced70-972">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ced70-972">Az.Resources</span></span>
* <span data-ttu-id="ced70-973">Åtgärda fel där det inte gick att anropa New-AzRoleAssignment utan parametern Scope.</span><span class="sxs-lookup"><span data-stu-id="ced70-973">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ced70-974">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ced70-974">Az.ServiceFabric</span></span>
* <span data-ttu-id="ced70-975">Stavfel har korrigerats i exempel för ”Update-AzServiceFabricReliability”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="ced70-975">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="ced70-976">Lägger till nya cmdletar för att hantera program och tjänster:</span><span class="sxs-lookup"><span data-stu-id="ced70-976">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="ced70-977">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="ced70-977">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="ced70-978">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="ced70-978">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="ced70-979">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="ced70-979">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="ced70-980">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="ced70-980">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="ced70-981">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="ced70-981">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="ced70-982">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="ced70-982">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="ced70-983">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="ced70-983">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="ced70-984">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="ced70-984">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="ced70-985">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="ced70-985">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="ced70-986">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="ced70-986">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="ced70-987">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="ced70-987">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="ced70-988">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="ced70-988">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="ced70-989">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="ced70-989">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="ced70-990">Service Fabric SDK har uppgraderats till version 1.2.0 som använder Service Fabric-resursprovidern med API-version 2019-03-01.</span><span class="sxs-lookup"><span data-stu-id="ced70-990">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="ced70-991">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="ced70-991">Az.SignalR</span></span>
* <span data-ttu-id="ced70-992">Lägg till Update-, Restart-, CheckNameAvailability- och GetUsage-cmdletar</span><span class="sxs-lookup"><span data-stu-id="ced70-992">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="ced70-993">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ced70-993">Az.Sql</span></span>
* <span data-ttu-id="ced70-994">Uppdatera exempel i referensdokumentationen för ”Get-AzSqlElasticPool”</span><span class="sxs-lookup"><span data-stu-id="ced70-994">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="ced70-995">vCore-exempel för att skapa en elastisk pool (New-AzSqlElasticPool) har lagts till.</span><span class="sxs-lookup"><span data-stu-id="ced70-995">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="ced70-996">Ta bort verifieringen av EmailAddresses och kontrollen som bekräftar att EmailAdmins inte är falskt när EmailAddresses är tomt i Set-AzSqlServerAdvancedThreatProtectionPolicy och Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="ced70-996">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="ced70-997">Server-/databasgranskningsinställningar kan tas bort när det finns flera diagnostikinställningar som aktiverar granskningskategorin.</span><span class="sxs-lookup"><span data-stu-id="ced70-997">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="ced70-998">Åtgärda verifiering av e-postadresser i flera Sql Vulnerability Assessment-cmdletar (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting och Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="ced70-998">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ced70-999">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ced70-999">Az.Storage</span></span>
* <span data-ttu-id="ced70-1000">Exempel i referensdokumentationen för ”Get-AzStorageAccountKey” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="ced70-1000">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="ced70-1001">Vid upp- och nedladdning av en Azure-fil kan SMB-egenskaperna för källfilen (t.ex. filattribut, tidpunkten då filen skapades och tidpunkten för den senaste skrivningen) sparas i målfilen</span><span class="sxs-lookup"><span data-stu-id="ced70-1001">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="ced70-1002">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="ced70-1002">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="ced70-1003">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="ced70-1003">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="ced70-1004">Korrigera problem med uppladdningen av blockblob med egenskaper/metadata för ImmutabilityPolicy i containrar.</span><span class="sxs-lookup"><span data-stu-id="ced70-1004">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="ced70-1005">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ced70-1005">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="ced70-1006">Stöd för hantering av Azure-filresurser med API för hanteringsplan</span><span class="sxs-lookup"><span data-stu-id="ced70-1006">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="ced70-1007">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="ced70-1007">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="ced70-1008">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="ced70-1008">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="ced70-1009">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="ced70-1009">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="ced70-1010">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="ced70-1010">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ced70-1011">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ced70-1011">Az.Websites</span></span>
* <span data-ttu-id="ced70-1012">Åtgärdar problemet där webapp-taggar togs bort när appen migrerades till nya ASP</span><span class="sxs-lookup"><span data-stu-id="ced70-1012">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="ced70-1013">Åtgärda Publish-AzureWebapp så att det fungerar i Linux och Windows</span><span class="sxs-lookup"><span data-stu-id="ced70-1013">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="ced70-1014">Uppdatera exempel i ”Get-AzWebAppPublishingProfile”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="ced70-1014">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="ced70-1015">2.6.0 – augusti 2019</span><span class="sxs-lookup"><span data-stu-id="ced70-1015">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="ced70-1016">Allmänt</span><span class="sxs-lookup"><span data-stu-id="ced70-1016">General</span></span>
* <span data-ttu-id="ced70-1017">Åtgärdade diverse skrivfel i flera moduler</span><span class="sxs-lookup"><span data-stu-id="ced70-1017">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="ced70-1018">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ced70-1018">Az.Accounts</span></span>
* <span data-ttu-id="ced70-1019">Stöd för användartilldelat MSI i Azure Functions-autentisering (#9479)</span><span class="sxs-lookup"><span data-stu-id="ced70-1019">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="ced70-1020">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="ced70-1020">Az.Aks</span></span>
* <span data-ttu-id="ced70-1021">Åtgärda problem med utdata för "Get-AzAks"</span><span class="sxs-lookup"><span data-stu-id="ced70-1021">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="ced70-1022">Mer information här: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="ced70-1022">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="ced70-1023">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ced70-1023">Az.ApiManagement</span></span>
* <span data-ttu-id="ced70-1024">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="ced70-1024">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="ced70-1025">Uppdatera .net-NuGet-versionen, som inte tillämpar begränsningar för productId, apiId och userId</span><span class="sxs-lookup"><span data-stu-id="ced70-1025">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="ced70-1026">**Get-AzApiManagementProduct** – Lade till stöd för frågekörning mot produkter via API.</span><span class="sxs-lookup"><span data-stu-id="ced70-1026">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="ced70-1027">**New-AzApiManagementApiRevision** – Korrigering för problem där ApiRevisionDescription inte angavs vid skapande av ny API-revision https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="ced70-1027">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="ced70-1028">Åtgärdade skrivfel i modellen "PsApiManagementOAuth2AuthrozationServer" till "PsApiManagementOAuth2AuthorizationServer"</span><span class="sxs-lookup"><span data-stu-id="ced70-1028">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="ced70-1029">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="ced70-1029">Az.Batch</span></span>
* <span data-ttu-id="ced70-1030">Åtgärdade skrivfel i hjälpmeddelande och dokumentation till att skriva Windows med versaler</span><span class="sxs-lookup"><span data-stu-id="ced70-1030">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="ced70-1031">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="ced70-1031">Az.Cdn</span></span>
* <span data-ttu-id="ced70-1032">Åtgärdade skrivfel i CDN-modulens konverteringshjälp</span><span class="sxs-lookup"><span data-stu-id="ced70-1032">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ced70-1033">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ced70-1033">Az.Compute</span></span>
* <span data-ttu-id="ced70-1034">Lägg till VmssId i New-AzVMConfig-cmdleten</span><span class="sxs-lookup"><span data-stu-id="ced70-1034">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="ced70-1035">Lägg till parametrarna TerminateScheduledEvents och TerminateScheduledEventNotBeforeTimeoutInMinutes i New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ced70-1035">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="ced70-1036">Lägg till egenskapen HyperVGeneration till avbildningsobjekt för virtuell dator</span><span class="sxs-lookup"><span data-stu-id="ced70-1036">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="ced70-1037">Lägg till funktioner för Host och HostGroup</span><span class="sxs-lookup"><span data-stu-id="ced70-1037">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="ced70-1038">Nya cmdletar:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="ced70-1038">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="ced70-1039">HostId-parametern läggs till i New-AzVMConfig och New-AzVM</span><span class="sxs-lookup"><span data-stu-id="ced70-1039">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="ced70-1040">Uppdatera exempel i "Invoke-AzVMRunCommand"-dokumentationen till att använda rätt parameternamn</span><span class="sxs-lookup"><span data-stu-id="ced70-1040">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="ced70-1041">Uppdatera "-VolumeType"-beskrivningen i referensdokumentationen för "set-AzVMDiskEncryptionExtension" och "set-AzVmssDiskEncryptionExtension"</span><span class="sxs-lookup"><span data-stu-id="ced70-1041">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ced70-1042">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ced70-1042">Az.DataFactory</span></span>
* <span data-ttu-id="ced70-1043">Åtgärda skrivfel till att använda versaler för "Windows" i "New-AzDataFactoryEncryptValue"-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="ced70-1043">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="ced70-1044">Uppdaterade ADF .Net SDK-versionen till 4.1.2</span><span class="sxs-lookup"><span data-stu-id="ced70-1044">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="ced70-1045">Lägg till parametrarna "DataProxyIntegrationRuntimeName", "DataProxyStagingLinkedServiceName" och "DataProxyStagingPath" för "Set-AzureRmDataFactoryV2IntegrationRuntime"-cmd för att aktivera konfiguration av lokalt installerad integrationskörning som en proxy för SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="ced70-1045">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="ced70-1046">Uppdaterade PSTriggerRun till att visa utlöst pipeline, meddelande och egenskaper samt PSActivityRun till att visa aktivitetstypen</span><span class="sxs-lookup"><span data-stu-id="ced70-1046">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ced70-1047">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ced70-1047">Az.DataLakeStore</span></span>
* <span data-ttu-id="ced70-1048">Korrigering av frysning av Get-DataLakeStoreDeletedItem för fel eller fjärrundantag.</span><span class="sxs-lookup"><span data-stu-id="ced70-1048">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="ced70-1049">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="ced70-1049">Az.EventHub</span></span>
* <span data-ttu-id="ced70-1050">Korrigering av problem #9658 : Skrivfel i parametern VirtualNteworkRule i Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="ced70-1050">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="ced70-1051">Korrigering av problem #9558 : Set-AzEventHubNamespace använder PATCH i stället för PUT</span><span class="sxs-lookup"><span data-stu-id="ced70-1051">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="ced70-1052">lade till parametern EnableKafka i Set-AzEventHubNamespace-cmdleten</span><span class="sxs-lookup"><span data-stu-id="ced70-1052">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="ced70-1053">Korrigering av problem #9786 : kan inte skapa en regel med Endast lyssna-behörighet</span><span class="sxs-lookup"><span data-stu-id="ced70-1053">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="ced70-1054">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="ced70-1054">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="ced70-1055">Åtgärdade skrivfel i dokumentation där "Azure" skrevs helt med gemener</span><span class="sxs-lookup"><span data-stu-id="ced70-1055">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ced70-1056">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ced70-1056">Az.Monitor</span></span>
* <span data-ttu-id="ced70-1057">Åtgärdade felaktigt parameternamn i hjälpdokumentationen</span><span class="sxs-lookup"><span data-stu-id="ced70-1057">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ced70-1058">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ced70-1058">Az.Network</span></span>
* <span data-ttu-id="ced70-1059">Uppdaterade New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="ced70-1059">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="ced70-1060">Gjorde parametern "PublicIpAddress" inaktuell eftersom den aldrig används på serversidan.</span><span class="sxs-lookup"><span data-stu-id="ced70-1060">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="ced70-1061">Lade till den valfria parametern "Primary", som anger huruvida den aktuella IP-konfigurationen är den primära.</span><span class="sxs-lookup"><span data-stu-id="ced70-1061">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="ced70-1062">Förbättrade hanteringen av felundantag för begärande från SDK – åtgärdar problemet att tidigare SDK-undantag inte hanteras på rätt sätt, vilket leder till att viktig felinformation inte visas</span><span class="sxs-lookup"><span data-stu-id="ced70-1062">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="ced70-1063">Justerade valideringslogiken för IPv6-IP-prefix till att kontrollera korrekt IPv6-prefixlängd.</span><span class="sxs-lookup"><span data-stu-id="ced70-1063">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="ced70-1064">Uppdaterade Get-AzVirtualNetworkSubnetConfig: Lade till parameter som anges till get av undernätets resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="ced70-1064">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="ced70-1065">Uppdaterade beskrivningen av parametern Location för AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="ced70-1065">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ced70-1066">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ced70-1066">Az.OperationalInsights</span></span>
* <span data-ttu-id="ced70-1067">Uppdaterade dokumentation för "New-AzOperationalInsightsLinuxSyslogDataSource"</span><span class="sxs-lookup"><span data-stu-id="ced70-1067">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="ced70-1068">Lade till exempel</span><span class="sxs-lookup"><span data-stu-id="ced70-1068">Added example</span></span>
    - <span data-ttu-id="ced70-1069">Uppdaterade beskrivningen av parametern "-Name"</span><span class="sxs-lookup"><span data-stu-id="ced70-1069">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="ced70-1070">Lade till ett exempel för New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="ced70-1070">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="ced70-1071">Ändrade beskrivningen av parametern -Name för New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="ced70-1071">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ced70-1072">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ced70-1072">Az.RecoveryServices</span></span>
* <span data-ttu-id="ced70-1073">Uppdatera "Get-AzRecoveryServicesBackupJobDetail.md"</span><span class="sxs-lookup"><span data-stu-id="ced70-1073">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="ced70-1074">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ced70-1074">Az.Resources</span></span>
* <span data-ttu-id="ced70-1075">Lägg till stöd för den nya API-versionen från 2019-05-10 för Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="ced70-1075">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="ced70-1076">Lägg till stöd för "copy.count = 0" för variabler, resurser och egenskaper</span><span class="sxs-lookup"><span data-stu-id="ced70-1076">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="ced70-1077">Resurser med "condition = false" eller "copy.count = 0" tas bort i complete-läget</span><span class="sxs-lookup"><span data-stu-id="ced70-1077">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="ced70-1078">Lägg till ett exempel på tilldelning av princip på prenumerationsnivå i hjälpdokumentationen</span><span class="sxs-lookup"><span data-stu-id="ced70-1078">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="ced70-1079">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ced70-1079">Az.ServiceBus</span></span>
* <span data-ttu-id="ced70-1080">Korrigering av problem #9658 : Skrivfel i parametern VirtualNetworkRule i set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="ced70-1080">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="ced70-1081">Korrigering av problem #9786 : kan inte skapa en regel med Endast lyssna-behörighet</span><span class="sxs-lookup"><span data-stu-id="ced70-1081">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="ced70-1082">Lade till det nya kommandot "Test-AzServiceBusNameAvailability" för att kontrollera namntillgängligheten för kö och ämne</span><span class="sxs-lookup"><span data-stu-id="ced70-1082">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ced70-1083">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ced70-1083">Az.ServiceFabric</span></span>
* <span data-ttu-id="ced70-1084">Åtgärda buggar med tillägg av nodtyps-cmdlet:</span><span class="sxs-lookup"><span data-stu-id="ced70-1084">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="ced70-1085">NullReferenceException-bugg när resursgrupp hade annan vmss som inte är relaterad till Service Fabric-klustret.</span><span class="sxs-lookup"><span data-stu-id="ced70-1085">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="ced70-1086">Åtgärdar problemet: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="ced70-1086">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="ced70-1087">Åtgärda bugg där cmdleten misslyckades om virtualNetwork var i en annan resursgrupp än klustret.</span><span class="sxs-lookup"><span data-stu-id="ced70-1087">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="ced70-1088">Åtgärdar problemet: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="ced70-1088">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="ced70-1089">AzServiceFabricApplicationCertificate-cmdleten görs inaktuell</span><span class="sxs-lookup"><span data-stu-id="ced70-1089">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="ced70-1090">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ced70-1090">Az.Sql</span></span>
* <span data-ttu-id="ced70-1091">Uppdatera dokumentation om gamla gransknings-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="ced70-1091">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ced70-1092">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ced70-1092">Az.Storage</span></span>
* <span data-ttu-id="ced70-1093">Uppdatera hjälpen för Get/Close-AzStorageFileHandle genom att lägga till fler scenarier i cmdlet-exempel och uppdatera parameterbeskrivningar</span><span class="sxs-lookup"><span data-stu-id="ced70-1093">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="ced70-1094">Stöd för StandardBlobTier i uppladdningsblob och kopieringsblob</span><span class="sxs-lookup"><span data-stu-id="ced70-1094">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="ced70-1095">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ced70-1095">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="ced70-1096">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="ced70-1096">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="ced70-1097">Stöd för rehydratiseringsprioritet i kopieringsblob</span><span class="sxs-lookup"><span data-stu-id="ced70-1097">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="ced70-1098">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="ced70-1098">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ced70-1099">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ced70-1099">Az.Websites</span></span>
* <span data-ttu-id="ced70-1100">Lägg till klargöranden gällande parametern -AppSettings i Set-AzWebApp och Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ced70-1100">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="ced70-1101">2.5.0 – July 2019</span><span class="sxs-lookup"><span data-stu-id="ced70-1101">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ced70-1102">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ced70-1102">Az.Accounts</span></span>
* <span data-ttu-id="ced70-1103">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="ced70-1103">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="ced70-1104">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="ced70-1104">Az.ApplicationInsights</span></span>
* <span data-ttu-id="ced70-1105">Korrigera skrivfel i exempel i dokumentationen för Remove-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="ced70-1105">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ced70-1106">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ced70-1106">Az.Automation</span></span>
* <span data-ttu-id="ced70-1107">Korrigera skrivfel i resurssträng</span><span class="sxs-lookup"><span data-stu-id="ced70-1107">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="ced70-1108">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ced70-1108">Az.CognitiveServices</span></span>
* <span data-ttu-id="ced70-1109">Stöd för NetworkRuleSet har lagts till.</span><span class="sxs-lookup"><span data-stu-id="ced70-1109">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ced70-1110">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ced70-1110">Az.Compute</span></span>
* <span data-ttu-id="ced70-1111">Lägg till saknade egenskaper (ComputerName, OsName, OsVersion och HyperVGeneration) för visningsobjekt i den virtuella datorinstansen.</span><span class="sxs-lookup"><span data-stu-id="ced70-1111">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="ced70-1112">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ced70-1112">Az.ContainerRegistry</span></span>
* <span data-ttu-id="ced70-1113">Åtgärda skrivfel i Remove-AzContainerRegistryReplication för parametern Replication</span><span class="sxs-lookup"><span data-stu-id="ced70-1113">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="ced70-1114">Mer information finns här: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="ced70-1114">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ced70-1115">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ced70-1115">Az.DataFactory</span></span>
* <span data-ttu-id="ced70-1116">ADF .Net SDK-versionen har uppdaterats till 4.1.0</span><span class="sxs-lookup"><span data-stu-id="ced70-1116">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="ced70-1117">Korrigera skrivfel i dokumentationen för Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="ced70-1117">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="ced70-1118">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="ced70-1118">Az.EventHub</span></span>
* <span data-ttu-id="ced70-1119">Ny cmmdlet har lagts till för att skapa SAS-token: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="ced70-1119">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="ced70-1120">verifierings- och felmeddelande har lagts till för authorizationrules-rättigheter om endast "hantera" har tilldelats</span><span class="sxs-lookup"><span data-stu-id="ced70-1120">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ced70-1121">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ced70-1121">Az.KeyVault</span></span>
* <span data-ttu-id="ced70-1122">Stöd har lagts till för att ange KeySize för certifikatprinciper</span><span class="sxs-lookup"><span data-stu-id="ced70-1122">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="ced70-1123">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="ced70-1123">Az.LogicApp</span></span>
* <span data-ttu-id="ced70-1124">Korrigering för Get-AzIntegrationAccountMap för att lista alla mappningstyper</span><span class="sxs-lookup"><span data-stu-id="ced70-1124">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="ced70-1125">Ny MapType-parameter har lagts till för filtrering</span><span class="sxs-lookup"><span data-stu-id="ced70-1125">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="ced70-1126">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="ced70-1126">Az.ManagedServices</span></span>
* <span data-ttu-id="ced70-1127">Stöd för API-versionen 2019-06-01 (GA) har lagts till</span><span class="sxs-lookup"><span data-stu-id="ced70-1127">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ced70-1128">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ced70-1128">Az.Network</span></span>
* <span data-ttu-id="ced70-1129">Lägg till stöd för privat slutpunkt och privat länktjänst</span><span class="sxs-lookup"><span data-stu-id="ced70-1129">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="ced70-1130">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="ced70-1130">New cmdlets</span></span>
        - <span data-ttu-id="ced70-1131">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ced70-1131">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="ced70-1132">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ced70-1132">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="ced70-1133">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ced70-1133">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="ced70-1134">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ced70-1134">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="ced70-1135">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ced70-1135">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="ced70-1136">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ced70-1136">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="ced70-1137">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="ced70-1137">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="ced70-1138">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ced70-1138">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="ced70-1139">Nedanstående kommandon för funktionen har uppdaterats: Flaggan PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies på undernätet i VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ced70-1139">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="ced70-1140">Uppdaterade New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="ced70-1140">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="ced70-1141">Valfri parameter har lagts till – PrivateEndpointNetworkPoliciesFlag som konfigurerar huruvida nätverksprinciper ska tillämpas på en privat slutpunkt i det här undernätet.</span><span class="sxs-lookup"><span data-stu-id="ced70-1141">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="ced70-1142">Valfri parameter har lagts till – PrivateLinkServiceNetworkPoliciesFlag som konfigurerar huruvida nätverksprinciper ska tillämpas på en privat länktjänst i det här undernätet.</span><span class="sxs-lookup"><span data-stu-id="ced70-1142">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="ced70-1143">AzPrivateLinkService för cmdlet-parametern ServiceName har bytt namn till Name med aliaset ServiceName för bakåtkompatibilitet</span><span class="sxs-lookup"><span data-stu-id="ced70-1143">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="ced70-1144">Aktivera ICMP-protokoll för konfiguration av nätverkssäkerhetsregler</span><span class="sxs-lookup"><span data-stu-id="ced70-1144">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="ced70-1145">Uppdaterade cmdletar</span><span class="sxs-lookup"><span data-stu-id="ced70-1145">Updated cmdlets</span></span>
        - <span data-ttu-id="ced70-1146">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ced70-1146">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="ced70-1147">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ced70-1147">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="ced70-1148">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ced70-1148">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="ced70-1149">Lägg till ConnectionProtocolType (Ikev1/Ikev2) som en konfigurerbar parameter för New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ced70-1149">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="ced70-1150">Lägg till PrivateIpAddressVersion i LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="ced70-1150">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="ced70-1151">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="ced70-1151">Updated cmdlet:</span></span>
        - <span data-ttu-id="ced70-1152">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ced70-1152">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="ced70-1153">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ced70-1153">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="ced70-1154">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ced70-1154">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="ced70-1155">Uppdatering av Application Gateway-kommandot New-AzApplicationGatewayProbeConfig för stöd av anpassad port i Probe</span><span class="sxs-lookup"><span data-stu-id="ced70-1155">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="ced70-1156">Uppdaterade New-AzApplicationGatewayProbeConfig: Den valfria parametern Port som används för avsökning i serverdelen har lagts till.</span><span class="sxs-lookup"><span data-stu-id="ced70-1156">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="ced70-1157">Denna parameter gäller för SKU:erna Standard_V2 och WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="ced70-1157">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ced70-1158">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ced70-1158">Az.OperationalInsights</span></span>
* <span data-ttu-id="ced70-1159">Uppdaterade standardversionen för sparade sökningar till 1.</span><span class="sxs-lookup"><span data-stu-id="ced70-1159">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="ced70-1160">Åtgärdade hantering av anpassad log null regex</span><span class="sxs-lookup"><span data-stu-id="ced70-1160">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ced70-1161">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ced70-1161">Az.RecoveryServices</span></span>
* <span data-ttu-id="ced70-1162">Uppdatera Get-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="ced70-1162">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="ced70-1163">Uppdatera Get-AzRecoveryServicesBackupContainer.md</span><span class="sxs-lookup"><span data-stu-id="ced70-1163">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="ced70-1164">Uppdatera Get-AzRecoveryServicesVault.md</span><span class="sxs-lookup"><span data-stu-id="ced70-1164">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="ced70-1165">Uppdatera Wait-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="ced70-1165">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="ced70-1166">Uppdatera Set-AzRecoveryServicesVaultContext.md</span><span class="sxs-lookup"><span data-stu-id="ced70-1166">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="ced70-1167">Uppdatera Get-AzRecoveryServicesBackupItem.md</span><span class="sxs-lookup"><span data-stu-id="ced70-1167">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="ced70-1168">Uppdatera Get-AzRecoveryServicesBackupRecoveryPoint.md</span><span class="sxs-lookup"><span data-stu-id="ced70-1168">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="ced70-1169">Uppdatera Restore-AzRecoveryServicesBackupItem.md</span><span class="sxs-lookup"><span data-stu-id="ced70-1169">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="ced70-1170">Uppdaterat tjänstanrop för avregistrering av container för Azure-filresurs</span><span class="sxs-lookup"><span data-stu-id="ced70-1170">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="ced70-1171">Uppdatera Set-AzRecoveryServicesAsrAlertSetting.md</span><span class="sxs-lookup"><span data-stu-id="ced70-1171">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="ced70-1172">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ced70-1172">Az.Resources</span></span>
- <span data-ttu-id="ced70-1173">Ta bort den cmdlet som saknas och som refereras i dokumentationen till New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ced70-1173">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="ced70-1174">Princip-cmdletar har uppdaterats så att de använder den nya API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="ced70-1174">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="ced70-1175">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ced70-1175">Az.ServiceBus</span></span>
* <span data-ttu-id="ced70-1176">Ny cmmdlet har lagts till för att skapa SAS-token: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="ced70-1176">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="ced70-1177">verifierings- och felmeddelande har lagts till för authorizationrules-rättigheter om endast "hantera" har tilldelats</span><span class="sxs-lookup"><span data-stu-id="ced70-1177">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="ced70-1178">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ced70-1178">Az.Sql</span></span>
* <span data-ttu-id="ced70-1179">Åtgärda saknade exempel för Set-AzSqlDatabaseSecondary cmdlet</span><span class="sxs-lookup"><span data-stu-id="ced70-1179">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="ced70-1180">Åtgärda angivna återkommande genomsökningar för bedömning av säkerhetsrisk utan angivna e-postadresser</span><span class="sxs-lookup"><span data-stu-id="ced70-1180">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="ced70-1181">Korrigera ett skrivfel i ett varningsmeddelande.</span><span class="sxs-lookup"><span data-stu-id="ced70-1181">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ced70-1182">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ced70-1182">Az.Storage</span></span>
* <span data-ttu-id="ced70-1183">Uppdatera exempel i referensdokumentationen för Get-AzStorageAccount så att rätt parameternamn används</span><span class="sxs-lookup"><span data-stu-id="ced70-1183">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="ced70-1184">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="ced70-1184">Az.StorageSync</span></span>
* <span data-ttu-id="ced70-1185">Lägger till cmdleten Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="ced70-1185">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="ced70-1186">Åtgärda problem 9551 så att TierFilesOlderThanDays föredras</span><span class="sxs-lookup"><span data-stu-id="ced70-1186">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ced70-1187">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ced70-1187">Az.Websites</span></span>
* <span data-ttu-id="ced70-1188">Åtgärdar ett fel där vissa SiteConfig-egenskaper inte returnerades av Get-AzWebApp och Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ced70-1188">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="ced70-1189">Lägger till en ny platsparameter för Get-AzDeletedWebApp och Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="ced70-1189">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="ced70-1190">Åtgärdar ett fel i kloning av webbapp-platser som använder New-AzWebApp-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="ced70-1190">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="ced70-1191">2.4.0 – juli 2019</span><span class="sxs-lookup"><span data-stu-id="ced70-1191">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ced70-1192">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ced70-1192">Az.Accounts</span></span>
* <span data-ttu-id="ced70-1193">Lägg till stöd för profil-cmdletar</span><span class="sxs-lookup"><span data-stu-id="ced70-1193">Add support for profile cmdlets</span></span>
* <span data-ttu-id="ced70-1194">Lägg till stöd för miljöer och dataplaner i genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="ced70-1194">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="ced70-1195">Åtgärda bugg där fel slutpunkt i vissa fall användes för cmdletar för dataplaner i Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="ced70-1195">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="ced70-1196">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="ced70-1196">Az.Advisor</span></span>
* <span data-ttu-id="ced70-1197">GA-version av Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="ced70-1197">GA release of Az.Advisor</span></span>
* <span data-ttu-id="ced70-1198">Den här modulen ingår nu som en del av `Az`-sammanslagningsmodulen</span><span class="sxs-lookup"><span data-stu-id="ced70-1198">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="ced70-1199">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ced70-1199">Az.ApiManagement</span></span>
* <span data-ttu-id="ced70-1200">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="ced70-1200">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="ced70-1201">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="ced70-1201">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="ced70-1202">Stöd för att fråga prenumerationer efter användare och produkt har lagts till</span><span class="sxs-lookup"><span data-stu-id="ced70-1202">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="ced70-1203">Stöd för att fråga med hjälp av omfång ”/”, ”/apis”, ”/apis/echo-api” har lagts till</span><span class="sxs-lookup"><span data-stu-id="ced70-1203">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="ced70-1204">Korrigering av problem https://github.com/Azure/azure-powershell/issues/9307 och https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="ced70-1204">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="ced70-1205">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="ced70-1205">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="ced70-1206">Stöd för att ange ”ApiVersion” och ”ApiVersionSetId” när API:er importeras har lagts till</span><span class="sxs-lookup"><span data-stu-id="ced70-1206">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ced70-1207">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ced70-1207">Az.Automation</span></span>
* <span data-ttu-id="ced70-1208">Bugg med cmdleten Set-AzAutomationConnectionFieldValue för att hantera strängvärde har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="ced70-1208">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ced70-1209">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ced70-1209">Az.Compute</span></span>
* <span data-ttu-id="ced70-1210">Lägg till parametern HyperVGeneration i New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="ced70-1210">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ced70-1211">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ced70-1211">Az.DataFactory</span></span>
* <span data-ttu-id="ced70-1212">Uppdaterar utdata från ADF-cmdletar som hämtar aktivitetskörningar, hämtar pipelinekörningar och hämtar utlösarkörningar för stöd för Select-Object-pipe.</span><span class="sxs-lookup"><span data-stu-id="ced70-1212">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="ced70-1213">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="ced70-1213">Az.EventGrid</span></span>
* <span data-ttu-id="ced70-1214">Korrigera stavfel i dokumentation om ”New-AzEventGridSubscription”</span><span class="sxs-lookup"><span data-stu-id="ced70-1214">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ced70-1215">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ced70-1215">Az.IotHub</span></span>
* <span data-ttu-id="ced70-1216">Lägg till stöd för att återskapa principnycklar för auktorisering.</span><span class="sxs-lookup"><span data-stu-id="ced70-1216">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ced70-1217">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ced70-1217">Az.Network</span></span>
* <span data-ttu-id="ced70-1218">”RoutingPreference” har lagts till i offentliga IP-taggar</span><span class="sxs-lookup"><span data-stu-id="ced70-1218">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="ced70-1219">Förbättra exempel för referensdokumentation om ”Get-AzNetworkServiceTag”</span><span class="sxs-lookup"><span data-stu-id="ced70-1219">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="ced70-1220">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ced70-1220">Az.PolicyInsights</span></span>
* <span data-ttu-id="ced70-1221">Åtgärda problem med null-referens i Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="ced70-1221">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="ced70-1222">Mer information här: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="ced70-1222">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ced70-1223">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ced70-1223">Az.OperationalInsights</span></span>
* <span data-ttu-id="ced70-1224">Modellen för CustomLog-datakälla som returneras i Get-AzOperationalInsightsDataSource har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="ced70-1224">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ced70-1225">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ced70-1225">Az.RecoveryServices</span></span>
* <span data-ttu-id="ced70-1226">Kommandot get-policy för IaaSVM:er har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="ced70-1226">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="ced70-1227">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ced70-1227">Az.Resources</span></span>
    - <span data-ttu-id="ced70-1228">Korrigera hjälptext för den översta parametern i Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="ced70-1228">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="ced70-1229">Lägg till växlingsstöd på klientsidan för Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="ced70-1229">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="ced70-1230">Lägg till nya parametrar för Set-AzPolicyAssignment, -PolicyParameters och -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="ced70-1230">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="ced70-1231">En mängd dokument- och exempeluppdateringar för Policy-cmdletar</span><span class="sxs-lookup"><span data-stu-id="ced70-1231">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="ced70-1232">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ced70-1232">Az.ServiceBus</span></span>
* <span data-ttu-id="ced70-1233">Korrigering av problem #4938 – New-AzureRmServiceBusQueue returnerar BadRequest vid konfiguration av MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="ced70-1233">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="ced70-1234">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ced70-1234">Az.Sql</span></span>
* <span data-ttu-id="ced70-1235">Lägg till cmdletar för instansredundansgrupper från förhandsversion till offentlig version</span><span class="sxs-lookup"><span data-stu-id="ced70-1235">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="ced70-1236">Stöd för granskning för Azure SQL Server\Database med nya cmdletar.</span><span class="sxs-lookup"><span data-stu-id="ced70-1236">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="ced70-1237">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="ced70-1237">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="ced70-1238">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="ced70-1238">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="ced70-1239">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="ced70-1239">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="ced70-1240">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="ced70-1240">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="ced70-1241">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="ced70-1241">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="ced70-1242">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="ced70-1242">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="ced70-1243">Ta bort begränsningar för e-post från inställningarna för sårbarhetsbedömning</span><span class="sxs-lookup"><span data-stu-id="ced70-1243">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ced70-1244">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ced70-1244">Az.Storage</span></span>
* <span data-ttu-id="ced70-1245">Ändra två parametrar ”-IndexDocument” och ”-ErrorDocument404Path” från ”krävs” till ”valfri” i cmdlet:</span><span class="sxs-lookup"><span data-stu-id="ced70-1245">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="ced70-1246">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="ced70-1246">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="ced70-1247">Uppdatera hjälpen för Get-AzStorageBlobContent genom att lägga till ett exempel</span><span class="sxs-lookup"><span data-stu-id="ced70-1247">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="ced70-1248">Visa mer felinformation när cmdleten misslyckas med StorageException</span><span class="sxs-lookup"><span data-stu-id="ced70-1248">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="ced70-1249">Stöd för att skapa eller uppdatera lagringskonto med Azure Files AAD DS-autentisering</span><span class="sxs-lookup"><span data-stu-id="ced70-1249">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="ced70-1250">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ced70-1250">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="ced70-1251">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ced70-1251">Set-AzStorageAccount</span></span>
* <span data-ttu-id="ced70-1252">Stöd för att lista eller stänga filreferenser för en filresurs, filkatalog eller en fil</span><span class="sxs-lookup"><span data-stu-id="ced70-1252">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="ced70-1253">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="ced70-1253">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="ced70-1254">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="ced70-1254">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="ced70-1255">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="ced70-1255">Az.StorageSync</span></span>
* <span data-ttu-id="ced70-1256">Den här modulen ingår nu som en del av `Az`-sammanslagningsmodulen</span><span class="sxs-lookup"><span data-stu-id="ced70-1256">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="ced70-1257">2.3.2 – juni 2019</span><span class="sxs-lookup"><span data-stu-id="ced70-1257">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ced70-1258">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ced70-1258">Az.Accounts</span></span>
* <span data-ttu-id="ced70-1259">Åtgärda bugg med felaktiga webbadresser som i vissa fall användes för Functions-anrop</span><span class="sxs-lookup"><span data-stu-id="ced70-1259">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="ced70-1260">Mer information här: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="ced70-1260">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="ced70-1261">Åtgärda problem med alias från AzureRM i Az-cmdletar</span><span class="sxs-lookup"><span data-stu-id="ced70-1261">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="ced70-1262">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="ced70-1262">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="ced70-1263">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="ced70-1263">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ced70-1264">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ced70-1264">Az.Compute</span></span>
* <span data-ttu-id="ced70-1265">Parameteruppsättningarna New-AzVm och New-AzVmss accepterar nu parametern ”ProximityPlacementGroup”.</span><span class="sxs-lookup"><span data-stu-id="ced70-1265">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="ced70-1266">Stavfel i referensdokumentationen för ”New-AzVM” har korrigerats</span><span class="sxs-lookup"><span data-stu-id="ced70-1266">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="ced70-1267">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="ced70-1267">Az.Dns</span></span>
* <span data-ttu-id="ced70-1268">Stavfel i hjälpexempel för ”Set-AzDnsZone” har korrigerats.</span><span class="sxs-lookup"><span data-stu-id="ced70-1268">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="ced70-1269">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="ced70-1269">Az.EventGrid</span></span>
* <span data-ttu-id="ced70-1270">Har uppdaterats för att använda API-versionen 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="ced70-1270">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="ced70-1271">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="ced70-1271">New cmdlets:</span></span>
    - <span data-ttu-id="ced70-1272">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="ced70-1272">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="ced70-1273">Skapar en ny Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="ced70-1273">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="ced70-1274">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="ced70-1274">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="ced70-1275">Hämtar information om en Event Grid-domän eller hämtar en lista med alla Event Grid-domäner i den aktuella Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="ced70-1275">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="ced70-1276">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="ced70-1276">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="ced70-1277">Tar bort en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="ced70-1277">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="ced70-1278">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="ced70-1278">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="ced70-1279">Återskapar nyckeln för delad åtkomst för en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="ced70-1279">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="ced70-1280">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="ced70-1280">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="ced70-1281">Hämtar de nycklar för delad åtkomst som används för att publicera händelser till en Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="ced70-1281">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="ced70-1282">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="ced70-1282">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="ced70-1283">Skapar ett nytt Azure Event Grid-domänämne.</span><span class="sxs-lookup"><span data-stu-id="ced70-1283">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="ced70-1284">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="ced70-1284">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="ced70-1285">Hämtar information om ett Event Grid-domänämne eller hämtar en lista med alla Event Grid-domänämnen under en specifik Event Grid-domän i nuvarande Azure</span><span class="sxs-lookup"><span data-stu-id="ced70-1285">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="ced70-1286">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="ced70-1286">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="ced70-1287">Tar bort ett befintligt Azure Event Grid-domänämne.</span><span class="sxs-lookup"><span data-stu-id="ced70-1287">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="ced70-1288">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="ced70-1288">Updated cmdlets:</span></span>
    - <span data-ttu-id="ced70-1289">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="ced70-1289">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="ced70-1290">Lägg till nya obligatoriska parametrar för att stödja piping för den nya Event Grid-domänen och Event Grid-domänämnet för att göra det möjligt att skapa nya händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="ced70-1290">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="ced70-1291">Lägg till nya obligatoriska parametrar för att ange det nya Event Grid-domännamnet och/eller namnet på Event Grid-domänämnet för att göra det möjligt att skapa nya händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="ced70-1291">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="ced70-1292">Lägg till ny parameteruppsättningar för domäner och domänämnen för att göra det möjligt att återanvända befintliga parametrar (t.ex. EndPointType, SubjectBeginsWith osv).</span><span class="sxs-lookup"><span data-stu-id="ced70-1292">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="ced70-1293">Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="ced70-1293">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="ced70-1294">Förfallodatum för händelseprenumeration</span><span class="sxs-lookup"><span data-stu-id="ced70-1294">Event subscription expiration date,</span></span>
            - <span data-ttu-id="ced70-1295">Avancerade filterparametrar.</span><span class="sxs-lookup"><span data-stu-id="ced70-1295">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="ced70-1296">Lägg till ny uppräkning för servicebusqueue som mål.</span><span class="sxs-lookup"><span data-stu-id="ced70-1296">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="ced70-1297">Tillåt inte användning av ”Alla” i alternativet -IncludedEventType och ersätt det med</span><span class="sxs-lookup"><span data-stu-id="ced70-1297">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="ced70-1298">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="ced70-1298">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="ced70-1299">Lägg till ny valfria parametrar (Top, ODataQuery och NextLink) för att stödja sidnumrering och filtrering av resultat.</span><span class="sxs-lookup"><span data-stu-id="ced70-1299">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="ced70-1300">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="ced70-1300">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="ced70-1301">Lägg till nya obligatoriska parametrar för att stödja piping för en Event Grid-domän och Event Grid-domänämnen för att göra det möjligt att ta bort befintliga händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="ced70-1301">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="ced70-1302">Lägg till nya obligatoriska parametrar för att ange Event Grid-domännamnet och/eller namnet på Event Grid-domänämnet för att göra det möjligt att ta bort befintliga händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="ced70-1302">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="ced70-1303">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="ced70-1303">Az.FrontDoor</span></span>
* <span data-ttu-id="ced70-1304">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="ced70-1304">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="ced70-1305">Lägg till stöd för transformeringar och nytt värde för automatisk komplettering för operatorer (RegEx)</span><span class="sxs-lookup"><span data-stu-id="ced70-1305">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="ced70-1306">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="ced70-1306">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="ced70-1307">Lägg till nya värden för automatisk komplettering</span><span class="sxs-lookup"><span data-stu-id="ced70-1307">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ced70-1308">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ced70-1308">Az.Network</span></span>
* <span data-ttu-id="ced70-1309">Lägg till stöd för resurs för virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="ced70-1309">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="ced70-1310">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="ced70-1310">New cmdlets</span></span>
        - <span data-ttu-id="ced70-1311">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="ced70-1311">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="ced70-1312">Lägg till AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="ced70-1312">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="ced70-1313">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="ced70-1313">New cmdlets</span></span>
        - <span data-ttu-id="ced70-1314">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="ced70-1314">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="ced70-1315">Lägg till PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ced70-1315">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="ced70-1316">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="ced70-1316">New cmdlets</span></span>
        - <span data-ttu-id="ced70-1317">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ced70-1317">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="ced70-1318">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ced70-1318">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="ced70-1319">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ced70-1319">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="ced70-1320">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="ced70-1320">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="ced70-1321">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ced70-1321">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="ced70-1322">Lägg till PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ced70-1322">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="ced70-1323">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="ced70-1323">New cmdlets</span></span>
        - <span data-ttu-id="ced70-1324">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ced70-1324">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="ced70-1325">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ced70-1325">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="ced70-1326">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ced70-1326">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="ced70-1327">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="ced70-1327">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="ced70-1328">Nedanstående kommandon för funktionen har uppdaterats: Flaggan UseLocalAzureIpAddress på VpnConnection</span><span class="sxs-lookup"><span data-stu-id="ced70-1328">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="ced70-1329">New-AzVpnConnection har uppdaterats: Den valfria parametern -UseLocalAzureIpAddress har lagts till för att visa att en lokal IP-adress i Azure ska användas som källadress när anslutningen initieras.</span><span class="sxs-lookup"><span data-stu-id="ced70-1329">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="ced70-1330">Set-AzVpnConnection har uppdaterats: Den valfria parametern -UseLocalAzureIpAddress har lagts till för att visa att en lokal IP-adress i Azure ska användas som källadress när anslutningen initieras.</span><span class="sxs-lookup"><span data-stu-id="ced70-1330">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="ced70-1331">Det skrivskyddade fältet PeeredConnections har lagts till i ExpressRoute-peering.</span><span class="sxs-lookup"><span data-stu-id="ced70-1331">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="ced70-1332">Det skrivskyddade fältet GlobalReachEnabled har lagts till i ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="ced70-1332">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="ced70-1333">Ett attribut för icke-bakåtkompatibla ändringar har lagts till för att lyfta fram utfasning av fältet AllowGlobalReach i modellen ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ced70-1333">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="ced70-1334">Problem 8756 har åtgärdats: Fel vid användning av TargetListenerID med AzApplicationGatewayRedirectConfiguration-cmdletar</span><span class="sxs-lookup"><span data-stu-id="ced70-1334">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="ced70-1335">En bugg i New-AzApplicationGatewayPathRuleConfig som gjorde att regeluppsättningen för att återskapa inte kunde anges har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="ced70-1335">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="ced70-1336">Visningen av VirtualNetworkTaps i NetworkInterfaceIpConfiguration har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="ced70-1336">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="ced70-1337">Cortex Get-cmdletar för att visa en lista med alla delar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="ced70-1337">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="ced70-1338">Funktionen för att skapa VirtualHub-referenser för ExpressRouteGateways och VpnGateway har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="ced70-1338">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="ced70-1339">Stöd för tillgänglighetszoner i AzureFirewall och NatGateway har lagts till</span><span class="sxs-lookup"><span data-stu-id="ced70-1339">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="ced70-1340">Cmdleten Get-AzNetworkServiceTag har lagts till</span><span class="sxs-lookup"><span data-stu-id="ced70-1340">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="ced70-1341">Lägg till stöd för flera offentliga IP-adresser för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="ced70-1341">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="ced70-1342">Cmdleten New-AzFirewall har uppdaterats:</span><span class="sxs-lookup"><span data-stu-id="ced70-1342">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="ced70-1343">Parametern -PublicIpAddress som accepterar ett eller flera offentliga IP-adressobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="ced70-1343">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="ced70-1344">Parametern -VirtualNetwork som accepterar ett virtuellt nätverksobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="ced70-1344">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="ced70-1345">Metoderna AddPublicIpAddress och RemovePublicIpAddress har lagts till på brandväggsobjekt – dessa accepterar ett offentligt IP-adressobjekt som indata</span><span class="sxs-lookup"><span data-stu-id="ced70-1345">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="ced70-1346">Inaktuella parametrar -PublicIpName och -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="ced70-1346">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="ced70-1347">Nedanstående kommandon för funktionen har uppdaterats: Ange autentiseringsalternativ för VpnClient AAD till resurser för virtuella nätverksgatewayer.</span><span class="sxs-lookup"><span data-stu-id="ced70-1347">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="ced70-1348">New-AzVirtualNetworkGateway har uppdaterats: De valfria parametrarna AadTenantUri, AadAudienceId och AadIssuerUri för att ange VpnClient AAD-autentiseringsalternativ på en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="ced70-1348">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="ced70-1349">Set-AzVirtualNetworkGateway har uppdaterats: De valfria parametrarna AadTenantUri, AadAudienceId och AadIssuerUri för att ange VpnClient AAD-autentiseringsalternativ på en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="ced70-1349">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="ced70-1350">Set-AzVirtualNetworkGateway har uppdaterats: Den valfria växelparametern RemoveAadAuthentication som tar bort VpnClient AAD-autentiseringsalternativ från en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="ced70-1350">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ced70-1351">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ced70-1351">Az.OperationalInsights</span></span>
* <span data-ttu-id="ced70-1352">Aktivera prisnivån **pergb2018** i kommandot ”New-AzureRmOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="ced70-1352">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="ced70-1353">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ced70-1353">Az.Resources</span></span>
* <span data-ttu-id="ced70-1354">Stöd för ytterligare alternativ för att exportera en mall</span><span class="sxs-lookup"><span data-stu-id="ced70-1354">Support for additional Template Export options</span></span>
    - <span data-ttu-id="ced70-1355">Lägg till parametern ”-SkipResourceNameParameterization” till Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ced70-1355">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="ced70-1356">Lägg till parametern ”-SkipAllParameterization” till Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ced70-1356">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="ced70-1357">Lägg till parametern ”-Resource” till Export-AzResourceGroup för exporterad resursfiltrering</span><span class="sxs-lookup"><span data-stu-id="ced70-1357">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ced70-1358">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ced70-1358">Az.ServiceFabric</span></span>
* <span data-ttu-id="ced70-1359">Åtgärda att fel tumavtryck används vid tilläggning av certifikat i ByExistingKeyVault i vissa fall</span><span class="sxs-lookup"><span data-stu-id="ced70-1359">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="ced70-1360">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ced70-1360">Az.Sql</span></span>
* <span data-ttu-id="ced70-1361">Åtgärda suffix för lagringsslutpunkt i Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="ced70-1361">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="ced70-1362">Åtgärda att aktivering av Advanced Data Security åsidosätter Advanced Threat Protection-princip</span><span class="sxs-lookup"><span data-stu-id="ced70-1362">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="ced70-1363">Nya cmdletar för Management.Sql som gör att kunderna kan lägga till nycklar för transparent datakryptering (TDE) och ange TDE-skydd för hanterade instanser</span><span class="sxs-lookup"><span data-stu-id="ced70-1363">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="ced70-1364">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ced70-1364">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="ced70-1365">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ced70-1365">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="ced70-1366">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ced70-1366">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="ced70-1367">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="ced70-1367">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="ced70-1368">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="ced70-1368">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ced70-1369">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ced70-1369">Az.Storage</span></span>
* <span data-ttu-id="ced70-1370">Stöd för typerna FileStorage och SkuName Premium_ZRS när lagringskonton skapas</span><span class="sxs-lookup"><span data-stu-id="ced70-1370">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="ced70-1371">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ced70-1371">New-AzStorageAccount</span></span>
* <span data-ttu-id="ced70-1372">Beskrivningen av cmdleten för bloboföränderlighet har förtydligats</span><span class="sxs-lookup"><span data-stu-id="ced70-1372">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="ced70-1373">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="ced70-1373">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ced70-1374">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ced70-1374">Az.Websites</span></span>
* <span data-ttu-id="ced70-1375">Optimerar Get-AzWebAppCertificate för att filtrera efter resursgrupp på servern i stället för klienten</span><span class="sxs-lookup"><span data-stu-id="ced70-1375">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="ced70-1376">Lägger till växlingsparametern -UseDisasterRecovery till Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="ced70-1376">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="ced70-1377">2.2.0 – juni 2019</span><span class="sxs-lookup"><span data-stu-id="ced70-1377">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="ced70-1378">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="ced70-1378">Az.Cdn</span></span>
* <span data-ttu-id="ced70-1379">Uppdaterade cmdletar för att ge stöd för rulesEngine-funktion baserat på API-version 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="ced70-1379">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ced70-1380">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ced70-1380">Az.Compute</span></span>
* <span data-ttu-id="ced70-1381">Lade till parameter `NoWait` som startar åtgärden och returnerar omedelbart, innan åtgärden har slutförts.</span><span class="sxs-lookup"><span data-stu-id="ced70-1381">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="ced70-1382">Uppdaterade cmdletar:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="ced70-1382">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="ced70-1383">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="ced70-1383">Az.EventHub</span></span>
* <span data-ttu-id="ced70-1384">Korrigering för #9231 – Get-AzEventHubNamespace returnerar inga taggar</span><span class="sxs-lookup"><span data-stu-id="ced70-1384">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="ced70-1385">Korrigering för #9230 – Get-AzEventHubNamespace returnerar ResourceGroup istället för ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ced70-1385">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ced70-1386">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ced70-1386">Az.Network</span></span>
* <span data-ttu-id="ced70-1387">Uppdatera ResourceId och InputObject för NAT-gateway</span><span class="sxs-lookup"><span data-stu-id="ced70-1387">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="ced70-1388">Lägg till alias för ResourceId och InputObject</span><span class="sxs-lookup"><span data-stu-id="ced70-1388">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="ced70-1389">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ced70-1389">Az.PolicyInsights</span></span>
* <span data-ttu-id="ced70-1390">Åtgärda Null-referensproblem i Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="ced70-1390">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ced70-1391">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ced70-1391">Az.RecoveryServices</span></span>
* <span data-ttu-id="ced70-1392">Minsta kvarhållning för IaaSVM-policy i dagar ändrat till 7 från 1</span><span class="sxs-lookup"><span data-stu-id="ced70-1392">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="ced70-1393">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ced70-1393">Az.ServiceBus</span></span>
* <span data-ttu-id="ced70-1394">Korrigering för ärende #9182 – Get-AzServiceBusNamespace returnerar ResourceGroup istället för ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ced70-1394">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ced70-1395">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ced70-1395">Az.ServiceFabric</span></span>
* <span data-ttu-id="ced70-1396">Åtgärda stavfel i felmeddelandet för Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="ced70-1396">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="ced70-1397">Åtgärda saknat tecken i Service Fabric-kommandorader</span><span class="sxs-lookup"><span data-stu-id="ced70-1397">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="ced70-1398">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ced70-1398">Az.Sql</span></span>
* <span data-ttu-id="ced70-1399">Lägg till parametern DnsZonePartner för New-AzureSqlInstance-cmdlet för att ge stöd för AutoDr för hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="ced70-1399">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="ced70-1400">Avvecklar cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="ced70-1400">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="ced70-1401">Döp om cmdletar för hotidentifiering till Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="ced70-1401">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="ced70-1402">Parametrarna New-AzSqlInstance -StorageSizeInGB och -LicenseType är nu valfria.</span><span class="sxs-lookup"><span data-stu-id="ced70-1402">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ced70-1403">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ced70-1403">Az.Websites</span></span>
* <span data-ttu-id="ced70-1404">åtgärdar problemet där användningen av Set-AzWebApp och Set-AzWebAppSlot med -WebApp-egenskap tog bort taggarna</span><span class="sxs-lookup"><span data-stu-id="ced70-1404">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="ced70-1405">2.1.0 – maj 2019</span><span class="sxs-lookup"><span data-stu-id="ced70-1405">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="ced70-1406">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ced70-1406">Az.ApiManagement</span></span>
* <span data-ttu-id="ced70-1407">Skapade nya cmdletar för att hantera diagnostik för global- och API-omfång</span><span class="sxs-lookup"><span data-stu-id="ced70-1407">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="ced70-1408">**Get-AzApiManagementDiagnostic** – Skaffa diagnostik konfigurerad för global- eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="ced70-1408">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="ced70-1409">**New-AzApiManagementDiagnostic** – Skapa ny diagnostik för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="ced70-1409">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="ced70-1410">**New-AzApiManagementHttpMessageDiagnostic** – Skapa diagnostikinställning om vilka rubriker som ska loggas och storleken på brödtextbyte</span><span class="sxs-lookup"><span data-stu-id="ced70-1410">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="ced70-1411">**New-AzApiManagementPipelineDiagnosticSetting** – Skapa diagnostikinställningar för inkommande/utgående HTTP-meddelanden till gatewayen.</span><span class="sxs-lookup"><span data-stu-id="ced70-1411">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="ced70-1412">**New-AzApiManagementSamplingSetting** – Skapa samplinginställningar för begäranden/svar för en diagnostik</span><span class="sxs-lookup"><span data-stu-id="ced70-1412">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="ced70-1413">**Remove-AzApiManagementDiagnostic** – Ta bort en diagnostikenhet för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="ced70-1413">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="ced70-1414">**Set-AzApiManagementDiagnostic** – Uppdatera en diagnostikenhet för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="ced70-1414">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="ced70-1415">Skapade nya cmdletar för hantering av cacheminne i ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="ced70-1415">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="ced70-1416">**Get-AzApiManagementCache** – Hämta information om cacheminnet som anges av identifierare eller alla cacheminnen</span><span class="sxs-lookup"><span data-stu-id="ced70-1416">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="ced70-1417">**New-AzApiManagementCache** – Skapa ett nytt default-cacheminne eller cacheminne i en viss Azure-region</span><span class="sxs-lookup"><span data-stu-id="ced70-1417">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="ced70-1418">**Remove-AzApiManagementCache** – Ta bort ett cacheminne</span><span class="sxs-lookup"><span data-stu-id="ced70-1418">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="ced70-1419">**Remove-AzApiManagementCache** – Ta bort ett cacheminne</span><span class="sxs-lookup"><span data-stu-id="ced70-1419">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="ced70-1420">Skapade nya cmdletar för hantering av API-schema</span><span class="sxs-lookup"><span data-stu-id="ced70-1420">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="ced70-1421">**New-AzApiManagementSchema** – Skapa ett nytt schema för ett API</span><span class="sxs-lookup"><span data-stu-id="ced70-1421">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="ced70-1422">**Get-AzApiManagementSchema** – Hämta de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="ced70-1422">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="ced70-1423">**Remove-AzApiManagementSchema** – Ta bort de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="ced70-1423">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="ced70-1424">**Set-AzApiManagementSchema** – Uppdatera de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="ced70-1424">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="ced70-1425">Skapa ny cmdlet för att generera en användartoken.</span><span class="sxs-lookup"><span data-stu-id="ced70-1425">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="ced70-1426">**New-AzApiManagementUserToken** – Skapa en ny användartoken som enligt standardinställning är giltig i 8 timmar. Token för GIT-användaren kan skapas med den här cmdleten./</span><span class="sxs-lookup"><span data-stu-id="ced70-1426">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="ced70-1427">Skapade en ny cmdlet för att hämta nätverksstatus</span><span class="sxs-lookup"><span data-stu-id="ced70-1427">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="ced70-1428">**Get-AzApiManagementNetworkStatus** – Hämta nätverksstatusanslutningen för resurserna som API Management-tjänsten är beroende av.</span><span class="sxs-lookup"><span data-stu-id="ced70-1428">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="ced70-1429">Det här är användbart när du distribuerar ApiManagement-tjänsten i ett virtuellt nätverk och validerar om något beroende är brutet.</span><span class="sxs-lookup"><span data-stu-id="ced70-1429">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="ced70-1430">Uppdaterade cmdlet **New-AzApiManagement** för att hantera ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="ced70-1430">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="ced70-1431">Lade till stöd för den nya SKU:n Consumption</span><span class="sxs-lookup"><span data-stu-id="ced70-1431">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="ced70-1432">Aktiverade stöd för att slå på flaggan EnableClientCertificate för SKU:n Consumption</span><span class="sxs-lookup"><span data-stu-id="ced70-1432">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="ced70-1433">Den nya cmdleten **New-AzApiManagementSslSetting** gör det möjligt att ställa in TLS/SSL-inställningen på ”Backend” och ”Frontend” (serverdel och klientdel).</span><span class="sxs-lookup"><span data-stu-id="ced70-1433">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="ced70-1434">Det här kan också användas till att konfigurera chiffer som 3DES och ServerProtocols som Http2 för Frontend för en ApiManagement-tjänst.</span><span class="sxs-lookup"><span data-stu-id="ced70-1434">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="ced70-1435">Stöd har lagts till för att konfigurera värdnamnet DeveloperPortal på ApiManagement-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="ced70-1435">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="ced70-1436">Uppdaterade cmdletar **Get-AzApiManagementSsoToken** för att ta PsApiManagement-objekt som indata</span><span class="sxs-lookup"><span data-stu-id="ced70-1436">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="ced70-1437">Uppdaterad cmdleten för att visa infogade felmeddelanden</span><span class="sxs-lookup"><span data-stu-id="ced70-1437">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="ced70-1438">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Felkod: Felmeddelande av typen ValidationError: Ett eller flera fält innehåller felaktiga värden: Felinformation:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="ced70-1438">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="ced70-1439">Uppdaterade cmdlet **Export-AzApiManagementApi** för att exportera API:er i OpenApi 3.0-format</span><span class="sxs-lookup"><span data-stu-id="ced70-1439">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="ced70-1440">Uppdaterade cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="ced70-1440">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="ced70-1441">Importera API från dokumentspecifikationen OpenApi 3.0</span><span class="sxs-lookup"><span data-stu-id="ced70-1441">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="ced70-1442">Om du vill åsidosätta egenskapen PsApiManagementSchema specificerad i ett dokument (Swagger, Wadl, Wsdl, OpenApi).</span><span class="sxs-lookup"><span data-stu-id="ced70-1442">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="ced70-1443">Åsidosätta egenskapen ServiceUrl som specificeras i ett dokument.</span><span class="sxs-lookup"><span data-stu-id="ced70-1443">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="ced70-1444">Uppdaterade cmdlet **Get-AzApiManagementPolicy** för att returnera policy i undantaget format av typen icke-XML med rawxml</span><span class="sxs-lookup"><span data-stu-id="ced70-1444">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="ced70-1445">Uppdaterade cmdlet **Set-AzApiManagementPolicy** för att godkänna policy i undantaget format av typen icke-XML med rawxml och XML undantaget med xml</span><span class="sxs-lookup"><span data-stu-id="ced70-1445">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="ced70-1446">Uppdaterad cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="ced70-1446">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="ced70-1447">Konfigurera API med OpenId auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="ced70-1447">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="ced70-1448">Skapa ett API i ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="ced70-1448">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="ced70-1449">Klona ett API med SourceApiId och SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="ced70-1449">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="ced70-1450">Möjlighet att konfigurera SubscriptionRequired i API-omfattningen.</span><span class="sxs-lookup"><span data-stu-id="ced70-1450">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="ced70-1451">Uppdaterad cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="ced70-1451">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="ced70-1452">Konfigurera API med OpenId auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="ced70-1452">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="ced70-1453">Uppdatera ett API till ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="ced70-1453">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="ced70-1454">Möjlighet att konfigurera SubscriptionRequired i API-omfattningen.</span><span class="sxs-lookup"><span data-stu-id="ced70-1454">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="ced70-1455">Uppdaterad cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="ced70-1455">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="ced70-1456">Klona en befintlig version med hjälp av SourceApiRevision (kopiera taggar, produkter, åtgärder och principer).</span><span class="sxs-lookup"><span data-stu-id="ced70-1456">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="ced70-1457">Den nya revisionen antar ApiId från den överordnade instansen.</span><span class="sxs-lookup"><span data-stu-id="ced70-1457">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="ced70-1458">Tillhandahålla ApiRevisionDescription</span><span class="sxs-lookup"><span data-stu-id="ced70-1458">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="ced70-1459">Åsidosätta ServiceUrl vid kloning av ett API.</span><span class="sxs-lookup"><span data-stu-id="ced70-1459">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="ced70-1460">Uppdaterad cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="ced70-1460">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="ced70-1461">Konfigurera AAD eller AADB2C med en Authority</span><span class="sxs-lookup"><span data-stu-id="ced70-1461">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="ced70-1462">Konfigurera SignupPolicy, SigninPolicy, ProfileEditingPolicy och PasswordResetPolicy</span><span class="sxs-lookup"><span data-stu-id="ced70-1462">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="ced70-1463">Uppdaterad cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="ced70-1463">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="ced70-1464">Kompensera för ny SubscriptonModel med Scope och UserId</span><span class="sxs-lookup"><span data-stu-id="ced70-1464">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="ced70-1465">Kompensera för gammal prenumerationsmodell med ProductId och UserId</span><span class="sxs-lookup"><span data-stu-id="ced70-1465">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="ced70-1466">Lägg till funktion för att aktivera AllowTracing på prenumerationsnivå.</span><span class="sxs-lookup"><span data-stu-id="ced70-1466">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="ced70-1467">Uppdaterad cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="ced70-1467">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="ced70-1468">Kompensera för ny SubscriptonModel med Scope och UserId</span><span class="sxs-lookup"><span data-stu-id="ced70-1468">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="ced70-1469">Kompensera för gammal prenumerationsmodell med ProductId och UserId</span><span class="sxs-lookup"><span data-stu-id="ced70-1469">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="ced70-1470">Lägg till funktion för att aktivera AllowTracing på prenumerationsnivå.</span><span class="sxs-lookup"><span data-stu-id="ced70-1470">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="ced70-1471">Uppdaterade följande cmdletar för att acceptera ResourceId som indata</span><span class="sxs-lookup"><span data-stu-id="ced70-1471">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="ced70-1472">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ced70-1472">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="ced70-1473">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="ced70-1473">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="ced70-1474">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="ced70-1474">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="ced70-1475">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="ced70-1475">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="ced70-1476">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="ced70-1476">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="ced70-1477">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="ced70-1477">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="ced70-1478">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="ced70-1478">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="ced70-1479">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="ced70-1479">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="ced70-1480">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="ced70-1480">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="ced70-1481">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="ced70-1481">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="ced70-1482">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="ced70-1482">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="ced70-1483">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="ced70-1483">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ced70-1484">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ced70-1484">Az.Automation</span></span>
* <span data-ttu-id="ced70-1485">Uppdaterade Get-AzAutomationJobOutputRecord för att hantera postvärden av typen JSON och Text.</span><span class="sxs-lookup"><span data-stu-id="ced70-1485">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="ced70-1486">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="ced70-1486">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="ced70-1487">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="ced70-1487">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="ced70-1488">Ändrade beteende för Start-AzAutomationDscCompilationJob till att bara starta jobbet istället för att vänta på slutförandet.</span><span class="sxs-lookup"><span data-stu-id="ced70-1488">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="ced70-1489">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="ced70-1489">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="ced70-1490">Korrigering för Get-AzAutomationDscNode när using -Name returnerar alla noder.</span><span class="sxs-lookup"><span data-stu-id="ced70-1490">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="ced70-1491">Nu returnerar den endast den matchande noden.</span><span class="sxs-lookup"><span data-stu-id="ced70-1491">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ced70-1492">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ced70-1492">Az.Compute</span></span>
* <span data-ttu-id="ced70-1493">Lägg till parametrarna ProtectFromScaleIn och ProtectFromScaleSetAction i cmdleten Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="ced70-1493">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="ced70-1494">Nu är standardinställningen att vimpelparametern New-AzVM använder en tillgänglig plats om USA, östra inte stöds</span><span class="sxs-lookup"><span data-stu-id="ced70-1494">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ced70-1495">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ced70-1495">Az.DataLakeStore</span></span>
* <span data-ttu-id="ced70-1496">Uppdatera ADLS-sdk för att använda httpclient, integrera dataplanstestning med Azure-ramverk</span><span class="sxs-lookup"><span data-stu-id="ced70-1496">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ced70-1497">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ced70-1497">Az.Monitor</span></span>
* <span data-ttu-id="ced70-1498">Korrigera felaktiga parameternamn i hjälpexempel</span><span class="sxs-lookup"><span data-stu-id="ced70-1498">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ced70-1499">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ced70-1499">Az.Network</span></span>
* <span data-ttu-id="ced70-1500">Lägg till flaggan DisableBgpRoutePropagation i utdata för effektiv routningstabell</span><span class="sxs-lookup"><span data-stu-id="ced70-1500">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="ced70-1501">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="ced70-1501">Updated cmdlet:</span></span>
        - <span data-ttu-id="ced70-1502">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="ced70-1502">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="ced70-1503">Åtgärda dubbelstreck i dokumentationen New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ced70-1503">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="ced70-1504">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ced70-1504">Az.Resources</span></span>
* <span data-ttu-id="ced70-1505">Lägg till ny cmdlet Get-AzureRmDenyAssignment för att hämta tilldelningsnekanden</span><span class="sxs-lookup"><span data-stu-id="ced70-1505">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="ced70-1506">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ced70-1506">Az.Sql</span></span>
* <span data-ttu-id="ced70-1507">Döp om Advanced Threat Protection-cmdletar för Advanced Data Security och aktivera Vulnerability Assessment som standard</span><span class="sxs-lookup"><span data-stu-id="ced70-1507">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="ced70-1508">2.0.0 – maj 2019</span><span class="sxs-lookup"><span data-stu-id="ced70-1508">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ced70-1509">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ced70-1509">Az.Accounts</span></span>
* <span data-ttu-id="ced70-1510">Uppdatera autentiseringsbiblioteket för att åtgärda ADFS-problem med autentisering av användarnamn/lösenord</span><span class="sxs-lookup"><span data-stu-id="ced70-1510">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="ced70-1511">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ced70-1511">Az.CognitiveServices</span></span>
* <span data-ttu-id="ced70-1512">Visa endast Bing-ansvarsfriskrivning för Bing-sökningstjänster.</span><span class="sxs-lookup"><span data-stu-id="ced70-1512">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="ced70-1513">Förbättra felmeddelande när det inte går att skapa konton.</span><span class="sxs-lookup"><span data-stu-id="ced70-1513">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ced70-1514">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ced70-1514">Az.Compute</span></span>
* <span data-ttu-id="ced70-1515">Funktion för närhetsplaceringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="ced70-1515">Proximity placement group feature.</span></span>
    - <span data-ttu-id="ced70-1516">Följande nya cmdletar har lagts till:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="ced70-1516">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="ced70-1517">Den nya parametern ProximityPlacementGroupId har lagts till i följande cmdletar:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="ced70-1517">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="ced70-1518">Parametern StorageAccountType har lagts till i New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="ced70-1518">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="ced70-1519">TargetRegion för New-AzGalleryImageVersion kan innehålla StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="ced70-1519">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="ced70-1520">Växlingsparametern SkipShutdown har lagts till i Stop-AzVM och Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ced70-1520">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="ced70-1521">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="ced70-1521">Breaking changes</span></span>
    - <span data-ttu-id="ced70-1522">Set-AzVMBootDiagnostics har ändrats till Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="ced70-1522">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="ced70-1523">Export-AzLogAnalyticThrottledRequests har ändrats till Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="ced70-1523">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="ced70-1524">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="ced70-1524">Az.DeploymentManager</span></span>
* <span data-ttu-id="ced70-1525">De första allmänt tillgängliga versionerna av cmdletar för Distributionshanteraren i Azure</span><span class="sxs-lookup"><span data-stu-id="ced70-1525">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="ced70-1526">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="ced70-1526">Az.Dns</span></span>
* <span data-ttu-id="ced70-1527">Automatisk delegering av DNS för NameServer</span><span class="sxs-lookup"><span data-stu-id="ced70-1527">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="ced70-1528">Det överordnade zonnamnet kan användas som ytterligare valfri parameter i cmdleten för att skapa DNS-zoner.</span><span class="sxs-lookup"><span data-stu-id="ced70-1528">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="ced70-1529">Lägger till NS-poster för en nyligen skapad underordnad zon i den överordnade zonen.</span><span class="sxs-lookup"><span data-stu-id="ced70-1529">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="ced70-1530">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="ced70-1530">Az.FrontDoor</span></span>
* <span data-ttu-id="ced70-1531">De första allmänt tillgängliga versionerna av cmdletar för Azure FrontDoor</span><span class="sxs-lookup"><span data-stu-id="ced70-1531">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="ced70-1532">Byt namn på WAF-cmdletar så att de omfattar ”Waf”</span><span class="sxs-lookup"><span data-stu-id="ced70-1532">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="ced70-1533">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="ced70-1533">Az.HDInsight</span></span>
* <span data-ttu-id="ced70-1534">Två cmdletar har tagits bort:</span><span class="sxs-lookup"><span data-stu-id="ced70-1534">Removed two cmdlets:</span></span>
    - <span data-ttu-id="ced70-1535">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="ced70-1535">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="ced70-1536">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="ced70-1536">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="ced70-1537">En ny cmdlet har lagts till, Set-AzHDInsightGatewayCredential, som ersätter Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="ced70-1537">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="ced70-1538">Uppdatera cmdleten Get-AzHDInsightJobOutput för att skilja mellan läsarrollen och HDInsight-operatörsrollen:</span><span class="sxs-lookup"><span data-stu-id="ced70-1538">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="ced70-1539">Användare med läsarrollen måste uttryckligen ange parametern ”DefaultStorageAccountKey”, annars uppstår fel.</span><span class="sxs-lookup"><span data-stu-id="ced70-1539">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="ced70-1540">Användare med HDInsight-operatörsrollen påverkas inte.</span><span class="sxs-lookup"><span data-stu-id="ced70-1540">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ced70-1541">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ced70-1541">Az.Monitor</span></span>
* <span data-ttu-id="ced70-1542">Nya cmdletar för SQR API (schemalagd frågeregel)</span><span class="sxs-lookup"><span data-stu-id="ced70-1542">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="ced70-1543">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="ced70-1543">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="ced70-1544">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="ced70-1544">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="ced70-1545">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="ced70-1545">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="ced70-1546">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="ced70-1546">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="ced70-1547">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="ced70-1547">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="ced70-1548">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="ced70-1548">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="ced70-1549">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="ced70-1549">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="ced70-1550">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="ced70-1550">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="ced70-1551">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="ced70-1551">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="ced70-1552">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="ced70-1552">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="ced70-1553">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="ced70-1553">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="ced70-1554">[Mer](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information om SQR API</span><span class="sxs-lookup"><span data-stu-id="ced70-1554">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="ced70-1555">Az.Monitor.md har uppdaterats för att omfatta cmdletar för måttbaserade aviseringsregler i GenV2 (inte klassiska)</span><span class="sxs-lookup"><span data-stu-id="ced70-1555">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ced70-1556">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ced70-1556">Az.Network</span></span>
* <span data-ttu-id="ced70-1557">Lägg till stöd för NAT Gateway-resurs</span><span class="sxs-lookup"><span data-stu-id="ced70-1557">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="ced70-1558">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="ced70-1558">New cmdlets</span></span>
        - <span data-ttu-id="ced70-1559">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="ced70-1559">New-AzNatGateway</span></span>
        - <span data-ttu-id="ced70-1560">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="ced70-1560">Get-AzNatGateway</span></span>
        - <span data-ttu-id="ced70-1561">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="ced70-1561">Set-AzNatGateway</span></span>
        - <span data-ttu-id="ced70-1562">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="ced70-1562">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="ced70-1563">Uppdaterade cmdletar</span><span class="sxs-lookup"><span data-stu-id="ced70-1563">Updated cmdlets</span></span>
        - <span data-ttu-id="ced70-1564">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="ced70-1564">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="ced70-1565">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="ced70-1565">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="ced70-1566">Nedanstående kommandon för funktionen har uppdaterats: Ange/ta bort anpassade vägar på Brooklyn Gateway.</span><span class="sxs-lookup"><span data-stu-id="ced70-1566">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="ced70-1567">New-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ställa in adressprefix som anpassade vägar för att ange gateway.</span><span class="sxs-lookup"><span data-stu-id="ced70-1567">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="ced70-1568">Set-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ange adressprefix som anpassade vägar för att ange gateway.</span><span class="sxs-lookup"><span data-stu-id="ced70-1568">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="ced70-1569">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ced70-1569">Az.PolicyInsights</span></span>
* <span data-ttu-id="ced70-1570">Stöd för att fråga efter information om principutvärdering.</span><span class="sxs-lookup"><span data-stu-id="ced70-1570">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="ced70-1571">Lägg till parametern ”-Expand” för Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="ced70-1571">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="ced70-1572">Stöd för -Expand PolicyEvaluationDetails.</span><span class="sxs-lookup"><span data-stu-id="ced70-1572">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ced70-1573">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ced70-1573">Az.RecoveryServices</span></span>
* <span data-ttu-id="ced70-1574">Stöd för att dela prenumeration mellan Azure och Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="ced70-1574">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="ced70-1575">Markering av kommande icke-bakåtkompatibla ändringar för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="ced70-1575">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="ced70-1576">Korrigering för återställningsplan och åtgärdsplan i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="ced70-1576">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="ced70-1577">Korrigering för mappning av uppdateringsnätverk i Azure Site Recovery för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="ced70-1577">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="ced70-1578">Korrigering för instruktioner för uppdateringsskydd i Azure Site Recovery för Azure till Azure för hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="ced70-1578">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="ced70-1579">Andra mindre korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="ced70-1579">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="ced70-1580">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="ced70-1580">Az.Relay</span></span>
* <span data-ttu-id="ced70-1581">Korrigera stavfel i kundriktade meddelanden</span><span class="sxs-lookup"><span data-stu-id="ced70-1581">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="ced70-1582">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ced70-1582">Az.ServiceBus</span></span>
* <span data-ttu-id="ced70-1583">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="ced70-1583">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ced70-1584">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ced70-1584">Az.Storage</span></span>
* <span data-ttu-id="ced70-1585">Uppgradera till lagringsklientbiblioteket 10.0.1 (namnområdet för alla objekt från detta SDK ändras från ”Microsoft.WindowsAzure.Storage. *till ”Microsoft.Azure.Storage.* ”)</span><span class="sxs-lookup"><span data-stu-id="ced70-1585">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="ced70-1586">Uppgradera till Microsoft.Azure.Management.Storage 11.0.0 för att stödja den nya API-versionen 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="ced70-1586">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="ced70-1587">Standardlagringskontot i Skapa lagringskonto ändras från ”Storage” till ”StorageV2”</span><span class="sxs-lookup"><span data-stu-id="ced70-1587">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="ced70-1588">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ced70-1588">New-AzStorageAccount</span></span>
* <span data-ttu-id="ced70-1589">Ändra lagringskontots cmdlet-utdata Sku.Name för att passa med indata-SkuName genom att lägga till ”-”. Till exempel ändras ”StandardLRS” till ”Standard_LRS”</span><span class="sxs-lookup"><span data-stu-id="ced70-1589">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="ced70-1590">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ced70-1590">New-AzStorageAccount</span></span>
    - <span data-ttu-id="ced70-1591">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ced70-1591">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="ced70-1592">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ced70-1592">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ced70-1593">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ced70-1593">Az.Websites</span></span>
* <span data-ttu-id="ced70-1594">Egenskapen ”typ” konfigureras nu för PSSite-objekt som returneras av Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ced70-1594">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="ced70-1595">Get-AzWebApp\*Metrics och Get-AzAppServicePlanMetrics markeras som inaktuella</span><span class="sxs-lookup"><span data-stu-id="ced70-1595">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="ced70-1596">1.8.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="ced70-1596">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="ced70-1597">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="ced70-1597">Highlights since the last major release</span></span>
* <span data-ttu-id="ced70-1598">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="ced70-1598">General availability of `Az` module</span></span>
* <span data-ttu-id="ced70-1599">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="ced70-1599">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="ced70-1600">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="ced70-1600">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="ced70-1601">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="ced70-1601">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="ced70-1602">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="ced70-1602">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="ced70-1603">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="ced70-1603">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="ced70-1604">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="ced70-1604">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="ced70-1605">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ced70-1605">Az.Accounts</span></span>
* <span data-ttu-id="ced70-1606">Uppdatera Uninstall-AzureRm för att ta bort moduler i Mac på ett korrekt sätt</span><span class="sxs-lookup"><span data-stu-id="ced70-1606">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="ced70-1607">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="ced70-1607">Az.Batch</span></span>
* <span data-ttu-id="ced70-1608">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="ced70-1608">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="ced70-1609">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="ced70-1609">Az.Cdn</span></span>
* <span data-ttu-id="ced70-1610">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="ced70-1610">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="ced70-1611">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ced70-1611">Az.CognitiveServices</span></span>
* <span data-ttu-id="ced70-1612">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="ced70-1612">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ced70-1613">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ced70-1613">Az.Compute</span></span>
* <span data-ttu-id="ced70-1614">Åtgärda problem med AEM-installationen om resurs-ID:n för diskar innehåller resourcegroups i gemener i resurs-ID:n</span><span class="sxs-lookup"><span data-stu-id="ced70-1614">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="ced70-1615">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="ced70-1615">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="ced70-1616">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="ced70-1616">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ced70-1617">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ced70-1617">Az.DataFactory</span></span>
* <span data-ttu-id="ced70-1618">Lägg till SsisProperties om NodeCount inte är null för hanterad integreringskörning.</span><span class="sxs-lookup"><span data-stu-id="ced70-1618">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ced70-1619">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ced70-1619">Az.DataLakeStore</span></span>
* <span data-ttu-id="ced70-1620">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="ced70-1620">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="ced70-1621">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="ced70-1621">Az.EventGrid</span></span>
* <span data-ttu-id="ced70-1622">Hjälptexten för slutpunkten har uppdaterats för att visa att resurser ska skapas innan cmdletarna för att skapa/uppdatera händelseprenumerationer används.</span><span class="sxs-lookup"><span data-stu-id="ced70-1622">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="ced70-1623">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="ced70-1623">Az.EventHub</span></span>
* <span data-ttu-id="ced70-1624">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="ced70-1624">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="ced70-1625">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="ced70-1625">Az.HDInsight</span></span>
* <span data-ttu-id="ced70-1626">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="ced70-1626">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ced70-1627">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ced70-1627">Az.IotHub</span></span>
* <span data-ttu-id="ced70-1628">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="ced70-1628">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ced70-1629">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ced70-1629">Az.KeyVault</span></span>
* <span data-ttu-id="ced70-1630">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="ced70-1630">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="ced70-1631">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="ced70-1631">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="ced70-1632">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="ced70-1632">Az.MachineLearning</span></span>
* <span data-ttu-id="ced70-1633">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="ced70-1633">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="ced70-1634">Az.Media</span><span class="sxs-lookup"><span data-stu-id="ced70-1634">Az.Media</span></span>
* <span data-ttu-id="ced70-1635">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="ced70-1635">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ced70-1636">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ced70-1636">Az.Monitor</span></span>
  * <span data-ttu-id="ced70-1637">Nya cmdletar för måttbaserad aviseringsregel i GenV2 (inte klassisk)</span><span class="sxs-lookup"><span data-stu-id="ced70-1637">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="ced70-1638">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="ced70-1638">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="ced70-1639">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="ced70-1639">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="ced70-1640">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="ced70-1640">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="ced70-1641">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="ced70-1641">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="ced70-1642">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="ced70-1642">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="ced70-1643">Monitor SDK har uppdaterats till version 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="ced70-1643">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ced70-1644">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ced70-1644">Az.Network</span></span>
* <span data-ttu-id="ced70-1645">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="ced70-1645">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="ced70-1646">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="ced70-1646">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="ced70-1647">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="ced70-1647">Az.NotificationHubs</span></span>
* <span data-ttu-id="ced70-1648">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="ced70-1648">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ced70-1649">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ced70-1649">Az.OperationalInsights</span></span>
* <span data-ttu-id="ced70-1650">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="ced70-1650">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="ced70-1651">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="ced70-1651">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="ced70-1652">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="ced70-1652">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ced70-1653">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ced70-1653">Az.RecoveryServices</span></span>
* <span data-ttu-id="ced70-1654">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="ced70-1654">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="ced70-1655">Tabellformatet för SQL i virtuella Azure-datorer har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="ced70-1655">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="ced70-1656">En alternativ metod för att hämta platser i AzureFileShare har lagts till</span><span class="sxs-lookup"><span data-stu-id="ced70-1656">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="ced70-1657">ScheduleRunDays i SchedulePolicy-objekt har uppdaterats enligt tidszon</span><span class="sxs-lookup"><span data-stu-id="ced70-1657">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="ced70-1658">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="ced70-1658">Az.RedisCache</span></span>
* <span data-ttu-id="ced70-1659">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="ced70-1659">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ced70-1660">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ced70-1660">Az.Resources</span></span>
* <span data-ttu-id="ced70-1661">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="ced70-1661">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="ced70-1662">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ced70-1662">Az.Sql</span></span>
* <span data-ttu-id="ced70-1663">Ersätt Monitor SDK-beroende med vanlig kod</span><span class="sxs-lookup"><span data-stu-id="ced70-1663">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="ced70-1664">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="ced70-1664">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="ced70-1665">Förbättrad process för klassificering av flera kolumner.</span><span class="sxs-lookup"><span data-stu-id="ced70-1665">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="ced70-1666">Inkludera SKU-egenskaper (SKU-namn, serie, kapacitet) i svaret från Get-AzSqlServerServiceObjective och formatera som tabell som standard.</span><span class="sxs-lookup"><span data-stu-id="ced70-1666">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="ced70-1667">Möjlighet att använda Get-AzSqlServerServiceObjective efter plats utan att behöva en redan befintlig server i regionen.</span><span class="sxs-lookup"><span data-stu-id="ced70-1667">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="ced70-1668">Stöd för tidszonsparametern när hanterade instanser skapas.</span><span class="sxs-lookup"><span data-stu-id="ced70-1668">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="ced70-1669">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="ced70-1669">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ced70-1670">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ced70-1670">Az.Websites</span></span>
* <span data-ttu-id="ced70-1671">åtgärdar Set-AzWebApp och Set-AzWebAppSlot så att de inte tar bort taggar vid körning</span><span class="sxs-lookup"><span data-stu-id="ced70-1671">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="ced70-1672">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="ced70-1672">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="ced70-1673">SDK för WebSites har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="ced70-1673">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="ced70-1674">Egenskapen AdminSiteName har tagits bort från PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="ced70-1674">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="ced70-1675">1.7.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="ced70-1675">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="ced70-1676">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="ced70-1676">Highlights since the last major release</span></span>
* <span data-ttu-id="ced70-1677">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="ced70-1677">General availability of `Az` module</span></span>
* <span data-ttu-id="ced70-1678">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="ced70-1678">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="ced70-1679">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="ced70-1679">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="ced70-1680">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="ced70-1680">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="ced70-1681">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="ced70-1681">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="ced70-1682">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="ced70-1682">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="ced70-1683">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="ced70-1683">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="ced70-1684">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ced70-1684">Az.Accounts</span></span>
* <span data-ttu-id="ced70-1685">Add-AzEnvironment och Set-AzEnvironment har uppdaterats för att godkänna parametern AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="ced70-1685">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="ced70-1686">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ced70-1686">Az.AnalysisServices</span></span>
* <span data-ttu-id="ced70-1687">ServiceClient används i cmdletar för dataplan och den ursprungliga autentiseringslogiken har tagits bort</span><span class="sxs-lookup"><span data-stu-id="ced70-1687">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="ced70-1688">Add-AzureASAccount används för omslutning av Connect-AzAccount för att undvika en icke-bakåtkompatibel ändring</span><span class="sxs-lookup"><span data-stu-id="ced70-1688">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ced70-1689">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ced70-1689">Az.Automation</span></span>
* <span data-ttu-id="ced70-1690">Buggen för cmdleten New-AzAutomationSoftwareUpdateConfiguration för inkluderingar har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="ced70-1690">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="ced70-1691">Nu bör parametern IncludedKbNumber och IncludedPackageNameMask fungera.</span><span class="sxs-lookup"><span data-stu-id="ced70-1691">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="ced70-1692">Felkorrigering för dynamiska grupper i uppdateringshanteringen för azure automation</span><span class="sxs-lookup"><span data-stu-id="ced70-1692">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ced70-1693">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ced70-1693">Az.Compute</span></span>
* <span data-ttu-id="ced70-1694">Lägg till parametern HyperVGeneration i New-AzDiskConfig och New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="ced70-1694">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="ced70-1695">Tillåt att virtuella datorer skapas med galleribilder från andra klientorganisationer.</span><span class="sxs-lookup"><span data-stu-id="ced70-1695">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="ced70-1696">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="ced70-1696">Az.ContainerInstance</span></span>
* <span data-ttu-id="ced70-1697">Ett problem har åtgärdats i parametern -Command för New-AzContainerGroup som lade till ett avslutande tomt argument</span><span class="sxs-lookup"><span data-stu-id="ced70-1697">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ced70-1698">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ced70-1698">Az.DataFactory</span></span>
* <span data-ttu-id="ced70-1699">ADF .Net SDK-versionen har uppdaterats till 3.0.2</span><span class="sxs-lookup"><span data-stu-id="ced70-1699">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="ced70-1700">Cmdleten Set-AzDataFactoryV2 har uppdaterats med extra parametrar för inställningar som rör RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="ced70-1700">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ced70-1701">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ced70-1701">Az.Resources</span></span>
* <span data-ttu-id="ced70-1702">Förbättra hanteringen av providrar för Get-AzResource när parametrarna -ResourceId eller -ResourceGroupName, -Name och -ResourceType tillhandahålls</span><span class="sxs-lookup"><span data-stu-id="ced70-1702">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="ced70-1703">Förbättra felhanteringen för ”Test-AzDeployment” och ”Test-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="ced70-1703">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="ced70-1704">Hantera fel utanför distributionsvalideringen och ta med dem i kommandoutdata istället</span><span class="sxs-lookup"><span data-stu-id="ced70-1704">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="ced70-1705">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="ced70-1705">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="ced70-1706">Lägg till växlingsparametern -IgnoreDynamicParameters till en uppsättning av cmdletar för distribution för att hoppa över fråga i skript och jobbscenarier</span><span class="sxs-lookup"><span data-stu-id="ced70-1706">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="ced70-1707">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="ced70-1707">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="ced70-1708">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ced70-1708">Az.Sql</span></span>
* <span data-ttu-id="ced70-1709">Stöd för dataklassificering av databaser.</span><span class="sxs-lookup"><span data-stu-id="ced70-1709">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ced70-1710">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ced70-1710">Az.Storage</span></span>
* <span data-ttu-id="ced70-1711">Rapportera detaljfel när lagringskontext skapas med parametern -UseConnectedAccount, men utan inloggning på Azure-kontot</span><span class="sxs-lookup"><span data-stu-id="ced70-1711">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="ced70-1712">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="ced70-1712">New-AzStorageContext</span></span>
* <span data-ttu-id="ced70-1713">Stöd för att hantera Blob Service-egenskaper för ett angivet lagringskonto med API:et för hanteringsplan</span><span class="sxs-lookup"><span data-stu-id="ced70-1713">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="ced70-1714">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="ced70-1714">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="ced70-1715">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="ced70-1715">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="ced70-1716">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="ced70-1716">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="ced70-1717">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="ced70-1717">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="ced70-1718">Stöd för -AsJob-cmdletar för att ladda upp och ladda ned blobar och filer</span><span class="sxs-lookup"><span data-stu-id="ced70-1718">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="ced70-1719">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ced70-1719">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="ced70-1720">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ced70-1720">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="ced70-1721">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="ced70-1721">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="ced70-1722">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="ced70-1722">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="ced70-1723">1.6.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="ced70-1723">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="ced70-1724">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="ced70-1724">Highlights since the last major release</span></span>
* <span data-ttu-id="ced70-1725">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="ced70-1725">General availability of `Az` module</span></span>
* <span data-ttu-id="ced70-1726">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="ced70-1726">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="ced70-1727">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="ced70-1727">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="ced70-1728">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="ced70-1728">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="ced70-1729">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="ced70-1729">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="ced70-1730">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="ced70-1730">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="ced70-1731">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="ced70-1731">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ced70-1732">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ced70-1732">Az.Automation</span></span>
* <span data-ttu-id="ced70-1733">Azure Automation – ändring av uppdateringshantering för stöd för de nya funktionerna:</span><span class="sxs-lookup"><span data-stu-id="ced70-1733">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="ced70-1734">Dynamisk gruppering</span><span class="sxs-lookup"><span data-stu-id="ced70-1734">Dynamic grouping</span></span>
    * <span data-ttu-id="ced70-1735">För-/efterskrift</span><span class="sxs-lookup"><span data-stu-id="ced70-1735">Pre-Post script</span></span>
    * <span data-ttu-id="ced70-1736">Inställning för omstart</span><span class="sxs-lookup"><span data-stu-id="ced70-1736">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ced70-1737">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ced70-1737">Az.Compute</span></span>
* <span data-ttu-id="ced70-1738">Åtgärda problem med sökvägsmatchning i Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="ced70-1738">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="ced70-1739">Uppdatera Compute-klientbibliotek till 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="ced70-1739">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ced70-1740">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ced70-1740">Az.KeyVault</span></span>
* <span data-ttu-id="ced70-1741">Stöd för jokertecken för KeyVault-cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="ced70-1741">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ced70-1742">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ced70-1742">Az.Network</span></span>
* <span data-ttu-id="ced70-1743">Lägg till stöd för Threat Intelligence för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="ced70-1743">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="ced70-1744">Lägg till resurs för brandväggsprincip på översta nivå och anpassade regler för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="ced70-1744">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ced70-1745">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ced70-1745">Az.RecoveryServices</span></span>
* <span data-ttu-id="ced70-1746">SnapshotRetentionInDays har lagts till i Azure-principen för virtuella datorer för stöd av Instant RP</span><span class="sxs-lookup"><span data-stu-id="ced70-1746">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="ced70-1747">Pipe-stöd för avregistrering av container har lagts till</span><span class="sxs-lookup"><span data-stu-id="ced70-1747">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="ced70-1748">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ced70-1748">Az.Resources</span></span>
* <span data-ttu-id="ced70-1749">Uppdatera stöd för jokertecken för Get-AzResource och Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ced70-1749">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="ced70-1750">Uppdatera autentiseringsuppgifter som används vid allmänna anrop till ARM</span><span class="sxs-lookup"><span data-stu-id="ced70-1750">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="ced70-1751">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ced70-1751">Az.Sql</span></span>
* <span data-ttu-id="ced70-1752">Cmdlet-parametern (ExcludeDetectionType) för Hotidentifiering ändrades från DetectionType till sträng[] för att framtidssäkra den när nya DetectionTypes läggs till, och även för att stödja automatisk ifyllning.</span><span class="sxs-lookup"><span data-stu-id="ced70-1752">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ced70-1753">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ced70-1753">Az.Storage</span></span>
* <span data-ttu-id="ced70-1754">Stöd för att hämta/ange/ta bort hanteringsprincip på ett lagringskonto</span><span class="sxs-lookup"><span data-stu-id="ced70-1754">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="ced70-1755">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="ced70-1755">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="ced70-1756">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="ced70-1756">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="ced70-1757">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="ced70-1757">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="ced70-1758">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="ced70-1758">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="ced70-1759">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="ced70-1759">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="ced70-1760">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="ced70-1760">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ced70-1761">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ced70-1761">Az.Websites</span></span>
* <span data-ttu-id="ced70-1762">Åtgärda fel med ARM-mall som avbryter kloning av alla platser med 'New-AzWebApp -IncludeSourceWebAppSlots'</span><span class="sxs-lookup"><span data-stu-id="ced70-1762">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="ced70-1763">1.5.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="ced70-1763">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ced70-1764">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ced70-1764">Az.Accounts</span></span>
* <span data-ttu-id="ced70-1765">Lägg till kommandot Register-AzModule för stöd för AutoRest-genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="ced70-1765">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="ced70-1766">Uppdatera exempel för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="ced70-1766">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ced70-1767">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ced70-1767">Az.Automation</span></span>
* <span data-ttu-id="ced70-1768">Problem med att hämta vissa månadsscheman i flera Azure Automation-cmdletar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="ced70-1768">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="ced70-1769">Åtgärda problem med att Get-AzAutomationDscNode bara returnerar de 20 översta noderna.</span><span class="sxs-lookup"><span data-stu-id="ced70-1769">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="ced70-1770">Nu returneras alla noder</span><span class="sxs-lookup"><span data-stu-id="ced70-1770">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="ced70-1771">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="ced70-1771">Az.Cdn</span></span>
* <span data-ttu-id="ced70-1772">Nya Powershell-cmdletar för att aktivera/inaktivera anpassade domän-HTTPS har lagts till och de gamla har gjorts inaktuella</span><span class="sxs-lookup"><span data-stu-id="ced70-1772">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ced70-1773">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ced70-1773">Az.Compute</span></span>
* <span data-ttu-id="ced70-1774">Lägg till stöd för jokertecken för Get-cmdletar</span><span class="sxs-lookup"><span data-stu-id="ced70-1774">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ced70-1775">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ced70-1775">Az.DataFactory</span></span>
* <span data-ttu-id="ced70-1776">ADF .Net SDK-versionen har uppdaterats till 3.0.1</span><span class="sxs-lookup"><span data-stu-id="ced70-1776">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="ced70-1777">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="ced70-1777">Az.LogicApp</span></span>
* <span data-ttu-id="ced70-1778">Åtgärda problemet med att ListWorkflows endast hämtar den första sidan med resultat</span><span class="sxs-lookup"><span data-stu-id="ced70-1778">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ced70-1779">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ced70-1779">Az.Network</span></span>
* <span data-ttu-id="ced70-1780">Lägg till stöd för jokertecken för Network-cmdletar</span><span class="sxs-lookup"><span data-stu-id="ced70-1780">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ced70-1781">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ced70-1781">Az.RecoveryServices</span></span>
* <span data-ttu-id="ced70-1782">Stöd har lagts till för SQL Server i virtuella Azure-datorer</span><span class="sxs-lookup"><span data-stu-id="ced70-1782">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="ced70-1783">SDK-uppdatering</span><span class="sxs-lookup"><span data-stu-id="ced70-1783">SDK Update</span></span>
* <span data-ttu-id="ced70-1784">Get-ProtectableItem-incheckning i VMappContainer har tagits bort</span><span class="sxs-lookup"><span data-stu-id="ced70-1784">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="ced70-1785">Name och ServerName har lagts till som parametrar för Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="ced70-1785">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="ced70-1786">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ced70-1786">Az.Resources</span></span>
* <span data-ttu-id="ced70-1787">Lägg till parametern `-TemplateObject` i cmdletar för distribution</span><span class="sxs-lookup"><span data-stu-id="ced70-1787">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="ced70-1788">Mer information här: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="ced70-1788">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="ced70-1789">Åtgärda problem med piping av resultatet i `Get-AzResource` till `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="ced70-1789">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="ced70-1790">Mer information här: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="ced70-1790">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="ced70-1791">Åtgärda problem med ändring av JSON-datatyp när `Set-AzResource` körs</span><span class="sxs-lookup"><span data-stu-id="ced70-1791">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="ced70-1792">Mer information här: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="ced70-1792">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="ced70-1793">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ced70-1793">Az.Sql</span></span>
* <span data-ttu-id="ced70-1794">AuditingEndpointsCommunicator uppdateras.</span><span class="sxs-lookup"><span data-stu-id="ced70-1794">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="ced70-1795">Åtgärdar beteendet hos ett gränsscenario när nya diagnostikinställningar skapas.</span><span class="sxs-lookup"><span data-stu-id="ced70-1795">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ced70-1796">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ced70-1796">Az.Storage</span></span>
* <span data-ttu-id="ced70-1797">Stöd för BlockBlobStorage när Storage-konto skapas      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ced70-1797">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="ced70-1798">1.4.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="ced70-1798">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="ced70-1799">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ced70-1799">Az.AnalysisServices</span></span>
* <span data-ttu-id="ced70-1800">Inaktuell AddAzureASAccount-cmdlet</span><span class="sxs-lookup"><span data-stu-id="ced70-1800">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ced70-1801">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ced70-1801">Az.Automation</span></span>
* <span data-ttu-id="ced70-1802">Hjälpen för Import-AzAutomationDscNodeConfiguration har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="ced70-1802">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="ced70-1803">Konfigurationsnamnsvalidering har lagts till i cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="ced70-1803">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="ced70-1804">Förbättrad felhantering för cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="ced70-1804">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="ced70-1805">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ced70-1805">Az.CognitiveServices</span></span>
* <span data-ttu-id="ced70-1806">CustomSubdomainName har lagts till som en ny valfri parameter för New-AzCognitiveServicesAccount, som används för att ange underdomän för resursen.</span><span class="sxs-lookup"><span data-stu-id="ced70-1806">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ced70-1807">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ced70-1807">Az.Compute</span></span>
* <span data-ttu-id="ced70-1808">Problemet med ID-parameteruppsättningar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="ced70-1808">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="ced70-1809">Get-AzVMExtension har uppdaterats så att alla installerade tillägg visas om parametern Name inte har angetts</span><span class="sxs-lookup"><span data-stu-id="ced70-1809">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="ced70-1810">Parametrarna Tag och ResourceId har lagts till i cmdleten Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="ced70-1810">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="ced70-1811">Get-AzVmssVM utan instans-ID och med InstanceView kan visa virtuella VMSS-datorer med instansvyn.</span><span class="sxs-lookup"><span data-stu-id="ced70-1811">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ced70-1812">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ced70-1812">Az.DataLakeStore</span></span>
* <span data-ttu-id="ced70-1813">Cmdletar har lagts till för uppräkning och återställning av borttagna objekt i ADL</span><span class="sxs-lookup"><span data-stu-id="ced70-1813">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="ced70-1814">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="ced70-1814">Az.EventHub</span></span>
* <span data-ttu-id="ced70-1815">Ny boolesk egenskap SkipEmptyArchives har lagts till i Skip Empty Archives i CaptureDescription-klassen i Eventhub</span><span class="sxs-lookup"><span data-stu-id="ced70-1815">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ced70-1816">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ced70-1816">Az.KeyVault</span></span>
* <span data-ttu-id="ced70-1817">Taggning i Set-AzKeyVaultSecret har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="ced70-1817">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="ced70-1818">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="ced70-1818">Az.LogicApp</span></span>
* <span data-ttu-id="ced70-1819">Grundläggande SKU har lagts till för Integrationskonton</span><span class="sxs-lookup"><span data-stu-id="ced70-1819">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="ced70-1820">XSLT 2.0, XSLT 3.0 och Flytande mappningstyper har lagts till</span><span class="sxs-lookup"><span data-stu-id="ced70-1820">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="ced70-1821">Nya cmdletar för integrationskontosammansättningar</span><span class="sxs-lookup"><span data-stu-id="ced70-1821">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="ced70-1822">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="ced70-1822">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="ced70-1823">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="ced70-1823">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="ced70-1824">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="ced70-1824">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="ced70-1825">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="ced70-1825">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="ced70-1826">Nya cmdletar för batchkonfiguration för integrationskonto</span><span class="sxs-lookup"><span data-stu-id="ced70-1826">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="ced70-1827">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="ced70-1827">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="ced70-1828">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="ced70-1828">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="ced70-1829">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="ced70-1829">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="ced70-1830">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="ced70-1830">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="ced70-1831">Logic App-SDK har uppdaterats till version 4.1.0</span><span class="sxs-lookup"><span data-stu-id="ced70-1831">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ced70-1832">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ced70-1832">Az.Monitor</span></span>
* <span data-ttu-id="ced70-1833">Hjälpen för Get-AzMetric har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="ced70-1833">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ced70-1834">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ced70-1834">Az.Network</span></span>
* <span data-ttu-id="ced70-1835">Hjälpexempel för Add-AzApplicationGatewayCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="ced70-1835">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ced70-1836">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ced70-1836">Az.OperationalInsights</span></span>
* <span data-ttu-id="ced70-1837">Ytterligare stöd för datakällorna New och Get ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="ced70-1837">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="ced70-1838">Ny ApplicationInsights-typ har lagts till för att ge stöd för ”Get specific” och ”Get all” för ApplicationInsights-datakällor för angiven arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="ced70-1838">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="ced70-1839">Cmdleten New-AzOperationalInsightsApplicationInsightsDataSource har lagts till för att skapa datakälla med angivna parametrar för Application Insights-resurs: subscription Id, resourceGroupName och name.</span><span class="sxs-lookup"><span data-stu-id="ced70-1839">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ced70-1840">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ced70-1840">Az.Resources</span></span>
* <span data-ttu-id="ced70-1841">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="ced70-1841">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="ced70-1842">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="ced70-1842">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="ced70-1843">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="ced70-1843">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="ced70-1844">Fel som gör att KeyCredentials inte kan skapas upprepade gånger har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="ced70-1844">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="ced70-1845">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ced70-1845">Az.Sql</span></span>
* <span data-ttu-id="ced70-1846">Lägg till stöd för hyperskalanivån för SQL DB</span><span class="sxs-lookup"><span data-stu-id="ced70-1846">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="ced70-1847">Ett fel har åtgärdats där återställningen kunde misslyckas på grund av onödiga inställningsegenskaper i restore-förfrågan</span><span class="sxs-lookup"><span data-stu-id="ced70-1847">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ced70-1848">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ced70-1848">Az.Websites</span></span>
* <span data-ttu-id="ced70-1849">Rätt exempel i Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="ced70-1849">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="ced70-1850">1.3.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="ced70-1850">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ced70-1851">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ced70-1851">Az.Accounts</span></span>
* <span data-ttu-id="ced70-1852">Uppdatera till den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="ced70-1852">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="ced70-1853">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ced70-1853">Az.AnalysisServices</span></span>
<span data-ttu-id="ced70-1854">Allmän tillgänglighet för Az.AnalysisServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="ced70-1854">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ced70-1855">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ced70-1855">Az.Compute</span></span>
* <span data-ttu-id="ced70-1856">AEM-tillägg: Lägg till stöd för UltraSSD-, P60-, P70- och P80-diskar</span><span class="sxs-lookup"><span data-stu-id="ced70-1856">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="ced70-1857">Uppdatera hjälpbeskrivning för Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="ced70-1857">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="ced70-1858">Uppdatera hjälpbeskrivning och exempel för Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="ced70-1858">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ced70-1859">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ced70-1859">Az.RecoveryServices</span></span>
<span data-ttu-id="ced70-1860">Allmän tillgänglighet för Az.RecoveryServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="ced70-1860">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ced70-1861">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ced70-1861">Az.Resources</span></span>
* <span data-ttu-id="ced70-1862">Korrigera taggar för resursgrupper</span><span class="sxs-lookup"><span data-stu-id="ced70-1862">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="ced70-1863">Mer information här: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="ced70-1863">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="ced70-1864">Åtgärda problem där `Get-AzureRmRoleAssignment` inte respekterar -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="ced70-1864">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="ced70-1865">Mer information här: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="ced70-1865">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="ced70-1866">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ced70-1866">Az.Sql</span></span>
* <span data-ttu-id="ced70-1867">Lägga till Get/Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="ced70-1867">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="ced70-1868">Åtgärda problem där ett nullref-undantag uppstår när du kör SQL-cmdletar och inte är inloggad på ett Azure-konto</span><span class="sxs-lookup"><span data-stu-id="ced70-1868">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="ced70-1869">Åtgärda nullref-undantag i Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="ced70-1869">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="ced70-1870">1.2.1 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="ced70-1870">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ced70-1871">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ced70-1871">Az.Accounts</span></span>
* <span data-ttu-id="ced70-1872">Version med rätt version av autentisering</span><span class="sxs-lookup"><span data-stu-id="ced70-1872">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="ced70-1873">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ced70-1873">Az.AnalysisServices</span></span>
* <span data-ttu-id="ced70-1874">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="ced70-1874">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ced70-1875">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ced70-1875">Az.RecoveryServices</span></span>
* <span data-ttu-id="ced70-1876">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="ced70-1876">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="ced70-1877">1.2.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="ced70-1877">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ced70-1878">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ced70-1878">Az.Accounts</span></span>
* <span data-ttu-id="ced70-1879">Lägga till interaktiv autentisering och autentisering med användarnamn/lösenord för endast Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="ced70-1879">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="ced70-1880">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="ced70-1880">Update incorrect online help URLs</span></span>
* <span data-ttu-id="ced70-1881">Lägga till varningsmeddelande i PS Core för Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="ced70-1881">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="ced70-1882">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="ced70-1882">Az.Aks</span></span>
* <span data-ttu-id="ced70-1883">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="ced70-1883">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ced70-1884">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ced70-1884">Az.Automation</span></span>
* <span data-ttu-id="ced70-1885">Stöd för Python 2-runbookflöden har lagts till</span><span class="sxs-lookup"><span data-stu-id="ced70-1885">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="ced70-1886">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="ced70-1886">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="ced70-1887">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="ced70-1887">Az.Cdn</span></span>
* <span data-ttu-id="ced70-1888">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="ced70-1888">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ced70-1889">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ced70-1889">Az.Compute</span></span>
* <span data-ttu-id="ced70-1890">Lägga till cmdleten Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="ced70-1890">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="ced70-1891">Lägga till TempDisk-parameter i Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ced70-1891">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="ced70-1892">Korrigera varningsmeddelande för New-AzVM</span><span class="sxs-lookup"><span data-stu-id="ced70-1892">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="ced70-1893">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ced70-1893">Az.ContainerRegistry</span></span>
* <span data-ttu-id="ced70-1894">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="ced70-1894">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ced70-1895">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ced70-1895">Az.DataFactory</span></span>
* <span data-ttu-id="ced70-1896">ADF .Net SDK-versionen har uppdaterats till 3.0.0</span><span class="sxs-lookup"><span data-stu-id="ced70-1896">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ced70-1897">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ced70-1897">Az.DataLakeStore</span></span>
* <span data-ttu-id="ced70-1898">Åtgärda problem med ADLS-slutpunkt vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="ced70-1898">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="ced70-1899">Mer information här: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="ced70-1899">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="ced70-1900">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="ced70-1900">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ced70-1901">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ced70-1901">Az.IotHub</span></span>
* <span data-ttu-id="ced70-1902">Lägga till kodningsformat i cmdleten Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="ced70-1902">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ced70-1903">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ced70-1903">Az.KeyVault</span></span>
* <span data-ttu-id="ced70-1904">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="ced70-1904">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ced70-1905">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ced70-1905">Az.Network</span></span>
* <span data-ttu-id="ced70-1906">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="ced70-1906">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="ced70-1907">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ced70-1907">Az.Resources</span></span>
* <span data-ttu-id="ced70-1908">Åtgärda felaktiga exempel i referensdokumentationen ”New-AzADAppCredential” och ”New-AzADSpCredential”</span><span class="sxs-lookup"><span data-stu-id="ced70-1908">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="ced70-1909">Åtgärda problem där sökvägen för parametern ”-TemplateFile” inte omvandlas innan cmdletarna för distribution i resursgruppen körs</span><span class="sxs-lookup"><span data-stu-id="ced70-1909">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="ced70-1910">Az.Resources: Korrigera dokumentationen om standardvärdet för New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="ced70-1910">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="ced70-1911">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="ced70-1911">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="ced70-1912">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="ced70-1912">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="ced70-1913">Åtgärda formateringsproblemet med objektet ”PSResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="ced70-1913">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="ced70-1914">Mer information här: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="ced70-1914">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ced70-1915">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ced70-1915">Az.ServiceFabric</span></span>
* <span data-ttu-id="ced70-1916">Återställ när ett certifikat läggs till i en Virtual Machine Scale Sets-modell men ett undantag genereras. Detta har gjorts för att åtgärda följande fel: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="ced70-1916">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="ced70-1917">Korrigera några felmeddelanden.</span><span class="sxs-lookup"><span data-stu-id="ced70-1917">Fix some error messages.</span></span>
* <span data-ttu-id="ced70-1918">Korrigering av skapande av kluster med ARM-mall som är standard för New-AzServiceFabriCluster som inte fungerade med migrering till Az.</span><span class="sxs-lookup"><span data-stu-id="ced70-1918">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="ced70-1919">Korrigering av tilläggning av kluster/programcertifikat så att endast VM Scale Sets som motsvarar klustret läggs till genom att kontrollera ID för klustret i tillägget.</span><span class="sxs-lookup"><span data-stu-id="ced70-1919">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="ced70-1920">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="ced70-1920">Az.SignalR</span></span>
* <span data-ttu-id="ced70-1921">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="ced70-1921">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="ced70-1922">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ced70-1922">Az.Sql</span></span>
* <span data-ttu-id="ced70-1923">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="ced70-1923">Update incorrect online help URLs</span></span>
* <span data-ttu-id="ced70-1924">Uppdaterad parameterbeskrivning för LicenseType-parameter med möjliga värden</span><span class="sxs-lookup"><span data-stu-id="ced70-1924">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="ced70-1925">Korrigering för att uppdatera hanterad instansidentitet som inte fungerar när det är den enda uppdaterade egenskapen</span><span class="sxs-lookup"><span data-stu-id="ced70-1925">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="ced70-1926">Stöd för anpassad sortering på hanterad instans</span><span class="sxs-lookup"><span data-stu-id="ced70-1926">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ced70-1927">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ced70-1927">Az.Storage</span></span>
* <span data-ttu-id="ced70-1928">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="ced70-1928">Update incorrect online help URLs</span></span>
* <span data-ttu-id="ced70-1929">Tillhandahåll detaljerat felmeddelande när en användare försöker hämta/konfigurera klassisk loggning/mått på ett Premium Storage-konto eftersom Premium Storage-kontot inte har stöd för klassisk loggning/mått.</span><span class="sxs-lookup"><span data-stu-id="ced70-1929">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="ced70-1930">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="ced70-1930">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="ced70-1931">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="ced70-1931">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="ced70-1932">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="ced70-1932">Az.TrafficManager</span></span>
* <span data-ttu-id="ced70-1933">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="ced70-1933">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ced70-1934">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ced70-1934">Az.Websites</span></span>
* <span data-ttu-id="ced70-1935">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="ced70-1935">Update incorrect online help URLs</span></span>
* <span data-ttu-id="ced70-1936">Korrigerar ”New-AzWebAppSSLBinding” så att certifikatet laddas upp till rätt resursgrupp och plats om appen finns i en ASE.</span><span class="sxs-lookup"><span data-stu-id="ced70-1936">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="ced70-1937">Korrigerar ”New-AzWebAppSSLBinding” så att taggarna inte skrivs över på en bindning av ett SSL-certifikat till en app</span><span class="sxs-lookup"><span data-stu-id="ced70-1937">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="ced70-1938">1.1.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="ced70-1938">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ced70-1939">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ced70-1939">Az.Accounts</span></span>
* <span data-ttu-id="ced70-1940">Lade till omfattningen ”Lokal” till Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="ced70-1940">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ced70-1941">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ced70-1941">Az.Compute</span></span>
* <span data-ttu-id="ced70-1942">Namn är nu valfritt i ID-parametern för Restart/Start/Stop/Remove/Set-AzVM och Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="ced70-1942">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="ced70-1943">Uppdaterade beskrivningen av ID i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="ced70-1943">Updated the description of ID in help files</span></span>
* <span data-ttu-id="ced70-1944">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ced70-1944">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ced70-1945">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ced70-1945">Az.DataLakeStore</span></span>
* <span data-ttu-id="ced70-1946">Uppdatera sdk-versionen av dataplanet till 1.1.14 för SDK-korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="ced70-1946">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="ced70-1947">Korrigerade hanteringen av negativ accesstime och modificationtime för getfilestatus och liststatus; korrigera asynkront annulleringstoken</span><span class="sxs-lookup"><span data-stu-id="ced70-1947">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="ced70-1948">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="ced70-1948">Az.EventGrid</span></span>
* <span data-ttu-id="ced70-1949">Uppdaterat för användning av API-versionen 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="ced70-1949">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="ced70-1950">Uppdaterade följande cmdletar för att stödja nytt scenario i API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="ced70-1950">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="ced70-1951">New-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="ced70-1951">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="ced70-1952">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="ced70-1952">Event Time-To-Live,</span></span>
        - <span data-ttu-id="ced70-1953">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="ced70-1953">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="ced70-1954">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="ced70-1954">Dead letter endpoint.</span></span>
    - <span data-ttu-id="ced70-1955">Update-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="ced70-1955">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="ced70-1956">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="ced70-1956">Event Time-To-Live,</span></span>
        - <span data-ttu-id="ced70-1957">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="ced70-1957">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="ced70-1958">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="ced70-1958">Dead letter endpoint.</span></span>
* <span data-ttu-id="ced70-1959">Lade till nya enum-värden (storageQueue och hybridConnection) för alternativet EndpointType i cmdletarna New-AzureRmEventGridSubscription och Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="ced70-1959">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="ced70-1960">Visa varningsmeddelanden om skapande eller uppdatering av händelseprenumerationen förväntas medföra manuell åtgärd från användaren.</span><span class="sxs-lookup"><span data-stu-id="ced70-1960">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ced70-1961">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ced70-1961">Az.IotHub</span></span>
* <span data-ttu-id="ced70-1962">Har uppdaterats till den senaste versionen av SDK:n lotHub</span><span class="sxs-lookup"><span data-stu-id="ced70-1962">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="ced70-1963">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="ced70-1963">Az.LogicApp</span></span>
* <span data-ttu-id="ced70-1964">Get-AzLogicApp visar en lista över alla som inte har angivet namn</span><span class="sxs-lookup"><span data-stu-id="ced70-1964">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="ced70-1965">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ced70-1965">Az.Resources</span></span>
* <span data-ttu-id="ced70-1966">Åtgärdade problem med parameteruppsättningen när parametrarna -ODataQuery och -ResourceId anges för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="ced70-1966">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="ced70-1967">Mer information här: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="ced70-1967">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="ced70-1968">Åtgärdade hantering av parametern -Custom i New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ced70-1968">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="ced70-1969">Korrigerade stavfel i New-AzDeployment-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="ced70-1969">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="ced70-1970">Gjorde parametern -MailNickname obligatorisk för New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="ced70-1970">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="ced70-1971">Mer information här: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="ced70-1971">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="ced70-1972">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="ced70-1972">Az.SignalR</span></span>
* <span data-ttu-id="ced70-1973">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ced70-1973">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="ced70-1974">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ced70-1974">Az.Sql</span></span>
* <span data-ttu-id="ced70-1975">Konverterade lagringshanteringsklientens beroende av den normala SDK-implementeringen.</span><span class="sxs-lookup"><span data-stu-id="ced70-1975">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ced70-1976">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ced70-1976">Az.Storage</span></span>
* <span data-ttu-id="ced70-1977">Angav StorageAccountName för lagringskontext som det verkliga namnet på lagringskontot när det skapas med Sas Token, OAuth eller Anonymous</span><span class="sxs-lookup"><span data-stu-id="ced70-1977">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="ced70-1978">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="ced70-1978">New-AzStorageContext</span></span>
* <span data-ttu-id="ced70-1979">Skapade Sas Token för Blob Snapshot-objekt med parametern -FullUri, åtgärdade den returnerade URI:n så att den blir URI för ögonblicksbild</span><span class="sxs-lookup"><span data-stu-id="ced70-1979">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="ced70-1980">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="ced70-1980">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ced70-1981">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ced70-1981">Az.Websites</span></span>
* <span data-ttu-id="ced70-1982">Åtgärdade en bugg i datumparsningen i Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="ced70-1982">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="ced70-1983">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ced70-1983">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="ced70-1984">1.0.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="ced70-1984">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="ced70-1985">Allmänt</span><span class="sxs-lookup"><span data-stu-id="ced70-1985">General</span></span>

- <span data-ttu-id="ced70-1986">Allmän tillgänglighet för Az-modulen</span><span class="sxs-lookup"><span data-stu-id="ced70-1986">General Availability of Az Module</span></span>
- <span data-ttu-id="ced70-1987">Onlinehjälp för varje modul</span><span class="sxs-lookup"><span data-stu-id="ced70-1987">Online help for each module</span></span>
- <span data-ttu-id="ced70-1988">Mer information och en översikt finns på [Az-informationssidan](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="ced70-1988">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="ced70-1989">Information om hur du migrerar från AzureRM finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ced70-1989">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="ced70-1990">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ced70-1990">Az.Accounts</span></span>
- <span data-ttu-id="ced70-1991">Har ändrats från Az.Profile</span><span class="sxs-lookup"><span data-stu-id="ced70-1991">Changed from Az.Profile</span></span>
- <span data-ttu-id="ced70-1992">Fasta tabellformat för profil- och kontexttyper</span><span class="sxs-lookup"><span data-stu-id="ced70-1992">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="ced70-1993">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ced70-1993">Az.ApiManagement</span></span>
- <span data-ttu-id="ced70-1994">Korrigeringar för #7002</span><span class="sxs-lookup"><span data-stu-id="ced70-1994">Fixes for #7002</span></span>
- <span data-ttu-id="ced70-1995">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ced70-1995">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="ced70-1996">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="ced70-1996">Az.Batch</span></span>
- <span data-ttu-id="ced70-1997">Lade till möjligheten att se vilken version av Azure Batch Node Agent som körs på var och en av de virtuella datorerna i en pool, via den nya egenskapen `NodeAgentInformation` på `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="ced70-1997">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="ced70-1998">Standarden `Caching` för `PSDataDisk` är nu `ReadWrite` i stället för `None`.</span><span class="sxs-lookup"><span data-stu-id="ced70-1998">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="ced70-1999">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ced70-1999">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="ced70-2000">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="ced70-2000">Az.Billing</span></span>
- <span data-ttu-id="ced70-2001">Kombinerar cmdletarna för fakturering, förbrukning och UsageAggregates. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ced70-2001">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="ced70-2002">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="ced70-2002">Az.CognitivServices</span></span>
- <span data-ttu-id="ced70-2003">Lade till kompletterare för SkuName och Typem som är tillgängliga i New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="ced70-2003">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="ced70-2004">Tog bort parameteruppsättningen GetSkusWithAccountParamSetName från Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="ced70-2004">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="ced70-2005">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="ced70-2005">Az.ContainerInstance</span></span>
- <span data-ttu-id="ced70-2006">Stöd för ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="ced70-2006">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="ced70-2007">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="ced70-2007">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="ced70-2008">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ced70-2008">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="ced70-2009">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ced70-2009">Az.DataLakeStore</span></span>
- <span data-ttu-id="ced70-2010">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ced70-2010">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="ced70-2011">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ced70-2011">Az.Monitor</span></span>
- <span data-ttu-id="ced70-2012">Döpte om Az.Insights till Az.Monitor och andra mindre icke-bakåtkompatibla ändringar. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ced70-2012">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="ced70-2013">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ced70-2013">Az.KeyVault</span></span>
- <span data-ttu-id="ced70-2014">Tog bort den inaktuella egenskapen PurgeDisabled från utdatatyper</span><span class="sxs-lookup"><span data-stu-id="ced70-2014">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="ced70-2015">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="ced70-2015">Az.MachineLearning</span></span>
- <span data-ttu-id="ced70-2016">Inkluderade cmdletarna från modulen Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="ced70-2016">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="ced70-2017">Az.Media</span><span class="sxs-lookup"><span data-stu-id="ced70-2017">Az.Media</span></span>
- <span data-ttu-id="ced70-2018">Tog bort inaktuella -Tags-alias från New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="ced70-2018">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="ced70-2019">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ced70-2019">Az.Network</span></span>
<span data-ttu-id="ced70-2020">Stöd har lagts till för konfiguration av RewriteRuleSets i Application Gateway</span><span class="sxs-lookup"><span data-stu-id="ced70-2020">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="ced70-2021">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="ced70-2021">New cmdlets added:</span></span>
        - <span data-ttu-id="ced70-2022">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ced70-2022">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="ced70-2023">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ced70-2023">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="ced70-2024">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ced70-2024">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="ced70-2025">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ced70-2025">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="ced70-2026">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ced70-2026">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="ced70-2027">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="ced70-2027">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="ced70-2028">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="ced70-2028">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="ced70-2029">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="ced70-2029">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="ced70-2030">Cmdletar har uppdaterats med den valfria parametern -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ced70-2030">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="ced70-2031">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ced70-2031">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="ced70-2032">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="ced70-2032">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="ced70-2033">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="ced70-2033">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="ced70-2034">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ced70-2034">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="ced70-2035">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="ced70-2035">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="ced70-2036">New-AzureRmApplicationGatewayUrlPathMapConfig har lagt till KeyVault-stöd för Application Gateway med Identity.</span><span class="sxs-lookup"><span data-stu-id="ced70-2036">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="ced70-2037">Cmdletar har uppdaterats med den valfria parametern -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="ced70-2037">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="ced70-2038">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ced70-2038">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="ced70-2039">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ced70-2039">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="ced70-2040">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ced70-2040">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="ced70-2041">Cmdleten New-AzApplicationGateway har uppdaterats med den valfria parametern -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="ced70-2041">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="ced70-2042">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ced70-2042">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="ced70-2043">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ced70-2043">Az.OperationalInsights</span></span>
- <span data-ttu-id="ced70-2044">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ced70-2044">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="ced70-2045">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="ced70-2045">Az.Profile</span></span>
- <span data-ttu-id="ced70-2046">Modulnamnet har ändrats till Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ced70-2046">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="ced70-2047">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ced70-2047">Az.RecoveryServices</span></span>
- <span data-ttu-id="ced70-2048">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ced70-2048">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="ced70-2049">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ced70-2049">Az.Resources</span></span>
- <span data-ttu-id="ced70-2050">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ced70-2050">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="ced70-2051">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ced70-2051">Az.ServiceFabric</span></span>
- <span data-ttu-id="ced70-2052">Stöd för specificering av certifikat efter eget namn och tumavtryck</span><span class="sxs-lookup"><span data-stu-id="ced70-2052">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="ced70-2053">Information om fler icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ced70-2053">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="ced70-2054">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="ced70-2054">Az.SIgnalR</span></span>
- <span data-ttu-id="ced70-2055">Allmän tillgänglighet för PowerShell-cmdletar för SIgnalR</span><span class="sxs-lookup"><span data-stu-id="ced70-2055">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="ced70-2056">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ced70-2056">Az.Sql</span></span>
- <span data-ttu-id="ced70-2057">Lade till de nya identifieringstyperna Data_Exfiltration och Unsafe_Action i Threat Detection-cmdletar</span><span class="sxs-lookup"><span data-stu-id="ced70-2057">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="ced70-2058">Uppdaterade dokumentationsexempel för Sql Auditing-cmdletar</span><span class="sxs-lookup"><span data-stu-id="ced70-2058">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="ced70-2059">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ced70-2059">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="ced70-2060">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ced70-2060">Az.Storage</span></span>
- <span data-ttu-id="ced70-2061">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ced70-2061">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="ced70-2062">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ced70-2062">Az.Websites</span></span>
- <span data-ttu-id="ced70-2063">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ced70-2063">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="ced70-2064">0.7.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="ced70-2064">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="ced70-2065">Allmänt</span><span class="sxs-lookup"><span data-stu-id="ced70-2065">General</span></span>

* <span data-ttu-id="ced70-2066">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="ced70-2066">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="ced70-2067">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ced70-2067">Az.Compute</span></span>

* <span data-ttu-id="ced70-2068">Lade till stöd för UltraSSD och Galleriavbildningar i de enkla parameteruppsättningarna för `New-AzVm(ss)`-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="ced70-2068">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="ced70-2069">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ced70-2069">Az.DataLakeStore</span></span>

* <span data-ttu-id="ced70-2070">Åtgärdade avslutande snedstreck i domänen för adls-konto</span><span class="sxs-lookup"><span data-stu-id="ced70-2070">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="ced70-2071">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="ced70-2071">Az.FrontDoor</span></span>

* <span data-ttu-id="ced70-2072">Brutna länkar korrigerades</span><span class="sxs-lookup"><span data-stu-id="ced70-2072">Fixed some broken links</span></span>
    - <span data-ttu-id="ced70-2073">I artiklarna New-AzureRmFrontDoor och Set-AzureRmFrontDoor artiklar korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="ced70-2073">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="ced70-2074">I artikeln New-AzureRmFrontDoorManagedRuleObject korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="ced70-2074">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="ced70-2075">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ced70-2075">Az.RecoveryServices</span></span>

* <span data-ttu-id="ced70-2076">Lade till valideringar på klientsidan för Azure-filresurs med återställningsåtgärder.</span><span class="sxs-lookup"><span data-stu-id="ced70-2076">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="ced70-2077">Gjorde storageAccountName och storageAccountResourceGroupName valfritt för afs-återställning.</span><span class="sxs-lookup"><span data-stu-id="ced70-2077">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="ced70-2078">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ced70-2078">Az.Resources</span></span>

* <span data-ttu-id="ced70-2079">Korrigering för https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="ced70-2079">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="ced70-2080">Uppdaterade Get-AzureRmRoleAssignment så att prenumerationsomfattningen används om den anges vid begäran om klassiska administratörer.</span><span class="sxs-lookup"><span data-stu-id="ced70-2080">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="ced70-2081">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ced70-2081">Az.Sql</span></span>

* <span data-ttu-id="ced70-2082">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="ced70-2082">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="ced70-2083">Korrigerade ett problem med Get-AzureRmSqlDatabaseVulnerabilityAssessment med DotNet-kärna</span><span class="sxs-lookup"><span data-stu-id="ced70-2083">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="ced70-2084">Ändrade dokumentationen för hjälpmeddelanden som rör SQL Auditing-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="ced70-2084">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="ced70-2085">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ced70-2085">Az.Storage</span></span>

* <span data-ttu-id="ced70-2086">Lade till -EnableHierarchicalNamespace i New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ced70-2086">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="ced70-2087">Åtgärdade problemet med att cmdleten Copy File inte kunde återanvända källkontexten på målet om inte -DestContext angetts</span><span class="sxs-lookup"><span data-stu-id="ced70-2087">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="ced70-2088">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="ced70-2088">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="ced70-2089">Stöd för statisk webbplatskonfiguration</span><span class="sxs-lookup"><span data-stu-id="ced70-2089">Support Static Website configuration</span></span>
    - <span data-ttu-id="ced70-2090">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="ced70-2090">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="ced70-2091">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="ced70-2091">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="ced70-2092">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ced70-2092">Az.Websites</span></span>

* <span data-ttu-id="ced70-2093">Set-AzureRmWebApp och Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ced70-2093">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="ced70-2094">Ny parameter (-AzureStoragePath) har lagts till för att ange att Azure Storage-sökvägar ska monteras i containerappar i Windows och Linux.</span><span class="sxs-lookup"><span data-stu-id="ced70-2094">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="ced70-2095">Använder utdata från den nya cmdleten New-AzureRmWebAppAzureStoragePath som en parameter för att ange sökvägar för Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="ced70-2095">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="ced70-2096">0.6.1 – november 2018</span><span class="sxs-lookup"><span data-stu-id="ced70-2096">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="ced70-2097">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ced70-2097">Az.ApiManagement</span></span>
* <span data-ttu-id="ced70-2098">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="ced70-2098">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="ced70-2099">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ced70-2099">Az.Automation</span></span>
* <span data-ttu-id="ced70-2100">Swagger baserade Azure Automation-cmdletar</span><span class="sxs-lookup"><span data-stu-id="ced70-2100">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="ced70-2101">Cmdletar för Uppdateringshantering har lagts till</span><span class="sxs-lookup"><span data-stu-id="ced70-2101">Added Update Management cmdlets</span></span>
* <span data-ttu-id="ced70-2102">Cmdletar för källkontroll har lagts till</span><span class="sxs-lookup"><span data-stu-id="ced70-2102">Added Source Control cmdlets</span></span>
* <span data-ttu-id="ced70-2103">Remove-AzureRmAutomationHybridWorkerGroup-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="ced70-2103">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="ced70-2104">Kommandot för DSC-registreringsnod har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="ced70-2104">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="ced70-2105">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ced70-2105">Az.Compute</span></span>
* <span data-ttu-id="ced70-2106">Problem med SystemAssigned-identitet har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="ced70-2106">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="ced70-2107">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="ced70-2107">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="ced70-2108">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="ced70-2108">Az.ContainerInstance</span></span>
* <span data-ttu-id="ced70-2109">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="ced70-2109">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="ced70-2110">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="ced70-2110">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="ced70-2111">uppdatera exempelbeskrivningen för marketplace-cmdletar</span><span class="sxs-lookup"><span data-stu-id="ced70-2111">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="ced70-2112">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ced70-2112">Az.Network</span></span>
* <span data-ttu-id="ced70-2113">Cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomErreller Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="ced70-2113">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="ced70-2114">ICMP tillbaka till stöd för Azure Firewall-nätverksprotokoll har lagts till</span><span class="sxs-lookup"><span data-stu-id="ced70-2114">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="ced70-2115">Uppdatera cmdlet Test-AzureRmNetworkWatcherConnectivity, lägga till verifiering av mål-id, adress och port.</span><span class="sxs-lookup"><span data-stu-id="ced70-2115">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="ced70-2116">Åtgärda problem med minnesanvändning i VirtualNetwork-karta</span><span class="sxs-lookup"><span data-stu-id="ced70-2116">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="ced70-2117">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="ced70-2117">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="ced70-2118">Åtgärda för att ändra principen för en skyddad fildelning.</span><span class="sxs-lookup"><span data-stu-id="ced70-2118">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="ced70-2119">Tidszonsprincipen har konverterats till versaler.</span><span class="sxs-lookup"><span data-stu-id="ced70-2119">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="ced70-2120">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="ced70-2120">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="ced70-2121">Exempel i New-AzureRmRecoveryServicesAsrProtectableItem har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="ced70-2121">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="ced70-2122">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="ced70-2122">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="ced70-2123">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="ced70-2123">Az.Relay</span></span>
* <span data-ttu-id="ced70-2124">Valfri parameter -KeyValue till New-AzureRmRelayKey cmdlet har lagts till, vilket gör det möjligt för användare att tillhandahålla KeyValue.</span><span class="sxs-lookup"><span data-stu-id="ced70-2124">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="ced70-2125">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ced70-2125">Az.Resources</span></span>
* <span data-ttu-id="ced70-2126">Uppdatera hjälpdokumentation för resursidentitet kopplad till parametrar i `New-AzureRmPolicyAssignment` och `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="ced70-2126">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="ced70-2127">Lägg till ett exempel för New-AzureRmPolicyDefinition som använder -Metadata</span><span class="sxs-lookup"><span data-stu-id="ced70-2127">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="ced70-2128">Korrigera så att skiftläge behålls i taggnycklar i NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="ced70-2128">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="ced70-2129">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ced70-2129">Az.ServiceFabric</span></span>
* <span data-ttu-id="ced70-2130">Lägg till utfasningsmeddelanden för kommande icke-kompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="ced70-2130">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="ced70-2131">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ced70-2131">Az.Sql</span></span>
* <span data-ttu-id="ced70-2132">Nya cmdletar för CRUD-åtgärder på Azure Sql Database-hanterad instans och Azure Sql-hanterad databas</span><span class="sxs-lookup"><span data-stu-id="ced70-2132">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="ced70-2133">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="ced70-2133">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="ced70-2134">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="ced70-2134">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="ced70-2135">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="ced70-2135">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="ced70-2136">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="ced70-2136">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="ced70-2137">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="ced70-2137">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="ced70-2138">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="ced70-2138">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="ced70-2139">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="ced70-2139">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="ced70-2140">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="ced70-2140">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="ced70-2141">Hantering av utökad granskningsprincip på en server eller en databas har aktiverats.</span><span class="sxs-lookup"><span data-stu-id="ced70-2141">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="ced70-2142">Ny parameter (PredicateExpression) har lagts till för att aktivera filtrering av granskningsloggar.</span><span class="sxs-lookup"><span data-stu-id="ced70-2142">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="ced70-2143">Cmdletar har ändrats så att de använder SQL-klienter i stället för äldre klienter.</span><span class="sxs-lookup"><span data-stu-id="ced70-2143">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="ced70-2144">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="ced70-2144">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="ced70-2145">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="ced70-2145">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="ced70-2146">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="ced70-2146">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="ced70-2147">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="ced70-2147">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="ced70-2148">Problem med att använda Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings med lagringskontots namnparameter har korrigerats</span><span class="sxs-lookup"><span data-stu-id="ced70-2148">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="ced70-2149">0.5.0 – november 2018</span><span class="sxs-lookup"><span data-stu-id="ced70-2149">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="ced70-2150">Allmänt</span><span class="sxs-lookup"><span data-stu-id="ced70-2150">General</span></span>
* <span data-ttu-id="ced70-2151">Lade till resurskompletterare till många kärn-cmdletar – dessa gör att du kan stega genom befintliga resursnamn med TABB vid interaktiva anrop till cmdletar</span><span class="sxs-lookup"><span data-stu-id="ced70-2151">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="ced70-2152">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="ced70-2152">Az.Profile</span></span>
* <span data-ttu-id="ced70-2153">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="ced70-2153">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="ced70-2154">Bytte namn på parametern TenantId i cmdleten Connect-AzAccount till Tenant och lade till ett alias för TenantId</span><span class="sxs-lookup"><span data-stu-id="ced70-2154">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="ced70-2155">Uppdaterade TenantId-beskrivningen för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="ced70-2155">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="ced70-2156">Åtgärda felmeddelande för misslyckad inloggning när du tillhandahåller klientdomän</span><span class="sxs-lookup"><span data-stu-id="ced70-2156">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="ced70-2157">Åtgärda problem med att kontextnamn hamnar i konflikt för konton utan prenumerationer i klientorganisationen</span><span class="sxs-lookup"><span data-stu-id="ced70-2157">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="ced70-2158">Åtgärda problem med DataLake-slutpunkter vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="ced70-2158">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="ced70-2159">Åtgärdade problem med att Disconnect-AzAccount kastades om den inte anslöts</span><span class="sxs-lookup"><span data-stu-id="ced70-2159">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="ced70-2160">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ced70-2160">Az.CognitiveServices</span></span>
* <span data-ttu-id="ced70-2161">Lade till åtgärden Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="ced70-2161">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ced70-2162">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ced70-2162">Az.Compute</span></span>
* <span data-ttu-id="ced70-2163">Lade till cmdletarna Add-AzVmssVMDataDisk och Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="ced70-2163">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="ced70-2164">Get-AzVMImage visar AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="ced70-2164">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="ced70-2165">Åtgärdade att värdena för alternativen SetAzVMChefExtension -BootstrapOptions och -JsonAttribute inte angavs i json-format.</span><span class="sxs-lookup"><span data-stu-id="ced70-2165">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ced70-2166">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ced70-2166">Az.DataLakeStore</span></span>
* <span data-ttu-id="ced70-2167">Uppdatera DataLake-paketet till 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="ced70-2167">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="ced70-2168">Lägg till standardsamtidighet för flertrådade åtgärder.</span><span class="sxs-lookup"><span data-stu-id="ced70-2168">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="ced70-2169">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="ced70-2169">Az.Insights</span></span>
* <span data-ttu-id="ced70-2170">Åtgärdade problem #7267 (autoskalningsområde)</span><span class="sxs-lookup"><span data-stu-id="ced70-2170">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="ced70-2171">Problem med att uppräknade parametrar inte ställdes in ordentligt när du skapade en ny autoskalningsregel (de ställdes alltid in med standardvärdet).</span><span class="sxs-lookup"><span data-stu-id="ced70-2171">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="ced70-2172">Åtgärdade problem #7513 [Insights] Set-AzDiagnosticSetting kräver uttrycklig specifikation av kategorier när inställningar skapas</span><span class="sxs-lookup"><span data-stu-id="ced70-2172">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="ced70-2173">Nu kräver inte cmdleten uttrycklig anvisning av kategorierna för att aktiveras under skapande, d.v.s. den fungerar enligt beskrivning</span><span class="sxs-lookup"><span data-stu-id="ced70-2173">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ced70-2174">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ced70-2174">Az.Network</span></span>
* <span data-ttu-id="ced70-2175">PeeringType ändrades till en obligatorisk parameter för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="ced70-2175">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="ced70-2176">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="ced70-2176">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="ced70-2177">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="ced70-2177">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="ced70-2178">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="ced70-2178">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="ced70-2179">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="ced70-2179">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="ced70-2180">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="ced70-2180">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="ced70-2181">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="ced70-2181">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="ced70-2182">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ced70-2182">Az.PolicyInsights</span></span>
* <span data-ttu-id="ced70-2183">Cmdletar för principreparation har lagts till</span><span class="sxs-lookup"><span data-stu-id="ced70-2183">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="ced70-2184">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ced70-2184">Az.Resources</span></span>
* <span data-ttu-id="ced70-2185">Korrigering för https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="ced70-2185">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="ced70-2186">Tillåt att resurser listas med parametern -ResourceId för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="ced70-2186">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="ced70-2187">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ced70-2187">Az.ServiceBus</span></span>
* <span data-ttu-id="ced70-2188">Skrivskyddad MigrationState-egenskap har lagts till i PSServiceBusMigrationConfigurationAttributes, som hjälper till att hålla koll på migreringstillståndet.</span><span class="sxs-lookup"><span data-stu-id="ced70-2188">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ced70-2189">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ced70-2189">Az.ServiceFabric</span></span>
* <span data-ttu-id="ced70-2190">Åtgärda att lägga till certifikat till Linux-Vmss.</span><span class="sxs-lookup"><span data-stu-id="ced70-2190">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="ced70-2191">Åtgärdade Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="ced70-2191">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="ced70-2192">Använd rätt tumavtryck från nya certifikat (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="ced70-2192">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="ced70-2193">Visa undantag korrekt (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="ced70-2193">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="ced70-2194">Åtgärdade Update-AzServiceFabricDurability så att klusterkonfigurationen uppdateras innan Vmss-åtgärden CreateOrUpdate påbörjas.</span><span class="sxs-lookup"><span data-stu-id="ced70-2194">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="ced70-2195">0.4.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="ced70-2195">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="ced70-2196">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="ced70-2196">Az.Profile</span></span>
* <span data-ttu-id="ced70-2197">Åtgärdade problemet med Get-AzSubscription i CloudShell</span><span class="sxs-lookup"><span data-stu-id="ced70-2197">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="ced70-2198">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="ced70-2198">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ced70-2199">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ced70-2199">Az.Compute</span></span>
* <span data-ttu-id="ced70-2200">Nya storlekar lades till i listan över godkända VM-storlekar för vilka accelererat nätverk kommer att aktiveras vid användning av den enkla parameteruppsättningen för New-AzVm</span><span class="sxs-lookup"><span data-stu-id="ced70-2200">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="ced70-2201">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="ced70-2201">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ced70-2202">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ced70-2202">Az.DataLakeStore</span></span>
* <span data-ttu-id="ced70-2203">Lägger till stöd för regler för virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="ced70-2203">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="ced70-2204">Get-AzDataLakeStoreVirtualNetworkRule: Hämtar eller listar regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ced70-2204">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="ced70-2205">Add-AzDataLakeStoreVirtualNetworkRule: Lägger till en regel för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="ced70-2205">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="ced70-2206">Set-AzDataLakeStoreVirtualNetworkRule: Ändrar den angivna regeln för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="ced70-2206">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="ced70-2207">Remove-AzDataLakeStoreVirtualNetworkRule: Tar bort en regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ced70-2207">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ced70-2208">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ced70-2208">Az.Network</span></span>
* <span data-ttu-id="ced70-2209">Skicka protokollvärdet till serverdelen för att uppdatera cmdleten Test-AzNetworkWatcherConnectivity.</span><span class="sxs-lookup"><span data-stu-id="ced70-2209">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="ced70-2210">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="ced70-2210">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ced70-2211">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ced70-2211">Az.Resources</span></span>
* <span data-ttu-id="ced70-2212">Åtgärdade problem där Get-AzRoleDefinition genererar ett oläsligt undantag (när standardprofilen inte innehåller någon prenumeration och ingen omfattning har angetts) genom att lägga till ett beskrivande undantag i scenariot.</span><span class="sxs-lookup"><span data-stu-id="ced70-2212">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="ced70-2213">Ställ in ”RoleDefinitionNameParameterSet” som standardparameteruppsättning.</span><span class="sxs-lookup"><span data-stu-id="ced70-2213">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="ced70-2214">0.3.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="ced70-2214">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="ced70-2215">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="ced70-2215">Azure.Storage</span></span>
* <span data-ttu-id="ced70-2216">Åtgärda fel där Kopiera blob/fil inte kopierar metadata när målplatsen har ett problem med metadata</span><span class="sxs-lookup"><span data-stu-id="ced70-2216">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="ced70-2217">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="ced70-2217">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="ced70-2218">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="ced70-2218">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="ced70-2219">Stöd för att hämta användningsinformation om en Storage-resurs för en specifik plats och för att lägga till ett varningsmeddelande för att hämta användningsinformation om en global Storage-resurs är inaktuellt.</span><span class="sxs-lookup"><span data-stu-id="ced70-2219">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="ced70-2220">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="ced70-2220">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="ced70-2221">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ced70-2221">Az.CognitiveServices</span></span>
* <span data-ttu-id="ced70-2222">Stöd för Get-AzCognitiveServicesAccountSkus utan ett befintligt konto.</span><span class="sxs-lookup"><span data-stu-id="ced70-2222">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ced70-2223">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ced70-2223">Az.Compute</span></span>
* <span data-ttu-id="ced70-2224">Åtgärdade fel där Get-AzVM -ResourceGroupName <rg> returnerar fler än 50 resultat om det behövs</span><span class="sxs-lookup"><span data-stu-id="ced70-2224">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="ced70-2225">Lade till ett exempel för SimpleParameterSet i hjälpen för cmdleten New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="ced70-2225">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="ced70-2226">Ett stavfel i förloppsmeddelandet för Azure Disk Encryption har korrigerats</span><span class="sxs-lookup"><span data-stu-id="ced70-2226">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="ced70-2227">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ced70-2227">Az.DataFactoryV2</span></span>
* <span data-ttu-id="ced70-2228">ADF .Net SDK-versionen har uppdaterats till 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="ced70-2228">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ced70-2229">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ced70-2229">Az.Network</span></span>
* <span data-ttu-id="ced70-2230">Funktionalitet för NetworkProfile har lagts till.</span><span class="sxs-lookup"><span data-stu-id="ced70-2230">Added NetworkProfile functionality.</span></span> <span data-ttu-id="ced70-2231">nya cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="ced70-2231">new cmdlets added</span></span>
    - <span data-ttu-id="ced70-2232">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ced70-2232">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="ced70-2233">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ced70-2233">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="ced70-2234">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ced70-2234">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="ced70-2235">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ced70-2235">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="ced70-2236">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="ced70-2236">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="ced70-2237">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="ced70-2237">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="ced70-2238">Länk för tjänstassociering på modell för undernät har lagts till</span><span class="sxs-lookup"><span data-stu-id="ced70-2238">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="ced70-2239">Cmdletarna New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap och Remove-AzVirtualNetworkTap har lagts till</span><span class="sxs-lookup"><span data-stu-id="ced70-2239">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="ced70-2240">Cmdletarna Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig och Remove-AzNEtworkInterfaceTapConfig har lagts till</span><span class="sxs-lookup"><span data-stu-id="ced70-2240">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="ced70-2241">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="ced70-2241">Az.RedisCache</span></span>
* <span data-ttu-id="ced70-2242">Tillåt att alla strängar används som storleksparametrar framöver.</span><span class="sxs-lookup"><span data-stu-id="ced70-2242">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="ced70-2243">Lägg till P5 i popup-fönstret PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="ced70-2243">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="ced70-2244">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ced70-2244">Az.Resources</span></span>
* <span data-ttu-id="ced70-2245">Parametern -Mode som saknades i Set-AzPolicyDefinition har lagts till</span><span class="sxs-lookup"><span data-stu-id="ced70-2245">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="ced70-2246">Åtgärdade buggen för cmdleten Get-AzProviderOperation för åtgärder med ursprung som innehåller användare</span><span class="sxs-lookup"><span data-stu-id="ced70-2246">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="ced70-2247">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ced70-2247">Az.Sql</span></span>
* <span data-ttu-id="ced70-2248">Ett problem där vissa cmdletar för säkerhetskopiering inte kunde identifiera den aktuella azure-prenumerationen har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="ced70-2248">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ced70-2249">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ced70-2249">Az.Websites</span></span>
* <span data-ttu-id="ced70-2250">Ny cmdlet: Get-AzWebAppContainerContinuousDeploymentUrl – Hämtar webhook-URL:en för kontinuerlig distribution av container</span><span class="sxs-lookup"><span data-stu-id="ced70-2250">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="ced70-2251">Nya cmdletar: New-AzWebAppContainerPSSession och Enter-WebAppContainerPSSession – Startar en PowerShell-fjärrsession i en containerapp för windows</span><span class="sxs-lookup"><span data-stu-id="ced70-2251">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="ced70-2252">0.2.0 – september 2018</span><span class="sxs-lookup"><span data-stu-id="ced70-2252">0.2.0 - September 2018</span></span>
 <span data-ttu-id="ced70-2253">Första versionen</span><span class="sxs-lookup"><span data-stu-id="ced70-2253">Initial Release</span></span>
